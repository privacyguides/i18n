---
title: "前端"
icon: material/flip-to-front
description: 這些用在各式網際網路服務的開源前端，可讓您訪問內容而無需 JavaScript 或其他干援。
cover: frontends.webp
---

有時，某些服務會以煩人的彈出窗口來封鎖訪問內容，強迫訪客須註冊帳戶。 如果不啓用JavaScript ，也可能會中斷。 這些前端可以讓您避開這些限制。

如您選擇自行託管這些前端，要緊的是讓別人可以使用您的實例，才能讓您融入其中。 對於在何處與如何託管實例，您該謹慎處之，尤其當有其它人的使用會連結到您的託管。

當您使用其它人的實例，請確認有細讀此實例的隱私政策。 它們可以任擁有者修改因此不必然反映原本預設的政策。 有些實例有[Tor](tor.md) .onion地址，只要您的搜尋查詢不包含PII ，這些地址可以保護某些隱私。

## Reddit

### Redlib

<div class="admonition recommendation" markdown>

![Redlib logo](assets/img/frontends/redlib.svg){ align=right }

**Redlib** 是 [Reddit](https://reddit.com) 的開源前端，也可自行託管。

有許多公共實例，其中一些實例支援 [Tor](tor.md) onion 服務。

[:octicons-repo-16: Repository](https://github.com/redlib-org/redlib){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/redlib-org/redlib-instances/blob/main/instances.md){ .card-link title="Public Instances"}
[:octicons-info-16:](https://github.com/redlib-org/redlib?tab=readme-ov-file#table-of-contents){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/redlib-org/redlib){ .card-link title="Source Code" }

</div>

<div class="admonition note" markdown>
<p class="admonition-title">Note "備註"</p>

[舊版 Reddit](https://old.reddit.com) 網站不需要像新 Reddit 網站使用過多的 JavaScript，但它最近阻止了為公共 VPN 保留的 IP 位址的存取。 您可以將舊Reddit 給合[2022年10月](https://forum.torproject.org/t/reddit-onion-service-launch/5305)所推出的[Tor](tor.md) Onion ，載取點 [https://old.reddittorjg6rue252oqsxryoxengawnmo46qy4kyii5wtqnwfj4ooad.onion](https://old.reddittorjg6rue252oqsxryoxengawnmo46qy4kyii5wtqnwfj4ooad.onion).

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">溫馨提示</p>

如果想在瀏覽器中禁用 JavaScript ，例如 [Tor瀏覽器](tor.md#tor-browser/) 最安全級別， Redlib 非常實用。
</div>

## TikTok

### ProxiTok

<div class="admonition recommendation" markdown>

![ProxiTok logo](assets/img/frontends/proxitok.svg){ align=right }

**ProxiTok** 是 [TikTok](https://tiktok.com)網站的開源前端，也可自主託管。

有許多公共實例，其中一些實例支援 [Tor](tor.md) onion 服務。

[:octicons-repo-16: Repository](https://github.com/pablouser1/ProxiTok){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/pablouser1/ProxiTok/wiki/Public-instances){ .card-link title="Public Instances"}
[:octicons-info-16:](https://github.com/pablouser1/ProxiTok/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/pablouser1/ProxiTok){ .card-link title="Source Code" }

</details>

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">溫馨提示</p>

如果想在瀏覽器中禁用 JavaScript ，例如 [Tor瀏覽器](tor.md#tor-browser/) 最安全級別， ProxiTok 非常有用。

</div>

## YouTube

### FreeTube

<div class="admonition recommendation" markdown>

![FreeTube logo](assets/img/frontends/freetube.svg){ align=right }

**FreeTube** 是 [YouTube](https://youtube.com)的免費開源桌面應用程式。 使用 FreeTube 時，訂閱清單和播放列表會在本地儲存在 本地裝置上。

預設情況下， FreeTube 會封鎖所有 YouTube 廣告。 此外， FreeTube 可選擇與 [SponsorBlock](https://sponsor.ajay.app) 整合，可以跳過贊助的影片段。

[:octicons-home-16: Homepage](https://freetubeapp.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://freetubeapp.io/privacy.php){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.freetubeapp.io){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/FreeTubeApp/FreeTube){ .card-link title="Source Code" }
[:octicons-heart-16:](https://liberapay.com/FreeTube){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://freetubeapp.io/#download)
- [:simple-apple: macOS](https://freetubeapp.io/#download)
- [:simple-linux: Linux](https://freetubeapp.io/#download)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/io.freetubeapp.FreeTube)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

When using FreeTube, your IP address may still be known to YouTube, [Invidious](https://instances.invidious.io), or [SponsorBlock](https://sponsor.ajay.app) depending on your configuration. 如果您的 [威脅模型](basics/threat-modeling.md) 需要隱藏您的IP 位址，請考慮使用 [VPN](vpn.md)或 [Tor](tor.md)。

</div>

### Yattee

<div class="admonition recommendation" markdown>

![Yattee logo](assets/img/frontends/yattee.svg){ align=right }

**Yattee** is a free and open-source privacy oriented video player for iOS, tvOS, and macOS for [YouTube](https://youtube.com). When using Yattee, your subscription list is saved locally on your device.

You will need to take a few [extra steps](https://web.archive.org/web/20230330122839/https://gonzoknows.com/posts/Yattee) before you can use Yattee to watch YouTube, due to App Store restrictions.

[:octicons-home-16: Homepage](https://github.com/yattee/yattee){ .md-button .md-button--primary }
[:octicons-eye-16:](https://r.yattee.stream/docs/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/yattee/yattee/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/yattee/yattee){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/yattee/yattee/wiki/Donations){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-apple: App Store](https://apps.apple.com/app/id1595136629)
- [:simple-github: GitHub](https://github.com/yattee/yattee/releases)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

When using Yattee, your IP address may still be known to YouTube, [Invidious](https://instances.invidious.io), [Piped](https://github.com/TeamPiped/Piped/wiki/Instances), or [SponsorBlock](https://sponsor.ajay.app) depending on your configuration. 如果您的 [威脅模型](basics/threat-modeling.md) 需要隱藏您的IP 位址，請考慮使用 [VPN](vpn.md)或 [Tor](tor.md)。

</div>

預設情況下， Yattee 會封鎖所有 YouTube 廣告。 此外， Yattee 可選擇與 [SponsorBlock](https://sponsor.ajay.app) 整合，可以跳過贊助的影片段。

### LibreTube (Android)

<div class="admonition recommendation" markdown>

![LibreTube logo](assets/img/frontends/libretube.svg#only-light){ align=right }
![LibreTube logo](assets/img/frontends/libretube-dark.svg#only-dark){ align=right }

**LibreTube** 是一款免費的 [YouTube](https://youtube.com)開源Android應用程序，使用 [Piped](# piped) API。

LibreTube 可將訂閱列表和播放列表存儲於 Android 設備，或者存儲到您選擇的 Piped 實例帳戶，以便利用其他設備無縫訪問。

[:octicons-home-16: Homepage](https://libretube.dev){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/libre-tube/LibreTube/blob/master/PRIVACY_POLICY.md){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://libretube.dev/#faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/libre-tube/LibreTube){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/libre-tube/LibreTube#donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-github: GitHub](https://github.com/libre-tube/LibreTube/releases)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

使用 LibreTube 時，IP 位址會為所用的 [Piped](https://github.com/TeamPiped/Piped/wiki/Instances)實例和 [SponsorBlock](https://sponsor.ajay.app)看見，具體取決於您的設定。 如果您的 [威脅模型](basics/threat-modeling.md) 需要隱藏您的IP 位址，請考慮使用 [VPN](vpn.md)或 [Tor](tor.md)。

</div>

預設情況下， LibreTube 會封鎖所有 YouTube 廣告。 此外， LibreTube 利用[SponsorBlock](https://sponsor.ajay.app) 來跳過贊助的影片段。 可以自行配置 SponsorBlock 要跳過的影片段類型，或完全禁用它。 播放器上有一個按鈕，如果需要，可以為特定影片禁用它。

### NewPipe (Android)

<div class="admonition recommendation annotate" markdown>

![Newpipe logo](assets/img/frontends/newpipe.svg){ align=right }

**NewPipe** 是 [YouTube](https://youtube.com)、 [SoundCloud](https://soundcloud.com)、 [media.ccc.de](https://media.ccc.de)、 [Bandcamp](https://bandcamp.com)和 [PeerTube](https://joinpeertube.org) (1)的免費開源 Android應用程式。

訂閱清單和播放列表會儲存在本地的 Android裝置。

[:octicons-home-16: Homepage](https://newpipe.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://newpipe.net/legal/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://newpipe.net/FAQ){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/TeamNewPipe/NewPipe){ .card-link title="Source Code" }
[:octicons-heart-16:](https://newpipe.net/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-github: GitHub](https://github.com/TeamNewPipe/NewPipe/releases)

</details>

</div>

1. 預設實例為 [FramaTube](https://framatube.org)，但可在 **Settings** → **Content** → **PeerTube instance ** 添加更多實例。

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

使用NewPipe時，IP 位址會被所使用的影片供應商看見。 如果您的 [威脅模型](basics/threat-modeling.md) 需要隱藏您的IP 位址，請考慮使用 [VPN](vpn.md)或 [Tor](tor.md)。

</div>

### Invidious

<div class="admonition recommendation" markdown>

![Invidious logo](assets/img/frontends/invidious.svg#only-light){ align=right }
![Invidious logo](assets/img/frontends/invidious-dark.svg#only-dark){ align=right }

**Invidious** 是 [YouTube](https://youtube.com)的免費開源前端，也可自行託管。

有許多公共實例，其中一些實例支援 [Tor](tor.md) onion 服務。

[:octicons-home-16: Homepage](https://invidious.io){ .md-button .md-button--primary }
[:octicons-server-16:](https://instances.invidious.io){ .card-link title="Public Instances"}
[:octicons-info-16:](https://docs.invidious.io){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/iv-org/invidious){ .card-link title="Source Code" }
[:octicons-heart-16:](https://invidious.io/donate){ .card-link title=Contribute }

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

預設情況下， Invidious不會代理影片串流。 通過 Invidious 觀看的影片會直接連接到 Google 伺服器（例如`googlevideo.com`)，但是有些實例支持影片代理-只需在實例設置中啟用*Proxy videos*或在 URL 中添加`&local = true`。

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">溫馨提示</p>

如果您想在瀏覽器中停用JavaScript ，例如 [Tor瀏覽器](tor.md#tor-browser)最安全級別，Invidious 非常有用。 它本身不提供隱私，故不建議登入任何帳戶。

</div>

### Piped

<div class="admonition recommendation" markdown>

![Piped logo](assets/img/frontends/piped.svg){ align=right }

**Piped** 是 [YouTube](https://youtube.com)的免費開源前端，也是可自主託管。

Piped 需要JavaScript 才能運行，它有許多公共實例。

[:octicons-repo-16: Repository](https://github.com/TeamPiped/Piped){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/TeamPiped/Piped/wiki/Instances){ .card-link title="Public Instances"}
[:octicons-info-16:](https://docs.piped.video/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/TeamPiped/Piped){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/TeamPiped/Piped#donations){ .card-link title=Contribute }

</details>

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">溫馨提示</p>

如果您想使用 [SponsorBlock](https://sponsor.ajay.app)但不安裝瀏覽器擴展或在不登入帳戶訪問有年齡限制的內容， Piped 非常有用。 它本身不提供隱私，故不建議登入任何帳戶。

</div>

## 標準

**請注意，我們所推薦專案沒有任何瓜葛。 ** 除了 [標準準則](about/criteria.md)外，我們還發展出一套明確要求以提出客觀建議。 建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

推薦的前端…

- 必須是開源軟體。
- 必須是可自行託管。
- 必須提供匿名訪客完整的網站基本功能。

我們只考慮符合以下條件的前端平台：

- 通常只能在啟用 JavaScript 的情況下才能存取。
- 通常只能透過帳戶存取。
- 封鎖商業 [VPN](vpn.md) 的存取。
