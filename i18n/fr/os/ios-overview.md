---
title: iOS Overview
icon: simple/apple
description: iOS is a mobile operating system developed by Apple for the iPhone.
---

**iOS** et **iPadOS** sont des systèmes d'exploitation mobiles propriétaires développés par Apple pour ses produits iPhone et iPad, respectivement. Si vous possédez un appareil mobile Apple, vous pouvez améliorer votre vie privée en désactivant certaines fonctions de télémétrie intégrées et en renforçant certains paramètres de sécurité et de protection de la vie privée intégrés au système.

## Remarques concernant la vie privée

Les experts en sécurité font souvent l'éloge des appareils iOS pour leur solide protection des données et leur respect des meilleures pratiques modernes. Cependant, le caractère restrictif de l'écosystème d'Apple - en particulier avec ses appareils mobiles - continue d'entraver la protection de la vie privée de plusieurs manières.

Nous considérons généralement qu'iOS offre des protections de la vie privée et de la sécurité supérieures à la moyenne pour la plupart des gens, par rapport aux appareils Android d'origine, quel que soit le fabricant. Cependant, vous pouvez atteindre des normes de vie privée encore plus élevées avec un [système d'exploitation Android personnalisé](../android.md) comme GrapheneOS, si vous voulez ou devez être complètement indépendant des services cloud d'Apple ou de Google.

### Verrouillage d'activation

Tous les appareils iOS doivent être vérifiés sur les serveurs de verrouillage d'activation d'Apple lors de leur configuration initiale ou de leur réinitialisation, ce qui signifie qu'une connexion internet est **nécessaire** pour utiliser un appareil iOS.

### App Store obligatoire

La seule source d'applications sur iOS est l'App Store d'Apple, dont l'accès nécessite un identifiant Apple. Cela signifie qu'Apple dispose d'un enregistrement de chaque application que vous installez sur votre appareil et qu'elle peut probablement relier ces informations à votre identité réelle si vous fournissez à l'App Store une méthode de paiement.

### Télémétrie invasive

Apple a, par le passé, eu des problèmes pour anonymiser correctement ses données télémétriques sur iOS. [En 2019](https://www.theguardian.com/technology/2019/jul/26/apple-contractors-regularly-hear-confidential-details-on-siri-recordings), il a été constaté qu'Apple transmettait des enregistrements Siri - dont certains contenaient des informations hautement confidentielles - à ses serveurs pour qu'ils soient examinés manuellement par des contractants tiers. Bien qu'ils aient temporairement arrêté ce programme après que cette pratique ait été [largement signalée](https://www.theverge.com/2019/8/23/20830120/apple-contractors-siri-recordings-listening-1000-a-day-globetech-microsoft-cortana), le problème n'a été complètement résolu [qu'en 2021](https://www.theguardian.com/technology/2021/jun/07/apple-overhauls-siri-to-address-privacy-concerns-and-improve-performance).

Plus récemment, il a été constaté qu'Apple [transmettait des données analytiques même lorsque le partage des données analytiques était désactivé](https://gizmodo.com/apple-iphone-analytics-tracking-even-when-off-app-store-1849757558) sur iOS, et ces données [semblent](https://twitter.com/mysk_co/status/1594515229915979776) être facilement reliées à des identifiants de compte iCloud uniques, bien qu'elles soient censées être anonymes.

## Configuration recommandée

### iCloud

La majorité des préoccupations relatives à la protection de la vie privée et à la sécurité des produits Apple sont liées à leurs services cloud, et non à leurs matériels ou à leurs logiciels. Lorsque vous utilisez des services Apple comme iCloud, la plupart de vos informations sont stockées sur leurs serveurs et sécurisées par des clés auxquelles Apple a accès par défaut. Vous pouvez consulter [la documentation d'Apple](https://support.apple.com/HT202303) pour savoir quels services sont chiffrés de bout en bout. Tout ce qui est mentionné comme étant "en transit" ou "sur serveur" signifie qu'il est possible pour Apple d'accéder à ces données sans votre permission. Ce niveau d'accès a parfois été utilisé de manière abusive par les forces de l'ordre pour contourner le fait que vos données sont par ailleurs chiffrées de manière sécurisée sur votre appareil, et bien sûr Apple est vulnérable aux fuites de données comme toute autre entreprise.

Par conséquent, si vous utilisez iCloud, vous devriez [activer la **protection avancée des données**](https://support.apple.com/HT212520). Cela permet de chiffrer la quasi-totalité de vos données iCloud à l'aide de clés stockées sur vos appareils (chiffrement de bout en bout), plutôt que sur les serveurs d'Apple, de sorte que vos données iCloud sont sécurisées en cas de fuite de données, et qu'elles sont par ailleurs cachées à Apple.

Le chiffrement utilisé par la protection avancée des données, bien que puissant, [n'est pas *aussi* robuste](https://discuss.privacyguides.net/t/apple-advances-user-security-with-powerful-new-data-protections/10778/4) que le chiffrement offert par d'autres [services cloud](../cloud.md), en particulier lorsqu'il s'agit d'iCloud Drive. Bien que nous vous recommandons vivement d'utiliser la protection avancée des données si vous utilisez iCloud, nous vous suggérons également d'envisager de trouver une alternative à iCloud auprès d'un [fournisseur de services plus axé sur la vie privée](../tools.md), bien qu'il soit peu probable que la plupart des gens soient affectés par ces bizarreries de chiffrement.

Vous pouvez également protéger vos données en limitant ce que vous synchronisez sur iCloud. En haut de l'application **Réglages**, vous verrez votre nom et votre photo de profil si vous êtes connecté à iCloud. Sélectionnez-les, puis **iCloud**, et désactivez les services que vous ne souhaitez pas synchroniser avec iCloud. Il se peut que des applications tierces soient répertoriées sous **Voir Tout** si elles se synchronisent avec iCloud, ce que vous pouvez désactiver ici.

#### iCloud+

Un abonnement payant à **iCloud+** (avec n'importe quelle offre de stockage iCloud) est assorti de fonctionnalités de protection de la vie privée. Bien qu'elles puissent fournir un service adéquat aux clients actuels d'iCloud, nous ne recommanderions pas l'achat d'une offre iCloud+ plutôt qu'un [VPN](../vpn.md) et qu'un [service d'alias d'e-mail indépendant](../email.md#email-aliasing-services), rien que pour ces fonctionnalités.

**Relai privé** est un service proxy qui relaie votre trafic Safari à travers deux serveurs : l'un appartenant à Apple et l'autre à un fournisseur tiers (notamment Akamai, Cloudflare et Fastly). En théorie, cela devrait empêcher tout fournisseur de la chaîne, y compris Apple, d'avoir une complète visibilité sur les sites web que vous visitez lorsque vous êtes connecté. Contrairement à un VPN complet, relai privé ne protège pas le trafic de vos applications en dehors de Safari.

**Masquer mon adresse e-mail** est le service d'alias de d'e-mail d'Apple. Vous pouvez créer un alias d'e-mail gratuitement lorsque vous faite *Se connecter avec Apple* sur un site web ou une application, ou générer un nombre illimité d'alias à la demande avec une offre iCloud+ payante. Masque mon adresse e-mail a l'avantage d'utiliser le domaine `@icloud.com` pour ses alias, ce qui peut être moins susceptible d'être bloqué par rapport à d'autres services d'alias d'email, mais n'offre pas de fonctionnalité offerte par des services indépendants tels que le chiffrement PGP automatique ou la prise en charge de plusieurs boîtes aux lettres.

#### Médias & achats

En haut de l'application **Réglages**, vous verrez votre nom et votre photo de profil si vous êtes connecté à un identifiant Apple. Sélectionnez les, puis sélectionnez **Médias & Achats** > **Voir Compte**.

- [ ] Désactivez **Recommandations Personnalisées**

#### Localiser

**Localiser** est un service qui vous permet de suivre vos appareils Apple et de partager votre localisation avec vos amis et votre famille. Il vous permet également d'effacer votre appareil à distance en cas de vol, empêchant ainsi un voleur d'accéder à vos données. Vos [données de localisation Localiser sont E2EE](https://www.apple.com/legal/privacy/data/fr/find-my/) lorsque :

- Votre position est partagée avec un membre de votre famille ou un ami, et vous utilisez tous deux iOS 15 ou une version ultérieure.
- Votre appareil est hors ligne et est localisé par le réseau de Localiser.

Vos données de localisation ne sont pas E2EE lorsque votre appareil est en ligne et que vous utilisez Localiser mon iPhone à distance pour localiser votre appareil. C'est à vous de décider si ces compromis valent les avantages antivol du verrouillage d'activation.

En haut de l'application **Réglages**, vous verrez votre nom et votre photo de profil si vous êtes connecté à un identifiant Apple. Sélectionnez-les, puis selectionnez **Localiser**. Vous pouvez ici choisir d'activer ou de désactiver les fonctions de Localiser ma position.

### Paramètres

De nombreux autres paramètres liés à la protection de la vie privée peuvent être trouvés dans l'application **Réglages**.

#### Mode avion

Activation du **mode avion** empêche votre téléphone de contacter les antennes cellulaires. Vous pourrez toujours vous connecter au Wi-Fi et au Bluetooth, donc chaque fois que vous êtes connecté au Wi-Fi, vous pouvez activer ce paramètre.

#### Wi-Fi

Vous pouvez activer la randomisation de l'adresse matérielle pour vous protéger contre le pistage des réseaux Wi-Fi. Sur le réseau auquel vous êtes actuellement connecté, appuyez sur le bouton :material-information: :

- [x] Activez **Adresse Wi-Fi privée**

Vous avez également la possibilité de **Limiter le suivi de l'adresse IP**. Cette fonction est similaire au relais privé iCloud, mais n'affecte que les connexions aux "traqueurs connus". Étant donné qu'il n'affecte que les connexions à des serveurs potentiellement malveillants, vous pouvez probablement laisser ce paramètre activé, mais si vous ne voulez *pas* que le trafic soit acheminé via les serveurs d'Apple, vous devriez le désactiver.

#### Bluetooth

**Bluetooth** doit être désactivé lorsque vous ne l'utilisez pas, car il augmente votre surface d'attaque. La désactivation du Bluetooth (ou du Wi-Fi) via le Centre de contrôle n'est que temporaire : vous devez le désactiver dans Paramètres pour que la désactivation soit effective.

- [ ] Désactivez **Bluetooth**

#### Général

Le nom d'appareil de votre iPhone contient par défaut votre prénom, qui sera visible par tous les utilisateurs des réseaux auxquels vous vous connectez. Vous devriez le remplacer par quelque chose de plus générique, comme "iPhone". Sélectionnez **Informations** > **Nom** et saisissez le nom de l'appareil que vous préférez.

Il est important d'installer fréquemment les **mises à jour logicielles** pour bénéficier des derniers correctifs de sécurité. Vous pouvez activer les **mises à jour automatiques** pour maintenir votre téléphone à jour sans avoir à vérifier constamment. Sélectionnez **Mise à jour logicielle** > **MAJ automatiques** :

- [x] Activez **Télécharger les mises à jour d'iOS**
- [x] Activez **Installer les mises à jour d'iOS**
- [x] Activez **Mises à jour de sécurité et fichiers système**

**AirDrop** vous permet de transférer facilement des fichiers, mais il peut permettre à des inconnus de vous envoyer des fichiers que vous ne souhaitez pas.

- [x] Sélectionnez **AirDrop** > **Réception désactivée**

**AirPlay** vous permet de diffuser de manière transparente du contenu de votre iPhone vers un téléviseur, mais vous n'en avez pas toujours besoin. Sélectionnez **AirDrop et Handoff** > **AirPlay automatique vers les téléviseurs** :

- [x] Sélectionnez **Jamais** ou **Demander**

**Actualisation des applications en arrière-plan** permet à vos applications d'actualiser leur contenu lorsque vous ne les utilisez pas. Cela peut les amener à établir des connexions non souhaitées. La désactivation de cette fonction permet également d'économiser la batterie, mais elle peut affecter la capacité d'une application à recevoir des informations actualisées, en particulier les applications de météo et de messagerie.

Sélectionnez **Actualisation des applications en arrière-plan** et désactivez toutes les applications que vous ne souhaitez pas voir actualisées en arrière-plan. Si vous ne souhaitez pas qu'une application soit actualisée en arrière-plan, vous pouvez sélectionner à nouveau **Actualisation des applications en arrière-plan** et la **désactiver**.

#### Siri et recherche

Si vous ne voulez pas que quelqu'un puisse contrôler votre téléphone avec Siri lorsqu'il est verrouillé, vous pouvez le désactiver ici.

- [ ] Désactivez **Autoriser Siri lorsque le téléphone est vérouillé**

#### Face ID/Touch ID et code

Définir un mot de passe fort pour votre téléphone est la mesure la plus importante que vous puissiez prendre pour assurer la sécurité physique de votre appareil. Vous devrez faire des compromis entre la sécurité et la commodité : un mot de passe plus long sera fastidieux à saisir à chaque fois, mais un mot de passe ou un code PIN plus court sera plus facile à deviner. Configurer Face ID ou Touch ID avec un mot de passe fort peut être un bon compromis entre convivialité et sécurité.

Sélectionnez **Activer le code d'accès** ou **Modifier le code d'accès** > **Options du code d'accès** > **Code alphanumérique personnalisé**. Veillez à créer un [mot de passe sûr](https://www.privacyguides.org/basics/passwords-overview/).

Si vous souhaitez utiliser Face ID ou Touch ID, vous pouvez le configurer maintenant. Votre téléphone utilisera le mot de passe que vous avez défini précédemment comme solution de secours en cas d'échec de la vérification biométrique. Les méthodes de déverrouillage biométrique existent principalement pour la commodité, même si elles empêchent les caméras de surveillance ou les personnes de vous regarder saisir votre code d'accès par-dessus votre épaule.

Si vous utilisez les déverouillages biométriques, vous devez savoir comment les désactiver rapidement en cas d'urgence. Maintenir enfoncé le bouton latéral ou le bouton d'alimentation et *l'un* des boutons de volume jusqu'à ce que vous voyiez le curseur Glisser pour éteindre désactivera la biométrie, exigeant votre code d'accès pour déverrouiller. Votre code d'accès sera également requis après le redémarrage de l'appareil.

Sur certains appareils plus anciens, vous devrez peut-être appuyer cinq fois sur le bouton d'alimentation pour désactiver la biométrie ou, pour les appareils dotés de Touch ID, il vous suffira de maintenir le bouton d'alimentation enfoncé, sans rien d'autre. Veillez à faire un essai préalable afin de savoir quelle méthode fonctionne pour votre appareil.

**Protection en cas de vol de l’appareil** est une nouvelle fonctionnalité d'iOS 17.3 qui ajoute une sécurité supplémentaire destinée à protéger vos données personnelles si votre appareil est volé alors qu'il est déverrouillé. Si vous utilisez la biométrie et la fonction Localiser dans vos réglages Apple ID, nous vous recommandons d'activer cette nouvelle protection :

- [x] Sélectionnez **Activer la protection**

Après avoir activé la protection en cas de vol de l’appareil, [certaines actions](https://support.apple.com/en-us/HT212510) nécessiteront une authentification biométrique sans possibilité de recourir au mot de passe (dans le cas où un passant obtient votre code PIN à la dérobée), comme l'utilisation du remplissage des mots de passe, l'accès aux informations de paiement et la désactivation du mode perdu. Elle ajoute également un délai de sécurité pour certaines actions effectuées en dehors de votre domicile ou d'un autre "lieu familier", comme la nécessité d'un délai d'une heure pour réinitialiser votre mot de passe Apple ID ou vous déconnecter de votre Apple ID. Ce délai a pour but de vous donner le temps d'activer le mode Perdu et de sécuriser votre compte avant qu'un voleur ne puisse réinitialiser votre appareil.

**Autoriser l'accès lorsque le téléphone est verrouillé** vous offre des options pour définir ce que vous pouvez autoriser lorsque votre téléphone est verrouillé. Plus vous désactivez d'options, moins quelqu'un qui n'a pas votre mot de passe peut faire de choses, mais moins c'est pratique pour vous. Choisissez les éléments auxquels vous ne voulez pas que quelqu'un ait accès s'il met la main sur votre téléphone.

- [ ] Désactivez **Aujourd'hui et recherche**
- [ ] Désactivez **Centre de notifications**
- [ ] Désactivez **Centre de contrôle**
- [ ] Désactivez **Gadgets de l'écran de verrouillage**
- [ ] Désactivez **Siri**
- [ ] Désactivez **Répondre avec Message**
- [ ] Désactivez **Contrôle de la maison**
- [ ] Désactivez **Portefeuille**
- [ ] Désactivez **Retourner les appels manqués**
- [ ] Désactivez **Accessoires USB**

Les iPhones sont déjà résistants aux attaques par force brute en vous faisant attendre de longues périodes de temps après plusieurs tentatives infructueuses ; cependant, il y a toujours eu des exploits pour contourner cette protection. Pour plus de sécurité, vous pouvez configurer votre téléphone pour qu'il s'efface de lui-même après 10 tentatives infructueuses de saisie du code d'accès.

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

Si ce paramètre est activé, quelqu'un peut intentionnellement effacer votre téléphone en entrant plusieurs fois le mauvais mot de passe. Assurez-vous d'avoir des sauvegardes appropriées et n'activez ce paramètre que si vous vous sentez à l'aise avec ça.

</div>

- [x] Activez **Effacer les données**

#### Confidentialité et sécurité

Les **services de localisation** vous permettent d'utiliser des fonctions telles que Localiser et Plan. Si vous n'avez pas besoin de ces fonctionnalités, vous pouvez désactiver les services de localisation. Vous pouvez également passer en revue et choisir les applications qui peuvent utiliser votre position ici. Sélectionnez **Services de localisation** :

- [ ] Désactivez **Services de localisation**

Vous pouvez décider ici d'autoriser les applications à demander à vous **suivre**. La désactivation de cette fonction empêche toutes les applications de vous suivre à l'aide de l'identifiant publicitaire de votre téléphone. Sélectionnez **Suivi** :

- [ ] Désactivez **Autoriser les demandes de suivi des apps**

Vous devriez désactiver **Données de capteur et d’utilisation à des fins de recherche** si vous ne souhaitez pas participer à des études. Sélectionnez **Données de capteur et d’utilisation à des fins de recherche** :

- [ ] Désactivez **Collecte de données de capteur et d'utilisation**

**Contrôle de sécurité** vous permet de visualiser et de révoquer rapidement certaines personnes et applications qui pourraient avoir l'autorisation d'accéder à vos données. Ici, vous pouvez effectuer une **Réinitialisation d'urgence**, qui réinitialise immédiatement les autorisations de toutes les personnes et applications susceptibles d'avoir accès aux ressources de l'appareil, et vous pouvez utiliser **Gérer les partages et les accès**, qui vous permet de passer en revue et de personnaliser qui et quoi a accès aux ressources de votre appareil et de votre compte.

Vous devriez désactiver l'analyse si vous ne souhaitez pas envoyer de données d'utilisation à Apple. Sélectionnez **Analyse et améliorations** :

- [ ] Désactivez **Partager l'analyse de l'iPhone** ou **Partager l’analyse (iPhone+Watch)**
- [ ] Désactivez **Partager l’analyse d’iCloud**
- [ ] Désactivez **Améliorer Fitness+**
- [ ] Désactivez **Améliorer la sécurité**
- [ ] Décochez **Améliorer Siri et Dictée**

Désactivez **Publicités personnalisées** si vous ne voulez pas de publicités ciblées. Sélectionnez **Publicité Apple**

- [ ] Décochez **Publicités personnalisées**

**Rapport de confidentialité des apps** est un outil intégré qui vous permet de voir quelles sont les autorisations utilisées par vos applications. Sélectionnez **Rapport de confidentialité des apps** :

- [x] Sélectionnez **Activer le rapport de confidentialité des apps**

Le [mode Isolement](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode) est un paramètre de sécurité que vous pouvez activer pour rendre votre téléphone plus résistant aux attaques. Sachez que certaines applications et fonctionnalités [ne fonctionneront pas](https://support.apple.com/fr-fr/HT212650) comme elles le font normalement.

- [x] Sélectionnez **Activer le mode Isolement**

## Conseils supplémentaires

### Appels E2EE

Les appels téléphoniques normaux effectués avec l'application Téléphone par l'intermédiaire de votre opérateur ne sont pas E2EE. Les appels FaceTime Vidéo et FaceTime Audio sont E2EE, ou vous pouvez utiliser [une autre application](../real-time-communication.md) comme Signal.

### Éviter le jailbreaking

Le jailbreaking d'un iPhone compromet sa sécurité et vous rend vulnérable. L'exécution de logiciels tiers non fiables peut entraîner l'infection de votre appareil par des logiciels malveillants.

### iMessage chiffré

La couleur de la bulle de message dans l'application Messages indique si vos messages sont E2EE ou non. Une bulle bleue indique que vous utilisez iMessage avec E2EE, tandis qu'une bulle verte indique qu'ils utilisent les protocoles SMS et MMS obsolètes. Actuellement, le seul moyen d'obtenir l'E2EE dans Messages est que les deux correspondants utilisent iMessage sur des appareils Apple.

Si vous ou votre partenaire de messagerie avez activé la sauvegarde iCloud sans la protection avancée des données, la clé de chiffrement sera stockée sur les serveurs d'Apple, ce qui signifie qu'ils peuvent accéder à vos messages. En outre, l'échange de clés d'iMessage n'est pas aussi sûr que d'autres implémentations, comme Signal (qui permet de voir la clé du destinataire et de vérifier par QR code), et ne doit donc pas être utilisé pour des communications particulièrement sensibles.

### Caviardage des visages/informations

Si vous devez masquer des informations dans une photo, vous pouvez utiliser les outils intégrés d'Apple pour le faire. Ouvrez la photo que vous souhaitez modifier, appuyez sur Modifier dans le coin supérieur droit de l'écran, puis appuyez sur le symbole de marquage en haut à droite. Appuyez sur le plus en bas à droite de l'écran, puis sur l'icône de rectangle. Vous pouvez maintenant placer un rectangle n'importe où sur l'image. Veillez à appuyer sur l'icône de forme en bas à gauche et à sélectionner le rectangle rempli. **N'utilisez pas** le surligneur pour obscurcir des informations, car son opacité n'est pas tout à fait de 100 %.

### Bêtas iOS

Apple met toujours des versions bêta d'iOS à la disposition de ceux qui souhaitent aider à trouver et à signaler des bogues. Nous vous déconseillons d'installer des logiciels bêta sur votre téléphone. Les versions bêta sont potentiellement instables et peuvent présenter des failles de sécurité non découvertes.

## Points forts en matière de sécurité

### Avant le premier déverrouillage

Si votre modèle de menace comprend des outils d'investigation et que vous souhaitez minimiser les risques d'utilisation d'exploits pour accéder à votre téléphone, vous devriez redémarrer votre appareil fréquemment. L'état *après* un redémarrage mais *avant* le déverrouillage de votre appareil est appelé "Before First Unlock" (BFU), et lorsque votre appareil est dans cet état, il est [nettement plus difficile](https://belkasoft.com/checkm8_glossary) pour les outils de criminalistique d'exploiter des vulnérabilités pour accéder à vos données. Cet état BFU vous permet de recevoir des notifications pour les appels, les textes et les alarmes, mais la plupart des données de votre appareil sont toujours chiffrées et inaccessibles. Cela peut s'avérer peu pratique, il convient donc de se demander si ces compromis sont judicieux dans votre situation.
