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
    name: 推奨するプライベートブラウザー
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

[Tor Browser](tor.md)と同様に、Mullvad Browserは、あなたのブラウザーのフィンガープリントを他のすべてのMullvadユーザーと同一にすることで、フィンガープリンティングを防ぐよう設計されています。また、*Standard（標準）*、*Safer（より安全）*、*Safest（最も安全）*の3つのデフォルトのセキュリティレベルにより自動的に調整される設定と拡張機能が含まれています。 したがって、デフォルトの[セキュリティーレベル](https://tb-manual.torproject.org/security-settings/)を調整する以外の変更は、決して行うべきではありません。 その他の変更を加えた場合、あなたのブラウザーのフィンガープリントは一意のものとなり、このブラウザを使う意味が無くなってしまいます。 ブラウザーをより詳細に設定したい場合、また、フィンガープリンティングも問題ではない場合は、代わりに[Firefox](#firefox)を推奨します。

### フィンガープリント対策

**[VPN](vpn.md)**を使用しなくても、Mullvad Browserを使えば、Firefox+[Arkenfox](#arkenfox-advanced)や[Brave](#brave)などの他のプライベートブラウザーと同様、[初歩的なフィンガープリントスクリプト](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting)から身を守ることができます。 Mullvad Browserは、他のプライベートブラウザーに備わる柔軟性や利便性に代えて、デフォルトでこれらの保護機能を提供しています。

==最も強力なフィンガープリンティングの保護を求めるなら、Mullvadまたは他の推奨されるVPNプロバイダーと**併せて**、Mullvad Browserを使うことを推奨します==。 VPNをMullvad Browserと併用すると、他の多くのユーザーと同じフィンガープリントとIPアドレスを共有することになり、「群衆」の中に紛れ込むことができます。 これは高度なトラッキングスクリプトを阻止する唯一の方法であり、また、Tor Browserが使用しているのと同じフィンガープリンティング対策技術です。

なお、Mullvad BrowserはどのVPNプロバイダーとも併用することができますが、この「群衆」が存在するには、そのVPNを使用している他の人々もまた、Mullvad Browserを使用している必要があります。Mullvad BrowserのローンチとMullvad VPNが非常に近いことを考慮すると、これは他のVPNプロバイダーよりも、Mullvad VPNにおいて見られる可能性が高いです。 Mullvad Browserには、組み込みのVPN接続機能は備わっていません。また、ブラウザーを使用する前にVPNを使用しているかどうかを確認する機能もありません。VPN接続については、別途設定し、管理する必要があります。

Mullvad Browserには、*uBlock Origin*と*NoScript*の拡張機能が予めインストールされています。 私たちは通常、*追加の*拡張機能をインストールすることは[推奨していません](#extensions)。これらの予めインストールされている拡張機能を削除したり、デフォルトの設定を変更したりするべきでは**ありません**。あなたのブラウザーのフィンガープリントが他のMullvad Browserユーザーと異なるものになってしまいます。 また、予めインストールされているMullvad Browser Extensionは、ブラウザのフィンガープリントに影響を及ぼさずに安全に削除*できます*が、Mullvad VPNを使用しない場合でもインストールしたままにしておくのが安全です。

### プライベートブラウジングモード

Mullvad Browserは常にプライベートブラウジングモードで動作します。履歴、クッキー、その他サイトに関するデータは、ブラウザーを閉じるたびに消去されます。 ブックマーク、ブラウザーの設定、拡張機能の設定はそのまま残ります。

これは、高度な形式のトラッキングを防ぐために必要ですが、これによって利便性が減少したり、Firefoxの一部の機能（例えば、Multi-Account Containersなど）が使えなくなったりします。 常に複数のブラウザーを使用できることを覚えておいてください。たとえば、ログインしたままにしたいサイトや、Mullvad Browserでは正しく動作しないサイトについては Firefox + Arkenfox を使い、一般的なブラウジングには Mullvad Browserを使うといった方法が考えられます。

### Mullvad Leta

Mullvad Browserでは、デフォルトの[検索エンジン](search-engines.md)としてDuckDuckGoが設定されていますが、**Mullvad Leta**も予めインストールされています。この検索エンジンにアクセスするには、Mullvad VPNの有効なサブスクリプションが必要です。 Mullvad LetaはGoogleの有料検索APIに直接問い合わせるため、有料会員に限定されています。したがって、Mullvadは、検索クエリーとMullvad VPNアカウントを関連付けることができます。 MullvadはVPN加入者について非常に少ない情報しか収集していませんが、以上の理由より、Mullvad Letaの使用は推奨されません。

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
FirefoxはMozillaのウェブサイトからのダウンロードに一意の[ダウンロードトークン](https://bugzilla.mozilla.org/show_bug.cgi?id=1677497#c0)を含み、このトークンを送信するためにFirefox内のテレメトリーを使用します。 このトークンは、[Mozilla FTP](https://ftp.mozilla.org/pub/firefox/releases/)からのリリースには**含まれません**。

### 推奨する設定

これらのオプションは :material-menu: → **設定**にあります。

#### 検索

- [ ] **検索候補を使用する**のチェックを外す

お住まいの地域では検索提案機能が利用できない場合があります。

検索提案機能は、実際に検索を行うかどうかに関わらず、アドレスバーに入力したすべての文字をデフォルトの検索エンジンに送信します。 検索提案機能を無効にすることで、検索エンジンプロバイダーに送信するデータを、より正確に制御することができます。

#### プライバシーとセキュリティ

##### 強化型トラッキング防止機能

- [x] 強化型トラッキング防止機能で**厳格**を選択する

これにより、ソーシャルメディアのトラッカー、フィンガープリンティングスクリプト（*すべての*フィンガープリンティングから保護するわけではありません）、暗号通貨のマイニングプログラム、クロスサイトのトラッキングクッキー、その他の追跡コンテンツをブロックすることであなたを保護します。 ETPは多くの一般的な脅威に対抗しますが、サイトの利便性にほとんど影響を与えないように設計されているため、すべてのトラッキング手段をブロックするわけではありません。

##### Firefox Suggest (アメリカのみ)

[Firefox Suggest](https://support.mozilla.org/en-US/kb/firefox-suggest)は、米国のみで利用可能な、検索提案機能と似た機能です。 私たちは、検索提案機能の無効化を推奨するのと同じ理由で、これを無効にすることを推奨します。 **アドレスバー**のヘッダーの下に以下のオプションが表示されない場合、この機能は備わっていないので、これらの変更を無視しても問題ありません。

- [ ] **ウェブからの提案**のチェックを外すこと
- [ ] **スポンサーからの提案**のチェックを外すこと

##### 終了時のクリーンアップ

特定のサイトにログインしたままにしたい場合は、**Cookie とサイトデータ** → **例外の管理...**で例外を許可することができます。

- [x] **Firefox を閉じたときに Cookie とサイトデータを削除する**にチェックをつける

これにより、永続的なクッキーからは保護されますが、1回の閲覧セッション中に取得されたクッキーからは保護されません。 これを有効にすると、Firefoxを再起動するだけで、ブラウザのクッキーを簡単に削除できるようになります。 よく訪れる特定のサイトにログインしたままにしたい場合は、サイトごとに例外を設定することができます。

##### テレメトリー

- [ ] **Firefox が技術的な対話データを Mozilla へ送信することを許可する**のチェックを外す
- [ ] **Firefox に調査のインストールと実行を許可する**のチェックを外す
- [ ] **Firefox があなたに代わって未送信のクラッシュレポートを送信することを許可する**のチェックを外すこと

> Firefox は、Firefoxのバージョンと言語、デバイスのオペレーティングシステムとハードウェア構成、メモリー、クラッシュやエラーに関する基本情報、アップデート、セーフブラウジング、アクティベーションなどの自動処理の結果に関するデータを送信します。 Firefoxが私たちにデータを送信するとき、あなたのIPアドレスは一時的に私たちのサーバーログの一部として収集されます。

さらに、Firefoxアカウントサービスは [いくつかの技術データ](https://www.mozilla.org/en-US/privacy/firefox/#firefox-accounts)を収集します。 Firefoxアカウントを使用している場合は、オプトアウトすることができます。

1. [accounts.firefox.comのプロフィール設定](https://accounts.firefox.com/settings#data-collection)を開く
2. **データの収集と使用** > **Firefoxアカウントの改善を支援する**のチェックを外す

##### HTTPS-Only モード

- [x] **すべてのウィンドウで HTTPS-Only モードを有効にする**を選択する

これにより、意図せずにプレーンテキストのHTTPでウェブサイトに接続することを防ぎます。 現在ではHTTPSを使用していないサイトは珍しいため、日常的なブラウジングにほとんど影響を及ぼさないはずです。

##### DNS over HTTPS

If you use a [DNS over HTTPS provider](dns.md):

- [x] Select **Max Protection** and choose a suitable provider

Max Protection enforces the use of DNS over HTTPS, and a security warning will show if Firefox can’t connect to your secure DNS resolver, or if your secure DNS resolver says that records for the domain you are trying to access do not exist. This stops the network you're connected to from secretly downgrading your DNS security.

#### 同期

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy/)は、あなたのブラウジングデータ（履歴、ブックマークなど）をすべてのデバイスで利用可能にし、それをE2EE（End-to-End Encryption, 端末間暗号化）で保護します。

### Arkenfox（高度）

!!! ヒント "高度なフィンガープリンティング対策にはMullvad Browserを使用してください"

    [Mullvad Browser](#mullvad-browser)は、初期設定でArkenfoxと同じフィンガープリンティング対策を行っています。なお、この機能を利用するためにMullvadのVPNを使用する必要はありません。 VPNと組み合わせることで、Mullvad BrowserはArkenfoxにはできない仕方で、より高度な追跡スクリプトを阻止することができます。 Arkenfoxには、より柔軟性があり、ログインしたままである必要があるウェブサイトに対してサイトごとの例外を許可するという利点があります。

[Arkenfoxプロジェクト](https://github.com/arkenfox/user.js)は、Firefoxのための慎重に考えられたオプションのセットを提供しています。 もしArkenfoxを使用することを[決めた](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not)場合、[いくつかのオプション](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common])は主観的に厳格であり、また、一部のウェブサイトが正しく動作しなくなる可能性があります。これらのオプションは、ニーズに合わせて[簡単に変更できます](https://github.com/arkenfox/user.js/wiki/3.1-Overrides)。 プロジェクトの[ウィキ](https://github.com/arkenfox/user.js/wiki)に全て目を通すことを**強くお勧めします**。 なお、Arkenfoxは[コンテナ](https://support.mozilla.org/ja/kb/containers#w_for-advanced-users)のサポートも有効にしています。

Arkenfoxでは、canvasのランダム化やFirefoxの組み込みのフィンガープリント対策の設定に基づき、基本的または単純なトラッキングスクリプトを防ぐことを唯一の目的としています。 Arkenfoxは、Mullvad BrowserやTor Browserのように、高度なフィンガープリンティングトラッキング用のスクリプトを防止するための唯一の方法である、他の多くのArkenfoxユーザーとブラウザを混ぜ合わせることを目指してはいません。 常に複数のブラウザを使用できることを覚えておいてください。たとえば、ログインしたままにしたいサイトや、それとは別の仕方で信頼したいサイトについては Firefox + Arkenfox を使用し、一般的なブラウジングには Mullvad Browserを使用するといった方法を考えることができます。

## Brave

!!! recommendation

    ![Brave ロゴ](assets/img/browsers/brave.svg){ align=right }
    
    **Brave Browser**には、コンテンツブロッカーと[いくつかのプライバシー機能](https://brave.com/privacy-features/)が内蔵されており、その多くはデフォルトで有効になっています。
    
    BraveはChromiumウェブブラウザープロジェクトに基づいて構築されているため、使い慣れた使用感があるほか、ウェブサイトの互換性問題を最小限に抑えられます。
    
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

**macOS users:** The download for Brave Browser from their official website is a `.pkg` installer which requires admin privileges to run (and may run other unnecessary scripts on your machine). As an alternative, you can download the latest `Brave-Browser-universal.dmg` file from their [GitHub releases](https://github.com/brave/brave-browser/releases/latest) page, which provides a traditional "drag to Applications folder" install.

!!! 警告

    Brave adds a "[referral code](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)" to the file name in downloads from the Brave website, which is used to track which source the browser was downloaded from, for example `BRV002` in a download named `Brave-Browser-BRV002.pkg`. The installer will then ping Brave's server with the referral code at the end of the installation process. If you're concerned about this, you can rename the installer file before opening it.

### 推奨する設定

これらのオプションは :material-menu: → **設定**にあります。

#### 設定

##### シールド

Braveには、[シールド](https://support.brave.com/hc/en-us/articles/360022973471-What-is-Shields-)機能にフィンガープリンティングへの対策が備わっています。 訪問する全てのページにおいて、これらのオプションを[グローバル](https://support.brave.com/hc/en-us/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings-)に設定することをお勧めします。

シールドのオプションは、必要に応じてサイトごとにダウングレードできますが、デフォルトでは以下の設定をおすすめします。

<div class="annotate" markdown>

- [x] **言語設定に基づく、サイトのフィンガープリントを禁止**を選択
- [x] 「トラッカーと広告をブロック」で**積極的**を選択

    ??? warning "デフォルトのフィルターリストを使用すること"
        Braveでは、 `brave://adblock` ページ内で追加のコンテンツフィルターを選択することができます。 この機能は使わず、デフォルトのフィルターの一覧のままにしておくことをお勧めします。 追加のリストを使用すると、他のBraveユーザーから目立つようになり、また、Braveの脆弱性によってリストに悪意のあるルールが追加された場合、攻撃対象となる領域が増えるおそれがあります。

- [x] **接続をHTTPSにアップグレードする**で**厳格**を選択
- [x] （オプション）**スクリプトをブロックする**を選択 (1)
- [x] 「フィンガープリンティングをブロック」で**厳格、サイトの表示が崩れる可能性**を選択

</div>

1. このオプションでは、uBlock Originの高度な[ブロックモード](https://github.com/gorhill/uBlock/wiki/Blocking-mode)や[NoScript](https://noscript.net/)拡張機能と同様の機能が有効になります。

##### ソーシャルメディアのブロック

- [ ] すべてのソーシャルメディアコンポーネントのチェックを外すこと

##### プライバシーとセキュリティー

<div class="annotate" markdown>

- [x] [WebRTC IP処理ポリシー](https://support.brave.com/hc/en-us/articles/360017989132-How-do-I-change-my-Privacy-Settings-#webrtc) で**非プロキシUDPを無効にする**を選択
- [ ] **プッシュメッセージングにGoogleサービスを使用**のチェックを外す
- [ ] **プライバシーを保護したプロダクト分析 (P3A) を許可する**のチェックを外す
- [ ] **毎日の使用状況のpingをBraveに自動送信する**のチェックを外す
- [ ] **診断レポートを自動送信する**のチェックを外す
- [ ] **Tor搭載のプライベートウィンドウ** (1) のチェックを外す

    !!! tip "終了時のクリーンアップ"

        - [x] *Cookie と他のサイトデータ* メニューから**すべてのウィンドウを閉じるときに Cookie とサイトデータを削除する**を選択

        頻繁にアクセスする特定のサイトにログインしたままにしたい場合は、*動作のカスタマイズ*セクションでサイトごとに例外を設定できます。

</div>

1. BraveはTor Browserほどフィンガープリントに対して強く**なく**、BraveでTorを使う人はずっと少ないため目立ってしまうでしょう。 [強力な匿名性が必要](https://support.brave.com/hc/en-us/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity-)な場合には[Tor Browser](tor.md#tor-browser)を使用してください。

##### 拡張機能

使わない組み込み**拡張機能**は無効にしてください。

- [ ] **Hangouts**のチェックを外す
- [ ] **WebTorrent**のチェックを外す

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

[Brave Sync](https://support.brave.com/hc/en-us/articles/360059793111-Understanding-Brave-Sync)は、あなたのブラウジングデータ（履歴、ブックマークなど）をすべてのデバイスで利用可能にし、それをE2EE（End-to-End Encryption, 端末間暗号化）で保護します。アカウントは不要です。

#### Brave RewardsとWallet

**Brave Rewards**では、Brave内で特定のアクションを実行することで、Basic Attention Token（BAT）という暗号通貨を受け取ることができます。 It relies on a custodial account and KYC from a select number of providers. We do not recommend BAT as a [private cryptocurrency](cryptocurrency.md), nor do we recommend using a [custodial wallet](advanced/payments.md#other-coins-bitcoin-ethereum-etc), so we would discourage using this feature.

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

##### その他のリスト

These are some other [filter lists](https://github.com/gorhill/uBlock/wiki/Dashboard:-Filter-lists) that you may want to consider adding:

- [x] Check **Privacy** > **AdGuard URL Tracking Protection**
- Add [Actually Legitimate URL Shortener Tool](https://raw.githubusercontent.com/DandelionSprout/adfilt/master/LegitimateURLShortener.txt)

## 規準

**私たちは、推薦するどのプロジェクトとも提携していません。**客観的に推薦できるよう、[標準となる規準](about/criteria.md)に加えて、一連の明確な要件を定めています。 プロジェクトを利用する前に、このリストをよく理解し、ご自身で調査を行って、そのプロジェクトがあなたにとって適切な選択かどうかをご確認ください。

!!! example "この項目は最近作成されました"

    私たちは、サイトの各項目に関して、定義された規準の確立に取り組んでいます。この規準は変更される可能性があります。 規準について疑問がある場合は、[フォーラムで質問](https://discuss.privacyguides.net/latest)してください。また、ここに記載されていない場合でも、私たちがプロジェクトを推奨する際に、そうした事柄を考慮しなかったと仮定するのはお止めください。 プロジェクトを推奨する際に考慮され、議論される要素は多くあり、そのすべてを文書化する作業は現在進行中です。

### 最低要件

- オープンソースのソフトウェアであること。
- 自動更新に対応している。
- Receives engine updates in 0-1 days from upstream release.
- Linux、macOS、Windowsで利用できる。
- ブラウザをよりプライバシーを尊重したものにするための変更が、ユーザーエクスペリエンスを損なうものではないこと。
- デフォルトでサードパーティCookieをブロックしている。
- Supports [state partitioning](https://developer.mozilla.org/en-US/docs/Web/Privacy/State_Partitioning) to mitigate cross-site tracking.[^1]

### 満たされることが望ましい基準

満たされることが望ましい基準には、このカテゴリーの完璧なプロジェクトに私たちが望むものを示しています。 私たちが推薦するプロジェクトは、この機能の一部または全部を含んでいないかもしれませんが、もし含んでいれば、このページで他のプロジェクトよりも上位にランクされるかもしれません。

- コンテンツブロック機能を内蔵していること。
- Supports cookie compartmentalization (à la [Multi-Account Containers](https://support.mozilla.org/en-US/kb/containers)).
- Supports Progressive Web Apps.  
  PWAs enable you to install certain websites as if they were native apps on your computer. This can have advantages over installing Electron-based apps, because you benefit from your browser's regular security updates.
- ユーザーのプライバシーに影響を与えないアドオン機能（ブロートウェア）が含まれていないこと。
- テレメトリーをデフォルトでは収集しないこと。
- オープンソースの同期サーバー実装を提供していること。
- [プライベートな検索エンジン](search-engines.md)をデフォルトで設定していること。

### 拡張機能の基準

- ブラウザやOSに含まれる機能と重複しないこと。
- ユーザーのプライバシーに直接影響を与えるものであること。つまり、単に情報を提供するだけではないこと。

[^1]: Braveにおける実装は、[Brave Privacy Updates: Partitioning network-state for privacy](https://brave.com/privacy-updates/14-partitioning-network-state/)で詳細に説明されています。
