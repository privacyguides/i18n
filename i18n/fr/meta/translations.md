---
title: Translations
description: A guide for website contributors on adding translations to our website.
---

Crowdin dispose d'une bonne documentation, et nous vous suggérons de consulter leur guide [Pour bien démarrer](https://support.crowdin.com/crowdin-intro). Notre site est en grande partie rédigé en [Markdown](https://en.wikipedia.org/wiki/Markdown), il devrait donc être facile d'y contribuer. Cette page contient des conseils utiles pour traduire certaines syntaxes spécifiques que vous pouvez rencontrer sur notre site.

Veuillez rejoindre notre salle de localisation sur Matrix ([#pg-i18n:aragon.sh](https://matrix.to/#/%23pg-i18n:aragon.sh)) si vous avez des questions supplémentaires, et lisez notre [article de blog d'annonce](https://blog.privacyguides.org/2023/02/26/i18n-announcement) pour plus d'informations sur le projet.

Notez que la version anglaise du site est la version principale, ce qui signifie que les modifications y sont apportées en premier. Si vous remarquez qu'une langue est en retard par rapport à la version anglaise, n'hésitez pas à nous aider. Nous ne pouvons pas garantir l'exactitude de toutes nos traductions. Si vous avez une suggestion concernant un contenu spécifique à votre région, veuillez ouvrir une issue ou unepull request dans notre [dépôt principal](https://github.com/privacyguides/privacyguides.org).

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

Les systèmes d'écriture CJK ont tendance à utiliser des variantes "pleine largeur" des symboles courants. These are different characters and cannot be used for Markdown syntax.

- Links must use regular parenthesis i.e. `(` (Left Parenthesis U+0028) and `)` (Right Parenthesis U+0029) and not `（` (Fullwidth Left Parenthesis U+FF08) or `）` (Fullwidth Right Parenthesis U+FF09)
- Le texte cité et en retrait doit utiliser `:` (deux-points U+003A) et non `：` (deux-points pleine largeur U+FF1A)
- Les images doivent utiliser `!` (point d'exclamation U+0021) et non `！` (point d'exclamation pleine largeur U+FF01)
