---
meta_title: "Recommandations et comparaison de services VPN privés, sans sponsors ni publicités - Privacy Guides"
title: "Services VPN"
icon: material/vpn
description: The best VPN services for protecting your privacy and security online. Find a provider here that isn't out to spy on you.
cover: vpn.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>Protects against the following threat(s):</small>

- [:material-account-cash: Capitalisme de surveillance](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

If you're looking for additional *privacy* from your ISP, on a public Wi-Fi network, or while torrenting files, a **VPN** may be the solution for you.

<div class="admonition danger" markdown>
<p class="admonition-title">Les VPN ne peuvent pas fournir d'anonymat</p>

L'utilisation d'un VPN ne rendra **pas** votre navigation anonyme et n'ajoutera pas de sécurité supplémentaire à un trafic non sécurisé (HTTP).

Si vous recherchez l'**anonymat**, vous devriez utiliser le Navigateur Tor. Si vous recherchez une **sécurité** supplémentaire, vous devez toujours assurer que vous vous connectez aux sites web en utilisant HTTPS. Un VPN ne se substitue pas à de bonnes pratiques de sécurité.

[Télécharger Tor](https://torproject.org/){ .md-button .md-button--primary } [Mythes sur Tor & FAQ](advanced/tor-overview.md){ .md-button }

</div>

[Présentation détaillée des VPNs :material-arrow-right-drop-circle:](basics/vpn-overview.md ""){.md-button}

## Fournisseurs recommandés

Les fournisseurs que nous recommandons utilisent le chiffrement, acceptent Monero, prennent en charge WireGuard & OpenVPN, et ont une politique de non-journalisation. Lisez notre \[liste complète de critères\](#criteres) pour plus d'informations.

| Fournisseur           | Pays | WireGuard                     | Redirection de port                                    | IPv6                                                         | Paiements anonymes     |
| --------------------- | ---- | ----------------------------- | ------------------------------------------------------ | ------------------------------------------------------------ | ---------------------- |
| [Proton](#proton-vpn) | 112+ | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange } Partial Support | :material-information-outline:{ .pg-blue } Limited Support   | Argent liquide         |
| [IVPN](#ivpn)         | 37+  | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                 | :material-information-outline:{ .pg-blue } Sortant seulement | Monero, argent liquide |
| [Mullvad](#mullvad)   | 45+  | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                 | :material-check:{ .pg-green }                                | Monero, argent liquide |

### Proton VPN

<div class="admonition recommendation" markdown>

![Proton VPN logo](assets/img/vpn/protonvpn.svg){ align=right }

**Proton VPN** est un concurrent de poids dans l'espace VPN, et il est en service depuis 2016. Proton AG est basé en Suisse et propose une offre gratuite limitée, ainsi qu'une option premium plus complète.

[:octicons-home-16: Page d'accueil](https://protonvpn.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://protonvpn.com/privacy-policy){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://protonvpn.com/support){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ProtonVPN){ .card-link title="Code source" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1437005085)
- [:simple-github: GitHub](https://github.com/ProtonVPN/android-app/releases)
- [:fontawesome-brands-windows: Windows](https://protonvpn.com/download-windows)
- [:simple-apple: macOS](https://protonvpn.com/download-macos)
- [:simple-linux: Linux](https://protonvpn.com/support/linux-vpn-setup)

</details>

</div>

#### :material-check:{ .pg-green } 112 Countries

Proton VPN has [servers in 112 countries](https://protonvpn.com/vpn-servers) or [5](https://protonvpn.com/support/how-to-create-free-vpn-account) if you use their [free plan](https://protonvpn.com/free-vpn/server).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Cela est dû à un itinéraire plus court (moins de sauts) vers la destination.
{ .annotate }

1. Last checked: 2024-08-06

Nous pensons également qu'il est préférable pour la sécurité des clés privées du fournisseur VPN d'utiliser des [serveurs dédiés](https://fr.wikipedia.org/wiki/Serveur_d%C3%A9di%C3%A9), plutôt que des solutions partagées (avec d'autres clients) moins chères telles que les [serveurs privés virtuels](https://fr.wikipedia.org/wiki/Serveur_d%C3%A9di%C3%A9_virtuel).

#### :material-check:{ .pg-green } Audit indépendant

Depuis janvier 2020, Proton VPN a fait l'objet d'un audit indépendant réalisé par SEC Consult. SEC Consult a trouvé quelques vulnérabilités à risque moyen et faible dans les applications Windows, Android et iOS de Proton VPN, qui ont toutes été "correctement corrigées" par Proton VPN avant la publication des rapports. Aucun des problèmes identifiés n'aurait permis à un attaquant d'accéder à distance à votre appareil ou à votre trafic. Vous pouvez consulter les rapports individuels pour chaque plateforme sur [protonvpn.com](https://protonvpn.com/blog/open-source). En avril 2022, Proton VPN a fait l'objet d'un [nouvel audit](https://protonvpn.com/blog/no-logs-audit). Une [lettre d'attestation](https://proton.me/blog/security-audit-all-proton-apps) a été fournie pour les applications de Proton VPN le 9 novembre 2021 par [Securitum](https://research.securitum.com).

#### :material-check:{ .pg-green } Clients open source

Proton VPN fournit le code source de ses clients bureau et mobile dans son [organisation GitHub](https://github.com/ProtonVPN).

#### :material-check:{ .pg-green } Accepte l'argent liquide

Proton VPN, en plus d'accepter les cartes de crédit/débit, PayPal, et [le Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), accepte également **les espèces/la monnaie locale** comme forme de paiement anonyme.

#### :material-check:{ .pg-green } Prise en charge de WireGuard

Proton VPN supports the WireGuard® protocol. [WireGuard](https://wireguard.com) est un protocole plus récent qui utilise une [cryptographie](https://wireguard.com/protocol) de pointe. De plus, WireGuard vise à être plus simple et plus performant.

Proton VPN [recommande](https://protonvpn.com/blog/wireguard) l'utilisation de WireGuard avec leur service. Proton VPN also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://wireguard.com/install).

#### :material-alert-outline:{ .pg-orange } Limited IPv6 Support

Proton [now supports IPv6](https://protonvpn.com/support/prevent-ipv6-vpn-leaks) in their browser extension and Linux client, but only 80% of their servers are IPv6-compatible. On other platforms, the Proton VPN client will block all outgoing IPv6 traffic, so you don't have to worry about your IPv6 address being leaked, but you will not be able to connect to any IPv6-only sites, nor will you be able to connect to Proton VPN from an IPv6-only network.

#### :material-information-outline:{ .pg-info } Redirection de port

Proton VPN ne prend actuellement en charge que la [redirection de port](https://protonvpn.com/support/port-forwarding) éphémère via NAT-PMP, avec des durées de location de 60 secondes. The official Windows and Linux apps provide an easy-to-access option for it, while on other operating systems you'll need to run your own [NAT-PMP client](https://protonvpn.com/support/port-forwarding-manual-setup). Les applications de torrent prennent souvent en charge NAT-PMP nativement.

#### :material-information-outline:{ .pg-blue } Anti-censure

Proton VPN has their [Stealth](https://protonvpn.com/blog/stealth-vpn-protocol) protocol which *may* help in situations where VPN protocols like OpenVPN or WireGuard are blocked with various rudimentary techniques. Stealth encapsule le tunnel VPN dans une session TLS afin de donner l'impression d'un trafic internet plus générique.

Unfortunately, it does not work very well in countries where sophisticated filters that analyze all outgoing traffic in an attempt to discover encrypted tunnels are deployed. Stealth is available on Android, iOS, Windows, and macOS, but it's not yet available on Linux.

#### :material-check:{ .pg-green } Clients mobiles

Proton VPN has published [App Store](https://apps.apple.com/app/id1437005085) and [Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android) clients, both supporting an easy-to-use interface as opposed to requiring you to manually configure your WireGuard connection. The Android client is also available on [GitHub](https://github.com/ProtonVPN/android-app/releases).

<div class="admonition warning" markdown>
<p class="admonition-title">How to opt out of sharing telemetry</p>

On Android, Proton hides telemetry settings under the misleadingly labeled "**Help us fight censorship**" menu in the settings panel. On other platforms these settings can be found under the "**Usage statistics**" menu.

We are noting this because while we don't necessarily recommend against sharing anonymous usage statistics with developers, it is important that these settings are easily found and clearly labeled.

</div>

#### :material-information-outline:{ .pg-blue } Notes supplémentaires

Proton VPN clients support two-factor authentication on all platforms. Proton VPN possède ses propres serveurs et centres de données en Suisse, en Islande et en Suède. Ils proposent le blocage des contenus et des domaines de logiciels malveillants connus avec leur service DNS. En outre, Proton VPN propose également des serveurs "Tor" vous permettant de vous connecter facilement aux sites onion, mais nous recommandons fortement d'utiliser [le navigateur officiel Tor](tor.md#tor-browser) à cette fin.

##### :material-alert-outline:{ .pg-orange } Kill switch feature is broken on Intel-based Macs

System crashes [may occur](https://protonvpn.com/support/macos-t2-chip-kill-switch) on Intel-based Macs when using the VPN kill switch. Si vous avez besoin de cette fonction, et que vous utilisez un Mac avec un chipset Intel, vous devriez envisager d'utiliser un autre service VPN.

### IVPN

<div class="admonition recommendation" markdown>

![Logo IVPN](assets/img/vpn/ivpn.svg){ align=right }

**IVPN** est un autre fournisseur de VPN haut de gamme, et il est en activité depuis 2009. IVPN est basé à Gibraltar et ne propose pas d'essai gratuit.

[:octicons-home-16: Page d'accueil](https://ivpn.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ivpn.net/privacy){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://ivpn.net/knowledgebase/general){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ivpn){ .card-link title="Code source" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/net.ivpn.client)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1193122683)
- [:fontawesome-brands-windows: Windows](https://ivpn.net/apps-windows)
- [:simple-apple: macOS](https://ivpn.net/apps-macos)
- [:simple-linux: Linux](https://ivpn.net/apps-linux)

</details>

</div>

#### :material-check:{ .pg-green } 37 pays

IVPN a des [serveurs dans 37 pays](https://ivpn.net/status).(1) Choisir un fournisseur VPN avec un serveur le plus proche de vous réduira la latence du trafic réseau que vous envoyez. Cela s'explique par un itinéraire plus court (moins de sauts) jusqu'à la destination.
{ .annotate }

1. Last checked: 2024-08-06

Nous pensons également qu'il est préférable pour la sécurité des clés privées du fournisseur VPN d'utiliser des [serveurs dédiés](https://fr.wikipedia.org/wiki/Serveur_d%C3%A9di%C3%A9), plutôt que des solutions partagées (avec d'autres clients) moins chères telles que les [serveurs privés virtuels](https://fr.wikipedia.org/wiki/Serveur_d%C3%A9di%C3%A9_virtuel).

#### :material-check:{ .pg-green } Audit indépendant

IVPN has had multiple [independent audits](https://ivpn.net/en/blog/tags/audit) since 2019 and has publicly announced their commitment to [annual security audits](https://ivpn.net/blog/ivpn-apps-security-audit-concluded).

#### :material-check:{ .pg-green } Clients open source

Depuis février 2020, [les applications IVPN sont désormais open-source](https://ivpn.net/blog/ivpn-applications-are-now-open-source). Le code source peut être obtenu auprès de leur [organisation GitHub](https://github.com/ivpn).

#### :material-check:{ .pg-green } Accepte l'argent liquide et le Monero

En plus d'accepter les cartes de crédit/débit et PayPal, IVPN accepte le Bitcoin, **le Monero** et **les espèces/la monnaie locale** (sur les abonnements annuels) comme formes de paiement anonymes. Des cartes prépayées avec des codes d'avoirs sont [également disponibles](https://ivpn.net/knowledgebase/billing/voucher-cards-faq).

#### :material-check:{ .pg-green } Prise en charge de WireGuard

IVPN prend en charge le protocole WireGuard®. [WireGuard](https://wireguard.com) est un protocole plus récent qui utilise une [cryptographie](https://wireguard.com/protocol) de pointe. De plus, WireGuard vise à être plus simple et plus performant.

IVPN [recommande](https://ivpn.net/wireguard) l'utilisation de WireGuard avec leur service et, en tant que tel, le protocole est par défaut sur toutes les applications d'IVPN. IVPN propose également un générateur de configuration WireGuard à utiliser avec les [applications](https://wireguard.com/install) officielles WireGuard.

#### :material-information-outline:{ .pg-blue } Prise en charge de l'IPv6

IVPN vous permet de vous [connecter à des services en utilisant l'IPv6](https://ivpn.net/knowledgebase/general/do-you-support-ipv6) mais ne vous permet pas de vous connecter à partir d'un appareil utilisant une adresse IPv6.

#### :material-alert-outline:{ .pg-orange } Redirection de port

IVPN prenait auparavant en charge la redirection de port, mais a supprimé cette option en [juin 2023](https://ivpn.net/blog/gradual-removal-of-port-forwarding). L'absence de cette fonctionnalité pourrait avoir un impact négatif sur certaines applications, en particulier les applications pair-à-pair telles que les clients torrent.

#### :material-check:{ .pg-green } Anti-censure

IVPN has obfuscation modes using [V2Ray](https://v2ray.com/en/index.html) which helps in situations where VPN protocols like OpenVPN or WireGuard are blocked. Currently, this feature is only available on Desktop and [iOS](https://ivpn.net/knowledgebase/ios/v2ray). Elle dispose de deux modes d'utilisation de [VMess](https://guide.v2fly.org/en_US/basics/vmess.html) via des connexions QUIC ou TCP. QUIC est un protocole moderne avec un meilleur contrôle de la congestion et peut donc être plus rapide avec une latence réduite. Le mode TCP fait apparaître vos données comme du trafic HTTP normal.

#### :material-check:{ .pg-green } Clients mobiles

IVPN has published [App Store](https://apps.apple.com/app/id1193122683) and [Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client) clients, both supporting an easy-to-use interface as opposed to requiring you to manually configure your WireGuard connection. The Android client is also available on [GitHub](https://github.com/ivpn/android-app/releases).

#### :material-information-outline:{ .pg-blue } Notes supplémentaires

IVPN clients support two-factor authentication. IVPN propose également la fonctionnalité "[AntiTraqueur](https://ivpn.net/antitracker)", qui bloque les réseaux publicitaires et les traqueurs au niveau du réseau.

### Mullvad

<div class="admonition recommendation" markdown>

![Logo Mullvad](assets/img/vpn/mullvad.svg){ align=right }

**Mullvad** est un VPN rapide et peu coûteux qui met l'accent sur la transparence et la sécurité. They have been in operation since 2009. Mullvad is based in Sweden and offers a 14-day money-back guarantee for [payment methods](https://mullvad.net/en/help/refunds) that allow it.

[:octicons-home-16: Page d'accueil](https://mullvad.net){ .md-button .md-button--primary }
[:simple-torbrowser:](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion){ .card-link title="Service onion" }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://mullvad.net/en/help){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/mullvad){ .card-link title="Code source" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1488466513)
- [:simple-github: GitHub](https://github.com/mullvad/mullvadvpn-app/releases)
- [:fontawesome-brands-windows: Windows](https://mullvad.net/en/download/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/linux)

</details>

</div>

#### :material-check:{ .pg-green } 49 Countries

Mullvad has [servers in 49 countries](https://mullvad.net/servers).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Cela s'explique par un itinéraire plus court (moins de sauts) jusqu'à la destination.
{ .annotate }

1. Last checked: 2025-03-10

Nous pensons également qu'il est préférable pour la sécurité des clés privées du fournisseur VPN d'utiliser des [serveurs dédiés](https://fr.wikipedia.org/wiki/Serveur_d%C3%A9di%C3%A9), plutôt que des solutions partagées (avec d'autres clients) moins chères telles que les [serveurs privés virtuels](https://fr.wikipedia.org/wiki/Serveur_d%C3%A9di%C3%A9_virtuel).

#### :material-check:{ .pg-green } Audit indépendant

Mullvad has had multiple [independent audits](https://mullvad.net/en/blog/tag/audits) and has publicly announced their endeavors to conduct [annual audits](https://mullvad.net/en/blog/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit) of their apps and infrastructure.

#### :material-check:{ .pg-green } Clients open source

Mullvad fournit le code source pour leurs clients de bureau et mobiles dans leur [organisation GitHub](https://github.com/mullvad/mullvadvpn-app).

#### :material-check:{ .pg-green } Accepte l'argent liquide et le Monero

Mullvad, en plus d'accepter les cartes de crédit/débit et PayPal, accepte le Bitcoin, le Bitcoin Cash, **le Monero** et **les espèces/la monnaie locale** comme formes de paiement anonymes. Des cartes prépayées avec des codes d'avoirs sont également disponibles. Mullvad also accepts Swish and bank wire transfers, as well as a few European payment systems.

#### :material-check:{ .pg-green } Prise en charge de WireGuard

Mullvad prend en charge le protocole WireGuard®. [WireGuard](https://wireguard.com) est un protocole plus récent qui utilise une [cryptographie](https://wireguard.com/protocol) de pointe. De plus, WireGuard vise à être plus simple et plus performant.

Mullvad [recommande](https://mullvad.net/en/help/why-wireguard) l'utilisation de WireGuard avec leur service. C'est le protocole par défaut ou le seul sur les applications Android, iOS, macOS et Linux de Mullvad, mais sur Windows vous devez [activer manuellement](https://mullvad.net/en/help/how-turn-wireguard-mullvad-app) WireGuard. Mullvad propose également un générateur de configuration WireGuard à utiliser avec les [applications](https://wireguard.com/install) officielles WireGuard.

#### :material-check:{ .pg-green } Prise en charge de l'IPv6

Mullvad vous permet d'[accéder à des services hébergés sur IPv6](https://mullvad.net/en/blog/2014/9/15/ipv6-support) et de vous connecter à partir d'un appareil utilisant une adresse IPv6.

#### :material-alert-outline:{ .pg-orange } Redirection de port

Mullvad prenait auparavant en charge la redirection de port, mais a supprimé cette option en [mai 2023](https://mullvad.net/en/blog/2023/5/29/removing-the-support-for-forwarded-ports). L'absence de cette fonctionnalité pourrait avoir un impact négatif sur certaines applications, en particulier les applications pair-à-pair telles que les clients torrent.

#### :material-check:{ .pg-green } Anti-censure

Mullvad offers several features to help bypass censorship and access the internet freely:

- **Obfuscation modes**: Mullvad has two built-in obfuscation modes: "UDP-over-TCP" and ["WireGuard over Shadowsocks"](https://mullvad.net/en/blog/introducing-shadowsocks-obfuscation-for-wireguard). These modes disguise your VPN traffic as regular web traffic, making it harder for censors to detect and block. Supposedly, China has to use a [new method to disrupt Shadowsocks-routed traffic](https://gfw.report/publications/usenixsecurity23/en).
- **Advanced obfuscation with Shadowsocks and v2ray**: For more advanced users, Mullvad provides a guide on how to use the [Shadowsocks with v2ray](https://mullvad.net/en/help/shadowsocks-with-v2ray) plugin with Mullvad clients. This setup provides an additional layer of obfuscation and encryption.
- **Custom server IPs**: To counter IP-blocking, you can request custom server IPs from Mullvad's support team. Once you receive the custom IPs, you can input the text file in the "Server IP override" settings, which will override the chosen server IP addresses with ones that aren't known to the censor.
- **Bridges and proxies**: Mullvad also allows you to use bridges or proxies to reach their API (needed for authentication), which can help bypass censorship attempts that block access to the API itself.

#### :material-check:{ .pg-green } Clients mobiles

Mullvad a publié des clients [App Store](https://apps.apple.com/app/id1488466513) et [Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn), tous deux avec une interface simple à utiliser plutôt que nécessiter de votre part une configuration manuelle de votre connexion WireGuard. Le client Android est également disponible sur [GitHub](https://github.com/mullvad/mullvadvpn-app/releases).

#### :material-information-outline:{ .pg-blue } Notes supplémentaires

Mullvad est très transparent quant aux nœuds qu'il [possède ou qu'il loue](https://mullvad.net/en/servers). They also provide the option to enable Defense Against AI-guided Traffic Analysis ([DAITA](https://mullvad.net/en/blog/daita-defense-against-ai-guided-traffic-analysis)) in their apps. DAITA protects against the threat of advanced traffic analysis which can be used to connect patterns in VPN traffic with specific websites.

## Critères

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

Il est important de noter que l'utilisation d'un fournisseur VPN ne vous rendra pas anonyme, mais qu'elle vous permettra de mieux protéger votre vie privée dans certaines situations. Un VPN n'est pas un outil pour des activités illégales. Ne vous fiez pas à une politique de "non-journalisation".

</div>

**Veuillez noter que nous ne sommes affiliés à aucun des fournisseurs que nous recommandons. Cela nous permet de fournir des recommandations totalement objectives.** En plus de [nos critères standards](about/criteria.md), nous avons développé un ensemble d'exigences claires pour tout fournisseur de VPN souhaitant être recommandé, y compris un chiffrement fort, des audits de sécurité indépendants, une technologie moderne, et plus encore. Nous vous suggérons de vous familiariser avec cette liste avant de choisir un fournisseur VPN, et de mener vos propres recherches pour vous assurer que le fournisseur VPN que vous choisissez est le plus digne de confiance possible.

### Technologie

We require all our recommended VPN providers to provide standard configuration files which can be used in a generic, open-source client. **If** a VPN provides their own custom client, we require a kill switch to block network data leaks when disconnected.

**Minimum pour se qualifier :**

- Support for strong protocols such as WireGuard.
- Kill switch built in to clients.
- Multi-hop support. Multi-hopping is important to keep data private in case of a single node compromise.
- Si des clients VPN sont fournis, ils doivent être [open source](https://en.wikipedia.org/wiki/Open_source), comme le logiciel VPN qui y est généralement intégré. We believe that [source code](https://en.wikipedia.org/wiki/Source_code) availability provides greater transparency about what the program is actually doing.
- Censorship resistance features designed to bypass firewalls without DPI.

**Dans le meilleur des cas :**

- Kill switch with highly configurable options (enable/disable on certain networks, on boot, etc.)
- Clients VPN faciles à utiliser
- [IPv6](https://en.wikipedia.org/wiki/IPv6) support. Nous nous attendons à ce que les serveurs autorisent les connexions entrantes via IPv6 et vous permettent d'accéder aux services hébergés sur des adresses IPv6.
- La capacité de [transfert de port à distance](https://en.wikipedia.org/wiki/Port_forwarding#Remote_port_forwarding) aide à créer des connexions lors de l'utilisation de logiciels de partage de fichiers P2P ([Peer-to-Peer](https://en.wikipedia.org/wiki/Peer-to-peer)) ou de l'hébergement d'un serveur (par exemple, Mumble).
- Obfuscation technology which camouflages the true nature of internet traffic, designed to circumvent advanced internet censorship methods like DPI.

### Confidentialité

Nous préférons que nos prestataires recommandés collectent le moins de données possible. Ne pas recueillir de renseignements personnels sur l'inscription et accepter des modes de paiement anonymes sont requis.

**Minimum pour se qualifier :**

- Option de paiement en [crypto-monnaie anonyme](cryptocurrency.md) **ou** en espèces.
- Aucune information personnelle requise pour s'inscrire : seuls le nom d'utilisateur, le mot de passe et l'e-mail sont requis.

**Dans le meilleur des cas :**

- Accepte plusieurs [options de paiement anonymes](advanced/payments.md).
- No personal information accepted (auto-generated username, no email required, etc.).

### Sécurité

Un VPN est inutile s'il ne peut même pas fournir une sécurité adéquate. We require all our recommended providers to abide by current security standards. Idéalement, ils utiliseraient par défaut des schémas de chiffrement plus évolutifs. Nous exigeons également qu'un tiers indépendant procède à un audit de la sécurité du fournisseur, idéalement de manière très complète et de manière répétée (chaque année).

**Minimum pour se qualifier :**

- Schémas de chiffrement forts : OpenVPN avec authentification SHA-256 ; poignée de main RSA-2048 ou mieux ; chiffrement des données AES-256-GCM ou AES-256-CBC.
- Confidentialité persistante.
- Des audits de sécurité publiés par une société tierce réputée.
- VPN servers that use full-disk encryption or are RAM-only.

**Dans le meilleur des cas :**

- Chiffrement le plus fort : RSA-4096.
- Optional quantum-resistant encryption.
- Confidentialité persistante.
- Des audits de sécurité complets publiés par une société tierce réputée.
- Des programmes de primes aux bugs et/ou un processus coordonné de divulgation des vulnérabilités.
- RAM-only VPN servers.

### Confiance

Vous ne confieriez pas vos finances à une personne ayant une fausse identité, alors pourquoi lui confier vos données internet ? Nous exigeons de nos fournisseurs recommandés qu'ils rendent public leur propriété ou leur direction. Nous aimerions également voir des rapports de transparence fréquents, notamment en ce qui concerne la manière dont les demandes de gouvernement sont traitées.

**Minimum pour se qualifier :**

- Une direction ou un propriétaire public.
- Company based in a jurisdiction where it cannot be forced to do secret logging.

**Dans le meilleur des cas :**

- Une direction publique.
- Rapports de transparence fréquents.

### Marketing

Avec les fournisseurs de VPN que nous recommandons, nous aimons voir un marketing responsable.

**Minimum pour se qualifier :**

- Must self-host analytics (i.e., no Google Analytics).

Ne doit pas avoir de marketing irresponsable :

- Garantir la protection de l'anonymat à 100%. Lorsque quelqu'un prétend que quelque chose est à 100%, cela signifie qu'il n'y a aucune certitude d'échec. Nous savons que les gens peuvent assez facilement se désanonymiser de plusieurs façons, par exemple :
    - Réutiliser des informations personnelles (par exemple, des comptes email, des pseudonymes uniques, etc.) auxquelles ils ont accédé sans logiciel d'anonymat (Tor, VPN, etc.)
    - [Empreinte numérique des navigateurs](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)
- Affirmer qu'un seul circuit VPN est « plus anonyme » que Tor, qui est un circuit de 3 sauts ou plus qui change régulièrement.
- Utilisez un langage responsable, par exemple, il est acceptable de dire qu'un VPN est "déconnecté" ou "non connecté", mais dire qu'une personne est "exposée", "vulnérable" ou "compromise" est une utilisation inutile d'un langage alarmant qui peut être incorrect. Par exemple, cette personne peut simplement être sur le service d'un autre fournisseur de VPN ou utiliser Tor.

**Dans le meilleur des cas :**

Un marketing responsable qui est à la fois éducatif et utile au consommateur pourrait inclure :

- Une comparaison précise pour savoir quand [Tor](tor.md) devrait être utilisée à la place.
- Disponibilité du site web du fournisseur VPN sur un [service .onion](https://en.wikipedia.org/wiki/.onion)

### Fonctionnalités supplémentaires

Bien qu'il ne s'agisse pas d'exigences strictes, nous avons tenu compte de certains facteurs pour déterminer les fournisseurs à recommander. These include content blocking functionality, warrant canaries, excellent customer support, the number of allowed simultaneous connections, etc.
