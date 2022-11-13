<div id="top"></div>

<div align="center">
  <a href="https://github.com/franckferman/Cyber_Threat_Intelligence-Digest">
    <img src="https://raw.githubusercontent.com/franckferman/Cyber_Threat_Intelligence-Digest/main/assets/img/logo.png" alt="Cyber_Threat_Intelligence-Digest" width="200" height="200">
  </a>

<h3 align="center">Cyber Threat Intelligence Digest</h3>

  <p align="center">
  Introduction à la Cyber Threat Tntelligence.
  </p>
</div>

<details>
  <summary>Table des matières</summary>
  <ol>
    <li><a href="#1-préambule">Préambule</a></li>
    <li><a href="#2-le-principe-de-la-cyber-threat-intelligence-cti">Le principe de la Cyber Threat Tntelligence (CTI)</a></li>
      <li><a href="#3-types-de-cyber-threat-intelligence">Types de Cyber Threat Intelligence</a></li>
      <li><a href="#4-les-indicateurs-de-compromissions">Les indicateurs de compromissions</a></li>
    <li><a href="#5-mieux-gérer-ses-indicateurs-de-compromissions">Mieux gérer ses indicateurs de compromissions</a></li>
  </ol>
</details>

<div align="center">
<h2>1. Préambule</h2>
</div>

<p>Le principe fondamental de renseignement existe depuis de nombreuses décennies. Historiquement, la notion de renseignement était déjà employé pendant l'Antiquité et au Moyen Âge — aussi bien au sein du Moyen-Orient (Mésopotamie, Égypte, Perse...), qu'en Extrême-Orient (Chine, Inde...) et en Europe (Carthage, Rome, Grèce). 
  
