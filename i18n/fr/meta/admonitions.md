---
title: Avertissements
---

**Les avertissements** (ou conseils) sont un choix que les rédacteurs peuvent utiliser pour inclure un contenu annexe dans un article sans interrompre le flux du document.

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

Le `TITRE` doit être spécifié, si vous ne voulez pas de titre spécifique, vous pouvez mettre le même texte que le `TYPE` (voir ci-dessous) en majuscule, par exemple `Note`. `TEXTE JOINT` doit être formaté en Markdown.

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

![logo PhotoPrism](assets/img/photo-management/photoprism.svg){ align=right }

**PhotoPrism** est une plateforme auto-hébergeable pour la gestion des photos. Elle prend en charge la synchronisation et le partage d'albums ainsi qu'une variété d'autres [fonctionnalités](https://www.photoprism.app/features). Elle ne fournit pas de E2EE, donc il est préférable de l'héberger sur un serveur de confiance et que vous contrôler.

[:octicons-home-16: Page d'accueil](https://www.photoprism.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://www.photoprism.app/privacy){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://www.photoprism.app/kb){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/photoprism){ .card-link title="Code source" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-github: GitHub](https://github.com/photoprism)

</details>

</div>
```

<div class="result" markdown>

<div class="admonition recommendation" markdown>

![logo PhotoPrism](../assets/img/photo-management/photoprism.svg){ align=right }

**PhotoPrism** est une plateforme auto-hébergée pour la gestion des photos. Elle prend en charge la synchronisation et le partage d'albums ainsi qu'une variété d'autres [fonctionnalités](https://www.photoprism.app/features). Elle n'inclut pas l'E2EE, il est donc préférable de l'héberger sur un serveur en lequel vous avez confiance et que vous contrôlez.

[:octicons-home-16: Page d'accueil](https://www.photoprism.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://www.photoprism.app/privacy){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://www.photoprism.app/kb){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/photoprism){ .card-link title="Code source" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-github: GitHub](https://github.com/photoprism)

</details>

</div>

</div>

#### `downloads`

Il s'agit d'un type spécial d'avertissement repliable, utilisé pour générer la section des liens de téléchargement. Il n'est utilisé qu'à l'intérieur des cartes de recommandation, comme le montre l'exemple ci-dessus.

```markdown title="Downloads Section"
<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/apple-store/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/proton-mail-android/releases)
- [:simple-windows11: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: Web](https://mail.proton.me)

</details>
```

<div class="result" markdown>

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/apple-store/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/proton-mail-android/releases)
- [:simple-windows11: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: Web](https://mail.proton.me)

</details>

</div>

## Ancien format

Tout au long du site, vous verrez peut-être des avertissements formatés de manière similaire à ces exemples :

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

**Ce format n'est désormais plus utilisé**, car il est incompatible avec les nouvelles versions de notre logiciel de traduction chez Crowdin. Lors de l'ajout d'une nouvelle page sur le site, seul le format HTML le plus récent doit être utilisé.

Il n'y a pas d'urgence à convertir les avertissements de l'ancien format au nouveau format. Les pages qui utilisent actuellement ce format devraient continuer à fonctionner, mais nous les mettrons à jour pour utiliser le nouveau format HTML ci-dessus au fur et à mesure que nous continuerons à mettre le site à jour.
