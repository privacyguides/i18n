---
title: Subir Imágenes
description: Una guía para los colaboradores del sitio web sobre la subida de imágenes en el formato y ubicación adecuados.
---

Si realiza cambios a este sitio web donde se requiera agregar nuevas imágenes o reemplazar las existentes, aquí tiene un par de recomendaciones generales:

## Imágenes

- **Preferimos** las imágenes SVG, pero si no existen podemos usar imágenes PNG. Además, para las imágenes de portada, preferimos que sean obtenidas de [Unsplash](https://unsplash.com) y estén en formato WebP.

Los logotipos de empresa deben ser cuadrados si es posible, y de al menos 200x200px si son PNG (imágenes no vectoriales).

## Optimización

### PNG

Use la herramienta [OptiPNG](https://sourceforge.net/projects/optipng) para optimizar las imágenes PNG:

```bash
optipng -o7 file.png
```

### SVG

#### Inkscape

[Explora](https://github.com/scour-project/scour) todas las imágenes SVG.

En Inkscape:

1. Archivo > Guardar Como...
2. Establecer tipo a: SVG optimizado (*.svg)

En la pestaña **Opciones**:

- **Número de cifras significativas para las coordenadas** > **5**
- [x] Activar **Acortar valores de color**
- [x] Activar **Convertir atributos CSS a atributos XML**
- [x] Activar **Colapsar grupos**
- [x] Activar **Crear grupos para atributos similares**
- [ ] Desactivar **Conservar datos del editor**
- [ ] Desactivar **Mantener definiciones no referenciadas**
- [x] Activar **Solucionar errores del renderizador**

En la pestaña **Salida SVG** bajo **Opciones de documento**:

- [ ] Desactivar **Eliminar la declaración XML**
- [x] Activar **Eliminar metadatos**
- [x] Activar **Eliminar comentarios**
- [x] Activar **Imágenes Rasterizadas Incrustadas**
- [x] Activar **Activar viewboxing**

En la **salida SVG** bajo **Pretty-printing**:

- [ ] Desactivar **Formato de salida con saltos de línea y sangría**
- **Caracteres de sangría** > Seleccionar **Espacio**
- **Profundidad de sangría** > **1**
- [ ] Desactivar **Eliminar el atributo "xml:space" del elemento SVG raíz**

En la pestaña **IDs**:

- [x] Activar **Eliminar ID no utilizados**
- [ ] Desactivar **Acortar IDs**
- **Prefijo de IDs acortadas con** > `dejar en blanco`
- [x] Activar **Conservar ID creados manualmente que no terminen con dígitos**
- **Conservar los siguientes IDs** > `dejar en blanco`
- **Conservar IDs que empiezan por** > `dejar en blanco`

#### CLI

Lo mismo puede conseguirse con el comando [Scour](https://github.com/scour-project/scour):

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
