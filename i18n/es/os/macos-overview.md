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

La mayoría de los problemas de privacidad y seguridad de los productos Apple están relacionados con sus *servicios en la nube*, no con su hardware o software. Cuando utilizas servicios de Apple como iCloud, la mayor parte de tu información se almacena en sus servidores y se protege con claves *a las que Apple tiene acceso* por defecto. En ocasiones, las fuerzas de seguridad han abusado de este nivel de acceso para eludir el hecho de que tus datos están cifrados de forma segura en tu dispositivo y, por supuesto, Apple es vulnerable a las filtraciones de datos como cualquier otra empresa.

Por lo tanto, si utilizas iCloud, deberías activar la [ **Protección de Datos Avanzada**](https://support.apple.com/HT212520). Esto encripta casi todos tus datos de iCloud con claves almacenadas en tus dispositivos (encriptación de extremo a extremo), en lugar de en los servidores de Apple, de modo que tus datos de iCloud están protegidos en caso de violación de datos y, por lo demás, ocultos a Apple.

### Ajustes del Sistema

Hay una serie de configuraciones integradas que deberías confirmar o cambiar para reforzar tu sistema. Abre la aplicación **Ajustes**:

#### Bluetooth

- [ ] Desmarca **Bluetooth** (a menos que lo estés utilizando actualmente)

#### Red

Dependiendo de si estás utilizando **Wi-Fi** o **Ethernet** (indicado con un punto verde y la palabra "conectado"), haz clic en el icono correspondiente.

Haz clic en el botón "Detalles" junto al nombre de tu red:

- [x] Selecciona **Limitar rastreo de dirección IP**

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

- [x] Click **Turn On**

##### Modo hermético

El [modo hermético](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode) desactiva algunas características para mejorar la seguridad. Algunas aplicaciones o características funcionan diferente, a comparación de cuando se encuentra desactivado. Por ejemplo, [JIT](https://hacks.mozilla.org/2017/02/a-crash-course-in-just-in-time-jit-compilers/) y [WASM](https://developer.mozilla.org/en-US/docs/WebAssembly) son desactivados en Safari con el modo hermético activado. Recomendamos activar el modo hermético y comprobar si este afecta significativamente su uso, porque muchos de los cambios que este hace son fáciles de manejar.

- [x] Click **Turn On**

### Aleatorización de direcciones Mac

macOS uses a randomized MAC address when performing Wi-Fi scans while disconnected from a network. However, when you connect to a preferred Wi-Fi network, the MAC address used is never randomized. Full MAC address randomization is an advanced topic, and most people don't need to worry about performing the following steps.

Unlike iOS, macOS doesn't give you an option to randomize your MAC address in the settings, so if you wish to change this identifier, you'll need to do it with a command or a script. To set a random MAC address, first disconnect from the network if you're already connected, then open **Terminal** and enter this command to randomize your MAC address:

``` zsh
openssl rand -hex 6 | sed 's/^\(.\{1\}\)./\12/; s/\(..\)/\1:/g; s/.$//' | xargs sudo ifconfig en0 ether
```

`en0` is the name of the interface you're changing the MAC address for. Puede que esto no sea correcto en todos los Mac, así que para comprobarlo puedes mantener presionada la tecla Opción y seleccionar el símbolo de Wi-Fi en la parte superior derecha de la pantalla. "Interface name" should be displayed at the top of the dropdown menu.

This command sets your MAC address to a randomized, "locally administered" address, matching the behavior of iOS, Windows, and Android's MAC address randomization features. This means that every character in the MAC address is fully randomized except the second character, which denotes the MAC address as *locally administered* and not in conflict with any actual hardware. This method is most compatible with modern networks. An alternative method is to set the first six characters of the MAC address to one of Apple's existing *Organizational Unique Identifiers*, which we'll leave as an exercise to the reader. That method is more likely to conflict with some networks, but may be less noticeable. Given the prevalence of randomized, locally administered MAC addresses in other modern operating systems, we don't think either method has significant privacy advantages over the other.

When you connect to the network again, you'll connect with a random MAC address. Esto se restablecerá al reiniciar.

Your MAC address is not the only unique information about your device which is broadcast on the network, your hostname is another piece of information which could uniquely identify you. You may wish to set your hostname to something generic like "MacBook Air", "Laptop", "John's MacBook Pro", or "iPhone" in **System Settings** > **General** > **Sharing**. Some [privacy scripts](https://github.com/sunknudsen/privacy-guides/tree/master/how-to-spoof-mac-address-and-hostname-automatically-at-boot-on-macos#guide) allow you to easily generate hostnames with random names.

## Protecciones de seguridad

macOS utiliza la defensa en profundidad, confiando en múltiples capas de protección basadas en software y hardware, con diferentes propiedades. Esto garantiza que un fallo en una capa no compromete la seguridad general del sistema.

### Seguridad del software

!!! warning "Advertencia"

    macOS permite instalar actualizaciones de prueba. Estas son inestables y pueden incluir telemetría adicional, porque son para fines de prueba. Debido a esto, recomendamos evitar las actualizaciones de prueba del software en general.

#### Volumen firmado del sistema

Los componentes del sistema de macOS se encuentran protegidos en un volumen firmado del sistema de solo lectura, significando que no usted ni el malware pueden modificar archivos importantes del sistema.

El volumen del sistema es verificado mientras se encuentra en ejecución y cualquier dato que no se encuentra firmado con una firma criptográfica válida de Apple será rechazado.

#### Protección de la integridad del sistema

macOS establece ciertas restricciones de seguridad que no pueden ser anuladas. Estos son llamados Controles de Acceso Obligatorios y constituyen la base del sandbox, los controles parentales y la Protección de la integridad del sistema en macOS.

La Protección de la integridad del sistema hace que las ubicaciones de los archivos críticos sean de solo lectura, para protegerlas contra la modificación de código malicioso. Esto se suma a la Protección de integridad del núcleo basada en hardware, que protege al kernel ante las modificaciones en memoria.

#### Seguridad de las aplicaciones

##### Sandbox de aplicaciones

Para las aplicaciones de macOS descargadas desde App Store, es necesario que estas se encuentren virtualizadas utilizando el [Sandbox de aplicaciones](https://developer.apple.com/documentation/security/app_sandbox).

!!! warning "Advertencia"

    El software descargado desde fuera de la App Store oficial no necesita ser virtualizado. Debes evitar en la medida de lo posible el software que no se encuentre en la App Store.

##### Antivirus

macOS incluye dos formas de defensa ante el malware:

1. La protección ante la ejecución del malware es proporcionada por el proceso de revisión de aplicaciones de la App Store, o la *Notarización* (parte de *Gatekeeper*), proceso donde las aplicaciones de terceros son escaneadas por Apple para buscar algún malware conocido, antes de que se le permita ser ejecutada.
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
