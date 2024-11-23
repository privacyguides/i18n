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

Navegador de Mullvad vem com o DuckDuckGo definido como o [mecanismo de pesquisa padrão](search-engines.md), mas também vem pré-instalado com o **Mullvad Leta**, um mecanismo de busca que requer uma assinatura ativa do Mullvad VPN para acessar. O Mullvad Leta consulta diretamente a API de pesquisa paga do Google, razão pela qual está limitado aos assinantes pagantes. No entanto, é possível ao Mullvad correlacionar as consultas de pesquisa e as contas VPN do Mullvad devido a esta limitação. Por esse motivo, desencorajamos o uso do Mullvad Leta, mesmo que o Mullvad colete muito pouca informação sobre seus assinantes de VPN.

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

Sugestões de pesquisa enviam tudo o que você digita na barra de endereços para o mecanismo de pesquisa padrão, independente se você enviar uma pesquisa real. Desabilitar sugestões de busca permite que você controle com mais precisão quais dados você envia para o seu provedor de mecanismo de pesquisa.

##### Firefox Suggest (apenas nos EUA)

[O Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest) é um recurso semelhante às sugestões de pesquisa que está disponível apenas nos EUA. Recomendamos desativá-lo pelo mesmo motivo que recomendamos desativar as sugestões de pesquisa. Se você não ver essas opções sob o **cabeçalho da barra de endereços**, você não tem esse novo experimento e pode ignorar essas alterações.

- [ ] Desmarque **Sugestões de patrocinadores**
- [ ] Desmarque **Sugestões de patrocinadores**

#### Privacidade & Segurança

##### Proteção Aprimorada contra Rastreamento (ETP)

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

De acordo com a política de privacidade do Mozilla para Firefox,

> O Firefox envia dados sobre a sua versão e língua do Firefox; sistema operacional e configuração de hardware; memória, informação básica sobre crashes e erros; resultados de processos automatizados como atualizações, navegação segura e ativação para nós. Quando o Firefox envia dados para nós, seu endereço IP é temporariamente coletado como parte dos registros do nosso servidor.

