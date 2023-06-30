---
meta_title: "Privacy Respecting Mobile Web Browsers for Android and iOS - Privacy Guides"
title: "Mobile Browsers"
icon: material/cellphone-information
description: These browsers are what we currently recommend for standard/non-anonymous internet browsing on your phone.
cover: mobile-browsers.png
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Private Mobile Browser Recommendations
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
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Safari
    image: /assets/img/browsers/safari.svg
    url: https://www.apple.com/safari/
    applicationCategory: Web Browser
    operatingSystem:
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
---

Estes são os navegadores de celular e as configurações recomendadas atualmente para a navegação padrão/não anônima na Internet. Se você precisa navegar pela internet anonimamente, você deve usar o [Tor](tor.md). In general, we recommend keeping extensions to a minimum; they have privileged access within your browser, require you to trust the developer, can make you [stand out](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint), and [weaken](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ) site isolation.

## Android

No Android, o Firefox continua a ser menos seguro do que as alternativas baseadas no Chromium: O motor da Mozilla, [GeckoView](https://mozilla.github.io/geckoview/), ainda não suporta [isolamento de site](https://hacks.mozilla.org/2021/05/introducing-firefox-new-site-isolation-security-architecture) nem ativa [isolamento de processo (isolatedProcess)](https://bugzilla.mozilla.org/show_bug.cgi?id=1565196).

### Brave

!!! recommendation

    ![Brave logo](assets/img/browsers/brave.svg){ align=right }
    
    **Brave Browser** includes a built-in content blocker and [privacy features](https://brave.com/privacy-features/), many of which are enabled by default.
    
    Brave is built upon the Chromium web browser project, so it should feel familiar and have minimal website compatibility issues.
    
    [:octicons-home-16: Homepage](https://brave.com/){ .md-button .md-button--primary }
    [:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
    [:octicons-eye-16:](https://brave.com/privacy/browser/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://support.brave.com/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Source Code" }
    
    ??? downloads annotate
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
        - [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)

#### Firefox

O Navegador Tor é a única maneira de realmente navegar na Internet de forma anônima. Ao usar o Brave, recomendamos que você altere as seguintes configurações para proteger sua privacidade de determinadas partes, mas todos os navegadores, exceto o [Navegador Tor](tor.md#tor-browser), serão rastreáveis por *alguém* de uma forma ou de outra.

Essas opções podem ser encontradas em :material-menu: → **Configurações** → **Proteções do Brave & privacidade**

##### Shields (Escudos)

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/en-us/articles/360022973471-What-is-Shields-) feature. We suggest configuring these options [globally](https://support.brave.com/hc/en-us/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings-) across all pages that you visit.

##### Brave shields global defaults

As opções do Shields (Escudos) podem ser reduzidas de acordo com o site, conforme necessário, mas, por padrão, recomendamos configurar o seguinte:

<div class="annotate" markdown>

- [x] Select **Agressivo** em Bloquear rastreadores e anúncios

    ??? warning "Use default filter lists"
        Brave allows you to select additional content filters within the internal `brave://adblock` page. We advise against using this feature; instead, keep the default filter lists. Using extra lists will make you stand out from other Brave users and may also increase attack surface if there is an exploit in Brave and a malicious rule is added to one of the lists you use.

- [x] Select **Upgrade connections to HTTPS**
- [x] Select **Always use secure connections**
- [x] (Optional) Select **Block Scripts** (1)
- [x] Select **Strict, may break sites** under **Block fingerprinting**

</div>

1. This option provides functionality similar to uBlock Origin's advanced [blocking modes](https://github.com/gorhill/uBlock/wiki/Blocking-mode) or the [NoScript](https://noscript.net/) extension.

##### Clear browsing data

- [x] Select **Clear data on exit**

##### Social Media Blocking

- [ ] Uncheck all social media components

##### Other privacy settings

<div class="annotate" markdown>

- [x] Select **Disable non-proxied UDP** under [WebRTC IP Handling Policy](https://support.brave.com/hc/en-us/articles/360017989132-How-do-I-change-my-Privacy-Settings-#webrtc)
- [ ] Uncheck **Allow sites to check if you have payment methods saved**
- [ ] Uncheck **IPFS Gateway** (1)
- [x] Select **Close tabs on exit**
- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send diagnostic reports**
- [ ] Uncheck **Automatically send daily usage ping to Brave**

</div>

1. O IPFS (InterPlanetary File System) é uma rede descentralizada, ponto a ponto, para armazenar e compartilhar dados em um sistema de arquivos distribuído. A menos que você use o recurso, desative-o.

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/en-us/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

## iOS

On iOS, any app that can browse the web is [restricted](https://developer.apple.com/app-store/review/guidelines) to using an Apple-provided [WebKit framework](https://developer.apple.com/documentation/webkit), so there is little reason to use a third-party web browser.

### Safari

!!! recommendation

    ![Safari logo](assets/img/browsers/safari.svg){ align=right }
    
    **Safari** is the default browser in iOS. It includes [privacy features](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/15.0/ios/15.0) such as [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention/), Privacy Report, isolated and ephemeral Private Browsing tabs, iCloud Private Relay, and fingerprinting reduction by presenting a simplified version of the system configuration to websites so more devices look identical.
    
    Safari is restricted to Apple devices and is covered by [System Integrity Protection](https://support.apple.com/guide/security/system-integrity-protection-secb7ea06b49/web), a security feature which limits system programs and files to being read-only so they can't be tampered with by you or malware.
    
    [:octicons-home-16: Homepage](https://www.apple.com/safari/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.apple.com/legal/privacy/data/en/safari/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://support.apple.com/guide/safari/welcome/mac){ .card-link title=Documentation}

#### Configuração Recomendada

Estas opções podem ser encontradas em :gear: **Configurações** → **Safari** → **Privacidade e Segurança**.

##### Cross-Site Tracking Prevention

- [x] Enable **Prevent Cross-Site Tracking**

This enables WebKit's [Intelligent Tracking Protection](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp). O recurso ajuda a proteger contra o rastreamento indesejado, usando o aprendizado de máquina no dispositivo para impedir os rastreadores. O ITP protege contra muitas ameaças comuns, mas não bloqueia todas as vias de rastreamento porque foi projetado para não interferir na usabilidade do site.

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

You can enable E2EE for your Safari bookmarks and downloads by enabling [Advanced Data Protection](https://support.apple.com/en-us/HT212520). Go to your **Apple ID name → iCloud → Advanced Data Protection**.

- [x] Turn On **Advanced Data Protection**

If you use iCloud with Advanced Data Protection disabled, we also recommend checking to ensure Safari's default download location is set to locally on your device. This option can be found in :gear: **Settings** → **Safari** → **General** → **Downloads**.

### AdGuard

!!! recommendation

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

## Criteria

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

!!! example "This section is new"

    We are working on establishing defined criteria for every section of our site, and this may be subject to change. If you have any questions about our criteria, please [ask on our forum](https://discuss.privacyguides.net/latest) and don't assume we didn't consider something when making our recommendations if it is not listed here. There are many factors considered and discussed when we recommend a project, and documenting every single one is a work-in-progress.

### Minimum Requirements

- Deve suportar atualizações automáticas.
- Must receive engine updates in 0-1 days from upstream release.
- Qualquer mudança necessária para tornar o navegador mais compatível com a privacidade não deve afetar negativamente a experiência do usuário.
- Navegadores Android devem usar o motor Chromium.
    - Infelizmente, o Mozilla GeckoView ainda é menos seguro que o Chromium no Android.
    - Navegadores iOS estão limitados ao WebKit.

### Critérios para Extensões

- Não deve copiar a funcionalidade existente no navegador ou no sistema operacional.
- Deve afetar diretamente a privacidade do usuário, ou seja, não deve simplesmente fornecer informações.
