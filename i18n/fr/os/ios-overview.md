---
title: Introduction à iOS
icon: simple/apple
description: iOS est un système d'exploitation mobile développé par Apple pour l'iPhone.
---

**iOS** et **iPadOS** sont des systèmes d'exploitation mobiles propriétaires développés par Apple pour ses produits iPhone et iPad, respectivement. Si vous possédez un appareil mobile Apple, vous pouvez améliorer votre vie privée en désactivant certaines fonctions de télémétrie intégrées et en renforçant certains paramètres de sécurité et de protection de la vie privée intégrés au système.

## Remarques concernant la vie privée

iOS devices are frequently praised by security experts for their robust data protection and adherence to modern best practices. Cependant, le caractère restrictif de l'écosystème d'Apple - en particulier avec ses appareils mobiles - continue d'entraver la protection de la vie privée de plusieurs manières.

Nous considérons généralement qu'iOS offre des protections de la vie privée et de la sécurité supérieures à la moyenne pour la plupart des gens, par rapport aux appareils Android d'origine, quel que soit le fabricant. However, you can achieve even higher standards of privacy with a [custom Android operating system](../android/distributions.md) like GrapheneOS, if you want or need to be completely independent of Apple or Google's cloud services.

### Verrouillage d'activation

Tous les appareils iOS doivent être vérifiés sur les serveurs de verrouillage d'activation d'Apple lors de leur configuration initiale ou de leur réinitialisation, ce qui signifie qu'une connexion internet est **nécessaire** pour utiliser un appareil iOS.

### App Store obligatoire

The only source for apps on iOS is Apple's App Store, which requires an Apple Account to access. Cela signifie qu'Apple dispose d'un enregistrement de chaque application que vous installez sur votre appareil et qu'elle peut probablement relier ces informations à votre identité réelle si vous fournissez à l'App Store une méthode de paiement.

### Télémétrie invasive

