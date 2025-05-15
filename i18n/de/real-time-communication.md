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

These are our recommendations for encrypted **real-time communication**. These come in the form of many [types of communication networks](./advanced/communication-network-types.md).

[:material-movie-open-play-outline: Video: It's time to stop using SMS](https://www.privacyguides.org/videos/2025/01/24/its-time-to-stop-using-sms-heres-why ""){.md-button}

## Verschlüsselte Messenger

Diese Messenger eignen sich hervorragend zur Sicherung deiner sensiblen Kommunikation.

### Signal

<div class="admonition recommendation" markdown>

![Signal logo](assets/img/messengers/signal.svg){ align=right }

**Signal** ist eine mobile App, die von Signal Messenger LLC entwickelt wurde. Die App bietet Instant Messaging und Anrufe, die mit dem Signal-Protokoll gesichert sind, einem extrem sicheren Verschlüsselungsprotokoll, dass Forward Secrecy[^1] und Post-Compromise Security[^2] unterstützt.

[:octicons-home-16: Homepage](https://signal.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://signal.org/legal/#privacy-policy){ .card-link title="Datenschutzerklärung" }
[:octicons-info-16:](https://support.signal.org){ .card-link title="Dokumentation" }
[:octicons-code-16:](https://github.com/signalapp){ .card-link title="Quellcode" }
[:octicons-heart-16:](https://signal.org/donate){ .card-link title="Spenden" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.thoughtcrime.securesms)
- [:simple-appstore: App Store](https://apps.apple.com/app/id874139669)
- [:simple-github: GitHub](https://github.com/signalapp/Signal-Android/releases)
- [:simple-android: Android](https://signal.org/android/apk)
- [:fontawesome-brands-windows: Windows](https://signal.org/de/download/windows)
- [:simple-apple: macOS](https://signal.org/de/download/macos)
- [:simple-linux: Linux](https://signal.org/de/download/linux)

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

**Molly** ist ein alternativer Signal-Client für Android, der es dir ermöglicht, die lokale Datenbank im Ruhezustand mit einer Passphrase zu verschlüsseln, ungenutzte RAM-Daten sicher zu schreddern, deine Verbindung über Tor zu leiten und [mehr](https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening#privacy-and-security-features). Es gibt auch Verbesserungen bei der Benutzerfreundlichkeit, darunter geplante Backups, automatisches Sperren, Unterstützung für [UnifiedPush](https://unifiedpush.org) und die Möglichkeit, dein Android-Telefon als verknüpftes Gerät anstelle des Hauptgeräts für ein Signal-Konto zu verwenden.

[:octicons-home-16: Homepage](https://molly.im){ .md-button .md-button--primary }
[:octicons-eye-16:](https://signal.org/legal/#privacy-policy){ .card-link title="Datenschutzerklärung" }
[:octicons-info-16:](https://github.com/mollyim/mollyim-android/wiki){ .card-link title="Dokumentation" }
[:octicons-code-16:](https://github.com/mollyim/mollyim-android){ .card-link title="Quellcode" }
[:octicons-heart-16:](https://opencollective.com/mollyim){ .card-link title="Spenden" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-fdroid: F-Droid](https://molly.im/fdroid)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/im.molly.app)
- [:simple-github: GitHub](https://github.com/mollyim/mollyim-android/releases)

</details>

</div>

Molly wird alle zwei Wochen aktualisiert, um die neuesten Funktionen und Fehlerbehebungen von Signal einzubinden. Die Ausnahme sind Sicherheitsprobleme, die so schnell wie möglich behoben werden. Allerdings solltest du dir darüber im Klaren sein, dass es zu einer leichten Verzögerung im Vergleich zum Upstream kommen kann, was sich auf Aktionen wie die [Migration von Signal zu Molly](https://github.com/mollyim/mollyim-android/wiki/Migrating-From-Signal#migrating-from-signal) auswirken kann.

Beachte, dass du durch die Verwendung von Molly mehreren Parteien vertraust, da du nun dem Signal-Team *und dem* Molly-Team vertrauen musst, dass sie sichere und rechtzeitige Aktualisierungen liefern.

There is a version of Molly called **Molly-FOSS** which removes proprietary code like the Google services used by both Signal and Molly, at the expense of some features like battery-saving push notifications via Google Play Services. You can regain push notifications without Google Play Services in either version of Molly with [UnifiedPush](https://unifiedpush.org), but it requires running a separate program called [Mollysocket](https://github.com/mollyim/mollysocket) on another device to function. Mollysocket can either be self-hosted on a separate computer or server (VPS), or alternatively a public Mollysocket instance can be used ([step-by-step tutorial, in German](https://kuketz-blog.de/messenger-wechsel-von-signal-zu-molly-unifiedpush-mollysocket-ntfy)).

Alle Versionen von Molly bieten die gleichen Sicherheitsverbesserungen.

Molly und Molly-FOSS unterstützen [reproduzierbare Builds](https://github.com/mollyim/mollyim-android/tree/main/reproducible-builds), d. h. es ist möglich zu bestätigen, dass die kompilierten APKs mit dem Quellcode übereinstimmen.

### SimpleX Chat

<div class="admonition recommendation" markdown>

![Simplex-Logo](assets/img/messengers/simplex.svg){ align=right }

**SimpleX Chat** ist ein Instant Messenger, der ohne eindeutigen Identifikatoren wie Telefonnummern oder Benutzernamen auskommt. Sein dezentrales Netzwerk macht SimpleX Chat zu einem effektiven Werkzeug gegen [:material-close-outline: Zensur](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }.

[:octicons-home-16: Homepage](https://simplex.chat){ .md-button .md-button--primary }
[:octicons-eye-16:](https://simplex.chat/privacy){ .card-link title="Datenschutzerklärung" }
[:octicons-info-16:](https://simplex.chat/docs/simplex.html){ .card-link title="Dokumentation" }
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

SimpleX provides direct messaging, group chats, and E2EE calls secured with the [SimpleX Messaging Protocol](https://github.com/simplex-chat/simplexmq/blob/stable/protocol/simplex-messaging.md), which uses double ratchet encryption with quantum resistance. Additionally, SimpleX Chat provides metadata protection by using unidirectional ["simplex queues"](https://github.com/simplex-chat/simplexmq/blob/stable/protocol/simplex-messaging.md#simplex-queue) to deliver messages.

To participate in conversations on SimpleX Chat, you must scan a QR code or click an invite link. This allows you to verify a contact out-of-band, which protects against man-in-the-middle attacks by network providers. Your data can be exported and imported onto another device, as there are no central servers where this is backed up.

Eine vollständige Liste der in SimpleX Chat implementierten [Datenschutz- und Sicherheitsfunktionen](https://github.com/simplex-chat/simplex-chat#privacy-and-security-technical-details-and-limitations) findest du im Repository der App.

SimpleX Chat wurde im [Juli 2024](https://simplex.chat/blog/20241014-simplex-network-v6-1-security-review-better-calls-user-experience.html#simplex-cryptographic-design-review-by-trail-of-bits) und im [Oktober 2022](https://simplex.chat/blog/20221108-simplex-chat-v4.2-security-audit-new-website) unabhängig geprüft.

### Briar

<div class="admonition recommendation" markdown>

![Briar-Logo](assets/img/messengers/briar.svg){ align=right }

**Briar** ist ein verschlüsselter Instant-Messenger, der sich mit anderen Geräten [über das Tor-Netzwerk verbindet](https://briarproject.org/how-it-works). Das macht es zu einem effektiven Werkzeug zur Umgehung von [:material-close-outline: Zensur](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }. Briar kann sich auch über Wi-Fi oder Bluetooth verbinden, wenn sich die Geräte in der Nähe befinden. Dieser lokale Mesh-Modus von Briar kann nützlich sein, wenn die Internetverfügbarkeit ein Problem darstellt.

[:octicons-home-16: Homepage](https://briarproject.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://briarproject.org/privacy-policy){ .card-link title="Datenschutzerklärung" }
[:octicons-info-16:](https://code.briarproject.org/briar/briar/-/wikis/home){ .card-link title="Dokumentation" }
[:octicons-code-16:](https://code.briarproject.org/briar/briar){ .card-link title="Quellcode" }
[:octicons-heart-16:](https://briarproject.org){ .card-link title="Spendenoptionen sind unten auf der Homepage aufgeführt" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.briarproject.briar.android)
- [:fontawesome-brands-windows: Windows](https://briarproject.org/download-briar-desktop)
- [:simple-linux: Linux](https://briarproject.org/download-briar-desktop)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.briarproject.Briar)

</details>

</div>

To add a contact on Briar, you must both add each other first. You can either exchange `briar://` links or scan a contact’s QR code if they are nearby.

The client software was independently [audited](https://briarproject.org/news/2017-beta-released-security-audit), and the anonymous routing protocol uses the Tor network which has also been audited.

Briar has a fully [published specification](https://code.briarproject.org/briar/briar-spec).

Briar supports forward secrecy[^1] by using the Bramble [Handshake](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BHP.md) and [Transport](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BTP.md) protocol.

## Weitere Optionen

<div class="admonition warning" markdown>
<p class="admonition-title">Warnung</p>

Diese Messenger haben keine Forward Secrecy[^1], und obwohl sie bestimmte Anforderungen erfüllen, die unsere obigen Empfehlungen nicht erfüllen, empfehlen wir sie nicht für langfristige oder sensible Kommunikation. Jede Kompromittierung eines Schlüssels zwischen den Empfängern einer Nachricht würde die Vertraulichkeit **aller** vergangenen Mitteilungen beeinträchtigen.

</div>

### Session

<div class="admonition recommendation" markdown>

![Session-Logo](assets/img/messengers/session.svg){ align=right }

**Session** ist ein dezentraler Messenger mit dem Schwerpunkt auf privater, sicherer und anonymer Kommunikation. Session bietet Unterstützung für Direktnachrichten, Gruppenchats und Sprachanrufe.

Session verwendet das dezentralisierte [Oxen Service Node Network](https://oxen.io) zum Speichern und Weiterleiten von Nachrichten. Jede verschlüsselte Nachricht wird über drei Knoten im Oxen Service Node Network geleitet, was es den Knoten praktisch unmöglich macht, aussagekräftige Informationen über die Nutzer des Netzwerks zu sammeln.

[:octicons-home-16: Homepage](https://getsession.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://getsession.org/privacy-policy){ .card-link title="Datenschutzerklärung" }
[:octicons-info-16:](https://getsession.org/faq){ .card-link title="Dokumentation" }
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

Session allows for E2EE in one-on-one chats or closed groups which allow for up to 100 members. It is also possible to [set up](https://docs.oxen.io/oxen-docs/products-built-on-oxen/session/guides/open-group-setup) or join open groups which can host thousands of members, but messages in these open groups are **not** end-to-end encrypted between participants.

Session was previously based on Signal Protocol before replacing it with their own in December 2020. Session Protocol does [not](https://getsession.org/blog/session-protocol-technical-information) support forward secrecy.[^1]

Oxen requested an independent audit for Session in March 2020. The audit [concluded](https://getsession.org/session-code-audit) in April 2021:

> Das allgemeine Sicherheitsniveau dieser Anwendung ist gut und macht sie für Menschen, die sich um ihre Privatsphäre sorgen, nutzbar.

Session has a [white paper](https://arxiv.org/pdf/2002.04609.pdf) describing the technical details of the app and protocol.

## Kriterien

**Bitte beachte, dass wir mit keinem der Projekte, die wir empfehlen, in Verbindung stehen.** Zusätzlich zu [unseren Standardkriterien](about/criteria.md) haben wir eine Reihe klarer Anforderungen entwickelt, die es uns ermöglichen, objektive Empfehlungen zu geben. Wir empfehlen dir, dich mit der Liste vertraut zu machen, bevor du dich für ein Projekt entscheidest, und deine eigenen Recherchen anzustellen, um sicherzustellen, dass es die richtige Wahl für dich ist.

### Mindestanforderungen

- Hat Open-Source-Clients.
- Es ist nicht erforderlich, persönliche Identifikatoren (insbesondere Telefonnummern oder E-Mail-Adressen) mit Kontakten zu teilen.
- Verwendet standardmäßig E2EE für private Nachrichten.
- Unterstützt E2EE für alle Nachrichten.
- Wurde einem unabhängigen Audit unterzogen.

### Im besten Fall

Unsere Best-Case-Kriterien stellen dar, was wir uns von einem perfekten Projekt in dieser Kategorie wünschen würden. Unsere Empfehlungen enthalten möglicherweise keine oder nicht alle dieser Merkmale, aber diejenigen, die sie enthalten, werden möglicherweise höher eingestuft als andere auf dieser Seite.

- Supports forward secrecy[^1]
- Unterstützt Future Secrecy (Post-Compromise-Sicherheit)[^2]
- Hat Open-Source-Server.
- Dezentralisiert, d.h. [Föderiert oder P2P](advanced/communication-network-types.md).
- Verwendet standardmäßig E2EE für alle Nachrichten.
- Unterstützt Linux, macOS, Windows, Android und iOS.

[^1]: [Forward secrecy](https://en.wikipedia.org/wiki/Forward_secrecy) is where keys are rotated very frequently, so that if the current encryption key is compromised, it does not expose **past** messages as well.
[^2]: Future Secrecy (oder Post-Compromise Security) ist eine Funktion, bei der ein Angreifer daran gehindert wird, **zukünftige** Nachrichten zu entschlüsseln, nachdem er einen privaten Schlüssel kompromittiert hat, es sei denn, er kompromittiert auch weitere Sitzungsschlüssel in der Zukunft. Dies zwingt den Angreifer dazu, die gesamte Kommunikation zwischen den Parteien abzufangen, da er den Zugang verliert, sobald ein Schlüsselaustausch stattfindet, der nicht abgefangen wird.
