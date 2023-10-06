---
meta_title: "Por Qué el Correo Electrónico No es la Mejor Opción para la Privacidad y la Seguridad - Privacy Guides"
title: Seguridad del correo electrónico
icon: material/email
description: El correo electrónico es intrínsecamente inseguro en muchos aspectos, y éstas son algunas de las razones por las que no es nuestra primera opción para las comunicaciones seguras.
---

El correo electrónico es una forma de comunicación insegura por defecto. Puedes mejorar la seguridad de tu correo electrónico con herramientas como OpenPGP, que añaden cifrado de extremo a extremo a tus mensajes, pero OpenPGP sigue teniendo una serie de inconvenientes en comparación con el cifrado de otras aplicaciones de mensajería, y algunos datos del correo electrónico nunca pueden cifrarse de forma inherente debido a cómo está diseñado el correo electrónico.

En consecuencia, el correo electrónico se utiliza mejor para recibir correos electrónicos transaccionales (como notificaciones, correos de verificación, restablecimiento de contraseñas, etc.) de los servicios en los que te registras en línea, no para comunicarte con otras personas.

## Descripción de la encriptación del correo electrónico

La forma estándar de añadir E2EE a los correos electrónicos entre diferentes proveedores de correo electrónico es utilizando OpenPGP. Existen diferentes implementaciones del estándar OpenPGP, siendo las más comunes [GnuPG](https://es.wikipedia.org/wiki/GNU_Privacy_Guard) y [OpenPGP.js](https://openpgpjs.org).

Hay otro estándar que es popular entre las empresas llamada [S/MIME](https://es.wikipedia.org/wiki/S/MIME), sin embargo, requiere un certificado emitido por una [Autoridad de certificación](https://es.wikipedia.org/wiki/Autoridad_de_certificaci%C3%B3n) (no todos emiten certificados S/MIME). Tiene soporte en [Google Workplace](https://support.google.com/a/topic/9061730?hl=es&amp%3Bref_topic=9061731) y [Outlook para Web o Exchange Server 2016, 2019](https://support.microsoft.com/es-es/office/cifrar-mensajes-mediante-s-mime-en-outlook-en-la-web-878c79fc-7088-4b39-966f-14512658f480?ui=en-us&rs=en-us&ad=us).

Incluso si utilizas OpenPGP, no admite el [secreto perfecto hacia adelante](https://es.wikipedia.org/wiki/Perfect_forward_secrecy), lo que significa que si alguna vez se roba tu clave privada o la del destinatario, todos los mensajes anteriores cifrados con ella se expondrán. Es por eso que recomendamos [servicios de mensajería instantáneos](../real-time-communication.md) que implementan el secreto perfecto hacia adelante por sobre el correo electrónico para las comunicaciones de persona a persona siempre que sea posible.

## What is the Web Key Directory standard?

The Web Key Directory (WKD) standard allows email clients to discover the OpenPGP key for other mailboxes, even those hosted on a different provider. Email clients which support WKD will ask the recipient's server for a key based on the email address' domain name. For example, if you emailed `jonah@privacyguides.org`, your email client would ask `privacyguides.org` for Jonah's OpenPGP key, and if `privacyguides.org` has a key for that account, your message would be automatically encrypted.

In addition to the [email clients we recommend](../email-clients.md) which support WKD, some webmail providers also support WKD. Whether *your own* key is published to WKD for others to use depends on your domain configuration. If you use an [email provider](../email.md#openpgp-compatible-services) which supports WKD, such as Proton Mail or Mailbox.org, they can publish your OpenPGP key on their domain for you.

If you use your own custom domain, you will need to configure WKD separately. If you control your domain name, you can set up WKD regardless of your email provider. One easy way to do this is to use the "[WKD as a Service](https://keys.openpgp.org/about/usage#wkd-as-a-service)" feature from keys.openpgp.org, by setting a CNAME record on the `openpgpkey` subdomain of your domain pointed to `wkd.keys.openpgp.org`, then uploading your key to [keys.openpgp.org](https://keys.openpgp.org/). Alternatively, you can [self-host WKD on your own web server](https://wiki.gnupg.org/WKDHosting).

If you use a shared domain from a provider which doesn't support WKD, like @gmail.com, you won't be able to share your OpenPGP key with others via this method.

### ¿Qué clientes de correo electrónico admiten E2EE?

Los proveedores de correo electrónico que permiten utilizar protocolos de acceso estándar como IMAP y SMTP pueden utilizarse con cualquiera de los clientes de correo electrónico [que recomendamos](../email-clients.md). Dependiendo del método de autenticación, esto puede conducir a la disminución de la seguridad si el proveedor o el cliente de correo electrónico no soporta OATH o una aplicación puente debido a que la [autenticación multifactor](multi-factor-authentication.md) no es posible con la autenticación de contraseña simple.

### ¿Cómo puedo proteger mis claves privadas?

Una tarjeta inteligente (como una [Yubikey](https://support.yubico.com/hc/en-us/articles/360013790259-Using-Your-YubiKey-with-OpenPGP) o una [Nitrokey](https://www.nitrokey.com)) funciona recibiendo un mensaje de correo electrónico cifrado desde un dispositivo (teléfono, tableta, ordenador, etc.) que ejecuta un cliente de correo electrónico/correo web. El mensaje es entonces descifrado por la tarjeta inteligente y el contenido descifrado es enviado de vuelta al dispositivo.

It is advantageous for the decryption to occur on the smartcard to avoid possibly exposing your private key to a compromised device.

## Descripción general de los metadatos de correo electrónico

Los metadatos del correo electrónico se almacenan en la [cabecera del mensaje](https://es.wikipedia.org/wiki/Correo_electr%C3%B3nico#Escritura_del_mensaje) del correo electrónico e incluye algunas cabeceras visibles que puedes haber visto como: `Para`, `De`, `Cc`, `Fecha`, `Asunto`. También hay una serie de encabezados ocultos incluidos por muchos clientes y proveedores de correo electrónico que pueden revelar información sobre tu cuenta.

El software del cliente puede usar metadatos de correo electrónico para mostrar de quién es un mensaje y a qué hora se recibió. Los servidores pueden utilizarlo para determinar dónde debe enviarse un mensaje de correo electrónico, [entre otros fines](https://es.wikipedia.org/wiki/Correo_electr%C3%B3nico#Escritura_del_mensaje) que no siempre son transparentes.

### ¿Quién puede ver los metadatos del correo electrónico?

Los metadatos del correo electrónico están protegidos de observadores externos con [STARTTLS](https://es.wikipedia.org/wiki/STARTTLS) protegiéndolos de observadores externos, pero aún pueden ser vistos por tu software de cliente de correo electrónico (o webmail) y cualquier servidor que retransmita el mensaje de ti a cualquier destinatario, incluyendo tu proveedor de correo electrónico. A veces, los servidores de correo electrónico también utilizan servicios de terceros para protegerse del spam, que generalmente también tienen acceso a tus mensajes.

### ¿Por qué los metadatos no pueden ser E2EE?

Los metadatos del correo electrónico son cruciales para la funcionalidad más básica del correo electrónico (de dónde viene y a dónde tiene que ir). E2EE no estaba integrado originalmente en los protocolos de correo electrónico, sino que requería un software adicional como OpenPGP. Dado que los mensajes OpenPGP todavía tienen que funcionar con los proveedores de correo electrónico tradicionales, no puede cifrar los metadatos del correo electrónico, sino sólo el cuerpo del mensaje. Esto significa que, incluso cuando se utiliza OpenPGP, los observadores externos pueden ver mucha información sobre tus mensajes, como a quién estás enviando correos electrónicos, las líneas de asunto, cuándo estás enviando correos, etc.
