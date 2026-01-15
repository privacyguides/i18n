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

Note that you are trusting multiple parties by using Molly, as you now need to trust the Signal team *and* the Molly team to deliver safe and timely updates.

**Molly-FOSS** is a version of Molly which removes proprietary code like the Google services used by both Signal and Molly at the expense of some features (like battery-saving push notifications via Google Play Services). You can set up push notifications without Google Play Services in either version of Molly with [UnifiedPush](https://unifiedpush.org). Using this notification delivery method requires access to a [MollySocket](https://github.com/mollyim/mollysocket) server, but you can choose a public MollySocket instance for this.[^3]

Both versions of Molly provide the same security improvements and support [reproducible builds](https://github.com/mollyim/mollyim-android/tree/main/reproducible-builds), meaning it's possible to confirm that the compiled APKs match the source code.

## SimpleX Chat

<div class="admonition recommendation" markdown>

![SimpleX Chat logo](assets/img/messengers/simplex.svg){ align=right }

**SimpleX Chat** is an instant messenger that doesn't depend on any unique identifiers such as phone numbers or usernames. 其分佈式網路使 SimpleX Chat 成為對抗 [:material-close-outline: 審查](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray } 的有效工具。

[:octicons-home-16: 首頁](https://simplex.chat){ .md-button .md-button--primary }
[:octicons-eye-16:](https://simplex.chat/privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://simplex.chat/docs/simplex.html){ .card-link title="說明文件" }
[:octicons-code-16:](https://github.com/simplex-chat){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=chat.simplex.app)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1605771084)
- [:simple-github: GitHub](https://github.com/simplex-chat/simplex-chat/releases)
- [:fontawesome-brands-windows: Windows](https://simplex.chat/downloads/#desktop-app)
- [:simple-apple: macOS](https://simplex.chat/downloads/#desktop-app)
- [:simple-linux: Linux](https://simplex.chat/downloads/#desktop-app)
- [:simple-flathub: Flathub](https://flathub.org/en/apps/chat.simplex.simplex)

</details>

</div>

SimpleX Chat provides direct messaging, group chats, and E2EE calls secured with the [SimpleX Messaging Protocol](https://github.com/simplex-chat/simplexmq/blob/stable/protocol/simplex-messaging.md), which uses double ratchet encryption with quantum resistance. Additionally, SimpleX Chat provides metadata protection by using unidirectional ["simplex queues"](https://github.com/simplex-chat/simplexmq/blob/stable/protocol/simplex-messaging.md#simplex-queue) to deliver messages.

To participate in conversations on SimpleX Chat, you must scan a QR code or click an invite link. This allows you to verify a contact out-of-band, which protects against man-in-the-middle attacks by network providers. Your data can be exported and imported onto another device, as there are no central servers where this is backed up.

You can find a full list of the privacy and security [features](https://github.com/simplex-chat/simplex-chat#privacy-and-security-technical-details-and-limitations) implemented in SimpleX Chat in the app's repository.

SimpleX Chat was independently audited in [July 2024](https://simplex.chat/blog/20241014-simplex-network-v6-1-security-review-better-calls-user-experience.html#simplex-cryptographic-design-review-by-trail-of-bits) and in [October 2022](https://simplex.chat/blog/20221108-simplex-chat-v4.2-security-audit-new-website).

## Briar

<div class="admonition recommendation" markdown>

![Briar logo](assets/img/messengers/briar.svg){ align=right }

**Briar** is an encrypted instant messenger that [connects](https://briarproject.org/how-it-works) to other clients using the [Tor network](alternative-networks.md#tor), making it an effective tool at circumventing [:material-close-outline: Censorship](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }. Briar 還可以使用鄰近 Wi-Fi 或藍牙連接。 當無法使用網際網路時， Briar 的本地網格（mesh）模式可能很有用。

[:octicons-home-16: Homepage](https://briarproject.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://briarproject.org/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://code.briarproject.org/briar/briar/-/wikis/home){ .card-link title="Documentation" }
[:octicons-code-16:](https://code.briarproject.org/briar/briar){ .card-link title="Source Code" }
[:octicons-heart-16:](https://code.briarproject.org/briar/briar#donate){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.briarproject.briar.android)
- [:fontawesome-brands-windows: Windows](https://briarproject.org/download-briar-desktop)
- [:simple-linux: Linux](https://briarproject.org/download-briar-desktop)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.briarproject.Briar)

</details>

</div>

To add a contact on Briar, you must both add each other first. You can either exchange `briar://` links or scan a contact’s QR code if they are nearby.

Briar has a fully [published specification](https://code.briarproject.org/briar/briar-spec). Briar supports forward secrecy[^1] by using the Bramble [Handshake](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BHP.md) and [Transport](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BTP.md) protocol.

The client software was independently [audited](https://briarproject.org/news/2017-beta-released-security-audit), and the anonymous routing protocol uses the Tor network which has also been audited.

## 標準

**請注意，我們與推薦的任何項目均無關。**除了[我們的通用標準](about/criteria.md)外，我們還制定了一套明確的要求，以便我們能夠提供客觀的建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

### 最低合格要求

- Must have open-source clients.
- Must not require sharing personal identifiers (particularly phone numbers or emails) with contacts.
- Must use E2EE for private messages by default.
- Must support E2EE for all messages.
- Must support forward secrecy[^1]
- 必須由信譽良好的獨立第三方進行公開審核。

### 最佳情況

最佳情況標準代表我們希望在這個類別的完美項目的應具備的特性。 推薦產品可能沒有此功能，但若有這些功能則會讓排名更為提高。

- Should support future secrecy (post-compromise security)[^2]
- Should have open-source servers.
- Should use a decentralized network, i.e. [federated or P2P](advanced/communication-network-types.md).
- Should use E2EE for all messages by default.
- Should support Linux, macOS, Windows, Android, and iOS.
[^3]: You may refer to this step-by-step tutorial in German on how to set up UnifiedPush as the notification provider for Molly: [https://kuketz-blog.de/messenger-wechsel-von-signal-zu-molly-unifiedpush-mollysocket-ntfy](https://kuketz-blog.de/messenger-wechsel-von-signal-zu-molly-unifiedpush-mollysocket-ntfy).

[^1]: [Forward secrecy](https://en.wikipedia.org/wiki/Forward_secrecy) is where keys are rotated very frequently, so that if the current encryption key is compromised, it does not expose **past** messages as well.
[^2]: Future secrecy (or [post-compromise security](https://eprint.iacr.org/2016/221.pdf)) is a feature where an attacker is prevented from decrypting **future** messages after compromising a private key, unless they compromise more session keys in the future as well. This effectively forces the attacker to intercept all communication between parties since they lose access as soon as a key exchange occurs that is not intercepted.
