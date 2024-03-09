---
meta_title: "The Best Private Instant Messengers - Privacy Guides"
title: "Real-Time Communicatie"
icon: material/chat-processing
description: Other instant messengers make all of your private conversations available to the company that runs them.
cover: real-time-communication.webp
---

Dit zijn onze aanbevelingen voor versleutelde real-time communicatie.

[Soorten communicatienetwerken :material-arrow-right-drop-circle:](./advanced/communication-network-types.md)

## Versleutelde Messengers

Deze boodschappers zijn geweldig voor het beveiligen van jouw gevoelige communicatie.

### Signal

<div class="admonition recommendation" markdown>

![Signal logo](assets/img/messengers/signal.svg){ align=right }

**Signal** is een mobiele app ontwikkeld door Signal Messenger LLC. The app provides instant messaging and calls secured with the Signal Protocol, an extremely secure encryption protocol which supports forward secrecy[^1] and post-compromise security.[^2]

[:octicons-home-16: Homepage](https://signal.org/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://signal.org/legal/#privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.signal.org/hc/en-us){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/signalapp){ .card-link title="Source Code" }
[:octicons-heart-16:](https://signal.org/donate/){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.thoughtcrime.securesms)
- [:simple-appstore: App Store](https://apps.apple.com/app/id874139669)
- [:simple-android: Android](https://signal.org/android/apk/)
- [:simple-windows11: Windows](https://signal.org/download/windows)
- [:simple-apple: macOS](https://signal.org/download/macos)
- [:simple-linux: Linux](https://signal.org/download/linux)

</details>

</div>

Signal requires your phone number for registration, however you should create a username to hide your phone number from your contacts:

1. In Signal, open the app's settings and tap your account profile at the top.
2. Tap **Username** and choose **Continue** on the "Set up your Signal username" screen.
3. Enter a username. Your username will always be paired with a unique set of digits to keep your username unique and prevent people from guessing it, for example if you enter "John" your username might end up being `@john.35`.
4. Go back to the main app settings page and select **Privacy**.
5. Select **Phone Number**
6. Change the **Who Can See My Number** setting to: **Nobody**

You can optionally change the **Who Can Find Me By Number** setting to **Nobody** as well, if you want to prevent people who already have your phone number from discovering your Signal account/username.

Contact lists on Signal are encrypted using your Signal PIN and the server does not have access to them. Persoonlijke profielen worden ook versleuteld en alleen gedeeld met contacten waarmee je chat. Signal supports [private groups](https://signal.org/blog/signal-private-group-system/), where the server has no record of your group memberships, group titles, group avatars, or group attributes. Signaal heeft minimale metadata wanneer [Verzegelde Afzender](https://signal.org/blog/sealed-sender/) is ingeschakeld. Het afzenderadres is versleuteld samen met de inhoud van het bericht, en alleen het adres van de ontvanger is zichtbaar voor de server. Verzegelde afzender is alleen ingeschakeld voor mensen in uw contactenlijst, maar kan ingeschakeld zijn voor alle ontvangers met een verhoogd risico om spam te ontvangen.

Het protocol was onafhankelijk [gecontroleerd](https://eprint.iacr.org/2016/1013.pdf) in 2016. De specificatie van het Signaal-protocol kan worden gevonden in hun [documentatie](https://signal.org/docs/).

We hebben nog enkele extra tips over het configureren en verharden van jouw signaalinstallatie:

[Signaalconfiguratie en Hardening :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening/)

### SimpleX Chat

<div class="admonition recommendation" markdown>

![Simplex logo](assets/img/messengers/simplex.svg){ align=right }

**SimpleX** Chat is een instant messenger die gedecentraliseerd is en niet afhankelijk is van unieke identifiers zoals telefoonnummers of gebruikersnamen. Berichten en bestanden die in privéruimten worden gedeeld (waarvoor een uitnodiging nodig is) zijn standaard E2EE, net als één-op-één spraak- en videogesprekken.

[:octicons-home-16: Homepage](https://simplex.chat){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/simplex-chat/simplex-chat/blob/stable/PRIVACY.md){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/simplex-chat/simplex-chat/tree/stable/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/simplex-chat){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=chat.simplex.app)
- [:simple-appstore: App Store](https://apps.apple.com/us/app/simplex-chat/id1605771084)
- [:simple-github: GitHub](https://github.com/simplex-chat/simplex-chat/releases)
- [:simple-windows11: Windows](https://simplex.chat/downloads/#desktop-app)
- [:simple-apple: macOS](https://simplex.chat/downloads/#desktop-app)
- [:simple-linux: Linux](https://simplex.chat/downloads/#desktop-app)

</details>

</div>

SimpleX Chat [werd gecontroleerd](https://simplex.chat/blog/20221108-simplex-chat-v4.2-security-audit-new-website.html) door Trail Bits in oktober 2022.

SimpleX Chat supports basic group chatting functionality, direct messaging, and editing of messages and markdown. E2EE audio- en video-oproepen worden ook ondersteund. Jouw gegevens kunnen worden geëxporteerd en geïmporteerd naar een ander apparaat, omdat er geen centrale servers zijn waar een back-up van wordt gemaakt.

### Briar

<div class="admonition recommendation" markdown>

![Briar logo](assets/img/messengers/briar.svg){ align=right }

**Briar** is een versleutelde instant messenger die [connects](https://briarproject.org/how-it-works/) gebruikt voor andere clients via het Tor Netwerk. Briar kan ook verbinding maken via Wi-Fi of Bluetooth wanneer hij in de buurt is. Briar's lokale mesh-modus kan nuttig zijn wanneer de beschikbaarheid van internet een probleem is.

[:octicons-home-16: Homepage](https://briarproject.org/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://briarproject.org/privacy-policy/){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://code.briarproject.org/briar/briar/-/wikis/home){ .card-link title=Documentation}
[:octicons-code-16:](https://code.briarproject.org/briar/briar){ .card-link title="Source Code" }
[:octicons-heart-16:](https://briarproject.org/){ .card-link title="Donation options are listed on the bottom of the homepage" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.briarproject.briar.android)
- [:simple-windows11: Windows](https://briarproject.org/download-briar-desktop/)
- [:simple-linux: Linux](https://briarproject.org/download-briar-desktop/)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.briarproject.Briar)

</details>

</div>

Om een contact toe te voegen aan Briar, moet je eerst beide elkaar toevoegen. Je kunt `briar://` links ruilen of de QR-code van een contactpersoon scannen als deze dichtbij zijn.

De clientsoftware was onafhankelijk [gecontroleerd](https://briarproject.org/news/2017-beta-released-security-audit/), en het anonieme routing protocol maakt gebruik van het Tor netwerk dat ook is gecontroleerd.

Briar heeft een volledig [gepubliceerde specificatie](https://code.briarproject.org/briar/briar-spec).

Briar supports forward secrecy[^1] by using the Bramble [Handshake](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BHP.md) and [Transport](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BTP.md) protocol.

## Aanvullende opties

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

These messengers do not have forward secrecy[^1], and while they fulfill certain needs that our previous recommendations may not, we do not recommend them for long-term or sensitive communications. Elke compromittering van sleutels tussen ontvangers van berichten zou de vertrouwelijkheid van **alle** eerdere communicaties aantasten.

</div>

### Element

<div class="admonition recommendation" markdown>

![Element logo](assets/img/messengers/element.svg){ align=right }

**Element** is the reference [client](https://matrix.org/ecosystem/clients/) for the [Matrix](https://matrix.org/docs/guides/introduction) protocol, an [open standard](https://matrix.org/docs/spec) for secure decentralized real-time communication.

Berichten en bestanden die in privéruimten worden gedeeld (waarvoor een uitnodiging nodig is) zijn standaard E2EE, net als één-op-één spraak- en videogesprekken.

[:octicons-home-16: Homepage](https://element.io/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://element.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://element.io/help){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/element-hq){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=im.vector.app)
- [:simple-appstore: App Store](https://apps.apple.com/app/vector/id1083446067)
- [:simple-github: GitHub](https://github.com/vector-im/element-android/releases)
- [:simple-windows11: Windows](https://element.io/get-started)
- [:simple-apple: macOS](https://element.io/get-started)
- [:simple-linux: Linux](https://element.io/get-started)
- [:octicons-globe-16: Web](https://app.element.io)

</details>

</div>

Profielfoto's, reacties en bijnamen zijn niet versleuteld.

Groepsgesprekken voor spraak en video zijn [niet](https://github.com/vector-im/element-web/issues/12878) E2EE, en gebruiken Jitsi, maar dit zal naar verwachting veranderen met [Native Group VoIP Signalling](https://github.com/matrix-org/matrix-doc/pull/3401). Groepsgesprekken hebben [momenteel geen authenticatie](https://github.com/vector-im/element-web/issues/13074), wat betekent dat ook deelnemers van buiten de zaal aan de gesprekken kunnen deelnemen. Wij raden je aan deze functie niet te gebruiken voor privévergaderingen.

The Matrix protocol itself [theoretically supports forward secrecy](https://gitlab.matrix.org/matrix-org/olm/blob/master/docs/megolm.md#partial-forward-secrecy)[^1], however this is [not currently supported in Element](https://github.com/vector-im/element-web/issues/7101) due to it breaking some aspects of the user experience such as key backups and shared message history.

Het protocol is in 2016 onafhankelijk [gecontroleerd](https://matrix.org/blog/2016/11/21/matrixs-olm-end-to-end-encryption-security-assessment-released-and-implemented-cross-platform-on-riot-at-last). De specificatie van het Matrix-protocol is te vinden in hun [documentatie](https://spec.matrix.org/latest/). The [Olm cryptographic ratchet](https://matrix.org/docs/matrix-concepts/end-to-end-encryption/) used by Matrix is an implementation of Signal’s [Double Ratchet algorithm](https://signal.org/docs/specifications/doubleratchet/).

### Session

<div class="admonition recommendation" markdown>

![Session logo](assets/img/messengers/session.svg){ align=right }

**Session** is een gedecentraliseerde messenger met een focus op private, veilige en anonieme communicatie. Session biedt ondersteuning voor directe berichten, groepschats en spraakoproepen.

Session maakt gebruik van het gedecentraliseerde [Oxen Service Node Network](https://oxen.io/) om berichten op te slaan en te routeren. Elk versleuteld bericht wordt door drie knooppunten in het Oxen Service Node Network geleid, waardoor het voor de knooppunten vrijwel onmogelijk wordt zinvolle informatie te verzamelen over degenen die het netwerk gebruiken.

[:octicons-home-16: Homepage](https://getsession.org/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://getsession.org/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://getsession.org/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/oxen-io){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=network.loki.messenger)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1470168868)
- [:simple-github: GitHub](https://github.com/oxen-io/session-android/releases)
- [:simple-windows11: Windows](https://getsession.org/download)
- [:simple-apple: macOS](https://getsession.org/download)
- [:simple-linux: Linux](https://getsession.org/download)

</details>

</div>

Session maakt E2EE mogelijk in één-op-één chats of gesloten groepen met maximaal 100 leden. Open groepen hebben geen beperking wat het aantal leden betreft, maar zijn open van opzet.

Session was previously based on Signal Protocol before replacing it with their own in December 2020. Session Protocol does [not](https://getsession.org/blog/session-protocol-technical-information) support forward secrecy.[^1]

Oxen requested an independent audit for Session in March 2020. The audit [concluded](https://getsession.org/session-code-audit) in April 2021, “The overall security level of this application is good and makes it usable for privacy-concerned people.”

Session has a [whitepaper](https://arxiv.org/pdf/2002.04609.pdf) describing the technical details of the app and protocol.

## Criteria

**Wij zijn niet verbonden aan de projecten die wij aanbevelen.** Naast [onze standaardcriteria](about/criteria.md)hebben wij een duidelijke reeks eisen ontwikkeld om objectieve aanbevelingen te kunnen doen. Wij stellen voor dat je jezelf vertrouwd maakt met deze lijst voordat je een project kiest, en jouw eigen onderzoek uitvoert om er zeker van te zijn dat je de juiste keuze maakt.

<div class="admonition example" markdown>
<p class="admonition-title">This section is new</p>

We werken aan het vaststellen van gedefinieerde criteria voor elk deel van onze site, en dit kan onderhevig zijn aan verandering. Als je vragen hebt over onze criteria, stel ze dan [op ons forum](https://discuss.privacyguides.net/latest) en neem niet aan dat we iets niet in overweging hebben genomen bij het opstellen van onze aanbevelingen als het hier niet vermeld staat. Er zijn veel factoren die worden overwogen en besproken wanneer wij een project aanbevelen, en het documenteren van elke factor is een werk in uitvoering.

</div>

- Has open-source clients.
- Does not require sharing personal identifiers (phone numbers or emails in particular) with contacts.
- Uses E2EE for private messages by default.
- Supports E2EE for all messages.
- Has been independently audited.

### Beste geval

Onze best-case criteria geven aan wat wij zouden willen zien van het perfecte project in deze categorie. Het is mogelijk dat onze aanbevelingen geen of niet alle functies bevatten, maar degene die dat wel doen kunnen hoger gerangschikt worden dan andere op deze pagina.

- Supports Forward Secrecy[^1]
- Supports Future Secrecy (Post-Compromise Security)[^2]
- Has open-source servers.
- Decentralized, i.e. [federated or P2P](advanced/communication-network-types.md).
- Uses E2EE for all messages by default.
- Supports Linux, macOS, Windows, Android, and iOS.

[^1]: [Forward Secrecy](https://en.wikipedia.org/wiki/Forward_secrecy) is where keys are rotated very frequently, so that if the current encryption key is compromised, it does not expose **past** messages as well.
[^2]: Future Secrecy (or Post-Compromise Security) is a feature where an attacker is prevented from decrypting **future** messages after compromising a private key, unless they compromise more session keys in the future as well. This effectively forces the attacker to intercept all communication between parties, since they lose access as soon as a key exchange occurs that is not intercepted.
