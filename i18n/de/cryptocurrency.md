---
meta_title: "Private Kryptowährungs-Blockchains - Privacy Guides"
title: Kryptowährung
icon: material/bank-circle
cover: cryptocurrency.webp
---

<small>Schützt vor der/den folgenden Bedrohung(en):</small>

- [:material-eye-outline: Massenüberwachung](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-close-outline: Zensur](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}

Online-Zahlungen sind eine der größten Herausforderungen für Privatsphäre. Diese Kryptowährungen bieten standardmäßig den Schutz der Privatsphäre bei Transaktionen (was bei den meisten Kryptowährungen **nicht** gewährleistet ist), vorausgesetzt, du weißt, wie du private Zahlungen effektiv durchführen kannst. Wir empfehlen dir dringend, zuerst unseren Artikel über Zahlungen zu lesen, bevor du einen Kauf tätigst:

[Private Zahlungsmethoden :material-arrow-right-drop-circle:](advanced/payments.md ""){.md-button}

<div class="admonition danger" markdown>
<p class="admonition-title">Achtung</p>

Viele, wenn nicht die meisten, Kryptowährungsprojekte sind Betrugsmaschen. Tätige Transaktionen nur mit Projekten, denen du vertraust.

</div>

## Monero

<div class="admonition recommendation" markdown>

![Monero-Logo](assets/img/cryptocurrency/monero.svg){ align=right }

**Monero** verwendet eine Blockchain mit Technologien zur Verbesserung der Privatsphäre, die Transaktionen verschleiern, um [:material-incognito: Anonymität](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple } zu erreichen. Jede Monero-Transaktion verbirgt den Transaktionsbetrag, die sendende und empfangende Adresse und die Quelle des Geldes, ohne dass man irgendwelche Hürden überwinden muss, was es zu einer idealen Wahl für Kryptowährungs-Neulinge macht.

[:octicons-home-16: Homepage](https://getmonero.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://getmonero.org/resources/user-guides){ .card-link title=Dokumentation}
[:octicons-code-16:](https://github.com/monero-project/monero){ .card-link title="Quellcode" }
[:octicons-heart-16:](https://getmonero.org/get-started/contributing){ .card-link title=Mitwirken }

</details>

</div>

Bei Monero können außenstehende Beobachter weder Adressen, die mit Monero handeln, noch Transaktionsbeträge, Adresssalden oder Transaktionshistorien entziffern.

Für einen optimalen Schutz der Privatsphäre solltest du eine Non-Custodial Wallet verwenden, bei der auch der Ansichtsschlüssel auf deinem Gerät bleibt. Das bedeutet, dass nur du die Möglichkeit hast, dein Geld auszugeben und ein- und ausgehende Transaktionen zu sehen. Wenn du eine Custodial Wallet verwendest, kann der Anbieter **alles** sehen, was du tust; wenn du eine „lightweight“ Wallet verwendest, bei der der Anbieter deinen privaten Ansichtsschlüssel beibehält, sieht dieser fast alles, was du tust. Einige Non-Custodial Wallets sind:

- [Offizieller Monero-Client](https://getmonero.org/downloads) (Desktop)
- [Cake Wallet](https://cakewallet.com) (iOS, Android, macOS)
    - Cake Wallet unterstützt mehrere Kryptowährungen. Eine reine Monero Version von Cake Wallet für iOS und Android ist auf [Monero.com](https://monero.com) verfügbar.
- [Feather Wallet](https://featherwallet.org) (Desktop)
- [Monerujo](https://monerujo.io) (Android)

Für maximale Privatsphäre (auch mit einer Non-Custodial Wallet) solltest du deinen eigenen Monero-Node betreiben. Wenn du den Node einer anderen Person verwendest, werden einige Informationen preisgegeben, z. B. die IP-Adresse, von der aus du dich mit dem Node verbindest, die Zeitpunkte, an denen du deine Wallet synchronisierst und der Transaktionen, die du von deiner Wallet aus sendest (allerdings keine weiteren Details über diese Transaktionen). Alternativ kannst du dich über Tor oder [I2P](alternative-networks.md#i2p-the-invisible-internet-project) mit dem Monero-Knoten einer anderen Person verbinden.

Im August 2021 [kündigte](https://web.archive.org/web/20240223224846/https://ciphertrace.com/enhanced-monero-tracing) CipherTrace erweiterte Monero-Verfolgungsfunktionen für Regierungsbehören an. Aus öffentlichen Veröffentlichungen geht hervor, dass das Financial Crimes Enforcement Network des US-Finanzministeriums das „Monero-Modul“ von CipherTrace Ende 2022 [lizenziert hat](https://sam.gov/opp/d12cbe9afbb94ca68006d0f006d355ac/view).

Die Vertraulichkeit des Monero-Transaktionsgraphen wird durch seine relativ kleinen Ringsignaturen eingeschränkt, insbesondere gegenüber gezielten Angriffen. Die Datenschutzfunktionen von Monero wurden auch von einigen Sicherheitsforschern [in Frage gestellt](https://web.archive.org/web/20180331203053/https://wired.com/story/monero-privacy), und in der Vergangenheit wurde eine Reihe schwerwiegender Server-Schwachstellen gefunden und gepatcht, sodass die Behauptungen von Organisationen wie CipherTrace nicht außer Frage stehen. Es ist zwar unwahrscheinlich, dass es für Monero Massenüberwachungs-Tools gibt, wie es sie für Bitcoin und andere Währungen gibt, aber es ist sicher, dass Rückverfolgungs-Tools bei gezielten Ermittlungen helfen.

Letzten Endes ist Monero der stärkste Kandidat für eine datenschutzfreundliche Kryptowährung, aber seine Datenschutzansprüche sind **nicht** definitiv bewiesen. Es ist mehr Zeit und Forschung nötig, um zu beurteilen, ob Monero widerstandsfähig genug gegen Angriffe ist, um immer eine angemessene Privatsphäre zu bieten.

## Kriterien

**Bitte beachte, dass wir mit keinem der Projekte, die wir empfehlen, in Verbindung stehen.** Zusätzlich zu unseren [Standardkriterien](about/criteria.md) haben wir eine Reihe klarer Anforderungen entwickelt, die es uns ermöglichen, objektive Empfehlungen zu geben. Wir empfehlen dir, dich mit der Liste vertraut zu machen, bevor du dich für ein Projekt entscheidest, und deine eigenen Recherchen anzustellen, um sicherzustellen, dass es die richtige Wahl für dich ist.

- Kryptowährungen müssen standardmäßig private/unverfolgbare Transaktionen ermöglichen.
