---
title: Uploading Images
description: A guide for website contributors on uploading images in the proper format and location.
---

If you make changes to this website that involve adding new images or replacing existing ones, here are a couple of general recommendations:

## Gambar

- We **prefer** SVG images, but if those do not exist we can use PNG images. Additionally, for cover images, we prefer that they are obtained from [Unsplash](https://unsplash.com) and are in the WebP format.

Company logos should be square if possible, and at least 200x200px if they are PNGs (non-vector images).

## Optimasi

### PNG

Use the [OptiPNG](https://sourceforge.net/projects/optipng) tool to optimize PNG images:

```bash
optipng -o7 file.png
```

### SVG

#### Inkscape

*[Scour](https://github.com/scour-project/scour)* semua gambar SVG.

Dalam Inkscape:

1. File > Save As...
2. Set type to: Optimized SVG (*.svg)

Pada tab **Opsi**:

- **Jumlah digit signifikan untuk koordinat** > **5**
- [x] Aktifkan **Persingkat nilai warna**
- [x] Aktifkan **Konversi atribut CSS ke atribut XML**
- [x] Aktifkan **Runtuhkan grup**
- [x] Aktifkan **Buat grup untuk atribut serupa**
- [ ] Matikan **Simpan data editor**
- [ ] Matikan **Simpan definisi yang tidak direferensikan**
- [x] Hidupkan **Bekerja di sekitar bug renderer**

Pada tab **SVG Output** di bawah **Opsi dokumen**:

- [ ] Matikan **Hapus deklarasi XML**
- [x] Aktifkan **Hapus metadata**
- [x] Aktifkan **Hapus komentar**
- [x] Turn on **Embedded raster images**
- [x] Aktifkan **Aktifkan viewboxing**

Pada tab **SVG Output** di bawah **Opsi dokumen**:

- [ ] Matikan **Format keluaran dengan pemisah baris dan indentasi**
- **Intentasi karakter** > Pilih **Spasi**
- **Kedalaman indentasi** > **1**
- [ ] Matikan **Hapus atribut "xml:space" dari elemen SVG akar**

Pada tab **IDs**:

- [x] Aktifkan **Hapus ID yang tidak digunakan**
- [] Nonaktifkan **Persingkat ID**
- **Awalan ID singkat dengan** > `biarkan kosong`
- [x] Nyalakan **Simpan ID yang dibuat secara manual yang tidak diakhiri dengan angka**
- **Awalan ID singkat dengan** > `biarkan kosong`
- **Simpan ID yang dimulai dengan** > `biarkan kosong`

#### CLI

Hal yang sama dapat dicapai dengan perintah [Scour](https://github.com/scour-project/scour):

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

### WebP

Use the [`cwebp`](https://developers.google.com/speed/webp/docs/using) command to convert PNG or JPEG image files to WebP format:

```bash
cwebp -m 6 input_file -o output.webp
```
