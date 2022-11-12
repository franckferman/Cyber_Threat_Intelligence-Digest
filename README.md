<div id="top"></div>

<div align="center">
  <a href="https://github.com/franckferman/Cyber_Threat_Intelligence-Digest">
    <img src="https://raw.githubusercontent.com/franckferman/Cyber_Threat_Intelligence-Digest/main/assets/img/logo.png" alt="Cyber_Threat_Intelligence-Digest" width="200" height="200">
  </a>

<h3 align="center">Cyber Threat Intelligence Digest</h3>

  <p align="center">
  Introduction à la Cyber Threat Tntelligence.  
  <br/>
  <br/>
  </p>
</div>

<details>
  <summary>Table des matières</summary>
  <ol>
    <li><a href="#1-préambule">Préambule</a></li>
    <li><a href="#2-le-principe-de-la-cti-cyber-threat-tntelligence">Le principe de la CTI (Cyber Threat Tntelligence)</a></li>
      <li><a href="#3-types-de-cyber-threat-intelligence">Types de Cyber Threat Intelligence</a></li>
      <li><a href="#4-les-indicateurs-de-compromissions">Les indicateurs de compromissions</a></li>
    <li><a href="#5-mieux-gérer-ses-indicateurs-de-compromissions">Mieux gérer ses indicateurs de compromissions</a></li>
  </ol>
</details>

<div align="center">
<h2>1. Préambule</h2>

<p>Le principe fondamental de renseignement existe depuis de nombreuses décennies. Historiquement, la notion de renseignement était déjà employé pendant l'Antiquité et au Moyen Âge — aussi bien au sein du Moyen-Orient (Mésopotamie, Égypte, Perse...), qu'en Extrême-Orient (Chine, Inde...) et en Europe (Carthage, Rome, Grèce). 
  
Il existe par ailleurs de très bons exemples historiques : dans l’Ancien Testament et la Bible ; dans les récits d’Hérodote et ceux des historiens romains ; pendant les Croisades (pratiqué tant par les royaumes Chrétiens que Musulmans) ; pendant la guerre de Cent Ans (caractérisée par une pratique constante de conspirations, d'intrigues et de manœuvres secrètes entre les belligérants pratiquées par des espions, des traîtres et des agents...) ; dans la péninsule ibérique lors de la Reconquista ; au Japon avec les ninjas (contrairement à la croyance commune probablement dû à la confusion qu'ont les individus à différencier Samouraï et Ninja, ces derniers n'étaient pas soumis au bushidō, et pratiquaient par conséquent de nombreuses missions d'espionnage, parfois peu éthiques) ; ou encore dans les deux plus anciens traités de stratégie au monde (L’Art de la Guerre de Sun Tse et l’Arthasastra de Kautilya)...
  
C'est à partir du 19e siècle que le terme de renseignement apparaît comme « information, plus ou moins difficile à obtenir, concernant l'ennemi », puis vers 1920 apparaît d'autres principes et expressions, à l'instar de celui de « service de recherche des renseignements » désignant les organismes étatiques consacrés à cette activité. Les services de renseignements ont notamment pour mission de collecter, d'analyser et de traiter des informations afin de fournir aux pouvoirs publics un appui dans la prise de décision.
  
Depuis l'évolution et la prolifération des menaces Cyber (déstabilisation, espionnage, sabotage...) aux alentours des années 2000, la notion d'intelligence du renseignement Cyber s'est particulièrement développé, d'où la naissance de la notion de Cyber Threat Intelligence (CTI).</p>

<div align="center">
<h2>2. Les principes de la CTI (Cyber Threat Tntelligence)</h2>

<p>Le principe du CTI est de recueillir et d'analyser l'information existante autour d'une menace ou d'un adversaire, cela permet notamment l'identification et l'analyse des cybers menaces.</br>
Il permet ainsi de définir les indicateurs, les techniques d'attaque utilisées, les groupes d'attaquants, ainsi que les outils utilisés.</br>
Ce profiling permet de mieux se défendre et d'anticiper au mieux les différents incidents en permettant une détection aux prémices d'une attaque d'envergure (APT).</br>  
En effet, le CTI, c'est également déjouer des attaques et récupérer un maximum de renseignements sur ces dits attaquants.</br>
Associé à cela, la mise en place de mesures préventives, de détection et de réponse grâce à la connaissance acquise.</br> 
Ces deux notions permettent d'obtenir une politique de CTI (association entre la collecte et la reconnaissance, et la mise en place de mesures préventives de détection et de réponse).</br>
On pourrait résumer le principe de la CTI par, mieux connaitre pour mieux se défendre et anticiper.</br>
</p></br></br>

<div align="center">
<h2>3. Types de Cyber Threat Intelligence</h2>

<p>Il existe plusieurs types (catégories) de CTI.</br>

Celles-ci sont essentiellement regroupées en quatre blocs.</br>

