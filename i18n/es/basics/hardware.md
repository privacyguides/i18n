---
title: "Eligiendo Tu Hardware"
icon: 'material/chip'
description: El software no es lo único importante; aprende sobre las herramientas de hardware que puedes utilizar a diario para proteger tu privacidad.
---

Cuando se habla sobre privacidad, no se piensa tanto en el hardware como en el software que utilizamos. Tu hardware debe ser considerado como la base sobre la que construirás el resto de tu configuración de privacidad.

## Eligiendo una computadora

Los componentes internos de tus dispositivos procesan y almacenan toda tu información digital. Es importante que todos los dispositivos cuenten con soporte de parte del fabricante y los desarrolladores, con la recepción de actualizaciones de seguridad.

### Programas de seguridad del hardware

Algunos dispositivos tienen un "programa de seguridad del hardware", que consiste en una colaboración entre los proveedores sobre las mejores prácticas y recomendaciones al momento de diseñar un hardware, por ejemplo:

- [Los equipos de núcleo seguro de Windows](https://learn.microsoft.com/en-us/windows-hardware/design/device-experiences/oem-highly-secure-11) cumplen con unos criterios superiores de seguridad especificados por Microsoft. Estas protecciones no aplican únicamente a los usuarios de Windows; los usuarios de otros sistemas operativos pueden aprovechar características como la [protección DMA](https://learn.microsoft.com/en-us/windows/security/information-protection/kernel-dma-protection-for-thunderbolt) y la capacidad de desconfiar completamente de los certificados de Microsoft.
- [Android Ready SE](https://developers.google.com/android/security/android-ready-se) es una colaboración entre proveedores para garantizar que sus dispositivos siguen las [mejores prácticas](https://source.android.com/docs/security/best-practices/hardware) e incluyen almacenamiento respaldado por hardware a prueba de manipulaciones para cosas como las claves de cifrado.
- La ejecución de macOS en un SoC de Apple aprovecha las ventajas de la [seguridad del hardware](../os/macos-overview.md#hardware-security) que pueden no estar disponibles con sistemas operativos de terceros.
- La [seguridad de ChromeOS](https://chromium.org/chromium-os/developer-library/reference/security/security-whitepaper) es óptima cuando se ejecuta en un Chromebook, ya que puede hacer uso de las funciones de hardware disponibles, como la [raíz de confianza de hardware](https://chromium.org/chromium-os/developer-library/reference/security/security-whitepaper/#hardware-root-of-trust-and-verified-boot).

Incluso si no utilizas estos sistemas operativos, la participación en estos programas puede indicar que el fabricante sigue las mejores prácticas en lo que respecta a la seguridad y las actualizaciones del hardware.

### SO Preinstalado

Los ordenadores nuevos casi siempre vienen con Windows preinstalado, a no ser que compres un Mac o una máquina especializada en Linux. Suele ser una buena idea borrar la unidad e instalar una copia nueva del sistema operativo elegido, aunque eso signifique reinstalar Windows desde cero. Debido a los acuerdos entre los proveedores de hardware y los proveedores de software sospechoso, la instalación predeterminada de Windows a menudo viene precargada con bloatware, [adware](https://bleepingcomputer.com/news/technology/lenovo-gets-a-slap-on-the-wrist-for-superfish-adware-scandal), o incluso [malware](https://zdnet.com/article/dell-poweredge-motherboards-ship-with-malware).

### Actualizaciones de Firmware

El hardware suele tener problemas de seguridad que se descubren y parchean mediante actualizaciones del firmware de tu hardware.

Casi todos los componentes de la computadora necesitan firmware para funcionar, desde la placa base hasta los dispositivos de almacenamiento. Lo ideal es que todos los componentes de tu dispositivo sean totalmente compatibles. Los dispositivos Apple, Chromebooks, la mayoría de los teléfonos Android y los dispositivos Microsoft Surface gestionarán las actualizaciones de firmware por ti siempre que el dispositivo sea compatible.

Si construyes tu propio PC, es posible que tengas que actualizar manualmente el firmware de la placa base descargándolo desde el sitio web del fabricante. Si usas Linux, considera usar la herramienta integrada [`fwupd`](https://fwupd.org) que te permitirá buscar y aplicar cualquier actualización de firmware disponible para tu placa base.

### TPM/Criptoprocesador Seguro

La mayoría de computadoras y teléfonos vienen equipados con un TPM (o un criptoprocesador seguro similar) que almacena de forma segura tus claves de cifrado y maneja otras funciones relacionadas con la seguridad. Si actualmente utilizas una máquina que no tiene una de estas características, puede que te convenga comprar un ordenador más nuevo que disponga de ella. Algunas placas base de ordenadores de sobremesa y servidores tienen un «encabezado TPM» que puede aceptar una pequeña placa accesoria que contiene el TPM.

<div class="admonition Note" markdown>
<p class="admonition-title">Nota</p>

Los TPM virtuales son susceptibles de sufrir ataques de canal lateral y los TPM externos, al estar separados de la CPU en la placa base, son vulnerables al [sniffing](https://pulsesecurity.co.nz/articles/TPM-sniffing) cuando un atacante tiene acceso al hardware. La solución a este problema es incluir el procesador seguro dentro de la propia CPU, como es el caso de los chips de Apple y [Pluton](https://microsoft.com/en-us/security/blog/2020/11/17/meet-the-microsoft-pluton-processor-the-security-chip-designed-for-the-future-of-windows-pcs) de Microsoft.

</div>

### Biometría

Muchos dispositivos vienen equipados con un lector de huellas dactilares o funciones de reconocimiento facial. Pueden ser muy prácticos, pero no son perfectos y a veces fallan. La mayoría de los dispositivos volverán a utilizar un PIN o una contraseña cuando esto ocurra, lo que significa que la seguridad de tus dispositivos sigue dependiendo de tu contraseña.

La biometría puede impedir que alguien te vea teclear tu contraseña, así que si el shoulder-surfing forma parte de tu modelo de amenazas, la biometría es una buena opción.

La mayoría de las implementaciones de autenticación facial requieren que estés mirando el teléfono y, además, solo funcionan desde una distancia relativamente cercana, por lo que no tienes que preocuparte demasiado de que alguien te apunte a la cara para desbloquearlo sin tu consentimiento. Si lo deseas, puedes desactivar la biometría cuando el teléfono esté bloqueado. En iOS, puedes mantener pulsado el botón lateral y un botón de volumen durante 3 segundos para desactivar Face ID en los modelos que lo admitan. En Android, mantén pulsado el botón de encendido y pulsa Bloqueo en el menú.

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

Algunos dispositivos no disponen del hardware adecuado para la autenticación facial segura. Hay dos tipos principales de autenticación facial: 2D y 3D. La autenticación facial 3D utiliza un proyector de puntos que permite al dispositivo crear un mapa de profundidad 3D de tu cara. Asegúrate de que tu dispositivo dispone de esta capacidad.

</div>

Android define tres [clases de seguridad](https://source.android.com/docs/security/features/biometric/measure#biometric-classes) para la biometría; debes comprobar que tu dispositivo es de Clase 3 antes de activar la biometría.

### Cifrado del Dispositivo

Si tu dispositivo está [cifrado](../encryption.md), tus datos estarán más seguros cuando el dispositivo esté completamente apagado (en lugar de simplemente dormido), es decir, antes de que hayas introducido la clave de cifrado o la contraseña de la pantalla de bloqueo por primera vez. En los teléfonos, este estado de mayor seguridad se denomina "Antes del primer desbloqueo" (BFU), y "Después del primer desbloqueo"(AFU) una vez que se introduce la contraseña correcta tras un reinicio/encendido. AFU es considerablemente menos seguro contra los kits de herramientas forenses digitales y otros exploits, en comparación con BFU. Por lo tanto, si te preocupa que un atacante tenga acceso físico a tu dispositivo, deberías apagarlo por completo siempre que no lo estés utilizando.

Esto puede ser poco práctico, así que considera si vale la pena, pero en cualquier caso incluso el modo AFU es efectivo contra la mayoría de las amenazas, siempre que estés usando una clave de cifrado fuerte.

## Hardware Externo

Existen amenazas contra las que no es posible protegerse únicamente con los componentes internos. Muchas de estas opciones son altamente situacionales; por favor, evalúa si son realmente necesarias para tu modelo de amenaza.

### Llaves de Seguridad

Las llaves son dispositivos que utilizan criptografía fuerte para autenticarte en un dispositivo o cuenta. La idea es que, como no se pueden copiar, se pueden utilizar para proteger cuentas de forma que solo se pueda acceder a ellas con la posesión física de la clave, lo que elimina muchos ataques remotos.

[Llaves Recomendadas :material-arrow-right-drop-circle:](../security-keys.md){ .md-button .md-button--primary } [Más Información sobre las Llaves :material-arrow-right-drop-circle:](multi-factor-authentication.md#hardware-security-keys){ .md-button }

### Cámara/Micrófono

Si no quieres confiar en que los controles de permisos de tu sistema operativo impidan que la cámara se active en primer lugar, puedes comprar bloqueadores de cámara que impidan físicamente que la luz llegue a la cámara. También puedes comprar un dispositivo que no tenga cámara integrada y utilizar una cámara externa que puedas desconectar cuando termines de usarla. Algunos dispositivos vienen con bloqueadores de cámara integrados o interruptores de hardware que desconectan físicamente la cámara de la corriente.

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

Solo debes comprar cubiertas que se adapten a tu portátil y no causen daños al cerrar la tapa. Cubrir la cámara interferirá con el brillo automático y las funciones de autenticación facial.

</div>

Para acceder al micrófono, en la mayoría de los casos tendrás que confiar en los controles de permisos integrados en tu sistema operativo. Otra opción es comprar un dispositivo que no tenga micrófono incorporado y utilizar un micrófono externo que puedas desconectar cuando termines de usarlo. Algunos dispositivos, como un [MacBook o un iPad](https://support.apple.com/guide/security/hardware-microphone-disconnect-secbbd20b00b/web), disponen de un hardware que desconecta el micrófono cuando cierras la tapa.

Muchas computadoras tienen una opción en el BIOS para desactivar la cámara y el micrófono. Cuando se desactiva, el hardware ni siquiera aparecerá como dispositivo en un sistema arrancado.

### Pantallas de Privacidad

Las pantallas de privacidad son una lámina que se coloca sobre la pantalla normal para que solo sea visible desde un ángulo determinado. Esto es bueno si tu modelo de amenaza incluye que otros miren tu pantalla, pero no es infalible, ya que cualquiera podría cambiar el ángulo de visión y ver lo que hay en tu pantalla.

### Dispositivos de Hombre Muerto

Un dispositivo de hombre muerto impide que una máquina funcione sin la presencia de un operario. Originalmente se diseñaron como medida de seguridad, pero el mismo concepto puede aplicarse a un dispositivo electrónico para bloquearlo cuando no estás presente.

Algunos portátiles son capaces de [detectar](https://support.microsoft.com/en-us/windows/managing-presence-sensing-settings-in-windows-11-82285c93-440c-4e15-9081-c9e38c1290bb) cuándo estás presente y pueden bloquearse automáticamente cuando no estás sentado frente a la pantalla. Deberías comprobar la configuración de tu sistema operativo para ver si tu ordenador admite esta función.

También puedes conseguir cables, como [BusKill](https://buskill.in), que bloquearán o borrarán tu ordenador cuando se desconecte el cable.

### Anti-Interdicción/Ataque de Doncella Malvada

La mejor manera de prevenir un ataque dirigido contra ti antes de que un dispositivo esté en tu posesión es comprarlo en una tienda física, en lugar de encargarlo a domicilio.

Asegúrate de que tu dispositivo es compatible con el arranque seguro/verificado y de que lo tienes activado. Intenta evitar dejar tu dispositivo desatendido siempre que sea posible.

### Candados Kensington

Muchos ordenadores portátiles vienen equipados con un [conector de seguridad Kensington](https://www.kensington.com/solutions/product-category/security/? srsltid=AfmBOorQOlRnqRJOAqM-Mvl7wumed0wBdiOgktlvdidpMHNIvGfwj9VI) que se puede utilizar para asegurar el dispositivo con un **cable metálico** que se fija a la ranura de tu equipo. Estos candados pueden ser de combinación o con llave.

Al igual que todos los candados, los candados Kensington son vulnerables a [ataques físicos](https://youtu.be/vgvCxL7dMJk), por lo que se deben utilizar principalmente para disuadir a los ladrones ocasionales. Puedes asegurar tu portátil en casa o incluso cuando estés en público utilizando la pata de una mesa o algo que no se mueva con facilidad.

## Asegura tu Red

### Compartimentación

Existen muchas soluciones que permiten separar lo que se hace en un ordenador, como las máquinas virtuales y el sandboxing. Sin embargo, la mejor compartimentación es la separación física. Esto resulta especialmente útil en situaciones en las que determinados programas requieren que el usuario se salte las funciones de seguridad del sistema operativo, como ocurre con el software antitrampas incluido en muchos juegos.

Para jugar, puede ser útil designar una máquina como «de juego» y utilizarla únicamente para esa tarea. Mantenla en una VLAN separada. Esto puede requerir el uso de un conmutador gestionado y un router que admita redes segregadas.

La mayoría de los routers de usuario permiten hacerlo habilitando una red "de invitados" independiente que no puede comunicarse con la red principal. Todos los dispositivos que no sean de confianza pueden ir aquí, incluidos los dispositivos IoT como tu frigorífico inteligente, termostato, televisor, etc.

### Minimalismo

Como dice el dicho, «menos es más». Cuantos menos dispositivos tengas conectados a tu red, menos superficie de ataque potencial tendrás y menos trabajo te supondrá asegurarte de que todos ellos se mantienen actualizados.

Puede que te resulte útil recorrer tu casa y hacer una lista de todos los dispositivos conectados que tienes para ayudarte a hacer un seguimiento.

### Routers

El router gestiona todo el tráfico de red y actúa como primera línea de defensa entre el usuario e Internet.

<div class="admonition Note" markdown>
<p class="admonition-title">Nota</p>

Muchos routers incluyen un espacio de almacenamiento en el que puedes guardar tus archivos y acceder a ellos desde cualquier ordenador de la red. Te recomendamos que no utilices los dispositivos de red para otras cosas que no sean trabajar en red. En caso de que tu router se viera comprometido, tus archivos también lo estarían.

</div>

Lo más importante con los routers es mantenerlos actualizados. Muchos routers modernos instalan automáticamente las actualizaciones, pero muchos otros no. Debes comprobar esta opción en la página de configuración de tu router. Normalmente se puede acceder a esa página escribiendo `192.168.1.1` o `192.168.0.1` en la barra de URL de cualquier navegador, suponiendo que estés en la misma red. También puedes buscar "router" o "gateway" en la configuración de red de tu sistema operativo.

Si tu router no admite actualizaciones automáticas, tendrás que ir al sitio del fabricante para descargar las actualizaciones y aplicarlas manualmente.

Muchos routers de usuario no reciben soporte técnico durante mucho tiempo. Si tu router ya no está soportado por el fabricante, puedes comprobar si está soportado por [firmware FOSS](../router.md). También puedes comprar routers que vienen con firmware FOSS instalado por defecto; éstos suelen recibir soporte durante más tiempo que la mayoría de los routers.

Algunos ISP ofrecen un router/módem combinado. Puede ser beneficioso para la seguridad comprar un router independiente y configurar el router/módem de tu ISP en modo sólo módem. De este modo, aunque el router proporcionado por tu proveedor de Internet deje de recibir actualizaciones, podrás seguir recibiendo actualizaciones y parches de seguridad. También significa que cualquier problema que afecte a tu módem no afectará a tu router y viceversa.
