---
title: "Introduction to Passwords"
icon: 'material/form-textbox-password'
description: These are some tips and tricks on how to create the strongest passwords and keep your accounts secure.
---

密码是我们日常数字生活的重要组成部分。 我们用它们来保护我们的账户、我们的设备和我们的秘密。 尽管密码可能是挡在觊觎我们私人信息的对手前的唯一屏障，但人们并没有在密码上花很多心思，这往往导致使用的密码很容易被猜出或被破解。

## 最佳实践

### 为每项服务使用独立的密码

想象一下；你用同一个电子邮件和相同的密码在 注册了多个在线服务的账户。 只要这些服务提供商有一个是恶意的，或者他们的服务出现数据泄露，使你的密码以明文形式暴露出来，那么坏人只需要在多个流行的服务中尝试这个电子邮件和密码的组合，就能得手。 密码有多强根本不重要，因为那个密码他们已经拿到了。

这被称为[凭据填充](https://en.wikipedia.org/wiki/Credential_stuffing), 这也是坏人攻破你帐户的最常见方式之一。 为了避免这种情况，确保你从不复用你的密码。

### 使用随机生成的密码

==你 **绝不**应该依靠自己去想出一个好密码 == 我们建议使用[随机生成的密码](#passwords) 或者 [diceware短语](#diceware) ，它们的熵值需要足够大，才能保护你的帐户和设备。

所有我们 [推荐的密码管理器](../passwords.md) 都有一个你可以使用的内置密码生成器。

### 轮换密码

除非你有理由相信它已被泄露，否则应避免过于频繁地更改你必须记住的密码（比如密码管理器的主密码），因为过于频繁地更改密码提高了你忘记密码的风险。

When it comes to passwords that you don't have to remember (such as passwords stored inside your password manager), if your [threat model](threat-modeling.md) calls for it, we recommend going through important accounts (especially accounts that don't use multifactor authentication) and changing their password every couple of months, in case they have been compromised in a data breach that hasn't become public yet. 大多数密码管理器允许你为你的密码设置一个到期日，使之更容易管理。

<div class="admonition tip" markdown>
<p class="admonition-title">Checking for data breaches</p>

如果你的密码管理器允许你检查被泄露的密码，请确保这样做，并及时更改任何可能在数据泄露中被泄露的密码。 你还可以在[新闻聚合器](.../news-aggregators.md)的帮助下关注[Have I Been Pwned's Latest Breaches feed]（https://feeds.feedburner.com/HaveIBeenPwnedLatestBreaches）。

</div>

## 创建强密码

### 密码

很多服务在涉及到密码时都有一定的标准，包括最小或最大长度，以及可以使用哪些特殊字符（如果有的话）。 你应该使用你的密码管理器的内置密码生成器，通过包括大写和小写字母、数字和特殊字符，创建当前服务所允许的尽可能长和复杂的密码。

如果你需要一个可以记住的密码，我们推荐[diceware口令](#diceware)。

### Diceware口令

Diceware是一种创建密码的方法，这种密码容易记忆，但很难猜到。

当你需要记忆或手动输入你的凭证时，Diceware口令是一个很好的选择，例如，你的密码管理器的主密码或你的设备的加密密码。

一个diceware口令的例子是`viewable fastness reluctant squishy seventeen shown pencil`.

要使用真正的骰子生成一个diceware口令，请遵循以下步骤。

<div class="admonition Note" markdown>
<p class="admonition-title">Note</p>

These instructions assume that you are using [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) to generate the passphrase, which requires five dice rolls per word. Other word lists may require more or less rolls per word, and may require a different amount of words to achieve the same entropy.

</div>

1. 掷一个六面体的骰子五次，每次掷完都记下数字。

2. 举个例子，假设你掷出 `2-5-2-6-6`。 Look through the [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) for the word that corresponds to `25266`.

3. 你可以得到这个词 `encrypt` 把这个词写下来。

4. 重复这个过程，直到你的口令有你所需要的字数，你应该用空格来分隔每个词。

<div class="admonition warning" markdown>
<p class="admonition-title">Important</p>

你**不**应该重新生成单词，来得到一个吸引你的单词组合。 这个过程应该是完全随机的。

</div>

如果你没有或者不愿意使用真正的骰子，你可以使用你的密码管理器的内置密码生成器，因为除了常规密码之外，大多数密码管理器都有生成骰子密码的选项。

We recommend using [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) to generate your diceware passphrases, as it offers the exact same security as the original list, while containing words that are easier to memorize. There are also [word lists in different languages](https://theworld.com/~reinhold/diceware.html#Diceware%20in%20Other%20Languages|outline), if you do not want your passphrase to be in English.

<details class="note" markdown>
<summary>Explanation of entropy and strength of diceware passphrases</summary>

To demonstrate how strong diceware passphrases are, we'll use the aforementioned seven word passphrase (`viewable fastness reluctant squishy seventeen shown pencil`) and [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) as an example.

One metric to determine the strength of a diceware passphrase is how much entropy it has. The entropy per word in a diceware passphrase is calculated as <math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <mtext>WordsInList</mtext> <mo form="postfix" stretchy="false">)</mo> </mrow> </math> and the overall entropy of the passphrase is calculated as: <math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <msup> <mtext>WordsInList</mtext> <mtext>WordsInPhrase</mtext> </msup> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>

Therefore, each word in the aforementioned list results in ~12.9 bits of entropy (<math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <mn>7776</mn> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>), and a seven word passphrase derived from it has ~90.47 bits of entropy (<math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <msup> <mn>7776</mn> <mn>7</mn> </msup> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>).

The [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) contains 7776 unique words. To calculate the amount of possible passphrases, all we have to do is <math> <msup> <mtext>WordsInList</mtext> <mtext>WordsInPhrase</mtext> </msup> </math>, or in our case, <math><msup><mn>7776</mn><mn>7</mn></msup></math>.

Let's put all of this in perspective: A seven word passphrase using [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) is one of ~1,719,070,799,748,422,500,000,000,000 possible passphrases.

平均而言，需要尝试所有可能的组合中的50%来猜测你的短语。 考虑到这一点，即使你的对手每秒能够猜出1,000,000,000,000次，他们仍然需要27,255,689年才能猜出你的口令。 即使以下情况属实，情况也是如此:

- 你的对手知道你使用了diceware方法。
- Your adversary knows the specific word list that you used.
- 你的对手知道你的口令包含多少个字。

</details>

总而言之，当你需要一些既容易记住 *，又特别强大的* ，Diceware密码是你最好的选择。

## 存储密码

### 生产力工具

存储密码的最佳方式是使用密码管理器。 它们允许你将密码存储在文件或云中，并以单一的主密码保护它们。 这样一来，你只需记住一个强密码，就可以访问其余的密码。

有许多好的选择，包括基于云的和本地的。 选择我们推荐的密码管理器之一，并使用它在你的所有账户中建立强大的密码。 我们建议用一个至少由七个词组成的 [diceware](#diceware) 口令来保护你的密码管理器。

[推荐的密码管理器列表](../passwords.md ""){.md-button}

<div class="admonition warning" markdown>
<p class="admonition-title">Don't place your passwords and TOTP tokens inside the same password manager</p>

When using [TOTP codes as multifactor authentication](multi-factor-authentication.md#time-based-one-time-password-totp), the best security practice is to keep your TOTP codes in a [separate app](../multi-factor-authentication.md).

你应该使用专门的[TOTP应用程序]（.../multi-factor-authentication.md/#authenticator-apps）来代替。

此外，我们不建议在您的密码管理器中存储用于一次性恢复的代码。 它们应当单独存储在，例如离线存储设备上的加密容器中。

</div>

### 备份

你应该在多个存储设备或云存储提供商上存储 [加密的](../encryption.md) 密码备份。 如果你的主要设备或你正在使用的服务发生意外，这可以帮助你访问你的密码。
