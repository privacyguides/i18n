---
title: Sur iOS
icon: simple/apple
description: iOS est un système d'exploitation mobile développé par Apple pour l'iPhone.
---

**iOS** et **iPadOS** sont des systèmes d'exploitation mobiles propriétaires développés par Apple pour ses produits iPhone et iPad, respectivement. Si vous possédez un appareil mobile Apple, vous pouvez améliorer votre vie privée en désactivant certaines fonctions de télémétrie intégrées et en renforçant certains paramètres de sécurité et de protection de la vie privée intégrés au système.

## Remarques concernant la vie privée

Les experts en sécurité font souvent l'éloge des appareils iOS pour leur politique protection des données et leur respect des pratiques modernes de sécurité. Cependant, le caractère restrictif de l'écosystème d'Apple - en particulier avec ses appareils mobiles - continue d'entraver la protection de la vie privée de plusieurs manières.

Nous considérons généralement qu'iOS offre des protections de la vie privée et de la sécurité supérieures à la moyenne pour la plupart des gens, par rapport aux appareils Android d'origine, quel que soit le fabricant. Cependant, vous pouvez atteindre des normes de confidentialité encore plus élevées avec un [système d'exploitation Android alternatif](../android/distributions.md) comme GrapheneOS, si vous voulez ou devez être complètement indépendant des services cloud d'Apple ou de Google.

### Verrouillage d'activation

Tous les appareils iOS doivent être vérifiés sur les serveurs de verrouillage d'activation d'Apple lors de leur configuration initiale ou de leur réinitialisation, ce qui signifie qu'une connexion internet est **nécessaire** pour utiliser un appareil iOS.

### App Store obligatoire

La seule source d'applications sur iOS est l'App Store d'Apple, dont l'accès nécessite un identifiant Apple. Cela signifie qu'Apple dispose d'un enregistrement de chaque application que vous installez sur votre appareil et qu'elle peut probablement relier ces informations à votre identité réelle si vous fournissez à l'App Store une méthode de paiement.

### Télémétrie invasive

Apple a toujours eu des problèmes pour dissocier correctement ses données télémétriques des identifiants Apple sur iOS. [En 2019](https://theguardian.com/technology/2019/jul/26/apple-contractors-regularly-hear-confidential-details-on-siri-recordings), il a été constaté qu'Apple transmettait des enregistrements Siri - dont certains contenaient des informations hautement confidentielles - à ses serveurs pour qu'ils soient examinés manuellement par des sous-traitants. Bien qu'Apple ait temporairement mis un terme à ce programme après que cette pratique ait fait l'objet d'une [large couverture médiatique](https://theverge.com/2019/8/23/20830120/apple-contractors-siri-recordings-listening-1000-a-day-globetech-microsoft-cortana), l'entreprise a mis en place, quelques mois plus tard, une option permettant de [**ne pas** télécharger les conversations avec Siri dans](https://theguardian.com/technology/2019/oct/30/apple-lets-users-opt-out-of-having-siri-conversations-recorded) la mise à jour suivante d'iOS. De plus, en 2021, [Apple a retravaillé Siri](https://theguardian.com/technology/2021/jun/07/apple-overhauls-siri-to-address-privacy-concerns-and-improve-performance) pour traiter les enregistrements vocaux localement plutôt que de les envoyer à leurs serveurs.

Plus récemment, il a été constaté qu'Apple [transmettait des données analytiques même lorsque le partage des données analytiques était désactivé](https://gizmodo.com/apple-iphone-analytics-tracking-even-when-off-app-store-1849757558) sur iOS, et ces données [semblent](https://twitter.com/mysk_co/status/1594515229915979776) être facilement reliées à des identifiants de compte iCloud uniques, bien qu'elles soient censées être anonymes.

### Trafic en dehors des connexions VPN actives

La [politique de confidentialité d'Apple concernant les VPN](https://apple.com/legal/privacy/data/en/vpns) stipule ce qui suit :

> Même lorsqu'un VPN est actif, une partie du trafic nécessaire aux services essentiels du système s'effectue en dehors du VPN afin que votre appareil puisse fonctionner correctement.

## Configuration recommandée

**Remarque :** ce guide suppose que vous utilisez la dernière version d'iOS.

### iCloud

La majorité des préoccupations relatives à la protection de la vie privée et à la sécurité des produits Apple sont liées à leurs services cloud, et non à leurs matériels ou à leurs logiciels. Lorsque vous utilisez des services Apple comme iCloud, la plupart de vos informations sont stockées sur leurs serveurs et sécurisées par des clés auxquelles Apple a accès par défaut. Vous pouvez consulter [la documentation d'Apple](https://support.apple.com/HT202303) pour savoir quels services sont chiffrés de bout en bout. Tout ce qui est mentionné comme étant "en transit" ou "sur serveur" signifie qu'il est possible pour Apple d'accéder à ces données sans votre permission. Ce niveau d'accès a parfois été utilisé de manière abusive par les forces de l'ordre pour contourner le fait que vos données sont par ailleurs chiffrées de manière sécurisée sur votre appareil, et bien sûr Apple est vulnérable aux fuites de données comme toute autre entreprise.

Par conséquent, si vous utilisez iCloud, vous devriez [activer la **protection avancée des données**](https://support.apple.com/HT212520). Cela permet de chiffrer la quasi-totalité de vos données iCloud à l'aide de clés stockées sur vos appareils (chiffrement de bout en bout), plutôt que sur les serveurs d'Apple, de sorte que vos données iCloud sont sécurisées en cas de fuite de données, et qu'elles sont par ailleurs cachées à Apple.

Le chiffrement utilisé par la protection avancée des données, bien que puissant, [n'est pas *aussi* robuste](https://discuss.privacyguides.net/t/apple-advances-user-security-with-powerful-new-data-protections/10778/4) que le chiffrement offert par d'autres [services cloud](../cloud.md), en particulier lorsqu'il s'agit d'iCloud Drive. Bien que nous vous recommandons vivement d'utiliser la protection avancée des données si vous utilisez iCloud, nous vous suggérons également d'envisager de trouver une alternative à iCloud auprès d'un [fournisseur de services plus axé sur la vie privée](../tools.md), bien qu'il soit peu probable que la plupart des gens soient affectés par ces bizarreries de chiffrement.

Vous pouvez également protéger vos données en limitant ce que vous synchronisez sur iCloud. En haut de l'application **Réglages**, vous verrez votre nom et votre photo de profil si vous êtes connecté à iCloud. Sélectionnez-les, puis **iCloud**, et désactivez les services que vous ne souhaitez pas synchroniser avec iCloud. Il se peut que des applications tierces soient répertoriées sous **Voir Tout** si elles se synchronisent avec iCloud, ce que vous pouvez désactiver ici.

#### iCloud+

Un abonnement payant à **iCloud+** (avec n'importe quelle offre de stockage iCloud) est assorti de fonctionnalités de protection de la vie privée. Bien qu'elles puissent fournir un service adéquat aux clients actuels d'iCloud, nous ne recommanderions pas l'achat d'une offre iCloud+ plutôt qu'un [VPN](../vpn.md) et qu'un [service d'alias d'e-mail indépendant](../email-aliasing.md), rien que pour ces fonctionnalités.

[**Private Relay**](https://apple.com/legal/privacy/data/en/icloud-relay) est un service proxy qui relaie l'ensemble de votre trafic Safari, vos requêtes DNS et le trafic non chiffré sur votre appareil via deux serveurs : l'un appartenant à Apple et l'autre à un fournisseur tiers (notamment Akamai, Cloudflare et Fastly). En théorie, cela devrait empêcher tout fournisseur de la chaîne, y compris Apple, d'avoir une complète visibilité sur les sites web que vous visitez lorsque vous êtes connecté. Contrairement à un VPN, Private Relay ne protège pas le trafic déjà chiffré.

**Masquer mon adresse e-mail** est le service d'alias de d'e-mail d'Apple. Vous pouvez créer un alias d'e-mail gratuitement lorsque vous faite *Se connecter avec Apple* sur un site web ou une application, ou générer un nombre illimité d'alias à la demande avec une offre iCloud+ payante. Masque mon adresse e-mail a l'avantage d'utiliser le domaine `@icloud.com` pour ses alias, ce qui peut être moins susceptible d'être bloqué par rapport à d'autres services d'alias d'email, mais n'offre pas de fonctionnalité offerte par des services indépendants tels que le chiffrement PGP automatique ou la prise en charge de plusieurs boîtes aux lettres.

#### Médias & achats

En haut de l'application **Réglages**, vous verrez votre nom et votre photo de profil si vous êtes connecté à un compte Apple. Sélectionnez-les, puis sélectionnez **Médias & Achats**  **Voir Compte**.

- [ ] Désactivez **Recommandations Personnalisées**

#### Localiser

**Localiser** est un service qui vous permet de suivre vos appareils Apple et de partager votre localisation avec vos amis et votre famille. Il vous permet également d'effacer votre appareil à distance en cas de vol, empêchant ainsi un voleur d'accéder à vos données. Vos [données de localisation Localiser sont E2EE](https://apple.com/legal/privacy/data/en/find-my) lorsque :

- Votre position est partagée avec un membre de votre famille ou un ami, et vous utilisez tous deux iOS 17 ou une version ultérieure.
- Votre appareil est hors ligne et est localisé par le réseau de Localiser.

Vos données de localisation ne sont pas E2EE lorsque votre appareil est en ligne et que vous utilisez Localiser mon iPhone à distance pour localiser votre appareil. C'est à vous de décider si ces compromis valent les avantages antivol du verrouillage d'activation.

En haut de l'application **Réglages**, vous verrez votre nom et votre photo de profil si vous êtes connecté à un compte Apple. Sélectionnez-les, puis selectionnez **Localiser**. Vous pouvez ici choisir d'activer ou de désactiver les fonctions de Localiser ma position.

### Paramètres

De nombreux autres paramètres liés à la protection de la vie privée peuvent être trouvés dans l'application **Réglages**.

#### Mode avion

Activation du **mode avion** empêche votre téléphone de contacter les antennes cellulaires. Vous pourrez toujours vous connecter au Wi-Fi et au Bluetooth, donc chaque fois que vous êtes connecté au Wi-Fi, vous pouvez activer ce paramètre.

#### Wi-Fi

Vous pouvez activer la [randomisation de l'adresse matérielle](https://support.apple.com/en-us/102509#triswitch) pour vous protéger contre le suivi sur les réseaux Wi-Fi et sur le même réseau au fil du temps. Sur le réseau auquel vous êtes actuellement connecté, appuyez sur le bouton :material-information: :

- [x] Définir l'**adresse Wi-Fi privée** comme **Fixe** ou **Rotation**

Vous avez également la possibilité de **Limiter le suivi de l'adresse IP**. Cette fonction est similaire au relais privé iCloud, mais n'affecte que les connexions aux "traqueurs connus". Étant donné qu'il n'affecte que les connexions à des serveurs potentiellement malveillants, vous pouvez probablement laisser ce paramètre activé, mais si vous ne voulez *pas* que le trafic soit acheminé via les serveurs d'Apple, vous devriez le désactiver.

#### Bluetooth

**Bluetooth** doit être désactivé lorsque vous ne l'utilisez pas, car il augmente votre surface d'attaque. La désactivation du Bluetooth (ou du Wi-Fi) via le Centre de contrôle n'est que temporaire : vous devez le désactiver dans Paramètres pour que la désactivation soit effective.

- [ ] Désactivez **Bluetooth**

Notez que le Bluetooth est automatiquement activé après chaque mise à jour du système.

#### Général

Le nom d'appareil de votre iPhone contient par défaut votre prénom, qui sera visible par tous les utilisateurs des réseaux auxquels vous vous connectez. Vous devriez le remplacer par quelque chose de plus générique, comme "iPhone". Sélectionnez **À propos** → **Nom** et entrez le nom que vous avez choisi.

It is important to install software updates frequently to get the latest security fixes. You can enable automatic updates to keep your phone up-to-date without needing to constantly check for updates. Sélectionnez **Mise à jour logicielle**  **MAJ automatiques** :

- [x] Turn on **Automatically Install**

**AirDrop** est couramment utilisé pour partager facilement des fichiers, mais il présente un risque important pour la vie privée. Le protocole AirDrop diffuse constamment vos informations personnelles à votre entourage, avec des protections de sécurité [très faibles](https://usenix.org/system/files/sec21-heinrich.pdf). Votre identité peut facilement être découverte par des attaquants, même avec des ressources limitées, et le gouvernement chinois a [ouvertement reconnu](https://arstechnica.com/security/2024/01/hackers-can-id-unique-apple-airdrop-users-chinese-authorities-claim-to-do-just-that) utiliser de telles techniques pour identifier les utilisateurs d'AirDrop en public depuis 2022.

- [x] Sélectionnez **AirDrop** → **Réception désactivée**

**AirPlay** vous permet de diffuser de manière transparente du contenu de votre iPhone vers un téléviseur, mais vous n'en avez pas toujours besoin. Sélectionnez **AirPlay & Continuité** → **AirPlay Automatiquement** :

- [x] Sélectionnez **Jamais** ou **Demander**

**Actualisation des applications en arrière-plan** permet à vos applications d'actualiser leur contenu lorsque vous ne les utilisez pas. Cela peut les amener à établir des connexions non souhaitées. Désactiver cette option peut permettre d'économiser la durée de vie de la batterie, mais peut affecter la capacité d'une application à recevoir des informations à jour, en particulier les applications météo et de messagerie.

Sélectionnez **Actualisation des applications en arrière-plan** et désactivez toutes les applications que vous ne souhaitez pas voir actualisées en arrière-plan. Si vous ne souhaitez pas qu'une application soit actualisée en arrière-plan, vous pouvez sélectionner à nouveau **Actualisation des applications en arrière-plan** et la **désactiver**.

#### Apple Intelligence & Siri

This is available if your device supports **[Apple Intelligence](https://support.apple.com/guide/iphone/apple-intelligence-and-privacy-iphe3f499e0e/ios)**. Apple Intelligence uses a combination of on-device processing and their **[Private Cloud Compute](https://security.apple.com/blog/private-cloud-compute)** for things that take more processing power than your device can provide.

To see a report of all the requests made to Apple's servers, you can navigate to **Privacy & Security** → **Apple Intelligence Report** and press **Export Activity** to see activity from the either the last 15 minutes or 7 days, depending on what you set it for. Cette fonctionnalité, assez similaire au **Rapport de confidentialité des apps** qui permet de connaitre les permissions récemment utilisées par les applications sur votre téléphone, vous permet de consulter ce qui est envoyé aux serveurs d'Apple lorsque vous utilisez Apple Intelligence.

Apple Intelligence can integrate with [ChatGPT](https://support.apple.com/guide/iphone/use-chatgpt-with-apple-intelligence-iph00fd3c8c2/ios). If you want ChatGPT integration, you can navigate to **ChatGPT** and press **Set Up**. If you want to disable it, go to the same place:

- [ ] Désactivez **Utiliser ChatGPT**

Vous pouvez également paramètrer une notification de confirmation à chaque fois que vous laissez allumée l'intégration ChatGPT :

- [x] Activez **Demander la Confirmation**

Si vous ne voulez pas que quelqu'un puisse contrôler votre téléphone avec Siri lorsqu'il est verrouillé, vous pouvez le désactiver ici.

- [ ] Désactivez **Autoriser Siri lorsque le téléphone est vérouillé**

#### Face ID/Touch ID et code

Définir un mot de passe fort pour votre téléphone est la mesure la plus importante que vous puissiez prendre pour assurer la sécurité physique de votre appareil. Vous devrez faire des compromis entre la sécurité et la commodité : un mot de passe plus long sera fastidieux à saisir à chaque fois, mais un mot de passe ou un code PIN plus court sera plus facile à deviner. Configurer Face ID ou Touch ID avec un mot de passe fort peut être un bon compromis entre convivialité et sécurité.

Sélectionnez **Activer le code d'accès** ou **Modifier le code d'accès**  **Options du code d'accès**  **Code alphanumérique personnalisé**. Veillez à créer un [mot de passe sûr](../basics/passwords-overview.md).

Si vous souhaitez utiliser Face ID ou Touch ID, vous pouvez le configurer maintenant. Votre téléphone utilisera le mot de passe que vous avez défini précédemment comme solution de secours en cas d'échec de la vérification biométrique. Les méthodes de déverrouillage biométrique existent principalement pour la commodité, même si elles empêchent les caméras de surveillance ou les personnes de vous regarder saisir votre code d'accès par-dessus votre épaule.

Si vous utilisez les déverouillages biométriques, vous devez savoir comment les désactiver rapidement en cas d'urgence. Holding down the [side button](https://support.apple.com/en-us/105103) and *either* volume button until you see the Slide to Power Off slider will disable biometrics, requiring your passcode to unlock. Your passcode will be required after your device restarts.

You can similarly disable biometrics by pressing the side button five times, or for devices with Touch ID, you can hold down the side button and nothing else. Assurez-vous faire un essai préalable afin de savoir quelle méthode fonctionne pour votre appareil.

**Protection en cas de vol de l’appareil** est une nouvelle fonctionnalité d'iOS  qui ajoute une sécurité supplémentaire destinée à protéger vos données personnelles si votre appareil est volé lorsqu'il est déverrouillé. If you enable both biometric authentication and the [Find My](#find-my) iPhone feature, we recommend enabling this protection:

- [x] Turn on **Stolen Device Protection**

Après avoir activé la protection en cas de vol de l’appareil, [certaines actions](https://support.apple.com/HT212510) nécessiteront une authentification biométrique sans possibilité de recourir au mot de passe (dans le cas où un passant obtient votre code PIN), comme l'utilisation du remplissage des mots de passe, l'accès aux informations de paiement et la désactivation du mode Perdu. Cela ajoute également un délai de sécurité pour certaines actions effectuées en dehors de votre domicile ou d'un autre "lieu familier", comme la nécessité d'un délai d'une heure pour réinitialiser votre mot de passe Apple ID ou vous déconnecter de votre Apple ID. Ce délai a pour but de vous donner le temps d'activer le mode Perdu et de sécuriser votre compte avant qu'un voleur ne puisse réinitialiser votre appareil.

**Allow Access When Locked** presents options for what you can allow when your phone is locked. Pick and choose which feature you want to disable to prevent unauthorized access if someone gets their hands on your phone. Plus vous désactivez d'options, moins quelqu'un qui n'a pas votre mot de passe peut faire de choses, mais moins c'est pratique pour vous.

Les iPhones sont déjà résistants aux attaques par force brute en vous faisant attendre de longues périodes de temps après plusieurs tentatives infructueuses ; cependant, il y a toujours eu des exploits pour contourner cette protection. Pour plus de sécurité, vous pouvez configurer votre téléphone pour qu'il s'efface de lui-même après 10 tentatives infructueuses de saisie du code d'accès.

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

Si ce paramètre est activé, quelqu'un peut intentionnellement effacer votre téléphone en entrant plusieurs fois le mauvais mot de passe. Assurez-vous d'avoir des sauvegardes appropriées et n'activez ce paramètre que si vous vous sentez à l'aise avec ça.

</div>

- [x] Activez **Effacer les données**

#### Confidentialité & sécurité

Les **services de localisation** vous permettent d'utiliser des fonctions telles que Localiser et Plan. Si vous n'avez pas besoin de ces fonctionnalités, vous pouvez désactiver les services de localisation. Vous pouvez également passer en revue et choisir les applications qui peuvent utiliser votre position ici. Sélectionnez **Services de localisation** :

- [ ] Désactivez **Services de localisation**

Une flèche violette apparaîtra à côté d'une application dans ces paramètres qui a récemment utilisé votre position alors qu'une flèche grise indique que votre emplacement a été accédé au cours des dernières 24 heures. Si vous décidez de laisser les services de localisation activés, Apple les utilisera par défaut pour les services système. Ici, vous pouvez également passer en revue et choisir les applications qui peuvent utiliser votre position. Toutefois, si vous ne souhaitez pas transmettre à Apple des données d'analyse relatives à la localisation, qui sont utilisées pour améliorer Apple Maps, vous pouvez également désactiver cette option ici. Sélectionnez **Services système**:

- [ ] Désactiver **iPhone Analytics**
- [ ] Désactiver **Router & Trafic**
- [ ] Désactiver **Améliorer Apple Maps**

Vous pouvez décider ici d'autoriser les applications à demander à vous **suivre**. La désactivation de cette fonction empêche toutes les applications de vous suivre à l'aide de l'identifiant publicitaire de votre téléphone. Sélectionnez **Suivi** :

- [ ] Désactivez **Autoriser les demandes de suivi des apps**

Cette option est désactivée par défaut et ne peut être modifiée pour les utilisateurs de moins de 18 ans.

Vous devriez désactiver **Données de capteur et d’utilisation à des fins de recherche** si vous ne souhaitez pas participer à des études. Sélectionnez **Données de capteur et d’utilisation à des fins de recherche** :

- [ ] Désactivez **Collecte de données de capteur et d'utilisation**

**[Safety Check](https://support.apple.com/guide/personal-safety/safety-check-iphone-ios-16-ips2aad835e1/1.0/web/1.0)** allows you to quickly view and revoke certain people and apps that might have permission to access your data. Here, you can perform an **Emergency Reset**, immediately resetting permissions for all people and apps which might have access to device resources. You can also **Manage Sharing & Access**, which allows you to review and customize who and what has access to your device and account resources. If you're in an abusive situation, read Apple's [Personal Safety User Guide](https://support.apple.com/guide/personal-safety/welcome/web) for guidance on what you should do.

You should disable analytics if you don't wish to send usage data to Apple. Select **Analytics & Improvements** and unselect the type(s) of analytics that you don't want to send to Apple.

Désactivez **Publicités personnalisées** si vous ne voulez pas de publicités ciblées. Sélectionnez **Apple Advertising**:

- [ ] Décochez **Publicités personnalisées**

**Rapport de confidentialité des apps** est un outil intégré qui vous permet de voir quelles sont les autorisations utilisées par vos applications. Sélectionnez **Rapport de confidentialité des apps** :

- [x] Sélectionnez **Activer le rapport de confidentialité des apps**

Set wired accessories to ask for permission when you connect them. Select **Wired Accessories**:

- [x] Select **Always Ask** or **Ask for New Accessories**

**[Lockdown Mode](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode)** is a security setting you can enable to make your phone more resistant to attacks. Sachez que certaines applications et fonctionnalités [ne fonctionneront pas](https://support.apple.com/HT212650) comme elles le font normalement.

- [x] Sélectionnez **Activer le mode Isolement**

## Conseils supplémentaires

### Appels E2EE

Les appels téléphoniques normaux effectués avec l'application Téléphone par l'intermédiaire de votre opérateur ne sont pas E2EE. Les appels FaceTime Video et FaceTime Audio sont tous deux E2EE. Vous pouvez également utiliser [une autre application](../real-time-communication.md) comme Signal pour les appels E2EE.

### iMessage chiffré

La [couleur de la bulle de message](https://support.apple.com/en-us/104972) dans l'application Messages indique si vos messages sont E2EE ou non. Une bulle bleue indique que vous utilisez iMessage avec E2EE, tandis qu'une bulle verte indique qu'ils utilisent les protocoles SMS et MMS ou RCS. RCS sur iOS n'est **pas** E2EE. Actuellement, le seul moyen d'utiliser l'E2EE dans Messages est que les deux parties utilisent iMessage sur des appareils Apple.

Si vous ou votre partenaire de messagerie avez activé la sauvegarde iCloud sans la protection avancée des données, la clé de chiffrement sera stockée sur les serveurs d'Apple, ce qui signifie qu'ils peuvent accéder à vos messages.

By default, you trust Apple's identity servers that you're messaging the right person. To defend yourself from a potentially malicious server, you can enable **[Contact Key Verification](https://support.apple.com/en-us/118246)**. At the top of the **Settings** app where your name is, select it, then go to **Contact Key Verification**.

- [x] Turn on **Verification in iMessage**

Both you and your contacts need to enable Contact Key Verification and follow Apple's [instructions](https://support.apple.com/en-us/118246#verify) for the security assurances mentioned above to take effect.

### Autorisations d'accès à la galerie

Lorsqu'une application vous demande d'accéder à la galerie de votre appareil, iOS vous propose des options pour limiter cet accès.

Plutôt que d'autoriser une application à accéder à toutes les photos de votre appareil, vous pouvez lui permettre de n'accéder qu'aux photos de votre choix en appuyant sur l'option "Sélectionner les photos..." dans la boîte de dialogue d'autorisation. Vous pouvez modifier les autorisations d'accès aux photos à tout moment en accédant à **Paramètres** → **Confidentialité & Sécurité** → **Photos**.

![Autorisations d'accès à la galerie](../assets/img/ios/photo-permissions-light.png#only-light) ![Autorisations d'accès à la galerie](../assets/img/ios/photo-permissions-dark.png#only-dark)

**Ajouter des photos uniquement** est une autorisation qui donne à une application la possibilité de télécharger uniquement des photos dans la galerie. Toutes les applications qui demandent l'accès à la galerie ne proposent pas cette option.

![Accès privé](../assets/img/ios/private-access-light.png#only-light) ![Accès privé](../assets/img/ios/private-access-dark.png#only-dark)

Certaines applications prennent également en charge l'**accès privé**, qui fonctionne de la même manière que l'autorisation d'**accès limité**. Cependant, les photos partagées à des applications utilisant un accès privé incluent par défaut leur localisation. Nous vous recommandons de décocher ce paramètre si vous ne supprimez pas au préalable [les métadonnées des photos](../data-redaction.md).

### Autorisations d'accès aux contacts

De façon similaire, plutôt que d'autoriser une application à accéder à tous les contacts enregistrés sur votre appareil, vous pouvez lui permettre de n'accéder qu'aux contacts de votre choix. Vous pouvez modifier les autorisations d'accès aux contacts à tout moment en accédant à **Paramètres** → **Confidentialité & Sécurité** → **Contacts**.

![Autorisations d'accès aux contacts](../assets/img/ios/contact-permissions-light.png#only-light) ![Autorisations d'accès aux contacts](../assets/img/ios/contact-permissions-dark.png#only-dark)

### Exiger des données biométriques et masquer des applications

iOS offre la possibilité de verrouiller la plupart des applications derrière Touch ID/Face ID ou votre code d'accès, qui peut être utile pour protéger le contenu sensible dans les applications qui ne fournissent pas l'option elle-même. Vous pouvez verrouiller une application en appuyant longuement dessus et en sélectionnant **Exiger Face ID/Touch ID.**. Toute application ainsi verrouillée nécessite une authentification biométrique à chaque fois qu'elle est ouverte ou que l'on accède à son contenu depuis d'autres applications. De plus, les aperçus de notification des applications verrouillées ne s'afficheront pas.

Outre le verrouillage biométrique des applications, vous pouvez également masquer des applications afin qu'elles n'apparaissent pas sur l'écran d'accueil, dans la bibliothèque d'applications, dans la liste d'applications des **Paramètres**, etc. Si masque des applications peut s'avérer utile lorsque vous devez remettre votre téléphone déverrouillé à quelqu'un d'autre, la dissimulation offerte par cette fonction n'est pas absolue, car une application masquée reste visible à certains endroits, comme dans la liste d'utilisation de la batterie. En outre, l'une des contreparties notables de cette fonctionnalité est que vous ne recevrez aucune de ses notifications.

Vous pouvez masquer une application en appuyant longuement dessus et en sélectionnant **Exiger Face ID/Touch ID** → **Masquer et Exiger Face ID/Touch ID.** Notez que les applications Apple préinstallées, ainsi que le navigateur web et l'application de messagerie par défaut, ne peuvent pas être masquées. Les applications masquées se trouvent dans un dossier **Applications masqué** au bas de la bibliothèque d'applications, qui peut être déverrouillé à l'aide des données biométriques. Ce dossier apparaît dans la bibliothèque d'applications, que vous ayez masqué des applications ou non, ce qui vous permet, dans une certaine mesure, de nier l'existence de certaines applications.

### Guided Access

Sometimes you might want to hand your phone to someone to make a call or do a specific task, but you don't want them to have full access to your phone. In these cases, you can quickly enable **[Guided Access](https://support.apple.com/guide/iphone/lock-iphone-to-one-app-iph7fad0d10/ios)** to lock the phone to one specific app until you authenticate.

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

Guided Access isn't foolproof, as it's possible you could leak data unintentionally or the feature could be bypassed. You should only use Guided Access for situations where you casually hand your phone to someone to use. You should not use it as a tool to protect against advanced adversaries.

</div>

### Effacer des éléments dans une image

Si vous devez masquer des informations dans une photo, vous pouvez utiliser les outils intégrés d'Apple pour le faire.

You can use the [Clean Up](https://support.apple.com/en-us/121429) feature on supported devices to pixelate faces or remove objects from images.

- Ouvrez l'application **Photos** et appuyez sur la photo que vous avez sélectionnée
- Tap the :material-tune:
- Appuyez sur **Nettoyer**
- Tracez un cercle autour de ce que vous souhaitez effacer. Les visages seront pixélisés, et il tentera de supprimer quoi que ce soit d'autre.

Notre mise en garde [contre le floutage du texte](../data-redaction.md) s'applique également ici. Nous vous recommandons donc plutôt d'ajouter une forme noire avec une opacité de 100 %. En plus d'effacer du texte, vous pouvez également masquer un visage ou un objet à l'aide de l'application **Photos.**

<div class="annotate" markdown>

- Tap the image you have selected for redaction
- Tap the :material-tune: → :material-dots-horizontal: (1) → Markup → :material-plus:
- Select **Add Shape** and choose the square or circle
- On the toolbar, tap the circle and choose black as the color for filling in the shape. Vous pouvez également déplacer la forme et augmenter sa taille comme vous le souhaitez.

</div>

1. This may not appear on certain iPhone models.

N'utilisez **pas** le surligneur pour obscurcir des informations, car son opacité n'est pas tout à fait de 100 %.

### Éviter le jailbreaking

Le jailbreaking d'un iPhone compromet sa sécurité et vous rend vulnérable. L'exécution de logiciels tiers non fiables peut entraîner l'infection de votre appareil par des logiciels malveillants.

### Bêtas iOS

Apple met toujours des versions bêta d'iOS à la disposition de ceux qui souhaitent aider à trouver et à signaler des bogues. Nous vous déconseillons d'installer des logiciels bêta sur votre téléphone. Les versions bêta sont potentiellement instables et peuvent présenter des failles de sécurité non découvertes.

## Points forts en matière de sécurité

### Avant le premier déverrouillage

Si votre modèle de menace comprend des

:material-target-account: Outils d'investigation et que vous souhaitez minimiser les risques d'utilisation de failles de sécurité pour accéder à votre téléphone, vous devriez redémarrer votre appareil fréquemment. L'état *après* un redémarrage mais *avant* le déverrouillage de votre appareil est appelé "Before First Unlock" (BFU), et lorsque votre appareil est dans cet état, il est [nettement plus difficile](https://belkasoft.com/checkm8_glossary) pour les outils de criminalistique d'exploiter des vulnérabilités pour accéder à vos données. Cet état BFU vous permet de recevoir des notifications pour les appels, les textes et les alarmes, mais la plupart des données de votre appareil sont toujours chiffrées et inaccessibles. Cela peut s'avérer peu pratique, il convient donc de se demander si ces compromis sont judicieux dans votre situation.</p> 

iPhones [automatically reboot](https://support.apple.com/guide/security/protecting-user-data-in-the-face-of-attack-secf5549a4f5/1/web/1#:~:text=On%20an%20iPhone%20or%20iPad%20with%20iOS%2018%20and%20iPadOS%2018%20or%20later%2C%20a%20new%20security%20protection%20will%20restart%20devices%20if%20they%20remain%20locked%20for%20a%20prolonged%20period%20of%20time.) if they're not unlocked after a period of time.



### MTE

The iPhone 17 line and later offer a security enhancement called [Memory Tagging Extension](https://developer.arm.com/documentation/108035/0100/Introduction-to-the-Memory-Tagging-Extension) (MTE), which makes it significantly harder for an attacker to exploit memory corruption vulnerabilities. This always-on protection depends on hardware support, so it's not available for older devices.

For more details on Apple's implementation of MTE, read the [blog post](https://security.apple.com/blog/memory-integrity-enforcement) published by Apple Security Research. We also cover Apple's implementation of MTE and how it compares to Android's implementation in the Google Pixel 8 series and later in our [own article](https://www.privacyguides.org/posts/2025/09/20/memory-integrity-enforcement-changes-the-game-on-ios).
