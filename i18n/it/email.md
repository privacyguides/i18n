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
- [Opzioni Self-Hosted :material-arrow-right-drop-circle:](#self-hosting-email)

In addition to (or instead of) an email provider recommended here, you may wish to consider a dedicated [email aliasing service](email-aliasing.md) to protect your privacy. Among other things, these services can help protect your real inbox from spam, prevent marketers from correlating your accounts, and encrypt all incoming messages with PGP.

- [More Information :material-arrow-right-drop-circle:](email-aliasing.md)

## Servizi Compatibili con OpenPGP

Questi provider supportano in modo nativo la crittografia/decrittografia OpenPGP e lo [standard Web Key Directory](basics/email-security.md#what-is-the-web-key-directory-standard), consentendo la creazione di e-mail E2EE indipendenti dal provider. Ad esempio, un utente di Proton Mail potrebbe inviare un messaggio E2EE a un utente Mailbox.org, o potresti ricevere notifiche crittografate in OpenPGP dai servizi Internet che le supportano.

<div class="grid cards" markdown>

- ![Logo Proton Mail](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![Logo Mailbox.org](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

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
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id979659905)
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

Gli abbonati a Proton Mail a pagamento possono utilizzare il proprio dominio con il servizio o un indirizzo [catch-all](https://proton.me/support/catch-all). Proton Mail also supports [sub-addressing](https://proton.me/support/creating-aliases), which is useful for people who don't want to purchase a domain.

#### :material-check:{ .pg-green } Metodi di pagamento privati

Proton Mail [accetta](https://proton.me/support/payment-options) contanti per posta, oltre ai normali pagamenti con carta di credito/debito, [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc) e PayPal.

#### :material-check:{ .pg-green } Sicurezza dell'account

Proton Mail supporta l'[autenticazione a due fattori](https://proton.me/support/two-factor-authentication-2fa) TOTP e le [chiavi di sicurezza hardware](https://proton.me/support/2fa-security-key), utilizzando gli standard FIDO2 o U2F. L'utilizzo di una chiave di sicurezza hardware richiede la configurazione precedente dell'autenticazione a due fattori TOTP.

#### :material-check:{ .pg-green } Sicurezza dei dati

Proton Mail presenta una [crittografia ad accesso zero](https://proton.me/blog/zero-access-encryption) a riposo, per le tue email e i tuoi [calendari](https://proton.me/news/protoncalendar-security-model). I dati protetti con la crittografia ad accesso zero sono accessibili soltanto da te.

Certe informazioni memorizzate su [Proton Contact](https://proton.me/support/proton-contacts), come i nomi visualizzati e gli indirizzi email, non sono protette da tale crittografia. I campi di contatto che supportano la crittografia ad accesso zero, come i numeri di telefono, sono indicati con l'icona di un lucchetto.

#### :material-check:{ .pg-green } Crittografia Email

Proton Mail ha una [crittografia OpenPGP integrata](https://proton.me/support/how-to-use-pgp) nella propria webmail. Le e-mail inviate ad altri account Proton Mail vengono crittografate automaticamente, e la crittografia verso indirizzi non Proton Mail con una chiave OpenPGP può essere abilitata nelle impostazioni dell'account. Proton supporta anche il rilevamento automatico di chiavi esterne con [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). Ciò significa che le e-mail inviate ad altri provider che utilizzano WKD saranno automaticamente crittografate con OpenPGP, senza dover scambiare manualmente le chiavi PGP pubbliche con i tuoi contatti. Consentono inoltre di [crittografare i messaggi inviati a indirizzi non Proton Mail senza OpenPGP](https://proton.me/support/password-protected-emails), senza la necessità di aprire un account Proton Mail.

Proton Mail pubblica anche le chiavi pubbliche degli account Proton via HTTP dal loro WKD. Ciò permette a coloro che non utilizzano Proton Mail, di trovare facilmente le chiavi OpenPGP dei profili di Proton Mail, per un'E2EE tra fornitori. Questo vale solo per gli indirizzi e-mail che terminano con uno dei domini di proprietà di Proton, come @proton.me. Se si utilizza un dominio personalizzato, è necessario [configurare il WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separatamente.

#### :material-information-outline:{ .pg-blue } Chiusura dell'account

Se hai un account a pagamento e il tuo [abbonamento non viene pagato](https://proton.me/support/delinquency) dopo 14 giorni, non potrai accedere ai tuoi dati. Dopo 30 giorni, il tuo account sarà considerato moroso e non riceverà la posta in arrivo. Durante questo periodo, continuerai a essere addebitato.

#### :material-information-outline:{ .pg-blue } Funzionalità aggiuntive

Proton Mail offre un profilo "Unlimited" per €9,99/Mese, che consente inoltre l'accesso a Proton VPN, oltre a fornire multipli profili, domini, alias e 500GB di archiviazione.

Proton Mail non offre una funzionalità di eredità digitale.

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

Mailbox.org lets you use your own domain, and they support [catch-all](https://kb.mailbox.org/en/private/custom-domains/how-to-set-up-a-catch-all-alias-with-a-custom-domain-name) addresses. Mailbox.org also supports [sub-addressing](https://kb.mailbox.org/en/private/account-article/what-is-an-alias-and-how-do-i-use-it), which is useful if you don't want to purchase a domain.

#### :material-check:{ .pg-green } Metodi di pagamento privati

Mailbox.org non accetta criptovalute a causa della sospensione delle attività del suo elaboratore di pagamenti BitPay, in Germania. Tuttavia, accettano contanti per posta, pagamento in contanti su conto corrente, bonifico bancario, carta di credito, PayPal e un paio di processori specifici per la Germania: paydirekt e Sofortüberweisung.

#### :material-check:{ .pg-green } Sicurezza dell'account

Mailbox.org supports [two factor authentication](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa) for their webmail only. You can use either TOTP or a [YubiKey](https://en.wikipedia.org/wiki/YubiKey) via the [YubiCloud](https://yubico.com/products/services-software/yubicloud). Gli standard Web come [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn) non sono ancora supportati.

#### :material-information-outline:{ .pg-blue } Sicurezza dei dati

Mailbox.org allows for encryption of incoming mail using their [encrypted mailbox](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox). I nuovi messaggi ricevuti, saranno immediatamente crittografati con la tua chiave pubblica.

However, [Open-Exchange](https://en.wikipedia.org/wiki/Open-Xchange), the software platform used by Mailbox.org, [does not support](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book) the encryption of your address book and calendar. Un'[opzione indipendente](calendar.md) può essere più appropriata per tali informazioni.

#### :material-check:{ .pg-green } Crittografia Email

Mailbox.org has [integrated encryption](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard) in their webmail, which simplifies sending messages to people with public OpenPGP keys. They also allow [remote recipients to decrypt an email](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp) on Mailbox.org's servers. Questa funzionalità è utile quando il destinatario da remoto non ha OpenPGP e non può decrittografare una copia dell'email nella propria casella.

Inoltre, Mailbox.org supporta la scoperta di chiavi pubbliche tramite HTTP dalla loro [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). Questo permette a persone esterne a Mailbox.org di trovare facilmente le chiavi OpenPGP degli account di Mailbox.org, per un E2EE fra provider diversi. Questo vale solo per gli indirizzi e-mail che terminano con uno dei domini di Mailbox.org, come @mailbox.org. Se si utilizza un dominio personalizzato, è necessario [configurare il WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separatamente.

#### :material-information-outline:{ .pg-blue } Chiusura dell'account

Il tuo profilo sarà impostato come limitato al termine del tuo contratto; dopo [30 giorni sarà irrevocabilmente eliminato](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } Funzionalità aggiuntive

You can access your Mailbox.org account via IMAP/SMTP using their [.onion service](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org). Tuttavia, l'interfaccia webmail non è accessibile tramite il loro servizio .onion e potresti riscontrare errori del certificato TLS.

All accounts come with limited cloud storage that [can be encrypted](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive). Mailbox.org also offers the alias [@secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely), which enforces the TLS encryption on the connection between mail servers, otherwise the message will not be sent at all. Mailbox.org supporta anche [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync), oltre ai protocolli di accesso standard come IMAP e POP3.

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

[:octicons-home-16: Homepage](https://tuta.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tuta.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://tuta.com/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="Source Code" }
[:octicons-heart-16:](https://tuta.com/community){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
- [:simple-appstore: App Store](https://apps.apple.com/app/id922429609)
- [:simple-github: GitHub](https://github.com/tutao/tutanota/releases)
- [:simple-windows11: Windows](https://tuta.com/#download)
- [:simple-apple: macOS](https://tuta.com/#download)
- [:simple-linux: Linux](https://tuta.com/#download)
- [:octicons-browser-16: Web](https://app.tuta.com)

</details>

</div>

Tuta non supporta il [protocollo IMAP](https://tuta.com/faq/#imap) o l'utilizzo di [client email](email-clients.md) di terze parti e, inoltre, non potrai aggiungere [account email esterni](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) all'app di Tuta. [L'importazione di email](https://github.com/tutao/tutanota/issues/630) non è attualmente supportata, anche se questo aspetto è destinato ad [essere modificato](https://tuta.com/blog/posts/kickoff-import). Le email possono essere esportate [singolarmente o tramite selezione in blocco](https://tuta.com/howto#generalMail) per cartella, il che può risultare scomodo se hai molte cartelle.

#### :material-check:{ .pg-green } Domini e Alias personalizzati

Gli account di Tuta a pagamento possono utilizzare 15 o 30 alias a seconda del piano e alias illimitati sui [domini personalizzati](https://tuta.com/faq#custom-domain). Tuta doesn't allow for [sub-addressing (plus addresses)](https://tuta.com/faq#plus), but you can use a [catch-all](https://tuta.com/howto#settings-global) with a custom domain.

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

Tuta also has a business feature called [Secure Connect](https://tuta.com/secure-connect). Questa, garantisce che il contatto del cliente con l'azienda utilizzi l'E2EE. La funzionalità costa €240 all'anno.

Tuta non offre una funzionalità di eredità digitale.

## Auto-Hosting Email

Gli amministratori di sistema avanzati potrebbero considerare la configurazione del proprio server email. I server email richiedono attenzione e manutenzione continua, per mantenere tutto in sicurezza e la consegna delle email affidabile.

### Soluzioni software combinate

<div class="admonition recommendation" markdown>

![Logo di Mailcow](assets/img/email/mailcow.svg){ align=right }

**Mailcow** è un server email più avanzato, perfetto per chi ha un po' più d'esperienza con Linux. Ha tutto il necessario in un contenitore Docker: Un server email con supporto DKIM, antivirus e monitoraggio dello spam, webmail e ActiveSync con SOGo e amministrazione basata sul web con supporto A2F.

[:octicons-home-16: Homepage](https://mailcow.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.mailcow.email){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="Source Code" }
[:octicons-heart-16:](https://servercow.de/mailcow?lang=en#sal){ .card-link title=Contribute }

</div>

<div class="admonition recommendation" markdown>

![Logo di Mail-in-a-Box](assets/img/email/mail-in-a-box.svg){ align=right }

**Mail-in-a-Box** è uno script di configurazione automatica per la distribuzione di un server email su Ubuntu. Il suo obiettivo è semplificare la configurazione del proprio server email alle persone.

[:octicons-home-16: Pagina Principale](https://mailinabox.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title=Documentazione}
[:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="Codice sorgente" }

</div>

Per un approccio più manuale, abbiamo scelto questi due articoli:

- [Setting up a mail server with OpenSMTPD, Dovecot and Rspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd) (2019)
- [How To Run Your Own Mail Server](https://c0ffee.net/blog/mail-server-guide) (August 2017)

## Criteri

**Si prega di notare che non siamo affiliati con alcun fornitore consigliato.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una chiara serie di requisiti per qualsiasi fornitore email che desideri essere consigliato, inclusa l'implementazione delle migliori pratiche del settore, tecnologia moderna e altro. Ti consigliamo di familiarizzare con questo elenco prima di scegliere un provider di posta elettronica e condurre le tue ricerche per assicurarti che il provider di posta elettronica che scegli sia la scelta giusta per te.

### Tecnologia

Consideriamo queste funzionalità come importanti per poter fornire un servizio sicuro e ottimale. Dovresti considerare se il fornitore ha le funzionalità di cui necessiti.

**Requisiti minimi:**

- Crittografia dei dati degli account email a riposo con crittografia ad "accesso zero".
- Export capability as [Mbox](https://en.wikipedia.org/wiki/Mbox) or individual .eml with [RFC5322](https://datatracker.ietf.org/doc/rfc5322) standard.
- Consente agli utenti di utilizzare il proprio [nome di dominio](https://en.wikipedia.org/wiki/Domain_name). I nomi di dominio personalizzati sono importanti per gli utenti, poiché consentono loro di mantenere la propria autonomia dal servizio, dovesse diventare negativo o essere acquisito da un'altra azienda che non dà priorità alla privacy.
- Opera su un'infrastruttura proprietaria, cioè, non basata su fornitori del servizio email di terze parti.

**Miglior Caso:**

- Crittografa tutti i dati del profilo (Contatti, Calendari, etc.) a riposo con crittografia ad accesso zero.
- Crittografia E2EE/PGP della webmail integrata, fornita per comodità.
- Supporto per [WKD](https://wiki.gnupg.org/WKD) per consentire la scoperta migliorata delle chiavi pubbliche di OpenPGP tramite HTTP. Gli utenti di GnuPG possono ottenere una chiave digitando: `gpg --locate-key example_user@example.com`
- Supporto per una casella temporanea per gli utenti esterni. Questo è utile quando desideri inviare un'email crittografata, senza inviare una copia effettiva al tuo destinatario. Queste email, solitamente, hanno una durata limitata, prima di essere eliminate automaticamente. Inoltre, non richiedono al destinatario di configurare alcuna crittografia, come OpenPGP.
- Disponibilità dei servizi del fornitore email tramite un [servizio onion](https://en.wikipedia.org/wiki/.onion).
- [Sub-addressing](https://en.wikipedia.org/wiki/Email_address#Sub-addressing) support.
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
- No TLS errors or vulnerabilities when being profiled by tools such as [Hardenize](https://hardenize.com), [testssl.sh](https://testssl.sh), or [Qualys SSL Labs](https://ssllabs.com/ssltest); this includes certificate related errors and weak DH parameters, such as those that led to [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- Una preferenza della suite del server (facoltativa su TLSv1.3), per forti suite di cifratura che supportino la segretezza in avanti e la crittografia autenticata.
- Una valida politica [MTA-STS](https://tools.ietf.org/html/rfc8461) e [TLS-RPT](https://tools.ietf.org/html/rfc8460).
- Registri [DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities) validi.
- Registri [SPF](https://en.wikipedia.org/wiki/Sender_Policy_Framework) e [DKIM](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail) validi.
- Disporre di un registro o una politica [DMARC](https://en.wikipedia.org/wiki/DMARC) adeguati o utilizzare [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) per l'autenticazione. Se si utilizza l'autenticazione DMARC, la politica dev'essere impostata su `rifiuta` o `quarantena`.
- A server suite preference of TLS 1.2 or later and a plan for [RFC8996](https://datatracker.ietf.org/doc/rfc8996).
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
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

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

**Caso migliore:**

- Documentazione chiara e di facile lettura. Ciò include cose come la configurazione dell'A2F, client email, OpenPGP, etc.

### Funzionalità aggiuntive

Sebbene non siano strettamente necessari, esistono ulteriori fattori di comodità o privacy che abbiamo analizzato, determinando quali fornitori consigliare.
