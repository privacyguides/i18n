---
meta_title: "プライバシーを尊重したPCとMac向けウェブブラウザ - Privacy Guides"
title: "デスクトップブラウザ"
icon: material/laptop
description: 標準的・非匿名のインターネットブラウジングにおいて推奨するデスクトップシステム向けプライバシー保護ブラウザ。
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

<small>以下の脅威から保護します：</small>

- [:material-account-cash: 監視資本主義](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

標準的・非匿名のインターネットブラウジングにおいて推奨する**デスクトップウェブブラウザ**は以下のものが挙げられます。 強力なプライバシー保護とフィンガープリント対策を重視する場合は[Mullvad Browser](#mullvad-browser)を、カジュアルなブラウジングやGoogle Chromeの良い代替品を探している場合は[Firefox](#firefox)を、Chromiumブラウザとの互換性が必要な場合は[Brave](#brave)をおすすめします。

匿名でインターネットを閲覧するには、[Tor](tor.md)を使用してください。 このページではいくつかの設定をおすすめしていますが、Tor Browser以外のブラウザは、何らかの方法で、*誰かしら*が、あなたを追跡できます。

## Mullvad Browser

<div class="admonition recommendation" markdown>

![Mullvad Browser logo](assets/img/browsers/mullvad_browser.svg){ align=right }

**Mullvad Browser**は[Tor Browser](tor.md#tor-browser)からTorネットワークの機能を削除したブラウザです。 [:material-eye-outline: 監視社会](basics/common-threats.md#mass-surveillance-programs){ .pg-blue }に対する鍵となるTor Browserのフィンガープリント対策技術をVPNの利用者に提供することを目的としています。 Tor Projectが開発し、[Mullvad](vpn.md#mullvad)が配布しています。MullvadのVPNを使用する必要は**ありません**。

[::octicons-home-16: ウェブページ](https://mullvad.net/en/browser){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://mullvad.net/en/help/tag/mullvad-browser){ .card-link title="Documentation" }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/mullvad-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>ダウンロード</summary>

- [:fontawesome-brands-windows: Windows](https://mullvad.net/en/download/browser/windows)
- [:simple-apple: macOS](https://mullvad.net/en/download/browser/macos)
- [:simple-linux: Linux](https://mullvad.net/en/download/browser/linux)

</details>

</div>

[Tor Browser](tor.md)と同様、Mullvad Browserは他の全てのMullvad Browserユーザーと同じフィンガープリントにすることでフィンガープリンティングを防ぐように設計されています。デフォルトのセキュリティレベル*既定の保護*、*強力な保護*と*最大限の保護*により自動的に設定されるデフォルトの設定と拡張機能が含まれています。

そのため、デフォルトの[セキュリティレベル](https://tb-manual.torproject.org/security-settings)を調整する以外の変更は、行うべきではありません。 セキュリティレベルを調整する際には、使い続ける前にブラウザを再起動**しなければなりません**。 再起動しなければ、[セキュリティ設定は完全に適用されない可能性があり](https://www.privacyguides.org/articles/2025/05/02/tor-security-slider-flaw/)、選択した設定よりもフィンガープリンティングやエクスプロイトのリスクが高くなります。

設定を調整する以外の変更をした場合、フィンガープリンティングは一意なものとなり、このブラウザを使う意味がなくなってしまいます。 ブラウザをより詳細に設定したい場合で、フィンガープリントが重要でない場合は、代わりに[Firefox](#firefox)を推奨します。

### フィンガープリント対策

**[VPN](vpn.md)**を使用しなくても、Mullvad Browserを使えば、Firefox+[Arkenfox](#arkenfox-advanced)や[Brave](#brave)などの他のプライベートブラウザと同様に、[初歩的なフィンガープリントスクリプト](https://github.com/arkenfox/user.js/wiki/3.3-Overrides-%5BTo-RFP-or-Not%5D#-fingerprinting)から身を守ることができます。 Mullvad Browserは、他のプライベートブラウザーに備わる柔軟性や利便性に代えて、デフォルトでこれらの保護機能を提供しています。

==最も強力なフィンガープリンティングの保護を求めるなら、Mullvadまたは他の推奨されるVPNプロバイダーと**併せて**、Mullvad Browserを使うことを推奨します==。 VPNをMullvad Browserと併用すると、他の多くのユーザーと同じフィンガープリントとIPアドレスを共有することになり、「群衆」の中に紛れ込むことができます。 これは高度なトラッキングスクリプトを阻止する唯一の方法であり、また、Tor Browserが使用しているのと同じフィンガープリンティング対策技術です。

なお、Mullvad BrowserはどのVPNプロバイダーとも併用することができますが、この「群衆」が存在するには、そのVPNを使用している他の人々もまた、Mullvad Browserを使用している必要があります。Mullvad BrowserのローンチとMullvad VPNが非常に近いことを考慮すると、これは他のVPNプロバイダーよりも、Mullvad VPNにおいて見られる可能性が高いです。 Mullvad Browserには、組み込みのVPN接続機能は備わっていません。また、ブラウザを使用する前にVPNを使用しているかどうかを確認する機能もありません。VPN接続については、別途設定し、管理する必要があります。

Mullvad Browserには、*uBlock Origin*と*NoScript*の拡張機能が予めインストールされています。 私たちは通常、*追加の*[拡張機能](browser-extensions.md)をインストールすることは推奨していません。あらかじめインストールされている拡張機能を削除したり、デフォルトの設定を変更したりするべきでは**ありません**。あなたのブラウザのフィンガープリントが他のMullvad Browserユーザーと異なるものになってしまいます。 また、予めインストールされているMullvad Browser Extensionは、ブラウザのフィンガープリントに影響を及ぼさずに安全に削除*できます*が、Mullvad VPNを使用しない場合でもインストールしたままにしておくのが安全です。

### プライベートブラウジングモード

Mullvad Browserは常にプライベートブラウジングモードで動作します。履歴、クッキー、その他サイトに関するデータは、ブラウザを閉じるたびに消去されます。 ブックマーク、ブラウザの設定、拡張機能の設定は引き続き保持されます。

これは、高度な形式のトラッキングを防ぐために必要ですが、これによって利便性が減少したり、Firefoxの一部の機能（例えば、Multi-Account Containersなど）が使えなくなったりします。 常に複数のブラウザを使用できることを覚えておいてください。たとえば、ログインしたままにしたいサイトや、Mullvad Browserでは正しく動作しないサイトについては Firefox + Arkenfox を使い、一般的なブラウジングには Mullvad Browserを使うといった方法が考えられます。

### Mullvad Leta

Mullvad Browserは [**Mullvad Leta**](https://leta.mullvad.net) が標準の検索エンジンになっています。Mullvad LetaはGoogleもしくはBrave（Mullvad Letaのウェブページから設定可能）で検索するプロキシの役割を果たします。

もしMullvad VPNのユーザーであるなら、Mullvad LetaのようなVPNプロバイダーが提供するサービスを利用することは一定程度のリスクが生じます。 Mullvadは（VPN経由で）利用している本当のIPアドレスと（Leta経由での）検索アクティビティに理論上はアクセスできてしまいます。これらは本来VPNが分離しようとしているものです。 MullvadはMullvad VPNの利用者やMullvad Letaの利用者からはほとんど情報を収集しませんが、そのようなリスクについて懸念があるならば、別の[検索エンジン](search-engines.md)の利用を検討すべきです。

## Firefox

<div class="admonition recommendation" markdown>

![Firefoxのロゴ](assets/img/browsers/firefox.svg){ align=right }

**Firefox**は、[強化型トラッキング防止](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop)などの強力なプライバシー設定を提供し、[様々な種類のトラッキング](https://support.mozilla.org/kb/enhanced-tracking-protection-firefox-desktop#w_what-enhanced-tracking-protection-blocks)をブロックするのに役立ちます。

[:octicons-home-16: ウェブページ](https://firefox.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mozilla.org/privacy/firefox){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.mozilla.org/products/firefox){ .card-link title="Documentation" }
[:octicons-code-16:](https://hg.mozilla.org/mozilla-central){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.mozilla.org){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>ダウンロード</summary>

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

以下のオプションは :material-menu: → **設定**から変更できます。

#### 検索

- [ ] **検索候補を表示する**からチェックを外す

「検索候補を表示する」機能はお住まいの地域によって利用できない場合があります。

「検索候補を表示する」機能は検索をしなくても、アドレスバーに入力した文字をすべてデフォルトの検索エンジンに送信します。 「検索候補を表示する」機能を無効化することで検索エンジンに送る情報をより厳密に決めることができます。

##### Firefox Suggest (アメリカのみ)

[Firefox Suggest](https://support.mozilla.org/kb/firefox-suggest)は「検索候補を表示する」と同様の機能を提供します（アメリカのみで利用可能）。 同じ理由でFirefox suggestも無効化することを推奨します。 **アドレスバー**のヘッダーに以下のオプションが表示されない場合、この機能は提供されていないので、設定を変更する必要はありません。

- [ ] **「Firefoxからの提案」**からチェックを外す
- [ ] **スポンサーからの提案**のチェックを外すこと

#### プライバシーとセキュリティ

##### 強化型トラッキング防止機能

- [x] 強化型トラッキング防止機能で**厳格**を選択する

この機能はソーシャルメディアトラッカー、フィンガープリンティングスクリプト（*すべての*フィンガープリンティングから保護されるわけではありません）、暗号通貨マイニング、クロスサイトのトラッキングクッキーやその他トラッキングコンテンツをブロッキングし、あなたを保護します。 強化型トラッキング防止機能は一般的な多くの脅威に対応しますが、ウェブサイトのユーザビリティに与える影響を最小限に抑えるため、すべてのトラッキングをブロックするわけではありません。

##### 終了時のクリーンアップ

特定のサイトのログインを維持したい場合、**Cookieとサイトデータ** →**例外を管理…**から例外を許可することができます

- [x] **Firefox を閉じたときに Cookie とサイトデータを削除する**にチェックをつける

この機能により永続的なクッキーからは保護されますが、1回のブラウジングセッション中に取得されたクッキーからは保護されません。 有効化することでFirefoxを再起動するだけでブラウザのクッキーを簡単に削除できるようになります。 よく見る特定のサイトのログインを維持したい場合、サイトごとに例外を設定することができます。

##### テレメトリー

- [ ] **Firefox が技術的な対話データを Mozilla へ送信することを許可する**のチェックを外す
- [ ] **Firefox に調査のインストールと実行を許可する**のチェックを外す
- [ ] **Firefox があなたに代わって未送信のクラッシュレポートを送信することを許可する**のチェックを外すこと

MozillaのFirefoxプライバシーポリシーでは以下のように記載されています

> Firefox は、Firefoxのバージョンと言語、デバイスのオペレーティングシステムとハードウェア構成、メモリー、クラッシュやエラーに関する基本情報、アップデート、セーフブラウジング、アクティベーションなどの自動処理の結果に関するデータを送信します。 Firefoxが私たちにデータを送信するとき、あなたのIPアドレスは一時的に私たちのサーバーログの一部として収集されます。

さらに、Mozillaアカウントサービスは[技術的なデータ](https://mozilla.org/privacy/mozilla-accounts)を収集します。 もし、Mozillaアカウントを利用している場合、以下のものをオプトアウトすることができます：

1. [accounts.firefox.comのプロフィール設定](https://accounts.firefox.com/settings#data-collection)を開く
2. **データの収集と使用** > **Firefoxアカウントの改善を支援する**のチェックを外す

##### ウェブサイトの広告設定

- [ ] **プライバシー保護された広告解析をウェブサイトに許可する**のチェックを外す

Firefox 128から、[プライバシー保護されたアトリビューション](https://support.mozilla.org/kb/privacy-preserving-attribution)（PPA）の新たな設定が追加され、[デフォルトで有効](https://blog.privacyguides.org/2024/07/14/mozilla-disappoints-us-yet-again-2)になりました。 従来のJavaScriptベースのトラッキングの代わりにPPAにより、広告主がウェブブラウザを通じてウェブキャンペーンの効果測定ができるようになります。 ユーザーが利用するブラウザの責任の範囲外であると考えていますが、Arkenfoxではデフォルトで無効化されていることは、この機能を無効化する指針になり得ます。

##### HTTPS-Only モード

- [x] **すべてのウィンドウで HTTPS-Only モードを有効にする**を選択する

この機能により、意図せずプレーンテキストのHTTPでウェブサイトに接続することを防ぎます。 現在ではHTTPSを使用していないサイトはほとんどないため、通常のブラウジングにおいて影響が出ることはあまりありません。

##### DNS over HTTPS

[DNS over HTTPSプロバイダー](dns.md)を使用している場合：

- [x] **最大限の保護**にチェックを入れ、適切なプロバイダーを選択する

最大限の保護を設定することで、DNS over HTTPSが常に使用されます。Firefoxが安全なDNSリゾルバに接続できない場合や、安全なDNSリゾルバがアクセスしようとしたドメインのレコードが存在しない場合、セキュリティ警告が表示されます。 接続しているネットワークによって、DNSのセキュリティが秘密裏にダウングレードされることを防ぎます。

#### 同期

[Firefox Sync](https://hacks.mozilla.org/2018/11/firefox-sync-privacy)により、ブラウザのデータ（履歴、ブックマークなど）をE2EE（エンドツーエンド暗号化）で保護した上で、すべてのデバイスでアクセス可能となります。

### Arkenfox（高度）

<div class="admonition tip" markdown>
<p class="admonition-title">高度なフィンガープリンティング対策にはMullvad Browserを使用してください</p>

[Mullvad Browser](#mullvad-browser) は、初期設定でArkenfoxと同じフィンガープリンティング対策を行っています。なお、この機能を利用するためにMullvadのVPNを使用する必要はありません。 VPNと組み合わせることで、Mullvad BrowserはArkenfoxにはできない仕方で、より高度な追跡スクリプトを阻止することができます。 Arkenfoxには、より柔軟性があり、ログインしたままである必要があるウェブサイトに対してサイトごとの例外を許可するという利点があります。

</div>

[Arkenfox project](https://github.com/arkenfox/user.js)はFirefoxの注意深く考えられた設定を提供しています。 もし、Arkenfoxを利用[する](https://github.com/arkenfox/user.js/wiki/1.1-To-Arkenfox-or-Not)場合、[いくつかの設定](https://github.com/arkenfox/user.js/wiki/3.2-Overrides-[Common])はあえて厳しくしているためウェブサイトが正常に表示されないことがあります。必要に応じ[簡単に変更](https://github.com/arkenfox/user.js/wiki/3.1-Overrides)できます。 プロジェクトの[wiki](https://github.com/arkenfox/user.js/wiki)をすべて読むことを**強く推奨**します。 Arkenfoxは[コンテナー](https://support.mozilla.org/kb/containers#w_for-advanced-users)をサポートしています。

Arkenfoxはcanvasのランダム化やFirefoxの標準で利用できるフィンガープリント対策で基本的・単純なトラッキングスクリプトを防ぐことのみを目的としています。 Mulllvad BrowserやTor BrowserのようにArkenfoxユーザーを一つの集団として扱うこと（高度なフィンガープリントトラッキングスクリプトを防ぐ唯一の方法）は目的としていません。 いつも複数のブラウザを利用できることを覚えておいてください。例えば、ログインを維持したい、もしくは信用できるウェブサイトはFirefoxとArkenfoxを利用し、通常のブラウジングではMullvad Browserを利用することもできます。

## Brave

<div class="admonition recommendation annotate" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

**Brave ブラウザ** にはコンテンツブロッカーと[プライバシー機能](https://brave.com/privacy-features)が組み込まれており、その多くはデフォルトで有効になっています。

BraveはChromiumウェブブラウザプロジェクトに基づいて構築されているため、使い慣れた使用感があるほか、ウェブサイトの互換性問題が最小限に抑えられます。

[:octicons-home-16: ウェブページ](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.brave.com){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>ダウンロード</summary>

- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:fontawesome-brands-windows: Windows](https://brave.com/download)
- [:simple-apple: macOS](https://brave.com/download)
- [:simple-linux: Linux](https://brave.com/linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/com.brave.Browser)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">注意</p>

どのブラウザからダウンロードされたか追跡するため、Braveのウェブサイトからダウンロードした際に「[リファラルコード](https://github.com/brave/brave-browser/wiki/Brave%E2%80%99s-Use-of-Referral-Codes)」がファイル名に追加されます。例えば「BRV002」をダウンロードした際のファイル名は「Brave-Browser-BRV002.pkg」となります。 インストーラーはインストールの終わりにBraveのサーバーにリファラルコードを送信します。 これが心配な場合は、インストーラファイルを開く前に名前を変更できます。

</div>

### 推奨するBraveの設定

以下のオプションは :material-menu: → **設定**から変更できます。

#### シールド

Braveの[シールド](https://support.brave.com/hc/articles/360022973471-What-is-Shields)にはアンチフィンガープリンティングの機能があります。 以下のオプションはアクセスするすべてのページを対象にするため、[グローバル](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings)に設定することを推奨します。

シールドのオプションは、必要に応じてサイトごとにダウングレードできますが、デフォルトでは以下の設定をおすすめします。

<div class="annotate" markdown>

- [x] *トラッカーと広告をブロック*の**積極的**を選択

<details class="warning" markdown>
<summary>デフォルトのフィルターリストの使用について</summary>

`brave://adblock` ページで追加のコンテンツフィルターを選択することができます。 この機能は使わず、デフォルトのフィルターの一覧のままにしておくことをお勧めします。 追加のリストを使用すると、他のBraveユーザーから目立つようになり、また、Braveの脆弱性によってリストに悪意のあるルールが追加された場合、攻撃対象となる領域が増えるおそれがあります。

</details>

- [x] *接続をHTTPSにアップグレードする*の**厳格**を選択
- [x] (オプション) **スクリプトをブロックする**を選択 (1)
- [x] **フィンガープリンティングをブロック**を選択
- [x] **3rdパーティクッキーをブロック**を選択
- [x] **このサイトを閉じる際にデータを削除**を選択 (2)
- [ ] ソーシャルメディアのブロックのすべてのチェックを外す

</div>

1. JavaScriptが無効となり、多くのサイトが正しく表示されなくなります。 修正するには、アドレスバーのシールドアイコンをクリックし、*高度なコントロール*からこの設定のチェックを外し、サイトごとに例外を設定します。
2. よく見る特定のサイトでログインを維持したいのであれば、アドレスバーのシールドアイコンをクリックし、*高度なコントロール*からこの設定のチェックを外し、サイトごとに例外を設定します。

#### プライバシーとセキュリティ

<div class="annotate" markdown>

- [x] *セキュリティ* → *V8のセキュリティを管理する*から**サイトでのV8オプティマイザーの使用を許可しない**を選択 (1)
- [x] *サイトとシールドの設定*から**使用していないサイトから権限を自動的に削除する**を選択
- [x] [*WebRTC IP処理ポリシー*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)の**非プロキシUDPを無効にする**を選択
- [ ] **プッシュメッセージングにGoogleサービスを使用**のチェックを外す
- [x] **AMPページを自動でリダイレクト**を選択
- [x] **自動リダイレクト追跡URL**を選択
- [x] **言語設定に基づく、サイトのフィンガープリンティングを禁止**を選択

</div>

1. V8オプティマイザーを無効にすることでJavaScriptの実行時(JIT)コンパイルの[*一部*](https://grapheneos.social/@GrapheneOS/112708049232710156)を無効化し、アタックサーフェスを減らすことができます。

##### Torウィンドウ

[**Tor搭載のプライベートウィンドウ**](https://support.brave.com/hc/articles/360018121491-What-is-a-Private-Window-with-Tor-Connectivity)を使うことで、プライベートウィンドウの通信はTorネットワークを経由し、.onionにアクセスでき、場合によっては役立つこともあります。 ただし、BraveはTor Browserよりもフィンガープリンティングに対して強く**ない**ことに加え、BraveでTorを使う人は非常に少ないため目立ってしまいます。 脅威モデルにより強い匿名性が必要な場合、[Tor Browser](tor.md#tor-browser)を使用します。

##### データ コレクション

- [ ] **プライバシーを保護したプロダクト分析(P3A)を許可する**のチェックを外す
- [ ] **毎日の使用状況のpingをBraveに自動送信する**のチェックを外す
- [ ] **診断レポートを自動送信する**のチェックを外す

#### Web3

BraveのWeb3機能はブラウザのフィンガープリントとアタックサーフェスを潜在的に増やす可能性があります。 これらの機能を使わないのであれば、無効化すべきです。

- *デフォルトのEthereumウォレット*の**拡張機能（フォールバックなし）**を選択
- *デフォルトのSolanaウォレット*の**拡張機能（フォールバックなし）**を選択

#### 拡張機能

- [ ] 使用していないビルトインの拡張機能のチェックをすべて外す

#### 検索エンジン

[Firefox](#search)で同様の機能を無効にしたのと同じ理由で「検索候補を表示」を無効にすることを推奨します。

- [ ] **検索候補を表示する**からチェックを外す

#### システム

<div class="annotate" markdown>

- [ ] **Braveを閉じた際にバックグラウンドアプリの処理を続行する**のチェックを外し、バックグラウンドアプリを無効にする (1)

</div>

1. このオプションはすべてのプラットフォームにあるわけではありません。

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync)により、ブラウジングデータ（履歴、ブックマークなど）をすべてのデバイスで利用可能にします。アカウントは不要でE2EE（エンドツーエンド暗号化）で保護されます。

#### Brave Rewardsとウォレット

**Brave Rewards**ではBraveで特定の行動を実行することにより、ベーシックアテンショントークン(BAT)という暗号通貨を得ることができます。 プロバイダーによるカストディアルアカウントと本人確認が必要となります。 BATを[プライベートな暗号通貨](cryptocurrency.md)として推奨はせず、[カストディアルウォレット](advanced/payments.md#wallet-custody)の使用も推奨しないため、この機能の使用は推奨しません。

**Brave ウォレット**はコンピューターのローカルで動作しますが、プライベートな暗号通貨をサポートしないため、この機能も推奨しません。

## 規準

**私たちは、推薦するどのプロジェクトとも提携していません。**客観的に推薦できるよう、[標準となる規準](about/criteria.md)に加えて、一連の明確な要件を定めています。 プロジェクトを利用する前に、このリストをよく理解し、ご自身で調査を行って、そのプロジェクトがあなたにとって適切な選択かどうかをご確認ください。

### 最低要件

- オープンソースのソフトウェアであること。
- 自動アップデートに対応していること。
- アップストリームのリリースから0～1日以内にエンジンのアップデートがあること。
- Linux、macOS、Windowsで利用可能であること。
- ブラウザをよりプライバシー重視にするための変更が、ユーザーエクスペリエンスを損なうものではないこと。
- デフォルトでサードパーティクッキーをブロックしていること。
- クロスサイトトラッキングを軽減する[state partitioning](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning)をサポートしていること。[^1]

### 満たされることが望ましい基準

満たされることが望ましい基準には、このカテゴリーの完璧なプロジェクトに私たちが望むものを示しています。 私たちが推薦するプロジェクトは、この機能の一部または全部を含んでいないかもしれませんが、もし含んでいれば、このページで他のプロジェクトよりも上位にランクされるかもしれません。

- ビルトインのコンテンツブロック機能があること。
- クッキーの区画化（[Multi-Account Containers](https://support.mozilla.org/kb/containers)）をサポートすること。
- プログレッシブウェブアプリ（PWA）をサポートすること。 PWAにより、ウェブサイトをネイティブアプリのようにコンピューターにインストールすることができます。 PWAはブラウザの定期的なセキュリティアップデートでアップデートされるため、Electronベースのアプリケーションをインストールするよりもメリットがあります。
- ユーザーのプライバシー保護に寄与しないアドオン（ブロートウェア）が含まれないこと。
- テレメトリーをデフォルトでは収集しないこと。
- オープンソースの同期サーバー実装を提供していること。
- [プライベートな検索エンジン](search-engines.md)をデフォルトで設定していること。

[^1]: Braveの実装は[Brave プライバシーアップデートで詳しく説明されています: プライバシーのためのネットワーク状態のパーティショニング](https://brave.com/privacy-updates/14-partitioning-network-state)
