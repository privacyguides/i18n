---
meta_title: "プライバシーを尊重するAndroidとiOS向けモバイルウェブブラウザー - Privacy Guides"
title: "モバイルブラウザー"
icon: material/cellphone-information
description: これらのブラウザは、現在お使いの携帯電話の標準/非匿名のインターネットブラウジングに推奨されています。
cover: mobile-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: 推奨するプライベートモバイルブラウザー
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
    url: https://apple.com/safari
    applicationCategory: Web Browser
    operatingSystem:
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
---

以下は、一般的な非匿名のブラウジング用に、現在おすすめされているモバイルウェブブラウザとその設定です。 匿名でインターネットを閲覧するには、[Tor](tor.md)を使用してください。 一般的に、拡張機能は最小限に抑えることをお勧めします。拡張機能は、ブラウザー内で特権的なアクセスを備えており、あなたは開発者を信頼する必要があります。また、[あなたを目立たせたり](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)、サイト分離を[弱めたりする](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ)こともあります。

## Android

On Android, Firefox is still less secure than Chromium-based alternatives: Mozilla's engine, [GeckoView](https://mozilla.github.io/geckoview), has yet to support [site isolation](https://hacks.mozilla.org/2021/05/introducing-firefox-new-site-isolation-security-architecture) or enable [isolatedProcess](https://bugzilla.mozilla.org/show_bug.cgi?id=1565196).

### Brave

