---
meta_title: "Navegadores de Internet que Respeitam a Privacidade para PC e Mac — Privacy Guides"
title: "Navegadores Desktop"
icon: material/laptop
description: Estes navegadores de internet dão uma proteção à privacidade mais forte do que o Google Chrome.
cover: desktop-browsers.png
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Recomendações de Navegadores Desktop Privativos
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

Estes são nossos navegadores desktop recomendados no momento e configurações para navegação padrão / não-anônima. Recomendamos [Mullvad Browser](#mullvad-browser) se estiver interessado em fortes proteção de privacidade e anti-fingerprinting por padrão, o [Firefox](#firefox) para navegadores de internet comuns que buscam uma boa alternativa ao Google Chrome e o [Brave](#brave) se você precisar de compatibilidade com a engine Chromium.

Se você precisa navegar na internet de maneira anônima, você deveria usar o [Tor](tor.md) em vez disso. Temos algumas recomendações de configuração nessa página, mas todos os navegadores que não sejam o Tor Browser são rastreáveis por *alguém* de alguma maneira ou de outra.

## Mullvad Browser

!!! recommendation

    ![Mullvad Browser logo](assets/img/browsers/mullvad_browser.svg){ align=right }
    
    **Mullvad Browser** é uma versão do [Tor Browser](tor.md#tor-browser) com a integração na rede Tor removida, buscando providenciar as tecnologias anti-fingerprinting do Tor Browser para usuários de VPN. É desenvolvido pelo Projeto Tor e distribuído pela [Mullvad](vpn.md#mullvad), e **não** requer o uso da VPN da Mullvad.
    
    [:octicons-home-16: Homepage](https://mullvad.net/en/browser){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser/){ .card-link title=Documentation}
    [:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Source Code" }
    
    ??? downloads
    
        - [:simple-windows11: Windows](https://mullvad.net/en/download/browser/windows)
        - [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
        - [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

Como o [Navegador Tor](tor.md), o Navegador Mullvad foi projetado para evitar a impressão digital, tornando a impressão digital de seu navegador igual a de todas as outras pessoas do Navegador Mullvad, de modo que ele inclui configurações e extensões predefinidas que são configuradas automaticamente pelos seguintes níveis de segurança padrão: Padrão *(Standard)*, Seguro *(Safer)* e O Mais Seguro *(Safest)*. Assim, é importante que você não modifique o navegador de forma alguma a não ser através do ajuste dos [níveis de segurança](https://tb-manual.torproject.org/security-settings/) disponíveis. Outras modificações tornariam a sua impressão digital única, derrotando o propósito de usar este navegador. Se você preferir personalizar mais o navegador e a identificação das suas impressões digitais não é uma preocupação para você, recomendamos o [Firefox](#firefox).

### Anti-impressões Digitais

**Sem** utilizar uma [VPN](vpn.md), o Mullvad Browser garante as mesmas proteções contra [ingênuos scripts de impressão digital](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting), assim como os outros navegadores tipo o Firefox + [Arkenfox](#arkenfox-advanced) e o [Brave](#brave). O Mullvad Broowser oferece proteções fora da caixa, as custas de algumas flexibilidades e conveniências que outros navegadores privados podem oferecer.

==Para a mais forte proteção contra impressões digitais, recomendamos o uso do Navegador Mullvad em conjunto **com** uma VPN==, seja ela Mullvad ou outro provedor de VPN recomendado. Quando você estiver usando uma VPN e o Navegador Mullvad, você compartilhará uma impressão digital e um grupo de endereços IP com uma grande variedade de outras pessoas, dando a você uma "multidão" para se misturar. Esta estratégia é a única forma de frustrar scripts avançados de rastreamento, e é a mesma técnica anti-impressão digital usada pelo Navegador Tor.

Note que enquanto você pode usar o Navegador Mullvad com qualquer fornecedor de VPN, outras pessoas nessa VPN também devem estar usando o Mullvad Browser para que essa "multidão" exista, algo que é mais provável na Mullvad VPN do que em outros fornecedores, principalmente por causa do recente lançamento do Navegador Mullvad. O Navegador Mullvad não possui conectividade VPN integrada, nem verifica se você está usando uma VPN antes de navegar; sua conexão VPN precisa ser configurada e administrada separadamente.

O Navegador Mullvad vem com as extensões de navegador *uBlock Origin* e *NoScript* pré-instaladas. Ainda que normalmente [não recomendemos](#extensions) acrescentar *mais* extensões ao navegador, estas extensões que vêm pré-instaladas com o navegador **não** devem ser removidas ou configuradas fora de seus valores padrão, pois isso tornaria sua impressão digital do navegador visivelmente diferente de outros usuários do Navegador Mullvad. Ele também vem pré-instalado com a Extensão Mullvad Browser, que *pode* ser removida em segurança, se você quiser, sem afetar a impressão digital do seu navegador, mas também é seguro para manter mesmo se você não usar o Mullvad VPN.

### Modo de Navegação Privada

O Navegador Mullvad opera em modo de navegação privada permanente, o que significa que o seu histórico, cookies e outros dados de sites serão apagados sempre que o navegador for fechado. Seus favoritos, configurações do navegador e configurações de extensão ainda serão preservados.

Isso é necessário para evitar formas avançadas de rastreamento, mas vem com o custo de conveniência e alguns recursos do Firefox, como contêineres de várias contas. Lembre-se de que você sempre pode usar vários navegadores, por exemplo, você pode considerar usar o Firefox+ Arkenfox para alguns sites em que deseja permanecer conectado ou não funcionar corretamente no Navegador Mullvad, e usar o Navegador Mullvad para navegação geral.

### Mullvad Leta

Navegador de Mullvad vem com o DuckDuckGo definido como o [mecanismo de pesquisa padrão](search-engines.md), mas também vem pré-instalado com o **Mullvad Leta**, um mecanismo de busca que requer uma assinatura ativa do Mullvad VPN para acessar. A Mullvad Leta consulta diretamente a API de pesquisa paga do Google (razão pela qual se limita a assinantes pagos), no entanto, devido a esta limitação, é possível à Mullvad correlacionar as consultas de pesquisa e as contas VPN da Mullvad. Por esse motivo, desencorajamos o uso do Mullvad Leta, mesmo que o Mullvad colete muito pouca informação sobre seus assinantes de VPN.

## Firefox

!!! recommendation

    ![Firefox logo](assets/img/browsers/firefox.svg){ align=right }
    
    O **Firefox** fornece configurações fortes de privacidade como a [Proteção avançada de rastreio](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop), que pode ajudar a bloquear varios [tipos de rastreio](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop#w_what-enhanced-tracking-protection-blocks).
    
    [:octicons-home-16: Homepage](https://firefox.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.mozilla.org/privacy/firefox/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://firefox-source-docs.mozilla.org/){ .card-link title=Documentation}
    [:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://donate.mozilla.org/){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-windows11: Windows](https://www.mozilla.org/firefox/windows)
        - [:simple-apple: macOS](https://www.mozilla.org/firefox/mac)
        - [:simple-linux: Linux](https://www.mozilla.org/firefox/linux)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

!!! aviso
    O Firefox inclui um token exclusivo de [download](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0) pelo site da Mozilla e usa telemetria no Firefox para enviar o token. O token é **não** incluído nas versões do [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/).

### Firefox

Essas opções podem ser encontradas em :material-menu: → **Configurações**

#### Pesquisa

- [ ] Desmarque **Mostrar sugestões de pesquisa**

Os recursos de sugestão de pesquisa podem não estar disponíveis na sua região.

Sugestões de pesquisa enviam tudo o que você digita na barra de endereços para o mecanismo de pesquisa padrão, independente se você enviar uma pesquisa real. Desabilitar sugestões de busca permite que você controle com mais precisão quais dados você envia para o seu provedor de mecanismo de pesquisa.

#### Privacidade & Segurança

##### Proteção aprimorada contra rastreamento (ETP)

- [x] Selecione **Rigoroso**

Isso protege você bloqueando rastreadores de mídia social, scripts de impressão digital (observe que isso não protege você de *todas as* impressões digitais), criptominers, “cookies” de rastreamento entre sites e alguns outros conteúdos de rastreamento. A Proteção aprimorada contra rastreamento (ETP) protege contra muitas ameaças comuns, mas isso não bloqueia todos os meios de rastreamento porque é projetado para ter um mínimo ou nenhum impacto na usabilidade do site.

##### Firefox Suggest (apenas nos EUA)

[Firefox Suggest](https://support.mozilla.org/en-US/kb/firefox-suggest) é um recurso semelhante às sugestões de pesquisa que só está disponível nos EUA. Recomendamos desativá-lo pelo mesmo motivo que recomendamos desativar as sugestões de pesquisa. Se você não ver essas opções sob o **cabeçalho da barra de endereços**, você não tem esse novo experimento e pode ignorar essas alterações.

- [ ] Desmarque **Sugestões da web**
- [ ] Desmarque **Sugestões de patrocinadores**

##### Sanitizar ao Fechar

O serviço [Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy/) usa E2EE.

- Selecione **Excluir cookies e dados do site quando o Firefox estiver fechado**

Isso protege você contra cookies persistentes, mas não te protege contra cookies adquiridos durante a atual sessão de navegação. A extensão também é uma extensão :trophy: [recomendada](https://support.mozilla.org/kb/add-on-badges#w_recommended-extensions) pela Mozilla. Você pode estabelecer exceções por site, se deseja permanecer logado em um site específico que você visita com frequência.

##### Desativar Telemetria

- Limpar **Permitir que o Firefox envie dados técnicos e de interação para o Mozilla**
- Limpar **Permitir que o Firefox instale e execute estudos**
- Limpar **Permitir que o Firefox envie relatórios de falhas identificadas em seu nome**

> O Firefox envia dados sobre a sua versão e língua do Firefox; sistema operacional e configuração de hardware; memória, informação básica sobre crashes e erros; resultados de processos automatizados como atualizações, navegação segura e ativação para nós. Quando o Firefox envia dados para nós, seu endereço IP é temporariamente coletado como parte dos registros do nosso servidor.

Adicionalmente, o serviço de contas Firefox coleta alguns [dados técnicos](https://www.mozilla.org/en-US/privacy/firefox/#firefox-accounts). Se você usa uma Conta Firefox, você pode não optar por isso:

1. Abra as suas [configurações de perfil em accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Desmarque **Coleta de dados e uso** > **Ajude a melhorar as contas Firefox**

##### Modo Somente HTTPS

- Selecione **Ativar modo somente HTTPS em todas as janelas**

Isso te previne de se conectar sem querer a um site em plain-text HTTP. Sites sem HTTPS são incomuns hoje em dia, então isso deve trazer pouco ou nenhum impacto na sua navegação do dia a dia.

#### Sync

O [Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy/) permite que seus dados de navegação (histórico, favoritos, etc.) sejam acessíveis em todos os seus dispositivos, além de protegê-los com E2EE.

### Extensões

!!! Dica "Use o Mullvad Browser para proteção avançada contra impressões digitais"

    [Mullvad Browser](#mullvad-browser) fornece as mesmas proteções contra impressões digitais que o Arkenfox, e não requer o uso do Mullvad VPN para usufruir dessas proteções. Acompanhado de uma VPN, o Mullvad Browser pode impedir scripts mais avançados de rastreio que o Arkenfox não é capaz. O Arkenfox ainda tem a vantagem de ser muito mais flexível e personalizável com exceções para cada site que você precisa permanecer logado.

O [projeto Arkenfox](https://github.com/arkenfox/user.js) fornece uma série de opções cuidadosamente selecionadas para o Firefox. Se você [decidir](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) usar o Arkenfox, [algumas opções](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) são subjetivamente estritas e/ou podem fazer alguns sites não funcionarem corretamente - [as quais você pode facilmente mudar](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) para atender as suas necessidades. Nós **fortemente recomendamos** que você leia [a wiki completa do projeto](https://github.com/arkenfox/user.js/wiki). O Arkenfox também suporta o uso de [containers](https://support.mozilla.org/en-US/kb/containers#w_for-advanced-users).

Arkenfox apenas mira em impedir básicos ou ingênuos scripts de rastreio através de uma aleatorização de tela e as configurações incorporadas do Firefox para resistir às impressões digitais. Ele não mira em fazer o seu navegador se misturar com uma grande multidão de outros usuários do Arkenfox na mesma forma que o Mullvad Browser ou o Tor Browser fazem, que é a única forma de impedir scripts avançados de rastreio de impressões digitais. Lembre-se que você pode sempre usar vários navegadores, por exemplo, você pode considerar usar o Firefox + Arkenfox para alguns poucos sites que você confia ou deseja permanecer logado, e o Mullvad Browser para a navegação em um geral.

## Brave

!!! recommendation

    ![Brave logo](assets/img/browsers/brave.svg){ align=right }
    
    O **Brave Browser** inclui um bloqueador de conteúdo embutido e [recursos de privacidade](https://brave.com/privacy-features/), os quais muitos são ativados por padrão.
    
    O Brave foi construído com base no projeto de navegador Chromium, então deve parecer familiar e ter mínimos problemas de compatibilidade em websites.
    
    [:octicons-home-16: Página Inicial](https://proton.me/mail){ .md-button .md-button--primary }
    [:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Serviço Onion" }
    [:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://support.brave.com){ .card-link title=Documentação}
    [:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Código-Fonte" }
    
    ??? downloads annotate
    
        - [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
        - [:simple-windows11: Windows](https://brave.com/download/)
        - [:simple-apple: macOS](https://brave.com/download/)
        - [:simple-linux: Linux](https://brave.com/linux/) (1)

    1. Nós aconselhamos a não usar a versão Flatpak do Brave, já que ela substitui o sandbox do Chromium com o Flatpak, que é menos eficaz. Além disso, o pacote de instalação não é mantido pela Brave Software, Inc.

### Firefox

Essas opções podem ser encontradas em :material-menu: → **Configurações**.

#### Configurações

##### Modo Somente HTTPS

A Brave inclui algumas medidas anti-impressão digital na sua funcionalidade [Shields](https://support.brave.com/hc/en-us/articles/360022973471-What-is-Shields-) . Nós sugerimos configurar essas opções [globalmente](https://support.brave.com/hc/en-us/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings-) em todas as páginas que você visitar.

As opções do Shields podem ser reduzidas para cada site caso necessário, mas por padrão nós recomendamos configurar as seguintes:

<div class="annotate" markdown>

- [x] Selecione **Evitar que os sites me identifiquem com base nas minhas preferências de idioma**
- [x] Selecione **Agressivo** em Rastreadores e bloqueio de anúncios

???? alerta "Use as listas de filtro padrão"
        O Brave permite que você acrescente listas adicionais de filtro através da página interna `brave://adblock`. Nós não aconselhamos a utilizar essa ferramenta; ao invés disso, mantenha as listas de filtro padrão. A utilização de listas extra fará com que se destaque dos outros usuários do Brave e pode também aumentar a superfície de ataque se houver uma vulnerabilidade no Brave e uma regra maliciosa for adicionada a uma das listas que utiliza.

- [x] (Opcional) Selecione **Bloquear scripts** (1)
- [x] Selecione **Restrito, pode quebrar sites** em Bloquear impressões digitais

</div>

1. Esta opção fornece uma funcionalidade semelhante aos modos de bloqueio avançados do uBlock Origin [](https://github.com/gorhill/uBlock/wiki/Blocking-mode) ou à extensão [NoScript](https://noscript.net/) .

##### Bloqueio de redes sociais

- [ ] Desmarque todos os componentes de redes sociais

##### Privacidade e Segurança

<div class="annotate" markdown>

- [x] Selecione **Desativar UDP não-proxy** em [Política de manuseio de IP do WebRTC] (https://support.brave.com/hc/en-us/articles/360017989132-How-do-I-change-my-Privacy-Settings-#webrtc)
- [ ] Desmarque **Use os serviços do Google para receber mensagens push**
- [ ] Desmarque **Permitir a análise de produtos com preservação da privacidade (P3A)**
- [ ]Desmarque **Enviar automaticamente um ping diário de uso ao Brave**
- [ ] Desmarque **Enviar relatórios de diagnóstico automaticamente**
- [x] Selecione **Sempre usar conexões seguras** no menu **Segurança**
- [ ] Desmarque **Janela privada com Tor** (1)

    !!! dica "Sanitizar ao fechar"

        - [x] Selecione **Limpar cookies e dados de sites quando você fechar todas as janelas** no menu *Cookies e outros dados do site*

        Se quiser permanecer logado em um site particular que visita com frequência, você pode adicionar exceções para cada site na seção *Comportamentos personalizados*.

</div>

1. O Brave **não** é tão resistente a impressões digitais como o Tor Browser e muito menos pessoas utilizam o Brave com o Tor, então você se destacará. Quando [é necessário um forte anonimato](https://support.brave.com/hc/en-us/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity-)utilize o Tor Browser[](tor.md#tor-browser).

##### Extensões

Desative as extensões internas que você não usa em **Extensões**

- [ ] Desmarque **Hangouts**
- [ ] Desmarque **WebTorrent**

##### Web3

As funcionalidades Web3 do Brave podem potencialmente acrescentar à impressão digital do seu navegador e a superfície de ataque. A menos que utilize alguma destas funcionalidades, elas devem estar desativadas.

- [ ] Defina **Carteira Ethereum padrão** para **Nenhum**
- [ ] Defina **Carteira Solana Padrão** para **Nenhum**
- [ ] Defina **Método para resolver recursos de IPFS** como **Desativado**

##### Sistema

<div class="annotate" markdown>

- [ ] Desmarque **Continuar executando os aplicativos em segundo plano quando o Brave for fechado** para desativar os aplicativos em segundo plano (1)

</div>

1. Esta opção não está presente em todas as plataformas.

#### Sync

O [Brave Sync](https://support.brave.com/hc/en-us/articles/360059793111-Understanding-Brave-Sync) permite que os seus dados de navegação (histórico, marcadores, etc.) sejam acessíveis em todos os seus dispositivos sem necessidade de uma conta e protege-os com E2EE.

#### Recompensas Brave e Carteira

O **Brave Rewards** te permite receber a criptomoeda Basic Attention Token (BAT) por performar certas atividades através do Brave. Ele depende de uma conta de custódia e KYC de um número selecionado de provedores. Nós não recomendamos o BAT como uma [criptomoeda privada](cryptocurrency.md), tampouco recomendamos usar uma [carteira de custódia](advanced/payments.md#other-coins-bitcoin-ethereum-etc), então nós desencorajamos o uso dessa função.

A **Carteira Brave** opera localmente em seu computador, mas não suporta nenhuma criptomoeda privada, então nós desencorajamos o uso dessa ferramenta também.

## Recursos Adicionais

Em geral, nós recomendamos manter as extensões do seu navegador em um mínimo para diminuir a sua superfície de ataque; elas tem acesso previlegiado através do seu navegador, requerem que você confie no desenvolvedor, podem fazer você [se destacar](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint), e [enfraquecer](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ) o isolamento do site. No entanto, o uBlock Origin pode ser útil se valorizar a funcionalidade de bloqueio de conteúdos.

### uBlock Origin

!!! recommendation

    ![uBlock Origin logo](assets/img/browsers/ublock_origin.svg){ align=right }
    
    O **uBlock Origin** é um bloqueador de conteúdo popular que pode te ajudar a bloquear anúncios, rastreadores e scripts de impressão digital.
    
    [:octicons-repo-16: Repositório](https://github.com/gorhill/uBlock#readme){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://github.com/gorhill/uBlock/wiki/Privacy-policy){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://github.com/gorhill/uBlock/wiki){ .card-link title=Documentação}
    [:octicons-code-16:](https://github.com/gorhill/uBlock){ .card-link title="Código-fonte" } downloads
    
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/ublock-origin/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm)
        - [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/ublock-origin/odfafepnkmbhccpbejgmiehpchacaeak)

Nós sugerimos seguir a [documentação do desenvolvedor](https://github.com/gorhill/uBlock/wiki/Blocking-mode) e escolher um dos "modos". Listas de filtros adicionais podem impactar o desempenho e [podem aumentar a superfície de ataque](https://portswigger.net/research/ublock-i-exfiltrate-exploiting-ad-blockers-with-css).

##### Outras listas

Essas são algumas outras [listas de filtros](https://github.com/gorhill/uBlock/wiki/Dashboard:-Filter-lists) que você pode querer considerar adicionar:

- [x] Verifique **Privacidade** > **AdGuard URL Tracking Protection**
- Adicione [Actually Legitimate URL Shortener Tool](https://raw.githubusercontent.com/DandelionSprout/adfilt/master/LegitimateURLShortener.txt)

## Critérios

**Por favor, note que não somos parceiros de nenhum dos produtos que recomendamos.**Em adição aos[nossos critérios básicos](about/criteria.md), desenvolvemos um conjunto claro de requisitos para nos permitir fornecer recomendações objetivas. Recomendamos que você se familiarize com esta lista antes de escolher usar um produto, e que faça sua própria pesquisa para garantir que o produto escolhido é o ideal para você.

!!! exemplo "Essa seção é nova"

    Estamos trabalhando para estabelecer critérios definidos para cada seção de nosso site, e isto pode estar sujeito a mudanças. Se você tiver alguma dúvida sobre nossos critérios, por favor [pergunte em nosso fórum](https://discuss.privacyguides.net/latest) e não assuma que não consideramos algo ao fazer nossas recomendações se não estiver listado aqui. Há muitos fatores considerados e discutidos quando recomendamos um projeto, e documentar cada um deles é um trabalho em andamento.

### Requisitos Mínimos

- Deve ser um software de código aberto.
- Suporta atualizações automáticas.
- Recebe atualizações de engine em 0-1 dias a partir da versão upstream.
- Disponível em Linux, macOS e Windows.
- Quaisquer alterações necessárias para tornar o navegador mais respeitador da privacidade não devem afetar negativamente a experiência do usuário.
- Bloqueia cookies de terceiros por padrão.
- Suporta [particionamento de estado](https://developer.mozilla.org/en-US/docs/Web/Privacy/State_Partitioning) para mitigar o rastreio entre sites.[^1]

### Melhor Caso

Os nossos critérios de melhor caso representam o que gostaríamos de ver no projeto perfeito desta categoria. As nossas recomendações podem não incluir todas ou algumas destas funcionalidades, mas as que as incluem podem ter uma classificação mais elevada do que outras nesta página.

- Inclui a funcionalidade de bloqueio de conteúdo integrado.
- Suporta a compartimentação de cookies (à la [Multi-Account Containers](https://support.mozilla.org/en-US/kb/containers)).
- Suporta Aplicativos Web Progressivos.  
  PWAs permitem que você instale certos sites como se eles fossem aplicativos nativos no seu computador. Isso pode ter vantagens sobre a instalação de aplicações baseadas no Electron, pois te beneficia das atualizações de segurança regulares do seu navegador.
- Não inclui funcionalidades adicionais (bloatware) que não afetam a privacidade do usuário.
- Não coleta telemetria por padrão.
- Fornece implementação de servidor de código aberto.
- O padrão é um [mecanismo de busca privado](search-engines.md).

### Critérios de extensão

- Não deve replicar a funcionalidade incorporada do navegador ou do sistema operacional.
- Deve ter um impacto direto na privacidade do usuário, ou seja, não deve limitar-se a fornecer informações.

[^1]: A implementação do Brave é detalhada em [Brave Privacy Updates: Particionamento do estado da rede para privacidade](https://brave.com/privacy-updates/14-partitioning-network-state/).
