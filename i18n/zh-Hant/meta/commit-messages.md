---
title: 提交訊息
description: 網站貢獻者在提出網站變更請求時，關於如何給出有用的 Git 提交訊息指南。
---

對於我們的提交訊息，我們遵循 [Conventional Commits](https://conventionalcommits.org) 所提供的樣式。 並非所有這些建議都適合 Privacy Guides，因此我們使用的主要建議有：

## 更新現有文本

此範例可用於網站中已存在的項目，但包括描述的小更新。

```text
update: Add mention of security audit (#0000)
```

## 新增或移除建議/頁面

此範例用於增加或移除項目。 您可以在下面的提交段落中詳細說明移除的原因。 請注意額外的 `！` ，以引起對重大變更的注意。

```text
update!: Remove foobar (#0000)

Foobar was removed due to it having numerious security issues and being unmaintained.
```

實際上，您可以在此頁面介紹的 _任一_ 變更種類中加入 `!`，以表示特別大的變更；但在通常情況下，這是最適合添加 `!` 的種類。

## 新功能/增強

對於網站的新功能或增強功能，例如在 GitHub 上有 `enhancements` 標籤的東西，可能適合以此來標示：

```text
feat: Add blah blah (#0000)

This change adds the forum topics to the main page
```

## 細節變動

**不影響文章意義** 的小變更，例如更正錯字、修正文法、變更格式/空格、CSS 更新等。

```text
style: Typo correction in VPN overview
```

## 開發相關的類型

這些提交類型通常用於一般閱聽人看不到的變更。

我們使用 `fix:` 來修正與網站相關的錯誤。 這些東西通常會在 GitHub 上貼上 `bug` 標籤。

```text
fix: Remove broken Invidious embeds (#0000)
```

我們使用 `docs:` 來表示本網站開發者文件的變更，包括（但不限於）README 檔案、 `/docs/about` 與 `/docs/meta` 中的大多數頁面：

```text
docs: Update Git commit message guidelines (#0000)
```

我們使用 `build:` 來處理與構建程序相關的提交，主要是依賴項更新。

```text
build: Bump modules/mkdocs-material from 463e535 to 621a5b8
```

我們使用 `ci:` 來處理與 GitHub Actions、DevContainers 或其他自動構建平台相關的提交。

```text
ci: Update Netlify config (#0000)
```

我們使用 `refactor:` 來處理既沒有修正錯誤也沒有新增功能的變更，例如重新排列檔案、導覽順序等。

```text
refactor: Move docs/assets to theme/assets
```
