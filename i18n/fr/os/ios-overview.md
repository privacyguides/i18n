---
title: Introduction à iOS
icon: simple/apple
description: iOS est un système d'exploitation mobile développé par Apple pour l'iPhone.
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

Plus récemment, il a été constaté qu'Apple [transmettait des données analytiques même lorsque le partage des données analytiques était désactivé](https://gizmodo.com/apple-iphone-analytics-tracking-even-when-off-app-store-1849757558) sur iOS, et ces données [semblent](https://twitter.com/mysk_co/status/1594515229915979776) être facilement reliées à des identifiants de compte iCloud uniques, bien qu'elles soient censées être anonymes. Apple n'a pas corrigé [ces problèmes](https://gizmodo.com/clarence-thomas-aide-venmo-laywers-supreme-court-1850631585) à date de juillet 2023.

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

- [x] Turn on **Private Wi-Fi Address**

You also have the option to **Limit IP Address Tracking**. This is similar to iCloud Private Relay but only affects connections to "known trackers." Because it only affects connections to potentially malicious servers, this setting is probably fine to leave enabled, but if you don't want *any* traffic to be routed through Apple's servers, you should turn it off.

#### Bluetooth

**Bluetooth** should be disabled when you aren't using it as it increases your attack surface. Disabling Bluetooth (or Wi-Fi) via the Control Center only disables it temporarily: you must switch it off in Settings for disabling it to remain effective.

- [ ] Turn off **Bluetooth**

#### Général

Your iPhone's device name will by default contain your first name, and this will be visible to anyone on networks you connect to. You should change this to something more generic, like "iPhone." Select **About** > **Name** and enter the device name you prefer.

It is important to install **Software Updates** frequently to get the latest security fixes. You can enable **Automatic Updates** to keep your phone up-to-date without needing to constantly check for updates. Select **Software Update** > **Automatic Updates**:

- [x] Turn on **Download iOS Updates**
- [x] Turn on **Install iOS Updates**
- [x] Turn on **Security Responses & System Files**

**AirDrop** allows you to easily transfer files, but it can allow strangers to send you files you do not want.

- [x] Select **AirDrop** > **Receiving Off**

**AirPlay** lets you seamlessly stream content from your iPhone to a TV; however, you might not always want this. Select **AirPlay & Handoff** > **Automatically AirPlay to TVs**:

- [x] Select **Never** or **Ask**

**Background App Refresh** allows your apps to refresh their content while you're not using them. This may cause them to make unwanted connections. Turning this off can also save battery life, but it may affect an app's ability to receive updated information, particularly weather and messaging apps.

Select **Background App Refresh** and switch off any apps you don't want to continue refreshing in the background. If you don't want any apps to refresh in the background, you can select **Background App Refresh** again and turn it **Off**.

#### Siri & Search

If you don't want anyone to be able to control your phone with Siri when it is locked, you can turn that off here.

- [ ] Turn off **Allow Siri When Locked**

#### Face ID/Touch ID & Passcode

Setting a strong password on your phone is the most important step you can take for physical device security. You'll have to make tradeoffs here between security and convenience: A longer password will be annoying to type in every time, but a shorter password or PIN will be easier to guess. Setting up Face ID or Touch ID along with a strong password can be a good compromise between usability and security.

