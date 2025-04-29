---
title: "一般的な脅威"
icon: 'material/eye-outline'
description: 脅威モデルは個々人によりますが、このサイトの閲覧者が気にしていることが含まれます。
---

一般的にいえば、推奨するものは多くの人に当てはまる[脅威](threat-modeling.md)や目標に分類することができます。 ==この可能性のうち、どれも心配していないかもしれませんし、一つ、２つ以上、もしくは全てに関心があるかもしれませんが、==使うツールやサービスは目標によります。 このカテゴリ以外の脅威に関心があるかもしれませんが、問題ありません！ 重要なのは、選んだツールの利点と欠点を理解することです。なぜならすべての脅威から保護するようなものは実際ないからです。

<span class="pg-purple">:material-incognito:**匿名性**</span>
:

オンライン上の活動を実際の身元から保護し、*あなたの*身元を特定しようとする人から守ります。

<span class="pg-red">:material-target-account:**標的型攻撃**</span>
:

*あなたの*データやデバイスを対象にアクセスしようとするハッカーや悪意のある者から守ります。

<span class="pg-viridian">:material-package-variant-closed-remove:**サプライチェーン攻撃**</span>
:

典型的な<span class="pg-red">:material-target-account:標的型攻撃</span>の一つで、正常なソフトウェアに直接もしくはサードパーティの依存関係の脆弱性やエクスプトイトを伝って行われる攻撃です。

<span class="pg-orange">:material-bug-outline:**パッシブ攻撃**</span>
:

マルウェア、データ漏洩など一度に多数の人を対象に行われる攻撃から守ります。

<span class="pg-teal">:material-server-network:**サービスプロバイダー**</span>
:

サービスの提供者からデータを守ります（例えば、エンドツーエンド暗号化によって、サーバーでデータを読み取ることができなくなります）。

<span class="pg-blue">:material-eye-outline:**監視社会**</span>
:

政府の機関・組織・ウェブサイトや活動を追跡することに協力するサービスから守ります。

<span class="pg-brown">:material-account-cash:**監視資本主義**</span>
:

GoogleやFacebookのような巨大な広告ネットワークやその他多数のサードパーティのデータ収集者から守ります。

<span class="pg-green">:material-account-search:**秘密の暴露**</span>
:

検索エンジンに対し、もしくは一般公開されている、オンライン上の情報へのアクセスに制限します。

<span class="pg-blue-gray">:material-close-outline:**検閲**</span>
:

オンライン上で発言する際、情報や自身に対する検閲を避けます。

懸念によりますが、脅威の中には他よりも重要だと思うものがあるかもしれません。 例えば、貴重なもしくは重要なデータにアクセスできるソフトウェア開発者は主に<span class="pg-viridian">:material-package-variant-closed-remove:サプライチェーン攻撃</span>や<span class="pg-red">:material-target-account:標的型攻撃</span>に関心を持つかもしれません。 また、<span class="pg-blue">:material-eye-outline:監視社会</span>のプログラムに巻き込まれないよう個人のデータを守りたいと思うでしょう。 同様に、多くの人は主に個人データの<span class="pg-green">:material-account-search:秘密の暴露</span>は気にしているかもしれませんが、デバイスがマルウェアに感染するなどの<span class="pg-orange">:material-bug-outline:パッシブ攻撃</span>のようなセキュリティの問題にも注意を向ける必要があります。

## 匿名性とプライバシーの比較

<span class="pg-purple">:material-incognito: 匿名性</span>

匿名性はしばしばプライバシーと混同されますが、それらは異なる概念です。 プライバシーは個人のデータがどのように使われ、共有されるかを選択するのに対し、匿名性は実際の身元とオンライン上での活動を完全に切り離すことです。

例えば、内部告発者やジャーナリストの脅威モデルは完全な匿名性が必要となる極端なものになるでしょう。 何をしているか、どんなデータを持っているかを隠し、悪意ある者や政府からハッキングされていないことだけではなく、誰であるかを完全に隠すことです。 命がかかっているため、匿名性、プライバシー、セキュリティを守るためであればどんな利便性も犠牲にするでしょう。 ほとんどの人はそこまでする必要はありません。

## セキュリティーとプライバシー

<span class="pg-orange">:material-bug-outline: パッシブ攻撃</span>