- Sratégique :</br> 

Le but est d'obtenir des renseignements sur les grandes tendances actuelles : quel est le groupe particulièrement virulent du moment ? Quel impact financier ce groupe a eu auprès d'entreprises ? Différentes informations sur les risques liés à un malware...</br>

Ces informations seront essentiellement destinées à l'exécutif — management), pour mesurer l'évolution de la menace et des risques, permettant de mieux anticiper les stratégies à adopter.</br>

Ce sont des informations de haut niveau, qui sont dédiées à un usage sur le long terme.</br>

- Tactique :</br>

Le but est d'obtenir des renseignements sur les techniques d'attaque, cela rassemble tout ce qui est utilisé par les attaquants pour récupérer des informations et attaquer — pénétrer votre infrastructure.</br>

Cela peut être les outils utilisés, leurs habitudes, les méthodes utilisées...</br>

Ces informations seront essentiellement destinées au SOC Manager — à l'intégrateur SIEM), permettant d'affiner les méthodes de détection et mettre à jour vos infrastructures.</br>

Ce sont des informations de bas niveau, qui sont dédiées à un usage sur le long terme.</br>

- Opérationnelle :</br>

Le but est d'obtenir des renseignements sur les attaques à venir.</br>

Cela passe le plus souvent par des veilles sur Internet, sur des forums de hacking, sur le DarkWeb, les commerces illégaux sur le DarkWeb, des leaks de credentials.</br>

Il s'agit en quelque sorte d'OSINT, le but étant en quelque sorte de produire du renseignement permettant d'identifier les risques en amont.</br>

Ce type est souvent géré par le RSSI / CERT (Computer Emergency Response Team), pour permettre essentiellement d'évaluer la capacité d'une organisation à se défendre contre de futures menaces.</br>

Ce sont des informations de haut niveau, qui sont dédiées à un usage sur le court terme.</br>

- Technique :</br>

Le but est d'obtenir des renseignements sur les indicateurs de compromissions.</br>

Prenons l'exemple d'un malware qui pénètre un système, le renseignement technique va avoir pour but de récolter des informations telles que : quel C2 (command and control) le malware a-t-il a contacté ? Quelle est la ou les signatures associées à celui-ci ?</br>

À distinguer et à ne pas confondre avec la tactique qui va plus d'avantage se concentrer sur la comphresion de quelle vulnérabilité a été exploité.</br>

La tactique se renseigne sur les méthodes et outils utilisées, alors que la technique va davantage se concentrer sur les données et traces laissées permettant d'identifier le ou la personne — le ou les groupes à l'origine de l'attaque.</br>

Ce type est souvent géré par le SOC / CSIRT (Computer emergency response team), pour permettre de mieux identifier les indicateurs de compromissions.</br>

Ce sont des informations de bas niveau, qui sont dédiées à un usage sur le court terme.</br>

</p></br></br>

<div align="center">
<h2>4. Les indicateurs de compromissions</h2>

<p>Il y a énormément d'indicateurs de compromissions qui se baladent dans la nature.</br>

Il faut (dans un premier temps) avoir une méthode correcte pour pouvoir les récupérer, par la suite (encore plus important) il faudra une méthode correcte pour définir la façon de les gérer.</br>

Typiquement, c'est bien beau de récolter une base de 10 millions d'indicateurs, mais avez-vous les moyens pour les gérer, les maintenir et les exploiter ?</br>

Il existe de nombreuses formes d'indicateurs, des règles YARA, des URLs, des adresses IPs, des hashs (md5, sha1...) et bien d'autres.</br>

Il s'agit probablement d'une erreur de vouloir récupérer trop d'indicateurs, en pensant que cela permettra de mieux se protéger.</br>

Le plus important est d'avoir la capacité de collecter de manière intelligente et se poser les bonnes questions.</br>

Typiquement, s'assurer que tous les indicateurs pourront être exploités.</br>

Est-ce que votre EDR remonte des signatures de type SHA-1 ? Si oui, il peut, dans ce cas, être intéressant de récupérer de nombreuses signatures de type SHA-1, autrement, cela n'a quasiment aucune utilité.</br>

</p></br></br>

<div align="center">
<h2>5. Mieux gérer ses indicateurs de compromissions</h2>

<p>Pour mieux gérer ses données (indicateurs), il faut également être capables de les classifier.</br>

Voici quelques exemples d'éléments essentiels pour la classification de celles-ci.</br>

- Le scoring :</br>

Il existe trois types de sources.</br>

- Les sources ouvertes : il s'agit des éléments récupérés sur Internet.</br>

Avec des sites tels que abuse.ch, AbuseIPDB, VirusTotal...</br>

