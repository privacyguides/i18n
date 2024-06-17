---
title: 提醒
---

**提醒**（或「補充說明」）是寫作者可以在文章中加入額外內容的選項，而不會影響文章的整體流暢度。

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

ENCLOSED TEXT

</div>
```

```markdown title="Collapsible Admonition"
<details class="TYPE" markdown>
<summary>TITLE</summary>

ENCLOSED TEXT

</details>
```

The `TITLE` must be specified, if you don't want a specific title you can set it to the same text as the `TYPE` (see below) in title case, e.g. `Note`. The `ENCLOSED TEXT` should be Markdown formatted.

### Regular types

Replace `TYPE` in the examples above with one of the following:

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
<p class="admonition-title">資訊</p>

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
<p class="admonition-title">警告</p>

雙因素身份驗證 端對端加密 虛擬私人網路 雜湊函數 數位簽章 公鑰加密 防火牆 安全殼層

</div>

#### `failure`

<div class="admonition failure" markdown>
<p class="admonition-title">Failure</p>

雙因素身份驗證 端對端加密 虛擬私人網路 雜湊函數 數位簽章 公鑰加密 防火牆 安全殼層

</div>

#### `danger`

<div class="admonition danger" markdown>
<p class="admonition-title">Danger "危險"</p>

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

This format is used to generate recommendation cards. Notably it is missing the `<p class="admonition-title">` element.

```markdown title="Recommendation Card"
<div class="admonition recommendation" markdown>

![PhotoPrism logo](assets/img/photo-management/photoprism.svg){ align=right }

**PhotoPrism** is a self-hostable platform for managing photos. It supports album syncing and sharing as well as a variety of other [features](https://photoprism.app/features). It does not include E2EE, so it's best hosted on a server that you trust and is under your control.

[:octicons-home-16: Homepage](https://photoprism.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://photoprism.app/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://photoprism.app/kb){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/photoprism){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/photoprism)

</details>

</div>
```

<div class="result" markdown>

<div class="admonition recommendation" markdown>

![PhotoPrism logo](../assets/img/photo-management/photoprism.svg){ align=right }

**PhotoPrism** 是一個管理照片的自架平台。 支援相簿同步和共享以及各種其他[功能](https://photoprism.app/features)。 它不包括 E2EE，因此最好將其託管在信任且能控制的伺服器上。

[:octicons-home-16: Homepage](https://photoprism.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://photoprism.app/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://photoprism.app/kb){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/photoprism){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-github: GitHub](https://github.com/photoprism)

</details>

</div>

</div>

#### `downloads`

This is a special type of collapsible admonition, used to generate the download links section. It is only used within recommendation cards, as shown in the example above.

```markdown title="Downloads Section"
<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/proton-mail-android/releases)
- [:simple-windows11: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: Web](https://mail.proton.me)

</details>
```

<div class="result" markdown>

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id979659905)
- [:simple-github: GitHub](https://github.com/ProtonMail/proton-mail-android/releases)
- [:simple-windows11: Windows](https://proton.me/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/mail/bridge#download)
- [:octicons-browser-16: Web](https://mail.proton.me)

</details>

</div>

## Old Format

Throughout the site, you may see some admonitions formatted similarly to these examples:

```markdown title="Admonition"
!!! note

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.
```

<div class="result" markdown>

<div class="admonition note" markdown>
<p class="admonition-title">Note</p>

雙因素身份驗證 端對端加密 虛擬私人網路 雜湊函數 數位簽章 公鑰加密 防火牆 安全殼層 Nulla et euismod
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

雙因素身份驗證 端對端加密 虛擬私人網路 雜湊函數 數位簽章 公鑰加密 防火牆 安全殼層 Nulla et euismod
nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
massa, nec semper lorem quam in massa.

</details>

</div>

**This format is no longer used going forward,** because it is incompatible with newer versions of our translation software at Crowdin. When adding a new page to the site, only the newer HTML-based format should be used.

There is no rush to convert admonitions with the old format to the new format. Pages currently using this formatting should continue to work, but we will be updating them to use the newer HTML-based format above over time as we continue to update the site.
