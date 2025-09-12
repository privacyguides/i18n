---
title: Servidores de Correo Electrónico
meta_title: "Autoalojamiento de Correo Electrónico - Privacy Guides"
icon: material/email
description: Para nuestros lectores más técnicos, el autoalojamiento de tu propio correo electrónico puede proporcionar garantías adicionales de privacidad al tener el máximo control sobre tus datos.
cover: email.webp
---

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-server-network: Proveedores de Servicios](../basics/common-threats.md#privacy-from-service-providers){ .pg-teal }

Los administradores de sistemas avanzados pueden considerar configurar su propio servidor de **correo electrónico**. Los servidores de correo requieren atención y un mantenimiento continuo para mantener la seguridad y la fiabilidad de la entrega del correo. Además de las soluciones «todo en uno» que aparecen a continuación, hemos seleccionado algunos artículos que cubren un enfoque más manual:

- [Configurando un servidor de correo con OpenSMTPD, Dovecot y Rspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd) (2019)
- [Cómo Ejecutar Tu Propio Servidor de Correo](https://www.c0ffee.net/blog/mail-server-guide) (Agosto 2017)

## Stalwart

<div class="admonition recommendation" markdown>

![Stalwart logo](../assets/img/self-hosting/stalwart.svg){ align=right }

**Stalwart** es un nuevo servidor de correo escrito en Rust que soporta JMAP además de los estándares IMAP, POP3 y SMTP. Dispone de una amplia variedad de opciones de configuración, pero también de una configuración predeterminada muy razonable tanto en términos de seguridad como de funciones, lo que facilita su uso inmediato. Tiene administración basada en web con soporte TOTP 2FA y te permite introducir tu clave PGP pública para encriptar **todos** los mensajes entrantes.

[:octicons-home-16: Página Principal](https://stalw.art){ .md-button .md-button--primary }
[:octicons-info-16:](https://stalw.art/docs/get-started){ .card-link title="Documentación" }
[:octicons-code-16:](https://github.com/stalwartlabs){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://github.com/sponsors/stalwartlabs){ .card-link title="Contribuir" }

</div>

La [implementación de PGP] de Stalwart(https://stalw.art/docs/encryption/overview) es única entre nuestras recomendaciones de autoalojamiento y te permite operar tu propio servidor de correo con almacenamiento de mensajes de conocimiento cero. Si además configuras Web Key Directory (WKD) en tu dominio, y si utilizas un cliente de correo electrónico que soporte PGP y WKD para el correo saliente (como Thunderbird), entonces esta es la forma más sencilla de conseguir compatibilidad E2EE autoalojada con todos los usuarios de [Proton Mail](../email.md#proton-mail).

Stalwart **no** tiene un correo web integrado, así que tendrás que usarlo con un [cliente de correo electrónico dedicado](../email-clients.md) o encontrar un correo web de código abierto para autoalojarlo, como la aplicación Mail de Nextcloud.

Utilizamos Stalwart para nuestro propio correo electrónico interno en _Privacy Guides_.

## Mailcow

<div class="admonition recommendation" markdown>

![Mailcow logo](../assets/img/self-hosting/mailcow.svg){ align=right }

**Mailcow** es un servidor de correo avanzado perfecto para aquellos con experiencia en Linux. Tiene todo lo que necesitas en un contenedor Docker: un servidor de correo con soporte DKIM, antivirus y monitorización de spam, correo web y ActiveSync con SOGo, y administración basada en web con soporte 2FA.

[:octicons-home-16: Página Principal](https://mailcow.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.mailcow.email){ .card-link title="Documentación" }
[:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://servercow.de/mailcow?lang=en#sal){ .card-link title="Contribuir" }

</div>

## Mail-in-a-Box

<div class="admonition recommendation" markdown>

![Mail-in-a-Box logo](../assets/img/self-hosting/mail-in-a-box.svg){ align=right }

**Mail-in-a-Box** es un script de configuración automatizado para desplegar un servidor de correo en Ubuntu. Su objetivo es facilitar a los usuarios la instalación de su propio servidor de correo.

[:octicons-home-16: Página Principal](https://mailinabox.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title="Documentación" }
[:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="Código Fuente" }

</div>
