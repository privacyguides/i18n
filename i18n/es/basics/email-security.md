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

Hay otro estándar que es popular entre las empresas llamada [S/MIME](https://es.wikipedia.org/wiki/S/MIME), sin embargo, requiere un certificado emitido por una [Autoridad de certificación](https://es.wikipedia.org/wiki/Autoridad_de_certificaci%C3%B3n) (no todos emiten certificados S/MIME). It has support in [Google Workplace](https://support.google.com/a/topic/9061730) and [Outlook for Web or Exchange Server 2016, 2019](https://support.office.com/article/encrypt-messages-by-using-s-mime-in-outlook-on-the-web-878c79fc-7088-4b39-966f-14512658f480).

Incluso si utilizas OpenPGP, no admite el [secreto perfecto hacia adelante](https://es.wikipedia.org/wiki/Perfect_forward_secrecy), lo que significa que si alguna vez se roba tu clave privada o la del destinatario, todos los mensajes anteriores cifrados con ella se expondrán. Es por eso que recomendamos [servicios de mensajería instantáneos](../real-time-communication.md) que implementan el secreto perfecto hacia adelante por sobre el correo electrónico para las comunicaciones de persona a persona siempre que sea posible.

## ¿Qué es el estándar del Directorio de Claves Web?

El estándar de Directorio de Claves Web (WKD, por sus siglas en inglés) permite a los clientes de correo electrónico descubrir la clave OpenPGP para otros buzones, incluyendo los que se encuentran hospedados en un proveedor diferente. Los clientes de correo electrónico compatibles con WKD le solicitarán al servidor receptor una clave basada en el nombre de dominio de la dirección de correo electrónico. Por ejemplo, si envías un correo electrónico a `jonah@privacyguides.org`, tu cliente de correo electrónico le solicitará a `privacyguides.org` la clave OpenPGP de Jonah, y si `privacyguides.org` tiene la clave para esa cuenta, tu mensaje se encriptará automáticamente.

Además de los [clientes de correo electrónico que recomendamos](../email-clients.md) y son compatibles con WKD, algunos clientes web de correo electrónico también son compatibles con WKD. Si *tu propia* clave es publicada en WKD para que otros la utilicen, esto dependerá de tu configuración de dominio. Si utilizas un [proveedor de correo electrónico](../email.md#openpgp-compatible-services) compatible con WKD, como Proton Mail o Mailbox.org, ellos pueden publicar tu clave OpenPGP en su dominio por usted.

Su utilizas tu propio dominio personalizado, necesitarás configurar WKD por separado. Si tienes control sobre tu nombre de dominio, puedes configurar WKD sin importar el proveedor de correo electrónico que utilices. One easy way to do this is to use the "[WKD as a Service](https://keys.openpgp.org/about/usage#wkd-as-a-service)" feature from keys.openpgp.org, by setting a CNAME record on the `openpgpkey` subdomain of your domain pointed to `wkd.keys.openpgp.org`, then uploading your key to [keys.openpgp.org](https://keys.openpgp.org). De manera alternativa, puedes [hospedar WKD en tu propio servidor web](https://wiki.gnupg.org/WKDHosting).

Si utilizar un dominio compartido desde un proveedor no compatible con WKD, como @gmail.com, no podrás compartir tu clave OpenPGP con otros a través de este método.

### ¿Qué clientes de correo electrónico admiten E2EE?

Los proveedores de correo electrónico que permiten utilizar protocolos de acceso estándar como IMAP y SMTP pueden utilizarse con cualquiera de los clientes de correo electrónico [que recomendamos](../email-clients.md). Dependiendo del método de autenticación, esto puede conducir a la disminución de la seguridad si el proveedor o el cliente de correo electrónico no soporta OATH o una aplicación puente debido a que la [autenticación multifactor](multi-factor-authentication.md) no es posible con la autenticación de contraseña simple.

### ¿Cómo puedo proteger mis claves privadas?

A smartcard (such as a [YubiKey](https://support.yubico.com/hc/articles/360013790259-Using-Your-YubiKey-with-OpenPGP) or [Nitrokey](https://nitrokey.com)) works by receiving an encrypted email message from a device (phone, tablet, computer, etc.) running an email/webmail client. El mensaje es entonces descifrado por la tarjeta inteligente y el contenido descifrado es enviado de vuelta al dispositivo.

Es ventajoso para el descifrado que suceda en la tarjeta inteligente para evitar la posible exposición de tu clave privada en un dispositivo comprometido.

## Descripción general de los metadatos de correo electrónico

Los metadatos del correo electrónico se almacenan en la [cabecera del mensaje](https://es.wikipedia.org/wiki/Correo_electr%C3%B3nico#Escritura_del_mensaje) del correo electrónico e incluye algunas cabeceras visibles que puedes haber visto como: `Para`, `De`, `Cc`, `Fecha`, `Asunto`. También hay una serie de encabezados ocultos incluidos por muchos clientes y proveedores de correo electrónico que pueden revelar información sobre tu cuenta.

El software del cliente puede usar metadatos de correo electrónico para mostrar de quién es un mensaje y a qué hora se recibió. Los servidores pueden utilizarlo para determinar dónde debe enviarse un mensaje de correo electrónico, [entre otros fines](https://es.wikipedia.org/wiki/Correo_electr%C3%B3nico#Escritura_del_mensaje) que no siempre son transparentes.

### ¿Quién puede ver los metadatos del correo electrónico?

Los metadatos del correo electrónico están protegidos de observadores externos con [STARTTLS](https://es.wikipedia.org/wiki/STARTTLS) protegiéndolos de observadores externos, pero aún pueden ser vistos por tu software de cliente de correo electrónico (o webmail) y cualquier servidor que retransmita el mensaje de ti a cualquier destinatario, incluyendo tu proveedor de correo electrónico. A veces, los servidores de correo electrónico también utilizan servicios de terceros para protegerse del spam, que generalmente también tienen acceso a tus mensajes.

### ¿Por qué los metadatos no pueden ser E2EE?

Los metadatos del correo electrónico son cruciales para la funcionalidad más básica del correo electrónico (de dónde viene y a dónde tiene que ir). E2EE no estaba integrado originalmente en los protocolos de correo electrónico, sino que requería un software adicional como OpenPGP. Dado que los mensajes OpenPGP todavía tienen que funcionar con los proveedores de correo electrónico tradicionales, no puede cifrar los metadatos del correo electrónico, sino sólo el cuerpo del mensaje. Esto significa que, incluso cuando se utiliza OpenPGP, los observadores externos pueden ver mucha información sobre tus mensajes, como a quién estás enviando correos electrónicos, las líneas de asunto, cuándo estás enviando correos, etc.
