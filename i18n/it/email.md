---
meta_title: "Email Private Crittografate Consigliate - Privacy Guides"
title: "Servizi Email"
icon: material/email
description: Questi fornitori di email offrono un luogo ideale per memorizzare in sicurezza le tue email e, molti, offrono crittografia OpenPGP interoperabile con altri fornitori.
cover: email.webp
global:
  - 
    - randomize-element
    - "tabella tbody"
---

<small>Protects against the following threat(s):</small>

- [:material-server-network: Fornitori di Servizi](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

L'email è praticamente una necessità per utilizzare qualsiasi servizio online, tuttavia, la sconsigliamo per le conversazioni personali. Piuttosto che utilizzare l'email per contattare altre persone, considera di utilizzare un mezzo di messaggistica istantanea che supporti la Forward Secrecy, letteralmente, Segretezza in avanti.

[Messaggistica istantanea consigliata](real-time-communication.md ""){.md-button}

## Fornitori consigliati

Per tutto il resto, consigliamo una varietà di provider di posta elettronica basati su modelli di business sostenibile e funzioni di sicurezza integrate. Leggi il nostro [elenco completo di criteri](#criteria) per ulteriori informazioni.

| Provider                    | OpenPGP / WKD                          | IMAP / SMTP                                                | Crittografia a conoscenza zero                       | Pagamenti anonimi                        |
| --------------------------- | -------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------- | ---------------------------------------- |
| [Proton Mail](#proton-mail) | :material-check:{ .pg-green }          | :material-information-outline:{ .pg-blue } Solo a pgamento | :material-check:{ .pg-green }                        | Contanti                                 |
| [Mailbox.org](#mailboxorg)  | :material-check:{ .pg-green }          | :material-check:{ .pg-green }                              | :material-information-outline:{ .pg-blue } Solo mail | Contanti                                 |
| [Tuta](#tuta)               | :material-alert-outline:{ .pg-orange } | :material-alert-outline:{ .pg-orange }                     | :material-check:{ .pg-green }                        | Monero & Contanti attraverso terze parti |

Oltre a (o al posto di) un provider di posta elettronica consigliato qui, potreste prendere in considerazione un [servizio di aliasing e-mail](email-aliasing.md) dedicato per proteggere la vostra privacy. Tra le altre cose, questi servizi possono aiutare a proteggere la vostra casella di posta reale dallo spam, a impedire ai marketer di correlare i vostri account e a criptare tutti i messaggi in arrivo con PGP.

- [Maggiori informazioni :material-arrow-right-drop-circle:](email-aliasing.md)

## Servizi compatibili con OpenPGP

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

**Proton Mail** è un servizio di posta elettronica incentrato su privacy, crittografia, sicurezza e facilità d'uso. They have been in operation since 2013. Proton AG is based in Geneva, Switzerland. The Proton Mail Free plan comes with 500 MB of Mail storage, which you can increase up to 1 GB for free.

[:octicons-home-16: Homepage](https://proton.me/mail){ .md-button .md-button--primary }
[:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://proton.me/mail/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://proton.me/support/mail){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/android-mail/releases)
- [:fontawesome-brands-windows: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: Web](https://mail.proton.me)

</details>

</div>

Gli account gratuiti presentano delle limitazioni, come l'incapacità di cercare il testo del corpo e l'assenza dell'accesso a [Proton Mail Bridge](https://proton.me/mail/bridge), necessario per utilizzare un [client email desktop consigliato](email-clients.md) (come Thunderbird). I profili a pagamento includono funzionalità come Proton Mail Bridge, archiviazione aggiuntiva e supporto ai domini personalizzati. Una [lettera di attestazione](https://proton.me/blog/security-audit-all-proton-apps) è stata fornita per le applicazioni di Proton Mail il 9 novembre 2021 da [Securitum](https://research.securitum.com).

If you have the Proton Unlimited plan or any multi-user Proton plan, you also get [SimpleLogin](email-aliasing.md#simplelogin) Premium for free.

Proton Mail ha dei rapporti sugli arresti anomali interni che **non** sono condivisi con terze parti. Questa funzione può essere disattivata nell'applicazione web: :gear: → **Tutte le impostazioni** → **Account** → **Sicurezza e privacy** → **Privacy e raccolta dati**.

#### :material-check:{ .pg-green } Domini e Alias Personalizzati

Gli abbonati a Proton Mail a pagamento possono utilizzare il proprio dominio con il servizio o un indirizzo [catch-all](https://proton.me/support/catch-all). Inoltre, Proton Mail supporta il [sub-addressing](https://proton.me/support/creating-aliases), utile per chi non desidera acquistare un dominio.

#### :material-check:{ .pg-green } Metodi di pagamento privati

Proton Mail [accetta](https://proton.me/support/payment-options) contanti per posta, oltre ai normali pagamenti con carta di credito/debito, [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc) e PayPal.

#### :material-check:{ .pg-green } Sicurezza dell'account

Proton Mail supports TOTP [two-factor authentication](https://proton.me/support/two-factor-authentication-2fa) and [hardware security keys](https://proton.me/support/2fa-security-key) using FIDO2 or U2F standards. The use of a hardware security key requires setting up TOTP two-factor authentication first.

#### :material-check:{ .pg-green } Sicurezza dei dati

Proton Mail presenta una [crittografia ad accesso zero](https://proton.me/blog/zero-access-encryption) a riposo, per le tue email e i tuoi [calendari](https://proton.me/news/protoncalendar-security-model). I dati protetti con la crittografia ad accesso zero sono accessibili soltanto da te.

Certe informazioni memorizzate su [Proton Contact](https://proton.me/support/proton-contacts), come i nomi visualizzati e gli indirizzi email, non sono protette da tale crittografia. I campi di contatto che supportano la crittografia ad accesso zero, come i numeri di telefono, sono indicati con l'icona di un lucchetto.

#### :material-check:{ .pg-green } Crittografia Email

Proton Mail ha una [crittografia OpenPGP integrata](https://proton.me/support/how-to-use-pgp) nella propria webmail. Le e-mail inviate ad altri account Proton Mail vengono crittografate automaticamente, e la crittografia verso indirizzi non Proton Mail con una chiave OpenPGP può essere abilitata nelle impostazioni dell'account. Proton supporta anche il rilevamento automatico di chiavi esterne con [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). Ciò significa che le e-mail inviate ad altri provider che utilizzano WKD saranno automaticamente crittografate con OpenPGP, senza dover scambiare manualmente le chiavi PGP pubbliche con i tuoi contatti. Consentono inoltre di [crittografare i messaggi inviati a indirizzi non Proton Mail senza OpenPGP](https://proton.me/support/password-protected-emails), senza la necessità di aprire un account Proton Mail.

Proton Mail pubblica anche le chiavi pubbliche degli account Proton via HTTP dal loro WKD. Ciò permette a coloro che non utilizzano Proton Mail, di trovare facilmente le chiavi OpenPGP dei profili di Proton Mail, per un'E2EE tra fornitori. Questo vale solo per gli indirizzi e-mail che terminano con uno dei domini di proprietà di Proton, come @proton.me. Se si utilizza un dominio personalizzato, è necessario [configurare il WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separatamente.

#### :material-information-outline:{ .pg-blue } Chiusura dell'account

Se hai un account a pagamento e il tuo [abbonamento non viene pagato](https://proton.me/support/delinquency) dopo 14 giorni, non potrai accedere ai tuoi dati. Dopo 30 giorni, il tuo account sarà considerato moroso e non riceverà la posta in arrivo. Durante questo periodo, continuerai a essere addebitato. Proton cancellerà gli [account gratuiti](https://proton.me/support/inactive-accounts) dopo un anno di inattività. **Non** è possibile riutilizzare l'indirizzo e-mail di un account disattivato.

#### :material-information-outline:{ .pg-blue } Funzionalità aggiuntive

Proton Mail's [Unlimited](https://proton.me/support/proton-plans#proton-unlimited) plan also enables access to other Proton services in addition to providing multiple custom domains, unlimited hide-my-email aliases, and 500 GB of storage.

Proton Mail non offre una funzionalità di eredità digitale.

### Mailbox.org

<div class="admonition recommendation" markdown>

![Logo di Mailbox.org](assets/img/email/mailboxorg.svg){ align=right }

**Mailbox.org** è un servizio email incentrato sull'essere sicuro, privo di pubblicità e alimentato privatamente da energia ecologica al 100%. Sono operativi dal 2014. Mailbox.org ha sede a Berlino, in Germania. Accounts start with up to 2 GB storage, which can be upgraded as needed.

[:octicons-home-16: Homepage](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title="Documentation" }

<details class="downloads" markdown>
<summary>Scarica</summary>

- [:octicons-browser-16: Web](https://login.mailbox.org)

</details>

</div>

#### :material-check:{ .pg-green } Domini e Alias personalizzati

Mailbox.org consente di utilizzare il proprio dominio e supporta gli indirizzi di tipo [catch-all](https://kb.mailbox.org/en/private/custom-domains/how-to-set-up-a-catch-all-alias-with-a-custom-domain-name). Mailbox.org supporta anche il [sub-addressing](https://kb.mailbox.org/en/private/account-article/what-is-an-alias-and-how-do-i-use-it), utile se non si vuole acquistare un dominio.

#### :material-check:{ .pg-green } Metodi di pagamento privati

Mailbox.org non accetta criptovalute a causa della sospensione delle attività del suo elaboratore di pagamenti BitPay, in Germania. However, they do accept cash by mail, cash payment to bank account, bank transfer, credit card, PayPal and a couple of German-specific processors: paydirekt and Sofortüberweisung.

#### :material-check:{ .pg-green } Sicurezza dell'account

Mailbox.org supports [two-factor authentication](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa) for their webmail only. È possibile utilizzare TOTP o una [YubiKey](https://en.wikipedia.org/wiki/YubiKey) tramite [YubiCloud](https://yubico.com/products/services-software/yubicloud). Gli standard Web come [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn) non sono ancora supportati.

#### :material-information-outline:{ .pg-blue } Sicurezza dei dati

Mailbox.org consente la crittografia della posta in arrivo utilizzando la sua [casella di posta crittografata](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox). I nuovi messaggi ricevuti, saranno immediatamente crittografati con la tua chiave pubblica.

Tuttavia, [Open-Exchange](https://en.wikipedia.org/wiki/Open-Xchange), la piattaforma software utilizzata da Mailbox.org, [non supporta](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book) la crittografia della rubrica e del calendario. Un'[opzione indipendente](calendar.md) può essere più appropriata per tali informazioni.

#### :material-check:{ .pg-green } Crittografia Email

Mailbox.org ha la [crittografia integrata](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard) nella sua webmail, il che semplifica l'invio di messaggi a persone con chiavi OpenPGP pubbliche. Inoltre, consentono ai [destinatari di decifrare un'e-mail](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp) sui server di Mailbox.org. Questa funzionalità è utile quando il destinatario da remoto non ha OpenPGP e non può decrittografare una copia dell'email nella propria casella.

Inoltre, Mailbox.org supporta la scoperta di chiavi pubbliche tramite HTTP dalla loro [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD). Questo permette a persone esterne a Mailbox.org di trovare facilmente le chiavi OpenPGP degli account di Mailbox.org, per un E2EE fra provider diversi. Questo vale solo per gli indirizzi e-mail che terminano con uno dei domini di Mailbox.org, come @mailbox.org. Se si utilizza un dominio personalizzato, è necessario [configurare il WKD](./basics/email-security.md#what-is-the-web-key-directory-standard) separatamente.

#### :material-information-outline:{ .pg-blue } Chiusura dell'account

Alla scadenza del contratto, l'account sarà impostato come account utente limitato. Verrà irrevocabilmente eliminato dopo [30 giorni](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } Funzionalità aggiuntive

È possibile accedere al proprio account Mailbox.org tramite IMAP/SMTP utilizzando il [ servizio .onion](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org). However, their webmail interface cannot be accessed via their .onion service, and you may experience TLS certificate errors.

Tutti gli account sono dotati di uno spazio di archiviazione cloud limitato che [può essere crittografato](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive). Mailbox.org offre anche l'alias [@secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely), che applica la crittografia TLS alla connessione tra i server di posta, altrimenti il messaggio non verrà inviato affatto. Mailbox.org supporta anche [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync), oltre ai protocolli di accesso standard come IMAP e POP3.

Mailbox.org dispone di una funzione di eredità digitale per tutti i piani. Puoi scegliere se desideri che i tuoi dati siano passati agli eredi, supponendo che lo richiedano e forniscano il tuo testamento. In alternativa, puoi nominare una persona per nome e indirizzo.

## Altri fornitori

Questi fornitori memorizzano le tue email con la crittografia a conoscenza zero, rendendoli ottime opzioni per mantenere protette le tue email memorizzate. Tuttavia, non supportano standard di crittografia interoperabili per le comunicazioni E2EE tra fornitori diversi.

<div class="grid cards" markdown>

- ![Logo di Tuta](assets/img/email/tuta.svg#only-light){ .twemoji loading=lazy }![Logo di Tuta](assets/img/email/tuta-dark.svg#only-dark){ .twemoji loading=lazy } [Tuta](email.md#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Tuta logo](assets/img/email/tuta.svg#only-light){ align=right }
![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ align=right }

**Tuta** (formerly *Tutanota*) is an email service with a focus on security and privacy through the use of encryption. Tuta has been in operation since 2011 and is based in Hanover, Germany. Free accounts start with 1 GB of storage.

[:octicons-home-16: Homepage](https://tuta.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tuta.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://tuta.com/support){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="Source Code" }
[:octicons-heart-16:](https://tuta.com/community){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
- [:simple-appstore: App Store](https://apps.apple.com/app/id922429609)
- [:simple-github: GitHub](https://github.com/tutao/tutanota/releases)
- [:fontawesome-brands-windows: Windows](https://tuta.com/#download)
- [:simple-apple: macOS](https://tuta.com/#download)
- [:simple-linux: Linux](https://tuta.com/#download)
- [:octicons-browser-16: Web](https://app.tuta.com)

</details>

</div>

Tuta non supporta il [protocollo IMAP](https://tuta.com/support#imap) o l'uso di [client di posta elettronica](email-clients.md) di terze parti, e non potrai nemmeno aggiungere [account email esterni](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) all'app Tuta. Anche [l'importazione delle email](https://github.com/tutao/tutanota/issues/630) non è attualmente supportata, anche se la situazione è [destinata a cambiare](https://tuta.com/blog/kickoff-import). Le email possono essere esportate [singolarmente o tramite selezione multipla](https://tuta.com/support#generalMail) per cartella, il che può risultare scomodo se si hanno molte cartelle.

#### :material-check:{ .pg-green } Domini e Alias personalizzati

Gli account Tuta a pagamento possono utilizzare 15 o 30 alias a seconda del piano e alias illimitati su [domini personalizzati](https://tuta.com/support#custom-domain). Tuta non consente l'uso di [sub-addressing (indirizzi aggiuntivi)](https://tuta.com/support#plus), ma è possibile utilizzare [catch-all](https://tuta.com/support#settings-global) con un dominio personalizzato.

#### :material-information-outline:{ .pg-blue } Metodi di pagamento privati

Tuta only directly accepts credit cards and PayPal, however [cryptocurrency](cryptocurrency.md) can be used to purchase gift cards via their [partnership](https://tuta.com/support/#cryptocurrency) with ProxyStore.

#### :material-check:{ .pg-green } Sicurezza dell'account

Tuta supports [two-factor authentication](https://tuta.com/support#2fa) with either TOTP or U2F.

#### :material-check:{ .pg-green } Sicurezza dei dati

Tuta dispone di una [crittografia ad accesso zero a riposo](https://tuta.com/support#what-encrypted) per le e-mail, i [contatti della rubrica](https://tuta.com/support#encrypted-address-book) e i [calendari](https://tuta.com/support#calendar). Ciò significa che messaggi e altri dati memorizzati nel tuo profilo, sono leggibili soltanto da te.

#### :material-information-outline:{ .pg-blue } Crittografia Email

Tuta [non utilizza OpenPGP](https://tuta.com/support/#pgp). Gli account Tuta possono ricevere email criptate da account email non Tuta solo se inviate tramite una [casella di posta Tuta temporanea](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } Chiusura dell'account

Tuta cancellerà gli  [account gratuiti](https://tuta.com/support#inactive-accounts) dopo sei mesi di inattività. Puoi riutilizzare un profilo gratuito disattivato, previo pagamento.

#### :material-information-outline:{ .pg-blue } Funzionalità aggiuntive

Tuta offre la versione business di [Tuta alle organizzazioni non profit](https://tuta.com/blog/secure-email-for-non-profit) gratuitamente o con un enorme sconto.

Tuta non offre una funzionalità di eredità digitale.

## Auto-Hosting Email

Gli amministratori di sistema avanzati potrebbero considerare la configurazione del proprio server email. I server email richiedono attenzione e manutenzione continua, per mantenere tutto in sicurezza e la consegna delle email affidabile. In addition to the "all-in-one" solutions below, we've picked out a few articles that cover a more manual approach:

- [Configurazione di un server di posta con OpenSMTPD, Dovecot e Rspamd](https://poolp.org/posts/2019-09-14/setting-up-a-mail-server-with-opensmtpd-dovecot-and-rspamd) (2019)
- [How To Run Your Own Mail Server](https://www.c0ffee.net/blog/mail-server-guide) (August 2017)

### Stalwart

<div class="admonition recommendation" markdown>

![Stalwart logo](assets/img/email/stalwart.svg){ align=right }

**Stalwart** is a newer mail server written in Rust which supports JMAP in addition to the standard IMAP, POP3, and SMTP. It has a wide variety of configuration options, but it also defaults to very reasonable settings (in terms of both security and features) making it easy to use immediately. It has web-based administration with TOTP 2FA support, and it allows you to enter your public PGP key to encrypt **all** incoming messages.

[:octicons-home-16: Homepage](https://stalw.art){ .md-button .md-button--primary }
[:octicons-info-16:](https://stalw.art/docs/get-started){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/stalwartlabs){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/sponsors/stalwartlabs){ .card-link title="Contribute" }

</div>

Stalwart's [PGP implementation](https://stalw.art/docs/encryption/overview) is unique among our self-hosted recommendations, and allows you to operate your own mail server with zero-knowledge message storage. If you additionally configure Web Key Directory on your domain, and if you use an email client which supports PGP and Web Key Directory for outgoing mail (like Thunderbird), then this is the easiest way to get self-hosted E2EE compatibility with all [Proton Mail](#proton-mail) users.

Stalwart does **not** have an integrated webmail, so you will need to use it with a [dedicated email client](email-clients.md) (or find an open-source webmail to self-host, like Nextcloud's Mail app). We use Stalwart for our own internal email at *Privacy Guides*.

### Mailcow

<div class="admonition recommendation" markdown>

![Logo di Mailcow](assets/img/email/mailcow.svg){ align=right }

**Mailcow** è un server email più avanzato, perfetto per chi ha un po' più d'esperienza con Linux. It has everything you need in a Docker container: a mail server with DKIM support, antivirus and spam monitoring, webmail and ActiveSync with SOGo, and web-based administration with 2FA support.

[:octicons-home-16: Homepage](https://mailcow.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.mailcow.email){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/mailcow/mailcow-dockerized){ .card-link title="Source Code" }
[:octicons-heart-16:](https://servercow.de/mailcow?lang=en#sal){ .card-link title="Contribute" }

</div>

### Mail-in-a-Box

<div class="admonition recommendation" markdown>

![Logo di Mail-in-a-Box](assets/img/email/mail-in-a-box.svg){ align=right }

**Mail-in-a-Box** è uno script di configurazione automatica per la distribuzione di un server email su Ubuntu. Il suo obiettivo è semplificare la configurazione del proprio server email alle persone.

[:octicons-home-16: Homepage](https://mailinabox.email){ .md-button .md-button--primary }
[:octicons-info-16:](https://mailinabox.email/guide.html){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/mail-in-a-box/mailinabox){ .card-link title="Source Code" }

</div>

## Criteri

**Si noti che non siamo affiliati a nessuno dei provider che raccomandiamo.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie di requisiti chiari per qualsiasi provider di posta elettronica che desideri essere raccomandato, tra cui l'implementazione delle migliori pratiche del settore, tecnologia moderna e altro ancora. Vi suggeriamo di familiarizzare con questo elenco prima di scegliere un provider di posta elettronica e di condurre le vostre ricerche per assicurarvi che il provider scelto sia la scelta giusta per voi.

### Tecnologia

Consideriamo queste funzionalità come importanti per poter fornire un servizio sicuro e ottimale. Dovresti considerare se il fornitore ha le funzionalità di cui necessiti.

**Requisiti minimi:**

- Crittografia dei dati degli account email a riposo con crittografia ad "accesso zero".
- Export capability as [Mbox](https://en.wikipedia.org/wiki/Mbox) or individual .EML with [RFC5322](https://datatracker.ietf.org/doc/rfc5322) standard.
- Opera su un'infrastruttura proprietaria, cioè, non basata su fornitori del servizio email di terze parti.

**Miglior Caso:**

- Crittografa tutti i dati del profilo (Contatti, Calendari, ecc.) a riposo con crittografia ad accesso zero.
- Crittografia E2EE/PGP della webmail integrata, fornita per comodità.
- Supporto per [WKD](https://wiki.gnupg.org/WKD) per consentire la scoperta migliorata delle chiavi pubbliche di OpenPGP tramite HTTP. Gli utenti di GnuPG possono ottenere una chiave digitando: `gpg --locate-key example_user@example.com`
- Supporto per una casella temporanea per gli utenti esterni. Questo è utile quando desideri inviare un'email crittografata, senza inviare una copia effettiva al tuo destinatario. Queste email, solitamente, hanno una durata limitata, prima di essere eliminate automaticamente. Inoltre, non richiedono al destinatario di configurare alcuna crittografia, come OpenPGP.
- Disponibilità dei servizi del fornitore email tramite un [servizio onion](https://en.wikipedia.org/wiki/.onion).
- Supporto per il [sub-addressing](https://en.wikipedia.org/wiki/Email_address#Sub-addressing).
- Allows users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). I nomi di dominio personalizzati sono importanti per gli utenti, poiché consentono loro di mantenere la propria autonomia dal servizio, dovesse diventare negativo o essere acquisito da un'altra azienda che non dà priorità alla privacy.
- Catch-all or alias functionality for those who use their own domains.
- Use of standard email access protocols such as IMAP, SMTP, or [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Standard access protocols ensure customers can easily download all of their email, should they want to switch to another provider.

### Privacy

Preferiamo che i fornitori consigliati raccolgano il minor numero di dati possibile.

**Requisiti minimi:**

- Protect sender's IP address, which can involve filtering it from showing in the `Received` header field.
- Non richiedere informazioni d'identificazione personale (PII), tranne un nome utente e una password.
- Politica sulla privacy che soddisfi i requisiti definiti dal GDPR.

**Caso migliore:**

- Accetta [opzioni di pagamento anonime](advanced/payments.md) ([criptovalute](cryptocurrency.md), contanti, carte regalo, etc.)
- Ospitato in una giurisdizione con forti regolamentazioni sulla protezione della privacy email.

### Sicurezza

I server email gestiscono molti dati, estremamente sensibili. We expect that providers will adopt best industry practices in order to protect their customers.

**Requisiti minimi:**

- Protezione della webmail con 2FA, ad esempio TOTP.
- Zero access encryption, which builds on encryption at rest. Il provider non deve disporre delle chiavi di decrittazione dei dati in loro possesso. Questo previene che dipendenti disonesti possano trapelare i dati sensibili, o che un avversario remoto possa rilasciarli, dopo averli rubati, ottenendo un accesso non autorizzato al server.
- Supporto [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions).
- Nessun errore o vulnerabilità TLS quando si viene profilato da strumenti come [Hardenize](https://hardenize.com), [testssl.sh](https://testssl.sh) o [Qualys SSL Labs](https://ssllabs.com/ssltest); questo include errori relativi ai certificati e parametri DH deboli, come quelli che hanno portato a [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- Una preferenza della suite del server (facoltativa su TLSv1.3), per forti suite di cifratura che supportino la segretezza in avanti e la crittografia autenticata.
- Una valida politica [MTA-STS](https://tools.ietf.org/html/rfc8461) e [TLS-RPT](https://tools.ietf.org/html/rfc8460).
- Registri [DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities) validi.
- Registri [SPF](https://en.wikipedia.org/wiki/Sender_Policy_Framework) e [DKIM](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail) validi.
- Disporre di un registro o una politica [DMARC](https://en.wikipedia.org/wiki/DMARC) adeguati o utilizzare [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) per l'autenticazione. Se si utilizza l'autenticazione DMARC, la politica dev'essere impostata su `rifiuta` o `quarantena`.
- Preferenza per una suite di server TLS 1.2 o successiva e un piano per [RFC8996](https://datatracker.ietf.org/doc/rfc8996).
- Invio [SMTPS](https://en.wikipedia.org/wiki/SMTPS), supponendo che SMTP sia utilizzato.
- Standard di sicurezza del sito web come:
    - [HTTP Strict Transport Security](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - [Integrità Subresource](https://en.wikipedia.org/wiki/Subresource_Integrity) se si caricano oggetti da domini esterni.
- Must support viewing of [message headers](https://en.wikipedia.org/wiki/Email#Message_header), as it is a crucial forensic feature to determine if an email is a phishing attempt.

**Miglior Caso:**

- Supporto all'autenticazione hardware, cioè U2F and [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online).
- [Registro Risorse di Autorizzazione dell'Autorità del Certificato (CAA) DNS](https://tools.ietf.org/html/rfc6844), oltre al supporto DANE.
- Implementation of [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), which is useful for people who post to mailing lists [RFC8617](https://tools.ietf.org/html/rfc8617).
- Controlli di sicurezza pubblicati da uno studio di terze parti affidabile.
- Programmi di caccia ai bug e/o un processo di divulgazione delle vulnerabilità coordinato.
- Standard di sicurezza del sito web, quali:
    - [Politica sulla Sicurezza dei Contenuti (CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### Fiducia

Non affideresti le tue finanze a qualcuno con un'identità falsa, quindi, perché affidare loro la tua email? Richiediamo ai nostri fornitori fidati di essere pubblici sulla propria proprietà o dirigenza. Inoltre, vorremmo vedere rapporti di trasparenza frequenti, specialmente relativi alla gestione delle richieste del governo.

**Requisiti minimi:**

- Dirigenza o proprietà rivolta al pubblico.

**Miglior Caso:**

- Rapporti di trasparenza frequenti.

### Marketing

With the email providers we recommend, we like to see responsible marketing.

**Requisiti minimi:**

- Must self-host analytics (no Google Analytics, Adobe Analytics, etc.).

Must not have any irresponsible marketing, which can include the following:

- Dichiarazioni di "crittografia impenetrabile." La crittografia dovrebbe essere utilizzata con l'intenzione che possa non essere segreta in futuro, quando esisterà la tecnologia per decifrarla.
- Garantire la protezione dell'anonimato al 100%. Quando qualcuno afferma che qualcosa è al 100%, significa che non vi è certezza di fallimento. We know people can quite easily de-anonymize themselves in a number of ways, e.g.:

    - Riutilizzo di informazioni personali, es. (profili email, pseudonimi univoci, etc.), accessibili senza software di anonimato (Tor, VPN, etc.)
    - [Browser fingerprinting](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**Caso migliore:**

- Clear and easy to read documentation for tasks like setting up 2FA, email clients, OpenPGP, etc.

### Funzionalità aggiuntive

Sebbene non siano strettamente necessari, esistono ulteriori fattori di comodità o privacy che abbiamo analizzato, determinando quali fornitori consigliare.
