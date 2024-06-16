---
title: 翻譯
---

Crowdin 有很好的文件，我們建議您查看他們的[入門指南](https://support.crowdin.com/crowdin-intro)。 我們的網站大量使用 [Markdown](https://en.wikipedia.org/wiki/Markdown) 撰寫，所以應該很容易貢獻翻譯。 這個頁面包含了一些有用的提示，教您如何翻譯我們網站上可能會遇到的特定語法。

如果您有其他問題的話，請加入我們在 Matrix 上的在地化群組 ([#pg-i18n:aragon.sh](https://matrix.to/#/%23pg-i18n:aragon.sh))，並閱讀 [部落格公告](https://blog.privacyguides.org/2023/02/26/i18n-announcement) 取得關於本計劃的進一步資訊。

請以本網站的英文版本為主，更新均以英文為優先。 如果您發現落後於英文，還請伸出援手。 我們無法保證所有翻譯的正確性 如果您對您所在地區的特定內容有任何建議，請在我們的 [主要存取庫](https://github.com/privacyguides/privacyguides.org) 中打開問題或 pull request。

## 匯出翻譯

翻譯軟體能夠提供相當準確的翻譯；然而，您需要確保翻譯的內容是正確的。

例如：

```text
![Software logo](assets/img/path/to/image.svg){ align=right }
```

我們有時發現，像上面那樣插入圖像的語法中缺少了 `![`，或者在文字和路徑之間多了一個空格，例如 `](`。 如果該字串翻譯的不正確，我們鼓勵您按下垃圾桶按鈕**刪除**，或是[投票](https://support.crowdin.com/enterprise/getting-started-for-volunteers/#voting-view)給您認為看起來最棒的翻譯。 當不適合的字串被刪除，它們會從組織裡的[翻譯記憶](https://support.crowdin.com/enterprise/translation-memory)刪除，意思是當來源字串再一次出現時，不會再推薦不正確的翻譯。

## 標點符號

For examples like the above admonitions, quotation marks, e.g.: `" "` must be used to specify string text. MkDocs will not correctly interpret other symbols i.e., `「 」` or `« »`. Other punctuation marks are fine for marking regular quotations within the text otherwise.

## Fullwidth alternatives and Markdown syntax

CJK writing systems tend to use alternative "fullwidth" variants of common symbols. These are different characters and cannot be used for markdown syntax.

- Links must use regular parenthesis ie `(` (Left Parenthesis U+0028) and `)` (Right Parenthesis U+0029) and not `（` (Fullwidth Left Parenthesis U+FF08) or `）` (Fullwidth Right Parenthesis U+FF09)
- Indented quoted text must use `:` (Colon U+003A) and not `：` (Fullwidth Colon U+FF1A)
- Pictures must use `!` (Exclamation Mark U+0021) and not `！` (Fullwidth Exclamation Mark U+FF01)
