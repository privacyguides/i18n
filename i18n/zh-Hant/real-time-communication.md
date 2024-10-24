---
meta_title: "最好的私人即時通訊軟體 - Privacy Guides"
title: "即時通訊軟體"
icon: material/chat-processing
description: 像 Signal 和 SimpleX 之類的加密通訊工具可讓您的敏感通訊不被窺探。
cover: real-time-communication.webp
---

<small>防護下列威脅：</small>

- [:material-bug-outline: 被動攻擊](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: 服務提供商](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}
- [:material-eye-outline: 大規模監控](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-account-cash: 監控資本主義](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

以上是我們對加密**即時通訊軟體**的建議。

[通訊網絡 :material-arrow-right-drop-circle:](./advanced/communication-network-types.md)

## 加密傳訊軟體

這些軟體非常適合保護您的敏感通訊。

### Signal

<div class="admonition recommendation" markdown>

![Signal logo](assets/img/messengers/signal.svg){ align=right }

**Signal** 是由Signal Messenger LLC開發的行動應用程式。 這款應用程式透過 Signal 協議來保護即時訊息和通話，它是極其安全的加密協議，支援前向保密[^1] 和洩露後安全性。[^2]

[:octicons-home-16: 首頁](https://signal.org/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://signal.org/legal/#privacy-policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://support.signal.org/hc/en-us){ .card-link title=文檔}
[:octicons-code-16:](https://github.com/signalapp){ .card-link title="原始碼" }
[:octicons-heart-16:](https://signal.org/donate/){ .card-link title=捐款 }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.thoughtcrime.securesms)
- [:simple-appstore: App Store](https://apps.apple.com/app/id874139669)
- [:simple-android: Android](https://signal.org/android/apk)
- [:fontawesome-brands-windows: Windows](https://signal.org/download/windows)
- [:simple-apple: macOS](https://signal.org/download/macos)
- [:simple-linux: Linux](https://signal.org/download/linux)

</details>

</div>

Signal 需要手機號碼才能註冊，但是您應該建立用戶名，以隱藏手機號碼：

1. 在 Signal 中，打開應用程式的設定並點擊上方的帳戶個人資料。
2. 點選**使用者名稱**，然後在「設定您的 Signal 使用者名稱」畫面上選擇**繼續**。
3. 輸入一個使用者名稱 此用戶名將一直與一組獨特數字配對，以保持用戶名的唯一性防止人們猜測它，例如，如果輸入“John”，您的用戶名最終可能會是`@john.35`。 根據預設設定，當您建立使用者名稱時，只有 2 位數字會與使用者名稱配對，但您可以增加更多位數，直到達到使用者名稱的長度限制 (32 個字元)。
4. 返回系統應用程式設定頁面並選擇**隱私權**。
5. 選擇**手機號碼**
6. 將 **誰可以看到我的號碼** 設置為：**沒有人**

若想防止已知您手機號碼的人找到您的 Signal 帳號或用戶名稱，也可以選擇把 **誰可以透過電話號碼找到我** 設置為 **沒有人** 。

連絡人清單會使用您的 Signal PIN 加密，而伺服器無法存取。 個人帳號也會加密，並僅與您聊天的聯絡人分享。 Signal 支援[私密 群組](https://signal.org/blog/signal-private-group-system)，伺服器不會記錄該群組成員資格、群組標題、群組頭像，或群組屬性。 當啓用 [Sealed Sender](https://signal.org/blog/sealed-sender) 時， Signal具有最小元數據。 發件人地址與訊息內文一起加密，伺服器只可見到收件人地址。 Sealed Sender 功能僅適用於聯絡人清單的成員，但在收訊時也可啟用以防止接收垃圾郵件增加的風險。

其協議在2016年獨立進行了 [審計](https://eprint.iacr.org/2016/1013.pdf) 。 Signal 協議的規範可以在他們的 [文檔](https://signal.org/docs)中找到。

我們有一些關於配置和硬化 Signal 安裝的額外提示：

[Signal 配置和硬化 :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening)

#### Molly (Android)

如果您使用 Android，且您的威脅模式需要防範 [:material-target-account: 針對性攻擊](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red} ，您可以考慮使用此替代應用程式存取 Signal 網路，此應用程式在安全性和可用性方面有許多改進。

<div class="admonition recommendation" markdown>

![Molly logo](assets/img/messengers/molly.svg){ align=right }

**Molly** 是 Android 的替代 Signal 用戶端，可讓您使用密碼加密本機資料庫、安全地刪除未使用的 RAM 資料、透過 Tor 路由連線；除此之外，還有 [許多](https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening#privacy-and-security-features)。 它還改善了可用性，包括排程備份、自動鎖定，以及使用 Android 手機作為連結裝置，而非 Signal 帳戶的主要裝置。

[:octicons-home-16: 首頁](https://molly.im){ .md-button .md-button--primary }
[:octicons-eye-16:](https://signal.org/legal/#privacy-policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://github.com/mollyim/mollyim-android/wiki){ .card-link title="文檔"}
[:octicons-code-16:](https://github.com/mollyim/mollyim-android){ .card-link title="原始碼" }
[:octicons-heart-16:](https://opencollective.com/mollyim){ .card-link title="捐款" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-fdroid: F-Droid](https://molly.im/fdroid)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/im.molly.app)
- [:simple-github: GitHub](https://github.com/mollyim/mollyim-android/releases)

</details>

</div>

Molly 每兩週更新一次，以包含 Signal 的最新功能和錯誤修正。 安全問題是例外，開發團隊會儘快修補安全問題。 儘管如此，您應該注意的是，與上游相比，可能會有少許延遲，這可能會影響 [從 Signal 遷移到 Molly](https://github.com/mollyim/mollyim-android/wiki/Migrating-From-Signal#migrating-from-signal) 等動作。

請注意，您使用 Molly 是對多方的信任，因為您現在需要信任 Signal 團隊 *和* Molly 團隊 ，以提供安全且及時的更新。

Molly 有一個稱為 **Molly-FOSS** 的版本，它移除了 Signal 和 Molly 所使用的 Google 服務等專有程式碼，但卻犧牲了一些功能，例如透過 Google Play 服務來推送通知（可節省電池用量）。

還有一個版本叫做 [**Molly-UP**](https://github.com/mollyim/mollyim-android#unifiedpush) 的版本，它以 Molly-FOSS 為基礎，並增加了使用 [UnifiedPush](https://unifiedpush.org/) 來推送通知的支援，這是一個能代替 Google Play 服務推送通知的開放原始碼專案，但它需要執行一個名為 [Mollysocket](https://github.com/mollyim/mollysocket) 的獨立程式才能運作。 Mollysocket 可以自行架設在獨立的電腦或伺服器（VPS），或者使用公開 Mollysocket 實例（[逐步教學，德文](https://www.kuketz-blog.de/messenger-wechsel-von-signal-zu-molly-unifiedpush-mollysocket-ntfy/)）。

三個版本的 Molly 都提供相同的安全性改進。

Molly 和 Molly-FOSS 支援 [可重現構建](https://github.com/mollyim/mollyim-android/tree/main/reproducible-builds) ，這表示可以確認編譯後的 APK 與原始碼相符。

### SimpleX Chat

<div class="admonition recommendation" markdown>

![Simplex logo](assets/img/messengers/simplex.svg){ align=right }

**SimpleX** Chat 是一款不依賴任何獨特識別碼（例如：電話號碼、使用者名稱）的即時通訊工具。 其分佈式網路使 SimpleX Chat 成為對抗 [:material-close-outline: 審查](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray } 的有效工具。 SimpleX Chat 使用者可以掃描二維碼或點擊邀請連結以參與羣組對話。

[:octicons-home-16: 首頁](https://simplex.chat){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/simplex-chat/simplex-chat/blob/stable/PRIVACY.md){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://github.com/simplex-chat/simplex-chat/tree/stable/docs){ .card-link title=文檔}
[:octicons-code-16:](https://github.com/simplex-chat){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=chat.simplex.app)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1605771084)
- [:simple-github: GitHub](https://github.com/simplex-chat/simplex-chat/releases)
- [:fontawesome-brands-windows: Windows](https://simplex.chat/downloads/#desktop-app)
- [:simple-apple: macOS](https://simplex.chat/downloads/#desktop-app)
- [:simple-linux: Linux](https://simplex.chat/downloads/#desktop-app)

</details>

</div>

SimpleX Chat 於2022年10月接受 Trail of Bits [審計](https://simplex.chat/blog/20221108-simplex-chat-v4.2-security-audit-new-website.html) 。

SimpleX Chat 提供基本的小組聊天功能、直接傳訊與 markdown 格式編輯。 也支持 E2EE 音頻和視頻通話。 您的資料可以匯出或匯入另一部裝置，因為沒有中央伺服器備份這些資料。

### Briar

<div class="admonition recommendation" markdown>

![Briar logo](assets/img/messengers/briar.svg){ align=right }

**Briar** 是一個加密的即時通訊軟體，可以使用 Tor 網路 [連線](https://briarproject.org/how-it-works) 到其他用戶端，使其成為規避 [:material-close-outline: 審查](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray } 的有效工具。 Briar 還可以使用鄰近 Wi-Fi 或藍牙連接。 當無法使用網際網路時， Briar 的本地網格（mesh）模式可能很有用。

[:octicons-home-16: 首頁](https://briarproject.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://briarproject.org/privacy-policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://code.briarproject.org/briar/briar/-/wikis/home){ .card-link title=文檔}
[:octicons-code-16:](https://code.briarproject.org/briar/briar){ .card-link title="原始碼" }
[:octicons-heart-16:](https://briarproject.org){ .card-link title="捐款方式列在其首頁底部" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.briarproject.briar.android)
- [:fontawesome-brands-windows: Windows](https://briarproject.org/download-briar-desktop)
- [:simple-linux: Linux](https://briarproject.org/download-briar-desktop)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.briarproject.Briar)

</details>

</div>

Briar 要新增聯絡人，必須先彼此互加。 您可以交換 `briar://` 鏈結或是掃瞄對方的QR碼。

客戶端軟體被獨立 [稽核](https://briarproject.org/news/2017-beta-released-security-audit)，而匿名路由協議使用Tor 網路也接受了審計。

Briar有一個完整 [發布的規範](https://code.briarproject.org/briar/briar-spec)。

Briar 利用[^1] Bramble[Handshake](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BHP.md) 和[Transport](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BTP.md)協定來支持前向保密。

## 額外選項

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

這些通訊軟體無向前保密[^1]，雖然它們達成我們之前建議的某些需求，但不推薦將其用於長期或敏感通信。 訊息收件人之間的任何密鑰洩露都會影響* *所有* *過去通信的機密性。

</div>

### Element

<div class="admonition recommendation" markdown>

![Element標誌](assets/img/messengers/element.svg){ align=right }

**Element** 是[Matrix](https://matrix.org/docs/chat_basics/matrix-for-im) 通訊協定的旗艦用戶端，該協定是安全分散式即時通訊的[開放標準](https://spec.matrix.org/latest)。

在私人聊天室 (需要邀請) 共用的訊息和檔案預設為 E2EE，一對一的語音和視訊通話也是如此。

[:octicons-home-16: 首頁](https://element.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://element.io/privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://element.io/help){ .card-link title=文檔}
[:octicons-code-16:](https://github.com/element-hq){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=im.vector.app)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1083446067)
- [:simple-github: GitHub](https://github.com/element-hq/element-android/releases)
- [:fontawesome-brands-windows: Windows](https://element.io/download)
- [:simple-apple: macOS](https://element.io/download)
- [:simple-linux: Linux](https://element.io/download)
- [:octicons-globe-16: Web](https://app.element.io)

</details>

</div>

個人資料圖片、反應和暱稱不會加密。

With the integration of [Element Call](https://element.io/blog/we-have-lift-off-element-x-call-and-server-suite-are-ready) into Element's web app, desktop apps, and its [rewritten mobile apps](https://element.io/blog/element-x-experience-the-future-of-element), group VoIP and video calls are E2EE by default.

Matrix協議本身 [理論上支援前向保密](https://gitlab.matrix.org/matrix-org/olm/blob/master/docs/megolm.md#partial-forward-secrecy)[^1] ，但 [目前在 Element 中並不支援](https://github.com/vector-im/element-web/issues/7101) ，因為這會破壞某些方面的使用者體驗，例如金鑰備份和共用訊息歷史記錄。

其協議在 2016年獨立進行了 [審計](https://matrix.org/blog/2016/11/21/matrixs-olm-end-to-end-encryption-security-assessment-released-and-implemented-cross-platform-on-riot-at-last) 。 Matrix 協議的規範可以在他們的 [文檔](https://spec.matrix.org/latest)中找到。 Matrix 使用的 [Olm 加密棘輪](https://matrix.org/docs/matrix-concepts/end-to-end-encryption) 是 Signal 的 [雙棘輪演算法](https 的實作: //signal.org/docs/specifications/doubleratchet)。

### Session

<div class="admonition recommendation" markdown>

![Session logo](assets/img/messengers/session.svg){ align=right }

**Session** 是一款分散式通訊軟體，專注於私密、安全和匿名。 Session 支援直接訊息、羣組聊天和語音通話。

Session使用去中心化的 [Oxen Service Node Network](https://oxen.io/) 來儲存和路由訊息。 每條加密訊息都通過 Oxen Service Node Network 中三個節點路由，使得節點幾乎不可能編譯有意義信息給此網路的使用者。

[:octicons-home-16: 首頁](https://getsession.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://getsession.org/privacy-policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://getsession.org/faq){ .card-link title=文檔}
[:octicons-code-16:](https://github.com/oxen-io){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=network.loki.messenger)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1470168868)
- [:simple-github: GitHub](https://github.com/oxen-io/session-android/releases)
- [:fontawesome-brands-windows: Windows](https://getsession.org/download)
- [:simple-apple: macOS](https://getsession.org/download)
- [:simple-linux: Linux](https://getsession.org/download)

</details>

</div>

Session 允許E2EE在一對一聊天或封閉羣組中，最多可容納100名成員。 開放群組對成員數量沒有限制，從設計上來說是開放的。

Session 先前基於 Signal 協議，並於 2020 年 12 月替換為自己的協議。 Session 協議[不](https://getsession.org/blog/session-protocol-technical-information)支持前向保密。[^1]

2020年3月Oxen 對 Session 進行獨立審計。 審計於 2021 年 4 月 [結束](https://getsession.org/session-code-audit) ：

> 此應用程式的整體安全層級良好，讓注重隱私的人也能使用。

Session [白皮書](https://arxiv.org/pdf/2002.04609.pdf) ，描述了應用程式和協議的技術。

## 標準

**請注意，我們所推薦專案沒有任何瓜葛。 ** 除了 [標準準則](about/criteria.md)外，我們還發展出一套明確要求以提出客觀建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

### 最低合格要求

- 有開源客戶端。
- 無需與聯絡人共用個人識別碼（特別是電話號碼或電子郵件）。
- 私人訊息預設必須使用E2EE。
- 支援所有訊息都可 E2EE。
- 進行獨立審計。

### 最佳案例

最佳案例標準代表了我們希望從這個類別的完美項目應具備的功能。 推薦產品可能沒有此功能，但若有這些功能則會讓排名更為提高。

- 支援前向保密[^1]
- 支持未來保密（入侵後安全）[^2]
- 開源伺候器。
- 去中心化，即[聯邦式或 P2P](advanced/communication-network-types.md)。
- 所有訊息預設為使用 E2EE。
- 支援多平台 Linux、macOS、Windows、Android 和 iOS。

[^1]: [前向保密](https://en.wikipedia.org/wiki/Forward_secrecy) 是指密鑰會非常頻繁地輪換，因此如果目前的加密密鑰被洩露，也不會暴露**過去的**訊息。
[^2]: 未來保密（或洩漏後安全）是防止攻擊者利用洩露的私鑰解密**未來**訊息，除非攻擊者將來也能取得更多會話金鑰。 這有效地迫使攻擊者攔截各方間的所有通訊，因為一旦發生未被攔截的密鑰交換，他們就會失去訪問權限。&#160;[ &#8617;](#fnref:2){.footnote-backref}