セキュリティとプライバシーはよく混同されます。プライバシーを確保するにはセキュリティが必要です：たとえ設計上はプライバシーが確保されているツールを使っていても、個人のデータを公開しようとする攻撃者が簡単に攻撃できるのであれば、意味がありません。 ただし、この逆は必ずしも正しいわけではありません：世界で最もセキュアなサービスはプライバシーがある*とは限りません*。 最もよい例はGoogleにデータを託すことです。インフラを保護するために業界トップのセキュリティ専門家を雇っており、Googleの規模を考えれば、セキュリティインシデントはほとんど起きていません。 Googleのサービスは非常に安全ではありますが、Googleの一般消費者向けの無料サービス（Gmail, YouTubeなど）で自分のデータのプライバシーがあると考える人はほとんどいないでしょう。

アプリケーションのセキュリティに関して、通常はそのソフトウェアが悪意のあるものか、あるいは悪意のあるものになるかは分かりません（知ることすらできないこともあります）。 たとえ信頼のできる開発者が関わっていたとしても、重大な脆弱性がなく、悪用されないという保証はありません。

悪意のあるソフトウェアの影響を最小限に抑え*うる*ためには、区画化によるセキュリティを採用することです。 例えば、ジョブごとにコンピューターを使い分けたり、関連するアプリケーションのグループごとに仮想マシンを分けたり、アプリケーションのサンドボックスや強制的なアクセス制御を重視したセキュアなOSを使ったりすることが挙げられます。

<div class="admonition tip" markdown>
<p class="admonition-title">ヒント</p>

一般的にモバイルOSはデスクトップOSよりもアプリケーションサンドボックス機能が優れています：アプリケーションはルートアクセスを取得できず、システムリソースへのアクセスは許可が必要です。

