---
title: "Résolveurs DNS"
icon: material/dns
description: Voici quelques fournisseurs de DNS chiffrés que nous vous recommandons d'utiliser pour remplacer la configuration par défaut de votre FAI.
cover: dns.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

Les DNS chiffrés avec des serveurs tiers ne doivent être utilisés que pour contourner le [blocage DNS](https://en.wikipedia.org/wiki/DNS_blocking) de base lorsque vous pouvez être sûr qu'il n'y aura pas de conséquences. Le DNS chiffré ne vous aidera pas à dissimuler vos activités de navigation.

[En savoir plus sur les DNS :material-arrow-right-drop-circle:](advanced/dns-overview.md ""){.md-button}

## Fournisseurs recommandés

| Fournisseur DNS                                                            | Politique de confidentialité                                                                         | Protocoles                                                                                 | Journalisation  | ECS       | Filtrage                                                                                                                                                                     |
| -------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ | --------------- | --------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [**AdGuard**](https://adguard.com/en/adguard-dns/overview.html)            | [:octicons-link-external-24:](https://adguard.com/en/privacy/dns.html)                               | Cleartext <br> DoH/3 <br> DoT <br> DoQ <br> DNSCrypt               | Un peu[^1]      | Oui       | En fonction de la configuration personnelle. La liste des filtres utilisés peut être consultée ici. [:octicons-link-external-24:](https://github.com/AdguardTeam/AdGuardDNS) |
| [**Cloudflare**](https://developers.cloudflare.com/1.1.1.1/setup)          | [:octicons-link-external-24:](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver) | Cleartext <br> DoH <br> DoT                                                    | Un peu[^2]      | Non       | En fonction de la configuration personnelle.                                                                                                                                 |
| [**Control D**](https://controld.com/free-dns)                             | [:octicons-link-external-24:](https://controld.com/privacy)                                          | Cleartext <br> DoH <br> DoT <br> DNSCrypt <br> DoQ <br> DoH3 | Optionnelle[^3] | Non       | En fonction de la configuration personnelle.                                                                                                                                 |
| [**Mullvad**](https://mullvad.net/en/help/dns-over-https-and-dns-over-tls) | [:octicons-link-external-24:](https://mullvad.net/en/help/no-logging-data-policy)                    | DoH <br> DoT                                                                         | Aucune[^4]      | Non       | En fonction de la configuration personnelle. La liste des filtres utilisés peut être consultée ici. [:octicons-link-external-24:](https://github.com/mullvad/dns-adblock)    |
| [**NextDNS**](https://nextdns.io)                                          | [:octicons-link-external-24:](https://nextdns.io/privacy)                                            | Cleartext <br> DoH <br> DoT <br> DNSCrypt <br> DoQ <br> DoH3 | Optionnelle[^5] | Optionnel | En fonction de la configuration personnelle.                                                                                                                                 |
| [**Quad9**](https://quad9.net)                                             | [:octicons-link-external-24:](https://quad9.net/privacy/policy)                                      | Cleartext <br> DoH <br> DoT <br> DNSCrypt                                | Un peu[^6]      | Optionnel | En fonction de la configuration personnelle, blocage des logiciels malveillants par défaut.                                                                                  |

### Critères

**Veuillez noter que nous ne sommes affiliés à aucun des projets que nous recommandons.** En plus de [nos critères de base](about/criteria.md), nous avons développé un ensemble d'exigences claires pour nous permettre de fournir des recommandations objectives. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

<div class="admonition example" markdown>
<p class="admonition-title">Cette section est nouvelle</p>

Nous travaillons à l'établissement de critères définis pour chaque section de notre site, et celles-ci peuvent être sujet à changement. Si vous avez des questions sur nos critères, veuillez [poser la question sur notre forum](https://discuss.privacyguides.net/latest) et ne supposez pas que nous n'avons pas pris en compte un élément dans nos recommandations s'il ne figure pas dans la liste. De nombreux facteurs sont pris en compte et discutés lorsque nous recommandons un projet, et la documentation de chacun d'entre eux est en cours.

</div>

- Doit supporter [DNSSEC](advanced/dns-overview.md#what-is-dnssec).
- [Minimisation QNAME](advanced/dns-overview.md#what-is-qname-minimization).
- Permettre la désactivation de [ECS](advanced/dns-overview.md#what-is-edns-client-subnet-ecs)
- Doit préférer la prise en charge [anycast](https://en.wikipedia.org/wiki/Anycast#Addressing_methods) ou geo-steering.

## Prise en charge native des systèmes d'exploitation

### Android

Android 9 et supérieur prennent en charge DNS via TLS. Les paramètres peuvent être trouvés dans : **Paramètres** &rarr; **Réseau & Internet** &rarr; **DNS Privé**.

### Appareils Apple

Les dernières versions d'iOS, iPadOS, tvOS et macOS prennent en charge à la fois DoT et DoH. Les deux protocoles sont pris en charge nativement par l'intermédiaire des [profils de configuration](https://support.apple.com/guide/security/configuration-profile-enforcement-secf6fb9f053/web) ou par l'intermédiaire de [l'API de Paramètres DNS](https://developer.apple.com/documentation/networkextension/dns_settings).

Après l'installation d'un profil de configuration ou d'une application qui utilise l'API des Paramètres DNS, la configuration DNS peut être sélectionnée. Si un VPN est actif, la résolution au sein du tunnel VPN utilisera les paramètres DNS du VPN et non les paramètres de votre système.

#### Profils signés

Apple ne fournit pas d'interface native pour la création de profils DNS chiffrés. Le [créateur de profil DNS Sécurisé](https://dns.notjakob.com/tool.html) est un outil non officiel permettant de créer vos propres profils DNS chiffrés, mais ils ne seront pas signés. Les profils signés sont préférables ; la signature valide l'origine d'un profil et contribue à garantir l'intégrité des profils. Un label vert "Vérifié" est attribué aux profils de configuration signés. Pour plus d'informations sur la signature de code, voir [A propos de la signature de code](https://developer.apple.com/library/archive/documentation/Security/Conceptual/CodeSigningGuide/Introduction/Introduction.html). **Signed profiles** are offered by [AdGuard](https://adguard.com/en/blog/encrypted-dns-ios-14.html), [NextDNS](https://apple.nextdns.io), and [Quad9](https://quad9.net/news/blog/ios-mobile-provisioning-profiles).

<div class="admonition info" markdown>
<p class="admonition-title">Info</p>

`systemd-resolved`, que de nombreuses distributions Linux utilisent pour effectuer leurs recherches DNS, ne [supporte pas encore DoH](https://github.com/systemd/systemd/issues/8639). Si vous voulez utiliser DoH, vous devez installer un proxy comme [dnscrypt-proxy](https://github.com/DNSCrypt/dnscrypt-proxy) et [le configurer](https://wiki.archlinux.org/title/Dnscrypt-proxy) pour prendre toutes les requêtes DNS du résolveur de votre système et les transmettre via HTTPS.

</div>

## Proxys DNS chiffrés

Un logiciel de proxy DNS chiffré fourni un proxy local vers lequel le résolveur [DNS non chiffré](advanced/dns-overview.md#unencrypted-dns) doit rediriger. Il est généralement utilisé sur les plates-formes qui ne supportent pas nativement les [DNS chiffrés](advanced/dns-overview.md#what-is-encrypted-dns).

### RethinkDNS

<div class="admonition recommendation" markdown>

![Logo RethinkDNS](assets/img/android/rethinkdns.svg#only-light){ align=right }
![Logo RethinkDNS](assets/img/android/rethinkdns-dark.svg#only-dark){ align=right }

**RethinkDNS** est un client Android open-source prenant en charge [DNS-over-HTTPS](advanced/dns-overview.md#dns-over-https-doh), [DNS-over-TLS](advanced/dns-overview.md#dns-over-tls-dot), [DNSCrypt](advanced/dns-overview.md#dnscrypt) et DNS Proxy, ainsi que la mise en cache des réponses DNS, l'enregistrement local des requêtes DNS et peut également être utilisé comme pare-feu.

[:octicons-home-16: Homepage](https://rethinkdns.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://rethinkdns.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.rethinkdns.com){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/celzero/rethink-app){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.celzero.bravedns)
- [:simple-github: GitHub](https://github.com/celzero/rethink-app/releases)

</details>

</div>

### dnscrypt-proxy

<div class="admonition recommendation" markdown>

![logo dnscrypt-proxy](assets/img/dns/dnscrypt-proxy.svg){ align=right }

**dnscrypt-proxy** est un proxy DNS qui prend en charge [DNSCrypt](advanced/dns-overview.md#dnscrypt), [DNS-over-HTTPS](advanced/dns-overview.md#dns-over-https-doh) et [Anonymized DNS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Anonymized-DNS).

<div class="admonition warning" markdown>
<p class="admonition-title">The anonymized DNS feature does <a href="advanced/dns-overview.md#why-shouldnt-i0-use-encrypted-dns"><strong>not</strong></a> anonymize other network traffic.</p>
</div>

[:octicons-repo-16: Repository](https://github.com/DNSCrypt/dnscrypt-proxy){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/DNSCrypt/dnscrypt-proxy/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/DNSCrypt/dnscrypt-proxy){ .card-link title="Source Code" }
[:octicons-heart-16:](https://opencollective.com/dnscrypt/contribute){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-Windows)
- [:simple-apple: macOS](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-macOS)
- [:simple-linux: Linux](https://github.com/DNSCrypt/dnscrypt-proxy/wiki/Installation-linux)

</details>

</div>

## Solutions auto-hébergées

Une solution DNS auto-hébergée est utile pour assurer le filtrage sur les plateformes contrôlées, telles que les téléviseurs intelligents et autres appareils IoT, car aucun logiciel côté client n'est nécessaire.

### AdGuard Home

<div class="admonition recommendation" markdown>

![AdGuard Home logo](assets/img/dns/adguard-home.svg){ align=right }

**AdGuard Home** is an open-source [DNS-sinkhole](https://en.wikipedia.org/wiki/DNS_sinkhole) which uses [DNS filtering](https://cloudflare.com/learning/access-management/what-is-dns-filtering) to block unwanted web content, such as advertisements.

AdGuard Home est doté d'une interface web conviviale qui permet de visualiser et de gérer le contenu bloqué.

[:octicons-home-16: Page d'accueil](https://adguard.com/adguard-home/overview.html){ .md-button .md-button--primary }
[:octicons-eye-16:](https://adguard.com/privacy/home.html){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://github.com/AdguardTeam/AdGuardHome/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/AdguardTeam/AdGuardHome){ .card-link title="Code source" }

</details>

</div>

### Pi-hole

<div class="admonition recommendation" markdown>

![Pi-hole logo](assets/img/dns/pi-hole.svg){ align=right }

**Pi-hole** is an open-source [DNS-sinkhole](https://en.wikipedia.org/wiki/DNS_sinkhole) which uses [DNS filtering](https://cloudflare.com/learning/access-management/what-is-dns-filtering) to block unwanted web content, such as advertisements.

Pi-hole est conçu pour être hébergé sur un Raspberry Pi, mais il n'est pas limité à ce type de matériel. Le logiciel est doté d'une interface web conviviale permettant de visualiser et de gérer les contenus bloqués.

[:octicons-home-16: Homepage](https://pi-hole.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://pi-hole.net/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.pi-hole.net){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/pi-hole/pi-hole){ .card-link title="Source Code" }
[:octicons-heart-16:](https://pi-hole.net/donate){ .card-link title=Contribute }

</details>

</div>

[^1]: AdGuard stocke des mesures de performance agrégées de ses serveurs DNS, à savoir le nombre de demandes complètes adressées à un serveur particulier, le nombre de demandes bloquées et la vitesse de traitement des demandes. Ils conservent et stockent également la base de données des domaines demandés dans les dernières 24 heures. "Nous avons besoin de ces informations pour identifier et bloquer les nouveaux traqueurs et menaces." "Nous enregistrons également le nombre de fois où tel ou tel traqueur a été bloqué. Nous avons besoin de ces informations pour supprimer les règles obsolètes de nos filtres." [https://adguard.com/fr/privacy/dns.html](https://adguard.com/en/privacy/dns.html)
[^2]: Cloudflare ne collecte et ne stocke que les données limitées des requêtes DNS qui sont envoyées au résolveur 1.1.1.1. Le service de résolution 1.1.1.1 n'enregistre pas de données personnelles, et la majeure partie des données de requête limitées et non personnellement identifiables n'est stockée que pendant 25 heures. [https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver/](https://developers.cloudflare.com/1.1.1.1/privacy/public-dns-resolver)
[^3]: Control D n'enregistre que les résolveurs Premium avec des profils DNS personnalisés. Les résolveurs libres n'enregistrent pas de données. [https://controld.com/privacy](https://controld.com/privacy)
[^4]: Le service DNS de Mullvad est disponible à la fois pour les abonnés et les non-abonnés de Mullvad VPN. Leur politique de confidentialité affirme explicitement qu'ils n'enregistrent pas les requêtes DNS de quelque manière que ce soit. [https://mullvad.net/en/help/no-logging-data-policy/](https://mullvad.net/en/help/no-logging-data-policy)
[^5]: When used with an account, NextDNS will enable insights and logging features by default (as some features require it). You can choose retention time and log storage location for any logs you choose to keep, or disable logs altogether. If used without an account, no data is logged. [https://nextdns.io/privacy](https://nextdns.io/privacy)
[^6]: Quad9 recueille certaines données à des fins de surveillance et de réponse aux menaces. Ces données peuvent ensuite être remélangées et partagées, par exemple à des fins de recherche sur la sécurité. Quad9 ne collecte ni n'enregistre les adresses IP ou d'autres données qu'elle juge personnellement identifiables. [https://quad9.net/privacy/policy](https://quad9.net/privacy/policy)
