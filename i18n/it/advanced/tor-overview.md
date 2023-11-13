---
title: "Panoramica Tor"
icon: 'simple/torproject'
description: Tor è una rete decentralizzata e libera, progettata per utilizzare Internet con quanta più privacy possibile.
---

Tor è una rete decentralizzata e libera, progettata per utilizzare Internet con quanta più privacy possibile. Se utilizzata adeguatamente, la rete consente navigazione e comunicazioni private e anonime.

## Connettersi in sicurezza a Tor

Before connecting to [Tor](../tor.md), you should carefully consider what you're looking to accomplish by using Tor in the first place, and who you're trying to hide your network activity from.

If you live in a free country, are accessing mundane content via Tor, aren't worried about your ISP or local network administrators having the knowledge that you're using Tor, and want to help [de-stigmatize](https://2019.www.torproject.org/about/torusers.html.en) Tor usage, you can likely connect to Tor directly via standard means like [Tor Browser](../tor.md) without worry.

If you have the ability to access a trusted VPN provider and **any** of the following are true, you almost certainly should connect to Tor through a VPN:

- You already use a [trusted VPN provider](../vpn.md)
- Your threat model includes an adversary which is capable of extracting information from your ISP
- Your threat model includes your ISP itself as an adversary
- Your threat model includes local network administrators before your ISP as an adversary

Because we already [generally recommend](../basics/vpn-overview.md) that the vast majority of people use a trusted VPN provider for a variety of reasons, the following recommendation about connecting to Tor via a VPN likely applies to you. <mark>There is no need to disable your VPN before connecting to Tor</mark>, as some online resources would lead you to believe.

Connecting directly to Tor will make your connection stand out to any local network administrators or your ISP. Detecting and correlating this traffic [has been done](https://edition.cnn.com/2013/12/17/justice/massachusetts-harvard-hoax/) in the past by network administrators to identify and deanonymize specific Tor users on their network. On the other hand, connecting to a VPN is almost always less suspicious, because commercial VPN providers are used by everyday consumers for a variety of mundane tasks like bypassing geo-restrictions, even in countries with heavy internet restrictions.

Therefore, you should make an effort to hide your IP address **before** connecting to the Tor network. You can do this by simply connecting to a VPN (through a client installed on your computer) and then accessing [Tor](../tor.md) as normal, through Tor Browser for example. This creates a connection chain like:

- [x] Tu → VPN → Tor → Internet

From your ISP's perspective, it looks like you're accessing a VPN normally (with the associated cover that provides you). From your VPN's perspective, they can see that you are connecting to the Tor network, but nothing about what websites you're accessing. From Tor's perspective, you're connecting normally, but in the unlikely event of some sort of Tor network compromise, only your VPN's IP would be exposed, and your VPN would *additionally* have to be compromised to deanonymize you.

This is **not** censorship circumvention advice, because if Tor is blocked entirely by your ISP, your VPN likely is as well. Rather, this recommendation aims to make your traffic blend in better with commonplace VPN user traffic, and provide you with some level of plausible deniability by obscuring the fact that you're connecting to Tor from your ISP.

---

We **very strongly discourage** combining Tor with a VPN in any other manner. Do not configure your connection in a way which resembles any of the following:

- Tu → Tor → VPN → Internet
- Tu → VPN → Tor → VPN → Internet
- Qualsiasi altra configurazione

Some VPN providers and other publications will occasionally recommend these **bad** configurations to evade Tor bans (exit nodes being blocked by websites) in some places. [Normally](https://support.torproject.org/#about_change-paths), Tor frequently changes your circuit path through the network. When you choose a permanent *destination* VPN (connecting to a VPN server *after* Tor), you're eliminating this advantage and drastically harming your anonymity.

Setting up bad configurations like these is difficult to do accidentally, because it usually involves either setting up custom proxy settings inside Tor Browser, or setting up custom proxy settings inside your VPN client which routes your VPN traffic through the Tor Browser. As long as you avoid these non-default configurations, you're probably fine.

---

!!! info "VPN/SSH Fingerprinting"

    The Tor Project [notes](https://gitlab.torproject.org/legacy/trac/-/wikis/doc/TorPlusVPN#vpnssh-fingerprinting) that *theoretically* using a VPN to hide Tor activities from your ISP may not be foolproof. VPNs have been found to be vulnerable to website traffic fingerprinting, where an adversary can still guess what website is being visited, because all websites have specific traffic patterns.
    
    Therefore, it's not unreasonable to believe that encrypted Tor traffic hidden by a VPN could also be detected via similar methods. There are no research papers on this subject, and we still consider the benefits of using a VPN to far outweigh these risks, but it is something to keep in mind.
    
    If you still believe that pluggable transports (bridges) provide additional protection against website traffic fingerprinting that a VPN does not, you always have the option to use a bridge **and** a VPN in conjunction.

Determining whether you should first use a VPN to connect to the Tor network will require some common sense and knowledge of your own government's and ISP's policies relating to what you're connecting to. However, again in most cases you will be better off being seen as connecting to a commercial VPN network than directly to the Tor network. If VPN providers are censored in your area, then you can also consider using Tor pluggable transports (e.g. Snowflake or meek bridges) as an alternative, but using these bridges may arouse more suspicion than standard WireGuard/OpenVPN tunnels.

## What Tor is Not

The Tor network is not the perfect privacy protection tool in all cases, and has a number of drawbacks which should be carefully considered. These things should not discourage you from using Tor if it is appropriate for your needs, but they are still things to think about when deciding which solution is most appropriate for you.

### Tor is not a free VPN

The release of the *Orbot* mobile app has lead many people to describe Tor as a "free VPN" for all of your device traffic. However, treating Tor like this poses some dangers compared to a typical VPN.

Unlike Tor exit nodes, VPN providers are usually not *actively* [malicious](#caveats). Because Tor exit nodes can be created by anybody, they are hotspots for network logging and modification. In 2020, many Tor exit nodes were documented to be downgrading HTTPS traffic to HTTP in order to [hijack cryptocurrency transactions](https://therecord.media/thousands-of-tor-exit-nodes-attacked-cryptocurrency-users-over-the-past-year). Other exit node attacks such as replacing downloads via unencrypted channels with malware have also been observed. HTTPS does mitigate these threats to an extent.

As we've alluded to already, Tor is also easily identifiable on the network. Unlike an actual VPN provider, using Tor will make you stick out as a person likely attempting to evade authorities. In a perfect world, Tor would be seen by network administrators and authorities as a tool with many uses (like how VPNs are viewed), but in reality the perception of Tor is still far less legitimate than the perception of commercial VPNs, so using a real VPN provides you with plausible deniability, e.g. "I was just using it to watch Netflix," etc.

### Tor usage is not undetectable

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
