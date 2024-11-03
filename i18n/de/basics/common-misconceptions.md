---
title: "Häufige Missverständnisse"
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
            Wenn man sich ausschließlich auf die Datenschutzrichtlinien und die Vermarktung eines Tools oder Anbieters konzentriert, kann man seine Schwächen übersehen. Wenn du nach einer datenschutzfreundlicheren Lösung suchst, solltest du das zugrunde liegende Problem bestimmen und technische Lösungen für dieses Problem finden. So solltest du beispielsweise Google Drive meiden, da Google dadurch Zugriff auf alle deine Daten hat. Das zugrundeliegende Problem ist in diesem Fall das Fehlen von E2EE. Du solltest also sicherstellen, dass der Anbieter, zu dem du wechselst, tatsächlich E2EE implementiert, oder ein Tool (wie Cryptomator) verwenden, das E2EE für jeden Cloud-Anbieter bereitstellt. Der Wechsel zu einem „datenschutzfreundlichen“ Anbieter (der kein E2EE implementiert) löst dein Problem nicht: Es verlagert lediglich das Vertrauen von Google auf diesen Anbieter.
      - 
        "@type": Question
        name: Wie kompliziert sollte mein Bedrohungsmodell sein?
        acceptedAnswer:
          "@type": Answer
          text: |
            Oft sehen wir Menschen, die Bedrohungsmodelle für ihre Privatsphäre beschreiben, die übermäßig komplex sind. Oft beinhalten diese Lösungen Probleme wie viele verschiedene E-Mail-Konten oder komplizierte Konfigurationen mit vielen beweglichen Teilen und Bedingungen. Die Antworten sind in der Regel Antworten auf die Frage „Wie kann man X am besten machen?“
            Die "beste" Lösung für sich selbst zu finden, bedeutet nicht unbedingt, dass du eine unfehlbare Lösung mit Dutzenden von Bedingungen anstrebst - solche Lösungen sind oft schwer realistisch zu handhaben. Wie wir bereits besprochen haben, geht Sicherheit oft auf Kosten der Bequemlichkeit.
---

## „Open-Source-Software ist immer sicher“oder „Proprietäre Software ist sicherer“

Diese Mythen beruhen auf einer Reihe von Vorurteilen, aber ob der Quellcode offen ist und wie die Software lizenziert wird, hat keinen Einfluss auf ihre Sicherheit. ==Open-Source-Software hat das *Potenzial*, sicherer zu sein als proprietäre Software, aber es gibt absolut keine Garantie dafür, dass dies der Fall ist.== Bei der Evaluierung von Software solltest du den Ruf und die Sicherheit jedes Tools einzeln betrachten.

