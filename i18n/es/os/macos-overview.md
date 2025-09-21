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

- [ ] Desactiva **Bluetooth** (a menos que lo estés utilizando actualmente)

#### Red

Dependiendo de si estás utilizando **Wi-Fi** o **Ethernet** (indicado con un punto verde y la palabra "conectado"), haz clic en el icono correspondiente.

Haz clic en el botón "Detalles" junto al nombre de tu red:

- [x] Selecciona **Rotatoria** en **Dirección Wi-Fi privada**

- [x] Activa **Limitar rastreo de dirección IP**

##### Firewall

Tu cortafuegos bloquea conexiones de red no deseadas. Cuanto más estricta sea la configuración de tu cortafuegos, más seguro estará su Mac. Sin embargo, algunos servicios estarán bloqueados. Debes configurar tu cortafuegos para que sea lo más estricto posible sin bloquear los servicios que utilizas.

- [x] Activa **Firewall**

Haz clic en el botón **Opciones**:

- [x] Activa **Bloquear todas las conexiones entrantes**

Si esta configuración es demasiado estricta, puedes volver y desmarcarla. Sin embargo, macOS normalmente te pedirá que permitas conexiones entrantes para una aplicación si la aplicación lo solicita.

#### General

Por defecto, el nombre de tu dispositivo será algo así como "iMac de [tu nombre]". Dado que este nombre se [difunde públicamente en tu red](https://support.apple.com/guide/mac-help/change-computers-local-hostname-mac-mchlp2322/26/mac/26#:~:text=The%20local%20hostname%2C%20or%20local%20network%20name%2C%20is%20displayed%20at%20the%20bottom%20of%20the%20Sharing%20settings%20window.%20It%20identifies%20your%20Mac%20to%20Bonjour%2Dcompatible%20services.), querrás cambiar el nombre de tu dispositivo por algo genérico como "Mac".

Haz clic en **Acerca de** y escribe el nombre del dispositivo que desees en el campo **Nombre**.

##### Actualizaciones de Software

Deberías instalar automáticamente todas las actualizaciones disponibles para asegurarte de que tu Mac cuenta con las últimas correcciones de seguridad.

Haz clic en el pequeño :material-information-outline: icono situado junto a **Actualizaciones Automáticas**:

- [x] Activa **Descargar las actualizaciones nuevas cuando estén disponibles**

- [x] Activa **Instalar actualizaciones de macOS**

- [x] Activa **Instalar respuestas de seguridad y archivos del sistema**

#### Apple Intelligence y Siri

Si no utilizas estas funciones en macOS, deberías desactivarlas:

- [ ] Desactiva **Apple Intelligence**
- [ ] Desactiva **Siri**

**[Apple Intelligence](https://apple.com/legal/privacy/data/en/intelligence-engine)** solo está disponible en dispositivos compatibles. Apple Intelligence utiliza una combinación de procesamiento en el dispositivo y su [Private Cloud Compute](https://security.apple.com/blog/private-cloud-compute) para cosas que requieren más potencia de procesamiento de la que puede proporcionar tu dispositivo.

Para ver un informe de todos los datos enviados a través de Apple Intelligence, puedes ir a **Privacidad y seguridad** → **Informe de Apple Intelligence** y pulsar **Exportar actividad** para ver la actividad de los últimos 15 minutos o 7 días, dependiendo de tu configuración. De forma similar al **Informe de privacidad de las apps**, que muestra los permisos recientes a los que han accedido las aplicaciones de tu teléfono, el Informe de Apple Intelligence también muestra lo que se envía a los servidores de Apple mientras utilizas Apple Intelligence.

Por defecto, la integración ChatGPT está desactivada. Si ya no quieres la integración con ChatGPT, puedes ir a **ChatGPT**:

- [ ] Desactiva **Usar ChatGPT**

También puedes hacer que te solicite una confirmación cada vez que dejes activada la integración con ChatGPT:

- [x] Activa **Confirmar peticiones**

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

Cualquier solicitud realizada con ChatGPT será enviada a los servidores de ChatGPT, no hay procesamiento en el dispositivo ni PCC como con Apple Intelligence.

</div>

#### Privacidad y Seguridad

Siempre que una aplicación solicite un permiso, aparecerá aquí. Puedes decidir a qué aplicaciones deseas permitir o denegar permisos específicos.

##### Servicios de Localización

Puedes permitir individualmente los servicios de localización por aplicación. Si no necesitas que las aplicaciones utilicen tu ubicación, desactivar por completo los servicios de localización es la opción más privada.

- [ ] Desactiva **Localización**

##### Análisis y Mejoras

Decide si quieres compartir datos analíticos con Apple y los desarrolladores de aplicaciones.

##### Publicidad de Apple

Decide si quieres anuncios personalizados en función de tu uso.

- [ ] Desactiva **Anuncios Personalizados**

##### FileVault

En los dispositivos modernos con Secure Enclave (Apple T2 Security Chip, Apple Silicon), tus datos siempre están cifrados, pero se descifran automáticamente mediante una llave de hardware si el dispositivo no detecta que ha sido manipulado. Activar [FileVault](../encryption.md#filevault) requiere además tu contraseña para descifrar tus datos, lo que mejora enormemente la seguridad, especialmente cuando está apagado o antes del primer inicio de sesión después de encenderlo.

En los ordenadores Mac basados en Intel más antiguos, FileVault es la única forma de cifrado de disco disponible por defecto, y debería estar siempre activada.

- [x] Seleccione **Encender**

##### Modo de Aislamiento

El **[Modo de aislamiento](https://support.apple.com/guide/mac-help/lock-mac-targeted-a-cyberattack-ibrw66f4e191/mac)** desactiva algunas funciones para mejorar la seguridad. Algunas aplicaciones o funciones no funcionarán igual que cuando está desactivado. Por ejemplo, la compilación Javascript Just-In-Time[(JIT](https://hacks.mozilla.org/2017/02/a-crash-course-in-just-in-time-jit-compilers)) y [WebAssembly](https://developer.mozilla.org/docs/WebAssembly) están desactivados en Safari con el Modo de Aislamiento activado. Recomendamos activar el Modo de Aislamiento y ver si afecta significativamente al uso diario.

- [x] Seleccione **Encender**

### Aleatorización de direcciones Mac

macOS utiliza una dirección MAC aleatoria cuando [realiza escaneos Wi-Fi](https://support.apple.com/guide/security/privacy-features-connecting-wireless-networks-secb9cb3140c/web) mientras está desconectado de una red.

Puedes configurar tu [dirección MAC para que sea aleatoria](https://support.apple.com/en-us/102509) por red y rotarla ocasionalmente para evitar el rastreo entre redes y en la misma red a lo largo del tiempo.

Ve a **Ajustes del Sistema** → **Red** → **Wi-Fi** → **Detalles** y establece **Dirección Wi-Fi privada** en **Fija** si quieres una dirección fija pero única para la red a la que estás conectado, o en **Rotatoria** si quieres que cambie con el tiempo.

Considera también la posibilidad de cambiar tu nombre de host, que es otro identificador de dispositivo que se difunde en la red a la que estás conectado. Es posible que desees establecer tu nombre de host en algo genérico como "MacBook Air", "Laptop", "MacBook Pro de John", o "iPhone" en **Ajustes del Sistema**→ **General**→ **Compartir**.

## Protecciones de seguridad

macOS utiliza la defensa en profundidad, confiando en múltiples capas de protección basadas en software y hardware, con diferentes propiedades. Esto garantiza que un fallo en una capa no compromete la seguridad general del sistema.

### Seguridad del software

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

macOS permite instalar actualizaciones de prueba. Estos son inestables y pueden venir con [telemetría adicional](https://beta.apple.com/privacy) ya que son para propósitos de prueba. Debido a esto, recomendamos evitar las actualizaciones de prueba del software en general.

</div>

#### Volumen firmado del sistema

Los componentes del sistema de macOS están protegidos en un [volumen de sistema firmado](https://support.apple.com/guide/security/signed-system-volume-security-secd698747c9/web) de solo lectura, lo que significa que ni tú ni el malware podéis alterar los archivos importantes del sistema.

El volumen del sistema es verificado mientras se encuentra en ejecución y cualquier dato que no se encuentra firmado con una firma criptográfica válida de Apple será rechazado.

#### Protección de la integridad del sistema

macOS establece ciertas restricciones de seguridad que no pueden ser anuladas. Estos son llamados [Controles de acceso obligatorios](https://support.apple.com/guide/security/system-integrity-protection-secb7ea06b49/1/web/1) y constituyen la base del aislamiento, los controles parentales y la [Protección de la integridad del sistema](https://support.apple.com/en-us/102149) en macOS.

La Protección de la integridad del sistema hace que las ubicaciones de los archivos críticos sean de solo lectura, para protegerlas contra la modificación de código malicioso. Esto se suma a la Protección de integridad del núcleo basada en hardware, que protege al kernel ante las modificaciones en memoria.

#### Seguridad de las aplicaciones

##### Sandbox de aplicaciones

En macOS, el desarrollador determina si una aplicación está aislada cuando la firma. La [App Sandbox](https://developer.apple.com/documentation/xcode/configuring-the-macos-app-sandbox) protege contra las vulnerabilidades de las aplicaciones que ejecutas, limitando el acceso de un actor malicioso en caso de que la aplicación sea objeto de un ataque. El App Sandbox *por sí solo* no puede proteger contra [:material-package-variant-closed-remove: Ataques a la Cadena de Suministro](../basics/common-threats.md#attacks-against-certain-organizations ""){.pg-viridian} por parte de desarrolladores maliciosos. Para ello, el aislamiento debe ser impuesto por alguien que no sea el propio desarrollador, como ocurre en la [App Store](https://support.apple.com/guide/security/gatekeeper-and-runtime-protection-sec5599b66df/1/web/1#:~:text=All%20apps%20from%20the%20App%20Store%20are%20sandboxed%20to%20restrict%20access%20to%20data%20stored%20by%20other%20apps.).

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

macOS incluye dos formas de [defensa frente al malware](https://support.apple.com/guide/security/protecting-against-malware-sec469d47bd8/1/web/1):

1. La protección ante la ejecución del malware es proporcionada por el proceso de revisión de aplicaciones de la App Store, o la *Notarización* (parte de *Gatekeeper*), proceso donde las aplicaciones de terceros son escaneadas por Apple para buscar algún malware conocido, antes de que se le permita ser ejecutada. Las aplicaciones deben ser firmadas por los desarrolladores con una clave que les da Apple. Esto asegura que estás ejecutando software de los desarrolladores reales. La notarización también requiere que los desarrolladores habiliten el Hardened Runtime para sus aplicaciones, lo que limita los métodos de explotación.
2. La protección contra otros malware y la remediación contra malware existente en el sistema, es proporcionada por *XProtect*, un antivirus tradicional incluido en macOS.

Desaconsejamos la instalación de antivirus de terceros, ya que no suelen tener el acceso a nivel de sistema necesario para funcionar correctamente, debido a las limitaciones de Apple a las aplicaciones de terceros, y porque conceder los altos niveles de acceso que solicitan suele suponer un riesgo aún mayor para la seguridad y la privacidad de tu ordenador.

##### Copias de seguridad

macOS incluye un software de copia de seguridad automática llamado [Time Machine](https://support.apple.com/HT201250), para que puedas crear [copias de seguridad cifradas](https://support.apple.com/guide/mac-help/keep-your-time-machine-backup-disk-secure-mh21241/mac) en una unidad externa o en una unidad de red en caso de que se corrompan o eliminen archivos.

### Seguridad del hardware

Muchas de las funciones modernas de seguridad de macOS, como el moderno Arranque Seguro, la mitigación de exploits a nivel de hardware, las verificaciones de integridad del sistema operativo y la encriptación basada en archivos, se basan en Apple Silicon, y el hardware más reciente de Apple siempre ofrece la [mejor seguridad](https://support.apple.com/guide/security/apple-soc-security-sec87716a080/1/web/1). Solo recomendamos el uso de Apple Silicon y no de ordenadores antiguos basados en Intel o Hackintosh.

Algunas de estas funciones modernas de seguridad están disponibles en las viejas computadoras Mac basadas en Intel, con el chip de seguridad Apple T2, pero este chip es susceptible a la vulnerabilidad de *checkm8*, que puede comprometer la seguridad.

Si utilizas accesorios Bluetooth como un teclado, te recomendamos que utilices los oficiales de Apple, ya que su firmware [se actualizará automáticamente](https://support.apple.com/en-us/120303#:~:text=Firmware%20updates%20are%20automatically%20delivered%20in%20the%20background%20while%20the%20Magic%20Keyboard%20is%20actively%20paired%20to%20a%20device%20running%20macOS%2C%20iOS%2C%20iPadOS%2C%20or%20tvOS.) con macOS. Utilizar accesorios de terceros está bien, pero debes recordar instalar las actualizaciones del firmware regularmente.

Los SoC de Apple se centran en [minimizar la superficie de ataque](https://support.apple.com/en-vn/guide/security/secf020d1074/web#:~:text=Security%2Dfocused%20hardware%20follows%20the%20principle%20of%20supporting%20limited%20and%20discretely%20defined%20functions%20to%20minimize%20attack%20surface.) relegando las funciones de seguridad a hardware dedicado con funcionalidad limitada.

#### ROM de arranque

macOS evita la persistencia del malware permitiendo únicamente que el software oficial de Apple se ejecute en el arranque; esto se conoce como [arranque seguro](https://support.apple.com/en-vn/guide/security/secac71d5623/1/web/1). Los ordenadores Mac verifican esto con un poco de memoria de solo lectura en el SoC llamada [ROM de arranque](https://support.apple.com/en-vn/guide/security/aside/sec5240db956/1/web/1), que se [establece durante la fabricación del chip](https://support.apple.com/en-vn/guide/security/secf020d1074/1/web/1#:~:text=which%20is%20laid%20down%20during%20Apple%20SoC%20fabrication).

La ROM de arranque conforma la raíz de confianza del hardware. Esto garantiza que el malware no pueda manipular el proceso de arranque, ya que la ROM de arranque es inmutable. Cuando tu Mac inicia, la ROM de arranque es lo primero que se ejecuta, conformando el primer eslabón en la cadena de confianza.

Los ordenadores Mac pueden configurarse para arrancar en [tres modos de seguridad](https://support.apple.com/guide/deployment/startup-security-dep5810e849c/web#dep32fb404e1): *Seguridad total*, *Seguridad media* y *Sin seguridad*, siendo la configuración por defecto Seguridad total. Lo ideal sería utilizar el modo de Seguridad Total y evitar cosas como **[extensiones del kernel](https://support.apple.com/guide/deployment/system-extensions-in-macos-depa5fb8376f/web#dep51e097f45)** que te obligan a reducir el modo de seguridad. Debes asegurarte de [comprobar](https://support.apple.com/guide/mac-help/change-security-settings-startup-disk-a-mac-mchl768f7291/mac) que estés utilizando el modo de Seguridad completa.

#### Secure Enclave

**[Secure Enclave](https://support.apple.com/guide/security/secure-enclave-sec59b0b31ff/web)** es un chip de seguridad integrado en los dispositivos con Apple Silicon que se encarga de almacenar y generar las claves de cifrado de los datos en reposo, así como de los datos de Face ID y Touch ID. Este contiene su [propia ROM de arranque independiente](https://support.apple.com/en-vn/guide/security/sec59b0b31ff/web#sec43006c49f).

Puedes pensar en el enclave seguro como el centro de seguridad de tu dispositivo: este tiene un motor de cifrado AES y un mecanismo para almacenar de manera segura tus claves de cifrado, y se encuentra separado del resto del sistema, por lo que, si el procesador principal se encuentra comprometido, este debe estar seguro.

#### Touch ID

La característica de Touch ID de Apple permite desbloquear de una manera segura tus dispositivos utilizando la biometría.

Tus datos biométricos [nunca salen de tu dispositivo](https://www.apple.com/legal/privacy/data/en/touch-id/#:~:text=Touch%C2%A0ID%20data%20does%20not%20leave%20your%20device%2C%20and%20is%20never%20backed%20up%20to%20iCloud%20or%20anywhere%20else.); solo se almacenan en Secure Enclave.

#### Desconexión del micrófono por hardware

Todos los portátiles con Apple Silicon o el chip T2 incorporan una [desconexión por hardware](https://support.apple.com/guide/security/hardware-microphone-disconnect-secbbd20b00b/web) para el micrófono integrado cada vez que se cierra la tapa. Esto significa que no hay alguna manera para los atacantes de escuchar el micrófono de tu Mac, incluso cuando el sistema operativo está comprometido.

Tome en cuenta que la cámara no cuenta con una desconexión del hardware, porque su vista se encuentra oscurecida cuando la tapa se encuentra cerrada.

#### Indicador de Cámara Segura

La cámara integrada en un Mac está diseñada para que la cámara no pueda encenderse sin que [también se encienda](https://support.apple.com/en-us/102177#:~:text=The%20camera%20is%20engineered%20so%20that%20it%20can’t%20activate%20without%20the%20camera%20indicator%20light%20also%20turning%20on.%20This%20is%20how%20you%20can%20tell%20if%20your%20camera%20is%20on.) la luz indicadora de la cámara.

#### Seguridad del procesador periférico

Además de la CPU principal, los ordenadores llevan [incorporados otros procesadores](https://support.apple.com/en-vn/guide/security/seca500d4f2b/1/web/1) que se encargan de cosas como las redes, los gráficos, la gestión de la energía, etc. Estos procesadores pueden tener una seguridad insuficiente y pueden verse comprometidos, por lo que Apple intenta minimizar la necesidad de estos procesadores en su hardware.

Cuando es necesario utilizar alguno de estos procesadores, Apple trabaja con el proveedor para garantizar que el procesador

- ejecute un firmware verificado desde la CPU primaria al iniciar
- tiene su propia cadena de Arranque seguro
- sigue los estándares criptográficos mínimos
- garantiza que el firmware defectuoso conocido es revocado correctamente
- tiene sus interfaces de depuración desactivadas
- está firmado con las claves criptográficas de Apple

#### Protecciones de Acceso Directo a la Memoria

Apple Silicon separa cada componente que requiere [acceso directo a la memoria](https://support.apple.com/guide/security/direct-memory-access-protections-seca4960c2b5/1/web/1). Por ejemplo, un puerto Thunderbolt no puede acceder a la memoria designada para el kernel.

#### Entrada Segura de Teclado en Terminal

Activa la [Entrada de teclado segura](https://support.apple.com/guide/terminal/use-secure-keyboard-entry-trml109/mac) para evitar que otras aplicaciones detecten lo que escribes en el terminal.
