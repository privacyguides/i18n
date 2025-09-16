---
title: Llaves de seguridad
icon: material/key-chain
description: Estas llaves de seguridad proporcionan una forma de autenticación inmune al phishing para las cuentas que lo admiten.
cover: multi-factor-authentication.webp
---

<small>Protege contra las siguientes amenazas:</small>

- [:material-target-account: Ataques dirigidos](basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: Ataques pasivos](basics/common-threats.md#security-and-privacy){ .pg-orange }

Una **llave de seguridad** física añade una capa fuerte de protección a tus cuentas en línea. Compared to [authenticator apps](multi-factor-authentication.md), the [FIDO2](basics/multi-factor-authentication.md#fido-fast-identity-online) security key protocol is immune to phishing, and cannot be compromised without physical possession of the key itself. Muchos servicios admiten FIDO2/WebAuthn como opción de autenticación multifactor para proteger tu cuenta, y algunos servicios te permiten utilizar una llave de seguridad como autenticador fuerte de factor único con autenticación sin contraseña.

## Llave de seguridad Yubico

<div class="admonition recommendation" markdown>

<figure markdown="span">  ![Serie de llaves de seguridad por Yubico](assets/img/security-keys/yubico-security-key.webp){ width="315" }</figure>

La serie **Yubico Security Key** es la llave de seguridad física más rentable con certificación FIDO de Nivel 2[^1]. It supports FIDO2/WebAuthn and FIDO Universal 2nd Factor (U2F), and works out of the box with most services that support a security key as a second factor, as well as many password managers.

[:octicons-home-16: Página Principal](https://yubico.com/products/security-key){ .md-button .md-button--primary }
[:octicons-eye-16:](https://yubico.com/support/terms-conditions/privacy-notice){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://docs.yubico.com){ .card-link title="Documentación" }

</details>

</div>

Estas llaves están disponibles en variantes USB-C y USB-A, y ambas opciones soportan NFC para ser utilizadas con un dispositivo móvil.

Esta llave proporciona únicamente la funcionalidad básica de FIDO2, pero para la mayoría de las personas esto es todo lo que necesitan. Algunas características notables que la serie de llave de seguridad **no** incluye son:

- [Autenticador Yubico](https://yubico.com/products/yubico-authenticator)
- CCID Smart Card support (PIV-compatible)
- OpenPGP

If you need any of those features, you should consider their higher-end [YubiKey](#yubikey) series instead.

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

El firmware de las llaves de seguridad de Yubico no es actualizable. Si quieres características en las versiones de firmware más nuevas o hay alguna vulnerabilidad en la versión de firmware que estás utilizando, necesitas adquirir una nueva llave.

</div>

## YubiKey

<div class="admonition recommendation" markdown>

<figure markdown="span">  ![YubiKeys](assets/img/security-keys/yubikey.png){ width="400" }</figure>

La serie **YubiKey** de Yubico se encuentra entre las llaves de seguridad más populares con certificación FIDO de Nivel 2[^1]. The **YubiKey 5 Series** has a wide range of features such as FIDO2/WebAuthn and FIDO U2F, [TOTP and HOTP](https://developers.yubico.com/OATH) authentication, [Personal Identity Verification (PIV)](https://developers.yubico.com/PIV), and [OpenPGP](https://developers.yubico.com/PGP).

[:octicons-home-16: Página Principal](https://yubico.com/products/yubikey-5-overview){ .md-button .md-button--primary }
[:octicons-eye-16:](https://yubico.com/support/terms-conditions/privacy-notice){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://docs.yubico.com){ .card-link title="Documentación" }

</details>

</div>

La [tabla comparativa](https://yubico.com/store/compare) muestra cómo se comparan las YubiKeys entre sí y con la serie [Security Key](#yubico-security-key) de Yubico en términos de características y otras especificaciones. Uno de los beneficios de la serie YubiKey es que una llave puede realizar casi todo lo que puedes esperar de una llave de seguridad física. Te recomendamos realizar su [cuestionario](https://yubico.com/quiz) antes de comprar para asegurarte de que eliges la llave de seguridad adecuada.

Las YubiKeys pueden ser programadas utilizando [YubiKey Manager](https://yubico.com/support/download/yubikey-manager) o [YubiKey Personalization Tools](https://yubico.com/support/download/yubikey-personalization-tools). Para gestionar los códigos TOTP, puedes utilizar el [Autenticador Yubico](https://yubico.com/products/yubico-authenticator). Todos los clientes de Yubico son de código abierto.

For models which [support HOTP and TOTP](https://support.yubico.com/hc/articles/360013790319-How-many-accounts-can-I-register-my-YubiKey-with), the secrets are stored encrypted on the key and never exposed to the devices they are plugged into. Cuando una semilla (secreto compartido) es proporcionada al Autenticador Yubico, este solo mostrará el código de seis dígitos y nunca la semilla. Este modelo de seguridad ayuda a limitar lo que un atacante puede reailzar si alguno de los dispositivos en los que se ejecuta el Autenticador Yubico y hace resistente a la YubiKey ante los ataques físicos.

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

El firmware de YubiKey no es actualizable. Si quieres características en las versiones de firmware más nuevas o hay alguna vulnerabilidad en la versión de firmware que estás utilizando, necesitas adquirir una nueva llave.

</div>

## Nitrokey

<div class="admonition recommendation" markdown>

<figure markdown="span">  ![Nitrokey](assets/img/security-keys/nitrokey.jpg){ width="300" }</figure>

**Nitrokey** has a cost-effective security key capable of FIDO2/WebAuthn and FIDO U2F called the **Nitrokey Passkey**. For support for features such as PIV, OpenPGP, and TOTP and HOTP authentication, you need to purchase one of their other keys like the **Nitrokey 3**. Currently, only the **Nitrokey 3A Mini** has [FIDO Level 1 Certification](https://nitrokey.com/news/2024/nitrokey-3a-mini-receives-official-fido2-certification).

[:octicons-home-16: Página Principal](https://nitrokey.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nitrokey.com/data-privacy-policy){ .card-link title="Politica de Privacidad" }
[:octicons-info-16:](https://docs.nitrokey.com){ .card-link title="Documentación" }

</details>

</div>

The [comparison table](https://nitrokey.com/products/nitrokeys#:~:text=The%20Nitrokey%20Family) shows how the different Nitrokey models compare to each other in terms of features and other specifications. Refer to Nitrokey's [documentation](https://docs.nitrokey.com/nitrokeys/features) for more details about the features available on your Nitrokey.

Los modelos de Nitrokey pueden ser configurados utilizando la [aplicación de Nitrokey](https://nitrokey.com/download).

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

Excluding the Nitrokey 3, Nitrokeys which support HOTP and TOTP do not have encrypted storage, making them vulnerable to physical attacks.

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
