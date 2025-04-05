---
meta_title: "プライバシーを尊重するAndroidとiOS向けウェブブラウザ - Privacy Guides"
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

<small>以下の脅威から保護します：</small>

- [:material-account-cash: 監視資本主義](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

標準的・非匿名のインターネットブラウジングにおいて推奨する**モバイルウェブブラウザ**と設定は以下の通りです。 匿名でインターネットを閲覧するには、[Tor](tor.md)を使用してください。

## Brave

<div class="admonition recommendation" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

**Brave ブラウザ** にはコンテンツブロッカーと[プライバシー機能](https://brave.com/privacy-features)が組み込まれており、その多くはデフォルトで有効になっています。

BraveはChromiumウェブブラウザープロジェクトに基づいて構築されているため、使い慣れた使用感があるほか、ウェブサイトの互換性問題を最小限に抑えられます。

[:octicons-home-16: ウェブページ](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.brave.com){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>ダウンロード</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1052879175)
- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)

</details>

</div>

### 推奨するBraveの設定

本当に匿名でインターネットを閲覧する唯一の方法は、Tor Browserを使うことです。 Braveを使用する際は、特定の相手からプライバシーを保護するために以下の設定を変更することをお勧めしますが、 [Tor Browser](tor.md#tor-browser) 以外のブラウザーについては、*誰か*が何らかの形で追跡することができます。

=== "Android"

    以下のオプションは:material-menu: → **設定** → **Brave Shields & プライバシー**にあります。

=== "iOS"

    以下のオプションは :fontawesome-solid-ellipsis: → **設定** → **Shields & プライバシー**にあります。

#### Brave shields グローバルデフォルト

Braveの[シールド](https://support.brave.com/hc/articles/360022973471-What-is-Shields)にはアンチフィンガープリンティングの機能があります。 以下のオプションはアクセスするすべてのページを対象にするため、[グローバル](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings)に設定することを推奨します。

シールドのオプションは、必要に応じてサイトごとにダウングレードできますが、デフォルトでは以下の設定をおすすめします。

=== "Android"

    <div class="annotate" markdown>

    - [x] *トラッカーと広告をブロック*で**アグレッシブ**を選択
    - [x] **AMPページを自動でリダイレクト**を選択
    - [x] **自動リダイレクト追跡URL**を選択
    - [x] *接続をHTTPSにアップグレードする*で**すべての接続にHTTPSを使用することを要求する（厳格）**を選択
    - [x] （オプション）**スクリプトをブロックする**を選択(1)
    - [x] *クッキーをブロック*で**3rdパーティクッキーをブロック**を選択
    - [x] **フィンガープリントをブロック**を選択
    - [x] **言語設定によるフィンガープリントの防止**を選択

    <details class="warning" markdown>
    <summary>デフォルトのフィルターリストを使用する</summary>

    **コンテンツフィルター**メニューもしくは`brave://adblock`のページから使用するコンテンツフィルターを追加で選択することができます。 この機能は使わず、デフォルトのフィルターの一覧のままにしておくことをお勧めします。 追加のリストを使用すると、他のBraveユーザーから目立つようになり、また、Braveの脆弱性によってリストに悪意のあるルールが追加された場合、攻撃対象となる領域が増えるおそれがあります。

    </details>

    - [x] **このサイトを閉じる際にデータを削除**を選択

    </div>

    1. JavaScriptが無効となり、多くのサイトが正しく表示されなくなります。 修正するには、アドレスバーのシールドアイコンをクリックし、*詳細設定*からこの設定のチェックを外し、サイトごとに例外を設定します。

=== "iOS"

    <div class="annotate" markdown>

    - [x] *トラッカーと広告をブロック*で**アグレッシブ**を選択
    - [x] *接続をHTTPSにアップグレードする*で**厳格**を選択
    - [x] **AMPページを自動でリダイレクト**を選択
    - [x] **自動リダイレクト追跡URL**を選択
    - [x] （オプション）**スクリプトをブロックする**を選択(1)
    - [x] **フィンガープリントをブロック**を選択
    - [x] *自動シュレッダー*で**閉じたタブ**を選択

    <details class="warning" markdown>
    <summary>デフォルトのフィルターリストを使用する</summary>

    **コンテンツフィルター**メニューから使用するコンテンツフィルターを追加で選択することができます。 この機能は使わず、デフォルトのフィルターの一覧のままにしておくことをお勧めします。 追加のリストを使用すると、他のBraveユーザーから目立つようになり、また、Braveの脆弱性によってリストに悪意のあるルールが追加された場合、攻撃対象となる領域が増えるおそれがあります。

    </details>

    </div>

    1. JavaScriptが無効となり、多くのサイトが正しく表示されなくなります。 修正するには、アドレスバーのシールドアイコンをクリックし、*詳細設定*からこの設定のチェックを外し、サイトごとに例外を設定します。

##### 閲覧履歴データの削除（Androidのみ）

- [x] **終了時にデータをクリア**を選択

##### ソーシャルメディアのブロック（Androidのみ）

- [ ] すべてのソーシャルメディアコンポーネントのチェックを外すこと

#### その他のプライバシー設定

=== "Android"

    <div class="annotate" markdown>

    - [x] Select **Disable non-proxied UDP** under [*WebRTC IP handling policy*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
    - \[x\] (Optional) Select **No protection** under *Safe Browsing* (1)
    - [ ] Uncheck **Allow sites to check if you have payment methods saved**
    - [ ] Uncheck **V8 Optimizer** under *Manage V8 security*
    - [x] Select **Close tabs on exit**
    - [ ] **プライバシーを保護したプロダクト分析(P3A)を許可する**のチェックを外す
    - [ ] **診断レポートを自動送信する**のチェックを外す
    - [ ] **毎日の使用状況のpingをBraveに自動送信する**のチェックを外す

    </div>

    1. Brave's [implementation of Safe Browsing](https://support.brave.com/hc/en-us/articles/15222663599629-Safe-Browsing-in-Brave) on Android **does not** proxy [Safe Browsing network requests](https://developers.google.com/safe-browsing/v4/update-api#checking-urls) like its desktop counterpart. This means that your IP address may be seen (and logged) by Google. Note that Safe Browsing is not available for Android devices without Google Play Services.

=== "iOS"

    - [ ] Uncheck **Allow Privacy-Preserving Product Analytics (P3A)**
    - [ ] **毎日の使用状況のpingをBraveに自動送信する**のチェックを外す

#### Leo

These options can be found in :material-menu: → **Settings** → **Leo**.

<div class="annotate" markdown>

- [ ] Uncheck **Show autocomplete suggestions in address bar** (1)

</div>

1. This option is not present in Brave's iOS app.

#### Search engines

These options can be found in :material-menu:/:fontawesome-solid-ellipsis: → **Settings** → **Search engines**.

- [ ] **検索候補を表示する**からチェックを外す

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync)により、ブラウジングデータ（履歴、ブックマークなど）をすべてのデバイスで利用可能にします。アカウントは不要でE2EE（エンドツーエンド暗号化）で保護されます。

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

### 推奨する設定

These options can be found in :material-menu: → :gear: **Settings** → **Privacy and security**.

#### Browsing data

- [x] Select **Close all open tabs on exit**

#### Incognito mode

- [x] Select **Open external links in incognito**

#### セキュリティー

- [x] Select **Always use secure connections**

この機能により、意図せずプレーンテキストのHTTPでウェブサイトに接続することを防ぎます。 HTTP is extremely uncommon nowadays, so this should have little to no impact on your day-to-day browsing.

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

#### 検索

- [ ] Disable **Search Engine Suggestions**

This setting sends whatever you type in the address bar to the search engine set in Safari. 「検索候補を表示する」機能を無効化することで検索エンジンに送る情報をより厳密に決めることができます。

#### Profiles

Safari allows you to separate your browsing with different profiles. All of your cookies, history, and website data are separate for each profile. You should use different profiles for different purposes e.g. Shopping, Work, or School.

#### プライバシーとセキュリティ

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

#### iCloud同期

Safariの履歴、タブグループ、iCloudタブ、保存されたパスワードの同期は端末間暗号化によって行われます。 However, by default, bookmarks are [not](https://support.apple.com/HT202303). Apple can decrypt and access them in accordance with their [privacy policy](https://apple.com/legal/privacy/en-ww).

You can enable E2EE for your Safari bookmarks and downloads by enabling [Advanced Data Protection](https://support.apple.com/HT212520). Go to :gear: **Settings** → **iCloud** → **Advanced Data Protection**.

- [x] Turn on **Advanced Data Protection**

If you use iCloud with Advanced Data Protection disabled, we also recommend setting Safari's default download location to a local folder on your device. This option can be found in :gear: **Settings** → **Apps** → **Safari** → **General** → **Downloads**.

## 規準

**私たちは、推奨するどのプロジェクトとも提携していないことに注意してください。** [標準的な基準](about/criteria.md) に加えて、客観的な推奨事項を提供できるようにするために明確な要件を定めています。 プロジェクトを利用する前に、このリストをよく理解し、ご自身で調査を行って、そのプロジェクトがあなたにとって適切な選択かどうかをご確認ください。

### 最低要件

- 自動アップデートに対応していること。
- Must receive engine updates from upstream releases quickly.
- Must support content blocking.
- ブラウザをよりプライバシーを尊重したものにするための変更が、ユーザーエクスペリエンスを損なうものではないこと。
