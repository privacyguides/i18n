---
title: Uploading Images
description: A guide for website contributors on uploading images in the proper format and location.
---

If you make changes to this website that involve adding new images or replacing existing ones, here are a couple of general recommendations:

## תמונות

- We **prefer** SVG images, but if those do not exist we can use PNG images. Additionally, for cover images, we prefer that they are obtained from [Unsplash](https://unsplash.com) and are in the WebP format.

Company logos should be square if possible, and at least 200x200px if they are PNGs (non-vector images).

## אופטימיזציה

### PNG

Use the [OptiPNG](https://sourceforge.net/projects/optipng) tool to optimize PNG images:

```bash
optipng -o7 file.png
```

### SVG

#### Inkscape

[סרקו](https://github.com/scour-project/scour) את כל תמונות ה-SVG.

ב-Inkscape:

1. File Save As..
2. הגדר את הסוג ל-SVG אופטימיזציה (*.svg)

בלשונית **האפשרויות**:

- **מספר הספרות המשמעותיות עבור קואורדינטות** > **5**
- [x] הפעל את **קיצור ערכי צבע**
- [x] הפעל את **המר תכונות CSS לתכונות XML**
- [x] הפעל את **כווץ קבוצות**
- [x] הפעל את **צור קבוצות עבור תכונות דומות**
- [ ] כבה את **שמור נתוני עורך**
- [ ] כבה את **שמור הגדרות ללא הפניות**
- [x] הפעל את **עקוף באגים במעבד**

בכרטיסייה **פלט SVG** תחת **אפשרויות מסמך**:

- [ ] תכבה **הסר את הצהרת ה-XML**
- [x] הפעל **הסר מטא נתונים**
- [x] הפעל **הסר תגובות**
- [x] הפעל את **תמונות רסטר מוטמעות**
- [x] הפעל את **הפעל צפייה ב-viewboxing**

ב**פלט SVG** תחת **הדפסה יפה**:

- [ ] כבה את **עיצוב פלט עם מעברי שורה והזחה**
- **תווי הזחה** > בחר **חלל**
- **עומק הזחה** > **1**
- [ ] כבה את **הסר את התכונה "xml:space" מאלמנט הבסיס SVG**

בכרטיסייה **מזהים**:

- [x] הפעל את **הסר מזהים שאינם בשימוש**
- [ ] כבה את **קיצור מזהים**
- **קידומת מזהים מקוצרים עם** > `להשאיר ריק`
- [x] הפעל את **שמור מזהים שנוצרו באופן ידני שאינם מסתיימים בספרות**
- **שמור את המזהים הבאים** > `להשאיר ריק`
- **שמור מזהים המתחילים ב** > `להשאיר ריק`

#### CLI

ניתן להשיג את אותו הדבר עם הפקודה [Scour](https://github.com/scour-project/scour):

```bash
scour --set-precision=5 \
      --create-groups \
      --renderer-workaround \
      --remove-descriptive-elements \
      --enable-comment-stripping \
      --enable-viewboxing \
      --indent=space \
      --nindent=1 \
      --no-line-breaks \
      --enable-id-stripping \
      --protect-ids-noninkscape \
      input.svg output.svg
```

### WebP

Use the [cwebp](https://developers.google.com/speed/webp/docs/using) command to convert PNG or JPEG image files to WebP format:

```bash
cwebp -q 70 -m 6 input_file -o output.webp
```
