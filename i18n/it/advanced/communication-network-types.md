---
title: "Tipi di reti di comunicazione"
icon: 'material/transit-connection-variant'
description: Una panoramica delle diverse architetture di rete, comunemente utilizzate dalle applicazioni di messaggistica istantanea.
---

Esistono svariate architetture di rete, utilizzate comunemente per trasmettere messaggi tra persone. Queste reti possono fornire diverse garanzie per la privacy, per cui vale la pena considerare il tuo [modello di minaccia](../basics/threat-modeling.md), decidendo quale app utilizzare.

[Recommended Instant Messengers](../real-time-communication.md ""){.md-button} [:material-movie-open-play-outline: Video: It's time to stop using SMS](https://www.privacyguides.org/videos/2025/01/24/its-time-to-stop-using-sms-heres-why/ ""){.md-button}

## Reti Centralizzate

![Diagramma delle reti centralizzate](../assets/img/layout/network-centralized.svg){ align=left }

I servizi di messaggistica centralizzati sono quelli in cui tutti i partecipanti si trovano sullo stesso server o la stessa rete di server, controllati dalla stessa organizzazione.

Alcuni servizi di messaggistica ospitati autonomamente, ti consentono di configurare il tuo server. L'hosting autonomo può fornire ulteriori garanzie per la privacy, come nessun registro di utilizzo o accesso limitato ai metadati (dati su chi sta parlando con chi). La messaggistica centralizzata ospitata autonomamente è isolata e, tutti, devono trovarsi sullo stesso server per comunicare.

**Vantaggi:**

- Implementazione di nuove funzionalità e modifiche più rapida.
- È più facile iniziare e trovare contatti.
- Ecosistemi di funzionalità più mature e stabili, essendo più facili da programmare in un software centralizzato.
- I problemi di privacy sono riducibili quando ti affidi a un server ospitato autonomamente.

**Svantaggi:**

- Possono includere [controllo o accesso limitato](https://drewdevault.com/2018/08/08/Signal.html). Questo può includere cose come:
- [Divieto di connettere client di terze parti](https://github.com/LibreSignal/LibreSignal/issues/37#issuecomment-217211165) alla rete centralizzata, che potrebbero fornire una maggiore personalizzazione o una migliore esperienza. Spesso definito nei Termini e Condizioni di utilizzo.
- Documentazione scarsa o assente per gli sviluppatori di terze parti.
- La [proprietà](https://web.archive.org/web/20210729191953/https://blog.privacytools.io/delisting-wire), politica sulla privacy e le operazioni del servizio possono cambiare facilmente quando una singola entità lo controlla, potenzialmente compromettendo il servizio in seguito.
- L'hosting autonomo richiede sforzi e conoscenze sulla configurazione di un servizio.

## Reti Federate

![Diagramma delle reti federate](../assets/img/layout/network-decentralized.svg){ align=left }

La messaggistica federata utilizza svariati server indipendenti e decentralizzati, capaci di comunicare tra loro (l'email è un esempio di servizio federato). La federazione consente agli amministratori di sistema di controllare i propri server, pur continuando a far parte della più grande rete comunicativa.

Quando ospitati autonomamente, i membri di un server federato possono scoprire e comunicare con i membri di altri server, sebbene alcuni di questi potrebbero scegliere di rimanere privati, disabilitando la federazione (es., server di team di lavoro).

**Vantaggi:**

- Consente un maggiore controllo sui propri dati, gestendo il proprio server.
- Ti consente di scegliere a chi affidare i tuoi dati, scegliendo tra svariati server "pubblici".
- Consente spesso i client di terze parti, che possono fornire un'esperienza più nativa, personalizzata o accessibile.
- Server software can be verified that it matches public source code, assuming you have access to the server, or you trust the person who does (e.g., a family member).

**Svantaggi:**

- Aggiungere nuove funzionalità è più complesso, poiché queste devono essere standardizzate e testate per garantirne il funzionamento con tutti i server sulla rete.
- A causa del punto precedente, le funzionalità possono essere carenti, incomplete o funzionare in modi imprevisti rispetto che sulle piattaforme centralizzate, come il trasferimento dei messaggi da offline o l'eliminazione dei messaggi.
- Alcuni metadati potrebbero essere disponibili (es., informazioni come "chi sta parlando con chi", ma non il contenuto effettivo del messaggio, se è utilizzata l'E2EE).
- I server federati richiedono generalmente di affidarsi all'amministratore del proprio server. Potrebbe essere un hobbista o, comunque, non un "professionista della sicurezza" e potrebbe non fornire documenti standard, come una politica sulla privacy o i termini di servizio, che descrivono come sono utilizzati i tuoi dati.
- Gli amministratori del server, talvolta, scelgono di bloccare altri server, fonte di abusi non moderati o che infrangono le regole generali di comportamento accettate. Questo ostacolerà la tua abilità di comunicare con i membri di quei server.

## Reti peer-to-peer

![Diagramma del P2P](../assets/img/layout/network-distributed.svg){ align=left }

La messaggistica P2P si connette a una [rete distribuita](https://en.wikipedia.org/wiki/Distributed_networking) di noti per trasmettere un messaggio al destinatario, senza un server di terze parti.

I client (pari), solitamente, si trovano utilizzando una rete di [calcolo distribuita](https://en.wikipedia.org/wiki/Distributed_computing). Esempi di ciò includono le [Tabelle di Hash Distribuite](https://en.wikipedia.org/wiki/Distributed_hash_table) (DHT), utilizzate ad esempio dai [torrent](https://en.wikipedia.org/wiki/BitTorrent_(protocol)) e da [IPFS](https://en.wikipedia.org/wiki/InterPlanetary_File_System). Another approach is proximity based networks, where a connection is established over Wi-Fi or Bluetooth (for example, Briar or the [Scuttlebutt](https://scuttlebutt.nz) social network protocol).

Una volta che un paro ha trovato un percorso al suo contatto tramite uno di questi metodi, una connessione diretta tra di essi è creata. Sebbene i messaggi siano solitamente crittografati, un osservatore potrà comunque dedurre la posizione e l'identità del mittente e del destinatario.

Le reti P2P non utilizzano i server, poiché i pari comunicano direttamente tra loro e, dunque, non sono ospitabili autonomamente. Tuttavia, alcuni servizi aggiuntivi potrebbero affidarsi ai server centralizzati, come la scoperta dell'utente o la trasmissione di messaggi offline, che possono trarre vantaggio dal hosting autonomo.

**Vantaggi:**

- Le informazioni esposte a terzi sono minime.
- Le moderne piattaforme P2P implementano l'E2EE di default. A differenza dei modelli centralizzati e federati, non esistono server capaci di intercettare e decrittografare le trasmissioni.

**Svantaggi:**

- Serie di funzionalità ridotte:
- I messaggi possono essere inviati solo quando entrambi i peer sono online; tuttavia, il client può memorizzare i messaggi in locale per attendere che il contatto torni online.
- Generalmente, incrementa il consumo di batteria sui dispositivi mobili, poiché il client deve rimanere connesso alla rete distribuita per comprendere chi è online.
- Alcune funzionalità di messaggistica comuni potrebbero non essere implementate o essere incomplete, come l'eliminazione dei messaggi.
- Il tuo indirizzo IP e quello dei contatti con cui stai comunicando, potrebbe essere esposto se non utilizzi il software con una [VPN](../vpn.md) o con [Tor](../tor.md). In molti paesi esiste una forma di sorveglianza di massa e/o di conservazione dei metadati.

## Instradamento anonimo

![Diagramma dell'instradamento anonimo](../assets/img/layout/network-anonymous-routing.svg){ align=left }

La messaggistica che utilizza l'[instradamento anonimo](https://doi.org/10.1007/978-1-4419-5906-5_628) nasconde l'identità del mittente, del destinatario o le prove che stessero comunicando. Idealmente, un servizio di messaggistica dovrebbe nascondere tutte e tre le cose.

There are [many](https://doi.org/10.1145/3182658) ways to implement anonymous routing. Uno dei più famosi è l'[instradamento onion](https://en.wikipedia.org/wiki/Onion_routing) (cioè, [Tor](tor-overview.md)), che comunic i messaggi crittografati attraverso una [rete di copertura](https://en.wikipedia.org/wiki/Overlay_network), che nasconde la posizione di ogni nodo, oltre che il mittente e destinatario di ogni messaggio. Il mittente e il destinatario non interagiscono mai direttamente e si incontrano esclusivamente tramite un nodo di incontro segreto, così che non si verifichi alcuna fuga di indirizzi IP, o di posizioni fisiche. I nodi non possono decrittografare i messaggi, né la destinazione finale; soltanto il destinatario può farlo. Ogni nodo intermedio può decrittografare soltanto una parte, che indica dove inviare il messaggio ancora crittografato, finché non raggiunge il destinatario, che può decrittografarlo interamente, da cui gli "strati a cipolla."

Self-hosting a node in an anonymous routing network does not provide the host with additional privacy benefits, but rather contributes to the whole network's resilience against identification attacks for everyone's benefit.

**Vantaggi:**

- Le informazioni esposte ad altre parti sono minime o nulle.
- I messaggi possono essere trasmessi in modo decentralizzato anche se una delle parti è offline.

**Svantaggi:**

- Propagazione lenta dei messaggi.
- Spesso limitato a pochi tipi di media, prevalentemente testo, a causa della lentezza della rete.
- Meno affidabile se i nodi sono selezionati dall'instradamento casuale, alcuni potrebbero essere molto distanti dal mittente e dal destinatario, aggiungendo latenza o persino fallendo nel trasmettere i messaggi, se uno dei nodi va offline.
- Maggiore complessità d'inizio, poiché la creazione e salvataggio sicuro del backup di una chiave crittografica privata sono necessari.
- Proprio come per altre piattaforme decentralizzate, aggiungere funzionalità è più complesso per gli sviluppatori, rispetto che su una piattaforma centralizzata. Dunque, le funzionalità potrebbero essere implementate male o essere incomplete, come la trasmissione di messaggi offline o l'eliminazione dei messaggi.
