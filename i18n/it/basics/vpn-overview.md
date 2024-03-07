---
meta_title: "Come le VPN proteggono la tua privacy? La nostra panoramica sulle VPN - Privacy Guides"
title: Panoramica VPN
icon: material/vpn
description: Le reti private virtuali spostano il rischio dal vostro ISP a una terza parte di cui vi fidate. Dovresti tenere a mente questi aspetti.
---

Le Reti Private Virtuali sono un metodo d'estensione del termine della tua rete, affinché il traffico esca da qualche altra parte nel mondo.

Normalmente, un ISP può visualizzare il flusso di traffico Internet in entrate e in uscita dal dispositivo di terminazione della tua rete (cioè, il modem). I protocolli crittografici come HTTPS sono comunemente utilizzati su Internet, quindi, potrebbero non riuscire a vedere esattamente ciò che stai pubblicando o leggendo, ma potrebbero farsi un'idea dei [domini che richiedi](../advanced/dns-overview.md#why-shouldnt-i-use-encrypted-dns).

L'utilizzo di una VPN nasconde persino queste informazioni dal tuo ISP, spostando la fiducia che poni nella tua rete, a un server da qualche altra parte nel mondo. Di conseguenza, l'ISP può soltanto vedere che sei conness* a una VPN e nulla sull'attività che vi stai svolgendo.

<div class="admonition note" markdown>
<p class="admonition-title">Nota</p>

Quando ci riferiamo a "Reti Private Virtuali" su questo sito web, solitamente ci riferiamo ai [fornitori di VPN](../vpn.md) **commerciali**, per cui paghi una tariffa mensile, in cambio dell'instradamento sicuro del tuo traffico Internet, tramite server pubblici. Esistono molte altre forme di VPN, come quelle auto-ospitate, o quelle operate dai luoghi di lavoro, che ti consentono di connetterti in sicurezza alle risorse di rete interne/dei dipendenti; tuttavia, queste VPN sono solitamente progettate per accedere in sicurezza alle reti da remoto, piuttosto che per proteggere la privacy della tua connessione a Internet.

</div>

## Come funziona una VPN?

Le VPN criptano il tuo traffico tra il tuo dispositivo e un server di proprietà del tuo fornitore VPN. Dal punto di vista di chiunque si trovi tra te e il server VPN, sembra che ti stia connettendo al server VPN. Dal punto di vista di chiunque si trovi tra il server VPN e il tuo sito di destinazione, tutto ciò che può vedere è il server VPN che si connette al sito web.

``` mermaid
flowchart LR
 763931["Tuo Dispositivo<div>(con Client VPN)</div>"] ===|"Crittografia VPN"| 404512{"Server VPN"}
 404512 -.-|"Nessuna Crittografia VPN"| 593753((("Internet\n(Tua Destinazione)")))
 subgraph 763931["Tuo Dispositivo<div>(con Client VPN)</div>"]
 end
```

Nota che una VPN non aggiunge alcuna sicurezza o crittografia al tuo traffico, tra il server della VPN e la tua destinazione su Internet. Per accedere in sicurezza a un sito web, **devi** comunque assicurarti che HTTPS sia in uso, indipendentemente dall'utilizzo di una VPN.

## Dovrei utilizzare una VPN?

**Sì**, quasi sicuramente. Una VPN presenta molti vantaggi, tra cui:

1. Nascondere il tuo traffico **solo** dal tuo Internet Service Provider.
1. Nascondere i tuoi download (come i torrent) dal tuo ISP e dalle organizzazioni antipirateria.
1. Nascondere il tuo IP da siti web e servizi di terze parti, aiutandoti a mimetizzarti e impedendo il tracciamento basato sull'IP.
1. Permette di aggirare le restrizioni geografiche su alcuni contenuti.

Le VPN possono fornire *alcuni* degli stessi vantaggi offerti da Tor, come nascondere il tuo IP dai siti web visitati e spostare geograficamente il tuo traffico di rete, inoltre i buoni fornitori di VPN non collaboreranno con le autorità legali di regimi oppressivi, soprattutto se scegli un fornitore di VPN al di fuori della tua giurisdizione.

Le VPN non possono criptare i dati al di fuori della connessione tra il tuo dispositivo e il server VPN. I fornitori VPN possono anche vedere e modificare il tuo traffico nello stesso modo in cui potrebbe fare il tuo ISP, quindi c'è ancora un livello di fiducia che stai riponendo in loro. E non c'è alcun modo di verificare le politiche di "nessuna registrazione" di un fornitore VPN.

## Quando non è adatta una VPN?

