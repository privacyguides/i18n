---
title: "路由器軔體"
icon: material/router-wireless
description: 能保護路由器或 Wi-Fi 存取點安全的替代作業系統。
cover: router.webp
---

<small>防護下列威脅：</small>

- [:material-account-cash: 監控資本主義](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}
- [:material-bug-outline: 被動攻擊](basics/common-threats.md#security-and-privacy ""){.pg-orange}

Below are a few alternative operating systems that can be used on routers, Wi-Fi access points, etc.

## OpenWrt

<div class="admonition recommendation" markdown>

![OpenWrt logo](assets/img/router/openwrt.svg#only-light){ align=right }
![OpenWrt logo](assets/img/router/openwrt-dark.svg#only-dark){ align=right }

**OpenWrt** 是一個基於 Linux 的操作系統；它主要用於嵌入式設備以路由網路流量。 它包括util-linux ， uClibc和BusyBox。 所有組件都已為家庭路由器進行了優化。

[:octicons-home-16: 首頁](https://openwrt.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://openwrt.org/docs/start){ .card-link title=說明文件}
[:octicons-code-16:](https://github.com/openwrt/openwrt){ .card-link title="原始碼" }
[:octicons-heart-16:](https://openwrt.org/donate){ .card-link title=捐款 }

</details>

</div>

您可以參考 OpenWrt 的 [硬體表格](https://openwrt.org/toh/start) 來檢查您的設備是否受到支援。

## OPNsense

<div class="admonition recommendation" markdown>

![OPNsense logo](assets/img/router/opnsense.svg){ align=right }

**OPNsense** 是開源的、基於FreeBSD 的防火牆和路由平臺，它包含許多進階功能，如流量整形、負載平衡和 VPN 功能，且有插件的形式提供更多功能。 OPNsense 通常部署作邊界防火牆、路由器、無線存取點、DHCP伺服器、DNS伺服器和 VPN 端點。

[:octicons-home-16: 首頁](https://opnsense.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.opnsense.org/index.html){ .card-link title=說明文件}
[:octicons-code-16:](https://github.com/opnsense){ .card-link title="原始碼" }
[:octicons-heart-16:](https://opnsense.org/donate){ .card-link title=捐款 }

</details>

</div>

OPNsense 是從 [pfSense](https://en.wikipedia.org/wiki/PfSense) 另外發展出來的分支，兩個項目都以免費和可靠的防火牆發行版而聞名，它們提供了通常只有昂貴的商業防火牆才具備的功能。  2015 年啟動後，OPNsense 開發人員[引述](https://docs.opnsense.org/history/thefork.html) pfSense  專案中一連串安全與代碼品質問題，因此覺得有必要對須目作分支。再者 Netgate 取得 pfSense 大部份所有權， pfSense 未來的方向也令他們擔憂。

## 標準

**請注意，我們所推薦專案沒有任何瓜葛。 ** 除了 [標準準則](about/criteria.md)外，我們還發展出一套明確要求以提出客觀建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

- 它必須是開源的。
- 必須定期更新。
- 需要支持各種各樣的硬體。
