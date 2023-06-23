---
meta_title: "Perché l'email non è la scelta migliore per la privacy e la sicurezza - Privacy Guides"
title: Sicurezza email
icon: material/email
description: La posta elettronica è intrinsecamente insicura sotto molti punti di vista e questi sono alcuni dei motivi per cui non è la nostra scelta principale per le comunicazioni sicure.
---

L'e-mail è una forma di comunicazione insicura per impostazione predefinita. È possibile migliorare la sicurezza delle e-mail con strumenti come OpenPGP, che aggiungono la crittografia end-to-end ai messaggi, ma OpenPGP presenta ancora una serie di svantaggi rispetto alla crittografia di altre applicazioni di messaggistica e alcuni dati delle e-mail non possono mai essere crittografati intrinsecamente a causa del modo in cui le e-mail sono progettate.

Di conseguenza, l'e-mail è utilizzata al meglio per ricevere e-mail transazionali (come notifiche, e-mail di verifica, reimpostazione della password e così via) dai servizi a cui ci si iscrive online, non per comunicare con gli altri.

## Panoramica sulla crittografia delle email

Il modo standard per aggiungere l'E2EE alle e-mail tra diversi provider di posta elettronica è l'utilizzo di OpenPGP. Esistono diverse implementazioni dello standard OpenPGP, le più comuni sono [GnuPG](https://en.wikipedia.org/wiki/GNU_Privacy_Guard) e [OpenPGP.js](https://openpgpjs.org).

Esiste un altro standard, molto diffuso nelle aziende, chiamato [S/MIME](https://en.wikipedia.org/wiki/S/MIME), che però richiede un certificato emesso da un'autorità di certificazione [](https://en.wikipedia.org/wiki/Certificate_authority) (non tutte emettono certificati S/MIME). È supportato da [Google Workplace](https://support.google.com/a/topic/9061730?hl=en&ref_topic=9061731) e [Outlook for Web o Exchange Server 2016, 2019](https://support.office.com/en-us/article/encrypt-messages-by-using-s-mime-in-outlook-on-the-web-878c79fc-7088-4b39-966f-14512658f480).

Anche se si utilizza OpenPGP, non supporta [forward secrecy](https://en.wikipedia.org/wiki/Forward_secrecy), il che significa che se la chiave privata dell'utente o del destinatario viene rubata, tutti i messaggi precedenti crittografati con essa saranno esposti. Per questo motivo si consiglia di utilizzare la [messaggistica istantanea](../real-time-communication.md) che implementano la segretezza in avanti rispetto alla posta elettronica per le comunicazioni da persona a persona, quando possibile.

### Quali client di posta elettronica supportano E2EE?

I provider di posta elettronica che consentono di utilizzare protocolli di accesso standard come IMAP e SMTP possono essere utilizzati con uno qualsiasi dei client di posta elettronica [che consigliamo](../email-clients.md). A seconda del metodo di autenticazione, ciò può comportare una riduzione della sicurezza se il provider o il client di posta elettronica non supportano OATH o un'applicazione ponte, poiché [l'autenticazione a più fattori](multi-factor-authentication.md) non è possibile con l'autenticazione con password semplice.

### Come proteggo la mia chiave privata?

Una smartcard (come una [ YubiKey](https://support.yubico.com/hc/en-us/articles/360013790259-Using-Your-YubiKey-with-OpenPGP) o [Nitrokey](https://www.nitrokey.com)) funziona ricevendo un messaggio email criptato da un dispositivo (telefono, tablet, computer, ecc.) con un client email/webmail. Il messaggio viene quindi decifrato dalla smartcard e il contenuto decifrato viene inviato al dispositivo.

È preferibile che la decodifica avvenga sulla smartcard, per evitare di esporre la chiave privata a un dispositivo compromesso.

## Panoramica sui metadati email

I metadati delle e-mail sono memorizzati [nell'header del messaggio](https://en.wikipedia.org/wiki/Email#Message_header) e comprendono alcune intestazioni visibili, come ad esempio: `A`, `Da`, `Cc`, `Data`, `Oggetto`. Ci sono anche una serie di intestazioni nascoste incluse da molti client e provider di posta elettronica che possono rivelare informazioni sul tuo account.

Il software client può utilizzare i metadati delle e-mail per indicare il mittente di un messaggio e l'ora in cui è stato ricevuto. I server possono utilizzarlo per determinare dove deve essere inviato un messaggio e-mail, tra [altri scopi](https://en.wikipedia.org/wiki/Email#Message_header) non sempre trasparenti.

### Chi può visualizzare i metadati delle email?

I metadati delle e-mail sono protetti da osservatori esterni con [Opportunistic TLS](https://en.wikipedia.org/wiki/Opportunistic_TLS), ma sono comunque visibili dal software del client di posta elettronica (o webmail) e da qualsiasi server che inoltra il messaggio dall'utente a qualsiasi destinatario, compreso il provider di posta elettronica. A volte i server di posta elettronica utilizzano anche servizi di terze parti per proteggersi dallo spam, che in genere hanno accesso ai messaggi.

### Perché i metadati non possono essere cifrati E2EE?

I metadati delle e-mail sono fondamentali per la funzionalità di base delle e-mail (da dove provengono e dove devono andare). Originariamente l'E2EE non era integrato nei protocolli di posta elettronica, ma richiedeva un software aggiuntivo come OpenPGP. Poiché i messaggi OpenPGP devono ancora funzionare con i provider di posta elettronica tradizionali, non può crittografare i metadati delle e-mail, ma solo il corpo del messaggio stesso. Ciò significa che anche quando si utilizza OpenPGP, gli osservatori esterni possono vedere molte informazioni sui vostri messaggi, come ad esempio chi state inviando, l'oggetto, quando state inviando, ecc.
