---
meta_title: "Usuwanie danych osobowych za pomocą narzędzi do usuwania metadanych i redakcji danych – Privacy Guides"
title: "Redakcja danych i metadanych"
icon: material/tag-remove
description: Skorzystaj z tych narzędzi, aby usunąć metadane, takie jak lokalizacja GPS i inne informacje identyfikujące, ze zdjęć i plików, które udostępniasz.
cover: data-redaction.webp
---

<small>Chroni przed następującymi zagrożeniami:</small>

- [:material-account-search: Ekspozycja publiczna](basics/common-threats.md#limiting-public-information ""){.pg-green}

Udostępniając pliki, pamiętaj o usunięciu powiązanych metadanych. Pliki graficzne zazwyczaj zawierają dane [Exif](https://pl.wikipedia.org/wiki/Exchangeable_Image_File_Format). Zdjęcia czasem zawierają nawet współrzędne GPS w metadanych pliku.

<div class="admonition warning" markdown>
<p class="admonition-title">Ostrzeżenie</p>

Nigdy nie należy używać efektu rozmycia do ukrycia [tekstu na obrazach](https://bishopfox.com/blog/unredacter-tool-never-pixelation). Jeśli chcesz zredagować tekst na zdjęciu, zakryj tekst prostokątnym polem.

</div>

## MAT2

<div class="admonition recommendation" markdown>

![Logo MAT2](assets/img/data-redaction/mat2.svg){ align=right }

**MAT2** to darmowe, wieloplatformowe oprogramowanie umożliwiające usuwanie metadanych z plików graficznych, audio, torrentów i dokumentów. Oferuje zarówno narzędzie wiersza poleceń, jak i interfejs graficzny za pośrednictwem rozszerzenia dla [Dolphin](https://github.com/jvoisin/mat2/tree/master/dolphin), domyślnego menedżera plików [KDE](https://kde.org).

[:octicons-repo-16: Repozytorium](https://github.com/jvoisin/mat2#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/jvoisin/mat2#how-to-use-mat2){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/jvoisin/mat2){ .card-link title="Kod źródłowy" }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:fontawesome-brands-windows: Windows](https://pypi.org/project/mat2)
- [:simple-apple: macOS](https://github.com/jvoisin/mat2#requirements-setup-on-macos-os-x-using-homebrew)
- [:simple-linux: Linux](https://pypi.org/project/mat2)
- [:octicons-browser-16: W przeglądarce](https://github.com/jvoisin/mat2#web-interface)

</details>

</div>

## ExifEraser (Android)

<div class="admonition recommendation" markdown>

![Logo ExifEraser](assets/img/data-redaction/exiferaser.svg){ align=right }

**ExifEraser** to nowoczesna aplikacja na Androida, która usuwa metadane obrazów bez konieczności nadawania jej specjalnych uprawnień.

Obecnie obsługuje pliki w formacie JPEG, PNG i WebP.

[:octicons-repo-16: Repozytorium](https://github.com/Tommy-Geenexus/exif-eraser#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/Tommy-Geenexus/exif-eraser#description){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/Tommy-Geenexus/exif-eraser){ .card-link title="Kod źródłowy" }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.none.tom.exiferaser)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/com.none.tom.exiferaser)
- [:simple-github: GitHub](https://github.com/Tommy-Geenexus/exif-eraser/releases)

</details>

</div>

Usuwane metadane zależą od formatu pliku obrazu:

- **JPEG**: profil ICC, Exif, zasoby obrazu Photoshopa oraz metadane XMP/ExtendedXMP zostaną usunięte, jeśli istnieją.
- **PNG**: profil ICC, Exif i metadane XMP zostaną usunięte, jeśli istnieją.
- **WebP**: profil ICC, Exif i metadane XMP zostaną usunięte, jeśli istnieją.

Po przetworzeniu zdjęć ExifEraser generuje szczegółowy raport pokazujący, co dokładnie zostało usunięte z każdego obrazu.

Aplikacja oferuje kilka sposobów usuwania metadanych z obrazów. Mianowicie:

- Można udostępnić obraz z innej aplikacji do ExifEraser.
- W samej aplikacji można wybrać pojedyncze zdjęcie, wiele zdjęć jednocześnie lub cały katalog.
- Dostępna jest opcja „Aparat”, która wykorzystuje systemową aplikację aparatu do wykonania zdjęcia, a następnie usuwa z niego metadane.
- Umożliwia przeciąganie zdjęć z innej aplikacji do ExifEraser, gdy obie są otwarte w trybie podzielonego ekranu.
- Na koniec pozwala wkleić obraz ze schowka.

## Skróty (iOS i macOS)

W systemiach iOS i macOS możesz usunąć metadane obrazów bez korzystania z aplikacji firm trzecich, tworząc [**skrót**](https://apps.apple.com/app/id915249334) do tego celu. Oto przykładowy skrót, który możesz pobrać i użyć bez zmian:

[:material-tag-minus: Wyczyść metadane obrazu](https://icloud.com/shortcuts/fb774ddb7b5b4296871776c67ac0fff9 ""){.md-button}

Możesz też użyć go jako wzoru do własnego skrótu — upewnij się tylko, że opcja **Zachowaj metadane** w akcji **Konwertuj** nie jest zaznaczona. Po dodaniu skrótu będzie on dostępny w arkuszu udostępniania, który pojawia się po wybraniu przycisku :octicons-share-24: Udostępnij. Można zaznaczyć wiele obrazów i uruchomić skrót, aby usunąć metadane ze wszystkich naraz.

Skrót ten usuwa metadane takie jak lokalizacja, model urządzenia, model obiektywu i inne informacje z aparatu. Ustawia również datę utworzenia obrazu na czas użycia skrótu.

## ExifTool (CLI)

<div class="admonition recommendation" markdown>

![Logo ExifTool](assets/img/data-redaction/exiftool.png){ align=right }

**ExifTool** to oryginalna biblioteka Perla oraz aplikacja wiersza poleceń do odczytu, zapisu i edycji metadanych (Exif, IPTC, XMP i innych) w wielu formatach plików (JPEG, TIFF, PNG, PDF, RAW i innych).

Często występuje on jako komponent innych narzędzi do usuwania Exif i jest dostępny w repozytoriach większości dystrybucji Linuksa.

[:octicons-home-16: Strona główna](https://exiftool.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://exiftool.org/faq.html){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/exiftool/exiftool){ .card-link title="Kod źródłowy" }
[:octicons-heart-16:](https://exiftool.org/#donate){ .card-link title="Wesprzyj" }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:fontawesome-brands-windows: Windows](https://exiftool.org)
- [:simple-apple: macOS](https://exiftool.org)
- [:simple-linux: Linux](https://exiftool.org)

</details>

</div>

<div class="admonition example" markdown>
<p class="admonition-title">Usuwanie danych z katalogu plików</p>

```bash
exiftool -all= *.rozszerzenie_pliku
```

</div>

## Kryteria

**Należy pamiętać, że nie jesteśmy powiązani z żadnym z polecanych przez nas projektów.** Oprócz [naszych standardowych kryteriów](about/criteria.md) opracowaliśmy jasny zestaw wymagań, które pozwalają nam formułować obiektywne zalecenia. Sugerujemy zapoznanie się z tą listą przed wyborem projektu oraz przeprowadzenie własnych badań, aby upewnić się, że jest to odpowiedni wybór dla Ciebie.

- Aplikacje opracowane dla systemów operacyjnych typu open source muszą być open source.
- Aplikacje muszą być bezpłatne i nie powinny zawierać reklam ani innych ograniczeń.
