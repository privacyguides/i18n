---
meta_title: "Recomendações e comparações de serviços de privacidade VPN, sem patrocinadores ou anúncios - Privacy Guides"
title: "Serviços VPN"
icon: material/vpn
description: Estes são os melhores serviços VPN para proteger a sua privacidade e segurança online. Encontrará aqui fornecedores de Vpn que não o espiam.
cover: vpn.webp
---

Se procura privacidade adicional **** para o seu ISP, quando usa uma rede Wi-Fi pública ou enquanto faz torrenting de ficheiros, uma VPN pode ser a solução para si, desde que compreenda os riscos envolvidos. Consideramos que estes fornecedores estão um passo à frente dos restantes:

<div class="grid cards" markdown>

- ![Logótipo da Proton VPN](assets/img/vpn/protonvpn.svg){ .twemoji } [Proton VPN](#proton-vpn)
- ![Logótipo da IVPN](assets/img/vpn/mini/ivpn.svg){ .twemoji } [IVPN](#ivpn)
- ![Logótipo da Mullvad](assets/img/vpn/mullvad.svg){ .twemoji } [Mullvad](#mullvad)

</div>

!!! perigo "As VPN não proporcionam anonimato"

    A utilização de uma VPN **não** manterá a sua navegação anónima, nem acrescentará segurança adicional ao tráfego não seguro (HTTP).
    
    If you are looking for **anonymity**, you should use the Tor Browser.
    
    Se procura mais **segurança**, deve sempre garantir que se liga a sites que utilizem ligações HTTPS. Uma VPN não substitui as boas práticas de segurança.
    
    [Descarregar Tor](https://www.torproject.org/){ .md-button .md-button--primary } [Mitos do Tor & FAQ](advanced/tor-overview.md){ .md-button }

[Visão detalhada da VPN :material-arrow-right-drop-circle:](basics/vpn-overview.md ""){.md-button}

## Fornecedores recomendados

Os nossos fornecedores recomendados usam encriptação, aceitam Monero, suportam WireGuard & OpenVPN e têm uma política de não registo. Para mais informações, consulte a lista completa de critérios [](#criteria).

### Proton VPN

!!! recommendation annotate

    ![Logótipo Proton VPN](assets/img/vpn/protonvpn.svg){ align=right }
    
    O **Proton VPN** é um forte concorrente no espaço VPN, e está em funcionamento desde 2016. A Proton AG está sediada na Suíça e oferece uma opção gratuita com limitações, bem como uma opção premium com mais funcionalidades.
    
    [:octicons-home-16: Homepage](https://protonvpn.com/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://protonvpn.com/privacy-policy){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://protonvpn.com/support/){ .card-link title=Documentação}
    [:octicons-code-16:](https://github.com/ProtonVPN){ .card-link title="Código-fonte" }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android)
        - [:simple-appstore: App Store](https://apps.apple.com/app/apple-store/id1437005085)
        - [:simple-github: GitHub](https://github.com/ProtonVPN/android-app/releases)
        - [:simple-windows11: Windows](https://protonvpn.com/download-windows)
        - [:simple-linux: Linux](https://protonvpn.com/support/linux-vpn-setup/)

#### :material-check:{ .pg-green } 71 Countries

Proton VPN has [servers in 71 countries](https://protonvpn.com/vpn-servers) [or 3 if you use their free plan](https://protonvpn.com/free-vpn).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Isto deve-se ao facto do percurso até ao destino ser mais curto (menos saltos).
{ .annotate }

1. Last checked: 2023-12-21

Também achamos que é melhor para a segurança das chaves privadas do fornecedor de VPN a utilização de servidores dedicados [](https://en.wikipedia.org/wiki/Dedicated_hosting_service), em vez de soluções partilhadas mais baratas (com outros clientes), como os servidores privados virtuais [](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Auditado de forma independente

Em janeiro de 2020, o Proton VPN foi submetido a uma auditoria independente realizada pela SEC Consult. A SEC Consult encontrou algumas vulnerabilidades de risco médio e baixo nas aplicações Windows, Android e iOS do Proton VPN, todas elas "devidamente corrigidas" pelo Proton VPN antes da publicação dos relatórios. Nenhum dos problemas identificados permitia a um atacante aceder remotamente ao seu dispositivo ou tráfego. Pode consultar os relatórios individuais por plataforma em [protonvpn.com](https://protonvpn.com/blog/open-source/). Em abril de 2022, o Proton VPN foi submetido a [outra auditoria](https://protonvpn.com/blog/no-logs-audit/), sendo o relatório [produzido pela Securitum](https://protonvpn.com/blog/wp-content/uploads/2022/04/securitum-protonvpn-nologs-20220330.pdf). Uma declaração de conformidade [](https://proton.me/blog/security-audit-all-proton-apps) foi emitida para as aplicações Proton VPN, em 9 de novembro de 2021, pela [Securitum](https://research.securitum.com).

#### :material-check:{ .pg-green } Clientes de código aberto

O Proton VPN fornece o código-fonte para os seus clientes para desktop e para dispositivos móveis na sua página do [GitHub](https://github.com/ProtonVPN).

#### :material-check:{ .pg-green } Aceita dinheiro

O Proton VPN, além de aceitar cartões de crédito/débito, PayPal, e [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), também aceita **dinheiro/moeda local** como forma de pagamento anónimo.

#### :material-check:{ .pg-green } Suporte WireGuard

O Proton VPN suporta maioritariamente o protocolo WireGuard®. [O WireGuard](https://www.wireguard.com) é um protocolo mais recente que utiliza [encriptação de ponta](https://www.wireguard.com/protocol/). Além disso, o WireGuard aposta na simplicidade e no desempenho.

O Proton VPN [recomenda](https://protonvpn.com/blog/wireguard/) a utilização do WireGuard com o seu serviço. Nas aplicações Windows, macOS, iOS, Android, ChromeOS e Android TV do Proton VPN, o WireGuard é o protocolo predefinido; no entanto, o [suporte](https://protonvpn.com/support/how-to-change-vpn-protocols/) para o protocolo não está presente na sua aplicação Linux.

#### :material-alert-outline:{ .pg-orange } Encaminhamento de porta remota

Atualmente, o Proton VPN apenas suporta o reencaminhamento efémero de porta remota [](https://protonvpn.com/support/port-forwarding/) via NAT-PMP, com tempos de reserva (lease) de 60 segundos. A aplicação para Windows oferece uma opção de acesso fácil, enquanto noutros sistemas operativos terá de executar o seu próprio cliente [NAT-PMP](https://protonvpn.com/support/port-forwarding-manual-setup/). As aplicações torrent suportam frequentemente NAT-PMP de forma nativa.

#### :material-check:{ .pg-green } Censorship Circumvention

Proton VPN has their [Stealth](https://protonvpn.com/blog/stealth-vpn-protocol/) protocol which helps in situations where VPN protocols like OpenVPN or Wireguard are blocked. Stealth works by using an obfuscated TLS tunnel over TCP making it more difficult for deep packet inspection (DPI) to block.

#### :material-check:{ .pg-green } Clientes para dispositivos móveis

Para além de fornecer ficheiros de configuração OpenVPN padrão, o Proton VPN tem clientes para dispositivos móveis na [App Store](https://apps.apple.com/us/app/protonvpn-fast-secure-vpn/id1437005085), [Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android&hl=en_US) e [GitHub](https://github.com/ProtonVPN/android-app/releases), permitindo ligações fáceis aos seus servidores.

#### :material-information-outline:{ .pg-blue } Funcionalidade adicional

Os clientes Proton VPN suportam a autenticação de dois fatores em todas as plataformas, exceto no Linux, de momento. O Proton VPN tem os seus próprios servidores e centros de dados na Suíça, Islândia e Suécia. They offer content blocking and known-malware blocking with their DNS service. Adicionalmente, o Proton VPN também oferece servidores "Tor" que lhe permitem ligar-se facilmente a sites onion. Contudo, para esse feito, recomendamos vivamente a utilização do [, browser Tor oficial](https://www.torproject.org/).

#### :material-alert-outline:{ .pg-orange } A funcionalidade Killswitch não funciona nos Macs baseados em Intel

Falhas do sistema [podem ocorrer](https://protonvpn.com/support/macos-t2-chip-kill-switch/) em Macs baseados em Intel quando se utiliza o VPN killswitch. Se precisar desta funcionalidade e estiver a utilizar um Mac com chipset Intel, deve considerar a utilização de outro serviço VPN.

### IVPN

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo IVPN](assets/img/vpn/ivpn.svg){ align=right }
    
    O **IVPN** é outro fornecedor de VPN premium, e está em funcionamento desde 2009. A IVPN tem sede em Gibraltar.
    
    [:octicons-home-16: Homepage](https://www.ivpn.net/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.ivpn.net/privacy/){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://www.ivpn.net/knowledgebase/general/){ .card-link title=Documentação}
    [:octicons-code-16:](https://github.com/ivpn){ .card-link title="Código-fonte" }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client)
        - [:octicons-moon-16: Accrescent](https://accrescent.app/app/net.ivpn.client)
        - [:simple-appstore: App Store](https://apps.apple.com/app/ivpn-serious-privacy-protection/id1193122683)
        - [:simple-windows11: Windows](https://www.ivpn.net/apps-windows/)
        - [:simple-apple: macOS](https://www.ivpn.net/apps-macos/)
        - [:simple-linux: Linux](https://www.ivpn.net/apps-linux/)

#### :material-check:{ .pg-green } 37 Countries

IVPN has [servers in 37 countries](https://www.ivpn.net/server-locations).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Isto deve-se ao facto do percurso até ao destino ser mais curto (menos saltos).
{ .annotate }

1. Last checked: 2023-12-21

Também achamos que é melhor para a segurança das chaves privadas do fornecedor de VPN a utilização de servidores dedicados [](https://en.wikipedia.org/wiki/Dedicated_hosting_service), em vez de soluções partilhadas mais baratas (com outros clientes), como os servidores privados virtuais [](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Auditado de forma independente

O IVPN foi submetido a uma auditoria de não-registo [da Cure53](https://cure53.de/audit-report_ivpn.pdf), que concluiu da veracidade da alegação dessa política feita pelo IVPN. O IVPN também foi submetido a um teste abrangente de penetração, realizado pela [Cure53](https://cure53.de/summary-report_ivpn_2019.pdf), em janeiro de 2020. O IVPN também afirmou que planeia disponibilizar relatórios anuais [](https://www.ivpn.net/blog/independent-security-audit-concluded) no futuro. Foi realizada uma nova análise, [em abril de 2022](https://www.ivpn.net/blog/ivpn-apps-security-audit-2022-concluded/), produzida pela Cure53, [que está disponível no seu site](https://cure53.de/pentest-report_IVPN_2022.pdf).

#### :material-check:{ .pg-green } Clientes de código aberto

As of February 2020 [IVPN applications are now open source](https://www.ivpn.net/blog/ivpn-applications-are-now-open-source). O código-fonte pode ser obtido na sua página do [GitHub](https://github.com/ivpn).

#### :material-check:{ .pg-green } Aceita dinheiro e Monero

Além de aceitar cartões de crédito/débito e PayPal, o IVPN aceita Bitcoin, **Monero** e **cash/moeda local** (em planos anuais) como formas de pagamento anónimas.

#### :material-check:{ .pg-green } Suporte WireGuard

O IVPN suporta o protocolo WireGuard®. [O WireGuard](https://www.wireguard.com) é um protocolo mais recente que utiliza [encriptação de ponta](https://www.wireguard.com/protocol/). Além disso, o WireGuard aposta na simplicidade e no desempenho.

O IVPN [recomenda](https://www.ivpn.net/wireguard/) a utilização do WireGuard com o seu serviço, motivo pelo qual é protocolo padrão em todas as suas aplicações. O IVPN também oferece um gerador de configuração do WireGuard para utilização com as aplicações oficiais do WireGuard [](https://www.wireguard.com/install/).

#### :material-alert-outline:{ .pg-orange } Encaminhamento de porta remota

A IVPN suportava anteriormente o reencaminhamento de portas, mas removeu a opção em [junho de 2023](https://www.ivpn.net/blog/gradual-removal-of-port-forwarding). A falta desta funcionalidade pode ter um impacto negativo em certas aplicações, especialmente nas aplicações ponto-a-ponto, como os clientes de torrent.

#### :material-check:{ .pg-green } Censorship Circumvention

IVPN has obfuscation modes using the [v2ray](https://www.v2ray.com/en/index.html) project which helps in situations where VPN protocols like OpenVPN or Wireguard are blocked. Currently this feature is only available on Desktop and [iOS](https://www.ivpn.net/knowledgebase/ios/v2ray/). It has two modes where it can use [VMess](https://guide.v2fly.org/en_US/basics/vmess.html) over QUIC or TCP connections. QUIC is a modern protocol with better congestion control and therefore may be faster with reduced latency. The TCP mode makes your data appear as regular HTTP traffic.

#### :material-check:{ .pg-green } Clientes para dispositivos móveis

Para além de fornecer ficheiros de configuração OpenVPN padrão, o IVPN tem clientes para dispositivos móveis na [App Store](https://apps.apple.com/us/app/ivpn-serious-privacy-protection/id1193122683), [Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client) e [GitHub](https://github.com/ivpn/android-app/releases), permitindo ligações fáceis aos seus servidores.

#### :material-information-outline:{ .pg-blue } Funcionalidade adicional

Os clientes IVPN suportam autenticação de dois fatores (os clientes da Mullvad não suportam). O IVPN também fornece a funcionalidade "[AntiTracker](https://www.ivpn.net/antitracker)", que bloqueia redes de publicidade e rastreadores ao nível da rede.

### Mullvad

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo Mullvad](assets/img/vpn/mullvad.svg){ align=right }
    
    O **Mullvad** é uma VPN rápida e económica, com grande foco na transparência e segurança. Estão em funcionamento desde **2009**. O Mullvad está sediado na Suécia e não dispõe de uma versão de avaliação gratuita.
    
    [:octicons-home-16: Homepage](https://mullvad.net){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion){ .card-link title="Serviço Onion" }
    [:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy/){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://mullvad.net/en/help/){ .card-link title=Documentação}
    [:octicons-code-16:](https://github.com/mullvad){ .card-link title="Código-fonte" }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn)
        - [:simple-appstore: App Store](https://apps.apple.com/app/mullvad-vpn/id1488466513)
        - [:simple-github: GitHub](https://github.com/mullvad/mullvadvpn-app/releases)
        - [:simple-windows11: Windows](https://mullvad.net/en/download/windows/)
        - [:simple-apple: macOS](https://mullvad.net/en/download/macos/)
        - [:simple-linux: Linux](https://mullvad.net/en/download/linux/)

#### :material-check:{ .pg-green } 40 Countries

Mullvad has [servers in 40 countries](https://mullvad.net/servers/).(1) Picking a VPN provider with a server nearest to you will reduce latency of the network traffic you send. Isto deve-se ao facto do percurso até ao destino ser mais curto (menos saltos).
{ .annotate }

1. Last checked: 2023-12-21

Também achamos que é melhor para a segurança das chaves privadas do fornecedor de VPN a utilização de servidores dedicados [](https://en.wikipedia.org/wiki/Dedicated_hosting_service), em vez de soluções partilhadas mais baratas (com outros clientes), como os servidores privados virtuais [](https://en.wikipedia.org/wiki/Virtual_private_server).

#### :material-check:{ .pg-green } Auditado de forma independente

Os clientes VPN do Mullvad foram auditados pela Cure53 e pela Assured AB, com os resultados disponíveis num relatório de testes de penetração [publicado em cure53.de](https://cure53.de/pentest-report_mullvad_v2.pdf). Os investigadores de segurança concluíram:

> A Cure53 e a Assured AB estão satisfeitas com os resultados da auditoria e referem que o software deixa uma impressão globalmente positiva. Com uma equipa interna dedicada à segurança a trabalhar nas instalações do Mullvad, os auditores não têm dúvidas de que o projeto está no bom caminho, do ponto de vista da segurança.

Em 2020, foi anunciada uma segunda auditoria,[](https://mullvad.net/blog/2020/6/25/results-available-audit-mullvad-app/) cujo relatório final foi disponibilizado [no site da Cure53](https://cure53.de/pentest-report_mullvad_2020_v2.pdf):

> Os resultados desta auditoria realizada em maio-junho de 2020, que visou as instalações do Mullvad, são bastante positivos. [...] O ecossistema global de aplicações utilizado pelo Mullvad deixa uma impressão sólida e estruturada. A estrutura geral da aplicação facilita a implementação de patches e correções de uma forma estruturada. Acima de tudo, o que foi detetado pela Cure53 mostra a importância de auditar e reavaliar constantemente os atuais vectores de fuga de informação, de modo a garantir sempre a privacidade dos utilizadores finais. Dito isto, o Mullvad faz um excelente trabalho ao proteger o utilizador final das fugas comuns de informações pessoais e dos riscos relacionados com a privacidade.

Em 2021, foi anunciada uma auditoria às infraestruturas [](https://mullvad.net/en/blog/2021/1/20/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit/), sendo relatório final da auditoria disponibilizado [no site da Cure53](https://cure53.de/pentest-report_mullvad_2021_v1.pdf). Foi encomendado outro relatório [em junho de 2022](https://mullvad.net/en/blog/2022/6/22/vpn-server-audit-found-no-information-leakage-or-logging-of-customer-data/), que está disponível no site da [Assured](https://www.assured.se/publications/Assured_Mullvad_relay_server_audit_report_2022.pdf).

#### :material-check:{ .pg-green } Clientes de código aberto

O Mullvad fornece o código-fonte dos seus clientes desktop e para dispositivos móveis na sua página do [GitHub](https://github.com/mullvad/mullvadvpn-app).

#### :material-check:{ .pg-green } Aceita dinheiro e Monero

O Mullvad, para além de aceitar cartões de crédito/débito e PayPal, aceita Bitcoin, Bitcoin Cash, **Monero** e **cash/moeda local** como formas de pagamento anónimas. Também aceita Swish e transferências bancárias.

#### :material-check:{ .pg-green } Suporte WireGuard

O Mullvad suporta o protocolo WireGuard®. [O WireGuard](https://www.wireguard.com) é um protocolo mais recente que utiliza [encriptação de ponta](https://www.wireguard.com/protocol/). Além disso, o WireGuard aposta na simplicidade e no desempenho.

O Mullvad [recomenda](https://mullvad.net/en/help/why-wireguard/) a utilização do WireGuard com o seu serviço. É o protocolo predefinido ou único nas aplicações do Mullvad para Android, iOS, macOS e Linux. No caso do Windows, deve ser feita [uma ativação manual](https://mullvad.net/en/help/how-turn-wireguard-mullvad-app/) do WireGuard. O Mullvad também oferece um gerador de configuração do WireGuard para utilização com as [aplicações oficiais do WireGuard](https://www.wireguard.com/install/).

#### :material-check:{ .pg-green } Suporte IPv6

O Mullvad permite-lhe [aceder a serviços alojados em IPv6](https://mullvad.net/en/blog/2014/9/15/ipv6-support/), ao contrário de outros fornecedores que bloqueiam as ligações IPv6.

#### :material-alert-outline:{ .pg-orange } Encaminhamento de porta remota

O Mullvad suportava anteriormente o reencaminhamento de portas, mas removeu a opção em [maio de 2023](https://mullvad.net/en/blog/2023/5/29/removing-the-support-for-forwarded-ports/). A falta desta funcionalidade pode ter um impacto negativo em certas aplicações, especialmente nas aplicações ponto-a-ponto, como os clientes de torrent.

#### :material-check:{ .pg-green } Censorship Circumvention

Mullvad has obfuscation an mode using [Shadowsocks with v2ray](https://mullvad.net/en/help/shadowsocks-with-v2ray) which may be useful in situations where VPN protocols like OpenVPN or Wireguard are blocked.

#### :material-check:{ .pg-green } Clientes para dispositivos móveis

O Mullvad disponibilizou [clientes na App Store](https://apps.apple.com/app/mullvad-vpn/id1488466513) e [clientes no Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn), ambos suportando uma interface de fácil utilização, que não necessita de uma configuração manual da conexão WireGuard. O cliente Android também está disponível na página do [GitHub](https://github.com/mullvad/mullvadvpn-app/releases).

#### :material-information-outline:{ .pg-blue } Funcionalidade adicional

O Mullvad é muito transparente relativamente aos nós de rede que [possui ou aluga](https://mullvad.net/en/servers/). Utiliza [ShadowSocks](https://shadowsocks.org/) na sua configuração ShadowSocks + OpenVPN, tornando-os mais resistentes a firewalls com [Deep Packet Inspection](https://en.wikipedia.org/wiki/Deep_packet_inspection) que tentam bloquear VPNs. Supostamente, a [China tem de utilizar um método diferente para bloquear os servidores ShadowSocks](https://github.com/net4people/bbs/issues/22). O site do Mullvad também está acessível através do Tor em [o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion).

## Critérios

!!! perigo

    É importante notar que a utilização de um fornecedor de VPN não o tornará anónimo, mas dar-lhe-á mais privacidade em determinadas situações. Uma VPN não é uma ferramenta para atividades ilegais. Não confie numa política de "não registo".

**Tenha em atenção que não somos afiliados de nenhum dos fornecedores que recomendamos. Esta facto permite-nos fornecer recomendações completamente objetivas.** Para além dos [nossos critérios padrão](about/criteria.md), desenvolvemos um conjunto claro de requisitos para qualquer fornecedor de VPN que pretenda ser recomendado, incluindo encriptação forte, auditorias de segurança independentes, tecnologia moderna e muito mais. Sugerimos que se familiarize com esta lista, antes de escolher um fornecedor de VPN, e que faça a sua própria pesquisa para garantir uma escolha de fornecedor de VPN o mais fiável possível.

### Tecnologia

Exigimos que todos os nossos fornecedores de VPN recomendados forneçam ficheiros de configuração OpenVPN para serem utilizados em qualquer cliente. **Se** uma VPN fornecer o seu próprio cliente personalizado, é necessário um killswitch que bloqueie as fugas de dados da rede no caso da VPN se desconectar.

**Mínimos de qualificação:**

- Suporte para protocolos fortes, como o WireGuard e OpenVPN.
- Killswitch incorporado nos clientes.
- Suporte multihop. O multihopping é importante para manter os dados privados, no caso de um nó de rede ser comprometido.
- If VPN clients are provided, they should be [open source](https://en.wikipedia.org/wiki/Open_source), like the VPN software they generally have built into them. Acreditamos que a disponibilidade do [código-fonte](https://pt.wikipedia.org/wiki/C%C3%B3digo-fonte) proporciona uma maior transparência em relação ao que o seu dispositivo está realmente a fazer.

**Melhor caso:**

- Suporte WireGuard e OpenVPN.
- Killswitch com opções altamente configuráveis (ativar/desativar em determinadas redes, no arranque, etc.)
- Clientes VPN fáceis de utilizar
- Suporte [IPv6](https://en.wikipedia.org/wiki/IPv6). É suposto que os servidores permitam ligações de entrada através do IPv6 e que lhe permitam aceder a serviços alojados em endereços IPv6.
- A capacidade de [reencaminhamento de portas remotas](https://en.wikipedia.org/wiki/Port_forwarding#Remote_port_forwarding) ajuda a criar ligações quando se utiliza software de partilha de ficheiros P2P ([Peer-to-Peer](https://en.wikipedia.org/wiki/Peer-to-peer)) ou se aloja um servidor (por exemplo, Mumble).

### Privacidade

Preferimos que os nossos fornecedores recomendados recolham o mínimo de dados possível. Não devem ser recolhidas informações pessoais aquando do registo e devem ser aceites formas de pagamento anónimas.

**Mínimos de qualificação:**

- [Criptomoeda anónima](cryptocurrency.md) **ou ** opção de pagamento em dinheiro.
- Não devem ser necessárias informações pessoais para o registo: no limite, apenas o nome de utilizador, a palavra-passe e o e-mail.

**Melhor caso:**

- Deve aceitar várias opções de pagamento anónimo [](advanced/payments.md).
- Não devem ser pedidas informações pessoais (deve ser possível utilizar um nome de utilizador gerado automaticamente, não deve ser necessário e-mail, etc.).

### Segurança

Uma VPN é inútil se não proporcionar uma segurança adequada. Exigimos que todos os nossos fornecedores recomendados cumpram as normas de segurança atuais para as suas ligações OpenVPN. O ideal será a utilização, por defeito, de esquemas de encriptação mais resistentes ao futuro. Também exigimos que um terceiro independente audite a segurança do fornecedor, idealmente de uma forma muito abrangente e numa base regular (anual).

**Mínimos de qualificação:**

- Esquemas de encriptação fortes: OpenVPN com autenticação SHA-256; handshake RSA-2048 ou superior; encriptação de dados AES-256-GCM ou AES-256-CBC.
- Forward Secrecy.
- Auditorias de segurança publicadas por uma empresa terceira de renome.

**Melhor caso:**

- Encriptação máxima: RSA-4096.
- Forward Secrecy.
- Auditorias de segurança exaustivas publicadas por uma empresa terceira de renome.
- Programas de recompensa por deteção de erros e/ou processos coordenados de divulgação de vulnerabilidades.

### Confiança

Se não confiaria as suas finanças a alguém com uma identidade falsa, porque motivo lhe confiaria os seus dados de Internet? Exigimos que os nossos fornecedores recomendados sejam transparentes em relação à sua propriedade ou liderança. Gostaríamos também de ver relatórios de transparência frequentes, especialmente no que diz respeito à forma como os pedidos do governo são tratados.

**Mínimos de qualificação:**

- Liderança ou propriedade virada para o público.

**Melhor caso:**

- Liderança virada para o público.
- Perfect Forward Secrecy (PFS).

### Marketing

Os fornecedores de VPN que recomendamos devem ter uma política de marketing responsável.

**Mínimos de qualificação:**

- Deve ter sistema de análise de estatísticas auto-hospedado (não podem usar o Google Analytics). O site do fornecedor deve estar em conformidade com a norma [DNT (Do Not Track)](https://en.wikipedia.org/wiki/Do_Not_Track), no caso das pessoas não pretenderem participar.

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

Embora não sejam requisitos obrigatórios, existem alguns fatores que valorizamos, quando determinamos quais os fornecedores a recomendar. These include content blocking functionality, warrant canaries, multihop connections, excellent customer support, the number of allowed simultaneous connections, etc.
