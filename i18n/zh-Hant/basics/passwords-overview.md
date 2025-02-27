---
title: "密碼介紹"
icon: 'material/form-textbox-password'
description: 以下是關於如何建立最強密碼並確保帳戶安全的一些提示和技巧。
---

密碼是我們日常數位生活的重要組成部分。 我們使用它們來保護自己帳戶、設備和祕密。 儘管密碼常常是我們與挖取我們私人資訊的對手之間僅有的唯一阻隔，但人們並未對密碼有充分的考量，導致人們使用的密碼很容易被猜到或強力破解。

## 最佳實踐

### 每項服務各選用不同的獨特密碼

想像一下，您在各個不同的網路服務註冊時都使用同一組電子郵件和密碼。 如果其中一個服務提供商懷有惡意，或者其服務發生資料洩露，以未加密格式暴露了您的密碼，那麼不良行為者只需嘗試跨多個流行服務的電子郵件和密碼組合，就可輕易得手。 密碼強度已無關緊要，因為對手已經打開它了。

這稱為 [憑證填充](https://en.wikipedia.org/wiki/Credential_stuffing)，是最常見帳戶被不良行為者破壞的方式之一。 為了避免這種情況，請確保您永遠不會重複使用密碼。

### 使用隨機生成的密碼

==您 **不應該** 僅靠自己去想出好密碼== ;建議使用充足熵量的[隨機產生密碼randomly generated passwords](#passwords) 或 [diceware 口令密語](#diceware-passphrases) ，以保護裝備和帳戶的安全。

我們所推薦的 [密碼管理器](../passwords.md) 都內建密碼生成器。

### 輪換密碼

應避免經常更改必須記住的密碼（例如密碼管理器的主密碼） ，除非有理由相信它已被破壞，否則頻繁更改它往往會使您面臨忘記密碼的風險。

When it comes to passwords that you don't have to remember (such as passwords stored inside your password manager), if your [threat model](threat-modeling.md) calls for it, we recommend going through important accounts (especially accounts that don't use multifactor authentication) and changing their password every couple of months, in case they have been compromised in a data breach that hasn't become public yet. 大多數密碼管理器可為密碼設定到期日期，以便更容易管理。

<div class="admonition tip" markdown>
<p class="admonition-title">檢查資料洩露</p>

如果您的密碼管理器可以檢查密碼是否已被破壞，請務必檢查並立即更改可能已暴露在資料外洩的密碼。 或者，您可以在 [news aggregator](../news-aggregators.md)的幫助下關注 [Have I Been Pwned 最新資料外洩情報](https://feeds.feedburner.com/HaveIBeenPwnedLatestBreaches)。

</div>

## 建立強密碼

### 密碼

許多服務對密碼施加了某些標準，包括最小或最大長度，以及可以使用哪些特殊字符（如果有的話）。 您應該利用密碼管理器內建的密碼生成器來創建夠長、複雜的密碼，只要服務允許，最好是混合大寫和小寫字母、數字和特殊字符搭配。

若需要一個記得住的密碼，建議採用 [diceware 口令密語](#diceware-passphrases)。

### Diceware 口令密語

Diceware 是一種創建密碼短語的方法，這些密短口令易於記憶，但很難猜測。

當您需要記憶或手動輸入憑證時，例如密碼管理員的主密碼或設備的加密密碼， Diceware 口令密語是個好選擇。

舉一個 Diceware 口令密語的例子 `viewable fastness reluctant squishy seventeen shown pencil`。

使用骰子來產生一組 diceware 口令密語，請按照以下步驟：

<div class="admonition Note" markdown>
<p class="admonition-title">Note "備註"</p>

These instructions assume that you are using [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) to generate the passphrase, which requires five dice rolls per word. Other word lists may require more or less rolls per word, and may require a different amount of words to achieve the same entropy.

</div>

1. 將1~6 骰子滾動五次，記下每次出現的數字。

2. 例如，假設您滾動了 `2-5-2-6-6`。 Look through the [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) for the word that corresponds to `25266`.

3. 你會得到單詞 `encrypt`。 把這個詞寫下來。

4. 重複相同手續，直到您的口令密語達到足夠的單詞，請用空格分隔單詞。

<div class="admonition warning" markdown>
<p class="admonition-title">重要</p>

你 **不應** 重新滾動單詞，以取得自己喜好的單詞組合。 這個過程應該是完全隨機的。

</div>

如果您手邊沒有或不想使用真正的骰子，可利用密碼管理器內建密碼生成器，因為大多數密碼生成器除了普通密碼之外還可以選擇生成 diceware 口令密語。

We recommend using [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) to generate your diceware passphrases, as it offers the exact same security as the original list, while containing words that are easier to memorize. There are also [word lists in different languages](https://theworld.com/~reinhold/diceware.html#Diceware%20in%20Other%20Languages|outline), if you do not want your passphrase to be in English.

<details class="note" markdown>
<summary>diceware 口令密語的熵和強度的說明</summary>

To demonstrate how strong diceware passphrases are, we'll use the aforementioned seven word passphrase (`viewable fastness reluctant squishy seventeen shown pencil`) and [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) as an example.

判斷 diceware 口令密語強度的衡量標準是確定它有多少熵。 Diceware 密碼短語中每個單字的熵計算如下 <math> <mrow> <msub> <mtext>記錄(log)</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <mtext>WordsInList</mtext> <mo form="postfix" stretchy="false">)</mo> </mrow> </math> 密碼短語的整體熵計算如下： <math> <mrow> <msub> <mtext>記錄(log)</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <msup> <mtext>WordsInList</mtext> <mtext>WordsInPhrase</mtext> </msup> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>

因此，上述列表中的每個單字都會產生約 12.9 位元的熵（<math> <mrow> <msub> <mtext>記錄(log)</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <mn>7776</mn> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>），從它衍生出的七字密碼有約 90.47 位元的熵（<math> <mrow> <msub> <mtext>記錄(log)</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <msup> <mn>7776</mn> <mn>7</mn> </msup> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>).

The [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) contains 7776 unique words. 要計算可能的密碼短語的數量，要做的就是 <math> <msup> <mtext>WordsInList</mtext> <mtext>WordsInPhrase</mtext> </msup> </math>，或者在我們的例子中， <math><msup><mn>7776</mn><mn>7</mn></msup></math>.

Let's put all of this in perspective: A seven word passphrase using [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) is one of ~1,719,070,799,748,422,500,000,000,000 possible passphrases.

平均而言，至少要嘗試所有可能組合的一半來猜測您的密語。 考慮到這一點，即使對手每秒能夠猜測~ 1,000,000,000,000 次，他們仍然需要~ 27,255,689 年來猜出您的密語。 即使以下情況屬實，也是如此：

- 對手知道您使用 diceware 方法。
- Your adversary knows the specific word list that you used.
- 對手知道您的密語包含多少個單詞。

</details>

總而言之， diceware 口令密語是最佳選擇，當您需要既容易記住 *又* 非常強大的東西。

## 儲存密碼

### 密碼管理器。

儲存密碼的最佳方式是使用密碼管理器。 可將密碼儲存在檔案或雲端，使用單個主密碼保護與開啟它們。 這樣，您只需要記住一個強大的密碼，就可以訪問其餘密碼。

有許多好的選項可參考，不管是雲端和本地設備安裝。 選擇任一推薦的密碼管理器，利用它為所有帳戶建立強密碼。 建議利用至少七個單詞的 [diceware 口令密語](#diceware-passphrases) 來保護密碼管理器的安全。

[推薦的密碼管理員列表](../passwords.md ""){.md-button}

<div class="admonition warning" markdown>
<p class="admonition-title">Warning "不要將密碼和 TOTP 令牌放在同一個密碼管理器中</p>

When using [TOTP codes as multifactor authentication](multi-factor-authentication.md#time-based-one-time-password-totp), the best security practice is to keep your TOTP codes in a [separate app](../multi-factor-authentication.md).

將您的 TOTP 令牌儲存在與密碼相同的位置，雖然方便，但假若對手可以存取密碼管理器，則帳戶安全驗證則減少為單一因素。

此外，我們不建議把一次性修復代碼儲存在密碼管理器。 它們應分開儲存，例如放在離線儲存設備的加密容器中。

</div>

### 備份

您應該將密碼備份 [加密](../encryption.md) 在 數個儲存裝置或雲端儲存服務。 如果您主要裝置或正在使用的服務出問題，這可以幫助您存得密碼。
