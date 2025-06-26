---
title: "Menaces courantes"
icon: 'material/eye-outline'
description: Votre modèle de menace vous est personnel, mais ce sont là quelques-unes des questions qui préoccupent de nombreux visiteurs de ce site.
---

Pour faire simple, nous classons nos recommandations dans ces catégories générales de [menaces](threat-modeling.md) ou d'objectifs qui s'appliquent à la plupart des gens. ==Vous pouvez vous sentir concerné par une, plusieurs, toutes, ou bien aucune de ces possibilités==. Les outils et les services que vous utilisez dépendent également de vos objectifs. Il est possible que vous ayez des menaces spécifiques ne rentrant dans aucune de ces catégories, ce qui est tout à fait normal ! L'important est de bien comprendre les avantages et les inconvénients des outils que vous choisissez d'utiliser, car pratiquement aucun d'entre eux ne vous protégera contre toutes les menaces possibles.

<span class="pg-purple">:material-incognito: **Anonymat**</span>
:

Dissocier votre activité en ligne par rapport à votre identité réelle, vous protégeant ainsi des personnes qui tentent de découvrir  *votre* identité en particulier.

<span class="pg-red">:material-target-account: **Attaques ciblées**</span>
:

Être protégé contre les hackers ou autres entités malveillantes qui essaient d'accéder spécifiquement à *vos* données ou à vos appareils.

<span class="pg-viridian">:material-package-variant-closed-remove: **Attaques de la chaîne d'approvisionnement**</span>
:

Il s'agit généralement d'une forme d'<span class="pg-red">:material-target-account: Attaque Ciblée</span> centrée sur une vulnérabilité ou un exploit introduit dans un logiciel par ailleurs satisfaisant, soit directement, soit par l'intermédiaire d'une dépendance d'une tierce partie.

<span class="pg-orange">:material-bug-outline: **Attaques passives**</span>
:

Être protégé contre les logiciels malveillants, les fuites de données et d'autres attaques dirigées contre de nombreuses personnes à la fois.

<span class="pg-teal">:material-server-network: **Fournisseurs de services**</span>
:

Protéger vos données des fournisseurs de services (par exemple avec E2EE, qui rend vos données illisibles pour le serveur).

<span class="pg-blue">:material-eye-outline: **Surveillance de masse**</span>
:

Protection contre les agences gouvernementales, les organisations, les sites web et les services qui travaillent ensemble pour suivre vos activités.

<span class="pg-brown">:material-account-cash: **Capitalisme de surveillance**</span>
:

Se protéger des grands réseaux publicitaires, comme Google et Facebook, ainsi que d'une myriade d'autres collecteurs de données tiers.

<span class="pg-green">:material-account-search: **Exposition publique**</span>
:

Limiter les informations vous concernant qui sont accessibles en ligne, aux moteurs de recherche ou au public.

<span class="pg-blue-gray">:material-close-outline: **Censure**</span>
:

Éviter l'accès censuré à l'information ou d'être censuré lorsque vous vous exprimez en ligne.

Certaines de ces menaces peuvent peser plus que d'autres en fonction de vos préoccupations. Par exemple, un développeur de logiciels ayant accès à des données précieuses ou critiques peut être principalement concerné par les <span class="pg-viridian">:material-package-variant-closed-remove: attaques de la chaîne d'approvisionnement</span> et les <span class="pg-red">:material-target-account: attaques ciblées</span>. Il voudra probablement tout de même protéger ses données personnelles pour éviter qu'elles ne soient englobées dans des programmes de <span class="pg-blue">:material-eye-outline: surveillance de masse</span>. De même, une « personne lambda » peut être principalement concernée par l'<span class="pg-green">:material-account-search: Exposition Publique</span> de ses données personnelles, mais devrait tout de même se méfier des problèmes de sécurité tels que les <span class="pg-orange">:material-bug-outline: Attaques Passives</span> comme les logiciels malveillants affectant ses appareils.

