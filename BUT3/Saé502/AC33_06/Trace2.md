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

<br/>



