---
meta_title: "最好的私人即時通訊軟體 - Privacy Guides"
title: "即時通訊軟體"
icon: material/chat-processing
description: 其他即時通訊則會讓用戶所有的私人對話被該軟體公司取得。
cover: real-time-communication.webp
---

These are our recommendations for encrypted **real-time communication**.

[通訊網絡 :material-arrow-right-drop-circle:](./advanced/communication-network-types.md)

## 加密傳訊軟體

這些軟體非常適合保護您的敏感通訊。

### Signal

<div class="admonition recommendation" markdown>

![Signal logo](assets/img/messengers/signal.svg){ align=right }

**Signal** 是由Signal Messenger LLC開發的行動應用程式。 這款應用程式透過 Signal 協議來保護即時訊息和通話，它是極其安全的加密協議，支援前向保密[^1] 和洩露後安全性。[^2]

[:octicons-home-16: Homepage](https://signal.org/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://signal.org/legal/#privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.signal.org/hc/en-us){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/signalapp){ .card-link title="Source Code" }
[:octicons-heart-16:](https://signal.org/donate/){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

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
3. 輸入一個使用者名稱 此用戶名將一直與一組獨特數字配對，以保持用戶名的唯一性防止人們猜測它，例如，如果輸入“John”，您的用戶名最終可能會是`@john.35`。 By default, only 2 digits are paired with your username when you create it, but you can add more digits until you reach the username length limit (32 characters).
4. 返回系統應用程式設定頁面並選擇**隱私權**。
5. 選擇**手機號碼r**
6. 將**誰可看見我的號碼**設置為: **Nobody**

若想防止已知您手機號碼的人可以找到您的 Signal 帳號或用戶名稱，也可以選擇把 **誰可看見我的號碼** 設置為**無人可見** 。

連絡人清單會使用您的 Signal PIN 加密，而伺服器無法存取。 個人帳號也會加密，並僅與您聊天的聯絡人分享。 Signal 支援[私密 群組](https://signal.org/blog/signal-private-group-system)，伺服器不會記錄該群組成員資格、群組標題、群組頭像，或群組屬性。 當啓用 [Sealed Sender](https://signal.org/blog/sealed-sender) 時， Signal具有最小元數據。 發件人地址與訊息內文一起加密，伺服器只可見到收件人地址。 Sealed Sender 功能僅適用於聯絡人清單的成員，但在收訊時也可啟用以防止接收垃圾郵件增加的風險。

其協議在2016年獨立進行了 [審計](https://eprint.iacr.org/2016/1013.pdf) 。 Signal 協議的規範可以在他們的 [文檔](https://signal.org/docs)中找到。

我們有一些關於配置和硬化 Signal 安裝的額外提示：

[Signal 配置和硬化 :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening)

### SimpleX Chat

<div class="admonition recommendation" markdown>

![Simplex logo](assets/img/messengers/simplex.svg){ align=right }

**SimpleX** Chat 是一個分散的即時通訊工具，不依賴任何獨有識別碼，如電話號碼或用戶名。 SimpleX Chat 使用者可以掃描二維碼或點擊邀請連結以參與羣組對話。

[:octicons-home-16: Homepage](https://simplex.chat){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/simplex-chat/simplex-chat/blob/stable/PRIVACY.md){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/simplex-chat/simplex-chat/tree/stable/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/simplex-chat){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=chat.simplex.app)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1605771084)
- [:simple-github: GitHub](https://github.com/simplex-chat/simplex-chat/releases)
- [:fontawesome-brands-windows: Windows](https://simplex.chat/downloads/#desktop-app)
- [:simple-apple: macOS](https://simplex.chat/downloads/#desktop-app)
- [:simple-linux: Linux](https://simplex.chat/downloads/#desktop-app)

</details>

</div>

SimpleX Chat 於2022年10月接受 Trail of Bits [審計](https://simplex.chat/blog/20221108-simplex-chat-v4.2-security-audit-new-website.html) 。

SimpleX Chat 提供基本的小組聊天功能、直接傳訊與 markdown 格式編輯。 也支持 E2EE 音頻和視頻通話。 您可以匯出資料，並匯入到另一個設備，因為沒有中央伺服器備份。

### Briar

<div class="admonition recommendation" markdown>

![Briar logo](assets/img/messengers/briar.svg){ align=right }

**Briar** 是 [連接](https://briarproject.org/how-it-works)其他使用 Tor網路客戶端的加密即時通訊工具。 Briar 還可以在本地附近通過 Wi-Fi 或藍牙連接。 當無法使用網際網路時， Briar 的本地網格(mesh)模式可能很有用。

[:octicons-home-16: Homepage](https://briarproject.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://briarproject.org/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://code.briarproject.org/briar/briar/-/wikis/home){ .card-link title=Documentation}
[:octicons-code-16:](https://code.briarproject.org/briar/briar){ .card-link title="Source Code" }
[:octicons-heart-16:](https://briarproject.org){ .card-link title="Donation options are listed on the bottom of the homepage" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.briarproject.briar.android)
- [:fontawesome-brands-windows: Windows](https://briarproject.org/download-briar-desktop)
- [:simple-linux: Linux](https://briarproject.org/download-briar-desktop)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.briarproject.Briar)

</details>

</div>

Briar 要新增聯絡人，必須先彼此互加。 您可以交換 `briar://` 鏈結或是掃瞄對方的二維碼。

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

![Element logo](assets/img/messengers/element.svg){ align=right }

**Element** 是 [Matrix](https://matrix.org/docs/chat_basics/matrix-for-im) 協議的參考[用戶端](https://matrix.org/ecosystem/clients/) ，這是一個 [開放標準](https://spec.matrix.org/latest) 、安全去中心化實時通訊。

在私人聊天室（需透過邀請加入）共享的訊息和文件預設為 E2EE ，一對一的語音和視訊通話也是如此。

[:octicons-home-16: Homepage](https://element.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://element.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://element.io/help){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/element-hq){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

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

羣組語音和視視通話 [則不是](https://github.com/vector-im/element-web/issues/12878) E2EE ，而是使用Jitsi ，但預計將隨著 [Native Group VoIP Signalling](https://github.com/matrix-org/matrix-doc/pull/3401)而發生變化。 群組通目前 [沒有驗證](https://github.com/vector-im/element-web/issues/13074) ，因此其它人員也可以加入。 我們建議您不要將此功能用於私人會議。

Matrix 協議本身[理論上支持前向保密](https://gitlab.matrix.org/matrix-org/olm/blob/master/docs/megolm.md#partial-forward-secrecy) [^1]，但[ Element 目前不支援](https:/ / github.com/vector-im/element-web/issues/7101)，因為會破壞某方面的使用者體驗，例如金鑰備份和共享訊息歷史記錄。

其協議在 2016年獨立進行了 [審計](https://matrix.org/blog/2016/11/21/matrixs-olm-end-to-end-encryption-security-assessment-released-and-implemented-cross-platform-on-riot-at-last) 。 Matrix 協議的規範可以在他們的 [文檔](https://spec.matrix.org/latest)中找到。 Matrix 使用的 [Olm 加密棘輪](https://matrix.org/docs/matrix-concepts/end-to-end-encryption) 是 Signal 的 [雙棘輪演算法](https 的實作: //signal.org/docs/specifications/doubleratchet)。

### Session

<div class="admonition recommendation" markdown>

![Session logo](assets/img/messengers/session.svg){ align=right }

**Session** 是一款分散式通訊軟體，專注於私密、安全和匿名。 Session 支援直接訊息、羣組聊天和語音通話。

Session使用去中心化的 [Oxen Service Node Network](https://oxen.io/) 來儲存和路由訊息。 每條加密訊息都通過 Oxen Service Node Network 中三個節點路由，使得節點幾乎不可能編譯有意義信息給此網路的使用者。

[:octicons-home-16: Homepage](https://getsession.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://getsession.org/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://getsession.org/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/oxen-io){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=network.loki.messenger)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1470168868)
- [:simple-github: GitHub](https://github.com/oxen-io/session-android/releases)
- [:fontawesome-brands-windows: Windows](https://getsession.org/download)
- [:simple-apple: macOS](https://getsession.org/download)
- [:simple-linux: Linux](https://getsession.org/download)

</details>

</div>

會話允許E2EE在一對一聊天或封閉羣組中，最多可容納100名成員。 開放羣組對成員數量沒有限制，從設計上來說是開放的。

Session 先前基於 Signal 協議，並於 2020 年 12 月替換為自己的協議。 Session 協議[不](https://getsession.org/blog/session-protocol-technical-information)支持前向保密。<sup id="fnref3:1"><a href= "#fn:1" class="footnote-ref">1</a></sup>

2020年3月Oxen 對 Session 進行獨立審計。 審計 [在2021年4月完成](https://getsession.org/session-code-audit) ， “此應用程式整體安全級別良好，可供關注隱私的人使用。

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

- 支持前向保密[^1]
- 支持未來保密（入侵後安全）[^2]
- 開源伺候器。
- 去中心化，即[聯邦式或 P2P](advanced/communication-network-types.md)。
- 所有訊息預設為使用 E2EE。
- 支援多平台 Linux、macOS、Windows、Android 和 iOS。

[^1]: [前向保密](https://en.wikipedia.org/wiki/Forward_secrecy)金鑰輪換非常頻繁，因此，如果當前加密金鑰被洩露，也不會暴露**過去**訊息
[^2]: 未來保密（或洩漏後安全）是防止攻擊者利用洩露的私鑰解密**未來**訊息，除非攻擊者將來也能取得更多會話金鑰。 這有效地迫使攻擊者攔截各方間的所有通訊，因為一旦發生未被攔截的密鑰交換，他們就會失去訪問權限。&#160;[ &#8617;](#fnref:2){.footnote-backref}
