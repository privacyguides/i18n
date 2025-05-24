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

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-server-network: Proveedores de servicios](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

El correo electrónico es prácticamente una necesidad para utilizar cualquier servicio en línea, sin embargo, no lo recomendamos para las conversaciones de persona a persona. En vez de utilizar el correo electrónico para comunicarte con otras personas, considera utilizar un servicio de mensajería instantánea que soporte el secreto hacia adelante.

[Servicios de Mensajería Instantánea Recomendados](real-time-communication.md ""){.md-button}

## Proveedores Recomendados

Para todo lo demás, recomendamos una variedad de proveedores de correo electrónico basados en modelos sostenibles, además de características de seguridad y privacidad integradas. Lee nuestra \[lista completa de criterios\](#criterios) para más información.

| Proveedor                   | OpenPGP / WKD                          | IMAP / SMTP                                                       | Zero-Access Encryption                                    | Anonymous Payment Methods             |
| --------------------------- | -------------------------------------- | ----------------------------------------------------------------- | --------------------------------------------------------- | ------------------------------------- |
| [Proton Mail](#proton-mail) | :material-check:{ .pg-green }          | :material-information-outline:{ .pg-blue } Sólo en planes de pago | :material-check:{ .pg-green }                             | Efectivo                              |
| [Mailbox.org](#mailboxorg)  | :material-check:{ .pg-green }          | :material-check:{ .pg-green }                                     | :material-information-outline:{ .pg-blue } Sólo el correo | Efectivo                              |
| [Tuta](#tuta)               | :material-alert-outline:{ .pg-orange } | :material-alert-outline:{ .pg-orange }                            | :material-check:{ .pg-green }                             | Monero <br>Cash via third party |

In addition to (or instead of) an email provider recommended here, you may wish to consider a dedicated [email aliasing service](email-aliasing.md#recommended-providers) to protect your privacy. Entre otras cosas, estos servicios pueden ayudarte a proteger tu bandeja de entrada real del spam, evitar que los profesionales del marketing correlacionen tus cuentas y cifrar todos los mensajes entrantes con PGP.

- [Más información :material-arrow-right-drop-circle:](email-aliasing.md)

## Servicios Compatibles con OpenPGP

These providers natively support OpenPGP encryption/decryption and the [Web Key Directory (WKD) standard](basics/email-security.md#what-is-the-web-key-directory-standard), allowing for provider-agnostic end-to-end encrypted emails. Por ejemplo, un usuario de Proton Mail podría enviar un mensaje E2EE a un usuario de Mailbox.org, o podrías recibir notificaciones encriptadas con OpenPGP desde servicios de Internet que lo soporten.

<div class="grid cards" markdown>

- ![Proton Mail logo](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![Mailbox.org logo](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

¡Al usar tecnologías de cifrado de extremo a extremo como OpenPGP, tu correo electrónico aún tendrá algunos metadatos que no son encriptados en el encabezado, por lo general incluyendo la línea del asunto! Lee más sobre los [metadatos de correo electrónico](basics/email-security.md#email-metadata-overview).

OpenPGP also does not support forward secrecy, which means if the private key of either you or the message recipient is ever stolen, all previous messages encrypted with it will be exposed.

- [How do I protect my private keys?](basics/email-security.md#how-do-i-protect-my-private-keys)

</div>

### Proton Mail

<div class="admonition recommendation" markdown>

![Logo Proton Mail](assets/img/email/protonmail.svg){ align=right }

**Proton Mail** es un servicio de correo electrónico con un enfoque en privacidad, encriptación, seguridad, y la facilidad de uso. Ha estado en operación desde 2013. Proton AG is based in Geneva, Switzerland.

The Proton Free plan comes with 500 MB of Mail storage, which you can increase up to 1 GB for free.

[:octicons-home-16: Página Principal](https://proton.me/mail){ .md-button .md-button--primary }
[:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Servicio Onion" }
[:octicons-eye-16:](https://proton.me/mail/privacy-policy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://proton.me/support/mail){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/android-mail/releases)
- [:fontawesome-brands-windows: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: Web](https://mail.proton.me)

</details>

</div>

Free accounts have some limitations, such as not being able to search body text and not having access to [Proton Mail Bridge](https://proton.me/mail/bridge), which is required to use a [recommended desktop email client](email-clients.md) (e.g., Thunderbird). Cuentas pagas incluyen funciones como Proton Mail Bridge, almacenamiento adicional, y soporte para dominios personalizados. Si tienes el plan Proton Unlimited o cualquier plan Proton multiusuario, también obtienes [SimpleLogin](email-aliasing.md#simplelogin) Premium gratis.

Una [carta de certificación](https://proton.me/blog/security-audit-all-proton-apps) fue proporcionada para las aplicaciones de Proton Mail el 9 de noviembre de 2021 por [Securitum](https://research.securitum.com).

Proton Mail tiene informes de errores internos que **no** son compartidos con terceros. Esto se puede desactivar en la aplicación web: :gear: → **Todos los ajustes** → **Cuenta** → **Seguridad y privacidad** → **Privacidad y recolección de datos**.

#### :material-check:{ .pg-green } Dominios Personalizados y Alias

Suscriptores de pago de Proton Mail pueden utilizar su propio dominio con el servicio o una direcciones [catch-all](https://proton.me/support/catch-all). Proton Mail también soporta el [subdireccionamiento](https://proton.me/support/creating-aliases), que es útil para las personas que no quieren comprar un dominio.

#### :material-check:{ .pg-green } Métodos de pago privados

Proton Mail [accepts](https://proton.me/support/payment-options) **cash** by mail in addition to standard credit/debit card, [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), and PayPal payments.

#### :material-check:{ .pg-green } Seguridad de Cuenta

Proton Mail supports TOTP [two-factor authentication](https://proton.me/support/two-factor-authentication-2fa) and [hardware security keys](https://proton.me/support/2fa-security-key) using FIDO2 or U2F standards. The use of a hardware security key requires setting up TOTP two-factor authentication first.

#### :material-check:{ .pg-green } Seguridad de Datos

Proton Mail tiene [encriptacion de cero acceso](https://proton.me/blog/zero-access-encryption) en reposo para tus correos electrónicos y [calendarios](https://proton.me/news/protoncalendar-security-model). Datos asegurados con encriptación de cero-acceso son solamente accesibles por ti.

Cierta información almacenada en [Proton Contacts](https://proton.me/support/proton-contacts), como nombres y direcciones de correo electrónico, no está protegida con encriptación de cero-acceso. Los campos de contacto que admiten encriptación de cero-acceso, como los números de teléfono, se indican con un icono de candado.

#### :material-check:{ .pg-green } Encriptación de Correo Electrónico

Proton Mail ha [integrado la encriptación OpenPGP](https://proton.me/support/how-to-use-pgp) en su webmail. Los correos electrónicos a otras cuentas de Proton Mail se encriptan automáticamente, y la encriptación a direcciones que no sean de Proton Mail con una clave OpenPGP pueden ser habilitados fácilmente en la configuración de tu cuenta. Proton also supports automatic external key discovery with WKD. Esto significa que los correos electrónicos enviados a otros proveedores que utilicen WKD también se cifrarán automáticamente con OpenPGP, sin necesidad de intercambiar manualmente claves PGP públicas con tus contactos. Estas también te permiten [cifrar los mensajes enviados a cuentas no pertenecientes a Proton](https://proton.me/support/password-protected-emails), sin la necesidad de que el receptor utilice OpenPGP o se registre en Proton Mail.

Proton Mail también publica las direcciones públicas de las cuentas a través de HTTP desde su WKD. This allows people who don't use Proton Mail to find the OpenPGP keys of Proton Mail accounts easily for cross-provider E2EE. This only applies to email addresses ending in one of Proton's own domains, like `@proton.me`. If you use a custom domain, you must [configure WKD](basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } Cancelación de Cuenta

Si tienes una cuenta de pago y tu factura [no esta paga](https://proton.me/support/delinquency) después de 14 días, no podrá acceder a tus datos. Transcurridos 30 días, tu cuenta se convertirá en morosa y no recibirás correo entrante. Seguirás siendo facturando durante este periodo. Proton [elimina las cuentas gratuitas sin actividad](https://proton.me/support/inactive-accounts) luego de un año. **No** puedes reutilizar la dirección de correo de una cuenta desactivada.

#### :material-information-outline:{ .pg-blue }: Funcionalidad Adicional

Proton Mail's [Unlimited](https://proton.me/support/proton-plans#proton-unlimited) plan also enables access to other Proton services in addition to providing multiple custom domains, unlimited hide-my-email aliases, and 500 GB of storage.

### Mailbox.org

<div class="admonition recommendation" markdown>

![Mailbox.org logo](assets/img/email/mailboxorg.svg){ align=right }

**Mailbox.org** is an email service with a focus on being secure, ad-free, and powered by 100% eco-friendly energy. Han estado en operación desde 2014. Mailbox.org tiene su sede en Berlín, Alemania.

Accounts start with up to 2 GB storage, which can be upgraded as needed.

[:octicons-home-16: Página Principal](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title="Documentación" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:octicons-browser-16: Web](https://login.mailbox.org)

</details>

</div>

#### :material-check:{ .pg-green } Dominios Personalizados y Alias

Mailbox.org te permite utilizar tu propio dominio y admite direcciones [catch-all](https://kb.mailbox.org/en/private/custom-domains/how-to-set-up-a-catch-all-alias-with-a-custom-domain-name). Mailbox.org también soporta el [subdireccionamiento](https://kb.mailbox.org/en/private/account-article/what-is-an-alias-and-how-do-i-use-it), lo que resulta útil si no desea adquirir un dominio.

#### :material-check:{ .pg-green } Métodos Privados de Pago

Mailbox.org no acepta criptomonedas debido a que su procesador de pagos BitPay suspendió sus operaciones en Alemania. However, they do accept **cash** by mail, **cash** payment to bank account, bank transfer, credit card, PayPal, and a couple of German-specific processors: Paydirekt and Sofortüberweisung.

#### :material-check:{ .pg-green } Seguridad de Cuenta

Mailbox.org supports [two-factor authentication](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa) for their webmail only. Puedes utilizar TOTP o una [YubiKey](https://en.wikipedia.org/wiki/YubiKey) a través de [YubiCloud](https://yubico.com/products/services-software/yubicloud). Web standards such as [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online) are not yet supported.

#### :material-information-outline:{ .pg-blue } Seguridad de Datos

Mailbox.org permite encriptación del correo entrante usando su [buzón encriptado](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox). Nuevos mensajes que recibas se encriptaran inmediatamente con tu clave pública.

However, [Open-Xchange](https://en.wikipedia.org/wiki/Open-Xchange), the software platform used by Mailbox.org, [does not support](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book) the encryption of your address book and calendar. A [standalone option](calendar.md) may be more appropriate for that data.

#### :material-check:{ .pg-green } Encriptación de Correo Electrónico

Mailbox.org tiene [encriptación integrada](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard) en su correo web, lo que simplifica el envío de mensajes a personas con claves públicas OpenPGP. También permiten [a destinatarios remotos descifrar un correo electrónico](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp) en los servidores de Mailbox.org. Esta característica es útil cuando el destinatario remoto no tiene OpenPGP y no puede descifrar una copia del correo electrónico en su propio buzón de correo.

Mailbox.org also supports the discovery of public keys via HTTP from their WKD. This allows people outside of Mailbox.org to find the OpenPGP keys of Mailbox.org accounts easily for cross-provider E2EE. This only applies to email addresses ending in one of Mailbox.org's own domains, like `@mailbox.org`. If you use a custom domain, you must [configure WKD](basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } Cancelación de Cuenta

Tu cuenta se convertirá en una cuenta de usuario restringida cuando tu contrato finalice. Se eliminará luego de [30 días](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } Funcionalidad Adicional

Puedes acceder a tu cuenta de Mailbox.org a través de IMAP/SMTP utilizando su [servicio.onion](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org). However, their webmail interface cannot be accessed via their .onion service, and you may experience TLS certificate errors.

Todas las cuentas incluyen almacenamiento limitado en la nube que [puede cifrarse](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive). Mailbox.org también ofrece el alias [@secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely), que impone el cifrado TLS en la conexión entre servidores de correo; de lo contrario, el mensaje no se enviará en absoluto. Mailbox.org también admite [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync) además de protocolos de acceso estándar como IMAP y POP3.

Mailbox.org tiene una función de legado digital para todos los planes. You can choose whether you want any of your data to be passed to heirs, providing that they apply and provide your testament. Alternativamente, puedes designar a una persona por su nombre y dirección.

## Más Proveedores

Estos proveedores almacenan tus correos electrónicos con cifrado de cero-conocimiento, lo que los convierte en excelentes opciones para mantener seguros tus correos electrónicos almacenados. Sin embargo, no admiten normas de cifrado interoperables para las comunicaciones E2EE entre distintos proveedores.

<div class="grid cards" markdown>

- ![Logo de Tuta](assets/img/email/tuta.svg#only-light){ .twemoji loading=lazy }![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ .twemoji loading=lazy } [Tuta](email.md#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Tuta logo](assets/img/email/tuta.svg#only-light){ align=right }
![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ align=right }

**Tuta** (antes *Tutanota*) es un servicio de correo electrónico centrado en la seguridad y la privacidad mediante el uso de cifrado. Tuta lleva funcionando desde 2011 y tiene su sede en Hannover, Alemania.

Free accounts start with 1 GB of storage.

[:octicons-home-16: Página Principal](https://tuta.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tuta.com/privacy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://tuta.com/support){ .card-link title="Documentación" }
[:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://tuta.com/community){ .card-link title="Contribuir" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

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

Tuta only directly accepts credit cards and PayPal, however [**cryptocurrency**](cryptocurrency.md) can be used to purchase gift cards via their [partnership](https://tuta.com/support/#cryptocurrency) with ProxyStore.

#### :material-check:{ .pg-green } Seguridad de Cuenta

Tuta supports [two-factor authentication](https://tuta.com/support#2fa) with either TOTP or U2F.

#### :material-check:{ .pg-green } Seguridad de los datos

Tuta has [zero-access encryption at rest](https://tuta.com/support#what-encrypted) for your emails, [address book contacts](https://tuta.com/support#encrypted-address-book), and [calendars](https://tuta.com/support#calendar). Esto significa que sólo tú puedes leer los mensajes y otros datos almacenados en tu cuenta.

#### :material-information-outline:{ .pg-blue } Cifrado de correo electrónico

Tuta [no utiliza OpenPGP](https://tuta.com/support/#pgp). Las cuentas de Tuta solo pueden recibir correos electrónicos cifrados de cuentas de correo electrónico que no sean de Tuta cuando se envían a través de un [buzón temporal de Tuta](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } Cancelación de la cuenta

Tuta [elimina las cuentas gratuitas inactivas](https://tuta.com/support#inactive-accounts) luego de seis meses. Puedes reutilizar una cuenta gratuita desactivada si pagas.

#### :material-information-outline:{ .pg-blue } Funciones adicionales

Tuta ofrece una versión empresarial para [organizaciones sin fines de lucro](https://tuta.com/blog/secure-email-for-non-profit) de manera gratuita o con un importante descuento.

## Criterios

**Por favor, ten en cuenta que no estamos afiliados con ninguno de los proveedores que recomendamos.** Además de [nuestros criterios estándar](about/criteria.md), hemos desarrollado un claro conjunto de requisitos para cualquier proveedor de correo electrónico que desee ser recomendado, incluyendo la implementación de las mejores prácticas de la industria, tecnología moderna y más. Sugerimos que te familiarices con esta lista antes de elegir un proveedor de correo electrónico, y que realices tu propia investigación para asegurarte de que el proveedor de correo electrónico que elijas sea la opción adecuada para ti.

### Tecnología

Consideramos que estas características son importantes para ofrecer un servicio seguro y óptimo. Debes considerar si el proveedor tiene las características que necesita.

**Mínimo para calificar:**

- Must encrypt email account data at rest with zero-access encryption.
- Must be capable of exporting emails as [Mbox](https://en.wikipedia.org/wiki/Mbox) or individual .EML with [RFC5322](https://datatracker.ietf.org/doc/rfc5322) standard.
- Allow users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). Los nombres de dominio personalizados son importantes para los usuarios porque les permiten mantener su agencia del servicio, en caso de que éste se estropee o sea adquirido por otra empresa que no dé prioridad a la privacidad.
- Must operate on owned infrastructure, i.e. not built upon third-party email service providers.

**Mejor Caso:**

- Should encrypt all account data (contacts, calendars, etc.) at rest with zero-access encryption.
- Should provide integrated webmail E2EE/PGP encryption as a convenience.
- Should support WKD to allow improved discovery of public OpenPGP keys via HTTP. GnuPG users can get a key with this command: `gpg --locate-key example_user@example.com`.
- Soporte para un buzón temporal para usuarios externos. This is useful when you want to send an encrypted email without sending an actual copy to your recipient. Estos correos electrónicos suelen tener una vida útil limitada y luego se eliminan automáticamente. Tampoco requieren que el destinatario configure ninguna criptografía como OpenPGP.
- Should support [sub-addressing](https://en.wikipedia.org/wiki/Email_address#Sub-addressing).
- Should allow users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). Los nombres de dominio personalizados son importantes para los usuarios porque les permiten mantener su agencia del servicio, en caso de que éste se estropee o sea adquirido por otra empresa que no dé prioridad a la privacidad.
- Catch-all or alias functionality for those who use their own domains.
- Should use standard email access protocols such as IMAP, SMTP, or [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Standard access protocols ensure customers can easily download all of their email, should they want to switch to another provider.
- Email provider's services should be available via an [onion service](https://en.wikipedia.org/wiki/.onion).

### Privacidad

Preferimos que nuestros proveedores recomendados recojan la menor cantidad de datos posible.

**Mínimo para Calificar:**

- Must protect sender's IP address, which can involve filtering it from showing in the `Received` header field.
- Must not require personally identifiable information (PII) besides a username and a password.
- Privacy policy must meet the requirements defined by the GDPR.

**Mejor Caso:**

- Should accept [anonymous payment options](advanced/payments.md) ([cryptocurrency](cryptocurrency.md), cash, gift cards, etc.)
- Should be hosted in a jurisdiction with strong email privacy protection laws.

### Seguridad

Email servers deal with a lot of very sensitive data. We expect that providers will adopt industry best practices in order to protect their customers.

**Mínimo para Calificar:**

- Protection of webmail with 2FA, such as [TOTP](basics/multi-factor-authentication.md#time-based-one-time-password-totp).
- Zero-access encryption, which builds on encryption at rest. El proveedor no disponga de las claves de descifrado de los datos que posee. Esto evita que un empleado deshonesto filtre datos a los que tiene acceso o que un adversario remoto divulgue datos que ha robado al obtener acceso no autorizado al servidor.
- Compatible con [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions).
- Sin errores o vulnerabilidades TLS al ser perfilado por herramientas como [Hardenize](https://hardenize.com), [testssl.sh](https://testssl.sh) o [Qualys SSL Labs](https://ssllabs.com/ssltest); esto incluye errores relacionados con certificados y parámetros DH débiles, como los que llevaron a [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- A server suite preference (optional on TLS 1.3) for strong cipher suites which support forward secrecy and authenticated encryption.
- Una política válida [MTA-STS](https://tools.ietf.org/html/rfc8461) y [TLS-RPT](https://tools.ietf.org/html/rfc8460).
- Registros válidos de [DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities).
- Registros válidos [SPF](https://en.wikipedia.org/wiki/Sender_Policy_Framework) y [DKIM](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail).
- Must have a proper [DMARC](https://en.wikipedia.org/wiki/DMARC) record and policy or use [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) for authentication. Si se utiliza la autenticación DMARC, la política debe establecerse en `rechazar` o `cuarentena`.
- Una preferencia de suite de servidor de TLS 1.2 o posterior y un plan para [RFC8996](https://datatracker.ietf.org/doc/rfc8996).
- [Envío de SMTPS](https://en.wikipedia.org/wiki/SMTPS), suponiendo que se utiliza SMTP.
- Estándares de seguridad del sitio web tales como:
    - [Seguridad de transporte estricta HTTP](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - [Integridad de subrecurso](https://en.wikipedia.org/wiki/Subresource_Integrity) si se cargan cosas desde dominios externos.
- Debe admitir la visualización de [encabezados de mensaje](https://en.wikipedia.org/wiki/Email#Message_header), ya que es una característica forense crucial para determinar si un correo electrónico es un intento de phishing.

**Mejor Caso:**

- Should support hardware authentication, i.e. U2F y [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online).
- [Registro de recursos de autorización de autoridad de certificación (CAA) de DNS](https://tools.ietf.org/html/rfc6844) además del soporte de DANE.
- Should implement [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), which is useful for people who post to mailing lists [RFC8617](https://tools.ietf.org/html/rfc8617).
- Published security audits from a reputable, third-party firm.
- Programas de recompensa de errores y/o un proceso coordinado de divulgación de vulnerabilidades.
- Estándares de seguridad del sitio web tales como:
    - [Política de seguridad de contenido (CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### Confianza

You wouldn't trust your finances to someone with a fake identity, so why trust them with your email? Requerimos que nuestros proveedores recomendados sean públicos sobre su propiedad o liderazgo. También nos gustaría ver informes de transparencia frecuentes, especialmente en lo que se refiere a cómo se gestionan las solicitudes del gobierno.

**Mínimo para Calificar:**

- Liderazgo o propiedad de cara al público.

**Mejor Caso:**

- Informes de transparencia frecuentes.

### Marketing

With the email providers we recommend, we like to see responsible marketing.

**Mínimo para Calificar:**

- Must self-host analytics (no Google Analytics, Adobe Analytics, etc.).
- Must not have any irresponsible marketing, which can include the following:
    - Claims of "unbreakable encryption." Encryption should be used with the intention that it may not be secret in the future when the technology exists to crack it.
    - Guarantees of protecting anonymity 100%. When someone makes a claim that something is 100%, it means there is no certainty for failure. We know people can quite easily de-anonymize themselves in a number of ways, e.g.:
        - Reusing personal information e.g. (email accounts, unique pseudonyms, etc.) that they accessed without anonymity software such as Tor
        - [Browser fingerprinting](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**Mejor Caso:**

- Clear and easy-to-read documentation for tasks like setting up 2FA, email clients, OpenPGP, etc.

### Funcionalidad Adicional

While not strictly requirements, there are some other convenience or privacy factors we looked into when determining which providers to recommend.
