---
meta_title: "Die besten privaten Instant Messengers - Privacy Guides"
title: Echtzeitkommunikation
icon: material/chat-processing
description: Verschlüsselte Messenger wie Signal und SimpleX schützen deine sensible Kommunikation vor neugierigen Blicken.
cover: real-time-communication.webp
---

<small>Schützt vor der/den folgenden Bedrohung(en):</small>

- [:material-bug-outline: Passive Angriffe](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: Diensteanbieter](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}
- [:material-eye-outline: Massenüberwachung](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-account-cash: Überwachungskapitalismus](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Diese Empfehlungen für verschlüsselte **Echtzeit-Kommunikation** sind gut um deine sensiblen Kommunikationen zu sichern. Diese Instant-Messenger kommen in Form von mehreren [Arten der Kommunikationsnetzwerke](advanced/communication-network-types.md) vor.

[:material-movie-open-play-outline: Video: It's time to stop using SMS](https://www.privacyguides.org/videos/2025/01/24/its-time-to-stop-using-sms-heres-why ""){.md-button}

## Signal

<div class="admonition recommendation" markdown>

![Signal logo](assets/img/messengers/signal.svg){ align=right }

**Signal** ist eine mobile App, die von Signal Messenger LLC entwickelt wurde. Die app beinhaltet Sofortnachrichten und Anrufe die mit dem Signal Protokoll geschützt werden, das Signal-Protokoll ist ein extrem sicheres Verschlüsselungsprotokoll, dass Forward Secrecy[^1] und Future Secrecy (Post-Compromise-Sicherheit)[^2] unterstützt.

[:octicons-home-16: Homepage](https://signal.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://signal.org/legal/#privacy-policy){ .card-link title="Datenschutzerklärung" }
[:octicons-info-16:](https://support.signal.org){ .card-link title="Dokumentation" }
[:octicons-code-16:](https://github.com/signalapp){ .card-link title="Quellcode" }
[:octicons-heart-16:](https://signal.org/donate){ .card-link title="beitragen" }

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

Signal braucht eine Telefonnummer für die Registrierung, aber du kannst einen Benutzernamen erstellen, um deine Telefonnummer vor deinen Kontakten zu verstecken:

1. Öffne in Signal die Einstellungen der App und tippe oben auf dein Kontoprofil.
2. In den Einstellungen, tippe auf deinem Namen und gehe auf **Benutzername**, danach tippe auf **Nutzername **.
3. Gebe einen Nutzernamen ein. Dein Benutzername wird immer mit einer zufälligen Kombination an Zahlen kombiniert, damit dein Name immer einzigartig ist und damit leute es nicht erraten können. Zum Beispiel, wenn du "John" als Benutzernamen eingibst, wird es als `@john.35` enden. Standardmäßig werden deinem Benutzernamen bei der Erstellung nur 2 Ziffern zugeordnet, aber du kannst weitere Ziffern hinzufügen, bis du die maximale Länge des Benutzernamens erreichst (32 Zeichen).
4. Gehe zurück zur Hauptseite der App-Einstellungen und wähle **Datenschutz**.
5. Wähle **Datenschutz** > **Telefonnummer**.
6. Ändere die **Wer kann meine Telefonnummer sehen** Einstellung auf **Niemand**.
7. (Optional) Ändere ebenfalls die **Wer kann mich anhand der Telefonnummer finden** auf **Niemand**, falls du verhindern willst, dass jemand der schon deine Telefonnummer hat, dein Signal Konto/Nutzername findet

Wir haben ebenfalls noch zusätzliche Tipps beim Einstellen und Härten deiner Signal Installation:

[Signal Einstellungen und Härtung :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening)

Kontaktlisten werden mit deinem Signal PIN verschlüsselt und der Server hat keinen Zugriff darauf. Persönliche Profile werden ebenfalls verschlüsselt und nur werden nur mit deinen Kontakten, mit denen du schreibst geteilt.

Signal unterstützt [private Gruppen](https://signal.org/blog/signal-private-group-system), wo der Server keine Aufzeichnungen der Gruppenmitglieder, Gruppentitel, Gruppenavatare oder Gruppenattribute hat. Signal hat minimale Metadaten wenn [Sealed Sender](https://signal.org/blog/sealed-sender) aktiviert wird. Die Absenderadresse und der Nachrichtenkörper werden verschlüsselt, nur die Empfängeradresse ist vom Server sichtbar. Sealed Sender ist nur für Leute in deiner Kontaktenliste aktiviert, aber es kann für alle Empfänger aktiviert werden, es gibt dann aber ein erhöhtes Risiko Spam zu erhalten.

Das Protokoll wurde unabhängig in 2016 [überprüft](https://eprint.iacr.org/2016/1013.pdf). Die Spezifikation für das Signalprotokoll kann in deren [Dokumentation](https://signal.org/docs) gefunden werden.

### Molly (Android)

If you use Android and your threat model requires protecting against [:material-target-account: Targeted Attacks](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red} you may consider using this alternative app, which features a number of security and usability improvements, to access the Signal network.

<div class="admonition recommendation" markdown>

![Molly-Logo](assets/img/messengers/molly.svg){ align=right }

**Molly** ist ein alternativer Signal-Client für Android, der es dir ermöglicht, die lokale Datenbank im Ruhezustand mit einer Passphrase zu verschlüsseln, ungenutzte RAM-Daten sicher zu schreddern, deine Verbindung über Tor zu leiten und [mehr](https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening#privacy-and-security-features). It also has usability improvements including scheduled backups, automatic locking, and the ability to use your Android phone as a linked device instead of the primary device for a Signal account.

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

Molly is updated every two weeks to include the latest features and bug fixes from Signal. The exception is security issues, which are patched as soon as possible. That said, you should be aware that there might be a slight delay compared to upstream, which may affect actions such as [migrating from Signal to Molly](https://github.com/mollyim/mollyim-android/wiki/Migrating-From-Signal#migrating-from-signal).

Note that you are trusting multiple parties by using Molly, as you now need to trust the Signal team *and* the Molly team to deliver safe and timely updates.

**Molly-FOSS** is a version of Molly which removes proprietary code like the Google services used by both Signal and Molly at the expense of some features (like battery-saving push notifications via Google Play Services). You can set up push notifications without Google Play Services in either version of Molly with [UnifiedPush](https://unifiedpush.org). Using this notification delivery method requires access to a [MollySocket](https://github.com/mollyim/mollysocket) server, but you can choose a public MollySocket instance for this.[^3]

Both versions of Molly provide the same security improvements and support [reproducible builds](https://github.com/mollyim/mollyim-android/tree/main/reproducible-builds), meaning it's possible to confirm that the compiled APKs match the source code.

## SimpleX Chat

<div class="admonition recommendation" markdown>

![SimpleX Chat logo](assets/img/messengers/simplex.svg){ align=right }

**SimpleX Chat** is an instant messenger that doesn't depend on any unique identifiers such as phone numbers or usernames. Sein dezentrales Netzwerk macht SimpleX Chat zu einem effektiven Werkzeug gegen [:material-close-outline: Zensur](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }.

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
- [:simple-flathub: Flathub](https://flathub.org/en/apps/chat.simplex.simplex)

</details>

</div>

SimpleX Chat provides direct messaging, group chats, and E2EE calls secured with the [SimpleX Messaging Protocol](https://github.com/simplex-chat/simplexmq/blob/stable/protocol/simplex-messaging.md), which uses double ratchet encryption with quantum resistance. Additionally, SimpleX Chat provides metadata protection by using unidirectional ["simplex queues"](https://github.com/simplex-chat/simplexmq/blob/stable/protocol/simplex-messaging.md#simplex-queue) to deliver messages.

To participate in conversations on SimpleX Chat, you must scan a QR code or click an invite link. This allows you to verify a contact out-of-band, which protects against man-in-the-middle attacks by network providers. Your data can be exported and imported onto another device, as there are no central servers where this is backed up.

You can find a full list of the privacy and security [features](https://github.com/simplex-chat/simplex-chat#privacy-and-security-technical-details-and-limitations) implemented in SimpleX Chat in the app's repository.

SimpleX Chat was independently audited in [July 2024](https://simplex.chat/blog/20241014-simplex-network-v6-1-security-review-better-calls-user-experience.html#simplex-cryptographic-design-review-by-trail-of-bits) and in [October 2022](https://simplex.chat/blog/20221108-simplex-chat-v4.2-security-audit-new-website).

## Briar

<div class="admonition recommendation" markdown>

![Briar logo](assets/img/messengers/briar.svg){ align=right }

**Briar** is an encrypted instant messenger that [connects](https://briarproject.org/how-it-works) to other clients using the [Tor network](alternative-networks.md#tor), making it an effective tool at circumventing [:material-close-outline: Censorship](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }. Briar kann sich auch über Wi-Fi oder Bluetooth verbinden, wenn sich die Geräte in der Nähe befinden. Dieser lokale Mesh-Modus von Briar kann nützlich sein, wenn die Internetverfügbarkeit ein Problem darstellt.

[:octicons-home-16: Homepage](https://briarproject.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://briarproject.org/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://code.briarproject.org/briar/briar/-/wikis/home){ .card-link title="Documentation" }
[:octicons-code-16:](https://code.briarproject.org/briar/briar){ .card-link title="Source Code" }
[:octicons-heart-16:](https://code.briarproject.org/briar/briar#donate){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.briarproject.briar.android)
- [:fontawesome-brands-windows: Windows](https://briarproject.org/download-briar-desktop)
- [:simple-linux: Linux](https://briarproject.org/download-briar-desktop)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.briarproject.Briar)

</details>

</div>

To add a contact on Briar, you must both add each other first. You can either exchange `briar://` links or scan a contact’s QR code if they are nearby.

Briar has a fully [published specification](https://code.briarproject.org/briar/briar-spec). Briar supports forward secrecy[^1] by using the Bramble [Handshake](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BHP.md) and [Transport](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BTP.md) protocol.

The client software was independently [audited](https://briarproject.org/news/2017-beta-released-security-audit), and the anonymous routing protocol uses the Tor network which has also been audited.

## Kriterien

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

### Mindestanforderungen

- Must have open-source clients.
- Must not require sharing personal identifiers (particularly phone numbers or emails) with contacts.
- Must use E2EE for private messages by default.
- Must support E2EE for all messages.
- Must support forward secrecy[^1]
- Es muss ein veröffentlichtes Audit von einem angesehenen, unabhängigen Dritten vorliegen.

### Im besten Fall

Unsere Best-Case-Kriterien stellen dar, was wir uns von einem perfekten Projekt in dieser Kategorie wünschen würden. Unsere Empfehlungen enthalten möglicherweise keine oder nicht alle dieser Merkmale, aber diejenigen, die sie enthalten, werden möglicherweise höher eingestuft als andere auf dieser Seite.

- Should support future secrecy (post-compromise security)[^2]
- Should have open-source servers.
- Should use a decentralized network, i.e. [federated or P2P](advanced/communication-network-types.md).
- Should use E2EE for all messages by default.
- Should support Linux, macOS, Windows, Android, and iOS.
[^3]: You may refer to this step-by-step tutorial in German on how to set up UnifiedPush as the notification provider for Molly: [https://kuketz-blog.de/messenger-wechsel-von-signal-zu-molly-unifiedpush-mollysocket-ntfy](https://kuketz-blog.de/messenger-wechsel-von-signal-zu-molly-unifiedpush-mollysocket-ntfy).

[^1]: [Forward secrecy](https://en.wikipedia.org/wiki/Forward_secrecy) is where keys are rotated very frequently, so that if the current encryption key is compromised, it does not expose **past** messages as well.
[^2]: Future secrecy (or [post-compromise security](https://eprint.iacr.org/2016/221.pdf)) is a feature where an attacker is prevented from decrypting **future** messages after compromising a private key, unless they compromise more session keys in the future as well. This effectively forces the attacker to intercept all communication between parties since they lose access as soon as a key exchange occurs that is not intercepted.
