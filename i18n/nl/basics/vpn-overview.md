---
meta_title: "Hoe beschermen VPN's je privacy? Ons VPN-overzicht - Privacy Guides"
title: VPN-overzicht
icon: material/vpn
description: Virtual Private Networks verschuiven het risico van je ISP naar een derde partij die je vertrouwt. Je moet deze dingen in het achterhoofd houden.
---

Virtual Private Networks zijn een manier om het einde van je netwerk uit te breiden naar een uitgang ergens anders in de wereld.

[:material-movie-open-play-outline: Video: Do you need a VPN?](https://www.privacyguides.org/videos/2024/12/12/do-you-need-a-vpn/ ""){.md-button}

Normaal gesproken kan een ISP de stroom internetverkeer zien die je netwerkapparaat (d.w.z. modem) binnenkomt en verlaat. Versleutelingsprotocollen zoals HTTPS worden vaak gebruikt op het internet, dus ze kunnen misschien niet precies zien wat je post of leest, maar ze kunnen wel een idee krijgen van de [domeinen die je opvraagt](../advanced/dns-overview.md#why-shouldnt-i-use-encrypted-dns).

Het gebruik van een VPN verbergt zelfs deze informatie voor je ISP, door het vertrouwen dat je in je netwerk stelt te verplaatsen naar een server ergens anders in de wereld. Hierdoor ziet de ISP alleen dat je verbonden bent met een VPN en niets over de activiteit die je er doorheen stuurt.

<div class="admonition note" markdown>
<p class="admonition-title">Opmerking</p>

Wanneer we op deze website verwijzen naar "Virtual Private Networks", bedoelen we meestal **commerciële** [VPN-providers](../vpn.md), aan wie je een maandelijks bedrag betaalt in ruil voor het veilig routeren van je internetverkeer via hun openbare servers. Er zijn vele andere vormen van VPN, zoals VPN's die je zelf host of VPN's die worden beheerd door werkplekken en waarmee je veilig verbinding kunt maken met interne/werknemersnetwerkbronnen, maar deze VPN's zijn meestal ontworpen voor veilige toegang tot externe netwerken, in plaats van voor het beschermen van de privacy van je internetverbinding.

</div>

## Hoe werkt een VPN?

VPN's versleutelen je verkeer tussen je apparaat en een server van je VPN-aanbieder. Vanuit het perspectief van eenieder die zich tussen jou en de VPN-server bevindt, lijkt het alsof je verbinding maakt met de VPN-server. Vanuit het perspectief van eenieder die zich tussen de VPN-server en uw bestemmingssite bevindt, is het enige wat ze kunnen zien de VPN-server die verbinding maakt met de website.

``` mermaid
flowchart LR
 763931["Your Device<div>(with VPN Client)</div>"] ===|"VPN Encryption"| 404512{"VPN Server"}
 404512 -.-|"No VPN Encryption"| 593753(("The Internet<div>(Your Destination)</div>"))
 subgraph 763931["Your Device<div>(with VPN Client)</div>"]
 end
```

Houd er rekening mee dat een VPN geen beveiliging of versleuteling toevoegt aan je verkeer tussen de VPN-server en je bestemming op het internet. Om veilig naar een website te gaan, **moet** je er nog steeds voor zorgen dat HTTPS wordt gebruikt, ongeacht of je een VPN gebruikt of niet.

## Moet ik een VPN gebruiken?

**Ja**, vrijwel zeker. Een VPN gebruiken heeft veel voordelen, waaronder:

1. Het verbergen van jouw verkeer van **is alleen** jouw Internet Service Provider.
1. Het verbergen van je downloads (zoals torrents) voor je ISP en anti-piraterij organisaties.
1. Je IP-adres verbergen voor websites en services van derden, zodat je opgaat in het verkeer van anderen en tracking op basis van je IP-adres wordt voorkomen.
1. Je kunt locatiegebonden restricties om bepaalde content te bekijken omzeilen.

VPNs can provide *some* of the same benefits Tor provides, such as hiding your IP from the websites you visit and geographically shifting your network traffic, and good VPN providers will not cooperate with e.g. legal authorities from oppressive regimes, especially if you choose a VPN provider outside your own jurisdiction.

VPN kunnen dataverkeer tussen jouw apparaat en de VPN-server niet versleutelen. VPN-aanbieders kunnen het verkeer inspecteren en veranderen net als een internetprovider dat kan. Daarom moet je dus kunnen vertrouwen op de aanbieder van de VPN. En er is geen enkele manier om het "no logging" beleid van een VPN provider te verifiëren.

## Wanneer is een VPN geen geschikte keuze?

Using a VPN in cases where you're using your [real-life or well-known identity](common-misconceptions.md#complicated-is-better) online is unlikely to be useful. Dit kan spam- en fraudedetectiesystemen alarmeren, zoals wanneer je zou inloggen op de website van uw bank.

It's important to remember that a VPN will not provide you with absolute anonymity because the VPN provider itself will still have access to your real IP address, destination website information, and often a money trail that can be linked directly back to you. "No logging" policies are merely a promise; if you need complete safety from the network itself, consider using [Tor](../advanced/tor-overview.md) in addition to or instead of a VPN.

You also should not trust a VPN to secure your connection to an unencrypted, HTTP destination. Om wat je doet op de websites die je bezoekt privé en veilig te houden, moet je HTTPS gebruiken. This will keep your passwords, session tokens, and queries safe from the VPN provider and other potential adversaries in between the VPN server and your destination. You should enable HTTPS-only mode in your browser (if it's supported) to mitigate attacks which try to downgrade your connection from HTTPS to HTTP.

## Moet ik versleutelde DNS gebruiken met een VPN?

Unless your VPN provider hosts the encrypted DNS servers themselves, **probably not**. Using DOH/DOT (or any other form of encrypted DNS) with third-party servers will simply add more entities to trust. Jouw VPN-provider kan nog steeds zien welke websites je bezoekt op basis van de IP-adressen en andere methoden. All this being said, there may be some advantages to enabling encrypted DNS in order to enable other security features in your browser, such as ECH. Browser technologies which are reliant on in-browser encrypted DNS are relatively new and not yet widespread, so whether they are relevant to you in particular is an exercise we will leave to you to research independently.

Another common reason encrypted DNS is recommended is that it prevents DNS spoofing. Jouw browser zou echter al moeten controleren op [TLS-certificaten](https://en.wikipedia.org/wiki/Transport_Layer_Security#Digital_certificates) met **HTTPS** en je daarvoor moeten waarschuwen. Als je **HTTPS** niet gebruikt, dan kan een tegenstander nog steeds gewoon iets anders dan jouw DNS-query's wijzigen en zal het eindresultaat weinig anders zijn.

## Moet ik Tor *gebruiken en* een VPN?

Maybe, Tor is not necessarily suitable for everybody in the first place. Consider your [threat model](threat-modeling.md), because if your adversary is not capable of extracting information from your VPN provider, using a VPN alone may provide enough protection.

If you do use Tor then you are *probably* best off connecting to the Tor network via a commercial VPN provider. However, this is a complex subject which we've written more about on our [Tor overview](../advanced/tor-overview.md) page.

## Should I access Tor through VPN providers that provide "Tor nodes"?

You should not use that feature: The primary advantage of using Tor is that you do not trust your VPN provider, which is negated when you use Tor nodes hosted by your VPN instead of connecting directly to Tor from your computer.

Currently, Tor only supports the TCP protocol. UDP (used by [WebRTC](https://en.wikipedia.org/wiki/WebRTC), [HTTP3/QUIC](https://en.wikipedia.org/wiki/HTTP/3), and other protocols), [ICMP](https://en.wikipedia.org/wiki/Internet_Control_Message_Protocol), and other packets will be dropped. Om dit te compenseren, routeren VPN-aanbieders gewoonlijk alle niet-TCP-pakketten via hun VPN-server (je eerste hop). This is the case with [ProtonVPN](https://protonvpn.com/support/tor-vpn). Additionally, when using this Tor over VPN setup, you do not have control over other important Tor features such as [Isolated Destination Address](https://whonix.org/wiki/Stream_Isolation) (using a different Tor circuit for every domain you visit).

The feature should be viewed as a *convenient* way to access hidden services on Tor, not to stay anonymous. For proper anonymity, use the actual [Tor Browser](../tor.md).

## Commercial VPN Ownership

Most VPN services are owned by the same [few companies](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies). These shady companies run lots of smaller VPN services to create the illusion that you have more choice than you actually do and to maximize profit. Typically, these providers that feed into their shell company have terrible privacy policies and shouldn't be trusted with your internet traffic. You should be very strict about which provider you decide to use.

You should also be wary that many VPN review sites are merely advertising vehicles open to the highest bidder. ==Privacy Guides does not make money from recommending external products, and never uses affiliate programs.==

[Our VPN Recommendations](../vpn.md ""){.md-button}

## Modern VPN Alternatives

Recently, some attempts have been made by various organizations to address some issues which centralized VPNs have. These technologies are relatively new, but worth keeping an eye on as the field develops.

### Multi-Party Relays

Multi-Party Relays (MPRs) use multiple nodes owned by different parties, such that no individual party knows both who you are and what you're connecting to. This is the basic idea behind Tor, but now there are some paid services that try to emulate this model.

MPRs seek to solve a problem inherent to VPNs: the fact that you must trust them completely. They accomplish this goal by segmenting the responsibilities between two or more different companies. For example, Apple's iCloud+ Private Relay routes your traffic through two servers:

1. Firstly, a server operated by Apple.

    This server is able to see your device's IP when you connect to it, and has knowledge of your payment information and Apple ID tied to your iCloud subscription. However, it is unable to see what website you are connecting to.

2. Secondly, a server operated by a partner CDN, such as Cloudflare or Fastly.

    This server actually makes the connection to your destination website, but has no knowledge of your device. The only IP address it knows about is Apple's server's.

Other MPRs run by different companies like Google or INVISV operate in a very similar manner. This protection by segmentation only exists if you trust the two companies to not collude with each other to deanonymize you.

### Decentralized VPNs

Another attempt at solving the issues with centralized VPN services are dVPNs. These are based on blockchain technology and claim to eliminate trust in a single party by distributing the nodes across lots of different people. However, many times a dVPN will default to a single node, meaning you need to trust that node completely, just like a traditional VPN. Unlike a traditional VPN, this one node that can see all your traffic is a random person instead of your VPN provider that can be audited and has legal responsibilities to uphold their privacy policy. Multi-hop is needed to solve this, but that comes with a stability and performance cost.

Another consideration is legal liability. The exit node will need to deal with legal problems from misuse of the network, an issue that the Tor network has contended with for its entire existence. This discourages regular people from running nodes and makes it more attractive for a malicious actor with lots of resources to host one. This is a big problem if the service is single-node, as the potentially malicious exit node can see who you are and what you're connecting to.

Many dVPNs are used to push a cryptocurrency rather than to make the best service. They also tend to be smaller networks with fewer nodes, making them more vulnerable to [Sybil attacks](https://en.wikipedia.org/wiki/Sybil_attack).

## Verwante VPN-informatie

- [Het probleem met VPN- en privacybeoordelingssites](https://blog.privacyguides.org/2019/11/20/the-trouble-with-vpn-and-privacy-review-sites)
- [Gratis VPN-app onderzoek](https://top10vpn.com/research/free-vpn-investigations/ownership)
- [Verborgen VPN-eigenaars onthuld: 101 VPN-producten van slechts 23 bedrijven](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies)
- [Dit Chinese bedrijf zit in het geheim achter 24 populaire apps die gevaarlijke toestemmingen zoeken](https://vpnpro.com/blog/chinese-company-secretly-behind-popular-apps-seeking-dangerous-permissions)
- [VPN - a Very Precarious Narrative](https://overengineer.dev/blog/2019/04/08/very-precarious-narrative.html) by Dennis Schubert
