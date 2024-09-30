---
meta_title: "Die besten privaten Instant Messengers - Privacy Guides"
title: "Echtzeitkommunikation"
icon: material/chat-processing
description: Verschlüsselte Messenger wie Signal und SimpleX schützen deine sensible Kommunikation vor neugierigen Blicken.
cover: real-time-communication.webp
---

<small>Schützt vor der/den folgenden Bedrohung(en):</small>

- [:material-bug-outline: Passive Angriffe](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: Diensteanbieter](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}
- [:material-eye-outline: Massenüberwachung](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-account-cash: Überwachungskapitalismus](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Dies sind unsere Empfehlungen für verschlüsselte **Echtzeitkommunikation**.

[Arten von Kommunikationsnetzen :material-arrow-right-drop-circle:](./advanced/communication-network-types.md)

## Verschlüsselte Messenger

Diese Messenger eignen sich hervorragend zur Sicherung deiner sensiblen Kommunikation.

### Signal

<div class="admonition recommendation" markdown>

![Signal logo](assets/img/messengers/signal.svg){ align=right }

**Signal** ist eine mobile App, die von Signal Messenger LLC entwickelt wurde. Die App bietet Instant Messaging und Anrufe, die mit dem Signal-Protokoll gesichert sind, einem extrem sicheren Verschlüsselungsprotokoll, das Forward Secrecy[^1] und Post-Compromise Security[^2] unterstützt.

[:octicons-home-16: Homepage](https://signal.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://signal.org/legal/#privacy-policy){ .card-link title="Datenschutzerklärung" }
[:octicons-info-16:](https://support.signal.org){ .card-link title=Dokumentation}
[:octicons-code-16:](https://github.com/signalapp){ .card-link title="Quellcode" }
[:octicons-heart-16:](https://signal.org/donate){ .card-link title=Spenden }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.thoughtcrime.securesms)
- [:simple-appstore: App Store](https://apps.apple.com/app/id874139669)
- [:simple-android: Android](https://signal.org/android/apk)
- [:fontawesome-brands-windows: Windows](https://signal.org/download/windows)
- [:simple-apple: macOS](https://signal.org/download/macos)
- [:simple-linux: Linux](https://signal.org/download/linux)

</details>

</div>

Signal benötigt deine Telefonnummer für die Registrierung, aber du solltest einen Benutzernamen erstellen, um deine Telefonnummer vor deinen Kontakten zu verbergen:

1. Öffne in Signal die Einstellungen der App und tippe oben auf dein Kontoprofil.
2. Tap **Username** and choose **Continue** on the "Set up your Signal username" screen.
3. Gebe einen Nutzernamen ein. Dein Benutzername wird immer mit einer eindeutigen Ziffernfolge gekoppelt, damit dein Benutzername eindeutig ist und nicht erraten werden kann. Wenn du beispielsweise "John" eingibst, könnte dein Benutzername `@john.35` lauten. Standardmäßig werden deinem Benutzernamen bei der Erstellung nur 2 Ziffern zugeordnet, aber du kannst weitere Ziffern hinzufügen, bis du die maximale Länge des Benutzernamens erreichst (32 Zeichen).
4. Gehe zurück zur Hauptseite der App-Einstellungen und wähle **Datenschutz**.
5. Wähle **Telefonnummer**
6. Ändere die Einstellung **Wer kann meine Telefonnummer sehen** zu: **Niemand**

Du kannst optional auch die Einstellung **Wer kann mich anhand der Telefonnummer finden** zu **Niemand** ändern, wenn du verhindern möchtest, dass Personen, die bereits deine Telefonnummer haben, dein Signal-Konto/Benutzernamen entdecken.

Kontaktlisten auf Signal werden mit deiner Signal-PIN verschlüsselt und der Server hat keinen Zugriff auf sie. Persönliche Profile sind ebenfalls verschlüsselt und werden nur an Kontakte weitergegeben, mit denen du chattest. Signal unterstützt [private Gruppen](https://signal.org/blog/signal-private-group-system), bei denen der Server keine Aufzeichnungen über deine Gruppenmitgliedschaften, Gruppentitel, Gruppenavatare oder Gruppenattribute hat. Signal verwendet minimale Metadaten, wenn [Vertraulicher Absender](https://signal.org/blog/sealed-sender) (Sealed Sender) aktiviert ist. Die Absenderadresse wird zusammen mit dem Nachrichtentext verschlüsselt, und nur die Empfängeradresse ist für den Server sichtbar. Vertraulicher Absender ist nur für Personen in deiner Kontaktliste aktiviert, kann aber für alle Empfänger mit dem erhöhten Risiko des Empfangs von Spam aktiviert werden.

Das Protokoll wurde 2016 unabhängig [geprüft](https://eprint.iacr.org/2016/1013.pdf). Die Spezifikation des Signal-Protokolls findest du in der entsprechenden [Dokumentation](https://signal.org/docs).

Wir haben einige zusätzliche Tipps zum Konfigurieren und Absichern deiner Signal-Installation:

[Signalkonfiguration und Hardening :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening)

#### Molly (Android)

If you use Android and your threat model requires protecting against [:material-target-account: Targeted Attacks](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red} you may consider using this alternative app, which features a number of security and usability improvements, to access the Signal network.

<div class="admonition recommendation" markdown>

![Molly-Logo](assets/img/messengers/molly.svg){ align=right }

**Molly** ist ein alternativer Signal-Client für Android, der es dir ermöglicht, die lokale Datenbank im Ruhezustand mit einer Passphrase zu verschlüsseln, ungenutzte RAM-Daten sicher zu schreddern, deine Verbindung über Tor zu leiten und [mehr](https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening#privacy-and-security-features). Außerdem gibt es Verbesserungen bei der Benutzerfreundlichkeit, wie z. B. geplante Backups, automatisches Sperren und die Möglichkeit, dein Android-Telefon als verknüpftes Gerät anstelle des Hauptgeräts für ein Signal-Konto zu verwenden.

[:octicons-home-16: Homepage](https://molly.im){ .md-button .md-button--primary }
[:octicons-eye-16:](https://signal.org/legal/#privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/mollyim/mollyim-android/wiki){ .card-link title="Documentation"}
[:octicons-code-16:](https://github.com/mollyim/mollyim-android){ .card-link title="Source Code" }
[:octicons-heart-16:](https://opencollective.com/mollyim){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-fdroid: F-Droid](https://molly.im/fdroid)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/im.molly.app)
- [:simple-github: GitHub](https://github.com/mollyim/mollyim-android/releases)

</details>

</div>

Molly wird alle zwei Wochen aktualisiert, um die neuesten Funktionen und Fehlerbehebungen von Signal einzubinden. Die Ausnahme sind Sicherheitsprobleme, die so schnell wie möglich behoben werden. Allerdings sollten Sie sich darüber im Klaren sein, dass es zu einer leichten Verzögerung im Vergleich zum Upstream kommen kann, was sich auf Aktionen wie die [Migration von Signal zu Molly](https://github.com/mollyim/mollyim-android/wiki/Migrating-From-Signal#migrating-from-signal) auswirken kann.

Beachte, dass du durch die Verwendung von Molly mehreren Parteien vertraust, da du nun dem Signal-Team *und dem* Molly-Team vertrauen musst, dass sie sichere und rechtzeitige Aktualisierungen liefern.

Es gibt eine Version von Molly namens **Molly-FOSS**, die proprietären Code wie die Google-Dienste, die sowohl von Signal als auch von Molly verwendet werden, entfernt, was allerdings auf Kosten einiger Funktionen wie akkusparende Push-Benachrichtigungen via Google Play Services geht.

There is also a version called [**Molly-UP**](https://github.com/mollyim/mollyim-android#unifiedpush) which is based on Molly-FOSS and adds support for push notifications with [UnifiedPush](https://unifiedpush.org/), an open source alternative to the push notifications provided by Google Play Services, but it requires running a separate program called [Mollysocket](https://github.com/mollyim/mollysocket) to function. Mollysocket can either be self-hosted on a separate computer or server (VPS), or alternatively a public Mollysocket instance can be used ([step-by-step tutorial, in German](https://www.kuketz-blog.de/messenger-wechsel-von-signal-zu-molly-unifiedpush-mollysocket-ntfy/)).

Alle drei Versionen von Molly bieten die gleichen Sicherheitsverbesserungen.

Molly und Molly-FOSS unterstützen [reproduzierbare Builds](https://github.com/mollyim/mollyim-android/tree/main/reproducible-builds), d.h. es ist möglich zu bestätigen, dass die kompilierten APKs mit dem Quellcode übereinstimmen.

### SimpleX Chat

<div class="admonition recommendation" markdown>

![Simplex-Logo](assets/img/messengers/simplex.svg){ align=right }

**SimpleX** Chat ist ein Instant Messenger, der ohne eindeutigen Identifikatoren wie Telefonnummern oder Benutzernamen auskommt. Sein dezentrales Netzwerk macht SimpleX Chat zu einem effektiven Werkzeug gegen [:material-close-outline: Zensur](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }. Benutzer von SimpleX Chat können einen QR-Code scannen oder auf einen Einladungslink klicken, um an Gruppengesprächen teilzunehmen.

[:octicons-home-16: Homepage](https://simplex.chat){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/simplex-chat/simplex-chat/blob/stable/PRIVACY.md){ .card-link title="Datenschutzrichtlinie" }
[:octicons-info-16:](https://github.com/simplex-chat/simplex-chat/tree/stable/docs){ .card-link title=Dokumentation}
[:octicons-code-16:](https://github.com/simplex-chat){ .card-link title="Quellcode" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=chat.simplex.app)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1605771084)
- [:simple-github: GitHub](https://github.com/simplex-chat/simplex-chat/releases)
- [:fontawesome-brands-windows: Windows](https://simplex.chat/downloads/#desktop-app)
- [:simple-apple: macOS](https://simplex.chat/downloads/#desktop-app)
- [:simple-linux: Linux](https://simplex.chat/downloads/#desktop-app)

</details>

</div>

SimpleX Chat wurde im Oktober 2016 einem [Audit](https://simplex.chat/blog/20221108-simplex-chat-v4.2-security-audit-new-website.html) von Trail of Bits unterzogen.

SimpleX Chat unterstützt grundlegende Gruppen-Chat-Funktionen, Direktnachrichten und die Bearbeitung von Nachrichten und Markdown. E2EE Audio- und Videoanrufe werden ebenfalls unterstützt. Deine Daten können exportiert und auf ein anderes Gerät importiert werden, da es keine zentralen Server gibt, auf denen die Daten gesichert werden.

### Briar

<div class="admonition recommendation" markdown>

![Briar-Logo](assets/img/messengers/briar.svg){ align=right }

**Briar** ist ein verschlüsselter Instant-Messenger, der sich mit anderen Geräten [über das Tor-Netzwerk verbindet](https://briarproject.org/how-it-works). Das macht es zu einem effektiven Werkzeug zur Umgehung von [:material-close-outline: Zensur](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }. Briar kann sich auch über Wi-Fi oder Bluetooth verbinden, wenn sich die Geräte in der Nähe befinden. Dieser lokale Mesh-Modus von Briar kann nützlich sein, wenn die Internetverfügbarkeit ein Problem darstellt.

[:octicons-home-16: Homepage](https://briarproject.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://briarproject.org/privacy-policy){ .card-link title="Datenschutzrichtlinie" }
[:octicons-info-16:](https://code.briarproject.org/briar/briar/-/wikis/home){ .card-link title=Dokumentation}
[:octicons-code-16:](https://code.briarproject.org/briar/briar){ .card-link title="Quellcode" }
[:octicons-heart-16:](https://briarproject.org){ .card-link title="Spendenoptionen sind unten auf der Hompage aufgeführt" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.briarproject.briar.android)
- [:fontawesome-brands-windows: Windows](https://briarproject.org/download-briar-desktop)
- [:simple-linux: Linux](https://briarproject.org/download-briar-desktop)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.briarproject.Briar)

</details>

</div>

Um einen Kontakt auf Briar hinzuzufügen, musst sich beide Seiten zuerst gegenseitig hinzufügen. Du kannst entweder `briar://` Links austauschen oder den QR-Code eines Kontakts scannen, wenn dieser in der Nähe ist.

Die Client-Software wurde von unabhängiger Seite [geprüft](https://briarproject.org/news/2017-beta-released-security-audit), und das anonyme Routing-Protokoll verwendet das Tor-Netzwerk, das ebenfalls geprüft ist.

Briar hat eine vollständig [veröffentlichte Spezifikation](https://code.briarproject.org/briar/briar-spec).

Briar unterstützt Forward Secrecy[^1] durch Verwendung des Bramble [Handshake-](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BHP.md) und [Transportprotokolls](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BTP.md).

## Weitere Optionen

<div class="admonition warning" markdown>
<p class="admonition-title">Warnung</p>

Diese Messenger haben keine Forward Secrecy[^1], und obwohl sie bestimmte Anforderungen erfüllen, die unsere obigen Empfehlungen nicht erfüllen, empfehlen wir sie nicht für langfristige oder sensible Kommunikation. Jede Kompromittierung eines Schlüssels zwischen den Empfängern einer Nachricht würde die Vertraulichkeit **aller** vergangenen Mitteilungen beeinträchtigen.

</div>

### Element

<div class="admonition recommendation" markdown>

![Element-Logo](assets/img/messengers/element.svg){ align=right }

**Element** ist der Flaggschiff-Client für das [Matrix](https://matrix.org/docs/chat_basics/matrix-for-im)-Protokoll, ein [offener Standard](https://spec.matrix.org/latest) für sichere dezentrale Echtzeitkommunikation.

Nachrichten und Dateien, die in privaten Räumen (für die eine Einladung erforderlich ist) geteilt werden, sind standardmäßig E2EE, ebenso wie persönliche Sprach- und Videoanrufe.

[:octicons-home-16: Homepage](https://element.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://element.io/privacy){ .card-link title="Datenschutzrichtlinie" }
[:octicons-info-16:](https://element.io/help){ .card-link title=Dokumentation}
[:octicons-code-16:](https://github.com/element-hq){ .card-link title="Quellcode" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=im.vector.app)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1083446067)
- [:simple-github: GitHub](https://github.com/element-hq/element-android/releases)
- [:fontawesome-brands-windows: Windows](https://element.io/download)
- [:simple-apple: macOS](https://element.io/download)
- [:simple-linux: Linux](https://element.io/download)
- [:octicons-globe-16: Web](https://app.element.io)

</details>

</div>

Profilbilder, Reaktionen und Spitznamen sind nicht verschlüsselt.

Gruppen-Sprach- und Videoanrufe sind [nicht](https://github.com/vector-im/element-web/issues/12878) E2EE und verwenden Jitsi, aber dies wird sich mit [Native Group VoIP Signalling](https://github.com/matrix-org/matrix-doc/pull/3401) ändern. Gruppenanrufe haben derzeit [keine Authentifizierung](https://github.com/vector-im/element-web/issues/13074), d. h., dass auch Personen, die nicht teil des Raumes sind, an den Anrufen teilnehmen können. Wir empfehlen, diese Funktion nicht für private Besprechungen zu verwenden.

Das Matrix-Protokoll selbst [unterstützt theoretisch Forward Secrecy](https://gitlab.matrix.org/matrix-org/olm/blob/master/docs/megolm.md#partial-forward-secrecy)[^1]. Dies wird jedoch [derzeit in Element nicht unterstützt](https://github.com/vector-im/element-web/issues/7101), da es einige Aspekte der Benutzerfreundlichkeit, wie z. B. das Schlüssel-Backup und den gemeinsamen Nachrichtenverlauf, beeinträchtigt.

Das Protokoll wurde 2016 einem unabhängigen [Audit](https://matrix.org/blog/2016/11/21/matrixs-olm-end-to-end-encryption-security-assessment-released-and-implemented-cross-platform-on-riot-at-last) unterzogen. Die Spezifikation des Matrix-Protokolls findest du in der entsprechenden [Dokumentation](https://spec.matrix.org/latest). Die von Matrix verwendete [kryptografische Olm Ratchet](https://matrix.org/docs/matrix-concepts/end-to-end-encryption) ist eine Implementierung des [Double-Ratchet-Algorithmus](https://signal.org/docs/specifications/doubleratchet) von Signal.

### Session

<div class="admonition recommendation" markdown>

![Session-Logo](assets/img/messengers/session.svg){ align=right }

**Session** ist ein dezentraler Messenger mit dem Schwerpunkt auf privater, sicherer und anonymer Kommunikation. Session bietet Unterstützung für Direktnachrichten, Gruppenchats und Sprachanrufe.

Session verwendet das dezentralisierte [Oxen Service Node Network](https://oxen.io) zum Speichern und Weiterleiten von Nachrichten. Jede verschlüsselte Nachricht wird über drei Knoten im Oxen Service Node Network geleitet, was es den Knoten praktisch unmöglich macht, aussagekräftige Informationen über die Nutzer des Netzwerks zu sammeln.

[:octicons-home-16: Homepage](https://getsession.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://getsession.org/privacy-policy){ .card-link title="Datenschutzrichtlinie" }
[:octicons-info-16:](https://getsession.org/faq){ .card-link title=Dokumentation}
[:octicons-code-16:](https://github.com/oxen-io){ .card-link title="Quellcode" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=network.loki.messenger)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1470168868)
- [:simple-github: GitHub](https://github.com/oxen-io/session-android/releases)
- [:fontawesome-brands-windows: Windows](https://getsession.org/download)
- [:simple-apple: macOS](https://getsession.org/download)
- [:simple-linux: Linux](https://getsession.org/download)

</details>

</div>

Session ermöglicht E2EE in Einzelchats oder geschlossenen Gruppen, die bis zu 100 Mitglieder umfassen können. Offene Gruppen haben keine Beschränkung für die Anzahl der Mitglieder, sondern sind von vornherein offen.

Session basierte früher auf dem Signal-Protokoll, bevor es im Dezember 2020 durch sein eigenes ersetzt wurde. Das Session-Protokoll unterstützt [keine](https://getsession.org/blog/session-protocol-technical-information) Forward-Secrecy.[^1]

Im März 2020 forderte Oxen ein unabhängiges Audit für Session an. Das Audit wurde im April 2021 [abgeschlossen](https://getsession.org/session-code-audit):

> Das allgemeine Sicherheitsniveau dieser Anwendung ist gut und macht sie für Menschen, die sich um ihre Privatsphäre sorgen, nutzbar.

Session hat ein [Whitepaper](https://arxiv.org/pdf/2002.04609.pdf), in dem die technischen Details der App und des Protokolls beschrieben werden.

## Kriterien

**Bitte beachte, dass wir mit keinem der Projekte, die wir empfehlen, in Verbindung stehen.** Zusätzlich zu unseren [Standardkriterien](about/criteria.md) haben wir eine Reihe klarer Anforderungen entwickelt, die es uns ermöglichen, objektive Empfehlungen zu geben. Wir empfehlen dir, dich mit der Liste vertraut zu machen, bevor du dich für ein Projekt entscheidest, und deine eigenen Recherchen anzustellen, um sicherzustellen, dass es die richtige Wahl für dich ist.

### Mindestanforderungen

- Hat Open-Source-Clients.
- Es ist nicht erforderlich, persönliche Identifikatoren (insbesondere Telefonnummern oder E-Mail-Adressen) mit Kontakten zu teilen.
- Verwendet standardmäßig E2EE für private Nachrichten.
- Unterstützt E2EE für alle Nachrichten.
- Wurde einem unabhängigen Audit unterzogen.

### Im besten Fall

Unsere Best-Case-Kriterien stellen dar, was wir uns von einem perfekten Projekt in dieser Kategorie wünschen würden. Unsere Empfehlungen enthalten möglicherweise keine oder nicht alle dieser Merkmale, aber diejenigen, die sie enthalten, werden möglicherweise höher eingestuft als andere auf dieser Seite.

- Unterstützt das Forward-Secrecy[^1]
- Unterstützt Future Secrecy (Post-Compromise-Sicherheit)[^2]
- Hat Open-Source-Server.
- Dezentralisiert, d.h. [Föderiert oder P2P](advanced/communication-network-types.md).
- Verwendet standardmäßig E2EE für alle Nachrichten.
- Unterstützt Linux, macOS, Windows, Android und iOS.

[^1]: Bei der [Forward Secrecy](https://en.wikipedia.org/wiki/Forward_secrecy) (dt.: „vorwärts gerichteten Geheimhaltung“) werden die Schlüssel sehr häufig gewechselt, so dass, wenn der aktuelle Verschlüsselungsschlüssel kompromittiert wird, nicht auch **frühere** Nachrichten offengelegt werden.
[^2]: Future Secrecy (oder Post-Compromise Security) ist eine Funktion, bei der ein Angreifer daran gehindert wird, **zukünftige** Nachrichten zu entschlüsseln, nachdem er einen privaten Schlüssel kompromittiert hat, es sei denn, er kompromittiert auch weitere Sitzungsschlüssel in der Zukunft. Dies zwingt den Angreifer dazu, die gesamte Kommunikation zwischen den Parteien abzufangen, da er den Zugang verliert, sobald ein Schlüsselaustausch stattfindet, der nicht abgefangen wird.
