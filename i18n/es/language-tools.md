---
title: "Herramientas Lingüísticas"
icon: material/alphabetical-variant
description: Estas herramientas lingüísticas no envían el texto introducido a un servidor y pueden utilizarse sin conexión y de forma autoalojada.
cover: language-tools.webp
---

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-server-network: Proveedores de Servicios](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }
- [:material-account-cash: Capitalismo de Vigilancia](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

El texto introducido en los correctores gramaticales, ortográficos y de estilo, así como en los servicios de traducción, puede contener información sensible que puede ser almacenada en sus servidores por tiempo indefinido y vendida a terceros. Las herramientas lingüísticas enumeradas en esta página no almacenan el texto enviado en un servidor y pueden autoalojarse y utilizarse sin conexión para tener el máximo control de tus datos.

## Herramientas de Traducción

### LibreTranslate

<div class="admonition recommendation" markdown>

![LibreTranslate logo](assets/img/language-tools/libretranslate.png){ align=right }

**LibreTranslate** es una interfaz web de traducción automática y un servidor API gratuitos y de código abierto. Utiliza modelos [Argos Translate](https://github.com/argosopentech/argos-translate) en el backend para las traducciones.

[:octicons-home-16: Página Principal](https://libretranslate.com){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/LibreTranslate/LibreTranslate#mirrors){ .card-link title="Instancias Públicas" }
[:octicons-code-16:](https://github.com/LibreTranslate/LibreTranslate){ .card-link title="Código Fuente" }

</div>

Puedes usar LibreTranslate a través de varias instancias públicas, algunas de las cuales ofrecen un servicio onion [Tor](tor.md) o eepsite [I2P](alternative-networks.md#i2p-the-invisible-internet-project). También puedes alojar el software tú mismo para tener el máximo control sobre el texto enviado para su traducción.

Utilizamos una instancia autoalojada de LibreTranslate para traducir automáticamente las publicaciones de nuestro [foro](https://discuss.privacyguides.net) a varios idiomas.

We use the VSCode extension in our GitHub repository configuration to find any grammar and spelling errors on our website and in our articles.

## Criterios

**Por favor, ten en cuenta que no estamos afiliados a ninguno de los proyectos que recomendamos.** Además de [nuestros criterios estándar](about/criteria.md), hemos desarrollado un conjunto claro de requisitos que nos permiten ofrecer recomendaciones objetivas. Sugerimos que te familiarices con esta lista, antes de decidir utilizar un proyecto y realizar tu propia investigación para asegurarte de que es la elección ideal para ti.

- Debe ser de código abierto.
- Must run completely offline.
