---
meta_title: "Por Qué el Correo Electrónico No es la Mejor Opción para la Privacidad y la Seguridad - Privacy Guides"
title: Seguridad del correo electrónico
icon: material/email
description: Email is insecure in many ways, and these are some of the reasons it isn't our top choice for secure communications.
---

El correo electrónico es una forma de comunicación insegura por defecto. You can improve your email security with tools such as OpenPGP, which add End-to-End Encryption to your messages, but OpenPGP still has a number of drawbacks compared to encryption in other messaging applications.

En consecuencia, el correo electrónico se utiliza mejor para recibir correos electrónicos transaccionales (como notificaciones, correos de verificación, restablecimiento de contraseñas, etc.) de los servicios en los que te registras en línea, no para comunicarte con otras personas.

## Descripción de la encriptación del correo electrónico

La forma estándar de añadir E2EE a los correos electrónicos entre diferentes proveedores de correo electrónico es utilizando OpenPGP. Existen diferentes implementaciones del estándar OpenPGP, siendo las más comunes [GnuPG](https://es.wikipedia.org/wiki/GNU_Privacy_Guard) y [OpenPGP.js](https://openpgpjs.org).

Incluso si utilizas OpenPGP, no admite el [secreto perfecto hacia adelante](https://es.wikipedia.org/wiki/Perfect_forward_secrecy), lo que significa que si alguna vez se roba tu clave privada o la del destinatario, todos los mensajes anteriores cifrados con ella se expondrán. Es por eso que recomendamos [servicios de mensajería instantáneos](../real-time-communication.md) que implementan el secreto perfecto hacia adelante por sobre el correo electrónico para las comunicaciones de persona a persona siempre que sea posible.

There is another standard which is popular with business called [S/MIME](https://en.wikipedia.org/wiki/S/MIME), however, it requires a certificate issued from a [Certificate Authority](https://en.wikipedia.org/wiki/Certificate_authority) (not all of them issue S/MIME certificates, and often a yearly payment is required). In some cases it is more usable than PGP because it has support in popular/mainstream email applications like Apple Mail, [Google Workplace](https://support.google.com/a/topic/9061730), and [Outlook](https://support.office.com/article/encrypt-messages-by-using-s-mime-in-outlook-on-the-web-878c79fc-7088-4b39-966f-14512658f480). However, S/MIME does not solve the issue of lack of forward secrecy, and isn't particularly more secure than PGP.

## ¿Qué es el estándar del Directorio de Claves Web?

The [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD) standard allows email clients to discover the OpenPGP key for other mailboxes, even those hosted on a different provider. Los clientes de correo electrónico compatibles con WKD le solicitarán al servidor receptor una clave basada en el nombre de dominio de la dirección de correo electrónico. Por ejemplo, si envías un correo electrónico a `jonah@privacyguides.org`, tu cliente de correo electrónico le solicitará a `privacyguides.org` la clave OpenPGP de Jonah, y si `privacyguides.org` tiene la clave para esa cuenta, tu mensaje se encriptará automáticamente.

Además de los [clientes de correo electrónico que recomendamos](../email-clients.md) y son compatibles con WKD, algunos clientes web de correo electrónico también son compatibles con WKD. Si *tu propia* clave es publicada en WKD para que otros la utilicen, esto dependerá de tu configuración de dominio. Si utilizas un [proveedor de correo electrónico](../email.md#openpgp-compatible-services) compatible con WKD, como Proton Mail o Mailbox.org, ellos pueden publicar tu clave OpenPGP en su dominio por usted.

Su utilizas tu propio dominio personalizado, necesitarás configurar WKD por separado. Si tienes control sobre tu nombre de dominio, puedes configurar WKD sin importar el proveedor de correo electrónico que utilices. Una manera fácil de hacer esto es utilizar la característica de "[WKD como servicio](https://keys.openpgp.org/about/usage#wkd-as-a-service)", desde keys.openpgp.org, al configurar un registro CNAME en el subdominio de `openpgpkey` de tu dominio, apuntando a `wkd.keys.openpgp.org`, y después publicando tu clave en [keys.openpgp.org](https://keys.openpgp.org). De manera alternativa, puedes [hospedar WKD en tu propio servidor web](https://wiki.gnupg.org/WKDHosting).

Si utilizar un dominio compartido desde un proveedor no compatible con WKD, como @gmail.com, no podrás compartir tu clave OpenPGP con otros a través de este método.

### ¿Qué clientes de correo electrónico admiten E2EE?

Los proveedores de correo electrónico que permiten utilizar protocolos de acceso estándar como IMAP y SMTP pueden utilizarse con cualquiera de los clientes de correo electrónico [que recomendamos](../email-clients.md). Depending on the authentication method, this may lead to the decrease security if either the provider or the email client does not support OATH or a bridge application as [multifactor authentication](multi-factor-authentication.md) is not possible with plain password authentication.

### ¿Cómo puedo proteger mis claves privadas?

A smart card (such as a [YubiKey](https://support.yubico.com/hc/articles/360013790259-Using-Your-YubiKey-with-OpenPGP) or [Nitrokey](../security-keys.md#nitrokey)) works by receiving an encrypted email message from a device (phone, tablet, computer, etc.) running an email/webmail client. The message is then decrypted by the smart card and the decrypted content is sent back to the device.

It is advantageous for the decryption to occur on the smart card to avoid possibly exposing your private key to a compromised device.

## Descripción general de los metadatos de correo electrónico

Los metadatos del correo electrónico se almacenan en la [cabecera del mensaje](https://es.wikipedia.org/wiki/Correo_electr%C3%B3nico#Escritura_del_mensaje) del correo electrónico e incluye algunas cabeceras visibles que puedes haber visto como: `Para`, `De`, `Cc`, `Fecha`, `Asunto`. También hay una serie de encabezados ocultos incluidos por muchos clientes y proveedores de correo electrónico que pueden revelar información sobre tu cuenta.

El software del cliente puede usar metadatos de correo electrónico para mostrar de quién es un mensaje y a qué hora se recibió. Los servidores pueden utilizarlo para determinar dónde debe enviarse un mensaje de correo electrónico, [entre otros fines](https://es.wikipedia.org/wiki/Correo_electr%C3%B3nico#Escritura_del_mensaje) que no siempre son transparentes.

### ¿Quién puede ver los metadatos del correo electrónico?

Los metadatos del correo electrónico están protegidos de observadores externos con [STARTTLS](https://es.wikipedia.org/wiki/STARTTLS) protegiéndolos de observadores externos, pero aún pueden ser vistos por tu software de cliente de correo electrónico (o webmail) y cualquier servidor que retransmita el mensaje de ti a cualquier destinatario, incluyendo tu proveedor de correo electrónico. A veces, los servidores de correo electrónico también utilizan servicios de terceros para protegerse del spam, que generalmente también tienen acceso a tus mensajes.

### ¿Por qué los metadatos no pueden ser E2EE?

Los metadatos del correo electrónico son cruciales para la funcionalidad más básica del correo electrónico (de dónde viene y a dónde tiene que ir). E2EE no estaba integrado originalmente en los protocolos de correo electrónico, sino que requería un software adicional como OpenPGP. Because OpenPGP messages still have to work with traditional email providers, it cannot encrypt some of this email metadata required for identifying the parties communicating. That means that even when using OpenPGP, outside observers can see lots of information about your messages, such as whom you're emailing, when you're emailing, etc.
