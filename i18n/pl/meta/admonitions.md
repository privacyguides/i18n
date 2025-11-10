---
title: Objaśnienia
description: Przewodnik dla współtwórców tej strony na temat tworzenia objaśnień.
---

Objaśnienia (ang. _admonitions_ lub _call-outs_) to narzędzie, z którego redaktorzy mogą korzystać, aby dodać treści poboczne do artykułu bez przerywania głównego toku dokumentu.

<div class="admonition example" markdown>
<p class="admonition-title">Przykładowe objaśnienie</p>

To jest przykład objaśnienia. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.

</div>

<details class="example" markdown>
<summary>Przykładowe zwijane objaśnienie</summary>

To jest przykład zwijanego objaśnienia. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.

</details>

## Formatowanie

Aby dodać objaśnienie do strony, możesz użyć poniższego kodu:

```markdown title="Admonition"
<div class="admonition TYPE" markdown>
<p class="admonition-title">TYTUŁ</p>

ZAWARTA TREŚĆ

</div>
```

```markdown title="Collapsible Admonition"
<details class="TYPE" markdown>
<summary>TYTUŁ</summary>

ZAWARTA TREŚĆ

</details>
```

Pole `TYTUŁ` jest obowiązkowe; jeśli nie chcesz określać konkretnego tytułu, możesz ustawić je na taki sam tekst jak `TYPE` (patrz poniżej), zapisany wielką literą na początku, np. `Uwaga`. `ZAWARTA TREŚĆ` powinna być sformatowana w Markdown.

### Typy standardowe

Zastąp `TYPE` w powyższych przykładach jednym z poniższych:

#### `note`

<div class="admonition note" markdown>
<p class="admonition-title">Uwaga</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `abstract`

<div class="admonition abstract" markdown>
<p class="admonition-title">Streszczenie</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `info`

<div class="admonition info" markdown>
<p class="admonition-title">Informacja</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `tip`

<div class="admonition tip" markdown>
<p class="admonition-title">Porada</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `success`

<div class="admonition success" markdown>
<p class="admonition-title">Sukces</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `question`

<div class="admonition question" markdown>
<p class="admonition-title">Pytanie</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `warning`

<div class="admonition warning" markdown>
<p class="admonition-title">Ostrzeżenie</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `failure`

<div class="admonition failure" markdown>
<p class="admonition-title">Niepowodzenie</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `danger`

<div class="admonition danger" markdown>
<p class="admonition-title">Zagrożenie</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `bug`

<div class="admonition bug" markdown>
<p class="admonition-title">Błąd</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `example`

<div class="admonition example" markdown>
<p class="admonition-title">Przykład</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

#### `quote`

<div class="admonition quote" markdown>
<p class="admonition-title">Cytat</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit.

</div>

### Typy specjalne

#### `recommendation`

Ten format służy do generowania kart z zaleceniami. Wyróżnia się tym, że nie zawiera elementu `<p class="admonition-title">`.

```markdown title="Recommendation Card"
<div class="admonition recommendation" markdown>

![Logo PhotoPrism](assets/img/self-hosting/photoprism.svg){ align=right }

**PhotoPrism** to platforma do samodzielnego hostowania i zarządzania zdjęciami. Obsługuje synchronizację i udostępnianie albumów oraz szereg innych [funkcji](https://photoprism.app/features). Nie oferuje jednak szyfrowania typu end-to-end, dlatego najlepiej hostować ją na zaufanym serwerze, nad którym masz pełną kontrolę.

[:octicons-home-16: Strona główna](https://photoprism.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://photoprism.app/privacy){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://photoprism.app/kb){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/photoprism){ .card-link title="Kod źródłowy" }

</div>
```

<div class="result" markdown>

<div class="admonition recommendation" markdown>

![Logo PhotoPrism](../assets/img/self-hosting/photoprism.svg){ align=right }

**PhotoPrism** to platforma do samodzielnego hostowania i zarządzania zdjęciami. Obsługuje synchronizację i udostępnianie albumów oraz szereg innych [funkcji](https://photoprism.app/features). Nie oferuje jednak szyfrowania typu end-to-end, dlatego najlepiej hostować ją na zaufanym serwerze, nad którym masz pełną kontrolę.

[:octicons-home-16: Strona główna](https://photoprism.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://photoprism.app/privacy){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://photoprism.app/kb){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/photoprism){ .card-link title="Kod źródłowy" }

</div>

</div>

#### `downloads`

Jest to specjalny typ zwijanego objaśnienia używanego do generowania sekcji zawierających linki do pobrania. Występuje wyłącznie wewnątrz kart z zaleceniami, jak pokazano w powyższym przykładzie.

```markdown title="Downloads Section"
<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/android-mail/releases)
- [:fontawesome-brands-windows: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: W przeglądarce](https://mail.proton.me)

</details>
```

<div class="result" markdown>

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/android-mail/releases)
- [:fontawesome-brands-windows: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: W przeglądarce](https://mail.proton.me)

</details>

</div>

## Stary format

Na stronie możesz natrafić na objaśnienia sformatowane na jeden z poniższych sposobów:

```markdown title="Admonition"
!!! note

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.
```

<div class="result" markdown>

<div class="admonition note" markdown>
<p class="admonition-title">Uwaga</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
massa, nec semper lorem quam in massa.

</div>

</div>

```markdown title="Collapsible Admonition"
??? example "Niestandardowy tytuł"

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.
```

<div class="result" markdown>

<details class="example" markdown>
<summary>Niestandardowy tytuł</summary>

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
massa, nec semper lorem quam in massa.

</details>

</div>

**Ten format nie jest już używany**, ponieważ jest niekompatybilny z nowszymi wersjami naszego oprogramowania tłumaczeniowego w Crowdin. Podczas dodawania nowej strony należy używać wyłącznie nowszego formatu opartego na HTML.

Nie ma jednak potrzeby natychmiastowej konwersji istniejących objaśnień do nowego formatu. Strony korzystające ze starego zapisu będą nadal działać, ale z czasem będziemy je stopniowo aktualizować do nowego, opartego na HTML formatu, w miarę wprowadzania kolejnych zmian na stronie.
