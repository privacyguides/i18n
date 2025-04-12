---
meta_title: "Perché l'Email Non È la Scelta Migliore per Privacy e Sicurezza - Privacy Guides"
title: Sicurezza dell'Email
icon: material/email
description: L'email è intrinsecamente non sicura in molti modi; ecco alcune delle motivazioni per cui non è la nostra scelta principale per le comunicazioni sicure.
---

L'email è una forma non sicura di comunicazione di default. Puoi migliorare la sicurezza della tua email con strumenti come OpenPGP, che aggiunge la Crittografia End-to-End ai tuoi messaggi; tuttavia, OpenPGP, presenta ancora numerosi svantaggi rispetto alla crittografia su altre applicazioni di messaggistica e, alcuni dati email, non possono mai essere intrinsecamente crittografati, a causa della progettazione dell'email.

Di conseguenza, l'email è utilizzata meglio per ricevere email di transazione (quali notifiche, email di verifica, ripristini di password, etc.) dai servizi cui ti iscrivi online, non per comunicare con gli altri.

## Panoramica sulla crittografia delle Email

Il metodo standard per aggiungere l'E2EE alle email tra diversi fornitori email è utilizzando OpenPGP. Esistono svariate implementazioni dello standard OpenPGP; le più comuni sono [GnuPG](https://en.wikipedia.org/wiki/GNU_Privacy_Guard) e [OpenPGP.js](https://openpgpjs.org).

Esiste un altro standard popolare tra le aziende, detto [S/MIME](https://en.wikipedia.org/wiki/S/MIME), tuttavia, richiede un certificato emesso da un'[Autorità di Certificazione](https://en.wikipedia.org/wiki/Certificate_authority) (non tutte emettono certificati S/MIME). È supportato da [Google Workplace](https://support.google.com/a/topic/9061730) e [Outlook sul Web o Exchange Server 2016 e 2019](https://support.office.com/article/encrypt-messages-by-using-s-mime-in-outlook-on-the-web-878c79fc-7088-4b39-966f-14512658f480).

Anche se utilizzi OpenPGP, non supporta la [segretezza in avanti](https://en.wikipedia.org/wiki/Forward_secrecy), il che significa che se la chiave privata tua o del destinatario viene rubata, tutti i messaggi precedentemente crittografati saranno esposti. Ecco perché consigliamo la [messaggistica istantanea](../real-time-communication.md), che implementa la segretezza in avanti via email, per le comunicazioni personali, quando possibile.

## Che cos'è lo standard Web Key Directory?

The [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD) standard allows email clients to discover the OpenPGP key for other mailboxes, even those hosted on a different provider. I client di posta elettronica che supportano il WKD chiederanno al server del destinatario una chiave basata sul nome di dominio dell'indirizzo e-mail. Ad esempio, se invii un'email a `jonah@privacyguides.org`, il tuo client di posta elettronica chiederà a `privacyguides.org` la chiave OpenPGP di Jonah e se `privacyguides.org` dispone di una chiave per quell'account, il tuo messaggio verrà automaticamente crittografato.

Oltre ai [client di posta elettronica che consigliamo](../email-clients.md) e che supportano WKD, anche alcuni provider di webmail supportano WKD. Se *la propria chiave* viene pubblicata su WKD per essere utilizzata da altri dipende dalla configurazione del dominio. Se utilizzi un [provider di posta elettronica](../email.md#openpgp-compatible-services) che supporta WKD, come Proton Mail o Mailbox.org, possono pubblicare la tua chiave OpenPGP sul loro dominio per te.

Se si utilizza un dominio personalizzato, è necessario configurare il WKD separatamente. Se si controlla il proprio nome di dominio, è possibile impostare il WKD indipendentemente dal provider di posta elettronica. Un modo semplice per farlo è quello di utilizzare la funzione "[WKD as a Service](https://keys.openpgp.org/about/usage#wkd-as-a-service)" di keys.openpgp.org, impostando una voce CNAME sul sottodominio `openpgpkey` del tuo dominio che punta a `wkd.keys.openpgp.org`, poi caricando la tua chiave su [keys.openpgp.org](https://keys.openpgp.org). In alternativa, è possibile effettuare il [self-host del WKD sul proprio server web](https://wiki.gnupg.org/WKDHosting).

Se utilizzi un dominio condiviso da un fornitore che non supporta WKD, come @gmail.com, non sarai in grado di condividere la tua chiave OpenPGP con altri tramite questo metodo.

### Quali client email supportano E2EE?

I fornitori email che ti consentono di utilizzare i protocolli d'accesso standard come IMAP e SMTP, sono utilizzabili con qualsiasi [client email che consigliamo](../email-clients.md). Depending on the authentication method, this may lead to the decrease security if either the provider or the email client does not support OATH or a bridge application as [multifactor authentication](multi-factor-authentication.md) is not possible with plain password authentication.

### Come proteggo le mie chiavi private?

A smart card (such as a [YubiKey](https://support.yubico.com/hc/articles/360013790259-Using-Your-YubiKey-with-OpenPGP) or [Nitrokey](../security-keys.md#nitrokey)) works by receiving an encrypted email message from a device (phone, tablet, computer, etc.) running an email/webmail client. The message is then decrypted by the smart card and the decrypted content is sent back to the device.

It is advantageous for the decryption to occur on the smart card to avoid possibly exposing your private key to a compromised device.

## Panoramica sui metadati email

I metadati dell'email sono memorizzati nell'[intestazione del messaggio](https://en.wikipedia.org/wiki/Email#Message_header) email e includono alcune intestazioni visibili che potresti aver visto, come: `A`, `Da`, `Cc`, `Data`, `Oggetto`. Esistono anche numerose intestazioni nascoste, incluse da molti client e fornitori email, che possono rivelare informazioni sul tuo profilo.

Il software client potrebbe utilizzare i metadati email per mostrare da chi proviene un messaggio e a che ora è stato ricevuto. I server potrebbero utilizzarlo per determinare dove dev'essere inviato un messaggio email, tra [gli altri scopi](https://en.wikipedia.org/wiki/Email#Message_header) non sempre trasparenti.

### Chi può visualizzare i metadati delle email?

I metadati dell'email sono protetti dagli osservatori esterni con il [TLS opportunistico](https://en.wikipedia.org/wiki/Opportunistic_TLS), ma sono comunque visualizzabili dal software del tuo client email (o webmail) e da qualsiasi server che trasmetta il messaggio da te a qualsiasi destinatario, incluso il tuo fornitore email. Talvolta i server email utilizzeranno i anche dei servizi di terze parti, per proteggere dallo spam che, generalmente, hanno accesso anche ai tuoi messaggi.

### Perché i metadati non possono essere E2EE?

I metadati dell'email sono fondamentali per le funzionalità di base dell'email (da dove proviene e dove deve andare). Originariamente, l'E2EE non è stata integrata nei protocolli email, richiedendo piuttosto dei software aggiuntivi, come OpenPGP. Poiché i messaggi di OpenPGP devono continuare a funzionare con i fornitori email tradizionali, esso non può crittografare i metadati email, ma soltanto il corpo del messaggio. That means that even when using OpenPGP, outside observers can see lots of information about your messages, such as whom you're emailing, the subject lines, when you're emailing, etc.
