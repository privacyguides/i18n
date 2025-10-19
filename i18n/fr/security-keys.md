---
title: Clés de sécurité
icon: material/key-chain
description: Ces clefs de sécurité vous permette d'ajouter une authentification immunisée contre l'hameçonnage (phishing) aux comptes qui sont compatibles.
cover: multi-factor-authentication.webp
---

<small>Protège contre les menaces suivantes :</small>

- [:material-target-account: Attaques Ciblées](basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: Attaques Passives](basics/common-threats.md#security-and-privacy){ .pg-orange }

Une **clef de sécurité** physique ajoute à vos comptes une couche de protection supplémentaire robuste. Comparé aux [applications d'authentification](multi-factor-authentication.md), le protocole de la clef de sécurité [FIDO2](basics/multi-factor-authentication.md#fido-fast-identity-online) est immunisé à l'hameçonnage et ne peux pas être compromise sans posséder physiquement cette clef. Many services support FIDO2/WebAuthn as a multifactor authentication option for securing your account, and some services allow you to use a security key as a strong single-factor authenticator with passwordless authentication.

## Yubico Security Key

<div class="admonition recommendation" markdown>

<figure markdown="span">
  ![Security Key Series by Yubico](assets/img/security-keys/yubico-security-key.webp){ width="315" }
</figure>

The **Yubico Security Key** series is the most cost-effective hardware security key with FIDO Level 2 certification[^1]. It supports FIDO2/WebAuthn and FIDO Universal 2nd Factor (U2F), and works out of the box with most services that support a security key as a second factor, as well as many password managers.

[:octicons-home-16: Homepage](https://yubico.com/products/security-key){ .md-button .md-button--primary }
[:octicons-eye-16:](https://yubico.com/support/terms-conditions/privacy-notice){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.yubico.com){ .card-link title="Documentation" }

</details>

</div>

These keys are available in both USB-C and USB-A variants, and both options support NFC for use with a mobile device as well.

This key provides only basic FIDO2 functionality, but for most people that is all you will need. Some notable features the Security Key series does **not** have include:

- [Yubico Authenticator](https://yubico.com/products/yubico-authenticator)
- CCID Smart Card support (PIV-compatible)
- OpenPGP

If you need any of those features, you should consider their higher-end [YubiKey](#yubikey) series instead.

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

The firmware of Yubico's Security Keys is not updatable. If you want features in newer firmware versions, or if there is a vulnerability in the firmware version you are using, you would need to purchase a new key.

</div>

## YubiKey

<div class="admonition recommendation" markdown>

<figure markdown="span">
  ![YubiKeys](assets/img/security-keys/yubikey.png){ width="400" }
</figure>

The **YubiKey** series from Yubico are among the most popular security keys with FIDO Level 2 Certification[^1]. The **YubiKey 5 Series** has a wide range of features such as FIDO2/WebAuthn and FIDO U2F, [TOTP and HOTP](https://developers.yubico.com/OATH) authentication, [Personal Identity Verification (PIV)](https://developers.yubico.com/PIV), and [OpenPGP](https://developers.yubico.com/PGP).

[:octicons-home-16: Homepage](https://yubico.com/products/yubikey-5-overview){ .md-button .md-button--primary }
[:octicons-eye-16:](https://yubico.com/support/terms-conditions/privacy-notice){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.yubico.com){ .card-link title="Documentation" }

</details>

</div>

The [comparison table](https://yubico.com/store/compare) shows how the YubiKeys compare to each other and to Yubico's [Security Key](#yubico-security-key) series in terms of features and other specifications. One of the benefits of the YubiKey series is that one key can do almost everything you could expect from a hardware security key. We encourage you to take their [quiz](https://yubico.com/quiz) before purchasing in order to make sure you choose the right security key.

YubiKeys can be programmed using the [YubiKey Manager](https://yubico.com/support/download/yubikey-manager) or [YubiKey Personalization Tools](https://yubico.com/support/download/yubikey-personalization-tools). For managing TOTP codes, you can use the [Yubico Authenticator](https://yubico.com/products/yubico-authenticator). All of Yubico's clients are open source.

For models which [support HOTP and TOTP](https://support.yubico.com/hc/articles/360013790319-How-many-accounts-can-I-register-my-YubiKey-with), the secrets are stored encrypted on the key and never exposed to the devices they are plugged into. Once a seed (shared secret) is given to the Yubico Authenticator, it will only give out the six-digit codes, but never the seed. This security model helps limit what an attacker can do if they compromise one of the devices running the Yubico Authenticator and make the YubiKey resistant to a physical attacker.

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

The firmware of YubiKey is not updatable. If you want features in newer firmware versions, or if there is a vulnerability in the firmware version you are using, you would need to purchase a new key.

</div>

## Nitrokey

<div class="admonition recommendation" markdown>

<figure markdown="span">
  ![Nitrokey](assets/img/security-keys/nitrokey.jpg){ width="300" }
</figure>

**Nitrokey** has a cost-effective security key capable of FIDO2/WebAuthn and FIDO U2F called the **Nitrokey Passkey**. For support for features such as PIV, OpenPGP, and TOTP and HOTP authentication, you need to purchase one of their other keys like the **Nitrokey 3**. Currently, only the **Nitrokey 3A Mini** has [FIDO Level 1 Certification](https://nitrokey.com/news/2024/nitrokey-3a-mini-receives-official-fido2-certification).

[:octicons-home-16: Homepage](https://nitrokey.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nitrokey.com/data-privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.nitrokey.com){ .card-link title="Documentation" }

</details>

</div>

The [comparison table](https://nitrokey.com/products/nitrokeys#:~:text=The%20Nitrokey%20Family) shows how the different Nitrokey models compare to each other in terms of features and other specifications. Refer to Nitrokey's [documentation](https://docs.nitrokey.com/nitrokeys/features) for more details about the features available on your Nitrokey.

Nitrokey models can be configured using the [Nitrokey app](https://nitrokey.com/download).

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

Excluding the Nitrokey 3, Nitrokeys which support HOTP and TOTP do not have encrypted storage, making them vulnerable to physical attacks.

</div>

## Critères

**Nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de nos [critères de base](about/criteria.md), nous avons élaboré un ensemble d'exigences clair nous permettant de proposer des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

### Exigences minimales

- Must use high-quality, tamper-resistant hardware security modules.
- Must support the latest FIDO2 specification.
- Must not allow private key extraction.
- Devices which cost over $35 must support handling OpenPGP and S/MIME.

### Critères optimaux

Nos critères optimaux représentent ce que nous aimerions voir d'un projet parfait dans cette catégorie. Nos recommandations peuvent ne pas inclure tout ou partie de ces fonctionnalités, mais celles qui l'inclus peuvent être mieux classées que les autres sur cette page.

- Should be available in USB-C form factor.
- Should be available with NFC.
- Should support TOTP secret storage.
- Should support secure firmware updates.

[^1]: Some governments or other organizations may require a key with Level 2 certification, but most people do not have to worry about this distinction.
