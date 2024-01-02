# SAÉ 5.02 : Piloter un projet informatique
### AC31.04 : Défendre/argumenter un projet
### Contexte de la Saé
<br/>
L'objectif de cette Saé est de définir les exigences d'un réseau sécurisé d'hôpital en termes de sécurité et de réaliser les tâches de configurations liées à la sécurisation du système informatique. 
Compte tenu des récentes attaques cyberet de la sensibilité des données médicales, il est essentiel de mettre en place une infrastructure informatique robuste et sécurisée. Le projet consistera à créer une architecture
réseau cloisonnée, à sécuriser l'accès aux données médicales, à établir une connexion VPN avec un autre hôpital, et à documenter l'ensemble du système.


<br/>Pour justifier que je suis compétent pour l'AC31.03, j'ai choisi de présenter :
-  le support de présentation de la maquette mise en place.
-  la photographie de l'installation de 2 routeurs Cisco 1900 series et d'une borne wifi Linksys WRT.
-  le schéma d'architecture réseau de la Saé.

Vous retrouverez les liens de ces documents dans la section liens en bas de cette page.

#### Trace 1 : Support de présentation de la maquette mise en place
<br/>

Pour faciliter la compréhension du projet, j'ai préparé un support de présentation de la maquette.
Celle-ci montre :
- les choix architecturaux de chacun des sites.
- Les serveurs et services mis en place.
- La haute disponibilité implémentée (Redondance et équilibrage de charge)
- Les scripts créés.
- La sécurité mise en place
- Les pistes d'améliorations du projet.

La démonstration de l'ensemble de ces éléments démontre ma compréhension de la Saé et ma capacité à proposer une solution cohérente en adéquation avec les problématiques d'un hôpital. (service ininterrompu et résistant, sécurité poussée, redondance)
Cela démontre également ma capacité à mettre en place ces éléments via les différentes preuves et démonstrations proposées dans le support.

<br/>

#### Trace 2 : Rédaction d'un rapport de Saé
<br/>

J'ai rédigé un rapport de cette Saé avec Arnaud Kastner, Alexandre Berot-Armand et Kyllian Cuevas.
Ma capacité à synthétiser les éléments mis en places démontre ma compréhension des configurations réalisées et leur maîtrise.
De plus, la partie piste d'améliorations met en avant ma compréhension plus globale du projet et mettant en avant ce qui aurait pu être fait pour améliorer la maquette mise en place.

<br/>

#### Trace 3 : Vidéo de démonstration d'une fonctionnalité mise en place
<br/>

La vidéo de démonstration met en avant la robustesse de l'infrastructure que j'ai configurée, notamment grâce aux fonctionnalités VRRP (keepalived) sur les brokers MQTT avec un SLB (Haproxy). 
VRRP est un protocole permettant de partager une adresse IP virtuelle entre deux équipements permettant de basculer le trafic plus facilement en cas de panne d'un des équipements.
SLB est un protocole permettant l'équilibrage de charges entre serveurs (Server Load Balancing). Le but est de permettre à chaque serveur de se répartir le trafic de manière équilibrée.
En cas de panne l'équilibrage continuera à fonctionner entre les serveurs en lignes.

Cette robustesse est un paramètre d'autant plus important dans le contexte de cette Saé (Réseau hospitalier).

<br/>

### Maîtrise de l'apprentissage critique
<br/>

Pour justifier ma compétence dans l'AC31.01, j'ai présenté trois traces. 

Mon approche de la conception de la maquette montre ma capacité à documenter de manière détaillée des fonctionnalités mises en places.

De plus je suis capable de mettre en place des services complexes et de la haute disponibilité répondant aux besoins d'un environnement hospitalier.

Ces trois traces prouvent ma maîtrise de cet apprentissage critique.


#### Liens :
[Support de présentation](https://www.canva.com/design/DAFycERss7U/IgD0LpFksewwwncMy_cW-g/view?utm_content=DAFycERss7U&utm_campaign=designshare&utm_medium=link&utm_source=editor)
[Rapport de Saé](https://docs.google.com/document/d/1ceTCKuImtVdPNZooNXrqD9qbkR_H65VHRI9zgdcTq98/edit?usp=sharing)
[Vidéo de démonstration](https://drive.google.com/file/d/1Bcb7qs9683V1hOu-9UW2KHCeML8JWAD2/view)
