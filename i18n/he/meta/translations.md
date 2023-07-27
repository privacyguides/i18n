---
title: תרגומים
---

ל-Crowdin יש תיעוד טוב, ואנו מציעים לעיין במדריך [תחילת העבודה](https://support.crowdin.com/crowdin-intro/) שלהם. האתר שלנו כתוב ברובו ב[Markdown](https://en.wikipedia.org/wiki/Markdown), כך שיהיה קל לתרום. דף זה מכיל כמה עצות מועילות לתרגום תחביר ספציפי שאתה עשוי להיתקל בו באתר שלנו.

אנא הצטרף לחדר הלוקליזציה שלנו ב-Matrix ([#pg-i18n:aragon.sh](https://matrix.to/#/%23pg-i18n:aragon.sh)) אם יש לך שאלות נוספות, וקרא את [פוסט בלוג ההכרזה](https://blog.privacyguides.org/2023/02/26/i18n-announcement/) שלנו לקבלת מידע נוסף על הפרויקט.

שימו לב שהגרסה האנגלית של האתר היא הגרסה הראשית, כלומר שינויים מתרחשים שם תחילה. אם אתה מבחין בשפה שנמצאת מאחורי הגרסה האנגלית, אנא עזור. איננו יכולים להבטיח את הדיוק של כל התרגומים שלנו. אם יש לך הצעה לגבי תוכן ספציפי לאזור שלך, פתח בעיה או שלח בקשה ל[מאגר הראשי](https://github.com/privacyguides/privacyguides.org) שלנו.

## אזהרות

Throughout the site we use MkDocs's [admonitions](https://squidfunk.github.io/mkdocs-material/reference/admonitions/#usage), to show information to readers. They come in a few different flavors such as `example`, `warning`, `tip`, etc.

When admonitions are used they will have an English string on the site by default. This can be [customized](https://squidfunk.github.io/mkdocs-material/reference/admonitions/#changing-the-title), without too much effort. For example, if you were translating an admonition of type [`warning`](https://squidfunk.github.io/mkdocs-material/reference/admonitions/#type:warning) to Dutch, this is how you would write it:

=== "Dutch translation"

    ```text
    !!! warning "Waarschuwing"
    ```

=== "English source text"

    ```text
    !!! warning "אזהרה"
    ```

Downloads are a [custom admonition](https://squidfunk.github.io/mkdocs-material/reference/admonitions/#custom-admonitions) which is written as follows:

=== "Dutch translation"

    ```text
    ??? downloads "Downloaden"
    ```

=== "English source text"

    ```text
    ??? downloads
    ```

The same goes for other types, such as `tip`, `example`, `warning`, `danger` etc.

Recommendations are a special type of admonition which do **not** need overriding as they have no visible text, so they are never changed:

=== "Dutch translation"

    ```text
    !!! recommendation
    ```

=== "English source text"

    ```text
    !!! recommendation
    ```

## Translation output

Translation software gets the translation quite accurate; however, you need to make sure the translated string is correct.

For example:

```text
![Software logo](assets/img/path/to/image.svg){ align=right }
```

We have sometimes found that the syntax for inserting an image like above was missing the `![` or an extra space was placed between the text and the path, e.g. `](`. If a translation string is clearly not correct, we encourage you to **delete** it by pressing the trash icon [or vote](https://support.crowdin.com/enterprise/getting-started-for-volunteers/#voting-view) on which one you think sounds best. When invalid strings are deleted, they are removed from the organization's [translation memory](https://support.crowdin.com/enterprise/translation-memory), meaning that when the source string is seen again, it won't suggest the incorrect translation.

## Punctuation

For examples like the above admonitions, quotation marks, e.g.: `" "` must be used to specify string text. MkDocs will not correctly interpret other symbols i.e., `「 」` or `« »`. Other punctuation marks are fine for marking regular quotations within the text otherwise.

## Fullwidth alternatives and Markdown syntax

CJK writing systems tend to use alternative "fullwidth" variants of common symbols. These are different characters and cannot be used for markdown syntax.

- Links must use regular parenthesis ie `(` (Left Parenthesis U+0028) and `)` (Right Parenthesis U+0029) and not `（` (Fullwidth Left Parenthesis U+FF08) or `）` (Fullwidth Right Parenthesis U+FF09)
- Indented quoted text must use `:` (Colon U+003A) and not `：` (Fullwidth Colon U+FF1A)
- Pictures must use `!` (Exclamation Mark U+0021) and not `！` (Fullwidth Exclamation Mark U+FF01) 
