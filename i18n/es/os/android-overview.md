---
title: Resumen de Android
icon: simple/android
description: Android es un sistema operativo de código abierto con fuertes medidas de seguridad, lo que lo convierte en nuestra primera opción para teléfonos.
robots: nofollow, max-snippet:-1, max-image-preview:large
---

![Logotipo de Android](../assets/img/android/android.svg){ align=right }

**Android Open Source Project** es un sistema operativo móvil seguro que cuenta con un fuerte [aislamiento de aplicaciones](https://source.android.com/security/app-sandbox), [arranque verificado](https://source.android.com/security/verifiedboot) (AVB) y un sólido sistema de control de [permisos ](https://developer.android.com/guide/topics/permissions/overview).

[:octicons-home-16:](https://source.android.com){ .card-link title=Homepage }
[:octicons-info-16:](https://source.android.com/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://cs.android.com/android/platform/superproject/main){ .card-link title="Source Code" }

[Our Android Advice :material-arrow-right-drop-circle:](../android/index.md ""){.md-button.md-button--primary}

## Protecciones de Seguridad

Key components of the Android security model include [verified boot](#verified-boot), [firmware updates](#firmware-updates), and a robust [permission system](#android-permissions). These important security features form the baseline of the minimum criteria for our [mobile phone](../mobile-phones.md) and [custom Android OS](../android/distributions.md) recommendations.

### Arranque verificado

[**Verified Boot**](https://source.android.com/security/verifiedboot) is an important part of the Android security model. Proviene de protección contra ataques [evil maid](https://en.wikipedia.org/wiki/Evil_maid_attack), persistencia del malware, y se asegura que las actualizaciones de seguridad no puedan ser desactualizadas gracias a la [protección de reversión](https://source.android.com/security/verifiedboot/verified-boot#rollback-protection).

Android 10 y superior se han alejado del cifrado de disco completo por un cifrado más flexible [basado en archivos](https://source.android.com/security/encryption/file-based). Tus datos se encriptan utilizando claves de encriptación únicas, y los archivos del sistema operativo se dejan sin encriptar.

El arranque verificado garantiza la integridad de los archivos del sistema operativo, evitando así que un adversario con acceso físico pueda manipular o instalar malware en el dispositivo. En el improbable caso de que el malware pueda explotar otras partes del sistema y obtener un acceso privilegiado más alto, el arranque verificado evitará y revertirá los cambios en la partición del sistema al reiniciar el dispositivo.

Desgraciadamente, los fabricantes de equipos originales (OEM) solo están obligados a dar soporte al arranque verificado en su distribución de Android de serie. Solo unos pocos fabricantes de equipos originales, como Google, admiten la inscripción de claves AVB modificadas en sus dispositivos. Además, algunos derivados de AOSP como LineageOS o /e/ OS no admiten arranque verificado, incluso en hardware con soporte de arranque verificado para sistemas operativos de terceros. Nosotros recomendamos que compruebe la compatibilidad **antes** de comprar un nuevo dispositivo. Los derivados de AOSP que no soportan el arranque verificado **no son** recomendados.

Muchos OEMs también han roto la implementación del Arranque Verificado que tienes que conocer más allá de su marketing. Por ejemplo, los Fairphone 3 y 4 no son seguros por defecto, ya que el [bootloader de serie confía en la clave de firma pública AVB](https://forum.fairphone.com/t/bootloader-avb-keys-used-in-roms-for-fairphone-3-4/83448/11). This breaks verified boot on a stock Fairphone device, as the system will boot alternative Android operating systems (such as /e/) [without any warning](https://source.android.com/security/verifiedboot/boot-flow#locked-devices-with-custom-root-of-trust) about custom operating system usage.

### Actualizaciones de firmware

**Firmware updates** are critical for maintaining security and without them your device cannot be secure. Los fabricantes de equipos originales tienen acuerdos de asistencia con sus socios para proporcionar los componentes de código cerrado durante un periodo de asistencia limitado. Estos se detallan en los [boletines de seguridad mensuales de Android](https://source.android.com/security/bulletin).

Dado que los componentes del teléfono, como el procesador y las tecnologías de radio, dependen de componentes de código cerrado, las actualizaciones deben ser proporcionadas por los respectivos fabricantes. Por lo tanto, es importante que compres un dispositivo dentro de un ciclo de soporte activo. [Qualcomm](https://www.qualcomm.com/news/releases/2020/12/qualcomm-and-google-announce-collaboration-extend-android-os-support-and) y [Samsung](https://news.samsung.com/us/samsung-galaxy-security-extending-updates-knox) dan 4 años de soporte a sus dispositivos, mientras que los productos más baratos suelen tener ciclos de soporte más cortos. Con la introducción del [Pixel 6](https://support.google.com/pixelphone/answer/4457705), Google ahora hace su propio SoC y van a ofrecer un mínimo de 5 años de soporte. Con la introducción de la serie Pixel 8, Google aumentó esa ventana de soporte a 7 años.

Los dispositivos EOL que ya no son compatibles con el fabricante del SoC no pueden recibir actualizaciones de firmware de los proveedores OEM o de los distribuidores Android posteriores al mercado. Esto significa que los problemas de seguridad con esos dispositivos permanecerán sin solucionar.

Fairphone, por ejemplo, comercializa su dispositivo Fairphone 4 con 6 años de soporte. Sin embargo, el SoC (Qualcomm Snapdragon 750G en el Fairphone 4) tiene una fecha de caducidad considerablemente más corta. Esto significa que las actualizaciones de seguridad de firmware de Qualcomm para el Fairphone 4 terminarán en septiembre de 2023, independientemente de que Fairphone siga publicando actualizaciones de seguridad de software.

### Permisos de Android

[**Permissions on Android**](https://developer.android.com/guide/topics/permissions/overview) grant you control over what apps are allowed to access. Google regularmente hace [mejoras](https://developer.android.com/about/versions/11/privacy/permissions) en el sistema de permisos en cada versión sucesiva. Todas las aplicaciones que instales están estrictamente [aisladas](https://source.android.com/security/app-sandbox), por lo que no es necesario instalar ninguna aplicación de antivirus.

Un smartphone con la última versión de Android siempre será más seguro que un smartphone antiguo con un antivirus que hayas pagado. It's better not to pay for antivirus software and to save money to buy a new smartphone such as a [Google Pixel](../mobile-phones.md#google-pixel).

Android 10:

- [Almacenamiento Específico](https://developer.android.com/about/versions/10/privacy/changes#scoped-storage) te da más control sobre tus archivos y puede limitar lo que puede acceder al [almacenamiento externo](https://developer.android.com/training/data-storage#permissions). Las aplicaciones pueden tener un directorio específico en el almacenamiento externo, así como la capacidad de almacenar tipos específicos de archivos allí.
- Acceso más estricto a la [ubicación del dispositivo](https://developer.android.com/about/versions/10/privacy/changes?hl=es-419#app-access-device-location) introduciendo el permiso `ACCESS_BACKGROUND_LOCATION`. Esto impide que las aplicaciones accedan a la ubicación cuando se ejecutan en segundo plano sin permiso expreso del usuario.

Android 11:

- [Permisos únicos](https://developer.android.com/about/versions/11/privacy/permissions?hl=es-419#one-time) que te permite conceder un permiso a una aplicación una sola vez.
- [Restablecimiento automático de permisos](https://developer.android.com/about/versions/11/privacy/permissions?hl=es-419#auto-reset), que restablece [los permisos de tiempo de ejecución](https://developer.android.com/guide/topics/permissions/overview?hl=es-419#runtime) que se concedieron al abrir la aplicación.
- Permisos detallados para acceder a funciones relacionadas con el [número de teléfono](https://developer.android.com/about/versions/11/privacy/permissions#phone-numbers).

Android 12:

- Un permiso para conceder sólo la [ubicación aproximada](https://developer.android.com/about/versions/12/behavior-changes-12#approximate-location).
- Reinicio automático de [aplicaciones hibernadas](https://developer.android.com/about/versions/12/behavior-changes-12?hl=es-419#app-hibernation).
- [Auditoría de acceso a los datos](https://developer.android.com/about/versions/12/behavior-changes-12?hl=es-419#data-access-auditing) que facilita determinar qué parte de una aplicación está realizando un tipo específico de acceso a los datos.

Android 13:

- Un permiso para [acceso Wi-Fi cercano](https://developer.android.com/about/versions/13/behavior-changes-13#nearby-wifi-devices-permission). The MAC addresses of nearby Wi-Fi access points were a popular way for apps to track a user's location.
- Más [permisos de contenido multimedia detallados](https://developer.android.com/about/versions/13/behavior-changes-13?hl=es-419#granular-media-permissions), lo que significa que puedes conceder acceso sólo a imágenes, vídeos o archivos de audio.
- El uso en segundo plano de los sensores requiere ahora el permiso [`BODY_SENSORS`](https://developer.android.com/about/versions/13/behavior-changes-13#body-sensors-background-permission).

Una aplicación puede solicitar un permiso para una función específica que tenga. Por ejemplo, cualquier aplicación que pueda escanear códigos QR necesitará el permiso de la cámara. Algunas aplicaciones pueden solicitar más permisos de los necesarios.

[Exodus](https://exodus-privacy.eu.org) puede ser útil para comparar aplicaciones con fines similares. Si una aplicación requiere muchos permisos y tiene un montón de publicidad y analíticas, probablemente sea un mal signo. Recomendamos consultar cada uno de los rastreadores y leer sus descripciones, en lugar de limitarse a **contar el total** y asumir que todos los elementos enumerados son iguales.

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

Si una aplicación es principalmente un servicio basado en web, el seguimiento puede producirse en el lado del servidor. [Facebook](https://reports.exodus-privacy.eu.org/en/reports/com.facebook.katana/latest) no muestra "ningún rastreador", pero sin duda rastrea los intereses y el comportamiento de los usuarios en todo el sitio. Las aplicaciones pueden eludir la detección si no utilizan las bibliotecas de código estándar producidas por la industria publicitaria, aunque esto es poco probable.

</div>

<div class="admonition note" markdown>
<p class="admonition-title">Nota</p>

Las aplicaciones que respetan la privacidad como [Bitwarden](https://reports.exodus-privacy.eu.org/en/reports/com.x8bit.bitwarden/latest) pueden mostrar algunos rastreadores como [Google Firebase Analytics](https://reports.exodus-privacy.eu.org/en/trackers/49). Esta biblioteca incluye [Firebase Cloud Messaging](https://en.wikipedia.org/wiki/Firebase_Cloud_Messaging) que puede proporcionar [notificaciones push](https://es.wikipedia.org/wiki/Tecnología_push) en las aplicaciones. Este [es el caso](https://fosstodon.org/@bitwarden/109636825700482007) con Bitwarden. Esto no significa que Bitwarden utilice todas las funciones analíticas que ofrece Google Firebase Analytics.

</div>

## Funciones de Privacidad

### Perfiles de usuario

Los perfiles de usuario múltiples pueden ser encontrados en **Ajustes** → **Sistema** → **Usuarios múltiples** y son la manera más simple de aislar en Android.

Con los perfiles de usuario, puedes imponer restricciones a un perfil específico, como: realizar llamadas, usar SMS o instalar aplicaciones en el dispositivo. Cada perfil se cifra con su propia clave de cifrado y no puede acceder a los datos de ningún otro perfil. Incluso el propietario del dispositivo no puede ver los datos de otros perfiles sin conocer su contraseña. Los perfiles de usuario múltiples son un método más seguro de aislamiento.

### Perfil de trabajo

Los [perfiles de trabajo](https://support.google.com/work/android/answer/6191949) son otra manera de aislar aplicaciones individuales y pueden ser más convenientes que usar perfiles de usuario separados.

A **device controller** app such as [Shelter](../android/general-apps.md#shelter) is required to create a Work Profile without an enterprise MDM, unless you're using a custom Android OS which includes one.

El perfil de trabajo depende de un controlador de dispositivo para funcionar. Características como el *transbordador de archivos* y el *bloqueo de búsqueda de contactos* o cualquier tipo de característica de aislamiento debe ser implementada por el controlador. También debes confiar plenamente en la aplicación del controlador del dispositivo, ya que tiene acceso total a tus datos dentro del perfil de trabajo.

Este método es generalmente menos seguro que un perfil de usuario secundario; sin embargo, le permite la comodidad de ejecutar aplicaciones tanto en el trabajo y perfiles personales simultáneamente.

### "Killswitch" de un VPN

Android 7 y superiores admiten un interruptor de corte de VPN (VPN kill switch), y está disponible sin necesidad de instalar aplicaciones de terceros. Esta función puede evitar fugas si la VPN está desconectada. Se puede encontrar en :gear: **Ajustes** → **Red e internet** → **VPN** → :gear: → **Bloquear conexiones sin VPN**.

### Cambios globales

Los dispositivos Android modernos tienen interruptores globales para desactivar los servicios de Bluetooth y de localización. Android 12 introdujo interruptores para la cámara y el micrófono. Cuando no estén en uso, recomendamos desactivar estas funciones. Apps cannot use disabled features (even if granted individual permissions) until re-enabled.

## Servicios de Google

If you are using a device with Google services—whether with the stock operating system or an operating system that safely sandboxes Google Play Services like GrapheneOS—there are a number of additional changes you can make to improve your privacy. Seguimos recomendando evitar los servicios de Google por completo, o limitar los servicios de Google Play a un perfil específico de usuario/trabajo combinando un controlador de dispositivo como *Shelter* con Google Play aislado de GrapheneOS.

### Programa de Protección Avanzada

Si tienes una cuenta de Google sugerimos que te inscribas en el [Programa de Protección Avanzada](https://landing.google.com/advancedprotection). Está disponible sin costo a cualquiera que tenga dos o más llaves de seguridad de hardware con soporte para [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online). Alternatively, you can use [passkeys](https://fidoalliance.org/passkeys).

El Programa de Protección Avanzada proporciona una supervisión de amenazas mejorada y permite:

- Autenticación de dos factores más estricta; por ejemplo, [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online) **debe** utilizarse y se prohíbe el uso de [OTP por SMS](../basics/multi-factor-authentication.md#sms-or-email-mfa), [TOTP](../basics/multi-factor-authentication.md#time-based-one-time-password-totp) y [OAuth](https://en.wikipedia.org/wiki/OAuth)
- Solo las aplicaciones de Google y de terceros verificadas pueden acceder a los datos de la cuenta
- Escaneo de correos electrónicos inminentes en las cuentas de Gmail contra los intentos de [phishing](https://es.wikipedia.org/wiki/Phishing#T%C3%A9cnicas_de_phishing)
- [Escaneo de navegador seguro](https://google.com/chrome/privacy/whitepaper.html#malware) más estricto con Google Chrome
- Proceso de recuperación más estricto para cuentas con credenciales perdidas

 Si usas los servicios de Google Play no aislados (común en los sistemas operativos por defecto), el Programa de Protección Avanzada también viene con [beneficios adicionales](https://support.google.com/accounts/answer/9764949) como:

- No permitir la instalación de aplicaciones fuera de Google Play Store, la tienda de aplicaciones del proveedor del sistema operativo o a través de [`adb`](https://en.wikipedia.org/wiki/Android_Debug_Bridge)
- Escaneo automático obligatorio de dispositivos con [Play Protect](https://support.google.com/googleplay/answer/2812853?#zippy=%2Chow-malware-protection-works%2Chow-privacy-alerts-work)
- Advertencia sobre aplicaciones no verificadas

### Actualizaciones del sistema de Google Play

En el pasado, las actualizaciones de seguridad de Android tenían que ser enviadas por el proveedor del sistema operativo. Android se ha vuelto más modular a partir de Android 10, y Google puede impulsar las actualizaciones de seguridad para **algunos** componentes del sistema vía los servicios de Google Play privilegiados.

Si tienes un dispositivo EOL (end-of-life) incluido con Android 10 o superior y no puedes ejecutar ninguno de nuestros sistemas operativos recomendados en tu dispositivo, es probable que te resulte mejor seguir con tu instalación de Android OEM (a diferencia de un sistema operativo que no aparece aquí, como LineageOS o /e/ OS). Esto te permitirá recibir **algunos** arreglos de seguridad de Google, mientras que no viola el modelo de seguridad de Android al usar un derivado de Android inseguro y aumentando tu superficie de ataque. Aún así, te recomendamos que actualices a un dispositivo compatible lo antes posible.

### ID de publicidad

Todos los dispositivos con Google Play Services instalado automáticamente generan un [ID de publicidad](https://support.google.com/googleplay/android-developer/answer/6048248) usado para la publicidad dirigida. Deshabilite esta función para limitar los datos recopilados sobre usted.

En las distribuciones de Android con los [servicios de Google Play aislados](https://grapheneos.org/usage#sandboxed-google-play), ve a :gear: **Ajustes** → **Aplicaciones** → **Google Play aislado** → **Ajustes de Google** → **Anuncios**, y selecciona *Eliminar el ID de publicidad*.

En las distribuciones de Android con servicios privilegiados de Google Play (como los sistemas operativos de serie), la configuración puede estar en una de varias ubicaciones. Revisa

- :gear: **Ajustes** → **Google** → **Anuncios**
- :gear: **Ajustes** → **Privacidad** → **Anuncios**

You will either be given the option to delete your advertising ID or to *Opt out of interest-based ads* (this varies between OEM distributions of Android). If presented with the option to delete the advertising ID, that is preferred. Si no es así, asegúrate de optar por no participar y restablecer tu ID de publicidad.

### SafetyNet y Play Integrity API

[SafetyNet](https://developer.android.com/training/safetynet/attestation) y el [Play Integrity APIs](https://developer.android.com/google/play/integrity) son generalmente usados para [aplicaciones bancarias](https://grapheneos.org/usage#banking-apps). Muchas aplicaciones bancarias funcionarán bien en GrapheneOS con los servicios de Google Play aislados, sin embargo, algunas aplicaciones no financieras tienen sus propios mecanismos anti-manipulación que pueden fallar. GrapheneOS pasa con éxito el chequeo `basicIntegrity`, pero no el check de certificación `ctsProfileMatch`. Los dispositivos con Android 8 o posterior tienen soporte de certificación de hardware que no se puede omitir sin claves filtradas o vulnerabilidades graves.

En cuanto a Google Wallet, no lo recomendamos debido a su [política de privacidad](https://payments.google.com/payments/apis-secure/get_legal_document?ldo=0&ldt=privacynotice&ldl=en), que establece que debes no participar si no quieres que tu calificación crediticia y tu información personal se compartan con servicios de marketing de afiliación.
