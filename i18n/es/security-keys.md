---
title: Llaves de seguridad
icon: material/key-chain
description: These security keys provide a form of phishing-immune authentication for accounts that support it.
cover: multi-factor-authentication.webp
---

<small>Protege contra las siguientes amenazas:</small>

- [:material-target-account: Ataques dirigidos](basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: Ataques pasivos](basics/common-threats.md#security-and-privacy){ .pg-orange }

Una **llave de seguridad** física añade una capa fuerte de protección a tus cuentas en línea. A comparación con las [aplicaciones de autenticación](multi-factor-authentication.md), el protocolo de llave de seguridad FIDO2 es innume al phishing y no puede ser comprometido sin tener la llave física. Many services support FIDO2/WebAuthn as a multifactor authentication option for securing your account, and some services allow you to use a security key as a strong single-factor authenticator with passwordless authentication.

## Llave de seguridad Yubico

<div class="admonition recommendation" markdown>

<figure markdown="span">  ![Serie de llaves de seguridad por Yubico](assets/img/security-keys/yubico-security-key.webp){ width="315" }</figure>

The **Yubico Security Key** series is the most cost-effective hardware security key with FIDO Level 2 certification[^1]. Esta es compatible con FIDO2/WebAuthn y FIDO U2F, y funciona con muchos servicios compatibles con una llave de seguridad como segundo factor, así como con muchos gestores de contraseñas.

[:octicons-home-16: Homepage](https://yubico.com/products/security-key){ .md-button .md-button--primary }
[:octicons-eye-16:](https://yubico.com/support/terms-conditions/privacy-notice){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.yubico.com){ .card-link title="Documentation" }

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

The **YubiKey** series from Yubico are among the most popular security keys with FIDO Level 2 Certification[^1]. The YubiKey 5 Series has a wide range of features such as [Universal 2nd Factor (U2F)](https://en.wikipedia.org/wiki/Universal_2nd_Factor), [FIDO2 and WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online), [Yubico OTP](basics/multi-factor-authentication.md#yubico-otp), [Personal Identity Verification (PIV)](https://developers.yubico.com/PIV), [OpenPGP](https://developers.yubico.com/PGP), and [TOTP and HOTP](https://developers.yubico.com/OATH) authentication.

[:octicons-home-16: Homepage](https://yubico.com/products/yubikey-5-overview){ .md-button .md-button--primary }
[:octicons-eye-16:](https://yubico.com/support/terms-conditions/privacy-notice){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.yubico.com){ .card-link title="Documentation" }

</details>

</div>

The [comparison table](https://yubico.com/store/compare) shows how the YubiKeys compare to each other and to Yubico's [Security Key](#yubico-security-key) series in terms of features and other specifications. Uno de los beneficios de la serie YubiKey es que una llave puede realizar casi todo lo que puedes esperar de una llave de seguridad física. We encourage you to take their [quiz](https://yubico.com/quiz) before purchasing in order to make sure you choose the right security key.

Las YubiKeys pueden ser programadas utilizando [YubiKey Manager](https://yubico.com/support/download/yubikey-manager) o [YubiKey Personalization Tools](https://yubico.com/support/download/yubikey-personalization-tools). Para gestionar los códigos TOTP, puedes utilizar el [Autenticador Yubico](https://yubico.com/products/yubico-authenticator). Todos los clientes de Yubico son de código abierto.

Para los modelos compatibles con HOTP y TOTP, hay 2 ranuras en la interfaz OTP que pueden utilizarse para HOTP y 32 ranuras para almacenar secretos TOTP. These secrets are stored encrypted on the key and never exposed to the devices they are plugged into. Cuando una semilla (secreto compartido) es proporcionada al Autenticador Yubico, este solo mostrará el código de seis dígitos y nunca la semilla. Este modelo de seguridad ayuda a limitar lo que un atacante puede reailzar si alguno de los dispositivos en los que se ejecuta el Autenticador Yubico y hace resistente a la YubiKey ante los ataques físicos.

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

El firmware de YubiKey no es actualizable. Si quieres características en las versiones de firmware más nuevas o hay alguna vulnerabilidad en la versión de firmware que estás utilizando, necesitas adquirir una nueva llave.

</div>

## Nitrokey

<div class="admonition recommendation" markdown>

<figure markdown="span">  ![Nitrokey](assets/img/security-keys/nitrokey.jpg){ width="300" }</figure>

**Nitrokey** tiene una llave de seguridad compatible con [FIDO2 y WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online) llamada **Nitrokey FIDO2**. For PGP support, you need to purchase one of their other keys such as the **Nitrokey Start**, **Nitrokey Pro 2**, or the **Nitrokey Storage 2**.

[:octicons-home-16: Homepage](https://nitrokey.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nitrokey.com/data-privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.nitrokey.com){ .card-link title="Documentation" }

</details>

</div>

The [comparison table](https://nitrokey.com/products/nitrokeys) shows how the different Nitrokey models compare to each other in terms of features and other specifications. La **Nitrokey 3** listada tiene un conjunto combinado de características.

Los modelos de Nitrokey pueden ser configurados utilizando la [aplicación de Nitrokey](https://nitrokey.com/download).

Para los modelos compatibles con HOTP y TOTP, hay 3 ranuras para HOTP y 15 para TOTP. Algunas Nitrokeys pueden actuar como un gestor de contraseñas. Estas pueden almacenar 16 credenciales diferentes y cifrarlas utilizando la misma contraseña de la interfaz OpenPGP.

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

Aunque las Nitrokeys no muestran los secretos HOTP/TOTP a los dispositivos donde se conectan, el almacenamiento HOTP y TOTP **no** está cifrado y es vulnerable ante ataques físicos. Si buscas almacenar secretos HOTP y TOTP, recomendamos utilizar una Yubikey.

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

Resetting the OpenPGP interface on a Nitrokey [Pro 2](https://docs.nitrokey.com/nitrokeys/pro/factory-reset) or Nitrokey [Start 2](https://docs.nitrokey.com/nitrokeys/storage/factory-reset) will also make the password database inaccessible.

</div>

## Criterios

**Por favor, tome en cuenta que no estamos afiliados con ninguno de los proyectos que recomendamos**. Además de [nuestros criterios estándar](about/criteria.md), hemos desarrollado un claro conjunto de requerimientos para permitirnos proporcionar recomendaciones objetivas. Sugerimos que te familiarices con esta lista, antes de decidir utilizar un proyecto y realizar tu propia investigación para asegurarte de que es la elección ideal para ti.

### Requisitos Mínimos

- Must use high-quality, tamper-resistant hardware security modules.
- Debe soportar la última especificación FIDO2.
- No debe permitir la extracción de claves privadas.
- Los dispositivos con un precio mayor a $35 dólares, deben soportar OpenPGP y S/MIME.

### Mejor Caso

Nuestro criterio del mejor caso representa lo que nos gustaría ver del proyecto perfecto en esta categoría. Es posible que nuestras recomendaciones no incluyan todas o algunas de estas funciones, pero las que sí las incluyan pueden estar mejor clasificadas que otras en esta página.

- Should be available in USB-C form factor.
- Debería ser compatible con NFC.
- Debería soportar el almacenamiento de secretos TOTP.
- Debería soportar actualizaciones seguras de firmware.

[^1]: Some governments or other organizations may require a key with Level 2 certification, but most people do not have to worry about this distinction.
