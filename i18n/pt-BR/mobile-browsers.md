---
meta_title: "Privacy Respecting Web Browsers for Android and iOS - Privacy Guides"
title: "Navegadores Móveis"
icon: material/cellphone-information
description:
cover: mobile-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name:
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

Essa é a lista de <0>navegadores móveis</0> recomendados para o acesso padrão/não-anônimo da internet em seu smartphone ou tablet Se você precisa navegar pela internet anonimamente, você deve usar o [Tor](tor.md).

## Brave

<div class="admonition recommendation" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

O **Brave Browser** inclui um bloqueador de conteúdo embutido e [recursos de privacidade](https://brave.com/privacy-features/), os quais muitos são ativados por padrão.

O Brave foi construído com base no projeto de navegador Chromium, seu funcionamento pode ser familiar e ter mínimos problemas de compatibilidade em websites.

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

    - [x] Select **Aggressive** under *Block trackers & ads*
    - [x] Select **Auto-redirect AMP pages**
    - [x] Select **Auto-redirect tracking URLs**
    - [x] Select **Require all connections to use HTTPS (strict)** under *Upgrade connections to HTTPS*
    - \[x\] (Optional) Select **Block Scripts** (1)
    - [x] Select **Block third-party cookies** under *Block Cookies*
    - [x] Select **Block Fingerprinting**
    - [x] Select **Prevent fingerprinting via language settings**

    <details class="warning" markdown>
    <summary>Use default filter lists</summary>

    Brave allows you to select additional content filters within the **Content Filtering** menu or the internal `brave://adblock` page. We advise against using this feature; instead, keep the default filter lists. Using extra lists will make you stand out from other Brave users and may also increase attack surface if there is an exploit in Brave and a malicious rule is added to one of the lists you use.

    </details>

    - [x] Select **Forget me when I close this site**

    </div>

    1. Essa opção desabilita o JavaScript, o que interromperá muitos sites. To unbreak them, you can set exceptions on a per-site basis by tapping on the Shield icon in the address bar and unchecking this setting under *Advanced controls*.

=== "iOS"

    <div class="annotate" markdown>

    - [x] Select **Aggressive** under *Trackers & Ads Blocking*
    - [x] Select **Strict** under *Upgrade Connections to HTTPS*
    - [x] Select **Auto-Redirect AMP pages**
    - [x] Select **Auto-Redirect Tracking URLs**
    - \[x\] (Optional) Select **Block Scripts** (1)
    - [x] Select **Block Fingerprinting**
    - [x] Select **Site Tabs Closed** under *Auto Shred*

    <details class="warning" markdown>
    <summary>Use default filter lists</summary>

    Brave allows you to select additional content filters within the **Content Filtering** menu. We advise against using this feature; instead, keep the default filter lists. Using extra lists will make you stand out from other Brave users and may also increase attack surface if there is an exploit in Brave and a malicious rule is added to one of the lists you use.

    </details>

    </div>

    1. Essa opção desabilita o JavaScript, o que interromperá muitos sites. Para desbloqueá-los, você pode definir exceções por site clicando no ícone do Shields na barra de endereços e desmarcando essa configuração em *Controles avançados*.

##### Clear browsing data (Android only)

- [x] Select **Clear data on exit**

##### Social Media Blocking (Android only)

- [ ] Uncheck all social media components

#### Other privacy settings

=== "Android"

    <div class="annotate" markdown>

    - [x] Select **Disable non-proxied UDP** under [*WebRTC IP handling policy*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
    - \[x\] (Optional) Select **No protection** under *Safe Browsing* (1)
    - [ ] Uncheck **Allow sites to check if you have payment methods saved**
    - [ ] Uncheck **V8 Optimizer** under *Manage V8 security*
    - [x] Select **Close tabs on exit**
    - [ ] Desmarque **Permitir análise de produtos com preservação da privacidade (P3A)**
    - [ ] Desmarque **Automaticamente enviar relatórios de diagnóstico**
    - [ ] Desmarque **Automaticamente enviar ping de uso diário para Brave**

    </div>

    1. A [implementação do Safe Browsing](https://support.brave.com/hc/en-us/articles/15222663599629-Safe-Browsing-in-Brave) da Brave no Android **não faz** proxy de [solicitações de rede do Safe Browsing](https://developers.google.com/safe-browsing/v4/update-api#checking-urls) como sua contraparte de desktop. Isso significa que o seu endereço IP pode ser descoberto (e registrado) pelo Google. Note que a Navegação segura não está disponível para dispositivos Android sem o Google Play Services.

=== "iOS"

    - [ ] Desmarque **Permitir análise de produtos com preservação da privacidade (P3A)**
    - [ ] Desmarque **Automaticamente enviar ping de uso diário para Brave**

#### Leo

These options can be found in :material-menu: → **Settings** → **Leo**.

<div class="annotate" markdown>

- [ ] Uncheck **Show autocomplete suggestions in address bar** (1)

</div>

1. Essa opção não está presente no aplicativo iOS do Brave.

#### Mecanismo de busca

Essas opções podem ser encontradas em :material-menu:/:fontawesome-solid-ellipsis: → **Settings** → **Search engines**.

- [ ] Desmarque **Mostrar sugestões de pesquisa**

#### Sincronização do Brave

O [Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) permite que os seus dados de navegação (histórico, marcadores, etc.) sejam acessíveis em todos os seus dispositivos sem necessidade de uma conta e protege-os com E2EE.

## Cromite (Android)

<div class="admonition recommendation" markdown>

![Cromite logo](assets/img/browsers/cromite.svg){ align=right }

**Cromite** is a Chromium-based browser with built-in ad blocking, fingerprinting protections, and other [privacy and security enhancements](https://github.com/uazo/cromite/blob/master/docs/FEATURES.md). It is a fork of the discontinued **Bromite** browser.

[:octicons-home-16: Homepage](https://cromite.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/uazo/cromite/blob/master/docs/PRIVACY_POLICY.md){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/uazo/cromite?tab=readme-ov-file#docs){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/uazo/cromite){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-android: F-Droid](https://cromite.org/fdroid/repo/?fingerprint=49F37E74DEE483DCA2B991334FB5A0200787430D0B5F9A783DD5F13695E9517B)
- [:simple-github: GitHub](https://github.com/uazo/cromite/releases/latest)

</details>

</div>

### Firefox

These options can be found in :material-menu: → :gear: **Settings** → **Privacy and security**.

#### Browsing data

- [x] Select **Close all open tabs on exit**

#### Incognito mode

- [x] Select **Open external links in incognito**

#### Segurança

- [x] Select **Always use secure connections**

This prevents you from unintentionally connecting to a website in plain-text HTTP. HTTP is extremely uncommon nowadays, so this should have little to no impact on your day-to-day browsing.

#### Adblock Plus settings

These options can be found in :material-menu: → :gear: **Settings** → **Adblock Plus settings**.

Cromite contains a customized version of Adblock Plus with EasyList enabled by default, as well as options to select more filter lists within the **Filter lists** menu.

Using extra lists will make you stand out from other Cromite users and may also increase attack surface if a malicious rule is added to one of the lists you use.

- \[x\] (Optional) Select **Enable anti-circumvention and snippets**

This setting adds an additional Adblock Plus list that may increase the effectiveness of Cromite's content blocking. The warnings about standing out and potentially increasing attack surface apply.

#### Legacy Adblock settings

These options can be found in :material-menu: → :gear: **Settings** → **Legacy Adblock settings**.

- [ ] Uncheck the autoupdate setting

This disables update checks for the unmaintained Bromite adblock filter.

## Safari (iOS)

On iOS, any app that can browse the web is [restricted](https://developer.apple.com/app-store/review/guidelines) to using an Apple-provided [WebKit framework](https://developer.apple.com/documentation/webkit), so a browser like [Brave](#brave) does not use the Chromium engine like its counterparts on other operating systems.

<div class="admonition recommendation" markdown>

![Safari logo](assets/img/browsers/safari.svg){ align=right }

**Safari** is the default browser in iOS. It includes [privacy features](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/ios) such as [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention), isolated and ephemeral Private Browsing tabs, fingerprinting protection (by presenting a simplified version of the system configuration to websites, so more devices look identical), and fingerprint randomization, as well as Private Relay for those with a paid iCloud+ subscription.

[:octicons-home-16: Homepage](https://apple.com/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/data/en/safari){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.apple.com/guide/iphone/browse-the-web-iph1fbef4daa/ios){ .card-link title="Documentation" }

</details>

</div>

### Recommended Safari Configuration

We would suggest installing [AdGuard](browser-extensions.md#adguard) if you want a content blocker in Safari.

The following privacy/security-related options can be found in :gear: **Settings** → **Apps** → **Safari**.

#### Allow Safari to Access

Under **Siri**:

- [ ] Disable **Learn from this App**
- [ ] Disable **Show in App**
- [ ] Disable **Show on Home Screen**
- [ ] Disable **Suggest App**

This prevents Siri from using content from Safari for Siri suggestions.

#### Pesquisa

- [ ] Disable **Search Engine Suggestions**

This setting sends whatever you type in the address bar to the search engine set in Safari. Disabling search suggestions allows you to more precisely control what data you send to your search engine provider.

#### Profiles

Safari allows you to separate your browsing with different profiles. All of your cookies, history, and website data are separate for each profile. You should use different profiles for different purposes e.g. Shopping, Work, or School.

#### Privacidade & Segurança

- [x] Enable **Prevent Cross-Site Tracking**

This enables WebKit's [Intelligent Tracking Protection](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp). The feature helps protect against unwanted tracking by using on-device machine learning to stop trackers. ITP protects against many common threats, but does not block all tracking avenues because it is designed to not interfere with website usability.

- [x] Enable **Require Face ID/Touch ID to Unlock Private Browsing**

This setting allows you to lock your private tabs behind biometrics/PIN when not in use.

- [ ] Disable **Fraudulent Website Warning**

This setting uses Google Safe Browsing (or Tencent Safe Browsing for users in mainland China or Hong Kong) to protect you while you browse. As such, your IP address may be logged by your Safe Browsing provider. Disabling this setting will disable this logging, but you might be more vulnerable to known phishing sites.

- [x] Enable **Not Secure Connection Warning**

This setting shows a warning screen if your connection to a website isn't using HTTPS. Safari will automatically try to upgrade the site to HTTPS, so you should only see this when there is no HTTPS connection available.

- [ ] Disable **Highlights**

Apple's privacy policy for Safari states:

> When visiting a webpage, Safari may send information calculated from the webpage address to Apple over OHTTP to determine if relevant highlights are available.

#### Settings for Websites

Under **Camera**

- [x] Select **Ask**

Under **Microphone**

- [x] Select **Ask**

Under **Location**

- [x] Select **Ask**

These settings ensure that websites can only access your camera, microphone, or location after you explicitly grant them access.

#### Other Privacy Settings

These options can be found in :gear: **Settings** → **Apps** → **Safari** → **Advanced**.

##### Fingerprinting Mitigations

The **Advanced Tracking and Fingerprinting Protection** setting will randomize certain values so that it's more difficult to fingerprint you:

- [x] Select **All Browsing** or **Private Browsing**

##### Privacy Preserving Ad Measurement

- [ ] Disable **Privacy Preserving Ad Measurement**

Ad click measurement has traditionally used tracking technology that infringes on user privacy. [Private Click Measurement](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm) is a WebKit feature and proposed web standard aimed towards allowing advertisers to measure the effectiveness of web campaigns without compromising on user privacy.

The feature has little privacy concerns on its own, so while you can choose to leave it on, we consider the fact that it's automatically disabled in Private Browsing to be an indicator for disabling the feature.

#### Always-on Private Browsing

Open Safari and tap the Tabs button, located in the bottom right. Then, expand the :material-format-list-bulleted: Tab Groups list.

- [x] Select **Private**

Safari's Private Browsing mode offers additional privacy protections. Private Browsing uses a new [ephemeral](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) session for each tab, meaning tabs are isolated from one another. There are other smaller privacy benefits with Private Browsing too, such as not sending a webpage’s address to Apple when using Safari's translation feature.

Do note that Private Browsing does not save cookies and website data, so it won't be possible to remain signed in to sites. This may be an inconvenience.

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
