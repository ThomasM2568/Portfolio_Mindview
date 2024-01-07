# SAÉ 5.02 : Piloter un projet informatique
###  AC33.06 : Sécuriser l'environnement numérique d'une application
### Contexte de la Saé
<br/>
L'objectif de cette Saé est de définir les exigences d'un réseau sécurisé d'hôpital en termes de sécurité et de réaliser les tâches de configurations liées à la sécurisation du système informatique. 
Compte tenu des récentes attaques cyberet de la sensibilité des données médicales, il est essentiel de mettre en place une infrastructure informatique robuste et sécurisée. Le projet consistera à créer une architecture
réseau cloisonnée, à sécuriser l'accès aux données médicales, à établir une connexion VPN avec un autre hôpital, et à documenter l'ensemble du système.


<br/>Pour justifier que je suis compétent pour l'AC33.04, j'ai choisi de présenter :
-  la configuration d'une access-list sur un routeur Cisco.
-  la photographie de l'installation de deux switch et d'un pare-feu.
-  la configuration de règles de pare-feu.
-  la schéma d'une DMZ.
-  l'organisation du réseau en VLAN.

Vous retrouverez les liens de ces documents dans la section liens en bas de cette page.

#### Trace 1 : Configuration d'access-list sur les routeurs cisco
<br/>

Une access list est un ensemble de règles qui détermine quels types de trafic réseau sont autorisés ou bloqués. Elles sont utilisées pour filtrer le trafic en fonction de critères comme les adresses IP source ou destination ou les ports utilisés.

La configuration d'access list sur nos routeurs Cisco montre que je suis capable sécuriser les environnements numériques. En définissant des règles de filtrage, je suis capable de restreindre l'accès au réseau et donc de limiter de potentiels accès indésirables. La configuration ci-dessous démontre ma maîtrise de la notion.
<br/>

```
ip access-list extended AKAT-ACL
!--- Local admin subnet to all admin subnets
permit ip 10.0.10.0 0.0.0.255 10.1.10.0 0.0.0.255
permit ip 10.0.10.0 0.0.0.255 10.0.10.0 0.0.0.255

!--- Deny all subnets to admin subnet
deny ip 10.0.0.0 0.0.255.255 10.1.10.0 0.0.0.255
deny ip 10.0.0.0 0.0.255.255 10.0.10.0 0.0.0.255

!--- All subnets to server
permit ip 10.0.0.0 0.0.255.255 10.0.50.0 0.0.0.3
permit ip 10.0.50.0 0.0.0.3 10.0.0.0 0.0.255.255
permit udp any 10.0.50.0 0.0.0.3
permit udp 10.0.50.0 0.0.0.3 10.0.0.0 0.0.255.255
permit udp any host 10.0.50.1 eq 67
permit udp host 10.0.50.1 eq 67 any
permit udp any host 10.0.50.2 eq 67
permit udp host 10.0.50.2 eq 67 any
permit udp any host 10.0.50.1 eq 68
permit udp host 10.0.50.1 eq 68 any
permit udp any host 10.0.50.2 eq 68
permit udp host 10.0.50.2 eq 68 any
permit any 255.255.255.255
permit 255.255.255.255 any

!--- IOT subnet to database
permit ip 10.0.90.0 0.0.0.255 host 10.0.50.3
permit ip 10.0.90.0 0.0.0.255 host 10.0.50.4
permit ip 10.0.90.0 0.0.0.255 host 10.0.50.5
permit ip 10.0.90.0 0.0.0.255 host 10.0.50.6
permit ip 10.0.90.0 0.0.0.255 host 10.0.50.7
permit ip 10.0.90.0 0.0.0.255 host 10.0.50.8
permit ip 10.0.90.0 0.0.0.255 host 10.1.50.3
permit ip 10.0.90.0 0.0.0.255 host 10.1.50.4
permit ip 10.0.90.0 0.0.0.255 host 10.1.50.5

!--- Deny all
deny ip any any
```

<br/>

#### Trace 2.X : Pare-feu

<br/>
Le but d'un pare-feu est d'analyser le trafic réseau entrant et sortant en fonction de règles que l'on configure. Cela se fait en se basant sur des critères tels que les adresses IP source et destination ou le type de protocole par exemple.
On peut par exemple exposer un serveur web sur Internet via l'utilisation du port DMZ du pare-feu stormshield en le sécurisant via un ensemble de règles, en autorisant que les fluxs HTTP et HTTPS. Les autres types de trafics vers le serveur web seront donc bloqués.
Le pare-feu renforce donc la sécurité du réseau.


J'ai installé un pare-feu stormshield sur notre réseau, celui-ci est branché sur des routeurs et est en bordure d'Internet.
J'ai défini un ensemble de règles séparées logiquement par des sections. Le but de celles-ci est de permettre une meilleure organisation des lignes de configuration en les séparer visuellement.
J'ai défini plusieurs sections qui respectent les mêmes conventions de nommage (Source_vers_Destination)

