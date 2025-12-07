---
meta_title: "Recomendações e comparações de serviços de privacidade VPN, sem patrocinadores ou anúncios - Privacy Guides"
title: Serviços VPN
icon: material/vpn
description: The best VPN services for protecting your privacy and security online. Find a provider here that isn't out to spy on you.
cover: vpn.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>Protects against the following threat(s):</small>

- [:material-account-cash: Capitalismo de vigilância](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

If you're looking for additional *privacy* from your ISP, on a public Wi-Fi network, or while torrenting files, a **VPN** may be the solution for you.

<div class="admonition danger" markdown>
<p class="admonition-title">VPNs do not provide anonymity</p>

Using a VPN will **not** keep your browsing habits anonymous, nor will it add additional security to non-secure (HTTP) traffic.

If you are looking for **anonymity**, you should use the Tor Browser. If you're looking for added **security**, you should always ensure you're connecting to websites using HTTPS. Uma VPN não substitui as boas práticas de segurança.

[Introduction to the Tor Browser](tor.md#tor-browser){ .md-button .md-button--primary } [Tor Myths & FAQ](advanced/tor-overview.md){ .md-button }

</div>

[Visão detalhada da VPN :material-arrow-right-drop-circle:](basics/vpn-overview.md ""){.md-button}

## Fornecedores recomendados

Our recommended providers use encryption, support WireGuard & OpenVPN, and have a no logging policy. Para mais informações, consulte a lista completa de critérios [](#criteria).

| Provider              | Countries | WireGuard                     | Port Forwarding                                        | IPv6                                                       | Anonymous Payments           |
| --------------------- | --------- | ----------------------------- | ------------------------------------------------------ | ---------------------------------------------------------- | ---------------------------- |
| [Proton](#proton-vpn) | 127+      | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange } Partial Support | :material-information-outline:{ .pg-blue } Limited Support | Cash  Monero via third party |
| [IVPN](#ivpn)         | 41+       | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                 | :material-information-outline:{ .pg-blue } Outgoing Only   | Monero  Cash                 |
| [Mullvad](#mullvad)   | 49+       | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                 | :material-check:{ .pg-green }                              | Monero  Cash                 |

### Proton VPN

<div class="admonition recommendation" markdown>

![Logótipo Proton VPN](assets/img/vpn/protonvpn.svg){ align=right }

O **Proton VPN** é um forte concorrente no espaço VPN, e está em funcionamento desde 2016. A Proton AG está sediada na Suíça e oferece uma opção gratuita com limitações, bem como uma opção premium com mais funcionalidades.

[:octicons-home-16: Homepage](https://protonvpn.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://protonvpn.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://protonvpn.com/support){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/ProtonVPN){ .card-link title="Source Code" }

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

#### :material-check:{ .pg-green } 127 Countries

Proton VPN has [servers in 127 countries](https://protonvpn.com/vpn-servers)(1) or [10](https://protonvpn.com/support/how-to-create-free-vpn-account) if you use their [free plan](https://protonvpn.com/blog/product-roadmap-winter-2025-2026).(2) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Isto deve-se ao facto do percurso até ao destino ser mais curto (menos saltos).
{ .annotate }

1. Of which at least 71 are virtual servers, meaning your IP will appear from the country but the server is in another. 12 more locations have both hardware and virtual servers. [Source](https://protonvpn.com/support/how-smart-routing-works)
2. Last checked: 2025-10-28

Também achamos que é melhor para a segurança das chaves privadas do fornecedor de VPN a utilização de servidores dedicados [](https://en.wikipedia.org/wiki/Dedicated_hosting_service), em vez de soluções partilhadas mais baratas (com outros clientes), como os servidores privados virtuais [](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Auditado de forma independente

Independent security researcher Ruben Santamarta conducted audits for Proton VPN's [browser extensions](https://drive.proton.me/urls/RWDD2SHT98#v7ZrwNcafkG8) and [apps](https://drive.proton.me/urls/RVW8TXG484#uTXX5Fc9GADo) in September 2024 and January 2025, respectively. Proton VPN's infrastrcture has undergone [annual audits](https://protonvpn.com/blog/no-logs-audit) by Securitum since 2022.

Previously, Proton VPN underwent an independent audit by SEC Consult in January 2020. A SEC Consult encontrou algumas vulnerabilidades de risco médio e baixo nas aplicações Windows, Android e iOS do Proton VPN, todas elas "devidamente corrigidas" pelo Proton VPN antes da publicação dos relatórios. Nenhum dos problemas identificados permitia a um atacante aceder remotamente ao seu dispositivo ou tráfego. You can view individual reports for each platform in their dedicated [blog post](https://web.archive.org/web/20250307041036/https://protonvpn.com/blog/open-source) on the audit.

#### :material-check:{ .pg-green } Clientes de código aberto

Proton VPN provides the source code for their desktop and mobile clients in their [GitHub organization](https://github.com/ProtonVPN).

#### :material-check:{ .pg-green } Aceita dinheiro

Proton VPN, in addition to accepting credit/debit cards, PayPal, and [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), also accepts **cash/local currency** as an anonymous form of payment. You can also use [**Monero**](cryptocurrency.md#monero) to purchase vouchers for Proton VPN Plus and Proton Unlimited via their [official](https://discuss.privacyguides.net/t/add-monero-as-an-anonymous-payment-method-for-proton-services/31058/15) reseller [ProxyStore](https://dys2p.com/en/2025-09-09-proton.html).

#### :material-check:{ .pg-green } Suporte WireGuard

Proton VPN supports the WireGuard® protocol. [WireGuard](https://wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://wireguard.com/protocol). Além disso, o WireGuard aposta na simplicidade e no desempenho.

Proton VPN [recommends](https://protonvpn.com/blog/wireguard) the use of WireGuard with their service. Proton VPN also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://wireguard.com/install).

#### :material-alert-outline:{ .pg-orange } Limited IPv6 Support

Proton [now supports IPv6](https://protonvpn.com/support/prevent-ipv6-vpn-leaks) in their browser extension and Linux client, but only 80% of their servers are IPv6-compatible. On other platforms, the Proton VPN client will block all outgoing IPv6 traffic, so you don't have to worry about your IPv6 address being leaked, but you will not be able to connect to any IPv6-only sites, nor will you be able to connect to Proton VPN from an IPv6-only network.

#### :material-information-outline:{ .pg-info } Remote Port Forwarding

Proton VPN currently only supports ephemeral remote [port forwarding](https://protonvpn.com/support/port-forwarding) via NAT-PMP, with 60 second lease times. The official Windows and Linux apps provide an easy-to-access option for it, while on other operating systems you'll need to run your own [NAT-PMP client](https://protonvpn.com/support/port-forwarding-manual-setup). As aplicações torrent suportam frequentemente NAT-PMP de forma nativa.

#### :material-information-outline:{ .pg-blue } Anti-Censorship

Proton VPN has their [Stealth](https://protonvpn.com/blog/stealth-vpn-protocol) protocol which *may* help in situations where VPN protocols like OpenVPN or WireGuard are blocked with various rudimentary techniques. Stealth encapsulates the VPN tunnel in TLS session in order to look like more generic internet traffic.

Unfortunately, it does not work very well in countries where sophisticated filters that analyze all outgoing traffic in an attempt to discover encrypted tunnels are deployed. Stealth is available on Android, iOS, Windows, and macOS, but it's not yet available on Linux.

#### :material-check:{ .pg-green } Clientes para dispositivos móveis

Proton VPN has published [App Store](https://apps.apple.com/app/id1437005085) and [Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android) clients, both supporting an easy-to-use interface as opposed to requiring you to manually configure your WireGuard connection. The Android client is also available on [GitHub](https://github.com/ProtonVPN/android-app/releases).

<div class="admonition warning" markdown>
<p class="admonition-title">How to opt out of sharing telemetry</p>

On Android, Proton hides telemetry settings under the misleadingly labeled "**Help us fight censorship**" menu in the settings panel. On other platforms these settings can be found under the "**Usage statistics**" menu.

We are noting this because while we don't necessarily recommend against sharing anonymous usage statistics with developers, it is important that these settings are easily found and clearly labeled.

</div>

#### :material-information-outline:{ .pg-blue } Additional Notes

Proton VPN clients support two-factor authentication on all platforms. O Proton VPN tem os seus próprios servidores e centros de dados na Suíça, Islândia e Suécia. They offer content blocking and known-malware blocking with their DNS service. Additionally, Proton VPN also offers "Tor" servers allowing you to easily connect to onion sites, but we still strongly recommend using [the official Tor Browser](tor.md#tor-browser) for this purpose.

##### :material-alert-outline:{ .pg-orange } Kill switch feature is broken on Intel-based Macs

System crashes [may occur](https://protonvpn.com/support/macos-t2-chip-kill-switch) on Intel-based Macs when using the VPN kill switch. Se precisar desta funcionalidade e estiver a utilizar um Mac com chipset Intel, deve considerar a utilização de outro serviço VPN.

### IVPN

<div class="admonition recommendation" markdown>

![Logótipo IVPN](assets/img/vpn/ivpn.svg){ align=right }

O **IVPN** é outro fornecedor de VPN premium, e está em funcionamento desde 2009. IVPN is based in Gibraltar and does not offer a free trial.

[:octicons-home-16: Homepage](https://ivpn.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ivpn.net/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://ivpn.net/knowledgebase/general){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/ivpn){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1193122683)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/net.ivpn.client)
- [:simple-github: GitHub](https://github.com/ivpn/android-app/releases)
- [:fontawesome-brands-windows: Windows](https://ivpn.net/apps-windows)
- [:simple-apple: macOS](https://ivpn.net/apps-macos)
- [:simple-linux: Linux](https://ivpn.net/apps-linux)

</details>

</div>

#### :material-check:{ .pg-green } 41 Countries

IVPN has [servers in 41 countries](https://ivpn.net/status).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Isto deve-se ao facto do percurso até ao destino ser mais curto (menos saltos).
{ .annotate }

1. Last checked: 2025-10-28

Também achamos que é melhor para a segurança das chaves privadas do fornecedor de VPN a utilização de servidores dedicados [](https://en.wikipedia.org/wiki/Dedicated_hosting_service), em vez de soluções partilhadas mais baratas (com outros clientes), como os servidores privados virtuais [](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Auditado de forma independente

IVPN has had multiple [independent audits](https://ivpn.net/en/blog/tags/audit) since 2019 and has publicly announced their commitment to [annual security audits](https://ivpn.net/blog/ivpn-apps-security-audit-concluded).

#### :material-check:{ .pg-green } Clientes de código aberto

As of February 2020 [IVPN applications are now open source](https://ivpn.net/blog/ivpn-applications-are-now-open-source). O código-fonte pode ser obtido na sua página do [GitHub](https://github.com/ivpn).

#### :material-check:{ .pg-green } Aceita dinheiro e Monero

In addition to accepting credit/debit cards and PayPal, IVPN accepts Bitcoin, **Monero** and **cash/local currency** (on annual plans) as anonymous forms of payment. You can also purchase [prepaid cards](https://ivpn.net/knowledgebase/billing/voucher-cards-faq) with redeem codes.

#### :material-check:{ .pg-green } Suporte WireGuard

O IVPN suporta o protocolo WireGuard®. [WireGuard](https://wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://wireguard.com/protocol). Além disso, o WireGuard aposta na simplicidade e no desempenho.

IVPN [recommends](https://ivpn.net/wireguard) the use of WireGuard with their service and, as such, the protocol is the default on all of IVPN's apps. IVPN also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://wireguard.com/install).

#### :material-information-outline:{ .pg-blue } IPv6 Support

IVPN allows you to [connect to services using IPv6](https://ivpn.net/knowledgebase/general/do-you-support-ipv6) but doesn't allow you to connect from a device using an IPv6 address.

#### :material-alert-outline:{ .pg-orange } Encaminhamento de porta remota

IVPN previously supported port forwarding, but removed the option in [June 2023](https://ivpn.net/blog/gradual-removal-of-port-forwarding). A falta desta funcionalidade pode ter um impacto negativo em certas aplicações, especialmente nas aplicações ponto-a-ponto, como os clientes de torrent.

#### :material-check:{ .pg-green } Anti-Censorship

IVPN has obfuscation modes using [V2Ray](https://v2ray.com/en/index) which helps in situations where VPN protocols like OpenVPN or WireGuard are blocked. It has two modes where it can use [VMess](https://guide.v2fly.org/en_US/basics/vmess) over QUIC or TCP connections. QUIC is a modern protocol with better congestion control and therefore may be faster with reduced latency. The TCP mode makes your data appear as regular HTTP traffic.

#### :material-check:{ .pg-green } Clientes para dispositivos móveis

IVPN has published [App Store](https://apps.apple.com/app/id1193122683) and [Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client) clients, both supporting an easy-to-use interface as opposed to requiring you to manually configure your WireGuard connection. The Android client is also available on [GitHub](https://github.com/ivpn/android-app/releases).

#### :material-information-outline:{ .pg-blue } Additional Notes

IVPN clients support two-factor authentication. IVPN also provides "[AntiTracker](https://ivpn.net/antitracker)" functionality, which blocks advertising networks and trackers from the network level.

### IVPN

<div class="admonition recommendation" markdown>

![Logótipo Mullvad](assets/img/vpn/mullvad.svg){ align=right }

O **Mullvad** é uma VPN rápida e económica, com grande foco na transparência e segurança. They have been in operation since 2009. Mullvad is based in Sweden and offers a 14-day money-back guarantee for [payment methods](https://mullvad.net/en/help/refunds) that allow it.

[:octicons-home-16: Homepage](https://mullvad.net){ .md-button .md-button--primary }
[:simple-torbrowser:](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://mullvad.net/en/help){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/mullvad){ .card-link title="Source Code" }

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

Mullvad has [servers in 49 countries](https://mullvad.net/servers).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Isto deve-se ao facto do percurso até ao destino ser mais curto (menos saltos).
{ .annotate }

1. Last checked: 2025-10-28

Também achamos que é melhor para a segurança das chaves privadas do fornecedor de VPN a utilização de servidores dedicados [](https://en.wikipedia.org/wiki/Dedicated_hosting_service), em vez de soluções partilhadas mais baratas (com outros clientes), como os servidores privados virtuais [](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Auditado de forma independente

Mullvad has had multiple [independent audits](https://mullvad.net/en/blog/tag/audits) and has publicly announced their endeavors to conduct [annual audits](https://mullvad.net/en/blog/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit) of their apps and infrastructure.

#### :material-check:{ .pg-green } Clientes de código aberto

O Mullvad fornece o código-fonte dos seus clientes desktop e para dispositivos móveis na sua página do [GitHub](https://github.com/mullvad/mullvadvpn-app).

#### :material-check:{ .pg-green } Aceita dinheiro e Monero

Mullvad, in addition to accepting credit/debit cards and PayPal, accepts Bitcoin, Bitcoin Cash, **Monero** and **cash/local currency** as anonymous forms of payment. You can also purchase [prepaid cards](https://mullvad.net/en/help/partnerships-and-resellers) with redeem codes. Mullvad also accepts Swish and bank wire transfers, as well as a few European payment systems.

#### :material-check:{ .pg-green } Suporte WireGuard

O Mullvad suporta o protocolo WireGuard®. [WireGuard](https://wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://wireguard.com/protocol). Além disso, o WireGuard aposta na simplicidade e no desempenho.

Mullvad [recommends](https://mullvad.net/en/help/why-wireguard) the use of WireGuard with their service. It is the only protocol supported on their mobile apps, and their desktop apps will [lose OpenVPN support](https://mullvad.net/en/blog/reminder-that-openvpn-is-being-removed) in 2025. Additionally, their servers will stop accepting OpenVPN connections by January 15, 2026. Mullvad also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://wireguard.com/install).

#### :material-check:{ .pg-green } Suporte IPv6

Mullvad allows you to [access services hosted on IPv6](https://mullvad.net/en/blog/2014/9/15/ipv6-support) and connect from a device using an IPv6 address.

#### :material-alert-outline:{ .pg-orange } Encaminhamento de porta remota

Mullvad previously supported port forwarding, but removed the option in [May 2023](https://mullvad.net/en/blog/2023/5/29/removing-the-support-for-forwarded-ports). A falta desta funcionalidade pode ter um impacto negativo em certas aplicações, especialmente nas aplicações ponto-a-ponto, como os clientes de torrent.

#### :material-check:{ .pg-green } Anti-Censorship

Mullvad offers several features to help bypass censorship and access the internet freely:

- **Obfuscation modes**: Mullvad has two built-in obfuscation modes: "UDP-over-TCP" and ["WireGuard over Shadowsocks"](https://mullvad.net/en/blog/introducing-shadowsocks-obfuscation-for-wireguard). These modes disguise your VPN traffic as regular web traffic, making it harder for censors to detect and block. Supposedly, China has to use a [new method to disrupt Shadowsocks-routed traffic](https://gfw.report/publications/usenixsecurity23/en).
- **Advanced obfuscation with Shadowsocks and v2ray**: For more advanced users, Mullvad provides a guide on how to use the [Shadowsocks with v2ray](https://mullvad.net/en/help/shadowsocks-with-v2ray) plugin with Mullvad clients. This setup provides an additional layer of obfuscation and encryption.
- **Custom server IPs**: To counter IP-blocking, you can request custom server IPs from Mullvad's support team. Once you receive the custom IPs, you can input the text file in the "Server IP override" settings, which will override the chosen server IP addresses with ones that aren't known to the censor.
- **Bridges and proxies**: Mullvad also allows you to use bridges or proxies to reach their API (needed for authentication), which can help bypass censorship attempts that block access to the API itself.

#### :material-check:{ .pg-green } Clientes para dispositivos móveis

Mullvad has published [App Store](https://apps.apple.com/app/id1488466513) and [Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn) clients, both supporting an easy-to-use interface as opposed to requiring you to manually configure your WireGuard connection. O cliente Android também está disponível na página do [GitHub](https://github.com/mullvad/mullvadvpn-app/releases).

#### :material-information-outline:{ .pg-blue } Additional Notes

Mullvad is very transparent about which nodes they [own or rent](https://mullvad.net/en/servers). They also provide the option to enable Defense Against AI-guided Traffic Analysis ([DAITA](https://mullvad.net/en/blog/daita-defense-against-ai-guided-traffic-analysis)) in their apps. DAITA protects against the threat of advanced traffic analysis which can be used to connect patterns in VPN traffic with specific websites.

## Critérios

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

É importante notar que a utilização de um fornecedor de VPN não o tornará anónimo, mas dar-lhe-á mais privacidade em determinadas situações. Uma VPN não é uma ferramenta para atividades ilegais. Não confie numa política de "não registo".

</div>

**Tenha em atenção que não somos afiliados de nenhum dos fornecedores que recomendamos. Esta facto permite-nos fornecer recomendações completamente objetivas.** Para além dos [nossos critérios padrão](about/criteria.md), desenvolvemos um conjunto claro de requisitos para qualquer fornecedor de VPN que pretenda ser recomendado, incluindo encriptação forte, auditorias de segurança independentes, tecnologia moderna e muito mais. Sugerimos que se familiarize com esta lista, antes de escolher um fornecedor de VPN, e que faça a sua própria pesquisa para garantir uma escolha de fornecedor de VPN o mais fiável possível.

### Tecnologia

We require all our recommended VPN providers to provide standard configuration files which can be used in a generic, open-source client. **If** a VPN provides their own custom client, we require a kill switch to block network data leaks when disconnected.

**Mínimos de qualificação:**

- Support for strong protocols such as WireGuard.
- Kill switch built in to clients.
- Multi-hop support. Multi-hopping is important to keep data private in case of a single node compromise.
- If VPN clients are provided, they should be [open source](https://en.wikipedia.org/wiki/Open_source), like the VPN software they generally have built into them. We believe that [source code](https://en.wikipedia.org/wiki/Source_code) availability provides greater transparency about what the program is actually doing.
- Censorship resistance features designed to bypass firewalls without DPI.

**Melhor caso:**

- Kill switch with highly configurable options (enable/disable on certain networks, on boot, etc.)
- Clientes VPN fáceis de utilizar
- [IPv6](https://en.wikipedia.org/wiki/IPv6) support. É suposto que os servidores permitam ligações de entrada através do IPv6 e que lhe permitam aceder a serviços alojados em endereços IPv6.
- A capacidade de [reencaminhamento de portas remotas](https://en.wikipedia.org/wiki/Port_forwarding#Remote_port_forwarding) ajuda a criar ligações quando se utiliza software de partilha de ficheiros P2P ([Peer-to-Peer](https://en.wikipedia.org/wiki/Peer-to-peer)) ou se aloja um servidor (por exemplo, Mumble).
- Obfuscation technology which camouflages the true nature of internet traffic, designed to circumvent advanced internet censorship methods like DPI.

### Privacidade

Preferimos que os nossos fornecedores recomendados recolham o mínimo de dados possível. Não devem ser recolhidas informações pessoais aquando do registo e devem ser aceites formas de pagamento anónimas.

**Mínimos de qualificação:**

- [Criptomoeda anónima](cryptocurrency.md) **ou ** opção de pagamento em dinheiro.
- Não devem ser necessárias informações pessoais para o registo: no limite, apenas o nome de utilizador, a palavra-passe e o e-mail.

**Melhor caso:**

- Deve aceitar várias opções de pagamento anónimo [](advanced/payments.md).
- No personal information accepted (auto-generated username, no email required, etc.).

### Segurança

Uma VPN é inútil se não proporcionar uma segurança adequada. We require all our recommended providers to abide by current security standards. O ideal será a utilização, por defeito, de esquemas de encriptação mais resistentes ao futuro. Também exigimos que um terceiro independente audite a segurança do fornecedor, idealmente de uma forma muito abrangente e numa base regular (anual).

**Mínimos de qualificação:**

- Esquemas de encriptação fortes: OpenVPN com autenticação SHA-256; handshake RSA-2048 ou superior; encriptação de dados AES-256-GCM ou AES-256-CBC.
- Forward Secrecy.
- Auditorias de segurança publicadas por uma empresa terceira de renome.
- VPN servers that use full-disk encryption or are RAM-only.

**Melhor caso:**

- Encriptação máxima: RSA-4096.
- Optional quantum-resistant encryption.
- Auditorias de segurança exaustivas publicadas por uma empresa terceira de renome.
- Programas de recompensa por deteção de erros e/ou processos coordenados de divulgação de vulnerabilidades.
- RAM-only VPN servers.

### Confiança

Se não confiaria as suas finanças a alguém com uma identidade falsa, porque motivo lhe confiaria os seus dados de Internet? Exigimos que os nossos fornecedores recomendados sejam transparentes em relação à sua propriedade ou liderança. Gostaríamos também de ver relatórios de transparência frequentes, especialmente no que diz respeito à forma como os pedidos do governo são tratados.

**Mínimos de qualificação:**

- Liderança ou propriedade virada para o público.
- Company based in a jurisdiction where it cannot be forced to do secret logging.

**Melhor caso:**

- Liderança virada para o público.
- Perfect Forward Secrecy (PFS).

### Marketing

Os fornecedores de VPN que recomendamos devem ter uma política de marketing responsável.

**Mínimos de qualificação:**

- Must self-host analytics (i.e., no Google Analytics).

Não deve implementar políticas de marketing irresponsáveis:

- Garantir a proteção do anonimato a 100%. Afirmar que algo é 100%, significa que não pode haver falhas. Sabemos que as pessoas podem desanonimizar-se muito facilmente de várias formas, por exemplo.:
    - Reutilizar informações pessoais (por exemplo, contas de e-mail, pseudónimos únicos, etc.) a que acederam sem software de anonimato (Tor, VPN, etc.)
    - [Impressão digital do browser](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)
- Afirmar que um circuito único de VPN é "mais anónimo" do que o Tor, que é um circuito de três ou mais saltos, que muda regularmente.
- Utilizar linguagem responsável: por exemplo, não há problema em dizer que uma VPN está "desligada" ou "não ligada", mas afirmar que alguém está "exposto", "vulnerável" ou "comprometido" é utilização desnecessária de uma linguagem alarmante, que pode ser incorreta. Por exemplo, essa pessoa pode simplesmente estar a utilizar o serviço de outro fornecedor de VPN ou a utilizar o Tor.

**Melhor caso:**

O marketing responsável, que é simultaneamente educativo e útil para o consumidor, pode incluir:

- Uma comparação de tecnologias precisa que permita dizer que a utilização do [Tor](tor.md) é preferível.
- Disponibilização de uma versão do site no serviço [.onion](https://en.wikipedia.org/wiki/.onion)

### Funcionalidade adicional

Embora não sejam requisitos obrigatórios, existem alguns fatores que valorizamos, quando determinamos quais os fornecedores a recomendar. These include content blocking functionality, warrant canaries, excellent customer support, the number of allowed simultaneous connections, etc.
