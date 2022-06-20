1. Introduction

Le renseignement de base existe depuis de nombreuses années mais depuis l'évolution et la prolifération de la menace cyber aux alentours des années 2000, la notion d'intelligence du renseignement cyber s'est particulièrement développé, nommée Cyber Threat Intelligence (CTI).

2. Le principe du CTI (Cyber Threat Intelligence) 

Le principe du CTI est de collecter et d'analyser les informations existant autour d'une menace ou d'un adversaire. 

Elle permet, entre autres, d'identifier et d'analyser des cybers menaces.

Elle permet de définir les indicateurs, les techniques d'attaque utilisées, les groupes d'attaquants, les outils utilisés...

Ce profiling permet de mieux se défendre et d'anticiper au mieux les différents incidents en permettant une détection aux prémices d'une attaque d'envergure (APT).  

En effet, le CTI, c'est également déjouer des attaques et récupérer un maximum de renseignements sur ces dits attaquants.

Associé à cela, la mise en place de mesures préventives, de détection et de réponse grâce à la connaissance acquise. 

Ces deux notions permettent d'obtenir une politique de CTI (association entre la collecte et la reconnaissance, et la mise en place de mesures préventives de détection et de réponse).

On pourrait résumer le principe de la CTI par, mieux connaitre pour mieux se défendre et anticiper.

3. Types de Cyber Threat Intelligence

Il existe plusieurs types (catégories) de CTI.

Celles-ci sont essentiellement regroupées en quatre blocs.

- Sratégique : 

Le but est d'obtenir des renseignements sur les grandes tendances actuelles : quel est le groupe particulièrement virulent du moment ? Quel impact financier ce groupe a eu auprès d'entreprises ? Différentes informations sur les risques liés à un malware...

Ces informations seront essentiellement destinées à l'exécutif — management), pour mesurer l'évolution de la menace et des risques, permettant de mieux anticiper les stratégies à adopter.

Ce sont des informations de haut niveau, qui sont dédiées à un usage sur le long terme.

- Tactique :

Le but est d'obtenir des renseignements sur les techniques d'attaque, cela rassemble tout ce qui est utilisé par les attaquants pour récupérer des informations et attaquer — pénétrer votre infrastructure.

Cela peut être les outils utilisés, leurs habitudes, les méthodes utilisées...

Ces informations seront essentiellement destinées au SOC Manager — à l'intégrateur SIEM), permettant d'affiner les méthodes de détection et mettre à jour vos infrastructures.

Ce sont des informations de bas niveau, qui sont dédiées à un usage sur le long terme.

- Opérationnelle :

Le but est d'obtenir des renseignements sur les attaques à venir.

Cela passe le plus souvent par des veilles sur Internet, sur des forums de hacking, sur le DarkWeb, les commerces illégaux sur le DarkWeb, des leaks de credentials.

Il s'agit en quelque sorte d'OSINT, le but étant en quelque sorte de produire du renseignement permettant d'identifier les risques en amont.

Ce type est souvent géré par le RSSI / CERT (Computer Emergency Response Team), pour permettre essentiellement d'évaluer la capacité d'une organisation à se défendre contre de futures menaces.

Ce sont des informations de haut niveau, qui sont dédiées à un usage sur le court terme.

- Technique :

Le but est d'obtenir des renseignements sur les indicateurs de compromissions.

Prenons l'exemple d'un malware qui pénètre un système, le renseignement technique va avoir pour but de récolter des informations telles que : quel C2 (command and control) le malware a-t-il a contacté ? Quelle est la ou les signatures associées à celui-ci ?

À distinguer et à ne pas confondre avec la tactique qui va plus d'avantage se concentrer sur la comphresion de quelle vulnérabilité a été exploité.

La tactique se renseigne sur les méthodes et outils utilisées, alors que la technique va davantage se concentrer sur les données et traces laissées permettant d'identifier le ou la personne — le ou les groupes à l'origine de l'attaque.

Ce type est souvent géré par le SOC / CSIRT (Computer emergency response team), pour permettre de mieux identifier les indicateurs de compromissions.

Ce sont des informations de bas niveau, qui sont dédiées à un usage sur le court terme.

4. Les indicateurs de compromissions :

Il y a énormément d'indicateurs de compromissions qui se baladent dans la nature.

Il faut (dans un premier temps) avoir une méthode correcte pour pouvoir les récupérer, par la suite (encore plus important) il faudra une méthode correcte pour définir la façon de les gérer.

Typiquement, c'est bien beau de récolter une base de 10 millions d'indicateurs, mais avez-vous les moyens pour les gérer, les maintenir et les exploiter ?

Il existe de nombreuses formes d'indicateurs, des règles YARA, des URLs, des adresses IPs, des hashs (md5, sha1...) et bien d'autres.

Il s'agit probablement d'une erreur de vouloir récupérer trop d'indicateurs, en pensant que cela permettra de mieux se protéger.

Le plus important est d'avoir la capacité de collecter de manière intelligente et se poser les bonnes questions.

Typiquement, s'assurer que tous les indicateurs pourront être exploités.

Est-ce que votre EDR remonte des signatures de type SHA-1 ? Si oui, il peut, dans ce cas, être intéressant de récupérer de nombreuses signatures de type SHA-1, autrement, cela n'a quasiment aucune utilité.

