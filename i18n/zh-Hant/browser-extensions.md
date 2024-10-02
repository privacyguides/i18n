---
title: 瀏覽器擴充套件
icon: material/puzzle-outline
description: 這些瀏覽器擴充套件可以增強瀏覽體驗並保護隱私。
cover: browser-extensions.webp
---

<small>防護下列威脅：</small>

- [:material-account-cash: 監控資本主義](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

一般來說，建議將瀏覽器擴充套件維持在最低限度，以減少攻擊面。 它們在您的瀏覽器中擁有特殊存取權限，需要您信任開發人員，而且可以讓您 [脫穎而出](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)，並 [削弱](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/0ei-UCHNm34/m/lDaXwQhzBAAJ) 站點隔離。

然而，有些提供的功能在某些情況下可以克服這些缺點，特別是在[內容攔截](basics/common-threats.md#mass-surveillance-programs)方面。

不要安裝無立即需求的擴充套件，或與瀏覽器功能重複的擴充套件。 例如，[Brave](desktop-browsers.md#brave)使用者不需要安裝uBlock Origin，因為Brave Shields 已經提供了相同的功能。

## 內容攔截

### uBlock Origin

<div class="admonition recommendation" markdown>

![uBlock Origin logo](assets/img/browsers/ublock_origin.svg){ align=right }

**uBlock Origin** 是一款流行的內容攔截器，可攔截廣告、追蹤器和指紋辨識腳本。

[:octicons-repo-16: 儲存庫](https://github.com/gorhill/uBlock#readme){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/gorhill/uBlock/wiki/Privacy-policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://github.com/gorhill/uBlock/wiki){ .card-link title=說明文件}
[:octicons-code-16:](https://github.com/gorhill/uBlock){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/ublock-origin)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/ublock-origin/odfafepnkmbhccpbejgmiehpchacaeak)

</details>

</div>

建議遵循[開發人員文檔](https://github.com/gorhill/uBlock/wiki/Blocking-mode)並選擇其中一種「模式」。 額外的過濾器清單可能會影響效能且[可能增加攻擊面](https://portswigger.net/research/ublock-i-exfiltrate-exploiting-ad-blockers-with-css)。

這些是可能需要考慮添加的其他[過濾器列表](https://github.com/gorhill/uBlock/wiki/Dashboard:-Filter-lists)：

- [x] 勾選 **Privacy** > **AdGuard URL Tracking Protection**
- 新增 [Actually Legitimate URL Shortener Tool](https://raw.githubusercontent.com/DandelionSprout/adfilt/master/LegitimateURLShortener.txt)

### uBlock Origin Lite

uBlock Origin 還有一個「Lite」版本，與原始版相比，其功能集非常有限。 但比之成熟的姊妹產品它具有一些明顯優勢值得考慮，如果...

- ...不想對擴充功能授予完整的「讀取/修改網站資料」權限（即使是像 uBlock Origin 這樣受信任的擴充功能）
- ....想要一個更多資源（記憶體/CPU）高效的內容攔截器[^1]
- ...瀏覽器只能支援 Manifest V3 擴展。

<div class="admonition recommendation" markdown>

![uBlock Origin Lite logo](assets/img/browsers/ublock_origin_lite.svg){ align=right }

**uBlock Origin Lite** 是相容於 Manifest V3 的內容攔截器。 與原版的 _uBlock Origin_ 相比，此擴充套件不需要廣泛的「讀取/修改資料」權限即可運作，這降低了在過濾器清單中加入惡意規則時，瀏覽器受到 [:material-bug-outline: 被動攻擊](basics/common-threats.md#security-and-privacy){ .pg-orange } 的風險。

[:octicons-repo-16: 儲存庫](https://github.com/uBlockOrigin/uBOL-home#readme){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/uBlockOrigin/uBOL-home/wiki/Privacy-policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://github.com/uBlockOrigin/uBOL-home/wiki){ .card-link title=說明文件}
[:octicons-code-16:](https://github.com/gorhill/uBlock/tree/master/platform/mv3){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/addon/ublock-origin-lite)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/ublock-origin-lite/ddkjiahejlhfcafbddmgiahcphecmpfh)

</details>

</div>

若不想更改過濾器列表，我們僅推薦此版本的 uBlock Origin，因為它僅支援一些預先選擇的列表，且不提供其他自訂選項，包括手動選擇要封鎖的元素的功能。 這些限制是由於 Manifest V3 設計之故。

此版本提供三種封鎖等級：「基本」等級不需要任何特殊權限即可查看和修改網站內容，而「最佳」和「完整」等級確實需要廣泛的權限，但透過附加裝飾規則提供更好的過濾體驗和腳本注入。

如將預設過濾模式設為“最佳”或“完整”，則擴充功能將要求讀取/修改**所有**造訪網站的存取權限。 不過也可以透過調整擴充功能彈出面板中的滑桿，在任何指定網站將設定變更為**個別**網站的「最佳」或「完整」。 當這樣，擴充功能將僅請求對該網站的讀取/修改存取權限。 因此，如想利用 uBlock Origin Lite 的“無權限”配置，應將預設保留為“基本”，並且僅在該級別不夠的網站上將其調整得更高。

uBlock Origin Lite 僅在擴充功能從瀏覽器的附加元件市場更新時接收封鎖清單更新，而不是按需求接收。 此意味著可能會錯過被封鎖數週的新威脅，直到附加元件發布完整的版本。

### AdGuard

我們為 iOS 用戶推薦 [Safari](mobile-browsers.md#safari)，遺憾的是 uBlock Origin 不支援。 幸好還有 Adguard 作為足夠的替代：

<div class="admonition recommendation" markdown>

![AdGuard logo](assets/img/browsers/adguard.svg){ align=right }

**適用於 iOS的 AdGuard** 使用原生[Content Blocker API](https://developer.apple.com/documentation/safariservices/creating_a_content_blocker) 的Safari 免費開源內容封鎖擴展。

[:octicons-home-16: 首頁](https://adguard.com/en/adguard-ios/overview.html){ .md-button .md-button--primary }
[:octicons-eye-16:](https://adguard.com/privacy/ios.html){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://kb.adguard.com/ios){ .card-link title=說明文件}
[:octicons-code-16:](https://github.com/AdguardTeam/AdguardForiOS){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id1047223162)

</details>

</div>

額外的過濾器清單會減慢速度，並可能會增加您的攻擊面，因此只應用您需要的東西。 iOS 版 AdGuard 有一些高級功能；然而，標準Safari 內容封鎖是免費的。

## 標準

- 不得複製內建瀏覽器或作業系統功能。
- 必須直接影響用戶隱私，即不得簡單地提供資訊。

[^1]: uBlock Origin Lite **本身**不會消耗任何資源，因為它使用更新的API，瀏覽器能夠本地處理過濾器列表，而不是在擴充功能中執行JavaScript 程式碼來處理過濾。 然而，這種資源優勢僅止於 [理論](https://github.com/uBlockOrigin/uBOL-home/wiki/Frequently-asked-questions-\(FAQ\)#is-ubol-more-efficient-cpu--and-memory-wise-than-ubo)，因為標準uBlock Origin 的過濾程式碼可能比瀏覽器的本機過濾程式碼更有效。 目前尚未對此進行基準測試。
