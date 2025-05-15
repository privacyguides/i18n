---
title: Advertencias
description: Una guía para colaboradores del sitio web sobre la creación de advertencias.
---

**Admonitions** (or "call-outs") are tools that writers can use to include side content in an article without interrupting the document flow.

<div class="admonition example" markdown>
<p class="admonition-title">Ejemplo de Advertencia</p>

Este es un ejemplo de una advertencia. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.

</div>

<details class="example" markdown>
<summary>Ejemplo de Advertencia Plegable</summary>

Este es un ejemplo de advertencia plegable. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.

</details>

## Formato

Para añadir una advertencia a una página, puedes utilizar el siguiente código:

```markdown title="Admonition"
<div class="admonition TYPE" markdown>
<p class="admonition-title">TÍTULO</p>

TEXTO INCLUIDO

</div>
```

```markdown title="Collapsible Admonition"
<details class="TYPE" markdown>
<summary>TÍTULO</summary>

TEXTO INCLUIDO

</details>
```

The `TITLE` must be specified; if you don't want a specific title you can set it to the same text as the `TYPE` (see below) in title case, e.g. `Note`. El "TEXTO INCLUIDO" debe tener formato Markdown.

### Tipos habituales

Reemplaza `TYPE` en los ejemplos anteriores con uno de los siguientes:

#### `note`

<div class="admonition note" markdown>
<p class="admonition-title">Nota</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `abstract`

<div class="admonition abstract" markdown>
<p class="admonition-title">Resumen</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `info`

<div class="admonition info" markdown>
<p class="admonition-title">Detalles</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `tip`

<div class="admonition tip" markdown>
<p class="admonition-title">Consejo</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `success`

<div class="admonition success" markdown>
<p class="admonition-title">Éxito</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `question`

<div class="admonition question" markdown>
<p class="admonition-title">Pregunta</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `warning`

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `failure`

<div class="admonition failure" markdown>
<p class="admonition-title">Fallo</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `danger`

<div class="admonition danger" markdown>
<p class="admonition-title">Peligro</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `bug`

<div class="admonition bug" markdown>
<p class="admonition-title">Bug</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `example`

<div class="admonition example" markdown>
<p class="admonition-title">Ejemplo</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `quote`

<div class="admonition quote" markdown>
<p class="admonition-title">Cita</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

### Tipos Especiales

#### `recommendation`

Este formato se utiliza para generar tarjetas de recomendación. En particular, falta el elemento `<p class="admonition-title">`.

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

![PhotoPrism logo](../assets/img/photo-management/photoprism.svg){ align=right }

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

</div>

#### `downloads`

This is a special type of collapsible admonition which is used to generate sections containing download links. Solo se utiliza dentro de las tarjetas de recomendación, como se muestra en el ejemplo anterior.

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

## Old Format

Throughout the site, you may see some admonitions formatted like the following examples:

```markdown title="Admonition"
!!! nota

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
??? ejemplo "Título Personalizado"

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.
```

<div class="result" markdown>

<details class="example" markdown>
<summary>Título Personalizado</summary>

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
massa, nec semper lorem quam in massa.

</details>

</div>

**This format is no longer used going forward** because it is incompatible with newer versions of our translation software at Crowdin. When adding a new page to the site, only the newer, HTML-based format should be used.

No hay prisa por convertir las advertencias con el formato antiguo al nuevo. Pages currently using this formatting should continue to work, but we will be updating them to use the newer, HTML-based format above over time as we continue to update the site.
