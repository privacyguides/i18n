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

[:octicons-home-16: Página inicial](https://mullvad.net/en/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Política de privacidade" }
[:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser){ .card-link title="Documentação" }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Código fonte" }

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

O Mullvad Browser vem com [**Mullvad Leta**](https://leta.mullvad.net) como mecanismo de pesquisa padrão, funcionando como um proxy para os resultados do Google ou do Brave (configurável na página inicial do Mullvad Leta).

Se você é usuário do Mullvad VPN, existe algum risco em usar serviços como o Mullvad Leta, que são oferecidos pelo próprio provedor de VPN. Isso ocorre porque, teoricamente, a Mullvad tem acesso ao seu endereço IP real (por meio da VPN) e à sua atividade de pesquisa (por meio do Leta), informações que uma VPN normalmente deveria manter separadas. Mesmo que a Mullvad colete pouquíssimas informações sobre seus assinantes de VPN ou usuários do Leta, você deve considerar um [mecanismo de pesquisa](search-engines.md) diferente se esse risco for uma preocupação para você.

## Firefox

<div class="admonition recommendation" markdown>

![Firefox logo](assets/img/browsers/firefox.svg){ align=right }

O **Firefox** fornece configurações fortes de privacidade como a [Proteção avançada de rastreio](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop), que pode ajudar a bloquear varios [tipos de rastreio](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop#w_what-enhanced-tracking-protection-blocks).

[:octicons-home-16: Página inicial](https://firefox.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/firefox){ .card-link title="Política de privacidade" }
[:octicons-info-16:](https://support.mozilla.org/products/firefox){ .card-link title="Documentação" }
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Código fonte" }
[:octicons-heart-16:](https://donate.mozilla.org){ .card-link title="Contribuir" }

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

O Firefox inclui um [token de download] exclusivo (https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) nos downloads do site da Mozilla e usa a telemetria no Firefox para enviar o token. O token **não** está incluído nas versões do [Mozilla FTP] (https://ftp.mozilla.org/pub/firefox/releases/).

</div>

### Configuração recomendada do Firefox

Essas opções podem ser encontradas em :material-menu: → **Configurações**.

#### Pesquisa

- [ ] Desmarque **Mostrar sugestões de pesquisa**

Os recursos de sugestão de pesquisa podem não estar disponíveis na sua região.

As sugestões de pesquisa enviam tudo o que você digita na barra de endereços para o mecanismo de pesquisa padrão, independentemente de você realizar uma pesquisa de fato. Desativar as sugestões de pesquisa permite que você controle com mais precisão quais dados são enviados ao seu provedor de mecanismo de pesquisa.

##### Firefox Suggest (apenas nos EUA)

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) é um recurso semelhante às sugestões de pesquisa, disponível apenas nos EUA. Recomendamos desativá-lo pelo mesmo motivo que sugerimos desativar as sugestões de pesquisa. Se você não ver essas opções sob o cabeçalho **Barra de Endereços**, significa que não possui a nova experiência e pode ignorar essas alterações.

- [ ] Desmarque **Sugestões de patrocinadores**
- [ ] Desmarque **Sugestões de patrocinadores**

#### Privacidade & Segurança

##### Proteção Aprimorada contra Rastreamento (ETP)

- [x] Selecione **Rigoroso**

Isso protege você ao bloquear rastreadores de mídias sociais, scripts de fingerprinting (mas note que isso não protege contra *todo* fingerprinting), mineradores de criptomoedas, cookies de rastreamento entre sites e alguns outros tipos de conteúdo de rastreamento. O ETP protege contra muitas ameaças comuns, mas não bloqueia todas as formas de rastreamento, pois foi projetado para ter impacto mínimo ou inexistente na usabilidade dos sites.

##### Sanitizar ao Fechar

Se quiser permanecer logado em sites específicos, você pode permitir exceções em **Cookies e Dados de Sites** → **Gerenciar Exceções...**

- Selecione **Excluir cookies e dados do site quando o Firefox estiver fechado**

Isso protege você contra cookies persistentes, mas não contra cookies adquiridos durante uma única sessão de navegação. Quando isso está ativado, torna-se possível limpar facilmente os cookies do seu navegador simplesmente reiniciando o Firefox. Você pode definir exceções para sites específicos, caso queira permanecer conectado a um site que visita com frequência.

##### Telemetria

- Limpar **Permitir que o Firefox envie dados técnicos e de interação para o Mozilla**
- Limpar **Permitir que o Firefox instale e execute estudos**
- Limpar **Permitir que o Firefox envie relatórios de falhas identificadas em seu nome**

De acordo com a política de privacidade do Firefox da Mozilla,

> O Firefox envia dados sobre a sua versão e língua do Firefox; sistema operacional e configuração de hardware; memória, informação básica sobre crashes e erros; resultados de processos automatizados como atualizações, navegação segura e ativação para nós. Quando o Firefox envia dados para nós, seu endereço IP é temporariamente coletado como parte dos registros do nosso servidor.

Além disso, o serviço de Contas Mozilla coleta [alguns dados técnicos](https://mozilla.org/privacy/mozilla-accounts). Se você usar uma Conta Mozilla, pode optar por não participar:

1. Abra as suas [configurações de perfil em accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Desmarque **Coleta de dados e uso** > **Ajude a melhorar as contas Firefox**

##### Preferências de publicidade em sites

- [ ] Desmarque **Permitir que sites façam medição de publicidade respeitando sua privacidade**

Com o lançamento do Firefox 128, uma nova configuração para [atribuição com preservação de privacidade](https://support.mozilla.org/kb/privacy-preserving-attribution) (PPA) foi adicionada e [ativada por padrão](https://blog.privacyguides.org/2024/07/14/mozilla-disappoints-us-yet-again-2). O PPA permite que os anunciantes usem seu navegador para medir a eficácia das campanhas na web, em vez de usar o rastreamento tradicional baseado em JavaScript. Consideramos esse comportamento fora do escopo das responsabilidades de um user agent, e o fato de estar desativado por padrão no Arkenfox é um indicativo adicional para desativar esse recurso.

##### Modo Somente HTTPS

- Selecione **Ativar modo somente HTTPS em todas as janelas**

Isso impede que você se conecte involuntariamente a um site usando HTTP em texto simples. Sites sem HTTPS são raros hoje em dia, portanto, isso deve ter pouco ou nenhum impacto na sua navegação diária.

##### DNS sobre HTTPS

Se você usar um [provedor de DNS sobre HTTPS](dns.md):

- [x] Selecione **Proteção Máxima** e escolha um provedor adequado

A Proteção Máxima impõe o uso de DNS sobre HTTPS, e um aviso de segurança será exibido se o Firefox não conseguir se conectar ao seu resolvedor DNS seguro ou se o resolvedor DNS seguro indicar que os registros para o domínio que você está tentando acessar não existem. Isso impede que a rede à qual você está conectado reduza secretamente a segurança do seu DNS.

#### Sincronização

[O Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) permite que seus dados de navegação (histórico, favoritos, etc.) fiquem acessíveis em todos os seus dispositivos e os protege com E2EE.

### Extensões

<div class="admonition tip" markdown>
<p class="admonition-title">Use o Mullvad Browser para obter uma proteção avançada contra impressões digitais</p>

[Mullvad Browser](#mullvad-browser) fornece as mesmas proteções contra impressões digitais que o Arkenfox, e não requer o uso do Mullvad VPN para usufruir dessas proteções. Acompanhado de uma VPN, o Mullvad Browser pode impedir scripts mais avançados de rastreio que o Arkenfox não é capaz. O Arkenfox ainda tem a vantagem de ser muito mais flexível e personalizável com exceções para cada site que você precisa permanecer logado.

</div>

O [projeto Arkenfox](https://github.com/arkenfox/user.js) oferece um conjunto de opções cuidadosamente selecionadas para o Firefox. Se você [decidir](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) usar o Arkenfox, [algumas opções](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) podem ser subjetivamente rígidas e/ou fazer com que alguns sites não funcionem corretamente — algo que você pode [ajustar facilmente](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) conforme suas necessidades. Nós **recomendamos fortemente** que você leia a [wiki completa](https://github.com/arkenfox/user.js/wiki) deles. .

Arkenfox only aims to thwart basic or naive tracking scripts through canvas randomization and Firefox's built-in fingerprint resistance configuration settings. It does not aim to make your browser blend in with a large crowd of other Arkenfox users in the same way Mullvad Browser or Tor Browser do, which is the only way to thwart advanced fingerprint tracking scripts. Remember that you can always use multiple browsers, for example, you could consider using Firefox+Arkenfox for a few sites that you want to stay logged in on or otherwise trust, and Mullvad Browser for general browsing.

## Brave

<div class="admonition recommendation annotate" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

O **Brave Browser** inclui um bloqueador de conteúdo embutido e [recursos de privacidade](https://brave.com/privacy-features/), os quais muitos são ativados por padrão.

O Brave foi construído com base no projeto de navegador Chromium, então deve parecer familiar e ter mínimos problemas de compatibilidade em websites.

[:octicons-home-16: Página inicial](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Serviço Onion" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Política de privacidade" }
[:octicons-info-16:](https://support.brave.com){ .card-link title="Documentação" }
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Código fonte" }

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
<p class="admonition-title">Aviso</p>

Brave adiciona um "[código de referência](https://github. om/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes) para o nome dos arquivos em downloads do site Brave, que é usado para rastrear de que origem o navegador foi baixado, por exemplo, `BRV002` em um download chamado `Brave-Browser-BRV002. kg`. O instalador enviará um ping para o servidor da Brave com o código de referência no final do processo de instalação. Se estiver preocupado com isso, você pode renomear o arquivo do instalador antes de abri-lo.

</div>

### Configuração recomendada do Brave

Essas opções podem ser encontradas em :material-menu: → **Configurações**.

#### Shields

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) feature. We suggest configuring these options [globally](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) across all pages that you visit.

As opções do Shields (Escudos) podem ser reduzidas de acordo com o site, conforme necessário, mas, por padrão, recomendamos configurar o seguinte:

<div class="annotate" markdown>

- [x] Selecione **Agressivo** em *Bloquear rastreadores e anúncios*

<details class="warning" markdown>
<summary>Usar listas de filtros padrão</summary>

O Brave permite que você selecione filtros de conteúdo adicionais na página interna `brave://adblock`. Nós não aconselhamos a utilizar essa ferramenta; ao invés disso, mantenha as listas de filtro padrão. A utilização de listas extra fará com que se destaque dos outros usuários do Brave e pode também aumentar a superfície de ataque se houver uma vulnerabilidade no Brave e uma regra maliciosa for adicionada a uma das listas que utiliza.

</details>

- [x] Selecione **Estrito** em *Fazer upgrade das conexões para HTTPS*
- [x] (Opcional) Selecione **Block Scripts** (1)
- [x] Marque **Block fingerprinting**
- [x] Selecione **Block third-party cookies**
- [x] Marque **Forget me when I close this site** (2)
- [ ] Desmarque todos os componentes de mídia social

</div>

1. Essa opção desabilita o JavaScript, o que interromperá muitos sites. To fix them, you can set exceptions on a per-site basis by clicking on the Shield icon in the address bar and unchecking this setting under *Advanced controls*.
2. Se desejar permanecer conectado a um site específico que visita com frequência, você pode definir exceções por site clicando no ícone do Shields na barra de endereços e desmarcando essa configuração em *Controles avançados*.

#### Privacidade e Segurança

<div class="annotate" markdown>

- [x] Selecione **Não permitir que sites usem o otimizador V8** em *Segurança* → *Gerenciar segurança V8* (1)
- [x] Selecione **Automaticamente remover permissões de sites inutilizados** em *Configurações de sites e Shields*
- [x] Selecione **Desabilitar UDP sem proxy** em [*WebRTC IP Handling Policy*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Desmarque **Usar serviços do Google para mensagens automáticas**
- [x] Selecione **Autoredirecionar páginas AMP**
- [x] Selecione **Autoredirecionar URLs de rastreamento**
- [x] Selecione **Impedir sites de obter minha impressão digital com base nas minhas preferências de linguagem.**

</div>

1. A desativação do otimizador V8 reduz sua superfície de ataque ao desativar [*algumas*](https://grapheneos.social/@GrapheneOS/112708049232710156) partes da compilação Just-In-Time (JIT) do JavaScript.

<div class="admonition tip" markdown>
<p class="admonition-title">Sanitarizando ao fechar</p>

— x] Selecione **Delete os dados que os sites salvaram no seu dispositivo ao fechar todas as janelas** em *Configurações de sites e Shields* → *Conteúdo* → *Configurações adicionais de conteúdo* → *dados de sites no dispositivo*.

Se desejar permanecer conectado a um site específico que visita com frequência, é possível definir exceções por site na seção *Comportamentos personalizados*.

</div>

##### Tor Windows

[**Private Window with Tor**](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity) allows you to route your traffic through the Tor network in Private Windows and access .onion services, which may be useful in some cases. However, Brave is **not** as resistant to fingerprinting as the Tor Browser is, and far fewer people use Brave with Tor, so you will stand out. If your threat model requires strong anonymity, use the [Tor Browser](tor.md#tor-browser).

##### Coleta de dados

- [ ] Desmarque **Permitir análise de produtos com preservação da privacidade (P3A)**
- [ ] Desmarque **Automaticamente enviar ping de uso diário para Brave**
- [ ] Desmarque **Automaticamente enviar relatórios de diagnóstico**

#### Web3

Brave's Web3 features can potentially add to your browser fingerprint and attack surface. Unless you use any of these features, they should be disabled.

- Selecione **Extensões (sem fallback)** sob *carteira Ethereum padrão*
- Selecione **Extensões (sem fallback)** sob *Carteira Solana padrão*

#### Extensões

- [ ] Desmarque todas as extensões integradas que você não usa

#### Motor de busca

We recommend disabling search suggestions in Brave for the same reason we recommend disabling this feature in [Firefox](#search).

- [ ] Desmarque **Mostrar sugestões de pesquisa**

#### Sistema

<div class="annotate" markdown>

- [ ] Desmarque **Continuar executando os aplicativos em segundo plano quando o Brave for fechado** para desativar os aplicativos em segundo plano (1)

</div>

1. Esta opção não está presente em todas as plataformas.

#### Sincronização do Brave

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

#### Recompensas Brave e Carteira

**Brave Rewards** lets you receive Basic Attention Token (BAT) cryptocurrency for performing certain actions within Brave. It relies on a custodial account and KYC from a select number of providers. We do not recommend BAT as a [private cryptocurrency](cryptocurrency.md), nor do we recommend using a [custodial wallet](advanced/payments.md#wallet-custody), so we would discourage using this feature.

**Brave Wallet** operates locally on your computer, but does not support any private cryptocurrencies, so we would discourage using this feature as well.

## Critérios

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

### Requisitos Mínimos

- Deve ser um software de código aberto.
- Deve suportar atualizações automáticas.
- Deve receber atualizações do mecanismo em 0 a 1 dias a partir da versão upstream.
- Deve estar disponível no Linux, macOS e Windows.
- Quaisquer alterações necessárias para tornar o navegador mais respeitoso com a privacidade não devem afetar negativamente a experiência do usuário.
- Deve bloquear cookies de terceiros por padrão.
- Deve suportar [particionamento de estado](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning) para mitigar o rastreamento entre sites.[^1]

### Melhor Caso

Nosso critério de melhor caso representa o que gostaríamos de ver em um projeto perfeito nessa categoria. Our recommendations may not include any or all of this functionality, but those which do may rank higher than others on this page.

- Deve incluir a funcionalidade integrada de bloqueio de conteúdo.
- Deve suportar compartimentação de cookie (à la [Contêineres de Multi-Contas](https://support.mozilla.org/kb/containers)).
- Deve oferecer suporte a PWAs (Progressive Web Apps). PWAs permite que você instale certos sites como se eles fossem aplicativos nativos no seu computador. Isso pode ter vantagens em relação à instalação de aplicativos baseados em Electron, pois os PWAs se beneficiam das atualizações de segurança regulares do seu navegador.
- Não deve incluir funcionalidades adicionais (bloatware) que não afetem a privacidade do usuário.
- Não deve coletar telemetria por padrão.
- Deve fornecer uma implementação de servidor de sincronização de código aberto.
- Deve ter como padrão um [mecanismo de pesquisa privado](search-engines.md).

[^1]: Implementação do Brave é detalhada em: [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state).
