---
meta_title: "最好的私人即時通訊軟體 - Privacy Guides"
title: 即時通訊軟體
icon: material/chat-processing
description: 像 Signal 和 SimpleX 之類的加密通訊工具可讓您的敏感通訊不被窺探。
cover: real-time-communication.webp
---

<small>防護下列威脅：</small>

- [:material-bug-outline: 被動攻擊](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: 服務提供商](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}
- [:material-eye-outline: 大規模監控](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-account-cash: 監控資本主義](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

這些加密**即時通訊**的建議對於保護您的敏感通訊非常有用。 這些即時通訊工具呈現為多種[通訊網路類型](advanced/communication-network-types.md)。

[:material-movie-open-play-outline: Video: It's time to stop using SMS](https://www.privacyguides.org/videos/2025/01/24/its-time-to-stop-using-sms-heres-why ""){.md-button}

## Signal

<div class="admonition recommendation" markdown>

![Signal logo](assets/img/messengers/signal.svg){ align=right }

**Signal** 是由Signal Messenger LLC開發的行動應用程式。 該應用程式提供即時通訊與通話服務，並採用 Signal 協定進行加密保護。此協定具備極高安全性，支援前向保密性[^1]與遭入侵後的安全性保障[^2]。

[:octicons-home-16: 首頁](https://signal.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://signal.org/legal/#privacy-policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://support.signal.org){ .card-link title="文件" }
[:octicons-code-16:](https://github.com/signalapp){ .card-link title="原始碼" }
[:octicons-heart-16:](https://signal.org/donate){ .card-link title="貢獻" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.thoughtcrime.securesms)
- [:simple-appstore: App Store](https://apps.apple.com/app/id874139669)
- [:simple-github: GitHub](https://github.com/signalapp/Signal-Android/releases)
- [:simple-android: Android](https://signal.org/android/apk)
- [:fontawesome-brands-windows: Windows](https://signal.org/download/windows)
- [:simple-apple: macOS](https://signal.org/download/macos)
- [:simple-linux: Linux](https://signal.org/download/linux)

</details>

</div>

Signal 註冊時需要您的電話號碼，但您應建立使用者名稱以隱藏您的電話號碼，使其不被聯絡人看見：

1. 在 Signal 中，打開應用程式的設定並點擊上方的帳戶個人資料。
2. 點選**使用者名稱**，然後在「設定您的 Signal 使用者名稱」畫面上選擇**繼續**。
3. 輸入一個使用者名稱 您的使用者名稱將一律與一組獨特的數字配對，以確保使用者名稱的唯一性，並防止他人猜測。 例如，如果您輸入「John」，您的使用者名稱可能會變成 `@john.35`。 根據預設設定，當您建立使用者名稱時，只有 2 位數字會與使用者名稱配對，但您可以增加更多位數，直到達到使用者名稱的長度限制 (32 個字元)。
4. 返回系統應用程式設定頁面並選擇**隱私權**。
5. 選取**電話號碼**。
6. 將**誰可以看見我的號碼**設定變更為**沒有人**。
7. （選擇性）若想防止知道您手機號碼的人找到您的 Signal 帳號或使用者名稱，也可以將**誰可以找到我的號碼**設定變更為**沒有人**

我們針對設定與強化您的 Signal 安裝提供以下額外建議：

[Signal 組態與安全性強化 :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening)

聯絡人清單會使用您的 Signal PIN 加密，而伺服器無法存取。 個人資料也會加密，僅與您聊天的聯絡人分享。

Signal 支援[私人群組](https://signal.org/blog/signal-private-group-system)，伺服器不會紀錄您群組的成員、標題、大頭照或屬性。 啟用[密封寄件者](https://signal.org/blog/sealed-sender)時，Signal 的中介資料最少。 寄件者位址與訊息內文一起加密，伺服器僅能看到收件者位址。 密封寄件者功能僅會對您聯絡人清單中的成員啟用，但也可以對所有收件者啟用以防止垃圾訊息變多的風險。

協定於2016年經過獨立[稽核](https://eprint.iacr.org/2016/1013.pdf)。 Signal 協定的規範可以在他們的[文件](https://signal.org/docs)中找到。

### Molly (Android)

若您使用 Android 且您的威脅模型需要防範[:material-target-account: 針對性攻擊](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}，您可以考慮使用此替代應用程式來存取 Signal 網路，此應用程式在安全性與可用性方面有許多改進。

<div class="admonition recommendation" markdown>

![Molly logo](assets/img/messengers/molly.svg){ align=right }

**Molly** 是 Android 的替代 Signal 用戶端，可讓您使用密碼加密本機資料庫、安全地刪除未使用的 RAM 資料、透過 Tor 路由連線；除此之外，還有 [許多](https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening#privacy-and-security-features)。 它還改善了可用性，包括排程備份、自動鎖定，以及使用 Android 手機作為連結裝置，而非 Signal 帳號的主要裝置。

[:octicons-home-16: 首頁](https://molly.im){ .md-button .md-button--primary }
[:octicons-eye-16:](https://signal.org/legal/#privacy-policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://github.com/mollyim/mollyim-android/wiki){ .card-link title="說明文件" }
[:octicons-code-16:](https://github.com/mollyim/mollyim-android){ .card-link title="原始碼" }
[:octicons-heart-16:](https://opencollective.com/mollyim){ .card-link title="捐款" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-fdroid: F-Droid](https://molly.im/fdroid)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/im.molly.app)
- [:simple-github: GitHub](https://github.com/mollyim/mollyim-android/releases)

</details>

</div>

Molly 每兩週更新一次，以包含 Signal 的最新功能與錯誤修正。 安全問題是例外，這類問題會盡快進行修補。 話雖如此，您應當留意相較於上游系統可能存在些微延遲，這可能影響諸如[從 Signal 遷移至 Molly](https://github.com/mollyim/mollyim-android/wiki/Migrating-From-Signal#migrating-from-signal) 等操作。

請注意，使用 Molly 意味著您需要多方信任，您現在必須信任 Signal 團隊*以及* Molly 團隊，以確保能安全且及時地接收更新。

**Molly-FOSS** 是 Molly 的改版，移除了如 Google 服務等專有程式碼（此類服務同時被 Signal 與 Molly 所採用），但代價是犧牲部分功能（例如透過 Google Play 服務實現的省電推播通知）。 無論使用哪個版本的 Molly，您皆可透過 [UnifiedPush](https://unifiedpush.org) 設定無需 Google Play 服務的推播通知。 使用此通知傳遞方式需存取 [MollySocket](https://github.com/mollyim/mollysocket) 伺服器，但您可選擇使用公開的 MollySocket 站台。[^3]

兩個版本的 Molly 皆提供相同的安全性強化措施，並支援[可重現的建置](https://github.com/mollyim/mollyim-android/tree/main/reproducible-builds)，這意味著可確認編譯後的 APK 檔案與原始碼完全一致。

## SimpleX 聊天

<div class="admonition recommendation" markdown>

![SimpleX 聊天](assets/img/messengers/simplex.svg){ align=right }

**SimpleX 聊天**是一款即時通訊軟體，其運作不依賴任何唯一識別碼，例如電話號碼或使用者名稱。 其分佈式網路使 SimpleX Chat 成為對抗 [:material-close-outline: 審查](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray } 的有效工具。

[:octicons-home-16: 首頁](https://simplex.chat){ .md-button .md-button--primary }
[:octicons-eye-16:](https://simplex.chat/privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://simplex.chat/docs/simplex.html){ .card-link title="說明文件" }
[:octicons-code-16:](https://github.com/simplex-chat){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=chat.simplex.app)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1605771084)
- [:simple-github: GitHub](https://github.com/simplex-chat/simplex-chat/releases)
- [:fontawesome-brands-windows: Windows](https://simplex.chat/downloads/#desktop-app)
- [:simple-apple: macOS](https://simplex.chat/downloads/#desktop-app)
- [:simple-linux: Linux](https://simplex.chat/downloads/#desktop-app)
- [:simple-flathub: Flathub](https://flathub.org/en/apps/chat.simplex.simplex)

</details>

</div>

SimpleX 聊天提供直接訊息傳遞、群組聊天及端對端加密通話功能，其安全性由 [SimpleX 訊息傳輸協定](https://github.com/simplex-chat/simplexmq/blob/stable/protocol/simplex-messaging.md)保障，該協定採用具量子抗性之雙重棘輪加密技術。 此外，SimpleX 聊天透過採用單向的[「simplex 佇列」](https://github.com/simplex-chat/simplexmq/blob/stable/protocol/simplex-messaging.md#simplex-queue)傳遞訊息，提供中介資料保護功能。

要參與 SimpleX 聊天上的對話，您必須掃描 QR code 或按一下邀請連結。 這使您能夠透過其他管道驗證聯絡人，從而防範網路供應商發動的中間人攻擊。 您的資料可匯出並匯入至其他裝置，因為並無中央伺服器進行備份。

您可以在應用程式的儲存庫中查閱 SimpleX 聊天實作的完整隱私與安全[功能清單](https://github.com/simplex-chat/simplex-chat#privacy-and-security-technical-details-and-limitations)。

SimpleX Chat 於[2024年7月](https://simplex.chat/blog/20241014-simplex-network-v6-1-security-review-better-calls-user-experience.html#simplex-cryptographic-design-review-by-trail-of-bits)及[2022年10月](https://simplex.chat/blog/20221108-simplex-chat-v4.2-security-audit-new-website)進行獨立稽核。

## Briar

<div class="admonition recommendation" markdown>

![Briar 標誌](assets/img/messengers/briar.svg){ align=right }

**Briar** 是一款加密即時通訊軟體，透過 [Tor 網路](alternative-networks.md#tor)與其他客戶端建立連線，使其成為有效繞過[:material-close-outline: 審查制度](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }。 Briar 還可以使用鄰近 Wi-Fi 或藍牙連接。 當無法使用網際網路時， Briar 的本地網格（mesh）模式可能很有用。

[:octicons-home-16: 首頁](https://briarproject.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://briarproject.org/privacy-policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://code.briarproject.org/briar/briar/-/wikis/home){ .card-link title="文件" }
[:octicons-code-16:](https://code.briarproject.org/briar/briar){ .card-link title="原始碼" }
[:octicons-heart-16:](https://code.briarproject.org/briar/briar#donate){ .card-link title="貢獻" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.briarproject.briar.android)
- [:fontawesome-brands-windows: Windows](https://briarproject.org/download-briar-desktop)
- [:simple-linux: Linux](https://briarproject.org/download-briar-desktop)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.briarproject.Briar)

</details>

</div>

要在 Briar 上新增聯絡人，雙方必須先互相新增對方。 您可以交換 `briar://` 連結或掃描聯絡人的 QR code（如果他們在附近的話）。

Briar 已經完全[公佈規格](https://code.briarproject.org/briar/briar-spec)。 Briar 透過使用 Bramble [握手](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BHP.md)及[傳輸](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BTP.md)協定實作前向保密[^1]。

客戶端軟體曾被獨立[稽核](https://briarproject.org/news/2017-beta-released-security-audit)，而使用 Tor 網路的匿名路由協定也接受了稽核。

## 標準

**請注意，我們與推薦的任何項目均無關。**除了[我們的通用標準](about/criteria.md)外，我們還制定了一套明確的要求，以便我們能夠提供客觀的建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

### 最低合格要求

- 必須要有開放原始碼。
- 不得要求使用者與聯絡人分享個人資訊（特別是電話號碼或電子郵件）。
- 必須在私人訊息預設使用端到端加密。
- 必須對所有訊息都支援端到端加密。
- 必須支援前向保密[^1]
- 必須由信譽良好的獨立第三方進行公開審核。

### 最佳情況

最佳情況標準代表我們希望在這個類別的完美項目的應具備的特性。 推薦產品可能沒有此功能，但若有這些功能則會讓排名更為提高。

- 應支援未來保密（入侵後安全）[^2]
- 應有開放原始碼伺服器。
- 應使用去中心化網路，例如[聯邦式或 P2P](advanced/communication-network-types.md)。
- 預設情況下，所有訊息皆應使用端到端加密。
- 應支援 Linux、macOS、Windows、Android 與 iOS。
[^3]: 您可參考這份德文版逐步教學，了解如何將 UnifiedPush 設定為 Molly 的通知提供者： [https://kuketz-blog.de/messenger-wechsel-von-signal-zu-molly-unifiedpush-mollysocket-ntfy](https://kuketz-blog.de/messenger-wechsel-von-signal-zu-molly-unifiedpush-mollysocket-ntfy)。

[^1]: [前向保密](https://en.wikipedia.org/wiki/Forward_secrecy)是指頻繁輪替金鑰，如此一來即使目前的加密金鑰遭洩露，亦不會同時暴露**過往**的訊息。
[^2]: 未來保密性（或[入侵後安全性](https://eprint.iacr.org/2016/221.pdf)）是一項機制，即使攻擊者已取得私鑰，仍無法解密**未來**的訊息，除非該攻擊者未來能同時取得更多工作階段金鑰。 這實際上迫使攻擊者必須攔截所有通訊方之間的通訊，因為只要發生未被攔截的金鑰交換，攻擊者便會立即喪失存取權。
