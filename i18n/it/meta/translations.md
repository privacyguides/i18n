---
title: Traduzioni
---

Crowdin ha una buona documentazione, e suggeriamo di consultare la loro guida [Per Iniziare](https://support.crowdin.com/crowdin-intro/). Il nostro sito è per lo più scritto in [Markdown](https://en.wikipedia.org/wiki/Markdown), quindi, contribuire, dovrebbe essere facile. Questa pagina contiene dei consigli utili per tradurre parte specifica della sintassi che potresti incontrare sul nostro sito.

Ti preghiamo di unirti alla nostra stanza di localizzazione su Matrix ([#pg-i18n:aragon.sh](https://matrix.to/#/%23pg-i18n:aragon.sh)), se hai qualsiasi ulteriore domanda, e di leggere i [post del nostro blog di annunci](https://blog.privacyguides.org/2023/02/26/i18n-announcement/), per ulteriori informazioni sul progetto.

Nota che la versione in inglese del sito è la versione principale, a significare che le modifiche si verificano lì per prime. Se noti che una lingua non è aggiornata, ti preghiamo di contribuire. Non possiamo garantire l'accuratezza di tutte le nostre traduzioni. Se hai un suggerimento sui contenuti specifici della tua regione, ti preghiamo di aprire un ticket o una richiesta di pull, nella nostra [repository principale](https://github.com/privacyguides/privacyguides.org).

## Ammonimenti

All'interno del sito utilizziamo gli [ammonimenti](https://squidfunk.github.io/mkdocs-material/reference/admonitions/#usage) di MkDocs, per mostrare le informazioni ai lettori. Possono avere diversi ambiti, quali `example` (esempio), `warning` (avviso), `tip` (consiglio), etc.

Quando sono utilizzati, gli ammonimenti avranno, di default, una stringa in inglese sul sito. Questa è [personalizzabile](https://squidfunk.github.io/mkdocs-material/reference/admonitions/#changing-the-title), senza troppi sforzi. Ad esempio, se stessi traducendo un ammonimento di tipo [`warning`](https://squidfunk.github.io/mkdocs-material/reference/admonitions/#type:warning) (avviso) in olandese, ecco come la dovresti scrivere:

=== "Traduzione olandese"

    ```text
    !!! warning "Waarschuwing"
    ```

=== "Testo di origine in inglese"

    ```text
    !!! warning "Attenzione"
    ```

I download sono [ammonimenti personalizzati](https://squidfunk.github.io/mkdocs-material/reference/admonitions/#custom-admonitions), scritti come segue:

=== "Traduzione olandese"

    ```text
    ??? downloads "Downloaden"
    ```

=== "Testo di origine in inglese"

    ```text
    ??? downloads
    ```

Lo stesso vale per altri tipi, quali `tip` (consiglio), `example` (esempio), `warning` (avviso), `danger` (pericolo), etc.

I consigli sono un tipo di ammonimento speciale che **non** necessita di sovrascrizione, essendo privo di testo visibile, quindi, che non è mai modificato:

=== "Traduzione olandese"

    ```text
    !!! recommendation
    ```

=== "Testo di origine in inglese"

    ```text
    !!! recommendation
    ```

## Risultato di traduzione

Il software di traduzione ottiene delle traduzioni abbastanza accurate; tuttavia, devi assicurarti che la stringa tradotta sia corretta.

Ad esempio:

```text
![Logo del software](assets/img/path/to/image.svg){ align=right }
```

Talvolta, ci siamo resi conto che la sintassi per inserire un'immagine come la precedente, mancava del `![` o che uno spazio aggiuntivo era posizionato tra il testo e il percorso, es. `](`. Se una stringa di traduzione è chiaramente errata, ti incoraggiamo a **eliminarla**, premendo l'icona del cestino, [o di votare](https://support.crowdin.com/enterprise/getting-started-for-volunteers/#voting-view) quella che suona meglio. Quando le stringhe non valide sono eliminate, sono rimosse dalla [memoria di traduzione](https://support.crowdin.com/enterprise/translation-memory) dell'organizzazione, a significare che quando la stringa sorgente viene incontrata nuovamente, la traduzione errata non sarà suggerita.

## Punteggiatura

Per gli esempi come gli ammonimenti precedenti, le virgolette, es.: `" "` devono essere utilizzate per specificare il testo della stringa. MkDocs non interpreterà correttamente altri simboli, cioè, `「 」` o `« »`. Altri segni di punteggiatura vanno bene per contrassegnare regolari citazioni all'interno del testo.

## Parentesi

I link in Markdown devono utilizzare le parentesi, come ad esempio, `[Link di esempio](https://esempio.it)`. Le parentesi in stile CJK, come `（ ）` non funzioneranno con i collegamenti. Crowdin, spesso, gestirà automaticamente i collegamenti, ma li incontrerai negli ammonimenti e in altri blocchi personalizzati di testo.
