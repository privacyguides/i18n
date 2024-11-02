---
title: Resumen de iOS
icon: simple/apple
description: iOS es un sistema operativo móvil desarrollado por Apple para el iPhone.
---

**iOS** y **iPadOS** son sistemas operativos móviles patentados desarrollados por Apple para sus productos iPhone y iPad, respectivamente. Si tienes un dispositivo móvil de Apple, puedes aumentar tu privacidad desactivando algunas funciones de telemetría integradas y reforzando algunos ajustes de privacidad y seguridad integrados en el sistema.

## Notas de Privacidad

Los dispositivos iOS suelen ser elogiados por los expertos en seguridad por su sólida protección de datos y su adhesión a las mejores prácticas modernas. Sin embargo, el carácter restrictivo del ecosistema de Apple -especialmente con sus dispositivos móviles- sigue obstaculizando la privacidad de varias maneras.

En general, consideramos que iOS ofrece una protección de la privacidad y la seguridad mejor que la media para la mayoría de la gente, en comparación con los dispositivos Android de serie de cualquier fabricante. However, you can achieve even higher standards of privacy with a [custom Android operating system](../android/distributions.md) like GrapheneOS, if you want or need to be completely independent of Apple or Google's cloud services.

### Bloqueo de Activación

Todos los dispositivos iOS deben ser verificados contra los servidores de bloqueo de activación de la aplicación cuando se configuran o se restablecen por primera vez, lo que significa que es **necesaria** una conexión a Internet para utilizar un dispositivo iOS.

### App Store Obligatoria

The only source for apps on iOS is Apple's App Store, which requires an Apple Account to access. Esto significa que Apple tiene un registro de todas las aplicaciones que instalas en tu dispositivo, y es probable que pueda relacionar esa información con tu identidad real si proporcionas a la App Store un método de pago.

### Telemetría Invasiva

