---
title: Moniti
description: A guide for website contributors on creating admonitions.
---

**Admonitions** (or "call-outs") are tools that writers can use to include side content in an article without interrupting the document flow.

<div class="admonition example" markdown>
<p class="admonition-title">Esempio di monito</p>

Questo è un esempio di monito. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.

</div>

<details class="example" markdown>
<summary>Esempio di monito a scomparsa</summary>

Questo è un esempio di monito a scomparsa. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.

</details>

## Formattazione

Per aggiungere un monito a una pagina, si può utilizzare il seguente codice:

```markdown title="Admonition"
<div class="admonition TYPE" markdown>
<p class="admonition-title">TITOLO</p>

TESTO ALLEGATO

</div>
```

```markdown title="Collapsible Admonition"
<details class="TYPE" markdown>
<summary>TITOLO</summary>

TESTO ALLEGATO

</details>
```

The `TITLE` must be specified; if you don't want a specific title you can set it to the same text as the `TYPE` (see below) in title case, e.g. `Note`. Il \`TESTO ALLEGATO' deve essere formattato in Markdown.

### Tipi regolari

Negli esempi precedenti, sostituisci `TIPO` con uno dei seguenti:

#### `note`

<div class="admonition note" markdown>
<p class="admonition-title">Nota</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `abstract`

<div class="admonition abstract" markdown>
<p class="admonition-title">Sommario</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `info`

<div class="admonition info" markdown>
<p class="admonition-title">Info</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `tip`

<div class="admonition tip" markdown>
<p class="admonition-title">Suggerimento</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `success`

<div class="admonition success" markdown>
<p class="admonition-title">Successo</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `question`

<div class="admonition question" markdown>
<p class="admonition-title">Domanda</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `warning`

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `failure`

<div class="admonition failure" markdown>
<p class="admonition-title">Fallimento</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `danger`

<div class="admonition danger" markdown>
<p class="admonition-title">Attenzione</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `bug`

<div class="admonition bug" markdown>
<p class="admonition-title">Bug</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `example`

<div class="admonition example" markdown>
<p class="admonition-title">Esempio</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `quote`

<div class="admonition quote" markdown>
<p class="admonition-title">Citazione</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

### Tipi speciali

#### `recommendation`

Questo formato viene utilizzato per generare schede di raccomandazione. In particolare, manca l'elemento `<p class="admonition-title">`.

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

![Logo PhotoPrism](../assets/img/photo-management/photoprism.svg){ align=right }

**PhotoPrism** is a self-hostable platform for managing photos. Supporta la sincronizzazione e condivisione degli album, nonché una varietà di altre [funzionalità](https://photoprism.app/features). It does not include end-to-end encryption, so it's best hosted on a server that you trust and is under your control.

[:octicons-home-16: Homepage](https://photoprism.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://photoprism.app/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://photoprism.app/kb){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/photoprism){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-github: GitHub](https://github.com/photoprism)

</details>

</div>

</div>

#### `downloads`

This is a special type of collapsible admonition which is used to generate sections containing download links. Viene utilizzato solo all'interno delle schede di raccomandazione, come mostrato nell'esempio precedente.

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
<summary>Scarica</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/android-mail/releases)
- [:fontawesome-brands-windows: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: Web](https://mail.proton.me)

</details>

</div>

## Vecchio formato

Throughout the site, you may see some admonitions formatted like the following examples:

```markdown title="Admonition"
!!! note

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.
```

<div class="result" markdown>

<div class="admonition note" markdown>
<p class="admonition-title">Nota</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
massa, nec semper lorem quam in massa.

</div>

</div>

```markdown title="Collapsible Admonition"
??? example "Titolo personalizzato"

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.
```

<div class="result" markdown>

<details class="example" markdown>
<summary>Titolo personalizzato</summary>

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
massa, nec semper lorem quam in massa.

</details>

</div>

**This format is no longer used going forward** because it is incompatible with newer versions of our translation software at Crowdin. When adding a new page to the site, only the newer, HTML-based format should be used.

Non c'è fretta di convertire i moniti con il vecchio formato in quello nuovo. Pages currently using this formatting should continue to work, but we will be updating them to use the newer, HTML-based format above over time as we continue to update the site.
