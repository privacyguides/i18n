---
meta_title: "Remove PII with Metadata Scrubbers and Data Redaction Tools - Privacy Guides"
title: "Data and Metadata Redaction"
icon: material/tag-remove
description: Use these tools to remove metadata like GPS location and other identifying information from photos and files you share.
cover: data-redaction.webp
---

<small>Protects against the following threat(s):</small>

- [:material-account-search: חשיפה ציבורית](basics/common-threats.md#limiting-public-information ""){.pg-green}

בעת שיתוף קבצים, הקפד להסיר מטא נתונים משויכים. קבצי תמונה כוללים בדרך כלל [נתוני Exif](https://en.wikipedia.org/wiki/Exif). תמונות לפעמים אפילו כוללות קואורדינטות GPS במטא-נתונים של הקובץ.

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

כדאי **לעולם** לא להשתמש בטשטוש כדי לעצב [טקסט בתמונות](https://bishopfox.com/blog/unredacter-tool-never-pixelation). If you want to redact text in an image, you should draw a box over the text.

</div>

## MAT2

<div class="admonition recommendation" markdown>

![MAT2 logo](assets/img/data-redaction/mat2.svg){ align=right }

**MAT2** is free, cross-platform software which allows you to remove metadata from image, audio, torrent, and document file types. It provides both a command line tool and a graphical user interface via an extension for [Dolphin](https://github.com/jvoisin/mat2/tree/master/dolphin), the default file manager of [KDE](https://kde.org).

[:octicons-repo-16: Repository](https://github.com/jvoisin/mat2#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/jvoisin/mat2#how-to-use-mat2){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/jvoisin/mat2){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://pypi.org/project/mat2)
- [:simple-apple: macOS](https://github.com/jvoisin/mat2#requirements-setup-on-macos-os-x-using-homebrew)
- [:simple-linux: Linux](https://pypi.org/project/mat2)
- [:octicons-browser-16: Web](https://github.com/jvoisin/mat2#web-interface)

</details>

</div>

## ExifEraser (אנדרואיד)

<div class="admonition recommendation" markdown>

![לוגו של ExifEraser](assets/img/data-redaction/exiferaser.svg){ align=right }

**ExifEraser** הוא יישום מודרני למחיקת מטא נתונים של תמונות ללא הרשאה עבור אנדרואיד.

It currently supports JPEG, PNG, and WebP files.

[:octicons-repo-16: Repository](https://github.com/Tommy-Geenexus/exif-eraser#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/Tommy-Geenexus/exif-eraser#description){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/Tommy-Geenexus/exif-eraser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.none.tom.exiferaser)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/com.none.tom.exiferaser)
- [:simple-github: GitHub](https://github.com/Tommy-Geenexus/exif-eraser/releases)

</details>

</div>

המטא נתונים שנמחקים תלויים בסוג הקובץ של התמונה:

- **JPEG**: פרופיל ICC, Exif, משאבי תמונה בפוטושופ ומטא-נתונים של XMP/ExtendedXMP יימחקו אם הם קיימים.
- **PNG**: פרופיל ICC, מטא נתונים של Exif ו - XMP יימחקו אם הם קיימים.
- **WebP**: פרופיל ICC, מטא נתונים של Exif ו - XMP יימחקו אם הם קיימים.

לאחר עיבוד התמונות, ExifEraser מספק לך דוח מלא על מה בדיוק הוסר מכל תמונה.

האפליקציה מציעה מספר דרכים למחיקת מטא - נתונים מתמונות. כלומר:

- באפשרותך לשתף תמונה מיישום אחר עם ExifEraser.
- דרך האפליקציה עצמה, אתה יכול לבחור תמונה אחת, תמונות מרובות בבת אחת, או אפילו ספריה שלמה.
- הוא כולל אפשרות "מצלמה ", המשתמשת באפליקציית המצלמה של מערכת ההפעלה כדי לצלם תמונה, ולאחר מכן מסירה ממנה את המטא נתונים.
- זה מאפשר לך לגרור תמונות מיישום אחר לתוך ExifEraser כאשר שניהם פתוחים במצב מסך מפוצל.
- לבסוף, הוא מאפשר לך להדביק תמונה מהלוח שלך.

## Shortcuts (iOS & macOS)

On iOS and macOS, you can remove image metadata without using any third-party apps by creating a [**shortcut**](https://apps.apple.com/app/id915249334) for this purpose. Here is an example shortcut you can download to use as is:

[:material-tag-minus: Clean Image Metadata](https://icloud.com/shortcuts/fb774ddb7b5b4296871776c67ac0fff9 ""){.md-button}

You can also use it as a model for your own shortcut; just make sure that the **Preserve Metadata** option under the **Convert** action is unchecked. Once added, you can access the shortcut in the share sheet that appears when you select the :octicons-share-24: Share button. You can select multiple images and invoke the shortcut to remove their metadata all at once.

This shortcut removes metadata such as location, device model, lens model, and other camera information. It also sets the image creation date to the time the shortcut was used.

## ExifTool (CLI)

<div class="admonition recommendation" markdown>

![ExifTool logo](assets/img/data-redaction/exiftool.png){ align=right }

**ExifTool** is the original Perl library and command-line application for reading, writing, and editing meta information (Exif, IPTC, XMP, and more) in a wide variety of file formats (JPEG, TIFF, PNG, PDF, RAW, and more).

It is often a component of other Exif removal applications and in most Linux distribution repositories.

[:octicons-home-16: Homepage](https://exiftool.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://exiftool.org/faq.html){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/exiftool/exiftool){ .card-link title="Source Code" }
[:octicons-heart-16:](https://exiftool.org/#donate){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://exiftool.org)
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

## קריטריונים

**שים לב שאיננו קשורים לאף אחד מהפרויקטים שאנו ממליצים עליהם.** בנוסף ל [הקריטריונים הסטנדרטיים שלנו](about/criteria.md), פיתחנו סט ברור של דרישות כדי לאפשר לנו לספק המלצות אובייקטיביות. אנו מציעים לך להכיר את הרשימה הזו לפני שתבחר להשתמש בפרויקט, ולערוך מחקר משלך כדי להבטיח שזו הבחירה הנכונה עבורך.

- Apps developed for open-source operating systems must be open source.
- יישומים חייבים להיות חינמיים ולא לכלול מודעות או מגבלות אחרות.
