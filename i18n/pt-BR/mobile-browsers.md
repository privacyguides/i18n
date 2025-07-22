---
meta_title: "Navegadores da Web que protegem sua privacidade"
title: "Navegadores Móveis"
icon: material/cellphone-information
description:
cover: mobile-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Recomendações de Navegadores Móveis () Privados
    url: "./"
    relatedLink: "../desktop-browsers/"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Brave
    image: /assets/img/browsers/brave.svg
    url: https://brave.com
    applicationCategory: Web Browser
    operatingSystem:
      - Android
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Cromite
    image: /assets/img/browsers/cromite.svg
    url: https://cromite.org
    applicationCategory: Web Browser
    operatingSystem:
      - Android
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": Aplicativo Móvel
    name: Safari
    image: /assets/img/browsers/safari.svg
    url: https://apple.com/safari
    applicationCategory: Navegador de Internet
    operatingSystem:
      - iOS
    subjectOf:
      "@type": Página da Web
      url: "./"
---

<small>Protege contra as seguintes ameaças:</small>

- [:material-account-cash: Surveillance Capitalism](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Essa é a lista de <strong x-id=1>navegadores móveis</strong> recomendados para o acesso padrão/não-anônimo da internet em seu smartphone ou tablet Se você precisa navegar pela internet anonimamente, você deve usar o [Tor](tor.md).

## Brave

<div class="admonition recommendation" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

O **Brave Browser** inclui um bloqueador de conteúdo embutido e [recursos de privacidade](https://brave.com/privacy-features/), os quais muitos são ativados por padrão.

O Brave teve seu projeto embasado no navegador Chromium (fork do Google Chrome), seu funcionamento pode ser familiar e você poderá encontrar problemas mínimos de compatibilidade em alguns websites.

[:octicons-home-16: Página inicial](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Serviço Onion" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Política de privacidade" }
[:octicons-info-16:](https://support.brave.com){ .card-link title="Documentação" }
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Código fonte" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1052879175)
- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:simple-fdroid: F-Droid](https://brave-browser-apk-release.s3.brave.com/fdroid/repo/index.html)

</details>

</div>

### Configuração recomendada do Brave

O Navegador Tor é a única maneira de realmente navegar na Internet de forma anônima. Ao usar o Brave, recomendamos que você altere as seguintes configurações para proteger sua privacidade de determinadas partes, mas todos os navegadores, exceto o [Navegador Tor](tor.md#tor-browser), serão rastreáveis por *alguém* de uma forma ou de outra.

=== "Android"

    Essas opções podem ser encontradas em :material-menu: → Configurações → Proteções do Brave & privacidade**.

=== "iOS"

    Essas opções podem ser encontradas em :fontawesome-solid-ellipsis: → Configurações → Proteções do Brave & privacidade**.

#### Configuração padrão dos filtros do Brave

O Brave inclui algumas medidas 'anti-fingerprinting' em seu recurso [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields). Sugerimos que você configure essas opções [globalmente](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) em todas as páginas da web que você visita.

As opções do Shields (Escudos) podem ser reduzidas de acordo com o site, conforme necessário, mas, por padrão, recomendamos configurar o seguinte:

=== "Android"

    <div class="annotate" markdown>

    - [x] Selecione **Aggressive (Agressivo** ) em *Block trackers (Bloquear rastreadores) & ads (Anúncios)*
    - [x] Selecione **Auto-redirecionamento de páginas AMP**
    - [x] Selecione **URLs com rastreamento de redirecionamento automático**
    - [x] Selecione **Exigir que todas as conexões usem HTTPS (estrito)** em *Atualizar conexões para HTTPS*
    - \[x\] (Opcional) Selecione **Block Scripts** (1)
    - [x] Selecione **Block third-party cookies (Bloquear cookies de terceiros** ) em *Block Cookies (Bloquear cookies)*
    - [x] Selecione **Block Fingerprinting**
    - [x] Selecione **Prevent fingerprinting (Impedir impressões digitais) por meio das configurações de idioma**

    <details class="warning" markdown>
    <summary>Usar listas de filtros padrão</summary>

    O Brave permite que você selecione filtros de conteúdo adicionais no menu **Content Filtering (Filtragem de conteúdo** ) ou na página interna `brave://adblock`. Não é aconselhado utilizar essa ferramenta; ao invés disso, mantenha as listas de filtro padrão. A utilização de listas complementares fará com que se destaque dos outros usuários do Brave e pode também aumentar as chances de ataque se houver uma vulnerabilidade no Brave ou uma regra maliciosa estiver presente em uma das listas que você utiliza.

    </details>

    - [x] Selecione **Esquecer-me quando eu fechar este site**

    </div>

    1. Essa opção desabilita o JavaScript, o que interromperá muitos sites. Você pode definir exceções por site clicando no ícone do Shields na barra de endereços e desmarcando essa configuração em *Controles avançados*.

=== "iOS"

    <div class="annotate" markdown>

    - [x] Selecione **Agressivo** em *Bloquear rastreadores e anúncios
    - [x] Selecione **Strict** em *Upgrade Connections to HTTPS (Atualizar conexões para HTTPS)*
    - [x] Selecione **Auto-Redirect AMP pages (páginas AMP de redirecionamento automático)**
    - [x] Selecione **URLs de rastreamento de redirecionamento automático**
    - \[x\] (Opcional) Selecione **Block Scripts** (1)
    - [x] Selecione **Block Fingerprinting**
    - [x] Selecione **as guias do site fechadas** em *Destruição automática*

    <details class="warning" markdown>
    <summary>Usar listas de filtros padrão</summary>

    O Brave permite que você selecione filtros de conteúdo adicionais no menu **Content Filtering (Filtragem de conteúdo** ). Não é aconselhado utilizar essa ferramenta; ao invés disso, mantenha as listas de filtro padrão. A utilização de listas complementares fará com que se destaque dos outros usuários do Brave e pode também aumentar as chances de ataque se houver uma vulnerabilidade no Brave ou uma regra maliciosa estiver presente em uma das listas que você utiliza

    </details>

    </div>

    1. Essa opção desabilita o JavaScript, o que interromperá muitos sites. Para desbloqueá-los, você pode definir exceções por site clicando no ícone do Shields na barra de endereços e desmarcando essa configuração em *Controles avançados*.

##### Limpar dados de navegação (somente Android)

- [x] Selecione **Limpar dados ao sair**

##### Bloqueio de mídia social (somente Android)

- [ ] Desmarque todos os componentes de redes sociais

#### Outras configurações de privacidade

=== "Android"

    <div class="annotate" markdown>

    - [x] Selecione **Disable non-proxied UDP (Desativar UDP sem proxy** ) em [*Política de tratamento de IP WebRTC*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
    - \[x\] (Opcional) Selecione **Nenhuma proteção** em *Navegação segura* (1)
    - [Desmarque a opção **Permitir que os sites verifiquem se você tem métodos de pagamento salvos**
    - [Desmarque a opção **V8 Optimizer** em *Gerenciar segurança do V8*
    - [x] Selecione **Fechar guias ao sair**
    - [ ] Desmarque **Permitir análise de produtos com preservação da privacidade (P3A)**
    - [ ] Desmarque **Automaticamente enviar relatórios de diagnóstico**
    - [ ] Desmarque **Automaticamente enviar ping de uso diário para Brave**

    </div>

    1. A [implementação do Safe Browsing](https://support.brave.com/hc/en-us/articles/15222663599629-Safe-Browsing-in-Brave) da Brave no Android **não faz** proxy de [solicitações de rede do Safe Browsing](https://developers.google.com/safe-browsing/v4/update-api#checking-urls) como sua contraparte de desktop. Isso significa que o seu endereço IP pode ser descoberto (e registrado) pelo Google. Note que a Navegação segura não está disponível para dispositivos Android sem o Google Play Services.

=== "iOS"

    - [ ] Desmarque **Permitir análise de produtos com preservação da privacidade (P3A)**
    - [ ] Desmarque **Automaticamente enviar ping de uso diário para Brave**

#### Leo

Essas opções podem ser encontradas em :material-menu:/ → **Settings** → **Search engines**.

<div class="annotate" markdown>

- [ ] Desmarque **Mostrar sugestões de preenchimento automático na barra de endereços** (1)

</div>

1. Essa opção não está presente no aplicativo iOS do Brave.

#### Mecanismo de busca

Essas opções podem ser encontradas em :material-menu:/:fontawesome-solid-ellipsis: → **Settings** → **Search engines**.

- [ ] Desmarque **Mostrar sugestões de pesquisa**

#### Sincronização do Brave

O [Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) permite que os seus dados de navegação (histórico, marcadores, etc.) sejam acessíveis em todos os seus dispositivos sem necessidade de uma conta e protege-os com E2EE.

## Cromite (Android)

<div class="admonition recommendation" markdown>

![Logotipo da Cromite](assets/img/browsers/cromite.svg){ align=right }

**Cromite** é um navegador baseado no Chromium (fork do Chrome) com bloqueio de anúncios incorporado, proteções de impressão digital e outros [aprimoramentos de privacidade e segurança](https://github.com/uazo/cromite/blob/master/docs/FEATURES.md). É um <em>fork</em> do navegador **Bromite**.

[:octicons-home-16: Repositório](https://cromite.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/uazo/cromite/blob/master/docs/PRIVACY_POLICY.md){ .card-link title="Política de Privacidade" }
[:octicons-info-16:](https://github.com/uazo/cromite?tab=readme-ov-file#docs){ .card-link title=Documentação}
[:octicons-code-16:](https://github.com/uazo/cromite){ .card-link title="Código-fonte" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-android: F-Droid](https://cromite.org/fdroid/repo/?fingerprint=49F37E74DEE483DCA2B991334FB5A0200787430D0B5F9A783DD5F13695E9517B)
- [:simple-github: GitHub](https://github.com/uazo/cromite/releases/latest)

</details>

</div>

### Firefox

Essas opções podem ser encontradas em :material-menu: → **Configurações** → **Privacidade  Segurança**.

#### Dados de navegação

- [x] Selecione **Fechar guias ao sair**

#### Modo incógnito (navegação "anônima")

- [x] Selecione **Abrir links externos no modo de navegação anônima**

#### Segurança

- [x] Selecione **Sempre usar conexões seguras**

Isso impede que você se conecte involuntariamente a um site usando HTTP em texto simples. Sites sem HTTPS são raros hoje em dia, portanto, isso deve ter pouco ou nenhum impacto na sua navegação diária.

#### Configurações do AdBlock Plus

Essas opções podem ser encontradas em :material-menu:/:gear: → **Settings** → **Search engines**.

O Cromite contém uma versão personalizada do Adblock Plus com o EasyList ativado por padrão, bem como opções para selecionar mais listas de filtros no menu **Listas de filtros**.

Utilizar listas complementares fará com que sua máquina se destaque na rede em relação aos outros usuários do Brave e pode aumentar as chances de ataque se houver uma vulnerabilidade no Brave ou uma regra maliciosa estiver presente em uma das listas que você utiliza.

- \[x\] (Opcional) Selecione **Enable anti-circumvention and snippets (Ativar anti-circunvenção e trechos**)

Essa configuração adiciona uma lista adicional do Adblock Plus que pode aumentar a eficácia do bloqueio de conteúdo da Cromite. Aplicam-se os avisos sobre permanência e potencialmente aumento da superfície de ataque.

#### Configurações antigas do Adblock

Essas opções podem ser encontradas em :material-menu:/:gear: → **Settings** → **Search engines**.

- [ ] Desmarque a configuração de atualização automática

Isso desativa as verificações de atualização do filtro de bloqueio de anúncios Bromite não atualizado.

## Safari (iOS)

No iOS, qualquer aplicativo que possa navegar na Web está [restrito](https://developer.apple.com/app-store/review/guidelines) ao uso de uma [estrutura WebKit](https://developer.apple.com/documentation/webkit) fornecida pela Apple, portanto, um navegador como o [Brave](#brave) não usa o mesmo mecanismo utilizado no Chromium assim seus equivalentes em outros sistemas operacionais como aparelhos Android.

<div class="admonition recommendation" markdown>

![Logotipo do Safari](assets/img/browsers/safari.svg){ align=right }

O **Safari** é o navegador padrão no iOS. Inclui [recursos de privacidade](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/ios), como [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention), guias de Navegação Privada isoladas e independentes, proteção ao rastreamento de impressões digitais (apresentando uma versão simplificada da configuração do sistema para sites, de modo que mais dispositivos pareçam idênticos) e randomização de 'impressão digital', bem como Private Relay para aqueles com uma assinatura paga do iCloud+.

[:octicons-home-16: Homepage](https://apple.com/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/data/en/safari){ .card-link title="Política de privacidade" }
[:octicons-info-16:](https://support.apple.com/guide/iphone/browse-the-web-iph1fbef4daa/ios){ .card-link title="Documentação" }

</details>

</div>

### Configurações recomendadas para o Safari

O [AdGuard](browser-extensions.md#adguard) é o programa recomendado se você quiser um **bloqueador de conteúdo** no Safari.

As seguintes opções relacionadas à privacidade/segurança podem ser encontradas em :gear: **Preferências** → **Apps** → **Safari**.

#### Permitir que o Safari acesse

Em **Siri**:

- [Desativar **o Learn deste aplicativo**
- [ ] Desativar **Mostrar no Aplicativo**
- [Desativar **Mostrar na tela inicial**
- [Desativar **o aplicativo Suggest**

Isso impede que a Siri use o conteúdo do Safari para sugestões da Siri.

#### Pesquisa

- [Desativar **Sugestões de mecanismo de busca**

Essa configuração envia tudo o que você digita na barra de endereços para o mecanismo de busca definido no Safari. Desativar as sugestões de pesquisa permite que você controle com mais precisão quais dados são enviados ao seu provedor de mecanismo de pesquisa.

#### Perfis

O Safari permite que você separe as seções de navegação em perfis diferentes. Seus seus cookies, histórico e dados do site são salvos separadamente em cada  perfil. Você deve usar perfis diferentes para finalidades diferentes, por exemplo: compras, trabalho, faculdade.

#### Privacidade & Segurança

- [x] Ativar **prevenção de rastreamento entre sites**

Ativa [a Proteção de Rastreamento Inteligente](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp) do WebKit. O recurso ajuda a proteger contra o rastreamento indesejado, usando o aprendizado de máquina no dispositivo para impedir os rastreadores. O ITP lhe protegerá contra uma gama de ameaças ameaças comuns, mas não bloqueia todas as vias de rastreamento porque foi projetado para não interferir na usabilidade do site.

- [x] Habilitar **Exigir Face ID/Touch ID para desbloquear a navegação privada**

Essa configuração permite bloquear suas guias privadas com biometria/PIN quando não estiverem em uso.

- [Desativar **Aviso de site fraudulento**

Essa configuração usa o Google Safe Browsing (ou Tencent Safe Browsing no caso de usuários da China continental ou de Hong Kong) para protegê-lo durante a navegação. Dessa maneira, o seu endereço IP pode ser registrado pelo seu provedor de navegação segura. Desabilitar essa configuração desativará esse registro, mas você poderá ficar mais vulnerável a sites de *phishing* conhecidos.

- [x] Ativar **Aviso de Conexão não segura**

Essa opção emoite um aviso caso sua conexão não estiver usando HTTPS. O seu navegador Safari tentará automaticamente atualizar o site para HTTPS, portanto, você só verá essa mensagem quando não houver uma conexão HTTPS disponível.

- [Desativar **Highlights**

A política de privacidade da Apple para o Safari afirma:

> Durante a navegação o Safari pode enviar informações calculadas a partir do endereço da página para a Apple via OHTTP para determinar se há destaques relevantes disponíveis.

#### Configurações para sites

Em **Câmera**

- [x] Selecione **Perguntar**

Sob o **microfone**

- [x] Selecione **Perguntar**

Sob a **Serviços de localização**

- [x] Selecione **Perguntar**

Essas configurações garantem que os sites só possam acessar sua câmera, seu microfone ou sua localização depois que você lhes conceder permissão.

#### Outras configurações de privacidade

Essa opção pode ser encontrada em :gear: **Settings** → **Aplicativos** → **Safari** → **Geral** → **Downloads**.

##### Redução da coleta de 'impressões digitais'

A configuração **Advanced Tracking and Fingerprinting Protection (Proteção Avançada contra Rastreamento e Impressão Digital)**  tornará determinados valores aleatórios para dificultar a obtenção de suas 'impressões digitais':

- [x] Selecione **All Browsing (Toda a navegação** ) ou **Private Browsing (Navegação privada)**

##### Medição de anúncios com preservação da privacidade

- [ ] Desativar **Privacy Preserving Ad Measurement**

A medição de cliques em anúncios tem usado tradicionalmente uma tecnologia de rastreamento que viola a privacidade do usuário. [A medição de cliques privados](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm) é um recurso do WebKit e um padrão da Web proposto com o objetivo de permitir que os anunciantes meçam a eficácia das campanhas na Web sem comprometer a privacidade do usuário.

O recurso tem poucas preocupações com a privacidade por si só, portanto, embora você possa optar por deixá-lo ativado, consideramos o fato de que ele é automaticamente desativado na Navegação privada como um indicador para desativar o recurso.

#### Navegação privada ativa permanenetemente

Abra o Safari e toque no botão Tabs, localizado no canto inferior direito. Em seguida, expanda a lista :material-format-list-bulleted: Tab Groups.

- [x] Selecionar **Privado**

O modo de navegação privada do Safari ofereçe proteção adicional à sua privacidade A navegação privada inicia uma nova sessão [efêmera](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) para cada guia, o que significa que as guias são completamente isoladas umas das outras. Existem outros benefícios menores em se utilizar a navegação privada como não compartilhar com a Apple quando se utiliza o serviço de tradução.

Observe que a navegação privada não salva cookies e dados de sites, portanto, não será possível permanecer conectado ou logado a sites. Isso pode ser um inconveniente em determinadas situações.

#### Sincronização do iCloud

A sincronização do histórico do Safari, bem como os Grupos de Abas e senhas salvas estão resguardadas por E2EE. No entanto, por padrão, os marcadores (bookmarks) [não estão](https://support.apple.com/HT202303) protegidos. A Apple pode descriptografar e acessá-los de acordo com sua [política de privacidade](https://apple.com/legal/privacy/en-ww).

Você pode habilitar o EE2E para seus favoritos no navegador Safari ao ativar a [ Proteção Avançada de Dados](https://support.apple.com/HT212520). Acesse :gear: **Configurações** → **iCloud** → **Proteção Avançada de Dados**.

- [x] Ative **Proteção de Dados Avançados**

Se você usar o iCloud com a proteção avançada de dados, também é recomendado mudar a localização da pasta padrão de seus arquivos descarregados (downloads). Essa opção pode ser encontrada em :gear: **Settings** → **Aplicativos** → **Safari** → **Geral** → **Downloads**.

## Critérios

<0>Por favor, note que não somos parceiros de nenhum dos produtos que recomendamos.</0>Em adição aos <1>nossos critérios básicos</1>, desenvolvemos um conjunto claro de requisitos para nos permitir fornecer recomendações objetivas. Sugerimos que você se familiarize com essa lista antes de escolher uma alternativa para usar e pesquise e se informe por conta própria para garantir que essa é a escolha ideal.

### Requisitos mínimos

- Deve suportar atualizações automáticas.
- Necessita ser provido de atualizações para novas versões constantemente.
- É obrigatorio o suporte à bloqueio de conteúdo (indesejável).
- Qualquer mudança necessária para tornar o navegador mais compatível com a privacidade não deve afetar negativamente a experiência do usuário.
