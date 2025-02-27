---
title: "Introduction aux mots de passe"
icon: 'material/form-textbox-password'
description: Voici quelques conseils et astuces pour créer des mots de passe plus forts et sécuriser vos comptes.
---

Les mots de passe sont un élément essentiel de notre vie numérique quotidienne. Nous les utilisons pour protéger nos comptes, nos appareils et nos secrets. Bien qu'ils soient souvent la seule chose qui nous sépare d'un adversaire qui en veut à nos informations privées, ils ne font pas l'objet d'une réflexion approfondie, ce qui conduit souvent les gens à utiliser des mots de passe faciles à deviner ou à forcer.

## Bonnes pratiques

### Utiliser des mots de passe uniques pour chaque service

Imaginez ceci : vous vous inscrivez à un compte avec le même e-mail et le même mot de passe sur plusieurs services en ligne. Si l'un de ces fournisseurs de services est malveillant ou si son service subit une fuite de données qui expose votre mot de passe dans un format non chiffré, il suffit à un acteur malveillant d'essayer cette combinaison d'e-mail et de mot de passe sur plusieurs services populaires jusqu'à ce qu'il obtienne un résultat. La force de ce mot de passe n'a pas d'importance, car ils l'ont déjà.

C'est ce qu'on appelle le [bourrage d'identifiants](https://en.wikipedia.org/wiki/Credential_stuffing), et c'est l'une des façons les plus courantes dont vos comptes peuvent être compromis par des cybercriminels. Pour éviter cela, assurez-vous de ne jamais réutiliser vos mots de passe.

### Utilisez des mots de passe générés de manière aléatoire

==Vous ne devez **jamais** compter sur vous-même pour trouver un bon mot de passe.== Nous vous recommandons d'utiliser [des mots de passe générés de manière aléatoire](#passwords) ou [des phrases secrètes de type "diceware"](#diceware-passphrases) avec une entropie suffisante pour protéger vos comptes et vos appareils.

Tous nos [gestionnaires de mots de passe recommandés](../passwords.md) comprennent un générateur de mots de passe intégré que vous pouvez utiliser.

### Rotation des mots de passe

Vous devez éviter de changer trop souvent les mots de passe que vous devez retenir (comme le mot de passe principal de votre gestionnaire de mots de passe), sauf si vous avez des raisons de penser qu'ils ont été compromis, car le fait de les changer trop souvent vous expose au risque de les oublier.

When it comes to passwords that you don't have to remember (such as passwords stored inside your password manager), if your [threat model](threat-modeling.md) calls for it, we recommend going through important accounts (especially accounts that don't use multifactor authentication) and changing their password every couple of months, in case they have been compromised in a data breach that hasn't become public yet. La plupart des gestionnaires de mots de passe vous permettent de fixer une date d'expiration pour votre mot de passe afin d'en faciliter la gestion.

<div class="admonition tip" markdown>
<p class="admonition-title">Vérifier les fuites/violations de données</p>

