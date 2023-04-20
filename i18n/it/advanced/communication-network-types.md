---
title: "Tipi di reti di comunicazione"
icon: 'material/transit-connection-variant'
description: Una panoramica dei diversi tipi di architetture di rete comunemente usate da applicazioni di messaggistica istantanea.
---

Esistono diverse architetture di rete comunemente usate per trasmettere messaggi tra le persone. Queste reti possono fornire garanzie di privacy diverse, motivo per cui vale la pena considerare il [modello di minaccia](../basics/threat-modeling.md) quando si decide quale app utilizzare.

[Messaggistica istantanea consigliata](../real-time-communication.md ""){.md-button}

## Reti centralizzate

![Diagramma reti centralizzate](../assets/img/layout/network-centralized.svg){ align=left }

I servizi di messaggistica centralizzati sono quelli in cui tutti i partecipanti si trovano sullo stesso server o rete di server controllati dalla stessa organizzazione.

Alcuni servizi di messaggistica autoserviti consentono di configurare il proprio server. Il self-hosting può fornire ulteriori garanzie di privacy, come l'assenza di log o l'accesso limitato ai metadati (dati su chi parla con chi). I servizi centralizzati self-hosted sono isolati e tutti devono essere sullo stesso server per comunicare.

**Vantaggi:**

- Le nuove funzionalità e le modifiche possono essere implementate più rapidamente.
- È più facile iniziare e trovare contatti.
- Gli ecosistemi con le caratteristiche più mature e stabili sono più facili da programmare in un software centralizzato.
- I problemi di privacy possono essere ridotti quando ci si affida a un server in self-hosting.

**Svantaggi:**