L'uso di una VPN nei casi in cui utilizzi la tua [vera identità o un'identità già conosciuta](common-misconceptions.md#complicated-is-better) online è improbabile che sia utile. In questo modo si possono attivare sistemi di spam e di rilevamento delle frodi, come nel caso in cui si acceda al sito web della propria banca.

È importante ricordare che una VPN non ti fornirà l'anonimato assoluto, poiché il provider VPN stesso vedrà comunque il tuo indirizzo IP reale, le informazioni sul sito web di destinazione e spesso ha una traccia di denaro che può essere collegata direttamente a te. Non puoi fare affidamento sulle politiche di "nessuna registrazione" per proteggere i tuoi dati da chiunque sia in grado di farlo. Se hai bisogno di una sicurezza totale dalla rete stessa, considera l'utilizzo di [Tor](../advanced/tor-overview.md) in aggiunta o al posto di una VPN.

Inoltre, non dovresti fidarti di una VPN per proteggere la connessione a una destinazione HTTP non criptata. Per garantire la riservatezza e la sicurezza di ciò che fai sui siti web che visiti, devi utilizzare il protocollo HTTPS. In questo modo le tue password, i token di sessione e le query saranno al sicuro dal provider VPN e da altri potenziali avversari tra il server VPN e la tua destinazione. Dovresti attivare la modalità solo HTTPS nel tuo browser (se è supportata) per mitigare gli attacchi che tentano di declassare la tua connessione da HTTPS a HTTP.

## Dovrei utilizzare un DNS criptato con una VPN?

A meno che il tuo fornitore di VPN non ospiti i server DNS crittografati, **probabilmente no**. Utilizzare DOH/DOT (o qualsiasi altra forma di DNS crittografato) con i server di terze parti, aggiungerà semplicemente più entità di cui fidarsi. Il tuo fornitore VPN può comunque vedere quali siti web visiti in base agli indirizzi IP e ad altri metodi. Detto ciò, potrebbero esistere dei vantaggi nell'abilitare il DNS crittografato, per consentire ulteriori funzionalità di sicurezza nel tuo browser, come ECH. Le tecnologie per browser che si affidano al DNS crittografato nel browser sono relativamente nuove e non ancora ampiamente diffuse, quindi, se sono rilevanti per te in particolare, è un esercizio che ti lasciamo ricercare indipendentemente.

Un'altra motivazione comune per cui il DNS crittografato è consigliato, è che impedisce lo spoofing DNS. Tuttavia, il browser dovrebbe già verificare la presenza di [certificati TLS](https://en.wikipedia.org/wiki/Transport_Layer_Security#Digital_certificates) con **HTTPS** e avvisare l'utente. Se non stai utilizzando **HTTPS**, un avversario può comunque modificare qualsiasi cosa oltre alle query DNS e il risultato finale sarà poco diverso.

## Dovrei usare Tor *e* una VPN?

Forse; Tor, in primo luogo, non è necessariamente idoneo per tutti. Considera il tuo [modello di minaccia](threat-modeling.md), poiché se il tuo concorrente non è capace di estrarre informazioni dal tuo fornitore VPN, utilizzare la sola VPN potrebbe fornire una protezione sufficiente.

Se utilizzi Tor, *probabilmente* faresti meglio a connetterti alla rete Tor tramite un fornitore di VPN commerciale. Tuttavia, questa è una materia complessa, approfondita sulla nostra pagina [Panoramica di Tor](../advanced/tor-overview.md).

## Dovrei accedere a Tor tramite i fornitori di VPN che forniscono i "nodi di Tor"?

Non dovresti utilizzare quella funzionalità. Il vantaggio principale dell'utilizzo di Tor è che non devi affidarti al fornitore della tua VPN, il che è negato utilizzando i nodi di Tor ospitati dalla tua VPN, invece di connettersi direttamente a Tor dal proprio computer.

Al momento, Tor supporta soltanto il protocollo TCP. UDP (utilizzato da [WebRTC](https://en.wikipedia.org/wiki/WebRTC), [HTTP3/QUIC](https://en.wikipedia.org/wiki/HTTP/3), e altri protocolli), [ICMP](https://en.wikipedia.org/wiki/Internet_Control_Message_Protocol) e altri pacchetti, saranno rilasciati. Per compensare questa situazione, i fornitori di VPN di solito instradano tutti i pacchetti non-TCP attraverso il loro server VPN (il primo hop). Questo è il caso di [ProtonVPN](https://protonvpn.com/support/tor-vpn/). Inoltre, quando si utilizza questa configurazione di Tor su VPN, non si ha il controllo su altre importanti funzionalità di Tor come [Isolated Destination Address](https://www.whonix.org/wiki/Stream_Isolation) (utilizzo di un circuito Tor diverso per ogni dominio visitato).

La funzionalità dovrebbe esser vista come un *comodo* metodo per accedere ai servizi nascosti su Tor, non per rimanere anonimi. Per un anonimato adeguato, utilizza [Tor Browser](../tor.md).

## Proprietà delle VPN commerciali

Gran parte dei servizi VPN sono posseduti dalle stesse [poche aziende](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies/). Queste losche aziende gestiscono molti piccoli servizi VPN per creare l'illusione di avere una maggiore scelta e massimizzare i profitti. Tipicamente, questi fornitori che si nutrono nella propria società di comodo, prevedono politiche sulla privacy terribili e non gli dovrebbe essere affidato il tuo traffico Internet. Dovresti essere molto rigido su quale fornitore decidi di utilizzare.

Dovresti anche essere consapevole del fatto che molti siti di recensioni delle VPN, sono meeri veicoli pubblicitari, aperti al maggior offerente. ==Privacy Guides non riceve denaro consigliando prodotti esterni, e non utilizza mai programmi d'affiliazione.==

[I nostri consigli sulle VPN](../vpn.md ""){.md-button}

## Alternative VPN Moderne

Di recente, sono stati compiuti alcuni tentativi da varie organizzazioni, per risolvere alcuni problemi delle VPN centralizzate. Queste tecnologie sono relativamente nuove, ma vale la pena tenerle d'occhio, allo svilupparsi del settore.

### Ripetitori Multiparte

I Ripetitori Multiparte (MPR) sono più nodi di proprietà di parti differenti, tali che nessuna parte individuale conosca chi sei e a chi ti stai collegando. Questa è l'idea fondamentale dietro Tor, tuttavia, ora esistono servizi a pagamento che provano a emulare tale modello.

I MPR cercano di risolvere un problema inerente alle VPN: il fatto che devi affidarti completamente a esse. Compiono tale obiettivo segmentando le responsabilità tra due o più aziende differenti. Ad esempio, il Ripetitore Privato di Apple iCloud+, indirizza il tuo traffico attraverso due server:

1. Prima di tutto, un server gestito da Apple.

    Questo server riesce a visualizzare l'IP del tuo dispositivo quando ti ci connetti, e conosce le tue informazioni di pagamento e il tuo ID di Apple, collegato al tuo abbonamento ad iCloud. Tuttavia, non riesce a visualizzare a quale sito web ti stai conneettendo.

2. Poi, per un server gestito da un CDN partner, come Cloudflare o Fastly.

    In realtà, questo server effettua la connessione al tuo sito web di destinazione, ma non ha alcuna conoscenza del tuo dispositivo. Il solo indirizzo IP che conosce è quello del server di Apple.

Altri MPR operati da aziende differenti, come Google o INVISV, operano in un modo molto simile. Questa protezione tramite la segmentazione esiste soltanto se ti fidi del fatto che le due aziende non colludano tra loro per deanonimizzarti.

### VPN Decentralizzate

Un altro tentativo di risoluzione dei poblemi con i servizi VPN centralizzati, sono le dVPN. Questi, si basano sulla tecnologia della blockchain e pretendono di eliminare la fiducia in una singola parte, distribuendo i nodi tra molte persone differenti. Tuttavia, molte volte una dVPN si affiderà predefinitamente a un singolo nodo, a significare che dovrai affidarti completamente a esso, proprio come in una VPN tradizionale. A differenza della VPN tradizionale, quel nodo che può visualizzare tutto il tuo traffico è una persona casuale, invece del fornitore della tua VPN, che può essere controllata e ha responsabilità legali per quanto concerne la tutela della privacy. Per risolvere questo problema, è necessario il salto multiplo, che però ha un costo in termini di stabilità e prestazioni.

Un'altra considerazione riguarda la responsabilità legale. Il nodo d'uscita dovrà affrontare dei problemi legali dall'utilizzo improprio della rete, un problema con cui la rete di Tor ha dovuto confrontarsi per la propria intera esistenza. Ciò scoraggia le persone regolari dall'operare nodi e rende più interessante, per un malintenzionato fornito di molte risorse, ospitarne uno. Questo è un grande problema se il servizio è a nodo singolo, poiché il nodo d'uscita potenzialmente malintenzionato, può vedere chi sei e a cosa ti stai connettendo.

Molte dVPN sono utilizzate per spingere una criptovaluta, piuttosto che per offrire il servizio migliore. Inoltre, tendono a essere reti più piccole con meno nodi, rendendole più vulnerabili agli [attacchi Sybil](https://en.wikipedia.org/wiki/Sybil_attack).

## Informazioni correlate alle VPN

- [The Trouble with VPN and Privacy Review Sites (Il problema dei siti di recensioni di VPN e privacy)](https://blog.privacyguides.org/2019/11/20/the-trouble-with-vpn-and-privacy-review-sites/)
- [Free VPN App Investigation (Indagine sulle app di VPN gratuite)](https://www.top10vpn.com/free-vpn-app-investigation/)
- [Hidden VPN owners unveiled: 101 VPN products run by just 23 companies (Svelati i proprietari segreti delle VPN: 101 prodotti per VPN gestiti da sole 23 aziende)](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies/)
- [This Chinese company is secretly behind 24 popular apps seeking dangerous permissions (Questa azienda cinese è segretamente dietro 24 app popolari che cercano autorizzazioni pericolose)](https://vpnpro.com/blog/chinese-company-secretly-behind-popular-apps-seeking-dangerous-permissions/)
- [VPN - a Very Precarious Narrative (VPN - una narrazione molto precaria)](https://schub.io/blog/2019/04/08/very-precarious-narrative.html) di Dennis Schubert
