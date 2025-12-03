---
title: Resumen de iOS
icon: simple/apple
description: iOS es un sistema operativo móvil desarrollado por Apple para el iPhone.
---

**iOS** y **iPadOS** son sistemas operativos móviles patentados desarrollados por Apple para sus productos iPhone y iPad, respectivamente. Si tienes un dispositivo móvil de Apple, puedes aumentar tu privacidad desactivando algunas funciones de telemetría integradas y reforzando algunos ajustes de privacidad y seguridad integrados en el sistema.

## Notas de Privacidad

Los dispositivos iOS suelen ser elogiados por los expertos en seguridad por su sólida protección de datos y su adhesión a las mejores prácticas modernas. Sin embargo, el carácter restrictivo del ecosistema de Apple -especialmente con sus dispositivos móviles- sigue obstaculizando la privacidad de varias maneras.

En general, consideramos que iOS ofrece una protección de la privacidad y la seguridad mejor que la media para la mayoría de la gente, en comparación con los dispositivos Android de serie de cualquier fabricante. Sin embargo, puedes alcanzar estándares de privacidad aún más altos con un [sistema operativo Android personalizado](../android/distributions.md) como GrapheneOS, si quieres o necesitas ser completamente independiente de los servicios en la nube de Apple o Google.

### Bloqueo de Activación

Todos los dispositivos iOS deben ser verificados contra los servidores de bloqueo de activación de la aplicación cuando se configuran o se restablecen por primera vez, lo que significa que es **necesaria** una conexión a Internet para utilizar un dispositivo iOS.

### App Store Obligatoria

La única fuente de aplicaciones en iOS es la App Store de Apple, que requiere una cuenta de Apple para acceder. Esto significa que Apple tiene un registro de todas las aplicaciones que instalas en tu dispositivo, y es probable que pueda relacionar esa información con tu identidad real si proporcionas a la App Store un método de pago.

### Telemetría Invasiva

