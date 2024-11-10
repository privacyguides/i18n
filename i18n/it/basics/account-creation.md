---
meta_title: "Come creare account internet privatamente - Privacy Guides"
title: "Creazione account"
icon: 'material/account-plus'
description: La creazione di account online è praticamente una necessità di internet, adotta questi accorgimenti per assicurare di rimanere privato.
---

Spesso le persone si iscrivono a servizi senza riflettere. Forse è un servizio di streaming per guardare quella nuova serie di cui tutti parlano, o di un profilo che ti offre uno sconto per il tuo fast food preferito. In ogni caso, dovresti considerare le implicazioni per i tuoi dati, ora e in futuro.

A ogni nuovo servizio che utilizzi, sono associati dei rischi. Violazioni dei dati; divulgazione di informazioni sui clienti a terze parti; dipendenti disonesti che accedono ai dati; sono tutte possibilità che devono essere considerate, fornendo le proprie informazioni. Devi essere sicuro di poterti fidare del servizio, per cui non consigliamo l'archiviazione di dati preziosi su nulla, se non sui prodotti più maturi e testati. Ciò, solitamente, preclude i servizi che forniscono E2EE e hanno subito un controllo crittografico. Un controllo incrementa la garanzia che il prodotto sia stato progettato senza problemi evidenti di sicurezza, causati da uno sviluppatore inesperto.

Inoltre, può essere difficile eliminare i profili, su alcuni servizi. Talvolta, [sovrascrivere i dati](account-deletion.md#overwriting-account-information) associati a un profilo è possibile ma, in altri casi, il servizio manterrà un intero storico delle modifiche al profilo.

## Termini di Servizio e Politica sulla Privacy

I ToS sono le regole che accetti di seguire, utilizzando il servizio. Spesso, nei servizi più grandi, tali regole sono imposte da sistemi automatizzati. Talvolta, questi sistemi automatizzati possono commettere degli errori. Ad esempiio, potresti essere bannato o bloccato dal tuo profilo su alcuni servizi, utilizzando una VPN o un numero VoIP. Fare appello a tali ban è spesso difficile, e richiede anch'esso un procedimento automatizzato, che non ha sempre successo. Ad esempio, questa è una delle motivazioni per cui non suggeriamo di utilizzare Gmail per l'email. L'email è fondamentale per accedere ad altri servizi cui potresti esserti iscritto.

La Politica sulla Privacy è come il servizio dichiara che utilizzerà i tuoi dati, e vale la pena di leggerla, così da meglio comprendere come saranno utilizzati i tuoi dati. Un'azienda od organizzazione, potrebbe non essere legalmente obbligata a seguire tutto ciò che è contenuto nella politica (a seconda della giurisdizione). Ti consigliamo di avere un'idea di quali leggi locali esistono e di ciò che consentono a un fornitore di raccogliere.

Consigliamo di cercare termini particolari, quali servizi di "raccolta dei dati", "analisi dei dati", "cookie", "pubblicità/annunci" o "terze parti". Talvolta, potrai rifiutare la raccolta o la condivisione dei tuoi dati, ma è sempre meglio scegliere un servizio che rispetti la tua privacy, fin dall'inizio.

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

Se non desideri fornire il tuo indirizzo email reale a un servizio, puoi utilizzare un alias. Li abbiamo descritti in maggiore dettaglio sulla nostra pagina di consigli dei servizi email. In breve, i servizi di alias ti consentono di generare nuovi indirizzi email, che inoltrano tutte le email al tuo indirizzo principale. Ciò può contribuire a impedire il tracciamento tra i vari servizi, nonché a gestire le email di marketing che talvolta accompagnano il processo d'iscrizione. Questi possono essere filtrati automaticamente in base all'alias a cui sono inviati.

Se un servizio dovesse essere violato, potresti iniziare a ricevere email di phishing o spam all'indirizzo utilizzato per iscriverti. Utilizzare alias univoci per ogni servizio può assisterti nell'identificare esattamente quale servizio è stato violato.

[Servizi di alias email consigliati](../email-aliasing.md ""){.md-button}

### "Accedi con..." (OAuth)

OAuth è un protocollo d'autenticazione che ti consente di registrarti a un servizio senza condividere troppe informazioni con il fornitore del servizio, se necessarie, utilizzando un profilo esistente presso un altro servizio. Quando nel modulo di registrazione noti qualcosa di simile ad "Accedi con *nome del fornitore*", tipicamente sta utilizzando OAuth.

Quando accedi con OAuth, si aprirà una pagina di login con il provider scelto e l'account esistente e quello nuovo verranno collegati. La tua password non sarà condivisa, a differenza di alcune informazioni essenziali (che potrai revisionare durante la richiesta d'accesso). Questo procedimento è necessario ogni volta che desideri accedere allo stesso profilo.

