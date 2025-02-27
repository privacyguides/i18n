---
title: "Veel voorkomende misvattingen"
icon: 'material/robot-confused'
description: Privacy is geen eenvoudig onderwerp, en men raakt gemakkelijk verstrikt in marketingclaims en andere desinformatie.
schema:
  - 
    "@context": https://schema.org
    "@type": FAQPage
    mainEntity:
      - 
        "@type": Question
        name: Is open-source software inherently secure?
        acceptedAnswer:
          "@type": Answer
          text: |
            Of de broncode beschikbaar is en hoe software is gelicentieerd, heeft op geen enkele manier invloed op de veiligheid ervan. Open-source software kan veiliger zijn dan private software, maar er is geen enkele garantie dat dit het geval is. Wanneer je software evalueert, moet je op individuele basis kijken naar de reputatie en beveiliging van elk hulpmiddel.
      - 
        "@type": Question
        name: Kan vertrouwen verschuiven naar een andere provider je privacy verbeteren?
        acceptedAnswer:
          "@type": Answer
          text: |
            We hebben het vaak over "verschuivend vertrouwen" bij het bespreken van oplossingen zoals VPN's (die het vertrouwen dat je in jouw ISP stelt verschuiven naar de VPN-aanbieder). Hiermee worden jouw internetgegevens speciaal door je internetprovider beschermd. de VPN-provider die je kiest heeft nog steeds toegang totjouw browsergegevens: jouw gegevens zijn niet volledig beveiligd voor alle partijen.
      - 
        "@type": Question
        name: Zijn privacygerichte oplossingen inherent betrouwbaar?
        acceptedAnswer:
          "@type": Answer
          text: |
            Als je je zich uitsluitend richt op het privacybeleid en de marketing van een tool of provider, kunt je je blindstaren op de zwakke punten ervan. Wanneer je op zoek bent naar een meer private oplossing, moet je bepalen wat het onderliggende probleem is en technische oplossingen voor dat probleem vinden. Je kunt bijvoorbeeld Google Drive vermijden, dat Google toegang geeft tot al Jouw gegevens. Het onderliggende probleem in dit geval is een gebrek aan E2EE, dus je moet ervoor zorgen dat de provider waarnaar je overstapt daadwerkelijk E2EE implementeert, of een tool gebruiken (zoals Cryptomator) die E2EE biedt op elke cloud provider. Overstappen naar een "privacygerichte" provider (die geen end-to-end encryptie implementeert) lost je probleem niet op: het verschuift alleen het vertrouwen van Google naar die provider.
      - 
        "@type": Question
        name: Hoe ingewikkeld zou mijn bedreigingsmodel moeten zijn?
        acceptedAnswer:
          "@type": Answer
          text: |
            We zien vaak dat mensen overdreven ingewikkelde dreigingsmodellen voor privacybedreigingen beschrijven. Vaak omvatten deze oplossingen problemen zoals veel verschillende e-mailaccounts of ingewikkelde opstellingen met veel bewegende delen en voorwaarden. De antwoorden zijn meestal antwoorden op "Wat is de beste manier om X te doen?"
            Het vinden van de "beste" oplossing voor jezelf betekent niet noodzakelijk dat je op zoek bent naar een onfeilbare oplossing met tientallen voorwaarden - deze oplossingen zijn vaak moeilijk om realistisch mee te werken. Zoals we eerder hebben besproken, gaat veiligheid vaak ten koste van gemak.
---

## "Open source software is altijd veilig" of "Private software is veiliger"

Deze mythes komen voort uit een aantal vooroordelen, maar of de broncode beschikbaar is en hoe software in licentie wordt gegeven, heeft op geen enkele manier invloed op de beveiliging ervan. ==Open-source software heeft de *potentieel* om veiliger te zijn dan propriëtaire software, maar er is absoluut geen garantie dat dit het geval is.== Wanneer je software evalueert, moet je op individuele basis naar de reputatie en beveiliging van elke tool kijken.

