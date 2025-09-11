---
title: 社交網路
icon: material/account-supervisor-circle-outline
description: 尋找一個不會窺探您的個人資料或將其貨幣化的新社交網路。
cover: social-networks.webp
---

<small>防護下列威脅：</small>

- [:material-close-outline: 審查](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }
- [:material-account-cash: 監控資本主義](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

These privacy-respecting **social networks** allow you to participate in online communities without giving up your personal information like your full name, phone number, and other data commonly requested by tech companies.

社交媒體平台間日益嚴重的問題是兩種不同形式的審查。 首先，他們經常默許非法的審查要求，這些要求可能來自惡意的政府，也可能來自他們自己的內部政策。 Second, they often require accounts to access walled-off content that would otherwise be published freely on the open internet; this effectively censors the browsing activities of privacy-conscious users who are unable to pay the privacy cost of opening an account on these networks.

我們推薦的社交網路透過開放且分散的社交網路協定來解決審查問題。 檢視公開內容也不需要帳號。

您應該注意，所有社交網路都 **不** 適合私人或敏感的通訊。 若要直接與他人聊天，您應該使用我們推薦—具有強大端對端加密功能的 [即時通訊工具](real-time-communication.md) ，並只使用社交媒體上的直接訊息，以便與聯絡人建立更私密、更安全的聊天平台。

## Decentralization

Decentralized social networks are built on an architecture that is fundamentally different than mainstream social media platforms, yet quite similar to the underlying structure of email. Instead of opening an account under a single, unified service like you would for Facebook or Discord, you instead choose an independent, public server to join. The server you join can communicate with and discover other servers; this aspect of decentralization is also known as _federation_.

A significant benefit of this decentralized model is that there is no central authority which can censor your account across the entire network, though it is possible for your account to be banned or silenced by an individual server.

A caveat of this decentralized model is that each server is its own legal entity, with its own privacy policy, terms of use, administration team, and moderators. 雖然其中許多伺服器比傳統的社交媒體平台限制 _少_ 且更尊重隱私權，但也有些可能限制更 _多_ 或 _可能_ 損害您的隱私。 Typically, the software on which the social network runs does not discriminate between these administrators or place any limitations on their powers.

## Censorship Resistance

While censorship in decentralized social networks does not exist on a network level, it is very possible to experience censorship on a server level depending on a server's administrator. Administrators have the power to _defederate_ from other servers, which leads to limiting the content you can view and the people you can interact with.

If you are greatly concerned about an existing server censoring your content, the content available to you, or other servers, you generally have two options:

1. **Host the social network software yourself.** This approach gives you the exact same censorship resistance as any other website you can host yourself, which is fairly high.

2. **Use a managed hosting service.** We don't have any specific recommendations, but there are a variety of hosting services which will create a brand-new server on your own domain (or occasionally a subdomain of their domain, but we recommend against this unless registering your own domain presents too much of a burden to your privacy).

   Typically, hosting providers will handle the _technical_ side of your server, but completely leave the _moderation_ side up to you. This often represents a better approach than self-hosting for most people because you can benefit from greater control over your own server without worrying about technical problems or unpatched security vulnerabilities.

   You should look closely at your hosting provider's terms of service and acceptable use policies before registering. These are often far more broad than typical hosted server rules, and they are far less likely to be enforced without recourse, but they can still be restrictive in undesirable ways.

## Mastodon

<div class="admonition recommendation" markdown>

![Mastodon logo](assets/img/social-networks/mastodon.svg){ align=right }

**Mastodon** 是基於開放網路通訊協定和自由及開放原始碼軟體的社交網路。 It uses the **:simple-activitypub: ActivityPub** protocol, which is decentralized like email: Users can exist on different servers or even different platforms but still communicate with each other.

[:octicons-home-16: 首頁](https://joinmastodon.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.joinmastodon.org){ .card-link title="說明文件" }

</div>

有許多軟體平台使用 ActivityPub 作為其後端社交網路通訊協定，這意味著即使它們執行不同的軟體，也能與伺服器進行通訊。 例如，PeerTube 是使用 ActivityPub 的影片發佈軟體，這表示您可以使用另一個 PeerTube 帳戶追蹤 PeerTube 上的頻道， _或_ 使用 Mastodon 帳戶，因為 Mastodon 也使用 ActivityPub。

基於以下這些原因，我們選擇推薦 Mastodon 而非其他 ActivityPub 軟體作為您的主要社交媒體平台：

1. Mastodon 具有穩固的安全更新歷史。 In the handful of circumstances where major security vulnerabilities have been found, they coordinate patch releases quickly and cleanly. 過去，他們也會將這些安全修補程式回傳到較舊的功能分支。 這讓資歷較淺的伺服器管理員更容易保持實例安全，因為他們可能不習慣立即升級到最新版本。 Mastodon 也在網頁介面中內建了更新通知系統，讓伺服器管理員更有可能知道可用於其實例的重要安全修補程式。

2. 大多數內容類型可用於 Mastodon。 While it is primarily a microblogging platform, Mastodon easily handles longer posts, image posts, video posts, and most other posts you might encounter when following ActivityPub users who aren't on Mastodon. 這讓您的 Mastodon 帳戶成為追蹤任何人的理想「中央樞紐」，不論他們選擇使用何種平台。 In contrast, if you were only using a PeerTube account, you would _only_ be able to follow other video channels, for example.

3. Mastodon 有相當全面的隱私權控制。 它有許多內建功能，可讓您限制是否共享資料和資料共用的方式，以下會介紹其中一些功能。 他們在開發新功能時也會考慮到隱私權。 For example, while other ActivityPub software quickly implemented "quote posts" by merely handling links to other posts with a slightly different embed modal, Mastodon is [developing](https://blog.joinmastodon.org/2025/02/bringing-quote-posts-to-mastodon) a quote post feature which will give you more fine-grained control when your post is quoted.

### 選擇實例

為了從 Mastodon 獲得最大的效益，選擇一個與您想要張貼或閱讀的內容類型相匹配的伺服器或「實例」是至關重要的。 我們目前不推薦任何特定的實例，但您可以在我們的社群中找到建議。 我們建議避免使用 _mastodon.social_ 和 _mastodon.online_ ，因為它們是由開發 Mastodon 軟體本身的同一家公司所經營。 從去中心化的角度長遠來看，不要使用軟體開發者所控制的伺服器是比較好的做法，這樣就沒有任何一方可以對整個網路施加過多的控制。

### Recommended Privacy Settings

From Mastodon's web interface, click the **Administration** link in the right sidebar. Within the administration control panel, you'll find these sections in the left sidebar:

#### Public Profile

There are a number of privacy controls under the **privacy and reach** tab here. Most notably, pay attention to these:

- [ ] **Automatically accept new followers**: You should consider unchecking this box to have a private profile. This will allow you to review who can follow your account before accepting them.

  In contrast to most social media platforms, if you have a private profile you still have the _option_ to publish posts which are publicly visible to non-followers and can still be boosted by non-followers. Therefore, unchecking this box is the only way to have the _choice_ to publish to either the entire world or a select group of people.

- [ ] **Show follows and followers on profile**: You should uncheck this box to hide your social graph from the public. It is fairly uncommon for the list of people you follow to have some genuine benefit to others, but that information can present a risk to you.

- [ ] **Display from which app you sent a post**: You should uncheck this box to prevent revealing information about your personal computing setup to others unnecessarily.

The other privacy controls on this page should be read through, but we would stress that they are **not** technical controls—they are merely requests that you make to others. For example, if you choose to hide your profile from search engines on this page, **nothing** is actually stopping a search engine from reading your profile. You are merely requesting search engine indexes not publish your content to their users.

You will likely still wish to make these requests because they can practically reduce your digital footprint. However, they should not be _relied_ upon. The only effective way to hide your posts from search engines and others is to post with non-public (followers only) visibility settings _and_ limit who can follow your account.

#### Preferences

You should change your **posting privacy** setting from public to: **Followers-only - Only show to followers**.

Note that this only changes your default settings to prevent accidental over-sharing. You can always adjust your visibility level when composing a new post.

#### Automated post deletion

- [x] Check the **Automatically delete old posts** box.

The default settings here are fine, and will delete any posts you make after 2 weeks, unless you favorite (star) them. This gives you an easy way to control which posts stick around forever, and which ones are only ephemeral. Many settings about how long and when posts are kept can be adjusted here to suit your own needs, however.

It is very rare for social media posts older than a few weeks to be read or relevant to others. These older posts are often ignored because they are challenging to deal with in bulk, but they can build a fairly comprehensive profile about you over time. You should always strive to publish content ephemerally by default, and only keep posts around for longer than that very intentionally.

### Posting Content

When publishing a new post, you will have the option to choose from one of these visibility settings:

- **Public**, which publishes your content to anyone on the internet.
- **Quiet public**, which you should consider equivalent to publicly posting! This is not a technical guarantee, but merely a request you are making to other servers to hide your post from some feeds.
- **Followers**, which publishes your content only to your followers. If you did not follow our recommendation of restricting your followers, you should consider this equivalent to publicly posting!
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

<details class="downloads" markdown><summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=im.vector.app)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1083446067)
- [:simple-github: GitHub](https://github.com/element-hq/element-android/releases)
- [:fontawesome-brands-windows: Windows](https://element.io/download)
- [:simple-apple: macOS](https://element.io/download)
- [:simple-linux: Linux](https://element.io/download)
- [:octicons-browser-16: Web](https://app.element.io)

</details>

</div>

### Choosing a Homeserver

To benefit the most from Matrix, it is critical to choose a homeserver which is well aligned with the subject(s) you want to chat about. We do not currently recommend any specific homeservers, but you may find advice within our communities or third-party resources like [_joinmatrix.org_](https://servers.joinmatrix.org). We recommend avoiding _matrix.org_ because they are operated by the same company which develops Matrix itself. 從去中心化的角度長遠來看，不要使用軟體開發者所控制的伺服器是比較好的做法，這樣就沒有任何一方可以對整個網路施加過多的控制。

### Recommended Privacy Settings

From Element's web or desktop app, go to :gear: → **All settings** to find these sections:

#### Sessions

By default, when you log in to Element on a new device, the session name will be automatically populated with the Matrix client and platform you used for login. This information may be visible to other users depending on the Matrix client they use.

To prevent revealing information about your personal device to others unnecessarily, consider emptying the session name; this will change the session name to the randomly generated alphanumeric Session ID instead.

#### Preferences

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

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

- Must be free and open-source software.
- 必須使用聯邦式通訊協定與社交網路軟體的其他實例通訊。
- 不得對可聯合的實例有非技術性的限制。
- 必須可在普通的 [網路瀏覽器](desktop-browsers.md) 中使用。
- 必須讓沒有帳號的訪客也能存取公開內容。
- 必須允許使用者限制他人追蹤個人檔案。
- 必須允許使用者張貼只有其追隨者可見的內容。
- 必須支援現代網路應用程式安全標準/功能（包括 [多重要素驗證](multi-factor-authentication.md)）。
