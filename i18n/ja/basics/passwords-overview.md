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

A lot of services impose certain criteria when it comes to passwords, including a minimum or maximum length, as well as which special characters, if any, can be used. You should use your password manager's built-in password generator to create passwords that are as long and complex as the service will allow by including capitalized and lowercase letters, numbers and special characters.

If you need a password you can memorize, we recommend a [diceware passphrase](#diceware-passphrases).

### Diceware Passphrases

Diceware is a method for creating passphrases which are easy to remember, but hard to guess.

Diceware passphrases are a great option when you need to memorize or manually input your credentials, such as for your password manager's master password or your device's encryption password.

An example of a diceware passphrase is `viewable fastness reluctant squishy seventeen shown pencil`.

To generate a diceware passphrase using real dice, follow these steps:

<div class="admonition Note" markdown>
<p class="admonition-title">Note</p>

These instructions assume that you are using [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) to generate the passphrase, which requires five dice rolls per word. Other word lists may require more or less rolls per word, and may require a different amount of words to achieve the same entropy.

</div>

1. Roll a six-sided die five times, noting down the number after each roll.

2. As an example, let's say you rolled `2-5-2-6-6`. Look through the [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) for the word that corresponds to `25266`.

3. You will find the word `encrypt`. Write that word down.

4. Repeat this process until your passphrase has as many words as you need, which you should separate with a space.

<div class="admonition warning" markdown>
<p class="admonition-title">Important</p>

You should **not** re-roll words until you get a combination of words that appeal to you. The process should be completely random.

</div>

If you don't have access to or would prefer to not use real dice, you can use your password manager's built-in password generator, as most of them have the option to generate diceware passphrases in addition to regular passwords.

We recommend using [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) to generate your diceware passphrases, as it offers the exact same security as the original list, while containing words that are easier to memorize. There are also [word lists in different languages](https://theworld.com/~reinhold/diceware.html#Diceware%20in%20Other%20Languages|outline), if you do not want your passphrase to be in English.

<details class="note" markdown>
<summary>Explanation of entropy and strength of diceware passphrases</summary>

To demonstrate how strong diceware passphrases are, we'll use the aforementioned seven word passphrase (`viewable fastness reluctant squishy seventeen shown pencil`) and [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) as an example.

One metric to determine the strength of a diceware passphrase is how much entropy it has. The entropy per word in a diceware passphrase is calculated as <math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <mtext>WordsInList</mtext> <mo form="postfix" stretchy="false">)</mo> </mrow> </math> and the overall entropy of the passphrase is calculated as: <math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <msup> <mtext>WordsInList</mtext> <mtext>WordsInPhrase</mtext> </msup> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>

Therefore, each word in the aforementioned list results in ~12.9 bits of entropy (<math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <mn>7776</mn> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>), and a seven word passphrase derived from it has ~90.47 bits of entropy (<math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <msup> <mn>7776</mn> <mn>7</mn> </msup> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>).

The [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) contains 7776 unique words. To calculate the amount of possible passphrases, all we have to do is <math> <msup> <mtext>WordsInList</mtext> <mtext>WordsInPhrase</mtext> </msup> </math>, or in our case, <math><msup><mn>7776</mn><mn>7</mn></msup></math>.

Let's put all of this in perspective: A seven word passphrase using [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) is one of ~1,719,070,799,748,422,500,000,000,000 possible passphrases.

On average, it takes trying 50% of all the possible combinations to guess your phrase. With that in mind, even if your adversary is capable of ~1,000,000,000,000 guesses per second, it would still take them ~27,255,689 years to guess your passphrase. That is the case even if the following things are true:

- Your adversary knows that you used the diceware method.
- Your adversary knows the specific word list that you used.
- Your adversary knows how many words your passphrase contains.

</details>

To sum it up, diceware passphrases are your best option when you need something that is both easy to remember *and* exceptionally strong.

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
