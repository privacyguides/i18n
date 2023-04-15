---
meta_title: "Privacy Respecting Web Browsers for PC and Mac - Privacy Guides"
title: "Desktop Browsers"
icon: material/laptop
description: These web browsers provide stronger privacy protections than Google Chrome.
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Private Desktop Browser Recommendations
    url: "./"
    relatedLink: "../mobile-browsers/"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Mullvad Browser
    image: /assets/img/browsers/mullvad_browser.svg
    url: https://mullvad.net/en/browser
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
    sameAs: https://en.wikipedia.org/wiki/Firefox
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
    sameAs: https://en.wikipedia.org/wiki/Brave_(web_browser)
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
---

These are our currently recommended desktop web browsers and configurations for standard/non-anonymous browsing. We recommend [Mullvad Browser](#mullvad-browser) if you are focused on strong privacy protections and anti-fingerprinting out of the box, [Firefox](#firefox) for casual internet browsers looking for a good alternative to Google Chrome, and [Brave](#brave) if you need Chromium browser compatibility.

Если вам нужна анонимность в сети, используйте [Tor](tor.md). We make some configuration recommendations on this page, but all browsers other than Tor Browser will be traceable by *somebody* in some manner or another.

## Mullvad Browser

!!! recommendation

    ![Mullvad Browser logo](assets/img/browsers/mullvad_browser.svg){ align=right }
    
    **Mullvad Browser** is a version of [Tor Browser](tor.md#tor-browser) with Tor network integrations removed, aimed at providing Tor Browser's anti-fingerprinting browser technologies to VPN users. It is developed by the Tor Project and distributed by [Mullvad](vpn.md#mullvad), and does **not** require the use of Mullvad's VPN.
    
    [:octicons-home-16: Homepage](https://mullvad.net/en/browser){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser/){ .card-link title=Documentation}
    [:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Source Code" }
    
    ??? downloads
    
        - [:simple-windows11: Windows](https://mullvad.net/en/download/browser/windows)
        - [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
        - [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

Like [Tor Browser](tor.md), Mullvad Browser is designed to prevent fingerprinting by making your browser fingerprint identical to all other Mullvad Browser users, and it includes default settings and extensions that are automatically configured by the default security levels: *Standard*, *Safer* and *Safest*. Therefore, it is imperative that you do not modify the browser at all outside adjusting the default [security levels](https://tb-manual.torproject.org/security-settings/). Other modifications would make your fingerprint unique, defeating the purpose of using this browser. If you want to configure your browser more heavily and fingerprinting is not a concern for you, we recommend [Firefox](#firefox) instead.

### Anti-Fingerprinting

**Without** using a [VPN](vpn.md), Mullvad Browser provides the same protections against [naive fingerprinting scripts](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting) as other private browsers like Firefox+[Arkenfox](#arkenfox-advanced) or [Brave](#brave). Mullvad Browser provides these protections out of the box, at the expense of some flexibility and convenience that other private browsers can provide.

==For the strongest anti-fingerprinting protection, we recommend using Mullvad Browser in conjunction **with** a VPN==, whether that is Mullvad or another recommended VPN provider. When using a VPN with Mullvad Browser, you will share a fingerprint and a pool of IP addresses with many other users, giving you a "crowd" to blend in with. This strategy is the only way to thwart advanced tracking scripts, and is the same anti-fingerprinting technique used by Tor Browser.

Note that while you can use Mullvad Browser with any VPN provider, other people on that VPN must also be using Mullvad Browser for this "crowd" to exist, something which is more likely on Mullvad VPN compared to other providers, particularly this close to the launch of Mullvad Browser. Mullvad Browser does not have built-in VPN connectivity, nor does it check whether you are using a VPN before browsing; your VPN connection has to be configured and managed separately.

Mullvad Browser comes with the *uBlock Origin* and *NoScript* browser extensions pre-installed. While we typically [don't recommend](#extensions) adding *additional* browser extensions, these extensions that come pre-installed with the browser should **not** be removed or configured outside their default values, because doing so would noticeably make your browser fingerprint distinct from other Mullvad Browser users. It also comes pre-installed with the Mullvad Browser Extension, which *can* be safely removed without impacting your browser fingerprint if you would like, but is also safe to keep even if you don't use Mullvad VPN.

### Private Browsing Mode

Mullvad Browser operates in permanent private browsing mode, meaning your history, cookies, and other site data will always be cleared every time the browser is closed. Your bookmarks, browser settings, and extension settings will still be preserved.

This is required to prevent advanced forms of tracking, but does come at the cost of convenience and some Firefox features, such as Multi-Account Containers. Remember you can always use multiple browsers, for example, you could consider using Firefox+Arkenfox for a few sites that you want to stay logged in on or otherwise don't work properly in Mullvad Browser, and Mullvad Browser for general browsing.

### Mullvad Leta

Mullvad Browser comes with DuckDuckGo set as the default [search engine](search-engines.md), but it also comes preinstalled with **Mullvad Leta**, a search engine which requires an active Mullvad VPN subscription to access. Mullvad Leta queries Google's paid search API directly (which is why it is limited to paying subscribers), however because of this limitation it is possible for Mullvad to correlate search queries and Mullvad VPN accounts. For this reason we discourage the use of Mullvad Leta, even though Mullvad collects very little information about their VPN subscribers.

## Firefox

!!! recommendation

    ![Логотип Bromite](assets/img/browsers/bromite.svg){ align=right }
    
    **Bromite** - это браузер, основанный на [Chromium](https://en.wikipedia.org/wiki/Chromium_(web_browser)), с основой на конфиденциальность и безопасность, встроенную блокировку рекламы и некоторую рандомизацию цифровых отпечатков.
    
    [Перейти на bromite.org](https://www.bromite.org){ .md-button .md-button--primary } [Политика конфиденциальности](https://www.bromite.org/privacy){ .md-button } downloads
    
        - [:simple-windows11: Windows](https://www.mozilla.org/firefox/windows)
        - [:simple-apple: macOS](https://www.mozilla.org/firefox/mac)
        - [:simple-linux: Linux](https://www.mozilla.org/firefox/linux)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

!!! warning
    Каждый установщик Firefox с веб-сайта Mozilla имеет в себе уникальный идентификатор, который используется для телеметрии. Идентификатор **не** включен в релизы браузера из [Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/).

### Рекомендованные настройки

These options can be found in :material-menu: → **Settings**

#### Search

- [ ] Uncheck **Provide search suggestions**

Функции предложения поиска могут быть недоступны в вашем регионе.

Поисковые предложения отправляют все, что вы набираете в адресной строке, в поисковую систему по умолчанию, независимо от того, отправляете ли вы фактический поиск. Отключение поисковых предложений позволяет более точно контролировать данные, которые вы отправляете поставщику поисковых систем.

#### Privacy & Security

##### Улучшенная защита от отслеживания:

- Выберите «Строгая»

Это защищает вас, блокируя трекеры социальных сетей, скрипты отпечатков пальцев (обратите внимание, что это не защищает вас от *всех* отпечатков пальцев), криптомайнеры, межсайтовые файлы cookie для отслеживания и некоторые другие средства отслеживания. Улучшенная защита от отслеживания защищает от многих распространенных угроз, но не блокирует все пути отслеживания, поскольку разработан таким образом, чтобы минимально или вообще не влиять на удобство использования сайта.

##### Firefox Suggest (US only)

[Firefox Suggest](https://support.mozilla.org/en-US/kb/firefox-suggest) is a feature similar to search suggestions which is only available in the US. We recommend disabling it for the same reason we recommend disabling search suggestions. If you don't see these options under the **Address Bar** header, you do not have the new experience and can ignore these changes.

- [ ] Uncheck **Suggestions from the web**
- [ ] Uncheck **Suggestions from sponsors**

##### Куки и данные сайтов:

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy/) использует сквозное шифрование.

- Выберите «Удалять куки и данные сайтов при закрытии Firefox»

Это защищает вас от постоянных файлов cookie, но не защищает вас от файлов cookie, полученных в течение одного сеанса просмотра. Когда эта функция включена, можно легко очистить куки браузера, просто перезапустив Firefox. Вы можете установить исключения для каждого сайта, если вы хотите оставаться зарегистрированным на определенном сайте, который вы часто посещаете.

##### Отключение телеметрии

- [ ] Uncheck **Allow Firefox to send technical and interaction data to Mozilla**
- [ ] Uncheck **Allow Firefox to install and run studies**
- [ ] Uncheck **Allow Firefox to send backlogged crash reports on your behalf**

> Firefox sends data about your Firefox version and language; device operating system and hardware configuration; memory, basic information about crashes and errors; outcome of automated processes like updates, safebrowsing, and activation to us. When Firefox sends data to us, your IP address is temporarily collected as part of our server logs.

Additionally, the Firefox Accounts service collects [some technical data](https://www.mozilla.org/en-US/privacy/firefox/#firefox-accounts). If you use a Firefox Account you can opt-out:

1. Open your [profile settings on accounts.firefox.com](https://accounts.firefox.com/settings#data-collection)
2. Uncheck **Data Collection and Use** > **Help improve Firefox Accounts**

##### Режим «Только HTTPS»:

- Выберите: "Включить режим «Только HTTPS» во всех окнах".

Это предотвращает непреднамеренное подключение к веб-сайту с обычным HTTP-текстом. Протокол HTTP в настоящее время используется крайне редко, поэтому это практически не должно повлиять на ваш ежедневный просмотр веб-страниц.

#### Sync

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy/) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices and protects it with E2EE.

### Расширения

!!! tip "Use Mullvad Browser for advanced anti-fingerprinting"

    [Mullvad Browser](#mullvad-browser) provides the same anti-fingerprinting protections as Arkenfox out of the box, and does not require the use of Mullvad's VPN to benefit from these protections. Coupled with a VPN, Mullvad Browser can thwart more advanced tracking scripts which Arkenfox cannot. Arkenfox still has the advantage of being much more flexible, and allowing per-site exceptions for websites which you need to stay logged in to.

The [Arkenfox project](https://github.com/arkenfox/user.js) provides a set of carefully considered options for Firefox. If you [decide](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) to use Arkenfox, a [few options](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) are subjectively strict and/or may cause some websites to not work properly - [which you can easily change](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) to suit your needs. We **strongly recommend** reading through their full [wiki](https://github.com/arkenfox/user.js/wiki). Arkenfox also enables [container](https://support.mozilla.org/en-US/kb/containers#w_for-advanced-users) support.

Arkenfox only aims to thwart basic or naive tracking scripts through canvas randomization and Firefox's built-in fingerprint resistance configuration settings. It does not aim to make your browser blend in with a large crowd of other Arkenfox users in the same way Mullvad Browser or Tor Browser do, which is the only way to thwart advanced fingerprint tracking scripts. Remember you can always use multiple browsers, for example, you could consider using Firefox+Arkenfox for a few sites that you want to stay logged in on or otherwise trust, and Mullvad Browser for general browsing.

## Brave

!!! recommendation

    ![Логотип Brave](assets/img/browsers/brave.svg){ align=right }
    
    **Браузер Brave** включает встроенный блокировщик контента и [инструменты приватности](https://brave.com/privacy-features/), многие из которых включены по умолчанию.
    
    Brave основан на Chromium, поэтому он покажется вам знакомым, а также у него не должно быть проблем с совместимостью.
    
    [:octicons-home-16: Официальный сайт](https://brave.com/ru/){ .md-button .md-button--primary }
    [:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion-сайт" }
    [:octicons-eye-16:](https://brave.com/privacy/browser/){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://support.brave.com/){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Исходный код" }
    
    ??? downloads annotate
    
        - [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
        - [:simple-windows11: Windows](https://brave.com/download/)
        - [:simple-apple: macOS](https://brave.com/download/)
        - [:simple-linux: Linux](https://brave.com/linux/) (1)

    1. We advise against using the Flatpak version of Brave, as it replaces Chromium's sandbox with Flatpak's, which is less effective. Additionally, the package is not maintained by Brave Software, Inc.

### Рекомендованные настройки

These options can be found in :material-menu: → **Settings**.

#### Settings

##### Режим «Только HTTPS»:

Brave включает несколько инструментов защиты от отслеживания в разделе [Shields](https://support.brave.com/hc/en-us/articles/360022973471-What-is-Shields-). Мы рекомендуем включить эти настройки [на всех сайтах](https://support.brave.com/hc/en-us/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings-), которые вы посещаете.

Shields' options can be downgraded on a per-site basis as needed, but by default we recommend setting the following:

<div class="annotate" markdown>

- [x] Select **Prevent sites from fingerprinting me based on my language preferences**
- [x] Select **Aggressive** under Trackers & ads blocking

    ??? warning "Use default filter lists"
        Brave allows you to select additional content filters within the internal `brave://adblock` page. We advise against using this feature; instead, keep the default filter lists. Using extra lists will make you stand out from other Brave users and may also increase attack surface if there is an exploit in Brave and a malicious rule is added to one of the lists you use.

- [x] (Optional) Select **Block Scripts** (1)
- [x] Select **Strict, may break sites** under Block fingerprinting

</div>

1. This option provides functionality similar to uBlock Origin's advanced [blocking modes](https://github.com/gorhill/uBlock/wiki/Blocking-mode) or the [NoScript](https://noscript.net/) extension.

##### Постоянно включенный режим инкогнито

- [ ] Отключите все компоненты социальных сетей

##### Предотвращение перекрестного отслеживания

<div class="annotate" markdown>

- [x] Select **Disable non-proxied UDP** under [WebRTC IP Handling Policy](https://support.brave.com/hc/en-us/articles/360017989132-How-do-I-change-my-Privacy-Settings-#webrtc)
- [ ] Uncheck **Use Google services for push messaging**
- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send daily usage ping to Brave**
- [ ] Uncheck **Automatically send diagnostic reports**
- [x] Select **Always use secure connections** in the **Security** menu
- [ ] Uncheck **Private window with Tor** (1)

    !!! tip "Sanitizing on Close"

        - [x] Select **Clear cookies and site data when you close all windows** in the *Cookies and other site data* menu

        If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis under the *Customized behaviors* section.

</div>

1. Brave is **not** as resistant to fingerprinting as the Tor Browser and far fewer people use Brave with Tor, so you will stand out. Where [strong anonymity is required](https://support.brave.com/hc/en-us/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity-) use the [Tor Browser](tor.md#tor-browser).

##### Отчет о конфиденциальности

Disable built-in extensions you do not use in **Extensions**

- [ ] Uncheck **Hangouts**
- [ ] Uncheck **WebTorrent**

##### Web3

Brave's Web3 features can potentially add to your browser fingerprint and attack surface. Unless you use any of features, they should be disabled.

- [ ] Set **Default Ethereum Wallet** to **None**
- [ ] Set **Default Solana Wallet** to **None**
- [ ] Set **Method to resolve IPFS resources** to **Disabled

##### System

<div class="annotate" markdown>

- [ ] Uncheck **Continue running apps when Brave is closed** to disable background apps (1)

</div>

1. This option is not present on all platforms.

#### Sync

[Brave Sync](https://support.brave.com/hc/en-us/articles/360059793111-Understanding-Brave-Sync) позволяет синхронизировать данные браузера (историю, закладки и т. д.) между несколькими устройствами без необходимости создавать аккаунт, а также защищает их при помощи E2EE.

#### Brave Rewards and Wallet

**Brave Rewards** lets you recieve Basic Attention Token (BAT) cryptocurrency for performing certain actions within Brave. It relies on a custodial account and KYC from a select number of providers. We do not recommend BAT as a [private cryptocurrency](cryptocurrency.md), nor do we recommend using a [custodial wallet](advanced/payments.md#other-coins-bitcoin-ethereum-etc), so we would discourage using this feature.

**Brave Wallet** operates locally on your computer, but does not support any private cryptocurrencies, so we would discourage using this feature as well.

## Дополнительные советы

In general, we recommend keeping your browser extensions to a minimum to decrease your attack surface; they have privileged access within your browser, require you to trust the developer, can make you [stand out](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint), and [weaken](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ) site isolation. However, uBlock Origin may prove useful if you value content blocking functionality.

### AdGuard для Safari

!!! recommendation

    ![Логотип Snowflake](assets/img/browsers/snowflake.svg#only-light){ align=right }
    ![Логотип Snowflake](assets/img/browsers/snowflake-dark.svg#only-dark){ align=right }
    
    **Snowflake** - это расширение для браузера, которое позволяет вам отдавать свою скорость интернета проекту Tor, используя "прокси Snowflake" в вашем браузере.
    
    Люди, подвергающиеся цензуре, могут использовать прокси-серверы Snowflake для подключения к сети Tor. downloads
    
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/ublock-origin/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm)
        - [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/ublock-origin/odfafepnkmbhccpbejgmiehpchacaeak)

We suggest following the [developer's documentation](https://github.com/gorhill/uBlock/wiki/Blocking-mode) and picking one of the "modes". Additional filter lists can impact performance and [may increase attack surface](https://portswigger.net/research/ublock-i-exfiltrate-exploiting-ad-blockers-with-css).

##### Other lists

These are some other [filter lists](https://github.com/gorhill/uBlock/wiki/Dashboard:-Filter-lists) that you may want to consider adding:

- [x] Check **Privacy** > **AdGuard URL Tracking Protection**
- Add [Actually Legitimate URL Shortener Tool](https://raw.githubusercontent.com/DandelionSprout/adfilt/master/LegitimateURLShortener.txt)

## Criteria

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

!!! Для уменьшения этой угрозы рассмотрите возможность самостоятельного хостинга.

    We are working on establishing defined criteria for every section of our site, and this may be subject to change. If you have any questions about our criteria, please [ask on our forum](https://discuss.privacyguides.net/latest) and don't assume we didn't consider something when making our recommendations if it is not listed here. Мы учитываем и обсуждаем много факторов, перед тем как рекомендовать какой-то проект, и документирование каждого из них ещё не завершено.

### Минимальные требования к сервисам

- Must be open-source software.
- Supports automatic updates.
- Receives engine updates in 0-1 days from upstream release.
- Available on Linux, macOS, and Windows.
- Any changes required to make the browser more privacy-respecting should not negatively impact user experience.
- Blocks third-party cookies by default.
- Supports [state partitioning](https://developer.mozilla.org/en-US/docs/Web/Privacy/State_Partitioning) to mitigate cross-site tracking.[^1]

### В лучшем случае

Эти критерии представляют собой то, что мы хотели бы видеть от идеального проекта в этой категории. Наши рекомендации могут не соответствовать всем или нескольким из этих критериев, но проекты, которые им соответствуют, расположены выше остальных.

- Includes built-in content blocking functionality.
- Supports cookie compartmentalization (à la [Multi-Account Containers](https://support.mozilla.org/en-US/kb/containers)).
- Supports Progressive Web Apps.  
  PWAs enable you to install certain websites as if they were native apps on your computer. This can have advantages over installing Electron-based apps, because you benefit from your browser's regular security updates.
- Does not include add-on functionality (bloatware) that does not impact user privacy.
- Does not collect telemetry by default.
- Provides open-source sync server implementation.
- Defaults to a [private search engine](search-engines.md).

### Extension Criteria

- Must not replicate built-in browser or OS functionality.
- Must directly impact user privacy, i.e. must not simply provide information.

[^1]: Brave's implementation is detailed at [Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state/).