Ademais, o serviço Mozilla Accounts coleta [alguns dados técnicos](https://mozilla.org/privacy/mozilla-accounts). Se você usa uma Conta Firefox, você pode não optar por isso:

1. Abra as suas [configurações de perfil em accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Desmarque **Coleta de dados e uso** > **Ajude a melhorar as contas Firefox**

##### Preferências de publicidade em sites

- [ ] Desmarque **Permitir que sites façam medição de publicidade respeitando sua privacidade**

Com o lançamento do Firefox 128, uma nova configuração para [atribuição de preservação da privacidade](https://support.mozilla.org/kb/privacy-preserving-attribution) (PPA) foi adicionada e [ativada por padrão](https://blog.privacyguides.org/2024/07/14/mozilla-disappoints-us-yet-again-2). O PPA permite que os anunciantes usem seu navegador da Web para medir a eficácia das campanhas na Web, em vez de usar o rastreamento tradicional baseado em JavaScript. Consideramos que esse comportamento está fora do escopo das responsabilidades de um agente de usuário, e o fato de estar desativado por padrão no Arkenfox é um indicador adicional para a desativação desse recurso.

##### Modo Somente HTTPS

- Selecione **Ativar modo somente HTTPS em todas as janelas**

Isso te previne de se conectar sem querer a um site em plain-text HTTP. Sites sem HTTPS são incomuns hoje em dia, então isso deve trazer pouco ou nenhum impacto na sua navegação do dia a dia.

##### DNS sobre HTTPS

Se você usar um [provedor de DNS sobre HTTPS](dns.md):

- [x] Selecione **Proteção Máxima** e escolha um provedor adequado

A Proteção Máxima impõe o uso de DNS sobre HTTPS e um aviso de segurança será exibido se o Firefox não conseguir se conectar ao seu resolvedor de DNS seguro ou se o seu resolvedor de DNS seguro informar que os registros do domínio que você está tentando acessar não existem. Isso impede que a rede à qual você está conectado faça o downgrade secreto de sua segurança de DNS.

#### Sincronização

A [Sincronização do Firefox](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) permite que seus dados de navegação (histórico, favoritos, etc.) sejam acessíveis em todos os seus dispositivos, além de protegê-los com E2EE.

### Extensões

<div class="admonition tip" markdown>
<p class="admonition-title">Use o Mullvad Browser para obter uma proteção avançada contra impressões digitais</p>

[Mullvad Browser](#mullvad-browser) fornece as mesmas proteções contra impressões digitais que o Arkenfox, e não requer o uso do Mullvad VPN para usufruir dessas proteções. Acompanhado de uma VPN, o Mullvad Browser pode impedir scripts mais avançados de rastreio que o Arkenfox não é capaz. O Arkenfox ainda tem a vantagem de ser muito mais flexível e personalizável com exceções para cada site que você precisa permanecer logado.

</div>

O [projeto Arkenfox](https://github.com/arkenfox/user.js) fornece uma série de opções cuidadosamente selecionadas para o Firefox. Se você [decidir](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) usar o Arkenfox, [algumas opções](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) são subjetivamente rigorosas e/ou podem fazer com que alguns sites não funcionem corretamente, o que pode ser [facilmente alterado](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) para atender às suas necessidades. Nós **fortemente recomendamos** que você leia [a wiki completa do projeto](https://github.com/arkenfox/user.js/wiki). O Arkenfox também permite o suporte a [contêineres](https://support.mozilla.org/kb/containers#w_for-advanced-users).

Arkenfox apenas mira em impedir básicos ou ingênuos scripts de rastreio através de uma aleatorização de tela e as configurações incorporadas do Firefox para resistir às impressões digitais. Ele não mira em fazer o seu navegador se misturar com uma grande multidão de outros usuários do Arkenfox na mesma forma que o Mullvad Browser ou o Tor Browser fazem, que é a única forma de impedir scripts avançados de rastreio de impressões digitais. Lembre-se que você pode sempre usar vários navegadores, por exemplo, você pode considerar usar o Firefox + Arkenfox para alguns poucos sites que você confia ou deseja permanecer logado, e o Mullvad Browser para a navegação em um geral.

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

O Brave inclui algumas medidas contra a impressão digital em seu recurso [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields). Sugerimos configurar essas opções [globalmente](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) em todas as páginas que você visita.

As opções do Shields podem ser reduzidas para cada site caso necessário, mas por padrão nós recomendamos configurar as seguintes:

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

1. Essa opção desabilita o JavaScript, o que interromperá muitos sites. Para desbloqueá-los, você pode definir exceções por site clicando no ícone do Shields na barra de endereços e desmarcando essa configuração em *Controles avançados*.
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

[**Janela privada com Tor**](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity) permite rotear seu tráfego pela rede Tor em janelas privadas e acessar serviços .onion, o que pode ser útil em alguns casos. No entanto, o Brave **não** é tão resistente à impressão digital quanto o Navegador Tor, e muito menos pessoas usam o Brave com o Tor, portanto, você se destacará. Se o seu modelo de ameaça exigir um forte anonimato, use o [Navegador Tor](tor.md#tor-browser).

##### Coleta de dados

- [ ] Desmarque **Permitir análise de produtos com preservação da privacidade (P3A)**
- [ ] Desmarque **Automaticamente enviar ping de uso diário para Brave**
- [ ] Desmarque **Automaticamente enviar relatórios de diagnóstico**

#### Web3

As funcionalidades Web3 do Brave podem potencialmente acrescentar à impressão digital do seu navegador e a superfície de ataque. A menos que você use qualquer um desses recursos, eles devem ser desativados.

- Selecione **Extensões (sem fallback)** sob *carteira Ethereum padrão*
- Selecione **Extensões (sem fallback)** sob *Carteira Solana padrão*

#### Extensões

- [ ] Desmarque todas as extensões integradas que você não usa

#### Motor de busca

Recomendamos a desativação das sugestões de pesquisa no Brave pelo mesmo motivo que recomendamos a desativação desse recurso no [Firefox](#search).

- [ ] Desmarque **Mostrar sugestões de pesquisa**

#### Sistema

<div class="annotate" markdown>

- [ ] Desmarque **Continuar executando os aplicativos em segundo plano quando o Brave for fechado** para desativar os aplicativos em segundo plano (1)

</div>

1. Esta opção não está presente em todas as plataformas.

#### Sincronização do Brave

A [Sincronização do Firefox](https://hacks.mozilla.org/2018/11/firefox-sync-privacy) permite que seus dados de navegação (histórico, favoritos, etc.) sejam acessíveis em todos os seus dispositivos, além de protegê-los com E2EE.

#### Recompensas Brave e Carteira

**O Recompensas Brave** permite que você receba a criptomoeda Basic Attention Token (BAT) por realizar determinadas ações no Brave. Ele depende de uma conta de custódia e KYC de um número selecionado de provedores. Não recomendamos o BAT como uma [criptomoeda privada](cryptocurrency.md), nem recomendamos o uso de uma [carteira de custódia](advanced/payments.md#wallet-custody), portanto, não recomendamos o uso desse recurso.

A **Carteira Brave** opera localmente em seu computador, mas não suporta nenhuma criptomoeda privada, então nós desencorajamos o uso dessa ferramenta também.

## Critérios

**Por favor, note que não somos parceiros de nenhum dos produtos que recomendamos.**Em adição aos[nossos critérios básicos](about/criteria.md), desenvolvemos um conjunto claro de requisitos para nos permitir fornecer recomendações objetivas. Recomendamos que você se familiarize com esta lista antes de escolher usar um produto, e que faça sua própria pesquisa para garantir que o produto escolhido é o ideal para você.

### Requisitos Mínimos

- Deve ser um software de código aberto.
- Deve suportar atualizações automáticas.
- Deve receber atualizações do mecanismo em 0 a 1 dias a partir da versão upstream.
- Deve estar disponível no Linux, macOS e Windows.
- Quaisquer alterações necessárias para tornar o navegador mais respeitoso com a privacidade não devem afetar negativamente a experiência do usuário.
- Deve bloquear cookies de terceiros por padrão.
- Deve suportar [particionamento de estado](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning) para mitigar o rastreamento entre sites.[^1]

### Melhor Caso

Os nossos critérios de melhor caso representam o que gostaríamos de ver no projeto perfeito desta categoria. As nossas recomendações podem não incluir todas ou algumas destas funcionalidades, mas as que as incluem podem ter uma classificação mais elevada do que outras nesta página.

- Deve incluir a funcionalidade integrada de bloqueio de conteúdo.
- Deve suportar compartimentação de cookie (à la [Contêineres de Multi-Contas](https://support.mozilla.org/kb/containers)).
- Deve oferecer suporte a PWAs (Progressive Web Apps). PWAs permite que você instale certos sites como se eles fossem aplicativos nativos no seu computador. Isso pode ter vantagens em relação à instalação de aplicativos baseados em Electron, pois os PWAs se beneficiam das atualizações de segurança regulares do seu navegador.
- Não deve incluir funcionalidades adicionais (bloatware) que não afetem a privacidade do usuário.
- Não deve coletar telemetria por padrão.
- Deve fornecer uma implementação de servidor de sincronização de código aberto.
- Deve ter como padrão um [mecanismo de pesquisa privado](search-engines.md).

[^1]: Implementação do Brave é detalhada em: [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state).
