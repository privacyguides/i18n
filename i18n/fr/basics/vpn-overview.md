---
meta_title: "Comment les VPNs protègent-ils votre vie privée ? Notre introduction aux VPNs - Privacy Guides"
title: Introduction aux VPNs
icon: material/vpn
description: Les réseaux privés virtuels déplacent le risque de votre FAI à un tiers en qui vous avez confiance. Vous devriez garder ces éléments à l'esprit.
---

Les Réseaux Privés Virtuels sont un moyen d'étendre l'extrémité de votre réseau avec une sortie située ailleurs dans le monde.

Normalement, un FAI peut voir le flux de trafic internet qui entre et sort de votre dispositif de terminaison de réseau (c'est-à-dire votre box/modem). Les protocoles de chiffrement tels que HTTPS sont couramment utilisés sur internet, ils se peut donc qu'ils ne soient pas en mesure de voir exactement ce que vous publiez ou lisez, mais ils peuvent avoir une idée [des domaines que vous visitez](../advanced/dns-overview.md#why-shouldnt-i-use-encrypted-dns).

L'utilisation d'un VPN permet de dissimuler ces informations à votre FAI, en transférant la confiance que vous accordez à votre réseau vers un serveur situé ailleurs dans le monde. Par conséquent, le FAI ne voit que le fait que vous êtes connecté à un VPN et rien sur l'activité que vous lui transmettez.

!!! note "À noter"

    Lorsque nous faisons référence aux "Réseaux Privés Virtuels" sur ce site, nous faisons généralement référence à [des fournisseurs VPN](.. vpn.md) **commerciaux**, à qui vous payez des frais mensuels en échange de l'acheminement sécurisé de votre trafic Internet à travers leurs serveurs publics. Il existe de nombreuses autres formes de VPN, tels que ceux que vous hébergez vous-même ou ceux gérés par des lieux de travail qui vous permettent de vous connecter en toute sécurité à des ressources réseau internes/employés, Cependant, ces VPNs sont généralement conçus pour accéder à des réseaux distants en toute sécurité, plutôt que pour protéger la confidentialité de votre connexion Internet.

## Comment fonctionne un VPN ?

Les VPNs chiffrent votre trafic entre votre appareil et un serveur appartenant à votre fournisseur VPN. Du point de vue de n'importe qui entre vous et le serveur VPN, il semble que vous vous connectiez au serveur VPN. Du point de vue de n'importe qui entre le serveur VPN et votre site de destination, tout ce qu'il peut voir est le serveur VPN se connectant au site Web.

``` mermaid
flowchart LR
 763931["Votre appareil<div>(avec client VPN)</div>"] ===|"chiffrement VPN"| 404512{"serveur VPN"}
 404512 -.-|"pas de chiffrement VPN"| 593753((("Internet\n(votre destination)")))
 subgraph 763931["Votre appareil<div>(avec client VPN)</div>"]
 end
```

Notez qu'un VPN n'ajoute pas de sécurité ou de chiffrement à votre trafic entre le serveur VPN et votre destination sur Internet. Pour accéder à un site Web en toute sécurité vous **devez** toujours vous assurer que HTTPS est utilisé, que vous utilisiez ou non un VPN.

## Dois-je utiliser un VPN ?

**Oui**, presque certainement. Un VPN a de nombreux avantages, y compris :

1. Cacher votre trafic de **seulement** votre Fournisseur d'Accès Internet.
1. Cacher vos téléchargements (tels que les torrents) à votre FAI et aux organisations anti-piratage.
1. Cacher votre adresse IP des sites et services tiers, et ce faisant vous aider à vous fondre dans le traffic et à prévenir le suivi basé sur l'adresse IP.
1. Permettre de contourner les restrictions géographiques sur certains contenus.

Les VPNs peuvent fournir *certains* des mêmes avantages fournis par Tor, comme cacher votre adresse IP aux sites Web que vous visitez et déplacer géographiquement votre trafic réseau, et de bons fournisseurs VPN ne coopéreront pas, par exemple avec les autorités légales de régimes oppressifs, en particulier si vous choisissez un fournisseur VPN hors de votre juridiction.

Les VPN ne peuvent pas chiffrer les données en dehors de la connexion entre votre appareil et le serveur VPN. Les fournisseurs de VPN peuvent également voir et modifier votre trafic de la même manière que pourrait le faire votre FAI, il y a donc encore un niveau de confiance que vous leur accordez. Et il n'existe aucun moyen de vérifier de quelque manière que ce soit la politique de "non journalisation" d'un fournisseur de VPN.

## Quand un VPN ne convient-il pas ?

L'utilisation d'un VPN dans les cas où vous utilisez votre [identité réelle ou connue](common-misconceptions.md#complicated-is-better) ne sera probablement pas utile. Cela peut déclencher des systèmes de détection de spam et de fraude, par exemple si vous vous connectez au site web de votre banque.

Il est important de se rappeler qu'un VPN ne vous procurera pas un anonymat absolu, car le fournisseur de VPN lui-même verra toujours votre adresse IP réelle, des informations sur le site Web de destination, et a souvent une trace financière qui peut être remontée directement jusqu'à vous. You can't rely on "no logging" policies to protect your data from anyone who is able to protect. Si vous avez besoin d'une protection complète du réseau lui-même, envisagez d'utiliser [Tor](../advanced/tor-overview.md) en plus ou au lieu d'un VPN.

Vous ne devriez pas non plus faire confiance à un VPN pour sécuriser votre connexion à une destination HTTP non chiffrée. Pour que ce que vous faites sur les sites web que vous visitez reste privé et sécurisé, vous devez utiliser le protocole HTTPS. Cela conservera vos mots de passe, jetons de session, et les requêtes à l'abri du fournisseur VPN et d'autres adversaires potentiels entre le serveur VPN et votre destination. Vous devriez activer le mode HTTPS-uniquement dans votre navigateur (s'il est pris en charge) pour atténuer les attaques qui tentent de rétrograder votre connexion de HTTPS à HTTP.

## Devrais-je utiliser un DNS chiffré avec un VPN ?

À moins que votre fournisseur VPN n'héberge les serveurs DNS chiffrés lui-même, **probablement que non**. L'utilisation du DOH/DOT (ou de toute autre forme de DNS chiffrés) avec des serveurs tiers ajoutera simplement plus d'entités à qui faire confiance. Votre fournisseur de VPN peut toujours voir quels sites web vous visitez en se basant sur les adresses IP et d'autres méthodes. Cela étant dit, il peut y avoir certains avantages à activer le DNS chiffré afin d'activer d'autres fonctionnalités de sécurité dans votre navigateur, comme ECH. Browser technologies which are reliant on in-browser encrypted DNS are relatively new and not yet widespread, so whether they are relevant to you in particular is an exercise we will leave to you to research independently.

Another common reason encrypted DNS is recommended is that it prevents DNS spoofing. Cependant, votre navigateur devrait déjà vérifier la présence de [certificats TLS](https://en.wikipedia.org/wiki/Transport_Layer_Security#Digital_certificates) avec **HTTPS** et vous en avertir. Si vous n'utilisez pas **HTTPS**, alors un adversaire peut toujours modifier n'importe quoi d'autre que vos requêtes DNS et le résultat final sera peu différent.

## Devrais-je utiliser Tor *et* un VPN?

Maybe, Tor is not necessarily suitable for everybody in the first place. Consider your [threat model](threat-modeling.md), because if your adversary is not capable of extracting information from your VPN provider, using a VPN alone may provide enough protection.

If you do use Tor then you are *probably* best off connecting to the Tor network via a commercial VPN provider. However, this is a complex subject which we've written more about on our [Tor overview](../advanced/tor-overview.md) page.

## Should I access Tor through VPN providers that provide "Tor nodes"?

You should not use that feature: The primary advantage of using Tor is that you do not trust your VPN provider, which is negated when you use Tor nodes hosted by your VPN instead of connecting directly to Tor from your computer.

Actuellement, Tor supporte seulement le protocole TCP. UDP (used by [WebRTC](https://en.wikipedia.org/wiki/WebRTC), [HTTP3/QUIC](https://en.wikipedia.org/wiki/HTTP/3), and other protocols), [ICMP](https://en.wikipedia.org/wiki/Internet_Control_Message_Protocol), and other packets will be dropped. Pour compenser cela, les fournisseurs de VPN acheminent généralement tous les paquets non TCP par leur serveur VPN (votre premier saut). C'est le cas de [Proton VPN](https://protonvpn.com/support/tor-vpn/). De plus, lorsque vous utilisez cette configuration Tor par VPN, vous n'avez pas le contrôle sur d'autres fonctionnalités importantes de Tor telles que [Adresse de Destination Isolée](https://www.whonix.org/wiki/Stream_Isolation) (utilisation d'un circuit Tor différent pour chaque domaine que vous visitez).

The feature should be viewed as a *convenient* way to access hidden services on Tor, not to stay anonymous. For proper anonymity, use the actual [Tor Browser](../tor.md).

## Commercial VPN Ownership

Most VPN services are owned by the same [few companies](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies/). These shady companies run lots of smaller VPN services to create the illusion that you have more choice than you actually do and to maximize profit. Typically, these providers that feed into their shell company have terrible privacy policies and shouldn't be trusted with your internet traffic. You should be very strict about which provider you decide to use.

You should also be wary that many VPN review sites are merely advertising vehicles open to the highest bidder. ==Privacy Guides does not make money from recommending external products, and never uses affiliate programs.==

[Nos recommandations VPN](../vpn.md ""){.md-button}

## Alternatives VPN modernes

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

## Informations VPN liées

- [Le problème avec les sites d'évaluation des VPNs et de la vie privée](https://blog.privacyguides.org/2019/11/20/the-trouble-with-vpn-and-privacy-review-sites/)
- [Enquête sur les applications VPN gratuites](https://www.top10vpn.com/free-vpn-app-investigation/)
- [Les propriétaires inconnus des VPNs dévoilés : 101 produits VPN gérés par seulement 23 sociétés](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies/)
- [Cette société chinoise est secrètement à l'origine de 24 applications populaires qui cherchent à obtenir des autorisations dangereuses](https://vpnpro.com/blog/chinese-company-secretly-behind-popular-apps-seeking-dangerous-permissions/)
- [VPN - un récit très précaire](https://schub.io/blog/2019/04/08/very-precarious-narrative.html) par Dennis Schubert
