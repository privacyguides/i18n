---
meta_title: "Browsers para Android e iOS que respeitam a privacidade - Privacy Guides"
title: "Browsers para dispositivos móveis"
icon: material/cellphone-information
description: Estes browsers são os que recomendamos atualmente para a navegação normal/não anónima na Internet no seu telemóvel.
cover: mobile-browsers.png
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Recomendações de browsers privados para dispositivos móveis
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

Estes são os browsers para dispositivos móveis e as configurações atualmente recomendados para a navegação normal/não anónima na Internet. Se precisar de navegar anonimamente na Internet, deve utilizar o [Tor](tor.md). Em geral, recomendamos que a utilização de extensões seja reduzida ao mínimo; têm acesso privilegiado no seu browser, exigem que confie no programador, podem fazer com que se destaque [](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)e [enfraquecem o isolamento do site](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ).

## Android

No Android, o Firefox continua a ser menos seguro do que as alternativas baseadas no Chromium: o motor da Mozilla, [GeckoView](https://mozilla.github.io/geckoview/), ainda não suporta [o isolamento de sites](https://hacks.mozilla.org/2021/05/introducing-firefox-new-site-isolation-security-architecture) nem ativa [isolatedProcess](https://bugzilla.mozilla.org/show_bug.cgi?id=1565196).

### Brave

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo Brave](assets/img/browsers/brave.svg){ align=right }
    
    O **Braver** inclui um bloqueador de conteúdos incorporado e [funcionalidades de privacidade] (https://brave.com/privacy-features/), muitas das quais estão ativadas por predefinição.
    
    O Brave foi criado com base no projeto do Chromium, pelo que deve ser familiar a muita gente e não deve grandes problemas de compatibilidade com sites.
    
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

    ??? aviso "Use listas de filtro padrão"
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

No iOS, qualquer aplicação que possa navegar na Web está [limitada](https://developer.apple.com/app-store/review/guidelines) à utilização de uma estrutura WebKit fornecida pela Apple [](https://developer.apple.com/documentation/webkit), pelo que não há nenhuma vantagem em utilizar um browser diferente de outro fornecedor.

### Safari

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo Safari](assets/img/browsers/safari.svg){ align=right }
    
    O **Safari** é o browser predefinido no iOS. Inclui [funcionalidades de privacidade] (https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/15.0/ios/15.0), tais como [Previsão inteligente de rastreio] (https://webkit.org/blog/7675/intelligent-tracking-prevention/), Relatório de Privacidade, separadores de navegação privada isolados e efémeros, iCloud Private Relay e redução de impressões digitais, através da apresentação de uma versão simplificada da configuração do sistema aos sites, para que o miro número possível de dispositivos pareçam idênticos.
    
    O Safari está limitado a dispositivos Apple e está coberto pela [Proteção de Integridade do Sistema] (https://support.apple.com/guide/security/system-integrity-protection-secb7ea06b49/web), uma funcionalidade de segurança que faz com que os programas e ficheiros do sistema sejam apenas de leitura, para que não possam ser alterados por si ou por malware.
    
    [:octicons-home-16: Homepage](https://www.apple.com/safari/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.apple.com/legal/privacy/data/en/safari/){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://support.apple.com/guide/safari/welcome/mac){ .card-link title=Documentação}

#### Configuração recomendada

Estas opções podem ser encontradas em :gear: **Definições** → **Safari** → **Privacidade e segurança**.

##### Prevenção de rastreio entre sites

- [x] Ativar **Prevenir o rastreio entre sites**

This enables WebKit's [Intelligent Tracking Protection](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp). The feature helps protect against unwanted tracking by using on-device machine learning to stop trackers. ITP protects against many common threats, but it does not block all tracking avenues because it is designed to not interfere with website usability.

##### Privacy Report

Privacy Report provides a snapshot of cross-site trackers currently prevented from profiling you on the website you're visiting. It can also display a weekly report to show which trackers have been blocked over time.

Privacy Report is accessible via the Page Settings menu.

##### Privacy Preserving Ad Measurement

- [ ] Disable **Privacy Preserving Ad Measurement**

Ad click measurement has traditionally used tracking technology that infringes on user privacy. [Private Click Measurement](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm/) is a WebKit feature and proposed web standard aimed towards allowing advertisers to measure the effectiveness of web campaigns without compromising on user privacy.

The feature has little privacy concerns on its own, so while you can choose to leave it on, we consider the fact that it's automatically disabled in Private Browsing to be an indicator for disabling the feature.

##### Always-on Private Browsing

Open Safari and tap the Tabs button, located in the bottom right. Then, expand the Tab Groups list.

- [x] Select **Private**

Safari's Private Browsing mode offers additional privacy protections. Private Browsing uses a new [ephemeral](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) session for each tab, meaning tabs are isolated from one another. There are also other smaller privacy benefits with Private Browsing, such as not sending a webpage’s address to Apple when using Safari's translation feature.

Do note that Private Browsing does not save cookies and website data, so it won't be possible to remain signed into sites. This may be an inconvenience.

##### iCloud Sync

Synchronization of Safari History, Tab Groups, iCloud Tabs and saved passwords are E2EE. However, by default, bookmarks are [not](https://support.apple.com/en-us/HT202303). Apple can decrypt and access them in accordance with their [privacy policy](https://www.apple.com/legal/privacy/en-ww/).

You can enable E2EE for you Safari bookmarks and downloads by enabling [Advanced Data Protection](https://support.apple.com/en-us/HT212520). Go to your **Apple ID name → iCloud → Advanced Data Protection**.

- [x] Turn On **Advanced Data Protection**

If you use iCloud with Advanced Data Protection disabled, we also recommend checking to ensure Safari's default download location is set to locally on your device. This option can be found in :gear: **Settings** → **Safari** → **General** → **Downloads**.

### AdGuard

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![AdGuard logo](assets/img/browsers/adguard.svg){ align=right }
    
    **AdGuard for iOS** is a free and open-source content-blocking extension for Safari that uses the native [Content Blocker API](https://developer.apple.com/documentation/safariservices/creating_a_content_blocker).
    
    AdGuard for iOS has some premium features; however, standard Safari content blocking is free of charge.
    
    [:octicons-home-16: Homepage](https://adguard.com/en/adguard-ios/overview.html){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://adguard.com/privacy/ios.html){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://kb.adguard.com/ios){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/AdguardTeam/AdguardForiOS){ .card-link title="Source Code" }
    
    ??? downloads
    
        - [:simple-appstore: App Store](https://apps.apple.com/app/apple-store/id1047223162)

Additional filter lists do slow things down and may increase your attack surface, so only apply what you need.

## Framadate

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

!!! Considere o auto-hospedagem para mitigar esta ameaça.

    ![logo PrivateBin](/assets/img/productivity/privatebin.svg){ align=right }
    
    **PrivateBin** é um pastebin online minimalista e de código aberto onde o servidor tem zero conhecimento de dados colados. Os dados são criptografados/descriptografados no navegador usando AES de 256 bits. Psono suporta compartilhamento seguro de senhas, arquivos, marcadores e e-mails.

### Minimum Requirements

- Must support automatic updates.
- Must receive engine updates in 0-1 days from upstream release.
- Any changes required to make the browser more privacy-respecting should not negatively impact user experience.
- Android browsers must use the Chromium engine.
    - Unfortunately, Mozilla GeckoView is still less secure than Chromium on Android.
    - iOS browsers are limited to WebKit.

### Extension Criteria

- Must not replicate built-in browser or OS functionality.
- Must directly impact user privacy, i.e. must not simply provide information.
