---
title: "通訊網路的類型"
icon: 'material/transit-connection-variant'
description: 簡介常見的即時通訊應用程式網路架構。
---

有幾種網路架構常運用於在人與人之間傳遞消息。 這些網路提供不同的隱私保證，這就是為什麼在決定使用哪個應用程式時，最好能考慮您的[威脅模型](../basics/threat-modeling.md) 。

[Recommended Instant Messengers](../real-time-communication.md ""){.md-button} [:material-movie-open-play-outline: Video: It's time to stop using SMS](https://www.privacyguides.org/videos/2025/01/24/its-time-to-stop-using-sms-heres-why ""){.md-button}

## 集中式網路

![集中網路圖](../assets/img/layout/network-centralized.svg){ align=left }

集中式信使是指所有參與者都在同一伺服器或同一組織所控制的伺服器網路。

有些自託管信使允許設定自己的伺服器。 自託管可以提供額外的隱私保證，例如不用記錄或限制讀取元數據（關於誰與誰交談的資料）。 自託管的集中式信使是隔離的，每個人都必須在同一個伺服器上進行通訊。

**優點**

- 新功能和變更可以更快地實施。
- 更容易使用和查找聯系人。
- 近乎成熟和穩定的生態系統，因為集中式軟件更容易編譯。
- 當您信任自我託管的伺服器時，隱私問題可能會減少。

**缺點**

- [限制控制或存取](https://drewdevault.com/2018/08/08/Signal.html)。 可能包括以下內容：
- 集中型網路 [禁封了](https://github.com/LibreSignal/LibreSignal/issues/37#issuecomment-217211165)可以提供更靈活自定與更佳使用體驗的第三方客戶端。 通常定義在使用條款和條件。
- 對於第三方開發人員來說，文件記錄很糟。
- 由單一實體控制服務時，其 [所有權](https://web.archive.org/web/20210729191953/https://blog.privacytools.io/delisting-wire)、隱私政策和服務操作可輕易改變，甚致危及服務。
- 自我託管需要精力和設定服務的知識。

## 聯邦式網路

![聯邦式網路圖](../assets/img/layout/network-decentralized.svg){ align=left }

聯合信使使用多個獨立的分散式伺服器，這些伺服器能夠彼此通訊（電子郵件是聯合服務的一個例子）。 聯邦讓系統管理員控制自己的伺服器，成為更大通訊網路中的一員。

當自行託管時，聯邦伺服器的成員可以發現並與其他伺服器的成員進行通訊，而有些伺服器可能會選擇保持私密而不加入聯邦（例如工作團隊伺服器）。

**優點**

- 運行自己的伺服器可以更加控制自己的資料。
- 可從多個“公共”伺服器之中選擇信任的資料託付者。
- 可讓第三方客戶端提供更原生、定制或親和的體驗。
- 伺服器軟體可以驗證是否與公開原始碼相符，但前提是您可以存取伺服器，或是您信任可以存取伺服器的人（例如家人）。

**缺點**

- 添加新功能較複雜，因為這些功能需要標準化和測試，以確保可與網路上的所有伺服器配合使用。
- 根據前一點，與集中式平臺相比，聯邦式網路欠缺完整功能或容易出現意外，例如離線時的訊息中繼或訊息刪除。
- 可能會產生某些元數據（例如使用 E2EE 時， “誰在與誰交談”但不知其實際內容的資料）。
- 聯邦式伺服器通常需要信任伺服器管理員。 他們可能是業餘愛好者，也不是“安全專業人士” ，欠缺標準文件，如隱私政策或服務條款，來詳細說明資料如何被使用。
- 伺服器管理員有時會封鎖其他伺服器，因為它們無節制地濫用的或違反公認行為的一般規則。 這會阻礙您與這些伺服器成員溝通的能力。

## 點對點網路

![P2P示意圖](../assets/img/layout/network-distributed.svg){ align=left }

P2P 軟體連接到 [分佈式網路](https://en.wikipedia.org/wiki/Distributed_networking) 中的節點，在沒有第三方伺服器的情況下將訊息傳遞給收件人。

客戶端（對等軟體）通常通過 [分布式計算](https://en.wikipedia.org/wiki/Distributed_computing) 網路找到彼此。 例如， [Distributed Hash Tables](https://en.wikipedia.org/wiki/Distributed_hash_table) (DHT)被 [torrents](https://en.wikipedia.org/wiki/BitTorrent_(protocol)) 和 [IPFS](https://en.wikipedia.org/wiki/InterPlanetary_File_System) 使用。 另一種方法是鄰近通訊，通過 Wi-Fi 或藍牙建立連接（例如：Briar 或 [Scuttlebutt](https://scuttlebutt.nz)社交網路協議）。

一旦對等體通過任何這些方法找到通往其聯繫的路徑，它們之間就會建立直接連接。 通常訊息內容會加密，但觀察者仍然可以推斷寄件人和收件人的位置和身份。

P2P 網路不使用伺服器，對等方彼此之間直接通訊，因此不能自我託管。 但是，一些額外的服務可能要靠集中式伺服器，例如用戶看到或轉發離線消息，這些需要自託管伺服器的協助。

**優點**

- 最少的信息暴露給第三方。
- 現代 P2P 平臺皆已預設為 E2EE。 不像集中和中心化網路，沒有伺服器會攔截和解密您的傳輸。

**缺點**

- 精簡功能集：
- 訊息只能在兩個對等方都在線時發送，但是，客戶端可能會在本地儲存訊息以等待聯絡人在線時送出。
- 增加行動裝置的電池使用量，因為客戶端必須保持與分佈式網路的連接，以了解誰在線。
- 缺少某些傳訊功能或不完整，例如訊息刪除。
- 如果您未將軟體與 [VPN](../vpn.md) 或 [Tor](../tor.md)配合使用，則很可能暴露了自己和通訊聯絡人的 IP 位址。 許多國家都有某種形式的大規模監控和/或元數據保留。

## 匿名路由

![匿名路由示意圖](../assets/img/layout/network-anonymous-routing.svg){ align=left }

使用 [匿名路由](https://doi.org/10.1007/978-1-4419-5906-5_628) 的傳訊方式會隱藏發送者、接收者的身份或他們一直在溝通的證據。 理想情況下，這三種東西都該被隱藏。

實現匿名路由的方法有[很多](https://doi.org/10.1145/3182658)。 其中最著名 [洋蔥路由](https://en.wikipedia.org/wiki/Onion_routing) （即 [Tor](tor-overview.md)） ，該虛擬 [覆蓋網路](https://en.wikipedia.org/wiki/Overlay_network) 隱藏節點位置以及收件人和寄件人之間的加密訊息。 發送者和接收者不會直接互動，而是通過祕密會合節點，這樣就不會洩漏 IP 位址或物理位置。 節點無法解密訊息，也無法解密最終目的地；只有收件人可以。 中間節點只能解密下一步送到哪裡的指示，消息本體仍保持加密直到送達最終有權限解密的收件人，因此是“洋蔥層”。

在匿名路由網路中自我託管節點無法增加額外隱私優勢，但有助於整個網路抵禦識別攻擊。

**優點**

- 很少甚至無資訊暴露給其他方。
- 消息可以以分散的方式接力傳遞，即使其中一方離線。

**缺點**

- 消息傳播速度慢。
- 通常僅支援少數媒體類型，因為網路速度慢主要為文字傳輸。
- 隨機路由選擇節點，某些節點可能遠離發送者和接收者，增加延遲，甚至因某個節點離線而無法傳輸消息。
- 入手更複雜，因為需要創建和備份加密私鑰。
- 如同其他分散式平臺，對開發人員而言，添加功能比集中式平臺更複雜。 因此，功能欠缺或未完全執行，例如離線消息中繼或消息刪除。