## Anonymat et vie privée

<span class="pg-purple">:material-incognito: Anonymat</span>

L'anonymat et le concept de vie privée sont deux concepts radicalement différents. Avoir une vie privée en ligne est un ensemble de choix que vous faites sur la façon dont vos données sont utilisées et partagées, alors que l'anonymat est la dissociation complète de vos activités en ligne de votre identité réelle.

Les lanceurs d'alerte et les journalistes, par exemple, peuvent avoir un modèle de menace beaucoup plus extrême nécessitant un anonymat total. Il ne s'agit pas seulement de cacher ce qu'ils font, les données dont ils disposent ou de ne pas se faire pirater par des hackers ou des gouvernements, mais aussi de cacher entièrement qui ils sont. Ils sont prêts à sacrifier tout type de commodité s'il s'agit de protéger leur anonymat, leur vie privée ou leur sécurité, car leur vie pourrait en dépendre. La plupart des gens n'ont pas besoin d'aller si loin.

## Sécurité et vie privée

<span class="pg-orange">:material-bug-outline: Attaques passives</span>

La sécurité et la vie privée sont souvent confondues, car vous avez besoin de sécurité pour obtenir tout semblant de vie privée. Utiliser des outils qui semblent respecter votre vie privée est futile s'ils peuvent facilement être exploités par des attaquants qui publieront vos données. Cependant, l'inverse n'est pas nécessairement vrai ; le service le plus sécurisé au monde *ne respecte pas nécessairement* votre vie privée. Le meilleur exemple est de confier des données à Google qui, compte tenu de leur envergure, ont connu un minimum d'incidents de sécurité grâce à l'emploi d'experts en sécurité de premier plan pour sécuriser leur infrastructure. Même si Google fournit un service très sécurisé, rares sont ceux qui considèrent que leurs données restent privées en utilisant leurs outils gratuits (Gmail, YouTube, etc).

En matière de sécurité des applications, nous ne savons généralement pas (et parfois ne pouvons pas) savoir si le logiciel que nous utilisons est malveillant, ou pourrait un jour le devenir. Même avec les développeurs les plus dignes de confiance, il n'y a généralement aucune garantie que leur logiciel ne présente pas une vulnérabilité grave qui pourrait être exploitée ultérieurement.

Pour minimiser les dommages potentiels qu'un logiciel malveillant *pourrait* causer, vous devez employer la sécurité par compartimentation. Il peut s'agir, par exemple, d'utiliser des ordinateurs différents pour des tâches différentes, d'utiliser des machines virtuelles pour séparer différents groupes d'applications connexes, ou d'utiliser un système d'exploitation sécurisé mettant l'accent sur le sandboxing des applications et le contrôle d'accès obligatoire.

<div class="admonition tip" markdown>
<p class="admonition-title">Conseil</p>

Les systèmes d'exploitation mobiles sont généralement plus sûrs que les systèmes d'exploitation de bureau en ce qui concerne le sandboxing des applications.