デスクトップOSは適切なサンドボックス化では遅れています。 ChromeOSにはAndroidと同じようなサンドボックス機能があり、macOSには完全なシステムの権限制御があります（開発者はアプリケーションのサンドボックス化を選ぶことができます）。 ただし、識別情報をOEM元に送信します。 Linuxはシステムベンダーに情報を送らないことが多いですが、エクスプロイトや悪意のあるアプリからの保護は不十分です。 [QubesOS](../desktop.md#qubes-os)のような仮想マシンやコンテナを多用する特別なディストリビューションを使えば影響は軽減されます。

</div>

## 特定の個人に対する攻撃

<span class="pg-red">:material-target-account:標的型攻撃</span>

特定の個人に対する標的型攻撃は、より対処が難しくなります。 一般的な攻撃として、メールに悪意のある文書を添付して送ることや（ブラウザやOSなどの）脆弱性の悪用、物理的な攻撃があります。 もし、懸念がある場合はより高度に脅威を緩和する戦略を取る必要があります。

<div class="admonition tip" markdown>
<p class="admonition-title">ヒント</p>

**ウェブブラウザ**、**メールクライアント**や**オフィスアプリケーション**は第三者から送られてきた信頼できないコードを実行します。 ホストのシステムからアプリケーションを分離するため、複数の仮想マシンを実行することはアプリケーションからシステムの他の部分への侵害の可能性を軽減するための方法の一つです。 例えば、Qubes OSやWindowsのMicrosoft Defender Application Guardのような技術により、実現できます。

</div>

**物理的攻撃**を懸念する場合、Android、iOS、macOSや[Windows(TPMあり)](https://learn.microsoft.com/windows/security/information-protection/secure-the-windows-10-boot-process)のような安全な検証済みブート実装のあるOSを使うべきです。 またドライブの暗号化を行うとともに、OSがTPMやSecure[Enclave](https://support.apple.com/guide/security/secure-enclave-sec59b0b31ff/1/web/1)や[Element](https://developers.google.com/android/security/android-ready-se)で暗号化パスフレーズの入力レートを制限していることも確認してください。 ほとんどのデスクトップOSはユーザーごとに分けて暗号化することはできないため、信頼できない人とコンピューターを共用することは避けてください。

## 特定の組織に対する攻撃

<span class="pg-viridian">:material-package-variant-closed-remove:サプライチェーン攻撃</span>

サプライチェーン攻撃は企業、政府や活動家に対する<span class="pg-red">:material-target-account:標的型攻撃</span>であることが多いですが、一般市民を対象に侵害することもあります。

<div class="admonition example" markdown>
<p class="admonition-title">例</p>

注目すべき例は、2017年、ウクライナで普及している会計ソフトであるM.E.Docが*NotPetya*ウイルスに感染し、それをダウンロードした人がランサムウェアに感染したことが挙げられます。 NotPetya自体は2000以上もの様々な国の企業に影響を与えたランサムウェア攻撃であり、NSAの開発した、ネットワーク経由でWindowsコンピューターを攻撃する*EternalBlue*エクスプロイトに基づいていました。

</div>

いくつかの攻撃方法があります：

1. 貢献者や従業員になり、最初はプロジェクトや組織で重要な地位に付くために働き、その地位を悪用して悪意のあるコードを追加する。
2. 開発者が外部の組織から悪意のあるコードを追加するよう強制される。
3. 個人もしくは団体が、サードパーティのソフトウェアへの依存関係（ライブラリとも言われる）を特定し、「ダウンストリーム」のソフトウェア開発者に使われることを想定し、上記の2つの方法によりそのソフトウェアに侵入する。

この方法は多くの時間と準備を必要とし、特にオープンソースプロジェクトで人気がある、あるいは外部の関心が高い場合、検知される可能性があります。 残念ながら完全に軽減することは難しく、最も危険性が高い攻撃方法の一つです。 評判が良く、リスクを減らそうとしているソフトウェアのみ使用することを推奨します：

1. しばらく前からある人気のあるソフトウェアだけを使う。 プロジェクトに対する関心が高いほど、悪意のある変更に対し外部から気づく可能性は高くなります。 また、悪意のある者はコミュニティからの信頼を得るため、さらに長い時間をかけて意義のある貢献をする必要があります。
2. 開発者のワークステーションやセルフホストのサーバーではなく、広く使われている信頼できるビルドインフラストラクチャープラットフォームでリリースされているバイナリを見つける。 GitHub Actionsのようなシステムでは信頼性を高めるために公開された実行されているビルドスクリプトを検証することができます。 開発者のマシンにあるパッケージがマルウェアに感染している可能性を減らし、バイナリが実際に正しく生成されている保証が得られます。
3. ソースコードの個別のコミットやリリースの署名を見て、誰が何をしたか監査可能な証跡を作成します。 例えば、ソフトウェアリポジトリに悪意のあるコードがあるか？ どの開発者が追加したか？ どのビルドプロセスで追加されたのか？
4. ソースコードに各変更が何をしようとしているか説明をしている （[conventional commits](https://conventionalcommits.org)のような）意味が分かるコミットメッセージがあるか確認する。 明確なメッセージにより、プロジェクトの部外者から検証、監査、バグの発見が容易になります。
5. プログラムのコントリビューターやメンテナーの人数に注意する。 単独の開発者の場合、外部から悪意のあるコードを追加するよう強制されたり、不注意で望ましくない動作ができてしまったりする可能性が高くなります。 「ビッグテック」が開発しているソフトウェアは、誰の質問に答えない単独の開発者よりも精査されることを意味します。

## サービスプロバイダーからのプライバシー保護

<span class="pg-teal">:material-server-network:サービスプロバイダー</span>

ほとんどすべてのものがインターネットに接続されています。 「プライベート」なメッセージ、メール、ソーシャルネットワークでのやり取りは通常、どこかのサーバーに保存されています。 一般的には、メッセージを送った際には、サーバーにメッセージが保存され、友人があなたからのメッセージを読みたいと思ったときにサーバーが表示します。

明らかな問題点はサービスプロバイダー（もしくはサーバーに侵入したハッカー）はあなたの知らないうちに、いつでも好きなように会話にアクセスできるということです。 SMSメッセージ、TelegramやDiscordといった一般的な多くのサービスに当てはまります。

幸いにも、エンドツーエンド暗号化により、サーバーに送信する前にあなたと受信者との会話を暗号化することでこの問題を軽減することができます。 サービスプロバイダーが両者の秘密鍵にアクセスできなければメッセージの機密性は保証されます。

<div class="admonition note" markdown>
<p class="admonition-title">ウェブベースの暗号化に関する注意</p>

実際には、エンドツーエンド暗号化の実装の有効性は様々です。 [Signal](../real-time-communication.md#signal)のようなアプリケーションはデバイス上でネイティブに実行され、コピーされたアプリケーションはどのインストールでも同じになります。 もし、サービスプロバイダーが秘密鍵を盗むために[バックドア](https://en.wikipedia.org/wiki/Backdoor_(computing))をアプリケーションに仕込んだとしても、[リバースエンジニアリング](https://en.wikipedia.org/wiki/Reverse_engineering)によって検知できます。

一方、Proton MailのウェブアプリやBitwardenの*Web Vault*のようなウェブベースのエンドツーエンド暗号化実装は、サーバーが動的に送る暗号化を処理するJavaScriptコードに依存しています。 悪意のあるサーバーがあなたを標的にし、暗号鍵を盗むために悪意のあるJavaScriptコードを送ることもできます（そして、気づくことは非常に難しいでしょう）。 たとえ攻撃に気づいたとしても、サーバーはそれぞれに異なるウェブクライアントを送ることができるため、プロバイダーの過失を証明することは非常に難しいでしょう。

そのため、可能な限りウェブクライアントよりもネイティブアプリケーションを使うべきです。

</div>

エンドツーエンド暗号化でも、サービスプロバイダーは通常、保護されていない**メタデータ**に基づいてプロファイリングできます。 サービスプロバイダーはメッセージを読むことができなくとも、誰と会話しているか、メッセージをどのぐらいやり取りしているか、普段はいつやり取りしているか、といった重要なことを知ることができます。 メタデータを保護することはあまり行われていません。もし[脅威モデル](threat-modeling.md)にあるならば、使っているソフトウェアのドキュメントを読み、メタデータを最小化することができるか、もしくは保護がまったくできないか、注意を払う必要があります。

## 大量監視プログラム

<span class="pg-blue">:material-eye-outline: 監視社会</span>

監視社会は集団全体（あるいは相当部分）の「振る舞い、活動、情報」を監視するための複雑な取り組みのことです。[^1] [2013年にエドワード・スノーデンが暴露した](https://en.wikipedia.org/wiki/Global_surveillance_disclosures_(2013%E2%80%93present))ような政府のプログラムを指すことが多いです。 ただし、企業が政府機関に代わり、もしくは自主的に実施することもあります。

<div class="admonition abstract" markdown>
<p class="admonition-title">Atlas of Surveillance</p>

監視方法や街でどのように実施されているかを知りたい場合、[電子フロンティア財団](https://eff.org)の[Atlas of Surveillance](https://atlasofsurveillance.org)を見てください。

フランスでは、非営利団体La Quadrature du Netが管理する[Technopolice website](https://technopolice.fr/villes) を見ることができます。

</div>

政府は監視社会プログラムをテロとの闘いや犯罪防止の目的で、正当化することが多いです。 ただし、マイノリティグループや政治的反体制派などを不当に標的とした人権侵害に使われることも多いのです。

<div class="admonition quote" markdown>
<p class="admonition-title">ACLU: <em><a href="https://aclu.org/news/national-security/the-privacy-lesson-of-9-11-mass-surveillance-is-not-the-way-forward">The Privacy Lesson of 9/11: Mass Surveillance is Not the Way Forward</a></em></p>

エドワード・スノーデンが[PRISM](https://en.wikipedia.org/wiki/PRISM)や[Upstream](https://en.wikipedia.org/wiki/Upstream_collection)といった政府のプログラムを暴露したことで、NSAが密かに何年もの間、事実上すべてのアメリカ人の通話記録（誰が誰にかけたか、いつどのぐらい通話していたか）を収集していたことを情報当局は認めました。 このような情報が日々蓄積されると、牧師、中絶を行う医師、中毒のカウンセラーや自殺ホットラインに電話したことがあるかなど、生活や交友関係の信じられないほどセンシティブな情報の詳細を明らかにすることができます。

</div>

アメリカでは監視社会が強化されているにも関わらず、第215条のような監視社会プログラムは実際の犯罪やテロ計画を阻止することに「ほとんど独自の価値がない」とされ、FBIの標的型監視プログラムと大部分が重複しているとされています。[^2]

オンライン上では、様々な方法で追跡することができます。以下は一例です：

- あなたのIPアドレス
- ブラウザーのクッキー
- ウェブサイトに送信するデータ
- ブラウザやデバイスのフィンガープリント
- 支払い方法の相関関係

監視社会プログラムに懸念がある場合、オンライン上のIDを区画化したり、他のユーザーに紛れ込んだり、可能な限り単に識別情報を提供することを避けたりします。

## ビジネスモデルとしての監視

<span class="pg-brown">:material-account-cash: 監視資本主義</span>

> 監視資本主義は営利目的のために個人データを収集し、商品化する経済的な仕組みのことです。[^3]

多くの人にとって、民間企業による追跡と監視への懸念は大きくなっています。 GoogleやFacebookが運営するような広範な広告ネットワークは自らが管理するサイトだけではなく、インターネット中に及び、人々の行動を追跡しています。 広告ネットワークサーバーへのネットワークリクエストを制限するコンテンツブロッカーを使ったり、使っているサービスのプライバシーポリシーを読んだりすることで多くの基本的なものを避けることができます（完全に追跡を防ぐことはできません）。[^4]

さらに、*アドテック*やトラッキング業界以外の企業であっても、[データブローカー](https://en.wikipedia.org/wiki/Information_broker)（Cambridge Analytica、ExperianやDatalogixなど）や他の事業者と共有することがあります。 利用しているサービスが典型的なアドテックやトラッキングのビジネスモデルのものではないからといって、自動的にデータが安全であると考えることはできません。 企業によるデータ収集に対する最も強力な保護方法は、可能な限りデータの暗号化や難読化をして、プロバイダーによるデータの関連付けとプロファイルの作成を難しくすることです。

## Limiting Public Information

<span class="pg-green">:material-account-search: Public Exposure</span>

The best way to keep your data private is simply not making it public in the first place. Deleting unwanted information you find about yourself online is one of the best first steps you can take to regain your privacy.

- [アカウント削除に関するガイド :material-arrow-right-drop-circle: を表示](account-deletion.md)

On sites where you do share information, checking the privacy settings of your account to limit how widely that data is spread is very important. For example, enable "private mode" on your accounts if given the option: This ensures that your account isn't being indexed by search engines, and that it can't be viewed without your permission.

If you've already submitted your real information to sites which shouldn't have it, consider using disinformation tactics, like submitting fictitious information related to that online identity. This makes your real information indistinguishable from the false information.

## 検閲の回避

<span class="pg-blue-gray">:material-close-outline: 検閲</span>

Censorship online can be carried out (to varying degrees) by actors including totalitarian governments, network administrators, and service providers. These efforts to control communication and restrict access to information will always be incompatible with the human right to Freedom of Expression.[^5]

Censorship on corporate platforms is increasingly common, as platforms like Twitter and Facebook give in to public demand, market pressures, and pressures from government agencies. Government pressures can be covert requests to businesses, such as the White House [requesting the takedown](https://nytimes.com/2012/09/17/technology/on-the-web-a-fine-line-on-free-speech-across-globe.html) of a provocative YouTube video, or overt, such as the Chinese government requiring companies to adhere to a strict regime of censorship.

People concerned with the threat of censorship can use technologies like [Tor](../advanced/tor-overview.md) to circumvent it, and support censorship-resistant communication platforms like [Matrix](../real-time-communication.md#element), which doesn't have a centralized account authority that can close accounts arbitrarily.

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

While evading censorship itself can be easy, hiding the fact that you are doing it can be very problematic.

You should consider which aspects of the network your adversary can observe, and whether you have plausible deniability for your actions. For example, using [encrypted DNS](../advanced/dns-overview.md#what-is-encrypted-dns) can help you bypass rudimentary, DNS-based censorship systems, but it can't truly hide what you are visiting from your ISP. A VPN or Tor can help hide what you are visiting from network administrators, but can't hide that you're using those networks in the first place. Pluggable transports (such as Obfs4proxy, Meek, or Shadowsocks) can help you evade firewalls that block common VPN protocols or Tor, but your circumvention attempts can still be detected by methods like probing or [deep packet inspection](https://en.wikipedia.org/wiki/Deep_packet_inspection).

</div>

You must always consider the risks of trying to bypass censorship, the potential consequences, and how sophisticated your adversary may be. You should be cautious with your software selection, and have a backup plan in case you are caught.

[^1]: Wikipedia: [*Mass Surveillance*](https://en.wikipedia.org/wiki/Mass_surveillance) and [*Surveillance*](https://en.wikipedia.org/wiki/Surveillance).
[^2]: United States Privacy and Civil Liberties Oversight Board: [*Report on the Telephone Records Program Conducted under Section 215*](https://documents.pclob.gov/prod/Documents/OversightReport/ec542143-1079-424a-84b3-acc354698560/215-Report_on_the_Telephone_Records_Program.pdf)
[^3]: Wikipedia: [*Surveillance capitalism*](https://en.wikipedia.org/wiki/Surveillance_capitalism)
[^4]: "[Enumerating badness](https://ranum.com/security/computer_security/editorials/dumb)" (or, "listing all the bad things that we know about"), as many content blockers and antivirus programs do, fails to adequately protect you from new and unknown threats because they have not yet been added to the filter list. You should also employ other mitigation techniques.
[^5]: United Nations: [*Universal Declaration of Human Rights*](https://un.org/en/about-us/universal-declaration-of-human-rights).