I principali vantaggi sono:

- **Sicurezza**: non devi affidarti alle pratiche di sicurezza del servizio cui ti stai connettendo quando si tratta di memorizzazione delle tue credenziali d'accesso, poiché sono memorizzate con il fornitore esterno di OAuth che, per quanto riguarda i servizi come Apple e Google, segue tipicamente le migliori pratiche di sicurezza, controlla costantemente i loro sistemi d'autenticazione e non memorizza le credenziali in modo inappropriato (come in testo semplice).
- **Facilità d'uso**: i profili multipli sono gestiti da un unico accesso.

Ma esistono degli svantaggi:

- **Privacy**: il fornitore di OAuth con cui effettui l'accesso conoscerà i servizi che utilizzi.
- **Centralizzazione**: Se il profilo che utilizzi per OAuth è compromesso, o non riesci ad accedervi, tutti gli altri profili a esso connesso ne saranno influenzati.

OAuth può essere specialmente utile in quelle situazioni in cui potresti beneficiare dalla più profonda integrazione tra servizi. Il nostro consiglio è quello di limitare l'utilizzo di OAuth soltanto laddove necessario e di proteggere sempre il profilo principale con l'[AFM](multi-factor-authentication.md).

Tutti i servizi che utilizzano OAuth saranno sicuri quanto il profilo del fornitore sottostante di OAuth. Ad esempio, se desideri proteggere un profilo con una chiave hardware, ma tale servizio non le supporta, puoi proteggerlo con OAuth e una chiave hardware e, ora, hai essenzialmente l'AFM su tutti i tuoi profili. Tuttavia, vale la pena di notare che un'autenticazione debole sul profilo del tuo fornitore OAuth, implica che qualsiasi profilo collegato a tale accesso, sarà anch'esso debole.

Esiste un ulteriore pericolo nell'utilizzo dell'*Accesso con Google*, *Facebook*, o con altri servizi, ossia che il processo di OAuth consente tipicamente la condivisione *bidirezionale* dei dati. Ad esempio l'accesso a un forum con il tuo profilo di Twitter potrebbe garantire a tale forum l'accesso al tuo profilo di Twitter, e di fare cose come pubblicare, leggere i tuoi messaggi, o accedere ad altri dati personali. I fornitori di OAuth ti presenteranno tipicamente un elenco di cose a cui stai garantendo l'accesso al servizio esterno; dovresti sempre assicurati di leggere tale elenco e di non concedere inavvertitamente l'accesso a qualsiasi cosa non sia necessaria.

Anche le applicazioni dannose, in particolare sui dispositivi mobili in cui l'app ha accesso alla sessione di WebView utilizzata per accedere al fornitore di OAuth, possono abusare di tale processo, dirottando la tua sessione con il fornitore di OAuth e ottenendo accesso al tuo profilo di OAuth, tramite tali mezzi. L'utilizzo dell'opzione *Accedi con* con qualsiasi fornitore, dovrebbe sempre essere considerata come una questione di convenienza, per la quale consideri che tali servizi cui ti affidi, non siano dannosi.

### Numero telefonico

Consigliamo di evitare i servizi che richiedono un numero telefonico per iscriversi. A phone number can identify you across multiple services and depending on data sharing agreements this will make your usage easier to track, particularly if one of those services is breached as the phone number is often **not** encrypted.

Dovresti evitare di dare il tuo vero numero di telefono, se possibile. Alcuni servizi consentiranno l'utilizzo di numeri VoIP, tuttavia, questi, innescano spesso dei sistemi di rilevamento delle frodi, causando il blocco di un profilo, quindi, li sconsigliamo per i profili importanti.

In molti casi dovrai fornire un numero che può ricevere SMS o chiamate, in particolare facendo acquisti internazionali, nel caso in cui si verifichi un problema con il tuo ordine ai controlli doganali. È comune che i servizi utilizzino il tuo numero come metodo di verifica; non consentire di essere bloccato da un profilo importante, perché volevi essere furbo e hai inserito un numero falso!

### Nome utente e password

Alcuni servizi ti consentono di registrarti senza utilizzare un indirizzo email e richiedono soltanto di impostare un nome utente e una password. Questi servizi potrebbero fornire un maggiore anonimato, se combinati con una VPN o Tor. Tieni a mente che per questi profili, **non sarà probabilmente possibile recuperarli**, nel caso in cui dimentichi il tuo nome utente o la tua password.
