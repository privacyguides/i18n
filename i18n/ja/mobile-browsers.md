---
meta_title: "プライバシーを尊重するAndroidとiOS向けウェブブラウザ - Privacy Guides"
title: モバイルブラウザー
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
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1052879175)
- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:simple-fdroid: F-Droid](https://brave-browser-apk-release.s3.brave.com/fdroid/repo/index.html)

</details>

</div>

### 推奨するBraveの設定

本当に匿名でインターネットを閲覧する唯一の方法は、Tor Browserを使うことです。 Braveを使用する際は、特定の相手からプライバシーを保護するために以下の設定を変更することをお勧めしますが、 [Tor Browser](tor.md#tor-browser) 以外のブラウザーについては、*誰か*が何らかの形で追跡することができます。

=== "Android"

    These options can be found in :material-dots-vertical: → **Settings** → **Brave Shields & privacy**.

=== "iOS"

    These options can be found in :material-dots-horizontal: → **All Settings** → **Shields & Privacy**.

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

    - [x] *自動シュレッダー*で**閉じたタブ**を選択

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

#### その他のプライバシー設定

=== "Android"

    <div class="annotate" markdown>

    - [x] （オプション）*セーフ ブラウジング*で**保護なし**を選択 (1)
    - [x] [*WebRTC IP処理ポリシー*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)で**非プロキシUDPを無効にする**を選択
    - [ ] **お支払い方法を保存しているかどうかの確認をサイトに許可する**のチェックを外す
    - [x] Select **Do not speed up sites with Brave's V8 engine but make Brave slightly more resistant to attacks**
    - [x] **終了時にタブを閉じる**を選択
    - [ ] **プライバシーを保護したプロダクト分析(P3A)を許可する**のチェックを外す
    - [ ] **診断レポートを自動送信する**のチェックを外す
    - [ ] **毎日の使用状況のpingをBraveに自動送信する**のチェックを外す

    </div>

    1. Android版Braveの[セーフブラウジングの実装](https://support.brave.com/hc/en-us/articles/15222663599629-Safe-Browsing-in-Brave)はデスクトップ版のように[セーフブラウジングネットワークリクエスト](https://developers.google.com/safe-browsing/v4/update-api#checking-urls)を経由**しません**。 GoogleがあなたのIPアドレスを見る（記録する）可能性があります。 Google Playサービスを利用していないAndroid端末ではセーフブラウジングは利用できません。

=== "iOS"

    - [ ] **プライバシーを保護したプロダクト分析(P3A)を許可する**のチェックを外す
    - [ ] **毎日の使用状況のpingをBraveに自動送信する**のチェックを外す

#### Leo AI

=== "Android"

    These options can be found in :material-dots-vertical: → **Settings** → **Leo AI**.

    - [ ] Uncheck **Show autocomplete suggestions in address bar**

=== "iOS"

    These options can be found in :material-dots-horizontal: → **All Settings** → **Leo AI**.

    - [ ] Uncheck **Show In Quick Search Engine Bar**

#### 検索エンジン

=== "Android"

    These options can be found in :material-dots-vertical: → **Settings** → **Search engines**.

    - [ ] **検索候補を表示する**からチェックを外す

=== "iOS"

    These options can be found in :material-dots-horizontal: → **All Settings** → **Search engines**.

    - [ ] Uncheck **Show In Quick Search Engine Bar**

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync)により、ブラウジングデータ（履歴、ブックマークなど）をすべてのデバイスで利用可能にします。アカウントは不要でE2EE（エンドツーエンド暗号化）で保護されます。

## Safari (iOS)

On iOS, any app that can browse the web is [restricted](https://developer.apple.com/app-store/review/guidelines) to using an Apple-provided [WebKit framework](https://developer.apple.com/documentation/webkit), so a browser like [Brave](#brave) does not use the Blink engine (the core component of Chromium) like its counterparts on other operating systems.

<div class="admonition recommendation" markdown>

![Safari logo](assets/img/browsers/safari.svg){ align=right }

**Safari**はiOSのデフォルトブラウザです。 Safariには、インテリジェント・トラッキング防止機能(https://webkit.org/blog/7675/intelligent-tracking-prevention)、隔離された一時的なタブであるプライベートブラウズタブ、フィンガープリント保護（ウェブサイトに対してシステム構成の簡易版を提示することで、より多くのデバイスが同じに見えるようにする）、フィンガープリントのランダム化などの[プライバシー機能](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/ios)があります。有料のiCloud+サブスクリプション利用者にはプライベートリレーという機能も含まれます。

[:octicons-home-16: ウェブページ](https://apple.com/safari){ .md-button .md-button--primary }
[:octicons-eye-16:](https://apple.com/legal/privacy/data/en/safari){ .card-link title="プライバシーポリシー" }
[:octicons-info-16:](https://support.apple.com/guide/iphone/browse-the-web-iph1fbef4daa/ios){ .card-link title="ドキュメント" }

</details>

</div>

### 推奨するSafariの設定

以下のプライバシー・セキュリティ関連のオプションは、 :gear: **設定**→**アプリ**→**Safari**にあります。

#### Safariにアクセスを許可

**Siri**：

- [ ] **このアプリから学習**を無効化
- [ ] **アプリに表示**を無効化
- [ ] **ホーム画面に表示**を無効化
- [ ] Disable **Suggest App**

これにより、SiriがSafari内のコンテンツを使って提案できなくなります。

#### 検索

- [ ] Disable **Search Engine Suggestions**

この設定がONだと、アドレスバーに入力した内容がすべてSafariに設定された検索エンジンに送られてしまいます。 「検索候補を表示する」機能を無効化することで検索エンジンに送る情報をより厳密に決めることができます。

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
