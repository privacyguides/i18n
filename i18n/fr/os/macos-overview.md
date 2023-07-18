---
title: Introduction à macOS
icon: material/apple-finder
description: macOS est le système d'exploitation d'Apple pour ordinateurs de bureau fonctionnant avec leur propre matériel pour assurer une sécurité renforcée.
---

**macOS** est un système d'exploitation Unix développé par Apple pour leurs ordinateurs Mac. Pour améliorer la confidentialité de macOS, il est possible de désactiver la télémétrie et renforcer les paramètres existants de confidentialité et de sécurité.

Les anciens Mac à base de processeur Intel et les Hackintosh ne prennent pas en charge toutes les fonctions de sécurité offertes par macOS. Pour améliorer la sécurité des données, nous recommandons d'utiliser un Mac plus récent avec un processeur [Apple Silicon](https://support.apple.com/fr-fr/HT211814).

## Remarques concernant la vie privée

macOS pose quelques problèmes importants en matière de protection de la vie privée, qu'il convient de prendre en compte. Ils concernent le système d'exploitation lui-même, et non les autres applications et services d'Apple.

### Verrouillage d'activation

Les nouveaux appareils Apple Silicon peuvent être configurés sans connexion internet. Cependant, la récupération ou la réinitialisation de votre Mac **nécessitera** une connexion internet aux serveurs d'Apple pour vérifier la base de données Verrouillage d'activation des appareils perdus ou volés.

### Contrôles de révocation des applications

macOS effectue des contrôles en ligne lorsque vous ouvrez une application afin de vérifier si elle contient des logiciels malveillants connus et si le certificat de signature du développeur a été révoqué.

Auparavant, ces vérifications étaient effectuées via un protocole OCSP non chiffré, ce qui pouvait entraîner une fuite d'informations sur les applications que vous exécutez sur votre réseau. Apple a mis à jour son service OCSP pour utiliser le chiffrement HTTPS en 2021, et [a publié des informations](https://support.apple.com/HT202491) sur sa politique de journalisation pour ce service. Ils ont également promis d'ajouter un mécanisme permettant aux personnes de se retirer de cette vérification en ligne, mais cela n'a pas été ajouté à macOS en date de juillet 2023.

