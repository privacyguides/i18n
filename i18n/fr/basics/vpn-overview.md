---
meta_title: "Comment les VPNs protègent-ils votre vie privée ? Notre introduction aux VPNs - Privacy Guides"
title: Introduction aux VPNs
icon: material/vpn
description: Les réseaux privés virtuels déplacent le risque de votre FAI à un tiers en qui vous avez confiance. Vous devriez garder ces éléments à l'esprit.
---

Les Réseaux Privés Virtuels sont un moyen d'étendre l'extrémité de votre réseau avec une sortie située ailleurs dans le monde.

[:material-movie-open-play-outline: Video: Do you need a VPN?](https://www.privacyguides.org/videos/2024/12/12/do-you-need-a-vpn ""){.md-button}

Normalement, un FAI peut voir le flux de trafic internet qui entre et sort de votre dispositif de terminaison de réseau (c'est-à-dire votre box/modem). Les protocoles de chiffrement tels que HTTPS sont couramment utilisés sur internet, ils se peut donc qu'ils ne soient pas en mesure de voir exactement ce que vous publiez ou lisez, mais ils peuvent avoir une idée [des domaines que vous visitez](../advanced/dns-overview.md#why-shouldnt-i-use-encrypted-dns).

L'utilisation d'un VPN permet de dissimuler ces informations à votre FAI, en transférant la confiance que vous accordez à votre réseau vers un serveur situé ailleurs dans le monde. Par conséquent, le FAI ne voit que le fait que vous êtes connecté à un VPN et rien sur l'activité que vous lui transmettez.

<div class="admonition note" markdown>
<p class="admonition-title">Note</p>

Lorsque nous faisons référence aux "Réseaux Privés Virtuels" sur ce site, nous faisons généralement référence à [des fournisseurs VPN](../vpn.md) **commerciaux**, à qui vous payez des frais mensuels en échange de l'acheminement sécurisé de votre trafic Internet à travers leurs serveurs publics. Il existe de nombreuses autres formes de VPN, tels que ceux que vous hébergez vous-même ou ceux gérés par des lieux de travail qui vous permettent de vous connecter en toute sécurité à des ressources réseau internes/employés, Cependant, ces VPNs sont généralement conçus pour accéder à des réseaux distants en toute sécurité, plutôt que pour protéger la confidentialité de votre connexion Internet.

</div>

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

L'utilisation d'un VPN dans les cas où vous utilisez votre [identité réelle ou connue](common-misconceptions.md#complicated-is-better) en ligne ne sera probablement pas utile. Cela peut déclencher des systèmes de détection de spam et de fraude, par exemple si vous vous connectez au site web de votre banque.

It's important to remember that a VPN will not provide you with absolute anonymity because the VPN provider itself will still have access to your real IP address, destination website information, and often a money trail that can be linked directly back to you. "No logging" policies are merely a promise; if you need complete safety from the network itself, consider using [Tor](../advanced/tor-overview.md) in addition to or instead of a VPN.

Vous ne devriez pas non plus faire confiance à un VPN pour sécuriser votre connexion à une destination HTTP non chiffrée. Pour que ce que vous faites sur les sites web que vous visitez reste privé et sécurisé, vous devez utiliser le protocole HTTPS. Cela conservera vos mots de passe, jetons de session, et les requêtes à l'abri du fournisseur VPN et d'autres adversaires potentiels entre le serveur VPN et votre destination. Vous devriez activer le mode HTTPS-uniquement dans votre navigateur (s'il est pris en charge) pour atténuer les attaques qui tentent de rétrograder votre connexion de HTTPS à HTTP.

## Devrais-je utiliser un DNS chiffré avec un VPN ?

À moins que votre fournisseur VPN n'héberge les serveurs DNS chiffrés lui-même, **probablement que non**. L'utilisation du DOH/DOT (ou de toute autre forme de DNS chiffrés) avec des serveurs tiers ajoutera simplement plus d'entités à qui faire confiance. Votre fournisseur de VPN peut toujours voir quels sites web vous visitez en se basant sur les adresses IP et d'autres méthodes. Cela étant dit, il peut y avoir certains avantages à activer le DNS chiffré afin d'activer d'autres fonctionnalités de sécurité dans votre navigateur, comme ECH. Les technologies de navigateur qui dépendent de DNS chiffré intégré dans le navigateur sont relativement nouvelles et pas encore répandues, donc sont-elles pertinentes pour vous spécifiquement c'est un exercice que nous vous laisserons explorer de vous-même.

Une autre raison courante pour laquelle le DNS chiffré est recommandé est qu'il empêche l'usurpation DNS. Cependant, votre navigateur devrait déjà vérifier la présence de [certificats TLS](https://en.wikipedia.org/wiki/Transport_Layer_Security#Digital_certificates) avec **HTTPS** et vous en avertir. Si vous n'utilisez pas **HTTPS**, alors un adversaire peut toujours modifier n'importe quoi d'autre que vos requêtes DNS et le résultat final sera peu différent.

## Devrais-je utiliser Tor *et* un VPN?

Peut-être, Tor n'est pas nécessairement adapté à tout le monde. Tenez compte de votre [modèle de menace](threat-modeling.md), car si votre adversaire n'est pas capable d'extraire des informations de votre fournisseur de VPN, l'utilisation d'un VPN seul peut fournir une protection suffisante.

Si vous utilisez Tor alors il est *probablement* préférable de vous connecter au réseau Tor via un fournisseur VPN commercial. Il s'agit toutefois d'un sujet complexe sur lequel nous avons écrit plus en détail sur notre page [Introduction à Tor](../advanced/tor-overview.md).

## Devrais-je accéder à Tor par le biais de fournisseurs VPN qui fournissent des "noeuds Tor" ?

Vous ne devriez pas utiliser cette fonctionnalité : l'avantage principal d'utiliser Tor est que vous ne faites pas confiance à votre fournisseur VPN, qui est annulée lorsque vous utilisez des nœuds Tor hébergés par votre VPN au lieu de vous connecter directement à Tor depuis votre ordinateur.

Actuellement, Tor supporte seulement le protocole TCP. UDP (utilisé par [WebRTC](https://en.wikipedia.org/wiki/WebRTC), [HTTP3/QUIC](https://en.wikipedia.org/wiki/HTTP/3), et d'autres protocoles), [ICMP](https://en.wikipedia.org/wiki/Internet_Control_Message_Protocol), et autres paquets seront lâchés. Pour compenser cela, les fournisseurs de VPN acheminent généralement tous les paquets non TCP par leur serveur VPN (votre premier saut). C'est le cas de [ProtonVPN](https://protonvpn.com/support/tor-vpn). De plus, lorsque vous utilisez cette configuration Tor sur VPN, vous n'avez pas le contrôle sur d'autres fonctionnalités importantes de Tor telles que l'[adresse de destination isolée](https://whonix.org/wiki/Stream_Isolation) (utilisation d'un circuit Tor différent pour chaque domaine que vous visitez).

La fonctionnalité doit être vue comme un moyen *pratique* pour accéder aux services cachés sur Tor, pas pour rester anonyme. Pour un véritable anonymat, utilisez le [Navigateur Tor](../tor.md).

## Propriété d'un VPN commercial

La plupart des services VPN sont détenus par les mêmes [entreprises](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies). Ces sociétés douteuses gèrent un grand nombre de petits services VPN afin de créer l'illusion que vous avez plus de choix qu'il n'y en a en réalité et de maximiser leurs profits. En règle générale, ces fournisseurs qui alimentent leur société écran ont des politiques de protection de la vie privée déplorables et il ne faut pas leur confier votre trafic internet. Vous devriez être très strict quant au fournisseur que vous décidez d'utiliser.

Vous devez également vous méfier du fait que de nombreux sites d'évaluation de VPN ne sont que des véhicules publicitaires ouverts au plus offrant. ==Privacy Guides ne gagne pas d'argent en recommandant des produits externes et n'utilise jamais de programmes d'affiliation.==

[Nos recommandations VPN](../vpn.md ""){.md-button}

## Alternatives modernes aux VPN

Récemment, plusieurs organisations ont tenté de résoudre certains problèmes posés par les VPN centralisés. Ces technologies sont relativement nouvelles, mais elles méritent d'être suivies de près au fur et à mesure que le domaine se développe.

### Relais multipartites

Les relais multipartites (MPR) utilisent plusieurs nœuds appartenant à différentes parties, de sorte qu'aucune partie ne sait à la fois qui vous êtes et à quoi vous vous connectez. C'est l'idée de base de Tor, mais il existe aujourd'hui des services payants qui tentent d'imiter ce modèle.

Les MPRs cherchent à résoudre un problème inhérent aux VPN: le fait que vous devez leur faire entièrement confiance. Elles atteignent cet objectif en segmentant les responsabilités entre deux ou plusieurs entreprises différentes.

One example of a commercially available MPR is Apple's iCloud+ Private Relay, which routes your traffic through two servers:

1. Premièrement, un serveur géré par Apple.

    Ce serveur est capable de voir l'adresse IP de votre appareil lorsque vous vous connectez, et a connaissance de vos informations de paiement et de l'identifiant Apple lié à votre abonnement iCloud. Cependant, il est incapable de voir sur quel site vous vous connectez.

2. Deuxièmement, un serveur géré par un partenaire CDN, tel que Cloudflare ou Fastly.

    Ce serveur établit la connexion avec votre site web de destination, mais n'a aucune connaissance de votre appareil. La seule adresse IP qu'il connaît est celle du serveur d'Apple.

Other MPRs run by different companies operate in a very similar manner. This protection by segmentation only exists if you trust the two companies to not collude with each other to deanonymize you.

### VPNs décentralisés

Another attempt at solving the issues with centralized VPN services are dVPNs. These are based on blockchain technology and claim to eliminate trust in a single party by distributing the nodes across lots of different people. However, many times a dVPN will default to a single node, meaning you need to trust that node completely, just like a traditional VPN. Unlike a traditional VPN, this one node that can see all your traffic is a random person instead of your VPN provider that can be audited and has legal responsibilities to uphold their privacy policy. Multi-hop is needed to solve this, but that comes with a stability and performance cost.

Another consideration is legal liability. The exit node will need to deal with legal problems from misuse of the network, an issue that the Tor network has contended with for its entire existence. This discourages regular people from running nodes and makes it more attractive for a malicious actor with lots of resources to host one. This is a big problem if the service is single-node, as the potentially malicious exit node can see who you are and what you're connecting to.

Many dVPNs are used to push a cryptocurrency rather than to make the best service. They also tend to be smaller networks with fewer nodes, making them more vulnerable to [Sybil attacks](https://en.wikipedia.org/wiki/Sybil_attack).

## Informations VPN liées

- [Le problème avec les sites d'évaluation des VPNs et de la vie privée](https://blog.privacyguides.org/2019/11/20/the-trouble-with-vpn-and-privacy-review-sites)
- [Enquête sur les applications VPN gratuites](https://top10vpn.com/research/free-vpn-investigations/ownership)
- [Les propriétaires inconnus des VPNs dévoilés : 101 produits VPN gérés par seulement 23 sociétés](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies)
- [Cette société chinoise est secrètement à l'origine de 24 applications populaires qui cherchent à obtenir des autorisations dangereuses](https://vpnpro.com/blog/chinese-company-secretly-behind-popular-apps-seeking-dangerous-permissions)
- [VPN - un récit très précaire](https://overengineer.dev/blog/2019/04/08/very-precarious-narrative.html) par Dennis Schubert
