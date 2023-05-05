---
meta_title: "Come creare account internet in maniera privata - Privacy Guides"
title: "Creazione account"
icon: 'material/account-plus'
description: La creazione di account online è praticamente una necessità di internet, adottate questi accorgimenti per assicurarvi di rimanere privati.
---

Spesso le persone si iscrivono a servizi senza riflettere. Forse si tratta di un servizio di streaming per guardare la nuova serie di cui tutti parlano, o di un account che ti offre uno sconto per il tuo supermercato preferito. In ogni caso, dovresti considerare le implicazioni per i tuoi dati ora e in futuro.

Ci sono rischi associati ad ogni nuovo servizio che utilizzi. Violazioni dei dati, divulgazione d'informazioni sui clienti a terzi, accesso ai dati da parte di dipendenti furfanti: sono tutte possibilità che devono essere prese in considerazione al momento in cui fornisci le tue informazioni. Devi essere sicuro di poterti fidare del servizio, motivo per cui non consigliamo di archiviare dati preziosi su nulla se non sui prodotti più maturi e testati. Ciò di solito significa servizi che forniscono E2EE e sono stati sottoposti a un ispezione crittografica. Un ispezione aumenta la garanzia che il prodotto sia stato progettato senza problemi di sicurezza evidenti causati da uno sviluppatore inesperto.

