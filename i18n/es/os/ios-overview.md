---
title: Vista general de iOS
icon: simple/apple
description: iOS es un sistema operativo móvil desarrollado por Apple para el iPhone.
---

**iOS** y **iPadOS** son sistemas operativos móviles patentados desarrollados por Apple para sus productos iPhone y iPad, respectivamente. Si tienes un dispositivo móvil de Apple, puedes aumentar tu privacidad desactivando algunas funciones de telemetría integradas y reforzando algunos ajustes de privacidad y seguridad integrados en el sistema.

## Notas de Privacidad

Los dispositivos iOS suelen ser elogiados por los expertos en seguridad por su sólida protección de datos y su adhesión a las mejores prácticas modernas. Sin embargo, el carácter restrictivo del ecosistema de Apple -especialmente con sus dispositivos móviles- sigue obstaculizando la privacidad de varias maneras.

En general, consideramos que iOS ofrece una protección de la privacidad y la seguridad mejor que la media para la mayoría de la gente, en comparación con los dispositivos Android de serie de cualquier fabricante. Sin embargo, puedes alcanzar estándares de privacidad aún más altos con un [sistema operativo Android personalizado](../android.md) como GrapheneOS, si quieres o necesitas ser completamente independiente de los servicios en la nube de Apple o Google.

### Bloqueo de Activación

Todos los dispositivos iOS deben ser verificados contra los servidores de bloqueo de activación de la aplicación cuando se configuran o se restablecen por primera vez, lo que significa que es **necesaria** una conexión a Internet para utilizar un dispositivo iOS.

### App Store Obligatoria

La única fuente de aplicaciones en iOS es la App Store de Apple, que requiere un ID de Apple para acceder. Esto significa que Apple tiene un registro de todas las aplicaciones que instalas en tu dispositivo, y es probable que pueda relacionar esa información con tu identidad real si proporcionas a la App Store un método de pago.

### Telemetría Invasiva

