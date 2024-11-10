---
meta_title: "Los Mejores Servicios de Mensajería Instantánea Privados - Privacy Guides"
title: "Comunicación en Tiempo Real"
icon: material/chat-processing
description: Los servicios de mensajería cifrados como Signal y SimpleX mantienen sus comunicaciones confidenciales a salvo de miradas indiscretas.
cover: real-time-communication.webp
---

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-bug-outline: Ataques pasivos](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: Proveedores de servicios](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}
- [:material-eye-outline: Vigilancia masiva](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-account-cash: Capitalismo de Vigilancia](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Estas son nuestras recomendaciones para la comunicación cifrada **en tiempo real**.

[Tipos de Redes de Comunicación :material-arrow-right-drop-circle:](./advanced/communication-network-types.md)

## Servicios de Mensajería Cifrados

Estos servicios de mensajería son ideales para proteger sus comunicaciones confidenciales.

### Signal

<div class="admonition recommendation" markdown>

![Logotipo de Signal](assets/img/messengers/signal.svg){ align=right }

**Signal** es una aplicación móvil desarrollada por Signal Messenger LLC. La aplicación ofrece mensajería instantánea y llamadas protegidas con el Protocolo Signal, un protocolo de cifrado extremadamente seguro que admite el secreto hacia adelante[^1] y la seguridad posterior al compromiso.[^2]

[:octicons-home-16: Página Principal](https://signal.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://signal.org/legal/#privacy-policy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://support.signal.org){ .card-link title="Documentación" }
[:octicons-code-16:](https://github.com/signalapp){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://signal.org/donate){ .card-link title="Contribuir" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.thoughtcrime.securesms)
- [:simple-appstore: App Store](https://apps.apple.com/app/id874139669)
- [:simple-android: Android](https://signal.org/android/apk)
- [:fontawesome-brands-windows: Windows](https://signal.org/download/windows)
- [:simple-apple: macOS](https://signal.org/download/macos)
- [:simple-linux: Linux](https://signal.org/download/linux)

</details>

</div>

Signal requiere su número de teléfono para el registro, sin embargo, debería crear un nombre de usuario para ocultar su número de teléfono de sus contactos:

1. En Signal, abra los ajustes de la aplicación y pulse en el perfil de su cuenta en la parte superior.
2. Pulse **Alias** y seleccione **Continuar** en la pantalla "Configure su alias de Signal".
3. Introduzca un alias. Su alias siempre irá emparejado con un único conjunto de dígitos para mantener su alias único y evitar que la gente lo adivine, por ejemplo, si introduce "John" su alias podría terminar siendo `@john.35`. Por defecto, solo se emparejan 2 dígitos con su nombre de usuario cuando lo crea, pero puede añadir más dígitos hasta alcanzar el límite de longitud del nombre de usuario (32 caracteres).
4. Vuelva a la página principal de ajustes de la aplicación y seleccione **Privacidad**.
5. Seleccione **Número de Teléfono**
6. Cambie el ajuste **Quién Puede Ver Mi Número** a: **Nadie**

También puedes cambiar opcionalmente el ajuste **Quién puede Encontrarme por mi Número** a **Nadie**, si quieres evitar que las personas que ya tienen tu número de teléfono descubran tu cuenta/nombre de usuario de Signal.

Las listas de contactos en Signal se cifran utilizando su PIN de Signal y el servidor no tiene acceso a ellas. Los perfiles personales también están encriptados y sólo se comparten con los contactos con los que chatea. Signal admite [grupos privados](https://signal.org/blog/signal-private-group-system), en los que el servidor no tiene constancia de la pertenencia a grupos, títulos de grupos, avatares de grupos o atributos de grupos. Signal tiene pocos metadatos cuando [Remitente Confidencial](https://signal.org/blog/sealed-sender) está activado. La dirección del remitente se encripta junto con el cuerpo del mensaje, y sólo la dirección del destinatario es visible para el servidor. Remitente confidencial sólo está activado para las personas de su lista de contactos, pero se puede activar para todos los destinatarios con el consiguiente riesgo de recibir spam.

El protocolo fue [auditado](https://eprint.iacr.org/2016/1013.pdf) de forma independiente en 2016. La especificación del protocolo Signal puede encontrarse en su [documentación](https://signal.org/docs).

Tenemos algunos consejos adicionales para configurar y endurecer su instalación de Signal:

[Configuración y Endurecimiento de Signal :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening)

#### Molly (Android)

Si utiliza Android y su modelo de amenazas requiere protección contra [:material-target-account: Ataques Dirigidos](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red} puede considerar el uso de esta aplicación alternativa, que cuenta con una serie de mejoras de seguridad y usabilidad, para acceder a la red Signal.

<div class="admonition recommendation" markdown>

![Molly logo](assets/img/messengers/molly.svg){ align=right }

**Molly** es un cliente alternativo de Signal para Android que le permite cifrar la base de datos local con una frase de contraseña en reposo, hacer que los datos de RAM no utilizados se destruyan de forma segura, enrutar su conexión a través de Tor, y [más](https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening#privacy-and-security-features). También presenta mejoras de usabilidad, como copias de seguridad programadas, bloqueo automático y la posibilidad de utilizar su teléfono Android como dispositivo vinculado en lugar de dispositivo principal para una cuenta Signal.

[:octicons-home-16: Página Principal](https://molly.im){ .md-button .md-button--primary }
[:octicons-eye-16:](https://signal.org/legal/#privacy-policy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://github.com/mollyim/mollyim-android/wiki){ .card-link title="Documentación" }
[:octicons-code-16:](https://github.com/mollyim/mollyim-android){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://opencollective.com/mollyim){ .card-link title="Contribuir" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-fdroid: F-Droid](https://molly.im/fdroid)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/im.molly.app)
- [:simple-github: GitHub](https://github.com/mollyim/mollyim-android/releases)

</details>

</div>

Molly se actualiza cada dos semanas para incluir las últimas funciones y correcciones de errores de Signal. La excepción son los problemas de seguridad, que se parchean lo antes posible. Dicho esto, debe tener en cuenta que puede haber un ligero retraso en comparación con la versión anterior, lo que puede afectar a acciones como la [migración de Signal a Molly](https://github.com/mollyim/mollyim-android/wiki/Migrating-From-Signal#migrating-from-signal).

Tenga en cuenta que está confiando en múltiples partes al utilizar Molly, ya que ahora necesita confiar en el equipo de Signal *y* en el equipo de Molly para entregar actualizaciones seguras y oportunas.

Existe una versión de Molly llamada **Molly-FOSS** que elimina el código propietario como los servicios de Google utilizados tanto por Signal como por Molly, a costa de algunas características como las notificaciones push que ahorran batería a través de Google Play Services.

There is also a version called [**Molly-UP**](https://github.com/mollyim/mollyim-android#unifiedpush) which is based on Molly-FOSS and adds support for push notifications with [UnifiedPush](https://unifiedpush.org), an open source alternative to the push notifications provided by Google Play Services, but it requires running a separate program called [Mollysocket](https://github.com/mollyim/mollysocket) to function. Mollysocket can either be self-hosted on a separate computer or server (VPS), or alternatively a public Mollysocket instance can be used ([step-by-step tutorial, in German](https://kuketz-blog.de/messenger-wechsel-von-signal-zu-molly-unifiedpush-mollysocket-ntfy)).

Las tres versiones de Molly ofrecen las mismas mejoras de seguridad.

Molly y Molly-FOSS admiten [compilaciones reproducibles](https://github.com/mollyim/mollyim-android/tree/main/reproducible-builds), lo que significa que es posible confirmar que los APK compilados coinciden con el código fuente.

### SimpleX Chat

<div class="admonition recommendation" markdown>

![Simplex logo](assets/img/messengers/simplex.svg){ align=right }

**SimpleX** Chat es un servicio de mensajería instantánea descentralizado que no depende de ningún identificador único, como números de teléfono o nombres de usuario. Su red descentralizada hace de SimpleX Chat una herramienta eficaz contra la [:material-close-outline: Censura](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }.

[:octicons-home-16: Página Principal](https://simplex.chat){ .md-button .md-button--primary }
[:octicons-eye-16:](https://simplex.chat/privacy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://simplex.chat/docs/simplex.html){ .card-link title="Documentación" }
[:octicons-code-16:](https://github.com/simplex-chat){ .card-link title="Código Fuente" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=chat.simplex.app)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1605771084)
- [:simple-github: GitHub](https://github.com/simplex-chat/simplex-chat/releases)
- [:fontawesome-brands-windows: Windows](https://simplex.chat/downloads/#desktop-app)
- [:simple-apple: macOS](https://simplex.chat/downloads/#desktop-app)
- [:simple-linux: Linux](https://simplex.chat/downloads/#desktop-app)

</details>

</div>

SimpleX proporciona mensajería directa, chats de grupo y llamadas E2EE protegidas con el [protocolo de mensajería SimpleX](https://github.com/simplex-chat/simplexmq/blob/stable/protocol/simplex-messaging.md), que utiliza cifrado de doble trinquete con resistencia cuántica. Además, SimpleX Chat proporciona protección de metadatos mediante el uso de ["colas simplex](https://github.com/simplex-chat/simplexmq/blob/stable/protocol/simplex-messaging.md#simplex-queue) " unidireccionales para entregar mensajes.

Para participar en conversaciones en SimpleX Chat, debe escanear un código QR o hacer clic en un enlace de invitación. Esto le permite verificar un contacto fuera de banda, lo que le protege contra los ataques man-in-the-middle por parte de los proveedores de red. Sus datos pueden ser exportados e importados a otro dispositivo, ya que no hay servidores centrales donde se hace una copia de seguridad.

Puede encontrar una lista completa de las [funciones](https://github.com/simplex-chat/simplex-chat#privacy-and-security-technical-details-and-limitations) de privacidad y seguridad implementadas en SimpleX Chat en el repositorio de la aplicación.

SimpleX Chat fue auditada de forma independiente en [julio de 2024](https://simplex.chat/blog/20241014-simplex-network-v6-1-security-review-better-calls-user-experience.html#simplex-cryptographic-design-review-by-trail-of-bits) y en [octubre de 2022](https://simplex.chat/blog/20221108-simplex-chat-v4.2-security-audit-new-website).

### Briar

<div class="admonition recommendation" markdown>

![Briar logo](assets/img/messengers/briar.svg){ align=right }

**Briar** es un servicio de mensajería instantánea cifrado que [se conecta](https://briarproject.org/how-it-works) a otros clientes utilizando la Red Tor, lo que lo convierte en una herramienta eficaz para eludir la [:material-close-outline: Censura](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }. Briar también puede conectarse a través de Wi-Fi o Bluetooth si está cerca. El modo de malla local de Briar puede ser útil cuando la disponibilidad de Internet es un problema.

[:octicons-home-16: Página Principal](https://briarproject.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://briarproject.org/privacy-policy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://code.briarproject.org/briar/briar/-/wikis/home){ .card-link title="Documentación" }
[:octicons-code-16:](https://code.briarproject.org/briar/briar){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://briarproject.org){ .card-link title="Las opciones de donación están listadas en la parte inferior de la página principal" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.briarproject.briar.android)
- [:fontawesome-brands-windows: Windows](https://briarproject.org/download-briar-desktop)
- [:simple-linux: Linux](https://briarproject.org/download-briar-desktop)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.briarproject.Briar)

</details>

</div>

Para añadir un contacto en Briar, ambos deben añadirse entre sí primero. Puede intercambiar enlaces `briar://` o escanear el código QR de un contacto si están cerca.

El software cliente fue [auditado](https://briarproject.org/news/2017-beta-released-security-audit) de forma independiente, y el protocolo de enrutamiento anónimo utiliza la red Tor, que también ha sido auditada.

Briar tiene una [especificación publicada](https://code.briarproject.org/briar/briar-spec) completamente.

Briar soporta el secreto hacia delante[^1] utilizando el protocolo Bramble [Handshake](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BHP.md) y [Transport](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BTP.md).

## Opciones Adicionales

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

Estos mensajeros no tienen secreto hacia adelante[^1], y aunque satisfacen ciertas necesidades que nuestras recomendaciones anteriores pueden no satisfacer, no los recomendamos para comunicaciones a largo plazo o sensibles. Cualquier compromiso de claves entre los destinatarios de los mensajes afectaría a la confidencialidad de **todas** las comunicaciones anteriores.

</div>

### Element

<div class="admonition recommendation" markdown>

![Element logo](assets/img/messengers/element.svg){ align=right }

**Element** es el cliente insignia del protocolo [Matrix](https://matrix.org/docs/chat_basics/matrix-for-im), un [estándar abierto](https://spec.matrix.org/latest) para la comunicación segura descentralizada en tiempo real.

Los mensajes y archivos compartidos en salas privadas (aquellas que requieren invitación) son por defecto E2EE, al igual que las llamadas de voz y vídeo uno a uno.

[:octicons-home-16: Página Principal](https://element.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://element.io/privacy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://element.io/help){ .card-link title="Documentación" }
[:octicons-code-16:](https://github.com/element-hq){ .card-link title="Código Fuente" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=im.vector.app)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1083446067)
- [:simple-github: GitHub](https://github.com/element-hq/element-android/releases)
- [:fontawesome-brands-windows: Windows](https://element.io/download)
- [:simple-apple: macOS](https://element.io/download)
- [:simple-linux: Linux](https://element.io/download)
- [:octicons-globe-16: Web](https://app.element.io)

</details>

</div>

Las fotos de perfil, las reacciones y los apodos no están cifrados.

Con la integración de [Element Call](https://element.io/blog/we-have-lift-off-element-x-call-and-server-suite-are-ready) en la aplicación web de Element, las aplicaciones de escritorio y sus [aplicaciones móviles reescritas](https://element.io/blog/element-x-experience-the-future-of-element), las llamadas VoIP y las videollamadas en grupo son E2EE por defecto.

El propio protocolo Matrix [soporta teóricamente el secreto hacia adelante](https://gitlab.matrix.org/matrix-org/olm/blob/master/docs/megolm.md#partial-forward-secrecy)[^1], sin embargo [no está soportado actualmente en Element](https://github.com/vector-im/element-web/issues/7101) debido a que rompe algunos aspectos de la experiencia del usuario como las copias de seguridad de claves y el historial de mensajes compartidos.

El protocolo fue [auditado](https://matrix.org/blog/2016/11/21/matrixs-olm-end-to-end-encryption-security-assessment-released-and-implemented-cross-platform-on-riot-at-last) de forma independiente en 2016. La especificación del protocolo Matrix puede encontrarse en su [documentación](https://spec.matrix.org/latest). El [trinquete criptográfico Olm](https://matrix.org/docs/matrix-concepts/end-to-end-encryption) utilizado por Matrix es una implementación del [algoritmo Double Ratchet](https://signal.org/docs/specifications/doubleratchet) de Signal.

### Session

<div class="admonition recommendation" markdown>

![Session logo](assets/img/messengers/session.svg){ align=right }

**Session** es un servicio de mensajería descentralizado centrado en las comunicaciones privadas, seguras y anónimas. Session ofrece soporte para mensajes directos, chats de grupo y llamadas de voz.

Session utiliza la red descentralizada [Oxen Service Node Network](https://oxen.io/) para almacenar y enrutar los mensajes. Cada mensaje encriptado pasa por tres nodos de la Oxen Service Node Network, lo que hace prácticamente imposible que los nodos recopilen información significativa sobre quienes utilizan la red.

[:octicons-home-16: Página Principal](https://getsession.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://getsession.org/privacy-policy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://getsession.org/faq){ .card-link title="Documentación" }
[:octicons-code-16:](https://github.com/oxen-io){ .card-link title="Código Fuente" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=network.loki.messenger)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1470168868)
- [:simple-github: GitHub](https://github.com/oxen-io/session-android/releases)
- [:fontawesome-brands-windows: Windows](https://getsession.org/download)
- [:simple-apple: macOS](https://getsession.org/download)
- [:simple-linux: Linux](https://getsession.org/download)

</details>

</div>

Session permite E2EE en chats individuales o grupos cerrados que admiten hasta 100 miembros. Los grupos abiertos no tienen ninguna restricción en cuanto al número de miembros, pero son abiertos por diseño.

Session se basaba anteriormente en el Protocolo Signal antes de sustituirlo por el suyo propio en diciembre de 2020. El Protocolo Sesion [no](https://getsession.org/blog/session-protocol-technical-information) soporta el secreto hacia adelante.[^1]

Oxen solicitó una auditoría independiente para Session en marzo de 2020. La auditoría [concluyó](https://getsession.org/session-code-audit) en abril de 2021:

> El nivel general de seguridad de esta aplicación es bueno y la hace utilizable para personas preocupadas por su privacidad.

Session tiene un [informe oficial](https://arxiv.org/pdf/2002.04609.pdf) que describe los aspectos técnicos de la aplicación y el protocolo.

## Criterios

**Por favor, tenga en cuenta que no estamos afiliados con ninguno de los proyectos que recomendamos.** Además de [nuestros criterios estándar](about/criteria.md), hemos desarrollado un conjunto claro de requisitos que nos permiten ofrecer recomendaciones objetivas. Sugerimos que usted se familiarice con esta lista, antes de decidir utilizar un proyecto y realizar su propia investigación para asegurarse de que es la elección ideal para usted.

### Requisitos Mínimos

- Tiene clientes de código abierto.
- No requiere compartir identificadores personales (números de teléfono o correos electrónicos en particular) con los contactos.
- Utiliza por defecto E2EE para los mensajes privados.
- Admite E2EE para todos los mensajes.
- Ha sido objeto de una auditoría independiente.

### Mejor Caso

Nuestro criterio del mejor caso representa lo que nos gustaría ver del proyecto perfecto en esta categoría. Es posible que nuestras recomendaciones no incluyan todas o algunas de estas funciones, pero las que sí las incluyan pueden estar mejor clasificadas que otras en esta página.

- Admite el secreto hacia adelante[^1]
- Admite el Secreto Futuro (Seguridad Poscompromiso)[^2]
- Dispone de servidores de código abierto.
- Descentralizado, es decir, [federado o P2P](advanced/communication-network-types.md).
- Utiliza E2EE para todos los mensajes por defecto.
- Compatible con Linux, macOS, Windows, Android e iOS.

[^1]: [El secreto hacia adelante](https://en.wikipedia.org/wiki/Forward_secrecy) es cuando las claves se rotan con mucha frecuencia, de modo que si la clave de cifrado actual se ve comprometida, no expone también los mensajes **anteriores**.
[^2]: El Secreto Futuro (o Seguridad Poscompromiso) es una característica que impide a un atacante descifrar mensajes **futuros** después de comprometer una clave privada, a menos que comprometa también más claves de sesión en el futuro. Esto obliga al atacante a interceptar todas las comunicaciones entre las partes, ya que pierde el acceso en cuanto se produce un intercambio de claves que no es interceptado.
