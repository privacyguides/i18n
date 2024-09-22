---
title: 文件協作
icon: material/account-group
description: 大多數線上辦公套件不支援 E2EE，這表示雲端供應商能存取您所做的一切。
cover: document-collaboration.webp
---

<small>防護下列威脅：</small>

- [:material-server-network: 服務提供商](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }

大多數線上辦公套件不支援 E2EE，這表示雲端供應商能存取您所做的一切。 提供者的隱私權政策可能會在法律上保護您的權利，但不會提供技術存取限制。

## 協作平台

### Nextcloud

<div class="admonition recommendation" markdown>

![Nextcloud logo](assets/img/document-collaboration/nextcloud.svg){ align=right }

**Nextcloud** 是一套自由及開放原始碼的用戶端-伺服器軟體，可在您控制的私人伺服器上建立自己的檔案託管服務。

[:octicons-home-16: 首頁](https://nextcloud.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nextcloud.com/privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://nextcloud.com/support){ .card-link title=文檔}
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

我們不建議使用 Nextcloud [E2EE App](https://apps.nextcloud.com/apps/end_to_end_encryption) ，因為它可能會導致資料丟失；目前它仍是高度實驗性，未達穩定品質。 因此，我們不推薦第三方 Nextcloud 提供商。

</div>

### CryptPad

<div class="admonition recommendation" markdown>

![CryptPad logo](assets/img/document-collaboration/cryptpad.svg){ align=right }

**CryptPad** 是流行辦公套件的替代方案，其設計優先考慮私密。 此網路服務上的所有內容都使用端對端加密，且可輕鬆與其他使用者分享。

[:octicons-home-16: 首頁](https://cryptpad.fr){ .md-button .md-button--primary }
[:octicons-eye-16:](https://cryptpad.fr/pad/#/2/pad/view/GcNjAWmK6YDB3EO2IipRZ0fUe89j43Ryqeb4fjkjehE){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://docs.cryptpad.fr){ .card-link title=文檔}
[:octicons-code-16:](https://github.com/xwiki-labs/cryptpad){ .card-link title="原始碼" }
[:octicons-heart-16:](https://opencollective.com/cryptpad){ .card-link title=捐款 }

</details>

</div>

### 標準

**請注意，我們與所推薦專案沒有任何瓜葛。** 除了 [我們的標準準則](about/criteria.md) 外，還有一套明確要求以提出客觀建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

#### 最低合格要求

一般而言，我們將協作平台定義為可完整取代 Google Drive 的成熟套件。

- 它必須是開源的。
- 必須透過 WebDAV 存取檔案，除非因為 E2EE 的關係而無法存取。
- 必須有適用於 Linux、macOS 和 Windows 的同步用戶端。
- 必須支援文件和試算表編輯。
- 必須支援即時文件協作。
- 必須支援將文件匯出為標準文件格式 (例如 ODF)。

#### 最佳案例

最佳案例標準代表了我們希望從這個類別的完美項目應具備的功能。 推薦產品可能沒有此功能，但若有這些功能則會讓排名更為提高。

- 應將檔案儲存在傳統檔案系統中。
- 應支援 TOTP 或 FIDO2 多因素驗證支援，或是能使用 通行金鑰 登入。