| Nom de la section | Source | Destination |
|----------|----------|----------|
| Dist_vers_Net | Réseaux distants | Réseaux internes |
| Any_vers_Net | Tous les réseaux | DMZ |
| Net_vers_Dist | Réseaux internes | Réseaux distants |
| Block_all | Tous les réseaux | Tous les réseaux |

Il faut savoir que le fonctionnement des règles est hiérarchique, c'est-à-dire que les règles sont vérifiées une par une. La première qui correspond est utilisée.
Il est donc important de ne pas oublier de préciser une règle pour bloquer tout le trafic qui n'a pas été explicitement autorisé.


La configuration de règles de pare-feu (Stormshield) montre que je suis capable sécuriser les environnements numériques. En définissant des règles, je suis capable de restreindre l'accès au réseau et donc de limiter de potentiels accès indésirables. La configuration ci-dessous démontre ma maîtrise de la notion.
<br/>


#### Trace 3 : Schéma d'une DMZ

<br/>
Le but d'une DMZ (zone démilitarisée) est d'être une zone intermédiaire entre le réseau interne et le réseau externe, généralement représenté par Internet. 
En isolant certaines parties du réseau, on améliore la sécurité du réseau.
De plus, lorsqu'on expose des serveurs sur Internet, il est crucial de sécuriser d'avantage la zone dans laquelle ils se trouvent pour limiter les attaques de l'extérieur comme de l'intérieur.
<br/>
J'ai schématisé la DMZ mise en place durant cette Saé, le but était d'isoler nos serveurs web du réseau interne, les rendants ainsi accessibles depuis Internet sans compromettre la sécurité du réseau Interne.
<br/>

#### Trace 4 : Séparation du réseau en VLAN
<br/>
Les VLANs (Virtual Local Area Network) sont des groupes permettant ainsi de segmenter et de cloisonner un réseau physique en plusieurs réseaux virtuels. 
<br/>
Afin d’améliorer la sécurité et faciliter l’administration du réseau j'ai créé plusieurs VLANs. 
Avec des VLAN, l'accès d'une zone à l'autre est impossible ce qui limite l'accès aux données sensibles au personnel autorisé. 
Par exemple, cela évite qu'une personne de l'administration accède à des données de recherches.<br/>

<br/>
Ainsi j'ai créé 8 VLANs :<br/>

| Numéro de VLAN | Objectif |
|----------------|----------|
| 1 | Liaisons Pare-feu/Routeurs |
| 10 | Administration du réseau. |
| 20 | VLAN DMZ (Une DMZ (zone démilitarisée) est une zone réseau intermédiaire entre un réseau interne sécurisé et un réseau externe non sécurisé, utilisée pour héberger des services accessibles depuis Internet tout en isolant le réseau interne des menaces potentielles.). Ici la DMZ correspond au serveur Web Apache. |
| 30 | Plage d’adresse IP du personnel de gestion du site (Secrétaire, Concierge, etc.). |
| 40 | VLAN voix dédié à la téléphonie sur IP. |
| 50 | VLAN données. Ce VLAN est dédié à la base de données et au serveur DNS, DHCP et Active Directory. |
| 60 | VLAN Médical. Plage d’adresse IP dédiée au personnel médical (médecins, infirmiers/ères, etc.) |
| 90 | VLAN réservé aux bornes WIFI et aux différents capteurs et lecteurs de badges. |

<br/>

### Maîtrise de l'apprentissage critique
<br/>

Pour justifier ma compétence dans l'AC33.06, j'ai présenté cinq traces. 

Les cinq traces sélectionnées pour justifier ma compétence dans l'AC33.06 démontrent ma capacité à sécuriser l'environnement numérique d'une application. 
La configuration d'access-list sur les routeurs Cisco démontre ma compétence à filtrer le trafic réseau en fonction de critères définis, renforçant ainsi la sécurité du réseau. 
L'installation d'un pare-feu Stormshield, associée à des règles de configuration logiquement organisées, prouve ma capacité à analyser et contrôler le trafic entrant et sortant, contribuant à une meilleure protection du réseau.
Le schéma de la DMZ témoigne de ma compréhension et de ma capacité de mise en place de zones intermédiaires pour isoler les serveurs exposés sur Internet, renforçant la sécurité du réseau interne. 
Enfin, la séparation du réseau en VLANs met en avant ma compétence à segmenter le réseau, limitant l'accès aux données sensibles et renforçant la protection globale du système informatique.

Ces cinq traces prouvent ma maîtrise de cet apprentissage critique.


#### Liens :
[Voir l'access list](https://github.com/ThomasM2568/sae502/blob/main/Configuration/acl)
<br/>
[access list](access_list.png)
