---
title: "Panoramica Tor"
icon: 'simple/torproject'
description: Tor è una rete decentralizzata e libera, progettata per utilizzare Internet con quanta più privacy possibile.
---

![Logo di Tor](../assets/img/self-contained-networks/tor.svg){ align=right }

[**Tor**](../alternative-networks.md#tor) è una rete decentralizzata e gratuita progettata per utilizzare Internet con la massima privacy possibile. Se utilizzata adeguatamente, la rete consente navigazione e comunicazioni private e anonime. Poiché il traffico di Tor è difficile da bloccare e tracciare, è un efficace strumento di elusione della censura.

[:material-movie-open-play-outline: Video: Why You Need Tor](https://www.privacyguides.org/videos/2025/03/02/why-you-need-tor/ ""){.md-button}

Tor funziona instradando il traffico tramite questi server gestiti da volontari, invece di effettuare una connessione diretta al sito che stai provando a visitare. In questo modo si offusca la provenienza del traffico e nessun server nel percorso di connessione è in grado di vedere il percorso completo del traffico proveniente e diretto, il che significa che nemmeno i server utilizzati per connettersi possono violare l'anonimato.

[:octicons-home-16:](https://torproject.org){ .card-link title=Homepage }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Servizio Onion" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=Documentazione}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/core/tor){ .card-link title="Codice sorgente" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribuisci }

## Connettersi in sicurezza a Tor

Prima di connetterti a Tor, dovresti considerare attentamente cosa vuoi ottenere utilizzando Tor e a chi vuoi nascondere la tua attività in rete.

If you live in a free country, are accessing mundane content via Tor, aren't worried about your ISP or local network administrators having the knowledge that you're using Tor, and want to help [destigmatize](https://2019.www.torproject.org/about/torusers.html.en) Tor usage, you can likely connect to Tor directly via standard means like [Tor Browser](../tor.md) without worry.

Se hai la possibilità di accedere a un provider VPN affidabile e **qualsiasi** dei seguenti punti è vero, quasi certamente dovresti connetterti a Tor attraverso una VPN:

- Utilizzi già un [fornitore VPN affidabile](../vpn.md)
- Il tuo modello di minaccia prevede un avversario in grado di estrarre informazioni dal tuo ISP
- Il tuo modello di minaccia include il tuo stesso ISP come avversario
- Il tuo modello di minaccia include gli amministratori della rete locale prima del tuo ISP come avversario

Poiché abbiamo già [raccomandato in generale](../basics/vpn-overview.md) che la stragrande maggioranza delle persone utilizzi un provider VPN affidabile per una serie di motivi, la seguente raccomandazione sulla connessione a Tor tramite una VPN probabilmente si applica anche a te. <mark>Non è necessario disattivare la VPN prima di connettersi a Tor</mark>, come alcune risorse online potrebbero farti credere.

Collegandosi direttamente a Tor, la tua connessione si farà notare dagli amministratori della rete locale o dal tuo ISP. Il rilevamento e la correlazione di questo traffico [è stato fatto](https://edition.cnn.com/2013/12/17/justice/massachusetts-harvard-hoax) in passato dagli amministratori di rete per identificare e deanonimizzare specifici utenti Tor sulla loro rete. D'altra parte, la connessione a una VPN è quasi sempre meno sospetta, perché i fornitori VPN commerciali sono utilizzati dai consumatori di tutti i giorni per una serie di attività banali come l'aggiramento delle geo-restrizioni, anche in Paesi con forti restrizioni su Internet.

Pertanto, dovresti fare uno sforzo per nascondere il tuo indirizzo IP **prima di** connetterti alla rete Tor. Puoi farlo semplicemente collegandoti a una VPN (tramite un client installato sul tuo computer) e poi accedere a [Tor](../tor.md) come di consueto, ad esempio tramite il Tor Browser. In questo modo si crea una catena di connessioni del tipo:

- [x] Tu → VPN → Tor → Internet

Dal punto di vista del tuo ISP, sembra che stai accedendo normalmente a una VPN (con la relativa copertura che ti fornisce). Dal punto di vista della tua VPN, possono vedere che ti stai connettendo alla rete Tor, ma non possono sapere a quali siti web stai accedendo. Dal punto di vista di Tor, ti stai connettendo normalmente, ma nell'improbabile caso di una qualche compromissione della rete Tor, solo l'IP della tua VPN sarebbe esposto, e la tua VPN dovrebbe *inoltre* essere compromessa per deanonimizzarvi.

Questo **non è** un consiglio per aggirare la censura, perché se Tor è bloccato completamente dal tuo ISP, probabilmente lo sarà anche la tua VPN. Piuttosto, questa raccomandazione mira a far sì che il tuo traffico si confonda meglio con il traffico comune degli utenti della VPN e ti fornisca un certo livello di plausibile negabilità nascondendo il fatto che ti stai connettendo a Tor dal tuo ISP.

---

Noi **sconsigliamo vivamente** di combinare Tor con una VPN in qualsiasi altro modo. Non configurare la connessione in un modo che assomigli a uno dei seguenti:

- Tu → Tor → VPN → Internet
- Tu → VPN → Tor → VPN → Internet
- Qualsiasi altra configurazione

Alcuni provider di VPN e altre pubblicazioni raccomandano occasionalmente queste **errate** configurazioni per eludere i ban di Tor (i nodi di uscita sono bloccati dai siti web) in alcuni luoghi. [Normalmente](https://support.torproject.org/#about_change-paths), Tor cambia frequentemente il percorso del circuito attraverso la rete. Quando si sceglie una *destinazione permanente* VPN (collegandosi a un server VPN *dopo* Tor), si elimina questo vantaggio e si danneggia drasticamente l'anonimato.

È difficile impostare accidentalmente configurazioni errate come queste, perché di solito si tratta di configurare impostazioni proxy personalizzate all'interno di Tor Browser o di configurare impostazioni proxy personalizzate all'interno del client VPN che instrada il traffico VPN attraverso Tor Browser. Se si evitano queste configurazioni non predefinite, probabilmente dovresti essere a posto.

---

<div class="admonition info" markdown>
<p class="admonition-title">Fingerprinting VPN/SSH</p>

Il Tor Project [notes](https://gitlab.torproject.org/legacy/trac/-/wikis/doc/TorPlusVPN#vpnssh-fingerprinting) afferma che *teoricamente* l'utilizzo di una VPN per nascondere le attività Tor al proprio ISP potrebbe non essere infallibile. Le VPN sono risultate vulnerabili al fingerprinting del traffico dei siti web, in cui un avversario può comunque indovinare quale sito web viene visitato, perché tutti i siti web hanno modelli di traffico specifici.

Pertanto, non è irragionevole credere che anche il traffico Tor crittografato nascosto da una VPN possa essere rilevato con metodi simili. Non esistono ricerche in merito e riteniamo che i vantaggi dell'utilizzo di una VPN siano di gran lunga superiori a questi rischi, ma è un aspetto da tenere presente.

Se sei ancora convinto che i trasporti collegabili (bridge) forniscano una protezione aggiuntiva contro il fingerprinting del traffico dei siti web che una VPN non offre, hai sempre la possibilità di utilizzare un bridge **e** una VPN insieme.

</div>

Per stabilire se sia il caso di utilizzare una VPN per connettersi alla rete Tor è necessario un po' di buon senso e la conoscenza delle politiche del proprio governo e del proprio ISP in merito a ciò a cui ci si connette. Tuttavia, anche in questo caso, nella maggior parte dei casi sarà meglio essere visti come connessi a una rete VPN commerciale piuttosto che direttamente alla rete Tor. Se i provider di VPN sono censurati nella tua zona, puoi anche considerare l'utilizzo di trasporti Tor pluggable (ad esempio Snowflake o meek bridge) come alternativa, ma l'uso di questi bridge può destare più sospetti rispetto ai tunnel WireGuard/OpenVPN standard.

## Cosa NON è Tor

La rete Tor non è uno strumento di protezione della privacy perfetto in tutti i casi e presenta una serie di svantaggi che devono essere considerati con attenzione. Questi elementi non ti devono scoraggiare dall'utilizzare Tor se è adatto alle tue esigenze, ma sono comunque elementi su cui riflettere per decidere la soluzione più adatta a te.

### Tor non è una VPN gratuita

Il rilascio dell'applicazione mobile *Orbot* ha portato molte persone a descrivere Tor come una "VPN gratuita" per tutto il traffico del tuo dispositivo. Tuttavia, trattare Tor in questo modo comporta alcuni pericoli rispetto a una tipica VPN.

A differenza dei nodi di uscita di Tor, i fornitori di VPN di solito non sono *attivamente* [malevoli](#caveats). Poiché i nodi di uscita Tor possono essere creati da chiunque, sono punti caldi per il monitoraggio della rete e per le modifiche. Nel 2020, è stato documentato che molti nodi di uscita Tor effettuavano il downgrade del traffico HTTPS in HTTP al fine di [dirottare le transazioni in criptovaluta](https://therecord.media/thousands-of-tor-exit-nodes-attacked-cryptocurrency-users-over-the-past-year). Sono stati osservati anche altri attacchi ai nodi di uscita, come la sostituzione dei download tramite canali non crittografati con malware. HTTPS attenua in una certa misura queste minacce.

Come abbiamo già accennato, Tor è anche facilmente identificabile sulla rete. A differenza di un vero e proprio provider VPN, l'utilizzo di Tor ti farà passare per una persona che probabilmente sta cercando di eludere le autorità. In un mondo perfetto, Tor sarebbe visto dagli amministratori di rete e dalle autorità come uno strumento dai molteplici usi (come vengono viste le VPN), ma in realtà la percezione di Tor è ancora molto meno legittima di quella delle VPN commerciali, per cui l'uso di una VPN vera e propria fornisce una plausibile negazione, ad esempio "la stavo usando solo per guardare Netflix", ecc.

### L'utilizzo di Tor non è irrilevabile

**Anche se utilizzi ponti e trasporti collegabili**, Tor Project non fornisce alcuno strumento per nascondere che tu stia utilizzando Tor dal tuo ISP. Nemmeno l'utilizzo di "trasporti collegabili" o di ponti non pubblici, nasconde il fatto che tu stia utilizzando un canale privato di comunicazione. I trasporti pluggable più popolari come obfs4 (che offusca il tuo traffico affinchè "non sembri nulla") e meek (che utilizza il domain fronting per mimetizzare il tuo traffico) possono essere [rilevati](https://hackerfactor.com/blog/index.php?/archives/889-Tor-0day-Burning-Bridges.html) con tecniche di analisi del traffico abbastanza standard. Snowflake presenta problemi simili e può essere [facilmente individuato](https://hackerfactor.com/blog/index.php?/archives/944-Tor-0day-Snowflake.html) *prima ancora* che venga stabilita una connessione Tor.

Esistono altri trasporti collegabili oltre questi tre, ma si affidano tipicamente alla sicurezza tramite l'oscuramento per eludere il rilevamento. Non sono impossibili da rilevare, sono semplicemente utilizzati da così poche persone, che non vale la pena creare dei rilevatori specifici. Non ci si dovrebbe affidare, specificamente se si è monitorati.

È fondamentale comprendere la differenza tra l'aggiramento della censura e l'elusione del rilevamento. È più facile compiere la prima a causa delle molte limitazioni reali su ciò che i censori della rete possano realmente compiere in massa, ma tali tecniche non nascondono che tu, tu *nello specifico*, stai utilizzando Tor, da una parte interessata che monitora la tua rete.

### Il Browser Tor non è il browser più *sicuro*

L'anonimato può spesso essere in contrasto con la sicurezza: l'anonimato di Tor richiede che ogni utente sia identico, creando una monocultura (gli stessi bug sono presenti per tutti gli utenti del Tor Browser). Come regola generale di cybersicurezza, le monoculture sono generalmente considerate come negative: la sicurezza tramite la diversità (che manca a Tor), fornisce la segmentazione naturale, limitando le vulnerabilità dei gruppi più piccoli, ed è dunque più desiderabile, pur essendo a costo dell'anonimato.

Inoltre, Tor Browser si basa sulle build delle Versioni di Supporto Esteso di Firefox, che ricevono correzioni soltanto per le vulnerabilità considerate *Critiche* ed *Elevate* (non *Medie* e *Basse*). Ciò significa che dei malintenzionati potrebbero, ad esempio:

1. Cercare delle vulnerabilità Critiche/Alte sulle build nightly o beta, quindi controllare se possano essere sfruttate su Tor Browser (questo periodo di vulnerabilità può durare settimane).
2. Incatenare tra loro *svariate* vulnerabilità Medie/Basse, fino all'ottenimento del livello d'accesso desiderato (questo periodo di vulnerabilità può durare mesi o più).

Coloro che sono a rischio di vulnerabilità del browser dovrebbero considerare ulteriori protezioni per difendersi dagli exploit di Tor Browser, come l'utilizzo di Whonix su [Qubes](../os/qubes-overview.md) per contenere la propria navigazione su Tor in una VM sicura e proteggersi dalle fughe di dati.

## Creazione del percorso verso i servizi Clearnet

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

### Il nodo centrale

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

Tor consente di connetterci a un server senza che alcuna singola parte conosca l'intero percorso. Il nodo d'accesso sa chi sei, ma non dove stai andando; il nodo intermedio non sa chi sei, né dove stai andando; il nodo d'uscita sa dove stai andando, ma non chi sei. Poiché il nodo d'uscita è quello che effettua la connessione finale, il server di destinazione non conoscerà il tuo indirizzo IP.

## Avvertenze

Sebbene Tor fornisca forti garanzie per la privacy, devi essere consapevole che Tor non è perfetto:

- Tor non ti protegge mai dall'esporti per errore, ad esempio, se condividi troppe informazioni sulla tua identità reale.
- I nodi d'uscita di Tor possono **modificare** il traffico non crittografato che li attraversa. Ciò significa che il traffico non crittografato, come il traffico HTTP semplice, è modificabile da un nodo d'uscita malintenzionato. Non scaricare **mai** i file da un sito web `http://` non crittografato tramite Tor e assicurati che il tuo browser sia impostato per aggiornare sempre il traffico HTTP in HTTPS.
- I nodi d'uscita di Tor, inoltre, possono monitorare il traffico che li attraversa. Il traffico non crittografato contenente informazioni personali identificative, può deanonimizzarti a quel nodo d'uscita. Ancora, consigliamo di utilizzare soltanto HTTPS su Tor.
- Tor **non** ti protegge da potenti avversari ("Avversari Passivi Globali"), capaci di osservare passivamente *tutto* il traffico di rete in tutto il mondo; e utilizzare Tor [con una VPN](#safely-connecting-to-tor) non cambia tale fatto.
- Gli avversari ben finanziati e capaci di osservare passivamente *gran parrte* del traffico di rete nel mondo, hanno comunque la *possibilità* di deanonimizzare gli utenti di Tor, tramite l'analisi avanzata del traffico.

Se desideri utilizzare Tor per navigare sul web, consigliamo soltanto il Tor Browser **ufficiale**, progettato per evitare il fingerprinting.

- [Tor Browser :material-arrow-right-drop-circle:](../tor.md#tor-browser)

### Protezione fornita dai ponti

I ponti di Tor sono comunemente indicati come un metodo alternativo per nascondere l'utilizzo di Tor da un ISP, piuttosto che una VPN (che suggeriamo di utilizzare, se possibile). Va considerato che, sebbene i ponti potrebbero fornire un'adeguata elusione della censura, questo è soltanto un vantaggio *transitorio*. Non ti proteggono adeguatamente dal fatto che il tuo ISP scopra che tu ti sia *precedentemente* connesso a Tor, tramite un'analisi dello storico del traffico.

Per illustrare tale punto, considera il seguente scenario: ti connetti a Tor tramite un ponte e il tuo ISP non lo rileva, perché non sta svolgendo un'analisi sofisticata del tuo traffico, quindi, tutto va come previsto. Ora, passano 4 mesi, e l'IP del tuo ponte è stato reso pubblico. Questo è un'evenienza molto comune nei ponti, scoperti e bloccati in modo relativamente frequente, ma non immediatamente.

Il tuo ISP desidera identificare gli utenti di Tor di 4 mesi fa e, tramite la registrazione limitata dei metadati, può scoprire che ti sei connesso a un indirizzo IP, che in seguito si è rivelato essere un ponte di Tor. Non hai praticamente nessun'altra scusa per effettuare una simile connessione, quindi l'ISP può dire con estrema sicurezza che, al tempo, tu fossi un utente di Tor.

Confronta ciò con il nostro scenario consigliato, in cui ti connetti a Tor tramite una VPN. Diciamo che, ancora una volta, 4 mesi dopo, il tuo ISP desidera identificare chiunque abbia utilizzato Tor 4 mesi fa. I loro registri sono quasi certamente capaci di identificare il tuo traffico 4 mesi fa, ma tutto ciò che potrebbero visualizzare, è la tua connessione all'indirizzo IP di una VPN. Questo perché, gran parte degli ISP, trattengono per lunghi periodi soltanto i metadati, non i contenuti completi del traffico che richiedi. Memorizzare la totalità dei dati del tuo traffico, richiederebbe una quantità di archiviazione tale, che quasi tutti gli attori di minaccia, non possiedono.

Poiché, quasi certamente, il tuo ISP non cattura tutti i dati a livello di pacchetti, memorizzandoli per sempre, non ha modo di determinare a cosa ti fossi connesso con tale VPN *dopo* il fatto, nemmeno con una tecnica avanzata come l'ispezione profonda dei pacchetti e, dunque, mantieni una negabilità plausibile.

Dunque, i ponti forniscono maggiori benefici per eludere la censura in Internet *sul momento*, ma non sono un sostituto adeguato per **tutti** i benefici forniti dall'utilizzo di una VPN con Tor. Ancora, questo non è un consiglio *contro* l'utilizzo dei ponti di Tor, dovresti essere consapevole di tali limitazioni, mentre prendi la tua decisione. In alcuni casi i ponti potrebbero essere la *sola* opzione (ad esempio, se tutti i fornitori di VPN sono bloccati), quindi, puoi comunque utilizzarli in tali circostanze, tenendone a mente le limitazioni.

Se pensi che un ponte possa aiutare a difendere dal rilevamento o altre analisi avanzate di rete più di quanto il tunnel crittografato di una VPN possa fare, puoi sempre utilizzare un ponte con un VPN. Così, sei comunque protetto dalle tecniche di offuscamento del trasporto collegabile, anche se un avversario ottiene un certo livello di visibilità nel tunnel della tua VPN. Se decidi di intraprendere questo percorso, ti consigliamo di connetterti a un ponte obfs4 dietro la tua VPN, per l'ottimale protezione dal rilevamento, piuttosto che meek o Snowflake.

È [possibile](https://discuss.privacyguides.net/t/clarify-tors-weaknesses-with-respect-to-observability/3676/16) che il trasporto collegabile di [WebTunnel](https://forum.torproject.org/t/tor-relays-announcement-webtunnel-a-new-pluggable-transport-for-bridges-now-available-for-deployment/8180), al momento in sperimentazione, potrebbe mitigare alcune di queste questioni. Continueremo a tenere d'occhio tale tecnologia, ma mano che si sviluppa.

## Risorse aggiuntive

- [Manuale Utente del Tor Browser](https://tb-manual.torproject.org)
- [How Tor Works - Computerphile](https://youtube.com/watch?v=QRYzre4bf7I) <small>(YouTube)</small>
- [Tor Onion Services - Computerphile](https://youtube.com/watch?v=lVcbq_a5N9I) <small>(YouTube)</small>

[^1]: Il primo relay nel tuo circuito è detto "guardia d'accesso" o "guardia". È un relay veloce e stabile che rimane il primo nel tuo circuito per 2-3 mesi, per proteggerti da attacchi di deanonimizzazione noti. Il resto del tuo circuito cambia a ogni nuovo sito web che visiti e, tutti insieme, questi relay, forniscono la completa protezione della privacy di Tor. Per ulteriori informazioni sul funzionamento dei relay di guardia, consulta questo [post del blog](https://blog.torproject.org/improving-tors-anonymity-changing-guard-parameters) e il [documento](https://www-users.cs.umn.edu/~hoppernj/single_guard.pdf) sulle guardie d'accesso. ([https://support.torproject.org/tbb/tbb-2/](https://support.torproject.org/tbb/tbb-2))

[^2]: Flag dei relay: una (s-)qualificazione speciale per le posizioni dei circuiti (ad esempio, "Guardia", "Uscita", "BadExit"), proprietà dei circuiti (ad esempio, "Veloce", "Stabile"), o ruoli (ad esempio, "Autorità", "HSDir"), come assegnato dalle autorità direttorie, e ulteriormente definito nelle specifiche del protocollo direttorio. ([https://metrics.torproject.org/glossary.html](https://metrics.torproject.org/glossary.html))