Apple has historically had problems with properly disassociating their telemetry from Apple Accounts on iOS. In [2019](https://theguardian.com/technology/2019/jul/26/apple-contractors-regularly-hear-confidential-details-on-siri-recordings), Apple was found to transmit Siri recordings—some containing highly confidential information—to their servers for manual review by third-party contractors. Though Apple temporarily stopped that program after that practice was [widely reported on](https://theverge.com/2019/8/23/20830120/apple-contractors-siri-recordings-listening-1000-a-day-globetech-microsoft-cortana), the company rolled out a switch to [**opt out** of uploading conversations with Siri](https://theguardian.com/technology/2019/oct/30/apple-lets-users-opt-out-of-having-siri-conversations-recorded) a few months later in the succeeding iOS update. Moreover, in 2021, [Apple reworked Siri](https://theguardian.com/technology/2021/jun/07/apple-overhauls-siri-to-address-privacy-concerns-and-improve-performance) so that it processes voice recordings locally rather than sending it to their servers.

More recently, Apple has been found to transmit analytics [even when analytics sharing is disabled](https://gizmodo.com/apple-iphone-analytics-tracking-even-when-off-app-store-1849757558) on iOS, and this data [appears](https://twitter.com/mysk_co/status/1594515229915979776) to be easily linked to unique iCloud account identifiers despite supposedly being decoupled from Apple Accounts.

### Traffic Outside Active VPN Connections

Apple's [privacy policy regarding VPNs](https://apple.com/legal/privacy/data/en/vpns) states:

> Even when a VPN is active, some traffic that is necessary for essential system services will take place outside the VPN so that your device can function properly.

## Configuration recommandée

**Note:** This guide assumes that you're running the latest version of iOS.

### iCloud

La majorité des préoccupations relatives à la protection de la vie privée et à la sécurité des produits Apple sont liées à leurs services cloud, et non à leurs matériels ou à leurs logiciels. Lorsque vous utilisez des services Apple comme iCloud, la plupart de vos informations sont stockées sur leurs serveurs et sécurisées par des clés auxquelles Apple a accès par défaut. Vous pouvez consulter [la documentation d'Apple](https://support.apple.com/HT202303) pour savoir quels services sont chiffrés de bout en bout. Tout ce qui est mentionné comme étant "en transit" ou "sur serveur" signifie qu'il est possible pour Apple d'accéder à ces données sans votre permission. Ce niveau d'accès a parfois été utilisé de manière abusive par les forces de l'ordre pour contourner le fait que vos données sont par ailleurs chiffrées de manière sécurisée sur votre appareil, et bien sûr Apple est vulnérable aux fuites de données comme toute autre entreprise.

Par conséquent, si vous utilisez iCloud, vous devriez [activer la **protection avancée des données**](https://support.apple.com/HT212520). Cela permet de chiffrer la quasi-totalité de vos données iCloud à l'aide de clés stockées sur vos appareils (chiffrement de bout en bout), plutôt que sur les serveurs d'Apple, de sorte que vos données iCloud sont sécurisées en cas de fuite de données, et qu'elles sont par ailleurs cachées à Apple.

Le chiffrement utilisé par la protection avancée des données, bien que puissant, [n'est pas *aussi* robuste](https://discuss.privacyguides.net/t/apple-advances-user-security-with-powerful-new-data-protections/10778/4) que le chiffrement offert par d'autres [services cloud](../cloud.md), en particulier lorsqu'il s'agit d'iCloud Drive. Bien que nous vous recommandons vivement d'utiliser la protection avancée des données si vous utilisez iCloud, nous vous suggérons également d'envisager de trouver une alternative à iCloud auprès d'un [fournisseur de services plus axé sur la vie privée](../tools.md), bien qu'il soit peu probable que la plupart des gens soient affectés par ces bizarreries de chiffrement.

Vous pouvez également protéger vos données en limitant ce que vous synchronisez sur iCloud. En haut de l'application **Réglages**, vous verrez votre nom et votre photo de profil si vous êtes connecté à iCloud. Sélectionnez-les, puis **iCloud**, et désactivez les services que vous ne souhaitez pas synchroniser avec iCloud. Il se peut que des applications tierces soient répertoriées sous **Voir Tout** si elles se synchronisent avec iCloud, ce que vous pouvez désactiver ici.

#### iCloud+

Un abonnement payant à **iCloud+** (avec n'importe quelle offre de stockage iCloud) est assorti de fonctionnalités de protection de la vie privée. Bien qu'elles puissent fournir un service adéquat aux clients actuels d'iCloud, nous ne recommanderions pas l'achat d'une offre iCloud+ plutôt qu'un [VPN](../vpn.md) et qu'un [service d'alias d'e-mail indépendant](../email-aliasing.md), rien que pour ces fonctionnalités.

[**Private Relay**](https://apple.com/legal/privacy/data/en/icloud-relay) is a proxy service which relays all of your Safari traffic, your DNS queries, and unencrypted traffic on your device through two servers: one owned by Apple and one owned by a third-party provider (including Akamai, Cloudflare, and Fastly). En théorie, cela devrait empêcher tout fournisseur de la chaîne, y compris Apple, d'avoir une complète visibilité sur les sites web que vous visitez lorsque vous êtes connecté. Unlike a VPN, Private Relay does not protect traffic that's already encrypted.

**Masquer mon adresse e-mail** est le service d'alias de d'e-mail d'Apple. Vous pouvez créer un alias d'e-mail gratuitement lorsque vous faite *Se connecter avec Apple* sur un site web ou une application, ou générer un nombre illimité d'alias à la demande avec une offre iCloud+ payante. Masque mon adresse e-mail a l'avantage d'utiliser le domaine `@icloud.com` pour ses alias, ce qui peut être moins susceptible d'être bloqué par rapport à d'autres services d'alias d'email, mais n'offre pas de fonctionnalité offerte par des services indépendants tels que le chiffrement PGP automatique ou la prise en charge de plusieurs boîtes aux lettres.

#### Médias & achats

At the top of the **Settings** app, you'll see your name and profile picture if you are signed in to an Apple Account. Select that, then select **Media & Purchases** → **View Account**.

- [ ] Désactivez **Recommandations Personnalisées**

#### Localiser

**Localiser** est un service qui vous permet de suivre vos appareils Apple et de partager votre localisation avec vos amis et votre famille. Il vous permet également d'effacer votre appareil à distance en cas de vol, empêchant ainsi un voleur d'accéder à vos données. Vos [données de localisation Localiser sont E2EE](https://apple.com/legal/privacy/data/en/find-my) lorsque :

- Your location is shared with a family member or friend, and you both use iOS 17 or greater.
- Votre appareil est hors ligne et est localisé par le réseau de Localiser.

Vos données de localisation ne sont pas E2EE lorsque votre appareil est en ligne et que vous utilisez Localiser mon iPhone à distance pour localiser votre appareil. C'est à vous de décider si ces compromis valent les avantages antivol du verrouillage d'activation.

At the top of the **Settings** app, you'll see your name and profile picture if you are signed in to an Apple Account. Sélectionnez-les, puis selectionnez **Localiser**. Vous pouvez ici choisir d'activer ou de désactiver les fonctions de Localiser ma position.

### Settings

De nombreux autres paramètres liés à la protection de la vie privée peuvent être trouvés dans l'application **Réglages**.

#### Mode avion

Activation du **mode avion** empêche votre téléphone de contacter les antennes cellulaires. Vous pourrez toujours vous connecter au Wi-Fi et au Bluetooth, donc chaque fois que vous êtes connecté au Wi-Fi, vous pouvez activer ce paramètre.

#### Wi-Fi

You can enable [hardware address randomization](https://support.apple.com/en-us/102509#triswitch) to protect you from tracking across Wi-Fi networks, and on the same network over time. On the network you are currently connected to, tap the :material-information: button:

- [x] Set **Private Wi-Fi Address** to **Fixed** or **Rotating**

Vous avez également la possibilité de **Limiter le suivi de l'adresse IP**. Cette fonction est similaire au relais privé iCloud, mais n'affecte que les connexions aux "traqueurs connus". Étant donné qu'il n'affecte que les connexions à des serveurs potentiellement malveillants, vous pouvez probablement laisser ce paramètre activé, mais si vous ne voulez *pas* que le trafic soit acheminé via les serveurs d'Apple, vous devriez le désactiver.

#### Bluetooth

**Bluetooth** doit être désactivé lorsque vous ne l'utilisez pas, car il augmente votre surface d'attaque. La désactivation du Bluetooth (ou du Wi-Fi) via le Centre de contrôle n'est que temporaire : vous devez le désactiver dans Paramètres pour que la désactivation soit effective.

- [ ] Désactivez **Bluetooth**

Note that Bluetooth is automatically turned on after every system update.

#### Général

Le nom d'appareil de votre iPhone contient par défaut votre prénom, qui sera visible par tous les utilisateurs des réseaux auxquels vous vous connectez. Vous devriez le remplacer par quelque chose de plus générique, comme "iPhone". Select **About** → **Name** and enter the device name you prefer.

Il est important d'installer fréquemment les **mises à jour logicielles** pour bénéficier des derniers correctifs de sécurité. Vous pouvez activer les **mises à jour automatiques** pour maintenir votre téléphone à jour sans avoir à vérifier constamment. Select **Software Update** → **Automatic Updates**:

- [x] Activez **Télécharger les mises à jour d'iOS**
- [x] Activez **Installer les mises à jour d'iOS**
- [x] Activez **Mises à jour de sécurité et fichiers système**

**AirDrop** is commonly used to easily share files, but it represents a significant privacy risk. The AirDrop protocol constantly broadcasts your personal information to your surroundings, with [very weak](https://www.usenix.org/system/files/sec21-heinrich.pdf) security protections. Your identity can easily be discovered by attackers even with limited resources, and the Chinese government has [openly acknowledged](https://arstechnica.com/security/2024/01/hackers-can-id-unique-apple-airdrop-users-chinese-authorities-claim-to-do-just-that/) using such techniques to identify AirDrop users in public since 2022.

- [x] Select **AirDrop** → **Receiving Off**

**AirPlay** vous permet de diffuser de manière transparente du contenu de votre iPhone vers un téléviseur, mais vous n'en avez pas toujours besoin. Select **AirPlay & Continuity** → **Automatically AirPlay**:

- [x] Sélectionnez **Jamais** ou **Demander**

**Actualisation des applications en arrière-plan** permet à vos applications d'actualiser leur contenu lorsque vous ne les utilisez pas. Cela peut les amener à établir des connexions non souhaitées. Turning this off can also save battery life, but may affect an app's ability to receive updated information, particularly weather and messaging apps.

Sélectionnez **Actualisation des applications en arrière-plan** et désactivez toutes les applications que vous ne souhaitez pas voir actualisées en arrière-plan. Si vous ne souhaitez pas qu'une application soit actualisée en arrière-plan, vous pouvez sélectionner à nouveau **Actualisation des applications en arrière-plan** et la **désactiver**.

#### Siri et recherche

Si vous ne voulez pas que quelqu'un puisse contrôler votre téléphone avec Siri lorsqu'il est verrouillé, vous pouvez le désactiver ici.

- [ ] Désactivez **Autoriser Siri lorsque le téléphone est vérouillé**

#### Face ID/Touch ID et code

Définir un mot de passe fort pour votre téléphone est la mesure la plus importante que vous puissiez prendre pour assurer la sécurité physique de votre appareil. Vous devrez faire des compromis entre la sécurité et la commodité : un mot de passe plus long sera fastidieux à saisir à chaque fois, mais un mot de passe ou un code PIN plus court sera plus facile à deviner. Configurer Face ID ou Touch ID avec un mot de passe fort peut être un bon compromis entre convivialité et sécurité.

Select **Turn Passcode On** or **Change Passcode** → **Passcode Options** → **Custom Alphanumeric Code**. Veillez à créer un [mot de passe sûr](../basics/passwords-overview.md).

Si vous souhaitez utiliser Face ID ou Touch ID, vous pouvez le configurer maintenant. Votre téléphone utilisera le mot de passe que vous avez défini précédemment comme solution de secours en cas d'échec de la vérification biométrique. Les méthodes de déverrouillage biométrique existent principalement pour la commodité, même si elles empêchent les caméras de surveillance ou les personnes de vous regarder saisir votre code d'accès par-dessus votre épaule.

Si vous utilisez les déverouillages biométriques, vous devez savoir comment les désactiver rapidement en cas d'urgence. Maintenir enfoncé le bouton latéral ou le bouton d'alimentation et *l'un* des boutons de volume jusqu'à ce que vous voyiez le curseur Glisser pour éteindre désactivera la biométrie, exigeant votre code d'accès pour déverrouiller. Votre code d'accès sera également requis après le redémarrage de l'appareil.

On some older devices, you may have to press the power button five times to disable biometrics instead, or for devices with Touch ID, you may just have to hold down the power button and nothing else. Veillez à faire un essai préalable afin de savoir quelle méthode fonctionne pour votre appareil.

**Stolen Device Protection** adds additional security intended to protect your personal data if your device is stolen while unlocked. If you use biometrics and the Find My Device feature in your Apple Account settings, we recommend enabling this new protection:

- [x] Sélectionnez **Activer la protection**

After enabling Stolen Device Protection, [certain actions](https://support.apple.com/HT212510) will require biometric authentication without a password fallback (in the event that a shoulder surfer has obtained your PIN), such as using password autofill, accessing payment information, and disabling Lost Mode. It also adds a security delay to certain actions performed away from your home or another "familiar location," such as requiring a 1-hour timer to reset your Apple Account password or sign out of your Apple Account. Ce délai a pour but de vous donner le temps d'activer le mode Perdu et de sécuriser votre compte avant qu'un voleur ne puisse réinitialiser votre appareil.

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

#### Confidentialité & sécurité

Les **services de localisation** vous permettent d'utiliser des fonctions telles que Localiser et Plan. Si vous n'avez pas besoin de ces fonctionnalités, vous pouvez désactiver les services de localisation. Vous pouvez également passer en revue et choisir les applications qui peuvent utiliser votre position ici. Sélectionnez **Services de localisation** :

- [ ] Désactivez **Services de localisation**

A purple arrow will appear next to an app in these settings that has used your location recently, while a gray arrow indicates that your location has been accessed within the last 24 hours. If you decide to leave Location Services on, Apple will use it for System Services by default. You can review and pick which services can use your location here. However, if you don't want to submit location analytics to Apple, which they use to improve Apple Maps, you can disable this here as well. Select **System Services**:

- [ ] Turn off **iPhone Analytics**
- [ ] Turn off **Routing & Traffic**
- [ ] Turn off **Improve Maps**

Vous pouvez décider ici d'autoriser les applications à demander à vous **suivre**. La désactivation de cette fonction empêche toutes les applications de vous suivre à l'aide de l'identifiant publicitaire de votre téléphone. Sélectionnez **Suivi** :

- [ ] Désactivez **Autoriser les demandes de suivi des apps**

This is disabled by default and cannot be changed for users under 18.

Vous devriez désactiver **Données de capteur et d’utilisation à des fins de recherche** si vous ne souhaitez pas participer à des études. Sélectionnez **Données de capteur et d’utilisation à des fins de recherche** :

- [ ] Désactivez **Collecte de données de capteur et d'utilisation**

**Contrôle de sécurité** vous permet de visualiser et de révoquer rapidement certaines personnes et applications qui pourraient avoir l'autorisation d'accéder à vos données. Here you can perform an **Emergency Reset**, immediately resetting permissions for all people and apps which might have access to device resources. You can also **Manage Sharing & Access** which allows you to go through and customize who and what has access to your device and account resources.

Vous devriez désactiver l'analyse si vous ne souhaitez pas envoyer de données d'utilisation à Apple. Sélectionnez **Analyse et améliorations** :

- [ ] Désactivez **Partager l'analyse de l'iPhone** ou **Partager l’analyse (iPhone+Watch)**
- [ ] Désactivez **Partager l’analyse d’iCloud**
- [ ] Désactivez **Améliorer Fitness+**
- [ ] Désactivez **Améliorer la sécurité**
- [ ] Décochez **Améliorer Siri et Dictée**
- [ ] Turn off **Improve Assistive Voice Features**
- [ ] Turn off **Improve AR Location Accuracy**

Désactivez **Publicités personnalisées** si vous ne voulez pas de publicités ciblées. Select **Apple Advertising**:

- [ ] Décochez **Publicités personnalisées**

**Rapport de confidentialité des apps** est un outil intégré qui vous permet de voir quelles sont les autorisations utilisées par vos applications. Sélectionnez **Rapport de confidentialité des apps** :

- [x] Sélectionnez **Activer le rapport de confidentialité des apps**

Le [mode Isolement](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode) est un paramètre de sécurité que vous pouvez activer pour rendre votre téléphone plus résistant aux attaques. Sachez que certaines applications et fonctionnalités [ne fonctionneront pas](https://support.apple.com/HT212650) comme elles le font normalement.

- [x] Sélectionnez **Activer le mode Isolement**

## Conseils supplémentaires

### Appels E2EE

Les appels téléphoniques normaux effectués avec l'application Téléphone par l'intermédiaire de votre opérateur ne sont pas E2EE. Both FaceTime Video and FaceTime Audio calls are E2EE. Alternatively, you can use [another app](../real-time-communication.md) like Signal for E2EE calls.

### iMessage chiffré

The [color of the message bubble](https://support.apple.com/en-us/104972) in the Messages app indicates whether your messages are E2EE or not. A blue bubble indicates that you're using iMessage with E2EE, while a green bubble indicates the other party is using either the outdated SMS and MMS protocols or RCS. RCS on iOS is **not** E2EE. Currently, the only way to have E2EE in Messages is for both parties to be using iMessage on Apple devices.

Si vous ou votre partenaire de messagerie avez activé la sauvegarde iCloud sans la protection avancée des données, la clé de chiffrement sera stockée sur les serveurs d'Apple, ce qui signifie qu'ils peuvent accéder à vos messages. Additionally, iMessage's key exchange is not as secure as alternative implementations like Signal's (which allows you to view the recipients key and verify by QR code), so it shouldn't be relied on for particularly sensitive communications.

### Photo Permissions

When an app prompts you for access to your device's photo library, iOS provides you with options to limit what an app can access.

Rather than allow an app to access all the photos on your device, you can allow it to only access whichever photos you choose by tapping the "Select Photos..." option in the permission dialog. You can change photo access permissions at any time by navigating to **Settings** → **Privacy & Security** → **Photos**.

![Photo Permissions](../assets/img/ios/photo-permissions-light.png#only-light) ![Photo Permissions](../assets/img/ios/photo-permissions-dark.png#only-dark)

**Add Photos Only** is a permission that only gives an app the ability to download photos to the photo library. Not all apps which request photo library access provide this option.

![Private Access](../assets/img/ios/private-access-light.png#only-light) ![Private Access](../assets/img/ios/private-access-dark.png#only-dark)

Some apps also support **Private Access**, which functions similarly to the **Limited Access** permission. However, photos shared to apps using Private Access include their location by default. We recommend unchecking this setting if you do not [remove photo metadata](../data-redaction.md) beforehand.

### Contact Permissions

Similarly, rather than allow an app to access all the contacts saved on your device, you can allow it to only access whichever contacts you choose. You can change contact access permissions at any time by navigating to **Settings** → **Privacy & Security** → **Contacts**.

![Contact Permissions](../assets/img/ios/contact-permissions-light.png#only-light) ![Contact Permissions](../assets/img/ios/contact-permissions-dark.png#only-dark)

### Require Biometrics and Hide Apps

iOS offers the ability to lock most apps behind Touch ID/Face ID or your passcode, which can be useful for protecting sensitive content in apps which do not provide the option themselves. You can lock an app by long-pressing on it and selecting **Require Face ID/Touch ID**. Any app locked in this way requires biometric authentication whenever opening it or accessing its contents in other apps. Also, notification previews for locked apps will not be shown.

In addition to locking apps behind biometrics, you can also hide apps so that they don't appear on the Home Screen, App Library, the app list in **Settings**, etc. While hiding apps may be useful in situations where you have to hand your unlocked phone to someone else, the concealment provided by the feature is not absolute, as a hidden app is still visible in some places such as the battery usage list. Moreover, one notable tradeoff of hiding an app is that you will not receive any of its notifications.

You can hide an app by long-pressing on it and selecting **Require Face ID/Touch ID** → **Hide and Require Face ID/Touch ID**. Note that pre-installed Apple apps, as well as the default web browser and email app, cannot be hidden. Hidden apps reside in a **Hidden** folder at the bottom of the App Library, which can be unlocked using biometrics. This folder appears in the App Library whether you hid any apps or not, which provides you a degree of plausible deniability.

### Redacting Elements in Images

If you need to hide information in a photo, you can use Apple's built-in editing tools to do so.

If your device supports it, you can use the [Clean Up](https://support.apple.com/en-us/121429) feature to pixelate faces or remove objects from images.

- Open the **Photos** app and tap the photo you have selected for redaction
- Tap the :material-tune: (at the bottom of the screen)
- Tap the button labeled **Clean Up**
- Draw a circle around whatever you want to redact. Faces will be pixelated and it will attempt to delete anything else.

Our warning [against blurring text](../data-redaction.md) also applies here, so we recommend to instead add a black shape with 100% opacity over it. In addition to redacting text, you can also black out any face or object using the **Photos** app.

- Tap the image you have selected for redaction
- Tap the :material-tune: (at the bottom of the screen) → markup symbol (top right) → plus icon at the bottom right
- Select **Add Shape** and choose the square or circle
- On the toolbar, tap the circle (left-most option) and choose black as the color for filling in the shape. You can also move the shape and increase its size as you see fit.

**Don't** use the highlighter to obfuscate information, as its opacity is not quite 100%.

### Éviter le jailbreaking

Le jailbreaking d'un iPhone compromet sa sécurité et vous rend vulnérable. L'exécution de logiciels tiers non fiables peut entraîner l'infection de votre appareil par des logiciels malveillants.

### Bêtas iOS

Apple met toujours des versions bêta d'iOS à la disposition de ceux qui souhaitent aider à trouver et à signaler des bogues. Nous vous déconseillons d'installer des logiciels bêta sur votre téléphone. Les versions bêta sont potentiellement instables et peuvent présenter des failles de sécurité non découvertes.

## Points forts en matière de sécurité

### Avant le premier déverrouillage

If your threat model includes [:material-target-account: Targeted Attacks](../basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red} that involve forensic tools, and you want to minimize the chance of exploits being used to access your phone, you should restart your device frequently. L'état *après* un redémarrage mais *avant* le déverrouillage de votre appareil est appelé "Before First Unlock" (BFU), et lorsque votre appareil est dans cet état, il est [nettement plus difficile](https://belkasoft.com/checkm8_glossary) pour les outils de criminalistique d'exploiter des vulnérabilités pour accéder à vos données. Cet état BFU vous permet de recevoir des notifications pour les appels, les textes et les alarmes, mais la plupart des données de votre appareil sont toujours chiffrées et inaccessibles. Cela peut s'avérer peu pratique, il convient donc de se demander si ces compromis sont judicieux dans votre situation.
