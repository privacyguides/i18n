---
meta_title: "プライバシーを尊重したPCとMac向けウェブブラウザ - Privacy Guides"
title: "デスクトップブラウザ"
icon: material/laptop
description: These privacy-protecting browsers are what we currently recommend for standard/non-anonymous internet browsing on desktop systems.
cover: desktop-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: プライベートデスクトップブラウザの推奨事項
    url: "./"
    relatedLink: "../mobile-browsers/"
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Mullvad Browser
    image: /assets/img/browsers/mullvad_browser.svg
    url: https://mullvad.net/ja/browser
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
    sameAs: https://ja.wikipedia.org/wiki/Mozilla_Firefox
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
    sameAs: https://ja.wikipedia.org/wiki/Brave_(ウェブブラウザ)
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@type": WebPage
      url: "./"
---

<small>Protects against the following threat(s):</small>

- [:material-account-cash: Surveillance Capitalism](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

These are our currently recommended **desktop web browsers** and configurations for standard/non-anonymous browsing. 強力なプライバシー保護とフィンガープリント対策を重視する場合は[Mullvad Browser](#mullvad-browser)を、カジュアルなブラウジングやGoogle Chromeの良い代替品を探している場合は[Firefox](#firefox)を、Chromiumブラウザとの互換性が必要な場合は[Brave](#brave)をおすすめします。

匿名でインターネットを閲覧するには、[Tor](tor.md)を使用してください。 このページではいくつかの設定をおすすめしていますが、Tor Browser以外のブラウザは、何らかの方法で、*誰かしら*が、あなたを追跡できます。

## Mullvad Browser

<div class="admonition recommendation" markdown>

![Mullvad Browser logo](assets/img/browsers/mullvad_browser.svg){ align=right }

**Mullvad Browser** is a version of [Tor Browser](tor.md#tor-browser) with Tor network integrations removed. It aims to provide to VPN users Tor Browser's anti-fingerprinting browser technologies, which are key protections against [:material-eye-outline: Mass Surveillance](basics/common-threats.md#mass-surveillance-programs){ .pg-blue }. Tor Projectが開発し、[Mullvad](vpn.md#mullvad)が配布しています。MullvadのVPNを使用する必要は**ありません**。

[:octicons-home-16: Homepage](https://mullvad.net/en/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser){ .card-link title="Documentation" }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://mullvad.net/en/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

</details>

</div>

[Tor Browser](tor.md)と同様に、Mullvad Browserは、あなたのブラウザのフィンガープリントを他のすべてのMullvadユーザーと同一にすることで、フィンガープリンティングを防ぐよう設計されています。また、*Standard（標準）*、*Safer（より安全）*、*Safest（最も安全）*の3つのデフォルトのセキュリティレベルにより自動的に調整される設定と拡張機能が含まれています。 したがって、デフォルトの[セキュリティレベル](https://tb-manual.torproject.org/security-settings)を調整する以外には、ブラウザを一切変更しないことが重要です。 その他の変更を加えた場合、あなたのブラウザのフィンガープリントは一意のものとなり、このブラウザを使う意味が無くなってしまいます。 ブラウザをより詳細に設定したい場合で、フィンガープリントが重要でない場合は、代わりに[Firefox](#firefox)を推奨します。

### フィンガープリント対策

**[VPN](vpn.md)**を使用しなくても、Mullvad Browserを使えば、Firefox+[Arkenfox](#arkenfox-advanced)や[Brave](#brave)などの他のプライベートブラウザと同様に、[初歩的なフィンガープリントスクリプト](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting)から身を守ることができます。 Mullvad Browserは、他のプライベートブラウザーに備わる柔軟性や利便性に代えて、デフォルトでこれらの保護機能を提供しています。

==最も強力なフィンガープリンティングの保護を求めるなら、Mullvadまたは他の推奨されるVPNプロバイダーと**併せて**、Mullvad Browserを使うことを推奨します==。 VPNをMullvad Browserと併用すると、他の多くのユーザーと同じフィンガープリントとIPアドレスを共有することになり、「群衆」の中に紛れ込むことができます。 これは高度なトラッキングスクリプトを阻止する唯一の方法であり、また、Tor Browserが使用しているのと同じフィンガープリンティング対策技術です。

なお、Mullvad BrowserはどのVPNプロバイダーとも併用することができますが、この「群衆」が存在するには、そのVPNを使用している他の人々もまた、Mullvad Browserを使用している必要があります。Mullvad BrowserのローンチとMullvad VPNが非常に近いことを考慮すると、これは他のVPNプロバイダーよりも、Mullvad VPNにおいて見られる可能性が高いです。 Mullvad Browserには、組み込みのVPN接続機能は備わっていません。また、ブラウザを使用する前にVPNを使用しているかどうかを確認する機能もありません。VPN接続については、別途設定し、管理する必要があります。

Mullvad Browserには、*uBlock Origin*と*NoScript*の拡張機能が予めインストールされています。 私たちは通常、*追加の*[拡張機能](browser-extensions.md)をインストールすることは推奨していません。あらかじめインストールされている拡張機能を削除したり、デフォルトの設定を変更したりするべきでは**ありません**。あなたのブラウザのフィンガープリントが他のMullvad Browserユーザーと異なるものになってしまいます。 また、予めインストールされているMullvad Browser Extensionは、ブラウザのフィンガープリントに影響を及ぼさずに安全に削除*できます*が、Mullvad VPNを使用しない場合でもインストールしたままにしておくのが安全です。

### プライベートブラウジングモード

Mullvad Browserは常にプライベートブラウジングモードで動作します。履歴、クッキー、その他サイトに関するデータは、ブラウザを閉じるたびに消去されます。 ブックマーク、ブラウザの設定、拡張機能の設定は引き続き保持されます。

これは、高度な形式のトラッキングを防ぐために必要ですが、これによって利便性が減少したり、Firefoxの一部の機能（例えば、Multi-Account Containersなど）が使えなくなったりします。 常に複数のブラウザを使用できることを覚えておいてください。たとえば、ログインしたままにしたいサイトや、Mullvad Browserでは正しく動作しないサイトについては Firefox + Arkenfox を使い、一般的なブラウジングには Mullvad Browserを使うといった方法が考えられます。

### Mullvad Leta

Mullvad Browser comes with DuckDuckGo set as the default [search engine](search-engines.md), but it also comes pre-installed with **Mullvad Leta**, a search engine which requires an active Mullvad VPN subscription to access. Mullvad Leta queries Google's paid search API directly, which is why it is limited to paying subscribers. However, it is possible for Mullvad to correlate search queries and Mullvad VPN accounts because of this limitation. MullvadはVPN加入者について非常に少ない情報しか収集していませんが、以上の理由より、Mullvad Letaの使用は推奨されません。

## Firefox

<div class="admonition recommendation" markdown>

![Firefoxのロゴ](assets/img/browsers/firefox.svg){ align=right }

**Firefox**は、[強化型トラッキング防止](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop)などの強力なプライバシー設定を提供し、[様々な種類のトラッキング](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop#w_what-enhanced-tracking-protection-blocks)をブロックするのに役立ちます。

[:octicons-home-16: Homepage](https://firefox.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/firefox){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.mozilla.org/products/firefox){ .card-link title="Documentation" }
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.mozilla.org){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://mozilla.org/firefox/windows)
- [:simple-apple: macOS](https://mozilla.org/firefox/mac)
- [:simple-linux: Linux](https://mozilla.org/firefox/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">注意</p>

Firefoxは、Mozillaのウェブサイトからのダウンロードに固有の[ダウンロードトークン](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c)が含まれており、トークンを送信するために Firefox のテレメトリーを使用しています。 このトークンは[Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/)からのリリースには含まれて**いません**

</div>

### 推奨するFirefoxの設定

これらのオプションは :material-menu: → **設定**にあります。

#### 検索

- [ ] Uncheck **Show search suggestions**

お住まいの地域では検索提案機能が利用できない場合があります。

検索提案機能は、実際に検索を行うかどうかに関わらず、アドレスバーに入力したすべての文字をデフォルトの検索エンジンに送信します。 検索提案機能を無効にすることで、検索エンジンプロバイダーに送信するデータを、より正確に制御することができます。

##### Firefox Suggest (アメリカのみ)

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest)は、米国でのみ利用可能な検索提案機能と似た機能です。 私たちは、検索提案機能の無効化を推奨するのと同じ理由で、これを無効にすることを推奨します。 **アドレスバー**のヘッダーの下に以下のオプションが表示されない場合、この機能は備わっていないので、これらの変更を無視しても問題ありません。

- [ ] Uncheck **Suggestions from Firefox**
- [ ] **スポンサーからの提案**のチェックを外すこと

#### プライバシーとセキュリティ

##### 強化型トラッキング防止機能

- [x] 強化型トラッキング防止機能で**厳格**を選択する

これにより、ソーシャルメディアのトラッカー、フィンガープリンティングスクリプト（*すべての*フィンガープリンティングから保護するわけではありません）、暗号通貨のマイニングプログラム、クロスサイトのトラッキングクッキー、その他の追跡コンテンツをブロックすることであなたを保護します。 ETPは多くの一般的な脅威に対抗しますが、サイトの利便性にほとんど影響を与えないように設計されているため、すべてのトラッキング手段をブロックするわけではありません。

##### 終了時のクリーンアップ

特定のサイトにログインしたままにしたい場合は、**Cookie とサイトデータ** → **例外の管理...**で例外を許可することができます。

- [x] **Firefox を閉じたときに Cookie とサイトデータを削除する**にチェックをつける

これにより、永続的なクッキーからは保護されますが、1回の閲覧セッション中に取得されたクッキーからは保護されません。 これを有効にすると、Firefoxを再起動するだけで、ブラウザのクッキーを簡単に削除できるようになります。 よく訪れる特定のサイトにログインしたままにしたい場合は、サイトごとに例外を設定することができます。

##### テレメトリー

- [ ] **Firefox が技術的な対話データを Mozilla へ送信することを許可する**のチェックを外す
- [ ] **Firefox に調査のインストールと実行を許可する**のチェックを外す
- [ ] **Firefox があなたに代わって未送信のクラッシュレポートを送信することを許可する**のチェックを外すこと

According to Mozilla's privacy policy for Firefox,

> Firefox は、Firefoxのバージョンと言語、デバイスのオペレーティングシステムとハードウェア構成、メモリー、クラッシュやエラーに関する基本情報、アップデート、セーフブラウジング、アクティベーションなどの自動処理の結果に関するデータを送信します。 Firefoxが私たちにデータを送信するとき、あなたのIPアドレスは一時的に私たちのサーバーログの一部として収集されます。

Additionally, the Mozilla Accounts service collects [some technical data](https://mozilla.org/privacy/mozilla-accounts). If you use a Mozilla Account you can opt out:

1. [accounts.firefox.comのプロフィール設定](https://accounts.firefox.com/settings#data-collection)を開く
2. **データの収集と使用** > **Firefoxアカウントの改善を支援する**のチェックを外す

##### Website Advertising Preferences

- [ ] Uncheck **Allow websites to perform privacy-preserving ad measurement**

With the release of Firefox 128, a new setting for [privacy-preserving attribution](https://support.mozilla.org/kb/privacy-preserving-attribution) (PPA) has been added and [enabled by default](https://blog.privacyguides.org/2024/07/14/mozilla-disappoints-us-yet-again-2). PPA allows advertisers to use your web browser to measure the effectiveness of web campaigns, instead of using traditional JavaScript-based tracking. We consider this behavior to be outside the scope of a user agent's responsibilities, and the fact that it is disabled by default in Arkenfox is an additional indicator for disabling this feature.

##### HTTPS-Only Mode

- [x] **すべてのウィンドウで HTTPS-Only モードを有効にする**を選択する

これにより、意図せずにプレーンテキストのHTTPでウェブサイトに接続することを防ぎます。 Sites without HTTPS are uncommon nowadays, so this should have little to no impact on your day-to-day browsing.

##### DNS over HTTPS

[DNS over HTTPSプロバイダー](dns.md)を使用している場合は、

- [x] Select **Max Protection** and choose a suitable provider

Max Protection enforces the use of DNS over HTTPS, and a security warning will show if Firefox can’t connect to your secure DNS resolver, or if your secure DNS resolver says that records for the domain you are trying to access do not exist. This stops the network you're connected to from secretly downgrading your DNS security.

#### Sync

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy)は、あなたの閲覧データ（履歴、ブックマークなど）をすべてのデバイスでアクセス可能にし、それをE2EEで保護します。

### Arkenfox（高度）

<div class="admonition tip" markdown>
<p class="admonition-title">高度なフィンガープリンティング対策にはMullvad Browserを使用してください</p>

[Mullvad Browser](#mullvad-browser)は、初期設定でArkenfoxと同じフィンガープリンティング対策を行っています。なお、この機能を利用するためにMullvadのVPNを使用する必要はありません。 VPNと組み合わせることで、Mullvad BrowserはArkenfoxにはできない仕方で、より高度な追跡スクリプトを阻止することができます。 Arkenfoxには、より柔軟性があり、ログインしたままである必要があるウェブサイトに対してサイトごとの例外を許可するという利点があります。

</div>

[Arkenfoxプロジェクト](https://github.com/arkenfox/user.js)は、Firefoxのための慎重に考えられたオプションのセットを提供しています。 If you [decide](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not) to use Arkenfox, a [few options](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common]) are subjectively strict and/or may cause some websites to not work properly—which you can [easily change](https://github.com/arkenfox/user.js/wiki/3.1-Overrides) to suit your needs. プロジェクトの[wiki](https://github.com/arkenfox/user.js/wiki)に全て目を通すことを**強くお勧めします**。 Arkenfoxは[コンテナ](https://support.mozilla.org/kb/containers#w_for-advanced-users)のサポートも可能にしています。

Arkenfoxでは、canvasのランダム化やFirefoxの組み込みのフィンガープリント対策の設定に基づき、基本的または単純なトラッキングスクリプトを防ぐことを唯一の目的としています。 Arkenfoxは、Mullvad BrowserやTor Browserが行う、高度なフィンガープリントトラッキング用のスクリプを防止する唯一の方法である大勢のユーザーの中に溶け込ませることは目的としていません。 Remember that you can always use multiple browsers, for example, you could consider using Firefox+Arkenfox for a few sites that you want to stay logged in on or otherwise trust, and Mullvad Browser for general browsing.

## Brave

<div class="admonition recommendation annotate" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

**Brave ブラウザ** にはコンテンツブロッカーと[プライバシー機能](https://brave.com/privacy-features)が組み込まれており、その多くはデフォルトで有効になっています。

BraveはChromiumウェブブラウザプロジェクトに基づいて構築されているため、使い慣れた使用感があるほか、ウェブサイトの互換性問題が最小限に抑えられます。

[:octicons-home-16: Homepage](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.brave.com){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:fontawesome-brands-windows: Windows](https://brave.com/download)
- [:simple-apple: macOS](https://brave.com/download)
- [:simple-linux: Linux](https://brave.com/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/com.brave.Browser)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">注意</p>

Brave adds a "[referral code](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)" to the file name in downloads from the Brave website, which is used to track which source the browser was downloaded from, for example `BRV002` in a download named `Brave-Browser-BRV002.pkg`. The installer will then ping Brave's server with the referral code at the end of the installation process. これが心配な場合は、インストーラファイルを開く前に名前を変更できます。

</div>

### 推奨するBraveの設定

これらのオプションは :material-menu: → **設定**にあります。

#### Shields

Brave includes some anti-fingerprinting measures in its [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) feature. We suggest configuring these options [globally](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) across all pages that you visit.

シールドのオプションは、必要に応じてサイトごとにダウングレードできますが、デフォルトでは以下の設定をおすすめします。

<div class="annotate" markdown>

- [x] Select **Aggressive** under *Trackers & ads blocking*

<details class="warning" markdown>
<summary>Use default filter lists</summary>

Brave allows you to select additional content filters within the internal `brave://adblock` page. この機能は使わず、デフォルトのフィルターの一覧のままにしておくことをお勧めします。 追加のリストを使用すると、他のBraveユーザーから目立つようになり、また、Braveの脆弱性によってリストに悪意のあるルールが追加された場合、攻撃対象となる領域が増えるおそれがあります。

</details>

- [x] Select **Strict** under *Upgrade connections to HTTPS*
- [x] (Optional) Select **Block Scripts** (1)
- [x] Check **Block fingerprinting**
- [x] Select **Block third-party cookies**
- [x] Check **Forget me when I close this site** (2)
- [ ] Uncheck all social media components

</div>

1. This option disables JavaScript, which will break a lot of sites. To fix them, you can set exceptions on a per-site basis by clicking on the Shield icon in the address bar and unchecking this setting under *Advanced controls*.
2. If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis by clicking on the Shield icon in the address bar and unchecking this setting under *Advanced controls*.

#### Privacy and security

<div class="annotate" markdown>

- [x] Select **Don't allow sites to use the V8 optimizer** under *Security* → *Manage V8 security* (1)
- [x] Select **Automatically remove permissions from unused sites** under *Sites and Shields Settings*
- [x] Select **Disable non-proxied UDP** under [*WebRTC IP Handling Policy*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
- [ ] Uncheck **Use Google services for push messaging**
- [x] Select **Auto-redirect AMP pages**
- [x] Select **Auto-redirect tracking URLs**
- [x] Select **Prevent sites from fingerprinting me based on my language preferences**

</div>

1. Disabling the V8 optimizer reduces your attack surface by disabling [*some*](https://grapheneos.social/@GrapheneOS/112708049232710156) parts of JavaScript Just-In-Time (JIT) compilation.

<div class="admonition tip" markdown>
<p class="admonition-title">Sanitizing on close</p>

- [x] Select **Delete data sites have saved to your device when you close all windows** under *Sites and Shields Settings* → *Content* → *Additional content settings* → *On-device site data*.

If you wish to stay logged in to a particular site you visit often, you can set exceptions on a per-site basis under the *Customized behaviors* section.

</div>

##### Tor windows

[**Private Window with Tor**](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity) allows you to route your traffic through the Tor network in Private Windows and access .onion services, which may be useful in some cases. However, Brave is **not** as resistant to fingerprinting as the Tor Browser is, and far fewer people use Brave with Tor, so you will stand out. If your threat model requires strong anonymity, use the [Tor Browser](tor.md#tor-browser).

##### Data Collection

- [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
- [ ] Uncheck **Automatically send daily usage ping to Brave**
- [ ] Uncheck **Automatically send diagnostic reports**

#### Web3

BraveのWeb3機能はブラウザのフィンガープリントなど攻撃面を潜在的に増やす可能性があります。 Unless you use any of these features, they should be disabled.

- Select **Extensions (no fallback)** under *Default Ethereum wallet*
- Select **Extensions (no fallback)** under *Default Solana wallet*

#### Extensions

- [ ] Uncheck all built-in extensions you don't use

#### Search engine

We recommend disabling search suggestions in Brave for the same reason we recommend disabling this feature in [Firefox](#search).

- [ ] Uncheck **Show search suggestions**

#### System

<div class="annotate" markdown>

- [ ] Uncheck **Continue running apps when Brave is closed** to disable background apps (1)

</div>

1. このオプションはすべてのプラットフォームにあるわけではありません。

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync) allows your browsing data (history, bookmarks, etc.) to be accessible on all your devices without requiring an account and protects it with E2EE.

#### Brave Rewards and Wallet

**Brave Rewards** lets you receive Basic Attention Token (BAT) cryptocurrency for performing certain actions within Brave. It relies on a custodial account and KYC from a select number of providers. We do not recommend BAT as a [private cryptocurrency](cryptocurrency.md), nor do we recommend using a [custodial wallet](advanced/payments.md#wallet-custody), so we would discourage using this feature.

**Brave Wallet** operates locally on your computer, but does not support any private cryptocurrencies, so we would discourage using this feature as well.

## 規準

**私たちは、推薦するどのプロジェクトとも提携していません。**客観的に推薦できるよう、[標準となる規準](about/criteria.md)に加えて、一連の明確な要件を定めています。 プロジェクトを利用する前に、このリストをよく理解し、ご自身で調査を行って、そのプロジェクトがあなたにとって適切な選択かどうかをご確認ください。

### 最低要件

- オープンソースのソフトウェアであること。
- 自動アップデートに対応していること。
- Must receive engine updates in 0-1 days from upstream release.
- Must be available on Linux, macOS, and Windows.
- Any changes required to make the browser more privacy-respecting must not negatively impact user experience.
- Must block third-party cookies by default.
- Must support [state partitioning](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning) to mitigate cross-site tracking.[^1]

### 満たされることが望ましい基準

満たされることが望ましい基準には、このカテゴリーの完璧なプロジェクトに私たちが望むものを示しています。 私たちが推薦するプロジェクトは、この機能の一部または全部を含んでいないかもしれませんが、もし含んでいれば、このページで他のプロジェクトよりも上位にランクされるかもしれません。

- Should include built-in content blocking functionality.
- Should support cookie compartmentalization (à la [Multi-Account Containers](https://support.mozilla.org/kb/containers)).
- Should support Progressive Web Apps (PWAs). PWAs enable you to install certain websites as if they were native apps on your computer. This can have advantages over installing Electron-based apps because PWAs benefit from your browser's regular security updates.
- Should not include add-on functionality (bloatware) that does not impact user privacy.
- Should not collect telemetry by default.
- Should provide an open-source sync server implementation.
- Should default to a [private search engine](search-engines.md).

[^1]: Braveの実装は[Brave プライバシーアップデートで詳しく説明されています: プライバシーのためのネットワーク状態のパーティショニング](https://brave.com/privacy-updates/14-partitioning-network-state)
