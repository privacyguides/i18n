---
meta_title: "Los Mejores Servicios de Mensajería Instantánea Privados - Privacy Guides"
title: Comunicación en Tiempo Real
icon: material/chat-processing
description: Los servicios de mensajería cifrados como Signal y SimpleX mantienen sus comunicaciones confidenciales a salvo de miradas indiscretas.
cover: real-time-communication.webp
---

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-bug-outline: Ataques pasivos](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: Proveedores de servicios](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}
- [:material-eye-outline: Vigilancia masiva](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-account-cash: Capitalismo de Vigilancia](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Estas recomendaciones para la **comunicación en tiempo real** encriptada son ideales para proteger sus comunicaciones confidenciales. Estos servicios de mensajería instantánea se presentan en forma de muchos [tipos de redes de comunicación](advanced/communication-network-types.md).

[:material-movie-open-play-outline: Vídeo: Es hora de dejar de utilizar los SMS](https://www.privacyguides.org/videos/2025/01/24/its-time-to-stop-using-sms-heres-why ""){.md-button}

## Signal

<div class="admonition recommendation" markdown>

![Logotipo de Signal](assets/img/messengers/signal.svg){ align=right }

**Signal** es una aplicación móvil desarrollada por Signal Messenger LLC. La aplicación ofrece mensajería instantánea y llamadas protegidas con el protocolo Signal, un protocolo de cifrado extremadamente seguro que admite el secreto hacia adelante[^1] y la seguridad posterior al compromiso.[^2]

[:octicons-home-16: Página Principal](https://signal.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://signal.org/legal/#privacy-policy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://support.signal.org){ .card-link title="Documentación" }
[:octicons-code-16:](https://github.com/signalapp){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://signal.org/donate){ .card-link title="Contribuir" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.thoughtcrime.securesms)
- [:simple-appstore: App Store](https://apps.apple.com/app/id874139669)
- [:simple-github: GitHub](https://github.com/signalapp/Signal-Android/releases)
- [:simple-android: Android](https://signal.org/android/apk)
- [:fontawesome-brands-windows: Windows](https://signal.org/download/windows)
- [:simple-apple: macOS](https://signal.org/download/macos)
- [:simple-linux: Linux](https://signal.org/download/linux)

</details>

</div>

Signal requiere su número de teléfono para el registro, sin embargo, debe crear un nombre de usuario para ocultar su número de teléfono de sus contactos:

1. En Signal, abra los ajustes de la aplicación y pulse en el perfil de su cuenta en la parte superior.
2. Pulse **Alias** y seleccione **Continuar** en la pantalla "Configure su alias de Signal".
3. Introduzca un alias. Su nombre de usuario siempre estará emparejado con un conjunto único de dígitos para mantener su alias único y evitar que la gente lo adivine. Por ejemplo, si introduce «John», su alias puede acabar siendo `@john.35`. Por defecto, solo se emparejan 2 dígitos con su nombre de usuario cuando lo crea, pero puede añadir más dígitos hasta alcanzar el límite de longitud del nombre de usuario (32 caracteres).
4. Vuelva a la página principal de ajustes de la aplicación y seleccione **Privacidad**.
5. Seleccione **Número de Teléfono**.
6. Cambie el ajuste **Quién Puede Ver Mi Número** a **Nadie**.
7. (Opcional) Cambie también el ajuste **Quién Puede Encontrarme Con Mi Número** a **Nadie**, si quiere evitar que las personas que ya tienen su número de teléfono descubran su cuenta/alias de Signal

Tenemos algunos consejos adicionales para configurar y reforzar su instalación de Signal:

[Configuración e Incremento de la Seguridad de Signal :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening)

Las listas de contactos en Signal se cifran utilizando su PIN de Signal y el servidor no tiene acceso a ellas. Los perfiles personales también están cifrados y solo se comparten con los contactos con los que chatea.

Signal admite [grupos privados](https://signal.org/blog/signal-private-group-system), en los que el servidor no tiene constancia de la pertenencia a grupos, títulos de grupos, avatares de grupos o atributos de grupos. Signal tiene pocos metadatos cuando [Remitente Confidencial](https://signal.org/blog/sealed-sender) está activado. La dirección del remitente se encripta junto con el cuerpo del mensaje, y solo la dirección del destinatario es visible para el servidor. Remitente Confidencial solo está activado para las personas de su lista de contactos, pero se puede activar para todos los destinatarios con un mayor riesgo de recibir spam.

El protocolo fue [auditado](https://eprint.iacr.org/2016/1013.pdf) independientemente en 2016. La especificación del protocolo Signal puede encontrarse en su [documentación](https://signal.org/docs).

### Molly (Android)

Si utiliza Android y su modelo de amenazas requiere protección frente a [:material-target-account: Ataques Dirigidos](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}, puede considerar el uso de esta aplicación alternativa, que presenta una serie de mejoras de seguridad y usabilidad, para acceder a la red Signal.

<div class="admonition recommendation" markdown>

![Logo de Molly](assets/img/messengers/molly.svg){ align=right }

**Molly** es un cliente de Android alternativo a Signal que te permite cifrar la base de datos local con una contraseña en reposo, elimina de forma segura los datos de memoria RAM no utilizados, enruta las conversaciones via Tor, y [más](https://www.privacyguides.org/articles/2022/07/07/signal-configuration-and-hardening#privacy-and-security-features). También presenta mejoras de usabilidad, como copias de seguridad programadas, bloqueo automático y la posibilidad de utilizar su teléfono Android como dispositivo vinculado en lugar de dispositivo principal para una cuenta Signal.

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

Tenga en cuenta que está confiando en varias partes al utilizar Molly, ya que ahora necesita confiar en el equipo de Signal *y en* el equipo de Molly para que le proporcionen actualizaciones seguras y puntuales.

Molly proporciona soporte para [construcciones reproducibles](https://github.com/mollyim/mollyim-android/tree/main/reproducible-builds) lo que hace posible confirmar que los APK compilados coinciden con el código fuente.

## SimpleX Chat

<div class="admonition recommendation" markdown>

![Logotipo de SimpleX Chat](assets/img/messengers/simplex.svg){ align=right }

**SimpleX Chat** es un servicio de mensajería instantánea que no depende de ningún identificador único, como números de teléfono o nombres de usuario. Su red descentralizada hace de SimpleX Chat una herramienta eficaz contra la [:material-close-outline: Censura](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }.

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
- [:simple-flathub: Flathub](https://flathub.org/en/apps/chat.simplex.simplex)

</details>

</div>

SimpleX Chat proporciona mensajería directa, chats de grupo y llamadas E2EE protegidas con el [Protocolo de Mensajería SimpleX](https://github.com/simplex-chat/simplexmq/blob/stable/protocol/simplex-messaging.md), que utiliza cifrado de doble trinquete con resistencia cuántica. Además, SimpleX Chat proporciona protección de metadatos mediante el uso de [«colas simplex»](https://github.com/simplex-chat/simplexmq/blob/stable/protocol/simplex-messaging.md#simplex-queue) unidireccionales para entregar mensajes.

Para participar en conversaciones en SimpleX Chat, debe escanear un código QR o hacer clic en un enlace de invitación. Esto le permite verificar un contacto fuera de banda, lo que le protege contra los ataques «man-in-the-middle» por parte de los proveedores de red. Sus datos pueden ser exportados e importados a otro dispositivo, ya que no hay servidores centrales donde se haga una copia de seguridad.

Puede encontrar una lista completa de las [funciones](https://github.com/simplex-chat/simplex-chat#privacy-and-security-technical-details-and-limitations) de privacidad y seguridad implementadas en SimpleX Chat en el repositorio de la aplicación.

SimpleX Chat fue auditada de forma independiente en [julio de 2024](https://simplex.chat/blog/20241014-simplex-network-v6-1-security-review-better-calls-user-experience.html#simplex-cryptographic-design-review-by-trail-of-bits) y en [octubre de 2022](https://simplex.chat/blog/20221108-simplex-chat-v4.2-security-audit-new-website).

## Briar

<div class="admonition recommendation" markdown>

![Briar logo](assets/img/messengers/briar.svg){ align=right }

**Briar** es un servicio de mensajería instantánea cifrado que [se conecta](https://briarproject.org/how-it-works) a otros clientes utilizando la [red Tor](alternative-networks.md#tor), lo que lo convierte en una herramienta eficaz para eludir la [:material-close-outline: Censura](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }. Briar también puede conectarse a través de Wi-Fi o Bluetooth si está cerca. El modo de malla local de Briar puede ser útil cuando la disponibilidad de Internet es un problema.

[:octicons-home-16: Página Principal](https://briarproject.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://briarproject.org/privacy-policy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://code.briarproject.org/briar/briar/-/wikis/home){ .card-link title="Documentación" }
[:octicons-code-16:](https://code.briarproject.org/briar/briar){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://code.briarproject.org/briar/briar#donate){ .card-link title="Contribuir" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.briarproject.briar.android)
- [:fontawesome-brands-windows: Windows](https://briarproject.org/download-briar-desktop)
- [:simple-linux: Linux](https://briarproject.org/download-briar-desktop)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.briarproject.Briar)

</details>

</div>

Para añadir un contacto en Briar, ambos deben añadirse entre sí primero. Pueden intercambiar enlaces `briar://` o escanear el código QR de un contacto si está cerca.

Briar tiene un [pliego de condiciones publicado](https://code.briarproject.org/briar/briar-spec). Briar soporta el secreto hacia delante[^1] utilizando los protocolos Bramble [Handsake](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BHP.md) y [Transport](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BTP.md).

El software cliente fue [auditado](https://briarproject.org/news/2017-beta-released-security-audit) de forma independiente, y el protocolo de enrutamiento anónimo utiliza la red Tor, que también ha sido auditada.

## Criterios

**Por favor, ten en cuenta que no estamos afiliados con ninguno de los proyectos que recomendamos.** Además de [nuestros criterios estándar](about/criteria.md), hemos desarrollado un conjunto claro de requisitos que nos permiten ofrecer recomendaciones objetivas. Sugerimos que te familiarices con esta lista, antes de decidir utilizar un proyecto y realizar tu propia investigación para asegurarte de que es la elección ideal para ti.

### Requisitos Mínimos

- Debe tener clientes de código abierto.
- No debe requerir compartir identificadores personales (particularmente números de teléfono o correos electrónicos) con los contactos.
- Debe utilizar E2EE para los mensajes privados por defecto.
- Debe ser compatible con E2EE para todos los mensajes.
- Debe dar soporte al secreto hacia delante[^1]
- Debe contar con una auditoría publicada de un tercero independiente y acreditado.

### Mejor Caso

Nuestro criterio del mejor caso representa lo que nos gustaría ver del proyecto perfecto en esta categoría. Es posible que nuestras recomendaciones no incluyan todas o algunas de estas funciones, pero las que sí las incluyan pueden estar mejor clasificadas que otras en esta página.

- Debe dar soporte a secreto futuro (seguridad post compromiso)[^2]
- Debería tener servidores de código abierto.
- Debería utilizar una red descentralizada, es decir, [federada o P2P](advanced/communication-network-types.md).
- Debería utilizar E2EE para todos los mensajes por defecto.
- Debería ser compatible con Linux, macOS, Windows, Android e iOS.

[^1]: El [secreto hacia adelante](https://en.wikipedia.org/wiki/Forward_secrecy) consiste en que las claves se rotan con mucha frecuencia, de modo que si la clave de cifrado actual se ve comprometida, no expone también los mensajes **anteriores**.
[^2]: El secreto futuro (o [seguridad poscompromiso](https://eprint.iacr.org/2016/221.pdf)) es una característica que impide a un atacante descifrar **futuros** mensajes tras comprometer una clave privada, a menos que comprometa también más claves de sesión en el futuro. Esto obliga al atacante a interceptar todas las comunicaciones entre las partes, ya que pierde el acceso en cuanto se produce un intercambio de claves que no es interceptado.
