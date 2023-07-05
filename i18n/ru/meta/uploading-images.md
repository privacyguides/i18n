---
title: Загрузка изображений
---

Here are a couple of general rules for contributing to Privacy Guides:

## Изображения

- Мы **предпочитаем** SVG-изображения, но если их нет, мы можем использовать PNG-изображения

Логотипы компании имеют размер холста:

- 128x128px
- 384x128px

## Оптимизация

### PNG

Используйте [OptiPNG](https://sourceforge.net/projects/optipng/) для оптимизации PNG-изображения:

```bash
optipng -o7 file.png
```

### SVG

#### Inkscape

Используйте [Scour](https://github.com/scour-project/scour) для всех SVG-изображений.

В Inkscape:

1. Файл Сохранить как..
2. Установите тип Оптимизированный SVG (*.svg)

In the **Options** tab:

- **Number of significant digits for coordinates** > **5**
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

The same can be achieved with the [Scour](https://github.com/scour-project/scour) command:

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
