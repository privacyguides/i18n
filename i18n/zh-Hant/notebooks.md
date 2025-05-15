---
title: "記事本"
icon: material/notebook-edit-outline
description: These encrypted note-taking apps let you keep track of your notes without giving them to a third party.
cover: notebooks.webp
---

<small>防護下列威脅：</small>

- [:material-server-network: 服務提供商](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

隨時紀錄您的筆記和日記，不需提供給第三方。

If you are currently using an application like Evernote, Google Keep, or Microsoft OneNote, we suggest you pick an alternative here that supports end-to-end encryption.

## 雲端型

### Standard Notes

<div class="admonition recommendation" markdown>

![Standard Notes logo](assets/img/notebooks/standard-notes.svg){ align=right }

**Standard Notes** is a simple and private notes app that features cross-platform sync for seamless use. 它在每個平臺上都採納 E2EE ，並且其電腦版具有強大的主題和自訂編輯器功能。

Standard Notes has also undergone multiple [independent audits](https://standardnotes.com/help/2/has-standard-notes-completed-a-third-party-security-audit).

[:octicons-home-16: Homepage](https://standardnotes.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://standardnotes.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://standardnotes.com/help){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/standardnotes){ .card-link title="Source Code" }
[:octicons-heart-16:](https://standardnotes.com/donate){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.standardnotes)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1285392450)
- [:simple-github: GitHub](https://github.com/standardnotes/app/releases)
- [:fontawesome-brands-windows: Windows](https://standardnotes.com)
- [:simple-apple: macOS](https://standardnotes.com)
- [:simple-linux: Linux](https://standardnotes.com)
- [:octicons-browser-16: Web](https://app.standardnotes.com)

</details>

</div>

Standard Notes 已於 2024 年 4 月 10 日 [加入 Proton AG](https://standardnotes.com/blog/joining-forces-with-proton)。

### Notesnook

<div class="admonition recommendation" markdown>

![Notesnook logo](assets/img/notebooks/notesnook.svg){ align=right }

**Notesnook** is a free (as in speech), open-source, and easy-to-use E2EE note-taking app focused on user privacy.

It features sync functionality that allows you to access your notes on multiple platforms. You can easily import your notes from Evernote, OneNote, and other apps using their [official importer](https://importer.notesnook.com).

[:octicons-home-16: Homepage](https://notesnook.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://notesnook.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://help.notesnook.com){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/streetwriters/notesnook){ .card-link title="Source Code" }
[:octicons-heart-16:](https://opencollective.com/notesnook){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.streetwriters.notesnook)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1544027013)
- [:simple-github: GitHub](https://github.com/streetwriters/notesnook/releases)
- [:fontawesome-brands-windows: Windows](https://notesnook.com/downloads)
- [:simple-apple: macOS](https://notesnook.com/downloads)
- [:simple-linux: Linux](https://notesnook.com/downloads)
- [:simple-flathub: Flathub](https://flathub.org/apps/com.notesnook.Notesnook)
- [:simple-firefoxbrowser: Firefox](https://notesnook.com/notesnook-web-clipper)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/kljhpemdlcnjohmfmkogahelkcidieaj)
- [:octicons-browser-16: Web](https://app.notesnook.com)

</details>

</div>

### Joplin

<div class="admonition recommendation" markdown>

![Joplin logo](assets/img/notebooks/joplin.svg){ align=right }

**Joplin** is a free, open-source, and fully-featured E2EE note-taking and to-do application which can handle numerous Markdown notes organized into notebooks and tags.

It can sync through Nextcloud, Dropbox, and more. 它也可以輕鬆的從 Evernote 和純文本筆記導入。

[:octicons-home-16: Homepage](https://joplinapp.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://joplinapp.org/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://joplinapp.org/help){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/laurent22/joplin){ .card-link title="Source Code" }
[:octicons-heart-16:](https://joplinapp.org/donate){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.cozic.joplin)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1315599797)
- [:simple-github: GitHub](https://github.com/laurent22/joplin-android/releases)
- [:fontawesome-brands-windows: Windows](https://joplinapp.org/#desktop-applications)
- [:simple-apple: macOS](https://joplinapp.org/#desktop-applications)
- [:simple-linux: Linux](https://joplinapp.org/#desktop-applications)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/joplin-web-clipper)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/alofnhikmmkdbbbgpnglcpdollgjjfek)

</details>

</div>

Joplin [does not support](https://github.com/laurent22/joplin/issues/289) password/PIN protection for the application itself or individual notes and notebooks. 但是您的資料在傳輸與同步過程中仍會使用主金鑰加密。 Since January 2023, Joplin [supports biometrics app lock](https://github.com/laurent22/joplin/commit/f10d9f75b055d84416053fab7e35438f598753e9) for Android and iOS.

### Cryptee

<div class="admonition recommendation" markdown>

![Cryptee logo](./assets/img/notebooks/cryptee.svg#only-light){ align=right }
![Cryptee logo](./assets/img/notebooks/cryptee-dark.svg#only-dark){ align=right }

**Cryptee** 是一個開源的，基於網頁的 E2EE 文件編輯器和照片儲存應用程式。

Cryptee offers 100 MB of storage for free, with paid options if you need more. Sign-up doesn't require an e-mail or other personally identifiable information.

[:octicons-home-16: Homepage](https://crypt.ee){ .md-button .md-button--primary }
[:octicons-eye-16:](https://crypt.ee/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://crypt.ee/help){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/cryptee){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:octicons-browser-16: Web](https://crypt.ee/download)

</details>

</div>

Cryptee is a PWA, which means that it works seamlessly across all modern devices without requiring native apps for each respective platform.

## 本地端的記事簿

### Org-mode

<div class="admonition recommendation" markdown>

![Org-mode logo](assets/img/notebooks/org-mode.svg){ align=right }

**Org-mode** 是GNU Emacs的 [主要模式](https://gnu.org/software/emacs/manual/html_node/elisp/Major-Modes.html)。 Org-mode 用於記錄筆記，維護待辦事項列表，規劃項目以及使用快速有效的純文字系統撰寫文件。 File synchronization is possible with tools like [Syncthing](file-sharing.md#syncthing-p2p).

[:octicons-home-16: Homepage](https://orgmode.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://orgmode.org/manuals.html){ .card-link title="Documentation" }
[:octicons-code-16:](https://git.savannah.gnu.org/cgit/emacs/org-mode.git){ .card-link title="Source Code" }
[:octicons-heart-16:](https://liberapay.com/bzg){ .card-link title="Contribute" }

</details>

</div>

## 標準

**請注意，我們與推薦的任何項目均無關。**除了[我們的通用標準](about/criteria.md)外，我們還制定了一套明確的要求，以便我們能夠提供客觀的建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

### 最低合格要求

- 客戶端應是開源的。
- 任何雲端同步都必須是 E2EE。
- 必須支援將文件匯出為標準格式。

### 最佳實踐

- 本地備份/同步功能應支援加密。
- 基於雲的平臺應支援文件共享。
