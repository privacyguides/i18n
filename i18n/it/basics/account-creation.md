---
meta_title: "Come creare account internet privatamente - Privacy Guides"
title: "Creazione account"
icon: 'material/account-plus'
description: La creazione di account online è praticamente una necessità di internet, adotta questi accorgimenti per assicurare di rimanere privato.
---

Spesso le persone si iscrivono a servizi senza riflettere. Maybe it's a streaming service to watch that new show everyone's talking about, or an account that gives you a discount for your favorite fast food place. In ogni caso, dovresti considerare le implicazioni per i tuoi dati, ora e in futuro.

A ogni nuovo servizio che utilizzi, sono associati dei rischi. Violazioni dei dati; divulgazione di informazioni sui clienti a terze parti; dipendenti disonesti che accedono ai dati; sono tutte possibilità che devono essere considerate, fornendo le proprie informazioni. Devi essere sicuro di poterti fidare del servizio, per cui non consigliamo l'archiviazione di dati preziosi su nulla, se non sui prodotti più maturi e testati. Ciò, solitamente, preclude i servizi che forniscono E2EE e hanno subito un controllo crittografico. Un controllo incrementa la garanzia che il prodotto sia stato progettato senza problemi evidenti di sicurezza, causati da uno sviluppatore inesperto.

