---
title: Uploading Images
description: A guide for website contributors on uploading images in the proper format and location.
---

If you make changes to this website that involve adding new images or replacing existing ones, here are a couple of general recommendations:

## Изображения

- We **prefer** SVG images, but if those do not exist we can use PNG images. Additionally, for cover images, we prefer that they are obtained from [Unsplash](https://unsplash.com) and are in the WebP format.

Company logos should be square if possible, and at least 200x200px if they are PNGs (non-vector images).

## Оптимизация

### PNG

Use the [OptiPNG](https://sourceforge.net/projects/optipng) tool to optimize PNG images:

```bash
optipng -o7 file.png
```

### SVG

#### Inkscape

Используйте [Scour](https://github.com/scour-project/scour) для всех SVG-изображений.

В Inkscape:

1. File > Save As...
2. Set type to: Optimized SVG (*.svg)

На вкладке **Параметры**:

- **Количество значащих цифр для координат** > **5**
- [x] Включите **Укорачивать значения цвета**
- [x] Включите **Преобразовывать атрибуты CSS в атрибуты XML**
- [x] Включите **Сворачивать группы**
- [x] Включите **Создавать группы для похожих атрибутов**
- [ ] Выключите **Сохранять данные редактора**
- [ ] Выключите **Сохранять определения без ссылок**
- [x] Включите **Обход ошибок обработчика**

На вкладке **Экспорт в SVG** в разделе **Параметры документа**:

- [ ] Выключите **Удалить объявление XML**
- [x] Включите **Удалить метаданные**
- [x] Включите **Удалить комментарии**
- [x] Включите **Встроить растровые изображения**
- [x] Включите **Включить viewbox**

На вкладке **Экспорт в SVG** в разделе **Качественная печать**:

- [ ] Выключите **Форматировать вывод с разрывами строк и отступами**
- **Символы отступа** > Выберите **Пробел**
- **Размер отступа** > **1**
- [ ] Выключить **Вырезать атрибут "xml:space" из корневого элемента SVG**

На вкладке **Идентификаторы**:

- [x] Включите **Удалить неиспользуемые идентификаторы**
- [ ] Отключите **Сократить идентификаторы**
- **Предварять сокращённые идентификаторы** > `оставьте пустым`
- [x] Включите **Сохранять созданные вручную идентификаторы, не заканчивающиеся цифрами**
- **Сохранять следующие идентификаторы** > `оставьте пустым`
- **Сохранять идентификаторы, начинающиеся с** > `оставьте пустым`

#### Интерфейс командной строки (CLI)

Того же можно добиться с помощью команды [Scour](https://github.com/scour-project/scour):

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

Use the [cwebp](https://developers.google.com/speed/webp/docs/using) command to convert PNG or JPEG image files to WebP format:

```bash
cwebp -q 70 -m 6 input_file -o output.webp
```
