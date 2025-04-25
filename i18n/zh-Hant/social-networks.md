---
title: 社交網路
icon: material/account-supervisor-circle-outline
description: 尋找一個不會窺探您的個人資料或將其貨幣化的新社交網路。
cover: social-networks.webp
---

<small>防護下列威脅：</small>

- [:material-close-outline: 審查](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }
- [:material-account-cash: 監控資本主義](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

這些尊重隱私的 **社交網路** 可讓您參與線上社群，而無須透露您的個人資訊，例如：您的全名、電話號碼，以及科技公司通常要求的其他資料。

社交媒體平台間日益嚴重的問題是兩種不同形式的審查。 首先，他們經常默許非法的審查要求，這些要求可能來自惡意的政府，也可能來自他們自己的內部政策。

其次，它們通常需要帳號才能存取發布在其之上的內容，而這些內容原本可以在開放的網際網路上自由發表。 這有效地審查了注重隱私的使用者的瀏覽活動，因為他們無法支付在這些服務開設帳戶的隱私成本。

我們推薦的社交網路透過開放且分散的社交網路協定來解決審查問題。 雖然您的帳號仍有可能被個別伺服器封禁或隱藏，但沒有中央機關可以在整個網路中審查您的帳號。 檢視公開內容也不需要帳號。

您應該注意，所有社交網路都 **不** 適合私人或敏感的通訊。 若要直接與他人聊天，您應該使用我們推薦—具有強大端對端加密功能的 [即時通訊工具](real-time-communication.md) ，並只使用社交媒體上的直接訊息，以便與聯絡人建立更私密、更安全的聊天平台。

## Mastodon

<div class="admonition recommendation" markdown>

![Mastodon logo](assets/img/social-networks/mastodon.svg){ align=right }

**Mastodon** 是基於開放網路通訊協定和自由及開放原始碼軟體的社交網路。 它使用 **:simple-activitypub: ActivityPub** 通訊協定，就像電子郵件一樣是分散式的：使用者可以存在於不同的伺服器甚至不同的社交平台上，但仍然可以相互溝通。

[:octicons-home-16: 首頁](https://joinmastodon.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.joinmastodon.org){ .card-link title="說明文件" }

</div>

有許多軟體平台使用 ActivityPub 作為其後端社交網路通訊協定，這意味著即使它們執行不同的軟體，也能與伺服器進行通訊。 例如，PeerTube 是使用 ActivityPub 的影片發佈軟體，這表示您可以使用另一個 PeerTube 帳戶追蹤 PeerTube 上的頻道， _或_ 使用 Mastodon 帳戶，因為 Mastodon 也使用 ActivityPub。

基於以下這些原因，我們選擇推薦 Mastodon 而非其他 ActivityPub 軟體作為您的主要社交媒體平台：

1. Mastodon 具有穩固的安全更新歷史。 In the handful of circumstances where major security vulnerabilities have been found, they coordinate patch releases quickly and cleanly. 過去，他們也會將這些安全修補程式回傳到較舊的功能分支。 這讓資歷較淺的伺服器管理員更容易保持實例安全，因為他們可能不習慣立即升級到最新版本。 Mastodon 也在網頁介面中內建了更新通知系統，讓伺服器管理員更有可能知道可用於其實例的重要安全修補程式。

2. 大多數內容類型可用於 Mastodon。 While it is primarily a microblogging platform, Mastodon easily handles longer posts, image posts, video posts, and most other posts you might encounter when following ActivityPub users who aren't on Mastodon. 這讓您的 Mastodon 帳戶成為追蹤任何人的理想「中央樞紐」，不論他們選擇使用何種平台。 In contrast, if you were only using a PeerTube account, you would _only_ be able to follow other video channels, for example.

3. Mastodon 有相當全面的隱私權控制。 它有許多內建功能，可讓您限制是否共享資料和資料共用的方式，以下會介紹其中一些功能。 他們在開發新功能時也會考慮到隱私權。 For example, while other ActivityPub software quickly implemented "quote posts" by merely handling links to other posts with a slightly different embed modal, Mastodon is [developing](https://blog.joinmastodon.org/2025/02/bringing-quote-posts-to-mastodon/) a quote post feature which will give you more fine-grained control when your post is quoted.

### 選擇實例

為了從 Mastodon 獲得最大的效益，選擇一個與您想要張貼或閱讀的內容類型相匹配的伺服器或「實例」是至關重要的。 雖然 Mastodon 中的審查制度不存在於網路層級，但在伺服器層級上卻很有可能遇到審查制度，這取決於您伺服器的管理員。

必須了解的是，Mastodon 並非像 X (Twitter) 或 Facebook 一樣是單一、統一的服務。 每個伺服器都是個別的的法律實體，有自己的隱私權政策、使用條款、管理團隊和版主。 雖然其中許多伺服器比傳統的社交媒體平台限制 _少_ 且更尊重隱私權，但也有些可能限制更 _多_ 或 _可能_ 損害您的隱私。 Mastodon 軟體不會區分這些管理員，也不會對他們的權力施加任何限制。

我們目前不推薦任何特定的實例，但您可以在我們的社群中找到建議。 我們建議避免使用 _mastodon.social_ 和 _mastodon.online_ ，因為它們是由開發 Mastodon 軟體本身的同一家公司所經營。 從去中心化的角度長遠來看，不要使用軟體開發者所控制的伺服器是比較好的做法，這樣就沒有任何一方可以對整個網路施加過多的控制。

如果您非常擔心現有伺服器會審查您發布的內容或您可以檢視的內容，您通常有兩個選擇：

1. **自己託管 Mastodon。** 這種方法可以讓您和任何其他您可以自己託管的網站一樣，具有完全相同的極高抗審查能力。 Mastodon 甚至能 [與 Tor 網路整合](https://docs.joinmastodon.org/admin/optional/tor)，以應付更極端的、甚至您的底層主機供應商也受到審查的情況，但這可能會限制誰可以存取您的內容，只能存取整合 Tor 的其他伺服器，就像其他大多數隱藏服務一樣。

    Mastodon 從龐大且活躍的自助託管社群中獲益良多，其也有極其全面針對管理的說明文件。 雖然許多其他 ActivityPub 平台可能需要豐富的技術知識才能執行和排除故障，但 Mastodon 擁有非常穩定且經過測試的版本，一般來說，任何人只要會使用 Linux 命令列並遵循他們的 [逐步教學](https://docs.joinmastodon.org/admin/prerequisites)，就可以安全無虞地執行它。

2. **Use a managed hosting service.** We don't have any specific recommendations, but there are a variety of Mastodon hosting services which will create a brand-new Mastodon server on your own domain (or occasionally a subdomain of their domain, but we recommend against this unless registering your own domain presents too much of a burden to your privacy).

    Typically, Mastodon hosting providers will handle the _technical_ side of your instance, but they completely leave the _moderation_ side up to you. This means that you will be able to follow any content you like, although it may expose you to more spam or unwanted content because you will not have the dedicated moderation team many larger instances will have.

    This often represents a better approach than self-hosting for most people, because you can benefit from greater control over your own instance without worrying about technical problems or unpatched security vulnerabilities.

    You should look closely at your hosting provider's terms of service and acceptable use policies before registering. These are often far more broad than typical hosted instance rules, and they are far less likely to be enforced without recourse, but they can still be restrictive in undesirable ways.

### 建議的隱私設定

From Mastodon's web interface, click the **Administration** link in the right sidebar. 在管理控制面板中，您可以在左側欄中找到這些區段：

#### Public Profile

There are a number of privacy controls under the **privacy and reach** tab here. Most notably, pay attention to these:

- [ ] **Automatically accept new followers**: You should consider unchecking this box to have a private profile. This will allow you to review who can follow your account before accepting them.

    In contrast to most social media platforms, if you have a private profile you still have the _option_ to publish posts which are publicly visible to non-followers, and which can still be boosted and seen by non-followers. Therefore, unchecking this box is the only way to have the _choice_ to publish to either the entire world or a select group of people.

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
- **Quiet public**, which you should consider equivalent to publicly posting! This is not a technical guarantee, merely a request you are making to other servers to hide your post from some feeds.
- **Followers**, which publishes your content only to your followers. If you did not follow our recommendation of restricting your followers, you should consider this equivalent to publicly posting!
- **Specific people**, which only shares the post with people who are specifically mentioned within the post. This is Mastodon's version of direct messages, but should never be relied on for private communications as we covered earlier, since Mastodon has no E2EE.

If you used our recommended configuration settings above, you should be posting to **Followers** by default, and only posting to **Public** on an intentional and case-by-case basis.

## 標準

\*\*請注意，我們與推薦的任何項目均無關。\*\*除了[我們的通用標準](about/criteria.md)外，我們還制定了一套明確的要求，以便我們能夠提供客觀的建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

- Must be free and open source software.
- Must use a federated protocol to communicate with other instances of the social networking software.
- Must not have non-technical restrictions on who can be federated with.
- Must be usable within a standard [web browser](desktop-browsers.md).
- Must make public content accessible to visitors without an account.
- Must allow you to limit who can follow your profile.
- Must allow you to post content visible only to your followers.
- Must support modern web application security standards/features (including [multifactor authentication](multi-factor-authentication.md)).
