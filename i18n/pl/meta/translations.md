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

## Interpunkcja

W przykładach takich jak powyższe ostrzeżenia należy używać cudzysłowów `" "` do oznaczania tekstu w postaci ciągów znaków (string). MkDocs nie interpretuje poprawnie innych symboli, takich jak `「 」` czy `« »`. Pozostałe znaki interpunkcyjne można stosować bez przeszkód w zwykłych cytatach w tekście.

## Odpowiedniki znaków o pełnej szerokości i składnia Markdown

Systemy pisma CJK (chiński, japoński, koreański) często używają alternatywnych wariantów popularnych symboli o pełnej szerokości. Są to jednak całkowicie inne znaki i nie mogą być używane w składni Markdown.

- Linki muszą korzystać ze zwykłych nawiasów okrągłych, tj. `(` (lewy nawias U+0028) i `)` (prawy nawias U+0029), a nie `（` (lewy nawias o pełnej szerokości U+FF08) ani `）` (prawy nawias o pełnej szerokości U+FF09),
- Cytaty ze wcięciem muszą używać dwukropka `:` (dwukropek U+003A), a nie `：` (dwukropek o pełnej szerokości U+FF1A),
- Obrazy muszą używać wykrzyknika `!` (wykrzyknik U+0021), a nie `！` (wykrzyknik o pełnej szerokości U+FF01).
