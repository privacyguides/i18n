---
title: Clés de sécurité
icon: material/key-chain
description: Ces clefs de sécurité vous permette d'ajouter aux comptes qui sont compatibles une authentification immunisée contre l'hameçonnage (phishing).
cover: multi-factor-authentication.webp
---

<small>Protège contre les menaces suivantes :</small>

- [:material-target-account: Attaques Ciblées](basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: Attaques Passives](basics/common-threats.md#security-and-privacy){ .pg-orange }

Une **clef de sécurité** physique ajoute à vos comptes une couche de protection robuste supplémentaire. Comparé aux [applications d'authentification](multi-factor-authentication.md), le protocole de la clef de sécurité [FIDO2](basics/multi-factor-authentication.md#fido-fast-identity-online) est immunisé à l'hameçonnage et ne peux pas être compromise sans posséder physiquement cette clef. Beaucoup de services permettent d'utiliser FIDO2/WebAuthn en tant qu'option d'authentification multifactorielle pour protéger vos comptes, et certains services vous permettent d'utiliser une clef de sécurité pour une authentification à seul facteur robuste sans mot de passe.

## Yubico Security Key

<div class="admonition recommendation" markdown>

<figure markdown="span">
  ![Série Security Key de Yubico](assets/img/security-keys/yubico-security-key.webp){ width="315" }
</figure>

La série **Yubico Security Keys** est la clé de sécurité hardware certifiée FIDO Level 2[^1] avec le meilleur rapport qualité prix. Elle est compatible avec FIDO2/WebAuthn et FIDO Universal 2nd Factor (U2F), et fonctionne sans manipulation particulière avec la plupart des services qui permettent d'utiliser une clef de sécurité en tant que deuxième facteur, ainsi qu'avec de nombreux gestionnaires de mots de passe.

[:octicons-home-16: Page d'Accueil](https://yubico.com/products/security-key){ .md-button .md-button--primary }
[:octicons-eye-16:](https://yubico.com/support/terms-conditions/privacy-notice){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://docs.yubico.com){ .card-link title="Documentation" }

</details>

</div>

Ces clefs sont disponibles en format USB-C et USB-A, et les deux options ont également un support NFC pour pouvoir fonctionner avec un smartphone.

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

Ce [tableau comparatif](https://yubico.com/store/compare) vous permet de visualiser les différentes spécificités des produits YubiKeys et [Security Key](#yubico-security-key). Les YubiKey présentent l'avantage de proposer en une seule clef presque toutes les fonctionnalités attendues d'une clef de sécurité physique. Nous vous encourageons à faire leur [questionnaire](https://yubico.com/quiz) avant de faire votre choix.

Les YubiKeys peuvent être programmées en utilisant le [YubiKey Manager](https://yubico.com/support/download/yubikey-manager) ou les [YubiKey Personalization Tools](https://yubico.com/support/download/yubikey-personalization-tools). Pour gérer les codes TOTP, vous pouvez utiliser le [Yubico Authenticator](https://yubico.com/products/yubico-authenticator). Tous les clients Yubico sont open source.

Pour les modèles [qui prennent en charge HOTP et TOTP](https://support.yubico.com/hc/articles/360013790319-How-many-accounts-can-I-register-my-YubiKey-with), les secrets sont chiffrés et stockés sur la clef et ne sont jamais en contact avec les appareils dans lesquels ils sont branchés. Lorsqu'une seed (secret partagé) est partagé au Yubico Authenticator, celui-ci fournira uniquement les codes à six chiffres, mais jamais la seed. Ce modèle de sécurité contribue à limiter les possibilités d'un attaquant qui compromettrai un des appareils utilisant le Yubico Authenticator et rend la clef robuste face à un attaquant physique.

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

Le micrologiciel de la YubiKey ne peut pas être mis à jour. Vous devrez acheter une nouvelle clef si vous souhaitez bénéficier des fonctionnalités des versions les plus récentes, ou si une faille a été trouvée dans la version que vous possédez actuellement.

</div>

## Nitrokey

<div class="admonition recommendation" markdown>

<figure markdown="span">
  ![Nitrokey](assets/img/security-keys/nitrokey.jpg){ width="300" }
</figure>

**Nitrokey** propose la **Nitrokey Passkey**, une clef de sécurité avec un bon rapport qualité prix, compatible avec FIDO2/WebAuthn et FIDO U2F. Si vous souhaitez bénéficier des fonctionnalités telles que la PIV, OpenPGP et l'authentification TOTP et HOTP, vous aurez besoin d'acheter une clef différente, comme la **NitroKey 3**. Actuellement, seule la **NitroKey 3A Mini** est certifiée [FIDO Level 1](https://nitrokey.com/news/2024/nitrokey-3a-mini-receives-official-fido2-certification).

[:octicons-home-16: Page d'Accueil](https://nitrokey.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nitrokey.com/data-privacy-policy){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://docs.nitrokey.com){ .card-link title="Documentation" }

</details>

</div>

Ce [tableau comparatif](https://nitrokey.com/products/nitrokeys#:~:text=The%20Nitrokey%20Family) vous permet de comparer les différentes fonctionnalités et spécificités des modèles Nitrokey. Vous pouvez consulter leur [documentation](https://docs.nitrokey.com/nitrokeys/features) pour plus d'informations.

Les modèles de Nitrokey peuvent être configurés en utilisant [l'application Nitrokey](https://nitrokey.com/download).

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

A l'exception de la Nitrokey 3, les Nitrokeys qui prennent en charge HOTP et TOTP n'ont pas de stockage chiffré, ce qui les rend vulnérables aux attaques physiques.

</div>

## Critères

**Nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de nos [critères de base](about/criteria.md), nous avons élaboré un ensemble d'exigences clair nous permettant de proposer des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de faire votre choix, et de mener vos propres recherches pour vous assurer que celui-ci répond bien à vos besoins.

### Exigences minimales

- Doit utiliser des modules de sécurités hardware de haute qualité résistants aux altérations.
- Doit prendre en charge les dernières spécificités FIDO2.
- Ne doit pas permettre l'extraction de la clé privée.
- Les appareils qui coûtent plus de 35 $ doivent prendre en charge OpenPGP et S/MIME.

### Critères optimaux

Nos critères optimaux représentent ce que nous aimerions voir d'un projet parfait dans cette catégorie. Nos recommandations peuvent ne pas inclure tout ou partie de ces fonctionnalités, mais celles qui l'inclus peuvent être mieux classées que les autres sur cette page.

- Devrait être disponible au format USB-C.
- Devrait proposer le NFC.
- Devrait proposer un stockage des secrets TOTP.
- Devrait permettre les mises à jour de sécurité du micrologiciel.

[^1]: Certaines organisations comme les gouvernements peuvent nécessiter une clef certifiée Level 2, mais la plupart des gens n'en n'ont pas l'utilité.
