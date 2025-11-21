---
title: "替代網路"
icon: material/vector-polygon
description: 這些工具可存取萬維網以外的網路。
cover: alternative-networks.webp
---

<small>防護下列威脅：</small>

- [:material-server-network: 服務提供商](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }
- [:material-eye-outline: 大規模監控](basics/common-threats.md#mass-surveillance-programs){ .pg-blue }
- [:material-account-cash: 監控資本主義](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

## 匿名網路

當談到匿名網路時，要特別注意的是 我們首選的[Tor](advanced/tor-overview.md) 。 它是迄今為止使用最多、研究最深入、開發最活躍的匿名網路。 使用其他網路可能會更容易危及您的 [:material-incognito: 匿名](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple } ，除非您知道自己在做什麼。

### Tor

<div class="admonition recommendation" markdown>

![Tor logo](assets/img/self-contained-networks/tor.svg){ align=right }

**Tor** 網路是一組由志願者操作的伺服器，可免費連線，並改善隱私權和安全性。 個人和組織還可以通過 Tor 網路與“.onion 隱藏服務”分享資訊，而不會侵犯他們的隱私。 由於 Tor 流量難以封鎖和追蹤，因此 Tor 是一種有效的 [:material-close-outline: 審查](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray } 規避工具。

[:octicons-home-16:](https://torproject.org){ .card-link title=首頁 }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="洋蔥服務" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=說明文件}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/core/tor){ .card-link title="原始碼" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=捐款 }

</div>

存取 Tor 網路的建議方式是透過官方 Tor 瀏覽器，我們在專用頁面作了更詳細的介紹：

[Tor 瀏覽器資訊 :material-arrow-right-drop-circle:](tor.md){ .md-button .md-button--primary } [Tor 詳細介紹 :material-arrow-right-drop-circle:](advanced/tor-overview.md){ .md-button }

您可以使用其他工具存取 Tor 網路；此決策取決於您的威脅模型。 如果是不用擔心 ISP 蒐集針對您的證據的一般 Tor 使用者，那麼使用 [Orbot](#orbot) 等應用程式或行動瀏覽器應用程式存取 Tor 網路就可以了。 越多人使用 Tor 有助於減少 Tor 的不良印記，降低 ISP 和政府可能編制的「Tor 用戶清單」內容。

<div class="admonition example" markdown>
<p class="admonition-title">試用一下！</p>

可以嘗試透過 Tor 連線到_Privacy Guides_：[xoe4vn5uwdztif6goazfbmogh6wh5jc4up35bqdflu6bkdc5cas5vjqd.onion](http://www.xoe4vn5uwdztif6goazfbmogh6wh5jc4up35bqdflu6bkdc5cas5vjqd.onion).

</div>

#### Orbot

<div class="admonition recommendation" markdown>

![Orbot 標誌](assets/img/self-contained-networks/orbot.svg){ align=right }

**Orbot** 是行動裝置應用程式，可將您裝置上任何應用程式的流量導向透過 Tor 網路傳輸。

[:octicons-home-16: 首頁](https://orbot.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://orbot.app/privacy-policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://orbot.app/faqs){ .card-link title="文件" }
[:octicons-code-16:](https://orbot.app/code){ .card-link title="原始碼" }
[:octicons-heart-16:](https://orbot.app/donate){ .card-link title="貢獻" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1609461599)
- [:simple-github: GitHub](https://github.com/guardianproject/orbot/releases)
- [:simple-fdroid: F-Droid](https://guardianproject.info/fdroid)

</details>

</div>

我們先前曾建議在 Orbot 設定中啟用「隔離目標位址」偏好設定。 雖然從理論上來說，此設定可以強制您連線至不同 IP 位址時使用不同的迴路來改善隱私，但其並未為大多數應用程式（特別是網路瀏覽器）提供實際的優勢，可能會帶來顯著的效能下降，增加 Tor 網路的負載。 我們不再建議您修改此設定，除非您非常確定您需要調整。[^1]

\=== "Android"

```
Orbot can proxy individual apps if they support SOCKS or HTTP proxying. It can also proxy all your network connections using [VpnService](https://developer.android.com/reference/android/net/VpnService) and can be used with the VPN kill switch in :gear: **Settings** → **Network & internet** → **VPN** → :gear: → **Block connections without VPN**.

Orbot is often outdated on Google Play and the Guardian Project's F-Droid repository, so consider downloading directly from the GitHub repository instead. All versions are signed using the same signature, so they should be compatible with each other.
```

\=== "iOS"

```
On iOS, Orbot has some limitations that could potentially cause crashes or leaks: iOS does not have an effective OS-level feature to block connections without a VPN like Android does, and iOS has an artificial memory limit for network extensions that makes it challenging to run Tor in Orbot without crashes. Currently, it is always safer to use Tor on a desktop computer compared to a mobile device.
```

#### Snowflake

<div class="admonition recommendation" markdown>

![Snowflake logo](assets/img/self-contained-networks/snowflake.svg#only-light){ align=right }
![Snowflake logo](assets/img/self-contained-networks/snowflake-dark.svg#only-dark){ align=right }

**Snowflake** 可透過瀏覽器中執行「Snowflake 代理」來向 Tor 專案捐贈頻寬。

被審查的人可以使用 Snowflake 代理來連接 Tor 網路。 Snowflake 是貢獻 Tor 網路的好方法，即便沒有運行 Tor 中繼或橋接的技術知識。

[:octicons-home-16: Homepage](https://snowflake.torproject.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/Technical%20Overview){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribute }

</details>

</div>

要啟用瀏覽器的 Snowflake 請在另一個標籤分頁下開啟其切換開關。 您可讓它在背景下執行而您的瀏覽器會協助其連接。 不建議將 Snowflake 作為瀏覽器附加元件安裝，因為第三方的擴展往往會增加攻擊面。

[瀏覽器下執行 Snowflake :material-arrow-right-drop-circle:](https://snowflake.torproject.org/embed.html){ .md-button }

Snowflake 無法加強隱私，也不會在個人瀏覽器中連接 Tor 網路。 但如果網際網路連接沒有被審查的情形，請考慮使用它，幫助受審查網路中的人們能有更好的隱私。 無需擔心人們通過您的代理訪問哪些網站----他們的可見瀏覽 IP 地址將與其 Tor 出口節點相匹配，而不是您的 IP 地址。

Running a Snowflake proxy is low-risk, even more so than running a Tor relay or bridge which are already not particularly risky endeavors. 但是，它通過您的網路進行代理流量，在某些方面可能會產生影響，特別是所用的網路頻寬有限制的話。 在決定是否要執行代理程式之前，請確保了解 [Snowflake 的工作原理](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/home) 。

### I2P (隱形網際網路計劃)

<div class="admonition recommendation" markdown>

![I2P logo](assets/img/self-contained-networks/i2p.svg#only-light){ align=right }
![I2P logo](assets/img/self-contained-networks/i2p-dark.svg#only-dark){ align=right }

**I2P** is a network layer which encrypts your connections and routes them via a network of computers distributed around the world. 它主要致力創建一個替代性的隱私保護網路，而不是使常規的網路連接匿名。

[:octicons-home-16: 首頁](https://geti2p.net/en){ .md-button .md-button--primary }
[:octicons-info-16:](https://geti2p.net/en/about/software){ .card-link title=說明文件 }
[:octicons-code-16:](https://github.com/i2p/i2p.i2p){ .card-link title="原始碼" }
[:octicons-heart-16:](https://geti2p.net/en/get-involved){ .card-link title=捐款 }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.i2p.android)
- [:simple-android: Android](https://geti2p.net/en/download#android)
- [:fontawesome-brands-windows: Windows](https://geti2p.net/en/download#windows)
- [:simple-apple: macOS](https://geti2p.net/en/download#mac)
- [:simple-linux: Linux](https://geti2p.net/en/download#unix)

</details>

</div>

不同於 Tor ，所有 I2P 流量都是 I2P 網路內部的，這意味著常規網站**不能**直接從 I2P 存取。 相反，可以連接到直接在 I2P 網路上匿名託管的網站，這些網站稱為“eepsites”，並且具有以“.i2p”結尾的網域。

<div class="admonition example" markdown>
<p class="admonition-title">試用一下！</p>

可試試透過 I2P 訪問 _Privacy Guides_ [privacyguides.i2p](http://privacyguides.i2p/?i2paddresshelper=fvbkmooriuqgssrjvbxu7nrwms5zyhf34r3uuppoakwwsm7ysv6q.b32.i2p).

</div>

再者，每個 I2P 節點預設都會為其他使用者中繼流量，而不是依賴專門的中繼志工來運行節點。 Tor 網路大約有[10,000](https://metrics.torproject.org/networksize.html) 個中繼和網橋，而I2P 上有大約50,000 個中繼和網橋，這意味著流量可能有更多的路由方式來最大化匿名性。 I2P also tends to be more performant than Tor, although this is likely a side effect of Tor being more focused on regular "clearnet" internet traffic and thus using more bottle necked exit nodes. 與 Tor 相比，通常認為 I2P 上的隱藏服務效能更優。 在 Tor 上運行 BitTorrent 等 P2P 應用程式具有挑戰性（並且會極大地影響 Tor 網路效能），而在 I2P 上運行卻非常簡單且高效能。

然而，I2P 的方法也有缺點。 Tor 依賴專用的出口節點，這意味著更多的人可以在不太安全的環境中使用它，而且Tor 上確實存在的中繼可能性能更高、更穩定，因為它們通常不在長駐連接上運行。 Tor 也更關注**瀏覽器隱私**（即防指紋），並配有專用的 [Tor 瀏覽器](tor.md) 來盡可能使瀏覽活動匿名。 I2P 透過[常用網頁瀏覽器](desktop-browsers.md) 使用，雖然可以將瀏覽器設定為更保護隱私，但可能不會與其他 I2P 使用者有相同的瀏覽器指紋（沒有在這方面混在「人群」）。

由於其強大的橋接網路和不同的[可插拔傳輸](https://tb-manual.torproject.org/circumvention)，Tor 更能抵抗審查。 另一方面，I2P 使用目錄伺服器進行初始連接，這些目錄伺服器是變化的/不受信任的，由志願者運行，而 Tor 使用的硬編碼/受信任的伺服器可能更容易被阻止。

[^1]: The `IsolateDestAddr` setting is discussed on the [Tor mailing list](https://lists.torproject.org/pipermail/tor-talk/2012-May/024403) and [Whonix's Stream Isolation documentation](https://whonix.org/wiki/Stream_Isolation), where both projects suggest that it is usually not a good approach for most people.
