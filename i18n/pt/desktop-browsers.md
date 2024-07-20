---
meta_title: "Web Browsers para PC e Mac que respeitam a privacidade - Privacy Guides"
title: "Browsers para Desktop"
icon: material/laptop
description: Estes browsers protegem muito mais a sua privacidade do que o Google Chrome.
cover: desktop-browsers.webp
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

<div class="admonition recommendation" markdown>

![Logotipo do Mullvad Browser](assets/img/browsers/mullvad_browser.svg){ align=right }

O **Mullvad Browser ** é baseado no [Tor](tor.md#tor-browser), mas com as integrações da rede Tor removidas. O objetivo é beneficiar das suas tecnologias de bloqueio de impressão digital para quem utilize uma VPN. É desenvolvido pelo Projeto Tor e distribuído por [Mullvad](vpn.md#mullvad), e **não** requer a utilização da VPN do Mullvad.

[:octicons-home-16: Homepage](https://mullvad.net/en/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://mullvad.net/en/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

</details>

</div>

Tal como o [Tor](tor.md), o Mullvad Browser foi concebido para evitar a recolha da sua impressão digital, tornando-a idêntica a todos os outros utilizadores do Mullvad Browser, e inclui configurações padrão e extensões que são configuradas automaticamente para níveis de segurança padrão: *Standard*, *Mais seguro* e *Segurança máxima*. Therefore, it is imperative that you do not modify the browser at all outside adjusting the default [security levels](https://tb-manual.torproject.org/security-settings). Quaisquer modificações tornariam a sua impressão digital única, anulando o objetivo da utilização deste browser. Se pretender configurar o seu browser de uma forma mais musculada e a impressão digital não for uma preocupação para si, recomendamos o [Firefox](#firefox).

### Bloqueio de impressão digital

**Mesmo sem** utilizar uma [VPN](vpn.md), o Mullvad Browser oferece as mesmas proteções contra [scripts naive de impressão digital](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) que outros browsers privados, como o Firefox+[Arkenfox](#arkenfox-advanced) ou o [Brave](#brave). O Mullvad Browser disponibiliza estas proteções por defeito, com prejuízo de alguma flexibilidade e conveniência que outros browsers privados possam fornecer.

==Para obter a melhor proteção contra rastreamento de impressão digital, recomendamos a utilização do Mullvad Browser em conjunto **com** uma VPN==, quer seja o Mullvad ou outro fornecedor de VPN recomendado. Ao utilizar uma VPN com o Mullvad Browser, partilhará uma impressão digital e um conjunto de endereços IP com muitos outros utilizadores, fazendo com que a sua identidade se disperse na "multidão". Esta estratégia é a única forma de impedir scripts de rastreio avançados e é a mesma técnica de bloqueio de impressão digital utilizada pelo Tor.

Note que, embora possa utilizar o Mullvad Browser com qualquer fornecedor de VPN, é necessário que outras pessoas nessa VPN também estejam a utilizar o Mullvad Browser para que essa "multidão" exista, algo que é mais provável no Mullvad VPN do que noutros fornecedores, particularmente numa altura em que se está muito perto do lançamento do Mullvad Browser. O Mullvad Browser não tem conetividade VPN incorporada, nem verifica se se está a utilizar uma VPN; a ligação VPN tem de ser configurada e gerida separadamente.

O Mullvad Browser vem com as extensões de browser *uBlock Origin* e *NoScript* pré-instaladas. While we typically discourage adding *additional* [browser extensions](browser-extensions.md), these extensions that come pre-installed with the browser should **not** be removed or configured outside their default values, because doing so would noticeably make your browser fingerprint distinct from other Mullvad Browser users. A extensão de browser Mullvad vem pré-instalada, mas, se assim o desejar, *pode* ser removida com segurança sem afetar a impressão digital. No entanto, é seguro mantê-la, mesmo que não utilize o Mullvad VPN.

### Modo Privado do Browser

O Mullvad Browser funciona permanentemente em modo de navegação privada, o que significa que o seu histórico, cookies e outros dados de sites serão limpos sempre que o browser for fechado. Os seus marcadores, definições do browser e definições de extensões continuarão a ser preservados.

Este procedimento serve para evitar formas avançadas de rastreio, mas sacrifica a conveniência e perde algumas funcionalidades, como, por exemplo, os contentores para várias contas. Lembre-se que pode sempre utilizar vários browsers. Pode, por exemplo, considerar utilizar o Firefox+Arkenfox para alguns sites, nos quais pretende manter a sessão iniciada, ou que não funcionem corretamente no Mullvad Browser, e o Mullvad Browser para a navegação geral.

### Mullvad Leta

O Mullvad Browser vem com o motor de pesquisa DuckDuckGo predefinido [](search-engines.md), mas também vem pré-instalado com o **Mullvad Leta**, um motor de pesquisa que requer uma subscrição VPN Mullvad ativa para ser acedido. Mullvad Leta queries Google's paid search API directly, which is why it is limited to paying subscribers. However, it is possible for Mullvad to correlate search queries and Mullvad VPN accounts because of this limitation. Por este motivo, desaconselhamos a utilização do Mullvad Leta, apesar do Mullvad recolher muito poucas informações sobre os seus subscritores de VPN.

## Firefox

<div class="admonition recommendation" markdown>

![Logótipo do Firefox](assets/img/browsers/firefox.svg){ align=right }

O **Firefox** possui definições de privacidade fortes, como a [Proteção Melhorada contra Monitorização] (https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop), que pode ajudar a bloquear vários [tipos de rastreio] (https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop#w_what-enhanced-tracking-protection-blocks).

[:octicons-home-16: Homepage](https://firefox.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/firefox){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.mozilla.org/products/firefox){ .card-link title=Documentation}
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.mozilla.org){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://mozilla.org/firefox/windows)
- [:simple-apple: macOS](https://mozilla.org/firefox/mac)
- [:simple-linux: Linux](https://mozilla.org/firefox/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Aviso</p>

Firefox includes a unique [download token](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) in downloads from Mozilla's website and uses telemetry in Firefox to send the token. The token is **not** included in releases from the [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/).

</div>

### Recommended Firefox Configuration

Estas opções podem ser encontradas em :material-menu: → **Definições...**.

#### Pesquisa

- [ ] Uncheck **Show search suggestions**

As funcionalidades de sugestão de pesquisa podem não estar disponíveis na sua região.

As sugestões de pesquisa enviam tudo o que escrever na barra de endereço para o motor de pesquisa predefinido, independentemente de efetuar uma pesquisa real. A desativação das sugestões de pesquisa permite-lhe controlar com maior precisão os dados que envia ao seu fornecedor de motores de pesquisa.

##### Firefox Suggest (apenas nos EUA)

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) is a feature similar to search suggestions which is only available in the US. Recomendamos a sua desativação pelo mesmo motivo que recomendamos a desativação das sugestões de pesquisa. Se não vir essa opções no cabeçalho da **Barra de endereço**, é porque não dispõe dessa nova experiência, devendo ignorar estas alterações.

- [ ] Uncheck **Suggestions from Firefox**
- [ ] Desmarque **Sugestões de patrocinadores**

#### Privacidade & Segurança

##### Proteção melhorada contra a monitorização

- [x] Selecione **Rigorosa** Proteção mais forte

Esta proteção bloqueia rastreadores de redes sociais, scripts de impressões digitais (note que isto não o protege de *todas as impressões digitais*), criptomineradores, cookies de rastreio entre sites e alguns outros conteúdos de rastreio. A Proteção Melhorada contra a monitorização protege-o contra muitas ameaças comuns, mas não bloqueia todos os modos de rastreio, uma vez que foi concebida para ter um impacto mínimo ou nulo na usabilidade do site.

##### Higienizar ao fechar

Se pretender manter a sessão iniciada em determinados sites, pode criar exceções em **Cookies e dados de sites** → **Gerir exceções...**

- [x] Selecione **Eliminar cookies e os dados de sites quando o Firefox é fechado**

Esta ação protege-o dos cookies persistentes, mas não o protege dos cookies adquiridos durante uma sessão de navegação. Quando esta opção está ativada, é possível limpar facilmente os cookies do seu browser, bastando reiniciar o Firefox. Pode definir exceções por site, se pretender manter a sessão iniciada num determinado site que visita frequentemente.

##### Recolha de dados e utilização do Firefox

- [ ] Desmarque **Permitir que o Firefox envie dados técnicos e de interação para o Mozilla**
- [ ] Desmarque **Permitir ao Firefox instalar e executar estudos**
- [ ] Desmarque **Permitir que o Firefox envie relatórios de falhas acumuladas em seu nome**

> O Firefox envia-nos dados sobre a sua versão e idioma do Firefox; sistema operativo e configuração de hardware do dispositivo; memória, informações básicas sobre falhas e erros; resultado de processos automatizados como atualizações, navegação segura e ativação. Quando o Firefox nos envia dados, o seu endereço IP é temporariamente recolhido como parte dos registos do nosso servidor.

Additionally, the Mozilla Accounts service collects [some technical data](https://mozilla.org/privacy/mozilla-accounts). If you use a Mozilla Account you can opt-out:

1. Abra as definições do seu perfil [em accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Desmarque **Recolha e utilização de dados** > **Ajudar a melhorar as contas Firefox**

##### Website Advertising Preferences

- [ ] Uncheck **Allow websites to perform privacy-preserving ad measurement**

With the release of Firefox 128, a new setting for [privacy-preserving attribution](https://support.mozilla.org/kb/privacy-preserving-attribution) (PPA) has been added and [enabled by default](https://blog.privacyguides.org/2024/07/14/mozilla-disappoints-us-yet-again-2). PPA allows advertisers to use your web browser to measure the effectiveness of web campaigns, instead of using traditional JavaScript-based tracking. We consider this behavior to be outside the scope of a user agent's responsibilities, and the fact that it is disabled by default in Arkenfox is an additional indicator for disabling this feature.

##### HTTPS-Only Mode

- [x] Selecione **Ativar o modo apenas HTTPS em todas as janelas**

Esta opção impede-o de se ligar involuntariamente a um site em texto simples HTTP. Os sites sem HTTPS são raros hoje em dia, pelo que esta opção deverá ter pouco ou nenhum impacto na sua navegação quotidiana.

##### DNS sobre HTTPS

If you use a [DNS over HTTPS provider](dns.md):

- [x] Select **Max Protection** and choose a suitable provider

Max Protection enforces the use of DNS over HTTPS, and a security warning will show if Firefox can’t connect to your secure DNS resolver, or if your secure DNS resolver says that records for the domain you are trying to access do not exist. This stops the network you're connected to from secretly downgrading your DNS security.

#### Sync

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices and protects it with E2EE.

### Arkenfox (avançado)

<div class="admonition tip" markdown>
<p class="admonition-title">Usa o Mullvad Browser para Bloqueio de Impressão Digital Avançado</p>

O [Mullvad Browser](#mullvad-browser) fornece as mesmas proteções de bloqueio de impressão digital que o Arkenfox, e não requer a utilização da VPN do Mullvad para o efeito. Juntamente com uma VPN, o Mullvad Browser pode impedir scripts de rastreio mais avançados, algo que o Arkenfox não consegue. O Arkenfox tem a vantagem de ser muito mais flexível e de permitir exceções por site, nos casos em que é necessário manter a sessão iniciada.

</div>

O projeto [Arkenfox](https://github.com/arkenfox/user.js) fornece um conjunto de opções cuidadosamente escolhidas para o Firefox. If you [decide](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) to use Arkenfox, a [few options](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) are subjectively strict and/or may cause some websites to not work properly—which you can [easily change](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) to suit your needs. Recomendamos vivamente a **** a leitura integral da sua [wiki](https://github.com/arkenfox/user.js/wiki). Arkenfox also enables [container](https://support.mozilla.org/kb/containers#w_for-advanced-users) support.

O Arkenfox apenas pretende impedir scripts de rastreio básicos ou naive, através da aleatorização do ecrã e das definições de configuração de resistência à impressão digital incorporadas no Firefox. Não tem como objetivo fazer com que o seu browser se misture com uma grande multidão de outros utilizadores do Arkenfox, como o Mullvad Browser ou o Tor, e que é a única forma de impedir scripts avançados de rastreio de impressões digitais. Lembre-se que pode sempre utilizar vários browsers. Pode, por exemplo, utilizar o Firefox+Arkenfox para alguns sites em que pretende manter a sessão iniciada ou em que confia, e o Mullvad Browser para navegação geral.

## Brave

<div class="admonition recommendation annotate" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** includes a built-in content blocker and [privacy features](https://brave.com/privacy-features), many of which are enabled by default.

O Brave foi desenvolvido com base no projeto do Chromium, pelo que deve ser familiar a muitos utilizadores e não deverá ter grandes problemas de compatibilidade com sites.

[:octicons-home-16: Homepage](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.brave.com){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:fontawesome-brands-windows: Windows](https://brave.com/download)
- [:simple-apple: macOS](https://brave.com/download)
- [:simple-linux: Linux](https://brave.com/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/com.brave.Browser)

</details>

</div>

**macOS users:** The download for Brave Browser from their official website is a `.pkg` installer which requires admin privileges to run (and may run other unnecessary scripts on your machine). As an alternative, you can download the latest `Brave-Browser-universal.dmg` file from their [GitHub releases](https://github.com/brave/brave-browser/releases/latest) page, which provides a traditional "drag to Applications folder" install.

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

Brave adds a "[referral code](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)" to the file name in downloads from the Brave website, which is used to track which source the browser was downloaded from, for example `BRV002` in a download named `Brave-Browser-BRV002.pkg`. The installer will then ping Brave's server with the referral code at the end of the installation process. If you're concerned about this, you can rename the installer file before opening it.

</div>

### Recommended Brave Configuration

Estas opções podem ser encontradas em :material-menu: → **Definições...**.

#### Settings

##### Proteções

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) feature. We suggest configuring these options [globally](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) across all pages that you visit.

As opções de proteção podem ser revogadas por cada site, de acordo com as necessidades, mas por predefinição recomendamos as seguintes definições:

<div class="annotate" markdown>

- [x] Select **Prevent sites from fingerprinting me based on my language preferences**
- [x] Select **Aggressive** under *Trackers & ads blocking*

<details class="warning" markdown>
<summary>Use default filter lists</summary>

Brave allows you to select additional content filters within the internal `brave://adblock` page. Aconselhamos a não utilizar esta funcionalidade; em vez disso, mantenha as listas de filtros predefinidas. A utilização de listas extra fará com que se destaque dos outros utilizadores do Brave e pode também aumentar a superfície de ataque se houver uma vulnerabilidade no Brave e uma regra maliciosa for adicionada a uma das listas que utiliza.

</details>

- [x] Select **Strict** under *Upgrade connections to HTTPS*
- [x] (Optional) Select **Block Scripts** (1)
- [x] Check **Block fingerprinting**
- [x] Check **Forget me when I close this site** (2)
- [ ] Uncheck all social media components

</div>

1. This option provides functionality similar to uBlock Origin's advanced [blocking modes](https://github.com/gorhill/uBlock/wiki/Blocking-mode).
2. If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis by clicking on the Shield icon in the address bar.

##### Privacy and security

<div class="annotate" markdown>

- [x] Select **Disable non-proxied UDP** under [WebRTC IP Handling Policy](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Uncheck **Use Google services for push messaging**
- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send daily usage ping to Brave**
- [ ] Uncheck **Automatically send diagnostic reports**
- [ ] Uncheck **Private window with Tor** (1)

</div>

1. O Brave **não é** tão resistente à recolha de impressões digitais como o Tor e muito menos pessoas utilizam o Brave com o Tor, pelo que a sua presença se destacará. Where [strong anonymity is required](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity) use the [Tor Browser](tor.md#tor-browser).

<div class="admonition tip" markdown>
<p class="admonition-title">Sanitizing on close</p>

- [x] In the *Sites and Shields Settings* menu, under Content, after clicking on the *On-device site data* menu, select **Delete data sites have saved to your device when you close all windows**.

If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis under the *Customized behaviors* section.

</div>

##### Extensions

- [ ] Uncheck all built-in extensions you do not use

##### Web3

As funcionalidades Web3 do Brave podem potencialmente aumentar a impressão digital do seu browser e a superfície de ataque. A menos que utilize alguma destas funcionalidades, desative-as.

- Select **Extensions (no fallback)** under *Default Ethereum wallet* and *Default Solana wallet*
- Set *Method to resolve IPFS resources* to **Disabled**

##### System

<div class="annotate" markdown>

- [ ] Desmarque a opção **Continuar a executar aplicações quando o Brave é fechado** para desativar as aplicações em segundo plano (1)

</div>

1. Esta opção não está presente em todas as plataformas.

#### Sincronização do Brave

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

#### Brave Rewards and Wallet

**Brave Rewards** lets you receive Basic Attention Token (BAT) cryptocurrency for performing certain actions within Brave. Baseia-se numa conta de custódia e no KYC de um número selecionado de fornecedores. We do not recommend BAT as a [private cryptocurrency](cryptocurrency.md), nor do we recommend using a [custodial wallet](advanced/payments.md#wallet-custody), so we would discourage using this feature.

**A Brave Wallet** funciona localmente no seu computador, mas não suporta quaisquer criptomoedas privadas, pelo que desencorajamos a utilização desta funcionalidade também.

## Recursos Adicionais

## Critérios

**Note que não estamos associados a nenhum dos projetos que recomendamos.** Para além dos [nossos critérios padrão](about/criteria.md), temos um conjunto claro de requisitos que nos permitem fornecer recomendações objetivas. Sugerimos que se familiarize com esta lista antes de optar por um projeto e que desenvolva a sua própria investigação para garantir que se trata da escolha certa para si.

### Requisitos mínimos

- Software de código aberto.
- Deve suportar atualizações automáticas.
- Must receive engine updates in 0-1 days from upstream release.
- Must be available on Linux, macOS, and Windows.
- Any changes required to make the browser more privacy-respecting must not negatively impact user experience.
- Must block third-party cookies by default.
- Must support [state partitioning](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning) to mitigate cross-site tracking.[^1]

### Melhor caso

Estes são os critérios que consideramos essenciais para um projeto perfeito nesta categoria. As nossas recomendações podem não incluir todas as funcionalidades, mas incluem as que, na nossa opinião, têm um impacto mais elevado.

- Should include built-in content blocking functionality.
- Should support cookie compartmentalization (à la [Multi-Account Containers](https://support.mozilla.org/kb/containers)).
- Should support Progressive Web Apps. PWAs enable you to install certain websites as if they were native apps on your computer. This can have advantages over installing Electron-based apps, because PWAs benefit from your browser's regular security updates.
- Should not include add-on functionality (bloatware) that does not impact user privacy.
- Should not collect telemetry by default.
- Should provide an open-source sync server implementation.
- Should default to a [private search engine](search-engines.md).

[^1]: Brave's implementation is detailed at [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state).
