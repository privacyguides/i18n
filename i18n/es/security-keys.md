---
title: Llaves de seguridad
icon: material/key-chain
description: Estas herramientas te ayudan a proteger tus cuentas de Internet con la autenticación multifactor sin enviar tus secretos a terceros.
cover: multi-factor-authentication.webp
---

<small>Protege contra las siguientes amenazas:</small>

- [:material-target-account: Ataques dirigidos](basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: Ataques pasivos](basics/common-threats.md#security-and-privacy){ .pg-orange }

Una **llave de seguridad** física añade una capa fuerte de protección a tus cuentas en línea. A comparación con las [aplicaciones de autenticación](multi-factor-authentication.md), el protocolo de llave de seguridad FIDO2 es innume al phishing y no puede ser comprometido sin tener la llave física. Muchos servicios son compatibles con FIDO2/WebAuthn como una opción de autenticación multifactor para asegurar tu cuenta, y algunos servicios te permiten usar una llave de seguridad como un autenticador fuerte de factor único con autenticación sin contraseña.

## Llave de seguridad Yubico

<div class="admonition recommendation" markdown>

<figure markdown="span">  ![Serie de llaves de seguridad por Yubico](assets/img/security-keys/yubico-security-key.webp){ width="315" }</figure>

La serie de **llave de seguridad de Yubico** es la llave de seguridad física más rentable con la certificación FIDO Nivel 2. Esta es compatible con FIDO2/WebAuthn y FIDO U2F, y funciona con muchos servicios compatibles con una llave de seguridad como segundo factor, así como con muchos gestores de contraseñas.

[:octicons-home-16: Página principal](https://yubico.com/products/security-key){ .md-button .md-button--primary }
[:octicons-eye-16:](https://yubico.com/support/terms-conditions/privacy-notice){ .card-link title="Política de privacidad" }
[:octicons-info-16:](https://docs.yubico.com){ .card-link title=Documentación}

</details>

</div>

Estas llaves están disponibles en variantes USB-C y USB-A, y ambas opciones soportan NFC para ser utilizadas con un dispositivo móvil.

Esta llave proporciona únicamente la funcionalidad básica de FIDO2, pero para la mayoría de las personas esto es todo lo que necesitan. Algunas características notables que la serie de llave de seguridad **no** incluye son:

- [Autenticador Yubico](https://yubico.com/products/yubico-authenticator)
- Soporte para la tarjeta inteligente CCID (compatible con PIV)
- OpenPGP

If you need any of those features, you should consider their higher-end [YubiKey](#yubikey) of products instead.

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

The firmware of Yubico's Security Keys is not updatable. If you want features in newer firmware versions, or if there is a vulnerability in the firmware version you are using, you would need to purchase a new key.

</div>

## YubiKey

<div class="admonition recommendation" markdown>

<figure markdown="span">
  ![YubiKeys](assets/img/security-keys/yubikey.png){ width="400" }
</figure>

The **YubiKey** series from Yubico are among the most popular security keys. The YubiKey 5 Series has a wide range of features such as: [Universal 2nd Factor (U2F)](https://en.wikipedia.org/wiki/Universal_2nd_Factor), [FIDO2 and WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online), [Yubico OTP](basics/multi-factor-authentication.md#yubico-otp), [Personal Identity Verification (PIV)](https://developers.yubico.com/PIV), [OpenPGP](https://developers.yubico.com/PGP), [TOTP and HOTP](https://developers.yubico.com/OATH) authentication.

[:octicons-home-16: Homepage](https://yubico.com/products/yubikey-5-overview){ .md-button .md-button--primary }
[:octicons-eye-16:](https://yubico.com/support/terms-conditions/privacy-notice){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.yubico.com){ .card-link title=Documentation}

</details>

</div>

The [comparison table](https://yubico.com/store/compare) shows the features and how the YubiKeys compare to each other and to Yubico's [Security Key](#yubico-security-key) series. One of the benefits of the YubiKey series is that one key can do almost everything you could expect from a hardware security key. We encourage you to take their [quiz](https://yubico.com/quiz) before purchasing in order to make sure you make the right choice.

The Yubikey 5 series has FIDO Level 1 certification, which is the most common. However, some governments or other organizations may require a key with Level 2 certification, in which case you'll have to purchase a [Yubikey 5 **FIPS** series](https://yubico.com/products/yubikey-fips) key, or a [Yubico Security Key](#yubico-security-key). Most people do not have to worry about this distinction.

YubiKeys can be programmed using the [YubiKey Manager](https://yubico.com/support/download/yubikey-manager) or [YubiKey Personalization Tools](https://yubico.com/support/download/yubikey-personalization-tools). For managing TOTP codes, you can use the [Yubico Authenticator](https://yubico.com/products/yubico-authenticator). All of Yubico's clients are open source.

For models which support HOTP and TOTP, there are 2 slots in the OTP interface which could be used for HOTP and 32 slots to store TOTP secrets. These secrets are stored encrypted on the key and never expose them to the devices they are plugged into. Once a seed (shared secret) is given to the Yubico Authenticator, it will only give out the six-digit codes, but never the seed. This security model helps limit what an attacker can do if they compromise one of the devices running the Yubico Authenticator and make the YubiKey resistant to a physical attacker.

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

The firmware of YubiKey is not updatable. If you want features in newer firmware versions, or if there is a vulnerability in the firmware version you are using, you would need to purchase a new key.

</div>

## Nitrokey

<div class="admonition recommendation" markdown>

<figure markdown="span">
  ![Nitrokey](assets/img/security-keys/nitrokey.jpg){ width="300" }
</figure>

**Nitrokey** has a security key capable of [FIDO2 and WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online) called the **Nitrokey FIDO2**. For PGP support, you need to purchase one of their other keys such as the **Nitrokey Start**, **Nitrokey Pro 2** or the **Nitrokey Storage 2**.

[:octicons-home-16: Homepage](https://nitrokey.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nitrokey.com/data-privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.nitrokey.com){ .card-link title=Documentation}

</details>

</div>

The [comparison table](https://nitrokey.com/#comparison) shows the features and how the Nitrokey models compare. The **Nitrokey 3** listed will have a combined feature set.

Nitrokey models can be configured using the [Nitrokey app](https://nitrokey.com/download).

For the models which support HOTP and TOTP, there are 3 slots for HOTP and 15 for TOTP. Some Nitrokeys can act as a password manager. They can store 16 different credentials and encrypt them using the same password as the OpenPGP interface.

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

While Nitrokeys do not release the HOTP/TOTP secrets to the device they are plugged into, the HOTP and TOTP storage is **not** encrypted and is vulnerable to physical attacks. If you are looking to store HOTP or TOTP secrets, we highly recommend that you use a YubiKey instead.

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

Resetting the OpenPGP interface on a Nitrokey will also make the password database [inaccessible](https://docs.nitrokey.com/pro/linux/factory-reset).

</div>

## Criterios

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. Sugerimos que te familiarices con esta lista, antes de decidir utilizar un proyecto y realizar tu propia investigación para asegurarte de que es la elección ideal para ti.

### Requisitos Mínimos

- Must use high quality, tamper resistant hardware security modules.
- Must support the latest FIDO2 specification.
- Must not allow private key extraction.
- Devices which cost over $35 must support handling OpenPGP and S/MIME.

### Mejor Caso

Nuestro criterio del mejor caso representa lo que nos gustaría ver del proyecto perfecto en esta categoría. Es posible que nuestras recomendaciones no incluyan todas o algunas de estas funciones, pero las que sí las incluyan pueden estar mejor clasificadas que otras en esta página.

- Should be available in USB-C form-factor.
- Should be available with NFC.
- Should support TOTP secret storage.
- Should support secure firmware updates.
