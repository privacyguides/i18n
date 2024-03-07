---
title: iOS Overview
icon: simple/apple
description: iOS is a mobile operating system developed by Apple for the iPhone.
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

Recientemente, se ha descubierto que Apple [transmite datos analíticos incluso cuando el envío de datos analíticos se encuentra desactivado](https://gizmodo.com/apple-iphone-analytics-tracking-even-when-off-app-store-1849757558) en iOS, y esta información [parece](https://twitter.com/mysk_co/status/1594515229915979776) estar fácilmente vinculados a identificadores de cuenta únicos de iCloud, a pesar de ser supuestamente anónimos.

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

**Protección de Datos Robados** es una nueva función de iOS 17.3 que añade seguridad adicional destinada a proteger tus datos personales si te roban el dispositivo mientras está desbloqueado. Si utilizas la biometría y la función Buscar Mi Dispositivo en la configuración de tu ID de Apple, te recomendamos que actives esta nueva protección:

- [x] Selecciona **Activar Protección**

Después de activar la protección de datos robados, [ciertas acciones](https://support.apple.com/en-us/HT212510) requerirán autenticación biométrica sin una contraseña de respaldo (en el caso de que un shoulder surfer haya obtenido tu PIN), tales como el uso de autorrelleno de contraseña, el acceso a la información de pago, y la desactivación del modo perdido. También añade un retardo de seguridad a ciertas acciones realizadas fuera de casa o de otro "lugar familiar", como el requerimiento de un temporizador de 1 hora para restablecer la contraseña de tu ID de Apple o cerrar sesión en tu ID de Apple. Este retraso pretende darte tiempo para activar el Modo Perdido y asegurar tu cuenta antes de que un ladrón pueda reiniciar tu dispositivo.

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

[Modo de Aislamiento](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode) es un ajuste de seguridad que puedes activar para que tu teléfono sea más resistente a los ataques. Ten en cuenta que algunas aplicaciones y funciones [no funcionarán](https://support.apple.com/en-us/HT212650) como lo hacen normalmente.

- [x] Selecciona **Activar el Modo de Aislamiento**

## Consejo Adicional

### Llamadas E2EE

Las llamadas telefónicas normales realizadas con la aplicación Teléfono a través de tu operador no son E2EE. Tanto las llamadas de FaceTime Vídeo como las de FaceTime Audio son E2EE, o puedes usar [otra app](../real-time-communication.md) como Signal.

### Evita el Jailbreaking

El jailbreaking en un iPhone socava su seguridad y te hace vulnerable. Ejecutar software de terceros que no sea de confianza podría infectar tu dispositivo con malware.

### iMessage Encriptado

El color de la burbuja de mensajes en la aplicación Mensajes indica si tus mensajes son E2EE o no. Una burbuja azul indica que estás utilizando iMessage con E2EE, mientras que una burbuja verde indica que están utilizando los anticuados protocolos SMS y MMS. Actualmente, la única forma de obtener E2EE en Mensajes es que ambas partes utilicen iMessage en dispositivos Apple.

Si tú o tu compañero de mensajería tenéis activada la Copia de Seguridad de iCloud sin Protección de Datos Avanzada, la clave de cifrado se almacenará en los servidores de Apple, lo que significa que podrán acceder a tus mensajes. Además, el intercambio de claves de iMessage no es tan seguro como otras implementaciones alternativas, como Signal (que permite ver la clave del destinatario y verificarla mediante un código QR), por lo que no se debería confiar en él para comunicaciones especialmente sensibles.

### Ocultar Caras/Información

Si necesitas ocultar información en una foto, puedes utilizar las herramientas integradas de Apple para hacerlo. Abre la foto que quieras editar, pulsa Editar en la esquina superior derecha de la pantalla y, a continuación, pulsa el símbolo de marcado de la parte superior derecha. Pulsa el signo más en la parte inferior derecha de la pantalla y, a continuación, pulsa el icono del rectángulo. Ahora, puede colocar un rectángulo en cualquier lugar de la imagen. Asegúrate de pulsar el icono de forma de la parte inferior izquierda y selecciona el rectángulo relleno. **No** utilices el resaltador para ocultar información, ya que su opacidad no es del 100%.

### Betas de iOS

Apple siempre pone las versiones beta de iOS a disposición de quienes deseen ayudar a encontrar y notificar errores. No recomendamos instalar software beta en tu teléfono. Las versiones beta son potencialmente inestables y podrían tener vulnerabilidades de seguridad no descubiertas.

## Aspectos Destacados de Seguridad

### Antes del Primer Desbloqueo

Si tu modelo de amenazas incluye herramientas forenses y quieres minimizar la posibilidad de que se utilicen exploits para acceder a tu teléfono, debes reiniciar el dispositivo con frecuencia. El estado *después de* un reinicio pero *antes de* desbloquear tu dispositivo se conoce como "Antes del Primer Desbloqueo" (BFU), y cuando tu dispositivo está en ese estado hace que sea [significativamente más difícil](https://belkasoft.com/checkm8_glossary) para las herramientas forenses explotar vulnerabilidades para acceder a tus datos. Este estado BFU te permite recibir notificaciones de llamadas, mensajes de texto y alarmas, pero la mayoría de los datos de tu dispositivo siguen estando encriptados y son inaccesibles. Esto puede ser poco práctico, así que considera si estas soluciones tienen sentido para tu situación.
