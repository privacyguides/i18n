---
title: Resumen de macOS
icon: material/apple-finder
description: macOS es el sistema operativo de escritorio de Apple que trabaja con su hardware para ofrecer una seguridad sólida.
---

**macOS** es un sistema operativo Unix desarrollado por Apple para sus ordenadores Mac. Para mejorar la privacidad en macOS, puedes desactivar las funciones de telemetría y reforzar los ajustes de privacidad y seguridad existentes.

Los Mac basados en Intel más antiguos y los Hackintosh no son compatibles con todas las funciones de seguridad que ofrece macOS. Para mejorar la seguridad de los datos, recomendamos utilizar un Mac más reciente con [Apple Silicon](https://support.apple.com/HT211814).

## Notas de Privacidad

Hay algunos problemas de privacidad importantes con macOS que deberías tener en cuenta. Estos conciernen al propio sistema operativo y no a otras aplicaciones y servicios de Apple.

### Bloqueo de Activación

Los nuevos dispositivos Apple Silicon pueden configurarse sin una conexión a Internet. Sin embargo, recuperar o restablecer tu Mac **requerirá ** una conexión a Internet a los servidores de Apple para comprobar la base de datos del Bloqueo de Activación de dispositivos perdidos o robados.

### Comprobaciones de Revocación de Aplicaciones

macOS realiza comprobaciones en línea al abrir una aplicación para verificar si contiene malware conocido y si el certificado de firma del desarrollador es revocado.

El servicio OCSP de Apple utiliza cifrado HTTPS, por lo que solo ellos pueden ver qué aplicaciones abres. Han [publicado información](https://support.apple.com/HT202491) sobre su política de registro para este servicio. Además, [prometieron](http://lapcatsoftware.com/articles/2024/8/3.html) añadir un mecanismo para que la gente pudiera optar por no participar en esta comprobación en línea, pero esto no se ha añadido a macOS.

Aunque [puedes](https://eclecticlight.co/2021/02/23/how-to-run-apps-in-private) excluirte manualmente de esta comprobación con relativa facilidad, recomendamos no hacerlo a menos que las comprobaciones de revocación realizadas por macOS te pongan en grave peligro, ya que desempeñan un papel importante a la hora de garantizar que se bloquee la ejecución de aplicaciones comprometidas.

## Configuración Recomendada

Tu cuenta cuando configures por primera vez tu Mac será una cuenta de Administrador, que tiene mayores privilegios que una cuenta de usuario Estándar. macOS cuenta con una serie de protecciones que evitan que el malware y otros programas abusen de tus privilegios de Administrador, por lo que generalmente es seguro utilizar esta cuenta.

Sin embargo, en utilidades de protección como `sudo`, [en el pasado](https://bogner.sh/2014/03/another-mac-os-x-sudo-password-bypass), se han descubierto exploits. Si quieres evitar la posibilidad de que los programas que ejecutas abusen de tus privilegios de Administrador, puedes plantearte crear una segunda cuenta de usuario Estándar que utilices para las operaciones diarias. Esto tiene la ventaja añadida de hacer más obvio cuándo una aplicación necesita acceso de administrador, porque te pedirá las credenciales cada vez.

Si utilizas una segunda cuenta, no es estrictamente necesario que inicies sesión en tu cuenta de Administrador original desde la pantalla de inicio de sesión de macOS. Cuando estés haciendo algo como usuario Estándar que requiera permisos de Administrador, el sistema debería pedirte autenticación, donde puedes introducir tus credenciales de Administrador como usuario Estándar una sola vez. Apple proporciona [orientación](https://support.apple.com/HT203998) sobre cómo ocultar tu cuenta de Administrador si prefieres ver sólo una cuenta en tu pantalla de inicio de sesión.

### iCloud

Cuando utilizas servicios de Apple como iCloud, la mayor parte de tu información se almacena en sus servidores y se protege con claves *a las que Apple tiene acceso* por defecto. Apple lo denomina [Protección de Datos Estándar](https://support.apple.com/en-us/102651).

Por lo tanto, si utilizas iCloud, deberías activar la [ **Protección de Datos Avanzada**](https://support.apple.com/HT212520). Esto encripta casi todos tus datos de iCloud con claves almacenadas en tus dispositivos (encriptación de extremo a extremo), en lugar de en los servidores de Apple, de modo que tus datos de iCloud están protegidos en caso de violación de datos y, por lo demás, ocultos a Apple.

Si quieres poder instalar aplicaciones desde el App Store pero no quieres activar iCloud, puedes iniciar sesión en tu cuenta de Apple desde el App Store en lugar de desde **Ajustes del Sistema**.

### Ajustes del Sistema

Hay una serie de configuraciones integradas que deberías confirmar o cambiar para reforzar tu sistema. Abre la aplicación **Ajustes**:

#### Bluetooth

- [ ] Turn off **Bluetooth** (unless you are currently using it)

#### Red

Dependiendo de si estás utilizando **Wi-Fi** o **Ethernet** (indicado con un punto verde y la palabra "conectado"), haz clic en el icono correspondiente.

Haz clic en el botón "Detalles" junto al nombre de tu red:

- [x] Selecciona **Rotatoria** en **Dirección Wi-Fi privada**

- [x] Turn on **Limit IP address tracking**

##### Firewall

Tu cortafuegos bloquea conexiones de red no deseadas. Cuanto más estricta sea la configuración de tu cortafuegos, más seguro estará su Mac. Sin embargo, algunos servicios estarán bloqueados. Debes configurar tu cortafuegos para que sea lo más estricto posible sin bloquear los servicios que utilizas.

- [x] Turn on **Firewall**

Haz clic en el botón **Opciones**:

- [x] Turn on **Block all incoming connections**

Si esta configuración es demasiado estricta, puedes volver y desmarcarla. Sin embargo, macOS normalmente te pedirá que permitas conexiones entrantes para una aplicación si la aplicación lo solicita.

#### General

Por defecto, el nombre de tu dispositivo será algo así como "iMac de [tu nombre]". Because this name is [publicly broadcast on your network](https://support.apple.com/guide/mac-help/change-computers-local-hostname-mac-mchlp2322/26/mac/26#:~:text=The%20local%20hostname%2C%20or%20local%20network%20name%2C%20is%20displayed%20at%20the%20bottom%20of%20the%20Sharing%20settings%20window.%20It%20identifies%20your%20Mac%20to%20Bonjour%2Dcompatible%20services.), you'll want to change your device name to something generic like "Mac".

Haz clic en **Acerca de** y escribe el nombre del dispositivo que desees en el campo **Nombre**.

##### Actualizaciones de Software

Deberías instalar automáticamente todas las actualizaciones disponibles para asegurarte de que tu Mac cuenta con las últimas correcciones de seguridad.

Haz clic en el pequeño :material-information-outline: icono situado junto a **Actualizaciones Automáticas**:

- [x] Turn on **Download new updates when available**

- [x] Turn on **Install macOS updates**

- [x] Turn on **Install Security Responses and system files**

#### Apple Intelligence & Siri

If you do not use these features on macOS, you should disable them:

- [ ] Turn off **Apple Intelligence**
- [ ] Desactiva **Siri**

**[Apple Intelligence](https://apple.com/legal/privacy/data/en/intelligence-engine)** is only available if your device supports it. Apple Intelligence uses a combination of on-device processing and their [Private Cloud Compute](https://security.apple.com/blog/private-cloud-compute) for things that take more processing power than your device can provide.

To see a report of all the data sent via Apple Intelligence, you can navigate to **Privacy & Security** → **Apple Intelligence Report** and press **Export Activity** to see activity from the either the last 15 minutes or 7 days, depending on what you set it for. Similar to the **App Privacy Report** which shows you the recent permissions accessed by the apps on your phone, the Apple Intelligence Report likewise shows what is being sent to Apple's servers while using Apple Intelligence.

By default, ChatGPT integration is disabled. If you don't want ChatGPT integration anymore, you can navigate to **ChatGPT**:

- [ ] Turn off **Use ChatGPT**

You can also have it ask for confirmation every time if you leave ChatGPT integration on:

- [x] Turn on **Confirm Requests**

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

Any request made with ChatGPT will be sent to ChatGPT's servers, there is no on-device processing and no PCC like with Apple Intelligence.

</div>

#### Privacidad y Seguridad

Siempre que una aplicación solicite un permiso, aparecerá aquí. Puedes decidir a qué aplicaciones deseas permitir o denegar permisos específicos.

##### Servicios de Localización

Puedes permitir individualmente los servicios de localización por aplicación. Si no necesitas que las aplicaciones utilicen tu ubicación, desactivar por completo los servicios de localización es la opción más privada.

- [ ] Desactiva **Localización**

##### Análisis y Mejoras

Decide whether you want to share analytics data with Apple and app developers.

##### Publicidad de Apple

Decide si quieres anuncios personalizados en función de tu uso.

- [ ] Desactiva **Anuncios Personalizados**

##### FileVault

En los dispositivos modernos con Secure Enclave (Apple T2 Security Chip, Apple Silicon), tus datos siempre están cifrados, pero se descifran automáticamente mediante una llave de hardware si el dispositivo no detecta que ha sido manipulado. Activar [FileVault](../encryption.md#filevault) requiere además tu contraseña para descifrar tus datos, lo que mejora enormemente la seguridad, especialmente cuando está apagado o antes del primer inicio de sesión después de encenderlo.

En los ordenadores Mac basados en Intel más antiguos, FileVault es la única forma de cifrado de disco disponible por defecto, y debería estar siempre activada.

- [x] Seleccione **Encender**

##### Modo hermético

**[Lockdown Mode](https://support.apple.com/guide/mac-help/lock-mac-targeted-a-cyberattack-ibrw66f4e191/mac)** disables some features in order to improve security. Some apps or features won't work the same way they do when it's off. For example, Javascript Just-In-Time ([JIT](https://hacks.mozilla.org/2017/02/a-crash-course-in-just-in-time-jit-compilers)) compilation and [WebAssembly](https://developer.mozilla.org/docs/WebAssembly) are disabled in Safari with Lockdown Mode enabled. We recommend enabling Lockdown Mode and seeing whether it significantly impacts daily usage.

- [x] Seleccione **Encender**

### Aleatorización de direcciones Mac

macOS uses a randomized MAC address when [performing Wi-Fi scans](https://support.apple.com/guide/security/privacy-features-connecting-wireless-networks-secb9cb3140c/web) while disconnected from a network.

You can set your [MAC address to be randomized](https://support.apple.com/en-us/102509) per network and rotate occasionally to prevent tracking between networks and on the same network over time.

Ve a **Ajustes del Sistema** → **Red** → **Wi-Fi** → **Detalles** y establece **Dirección Wi-Fi privada** en **Fija** si quieres una dirección fija pero única para la red a la que estás conectado, o en **Rotatoria** si quieres que cambie con el tiempo.

Considera también la posibilidad de cambiar tu nombre de host, que es otro identificador de dispositivo que se difunde en la red a la que estás conectado. Es posible que desees establecer tu nombre de host en algo genérico como "MacBook Air", "Laptop", "MacBook Pro de John", o "iPhone" en **Ajustes del Sistema**→ **General**→ **Compartir**.

## Protecciones de seguridad

macOS utiliza la defensa en profundidad, confiando en múltiples capas de protección basadas en software y hardware, con diferentes propiedades. Esto garantiza que un fallo en una capa no compromete la seguridad general del sistema.

### Seguridad del software

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

macOS permite instalar actualizaciones de prueba. These are unstable and may come with [extra telemetry](https://beta.apple.com/privacy) since they're for testing purposes. Debido a esto, recomendamos evitar las actualizaciones de prueba del software en general.

</div>

#### Volumen firmado del sistema

macOS's system components are protected in a read-only [signed system volume](https://support.apple.com/guide/security/signed-system-volume-security-secd698747c9/web), meaning that neither you nor malware can alter important system files.

El volumen del sistema es verificado mientras se encuentra en ejecución y cualquier dato que no se encuentra firmado con una firma criptográfica válida de Apple será rechazado.

#### Protección de la integridad del sistema

macOS establece ciertas restricciones de seguridad que no pueden ser anuladas. These are called [Mandatory Access Controls](https://support.apple.com/guide/security/system-integrity-protection-secb7ea06b49/1/web/1), and they form the basis of the sandbox, parental controls, and [System Integrity Protection](https://support.apple.com/en-us/102149) on macOS.

La Protección de la integridad del sistema hace que las ubicaciones de los archivos críticos sean de solo lectura, para protegerlas contra la modificación de código malicioso. Esto se suma a la Protección de integridad del núcleo basada en hardware, que protege al kernel ante las modificaciones en memoria.

#### Seguridad de las aplicaciones

##### Sandbox de aplicaciones

En macOS, el desarrollador determina si una aplicación está aislada cuando la firma. The [App Sandbox](https://developer.apple.com/documentation/xcode/configuring-the-macos-app-sandbox) protects against vulnerabilities in the apps you run by limiting what a malicious actor can access in the event that the app is exploited. El App Sandbox *por sí solo* no puede proteger contra [:material-package-variant-closed-remove: Ataques a la Cadena de Suministro](../basics/common-threats.md#attacks-against-certain-organizations ""){.pg-viridian} por parte de desarrolladores maliciosos. For that, sandboxing needs to be enforced by someone other than the developer themselves, as it is on the [App Store](https://support.apple.com/guide/security/gatekeeper-and-runtime-protection-sec5599b66df/1/web/1#:~:text=All%20apps%20from%20the%20App%20Store%20are%20sandboxed%20to%20restrict%20access%20to%20data%20stored%20by%20other%20apps.).

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

El software descargado desde fuera de la App Store oficial no necesita ser virtualizado. Si tu modelo de amenazas prioriza la defensa contra [:material-bug-outline: Ataques Pasivos](../basics/common-threats.md#security-and-privacy){ .pg-orange }, entonces es posible que quieras comprobar si el software que descargas fuera de la App Store está protegido por un sandbox, que depende del desarrollador para *optar por él*.

</div>

Puedes comprobar si una aplicación utiliza App Sandbox de varias maneras:

Puedes comprobar si las aplicaciones que ya se están ejecutando están aisladas mediante el [Monitor de Actividad](https://developer.apple.com/documentation/security/protecting-user-data-with-app-sandbox#Verify-that-your-app-uses-App-Sandbox).

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

Que uno de los procesos de una aplicación esté aislado no significa que todos lo estén.

</div>

También puedes comprobar las aplicaciones antes de ejecutarlas ejecutando este comando en el terminal:

``` zsh
codesign -dvvv --entitlements - <path to your app>
```

Si una aplicación está aislada, deberías ver el siguiente resultado:

``` zsh
    [Key] com.apple.security.app-sandbox
    [Value]
        [Bool] true
```

Si descubres que la aplicación que deseas ejecutar no está aislada, puedes emplear métodos de [compartimentación](../basics/common-threats.md#security-and-privacy) como máquinas virtuales o dispositivos separados, utilizar una aplicación similar que sí esté aislada o decidir no utilizar la aplicación no aislada.

##### Hardened Runtime

El [Hardened Runtime](https://developer.apple.com/documentation/security/hardened_runtime) es una forma extra de protección para apps que previene ciertas clases de exploits. Mejora la seguridad de las aplicaciones contra la explotación deshabilitando ciertas características como JIT.

Puede comprobar si una aplicación utiliza el Hardened Runtime mediante este comando:

``` zsh
codesign -dv <path to your app>
```

Si el Hardened Runtime está activado, verás `flags=0x10000(runtime)`. La salida `runtime` significa que Hardened Runtime está activado. Puede haber otras señales, pero la señal de runtime es la que buscamos aquí.

Puedes activar una columna en el Monitor de Actividad llamada «Restringido», que es una marca que impide que los programas inyecten código a través del [dynamic linker](https://pewpewthespells.com/blog/blocking_code_injection_on_ios_and_os_x.html) de macOS. Lo ideal sería que dijera "Sí".

##### Antivirus

macOS comes with two forms of [malware defense](https://support.apple.com/guide/security/protecting-against-malware-sec469d47bd8/1/web/1):

1. La protección ante la ejecución del malware es proporcionada por el proceso de revisión de aplicaciones de la App Store, o la *Notarización* (parte de *Gatekeeper*), proceso donde las aplicaciones de terceros son escaneadas por Apple para buscar algún malware conocido, antes de que se le permita ser ejecutada. Las aplicaciones deben ser firmadas por los desarrolladores con una clave que les da Apple. Esto asegura que estás ejecutando software de los desarrolladores reales. La notarización también requiere que los desarrolladores habiliten el Hardened Runtime para sus aplicaciones, lo que limita los métodos de explotación.
2. La protección contra otros malware y la remediación contra malware existente en el sistema, es proporcionada por *XProtect*, un antivirus tradicional incluido en macOS.

Desaconsejamos la instalación de antivirus de terceros, ya que no suelen tener el acceso a nivel de sistema necesario para funcionar correctamente, debido a las limitaciones de Apple a las aplicaciones de terceros, y porque conceder los altos niveles de acceso que solicitan suele suponer un riesgo aún mayor para la seguridad y la privacidad de tu ordenador.

##### Copias de seguridad

macOS comes with automatic backup software called [Time Machine](https://support.apple.com/HT201250), so you can create [encrypted backups](https://support.apple.com/guide/mac-help/keep-your-time-machine-backup-disk-secure-mh21241/mac) to an external drive or a network drive in the event of corrupted/deleted files.

### Seguridad del hardware

Muchas de las funciones modernas de seguridad de macOS, como el moderno Arranque Seguro, la mitigación de exploits a nivel de hardware, las verificaciones de integridad del sistema operativo y la encriptación basada en archivos, se basan en Apple Silicon, y el hardware más reciente de Apple siempre ofrece la [mejor seguridad](https://support.apple.com/guide/security/apple-soc-security-sec87716a080/1/web/1). Solo recomendamos el uso de Apple Silicon y no de ordenadores antiguos basados en Intel o Hackintosh.

Algunas de estas funciones modernas de seguridad están disponibles en las viejas computadoras Mac basadas en Intel, con el chip de seguridad Apple T2, pero este chip es susceptible a la vulnerabilidad de *checkm8*, que puede comprometer la seguridad.

If you use Bluetooth accessories such as a keyboard, we recommend that you use official Apple ones as their firmware will [automatically be updated](https://support.apple.com/en-us/120303#:~:text=Firmware%20updates%20are%20automatically%20delivered%20in%20the%20background%20while%20the%20Magic%20Keyboard%20is%20actively%20paired%20to%20a%20device%20running%20macOS%2C%20iOS%2C%20iPadOS%2C%20or%20tvOS.) for you by macOS. Utilizar accesorios de terceros está bien, pero debes recordar instalar las actualizaciones del firmware regularmente.

Apple's SoCs focus on [minimizing attack surface](https://support.apple.com/en-vn/guide/security/secf020d1074/web#:~:text=Security%2Dfocused%20hardware%20follows%20the%20principle%20of%20supporting%20limited%20and%20discretely%20defined%20functions%20to%20minimize%20attack%20surface.) by relegating security functions to dedicated hardware with limited functionality.

#### ROM de arranque

macOS prevents malware persistence by only allowing official Apple software to run at boot time; this is known as [secure boot](https://support.apple.com/en-vn/guide/security/secac71d5623/1/web/1). Mac computers verify this with a bit of read-only memory on the SoC called the [boot ROM](https://support.apple.com/en-vn/guide/security/aside/sec5240db956/1/web/1), which is [laid down during the manufacturing of the chip](https://support.apple.com/en-vn/guide/security/secf020d1074/1/web/1#:~:text=which%20is%20laid%20down%20during%20Apple%20SoC%20fabrication).

La ROM de arranque conforma la raíz de confianza del hardware. This ensures that malware cannot tamper with the boot process, since the boot ROM is immutable. Cuando tu Mac inicia, la ROM de arranque es lo primero que se ejecuta, conformando el primer eslabón en la cadena de confianza.

Mac computers can be configured to boot in [three security modes](https://support.apple.com/guide/deployment/startup-security-dep5810e849c/web#dep32fb404e1): *Full Security*, *Reduced Security*, and *Permissive Security*, with the default setting being Full Security. You should ideally be using Full Security mode and avoid things like **[kernel extensions](https://support.apple.com/guide/deployment/system-extensions-in-macos-depa5fb8376f/web#dep51e097f45)** that force you to lower your security mode. Debes asegurarte de [comprobar](https://support.apple.com/guide/mac-help/change-security-settings-startup-disk-a-mac-mchl768f7291/mac) que estés utilizando el modo de Seguridad completa.

#### Secure Enclave

The **[Secure Enclave](https://support.apple.com/guide/security/secure-enclave-sec59b0b31ff/web)** is a security chip built into devices with Apple Silicon which is responsible for storing and generating encryption keys for data at rest as well as Face ID and Touch ID data. It contains its own [separate boot ROM](https://support.apple.com/en-vn/guide/security/sec59b0b31ff/web#sec43006c49f).

Puedes pensar en el enclave seguro como el centro de seguridad de tu dispositivo: este tiene un motor de cifrado AES y un mecanismo para almacenar de manera segura tus claves de cifrado, y se encuentra separado del resto del sistema, por lo que, si el procesador principal se encuentra comprometido, este debe estar seguro.

#### Touch ID

La característica de Touch ID de Apple permite desbloquear de una manera segura tus dispositivos utilizando la biometría.

Your biometric data [never leaves your device](https://www.apple.com/legal/privacy/data/en/touch-id/#:~:text=Touch%C2%A0ID%20data%20does%20not%20leave%20your%20device%2C%20and%20is%20never%20backed%20up%20to%20iCloud%20or%20anywhere%20else.); it's stored only in the Secure Enclave.

#### Desconexión del micrófono por hardware

All laptops with Apple Silicon or the T2 chip feature a [hardware disconnect](https://support.apple.com/guide/security/hardware-microphone-disconnect-secbbd20b00b/web) for the built-in microphone whenever the lid is closed. Esto significa que no hay alguna manera para los atacantes de escuchar el micrófono de tu Mac, incluso cuando el sistema operativo está comprometido.

Tome en cuenta que la cámara no cuenta con una desconexión del hardware, porque su vista se encuentra oscurecida cuando la tapa se encuentra cerrada.

#### Secure Camera Indicator

The built-in camera in a Mac is designed so that the camera can't turn on without the camera indicator light [also turning on](https://support.apple.com/en-us/102177#:~:text=The%20camera%20is%20engineered%20so%20that%20it%20can’t%20activate%20without%20the%20camera%20indicator%20light%20also%20turning%20on.%20This%20is%20how%20you%20can%20tell%20if%20your%20camera%20is%20on.).

#### Seguridad del procesador periférico

Computers have [built-in processors](https://support.apple.com/en-vn/guide/security/seca500d4f2b/1/web/1) other than the main CPU that handle things like networking, graphics, power management, etc. Estos procesadores pueden tener una seguridad insuficiente y pueden verse comprometidos, por lo que Apple intenta minimizar la necesidad de estos procesadores en su hardware.

Cuando es necesario utilizar alguno de estos procesadores, Apple trabaja con el proveedor para garantizar que el procesador

- ejecute un firmware verificado desde la CPU primaria al iniciar
- tiene su propia cadena de Arranque seguro
- sigue los estándares criptográficos mínimos
- garantiza que el firmware defectuoso conocido es revocado correctamente
- tiene sus interfaces de depuración desactivadas
- está firmado con las claves criptográficas de Apple

#### Protecciones de Acceso Directo a la Memoria

Apple Silicon separates each component that requires [direct memory access](https://support.apple.com/guide/security/direct-memory-access-protections-seca4960c2b5/1/web/1). Por ejemplo, un puerto Thunderbolt no puede acceder a la memoria designada para el kernel.

#### Terminal Secure Keyboard Entry

Enable [Secure Keyboard Entry](https://support.apple.com/guide/terminal/use-secure-keyboard-entry-trml109/mac) to prevent other apps from detecting what you type in the terminal.
