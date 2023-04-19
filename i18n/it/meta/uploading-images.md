---
title: Caricamento delle immagini
---

Ecco un paio di regole generali per contribuire a Privacy Guides:

## Immagini

- Noi **preferiamo** immagini in formato SVG, ma se non esistono possiamo usare anche immagini in formato PNG

I loghi aziendali hanno dimensioni canvas di:

- 128x128px
- 384x128px

## Ottimizzazione

### PNG

Usa [OptiPNG](https://sourceforge.net/projects/optipng/) per ottimizzare i file immagine PNG:

```bash
optipng -o7 file.png
```

### SVG

#### Inkscape

Utilizza [Scour](https://github.com/scour-project/scour) su tutte le immagini in formato SVG.

In Inkscape:

1. File Salva come...
2. Seleziona formato SVG ottimizzato (*.svg)

Nella scheda **Opzioni**:

- **Numero di cifre significative per le coordinate:** > **5**
- [x] Attiva **Abbrevia i valori dei colori**
- [x] Attiva **Converte gli attributi CSS in attributi XML**
- [x] Attiva **Unisci i gruppi**
- [x] Attiva **Crea gruppi per attributi simili**
- [ ] Disattiva **Mantieni i dati dell'editor**
- [ ] Disattiva **Mantieni le definizioni senza riferimenti**
- [x] Attiva **Correggi gli errori di rendering**

Nella scheda **Output SVG** sotto **Opzioni documento**:

- [ ] Disattiva **Rimuovi dichiarazione XML**
- [x] Attiva **Rimuovi metadati**
- [x] Attiva **Rimuovi commenti**
- [x] Attiva **Incorpora immagini raster**
- [x] Attiva **Attiva anteprima**

Nella scheda **Output SVG** sotto **Formattazione**:

- [ ] Disattiva **Output con a capo e indentazioni**
- **Caratteri di indentazione** > Seleziona**Spazio**
- **Ampiezza indentazione** > **1**
- [ ] Disattiva **Elimina l'attributo "xml:space" dall'elemento SVG di base**

Nella scheda **ID**:

- [x] Attiva **Rimuovi ID non utilizzati**
- [ ] Disattiva **Abbrevia ID**
- **Prefissa gli ID abbreviati** > `lascia vuoto`
- [x] Attiva **Mantieni ID manuali che non finiscono per cifra**
- **Mantieni gli ID seguenti** > `lascia vuoto`
- **Mantieni gli ID che iniziano con** > `lascia vuoto`

#### CLI

Si può ottenere lo stesso risultato con il comando [Scour](https://github.com/scour-project/scour):

```bash
scour --set-precision=5 \
      --create-groups \
      --renderer-workaround \
      --remove-descriptive-elements \
      --enable-comment-stripping \
      --enable-viewboxing \
      --indent=space \
      --nindent=1 \
      --no-line-breaks \
      --enable-id-stripping \
      --protect-ids-noninkscape \
      input.svg output.svg
```
