---
meta_title: "Recomendações e Comparação de Serviços VPN Privados, Sem Patrocinadores ou Anúncios — Privacy Guides"
title: "Serviços de VPN"
icon: material/vpn
description: Estes são os melhores serviços VPN para proteger sua privacidade e segurança on-line. Encontre aqui um provedor que não tem como objetivo espionar você.
cover: vpn.png
---

Se você está procurando mais **privacidade** do seu provedor de internet (ISP), ou em uma rede Wi-Fi pública, ou ao fazer torrent de arquivos, uma VPN pode ser a solução para você, desde que entenda os riscos envolvidos. Nós entendemos que estes provedores estão acima dos demais:

<div class="grid cards" markdown>

- ![Proton VPN logo](assets/img/vpn/protonvpn.svg){ .twemoji } [Proton VPN](#proton-vpn)
- ![IVPN logo](assets/img/vpn/mini/ivpn.svg){ .twemoji } [IVPN](#ivpn)
- ![Mullvad logo](assets/img/vpn/mullvad.svg){ .twemoji } [Mullvad](#mullvad)

</div>

!!! danger "As VPNs não proporcionam anonimato"

    Usar uma VPN **não** manterá seus hábitos de navegação anônimos, nem adicionará segurança ao tráfego não seguro (HTTP).
    
    Se você está procurando por **anonimato**, você deve usar o Navegador Tor **ao invés de ** de uma VPN.
    
    Se você está procurando por * * segurança * * adicional, você sempre deve verificar se está se conectando a sites que usam HTTPS. Uma VPN não substitui boas práticas de segurança.
    
    [Baixar Tor Browser](https://www.torproject.org/){ .md-button .md-button--primary } [Mitos sobre o Tor Browser & FAQ](advanced/tor-overview.md){ .md-button }

[Detalhes sobre VPNs :material-arrow-right-drop-circle:](basics/vpn-overview.md ""){.md-button}

## Provedores Recomendados

Nossos provedores recomendados usam criptografia, aceitam Monero, suportam WireGuard & OpenVPN, e têm uma política de não registro. Leia nossa [lista completa de requisitos](#criteria) para mais informações.

### Proton VPN

!!! anotar recomendação

    ![Logomarca ProtonVPN](assets/img/vpn/protonvpn.svg){ align=right }
    
    **Proton VPN** é um forte concorrente no espaço VPN, e estão em funcionamento desde 2016. Proton AG está sediada na Suíça e oferece um plano gratuito limitado, bem como uma opção paga com mais recursos.
    
    [:octicons-home-16: Página Inicial](https://protonvpn.com/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://protonvpn.com/privacy-policy){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://protonvpn.com/support/){ .card-link title=Documentação}
    [:octicons-code-16:](https://github.com/ProtonVPN){ .card-link title="Código Fonte" }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android)
        - [:simple-appstore: App Store](https://apps.apple.com/app/apple-store/id1437005085)
        - [:simple-github: GitHub](https://github.com/ProtonVPN/android-app/releases)
        - [:simple-windows11: Windows](https://protonvpn.com/download-windows)
        - [:simple-linux: Linux](https://protonvpn.com/support/linux-vpn-setup/)

#### :material-check:{ .pg-green } 67 Countries

Proton VPN tem [servidores em 67 países](https://protonvpn.com/vpn-servers). (1) Escolher um provedor VPN com um servidor mais próximo de você reduzirá a latência do tráfego de rede que você envia. Isto deve-se a um caminho mais curto (menos pulos) até ao destino.
{ .annotate }

1. Última verificação: 16-09-2022

Nós também consideramos que é melhor para a segurança das chaves privadas do provedor VPN se eles usarem [servidores dedicados](https://en.wikipedia.org/wiki/Dedicated_hosting_service), em vez de soluções compartilhadas mais baratas (com outros clientes) como [servidores virtuais privados](https://pt.wikipedia.org/wiki/Servidor_virtual_privado).

#### :material-check:{ .pg-green } Examinado por auditores externos

Em Janeiro de 2020, ProtonVPN foi submetida a uma auditoria independente pela SEC Consult. A SEC Consult encontrou algumas vulnerabilidades de médio e baixo risco nos aplicativos Windows, Android e iOS da Proton VPN, todos os quais foram "devidamente corrigidos" pela Proton VPN antes que os relatórios fossem publicados. Nenhum dos problemas identificados teria proporcionado acesso remoto ao seu dispositivo ou tráfego. Você pode ver os relatórios individuais para cada plataforma em [protonvpn.com](https://protonvpn.com/blog/open-source/). Em abril de 2022 Proton VPN passou por [outra auditoria](https://protonvpn.com/blog/no-logs-audit/) e o relatório foi [produzido pelo Securitum](https://protonvpn.com/blog/wp-content/uploads/2022/04/securitum-protonvpn-nologs-20220330.pdf). Um [certificado de segurança](https://proton.me/blog/security-audit-all-proton-apps) foi concedido para os aplicativos do Proton Mail em 9 de Novembro de 2021 pela [Securitium](https://research.securitum.com).

#### :material-check:{ .pg-green } Clientes de Código Aberto (Open-Source)

Proton VPN fornece o código-fonte de seus clientes móveis e de desktop em sua [organização GitHub](https://github.com/ProtonVPN).

#### :material-check:{ .pg-green } Aceita Dinheiro

Proton VPN, além de aceitar cartões de crédito/débito, PayPal e [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc), também aceita **dinheiro/moeda local** como forma anônima de pagamento.

#### :material-check:{ .pg-green } Suporta WireGuard

Proton VPN suporta principalmente o protocolo WireGuard®. [WireGuard](https://www.wireguard.com) é um protocolo mais recente que usa criptografia de última geração [](https://www.wireguard.com/protocol/). Além disso, WireGuard pretende ser mais simples e mais eficiente.

Proton VPN [recomenda](https://protonvpn.com/blog/wireguard/) o uso do WireGuard em seu serviço. Nos aplicativos do Proton VPN para Windows, macOS, iOS, Android, ChromeOS e Android TV, o WireGuard é o protocolo padrão; no entanto, o [suporte](https://protonvpn.com/support/how-to-change-vpn-protocols/) para o protocolo não está presente em seu aplicativo para Linux.

#### :material-alert-outline:{ .pg-orange } Encaminhamento de Porta Remoto

Proton VPN currently only supports ephemeral remote [port forwarding](https://protonvpn.com/support/port-forwarding/) via NAT-PMP, with 60 second lease times. The Windows app provides an easy to access option for it, while on other operating systems you'll need to run your own [NAT-PMP client](https://protonvpn.com/support/port-forwarding-manual-setup/). Torrent applications often support NAT-PMP natively.

#### :material-check:{ .pg-green } Clientes Móveis

Além de fornecer arquivos de configuração padronizados para o OpenVPN, o Proton VPN tem clientes móveis para a [App Store](https://apps.apple.com/us/app/protonvpn-fast-secure-vpn/id1437005085), [Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android&hl=en_US) e [GitHub](https://github.com/ProtonVPN/android-app/releases), permitindo conexões fáceis com seus servidores.

#### :material-information-outline:{ .pg-blue } Funcionalidades Adicionais

Os clientes Proton VPN suportam a autenticação de dois fatores em todas as plataformas, exceto no Linux, no momento. Proton VPN tem seus próprios servidores e centros de dados na Suíça, Islândia e Suécia. Eles oferecem bloqueio de anúncios e bloqueio de domínios de vírus (malware) conhecidos com seu serviço DNS. Além disso, Proton VPN também oferece servidores "Tor" que permitem que você se conecte facilmente a sites onion, mas ainda recomendamos fortemente o uso do [Navegador Tor oficial](https://www.torproject.org/) para essa finalidade.

#### :material-alert-outline:{ .pg-orange } O recurso Killswitch não funciona em Macs baseados em Intel

Podem [ocorrer falhas](https://protonvpn.com/support/macos-t2-chip-kill-switch/) no sistema em Macs baseados em Intel ao usar o VPN killswitch. Se você precisar desse recurso e estiver usando um Mac com chipset Intel, considere usar outro serviço de VPN.

### IVPN

!!! recommendation

    ![IVPN logo](assets/img/vpn/ivpn.svg){ align=right }
    
    **IVPN** is another premium VPN provider, and they have been in operation since 2009. A IVPN está sediada em Gibraltar.
    
    [:octicons-home-16: Homepage](https://www.ivpn.net/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.ivpn.net/privacy/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://www.ivpn.net/knowledgebase/general/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/ivpn){ .card-link title="Source Code" }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client)
        - [:octicons-moon-16: Accrescent](https://accrescent.app/app/net.ivpn.client)
        - [:simple-appstore: App Store](https://apps.apple.com/app/ivpn-serious-privacy-protection/id1193122683)
        - [:simple-windows11: Windows](https://www.ivpn.net/apps-windows/)
        - [:simple-apple: macOS](https://www.ivpn.net/apps-macos/)
        - [:simple-linux: Linux](https://www.ivpn.net/apps-linux/)

#### :material-check:{ .pg-green } 35 Countries

IVPN tem [servidores em 35 países](https://www.ivpn.net/server-locations). (1) Escolher um provedor VPN com um servidor mais próximo de você reduzirá a latência do tráfego de rede que você envia. Isto deve-se a um caminho mais curto (menos pulos) até ao destino.
{ .annotate }

1. Última verificação: 16-09-2022

Nós também consideramos que é melhor para a segurança das chaves privadas do provedor VPN se eles usarem [servidores dedicados](https://en.wikipedia.org/wiki/Dedicated_hosting_service), em vez de soluções compartilhadas mais baratas (com outros clientes) como [servidores virtuais privados](https://pt.wikipedia.org/wiki/Servidor_virtual_privado).

#### :material-check:{ .pg-green } Examinado por auditores externos

IVPN foi submetido a uma [auditoria de ausência de registro de dados (no-logging) pela Cure53](https://cure53.de/audit-report_ivpn.pdf), cuja conclusão confirmou a reivindicação de que o IVPN não registra dados. IVPN também elaborou um [relatório completo de Teste de Penetração (pentest) pela Cure53](https://cure53.de/summary-report_ivpn_2019.pdf) em janeiro de 2020. IVPN também disse que eles planejam ter [relatórios anuais](https://www.ivpn.net/blog/independent-security-audit-concluded) no futuro. Uma revisão adicional foi feita [em abril de 2022](https://www.ivpn.net/blog/ivpn-apps-security-audit-2022-concluded/) e foi publicada pela Cure53 [em seu site](https://cure53.de/pentest-report_IVPN_2022.pdf).

#### :material-check:{ .pg-green } Clientes de Código Aberto (Open-Source)

A partir de fevereiro de 2020, [aplicativos IVPN agora são de código aberto](https://www.ivpn.net/blog/ivpn-applications-are-now-open-source). O código-fonte pode ser obtido da sua [organização (GitHub)](https://github.com/ivpn).

#### :material-check:{ .pg-green } Aceita Dinheiro e Monero

Além de aceitar cartões de crédito/débito e PayPal, IVPN aceita Bitcoin, **Monero** e **dinheiro/moeda local** (em planos anuais) como formas anônimas de pagamento.

#### :material-check:{ .pg-green } Suporta WireGuard

IVPN suporta o protocolo WireGuard®️. [WireGuard](https://www.wireguard.com) é um protocolo mais recente que usa criptografia de última geração [](https://www.wireguard.com/protocol/). Além disso, WireGuard pretende ser mais simples e mais eficiente.

IVPN [recomenda](https://www.ivpn.net/wireguard/) o uso do WireGuard em seu serviço e, sendo assim, ele é o protocolo padrão em todos os aplicativos do IVPN. O IVPN também oferece um gerador de configuração do WireGuard para ser usado com os [aplicativos](https://www.wireguard.com/install/) oficiais do WireGuard.

#### :material-alert-outline:{ .pg-orange } Encaminhamento de Porta Remoto

IVPN previously supported port forwarding, but removed the option in [June 2023](https://www.ivpn.net/blog/gradual-removal-of-port-forwarding). Missing this feature could negatively impact certain applications, especially peer-to-peer applications like torrent clients.

#### :material-check:{ .pg-green } Clientes Móveis

Além de disponibilizar os arquivos de configuração padrão do OpenVPN, o IVPN tem aplicativos móveis disponíveis na [App Store](https://apps.apple.com/us/app/ivpn-serious-privacy-protection/id1193122683), [Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client) e [GitHub](https://github.com/ivpn/android-app/releases), facilitando a conexão com seus servidores.

#### :material-information-outline:{ .pg-blue } Funcionalidades Adicionais

Aplicativos IVPN suportam autenticação de dois fatores (aplicativos Mullvad não suportam). IVPN também oferece a função "[AntiTracker](https://www.ivpn.net/antitracker)", que bloqueia redes de anúncios e rastreadores desde o nível da rede.

### Mullvad

!!! recommendation

    ![Mullvad logo](assets/img/vpn/mullvad.svg){ align=right }
    
    **Mullvad** é uma VPN rápida e barata com uma séria ênfase em transparência e segurança. Eles estão ativos desde **2009***. Mullvad está localizado na Suécia e não oferece um teste gratuito de avaliação.
    
    [:octicons-home-16: Homepage](https://mullvad.net){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion){ .card-link title="Onion Service" }
    [:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://mullvad.net/en/help/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/mullvad){ .card-link title="Source Code" }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn)
        - [:simple-appstore: App Store](https://apps.apple.com/app/mullvad-vpn/id1488466513)
        - [:simple-github: GitHub](https://github.com/mullvad/mullvadvpn-app/releases)
        - [:simple-windows11: Windows](https://mullvad.net/en/download/windows/)
        - [:simple-apple: macOS](https://mullvad.net/en/download/macos/)
        - [:simple-linux: Linux](https://mullvad.net/en/download/linux/)

#### :material-check:{ .pg-green } 41 Países

Mullvad tem [servidores em 41 países](https://mullvad.net/servers/). (1) Escolher um provedor VPN com um servidor mais próximo de você reduzirá a latência do tráfego de rede que você envia. Isso se deve a uma rota mais curta (menos saltos) até o destino.
{ .annotate }

1. Última verificação: 16-09-2022

Nós também consideramos que é melhor para a segurança das chaves privadas do provedor VPN se eles usarem [servidores dedicados](https://en.wikipedia.org/wiki/Dedicated_hosting_service), em vez de soluções compartilhadas mais baratas (com outros clientes) como [servidores virtuais privados](https://pt.wikipedia.org/wiki/Servidor_virtual_privado).

#### :material-check:{ .pg-green } Examinado por auditores externos

Mullvad's VPN clients have been audited by Cure53 and Assured AB in a pentest report [published at cure53.de](https://cure53.de/pentest-report_mullvad_v2.pdf). The security researchers concluded:

> Cure53 and Assured AB are happy with the results of the audit and the software leaves an overall positive impression. With security dedication of the in-house team at the Mullvad VPN compound, the testers have no doubts about the project being on the right track from a security standpoint.

In 2020 a second audit [was announced](https://mullvad.net/blog/2020/6/25/results-available-audit-mullvad-app/) and the [final audit report](https://cure53.de/pentest-report_mullvad_2020_v2.pdf) was made available on Cure53's website:

> The results of this May-June 2020 project targeting the Mullvad complex are quite positive. [...] The overall application ecosystem used by Mullvad leaves a sound and structured impression. The overall structure of the application makes it easy to roll out patches and fixes in a structured manner. More than anything, the findings spotted by Cure53 showcase the importance of constantly auditing and re-assessing the current leak vectors, in order to always ensure privacy of the end-users. With that being said, Mullvad does a great job protecting the end-user from common PII leaks and privacy related risks.

In 2021 an infrastructure audit [was announced](https://mullvad.net/en/blog/2021/1/20/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit/) and the [final audit report](https://cure53.de/pentest-report_mullvad_2021_v1.pdf) was made available on Cure53's website. Another report was commissioned [in June 2022](https://mullvad.net/en/blog/2022/6/22/vpn-server-audit-found-no-information-leakage-or-logging-of-customer-data/) and is available on [Assured's website](https://www.assured.se/publications/Assured_Mullvad_relay_server_audit_report_2022.pdf).

#### :material-check:{ .pg-green } Clientes de Código Aberto (Open-Source)

Mullvad provides the source code for their desktop and mobile clients in their [GitHub organization](https://github.com/mullvad/mullvadvpn-app).

#### :material-check:{ .pg-green } Aceita Dinheiro e Monero

Mullvad, além de aceitar cartões de crédito/débito e PayPal, aceita Bitcoin, Bitcoin Cash, **Monero** e **dinheiro / moeda local** como formas anônimas de pagamento. Eles também aceitam Swish e transferências bancárias.

#### :material-check:{ .pg-green } Suporta WireGuard

Mullvad suporta o protocolo WireGuard®. [WireGuard](https://www.wireguard.com) é um protocolo mais recente que usa criptografia de última geração [](https://www.wireguard.com/protocol/). Além disso, WireGuard pretende ser mais simples e mais eficiente.

Mullvad [recomenda](https://mullvad.net/en/help/why-wireguard/) o uso do WireGuard em seu serviço. It is the default or only protocol on Mullvad's Android, iOS, macOS, and Linux apps, but on Windows you have to [manually enable](https://mullvad.net/en/help/how-turn-wireguard-mullvad-app/) WireGuard. Mullvad also offers a WireGuard configuration generator for use with the official WireGuard [apps](https://www.wireguard.com/install/).

#### :material-check:{ .pg-green } IPv6 Support

Mullvad allows you to [access services hosted on IPv6](https://mullvad.net/en/blog/2014/9/15/ipv6-support/), as opposed to other providers which block IPv6 connections.

#### :material-alert-outline:{ .pg-orange } Encaminhamento de Porta Remoto

Mullvad previously supported port forwarding, but removed the option in [May 2023](https://mullvad.net/en/blog/2023/5/29/removing-the-support-for-forwarded-ports/). Missing this feature could negatively impact certain applications, especially peer-to-peer applications like torrent clients.

#### :material-check:{ .pg-green } Clientes Móveis

Mullvad has published [App Store](https://apps.apple.com/app/mullvad-vpn/id1488466513) and [Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn) clients, both supporting an easy-to-use interface as opposed to requiring you to manually configure your WireGuard connection. The Android client is also available on [GitHub](https://github.com/mullvad/mullvadvpn-app/releases).

#### :material-information-outline:{ .pg-blue } Funções Adicionais

Mullvad is very transparent about which nodes they [own or rent](https://mullvad.net/en/servers/). They use [ShadowSocks](https://shadowsocks.org/) in their ShadowSocks + OpenVPN configuration, making them more resistant against firewalls with [Deep Packet Inspection](https://en.wikipedia.org/wiki/Deep_packet_inspection) trying to block VPNs. Supposedly, [China has to use a different method to block ShadowSocks servers](https://github.com/net4people/bbs/issues/22). Mullvad's website is also accessible via Tor at [o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion).

## Requisitos

!!! danger

    É importante observar que o uso de um provedor de VPN não o tornará anônimo, mas lhe dará mais privacidade em determinadas situações. Uma VPN não é uma ferramenta para atividades ilegais. Não confie em uma política de "nenhum registro".

**Observe que não somos afiliados a nenhum dos provedores que recomendamos. Isso nos permite fornecer recomendações totalmente objetivas. **Em adição aos [nossos critérios básicos](about/criteria.md), desenvolvemos um conjunto claro de requisitos para qualquer provedor de VPN que deseje ser recomendado, incluindo criptografia forte, auditorias de segurança independentes, tecnologia moderna e muito mais. Sugerimos que você se familiarize com esta lista antes de escolher um provedor de VPN e faça sua própria pesquisa para garantir que o provedor de VPN escolhido seja o mais confiável possível.

### Tecnologia

Exigimos que todos os nossos provedores de VPN recomendados forneçam arquivos de configuração OpenVPN para serem usados em qualquer cliente. **Se** uma VPN fornecer seu próprio cliente personalizado, será necessário um killswitch para bloquear vazamentos de dados de rede quando desconectado.

**Mínimo Para Qualificação:**

- Suporte para protocolos fortes, como WireGuard & OpenVPN.
- Killswitch integrado aos clientes.
- Suporte a Multihop. O Multihopping é importante para manter os dados privados no caso de comprometimento de um único nó.
- Se forem fornecidos clientes VPN, eles devem ser de [código aberto](https://en.wikipedia.org/wiki/Open_source), como o software VPN que eles normalmente trazem incorporado. Acreditamos que a disponibilidade do [código-fonte](https://en.wikipedia.org/wiki/Source_code) proporciona maior transparência sobre o que o seu dispositivo está realmente fazendo.

**Melhor Caso:**

- Suporte WireGuard e OpenVPN.
- Killswitch com opções altamente configuráveis (ativar/desativar em determinadas redes, na inicialização, etc.)
- Clientes VPN fáceis de usar
- Suporta [IPv6](https://en.wikipedia.org/wiki/IPv6). Esperamos que os servidores permitam conexões de entrada via IPv6 e que você possa acessar serviços hospedados em endereços IPv6.
- O recurso de [encaminhamento remoto de portas](https://en.wikipedia.org/wiki/Port_forwarding#Remote_port_forwarding) ajuda a criar conexões ao usar o software de compartilhamento de arquivos P2P ([Peer-to-Peer](https://en.wikipedia.org/wiki/Peer-to-peer)) ou ao hospedar um servidor (por exemplo, Mumble).

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

Embora não sejam requisitos estritos, há alguns fatores que consideramos ao determinar quais provedores recomendar. Isso inclui a funcionalidade de bloqueio de anúncios/rastreadores, canários de garantia, conexões multihop, excelente suporte ao cliente, o número de conexões simultâneas permitidas, etc.
