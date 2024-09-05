---
title: "Common Misconceptions"
icon: 'material/robot-confused'
description: Datenschutz ist kein einfaches Thema, und es ist leicht, sich von Marketingaussagen und anderen Desinformationen täuschen zu lassen.
schema:
  - 
    "@context": https://schema.org
    "@type": FAQPage
    mainEntity:
      - 
        "@type": Question
        name: Ist Open-Source-Software per se sicher?
        acceptedAnswer:
          "@type": Answer
          text: |
            Ob der Quellcode verfügbar ist und wie die Software lizenziert wird, hat erstmal keinen Einfluss auf ihre Sicherheit. Open-Source-Software hat das Potenzial, sicherer zu sein als proprietäre Software, aber es gibt absolut keine Garantie dafür, dass dies der Fall ist. Bei der Bewertung von Software sollten Sie den Ruf und die Sicherheit jedes einzelnen Tools berücksichtigen.
      - 
        "@type": Question
        name: Kann die Verlagerung von Vertrauen auf einen anderen Anbieter die Privatsphäre erhöhen?
        acceptedAnswer:
          "@type": Answer
          text: |
            Bei Lösungen wie VPNs (bei denen das Vertrauen in den Internetanbieter auf den VPN-Anbieter übertragen wird) sprechen wir häufig von „Vertrauensverlagerung“. Dies schützt deine Surfverhalten zwar vor deinem Internetanbieter, aber der von dir gewählte VPN-Anbieter hat immer noch Zugriff auf deine Surfdaten: Deine Daten sind nicht vollständig vor allen Parteien geschützt.
      - 
        "@type": Question
        name: Sind auf Datenschutz ausgerichtete Lösungen von Natur aus vertrauenswürdig?
        acceptedAnswer:
          "@type": Answer
          text: |
            Focusing solely on the privacy policies and marketing of a tool or provider can blind you to its weaknesses. When you're looking for a more private solution, you should determine what the underlying problem is and find technical solutions to that problem. For example, you may want to avoid Google Drive, which gives Google access to all of your data. The underlying problem in this case is lack of E2EE, so you should make sure that the provider you switch to actually implements E2EE, or use a tool (like Cryptomator) which provides E2EE on any cloud provider. Switching to a "privacy-focused" provider (that doesn't implement E2EE) doesn't solve your problem: it just shifts trust from Google to that provider.
      - 
        "@type": Question
        name: Wie kompliziert sollte mein Bedrohungsmodell sein?
        acceptedAnswer:
          "@type": Answer
          text: |
            We often see people describing privacy threat models that are overly complex. Often, these solutions include problems like many different email accounts or complicated setups with lots of moving parts and conditions. The replies are usually answers to "What is the best way to do X?"
            Finding the "best" solution for yourself doesn't necessarily mean you are after an infallible solution with dozens of conditions—these solutions are often difficult to work with realistically. As we discussed previously, security often comes at the cost of convenience.
---

## „Open-Source-Software ist immer sicher“oder „Proprietäre Software ist sicherer“

These myths stem from a number of prejudices, but whether the source code is available and how software is licensed does not inherently affect its security in any way. ==Open-source software has the *potential* to be more secure than proprietary software, but there is absolutely no guarantee this is the case.== When you evaluate software, you should look at the reputation and security of each tool on an individual basis.

