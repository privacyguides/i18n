---
meta_title: "Por Qué el Correo Electrónico No es la Mejor Opción para la Privacidad y la Seguridad - Privacy Guides"
title: Seguridad del correo electrónico
icon: material/email
description: El correo electrónico es inseguro en muchos aspectos, y estas son algunas de las razones por las que no es nuestra primera opción para las comunicaciones seguras.
---

El correo electrónico es una forma de comunicación insegura por defecto. Puedes mejorar la seguridad de tu correo electrónico con herramientas como OpenPGP, que añaden cifrado de extremo a extremo a tus mensajes, pero OpenPGP sigue teniendo una serie de inconvenientes en comparación con el cifrado de otras aplicaciones de mensajería.

En consecuencia, el correo electrónico se utiliza mejor para recibir correos electrónicos transaccionales (como notificaciones, correos de verificación, restablecimiento de contraseñas, etc.) de los servicios en los que te registras en línea, no para comunicarte con otras personas.

## Descripción de la encriptación del correo electrónico

La forma estándar de añadir E2EE a los correos electrónicos entre diferentes proveedores de correo electrónico es utilizando OpenPGP. Existen diferentes implementaciones del estándar OpenPGP, siendo las más comunes [GnuPG](../encryption.md#gnu-privacy-guard) y [OpenPGP.js](https://openpgpjs.org).

Aunque utilices OpenPGP, no es compatible con [el secreto hacia adelante](https://en.wikipedia.org/wiki/Forward_secrecy), lo que significa que si alguna vez te roban la clave privada a ti o al destinatario del mensaje, todos los mensajes cifrados previamente con ella quedarán expuestos. Es por eso que recomendamos [servicios de mensajería instantáneos](../real-time-communication.md) que implementan el secreto perfecto hacia adelante por sobre el correo electrónico para las comunicaciones de persona a persona siempre que sea posible.

Existe otro estándar muy popular entre las empresas, llamado [S/MIME](https://en.wikipedia.org/wiki/S/MIME), pero requiere un certificado emitido por una [Autoridad de Certificación](https://en.wikipedia.org/wiki/Certificate_authority) (no todas emiten certificados S/MIME y a menudo hay que pagar una cuota anual). En algunos casos es más útil que PGP porque es compatible con aplicaciones de correo electrónico populares como Apple Mail, [Google Workplace](https://support.google.com/a/topic/9061730) y [Outlook](https://support.office.com/article/encrypt-messages-by-using-s-mime-in-outlook-on-the-web-878c79fc-7088-4b39-966f-14512658f480). Sin embargo, S/MIME no resuelve el problema de la falta de secreto hacia adelante, y no es particularmente más seguro que PGP.

## ¿Qué es el estándar del Directorio de Claves Web?

El estándar [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD) permite a los clientes de correo electrónico descubrir la clave OpenPGP de otros buzones, incluso los alojados en un proveedor diferente. Los clientes de correo electrónico compatibles con WKD le solicitarán al servidor receptor una clave basada en el nombre de dominio de la dirección de correo electrónico. Por ejemplo, si envías un correo electrónico a `jonah@privacyguides.org`, tu cliente de correo electrónico le solicitará a `privacyguides.org` la clave OpenPGP de Jonah, y si `privacyguides.org` tiene la clave para esa cuenta, tu mensaje se encriptará automáticamente.

Además de los [clientes de correo electrónico que recomendamos](../email-clients.md) y son compatibles con WKD, algunos clientes web de correo electrónico también son compatibles con WKD. Si *tu propia* clave es publicada en WKD para que otros la utilicen, esto dependerá de tu configuración de dominio. Si utilizas un [proveedor de correo electrónico](../email.md#openpgp-compatible-services) compatible con WKD, como Proton Mail o Mailbox.org, ellos pueden publicar tu clave OpenPGP en su dominio por usted.

Su utilizas tu propio dominio personalizado, necesitarás configurar WKD por separado. Si tienes control sobre tu nombre de dominio, puedes configurar WKD sin importar el proveedor de correo electrónico que utilices. Una forma sencilla de hacer esto es utilizar la función «[WKD as a Service](https://keys.openpgp.org/about/usage#wkd-as-a-service)» del servidor `keys.openpgp.org`: Establece un registro CNAME en el subdominio `openpgpkey` de tu dominio apuntando a `wkd.keys.openpgp.org`, luego sube tu clave a [keys.openpgp.org](https://keys.openpgp.org). De manera alternativa, puedes [hospedar WKD en tu propio servidor web](https://wiki.gnupg.org/WKDHosting).

Si utilizas un dominio compartido de un proveedor que no admite WKD, como `@gmail.com`, no podrás compartir tu clave OpenPGP con otros a través de este método.

### ¿Qué clientes de correo electrónico admiten E2EE?

Los proveedores de correo electrónico que permiten utilizar protocolos de acceso estándar como IMAP y SMTP pueden utilizarse con cualquiera de los clientes de correo electrónico [que recomendamos](../email-clients.md). Dependiendo del método de autenticación, esto puede conducir a una disminución de la seguridad si el proveedor o el cliente de correo electrónico no es compatible con [OAuth](account-creation.md#sign-in-with-oauth) o una aplicación puente, ya que la [autenticación multifactor](multi-factor-authentication.md) no es posible con la autenticación de contraseña simple.

### ¿Cómo puedo proteger mis claves privadas?

Una tarjeta inteligente (como [YubiKey](https://support.yubico.com/hc/articles/360013790259-Using-Your-YubiKey-with-OpenPGP) o [Nitrokey](../security-keys.md#nitrokey)) funciona recibiendo un mensaje de correo electrónico cifrado desde un dispositivo (teléfono, tableta, ordenador, etc.) que ejecute un cliente de correo electrónico/correo web. A continuación, la tarjeta inteligente descifra el mensaje y envía el contenido descifrado al dispositivo.

Es beneficioso que el descifrado se produzca en la tarjeta inteligente para evitar la posible exposición de tu clave privada a un dispositivo comprometido.

## Descripción general de los metadatos de correo electrónico

Los metadatos del correo electrónico se almacenan en el [encabezado del mensaje](https://en.wikipedia.org/wiki/Email#Message_header) del correo electrónico e incluyen algunos encabezados visibles que es posible que hayas visto, como `Para`, `De`, `CC`, `Fecha` y `Asunto`. También hay una serie de encabezados ocultos incluidos por muchos clientes y proveedores de correo electrónico que pueden revelar información sobre tu cuenta.

El software del cliente puede usar metadatos de correo electrónico para mostrar de quién es un mensaje y a qué hora se recibió. Los servidores pueden utilizarlo para determinar dónde debe enviarse un mensaje de correo electrónico, [entre otros fines](https://es.wikipedia.org/wiki/Correo_electr%C3%B3nico#Escritura_del_mensaje) que no siempre son transparentes.

### ¿Quién puede ver los metadatos del correo electrónico?

Los metadatos del correo electrónico están protegidos de observadores externos con [TLS oportunista](https://en.wikipedia.org/wiki/Opportunistic_TLS), pero aún pueden ser vistos por tu software de cliente de correo electrónico (o webmail) y cualquier servidor que retransmita el mensaje de ti a cualquier destinatario, incluido tu proveedor de correo electrónico. A veces, los servidores de correo electrónico también utilizan servicios de terceros para protegerse del spam, que generalmente también tienen acceso a tus mensajes.

### ¿Por qué los metadatos no pueden ser E2EE?

Los metadatos del correo electrónico son cruciales para la funcionalidad más básica del correo electrónico (de dónde viene y a dónde tiene que ir). Originalmente, E2EE no estaba integrado en los protocolos de correo electrónico estándar, sino que requería un software adicional como OpenPGP. Dado que los mensajes OpenPGP siguen teniendo que funcionar con proveedores de correo electrónico tradicionales, no puede cifrar algunos de estos metadatos de correo electrónico necesarios para identificar a las partes que se comunican. Esto significa que, aunque utilices OpenPGP, los observadores externos pueden ver mucha información sobre tus mensajes, como a quién envías correos, cuándo lo haces, etc.
