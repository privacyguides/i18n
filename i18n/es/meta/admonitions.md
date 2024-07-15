---
title: Advertencias
---

**Las advertencias** (o "llamadas de atención") son una opción que los redactores pueden utilizar para incluir contenidos secundarios en un artículo sin interrumpir el flujo del documento.

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

Debe especificarse el `TÍTULO`, si no deseas un título específico puedes establecerlo con el mismo texto que el `TIPO` (véase más abajo) en el caso del título, por ejemplo, `Nota`. El "TEXTO INCLUIDO" debe tener formato Markdown.

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

**PhotoPrism** es una plataforma autoalojable para la gestión de fotos. Admite la sincronización y compartición de álbumes, así como una variedad de otras [características](https://www.photoprism.app/features). No incluye E2EE, por lo que es mejor alojarlo en un servidor en el que confíes y que esté bajo tu control.

[:octicons-home-16: Página Principal](https://photoprism.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://photoprism.app/privacy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://photoprism.app/kb){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/photoprism){ .card-link title="Código Fuente" }

<details class="downloads" markdown>
<summary>Downloads "Descargas</summary>

- [:simple-github: GitHub](https://github.com/photoprism)

</details>

</div>
```

<div class="result" markdown>

<div class="admonition recommendation" markdown>

![PhotoPrism logo](../assets/img/photo-management/photoprism.svg){ align=right }

**PhotoPrism** es una plataforma autoalojable para la gestión de fotos. Permite sincronizar y compartir álbumes y tiene otras muchas [funciones](https://photoprism.app/features). No incluye E2EE, por lo que es mejor alojarlo en un servidor en el que confíes y que esté bajo tu control.

[:octicons-home-16: Página Principal](https://photoprism.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://photoprism.app/privacy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://photoprism.app/kb){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/photoprism){ .card-link title="Código Fuente" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-github: GitHub](https://github.com/photoprism)

</details>

</div>

</div>

#### `downloads`

Se trata de un tipo especial de advertencia plegable, utilizada para generar la sección de enlaces de descarga. Solo se utiliza dentro de las tarjetas de recomendación, como se muestra en el ejemplo anterior.

```markdown title="Downloads Section"
<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/proton-mail-android/releases)
- [:fontawesome-brands-windows: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: Web](https://mail.proton.me)

</details>
```

<div class="result" markdown>

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/proton-mail-android/releases)
- [:fontawesome-brands-windows: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: Web](https://mail.proton.me)

</details>

</div>

## Old Format

Throughout the site, you may see some admonitions formatted similarly to these examples:

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

**Este formato ya no se utiliza en adelante,** porque es incompatible con las nuevas versiones de nuestro software de traducción en Crowdin. Al añadir una nueva página al sitio, solo debe utilizarse el nuevo formato basado en HTML.

No hay prisa por convertir las advertencias con el formato antiguo al nuevo. Las páginas que actualmente utilizan este formato deberían seguir funcionando, pero las iremos actualizando para que utilicen el nuevo formato basado en HTML a medida que sigamos actualizando el sitio.
