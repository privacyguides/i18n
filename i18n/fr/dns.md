---
title: Résolveurs DNS
icon: material/dns
description: Nous vous recommandons d'utiliser ces DNS chiffrés pour remplacer la configuration par défaut de votre FAI.
cover: dns.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>Protège contre les menaces suivantes :</small>

- [:material-account-cash: Capitalisme de surveillance](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Les **DNS** chiffrés avec des serveurs tiers ne devraient être utilisés que pour contourner un [blocage DNS](https://en.wikipedia.org/wiki/DNS_blocking) basique lorsque vous êtes sûrs que cela n'aura aucune conséquence. Le DNS chiffré ne vous aidera pas à dissimuler vos activités de navigation.

[En savoir plus sur les DNS :material-arrow-right-drop-circle:](advanced/dns-overview.md ""){.md-button}

## Fournisseurs recommandés

Voici nos résolveurs DNS public favoris, basés sur leur confidentialité et leur sécurité, ainsi que leurs performances à l'échelle mondiale. Certains de ces services proposent une protection de base au niveau DNS contre les logiciels malveillants et les trackers selon le serveur que vous choisissez, mais si vous voulez les personnaliser il est préférable d'utiliser un service dédié au filtrage DNS.

| Fournisseur DNS                                                            | Protocoles                                                               | Journalisation / Politique de confidentialité | [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) | Filtrage                                                                                                                                                         | Profil Apple signé                                                                                                                                                                                                          |
| -------------------------------------------------------------------------- | ------------------------------------------------------------------------ | --------------------------------------------- | -------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [**DNS public AdGuard**](https://adguard-dns.io/en/public-dns.html)        | Cleartext <br>DoH/3 <br>DoT <br>DoQ <br>DNSCrypt | Anonymisé[^1]                                 | Anonymisé                                                      | Dépend du serveur choisi. La liste des filtres utilisés peut être consultée ici. [:octicons-link-external-24:](https://github.com/AdguardTeam/AdGuardSDNSFilter) | Oui [:octicons-link-external-24:](https://adguard-dns.io/en/blog/encrypted-dns-ios-14.html)                                                                                                                                 |
| [**Cloudflare**](https://developers.cloudflare.com/1.1.1.1/setup)          | Cleartext <br>DoH/3 <br>DoT                                  | Anonymisé[^2]                                 | Non                                                            | Dépend du serveur choisi.                                                                                                                                        | Non [:octicons-link-external-24:](https://community.cloudflare.com/t/requesting-1-1-1-1-signed-profiles-for-apple/571846)                                                                                                   |
| [**Control D Free DNS**](https://controld.com/free-dns)                    | Cleartext <br>DoH/3 <br>DoT <br>DoQ                    | Non[^3]                                       | Non                                                            | Dépend du serveur choisi.                                                                                                                                        | Oui <br>[:simple-apple: iOS](https://docs.controld.com/docs/ios-platform) <br>[:material-apple-finder: macOS](https://docs.controld.com/docs/macos-platform#manual-setup-profile)                               |
| [**DNS0.eu**](https://dns0.eu)                                             | Cleartext <br>DoH/3 <br>DoH <br>DoT <br>DoQ      | Anonymisé[^4]                                 | Anonymisé                                                      | Dépend du serveur choisi.                                                                                                                                        | Oui [:octicons-link-external-24:](https://dns0.eu/zero.dns0.eu.mobileconfig)                                                                                                                                                |
| [**Mullvad**](https://mullvad.net/en/help/dns-over-https-and-dns-over-tls) | DoH <br>DoT                                                        | Non[^5]                                       | Non                                                            | Dépend du serveur choisi. La liste des filtres utilisés peut être consultée ici. [:octicons-link-external-24:](https://github.com/mullvad/dns-adblock)           | Oui [:octicons-link-external-24:](https://github.com/mullvad/encrypted-dns-profiles)                                                                                                                                        |
| [**Quad9**](https://quad9.net)                                             | Cleartext <br>DoH <br>DoT <br>DNSCrypt                 | Anonymisé[^6]                                 | Optionnel                                                      | Dépend du serveur choisi. La protection contre les logiciels malveillants est incluse par défaut.                                                                | Oui <br>[:simple-apple: iOS](https://docs.quad9.net/Setup_Guides/iOS/iOS_14_and_later_(Encrypted)) <br>[:material-apple-finder: macOS](https://docs.quad9.net/Setup_Guides/MacOS/Big_Sur_and_later_(Encrypted)) |

## Filtrage DNS basé sur un cloud

Grâce à ces services de filtrage DNS, personnalisez les listes de blocage selon vos besoins via un tableau de bord web. Ils peuvent être utilisés facilement sur plusieurs réseaux.

### Control D

<div class="admonition recommendation" markdown>

![Logo de Control D](assets/img/dns/control-d.svg){ align=right }

**Control D** est un service DNS personnalisable qui vous permet de bloquer des menaces, du contenu indésirable et les publicités au niveau DNS.

En plus de leurs versions payantes, ils proposent plusieurs résolveurs DNS préconfigurés gratuits.

[:octicons-home-16: Page d'Accueil](https://controld.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://controld.com/privacy){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://docs.controld.com/docs/getting-started){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/Control-D-Inc/ctrld){ .card-link title="Code Source" }

<details class="downloads" markdown>
<summary>Télécharger</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.controld.setuputility)
- [:simple-appstore: App Store](https://apps.apple.com/app/1518799460)
- [:simple-github: GitHub](https://github.com/Control-D-Inc/ctrld/releases)
- [:fontawesome-brands-windows: Windows](https://docs.controld.com/docs/gui-setup-utility)
- [:simple-apple: macOS](https://docs.controld.com/docs/gui-setup-utility)
- [:simple-linux: Linux](https://docs.controld.com/docs/ctrld)

</details>

</div>

### NextDNS

<div class="admonition recommendation" markdown>

![Logo de NextDNS](assets/img/dns/nextdns.svg){ align=right }

**Next DNS** est un service DNS personnalisable qui vous permet de bloquer des menaces, du contenu indésirable et les publicités au niveau DNS.

Ils proposent une version gratuite à usage limité mais totalement fonctionnelle.

[:octicons-home-16: Page d'Accueil](https://nextdns.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nextdns.io/privacy){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://help.nextdns.io){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/nextdns/nextdns){ .card-link title="Code Source" }

<details class="downloads" markdown>
<summary>Télécharger</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/nextdns/id1463342498)
- [:simple-github: GitHub](https://github.com/nextdns/nextdns/releases)
- [:fontawesome-brands-windows: Windows](https://github.com/nextdns/nextdns/wiki/Windows)
- [:simple-apple: macOS](https://apps.apple.com/us/app/nextdns/id1464122853)
- [:simple-linux: Linux](https://github.com/nextdns/nextdns/wiki)

</details>

</div>

Lorsqu'il est utilisé avec un compte, NextDNS active par défaut les fonctionnalités d'analyse et de journalisation (requises par d'autre fonctionnalités). Vous pouvez configurer combien de temps et où sont stockés les logs que vous souhaitez conserver, ou bien les désactiver complètement.

La version gratuite de NextDNs est entièrement fonctionnelle, mais ne devrait pas être utilisée pour assurer la sécurité ou des opérations de filtrage critique, car le filtrage, la journalisation et toutes les autres fonctionnalités dépendantes d'un compte sont désactivées après 300 000 requêtes DNS par mois. Après cela, elle peut quand même être utilisée en tant que fournisseur DNS classique, vos appareils devraient donc continuer à fonctionner normalement en faisant des requêtes sécurisées DNS-over-HTTPS (DoH), mais sans vos listes de filtrage.

NextDNS fournit également un service DoH public sur `https://dns.nextdns.io` et DNS-over-TLS/QUIC (DoT/DoQ) sur `dns.nextdns.io`. Ces fonctionnalités sont disponibles par défaut dans Firefox et Chromium, et sont soumises à leur [politique de confidentialité](https://nextdns.io/privacy) par défaut, sans journalisation.

## Proxys DNS chiffrés

Un logiciel de proxy DNS chiffré fourni un proxy local vers lequel le résolveur [DNS non chiffré](advanced/dns-overview.md#unencrypted-dns) doit rediriger. Typically, it is used on platforms that don't natively support [encrypted DNS](advanced/dns-overview.md#what-is-encrypted-dns).

### RethinkDNS

<div class="admonition recommendation" markdown>

![RethinkDNS logo](assets/img/android/rethinkdns.svg#only-light){ align=right }
![RethinkDNS logo](assets/img/android/rethinkdns-dark.svg#only-dark){ align=right }

**RethinkDNS** is an open-source Android client that supports [DoH](advanced/dns-overview.md#dns-over-https-doh), [DoT](advanced/dns-overview.md#dns-over-tls-dot), [DNSCrypt](advanced/dns-overview.md#dnscrypt) and DNS Proxy. It also provides additional functionality such as caching DNS responses, locally logging DNS queries, and using the app as a firewall.

[:octicons-home-16: Homepage](https://rethinkdns.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://rethinkdns.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.rethinkdns.com){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/celzero/rethink-app){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.celzero.bravedns)
- [:simple-github: GitHub](https://github.com/celzero/rethink-app/releases)

</details>

</div>

While RethinkDNS takes up the Android VPN slot, you can still use a VPN or Orbot with the app by [adding a WireGuard configuration](https://docs.rethinkdns.com/proxy/wireguard) or [manually configuring Orbot as a Proxy server](https://docs.rethinkdns.com/firewall/orbot), respectively.

### DNSCrypt-Proxy

<div class="admonition recommendation" markdown>

![DNSCrypt-Proxy logo](assets/img/dns/dnscrypt-proxy.svg){ align=right }

**DNSCrypt-Proxy** is a DNS proxy with support for [DNSCrypt](advanced/dns-overview.md#dnscrypt), [DoH](advanced/dns-overview.md#dns-over-https-doh), and [Anonymized DNS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Anonymized-DNS).

[:octicons-repo-16: Repository](https://github.com/DNSCrypt/dnscrypt-proxy#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/DNSCrypt/dnscrypt-proxy/wiki){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/DNSCrypt/dnscrypt-proxy){ .card-link title="Source Code" }
[:octicons-heart-16:](https://opencollective.com/dnscrypt/contribute){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-Windows)
- [:simple-apple: macOS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-macOS)
- [:simple-linux: Linux](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-linux)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

The anonymized DNS feature does [not](advanced/dns-overview.md#why-shouldnt-i-use-encrypted-dns) anonymize other network traffic.

</div>

## Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

All DNS products...

- Must support [DNSSEC](advanced/dns-overview.md#what-is-dnssec).
- Must support [QNAME Minimization](advanced/dns-overview.md#what-is-qname-minimization).
- Must anonymize [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs) or disable it by default.

Additionally, all public providers...

- Must not log any personal data to disk.
    - As noted in the footnotes, some providers collect query information for purposes like security research, but in that case the data must not be associated with any PII such as IP address, etc.
- Should support [anycast](https://en.wikipedia.org/wiki/Anycast) or geo-steering.

[^1]: AdGuard stocke des mesures de performance agrégées de ses serveurs DNS, à savoir le nombre de demandes complètes adressées à un serveur particulier, le nombre de demandes bloquées et la vitesse de traitement des demandes. They also keep and store the database of domains requested within the last 24 hours.

    > We need this information to identify and block new trackers and threats. We also log how many times this or that tracker has been blocked. We need this information to remove outdated rules from our filters.

    AdGuard DNS: [*Privacy Policy*](https://adguard-dns.io/en/privacy.html) [^2]: Cloudflare collects and stores only the limited DNS query data that is sent to the 1.1.1.1 resolver. The 1.1.1.1 resolver service does not log personal data, and the bulk of the limited non-personally identifiable query data is stored only for 25 hours.

    1.1.1.1 Public DNS Resolver: [*Cloudflare’s commitment to privacy*](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver) [^3]: Control D only logs specific account data for Premium resolvers with custom DNS profiles. Free resolvers do not retain any data.

    Control D: [*Privacy Policy*](https://controld.com/privacy) [^4]: DNS0.eu collects some data for their threat intelligence feeds to monitor for newly registered/observed/active domains and other bulk data. That data is shared with some [partners](https://docs.dns0.eu/data-feeds/introduction) for e.g. security research. They do not collect any personally identifiable information.

    DNS0.eu: [*Privacy Policy*](https://dns0.eu/privacy) [^5]: Mullvad's DNS service is available to both subscribers and non-subscribers of Mullvad VPN. Leur politique de confidentialité affirme explicitement qu'ils n'enregistrent pas les requêtes DNS de quelque manière que ce soit.

    Mullvad: [*No-logging of user activity policy*](https://mullvad.net/en/help/no-logging-data-policy) [^6]: Quad9 collects some data for the purposes of threat monitoring and response. That data may then be remixed and shared for purposes like furthering their security research. Quad9 ne collecte ni n'enregistre les adresses IP ou d'autres données qu'elle juge personnellement identifiables.

    Quad9: [*Data and Privacy Policy*](https://quad9.net/privacy/policy)