Bien que vous [puissiez](https://eclecticlight.co/2021/02/23/how-to-run-apps-in-private/) désactiver manuellement cette vérification assez facilement, nous vous déconseillons de le faire à moins que les vérifications de révocation effectuées par macOS ne vous compromettent gravement, car elles jouent un rôle important en empêchant l'exécution d'applications compromises.

## Configuration recommandée

Lorsque vous configurez votre Mac pour la première fois, vous disposez d'un compte d'administrateur, dont les privilèges sont plus élevés que ceux d'un compte d'utilisateur standard. macOS dispose d'un certain nombre de protections qui empêchent les logiciels malveillants et d'autres programmes d'abuser de vos privilèges d'administrateur, de sorte que l'utilisation de ce compte est généralement sûre.

Cependant, des exploits dans des utilitaires de protection tels que `sudo` ont été [découverts dans le passé](https://bogner.sh/2014/03/another-mac-os-x-sudo-password-bypass/). Si vous souhaitez éviter que les programmes que vous exécutez n'abusent de vos privilèges d'administrateur, vous pouvez envisager de créer un deuxième compte d'utilisateur standard, que vous utiliserez pour les opérations quotidiennes. Cela présente l'avantage supplémentaire de rendre plus évident le fait qu'une application a besoin d'un accès administrateur, parce qu'elle vous demandera à chaque fois de fournir des informations d'identification.

Si vous utilisez un deuxième compte, il n'est pas strictement nécessaire de vous connecter à votre compte administrateur d'origine à partir de l'écran de connexion de macOS. Lorsque vous effectuez, en tant qu'utilisateur standard, une opération nécessitant des autorisations d'administrateur, le système vous invite à vous authentifier, ce qui vous permet d'entrer une seule fois vos informations d'identification d'administrateur en tant qu'utilisateur standard. Apple fournit des [conseils](https://support.apple.com/HT203998) sur la façon de masquer votre compte administrateur si vous préférez ne voir qu'un seul compte sur votre écran de connexion.

Vous pouvez également utiliser un utilitaire tel que [macOS Enterprise Privileges](https://github.com/SAP/macOS-enterprise-privileges) pour obtenir les droits d'administrateur à la demande, mais cette solution peut être vulnérable à un exploit non découvert, comme toutes les protections basées sur des logiciels.

### iCloud

La majorité des préoccupations relatives à la protection de la vie privée et à la sécurité des produits Apple sont liées à leurs *services cloud*, et non à leurs matériels ou à leurs logiciels. Lorsque vous utilisez des services Apple comme iCloud, la plupart de vos informations sont stockées sur leurs serveurs et sécurisées par des clés *auxquelles Apple a accès* par défaut. Ce niveau d'accès a parfois été utilisé de manière abusive par les forces de l'ordre pour contourner le fait que vos données sont par ailleurs chiffrées de manière sécurisée sur votre appareil, et bien sûr Apple est vulnérable aux fuites de données comme toute autre entreprise.

Par conséquent, si vous utilisez iCloud, vous devriez [activer la**Protection avancée des données**](https://support.apple.com/HT212520). Cela permet de chiffrer la quasi-totalité de vos données iCloud à l'aide de clés stockées sur vos appareils (chiffrement de bout en bout), plutôt que sur les serveurs d'Apple, de sorte que vos données iCloud sont sécurisées en cas de fuite de données, et qu'elles sont par ailleurs cachées à Apple.

### System Settings

There are a number of built-in settings you should confirm or change to harden your system. Open the **Settings** app:

#### Bluetooth

- [ ] Uncheck **Bluetooth** (unless you are currently using it)

#### Network

Depending on if you are using **Wi-Fi** or **Ethernet** (denoted by a green dot and the word "connected"), click on the corresponding icon.

Click on the "Details" button by your network name:

- [x] Check **Limit IP address tracking**

##### Firewall

Your firewall blocks unwanted network connections. The stricter your firewall settings are, the more secure your Mac is. However, certain services will be blocked. You should configure your firewall to be as strict as you can without blocking services you use.

- [x] Check **Firewall**

Click the **Options** button:

- [x] Check **Block all incoming connections**

If this configuration is too strict, you can come back and uncheck this. However, macOS will typically prompt you to allow incoming connections for an app if the app requests it.

#### General

By default, your device name will be something like "[your name]'s iMac". Because this name is publicly broadcast on your network, you'll want to change your device name to something generic like "Mac".

Click on **About** and type your desired device name into the **Name** field.

##### Software Updates

You should automatically install all available updates to make sure your Mac has the latest security fixes.

Click the small :material-information-outline: icon next to **Automatic Updates**:

- [x] Check **Check for updates**

- [x] Check **Download new updates when available**

- [x] Check **Install macOS updates**

- [x] Check **Install application updates from the App Store**

- [x] Check **Install Security Responses and system files**

#### Confidentialité & sécurité

Whenever an application requests a permission, it will show up here. You can decide which applications you want to allow or deny specific permissions.

##### Location Services

You can individually allow location services per-app. If you don't need apps to use your location, turning off location services entirely is the most private option.

- [ ] Uncheck **Location Services**

##### Analytics & Improvements

Decide whether you want to share analytics data with Apple and developers.

- [ ] Uncheck **Share Mac Analytics**

- [ ] Uncheck **Improve Siri & Dictation**

- [ ] Uncheck **Share with app developers**

- [ ] Uncheck **Share iCloud Analytics** (visible if you are signed in to iCloud)

##### Apple Advertising

Decide whether you want personalized ads based on your usage.

- [ ] Uncheck **Personalized Ads**

##### Sécurité

Apps from the App Store are subject to stricter security guidelines, such as stricter sandboxing. If the only apps you need are available from the App Store, change the **Allow applications downloaded from** setting to **App Store** to prevent accidentally running other apps. This is a good option particularly if you are configuring a machine for other, less technical users such as children.

If you choose to also allow applications from identified developers, be careful about the apps you run and where you obtain them.

##### FileVault

On modern devices with a Secure Enclave (Apple T2 Security Chip, Apple silicon), your data is always encrypted, but is decrypted automatically by a hardware key if your device doesn't detect it's been tampered with. Enabling FileVault additionally requires your password to decrypt your data, greatly improving security, especially when powered off or before the first login after powering on.

On older Intel-based Mac computers, FileVault is the only form of disk encryption available by default, and should always be enabled.

- [x] Click **Turn On**

##### Lockdown Mode

[Lockdown Mode](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode) disables some features in order to improve security. Some apps or features won't work the same way they do when it's off, for example, [JIT](https://hacks.mozilla.org/2017/02/a-crash-course-in-just-in-time-jit-compilers/) and [WASM](https://developer.mozilla.org/en-US/docs/WebAssembly) are disabled in Safari with Lockdown Mode enabled. We recommend enabling Lockdown Mode and seeing whether it significantly impacts your usage, many of the changes it makes are easy to live with.

- [x] Click **Turn On**

### Adresse MAC aléatoire

Unlike iOS, macOS doesn't give you an option to randomize your MAC address in the settings, so you'll need to do it with a command or a script.

You open up your Terminal and enter this command to randomize your MAC address:

``` zsh
openssl rand -hex 6 | sed 's/\(..\)/\1:/g; s/.$//' | xargs sudo ifconfig en1 ether 
```

en1 is the name of the interface you're changing the MAC address for. This might not be the right one on every Mac, so to check you can hold the option key and click the Wi-Fi symbol at the top right of your screen.

This will be reset on reboot.

## Security Protections

macOS employs defense in depth by relying on multiple layers of software and hardware-based protections, with different properties. This ensures that a failure in one layer does not compromise the system's overall security.

### Software Security

!!! warning "Avertissement"

    macOS allows you to install beta updates. These are unstable and may come with extra telemetry since they're for testing purposes. Because of this, we recommend you avoid beta software in general.

#### Signed System Volume

macOS's system components are protected in a read-only signed system volume, meaning that neither you nor malware can alter important system files.

The system volume is verified while it's running and any data that's not signed with a valid cryptographic signature from Apple will be rejected.

#### System Integrity Protection

macOS sets certain security restrictions that can't be overridden. These are called Mandatory Access Controls, and they form the basis of the sandbox, parental controls, and System Integrity Protection on macOS.

System Integrity Protection makes critical file locations read-only to protect against modification from malicious code. This is on top of the hardware-based Kernel Integrity Protection that keeps the kernel from being modified in-memory.

#### Application Security

##### App Sandbox

macOS apps downloaded from the App Store are required to be sandboxed usng the [App Sandbox](https://developer.apple.com/documentation/security/app_sandbox).

!!! warning "Avertissement"

    Software downloaded from outside the official App Store is not required to be sandboxed. You should avoid non-App Store software as much as possible.

##### Antivirus

macOS comes with two forms of malware defense:

1. Protection against launching malware in the first place is provided by the App Store's review process for App Store applications, or *Notarization* (part of *Gatekeeper*), a process where third-party apps are scanned for known malware by Apple before they are allowed to run.
2. Protection against other malware and remediation from existing malware on your system is provided by *XProtect*, a more traditional antivirus software built-in to macOS.

We recommend against installing third-party antivirus software as they typically do not have the system-level access required to properly function anyways, because of Apple's limitations on third-party apps, and because granting the high levels of access they do ask for often poses an even greater security and privacy risk to your computer.

##### Sauvegardes

macOS comes with automatic backup software called [Time Machine](https://support.apple.com/HT201250), so you can create encrypted backups to an external or network drive in the event of corrupted/deleted files.

### Hardware Security

Many modern security features in macOS—such as modern Secure Boot, hardware-level exploit mitigation, OS integrity checks, and file-based encryption—rely on Apple silicon, and Apple's newer hardware always has the [best security](https://support.apple.com/guide/security/apple-soc-security-sec87716a080/1/web/1). We only encourage the use of Apple silicon, and not older Intel-based Mac computers or Hackintoshes.

Some of these modern security features are available on older Intel-based Mac computers with the Apple T2 Security Chip, but that chip is susceptible to the *checkm8* exploit which could compromise its security,

If you use Bluetooth accessories such as a keyboard, we recommend that you use official Apple ones as their firmware will automatically be updated for you by macOS. Using third party accessories is fine, but you should remember to install firmware updates for them regularly.

Apple's SoCs focus on minimizing attack surface by relegating security functions to dedicated hardware with limited functionality.

#### Boot ROM

macOS prevents malware persistence by only allowing official Apple software to run at boot time; this is known as secure boot. Mac computers verify this with a bit of read-only memory on the SoC called the boot ROM, which is laid down during the manufacturing of the chip.

The boot ROM forms the hardware root of trust. This ensures that malware cannot tamper with the boot process. When your Mac boots up, the boot ROM is the first thing that runs, forming the first link in the chain of trust.

Mac computers can be configured to boot in three security modes: *Full Security*, *Reduced Security*, and *Permissive Security*, with the default setting being Full Security. You should ideally be using Full Security mode and avoid things like **kernel extensions** that force you to lower your security mode. Make sure to [check](https://support.apple.com/guide/mac-help/change-security-settings-startup-disk-a-mac-mchl768f7291/mac) that you're using Full Security mode.

#### Secure Enclave

The Secure Enclave is a security chip built into devices with Apple silicon which is responsible for storing and generating encryption keys for data at rest as well as Face ID and Touch ID data. It contains its own separate boot ROM.

You can think of the Secure Enclave as your device's security hub: it has an AES encryption engine and a mechanism to securely store your encryption keys, and it's separated from the rest of the system, so even if the main processor is compromised, it should still be safe.

#### Touch ID

Apple's Touch ID feature allows you to securely unlock your devices using biometrics.

Your biometric data never leaves your device; it's stored only in the Secure Enclave.

#### Hardware Microphone Disconnect

All laptops with Apple silicon or the T2 chip feature a hardware disconnect for the built-in microphone whenever the lid is closed. This means that there is no way for an attacker to listen to your Mac's microphone even if the operating system is compromised.

Note that the camera does not have a hardware disconnect, since its view is obscured when the lid is closed anyway.

#### Peripheral Processor Security

Computers have built-in processors other than the main CPU that handle things like networking, graphics, power management, etc. These processors can have insufficient security and become compromised, therefore Apple tries to minimize the need for these processors in their hardware.

When it is necessary to use one of these processors, Apple works with the vendor to ensure that the processor

- runs verified firmware from the primary CPU on startup
- has its own Secure Boot chain
- follows minimum cryptographic standards
- ensures known bad firmware is properly revoked
- has its debug interfaces disabled
- is signed with Apple's cryptographic keys

#### Direct Memory Access Protections

Apple silicon separates each component that requires direct memory access. For example, a Thunderbolt port can't access memory designated for the kernel.

## Sources

- [Apple Platform Security](https://support.apple.com/guide/security/welcome/web)