- Possono includere [controllo o accesso limitato](https://drewdevault.com/2018/08/08/Signal.html). Questo può includere cose come:
- Il [divieto di connettere client di terze parti](https://github.com/LibreSignal/LibreSignal/issues/37#issuecomment-217211165) alla rete centralizzata che potrebbero fornire una migliore personalizzazione o esperienza. Spesso definito nei Termini e condizioni d'uso.
- Documentazione scarsa o assente per gli sviluppatori di terze parti.
- La [proprietà](https://web.archive.org/web/20210729191953/https://blog.privacytools.io/delisting-wire/), la politica sulla privacy e le operazioni del servizio possono cambiare facilmente quando un'unica entità lo controlla, compromettendo potenzialmente il servizio in un secondo momento.
- Il self-hosting richiede impegno e conoscenza di come impostare un servizio.

## Reti federate

![Diagramma reti federate](../assets/img/layout/network-decentralized.svg){ align=left }

I servizi di messaggistica federati usano più server indipendenti e decentralizzati, i quali sono in grado di comunicare l'uno con l'altro (la posta elettronica è un esempio di servizio federato). La federazione permette agli amministratori di sistema di controllare i loro server e far comunque parte di una rete di comunicazione più ampia.

Quando "self-hostati", i membri di un server federato possono scoprire e comunicare con i membri di altri server, anche se alcuni server possono scegliere di rimanere privati disabilitando la federazione (es. Il server di un gruppo di lavoro).

**Vantaggi:**

- Consente un maggiore controllo sui propri dati quando si gestisce un proprio server.
- Permette di scegliere a chi affidare i propri dati, scegliendo tra più server "pubblici".
- Spesso consente di utilizzare client di terze parti che possono fornire un'esperienza più nativa, personalizzata o accessibile.
- È possibile verificare che il software del server corrisponda al codice sorgente pubblico, a condizione che si abbia accesso al server o che ci si fidi della persona che lo possiede (ad esempio, un familiare).

**Svantaggi:**

- L'aggiunta di nuove funzionalità è più complessa perché queste devono essere standardizzate e testate per garantire il funzionamento con tutti i server della rete.
- A causa del punto precedente, le funzionalità possono essere carenti, incomplete o funzionare in modo inaspettato rispetto alle piattaforme centralizzate, come ad esempio il trasferimento dei messaggi quando sono offline o la loro cancellazione.
- Alcuni metadati possono essere disponibili (ad esempio, informazioni come "chi sta parlando con chi", ma non il contenuto effettivo del messaggio se si utilizza E2EE).
- I server federati richiedono generalmente la fiducia dell'amministratore del server. Può trattarsi di un appassionato o comunque non di un "professionista della sicurezza" e potrebbe non servire documenti standard come l'informativa sulla privacy o i termini di servizio che descrivono in dettaglio l'utilizzo dei vostri dati.
- Gli amministratori dei server scelgono talvolta di bloccare altri server che sono fonte di abusi non moderati o che violano le regole generali di comportamento accettate. Questo ostacolerà la vostra capacità di comunicare con i membri di quei server.

## Reti peer-to-peer

![Diagramma P2P](../assets/img/layout/network-distributed.svg){ align=left }

I messaggeri P2P si collegano a una [rete distribuita](https://en.wikipedia.org/wiki/Distributed_networking) di nodi per trasmettere un messaggio al destinatario senza l'ausilio di un server di terze parti.

I client (peer) di solito si trovano l'un l'altro attraverso l'uso di una rete [computazionale distribuita](https://en.wikipedia.org/wiki/Distributed_computing). Ne sono un esempio le [Distributed Hash Tables](https://en.wikipedia.org/wiki/Distributed_hash_table) (DHT), utilizzate ad esempio da [torrent](https://en.wikipedia.org/wiki/BitTorrent_(protocol)) e [IPFS](https://en.wikipedia.org/wiki/InterPlanetary_File_System). Un altro approccio è quello delle reti di prossimità, in cui si stabilisce una connessione tramite WiFi o Bluetooth (ad esempio, Briar o il protocollo di social network [Scuttlebutt](https://www.scuttlebutt.nz)).

Una volta che un peer ha trovato un percorso verso il suo contatto attraverso uno di questi metodi, viene stabilita una connessione diretta tra i due. Sebbene i messaggi siano solitamente criptati, un osservatore può comunque dedurre la posizione e l'identità del mittente e del destinatario.

Le reti P2P non utilizzano server, poiché i peer comunicano direttamente tra loro e quindi non possono essere auto-ospitati. Tuttavia, alcuni servizi aggiuntivi possono dipendere da server centralizzati, come la scoperta degli utenti o la trasmissione di messaggi offline, che possono trarre vantaggio dall'auto-ospitalità.

**Vantaggi:**

- Le informazioni esposte a terzi sono minime.
- Le moderne piattaforme P2P implementano E2EE per impostazione predefinita. A differenza dei modelli centralizzati e federati, non ci sono server che possano intercettare e decriptare le trasmissioni.

**Svantaggi:**

- Set di funzioni ridotto:
- I messaggi possono essere inviati solo quando entrambi i peer sono online; tuttavia, il client può memorizzare i messaggi in locale per attendere che il contatto torni online.
- In genere aumenta l'utilizzo della batteria sui dispositivi mobili, perché il client deve rimanere connesso alla rete distribuita per sapere chi è online.
- Alcune funzioni comuni del messenger potrebbero non essere implementate o essere incomplete, come l'eliminazione dei messaggi.
- Il vostro indirizzo IP e quello dei contatti con cui state comunicando possono essere esposti se non utilizzate il software insieme a una [VPN](../vpn.md) o a [Tor](../tor.md). In molti Paesi esiste una forma di sorveglianza di massa e/o di conservazione dei metadati.

## Instradamento anonimo

![Diagramma d'instradamento anonimo](../assets/img/layout/network-anonymous-routing.svg){ align=left }

Un messaggero che utilizza il [routing anonimo](https://doi.org/10.1007/978-1-4419-5906-5_628) nasconde l'identità del mittente, del destinatario o l'evidenza della comunicazione. Idealmente, un messaggero dovrebbe nascondere tutte e tre le cose.

Esistono [molti](https://doi.org/10.1145/3182658) modi diversi per implementare il routing anonimo. Uno dei più famosi è l'[onion routing](https://en.wikipedia.org/wiki/Onion_routing) (cioè [Tor](tor-overview.md)), che comunica messaggi crittografati attraverso una [rete di overlay](https://en.wikipedia.org/wiki/Overlay_network) virtuale che nasconde la posizione di ogni nodo, nonché il destinatario e il mittente di ogni messaggio. Il mittente e il destinatario non interagiscono mai direttamente e si incontrano solo attraverso un nodo d'incontro segreto, in modo che non vi sia alcuna fuga d'indirizzi IP o di posizione fisica. I nodi non possono decrittare i messaggi, né la destinazione finale; solo il destinatario può farlo. Ogni nodo intermedio può decifrare solo una parte che indica dove inviare successivamente il messaggio ancora criptato, finché non arriva al destinatario che può decifrarlo completamente, da cui gli "strati a cipolla".

L'auto-ospitazione di un nodo in una rete di routing anonimo non fornisce al proprietario ulteriori vantaggi in termini di privacy, ma piuttosto contribuisce alla resilienza dell'intera rete contro gli attacchi d'identificazione, a vantaggio di tutti.

**Vantaggi:**

- Le informazioni esposte ad altre parti sono minime o nulle.
- I messaggi possono essere trasmessi in modo decentralizzato anche se una delle parti è offline.

**Svantaggi:**

- Propagazione lenta dei messaggi.
- Spesso limitato a pochi tipi di media, soprattutto testo, perché la rete è lenta.
- Meno affidabile se i nodi sono selezionati con un routing randomizzato, alcuni nodi possono essere molto lontani dal mittente e dal destinatario, aggiungendo latenza o addirittura non riuscendo a trasmettere i messaggi se uno dei nodi va offline.
- È più complesso iniziare, poiché è necessaria la creazione e il backup sicuro di una chiave privata crittografica.
- Come per altre piattaforme decentralizzate, l'aggiunta di funzionalità è più complessa per gli sviluppatori rispetto a una piattaforma centralizzata. Di conseguenza, potrebbero mancare o essere implementate in modo incompleto alcune funzioni, come la trasmissione dei messaggi offline o la cancellazione dei messaggi.
