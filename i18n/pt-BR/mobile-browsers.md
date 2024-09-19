---
meta_title: "Privacy Respecting Mobile Web Browsers for Android and iOS - Privacy Guides"
title: "Mobile Browsers"
icon: material/cellphone-information
description: These browsers are what we currently recommend for standard/non-anonymous internet browsing on your phone.
cover: mobile-browsers.webp
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
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Safari
    image: /assets/img/browsers/safari.svg
    url: https://apple.com/safari
    applicationCategory: Web Browser
    operatingSystem:
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
---

<small>Protects against the following threat(s):</small>

- [:material-account-cash: Surveillance Capitalism](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

These are our currently recommended **mobile web browsers** and configurations for standard/non-anonymous internet browsing. Se você precisa navegar pela internet anonimamente, você deve usar o [Tor](tor.md).

## Brave

<div class="admonition recommendation" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** includes a built-in content blocker and [privacy features](https://brave.com/privacy-features), many of which are enabled by default.

Brave is built upon the Chromium web browser project, so it should feel familiar and have minimal website compatibility issues.

[:octicons-home-16: Homepage](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.brave.com){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1052879175)

</details>

</div>

### Recommended Brave Configuration

O Navegador Tor é a única maneira de realmente navegar na Internet de forma anônima. Ao usar o Brave, recomendamos que você altere as seguintes configurações para proteger sua privacidade de determinadas partes, mas todos os navegadores, exceto o [Navegador Tor](tor.md#tor-browser), serão rastreáveis por *alguém* de uma forma ou de outra.

Essas opções podem ser encontradas em :material-menu: → **Configurações** → **Proteções do Brave & privacidade**

#### Shields

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) feature. We suggest configuring these options [globally](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) across all pages that you visit.

#### Brave shields global defaults

As opções do Shields (Escudos) podem ser reduzidas de acordo com o site, conforme necessário, mas, por padrão, recomendamos configurar o seguinte:

<div class="annotate" markdown>

- [x] Select **Aggressive** under **Block trackers & ads**

<details class="warning" markdown>
<summary>Use default filter lists</summary>

Brave allows you to select additional content filters within the internal `brave://adblock` page. We advise against using this feature; instead, keep the default filter lists. Using extra lists will make you stand out from other Brave users and may also increase attack surface if there is an exploit in Brave and a malicious rule is added to one of the lists you use.

</details>

- [x] Select **Auto-redirect AMP pages**
- [x] Select **Auto-redirect tracking URLs**
- [x] Select **strict** under **Upgrade connections to HTTPS**
- [x] (Optional) Select **Block Scripts** (1)
- [x] Select **Block third-party cookies** under **Block Cookies**
- [x] Select **Block fingerprinting**
- [x] Select **Prevent fingerprinting via language settings**

</div>

1. This option provides functionality similar to uBlock Origin's advanced [blocking modes](https://github.com/gorhill/uBlock/wiki/Blocking-mode) or the [NoScript](https://noscript.net) extension.

#### Clear browsing data

- [x] Select **Clear data on exit**

#### Social Media Blocking

- [ ] Uncheck all social media components

#### Other privacy settings

<div class="annotate" markdown>

- [x] Select **Disable non-proxied UDP** under [WebRTC IP handling policy](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [x] (Optional) Select **No protection** under **Safe Browsing** (1)
- [ ] Uncheck **Allow sites to check if you have payment methods saved**
- [ ] Uncheck **IPFS Gateway** (2)
- [x] Select **Close tabs on exit**
- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send diagnostic reports**
- [ ] Uncheck **Automatically send daily usage ping to Brave**

</div>

1. Brave's [implementation of Safe Browsing](https://support.brave.com/hc/en-us/articles/15222663599629-Safe-Browsing-in-Brave) on Android **does not** proxy [Safe Browsing network requests](https://developers.google.com/safe-browsing/v4/update-api#checking-urls) like its desktop counterpart. This means that your IP address may be seen (and logged) by Google. Note that Safe Browsing is not available for Android devices without Google Play Services.
2. O IPFS (InterPlanetary File System) é uma rede descentralizada, ponto a ponto, para armazenar e compartilhar dados em um sistema de arquivos distribuído. A menos que você use o recurso, desative-o.

### Leo

These options can be found in :material-menu: → **Settings** → **Leo**

- [ ] Uncheck **Show autocomplete suggestions in address bar**

### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

## Mull (Android)

<div class="admonition recommendation" markdown>

![Mull logo](assets/img/browsers/mull.svg){ align=right }

**Mull** is a privacy oriented and deblobbed Android browser based on Firefox. Compared to Firefox, it offers much greater fingerprinting protection out of the box, and disables JavaScript Just-in-Time (JIT) compilation for enhanced security. It also removes all proprietary elements from Firefox, such as replacing Google Play Services references.

[:octicons-home-16: Homepage](https://divestos.org/pages/our_apps#mull){ .md-button .md-button--primary }
[:octicons-eye-16:](https://divestos.org/pages/privacy_policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://divestos.org/pages/browsers#tuningFenix){ .card-link title=Documentation }
[:octicons-code-16:](https://codeberg.org/divested-mobile/mull-fenix){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-fdroid: F-Droid](https://f-droid.org/en/packages/us.spotco.fennec_dos)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

Firefox (Gecko)-based browsers on Android [lack](https://bugzilla.mozilla.org/show_bug.cgi?id=1610822) [site isolation](https://wiki.mozilla.org/Project_Fission),[^1] a powerful security feature that protects against a malicious site performing a [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability))-like attack to gain access to the memory of another website you have open.[^2] Chromium-based browsers like [Brave](#brave) will provide more robust protection against malicious websites.

</div>

Enable DivestOS's [F-Droid repository](https://divestos.org/fdroid/official) to receive updates directly from the developer. Downloading Mull from the default F-Droid repo will mean your updates could be delayed by a few days or longer.

Mull enables many features upstreamed by the [Tor uplift project](https://wiki.mozilla.org/Security/Tor_Uplift) using preferences from [Arkenfox](desktop-browsers.md#arkenfox-advanced). Proprietary blobs are removed from Mozilla's code using the scripts developed for Fennec F-Droid.

### Recommended Mull Configuration

We would suggest installing [uBlock Origin](browser-extensions.md#ublock-origin) as a content blocker if you want to block trackers within Mull.

Mull comes with privacy protecting settings configured by default. You might consider configuring the **Delete browsing data on quit** options in Mull's settings if you want to close all your open tabs when quitting the app automatically, or clear other data such as browsing history and cookies automatically.

Because Mull has more advanced and strict privacy protections enabled by default compared to most browsers, some websites may not load or work properly unless you adjust those settings. You can consult this [list of known issues and workarounds](https://divestos.org/pages/broken#mull) for advice on a potential fix if you do encounter a broken site. Adjusting a setting in order to fix a website could impact your privacy/security, so make sure you fully understand any instructions you follow.

## Safari (iOS)

On iOS, any app that can browse the web is [restricted](https://developer.apple.com/app-store/review/guidelines) to using an Apple-provided [WebKit framework](https://developer.apple.com/documentation/webkit), so there is little reason to use a third-party web browser.

<div class="admonition recommendation" markdown>

![Safari logo](assets/img/browsers/safari.svg){ align=right }

**Safari** is the default browser in iOS. It includes [privacy features](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/ios) such as [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention), Privacy Report, isolated and ephemeral Private Browsing tabs, fingerprinting protection (by presenting a simplified version of the system configuration to websites so more devices look identical) as well as fingerprint randomization, and Private Relay for those with a paid iCloud+ subscription. It also allows you to separate your browsing with different profiles and lock private tabs with your biometrics/PIN.

[:octicons-home-16: Homepage](https://apple.com/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/data/en/safari){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.apple.com/guide/iphone/browse-the-web-iph1fbef4daa/ios){ .card-link title=Documentation}

</details>

</div>

### Recommended Safari Configuration

We would suggest installing [AdGuard](browser-extensions.md#adguard) if you want a content blocker in Safari.

The following privacy/security-related options can be found in the :gear: **Settings** app → **Safari**

#### Profiles

All of your cookies, history, and website data will be separate for each profile. You should use different profiles for different purposes e.g. Shopping, Work, or School.

#### Privacidade & Segurança

- [x] Enable **Prevent Cross-Site Tracking**

    This enables WebKit's [Intelligent Tracking Protection](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp). O recurso ajuda a proteger contra o rastreamento indesejado, usando o aprendizado de máquina no dispositivo para impedir os rastreadores. O ITP protege contra muitas ameaças comuns, mas não bloqueia todas as vias de rastreamento porque foi projetado para não interferir na usabilidade do site.

- [x] Enable **Require Face ID to Unlock Private Browsing**

    This setting allows you to lock your private tabs behind biometrics/PIN when not in use.

#### Advanced → Privacy

The **Advanced Tracking and Fingerprinting Protection** setting will randomize certain values so that it's more difficult to fingerprint you:

- [x] Select **All Browsing** or **Private Browsing**

#### Privacy Report

Privacy Report provides a snapshot of cross-site trackers currently prevented from profiling you on the website you're visiting. It can also display a weekly report to show which trackers have been blocked over time.

Privacy Report is accessible via the Page Settings menu.

#### Privacy Preserving Ad Measurement

- [ ] Disable **Privacy Preserving Ad Measurement**

Ad click measurement has traditionally used tracking technology that infringes on user privacy. [Private Click Measurement](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm) is a WebKit feature and proposed web standard aimed towards allowing advertisers to measure the effectiveness of web campaigns without compromising on user privacy.

The feature has little privacy concerns on its own, so while you can choose to leave it on, we consider the fact that it's automatically disabled in Private Browsing to be an indicator for disabling the feature.

#### Always-on Private Browsing

Open Safari and tap the Tabs button, located in the bottom right. Then, expand the Tab Groups list.

- [x] Select **Private**

Safari's Private Browsing mode offers additional privacy protections. Private Browsing uses a new [ephemeral](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) session for each tab, meaning tabs are isolated from one another. There are also other smaller privacy benefits with Private Browsing, such as not sending a webpage’s address to Apple when using Safari's translation feature.

Do note that Private Browsing does not save cookies and website data, so it won't be possible to remain signed into sites. This may be an inconvenience.

#### iCloud Sync

Synchronization of Safari History, Tab Groups, iCloud Tabs and saved passwords are E2EE. However, by default, bookmarks are [not](https://support.apple.com/HT202303). Apple can decrypt and access them in accordance with their [privacy policy](https://apple.com/legal/privacy/en-ww).

You can enable E2EE for your Safari bookmarks and downloads by enabling [Advanced Data Protection](https://support.apple.com/HT212520). Go to your **Apple ID name → iCloud → Advanced Data Protection**.

- [x] Turn On **Advanced Data Protection**

If you use iCloud with Advanced Data Protection disabled, we also recommend checking to ensure Safari's default download location is set to locally on your device. This option can be found in :gear: **Settings** → **Safari** → **General** → **Downloads**.

## Criteria

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

### Minimum Requirements

- Deve suportar atualizações automáticas.
- Must receive engine updates from upstream releases quickly.
- Must support content blocking.
- Qualquer mudança necessária para tornar o navegador mais compatível com a privacidade não deve afetar negativamente a experiência do usuário.
