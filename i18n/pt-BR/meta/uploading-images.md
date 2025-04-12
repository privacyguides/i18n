---
title: Fazendo *upload* de imagens
description: Esse é um guia para os contribuidores do site para subir imagens no padrão e caminho (pasta no diretório do site) corretos.
---

Se você fizer mudanças nesse website que envolvam adicionar novos arquivos de imagem ou até substituir arquivos existentes, aqui estão algumas recomendações:

## Imagens

- Nós **preferimos** imagens no formato SVG, mas se elas não existirem, você  também pode subir em PNG. Além disso, para imagens de capa, preferimos que elas sejam provenientes do serviço [Unsplash](https://unsplash.com) e que estejam no formato WebP.

Os logotipos da empresa devem ser quadrados, se possível, e ter pelo menos 200x200px se forem PNGs (imagens não-vetorizadas).

## Otimização

### PNG

Use a ferramenta [OptiPNG](https://sourceforge.net/projects/optipng) para otimizar imagens PNG:

```bash
optipng -o7 file.png
```

### SVG

#### Inkscape

[Examine](https://github.com/scour-project/scour) Todas as imagens no formato SVG.

No Inkscape:

1. Arquivo > Salvar como...
2. Definir o tipo como: SVG otimizado (*.svg)

Na guia **Opções**:

- **Número de dígitos significativos para coordenadas** > **5**
- [x] Ativar a opção **Reduzir valores de cor**
- [x] Ative a opção **Converter atributos CSS em atributos XML**
- [x] Ativar **grupos de recolhimento**
- [Ative a opção **Criar grupos para atributos semelhantes**
- [ ] Desativar **Manter dados do editor**
- [Desativar **Manter definições não referenciadas**
- [x] Ativar a opção Contornar **bugs do renderizador**

Na guia **Saída SVG**, em **Opções do documento**:

- [Desligar **Remover a declaração XML**
- [x] Ativar a opção **Remover metadados**
- [x] Ativar a opção **Remover comentários**
- [x] Ativar **imagens raster incorporadas**
- [x] Ative **a opção Ativar caixa de visualização**

Na **saída SVG**, em **Pretty-printing**:

- [ ] Desativar **Formatar saída com quebras de linha, indentação e recuo**
- **Caracteres de recuo** > Selecionar **espaço**
- **Profundidade de indentação** > **1**
- [ **Desativar o atributo "xml:space" do elemento SVG raiz**

Na guia **IDs**:

- [x] Ativar a opção **Remover IDs não utilizados**
- [ ] Desativar **Encurtar IDs**
- **Prefixar IDs abreviados com** > `deixar em branco`
- [x] Ativar **Preservar IDs criadas manualmente que não terminam com dígitos**
- **Preserve as seguintes IDs** > `deixar em branco`
- **Preservar IDs que começam com** > `deixar em branco`

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

### WebP

Use the [`cwebp`](https://developers.google.com/speed/webp/docs/using) command to convert PNG or JPEG image files to WebP format:

```bash
cwebp -m 6 input_file -o output.webp
```
