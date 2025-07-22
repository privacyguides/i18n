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

<small>Protegge dalle seguenti minacce:</small>

- [:material-server-network: Fornitori di Servizi](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

L'email è praticamente una necessità per utilizzare qualsiasi servizio online, tuttavia, la sconsigliamo per le conversazioni personali. Piuttosto che utilizzare l'email per contattare altre persone, considera di utilizzare un mezzo di messaggistica istantanea che supporti la Forward Secrecy, letteralmente, Segretezza in avanti.

[Messaggistica istantanea consigliata](real-time-communication.md ""){.md-button}

## Fornitori consigliati

Per tutto il resto, consigliamo una varietà di provider di posta elettronica basati su modelli di business sostenibile e funzioni di sicurezza integrate. Leggi il nostro [elenco completo di criteri](#criteria) per ulteriori informazioni.

| Provider                    | OpenPGP / WKD                          | IMAP / SMTP                                                | Crittografia ad accesso zero                         | Metodi di pagamento anonimi             |
| --------------------------- | -------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------- | --------------------------------------- |
| [Proton Mail](#proton-mail) | :material-check:{ .pg-green }          | :material-information-outline:{ .pg-blue } Solo a pgamento | :material-check:{ .pg-green }                        | Contanti                                |
| [Mailbox.org](#mailboxorg)  | :material-check:{ .pg-green }          | :material-check:{ .pg-green }                              | :material-information-outline:{ .pg-blue } Solo mail | Contanti                                |
| [Tuta](#tuta)               | :material-alert-outline:{ .pg-orange } | :material-alert-outline:{ .pg-orange }                     | :material-check:{ .pg-green }                        | Monero <br>Contanti tramite terzi |

Oltre a (o al posto di) un fornitore di posta elettronica consigliato qui, potresti prendere in considerazione un [servizio di aliasing e-mail](email-aliasing.md#recommended-providers) dedicato per proteggere la tua privacy. Tra le altre cose, questi servizi possono aiutare a proteggere la vostra casella di posta reale dallo spam, a impedire ai marketer di correlare i vostri account e a criptare tutti i messaggi in arrivo con PGP.

- [Maggiori informazioni :material-arrow-right-drop-circle:](email-aliasing.md)

## Servizi compatibili con OpenPGP

Questi fornitori supportano in modo nativo la crittografia/decrittografia OpenPGP e lo [standard Web Key Directory (WKD)](basics/email-security.md#what-is-the-web-key-directory-standard), consentendo d'inviare e-mail crittografate end-to-end indipendentemente dal fornitore scelto. Ad esempio, un utente di Proton Mail potrebbe inviare un messaggio E2EE a un utente Mailbox.org, o potresti ricevere notifiche crittografate in OpenPGP dai servizi Internet che le supportano.

<div class="grid cards" markdown>

- ![Logo Proton Mail](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](email.md#proton-mail)
- ![Logo Mailbox.org](assets/img/email/mailboxorg.svg){ .twemoji } [Mailbox.org](email.md#mailboxorg)

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avviso</p>

Quando si utilizza una tecnologia E2EE come OpenPGP, la tua e-mail presenta ancora alcuni metadati non crittografati nell'intestazione dell'e-mail, tra cui generalmente l'oggetto! Per saperne di più sui [matadati delle e-mail](basics/email-security.md#email-metadata-overview).

OpenPGP also does not support forward secrecy, which means if the private key of either you or the message recipient is ever stolen, all previous messages encrypted with it will be exposed.

- [Come proteggo le mie chiavi private?](basics/email-security.md#how-do-i-protect-my-private-keys)

</div>

### Proton Mail

<div class="admonition recommendation" markdown>

![Proton Mail logo](assets/img/email/protonmail.svg){ align=right }

**Proton Mail** è un servizio di posta elettronica incentrato su privacy, crittografia, sicurezza e facilità d'uso. They have been in operation since 2013. Proton AG is based in Geneva, Switzerland.

The Proton Free plan comes with 500 MB of Mail storage, which you can increase up to 1 GB for free.

[:octicons-home-16: Pagina Principale](https://proton.me/mail){ .md-button .md-button--primary }
[:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Servizio Onion"}
[:octicons-eye-16:](https://proton.me/mail/privacy-policy){ .card-link title="Politica sulla Privacy" }
[:octicons-info-16:](https://proton.me/support/mail){ .card-link title="Documentazione" }
[:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Codice Sorgente" }

<details class="downloads" markdown>
<summary>Download</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/android-mail/releases)
- [:fontawesome-brands-windows: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: Web](https://mail.proton.me)

</details>

</div>

Free accounts have some limitations, such as not being able to search body text and not having access to [Proton Mail Bridge](https://proton.me/mail/bridge), which is required to use a [recommended desktop email client](email-clients.md) (e.g., Thunderbird). I profili a pagamento includono funzionalità come Proton Mail Bridge, archiviazione aggiuntiva e supporto ai domini personalizzati. If you have the Proton Unlimited plan or any multi-user Proton plan, you also get [SimpleLogin](email-aliasing.md#simplelogin) Premium for free.

Una [lettera di attestazione](https://proton.me/blog/security-audit-all-proton-apps) è stata fornita per le applicazioni di Proton Mail il 9 novembre 2021 da [Securitum](https://research.securitum.com).

Proton Mail ha dei rapporti sugli arresti anomali interni che **non** sono condivisi con terze parti. Questa funzione può essere disattivata nell'applicazione web: :gear: → **Tutte le impostazioni** → **Account** → **Sicurezza e privacy** → **Privacy e raccolta dati**.

#### :material-check:{ .pg-green } Domini e Alias Personalizzati

Gli abbonati a Proton Mail a pagamento possono utilizzare il proprio dominio con il servizio o un indirizzo [catch-all](https://proton.me/support/catch-all). Inoltre, Proton Mail supporta il [sub-addressing](https://proton.me/support/creating-aliases), utile per chi non desidera acquistare un dominio.

#### :material-check:{ .pg-green } Metodi di pagamento privati

Proton Mail [accepts](https://proton.me/support/payment-options) **cash** by mail in addition to standard credit/debit card, [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), and PayPal payments.

#### :material-check:{ .pg-green } Sicurezza dell'account

Proton Mail supports TOTP [two-factor authentication](https://proton.me/support/two-factor-authentication-2fa) and [hardware security keys](https://proton.me/support/2fa-security-key) using FIDO2 or U2F standards. The use of a hardware security key requires setting up TOTP two-factor authentication first.

#### :material-check:{ .pg-green } Sicurezza dei dati

Proton Mail presenta una [crittografia ad accesso zero](https://proton.me/blog/zero-access-encryption) a riposo, per le tue email e i tuoi [calendari](https://proton.me/news/protoncalendar-security-model). I dati protetti con la crittografia ad accesso zero sono accessibili soltanto da te.

Certe informazioni memorizzate su [Proton Contact](https://proton.me/support/proton-contacts), come i nomi visualizzati e gli indirizzi email, non sono protette da tale crittografia. I campi di contatto che supportano la crittografia ad accesso zero, come i numeri di telefono, sono indicati con l'icona di un lucchetto.

#### :material-check:{ .pg-green } Crittografia Email

Proton Mail ha una [crittografia OpenPGP integrata](https://proton.me/support/how-to-use-pgp) nella propria webmail. Le e-mail inviate ad altri account Proton Mail vengono crittografate automaticamente, e la crittografia verso indirizzi non Proton Mail con una chiave OpenPGP può essere abilitata nelle impostazioni dell'account. Proton also supports automatic external key discovery with WKD. Ciò significa che le e-mail inviate ad altri provider che utilizzano WKD saranno automaticamente crittografate con OpenPGP, senza dover scambiare manualmente le chiavi PGP pubbliche con i tuoi contatti. Consentono inoltre di [crittografare i messaggi inviati a indirizzi non Proton Mail senza OpenPGP](https://proton.me/support/password-protected-emails), senza la necessità di aprire un account Proton Mail.

Proton Mail pubblica anche le chiavi pubbliche degli account Proton via HTTP dal loro WKD. This allows people who don't use Proton Mail to find the OpenPGP keys of Proton Mail accounts easily for cross-provider E2EE. This only applies to email addresses ending in one of Proton's own domains, like `@proton.me`. If you use a custom domain, you must [configure WKD](basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } Chiusura dell'account

Se hai un account a pagamento e il tuo [abbonamento non viene pagato](https://proton.me/support/delinquency) dopo 14 giorni, non potrai accedere ai tuoi dati. Dopo 30 giorni, il tuo account sarà considerato moroso e non riceverà la posta in arrivo. Durante questo periodo, continuerai a essere addebitato. Proton cancellerà gli [account gratuiti](https://proton.me/support/inactive-accounts) dopo un anno di inattività. **Non** è possibile riutilizzare l'indirizzo e-mail di un account disattivato.

#### :material-information-outline:{ .pg-blue } Funzionalità aggiuntive

Proton Mail's [Unlimited](https://proton.me/support/proton-plans#proton-unlimited) plan also enables access to other Proton services in addition to providing multiple custom domains, unlimited hide-my-email aliases, and 500 GB of storage.

### Mailbox.org

<div class="admonition recommendation" markdown>

![Mailbox.org logo](assets/img/email/mailboxorg.svg){ align=right }

**Mailbox.org** is an email service with a focus on being secure, ad-free, and powered by 100% eco-friendly energy. Sono operativi dal 2014. Mailbox.org ha sede a Berlino, in Germania.

Accounts start with up to 2 GB storage, which can be upgraded as needed.

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

Mailbox.org non accetta criptovalute a causa della sospensione delle attività del suo elaboratore di pagamenti BitPay, in Germania. However, they do accept **cash** by mail, **cash** payment to bank account, bank transfer, credit card, PayPal, and a couple of German-specific processors: Paydirekt and Sofortüberweisung.

#### :material-check:{ .pg-green } Sicurezza dell'account

Mailbox.org supports [two-factor authentication](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa) for their webmail only. È possibile utilizzare TOTP o una [YubiKey](https://en.wikipedia.org/wiki/YubiKey) tramite [YubiCloud](https://yubico.com/products/services-software/yubicloud). Web standards such as [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online) are not yet supported.

#### :material-information-outline:{ .pg-blue } Sicurezza dei dati

Mailbox.org consente la crittografia della posta in arrivo utilizzando la sua [casella di posta crittografata](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox). I nuovi messaggi ricevuti, saranno immediatamente crittografati con la tua chiave pubblica.

However, [Open-Xchange](https://en.wikipedia.org/wiki/Open-Xchange), the software platform used by Mailbox.org, [does not support](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book) the encryption of your address book and calendar. A [standalone option](calendar.md) may be more appropriate for that data.

#### :material-check:{ .pg-green } Crittografia Email

Mailbox.org ha la [crittografia integrata](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard) nella sua webmail, il che semplifica l'invio di messaggi a persone con chiavi OpenPGP pubbliche. Inoltre, consentono ai [destinatari di decifrare un'e-mail](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp) sui server di Mailbox.org. Questa funzionalità è utile quando il destinatario da remoto non ha OpenPGP e non può decrittografare una copia dell'email nella propria casella.

Mailbox.org also supports the discovery of public keys via HTTP from their WKD. This allows people outside of Mailbox.org to find the OpenPGP keys of Mailbox.org accounts easily for cross-provider E2EE. This only applies to email addresses ending in one of Mailbox.org's own domains, like `@mailbox.org`. If you use a custom domain, you must [configure WKD](basics/email-security.md#what-is-the-web-key-directory-standard) separately.

#### :material-information-outline:{ .pg-blue } Chiusura dell'account

Alla scadenza del contratto, l'account sarà impostato come account utente limitato. Verrà irrevocabilmente eliminato dopo [30 giorni](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } Funzionalità aggiuntive

È possibile accedere al proprio account Mailbox.org tramite IMAP/SMTP utilizzando il [ servizio .onion](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org). However, their webmail interface cannot be accessed via their .onion service, and you may experience TLS certificate errors.

Tutti gli account sono dotati di uno spazio di archiviazione cloud limitato che [può essere crittografato](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive). Mailbox.org offre anche l'alias [@secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely), che applica la crittografia TLS alla connessione tra i server di posta, altrimenti il messaggio non verrà inviato affatto. Mailbox.org supporta anche [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync), oltre ai protocolli di accesso standard come IMAP e POP3.

Mailbox.org dispone di una funzione di eredità digitale per tutti i piani. You can choose whether you want any of your data to be passed to heirs, providing that they apply and provide your testament. In alternativa, puoi nominare una persona per nome e indirizzo.

## Altri fornitori

Questi fornitori memorizzano le tue email con la crittografia a conoscenza zero, rendendoli ottime opzioni per mantenere protette le tue email memorizzate. Tuttavia, non supportano standard di crittografia interoperabili per le comunicazioni E2EE tra fornitori diversi.

<div class="grid cards" markdown>

- ![Logo di Tuta](assets/img/email/tuta.svg#only-light){ .twemoji loading=lazy }![Logo di Tuta](assets/img/email/tuta-dark.svg#only-dark){ .twemoji loading=lazy } [Tuta](email.md#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Tuta logo](assets/img/email/tuta.svg#only-light){ align=right }
![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ align=right }

**Tuta** (formerly *Tutanota*) is an email service with a focus on security and privacy through the use of encryption. Tuta has been in operation since 2011 and is based in Hanover, Germany.

Free accounts start with 1 GB of storage.

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

Tuta only directly accepts credit cards and PayPal, however [**cryptocurrency**](cryptocurrency.md) can be used to purchase gift cards via their [partnership](https://tuta.com/support/#cryptocurrency) with ProxyStore.

#### :material-check:{ .pg-green } Sicurezza dell'account

Tuta supports [two-factor authentication](https://tuta.com/support#2fa) with either TOTP or U2F.

#### :material-check:{ .pg-green } Sicurezza dei dati

Tuta has [zero-access encryption at rest](https://tuta.com/support#what-encrypted) for your emails, [address book contacts](https://tuta.com/support#encrypted-address-book), and [calendars](https://tuta.com/support#calendar). Ciò significa che messaggi e altri dati memorizzati nel tuo profilo, sono leggibili soltanto da te.

#### :material-information-outline:{ .pg-blue } Crittografia Email

Tuta [non utilizza OpenPGP](https://tuta.com/support/#pgp). Gli account Tuta possono ricevere email criptate da account email non Tuta solo se inviate tramite una [casella di posta Tuta temporanea](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } Chiusura dell'account

Tuta cancellerà gli  [account gratuiti](https://tuta.com/support#inactive-accounts) dopo sei mesi di inattività. Puoi riutilizzare un profilo gratuito disattivato, previo pagamento.

#### :material-information-outline:{ .pg-blue } Funzionalità aggiuntive

Tuta offre la versione business di [Tuta alle organizzazioni non profit](https://tuta.com/blog/secure-email-for-non-profit) gratuitamente o con un enorme sconto.

## Criteri

**Si noti che non siamo affiliati a nessuno dei provider che raccomandiamo.** Oltre ai [nostri criteri standard](about/criteria.md), abbiamo sviluppato una serie di requisiti chiari per qualsiasi provider di posta elettronica che desideri essere raccomandato, tra cui l'implementazione delle migliori pratiche del settore, tecnologia moderna e altro ancora. Vi suggeriamo di familiarizzare con questo elenco prima di scegliere un provider di posta elettronica e di condurre le vostre ricerche per assicurarvi che il provider scelto sia la scelta giusta per voi.

### Tecnologia

Consideriamo queste funzionalità come importanti per poter fornire un servizio sicuro e ottimale. You should consider whether the provider has the features you require.

**Requisiti minimi:**

- Must encrypt email account data at rest with zero-access encryption.
- Must be capable of exporting emails as [Mbox](https://en.wikipedia.org/wiki/Mbox) or individual .EML with [RFC5322](https://datatracker.ietf.org/doc/rfc5322) standard.
- Allow users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). I nomi di dominio personalizzati sono importanti per gli utenti, poiché consentono loro di mantenere la propria autonomia dal servizio, dovesse diventare negativo o essere acquisito da un'altra azienda che non dà priorità alla privacy.
- Must operate on owned infrastructure, i.e. not built upon third-party email service providers.

**Caso migliore:**

- Should encrypt all account data (contacts, calendars, etc.) at rest with zero-access encryption.
- Should provide integrated webmail E2EE/PGP encryption as a convenience.
- Should support WKD to allow improved discovery of public OpenPGP keys via HTTP. GnuPG users can get a key with this command: `gpg --locate-key example_user@example.com`.
- Supporto per una casella temporanea per gli utenti esterni. This is useful when you want to send an encrypted email without sending an actual copy to your recipient. Queste email, solitamente, hanno una durata limitata, prima di essere eliminate automaticamente. Inoltre, non richiedono al destinatario di configurare alcuna crittografia, come OpenPGP.
- Should support [sub-addressing](https://en.wikipedia.org/wiki/Email_address#Sub-addressing).
- Should allow users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). I nomi di dominio personalizzati sono importanti per gli utenti, poiché consentono loro di mantenere la propria autonomia dal servizio, dovesse diventare negativo o essere acquisito da un'altra azienda che non dà priorità alla privacy.
- Catch-all or alias functionality for those who use their own domains.
- Should use standard email access protocols such as IMAP, SMTP, or [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Standard access protocols ensure customers can easily download all of their email, should they want to switch to another provider.
- Email provider's services should be available via an [onion service](https://en.wikipedia.org/wiki/.onion).

### Privacy

Preferiamo che i provider da noi consigliati raccolgano il minor numero di dati possibile.

**Requisiti minimi:**

- Must protect sender's IP address, which can involve filtering it from showing in the `Received` header field.
- Must not require personally identifiable information (PII) besides a username and a password.
- Privacy policy must meet the requirements defined by the GDPR.

**Caso migliore:**

- Should accept [anonymous payment options](advanced/payments.md) ([cryptocurrency](cryptocurrency.md), cash, gift cards, etc.)
- Should be hosted in a jurisdiction with strong email privacy protection laws.

### Sicurezza

Email servers deal with a lot of very sensitive data. We expect that providers will adopt industry best practices in order to protect their customers.

**Requisiti minimi:**

- Protection of webmail with 2FA, such as [TOTP](basics/multi-factor-authentication.md#time-based-one-time-password-totp).
- Zero-access encryption, which builds on encryption at rest. Il provider non deve disporre delle chiavi di decrittazione dei dati in loro possesso. Questo previene che dipendenti disonesti possano trapelare i dati sensibili, o che un avversario remoto possa rilasciarli, dopo averli rubati, ottenendo un accesso non autorizzato al server.
- Supporto [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions).
- Nessun errore o vulnerabilità TLS quando si viene profilato da strumenti come [Hardenize](https://hardenize.com), [testssl.sh](https://testssl.sh) o [Qualys SSL Labs](https://ssllabs.com/ssltest); questo include errori relativi ai certificati e parametri DH deboli, come quelli che hanno portato a [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- A server suite preference (optional on TLS 1.3) for strong cipher suites which support forward secrecy and authenticated encryption.
- Una valida politica [MTA-STS](https://tools.ietf.org/html/rfc8461) e [TLS-RPT](https://tools.ietf.org/html/rfc8460).
- Registri [DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities) validi.
- Registri [SPF](https://en.wikipedia.org/wiki/Sender_Policy_Framework) e [DKIM](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail) validi.
- Must have a proper [DMARC](https://en.wikipedia.org/wiki/DMARC) record and policy or use [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) for authentication. Se si utilizza l'autenticazione DMARC, la politica dev'essere impostata su `rifiuta` o `quarantena`.
- Preferenza per una suite di server TLS 1.2 o successiva e un piano per [RFC8996](https://datatracker.ietf.org/doc/rfc8996).
- Invio [SMTPS](https://en.wikipedia.org/wiki/SMTPS), supponendo che SMTP sia utilizzato.
- Standard di sicurezza del sito web come:
    - [HTTP Strict Transport Security](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - [Integrità Subresource](https://en.wikipedia.org/wiki/Subresource_Integrity) se si caricano oggetti da domini esterni.
- Must support viewing of [message headers](https://en.wikipedia.org/wiki/Email#Message_header), as it is a crucial forensic feature to determine if an email is a phishing attempt.

**Caso migliore:**

- Should support hardware authentication, i.e. U2F and [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online).
- [Registro Risorse di Autorizzazione dell'Autorità del Certificato (CAA) DNS](https://tools.ietf.org/html/rfc6844), oltre al supporto DANE.
- Should implement [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), which is useful for people who post to mailing lists [RFC8617](https://tools.ietf.org/html/rfc8617).
- Published security audits from a reputable, third-party firm.
- Programmi di caccia ai bug e/o un processo di divulgazione delle vulnerabilità coordinato.
- Standard di sicurezza del sito web, quali:
    - [Politica sulla Sicurezza dei Contenuti (CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### Fiducia

You wouldn't trust your finances to someone with a fake identity, so why trust them with your email? Richiediamo che i fornitori da noi consigliati rendano pubbliche la propria dirigenza o proprietà. Inoltre, vorremmo vedere rapporti di trasparenza frequenti, specialmente relativi alla gestione delle richieste del governo.

**Requisiti minimi:**

- Dirigenza o proprietà rivolta al pubblico.

**Caso migliore:**

- Rapporti di trasparenza frequenti.

### Marketing

With the email providers we recommend, we like to see responsible marketing.

**Requisiti minimi:**

- Must self-host analytics (no Google Analytics, Adobe Analytics, etc.).
- Must not have any irresponsible marketing, which can include the following:
    - Claims of "unbreakable encryption." Encryption should be used with the intention that it may not be secret in the future when the technology exists to crack it.
    - Guarantees of protecting anonymity 100%. When someone makes a claim that something is 100%, it means there is no certainty for failure. We know people can quite easily de-anonymize themselves in a number of ways, e.g.:
        - Reusing personal information e.g. (email accounts, unique pseudonyms, etc.) that they accessed without anonymity software such as Tor
        - [Browser fingerprinting](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**Caso migliore:**

- Clear and easy-to-read documentation for tasks like setting up 2FA, email clients, OpenPGP, etc.

### Funzionalità aggiuntive

While not strictly requirements, there are some other convenience or privacy factors we looked into when determining which providers to recommend.
