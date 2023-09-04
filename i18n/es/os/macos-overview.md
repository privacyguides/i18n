---
title: Vista general de macOS
icon: material/apple-finder
description: macOS es el sistema operativo de escritorio de Apple que trabaja con su hardware para ofrecer una seguridad sólida.
---

**macOS** es un sistema operativo Unix desarrollado por Apple para sus ordenadores Mac. Para mejorar la privacidad en macOS, puedes desactivar las funciones de telemetría y reforzar los ajustes de privacidad y seguridad existentes.

Los Mac basados en Intel más antiguos y los Hackintosh no son compatibles con todas las funciones de seguridad que ofrece macOS. Para mejorar la seguridad de los datos, recomendamos utilizar un Mac más reciente con [Apple Silicon](https://support.apple.com/en-us/HT211814).

## Notas de Privacidad

Hay algunos problemas de privacidad importantes con macOS que deberías tener en cuenta. Estos conciernen al propio sistema operativo y no a otras aplicaciones y servicios de Apple.

### Bloqueo de Activación

Los nuevos dispositivos de Apple Silicon pueden configurarse sin una conexión a Internet. Sin embargo, recuperar o restablecer tu Mac **requerirá ** una conexión a Internet a los servidores de Apple para comprobar la base de datos del Bloqueo de Activación de dispositivos perdidos o robados.

### Comprobaciones de Revocación de Aplicaciones

macOS realiza comprobaciones en línea al abrir una aplicación para verificar si contiene malware conocido y si el certificado de firma del desarrollador es revocado.

Anteriormente, estas comprobaciones se realizaban a través de un protocolo OCSP no cifrado que podía filtrar información sobre las aplicaciones que ejecutaba en tu red. Apple actualizó su servicio OCSP para utilizar el cifrado HTTPS en 2021, y [publicó información](https://support.apple.com/HT202491) sobre su política de registro para este servicio. Además, prometieron añadir un mecanismo para que las personas pudieran optar por no participar en esta comprobación en línea, pero esto no se ha añadido a macOS todavía (julio de 2023).

Aunque [puedes](https://eclecticlight.co/2021/02/23/how-to-run-apps-in-private/) excluirte manualmente de esta comprobación con relativa facilidad, recomendamos no hacerlo a menos que las comprobaciones de revocación realizadas por macOS te pongan en grave peligro, ya que desempeñan un papel importante a la hora de garantizar que se bloquea la ejecución de aplicaciones comprometidas.

## Configuración Recomendada

Tu cuenta cuando configures por primera vez tu Mac será una cuenta de Administrador, que tiene mayores privilegios que una cuenta de usuario Estándar. macOS cuenta con una serie de protecciones que evitan que el malware y otros programas abusen de tus privilegios de Administrador, por lo que generalmente es seguro utilizar esta cuenta.

Sin embargo, en utilidades de protección como `sudo`, [en el pasado](https://bogner.sh/2014/03/another-mac-os-x-sudo-password-bypass/), se han descubierto exploits. Si quieres evitar la posibilidad de que los programas que ejecutas abusen de tus privilegios de Administrador, puedes plantearte crear una segunda cuenta de usuario Estándar que utilices para las operaciones diarias. Esto tiene la ventaja añadida de hacer más obvio cuándo una aplicación necesita acceso de administrador, porque te pedirá las credenciales cada vez.

Si utilizas una segunda cuenta, no es estrictamente necesario que inicies sesión en tu cuenta de Administrador original desde la pantalla de inicio de sesión de macOS. Cuando estés haciendo algo como usuario Estándar que requiera permisos de Administrador, el sistema debería pedirte autenticación, donde puedes introducir tus credenciales de Administrador como usuario Estándar una sola vez. Apple proporciona [orientación](https://support.apple.com/HT203998) sobre cómo ocultar tu cuenta de Administrador si prefieres ver sólo una cuenta en tu pantalla de inicio de sesión.

Alternativamente, puedes utilizar una utilidad como [macOS Enterprise Privileges](https://github.com/SAP/macOS-enterprise-privileges) para escalar a derechos de Administrador bajo demanda, pero esto puede ser vulnerable a algún exploit no descubierto, como todas las protecciones basadas en software.

### iCloud

The majority of privacy and security concerns with Apple products are related to their *cloud services*, not their hardware or software. When you use Apple services like iCloud, most of your information is stored on their servers and secured with keys *which Apple has access to* by default. This level of access has occasionally been abused by law enforcement to get around the fact that your data is otherwise securely encrypted on your device, and of course Apple is vulnerable to data breaches like any other company.

Therefore, if you use iCloud you should [enable **Advanced Data Protection**](https://support.apple.com/HT212520). This encrypts nearly all of your iCloud data with keys stored on your devices (end-to-end encryption), rather than Apple's servers, so that your iCloud data is secured in the event of a data breach, and otherwise hidden from Apple.

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

#### Privacidad & Seguridad

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

##### Seguridad

Apps from the App Store are subject to stricter security guidelines, such as stricter sandboxing. If the only apps you need are available from the App Store, change the **Allow applications downloaded from** setting to **App Store** to prevent accidentally running other apps. This is a good option particularly if you are configuring a machine for other, less technical users such as children.

If you choose to also allow applications from identified developers, be careful about the apps you run and where you obtain them.

##### FileVault

On modern devices with a Secure Enclave (Apple T2 Security Chip, Apple silicon), your data is always encrypted, but is decrypted automatically by a hardware key if your device doesn't detect it's been tampered with. Enabling FileVault additionally requires your password to decrypt your data, greatly improving security, especially when powered off or before the first login after powering on.

On older Intel-based Mac computers, FileVault is the only form of disk encryption available by default, and should always be enabled.

- [x] Click **Turn On**

##### Lockdown Mode

[Lockdown Mode](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode) disables some features in order to improve security. Some apps or features won't work the same way they do when it's off, for example, [JIT](https://hacks.mozilla.org/2017/02/a-crash-course-in-just-in-time-jit-compilers/) and [WASM](https://developer.mozilla.org/en-US/docs/WebAssembly) are disabled in Safari with Lockdown Mode enabled. We recommend enabling Lockdown Mode and seeing whether it significantly impacts your usage, many of the changes it makes are easy to live with.

- [x] Click **Turn On**

### Aleatorización de direcciones Mac

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

!!! warning "Advertencia"

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

!!! warning "Advertencia"

    Software downloaded from outside the official App Store is not required to be sandboxed. You should avoid non-App Store software as much as possible.

##### Antivirus

macOS comes with two forms of malware defense:

1. Protection against launching malware in the first place is provided by the App Store's review process for App Store applications, or *Notarization* (part of *Gatekeeper*), a process where third-party apps are scanned for known malware by Apple before they are allowed to run.
2. Protection against other malware and remediation from existing malware on your system is provided by *XProtect*, a more traditional antivirus software built-in to macOS.

We recommend against installing third-party antivirus software as they typically do not have the system-level access required to properly function anyways, because of Apple's limitations on third-party apps, and because granting the high levels of access they do ask for often poses an even greater security and privacy risk to your computer.

##### Copias de seguridad

macOS comes with automatic backup software called [Time Machine](https://support.apple.com/HT201250), so you can create encrypted backups to an external or network drive in the event of corrupted/deleted files.

### Hardware Security

Many modern security features in macOS—such as modern Secure Boot, hardware-level exploit mitigation, OS integrity checks, and file-based encryption—rely on Apple silicon, and Apple's newer hardware always has the [best security](https://support.apple.com/guide/security/apple-soc-security-sec87716a080/1/web/1). We only encourage the use of Apple silicon, and not older Intel-based Mac computers or Hackintoshes.

Some of these modern security features are available on older Intel-based Mac computers with the Apple T2 Security Chip, but that chip is susceptible to the *checkm8* exploit which could compromise its security.

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

## Fuentes

- [Apple Platform Security](https://support.apple.com/guide/security/welcome/web)
