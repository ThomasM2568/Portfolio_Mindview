# SAÉ 5.02 : Piloter un projet informatique
###  AC33.04 : Déployer et maintenir une solution informatique
### Contexte de la Saé
<br/>
L'objectif de cette Saé est de définir les exigences d'un réseau sécurisé d'hôpital en termes de sécurité et de réaliser les tâches de configurations liées à la sécurisation du système informatique. 
Compte tenu des récentes attaques cyberet de la sensibilité des données médicales, il est essentiel de mettre en place une infrastructure informatique robuste et sécurisée. Le projet consistera à créer une architecture
réseau cloisonnée, à sécuriser l'accès aux données médicales, à établir une connexion VPN avec un autre hôpital, et à documenter l'ensemble du système.


<br/>Pour justifier que je suis compétent pour l'AC33.04, j'ai choisi de présenter :
-  le schéma de l'architecture réseau.
-  la sauvegarde des équipements réseaux sur Github.
-  une photographie des équipements mis en place.
-  une vidéo de démonstration d'une fonctionnalité mise en place.

Vous retrouverez les liens de ces documents dans la section liens en bas de cette page.

#### Trace 1 : Schéma de l'architecture réseau
<br/>

Le but était de définir l'ensemble des fonctionnalités à mettre en place. 
Etre capable de réaliser un schéma complet intégrant des serveurs, des services, de la sécurité et de la haute disponibilité démontre à concevoir l'infrastructure réseau d'un projet en tenant compte des spécificités techniques de celui-ci.

<br/>

#### Trace 2 : Sauvegarde et versionnage des configurations des équipements réseaux
<br/>

Nous avons choisi d'utiliser github comme outil de versionnage. Le but est de garder les différentes versions des configurations dans un outil centralisé.
L'ensemble des configurations comprend les serveurs, les services et le réseau. J'ai choisi de présenter cette capture d'écran car elle permet de montrer ma maîtrise des configurations en retrouvant directement celles-ci sur mon Github.
De plus, on peut facilement voir les différences entre les versions ce qui montre l'évolution du projet.
cela démontre également ma capacité déployer les configurations et à les mettre à jour.

<br/>

#### Trace 3 : Photographie des équipements réseaux mis en place
<br/>

La photographie des équipements réseaux permet de voir une partie du réseau mis en place physiquement d'après les schémas et les configurations réalisées et présentées préalablement.
Cela montre que je suis capable de déployer des équipements informatiques.
<br/>

#### Trace 4 : Vidéo de démonstration d'une fonctionnalité mise en place
<br/>

La vidéo de démonstration met en avant la robustesse de l'infrastructure que j'ai configurée, notamment grâce aux fonctionnalités VRRP (keepalived) sur les brokers MQTT avec un SLB (Haproxy). VRRP est un protocole permettant de partager une adresse IP virtuelle entre deux équipements permettant de basculer le trafic plus facilement en cas de panne d'un des équipements. SLB est un protocole permettant l'équilibrage de charges entre serveurs (Server Load Balancing). Le but est de permettre à chaque serveur de se répartir le trafic de manière équilibrée. En cas de panne l'équilibrage continuera à fonctionner entre les serveurs en lignes.

Cette robustesse est un paramètre d'autant plus important dans le contexte de cette Saé (Réseau hospitalier).

Cette vidéo permet de valider le bon fonctionnement global du réseau et démontre donc ma compétence à déployer et maintenir une solution informatique.

<br/>

### Maîtrise de l'apprentissage critique
<br/>

Pour justifier ma compétence dans l'AC33.04, j'ai présenté quatre traces. 

Ces traces sont évolutives, dans le sens où elles permettent de se rendre compte de ma maîtrise des configurations et du matériel. En effet, on peut voir toutes les étapes du projet, de la phase de conceptions à la phase de mise en production.
Chaque configuration réalisée a été réalisée d'après le schéma sur une maquette de tests, puis validées par une série de tests unitaires et de non-regression. Je les ai ensuite versionnées sur Github et déployées sur les équipements physiques.
Je les ai ensuite testé à nouveau dans le but de valider le bon fonctionnement global de la solution.
J'ai finalement réalisé une vidéo de démonstration qui atteste de ce bon fonctionnement.

Je suis donc capable de déployer et maintenir une solution informatique de sa phase de conception à sa phase de mise en production.

Ces trois traces prouvent ma maîtrise de cet apprentissage critique.


#### Liens :
[Dépôt Github de la saé](https://github.com/ThomasM2568/sae502)

<br/> [Vidéo de démonstration](https://drive.google.com/file/d/1Bcb7qs9683V1hOu-9UW2KHCeML8JWAD2/view)
