---
meta_title: "Recomendações e Comparação de Serviços VPN Privados, Sem Patrocinadores ou Anúncios — Privacy Guides"
title: Serviços de VPN
icon: material/vpn
description: Os melhore serviços de VPN para proteção de sua privacidade digital e segurança online. Encontre aqui provedores que também não vão te espionar ou coletar seus dados.
cover: vpn.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>Protege contra as seguintes ameaças:</small>

- [:material-account-cash: Capitalismo de Vigilância](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Se você está procurando mais **privacidade** do seu provedor de internet (ISP), ou em uma rede Wi-Fi pública, ou ao fazer arquivos do tipo torrent, uma VPN pode será a melhor solução para você, desde que você também entenda os riscos envolvidos.

<div class="admonition danger" markdown>
<p class="admonition-title">As VPNs não fornecem anonimato</p>

O uso de uma VPN **não** manterá seus hábitos de navegação anônimos, nem adicionará segurança ao tráfego não seguro (HTTP).

Se você está procurando por **anonimato**, você deve usar o Navegador Tor **ao invés de ** de um serviço VPN. Se você está procurando por * * segurança * * adicional, você sempre deve verificar se está se conectando a sites que usam o prefixo HTTPS. Uma VPN não substitui boas práticas de segurança.

[Introduction to the Tor Browser](tor.md#tor-browser){ .md-button .md-button--primary } [Tor Myths & FAQ](advanced/tor-overview.md){ .md-button }

</div>

[Detalhes sobre VPNs :material-arrow-right-drop-circle:](basics/vpn-overview.md ""){.md-button}

## Provedores Recomendados

Nossas recomendações de provedores VPN usam criptografia, aceitam métodos de pagamento como Monero, suportam WireGuard & OpenVPN, e têm uma política de não registro de seus dados. Leia nossa [lista completa de requisitos](#criteria) para mais informações.

| Provedore             | Páises | WireGuard                     | Redirecionamento/Encaminhamento de portas | IPv6 (protocolo IP versão 6)                                   | Pagamentos anônimos          |
| --------------------- | ------ | ----------------------------- | ----------------------------------------- | -------------------------------------------------------------- | ---------------------------- |
| [Proton](#proton-vpn) | 127+   | :material-check:              | :material-alert-outline:{ .pg-orange }    | :material-information-outline:{ .pg-blue } Segurança dos Dados | Cash  Monero via third party |
| [IVPN](#ivpn)         | 41+    | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }    | :material-information-outline:{ .pg-blue } Mail apenas         | Monero  Cash                 |
| [Mullvad](#mullvad)   | 49+    | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange }    | :material-check:{ .pg-green }                                  | Monero  Cash                 |

### Proton VPN

<div class="admonition recommendation" markdown>

![Logomarca ProtonVPN](assets/img/vpn/protonvpn.svg){ align=right }

**Proton VPN** é um forte concorrente no espaço VPN, e estão em funcionamento desde 2016. Proton AG está sediada na Suíça e oferece um plano gratuito limitado, bem como uma opção paga com mais recursos.

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
- [ Web]()

</details>

</div>

#### :material-check:{ .pg-green } 127 Countries

Proton VPN has [servers in 127 countries](https://protonvpn.com/vpn-servers)(1) or [10](https://protonvpn.com/support/how-to-create-free-vpn-account) if you use their [free plan](https://protonvpn.com/blog/product-roadmap-winter-2025-2026).(2) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Isto deve-se a um caminho mais curto (menos pulos) até ao destino.
{ .annotate }

1. Of which at least 71 are virtual servers, meaning your IP will appear from the country but the server is in another. 12 more locations have both hardware and virtual servers. [Source](https://protonvpn.com/support/how-smart-routing-works)
2. Last checked: 2025-10-28

Nós também consideramos que é melhor para a segurança das chaves privadas do provedor VPN se eles usarem [servidores dedicados](https://en.wikipedia.org/wiki/Dedicated_hosting_service), em vez de soluções compartilhadas mais baratas (com outros clientes) como [servidores virtuais privados](https://pt.wikipedia.org/wiki/Servidor_virtual_privado).

#### :material-check:{ .pg-green } Revisado por auditoria independente

Independent security researcher Ruben Santamarta conducted audits for Proton VPN's [browser extensions](https://drive.proton.me/urls/RWDD2SHT98#v7ZrwNcafkG8) and [apps](https://drive.proton.me/urls/RVW8TXG484#uTXX5Fc9GADo) in September 2024 and January 2025, respectively. Proton VPN's infrastrcture has undergone [annual audits](https://protonvpn.com/blog/no-logs-audit) by Securitum since 2022.

Previously, Proton VPN underwent an independent audit by SEC Consult in January 2020. A SEC Consult encontrou algumas vulnerabilidades de médio e baixo risco nos aplicativos Windows, Android e iOS da Proton VPN, todos os quais foram "devidamente corrigidos" pela Proton VPN antes que os relatórios fossem publicados. Nenhum dos problemas identificados teria proporcionado acesso remoto ao seu dispositivo ou tráfego. You can view individual reports for each platform in their dedicated [blog post](https://web.archive.org/web/20250307041036/https://protonvpn.com/blog/open-source) on the audit.

#### :material-check:{ .pg-green } Clientes de Código Aberto (Open-Source)

Proton VPN provides the source code for their desktop and mobile clients in their [GitHub organization](https://github.com/ProtonVPN).

#### :material-check:{ .pg-green } Aceita Dinheiro

Proton VPN, in addition to accepting credit/debit cards, PayPal, and [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), also accepts **cash/local currency** as an anonymous form of payment. You can also use [**Monero**](cryptocurrency.md#monero) to purchase vouchers for Proton VPN Plus and Proton Unlimited via their [official](https://discuss.privacyguides.net/t/add-monero-as-an-anonymous-payment-method-for-proton-services/31058/15) reseller [ProxyStore](https://dys2p.com/en/2025-09-09-proton.html).

#### :material-check:{ .pg-green } Suporta WireGuard

IVPN tem suporte ao protocolo WireGuard®️. [O WireGuard](https://wireguard.com) é um protocolo mais recente que utiliza [criptografia](https://wireguard.com/protocol) de última geração. Além disso, WireGuard pretende ser mais simples e mais eficiente.

Proton VPN [recomenda](https://protonvpn.com/blog/wireguard) o uso do WireGuard em seus serviços. A Proton VPN também oferece um gerador de configuração do WireGuard para ser usado com os [aplicativos](https://www.wireguard.com/install/) oficiais do WireGuard.

#### :material-alert-outline:{ .pg-orange } Encaminhamento Remoto de Portas

O serviço de VPN da Proton [agora suporta IPv6](https://protonvpn.com/support/prevent-ipv6-vpn-leaks) em sua extensão de navegador e cliente Linux, mas apenas 80% de seus servidores são compatíveis com IPv6. Em outras plataformas, o cliente Proton VPN bloqueará todo o tráfego IPv6 de saída, para que você não precise se preocupar com o vazamento do seu endereço IPv6, mas não poderá se conectar a nenhum site somente IPv6, nem poderá se conectar ao Proton VPN a partir de uma rede somente IPv6.

#### :material-information-outline:{ .pg-info } Encaminhamento Remoto de Portas

Atualmente, o Proton VPN apenas oferece suporte ao [encaminhamento de porta](https://protonvpn.com/support/port-forwarding) remota efêmera via NAT-PMP, com tempos de concessão de 60 segundos. Os aplicativos oficiais para Windows e Linux oferecem uma opção de fácil acesso, enquanto em outros sistemas operacionais você precisará executar seu próprio [cliente NAT-PMP](https://protonvpn.com/support/port-forwarding-manual-setup). Os aplicativos de torrent geralmente têm suporte nativo NAT-PMP.

#### :material-information-outline:{ .pg-blue } Segurança dos Dados

O Proton VPN tem seu protocolo [Stealth](https://protonvpn.com/blog/stealth-vpn-protocol), que *pode* ajudar em situações em que os protocolos VPN, como o OpenVPN ou o WireGuard, são bloqueados com várias técnicas rudimentares. O Stealth isola o túnel VPN em uma sessão TLS para se parecer com o tráfego mais genérico da Internet.

Infelizmente, esse serviço não funciona muito bem em países onde são implantados filtros sofisticados que analisam todo o tráfego de saída na tentativa de descobrir túneis criptografados. O Stealth está disponível para Android, iOS, Windows e macOS, mas ainda não está disponível para Linux.

#### :material-check:{ .pg-green } Clientes Móveis

O Proton VPN publicou seus clientes na [App Store](https://apps.apple.com/app/id1437005085) e [no Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android), ambos com suporte a uma interface fácil de usar, em vez de exigir que você configure manualmente sua conexão WireGuard. A versão para Android também está disponível no [GitHub](https://github.com/ProtonVPN/android-app/releases).

<div class="admonition warning" markdown>
<p class="admonition-title">How to opt out of sharing telemetry</p>

On Android, Proton hides telemetry settings under the misleadingly labeled "**Help us fight censorship**" menu in the settings panel. On other platforms these settings can be found under the "**Usage statistics**" menu.

We are noting this because while we don't necessarily recommend against sharing anonymous usage statistics with developers, it is important that these settings are easily found and clearly labeled.

</div>

#### :material-information-outline:{ .pg-blue } Notas Adicionais

Os clientes Proton VPN suportam a autenticação de dois fatores em todas as plataformas, exceto no Linux, no momento. Proton VPN tem seus próprios servidores e centros de dados na Suíça, Islândia e Suécia. Eles oferecem bloqueio de propagandas e domínios de suspeitos (malware) conhecidos o serviço DNS. Além disso, Proton VPN também oferece servidores "Tor" que permitem que você se conecte facilmente a sites .onion, mas ainda fortemente recomendado o uso do [Navegador Tor](tor.md#tor-browser) oficial para essa finalidade.

##### :material-alert-outline:{ .pg-orange } O recurso Killswitch não funciona em Macs baseados em Intel

Podem [ocorrer erros](https://protonvpn.com/support/macos-t2-chip-kill-switch/) no sistema em Macs baseados em Intel ao usar o VPN *killswitch*. Se você precisar desse recurso e estiver usando um Mac com chipset Intel, considere usar outro serviço de VPN.

### IVPN

<div class="admonition recommendation" markdown>

![IVPN logo](assets/img/vpn/ivpn.svg){ align=right }

O **IVPN** é outro provedor de VPN premium e está em operação desde 2009. A IVPN está sediada em Gibraltar e não oferece uma avaliação gratuita.

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

IVPN has [servers in 41 countries](https://ivpn.net/status).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Isto deve-se a um caminho mais curto (menos pulos) até ao destino.
{ .annotate }

1. Last checked: 2025-10-28

Nós também consideramos que é melhor para a segurança das chaves privadas do provedor VPN se eles usarem [servidores dedicados](https://en.wikipedia.org/wiki/Dedicated_hosting_service), em vez de soluções compartilhadas mais baratas (com outros clientes) como [servidores virtuais privados](https://pt.wikipedia.org/wiki/Servidor_virtual_privado).

#### :material-check:{ .pg-green } Revisado por auditoria independente

A IVPN passou por várias [auditorias independentes](https://ivpn.net/en/blog/tags/audit) desde 2019 e anunciou publicamente seu compromisso com [auditorias de segurança anuais](https://ivpn.net/blog/ivpn-apps-security-audit-concluded).

#### :material-check:{ .pg-green } Clientes de Código Aberto (Open-Source)

A partir de fevereiro de 2020, [os aplicativos IVPN passaram a ser de código aberto](https://ivpn.net/blog/ivpn-applications-are-now-open-source). O código-fonte pode ser obtido da sua [organização (GitHub)](https://github.com/ivpn).

#### :material-check:{ .pg-green } Aceita Dinheiro e Monero

Além de aceitar cartões de crédito/débito e PayPal, IVPN aceita criptomoedas como Bitcoin, métodos de pagamento como **Monero** e **dinheiro** (em planos anuais) como formas anônimas de pagamento. You can also purchase [prepaid cards](https://ivpn.net/knowledgebase/billing/voucher-cards-faq) with redeem codes.

#### :material-check:{ .pg-green } Suporta WireGuard

IVPN suporta o protocolo WireGuard®️. [O WireGuard](https://wireguard.com) é um protocolo mais recente que utiliza [criptografia](https://wireguard.com/protocol) de última geração. Além disso, WireGuard pretende ser mais simples e mais eficiente.

IVPN [recomenda](https://ivpn.net/wireguard) o uso do serviço WireGuard em sua navegação, sendo assim, o protocolo padrão em todos os aplicativos do IVPN. O IVPN oferece também um gerador de configuração de perfis do WireGuard para ser usado com os [aplicativos](https://wireguard.com/install) oficiais do WireGuard.

#### :material-information-outline:{ .pg-blue } Suporte IPv6

A IVPN permite que você se conecte [a serviços que usam IPv6](https://ivpn.net/knowledgebase/general/do-you-support-ipv6), porém não permite que você se conecte a partir de um dispositivo que usa um endereço IPv6.

#### :material-alert-outline:{ .pg-orange } Encaminhamento de Porta Remoto

O IVPN suportava anteriormente o encaminhamento de portas, mas removeu a opção em [junho de 2023](https://ivpn.net/blog/gradual-removal-of-port-forwarding). A falta desse recurso pode afetar negativamente determinados aplicativos, especialmente aplicativos ponto a ponto, como clientes de torrent.

#### :material-check:{ .pg-green } Anti-censura

O IVPN tem modos de ofuscação usando o [V2Ray](https://v2ray.com/en/index.html), o que ajuda em situações em que os protocolos de VPN, como o OpenVPN ou o WireGuard, são bloqueados. Atualmente, esse recurso está disponível apenas para desktop e [iOS](https://ivpn.net/knowledgebase/ios/v2ray). Existem dois modos em que pode-se usar o [VMess](https://guide.v2fly.org/en_US/basics/vmess.html) em conexões QUIC ou TCP. O QUIC é um protocolo moderno com melhor controle de congestionamento e, portanto, pode ser mais rápido com latência reduzida. O modo TCP faz com que seus dados apareçam como tráfego HTTP normal.

#### :material-check:{ .pg-green } Clientes Móveis

A IVPN tem seus aplicativos disponíveis na [App Store](https://apps.apple.com/app/id1193122683) e [no Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client), ambos com uma interface fácil de usar, em vez de exigir que você configure manualmente sua conexão WireGuard. O cliente Android também está disponível no [GitHub](https://github.com/ivpn/android-app/releases).

#### :material-information-outline:{ .pg-blue } Notas Adicionais

Os clientes IVPN são compatíveis com a autenticação de dois fatores. IVPN também oferece a função "[AntiTracker](https://ivpn.net/antitracker)", que bloqueia redes de anúncios e rastreadores desde o nível da rede.

### Mullvad

<div class="admonition recommendation" markdown>

![Mullvad logo](assets/img/vpn/mullvad.svg){ align=right }

**Mullvad** é uma VPN rápida e barata com uma séria ênfase em transparência e segurança. A empresa opera desde 2009. A Mullvad está sediada na Suécia e oferece uma garantia de reembolso de 14 dias para os [métodos de pagamento](https://mullvad.net/en/help/refunds) que permitem isso.

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

#### :material-check:{ .pg-green } 49 Países

Mullvad possui [servidores em 49 países](https://mullvad.net/servers). (1) Escolher um provedor VPN com um servidor mais próximo a você reduzirá a latência do tráfego de rede que você envia. Isso se deve a uma rota mais curta (menos saltos) até o destino.
{ .annotate }

1. Last checked: 2025-10-28

Nós também consideramos que é melhor para a segurança das chaves privadas do provedor VPN se eles usarem [servidores dedicados](https://en.wikipedia.org/wiki/Dedicated_hosting_service), em vez de soluções compartilhadas mais baratas (com outros clientes) como [servidores virtuais privados](https://pt.wikipedia.org/wiki/Servidor_virtual_privado).

#### :material-check:{ .pg-green } Revisado por auditoria independente

A Mullvad se submeteu a várias [auditorias independentes](https://mullvad.net/en/blog/tag/audits) e anunciou publicamente seus esforços para realizar [auditorias anuais](https://mullvad.net/en/blog/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit) de seus aplicativos e infraestrutura.

#### :material-check:{ .pg-green } Clientes de Código Aberto (Open-Source)

A Mullvad fornece o código-fonte de seus clientes móveis e de desktop na página da  [organização no GitHub](https://github.com/mullvad/mullvadvpn-app).

#### :material-check:{ .pg-green } Aceita pagamentos em Dinheiro (depósito) e Monero

Mullvad, além de aceitar cartões de crédito/débito e PayPal, aceita criptomoedas como: Bitcoin, Bitcoin Cash, métodos de pagamento como **Monero** e **dinheiro** como formas anônimas de pagamento. You can also purchase [prepaid cards](https://mullvad.net/en/help/partnerships-and-resellers) with redeem codes. A Mullvad também aceita Swish e transferências bancárias, bem como alguns sistemas de pagamento europeus.

#### :material-check:{ .pg-green } Suporta WireGuard

Mullvad suporta o protocolo WireGuard®. [O WireGuard](https://wireguard.com) é um protocolo mais recente que utiliza [criptografia](https://wireguard.com/protocol) de última geração. Além disso, WireGuard pretende ser mais simples e mais eficiente.

Mullvad [recomenda](https://mullvad.net/en/help/why-wireguard) o uso do WireGuard em seu serviço. It is the only protocol supported on their mobile apps, and their desktop apps will [lose OpenVPN support](https://mullvad.net/en/blog/reminder-that-openvpn-is-being-removed) in 2025. Additionally, their servers will stop accepting OpenVPN connections by January 15, 2026. O IVPN também oferece um gerador de configuração do WireGuard para ser usado com os [aplicativos](https://www.wireguard.com/install/) oficiais do WireGuard.

#### :material-check:{ .pg-green } Suporte a IPv6

O Mullvad permite que você [acesse serviços hospedados no IPv6](https://mullvad.net/en/blog/2014/9/15/ipv6-support) e se conecte a partir de um dispositivo que usa um endereço IPv6.

#### :material-alert-outline:{ .pg-orange } Encaminhamento de Porta Remoto

O Mullvad suportava anteriormente o encaminhamento de portas, mas removeu a opção em [maio de 2023](https://mullvad.net/en/blog/2023/5/29/removing-the-support-for-forwarded-ports). A falta desse recurso pode afetar negativamente determinados aplicativos, especialmente aplicativos ponto a ponto, como clientes de torrent.

#### :material-check:{ .pg-green } Anti-censura

O Mullvad oferece vários recursos para ajudar a contornar a censura e acessar a Internet livremente:

- **Modos de ofuscação**: O Mullvad tem dois modos de ofuscação incorporados: "UDP-over-TCP" e ["WireGuard over Shadowsocks"](https://mullvad.net/en/blog/introducing-shadowsocks-obfuscation-for-wireguard). Esses modos disfarçam/camuflam o tráfego da VPN como tráfego normal da Web, dificultando a detecção e o bloqueio pelos censores. Supostamente, a China precisa usar um [novo método para interromper o tráfego roteado pelo Shadowsocks](https://gfw.report/publications/usenixsecurity23/en).
- **Ofuscação avançada com Shadowsocks e v2ray**: Para usuários mais avançados, o Mullvad fornece um guia sobre como usar o plug-in [Shadowsocks com v2ray](https://mullvad.net/en/help/shadowsocks-with-v2ray) com clientes Mullvad. Essa configuração fornece uma camada adicional de ofuscação e criptografia.
- **IPs de servidor personalizados**: Para evitar o bloqueio de IP, você pode solicitar IPs de servidor personalizados à equipe de suporte da Mullvad. Depois de receber os IPs personalizados, você pode inserir o arquivo de texto nas configurações de "Server IP override" (Substituição do IP do servidor), que substituirá os endereços IP do servidor escolhido por outros que não são conhecidos pelo censor.
- **Pontes e proxies**: A Mullvad também permite que você use pontes ou proxies para acessar a API (necessária para autenticação), o que pode ajudar a contornar tentativas de censura que bloqueiam o acesso à própria API.

#### :material-check:{ .pg-green } Clientes Móveis

O Mullvad publicou clientes [na App Store](https://apps.apple.com/app/id1488466513) e [no Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn), ambos com suporte a uma interface fácil de usar, em vez de exigir que você configure manualmente sua conexão WireGuard. O cliente Android também está disponível no [GitHub](https://github.com/mullvad/mullvadvpn-app/releases).

#### :material-information-outline:{ .pg-blue } Notas Adicionais

A Mullvad é muito transparente sobre quais nós são [de](https://mullvad.net/en/servers) sua [propriedade ou alugados](https://mullvad.net/en/servers). Eles também oferecem a opção de ativar a[DAITA (](https://mullvad.net/en/blog/daita-defense-against-ai-guided-traffic-analysis)Defense Against AI-guided Traffic Analysis) em seus aplicativos. A DAITA protege contra a ameaça da análise avançada de tráfego, que pode ser usada para conectar padrões no tráfego da VPN a sites específicos.

## Requisitos

<div class="admonition danger" markdown>
<p class="admonition-title">Aviso</p>

É importante observar que o uso de um provedor de VPN não o tornará anônimo, mas lhe dará mais privacidade em determinadas situações. Uma VPN não é uma ferramenta para atividades ilegais. Não confie em uma política de "nenhum registro".

</div>

**Observe que não somos afiliados a nenhum dos provedores que recomendamos. Isso nos permite fornecer recomendações totalmente objetivas. **Em adição aos [nossos critérios básicos](about/criteria.md), desenvolvemos um conjunto claro de requisitos para qualquer provedor de VPN que deseje ser recomendado, incluindo criptografia forte, auditorias de segurança independentes, tecnologia moderna e muito mais. Sugerimos que você se familiarize com esta lista antes de escolher um provedor de VPN e faça sua própria pesquisa para garantir que o provedor de VPN escolhido seja o mais confiável possível.

### Tecnologia

Exigimos que todos os nossos provedores de VPN recomendados forneçam arquivos de configuração OpenVPN para serem usados em qualquer cliente. **Se** uma VPN fornecer seu próprio cliente personalizado, será necessário um killswitch para bloquear vazamentos de dados de rede quando desconectado.

**Mínimo Para Qualificação:**

- Suporte a protocolos robustos, como o WireGuard e o OpenVPN.
- Killswitch integrado aos clientes.
- Suporte a Multihop. O *Multihopping* é importante para manter os dados protegidos no caso de comprometimento de um único nó da rede.
- Todos os clientes VPN fornecidos pelas marcas devem ser de [código aberto](https://en.wikipedia.org/wiki/Open_source), como o software VPN que eles normalmente trazem incorporado. Acreditamos que a disponibilidade do [código-fonte](https://en.wikipedia.org/wiki/Source_code) proporciona maior transparência sobre o que o seu dispositivo está realmente fazendo.
- Recursos de resistência à censura projetados para contornar firewalls sem DPI.

**Melhor Caso:**

- Função Killswitch com opções altamente personalizáveis (ativar/desativar em determinadas redes, na inicialização, etc.)
- Clientes VPN fáceis de usar
- Suporte a [IPv6](https://en.wikipedia.org/wiki/IPv6). Esperamos que os servidores permitam conexões de entrada via IPv6 e que você possa acessar serviços hospedados em endereços IPv6.
- O recurso de [encaminhamento remoto de portas](https://en.wikipedia.org/wiki/Port_forwarding#Remote_port_forwarding) ajuda a criar conexões ao usar o software de compartilhamento de arquivos P2P ([Peer-to-Peer](https://en.wikipedia.org/wiki/Peer-to-peer)) ou ao hospedar um servidor (por exemplo, Mumble).
- Tecnologia de ofuscação que camufla a verdadeira natureza do tráfego na internet, projetada para contornar métodos avançados de censura na internet, como DPI.

### Privacidade

Preferimos que nossos provedores recomendados coletem o mínimo possível de dados. É necessário não coletar informações pessoais no registro e aceitar formas anônimas de pagamento.

**Mínimo Para Qualificação:**

- Opção de pagamento anônimo em [criptomoeda](cryptocurrency.md) **ou** em dinheiro.
- Nenhuma informação pessoal requerida para registro: Apenas nome de usuário, senha e e-mail, no máximo.

**Melhor Caso:**

- Aceita múltiplas [opções de pagamento anônimas](advanced/payments.md).
- Não é necessário que sejam submetidas informações pessoais (nome de usuário gerado automaticamente, não é necessário e-mail, etc.).

### Segurança

Uma VPN é inútil se não puder fornecer nem mesmo a segurança adequada. Exigimos que todos os nossos provedores recomendados cumpram os padrões de segurança atuais para suas conexões OpenVPN. O ideal é que eles usem, por padrão, esquemas de criptografia resistentes às mudanças futuras. Também exigimos que um terceiro independente audite a segurança do provedor, de preferência de forma bastante abrangente e repetida (anualmente).

**Mínimo Para Qualificação:**

- Esquemas de Criptografia Fortes: OpenVPN com autenticação SHA-256; handshake RSA-2048 ou melhor; criptografia de dados AES-256-GCM ou AES-256-CBC.
- Sigilo de encaminhamento.
- Auditorias de segurança publicadas por uma empresa terceirizada de boa reputação.
- Servidores VPN que usam criptografia de disco completo ou são somente de RAM.

**Melhor Caso:**

- Criptografia Mais Forte: RSA-4096.
- Criptografia *quantum-resistant* opcional.
- Auditorias abrangentes de segurança publicadas por uma empresa terceirizada de boa reputação.
- Programas de recompensa por bugs e/ou um processo coordenado de divulgação de vulnerabilidades.
- Servidores VPN somente com RAM.

### Confiança

Você não confiaria suas finanças a alguém com uma identidade falsa, então por que confiar seus dados de Internet a essa pessoa? Exigimos que nossos provedores recomendados sejam transparentes quanto a seus proprietários ou lideranças. Também esperamos ver relatórios de transparência frequentes, especialmente com relação à forma como as solicitações do governo são tratadas.

**Mínimo Para Qualificação:**

- Liderança ou propriedade voltada para o público.
- Empresa sediada em uma jurisdição onde não pode se pode fazer registro secreto.

**Melhor Caso:**

- Liderança orientada para o público (usuário).
- Relatórios de transparência frequentes.

### Marketing

Com os provedores de VPN que recomendamos, gostamos de ver um marketing responsável.

**Mínimo Para Qualificação:**

- Deve hospedar seus dados estatísticos por conta própria (ou seja, nada de Google Analytics, Adobe Analytics, etc. ).

Não deve ter nenhum marketing irresponsável:

- Garantir 100% de proteção ao anonimato. Quando alguém afirma que alguma coisa é "100%", significa que não há certeza de fracasso. Sabemos que as pessoas podem se desanonimizar facilmente de várias maneiras, por exemplo:
    - Reutilização de informações pessoais (por exemplo, contas de e-mail, pseudônimos exclusivos, etc.) que eles acessaram sem software de anonimato (Tor, VPN, etc.)
    - [Impressão digital do navegador](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)
- Afirmar que uma VPN de circuito único é "mais anônima" do que o Tor, que é um circuito de três ou mais saltos que muda constantemente.
- Use uma linguagem responsável: por exemplo, não há problema em dizer que uma VPN está "desconectada" ou "não conectada", mas afirmar que alguém está "exposto", "vulnerável" ou "comprometido" é um uso desnecessário de linguagem alarmante que pode estar incorreta. Por exemplo, essa pessoa pode simplesmente estar no serviço de outro provedor de VPN ou usando o Tor.

**Melhor Caso:**

O marketing responsável que é educativo e útil para o consumidor pode incluir:

- Uma comparação precisa de quando o [Tor](tor.md) deve ser usado como alternativa.
- Disponibilidade do site do provedor de VPN em um [serviço .onion](https://en.wikipedia.org/wiki/.onion)

### Funções Adicionais

Embora não sejam requisitos estritos, há alguns fatores que consideramos ao determinar quais provedores recomendar. Isso inclui a funcionalidade de bloqueio de anúncios/rastreadores, canários de garantia, conexões multihop, excelente suporte ao cliente, o número de conexões simultâneas permitidas, etc.
