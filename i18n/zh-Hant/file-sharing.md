---
title: "文件共享和同步"
icon: material/share-variant
description: 探索如何在裝置之間、與朋友和家人私下分享檔案，或匿名上線。
cover: file-sharing.webp
---

探索如何在裝置之間、與朋友和家人私下分享檔案，或匿名上線。

## 檔案分享

### Send

<div class="admonition recommendation" markdown>

![Send logo](assets/img/file-sharing-sync/send.svg){ align=right }

**Send** 是分支自 Mozilla 已停止的 Firefox Send服務，它允許您使用鏈接將檔案發送給其他人。 檔案在您的裝置上已加密，因此無法被伺服器讀取，並且它們也可以選擇受密碼保護。 Send 維護者託管 [公共實例](https://send.vis.ee)。 你可以利用其他公開實例，也可以自行託管 Send。

[:octicons-home-16: Homepage](https://send.vis.ee){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/timvisee/send-instances){ .card-link title="Public Instances"}
[:octicons-info-16:](https://github.com/timvisee/send#readme){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/timvisee/send){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/sponsors/timvisee){ .card-link title=Contribute }

</details>

</div>

Send 可利用網頁界面或文字指令 [ffsend](https://github.com/timvisee/ffsend) 來傳送檔案。 如果您熟悉命令行並經常發送檔案，我們建議您使用文字指令的用戶端以避免基於JavaScript 的加密。 您可以利用 `--host` 指令來標記使用特定的伺服器：

```bash
ffsend upload --host https://send.vis.ee/ FILE
```

### OnionShare

<div class="admonition recommendation" markdown>

![OnionShare logo](assets/img/file-sharing-sync/onionshare.svg){ align=right }

**OnionShare** 是一個開源工具，可讓您安全匿名地共享任何大小的檔案。 它的工作原理是啟動可作為 Tor 洋蔥服務訪問的網頁伺服器，具有一個無法猜測的URL ，您可以與收件人共享以下載或發送檔案。

[:octicons-home-16: Homepage](https://onionshare.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://lldan5gahapx5k7iafb3s4ikijc4ni7gx5iywdflkba5y2ezyg6sjgyd.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://docs.onionshare.org){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/onionshare/onionshare){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://onionshare.org/#download)
- [:simple-apple: macOS](https://onionshare.org/#download)
- [:simple-linux: Linux](https://onionshare.org/#download)

</details>

</div>

### 標準

**請注意，我們所推薦專案沒有任何瓜葛。 ** 除了 [標準準則](about/criteria.md)外，我們還發展出一套明確要求以提出客觀建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

- 不得將解密的資料儲存在遠端伺服器上。
- 必須是開源軟體。
- 必須有 Linux、macOS 和 Windows 用戶端；或 Web 網頁界面。

## FreedomBox

<div class="admonition recommendation" markdown>

![FreedomBox logo](assets/img/file-sharing-sync/freedombox.svg){ align=right }

**FreedomBox** 是設計在[單板電腦(SBC)](https://en.wikipedia.org/wiki/Single-board_computer)上執行的作業系統。 其目的是讓設置自主託管的伺服器應用程式變得容易。

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

**Nextcloud** is a suite of free and open-source client-server software for creating your own file hosting services on a private server you control.

[:octicons-home-16: Homepage](https://nextcloud.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nextcloud.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://nextcloud.com/support){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/nextcloud){ .card-link title="Source Code" }
[:octicons-heart-16:](https://nextcloud.com/contribute){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

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

**Syncthing** 是一個開源的點對點連續檔案件同步實用程式。 它可用在本地網路或網際網路的多個設備之間同步檔案。 Syncthing 不使用集中式伺服器；它使用 [Block Exchange Protocol](https://docs.syncthing.net/specs/bep-v1.html#bep-v1) 在裝置之間傳輸資料。 所有資料都使用 TLS 加密。

[:octicons-home-16: Homepage](https://syncthing.net){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.syncthing.net){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/syncthing){ .card-link title="Source Code" }
[:octicons-heart-16:](https://syncthing.net/donations){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.nutomic.syncthingandroid)
- [:fontawesome-brands-windows: Windows](https://syncthing.net/downloads)
- [:simple-apple: macOS](https://syncthing.net/downloads)
- [:simple-linux: Linux](https://syncthing.net/downloads)
- [:simple-freebsd: FreeBSD](https://syncthing.net/downloads)

</details>

</div>

<!-- markdownlint-disable-next-line -->
### 標準

**請注意，我們所推薦專案沒有任何瓜葛。 ** 除了 [標準準則](about/criteria.md)外，我們還發展出一套明確要求以提出客觀建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

#### 最低合格要求

- 必須不需要第三方遠端/雲端伺服器。
- 必須是開源軟體。
- 必須有 Linux、macOS 和 Windows 用戶端；或 Web 網頁界面。

#### 最好的情况

最佳案例標準代表了我們希望從這個類別的完美項目應具備的功能。 推薦產品可能沒有此功能，但若有這些功能則會讓排名更為提高。

- 具有適用於 iOS 和 Android 的移動客戶端，其至少支持文件預覽。
- 支援 iOS 和 Android 照片備份， 或是最好能 支援Android 檔案/資料夾同步。
