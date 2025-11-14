---
meta_title: "Recommandations et comparaison de services VPN privés, sans sponsors ni publicités - Privacy Guides"
title: Services VPN
icon: material/vpn
description: Les meilleurs services VPN pour protéger votre vie privée et votre sécurité en ligne. Trouvez ici un fournisseur qui ne cherche pas à vous espionner.
cover: vpn.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>Protège contre la (les) menace(s) suivante(s) :</small>

- [:material-account-cash: Capitalisme de surveillance](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Si vous recherchez plus de *confidentialité* vis-à-vis de votre fournisseur d'accès à Internet, sur un réseau Wi-Fi public ou lorsque vous téléchargez des fichiers en torrent, un **VPN** peut être la solution qu'il vous faut.

<div class="admonition danger" markdown>
<p class="admonition-title">Les VPN ne garantissent pas l'anonymat</p>

L'utilisation d'un VPN n'assure **pas** l'anonymat de vos habitudes de navigation et n'ajoute pas de sécurité supplémentaire au trafic non sécurisé (HTTP).

Si vous recherchez l'**anonymat**, vous devriez utiliser le navigateur Tor. Si vous recherchez une **sécurité** supplémentaire, vous devriez toujours vous assurer que vous vous connectez à des sites web en utilisant HTTPS. Un VPN ne se substitue pas à de bonnes pratiques de sécurité.

[Introduction au Navigateur Tor](tor.md#tor-browser){ .md-button .md-button--primary } [Tor : mythes & FAQ](advanced/tor-overview.md){ .md-button }

</div>

[Présentation détaillée des VPNs :material-arrow-right-drop-circle:](basics/vpn-overview.md ""){.md-button}

## Fournisseurs recommandés

Les fournisseurs que nous recommandons utilisent le cryptage, supportent WireGuard & OpenVPN, et ont une politique de non journalisation. Lisez notre \[liste complète de critères\](#criteres) pour plus d'informations.

| Fournisseur           | Pays | WireGuard                     | Redirection de port                                               | IPv6                                                               | Paiements anonymes                     |
| --------------------- | ---- | ----------------------------- | ----------------------------------------------------------------- | ------------------------------------------------------------------ | -------------------------------------- |
| [Proton](#proton-vpn) | 127+ | :material-check:{ .pg-green } | :material-alert-outline: { .pg-orange } Prise en charge partielle | :material-information-outline:{ .pg-blue } Prise en charge limitée | Cash Monero via une application tierce |
| [IVPN](#ivpn)         | 41+  | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                            | :material-information-outline:{ .pg-blue } Sortant seulement       | Monero  Cash                           |
| [Mullvad](#mullvad)   | 49+  | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                            | :material-check:{ .pg-green }                                      | Monero  Cash                           |

### Proton VPN

<div class="admonition recommendation" markdown>

![Proton VPN logo](assets/img/vpn/protonvpn.svg){ align=right }

**Proton VPN** est un concurrent de poids dans l'espace VPN, et il est en service depuis 2016. Proton AG est basé en Suisse et propose une offre gratuite limitée, ainsi qu'une option premium plus complète.

[:octicons-home-16: Page d'Accueil](https://protonvpn.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://protonvpn.com/privacy-policy){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://protonvpn.com/support){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/ProtonVPN){ .card-link title="Code Source" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-googleplay: Play Store](https://play.google.com/store/apps/details?id=ch.protonvpn.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1437005085)
- [:simple-github: GitHub](https://github.com/ProtonVPN/android-app/releases)
- [:fontawesome-brands-windows: Windows](https://protonvpn.com/download-windows)
- [:simple-apple: macOS](https://protonvpn.com/download-macos)
- [:simple-linux: Linux](https://protonvpn.com/support/linux-vpn-setup)

</details>

</div>

#### :material-check:{ .pg-green } 127 Pays

Proton VPN a des [serveurs dans 127 pays](https://protonvpn.com/fr/vpn-servers)(1) ou [10](https://protonvpn.com/support/fr/how-to-create-free-vpn-account) si vous utilisez leur [plan gratuit](https://protonvpn.com/blog/fr/product-roadmap-winter-2025-2026).(2) Choisir un fournisseur VPN avec un serveur le plus proche de vous réduira la latence du trafic réseau que vous envoyez. Cela est dû à un itinéraire plus court (moins de sauts) vers la destination.
{ .annotate }

1. Dont au moins 71 sont des serveurs virtuels, ce qui signifie que votre IP apparaîtra comme provenant d'un pays, mais que le serveur se trouve dans un autre. 12 autres sites disposent à la fois de serveurs matériels et virtuels. [Source](https://protonvpn.com/support/fr/how-smart-routing-works)
2. Dernière vérification : 2025-10-28

Nous pensons également qu'il est préférable pour la sécurité des clés privées du fournisseur VPN d'utiliser des [serveurs dédiés](https://fr.wikipedia.org/wiki/Serveur_d%C3%A9di%C3%A9), plutôt que des solutions partagées (avec d'autres clients) moins chères telles que les [serveurs privés virtuels](https://fr.wikipedia.org/wiki/Serveur_d%C3%A9di%C3%A9_virtuel).

#### :material-check:{ .pg-green } Audit indépendant

Le chercheur indépendant en sécurité numérique Ruben Santamarta a mené un audit des [extensions de navigateur](https://drive.proton.me/urls/RWDD2SHT98#v7ZrwNcafkG8) et [des applications](https://drive.proton.me/urls/RVW8TXG484#uTXX5Fc9GADo) de Proton VPN en septembre 2024 et janvier 2025, respectivement. L'infrastructure de Proton VPN fait l'objet d'[audits annuels](https://protonvpn.com/blog/no-logs-audit) par Securitum depuis 2022.

En janvier 2020., Proton VPN a fait l'objet d'un audit indépendant par SEC Consult. SEC Consult a trouvé quelques vulnérabilités à risque moyen et faible dans les applications Windows, Android et iOS de Proton VPN, qui ont toutes été "correctement corrigées" par Proton VPN avant la publication des rapports. Aucun des problèmes identifiés n'aurait permis à un attaquant d'accéder à distance à votre appareil ou à votre trafic. Vous pouvez consulter leur rapport sur chaque plateforme de Proton VPN dans leur [post de blog](https://web.archive.org/web/20250307041036/https://protonvpn.com/blog/open-source) dédié à l'audit.

#### :material-check:{ .pg-green } Clients open source

Proton VPN a mis à disposition le code source de leurs clients mobile et bureau dans leur [organisation GitHub](https://github.com/ProtonVPN).

#### :material-check:{ .pg-green } Accepte l'argent liquide

En plus d'accepter les paiements par carte bancaires, Paypal et [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), Proton VPN accepte également les **espèces/monnaie locale** comme forme de paiement anonyme. Vous pouvez également utiliser [**Monero**](cryptocurrency.md#monero) pour acheter des bons d'achat pour Proton VPN Plus et Proton Unlimited via leur revendeur [officiel](https://discuss.privacyguides.net/t/add-monero-as-an-anonymous-payment-method-for-proton-services/31058/15), [ProxyStore](https://dys2p.com/en/2025-09-09-proton.html).

#### :material-check:{ .pg-green } Prise en charge de WireGuard

Proton VPN supporte le protocole WireGuard®. [WireGuard](https://wireguard.com) est un protocole plus récent qui utilise une [cryptographie](https://wireguard.com/protocol) de pointe. De plus, WireGuard vise à être plus simple et plus performant.

Proton VPN [recommande](https://protonvpn.com/blog/wireguard) l'utilisation de WireGuard avec leur service. Proton VPN offre également un générateur de configuration WireGuard à utiliser avec les [applications officielles WireGuard](https://wireguard.com/install).

#### :material-alert-outline:{ .pg-orange } Prise en charge limitée de l'IPv6

Proton [supporte désormais l'IPv6](https://protonvpn.com/support/prevent-ipv6-vpn-leaks) dans leur extension de navigateur et leur client Linux, mais seul 80% de leurs serveurs sont compatibles IPv6. Les applications Proton VPN bloqueront tout le trafic IPv6 sortant, de sorte que vous n'aurez pas à vous soucier de la fuite de votre adresse IPv6, mais vous ne pourrez pas vous connecter à des sites exclusivement IPv6, et vous ne pourrez pas vous connecter à Proton VPN à partir d'un réseau exclusivement IPv6.

#### :material-information-outline:{ .pg-info } Redirection de port

Proton VPN ne prend actuellement en charge que la [redirection de port](https://protonvpn.com/support/port-forwarding) éphémère via NAT-PMP, avec des durées de location de 60 secondes. Les applications officielles Windows et Linux offrent une option facile d'accès, tandis que sur d'autres systèmes d'exploitation, vous devrez exécuter votre propre [client NAT-PMP](https://protonvpn.com/support/port-forwarding-manual-setup). Les applications de torrent prennent souvent en charge NAT-PMP nativement.

#### :material-information-outline:{ .pg-blue } Anti-censure

Proton VPN propose son propre protocole nommé [Stealth](https://protonvpn.com/blog/stealth-vpn-protocol) qui *peut* aider dans certaines situations où les protocoles VPN comme OpenVPN ou WireGuard sont bloqués avec diverses techniques rudimentaires. Stealth encapsule le tunnel VPN dans une session TLS afin de donner l'impression d'un trafic internet plus générique.

Malheureusement, il ne fonctionne pas très bien dans des pays où des filtres sophistiqués analysant tout le trafic sortant sont déployés, pour tenter de découvrir les tunnels chiffrés. Le protocole Stealth est disponible sur Android, iOS, Windows et macOS, mais n'est pas encore disponible sur Linux.

#### :material-check:{ .pg-green } Clients mobiles

Proton VPN propose son client mobile sur l'[App Store](https://apps.apple.com/fr/app/id1437005085) et sur le [Google Play Store](https://play.google.com/store/apps/details?id=ch.protonvpn.android), doté d'une interface conviviale qui ne nécessite pas une configuration manuelle de votre connexion WireGuard. La version Android du client est également disponible sur [GitHub](https://github.com/ProtonVPN/android-app/releases).

<div class="admonition warning" markdown>
<p class="admonition-title">Comment refuser le partage des données de télémétries</p>

Sur Android, Proton cache les paramètres de télémétrie sous le label trompeur de "**Aidez-nous à combattre la censure**". Sur les autres plateformes, ces paramètres se trouvent dans le menu « **Statistiques d'utilisation** ».

Nous tenons à le signaler car, bien que nous ne déconseillions pas nécessairement le partage de statistiques d'utilisation anonymes avec les développeurs, il est important que ces paramètres soient faciles à trouver et clairement identifiés.

</div>

#### :material-information-outline:{ .pg-blue } Notes supplémentaires

Les clients Proton VPN prennent en charge l'authentification à deux facteurs sur toutes les plateformes. Proton VPN possède ses propres serveurs et centres de données en Suisse, en Islande et en Suède. Ils proposent le blocage des contenus et des domaines de logiciels malveillants connus avec leur service DNS. En outre, Proton VPN propose également des serveurs "Tor" vous permettant de vous connecter facilement aux sites onion, mais nous recommandons fortement d'utiliser [le navigateur officiel Tor](tor.md#tor-browser) à cette fin.

##### :material-alert-outline:{ .pg-orange } La fonction "Arrêt d'Urgence" ne fonctionne pas sur les Macs Intel.

Des crashs système[peuvent se produire](https://protonvpn.com/support/macos-t2-chip-kill-switch) sur les Mac basés sur Intel lors de l'utilisation de la fonction "Arrêt d'Urgence" Si vous avez besoin de cette fonction, et que vous utilisez un Mac avec un chipset Intel, vous devriez envisager d'utiliser un autre service VPN.

### IVPN

<div class="admonition recommendation" markdown>

![Logo IVPN](assets/img/vpn/ivpn.svg){ align=right }

**IVPN** est un autre fournisseur de VPN haut de gamme, et il est en activité depuis 2009. IVPN est basé à Gibraltar et ne propose pas d'essai gratuit.

[:octicons-home-16: Page d'Accueil](https://ivpn.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ivpn.net/privacy){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://ivpn.net/knowledgebase/general){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/ivpn){ .card-link title="Code Source" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client)
- [:simple-appstore: App Store](https://apps.apple.com/fr/app/id1193122683)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/net.ivpn.client)
- [:simple-github: GitHub](https://github.com/ivpn/android-app/releases)
- [:fontawesome-brands-windows: Windows](https://ivpn.net/apps-windows)
- [:simple-apple: macOS](https://ivpn.net/apps-macos)
- [:simple-linux: Linux](https://ivpn.net/apps-linux)

</details>

</div>

#### :material-check:{ .pg-green } 41 pays

IVPN a des [serveurs dans 41 pays](https://ivpn.net/status)(1). Choisir un fournisseur de VPN avec un serveur le plus proche de vous réduira la latence du trafic réseau que vous envoyez. Cela s'explique par un itinéraire plus court (moins de sauts) jusqu'à la destination.
{ .annotate }

1. Dernière vérification : 2025-10-28

Nous pensons également qu'il est préférable pour la sécurité des clés privées du fournisseur VPN d'utiliser des [serveurs dédiés](https://fr.wikipedia.org/wiki/Serveur_d%C3%A9di%C3%A9), plutôt que des solutions partagées (avec d'autres clients) moins chères telles que les [serveurs privés virtuels](https://fr.wikipedia.org/wiki/Serveur_d%C3%A9di%C3%A9_virtuel).

#### :material-check:{ .pg-green } Audit indépendant

IVPN a fait l'objet de plusieurs [audits indépendants](https://ivpn.net/en/blog/tags/audit) depuis 2019 et a annoncé publiquement son engagement à se soumettre à [des audits de sécurité annuels](https://ivpn.net/blog/ivpn-apps-security-audit-concluded).

#### :material-check:{ .pg-green } Clients open source

Depuis février 2020, [les applications IVPN sont désormais open-source](https://ivpn.net/blog/ivpn-applications-are-now-open-source). Le code source peut être obtenu auprès de leur [organisation GitHub](https://github.com/ivpn).

#### :material-check:{ .pg-green } Accepte l'argent liquide et le Monero

En plus d'accepter les cartes de crédit/débit et PayPal, IVPN accepte le Bitcoin, **le Monero** et **les espèces/la monnaie locale** (sur les abonnements annuels) comme formes de paiement anonymes. Vous pouvez également acheter des [cartes prépayées](https://ivpn.net/knowledgebase/billing/voucher-cards-faq) avec des codes d'échange.

#### :material-check:{ .pg-green } Prise en charge de WireGuard

IVPN prend en charge le protocole WireGuard®. [WireGuard](https://wireguard.com) est un protocole plus récent qui utilise une [cryptographie](https://wireguard.com/protocol) de pointe. De plus, WireGuard vise à être plus simple et plus performant.

IVPN [recommande](https://ivpn.net/wireguard) l'utilisation de WireGuard avec leur service et, en tant que tel, le protocole est par défaut sur toutes les applications d'IVPN. IVPN propose également un générateur de configuration WireGuard à utiliser avec les [applications](https://wireguard.com/install) officielles WireGuard.

#### :material-information-outline:{ .pg-blue } Prise en charge de l'IPv6

IVPN vous permet de vous [connecter à des services en utilisant l'IPv6](https://ivpn.net/knowledgebase/general/do-you-support-ipv6) mais ne vous permet pas de vous connecter à partir d'un appareil utilisant une adresse IPv6.

#### :material-alert-outline:{ .pg-orange } Redirection de port

IVPN prenait auparavant en charge la redirection de port, mais a supprimé cette option en [juin 2023](https://ivpn.net/blog/gradual-removal-of-port-forwarding). L'absence de cette fonctionnalité pourrait avoir un impact négatif sur certaines applications, en particulier les applications pair-à-pair telles que les clients torrent.

#### :material-check:{ .pg-green } Anti-censure

IVPN utilise [V2Ray](https://v2ray.com/en/index.html) pour offusquer (cacher la vraie nature) le trafic internet, ce qui est utile dans les situations où OpenVPN et WireGuard sont bloqués. Pour le moment, cette fonctionnalité est disponible uniquement sur PC et sur [iOS](https://ivpn.net/knowledgebase/ios/v2ray). Elle dispose de deux modes d'utilisation de [VMess](https://guide.v2fly.org/en_US/basics/vmess.html) via des connexions QUIC ou TCP. QUIC est un protocole moderne avec un meilleur contrôle de la congestion et peut donc être plus rapide avec une latence réduite. Le mode TCP fait apparaître vos données comme du trafic HTTP normal.

#### :material-check:{ .pg-green } Clients mobiles

IVPN propose son client mobile sur l'[App Store](https://apps.apple.com/fr/app/id1193122683) et sur le [Google Play Store](https://play.google.com/store/apps/details?id=net.ivpn.client), doté d'une interface conviviale qui ne nécessite pas une configuration manuelle de votre connexion WireGuard. La version Android du client est également disponible sur [GitHub](https://github.com/ivpn/android-app/releases).

#### :material-information-outline:{ .pg-blue } Notes supplémentaires

Les clients IVPN prennent en charge l'authentification à deux facteurs. IVPN propose également la fonctionnalité "[AntiTraqueur](https://ivpn.net/antitracker)", qui bloque les réseaux publicitaires et les traqueurs au niveau du réseau.

### Mullvad

<div class="admonition recommendation" markdown>

![Logo Mullvad](assets/img/vpn/mullvad.svg){ align=right }

**Mullvad** est un VPN rapide et peu coûteux qui met l'accent sur la transparence et la sécurité. Ils sont en activité depuis 2009. Mullvad est basé en Suède et offre une garantie de remboursement de 14 jours pour les [méthodes de paiement] (https://mullvad.net/fr/help/refunds) qui le permettent.

[:octicons-home-16: Page d'Accueil](https://mullvad.net){ .md-button .md-button--primary }
[:simple-torbrowser:](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion){ .card-link title="Service Onion" }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Politique de Confidentialité" }
[:octicons-info-16:](https://mullvad.net/en/help){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/mullvad){ .card-link title="Code Source" }

<details class="downloads" markdown>
<summary>Téléchargements</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn)
- [:simple-appstore: App Store](https://apps.apple.com/fr/app/id1488466513)
- [:simple-github: GitHub](https://github.com/mullvad/mullvadvpn-app/releases)
- [:fontawesome-brands-windows: Windows](https://mullvad.net/fr/download/vpn/windows)
- [:simple-apple: macOS](https://mullvad.net/fr/download/vpn/macos)
- [:simple-linux: Linux](https://mullvad.net/fr/download/vpn/linux)

</details>

</div>

#### :material-check: 49 Pays

Mullvad a [ des serveurs dans 49 pays](https://mullvad.net/fr/servers).(1) Choisir un fournisseur VPN avec un serveur proche de votre position géographique réduira la latence du trafic réseau entre vous et ce serveur. Cela s'explique par un itinéraire plus court (moins de sauts) jusqu'à la destination.
{ .annotate }

1. Dernière vérification : 2025-10-28

Nous pensons également qu'il est préférable pour la sécurité des clés privées du fournisseur VPN d'utiliser des [serveurs dédiés](https://fr.wikipedia.org/wiki/Serveur_d%C3%A9di%C3%A9), plutôt que des solutions partagées (avec d'autres clients) moins chères telles que les [serveurs privés virtuels](https://fr.wikipedia.org/wiki/Serveur_d%C3%A9di%C3%A9_virtuel).

#### :material-check:{ .pg-green } Audit indépendant

Mullvad a fait l'objet de plusieurs [audits indépendants](https://mullvad.net/fr/blog/tag/audits) et a annoncé publiquement son intention de procéder à [des audits de sécurité annuels](https://mullvad.net/fr/blog/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit) de leurs applications et de leurs infrastructures.

#### :material-check:{ .pg-green } Clients open source

Mullvad fournit le code source pour leurs clients de bureau et mobiles dans leur [organisation GitHub](https://github.com/mullvad/mullvadvpn-app).

#### :material-check:{ .pg-green } Accepte l'argent liquide et le Monero

Mullvad, en plus d'accepter les cartes de crédit/débit et PayPal, accepte le Bitcoin, le Bitcoin Cash, **le Monero** et **les espèces/la monnaie locale** comme formes de paiement anonymes. Vous pouvez également acheter des [cartes prépayées](https://mullvad.net/en/help/partnerships-and-resellers) avec des codes à échanger. Mullvad accepte également les virements Swish et les virements bancaires, ainsi que certains systèmes de paiement européens.

#### :material-check:{ .pg-green } Prise en charge de WireGuard

Mullvad prend en charge le protocole WireGuard®. [WireGuard](https://wireguard.com) est un protocole plus récent qui utilise une [cryptographie](https://wireguard.com/protocol) de pointe. De plus, WireGuard vise à être plus simple et plus performant.

Mullvad [recommande](https://mullvad.net/en/help/why-wireguard) l'utilisation de WireGuard avec leur service. C'est le seul protocole pris en charge par leurs applications mobiles, et leurs applications de bureau [ne prendront plus en charge OpenVPN](https://mullvad.net/fr/blog/reminder-that-openvpn-is-being-removed) en 2025. En outre, leurs serveurs cesseront d'accepter les connexions OpenVPN d'ici au 15 janvier 2026. Mullvad propose également un générateur de configuration WireGuard à utiliser avec les [applications](https://wireguard.com/install) officielles WireGuard.

#### :material-check:{ .pg-green } Prise en charge de l'IPv6

Mullvad vous permet d'[accéder à des services hébergés sur IPv6](https://mullvad.net/en/blog/2014/9/15/ipv6-support) et de vous connecter à partir d'un appareil utilisant une adresse IPv6.

#### :material-alert-outline:{ .pg-orange } Redirection de port

Mullvad prenait auparavant en charge la redirection de port, mais a supprimé cette option en [mai 2023](https://mullvad.net/en/blog/2023/5/29/removing-the-support-for-forwarded-ports). L'absence de cette fonctionnalité pourrait avoir un impact négatif sur certaines applications, en particulier les applications pair-à-pair telles que les clients torrent.

#### :material-check:{ .pg-green } Anti-censure

Mullvad offre plusieurs fonctionnalités permettant de contourner la censure et d'accéder librement à Internet :

- **Mode d'offuscation**: Mullvad propose deux modes d'offuscation intégrés : "UDP-sur-TCP" et ["Wireguard sur Shadowsocks](https://mullvad.net/fr/blog/introducing-shadowsocks-obfuscation-for-wireguard). Ces modes déguisent votre trafic VPN en trafic web normal, ce qui le rend plus difficile à détecter et à bloquer pour les organismes de censure. Il semblerait que la Chine utilise une [nouvelle méthode pour perturber le trafic acheminé via le protocole Shadowsocks](https://gfw.report/publications/usenixsecurity23/en).
- **Offuscation avancée avec Shadowsocks et v2ray**: Pour les utilisateurs plus avancés, Mullvad fournit un guide sur l'utilisation du plugin [Shadowsocks with v2ray](https://mullvad.net/fr/help/shadowsocks-with-v2ray) avec les clients Mullvad. Cette configuration fournit une couche supplémentaire d'offuscation et de chiffrement.
- **IP de serveur personnalisé**: Pour contrer le blocage d'IP, vous pouvez demander des IP de serveur personnalisée à l'équipe d'assistance de Mullvad. Une fois que vous avez reçu les adresses IP personnalisées, vous pouvez entrer le fichier texte dans les paramètres « Server IP override », ce qui remplacera les adresses IP du serveur choisi par des adresses qui ne sont pas connues du système de censure.
- **Ponts et proxies** : Mullvad vous permet également d'utiliser des ponts ou des proxies pour accéder à son API (nécessaire pour l'authentification), ce qui peut aider à contourner les tentatives de censure qui bloquent l'accès à l'API elle-même.

#### :material-check:{ .pg-green } Clients mobiles

Mullvad a publié des clients [App Store](https://apps.apple.com/app/id1488466513) et [Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn), tous deux avec une interface simple à utiliser plutôt que nécessiter de votre part une configuration manuelle de votre connexion WireGuard. Le client Android est également disponible sur [GitHub](https://github.com/mullvad/mullvadvpn-app/releases).

#### :material-information-outline:{ .pg-blue } Notes supplémentaires

Mullvad est très transparent quant aux nœuds qu'il [possède ou qu'il loue](https://mullvad.net/en/servers). Ils offrent également la possibilité d'activer l'option "Défense contre l'analyse du trafic guidée par IA" ([DAITA en anglais](https://mullvad.net/fr/blog/daita-defense-against-ai-guided-traffic-analysis)) dans leurs applications. Cette option est une protection contre la menace de l'analyse avancée du trafic, qui peut être utilisée pour relier des modèles de trafic VPN à des sites web spécifiques.

## Critères

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

Il est important de noter que l'utilisation d'un fournisseur VPN ne vous rendra pas anonyme, mais qu'elle vous permettra de mieux protéger votre vie privée dans certaines situations. Un VPN n'est pas un outil pour des activités illégales. Ne vous fiez pas à une politique de "non-journalisation".

</div>

**Veuillez noter que nous ne sommes affiliés à aucun des fournisseurs que nous recommandons. Cela nous permet de fournir des recommandations totalement objectives.** En plus de [nos critères standards](about/criteria.md), nous avons développé un ensemble d'exigences claires pour tout fournisseur de VPN souhaitant être recommandé, y compris un chiffrement fort, des audits de sécurité indépendants, une technologie moderne, et plus encore. Nous vous suggérons de vous familiariser avec cette liste avant de choisir un fournisseur VPN, et de mener vos propres recherches pour vous assurer que le fournisseur VPN que vous choisissez est le plus digne de confiance possible.

### Technologie

Nous demandons à tous les fournisseurs de VPN que nous recommandons de fournir des fichiers de configuration standard qui peuvent être utilisés dans un client générique à code source ouvert. <strong x-id=« 1 »>Si</strong> un VPN fournit son propre client personnalisé, nous exigeons une fonction d'arrêt d'urgence ("kill switch") pour bloquer les fuites de données du réseau en cas de déconnexion.

**Minimum pour se qualifier :**

- Prise en charge de protocoles robustes tels que WireGuard.
- Fonction d'arrêt d'urgence (kill switch) intégrée aux clients
- Prise en charge du multi-hop. Le multi-hop est important pour préserver la confidentialité des données en cas de compromission d'un seul nœud.
- Si des clients VPN sont fournis, ils doivent être [open source](https://en.wikipedia.org/wiki/Open_source), comme le logiciel VPN qui y est généralement intégré. Nous pensons que la disponibilité du [code source](https://fr.wikipedia.org/wiki/Code_source) offre une plus grande transparence sur les activités réelles du programme.
- Fonctions de résistance à la censure conçues pour contourner les pare-feux sans Inspection Profonde des Paquets (IPP)

**Dans le meilleur des cas :**

- Fonction d'arrêt d'urgence avec des options hautement configurables (activation/désactivation sur certains réseaux, au démarrage, etc.)
- Clients VPN faciles à utiliser
- Prise en charge de l'[IPV6](https://fr.wikipedia.org/wiki/IPv6). Nous nous attendons à ce que les serveurs autorisent les connexions entrantes via IPv6 et vous permettent d'accéder aux services hébergés sur des adresses IPv6.
- La capacité de [transfert de port à distance](https://en.wikipedia.org/wiki/Port_forwarding#Remote_port_forwarding) aide à créer des connexions lors de l'utilisation de logiciels de partage de fichiers P2P ([Peer-to-Peer](https://en.wikipedia.org/wiki/Peer-to-peer)) ou de l'hébergement d'un serveur (par exemple, Mumble).
- Technologie d'offuscation qui camoufle la vraie nature du trafic internet, conçue pour contourner les méthodes avancées de censure de l'internet telles que l'IPP.

### Confidentialité

Nous préférons que nos prestataires recommandés collectent le moins de données possible. Ne pas recueillir de renseignements personnels sur l'inscription et accepter des modes de paiement anonymes sont requis.

**Minimum pour se qualifier :**

- Option de paiement en [crypto-monnaie anonyme](cryptocurrency.md) **ou** en espèces.
- Aucune information personnelle requise pour s'inscrire : seuls le nom d'utilisateur, le mot de passe et l'e-mail sont requis.

**Dans le meilleur des cas :**

- Accepte plusieurs [options de paiement anonymes](advanced/payments.md).
- Aucune information personnelle n'est acceptée (nom d'utilisateur généré automatiquement, pas d'email requis, etc.)

### Sécurité

Un VPN est inutile s'il ne peut même pas fournir une sécurité adéquate. Nous exigeons de tous les fournisseurs que nous recommandons qu'ils respectent les normes de sécurité en vigueur. Idéalement, ils utiliseraient par défaut des schémas de chiffrement plus évolutifs. Nous exigeons également qu'un tiers indépendant procède à un audit de la sécurité du fournisseur, idéalement de manière très complète et de manière répétée (chaque année).

**Minimum pour se qualifier :**

- Schémas de chiffrement forts : OpenVPN avec authentification SHA-256 ; poignée de main RSA-2048 ou mieux ; chiffrement des données AES-256-GCM ou AES-256-CBC.
- Confidentialité persistante.
- Des audits de sécurité publiés par une société tierce réputée.
- Les serveurs VPN qui utilisent le chiffrement du disque complet ou qui sont uniquement en mémoire vive.

**Dans le meilleur des cas :**

- Chiffrement le plus fort : RSA-4096.
- Cryptographie post-quantique optionnelle
- Des audits de sécurité complets publiés par une société tierce réputée.
- Des programmes de primes aux bugs et/ou un processus coordonné de divulgation des vulnérabilités.
- Serveurs VPN à mémoire vive uniquement.

### Confiance

Vous ne confieriez pas vos finances à une personne ayant une fausse identité, alors pourquoi lui confier vos données internet ? Nous exigeons de nos fournisseurs recommandés qu'ils rendent public leur propriété ou leur direction. Nous aimerions également voir des rapports de transparence fréquents, notamment en ce qui concerne la manière dont les demandes de gouvernement sont traitées.

**Minimum pour se qualifier :**

- Une direction ou un propriétaire public.
- Entreprise basée dans une juridiction où elle ne peut être contrainte à une journalisation secrète.

**Dans le meilleur des cas :**

- Une direction publique.
- Rapports de transparence fréquents.

### Marketing

Avec les fournisseurs de VPN que nous recommandons, nous aimons voir un marketing responsable.

**Minimum pour se qualifier :**

- Doit héberger soi-même ses systèmes de télémétrie (ex : pas d'utilisation de Google Analytics).

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

Bien qu'il ne s'agisse pas d'exigences strictes, nous avons tenu compte de certains facteurs pour déterminer les fournisseurs à recommander. Ces facteurs comprennent la fonctionnalité de blocage de contenu, les alertes de contrainte légale, une excellente assistance à la clientèle, le nombre de connexions simultanées autorisées, etc.