Apple ha tenido históricamente problemas para anonimizar correctamente su telemetría en iOS. [En 2019](https://theguardian.com/technology/2019/jul/26/apple-contractors-regularly-hear-confidential-details-on-siri-recordings), se descubrió que Apple transmitía grabaciones de Siri, algunas con información altamente confidencial, a sus servidores para que terceros contratistas las revisaran manualmente. Aunque detuvieron temporalmente ese programa después de que se [informara ampliamente de](https://theverge.com/2019/8/23/20830120/apple-contractors-siri-recordings-listening-1000-a-day-globetech-microsoft-cortana) esa práctica, el problema no se resolvió por completo [hasta 2021](https://theguardian.com/technology/2021/jun/07/apple-overhauls-siri-to-address-privacy-concerns-and-improve-performance).

Recientemente, se ha descubierto que Apple [transmite datos analíticos incluso cuando el envío de datos analíticos se encuentra desactivado](https://gizmodo.com/apple-iphone-analytics-tracking-even-when-off-app-store-1849757558) en iOS, y esta información [parece](https://twitter.com/mysk_co/status/1594515229915979776) estar fácilmente vinculados a identificadores de cuenta únicos de iCloud, a pesar de ser supuestamente anónimos.

## Configuración Recomendada

**Note:** This guide assumes that you're running the latest version of iOS.

### iCloud

La mayoría de los problemas de privacidad y seguridad de los productos de Apple están relacionados con sus servicios en la nube, no con su hardware o software. Cuando utilizas servicios de Apple como iCloud, la mayor parte de tu información se almacena en sus servidores y se protege con claves a las que Apple tiene acceso por defecto. Puedes consultar la [documentación de Apple](https://support.apple.com/HT202303) para saber qué servicios están cifrados de extremo a extremo. Todo lo que aparezca como "in transit" o "on server" significa que es posible que Apple acceda a esos datos sin tu permiso. En ocasiones, las fuerzas de seguridad han abusado de este nivel de acceso para eludir el hecho de que tus datos están cifrados de forma segura en tu dispositivo y, por supuesto, Apple es vulnerable a las filtraciones de datos como cualquier otra empresa.

Por lo tanto, si utilizas iCloud, deberías [activar **Protección de Datos Avanzada**](https://support.apple.com/HT212520). Esto encripta casi todos tus datos de iCloud con claves almacenadas en tus dispositivos (encriptación de extremo a extremo), en lugar de en los servidores de Apple, de modo que tus datos de iCloud están protegidos en caso de violación de datos y, por lo demás, ocultos a Apple.

El cifrado utilizado por la Protección de Datos Avanzada, aunque potente, [no es ** tan robusta](https://discuss.privacyguides.net/t/apple-advances-user-security-with-powerful-new-data-protections/10778/4) como el cifrado ofrecido por otros [servicios en la nube](../cloud.md), especialmente cuando se trata de iCloud Drive. Aunque recomendamos encarecidamente el uso de la Protección de Datos Avanzada si utilizas iCloud, también sugeriríamos considerar la búsqueda de una alternativa a iCloud de un [proveedor de servicios más centrado en la privacidad](../tools.md), aunque es poco probable que la mayoría de la gente se vea afectada por estas peculiaridades de cifrado.

También puedes proteger tus datos limitando lo que sincronizas con iCloud. En la parte superior de la aplicación **Ajustes**, verás tu nombre y tu foto de perfil si has iniciado sesión en iCloud. Selecciónalo, luego **iCloud**, y desactiva los interruptores de los servicios que no quieras sincronizar con iCloud. Es posible que veas aplicaciones de terceros en **Mostrar Todo** si se sincronizan con iCloud, que puedes desactivarlas aquí.

#### iCloud+

Una suscripción de pago a **iCloud+** (con cualquier plan de almacenamiento de iCloud) incluye algunas funciones de protección de la privacidad. Si bien pueden ofrecer un servicio adecuado a los clientes actuales de iCloud, no recomendaríamos adquirir un plan iCloud+ en lugar de una [VPN ](../vpn.md) y un [servicio independiente de alias de correo electrónico](../email-aliasing.md) solo por estas funciones.

[**Relay Privado**](https://apple.com/legal/privacy/data/en/icloud-relay) es un servicio proxy que retransmite todo tu tráfico de Safari, tus consultas DNS y el tráfico no cifrado de tu dispositivo a través de dos servidores: uno propiedad de Apple y otro de un proveedor externo (incluidos Akamai, Cloudflare y Fastly). En teoría, esto debería impedir que cualquier proveedor de la cadena -incluido Apple- tenga plena visibilidad de los sitios web que visitas mientras estás conectado. A diferencia de una VPN, el Relay Privado no protege el tráfico que ya está cifrado.

**Ocultar Mi Correo Electrónico** es el servicio de alias de correo electrónico de Apple. Puede crear un alias de correo electrónico de forma gratuita al *Iniciar sesión con Apple* en un sitio web o una aplicación, o generar alias ilimitados bajo demanda con un plan iCloud+ de pago. Ocultar Mi Correo Electrónico tiene la ventaja de utilizar el dominio `@icloud.com` para sus alias, que puede ser menos susceptible de ser bloqueado en comparación con otros servicios de alias de correo electrónico, pero no ofrece la funcionalidad que ofrecen los servicios independientes, como el cifrado PGP automático o la compatibilidad con múltiples buzones de correo.

#### Contenido y Compras

At the top of the **Settings** app, you'll see your name and profile picture if you are signed in to an Apple Account. Select that, then select **Media & Purchases** → **View Account**.

- [ ] Desactiva **Recomendaciones Personalizadas**

#### Buscar

**Buscar** es un servicio que te permite rastrear tus dispositivos Apple y compartir tu ubicación con tus amigos y familiares. También te permite borrar el dispositivo a distancia en caso de robo, evitando que un ladrón acceda a tus datos. Tus [datos de localización de Buscar son E2EE](https://apple.com/legal/privacy/data/en/find-my) cuando:

- Tu localización se comparte con un familiar o amigo, y ambos utilizáis iOS 17 o superior.
- Tu dispositivo está desconectado y es localizado por la red Buscar.

Tus datos de localización no son E2EE cuando tu dispositivo está conectado y utilizas Buscar iPhone remotamente para localizar tu dispositivo. Tendrá que decidir si estas ventajas compensan los beneficios antirrobo del Bloqueo de Activación.

At the top of the **Settings** app, you'll see your name and profile picture if you are signed in to an Apple Account. Selecciónelo y, a continuación, selecciona **Buscar**. Aquí puedes elegir si quieres activar o desactivar las funciones de localización de Buscar.

### Ajustes

Muchos otros ajustes relacionados con la privacidad se pueden encontrar en la aplicación **Ajustes**.

#### Modo Avión

Activar el **Modo Avión**, evita que tu teléfono entre en contacto con las torres de telefonía móvil. Seguirás pudiendo conectarte al Wi-Fi y Bluetooth, así que siempre que estés conectado al Wi-Fi puedes activar este ajuste.

#### Wi-Fi

You can enable [hardware address randomization](https://support.apple.com/en-us/102509#triswitch) to protect you from tracking across Wi-Fi networks, and on the same network over time. On the network you are currently connected to, tap the :material-information: button:

- [x] Set **Private Wi-Fi Address** to **Fixed** or **Rotating**

También tienes la opción de **Limitar rastreo de dirección IP**. Esto es similar a iCloud Private Relay pero sólo afecta a las conexiones con "rastreadores conocidos". Dado que sólo afecta a las conexiones con servidores potencialmente maliciosos, probablemente esté bien dejar activada esta opción, pero si no quieres que enrute *ningún* tráfico a través de los servidores de Apple, deberías desactivarla.

#### Bluetooth

**Bluetooth** debe estar desactivado cuando no se esté utilizando, ya que aumenta la superficie de ataque. Desactivar el Bluetooth (o Wi-Fi) a través del Centro de Control sólo lo desactiva temporalmente: debes desactivarlo en Ajustes para que el efecto de la desactivación se mantenga.

- [ ] Desactiva **Bluetooth**

Note that Bluetooth is automatically turned on after every system update.

#### General

El nombre de dispositivo de tu iPhone contendrá por defecto tu nombre de pila, y éste será visible para cualquiera en las redes a las que te conectes. Deberías cambiarlo por algo más genérico, como "iPhone". Select **About** → **Name** and enter the device name you prefer.

Es importante instalar con frecuencia **Actualizaciones de Software** para obtener las últimas correcciones de seguridad. Puedes activar **Actualizaciones Automáticas** para mantener tu teléfono al día sin necesidad de buscar actualizaciones constantemente. Select **Software Update** → **Automatic Updates**:

- [x] Activa **Descargar Actualizaciones de iOS**
- [x] Activa **Instalar Actualizaciones de iOS**
- [x] Activa **Respuestas de Seguridad y Archivos del Sistema**

**AirDrop** te permite transferir archivos fácilmente, pero puede permitir que extraños te envíen archivos que no deseas.

- [x] Select **AirDrop** → **Receiving Off**

**AirPlay** te permite transmitir sin interrupciones contenidos desde tu iPhone a un televisor; sin embargo, es posible que no siempre quieras hacerlo. Select **AirPlay & Continuity** → **Automatically AirPlay**:

- [x] Selecciona **Nunca** o **Preguntar**

**Actualización en Segundo Plano** permite que tus aplicaciones actualicen su contenido mientras no las estás utilizando. Esto puede provocar que realicen conexiones no deseadas. Turning this off can also save battery life, but may affect an app's ability to receive updated information, particularly weather and messaging apps.

Selecciona **Actualización en Segundo Plano** y desactiva las aplicaciones que no quieras que sigan actualizándose en segundo plano. Si no quieres que ninguna aplicación se actualice en segundo plano, puedes volver a seleccionar **Actualización en Segundo Plano** y **desactivarla **.

#### Siri y Buscar

Si no quieres que nadie pueda controlar tu teléfono con Siri cuando está bloqueado, puedes desactivarlo aquí.

- [ ] Desactiva **Siri con Pantalla de Bloqueo**

#### Face ID/Touch ID y Código

Establecer una contraseña segura en tu teléfono es el paso más importante que puedes dar para la seguridad física del dispositivo. Tendrás que elegir entre seguridad y comodidad: Una contraseña más larga será molesta de escribir cada vez, pero una contraseña más corta o un PIN serán más fáciles de adivinar. Configurar Face ID o Touch ID junto con una contraseña segura puede ser un buen compromiso entre usabilidad y seguridad.

Select **Turn Passcode On** or **Change Passcode** → **Passcode Options** → **Custom Alphanumeric Code**. Asegúrate de crear una [contraseña segura](../basics/passwords-overview.md).

Si deseas utilizar Face ID o Touch ID, puedes seguir adelante y configurarlo ahora. Tu teléfono utilizará la contraseña que configuraste anteriormente como alternativa en caso de que falle la verificación biométrica. Los métodos de desbloqueo biométrico son ante todo una ventaja, aunque impiden que las cámaras de vigilancia o las personas por encima de su hombro te vean introducir el código.

Si utilizas datos biométricos, debes saber cómo desactivarlos rápidamente en caso de emergencia. Si mantienes pulsado el botón lateral o de encendido y *o* el botón de volumen hasta que veas el control deslizante para Apagar, se desactivará la biometría y tendrás que introducir el código para desbloquear. El código también será necesario después de reiniciar el dispositivo.

On some older devices, you may have to press the power button five times to disable biometrics instead, or for devices with Touch ID, you may just have to hold down the power button and nothing else. Asegúrate de probarlo con antelación para saber qué método funciona con tu dispositivo.

**Stolen Device Protection** adds additional security intended to protect your personal data if your device is stolen while unlocked. If you use biometrics and the Find My Device feature in your Apple Account settings, we recommend enabling this new protection:

- [x] Selecciona **Activar Protección**

Después de activar la Protección en Caso de Robo, [ciertas acciones](https://support.apple.com/HT212510) requerirán autenticación biométrica sin una contraseña de respaldo (en el caso de que un "shoulder surfer" haya obtenido tu PIN), como el uso de autorrelleno de contraseña, el acceso a información de pago y la desactivación del Modo Perdido. It also adds a security delay to certain actions performed away from your home or another "familiar location," such as requiring a 1-hour timer to reset your Apple Account password or sign out of your Apple Account. Este retraso pretende darte tiempo para activar el Modo Perdido y asegurar tu cuenta antes de que un ladrón pueda reiniciar tu dispositivo.

**Permitir Acceso al Estar Bloqueado** te da opciones para lo que puedes permitir cuando tu teléfono está bloqueado. Cuantas más de estas opciones deshabilites, menos podrá hacer alguien sin tu contraseña, pero menos cómodo será para ti. Elige a cuáles de ellos no quieres que alguien tenga acceso si llega a poner sus manos en tu teléfono.

- [ ] Desactiva **Visualización Hoy y Búsqueda**
- [ ] Desactiva **Centro de Notificaciones**
- [ ] Desactiva **Centro de Control**
- [ ] Desactiva **Widgets (pantalla bloqueada)**
- [ ] Desactiva **Siri**
- [ ] Desactiva **Responder con Mensaje**
- [ ] Desactiva **Control de Casa**
- [ ] Desactiva **Cartera**
- [ ] Desactiva **Devolver Llamadas Perdidas**
- [ ] Desactiva **Accesorios USB**

Los iPhones ya son resistentes a los ataques de fuerza bruta, ya que te hacen esperar largos periodos de tiempo después de varios intentos fallidos; sin embargo, históricamente ha habido exploits para sortear esto. Para mayor seguridad, puedes configurar tu teléfono para que se borre automáticamente después de 10 intentos fallidos.

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

Con esta opción activada, alguien podría borrar intencionadamente tu teléfono introduciendo muchas veces una contraseña incorrecta. Asegúrate de tener copias de seguridad adecuadas y activa esta configuración sólo si te sientes cómodo con ella.

</div>

- [x] Activa **Borrar Datos**

#### Privacidad y seguridad

**Localización** te permite utilizar funciones como Buscar y Mapas. Si no necesitas estas funciones, puedes desactivar Localización. Alternativamente, puede revisar y elegir qué aplicaciones pueden usar tu ubicación aquí. Selecciona **Localización**:

- [ ] Desactiva **Localización**

Aparecerá una flecha morada junto a una aplicación en estos ajustes que haya utilizado tu ubicación recientemente, mientras que una flecha gris indica que se ha accedido a tu ubicación en las últimas 24 horas. Si decides dejar activada la Localización, Apple la utilizará por defecto para los Servicios del Sistema. Aquí puede revisar y elegir qué servicios pueden utilizar tu localización. Sin embargo, si no quieres enviar análisis de localización a Apple, que utilizan para mejorar Mapas, también puedes desactivar esta opción. Selecciona **Servicios del Sistema**:

- [ ] Desactiva **Análisis de iPhone**
- [ ] Desactiva **Enrutamiento y Tráfico**
- [ ] Desactiva **Mejorar Mapas**

Aquí puedes decidir si permites que las aplicaciones soliciten **rastrearte**. Desactivar esta opción impide que todas las aplicaciones te rastreen con el ID de publicidad de tu teléfono. Selecciona **Rastreo**:

- [ ] Desactiva **Permitir que las Apps Soliciten Rastrearte**

Esta opción está desactivada por defecto y no puede modificarse para usuarios menores de 18 años.

Deberías desactivar **Datos de Uso y de los Sensores** si no deseas participar en estudios. Selecciona **Datos de Uso y de los Sensores**:

- [ ] Desactiva **Datos de Uso y de los Sensores**

**Comprobación de Seguridad** te permite ver y revocar rápidamente a determinadas personas y aplicaciones que podrían tener permiso para acceder a tus datos. Aquí puedes realizar un **Restablecimiento de Emergencia**, restableciendo inmediatamente los permisos para todas las personas y aplicaciones que puedan tener acceso a los recursos del dispositivo. También puedes **Gestionar Accesos y Datos Compartidos** que te permite revisar y personalizar quién y qué tiene acceso a tu dispositivo y a los recursos de tu cuenta.

Deberías desactivar los análisis si no deseas enviar datos de uso a Apple. Selecciona **Análisis y Mejoras**:

- [ ] Desactiva **Compartir Análisis (iPhone)** o **Compartir Análisis (iPhone y Apple Watch)**
- [ ] Desactiva **Compartir Análisis (iCloud)**
- [ ] Desactiva **Mejorar Fitness++**
- [ ] Desactiva **Mejorar Seguridad**
- [ ] Desactiva **Mejorar Siri y Dictado**
- [ ] Turn off **Improve Assistive Voice Features**
- [ ] Turn off **Improve AR Location Accuracy**

Desactiva **Anuncios Personalizados** si no quieres anuncios personalizados. Selecciona **Publicidad de Apple**:

- [ ] Desactiva **Anuncios Personalizados**

**Informe de Privacidad de las Apps** es una herramienta integrada que te permite ver qué permisos utilizan tus aplicaciones. Selecciona **Informe de Privacidad de las Apps**:

- [x] Selecciona **Activar el Informe de Privacidad de las Apps**

[Modo de Aislamiento](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode) es un ajuste de seguridad que puedes activar para que tu teléfono sea más resistente a los ataques. Ten en cuenta que algunas aplicaciones y funciones [no funcionarán](https://support.apple.com/HT212650) como lo hacen normalmente.

- [x] Selecciona **Activar el Modo de Aislamiento**

## Consejo Adicional

### Llamadas E2EE

Las llamadas telefónicas normales realizadas con la aplicación Teléfono a través de tu operador no son E2EE. Both FaceTime Video and FaceTime Audio calls are E2EE. Alternatively, you can use [another app](../real-time-communication.md) like Signal for E2EE calls.

### iMessage Encriptado

The [color of the message bubble](https://support.apple.com/en-us/104972) in the Messages app indicates whether your messages are E2EE or not. A blue bubble indicates that you're using iMessage with E2EE, while a green bubble indicates the other party is using either the outdated SMS and MMS protocols or RCS. RCS on iOS is **not** E2EE. Currently, the only way to have E2EE in Messages is for both parties to be using iMessage on Apple devices.

Si tú o tu compañero de mensajería tenéis activada la Copia de Seguridad de iCloud sin Protección de Datos Avanzada, la clave de cifrado se almacenará en los servidores de Apple, lo que significa que podrán acceder a tus mensajes. Additionally, iMessage's key exchange is not as secure as alternative implementations like Signal's (which allows you to view the recipients key and verify by QR code), so it shouldn't be relied on for particularly sensitive communications.

### Photo Permissions

When an app prompts you for access to your device's photo library, iOS provides you with options to limit what an app can access.

Rather than allow an app to access all the photos on your device, you can allow it to only access whichever photos you choose by tapping the "Select Photos..." option in the permission dialog. You can change photo access permissions at any time by navigating to **Settings** → **Privacy & Security** → **Photos**.

![Photo Permissions](../assets/img/ios/photo-permissions-light.png#only-light) ![Photo Permissions](../assets/img/ios/photo-permissions-dark.png#only-dark)

**Add Photos Only** is a permission that only gives an app the ability to download photos to the photo library. Not all apps which request photo library access provide this option.

![Private Access](../assets/img/ios/private-access-light.png#only-light) ![Private Access](../assets/img/ios/private-access-dark.png#only-dark)

Some apps also support **Private Access**, which functions similarly to the **Limited Access** permission. However, photos shared to apps using Private Access include their location by default. We recommend unchecking this setting if you do not [remove photo metadata](../data-redaction.md) beforehand.

### Contact Permissions

Similarly, rather than allow an app to access all the contacts saved on your device, you can allow it to only access whichever contacts you choose. You can change contact access permissions at any time by navigating to **Settings** → **Privacy & Security** → **Contacts**.

![Contact Permissions](../assets/img/ios/contact-permissions-light.png#only-light) ![Contact Permissions](../assets/img/ios/contact-permissions-dark.png#only-dark)

### Require Biometrics and Hide Apps

iOS offers the ability to lock most apps behind Touch ID/Face ID or your passcode, which can be useful for protecting sensitive content in apps which do not provide the option themselves. You can lock an app by long-pressing on it and selecting **Require Face ID/Touch ID**. Any app locked in this way requires biometric authentication whenever opening it or accessing its contents in other apps. Also, notification previews for locked apps will not be shown.

In addition to locking apps behind biometrics, you can also hide apps so that they don't appear on the Home Screen, App Library, the app list in **Settings**, etc. While hiding apps may be useful in situations where you have to hand your unlocked phone to someone else, the concealment provided by the feature is not absolute, as a hidden app is still visible in some places such as the battery usage list. Moreover, one notable tradeoff of hiding an app is that you will not receive any of its notifications.

You can hide an app by long-pressing on it and selecting **Require Face ID/Touch ID** → **Hide and Require Face ID/Touch ID**. Note that pre-installed Apple apps, as well as the default web browser and email app, cannot be hidden. Hidden apps reside in a **Hidden** folder at the bottom of the App Library, which can be unlocked using biometrics. This folder appears in the App Library whether you hid any apps or not, which provides you a degree of plausible deniability.

### Ocultar Caras/Información

If you need to hide information in a photo, you can use Apple's built-in editing tools to do so.

- Open the **Photos** app and tap the photo you have selected for redaction
- Tap the :material-tune: (at the bottom of the screen) → markup symbol (top right) → plus icon at the bottom right
- Select **Add Shape** and choose the square or circle
- On the toolbar, tap the circle (left-most option) and choose black as the color for filling in the shape. You can also move the shape and increase its size as you see fit.

**Don't** use the highlighter to obfuscate information, as its opacity is not quite 100%.

### Evita el Jailbreaking

El jailbreaking en un iPhone socava su seguridad y te hace vulnerable. Ejecutar software de terceros que no sea de confianza podría infectar tu dispositivo con malware.

### Betas de iOS

Apple siempre pone las versiones beta de iOS a disposición de quienes deseen ayudar a encontrar y notificar errores. No recomendamos instalar software beta en tu teléfono. Las versiones beta son potencialmente inestables y podrían tener vulnerabilidades de seguridad no descubiertas.

## Aspectos Destacados de Seguridad

### Antes del Primer Desbloqueo

If your threat model includes [:material-target-account: Targeted Attacks](../basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red} that involve forensic tools, and you want to minimize the chance of exploits being used to access your phone, you should restart your device frequently. El estado *después de* un reinicio pero *antes de* desbloquear tu dispositivo se conoce como "Antes del Primer Desbloqueo" (BFU), y cuando tu dispositivo está en ese estado hace que sea [significativamente más difícil](https://belkasoft.com/checkm8_glossary) para las herramientas forenses explotar vulnerabilidades para acceder a tus datos. Este estado BFU te permite recibir notificaciones de llamadas, mensajes de texto y alarmas, pero la mayoría de los datos de tu dispositivo siguen estando encriptados y son inaccesibles. Esto puede ser poco práctico, así que considera si estas soluciones tienen sentido para tu situación.
