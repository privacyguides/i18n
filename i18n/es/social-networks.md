---
title: Redes Sociales
icon: material/account-supervisor-circle-outline
description: Encuentra una nueva red social que no husmee en tus datos ni monetice tu perfil.
cover: social-networks.webp
---

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-close-outline: Censura](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }
- [:material-account-cash: Capitalismo de Vigilancia](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

Estas **redes sociales** respetuosas con la privacidad te permiten participar en comunidades online sin tener que dar tu información personal, como tu nombre completo, número de teléfono y otros datos que suelen pedir las empresas tecnológicas.

Un problema creciente entre las plataformas de redes sociales es la censura en dos formas diferentes. En primer lugar, a menudo acceden a peticiones de censura ilegítimas, ya sea de gobiernos malintencionados o de sus propias políticas internas. En segundo lugar, a menudo exigen cuentas para acceder a contenidos amurallados que de otro modo se publicarían libremente en la Internet abierta; esto censura las actividades de navegación de los usuarios preocupados por su privacidad que no pueden pagar el coste de privacidad que supone abrir una cuenta en estas redes.

Las redes sociales que recomendamos resuelven el problema de la censura al funcionar con un protocolo de red social abierto y descentralizado. Tampoco requieren una cuenta para solamente ver los contenidos disponibles públicamente.

Deberías tener en cuenta que **ninguna** red social es apropiada para comunicaciones privadas o sensibles. Para chatear directamente con otras personas, deberías utilizar un [servicio de mensajería instantánea] recomendado(real-time-communication.md) con un cifrado fuerte de extremo a extremo, y solo utilizar mensajes directos en las redes sociales para establecer una plataforma de chat más privada y segura con tus contactos.

## Descentralización

Las redes sociales descentralizadas se basan en una arquitectura fundamentalmente diferente a la de las principales plataformas de redes sociales, aunque bastante similar a la estructura subyacente del correo electrónico. En lugar de abrir una cuenta en un servicio único y unificado, como harías en Facebook o Discord, eliges un servidor público independiente al que unirte. El servidor al que te unes puede comunicarse con otros servidores y descubrirlos; este aspecto de la descentralización también se conoce como _federación_.

Una ventaja importante de este modelo descentralizado es que no existe una autoridad central que pueda censurar tu cuenta en toda la red, aunque es posible que un servidor individual la bloquee o silencie.

Una limitación de este modelo descentralizado es que cada servidor es su propia entidad legal, con su propia política de privacidad, condiciones de uso, equipo de administración y moderadores. Aunque muchos de estos servidores son mucho _menos_ restrictivos y respetan más la privacidad que las plataformas tradicionales de redes sociales, algunos pueden ser mucho _más_ restrictivos o potencialmente _peores_ para tu privacidad. Normalmente, el software sobre el que funciona la red social no discrimina entre estos administradores ni impone limitaciones a sus poderes.

## Resistencia a la Censura

Mientras que la censura en las redes sociales descentralizadas no existe a nivel de red, es muy posible experimentar censura a nivel de servidor dependiendo del administrador del mismo. Los administradores tienen el poder de _defederarse_ de otros servidores, lo que lleva a limitar el contenido que puedes ver y la gente con la que puedes interactuar.

Si te preocupa mucho que un servidor existente censure tu contenido, el contenido disponible para ti u otros servidores, generalmente tienes dos opciones:

1. **Aloja tú mismo el software de la red social.** Este enfoque te da exactamente la misma resistencia a la censura que cualquier otro sitio web que puedas alojar tú mismo, la cual es bastante alta.

2. **Utiliza un servicio de alojamiento gestionado.** No tenemos recomendaciones específicas, pero hay una gran variedad de servicios de alojamiento que crearán un servidor completamente nuevo en tu propio dominio (u ocasionalmente un subdominio de su dominio, pero no lo recomendamos a menos que registrar tu propio dominio suponga una carga demasiado grande para tu privacidad).

    Normalmente, los proveedores de alojamiento se encargan de la parte _técnica_ de tu servidor, pero dejan completamente en tus manos la _moderación_. Esto suele ser mejor que el autoalojamiento para la mayoría de la gente, ya que puedes beneficiarte de un mayor control sobre tu propio servidor sin preocuparte por problemas técnicos o vulnerabilidades de seguridad sin parchear.

    Antes de registrarte, deberías leer atentamente las condiciones de servicio y la política de uso aceptable de tu proveedor de alojamiento. Suelen ser mucho más amplias que las normas típicas de los servidores alojados, y es mucho menos probable que se apliquen sin recurso, pero aun así pueden ser restrictivas de formas no deseadas.

## Mastodon

<div class="admonition recommendation" markdown>

![Mastodon logo](assets/img/social-networks/mastodon.svg){ align=right }

**Mastodon** es una red social basada en protocolos web abiertos y software libre de código abierto. Utiliza el protocolo **:simple-activitypub: ActivityPub**, que está descentralizado como el correo electrónico: los usuarios pueden estar en distintos servidores o incluso plataformas, pero seguir comunicándose entre sí.

[:octicons-home-16: Página Principal](https://joinmastodon.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.joinmastodon.org){ .card-link title="Documentación" }

</div>

Hay muchas plataformas de software que utilizan ActivityPub como su protocolo de red social backend, lo que significa que pueden hablar con los servidores incluso cuando están ejecutando un software diferente. Por ejemplo, PeerTube es un software de publicación de vídeo que utiliza ActivityPub, lo que significa que puedes seguir canales en PeerTube con otra cuenta de PeerTube, _o_ con una cuenta de Mastodon porque Mastodon también utiliza ActivityPub.

Decidimos recomendar Mastodon sobre otro software ActivityPub como tu principal plataforma de redes sociales por estas razones:

1. Mastodon tiene un sólido historial de actualizaciones de seguridad. En las varias circunstancias en las que se han encontrado vulnerabilidades de seguridad importantes, han coordinado la publicación de parches de forma rápida y limpia. Históricamente, también han aplicado estos parches de seguridad a ramas más antiguas. Esto facilita la tarea de los anfitriones de servidores con menos experiencia que no se sientan cómodos actualizando a las últimas versiones de inmediato para mantener la seguridad de sus instancias. Mastodon también cuenta con un sistema de notificación de actualizaciones integrado en la interfaz web, lo que hace mucho más probable que los administradores de servidores estén al tanto de los parches de seguridad críticos disponibles para su instancia.

2. Mastodon es ampliamente utilizable con la mayoría de los tipos de contenido. Aunque es principalmente una plataforma de microblogging, Mastodon maneja fácilmente publicaciones más largas, publicaciones de imágenes, publicaciones de vídeo y la mayoría de las otras publicaciones que puedes encontrar cuando sigues a usuarios de ActivityPub que no están en Mastodon. Esto convierte tu cuenta de Mastodon en un "eje central" ideal para seguir a cualquier persona, independientemente de la plataforma que elija utilizar. En cambio, si solo utilizaras una cuenta de PeerTube, _solo_ podrías seguir otros canales de vídeo, por ejemplo.

3. Mastodon tiene controles de privacidad bastante completos. Tiene muchas funciones integradas que te permiten limitar cómo y cuándo se comparten tus datos, algunas de las cuales veremos a continuación. También desarrollan nuevas funciones pensando en la privacidad. Por ejemplo, mientras que otros programas con ActivityPub han implementado rápidamente las "publicaciones citadas" limitándose a gestionar los enlaces a otras publicaciones con un modo de incrustación ligeramente diferente, Mastodon está [desarrollando](https://blog.joinmastodon.org/2025/02/bringing-quote-posts-to-mastodon) una función de publicación citada que te proporcionará un control más preciso cuando se cite tu publicación.

### Elegir una Instancia

Para beneficiarse al máximo de Mastodon, es fundamental elegir un servidor, o una "instancia", que esté bien alineado con el tipo de contenido que deseas publicar o leer. Actualmente no recomendamos ninguna instancia específica, pero puedes encontrar asesoramiento en nuestras comunidades. Recomendamos evitar _mastodon.social_ y _mastodon.online_ porque están operados por la misma empresa que desarrolla el propio Mastodon. Desde el punto de vista de la descentralización, es mejor a largo plazo separar a los desarrolladores de software y los servidores anfitriones para que ninguna de las partes pueda ejercer demasiado control sobre la red en su conjunto.

### Ajustes de Privacidad Recomendados

Desde la interfaz web de Mastodon, haz clic en el enlace **Preferencias** de la barra lateral derecha. Dentro del panel de control de administración, encontrarás estas secciones en la barra lateral izquierda:

#### Perfil Público

Hay una serie de controles de privacidad en la pestaña **privacidad y alcance**. Sobre todo, presta atención a estos:

- [ ] **Aceptar automáticamente nuevos seguidores**: Deberías considerar desmarcar esta casilla para tener un perfil privado. Esto te permitirá revisar quién puede seguir tu cuenta antes de aceptarlos.

    A diferencia de la mayoría de las plataformas de redes sociales, si tienes un perfil privado todavía tienes la _opción_ de publicar mensajes que son visibles públicamente para los que no te siguen y que pueden ser impulsados por los que no te siguen. Por lo tanto, desmarcar esta casilla es la única manera de tener la _opción_ de publicar para todo el mundo o para un grupo selecto de personas.

- [ ] **Mostrar seguidos y seguidores en el perfil**: Deberías desmarcar esta casilla para ocultar tu gráfico social al público. Es bastante infrecuente que la lista de personas a las que sigues tenga algún beneficio genuino para los demás, pero esa información puede suponer un riesgo para ti.

- [ ] **Mostrar desde qué aplicación enviaste una publicación**: Deberías desmarcar esta casilla para evitar revelar información sobre tu configuración informática personal a otras personas innecesariamente.

Conviene leer los demás controles de privacidad de esta página, pero insistimos en que **no** son controles técnicos, sino meras peticiones que haces a los demás. Por ejemplo, si eliges ocultar tu perfil de los buscadores en esta página, **nada** impide realmente que un buscador lea tu perfil. Simplemente estás solicitando a los índices de los buscadores que no muestren tu contenido a sus usuarios.

Es probable que con todo esto sigas deseando hacer estas solicitudes porque prácticamente pueden reducir tu huella digital. Sin embargo, no se debe _depender_ de ellos. La única forma eficaz de ocultar tus publicaciones a los buscadores y a otras personas es publicar con una configuración de visibilidad no pública (solo para seguidores) _y_ limitar quién puede seguir tu cuenta.

#### Preferencias

Deberías cambiar la configuración de tu **privacidad de publicaciones** de pública a: **Solo seguidores - Solo mostrar a tus seguidores**.

Ten en cuenta que esto solo cambia la configuración predeterminada para evitar que se comparta más de la cuenta accidentalmente. Siempre puedes ajustar tu nivel de visibilidad al redactar una nueva publicación.

#### Eliminación automática de publicaciones

- [x] Marca la casilla **Borrar automáticamente publicaciones antiguas**.

La configuración predeterminada aquí está bien, y borrará cualquier publicación que hagas después de 2 semanas, a menos que lo marques como favorito (estrella). Esto te permite controlar fácilmente qué publicaciones permanecen para siempre y cuáles son efímeras. Sin embargo, aquí se pueden ajustar muchos parámetros sobre cuánto tiempo y cuándo se guardan las publicaciones para adaptarlos a tus propias necesidades.

Es muy raro que las publicaciones en las redes sociales con más de unas semanas de antigüedad sean leídas o relevantes para los demás. A menudo se ignoran estas publicaciones antiguas porque son difíciles de tratar en masa, pero con el tiempo pueden crear un perfil bastante completo sobre ti. Siempre debes esforzarte por publicar contenido de forma efímera por defecto, y solo mantener las publicaciones durante más tiempo de forma muy intencionada.

### Publicar Contenido

Al realizar una nueva publicación, tendrás la opción de elegir una de estas opciones de visibilidad:

- **Pública**, que muestra tu contenido a cualquier persona en Internet.
- **Pública silenciosa**, ¡lo que debería considerar equivalente a hacerla pública! Esto no es una garantía técnica, sino simplemente una petición que estás haciendo a otros servidores para ocultar tu publicación de algunas fuentes.
- **Seguidores**, que muestra tu contenido solo a tus seguidores. Si no has seguido nuestra recomendación de restringir tus seguidores, ¡deberías considerar que esto equivale a hacerla pública!
- **Personas específicas**, que solo comparte la publicación con las personas que se mencionan específicamente en la publicación. Esta es la versión de Mastodon de los mensajes directos, pero nunca se debe confiar en ellos para las comunicaciones privadas, ya que como hemos cubierto anteriormente, Mastodon no tiene E2EE.

Si has utilizado nuestros ajustes de configuración recomendados arriba, deberías publicar en **Seguidores** por defecto, y solo publicar en **Público** de forma intencionada y en casos determinados.

## Element

<div class="admonition recommendation" markdown>

![Element logo](assets/img/social-networks/element.svg){ align=right }

**Element** es el cliente insignia del protocolo **:simple-matrix: [Matrix](https://matrix.org/docs/chat_basics/matrix-for-im)**, un [estándar abierto](https://spec.matrix.org/latest) que permite la comunicación descentralizada mediante salas de chat federadas. Los usuarios pueden existir en diferentes servidores domésticos y seguir comunicándose entre sí.

[:octicons-home-16: Página Principal](https://element.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://element.io/privacy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://element.io/help){ .card-link title="Documentación" }
[:octicons-code-16:](https://github.com/element-hq){ .card-link title="Código Fuente" }

<details class="downloads" markdown><summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=im.vector.app)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1083446067)
- [:simple-github: GitHub](https://github.com/element-hq/element-android/releases)
- [:fontawesome-brands-windows: Windows](https://element.io/download)
- [:simple-apple: macOS](https://element.io/download)
- [:simple-linux: Linux](https://element.io/download)
- [:octicons-browser-16: Web](https://app.element.io)

</details>

</div>

### Elegir un Servidor Doméstico

Para sacar el máximo provecho de Matrix, es fundamental elegir un servidor doméstico que esté bien alineado con el tema o los temas sobre los que se quiere charlar. Actualmente no recomendamos ningún servidor doméstico específico, pero puedes encontrar recomendaciones en nuestras comunidades o en recursos de terceros como [_joinmatrix.org_](https://servers.joinmatrix.org). Recomendamos evitar _matrix.org_ porque está gestionado por la misma empresa que desarrolla el propio Matrix. Desde el punto de vista de la descentralización, es mejor a largo plazo separar a los desarrolladores de software y los servidores anfitriones para que ninguna de las partes pueda ejercer demasiado control sobre la red en su conjunto.

### Ajustes de Privacidad Recomendados

Desde la aplicación web o de escritorio de Element, ve a :gear: → **Más ajustes** para encontrar estas secciones:

#### Sesiones

Por defecto, al iniciar sesión en Element en un nuevo dispositivo, el nombre de sesión se rellenará automáticamente con el cliente de Matrix y la plataforma que utilizaste para iniciar sesión. Esta información puede ser visible para otros usuarios dependiendo del cliente Matrix que utilicen.

Para evitar revelar información sobre tu dispositivo personal a otros innecesariamente, considera vaciar el nombre de sesión; esto cambiará el nombre de sesión al ID de sesión alfanumérico generado aleatoriamente en su lugar.

#### Opciones

- [ ] Desmarca **Enviar acuses de recibo**
- [ ] Desmarca **Enviar notificaciones de tecleo**

Deberías desmarcar estas opciones para reducir la exposición de metadatos a otros usuarios cuando chateas en una sala pública.

#### Voz y Vídeo

- [ ] Desmarca **Permitir llamadas directas 1-a-1 (peer-to-peer)**
- [ ] Desmarca **Allow fallback call assist server (turn.matrix.org)**

Si decides utilizar Element para la comunicación uno a uno, te recomendamos que desmarques estas opciones para evitar que tu dirección IP quede expuesta a la otra parte.

#### Seguridad y Privacidad

##### Gestor de integraciones (scalar.vector.im)

Un gestor de integraciones de Matrix conecta Matrix a servicios de terceros como bots, puentes y otras mejoras. Element recopila información para prestar estos servicios a quienes utilizan un gestor de integraciones; puedes consultar su [Aviso de Privacidad](https://element.io/integration-manager-privacy-notice) detallado para conocer la información exacta que Element recopila y el modo en que utiliza dicha información.

Como usuario final en un servidor doméstico público, puedes considerar desmarcar la opción **Enable the integration manager**, que no afecta a la visibilidad de los bots u otros servicios de terceros. Como administrador de un servidor doméstico, considera si las partes adicionales con las que compartes tus datos merecen la funcionalidad adicional.

##### Sesiones

- [ ] (Opcional) Desmarca **Registrar el nombre del cliente, la versión y URL para reconocer de forma más fácil las sesiones en el gestor**

Desmarcar esta opción puede hacer más difícil discernir tus sesiones activas si has iniciado sesión en tu cuenta de Matrix en varios dispositivos.

#### Cifrado

- [x] (Opcional) Activa **In encrypted rooms, only send messages to verified users**

Con esta opción activada, los usuarios no verificados (es decir, aquellos que no hayan utilizado la función **Verificar Usuario**) y los dispositivos no verificados de usuarios verificados no recibirán tus mensajes en una sala con el cifrado activado. Esto puede limitar los mensajes que puedes ver y las personas con las que puedes interactuar.

## Criterios

**Por favor, ten en cuenta que no estamos afiliados a ninguno de los proyectos que recomendamos.** Además de [nuestros criterios estándar](about/criteria.md), hemos desarrollado un conjunto claro de requisitos que nos permiten ofrecer recomendaciones objetivas. Sugerimos que te familiarices con esta lista, antes de decidir utilizar un proyecto y realizar tu propia investigación para asegurarte de que es la elección ideal para ti.

- Debe ser software libre y de código abierto.
- Debe utilizar un protocolo federado para comunicarse con otras instancias del software de red social.
- No debe tener restricciones no técnicas sobre con quién puede estar federada.
- Debe poder utilizarse en un [navegador web] estándar (desktop-browsers.md).
- Debe hacer que los contenidos públicos sean accesibles a los visitantes sin cuenta.
- Debe permitirte limitar quién puede seguir tu perfil.
- Debe permitirte publicar contenidos visibles solo para tus seguidores.
- Debe ser compatible con los modernos estándares/características de seguridad de las aplicaciones web (incluida la [autenticación multifactor](multi-factor-authentication.md)).
