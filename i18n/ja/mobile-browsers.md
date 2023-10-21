---
meta_title: "プライバシーを尊重するAndroidとiOS向けモバイルウェブブラウザ - Privacy Guides"
title: "モバイルブラウザ"
icon: material/cellphone-information
description: これらのブラウザは、現在お使いの携帯電話の標準/非匿名のインターネットブラウジングに推奨されています。
cover: mobile-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: プライベートモバイルブラウザの推奨事項
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

以下は、一般的な非匿名のブラウジング用に、現在おすすめされているモバイルウェブブラウザとその設定です。 匿名でインターネットを閲覧するには、[Tor](tor.md)を使用してください。 一般的に、拡張機能は最小限に抑えることをお勧めします。ブラウザ内で特権的なアクセスを持ち、開発者を信頼する必要があり、[あなたを目立たせ](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)、[サイト分離を弱めます](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ)。

## Android

Androidでは、FirefoxはChromiumベースのブラウザよりもまだ安全性が低いです。Mozillaのエンジンである[GeckoView](https://mozilla.github.io/geckoview/)は、まだ[サイト分離](https://hacks.mozilla.org/2021/05/introducing-firefox-new-site-isolation-security-architecture)をサポートしておらず、また [分離プロセス](https://bugzilla.mozilla.org/show_bug.cgi?id=1565196)を有効にしていません。

### Brave

!!! recommendation

    ![Brave logo](assets/img/browsers/brave.svg){ align=right }
    
    **Brave Browser**には、コンテンツブロッカーと [プライバシー機能](https://brave.com/privacy-features/) が内蔵されていて、その多くがデフォルトで有効になっています。
    
    Brave is built upon the Chromium web browser project, so it should feel familiar and have minimal website compatibility issues.
    
    [:octicons-home-16: ホームページ](https://brave.com/ja/){ .md-button .md-button--primary }
    [:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
    [:octicons-eye-16:](https://brave.com/privacy/browser/){ .card-link title="プライバシーポリシー" }
    [:octicons-info-16:](https://support.brave.com/hc/en-us/categories/360006507272){ .card-link title=ドキュメント}
    [:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="ソースコード" }
    
    ??? ダウンロード
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
        - [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)

#### 推奨する設定

本当に匿名でインターネットを閲覧する唯一の方法は、Tor Browserを使うことです。 Braveを使用する際は、特定の相手からプライバシーを保護するために以下の設定を変更することをお勧めしますが、 [Tor Browser](tor.md#tor-browser) 以外のブラウザについては、*誰か*が何らかの形で追跡することができます。

These options can be found in :material-menu: → **Settings** → **Brave Shields & privacy**

##### Shields

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/en-us/articles/360022973471-What-is-Shields-) feature. We suggest configuring these options [globally](https://support.brave.com/hc/en-us/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings-) across all pages that you visit.

##### Braveシールドのグローバルデフォルト

Shields' options can be downgraded on a per-site basis as needed, but by default we recommend setting the following:

<div class="annotate" markdown>

- [x] Select **Aggressive** under **Block trackers & ads**

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

- [x] Select **Disable non-proxied UDP** under [WebRTC IP handling policy](https://support.brave.com/hc/en-us/articles/360017989132-How-do-I-change-my-Privacy-Settings-#webrtc)
- [ ] Uncheck **Allow sites to check if you have payment methods saved**
- [ ] Uncheck **IPFS Gateway** (1)
- [x] Select **Close tabs on exit**
- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send diagnostic reports**
- [ ] Uncheck **Automatically send daily usage ping to Brave**

</div>

1. InterPlanetary File System (IPFS) is a decentralized, peer-to-peer network for storing and sharing data in a distributed filesystem. Unless you use the feature, disable it.

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/en-us/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

## iOS

On iOS, any app that can browse the web is [restricted](https://developer.apple.com/app-store/review/guidelines) to using an Apple-provided [WebKit framework](https://developer.apple.com/documentation/webkit), so there is little reason to use a third-party web browser.

### Safari

!!! recommendation

    ![Safari logo](assets/img/browsers/safari.svg){ align=right }
    
    **Safari** is the default browser in iOS. It includes [privacy features](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/15.0/ios/15.0) such as [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention/), Privacy Report, isolated and ephemeral Private Browsing tabs, iCloud Private Relay, and fingerprinting reduction by presenting a simplified version of the system configuration to websites so more devices look identical.
    
    [:octicons-home-16: Homepage](https://www.apple.com/safari/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.apple.com/legal/privacy/data/en/safari/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://support.apple.com/guide/safari/welcome/mac){ .card-link title=Documentation}

#### 推奨する設定

These options can be found in :gear: **Settings** → **Safari** → **Privacy and Security**.

##### Cross-Site Tracking Prevention

- [x] Enable **Prevent Cross-Site Tracking**

This enables WebKit's [Intelligent Tracking Protection](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp). The feature helps protect against unwanted tracking by using on-device machine learning to stop trackers. ITP protects against many common threats, but it does not block all tracking avenues because it is designed to not interfere with website usability.

##### プライバシーレポート

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

## 基準

**私たちは、推奨するどのプロジェクトとも提携していないことに注意してください。** [標準的な基準](about/criteria.md) に加えて、客観的な推奨事項を提供できるようにするために明確な要件を定めています。 プロジェクトを利用する前にこのリストをよく理解し、それが自分にとって正しい選択であることを確認するために自身で調査を行うことをお勧めします。

!!! example "この項目は最近作成されました"

    私たちは、サイトの各項目に定義された基準を確立することに取り組んでおり、これは変更される可能性があります。 私たちの基準について疑問がある場合は、[フォーラムで質問](https://discuss.privacyguides.net/latest)してください。また、ここに記載されていない場合でも、私たちが推奨事項を作成する際に考慮しなかったと仮定しないでください。 プロジェクトを推奨する際には多くの要素が考慮され、議論されており、そのすべてを文書化する作業は現在進行中です。

### 最低要件

- Must support automatic updates.
- Must receive engine updates in 0-1 days from upstream release.
- Any changes required to make the browser more privacy-respecting should not negatively impact user experience.
- Android browsers must use the Chromium engine.
    - Unfortunately, Mozilla GeckoView is still less secure than Chromium on Android.
    - iOS browsers are limited to WebKit.

### 拡張機能の基準

- ブラウザやOSに含まれる機能と重複しないこと。
- ユーザーのプライバシーに直接影響を与える必要があります。つまり、単に情報を提供するだけではない必要があります。
