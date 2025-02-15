---
title: Локализация
description: Руководство для людей, которые хотят сделать перевод нашего сайта.
---

У Crowdin хорошая документация, и мы рекомендуем ознакомиться с их руководством по [началу работы](https://support.crowdin.com/crowdin-intro). Наш сайт в основном использует формат [Markdown](https://en.wikipedia.org/wiki/Markdown), поэтому внести свой вклад будет просто. На этой странице собраны полезные советы по использованию специфического синтаксиса, который вы можете встретить во время перевода.

Если у вас есть дополнительные вопросы, пожалуйста, вступите в нашу группу по локализации в Matrix ([#pg-i18n:aragon.sh](https://matrix.to/#/%23pg-i18n:aragon.sh)) и прочитайте [анонс в нашем блоге](https://blog.privacyguides.org/2023/02/26/i18n-announcement) для получения дополнительной информации о проекте.

Note that the English version of the site is the primary version, meaning changes occur there first. If you notice a language falling behind the English version, please help out. We cannot guarantee the accuracy of all our translations. If you have a suggestion about content specific to your region, please open an issue or pull request to our [main repository](https://github.com/privacyguides/privacyguides.org).

## Translation output

Translation software gets the translation quite accurate; however, you need to make sure the translated string is correct.

For example:

```text
![Логотип программы](assets/img/path/to/image.svg){ align=right }
```

We have sometimes found that the syntax for inserting an image like above was missing the `![` or an extra space was placed between the text and the path, e.g. `](`. If a translation string is clearly not correct, we encourage you to **delete** it by pressing the trash icon [or vote](https://support.crowdin.com/enterprise/getting-started-for-volunteers/#voting-view) on which one you think sounds best. When invalid strings are deleted, they are removed from the organization's [translation memory](https://support.crowdin.com/enterprise/translation-memory), meaning that when the source string is seen again, it won't suggest the incorrect translation.

## Пунктуация

For examples like the above admonitions, quotation marks, e.g.: `" "` must be used to specify string text. MkDocs will not correctly interpret other symbols i.e., `「 」` or `« »`. Other punctuation marks are fine for marking regular quotations within the text otherwise.

## Fullwidth alternatives and Markdown syntax

CJK writing systems tend to use alternative "fullwidth" variants of common symbols. These are different characters and cannot be used for markdown syntax.

- Links must use regular parenthesis ie `(` (Left Parenthesis U+0028) and `)` (Right Parenthesis U+0029) and not `（` (Fullwidth Left Parenthesis U+FF08) or `）` (Fullwidth Right Parenthesis U+FF09)
- Indented quoted text must use `:` (Colon U+003A) and not `：` (Fullwidth Colon U+FF1A)
- Pictures must use `!` (Exclamation Mark U+0021) and not `！` (Fullwidth Exclamation Mark U+FF01)
