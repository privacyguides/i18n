---
title: "Panoramica Tor"
icon: 'simple/torproject'
description: Tor è una rete decentralizzata e libera, progettata per utilizzare Internet con quanta più privacy possibile.
---

Tor è una rete decentralizzata e libera, progettata per utilizzare Internet con quanta più privacy possibile. Se utilizzata adeguatamente, la rete consente navigazione e comunicazioni private e anonime.

## Connettersi in sicurezza a Tor

Prima di connettersi a [Tor](../tor.md), è necessario considerare attentamente cosa si vuole ottenere utilizzando Tor e a chi si vuole nascondere la propria attività in rete.

Se vivi in un Paese libero, accedi a contenuti banali tramite Tor, non sei preoccupato che il tuo ISP o gli amministratori della rete locale sappiano che stai usando Tor e vuoi aiutare [a de-stigmatizzare](https://2019.www.torproject.org/about/torusers.html.en) l'uso di Tor, puoi probabilmente connetterti a Tor direttamente tramite mezzi standard come [Tor Browser](../tor.md) senza preoccupazioni.

Se hai la possibilità di accedere a un provider VPN affidabile e **qualsiasi** dei seguenti punti è vero, quasi certamente dovresti connetterti a Tor attraverso una VPN:

- Utilizzi già un [provider VPN affidabile](../vpn.md)
- Il tuo modello di minaccia prevede un avversario in grado di estrarre informazioni dal tuo ISP
- Il tuo modello di minaccia include il tuo stesso ISP come avversario
- Il tuo modello di minaccia include gli amministratori della rete locale prima del tuo ISP come avversario

Poiché abbiamo già [raccomandato in generale](../basics/vpn-overview.md) che la stragrande maggioranza delle persone utilizzi un provider VPN affidabile per una serie di motivi, la seguente raccomandazione sulla connessione a Tor tramite una VPN probabilmente si applica anche a te. <mark>Non è necessario disattivare la VPN prima di connettersi a Tor</mark>, come alcune risorse online potrebbero far credere.

Collegandosi direttamente a Tor, la connessione si farà notare dagli amministratori della rete locale o dal tuo ISP. Il rilevamento e la correlazione di questo traffico [è stato fatto](https://edition.cnn.com/2013/12/17/justice/massachusetts-harvard-hoax/) in passato dagli amministratori di rete per identificare e deanonimizzare specifici utenti Tor sulla loro rete. D'altra parte, la connessione a una VPN è quasi sempre meno sospetta, perché i provider VPN commerciali sono utilizzati dai consumatori di tutti i giorni per una serie di attività banali come l'aggiramento delle geo-restrizioni, anche in Paesi con forti restrizioni su Internet.

Pertanto, si dovrebbe fare uno sforzo per nascondere il proprio indirizzo IP **prima di** connettersi alla rete Tor. È possibile farlo semplicemente collegandosi a una VPN (tramite un client installato sul computer) e poi accedere a [Tor](../tor.md) come di consueto, ad esempio tramite Tor Browser. In questo modo si crea una catena di connessioni del tipo:

- [x] Tu → VPN → Tor → Internet

Dal punto di vista del tuo ISP, sembra che stai accedendo normalmente a una VPN (con la relativa copertura che ti fornisce). Dal punto di vista della VPN, possono vedere che ti stai connettendo alla rete Tor, ma non possono sapere a quali siti web stai accedendo. Dal punto di vista di Tor, ti stai connettendo normalmente, ma nell'improbabile caso di una qualche compromissione della rete Tor, solo l'IP della tua VPN sarebbe esposto, e la tua VPN dovrebbe *inoltre* essere compromessa per deanonimizzarvi.

Questo **non è** un consiglio per aggirare la censura, perché se Tor è bloccato completamente dal tuo ISP, probabilmente lo sarà anche la tua VPN. Piuttosto, questa raccomandazione mira a far sì che il tuo traffico si confonda meglio con il traffico comune degli utenti della VPN e ti fornisca un certo livello di plausibile negabilità nascondendo il fatto che ti stai connettendo a Tor dal tuo ISP.

---

Noi **sconsigliamo vivamente** di combinare Tor con una VPN in qualsiasi altro modo. Non configurare la connessione in un modo che assomigli a uno dei seguenti:

- Tu → Tor → VPN → Internet
- Tu → VPN → Tor → VPN → Internet
- Qualsiasi altra configurazione

Alcuni provider di VPN e altre pubblicazioni raccomandano occasionalmente queste **errate** configurazioni per eludere i ban di Tor (i nodi di uscita sono bloccati dai siti web) in alcuni luoghi. [Normalmente](https://support.torproject.org/#about_change-paths), Tor cambia frequentemente il percorso del circuito attraverso la rete. Quando si sceglie una *destinazione permanente* VPN (collegandosi a un server VPN *dopo* Tor), si elimina questo vantaggio e si danneggia drasticamente l'anonimato.

È difficile impostare accidentalmente configurazioni errate come queste, perché di solito si tratta di configurare impostazioni proxy personalizzate all'interno di Tor Browser o di configurare impostazioni proxy personalizzate all'interno del client VPN che instrada il traffico VPN attraverso Tor Browser. Se si evitano queste configurazioni non predefinite, probabilmente dovresti essere a posto.

---

!!! info "VPN/SSH Fingerprinting"

    Il Tor Project [notes](https://gitlab.torproject.org/legacy/trac/-/wikis/doc/TorPlusVPN#vpnssh-fingerprinting) afferma che *teoricamente* l'utilizzo di una VPN per nascondere le attività Tor al proprio ISP potrebbe non essere infallibile. Le VPN sono risultate vulnerabili al fingerprinting del traffico dei siti web, in cui un avversario può comunque indovinare quale sito web viene visitato, perché tutti i siti web hanno modelli di traffico specifici.
    
    Pertanto, non è irragionevole credere che anche il traffico Tor crittografato nascosto da una VPN possa essere rilevato con metodi simili. Non esistono ricerche in merito e riteniamo che i vantaggi dell'utilizzo di una VPN siano di gran lunga superiori a questi rischi, ma è un aspetto da tenere presente.
    
    Se sei ancora convinto che i trasporti collegabili (bridge) forniscano una protezione aggiuntiva contro il fingerprinting del traffico dei siti web che una VPN non offre, hai sempre la possibilità di utilizzare un bridge **e** una VPN insieme.

Per stabilire se sia il caso di utilizzare una VPN per connettersi alla rete Tor è necessario un po' di buon senso e la conoscenza delle politiche del proprio governo e del proprio ISP in merito a ciò a cui ci si connette. Tuttavia, anche in questo caso, nella maggior parte dei casi sarà meglio essere visti come connessi a una rete VPN commerciale piuttosto che direttamente alla rete Tor. Se i provider di VPN sono censurati nella tua zona, puoi anche considerare l'utilizzo di trasporti Tor pluggable (ad esempio Snowflake o meek bridge) come alternativa, ma l'uso di questi bridge può destare più sospetti rispetto ai tunnel WireGuard/OpenVPN standard.

## Cosa NON è Tor

La rete Tor non è uno strumento di protezione della privacy perfetto in tutti i casi e presenta una serie di svantaggi che devono essere considerati con attenzione. Questi elementi non ti devono scoraggiare dall'utilizzare Tor se è adatto alle tue esigenze, ma sono comunque elementi su cui riflettere per decidere la soluzione più adatta a te.

### Tor non è una VPN gratuita

Il rilascio dell'applicazione mobile *Orbot* ha portato molte persone a descrivere Tor come una "VPN gratuita" per tutto il traffico del tuo dispositivo. Tuttavia, trattare Tor in questo modo comporta alcuni pericoli rispetto a una tipica VPN.

A differenza dei nodi di uscita di Tor, i fornitori di VPN di solito non sono *attivamente* [malintenzionati](#caveats). Poiché i nodi di uscita Tor possono essere creati da chiunque, sono punti caldi per il monitoraggio della rete e per le modifiche. Nel 2020, è stato documentato che molti nodi di uscita Tor effettuavano il downgrade del traffico HTTPS in HTTP al fine di [dirottare le transazioni in criptovaluta](https://therecord.media/thousands-of-tor-exit-nodes-attacked-cryptocurrency-users-over-the-past-year). Sono stati osservati anche altri attacchi ai nodi di uscita, come la sostituzione dei download tramite canali non crittografati con malware. HTTPS attenua in una certa misura queste minacce.

Come abbiamo già accennato, Tor è anche facilmente identificabile sulla rete. A differenza di un vero e proprio provider VPN, l'utilizzo di Tor ti farà passare per una persona che probabilmente sta cercando di eludere le autorità. In a perfect world, Tor would be seen by network administrators and authorities as a tool with many uses (like how VPNs are viewed), but in reality the perception of Tor is still far less legitimate than the perception of commercial VPNs, so using a real VPN provides you with plausible deniability, e.g. "I was just using it to watch Netflix," etc.

### L'utilizzo di Tor non è irrivelabile

**Even if you use bridges and pluggable transports,** the Tor Project provides no tools to hide the fact that you are using Tor from your ISP. Even using obfuscated "pluggable transports" or non-public bridges do not hide the fact that you are using a private communications channel. The most popular pluggable transports like obfs4 (which obfuscates your traffic to "look like nothing") and meek (which uses domain fronting to camouflage your traffic) can be [detected](https://www.hackerfactor.com/blog/index.php?/archives/889-Tor-0day-Burning-Bridges.html) with fairly standard traffic analysis techniques. Snowflake has similar issues, and can be [easily detected](https://www.hackerfactor.com/blog/index.php?/archives/944-Tor-0day-Snowflake.html) *before* a Tor connection is even established.

Pluggable transports other than these three do exist, but typically rely on security through obscurity to evade detection. They aren't impossible to detect, they are just used by so few people that it's not worth the effort building detectors for them. They shouldn't be relied upon if you specifically are being monitored.

It is critical to understand the difference between bypassing censorship and evading detection. It is easier to accomplish the former because of the many real-world limitations on what network censors can realistically do en masse, but these techniques do not hide the fact that you—*specifically* you—are using Tor from an interested party monitoring your network.

### Tor Browser is not the most *secure* browser

Anonymity can often be at odds with security: Tor's anonymity requires every user to be identical, which creates a monoculture (the same bugs are present across all Tor Browser users). As a cybersecurity rule of thumb, monocultures are generally regarded as bad: Security through diversity (which Tor lacks) provides natural segmentation by limiting vulnerabilities to smaller groups, and is therefore usually desirable, but this diversity is also less good for anonymity.

Additionally, Tor Browser is based on Firefox's Extended Support Release builds, which only receives patches for vulnerabilities considered *Critical* and *High* (not *Medium* and *Low*). This means that attackers could (for example):

1. Look for new Critical/High vulnerabilities in Firefox nightly or beta builds, then check if they are exploitable in Tor Browser (this vulnerability period can last weeks).
2. Chain *multiple* Medium/Low vulnerabilities together until they get the level of access they're looking for (this vulnerability period can last months or longer).

Those at risk of browser vulnerabilities should consider additional protections to defend against Tor Browser exploits, such as using Whonix in [Qubes](../os/qubes-overview.md) to contain your Tor browsing in a secure VM and protect against leaks.

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

Tor consente di connetterci a un server senza che alcuna signola parte conosca l'intero percorso. Il nodo d'accesso sa chi sei, ma non dove stai andando; il nodo intermedio non sa chi sei, né dove stai andando; il nodo d'uscita sa dove stai andando, ma non chi sei. Poiché il nodo d'uscita è quello che effettua la connessione finale, il server di destinazione non conoscerà il tuo indirizzo IP.

## Avvertenze

Sebbene Tor fornisca forti garanzie per la privacy, devi essere consapevole che Tor non è perfetto:

- Tor never protects you from exposing yourself by mistake, such as if you share too much information about your real identity.
- Tor exit nodes can **modify** unencrypted traffic which passes through them. This means traffic which is not encrypted, such as plain HTTP traffic, can be changed by a malicious exit node. **Never** download files from an unencrypted `http://` website over Tor, and ensure your browser is set to always upgrade HTTP traffic to HTTPS.
- I nodi d'uscita di Tor, inoltre, possono monitorare il traffico che li attraversa. Unencrypted traffic which contains personally identifiable information can deanonymize you to that exit node. Again, we recommend only using HTTPS over Tor.
- Powerful adversaries with the capability to passively watch *all* network traffic around the globe ("Global Passive Adversaries") are **not** something that Tor protects you against (and using Tor [with a VPN](#safely-connecting-to-tor) doesn't change this fact).
- Well-funded adversaries with the capability to passively watch *most* network traffic around the globe still have a *chance* of deanonymizing Tor users by means of advanced traffic analysis.

Se desideri utilizzare Tor per navigare sul web, consigliamo soltanto il Tor Browser **ufficiale**, progettato per evitare il fingerprinting.

- [Tor Browser :material-arrow-right-drop-circle:](../tor.md#tor-browser)

### Protections provided by bridges

Tor bridges are commonly touted as an alternative method to hiding Tor usage from an ISP, instead of a VPN (as we suggest using if possible). Something to consider is that while bridges may provide adequate censorship circumvention, this is only a *transient* benefit. They do not adequately protect you from your ISP discovering you connected to Tor in the *past* with historical traffic log analysis.

To illustrate this point, consider the following scenario: You connect to Tor via a bridge, and your ISP doesn’t detect it because they are not doing sophisticated analysis of your traffic, so things are working as intended. Now, 4 months go by, and the IP of your bridge has been made public. This is a very common occurrence with bridges, they are discovered and blocked relatively frequently, just not immediately.

Your ISP wants to identify Tor users 4 months ago, and with their limited metadata logging they can see that you connected to an IP address which was later revealed to be a Tor bridge. You have virtually no other excuse to be making such a connection, so the ISP can say with very high confidence that you were a Tor user at that time.

Contrast this with our recommended scenario, where you connect to Tor via a VPN. Say that 4 months later your ISP again wants to identify anybody who used Tor 4 months ago. Their logs almost certainly can identify your traffic 4 months ago, but all they would likely be able to see is that you connected to a VPN’s IP address. This is because most ISPs only retain metadata over long periods of time, not the full contents of the traffic you request. Storing the entirety of your traffic data would require a massive quantity of storage which nearly all threat actors wouldn't possess.

Because your ISP almost certainly is not capturing all packet-level data and storing it forever, they have no way of determining what you connected to with that VPN *after* the fact with an advanced technique like deep packet inspection, and therefore you have plausible deniability.

Therefore, bridges provide the most benefit when circumventing internet censorship *in the moment*, but they are not an adequate substitute for **all** the benefits that using a VPN alongside Tor can provide. Again, this is not advice *against* using Tor bridges, you should just be aware of these limitations while making your decision. In some cases bridges may be the *only* option (if all VPN providers are blocked, for instance), so you can still use them in those circumstances with this limitation in mind.

If you think that a bridge can aid in defending against fingerprinting or other advanced network analysis more than a VPN's encrypted tunnel already can, you always have the option to use a bridge in conjunction with a VPN as well. That way you are still protected by the pluggable transport's obfuscation techniques even if an adversary gains some level of visibility into your VPN tunnel. If you decide to go this route, we recommend connecting to an obfs4 bridge behind your VPN for optimal fingerprinting protection, rather than meek or Snowflake.

It is [possible](https://discuss.privacyguides.net/t/clarify-tors-weaknesses-with-respect-to-observability/3676/16) that the [WebTunnel](https://forum.torproject.org/t/tor-relays-announcement-webtunnel-a-new-pluggable-transport-for-bridges-now-available-for-deployment/8180) pluggable transport currently being trialed may mitigate some of these concerns. We will continue to keep an eye on that technology as it develops.

## Risorse aggiuntive

- [Manuale Utente del Tor Browser](https://tb-manual.torproject.org)
- [Come funziona Tor - Computerphile](https://invidious.privacyguides.net/embed/QRYzre4bf7I?local=true) <small>(YouTube)</small>
- [Servizi Onion di Tor - Computerphile](https://invidious.privacyguides.net/embed/lVcbq_a5N9I?local=true) <small>(YouTube)</small>

[^1]: Il primo relay nel tuo circuito è detto "guardia d'accesso" o "guardia". È un relay veloce e stabile che rimane il primo nel tuo circuito per 2-3 mesi, per proteggerti da attacchi di deanonimizzazione noti. Il resto del tuo circuito cambia a ogni nuovo sito web che visiti e, tutti insieme, questi relay, forniscono la completa protezione della privacy di Tor. Per ulteriori informazioni sul funzionamento dei relay di guardia, consulta questo [post del blog](https://blog.torproject.org/improving-tors-anonymity-changing-guard-parameters) e il [documento](https://www-users.cs.umn.edu/~hoppernj/single_guard.pdf) sulle guardie d'accesso. ([https://support.torproject.org/tbb/tbb-2/](https://support.torproject.org/tbb/tbb-2/))

[^2]: Flag dei relay: una (s-)qualificazione speciale per le posizioni dei circuiti (ad esempio, "Guardia", "Uscita", "BadExit"), proprietà dei circuiti (ad esempio, "Veloce", "Stabile"), o ruoli (ad esempio, "Autorità", "HSDir"), come assegnato dalle autorità direttorie, e ulteriormente definito nelle specifiche del protocollo direttorio. ([https://metrics.torproject.org/glossary.html](https://metrics.torproject.org/glossary.html))
