---
title: Android
description: Nuestros consejos para sustituir las funciones predeterminadas de Android que invaden la privacidad por alternativas privadas y seguras.
icon: simple/android
cover: android.webp
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: Recomendaciones de Android
    url: ./
  - "@context": http://schema.org
    "@type": CreativeWork
    name: Android
    image: /assets/img/android/android.svg
    url: https://source.android.com/
    sameAs: https://en.wikipedia.org/wiki/Android_(operating_system)
---

![Logo de Android](../assets/img/android/android.svg){ align=right }

El **Android Open Source Project** (AOSP) es un sistema operativo de código abierto liderado por Google, que se encuentra detrás de la mayoría de dispositivos móviles a nivel mundial. La mayoría de los teléfonos vendidos con Android son modificados para incluir integraciones invasivas y aplicaciones como los Servicios de Google Play, por lo que puedes mejorar de manera significativa tu privacidad en tu dispositivo móvil al reemplazar la instalación predeterminada con una versión de Android sin estas características invasivas.

[Resumen General de Android :material-arrow-right-drop-circle:](../os/android-overview.md){ .md-button .md-button--primary }

## Nuestro Consejo

### Sustituye los Servicios de Google

Hay muchos métodos para obtener aplicaciones en Android sin tener que recurrir a Google Play. Siempre que sea posible, intenta utilizar uno de estos métodos antes de obtener tus aplicaciones de fuentes no privadas:

[Obtener Aplicaciones :material-arrow-right-drop-circle:](obtaining-apps.md){ .md-button }

También hay muchas alternativas privadas a las aplicaciones que vienen preinstaladas en el teléfono, como la aplicación de la cámara. Además de las aplicaciones para Android que recomendamos en este sitio en general, hemos creado una lista de utilidades del sistema específicas para Android que pueden resultarte útiles.

[Recomendaciones Generales de Aplicaciones :material-arrow-right-drop-circle:](general-apps.md){ .md-button }

### Instala una Distribución Personalizada

Cuando compras un teléfono Android, el sistema operativo por defecto viene con aplicaciones y funcionalidades que no forman parte de Android Open Source Project. Muchas de estas aplicaciones -incluso aplicaciones como el marcador que proporcionan una funcionalidad básica del sistema- requieren integraciones invasivas con Google Play Services, que a su vez pide privilegios para acceder a tus archivos, almacenamiento de contactos, registros de llamadas, mensajes SMS, ubicación, cámara, micrófono y muchas otras cosas en tu dispositivo para que esas aplicaciones básicas del sistema y muchas otras aplicaciones funcionen en primer lugar. Frameworks como Google Play Services aumentan la superficie de ataque de tu dispositivo y son la fuente de varios problemas de privacidad con Android.

Este problema se puede resolver utilizando una distribución alternativa de Android, comúnmente conocida como _ROM personalizada_, que no venga con una integración tan invasiva. Desafortunadamente, varias distribuciones modificadas de Android suelen violar el modelo de seguridad de Android al no soportar características críticas de seguridad como el AVB, protección de reversión, actualizaciones del firmware, etc. Algunas distribuciones también incluyen compilaciones [`userdebug`](https://source.android.com/setup/build/building#choose-a-target) que exponen la raíz a través de [ADB](https://developer.android.com/studio/command-line/adb) y requieren políticas SELinux más permisivas para acomodar las características de depuración, lo que resulta en una mayor superficie de ataque y un modelo de seguridad debilitado.

Idealmente, cuando escojas una distribución de Android, deberías asegurarte de que mantenga el modelo de seguridad de Android. Como mínimo, la distribución debería tener compilaciones de producción, compatibilidad con AVB, protección contra reversiones, actualizaciones puntuales del firmware y del sistema operativo, y SELinux en [modo de imposición](https://source.android.com/security/selinux/concepts#enforcement_levels). Todas nuestras distribuciones de Android recomendadas cumplen estos criterios:

[Distribuciones Recomendadas :material-arrow-right-drop-circle:](distributions.md){ .md-button }

### Evita Rootear

El [Rooting](https://es.wikipedia.org/wiki/Root_\(Android\)) de los teléfonos Android puede disminuir la seguridad de forma significativa, ya que debilita todo el [modelo de seguridad de Android](https://es.wikipedia.org/wiki/Android#Seguridad,_privacidad_y_vigilancia). Esto puede debilitar la privacidad en caso de que haya un exploit que sea asistido por la seguridad debilitada. Los métodos de rooteo más comunes involucran la manipulación directa de la partición de arranque, haciendo que sea imposible realizar con éxito el arranque verificado. Las aplicaciones que requieren root también modificarán la partición del sistema, lo que significa que el Arranque Verificado tendría que permanecer desactivado. Tener la raíz expuesta directamente en la interfaz de usuario también aumenta la superficie de ataque de su dispositivo y puede ayudar en las vulnerabilidades de [escalada de privilegios](https://es.wikipedia.org/wiki/Escalada_de_privilegios) y las omisiones de la política SELinux.

Content blockers which modify the [hosts file](https://en.wikipedia.org/wiki/Hosts_\(file\)) (like AdAway) and firewalls which require root access persistently (like AFWall+) are dangerous and should not be used. Tampoco son la forma correcta de resolver sus propósitos. Para el bloqueo de contenidos, sugerimos [DNS](../dns.md) cifrado o la funcionalidad de bloqueo de contenidos proporcionada por una VPN. TrackerControl and AdAway in non-root mode will take up the VPN slot (by using a local loopback VPN), preventing you from using privacy-enhancing services such as [Orbot](../alternative-networks.md#orbot) or a [real VPN provider](../vpn.md).

AFWall+ funciona basado en el enfoque [filtrado de paquetes](https://es.wikipedia.org/wiki/Cortafuegos_\(inform%C3%A1tica\)#Cortafuegos_de_capa_de_red_o_de_filtrado_de_paquetes) y puede ser evitable en algunas situaciones.

No creemos que los sacrificios de seguridad realizados al rootear un teléfono merezcan la pena por los cuestionables beneficios de privacidad de esas aplicaciones.

### Instala Actualizaciones Periódicamente

Es importante no utilizar una versión [end-of-life](https://endoflife.date/android) de Android. Las nuevas versiones de Android no solo reciben actualizaciones de seguridad para el sistema operativo, sino también importantes actualizaciones para mejorar la privacidad.

Por ejemplo, [antes de Android 10](https://developer.android.com/about/versions/10/privacy/changes) cualquier app con el permiso [`READ_PHONE_STATE`](https://developer.android.com/reference/android/Manifest.permission#READ_PHONE_STATE) podía acceder a números de serie sensibles y únicos de tu teléfono como [IMEI](https://es.wikipedia.org/wiki/IMEI), [MEID](https://en.wikipedia.org/wiki/Mobile_equipment_identifier), o el [IMSI](https://es.wikipedia.org/wiki/IMSI) de tu tarjeta SIM; mientras que ahora deben ser apps del sistema para hacerlo. Las aplicaciones del sistema sólo las proporciona el OEM o la distribución de Android.

### Utiliza las Funciones Integradas para Compartir

Puedes evitar dar permiso a muchas aplicaciones para acceder a tus archivos multimedia con las funciones de uso compartido integradas en Android. Muchas aplicaciones te permiten "compartir" un archivo con ellas para cargarlo.

Por ejemplo, si quieres publicar una foto en Discord, puedes abrir tu gestor de archivos o galería y compartir esa foto con la aplicación Discord, en lugar de conceder a Discord acceso completo a tus archivos miltimedia y fotos.
