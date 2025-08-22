---
title: Avertissements
description: A guide for website contributors on creating admonitions.
---

**Admonitions** (or "call-outs") are tools that writers can use to include side content in an article without interrupting the document flow.

<div class="admonition example" markdown>
<p class="admonition-title">Exemple d'avertissement</p>

Ceci est un exemple d'avertissement. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.

</div>

<details class="example" markdown>
<summary>Exemple d'avertissement repliable</summary>

Ceci est un exemple d'avertissement repliable. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.

</details>

## Mise en forme

Pour ajouter un avertissement à une page, vous pouvez utiliser le code suivant :

```markdown title="Admonition"
<div class="admonition TYPE" markdown>
<p class="admonition-title">TITRE</p>

TEXTE JOINT

</div>
```

```markdown title="Collapsible Admonition"
<details class="TYPE" markdown>
<summary>TITRE</summary>

TEXTE JOINT

</details>
```

The `TITLE` must be specified; if you don't want a specific title you can set it to the same text as the `TYPE` (see below) in title case, e.g. `Note`. `TEXTE JOINT` doit être formaté en Markdown.

### Types ordinaires

Remplacez `TYPE` dans les exemples ci-dessus par l'un des éléments suivants :

#### `note`

<div class="admonition note" markdown>
<p class="admonition-title">Note</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `abstract`

<div class="admonition abstract" markdown>
<p class="admonition-title">Abstract</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `info`

<div class="admonition info" markdown>
<p class="admonition-title">Info</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `tip`

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `success`

<div class="admonition success" markdown>
<p class="admonition-title">Success</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `question`

<div class="admonition question" markdown>
<p class="admonition-title">Question</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `warning`

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `failure`

<div class="admonition failure" markdown>
<p class="admonition-title">Failure</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `danger`

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `bug`

<div class="admonition bug" markdown>
<p class="admonition-title">Bug</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `example`

<div class="admonition example" markdown>
<p class="admonition-title">Example</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `quote`

<div class="admonition quote" markdown>
<p class="admonition-title">Quote</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

### Type spéciaux

#### `recommendation`

Ce format est utilisé pour générer des cartes de recommandation. Il manque notamment l'élément `<p class="admonition-title">`.

```markdown title="Recommendation Card"
<div class="admonition recommendation" markdown>

![PhotoPrism logo](assets/img/photo-management/photoprism.svg){ align=right }

**PhotoPrism** is a self-hostable platform for managing photos. It supports album syncing and sharing as well as a variety of other [features](https://photoprism.app/features). It does not include end-to-end encryption, so it's best hosted on a server that you trust and is under your control.

[:octicons-home-16: Homepage](https://photoprism.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://photoprism.app/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://photoprism.app/kb){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/photoprism){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/photoprism)

</details>

</div>
```

<div class="result" markdown>

<div class="admonition recommendation" markdown>

![logo PhotoPrism](../assets/img/photo-management/photoprism.svg){ align=right }

**PhotoPrism** is a self-hostable platform for managing photos. Elle prend en charge la synchronisation et le partage d'albums ainsi qu'une variété d'autres [fonctionnalités](https://photoprism.app/features). It does not include end-to-end encryption, so it's best hosted on a server that you trust and is under your control.

[:octicons-home-16: Homepage](https://photoprism.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://photoprism.app/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://photoprism.app/kb){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/photoprism){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

 - [:simple-github: GitHub](https://github.com/photoprism)

</details>

</div>

</div>

#### `downloads`

This is a special type of collapsible admonition which is used to generate sections containing download links. Il n'est utilisé qu'à l'intérieur des cartes de recommandation, comme le montre l'exemple ci-dessus.

```markdown title="Downloads Section"
<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/android-mail/releases)
- [:fontawesome-brands-windows: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: Web](https://mail.proton.me)

</details>
```

<div class="result" markdown>

<details class="downloads" markdown>
<summary>Downloads</summary>

 - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
 - [:simple-appstore: App Store](https://apps.apple.com/app/id979659905)
 - [:simple-github: GitHub](https://github.com/ProtonMail/android-mail/releases)
 - [:fontawesome-brands-windows: Windows](https://proton.me/mail/bridge#download)
 - [:simple-apple: macOS](https://proton.me/mail/bridge#download)
 - [:simple-linux: Linux](https://proton.me/mail/bridge#download)
 - [:octicons-browser-16: Web](https://mail.proton.me)

</details>

</div>

## Ancien format

Throughout the site, you may see some admonitions formatted like the following examples:

```markdown title="Admonition"
!!! note

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.
```

<div class="result" markdown>

<div class="admonition note" markdown>
<p class="admonition-title">Note</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
massa, nec semper lorem quam in massa.

</div>

</div>

```markdown title="Collapsible Admonition"
??? example "Titre personnalisé"

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.
```

<div class="result" markdown>

<details class="example" markdown>
<summary>Titre personnalisé</summary>

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
massa, nec semper lorem quam in massa.

</details>

</div>

**This format is no longer used going forward** because it is incompatible with newer versions of our translation software at Crowdin. When adding a new page to the site, only the newer, HTML-based format should be used.

Il n'y a pas d'urgence à convertir les avertissements de l'ancien format au nouveau format. Pages currently using this formatting should continue to work, but we will be updating them to use the newer, HTML-based format above over time as we continue to update the site.