Les systèmes d'exploitation de bureau sont généralement à la traîne en ce qui concerne l'isolation l'isolation des applications. ChromeOS dispose de capacités d'isolation similaires à celles d'Android, et macOS dispose d'un contrôle complet des autorisations système (et les développeurs peuvent opter pour l'isolation pour les applications). Cependant, ces systèmes d'exploitation transmettent des informations d'identification à leurs constructeurs respectifs. Linux a tendance à ne pas soumettre d'informations aux fournisseurs de systèmes, mais il a une mauvaise protection contre les exploits et les applications malveillantes. Ce problème peut être quelque peu atténué avec des distributions spécialisées qui font un usage intensif des machines virtuelles ou des conteneurs, comme [Qubes OS](../desktop.md#qubes-os).

</div>

## Attaques contre des individus spécifiques

<span class="pg-red">:material-target-account: Attaques ciblées</span>

Les attaques ciblées contre une personne spécifique sont plus difficiles à gérer. Les voies d'attaque les plus courantes sont l'envoi de documents malveillants par courrier électronique, l'exploitation de vulnérabilités dans le navigateur et les systèmes d'exploitation, et les attaques physiques. Si cela vous préoccupe, il vous sera nécessaire de recourir à des stratégies plus avancées d'atténuation des menaces.

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

**Les navigateurs web**, **les clients de messagerie électronique** et **les applications de bureautique** exécutent généralement volontairement, et par conception, du code non fiable qui vous est envoyé par des tiers. L'exécution de plusieurs machines virtuelles pour séparer les applications de ce type de votre système hôte ainsi que les unes des autres est une technique que vous pouvez utiliser pour éviter qu'un code d'exploitation dans ces applications ne compromette le reste de votre système. Les technologies comme Qubes OS ou Microsoft Defender Application Guard sur Windows fournissent des méthodes pratiques pour le faire de manière transparente, par exemple.

</div>

Si vous êtes préoccupé par les **attaques physiques**, vous devriez utiliser un système d'exploitation doté d'une implémentation sécurisée de démarrage vérifié, comme Android, iOS, macOS ou [Windows (avec TPM)](https://learn.microsoft.com/windows/security/information-protection/secure-the-windows-10-boot-process). Vous devriez également vous assurer que votre disque est chiffré et que le système d'exploitation utilise un TPM, une [Enclave sécurisée](https://support.apple.com/guide/security/secure-enclave-sec59b0b31ff/1/web/1) ou un [Element sécurisé](https://developers.google.com/android/security/android-ready-se) pour limiter le taux de tentatives de saisie de la phrase de passe. Vous devriez éviter de partager votre ordinateur avec des personnes en qui vous n'avez pas confiance, car la plupart des systèmes d'exploitation de bureau ne chiffrent pas les données séparément par utilisateur.

## Attaques contre certaines organisations

<span class="pg-viridian">:material-package-variant-closed-remove: Attaques de la chaîne d'approvisionnement</span>

Les attaques de la chaîne d'approvisionnement sont souvent une forme d'<span class="pg-red">:material-target-account: attaque ciblée</span> visant les entreprises, les gouvernements et les activistes, bien qu'elles puissent également compromettre le grand public.

<div class="admonition example" markdown>
<p class="admonition-title">Example</p>

Un exemple notable s'est produit en 2017 lorsque M.E.Doc, un logiciel de comptabilité populaire en Ukraine, a été infecté par le virus *NotPetya*, infectant ensuite les personnes qui ont téléchargé ce logiciel avec un rançongiciel. NotPetya est une attaque par rançongiciel qui a touché plus de 2 000 entreprises dans différents pays. Elle est basée sur l'exploit *EternalBlue* mis au point par la NSA pour attaquer les ordinateurs Windows via le réseau.

</div>

Ce type d'attaque peut être mené de plusieurs manières :

1. Un collaborateur ou un employé peut d'abord se frayer un chemin jusqu'à une position de pouvoir au sein d'un projet ou d'une organisation, puis abuser de cette position en ajoutant un code malveillant.
2. Un développeur peut être contraint par un tiers d'ajouter un code malveillant.
3. Un individu ou un groupe peut identifier une dépendance logicielle tierce (également connue sous le nom de bibliothèque) et s'efforcer de l'infiltrer à l'aide des deux méthodes susmentionnées, en sachant qu'elle sera utilisée par les développeurs de logiciels "en aval".

Ces types d'attaques peuvent nécessiter beaucoup de temps et de préparation et sont risquées car elles peuvent être détectées, en particulier dans les projets open source s'ils sont populaires et s'ils suscitent un intérêt extérieur. Malheureusement, ce sont aussi parmi les plus dangereuses, car il est très difficile de les atténuer complètement. Nous encourageons les lecteurs à n'utiliser que des logiciels qui ont une bonne réputation et qui s'efforcent de réduire les risques en :

1. N'adoptant que des logiciels populaires qui existent depuis un certain temps. Plus l'intérêt pour un projet est grand, plus il y a de chances que des parties externes remarquent les changements malveillants. Un acteur malveillant devra également consacrer plus de temps à gagner la confiance de la communauté par des contributions significatives.
2. Trouvant des logiciels qui publient des binaires avec des plates-formes d'infrastructure de construction fiables et largement utilisées, par opposition aux stations de travail des développeurs ou aux serveurs auto-hébergés. Certains systèmes comme GitHub Actions vous permettent d'inspecter le script de construction qui s'exécute publiquement pour plus de confiance. Cela réduit la probabilité qu'un logiciel malveillant présent sur la machine d'un développeur puisse infecter ses paquets, et permet de s'assurer que les binaires produits sont bien produits correctement.
3. Recherchant la signature de code sur les commits individuels et les versions du code source, ce qui crée une trace vérifiable de qui a fait quoi. Par exemple : le code malveillant se trouvait-il dans le dépôt du logiciel ? Quel développeur l'a ajouté ? A-t-il été ajouté au cours du processus de construction ?
4. Vérifiant si le code source comporte des messages de commit significatifs (tels que les [commits conventionnels](https://conventionalcommits.org)) qui expliquent ce que la modification est censée accomplir. Des messages clairs peuvent faciliter la vérification, l'audit et la détection des bugs pour les personnes extérieures au projet.
5. Notant le nombre de contributeurs ou de mainteneurs d'un programme. Un développeur isolé peut être plus susceptible d'être contraint d'ajouter un code malveillant par un tiers, ou d'activer par négligence un comportement indésirable. Cela pourrait bien signifier que les logiciels développés par les "Géants du Web" font l'objet d'un examen plus approfondi que ceux d'un développeur isolé qui n'a de comptes à rendre à personne.

## Protection de ses données des fournisseurs de services

<span class="pg-teal">:material-server-network: Fournisseurs de service</span>

Nous vivons dans un monde où presque tout est connecté à Internet. Nos messages « privés », e-mails et nos interactions sociales sont généralement stockés sur un serveur quelque part. Généralement, lorsque vous envoyez un message à quelqu'un, ce message est alors stocké en clair sur un serveur, et lorsque votre ami souhaite lire le message, le serveur le lui montre.

Le problème évident avec cela est que le fournisseur de services (ou un pirate informatique qui a compromis le serveur) peut consulter vos conversations "privées" quand et comme il le souhaite, sans jamais que vous ne le sachiez. Cela s'applique à de nombreux services courants tels que la messagerie SMS, Telegram, Discord, etc.

Heureusement, le chiffrement de bout en bout peut atténuer ce problème en rendant illisibles les communications entre vous et vos destinataires avant même qu'elles ne soient envoyées au serveur. La confidentialité de vos messages est garantie, tant que le prestataire de services n'a pas accès aux clés privées d'une des deux personnes.

<div class="admonition note" markdown>
<p class="admonition-title">Remarque sur le chiffrement basé sur le web</p>

Dans la pratique, l'efficacité des différentes mises en œuvre du chiffrement de bout en bout varie. Des applications telles que [Signal](../real-time-communication.md#signal) s'exécutent nativement sur votre appareil, et chaque copie de l'application est la même sur différentes installations. Si le fournisseur de services venait à ouvrir une porte dérobée dans son application pour tenter de voler vos clés privées, cela pourrait être détecté ultérieurement par rétro-ingénierie.

D'autre part, les implémentations E2EE basées sur le web, telles que l'application web de Proton Mail ou *Web Vault* de Bitwarden, s'appuient sur le serveur qui sert dynamiquement le code JavaScript au navigateur pour gérer la cryptographie. Un serveur malveillant peut vous cibler et vous envoyer un code JavaScript malveillant pour voler votre clé de chiffrement (et il serait extrêmement difficile de le remarquer). Même si cette personne s'aperçoit de la tentative de vol de sa clé, il serait incroyablement difficile de prouver que c'est le fournisseur qui tente de le faire, car le serveur peut choisir de servir différents clients web à différentes personnes.

Par conséquent, lorsque vous comptez sur le chiffrement de bout en bout, vous devriez choisir d'utiliser des applications natives plutôt que des clients web, dans la mesure du possible.

</div>

Même avec le chiffrement de bout en bout, les fournisseurs de services peuvent toujours vous profiler sur la base des **métadonnées**, qui ne sont généralement pas protégées. Si le fournisseur de services ne peut pas lire vos messages, il peut néanmoins observer des éléments importants, tels que les personnes à qui vous parlez, la fréquence des messages que vous leur envoyez et les moments où vous êtes généralement actif. La protection des métadonnées est assez rare, et vous devriez prêter une attention particulière à la documentation technique du logiciel que vous utilisez pour voir s'il y a une minimisation ou une protection des métadonnées, si cela vous préoccupe.

## Programmes de surveillance de masse

<span class="pg-blue">:material-eye-outline: Surveillance de masse</span>

La surveillance de masse est un effort visant à surveiller le "comportement, de nombreuses activités ou les informations" d'une population entière (ou d'une fraction substantielle d'une population).[^1] Elle fait souvent référence à des programmes gouvernementaux, tels que ceux [divulgués par Edward Snowden en 2013](https://en.wikipedia.org/wiki/Global_surveillance_disclosures_(2013%E2%80%93present)). Cependant, elle peut également être réalisée par des entreprises, soit pour le compte d'agences gouvernementales, soit de leur propre initiative.

<div class="admonition abstract" markdown>
<p class="admonition-title">Atlas de la surveillance</p>

Si vous souhaitez en savoir plus sur les méthodes de surveillance et la manière dont elles sont mises en œuvre dans votre ville, vous pouvez également consulter l'[Atlas de la surveillance](https://atlasofsurveillance.org/) de l'[Electronic Frontier Foundation](https://eff.org/).

En France, vous pouvez consulter le [site Technopolice](https://technopolice.fr/villes) tenu par l'association à but non lucratif La Quadrature du Net.

</div>

Les gouvernements justifient souvent les programmes de surveillance de masse comme des moyens nécessaires pour combattre le terrorisme et prévenir la criminalité. Toutefois, en tant que violations des droits de l'homme, elles sont le plus souvent utilisées pour cibler de manière disproportionnée les groupes minoritaires et les dissidents politiques, entre autres.

<div class="admonition quote" markdown>
<p class="admonition-title">ACLU: <em><a href="https://aclu.org/news/national-security/the-privacy-lesson-of-9-11-mass-surveillance-is-not-the-way-forward">The Privacy Lesson of 9/11: Mass Surveillance is Not the Way Forward</a></em></p>

Après les révélations d'Edward Snowden sur des programmes gouvernementaux tels que [PRISM](https://en.wikipedia.org/wiki/PRISM) et [Upstream](https://en.wikipedia.org/wiki/Upstream_collection), les responsables du renseignement ont également admis que la NSA collectait secrètement depuis des années des enregistrements sur pratiquement tous les appels téléphoniques des Américains - qui appelle qui, quand ces appels sont effectués et combien de temps ils durent. Ce type d'informations, lorsqu'il est amassé par la NSA quotidiennement, peut révéler des détails terriblement sensibles sur la vie des gens en associant ces données : s'ils ont appelé un pasteur, une clinique d'avortement, un centre d'addiction ou une ligne d'assistance contre le suicide par exemple.

</div>

Malgré la surveillance de masse croissante aux États-Unis, le gouvernement a constaté que les programmes de surveillance de masse comme la section 215 ont eu "peu de valeur unique" en ce qui concerne l'arrêt de crimes réels ou de complots terroristes, les efforts faisant largement double emploi avec les programmes de surveillance ciblée du FBI.[^2]

En ligne, vous pouvez être suivi par une grande variété de méthodes, y compris, mais pas que, par :

- Votre adresse IP
- Les cookies de votre navigateur
- Les données que vous soumettez aux sites web
- L'empreinte numérique de votre navigateur ou de votre appareil
- La corrélation des modes de paiement

Si vous êtes préoccupé par les programmes de surveillance de masse, vous pouvez utiliser des stratégies comme cloisonner vos identités virtuelles, vous fondre dans la masse des utilisateurs, ou, dans la mesure du possible, simplement éviter de renseigner des informations qui pourraient permettre de vous identifier.

## La surveillance comme modèle économique

<span class="pg-brown">:material-account-cash: Capitalisme de surveillance</span>

> Le capitalisme de surveillance est un système économique centré sur la collecte et la marchandisation des données personnelles dont le principal but est de faire du profit.[^3]

Pour de nombreuses personnes, le pistage et la surveillance par des sociétés privées constituent une préoccupation croissante. Les réseaux publicitaires omniprésents, tels que ceux exploités par Google et Facebook, s'étendent sur internet bien au-delà des sites qu'ils contrôlent et suivent vos actions tout le long de votre navigation. L'utilisation d'outils tels que des bloqueurs de contenu pour limiter les requêtes du réseau vers leurs serveurs, et la lecture des politiques de confidentialité des services que vous utilisez peuvent vous aider à éviter de nombreux adversaires de base (bien que cela ne puisse pas empêcher complètement le pistage).[^4]

En outre, même les entreprises n'appartenant pas au secteur de l'*AdTech* ou du suivi peuvent partager vos informations avec des [courtiers en données](https://en.wikipedia.org/wiki/Information_broker) (tels que Cambridge Analytica, Experian ou Datalogix) ou d'autres parties. Vous ne pouvez pas automatiquement supposer que vos données sont en sécurité simplement parce que le service que vous utilisez n'a pas un modèle économique typique de l'AdTech ou du pistage. La meilleure protection contre la collecte de données par les entreprises est de chiffrer ou d'obscurcir vos données dans la mesure du possible, afin qu'il soit plus difficile pour les différents fournisseurs de corréler les données entre elles et d'établir un profil sur vous.

## Limiter l'information publique

<span class="pg-green">:material-account-search: Exposition publique</span>

La meilleure façon de préserver la confidentialité de vos données est tout simplement de ne pas les mettre en ligne. La suppression des informations indésirables que vous trouvez sur vous en ligne est l'une des meilleures premières mesures que vous pouvez prendre pour retrouver votre vie privée.

- [Consultez notre guide sur la suppression de compte :material-arrow-right-drop-circle:](account-deletion.md)

Il est très important de vérifier les paramètres de confidentialité de votre compte pour limiter la diffusion de ces données sur les sites dans lesquels vous partagez des informations. Par exemple, activez le "mode privé" sur vos comptes si vous en avez la possibilité : cela garantit que votre compte n'est pas indexé par les moteurs de recherche et qu'il ne peut pas être consulté sans votre permission.

Si vous avez déjà soumis vos véritables informations à des sites qui ne devraient pas les avoir, envisagez d'utiliser des tactiques de désinformation, comme la soumission d'informations fictives liées à cette identité en ligne. Vos vraies informations seront alors indiscernables des fausses informations.

## Éviter la censure

<span class="pg-blue-gray">:material-close-outline: Censure</span>

La censure en ligne peut être exercée (à des degrés divers) par des acteurs tels que des gouvernements totalitaires, des administrateurs de réseaux et des fournisseurs de services. Ces efforts pour contrôler la communication et restreindre l'accès à l'information seront toujours incompatibles avec le droit humain à la liberté d'expression.[^5]

La censure sur les plateformes privées est de plus en plus courante, car des plateformes comme Twitter et Facebook cèdent à la demande du public, aux pressions du marché et à celles des agences gouvernementales. Les pressions gouvernementales peuvent prendre la forme de demandes secrètes adressées aux entreprises, comme la Maison Blanche [demandant le retrait](https://nytimes.com/2012/09/17/technology/on-the-web-a-fine-line-on-free-speech-across-globe.html) d'une vidéo provocante sur YouTube, ou de demandes manifestes, comme le gouvernement chinois exigeant des entreprises qu'elles adhèrent à un régime de censure strict.

Les personnes préoccupées par la menace de la censure peuvent utiliser des technologies comme [Tor](../advanced/tor-overview.md) pour la contourner et soutenir des plateformes de communication résistantes à la censure comme [Matrix](../social-networks.md#element), qui ne dispose pas d'une autorité de compte centralisée pouvant fermer des comptes de manière arbitraire.

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

S'il peut être facile d'échapper à la censure en soi, cacher le fait que vous le faites peut être très problématique.

Vous devez prendre en compte quels aspects du réseau votre adversaire peut observer, et si vous avez une possibilité de déni plausible pour vos actions. Par exemple, l'utilisation de [DNS chiffrés](../advanced/dns-overview.md#what-is-encrypted-dns) peut vous aider à contourner les systèmes de censure rudimentaires basés sur les DNS, mais elle ne peut pas vraiment cacher ce que vous visitez à votre FAI. Un VPN ou Tor peut aider à cacher ce que vous visitez aux administrateurs du réseaux, mais ne peut pas cacher que vous utilisez ces réseaux. Les transports enfichables (tels que Obfs4proxy, Meek ou Shadowsocks) peuvent vous aider à contourner les pare-feu qui bloquent les protocoles VPN courants ou Tor, mais vos tentatives de contournement peuvent toujours être détectées par des méthodes telles que le sondage ou [l'inspection approfondie des paquets](https://fr.wikipedia.org/wiki/Deep_packet_inspection).

</div>

Vous devez toujours tenir compte des risques encourus en essayant de contourner la censure, des conséquences potentielles et du degré de sophistication de votre adversaire. Soyez très prudent dans le choix de vos logiciels et prévoyez un plan de secours au cas où vous seriez pris.

[^1]: Commission de surveillance de la vie privée et des libertés civiles des États-Unis : [Rapport sur le programme d'enregistrements téléphoniques mené en vertu de la section 215](https://documents.pclob.gov/prod/Documents/OversightReport/ec542143-1079-424a-84b3-acc354698560/215-Report_on_the_Telephone_Records_Program.pdf)
[^2]: Conseil de surveillance de la vie privée et des libertés civiles des États-Unis : [*Rapport sur le programme d'enregistrements téléphoniques mené en vertu de la section 215*](https://documents.pclob.gov/prod/Documents/OversightReport/ec542143-1079-424a-84b3-acc354698560/215-Report_on_the_Telephone_Records_Program.pdf)
[^3]: Wikipédia : [*Capitalisme de surveillance*](https://en.wikipedia.org/wiki/Surveillance_capitalism)
[^4]: "[Énumérer la méchanceté](https://ranum.com/security/computer_security/editorials/dumb)" (ou "énumérer toutes les mauvaises choses que nous connaissons") comme le font de nombreux bloqueurs de contenu et programmes antivirus, ne permet pas de vous protéger correctement contre les menaces nouvelles et inconnues, car elles n'ont pas encore été ajoutées à la liste des filtres. Vous devriez également utiliser d'autres techniques d'atténuation.
[^5]: Nations Unies : [*Déclaration universelle des droits de l'homme*](https://un.org/en/about-us/universal-declaration-of-human-rights).
