---
meta_title: "Web Browsers para PC e Mac que respeitam a privacidade - Privacy Guides"
title: "Browsers para Desktop"
icon: material/laptop
description: Estes browsers protegem muito mais a sua privacidade do que o Google Chrome.
cover: desktop-browsers.png
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Recomendações de browsers privados para Desktop
    url: "./"
    relatedLink: "../mobile-browsers/"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Mullvad Browser
    image: /assets/img/browsers/mullvad_browser.svg
    url: https://mullvad.net/en/browser
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Firefox
    image: /assets/img/browsers/firefox.svg
    url: https://firefox.com
    sameAs: https://pt.wikipedia.org/wiki/Firefox
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Bromite
    image: /assets/img/browsers/brave.svg
    url: https://brave.com
    sameAs: https://pt.wikipedia.org/wiki/Brave_(web_browser)
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
---

De momento, são estes os browsers para desktop e estas as configurações para uma navegação standard/não-anónima que recomendamos. Recomendamos o [Mullvad Browser](#mullvad-browser) para quem pretenda fortes proteções de privacidade e ferramentas de bloqueio de impressão digital por defeito, o [Firefox](#firefox) para utilizadores casuais da internet que procurem uma boa alternativa ao Google Chrome e o [Brave](#brave) para quem necessite de compatibilidade com o Chromium.

Se precisar de navegar anonimamente na internet, deverá usar antes o [Tor](tor.md). Fazemos algumas recomendações de configuração nesta página, mas todos os browsers, com a exceção do Tor, são rastreáveis por *qualquer pessoa*, de uma maneira ou de outra.

## Mullvad Browser

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logotipo do Mullvad Browser](assets/img/browsers/mullvad_browser.svg){ align=right }
    
    O **Mullvad Browser ** é baseado no [Tor](tor.md#tor-browser), mas com as integrações da rede Tor removidas. O objetivo é beneficiar das suas tecnologias de bloqueio de impressão digital para quem utilize uma VPN. É desenvolvido pelo Projeto Tor e distribuído por [Mullvad](vpn.md#mullvad), e **não** requer a utilização da VPN do Mullvad.
    
    [:octicons-home-16: Homepage](https://mullvad.net/en/browser){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy/){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser/){ .card-link title=Documentação}
    [:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Código Fonte" }
    
    ??? - [:simple-windows11: Windows](https://mullvad.net/en/download/browser/windows)
        - [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
        - [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

Tal como o [Tor](tor.md), o Mullvad Browser foi concebido para evitar a recolha da sua impressão digital, tornando-a idêntica a todos os outros utilizadores do Mullvad Browser, e inclui configurações padrão e extensões que são configuradas automaticamente para níveis de segurança padrão: *Standard*, *Mais seguro* e *Segurança máxima*. Por esse motivo, é imperativo que não altere os ajustes dos [níveis de segurança](https://tb-manual.torproject.org/security-settings/) padrão do browser. Quaisquer modificações tornariam a sua impressão digital única, anulando o objetivo da utilização deste browser. Se pretender configurar o seu browser de uma forma mais musculada e a impressão digital não for uma preocupação para si, recomendamos o [Firefox](#firefox).

### Bloqueio de impressão digital

**Mesmo sem** utilizar uma [VPN](vpn.md), o Mullvad Browser oferece as mesmas proteções contra [scripts naive de impressão digital](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) que outros browsers privados, como o Firefox+[Arkenfox](#arkenfox-advanced) ou o [Brave](#brave). O Mullvad Browser disponibiliza estas proteções por defeito, com prejuízo de alguma flexibilidade e conveniência que outros browsers privados possam fornecer.

==Para obter a melhor proteção contra rastreamento de impressão digital, recomendamos a utilização do Mullvad Browser em conjunto **com** uma VPN==, quer seja o Mullvad ou outro fornecedor de VPN recomendado. Ao utilizar uma VPN com o Mullvad Browser, partilhará uma impressão digital e um conjunto de endereços IP com muitos outros utilizadores, fazendo com que a sua identidade se disperse na "multidão". Esta estratégia é a única forma de impedir scripts de rastreio avançados e é a mesma técnica de bloqueio de impressão digital utilizada pelo Tor.

Note que, embora possa utilizar o Mullvad Browser com qualquer fornecedor de VPN, é necessário que outras pessoas nessa VPN também estejam a utilizar o Mullvad Browser para que essa "multidão" exista, algo que é mais provável no Mullvad VPN do que noutros fornecedores, particularmente numa altura em que se está muito perto do lançamento do Mullvad Browser. O Mullvad Browser não tem conetividade VPN incorporada, nem verifica se se está a utilizar uma VPN; a ligação VPN tem de ser configurada e gerida separadamente.

O Mullvad Browser vem com as extensões de browser *uBlock Origin* e *NoScript* pré-instaladas. Embora normalmente [não recomendemos](#extensions) a instalação de *extensões de browser adicionais*, as extensões pré-instaladas no browser não devem **** ser removidas ou configuradas fora dos seus valores predefinidos, uma vez que isso tornaria a impressão digital do seu browser visivelmente diferente da de outros utilizadores do Mullvad Browser. A extensão de browser Mullvad vem pré-instalada, mas, se assim o desejar, *pode* ser removida com segurança sem afetar a impressão digital. No entanto, é seguro mantê-la, mesmo que não utilize o Mullvad VPN.

### Modo Privado do Browser

O Mullvad Browser funciona permanentemente em modo de navegação privada, o que significa que o seu histórico, cookies e outros dados de sites serão limpos sempre que o browser for fechado. Os seus marcadores, definições do browser e definições de extensões continuarão a ser preservados.

Este procedimento serve para evitar formas avançadas de rastreio, mas sacrifica a conveniência e perde algumas funcionalidades, como, por exemplo, os contentores para várias contas. Lembre-se que pode sempre utilizar vários browsers. Pode, por exemplo, considerar utilizar o Firefox+Arkenfox para alguns sites, nos quais pretende manter a sessão iniciada, ou que não funcionem corretamente no Mullvad Browser, e o Mullvad Browser para a navegação geral.

### Mullvad Leta

O Mullvad Browser vem com o motor de pesquisa DuckDuckGo predefinido [](search-engines.md), mas também vem pré-instalado com o **Mullvad Leta**, um motor de pesquisa que requer uma subscrição VPN Mullvad ativa para ser acedido. O Mullvad Leta consulta diretamente a API de pesquisa paga do Google (razão pela qual está limitado a subscritores pagantes). No entanto, devido a essa limitação, é possível ao Mullvad correlacionar as consultas de pesquisa e as contas VPN Mullvad. Por este motivo, desaconselhamos a utilização do Mullvad Leta, apesar do Mullvad recolher muito poucas informações sobre os seus subscritores de VPN.

## Firefox

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo do Firefox](assets/img/browsers/firefox.svg){ align=right }
    
    O **Firefox** possui definições de privacidade fortes, como a [Proteção Melhorada contra Monitorização] (https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop), que pode ajudar a bloquear vários [tipos de rastreio] (https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop#w_what-enhanced-tracking-protection-blocks).
    
    [Visite bromite.org](https://www.bromite.org){ .md-button .md-button--primary } [Política de Privacidade](https://www.bromite.org/privacy){ .md-button }
    
    **Downloads***
    - [:fontawesome-brands-android: Android](https://www.bromite.org/fdroid)
    - [:fontawesome-brands-github: Fonte](https://github.com/bromite/bromite) downloads
    
        - [:simple-windows11: Windows](https://www.mozilla.org/firefox/windows)
        - [:simple-apple: macOS](https://www.mozilla.org/firefox/mac)
        - [:simple-linux: Linux](https://www.mozilla.org/firefox/linux)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

!!! warning
    O Firefox inclui no seu site um token de transferência [único](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) e utiliza a telemetria no Firefox para enviar o token. O token não é **** incluído nas versões do [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/).

### Configuração recomendada

Estas opções podem ser encontradas em :material-menu: → **Ajustes...**

#### Pesquisa

- [ ] Desmarque **Mostrar sugestões de pesquisa**

As funcionalidades de sugestão de pesquisa podem não estar disponíveis na sua região.

As sugestões de pesquisa enviam tudo o que escrever na barra de endereço para o motor de pesquisa predefinido, independentemente de efetuar uma pesquisa real. A desativação das sugestões de pesquisa permite-lhe controlar com maior precisão os dados que envia ao seu fornecedor de motores de pesquisa.

#### Privacidade & Segurança

##### Proteção melhorada contra a monitorização

- [x] Selecione **Rigorosa** Proteção mais forte

Esta proteção bloqueia rastreadores de redes sociais, scripts de impressões digitais (note que isto não o protege de *todas as impressões digitais*), criptomineradores, cookies de rastreio entre sites e alguns outros conteúdos de rastreio. A Proteção Melhorada contra a monitorização protege-o contra muitas ameaças comuns, mas não bloqueia todos os modos de rastreio, uma vez que foi concebida para ter um impacto mínimo ou nulo na usabilidade do site.

##### Firefox Suggest (apenas nos EUA)

[O Firefox Suggest](https://support.mozilla.org/en-US/kb/firefox-suggest) é uma funcionalidade semelhante às sugestões de pesquisa que só está disponível nos EUA. Recomendamos a sua desativação pelo mesmo motivo que recomendamos a desativação das sugestões de pesquisa. Se não vir essa opções no cabeçalho da **Barra de endereço**, é porque não dispõe dessa nova experiência, devendo ignorar estas alterações.

- [ ] Desmarque **Sugestões da web**
- [ ] Desmarque **Sugestões de patrocinadores**

##### Higienizar ao fechar

Se pretender manter a sessão iniciada em determinados sites, pode criar exceções em **Cookies e dados de sites** → **Gerir exceções...**

- [x] Selecione **Eliminar cookies e os dados de sites quando o Firefox é fechado**

Esta ação protege-o dos cookies persistentes, mas não o protege dos cookies adquiridos durante uma sessão de navegação. Quando esta opção está ativada, é possível limpar facilmente os cookies do seu browser, bastando reiniciar o Firefox. Pode definir exceções por site, se pretender manter a sessão iniciada num determinado site que visita frequentemente.

##### Recolha de dados e utilização do Firefox

- [ ] Desmarque **Permitir que o Firefox envie dados técnicos e de interação para o Mozilla**
- [ ] Desmarque **Permitir ao Firefox instalar e executar estudos**
- [ ] Desmarque **Permitir que o Firefox envie relatórios de falhas acumuladas em seu nome**

> O Firefox envia-nos dados sobre a sua versão e idioma do Firefox; sistema operativo e configuração de hardware do dispositivo; memória, informações básicas sobre falhas e erros; resultado de processos automatizados como atualizações, navegação segura e ativação. Quando o Firefox nos envia dados, o seu endereço IP é temporariamente recolhido como parte dos registos do nosso servidor.

Além disso, o serviço de contas Firefox recolhe [alguns dados técnicos](https://www.mozilla.org/en-US/privacy/firefox/#firefox-accounts). Se utilizar uma conta Firefox, pode optar por não participar:

1. Abra as definições do seu perfil [em accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Desmarque **Recolha e utilização de dados** > **Ajudar a melhorar as contas Firefox**

##### Modo apenas HTTPS

- [x] Selecione **Ativar o modo apenas HTTPS em todas as janelas**

Esta opção impede-o de se ligar involuntariamente a um site em texto simples HTTP. Os sites sem HTTPS são raros hoje em dia, pelo que esta opção deverá ter pouco ou nenhum impacto na sua navegação quotidiana.

#### Sincronizar

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy/) permite que os seus dados de navegação (histórico, marcadores, etc.) estejam acessíveis em todos os seus dispositivos e protege-os com E2EE.

### Arkenfox (avançado)

!!! dica "Utilize o Mullvad Browser para bloqueio de impressão digital avançado"

    O [Mullvad Browser](#mullvad-browser) fornece as mesmas proteções de bloqueio de impressão digital que o Arkenfox, e não requer a utilização da VPN do Mullvad para o efeito. Juntamente com uma VPN, o Mullvad Browser pode impedir scripts de rastreio mais avançados, algo que o Arkenfox não consegue. O Arkenfox tem a vantagem de ser muito mais flexível e de permitir exceções por site, nos casos em que é necessário manter a sessão iniciada.

O projeto [Arkenfox](https://github.com/arkenfox/user.js) fornece um conjunto de opções cuidadosamente escolhidas para o Firefox. Se [decidir](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) utilizar o Arkenfox, algumas [opções](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) são subjetivamente restritivas e/ou podem fazer com que alguns sites não funcionem corretamente - [algo que pode facilmente alterar](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) de forma a satisfazer as suas necessidades. Recomendamos vivamente a **** a leitura integral da sua [wiki](https://github.com/arkenfox/user.js/wiki). O Arkenfox também ativa o suporte de contentor [](https://support.mozilla.org/en-US/kb/containers#w_for-advanced-users).

O Arkenfox apenas pretende impedir scripts de rastreio básicos ou naive, através da aleatorização do ecrã e das definições de configuração de resistência à impressão digital incorporadas no Firefox. Não tem como objetivo fazer com que o seu browser se misture com uma grande multidão de outros utilizadores do Arkenfox, como o Mullvad Browser ou o Tor, e que é a única forma de impedir scripts avançados de rastreio de impressões digitais. Lembre-se que pode sempre utilizar vários browsers. Pode, por exemplo, utilizar o Firefox+Arkenfox para alguns sites em que pretende manter a sessão iniciada ou em que confia, e o Mullvad Browser para navegação geral.

## Brave

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo Brave](assets/img/browsers/brave.svg){ align=right }
    
    O **Brave** inclui um bloqueador de conteúdos incorporado e [funcionalidades de privacidade] (https://brave.com/privacy-features/), muitas das quais estão ativadas por predefinição.
    
    O Brave foi desenvolvido com base no projeto do Chromium, pelo que deve ser familiar a muitos utilizadores e não deverá ter grandes problemas de compatibilidade com sites.
    
    [:octicons-home-16: Homepage](https://brave.com/){ .md-button .md-button--primary }
    [:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Serviço Onion" }
    [:octicons-eye-16:](https://brave.com/privacy/browser/){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://support.brave.com/){ .card-link title=Documentação}
    [:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Código Fonte" }
    
    ??? downloads anotar
    
        - [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
        - [:simple-windows11: Windows](https://brave.com/download/)
        - [:simple-apple: macOS](https://brave.com/download/)
        - [:simple-linux: Linux](https://brave.com/linux/) (1)

    1. Aconselhamos a não utilização da versão Flatpak do Brave, uma vez que substitui a sandbox do Chromium pela do Flatpak, que é menos eficaz. Para além disso, o pacote de software não é mantido pela Brave Software, Inc.

### Configuração recomendada

Estas opções podem ser encontradas em :material-menu: → **Definições...**.

#### Definições

##### Proteções

O Brave inclui algumas medidas de bloqueio de impressão digital nas suas [Proteções](https://support.brave.com/hc/en-us/articles/360022973471-What-is-Shields-). Sugerimos que configure estas opções [globalmente](https://support.brave.com/hc/en-us/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings-) em todas as páginas que visitar.

As opções de proteção podem ser revogadas por cada site, de acordo com as necessidades, mas por predefinição recomendamos as seguintes definições:

<div class="annotate" markdown>

- [x] Selecione **Impedir que sites criem impressões digitais minhas, com base nas minhas preferências de idioma**
- [x] Selecione **Agressivo** em Rastreadores e bloqueio de anúncios

??? aviso "Use listas de filtro padrão"
        O Brave permite-lhe selecionar filtros de conteúdo adicional na página interna `brave://adblock`. Aconselhamos a não utilizar esta funcionalidade; em vez disso, mantenha as listas de filtros predefinidas. A utilização de listas extra fará com que se destaque dos outros utilizadores do Brave e pode também aumentar a superfície de ataque se houver uma vulnerabilidade no Brave e uma regra maliciosa for adicionada a uma das listas que utiliza.

- [x] (Opcional) Selecionar **Bloquear scripts** (1)
- [x] na opção Bloquear impressão digital, selecionar **Estrito, pode causar problemas nos sites**

</div>

1. Esta opção disponibiliza uma funcionalidade semelhante aos modos de bloqueio avançados do uBlock Origin [](https://github.com/gorhill/uBlock/wiki/Blocking-mode) ou à extensão [NoScript](https://noscript.net/).

##### Bloqueio das redes sociais

- [ ] Desative todos os componentes de redes sociais

##### Privacidade e segurança

<div class="annotate" markdown>

- [x] Selecione **Desativar UDP não-proxy**, em [Política de utilização WebRTC IP](https://support.brave.com/hc/en-us/articles/360017989132-How-do-I-change-my-Privacy-Settings-#webrtc)
- [ ] Desative **Utilizar Google services para notificações push**
- [ ] Desative **Permitir análises de produtos que preservam a privacidade (P3A)**
- [ ] Desative **Enviar automaticamente ping de utilização diária para a Brave**
- [ ] Desative **Enviar relatórios de diagnóstico automaticamente**
- [x] Selecione **Usar o DNS** no menu **Segurança**, na opção Avançadas
- [ ] Desative **Janelas em modo privado com Tor** (1), em Janelas Tor

    !!! dica "Higienizar ao fechar"

        - [x] Selecione **Limpar cookies e dados do site ao fechar todas as janelas** no menu *Cookies e outros dados do site*

        Se pretender manter a sessão iniciada num determinado site que visita frequentemente, pode definir excepções por site na secção *Comportamentos personalizados*.

</div>

1. O Brave **não é** tão resistente à recolha de impressões digitais como o Tor e muito menos pessoas utilizam o Brave com o Tor, pelo que a sua presença se destacará. Quando [é necessário um forte anonimato](https://support.brave.com/hc/en-us/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity-), utilize o navegador Tor [](tor.md#tor-browser).

##### Extensões

Desative as extensões incluídas que não utilizar em **Extensões**

- [ ] Desmarque **Hangouts**
- [ ] Desmarque **WebTorrent**

##### Web3

As funcionalidades Web3 do Brave podem potencialmente aumentar a impressão digital do seu browser e a superfície de ataque. A menos que utilize alguma destas funcionalidades, desative-as.

Defina **Carteira Ethereum predefinida** para **Extensões (sem cópia de segurança)** Defina **Carteira Solana predefinida** para **Extensões (sem cópia de segurança)** Defina **Método para solucionar métodos IPFS** para **Desativada**

##### Sistema

<div class="annotate" markdown>

- [ ] Desmarque a opção **Continuar a executar aplicações quando o Brave é fechado** para desativar as aplicações em segundo plano (1)

</div>

1. Esta opção não está presente em todas as plataformas.

#### Sincronização

[A Sincronização do Brave](https://support.brave.com/hc/en-us/articles/360059793111-Understanding-Brave-Sync) permite que os seus dados de navegação (histórico, marcadores, etc.) estejam acessíveis em todos os seus dispositivos, sem necessidade de uma conta, e protege-os com E2EE.

#### Recompensar Brave

**Recompensas Brave** permite-lhe receber criptomoeda Basic Attention Token (BAT) pelo facto de realizar determinadas ações. Baseia-se numa conta de custódia e no KYC de um número selecionado de fornecedores. Não recomendamos a BAT como uma criptomoeda privada [](cryptocurrency.md), nem recomendamos a utilização de uma carteira de custódia [](advanced/payments.md#other-coins-bitcoin-ethereum-etc), pelo que desencorajamos a utilização desta funcionalidade.

**A Brave Wallet** funciona localmente no seu computador, mas não suporta quaisquer criptomoedas privadas, pelo que desencorajamos a utilização desta funcionalidade também.

## Recursos Adicionais

Em geral, recomendamos que a utilização de extensões seja reduzida ao mínimo; têm acesso privilegiado no seu browser, exigem que confie no programador, podem fazer com que se [destaque](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)e [enfraquecem](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ) o isolamento do site. No entanto, o uBlock Origin pode ser útil se valorizar a funcionalidade de bloqueio de conteúdos.

### uBlock Origin

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![logótipo uBlock Origin](assets/img/browsers/ublock_origin.svg){ align=right }
    
    O **uBlock Origin** é um popular bloqueador de conteúdos que pode ajudá-lo a bloquear anúncios, rastreadores e scripts de impressões digitais.
    
    [:octicons-repo-16: Repositório](https://github.com/gorhill/uBlock#readme){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://github.com/gorhill/uBlock/wiki/Privacy-policy){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://github.com/gorhill/uBlock/wiki){ .card-link title=Documentação}
    [:octicons-code-16:](https://github.com/gorhill/uBlock){ .card-link title="Código-fonte" }
    
    ??? downloads
    
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/ublock-origin/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm)
        - [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/ublock-origin/odfafepnkmbhccpbejgmiehpchacaeak)

Sugerimos que siga as instruções da documentação do programador [](https://github.com/gorhill/uBlock/wiki/Blocking-mode) e escolha um dos "modos". Listas de filtros adicionais podem afetar o desempenho e [podem aumentar a superfície de ataque](https://portswigger.net/research/ublock-i-exfiltrate-exploiting-ad-blockers-with-css).

##### Outras listas

Estas são algumas [listas de filtros](https://github.com/gorhill/uBlock/wiki/Dashboard:-Filter-lists) que pode querer considerar adicionar:

- [x] Selecione **Privacidade** > **Proteção de rastreio de URL do AdGuard**
- Adicionar [Ferramenta de encurtamento de URL realmente legítima](https://raw.githubusercontent.com/DandelionSprout/adfilt/master/LegitimateURLShortener.txt)

## Critérios

**Note que não estamos associados a nenhum dos projetos que recomendamos.** Para além dos [nossos critérios padrão](about/criteria.md), temos um conjunto claro de requisitos que nos permitem fornecer recomendações objetivas. Sugerimos que se familiarize com esta lista antes de optar por um projeto e que desenvolva a sua própria investigação para garantir que se trata da escolha certa para si.

!!! exemplo "Esta secção é nova"

    Estamos a trabalhar no sentido de estabelecer critérios para cada secção do nosso site, o que pode originar alterações. Se tiver alguma dúvida sobre os critérios utilizados, por favor [pergunte no nosso fórum] (https://discuss.privacyguides.net/latest) e não parta do princípio de que algo foi excluído das nossas recomendações, caso não esteja listado aqui. São muitos os fatores considerados e discutidos quando recomendamos um projeto, e documentar cada um deles é um trabalho em curso.

### Requisitos mínimos

- Software de código aberto.
- Atualizações automáticas.
- Atualizações do motor em 0-1 dias a partir do lançamento upstream.
- Disponível em Linux, macOS e Windows.
- Alterações necessárias para tornar o browser mais respeitador da privacidade não devem afetar negativamente a experiência do utilizador.
- Bloqueio de cookies de terceiros por defeito.
- [Particionamento de estado](https://developer.mozilla.org/en-US/docs/Web/Privacy/State_Partitioning) para mitigar o rastreio entre sítios.[^1]

### Melhor caso

Estes são os critérios que consideramos essenciais para um projeto perfeito nesta categoria. As nossas recomendações podem não incluir todas as funcionalidades, mas incluem as que, na nossa opinião, têm um impacto mais elevado.

- Inclui a funcionalidade de bloqueio de conteúdos incorporada.
- Suporta a compartimentação de cookies (à la [Multi-Account Containers](https://support.mozilla.org/en-US/kb/containers)).
- Suporta Progressive Web Apps.  
  Os PWAs permitem-lhe instalar determinados sites como se fossem aplicações nativas no seu computador. Isto pode ter vantagens sobre a instalação de aplicações baseadas no Electron, uma vez que beneficia das atualizações de segurança regulares do seu browser.
- Não inclui funcionalidades adicionais (bloatware) que não afetam a privacidade do utilizador.
- Não recolhe telemetria por predefinição.
- Fornece implementação de código aberto de sincronização de servidor.
- Tem predefinido um motor de busca privado [](search-engines.md).

### Critérios de extensão

- Não deve replicar a funcionalidade incorporada do browser ou do sistema operativo.
- Deve ter um impacto direto na privacidade do utilizador, ou seja, não deve limitar-se a fornecer informações.

[^1]: A implementação do Brave é pormenorizada em [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state/).
