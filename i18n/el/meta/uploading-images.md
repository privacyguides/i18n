---
title: Ανέβασμα Εικονών
---

Ακολουθούν μερικοί γενικοί κανόνες για τη συνεισφορά στο Privacy Guides:

## Εικόνες

- **Προτιμούμε** εικόνες SVG, αλλά αν δεν υπάρχουν, μπορούμε να χρησιμοποιήσουμε εικόνες PNG.

Τα λογότυπα εταιρειών έχουν μέγεθος καμβά:

- 128x128px
- 384x128px

## Βελτιστοποίηση

### PNG

Χρησιμοποίησε το [OptiPNG](https://sourceforge.net/projects/optipng) για να βελτιστοποιήσεις την εικόνα PNG:

```bash
optipng -o7 file.png
```

### SVG

#### Inkscape

[Scour](https://github.com/scour-project/scour)αρε όλες τις SVG εικόνες.

Στο Inkscape:

1. Αποθήκευση Αρχείου ως..
2. Όρισε τύπο σε βελτιστοποιημένο SVG (*.svg)

Στην καρτέλα **Options**:

- **Number of significant digits for coordinates** > **5**
- [x] Ενεργοποιήστε **Shorten color values**
- [x] Ενεργοποιήστε **Convert CSS attributes to XML attributes**
- [x] Ενεργοποιήστε **Collapse groups**
- [x] Ενεργοποιήστε **Create groups for similar attributes**
- [ ] Απενεργοποιήστε **Keep editor data**
- [ ] Απενεργοποιήστε **Keep unreferenced definitions**
- [x] Ενεργοποιήστε **Work around renderer bugs**

Στην καρτέλα **SVG Output** στις επιλογές εγγράφου ****:

- [ ] Απενεργοποιήστε **Remove the XML declaration**
- [x] Ενεργοποιήστε **Remove metadata**
- [x] Ενεργοποιήστε **Remove comments**
- [x] Ενεργοποιήστε **Embeded raster images**
- [x] Ενεργοποιήστε **Enable viewboxing**

Στην καρτέλα **SVG Output** στις επιλογές εγγράφου **Pretty-printing**:

- [ ] Απενεργοποίηση της επιλογής **Format output with line-breaks and indentation**
- **Indentation characters** > Επιλέξτε **Space**
- **Depth of indentation** > **1**
- [ ] Απενεργοποιήστε **Strip the "xml:space" attribute from the root SVG element**

Στην καρτέλα **IDs**:

- [x] Ενεργοποιήστε **Remove unused IDs**
- [ ] Απενεργοποιήστε **Shorten IDs**
- **Prefix shortened IDs with** > `αφήστε το κενό`
- [x] Ενεργοποιήστε **Preserve manually created IDs not ending with digits**
- **Preserve the following IDs** > `αφήστε το κενό`
- **Preserve IDs starting with** > `αφήστε το κενό`

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
