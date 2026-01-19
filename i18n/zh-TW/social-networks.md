---
title: 社交網路
icon: material/account-supervisor-circle-outline
description: 尋找一個不會窺探您的個人資料或將其貨幣化的新社交網路。
cover: social-networks.webp
---

<small>防護下列威脅：</small>

- [:material-close-outline: 審查](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }
- [:material-account-cash: 監控資本主義](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

這些尊重隱私的**社交網絡**，讓您能在不透露全名、電話號碼等個人資訊的情況下參與線上社群，這些資料正是科技公司常要求提供的內容。

社交媒體平台間日益嚴重的問題是兩種不同形式的審查。 首先，他們經常默許非法的審查要求，這些要求可能來自惡意的政府，也可能來自他們自己的內部政策。 其次，這些平台常要求使用者註冊帳號才能存取封閉內容，此類內容若在開放網路中本可自由發佈；此舉實質上審查了注重隱私的使用者瀏覽行為，因為這些使用者無法承擔在該類網路開立帳號所衍生的隱私代價。

我們推薦的社交網路透過開放且分散的社交網路協定來解決審查問題。 檢視公開內容也不需要帳號。

您應該注意，所有社交網路都 **不** 適合私人或敏感的通訊。 若要直接與他人聊天，您應該使用我們推薦—具有強大端對端加密功能的 [即時通訊工具](real-time-communication.md) ，並只使用社交媒體上的直接訊息，以便與聯絡人建立更私密、更安全的聊天平台。

## 去中心化

去中心化社交網絡的架構與主流社交媒體平台截然不同，卻與電子郵件的底層結構頗為相似。 與其像在 Facebook 或 Discord 上那樣，透過單一整合服務開立帳號，您反而會選擇加入獨立的公開伺服器。 您所加入的伺服器能夠與其他伺服器進行通訊並發現它們；這種去中心化的特性亦稱為_聯邦制_。

此去中心化模式的一項顯著優勢在於，整個網路中不存在能夠審查您帳號的中央權威機構，儘管您的帳號仍可能被個別伺服器封禁或禁言。

此去中心化模式的注意事項在於：每台伺服器皆為獨立的法律實體，擁有各自的隱私政策、使用條款、管理團隊及版主。 雖然其中許多伺服器比傳統的社交媒體平台限制 _少_ 且更尊重隱私權，但也有些可能限制更 _多_ 或 _可能_ 損害您的隱私。 通常，社交網路所執行的軟體不會區分這些管理員，也不會對其權限施加任何限制。

## 抵抗審查

儘管去中心化社交網路在網路層級上沒有審查制度，但根據伺服器管理員的決定，使用者仍可能在伺服器層級遭遇審查。 管理員有權**解除**與其他伺服器的聯邦關係，此舉將導致您可檢視的內容與可互動的對象受到限制。

若您非常擔心現有伺服器會審查您的內容、您可取得的內容或其他伺服器，通常有兩種選擇：

1. \*\*自行架設社交網路軟體。\*\*這種方法可以讓您與任何其他您可以自行架設的網站一樣，具有完全相同的極高抗審查能力。

2. **使用受管主機服務。** 我們沒有特定推薦方案，但市面上有眾多主機服務商可為您在自有網域（或偶爾在其網域的子網域）建立全新伺服器，我們不建議採用後者，除非註冊自有網域對您的隱私造成過大負擔。

   通常，主機服務供應商會負責處理您伺服器的**技術**層面，但**內容管理**部分則完全交由您自行處理。 對多數人而言，這通常比自行架設伺服器更為理想，因為您既能享有對自身伺服器的更大控制權，又無需擔憂技術問題或未修補的安全漏洞。

   在註冊之前，您應仔細閱讀您的主機供應商的服務條款及可接受使用政策。 這些條款通常遠比典型的主機伺服器規則更為寬泛，且在缺乏追索權的情況下，其強制執行的可能性也低得多，但它們仍可能以令人不悅的方式施加限制。

## Mastodon

<div class="admonition recommendation" markdown>

![Mastodon logo](assets/img/social-networks/mastodon.svg){ align=right }

**Mastodon** 是基於開放網路通訊協定和自由及開放原始碼軟體的社交網路。 它使用 **:simple-activitypub: ActivityPub** 協定，就像電子郵件一樣是去中心化的：使用者可以存在於不同的伺服器甚至不同的社交平台上，但仍然可以相互溝通。

[:octicons-home-16: 首頁](https://joinmastodon.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.joinmastodon.org){ .card-link title="說明文件" }

</div>

有許多軟體平台使用 ActivityPub 作為其後端社交網路通訊協定，這意味著即使它們執行不同的軟體，也能與伺服器進行通訊。 例如，PeerTube 是使用 ActivityPub 的影片發佈軟體，這表示您可以使用另一個 PeerTube 帳戶追蹤 PeerTube 上的頻道， _或_ 使用 Mastodon 帳戶，因為 Mastodon 也使用 ActivityPub。

基於以下這些原因，我們選擇推薦 Mastodon 而非其他 ActivityPub 軟體作為您的主要社交媒體平台：

1. Mastodon 具有穩固的安全更新歷史。 在極少數發現重大安全漏洞的情況下，他們能迅速且妥善地協調修補程式釋出事宜。 過去，他們也會將這些安全修補程式回傳到較舊的功能分支。 這讓資歷較淺的伺服器管理員更容易保持實例安全，因為他們可能不習慣立即升級到最新版本。 Mastodon 也在網頁介面中內建了更新通知系統，讓伺服器管理員更有可能知道可用於其實例的重要安全修補程式。

2. 大多數內容類型可用於 Mastodon。 儘管主要作為微部落格平台，Mastodon 仍能輕鬆處理較長的貼文、圖片貼文、影片貼文，以及追蹤非 Mastodon 使用者的 ActivityPub 活動時可能遇到的多數其他貼文類型。 這讓您的 Mastodon 帳戶成為追蹤任何人的理想「中央樞紐」，不論他們選擇使用何種平台。 相較之下，如果你只用 PeerTube 帳號，你就**只能**追蹤其他的影音頻道。

3. Mastodon 有相當全面的隱私權控制。 它有許多內建功能，可讓您限制是否共享資料和資料共用的方式，以下會介紹其中一些功能。 他們在開發新功能時也會考慮到隱私權。 舉例來說，當其他 ActivityPub 軟體僅透過略微調整嵌入式互動視窗來處理其他貼文連結，便快速實現「引用貼文」功能時，Mastodon 正在[開發](https://blog.joinmastodon.org/2025/02/bringing-quote-posts-to-mastodon)一項引用貼文功能，讓您在貼文被引用時能享有更精細的控制權。

### 選擇實例

為了從 Mastodon 獲得最大的效益，選擇一個與您想要張貼或閱讀的內容類型相匹配的伺服器或「實例」是至關重要的。 我們目前不推薦任何特定的實例，但您可以在我們的社群中找到建議。 我們建議避免使用 _mastodon.social_ 和 _mastodon.online_ ，因為它們是由開發 Mastodon 軟體本身的同一家公司所經營。 從去中心化的角度長遠來看，不要使用軟體開發者所控制的伺服器是比較好的做法，這樣就沒有任何一方可以對整個網路施加過多的控制。

### 建議的隱私設定

從 Mastodon 的網頁介面，點選右邊側邊欄的**管理介面**連結。 在管理介面的控制面板中，您可以在左側邊欄中找到這些區塊：

#### 公開的個人檔案

在此處的**隱私權及觸及**分頁下，設有多項隱私控制選項。 尤其要注意以下事項：

- [ ] **自動同意新跟隨者**：您應該考慮取消勾選此方塊，以建立私人檔案。 這將讓您在接受追蹤前，先檢視哪些人可以追蹤您的帳號。

  與大多數社群媒體平台不同，即使您擁有私人檔案，仍可選擇發表對非跟隨者公開可見的貼文，且這些貼文仍可被非跟隨者轉嘟。 因此，取消勾選此方塊是唯一可以**選擇**發表給全世界或特定人群的方法。

- [ ] **於個人檔案中顯示跟隨中及跟隨者**：您應該取消勾選此方塊以隱藏您的社交圖譜。 你追蹤的人名單對他人產生實質助益的情況相當罕見，但這類資訊卻可能對你構成風險。

- [ ] **顯示您發嘟文之應用程式**：您應該取消勾選此方塊，以避免不必要地向他人透露您的個人電腦組態資訊。

本頁面的其他隱私控制措施仍應詳閱，但我們必須強調這些措施並非技術性控制，它們僅是您向他人提出的要求。 舉例來說，即使您在此頁面選擇將個人檔案隱藏於搜尋引擎，實際上**並無**任何機制能阻止搜尋引擎讀取您的個人檔案。 您僅是要求搜尋引擎索引不要將您的內容發佈給其使用者。

您仍可能希望提出這些請求，因為它們能實際減少您的數位足跡。 然而，不應過分**依賴**它們。 要讓您的貼文不被搜尋引擎和其他人看見，唯一有效的方法是採用非公開（僅限追蹤者）的可見性設定，**並**限制可追蹤您帳號的人員範圍。

#### 偏好設定

您應將您的**嘟文可見性**設定從公開變更為**僅限跟隨者**。

請注意，這只會變更您的預設設定，以防止意外的過度分享。 您可以在撰寫新貼文時隨時調整可見性。

#### 自動嘟文刪除

- [x] 勾選**自動刪除舊嘟文**方塊。

此處的預設設定已足夠完善，系統將自動刪除您發布後超過兩週的嘟文，除非您將其標記為最愛。 這為您提供了一個簡易的方法來控制哪些嘟文永久保留，哪些則僅是短暫存在。 然而，關於嘟文保留時間長短與時機的諸多設定，皆可在此處依個人需求進行調整。

超過數週的社群媒體嘟文，極少會被閱讀或對他人產生相關性。 這些較早的嘟文常被忽略，因為批次處理它們頗具挑戰性，但隨著時間推移，它們能逐步構築出關於你的相當完整的個人檔案。 您應始終以短暫性為預設目標發表內容，僅在經過深思熟慮後才讓嘟文保留更長時間。

### 張貼內容

發表新嘟文時，您將可從下列可見性設定中選擇其中一項：

- **公開**，可將您的內容發表給網際網路上的任何人。
- **不公開**，您應該認為等同於公開張貼！ 這並非技術性保證，僅是您向其他伺服器提出的要求，以將您的嘟文隱藏於某些 feed 之外。
- **跟隨者**，只向您的跟隨者發表您的內容。 If you did not follow our recommendation of restricting your followers, you should consider this equivalent to publicly posting!
- **Specific people**, which only shares the post with people who are specifically mentioned within the post. This is Mastodon's version of direct messages, but should never be relied on for private communications as we covered earlier since Mastodon has no E2EE.

If you used our recommended configuration settings above, you should be posting to **Followers** by default, and only posting to **Public** on an intentional and case-by-case basis.

## Element

<div class="admonition recommendation" markdown>

![Element logo](assets/img/social-networks/element.svg){ align=right }

**Element** is the flagship client for the **:simple-matrix: [Matrix](https://matrix.org/docs/chat_basics/matrix-for-im)** protocol, an [open standard](https://spec.matrix.org/latest) that enables decentralized communication by way of federated chat rooms. Users can exist on different homeservers but still communicate with each other.

[:octicons-home-16: 首頁](https://element.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://element.io/privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://element.io/help){ .card-link title="說明文件" }
[:octicons-code-16:](https://github.com/element-hq){ .card-link title="原始碼" }

<details class="downloads" markdown><summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.element.android.x)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1631335820)
- [:simple-github: GitHub](https://github.com/element-hq/element-x-android/releases)
- [:fontawesome-brands-windows: Windows](https://element.io/download)
- [:simple-apple: macOS](https://element.io/download)
- [:simple-linux: Linux](https://element.io/download)
- [:octicons-browser-16: Web](https://app.element.io)

</details>

</div>

### Choosing a Homeserver

To benefit the most from Matrix, it is critical to choose a homeserver which is well aligned with the subject(s) you want to chat about. We do not currently recommend any specific homeservers, but you may find advice within our communities or third-party resources like [_joinmatrix.org_](https://servers.joinmatrix.org). We recommend avoiding _matrix.org_ because they are operated by the same company which develops Matrix itself. 從去中心化的角度長遠來看，不要使用軟體開發者所控制的伺服器是比較好的做法，這樣就沒有任何一方可以對整個網路施加過多的控制。

### 建議的隱私設定

From Element's web or desktop app, go to :gear: → **All settings** to find these sections:

#### Sessions

By default, when you log in to Element on a new device, the session name will be automatically populated with the Matrix client and platform you used for login. This information may be visible to other users depending on the Matrix client they use.

To prevent revealing information about your personal device to others unnecessarily, consider emptying the session name; this will change the session name to the randomly generated alphanumeric Session ID instead.

#### 偏好設定

- [ ] Uncheck **Send read receipts**
- [ ] Uncheck **Send typing notifications**

You should uncheck these options to reduce the exposure of metadata to other users when chatting in a public room.

#### Voice & Video

- [ ] Uncheck **Allow Peer-to-Peer for 1:1 calls**
- [ ] Uncheck **Allow fallback call assist server (turn.matrix.org)**

If you do decide to use Element for one-to-one communication, we recommend unchecking these settings to prevent the exposure of your IP address to the other party.

#### Security & Privacy

##### Manage integrations (scalar.vector.im)

A Matrix integration manager connects Matrix to third-party services such as bots, bridges, and other enhancements. Element collects information to provide these services to those using an integration manager; you can review its detailed [Privacy Notice](https://element.io/integration-manager-privacy-notice) for the exact information Element collects and the ways it uses such information.

As an end user on a public homeserver, you can consider unchecking the **Enable the integration manager** option, which does not affect the visibility of bots or other third-party services. As a homeserver administrator, consider whether the additional parties with which you share your data are worth the extra functionality.

##### Sessions

- [ ] (Optional) Uncheck **Record the client name, version, and url to recognize sessions for easily in session manager**

Unchecking this option may make it more diffcult to discern your active sessions if you logged in to your Matrix account on multiple devices.

#### 加密

- [x] (Optional) Check **In encrypted rooms, only send messages to verified users**

With this setting enabled, unverified users (i.e., those who have not used the **Verify User** function) and unverified devices of verified users will not receive your messages in a room with encryption enabled. This may limit the messages you can view and the people you can interact with.

## 標準

\*\*請注意，我們與推薦的任何專案均無隸屬關係。\*\*除了[我們的通用標準](about/criteria.md)以外，我們還制定了一套明確的要求，讓我們能夠提供客觀的推薦。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

- Must be free and open-source software.
- 必須使用聯邦式通訊協定與社交網路軟體的其他實例通訊。
- 不得對可聯合的實例有非技術性的限制。
- 必須可在普通的 [網路瀏覽器](desktop-browsers.md) 中使用。
- 必須讓沒有帳號的訪客也能存取公開內容。
- 必須允許使用者限制他人追蹤個人檔案。
- 必須允許使用者張貼只有其追隨者可見的內容。
- 必須支援現代網路應用程式安全標準/功能（包括 [多重要素驗證](multi-factor-authentication.md)）。
