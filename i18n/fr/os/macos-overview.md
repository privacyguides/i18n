---
title: Sur macOS
icon: material/apple-finder
description: macOS est le système d'exploitation d'Apple pour ordinateurs de bureau fonctionnant avec leur propre matériel pour assurer une sécurité renforcée.
---

**macOS** est un système d'exploitation Unix développé par Apple pour leurs ordinateurs Mac. Pour améliorer la confidentialité de macOS, il est possible de désactiver la télémétrie et renforcer les paramètres existants de confidentialité et de sécurité.

Les anciens Mac à base de processeur Intel et les Hackintosh ne prennent pas en charge toutes les fonctions de sécurité offertes par macOS. Pour améliorer la sécurité des données, nous recommandons d'utiliser un Mac plus récent avec [Apple Silicon](https://support.apple.com/HT211814).

## Remarques concernant la vie privée

macOS pose quelques problèmes importants en matière de protection de la vie privée, qu'il convient de prendre en compte. Ils concernent le système d'exploitation lui-même, et non les autres applications et services d'Apple.

### Verrouillage d'activation

Les nouveaux appareils Apple Silicon peuvent être configurés sans connexion internet. Cependant, la récupération ou la réinitialisation de votre Mac **nécessitera** une connexion internet aux serveurs d'Apple pour vérifier la base de données Verrouillage d'activation des appareils perdus ou volés.

### Contrôles de révocation des applications

macOS effectue des contrôles en ligne lorsque vous ouvrez une application afin de vérifier si elle contient des logiciels malveillants connus et si le certificat de signature du développeur a été révoqué.

Le service OCSP d'Apple utilise le chiffrement HTTPS, de sorte que seul Apple soit en mesure de voir quelles applications vous ouvrez. Ils ont [publié des informations](https://support.apple.com/HT202491) sur leur politique de journalisation pour ce service. Ils ont également [promis](http://lapcatsoftware.com/articles/2024/8/3.html) d'ajouter un mécanisme permettant aux personnes de refuser ce contrôle en ligne, mais celui-ci n'a pas été ajouté à macOS.

