---
title: "Idées reçues"
icon: 'material/robot-confused'
description: La protection de la vie privée n'est pas un sujet simple, et il est facile de se laisser piéger par les affirmations marketing et autres désinformations.
schema:
  - 
    "@context": https://schema.org
    "@type": FAQPage
    mainEntity:
      - 
        "@type": Question
        name: Les logiciels libres sont-ils intrinsèquement sûrs ?
        acceptedAnswer:
          "@type": Answer
          text: |
            Le fait que le code source soit disponible et la manière dont le logiciel est concédé sous licence n'ont pas d'incidence intrinsèque sur sa sécurité. Les logiciels libres ont le potentiel d'être plus sûrs que les logiciels propriétaires, mais il n'y a aucune garantie que ce soit le cas. Lorsque vous évaluez un logiciel, vous devez examiner la réputation et la sécurité de chaque outil au cas par cas.
      - 
        "@type": Question
        name: Déplacer la confiance vers un autre fournisseur peut-il améliorer la vie privée ?
        acceptedAnswer:
          "@type": Answer
          text: |
            Nous parlons souvent de "déplacement de confiance" lorsque nous abordons des solutions telles que les VPN (qui déplacent la confiance que vous accordez à votre Fournisseur d'Accès Internet vers le fournisseur de VPN). Bien que cela protège vos données de navigation de votre FAI spécifiquement, le fournisseur de VPN que vous choisissez a toujours accès à vos données de navigation : vos données ne sont pas complètement protégées de toutes les parties.
      - 
        "@type": Question
        name: Les solutions axées sur la protection de la vie privée sont-elles intrinsèquement dignes de confiance ?
        acceptedAnswer:
          "@type": Answer
          text: |
            Se concentrer uniquement sur les politiques de confidentialité et le marketing d'un outil ou d'un fournisseur peut vous aveugler face à ses faiblesses. Lorsque vous recherchez une solution plus privée, vous devez déterminer quel est le problème sous-jacent et trouver des solutions techniques à ce problème. Par exemple, vous voudrez peut-être éviter Google Drive, qui donne à Google l'accès à toutes vos données. Le problème sous-jacent dans ce cas est l'absence d'E2EE, vous devez donc vous assurer que le fournisseur vers lequel vous allez met effectivement en œuvre E2EE, ou utiliser un outil (comme Cryptomator) qui fournit l'E2EE sur n'importe quel fournisseur de cloud. Le passage à un fournisseur "soucieux de la protection de la vie privée" (qui ne met pas en œuvre E2EE) ne résout pas votre problème : il ne fait que déplacer la confiance de Google vers ce fournisseur.
      - 
        "@type": Question
        name: Quelle doit être la complexité de mon modèle de menace ?
        acceptedAnswer:
          "@type": Answer
          text: |
            Nous voyons souvent des personnes décrire des modèles de menace pour protéger leurs vies privées qui sont trop complexes. Souvent, ces solutions incluent des problèmes tels que de nombreux comptes email différents ou des configurations compliquées avec de nombreuses pièces mouvantes et conditions. Les réponses sont généralement des réponses à la question "Quelle est la meilleure façon de faire X ?".
            Trouver la "meilleure" solution pour soi ne signifie pas nécessairement que l'on recherche une solution infaillible avec des dizaines de conditions - ces solutions sont souvent difficiles à utiliser de manière réaliste. Comme nous l'avons vu précédemment, la sécurité se fait souvent au détriment de la commodité.
---

## "Les logiciels libres et open-source sont toujours sécurisés" ou "Les logiciels propriétaires sont plus sécurisé"

Ces mythes découlent d'un certain nombre de préjugés, mais le fait que le code source soit disponible ou non et la manière dont les logiciels sont concédés sous licence n'affectent en rien leur sécurité. ==Les logiciels open-source ont le *potentiel* d'être plus sécurisé que les logiciels propriétaires, mais il n'y a absolument aucune garantie que ce soit le cas.== Lorsque vous évaluez un logiciel, vous devez examiner la réputation et la sécurité de chaque outil individuellement.

Les logiciels libres *peuvent* être audités par des tiers et sont souvent plus transparents sur les vulnérabilités potentielles que leurs homologues propriétaires. Ils vous permettent également d'examiner le code et de désactiver vous-même toute fonctionnalité suspecte. Cependant, *à moins que vous ne le fassiez*, il n'y a aucune garantie que le code ait jamais été évalué, en particulier pour les petits projets. Le processus de développement ouvert a aussi parfois été exploité pour introduire de nouvelles vulnérabilités même dans des projets importants.[^1]

Par ailleurs, les logiciels propriétaires sont moins transparents, mais cela ne signifie pas qu'ils ne sont pas sécurisés. Des projets logiciels propriétaires majeurs peuvent être audités en interne et par des agences tierces, et des chercheurs indépendants en sécurité peuvent toujours trouver des vulnérabilités avec des techniques telles que la rétro-ingénierie.

Pour éviter les décisions biaisées, il est *essentiel* que vous évaluiez les normes de confidentialité et de sécurité des logiciels que vous utilisez.

## "Déplacer la confiance peut améliorer la vie privée"

Nous parlons souvent de "déplacement de confiance" lorsque nous abordons des solutions telles que les VPN (qui déplacent la confiance que vous accordez à votre Fournisseur d'Accès Internet vers le fournisseur de VPN). Bien que cela protège vos données de navigation de votre FAI *spécifiquement*, le fournisseur de VPN que vous choisissez a toujours accès à vos données de navigation : Vos données ne sont pas complètement protégées de toutes les parties. Cela signifie que :

1. Vous devez faire preuve de prudence lorsque vous choisissez un fournisseur auquel accorder votre confiance.
2. Vous devez toujours utiliser d'autres techniques, comme E2EE, pour protéger complètement vos données. Le simple fait de se méfier d'un fournisseur pour faire confiance à un autre ne sécurise pas vos données.

## "Les solutions axées sur la protection de la vie privée sont intrinsèquement dignes de confiance"

Se concentrer uniquement sur les politiques de confidentialité et le marketing d'un outil ou d'un fournisseur peut vous aveugler face à ses faiblesses. Lorsque vous recherchez une solution plus privée, vous devez déterminer quel est le problème sous-jacent et trouver des solutions techniques à ce problème. Par exemple, vous voudrez peut-être éviter Google Drive, qui donne à Google l'accès à toutes vos données. Le problème sous-jacent dans ce cas est l'absence d'E2EE, vous devez donc vous assurer que le fournisseur vers lequel vous passez met effectivement en œuvre E2EE, ou utiliser un outil (comme [Cryptomator](../encryption.md#cryptomator-cloud)) qui fournit E2EE sur n'importe quel fournisseur de cloud. Le passage à un fournisseur "soucieux de la protection de la vie privée" (qui ne met pas en œuvre E2EE) ne résout pas votre problème : il ne fait que déplacer la confiance de Google vers ce fournisseur.

Les politiques de confidentialité et les pratiques commerciales des fournisseurs que vous choisissez sont très importantes, mais doivent être considérées comme secondaires par rapport aux garanties techniques de votre vie privée : Vous ne devriez pas faire confiance à un autre fournisseur lorsque la confiance en un fournisseur n'est pas du tout requise.

## "Plus c'est complexe mieux c'est"

Nous voyons souvent des personnes décrire des modèles de menace pour protéger leurs vies privées qui sont trop complexes. Souvent, ces solutions incluent des problèmes tels que de nombreux comptes email différents ou des configurations compliquées avec de nombreuses pièces mouvantes et conditions. Les réponses sont généralement des réponses à la question "Quelle est la meilleure façon de faire *X*?"

Trouver la "meilleure" solution pour soi ne signifie pas nécessairement que l'on recherche une solution infaillible avec des dizaines de conditions - ces solutions sont souvent difficiles à utiliser de manière réaliste. Comme nous l'avons vu précédemment, la sécurité se fait souvent au détriment de la commodité. Nous vous donnons ci-dessous quelques conseils :

1. ==Les actions doivent servir un objectif particulier:== réfléchissez à la manière de faire ce que vous voulez avec le moins d'actions possible.
2. ==Supprimer les points d'échec humains:== nous échouons, nous nous fatiguons et nous oublions des choses. Pour maintenir la sécurité, évitez de vous appuyer sur des conditions et des processus manuels dont vous devez vous souvenir.
3. ==Utilisez le bon niveau de protection pour ce que vous voulez faire.== Nous voyons souvent des recommandations de solutions soi-disant à l'épreuve des forces de l'ordre et des assignations/mandats. Celles-ci nécessitent souvent des connaissances spécialisées et ne sont généralement pas ce que les gens recherchent. Il ne sert à rien de construire un modèle de menace complexe pour l'anonymat si vous pouvez être facilement désanonymisé par un simple oubli.

Alors, à quoi ça pourrait ressembler ?

Les modèles de menace les plus clairs sont ceux où les gens *savent qui vous êtes* et ceux où ils ne le savent pas. Il y aura toujours des situations où vous devrez déclarer votre nom légal et d'autres où vous n'aurez pas à le faire.

1. **Known identity** - A known identity is used for things where you must declare your name. There are many legal documents and contracts where a legal identity is required. This could range from opening a bank account, signing a property lease, obtaining a passport, customs declarations when importing items, or otherwise dealing with your government. These things will usually lead to credentials such as credit cards, credit rating checks, account numbers, and possibly physical addresses.

    We don't suggest using a VPN or Tor for any of these things, as your identity is already known through other means.

    <div class="admonition tip" markdown>
    <p class="admonition-title">Tip</p>

    When shopping online, the use of a [parcel locker](https://en.wikipedia.org/wiki/Parcel_locker) can help keep your physical address private.

    </div>

2. **Unknown identity** - An unknown identity could be a stable pseudonym that you regularly use. It is not anonymous because it doesn't change. If you're part of an online community, you may wish to retain a persona that others know. This pseudonym isn't anonymous because—if monitored for long enough—details about the owner can reveal further information, such as the way they write, their general knowledge about topics of interest, etc.

    You may wish to use a VPN for this, to mask your IP address. Financial transactions are more difficult to mask: You could consider using anonymous cryptocurrencies, such as [Monero](https://getmonero.org). Employing altcoin shifting may also help to disguise where your currency originated. Typically, exchanges require KYC (know your customer) to be completed before they'll allow you to exchange fiat currency into any kind of cryptocurrency. Local meet-up options may also be a solution; however, those are often more expensive and sometimes also require KYC.

3. **Anonymous identity** - Even with experience, anonymous identities are difficult to maintain over long periods of time. They should be short-term and short-lived identities which are rotated regularly.

    Using Tor can help with this. It is also worth noting that greater anonymity is possible through asynchronous communication: Real-time communication is vulnerable to analysis of typing patterns (i.e. more than a paragraph of text, distributed on a forum, via email, etc.)

[^1]: One notable example of this is the [2021 incident in which University of Minnesota researchers introduced three vulnerabilities into the Linux kernel development project](https://cse.umn.edu/cs/linux-incident).
