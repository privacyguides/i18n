---
meta_title: "Come le VPN proteggono la tua privacy? La nostra panoramica sulle VPN - Privacy Guides"
title: Panoramica VPN
icon: material/vpn
description: Le reti virtuali private spostano il rischio dal vostro ISP a una terza parte di cui vi fidate. Dovresti tenere a mente questi aspetti.
---

Virtual Private Networks are a way of extending the end of your network to exit somewhere else in the world.

Normally, an ISP can see the flow of internet traffic entering and exiting your network termination device (i.e. modem). Encryption protocols such as HTTPS are commonly used on the internet, so they may not be able to see exactly what you're posting or reading, but they can get an idea of the [domains you request](../advanced/dns-overview.md#why-shouldnt-i-use-encrypted-dns).

Using a VPN hides even this information from your ISP, by shifting the trust you place in your network to a server somewhere else in the world. As a result, the ISP then only sees that you are connected to a VPN and nothing about the activity that you're passing through it.

!!! note "Nota"

    When we refer to "Virtual Private Networks" on this website, we are usually referring to **commercial** [VPN providers](../vpn.md), who you pay a monthly fee to in exchange for routing your internet traffic securely through their public servers. There are many other forms of VPN, such as ones you host yourself or ones operated by workplaces which allow you to securely connect to internal/employee network resources, however, these VPNs are usually designed for accessing remote networks securely, rather than protecting the privacy of your internet connection.

## Come funziona una VPN?

Le VPN criptano il tuo traffico tra il tuo dispositivo e un server di proprietà del tuo fornitore VPN. Dal punto di vista di chiunque si trovi tra te e il server VPN, sembra che ti stia connettendo al server VPN. Dal punto di vista di chiunque si trovi tra il server VPN e il tuo sito di destinazione, tutto ciò che può vedere è il server VPN che si connette al sito web.

``` mermaid
flowchart LR
 763931["Your Device<div>(with VPN Client)</div>"] ===|"VPN Encryption"| 404512{"VPN Server"}
 404512 -.-|"No VPN Encryption"| 593753((("The Internet\n(Your Destination)")))
 subgraph 763931["Your Device<div>(with VPN Client)</div>"]
 end
```

Note that a VPN does not add any security or encryption to your traffic between the VPN server and your destination on the internet. To access a website securely you **must** still ensure HTTPS is in use regardless of whether you use a VPN.

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

Unless your VPN provider hosts the encrypted DNS servers themselves, **probably not**. Using DOH/DOT (or any other form of encrypted DNS) with third-party servers will simply add more entities to trust. Il tuo fornitore VPN può comunque vedere quali siti web visiti in base agli indirizzi IP e ad altri metodi. All this being said, there may be some advantages to enabling encrypted DNS in order to enable other security features in your browser, such as ECH. Browser technologies which are reliant on in-browser encrypted DNS are relatively new and not yet widespread, so whether they are relevant to you in particular is an exercise we will leave to you to research independently.