Bien que vous [puissiez](https://eclecticlight.co/2021/02/23/how-to-run-apps-in-private) désactiver manuellement cette vérification assez facilement, nous vous déconseillons de le faire à moins que les vérifications de révocation effectuées par macOS ne vous compromettent gravement, car elles jouent un rôle important en empêchant l'exécution d'applications compromises.

## Configuration recommandée

Lorsque vous configurez votre Mac pour la première fois, vous disposez d'un compte d'administrateur, dont les privilèges sont plus élevés que ceux d'un compte d'utilisateur standard. macOS dispose d'un certain nombre de protections qui empêchent les logiciels malveillants et d'autres programmes d'abuser de vos privilèges d'administrateur, de sorte que l'utilisation de ce compte est généralement sûre.

Cependant, des exploits dans des utilitaires de protection tels que `sudo` ont été [découverts dans le passé](https://bogner.sh/2014/03/another-mac-os-x-sudo-password-bypass). Si vous souhaitez éviter que les programmes que vous exécutez n'abusent de vos privilèges d'administrateur, vous pouvez envisager de créer un deuxième compte d'utilisateur standard, que vous utiliserez pour les opérations quotidiennes. Cela présente l'avantage supplémentaire de rendre plus évident le fait qu'une application a besoin d'un accès administrateur, parce qu'elle vous demandera à chaque fois de fournir des informations d'identification.

Si vous utilisez un deuxième compte, il n'est pas strictement nécessaire de vous connecter à votre compte administrateur d'origine à partir de l'écran de connexion de macOS. Lorsque vous effectuez, en tant qu'utilisateur standard, une opération nécessitant des autorisations d'administrateur, le système vous invite à vous authentifier, ce qui vous permet d'entrer une seule fois vos informations d'identification d'administrateur en tant qu'utilisateur standard. Apple fournit des [conseils](https://support.apple.com/HT203998) sur la façon de masquer votre compte administrateur si vous préférez ne voir qu'un seul compte sur votre écran de connexion.

### iCloud

Lorsque vous utilisez des services Apple comme iCloud, la plupart de vos informations sont stockées sur leurs serveurs et sécurisées par des clés *auxquelles Apple a accès* par défaut. C'est ce qu'Apple appelle la [Protection Standard des Données](https://support.apple.com/en-us/102651).

Par conséquent, si vous utilisez iCloud, vous devriez [activer la**Protection avancée des données**](https://support.apple.com/HT212520). Cela permet de chiffrer la quasi-totalité de vos données iCloud à l'aide de clés stockées sur vos appareils (chiffrement de bout en bout), plutôt que sur les serveurs d'Apple, de sorte que vos données iCloud sont sécurisées en cas de fuite de données, et qu'elles sont par ailleurs cachées à Apple.

Si vous souhaitez pouvoir installer des applications à partir de l'App Store mais que vous ne voulez pas activer iCloud, vous pouvez vous connecter à votre compte Apple à partir de l'App Store plutôt qu'à partir des **Réglages du Système**.

### Paramètres systèmes

Il y a un certain nombre de paramètres intégrés que vous devriez confirmer ou modifier pour renforcer votre système. Ouvrez l'application **Paramètres** :

#### Bluetooth

- [ ] Désactiver **Bluetooth** (sauf si vous l'utilisez)

#### Réseau

Selon que vous utilisez **Wi-Fi** ou **Ethernet** (indiqué par un point vert et le mot "connecté"), cliquez sur l'icône correspondante.

Cliquez sur le bouton "Détails" à côté du nom de votre réseau :

- [x] Sélectionnez **Rotation** sous **Adresse Wi-Fi privée**

- [x] Activer **Limiter le pistage des adresses IP**

##### Pare-feu

Votre pare-feu bloque les connexions réseau indésirables. Plus les réglages de votre pare-feu sont stricts, plus votre Mac est sécurisé. Toutefois, certains services seront bloqués. Vous devriez configurer votre pare-feu de manière à ce qu'il soit aussi strict que possible sans bloquer les services que vous utilisez.

- [x] Activer **Pare-feu**

Cliquez sur le bouton **Options** :

- [x] Activer **Bloquer toutes les connexions entrantes**

Si cette configuration est trop stricte, vous pouvez revenir et la décocher. Toutefois, macOS vous invitera généralement à autoriser les connexions entrantes pour une application si celle-ci le demande.

#### Général

Par défaut, le nom de votre appareil sera quelque chose comme "iMac de [votre nom]". Comme ce nom est [diffusé publiquement sur votre réseau](https://support.apple.com/guide/mac-help/change-computers-local-hostname-mac-mchlp2322/26/mac/26#:~:text=The%20local%20hostname%2C%20or%20local%20network%20name%2C%20is%20displayed%20at%20the%20bottom%20of%20the%20Sharing%20settings%20window.%20It%20identifies%20your%20Mac%20to%20Bonjour%2Dcompatible%20services.), vous voulez changer le nom de votre appareil en quelque chose de générique comme "Mac".

Cliquez sur **A propos** et tapez le nom de votre appareil dans le champ **Nom**.

##### Mises à jour du logiciel

Vous devriez installer automatiquement toutes les mises à jour disponibles pour vous assurer que votre Mac dispose des derniers correctifs de sécurité.

Cliquez sur la petite icône :material-information-outline: à côté de **Mises à jour automatiques** :

- [x] Activer **Télécharger les nouvelles mises à jour lorsqu'elles sont disponibles**

- [x] Activer **Installer les mises à jour de macOS**

- [x] Activer **Installer les réponses de sécurité et les fichiers système**

#### Apple Intelligence & Siri

Si vous n'utilisez pas ces fonctionnalités sur macOS, vous devriez les désactiver :

- [Désactiver **Apple Intelligence**
- [ ] Désactivez **Siri**

**[Apple Intelligence](https://apple.com/legal/privacy/data/en/intelligence-engine)** n'est disponible que si votre appareil le prend en charge. Apple Intelligence utilise une combinaison de traitement sur l'appareil et de son [Private Cloud Compute](https://security.apple.com/blog/private-cloud-compute) pour les tâches qui nécessitent une puissance de traitement supérieure à celle que votre appareil peut fournir.

To see a report of all the data sent via Apple Intelligence, you can navigate to **Privacy & Security** → **Apple Intelligence Report** and press **Export Activity** to see activity from the either the last 15 minutes or 7 days, depending on what you set it for. Similar to the **App Privacy Report** which shows you the recent permissions accessed by the apps on your phone, the Apple Intelligence Report likewise shows what is being sent to Apple's servers while using Apple Intelligence.

Par défaut, l'intégration de ChatGPT est désactivée. If you don't want ChatGPT integration anymore, you can navigate to **ChatGPT**:

- [ ] Turn off **Use ChatGPT**

You can also have it ask for confirmation every time if you leave ChatGPT integration on:

- [x] Turn on **Confirm Requests**

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

Any request made with ChatGPT will be sent to ChatGPT's servers, there is no on-device processing and no PCC like with Apple Intelligence.

</div>

#### Confidentialité & sécurité

Chaque fois qu'une application demande une autorisation, celle-ci apparaît ici. Vous pouvez décider des applications pour lesquelles vous souhaitez autoriser ou refuser des autorisations spécifiques.

##### Services de localisation

Vous pouvez autoriser les services de localisation individuellement pour chaque application. Si vous n'avez pas besoin que des applications utilisent votre position, la désactivation complète des services de localisation est l'option la plus privée.

- [ ] Désactivez **Services de localisation**

##### Statistiques & améliorations

Decide whether you want to share analytics data with Apple and app developers.

##### Publicité Apple

Décidez si vous souhaitez des publicités personnalisées en fonction de votre utilisation.

- [ ] Décochez **Publicités personnalisées**

##### FileVault

Sur les appareils modernes dotés d'une Secure Enclave (puce de sécurité T2 Apple, Apple Silicon), vos données sont toujours chiffrées, mais elles sont déchiffrées automatiquement par une clé matérielle si votre appareil ne détecte pas qu'il a été altéré. L'activation de [FileVault](../encryption.md#filevault) requiert en outre votre mot de passe pour déchiffrer vos données, ce qui améliore considérablement la sécurité, en particulier lorsque l'ordinateur est éteint ou avant la première connexion après l'allumage.

Sur les anciens ordinateurs Mac à processeur Intel, FileVault est la seule forme de chiffrement de disque disponible par défaut et doit toujours être activé.

- [x] Cliquez sur **Activer**

##### Mode Isolement

**[Lockdown Mode](https://support.apple.com/guide/mac-help/lock-mac-targeted-a-cyberattack-ibrw66f4e191/mac)** disables some features in order to improve security. Some apps or features won't work the same way they do when it's off. For example, Javascript Just-In-Time ([JIT](https://hacks.mozilla.org/2017/02/a-crash-course-in-just-in-time-jit-compilers)) compilation and [WebAssembly](https://developer.mozilla.org/docs/WebAssembly) are disabled in Safari with Lockdown Mode enabled. We recommend enabling Lockdown Mode and seeing whether it significantly impacts daily usage.

- [x] Cliquez sur **Activer**

### Adresse MAC aléatoire

macOS uses a randomized MAC address when [performing Wi-Fi scans](https://support.apple.com/guide/security/privacy-features-connecting-wireless-networks-secb9cb3140c/web) while disconnected from a network.

You can set your [MAC address to be randomized](https://support.apple.com/en-us/102509) per network and rotate occasionally to prevent tracking between networks and on the same network over time.

Allez dans **Paramètres Système** → **Réseaux** → **Wi-Fi** → **Détails** et réglez l'**adresse Wi-Fi privée** sur **Fixe** si vous souhaitez une adresse fixe mais unique pour le réseau auquel vous êtes connecté, ou sur **Rotation** si vous souhaitez qu'elle change au fil du temps.

Envisagez également de modifier votre nom d'hôte, qui est un autre identifiant d'appareil diffusé sur le réseau auquel vous êtes connecté. Vous pouvez définir votre nom d'hôte avec quelque chose de générique comme "MacBook Air", "Laptop", "MacBook Pro de John", ou "iPhone" dans **Réglages système** → **Général** → **Partage**.

## Protections de sécurité

macOS utilise la défense en profondeur en s'appuyant sur plusieurs couches de protections logicielles et matérielles, avec des propriétés différentes. Cela garantit qu'une défaillance dans une couche ne compromet pas la sécurité globale du système.

### Sécurité du logiciel

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

macOS vous permet d'installer des mises à jour bêta. These are unstable and may come with [extra telemetry](https://beta.apple.com/privacy) since they're for testing purposes. Pour cette raison, nous vous recommandons d'éviter les logiciels bêta en général.

</div>

#### Volume du système signé

macOS's system components are protected in a read-only [signed system volume](https://support.apple.com/guide/security/signed-system-volume-security-secd698747c9/web), meaning that neither you nor malware can alter important system files.

Le volume du système est vérifié en cours d'exécution et toute donnée qui n'est pas signée par une signature cryptographique valide d'Apple sera rejetée.

#### Protection de l'intégrité du système

macOS définit certaines restrictions de sécurité qui ne peuvent pas être contournées. These are called [Mandatory Access Controls](https://support.apple.com/guide/security/system-integrity-protection-secb7ea06b49/1/web/1), and they form the basis of the sandbox, parental controls, and [System Integrity Protection](https://support.apple.com/en-us/102149) on macOS.

La protection de l'intégrité du système met en lecture seule les emplacements de fichiers critiques afin de les protéger contre toute modification par des codes malveillants. Cela s'ajoute à la protection de l'intégrité du noyau basée sur le matériel, qui empêche le noyau d'être modifié en mémoire.

#### Sécurité des applications

##### Sandbox des applications

Sur macOS, c'est le développeur qui détermine si une application est mise en bac à sable (sandbox) lorsqu'il la signe. The [App Sandbox](https://developer.apple.com/documentation/xcode/configuring-the-macos-app-sandbox) protects against vulnerabilities in the apps you run by limiting what a malicious actor can access in the event that the app is exploited. L'App Sandbox ne peut *à lui seul* protéger contre les [:material-package-variant-closed-remove: Attaques de la Chaîne d'Approvisionnement ](../basics/common-threats.md#attacks-against-certain-organizations ""){.pg-viridian} par des développeurs malveillants. For that, sandboxing needs to be enforced by someone other than the developer themselves, as it is on the [App Store](https://support.apple.com/guide/security/gatekeeper-and-runtime-protection-sec5599b66df/1/web/1#:~:text=All%20apps%20from%20the%20App%20Store%20are%20sandboxed%20to%20restrict%20access%20to%20data%20stored%20by%20other%20apps.).

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

Les logiciels téléchargés en dehors de l'App Store officiel n'ont pas besoin d'être placés en sandbox. Si votre modèle de menace donne la priorité à la défense contre [:material-bug-outline: Attaques passives](../basics/common-threats.md#security-and-privacy){ .pg-orange }, vous pouvez alors vérifier si le logiciel que vous téléchargez en dehors de l'App Store est en bac à sable (sandbox), ce qui est laissé à l'appréciation du développeur.

</div>

Vous pouvez vérifier si une application utilise l'App Sandbox de plusieurs façons :

Vous pouvez vérifier si les applications déjà en cours d'exécution sont placées dans un bac à sable à l'aide du [Moniteur d'Activité](https://developer.apple.com/documentation/security/protecting-user-data-with-app-sandbox#Verify-that-your-app-uses-App-Sandbox).

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

Attention, ce n'est pas parce que l'un des processus d'une application est sandboxé que tous le sont.

</div>

Vous pouvez aussi vérifier les applications avant de les exécuter en lançant cette commande dans le terminal :

``` zsh
codesign -dvvv --entitlements - <path to your app>
```

Si une application est sandboxée, vous devriez obtenir le résultat suivant :

``` zsh
    [Key] com.apple.security.app-sandbox
    [Value]
        [Bool] true
```

Si vous constatez que l'application que vous souhaitez utiliser n'est pas sandboxée, vous pouvez utiliser des méthodes de [compartimentage](../basics/common-threats.md#security-and-privacy) telles que des machines virtuelles ou des appareils séparés, utiliser une application similaire qui est sandboxée, ou choisir de ne pas utiliser l'application.

##### Hardened Runtime (exécution renforcée)

[L'exécution renforcée](https://developer.apple.com/documentation/security/hardened_runtime) est une forme de protection supplémentaire pour les applications qui empêche certains types d'exploitations. Il améliore la sécurité des applications contre de potentielles exploitations en désactivant certaines fonctions comme le JIT.

Vous pouvez vérifier si une application utilise le Hardened Runtime en utilisant cette commande :

``` zsh
codesign -dv <path to your app>
```

Si l'option Hardened Runtime est activée, vous verrez `flags=0x10000(runtime)`. La sortie `runtime` signifie que Hardened Runtime est activé. Il peut y avoir d'autres indicateurs, mais c'est l'indicateur runtime qui nous intéresse ici.

Vous pouvez activer une colonne dans Activity Monitor appelée "Restricted", qui est un drapeau empêchant les programmes d'injecter du code via l'[éditeur de liens dynamiques](https://pewpewthespells.com/blog/blocking_code_injection_on_ios_and_os_x.html) de macOS. Idéalement, la réponse devrait être "Oui".

##### Antivirus

macOS comes with two forms of [malware defense](https://support.apple.com/guide/security/protecting-against-malware-sec469d47bd8/1/web/1):

1. La protection contre le lancement de logiciels malveillants est assurée par le processus d'examen des applications de l'App Store, ou *Notarization* (fait partie de *Gatekeeper*), un processus au cours duquel les applications tierces sont analysées par Apple à la recherche de logiciels malveillants connus avant d'être autorisées à s'exécuter. Les applications doivent être signées par les développeurs à l'aide d'une clé fournie par Apple. Cela garantit que vous exécutez des logiciels provenant des vrais développeurs. La notarisation exige également que les développeurs activent le Hardened Runtime pour leurs applications, ce qui limite les vulnérabiltés.
2. La protection contre les autres logiciels malveillants et la remédiation des logiciels malveillants existants sur votre système sont assurées par *XProtect*, un logiciel antivirus plus traditionnel intégré à macOS.

Nous vous déconseillons d'installer des logiciels antivirus tiers, car ils n'ont généralement pas l'accès nécessaire au niveau du système pour fonctionner correctement, en raison des limitations imposées par Apple aux applications tierces, et parce que l'octroi des niveaux d'accès élevés qu'ils demandent pose souvent un risque encore plus grand pour la sécurité et la confidentialité de votre ordinateur.

##### Sauvegardes

macOS comes with automatic backup software called [Time Machine](https://support.apple.com/HT201250), so you can create [encrypted backups](https://support.apple.com/guide/mac-help/keep-your-time-machine-backup-disk-secure-mh21241/mac) to an external drive or a network drive in the event of corrupted/deleted files.

### Sécurité matérielle

De nombreuses fonctions de sécurité modernes de macOS - telles que le Secure Boot moderne, l'atténuation des vulnérabilité au niveau matériel, les vérifications de l'intégrité du système d'exploitation et le chiffrement des fichiers - reposent sur l'Apple Silicon, et le matériel le plus récent d'Apple est toujours doté de la [meilleure sécurité](https://support.apple.com/guide/security/apple-soc-security-sec87716a080/1/web/1). Nous encourageons uniquement l'utilisation d'Apple Silicon, et non d'anciens ordinateurs Mac basés sur Intel, ou Hackintoshes.

Certaines de ces fonctions de sécurité modernes sont disponibles sur les anciens ordinateurs Mac à base d'Intel équipés de la puce de sécurité T2 d'Apple, mais cette puce est susceptible d'être exploitée par *checkm8*, ce qui pourrait compromettre sa sécurité.

If you use Bluetooth accessories such as a keyboard, we recommend that you use official Apple ones as their firmware will [automatically be updated](https://support.apple.com/en-us/120303#:~:text=Firmware%20updates%20are%20automatically%20delivered%20in%20the%20background%20while%20the%20Magic%20Keyboard%20is%20actively%20paired%20to%20a%20device%20running%20macOS%2C%20iOS%2C%20iPadOS%2C%20or%20tvOS.) for you by macOS. L'utilisation d'accessoires tiers est possible, mais il faut penser à installer régulièrement les mises à jour du micrologiciel de ces accessoires.

Apple's SoCs focus on [minimizing attack surface](https://support.apple.com/en-vn/guide/security/secf020d1074/web#:~:text=Security%2Dfocused%20hardware%20follows%20the%20principle%20of%20supporting%20limited%20and%20discretely%20defined%20functions%20to%20minimize%20attack%20surface.) by relegating security functions to dedicated hardware with limited functionality.

#### ROM d'amorçage

macOS prevents malware persistence by only allowing official Apple software to run at boot time; this is known as [secure boot](https://support.apple.com/en-vn/guide/security/secac71d5623/1/web/1). Mac computers verify this with a bit of read-only memory on the SoC called the [boot ROM](https://support.apple.com/en-vn/guide/security/aside/sec5240db956/1/web/1), which is [laid down during the manufacturing of the chip](https://support.apple.com/en-vn/guide/security/secf020d1074/1/web/1#:~:text=which%20is%20laid%20down%20during%20Apple%20SoC%20fabrication).

La ROM d'amorçage constitue la racine de confiance du matériel. This ensures that malware cannot tamper with the boot process, since the boot ROM is immutable. Lorsque votre Mac démarre, la ROM d'amorçage est la première chose qui s'exécute, formant le premier maillon de la chaîne de confiance.

Mac computers can be configured to boot in [three security modes](https://support.apple.com/guide/deployment/startup-security-dep5810e849c/web#dep32fb404e1): *Full Security*, *Reduced Security*, and *Permissive Security*, with the default setting being Full Security. You should ideally be using Full Security mode and avoid things like **[kernel extensions](https://support.apple.com/guide/deployment/system-extensions-in-macos-depa5fb8376f/web#dep51e097f45)** that force you to lower your security mode. Veillez à [vérifier](https://support.apple.com/guide/mac-help/change-security-settings-startup-disk-a-mac-mchl768f7291/mac) que vous utilisez le mode Sécurité complète.

#### Enclave sécurisée

The **[Secure Enclave](https://support.apple.com/guide/security/secure-enclave-sec59b0b31ff/web)** is a security chip built into devices with Apple Silicon which is responsible for storing and generating encryption keys for data at rest as well as Face ID and Touch ID data. It contains its own [separate boot ROM](https://support.apple.com/en-vn/guide/security/sec59b0b31ff/web#sec43006c49f).

Vous pouvez considérer l'Enclave sécurisée comme le centre de sécurité de votre appareil : elle dispose d'un moteur de chiffrement AES et d'un mécanisme pour stocker en toute sécurité vos clés de chiffrement, et elle est séparée du reste du système, de sorte que même si le processeur principal est compromis, elle devrait rester sûre.

#### Touch ID

La fonction Touch ID d'Apple vous permet de déverrouiller vos appareils en toute sécurité à l'aide de la biométrie.

Your biometric data [never leaves your device](https://www.apple.com/legal/privacy/data/en/touch-id/#:~:text=Touch%C2%A0ID%20data%20does%20not%20leave%20your%20device%2C%20and%20is%20never%20backed%20up%20to%20iCloud%20or%20anywhere%20else.); it's stored only in the Secure Enclave.

#### Déconnexion matérielle du microphone

All laptops with Apple Silicon or the T2 chip feature a [hardware disconnect](https://support.apple.com/guide/security/hardware-microphone-disconnect-secbbd20b00b/web) for the built-in microphone whenever the lid is closed. Cela signifie qu'il n'y a aucun moyen pour un attaquant d'écouter le microphone de votre Mac, même si le système d'exploitation est compromis.

Notez que la caméra n'a pas de déconnexion matérielle, puisque sa vue est de toute façon obscurcie lorsque le couvercle est fermé.

#### Secure Camera Indicator

The built-in camera in a Mac is designed so that the camera can't turn on without the camera indicator light [also turning on](https://support.apple.com/en-us/102177#:~:text=The%20camera%20is%20engineered%20so%20that%20it%20can’t%20activate%20without%20the%20camera%20indicator%20light%20also%20turning%20on.%20This%20is%20how%20you%20can%20tell%20if%20your%20camera%20is%20on.).

#### Sécurité des processeurs périphériques

Computers have [built-in processors](https://support.apple.com/en-vn/guide/security/seca500d4f2b/1/web/1) other than the main CPU that handle things like networking, graphics, power management, etc. Ces processeurs peuvent avoir une sécurité insuffisante et être compromis, c'est pourquoi Apple essaie de minimiser la nécessité de ces processeurs dans son matériel.

Lorsqu'il est nécessaire d'utiliser l'un de ces processeurs, Apple travaille avec le fournisseur pour s'assurer que le processeur

- exécute le micrologiciel vérifié du processeur principal au démarrage
- possède sa propre chaîne de démarrage sécurisé
- respecte des normes cryptographiques minimales
- garantit que les microprogrammes connus comme étant défectueux sont révoqués de manière appropriée
- a ses interfaces de débogage désactivées
- est signé avec les clés cryptographiques d'Apple

#### Protections contre l'accès direct à la mémoire

Apple Silicon separates each component that requires [direct memory access](https://support.apple.com/guide/security/direct-memory-access-protections-seca4960c2b5/1/web/1). Par exemple, un port Thunderbolt ne peut pas accéder à la mémoire réservée au noyau.

#### Terminal Secure Keyboard Entry

Enable [Secure Keyboard Entry](https://support.apple.com/guide/terminal/use-secure-keyboard-entry-trml109/mac) to prevent other apps from detecting what you type in the terminal.
