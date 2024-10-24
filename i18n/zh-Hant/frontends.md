---
title: "前端"
icon: material/flip-to-front
description: 這些用在各式網際網路服務的開源前端，可讓您訪問內容而無需 JavaScript 或其他干援。
cover: frontends.webp
---

<small>防護下列威脅：</small>

- [:material-account-cash: 監控資本主義](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

有時，某些服務會以煩人的彈出窗口來封鎖訪問內容，強迫訪客須註冊帳戶。 如果不啓用JavaScript ，也可能會中斷。 These frontends can allow you to circumvent these restrictions.

如您選擇自行託管這些前端，要緊的是讓別人可以使用您的實例，才能讓您融入其中。 您應該謹慎處理託管的地點和方式，因為其他人如何使用將會影響到您的託管。

When you are using an instance run by someone else, make sure to read the privacy policy of that specific instance (if available). 它們可以任擁有者修改因此不必然反映原本預設的政策。 Some instances have [Tor](tor.md) .onion addresses, which may grant some privacy as long as your search queries don't contain personally identifiable information.

## Reddit

### Redlib

<div class="admonition recommendation" markdown>

![Redlib logo](assets/img/frontends/redlib.svg){ align=right }

**Redlib** 是 [Reddit](https://reddit.com) 的開源前端，也可自行託管。 You can access Redlib through a number of public instances.

[:octicons-repo-16: Repository](https://github.com/redlib-org/redlib){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/redlib-org/redlib-instances/blob/main/instances.md){ .card-link title="Public Instances" }
[:octicons-info-16:](https://github.com/redlib-org/redlib?tab=readme-ov-file#table-of-contents){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/redlib-org/redlib){ .card-link title="Source Code" }

</div>

<div class="admonition note" markdown>
<p class="admonition-title">備註</p>

[舊版 Reddit](https://old.reddit.com) 網站不需要像新 Reddit 網站使用過多的 JavaScript，但它最近阻止了對公共 VPN 所使用的 IP 位址的存取。 您可以將 舊界面 Reddit 與他們在 [2022 年 10 月推出](https://forum.torproject.org/t/reddit-onion-service-launch/5305) 的 [Tor](tor.md) 洋蔥服務： [https://old.reddittorjg6rue252oqsxryoxengawnmo46qy4kyii5wtqnwfj4ooad.onion](https://old.reddittorjg6rue252oqsxryoxengawnmo46qy4kyii5wtqnwfj4ooad.onion) 結合使用。

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">溫馨提示</p>

如果想在瀏覽器中禁用 JavaScript ，例如 [Tor瀏覽器](tor.md#tor-browser/) 的 最安全級別， Redlib 非常實用。

</div>

## TikTok

### ProxiTok

<div class="admonition recommendation" markdown>

![ProxiTok logo](assets/img/frontends/proxitok.svg){ align=right }

**ProxiTok** 是 [TikTok](https://tiktok.com)網站的開源前端，也可自主託管。

There are a number of public instances, with some that offer a [Tor](tor.md) onion service or an [I2P](alternative-networks.md#i2p-the-invisible-internet-project) eepsite.

[:octicons-repo-16: Repository](https://github.com/pablouser1/ProxiTok){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/pablouser1/ProxiTok/wiki/Public-instances){ .card-link title="Public Instances" }
[:octicons-info-16:](https://github.com/pablouser1/ProxiTok/wiki){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/pablouser1/ProxiTok){ .card-link title="Source Code" }

</details>

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">溫馨提示</p>

如果想在瀏覽器中禁用 JavaScript ，例如 [Tor瀏覽器](tor.md#tor-browser/) 最安全級別， ProxiTok 非常有用。

</div>

## YouTube

**Note:** YouTube has gradually rolled out changes to its video player and API that have thwarted some of the methods used by third-party frontends for extracting YouTube data. If you experience reliability issues with one YouTube frontend, consider trying out another that uses a different extraction method.

### Invidious

<div class="admonition recommendation" markdown>

![Invidious logo](assets/img/frontends/invidious.svg#only-light){ align=right }
![Invidious logo](assets/img/frontends/invidious-dark.svg#only-dark){ align=right }

**Invidious** 是 [YouTube](https://youtube.com)的免費開源前端，也可自行託管。

There are a number of public instances, with some that offer a [Tor](tor.md) onion service or an [I2P](alternative-networks.md#i2p-the-invisible-internet-project) eepsite.

[:octicons-home-16: Homepage](https://invidious.io){ .md-button .md-button--primary }
[:octicons-server-16:](https://instances.invidious.io){ .card-link title="Public Instances" }
[:octicons-info-16:](https://docs.invidious.io){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/iv-org/invidious){ .card-link title="Source Code" }
[:octicons-heart-16:](https://invidious.io/donate){ .card-link title="Contribute" }

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

預設情況下， Invidious不會代理影片串流。 通過 Invidious 觀看的影片會直接連接到 Google 伺服器（例如`googlevideo.com`)，但是有些實例支持影片代理-只需在實例設置中啟用*Proxy videos*或在 URL 中添加`&local = true`。

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">溫馨提示</p>

如果您想在瀏覽器中停用JavaScript ，例如 [Tor瀏覽器](tor.md#tor-browser) 的最安全級別，Invidious 非常有用。 它本身並不保證您的隱私，故不建議登入任何帳戶。

</div>

### Piped

<div class="admonition recommendation" markdown>

![Piped logo](assets/img/frontends/piped.svg){ align=right }

**Piped** 是 [YouTube](https://youtube.com)的自由及開放原始碼前端，同樣可自主託管。

Piped 需要 JavaScript 才能運行，它有許多公共伺服器。

[:octicons-repo-16: Repository](https://github.com/TeamPiped/Piped){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/TeamPiped/Piped/wiki/Instances){ .card-link title="Public Instances" }
[:octicons-info-16:](https://docs.piped.video/docs){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/TeamPiped/Piped){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/TeamPiped/Piped#donations){ .card-link title="Contribute" }

</details>

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">溫馨提示</p>

如果您想在不安裝擴充套件的情況下使用 [SponsorBlock](https://sponsor.ajay.app) ，Piped 會很有用。 它本身並不保證您的隱私，故不建議登入任何帳戶。

</div>

### FreeTube

<div class="admonition recommendation" markdown>

![FreeTube logo](assets/img/frontends/freetube.svg){ align=right }

**FreeTube** 是 [YouTube](https://youtube.com)的免費開源桌面應用程式。 FreeTube extracts data from YouTube using its built-in API based on [YouTube.js](https://github.com/LuanRT/YouTube.js) or the [Invidious](#invidious) API. You can configure either as the default, with the other serving as a fallback.

使用 FreeTube 時，訂閱清單和播放列表會在本地儲存在 本地裝置上。

[:octicons-home-16: Homepage](https://freetubeapp.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://freetubeapp.io/privacy.php){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.freetubeapp.io){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/FreeTubeApp/FreeTube){ .card-link title="Source Code" }
[:octicons-heart-16:](https://liberapay.com/FreeTube){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:fontawesome-brands-windows: Windows](https://freetubeapp.io/#download)
- [:simple-apple: macOS](https://freetubeapp.io/#download)
- [:simple-linux: Linux](https://freetubeapp.io/#download)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/io.freetubeapp.FreeTube)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

使用 FreeTube 時，YouTube、 [Invidious](https://instances.invidious.io) 或 [SponsorBlock](https://sponsor.ajay.app) 仍可能知道您的 IP 位址，具體取決於您的設定。 如果您的 [威脅模型](basics/threat-modeling.md) 需要隱藏您的IP 位址，請考慮使用 [VPN](vpn.md) 或 [Tor](tor.md)。

</div>

預設情況下， FreeTube 會封鎖所有 YouTube 廣告。 In addition, FreeTube optionally integrates with [SponsorBlock](https://sponsor.ajay.app) to help you skip sponsored video segments.

### Yattee

<div class="admonition recommendation" markdown>

![Yattee logo](assets/img/frontends/yattee.svg){ align=right }

**Yattee** 是 iOS、tvOS 和 macOS 適用於 [YouTube](https://youtube.com) 的自由、開放原始碼、以隱私為重點的影片播放器。 Due to App Store restrictions, you will need to take a few [extra steps](https://web.archive.org/web/20230330122839/https://gonzoknows.com/posts/Yattee) before you can use Yattee to watch YouTube. Yattee allows you to connect to instances of [Invidious](#invidious) or [Piped](#piped).

使用 Yattee 時，您的訂閱清單會儲存在本機裝置上。

[:octicons-home-16: Homepage](https://github.com/yattee/yattee){ .md-button .md-button--primary }
[:octicons-eye-16:](https://r.yattee.stream/docs/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/yattee/yattee/wiki){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/yattee/yattee){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/yattee/yattee/wiki/Donations){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-apple: App Store](https://apps.apple.com/app/id1595136629)
- [:simple-github: GitHub](https://github.com/yattee/yattee/releases)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

使用 Yattee 時，您的 IP位址 可能仍會被 YouTube、 [Invidious](https://instances.invidious.io) 、 [Piped](https://github.com/TeamPiped/Piped/wiki/Instances) 或 [SponsorBlock](https://sponsor.ajay.app) 所知曉，具體取決於您的設定。 如果您的 [威脅模型](basics/threat-modeling.md) 需要隱藏您的IP 位址，請考慮使用 [VPN](vpn.md) 或 [Tor](tor.md)。

</div>

預設情況下， Yattee 會封鎖所有 YouTube 廣告。 此外， Yattee 可選擇與 [SponsorBlock](https://sponsor.ajay.app) 整合，可以跳過贊助的影片段。

### LibreTube (Android)

<div class="admonition recommendation" markdown>

![LibreTube logo](assets/img/frontends/libretube.svg#only-light){ align=right }
![LibreTube logo](assets/img/frontends/libretube-dark.svg#only-dark){ align=right }

**LibreTube** 是一款免費的 [YouTube](https://youtube.com)開源Android應用程序，使用 [Piped](# piped) API。

訂閱清單和播放列表會儲存在本地的 Android 裝置上。

[:octicons-home-16: Homepage](https://libretube.dev){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/libre-tube/LibreTube/blob/master/PRIVACY_POLICY.md){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://libretube.dev/#faq){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/libre-tube/LibreTube){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/libre-tube/LibreTube#donate){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-github: GitHub](https://github.com/libre-tube/LibreTube/releases)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

When using LibreTube, your IP address will be visible to YouTube, [Piped](https://github.com/TeamPiped/Piped/wiki/Instances), or [SponsorBlock](https://sponsor.ajay.app) depending on your configuration. 如果您的 [威脅模型](basics/threat-modeling.md) 需要隱藏您的IP 位址，請考慮使用 [VPN](vpn.md) 或 [Tor](tor.md)。

</div>

預設情況下， LibreTube 會封鎖所有 YouTube 廣告。 此外， LibreTube 利用[SponsorBlock](https://sponsor.ajay.app) 來跳過贊助的影片段。 可以自行配置 SponsorBlock 要跳過的影片段類型，或完全禁用它。 播放器上有一個按鈕，如果需要，可以為特定影片禁用它。

### NewPipe (Android)

<div class="admonition recommendation annotate" markdown>

![Newpipe logo](assets/img/frontends/newpipe.svg){ align=right }

**NewPipe** 是自由及開放原始碼的 Android 應用程式，可用於觀看 [YouTube](https://youtube.com)、 [SoundCloud](https://soundcloud.com)、 [media.ccc.de](https://media.ccc.de)、 [Bandcamp](https://bandcamp.com)和 [PeerTube](https://joinpeertube.org) (1)。

訂閱清單和播放列表會儲存在本地的 Android 裝置上。

[:octicons-home-16: Homepage](https://newpipe.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://newpipe.net/legal/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://newpipe.net/FAQ){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/TeamNewPipe/NewPipe){ .card-link title="Source Code" }
[:octicons-heart-16:](https://newpipe.net/donate){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-github: GitHub](https://github.com/TeamNewPipe/NewPipe/releases)

</details>

</div>

1. The default instance is [FramaTube](https://framatube.org), however more can be added via **Settings** → **Content** → **PeerTube instances**.

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

使用NewPipe時，IP 位址會被所使用的影片供應商看見。 如果您的 [威脅模型](basics/threat-modeling.md) 需要隱藏您的IP 位址，請考慮使用 [VPN](vpn.md) 或 [Tor](tor.md)。

</div>

## 標準

**請注意，我們所推薦專案沒有任何瓜葛。 ** 除了 [標準準則](about/criteria.md)外，我們還發展出一套明確要求以提出客觀建議。 建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

我們只會在平台符合下列條件之一時，才會考慮前端：

- 通常只有在啟用 JavaScript 的情況下才能存取。
- 通常必須登入帳戶才能存取。
- 封鎖商業 [VPN](vpn.md) 的存取。

推薦的前端…

- 必須是開源軟體。
- 必須可自行託管。
- 必須提供匿名訪客完整的網站基本功能。
