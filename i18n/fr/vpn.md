---
meta_title: "Recommandations et comparaison de services VPN privés, sans sponsors ni publicités - Privacy Guides"
title: "Services VPN"
icon: material/vpn
description: Voici les meilleurs services VPN pour protéger votre vie privée et votre sécurité en ligne. Trouvez ici un fournisseur qui ne cherche pas à vous espionner.
cover: vpn.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<!-- markdownlint-disable MD024 -->

Si vous recherchez à protéger votre **vie privée** vis-à-vis de votre FAI, sur un réseau Wi-Fi public ou lorsque vous téléchargez des fichiers en torrent, un VPN peut être la solution pour vous.

<div class="admonition danger" markdown>
<p class="admonition-title">Les VPN ne peuvent pas fournir d'anonymat</p>

L'utilisation d'un VPN ne rendra **pas** votre navigation anonyme et n'ajoutera pas de sécurité supplémentaire à un trafic non sécurisé (HTTP).

Si vous recherchez l'**anonymat**, vous devriez utiliser le Navigateur Tor. Si vous recherchez une **sécurité** supplémentaire, vous devez toujours assurer que vous vous connectez aux sites web en utilisant HTTPS. Un VPN ne se substitue pas à de bonnes pratiques de sécurité.

[Télécharger Tor](https://torproject.org/){ .md-button .md-button--primary } [Mythes sur Tor & FAQ](advanced/tor-overview.md){ .md-button }

</div>

[Présentation détaillée des VPNs :material-arrow-right-drop-circle:](basics/vpn-overview.md ""){.md-button}

## Fournisseurs recommandés

Les fournisseurs que nous recommandons utilisent le chiffrement, acceptent Monero, prennent en charge WireGuard & OpenVPN, et ont une politique de non-journalisation. Lisez notre \[liste complète de critères\](#criteres) pour plus d'informations.

| Fournisseur           | Pays | WireGuard                     | Redirection de port                                        | IPv6                                                         | Paiements anonymes     |
| --------------------- | ---- | ----------------------------- | ---------------------------------------------------------- | ------------------------------------------------------------ | ---------------------- |
| [Proton](#proton-vpn) | 91+  | :material-check:{ .pg-green } | :material-information-outline:{ .pg-blue } Support partiel | :material-alert-outline:{ .pg-orange }                       | Argent liquide         |
| [IVPN](#ivpn)         | 37+  | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                     | :material-information-outline:{ .pg-blue } Sortant seulement | Monero, argent liquide |
| [Mullvad](#mullvad)   | 41+  | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                     | :material-check:{ .pg-green }                                | Monero, argent liquide |

### Proton VPN

<div class="admonition recommendation" markdown>

![Proton VPN logo](assets/img/vpn/protonvpn.svg){ align=right }

**Proton VPN** est un concurrent de poids dans l'espace VPN, et il est en service depuis 2016. Proton AG est basé en Suisse et propose une offre gratuite limitée, ainsi qu'une option premium plus complète.

[:octicons-home-16: Page d'accueil](https://protonvpn.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://protonvpn.com/privacy-policy){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://protonvpn.com/support){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ProtonVPN){ .card-link title="Code source" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1437005085)
- [:simple-github: GitHub](https://github.com/ProtonVPN/android-app/releases)
- [:simple-windows11: Windows](https://protonvpn.com/download-windows)
- [:simple-linux: Linux](https://protonvpn.com/support/linux-vpn-setup)

</details>

</div>

#### :material-check:{ .pg-green } 91 pays

Proton VPN a [des serveurs dans 91 pays](https://protonvpn.com/vpn-servers) ou [5](https://protonvpn.com/support/how-to-create-free-vpn-account) si vous utilisez leur [offre gratuite](https://protonvpn.com/free-vpn/server).(1) Choisir un fournisseur VPN avec un serveur le plus proche de vous réduira la latence du trafic réseau que vous envoyez. Cela est dû à un itinéraire plus court (moins de sauts) vers la destination.
{ .annotate }

1. Dernière vérification : 2024-04-02

Nous pensons également qu'il est préférable pour la sécurité des clés privées du fournisseur VPN d'utiliser des [serveurs dédiés](https://fr.wikipedia.org/wiki/Serveur_d%C3%A9di%C3%A9), plutôt que des solutions partagées (avec d'autres clients) moins chères telles que les [serveurs privés virtuels](https://fr.wikipedia.org/wiki/Serveur_d%C3%A9di%C3%A9_virtuel).

#### :material-check:{ .pg-green } Audit indépendant

Depuis janvier 2020, Proton VPN a fait l'objet d'un audit indépendant réalisé par SEC Consult. SEC Consult a trouvé quelques vulnérabilités à risque moyen et faible dans les applications Windows, Android et iOS de Proton VPN, qui ont toutes été "correctement corrigées" par Proton VPN avant la publication des rapports. Aucun des problèmes identifiés n'aurait permis à un attaquant d'accéder à distance à votre appareil ou à votre trafic. Vous pouvez consulter les rapports individuels pour chaque plateforme sur [protonvpn.com](https://protonvpn.com/blog/open-source). En avril 2022, Proton VPN a fait l'objet d'un [nouvel audit](https://protonvpn.com/blog/no-logs-audit) dont le rapport a été [établi par Securitum](https://protonvpn.com/blog/wp-content/uploads/2022/04/securitum-protonvpn-nologs-20220330.pdf). Une [lettre d'attestation](https://proton.me/blog/security-audit-all-proton-apps) a été fournie pour les applications de Proton VPN le 9 novembre 2021 par [Securitum](https://research.securitum.com).

#### :material-check:{ .pg-green } Clients open source

Proton VPN fournit le code source de ses clients bureau et mobile dans son [organisation GitHub](https://github.com/ProtonVPN).

#### :material-check:{ .pg-green } Accepte l'argent liquide

Proton VPN, en plus d'accepter les cartes de crédit/débit, PayPal, et [le Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), accepte également **les espèces/la monnaie locale** comme forme de paiement anonyme.

#### :material-check:{ .pg-green } Prise en charge de WireGuard

Proton VPN prend principalement en charge le protocole WireGuard®. [WireGuard](https://wireguard.com) est un protocole plus récent qui utilise une [cryptographie](https://wireguard.com/protocol) de pointe. De plus, WireGuard vise à être plus simple et plus performant.

Proton VPN [recommande](https://protonvpn.com/blog/wireguard) l'utilisation de WireGuard avec leur service. Sur les applications Windows, macOS, iOS, Android, ChromeOS et Android TV de Proton VPN, WireGuard est le protocole par défaut ; cependant, la [prise en charge](https://protonvpn.com/support/how-to-change-vpn-protocols) du protocole n'est pas présente dans leur application Linux.

#### :material-alert-outline:{ .pg-orange } Pas de prise en charge de l'IPv6

Les serveurs de Proton VPN ne sont compatibles qu'avec IPv4. Les applications Proton VPN bloqueront tout le trafic IPv6 sortant, de sorte que vous n'aurez pas à vous soucier de la fuite de votre adresse IPv6, mais vous ne pourrez pas vous connecter à des sites exclusivement IPv6, et vous ne pourrez pas vous connecter à Proton VPN à partir d'un réseau exclusivement IPv6.

#### :material-information-outline:{ .pg-info } Redirection de port

Proton VPN ne prend actuellement en charge que la [redirection de port](https://protonvpn.com/support/port-forwarding) éphémère via NAT-PMP, avec des durées de location de 60 secondes. L'application Windows offre une option facile d'accès, tandis que sur les autres systèmes d'exploitation, vous devrez exécuter votre propre [client NAT-PMP](https://protonvpn.com/support/port-forwarding-manual-setup). Les applications de torrent prennent souvent en charge NAT-PMP nativement.

#### :material-information-outline:{ .pg-blue } Anti-censure

Proton VPN a son protocole [Stealth](https://protonvpn.com/blog/stealth-vpn-protocol) qui *peut* aider dans les situations où les protocoles VPN comme OpenVPN ou Wireguard sont bloqués par diverses techniques rudimentaires. Stealth encapsule le tunnel VPN dans une session TLS afin de donner l'impression d'un trafic internet plus générique.

Malheureusement, il ne fonctionne pas très bien dans les pays où sont déployés des filtres sophistiqués qui analysent l'ensemble du trafic sortant pour tenter de découvrir les tunnels chiffrés. Stealth n'est également pas encore disponible sur [Windows](https://github.com/ProtonVPN/win-app/issues/64) ou Linux.

#### :material-check:{ .pg-green } Clients mobiles

En plus de fournir des fichiers de configuration OpenVPN standard, Proton VPN a des clients mobiles pour l'[App Store](https://apps.apple.com/app/id1437005085), [Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android), et [GitHub](https://github.com/ProtonVPN/android-app/releases) permettant des connexions faciles à leurs serveurs.

#### :material-information-outline:{ .pg-blue } Notes supplémentaires

Les clients Proton VPN prennent en charge l'authentification à deux facteurs sur toutes les plateformes. Proton VPN possède ses propres serveurs et centres de données en Suisse, en Islande et en Suède. Ils proposent le blocage des contenus et des domaines de logiciels malveillants connus avec leur service DNS. En outre, Proton VPN propose également des serveurs "Tor" vous permettant de vous connecter facilement aux sites onion, mais nous recommandons fortement d'utiliser [le navigateur officiel Tor](tor.md#tor-browser) à cette fin.

##### :material-alert-outline:{ .pg-orange } La fonction d'arrêt d'urgence ne fonctionne pas sur les Macs à processeur Intel

Des pannes système [peuvent se produire](https://protonvpn.com/support/macos-t2-chip-kill-switch) sur les Mac basés sur Intel lors de l'utilisation de l'arrêt d'urgence du VPN. Si vous avez besoin de cette fonction, et que vous utilisez un Mac avec un chipset Intel, vous devriez envisager d'utiliser un autre service VPN.

### IVPN

<div class="admonition recommendation" markdown>

![Logo IVPN](assets/img/vpn/ivpn.svg){ align=right }

**IVPN** est un autre fournisseur de VPN haut de gamme, et il est en activité depuis 2009. IVPN est basé à Gibraltar et ne propose pas d'essai gratuit.

[:octicons-home-16: Page d'accueil](https://ivpn.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ivpn.net/privacy){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://ivpn.net/knowledgebase/general){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ivpn){ .card-link title="Code source" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/net.ivpn.client)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1193122683)
- [:simple-windows11: Windows](https://ivpn.net/apps-windows)
- [:simple-apple: macOS](https://ivpn.net/apps-macos)
- [:simple-linux: Linux](https://ivpn.net/apps-linux)

</details>

</div>

#### :material-check:{ .pg-green } 37 pays

IVPN a des [serveurs dans 37 pays](https://ivpn.net/status).(1) Choisir un fournisseur VPN avec un serveur le plus proche de vous réduira la latence du trafic réseau que vous envoyez. Cela s'explique par un itinéraire plus court (moins de sauts) jusqu'à la destination.
{ .annotate }

1. Dernière vérification : 2024-04-02

Nous pensons également qu'il est préférable pour la sécurité des clés privées du fournisseur VPN d'utiliser des [serveurs dédiés](https://fr.wikipedia.org/wiki/Serveur_d%C3%A9di%C3%A9), plutôt que des solutions partagées (avec d'autres clients) moins chères telles que les [serveurs privés virtuels](https://fr.wikipedia.org/wiki/Serveur_d%C3%A9di%C3%A9_virtuel).

#### :material-check:{ .pg-green } Audit indépendant

IVPN a fait l'objet d'un [audit de non-journalisation par Cure53](https://cure53.de/audit-report_ivpn.pdf) qui a conclu à la validité de l'affirmation d'IVPN concernant l'absence de journaux. IVPN a également terminé un [rapport complet de test d'intrusion par Cure53](https://cure53.de/summary-report_ivpn_2019.pdf) en janvier 2020. IVPN a également indiqué qu'il prévoyait d'établir des [rapports annuels](https://ivpn.net/blog/independent-security-audit-concluded) à l'avenir. Une nouvelle étude a été réalisée [en avril 2022](https://ivpn.net/blog/ivpn-apps-security-audit-2022-concluded) et a été publiée par Cure53 [sur son site web](https://cure53.de/pentest-report_IVPN_2022.pdf).

#### :material-check:{ .pg-green } Clients open source

Depuis février 2020, [les applications IVPN sont désormais open-source](https://ivpn.net/blog/ivpn-applications-are-now-open-source). Le code source peut être obtenu auprès de leur [organisation GitHub](https://github.com/ivpn).

#### :material-check:{ .pg-green } Accepte l'argent liquide et le Monero

In addition to accepting credit/debit cards and PayPal, IVPN accepts Bitcoin, **Monero** and **cash/local currency** (on annual plans) as anonymous forms of payment. Prepaid cards with redeem codes are [also available](https://ivpn.net/knowledgebase/billing/voucher-cards-faq).

#### :material-check:{ .pg-green } Prise en charge de WireGuard

IVPN prend en charge le protocole WireGuard®. [WireGuard](https://wireguard.com) est un protocole plus récent qui utilise une [cryptographie](https://wireguard.com/protocol) de pointe. De plus, WireGuard vise à être plus simple et plus performant.

IVPN [recommande](https://ivpn.net/wireguard) l'utilisation de WireGuard avec leur service et, en tant que tel, le protocole est par défaut sur toutes les applications d'IVPN. IVPN propose également un générateur de configuration WireGuard à utiliser avec les [applications](https://wireguard.com/install) officielles WireGuard.

#### :material-information-outline:{ .pg-blue } Prise en charge de l'IPv6

IVPN vous permet de vous [connecter à des services en utilisant l'IPv6](https://ivpn.net/knowledgebase/general/do-you-support-ipv6) mais ne vous permet pas de vous connecter à partir d'un appareil utilisant une adresse IPv6.

#### :material-alert-outline:{ .pg-orange } Redirection de port

IVPN prenait auparavant en charge la redirection de port, mais a supprimé cette option en [juin 2023](https://ivpn.net/blog/gradual-removal-of-port-forwarding). L'absence de cette fonctionnalité pourrait avoir un impact négatif sur certaines applications, en particulier les applications pair-à-pair telles que les clients torrent.

#### :material-check:{ .pg-green } Anti-censure

IVPN dispose de modes d'obscurcissement utilisant le projet [v2ray](https://v2ray.com/en/index.html) qui aide dans les situations où les protocoles VPN comme OpenVPN ou Wireguard sont bloqués. Actuellement, cette fonctionnalité n'est disponible que sur bureau et [iOS](https://ivpn.net/knowledgebase/ios/v2ray). Elle dispose de deux modes d'utilisation de [VMess](https://guide.v2fly.org/en_US/basics/vmess.html) via des connexions QUIC ou TCP. QUIC est un protocole moderne avec un meilleur contrôle de la congestion et peut donc être plus rapide avec une latence réduite. Le mode TCP fait apparaître vos données comme du trafic HTTP normal.

#### :material-check:{ .pg-green } Clients mobiles

En plus de fournir des fichiers de configuration OpenVPN standard, IVPN a des clients mobiles pour l'[App Store](https://apps.apple.com/app/id1193122683), [Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client), et [GitHub](https://github.com/ivpn/android-app/releases) permettant des connexions faciles à leurs serveurs.

#### :material-information-outline:{ .pg-blue } Notes supplémentaires

Les clients IVPN prennent en charge l'authentification à deux facteurs. IVPN propose également la fonctionnalité "[AntiTraqueur](https://ivpn.net/antitracker)", qui bloque les réseaux publicitaires et les traqueurs au niveau du réseau.

### Mullvad

<div class="admonition recommendation" markdown>

![Logo Mullvad](assets/img/vpn/mullvad.svg){ align=right }

**Mullvad** est un VPN rapide et peu coûteux qui met l'accent sur la transparence et la sécurité. Ils sont en activité depuis **2009**. Mullvad est basé en Suède et n'a pas de période d'essai gratuit.

[:octicons-home-16: Page d'accueil](https://mullvad.net){ .md-button .md-button--primary }
[:simple-torbrowser:](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion){ .card-link title="Service onion" }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Politique de confidentialité" }
[:octicons-info-16:](https://mullvad.net/en/help){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/mullvad){ .card-link title="Code source" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1488466513)
- [:simple-github: GitHub](https://github.com/mullvad/mullvadvpn-app/releases)
- [:simple-windows11: Windows](https://mullvad.net/en/download/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/linux)

</details>

</div>

#### :material-check:{ .pg-green } 41 pays

Mullvad a des [serveurs dans 41 pays](https://mullvad.net/servers).(1) Choisir un fournisseur VPN avec un serveur le plus proche de vous réduira la latence du trafic réseau que vous envoyez. Cela s'explique par un itinéraire plus court (moins de sauts) jusqu'à la destination.
{ .annotate }

1. Dernière vérification : 2024-04-02

Nous pensons également qu'il est préférable pour la sécurité des clés privées du fournisseur VPN d'utiliser des [serveurs dédiés](https://fr.wikipedia.org/wiki/Serveur_d%C3%A9di%C3%A9), plutôt que des solutions partagées (avec d'autres clients) moins chères telles que les [serveurs privés virtuels](https://fr.wikipedia.org/wiki/Serveur_d%C3%A9di%C3%A9_virtuel).

#### :material-check:{ .pg-green } Audit indépendant

Les clients VPN de Mullvad ont été audités par Cure53 et Assured AB dans un rapport de test d'intrusion [publié sur cure53.de](https://cure53.de/pentest-report_mullvad_v2.pdf). Les chercheurs en sécurité ont conclu :

> Cure53 et Assured AB sont satisfaits des résultats de l'audit et le logiciel laisse une impression générale positive. Grâce au dévouement de l'équipe interne du complexe du VPN Mullvad, les testeurs n'ont aucun doute sur le fait que le projet est sur la bonne voie du point de vue de la sécurité.

En 2020, un deuxième audit [a été annoncé](https://mullvad.net/blog/2020/6/25/results-available-audit-mullvad-app) et le [rapport d'audit final](https://cure53.de/pentest-report_mullvad_2020_v2.pdf) a été publié sur le site web de Cure53 :

> Les résultats de ce projet de mai-juin 2020 ciblant le complexe de Mullvad sont assez positifs. [...] L'écosystème applicatif utilisé par Mullvad laisse une impression solide et structurée. La structure globale de l'application permet de déployer facilement des correctifs et corrections de manière structurée. Plus que tout, les résultats repérés par Cure53 montrent l'importance d'un audit et d'une réévaluation constante des vecteurs de fuite actuels, afin de toujours garantir la confidentialité des utilisateurs finaux. Ceci étant dit, Mullvad fait un excellent travail en protégeant l'utilisateur final contre les fuites courantes de DCP et les risques liés à la confidentialité.

En 2021, un audit des infrastructures [a été annoncé](https://mullvad.net/en/blog/2021/1/20/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit) et le [rapport d'audit final](https://cure53.de/pentest-report_mullvad_2021_v1.pdf) a été publié sur le site web de Cure53. Un autre rapport a été commandé [en juin 2022](https://mullvad.net/en/blog/2022/6/22/vpn-server-audit-found-no-information-leakage-or-logging-of-customer-data) et est disponible sur le [site web d'Assured](https://assured.se/publications/Assured_Mullvad_relay_server_audit_report_2022.pdf).

#### :material-check:{ .pg-green } Clients open source

Mullvad fournit le code source pour leurs clients de bureau et mobiles dans leur [organisation GitHub](https://github.com/mullvad/mullvadvpn-app).

#### :material-check:{ .pg-green } Accepte l'argent liquide et le Monero

Mullvad, in addition to accepting credit/debit cards and PayPal, accepts Bitcoin, Bitcoin Cash, **Monero** and **cash/local currency** as anonymous forms of payment. Prepaid cards with redeem codes are also available. Mullvad also accepts Swish and bank wire transfers.

#### :material-check:{ .pg-green } Prise en charge de WireGuard

Mullvad prend en charge le protocole WireGuard®. [WireGuard](https://wireguard.com) est un protocole plus récent qui utilise une [cryptographie](https://wireguard.com/protocol) de pointe. De plus, WireGuard vise à être plus simple et plus performant.

Mullvad [recommande](https://mullvad.net/en/help/why-wireguard) l'utilisation de WireGuard avec leur service. C'est le protocole par défaut ou le seul sur les applications Android, iOS, macOS et Linux de Mullvad, mais sur Windows vous devez [activer manuellement](https://mullvad.net/en/help/how-turn-wireguard-mullvad-app) WireGuard. Mullvad propose également un générateur de configuration WireGuard à utiliser avec les [applications](https://wireguard.com/install) officielles WireGuard.

#### :material-check:{ .pg-green } Prise en charge de l'IPv6

Mullvad vous permet d'[accéder à des services hébergés sur IPv6](https://mullvad.net/en/blog/2014/9/15/ipv6-support) et de vous connecter à partir d'un appareil utilisant une adresse IPv6.

#### :material-alert-outline:{ .pg-orange } Redirection de port

Mullvad prenait auparavant en charge la redirection de port, mais a supprimé cette option en [mai 2023](https://mullvad.net/en/blog/2023/5/29/removing-the-support-for-forwarded-ports). L'absence de cette fonctionnalité pourrait avoir un impact négatif sur certaines applications, en particulier les applications pair-à-pair telles que les clients torrent.

#### :material-check:{ .pg-green } Anti-censure

Mullvad dispose d'un mode d'obscurcissement utilisant [Shadowsocks avec v2ray](https://mullvad.net/en/help/shadowsocks-with-v2ray) qui peut être utile dans les situations où les protocoles VPN comme OpenVPN ou Wireguard sont bloqués.

#### :material-check:{ .pg-green } Clients mobiles

Mullvad a publié des clients [App Store](https://apps.apple.com/app/id1488466513) et [Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn), tous deux avec une interface simple à utiliser plutôt que nécessiter de votre part une configuration manuelle de votre connexion WireGuard. Le client Android est également disponible sur [GitHub](https://github.com/mullvad/mullvadvpn-app/releases).

#### :material-information-outline:{ .pg-blue } Notes supplémentaires

Mullvad est très transparent quant aux nœuds qu'il [possède ou qu'il loue](https://mullvad.net/en/servers). Ils utilisent [ShadowSocks](https://shadowsocks.org) dans leur configuration ShadowSocks + OpenVPN, ce qui les rend plus résistants aux pare-feux avec de l'[inspection profonde de paquets](https://en.wikipedia.org/wiki/Deep_packet_inspection) qui tentent de bloquer les VPN. Il semblerait que [la Chine utilise une méthode différente pour bloquer les serveurs ShadowSocks](https://github.com/net4people/bbs/issues/22).

## Critères

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

Il est important de noter que l'utilisation d'un fournisseur VPN ne vous rendra pas anonyme, mais qu'elle vous permettra de mieux protéger votre vie privée dans certaines situations. Un VPN n'est pas un outil pour des activités illégales. Ne vous fiez pas à une politique de "non-journalisation".

</div>

**Veuillez noter que nous ne sommes affiliés à aucun des fournisseurs que nous recommandons. Cela nous permet de fournir des recommandations totalement objectives.** En plus de [nos critères standards](about/criteria.md), nous avons développé un ensemble d'exigences claires pour tout fournisseur de VPN souhaitant être recommandé, y compris un chiffrement fort, des audits de sécurité indépendants, une technologie moderne, et plus encore. Nous vous suggérons de vous familiariser avec cette liste avant de choisir un fournisseur VPN, et de mener vos propres recherches pour vous assurer que le fournisseur VPN que vous choisissez est le plus digne de confiance possible.

### Technologie

Nous exigeons de tous nos fournisseurs VPN recommandés qu'ils fournissent des fichiers de configuration OpenVPN utilisables dans n'importe quel client. **Si** un VPN fournit son propre client personnalisé, nous exigeons un killswitch pour bloquer les fuites de données du réseau lors de la déconnexion.

**Minimum pour se qualifier :**

- Prise en charge de protocoles forts tels que WireGuard & OpenVPN.
- Arrêt d'urgence intégré dans les clients.
- Prise en charge du multi-sauts. Le multi-sauts est important pour garder les données privées en cas de compromission d'un seul noeud.
- Si des clients VPN sont fournis, ils doivent être [open source](https://en.wikipedia.org/wiki/Open_source), comme le logiciel VPN qui y est généralement intégré. Nous pensons que la disponibilité du [code source](https://en.wikipedia.org/wiki/Source_code) offre une plus grande transparence sur ce que fait réellement votre appareil.

**Dans le meilleur des cas :**

- Un arrêt d'urgence avec des options hautement configurables (activer/désactiver sur certains réseaux, au démarrage, etc.)
- Clients VPN faciles à utiliser
- Prend en charge [IPv6](https://en.wikipedia.org/wiki/IPv6). Nous nous attendons à ce que les serveurs autorisent les connexions entrantes via IPv6 et vous permettent d'accéder aux services hébergés sur des adresses IPv6.
- La capacité de [transfert de port à distance](https://en.wikipedia.org/wiki/Port_forwarding#Remote_port_forwarding) aide à créer des connexions lors de l'utilisation de logiciels de partage de fichiers P2P ([Peer-to-Peer](https://en.wikipedia.org/wiki/Peer-to-peer)) ou de l'hébergement d'un serveur (par exemple, Mumble).
- Technologie d'obscurcissement qui remplit les paquets de données avec des données aléatoires afin de contourner la censure sur l'internet.

### Confidentialité

Nous préférons que nos prestataires recommandés collectent le moins de données possible. Ne pas recueillir de renseignements personnels sur l'inscription et accepter des modes de paiement anonymes sont requis.

**Minimum pour se qualifier :**

- Option de paiement en [crypto-monnaie anonyme](cryptocurrency.md) **ou** en espèces.
- Aucune information personnelle requise pour s'inscrire : seuls le nom d'utilisateur, le mot de passe et l'e-mail sont requis.

**Dans le meilleur des cas :**

- Accepte plusieurs [options de paiement anonymes](advanced/payments.md).
- Aucune information personnelle acceptée (nom d'utilisateur généré automatiquement, pas d'email requis, etc.).

### Sécurité

Un VPN est inutile s'il ne peut même pas fournir une sécurité adéquate. Nous exigeons de tous nos fournisseurs recommandés qu'ils respectent les normes de sécurité en vigueur pour leurs connexions OpenVPN. Idéalement, ils utiliseraient par défaut des schémas de chiffrement plus évolutifs. Nous exigeons également qu'un tiers indépendant procède à un audit de la sécurité du fournisseur, idéalement de manière très complète et de manière répétée (chaque année).

**Minimum pour se qualifier :**

- Schémas de chiffrement forts : OpenVPN avec authentification SHA-256 ; poignée de main RSA-2048 ou mieux ; chiffrement des données AES-256-GCM ou AES-256-CBC.
- Confidentialité persistante.
- Des audits de sécurité publiés par une société tierce réputée.

**Dans le meilleur des cas :**

- Chiffrement le plus fort : RSA-4096.
- Confidentialité persistante.
- Des audits de sécurité complets publiés par une société tierce réputée.
- Des programmes de primes aux bugs et/ou un processus coordonné de divulgation des vulnérabilités.

### Confiance

Vous ne confieriez pas vos finances à une personne ayant une fausse identité, alors pourquoi lui confier vos données internet ? Nous exigeons de nos fournisseurs recommandés qu'ils rendent public leur propriété ou leur direction. Nous aimerions également voir des rapports de transparence fréquents, notamment en ce qui concerne la manière dont les demandes de gouvernement sont traitées.

**Minimum pour se qualifier :**

- Une direction ou un propriétaire public.

**Dans le meilleur des cas :**

- Une direction publique.
- Rapports de transparence fréquents.

### Marketing

Avec les fournisseurs de VPN que nous recommandons, nous aimons voir un marketing responsable.

**Minimum pour se qualifier :**

- Doit héberger lui-même ses outils d'analyse de traffic (pas de Google Analytics, etc.). Le site du fournisseur doit également se conformer à [DNT (Do Not Track)](https://en.wikipedia.org/wiki/Do_Not_Track) pour les personnes qui souhaitent se désinscrire.

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

Bien qu'il ne s'agisse pas d'exigences strictes, nous avons tenu compte de certains facteurs pour déterminer les fournisseurs à recommander. Ceux-ci incluent la fonctionnalité de blocage de contenus, les canaris de mandats, les connexions multi-sauts, un excellent support client, le nombre de connexions simultanées autorisées, etc.
