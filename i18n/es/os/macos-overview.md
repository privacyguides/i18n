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

Los nuevos dispositivos de Apple Silicon pueden configurarse sin una conexión a Internet. Sin embargo, recuperar o restablecer tu Mac **requerirá ** una conexión a Internet a los servidores de Apple para comprobar la base de datos del Bloqueo de Activación de dispositivos perdidos o robados.

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

- [ ] Desmarca **Bluetooth** (a menos que lo estés utilizando actualmente)

#### Red

Dependiendo de si estás utilizando **Wi-Fi** o **Ethernet** (indicado con un punto verde y la palabra "conectado"), haz clic en el icono correspondiente.

Haz clic en el botón "Detalles" junto al nombre de tu red:

- [x] Select **Rotating** under **Private Wi-Fi address**

- [x] Check **Limit IP address tracking**

##### Firewall

Tu cortafuegos bloquea conexiones de red no deseadas. Cuanto más estricta sea la configuración de tu cortafuegos, más seguro estará su Mac. Sin embargo, algunos servicios estarán bloqueados. Debes configurar tu cortafuegos para que sea lo más estricto posible sin bloquear los servicios que utilizas.

- [x] Selecciona **Firewall**

Haz clic en el botón **Opciones**:

- [x] Selecciona **Bloquear todas las conexiones entrantes**

Si esta configuración es demasiado estricta, puedes volver y desmarcarla. Sin embargo, macOS normalmente te pedirá que permitas conexiones entrantes para una aplicación si la aplicación lo solicita.

#### General

Por defecto, el nombre de tu dispositivo será algo así como "iMac de [tu nombre]". Dado que este nombre se difunde públicamente en tu red, querrás cambiar el nombre de tu dispositivo por algo genérico como "Mac".

Haz clic en **Acerca de** y escribe el nombre del dispositivo que desees en el campo **Nombre**.

##### Actualizaciones de Software

Deberías instalar automáticamente todas las actualizaciones disponibles para asegurarte de que tu Mac cuenta con las últimas correcciones de seguridad.

Haz clic en el pequeño :material-information-outline: icono situado junto a **Actualizaciones Automáticas**:

- [x] Selecciona **Buscar actualizaciones**

- [x] Selecciona **Descargar las actualizaciones nuevas cuando estén disponibles**

- [x] Selecciona **Instalar actualizaciones de macOS**

- [x] Selecciona **Instalar actualizaciones de aplicaciones de App Store**

- [x] Selecciona **Instalar respuestas de seguridad y archivos del sistema**

#### Privacidad y Seguridad

Siempre que una aplicación solicite un permiso, aparecerá aquí. Puedes decidir a qué aplicaciones deseas permitir o denegar permisos específicos.

##### Servicios de Localización

Puedes permitir individualmente los servicios de localización por aplicación. Si no necesitas que las aplicaciones utilicen tu ubicación, desactivar por completo los servicios de localización es la opción más privada.

- [ ] Desactiva **Localización**

##### Análisis y Mejoras

Decide si quieres compartir datos analíticos con Apple y los desarrolladores.

- [ ] Desactiva **Compartir análisis del Mac**

- [ ] Desactiva **Mejorar Siri y Dictado**

- [ ] Desactiva **Compartir con los desarrolladores de las apps**

- [ ] Desactiva **Compartir Análisis (iCloud)** (visible si has iniciado sesión en iCloud)

##### Publicidad de Apple

Decide si quieres anuncios personalizados en función de tu uso.

- [ ] Desactiva **Anuncios Personalizados**

##### FileVault

En dispositivos modernos con un Secure Enclave (Chip de Seguridad T2 de Apple, Apple Silicon), tus datos siempre están cifrados, pero son descifrados automáticamente por una clave de hardware si tu dispositivo no detecta que ha sido manipulado. Activar FileVault requiere además tu contraseña para descifrar tus datos, lo que mejora enormemente la seguridad, especialmente cuando está apagado o antes del primer inicio de sesión después de encenderlo.