Select **Turn Passcode On** or **Change Passcode** > **Passcode Options** > **Custom Alphanumeric Code**. Make sure that you create a [secure password](https://www.privacyguides.org/basics/passwords-overview/).

If you wish to use Face ID or Touch ID, you can go ahead and set it up now. Your phone will use the password you set up earlier as a fallback in case your biometric verification fails. Biometric unlock methods are primarily a convenience, although they do stop surveillance cameras or people over your shoulder from watching you input your passcode.

If you use biometrics, you should know how to turn them off quickly in an emergency. Holding down the side or power button and *either* volume button until you see the Slide to Power Off slider will disable biometrics, requiring your passcode to unlock. Your passcode will also be required after device restarts.

On some older devices, you may have to press the power button five times to disable biometrics instead, or for devices with Touch ID you may just have to hold down the power button and nothing else. Make sure you try this in advance so you know which method works for your device.

**Allow Access When Locked** gives you options for what you can allow when your phone is locked. The more of these options you disable, the less someone without your password can do, but the less convenient it will be for you. Pick and choose which of these you don't want someone to have access to if they get their hands on your phone.

- [ ] Turn off **Today View and Search**
- [ ] Turn off **Notification Center**
- [ ] Turn off **Control Center**
- [ ] Turn off **Lock Screen Widgets**
- [ ] Turn off **Siri**
- [ ] Turn off **Reply with Message**
- [ ] Turn off **Home Control**
- [ ] Turn off **Wallet**
- [ ] Turn off **Return Missed Calls**
- [ ] Turn off **USB Accessories**

iPhones are already resistant to brute-force attacks by making you wait long periods of time after multiple failed attempts; however, there have historically been exploits to get around this. To be extra safe, you can set your phone to wipe itself after 10 failed passcode attempts.

!!! warning "Avertissement"

    With this setting enabled, someone could intentionally wipe your phone by entering the wrong password many times. Make sure you have proper backups and only enable this setting if you feel comfortable with it.

- [x] Turn on **Erase Data**

#### Confidentialité

**Location Services** allows you to use features like Find My and Maps. If you don't need these features, you can disable Location Services. Alternatively, you can review and pick which apps can use your location here. Select **Location Services**:

- [ ] Turn off **Location Services**

You can decide to allow apps to request to **track** you here. Disabling this disallows all apps from tracking you with your phone's advertising ID. Select **Tracking**:

- [ ] Turn off **Allow Apps to Request to Track**

You should turn off **Research Sensor & Usage Data** if you don't wish to participate in studies. Select **Research Sensor & Usage Data**:

- [ ] Turn off **Sensor & Usage Data Collection**

**Safety Check** allows you to quickly view and revoke certain people and apps that might have permission to access your data. Here you can perform an **Emergency Reset**, immediately resetting permissions for all people and apps which might have access to device resources, and you can **Manage Sharing & Access** which allows you to go through and customize who and what has access to your device and account resources.

You should disable analytics if you don't wish to send Apple usage data. Select **Analytics & Improvements**:

- [ ] Turn off **Share iPhone Analytics** or **Share iPhone & Watch Analytics**
- [ ] Turn off **Share iCloud Analytics**
- [ ] Turn off **Improve Fitness+**
- [ ] Turn off **Improve Safety**
- [ ] Turn off **Improve Siri & Dictation**

Disable **Personalized Ads** if you don't want targeted ads. Select **Apple Advertising**

- [ ] Turn off **Personalized Ads**

**App Privacy Report** is a built-in tool that allows you to see which permissions your apps are using. Select **App Privacy Report**:

- [x] Select **Turn On App Privacy Report**

[Lockdown Mode](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode) is a security setting you can enable to make your phone more resistant to attacks. Be aware that certain apps and features [won't work](https://support.apple.com/en-us/HT212650) as they do normally.

- [x] Select **Turn On Lockdown Mode**

## Additional Advice

### E2EE Calls

Normal phone calls made with the Phone app through your carrier are not E2EE. Both FaceTime Video and FaceTime Audio calls are E2EE, or you can use [another app](../real-time-communication.md) like Signal.

### Avoid Jailbreaking

Jailbreaking an iPhone undermines its security and makes you vulnerable. Running untrusted, third-party software could cause your device to be infected with malware.

### Encrypted iMessage

The color of the message bubble in the Messages app indicates whether your messages are E2EE or not. A blue bubble indicates that you're using iMessage with E2EE, while a green bubble indicates they're using the outdated SMS and MMS protocols. Currently, the only way to get E2EE in Messages is for both parties to be using iMessage on Apple devices.

If either you or your messaging partner have iCloud Backup enabled without Advanced Data Protection, the encryption key will be stored on Apple's servers, meaning they can access your messages. Additionally, iMessage's key exchange is not as secure as alternative implementations, like Signal (which allows you to view the recipients key and verify by QR code), so it shouldn't be relied on for particularly sensitive communications.

### Blacking Out Faces/Information

If you need to hide information in a photo, you can use Apple's built-in tools to do so. Open the photo you want to edit, press edit in the top right corner of the screen, then press the markup symbol at the top right. Press the plus at the bottom right of the screen, then press the rectangle icon. Now, you can place a rectangle anywhere on the image. Make sure to press the shape icon at the bottom left and select the filled-in rectangle. **Don't** use the highlighter to obfuscate information, because its opacity is not quite 100%.

### iOS Betas

Apple always makes beta versions of iOS available early for those that wish to help find and report bugs. We don't recommend installing beta software on your phone. Beta releases are potentially unstable and could have undiscovered security vulnerabilities.

## Security Highlights

### Before First Unlock

If your threat model includes forensic tools and you want to minimize the chance of exploits being used to access your phone, you should restart your device frequently. The state *after* a reboot but *before* unlocking your device is referred to as "Before First Unlock" (BFU), and when your device is in that state it makes it [significantly more difficult](https://belkasoft.com/checkm8_glossary) for forensic tools to exploit vulnerabilities to access your data. This BFU state allows you to receive notifications for calls, texts, and alarms, but most of the data on your device is still encrypted and inaccessible. This can be impractical, so consider whether these trade-offs make sense for your situation.
