---
title: "パスワードの概要"
icon: 'material/form-textbox-password'
description: 強固なパスワードを作成し、アカウントを安全に保つヒントやコツを紹介します。
---

パスワードは、日々のデジタルライフに欠かせないものです。 私たちは、アカウント、デバイス、秘密を守るためにパスワードを使用します。 パスワードは多くの場合、敵対者から個人情報を守る唯一の要素です。にも関わらず、十分に検討されず、簡単に推測できたり、総当たりできるパスワードが使われることが多いようです。

## ベストプラクティス

### 各サービスで異なるパスワードを使う

複数のオンラインサービスで、同じメールアドレスとパスワードを使ってアカウントを作成した場合を想像してください。 もし、いずれかのサービス提供者が悪意を持っていたり、サービスが情報漏洩を起こしてパスワードが暗号化されていない状態で公開された場合、悪意ある者は他の人気あるサービスでそのメールアドレスとパスワードの組み合わせでログインを試すことができます。 そのパスワードがどれだけ強固でも、悪意ある者に漏洩した場合は安全性を担保できません。

これは、[クレデンシャルスタッフィング攻撃](https://en.wikipedia.org/wiki/Credential_stuffing)と呼ばれ、悪意ある者がアカウントを侵害するために用いる、よくある攻撃の一つです。 この攻撃への有効な対策は、パスワードを使いまわさないことです。

### ランダムに生成されたパスワードを使う

==自力でパスワードを考え出すことは**決して**行わないでください。==アカウントやデバイスを保護するために、十分なエントロピーがある[ランダムに生成されたパスワード](#passwords)や[ダイスウェアパスフレーズ](#diceware-passphrases)を使うことを推奨します。

推奨する[パスワードマネージャー](../passwords.md)にはパスワードジェネレーターが組み込まれており、使うことができます。

### パスワードを変更する

パスワードの安全性が損なわれたと信じるに足る理由がない限り、覚えて置かなければならないパスワード（パスワードマネージャーのマスターパスワードなど）を頻繁に変更することは避けるべきです。忘れてしまうリスクがあるためです。

覚えておく必要のないパスワード（パスワードマネージャーで保存しているパスワードなど）は[脅威モデル](threat-modeling.md)に基づき、まだ公になっていないデータ漏洩が起きている場合に備え、重要なアカウント（特に多要素認証が使われていないアカウント）を確認し、2〜3ヶ月ごとに変更することを推奨します。 多くのパスワードマネージャーではパスワードの有効期限を設定できるため、管理が簡単になります。

<div class="admonition tip" markdown>
<p class="admonition-title">データ漏洩の確認</p>

パスワードマネージャーで漏洩したパスワードを確認できる場合、必ず確認し、データ漏洩で流出した可能性のあるパスワードは速やかに変更してください。 もしくは[ニュースアグリゲーター](../news-aggregators.md)で[Have I Been Pwned's Latest Breaches feed](https://feeds.feedburner.com/HaveIBeenPwnedLatestBreaches)をフォローすることもできます。

</div>

## 強力なパスワードの作成

### パスワード

多くのサービスでは最小・最大の長さや使用できる特殊文字などパスワードに対し、一定の基準を定めています。 パスワードマネージャーにあるパスワードジェネレーターで 大文字、小文字、数字、特殊文字を含み、サービスが許容する限り長く、複雑なパスワードを生成する必要があります。

覚えておく必要のあるパスワード必要な場合、[ダイスウェアパスフレーズ](#diceware-passphrases)を推奨します。

### ダイスウェアパスフレーズ

ダイスウェアは覚えやすく、推測されにくいパスフレーズを作る方法です。

ダイスウェアパスフレーズはパスワードマネージャーのマスターパスワードやデバイスの暗号化パスワードなど、覚えておく必要があったり、手入力したりする認証情報に適しています。

ダイスウェアパスフレーズの例は`viewable fastness reluctant squishy seventeen shown pencil`です。

ダイスウェアパスフレーズを作成するには実際にサイコロを使って、以下の手順に従ってください：

<div class="admonition Note" markdown>
<p class="admonition-title">メモ</p>

以下の手順では[EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt)を使ってパスフレーズを作成します。1つの単語につき、5回サイコロを振る必要があります。 同じエントロピーを得るために、他の単語リストでは1単語あたりのサイコロを振る回数が上下したり、単語数が異なったりすることがあります。

</div>

1. 6面体のサイコロを5回振り、数値をメモします。

2. 例として、`2-5-2-6-6`が出たとします。 [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt)から`25266`に対応する単語を探します。

3. `encrypt`でした。 これを書き留めます。

4. スペースで区切り、パスフレーズが必要な単語数になるまで繰り返します。

<div class="admonition warning" markdown>
<p class="admonition-title">重要</p>

自分がいいと思うような単語の組み合わせになるまでサイコロを振り直すことは**してはいけません**。 この手順は完全にランダムである必要があります。

</div>

もしサイコロがない、使いたくない場合、パスワードマネージャーのパスワードジェネレーターを使うことができます。多くの場合、通常のパスワードに加え、ダイスウェアパスフレーズを生成するオプションがあります。

ダイスウェアパスフレーズを作るには[EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt)を使うことを推奨します。オリジナルのリストと同じく安全で、覚えやすい単語が含まれています。 英語のパスフレーズを使いたくない場合、[他言語の単語リスト](https://theworld.com/~reinhold/diceware.html#Diceware%20in%20Other%20Languages|outline)もあります。

<details class="note" markdown>
<summary>ダイスウェアパスフレーズのエントロピーと強度の説明</summary>

ダイスウェアパスフレーズの強力さを示すために、先に挙げた7単語のパスフレーズ（ `viewable fastness reluctant squishy seventeen shown pencil`）と[EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt)を例に挙げます。

ダイスウェアパスフレーズの強さを測る指標の一つに、どれだけエントロピーがあるかがあります。 ダイスウェアパスフレーズの単語ごとのエントロピーを計算する方法は次の通りです <math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <mtext>リストの単語数</mtext> <mo form="postfix" stretchy="false">)</mo> </mrow> </math> パスフレーズ全てのエントロピーを計算する方法は次の通りです： <math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <msup> <mtext>リストの単語数</mtext> <mtext>フレーズの単語数</mtext> </msup> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>

以上より、リストにある各単語は12.9ビットのエントロピー（<math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <mn>7776</mn> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>）、７単語のパスフレーズは90.47ビットのエントロピーがあります（<math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <msup> <mn>7776</mn> <mn>7</mn> </msup> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>).

[EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt)には7776個の固有の単語があります。 生成されうるパスフレーズ数を計算する方法は次の通りです <math> <msup> <mtext>リストの単語数</mtext> <mtext>フレーズの単語数</mtext> </msup> </math>今回の場合は次の通りです <math><msup><mn>7776</mn><mn>7</mn></msup></math>.

以上の情報をまとめます：[EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt)を使った7単語のパスフレーズは1,719,070,799,748,422,500,000,000,000個の生成されうるパスフレーズのうちの一つです。

パスフレーズを推測するためには、生成されうる組み合わせの平均50%を試す必要があります。 その場合、敵対者が1秒間に1,000,000,000,000回推測できたとしても、パスフレーズを推測するためには27,255,689年もかかることになります。 たとえ、以下の場合でも同じです：

- 敵対者はあなたがダイスウェアパスフレーズを使ったことを知っている。
- 敵対者はあなたが使った単語リストを知っている。
- 敵対者はパスフレーズに含まれる単語数を知っている。

</details>

以上をまとめると、ダイスウェアパスフレーズは覚えやすく、*かつ*非常に強力なものが必要な場合に最適です。

## パスワードの保存

### パスワードマネージャー

The best way to store your passwords is by using a password manager. They allow you to store your passwords in a file or in the cloud and protect them with a single master password. That way, you will only have to remember one strong password, which lets you access the rest of them.

There are many good options to choose from, both cloud-based and local. Choose one of our recommended password managers and use it to establish strong passwords across all of your accounts. We recommend securing your password manager with a [diceware passphrase](#diceware-passphrases) comprised of at least seven words.

[List of recommended password managers](../passwords.md ""){.md-button}

<div class="admonition warning" markdown>
<p class="admonition-title">Don't place your passwords and TOTP tokens inside the same password manager</p>

When using [TOTP codes as multifactor authentication](multi-factor-authentication.md#time-based-one-time-password-totp), the best security practice is to keep your TOTP codes in a [separate app](../multi-factor-authentication.md).

Storing your TOTP tokens in the same place as your passwords, while convenient, reduces the accounts to a single factor in the event that an adversary gains access to your password manager.

Furthermore, we do not recommend storing single-use recovery codes in your password manager. Those should be stored separately such as in an encrypted container on an offline storage device.

</div>

### バックアップ

You should store an [encrypted](../encryption.md) backup of your passwords on multiple storage devices or a cloud storage provider. This can help you access your passwords if something happens to your primary device or the service you are using.
