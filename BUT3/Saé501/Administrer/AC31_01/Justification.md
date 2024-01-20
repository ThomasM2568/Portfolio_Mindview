# SAÉ 5.01 : Concevoir, réaliser et présenter une solution technique
### AC31.01 : Concevoir un projet de réseau informatique d’une entreprise en intégrant les problématiques de haute disponibilité, de QoS, de sécurité et de supervision
### Contexte de la Saé
<br/>
Cette SAÉ 5.01, intitulée “Concevoir, réaliser et présenter une solution technique”, a été encadrée par M.BOUILLET et M.CHARTON. Nous avons réalisé ce projet à l’IUT de Montbéliard du lundi 11 décembre au vendredi 22 décembre.

Le projet visait à mettre en place une infrastructure complète système et réseau basée sur des équipements réseaux réels et plusieurs serveurs de machines virtuelles (Proxmox VE et ESXi)

Chaque membre a pu apporter ses connaissances et son expertise pour concevoir une solution intégrée, depuis la phase de conception jusqu'à la réalisation finale.

Il était important de bien organiser le projet afin de travailler en équipe de manière efficace.


<br/>Pour justifier que je suis compétent pour l'AC31.01, j'ai choisi de présenter :
- la configuration d'un DHCP failover
- l'explication de la configuration de HSRP sur des routeurs et switch Cisco
- la configuration d'un port channel
- une cartographie Zabbix

#### Trace 1 : Configuration du DHCP Failover  (Haute Disponibilité)
<br/>
La configuration du DHCP Failover permet d'avoir un serveur DHCP secondaire qui prendra le relai en cas de panne du premier.
Un serveur DHCP permet de donner les informations de configurations IP (adresse, masque, passerelle, dns) aux clients du réseau.
En mettant en place un DHCP Failover, j'ai assuré une continuité de service, permettant aux utilisateurs du réseau d'obtenir des adresses IP même en cas de défaillance d'un serveur DHCP princial. 
Ce mécanisme permet d'assurer de la haute disponibilité.
<br/>

#### Trace 2 : Explication de la configuration de HSRP sur des routeurs et switch Cisco (Haute Disponibilité et QoS)
<br/>
 
J'ai été capable d'expliquer l'intérêt de configurer la fonctionnalité HSRP sur des équipements réseaux Cisco en m'appuyant sur des schémas.
Cela montre ma compréhension et ma maîtrise de la notion de haute disponibilité et de qualité de service (QoS), mais également ma capacité à mettre en place cette fonctionnalité.
Ce mécanisme est fréquemment utilisé en réseau pour assurer des communications ininterrompues et transparentes pour l'utilisateur en cas de panne d'un équipement.
Cela démontre ma capacité à mettre en place des mécanismes de Haute Disponibilité et de Qos.

<br/>

#### Trace 3 : Configuration d'un port Channel (Haute Disponibilité et QoS)
<br/>
Je suis capable de comprendre et configurer un port channel.
Cette fonctionnalité permet de regrouper plusieurs liens physique en un seul lien logique, augmentant donc la bande passante et la redondance. En effet, si un lien physique venait à tomber, les autres liens du même groupe logiques continueraient à assurer le service.
Ma capacité à configurer cette fonctionnalité démontre ma capacité à mettre en place des mécanismes de Haute Disponibilité et de Qos.
<br/>

#### Trace 4 : Cartographie Zabbix (Supervision)
<br/>
Je suis capable de réaliser une cartographie du réseau sur le logiciel de supervision Zabbix. Le but est de pouvoir surveiller l'état de tous les équipements du réseau en temps réel.
On peut voir sur la cartographie qu'un des deux serveurs n'est pas joignable. Je suis donc capable de le montrer via ma cartographie zabbix, permettant d'alerter les administrateurs réseaux d'un état anormal d'un équipement.
<br/>
### Maîtrise de l'apprentissage critique
<br/>
Pour justifier ma compétence dans l'AC31.01, j'ai présenté quatre traces. 
<br/>
La configuration du DHCP failover. Cette fonctionnalité permet d'assurer le bon fonctionnement de la distribution d'adresses IP sur le réseau en cas de panne du serveur principal. (Haute disponibilité)
L'explication de la configuration HSRP. Je suis capable de vulgariser une notion technique et d'expliquer son intérêt ainsi que sa pertinence dans le cadre de la saé. Je suis également capable de la mettre en place et de fournir les configurations réalisées. (Haute Disponibilité et QoS)
La configuration d'un port channel. L'intérêt de ce mécanisme est de regrouper plusieurs liens physiques dans un lien logique, augmentant donc la résistance du lien logique en cas de panne.(Haute Disponibilité et QoS)
Je suis capable de superviser mon réseau et de me rendre compte d'anomalies à l'aide de Zabbix. Je suis également capable de réaliser une cartographie et d'intégrer les équipements réseaux à celle-ci.

<br/>