Open-source software *can* be audited by third-parties, and is often more transparent about potential vulnerabilities than proprietary counterparts. It also allows you to review the code and disable any suspicious functionality you find yourself. However, *unless you do so*, there is no guarantee that code has ever been evaluated, especially with smaller software projects. The open development process has also sometimes been exploited to introduce new vulnerabilities known as [:material-package-variant-closed-remove: Supply Chain Attacks](common-threats.md#attacks-against-certain-organizations ""){.pg-viridian}, which are discussed further in our [Common Threats](common-threats.md) page.[^1]

On the flip side, proprietary software is less transparent, but that doesn't imply that it's not secure. Major proprietary software projects can be audited internally and by third-party agencies, and independent security researchers can still find vulnerabilities with techniques like reverse engineering.

To avoid biased decisions, it's *vital* that you evaluate the privacy and security standards of the software you use.

## „Die Verlagerung von Vertrauen kann die Privatsphäre stärken“

Bei Lösungen wie VPNs (bei denen das Vertrauen in den Internetanbieter auf den VPN-Anbieter übertragen wird) sprechen wir häufig von „Vertrauensverlagerung“. Dies schützt deine Surfverhalten zwar *speziell* vor deinem Internetanbieter, aber der von dir gewählte VPN-Anbieter hat immer noch Zugriff auf deine Surfdaten: Deine Daten sind nicht vollständig vor allen Parteien geschützt. Das bedeutet:

1. Bei der Auswahl eines Anbieters, dem du dein Vertrauen schenkst, musst du Vorsicht walten lassen.
2. Du solltest trotzdem andere Techniken wie E2EE verwenden, um deine Daten vollständig zu schützen. Einem Anbieter zu misstrauen, um einem anderen zu vertrauen, bedeutet nicht, deine Daten zu sichern.

## „Auf den Datenschutz ausgerichtete Lösungen sind von Natur aus vertrauenswürdig“

Focusing solely on the privacy policies and marketing of a tool or provider can blind you to its weaknesses. When you're looking for a more private solution, you should determine what the underlying problem is and find technical solutions to that problem. For example, you may want to avoid Google Drive, which gives Google access to all of your data. The underlying problem in this case is lack of E2EE, so you should make sure that the provider you switch to actually implements E2EE, or use a tool (like [Cryptomator](../encryption.md#cryptomator-cloud)) which provides E2EE on any cloud provider. Switching to a "privacy-focused" provider (that doesn't implement E2EE) doesn't solve your problem: it just shifts trust from Google to that provider.

The privacy policies and business practices of providers you choose are very important, but should be considered secondary to technical guarantees of your privacy: You shouldn't shift trust to another provider when trusting a provider isn't a requirement at all.

## „Kompliziert ist besser“

Oft sehen wir Menschen, die Bedrohungsmodelle für Privatsphäre beschreiben, die übermäßig komplex sind. Often, these solutions include problems like many different email accounts or complicated setups with lots of moving parts and conditions. The replies are usually answers to "What is the best way to do *X*?"

Finding the "best" solution for yourself doesn't necessarily mean you are after an infallible solution with dozens of conditions—these solutions are often difficult to work with realistically. As we discussed previously, security often comes at the cost of convenience. Below, we provide some tips:

1. ==Aktionen müssen einem bestimmten Zweck dienen:== Überlege dir, wie du dein Ziel mit möglichst wenigen Aktionen erreichen kannst.
2. ==Beseitige menschliche Schwachstellen:== Wir versagen, werden müde und vergessen Dinge. Um Sicherheit zu gewährleisten, solltest du dich nicht auf manuelle Bedingungen und Prozesse verlassen, die du dir merken musst.
3. ==Wähle das richtige Maß an Schutz für das, was du beabsichtigst.== Wir sehen oft Empfehlungen für sogenannte gesetzeskonforme oder vorladungssichere Lösungen. Diese erfordern oft Fachwissen und sind im Allgemeinen nicht das, was die Meisten wollen. Es macht keinen Sinn, ein kompliziertes Bedrohungsmodell für Anonymität zu entwickeln, wenn man durch ein einfaches Versehen de-anonymisiert werden kann.

Wie könnte das also aussehen?

One of the clearest threat models is one where people *know who you are* and one where they do not. There will always be situations where you must declare your legal name and there are others where you don't need to.

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

[^1]: A notable supply chain attack occurred in March 2024, when a malicious maintainer added a obfuscated backdoor into `xz`, a popular compression library. The backdoor ([CVE-2024-3094](https://cve.org/CVERecord?id=CVE-2024-3094)) was intended to give an unknown party remote access to most Linux servers via SSH, but it was discovered before it had been widely deployed.
