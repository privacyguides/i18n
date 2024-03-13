---
title: Übersetzungen
---

Crowdin has good documentation, and we suggest looking at their [Getting Started](https://support.crowdin.com/crowdin-intro) guide. Unsere Website ist größtenteils in [Markdown](https://de.wikipedia.org/wiki/Markdown) geschrieben, so dass es einfach sein sollte, etwas beizutragen. Diese Seite enthält einige hilfreiche Hinweise zur Übersetzung bestimmter Syntax, die dir auf unserer Website begegnen können.

Please join our localization room on Matrix ([#pg-i18n:aragon.sh](https://matrix.to/#/%23pg-i18n:aragon.sh)) if you have any additional questions, and read our [announcement blog post](https://blog.privacyguides.org/2023/02/26/i18n-announcement) for additional information about the project.

Bitte beachte, dass die englische Version der Website die primäre Version ist, d.h. Änderungen werden dort zuerst vorgenommen. Wenn du bemerkst, dass eine Sprache hinter der englischen Version liegt, hilf bitte mit. Wir können nicht für die Richtigkeit aller unserer Übersetzungen garantieren. Wenn du einen Vorschlag zu Inhalten hast, die speziell für deine Region gelten, öffne bitte ein Issue oder einen Pull Request in unserem [Main-Repository](https://github.com/privacyguides/privacyguides.org).

## Übersetzungsausgabe

Die Übersetzungssoftware sorgt für eine recht genaue Übersetzung; Du musst jedoch sicherstellen, dass die übersetzte Zeichenfolge korrekt ist.

Zum Beispiel:

```text
![Software logo](assets/img/path/to/image.svg){ align=right }
```

Wir haben manchmal festgestellt, dass in der Syntax zum Einfügen eines Bildes wie oben der `![` fehlte oder ein zusätzliches Leerzeichen zwischen dem Text und dem Pfad eingefügt wurde, z. B. `](`. Wenn eine Übersetzung eindeutig nicht korrekt ist, empfehlen wir dir, sie **zu löschen**, indem du auf das Papierkorbsymbol klickst, oder darüber [abzustimmen](https://support.crowdin.com/enterprise/getting-started-for-volunteers/#voting-view), welche Übersetzung deiner Meinung nach am besten klingt. Wenn ungültige Zeichenfolgen gelöscht werden, werden sie aus dem [Übersetzungsspeicher](https://support.crowdin.com/enterprise/translation-memory) der Organisation entfernt, d. h., wenn die Ausgangszeichenfolge erneut angezeigt wird, wird die falsche Übersetzung nicht erneut vorgeschlagen.

## Zeichensetzung

Bei Beispielen wie den obigen Admonitions müssen Anführungszeichen, z. B.: `" "`, verwendet werden, um den Text der Zeichenkette anzugeben. MkDocs interpretiert andere Symbole, z. B. `「 」` oder `« »`, nicht korrekt. Andere Satzzeichen sind gut geeignet, um regelmäßige Zitate innerhalb des Textes zu kennzeichnen.

## Alternativen in voller Breite und Markdown-Syntax

CJK Schreibsysteme neigen dazu, alternative "Vollbreite"-Varianten von gängigen Symbolen zu verwenden. Dies sind unterschiedliche Zeichen und können nicht für die Markdown-Syntax verwendet werden.

- Links müssen reguläre Klammern verwenden, d. h. `(` (Linke Parenthese U+0028) und `)` (Rechte Parenthese U+0029) und nicht `（` (Linke Parenthese in voller Breite U+FF08) oder `）` (volle Breite der rechten Klammer U+FF09)
- Eingerückter Text in Anführungszeichen muss `:` (Doppelpunkt U+003A) und nicht `：` (Doppelpunkt mit voller Breite U+FF1A) verwenden
- Bilder müssen `!` (Ausrufezeichen U+0021) und nicht `！` (Ausrufezeichen in voller Breite U+FF01) verwenden
