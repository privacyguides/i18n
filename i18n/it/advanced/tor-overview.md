---
title: "Panoramica Tor"
icon: 'simple/torproject'
description: Tor è una rete decentralizzata e libera, progettata per utilizzare Internet con quanta più privacy possibile.
---

Tor è una rete decentralizzata e libera, progettata per utilizzare Internet con quanta più privacy possibile. Se utilizzata adeguatamente, la rete consente navigazione e comunicazioni private e anonime.

## Costruzione del percorso verso i servizi Clearnet

I "servizi Clearnet" sono siti web accessibili da qualsiasi browser, come [privacyguides.org](https://www.privacyguides.org). Tor ti consente di collegarti anonimamente a questi siti web indirizzando il tuo traffico attraverso una rete composta da migliaia di server gestiti da volontari, detti nodi (o relay).

Ogni volta che ti [connetti a Tor](../tor.md), sceglierà tre nodi per costruire un percorso verso Internet, detto "circuito."

<figure markdown>
  ![Percorso di Tor che mostra la connessione del tuo dispositivo a un nodo d'accesso, nodo intermedio e nodo d'uscita, prima di raggiungere il sito di destinazione](../assets/img/how-tor-works/tor-path.svg#only-light)
  ![Percorso di Tor che mostra la connessione del tuo dispositivo a un nodo d'accesso, nodo intermedio e nodo d'uscita, prima di raggiungere il siito di destinazione](../assets/img/how-tor-works/tor-path-dark.svg#only-dark)
  <figcaption>Percorso del circuito di Tor</figcaption>
</figure>

Ognuno di questi nodi ha la propria funzione:

### Il Nodo d'Accesso

Il nodo d'accesso, spesso detto nodo di guardia, è il primo nodo cui si connette il client di Tor. Il nodo d'accesso può visualizzare il tuo indirizzo IP, tuttavia non è in grado di visualizzare a cosa ti stai connettendo.

A differenza degli altri nodi, il client di Tor selezionerà casualmente un nodo d'accesso, utilizzandolo per due o tre mesi, per proteggerti da certi attacchi.[^1]

### Il Nodo Intermedio

Il nodo intermedio è il secondo nodo cui si connette il tuo client di Tor. Può visualizzare da quale nodo proviene il traffico (il nodo d'accesso) e a quale nodo andrà in seguito. Il nodo intermedio non può visualizzare l'indirizzo IP o il dominio cui ti stai connettendo.

Per ogni nuovo circuito, il nodo intermedio è selezionato casualmente tra tutti i nodi disponibili di Tor.

### Il Nodo d'Uscita

Il nodo d'uscita è il punto in cui il tuo traffico web abbandona la rete di Tor ed è inoltrato alla tua destinazione desiderata. Il nodo d'uscita non è in grado di visualizzare il tuo indirizzo IP, ma sa a quale sito ti stai connettendo.

Il nodo d'uscita sarà scelto casualmente da tutti i nodi disponibili di Tor, aventi un flag d'uscita.[^2]

## Costruzione del percorso ai Servizi Onion

I "servizi Onion" (anche comunemente noti come "servizi nascosti") sono siti web accessibili esclusivamente dal browser di Tor. Questi hanno un nome di dominio lungo e generato casualmente, che termina per `.onion`.

La connessione a un Servizio Onion su Tor funziona molto similmente alla connessione a un servizio Clearnet, ma il tuo traffico è indirizzato attraverso un totale di **sei** nodi, prima di raggiungere il server di destinazione. Come prima, tuttaviaa, soltanto tre di questi nodi contribuiscono al *tuo* anonimato, mentre gli altri tre proteggono l'anonimato del *Servizio Onion*, nascondendo l'indirizzo IP e la posizione reali del sito web, così come Tor Browser sta nascondendo i tuoi.

<figure style="width:100%" markdown>
  ![Percorso di Tor che mostra il traffico indirizzato attraverso i tuoi tre nodi di Tor, più tre nodi aggiuntivi Tor che nascondono l'identità del sito web](../assets/img/how-tor-works/tor-path-hidden-service.svg#only-light)
  ![Percorso di Tor che mostra il traffico indirizzato attraverso i tuoi tre nodi Tor, più tre nodi aggiuntivi Tor che nascondono l'identità del sito web](../assets/img/how-tor-works/tor-path-hidden-service-dark.svg#only-dark)
  <figcaption>Percorso del circuito Tor con i Servizi Onion. I nodi nel recinto <span class="pg-blue">blu</span> appartengono al tuo browser, mentre i nodi in quello <span class="pg-red">rosso</span> appartengono al server, quindi, la loro identità ti è nascosta.</figcaption>
</figure>

## Crittografia

Tor crittografa tre volte ogni pacchetto (un blocco di dati trasmessi), con le chiavi dai nodi d'uscita, intermedio e d'accesso, in quest'ordine.

Una volta che Tor ha costruito un circuito, la trasmissione dei dati avviene come segue:

1. Prima di tutto, quando il pacchetto arriva al nodo d'accesso, il primo livello di crittografia viene rimosso. In questo pacchetto crittografato, il nodo d'accesso troverà un altro pacchetto crittografato con l'indirizzo del nodo intermedio. Il nodo d'accesso, quindi, inoltrerà il pacchetto al nodo intermedio.

2. Quindi, quando il nodo intermedio riceve il pacchetto dal nodo d'accesso, anch'esso rimuoverà un livello di crittografia con la propria chiave, trovando questa volta un pacchetto crittografato con l'indirizzo del nodo d'uscita. Il nodo intermedio, quindi, inoltrerà il pacchetto al nodo d'uscita.

3. Infine, quando il nodo d'uscit riceve il suo pacchetto, rimuove l'ultimo livello crittografico, con la propria chiave. Il nodo d'uscita visualizzerà l'indirizzo di destinazione e inoltrerà il pacchetto a tale indirizzo.

Segue un diagramma alternativo che mostra il processo. Ogni nodo rimuove il proprio livello crittografico e, quando il server di destinazione restituisce i dati, lo stesso processo si verifica interamente al contrario. Ad esempio, il nodo d'uscita non sa chi sei, ma sa da quale nodo arriva il pacchetto, quindi, aggiunge il proprio livello di crittografia, inviandolo indietro.

<figure markdown>
  ![Crittografia Tor](../assets/img/how-tor-works/tor-encryption.svg#only-light)
  ![Crittografia Tor](../assets/img/how-tor-works/tor-encryption-dark.svg#only-dark)
  <figcaption>Inviare e ricevere dati attraverso la rete Tor</figcaption>
</figure>

Tor consente di connetterci a un server senza che alcuna signola parte conosca l'intero percorso. Il nodo d'accesso sa chi sei, ma non dove stai andando; il nodo intermedio non sa chi sei, né dove stai andando; il nodo d'uscita sa dove stai andando, ma non chi sei. Poiché il nodo d'uscita è quello che effettua la connessione finale, il server di destinazione non conoscerà il tuo indirizzo IP.

## Avvertenze

Sebbene Tor fornisca forti garanzie per la privacy, devi essere consapevole che Tor non è perfetto:

- Gli avversari ben finanziati, capaci di osservare passivamente gran parte del traffico di rete nel globo, sono capaci di deanonimizzare gli utenti di Tor, tramite l'analisi avanzata del traffico. Tor non ti protegge nemmeno dal rischio di esporti per errore, ad esempio, se condividi troppe informazioni sulla tua vera identità.
- I nodi d'uscita di Tor, inoltre, possono monitorare il traffico che li attraversa. Ciò significa che il traffico non crittografato, come quello in HTTP semplice, è registrabile e monitorabile. Se tale traffico contiene informazioni personali identificative, può deanonimizzarti a quel nodo d'uscita. Pertanto, consigliamo di utilizzare HTTPS su Tor, laddove possibile.

Se desideri utilizzare Tor per navigare sul web, consigliamo soltanto il Tor Browser **ufficiale**, progettato per evitare il fingerprinting.

- [Tor Browser :material-arrow-right-drop-circle:](../tor.md#tor-browser)

## Ulteriori Risorse

- [Manuale Utente del Tor Browser](https://tb-manual.torproject.org)
- [Come funziona Tor - Computerphile](https://invidious.privacyguides.net/embed/QRYzre4bf7I?local=true) <small>(YouTube)</small>
- [Servizi Onion di Tor - Computerphile](https://invidious.privacyguides.net/embed/lVcbq_a5N9I?local=true) <small>(YouTube)</small>

[^1]: Il primo relay nel tuo circuito è detto "guardia d'accesso" o "guardia". È un relay veloce e stabile che rimane il primo nel tuo circuito per 2-3 mesi, per proteggerti da attacchi di deanonimizzazione noti. Il resto del tuo circuito cambia a ogni nuovo sito web che visiti e, tutti insieme, questi relay, forniscono la completa protezione della privacy di Tor. Per ulteriori informazioni sul funzionamento dei relay di guardia, consulta questo [post del blog](https://blog.torproject.org/improving-tors-anonymity-changing-guard-parameters) e il [documento](https://www-users.cs.umn.edu/~hoppernj/single_guard.pdf) sulle guardie d'accesso. ([https://support.torproject.org/tbb/tbb-2/](https://support.torproject.org/tbb/tbb-2/))

[^2]: Flag dei relay: una (s-)qualificazione speciale per le posizioni dei circuiti (ad esempio, "Guardia", "Uscita", "BadExit"), proprietà dei circuiti (ad esempio, "Veloce", "Stabile"), o ruoli (ad esempio, "Autorità", "HSDir"), come assegnato dalle autorità direttorie, e ulteriormente definito nelle specifiche del protocollo direttorio. ([https://metrics.torproject.org/glossary.html](https://metrics.torproject.org/glossary.html))