Apple ha tenido históricamente problemas con la correcta disociación de su telemetría de las Cuentas de Apple en iOS. En [2019](https://theguardian.com/technology/2019/jul/26/apple-contractors-regularly-hear-confidential-details-on-siri-recordings), se descubrió que Apple transmitía grabaciones de Siri -algunas con información altamente confidencial- a sus servidores para que terceros contratistas las revisaran manualmente. Aunque Apple detuvo temporalmente ese programa después de que se [informara ampliamente sobre](https://theverge.com/2019/8/23/20830120/apple-contractors-siri-recordings-listening-1000-a-day-globetech-microsoft-cortana) esa práctica, la compañía puso en marcha un interruptor para [**optar por no** subir conversaciones con Siri](https://theguardian.com/technology/2019/oct/30/apple-lets-users-opt-out-of-having-siri-conversations-recorded) unos meses más tarde en la siguiente actualización de iOS. Además, en 2021, [Apple retocó Siri](https://theguardian.com/technology/2021/jun/07/apple-overhauls-siri-to-address-privacy-concerns-and-improve-performance) para que procese las grabaciones de voz localmente en lugar de enviarlas a sus servidores.

Más recientemente, se ha descubierto que Apple transmite datos analíticos [incluso cuando el uso compartido de datos analíticos está desactivado](https://gizmodo.com/apple-iphone-analytics-tracking-even-when-off-app-store-1849757558) en iOS, y estos datos [parecen](https://twitter.com/mysk_co/status/1594515229915979776) estar fácilmente vinculados a identificadores de cuenta únicos de iCloud a pesar de estar supuestamente desvinculados de las cuentas de Apple.

### Tráfico Fuera de las Conexiones VPN Activas

La [política de privacidad de Apple en relación con las VPN](https://apple.com/legal/privacy/data/en/vpns) establece:

> Incluso cuando una VPN está activa, parte del tráfico necesario para los servicios esenciales del sistema tendrá lugar fuera de la VPN para que tu dispositivo pueda funcionar correctamente.

## Configuración Recomendada

**Nota:** En esta guía se asume que utilizas la última versión de iOS.

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

En la parte superior de la aplicación **Ajustes**, verás tu nombre y tu foto de perfil si has iniciado sesión con una cuenta de Apple. Selecciónalo y, a continuación, selecciona **Contenido y compras**→**Ver cuenta**.

- [ ] Desactiva **Recomendaciones Personalizadas**

#### Buscar

**Buscar** es un servicio que te permite rastrear tus dispositivos Apple y compartir tu ubicación con tus amigos y familiares. También te permite borrar el dispositivo a distancia en caso de robo, evitando que un ladrón acceda a tus datos. Tus [datos de localización de Buscar son E2EE](https://apple.com/legal/privacy/data/en/find-my) cuando:

- Tu localización se comparte con un familiar o amigo, y ambos utilizáis iOS 17 o superior.
- Tu dispositivo está desconectado y es localizado por la red Buscar.

Tus datos de localización no son E2EE cuando tu dispositivo está conectado y utilizas Buscar iPhone remotamente para localizar tu dispositivo. Tendrá que decidir si estas ventajas compensan los beneficios antirrobo del Bloqueo de Activación.

En la parte superior de la aplicación **Ajustes**, verás tu nombre y tu foto de perfil si has iniciado sesión con una cuenta de Apple. Selecciónelo y, a continuación, selecciona **Buscar**. Aquí puedes elegir si quieres activar o desactivar las funciones de localización de Buscar.

### Ajustes

Muchos otros ajustes relacionados con la privacidad se pueden encontrar en la aplicación **Ajustes**.

#### Modo Avión

Activar el **Modo Avión**, evita que tu teléfono entre en contacto con las torres de telefonía móvil. Seguirás pudiendo conectarte al Wi-Fi y Bluetooth, así que siempre que estés conectado al Wi-Fi puedes activar este ajuste.

#### Wi-Fi

Puedes activar [la aleatorización de direcciones de hardware](https://support.apple.com/en-us/102509#triswitch) para protegerte del rastreo a través de redes Wi-Fi, y en la misma red a lo largo del tiempo. En la red a la que está conectado actualmente, pulsa el :material-information: botón :

- [x] Configura la **Dirección Wi-Fi Privada ** como **Fija** o **Rotatoria**

También tienes la opción de **Limitar rastreo de dirección IP**. Esto es similar a iCloud Private Relay pero sólo afecta a las conexiones con "rastreadores conocidos". Dado que sólo afecta a las conexiones con servidores potencialmente maliciosos, probablemente esté bien dejar activada esta opción, pero si no quieres que enrute *ningún* tráfico a través de los servidores de Apple, deberías desactivarla.

#### Bluetooth

**Bluetooth** debe estar desactivado cuando no se esté utilizando, ya que aumenta la superficie de ataque. Desactivar el Bluetooth (o Wi-Fi) a través del Centro de Control sólo lo desactiva temporalmente: debes desactivarlo en Ajustes para que el efecto de la desactivación se mantenga.

- [ ] Desactiva **Bluetooth**

Ten en cuenta que Bluetooth se activa automáticamente después de cada actualización del sistema.

#### General

El nombre de dispositivo de tu iPhone contendrá por defecto tu nombre de pila, y éste será visible para cualquiera en las redes a las que te conectes. Deberías cambiarlo por algo más genérico, como "iPhone". Selecciona **Información**→**Nombre** e introduce el nombre de dispositivo que prefieras.

Es importante instalar actualizaciones de software con frecuencia para obtener las últimas correcciones de seguridad. Puedes activar las actualizaciones automáticas para mantener tu teléfono al día sin necesidad de comprobar constantemente si hay actualizaciones. Selecciona **Actualización de Software**→**Actualizaciones Automáticas**:

- [x] Activa **Instalación Automática**

**AirDrop** se utiliza habitualmente para compartir archivos con facilidad, pero representa un importante riesgo para la privacidad. El protocolo AirDrop transmite constantemente tu información personal a tu entorno, con protecciones de seguridad [muy débiles](https://usenix.org/system/files/sec21-heinrich.pdf). Tu identidad puede ser descubierta fácilmente por los atacantes, incluso con recursos limitados, y el gobierno chino ha [reconocido abiertamente](https://arstechnica.com/security/2024/01/hackers-can-id-unique-apple-airdrop-users-chinese-authorities-claim-to-do-just-that) el uso de tales técnicas para identificar a los usuarios de AirDrop en público desde 2022.

- [x] Selecciona **AirDrop** → **Recepción Desactivada**

**AirPlay** te permite transmitir sin interrupciones contenidos desde tu iPhone a un televisor; sin embargo, es posible que no siempre quieras hacerlo. Selecciona **AirPlay y Continuidad**→ **Transmisión por AirPlay Automática**:

- [x] Selecciona **Nunca** o **Preguntar**

**Actualización en Segundo Plano** permite que tus aplicaciones actualicen su contenido mientras no las estás utilizando. Esto puede provocar que realicen conexiones no deseadas. Desactivar esta opción también puede ahorrar batería, pero puede afectar a la capacidad de una aplicación para recibir información actualizada, en particular las aplicaciones meteorológicas y de mensajería.

Selecciona **Actualización en Segundo Plano** y desactiva las aplicaciones que no quieras que sigan actualizándose en segundo plano. Si no quieres que ninguna aplicación se actualice en segundo plano, puedes volver a seleccionar **Actualización en Segundo Plano** y **desactivarla **.

#### Apple Intelligence y Siri

Esto está disponible si tu dispositivo es compatible con **[Apple Intelligence](https://support.apple.com/guide/iphone/apple-intelligence-and-privacy-iphe3f499e0e/ios)**. Apple Intelligence utiliza una combinación de procesamiento en el dispositivo y su **[Private Cloud Compute](https://security.apple.com/blog/private-cloud-compute)** para cosas que requieren más potencia de procesamiento de la que puede proporcionar tu dispositivo.

Para ver un informe de todas las solicitudes realizadas a los servidores de Apple, puedes ir a **Privacidad y seguridad** → **Informe de Apple Intelligence** y pulsar **Exportar actividad** para ver la actividad de los últimos 15 minutos o 7 días, según lo que hayas configurado. De forma similar al **Informe de privacidad de las apps**, que muestra los permisos recientes a los que han accedido las aplicaciones de tu teléfono, el Informe de Apple Intelligence también muestra lo que se envía a los servidores de Apple mientras utilizas Apple Intelligence.

Apple Intelligence puede integrarse con [ChatGPT](https://support.apple.com/guide/iphone/use-chatgpt-with-apple-intelligence-iph00fd3c8c2/ios). Si deseas la integración con ChatGPT, puedes navegar hasta **ChatGPT** y pulsar **Configurar**. Si quieres desactivarla, ve al mismo sitio:

- [ ] Desactiva **Usar ChatGPT**

También puedes hacer que te solicite una confirmación cada vez que dejes activada la integración con ChatGPT:

- [x] Activa **Confirmar peticiones**

Si no quieres que nadie pueda controlar tu teléfono con Siri cuando está bloqueado, puedes desactivarlo aquí.

- [ ] Desactiva **Siri con Pantalla de Bloqueo**

#### Face ID/Touch ID y Código

Establecer una contraseña segura en tu teléfono es el paso más importante que puedes dar para la seguridad física del dispositivo. Tendrás que elegir entre seguridad y comodidad: una contraseña más larga será molesta de escribir cada vez, pero una contraseña más corta o un PIN serán más fáciles de adivinar. Configurar Face ID o Touch ID junto con una contraseña segura puede ser un buen compromiso entre usabilidad y seguridad.

Selecciona **Activar Código** o **Cambiar Código**→ **Opciones de Código**→ **Código Alfanumérico Personalizado**. Asegúrate de crear una [contraseña segura](../basics/passwords-overview.md).

Si deseas utilizar Face ID o Touch ID, puedes seguir adelante y configurarlo ahora. Tu teléfono utilizará la contraseña que configuraste anteriormente como alternativa en caso de que falle la verificación biométrica. Los métodos de desbloqueo biométrico son ante todo una ventaja, aunque impiden que las cámaras de vigilancia o las personas por encima de su hombro te vean introducir el código.

Si utilizas datos biométricos, debes saber cómo desactivarlos rápidamente en caso de emergencia. Si mantienes pulsado el [botón lateral](https://support.apple.com/en-us/105103) y *cualquiera* de los botones de volumen hasta que veas el control deslizante para Apagar, se desactivará la biometría y tendrás que usar el código para desbloquear. Se te pedirá tu código después de que tu dispositivo se reinicie.

De forma similar, puedes desactivar la biometría pulsando cinco veces el botón lateral o, en el caso de los dispositivos con Touch ID, simplemente manteniendo pulsado el botón lateral. Asegúrate de probarlo con antelación para saber qué método funciona en tu dispositivo.

**Protección en Caso de Robo** añade seguridad adicional destinada a proteger tus datos personales si te roban el dispositivo mientras está desbloqueado. Si activas tanto la autenticación biométrica como la función [Buscar](#find-my) de iPhone, te recomendamos que actives esta protección:

- [x] Activa **Protección del Dispositivo en Caso de Robo**

Después de activar la Protección en Caso de Robo, [ciertas acciones](https://support.apple.com/HT212510) requerirán autenticación biométrica sin una contraseña de respaldo (en el caso de que un "shoulder surfer" haya obtenido tu PIN), como el uso de autorrelleno de contraseña, el acceso a información de pago y la desactivación del Modo Perdido. También añade un retardo de seguridad a ciertas acciones que se realizan fuera de casa o de otro "lugar conocido", como exigir un temporizador de 1 hora para restablecer la contraseña de la cuenta de Apple o cerrar sesión en ella. Este retraso pretende darte tiempo para activar el Modo Perdido y asegurar tu cuenta antes de que un ladrón pueda reiniciar tu dispositivo.

**Permitir Acceso al Estar Bloqueado** te da opciones sobre lo que puedes permitir cuando tu teléfono está bloqueado. Elige qué función quieres desactivar para evitar accesos no autorizados si alguien se hace con tu teléfono. Cuantas más de estas opciones deshabilites, menos podrá hacer alguien sin tu contraseña, pero menos cómodo será para ti.

Los iPhones ya son resistentes a los ataques de fuerza bruta, ya que te hacen esperar largos periodos de tiempo después de varios intentos fallidos; sin embargo, históricamente ha habido exploits para sortear esto. Para mayor seguridad, puedes configurar tu teléfono para que se borre automáticamente después de 10 intentos fallidos.

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

Con esta opción activada, alguien podría borrar intencionadamente tu teléfono introduciendo muchas veces una contraseña incorrecta. Asegúrate de tener copias de seguridad adecuadas y activa esta configuración sólo si te sientes cómodo con ella.

</div>

- [x] Activa **Borrar Datos**

#### Privacidad & Seguridad

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

**[Comprobación de seguridad](https://support.apple.com/guide/personal-safety/safety-check-iphone-ios-16-ips2aad835e1/1.0/web/1.0)** te permite ver y revocar rápidamente a determinadas personas y aplicaciones que podrían tener permiso para acceder a tus datos. Aquí puedes realizar un **Restablecimiento de Emergencia**, restableciendo inmediatamente los permisos para todas las personas y aplicaciones que puedan tener acceso a los recursos del dispositivo. También puedes **Gestionar Accesos y Datos Compartidos**, lo cual te permite revisar y personalizar quién y qué tiene acceso a tu dispositivo y a los recursos de tu cuenta. Si te encuentras en una situación de abuso, lee el [Manual de Uso de Seguridad Personal](https://support.apple.com/guide/personal-safety/welcome/web) de Apple para que orientarte sobre lo que debes hacer.

Deberías desactivar los análisis si no deseas enviar datos de uso a Apple. Selecciona **Análisis y Mejoras** y desmarca los tipos de análisis que no deseas enviar a Apple.

Desactiva **Anuncios Personalizados** si no quieres anuncios personalizados. Selecciona **Publicidad de Apple**:

- [ ] Desactiva **Anuncios Personalizados**

**Informe de Privacidad de las Apps** es una herramienta integrada que te permite ver qué permisos utilizan tus aplicaciones. Selecciona **Informe de Privacidad de las Apps**:

- [x] Selecciona **Activar el Informe de Privacidad de las Apps**

Configura los accesorios conectados por cable para que soliciten permiso cuando los conectes. Selecciona **Accesorios con cable**:

- [x] Selecciona **Preguntar siempre** o **Preguntar con nuevos accesorios**

El **[Modo de Aislamiento](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode)** es un ajuste de seguridad que puedes activar para que tu teléfono sea más resistente a los ataques. Ten en cuenta que algunas aplicaciones y funciones [no funcionarán](https://support.apple.com/HT212650) como lo hacen normalmente.

- [x] Selecciona **Activar el Modo de Aislamiento**

## Consejo Adicional

### Llamadas E2EE

Las llamadas telefónicas normales realizadas con la aplicación Teléfono a través de tu operador no son E2EE. Tanto las llamadas de FaceTime Video como las de FaceTime Audio son E2EE. También puedes utilizar [otra aplicación](../real-time-communication.md) como Signal para las llamadas E2EE.

### iMessage Encriptado

El [color de la burbuja de mensajes](https://support.apple.com/en-us/104972) en la aplicación Mensajes indica si tus mensajes son E2EE o no. Una burbuja azul indica que estás utilizando iMessage con E2EE, mientras que una burbuja verde indica que la otra parte está utilizando los anticuados protocolos SMS y MMS o RCS. RCS en iOS **no** es E2EE. Actualmente, la única forma de tener E2EE en Mensajes es que ambas partes utilicen iMessage en dispositivos Apple.

Si tú o tu compañero de mensajería tenéis activada la Copia de Seguridad de iCloud sin Protección de Datos Avanzada, la clave de cifrado se almacenará en los servidores de Apple, lo que significa que podrán acceder a tus mensajes.

By default, you trust Apple's identity servers that you're messaging the right person. To defend yourself from a potentially malicious server, you can enable **[Contact Key Verification](https://support.apple.com/en-us/118246)**. At the top of the **Settings** app where your name is, select it, then go to **Contact Key Verification**.

- [x] Turn on **Verification in iMessage**

Both you and your contacts need to enable Contact Key Verification and follow Apple's [instructions](https://support.apple.com/en-us/118246#verify) for the security assurances mentioned above to take effect.

### Permisos de Fotos

Cuando una aplicación te pide acceso a la biblioteca de fotos de tu dispositivo, iOS te ofrece opciones para limitar a qué puede acceder una aplicación.

En lugar de permitir que una aplicación acceda a todas las fotos de tu dispositivo, puedes permitir que solo acceda a las fotos que tú elijas pulsando la opción "Seleccionar Fotos..." en el cuadro de diálogo de permisos. Puedes cambiar los permisos de acceso a las fotos en cualquier momento navegando hasta **Ajustes** → **Privacidad y Seguridad** → **Fotos**.

![Permisos de Fotos](../assets/img/ios/photo-permissions-light.png#only-light) ![Permisos de Fotos](../assets/img/ios/photo-permissions-dark.png#only-dark)

**Solo Añadir Fotos** es un permiso que solo permite a una aplicación descargar fotos a la biblioteca de fotos. No todas las aplicaciones que solicitan acceso a la biblioteca de fotos proporcionan esta opción.

![Acceso Privado](../assets/img/ios/private-access-light.png#only-light) ![Acceso Privado](../assets/img/ios/private-access-dark.png#only-dark)

Algunas aplicaciones también admiten el **Acceso Privado**, que funciona de forma similar al permiso de **Acceso Limitado**. Sin embargo, las fotos compartidas con aplicaciones que utilizan Acceso Privado incluyen su ubicación por defecto. Te recomendamos que desactives esta opción si previamente no [eliminas los metadatos de las fotos](../data-redaction.md).

### Permisos de Contacto

Del mismo modo, en lugar de permitir que una aplicación acceda a todos los contactos guardados en tu dispositivo, puedes permitir que solo acceda a los contactos que tú elijas. Puede cambiar los permisos de acceso a los contactos en cualquier momento navegando hasta **Ajustes** → **Privacidad y Seguridad** → **Contactos**.

![Permisos de Contacto](../assets/img/ios/contact-permissions-light.png#only-light) ![Permisos de Contacto](../assets/img/ios/contact-permissions-dark.png#only-dark)

### Exigir Datos Biométricos y Ocultar Aplicaciones

iOS ofrece la posibilidad de bloquear la mayoría de las aplicaciones con Touch ID/Face ID o tu código, lo que puede ser útil para proteger contenido sensible en aplicaciones que no ofrecen esta opción. Puedes bloquear una aplicación pulsando prolongadamente sobre ella y seleccionando **Requerir Face ID/Touch ID**. Cualquier aplicación bloqueada de este modo requiere autenticación biométrica cada vez que se abre o se accede a su contenido en otras aplicaciones. Además, no se mostrarán las vistas previas de las notificaciones de las aplicaciones bloqueadas.

Además de bloquear las aplicaciones tras los datos biométricos, también puedes ocultarlas para que no aparezcan en la pantalla de inicio, la biblioteca de aplicaciones, la lista de aplicaciones en **Ajustes**, etc. Aunque ocultar aplicaciones puede ser útil en situaciones en las que tienes que entregar tu teléfono desbloqueado a otra persona, la ocultación que proporciona la función no es absoluta, ya que una aplicación oculta sigue siendo visible en algunos lugares, como la lista de uso de la batería. Además, una desventaja notable de ocultar una aplicación es que no recibirás ninguna de sus notificaciones.

Puedes ocultar una aplicación pulsando prolongadamente sobre ella y seleccionando **Requerir Face ID/Touch**→**Ocultar y Requerir Face ID/Touch ID**. Ten en cuenta que las aplicaciones de Apple preinstaladas, así como el navegador web y la aplicación de correo electrónico predeterminados, no se pueden ocultar. Las aplicaciones ocultas residen en una carpeta **Oculta** en la parte inferior de la biblioteca de aplicaciones, que puede desbloquearse utilizando datos biométricos. Esta carpeta aparece en la Biblioteca de Aplicaciones tanto si has ocultado aplicaciones como si no, lo que te proporciona un grado de negación plausible.

### Guided Access

Sometimes you might want to hand your phone to someone to make a call or do a specific task, but you don't want them to have full access to your phone. In these cases, you can quickly enable **[Guided Access](https://support.apple.com/guide/iphone/lock-iphone-to-one-app-iph7fad0d10/ios)** to lock the phone to one specific app until you authenticate.

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

Guided Access isn't foolproof, as it's possible you could leak data unintentionally or the feature could be bypassed. You should only use Guided Access for situations where you casually hand your phone to someone to use. You should not use it as a tool to protect against advanced adversaries.

</div>

### Ocultar Elementos en Imágenes

Si necesitas ocultar información en una foto, puedes utilizar las herramientas de edición integradas de Apple para hacerlo.

You can use the [Clean Up](https://support.apple.com/en-us/121429) feature on supported devices to pixelate faces or remove objects from images.

- Abre la aplicación **Fotos** y toca la foto que hayas seleccionado para editarla
- Tap the :material-tune:
- Pulsa el botón **Limpiar**
- Dibuja un círculo alrededor de lo que quieras ocultar. Las caras se pixelarán y se intentará borrar todo lo demás.

Nuestra advertencia [en contra de difuminar el texto](../data-redaction.md) también se aplica aquí, por lo que recomendamos en su lugar añadir una forma negra con una opacidad del 100% sobre ello. Además de ocultar texto, también puedes tachar cualquier cara u objeto con la aplicación **Fotos**.

<div class="annotate" markdown>

- Tap the image you have selected for redaction
- Tap the :material-tune: → :material-dots-horizontal: (1) → Markup → :material-plus:
- Select **Add Shape** and choose the square or circle
- On the toolbar, tap the circle and choose black as the color for filling in the shape. También puedes mover la forma y aumentar su tamaño según te convenga.

</div>

1. This may not appear on certain iPhone models.

**No** utilices el resaltador para ocultar información, ya que su opacidad no es del 100%.

### Evita el Jailbreaking

El jailbreaking en un iPhone socava su seguridad y te hace vulnerable. Ejecutar software de terceros que no sea de confianza podría infectar tu dispositivo con malware.

### Betas de iOS

Apple siempre pone las versiones beta de iOS a disposición de quienes deseen ayudar a encontrar y notificar errores. No recomendamos instalar software beta en tu teléfono. Las versiones beta son potencialmente inestables y podrían tener vulnerabilidades de seguridad no descubiertas.

## Aspectos Destacados de Seguridad

### Antes del Primer Desbloqueo

Si tu modelo de amenaza incluye [:material-target-account: Ataques Dirigidos](../basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red} que implican herramientas forenses, y quieres minimizar la posibilidad de que se utilicen exploits para acceder a tu teléfono, deberías reiniciar tu dispositivo con frecuencia. El estado *después de* un reinicio pero *antes de* desbloquear tu dispositivo se conoce como "Antes del Primer Desbloqueo" (BFU), y cuando tu dispositivo está en ese estado hace que sea [significativamente más difícil](https://belkasoft.com/checkm8_glossary) para las herramientas forenses explotar vulnerabilidades para acceder a tus datos. Este estado BFU te permite recibir notificaciones de llamadas, mensajes de texto y alarmas, pero la mayoría de los datos de tu dispositivo siguen estando encriptados y son inaccesibles. Esto puede ser poco práctico, así que considera si estas soluciones tienen sentido para tu situación.

iPhones [automatically reboot](https://support.apple.com/guide/security/protecting-user-data-in-the-face-of-attack-secf5549a4f5/1/web/1#:~:text=On%20an%20iPhone%20or%20iPad%20with%20iOS%2018%20and%20iPadOS%2018%20or%20later%2C%20a%20new%20security%20protection%20will%20restart%20devices%20if%20they%20remain%20locked%20for%20a%20prolonged%20period%20of%20time.) if they're not unlocked after a period of time.

### MTE

The iPhone 17 line and later offer a security enhancement called [Memory Tagging Extension](https://developer.arm.com/documentation/108035/0100/Introduction-to-the-Memory-Tagging-Extension) (MTE), which makes it significantly harder for an attacker to exploit memory corruption vulnerabilities. This always-on protection depends on hardware support, so it's not available for older devices.

For more details on Apple's implementation of MTE, read the [blog post](https://security.apple.com/blog/memory-integrity-enforcement) published by Apple Security Research. We also cover Apple's implementation of MTE and how it compares to Android's implementation in the Google Pixel 8 series and later in our [own article](https://www.privacyguides.org/posts/2025/09/20/memory-integrity-enforcement-changes-the-game-on-ios).