Open-Source-Software *kann* von Dritten geprüft werden und ist in Bezug auf potenzielle Schwachstellen oft transparenter als proprietäre Software. Außerdem kannst du den Code überprüfen und verdächtige Funktionen deaktivieren, die du selbst findest. *Wenn du dies nicht tust*, gibt es keine Garantie, dass der Code jemals evaluiert wurde, insbesondere bei kleineren Softwareprojekten. The open development process has also sometimes been exploited to introduce new vulnerabilities known as [:material-package-variant-closed-remove: Supply Chain Attacks](common-threats.md#attacks-against-certain-organizations ""){.pg-viridian}, which are discussed further in our [Common Threats](common-threats.md) page.[^1]

Auf der anderen Seite ist proprietäre Software weniger transparent, was aber nicht bedeutet, dass sie nicht sicher ist. Große proprietäre Softwareprojekte können intern und von Drittanbietern geprüft werden, und unabhängige Sicherheitsforscher können mit Techniken wie Reverse Engineering immer noch Schwachstellen finden.

Um voreingenommene Entscheidungen zu vermeiden, ist es *wichtig,* dass du die Datenschutz- und Sicherheitsstandards der von dir verwendeten Software bewertest.

## „Die Verlagerung von Vertrauen kann die Privatsphäre stärken“

Bei Lösungen wie VPNs (bei denen das Vertrauen in den Internetanbieter auf den VPN-Anbieter übertragen wird) sprechen wir häufig von „Vertrauensverlagerung“. Dies schützt deine Surfverhalten zwar *speziell* vor deinem Internetanbieter, aber der von dir gewählte VPN-Anbieter hat immer noch Zugriff auf deine Surfdaten: Deine Daten sind nicht vollständig vor allen Parteien geschützt. Das bedeutet:

1. Bei der Auswahl eines Anbieters, dem du dein Vertrauen schenkst, musst du Vorsicht walten lassen.
2. Du solltest trotzdem andere Techniken wie E2EE verwenden, um deine Daten vollständig zu schützen. Einem Anbieter zu misstrauen, um einem anderen zu vertrauen, bedeutet nicht, deine Daten zu sichern.

## „Auf den Datenschutz ausgerichtete Lösungen sind von Natur aus vertrauenswürdig“

Wenn man sich ausschließlich auf die Datenschutzrichtlinien und die Vermarktung eines Tools oder Anbieters konzentriert, kann man seine Schwächen übersehen. Wenn du nach einer datenschutzfreundlicheren Lösung suchst, solltest du das zugrunde liegende Problem bestimmen und technische Lösungen für dieses Problem finden. So solltest du beispielsweise Google Drive meiden, da Google dadurch Zugriff auf alle deine Daten hat. Das zugrundeliegende Problem ist in diesem Fall das Fehlen von E2EE. Du solltest also sicherstellen, dass der Anbieter, zu dem du wechselst, tatsächlich E2EE implementiert, oder ein Tool (wie [Cryptomator](../encryption.md#cryptomator-cloud)) verwenden, das E2EE für jeden Cloud-Anbieter bereitstellt. Der Wechsel zu einem „datenschutzfreundlichen“ Anbieter (der kein E2EE implementiert) löst dein Problem nicht: Es verlagert lediglich das Vertrauen von Google auf diesen Anbieter.

Die Datenschutzrichtlinien und Geschäftspraktiken der Anbieter, die du auswählst, sind sehr wichtig, sollten aber gegenüber den technischen Garantien für deine Privatsphäre als zweitrangig betrachtet werden: Du solltest dein Vertrauen nicht auf einen anderen Anbieter übertragen, wenn das Vertrauen in einen Anbieter gar nicht erforderlich ist.

## „Kompliziert ist besser“

Oft sehen wir Menschen, die Bedrohungsmodelle für ihre Privatsphäre beschreiben, die übermäßig komplex sind. Oft beinhalten diese Lösungen Probleme wie viele verschiedene E-Mail-Konten oder komplizierte Konfigurationen mit vielen beweglichen Teilen und Bedingungen. Die Antworten sind in der Regel Antworten auf die Frage "Wie kann man *X* am besten machen?"

Die "beste" Lösung für sich selbst zu finden, bedeutet nicht unbedingt, dass du eine unfehlbare Lösung mit Dutzenden von Bedingungen anstrebst - solche Lösungen sind oft schwer realistisch zu handhaben. Wie wir bereits besprochen haben, geht Sicherheit oft auf Kosten der Bequemlichkeit. Unten geben wir einige Tipps:

1. ==Aktionen müssen einem bestimmten Zweck dienen:== Überlege dir, wie du dein Ziel mit möglichst wenigen Aktionen erreichen kannst.
2. ==Beseitige menschliche Schwachstellen:== Wir versagen, werden müde und vergessen Dinge. Um Sicherheit zu gewährleisten, solltest du dich nicht auf manuelle Bedingungen und Prozesse verlassen, die du dir merken musst.
3. ==Wähle das richtige Maß an Schutz für das, was du beabsichtigst.== Wir sehen oft Empfehlungen für sogenannte gesetzeskonforme oder vorladungssichere Lösungen. Diese erfordern oft Fachwissen und sind im Allgemeinen nicht das, was die Meisten wollen. Es macht keinen Sinn, ein kompliziertes Bedrohungsmodell für Anonymität zu entwickeln, wenn man durch ein einfaches Versehen de-anonymisiert werden kann.

Wie könnte das also aussehen?

Eines der klarsten Bedrohungsmodelle ist eines, bei dem die Menschen *wissen, wer man ist*, und eines, bei dem sie es nicht wissen. Es wird immer Situationen geben, in denen du deinen gesetzlichen Namen angeben musst, und andere, in denen das nicht nötig ist.

1. **Bekannte Identität** - Eine bekannte Identität wird für Dinge verwendet, bei denen du deinen Namen angeben musst. Es gibt viele juristische Dokumente und Verträge, für die eine juristische Identität erforderlich ist. Dies kann die Eröffnung eines Bankkontos, die Unterzeichnung eines Mietvertrags, die Beantragung eines Reisepasses, Zollerklärungen bei der Einfuhr von Waren oder andere Behördengänge umfassen. Diese Dinge führen in der Regel zu Anmeldedaten wie Kreditkarten, Bonitätsprüfungen, Kontonummern und möglicherweise physischen Adressen.

    Wir raten davon ab, ein VPN oder Tor für diese Dinge zu verwenden, da deine Identität bereits durch andere Mittel bekannt ist.

    <div class="admonition tip" markdown>
    <p class="admonition-title">Tipp</p>

    Beim Online-Einkauf kann die Nutzung eines [Paketautomaten](https://de.wikipedia.org/wiki/Paketautomat) dazu beitragen, dass deine physische Adresse geheim bleibt.

    </div>

2. **Unbekannte Identität** - Eine unbekannte Identität könnte ein festes Pseudonym sein, das du regelmäßig verwendest. Sie ist nicht anonym, weil sie sich nicht verändert. Wenn du Teil einer Online-Community bist, möchtest du womöglich eine Persona beibehalten, die andere kennen. Dieses Pseudonym ist nicht anonym, da — wenn es lange genug beobachtet wird — Details über den Besitzer weitere Informationen preisgeben können, z. B. die Art, wie man schreibt, das allgemeine Wissen über Themen, die einen interessieren usw.

    Du kannst beispielsweise ein VPN dafür verwenden, deine IP-Adresse zu verschleiern. Finanzielle Transaktionen sind schwieriger zu verbergen: Du könntest anonyme Kryptowährungen wie [Monero](../cryptocurrency.md#monero) verwenden. Die Verwendung von Altcoin-Shifting kann auch dazu beitragen, den Ursprung deiner Crypto-Währung zu verschleiern. In der Regel verlangen Börsen KYC, bevor sie dir den Umtausch von Fiatgeld in Kryptowährungen jeglicher Art erlauben. Lokale Treffpunkte können ebenfalls eine Lösung sein; diese sind jedoch oft teurer und erfordern manchmal auch KYC.

3. **Anonyme Identität** - Selbst mit Erfahrung ist es schwierig, anonyme Identitäten über einen längeren Zeitraum aufrechtzuerhalten. Es sollte sich um kurzfristige und kurzlebige Identitäten handeln, die regelmäßig gewechselt werden.

    Die Verwendung von Tor kann dabei helfen. Es ist auch erwähnenswert, dass eine größere Anonymität durch asynchrone Kommunikation möglich ist: Echtzeitkommunikation ist anfällig für die Analyse von Tippmustern (d. h. mehr als ein Absatz Text, der in einem Forum, per E-Mail usw. verbreitet wird).

[^1]: A notable supply chain attack occurred in March 2024, when a malicious maintainer added a obfuscated backdoor into `xz`, a popular compression library. The backdoor ([CVE-2024-3094](https://cve.org/CVERecord?id=CVE-2024-3094)) was intended to give an unknown party remote access to most Linux servers via SSH, but it was discovered before it had been widely deployed.
