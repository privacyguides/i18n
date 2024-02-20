---
meta_title: "Le migliori app di messaggistica istantanea private - Privacy Guides"
title: "Comunicazione in tempo reale"
icon: material/chat-processing
description: Le altre app di messaggistica istantanea rendono disponibili tutte le tue conversazioni private all'azienda che le gestisce.
cover: real-time-communication.webp
---

Questi sono i nostri consigli per le comunicazioni crittografate in tempo reale.

[Tipi di reti di comunicazione :material-arrow-right-drop-circle:](./advanced/communication-network-types.md)

## Messaggistica Crittografata

Queste app di messaggistica sono ottime per proteggere le tue comunicazioni sensibili.

### Signal

<div class="admonition recommendation" markdown>

![Logo di Signal](assets/img/messengers/signal.svg){ align=right }

**Signal** è un'app per dispositivi mobili sviluppata da Signal Messenger LLC. The app provides instant messaging and calls secured with the Signal Protocol, an extremely secure encryption protocol which supports forward secrecy[^1] and post-compromise security.[^2]

[:octicons-home-16: Homepage](https://signal.org/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://signal.org/legal/#privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.signal.org/hc/en-us){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/signalapp){ .card-link title="Source Code" }
[:octicons-heart-16:](https://signal.org/donate/){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Scarica</summary>

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

Contact lists on Signal are encrypted using your Signal PIN and the server does not have access to them. Inoltre, i profili personali sono crittografati e condivisi esclusivamente con i contatti con cui parli. Signal supports [private groups](https://signal.org/blog/signal-private-group-system/), where the server has no record of your group memberships, group titles, group avatars, or group attributes. Signal ha metadati minimi quando [Mittente sigillato](https://signal.org/blog/sealed-sender/) è abilitato. L'indirizzo del mittente è crittografato insieme al corpo del messaggio e soltanto l'indirizzo del destinatario è visibile al server. Mittente Sigillato è abilitato esclusivamente per i tuoi contatti, ma è attivabile per tutti i destinatari con il rischio incrementato di ricevere spam.

Il protocollo è stato [controllato](https://eprint.iacr.org/2016/1013.pdf) indipendentemente nel 2016. Le specifiche per il protocollo di Signal si possono trovare nella sua [documentazione](https://signal.org/docs/).

Abbiamo alcuni consigli aggiuntivi sulla configurazione e rafforzamento della tua installazione di Signal:

[Configurazione e Rafforzamento di Signal :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening/)

### SimpleX Chat

<div class="admonition recommendation" markdown>

![Logo di Simplex](assets/img/messengers/simplex.svg){ align=right }

**SimpleX** Chat è un'app di messaggistica istantanea decentralizzata che non dipende da alcun identificatore univoco, come numeri telefonici o nomi utente. Gli utenti di SimpleX Chat possono scansionare un codice QR o cliccare su un link di invito per partecipare alle conversazioni di gruppo.

[:octicons-home-16: Homepage](https://simplex.chat){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/simplex-chat/simplex-chat/blob/stable/PRIVACY.md){ .card-link title="Informativa sulla Privacy" }
[:octicons-info-16:](https://github.com/simplex-chat/simplex-chat/tree/stable/docs){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/simplex-chat){ .card-link title="Codice sorgente" }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=chat.simplex.app)
- [:simple-appstore: App Store](https://apps.apple.com/us/app/simplex-chat/id1605771084)
- [:simple-github: GitHub](https://github.com/simplex-chat/simplex-chat/releases)
- [:simple-windows11: Windows](https://simplex.chat/downloads/#desktop-app)
- [:simple-apple: macOS](https://simplex.chat/downloads/#desktop-app)
- [:simple-linux: Linux](https://simplex.chat/downloads/#desktop-app)

</details>

</div>

SimpleX Chat [è stato controllato](https://simplex.chat/blog/20221108-simplex-chat-v4.2-security-audit-new-website.html) da Trail of Bits a ottobre 2022.

SimpleX Chat supporta le funzionalità di base per le chat di gruppo, messaggi diretti, e la modifica dei messaggi e del Markdown. Sono supportate anche le chiamate e le videochiamate in E2EE. I dati possono essere esportati e importati su un altro dispositivo, poiché non esistono server centrali in cui ne è eseguito il backup.

### Briar

<div class="admonition recommendation" markdown>

![Logo di Briar](assets/img/messengers/briar.svg){ align=right }

**Briar** è un'app di messaggistica istantanea crittografata che si [connette](https://briarproject.org/how-it-works/) ad altri client utilizzando la Rete di Tor. Briar può anche connettersi via Wi-Fi o Bluetooth quando si trova nelle vicinanze. La modalità mesh locale di Briar può essere utile quando la connessione a Internet è problematica.

[:octicons-home-16: Homepage](https://briarproject.org/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://briarproject.org/privacy-policy/){ .card-link title="Informativa sulla Privacy" }
[:octicons-info-16:](https://code.briarproject.org/briar/briar/-/wikis/home){ .card-link title=Documentazione}
[:octicons-code-16:](https://code.briarproject.org/briar/briar){ .card-link title="Codice sorgente" }
[:octicons-heart-16:](https://briarproject.org/){ .card-link title="Le opzioni per donare sono elencate in fondo alla homepage" }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.briarproject.briar.android)
- [:simple-windows11: Windows](https://briarproject.org/download-briar-desktop/)
- [:simple-linux: Linux](https://briarproject.org/download-briar-desktop/)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.briarproject.Briar)

</details>

</div>

Per aggiungere un contatto su Briar, è necessario prima aggiungersi a vicenda. Puoi scambiare i link `briar://` o scansionare il codice QR di un contatto, se è nelle vicinanze.

Il software per il client è stato [controllato](https://briarproject.org/news/2017-beta-released-security-audit/) indipendentemente, così come il protocollo anonimo di trasmissione che utilizza la Rete di Tor.

Briar ha [pubblicato le specifiche](https://code.briarproject.org/briar/briar-spec) complete.

Briar supports forward secrecy[^1] by using the Bramble [Handshake](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BHP.md) and [Transport](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BTP.md) protocol.

## Opzioni Aggiuntive

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

These messengers do not have forward secrecy[^1], and while they fulfill certain needs that our previous recommendations may not, we do not recommend them for long-term or sensitive communications. Qualsiasi compromissione di chiavi tra i destinatari del messaggio, influenzerebbe la confidenzialità di **tutte** le comunicazioni precedenti.

</div>

### Element

<div class="admonition recommendation" markdown>

![Logo Element](assets/img/messengers/element.svg){ align=right }

**Element** è il [client](https://matrix.org/ecosystem/clients/) di riferimento per il protocollo [Matrix](https://matrix.org/docs/guides/introduction), uno [standard aperto](https://matrix.org/docs/spec) per la comunicazione decentralizzata sicura in tempo reale.

I messaggi e i file condivisi nelle stanze private (che richiedono un invito), sono di default in E2EE, così come le chiamate e videochiamate tra due persone.

[:octicons-home-16: Homepage](https://element.io/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://element.io/privacy){ .card-link title="Informativa sulla Privacy" }
[:octicons-info-16:](https://element.io/help){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/vector-im){ .card-link title="Codice sorgente" }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=im.vector.app)
- [:simple-appstore: App Store](https://apps.apple.com/app/vector/id1083446067)
- [:simple-github: GitHub](https://github.com/vector-im/element-android/releases)
- [:simple-windows11: Windows](https://element.io/get-started)
- [:simple-apple: macOS](https://element.io/get-started)
- [:simple-linux: Linux](https://element.io/get-started)
- [:octicons-globe-16: Web](https://app.element.io)

</details>

</div>

Le immagini del profilo, le reazioni e i nomi utente non sono crittografati.

Le chiamate e le videochiamate [non](https://github.com/vector-im/element-web/issues/12878) sono in E2EE e utilizzano Jitsi, ma ciò cambierà con la [Segnalazione Nativa VoIP del Gruppo](https://github.com/matrix-org/matrix-doc/pull/3401). Le chiamate di gruppo, correntemente, non dispongono di [autenticazione](https://github.com/vector-im/element-web/issues/13074), a significare che i non partecipanti alla stanza, possono anche unirsi alle chiamate. Consigliamo di non utilizzare questa funzionalità per le riunioni private.

The Matrix protocol itself [theoretically supports forward secrecy](https://gitlab.matrix.org/matrix-org/olm/blob/master/docs/megolm.md#partial-forward-secrecy)[^1], however this is [not currently supported in Element](https://github.com/vector-im/element-web/issues/7101) due to it breaking some aspects of the user experience such as key backups and shared message history.

Il protocollo è stato [controllato](https://matrix.org/blog/2016/11/21/matrixs-olm-end-to-end-encryption-security-assessment-released-and-implemented-cross-platform-on-riot-at-last) indipendentemente nel 2016. Le specifiche per il protocollo di Matrix possono essere trovate nella sua [documentazione](https://spec.matrix.org/latest/). Il [ratchet di crittografia Olm](https://matrix.org/docs/matrix-concepts/end-to-end-encryption/) utilizzato da Matrix è un'implementazione dell'[algoritmo Double Ratchet](https://signal.org/docs/specifications/doubleratchet/) di Signal.

### Session

<div class="admonition recommendation" markdown>

![Logo di Session](assets/img/messengers/session.svg){ align=right }

**Session** è un'app di messaggistica decentralizzata incentrata sulle comunicazioni private, sicure e anonime. Session offre il supporto ai messaggi diretti, alle chat di gruppo e alle chiamate vocali.

Session utilizza la [Rete Oxen Service Node](https://oxen.io/) decentralizzata per memorizzare e instradare i messaggi. Ogni messaggio crittografato è indirizzato tramite tre nodi nella Rete del Nodo del Servizio di Oxen, rendendo virtualmente impossibile, per i nodi, la compilazione di informazioni significative su coloro che utilizzano la rete.

[:octicons-home-16: Homepage](https://getsession.org/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://getsession.org/privacy-policy){ .card-link title="Informativa sulla Privacy" }
[:octicons-info-16:](https://getsession.org/faq){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/oxen-io){ .card-link title="Codice sorgente" }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=network.loki.messenger)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1470168868)
- [:simple-github: GitHub](https://github.com/oxen-io/session-android/releases)
- [:simple-windows11: Windows](https://getsession.org/download)
- [:simple-apple: macOS](https://getsession.org/download)
- [:simple-linux: Linux](https://getsession.org/download)

</details>

</div>

Session consente l'E2EE per le chat individuali o i gruppi chiusi, che consentono fino a 100 membri. I gruppi aperti non hanno limitazioni sul numero di membri, ma sono aperti per scelta.

Session was previously based on Signal Protocol before replacing it with their own in December 2020. Session Protocol does [not](https://getsession.org/blog/session-protocol-technical-information) support forward secrecy.[^1]

Oxen requested an independent audit for Session in March 2020. The audit [concluded](https://getsession.org/session-code-audit) in April 2021, “The overall security level of this application is good and makes it usable for privacy-concerned people.”

Session has a [whitepaper](https://arxiv.org/pdf/2002.04609.pdf) describing the technical details of the app and protocol.

## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

<div class="admonition example" markdown>
<p class="admonition-title">Questa sezione è nuova</p>

Stiamo lavorando per stabilire i criteri definiti per ogni sezione del nostro sito e, questa, potrebbe essere soggetta a modifiche. Se hai qualsiasi domanda sui nostri criteri, ti preghiamo di [chiedere sul nostro forum](https://discuss.privacyguides.net/latest) e di non supporre che non abbiamo considerato qualcosa, formulando i nostri consigli, se non elencato qui. Molti fattori sono presi in considerazione e discussi quando consigliamo un progetto e la documentazione di ognuno è in lavorazione.

</div>

- Has open-source clients.
- Does not require sharing personal identifiers (phone numbers or emails in particular) with contacts.
- Uses E2EE for private messages by default.
- Supports E2EE for all messages.
- Has been independently audited.

### Miglior Caso

I nostri criteri ottimali rappresentano ciò che vorremmo vedere dal progetto perfetto in questa categoria. I nostri consigli potrebbero non includere tutte o alcune di queste funzionalità, ma quelli che le includono potrebbero essere preferiti ad altri su questa pagina.

- Supports Forward Secrecy[^1]
- Supports Future Secrecy (Post-Compromise Security)[^2]
- Has open-source servers.
- Decentralized, i.e. [federated or P2P](advanced/communication-network-types.md).
- Uses E2EE for all messages by default.
- Supports Linux, macOS, Windows, Android, and iOS.

[^1]: [Forward Secrecy](https://en.wikipedia.org/wiki/Forward_secrecy) is where keys are rotated very frequently, so that if the current encryption key is compromised, it does not expose **past** messages as well.
[^2]: Future Secrecy (or Post-Compromise Security) is a feature where an attacker is prevented from decrypting **future** messages after compromising a private key, unless they compromise more session keys in the future as well. This effectively forces the attacker to intercept all communication between parties, since they lose access as soon as a key exchange occurs that is not intercepted.