Inoltre, può essere difficile eliminare i profili, su alcuni servizi. Talvolta, [sovrascrivere i dati](account-deletion.md#overwriting-account-information) associati a un profilo è possibile ma, in altri casi, il servizio manterrà un intero storico delle modifiche al profilo.

## Termini di Servizio e Politica sulla Privacy

I ToS sono le regole che accetti di seguire, utilizzando il servizio. Spesso, nei servizi più grandi, tali regole sono imposte da sistemi automatizzati. Talvolta, questi sistemi automatizzati possono commettere degli errori. For example, you may be banned or locked out of your account on some services for using a VPN or VoIP number. Fare appello a tali ban è spesso difficile, e richiede anch'esso un procedimento automatizzato, che non ha sempre successo. Ad esempio, questa è una delle motivazioni per cui non suggeriamo di utilizzare Gmail per l'email. L'email è fondamentale per accedere ad altri servizi cui potresti esserti iscritto.

The Privacy Policy is how the service says they will use your data, and it is worth reading so that you understand how your data will be used. Un'azienda od organizzazione, potrebbe non essere legalmente obbligata a seguire tutto ciò che è contenuto nella politica (a seconda della giurisdizione). Ti consigliamo di avere un'idea di quali leggi locali esistono e di ciò che consentono a un fornitore di raccogliere.

Consigliamo di cercare termini particolari, quali servizi di "raccolta dei dati", "analisi dei dati", "cookie", "pubblicità/annunci" o "terze parti". Sometimes you will be able to opt out from data collection or from sharing your data, but it is best to choose a service that respects your privacy from the start.

Tieni a mente che stai anche riponendo la tua fiducia nell'azienda od organizzazione, affinché si conformeranno alla propria politica sulla privacy.

## Metodi d'autenticazione

Solitamente, esistono svariati metodi per iscriversi a un profilo, ognuno con i propri benefici e svantaggi.

### Email e password

Il modo più comune per creare un nuovo account è tramite un indirizzo e-mail e una password. Utilizzando questo metodo, dovresti utilizzare un gestore di password e seguire le [migliori pratiche](passwords-overview.md) per ciò che riguarda le password.

<div class="admonition tip" markdown>
<p class="admonition-title">Suggerimento</p>

Puoi utilizzare il tuo gestore di password per organizzare anche altri metodi d'autenticazione! Basta aggiungere la nuova voce e compilare i campi appropriati; puoi aggiungere note per cose come le domande di sicurezza o le chiavi di backup.

</div>

Sarai responsabile della gestione delle tue credenziali di accesso. Per una maggiore sicurezza, puoi impostare l'[AFM](multi-factor-authentication.md) sui tuoi profili.

[Gestori di password consigliati](../passwords.md ""){.md-button}

#### Alias email

Se non desideri fornire il tuo indirizzo email reale a un servizio, puoi utilizzare un alias. We describe them in more detail on our email services recommendation page. In breve, i servizi di alias ti consentono di generare nuovi indirizzi email, che inoltrano tutte le email al tuo indirizzo principale. This can help prevent tracking across services and help you manage the marketing emails that sometimes come with the sign-up process. Questi possono essere filtrati automaticamente in base all'alias a cui sono inviati.

Se un servizio dovesse essere violato, potresti iniziare a ricevere email di phishing o spam all'indirizzo utilizzato per iscriverti. Utilizzare alias univoci per ogni servizio può assisterti nell'identificare esattamente quale servizio è stato violato.

[Servizi di alias email consigliati](../email-aliasing.md ""){.md-button}

### "Accedi con..." (OAuth)

[Open Authorization (OAuth)](https://en.wikipedia.org/wiki/OAuth) is an authentication protocol that allows you to register for a service without sharing much information with the service provider, if any, by using an existing account you have with another service instead. Quando nel modulo di registrazione noti qualcosa di simile ad "Accedi con *nome del fornitore*", tipicamente sta utilizzando OAuth.

Quando accedi con OAuth, si aprirà una pagina di login con il provider scelto e l'account esistente e quello nuovo verranno collegati. La tua password non sarà condivisa, a differenza di alcune informazioni essenziali (che potrai revisionare durante la richiesta d'accesso). Questo procedimento è necessario ogni volta che desideri accedere allo stesso profilo.

I principali vantaggi sono:

- **Security**: You don't have to trust the security practices of the service you're logging into when it comes to storing your login credentials because they are stored with the external OAuth provider. Common OAuth providers like Apple and Google typically follow the best security practices, continuously audit their authentication systems, and don't store credentials inappropriately (such as in plain text).
- **Ease-of-use**: Multiple accounts are managed by a single login.

Ma esistono degli svantaggi:

- **Privacy**: The OAuth provider you log in with will know the services you use.
- **Centralization**: If the account you use for OAuth is compromised, or you aren't able to log in to it, all other accounts connected to it are affected.

OAuth può essere specialmente utile in quelle situazioni in cui potresti beneficiare dalla più profonda integrazione tra servizi. Il nostro consiglio è quello di limitare l'utilizzo di OAuth soltanto laddove necessario e di proteggere sempre il profilo principale con l'[AFM](multi-factor-authentication.md).

Tutti i servizi che utilizzano OAuth saranno sicuri quanto il profilo del fornitore sottostante di OAuth. Ad esempio, se desideri proteggere un profilo con una chiave hardware, ma tale servizio non le supporta, puoi proteggerlo con OAuth e una chiave hardware e, ora, hai essenzialmente l'AFM su tutti i tuoi profili. Tuttavia, vale la pena di notare che un'autenticazione debole sul profilo del tuo fornitore OAuth, implica che qualsiasi profilo collegato a tale accesso, sarà anch'esso debole.

Esiste un ulteriore pericolo nell'utilizzo dell'*Accesso con Google*, *Facebook*, o con altri servizi, ossia che il processo di OAuth consente tipicamente la condivisione *bidirezionale* dei dati. Ad esempio l'accesso a un forum con il tuo profilo di Twitter potrebbe garantire a tale forum l'accesso al tuo profilo di Twitter, e di fare cose come pubblicare, leggere i tuoi messaggi, o accedere ad altri dati personali. I fornitori di OAuth ti presenteranno tipicamente un elenco di cose a cui stai garantendo l'accesso al servizio esterno; dovresti sempre assicurati di leggere tale elenco e di non concedere inavvertitamente l'accesso a qualsiasi cosa non sia necessaria.

Anche le applicazioni dannose, in particolare sui dispositivi mobili in cui l'app ha accesso alla sessione di WebView utilizzata per accedere al fornitore di OAuth, possono abusare di tale processo, dirottando la tua sessione con il fornitore di OAuth e ottenendo accesso al tuo profilo di OAuth, tramite tali mezzi. L'utilizzo dell'opzione *Accedi con* con qualsiasi fornitore, dovrebbe sempre essere considerata come una questione di convenienza, per la quale consideri che tali servizi cui ti affidi, non siano dannosi.

### Numero telefonico

Consigliamo di evitare i servizi che richiedono un numero telefonico per iscriversi. A phone number can identify you across multiple services and depending on data sharing agreements this will make your usage easier to track, particularly if one of those services is breached as the phone number is often **not** encrypted.

Dovresti evitare di dare il tuo vero numero di telefono, se possibile. Some services will allow the use of VoIP numbers, however these often trigger fraud detection systems, causing an account to be locked down, so we don't recommend that for important accounts.

In molti casi dovrai fornire un numero che può ricevere SMS o chiamate, in particolare facendo acquisti internazionali, nel caso in cui si verifichi un problema con il tuo ordine ai controlli doganali. È comune che i servizi utilizzino il tuo numero come metodo di verifica; non consentire di essere bloccato da un profilo importante, perché volevi essere furbo e hai inserito un numero falso!

### Nome utente e password

Alcuni servizi ti consentono di registrarti senza utilizzare un indirizzo email e richiedono soltanto di impostare un nome utente e una password. Questi servizi potrebbero fornire un maggiore anonimato, se combinati con una VPN o Tor. Tieni a mente che per questi profili, **non sarà probabilmente possibile recuperarli**, nel caso in cui dimentichi il tuo nome utente o la tua password.
