---
title: Traduções
description: Um guia para os tradutores do projeto.
---

A Crowdin tem uma boa documentação que pode ser encontrada na página [Guia Inicial](https://support.crowdin.com/crowdin-intro). Nosso site é majoritariamente escrito em [Markdown](https://en.wikipedia.org/wiki/Markdown), portanto, deve ser fácil contribuir. Essa página contem algumas dicas importantes para traduzir alguns termos específicos que você pode encontrar em nossas páginas.

Entre em contato no nosso servidor na Matrix ([#pg-i18n:aragon.sh](https://matrix.to/#/%23pg-i18n:aragon.sh)) caso tenha alguma dúvida adicional e leia nossos[anúnicos no blog](https://blog.privacyguides.org/2023/02/26/i18n-announcement) para informações adicionais sobre o projeto.

Note que a versão em **inglês** do site é a versão principal onde provavelmente mudanças ocorrerão primeiro. Se você notar algum idioma que está 'ficando para trás' em relação à instância em inglês, por favor nos ajude. Não podemos garantir a exatidão de todas as traduções. Se você tem alguma sugestão sobre um conteúdo específico para sua região, por favor, abra um problema ou pull request para nosso [repositório principal](https://github.com/privacyguides/privacyguides.org).

## Saída de Tradução (automatizada)

Os *softwares* de tradução tem uma precisão consideravelmente aceitável, porém, você deve checar se as *strings* (frases e termos) foram traduzidas corretamente.

Exemplo:

```text
![Shelter logo](assets/img/path/to/image.svg){ align=right }
```

Às vezes, descobrimos que a sintaxe para inserir uma imagem como a situação acima se dá por erros com espaços extras entre o texto e o caminho do arquivo. Se uma frase ou termo traduzido claramente não estiver correta ou em corcodância com o conteúdo original, recomendamos que você **exclua** pressionando o ícone da lixeira [ou vote](https://support.crowdin.com/enterprise/getting-started-for-volunteers/#voting-view) na que achar melhor. Quando  *strings* de caracteres inválidas são excluídas, elas também serão removidas da [memória de tradução](https://support.crowdin.com/enterprise/translation-memory) da organização, o que significa que, quando a cadeia de caracteres de origem for vista novamente, ela não sugerirá esta mesma tradução incorreta.

## Pontuação

Para exemplos como as advertências acima, as aspas, por exemplo: `" "` devem ser usadas para especificar o texto da string. O MkDocs não interpretará corretamente outros símbolos, ou seja, 「 `」` ou `" ".` Outros sinais de pontuação são adequados para marcar citações regulares dentro do texto.

## Alternativas de sintaxe longa e Markdown

Os sistemas de escrita CJK tendem a usar variantes alternativas de "largura total" de símbolos comuns. Estes são caracteres diferentes e não podem ser usados para sintaxe Markdown.

- Os links devem usar parênteses regulares, ou seja, `(` (Parêntese esquerdo U+0028) e `)` (Parêntese direito U+0029) e não `（` (Fullwidth Left Parenthesis U+FF08) ou `）` (Fullwidth Right Parenthesis U+FF09)
- O texto entre aspas com recuo deve usar `:` (dois pontos U+003A) e não `：` (Fullwidth Colon U+FF1A)
- As imagens devem usar `!` (Ponto de exclamação U+0021) e não `！` (Ponto de exclamação de largura total U+FF01)