En los ordenadores Mac basados en Intel más antiguos, FileVault es la única forma de cifrado de disco disponible por defecto, y debería estar siempre activada.

- [x] Seleccione **Encender**

##### Modo hermético

El [modo hermético](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode) desactiva algunas características para mejorar la seguridad. Algunas aplicaciones o funciones no funcionarán igual que cuando está desactivado, por ejemplo, [JIT](https://hacks.mozilla.org/2017/02/a-crash-course-in-just-in-time-jit-compilers) y [WASM](https://developer.mozilla.org/docs/WebAssembly) están desactivados en Safari con el Modo de Aislamiento activado. Recomendamos activar el modo hermético y comprobar si este afecta significativamente su uso, porque muchos de los cambios que este hace son fáciles de manejar.

- [x] Seleccione **Encender**

### Aleatorización de direcciones Mac

macOS uses a randomized MAC address when performing Wi-Fi scans while disconnected from a network.

You can set your MAC address to be randomized per network and rotate occasionally to prevent tracking between networks and on the same network over time.

Go to **System Settings** → **Network** → **Wi-Fi** → **Details** and set **Private Wi-Fi address** to either **Fixed** if you want a fixed but unique address for the network you're connected to, or **Rotating** if you want it to change over time.

Consider changing your hostname as well, which is another device identifier that's broadcast on the network you're connected to. You may wish to set your hostname to something generic like "MacBook Air", "Laptop", "John's MacBook Pro", or "iPhone" in **System Settings** → **General** → **Sharing**. Algunos [scripts de privacidad](https://github.com/sunknudsen/privacy-guides/tree/master/how-to-spoof-mac-address-and-hostname-automatically-at-boot-on-macos#guide) le permiten generar fácilmente nombres de host aleatorios.

## Protecciones de seguridad

macOS utiliza la defensa en profundidad, confiando en múltiples capas de protección basadas en software y hardware, con diferentes propiedades. Esto garantiza que un fallo en una capa no compromete la seguridad general del sistema.

### Seguridad del software

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

macOS permite instalar actualizaciones de prueba. Estas son inestables y pueden incluir telemetría adicional, porque son para fines de prueba. Debido a esto, recomendamos evitar las actualizaciones de prueba del software en general.

</div>

#### Volumen firmado del sistema

Los componentes del sistema de macOS se encuentran protegidos en un volumen firmado del sistema de solo lectura, significando que no usted ni el malware pueden modificar archivos importantes del sistema.

El volumen del sistema es verificado mientras se encuentra en ejecución y cualquier dato que no se encuentra firmado con una firma criptográfica válida de Apple será rechazado.

#### Protección de la integridad del sistema

macOS establece ciertas restricciones de seguridad que no pueden ser anuladas. Estos son llamados Controles de Acceso Obligatorios y constituyen la base del sandbox, los controles parentales y la Protección de la integridad del sistema en macOS.

La Protección de la integridad del sistema hace que las ubicaciones de los archivos críticos sean de solo lectura, para protegerlas contra la modificación de código malicioso. Esto se suma a la Protección de integridad del núcleo basada en hardware, que protege al kernel ante las modificaciones en memoria.

#### Seguridad de las aplicaciones

##### Sandbox de aplicaciones

On macOS, whether an app is sandboxed is determined by the developer when they sign it. The App Sandbox protects against vulnerabilities in the apps you run by limiting what a malicious actor can access in the event that the app is exploited. The App Sandbox *alone* can't protect against [:material-package-variant-closed-remove: Supply Chain Attacks](../basics/common-threats.md#attacks-against-certain-organizations ""){.pg-viridian} by malicious developers. For that, sandboxing needs to be enforced by someone other than the developer themselves, as it is on the App Store.

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

El software descargado desde fuera de la App Store oficial no necesita ser virtualizado. If your threat model prioritizes defending against [:material-bug-outline: Passive Attacks](../basics/common-threats.md#security-and-privacy){ .pg-orange }, then you may want to check if the software you download outside the App Store is sandboxed, which is up to the developer to *opt in*.

</div>

You can check if an app uses the App Sandbox in a few ways:

You can check if apps that are already running are sandboxed using the [Activity Monitor](https://developer.apple.com/documentation/security/protecting-user-data-with-app-sandbox#Verify-that-your-app-uses-App-Sandbox).

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

Just because one of an app's processes is sandboxed doesn't mean they all are.

</div>

Alternatively, you can check apps before you run them by running this command in the terminal:

``` zsh
% codesign -dvvv --entitlements - <path to your app>
```

If an app is sandboxed, you should see the following output:

``` zsh
    [Key] com.apple.security.app-sandbox
    [Value]
        [Bool] true
```

If you find that the app you want to run is not sandboxed, then you may employ methods of [compartmentalization](../basics/common-threats.md#security-and-privacy) such as virtual machines or separate devices, use a similar app that is sandboxed, or choose to not use the unsandboxed app altogether.

##### Hardened Runtime

The [Hardened Runtime](https://developer.apple.com/documentation/security/hardened_runtime) is an extra form of protection for apps that prevents certain classes of exploits. It improves the security of apps against exploitation by disabling certain features like JIT.

You can check if an app uses the Hardened Runtime using this command:

``` zsh
codesign --display --verbose /path/to/bundle.app
```

If Hardened Runtime is enabled, you will see `flags=0x10000(runtime)`. The `runtime` output means Hardened Runtime is enabled. There might be other flags, but the runtime flag is what we're looking for here.

You can enable a column in Activity Monitor called "Restricted" which is a flag that prevents programs from injecting code via macOS's [dynamic linker](https://pewpewthespells.com/blog/blocking_code_injection_on_ios_and_os_x.html). Ideally, this should say "Yes".

##### Antivirus

macOS incluye dos formas de defensa ante el malware:

1. La protección ante la ejecución del malware es proporcionada por el proceso de revisión de aplicaciones de la App Store, o la *Notarización* (parte de *Gatekeeper*), proceso donde las aplicaciones de terceros son escaneadas por Apple para buscar algún malware conocido, antes de que se le permita ser ejecutada. Apps are required to be signed by the developers using a key given to them by Apple. This ensures that you are running software from the real developers. Notarization also requires that developers enable the Hardened Runtime for their apps, which limits methods of exploitation.
2. La protección contra otros malware y la remediación contra malware existente en el sistema, es proporcionada por *XProtect*, un antivirus tradicional incluido en macOS.

Recomendamos evitar la instalación de antivirus desarrollados por terceras personas porque, generalmente, estos no cuentan con acceso al nivel del sistema, requerido para funcionar correctamente. Esto se debe a las limitaciones de Apple en las aplicaciones de terceros, además de que garantizar altos niveles de acceso puede afectar la seguridad y la privacidad de la computadora.

##### Copias de seguridad

macOS incluye un programa de copia de seguridad automática llamado [Time Machine](https://support.apple.com/HT201250), para que pueda crear respaldos encriptados a una unidad externa o de red, en caso de que se corrompan o eliminen archivos.

### Seguridad del hardware

Muchas de las funciones modernas de seguridad en macOS—como el moderno Arranque Seguro, la mitigación de vulnerabilidades a nivel del hardware, la verificación de integridad del sistema operativo, y la encriptación basada en archivos—dependen de Apple Silicon, y el nuevo hardware de Apple siempre tiene una [mejor seguridad](https://support.apple.com/guide/security/apple-soc-security-sec87716a080/1/web/1). Recomendamos el uso de Apple Silicon y no de computadoras antiguas basadas en Intel o Hackintosh.

Algunas de estas funciones modernas de seguridad están disponibles en las viejas computadoras Mac basadas en Intel, con el chip de seguridad Apple T2, pero este chip es susceptible a la vulnerabilidad de *checkm8*, que puede comprometer la seguridad.

Si utilizas accesorios Bluetooth como un teclado, recomendamos que únicamente utiliza los oficiales de Apple, porque su firmware puede ser actualizado automáticamente por macOS. Utilizar accesorios de terceros está bien, pero debes recordar instalar las actualizaciones del firmware regularmente.

Los SoC de Apple se encuentran enfocados en minimizar la superficie de ataque, relegando las funciones de seguridad al hardware dedicado con funcionalidad limitada.

#### ROM de arranque

macOS previene la persistencia del malware, al permitir que únicamente el software de Apple se ejecute durante el tiempo de arranque. Esto es conocido como arranque seguro. Las computadoras Mac verifican esto con un poco de memoria de solo lectura en el SoC, llamada ROM de arranque, que se establece durante la fabricación del chip.

La ROM de arranque conforma la raíz de confianza del hardware. Esto asegura que el malware no manipule el proceso de arranque. Cuando tu Mac inicia, la ROM de arranque es lo primero que se ejecuta, conformando el primer eslabón en la cadena de confianza.

Las computadoras Mac se pueden configurar para iniciar en tres modos de seguridad: *Seguridad completa*, *Seguridad reducida*, y *Seguridad permisiva*, con la Seguridad completa como configuración por defecto. Lo ideal es que utilices el modo de Seguridad completa y evites cosas como las **extensiones del kernel**, que te obligan a reducir el modo de seguridad. Debes asegurarte de [comprobar](https://support.apple.com/guide/mac-help/change-security-settings-startup-disk-a-mac-mchl768f7291/mac) que estés utilizando el modo de Seguridad completa.

#### Enclave seguro

El enclave seguro es un chip de seguridad incluido en los dispositivos con Apple Silicon y es responsable de almacenar y generar las claves de cifrado para los datos en reposo, así comolos datos de Face ID y Touch ID. Este contiene su propia ROM de arranque.

Puedes pensar en el enclave seguro como el centro de seguridad de tu dispositivo: este tiene un motor de cifrado AES y un mecanismo para almacenar de manera segura tus claves de cifrado, y se encuentra separado del resto del sistema, por lo que, si el procesador principal se encuentra comprometido, este debe estar seguro.

#### Touch ID

La característica de Touch ID de Apple permite desbloquear de una manera segura tus dispositivos utilizando la biometría.

Tus datos biométricos nunca abandonan tu dispositivo; es almacenado únicamente en el enclave seguro.

#### Desconexión del micrófono por hardware

Todas las computadoras con Apple Silicon o el chip T2 cuentan con una característica para la desconexión del hardware del micrófono cuando se cierra la tapa. Esto significa que no hay alguna manera para los atacantes de escuchar el micrófono de tu Mac, incluso cuando el sistema operativo está comprometido.

Tome en cuenta que la cámara no cuenta con una desconexión del hardware, porque su vista se encuentra oscurecida cuando la tapa se encuentra cerrada.

#### Seguridad del procesador periférico

Las computadoras cuentan con procesadores incorporados, además de la CPU, que manejan cosas como las conexiones de red, los gráficos, la gestión de la energía, etc. Estos procesadores pueden tener una seguridad insuficiente y pueden verse comprometidos, por lo que Apple intenta minimizar la necesidad de estos procesadores en su hardware.

Cuando es necesario utilizar alguno de estos procesadores, Apple trabaja con el proveedor para garantizar que el procesador

- ejecute un firmware verificado desde la CPU primaria al iniciar
- tiene su propia cadena de Arranque seguro
- sigue los estándares criptográficos mínimos
- garantiza que el firmware defectuoso conocido es revocado correctamente
- tiene sus interfaces de depuración desactivadas
- está firmado con las claves criptográficas de Apple

#### Protecciones de Acceso Directo a la Memoria

Apple Silicon separa cada componente que requiere acceso directo a la memoria. Por ejemplo, un puerto Thunderbolt no puede acceder a la memoria designada para el kernel.

## Fuentes

- [Seguridad de la plataforma Apple](https://support.apple.com/guide/security/welcome/web)
