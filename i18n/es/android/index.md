---
title: Android
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

[General Android Overview :material-arrow-right-drop-circle:](../os/android-overview.md){ .md-button .md-button--primary }

## Nuestro Consejo

### Replace Google Services

There are many methods of obtaining apps on Android while avoiding Google Play. Whenever possible, try using one of these methods before getting your apps from non-private sources:

[Obtaining Applications :material-arrow-right-drop-circle:](obtaining-apps.md){ .md-button }

There are also many private alternatives to the apps that come pre-installed on your phone, such as the camera app. Besides the Android apps we recommend throughout this site in general, we've created a list of system utilities specific to Android which you might find useful.

[General App Recommendations :material-arrow-right-drop-circle:](general-apps.md){ .md-button }

### Install a Custom Distribution

Cuando compras un teléfono Android, el sistema operativo por defecto viene con aplicaciones y funcionalidades que no forman parte de Android Open Source Project. Muchas de estas aplicaciones -incluso aplicaciones como el marcador que proporcionan una funcionalidad básica del sistema- requieren integraciones invasivas con Google Play Services, que a su vez pide privilegios para acceder a tus archivos, almacenamiento de contactos, registros de llamadas, mensajes SMS, ubicación, cámara, micrófono y muchas otras cosas en tu dispositivo para que esas aplicaciones básicas del sistema y muchas otras aplicaciones funcionen en primer lugar. Frameworks como Google Play Services aumentan la superficie de ataque de tu dispositivo y son la fuente de varios problemas de privacidad con Android.

This problem could be solved by using an alternative Android distribution, commonly known as a _custom ROM_, that does not come with such invasive integration. Desafortunadamente, varias distribuciones modificadas de Android suelen violar el modelo de seguridad de Android al no soportar características críticas de seguridad como el AVB, protección de reversión, actualizaciones del firmware, etc. Some distributions also ship [`userdebug`](https://source.android.com/setup/build/building#choose-a-target) builds which expose root via [ADB](https://developer.android.com/studio/command-line/adb) and require [more permissive](https://github.com/LineageOS/android_system_sepolicy/search?q=userdebug\&type=code) SELinux policies to accommodate debugging features, resulting in a further increased attack surface and weakened security model.

Idealmente, cuando escojas una distribución de Android, deberías asegurarte de que mantenga el modelo de seguridad de Android. At the very least, the distribution should have production builds, support for AVB, rollback protection, timely firmware and operating system updates, and SELinux in [enforcing mode](https://source.android.com/security/selinux/concepts#enforcement_levels). All of our recommended Android distributions satisfy these criteria:

[Recommended Distributions :material-arrow-right-drop-circle:](distributions.md){ .md-button }

### Avoid Root

[Rooting](https://en.wikipedia.org/wiki/Rooting_\(Android\)) Android phones can decrease security significantly as it weakens the complete [Android security model](https://en.wikipedia.org/wiki/Android_\(operating_system\)#Security_and_privacy). Esto puede debilitar la privacidad en caso de que haya un exploit que sea asistido por la seguridad debilitada. Los métodos de rooteo más comunes involucran la manipulación directa de la partición de arranque, haciendo que sea imposible realizar con éxito el arranque verificado. Apps that require root will also modify the system partition, meaning that Verified Boot would have to remain disabled. Having root exposed directly in the user interface also increases the attack surface of your device and may assist in [privilege escalation](https://en.wikipedia.org/wiki/Privilege_escalation) vulnerabilities and SELinux policy bypasses.

Content blockers which modify the [hosts file](https://en.wikipedia.org/wiki/Hosts_\(file\)) (AdAway) and firewalls (AFWall+) which require root access persistently are dangerous and should not be used. Tampoco son la forma correcta de resolver sus propósitos. For content blocking, we suggest encrypted [DNS](../dns.md) or content blocking functionality provided by a VPN instead. TrackerControl and AdAway in non-root mode will take up the VPN slot (by using a local loopback VPN), preventing you from using privacy enhancing services such as [Orbot](../tor.md#orbot) or a [real VPN provider](../vpn.md).

AFWall+ works based on the [packet filtering](https://en.wikipedia.org/wiki/Firewall_\(computing\)#Packet_filter) approach and may be bypassable in some situations.

No creemos que los sacrificios de seguridad realizados al rootear un teléfono merezcan la pena por los cuestionables beneficios de privacidad de esas aplicaciones.

### Install Updates Regularly

It's important to not use an [end-of-life](https://endoflife.date/android) version of Android. Newer versions of Android receive not only security updates for the operating system but also important privacy enhancing updates too.

For example, [prior to Android 10](https://developer.android.com/about/versions/10/privacy/changes) any apps with the [`READ_PHONE_STATE`](https://developer.android.com/reference/android/Manifest.permission#READ_PHONE_STATE) permission could access sensitive and unique serial numbers of your phone such as [IMEI](https://en.wikipedia.org/wiki/International_Mobile_Equipment_Identity), [MEID](https://en.wikipedia.org/wiki/Mobile_equipment_identifier), or your SIM card's [IMSI](https://en.wikipedia.org/wiki/International_mobile_subscriber_identity); whereas now they must be system apps to do so. Las aplicaciones del sistema sólo las proporciona el OEM o la distribución de Android.

### Use Built-in Sharing Features

Puedes evitar dar permiso a muchas aplicaciones para acceder a tus archivos multimedia con las funciones de uso compartido integradas en Android. Muchas aplicaciones te permiten "compartir" un archivo con ellas para cargarlo.

Por ejemplo, si quieres publicar una foto en Discord, puedes abrir tu gestor de archivos o galería y compartir esa foto con la aplicación Discord, en lugar de conceder a Discord acceso completo a tus archivos miltimedia y fotos.
