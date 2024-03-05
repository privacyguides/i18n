---
meta_title: "Remove PII with Metadata Scrubbers and Data Redaction Tools - Privacy Guides"
title: "Data and Metadata Redaction"
icon: material/tag-remove
description: Use these tools to remove metadata like GPS location and other identifying information from photos and files you share.
cover: data-redaction.webp
---

Когда вы делитесь с кем-то файлами, то не забудьте удалить связанные с ними метаданные. Файлы изображений обычно содержат [данные EXIF](https://ru.wikipedia.org/wiki/Exif). Иногда фотографии даже содержат ваши GPS координаты в метаданных файла.

## Для компьютеров

### MAT2

<div class="admonition recommendation" markdown>

![Логотип MAT2](assets/img/data-redaction/mat2.svg){ align=right }

**MAT2** - это бесплатное программное обеспечение, которое позволяет удалять метаданные из изображений, аудио, торрентов и документов. It provides both a command line tool and a graphical user interface via an extension for [Dolphin](https://0xacab.org/jvoisin/mat2/-/tree/master/dolphin), the default file manager of [KDE](https://kde.org).

В Linux существует сторонний графический инструмент [Metadata Cleaner](https://gitlab.com/rmnvgr/metadata-cleaner) на базе MAT2, который [доступен на Flathub](https://flathub.org/apps/details/fr.romainvigier.MetadataCleaner).

[:octicons-repo-16: Repository](https://0xacab.org/jvoisin/mat2){ .md-button .md-button--primary }
[:octicons-info-16:](https://0xacab.org/jvoisin/mat2/-/blob/master/README.md){ .card-link title=Documentation}
[:octicons-code-16:](https://0xacab.org/jvoisin/mat2){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://pypi.org/project/mat2)
- [:simple-apple: macOS](https://0xacab.org/jvoisin/mat2#requirements-setup-on-macos-os-x-using-homebrew)
- [:simple-linux: Linux](https://pypi.org/project/mat2)
- [:octicons-globe-16: Web](https://0xacab.org/jvoisin/mat2#web-interface)

</details>

</div>

## Для телефонов

### ExifEraser (Android)

<div class="admonition recommendation" markdown>

![Логотип ExifEraser](assets/img/data-redaction/exiferaser.svg){ align=right }

**ExifEraser** - это современное приложение, не требующее разрешений, для удаления метаданных изображений для Android.

В настоящее время он поддерживает файлы JPEG, PNG и WebP.

[:octicons-repo-16: Repository](https://github.com/Tommy-Geenexus/exif-eraser){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/Tommy-Geenexus/exif-eraser#readme){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/Tommy-Geenexus/exif-eraser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.none.tom.exiferaser)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/com.none.tom.exiferaser)
- [:simple-github: GitHub](https://github.com/Tommy-Geenexus/exif-eraser/releases)

</details>

</div>

Удаляемые метаданные зависят от типа файла изображения:

- **JPEG**: ICC Профиль, Exif, Photoshop Image Resources и XMP/ExtendedXMP будут удалены, если они существуют.
- **PNG**: ICC Profile, Exif и XMP будут удалены, если они существуют.
- **WebP**: ICC Profile, Exif и XMP будут удалены, если они существуют.

После обработки изображений ExifEraser предоставляет вам полный отчет о том, что именно было удалено с каждого изображения.

Приложение предлагает несколько способов удаления метаданных с изображений. А именно:

- С помощью ExifEraser можно поделиться изображением из другого приложения.
- В самом приложении можно выбрать одно изображение, несколько изображений сразу или даже целый каталог.
- В нем есть опция "Камера", которая использует приложение камеры вашей операционной системы для создания фотографии, а затем удаляет из нее метаданные.
- Он позволяет перетаскивать фотографии из другого приложения в ExifEraser, когда они оба открыты в режиме разделенного экрана.
- Наконец, он позволяет вставить изображение из буфера обмена.

### Metapho (iOS)

<div class="admonition recommendation" markdown>

![Логотип Metapho](assets/img/data-redaction/metapho.jpg){ align=right }

**Metapho** - это простая и чистая программа для просмотра метаданных фотографии, таких как дата, имя файла, размер, модель камеры, выдержка и местоположение.

[:octicons-home-16: Homepage](https://zininworks.com/metapho){ .md-button .md-button--primary }
[:octicons-eye-16:](https://zininworks.com/privacy/){ .card-link title="Privacy Policy" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-appstore: App Store](https://apps.apple.com/us/app/metapho/id914457352)

</details>

</div>

### PrivacyBlur

<div class="admonition recommendation" markdown>

![Логотип PrivacyBlur](assets/img/data-redaction/privacyblur.svg){ align=right }

**PrivacyBlur** - это бесплатное приложение, которое позволяет размыть чувствительные части фотографий перед тем, как поделиться ими в интернете.

[:octicons-home-16: Homepage](https://privacyblur.app/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://privacyblur.app/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/MATHEMA-GmbH/privacyblur#readme){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/MATHEMA-GmbH/privacyblur){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.mathema.privacyblur)
- [:simple-appstore: App Store](https://apps.apple.com/us/app/privacyblur/id1536274106)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Предупреждение</p>

Вы **никогда** не должны использовать размытие для редактирования [текста на изображениях](https://bishopfox.com/blog/unredacter-tool-never-pixelation). Если вы хотите скрыть текст на изображении, закройте текст черным квадратом. Для этого мы предлагаем такие приложения, как [Pocket Paint](https://github.com/Catrobat/Paintroid).

</div>

## Для командной строки

### ExifTool

<div class="admonition recommendation" markdown>

![Логотип ExifTool](assets/img/data-redaction/exiftool.png){ align=right }

**ExifTool** - это оригинальная библиотека perl и приложение командной строки для чтения, записи и редактирования метаинформации (Exif, IPTC, XMP и др.) в самых разных форматах файлов (JPEG, TIFF, PNG, PDF, RAW и др.).

Он часто является компонентом других приложений для удаления Exif и находится в репозиториях большинства дистрибутивов Linux.

[:octicons-home-16: Homepage](https://exiftool.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://exiftool.org/faq.html){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/exiftool/exiftool){ .card-link title="Source Code" }
[:octicons-heart-16:](https://exiftool.org/#donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://exiftool.org)
- [:simple-apple: macOS](https://exiftool.org)
- [:simple-linux: Linux](https://exiftool.org)

</details>

</div>

<div class="admonition example" markdown>
<p class="admonition-title">Deleting data from a directory of files</p>

```bash
exiftool -all= *.file_extension
```

</div>

## Критерии

**Обрати внимание, что у нас нет связей ни с одним проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Перед тем, как вы решите выбрать какой-либо проект, мы рекомендуем вам ознакомиться со списком критериев и провести собственное исследование, чтобы убедиться в правильности своего выбора.

<div class="admonition example" markdown>
<p class="admonition-title">This section is new</p>

Мы всё еще работаем над установлением критериев для каждого раздела нашего сайта, поэтому они могут поменяться в будущем. Если у вас есть вопросы по поводу наших критериев, пожалуйста, [задавайте их на нашем форуме](https://discuss.privacyguides.net/latest). Если какой-то критерий здесь не указан, это не значит, что мы его не учли. Перед тем, как рекомендовать какой-либо проект мы учитываем и обсуждаем множество факторов. Документирование этих факторов ещё не завершено.

</div>

- Apps developed for open-source operating systems must be open source.
- Приложения должны быть бесплатными и не должны содержать рекламы или других ограничений.