Può anche essere difficile eliminare gli account su alcuni servizi. A volte [sovrascrivere i dati](account-deletion.en.md#overwriting-account-information) associati a un account può essere possibile, ma in altri casi il servizio manterrà un'intera cronologia delle modifiche apportate all'account.

## Termini di servizio & Informativa sulla privacy

I ToS sono le regole che accetti di seguire quando utilizzi il servizio. Nei servizi più grandi queste regole sono spesso applicate da sistemi automatici. A volte questi sistemi automatici possono commettere errori. Ad esempio, potresti essere bandito o bloccato dal tuo account di alcuni servizi per l'utilizzo di una VPN o un numero VOIP. Appellare l'espulsione è spesso difficile e comporta anche un processo automatizzato, che non sempre ha successo. Questo è uno dei motivi per cui non suggeriamo di usare Gmail per la posta elettronica ad esempio. L'email è fondamentale per l'accesso ad altri servizi a cui potresti esserti iscritto.

L'informativa sulla privacy è il modo in cui il servizio dichiara di utilizzare i tuoi dati e vale la pena di leggerla per capire come verranno utilizzati. Un'azienda o un'organizzazione potrebbe non essere legalmente obbligata a seguire tutto ciò che è contenuto nell'informativa (dipende dalla giurisdizione). Ti consigliamo di avere un'idea di quali sono le leggi locali e cosa consentono a un fornitore di raccogliere.

Consigliamo di cercare termini particolari come "raccolta dati", "analisi dei dati", "cookie", "annunci" o servizi "di terze parti". A volte potrai rifiutare la raccolta o la condivisione dei tuoi dati, ma è meglio scegliere un servizio che rispetti la tua privacy fin dall'inizio.

Inoltre, riponi la tua fiducia nell'azienda o nell'organizzazione per rispettare effettivamente la loro informativa sulla privacy.

## Metodi di autenticazione

Di solito ci sono diversi modi per iscriversi ad un account, ognuno con i propri vantaggi e svantaggi.

### Email e password

Il modo più comune per creare un nuovo account è tramite un indirizzo e-mail e una password. Quando si utilizza questo metodo, è necessario utilizzare un gestore di password e seguire le [migliori pratiche](passwords-overview.md) per quanto riguarda le password.

!!! important

    Puoi utilizzare il tuo gestore di password per organizzare anche altri metodi di autenticazione! Basta aggiungere la nuova voce e riempire i relativi campi; è inoltre possibile aggiungere note per cose come le domande di sicurezza o per una chiave di backup.

Sarai responsabile della gestione delle tue credenziali di accesso. Per una maggiore sicurezza, puoi impostare [MFA](multi-factor-authentication.md) sui tuoi account.

[Gestori di password consigliati](../passwords.md ""){.md-button}

#### Alias email

Se non vuoi fornire il tuo vero indirizzo email ad un servizio, hai la possibilità di utilizzare un alias. Li abbiamo descritti in modo più dettagliato nella nostra pagina di raccomandazione dei servizi di posta elettronica. In sostanza, i servizi alias consentono di generare nuovi indirizzi email che inoltrano tutte le email al tuo indirizzo principale. Questo può aiutare a prevenire il tracciamento tra i vari servizi e a gestire le email di marketing che talvolta accompagnano il processo di iscrizione. Questi possono essere filtrati automaticamente in base all'alias a cui vengono inviati.

Se un servizio viene violato, potresti iniziare a ricevere email di phishing o spam all'indirizzo che hai utilizzato per iscriverti. L'uso di alias unici per ogni servizio può aiutare a identificare esattamente quale servizio è stato violato.

[Servizi di aliasing email consigliati](../email.md#email-aliasing-services ""){.md-button}

### "Accedi con..." (OAuth)

OAuth è un protocollo di autenticazione che consente di registrarti ad un servizio senza condividere molte informazioni con l'eventuale sito, utilizzando invece un account esistente presso un altro servizio. Quando nel modulo di registrazione noti una cosa simile a: "Accedi con *nome del provider*", in genere il sito utilizza OAuth.

Quando accedi con OAuth, si aprirà una pagina di login con il provider scelto e l'account esistente e quello nuovo verranno collegati. La tua password non verrà condivisa, ma alcune informazioni di base invece si (potrai rivedere quali informazioni verranno condivise durante la richiesta di login). Questo processo è necessario ogni volta che si desidera accedere allo stesso account.

I principali vantaggi sono:

- **Sicurezza**: nessun rischio di essere coinvolti in una [violazione dei dati](https://en.wikipedia.org/wiki/Data_breach) perché il sito non memorizza le tue credenziali.
- **Facilità d'uso**: gli account multipli sono gestiti da un unico accesso.

Ma ci sono degli svantaggi:

- **Privacy**: il provider OAuth con cui effettui l'accesso conoscerà i servizi che utilizzi.
- **Centralizzazione**: se l'account utilizzato per l'OAuth viene compromesso o non riesci ad effettuare il login, tutti gli altri account ad esso collegati saranno a rischio.

L'autenticazione OAuth può essere particolarmente utile nelle situazioni in cui puoi beneficiare di un'integrazione più completa tra i vari servizi. Il nostro consiglio è quello di limitare l'uso di OAuth solo dove è strettamente necessario e di proteggere sempre l'account principale con [MFA](multi-factor-authentication.md).

Tutti i servizi che utilizzano OAuth saranno sicuri tanto quanto l'account del vostro provider principale. Per esempio, se vuoi proteggere un account con una chiave hardware, ma il servizio in questione non le supporta, puoi proteggere l'account che utilizzi con OAuth con una chiave hardware e ora hai essenzialmente l'MFA hardware su tutti i tuoi account. Vale la pena notare, tuttavia, che un'autenticazione debole sull'account del provider OAuth implica che anche qualsiasi account collegato a quel login avrà una sicurezza debole.

### Numero di telefono

Consigliamo di evitare i servizi che richiedono un numero di telefono per l'iscrizione. Un numero di telefono può identificarti su più servizi e, a seconda degli accordi di condivisione dei dati, ciò renderà più facile tenere traccia del tuo utilizzo, in particolare se uno di questi servizi viene violato poiché il numero di telefono è spesso **non** crittografato.

Dovresti evitare di dare il tuo vero numero di telefono se puoi. Alcuni servizi consentono l'uso di numeri VOIP, ma spesso questi attivano i sistemi di rilevamento delle frodi, causando il blocco del account, quindi non li consigliamo per i account importanti.

In molti casi dovrai fornire un numero da cui puoi ricevere SMS o chiamate, in particolare quando fai acquisti a livello internazionale, nel caso in cui ci sia un problema con il tuo ordine ai controlli doganali. È comune che i servizi utilizzino il tuo numero come metodo di verifica; non lasciarti bloccare un account importante perché volevi essere furbo e dare un numero falso!

### Nome utente e password

Alcuni servizi ti consentono di registrarti senza utilizzare un indirizzo email e richiedono solo d'impostare un nome utente e una password. Questi servizi possono fornire un maggiore anonimato se combinati con una VPN o Tor. Tieni presente che per questi account molto probabilmente non ci sarà **nessun modo per recuperare il tuo account** nel caso in cui dimentichi il tuo nome utente o password.
