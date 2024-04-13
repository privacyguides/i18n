---
title: Μεταφόρτωση Εικόνων
---

Εδώ είναι μερικοί γενικοί κανόνες για τη συνεισφορά στο Privacy Guides:

## Εικόνες

- **Προτιμούμε** εικόνες SVG, αλλά αν δεν υπάρχουν, μπορούμε να χρησιμοποιήσουμε εικόνες PNG.

Τα λογότυπα της εταιρείας έχουν μέγεθος καμβά:

- 128x128px
- 384x128px

## Βελτιστοποίηση

### PNG

Χρησιμοποιήστε το [OptiPNG](https://sourceforge.net/projects/optipng) για να βελτιστοποιήσετε την εικόνα PNG:

```bash
optipng -o7 file.png
```

### SVG

#### Inkscape

[Scour](https://github.com/scour-project/scour) all SVG images.

Στο Inkscape:

1. Αρχείο Αποθήκευση ως..
2. Ορισμός τύπου σε βελτιστοποιημένο SVG (*.svg)

Στην καρτέλα **Options**:

- **Number of significant digits for coordinates** > **5**
- [x] Turn on **Shorten color values**
- [x] Turn on **Convert CSS attributes to XML attributes**
- [x] Turn on **Collapse groups**
- [x] Turn on **Create groups for similar attributes**
- [ ] Turn off **Keep editor data**
- [ ] Turn off **Keep unreferenced definitions**
- [x] Turn on **Work around renderer bugs**

Στην καρτέλα **SVG Output** στις επιλογές εγγράφου ****:

- [ ] Απενεργοποίηση **Remove the XML declaration**
- [x] Ενεργοποίηση της λειτουργίας **Remove metadata**
- [x] Ενεργοποίηση της λειτουργίας **Remove metadata**
- [x] Ενεργοποίηση **Embeded raster image**
- [x] Ενεργοποίηση **Enable viewboxing**

Στην καρτέλα **SVG Output** στις επιλογές εγγράφου **Pretty-printing**:

- [ ] Απενεργοποίηση της επιλογής **Format output with line-breaks and indentation**
- **Χαρακτήρες εσοχής** > Επιλέξτε **Space**
- **Depth of indentation** > **1**
- [ ] Απενεργοποίηση **Strip the "xml:space" attribute from the root SVG element**

Στην καρτέλα **IDs**:

- [x] Turn on **Remove unused IDs**
- [ ] Turn off **Shorten IDs**
- **Prefix shortened IDs with** > `leave blank`
- [x] Turn on **Preserve manually created IDs not ending with digits**
- **Preserve the following IDs** > `leave blank`
- **Preserve IDs starting with** > `leave blank`

#### CLI

Το ίδιο μπορεί να επιτευχθεί με την εντολή [Scour](https://github.com/scour-project/scour):

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
