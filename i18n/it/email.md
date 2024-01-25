---
meta_title: "Email Private Crittografate Consigliate - Privacy Guides"
title: "Servizi Email"
icon: material/email
description: Questi fornitori di email offrono un luogo ideale per memorizzare in sicurezza le tue email e, molti, offrono crittografia OpenPGP interoperabile con altri fornitori.
cover: email.webp
---

L'email è praticamente una necessità per utilizzare qualsiasi servizio online, tuttavia, la sconsigliamo per le conversazioni personali. Piuttosto che utilizzare l'email per contattare altre persone, considera di utilizzare un mezzo di messaggistica istantanea che supporti la Forward Secrecy, letteralmente, Segretezza in avanti.

[Messaggistica istantanea consigliata](real-time-communication.md ""){.md-button}

Per tutto il resto, consigliamo una varietà di provider di posta elettronica basati su modelli di business sostenibile e funzioni di sicurezza integrate.

- [Fornitori Email Compatibili con OpenPGP :material-arrow-right-drop-circle:](#openpgp-compatible-services)
- [Altri Fornitori Criptati :material-arrow-right-drop-circle:](#more-providers)
- [Servizi di Aliasing Email :material-arrow-right-drop-circle:](#email-aliasing-services)
- [Opzioni Self-Hosted :material-arrow-right-drop-circle:](#self-hosting-email)

## Servizi Compatibili con OpenPGP

Questi provider supportano in modo nativo la crittografia/decrittografia OpenPGP e lo [standard Web Key Directory](basics/email-security.md#what-is-the-web-key-directory-standard), consentendo la creazione di e-mail E2EE indipendenti dal provider. Ad esempio, un utente di Proton Mail potrebbe inviare un messaggio E2EE a un utente Mailbox.org, o potresti ricevere notifiche crittografate in OpenPGP dai servizi Internet che le supportano.

<div class="grid cards" markdown>

- ![Proton Mail logo](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![Skiff Mail logo](assets/img/email/skiff-mail.svg){ .twemoji } [Skiff Mail](email.md#skiff-mail)
- ![Mailbox.org logo](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

Quando si utilizza una tecnologia E2EE come OpenPGP, la tua e-mail presenta ancora alcuni metadati non crittografati nell'intestazione dell'e-mail, tra cui generalmente l'oggetto! Per saperne di più sui [matadati delle e-mail](basics/email-security.md#email-metadata-overview).

Inoltre, OpenPGP non supporta la Forward Secrecy, ciò significa che se la chiave privata tua o del destinatario viene rubata, tutti i messaggi precedenti crittografati con essa, saranno esposti. [Come proteggo le mie chiavi private?](basics/email-security.md#how-do-i-protect-my-private-keys)

</div>

### Proton Mail

<div class="admonition recommendation" markdown>

![Proton Mail logo](assets/img/email/protonmail.svg){ align=right }

**Proton Mail** è un servizio di posta elettronica incentrato su privacy, crittografia, sicurezza e facilità d'uso. Operano dal **2013**. Proton AG ha sede a Ginevra, Svizzera. Gli account partono da 500MB di spazio di archiviazione con il piano gratuito.

[:octicons-home-16: Homepage](https://proton.me/mail){ .md-button .md-button--primary }
[:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Servizio Onion" }
[:octicons-eye-16:](https://proton.me/legal/privacy){ .card-link title="Informativa sulla Privacy" }
[:octicons-info-16:](https://proton.me/support/mail){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Codice sorgente" }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/apple-store/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/proton-mail-android/releases)
- [:simple-windows11: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: Web](https://mail.proton.me)

</details>

</div>

Gli account gratuiti presentano delle limitazioni, come l'incapacità di cercare il testo del corpo e l'assenza dell'accesso a [Proton Mail Bridge](https://proton.me/mail/bridge), necessario per utilizzare un [client email desktop consigliato](email-clients.md) (come Thunderbird). I profili a pagamento includono funzionalità come Proton Mail Bridge, archiviazione aggiuntiva e supporto ai domini personalizzati. Una [lettera di attestazione](https://proton.me/blog/security-audit-all-proton-apps) è stata fornita per le applicazioni di Proton Mail il 9 novembre 2021 da [Securitum](https://research.securitum.com).

Se hai il piano Proton Unlimited, Business o Visionary, inoltre, ottieni [SimpleLogin](#simplelogin) Premium, gratuitamente.

Proton Mail ha dei rapporti sugli arresti anomali interni che **non** condividono con terze parti. Ciò è disabilitabile in: **Impostazioni** > **Vai alle Impostazioni** > **Profilo** > **Sicurezza e privacy** > **Invia rapporti sugli arresti anomali**.

#### :material-check:{ .pg-green } Domini e Alias Personalizzati

Gli abbonati a Proton Mail a pagamento possono utilizzare il proprio dominio con il servizio o un indirizzo [catch-all](https://proton.me/support/catch-all). Inoltre, Proton Mail supporta il [sottoindirizzamento](https://proton.me/support/creating-aliases), utile per chi non desidera acquistare un dominio.

#### :material-check:{ .pg-green } Metodi di pagamento privati

Proton Mail [accetta](https://proton.me/support/payment-options) contanti per posta, oltre ai normali pagamenti con carta di credito/debito, [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc) e PayPal.

#### :material-check:{ .pg-green } Sicurezza dell'account

Proton Mail supporta l'[autenticazione a due fattori](https://proton.me/support/two-factor-authentication-2fa) TOTP e le [chiavi di sicurezza hardware](https://proton.me/support/2fa-security-key), utilizzando gli standard FIDO2 o U2F. L'utilizzo di una chiave di sicurezza hardware richiede la configurazione precedente dell'autenticazione a due fattori TOTP.

#### :material-check:{ .pg-green } Sicurezza dei dati

Proton Mail presenta una [crittografia ad accesso zero](https://proton.me/blog/zero-access-encryption) a riposo, per le tue email e i tuoi [calendari](https://proton.me/news/protoncalendar-security-model). I dati protetti con la crittografia ad accesso zero sono accessibili soltanto da te.

Certe informazioni memorizzate su [Proton Contact](https://proton.me/support/proton-contacts), come i nomi visualizzati e gli indirizzi email, non sono protette da tale crittografia. I campi di contatto che supportano la crittografia ad accesso zero, come i numeri di telefono, sono indicati con l'icona di un lucchetto.

#### :material-check:{ .pg-green } Crittografia Email

Proton Mail ha una [crittografia OpenPGP integrata](https://proton.me/support/how-to-use-pgp) nella propria webmail. Le e-mail inviate ad altri account Proton Mail vengono crittografate automaticamente, e la crittografia verso indirizzi non Proton Mail con una chiave OpenPGP può essere abilitata nelle impostazioni dell'account. Proton supporta anche il rilevamento automatico di chiavi esterne con [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). Ciò significa che anche le e-mail inviate ad altri provider che utilizzano WKD, come Skiff Mail, saranno automaticamente crittografate con OpenPGP, senza la necessità di scambiare manualmente le chiavi PGP pubbliche con i tuoi contatti. Consentono inoltre di [crittografare i messaggi inviati a indirizzi non Proton Mail senza OpenPGP](https://proton.me/support/password-protected-emails), senza la necessità di aprire un account Proton Mail.

Proton Mail pubblica anche le chiavi pubbliche degli account Proton via HTTP dal loro WKD. Ciò permette a coloro che non utilizzano Proton Mail, di trovare facilmente le chiavi OpenPGP dei profili di Proton Mail, per un'E2EE tra fornitori. Questo vale solo per gli indirizzi e-mail che terminano con uno dei domini di proprietà di Proton, come @proton.me. Se si utilizza un dominio personalizzato, è necessario [configurare il WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separatamente.

#### :material-information-outline:{ .pg-blue } Chiusura dell'account

Se hai un account a pagamento e il tuo [abbonamento non viene pagato](https://proton.me/support/delinquency) dopo 14 giorni, non potrai accedere ai tuoi dati. Dopo 30 giorni, il tuo account sarà considerato moroso e non riceverà la posta in arrivo. Durante questo periodo, continuerai a essere addebitato.

#### :material-information-outline:{ .pg-blue } Funzionalità aggiuntive

Proton Mail offre un profilo "Unlimited" per €9,99/Mese, che consente inoltre l'accesso a Proton VPN, oltre a fornire multipli profili, domini, alias e 500GB di archiviazione.

Proton Mail non offre una funzionalità di eredità digitale.

### Skiff Mail

<div class="admonition recommendation" markdown>

![Logo di Skiff Mail](assets/img/email/skiff-mail.svg){ align=right }

**Skiff Mail** è un servizio email basato sul web con E2EE, nato nel 2020 con sede a San Francisco e sviluppatori da tutto il mondo. I profili partono da 10GB di archiviazione gratuita.

[:octicons-home-16: Pagina Principale](https://skiff.com/mail){ .md-button .md-button--primary }
[:octicons-eye-16:](https://app.skiff.com/docs/db93c237-84c2-4b2b-9588-19a7cd2cd45a#tyGksN9rkqbo2uGYASxsA6HVLjUoly/wTYK8tncTto8=){ .card-link title="Politica sulla Privacy" }
[:octicons-info-16:](https://skiff.com/help){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/skiff-org/skiff-apps){ .card-link title="Codice Sorgente" }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-android: Android](https://play.google.com/store/apps/details?id=com.skemailmobileapp&gl=IT)
- [:simple-appstore: iOS](https://apps.apple.com/it/app/skiff-mail-private-email/id1619168801)
- [:octicons-browser-16: Web](https://app.skiff.com/mail)

</details>

</div>

Durante lo sviluppo, Skiff è stato sottoposto ad alcuni [controlli](https://skiff.com/transparency).

#### :material-check:{ .pg-green } Domini e Alias personalizzati

Puoi creare fino a 3 alias email @skiff.com aggiuntivi, oltre all'indirizzo del tuo profilo principale, con il loro piano gratuito. Gli account gratuiti possono aggiungere 1 [dominio personalizzato](https://skiff.com/blog/custom-domain-setup), e fino a 15 domini personalizzati con un piano a pagamento. Puoi creare un numero illimitato di alias o un alias [di tipo catch-all](https://skiff.com/blog/catch-all-email-alias) sul tuo dominio personalizzato.

#### :material-alert-outline:{ .pg-orange } Metodi di pagamento privati

Skiff Mail accetta i pagamenti in criptovalute tramite Coinbase Commerce, tra cui Bitcoin ed Ethereum, ma non accetta la nostra [criptovaluta](cryptocurrency.md) consigliata, Monero. Inoltre, accetta i pagamenti con carta di credito, tramite Stripe.

#### :material-check:{ .pg-green } Sicurezza dell'account

Skiff Mail supporta l'autenticazione a due fattori TOTP e le chiavi di sicurezza hardware, utilizzando gli standard FIDO2 o U2F. L'utilizzo di una chiave di sicurezza hardware richiede prima l'impostazione dell'autenticazione a due fattori TOTP.

#### :material-check:{ .pg-green } Sicurezza dei dati

Skiff Mail ha una crittografia ad accesso zero a riposo per tutti i tuoi dati. Ciò significa che messaggi e altri dati memorizzati nel tuo profilo, sono leggibili soltanto da te.

#### :material-check:{ .pg-green } Crittografia Email

Skiff Mail cifra automaticamente i messaggi verso altre caselle di posta Skiff con E2EE. Il 18 dicembre 2023, Skiff ha aggiunto il supporto per PGP e il rilevamento automatico delle chiavi pubbliche tramite Web Key Directory (WKD). Ciò significa che le e-mail inviate ad altri provider che utilizzano WKD, come Proton Mail, saranno automaticamente crittografate anche con OpenPGP senza dover scambiare chiavi PGP pubbliche con i tuoi contatti. I nuovi account Skiff Mail dovrebbero avere una chiave PGP generata automaticamente, mentre gli account precedenti all'introduzione di questa funzione devono generare una nuova chiave PGP per il loro indirizzo (o caricare una chiave privata esistente) nelle impostazioni dell'indirizzo dell'account. Skiff Mail supporta solo la lettura di messaggi crittografati con PGP/MIME, non con il vecchio standard PGP/Inline. L'invio di messaggi con PGP/MIME è [l'approccio consigliato](https://www.gnupg.org/faq/gnupg-faq.html#use_pgpmime), ma può presentare problemi di compatibilità in alcuni casi limite.

Anche Skiff Mail pubblica le chiavi pubbliche degli account Skiff Mail via HTTP dal proprio [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). Questo permette a chi non usa Skiff Mail di trovare facilmente le chiavi OpenPGP degli account Skiff Mail, per un E2EE cross-provider. Questo vale solo per gli indirizzi e-mail che terminano con uno dei domini di Skiff, come @skiff.com. Se si utilizza un dominio personalizzato, è necessario [configurare il WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separatamente.

Skiff non dispone di una funzione di "casella di posta temporanea" o di "e-mail con password" come altri provider, per cui gli utenti esterni senza OpenPGP non possono ricevere o rispondere ai messaggi con E2EE.

#### :material-information-outline:{ .pg-blue } Chiusura dell'account

Gli account Skiff Mail non scadono, ma agli account non paganti verrà richiesto di rimuovere eventuali funzioni a pagamento abilitate (come gli alias aggiuntivi) o di rinnovare il piano prima che l'account possa essere utilizzato.

#### :material-information-outline:{ .pg-blue } Funzionalità aggiuntive

Inoltre, Skiff offre [funzionalità di produttività sul lavoro](https://discuss.privacyguides.net/t/skiff-pages-drive-productivity-tools/11758/13), ma preferiamo comunque delle opzioni [alternative](productivity.md) per la collaborazione e la condivisione dei file, al momento.

Skiff Mail non offre una funzionalità di eredità digitale.

### Mailbox.org

<div class="admonition recommendation" markdown>

![Logo di Mailbox.org](assets/img/email/mailboxorg.svg){ align=right }

**Mailbox.org** è un servizio email incentrato sull'essere sicuro, privo di pubblicità e alimentato privatamente da energia ecologica al 100%. Sono operativi dal 2014. Mailbox.org ha sede a Berlino, in Germania. I profili partono da 2 GB di archiviazione, aggiornabile se necessario.

[:octicons-home-16: Pagina Principale](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Politica sulla Privacy" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title=Documentazione}

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:octicons-browser-16: Web](https://login.mailbox.org)

</details>

</div>

#### :material-check:{ .pg-green } Domini e Alias personalizzati

Mailbox.org ti consente di utilizzare il tuo dominio e supporta gli indirizzi [catch-all](https://kb.mailbox.org/display/MBOKBEN/Using+catch-all+alias+with+own+domain). Anche Mailbox.org supporta il [sottoindirizzamento](https://kb.mailbox.org/display/BMBOKBEN/What+is+an+alias+and+how+do+I+use+it), utile se non desideri acquistare un dominio.

#### :material-check:{ .pg-green } Metodi di pagamento privati

Mailbox.org non accetta criptovalute a causa della sospensione delle attività del suo elaboratore di pagamenti BitPay, in Germania. Tuttavia, accettano contanti per posta, pagamento in contanti su conto corrente, bonifico bancario, carta di credito, PayPal e un paio di processori specifici per la Germania: paydirekt e Sofortüberweisung.

#### :material-check:{ .pg-green } Sicurezza dell'account

Mailbox.org supporta l'[autenticazione a due fattori](https://kb.mailbox.org/display/MBOKBEN/How+to+use+two-factor+authentication+-+2FA) solo per la propria webmail. Puoi utilizzare TOTP o una [YubiKey](https://en.wikipedia.org/wiki/YubiKey), tramite [YubiCloud](https://www.yubico.com/products/services-software/yubicloud). Gli standard Web come [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn) non sono ancora supportati.

#### :material-information-outline:{ .pg-blue } Sicurezza dei dati

Mailbox.org consente la crittografia della posta in arrivo, tramite la loro [casella di posta crittografata](https://kb.mailbox.org/display/MBOKBEN/The+Encrypted+Mailbox). I nuovi messaggi ricevuti, saranno immediatamente crittografati con la tua chiave pubblica.

Tuttavia, [Open-Exchange](https://en.wikipedia.org/wiki/Open-Xchange), la piattaforma software utilizzata da Mailbox.org, [non supporta](https://kb.mailbox.org/display/BMBOKBEN/Encryption+of+calendar+and+address+book) la crittografia della tua rubrica e del calendario. Un'[opzione indipendente](calendar.md) può essere più appropriata per tali informazioni.

#### :material-check:{ .pg-green } Crittografia Email

Mailbox.org presenta una [crittografia integrata](https://kb.mailbox.org/display/MBOKBEN/Send+encrypted+e-mails+with+Guard) nella propria webmail, che semplifica l'invio di messaggi a persone con le chiavi OpenPGP pubbliche. Inoltre, consente ai [destinatari da remoto di decrittografare un'email](https://kb.mailbox.org/display/MBOKBEN/My+recipient+does+not+use+PGP) sui server di Mailbox.org. Questa funzionalità è utile quando il destinatario da remoto non ha OpenPGP e non può decrittografare una copia dell'email nella propria casella.

Inoltre, Mailbox.org supporta la scoperta di chiavi pubbliche tramite HTTP dalla loro [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). Questo permette a persone esterne a Mailbox.org di trovare facilmente le chiavi OpenPGP degli account di Mailbox.org, per un E2EE fra provider diversi. Questo vale solo per gli indirizzi e-mail che terminano con uno dei domini di Mailbox.org, come @mailbox.org. Se si utilizza un dominio personalizzato, è necessario [configurare il WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separatamente.

#### :material-information-outline:{ .pg-blue } Chiusura dell'account

Il tuo profilo sarà impostato come limitato al termine del tuo contratto; dopo [30 giorni sarà irrevocabilmente eliminato](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } Funzionalità aggiuntive

Puoi accedere al tuo profilo di Mailbox.org tramite IMAP/SMTP, utilizzando il loro [servizio .onion](https://kb.mailbox.org/display/MBOKBEN/The+Tor+exit+node+of+mailbox.org). Tuttavia, l'interfaccia webmail non è accessibile tramite il loro servizio .onion e potresti riscontrare errori del certificato TLS.

Tutti i profili presentano archiviazione su cloud limitata e [crittografabile](https://kb.mailbox.org/display/MBOKBEN/Encrypt+files+on+your+Drive). Inoltre, Mailbox.org offre l'alias [@secure.mailbox.org](https://kb.mailbox.org/display/MBOKBEN/Ensuring+E-Mails+are+Sent+Securely), che impone la crittografia TLS sulla connessione tra server email, altrimenti, il messaggio non sarà affatto inviato. Mailbox.org supporta anche [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync), oltre ai protocolli di accesso standard come IMAP e POP3.

Mailbox.org dispone di una funzione di eredità digitale per tutti i piani. Puoi scegliere se desideri che i tuoi dati siano passati agli eredi, supponendo che lo richiedano e forniscano il tuo testamento. In alternativa, puoi nominare una persona per nome e indirizzo.

## Altri fornitori

Questi fornitori memorizzano le tue email con la crittografia a conoscenza zero, rendendoli ottime opzioni per mantenere protette le tue email memorizzate. Tuttavia, non supportano standard di crittografia interoperabili per le comunicazioni E2EE tra fornitori diversi.

<div class="grid cards" markdown>

- ![Logo Tuta](assets/img/email/tuta.svg){ .twemoji } [Tuta](email.md#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Logo di Tuta](assets/img/email/tuta.svg){ align=right }

**Tuta** è un servizio di posta elettronica incentrato sulla sicurezza e sulla privacy attraverso l'uso della crittografia. Tuta è operativo dal **2011** e ha sede ad Hannover, in Germania. I profili partono da 1GB di archiviazione, con il loro piano gratuito.

[:octicons-home-16: Pagina Principale](https://tuta.com/it/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tuta.com/it/privacy){ .card-link title="Politica sulla Privacy" }
[:octicons-info-16:](https://tuta.com/faq){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="Codice Sorgente" }
[:octicons-heart-16:](https://tuta.com/it/community/){ .card-link title=Contribuisci }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota&gl=IT)
- [:simple-appstore: App Store](https://apps.apple.com/it/app/tuta-encrypted-email-app/id922429609)
- [:simple-github: GitHub](https://github.com/tutao/tutanota/releases)
- [:simple-windows11: Windows](https://tuta.com/it/#download)
- [:simple-apple: macOS](https://tuta.com/it/#download)
- [:simple-linux: Linux](https://tuta.com/it/#download)
- [:octicons-browser-16: Web](https://app.tuta.com/)

</details>

</div>

Tuta non supporta il [protocollo IMAP](https://tuta.com/faq/#imap) o l'utilizzo di [client email](email-clients.md) di terze parti e, inoltre, non potrai aggiungere [account email esterni](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) all'app di Tuta. [L'importazione di email](https://github.com/tutao/tutanota/issues/630) non è attualmente supportata, anche se questo aspetto è destinato ad [essere modificato](https://tuta.com/blog/posts/kickoff-import). Le email possono essere esportate [singolarmente o tramite selezione in blocco](https://tuta.com/howto#generalMail) per cartella, il che può risultare scomodo se hai molte cartelle.

#### :material-check:{ .pg-green } Domini e Alias Personalizzati

Gli account di Tuta a pagamento possono utilizzare 15 o 30 alias a seconda del piano e alias illimitati sui [domini personalizzati](https://tuta.com/faq#custom-domain). Tuta non consente il [sottoindirizzamento (più indirizzi)](https://tuta.com/faq#plus), ma puoi utilizzare un [catch-all](https://tuta.com/howto#settings-global) con un dominio personalizzato.

#### :material-information-outline:{ .pg-blue } Metodi di pagamento privati

Tuta accetta diretti soltanto carte di credito e PayPal, tuttavia, le [criptovalute](cryptocurrency.md) sono utilizzabili per acquistare carte regalo tramite la loro [collaborazione](https://tuta.com/faq/#cryptocurrency) con Proxystore.

#### :material-check:{ .pg-green } Sicurezza dell'account

Tuta supporta [l'autenticazione a due fattori](https://tuta.com/faq#2fa) con TOTP o U2F.

#### :material-check:{ .pg-green } Sicurezza dei dati

Tuta dispone di [crittografia ad accesso zero a riposo](https://tuta.com/faq#what-encrypted) per le tue email, [i tuoi contatti della rubrica](https://tuta.com/faq#encrypted-address-book) e [i tuoi calendari](https://tuta.com/faq#calendar). Ciò significa che messaggi e altri dati memorizzati nel tuo profilo, sono leggibili soltanto da te.

#### :material-information-outline:{ .pg-blue } Crittografia Email

Tuta [non utilizza OpenPGP](https://tuta.com/support/#pgp). Gli account Tuta possono ricevere email criptate da account email non Tuta solo se inviate tramite una [casella di posta Tuta temporanea](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } Chiusura dell'account

Tuta [eliminerà gli account gratuiti inattivi](https://tuta.com/faq#inactive-accounts) dopo sei mesi. Puoi riutilizzare un profilo gratuito disattivato, previo pagamento.

#### :material-information-outline:{ .pg-blue } Funzionalità aggiuntive

Tuta offre la versione aziendale di [Tuta alle organizzazioni non profit](https://tuta.com/blog/posts/secure-email-for-non-profit) gratuitamente o con un ottimo sconto.

Tuta ha anche una funzionalità aziendale, chiamata [Secure Connect](https://tuta.com/secure-connect/). Questa, garantisce che il contatto del cliente con l'azienda utilizzi l'E2EE. La funzionalità costa €240 all'anno.

Tuta non offre una funzionalità di eredità digitale.

## Servizi di Alias per Email

Un servizio di alias dell'email ti consente di generare facilmente un nuovo indirizzo email per ogni sito web cui ti registri. Gli alias email che generi sono quindi inoltrati a un indirizzo email di tua scelta, nascondendo sia il tuo indirizzo email "principale" che l'identità del tuo fornitore email. Il vero aliasing email è migliore dell'indirizzamento più comunemente utilizzato ed è supportato da molti fornitori, consentendoti di creare alias come tuonome+[qualsiasicosaqui]@esempio.it, poiché siti web, inserzionisti e reti di tracciamento, possono banalmente rimuovere qualsiasi cosa dopo il segno '+', per conoscere il tuo vero indirizzo email.

<div class="grid cards" markdown>

- ![Logo di addy.io](assets/img/email/mini/addy.svg){ .twemoji } [addy.io](email.md#addyio)
- ![Logo di SimpleLogin](assets/img/email/simplelogin.svg){ .twemoji } [SimpleLogin](email.md#simplelogin)

</div>

L'alias email può agire da salvaguardia, nel caso in cui il tuo fornitore di email cessi di operare. In tal caso, è possibile reindirizzare facilmente gli alias a un nuovo indirizzo email. A sua volta, tuttavia, ti stai affidando al fatto che il servizio di aliasing continui a funzionare.

Inoltre, utilizzare un servizio dedicato di alias email, presenta numerosi benefici rispetto a un alias catch-all su un dominio personalizzato:

- Gli alias possono essere attivati e disattivati singolarmente quando se ne ha bisogno, evitando che i siti web inviino e-mail a caso.
- Le risposte sono inviate dall'indirizzo dell'alias, proteggendo il tuo indirizzo email reale.

Inoltre, presentano numerosi benefici, rispetto ai servizi di "email temporanea":

- Gli alias sono permanenti e possono essere riattivati nel caso in cui sia necessario ricevere qualcosa come la reimpostazione della password.
- Le email sono inviate alla tua casella di fiducia, piuttosto che memorizzate dal fornitore dell'alias.
- I servizi di posta elettronica temporanea hanno in genere caselle di posta pubbliche a cui può accedere chiunque conosca l'indirizzo, mentre gli alias sono privati.

Gli alias email che consigliamo, sono fornitori che ti consentono di creare alias sui domini che controllano, nonché sui tuoi domini personalizzati, per un modesto costo annuale. Inoltre, possono essere auto-ospitati, se desideri il massimo controllo. Tuttavia, utilizzare un dominio personalizzato può avere degli svantaggi relativi alla privacy: Se sei il solo a utilizzare il tuo dominio personalizzato, le tue azioni sono facilmente monitorabili sui siti web, semplicemente osservando il nome di dominio nell'indirizzo email, e ignorando tutto ciò che precede il segno della chiocciola (@).

Utilizzare un servizio di alias richiede di affidare i tuoi messaggi crittografati sia al fornitore della tua email che al fornitore del tuo alias. Alcuni fornitori mitigano lievemente questo problema con la crittografia PGP automatica, riiducendo il numero di parti di cui devi fidarti da due a una, crittografando le email in entrata prima che siano consegnate al fornitore finale della tua casella.

### addy.io

<div class="admonition recommendation" markdown>

![Logo di addy.io](assets/img/email/addy.svg#only-light){ align=right }
![Logo di addy.io](assets/img/email/addy-dark.svg#only-dark){ align=right }

**addy.io** ti consente di creare gratuitamente 10 alias di dominio su un dominio condiviso, oppure alias "standard" illimitati, meno anonimi.

[:octicons-home-16: Pagina Principale](https://addy.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://addy.io/privacy){ .card-link title="Politica sulla Privacy" }
[:octicons-info-16:](https://app.addy.io/docs){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/anonaddy){ .card-link title="Codice Sorgente" }
[:octicons-heart-16:](https://addy.io/donate){ .card-link title=Contribuisci }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-android: Android](https://addy.io/faq/#is-there-an-android-app)
- [:material-apple-ios: iOS](https://addy.io/faq/#is-there-an-ios-app)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/it/firefox/addon/addy_io/)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/addyio-anonymous-email-fo/iadbdpnoknmbdeolbapdackdcogdmjpe?hl=it)

</details>

</div>

Il numero di alias condivisi (che terminano con un dominio condiviso come @addy.io) che puoi creare è limitato a 10 sul piano gratuito di addy.io, 50 sul piano da €1/mese e illimitato sul piano da €4/mese (fatturato €3 per un anno). Puoi creare un numero illimitato di alias standard (che terminano con un dominio come @[username].addy.io o con un dominio personalizzato nei piani a pagamento), tuttavia, come detto in precedenza, questo può essere dannoso per la privacy poichè le persone possono banalmente collegare i tuoi alias standard basandosi unicamente sul nome del dominio. Sono utili quando un dominio condiviso potrebbe essere bloccato da un servizio. Securitum [ha effettuato un audit](https://addy.io/blog/addy-io-passes-independent-security-audit/) su addy.io nel settembre 2023 e non sono state identificate [vulnerabilità significative](https://addy.io/addy-io-security-audit.pdf).

Funzionalità gratuite degne di nota:

- [x] 10 alias condivisi
- [x] Alias standard illimitati
- [ ] Non sono possibili le risposte in uscita
- [x] 1 Casella email del destinatario
- [x] Crittografia automatica PGP

### SimpleLogin

<div class="admonition recommendation" markdown>

![Logo di Simplelogin](assets/img/email/simplelogin.svg){ align=right }

**SimpleLogin** è un servizio gratuito che fornisce alias email su numerosi nomi di dominio condivisi e, facoltativamente, fornisce funzionalità a pagamento quali alias illimitati e domini personalizzati.

[:octicons-home-16: Pagina Principale](https://simplelogin.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://simplelogin.io/privacy/){ .card-link title="Politica sulla Privacy" }
[:octicons-info-16:](https://simplelogin.io/docs/){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/simple-login){ .card-link title="Codice Sorgente" }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.simplelogin.android&gl=IT)
- [:simple-appstore: App Store](https://apps.apple.com/it/app/simplelogin-email-alias/id1494359858)
- [:simple-github: GitHub](https://github.com/simple-login/Simple-Login-Android/releases)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/it/firefox/addon/simplelogin/)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/dphilobhebphkdjbpfohgikllaljmgbn?hl=it)
- [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/simpleloginreceive-sen/diacfpipniklenphgljfkmhinphjlfff?hl=it-IT&gl=IT)
- [:simple-safari: Safari](https://apps.apple.com/app/id1494051017)

</details>

</div>

SimpleLogin è stata [acquisita da Proton AG](https://proton.me/news/proton-and-simplelogin-join-forces) l'8 aprile del 2022. Se utilizzi Proton Mail come tua casella di posta principale, SimpleLogin è un'ottima scelta. Poiché entrambi i prodotti sono ora posseduti dalla stessa azienda, devi ora affidarti a una singola entità. Inoltre, prevediamo che SimpleLogin sarà maggiormente integrato con le offerte future di Proton. SimpleLogin continua a supportare l'inoltro a qualsiasi fornitore di email di tua scelta. Securitum [ha revisionato](https://simplelogin.io/blog/security-audit/) SimpleLogin all'inizio del 2022 e tutti i problemi [sono stati risolti](https://simplelogin.io/audit2022/web.pdf).

Puoi collegare il tuo profilo di SimpleLogin con quello di Proton nelle impostazioni. Se hai il Piano Unlimited, Business o Visionary di Proton, avrai SimpleLogin Premium gratuitamente.

Caratteristiche gratuite degne di nota:

- [x] 10 alias condivisi
- [x] Risposte illimitate
- [x] 1 Casella email del destinatario

## Auto-Hosting Email

Gli amministratori di sistema avanzati potrebbero considerare la configurazione del proprio server email. I server email richiedono attenzione e manutenzione continua, per mantenere tutto in sicurezza e la consegna delle email affidabile.

### Soluzioni software combinate

<div class="admonition recommendation" markdown>

![Logo di Mailcow](assets/img/email/mailcow.svg){ align=right }

**Mailcow** è un server email più avanzato, perfetto per chi ha un po' più d'esperienza con Linux. Ha tutto il necessario in un contenitore Docker: Un server email con supporto DKIM, antivirus e monitoraggio dello spam, webmail e ActiveSync con SOGo e amministrazione basata sul web con supporto A2F.

[:octicons-home-16: Pagina Principale](https://mailcow.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://mailcow.github.io/mailcow-dockerized-docs/){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="Codice sorgente" }
[:octicons-heart-16:](https://www.servercow.de/mailcow?lang=en#sal){ .card-link title=Contribuisci }

</div>

<div class="admonition recommendation" markdown>

![Logo di Mail-in-a-Box](assets/img/email/mail-in-a-box.svg){ align=right }

**Mail-in-a-Box** è uno script di configurazione automatica per la distribuzione di un server email su Ubuntu. Il suo obiettivo è semplificare la configurazione del proprio server email alle persone.

[:octicons-home-16: Pagina Principale](https://mailinabox.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="Codice sorgente" }

</div>

Per un approccio più manuale, abbiamo scelto questi due articoli:

- [Configurare un server email con OpenSMTPD, Dovecot e Rspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd/) (2019)
- [Come Gestire il Tuo Server Email](https://www.c0ffee.net/blog/mail-server-guide/) (Agosto 2017)

## Criteri

**Si prega di notare che non siamo affiliati con alcun fornitore consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una chiara serie di requisiti per qualsiasi fornitore email che desideri essere consigliato, inclusa l'implementazione delle migliori pratiche del settore, tecnologia moderna e altro. Ti consigliamo di familiarizzare con questo elenco prima di scegliere un provider di posta elettronica e condurre le tue ricerche per assicurarti che il provider di posta elettronica che scegli sia la scelta giusta per te.

### Tecnologia

Consideriamo queste funzionalità come importanti per poter fornire un servizio sicuro e ottimale. Dovresti considerare se il fornitore ha le funzionalità di cui necessiti.

**Requisiti minimi:**

- Crittografia dei dati degli account email a riposo con crittografia ad "accesso zero".
- Possibilità di esportazione come [Mbox](https://en.wikipedia.org/wiki/Mbox) o singoli .eml con lo standard [RFC5322](https://datatracker.ietf.org/doc/rfc5322/) .
- Consente agli utenti di utilizzare il proprio [nome di dominio](https://en.wikipedia.org/wiki/Domain_name). I nomi di dominio personalizzati sono importanti per gli utenti, poiché consentono loro di mantenere la propria autonomia dal servizio, dovesse diventare negativo o essere acquisito da un'altra azienda che non dà priorità alla privacy.
- Opera su un'infrastruttura proprietaria, cioè, non basata su fornitori del servizio email di terze parti.

**Miglior Caso:**

- Crittografa tutti i dati del profilo (Contatti, Calendari, etc.) a riposo con crittografia ad accesso zero.
- Crittografia E2EE/PGP della webmail integrata, fornita per comodità.
- Supporto per [WKD](https://wiki.gnupg.org/WKD) per consentire la scoperta migliorata delle chiavi pubbliche di OpenPGP tramite HTTP. Gli utenti di GnuPG possono ottenere una chiave digitando: `gpg --locate-key example_user@example.com`
- Supporto per una casella temporanea per gli utenti esterni. Questo è utile quando desideri inviare un'email crittografata, senza inviare una copia effettiva al tuo destinatario. Queste email, solitamente, hanno una durata limitata, prima di essere eliminate automaticamente. Inoltre, non richiedono al destinatario di configurare alcuna crittografia, come OpenPGP.
- Disponibilità dei servizi del fornitore email tramite un [servizio onion](https://en.wikipedia.org/wiki/.onion).
- Supporto del [sottoindirizzamento](https://en.wikipedia.org/wiki/Email_address#Subaddressing).
- Funzionalità di catch-all o alias per coloro che possiedono i propri domini.
- Utilizzo di protocolli d'accesso email standard, quali IMAP, SMTP o [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). I protocolli d'accesso standard assicurano ai clienti di scaricare facilmente tutte le proprie email, qualora dovessero passare a un altro fornitore.

### Privacy

Preferiamo che i fornitori consigliati raccolgano il minor numero di dati possibile.

**Requisiti minimi:**

- Protezione dell'indirizzo IP del mittente. Filtraggio dello stesso dalla visualizzazione nel campo dell'intestazione `Ricevuto`.
- Non richiedere informazioni d'identificazione personale (PII), tranne un nome utente e una password.
- Politica sulla privacy che soddisfi i requisiti definiti dal GDPR.

**Miglior Caso:**

- Accetta [opzioni di pagamento anonime](advanced/payments.md) ([criptovalute](cryptocurrency.md), contanti, carte regalo, etc.)
- Ospitato in una giurisdizione con forti regolamentazioni sulla protezione della privacy email.

### Sicurezza

I server email gestiscono molti dati, estremamente sensibili. Ci aspettiamo che i fornitori adotteranno le migliori pratiche del settore, per proteggere i propri membri.

**Requisiti minimi:**

- Protezione della webmail con 2FA, ad esempio TOTP.
- Crittografia ad accesso zero, basata sulla crittografia a riposo. Il provider non deve disporre delle chiavi di decrittazione dei dati in loro possesso. Questo previene che dipendenti disonesti possano trapelare i dati sensibili, o che un avversario remoto possa rilasciarli, dopo averli rubati, ottenendo un accesso non autorizzato al server.
- Supporto [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions).
- Nessun errore o vulnerabilità TLS quando profilati da strumenti quali [Hardenize](https://www.hardenize.com/), [testssl.sh](https://testssl.sh/) o [Qualys SSL Labs](https://www.ssllabs.com/ssltest); ciò include gli errori relativi al certificato e i parametri deboli DH, come quelli che hanno portato al [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- Una preferenza della suite del server (facoltativa su TLSv1.3), per forti suite di cifratura che supportino la segretezza in avanti e la crittografia autenticata.
- Una valida politica [MTA-STS](https://tools.ietf.org/html/rfc8461) e [TLS-RPT](https://tools.ietf.org/html/rfc8460).
- Registri [DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities) validi.
- Registri [SPF](https://en.wikipedia.org/wiki/Sender_Policy_Framework) e [DKIM](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail) validi.
- Disporre di un registro o una politica [DMARC](https://en.wikipedia.org/wiki/DMARC) adeguati o utilizzare [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) per l'autenticazione. Se si utilizza l'autenticazione DMARC, la politica dev'essere impostata su `rifiuta` o `quarantena`.
- Preferenza per una suite di server TLS 1.2 o successivo e un piano per [RFC8996](https://datatracker.ietf.org/doc/rfc8996/).
- Invio [SMTPS](https://en.wikipedia.org/wiki/SMTPS), supponendo che SMTP sia utilizzato.
- Standard di sicurezza del sito web come:
    - [HTTP Strict Transport Security](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - [Integrità Subresource](https://en.wikipedia.org/wiki/Subresource_Integrity) se si caricano oggetti da domini esterni.
- Deve supportare la visualizzazione delle [Intestazioni dei messaggi](https://en.wikipedia.org/wiki/Email#Message_header), essendo una funzionalità forense cruciale per determinare se un'email è un tentativo di phishing.

**Miglior Caso:**

- Supporto all'autenticazione hardware, cioè U2F e [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn). U2F e WebAuthn sono più sicuri, utilizzando una chiave privata, memorizzata su un dispositivo hardware dal lato del client per autenticare le persone, rispetto a un codice segreto condiviso, memorizzato sul server web e dal lato del client, utilizzando TOTP. Inoltre, U2F e WebAuthn sono più resistenti al phishing, poiché la loro risposta d'autenticazione si basa sul [nome di dominio](https://en.wikipedia.org/wiki/Domain_name) autenticato.
- [Registro Risorse di Autorizzazione dell'Autorità del Certificato (CAA) DNS](https://tools.ietf.org/html/rfc6844), oltre al supporto DANE.
- Implementazione della [Catena Autenticata Ricevuta (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), utile per le persone che pubblicano alle mailing list [RFC8617](https://tools.ietf.org/html/rfc8617).
- Programmi di caccia ai bug e/o un processo di divulgazione delle vulnerabilità coordinato.
- Standard di sicurezza del sito web, quali:
    - [Politica sulla Sicurezza dei Contenuti (CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163/)

### Fiducia

Non affideresti le tue finanze a qualcuno con un'identità falsa, quindi, perché affidare loro la tua email? Richiediamo ai nostri fornitori fidati di essere pubblici sulla propria proprietà o dirigenza. Inoltre, vorremmo vedere rapporti di trasparenza frequenti, specialmente relativi alla gestione delle richieste del governo.

**Requisiti minimi:**

- Dirigenza o proprietà rivolta al pubblico.

**Miglior Caso:**

- Dirigenza rivolta al pubblico.
- Rapporti di trasparenza frequenti.

### Marketing

Con i fornitori email che consigliamo, vorremmo vedere del marketing responsabile.

**Requisiti minimi:**

- Deve auto-ospitare le statistiche (senza Google Analytics, Adobe Analytics, etc.). Il sito del fornitore, inoltre, deve essere conforme a [DNT (Non Tracciare)](https://en.wikipedia.org/wiki/Do_Not_Track), per coloro che desiderano rinunciare.

Non deve avere alcun marketing irresponsabile:

- Dichiarazioni di "crittografia impenetrabile." La crittografia dovrebbe essere utilizzata con l'intenzione che possa non essere segreta in futuro, quando esisterà la tecnologia per decifrarla.
- Garantire la protezione dell'anonimato al 100%. Quando qualcuno afferma che qualcosa è al 100%, significa che non vi è certezza di fallimento. Sappiamo che le persone possono facilmente deanonimizzarsi in numerosi modi, es.:

    - Riutilizzo di informazioni personali, es. (profili email, pseudonimi univoci, etc.), accessibili senza software di anonimato (Tor, VPN, etc.)
    - [Browser fingerprinting](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**Miglior Caso:**

- Documentazione chiara e di facile lettura. Ciò include cose come la configurazione dell'A2F, client email, OpenPGP, etc.

### Funzionalità aggiuntive

Sebbene non siano strettamente necessari, esistono ulteriori fattori di comodità o privacy che abbiamo analizzato, determinando quali fornitori consigliare.