Il existe par ailleurs de très bons exemples historiques : dans l’Ancien Testament et la Bible ; dans les récits d’Hérodote et ceux des historiens romains ; pendant les Croisades (pratiqué tant par les royaumes Chrétiens que Musulmans) ; pendant la guerre de Cent Ans (caractérisée par une pratique constante de conspirations, d'intrigues et de manœuvres secrètes entre les belligérants, pratiquées par des espions, des traîtres et des agents...) ; dans la péninsule ibérique lors de la Reconquista ; au Japon avec les ninjas (contrairement à la croyance commune, probablement dû à la confusion qu'ont les individus quand il s'agit de différencier Samouraï et Ninja, ces derniers n'étaient pas soumis au Bushidō, et pratiquaient, souvent en omettant volontairement toutes valeurs ou éthiques, de nombreuses missions d'espionnage, d'infiltration, de sabotage, d'assassinat...) ; ou encore dans les deux plus anciens traités de stratégie au monde (L’Art de la Guerre de Sun Tse et l’Arthasastra de Kautilya)...
  
C'est à partir du 19e siècle que le terme de renseignement apparaît comme « information, plus ou moins difficile à obtenir, concernant l'ennemi », puis vers 1920 apparaît d'autres principes et expressions, à l'instar de celui de « service de recherche des renseignements » désignant les organismes étatiques consacrés à cette activité. Les services de renseignements avaient notamment pour mission de collecter, d'analyser et de traiter des informations afin de fournir aux pouvoirs publics un appui dans la prise de décision.
  
Mais depuis l'évolution et la prolifération des menaces Cyber (déstabilisation, espionnage, sabotage...) aux alentours des années 2000, une nouvelle notion est née et s'est particulièrement développé, celle d'intelligence du renseignement Cyber, justifiant la naissance de la notion de Cyber Threat Intelligence (CTI).</p>

<br>

<div align="center">
<h2>2. Le principe de la Cyber Threat Intelligence (CTI) et ses moyens</h2>
</div>

<p>La CTI vise à collecter et à analyser les informations existant sur une menace ou un adversaire, notamment en dressant un portrait des attaquants ou en mettant en exergue des tendances (secteurs d'activités touchés, méthode utilisée, etc.), ce qui permettra de mieux identifier et analyser les cybermenaces.

La CTI inclut le « renseignement d'origine sources ouvertes » (OSINT), le renseignement à travers des sources privés (notamment sur des groupes Telegram, des sections privées de forums, des groupes Discord...), le renseignement humain et l'ingénierie sociale (Social Engineering), le renseignement technique, les fichiers journaux (logs), les données acquises « judiciairement » ou le renseignement sur le trafic Internet (à l'échelle du fournisseur) et les données dérivées du Dark Web.

Plus précisément, la CTI permet de définir les indicateurs d'attaque, les techniques utilisées, les groupes d'attaquants et les outils utilisés. Ce « profiling » permet de se défendre et anticiper au mieux les différents incidents, en permettant une détection aux prémices d'une attaque d'envergure (APT). 

En effet, la CTI vise également à se préparer aux attaques en amont, en récupérant le plus d'informations possible sur ces attaquants. Couplé à cela, la mise en œuvre de mesures de prévention, de détection et de réponse par le biais des connaissances acquises.

Ces deux concepts (l'association de la collecte et la reconnaissance, avec la mise en place de mesures préventives de détection et de réponse) permettent d'obtenir une stratégie de CTI.

La CTI pourrait être résumée par le fait qu'elle vise à mieux connaître les menaces pour mieux se défendre et anticiper.</p>

<br>

<div align="center">
<h2>3. Les différents types de la Cyber Threat Tntelligence</h2>
</div>

<p>Les différents types de Cyber Threat Tntelligence sont essentiellement regroupées en quatre blocs.

- Tactique :

Le but est d'obtenir des renseignements sur les techniques d'attaque, cela rassemble tout ce qui est utilisé par les attaquants pour récupérer des informations et attaquer votre infrastructure, cela inclut notamment les méthodes utilisées par les attaquants, leurs habitudes et les outils dont ils se servent.

Les informations fournies ici seront principalement utilisées par le SOC Manager ou par l'intégrateur SIEM afin d'améliorer d'affiner les méthodes de détection et mettre à jour vos infrastructures.

Ce sont des informations de bas niveau, dédiées à un usage sur le long terme.

- Technique :

L'objectif est de collecter des données sur les indicateurs de compromissions.

Prenons l'exemple d'un malware qui s'introduit dans un système. L'objectif du renseignement technique sera la collecte de renseignements connexes, en un sens, associés à la compromission, par exemple : quelle infrastructure de « Commande et Contrôle » (C&C ou C²) le malware a-t-il a contacté ? Quelle est là, ou quelles sont les signatures qui y sont associées ?

Le bloc technique ne doit pas être confondu avec le bloc tactique, puisque ce dernier se concentre davantage sur la compréhension de la vulnérabilité ayant été exploité. En effet, le bloc tactique se renseigne sur les méthodes et outils utilisées, alors qu'antithétiquement, le bloc technique se concentrera davantage sur les données et traces laissées permettant d'identifier le ou la personne — le ou les groupes à l'origine d'une attaque.

Ce bloc est souvent géré par le SOC — CSIRT (Computer Emergency Response Team), afin de permettre une meilleure identification des indicateurs de compromissions.

Ce sont des informations de bas niveau, dédiées à un usage sur le court terme.

- Opérationnelle :

L'objectif consiste à obtenir des informations sur les attaques futures.

Cela passe habituellement par des veilles sur Internet, sur les forums (de hacking), sur le Dark Web (commerces illégaux, forums), notamment à la recherche de leaks de credentials.

Il s'agit en quelque sorte d'OSINT, c'est-à-dire, en quelque sorte de produire du renseignement, permettant d'identifier les risques en amont.

Ce bloc est souvent géré par le RSSI ou le CERT (Computer Emergency Response Team), pour permettre essentiellement d'évaluer la capacité d'une organisation à se défendre contre de futures menaces.

Ce sont des informations de haut niveau, dédiées à un usage sur le court terme.

- Sratégique :

L'objectif consiste à obtenir de l'information sur les principales tendances actuelles, par exemple : quel groupe est particulièrement virulent ces derniers temps ? Quelles ont été les répercussions financières de l'attaque de la part de ce groupe pour les entreprises ? Divers renseignements au sujet des risques associés à un malware...

Ces renseignements seront principalement utilisés par l'exécutif (management) pour mesurer l'évolution de la menace et des risques, ce qui permettra de mieux prévoir les stratégies à adopter.

Ce sont des informations de haut niveau, dédiées à un usage sur le long terme.</p>

<br>

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
