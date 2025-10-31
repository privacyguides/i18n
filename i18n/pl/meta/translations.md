---
title: Tłumaczenia
description: Przewodnik dla współtwórców tej strony na temat dodawania tłumaczeń do naszego serwisu.
---

Crowdin posiada dobrą dokumentację i zalecamy zapoznanie się z ich przewodnikiem [„Pierwsze kroki”](https://support.crowdin.com/crowdin-intro) (w języku angielskim). Nasza strona jest w dużej mierze napisana w języku [Markdown](https://pl.wikipedia.org/wiki/Markdown), dzięki czemu powinno być łatwo wnieść swój wkład. Ta strona zawiera kilka pomocnych wskazówek dotyczących tłumaczenia pewnych specyficznych konstrukcji składniowych, na które można natrafić na naszej stronie.

Jeśli masz dodatkowe pytania, dołącz do naszego pokoju tłumaczeniowego na Matrixie ([#pg-i18n:aragon.sh](https://matrix.to/#/%23pg-i18n:aragon.sh)) oraz przeczytaj nasz [wpis na blogu z ogłoszeniem](https://blog.privacyguides.org/2023/02/26/i18n-announcement), aby dowiedzieć się więcej o projekcie.

Należy pamiętać, że wersja angielska strony jest wersją podstawową, co oznacza, że zmiany wprowadzane są najpierw tam. Jeśli zauważysz, że jakaś wersja językowa pozostaje w tyle za wersją angielską, prosimy o pomoc. Nie możemy jednak zagwarantować dokładności wszystkich naszych tłumaczeń. Jeśli masz sugestie dotyczące treści dotyczących Twojego regionu, utwórz zgłoszenie (issue) lub pull request w naszym [głównym repozytorium](https://github.com/privacyguides/privacyguides.org).

## Wynik tłumaczenia

Narzędzia tłumaczeniowe zapewniają całkiem dokładne tłumaczenia, jednak trzeba upewnić się, że przetłumaczony tekst jest poprawny.

Na przykład:

```text
![Logo programu](assets/img/path/to/image.svg){ align=right }
```

Czasami zdarzało się, że w powyższej składni do wstawiania obrazu brakowało znaku `![` lub między tekstem a ścieżką obrazu znajdowała się dodatkowa spacja, np. `](`. Jeśli tłumaczenie jest ewidentnie błędne, zalecamy jego **usunięcie** poprzez kliknięcie ikony kosza lub [oddanie głosu](https://support.crowdin.com/enterprise/getting-started-for-volunteers/#voting-view) na tłumaczenie, które wydaje się najbardziej poprawne. Po usunięciu nieprawidłowych tłumaczeń są one usuwane z [„pamięci tłumaczeniowej”](https://support.crowdin.com/enterprise/translation-memory) organizacji, co oznacza, że gdy tłumaczenie źródłowe pojawi się ponownie, nie będzie ono sugerować nieprawidłowego tłumaczenia.

## Punctuation

For examples like the above admonitions, quotation marks, e.g.: `" "` must be used to specify string text. MkDocs will not correctly interpret other symbols i.e., `「 」` or `« »`. Other punctuation marks are fine for marking regular quotations within the text otherwise.

## Fullwidth alternatives and Markdown syntax

CJK writing systems tend to use alternative "fullwidth" variants of common symbols. These are different characters and cannot be used for Markdown syntax.

- Links must use regular parenthesis i.e. `(` (Left Parenthesis U+0028) and `)` (Right Parenthesis U+0029) and not `（` (Fullwidth Left Parenthesis U+FF08) or `）` (Fullwidth Right Parenthesis U+FF09)
- Indented quoted text must use `:` (Colon U+003A) and not `：` (Fullwidth Colon U+FF1A)
- Pictures must use `!` (Exclamation Mark U+0021) and not `！` (Fullwidth Exclamation Mark U+FF01)