Open-source software *kan* worden gecontroleerd door derden, en is vaak transparanter over mogelijke kwetsbaarheden dan propriëtaire tegenhangers. Ze kunnen ook flexibeler zijn, zodat je in de code kunt duiken en alle verdachte functionaliteit kunt uitschakelen die je zelf vindt. Echter, *tenzij je dit zelf doet*, is er geen garantie dat code ooit is geëvalueerd, vooral bij kleinere softwareprojecten. The open development process has also sometimes been exploited to introduce new vulnerabilities known as [:material-package-variant-closed-remove: Supply Chain Attacks](common-threats.md#attacks-against-certain-organizations ""){.pg-viridian}, which are discussed further in our [Common Threats](common-threats.md) page.[^1]

Aan de andere kant is propriëtaire software minder transparant, maar dat betekent niet dat het niet veilig is. Grote propriëtaire softwareprojecten kunnen intern en door derden worden gecontroleerd, en onafhankelijke veiligheidsonderzoekers kunnen nog steeds kwetsbaarheden vinden met technieken als reverse engineering.

Om bevooroordeelde beslissingen te vermijden, is het *van vitaal belang* dat je de privacy- en veiligheidsnormen evalueert van de software die je gebruikt.

## "Verschuiven van vertrouwen kan de privacy vergroten"

We hebben het vaak over "verschuivend vertrouwen" bij het bespreken van oplossingen zoals VPN's (die het vertrouwen dat je in jouw ISP stelt verschuiven naar de VPN-aanbieder). Hoewel dit je surf gedrag beschermt tegen uw ISP *specifiek*, heeft de VPN provider die je kiest nog steeds toegang tot jouw surf gedrag: jouw gegevens zijn niet volledig beveiligd tegen alle partijen. Dit betekent dat:

1. Je moet voorzichtig zijn bij het kiezen van een provider om je vertrouwen naar toe te verschuiven.
2. Je zou nog steeds andere technieken moeten gebruiken, zoals E2EE, om je gegevens volledig te beschermen. Alleen al het wantrouwen van een provider om een andere te vertrouwen, staat niet gelijk aan het beveiligen van je gegevens.

## Privacy-gerichte oplossingen zijn van nature betrouwbaar

Als je je zich uitsluitend richt op het privacybeleid en de marketing van een tool of provider, kunt je je blindstaren op de zwakke punten ervan. Wanneer je op zoek bent naar een meer private oplossing, moet je bepalen wat het onderliggende probleem is en technische oplossingen voor dat probleem vinden. Je kunt bijvoorbeeld Google Drive vermijden, dat Google toegang geeft tot al Jouw gegevens. Het onderliggende probleem is in dit geval een gebrek aan end-to-end encryptie, dus je moet ervoor zorgen dat de provider waar je naar overstapt daadwerkelijk end-to-end encryptie implementeert of een tool (zoals [Cryptomator](../encryption.md#cryptomator-cloud)) gebruiken die end-to-end encryptie biedt op elke cloud provider. Overstappen naar een "privacygerichte" provider (die geen end-to-end encryptie implementeert) lost je probleem niet op: het verschuift alleen het vertrouwen van Google naar die provider.

Het privacybeleid en de zakelijke praktijken van de aanbieders die je kiest, zijn zeer belangrijk. Maar moeten toch worden beschouwd als minder belangrijk dan technische garanties van jouw privacy: je moet vertrouwen niet overdragen naar een andere provider wanneer het vertrouwen in een provider helemaal geen vereiste is.

## "Ingewikkeld is beter"

We zien vaak dat mensen overdreven ingewikkelde dreigingsmodellen voor privacybedreigingen beschrijven. Often, these solutions include problems like multiple email accounts or complicated setups with lots of moving parts and conditions. De antwoorden zijn meestal antwoorden op "Wat is de beste manier om *X* te doen?"

Het vinden van de "beste" oplossing voor jezelf betekent niet noodzakelijk dat je op zoek bent naar een onfeilbare oplossing met tientallen voorwaarden - deze oplossingen zijn vaak moeilijk om realistisch mee te werken. Zoals we eerder hebben besproken, gaat veiligheid vaak ten koste van gemak. Hieronder geven we enkele tips:

1. ==Acties moeten een bepaald doel dienen==, denk na over hoe je met zo weinig mogelijk acties kunt doen wat je wilt.
2. ==Verwijder menselijke faalpunten:== We maken fouten, worden moe, en vergeten dingen. Om de veiligheid te behouden, moet je voorkomen dat je vertrouwt op handmatige acties en processen die je moet onthouden.
3. ==Gebruik het juiste niveau van bescherming voor wat je van plan bent.== Wij zien vaak aanbevelingen van zogenaamde politie, en legerbestendige oplossingen. Deze vereisen vaak specialistische kennis en zijn over het algemeen niet wat de mensen willen. There's no point in building an intricate threat model for anonymity if you can be easily deanonymized by a simple oversight.

Dus, hoe zou dit eruit zien?

Een van de duidelijkste dreigingsmodellen is een model waarbij mensen *weten wie je bent* en een model waarbij ze dat niet weten. Er zullen altijd situaties zijn waarin je je wettelijke naam moet opgeven en er zijn situaties waarin je dat niet hoeft te doen.

1. **Known identity** - A known identity is used for things where you must declare your name. There are many legal documents and contracts where a legal identity is required. This could range from opening a bank account, signing a property lease, obtaining a passport, customs declarations when importing items, or otherwise dealing with your government. These things will usually lead to credentials such as credit cards, credit rating checks, account numbers, and possibly physical addresses.

    We don't suggest using a VPN or Tor for any of these things, as your identity is already known through other means.

    <div class="admonition tip" markdown>
    <p class="admonition-title">Tip</p>

    When shopping online, the use of a [parcel locker](https://en.wikipedia.org/wiki/Parcel_locker) can help keep your physical address private.

    </div>

2. **Unknown identity** - An unknown identity could be a stable pseudonym that you regularly use. It is not anonymous because it doesn't change. If you're part of an online community, you may wish to retain a persona that others know. This pseudonym isn't anonymous because—if monitored for long enough—details about the owner can reveal further information, such as the way they write, their general knowledge about topics of interest, etc.

    You may wish to use a VPN for this, to mask your IP address. Financial transactions are more difficult to mask: You could consider using anonymous cryptocurrencies, such as [Monero](../cryptocurrency.md#monero). Employing altcoin shifting may also help to disguise where your currency originated. Typically, exchanges require KYC (know your customer) to be completed before they'll allow you to exchange fiat currency into any kind of cryptocurrency. Local meet-up options may also be a solution; however, those are often more expensive and sometimes also require KYC.

3. **Anonymous identity** - Even with experience, anonymous identities are difficult to maintain over long periods of time. They should be short-term and short-lived identities which are rotated regularly.

    Using Tor can help with this. It is also worth noting that greater anonymity is possible through asynchronous communication: Real-time communication is vulnerable to analysis of typing patterns (i.e. more than a paragraph of text, distributed on a forum, via email, etc.)

[^1]: A notable supply chain attack occurred in March 2024, when a malicious maintainer added an obfuscated backdoor into `xz`, a popular compression library. The backdoor ([CVE-2024-3094](https://cve.org/CVERecord?id=CVE-2024-3094)) was intended to give an unknown party remote access to most Linux servers via SSH, but it was discovered before it had been widely deployed.
