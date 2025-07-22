---
meta_title: "Le migliori app di messaggistica istantanea private - Privacy Guides"
title: Comunicazione in tempo reale
icon: material/chat-processing
description: Applicazioni di messaggistica crittografate come Signal e SimpleX mantengono le tue conversazioni sensibili al riparo da occhi indiscreti.
cover: real-time-communication.webp
---

<small>Protegge dalle seguenti minacce:</small>

- [:material-bug-outline: Attacchi Passivi](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: Fornitori di Servizi](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}
- [:material-eye-outline: Sorveglianza di massa](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-account-cash: Capitalismo di sorveglianza](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Queste raccomandazioni per **comunicazioni in tempo reale** crittografate sono ottime per proteggere le tue conversazioni sensibili. Queste applicazioni di messaggistica istantanea comprendono vari [tipi di rete di comunicazione](advanced/communication-network-types.md).

[:material-movie-open-play-outline: Video: It's time to stop using SMS](https://www.privacyguides.org/videos/2025/01/24/its-time-to-stop-using-sms-heres-why ""){.md-button}

## Signal

<div class="admonition recommendation" markdown>

![Logo di Signal](assets/img/messengers/signal.svg){ align=right }

**Signal** è un'app per dispositivi mobili sviluppata da Signal Messenger LLC. L'applicazione fornisce messaggistica istantanea e chiamate protette con il protocollo Signal, un protocollo di crittografia estremamente sicuro che supporta la segretezza in avanti[^1] e la sicurezza post compromissione.[^2]

[:octicons-home-16: Pagina Principale](https://signal.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://signal.org/legal/#privacy-policy){ .card-link title="Politica sulla Privacy" }
[:octicons-info-16:](https://support.signal.org){ .card-link title="Documentazione" }
[:octicons-code-16:](https://github.com/signalapp){ .card-link title="Codice Sorgente" }
[:octicons-heart-16:](https://signal.org/donate){ .card-link title="Contribuisci" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.thoughtcrime.securesms)
- [:simple-appstore: App Store](https://apps.apple.com/app/id874139669)
- [:simple-github: GitHub](https://github.com/signalapp/Signal-Android/releases)
- [:simple-android: Android](https://signal.org/android/apk)
- [:fontawesome-brands-windows: Windows](https://signal.org/download/windows)
- [:simple-apple: macOS](https://signal.org/download/macos)
- [:simple-linux: Linux](https://signal.org/download/linux)

</details>

</div>

Signal richiede il tuo numero di telefono al momento della registrazione, però dovresti creare un nome utente per nascondere il tuo numero di telefono dai tuoi contatti:

1. In Signal, apri le impostazioni dell'app e tocca il profilo del tuo account in alto.
2. Tocca **Nome utente** e scegli **Continua** nella schermata "Imposta il tuo nome utente Signal".
3. Inserisci un nome utente. Il tuo nome utente è sempre abbinato a un'unica serie di cifre per mantenere il tuo nome utente unico ed evitare che le persone lo indovinino.  Per esempio se inserisci "John" il tuo nome utente potrebbe essere `@john.35`. Per impostazione predefinita solo 2 cifre sono abbinate al tuo nome utente quando lo crei, ma ne puoi aggiungere altre fino a che non raggiungi la lunghezza limite per il nome utente (32 caratteri).
4. Torna alla pagina delle impostazioni principali dell'app e seleziona **Privacy**.
5. Seleziona **Numero di telefono**.
6. Metti l'impostazione **Chi può vedere il mio numero di telefono** su **Nessuno**.
7. (Opzionale) Cambia anche l'impostazione **Chi può trovarmi tramite il mio numero** su **Nessuno**  se vuoi evitare che persone che hanno il tuo numero di telefono scoprano il tuo account/nome utente Signal

Abbiamo alcuni consigli aggiuntivi su come rendere più sicura la tua applicazione Signal:

[Signal configurazione e messa in sicurezza :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening)

Su Signal le liste dei contatti sono crittografate con il tuo PIN di Signal e il server non ne ha accesso. Anche i profili personali sono crittografati e sono condivisi solamente con i contatti con cui chatti.

Signal supporta i [gruppi privati](https://signal.org/blog/signal-private-group-system), il server non ha accesso alle informazioni dei gruppi tra cui: chi appartiene al gruppo, il nome, l'avatar o le caratteristiche del gruppo. Signal ha dei metadati minimi quando il [Mittente Sigillato](https://signal.org/blog/sealed-sender)  è abilitato. L'indirizzo del mittente è crittografato con il testo del messaggio e solamente l'indirizzo del destinatario è visibile al server. Il Mittente Sigillato è abilitato solamente per le persone nella tua lista dei contatti, ma lo puoi abilitare per tutti i destinatari con un maggior rischio di ricevere spam.

Il protocollo è stato indipendentemente  [revisionato](https://eprint.iacr.org/2016/1013.pdf) nel 2016. Le specifiche del protocollo Signal possono essere trovate nella [documentazione](https://signal.org/docs).

### Molly (Android)

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

**Molly-FOSS** is a version of Molly which removes proprietary code like the Google services used by both Signal and Molly at the expense of some features (like battery-saving push notifications via Google Play Services). You can set up push notifications without Google Play Services in either version of Molly with [UnifiedPush](https://unifiedpush.org). Using this notification delivery method requires access to a [MollySocket](https://github.com/mollyim/mollysocket) server, but you can choose a public MollySocket instance for this.[^3]

Both versions of Molly provide the same security improvements and support [reproducible builds](https://github.com/mollyim/mollyim-android/tree/main/reproducible-builds), meaning it's possible to confirm that the compiled APKs match the source code.

## SimpleX Chat

<div class="admonition recommendation" markdown>

![SimpleX Chat logo](assets/img/messengers/simplex.svg){ align=right }

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

SimpleX Chat provides direct messaging, group chats, and E2EE calls secured with the [SimpleX Messaging Protocol](https://github.com/simplex-chat/simplexmq/blob/stable/protocol/simplex-messaging.md), which uses double ratchet encryption with quantum resistance. Additionally, SimpleX Chat provides metadata protection by using unidirectional ["simplex queues"](https://github.com/simplex-chat/simplexmq/blob/stable/protocol/simplex-messaging.md#simplex-queue) to deliver messages.

To participate in conversations on SimpleX Chat, you must scan a QR code or click an invite link. This allows you to verify a contact out-of-band, which protects against man-in-the-middle attacks by network providers. Your data can be exported and imported onto another device, as there are no central servers where this is backed up.

You can find a full list of the privacy and security [features](https://github.com/simplex-chat/simplex-chat#privacy-and-security-technical-details-and-limitations) implemented in SimpleX Chat in the app's repository.

SimpleX Chat was independently audited in [July 2024](https://simplex.chat/blog/20241014-simplex-network-v6-1-security-review-better-calls-user-experience.html#simplex-cryptographic-design-review-by-trail-of-bits) and in [October 2022](https://simplex.chat/blog/20221108-simplex-chat-v4.2-security-audit-new-website).

## Briar

<div class="admonition recommendation" markdown>

![Briar logo](assets/img/messengers/briar.svg){ align=right }

**Briar** is an encrypted instant messenger that [connects](https://briarproject.org/how-it-works) to other clients using the [Tor network](alternative-networks.md#tor), making it an effective tool at circumventing [:material-close-outline: Censorship](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }. Briar può anche connettersi via Wi-Fi o Bluetooth quando si trova nelle vicinanze. La modalità mesh locale di Briar può essere utile quando la connessione a Internet è problematica.

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

## Criteri

**Ti preghiamo di notare che non siamo affiliati con alcun progetto consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie chiara di requisiti per consentirci di fornire consigli oggettivi. Ti suggeriamo di familiarizzare con questo elenco prima di scegliere di utilizzare un progetto e di condurre le tue ricerche per assicurarti che si tratti della scelta adatta a te.

### Requisiti minimi

- Deve avere i client Open Source.
- Non deve richiedere la condivisione di identificativi personali (in particolare numero di telefono o email) con i contatti.
- Deve usare E2EE per i messaggi personali di default.
- Deve supportare E2EE per tutti i messaggi.
- Deve supportare la segretezza in avanti<sup id="fnref2:1"><a href="#fn:1" class="footnote-ref">2</sup></li> 
  
  <li>
    Deve avere una revisione pubblicata da una terza parte indipendente e rispettabile.
  </li></ul>

<h3 spaces-before="0">
  Caso migliore
</h3>

<p spaces-before="0">
  I nostri criteri ottimali rappresentano ciò che vorremmo vedere dal progetto perfetto in questa categoria. I nostri consigli potrebbero non includere tutte o alcune di queste funzionalità, ma quelli che le includono potrebbero essere preferiti ad altri su questa pagina.
</p>

<ul>
  <li>
    Dovrebbe supportare la segretezza futura (sicurezza post compromesso)<sup id="fnref:2"><a href="#fn:2" class="footnote-ref">3</sup></li> 
    
    <li>
      Dovrebbe avere i server Open Source.
    </li>
    
    <li>
      Dovrebbe utilizzare una rete decentralizzata: <a href="advanced/communication-network-types.md">federata o P2P</a>.
    </li>
    
    <li>
      Dovrebbe usare E2EE per tutti i messaggi di default.
    </li>
    
    <li>
      Dovrebbe supportare Linux, macOS, Windows, Android e iOS.
    </li></ul> 
    
    <footnotes>
      <fn name="3" spaces-before="0">
        <p spaces-before="0">
          You may refer to this step-by-step tutorial in German on how to set up UnifiedPush as the notification provider for Molly: <a href="https://kuketz-blog.de/messenger-wechsel-von-signal-zu-molly-unifiedpush-mollysocket-ntfy">https://kuketz-blog.de/messenger-wechsel-von-signal-zu-molly-unifiedpush-mollysocket-ntfy</a>.
        </p>
      </fn>
      
      <fn name="1" spaces-before="0">
        <p spaces-before="0">
          <a href="https://en.wikipedia.org/wiki/Forward_secrecy">Segretezza in avanti</a> è quando le chiavi sono ruotate molto frequentemente, in questo modo anche se la chiave crittografica attuale viene compromessa questo non espone anche messaggi <strong x-id="1">passati</strong>.
        </p>
      </fn>
      
      <fn name="2" spaces-before="0">
        <p spaces-before="0">
          La segretezza futura ( o <a href="https://eprint.iacr.org/2016/221.pdf">sicurezza post compromesso</a>) è una funzione dove a un malintenzionato viene impedito di decriptare messaggi <strong x-id="1">futuri</strong> dopo aver compromesso una chiave privata, a meno che non comprometta altre chiavi di sessione in futuro. Questo forza efficacemente il malintenzionato a intercettare tutta la comunicazione tra le persone dato che ne perde l'accesso non appena avviene uno scambio di chiave non intercettato.
        </p>
      </fn>
    </footnotes>
