---
title: 翻譯
description: 網站貢獻者在我們的網站上新增翻譯的指南。
---

Crowdin 有很好的文件，我們建議您查看他們的 [入門指南](https://support.crowdin.com/crowdin-intro)。 我們的網站大量使用 [Markdown](https://en.wikipedia.org/wiki/Markdown) 撰寫，所以應該很容易貢獻翻譯。 這個頁面包含了一些有用的提示，教您如何翻譯我們網站上可能會遇到的特定語法。

如果您有其他問題的話，請加入我們在 Matrix 上的在地化群組 ([#pg-i18n:aragon.sh](https://matrix.to/#/%23pg-i18n:aragon.sh))，並閱讀 [部落格公告](https://blog.privacyguides.org/2023/02/26/i18n-announcement) 取得關於本計劃的進一步資訊。

請以本網站的英文版本為主，更新均以英文為優先。 如果您發現落後於英文，還請伸出援手。 我們無法保證所有翻譯的正確性。 如果您對您所在地區的特定內容有任何建議，請在我們的 [主要存取庫](https://github.com/privacyguides/privacyguides.org) 中打開問題或 pull request。

## 翻譯輸出

翻譯軟體能夠提供相當準確的翻譯；然而，您需要確保翻譯的內容是正確的。

例如：

```text
![Software logo](assets/img/path/to/image.svg){ align=right }
```

我們有時發現，像上面那樣插入圖像的語法中缺少了 `![`，或者在文字和路徑之間多了一個空格，例如 `](`。 如果該字串翻譯的不正確，我們鼓勵您按下垃圾桶按鈕**刪除**，或是[投票](https://support.crowdin.com/enterprise/getting-started-for-volunteers/#voting-view)給您認為看起來最棒的翻譯。 當不適合的字串被刪除，它們會從組織裡的[翻譯記憶](https://support.crowdin.com/enterprise/translation-memory)刪除，意思是當來源字串再一次出現時，不會再推薦不正確的翻譯。

## 標點符號

例如上面的警告、引號，例如：`" "` 必須用來指定字串文字。 MkDocs 不會正確解析其他符號，例如： `「 」` 或 `« »`。 其他標點符號用於在文字中標記普通引文則沒有問題。

## 全形標點符號和 Markdown 語法

在中日韓書寫系統中的常見標點符號，往往使用"全形"。 These are different characters and cannot be used for Markdown syntax.

- Links must use regular parenthesis i.e. `(` (Left Parenthesis U+0028) and `)` (Right Parenthesis U+0029) and not `（` (Fullwidth Left Parenthesis U+FF08) or `）` (Fullwidth Right Parenthesis U+FF09)
- 內縮的引用文字必須使用 `:` (冒號 U+003A)，而不是 `：` (全形冒號 U+FF1A)
- 圖片必須使用 `!` (驚嘆號 U+0021)，而不是 `！` (全形驚嘆號 U+FF01)