Mais également des données récupérées après des veilles réalisées sur des sites telles que Twitter, LinkedIn, des forums sur le clearWeb mais également sur DarkWeb (ces éléments peuvent être une véritable mine d'or).</br>

- Les sources privées :</br>

Il s'agit le plus souvent des éditeurs de logiciels de CTI.</br>

Le plus gros avantage réside dans le fait qu'il s'agit de données bien quantifiées et particulièrement fiables.</br>

- Les sources internes :</br> 

Il s'agit des données récupérées en interne, par le biais de nos infrastructures.</br>

Il s'agit bien évidemment de la donnée la plus fiable de ces trois types.</br>

Si nous avons subi une compromission avec une signature spécifique, il n'y a aucun doute sur cet indicateur.</br>

Bien évidemment, chacun de ces types apporte des avantages et des inconvénients, typiquement, la source publique apporte bien plus d'éléments, mais bien moins fiables que les autres types.</br>

C'est pour cette raison qu'il est intéressant de mettre un système de scale en place.</br>

Je récupère les informations de la source ouvertures mais ne les considères pas comme fiable.</br>

Si je récupère une information provenant de ma source privée, qui entre en corrélation avec celle de ma source publique, cela fait au total un indicateur détecté par deux sources.</br>

Je peux donc considérer mon indacteur comme relativement fiable et le placer au sein de mon SIEM (Security Information & Event Management).</br>

- La durée de vie des indicateurs :</br>

Il est important de ne pas garder éternellement les indicateurs dans sa base pour éviter de complexifier celle-ci (pas seulement, cf. Le statut des indicateurs).</br>

La durée de vie des indicateurs dépend de nombreux facteurs, dont la provenance de la source.</br>

Provenant d'un source ouvert : cela dépend de la source et sa fiabilité mais il s'agit généralement d'une durée de vie des indicateurs assez courts.</br>

Provenant d'un source privée : la durée de vie des indicateurs est généralement gérée automatiquement par les éditeurs de logiciels de CTI.</br>

Provenant de sources internes : cela dépend beaucoup du type d'indicateur, une signature par exemple peut facilement être changée et il ne faut donc pas trop se concentrer dessus.</br>

Une fois que la signature a déjà été flag par absolument tous les antivirus, est-ce vraiment nécessaire de la conserver dans sa base.</br>

En revanche, garder des adresses IP où des noms de domaines par exemple me paraît bien plus pertinent, étant des données plus difficiles à obtenir (du moins, comparer à une simple signature).</br>

- Le statut des indicateurs :</br>

C'est un facteur partiellement lié à la durée de vie des indicateurs.</br>

- Le statut actif (indicateur actif) : il s'agit de menaces actuelles.</br>

- Le status whitelist : j'ai entendu l'anecdote d'une entreprise ayant eu un blocage du logiciel Teams au sein de toute l'entreprise pour une durée de 3h. Ce qui peut être catastrophique pour certaines grosses entreprises dépendantes de cet outil. A l'origine du blocage ? Une veille adresse IP qui avait été définis comme malveillante, sauf qu'avec les années, celle-ci s'est retrouvé attribué à des serveurs Microsoft. Il est donc important de tenir à jour sa base et bien gérer ses délais d'expiration.</br>

- Le statut à définir : si l'indicateur n'est ni actif, ni dans la whitelist, il faut prendre le temps de vérifier ces indicateurs.</br>

- La confidentialité :</br>

Il s'agit d'un facteur très important et déterminant.</br>

Il existe trois niveaux de TLP.</br>

Le TLP est un protocole qui oblige toute personne qui transmet une information à l’associer à une couleur selon un code couleur. Cette couleur indique dans quelle mesure l’information peut ensuite être diffusée. Si la personne qui reçoit l’information estime que celle-ci doit pouvoir être diffusée plus largement, elle doit au préalable demander l'accord de l’expéditeur.</br>

Il existe par exemple :</br>

- Le TLP Red : le code le plus restrictif. Il ne doit pas être divulgué et est réservé aux participants (ou au service).</br>

- Le TLP Amber : divulgation limitée, restreinte à l'organisation (à l'entreprise) des participants.</br>

- Le TLP Green : Réservé à un groupe, une communauté (ou entre entreprises de confiance par exemple)...</br>

- Le TLP White : Aucune restriction.</br>

En quoi c'est important ?</br>

Voici un exemple concret, tiré d'une histoire réelle vécu par M. LEROUX Julien, ancien responsable au sein de l'ANSSI.</br>

Votre organisation subit actuellement une attaque. Le TLP a mal été flagé, ce qui a comme conséquence qu'une des agents envoie la signature du malware sur VirusTotal.</br>

En quoi est-ce grave ? Sur VirusTotal, il y a une fonction de monitoring, permettant de surveiller la liste des programmes soumis sur la plateforme.</br>

L'attaquant qui était en train de monitorer les soumissions en cours pour son malware va s'apercevoir que celui-ci vient d'être analysé et va par conséquent tout faire pour déguerpir le plus vite possible (en laissant par ailleurs le moins de traces possible).</br>

</p></br></br>
