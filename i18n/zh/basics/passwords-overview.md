---
title: "密码简介"
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

而那些你不需要记住的密码（如存储在密码管理器内的密码），如果你的 [威胁模型](threat-modeling.md) 有需求，我们建议每隔几个月对重要账户（尤其是不使用多因认证的账户）进行检查并更改其密码，以防它们在尚未公开的数据泄露事件中被泄露。 大多数密码管理器允许你为你的密码设置一个到期日，使之更容易管理。

!!! 提示 "检查数据泄露情况"

    如果你的密码管理器允许你检查被泄露的密码，请确保这样做，并及时更改任何可能在数据泄露中被泄露的密码。 你还可以在[新闻聚合器](.../news-aggregators.md)的帮助下关注[Have I Been Pwned's Latest Breaches feed]（https://feeds.feedburner.com/HaveIBeenPwnedLatestBreaches）。

## 创建强密码

### 密码

很多服务在涉及到密码时都有一定的标准，包括最小或最大长度，以及可以使用哪些特殊字符（如果有的话）。 你应该使用你的密码管理器的内置密码生成器，通过包括大写和小写字母、数字和特殊字符，创建当前服务所允许的尽可能长和复杂的密码。

如果你需要一个可以记住的密码，我们推荐[diceware口令](#diceware)。

### Diceware口令

Diceware是一种创建密码的方法，这种密码容易记忆，但很难猜到。

当你需要记忆或手动输入你的凭证时，Diceware口令是一个很好的选择，例如，你的密码管理器的主密码或你的设备的加密密码。

一个diceware口令的例子是`viewable fastness reluctant squishy seventeen shown pencil`.

要使用真正的骰子生成一个diceware口令，请遵循以下步骤。

!!! note

    这里的说明步骤假定你使用[EFF的大型词汇表](https://www.eff.org/files/2016/07/18/eff_large_wordlist.txt)来生成口令，每个词需要掷五个骰子。 其他词表可能需要更多或更少的回合，也可能需要不同数量的词来实现相同的熵值。

1. 掷一个六面体的骰子五次，每次掷完都记下数字。

2. 举个例子，假设你掷出 `2-5-2-6-6`。 通过 [EFF的大词表](https://www.eff.org/files/2016/07/18/eff_large_wordlist.txt) ，寻找与 `25266`相对应的词。

3. 你可以得到这个词 `encrypt` 把这个词写下来。

4. 重复这个过程，直到你的口令有你所需要的字数，你应该用空格来分隔每个词。

!!! 警告 “重要”

    你**不**应该重新生成单词，来得到一个吸引你的单词组合。 这个过程应该是完全随机的。

如果你没有或者不愿意使用真正的骰子，你可以使用你的密码管理器的内置密码生成器，因为除了常规密码之外，大多数密码管理器都有生成骰子密码的选项。

我们建议使用 [EFF的大型词表](https://www.eff.org/files/2016/07/18/eff_large_wordlist.txt) ，以生成你的二维码密码，因为它提供了与原始列表完全相同的安全性，同时包含更容易记忆的单词。 There are also [other wordlists in different languages](https://theworld.com/~reinhold/diceware.html#Diceware%20in%20Other%20Languages|outline), if you do not want your passphrase to be in English.

??? 注："解释熵和二维码密码的强度"

    为了演示diceware密码短语有多强，我们将使用前面提到的七个单词密码短语`'viewable fastness，squishy seventeen showed pencil'`和[EFF的大单词列表]（https://www.eff.org/files/2016/07/18/eff_large_wordlist.txt)为例。
    
    确定双关口令强度的一个指标是它的熵值有多少。 双关口令中每个字的熵计算为$\text{log}_2(\text{WordsInList})$，口令的整体熵计算为$\text{log}_2(\text{WordsInList}^\text{WordsInPhrase})$。
    
    因此，上述列表中的每个词都会产生~12.9比特的熵($\text{log}_2(7776)$)，而由它衍生出的七个词的口令有~90.47比特的熵($\text{log}_2(7776^7)$)。
    
    [EFF的大词表](https://www.eff.org/files/2016/07/18/eff_large_wordlist.txt)包含7776个独特的词。 要计算可能的口令数量，我们所要做的就是$\text{WordsInList}^\text{WordsInPhrase}$，或者在我们的例子中，$7776^7$。
    
    让我们换一个角度来看：使用[EFF 's large wordlist] （ https://www.eff.org/files/2016/07/18/eff_large_wordlist.txt ）的七个单词密码是~ 1,719,070,799,748,422,500,000,000,000个可能的密码之一。
    
    平均而言，需要尝试所有可能的组合中的50%来猜测你的短语。 考虑到这一点，即使你的对手每秒能够猜出1,000,000,000,000次，他们仍然需要27,255,689年才能猜出你的口令。 即使以下情况属实，情况也是如此:

    - 你的对手知道你使用了diceware方法。
    - 你的对手知道你使用的具体词表。
    - 你的对手知道你的口令包含多少个字。

总而言之，当你需要一些既容易记住 *，又特别强大的* ，Diceware密码是你最好的选择。

## 存储密码

### 生产力工具

存储密码的最佳方式是使用密码管理器。 它们允许你将密码存储在文件或云中，并以单一的主密码保护它们。 这样一来，你只需记住一个强密码，就可以访问其余的密码。

有许多好的选择，包括基于云的和本地的。 选择我们推荐的密码管理器之一，并使用它在你的所有账户中建立强大的密码。 我们建议用一个至少由七个词组成的 [diceware](#diceware) 口令来保护你的密码管理器。

[推荐的密码管理器列表](../passwords.md ""){.md-button}

!!! 警告 "不要把你的密码和TOTP令牌放在同一个密码管理器中"

    如果您将TOTP用作任何帐户的 [多因素身份验证](../multi-factor-authentication.md) 方法，请勿在密码管理器中存储这些令牌、它们的任何备份代码或TOTP秘密本身，那样会抵消掉多因认证的益处。
    
    你应该使用专门的[TOTP应用程序]（.../multi-factor-authentication.md/#authenticator-apps）来代替。
    
    此外，我们不建议在您的密码管理器中存储用于一次性恢复的代码。 它们应当单独存储在，例如离线存储设备上的加密容器中。

### 备份

你应该在多个存储设备或云存储提供商上存储 [加密的](../encryption.md) 密码备份。 如果你的主要设备或你正在使用的服务发生意外，这可以帮助你访问你的密码。