5. Mieux gérer ses indicateurs de compromissions :

Pour mieux gérer ses données (indicateurs), il faut également être capables de les classifier.

Voici quelques exemples d'éléments essentiels pour la classification de celles-ci.

- Le scoring :

Il existe trois types de sources.

- Les sources ouvertes : il s'agit des éléments récupérés sur Internet.

Avec des sites tels que abuse.ch, AbuseIPDB, VirusTotal...

Mais également des données récupérées après des veilles réalisées sur des sites telles que Twitter, LinkedIn, des forums sur le clearWeb mais également sur DarkWeb (ces éléments peuvent être une véritable mine d'or).

- Les sources privées :

Il s'agit le plus souvent des éditeurs de logiciels de CTI.

Le plus gros avantage réside dans le fait qu'il s'agit de données bien quantifiées et particulièrement fiables.

- Les sources internes : 

Il s'agit des données récupérées en interne, par le biais de nos infrastructures.

Il s'agit bien évidemment de la donnée la plus fiable de ces trois types.

Si nous avons subi une compromission avec une signature spécifique, il n'y a aucun doute sur cet indicateur.

Bien évidemment, chacun de ces types apporte des avantages et des inconvénients, typiquement, la source publique apporte bien plus d'éléments, mais bien moins fiables que les autres types.

C'est pour cette raison qu'il est intéressant de mettre un système de scale en place.

Je récupère les informations de la source ouvertures mais ne les considères pas comme fiable.

Si je récupère une information provenant de ma source privée, qui entre en corrélation avec celle de ma source publique, cela fait au total un indicateur détecté par deux sources.

Je peux donc considérer mon indacteur comme relativement fiable et le placer au sein de mon SIEM (Security Information & Event Management).

- La durée de vie des indicateurs :

Il est important de ne pas garder éternellement les indicateurs dans sa base pour éviter de complexifier celle-ci (pas seulement, cf. Le statut des indicateurs).

La durée de vie des indicateurs dépend de nombreux facteurs, dont la provenance de la source.

Provenant d'un source ouvert : cela dépend de la source et sa fiabilité mais il s'agit généralement d'une durée de vie des indicateurs assez courts.

Provenant d'un source privée : la durée de vie des indicateurs est généralement gérée automatiquement par les éditeurs de logiciels de CTI.

Provenant de sources internes : cela dépend beaucoup du type d'indicateur, une signature par exemple peut facilement être changée et il ne faut donc pas trop se concentrer dessus.

Une fois que la signature a déjà été flag par absolument tous les antivirus, est-ce vraiment nécessaire de la conserver dans sa base.

En revanche, garder des adresses IP où des noms de domaines par exemple me paraît bien plus pertinent, étant des données plus difficiles à obtenir (du moins, comparer à une simple signature).

- Le statut des indicateurs :

C'est un facteur partiellement lié à la durée de vie des indicateurs.

- Le statut actif (indicateur actif) : il s'agit de menaces actuelles.

- Le status whitelist : j'ai entendu l'anecdote d'une entreprise ayant eu un blocage du logiciel Teams au sein de toute l'entreprise pour une durée de 3h. Ce qui peut être catastrophique pour certaines grosses entreprises dépendantes de cet outil. A l'origine du blocage ? Une veille adresse IP qui avait été définis comme malveillante, sauf qu'avec les années, celle-ci s'est retrouvé attribué à des serveurs Microsoft. Il est donc important de tenir à jour sa base et bien gérer ses délais d'expiration.

- Le statut à définir : si l'indicateur n'est ni actif, ni dans la whitelist, il faut prendre le temps de vérifier ces indicateurs.

- La confidentialité :

Il s'agit d'un facteur très important et déterminant.

Il existe trois niveaux de TLP.

Le TLP est un protocole qui oblige toute personne qui transmet une information à l’associer à une couleur selon un code couleur. Cette couleur indique dans quelle mesure l’information peut ensuite être diffusée. Si la personne qui reçoit l’information estime que celle-ci doit pouvoir être diffusée plus largement, elle doit au préalable demander l'accord de l’expéditeur.

Il existe par exemple :

- Le TLP Red : le code le plus restrictif. Il ne doit pas être divulgué et est réservé aux participants (ou au service).

- Le TLP Amber : divulgation limitée, restreinte à l'organisation (à l'entreprise) des participants.

- Le TLP Green : Réservé à un groupe, une communauté (ou entre entreprises de confiance par exemple)...

- Le TLP White : Aucune restriction.

En quoi c'est important ?

Voici un exemple concret, tiré d'une histoire réelle vécu par M. LEROUX Julien, ancien responsable au sein de l'ANSSI.

Votre organisation subit actuellement une attaque. Le TLP a mal été flagé, ce qui a comme conséquence qu'une des agents envoie la signature du malware sur VirusTotal.

En quoi est-ce grave ? Sur VirusTotal, il y a une fonction de monitoring, permettant de surveiller la liste des programmes soumis sur la plateforme.

L'attaquant qui était en train de monitorer les soumissions en cours pour son malware va s'apercevoir que celui-ci vient d'être analysé et va par conséquent tout faire pour déguerpir le plus vite possible (en laissant par ailleurs le moins de traces possible).
