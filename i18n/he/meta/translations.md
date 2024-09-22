---
title: Translations
description: A guide for website contributors on adding translations to our website.
---

Crowdin has good documentation, and we suggest looking at their [Getting Started](https://support.crowdin.com/crowdin-intro) guide. האתר שלנו כתוב ברובו ב[Markdown](https://en.wikipedia.org/wiki/Markdown), כך שיהיה קל לתרום. דף זה מכיל כמה עצות מועילות לתרגום תחביר ספציפי שאתה עשוי להיתקל בו באתר שלנו.

Please join our localization room on Matrix ([#pg-i18n:aragon.sh](https://matrix.to/#/%23pg-i18n:aragon.sh)) if you have any additional questions, and read our [announcement blog post](https://blog.privacyguides.org/2023/02/26/i18n-announcement) for additional information about the project.

שימו לב שהגרסה האנגלית של האתר היא הגרסה הראשית, כלומר שינויים מתרחשים שם תחילה. אם אתה מבחין בשפה שנמצאת מאחורי הגרסה האנגלית, אנא עזור. איננו יכולים להבטיח את הדיוק של כל התרגומים שלנו. אם יש לך הצעה לגבי תוכן ספציפי לאזור שלך, פתח בעיה או שלח בקשה ל[מאגר הראשי](https://github.com/privacyguides/privacyguides.org) שלנו.

## פלט תרגום

תוכנת תרגום משיגה את התרגום מדויק למדי; עם זאת, עליך לוודא שהמחרוזת המתורגמת נכונה.

לדוגמה:

```text
![לוגו של התוכנה](assets/img/path/to/image.svg){ align=right }
```

מצאנו לפעמים שבתחביר להכנסת תמונה כמו לעיל חסר ה-`![` או שהוצב רווח נוסף בין הטקסט לנתיב, למשל. `](`. אם מחרוזת תרגום אינה נכונה בבירור, אנו ממליצים לך **למחוק** אותה על ידי לחיצה על סמל האשפה [או הצביעו](https://support.crowdin.com/enterprise /getting-started-for-volunteers/#voting-view) על מי לדעתכם נשמע הכי טוב. כאשר מחרוזות לא חוקיות נמחקות, הן מוסרות מ[זיכרון התרגום](https://support.crowdin.com/enterprise/translation-memory) של הארגון, כלומר כאשר מחרוזת המקור נראית שוב, זה לא יציע את התרגום השגוי.

## סימני פיסוק

עבור דוגמאות כמו האזהרות לעיל, מרכאות, למשל: יש להשתמש ב-`" "` כדי לציין טקסט מחרוזת. MkDocs לא יפרש נכון סמלים אחרים, כלומר `「 」` או `« »`. סימני פיסוק אחרים מתאימים לסימון ציטוטים רגילים בתוך הטקסט אחרת.

## חלופות ברוחב מלא ותחביר Markdown

מערכות כתיבה של CJK נוטות להשתמש בגרסאות חלופיות "ברוחב מלא" של סמלים נפוצים. אלו תווים שונים ולא ניתן להשתמש בהם עבור markdown.

- קישורים חייבים להשתמש בסוגריים רגילים, כלומר `(` (Left Parenthesis U+0028) ו-`)` (Right Parenthesis U+0029) ולא `（` (סוגריים שמאליים ברוחב מלא U+FF08) או `）` (סוגריים ימניים ברוחב מלא U+FF09)
- טקסט מצוטט עם הזחה חייב להשתמש ב-`:` (נקודתיים U+003A) ולא ב-`：` (נקודתיים U+FF1A ברוחב מלא)
- תמונות חייבות להשתמש ב-`!` (סימן קריאה U+0021) ולא ב-`！` (סימן קריאה ברוחב מלא U+FF01)