Another common reason encrypted DNS is recommended is that it prevents DNS spoofing. Tuttavia, il browser dovrebbe già verificare la presenza di [certificati TLS](https://en.wikipedia.org/wiki/Transport_Layer_Security#Digital_certificates) con **HTTPS** e avvisare l'utente. Se non stai utilizzando **HTTPS**, un avversario può comunque modificare qualsiasi cosa oltre alle query DNS e il risultato finale sarà poco diverso.

## Dovrei usare Tor *e* una VPN?

Maybe, Tor is not necessarily suitable for everybody in the first place. Consider your [threat model](threat-modeling.md), because if your adversary is not capable of extracting information from your VPN provider, using a VPN alone may provide enough protection.

If you do use Tor then you are *probably* best off connecting to the Tor network via a commercial VPN provider. However, this is a complex subject which we've written more about on our [Tor overview](../advanced/tor-overview.md) page.

## Should I access Tor through VPN providers that provide "Tor nodes"?

You should not use that feature: The primary advantage of using Tor is that you do not trust your VPN provider, which is negated when you use Tor nodes hosted by your VPN instead of connecting directly to Tor from your computer.

Currently, Tor only supports the TCP protocol. UDP (used by [WebRTC](https://en.wikipedia.org/wiki/WebRTC), [HTTP3/QUIC](https://en.wikipedia.org/wiki/HTTP/3), and other protocols), [ICMP](https://en.wikipedia.org/wiki/Internet_Control_Message_Protocol), and other packets will be dropped. Per compensare questa situazione, i fornitori di VPN di solito instradano tutti i pacchetti non-TCP attraverso il loro server VPN (il primo hop). Questo è il caso di [ProtonVPN](https://protonvpn.com/support/tor-vpn/). Inoltre, quando si utilizza questa configurazione di Tor su VPN, non si ha il controllo su altre importanti funzionalità di Tor come [Isolated Destination Address](https://www.whonix.org/wiki/Stream_Isolation) (utilizzo di un circuito Tor diverso per ogni dominio visitato).

The feature should be viewed as a *convenient* way to access hidden services on Tor, not to stay anonymous. For proper anonymity, use the actual [Tor Browser](../tor.md).

## Commercial VPN Ownership

Most VPN services are owned by the same [few companies](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies/). These shady companies run lots of smaller VPN services to create the illusion that you have more choice than you actually do and to maximize profit. Typically, these providers that feed into their shell company have terrible privacy policies and shouldn't be trusted with your internet traffic. You should be very strict about which provider you decide to use.

You should also be wary that many VPN review sites are merely advertising vehicles open to the highest bidder. ==Privacy Guides does not make money from recommending external products, and never uses affiliate programs.==

[Our VPN Recommendations](../vpn.md ""){.md-button}

## Alternative VPN Moderne

Recently, some attempts have been made by various organizations to address some issues which centralized VPNs have. These technologies are relatively new, but worth keeping an eye on as the field develops.

### Multi-Party Relays

Multi-Party Relays (MPRs) use multiple nodes owned by different parties, such that no individual party knows both who you are and what you're connecting to. This is the basic idea behind Tor, but now there are some paid services that try to emulate this model.

MPRs seek to solve a problem inherent to VPNs: the fact that you must trust them completely. They accomplish this goal by segmenting the responsibilities between two or more different companies. For example, Apple's iCloud+ Private Relay routes your traffic through two servers:

1. Firstly, a server operated by Apple.

    This server is able to see your device's IP when you connect to it, and has knowledge of your payment information and Apple ID tied to your iCloud subscription. However, it is unable to see what website you are connecting to.

2. Secondly, a server operated by a partner CDN, such as Cloudflare or Fastly.

    This server actually makes the connection to your destination website, but has no knowledge of your device. The only IP address it knows about is Apple's server's.

Other MPRs run by different companies like Google or INVISV operate in a very similar manner. This protection by segmentation only exists if you trust the two companies to not collude with each other to deanonymize you.

### VPN Decentralizzate

Another attempt at solving the issues with centralized VPN services are dVPNs. These are based on blockchain technology and claim to eliminate trust in a single party by distributing the nodes across lots of different people. However, many times a dVPN will default to a single node, meaning you need to trust that node completely, just like a traditional VPN. Unlike a traditional VPN, this one node that can see all your traffic is a random person instead of your VPN provider that can be audited and has legal responsibilities to uphold their privacy policy. Multi-hop is needed to solve this, but that comes with a stability and performance cost.

Another consideration is legal liability. The exit node will need to deal with legal problems from misuse of the network, an issue that the Tor network has contended with for its entire existence. This discourages regular people from running nodes and makes it more attractive for a malicious actor with lots of resources to host one. This is a big problem if the service is single-node, as the potentially malicious exit node can see who you are and what you're connecting to.

Many dVPNs are used to push a cryptocurrency rather than to make the best service. They also tend to be smaller networks with fewer nodes, making them more vulnerable to [Sybil attacks](https://en.wikipedia.org/wiki/Sybil_attack).

## Informazioni correlate alle VPN

- [The Trouble with VPN and Privacy Review Sites (Il problema dei siti di recensioni di VPN e privacy)](https://blog.privacyguides.org/2019/11/20/the-trouble-with-vpn-and-privacy-review-sites/)
- [Free VPN App Investigation (Indagine sulle app di VPN gratuite)](https://www.top10vpn.com/free-vpn-app-investigation/)
- [Hidden VPN owners unveiled: 101 VPN products run by just 23 companies (Svelati i proprietari segreti delle VPN: 101 prodotti per VPN gestiti da sole 23 aziende)](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies/)
- [This Chinese company is secretly behind 24 popular apps seeking dangerous permissions (Questa azienda cinese è segretamente dietro 24 app popolari che cercano autorizzazioni pericolose)](https://vpnpro.com/blog/chinese-company-secretly-behind-popular-apps-seeking-dangerous-permissions/)
- [VPN - a Very Precarious Narrative (VPN - una narrazione molto precaria)](https://schub.io/blog/2019/04/08/very-precarious-narrative.html) di Dennis Schubert
