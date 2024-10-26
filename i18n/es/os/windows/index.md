---
title: Resumen de Windows
icon: material/microsoft-windows
description: Microsoft Windows es un sistema operativo común que es extremadamente poco privado desde el principio. Nuestra guía cubre la realización de algunas mejoras en tu computadora sin reemplazar tu sistema operativo.
---

**Microsoft Windows** es un sistema operativo común que se incluye por defecto en muchos PC. Las siguientes guías pretenden ofrecer algunas formas de mejorar la privacidad y reducir la telemetría y los datos almacenados por defecto desactivando algunas funciones innecesarias. Con el tiempo, Microsoft añade funciones al sistema operativo que, en ocasiones, pueden depender de servicios basados en la nube. Estas funciones suelen requerir ciertos tipos de [datos opcionales](https://privacy.microsoft.com/data-collection-windows) que a veces se envían a servidores remotos para su procesamiento.

Uno de los ejemplos más recientes se llama **Recall**, que forma parte del conjunto de funciones de IA de Copilot. Recall realiza periódicamente capturas de pantalla de cualquier cosa que hayas visto en tu PC para mostrártela más tarde. Estas funciones "útiles" crean metadatos considerables que pueden analizarse desde el punto de vista forense. En la mayoría de los casos, el historial de navegación es suficiente y esta función puede desactivarse de forma segura. La principal preocupación con Recall era que los datos se almacenan en una base de datos local que se descifra cuando el dispositivo está encendido, lo que significa que es un blanco fácil para los hackers si el dispositivo se infecta con malware. Recall no eliminará de la base de datos información confidencial como contraseñas copiadas o información financiera, pero sí protege contra la realización de capturas de pantalla de cualquier contenido protegido por derechos de autor mediante sistemas de gestión de derechos digitales (DRM).

Lamentablemente, esta función se añadió sin pensar demasiado en las implicaciones para la privacidad de tenerla activada por defecto (que ahora [ya no lo está](https://wired.com/story/microsoft-recall-off-default-security-concerns)). Sin embargo, no es un ejemplo aislado. Otro ejemplo fue Microsoft automáticamente [habilitando copias de seguridad de carpetas en OneDrive](https://neowin.net/news/windows-11-is-now-automatically-enabling-onedrive-folder-backup-without-asking-permission) en nuevas instalaciones de Windows 11 sin pedir permiso.

Puede mejorar tu privacidad y seguridad en Windows sin descargar ninguna herramienta de terceros con estas guías:

- Instalación Inicial (próximamente)
- [Configuración de las Directivas de Grupo](group-policies.md)
- Ajustes de Privacidad (próximamente)
- Sandboxing de Aplicaciones (próximamente)
- Endurecimiento de Seguridad (próximamente)

<div class="admonition example" markdown>
<p class="admonition-title">Esta sección es nueva</p>

Esta sección es un trabajo en curso, porque lleva bastante más tiempo y esfuerzo hacer que una instalación de Windows sea más respetuosa con la privacidad que otros sistemas operativos.

</div>

## Notas de Privacidad

Microsoft Windows, especialmente las versiones dirigidas a los consumidores, como la versión **Home**, no suelen dar prioridad a las funciones de privacidad por [defecto](https://theguardian.com/technology/2015/jul/31/windows-10-microsoft-faces-criticism-over-privacy-default-settings). Como resultado, a menudo vemos más [recopilación de datos](https://en.wikipedia.org/wiki/Criticism_of_Microsoft#Telemetry_and_data_collection) de lo necesario, sin ninguna advertencia real de que este es el comportamiento por defecto. En un intento de competir con Google en el espacio publicitario, [Cortana](https://es.wikipedia.org/wiki/Microsoft_Cortana) ha incluido identificadores únicos como un "ID de publicidad" para correlacionar el uso y ayudar a los anunciantes en la publicidad dirigida.  En el momento del lanzamiento, la telemetría no se podía desactivar en las ediciones no empresariales de Windows 10. Sigue sin poder desactivarse, pero Microsoft ha añadido la posibilidad de [reducir](https://extremetech.com/computing/243079-upcoming-windows-update-reduces-spying-microsoft-still-mum-data-collects) los datos que se les envían.

Con Windows 11 hay una serie de restricciones o valores predeterminados tales como:

- Exigir el uso de una cuenta Microsoft en lugar de una cuenta local.
- Hacer más difícil encontrar opciones de cuentas locales para Windows **Pro** y **Enterprise**.
- Habilitar por defecto todas las opciones de recogida de datos, exigiendo a los usuarios que "opten por no hacerlo".
- Integrar fuertemente servicios de Microsoft como Bing, OneDrive y Teams de forma que sean difíciles de eliminar y se presenten como la única opción a los usuarios.
- Establecer el navegador predeterminado siempre en Edge, o volver a Edge si se cambia.
- Añadir funciones de IA basadas en la nube a muchas áreas de Windows y varias aplicaciones de Microsoft.
- Almacenamiento innecesario de datos sensibles. Incluso los datos que se almacenan localmente y no se envían a Microsoft siguen siendo un objetivo para los hackers o el malware en tu dispositivo.

Microsoft suele utilizar la función de actualizaciones automáticas para añadir nuevas funciones a tu dispositivo y realizar cambios que recopilan tus datos y están activados por defecto. Algunas [funciones de privacidad](https://blogs.windows.com/windows-insider/2023/11/16/previewing-changes-in-windows-to-comply-with-the-digital-markets-act-in-the-european-economic-area), como la opción de _no participar_ en la sincronización de una cuenta Microsoft en línea con Windows, requieren que selecciones un país del EEE (Espacio Económico Europeo) durante la instalación. Se puede cambiar a tu país real después de instalar Windows.

## Ediciones de Windows

Desgraciadamente, muchas funciones críticas de privacidad y seguridad están solo disponibles en ediciones más caras de Windows, en lugar de estar disponibles en Windows **Home**. Algunas características que faltan en **Home** incluyen Bitlocker Drive Encryption, Hyper-V, y Windows Sandbox. En nuestras guías de Windows cubriremos cómo utilizar todas estas funciones adecuadamente, por lo que será necesario disponer de una edición premium de Windows.

Windows **Enterprise** ofrece la mayor flexibilidad a la hora de configurar los parámetros de privacidad y seguridad integrados en Windows. Por ejemplo, son las únicas ediciones que permiten activar el máximo nivel de restricciones en los datos enviados a Microsoft a través de herramientas de telemetría. Lamentablemente, Enterprise no está disponible para la venta al por menor, por lo que es posible que no esté disponible para ti.

La mejor versión disponible para la compra _al por menor_ es Windows **Pro**, ya que tiene casi todas las funciones que querrás utilizar para proteger tu dispositivo, como Bitlocker, Hyper-V, etc. Lo único que falta son algunas de las limitaciones más restrictivas de la telemetría de Microsoft, por desgracia.

Los estudiantes y profesores pueden obtener una licencia de Windows **Education** (equivalente a Enterprise) o **Pro Education** (equivalente a Pro) de forma gratuita, incluso en dispositivos personales, a través de su institución educativa. Muchas escuelas colaboran con Microsoft a través de OnTheHub o Microsoft Azure for Education, así que puedes consultar esos sitios o la página de beneficios de tu escuela para ver si cumples los requisitos. La obtención de estas licencias depende enteramente de su institución. Esta puede ser la mejor forma de obtener una edición Enterprise de Windows para uso personal. No existen riesgos adicionales para la privacidad o la seguridad asociados al uso de una licencia educativa en comparación con las versiones comerciales.

No se recomienda utilizar versiones modificadas de Windows de terceros, como Windows AME. Dado que las versiones modificadas de Windows, como Windows AME, no reciben actualizaciones, las funciones de seguridad y las definiciones antivirus de Windows Defender quedarán rezagadas con respecto al panorama actual de amenazas, lo que te expondrá a ataques y te hará aún menos seguro.

## Obtener Windows

Actualmente, solo están disponibles para su compra las claves de licencia de Windows 11, pero estas claves funcionarán también en Windows 10, por lo que puedes seguir comprando una clave de Windows 11 Pro para activar una instalación de Windows 10.

La herramienta oficial [Media Creation Tool](https://microsoft.com/software-download/windows11) es la mejor forma de poner un instalador de Windows en una unidad flash USB. Herramientas de terceros como Rufus o Etcher pueden modificar inesperadamente los archivos, lo que podría provocar problemas de arranque u otros problemas durante la instalación.

Esta herramienta solo permite realizar una instalación **Home** o **Pro**, ya que no hay descargas disponibles públicamente para la edición **Enterprise** de Windows. Si dispones de una clave de licencia **Enterpise**, puedes mejorar fácilmente una instalación **Pro**. Para ello, instala Windows **Pro** sin introducir una clave de licencia durante la instalación y, a continuación, introduce tu clave **Enterprise** en la aplicación Configuración una vez completada la instalación. Tu instalación **Pro** se actualizará a **Enterprise** automáticamente tras introducir una clave de licencia válida.

Si estás instalando una licencia **Education**, normalmente dispondrás de un enlace de descarga privado que se te proporcionará junto con tu clave de licencia cuando la obtengas del portal de beneficios de tu institución.
