---
meta_title: "Navegadores para Android e iOS que respeitam a privacidade - Privacy Guides"
title: "Navegadores para dispositivos móveis"
icon: material/cellphone-information
description: Estes navegadores são os que recomendamos atualmente para a navegação normal/não anónima na Internet no seu telemóvel.
cover: mobile-browsers.png
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Recomendações de navegadores privados para dispositivos móveis
    url: "./"
    relatedLink: "../desktop-browsers/"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Bromite
    image: /assets/img/browsers/brave.svg
    url: https://brave.com
    applicationCategory: Web Browser
    operatingSystem:
      - Android
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Origem do uBlock
    image: /assets/img/browsers/safari.svg
    url: https://www.apple.com/safari/
    applicationCategory: Web Browser
    operatingSystem:
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
---

Estes são os navegadores para dispositivos móveis e as configurações atualmente recomendados para a navegação normal/não anónima na Internet. Se precisar de navegar anonimamente na Internet, deve utilizar o [Tor](tor.md). Em geral, recomendamos que a utilização de extensões seja reduzida ao mínimo; têm acesso privilegiado no seu browser, exigem que confie no programador, podem fazer com que se destaque [](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)e [enfraquecem o isolamento do site](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ).

## Android

No Android, o Firefox continua a ser menos seguro do que as alternativas baseadas no Chromium: o motor da Mozilla, [GeckoView](https://mozilla.github.io/geckoview/), ainda não suporta [o isolamento de sites](https://hacks.mozilla.org/2021/05/introducing-firefox-new-site-isolation-security-architecture) nem ativa [isolatedProcess](https://bugzilla.mozilla.org/show_bug.cgi?id=1565196).

### Brave

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo Brave](assets/img/browsers/brave.svg){ align=right }
    
    O **Brave** inclui um bloqueador de conteúdos incorporado e [funcionalidades de privacidade] (https://brave.com/privacy-features/), muitas das quais estão ativadas por predefinição.
    
    Inclui [características de privacidade](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/15.0/ios/15.0), tais como Proteção de Rastreamento Inteligente, Relatório de Privacidade, abas isoladas de Navegação Privada, iCloud Private Relay, e atualizações automáticas de HTTPS.
    
    [:octicons-home-16: Homepage](https://brave.com/){ .md-button .md-button--primary }
    [:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Serviço Onion" }
    [:octicons-eye-16:](https://brave.com/privacy/browser/){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://support.brave.com/){ .card-link title=Documentação}
    [:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Código-fonte" }
    
    ??? downloads anotar
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
        - [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)

#### Configuração recomendada

O Tor é a única forma de navegar verdadeiramente de forma anónima na Internet. Quando utilizar o Brave, recomendamos que altere as seguintes definições para proteger a sua privacidade de determinadas entidades terceiras. Contudo, todos os browsers, com a exceção do [Tor](tor.md#tor-browser) serão rastreáveis por *alguém* de uma forma ou de outra.

Estas opções podem ser encontradas em :material-menu: → **Definições** → **Proteção do Brave & privacidade**

##### Proteções

A Brave inclui algumas medidas de bloqueio de impressão digital na sua funcionalidade [Proteção](https://support.brave.com/hc/en-us/articles/360022973471-What-is-Shields-). Sugerimos que configure estas opções [globalmente](https://support.brave.com/hc/en-us/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings-) em todas as páginas que visitar.

##### Predefinições globais das proteções do Brave

As opções de proteção podem ser revogadas por cada site, de acordo com as necessidades, mas por predefinição recomendamos as seguintes definições:

<div class="annotate" markdown>

- [x] Selecione **Agressivo** em Rastreadores e bloqueio de anúncios

    ??? aviso "Use listas de filtro por padrão"
        O Brave permite-lhe selecionar filtros de conteúdo adicional na página interna `brave://adblock`. Aconselhamos a não utilizar esta funcionalidade; em vez disso, mantenha as listas de filtros predefinidas. A utilização de listas extra fará com que se destaque dos outros utilizadores do Brave e pode também aumentar a superfície de ataque se houver uma vulnerabilidade no Brave e uma regra maliciosa for adicionada a uma das listas que utiliza.

- [x] Selecione **Atualizar as ligações para HTTPS**
- [x] Selecione **Utilizar sempre ligações seguras**
- [x] (Opcional) Selecionar **Bloquear scripts** (1)
- [x] na opção Bloquear impressão digital, selecionar **Estrito, pode causar problemas nos sites**

</div>

1. Esta opção disponibiliza uma funcionalidade semelhante aos modos de bloqueio avançados do uBlock Origin [](https://github.com/gorhill/uBlock/wiki/Blocking-mode) ou à extensão [NoScript](https://noscript.net/).

##### Limpar dados de navegação

- [x] Selecionar **Limpar dados ao sair**

##### Bloqueio de redes sociais

- [ ] Desmarcar todos os componentes das redes sociais

##### Outras definições de privacidade

<div class="annotate" markdown>

- [x] Selecione **Desativar UDP não-proxy**, em [Política de utilização WebRTC IP](https://support.brave.com/hc/en-us/articles/360017989132-How-do-I-change-my-Privacy-Settings-#webrtc)
- [ ] Desative **Permitir aos sites verificar as suas opções de pagamento**
- [ ] Desative **IPFS Gateway** (1)
- [x] Selecione **Fechar tabs ao sair**
- [ ] Desative **Permitir análises de produtos que preservam a privacidade (P3A)**
- [ ] Desative **Enviar relatórios de diagnóstico automaticamente**
- [ ] Desative **Enviar automaticamente ping de utilização diária para a Brave**

</div>

1. O InterPlanetary File System (IPFS) é uma rede descentralizada, peer-to-peer, para armazenar e partilhar dados num sistema de ficheiros distribuído. A menos que utilize a funcionalidade, desative-a.

#### Sincronização do Brave

[A Sincronização do Brave](https://support.brave.com/hc/en-us/articles/360059793111-Understanding-Brave-Sync) permite que os seus dados de navegação (histórico, marcadores, etc.) estejam acessíveis em todos os seus dispositivos, sem necessidade de uma conta, e protege-os com E2EE.

## iOS

No iOS, qualquer aplicação que possa navegar na Web está [limitada](https://developer.apple.com/app-store/review/guidelines) à utilização de uma estrutura WebKit fornecida pela Apple [](https://developer.apple.com/documentation/webkit), pelo que não há nenhuma vantagem em utilizar um navegador diferente de outro fornecedor.

### Safari

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo Safari](assets/img/browsers/safari.svg){ align=right }
    
    O **Safari** é o navegador predefinido no iOS. Inclui [funcionalidades de privacidade] (https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/15.0/ios/15.0), tais como [Previsão inteligente de rastreio] (https://webkit.org/blog/7675/intelligent-tracking-prevention/), Relatório de Privacidade, separadores de navegação privada isolados e efémeros, iCloud Private Relay e redução de impressões digitais, através da apresentação de uma versão simplificada da configuração do sistema aos sites, para que o miro número possível de dispositivos pareçam idênticos.
    
    [:octicons-home-16: Homepage](https://www.apple.com/safari/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.apple.com/legal/privacy/data/en/safari/){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://support.apple.com/guide/safari/welcome/mac){ .card-link title=Documentação}

#### Configuração recomendada

Estas opções podem ser encontradas em :gear: **Definições** → **Safari** → **Privacidade e segurança**.

##### Prevenção de rastreio entre sites

- [x] Ativar **Prevenir o rastreio entre sites**

Isto liga a [Proteção Inteligente de Rastreio da WebKit](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp). A funcionalidade ajuda a proteger contra o rastreio indesejado, utilizando a aprendizagem automática no dispositivo para impedir os rastreadores. A ITP contra a monitorização protege-o contra muitas ameaças comuns, mas não bloqueia todos os modos de rastreio, uma vez que foi concebida para ter um impacto mínimo ou nulo na usabilidade do site.

##### Relatório de Privacidade

O Relatório de Privacidade fornece uma foto de rastreadores entre sites atualmente impedidos de criar perfis no site que está a visitar. Também pode exibir um relatório semanal para mostrar quais rastreadores foram bloqueados ao longo do tempo.

O Relatório de Privacidade é acessível através do menu de Configurações.

##### Medidor de Anúncios Respeitador de Privacidade

- [ ] Desativar **Medidor de Anúncios Respeitador de Privacidade**

A medição de clique em anúncios tem usado tradicionalmente a tecnologia de rastreamento que viola a privacidade do utilizador. A [Medição de Clique Privado](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm/) é um recurso de WebKit e um padrão proposto para permitir que anunciantes meçam a eficácia de campanhas na web sem comprometer a privacidade do utilizador.

A funcionalidade tem poucas preocupações de privacidade por si só, então enquanto pode optar por deixá-lo ligado, nós consideramos que ele é automaticamente desativado na navegação privativa como um indicador para desativar o recurso.

##### Navegação Privada sempre-ativa

Abra o Safari e clique no botão Abas, localizado na parte inferior direita. Depois, expanda a lista de Grupos de Abas.

- [x] Selecione **Privado**

O modo de Navegação Privada do Safari oferece adicionais proteções de privacidade. A Navegação Privada usa uma nova sessão [efémera](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) para cada aba, o que significa que as abas estão isoladas uma da outra. Também há outras vantagens pequenas em privacidade com a Navegação Privada, como não enviar o endereço de página de web à Apple quando usar a funcionalidade de tradução do Safari.

Tenha em atenção que a Navegação Privada não guarda cookies e dados de sítios Web, pelo que não será possível permanecer ligado a sítios. Isto pode ser uma inconveniência.

##### Sincronização iCloud

A sincronização do histórico do Safari, grupos de separadores, separadores do iCloud e palavras-passe guardadas são E2EE. No entanto, por predefinição, os marcadores não [são](https://support.apple.com/en-us/HT202303). A Apple pode desencriptá-los e aceder-lhes segundo a sua [política de privacidade](https://www.apple.com/legal/privacy/en-ww/).

Pode ativar o E2EE para os seus favoritos e transferências do Safari ativando a [Proteção Avançada de Dados](https://support.apple.com/en-us/HT212520). Aceda ao seu **Nome de ID Apple → iCloud → Proteção de Dados Avançada**.

- [x] Ligue a **Proteção de Dados Avançada**

Se utilizar o iCloud com a Proteção Avançada de Dados desativada, também recomendamos que verifique se a localização de transferência predefinida do Safari está definida para localmente no seu dispositivo. Esta opção pode ser encontrada em :gear: **Definições** → **Safari** → **General** → **Transferências**.

### AdGuard

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo do AdGuard](assets/img/browsers/adguard.svg){ align=right }
    
    O **AdGuard para iOS** é uma extensão de bloqueio de conteúdos gratuita e de código aberto para o Safari que utiliza a [Content Blocker API] nativa (https://developer.apple.com/documentation/safariservices/creating_a_content_blocker).
    
    O AdGuard para iOS tem algumas funcionalidades premium; no entanto, o bloqueio de conteúdos normal do Safari é gratuito.
    
    [:octicons-home-16: Página Inicial](https://adguard.com/pt_pt/adguard-ios/overview.html){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://adguard.com/pt_pt/privacy/ios.html){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://kb.adguard.com/ios){ .card-link title=Documentação}
    [:octicons-code-16:](https://github.com/AdguardTeam/AdguardForiOS){ .card-link title="Código fonte" }
    ??? transferências
    
        - [:simple-appstore: App Store](https://apps.apple.com/app/apple-store/id1047223162)

As listas de filtros adicionais tornam as coisas mais lentas e podem aumentar a sua superfície de ataque, por isso aplique apenas o necessário.

## Framadate

**Por favor, note que não somos afiliados a nenhum dos projetos que recomendamos.** Para além dos [nossos critérios padrões](about/criteria.md), desenvolvemos um conjunto claro de requisitos que nos permitem fornecer recomendações objetivas. Sugerimos que se familiarize com esta lista antes de optar por utilizar um projeto e que faça a sua própria investigação para garantir que é a escolha certa para si.

!!! Considere o auto-hospedagem para mitigar esta ameaça.

    ![logo PrivateBin](/assets/img/productivity/privatebin.svg){ align=right }
    
    **PrivateBin** é um pastebin online minimalista e de código aberto onde o servidor tem zero conhecimento de dados colados. Os dados são criptografados/descriptografados no navegador usando AES de 256 bits. Psono suporta compartilhamento seguro de senhas, arquivos, marcadores e e-mails.

### Requisitos Mínimos

- Deve suportar atualizações automáticas.
- Deve receber atualizações do motor em 0-1 dias a partir do lançamento do upstream.
- Quaisquer alterações necessárias para tornar o browser mais respeitador da privacidade não devem afetar negativamente a experiência do utilizador.
- Os navegadores Android têm de utilizar o motor Chromium.
    - Infelizmente, o Mozilla GeckoView continua menos seguro do que o Chromium no Android.
    - Os navegadores iOS estão limitados ao WebKit.

### Critérios das Extensões

- Não deve replicar a funcionalidade incorporada do browser ou do sistema operativo.
- Deve ter um impacto direto na privacidade do utilizador, ou seja, não deve limitar-se a fornecer informações.
