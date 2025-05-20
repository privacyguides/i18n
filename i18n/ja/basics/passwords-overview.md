---
title: パスワードの概要
icon: material/form-textbox-password
description: 強固なパスワードを作成し、アカウントを安全に保つヒントやコツを紹介します。
---

パスワードは、日々のデジタルライフに欠かせないものです。 We use them to protect our accounts, our devices, and our secrets. パスワードは多くの場合、敵対者から個人情報を守る唯一の要素です。にも関わらず、十分に検討されず、簡単に推測できたり、総当たりできるパスワードが使われることが多いようです。

## ベストプラクティス

### 各サービスで異なるパスワードを使う

Imagine this: You sign up for an account with the same e-mail and password on multiple online services. もし、いずれかのサービス提供者が悪意を持っていたり、サービスが情報漏洩を起こしてパスワードが暗号化されていない状態で公開された場合、悪意ある者は他の人気あるサービスでそのメールアドレスとパスワードの組み合わせでログインを試すことができます。 そのパスワードがどれだけ強固でも、悪意ある者に漏洩した場合は安全性を担保できません。

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

If you don't have access to or would prefer to not use real dice, you can use your password manager's built-in password generator, as most of them have the option to generate diceware passphrases in addition to regular passwords. We recommend setting the generated passphrase length to at least 6 words.

We also recommend using [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) to generate your diceware passphrases, as it offers the exact same security as the original list, while containing words that are easier to memorize. 英語のパスフレーズを使いたくない場合、[他言語の単語リスト](https://theworld.com/~reinhold/diceware.html#Diceware%20in%20Other%20Languages|outline)もあります。

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

パスワードを保存する最もよい方法は、パスワードマネージャーを使うことです。 パスワードをファイルやクラウド上に保存し、一つのマスターパスワードで保護することができます。 一つの強力なパスワードを覚えておくだけで全てのパスワードにアクセスすることができます。

クラウドでもローカルでも、多くのよい選択肢があります。 推奨されるパスワードマネージャーを選び、使うことで全てのアカウントに強力なパスワードを設定してください。 パスワードマネージャーには少なくとも7単語の[ダイスウェアパスフレーズ](#diceware-passphrases)で保護することを推奨します。

[推奨するパスワードマネージャー](../passwords.md ""){.md-button}

<div class="admonition warning" markdown>
<p class="admonition-title">パスワードとTOTPトークンを同じパスワードマネージャーに保存しないこと</p>

[TOTPコードを多要素認証](multi-factor-authentication.md#time-based-one-time-password-totp)として使用する場合、TOTPコードは[別のアプリ](../multi-factor-authentication.md)に保存することが最もよいセキュリティプラクティスです。

TOTPトークンとパスワードを同じ場所に保存するのは便利ですが、敵対者がパスワードマネージャーにアクセスできた場合に、一要素に減ってしまいます。

さらに、パスワードマネージャーには1回のみ利用できるリカバリーコードを保存することは推奨しません。 暗号化されたコンテナなど、オフラインのストレージデバイスに分けて保存する必要があります。

</div>

### バックアップ

パスワードの[暗号化された](../encryption.md)バックアップは、複数のストレージデバイスやクラウドストレージなどに保存する必要があります。 主に使っているデバイスやサービスに何かあった場合に、パスワードにアクセスするのに役立ちます。
