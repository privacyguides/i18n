---
title: "前端"
icon: material/flip-to-front
description: These open-source frontends for various internet services allow you to access content without JavaScript or other annoyances.
cover: frontends.webp
---

有時，某些服務會以煩人的彈出窗口來封鎖訪問內容，強迫訪客須註冊帳戶。 如果不啓用JavaScript ，也可能會中斷。 這些前端可以讓您避開這些限制。

如您選擇自行託管這些前端，要緊的是讓別人可以使用您的實例，才能讓您融入其中。 對於在何處與如何託管實例，您該謹慎處之，尤其當有其它人的使用會連結到您的託管。

當您使用其它人的實例，請確認有細讀此實例的隱私政策。 它們可以任擁有者修改因此不必然反映原本預設的政策。 有些實例有Tor .onion地址，只要您的搜尋查詢不包含PII ，這些地址可以保護某些隱私。

## TikTok

### ProxiTok

<div class="admonition recommendation" markdown>

![ProxiTok logo](assets/img/frontends/proxitok.svg){ align=right }

**ProxiTok** 是 [TikTok](https://www.tiktok.com)網站的開源前端，也可自主託管。

有許多公共實例，其中一些實例支援 [Tor](https://www.torproject.org) onion 服務。

[:octicons-repo-16: Repository](https://github.com/pablouser1/ProxiTok){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/pablouser1/ProxiTok/wiki/Public-instances){ .card-link title="Public Instances"}
[:octicons-info-16:](https://github.com/pablouser1/ProxiTok/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/pablouser1/ProxiTok){ .card-link title="Source Code" }

</details>

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

如果想在瀏覽器中禁用 JavaScript ，例如 [Tor瀏覽器](https://www.torproject.org/) 最安全級別， ProxiTok 非常有用。

</div>

## YouTube

### FreeTube

<div class="admonition recommendation" markdown>

![FreeTube logo](assets/img/frontends/freetube.svg){ align=right }

**FreeTube** 是 [YouTube](https://youtube.com)的免費開源桌面應用程式。 使用 FreeTube 時，訂閱清單和播放列表會在本地儲存在 本地裝置上。

預設情況下， FreeTube 會封鎖所有 YouTube 廣告。 此外， FreeTube 可選擇與 [SponsorBlock](https://sponsor.ajay.app) 整合，可以跳過贊助的影片段。

[:octicons-home-16: Homepage](https://freetubeapp.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://freetubeapp.io/privacy.php){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.freetubeapp.io/){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/FreeTubeApp/FreeTube){ .card-link title="Source Code" }
[:octicons-heart-16:](https://liberapay.com/FreeTube){ .card-link title=Contribute }
    
<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://freetubeapp.io/#download)
- [:simple-apple: macOS](https://freetubeapp.io/#download)
- [:simple-linux: Linux](https://freetubeapp.io/#download)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/io.freetubeapp.FreeTube)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning "警告"</p>

使用 FreeTube 時，IP 位址可能會被 YouTube、[Invidious](https://instances.invidious.io)或 [SponsorBlock](https://sponsor.ajay.app/) 所知，具體取決於您的設定。 如果您的 [威脅模型](basics/threat-modeling.md) 需要隱藏您的IP 位址，請考慮使用 [VPN](vpn.md) 或 [Tor](https://www.torproject.org)。

</div>

### Yattee

<div class="admonition recommendation" markdown>

![Yattee logo](assets/img/frontends/yattee.svg){ align=right }

**Yattee** 是一款免費的開源隱私導向影片播放器，適用於iOS、tvOS 和 macOS 觀看 [YouTube](https://youtube.com)。 使用 Yattee 時，訂閱清單和播放列表會儲存在 本地裝置上。

由於 App Store 限制，您需要採取一些[額外步驟](https://gonzoknows.com/posts/Yattee/) 才能使用 Yattee 觀看YouTube。

[:octicons-home-16: Homepage](https://github.com/yattee/yattee){ .md-button .md-button--primary }
[:octicons-eye-16:](https://r.yattee.stream/docs/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/yattee/yattee/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/yattee/yattee){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/yattee/yattee/wiki/Donations){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-apple: App Store](https://apps.apple.com/us/app/yattee/id1595136629)
- [:simple-github: GitHub](https://github.com/yattee/yattee/releases)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning "警告"</p>

使用 Yattee 時，IP位址可能仍會被 YouTube、 [Invidious](https://instances.invidious.io)、 [Piped](https://github.com/TeamPiped/Piped/wiki/Instances)或 [SponsorBlock](https://sponsor.ajay.app/)所知曉，具體取決於您的設定。 如果您的 [威脅模型](basics/threat-modeling.md)需要隱藏您的IP 位址，請考慮使用 [VPN](vpn.md)或 [Tor](https://www.torproject.org)。

</div>

預設情況下， Yattee 會封鎖所有 YouTube 廣告。 此外， Yattee 可選擇與 [SponsorBlock](https://sponsor.ajay.app) 整合，可以跳過贊助的影片段。

### LibreTube (Android)

<div class="admonition recommendation" markdown>

![LibreTube logo](assets/img/frontends/libretube.svg#only-light){ align=right }
![LibreTube logo](assets/img/frontends/libretube-dark.svg#only-dark){ align=right }

**LibreTube** 是一款免費的 [YouTube](https://youtube.com)開源Android應用程序，使用 [Piped](# piped) API。

LibreTube 可將訂閱列表和播放列表存儲於 Android 設備，或者存儲到您選擇的 Piped 實例帳戶，以便利用其他設備無縫訪問。

[:octicons-home-16: Homepage](https://libre-tube.github.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/libre-tube/LibreTube#privacy-policy-and-disclaimer){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/libre-tube/LibreTube#readme){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/libre-tube/LibreTube){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/libre-tube/LibreTube/releases)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning "警告"</p>

使用 LibreTube 時，IP 位址會為所用的 [Piped](https://github.com/TeamPiped/Piped/wiki/Instances)實例和 [SponsorBlock](https://sponsor.ajay.app/)看見，具體取決於您的設定。 如果您的 [威脅模型](basics/threat-modeling.md) 需要隱藏您的IP 位址，請考慮使用 [VPN](vpn.md)或 [Tor](https://www.torproject.org)。

</div>

預設情況下， LibreTube 會封鎖所有 YouTube 廣告。 此外， LibreTube 利用[SponsorBlock](https://sponsor.ajay.app) 來跳過贊助的影片段。 可以自行配置 SponsorBlock 要跳過的影片段類型，或完全禁用它。 播放器上有一個按鈕，如果需要，可以為特定影片禁用它。

### NewPipe (Android)

<div class="admonition recommendation annotate" markdown>

![Newpipe logo](assets/img/frontends/newpipe.svg){ align=right }

**NewPipe** 是 [YouTube](https://youtube.com)、 [SoundCloud](https://soundcloud.com)、 [media.ccc.de](https://media.ccc.de)、 [Bandcamp](https://bandcamp.com)和 [PeerTube](https://joinpeertube.org/) (1)的免費開源 Android應用程式。

訂閱清單和播放列表會儲存在本地的 Android裝置。

[:octicons-home-16: Homepage](https://newpipe.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://newpipe.net/legal/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://teamnewpipe.github.io/documentation/){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/TeamNewPipe/NewPipe){ .card-link title="Source Code" }
[:octicons-heart-16:](https://newpipe.net/donate/){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/TeamNewPipe/NewPipe/releases)

</details>

</div>

1. 預設實例為 [FramaTube](https://framatube.org/)，但可在 **Settings** → **Content** → **PeerTube instance ** 添加更多實例。

<div class="admonition warning" markdown>
<p class="admonition-title">Warning "警告"</p>

使用NewPipe時，IP 位址會被所使用的影片供應商看見。 如果您的 [威脅模型](basics/threat-modeling.md) 需要隱藏您的IP 位址，請考慮使用 [VPN](vpn.md)或 [Tor](https://www.torproject.org)。

</div>

### Invidious

<div class="admonition recommendation" markdown>

![Invidious logo](assets/img/frontends/invidious.svg#only-light){ align=right }
![Invidious logo](assets/img/frontends/invidious-dark.svg#only-dark){ align=right }

**Invidious** 是 [YouTube](https://youtube.com)的免費開源前端，也可自行託管。

有許多公共實例，其中一些實例支援 [Tor](https://www.torproject.org) onion 服務。

[:octicons-home-16: Homepage](https://invidious.io){ .md-button .md-button--primary }
[:octicons-server-16:](https://instances.invidious.io){ .card-link title="Public Instances"}
[:octicons-info-16:](https://docs.invidious.io/){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/iv-org/invidious){ .card-link title="Source Code" }
[:octicons-heart-16:](https://invidious.io/donate/){ .card-link title=Contribute }

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning "警告"</p>

預設情況下， Invidious不會代理影片串流。 Videos watched through Invidious will still make direct connections to Google's servers (e.g. `googlevideo.com`); however, some instances support video proxying—simply enable *Proxy videos* within the instances' settings or add `&local=true` to the URL.

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

如果您想在瀏覽器中停用JavaScript ，例如 [Tor瀏覽器](https://www.torproject.org/)最安全級別，Invidious 非常有用。 它本身不提供隱私，故不建議登入任何帳戶。

</div>

### Piped

<div class="admonition recommendation" markdown>

![Piped logo](assets/img/frontends/piped.svg){ align=right }

**Piped** 是 [YouTube](https://youtube.com)的免費開源前端，也是可自主託管。

Piped 需要JavaScript 才能運行，它有許多公共實例。

[:octicons-repo-16: Repository](https://github.com/TeamPiped/Piped){ .md-button .md-button--primary }
[:octicons-server-16:](https://piped.kavin.rocks/preferences#ddlInstanceSelection){ .card-link title="Public Instances"}
[:octicons-info-16:](https://piped-docs.kavin.rocks/){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/TeamPiped/Piped){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/TeamPiped/Piped#donations){ .card-link title=Contribute }

</details>

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

如果您想使用 [SponsorBlock](https://sponsor.ajay.app)但不安裝瀏覽器擴展或在不登入帳戶訪問有年齡限制的內容， Piped 非常有用。 它本身不提供隱私，故不建議登入任何帳戶。

</div>

## 標準

**請注意，我們所推薦專案沒有任何瓜葛。 ** 除了 [標準準則](about/criteria.md)外，我們還發展出一套明確要求以提出客觀建議。 建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

<div class="admonition example" markdown>
<p class="admonition-title">此部份新增</p>

我們正在努力為這個網站的各個部分建立明確標準，它可能依情況變化。 如果您對我們的標準有任何疑問，請在 [論壇上提問](https://discuss.privacyguides.net/latest) ，如果沒有列出，請不要認為我們在提出建議時沒有考慮到某些事情。 當我們推薦一個項目時，有許多因素被考慮和討論，記錄每一個項目都是正在進行式。

</div>

推薦的前端…

- 必須是開源軟體。
- 必須是可自行託管。
- 必須提供匿名訪客完整的網站基本功能。

我們只考慮網站的前端是...

- Normally only accessible with JavaScript enabled.
