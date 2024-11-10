---
meta_title: "Privacy Respecting Web Browsers for Android and iOS - Privacy Guides"
title: "Мобильные браузеры"
icon: material/cellphone-information
description: Мы рекомендуем эти браузеры для обычного/неанонимного браузинга в интернете на вашем телефоне.
cover: mobile-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Рекомендации приватных браузеров для телефонов
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

- [:material-account-cash: Капитализм слежки](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

These are our currently recommended **mobile web browsers** and configurations for standard/non-anonymous internet browsing. Если вам нужна анонимность в сети, используйте [Tor](tor.md).

## Brave

<div class="admonition recommendation" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** includes a built-in content blocker and [privacy features](https://brave.com/privacy-features), many of which are enabled by default.

Brave основан на Chromium, поэтому он покажется тебе знакомым, а также у него не должно быть проблем совместимости с сайтами.

[:octicons-home-16: Homepage](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.brave.com){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1052879175)
- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)

</details>

</div>

### Recommended Brave Configuration

Tor Browser — это единственный способ действительно анонимно пользоваться интернетом. Если ты используешь Brave, мы рекомендуем изменить следующие настройки, чтобы сохранить приватность, но все браузеры кроме [Tor](tor.md#tor-browser) могут *кем-нибудь* отслеживаться в том или ином виде.

=== "Android"

    These options can be found in :material-menu: → **Settings** → **Brave Shields & privacy**.

=== "iOS"

    These options can be found in :fontawesome-solid-ellipsis: → **Settings** → **Shields & Privacy**.

#### Brave shields global defaults

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) feature. We suggest configuring these options [globally](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) across all pages that you visit.

Опции щитов можно понижать по мере необходимости для каждого конкретного сайта, но по умолчанию мы рекомендуем установить следующие параметры:

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

    Brave allows you to select additional content filters within the **Content Filtering** menu or the internal `brave://adblock` page. Мы не рекомендуем использовать эту функцию; вместо этого оставь списки фильтров по умолчанию. Использование дополнительных фильтров выделит тебя среди других пользователей Brave, а также может увеличить площадь атаки, если в Brave есть эксплойт и вредоносное правило будет добавлено в один из используемых тобой списков.

    </details>

    - [x] Select **Forget me when I close this site**

    </div>

    1. This option disables JavaScript, which will break a lot of sites. To unbreak them, you can set exceptions on a per-site basis by tapping on the Shield icon in the address bar and unchecking this setting under *Advanced controls*.

=== "iOS"

    <div class="annotate" markdown>

    - [x] Select **Aggressive** under *Trackers & Ads Blocking*
    - [x] Select **Strict** under *Upgrade Connections to HTTPS*
    - [x] Select **Auto-Redirect AMP pages**
    - [x] Select **Auto-Redirect Tracking URLs**
    - \[x\] (Optional) Select **Block Scripts** (1)
    - [x] Select **Block Fingerprinting**

    <details class="warning" markdown>
    <summary>Use default filter lists</summary>

    Brave allows you to select additional content filters within the **Content Filtering** menu. Мы не рекомендуем использовать эту функцию; вместо этого оставь списки фильтров по умолчанию. Использование дополнительных фильтров выделит тебя среди других пользователей Brave, а также может увеличить площадь атаки, если в Brave есть эксплойт и вредоносное правило будет добавлено в один из используемых тобой списков.

    </details>

    </div>

    1. This option disables JavaScript, which will break a lot of sites. To unbreak them, you can set exceptions on a per-site basis by tapping on the Shield icon in the address bar and unchecking this setting under *Advanced controls*.

##### Clear browsing data (Android only)

- [x] Выбери **Удалять данные при выходе**

##### Social Media Blocking (Android only)

- [ ] Отключи все переключатели в этой секции

#### Other privacy settings

=== "Android"

    <div class="annotate" markdown>

    - [x] Select **Disable non-proxied UDP** under [*WebRTC IP handling policy*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
    - \[x\] (Optional) Select **No protection** under *Safe Browsing* (1)
    - [ ] Uncheck **Allow sites to check if you have payment methods saved**
    - [x] Select **Close tabs on exit**
    - [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
    - [ ] Uncheck **Automatically send diagnostic reports**
    - [ ] Uncheck **Automatically send daily usage ping to Brave**

    </div>

    1. Brave's [implementation of Safe Browsing](https://support.brave.com/hc/en-us/articles/15222663599629-Safe-Browsing-in-Brave) on Android **does not** proxy [Safe Browsing network requests](https://developers.google.com/safe-browsing/v4/update-api#checking-urls) like its desktop counterpart. This means that your IP address may be seen (and logged) by Google. Note that Safe Browsing is not available for Android devices without Google Play Services.

=== "iOS"

    - [ ] Uncheck **Allow Privacy-Preserving Product Analytics (P3A)**
    - [ ] Uncheck **Automatically send daily usage ping to Brave**

### Leo

These options can be found in :material-menu: → **Settings** → **Leo**.

<div class="annotate" markdown>

- [ ] Uncheck **Show autocomplete suggestions in address bar** (1)

</div>

1. This option is not present in Brave's iOS app.

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

On iOS, any app that can browse the web is [restricted](https://developer.apple.com/app-store/review/guidelines) to using an Apple-provided [WebKit framework](https://developer.apple.com/documentation/webkit), so a browser like [Brave](#brave) does not use the Chromium engine like its counterparts on other operating systems.

<div class="admonition recommendation" markdown>

![Логотип Safari](assets/img/browsers/safari.svg){ align=right }

**Safari** — браузер по умолчанию на iOS. It includes [privacy features](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/ios) such as [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention), isolated and ephemeral Private Browsing tabs, fingerprinting protection (by presenting a simplified version of the system configuration to websites so more devices look identical), and fingerprint randomization, as well as Private Relay for those with a paid iCloud+ subscription.

[:octicons-home-16: Homepage](https://apple.com/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/data/en/safari){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.apple.com/guide/iphone/browse-the-web-iph1fbef4daa/ios){ .card-link title=Documentation}

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

#### Поиск

- [ ] Disable **Search Engine Suggestions**

This setting sends whatever you type in the address bar to the search engine set in Safari. Отключение поисковых предложений позволяет более точно контролировать данные, которые вы отправляете поисковой системе.

#### Profiles

Safari allows you to separate your browsing with different profiles. All of your cookies, history, and website data are separate for each profile. You should use different profiles for different purposes e.g. Shopping, Work, or School.

#### Приватность и защита

- [x] Enable **Prevent Cross-Site Tracking**

This enables WebKit's [Intelligent Tracking Protection](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp). The feature helps protect against unwanted tracking by using on-device machine learning to stop trackers. ITP protects against many common threats, but does not block all tracking avenues because it is designed to not interfere with website usability.

- [x] Enable **Require Face ID/Touch ID to Unlock Private Browsing**

This setting allows you to lock your private tabs behind biometrics/PIN when not in use.

- [ ] Disable **Fraudulent Website Warning**

This setting uses Google Safe Browsing (or Tencent Safe Browsing for users in mainland China or Hong Kong) to protect you while you browse. As such, your IP address may be logged by your Safe Browsing provider. Disabling this setting will disable this logging, but you might be more vulnerable to known phishing sites.

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

##### Конфиденциальные рекламные отчеты

- [ ] Отключи **Конфиденциальные рекламные отчеты**

Для измерения количества рекламных кликов традиционно используется технология отслеживания, нарушающая конфиденциальность пользователей. [Private Click Measurement](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm) is a WebKit feature and proposed web standard aimed towards allowing advertisers to measure the effectiveness of web campaigns without compromising on user privacy.

Сама по себе эта функция не вызывает особых опасений в плане конфиденциальности, и хотя вы можете оставить ее включенной, мы рекомендуем её отключить, так как она автоматически отключается в Private Browsing.

#### Всегда включенный частный доступ

Откройте Safari и нажмите кнопку Вкладки, расположенную в правом нижнем углу. Then, expand the :material-format-list-bulleted: Tab Groups list.

- [x] Выбери **Частный доступ**

Режим Частный доступ в Safari обеспечивает дополнительную защиту конфиденциальности. Приватный просмотр использует новую [эфемерную](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) сессию для каждой вкладки, то есть вкладки изолированы друг от друга. При использовании частного доступа есть и другие небольшие преимущества, например, не отправлять адрес веб-страницы в Apple при использовании функции перевода в Safari.

Do note that Private Browsing does not save cookies and website data, so it won't be possible to remain signed in to sites. Это может доставить неудобства.

#### Синхронизация iCloud

Синхронизация истории Safari, групп вкладок, вкладок iCloud и сохраненных паролей осуществляется с E2EE. However, by default, bookmarks are [not](https://support.apple.com/HT202303). Apple can decrypt and access them in accordance with their [privacy policy](https://apple.com/legal/privacy/en-ww).

You can enable E2EE for your Safari bookmarks and downloads by enabling [Advanced Data Protection](https://support.apple.com/HT212520). Go to :gear: **Settings** → **iCloud** → **Advanced Data Protection**.

- [x] Turn on **Advanced Data Protection**

If you use iCloud with Advanced Data Protection disabled, we also recommend setting Safari's default download location to a local folder on your device. This option can be found in :gear: **Settings** → **Apps** → **Safari** → **General** → **Downloads**.

## Критерии

**Обрати внимание, что у нас нет связей ни с одним проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Мы рекомендуем тебе ознакомиться с этим списком, прежде чем выбрать продукт, и провести собственное исследование, чтобы убедиться в правильности своего выбора.

### Минимальные требования к сервисам

- Должен поддерживать автоматические обновления.
- Must receive engine updates from upstream releases quickly.
- Must support content blocking.
- Любые изменения, необходимые для того, чтобы браузер больше соблюдал конфиденциальность, не должны негативно влиять на опыт использования.
