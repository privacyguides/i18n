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

!!! aviso
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
        O Brave permite-lhe selecionar filtros de conteúdo adicional na página interna `brave://adblock`. Aconselhamos a não utilizar esta funcionalidade; em vez disso, mantenha as listas de filtros predefinidas. A utilização de listas extra fará com que se destaque dos outros utilizadores do Brave e pode também aumentar a superfície de ataque se houver uma exploração no Brave e uma regra maliciosa for adicionada a uma das listas que utiliza.

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

1. Brave is **not** as resistant to fingerprinting as the Tor Browser and far fewer people use Brave with Tor, so you will stand out. Where [strong anonymity is required](https://support.brave.com/hc/en-us/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity-) use the [Tor Browser](tor.md#tor-browser).

##### Extensões

Disable built-in extensions you do not use in **Extensions**

- [ ] Uncheck **Hangouts**
- [ ] Uncheck **WebTorrent**

##### Web3

Brave's Web3 features can potentially add to your browser fingerprint and attack surface. Unless you use any of features, they should be disabled.

Set **Default Ethereum wallet** to **Extensions (no fallback)** Set **Default Solana wallet** to **Extensions (no fallback)** Set **Method to resolve IPFS resources** to **Disabled**

##### System

<div class="annotate" markdown>

- [ ] Uncheck **Continue running apps when Brave is closed** to disable background apps (1)

</div>

1. This option is not present on all platforms.

#### Sincronizar

[Brave Sync](https://support.brave.com/hc/en-us/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

#### Brave Rewards and Wallet

**Brave Rewards** lets you recieve Basic Attention Token (BAT) cryptocurrency for performing certain actions within Brave. It relies on a custodial account and KYC from a select number of providers. We do not recommend BAT as a [private cryptocurrency](cryptocurrency.md), nor do we recommend using a [custodial wallet](advanced/payments.md#other-coins-bitcoin-ethereum-etc), so we would discourage using this feature.

**Brave Wallet** operates locally on your computer, but does not support any private cryptocurrencies, so we would discourage using this feature as well.

## Recursos Adicionais

In general, we recommend keeping your browser extensions to a minimum to decrease your attack surface; they have privileged access within your browser, require you to trust the developer, can make you [stand out](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint), and [weaken](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ) site isolation. However, uBlock Origin may prove useful if you value content blocking functionality.

### AdGuard para Safari

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    Não recomendamos a instalação do ToS;DR como uma extensão do navegador.
    
    A mesma informação é fornecida no site deles. downloads
    
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/ublock-origin/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm)
        - [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/ublock-origin/odfafepnkmbhccpbejgmiehpchacaeak)

We suggest following the [developer's documentation](https://github.com/gorhill/uBlock/wiki/Blocking-mode) and picking one of the "modes". Additional filter lists can impact performance and [may increase attack surface](https://portswigger.net/research/ublock-i-exfiltrate-exploiting-ad-blockers-with-css).

##### Other lists

These are some other [filter lists](https://github.com/gorhill/uBlock/wiki/Dashboard:-Filter-lists) that you may want to consider adding:

- [x] Check **Privacy** > **AdGuard URL Tracking Protection**
- Add [Actually Legitimate URL Shortener Tool](https://raw.githubusercontent.com/DandelionSprout/adfilt/master/LegitimateURLShortener.txt)

## Framadate

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

!!! Considere o auto-hospedagem para mitigar esta ameaça.

    ![logo PrivateBin](/assets/img/productivity/privatebin.svg){ align=right }
    
    **PrivateBin** é um pastebin online minimalista e de código aberto onde o servidor tem zero conhecimento de dados colados. Os dados são criptografados/descriptografados no navegador usando AES de 256 bits. Psono suporta compartilhamento seguro de senhas, arquivos, marcadores e e-mails.

### Minimum Requirements

- Must be open-source software.
- Supports automatic updates.
- Receives engine updates in 0-1 days from upstream release.
- Available on Linux, macOS, and Windows.
- Any changes required to make the browser more privacy-respecting should not negatively impact user experience.
- Blocks third-party cookies by default.
- Supports [state partitioning](https://developer.mozilla.org/en-US/docs/Web/Privacy/State_Partitioning) to mitigate cross-site tracking.[^1]

### Best-Case

Our best-case criteria represents what we would like to see from the perfect project in this category. Our recommendations may not include any or all of this functionality, but those which do may rank higher than others on this page.

- Includes built-in content blocking functionality.
- Supports cookie compartmentalization (à la [Multi-Account Containers](https://support.mozilla.org/en-US/kb/containers)).
- Supports Progressive Web Apps.  
  PWAs enable you to install certain websites as if they were native apps on your computer. This can have advantages over installing Electron-based apps, because you benefit from your browser's regular security updates.
- Does not include add-on functionality (bloatware) that does not impact user privacy.
- Does not collect telemetry by default.
- Provides open-source sync server implementation.
- Defaults to a [private search engine](search-engines.md).

### Extension Criteria

- Must not replicate built-in browser or OS functionality.
- Must directly impact user privacy, i.e. must not simply provide information.

[^1]: Brave's implementation is detailed at [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state/).
