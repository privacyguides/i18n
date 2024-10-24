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

## מחשב שולחני

### MAT2

<div class="admonition recommendation" markdown>

![MAT2 לוגו](assets/img/data-redaction/mat2.svg){ align=right }

**MAT2** היא תוכנה חופשית, המאפשרת להסיר את המטא נתונים מסוגים של תמונות, אודיו, טורנטים ומסמכים. It provides both a command line tool and a graphical user interface via an extension for [Dolphin](https://0xacab.org/jvoisin/mat2/-/tree/master/dolphin), the default file manager of [KDE](https://kde.org).

בלינקוס, קיים כלי גרפי של צד שלישי [Metadata Cleaner](https://gitlab.com/rmnvgr/metadata-cleaner) המופעל על ידי MAT2 והוא [זמין ב-Flathub](https://flathub.org/apps/details/fr.romainvigier.MetadataCleaner).

[:octicons-repo-16: Repository](https://0xacab.org/jvoisin/mat2){ .md-button .md-button--primary }
[:octicons-info-16:](https://0xacab.org/jvoisin/mat2/-/blob/master/README.md){ .card-link title=Documentation}
[:octicons-code-16:](https://0xacab.org/jvoisin/mat2){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://pypi.org/project/mat2)
- [:simple-apple: macOS](https://0xacab.org/jvoisin/mat2#requirements-setup-on-macos-os-x-using-homebrew)
- [:simple-linux: Linux](https://pypi.org/project/mat2)
- [:octicons-globe-16: Web](https://0xacab.org/jvoisin/mat2#web-interface)

</details>

</div>

## נייד

### ExifEraser (אנדרואיד)

<div class="admonition recommendation" markdown>

![לוגו של ExifEraser](assets/img/data-redaction/exiferaser.svg){ align=right }

**ExifEraser** הוא יישום מודרני למחיקת מטא נתונים של תמונות ללא הרשאה עבור אנדרואיד.

בשלב זה הוא תומך בקבצי JPEG, PNG ו - WebP.

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

### Metapho (iOS)

<div class="admonition recommendation" markdown>

![Metapho לוגו](assets/img/data-redaction/metapho.jpg){ align=right }

**Metapho** הוא צופה פשוט ונקי עבור מטא נתונים של תמונות כגון תאריך, שם קובץ, גודל, מודל מצלמה, מהירות צמצם ומיקום.

[:octicons-home-16: Homepage](https://zininworks.com/metapho){ .md-button .md-button--primary }
[:octicons-eye-16:](https://zininworks.com/privacy){ .card-link title="Privacy Policy" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id914457352)

</details>

</div>

### PrivacyBlur

<div class="admonition recommendation" markdown>

![PrivacyBlur logo](assets/img/data-redaction/privacyblur.svg){ align=right }

** PrivacyBlur** היא אפליקציה חינמית שיכולה לטשטש חלקים רגישים של תמונות לפני שהיא משתפת אותם באינטרנט.

[:octicons-home-16: Homepage](https://privacyblur.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://privacyblur.app/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/MATHEMA-GmbH/privacyblur#readme){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/MATHEMA-GmbH/privacyblur){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.mathema.privacyblur)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1536274106)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

כדאי **לעולם** לא להשתמש בטשטוש כדי לעצב [טקסט בתמונות](https://bishopfox.com/blog/unredacter-tool-never-pixelation). אם ברצונך לשנות טקסט בתמונה, צייר תיבה מעל הטקסט. לשם כך, אנו מציעים אפליקציות כמו [Pocket Paint](https://github.com/Catrobat/Paintroid).

</div>

## שורת הפקודה

### ExifTool

<div class="admonition recommendation" markdown>

![ExifTool לוגו](assets/img/data-redaction/exiftool.png){ align=right }

**ExifTool** הוא ספריית ה-perl המקורית ויישום שורת הפקודה לקריאה, כתיבה ועריכה של מטא מידע (Exif, IPTC, XMP ועוד) במגוון רחב של פורמטים של קבצים (JPEG, TIFF, PNG, PDF, RAW ועוד).

לעתים קרובות זה מרכיב של יישומי הסרת Exif אחרים ונמצא ברוב מאגרי ההפצה של לינוקס.

[:octicons-home-16: Homepage](https://exiftool.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://exiftool.org/faq.html){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/exiftool/exiftool){ .card-link title="Source Code" }
[:octicons-heart-16:](https://exiftool.org/#donate){ .card-link title=Contribute }

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
