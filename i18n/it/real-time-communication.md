---
meta_title: "The Best Private Instant Messengers - Privacy Guides"
title: "Comunicazione in tempo reale"
icon: material/chat-processing
description: Other instant messengers make all of your private conversations available to the company that runs them.
cover: real-time-communication.webp
---

Questi sono i nostri consigli per le comunicazioni crittografate in tempo reale.

[Tipi di reti di comunicazione :material-arrow-right-drop-circle:](./advanced/communication-network-types.md)

## Messaggistica Crittografata

Queste app di messaggistica sono ottime per proteggere le tue comunicazioni sensibili.

### Signal

<div class="admonition recommendation" markdown>

![Logo di Signal](assets/img/messengers/signal.svg){ align=right }

**Signal** è un'app per dispositivi mobili sviluppata da Signal Messenger LLC. L'app offre messaggistica istantanea, oltre che chiamate e videochiamate.

Tutte le comunicazioni sono E2EE. Gli elenchi di contatti sono crittografati utilizzando il tuo PIN di Signal e il server non vi ha accesso. Inoltre, i profili personali sono crittografati e condivisi esclusivamente con i contatti con cui parli.

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

Signal supporta i [gruppi privati](https://signal.org/blog/signal-private-group-system/). Il server non registra le appartenenze ai gruppi, i titoli, gli avatar o gli attributi dei gruppi. Signal ha metadati minimi quando [Mittente sigillato](https://signal.org/blog/sealed-sender/) è abilitato. L'indirizzo del mittente è crittografato insieme al corpo del messaggio e soltanto l'indirizzo del destinatario è visibile al server. Mittente Sigillato è abilitato esclusivamente per i tuoi contatti, ma è attivabile per tutti i destinatari con il rischio incrementato di ricevere spam. Signal richiede il numero di telefono come identificativo personale.

Il protocollo è stato [controllato](https://eprint.iacr.org/2016/1013.pdf) indipendentemente nel 2016. Le specifiche per il protocollo di Signal si possono trovare nella sua [documentazione](https://signal.org/docs/).

Abbiamo alcuni consigli aggiuntivi sulla configurazione e rafforzamento della tua installazione di Signal:

[Configurazione e Rafforzamento di Signal :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening/)

### SimpleX Chat

<div class="admonition recommendation" markdown>

![Logo di Simplex](assets/img/messengers/simplex.svg){ align=right }

**SimpleX** Chat è un'app di messaggistica istantanea decentralizzata che non dipende da alcun identificatore univoco, come numeri telefonici o nomi utente. Gli utenti di SimpleX Chat possono scansionare un codice QR o cliccare su un link di invito per partecipare alle conversazioni di gruppo.

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

SimpleX Chat [è stato controllato](https://simplex.chat/blog/20221108-simplex-chat-v4.2-security-audit-new-website.html) da Trail of Bits a ottobre 2022.

SimpleX Chat supporta le funzionalità di base per le chat di gruppo, messaggi diretti, e la modifica dei messaggi e del Markdown. Sono supportate anche le chiamate e le videochiamate in E2EE. I dati possono essere esportati e importati su un altro dispositivo, poiché non esistono server centrali in cui ne è eseguito il backup.

### Briar

<div class="admonition recommendation" markdown>

![Logo di Briar](assets/img/messengers/briar.svg){ align=right }

**Briar** è un'app di messaggistica istantanea crittografata che si [connette](https://briarproject.org/how-it-works/) ad altri client utilizzando la Rete di Tor. Briar può anche connettersi via Wi-Fi o Bluetooth quando si trova nelle vicinanze. La modalità mesh locale di Briar può essere utile quando la connessione a Internet è problematica.

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

Per aggiungere un contatto su Briar, è necessario prima aggiungersi a vicenda. Puoi scambiare i link `briar://` o scansionare il codice QR di un contatto, se è nelle vicinanze.

Il software per il client è stato [controllato](https://briarproject.org/news/2017-beta-released-security-audit/) indipendentemente, così come il protocollo anonimo di trasmissione che utilizza la Rete di Tor.

Briar ha [pubblicato le specifiche](https://code.briarproject.org/briar/briar-spec) complete.

Briar supporta la Segretezza in Avanti utilizzando l'[Handshake](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BHP.md) di Bramble e il protocollo di [Transport](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BTP.md).

## Opzioni Aggiuntive

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

Queste app di messaggistica non dispongono della [Segretezza in Avanti](https://it.wikipedia.org/wiki/Forward_secrecy) e, sebbene soddisfino certe esigenze non soddisfatte dai nostri consigli precedenti, le sconsigliamo per le comunicazioni a lungo termine o sensibili. Qualsiasi compromissione di chiavi tra i destinatari del messaggio, influenzerebbe la confidenzialità di **tutte** le comunicazioni precedenti.

</div>

### Element

<div class="admonition recommendation" markdown>

![Element logo](assets/img/messengers/element.svg){ align=right }

**Element** is the reference [client](https://matrix.org/ecosystem/clients/) for the [Matrix](https://matrix.org/docs/guides/introduction) protocol, an [open standard](https://matrix.org/docs/spec) for secure decentralized real-time communication.

I messaggi e i file condivisi nelle stanze private (che richiedono un invito), sono di default in E2EE, così come le chiamate e videochiamate tra due persone.

[:octicons-home-16: Homepage](https://element.io/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://element.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://element.io/help){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/vector-im){ .card-link title="Source Code" }

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

Le immagini del profilo, le reazioni e i nomi utente non sono crittografati.

Le chiamate e le videochiamate [non](https://github.com/vector-im/element-web/issues/12878) sono in E2EE e utilizzano Jitsi, ma ciò cambierà con la [Segnalazione Nativa VoIP del Gruppo](https://github.com/matrix-org/matrix-doc/pull/3401). Le chiamate di gruppo, correntemente, non dispongono di [autenticazione](https://github.com/vector-im/element-web/issues/13074), a significare che i non partecipanti alla stanza, possono anche unirsi alle chiamate. Consigliamo di non utilizzare questa funzionalità per le riunioni private.

Lo stesso protocollo Matrix [supporta teoricamente il PFS](https://gitlab.matrix.org/matrix-org/olm/blob/master/docs/megolm.md#partial-forward-secrecy), tuttavia [non è correntemente supportato su Element](https://github.com/vector-im/element-web/issues/7101), poiché rovina alcuni aspetti dell'esperienza utente, come il backup delle chiavi e la cronologia dei messaggi condivisi.

Il protocollo è stato [controllato](https://matrix.org/blog/2016/11/21/matrixs-olm-end-to-end-encryption-security-assessment-released-and-implemented-cross-platform-on-riot-at-last) indipendentemente nel 2016. Le specifiche per il protocollo di Matrix possono essere trovate nella sua [documentazione](https://spec.matrix.org/latest/). Il [ratchet di crittografia Olm](https://matrix.org/docs/matrix-concepts/end-to-end-encryption/) utilizzato da Matrix è un'implementazione dell'[algoritmo Double Ratchet](https://signal.org/docs/specifications/doubleratchet/) di Signal.

### Session

<div class="admonition recommendation" markdown>

![Logo di Session](assets/img/messengers/session.svg){ align=right }

**Session** è un'app di messaggistica decentralizzata incentrata sulle comunicazioni private, sicure e anonime. Session offre il supporto ai messaggi diretti, alle chat di gruppo e alle chiamate vocali.

Session utilizza la [Rete Oxen Service Node](https://oxen.io/) decentralizzata per memorizzare e instradare i messaggi. Ogni messaggio crittografato è indirizzato tramite tre nodi nella Rete del Nodo del Servizio di Oxen, rendendo virtualmente impossibile, per i nodi, la compilazione di informazioni significative su coloro che utilizzano la rete.

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

Session consente l'E2EE per le chat individuali o i gruppi chiusi, che consentono fino a 100 membri. I gruppi aperti non hanno limitazioni sul numero di membri, ma sono aperti per scelta.

Session [non](https://getsession.org/blog/session-protocol-technical-information) supporta PFD, ossia quando un sistema crittografico modifica automaticamente e frequentemente le chiavi utilizzate per crittografare e decrittografare le informazioni, così che se l'ultima chiave è compromessa, espone una porzione minore di informazioni sensibili.

Oxen ha richiesto un controllo indipendente per Session a marzo 2020. Il controllo [è stato concluso](https://getsession.org/session-code-audit) ad aprile 2021, "Il livello di sicurezza complessivo di questa applicazione è buono e la rende utilizzabile per gli individui interessati alla propria privacy."

Session ha un [whitepaper](https://arxiv.org/pdf/2002.04609.pdf) che descrive le caratteristiche tecniche dell'app e del protocollo.

## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

<div class="admonition example" markdown>
<p class="admonition-title">Questa sezione è nuova</p>

Stiamo lavorando per stabilire i criteri definiti per ogni sezione del nostro sito e, questa, potrebbe essere soggetta a modifiche. Se hai qualsiasi domanda sui nostri criteri, ti preghiamo di [chiedere sul nostro forum](https://discuss.privacyguides.net/latest) e di non supporre che non abbiamo considerato qualcosa, formulando i nostri consigli, se non elencato qui. Molti fattori sono presi in considerazione e discussi quando consigliamo un progetto e la documentazione di ognuno è in lavorazione.

</div>

- Deve avere dei client open source.
- Deve utilizzare l'E2EE per i messaggi privati di default.
- Deve supportare l'E2EE per tutti i messaggi.
- Deve essere stato controllato indipendentemente.

### Miglior Caso

I nostri criteri ottimali rappresentano ciò che vorremmo vedere dal progetto perfetto in questa categoria. I nostri consigli potrebbero non includere tutte o alcune di queste funzionalità, ma quelli che le includono potrebbero essere preferiti ad altri su questa pagina.

- Dovrebbe disporre della Segretezza in Avanti.
- Dovrebbe disporre di server open source.
- Dovrebbe essere decentralizzato, cioè federato o P2P.
- Dovrebbe utilizzare l'E2EE per tutti i messaggi di default.
- Dovrebbe supportare Linux, macOS, Windows, Android e iOS.
