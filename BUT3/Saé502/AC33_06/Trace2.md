# SAÉ 5.02 : Piloter un projet informatique
###  AC33.06 : Sécuriser l’environnement numérique d’une application
#### Trace 1 : Configuration d'access list sur les routeurs Cisco

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



