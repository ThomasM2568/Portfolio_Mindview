# SAÉ 5.02 : Piloter un projet informatique
###  AC33.06 : Sécuriser l’environnement numérique d’une application
#### Trace 4 : Séparation du réseau en VLAN
<br/>
Les VLANs (Virtual Local Area Network) sont des groupes permettant ainsi de segmenter et de cloisonner un réseau physique en plusieurs réseaux virtuels. 
<br/>
Afin d’améliorer la sécurité et faciliter l’administration du réseau j'ai créé plusieurs VLANs. 
Avec des VLAN, l'accès d'une zone à l'autre est impossible ce qui limite l'accès aux données sensibles au personnel autorisé. 
Par exemple, cela évite qu'une personne de l'administration accède à des données de recherches.
<br/>
Ainsi j'ai créé 8 VLANs :
<br/>
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


