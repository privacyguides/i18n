---
meta_title: "Le migliori app di messaggistica istantanea private - Privacy Guides"
title: "Comunicazione in tempo reale"
icon: material/chat-processing
description: Encrypted messengers like Signal and SimpleX keep your sensitive communications secure from prying eyes.
cover: real-time-communication.webp
---

<small>Protects against the following threat(s):</small>

- [:material-bug-outline: Attacchi Passivi](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: Fornitori di Servizi](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}
- [:material-eye-outline: Sorveglianza di massa](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-account-cash: Capitalismo di sorveglianza](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

These are our recommendations for encrypted **real-time communication**.

[Tipi di reti di comunicazione :material-arrow-right-drop-circle:](./advanced/communication-network-types.md)

## Messaggistica Crittografata

Queste app di messaggistica sono ottime per proteggere le tue comunicazioni sensibili.

### Signal

<div class="admonition recommendation" markdown>

![Logo di Signal](assets/img/messengers/signal.svg){ align=right }

**Signal** è un'app per dispositivi mobili sviluppata da Signal Messenger LLC. The app provides instant messaging and calls secured with the Signal Protocol, an extremely secure encryption protocol which supports forward secrecy[^1] and post-compromise security.[^2]

[:octicons-home-16: Homepage](https://signal.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://signal.org/legal/#privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.signal.org){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/signalapp){ .card-link title="Source Code" }
[:octicons-heart-16:](https://signal.org/donate){ .card-link title="Contribute" }

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

Signal richiede il tuo numero di telefono per la registrazione, ma dovresti creare un nome utente per nascondere il tuo numero di telefono ai tuoi contatti:

1. In Signal, apri le impostazioni dell'app e tocca il profilo del tuo account in alto.
2. Tocca **Username** e scegli **Continua** nella schermata "Imposta il tuo username Signal".
3. Inserisci un username. Il tuo username sarà sempre abbinato a un set di cifre univoche per mantenere il tuo username unico e impedire alle persone di indovinarlo, per esempio se inserisci "John" il tuo nome utente potrebbe finire per essere `@john.35`. By default, only 2 digits are paired with your username when you create it, but you can add more digits until you reach the username length limit (32 characters).
4. Torna alla pagina delle impostazioni principali dell'app e seleziona **Privacy**.
5. Seleziona **Numero Di Telefono**
6. Modifica l'impostazione **Chi può vedere il mio numero** in: **Nessuno**

È possibile modificare l'impostazione **Chi può trovarmi con il numero** in **Nessuno** se si vuole evitare che persone che hanno già il tuo numero di telefono scoprano il tuo account/nome utente Signal.

Gli elenchi di contatti su Signal sono crittografati utilizzando il PIN di Signal e il server non ha accesso ad essi. Inoltre, i profili personali sono crittografati e condivisi esclusivamente con i contatti con cui parli. Signal supports [private groups](https://signal.org/blog/signal-private-group-system), where the server has no record of your group memberships, group titles, group avatars, or group attributes. Signal has minimal metadata when [Sealed Sender](https://signal.org/blog/sealed-sender) is enabled. L'indirizzo del mittente è crittografato insieme al corpo del messaggio e soltanto l'indirizzo del destinatario è visibile al server. Mittente Sigillato è abilitato esclusivamente per i tuoi contatti, ma è attivabile per tutti i destinatari con il rischio incrementato di ricevere spam.

Il protocollo è stato [controllato](https://eprint.iacr.org/2016/1013.pdf) indipendentemente nel 2016. The specification for the Signal protocol can be found in their [documentation](https://signal.org/docs).

Abbiamo alcuni consigli aggiuntivi sulla configurazione e rafforzamento della tua installazione di Signal:

[Configurazione e Rafforzamento di Signal :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening)

#### Molly (Android)

If you use Android and your threat model requires protecting against [:material-target-account: Targeted Attacks](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red} you may consider using this alternative app, which features a number of security and usability improvements, to access the Signal network.

<div class="admonition recommendation" markdown>

![Molly logo](assets/img/messengers/molly.svg){ align=right }

**Molly** is an alternative Signal client for Android which allows you to encrypt the local database with a passphrase at rest, to have unused RAM data securely shredded, to route your connection via Tor, and [more](https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening#privacy-and-security-features). It also has usability improvements including scheduled backups, automatic locking, and the ability to use your Android phone as a linked device instead of the primary device for a Signal account.

[:octicons-home-16: Homepage](https://molly.im){ .md-button .md-button--primary }
[:octicons-eye-16:](https://signal.org/legal/#privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/mollyim/mollyim-android/wiki){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/mollyim/mollyim-android){ .card-link title="Source Code" }
[:octicons-heart-16:](https://opencollective.com/mollyim){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-fdroid: F-Droid](https://molly.im/fdroid)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/im.molly.app)
- [:simple-github: GitHub](https://github.com/mollyim/mollyim-android/releases)

</details>

</div>

Molly is updated every two weeks to include the latest features and bug fixes from Signal. The exception is security issues, which are patched as soon as possible. That said, you should be aware that there might be a slight delay compared to upstream, which may affect actions such as [migrating from Signal to Molly](https://github.com/mollyim/mollyim-android/wiki/Migrating-From-Signal#migrating-from-signal).

Note that you are trusting multiple parties by using Molly, as you now need to trust the Signal team *and* the Molly team to deliver safe and timely updates.

There is a version of Molly called **Molly-FOSS** which removes proprietary code like the Google services used by both Signal and Molly, at the expense of some features like battery-saving push notifications via Google Play Services.

There is also a version called [**Molly-UP**](https://github.com/mollyim/mollyim-android#unifiedpush) which is based on Molly-FOSS and adds support for push notifications with [UnifiedPush](https://unifiedpush.org), an open source alternative to the push notifications provided by Google Play Services, but it requires running a separate program called [Mollysocket](https://github.com/mollyim/mollysocket) to function. Mollysocket can either be self-hosted on a separate computer or server (VPS), or alternatively a public Mollysocket instance can be used ([step-by-step tutorial, in German](https://kuketz-blog.de/messenger-wechsel-von-signal-zu-molly-unifiedpush-mollysocket-ntfy)).

All three versions of Molly provide the same security improvements.

Molly and Molly-FOSS support [reproducible builds](https://github.com/mollyim/mollyim-android/tree/main/reproducible-builds), meaning it's possible to confirm that the compiled APKs match the source code.

### SimpleX Chat

<div class="admonition recommendation" markdown>

![Simplex logo](assets/img/messengers/simplex.svg){ align=right }

**SimpleX Chat** is an instant messenger that doesn't depend on any unique identifiers such as phone numbers or usernames. Its decentralized network makes SimpleX Chat an effective tool against [:material-close-outline: Censorship](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }.

[:octicons-home-16: Homepage](https://simplex.chat){ .md-button .md-button--primary }
[:octicons-eye-16:](https://simplex.chat/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://simplex.chat/docs/simplex.html){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/simplex-chat){ .card-link title="Source Code" }

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

You can find a full list of the privacy and security [features](https://github.com/simplex-chat/simplex-chat#privacy-and-security-technical-details-and-limitations) implemented in SimpleX Chat on the app's repository.

SimpleX Chat was independently audited in [July 2024](https://simplex.chat/blog/20241014-simplex-network-v6-1-security-review-better-calls-user-experience.html#simplex-cryptographic-design-review-by-trail-of-bits) and in [October 2022](https://simplex.chat/blog/20221108-simplex-chat-v4.2-security-audit-new-website).

### Briar

<div class="admonition recommendation" markdown>

![Briar logo](assets/img/messengers/briar.svg){ align=right }

**Briar** is an encrypted instant messenger that [connects](https://briarproject.org/how-it-works) to other clients using the Tor Network, making it an effective tool at circumventing [:material-close-outline: Censorship](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }. Briar può anche connettersi via Wi-Fi o Bluetooth quando si trova nelle vicinanze. La modalità mesh locale di Briar può essere utile quando la connessione a Internet è problematica.

[:octicons-home-16: Homepage](https://briarproject.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://briarproject.org/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://code.briarproject.org/briar/briar/-/wikis/home){ .card-link title="Documentation" }
[:octicons-code-16:](https://code.briarproject.org/briar/briar){ .card-link title="Source Code" }
[:octicons-heart-16:](https://briarproject.org){ .card-link title="Donation options are listed on the bottom of the homepage" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.briarproject.briar.android)
- [:fontawesome-brands-windows: Windows](https://briarproject.org/download-briar-desktop)
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

**Element** is the flagship client for the [Matrix](https://matrix.org/docs/chat_basics/matrix-for-im) protocol, an [open standard](https://spec.matrix.org/latest) for secure decentralized real-time communication.

Messages and files shared in private rooms (those which require an invite) are by default E2EE, as are one-to-one voice and video calls.

[:octicons-home-16: Homepage](https://element.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://element.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://element.io/help){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/element-hq){ .card-link title="Source Code" }

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

Le immagini del profilo, le reazioni e i nomi utente non sono crittografati.

With the integration of [Element Call](https://element.io/blog/we-have-lift-off-element-x-call-and-server-suite-are-ready) into Element's web app, desktop apps, and its [rewritten mobile apps](https://element.io/blog/element-x-experience-the-future-of-element), group VoIP and video calls are E2EE by default.

Il protocollo Matrix stesso [teoricamente supporta la segretezza in avanti](https://gitlab.matrix.org/matrix-org/olm/blob/master/docs/megolm.md#partial-forward-secrecy)[^1], tuttavia questo è [attualmente non supportato in Element](https://github.com/vector-im/element-web/issues/7101) a causa dell'interruzione di alcuni aspetti dell'esperienza utente, come i backup delle chiavi e la cronologia dei messaggi condivisi.

Il protocollo è stato [controllato](https://matrix.org/blog/2016/11/21/matrixs-olm-end-to-end-encryption-security-assessment-released-and-implemented-cross-platform-on-riot-at-last) indipendentemente nel 2016. The specification for the Matrix protocol can be found in their [documentation](https://spec.matrix.org/latest). The [Olm cryptographic ratchet](https://matrix.org/docs/matrix-concepts/end-to-end-encryption) used by Matrix is an implementation of Signal’s [Double Ratchet algorithm](https://signal.org/docs/specifications/doubleratchet).

### Session

<div class="admonition recommendation" markdown>

![Logo di Session](assets/img/messengers/session.svg){ align=right }

**Session** è un'app di messaggistica decentralizzata incentrata sulle comunicazioni private, sicure e anonime. Session offre il supporto ai messaggi diretti, alle chat di gruppo e alle chiamate vocali.

Session uses the decentralized [Oxen Service Node Network](https://oxen.io) to store and route messages. Ogni messaggio crittografato è indirizzato tramite tre nodi nella Rete del Nodo del Servizio di Oxen, rendendo virtualmente impossibile, per i nodi, la compilazione di informazioni significative su coloro che utilizzano la rete.

[:octicons-home-16: Homepage](https://getsession.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://getsession.org/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://getsession.org/faq){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/oxen-io){ .card-link title="Source Code" }

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

Session consente l'E2EE per le chat individuali o i gruppi chiusi, che consentono fino a 100 membri. It is also possible to [set up](https://docs.oxen.io/oxen-docs/products-built-on-oxen/session/guides/open-group-setup) or join open groups which can host thousands of members, but messages in these open groups are **not** end-to-end encrypted between participants.

Session si basava in precedenza sul Signal Protocol, prima di sostituirlo con il proprio nel dicembre 2020. Session Protocol [non](https://getsession.org/blog/session-protocol-technical-information) supporta la segretezza in avanti.[^1]

Oxen ha richiesto un controllo indipendente per Session a marzo 2020. The audit [concluded](https://getsession.org/session-code-audit) in April 2021:

> The overall security level of this application is good and makes it usable for privacy-concerned people.

Session ha un [whitepaper](https://arxiv.org/pdf/2002.04609.pdf) che descrive i dettagli tecnici dell'applicazione e del protocollo.

## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

### Requisiti minimi

- Ha client open-source.
- Non richiede la condivisione di identificativi personali (numeri di telefono o e-mail in particolare) con i contatti.
- Usa E2EE per i messaggi privati di default.
- Supporta E2EE per tutti i messaggi.
- È stato sottoposto ad audit indipendente.

### Miglior Caso

I nostri criteri ottimali rappresentano ciò che vorremmo vedere dal progetto perfetto in questa categoria. I nostri consigli potrebbero non includere tutte o alcune di queste funzionalità, ma quelli che le includono potrebbero essere preferiti ad altri su questa pagina.

- Supports forward secrecy[^1]
- Supporta la segretezza futura (sicurezza post-compromissione)[^2]
- Ha server open-source.
- Decentralizzato, cioè [federato o P2P](advanced/communication-network-types.md).
- Usa E2EE per tutti i messaggi di default.
- Supporta Linux, macOS, Windows, Android e iOS.

[^1]: [Forward secrecy](https://en.wikipedia.org/wiki/Forward_secrecy) is where keys are rotated very frequently, so that if the current encryption key is compromised, it does not expose **past** messages as well.
[^2]: La segretezza futura (o sicurezza post-compromissione) è una caratteristica che impedisce a un utente malintenzionato di decifrare i messaggi **futuri** dopo aver compromesso una chiave privata, a meno che non comprometta anche altre chiavi di sessione in futuro. Questo costringe di fatto l'aggressore a intercettare tutte le comunicazioni tra le parti, poiché perde l'accesso non appena avviene uno scambio di chiavi che non viene intercettato.
