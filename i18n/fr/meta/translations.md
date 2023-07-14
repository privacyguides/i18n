---
title: Traductions
---

Crowdin dispose d'une bonne documentation, et nous vous suggérons de consulter leur guide [Getting Started](https://support.crowdin.com/crowdin-intro/) . Notre site est en grande partie rédigé en [Markdown](https://en.wikipedia.org/wiki/Markdown), il devrait donc être facile d'y contribuer. Cette page contient des conseils utiles pour traduire certaines syntaxes spécifiques que vous pouvez rencontrer sur notre site.

Veuillez rejoindre notre salle de localisation sur Matrix ([#pg-i18n:aragon.sh](https://matrix.to/#/%23pg-i18n:aragon.sh)) si vous avez des questions supplémentaires, et lisez notre [article de blog d'announce](https://blog.privacyguides.org/2023/02/26/i18n-announcement/) pour plus d'informations sur le projet.

Notez que la version anglaise du site est la version principale, ce qui signifie que les modifications y sont apportées en premier. Si vous remarquez qu'une langue est en retard par rapport à la version anglaise, n'hésitez pas à nous aider. Nous ne pouvons pas garantir l'exactitude de toutes nos traductions. Si vous avez une suggestion concernant un contenu spécifique à votre région, veuillez ouvrir une issue ou unepull request dans notre [dépôt principal](https://github.com/privacyguides/privacyguides.org).

## Admonitions

Tout au long du site, nous utilisons les [admonitions](https://squidfunk.github.io/mkdocs-material/reference/admonitions/#usage) de MkDocs, pour montrer des informations aux lecteurs. Ils se présentent sous différentes formes telles que `example`, `warning`, `tip`, etc.

Lorsque les admonitions sont utilisées, elles sont accompagnées par défaut d'une chaîne de caractères en anglais sur le site. Il est possible de les [personnaliser](https://squidfunk.github.io/mkdocs-material/reference/admonitions/#changing-the-title), sans trop d'efforts. Par exemple, si vous traduisez en néerlandais une admonition du type [`warning`](https://squidfunk.github.io/mkdocs-material/reference/admonitions/#type:warning) , voici comment vous l'écrirez :

=== "Traduction en néerlandais"

    ```text
    !!! warning "Waarschuwing"
    ```

=== "Texte source en anglais"

    ```text
    !!! warning "Avertissement"
    ```

Les téléchargements sont une [admonition personnalisée](https://squidfunk.github.io/mkdocs-material/reference/admonitions/#custom-admonitions) qui s'écrit comme suit :

=== "Traduction en néerlandais"

    ```text
    ??? downloads "Downloaden"
    ```

=== "Texte source en anglais"

    ```text
    ??? downloads
    ```

Il en va de même pour d'autres types, tels que `tip`, `example`, `warning`, `danger` etc.

Les recommandations sont un type particulier d'admonition qui ne nécessite **pas** de personnalisation car elles n'ont pas de texte visible et ne sont donc jamais modifiées :

=== "Traduction en néerlandais"

    ```text
    !!! recommendation
    ```

=== "Texte source en anglais"

    ```text
    !!! recommendation
    ```

## Sortie de traduction

Les logiciels de traduction permettent d'obtenir des traductions assez précises, mais vous devez vous assurer que la chaîne traduite est correcte.

Par exemple :

```text
![Logo du logiciel](assets/img/path/to/image.svg){ align=right }
```

Nous avons parfois constaté que la syntaxe pour l'insertion d'une image comme ci-dessus manquait le `![` ou qu'un espace supplémentaire était placé entre le texte et le chemin, par exemple `](`. Si une chaîne de traduction n'est manifestement pas correcte, nous vous encourageons à la **supprimer** en appuyant sur l'icône de la corbeille [ou à voter](https://support.crowdin.com/enterprise/getting-started-for-volunteers/#voting-view) pour celle qui vous semble la meilleure. Lorsque les chaînes invalides sont supprimées, elles sont retirées de la [mémoire de traduction](https://support.crowdin.com/enterprise/translation-memory) de l'organisation, ce qui signifie que lorsque la chaîne source sera vue à nouveau, elle ne suggérera pas la traduction incorrecte.

## Ponctuation

Pour des exemples tels que les admonitions ci-dessus, les guillemets, par exemple : `" "` doivent être utilisés pour spécifier un texte sous forme de chaîne. MkDocs n'interprète pas correctement les autres symboles, par exemple `「 」` ou `« »`. Les autres signes de ponctuation conviennent pour marquer les citations régulières dans le texte.

## Alternatives en pleine largeur et syntaxe Markdown

Les systèmes d'écriture CJK ont tendance à utiliser des variantes "pleine largeur" des symboles courants. Il s'agit de caractères différents qui ne peuvent pas être utilisés pour la syntaxe Markdown.

- Les liens doivent utiliser des parenthèses normales, c'est-à-dire `(` (parenthèse gauche U+0028) et `)` (parenthèse droite U+0029) et non `（` (parenthèse gauche pleine largeur U+FF08) ou `）` (parenthèse droite pleine largeur U+FF09)
- Le texte cité et en retrait doit utiliser `:` (deux-points U+003A) et non `：` (deux-points pleine largeur U+FF1A)
- Les images doivent utiliser `!` (point d'exclamation U+0021) et non `！` (point d'exclamation pleine largeur U+FF01) 
