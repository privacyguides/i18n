---
title: Llaves de seguridad
icon: material/key-chain
description: Estas llaves de seguridad proporcionan una forma de autenticación inmune al phishing para las cuentas que lo admiten.
cover: multi-factor-authentication.webp
---

<small>Protege contra las siguientes amenazas:</small>

- [:material-target-account: Ataques dirigidos](basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: Ataques pasivos](basics/common-threats.md#security-and-privacy){ .pg-orange }

Una **llave de seguridad** física añade una capa fuerte de protección a tus cuentas en línea. A comparación con las [aplicaciones de autenticación](multi-factor-authentication.md), el protocolo de llave de seguridad FIDO2 es innume al phishing y no puede ser comprometido sin tener la llave física. Muchos servicios admiten FIDO2/WebAuthn como opción de autenticación multifactor para proteger tu cuenta, y algunos servicios te permiten utilizar una llave de seguridad como autenticador fuerte de factor único con autenticación sin contraseña.

## Llave de seguridad Yubico

<div class="admonition recommendation" markdown>

<figure markdown="span">  ![Serie de llaves de seguridad por Yubico](assets/img/security-keys/yubico-security-key.webp){ width="315" }</figure>

La serie **Yubico Security Key** es la llave de seguridad física más rentable con certificación FIDO de Nivel 2[^1]. Esta es compatible con FIDO2/WebAuthn y FIDO U2F, y funciona con muchos servicios compatibles con una llave de seguridad como segundo factor, así como con muchos gestores de contraseñas.

[:octicons-home-16: Página Principal](https://yubico.com/products/security-key){ .md-button .md-button--primary }
[:octicons-eye-16:](https://yubico.com/support/terms-conditions/privacy-notice){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://docs.yubico.com){ .card-link title="Documentación" }

</details>

</div>

Estas llaves están disponibles en variantes USB-C y USB-A, y ambas opciones soportan NFC para ser utilizadas con un dispositivo móvil.

Esta llave proporciona únicamente la funcionalidad básica de FIDO2, pero para la mayoría de las personas esto es todo lo que necesitan. Algunas características notables que la serie de llave de seguridad **no** incluye son:

- [Autenticador Yubico](https://yubico.com/products/yubico-authenticator)
- Soporte para la tarjeta inteligente CCID (compatible con PIV)
- OpenPGP

Si necesitas alguna de estas características, deberías considerar alguno de los [YubiKey](#yubikey) de alta gama.

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

El firmware de las llaves de seguridad de Yubico no es actualizable. Si quieres características en las versiones de firmware más nuevas o hay alguna vulnerabilidad en la versión de firmware que estás utilizando, necesitas adquirir una nueva llave.

</div>

## YubiKey

<div class="admonition recommendation" markdown>

<figure markdown="span">  ![YubiKeys](assets/img/security-keys/yubikey.png){ width="400" }</figure>

La serie **YubiKey** de Yubico se encuentra entre las llaves de seguridad más populares con certificación FIDO de Nivel 2[^1]. La serie YubiKey 5 cuenta con una amplia gama de funciones como [Segundo Factor Universal (U2F)](https://en.wikipedia.org/wiki/Universal_2nd_Factor), [FIDO2 y WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online), [Yubico OTP](basics/multi-factor-authentication.md#yubico-otp), [Verificación de Identidad Personal (PIV)](https://developers.yubico.com/PIV), [OpenPGP](https://developers.yubico.com/PGP) y autenticación [TOTP y HOTP](https://developers.yubico.com/OATH).

[:octicons-home-16: Página Principal](https://yubico.com/products/yubikey-5-overview){ .md-button .md-button--primary }
[:octicons-eye-16:](https://yubico.com/support/terms-conditions/privacy-notice){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://docs.yubico.com){ .card-link title="Documentación" }

</details>

</div>

La [tabla comparativa](https://yubico.com/store/compare) muestra cómo se comparan las YubiKeys entre sí y con la serie [Security Key](#yubico-security-key) de Yubico en términos de características y otras especificaciones. Uno de los beneficios de la serie YubiKey es que una llave puede realizar casi todo lo que puedes esperar de una llave de seguridad física. Te recomendamos realizar su [cuestionario](https://yubico.com/quiz) antes de comprar para asegurarte de que eliges la llave de seguridad adecuada.

Las YubiKeys pueden ser programadas utilizando [YubiKey Manager](https://yubico.com/support/download/yubikey-manager) o [YubiKey Personalization Tools](https://yubico.com/support/download/yubikey-personalization-tools). Para gestionar los códigos TOTP, puedes utilizar el [Autenticador Yubico](https://yubico.com/products/yubico-authenticator). Todos los clientes de Yubico son de código abierto.

Para los modelos compatibles con HOTP y TOTP, hay 2 ranuras en la interfaz OTP que pueden utilizarse para HOTP y 32 ranuras para almacenar secretos TOTP. Estos secretos se almacenan cifrados en la llave y nunca son expuestos a los dispositivos a los que se conectan. Cuando una semilla (secreto compartido) es proporcionada al Autenticador Yubico, este solo mostrará el código de seis dígitos y nunca la semilla. Este modelo de seguridad ayuda a limitar lo que un atacante puede reailzar si alguno de los dispositivos en los que se ejecuta el Autenticador Yubico y hace resistente a la YubiKey ante los ataques físicos.

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

El firmware de YubiKey no es actualizable. Si quieres características en las versiones de firmware más nuevas o hay alguna vulnerabilidad en la versión de firmware que estás utilizando, necesitas adquirir una nueva llave.

</div>

## Nitrokey

<div class="admonition recommendation" markdown>

<figure markdown="span">  ![Nitrokey](assets/img/security-keys/nitrokey.jpg){ width="300" }</figure>

**Nitrokey** tiene una llave de seguridad compatible con [FIDO2 y WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online) llamada **Nitrokey FIDO2**. Para obtener compatibilidad con PGP, necesitas comprar una de sus otras llaves, como la **Nitrokey Start**, la **Nitrokey Pro 2** o la **Nitrokey Storage 2**.

[:octicons-home-16: Página Principal](https://nitrokey.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nitrokey.com/data-privacy-policy){ .card-link title="Politica de Privacidad" }
[:octicons-info-16:](https://docs.nitrokey.com){ .card-link title="Documentación" }

</details>

</div>

La [tabla comparativa](https://nitrokey.com/products/nitrokeys) muestra cómo los diferentes modelos de Nitrokey se comparan entre sí en términos de características y otras especificaciones. La **Nitrokey 3** listada tiene un conjunto combinado de características.

Los modelos de Nitrokey pueden ser configurados utilizando la [aplicación de Nitrokey](https://nitrokey.com/download).

Para los modelos compatibles con HOTP y TOTP, hay 3 ranuras para HOTP y 15 para TOTP. Algunas Nitrokeys pueden actuar como un gestor de contraseñas. Estas pueden almacenar 16 credenciales diferentes y cifrarlas utilizando la misma contraseña de la interfaz OpenPGP.

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

Aunque las Nitrokeys no muestran los secretos HOTP/TOTP a los dispositivos donde se conectan, el almacenamiento HOTP y TOTP **no** está cifrado y es vulnerable ante ataques físicos. Si buscas almacenar secretos HOTP y TOTP, recomendamos utilizar una Yubikey.

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

El restablecimiento de la interfaz OpenPGP en una Nitrokey [Pro 2](https://docs.nitrokey.com/nitrokeys/pro/factory-reset) o Nitrokey [Start 2](https://docs.nitrokey.com/nitrokeys/storage/factory-reset) también hará que la base de datos de contraseñas sea inaccesible.

</div>

## Criterios

**Por favor, ten en cuenta que no estamos afiliados a ninguno de los proyectos que recomendamos.** Además de [nuestros criterios estándar](about/criteria.md), hemos desarrollado un conjunto claro de requisitos que nos permiten ofrecer recomendaciones objetivas. Sugerimos que te familiarices con esta lista, antes de decidir utilizar un proyecto y realizar tu propia investigación para asegurarte de que es la elección ideal para ti.

### Requisitos Mínimos

- Debe utilizar módulos de seguridad físicos de alta calidad y a prueba de manipulaciones.
- Debe soportar la última especificación FIDO2.
- No debe permitir la extracción de claves privadas.
- Los dispositivos con un precio mayor a $35 dólares, deben soportar OpenPGP y S/MIME.

### Mejor Caso

Nuestro criterio del mejor caso representa lo que nos gustaría ver del proyecto perfecto en esta categoría. Es posible que nuestras recomendaciones no incluyan todas o algunas de estas funciones, pero las que sí las incluyan pueden estar mejor clasificadas que otras en esta página.

- Debería estar disponible en formato USB-C.
- Debería ser compatible con NFC.
- Debería soportar el almacenamiento de secretos TOTP.
- Debería soportar actualizaciones seguras de firmware.

[^1]: Algunos gobiernos u otras organizaciones pueden exigir una llave con certificación de Nivel 2, pero la mayoría de la gente no tiene que preocuparse por esta distinción.