Apple ha tenido históricamente problemas para anonimizar correctamente su telemetría en iOS. [En 2019](https://www.theguardian.com/technology/2019/jul/26/apple-contractors-regularly-hear-confidential-details-on-siri-recordings), se descubrió que Apple transmitía grabaciones de Siri -algunas con información altamente confidencial- a sus servidores para que terceros contratistas las revisaran manualmente. Aunque detuvieron temporalmente ese programa después de que se [informara ampliamente](https://www.theverge.com/2019/8/23/20830120/apple-contractors-siri-recordings-listening-1000-a-day-globetech-microsoft-cortana) de esa práctica, el problema no se resolvió por completo [hasta 2021](https://www.theguardian.com/technology/2021/jun/07/apple-overhauls-siri-to-address-privacy-concerns-and-improve-performance).

Más recientemente, se ha descubierto que Apple [transmite datos analíticos incluso cuando el uso compartido de datos analíticos está desactivado](https://gizmodo.com/apple-iphone-analytics-tracking-even-when-off-app-store-1849757558) en iOS, y estos datos [parecen](https://twitter.com/mysk_co/status/1594515229915979776) ser fácilmente vinculados a identificadores de cuenta únicos de iCloud a pesar de ser supuestamente anónimos. Apple no ha solucionado [estos problemas](https://gizmodo.com/clarence-thomas-aide-venmo-laywers-supreme-court-1850631585) hasta la fecha actual, julio de 2023.

## Configuración Recomendada

### iCloud

La mayoría de los problemas de privacidad y seguridad de los productos de Apple están relacionados con sus servicios en la nube, no con su hardware o software. Cuando utilizas servicios de Apple como iCloud, la mayor parte de tu información se almacena en sus servidores y se protege con claves a las que Apple tiene acceso por defecto. Puedes consultar la [documentación de Apple](https://support.apple.com/HT202303) para saber qué servicios están cifrados de extremo a extremo. Todo lo que aparezca como "in transit" o "on server" significa que es posible que Apple acceda a esos datos sin tu permiso. En ocasiones, las fuerzas de seguridad han abusado de este nivel de acceso para eludir el hecho de que tus datos están cifrados de forma segura en tu dispositivo y, por supuesto, Apple es vulnerable a las filtraciones de datos como cualquier otra empresa.

Por lo tanto, si utilizas iCloud, deberías [activar **Protección de Datos Avanzada**](https://support.apple.com/HT212520). Esto encripta casi todos tus datos de iCloud con claves almacenadas en tus dispositivos (encriptación de extremo a extremo), en lugar de en los servidores de Apple, de modo que tus datos de iCloud están protegidos en caso de violación de datos y, por lo demás, ocultos a Apple.

El cifrado utilizado por la Protección de Datos Avanzada, aunque potente, [no es ** tan robusta](https://discuss.privacyguides.net/t/apple-advances-user-security-with-powerful-new-data-protections/10778/4) como el cifrado ofrecido por otros [servicios en la nube](../cloud.md), especialmente cuando se trata de iCloud Drive. Aunque recomendamos encarecidamente el uso de la Protección de Datos Avanzada si utilizas iCloud, también sugeriríamos considerar la búsqueda de una alternativa a iCloud de un [proveedor de servicios más centrado en la privacidad](../tools.md), aunque es poco probable que la mayoría de la gente se vea afectada por estas peculiaridades de cifrado.

También puedes proteger tus datos limitando lo que sincronizas con iCloud. En la parte superior de la aplicación **Ajustes**, verás tu nombre y tu foto de perfil si has iniciado sesión en iCloud. Selecciónalo, luego **iCloud**, y desactiva los interruptores de los servicios que no quieras sincronizar con iCloud. Es posible que veas aplicaciones de terceros en **Mostrar Todo** si se sincronizan con iCloud, que puedes desactivarlas aquí.

#### iCloud+

Una suscripción de pago a **iCloud+** (con cualquier plan de almacenamiento de iCloud) incluye algunas funciones de protección de la privacidad. Si bien pueden ofrecer un servicio adecuado a los clientes actuales de iCloud, no recomendaríamos adquirir un plan iCloud+ en lugar de una [VPN ](../vpn.md) y un [servicio independiente de alias de correo electrónico](../email.md#email-aliasing-services) sólo por estas funciones.

**Relay Privado** es un servicio proxy que retransmite tu tráfico de Safari a través de dos servidores: uno propiedad de Apple y otro de un proveedor externo (incluyendo Akamai, Cloudflare y Fastly). En teoría, esto debería impedir que cualquier proveedor de la cadena -incluido Apple- tenga plena visibilidad de los sitios web que visitas mientras estás conectado. A diferencia de una VPN completa, el Relay Privado no protege el tráfico de tus aplicaciones fuera de Safari.

**Ocultar Mi Correo Electrónico** es el servicio de alias de correo electrónico de Apple. Puede crear un alias de correo electrónico de forma gratuita al *Iniciar sesión con Apple* en un sitio web o una aplicación, o generar alias ilimitados bajo demanda con un plan iCloud+ de pago. Ocultar Mi Correo Electrónico tiene la ventaja de utilizar el dominio `@icloud.com` para sus alias, que puede ser menos susceptible de ser bloqueado en comparación con otros servicios de alias de correo electrónico, pero no ofrece la funcionalidad que ofrecen los servicios independientes, como el cifrado PGP automático o la compatibilidad con múltiples buzones de correo.

#### Contenido y Compras

En la parte superior de la aplicación **Ajustes**, verás tu nombre y tu foto de perfil si has iniciado sesión con un ID de Apple. Selecciónelo y, a continuación, seleccione **Contenido y compras** > **Ver cuenta**.

- [ ] Desactiva **Recomendaciones Personalizadas**

#### Buscar

**Buscar** es un servicio que te permite rastrear tus dispositivos Apple y compartir tu ubicación con tus amigos y familiares. También te permite borrar el dispositivo a distancia en caso de robo, evitando que un ladrón acceda a tus datos. En Buscar, tus [datos de localización son E2EE](https://www.apple.com/legal/privacy/data/en/find-my/) cuando:

- Tu localización se comparte con un familiar o amigo, y ambos utilizáis iOS 15 o superior.
- Tu dispositivo está desconectado y es localizado por la red Buscar.

Tus datos de localización no son E2EE cuando tu dispositivo está conectado y utilizas Buscar iPhone remotamente para localizar tu dispositivo. Tendrá que decidir si estas ventajas compensan los beneficios antirrobo del Bloqueo de Activación.

En la parte superior de la aplicación **Ajustes**, verás tu nombre y tu foto de perfil si has iniciado sesión con un ID de Apple. Selecciónelo y, a continuación, selecciona **Buscar**. Aquí puedes elegir si quieres activar o desactivar las funciones de localización de Buscar.

### Ajustes

Muchos otros ajustes relacionados con la privacidad se pueden encontrar en la aplicación **Ajustes**.

#### Modo Avión

Activar el **Modo Avión**, evita que tu teléfono entre en contacto con las torres de telefonía móvil. Seguirás pudiendo conectarte al Wi-Fi y Bluetooth, así que siempre que estés conectado al Wi-Fi puedes activar este ajuste.

#### Wi-Fi

Puedes activar la aleatorización de direcciones de hardware para protegerte del rastreo a través de redes Wi-Fi. En la red a la que está conectado actualmente, pulsa el :material-information: botón :

- [x] Activa **Dirección Wi-Fi privada**

También tienes la opción de **Limitar rastreo de dirección IP**. Esto es similar a iCloud Private Relay pero sólo afecta a las conexiones con "rastreadores conocidos". Dado que sólo afecta a las conexiones con servidores potencialmente maliciosos, probablemente esté bien dejar activada esta opción, pero si no quieres que enrute *ningún* tráfico a través de los servidores de Apple, deberías desactivarla.

#### Bluetooth

**Bluetooth** debe estar desactivado cuando no se esté utilizando, ya que aumenta la superficie de ataque. Desactivar el Bluetooth (o Wi-Fi) a través del Centro de Control sólo lo desactiva temporalmente: debes desactivarlo en Ajustes para que el efecto de la desactivación se mantenga.

- [ ] Desactiva **Bluetooth**

#### General

El nombre de dispositivo de tu iPhone contendrá por defecto tu nombre de pila, y éste será visible para cualquiera en las redes a las que te conectes. Deberías cambiarlo por algo más genérico, como "iPhone". Selecciona **Información** > **Nombre** e introduce el nombre de dispositivo que prefieras.

Es importante instalar con frecuencia **Actualizaciones de Software** para obtener las últimas correcciones de seguridad. Puedes activar **Actualizaciones Automáticas** para mantener tu teléfono al día sin necesidad de buscar actualizaciones constantemente. Selecciona **Actualización de Software** > **Actualizaciones Automáticas**:

- [x] Activa **Descargar Actualizaciones de iOS**
- [x] Activa **Instalar Actualizaciones de iOS**
- [x] Activa **Respuestas de Seguridad y Archivos del Sistema**

**AirDrop** te permite transferir archivos fácilmente, pero puede permitir que extraños te envíen archivos que no deseas.

- [x] Selecciona **AirDrop** > **Recepción Desactivada**

**AirPlay** te permite transmitir sin interrupciones contenidos desde tu iPhone a un televisor; sin embargo, es posible que no siempre quieras hacerlo. Selecciona **AirPlay y Handoff** > **Transmisión por AirPlay Automática**:

- [x] Selecciona **Nunca** o **Preguntar**

**Actualización en Segundo Plano** permite que tus aplicaciones actualicen su contenido mientras no las estás utilizando. Esto puede provocar que realicen conexiones no deseadas. Desactivar esta opción también puede ahorrar batería, pero puede afectar a la capacidad de una aplicación para recibir información actualizada, en particular las aplicaciones meteorológicas y de mensajería.

Selecciona **Actualización en Segundo Plano** y desactiva las aplicaciones que no quieras que sigan actualizándose en segundo plano. Si no quieres que ninguna aplicación se actualice en segundo plano, puedes volver a seleccionar **Actualización en Segundo Plano** y **desactivarla **.

#### Siri y Buscar

Si no quieres que nadie pueda controlar tu teléfono con Siri cuando está bloqueado, puedes desactivarlo aquí.

- [ ] Desactiva **Siri con Pantalla de Bloqueo**

#### Face ID/Touch ID y Código

Establecer una contraseña segura en tu teléfono es el paso más importante que puedes dar para la seguridad física del dispositivo. Tendrás que elegir entre seguridad y comodidad: Una contraseña más larga será molesta de escribir cada vez, pero una contraseña más corta o un PIN serán más fáciles de adivinar. Configurar Face ID o Touch ID junto con una contraseña segura puede ser un buen compromiso entre usabilidad y seguridad.

Selecciona **Activar Código** o **Cambiar Código** > **Opciones de Código** > **Código Alfanumérico Personalizado**. Asegúrate de crear una [contraseña segura](https://www.privacyguides.org/basics/passwords-overview/).

Si deseas utilizar Face ID o Touch ID, puedes seguir adelante y configurarlo ahora. Tu teléfono utilizará la contraseña que configuraste anteriormente como alternativa en caso de que falle la verificación biométrica. Los métodos de desbloqueo biométrico son ante todo una ventaja, aunque impiden que las cámaras de vigilancia o las personas por encima de su hombro te vean introducir el código.

Si utilizas datos biométricos, debes saber cómo desactivarlos rápidamente en caso de emergencia. Si mantienes pulsado el botón lateral o de encendido y *o* el botón de volumen hasta que veas el control deslizante para Apagar, se desactivará la biometría y tendrás que introducir el código para desbloquear. El código también será necesario después de reiniciar el dispositivo.

En algunos dispositivos antiguos, puede que tengas que pulsar el botón de encendido cinco veces para desactivar la biometría en su lugar, o para los dispositivos con Touch ID puede que sólo tengas que mantener pulsado el botón de encendido y nada más. Asegúrate de probarlo con antelación para saber qué método funciona con tu dispositivo.

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

!!! warning "Advertencia"

    Con esta opción activada, alguien podría borrar intencionadamente tu teléfono introduciendo muchas veces una contraseña incorrecta. Asegúrate de tener copias de seguridad adecuadas y activa esta configuración sólo si te sientes cómodo con ella.

- [x] Activa **Borrar Datos**

#### Privacidad

**Localización** te permite utilizar funciones como Buscar y Mapas. Si no necesitas estas funciones, puedes desactivar Localización. Alternativamente, puede revisar y elegir qué aplicaciones pueden usar tu ubicación aquí. Selecciona **Localización**:

- [ ] Desactiva **Localización**

Aquí puedes decidir si permites que las aplicaciones soliciten **rastrearte**. Desactivar esta opción impide que todas las aplicaciones te rastreen con el ID de publicidad de tu teléfono. Selecciona **Rastreo**:

- [ ] Desactiva **Permitir que las Apps Soliciten Rastrearte**

Deberías desactivar **Datos de Uso y de los Sensores** si no deseas participar en estudios. Selecciona **Datos de Uso y de los Sensores**:

- [ ] Desactiva **Datos de Uso y de los Sensores**

**Comprobación de Seguridad** te permite ver y revocar rápidamente a determinadas personas y aplicaciones que podrían tener permiso para acceder a tus datos. Aquí puedes realizar un **Restablecimiento de Emergencia**, restableciendo inmediatamente los permisos de todas las personas y aplicaciones que puedan tener acceso a los recursos del dispositivo, y puedes **Gestionar Accesos y Datos Compartidos;** que te permite revisar y personalizar quién y qué tiene acceso a los recursos de tu dispositivo y cuenta.

Deberías desactivar los análisis si no deseas enviar datos de uso a Apple. Selecciona **Análisis y Mejoras**:

- [ ] Desactiva **Compartir Análisis (iPhone)** o **Compartir Análisis (iPhone y Apple Watch)**
- [ ] Desactiva **Compartir Análisis (iCloud)**
- [ ] Desactiva **Mejorar Fitness++**
- [ ] Desactiva **Mejorar Seguridad**
- [ ] Desactiva **Mejorar Siri y Dictado**

Desactiva **Anuncios Personalizados** si no quieres anuncios personalizados. Selecciona **Publicidad de Apple**

- [ ] Desactiva **Anuncios Personalizados**

**Informe de Privacidad de las Apps** es una herramienta integrada que te permite ver qué permisos utilizan tus aplicaciones. Selecciona **Informe de Privacidad de las Apps**:

- [x] Selecciona **Activar el Informe de Privacidad de las Apps**

[Modo de Aislamiento](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode) es un ajuste de seguridad que puedes activar para que tu teléfono sea más resistente a los ataques. Be aware that certain apps and features [won't work](https://support.apple.com/en-us/HT212650) as they do normally.

- [x] Select **Turn On Lockdown Mode**

## Additional Advice

### E2EE Calls

Normal phone calls made with the Phone app through your carrier are not E2EE. Both FaceTime Video and FaceTime Audio calls are E2EE, or you can use [another app](../real-time-communication.md) like Signal.

### Avoid Jailbreaking

Jailbreaking an iPhone undermines its security and makes you vulnerable. Running untrusted, third-party software could cause your device to be infected with malware.

### Encrypted iMessage

The color of the message bubble in the Messages app indicates whether your messages are E2EE or not. A blue bubble indicates that you're using iMessage with E2EE, while a green bubble indicates they're using the outdated SMS and MMS protocols. Currently, the only way to get E2EE in Messages is for both parties to be using iMessage on Apple devices.

If either you or your messaging partner have iCloud Backup enabled without Advanced Data Protection, the encryption key will be stored on Apple's servers, meaning they can access your messages. Additionally, iMessage's key exchange is not as secure as alternative implementations, like Signal (which allows you to view the recipients key and verify by QR code), so it shouldn't be relied on for particularly sensitive communications.

### Blacking Out Faces/Information

If you need to hide information in a photo, you can use Apple's built-in tools to do so. Open the photo you want to edit, press edit in the top right corner of the screen, then press the markup symbol at the top right. Press the plus at the bottom right of the screen, then press the rectangle icon. Now, you can place a rectangle anywhere on the image. Make sure to press the shape icon at the bottom left and select the filled-in rectangle. **Don't** use the highlighter to obfuscate information, because its opacity is not quite 100%.

### iOS Betas

Apple always makes beta versions of iOS available early for those that wish to help find and report bugs. We don't recommend installing beta software on your phone. Beta releases are potentially unstable and could have undiscovered security vulnerabilities.

## Security Highlights

### Before First Unlock

If your threat model includes forensic tools and you want to minimize the chance of exploits being used to access your phone, you should restart your device frequently. The state *after* a reboot but *before* unlocking your device is referred to as "Before First Unlock" (BFU), and when your device is in that state it makes it [significantly more difficult](https://belkasoft.com/checkm8_glossary) for forensic tools to exploit vulnerabilities to access your data. This BFU state allows you to receive notifications for calls, texts, and alarms, but most of the data on your device is still encrypted and inaccessible. This can be impractical, so consider whether these trade-offs make sense for your situation.
