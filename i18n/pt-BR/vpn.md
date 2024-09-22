---
meta_title: "Recomendações e Comparação de Serviços VPN Privados, Sem Patrocinadores ou Anúncios — Privacy Guides"
title: "Serviços de VPN"
icon: material/vpn
description: The best VPN services for protecting your privacy and security online. Encontre aqui um provedor que não tem como objetivo espionar você.
cover: vpn.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>Protects against the following threat(s):</small>

- [:material-account-cash: Surveillance Capitalism](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

If you're looking for additional *privacy* from your ISP, on a public Wi-Fi network, or while torrenting files, a **VPN** may be the solution for you.

<div class="admonition danger" markdown>
<p class="admonition-title">VPNs do not provide anonymity</p>

Using a VPN will **not** keep your browsing habits anonymous, nor will it add additional security to non-secure (HTTP) traffic.

If you are looking for **anonymity**, you should use the Tor Browser. If you're looking for added **security**, you should always ensure you're connecting to websites using HTTPS. Uma VPN não substitui boas práticas de segurança.

[Download Tor](https://torproject.org){ .md-button .md-button--primary } [Tor Myths & FAQ](advanced/tor-overview.md){ .md-button }

</div>

[Detalhes sobre VPNs :material-arrow-right-drop-circle:](basics/vpn-overview.md ""){.md-button}

## Provedores Recomendados

Our recommended providers use encryption, support WireGuard & OpenVPN, and have a no logging policy. Leia nossa [lista completa de requisitos](#criteria) para mais informações.

| Provider              | Countries | WireGuard                     | Port Forwarding                                            | IPv6                                                     | Anonymous Payments |
| --------------------- | --------- | ----------------------------- | ---------------------------------------------------------- | -------------------------------------------------------- | ------------------ |
| [Proton](#proton-vpn) | 112+      | :material-check:{ .pg-green } | :material-information-outline:{ .pg-blue } Partial Support | :material-alert-outline:{ .pg-orange }                   | Dinheiro           |
| [IVPN](#ivpn)         | 37+       | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                     | :material-information-outline:{ .pg-blue } Outgoing Only | Monero, Cash       |
| [Mullvad](#mullvad)   | 45+       | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }                     | :material-check:{ .pg-green }                            | Monero, Cash       |

### Proton VPN

<div class="admonition recommendation" markdown>

![Logomarca ProtonVPN](assets/img/vpn/protonvpn.svg){ align=right }

**Proton VPN** é um forte concorrente no espaço VPN, e estão em funcionamento desde 2016. Proton AG está sediada na Suíça e oferece um plano gratuito limitado, bem como uma opção paga com mais recursos.

[:octicons-home-16: Homepage](https://protonvpn.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://protonvpn.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://protonvpn.com/support){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ProtonVPN){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1437005085)
- [:simple-github: GitHub](https://github.com/ProtonVPN/android-app/releases)
- [:fontawesome-brands-windows: Windows](https://protonvpn.com/download-windows)
- [:simple-linux: Linux](https://protonvpn.com/support/linux-vpn-setup)

</details>

</div>

#### :material-check:{ .pg-green } 112 Countries

Proton VPN has [servers in 112 countries](https://protonvpn.com/vpn-servers) or [5](https://protonvpn.com/support/how-to-create-free-vpn-account) if you use their [free plan](https://protonvpn.com/free-vpn/server).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Isto deve-se a um caminho mais curto (menos pulos) até ao destino.
{ .annotate }

1. Last checked: 2024-08-06

Nós também consideramos que é melhor para a segurança das chaves privadas do provedor VPN se eles usarem [servidores dedicados](https://en.wikipedia.org/wiki/Dedicated_hosting_service), em vez de soluções compartilhadas mais baratas (com outros clientes) como [servidores virtuais privados](https://pt.wikipedia.org/wiki/Servidor_virtual_privado).

#### :material-check:{ .pg-green } Revisado por auditoria independente

Em Janeiro de 2020, ProtonVPN foi submetida a uma auditoria independente pela SEC Consult. A SEC Consult encontrou algumas vulnerabilidades de médio e baixo risco nos aplicativos Windows, Android e iOS da Proton VPN, todos os quais foram "devidamente corrigidos" pela Proton VPN antes que os relatórios fossem publicados. Nenhum dos problemas identificados teria proporcionado acesso remoto ao seu dispositivo ou tráfego. You can view individual reports for each platform at [protonvpn.com](https://protonvpn.com/blog/open-source). In April 2022 Proton VPN underwent [another audit](https://protonvpn.com/blog/no-logs-audit). Um [certificado de segurança](https://proton.me/blog/security-audit-all-proton-apps) foi concedido para os aplicativos do Proton Mail em 9 de Novembro de 2021 pela [Securitium](https://research.securitum.com).

#### :material-check:{ .pg-green } Clientes de Código Aberto (Open-Source)

Proton VPN fornece o código-fonte de seus clientes móveis e de desktop em sua [organização GitHub](https://github.com/ProtonVPN).

#### :material-check:{ .pg-green } Aceita Dinheiro

Proton VPN, além de aceitar cartões de crédito/débito, PayPal e [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), também aceita **dinheiro/moeda local** como forma anônima de pagamento.

#### :material-check:{ .pg-green } Suporta WireGuard

Proton VPN suporta principalmente o protocolo WireGuard®. [WireGuard](https://wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://wireguard.com/protocol). Além disso, WireGuard pretende ser mais simples e mais eficiente.

Proton VPN [recommends](https://protonvpn.com/blog/wireguard) the use of WireGuard with their service. On Proton VPN's Windows, macOS, iOS, Android, ChromeOS, and Android TV apps, WireGuard is the default protocol; however, [support](https://protonvpn.com/support/how-to-change-vpn-protocols) for the protocol is not present in their Linux app.

#### :material-alert-outline:{ .pg-orange } No IPv6 Support

Proton VPN's servers are only compatible with IPv4. The Proton VPN applications will block all outgoing IPv6 traffic, so you don't have to worry about your IPv6 address being leaked, but you will not be able to connect to any IPv6-only sites, and you will not be able to connect to Proton VPN from an IPv6-only network.

#### :material-information-outline:{ .pg-info } Remote Port Forwarding

Proton VPN currently only supports ephemeral remote [port forwarding](https://protonvpn.com/support/port-forwarding) via NAT-PMP, with 60 second lease times. The Windows app provides an easy to access option for it, while on other operating systems you'll need to run your own [NAT-PMP client](https://protonvpn.com/support/port-forwarding-manual-setup). Torrent applications often support NAT-PMP natively.

#### :material-information-outline:{ .pg-blue } Anti-Censorship

Proton VPN has their [Stealth](https://protonvpn.com/blog/stealth-vpn-protocol) protocol which *may* help in situations where VPN protocols like OpenVPN or Wireguard are blocked with various rudimentary techniques. Stealth encapsulates the VPN tunnel in TLS session in order to look like more generic internet traffic.

Unfortunately, it does not work very well in countries where sophisticated filters that analyze all outgoing traffic in an attempt to discover encrypted tunnels are deployed. Stealth is available on Android, iOS, Windows, and macOS, but it's not yet available on Linux.

#### :material-check:{ .pg-green } Clientes Móveis

In addition to providing standard OpenVPN configuration files, Proton VPN has mobile clients for [App Store](https://apps.apple.com/app/id1437005085), [Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android), and [GitHub](https://github.com/ProtonVPN/android-app/releases) allowing for easy connections to their servers.

#### :material-information-outline:{ .pg-blue } Additional Notes

Proton VPN clients support two factor authentication on all platforms. Proton VPN tem seus próprios servidores e centros de dados na Suíça, Islândia e Suécia. They offer content blocking and known-malware blocking with their DNS service. Additionally, Proton VPN also offers "Tor" servers allowing you to easily connect to onion sites, but we still strongly recommend using [the official Tor Browser](tor.md#tor-browser) for this purpose.

##### :material-alert-outline:{ .pg-orange } O recurso Killswitch não funciona em Macs baseados em Intel

System crashes [may occur](https://protonvpn.com/support/macos-t2-chip-kill-switch) on Intel-based Macs when using the VPN killswitch. Se você precisar desse recurso e estiver usando um Mac com chipset Intel, considere usar outro serviço de VPN.

### IVPN

<div class="admonition recommendation" markdown>

![IVPN logo](assets/img/vpn/ivpn.svg){ align=right }

**IVPN** is another premium VPN provider, and they have been in operation since 2009. IVPN is based in Gibraltar and does not offer a free trial.

[:octicons-home-16: Homepage](https://ivpn.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ivpn.net/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://ivpn.net/knowledgebase/general){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ivpn){ .card-link title="Source Code" }

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

#### :material-check:{ .pg-green } 37 Countries

IVPN has [servers in 37 countries](https://ivpn.net/status).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Isto deve-se a um caminho mais curto (menos pulos) até ao destino.
{ .annotate }

1. Last checked: 2024-08-06

Nós também consideramos que é melhor para a segurança das chaves privadas do provedor VPN se eles usarem [servidores dedicados](https://en.wikipedia.org/wiki/Dedicated_hosting_service), em vez de soluções compartilhadas mais baratas (com outros clientes) como [servidores virtuais privados](https://pt.wikipedia.org/wiki/Servidor_virtual_privado).

#### :material-check:{ .pg-green } Revisado por auditoria independente

IVPN foi submetido a uma [auditoria de ausência de registro de dados (no-logging) pela Cure53](https://cure53.de/audit-report_ivpn.pdf), cuja conclusão confirmou a reivindicação de que o IVPN não registra dados. IVPN também elaborou um [relatório completo de Teste de Penetração (pentest) pela Cure53](https://cure53.de/summary-report_ivpn_2019.pdf) em janeiro de 2020. IVPN has also said they plan to have [annual reports](https://ivpn.net/blog/independent-security-audit-concluded) in the future. A further review was conducted [in April 2022](https://ivpn.net/blog/ivpn-apps-security-audit-2022-concluded) and was produced by Cure53 [on their website](https://cure53.de/pentest-report_IVPN_2022.pdf).

#### :material-check:{ .pg-green } Clientes de Código Aberto (Open-Source)

As of February 2020 [IVPN applications are now open source](https://ivpn.net/blog/ivpn-applications-are-now-open-source). O código-fonte pode ser obtido da sua [organização (GitHub)](https://github.com/ivpn).

#### :material-check:{ .pg-green } Aceita Dinheiro e Monero

In addition to accepting credit/debit cards and PayPal, IVPN accepts Bitcoin, **Monero** and **cash/local currency** (on annual plans) as anonymous forms of payment. Prepaid cards with redeem codes are [also available](https://ivpn.net/knowledgebase/billing/voucher-cards-faq).

#### :material-check:{ .pg-green } Suporta WireGuard

IVPN suporta o protocolo WireGuard®️. [WireGuard](https://wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://wireguard.com/protocol). Além disso, WireGuard pretende ser mais simples e mais eficiente.

IVPN [recommends](https://ivpn.net/wireguard) the use of WireGuard with their service and, as such, the protocol is the default on all of IVPN's apps. IVPN also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://wireguard.com/install).

#### :material-information-outline:{ .pg-blue } IPv6 Support

IVPN allows you to [connect to services using IPv6](https://ivpn.net/knowledgebase/general/do-you-support-ipv6) but doesn't allow you to connect from a device using an IPv6 address.

#### :material-alert-outline:{ .pg-orange } Encaminhamento de Porta Remoto

IVPN previously supported port forwarding, but removed the option in [June 2023](https://ivpn.net/blog/gradual-removal-of-port-forwarding). Missing this feature could negatively impact certain applications, especially peer-to-peer applications like torrent clients.

#### :material-check:{ .pg-green } Anti-Censorship

IVPN has obfuscation modes using the [v2ray](https://v2ray.com/en/index.html) project which helps in situations where VPN protocols like OpenVPN or Wireguard are blocked. Currently this feature is only available on Desktop and [iOS](https://ivpn.net/knowledgebase/ios/v2ray). It has two modes where it can use [VMess](https://guide.v2fly.org/en_US/basics/vmess.html) over QUIC or TCP connections. QUIC is a modern protocol with better congestion control and therefore may be faster with reduced latency. The TCP mode makes your data appear as regular HTTP traffic.

#### :material-check:{ .pg-green } Clientes Móveis

In addition to providing standard OpenVPN configuration files, IVPN has mobile clients for [App Store](https://apps.apple.com/app/id1193122683), [Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client), and [GitHub](https://github.com/ivpn/android-app/releases) allowing for easy connections to their servers.

#### :material-information-outline:{ .pg-blue } Additional Notes

IVPN clients support two factor authentication. IVPN also provides "[AntiTracker](https://ivpn.net/antitracker)" functionality, which blocks advertising networks and trackers from the network level.

### Mullvad

<div class="admonition recommendation" markdown>

![Mullvad logo](assets/img/vpn/mullvad.svg){ align=right }

**Mullvad** é uma VPN rápida e barata com uma séria ênfase em transparência e segurança. They have been in operation since 2009. Mullvad is based in Sweden and does not offer a free trial.

[:octicons-home-16: Homepage](https://mullvad.net){ .md-button .md-button--primary }
[:simple-torbrowser:](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://mullvad.net/en/help){ .card-link title=Documentation}
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

#### :material-check:{ .pg-green } 45 Countries

Mullvad has [servers in 45 countries](https://mullvad.net/servers).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Isso se deve a uma rota mais curta (menos saltos) até o destino.
{ .annotate }

1. Last checked: 2024-08-06

Nós também consideramos que é melhor para a segurança das chaves privadas do provedor VPN se eles usarem [servidores dedicados](https://en.wikipedia.org/wiki/Dedicated_hosting_service), em vez de soluções compartilhadas mais baratas (com outros clientes) como [servidores virtuais privados](https://pt.wikipedia.org/wiki/Servidor_virtual_privado).

#### :material-check:{ .pg-green } Revisado por auditoria independente

Mullvad's VPN clients have been audited by Cure53 and Assured AB in a pentest report [published at cure53.de](https://cure53.de/pentest-report_mullvad_v2.pdf). The security researchers concluded:

> Cure53 and Assured AB are happy with the results of the audit and the software leaves an overall positive impression. With security dedication of the in-house team at the Mullvad VPN compound, the testers have no doubts about the project being on the right track from a security standpoint.

In 2020 a second audit [was announced](https://mullvad.net/blog/2020/6/25/results-available-audit-mullvad-app) and the [final audit report](https://cure53.de/pentest-report_mullvad_2020_v2.pdf) was made available on Cure53's website:

> The results of this May-June 2020 project targeting the Mullvad complex are quite positive. [...] The overall application ecosystem used by Mullvad leaves a sound and structured impression. The overall structure of the application makes it easy to roll out patches and fixes in a structured manner. More than anything, the findings spotted by Cure53 showcase the importance of constantly auditing and re-assessing the current leak vectors, in order to always ensure privacy of the end-users. With that being said, Mullvad does a great job protecting the end-user from common PII leaks and privacy related risks.

In 2021 an infrastructure audit [was announced](https://mullvad.net/en/blog/2021/1/20/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit) and the [final audit report](https://cure53.de/pentest-report_mullvad_2021_v1.pdf) was made available on Cure53's website. Another report was commissioned [in June 2022](https://mullvad.net/en/blog/2022/6/22/vpn-server-audit-found-no-information-leakage-or-logging-of-customer-data) and is available on [Assured's website](https://assured.se/publications/Assured_Mullvad_relay_server_audit_report_2022.pdf).

#### :material-check:{ .pg-green } Clientes de Código Aberto (Open-Source)

Mullvad provides the source code for their desktop and mobile clients in their [GitHub organization](https://github.com/mullvad/mullvadvpn-app).

#### :material-check:{ .pg-green } Aceita Dinheiro e Monero

Mullvad, in addition to accepting credit/debit cards and PayPal, accepts Bitcoin, Bitcoin Cash, **Monero** and **cash/local currency** as anonymous forms of payment. Prepaid cards with redeem codes are also available. Mullvad also accepts Swish and bank wire transfers.

#### :material-check:{ .pg-green } Suporta WireGuard

Mullvad suporta o protocolo WireGuard®. [WireGuard](https://wireguard.com) is a newer protocol that uses state-of-the-art [cryptography](https://wireguard.com/protocol). Além disso, WireGuard pretende ser mais simples e mais eficiente.

Mullvad [recommends](https://mullvad.net/en/help/why-wireguard) the use of WireGuard with their service. It is the default or only protocol on Mullvad's Android, iOS, macOS, and Linux apps, but on Windows you have to [manually enable](https://mullvad.net/en/help/how-turn-wireguard-mullvad-app) WireGuard. Mullvad also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://wireguard.com/install).

#### :material-check:{ .pg-green } IPv6 Support

Mullvad allows you to [access services hosted on IPv6](https://mullvad.net/en/blog/2014/9/15/ipv6-support) and connect from a device using an IPv6 address.

#### :material-alert-outline:{ .pg-orange } Encaminhamento de Porta Remoto

Mullvad previously supported port forwarding, but removed the option in [May 2023](https://mullvad.net/en/blog/2023/5/29/removing-the-support-for-forwarded-ports). Missing this feature could negatively impact certain applications, especially peer-to-peer applications like torrent clients.

#### :material-check:{ .pg-green } Anti-Censorship

Mullvad has obfuscation an mode using [Shadowsocks with v2ray](https://mullvad.net/en/help/shadowsocks-with-v2ray) which may be useful in situations where VPN protocols like OpenVPN or Wireguard are blocked.

#### :material-check:{ .pg-green } Clientes Móveis

Mullvad has published [App Store](https://apps.apple.com/app/id1488466513) and [Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn) clients, both supporting an easy-to-use interface as opposed to requiring you to manually configure your WireGuard connection. The Android client is also available on [GitHub](https://github.com/mullvad/mullvadvpn-app/releases).

#### :material-information-outline:{ .pg-blue } Additional Notes

Mullvad is very transparent about which nodes they [own or rent](https://mullvad.net/en/servers). They use [ShadowSocks](https://shadowsocks.org) in their ShadowSocks + OpenVPN configuration, making them more resistant against firewalls with [Deep Packet Inspection](https://en.wikipedia.org/wiki/Deep_packet_inspection) trying to block VPNs. Supposedly, [China has to use a different method to block ShadowSocks servers](https://github.com/net4people/bbs/issues/22).

## Requisitos

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

É importante observar que o uso de um provedor de VPN não o tornará anônimo, mas lhe dará mais privacidade em determinadas situações. Uma VPN não é uma ferramenta para atividades ilegais. Não confie em uma política de "nenhum registro".

</div>

**Observe que não somos afiliados a nenhum dos provedores que recomendamos. Isso nos permite fornecer recomendações totalmente objetivas. **Em adição aos [nossos critérios básicos](about/criteria.md), desenvolvemos um conjunto claro de requisitos para qualquer provedor de VPN que deseje ser recomendado, incluindo criptografia forte, auditorias de segurança independentes, tecnologia moderna e muito mais. Sugerimos que você se familiarize com esta lista antes de escolher um provedor de VPN e faça sua própria pesquisa para garantir que o provedor de VPN escolhido seja o mais confiável possível.

### Tecnologia

Exigimos que todos os nossos provedores de VPN recomendados forneçam arquivos de configuração OpenVPN para serem usados em qualquer cliente. **Se** uma VPN fornecer seu próprio cliente personalizado, será necessário um killswitch para bloquear vazamentos de dados de rede quando desconectado.

**Mínimo Para Qualificação:**

- Suporte para protocolos fortes, como WireGuard & OpenVPN.
- Killswitch integrado aos clientes.
- Suporte a Multihop. O Multihopping é importante para manter os dados privados no caso de comprometimento de um único nó.
- If VPN clients are provided, they should be [open source](https://en.wikipedia.org/wiki/Open_source), like the VPN software they generally have built into them. Acreditamos que a disponibilidade do [código-fonte](https://en.wikipedia.org/wiki/Source_code) proporciona maior transparência sobre o que o seu dispositivo está realmente fazendo.

**Melhor Caso:**

- Killswitch com opções altamente configuráveis (ativar/desativar em determinadas redes, na inicialização, etc.)
- Clientes VPN fáceis de usar
- Suporta [IPv6](https://en.wikipedia.org/wiki/IPv6). Esperamos que os servidores permitam conexões de entrada via IPv6 e que você possa acessar serviços hospedados em endereços IPv6.
- O recurso de [encaminhamento remoto de portas](https://en.wikipedia.org/wiki/Port_forwarding#Remote_port_forwarding) ajuda a criar conexões ao usar o software de compartilhamento de arquivos P2P ([Peer-to-Peer](https://en.wikipedia.org/wiki/Peer-to-peer)) ou ao hospedar um servidor (por exemplo, Mumble).
- Obfuscation technology which pads data packets with random data to circumvent internet censorship.

### Privacidade

Preferimos que nossos provedores recomendados coletem o mínimo possível de dados. É necessário não coletar informações pessoais no registro e aceitar formas anônimas de pagamento.

**Mínimo Para Qualificação:**

- Opção de pagamento anônimo em [criptomoeda](cryptocurrency.md) **ou** em dinheiro.
- Nenhuma informação pessoal requerida para registro: Apenas nome de usuário, senha e e-mail, no máximo.

**Melhor Caso:**

- Aceita múltiplas [opções de pagamento anônimas](advanced/payments.md).
- Nenhuma informação pessoal é aceita (nome de usuário gerado automaticamente, nenhum e-mail necessário, etc.).

### Segurança

Uma VPN é inútil se não puder fornecer nem mesmo a segurança adequada. Exigimos que todos os nossos provedores recomendados cumpram os padrões de segurança atuais para suas conexões OpenVPN. O ideal é que eles usem, por padrão, esquemas de criptografia resistentes às mudanças futuras. Também exigimos que um terceiro independente audite a segurança do provedor, de preferência de forma bastante abrangente e repetida (anualmente).

**Mínimo Para Qualificação:**

- Esquemas de Criptografia Fortes: OpenVPN com autenticação SHA-256; handshake RSA-2048 ou melhor; criptografia de dados AES-256-GCM ou AES-256-CBC.
- Forward Secrecy.
- Auditorias de segurança publicadas por uma empresa terceirizada de boa reputação.

**Melhor Caso:**

- Criptografia Mais Forte: RSA-4096.
- Forward Secrecy.
- Auditorias abrangentes de segurança publicadas por uma empresa terceirizada de boa reputação.
- Programas de recompensa por bugs e/ou um processo coordenado de divulgação de vulnerabilidades.

### Confiança

Você não confiaria suas finanças a alguém com uma identidade falsa, então por que confiar seus dados de Internet a essa pessoa? Exigimos que nossos provedores recomendados sejam transparentes quanto a seus proprietários ou lideranças. Também esperamos ver relatórios de transparência frequentes, especialmente com relação à forma como as solicitações do governo são tratadas.

**Mínimo Para Qualificação:**

- Liderança ou propriedade voltada para o público.

**Melhor Caso:**

- Liderança orientada para o público (usuário).
- Relatórios de transparência frequentes.

### Marketing

Com os provedores de VPN que recomendamos, gostamos de ver um marketing responsável.

**Mínimo Para Qualificação:**

- Deve hospedar análises por conta própria (ou seja, nada de Google Analytics). O site do provedor também deve estar em conformidade com [DNT (Do Not Track)](https://en.wikipedia.org/wiki/Do_Not_Track) para pessoas que queiram optar por não participar.

Não deve ter nenhum marketing irresponsável:

- Garantir 100% de proteção ao anonimato. When someone makes a claim that something is 100% it means there is no certainty for failure. Sabemos que as pessoas podem se desanonimizar facilmente de várias maneiras, por exemplo:
    - Reutilização de informações pessoais (por exemplo, contas de e-mail, pseudônimos exclusivos, etc.) que eles acessaram sem software de anonimato (Tor, VPN, etc.)
    - [Impressão digital do navegador](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)
- Afirmar que uma VPN de circuito único é "mais anônima" do que o Tor, que é um circuito de três ou mais saltos que muda constantemente.
- Use uma linguagem responsável: por exemplo, não há problema em dizer que uma VPN está "desconectada" ou "não conectada", mas afirmar que alguém está "exposto", "vulnerável" ou "comprometido" é um uso desnecessário de linguagem alarmante que pode estar incorreta. Por exemplo, essa pessoa pode simplesmente estar no serviço de outro provedor de VPN ou usando o Tor.

**Melhor Caso:**

O marketing responsável que é educativo e útil para o consumidor pode incluir:

- Uma comparação precisa de quando o [Tor](tor.md) deve ser usado como alternativa.
- Disponibilidade do site do provedor de VPN em um [serviço .onion](https://en.wikipedia.org/wiki/.onion)

### Funções Adicionais

Embora não sejam requisitos estritos, há alguns fatores que consideramos ao determinar quais provedores recomendar. These include content blocking functionality, warrant canaries, multihop connections, excellent customer support, the number of allowed simultaneous connections, etc.
