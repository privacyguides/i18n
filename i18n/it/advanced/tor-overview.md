---
title: "Panoramica Tor"
icon: 'simple/torproject'
description: Tor è una rete decentralizzata e gratuita progettata per utilizzare Internet con la massima privacy possibile.
---

Tor è una rete decentralizzata e gratuita progettata per utilizzare Internet con la massima privacy possibile. Se utilizzata correttamente, la rete consente di navigare e comunicare in modo privato e anonimo.

## Costruzione del percorso verso i servizi Clearnet

I "servizi Clearnet" sono siti web accessibili tramite qualsiasi browser, come [privacyguides.org](https://www.privacyguides.org). Tor ti consente di collegarti a questi siti web in maniera anonima indirizzando il tuo traffico attraverso una rete composta da migliaia di server gestiti da volontari chiamati nodi (o relay).

Ogni volta che ti [connetti a Tor](../tor.md), sceglierà 3 nodi per costruire un percorso verso internet—questo percorso è chiamato "circuito."

<figure markdown>
  ![Percorso di Tor che mostra il tuo dispositivo che si connette ad un nodo di ingresso, ad un nodo centrale, e ad un nodo di uscita prima di raggiungere il sito web di destinazione](../assets/img/how-tor-works/tor-path.svg#only-light)
  ![Percorso di Tor che mostra il tuo dispositivo che si connette ad un nodo di ingresso, ad un nodo centrale, e ad un nodo di uscita prima di raggiungere il sito web di destinazione](../assets/img/how-tor-works/tor-path-dark.svg#only-dark)
  <figcaption>Percorso del circuito Tor</figcaption>
</figure>

Ciascuno di questi nodi ha una propria funzione:

### Il nodo di ingresso

Il nodo di ingresso, spesso chiamato nodo di guardia, è il primo nodo a cui si connette il client Tor. Il nodo di ingresso è in grado di vedere il tuo indirizzo IP, ma non è in grado di vedere a cosa ti stai connettendo.

A differenza degli altri nodi, il client Tor seleziona casualmente un nodo di ingresso e vi rimane per due o tre mesi per proteggerti da alcuni attacchi.[^1]

### Il nodo centrale

Il nodo centrale è il secondo nodo a cui si connette il client Tor. Può vedere da quale nodo proviene il traffico, il nodo di ingresso, e a quale nodo va successivamente. Il nodo centrale non può vedere il tuo indirizzo IP o il dominio a cui ti stai connettendo.

Per ogni nuovo circuito, il nodo centrale viene selezionato a caso tra tutti i nodi Tor disponibili.

### Il nodo di uscita

Il nodo di uscita è il punto in cui il traffico web lascia la rete Tor e viene inoltrato alla destinazione desiderata. Il nodo di uscita non è in grado di vedere l'indirizzo IP, ma sa a quale sito ti stai collegando.

Il nodo di uscita sarà scelto a caso tra tutti i nodi Tor disponibili con un flag di uscita.[^2]

## Costruzione del percorso verso i servizi Onion

I "servizi Onion" (comunemente chiamati "servizi nascosti") sono siti web accessibili solo attraverso il browser Tor. Questi siti web hanno un lungo dominio generato randomicamente che termina con `.onion`.

La connessione ad un servizio Onion su Tor funziona in un modo simile alla connessione ad un servizio Clearnet, ma il tuo traffico viene indirizzato attraverso un totale di **sei** nodi prima di raggiungere il server di destinazione. Come in precedenza, tuttavia, solo tre di questi nodi contribuiscono al *tuo* anonimato, mentre gli altri tre nodi proteggono *l'anonimato dei servizi Onion *nascondendo il vero IP e la posizione del sito web nello stesso modo in cui il browser Tor nasconde la tua.

<figure style="width:100%" markdown>
  ![Percorso di Tor che mostra il traffico indirizzato attraverso i tuoi tre nodi Tor più altri tre nodi Tor che nascondono l'identità del sito web](../assets/img/how-tor-works/tor-path-hidden-service.svg#only-light)
  ![Percorso di Tor che mostra il traffico indirizzato attraverso i tuoi tre nodi Tor più altri tre nodi Tor che nascondono l'identità del sito web](../assets/img/how-tor-works/tor-path-hidden-service-dark.svg#only-dark)
  <figcaption>Percorso del circuito Tor con i servizi Onion. I nodi nel recinto <span class="pg-blue">blu</span> appartengono al tuo browser, mentre i nodi nel recinto <span class="pg-red">rosso</span> appartengono al server, quindi la loro identità è nascosta all'utente.</figcaption>
</figure>

## Crittografia

Tor cripta ogni pacchetti (un blocco di dati trasmetti) tre volte con la chiave dei nodi di uscita, centrale e di ingresso—in questo ordine.

Una volta che Tor ha costruito un circuito, la trasmissione dei dati avviene in questo modo:

1. Prima di tutto, quando il pacchetto arriva al nodo di ingresso, il primo livello di crittografia viene rimosso. In questo pacchetto criptato, il nodo di ingresso troverà un altro pacchetto criptato con l'indirizzo del nodo centrale. Il nodo di ingresso invierà quindi il pacchetto al nodo centrale.

2. Successivamente, quando il nodo centrale riceve il pacchetto dal nodo di ingresso, rimuoverà anche lui un livello di crittografia con la sua chiave, e questa volta troverà un pacchetto criptato con l'indirizzo del nodo di uscita. Il nodo centrale invierà quindi il pacchetto al nodo di uscita.

3. Infine, quando il nodo di uscita riceve il suo pacchetto, rimuoverà l'ultimo livello di crittografia con la sua chiave. Il nodo d'uscita vedrà l'indirizzo di destinazione e invierà il pacchetto a quell'indirizzo.

Di seguito è riportato un diagramma alternativo che mostra il processo. Ogni nodo rimuove il proprio livello di crittografia e quando il server di destinazione ritorna i dati, lo stesso processo avviene interamente al contrario. Per esempio, il nodo di uscita non sa chi sei, ma sa da quale nodo arriva il pacchetto, e quindi aggiunge il proprio livello di crittografia e lo invia indietro.

<figure markdown>
  ![Crittografia Tor](../assets/img/how-tor-works/tor-encryption.svg#only-light)
  ![Crittografia Tor](../assets/img/how-tor-works/tor-encryption-dark.svg#only-dark)
  <figcaption>Inviare e ricevere dati attraverso la rete Tor</figcaption>
</figure>

Tor permette di connetterci ad un server senza che nessuno conosca l'intero percorso. Il nodo di ingresso sa chi sei, ma non sa dove stai andando; il nodo centrale non sa chi sei o dove stai andando; e il nodo di uscita sa dove stai andando, ma non sa chi sei. Poiché il nodo di uscita è quello che effettua la connessione finale, il server di destinazione non saprà mai il vostro indirizzo IP.

## Avvertenze

Sebbene Tor fornisca forti garanzie di privacy, devi essere consapevole che Tor non è perfetto:

- Avversari ben finanziati, in grado di osservare passivamente la maggior parte del traffico di rete in tutto il mondo, hanno la possibilità di deanonimizzare gli utenti Tor attraverso un'analisi avanzata del traffico. Tor non vi protegge nemmeno dal rischio di esporvi per errore, per esempio se condividete troppe informazioni private sulla vostra identità.
- I nodi di uscita Tor possono monitorare il traffico che li attraversa. Questo significa il traffico non è criptato, come il semplice traffico HTTP, può essere facilmente registrato e monitorato. Se tale traffico contiene informazioni personali, allora può deanonimizzarti a quel nodo d'uscita. Pertanto, consigliamo di usare HTTPS over Tor, ove possibile.

Se desideri utilizzare Tor per navigare nel web, consigliamo solo il browser Tor **ufficiale**—è progettato per prevenire il rilevamento del fingerprinting.

- [Tor Browser :material-arrow-right-drop-circle:](../tor.md#tor-browser)

## Risorse aggiuntive

- [Manuale d'uso del Tor browser](https://tb-manual.torproject.org)
- [Come funziona Tor - Computerphile](https://invidious.privacyguides.net/embed/QRYzre4bf7I?local=true) <small>(YouTube)</small>
- [Servizi Tor Onion - Computerphile](https://invidious.privacyguides.net/embed/lVcbq_a5N9I?local=true) <small>(YouTube)</small>

[^1]: Il primo relè del tuo circuito viene chiamato "guardia d'ingresso" o "guardia". Si tratta di un relè veloce e stabile che resta il primo nel tuo circuito per 2-3 mesi per proteggerti da un attacco utile a deanonimizzarti. Il resto del circuito cambia ad ogni nuovo sito web che visiti, e tutti insieme questi relè forniscono la protezione completa della privacy di Tor. Per informazioni aggiuntive sul funzionamento dei relè di protezione, consulta il [post del blog](https://blog.torproject.org/improving-tors-anonymity-changing-guard-parameters) e il [documento](https://www-users.cs.umn.edu/~hoppernj/single_guard.pdf) sulle guardie d'ingresso. ([https://support.torproject.org/tbb/tbb-2/](https://support.torproject.org/tbb/tbb-2/))

[^2]: Flag dei relè: una speciale (s-)qualificazione dei relè per le posizioni dei circuiti (ad esempio, "Guardia", "Uscita", "BadExit"), le proprietà dei circuiti (ad esempio, "Veloce", "Stabile") o i ruoli (ad esempio, "Authority", "HSDir"), come assegnati dalle autorità di directory e ulteriormente definiti nelle specifiche del protocollo di directory. ([https://metrics.torproject.org/glossary.html](https://metrics.torproject.org/glossary.html))