<div class="admonition recommendation" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** includes a built-in content blocker and [privacy features](https://brave.com/privacy-features), many of which are enabled by default.

BraveはChromiumウェブブラウザープロジェクトに基づいて構築されているため、使い慣れた使用感があるほか、ウェブサイトの互換性問題を最小限に抑えられます。

[:octicons-home-16: Homepage](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.brave.com){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)

</details>

</div>

#### Recommended Brave Configuration

本当に匿名でインターネットを閲覧する唯一の方法は、Tor Browserを使うことです。 Braveを使用する際は、特定の相手からプライバシーを保護するために以下の設定を変更することをお勧めしますが、 [Tor Browser](tor.md#tor-browser) 以外のブラウザーについては、*誰か*が何らかの形で追跡することができます。

これらのオプションは、 :material-menu: → **設定** → **Braveシールド & プライバシー**にあります。

##### シールド

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) feature. We suggest configuring these options [globally](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) across all pages that you visit.

##### Braveシールドのグローバルデフォルト

シールドのオプションは、必要に応じてサイトごとにダウングレードできますが、デフォルトでは以下の設定をおすすめします。

<div class="annotate" markdown>

- [x] Select **Aggressive** under **Block trackers & ads**

<details class="warning" markdown>
<summary>Use default filter lists</summary>

Brave allows you to select additional content filters within the internal `brave://adblock` page. この機能は使わず、デフォルトのフィルターの一覧のままにしておくことをお勧めします。 追加のリストを使用すると、他のBraveユーザーから目立つようになり、また、Braveの脆弱性によってリストに悪意のあるルールが追加された場合、攻撃対象となる領域が増えるおそれがあります。

</details>

- [x] **接続をHTTPSにアップグレード**を選択
- [x] **常に安全な接続を使用**を選択
- [x] （オプション）**スクリプトをブロック**を選択 (1)
- [x] **フィンガープリンティング**の下にある**厳格、サイトが適切に機能しなくなる可能性あり**を選択

</div>

1. This option provides functionality similar to uBlock Origin's advanced [blocking modes](https://github.com/gorhill/uBlock/wiki/Blocking-mode) or the [NoScript](https://noscript.net) extension.

##### ブラウジングデータを消去

- [x] Select **Clear data on exit**

##### Social Media Blocking

- [ ] すべてのソーシャルメディアコンポーネントのチェックを外すこと

##### その他のプライバシーの設定

<div class="annotate" markdown>

- [x] Select **Disable non-proxied UDP** under [WebRTC IP handling policy](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Uncheck **Allow sites to check if you have payment methods saved**
- [ ] Uncheck **IPFS Gateway** (1)
- [x] Select **Close tabs on exit**
- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send diagnostic reports**
- [ ] Uncheck **Automatically send daily usage ping to Brave**

</div>

1. InterPlanetary File System (IPFS) is a decentralized, peer-to-peer network for storing and sharing data in a distributed filesystem. Unless you use the feature, disable it.

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

## iOS

On iOS, any app that can browse the web is [restricted](https://developer.apple.com/app-store/review/guidelines) to using an Apple-provided [WebKit framework](https://developer.apple.com/documentation/webkit), so there is little reason to use a third-party web browser.

### Safari

<div class="admonition recommendation" markdown>

![Safari logo](assets/img/browsers/safari.svg){ align=right }

**Safari** is the default browser in iOS. It includes [privacy features](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/15.0/ios/15.0) such as [Intelligent Tracking Prevention](https://webkit.org/blog/7675/intelligent-tracking-prevention), Privacy Report, isolated and ephemeral Private Browsing tabs, iCloud Private Relay, fingerprinting protection by randomizing and presenting a simplified version of the system configuration to websites so more devices look identical, and the ability to lock private tabs with your biometrics/PIN. It also allows you to separate your browsing with different profiles.

[:octicons-home-16: Homepage](https://apple.com/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/data/en/safari){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.apple.com/guide/safari/welcome/mac){ .card-link title=Documentation}

</details>

</div>

#### Recommended Safari Configuration

These options can be found in :gear: **Settings** → **Safari**

##### Profiles

All of your cookies, history, and website data will be separate for each profile. You should use different profiles for different purposes e.g. Shopping, Work, or School.

##### プライバシーとセキュリティ

- [x] Enable **Prevent Cross-Site Tracking**

    This enables WebKit's [Intelligent Tracking Protection](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp). The feature helps protect against unwanted tracking by using on-device machine learning to stop trackers. ITP protects against many common threats, but it does not block all tracking avenues because it is designed to not interfere with website usability.

- [x] Enable **Require Face ID to Unlock Private Browsing**

    This setting allows you to lock your private tabs behind biometrics/PIN when not in use.

##### Advanced → Privacy

The **Advanced Tracking and Fingerprinting Protection** setting will randomize certain values so that it's more difficult to fingerprint you:

- [x] Select **All Browsing** or **Private Browsing**

##### プライバシーレポート

Privacy Report provides a snapshot of cross-site trackers currently prevented from profiling you on the website you're visiting. It can also display a weekly report to show which trackers have been blocked over time.

プライバシーレポートには、ページ設定メニューからアクセスできます。

##### Privacy Preserving Ad Measurement

- [ ] Disable **Privacy Preserving Ad Measurement**

Ad click measurement has traditionally used tracking technology that infringes on user privacy. [Private Click Measurement](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm) is a WebKit feature and proposed web standard aimed towards allowing advertisers to measure the effectiveness of web campaigns without compromising on user privacy.

The feature has little privacy concerns on its own, so while you can choose to leave it on, we consider the fact that it's automatically disabled in Private Browsing to be an indicator for disabling the feature.

##### Always-on Private Browsing

Open Safari and tap the Tabs button, located in the bottom right. Then, expand the Tab Groups list.

- [x] Select **Private**

Safari's Private Browsing mode offers additional privacy protections. Private Browsing uses a new [ephemeral](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) session for each tab, meaning tabs are isolated from one another. There are also other smaller privacy benefits with Private Browsing, such as not sending a webpage’s address to Apple when using Safari's translation feature.

Do note that Private Browsing does not save cookies and website data, so it won't be possible to remain signed into sites. This may be an inconvenience.

##### iCloud同期

Safariの履歴、タブグループ、iCloudタブ、保存されたパスワードの同期は端末間暗号化によって行われます。 However, by default, bookmarks are [not](https://support.apple.com/HT202303). Apple can decrypt and access them in accordance with their [privacy policy](https://apple.com/legal/privacy/en-ww).

You can enable E2EE for your Safari bookmarks and downloads by enabling [Advanced Data Protection](https://support.apple.com/HT212520). **Apple ID名 → iCloud → 高度なデータ保護**にアクセスしてください。

- [x] **高度なデータ保護**を有効にする

高度なデータ保護を無効にしてiCloudを使用している場合は、Safariのデフォルトのダウンロード場所が、デバイスのローカルに設定されているかどうかを確認することもお勧めします。 This option can be found in :gear: **Settings** → **Safari** → **General** → **Downloads**.

## 規準

**私たちは、推奨するどのプロジェクトとも提携していないことに注意してください。** [標準的な基準](about/criteria.md) に加えて、客観的な推奨事項を提供できるようにするために明確な要件を定めています。 プロジェクトを利用する前に、このリストをよく理解し、ご自身で調査を行って、そのプロジェクトがあなたにとって適切な選択かどうかをご確認ください。

### 最低要件

- 自動アップデートに対応していること。
- アップストリームのリリースから0～1日以内にエンジンアップデートを受けること。
- ブラウザをよりプライバシーを尊重したものにするための変更が、ユーザーエクスペリエンスを損なうものではないこと。
- Androidのブラウザーの場合はChromiumエンジンを使用していること。
    - 残念ながら、Mozilla GeckoViewはAndroidのChromiumよりもまだ安全性が低いです。
    - iOSブラウザはWebKitに制限されています。
