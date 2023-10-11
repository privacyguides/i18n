---
meta_title: "プライバシーを尊重したPCとMac向けウェブブラウザ - Privacy Guides"
title: "デスクトップブラウザ"
icon: material/laptop
description: これらのウェブブラウザは、Google Chromeよりも強力なプライバシー保護を提供します。
cover: desktop-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: プライベートデスクトップブラウザの推奨
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

以下は、一般的な、非匿名のブラウジング用に、現在おすすめされているデスクトップ版のウェブブラウザとその設定です。 強力なプライバシー保護とフィンガープリント対策を重視する場合は[Mullvad Browser](#mullvad-browser)を、カジュアルなブラウジングやGoogle Chromeの良い代替品を探している場合は[Firefox](#firefox)を、Chromiumブラウザとの互換性が必要な場合は[Brave](#brave)をおすすめします。

匿名でインターネットを閲覧するには、[Tor](tor.md)を使用してください。 このページではいくつかの設定をおすすめしていますが、Tor Browser以外のブラウザは、何らかの方法で、*誰かしら*が、あなたを追跡できます。

## Mullvad Browser

!!! recommendation

    ![Mullvad Browserのロゴ](assets/img/browsers/mullvad_browser.svg){ align=right }
    
    **Mullvad Browser**はVPNユーザーにTor Browserのフィンガープリント対策のブラウザ技術を提供することを目的とした、Torネットワークへの接続機能のない[Tor Browser](tor.md#tor-browser)です。 Tor Projectが開発し、[Mullvad](vpn.md#mullvad)が配布しています。MullvadのVPNを使用する必要は**ありません**。
    
    [:octicons-home-16: ホームページ](https://mullvad.net/ja/browser){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://mullvad.net/ja/help/privacy-policy/){ .card-link title="プライバシーポリシー" }
    [:octicons-info-16:](https://mullvad.net/ja/help/tag/mullvad-browser/){ .card-link title=ドキュメント}
    [:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="ソースコード" }
    
    ??? ダウンロード
    
        - [:simple-windows11: Windows](https://mullvad.net/en/download/browser/windows)
        - [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
        - [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

[Torブラウザ](tor.md)と同様に、Mullvadブラウザは、あなたのブラウザのフィンガープリントを他のすべてのMullvadユーザーと同一にすることでフィンガープリントを防ぐように設計されています。また、デフォルトのセキュリティレベル：*Standard（標準）*、*Safer（より安全）*、*Safest（最も安全）*によって自動的に設定されるデフォルトの設定と拡張機能が含まれています。 したがって、[デフォルトのセキュリティレベル](https://tb-manual.torproject.org/security-settings/)を調整する以外の変更をしないことが大事です。 その他の変更は、あなたのフィンガープリントを特有なものにし、このブラウザを使用する目的を失うことになるでしょう。 ブラウザをより詳細に設定し、フィンガープリントも気にならない場合は、代わりに[Firefox](#firefox)を推奨します。

### フィンガープリント対策

**[VPN](vpn.md)**を使用せずとも、MullvadブラウザはFirefox+[Arkenfox](#arkenfox-advanced)や[Brave](#brave)などの他のプライベートブラウザと同様に、[初歩的なフィンガープリントスクリプト](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting)に対する保護を提供します。 Mullvad Browserは、そのままでこれらの保護機能を提供しますが、その一方で、他のプライベートブラウザが提供できる柔軟性と利便性を犠牲にしています。

==最強のフィンガープリンティング保護を求めるのであれば、Mullvadであろうと他の推奨されるVPNプロバイダであろうと、VPNと**併用**してMullvad Browserを使用することを推奨します==。 VPNをMullvad Browserと併用すると、多数の他のユーザーと同じフィンガープリントとIPアドレスを共有することになり、あなたは"群衆"の中に溶け込むことができます。 この戦略は高度なトラッキングスクリプトを阻止する唯一の方法であり、Torブラウザが使用しているのと同じ対フィンガープリンティング技術です。

注意してください。Mullvad BrowserはどのVPNプロバイダとも使用することができますが、そのVPNを使用している他のユーザーもMullvad Browserを使用している必要があります。この"群衆"が存在するためには、Mullvad VPNにおいて他のプロバイダよりも特にMullvad Browserのリリース直前において、それがより可能性が高いです。 Mullvad Browserは、組み込みのVPN接続機能がなく、ブラウジングする前にVPNを使用しているかどうかを確認する機能もありません。VPN接続は別途設定し、管理する必要があります。

Mullvad Browserには、*uBlock Origin*と*NoScript*のブラウザ拡張機能が事前にインストールされています。 通常、*余分な*ブラウザ拡張機能の追加は[推奨していません](#extensions)が、ブラウザに事前にインストールされているこれらの拡張機能は、デフォルトの設定を変更したり削除したりしないでください。それを行うと、あなたのフィンガープリントが他のMullvad Browserユーザーと比べ特有なものになるからです。 また、Mullvad Browser Extensionも事前にインストールされており、必要に応じて安全に削除してもブラウザのフィンガープリントに影響を及ぼしません。Mullvad Vpnを使用しない場合でも保持しておいても安全です。

### プライベートブラウジングモード

Mullvad Browserは常にプライベートブラウジングモードで動作します。つまり、履歴、クッキー、その他のサイトデータはブラウザを閉じるたびに常にクリアされます。 しかし、ブックマーク、ブラウザ設定、拡張機能の設定は保存され続けます。

これは、高度な形式のトラッキングを防ぐために必要ですが、便利さやFirefoxの一部の機能（例えば、Multi-Account Containersなど）を犠牲にしています。 常に複数のブラウザを使用することができます。例えば、ログインしたままにしたいサイトや、Mullvad Browserでは正しく動作しないサイトについてはFirefox+Arkenfoxを使用し、一般的なブラウジングにはMullvad Browserを使用するといった方法を考えることができます。

### Mullvad Leta

Mullvad Browserはデフォルトの[検索エンジン](search-engines.md)としてDuckDuckGoが設定されていますが、Mullvad VPNの有効なサブスクリプションが必要な検索エンジン、**Mullvad Leta**も事前にインストールされています。 Mullvad LetaはGoogleの有料検索APIに直接問い合わせます（そのため、有料加入者に限定されます）。しかし、この制限のため、Mullvadは検索クエリとMullvad VPNのアカウントを相関させることが可能です。 このため、MullvadがVPN加入者について非常に少ない情報しか収集していないにもかかわらず、Mullvad Letaの使用はおすすめしません。

## Firefox

!!! recommendation

    ![Firefoxのロゴ](assets/img/browsers/firefox.svg){ align=right }
    
    **Firefox**は、[強化型トラッキング防止](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop)などの強力なプライバシー設定を提供し、[様々な種類のトラッキング](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop#w_what-enhanced-tracking-protection-blocks)をブロックするのに役立ちます。
    
    [:octicons-home-16: ホームページ](https://firefox.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.mozilla.org/privacy/firefox/){ .card-link title="プライバシーポリシー" }
    [:octicons-info-16:](https://firefox-source-docs.mozilla.org/){ .card-link title=文書}
    [:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="ソースコード" }
    [:octicons-heart-16:](https://donate.mozilla.org/){ .card-link title=貢献 }
    
    ??? ダウンロード
    
        - [:simple-windows11: Windows](https://www.mozilla.org/firefox/windows)
        - [:simple-apple: macOS](https://www.mozilla.org/firefox/mac)
        - [:simple-linux: Linux](https://www.mozilla.org/firefox/linux)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.mozilla.firefox)

!!! 警告
FirefoxはMozillaのウェブサイトからのダウンロードにユニークな[ダウンロードトークン](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0)を含み、このトークンを送信するためにFirefox内のテレメトリーを使用します。 このトークンは、[Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/)からのリリースには**含まれません**。

### おすすめの設定

これらのオプションは、:material-menu: → **設定**で見つけることができます。

#### 検索

- [ ] **検索候補を使用する**のチェックを外す

あなたの地域では検索提案機能の利用はできないかもしれません。

検索候補は、実際に検索を行うかどうかに関わらず、アドレスバーに入力したすべてのものをデフォルトの検索エンジンに送信します。 検索候補を無効にすることで、あなたが検索エンジンプロバイダに送信するデータをより正確に制御することができます。

#### プライバシーとセキュリティ

##### 強化型トラッキング防止機能

- [x] 強化型トラッキング防止機能で**厳格**を選択する

これにより、ソーシャルメディアのトラッカー、フィンガープリンティングスクリプト（これが*すべての*フィンガープリンティングから保護するわけではないことに注意）、暗号マイナー、クロスサイトのトラッキングクッキー、その他の一部の追跡コンテンツをブロックすることであなたを保護します。 ETPは多くの一般的な脅威に対抗しますが、サイトの利便性にほとんど影響を与えないように設計されているため、すべての追跡経路をブロックするわけではありません。

##### Firefox Suggest (アメリカのみ)

[Firefox Suggest](https://support.mozilla.org/en-US/kb/firefox-suggest)は、米国のみで利用可能な、検索候補と似た機能です。 私たちは、検索候補を無効にすることを推奨するのと同じ理由で、これを無効にすることを推奨します。 **アドレスバー**のヘッダーの下にこれらのオプションが表示されない場合、新しいエクスペリエンスは持っていないので、これらの変更を無視しても問題ありません。

- [ ] **ウェブからの提案**のチェックを外します
- [ ] **スポンサーからの提案**のチェックを外します

##### 終了時にサニタイズ

特定のサイトにログインしたままにしたい場合は、**Cookie とサイトデータ** → **例外の管理...**で例外を許可することができます。

- [x] **Firefox を閉じたときに Cookie とサイトデータを削除する**にチェックをつける

これにより、永続的なクッキーからあなたを保護しますが、一度のブラウジングセッション中に取得されたクッキーからあなたを保護することはありません。 これを有効にすると、Firefoxを再起動するだけで、ブラウザのクッキーを簡単に削除できるようになります。 よく訪れる特定のサイトにログインしたままにしたい場合、サイトごとに例外を設定することができます。

##### テレメトリー

- [ ] **Firefox が技術的な対話データを Mozilla へ送信することを許可する**のチェックを外す
- [ ] **Firefox に調査のインストールと実行を許可する**のチェックを外す
- [ ] **Firefox があなたに代わって未送信のクラッシュレポートを送信することを許可する**のチェックを外します

> Firefoxは、あなたのFirefoxのバージョンや言語、デバイスのオペレーティングシステムとハードウェア構成、メモリ、クラッシュやエラーに関する基本情報、アップデートやセーフブラウジング、アクティベーションなどの自動化されたプロセスの結果などのデータを私たちに送信します。 Firefoxが私たちにデータを送信するとき、あなたのIPアドレスは一時的に私たちのサーバーログの一部として収集されます。

さらに、Firefoxアカウントサービスは[一部の技術データ](https://www.mozilla.org/ja/privacy/firefox/#firefox-accounts)を収集します。 Firefoxアカウントを使用している場合は、オプトアウトすることができます：

1. [accounts.firefox.comのプロフィール設定](https://accounts.firefox.com/settings#data-collection)を開きます
2. **データの収集と使用** > **Firefoxアカウントの改善を支援する**のチェックを外します

##### HTTPS-Only モード

- [x] **すべてのウィンドウで HTTPS-Only モードを有効にする**を選択する

これにより、意図せずにプレーンテキストのHTTPでウェブサイトに接続することを防ぎます。 現在ではHTTPSを使用していないサイトは珍しいため、日常的なブラウジングにほとんど影響を及ぼさないはずです。

#### 同期

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy/)は、あなたのブラウジングデータ（履歴、ブックマークなど）をすべてのデバイスで利用可能にし、それをE2EE（End-to-End Encryption, 端末間暗号化）で保護します。

### Arkenfox（高度）

!!! ヒント "高度なフィンガープリンティング対策にはMullvad Browserを使用してください"

    [Mullvad Browser](#mullvad-browser)は、初期設定からArkenfoxと同じフィンガープリンティング対策を提供し、これらの保護を利用するためにMullvadのVPNを使用する必要はありません。 VPNと組み合わせることで、Mullvad BrowserはArkenfoxにはできない、より高度な追跡スクリプトを阻止することができます。 Arkenfoxははるかに柔軟性があり、ログインしたままである必要があるウェブサイトに対してサイトごとの例外を許可するという利点があります。

[Arkenfoxプロジェクト](https://github.com/arkenfox/user.js)は、Firefoxのための慎重に考えられたオプションのセットを提供しています。 もし[Arkenfoxを使用することを決定した場合](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not)、[いくつかのオプション](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common])は主観的に厳格であり、または一部のウェブサイトが正しく動作しない可能性があります - これらは[あなたのニーズに合わせて簡単に変更することができます](https://github.com/arkenfox/user.js/wiki/3.1-Overrides)。 私たちは、彼らの[wiki](https://github.com/arkenfox/user.js/wiki)をすべて読むことを**強くお勧めします**。 Arkenfoxは[コンテナ](https://support.mozilla.org/ja/kb/containers#w_for-advanced-users)のサポートも有効にしています。

Arkenfoxは、キャンバスのランダム化やFirefoxの組み込みのフィンガープリント対策の設定を通じて、基本的または単純なトラッキングスクリプトを阻止することを目指しています。 Arkenfoxは、Mullvad BrowserやTor Browserのように、高度なフィンガープリンティングトラッキングスクリプトを防止する唯一の方法である他の多くのArkenfoxユーザーとブラウザを溶け込ませることを目指していません。 常に複数のブラウザを使用できることを覚えておいてください。たとえば、ログインしたままにするか信頼したいいくつかのサイトには Firefox + Arkenfox を使用し、一般的なブラウジングには Mullvad Browserを使用することを検討できます。

## Brave

!!! recommendation

    ![Brave logo](assets/img/browsers/brave.svg){ align=right }
    
    **Brave Browser** には、コンテンツブロッカーと [いくつかのプライバシー機能](https://brave.com/privacy-features/) が内蔵されていて、その多くがデフォルトで有効になっています。
    
    BraveはChromiumウェブブラウザプロジェクトに基づいて構築されているため、使い慣れた使用感、ウェブサイトの互換性問題が最小限に抑えられます。
    
    [:octicons-home-16: ホームページ](https://brave.com/ja/){ .md-button .md-button--primary }
    [:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
    [:octicons-eye-16:](https://brave.com/privacy/browser/){ .card-link title="プライバシーポリシー" }
    [:octicons-info-16:](https://support.brave.com/hc/en-us/categories/360006507272){ .card-link title=ドキュメント}
    [:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="ソースコード" }
    
    ??? ダウンロード
    
        - [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
        - [:simple-windows11: Windows](https://brave.com/download/)
        - [:simple-apple: macOS](https://brave.com/download/)
        - [:simple-linux: Linux](https://brave.com/linux/) (1)

    1. FlatpakバージョンのBraveを使用した場合、ChromiumのサンドボックスがFlatpakのものに置き換えられてしまうため、推奨されません。 さらに、このパッケージはBrave Software, Inc. によるメンテナンスがされていません。

### 推奨する設定

これらのオプションは :material-menu: → **設定**にあります。

#### 設定

##### Shields

Braveは[Shields](https://support.brave.com/hc/en-us/articles/360022973471-What-is-Shields-)の機能にいくつかのフィンガープリント対策を盛り込んでいます。 これらのオプションを訪問したすべてのページにおいて[グローバルに](https://support.brave.com/hc/en-us/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings-)設定することをおすすめします。

Shieldsのオプションは必要に応じてサイトごとにダウングレードできますが、デフォルトでは以下の設定をおすすめします。

<div class="annotate" markdown>

- [x] **言語設定に基づく、サイトのフィンガープリントを禁止** を選択
- [x] トラッカーと広告をブロックで **積極的** を選択

    ??? warning "デフォルトのフィルターリストを使用する"
        Braveでは、 `brave://adblock` ページ内で追加のコンテンツフィルターを選択することができます。 この機能を使用しないで、デフォルトのフィルターリストを維持することをお勧めします。 追加のリストを使用すると、他の Brave ユーザーより目立つようになり、Brave にエクスプロイトがあり、使用するリストの1つに悪意のあるルールが追加された場合に攻撃対象領域が増加する可能性があります。

- [x] **接続をHTTPSにアップグレードする** で **厳格** を選択
- [x] (オプション) **スクリプトをブロックする** を選択 (1)
- [x] フィンガープリンティングをブロックで **厳格、サイトの表示が崩れる可能性** を選択

</div>

1. このオプションはuBlock Originの高度な[ブロックモード](https://github.com/gorhill/uBlock/wiki/Blocking-mode)や[NoScript](https://noscript.net/)拡張機能に似た機能を提供します。

##### ソーシャルメディアのブロック

- [ ] すべてのソーシャルメディアコンポーネントのチェックを外す

##### プライバシーとセキュリティ

<div class="annotate" markdown>

- [x] [WebRTC IP処理ポリシー](https://support.brave.com/hc/en-us/articles/360017989132-How-do-I-change-my-Privacy-Settings-#webrtc) で **非プロキシUDPを無効にする** を選択
- [ ] **プッシュメッセージングにGoogleサービスを使用** のチェックを外す
- [ ] **プライバシーを保護したプロダクト分析 (P3A) を許可する** のチェックを外す
- [ ] **毎日の使用状況のpingをBraveに自動送信する** のチェックを外す
- [ ] **診断レポートを自動送信する** のチェックを外す
- [ ] **Tor搭載のプライベートウィンドウ** (1)  のチェックを外す

    !!! tip "終了時のクリーンアップ"

        - [x] *Cookie と他のサイトデータ* メニューから **すべてのウィンドウを閉じるときに Cookie とサイトデータを削除する** を選択

        頻繁にアクセスする特定のサイトにログインしたままにしたい場合は、 *動作のカスタマイズ* セクションでサイトごとに例外を設定できます。

</div>

1. BraveはTor Browserほどフィンガープリントに対して強く**なく**、BraveでTorを使う人はずっと少ないので目立つでしょう。 [強力な匿名性が必要](https://support.brave.com/hc/en-us/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity-)な場合には[Tor Browser](tor.md#tor-browser)を使用してください。

##### 拡張機能

使わない組み込み**拡張機能**は無効にしてください。

- [ ] **Hangouts** のチェックを外す
- [ ] **WebTorrent** のチェックを外す

##### Web3

BraveのWeb3機能はブラウザのフィンガープリントなど攻撃面を潜在的に増やす可能性があります。 どの機能も使用しないなら、無効にしておくべきです。

- Select **Extensions (no fallback)** under Default Ethereum wallet and Default Solana wallet
- Set **Method to resolve IPFS resources** to **Disabled**

##### システム

<div class="annotate" markdown>

- [ ] Uncheck **Continue running apps when Brave is closed** to disable background apps (1)

</div>

1. このオプションはすべてのプラットフォームにあるわけではありません。

#### 同期

[Brave Sync](https://support.brave.com/hc/en-us/articles/360059793111-Understanding-Brave-Sync)は、あなたのブラウジングデータ(履歴、ブックマークなど)をアカウント不要ですべてのデバイスで利用可能にし、それをE2EEで保護します。

#### Brave Rewards と Wallet

**Brave Rewards**では、Brave内で特定のアクションを実行することで、Basic Attention Token (BAT)という仮想通貨を受け取ることができます。 It relies on a custodial account and KYC from a select number of providers. We do not recommend BAT as a [private cryptocurrency](cryptocurrency.md), nor do we recommend using a [custodial wallet](advanced/payments.md#other-coins-bitcoin-ethereum-etc), so we would discourage using this feature.

**Brave Wallet** operates locally on your computer, but does not support any private cryptocurrencies, so we would discourage using this feature as well.

## 追加のリソース

In general, we recommend keeping your browser extensions to a minimum to decrease your attack surface; they have privileged access within your browser, require you to trust the developer, can make you [stand out](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint), and [weaken](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ) site isolation. However, uBlock Origin may prove useful if you value content blocking functionality.

### uBlock Origin

!!! recommendation

    ![uBlock Originのロゴ](assets/img/browsers/ublock_origin.svg){ align=right }
    
    **uBlock Origin**は、広告、トラッカー、フィンガープリントスクリプトのブロックに役立つ人気のコンテンツブロッカーです。
    
    [:octicons-repo-16: Repository](https://github.com/gorhill/uBlock#readme){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://github.com/gorhill/uBlock/wiki/Privacy-policy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://github.com/gorhill/uBlock/wiki){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/gorhill/uBlock){ .card-link title="Source Code" }
    
    ??? downloads
    
        - [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/ublock-origin/)
        - [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm)
        - [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/ublock-origin/odfafepnkmbhccpbejgmiehpchacaeak)

We suggest following the [developer's documentation](https://github.com/gorhill/uBlock/wiki/Blocking-mode) and picking one of the "modes". Additional filter lists can impact performance and [may increase attack surface](https://portswigger.net/research/ublock-i-exfiltrate-exploiting-ad-blockers-with-css).

##### Other lists

These are some other [filter lists](https://github.com/gorhill/uBlock/wiki/Dashboard:-Filter-lists) that you may want to consider adding:

- [x] Check **Privacy** > **AdGuard URL Tracking Protection**
- Add [Actually Legitimate URL Shortener Tool](https://raw.githubusercontent.com/DandelionSprout/adfilt/master/LegitimateURLShortener.txt)

## 基準

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

!!! example "この項目は最近作成されました"

    We are working on establishing defined criteria for every section of our site, and this may be subject to change. If you have any questions about our criteria, please [ask on our forum](https://discuss.privacyguides.net/latest) and don't assume we didn't consider something when making our recommendations if it is not listed here. There are many factors considered and discussed when we recommend a project, and documenting every single one is a work-in-progress.

### 最低要件

- オープンソース ソフトウェアである必要があります。
- 自動更新に対応している。
- Receives engine updates in 0-1 days from upstream release.
- Linux、macOS、Windowsで利用できる。
- Any changes required to make the browser more privacy-respecting should not negatively impact user experience.
- デフォルトでサードパーティCookieをブロックしている。
- Supports [state partitioning](https://developer.mozilla.org/en-US/docs/Web/Privacy/State_Partitioning) to mitigate cross-site tracking.[^1]

### 最良の場合

Our best-case criteria represents what we would like to see from the perfect project in this category. Our recommendations may not include any or all of this functionality, but those which do may rank higher than others on this page.

- コンテンツブロック機能が内蔵されている。
- Supports cookie compartmentalization (à la [Multi-Account Containers](https://support.mozilla.org/en-US/kb/containers)).
- Supports Progressive Web Apps.  
  PWAs enable you to install certain websites as if they were native apps on your computer. This can have advantages over installing Electron-based apps, because you benefit from your browser's regular security updates.
- ユーザーのプライバシーに影響を与えないアドオン機能（ブロートウェア）が含まれていない。
- テレメトリーをデフォルトで収集しない。
- オープンソースの同期サーバ実装を提供する。
- デフォルトで、[プライベートな検索エンジン](search-engines.md)が設定されている。

### 拡張機能の基準

- ブラウザやOSに含まれる機能と重複しないこと。
- ユーザーのプライバシーに直接影響を与える必要があります。つまり、単に情報を提供するだけではない必要があります。

[^1]: Braveの実装は、[Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state/)で詳細に説明されています。