Si votre gestionnaire de mots de passe vous permet de vérifier les mots de passe compromis, assurez-vous de le faire et changez rapidement tout mot de passe qui pourrait avoir été exposé dans une fuite de données. Vous pouvez également suivre le flux [Dernières Brèches de Have I Been Pwned](https://feeds.feedburner.com/HaveIBeenPwnedLatestBreaches) à l'aide d'un [agrégateur d'actualités](../news-aggregators.md).

</div>

## Créer des mots de passe forts

### Mots de passe

De nombreux services imposent certains critères en ce qui concerne les mots de passe, notamment une longueur minimale ou maximale, ainsi que les caractères spéciaux qui peuvent être utilisés le cas échéant. Vous devez utiliser le générateur de mots de passe intégré à votre gestionnaire de mots de passe pour créer des mots de passe aussi longs et complexes que le service le permet en incluant des lettres majuscules et minuscules, des chiffres et des caractères spéciaux.

Si vous avez besoin d'un mot de passe que vous pouvez mémoriser, nous vous recommandons la [phrase secrète diceware](#diceware-passphrases).

### Phrases secrètes Diceware

Diceware est une méthode permettant de créer des phrases secrètes faciles à retenir, mais difficiles à deviner.

Les phrases secrètes Diceware sont une excellente option lorsque vous devez mémoriser ou saisir manuellement vos informations d'identification, par exemple pour le mot de passe principal de votre gestionnaire de mots de passe ou le mot de passe de chiffrement de votre appareil.

Un exemple de phrase secrète diceware est `viewable fastness reluctant squishy seventeen shown pencil`.

Pour générer une phrase secrète diceware à l'aide de vrais dés, suivez ces étapes :

<div class="admonition Note" markdown>
<p class="admonition-title">Note</p>

These instructions assume that you are using [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) to generate the passphrase, which requires five dice rolls per word. Other word lists may require more or less rolls per word, and may require a different amount of words to achieve the same entropy.

</div>

1. Lancez cinq fois un dé à six faces, en notant le nombre après chaque lancer.

2. Par exemple, disons que vous avez obtenu `2-5-2-6-6`. Look through the [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) for the word that corresponds to `25266`.

3. Vous trouverez le mot `encrypt`. Notez ce mot.

4. Répétez ce processus jusqu'à ce que votre phrase secrète comporte autant de mots que nécessaire, que vous devez séparer par un espace.

<div class="admonition warning" markdown>
<p class="admonition-title">Important</p>

Vous ne devez **pas** relancer les mots jusqu'à ce que vous obteniez une combinaison de mots qui vous plaît. Le processus doit être complètement aléatoire.

</div>

Si vous n'avez pas accès à de vrais dés ou si vous préférez ne pas en utiliser, vous pouvez utiliser le générateur de mots de passe intégré à votre gestionnaire de mots de passe, car la plupart d'entre eux ont la possibilité de générer des phrases secrètes diceware en plus des mots de passe ordinaires.

We recommend using [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) to generate your diceware passphrases, as it offers the exact same security as the original list, while containing words that are easier to memorize. There are also [word lists in different languages](https://theworld.com/~reinhold/diceware.html#Diceware%20in%20Other%20Languages|outline), if you do not want your passphrase to be in English.

<details class="note" markdown>
<summary>Explication de l'entropie et de la force des phrases secrètes diceware</summary>

To demonstrate how strong diceware passphrases are, we'll use the aforementioned seven word passphrase (`viewable fastness reluctant squishy seventeen shown pencil`) and [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) as an example.

L'une des mesures permettant de déterminer la force d'une phrase secrète est son degré d'entropie. L'entropie par mot d'une phrase secrète est calculée comme suit <math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <mtext>MotsDansLaListe</mtext> <mo form="postfix" stretchy="false">)</mo> </mrow> </math> et l'entropie globale de la phrase secrète est calculée comme suit : <math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <msup> <mtext>MotsDansLaListe</mtext> <mtext>MotsDansLaPhrase</mtext> </msup> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>

Par conséquent, chaque mot de la liste susmentionnée représente ~12,9 bits d'entropie (<math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <mn>7776</mn> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>), et une phrase secrète de sept mots dérivée de celle-ci a ~90,47 bits d'entropie (<math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <msup> <mn>7776</mn> <mn>7</mn> </msup> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>).

The [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) contains 7776 unique words. Pour calculer le nombre de phrases secrètes possibles, il suffit de faire ce qui suit <math> <msup> <mtext>MotsDansLaListe</mtext> <mtext>MotsDansLaPhrase</mtext> </msup> </math>ou dans notre cas, <math><msup><mn>7776</mn><mn>7</mn></msup></math>.

Let's put all of this in perspective: A seven word passphrase using [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) is one of ~1,719,070,799,748,422,500,000,000,000 possible passphrases.

En moyenne, il faut essayer 50 % de toutes les combinaisons possibles pour deviner votre phrase. En gardant cela à l'esprit, même si votre adversaire est capable de faire ~1 000 000 000 000 de suppositions par seconde, il lui faudrait toujours ~27 255 689 ans pour deviner votre phrase secrète. C'est le cas même si les choses suivantes sont vraies :

- Votre adversaire sait que vous avez utilisé la méthode du diceware.
- Your adversary knows the specific word list that you used.
- Votre adversaire sait combien de mots contient votre phrase secrète.

</details>

Pour résumer, les phrases secrètes diceware sont votre meilleure option lorsque vous avez besoin d'une phrase à la fois facile à retenir *et* exceptionnellement forte.

## Stockage des mots de passe

### Gestionnaires de mots de passe

La meilleure façon de stocker vos mots de passe est d'utiliser un gestionnaire de mots de passe. Ils vous permettent de stocker vos mots de passe dans un fichier ou dans le cloud et de les protéger avec un seul mot de passe principal. Ainsi, vous n'aurez à retenir qu'un seul mot de passe fort, qui vous permettra d'accéder aux autres.

Il existe de nombreuses options intéressantes, qu'elles soient basées sur le cloud ou locales. Choisissez l'un de nos gestionnaires de mots de passe recommandés et utilisez-le pour établir des mots de passe forts pour tous vos comptes. Nous vous recommandons de sécuriser votre gestionnaire de mots de passe avec une [phrase secrète diceware](#diceware-passphrases) composée d'au moins sept mots.

[Liste des gestionnaires de mots de passe recommandés](../passwords.md ""){.md-button}

<div class="admonition warning" markdown>
<p class="admonition-title">Ne placez pas vos mots de passe et vos codes TOTP dans le même gestionnaire de mots de passe</p>

When using [TOTP codes as multifactor authentication](multi-factor-authentication.md#time-based-one-time-password-totp), the best security practice is to keep your TOTP codes in a [separate app](../multi-factor-authentication.md).

Le stockage de vos codes TOTP au même endroit que vos mots de passe, bien que pratique, réduit les comptes à un seul facteur dans le cas où un adversaire aurait accès à votre gestionnaire de mots de passe.

En outre, nous ne recommandons pas de stocker des codes de récupération à usage unique dans votre gestionnaire de mots de passe. Ils doivent être stockés séparément, par exemple dans un conteneur chiffré sur un dispositif de stockage hors ligne.

</div>

### Sauvegardes

Vous devriez conserver une sauvegarde [chiffrée](../encryption.md) de vos mots de passe sur plusieurs dispositifs de stockage ou sur un fournisseur de stockage cloud. Cela peut vous aider à accéder à vos mots de passe si quelque chose arrive à votre appareil principal ou au service que vous utilisez.
