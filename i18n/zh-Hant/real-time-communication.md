---
meta_title: "The Best Private Instant Messengers - Privacy Guides"
title: "即時通訊軟體"
icon: material/chat-processing
description: Other instant messengers make all of your private conversations available to the company that runs them.
cover: real-time-communication.webp
---

這些是我們所推薦的加密實時通訊軟體。

[通訊網絡 :material-arrow-right-drop-circle:](./advanced/communication-network-types.md)

## 加密傳訊軟體

這些軟體非常適合保護您的敏感通訊。

### Signal

<div class="admonition recommendation" markdown>

![Signal logo](assets/img/messengers/signal.svg){ align=right }

**Signal** 是由Signal Messenger LLC開發的行動應用程式。 The app provides instant messaging and calls secured with the Signal Protocol, an extremely secure encryption protocol which supports forward secrecy[^1] and post-compromise security.[^2]

[:octicons-home-16: Homepage](https://signal.org/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://signal.org/legal/#privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.signal.org/hc/en-us){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/signalapp){ .card-link title="Source Code" }
[:octicons-heart-16:](https://signal.org/donate/){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads "下載"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.thoughtcrime.securesms)
- [:simple-appstore: App Store](https://apps.apple.com/app/id874139669)
- [:simple-android: Android](https://signal.org/android/apk/)
- [:simple-windows11: Windows](https://signal.org/download/windows)
- [:simple-apple: macOS](https://signal.org/download/macos)
- [:simple-linux: Linux](https://signal.org/download/linux)

</details>

</div>

Signal requires your phone number for registration, however you should create a username to hide your phone number from your contacts:

1. In Signal, open the app's settings and tap your account profile at the top.
2. Tap **Username** and choose **Continue** on the "Set up your Signal username" screen.
3. Enter a username. Your username will always be paired with a unique set of digits to keep your username unique and prevent people from guessing it, for example if you enter "John" your username might end up being `@john.35`.
4. Go back to the main app settings page and select **Privacy**.
5. Select **Phone Number**
6. Change the **Who Can See My Number** setting to: **Nobody**

You can optionally change the **Who Can Find Me By Number** setting to **Nobody** as well, if you want to prevent people who already have your phone number from discovering your Signal account/username.

Contact lists on Signal are encrypted using your Signal PIN and the server does not have access to them. 個人帳號也會加密，並僅與您聊天的聯絡人分享。 Signal supports [private groups](https://signal.org/blog/signal-private-group-system/), where the server has no record of your group memberships, group titles, group avatars, or group attributes. 當啓用 [Sealed Sender](https://signal.org/blog/sealed-sender/) 時， Signal具有最小元數據。 發件人地址與訊息內文一起加密，伺服器只可見到收件人地址。 Sealed Sender 功能僅適用於聯絡人清單的成員，但在收訊時也可啟用以防止接收垃圾郵件增加的風險。

其協議在2016年獨立進行了 [審計](https://eprint.iacr.org/2016/1013.pdf) 。 Signal 協議的規範可以在他們的 [文檔](https://signal.org/docs/)中找到。

我們有一些關於配置和硬化 Signal 安裝的額外提示：

[Signal 配置和硬化 :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening/)

### SimpleX Chat

<div class="admonition recommendation" markdown>

![Simplex logo](assets/img/messengers/simplex.svg){ align=right }

**SimpleX** Chat 是一個分散的即時通訊工具，不依賴任何獨有識別碼，如電話號碼或用戶名。 SimpleX Chat 使用者可以掃描二維碼或點擊邀請連結以參與羣組對話。

[:octicons-home-16: Homepage](https://simplex.chat){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/simplex-chat/simplex-chat/blob/stable/PRIVACY.md){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/simplex-chat/simplex-chat/tree/stable/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/simplex-chat){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads "下載"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=chat.simplex.app)
- [:simple-appstore: App Store](https://apps.apple.com/us/app/simplex-chat/id1605771084)
- [:simple-github: GitHub](https://github.com/simplex-chat/simplex-chat/releases)
- [:simple-windows11: Windows](https://simplex.chat/downloads/#desktop-app)
- [:simple-apple: macOS](https://simplex.chat/downloads/#desktop-app)
- [:simple-linux: Linux](https://simplex.chat/downloads/#desktop-app)

</details>

</div>

SimpleX Chat 於2022年10月接受 Trail of Bits [審計](https://simplex.chat/blog/20221108-simplex-chat-v4.2-security-audit-new-website.html) 。

SimpleX Chat 提供基本的小組聊天功能、直接傳訊與 markdown 格式編輯。 也支持 E2EE 音頻和視頻通話。 您可以匯出資料，並匯入到另一個設備，因為沒有中央伺服器備份。

### Briar

<div class="admonition recommendation" markdown>

![Briar logo](assets/img/messengers/briar.svg){ align=right }

**Briar** 是 [連接](https://briarproject.org/how-it-works/)其他使用 Tor網路客戶端的加密即時通訊工具。 Briar 還可以在本地附近通過 Wi-Fi 或藍牙連接。 當無法使用網際網路時， Briar 的本地網格(mesh)模式可能很有用。

[:octicons-home-16: Homepage](https://briarproject.org/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://briarproject.org/privacy-policy/){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://code.briarproject.org/briar/briar/-/wikis/home){ .card-link title=Documentation}
[:octicons-code-16:](https://code.briarproject.org/briar/briar){ .card-link title="Source Code" }
[:octicons-heart-16:](https://briarproject.org/){ .card-link title="Donation options are listed on the bottom of the homepage" }

<details class="downloads" markdown>
<summary>Downloads "下載"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.briarproject.briar.android)
- [:simple-windows11: Windows](https://briarproject.org/download-briar-desktop/)
- [:simple-linux: Linux](https://briarproject.org/download-briar-desktop/)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.briarproject.Briar)

</details>

</div>

Briar 要新增聯絡人，必須先彼此互加。 您可以交換 `briar://` 鏈結或是掃瞄對方的二維碼。

客戶端軟體被獨立 [稽核](https://briarproject.org/news/2017-beta-released-security-audit/)，而匿名路由協議使用Tor 網路也接受了審計。

Briar有一個完整 [發布的規範](https://code.briarproject.org/briar/briar-spec)。

Briar supports forward secrecy[^1] by using the Bramble [Handshake](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BHP.md) and [Transport](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BTP.md) protocol.

## 額外選項

<div class="admonition warning" markdown>
<p class="admonition-title">Warning "警告"</p>

These messengers do not have forward secrecy[^1], and while they fulfill certain needs that our previous recommendations may not, we do not recommend them for long-term or sensitive communications. 訊息收件人之間的任何密鑰洩露都會影響* *所有* *過去通信的機密性。

</div>

### Element

<div class="admonition recommendation" markdown>

![Element logo](assets/img/messengers/element.svg){ align=right }

**Element** is the reference [client](https://matrix.org/ecosystem/clients/) for the [Matrix](https://matrix.org/docs/guides/introduction) protocol, an [open standard](https://matrix.org/docs/spec) for secure decentralized real-time communication.

在私人聊天室（需透過邀請加入）共享的訊息和文件預設為 E2EE ，一對一的語音和視訊通話也是如此。

[:octicons-home-16: Homepage](https://element.io/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://element.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://element.io/help){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/vector-im){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads "下載"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=im.vector.app)
- [:simple-appstore: App Store](https://apps.apple.com/app/vector/id1083446067)
- [:simple-github: GitHub](https://github.com/vector-im/element-android/releases)
- [:simple-windows11: Windows](https://element.io/get-started)
- [:simple-apple: macOS](https://element.io/get-started)
- [:simple-linux: Linux](https://element.io/get-started)
- [:octicons-globe-16: Web](https://app.element.io)

</details>

</div>

個人資料圖片、反應和暱稱不會加密。

羣組語音和視視通話 [則不是](https://github.com/vector-im/element-web/issues/12878) E2EE ，而是使用Jitsi ，但預計將隨著 [Native Group VoIP Signalling](https://github.com/matrix-org/matrix-doc/pull/3401)而發生變化。 群組通目前 [沒有驗證](https://github.com/vector-im/element-web/issues/13074) ，因此其它人員也可以加入。 我們建議您不要將此功能用於私人會議。

The Matrix protocol itself [theoretically supports forward secrecy](https://gitlab.matrix.org/matrix-org/olm/blob/master/docs/megolm.md#partial-forward-secrecy)[^1], however this is [not currently supported in Element](https://github.com/vector-im/element-web/issues/7101) due to it breaking some aspects of the user experience such as key backups and shared message history.

其協議在 2016年獨立進行了 [審計](https://matrix.org/blog/2016/11/21/matrixs-olm-end-to-end-encryption-security-assessment-released-and-implemented-cross-platform-on-riot-at-last) 。 Matrix 協議的規範可以在他們的 [文檔](https://spec.matrix.org/latest/)中找到。 Matrix 使用的 [Olm 加密棘輪](https://matrix.org/docs/matrix-concepts/end-to-end-encryption/)是執行Signal [Double Ratchet 演算法](https://signal.org/docs/specifications/doubleratchet/)。

### Session

<div class="admonition recommendation" markdown>

![Session logo](assets/img/messengers/session.svg){ align=right }

**Session** 是一款分散式通訊軟體，專注於私密、安全和匿名。 Session 支援直接訊息、羣組聊天和語音通話。

Session使用去中心化的 [Oxen Service Node Network](https://oxen.io/) 來儲存和路由訊息。 每條加密訊息都通過 Oxen Service Node Network 中三個節點路由，使得節點幾乎不可能編譯有意義信息給此網路的使用者。

[:octicons-home-16: Homepage](https://getsession.org/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://getsession.org/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://getsession.org/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/oxen-io){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads "下載"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=network.loki.messenger)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1470168868)
- [:simple-github: GitHub](https://github.com/oxen-io/session-android/releases)
- [:simple-windows11: Windows](https://getsession.org/download)
- [:simple-apple: macOS](https://getsession.org/download)
- [:simple-linux: Linux](https://getsession.org/download)

</details>

</div>

會話允許E2EE在一對一聊天或封閉羣組中，最多可容納100名成員。 開放羣組對成員數量沒有限制，從設計上來說是開放的。

Session was previously based on Signal Protocol before replacing it with their own in December 2020. Session Protocol does [not](https://getsession.org/blog/session-protocol-technical-information) support forward secrecy.[^1]

Oxen requested an independent audit for Session in March 2020. The audit [concluded](https://getsession.org/session-code-audit) in April 2021, “The overall security level of this application is good and makes it usable for privacy-concerned people.”

Session has a [whitepaper](https://arxiv.org/pdf/2002.04609.pdf) describing the technical details of the app and protocol.

## 標準

**請注意，我們所推薦專案沒有任何瓜葛。 ** 除了 [標準準則](about/criteria.md)外，我們還發展出一套明確要求以提出客觀建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

<div class="admonition example" markdown>
<p class="admonition-title">此部份新增</p>

我們正在努力為我們網站的每個部分建立定義的標準，這可能會有所變化。 如果您對我們的標準有任何疑問，請在 [論壇上提問](https://discuss.privacyguides.net/latest) ，如果沒有列出，請不要認為我們在提出建議時沒有考慮到某些事情。 當我們推薦一個項目時，有許多因素被考慮和討論，記錄每一個項目都是正在進行式。

</div>

- Has open-source clients.
- Does not require sharing personal identifiers (phone numbers or emails in particular) with contacts.
- Uses E2EE for private messages by default.
- Supports E2EE for all messages.
- Has been independently audited.

### 最佳案例

最佳案例標準代表了我們希望從這個類別的完美項目應具備的功能。 推薦產品可能沒有此功能，但若有這些功能則會讓排名更為提高。

- Supports Forward Secrecy[^1]
- Supports Future Secrecy (Post-Compromise Security)[^2]
- Has open-source servers.
- Decentralized, i.e. [federated or P2P](advanced/communication-network-types.md).
- Uses E2EE for all messages by default.
- Supports Linux, macOS, Windows, Android, and iOS.

[^1]: [Forward Secrecy](https://en.wikipedia.org/wiki/Forward_secrecy) is where keys are rotated very frequently, so that if the current encryption key is compromised, it does not expose **past** messages as well.
[^2]: Future Secrecy (or Post-Compromise Security) is a feature where an attacker is prevented from decrypting **future** messages after compromising a private key, unless they compromise more session keys in the future as well. This effectively forces the attacker to intercept all communication between parties, since they lose access as soon as a key exchange occurs that is not intercepted.
