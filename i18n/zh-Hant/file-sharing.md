---
title: "檔案共享和同步"
icon: material/share-variant
description: 探索如何在裝置之間、與朋友和家人在私底下分享檔案，甚至是匿名共享。
cover: file-sharing.webp
---

<small>防護下列威脅：</small>

- [:material-server-network: 服務提供商](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

探索如何在裝置之間、與朋友和家人私下分享檔案，或匿名上線。

## 檔案分享

如果您已經使用 [Proton Drive](cloud.md#proton-drive)[^1] 或已訂閱 [Bitwarden](passwords.md#bitwarden) Premium[^2] ，請考慮使用它們各自提供的檔案分享功能，這兩種功能都使用端對端加密。 如果沒有，則這裡列出的獨立選項可確保您打算共享的檔案不會被遠端伺服器讀取。

### Send

<div class="admonition recommendation" markdown>

![Send logo](assets/img/file-sharing-sync/send.svg){ align=right }

**Send** 是分支自 Mozilla 已停止的 Firefox Send服務，它允許您使用鏈接將檔案發送給其他人。 檔案在您的裝置上已加密，因此無法被伺服器讀取，並且它們也可以選擇受密碼保護。 Send 維護者有託管自己的 [公開伺服器](https://send.vis.ee)。 你可以利用其他公開伺服器，也可以自行託管 Send。

[:octicons-home-16: 首頁](https://send.vis.ee){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/timvisee/send-instances){ .card-link title="公開伺服器列表"}
[:octicons-info-16:](https://github.com/timvisee/send#readme){ .card-link title=說明文件}
[:octicons-code-16:](https://github.com/timvisee/send){ .card-link title="原始碼" }
[:octicons-heart-16:](https://github.com/sponsors/timvisee){ .card-link title=捐款 }

</details>

</div>

Send 可利用網頁界面或文字指令 [ffsend](https://github.com/timvisee/ffsend) 來傳送檔案。 如果您熟悉命令行並經常發送檔案，我們建議您使用文字指令的用戶端以避免基於JavaScript 的加密。 您可以利用 `--host` 指令來標記使用特定的伺服器：

```bash
ffsend upload --host https://send.vis.ee/ FILE
```

### OnionShare

<div class="admonition recommendation" markdown>

![OnionShare logo](assets/img/file-sharing-sync/onionshare.svg){ align=right }

**OnionShare** 是一個開放原始碼工具，可讓您安全地 [:material-incognito: 匿名](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple } 分享任何大小的檔案。 它的運作方式是啟動一個網路伺服器，使其以 Tor 洋蔥服務 的方式存取，並提供一個無法猜測的 URL，您可以與收件者分享該 URL 來下載或傳送檔案。

[:octicons-home-16: 首頁](https://onionshare.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://lldan5gahapx5k7iafb3s4ikijc4ni7gx5iywdflkba5y2ezyg6sjgyd.onion){ .card-link title="洋蔥服務" }
[:octicons-info-16:](https://docs.onionshare.org){ .card-link title=說明文件}
[:octicons-code-16:](https://github.com/onionshare/onionshare){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:fontawesome-brands-windows: Windows](https://onionshare.org/#download)
- [:simple-apple: macOS](https://onionshare.org/#download)
- [:simple-linux: Linux](https://onionshare.org/#download)

</details>

</div>

OnionShare 提供透過 [Tor 橋接器](https://docs.onionshare.org/2.6.2/en/tor.html#automatic-censorship-circumvention) 連線的選項，以規避 [:material-close-outline: 審查](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}。

### 標準

**請注意，我們與推薦的任何項目均無關。**除了[我們的通用標準](about/criteria.md)外，我們還制定了一套明確的要求，以便我們能夠提供客觀的建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

- 不得將解密的資料儲存在遠端伺服器上。
- 必須是開源軟體。
- 必須有 Linux、macOS 和 Windows 用戶端；或 Web 網頁界面。

## FreedomBox

<div class="admonition recommendation" markdown>

![FreedomBox logo](assets/img/file-sharing-sync/freedombox.svg){ align=right }

**FreedomBox** 是設計在[單板電腦(SBC)](https://en.wikipedia.org/wiki/Single-board_computer)上執行的作業系統。 其目的是讓設定自主託管的伺服器應用程式變得容易。

[:octicons-home-16: Homepage](https://freedombox.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://wiki.debian.org/FreedomBox/Manual){ .card-link title=Documentation}
[:octicons-code-16:](https://salsa.debian.org/freedombox-team/freedombox){ .card-link title="Source Code" }
[:octicons-heart-16:](https://freedomboxfoundation.org/donate){ .card-link title=Contribute }

</details>

</div>

## 文件同步

### Nextcloud (客戶端-伺服器)

<div class="admonition recommendation" markdown>

![Nextcloud logo](assets/img/document-collaboration/nextcloud.svg){ align=right }

**Nextcloud** 是一套自由和開放原始碼的用戶端及伺服器軟體，可在您控制的私人伺服器上建立自己的檔案託管服務。

[:octicons-home-16: 首頁](https://nextcloud.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nextcloud.com/privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://nextcloud.com/support){ .card-link title=說明文件}
[:octicons-code-16:](https://github.com/nextcloud){ .card-link title="原始碼" }
[:octicons-heart-16:](https://nextcloud.com/contribute){ .card-link title=捐款 }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.nextcloud.client)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1125420102)
- [:simple-github: GitHub](https://github.com/nextcloud/android/releases)
- [:fontawesome-brands-windows: Windows](https://nextcloud.com/install/#install-clients)
- [:simple-apple: macOS](https://nextcloud.com/install/#install-clients)
- [:simple-linux: Linux](https://nextcloud.com/install/#install-clients)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Danger "危險"</p>

我們不建議使用 Nextcloud [E2EE App](https://apps.nextcloud.com/apps/end_to_end_encryption) ，因為它可能會導致資料丟失；目前它仍是高度實驗性，未達穩定品質。

</div>

### Syncthing （ P2P ）

<div class="admonition recommendation" markdown>

![Syncthing logo](assets/img/file-sharing-sync/syncthing.svg){ align=right }

**Syncthing** 是一個開源的點對點連續檔案件同步實用程式。 它可用在區域網路或網際網路的多個設備之間同步檔案。 Syncthing 不使用集中式伺服器；它使用 [Block Exchange Protocol](https://docs.syncthing.net/specs/bep-v1.html#bep-v1) 在裝置之間傳輸資料。 所有資料都使用 TLS 加密。

[:octicons-home-16: 首頁](https://syncthing.net){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.syncthing.net){ .card-link title=說明文件}
[:octicons-code-16:](https://github.com/syncthing){ .card-link title="原始碼" }
[:octicons-heart-16:](https://syncthing.net/donations){ .card-link title=捐款 }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://syncthing.net/downloads)
- [:simple-apple: macOS](https://syncthing.net/downloads)
- [:simple-linux: Linux](https://syncthing.net/downloads)
- [:simple-freebsd: FreeBSD](https://syncthing.net/downloads)

</details>

</div>

### 標準

**請注意，我們與推薦的任何項目均無關。**除了[我們的通用標準](about/criteria.md)外，我們還制定了一套明確的要求，以便我們能夠提供客觀的建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

#### 最低合格要求

- 必須不需要第三方遠端/雲端伺服器。
- 必須是開源軟體。
- 必須有 Linux、macOS 和 Windows 用戶端；或有 網頁版 界面。

#### 最佳情況

最佳情況標準代表我們希望在這個類別的完美項目的應具備的特性。 推薦產品可能沒有此功能，但若有這些功能則會讓排名更為提高。

- 應該有 iOS 和 Android 的行動平台客戶端，至少支援文件預覽。
- 應支援 iOS 和 Android 的相片備份，並可選擇支援 Android 上的檔案/資料夾同步。

[^1]: Proton Drive 可讓您透過生成可分享的公開連結或傳送獨特的連結至指定的電子郵件位址來 [分享檔案或資料夾](https://proton.me/support/drive-shareable-link) 。 公開連結可以使用密碼保護、設定過期時間，需要時也可完全撤銷，而透過電子郵件分享的連結則可以自訂權限，也可以完全撤銷。 根據 Proton Drive 的 [隱私權政策](https://proton.me/drive/privacy-policy) ，檔案內容、檔案和資料夾名稱以及縮圖預覽均經過端對端加密。
[^2]: 如有 [premium](https://bitwarden.com/help/about-bitwarden-plans/#compare-personal-plans) 訂閱，[Bitwarden Send](https://bitwarden.com/products/send) 可讓您以 [端對端加密](https://bitwarden.com/help/send-encryption) 的方式安全地分享檔案和文字。 可以要求收件人在收到並開啟連結後需輸入 [密碼](https://bitwarden.com/help/send-privacy/#send-passwords) 才能存取 Bitwarden Send 還具有 [自動刪除](https://bitwarden.com/help/send-lifespan) 功能。
