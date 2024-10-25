---
meta_title: "Navegadores de Internet que Respeitam a Privacidade para PC e Mac — Privacy Guides"
title: "Navegadores Desktop"
icon: material/laptop
description: Estes navegadores com foco em privacidade são o que recomendamos atualmente para a navegação normal/não anônima na Internet em computadores de uso doméstico.
cover: desktop-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Recomendações de Navegadores Desktop Privados
    url: "./"
    relatedLink: "../mobile-browsers/"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Mullvad Browser
    image: /assets/img/browsers/mullvad_browser.svg
    url: https://mullvad.net/pt/browser
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
    sameAs: https://pt.wikipedia.org/wiki/Mozilla_Firefox
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
    name: Brave
    image: /assets/img/browsers/brave.svg
    url: https://brave.com
    sameAs: https://pt.wikipedia.org/wiki/Brave_(navegador)
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
---

<small>Protege contra as seguintes ameaça(s):</small>

- [:material-account-cash: Sistemas de Vigilância](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Estas são as nossas recomendações atuais ** navegadores de computador ** e configurações para navegação padrão/não anônima. Recomendamos [Mullvad Browser](#mullvad-browser) se estiver interessado em fortes proteções de privacidade e anti-fingerprinting por padrão, o [Firefox](#firefox) para navegadores de internet comuns que buscam uma boa alternativa ao Google Chrome e o [Brave](#brave) se você precisar de compatibilidade com a engine Chromium.

Se você precisa navegar na internet de maneira anônima, você deveria usar o [Tor](tor.md) em vez disso. Temos algumas recomendações de configuração nessa página, mas todos os navegadores que não sejam o Tor Browser são rastreáveis por *alguém* de alguma maneira ou de outra.

## Mullvad Browser

<div class="admonition recommendation" markdown>

![Mullvad Browser logo]
(assets/img/browsers/mullvad_browser.svg){ align=right }

**Navegador Mullvad** é uma versão de [Negador Tor](tor.md#tor-browser) com as integrações da rede  Tor removida.
 O seu objetivo é fornecer aos utilizadores de VPN as tecnologias de navegação anti-fingerprinting do Navegador Tor, que são proteções fundamentais contra [:material-eye-outline: Vigilância em massa](basics/common-threats.md#mass-surveillance-programs){ .pg-blue } É desenvolvido pelo Projeto Tor e distribuído pela [Mullvad](vpn.md#mullvad), e **não** requer o uso da VPN da Mullvad.

[:octicons-home-16: Pagina Inicial]
(https://mullvad.net/en/browser){ .md-button .md-button--primary }
[:octicons-eye-16:]
(https://mullvad.net/en/help/privacy-policy){ .card-link title="Política de privacidade" }
[:octicons-info-16:]
(https://mullvad.net/en/help/tag/mullvad-browser){ .card-link title=Documentação}
[:octicons-code-16:]
(https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Código fonte" }

<details class="downloads" markdown>
<summary>Downloads</summary>
- [:fontawesome-brands-windows: Windows]
(https://mullvad.net/en/download/browser/windows)
- [:simple-apple: macOS]
(https://mullvad.net/en/download/browser/macos)
- [:simple-linux: Linux]
(https://mullvad.net/en/download/browser/linux)

</details>

</div>

Como o [Navegador Tor](tor.md), o Navegador Mullvad foi projetado para evitar a impressão digital, tornando a impressão digital de seu navegador igual a de todas as outras pessoas do Navegador Mullvad, de modo que ele inclui configurações e extensões predefinidas que são configuradas automaticamente pelos seguintes níveis de segurança padrão: Padrão *(Standard)*, Seguro *(Safer)* e O Mais Seguro *(Safest)*. Por conseguinte, é imperativo que não modifique o browser para além de ajustar a predefinição [ Níveis de segurança](https://tb-manual.torproject.org/security-settings). Outras modificações tornariam a sua impressão digital única, derrotando o propósito de usar este navegador. Se você preferir personalizar mais o navegador e a identificação das suas impressões digitais não é uma preocupação para você, recomendamos o [Firefox](#firefox).

### Anti-impressões Digitais

**Sem** utilizar uma [VPN](vpn.md), o Mullvad Browser garante as mesmas proteções contra [ingênuos scripts de impressão digital](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting), assim como os outros navegadores tipo o Firefox + [Arkenfox](#arkenfox-advanced) e o [Brave](#brave). O Mullvad Broowser oferece proteções fora da caixa, as custas de algumas flexibilidades e conveniências que outros navegadores privados podem oferecer.

==Para a mais forte proteção contra impressões digitais, recomendamos o uso do Navegador Mullvad em conjunto **com** uma VPN==, seja ela Mullvad ou outro provedor de VPN recomendado. Quando você estiver usando uma VPN e o Navegador Mullvad, você compartilhará uma impressão digital e um grupo de endereços IP com uma grande variedade de outras pessoas, dando a você uma "multidão" para se misturar. Esta estratégia é a única forma de frustrar scripts avançados de rastreamento, e é a mesma técnica anti-impressão digital usada pelo Navegador Tor.

Note que enquanto você pode usar o Navegador Mullvad com qualquer fornecedor de VPN, outras pessoas nessa VPN também devem estar usando o Mullvad Browser para que essa "multidão" exista, algo que é mais provável na Mullvad VPN do que em outros fornecedores, principalmente por causa do recente lançamento do Navegador Mullvad. O Navegador Mullvad não possui conectividade VPN integrada, nem verifica se você está usando uma VPN antes de navegar; sua conexão VPN precisa ser configurada e administrada separadamente.

O Navegador Mullvad vem com as extensões de navegador *uBlock Origin* e *NoScript* pré-instaladas. Embora normalmente desencorajemos a adição de * adicionais* [ extensões de navegador](browser-extensions.md), estas extensões que vêm pré-instaladas com o browser devem **não** ser removidas ou configurados fora dos seus valores predefinidos, porque isso tornaria a impressão digital do seu browser visivelmente diferente da de outros utilizadores do Mullvad Browser. Ele também vem pré-instalado com a Extensão Mullvad Browser, que *pode* ser removida em segurança, se você quiser, sem afetar a impressão digital do seu navegador, mas também é seguro para manter mesmo se você não usar o Mullvad VPN.

### Modo de Navegação Privada

O Navegador Mullvad opera em modo de navegação privada permanente, o que significa que o seu histórico, cookies e outros dados de sites serão apagados sempre que o navegador for fechado. Seus favoritos, configurações do navegador e configurações de extensão ainda serão preservados.

Isso é necessário para evitar formas avançadas de rastreamento, mas vem com o custo de conveniência e alguns recursos do Firefox, como contêineres de várias contas. Lembre-se de que você sempre pode usar vários navegadores, por exemplo, você pode considerar usar o Firefox+ Arkenfox para alguns sites em que deseja permanecer conectado ou não funcionar corretamente no Navegador Mullvad, e usar o Navegador Mullvad para navegação geral.

### Mullvad Leta

Navegador de Mullvad vem com o DuckDuckGo definido como o [mecanismo de pesquisa padrão](search-engines.md), mas também vem pré-instalado com o **Mullvad Leta**, um mecanismo de busca que requer uma assinatura ativa do Mullvad VPN para acessar. O Mullvad Leta consulta diretamente a API de pesquisa paga do Google, razão pela qual está limitado aos assinantes pagantes. No entanto, é possível ao Mullvad correlacionar as consultas de pesquisa e as contas VPN do Mullvad devido a esta limitação. Por esse motivo, desencorajamos o uso do Mullvad Leta, mesmo que o Mullvad colete muito pouca informação sobre seus assinantes de VPN.

## Firefox

<div class="admonition recommendation" markdown>

![Firefox logo](assets/img/browsers/firefox.svg){ align=right }

O **Firefox** fornece configurações fortes de privacidade como a [Proteção avançada de rastreio](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop), que pode ajudar a bloquear varios [tipos de rastreio](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop#w_what-enhanced-tracking-protection-blocks).

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
<p class="admonition-title">Warning</p>

Firefox includes a unique [download token](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) in downloads from Mozilla's website and uses telemetry in Firefox to send the token. The token is **not** included in releases from the [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/).

</div>

### Recommended Firefox Configuration

Essas opções podem ser encontradas em :material-menu: → **Configurações**.

#### Pesquisa

- [ ] Uncheck **Show search suggestions**

Os recursos de sugestão de pesquisa podem não estar disponíveis na sua região.

Sugestões de pesquisa enviam tudo o que você digita na barra de endereços para o mecanismo de pesquisa padrão, independente se você enviar uma pesquisa real. Desabilitar sugestões de busca permite que você controle com mais precisão quais dados você envia para o seu provedor de mecanismo de pesquisa.

##### Firefox Suggest (apenas nos EUA)

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) is a feature similar to search suggestions which is only available in the US. Recomendamos desativá-lo pelo mesmo motivo que recomendamos desativar as sugestões de pesquisa. Se você não ver essas opções sob o **cabeçalho da barra de endereços**, você não tem esse novo experimento e pode ignorar essas alterações.

- [ ] Uncheck **Suggestions from Firefox**
- [ ] Desmarque **Sugestões de patrocinadores**

#### Privacidade & Segurança

##### Proteção aprimorada contra rastreamento (ETP)

- [x] Selecione **Rigoroso**

Isso protege você bloqueando rastreadores de mídia social, scripts de impressão digital (observe que isso não protege você de *todas as* impressões digitais), criptominers, “cookies” de rastreamento entre sites e alguns outros conteúdos de rastreamento. A Proteção aprimorada contra rastreamento (ETP) protege contra muitas ameaças comuns, mas isso não bloqueia todos os meios de rastreamento porque é projetado para ter um mínimo ou nenhum impacto na usabilidade do site.

##### Sanitizar ao Fechar

O serviço [Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy/) usa E2EE.

- Selecione **Excluir cookies e dados do site quando o Firefox estiver fechado**

Isso protege você contra cookies persistentes, mas não te protege contra cookies adquiridos durante a atual sessão de navegação. Quando isso está ativado, é possível limpar facilmente os cookies do navegador simplesmente reiniciando o Firefox. Você pode estabelecer exceções por site, se deseja permanecer logado em um site específico que você visita com frequência.

##### Telemetria

- Limpar **Permitir que o Firefox envie dados técnicos e de interação para o Mozilla**
- Limpar **Permitir que o Firefox instale e execute estudos**
- Limpar **Permitir que o Firefox envie relatórios de falhas identificadas em seu nome**

> O Firefox envia dados sobre a sua versão e língua do Firefox; sistema operacional e configuração de hardware; memória, informação básica sobre crashes e erros; resultados de processos automatizados como atualizações, navegação segura e ativação para nós. Quando o Firefox envia dados para nós, seu endereço IP é temporariamente coletado como parte dos registros do nosso servidor.

Additionally, the Mozilla Accounts service collects [some technical data](https://mozilla.org/privacy/mozilla-accounts). If you use a Mozilla Account you can opt-out:

1. Abra as suas [configurações de perfil em accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Desmarque **Coleta de dados e uso** > **Ajude a melhorar as contas Firefox**

##### Website Advertising Preferences

- [ ] Uncheck **Allow websites to perform privacy-preserving ad measurement**

With the release of Firefox 128, a new setting for [privacy-preserving attribution](https://support.mozilla.org/kb/privacy-preserving-attribution) (PPA) has been added and [enabled by default](https://blog.privacyguides.org/2024/07/14/mozilla-disappoints-us-yet-again-2). PPA allows advertisers to use your web browser to measure the effectiveness of web campaigns, instead of using traditional JavaScript-based tracking. We consider this behavior to be outside the scope of a user agent's responsibilities, and the fact that it is disabled by default in Arkenfox is an additional indicator for disabling this feature.

##### HTTPS-Only Mode

- Selecione **Ativar modo somente HTTPS em todas as janelas**

Isso te previne de se conectar sem querer a um site em plain-text HTTP. Sites sem HTTPS são incomuns hoje em dia, então isso deve trazer pouco ou nenhum impacto na sua navegação do dia a dia.

##### DNS sobre HTTPS

If you use a [DNS over HTTPS provider](dns.md):

- [x] Select **Max Protection** and choose a suitable provider

Max Protection enforces the use of DNS over HTTPS, and a security warning will show if Firefox can’t connect to your secure DNS resolver, or if your secure DNS resolver says that records for the domain you are trying to access do not exist. This stops the network you're connected to from secretly downgrading your DNS security.

#### Sync

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices and protects it with E2EE.

### Extensões

<div class="admonition tip" markdown>
<p class="admonition-title">Use Mullvad Browser for advanced anti-fingerprinting</p>

[Mullvad Browser](#mullvad-browser) fornece as mesmas proteções contra impressões digitais que o Arkenfox, e não requer o uso do Mullvad VPN para usufruir dessas proteções. Acompanhado de uma VPN, o Mullvad Browser pode impedir scripts mais avançados de rastreio que o Arkenfox não é capaz. O Arkenfox ainda tem a vantagem de ser muito mais flexível e personalizável com exceções para cada site que você precisa permanecer logado.

</div>

O [projeto Arkenfox](https://github.com/arkenfox/user.js) fornece uma série de opções cuidadosamente selecionadas para o Firefox. If you [decide](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) to use Arkenfox, a [few options](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) are subjectively strict and/or may cause some websites to not work properly—which you can [easily change](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) to suit your needs. Nós **fortemente recomendamos** que você leia [a wiki completa do projeto](https://github.com/arkenfox/user.js/wiki). Arkenfox also enables [container](https://support.mozilla.org/kb/containers#w_for-advanced-users) support.

Arkenfox apenas mira em impedir básicos ou ingênuos scripts de rastreio através de uma aleatorização de tela e as configurações incorporadas do Firefox para resistir às impressões digitais. Ele não mira em fazer o seu navegador se misturar com uma grande multidão de outros usuários do Arkenfox na mesma forma que o Mullvad Browser ou o Tor Browser fazem, que é a única forma de impedir scripts avançados de rastreio de impressões digitais. Lembre-se que você pode sempre usar vários navegadores, por exemplo, você pode considerar usar o Firefox + Arkenfox para alguns poucos sites que você confia ou deseja permanecer logado, e o Mullvad Browser para a navegação em um geral.

## Brave

<div class="admonition recommendation annotate" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** includes a built-in content blocker and [privacy features](https://brave.com/privacy-features), many of which are enabled by default.

O Brave foi construído com base no projeto de navegador Chromium, então deve parecer familiar e ter mínimos problemas de compatibilidade em websites.

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

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

Brave adds a "[referral code](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)" to the file name in downloads from the Brave website, which is used to track which source the browser was downloaded from, for example `BRV002` in a download named `Brave-Browser-BRV002.pkg`. The installer will then ping Brave's server with the referral code at the end of the installation process. If you're concerned about this, you can rename the installer file before opening it.

</div>

### Recommended Brave Configuration

Essas opções podem ser encontradas em :material-menu: → **Configurações**.

#### Shields

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) feature. We suggest configuring these options [globally](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) across all pages that you visit.

As opções do Shields podem ser reduzidas para cada site caso necessário, mas por padrão nós recomendamos configurar as seguintes:

<div class="annotate" markdown>

- [x] Select **Aggressive** under *Trackers & ads blocking*

<details class="warning" markdown>
<summary>Use default filter lists</summary>

Brave allows you to select additional content filters within the internal `brave://adblock` page. Nós não aconselhamos a utilizar essa ferramenta; ao invés disso, mantenha as listas de filtro padrão. A utilização de listas extra fará com que se destaque dos outros usuários do Brave e pode também aumentar a superfície de ataque se houver uma vulnerabilidade no Brave e uma regra maliciosa for adicionada a uma das listas que utiliza.

</details>

- [x] Select **Strict** under *Upgrade connections to HTTPS*
- [x] (Optional) Select **Block Scripts** (1)
- [x] Check **Block fingerprinting**
- [x] Select **Block third-party cookies**
- [x] Check **Forget me when I close this site** (2)
- [ ] Uncheck all social media components

</div>

1. This option disables JavaScript, which will break a lot of sites. To unbreak them, you can set exceptions on a per-site basis by clicking on the Shield icon in the address bar and unchecking this setting under *Advanced controls*.
2. If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis by clicking on the Shield icon in the address bar and unchecking this setting under *Advanced controls*.

#### Privacy and security

<div class="annotate" markdown>

- [x] Select **Don't allow sites to use the V8 optimizer** under *Security* → *Manage V8 security* (1)
- [x] Select **Automatically remove permissions from unused sites** under *Sites and Shields Settings*
- [x] Select **Disable non-proxied UDP** under [*WebRTC IP Handling Policy*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Uncheck **Use Google services for push messaging**
- [x] Select **Auto-redirect AMP pages**
- [x] Select **Auto-redirect tracking URLs**
- [x] Select **Prevent sites from fingerprinting me based on my language preferences**

</div>

1. Disabling the V8 optimizer reduces your attack surface by disabling [*some*](https://grapheneos.social/@GrapheneOS/112708049232710156) parts of JavaScript Just-In-Time (JIT) compilation.

<div class="admonition tip" markdown>
<p class="admonition-title">Sanitizing on close</p>

- [x] Select **Delete data sites have saved to your device when you close all windows** under *Sites and Shields Settings* → *Content* → *Additional content settings* → *On-device site data*.

If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis under the *Customized behaviors* section.

</div>

##### Tor windows

[**Private Window with Tor**](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity) allows you to route your traffic through the Tor network in Private Windows and access .onion services, which may be useful in some cases. However, Brave is **not** as resistant to fingerprinting as the Tor Browser and far fewer people use Brave with Tor, so you will stand out. If your threat model requires strong anonymity, use the [Tor Browser](tor.md#tor-browser).

##### Data Collection

- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send daily usage ping to Brave**
- [ ] Uncheck **Automatically send diagnostic reports**

#### Web3

As funcionalidades Web3 do Brave podem potencialmente acrescentar à impressão digital do seu navegador e a superfície de ataque. Unless you use any of these features, they should be disabled.

- Select **Extensions (no fallback)** under *Default Ethereum wallet*
- Select **Extensions (no fallback)** under *Default Solana wallet*

#### Extensions

- [ ] Uncheck all built-in extensions you don't use

#### System

<div class="annotate" markdown>

- [ ] Desmarque **Continuar executando os aplicativos em segundo plano quando o Brave for fechado** para desativar os aplicativos em segundo plano (1)

</div>

1. Esta opção não está presente em todas as plataformas.

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

#### Brave Rewards and Wallet

**Brave Rewards** lets you receive Basic Attention Token (BAT) cryptocurrency for performing certain actions within Brave. Ele depende de uma conta de custódia e KYC de um número selecionado de provedores. We do not recommend BAT as a [private cryptocurrency](cryptocurrency.md), nor do we recommend using a [custodial wallet](advanced/payments.md#wallet-custody), so we would discourage using this feature.

A **Carteira Brave** opera localmente em seu computador, mas não suporta nenhuma criptomoeda privada, então nós desencorajamos o uso dessa ferramenta também.

## Critérios

**Por favor, note que não somos parceiros de nenhum dos produtos que recomendamos.**Em adição aos[nossos critérios básicos](about/criteria.md), desenvolvemos um conjunto claro de requisitos para nos permitir fornecer recomendações objetivas. Recomendamos que você se familiarize com esta lista antes de escolher usar um produto, e que faça sua própria pesquisa para garantir que o produto escolhido é o ideal para você.

### Requisitos Mínimos

- Deve ser um software de código aberto.
- Deve suportar atualizações automáticas.
- Must receive engine updates in 0-1 days from upstream release.
- Must be available on Linux, macOS, and Windows.
- Any changes required to make the browser more privacy-respecting must not negatively impact user experience.
- Must block third-party cookies by default.
- Must support [state partitioning](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning) to mitigate cross-site tracking.[^1]

### Melhor Caso

Os nossos critérios de melhor caso representam o que gostaríamos de ver no projeto perfeito desta categoria. As nossas recomendações podem não incluir todas ou algumas destas funcionalidades, mas as que as incluem podem ter uma classificação mais elevada do que outras nesta página.

- Should include built-in content blocking functionality.
- Should support cookie compartmentalization (à la [Multi-Account Containers](https://support.mozilla.org/kb/containers)).
- Should support Progressive Web Apps. PWAs enable you to install certain websites as if they were native apps on your computer. This can have advantages over installing Electron-based apps, because PWAs benefit from your browser's regular security updates.
- Should not include add-on functionality (bloatware) that does not impact user privacy.
- Should not collect telemetry by default.
- Should provide an open-source sync server implementation.
- Should default to a [private search engine](search-engines.md).

[^1]: Brave's implementation is detailed at [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state).
