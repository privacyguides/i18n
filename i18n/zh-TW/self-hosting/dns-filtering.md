---
title: DNS 過濾
meta_title: "自行架設 DNS 解決方案 - Privacy Guides"
icon: material/dns
description: 對於技術能力較高的讀者，自行架設 DNS 解決方案可為雲端 DNS 解決方案無法涵蓋的裝置提供過濾功能。
cover: dns.webp
---

<small>防護下列威脅：</small>

- [:material-server-network: 服務供應商](../basics/common-threats.md#privacy-from-service-providers){ .pg-teal }
- [:material-account-cash: 監控資本主義](../basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

\*\* 自架 DNS\*\* 無須另外安裝客戶端軟體，對於在功能受控制的平台（例如智慧型電視和其他 IoT 裝置）進行 [DNS 過濾](https://cloudflare.com/learning/access-management/what-is-dns-filtering)非常有用。 請記得，除非您進行更進階的設定，不然下列 DNS 解決方案通常都只會對您住家網路或區域網路生效。

## DNS 天坑

[**DNS 天坑（DNS Sinkhole）**](https://en.wikipedia.org/wiki/DNS_sinkhole)就是使用 DNS 過濾技術來封鎖廣告等不想要的網頁內容。

### Pi-Hole

<div class="admonition recommendation" markdown>

![Pi-hole 圖示](../assets/img/self-hosting/pi-hole.svg){ align=right }

**Pi-hole** 是一套開放原始碼的 DNS 天坑，提供友善的網頁介面，讓您可以看到統計資訊，並管理要封鎖的內容。 Pi-hole 設計應用在 Raspberry Pi ，但它並不限於這種硬體。

[:octicons-home-16: 首頁](https://pi-hole.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://pi-hole.net/privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://docs.pi-hole.net){ .card-link title="文件" }
[:octicons-code-16:](https://github.com/pi-hole/pi-hole){ .card-link title="原始碼" }
[:octicons-heart-16:](https://pi-hole.net/donate){ .card-link title="捐款" }

</div>

### AdGuard Home

<div class="admonition recommendation" markdown>

![AdGuard Home 圖示](../assets/img/self-hosting/adguard-home.svg){ align=right }

**AdGuard Home** 是一套開放原始碼的 DNS 天坑，提供精緻的網頁介面，讓您可以看到統計資訊，並管理要封鎖的內容。

[:octicons-home-16: 首頁](https://adguard.com/adguard-home/overview.html){ .md-button .md-button--primary }
[:octicons-eye-16:](https://adguard.com/privacy/home.html){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://github.com/AdguardTeam/AdGuardHome/wiki){ .card-link title="文件" }
[:octicons-code-16:](https://github.com/AdguardTeam/AdGuardHome){ .card-link title="原始碼" }

</div>
