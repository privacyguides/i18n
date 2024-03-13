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

[:octicons-home-16: Homepage](https://signal.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://signal.org/legal/#privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.signal.org){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/signalapp){ .card-link title="Source Code" }
[:octicons-heart-16:](https://signal.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.thoughtcrime.securesms)
- [:simple-appstore: App Store](https://apps.apple.com/app/id874139669)
- [:simple-android: Android](https://signal.org/android/apk)
- [:simple-windows11: Windows](https://signal.org/download/windows)
- [:simple-apple: macOS](https://signal.org/download/macos)
- [:simple-linux: Linux](https://signal.org/download/linux)

</details>

</div>

Signal richiede il tuo numero di telefono per la registrazione, ma dovresti creare un nome utente per nascondere il tuo numero di telefono ai tuoi contatti:

1. In Signal, apri le impostazioni dell'app e tocca il profilo del tuo account in alto.
2. Tocca **Username** e scegli **Continua** nella schermata "Imposta il tuo username Signal".
3. Inserisci un username. Il tuo username sarà sempre abbinato a un set di cifre univoche per mantenere il tuo username unico e impedire alle persone di indovinarlo, per esempio se inserisci "John" il tuo nome utente potrebbe finire per essere `@john.35`.
4. Torna alla pagina delle impostazioni principali dell'app e seleziona **Privacy**.
5. Seleziona **Numero Di Telefono**
6. Modifica l'impostazione **Chi può vedere il mio numero** in: **Nessuno**

È possibile modificare l'impostazione **Chi può trovarmi con il numero** in **Nessuno** se si vuole evitare che persone che hanno già il tuo numero di telefono scoprano il tuo account/nome utente Signal.

Gli elenchi di contatti su Signal sono crittografati utilizzando il PIN di Signal e il server non ha accesso ad essi. Inoltre, i profili personali sono crittografati e condivisi esclusivamente con i contatti con cui parli. Signal supports [private groups](https://signal.org/blog/signal-private-group-system), where the server has no record of your group memberships, group titles, group avatars, or group attributes. Signal has minimal metadata when [Sealed Sender](https://signal.org/blog/sealed-sender) is enabled. L'indirizzo del mittente è crittografato insieme al corpo del messaggio e soltanto l'indirizzo del destinatario è visibile al server. Mittente Sigillato è abilitato esclusivamente per i tuoi contatti, ma è attivabile per tutti i destinatari con il rischio incrementato di ricevere spam.

Il protocollo è stato [controllato](https://eprint.iacr.org/2016/1013.pdf) indipendentemente nel 2016. The specification for the Signal protocol can be found in their [documentation](https://signal.org/docs).

Abbiamo alcuni consigli aggiuntivi sulla configurazione e rafforzamento della tua installazione di Signal:

[Configurazione e Rafforzamento di Signal :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening)

### SimpleX Chat

<div class="admonition recommendation" markdown>

![Logo di Simplex](assets/img/messengers/simplex.svg){ align=right }

**SimpleX** Chat è un'app di messaggistica istantanea decentralizzata che non dipende da alcun identificatore univoco, come numeri telefonici o nomi utente. Gli utenti di SimpleX Chat possono scansionare un codice QR o cliccare su un link di invito per partecipare alle conversazioni di gruppo.

[:octicons-home-16: Homepage](https://simplex.chat){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/simplex-chat/simplex-chat/blob/stable/PRIVACY.md){ .card-link title="Informativa sulla Privacy" }
[:octicons-info-16:](https://github.com/simplex-chat/simplex-chat/tree/stable/docs){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/simplex-chat){ .card-link title="Codice sorgente" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=chat.simplex.app)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1605771084)
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

![Briar logo](assets/img/messengers/briar.svg){ align=right }

**Briar** is an encrypted instant messenger that [connects](https://briarproject.org/how-it-works) to other clients using the Tor Network. Briar può anche connettersi via Wi-Fi o Bluetooth quando si trova nelle vicinanze. La modalità mesh locale di Briar può essere utile quando la connessione a Internet è problematica.

[:octicons-home-16: Homepage](https://briarproject.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://briarproject.org/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://code.briarproject.org/briar/briar/-/wikis/home){ .card-link title=Documentation}
[:octicons-code-16:](https://code.briarproject.org/briar/briar){ .card-link title="Source Code" }
[:octicons-heart-16:](https://briarproject.org){ .card-link title="Donation options are listed on the bottom of the homepage" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.briarproject.briar.android)
- [:simple-windows11: Windows](https://briarproject.org/download-briar-desktop)
- [:simple-linux: Linux](https://briarproject.org/download-briar-desktop)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.briarproject.Briar)

</details>

</div>

Per aggiungere un contatto su Briar, è necessario prima aggiungersi a vicenda. Puoi scambiare i link `briar://` o scansionare il codice QR di un contatto, se è nelle vicinanze.

The client software was independently [audited](https://briarproject.org/news/2017-beta-released-security-audit), and the anonymous routing protocol uses the Tor network which has also been audited.

Briar ha [pubblicato le specifiche](https://code.briarproject.org/briar/briar-spec) complete.

Briar supporta la segretezza in avanti[^1] utilizzando il Bramble [Handshake](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BHP.md) e il protocollo [Transport](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BTP.md).

## Opzioni Aggiuntive

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

Questi messanger non hanno la segretezza in avanti[^1], e mentre soddisfano determinati criterie che le nostre raccomandazioni precedenti non soddisfano, non li consigliamo per comunicazioni a lungo termine o sensibili. Qualsiasi compromissione di chiavi tra i destinatari del messaggio, influenzerebbe la confidenzialità di **tutte** le comunicazioni precedenti.

</div>

### Element

<div class="admonition recommendation" markdown>

![Element logo](assets/img/messengers/element.svg){ align=right }

**Element** is the reference [client](https://matrix.org/ecosystem/clients) for the [Matrix](https://matrix.org/docs/chat_basics/matrix-for-im) protocol, an [open standard](https://spec.matrix.org/latest) for secure decentralized real-time communication.

I messaggi e i file condivisi nelle stanze private (che richiedono un invito), sono di default in E2EE, così come le chiamate e videochiamate tra due persone.

[:octicons-home-16: Homepage](https://element.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://element.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://element.io/help){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/element-hq){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=im.vector.app)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1083446067)
- [:simple-github: GitHub](https://github.com/element-hq/element-android/releases)
- [:simple-windows11: Windows](https://element.io/download)
- [:simple-apple: macOS](https://element.io/download)
- [:simple-linux: Linux](https://element.io/download)
- [:octicons-globe-16: Web](https://app.element.io)

</details>

</div>

Le immagini del profilo, le reazioni e i nomi utente non sono crittografati.

Le chiamate e le videochiamate [non](https://github.com/vector-im/element-web/issues/12878) sono in E2EE e utilizzano Jitsi, ma ciò cambierà con la [Segnalazione Nativa VoIP del Gruppo](https://github.com/matrix-org/matrix-doc/pull/3401). Le chiamate di gruppo, correntemente, non dispongono di [autenticazione](https://github.com/vector-im/element-web/issues/13074), a significare che i non partecipanti alla stanza, possono anche unirsi alle chiamate. Consigliamo di non utilizzare questa funzionalità per le riunioni private.

Il protocollo Matrix stesso [teoricamente supporta la segretezza in avanti](https://gitlab.matrix.org/matrix-org/olm/blob/master/docs/megolm.md#partial-forward-secrecy)[^1], tuttavia questo è [attualmente non supportato in Element](https://github.com/vector-im/element-web/issues/7101) a causa dell'interruzione di alcuni aspetti dell'esperienza utente, come i backup delle chiavi e la cronologia dei messaggi condivisi.

Il protocollo è stato [controllato](https://matrix.org/blog/2016/11/21/matrixs-olm-end-to-end-encryption-security-assessment-released-and-implemented-cross-platform-on-riot-at-last) indipendentemente nel 2016. The specification for the Matrix protocol can be found in their [documentation](https://spec.matrix.org/latest). The [Olm cryptographic ratchet](https://matrix.org/docs/matrix-concepts/end-to-end-encryption) used by Matrix is an implementation of Signal’s [Double Ratchet algorithm](https://signal.org/docs/specifications/doubleratchet).

### Session

<div class="admonition recommendation" markdown>

![Logo di Session](assets/img/messengers/session.svg){ align=right }

**Session** è un'app di messaggistica decentralizzata incentrata sulle comunicazioni private, sicure e anonime. Session offre il supporto ai messaggi diretti, alle chat di gruppo e alle chiamate vocali.

Session uses the decentralized [Oxen Service Node Network](https://oxen.io) to store and route messages. Ogni messaggio crittografato è indirizzato tramite tre nodi nella Rete del Nodo del Servizio di Oxen, rendendo virtualmente impossibile, per i nodi, la compilazione di informazioni significative su coloro che utilizzano la rete.

[:octicons-home-16: Homepage](https://getsession.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://getsession.org/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://getsession.org/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/oxen-io){ .card-link title="Source Code" }

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

Session si basava in precedenza sul Signal Protocol, prima di sostituirlo con il proprio nel dicembre 2020. Session Protocol [non](https://getsession.org/blog/session-protocol-technical-information) supporta la segretezza in avanti.[^1]

Oxen ha richiesto un controllo indipendente per Session a marzo 2020. Il controllo [è stato concluso](https://getsession.org/session-code-audit) ad aprile 2021, "Il livello di sicurezza complessivo di questa applicazione è buono e la rende utilizzabile per gli individui interessati alla propria privacy."

Session ha un [whitepaper](https://arxiv.org/pdf/2002.04609.pdf) che descrive i dettagli tecnici dell'applicazione e del protocollo.

## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

<div class="admonition example" markdown>
<p class="admonition-title">Questa sezione è nuova</p>

Stiamo lavorando per stabilire i criteri definiti per ogni sezione del nostro sito e, questa, potrebbe essere soggetta a modifiche. Se hai qualsiasi domanda sui nostri criteri, ti preghiamo di [chiedere sul nostro forum](https://discuss.privacyguides.net/latest) e di non supporre che non abbiamo considerato qualcosa, formulando i nostri consigli, se non elencato qui. Molti fattori sono presi in considerazione e discussi quando consigliamo un progetto e la documentazione di ognuno è in lavorazione.

</div>

- Ha client open-source.
- Non richiede la condivisione di identificativi personali (numeri di telefono o e-mail in particolare) con i contatti.
- Usa E2EE per i messaggi privati di default.
- Supporta E2EE per tutti i messaggi.
- È stato sottoposto ad audit indipendente.

### Miglior Caso

I nostri criteri ottimali rappresentano ciò che vorremmo vedere dal progetto perfetto in questa categoria. I nostri consigli potrebbero non includere tutte o alcune di queste funzionalità, ma quelli che le includono potrebbero essere preferiti ad altri su questa pagina.

- Supporta la segretezza in avanti[^1]
- Supporta la segretezza futura (sicurezza post-compromissione)[^2]
- Ha server open-source.
- Decentralizzato, cioè [federato o P2P](advanced/communication-network-types.md).
- Usa E2EE per tutti i messaggi di default.
- Supporta Linux, macOS, Windows, Android e iOS.

[^1]: [La segretezza in avanti](https://en.wikipedia.org/wiki/Forward_secrecy) è il caso in cui le chiavi vengono ruotate molto frequentemente, in modo che se la chiave di crittografia corrente viene compromessa, non si espongano anche i messaggi **passati**.
[^2]: La segretezza futura (o sicurezza post-compromissione) è una caratteristica che impedisce a un utente malintenzionato di decifrare i messaggi **futuri** dopo aver compromesso una chiave privata, a meno che non comprometta anche altre chiavi di sessione in futuro. Questo costringe di fatto l'aggressore a intercettare tutte le comunicazioni tra le parti, poiché perde l'accesso non appena avviene uno scambio di chiavi che non viene intercettato.
