---
title: 画像のアップロード
---

プライバシーガイドに投稿する際の一般的なルールをいくつか紹介します：

## 画像

- 私たちはSVG画像を**推奨**しますが、存在しない場合は PNG 画像を使用できます

企業ロゴのキャンバスサイズ：

- 128x128px
- 384x128px

## 最適化

### PNG

[OptiPNG](https://sourceforge.net/projects/optipng/)を使用してPNG画像を最適化します。

```bash
optipng -o7 file.png
```

### SVG

#### Inkscape

すべてのSVG画像に[Scour](https://github.com/scour-project/scour)を使用します。

Inkscapeで：

1. 名前を付けてファイルを保存...
2. タイプを最適化されたSVG (*.svg)に設定する

**オプション** タブで：

- **座標の有効桁数** > **5**
- [x] Turn on **Shorten color values**
- [x] Turn on **Convert CSS attributes to XML attributes**
- [x] Turn on **Collapse groups**
- [x] Turn on **Create groups for similar attributes**
- [ ] Turn off **Keep editor data**
- [ ] Turn off **Keep unreferenced definitions**
- [x] Turn on **Work around renderer bugs**

In the **SVG Output** tab under **Document options**:

- [ ] Turn off **Remove the XML declaration**
- [x] Turn on **Remove metadata**
- [x] Turn on **Remove comments**
- [x] Turn on **Embeded raster images**
- [x] Turn on **Enable viewboxing**

In the **SVG Output** under **Pretty-printing**:

- [ ] Turn off **Format output with line-breaks and indentation**
- **Indentation characters** > Select **Space**
- **Depth of indentation** > **1**
- [ ] Turn off **Strip the "xml:space" attribute from the root SVG element**

In the **IDs** tab:

- [x] Turn on **Remove unused IDs**
- [ ] Turn off **Shorten IDs**
- **Prefix shortened IDs with** > `leave blank`
- [x] Turn on **Preserve manually created IDs not ending with digits**
- **Preserve the following IDs** > `leave blank`
- **Preserve IDs starting with** > `leave blank`

#### CLI

同じことが [Scour](https://github.com/scour-project/scour) コマンドでも可能です：

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
