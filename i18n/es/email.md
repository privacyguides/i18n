---
meta_title: "Recomendaciones de Correo Electrónico Privado Cifrado - Privacy Guides"
title: "Servicios de Correo Electrónico"
icon: material/email
description: Estos proveedores de correo electrónico ofrecen un lugar estupendo para almacenar tus correos de forma segura, y muchos ofrecen encriptación OpenPGP inter operable con otros proveedores.
cover: email.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<!-- markdownlint-disable MD024 -->
Correo electrónico es prácticamente una necesidad para utilizar cualquier servicio en línea, sin embargo, no lo recomendamos para las conversaciones de persona a persona. En vez de utilizar el correo electrónico para comunicarte con otras personas, considera utilizar un servicio de mensajería instantánea que soporte el secreto hacia adelante.

[Servicios de Mensajería Instantánea Recomendados](real-time-communication.md ""){.md-button}

## Proveedores Recomendados

Para todo lo demás, recomendamos una variedad de proveedores de correo electrónico basados en modelos sostenibles, además de características de seguridad y privacidad integradas. Lee nuestra \[lista completa de criterios\](#criterios) para más información.

| Proveedor                   | OpenPGP / WKD                          | IMAP / SMTP                                                       | Cifrado de acceso cero                                    | Pagos anónimos                         |
| --------------------------- | -------------------------------------- | ----------------------------------------------------------------- | --------------------------------------------------------- | -------------------------------------- |
| [Proton Mail](#proton-mail) | :material-check:{ .pg-green }          | :material-information-outline:{ .pg-blue } Sólo en planes de pago | :material-check:{ .pg-green }                             | Efectivo                               |
| [Mailbox.org](#mailboxorg)  | :material-check:{ .pg-green }          | :material-check:{ .pg-green }                                     | :material-information-outline:{ .pg-blue } Sólo el correo | Efectivo                               |
| [Tuta](#tuta)               | :material-alert-outline:{ .pg-orange } | :material-alert-outline:{ .pg-orange }                            | :material-check:{ .pg-green }                             | Monero y efectivo a través de terceros |

Además de (o en lugar de) un proveedor de correo electrónico recomendado aquí, es posible que desees considerar un [servicio de alias de correo electrónico](email-aliasing.md) dedicado para proteger tu privacidad. Entre otras cosas, estos servicios pueden ayudarte a proteger tu bandeja de entrada real del spam, evitar que los profesionales del marketing correlacionen tus cuentas y cifrar todos los mensajes entrantes con PGP.

- [Más información :material-arrow-right-drop-circle:](email-aliasing.md)

## Servicios Compatibles con OpenPGP

Estos proveedores soportan de manera nativa el cifrado/descifrado de OpenPGP y el [estándar de Directorio de Clave Web](basics/email-security.md#what-is-the-web-key-directory-standard), permitiendo que los correos electrónicos cifrados de extremo a extremo sean independientes del proveedor. Por ejemplo, un usuario de Proton Mail podría enviar un mensaje E2EE a un usuario de Mailbox.org, o podrías recibir notificaciones encriptadas con OpenPGP desde servicios de Internet que lo soporten.

<div class="grid cards" markdown>

- ![Proton Mail logo](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![Mailbox.org logo](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

¡Al usar tecnologías de cifrado de extremo a extremo como OpenPGP, tu correo electrónico aún tendrá algunos metadatos que no son encriptados en el encabezado, por lo general incluyendo la línea del asunto! Lee más sobre los [metadatos de correo electrónico](basics/email-security.md#email-metadata-overview).

OpenPGP tampoco soporta Forward secrecy, lo que significa que si tu clave privada o la del destinatario es robada, todos los mensajes cifrados previamente con esta, estarán expuestos. [¿Cómo protejo mis claves privadas?](basics/email-security.md#how-do-i-protect-my-private-keys)

</div>

### Proton Mail

<div class="admonition recommendation" markdown>

![Logo Proton Mail](assets/img/email/protonmail.svg){ align=right }

**Proton Mail** es un servicio de correo electrónico con un enfoque en privacidad, encriptación, seguridad, y la facilidad de uso. Han estado en operación desde **2013**. Proton AG tiene su sede en Ginebra, Suiza. El plan gratuito de Proton Mail incluye 500MB de almacenamiento, que puede ser aumentado hasta 1GB sin costo.

[:octicons-home-16: Página principal](https://proton.me/mail){ .md-button .md-button--primary }
[:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Servicio Onion" }
[:octicons-eye-16:](https://proton.me/legal/privacy){ .card-link title="Política de privacidad" }
[:octicons-info-16:](https://proton.me/support/mail){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Código fuente" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/android-mail/releases)
- [:fontawesome-brands-windows: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: Web](https://mail.proton.me)

</details>

</div>

Las cuentas gratuitas tienen algunas limitaciones, como no poder buscar texto en el contenido, y no tener acceso a [Proton Mail Bridge](https://proton.me/mail/bridge), que es requerido para utilizar un [cliente recomendado de correo electrónico para escritorio](email-clients.md) (como Thunderbird). Cuentas pagas incluyen funciones como Proton Mail Bridge, almacenamiento adicional, y soporte para dominios personalizados. Una [carta de certificación](https://proton.me/blog/security-audit-all-proton-apps) fue proporcionada para las aplicaciones de Proton Mail el 9 de noviembre de 2021 por [Securitum](https://research.securitum.com).

Si tienes el plan de Proton Unlimited, Business, Family o Visionary, también recibes [SimpleLogin](email-aliasing.md#simplelogin) Premium sin costo adicional.

Proton Mail tiene informes de errores internos que **no** son compartidos con terceros. Esto se puede desactivar en la aplicación web: :gear: → **Todos los ajustes** → **Cuenta** → **Seguridad y privacidad** → **Privacidad y recolección de datos**.

#### :material-check:{ .pg-green } Dominios Personalizados y Alias

Suscriptores de pago de Proton Mail pueden utilizar su propio dominio con el servicio o una direcciones [catch-all](https://proton.me/support/catch-all). Proton Mail también soporta el [subdireccionamiento](https://proton.me/support/creating-aliases), que es útil para las personas que no quieren comprar un dominio.

#### :material-check:{ .pg-green } Métodos de pago privados

Proton Mail [acepta](https://proton.me/support/payment-options) dinero en efectivo por correo, además de tarjeta de crédito/débito estándar, [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), y pagos por PayPal.

#### :material-check:{ .pg-green } Seguridad de Cuenta

Proton Mail es compatible con TOTP [autenticación de dos factores](https://proton.me/support/two-factor-authentication-2fa) y [ llaves de seguridad de hardware](https://proton.me/support/2fa-security-key) que utilizan los estándares FIDO2 o U2F. El uso de una llave de seguridad de hardware requiere configurar primero la autenticación TOTP de dos factores.

#### :material-check:{ .pg-green } Seguridad de Datos

Proton Mail tiene [encriptacion de cero acceso](https://proton.me/blog/zero-access-encryption) en reposo para tus correos electrónicos y [calendarios](https://proton.me/news/protoncalendar-security-model). Datos asegurados con encriptación de cero-acceso son solamente accesibles por ti.

Cierta información almacenada en [Proton Contacts](https://proton.me/support/proton-contacts), como nombres y direcciones de correo electrónico, no está protegida con encriptación de cero-acceso. Los campos de contacto que admiten encriptación de cero-acceso, como los números de teléfono, se indican con un icono de candado.

#### :material-check:{ .pg-green } Encriptación de Correo Electrónico

Proton Mail ha [integrado la encriptación OpenPGP](https://proton.me/support/how-to-use-pgp) en su webmail. Los correos electrónicos a otras cuentas de Proton Mail se encriptan automáticamente, y la encriptación a direcciones que no sean de Proton Mail con una clave OpenPGP pueden ser habilitados fácilmente en la configuración de tu cuenta. Proton también soporta el descubrimiento automático de claves externas con [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). Esto significa que los correos electrónicos enviados a otros proveedores que utilicen WKD también se cifrarán automáticamente con OpenPGP, sin necesidad de intercambiar manualmente claves PGP públicas con tus contactos. Estas también te permiten [cifrar los mensajes enviados a cuentas no pertenecientes a Proton](https://proton.me/support/password-protected-emails), sin la necesidad de que el receptor utilice OpenPGP o se registre en Proton Mail.

Proton Mail también publica las direcciones públicas de las cuentas a través de HTTP desde su WKD. Esto permite las personas quienes no utilizan Proton Mail a encontrar fácilmente las claves OpenPGP de las cuentas de Proton Mail, para E2EE entre proveedores. Esto solo aplica para las direcciones de correo electrónico que terminen en uno de los dominios de Proton, como @proton.me. Si utilizas un dominio personalizado, debes [configurar WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) por separado.

#### :material-information-outline:{ .pg-blue } Cancelación de Cuenta

Si tienes una cuenta de pago y tu factura [no esta paga](https://proton.me/support/delinquency) después de 14 días, no podrá acceder a tus datos. Transcurridos 30 días, tu cuenta se convertirá en morosa y no recibirás correo entrante. Seguirás siendo facturando durante este periodo. Proton [elimina las cuentas gratuitas sin actividad](https://proton.me/support/inactive-accounts) luego de un año. **No** puedes reutilizar la dirección de correo de una cuenta desactivada.

#### :material-information-outline:{ .pg-blue }: Funcionalidad Adicional

El plan [Unlimited](https://proton.me/support/proton-plans#proton-unlimited) de Proton Mail también activa el acceso a otros servicios de Proton, además de proporcionar múltiples dominios personalizados, alias hide-my-email ilimitados y 500GB de almacenamiento.

Proton Mail no ofrece la función de legado digital.

### Mailbox.org

<div class="admonition recommendation" markdown>

![Logo de Mailbox.org](assets/img/email/mailboxorg.svg){ align=right }

**Mailbox.org** es un servicio de correo electrónico centrado en ser seguro, sin publicidad, y alimentado de forma privada con energía 100% ecológica. Han estado en operación desde 2014. Mailbox.org tiene su sede en Berlín, Alemania. Las cuentas inician con hasta 2GB de almacenamiento, que pueden ser ampliados cuando sea necesario.

[:octicons-home-16: Página Principal](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Politica de Privacidad" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title=Documentación}

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:octicons-browser-16: Web](https://login.mailbox.org)

</details>

</div>

#### :material-check:{ .pg-green } Dominios Personalizados y Alias

Mailbox.org te permite utilizar tu propio dominio y admite direcciones [catch-all](https://kb.mailbox.org/en/private/custom-domains/how-to-set-up-a-catch-all-alias-with-a-custom-domain-name). Mailbox.org también soporta el [subdireccionamiento](https://kb.mailbox.org/en/private/account-article/what-is-an-alias-and-how-do-i-use-it), lo que resulta útil si no desea adquirir un dominio.

#### :material-check:{ .pg-green } Métodos Privados de Pago

Mailbox.org no acepta criptomonedas debido a que su procesador de pagos BitPay suspendió sus operaciones en Alemania. Sin embargo, aceptan los pagos por correo, pagos a una cuenta bancaria, transferencias bancarias, tarjetas de crédito, PayPal y algunos procesadores de pago alemanes: paydirekt y Sofortüberweisung.

#### :material-check:{ .pg-green } Seguridad de Cuenta

Mailbox.org solo admite la [autenticación de dos factores](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa) para su correo web. Puedes utilizar TOTP o una [YubiKey](https://en.wikipedia.org/wiki/YubiKey) a través de [YubiCloud](https://yubico.com/products/services-software/yubicloud). Estándares web como [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn) aún no son soportados.

#### :material-information-outline:{ .pg-blue } Seguridad de Datos

Mailbox.org permite encriptación del correo entrante usando su [buzón encriptado](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox). Nuevos mensajes que recibas se encriptaran inmediatamente con tu clave pública.

Sin embargo, [Open-Exchange](https://en.wikipedia.org/wiki/Open-Xchange), la plataforma de software utilizada por Mailbox.org, [no admite](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book) el cifrado de su libreta de direcciones y calendario. Una [opción independiente](calendar.md) puede ser más apropiada para esa información.

#### :material-check:{ .pg-green } Encriptación de Correo Electrónico

Mailbox.org tiene [encriptación integrada](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard) en su correo web, lo que simplifica el envío de mensajes a personas con claves públicas OpenPGP. También permiten [a destinatarios remotos descifrar un correo electrónico](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp) en los servidores de Mailbox.org. Esta característica es útil cuando el destinatario remoto no tiene OpenPGP y no puede descifrar una copia del correo electrónico en su propio buzón de correo.

Mailbox.org también admite el descubrimiento de claves públicas a través de HTTP desde su [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). Esto permite que personas afuera de Mailbox.org encuentren fácilmente las claves OpenPGP de las cuentas de Mailbox.org, para E2EE entre proveedores. Esto solo aplica para las direcciones de correo electrónico que terminan en un dominio de Mailbox.org, como @mailbox.org. Si utilizas un dominio personalizado, debes [configurar WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) por separado.

#### :material-information-outline:{ .pg-blue } Cancelación de Cuenta

Tu cuenta se convertirá en una cuenta de usuario restringida cuando tu contrato finalice. Se eliminará luego de [30 días](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } Funcionalidad Adicional

Puedes acceder a tu cuenta de Mailbox.org a través de IMAP/SMTP utilizando su [servicio.onion](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org). Sin embargo, no se puede acceder a su interfaz de correo web a través de su servicio .onion y es posible que se produzcan errores de certificado TLS.

Todas las cuentas incluyen almacenamiento limitado en la nube que [puede cifrarse](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive). Mailbox.org también ofrece el alias [@secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely), que impone el cifrado TLS en la conexión entre servidores de correo; de lo contrario, el mensaje no se enviará en absoluto. Mailbox.org también admite [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) además de protocolos de acceso estándar como IMAP y POP3.

Mailbox.org tiene una función de legado digital para todos los planes. Puedes elegir si deseas que alguno de tus datos se transmita a los herederos, siempre que lo soliciten y aporten tu testamento. Alternativamente, puedes designar a una persona por su nombre y dirección.

## Más Proveedores

Estos proveedores almacenan tus correos electrónicos con cifrado de cero-conocimiento, lo que los convierte en excelentes opciones para mantener seguros tus correos electrónicos almacenados. Sin embargo, no admiten normas de cifrado interoperables para las comunicaciones E2EE entre distintos proveedores.

<div class="grid cards" markdown>

- ![Logo de Tuta](assets/img/email/tuta.svg#only-light){ .twemoji loading=lazy }![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ .twemoji loading=lazy } [Tuta](email.md#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Logo de Tuta](assets/img/email/tuta.svg#only-light){ align=right }
![Logo de Tuta](assets/img/email/tuta-dark.svg#only-dark){ align=right }

**Tuta** es un servicio de correo electrónico enfocado en la seguridad y la privacidad, a través del uso del cifrado. Tuta lleva en funcionamiento desde **2011** y tiene su sede en Hanóver, Alemania. Las cuentas gratuitas inician con 1GB de almacenamiento.

[:octicons-home-16: Página principal](https://tuta.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tuta.com/privacy){ .card-link title="Política de privacidad" }
[:octicons-info-16:](https://tuta.com/support){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="Código fuente" }
[:octicons-heart-16:](https://tuta.com/community){ .card-link title=Contribuir }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
- [:simple-appstore: App Store](https://apps.apple.com/app/id922429609)
- [:simple-github: GitHub](https://github.com/tutao/tutanota/releases)
- [:fontawesome-brands-windows: Windows](https://tuta.com/#download)
- [:simple-apple: macOS](https://tuta.com/#download)
- [:simple-linux: Linux](https://tuta.com/#download)
- [:octicons-browser-16: Web](https://app.tuta.com)

</details>

</div>

Tuta no es compatible con el [protocolo IMAP](https://tuta.com/support#imap) o el uso de [clientes de terceros](email-clients.md), y tampoco pdrás agregar [cuentas externas de correo electrónico](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) en la aplicación de Tuta. La [importación de correo electrónico](https://github.com/tutao/tutanota/issues/630) tampoco es soportada actualmente, pero esto [puede cambiar pronto](https://tuta.com/blog/kickoff-import). Los correos electrónicos pueden ser exportados [individual o grupalmente](https://tuta.com/support#generalMail) por carpeta, lo que puede ser poco conveniente si tienes varias carpetas.

#### :material-check:{ .pg-green } Dominios Personalizados y Alias

Las cuentas de pago de Tuta cuentan con 15 o 30 alias dependiendo del plan y alias ilimitados en [dominios personalizados](https://tuta.com/support#custom-domain). Tuta no permite el [subdireccionamiento (direcciones con un más)](https://tuta.com/support#plus), pero puedes usar [catch-all](https://tuta.com/support#settings-global) con un dominio personalizado.

#### :material-information-outline:{ .pg-blue } Métodos de pago privados

Tuta únicamente acepta el pago con tarjetas de crédito y PayPal. Sin embargo, se pueden utilizar [criptomonedas](cryptocurrency.md) para comprar tarjetas de regalo gracias a la [asociación](https://tuta.com/support/#cryptocurrency) con Proxystore.

#### :material-check:{ .pg-green } Seguridad de Cuenta

Tuta soporta la [autenticación de dos factores](https://tuta.com/support#2fa) ya sea con TOTP o U2F.

#### :material-check:{ .pg-green } Seguridad de los datos

Tuta tiene [cifrado de acceso cero en reposo](https://tuta.com/support#what-encrypted) para tus correos, [contactos de la libreta de direcciones](https://tuta.com/support#encrypted-address-book) y [calendarios](https://tuta.com/support#calendar). Esto significa que sólo tú puedes leer los mensajes y otros datos almacenados en tu cuenta.

#### :material-information-outline:{ .pg-blue } Cifrado de correo electrónico

Tuta [no utiliza OpenPGP](https://tuta.com/support/#pgp). Las cuentas de Tuta solo pueden recibir correos electrónicos cifrados de cuentas de correo electrónico que no sean de Tuta cuando se envían a través de un [buzón temporal de Tuta](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } Cancelación de la cuenta

Tuta [elimina las cuentas gratuitas inactivas](https://tuta.com/support#inactive-accounts) luego de seis meses. Puedes reutilizar una cuenta gratuita desactivada si pagas.

#### :material-information-outline:{ .pg-blue } Funciones adicionales

Tuta ofrece una versión empresarial para [organizaciones sin fines de lucro](https://tuta.com/blog/secure-email-for-non-profit) de manera gratuita o con un importante descuento.

Tuta no ofrece una función de legado digital.

## Correo de auto-alojamiento

Los administradores de sistemas avanzados pueden plantearse crear su propio servidor de correo electrónico. Los servidores de correo requieren atención y un mantenimiento continuo para mantener la seguridad y la fiabilidad de la entrega del correo.

### Soluciones de software combinadas

<div class="admonition recommendation" markdown>

![Logo de Mailcow](assets/img/email/mailcow.svg){ align=right }

**Mailcow** es un servidor de correo más avanzado perfecto para aquellos con un poco más de experiencia en Linux. Tiene todo lo que necesitas en un contenedor Docker: Un servidor de correo con soporte DKIM, antivirus, monitorización de spam, webmail, ActiveSync con SOGo y administración basada en web con soporte 2FA.

[:octicons-home-16: Página Principal](https://mailcow.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.mailcow.email){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://servercow.de/mailcow?lang=en#sal){ .card-link title=Contribuir }

</div>

<div class="admonition recommendation" markdown>

![Logo de Mail-in-a-Box](assets/img/email/mail-in-a-box.svg){ align=right }

**Mail-in-a-Box** es un script de configuración automatizada para desplegar un servidor de correo en Ubuntu. Su objetivo es facilitar a los usuarios la instalación de su propio servidor de correo.

[:octicons-home-16: Página Principal](https://mailinabox.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="Código Fuente" }

</div>

Para un enfoque más manual, hemos seleccionado estos dos artículos:

- [Configuración de un servidor de correo con OpenSMTPD, Dovecot y Rspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd) (2019)
- [Cómo Ejecutar Tu Propio Servidor De Correo](https://c0ffee.net/blog/mail-server-guide) (Agosto de 2017)

## Criterios

**Por favor, ten en cuenta que no estamos afiliados con ninguno de los proveedores que recomendamos.** Además de [nuestros criterios estándar](about/criteria.md), hemos desarrollado un claro conjunto de requisitos para cualquier proveedor de correo electrónico que desee ser recomendado, incluyendo la implementación de las mejores prácticas de la industria, tecnología moderna y más. Sugerimos que te familiarices con esta lista antes de elegir un proveedor de correo electrónico, y que realices tu propia investigación para asegurarte de que el proveedor de correo electrónico que elijas sea la opción adecuada para ti.

### Tecnología

Consideramos que estas características son importantes para ofrecer un servicio seguro y óptimo. Debes considerar si el proveedor tiene las características que necesita.

**Mínimo para calificar:**

- Cifra los datos de las cuentas de correo electrónico en reposo con cifrado de acceso cero.
- Capacidad de exportación como [Mbox](https://en.wikipedia.org/wiki/Mbox) o .eml individual con el estándar [RFC5322](https://datatracker.ietf.org/doc/rfc5322).
- Permitir a los usuarios utilizar su propio [nombre de dominio](https://en.wikipedia.org/wiki/Domain_name). Los nombres de dominio personalizados son importantes para los usuarios porque les permiten mantener su agencia del servicio, en caso de que éste se estropee o sea adquirido por otra empresa que no dé prioridad a la privacidad.
- Operaciones en infraestructura propia, es decir, no construidas sobre proveedores de servicios de correo electrónico de terceros.

**Mejor caso:**

- Cifra todos los datos de la cuenta (contactos, calendarios, etc.) en reposo con cifrado de acceso cero.
- Cifrado integrado de correo web E2EE/PGP proporcionado como una conveniencia.
- Compatibilidad con [WKD](https://wiki.gnupg.org/WKD) para permitir un mejor descubrimiento de claves OpenPGP públicas a través de HTTP. Los usuarios de GnuPG pueden obtener una clave escribiendo: `gpg --locate-key usuario_ejemplo@ejemplo.com`
- Soporte para un buzón temporal para usuarios externos. Esto es útil cuando quieres enviar un correo electrónico encriptado, sin enviar una copia real a tu destinatario. Estos correos electrónicos suelen tener una vida útil limitada y luego se eliminan automáticamente. Tampoco requieren que el destinatario configure ninguna criptografía como OpenPGP.
- Disponibilidad de los servicios del proveedor de correo electrónico a través de un [ servicio onion](https://en.wikipedia.org/wiki/.onion).
- Soporte de [subdireccionamiento](https://en.wikipedia.org/wiki/Email_address#Sub-addressing).
- Funcionalidad Catch-all o alias para aquellos que poseen sus propios dominios.
- Utilización de protocolos estándar de acceso al correo electrónico como IMAP, SMTP o [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Los protocolos de acceso estándar garantizan que los clientes puedan descargar fácilmente todo su correo electrónico en caso de que quieran cambiar de proveedor.

### Privacidad

Preferimos que nuestros proveedores recomendados recojan la menor cantidad de datos posible.

**Mínimo para calificar:**

- Protege la dirección IP del remitente. La filtra para que no aparezca en el campo de cabecera `Recibido`.
- No requiere información personal identificable (PII) aparte de un nombre de usuario y una contraseña.
- Política de privacidad que cumple los requisitos definidos por el RGPD.

**Mejor Caso:**

- Acepta [opciones de pago anónimas](advanced/payments.md) ([criptomonedas](cryptocurrency.md), efectivo, tarjetas regalo, etc.)
- Alojado en una jurisdicción con leyes de protección de la privacidad del correo electrónico estrictas.

### Seguridad

Los servidores de correo electrónico manejan muchos datos sensibles. Esperamos que los proveedores adopten las mejores prácticas de la industria para proteger a sus miembros.

**Mínimo para calificar:**

- Protección del correo web con 2FA, como TOTP.
- Cifrado de acceso cero, basado en el cifrado en reposo. El proveedor no disponga de las claves de descifrado de los datos que posee. Esto evita que un empleado deshonesto filtre datos a los que tiene acceso o que un adversario remoto divulgue datos que ha robado al obtener acceso no autorizado al servidor.
- Compatible con [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions).
- Sin errores o vulnerabilidades TLS al ser perfilado por herramientas como [Hardenize](https://hardenize.com), [testssl.sh](https://testssl.sh) o [Qualys SSL Labs](https://ssllabs.com/ssltest); esto incluye errores relacionados con certificados y parámetros DH débiles, como los que llevaron a [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- Una preferencia de suite de servidor (opcional en TLSv1.3) para suites de cifrado potentes que soporten forward secrecy y encriptación autenticada.
- Una política válida [MTA-STS](https://tools.ietf.org/html/rfc8461) y [TLS-RPT](https://tools.ietf.org/html/rfc8460).
- Registros válidos de [DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities).
- Registros válidos [SPF](https://en.wikipedia.org/wiki/Sender_Policy_Framework) y [DKIM](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail).
- Tenga un registro y una política adecuados de [DMARC](https://en.wikipedia.org/wiki/DMARC) o use [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) para la autenticación. Si se utiliza la autenticación DMARC, la política debe establecerse en `rechazar` o `cuarentena`.
- Una preferencia de suite de servidor de TLS 1.2 o posterior y un plan para [RFC8996](https://datatracker.ietf.org/doc/rfc8996).
- [Envío de SMTPS](https://en.wikipedia.org/wiki/SMTPS), suponiendo que se utiliza SMTP.
- Estándares de seguridad del sitio web tales como:
    - [Seguridad de transporte estricta HTTP](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - [Integridad de subrecurso](https://en.wikipedia.org/wiki/Subresource_Integrity) si se cargan cosas desde dominios externos.
- Debe admitir la visualización de [Encabezados de mensaje](https://en.wikipedia.org/wiki/Email#Message_header), ya que es una característica forense crucial para determinar si un correo electrónico es un intento de phishing.

**Mejor caso:**

- Soporte para autenticación de hardware, ej. U2F y [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn). U2F y WebAuthn son más seguros ya que utilizan una clave privada almacenada en un dispositivo de hardware del lado del cliente para autenticar a las personas, a diferencia de un secreto compartido que se almacena en el servidor web y en el lado del cliente cuando se utiliza TOTP. Además, U2F y WebAuthn son más resistentes al phishing ya que su respuesta de autenticación se basa en el [nombre de dominio](https://en.wikipedia.org/wiki/Domain_name) autenticado.
- [Registro de recursos de autorización de autoridad de certificación (CAA) de DNS](https://tools.ietf.org/html/rfc6844) además del soporte de DANE.
- Implementación de la [cadena recibida autenticada (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), esto es útil para las personas que publican en listas de correo [RFC8617](https://tools.ietf.org/html/rfc8617).
- Programas de recompensa de errores y/o un proceso coordinado de divulgación de vulnerabilidades.
- Estándares de seguridad del sitio web tales como:
    - [Política de seguridad de contenido (CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### Confianza

No confiarías tus finanzas a alguien con una identidad falsa, así que ¿por qué confiarle tus datos de Internet? Exigimos a nuestros proveedores recomendados que hagan pública su propiedad o liderazgo. También nos gustaría ver informes de transparencia frecuentes, especialmente en lo que se refiere a cómo se gestionan las solicitudes del gobierno.

**Mínimo para Calificar:**

- Liderazgo o propiedad de cara al público.

**Mejor Caso:**

- Liderazgo de cara al público.
- Informes de transparencia frecuentes.

### Marketing

Con los proveedores de correo electrónico que recomendamos nos gusta ver el marketing responsable.

**Mejor caso:**

- Debe autoalojar las analíticas (no Google Analytics, Adobe Analytics, etc.). El sitio del proveedor también debe cumplir con [DNT (Do Not Track, sin rastreo)](https://en.wikipedia.org/wiki/Do_Not_Track) para las personas que deseen darse de baja.

No debe tener ningún tipo de marketing que sea irresponsable:

- Reclamaciones de "cifrado irrompible" El cifrado debe usarse con la intención de que no sea secreto en el futuro cuando exista la tecnología para descifrarlo.
- Haciendo garantías de proteger el anonimato al 100%. Cuando alguien afirma que algo es 100% significa que no hay certeza de fracaso. Sabemos que la gente puede desanonimizarse fácilmente de varias maneras, por ejemplo:

    - Reutilizar información personal (como cuentas de correo electrónico, seudónimos únicos, etc.) que ellos accesaron sin programas de anonimato (Tor, VPN, etc.)
    - [Browser fingerprinting](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**Mejor Caso:**

- Documentación clara y fácil de leer. Esto incluye cosas como configurar 2FA, clientes de correo electrónico, OpenPGP, etc.

### Funcionalidad Adicional

Aunque no son exactamente requisitos, hay algunos otros factores de conveniencia o privacidad que hemos analizado para determinar qué proveedores recomendar.
