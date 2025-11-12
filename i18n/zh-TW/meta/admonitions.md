---
title: 提醒
description: 網站撰稿人建立提醒的指南。
---

**Admonitions** (or "call-outs") are tools that writers can use to include side content in an article without interrupting the document flow.

<div class="admonition example" markdown>
<p class="admonition-title">提醒範例</p>

這是提醒的範例。 雙因素身份驗證 端對端加密 虛擬私人網路 雜湊函數 數位簽章 公鑰加密 防火牆 安全殼層 傳輸層安全 數據泄露 零知識證明 隱私權管理 加密貨幣 身份驗證 多重加密 隱私政策 生物識別技術 數據抹除

</div>

<details class="example" markdown>
<summary>可摺疊式提醒的範例</summary>

這是可摺疊式提醒的範例。 雙因素身份驗證 端對端加密 虛擬私人網路 雜湊函數 數位簽章 公鑰加密 防火牆 安全殼層 傳輸層安全 數據泄露 零知識證明 隱私權管理 加密貨幣 身份驗證 多重加密 隱私政策 生物識別技術 數據抹除

</details>

## 格式

要將提醒加入頁面，您可以使用以下程式碼：

```markdown title="Admonition"
<div class="admonition TYPE" markdown>
<p class="admonition-title">TITLE</p>

內文

</div>
```

```markdown title="Collapsible Admonition"
<details class="TYPE" markdown>
<summary>TITLE</summary>

內文

</details>
```

The `TITLE` must be specified; if you don't want a specific title you can set it to the same text as the `TYPE` (see below) in title case, e.g. `Note`. `內文`必須使用 Markdown 格式。

### 一般類型

用以下其中一個類型替換上面範例的`類型`：

#### `note`

<div class="admonition note" markdown>
<p class="admonition-title">Note</p>

雙因素身份驗證 端對端加密 虛擬私人網路 雜湊函數 數位簽章 公鑰加密 防火牆 安全殼層

</div>

#### `abstract`

<div class="admonition abstract" markdown>
<p class="admonition-title">Abstract</p>

雙因素身份驗證 端對端加密 虛擬私人網路 雜湊函數 數位簽章 公鑰加密 防火牆 安全殼層

</div>

#### `info`

<div class="admonition info" markdown>
<p class="admonition-title">Info</p>

雙因素身份驗證 端對端加密 虛擬私人網路 雜湊函數 數位簽章 公鑰加密 防火牆 安全殼層

</div>

#### `tip`

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

雙因素身份驗證 端對端加密 虛擬私人網路 雜湊函數 數位簽章 公鑰加密 防火牆 安全殼層

</div>

#### `success`

<div class="admonition success" markdown>
<p class="admonition-title">Success</p>

雙因素身份驗證 端對端加密 虛擬私人網路 雜湊函數 數位簽章 公鑰加密 防火牆 安全殼層

</div>

#### `question`

<div class="admonition question" markdown>
<p class="admonition-title">Question</p>

雙因素身份驗證 端對端加密 虛擬私人網路 雜湊函數 數位簽章 公鑰加密 防火牆 安全殼層

</div>

#### `warning`

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

雙因素身份驗證 端對端加密 虛擬私人網路 雜湊函數 數位簽章 公鑰加密 防火牆 安全殼層

</div>

#### `failure`

<div class="admonition failure" markdown>
<p class="admonition-title">Failure</p>

雙因素身份驗證 端對端加密 虛擬私人網路 雜湊函數 數位簽章 公鑰加密 防火牆 安全殼層

</div>

#### `danger`

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

雙因素身份驗證 端對端加密 虛擬私人網路 雜湊函數 數位簽章 公鑰加密 防火牆 安全殼層

</div>

#### `bug`

<div class="admonition bug" markdown>
<p class="admonition-title">Bug</p>

雙因素身份驗證 端對端加密 虛擬私人網路 雜湊函數 數位簽章 公鑰加密 防火牆 安全殼層

</div>

#### `example`

<div class="admonition example" markdown>
<p class="admonition-title">Example</p>

雙因素身份驗證 端對端加密 虛擬私人網路 雜湊函數 數位簽章 公鑰加密 防火牆 安全殼層

</div>

#### `quote`

<div class="admonition quote" markdown>
<p class="admonition-title">Quote</p>

雙因素身份驗證 端對端加密 虛擬私人網路 雜湊函數 數位簽章 公鑰加密 防火牆 安全殼層

</div>

### Special Types

#### `recommendation`

這個格式用來產生推薦卡。 要注意的是它缺少 `<p class="admonition-title">` 元件。

```markdown title="Recommendation Card"
<div class="admonition recommendation" markdown>

![PhotoPrism logo](assets/img/self-hosting/photoprism.svg){ align=right }

**PhotoPrism** is a self-hostable platform for managing photos. It supports album syncing and sharing as well as a variety of other [features](https://photoprism.app/features). It does not include end-to-end encryption, so it's best hosted on a server that you trust and is under your control.

[:octicons-home-16: Homepage](https://photoprism.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://photoprism.app/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://photoprism.app/kb){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/photoprism){ .card-link title="Source Code" }

</div>
```

<div class="result" markdown>

<div class="admonition recommendation" markdown>

![PhotoPrism 圖示](../assets/img/self-hosting/photoprism.svg){ align=right }

**PhotoPrism** is a self-hostable platform for managing photos. It supports album syncing and sharing as well as a variety of other [features](https://photoprism.app/features). It does not include end-to-end encryption, so it's best hosted on a server that you trust and is under your control.

[:octicons-home-16: Homepage](https://photoprism.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://photoprism.app/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://photoprism.app/kb){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/photoprism){ .card-link title="Source Code" }

</div>

</div>

#### `downloads`

This is a special type of collapsible admonition which is used to generate sections containing download links. 只與推薦卡一起使用，如上面的範例。

```markdown title="Downloads Section"
<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/android-mail/releases)
- [:fontawesome-brands-windows: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: Web](https://mail.proton.me)

</details>
```

<div class="result" markdown>

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/android-mail/releases)
- [:fontawesome-brands-windows: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: Web](https://mail.proton.me)

</details>

</div>

## 舊格式

Throughout the site, you may see some admonitions formatted like the following examples:

```markdown title="Admonition"
!!! note

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.
```

<div class="result" markdown>

<div class="admonition note" markdown>
<p class="admonition-title">Note</p>

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
massa, nec semper lorem quam in massa.

</div>

</div>

```markdown title="Collapsible Admonition"
??? example "Custom Title"

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.
```

<div class="result" markdown>

<details class="example" markdown>
<summary>Custom Title</summary>

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
massa, nec semper lorem quam in massa.

</details>

</div>

**This format is no longer used going forward** because it is incompatible with newer versions of our translation software at Crowdin. When adding a new page to the site, only the newer, HTML-based format should be used.

舊格式的提醒內容暫時不需要急著轉換成新格式。 Pages currently using this formatting should continue to work, but we will be updating them to use the newer, HTML-based format above over time as we continue to update the site.
