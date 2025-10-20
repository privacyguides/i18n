---
title: Admonitions
description: Un guide pour les contributeurs du site web sur la création d'admonitions.
---

Les **admonitions** (ou "call-outs") sont des outils que les écrivains peuvent utiliser pour inclure du contenu latéral dans un article sans interrompre le flux du document.

<div class="admonition example" markdown>
<p class="admonition-title">Exemple d'admonition</p>

Ceci est un exemple d'admonition. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.

</div>

<details class="example" markdown>
<summary>Exemple d'admonition repliable</summary>

Ceci est un exemple d'admonition repliable. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.

</details>

## Mise en forme

Pour ajouter une admonition à une page, vous pouvez utiliser le code suivant :

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
<p class="admonition-title">Résumé</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `info`

<div class="admonition info" markdown>
<p class="admonition-title">Info</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `tip`

<div class="admonition tip" markdown>
<p class="admonition-title">Conseil</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `success`

<div class="admonition success" markdown>
<p class="admonition-title">Succès</p>

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
<p class="admonition-title">Erreur</p>

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
<p class="admonition-title">Exemple</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `quote`

<div class="admonition quote" markdown>
<p class="admonition-title">Citation</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

### Type spéciaux

#### `recommendation`

Ce format est utilisé pour générer des cartes de recommandation. Il manque notamment l'élément `<p class="admonition-title">`.

```markdown title="Recommendation Card"
<div class="admonition recommendation" markdown>

![Logo de PhotoPrism](assets/img/self-hosting/photoprism.svg){ align=right }

**PhotoPrism** est une plateforme auto-hébergeable de gestion de photos. Elle permet de synchroniser et partager des albums ainsi que beaucoup d'autres [fonctionnalités](https://photoprism.app/features). Il est préférable de l'héberger sur un serveur de confiance que vous contrôlez car elle ne propose pas de chiffrement de bout-en-bout.

[:octicons-home-16: Page d'Accueil](https://photoprism.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://photoprism.app/privacy){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://photoprism.app/kb){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/photoprism){ .card-link title="Code Source" }

</div>
```

<div class="result" markdown>

<div class="admonition recommendation" markdown>

![Logo de PhotoPrism](../assets/img/self-hosting/photoprism.svg){ align=right }

**PhotoPrism** est une plateforme auto-hébergeable de gestion de photos. Elle permet de synchroniser et partager des albums ainsi que beaucoup d'autres [fonctionnalités](https://photoprism.app/features). Il est préférable de l'héberger sur un serveur de confiance que vous contrôlez car elle ne propose pas de chiffrement de bout-en-bout.

[:octicons-home-16: Page d'Accueil](https://photoprism.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://photoprism.app/privacy){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://photoprism.app/kb){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/photoprism){ .card-link title="Code Source" }

</div>

</div>

#### `downloads`

Il s'agit d'un type spécial d'admonition repliable qui est utilisé pour générer des sections contenant des liens de téléchargement. Il n'est utilisé qu'à l'intérieur des cartes de recommandation, comme le montre l'exemple ci-dessus.

```markdown title="Downloads Section"
<details class="downloads" markdown>
<summary>Télécharger</summary>

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
<summary>Télécharger</summary>

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

Dans tout le site, vous pouvez voir quelques admonitions formatées comme les exemples suivants :

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
??? exemple "Titre personnalisé"

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

Il n'y a pas d'urgence à convertir les avertissements de l'ancien format au nouveau format. Les pages qui utilisent actuellement ce format devraient continuer à fonctionner, mais nous les mettrons à jour pour utiliser le nouveau format HTML ci-dessus au fur et à mesure que nous continuerons de mettre le site à jour.
