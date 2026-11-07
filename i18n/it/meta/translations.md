---
title: Translations
description: A guide for website contributors on adding translations to our website.
---

Crowdin dispone di una buona documentazione, e suggeriamo di consultare la loro guida [Per Iniziare](https://support.crowdin.com/crowdin-intro). Il nostro sito è per lo più scritto in [Markdown](https://en.wikipedia.org/wiki/Markdown), quindi, contribuire, dovrebbe essere facile. Questa pagina contiene dei consigli utili per tradurre parte specifica della sintassi che potresti incontrare sul nostro sito.

Ti preghiamo di unirti alla nostra stanza di localizzazione su Matrix ([#pg-i18n:aragon.sh](https://matrix.to/#/%23pg-i18n:aragon.sh)) se hai ulteriori domande, e di leggere il nostro [post di annuncio del blog](https://blog.privacyguides.org/2023/02/26/i18n-announcement) per ulteriori informazioni sul progetto.

Nota che la versione in inglese del sito è la versione principale, a significare che le modifiche si verificano lì per prime. Se noti che una lingua non è aggiornata, ti preghiamo di contribuire. Non possiamo garantire l'accuratezza di tutte le nostre traduzioni. Se hai un suggerimento sui contenuti specifici della tua regione, ti preghiamo di aprire un ticket o una richiesta di pull, nel nostro [repository principale](https://github.com/privacyguides/privacyguides.org).

## Risultato traduzione

Il software di traduzione ottiene delle traduzioni abbastanza accurate; tuttavia, devi assicurarti che la stringa tradotta sia corretta.

Ad esempio:

```text
![Software logo](assets/images/path/to/image.svg){ align=right }
```

Talvolta, ci siamo resi conto che la sintassi per inserire un'immagine come la precedente, mancava del `![` o che uno spazio aggiuntivo era posizionato tra il testo e il percorso, es. `](`. Se una stringa di traduzione è chiaramente errata, ti incoraggiamo a **eliminarla**, premendo l'icona del cestino, [o di votare](https://support.crowdin.com/enterprise/getting-started-for-volunteers/#voting-view) quella che suona meglio. Quando le stringhe non valide sono eliminate, sono rimosse dalla [memoria di traduzione](https://support.crowdin.com/enterprise/translation-memory) dell'organizzazione, a significare che quando la stringa sorgente viene incontrata nuovamente, la traduzione errata non sarà suggerita.

## Immagini

Images shared by all languages live in `docs/assets/images` and are excluded from Crowdin. When you run `SITE_LANGUAGE=fr ./run.sh` (replacing `fr` with your language code), the build script links this directory into `i18n/fr/assets/images` so translated builds and Markdown previews can use the same files.

Images containing text that needs translation live in `docs/assets/images-localized` and are uploaded to Crowdin. They retain their existing `docs/assets/img` paths in Crowdin to preserve translations, but are exported to `i18n/<language>/assets/images-localized`. Keep `assets/images-localized` in translated Markdown image paths so the same references resolve to the appropriate images in every language.

## Punteggiatura

Per gli esempi come gli ammonimenti precedenti, le virgolette, es.: `" "` devono essere utilizzate per specificare il testo della stringa. MkDocs non interpreterà correttamente altri simboli, cioè, `「 」` o `« »`. Altri segni di punteggiatura vanno bene per contrassegnare regolari citazioni all'interno del testo.

## Alternative a larghezza intera e sintassi di Markdown

Sistemi di scrittura CJK tendono a utilizzare varianti alternative "a larghezza intera" di simboli comuni. These are different characters and cannot be used for Markdown syntax.

- Links must use regular parenthesis i.e. `(` (Left Parenthesis U+0028) and `)` (Right Parenthesis U+0029) and not `（` (Fullwidth Left Parenthesis U+FF08) or `）` (Fullwidth Right Parenthesis U+FF09)
- Il testo tra virgolette rientrato deve utilizzare `:` (Due punti U+003A) e non `：` (Due Punti a Larghezza Intera U+FF1A)
- Le immagini devono utilizzare `!` (Punto Esclamativo U+0021) e non `！` (Punto Esclamativo a Larghezza Intera U+FF01)
