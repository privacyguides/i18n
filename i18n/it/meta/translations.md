---
title: Traduzioni
---

Crowdin has good documentation, and we suggest looking at their [Getting Started](https://support.crowdin.com/crowdin-intro) guide. Il nostro sito è per lo più scritto in [Markdown](https://en.wikipedia.org/wiki/Markdown), quindi, contribuire, dovrebbe essere facile. Questa pagina contiene dei consigli utili per tradurre parte specifica della sintassi che potresti incontrare sul nostro sito.

Please join our localization room on Matrix ([#pg-i18n:aragon.sh](https://matrix.to/#/%23pg-i18n:aragon.sh)) if you have any additional questions, and read our [announcement blog post](https://blog.privacyguides.org/2023/02/26/i18n-announcement) for additional information about the project.

Nota che la versione in inglese del sito è la versione principale, a significare che le modifiche si verificano lì per prime. Se noti che una lingua non è aggiornata, ti preghiamo di contribuire. Non possiamo garantire l'accuratezza di tutte le nostre traduzioni. Se hai un suggerimento sui contenuti specifici della tua regione, ti preghiamo di aprire un ticket o una richiesta di pull, nel nostro [repository principale](https://github.com/privacyguides/privacyguides.org).

## Risultato traduzione

Il software di traduzione ottiene delle traduzioni abbastanza accurate; tuttavia, devi assicurarti che la stringa tradotta sia corretta.

Ad esempio:

```text
![Logo del software](assets/img/path/to/image.svg){ align=right }
```

Talvolta, ci siamo resi conto che la sintassi per inserire un'immagine come la precedente, mancava del `![` o che uno spazio aggiuntivo era posizionato tra il testo e il percorso, es. `](`. Se una stringa di traduzione è chiaramente errata, ti incoraggiamo a **eliminarla**, premendo l'icona del cestino, [o di votare](https://support.crowdin.com/enterprise/getting-started-for-volunteers/#voting-view) quella che suona meglio. Quando le stringhe non valide sono eliminate, sono rimosse dalla [memoria di traduzione](https://support.crowdin.com/enterprise/translation-memory) dell'organizzazione, a significare che quando la stringa sorgente viene incontrata nuovamente, la traduzione errata non sarà suggerita.

## Punteggiatura

Per gli esempi come gli ammonimenti precedenti, le virgolette, es.: `" "` devono essere utilizzate per specificare il testo della stringa. MkDocs non interpreterà correttamente altri simboli, cioè, `「 」` o `« »`. Altri segni di punteggiatura vanno bene per contrassegnare regolari citazioni all'interno del testo.

## Alternative a larghezza intera e sintassi di Markdown

Sistemi di scrittura CJK tendono a utilizzare varianti alternative "a larghezza intera" di simboli comuni. Si tratta di caratteri differenti e non utilizzabili per la sintassi di Markdown.

- I link devono utilizzare le parentesi regolari, cioè `(` (Parentesi Sinistra U+0028) e `)` (Parentesi Destra U+0029) ee non `（` (Parentesi Sinistra a Larghezza Intera U+FF08) o `）` (Parentesi Destra a Larghezza Intera U+FF09)
- Il testo tra virgolette rientrato deve utilizzare `:` (Due punti U+003A) e non `：` (Due Punti a Larghezza Intera U+FF1A)
- Le immagini devono utilizzare `!` (Punto Esclamativo U+0021) e non `！` (Punto Esclamativo a Larghezza Intera U+FF01)
