---
meta_title: "Come creare profili internet privatamente - Privacy Guides"
title: "Creare profili"
icon: 'material/account-plus'
description: La creazione di profili online è praticamente una necessità di Internet, aadotta questi accorgimenti per assicurarti di rimanere privato.
---

Spesso le persone si iscrivono a servizi senza riflettere. Forse è un servizio di streaming per guardare quella nuova serie di cui tutti parlano, o di un profilo che ti offre uno sconto per il tuo fast food preferito. In ogni caso, dovresti considerare le implicazioni per i tuoi dati, ora e in futuro.

A ogni nuovo servizio che utilizzi, sono associati dei rischi. Violazioni dei dati; divulgazione di informazioni sui clienti a terze parti; dipendenti disonesti che accedono ai dati; sono tutte possibilità che devono essere considerate, fornendo le proprie informazioni. Devi essere sicuro di poterti fidare del servizio, per cui non consigliamo l'archiviazione di dati preziosi su nulla, se non sui prodotti più maturi e testati. Ciò, solitamente, preclude i servizi che forniscono E2EE e hanno subito un controllo crittografico. Un controllo incrementa la garanzia che il prodotto sia stato progettato senza problemi evidenti di sicurezza, causati da uno sviluppatore inesperto.

Inoltre, può essere difficile eliminare i profili, su alcuni servizi. Talvolta, [sovrascrivere i dati](account-deletion.md#overwriting-account-information) associati a un profilo è possibile ma, in altri casi, il servizio manterrà un intero storico delle modifiche al profilo.

## Termini di Servizio e Politica sulla Privacy

I ToS sono le regole che accetti di seguire, utilizzando il servizio. Spesso, nei servizi più grandi, tali regole sono imposte da sistemi automatizzati. Talvolta, questi sistemi automatizzati possono commettere degli errori. Ad esempiio, potresti essere bannato o bloccato dal tuo profilo su alcuni servizi, utilizzando una VPN o un numero VoIP. Fare appello a tali ban è spesso difficile, e richiede anch'esso un procedimento automatizzato, che non ha sempre successo. Ad esempio, questa è una delle motivazioni per cui non suggeriamo di utilizzare Gmail per l'email. L'email è fondamentale per accedere ad altri servizi cui potresti esserti iscritto.

La Politica sulla Privacy è come il servizio dichiara che utilizzerà i tuoi dati, e vale la pena di leggerla, così da meglio comprendere come saranno utilizzati i tuoi dati. Un'azienda od organizzazione, potrebbe non essere legalmente obbligata a seguire tutto ciò che è contenuto nella politica (a seconda della giurisdizione). Ti consigliamo di avere un'idea di quali leggi locali esistono e di ciò che consentono a un fornitore di raccogliere.

Consigliamo di cercare termini particolari, quali servizi di "raccolta dei dati", "analisi dei dati", "cookie", "pubblicità/annunci" o "terze parti". Talvolta, potrai rifiutare la raccolta o la condivisione dei tuoi daati, ma è sempre meglio scegliere un servizio che rispetti la tua privacy, fin dall'inizio.

Tieni a mente che stai anche riponendo la tua fiducia nell'azienda od organizzazione, affinché si conformeranno alla propria politica sulla privacy.

## Metodi d'autenticazione

Solitamente, esistono svariati metodi per iscriversi a un profilo, ognuno con i propri benefici e svantaggi.

### Email e password

Il modo più comune per creare un nuovo profiilo è con un indirizzo email e una password. Utilizzando questo metodo, dovresti utilizzare un gestore di password e seguire le [migliori pratiche](passwords-overview.md) per ciò che riguarda le password.

!!! tip

    Puoi utilizzare il tuo gestore di password per organizzare anche altri metodi d'autenticazione! Basta aggiungere la nuova voce e compilare i campi appropriati; puoi aggiungere note per cose come le domande di sicurezza o le chiavi di backup.

Sarai responsabile della gestione delle tue credenziali di accesso. Per una maggiore sicurezza, puoi impostare l'[AFM](multi-factor-authentication.md) sui tuoi profili.

[Gestori di password consigliati](../passwords.md ""){.md-button}

#### Alias email

Se non desideri fornire il tuo indirizzo email reale a un servizio, puoi utilizzare un alias. Li abbiamo descritti in maggiore dettaglio sulla nostra pagina di consigli dei servizi email. In breve, i servizi di alias ti consentono di generare nuovi indirizzi email, che inoltrano tutte le email al tuo indirizzo principale. Ciò può contribuire a impedire il tracciamento tra servizi, nonché a gestiire le email di marketing che talvolta accompagnano il processo d'iscrizione. Questi possono essere filtrati automaticamente in base all'alias a cui sono inviati.

Se un servizio dovesse essere violato, potresti iniziare a ricevere email di phishing o spam all'indirizzo utilizzato per iscriverti. Utilizzare alias univoci per ogni servizio può assisterti nell'identificare esattamente quale servizio è stato violato.

[Servizi di alias email consigliati](../email.md#email-aliasing-services ""){.md-button}

### "Accedi con..." (OAuth)

OAuth è un protocollo d'autenticazione che ti consente di registrarti a un servizio senza condividere troppe informazioni con il fornitore del servizio, se necessarie, utilizzando un profilo esistente presso un altro servizio. Quando nel modulo di registrazione noti qualcosa di simile ad "Accedi con *nome del fornitore*", tipicamente sta utilizzando OAuth.

Quando accedi con OAuth, si aprirà una pgina d'accesso con il fornitore di tua scelta, e il tuo profilo esistente e quello nuovo saranno collegati. La tua password non sarà condivisa, a differenza di alcune informazioni essenziali (che potrai revisionare durante la richiesta d'accesso). Questo procedimento è necessario ogni volta che desideri accedere allo stesso profilo.

I principali vantaggi sono:

- **Sicurezza**: nessun rischio di essere coinvolti in una [violazione dei dati](https://en.wikipedia.org/wiki/Data_breach), poiché il sito non memorizza le tue credenziali.
- **Facilità d'uso**: i profili multipli sono gestiti da un unico accesso.

Ma esistono degli svantaggi:

- **Privacy**: il fornitore di OAuth con cui effettui l'accesso conoscerà i servizi che utilizzi.
- **Centralizzazione**: se il profilo utilizzato per OAuth viene compromesso o non riesci ad effettuare l'accesso, tutti gli altri profili a esso collegati saranno a influenzati.

L'autenticazione OAuth può essere specialmente utile in quelle situazioni in cui potresti beneficiare da una migliore integrazione tra servizi. Il nostro consiglio è quello di limitare l'utilizzo di OAuth soltanto laddove necessario e di proteggere sempre il profilo principale con l'[AFM](multi-factor-authentication.md).

Tutti i servizi che utilizzano OAuth saranno sicuri tanto quanto il profilo del tuo fornitore principale. Ad esempio, se desideri proteggere un profilo con una chiave hardware, ma tale servizio non le supporta, puoi proteggerlo con OAuth e una chiave hardware e, ora, hai essenzialmente l'AFM su tutti i tuoi profili. Tuttavia, vale la pena di notare che un'autenticazione debole sul profilo del tuo fornitore OAuth, implica che qualsiasi profilo collegato a tale accesso, sarà anch'esso debole.

### Numero telefonico

Consigliamo di evitare i servizi che richiedono un numero telefonico per iscriversi. Un numero telefonico può identificarti su svariati servizi e, a seconda degli accordi di condivisione dei dati, semplificherà il tracciaamento del tuo utilizzo, particolarmente se uno di essi è violato, poiché, spesso, il numero telefonico **non** è crittografato.

Dovresti evitare di dare il tuo numero telefonico reale, se possibile. Alcuni servizi consentiranno l'utilizzo di numeri VoIP, tuttavia, questi, innescano spesso dei sistemi di rilevamento delle frodi, causando il blocco di un profilo, quindi, li sconsigliamo per i profili importanti.

In molti casi dovrai fornire un numero che può ricevere SMS o chiamate, in particolare facendo acquisti internazionali, nel caso in cui si verifichi un problema con il tuo ordine ai controlli doganali. È comune che i servizi utilizzino il tuo numero come metodo di verifica; non consentire di essere bloccato da un profilo importante, perché volevi essere furbo e hai inserito un numero falso!

### Nome utente e password

Alcuni servizi ti consentono di registrarti senza utilizzare un indirizzo email e richiedono soltanto di impostare un nome utente e una password. Questi servizi potrebbero fornire un maggiore anonimato, se combinati con una VPN o Tor. Tieni a mente che per questi profili, **non sarà probabilmente possibile recuperarli**, nel caso in cui dimentichi il tuo nome utente o la tua password.
