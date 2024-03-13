---
title: Carregamento de imagens
---

Eis algumas regras para contribuir para o Privacy Guides:

## Imagens

- Nós **preferimos** a utilização de imagens SVG, mas se tal não for possível, podem ser usadas imagens PNG

Os logótipos das empresas devem ter um tamanho de tela de:

- 128x128px
- 384x128px

## Otimização

### PNG

Use the [OptiPNG](https://sourceforge.net/projects/optipng) to optimize the PNG image:

```bash
optipng -o7 file.png
```

### SVG

#### Inkscape

[Examine](https://github.com/scour-project/scour) todas as imagens SVG.

No Inkscape:

1. Na aba Ficheiro, selecione Guardar como..
2. Defina o tipo para SVG otimizado (*.svg)

Na aba das **Opções**:

- **Número de dígitos significantes para as coordenadas** > **5**
- [x] Ative **Abreviar valores de cor**
- [x] Ative **Converter atributos CSS em atributos XML**
- [x] Ative **Contrair grupos**
- [x] Ative **Criar grupos para atributos similares**
- [ ] Desative **Manter dados do editor**
- [ ] Desative **Manter definições não referenciadas**
- [x] Ative **Usar recurso alternativo para evitar erros**

Na janela **Exportar em SVG** nas **Opções do documento**:

- [ ] Desative **Remover a declaração XML**
- [x] Ative **Remover metadados**
- [x] Ative **Remover comentários**
- [x] Ative **Embutir imagens raster**
- [x] Ative **Ativar viewBox**

Na janela **Exportar em SVG** em **Impressão organizada**:

- [ ] Desative **Formatar saída com quebras de linha e indentação**
- **Caracteres de indentação** > Selecione **Espaço**
- **Profundidade da indentação** > **1**
- [ ] Desative **Retirar o atributo "xml:space" do elemento SVG raiz**

Na janela **Exportar em SVG** em **IDs**:

- [x] Ative **Remover IDs por usar**
- [ ] Desative **Abreviar IDs**
- **Adicionar prefixo nos IDs abreviados com** > `deixe em branco`
- [x] Ative **Preservar IDs criados manualmente que não terminem com dígitos**
- **Preservar os seguintes IDs** > `deixe em branco`
- **Preservar IDs que começam com** > `deixe em branco`

#### CLI

O mesmo pode ser feito com o comando [Scour](https://github.com/scour-project/scour):

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
