---
title: Clés de sécurité
icon: material/key-chain
description: Ces clefs de sécurité vous permette d'ajouter une authentification immunisée contre l'hameçonnage (phishing) aux comptes qui sont compatibles.
cover: multi-factor-authentication.webp
---

<small>Protège contre les menaces suivantes :</small>

- [:material-target-account: Attaques Ciblées](basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: Attaques Passives](basics/common-threats.md#security-and-privacy){ .pg-orange }

Une **clef de sécurité** physique ajoute à vos comptes une couche de protection supplémentaire robuste. Comparé aux [applications d'authentification](multi-factor-authentication.md), le protocole de la clef de sécurité [FIDO2](basics/multi-factor-authentication.md#fido-fast-identity-online) est immunisé à l'hameçonnage et ne peux pas être compromise sans posséder physiquement cette clef. Beaucoup de services permettent d'utiliser FIDO2/WebAuthn en tant qu'option d'authentification multifactorielle pour protéger vos comptes, et certains services vous permettent d'utiliser une clef de sécurité d'authentification robuste à seul facteur pour une authentification sans mot de passe.

## Yubico Security Key

<div class="admonition recommendation" markdown>

<figure markdown="span">
  ![Security Key Series de Yubico](assets/img/security-keys/yubico-security-key.webp){ width="315" }
</figure>

La série **Yubico Security Keys** est la clé de sécurité hardware certifiée FIDO Level 2[^1] avec le meilleur rapport qualité prix. Elle est compatible avec FIDO2/WebAuthn et FIDO Universal 2nd Factor (U2F), et fonctionne sans manipulation particulière avec la plupart des services qui permettent d'utiliser une clef de sécurité en tant que deuxième facteur, ainsi qu'avec de nombreux gestionnaires de mots de passe.

[:octicons-home-16: Page d'Accueil](https://yubico.com/products/security-key){ .md-button .md-button--primary }
[:octicons-eye-16:](https://yubico.com/support/terms-conditions/privacy-notice){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://docs.yubico.com){ .card-link title="Documentation" }

</details>

</div>

La clef possède seulement des fonctionnalités FIDO2 basique, mais cela est suffisant pour la plupart des gens.

La clef possède seulement des fonctionnalités FIDO2 basique, mais cela est suffisant pour la plupart des gens. Fonctionnalités notables qui ne sont **pas** incluses dans la série Security Key :

- [Yubico Authentificator](https://yubico.com/products/yubico-authenticator)
- Prise en charge des cartes à puces CCID (compatible PIV)
- OpenPGP

Si vous avez besoin de ces fonctionnalités, vous devriez plutôt vous tourner vers leur série haut de gamme [YubiKey](#yubikey).

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

Le firmware des Security Keys de Yubico ne peut pas être mis à jour. Vous devrez acheter une nouvelle clef si vous souhaitez bénéficier des fonctionnalités des versions les plus récentes, ou si une faille a été trouvée dans la version que vous possédez actuellement.

</div>

## YubiKey

<div class="admonition recommendation" markdown>

<figure markdown="span">
  ![YubiKeys](assets/img/security-keys/yubikey.png){ width="400" }
</figure>

La série **YubiKey** de Yubico fait partie des clefs de sécurité certifiée FIDO Level 2 les plus populaires[^1]. La **YubiKey 5 Series** propose un grand nombre de fonctionnalités comme FIDO/WebAuthn et FIDO U2F, l'authentification [TOTP et HOTP](https://developers.yubico.com/OATH), la [Vérification d'Identité Personnelle (Personal Identity Verification, ou PIV)](https://developers.yubico.com/PIV) et [OpenPGP](https://developers.yubico.com/PGP).

[:octicons-home-16: Page d'Accueil](https://yubico.com/products/yubikey-5-overview){ .md-button .md-button--primary }
[:octicons-eye-16:](https://yubico.com/support/terms-conditions/privacy-notice){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://docs.yubico.com){ .card-link title="Documentation" }

</details>

</div>

Le [tableau comparatif](https://yubico.com/store/compare) vous permet de visualiser les différentes spécificités des produits YubiKeys et [Security Key](#yubico-security-key). Les YubiKey présentent l'avantage de proposer en une seule clef presque toutes les fonctionnalités attendues d'une clef de sécurité physique. We encourage you to take their [quiz](https://yubico.com/quiz) before purchasing in order to make sure you choose the right security key.

YubiKeys can be programmed using the [YubiKey Manager](https://yubico.com/support/download/yubikey-manager) or [YubiKey Personalization Tools](https://yubico.com/support/download/yubikey-personalization-tools). For managing TOTP codes, you can use the [Yubico Authenticator](https://yubico.com/products/yubico-authenticator). All of Yubico's clients are open source.

For models which [support HOTP and TOTP](https://support.yubico.com/hc/articles/360013790319-How-many-accounts-can-I-register-my-YubiKey-with), the secrets are stored encrypted on the key and never exposed to the devices they are plugged into. Once a seed (shared secret) is given to the Yubico Authenticator, it will only give out the six-digit codes, but never the seed. This security model helps limit what an attacker can do if they compromise one of the devices running the Yubico Authenticator and make the YubiKey resistant to a physical attacker.

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

The firmware of YubiKey is not updatable. Vous devrez acheter une nouvelle clef si vous souhaitez bénéficier des fonctionnalités des versions les plus récentes, ou si une faille a été trouvée dans la version que vous possédez actuellement.

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
