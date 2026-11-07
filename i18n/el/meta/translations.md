---
title: Translations
description: A guide for website contributors on adding translations to our website.
---

Το Crowdin διαθέτει καλή τεκμηρίωση και σας προτείνουμε να διαβάσετε τον οδηγό τους για τα [πρώτα βήματα](https://support.crowdin.com/crowdin-intro). Ο ιστότοπός μας είναι σε μεγάλο βαθμό γραμμένος σε [Markdown](https://en.wikipedia.org/wiki/Markdown), οπότε θα είναι εύκολο να συνεισφέρετε. Αυτή η σελίδα περιέχει μερικές χρήσιμες συμβουλές για τη μετάφραση ορισμένων συγκεκριμένων συντακτικών που μπορεί να συναντήσετε στον ιστότοπό μας.

Παρακαλείστε να συμμετάσχετε στο δωμάτιο μετάφρασης στο Matrix[(#pg-i18n:aragon.sh](https://matrix.to/#/%23pg-i18n:aragon.sh)) αν έχετε επιπλέον ερωτήσεις και διαβάστε [την ανάρτηση της ανακοίνωσής μας στο ιστολόγιο](https://blog.privacyguides.org/2023/02/26/i18n-announcement) για περισσότερες πληροφορίες σχετικά με το έργο.

Σημειώστε ότι η αγγλική έκδοση του ιστότοπου είναι η κύρια έκδοση, πράγμα που σημαίνει ότι οι αλλαγές γίνονται πρώτα εκεί. Αν παρατηρήσετε ότι μια γλώσσα υστερεί σε σχέση με την αγγλική έκδοση, παρακαλώ βοηθήστε μας. Δεν μπορούμε να εγγυηθούμε την ακρίβεια όλων των μεταφράσεών μας. Αν έχετε κάποια πρόταση σχετικά με το περιεχόμενο που αφορά την περιοχή σας, ανοίξτε ένα θέμα ή ένα pull request στο [κύριο repository](https://github.com/privacyguides/privacyguides.org) μας.

## Απόδοση μετάφρασης

Το μεταφραστικό λογισμικό κάνει τη μετάφραση αρκετά ακριβή- ωστόσο, πρέπει να βεβαιωθείτε ότι η μεταφρασμένη συμβολοσειρά είναι σωστή.

Για παράδειγμα:

```text
![Software logo](assets/images/path/to/image.svg){ align=right }
```

Μερικές φορές διαπιστώσαμε ότι από τη σύνταξη για την εισαγωγή μιας εικόνας, όπως παραπάνω, έλειπε το `![` ή ότι ένα επιπλέον κενό βρισκόταν μεταξύ του κειμένου και της διαδρομής, π.χ. `](`. Εάν μια συμβολοσειρά μετάφρασης είναι σαφώς μη σωστή, σας ενθαρρύνουμε να τη **διαγράψετε** πατώντας το εικονίδιο του κάδου απορριμμάτων [ή να ψηφίσετε](https://support.crowdin.com/enterprise/getting-started-for-volunteers/#voting-view) ποια νομίζετε ότι ακούγεται καλύτερα. Όταν οι άκυρες συμβολοσειρές διαγράφονται, αφαιρούνται από τη [μεταφραστική μνήμη](https://support.crowdin.com/enterprise/translation-memory) του οργανισμού, πράγμα που σημαίνει ότι όταν η συμβολοσειρά πηγής εμφανίζεται ξανά, δεν θα προτείνει τη λανθασμένη μετάφραση.

## Εικόνες

Images shared by all languages live in `docs/assets/images` and are excluded from Crowdin. When you run `SITE_LANGUAGE=fr ./run.sh` (replacing `fr` with your language code), the build script links this directory into `i18n/fr/assets/images` so translated builds and Markdown previews can use the same files.

Images containing text that needs translation live in `docs/assets/images-localized` and are uploaded to Crowdin. They retain their existing `docs/assets/img` paths in Crowdin to preserve translations, but are exported to `i18n/<language>/assets/images-localized`. Keep `assets/images-localized` in translated Markdown image paths so the same references resolve to the appropriate images in every language.

## Στίξη

Για παραδείγματα όπως οι παραπάνω παραινέσεις, τα εισαγωγικά, π.χ.: `" "` πρέπει να χρησιμοποιούνται για τον προσδιορισμό κειμένου συμβολοσειράς. Το MkDocs δεν θα ερμηνεύσει σωστά άλλα σύμβολα, π.χ. 「 `」` ή `" ".` Τα άλλα σημεία στίξης είναι εντάξει για την επισήμανση κανονικών παραθεμάτων εντός του κειμένου.

## Εναλλακτικές λύσεις Fullwidth και σύνταξη Markdown

Τα συστήματα γραφής CJK τείνουν να χρησιμοποιούν εναλλακτικές παραλλαγές "fullwidth" κοινών συμβόλων. These are different characters and cannot be used for Markdown syntax.

- Links must use regular parenthesis i.e. `(` (Left Parenthesis U+0028) and `)` (Right Parenthesis U+0029) and not `（` (Fullwidth Left Parenthesis U+FF08) or `）` (Fullwidth Right Parenthesis U+FF09)
- Το κείμενο με εισαγωγικά σε εσοχή πρέπει να χρησιμοποιεί `:` (άνω και κάτω τελεία U+003A) και όχι `：` (Fullwidth Colon U+FF1A)
- Οι εικόνες πρέπει να χρησιμοποιούν `!` (Θαυμαστικό U+0021) και όχι `！` (Θαυμαστικό fullwidth U+FF01)
