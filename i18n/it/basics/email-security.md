---
meta_title: "Perché l'Email Non È la Scelta Migliore per Privacy e Sicurezza - Privacy Guides"
title: Sicurezza dell'Email
icon: material/email
description: Email is insecure in many ways, and these are some of the reasons it isn't our top choice for secure communications.
---

L'email è una forma non sicura di comunicazione di default. You can improve your email security with tools such as OpenPGP, which add end-to-end encryption to your messages, but OpenPGP still has a number of drawbacks compared to encryption in other messaging applications.

Di conseguenza, l'email è utilizzata meglio per ricevere email di transazione (quali notifiche, email di verifica, ripristini di password, etc.) dai servizi cui ti iscrivi online, non per comunicare con gli altri.

## Panoramica sulla crittografia delle Email

Il metodo standard per aggiungere l'E2EE alle email tra diversi fornitori email è utilizzando OpenPGP. There are different implementations of the OpenPGP standard, the most common being [GnuPG](../encryption.md#gnu-privacy-guard) and [OpenPGP.js](https://openpgpjs.org).

Even if you use OpenPGP, it does not support [forward secrecy](https://en.wikipedia.org/wiki/Forward_secrecy), which means if the private key of either you or the message recipient is ever stolen, all previous messages encrypted with it will be exposed. Ecco perché consigliamo la [messaggistica istantanea](../real-time-communication.md), che implementa la segretezza in avanti via email, per le comunicazioni personali, quando possibile.

There is another standard which is popular with business called [S/MIME](https://en.wikipedia.org/wiki/S/MIME), however it requires a certificate issued from a [Certificate Authority](https://en.wikipedia.org/wiki/Certificate_authority) (not all of them issue S/MIME certificates, and often a yearly payment is required). In some cases it is more usable than PGP because it has support in popular/mainstream email applications like Apple Mail, [Google Workplace](https://support.google.com/a/topic/9061730), and [Outlook](https://support.office.com/article/encrypt-messages-by-using-s-mime-in-outlook-on-the-web-878c79fc-7088-4b39-966f-14512658f480). However, S/MIME does not solve the issue of lack of forward secrecy, and isn't particularly more secure than PGP.

## Che cos'è lo standard Web Key Directory?

The [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD) standard allows email clients to discover the OpenPGP key for other mailboxes, even those hosted on a different provider. I client di posta elettronica che supportano il WKD chiederanno al server del destinatario una chiave basata sul nome di dominio dell'indirizzo e-mail. Ad esempio, se invii un'email a `jonah@privacyguides.org`, il tuo client di posta elettronica chiederà a `privacyguides.org` la chiave OpenPGP di Jonah e se `privacyguides.org` dispone di una chiave per quell'account, il tuo messaggio verrà automaticamente crittografato.

Oltre ai [client di posta elettronica che consigliamo](../email-clients.md) e che supportano WKD, anche alcuni provider di webmail supportano WKD. Se *la propria chiave* viene pubblicata su WKD per essere utilizzata da altri dipende dalla configurazione del dominio. Se utilizzi un [provider di posta elettronica](../email.md#openpgp-compatible-services) che supporta WKD, come Proton Mail o Mailbox.org, possono pubblicare la tua chiave OpenPGP sul loro dominio per te.

Se si utilizza un dominio personalizzato, è necessario configurare il WKD separatamente. Se si controlla il proprio nome di dominio, è possibile impostare il WKD indipendentemente dal provider di posta elettronica. One easy way to do this is to use the "[WKD as a Service](https://keys.openpgp.org/about/usage#wkd-as-a-service)" feature from the `keys.openpgp.org` server: Set a CNAME record on the `openpgpkey` subdomain of your domain pointed to `wkd.keys.openpgp.org`, then upload your key to [keys.openpgp.org](https://keys.openpgp.org). In alternativa, è possibile effettuare il [self-host del WKD sul proprio server web](https://wiki.gnupg.org/WKDHosting).

If you use a shared domain from a provider which doesn't support WKD, like `@gmail.com`, you won't be able to share your OpenPGP key with others via this method.

### Quali client email supportano E2EE?

I fornitori email che ti consentono di utilizzare i protocolli d'accesso standard come IMAP e SMTP, sono utilizzabili con qualsiasi [client email che consigliamo](../email-clients.md). Depending on the authentication method, this may lead to decreased security if either the provider or the email client does not support [OAuth](account-creation.md#sign-in-with-oauth) or a bridge application as [multifactor authentication](multi-factor-authentication.md) is not possible with plain password authentication.

### Come proteggo le mie chiavi private?

A smart card (such as a [YubiKey](https://support.yubico.com/hc/articles/360013790259-Using-Your-YubiKey-with-OpenPGP) or [Nitrokey](../security-keys.md#nitrokey)) works by receiving an encrypted email message from a device (phone, tablet, computer, etc.) running an email/webmail client. The message is then decrypted by the smart card and the decrypted content is sent back to the device.

It is advantageous for the decryption to occur on the smart card to avoid possibly exposing your private key to a compromised device.

## Panoramica sui metadati email

Email metadata is stored in the [message header](https://en.wikipedia.org/wiki/Email#Message_header) of the email message and includes some visible headers that you may have seen such as `To`, `From`, `Cc`, `Date`, and `Subject`. Esistono anche numerose intestazioni nascoste, incluse da molti client e fornitori email, che possono rivelare informazioni sul tuo profilo.

Il software client potrebbe utilizzare i metadati email per mostrare da chi proviene un messaggio e a che ora è stato ricevuto. I server potrebbero utilizzarlo per determinare dove dev'essere inviato un messaggio email, tra [gli altri scopi](https://en.wikipedia.org/wiki/Email#Message_header) non sempre trasparenti.

### Chi può visualizzare i metadati delle email?

Email metadata is protected from outside observers with [opportunistic TLS](https://en.wikipedia.org/wiki/Opportunistic_TLS), but it is still able to be seen by your email client software (or webmail) and any servers relaying the message from you to any recipients including your email provider. Talvolta i server email utilizzeranno i anche dei servizi di terze parti, per proteggere dallo spam che, generalmente, hanno accesso anche ai tuoi messaggi.

### Perché i metadati non possono essere E2EE?

I metadati dell'email sono fondamentali per le funzionalità di base dell'email (da dove proviene e dove deve andare). E2EE was not built into standard email protocols originally, instead requiring add-on software like OpenPGP. Because OpenPGP messages still have to work with traditional email providers, it cannot encrypt some of this email metadata required for identifying the parties communicating. That means that even when using OpenPGP, outside observers can see lots of information about your messages, such as whom you're emailing, when you're emailing, etc.
