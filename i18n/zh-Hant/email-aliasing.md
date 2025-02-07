---
title: 電子郵件別名
icon: material/email-lock
description: 電子郵件別名服務可輕鬆地替每次網站註冊生成一個新的電子郵件地址。
cover: email-aliasing.webp
---

<small>防護下列威脅：</small>

- [:material-account-cash: 監控資本主義](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }
- [:material-account-search: 公共暴露](basics/common-threats.md#limiting-public-information){ .pg-green }

**電子郵件別名服務** 可讓您輕鬆地為每個註冊的網站產生一個新的電子郵件地址。 電子郵件別名會自動把郵件轉發到所選擇的電子郵件地址，以隱藏「主要」電子郵件地址和 [電子郵件提供商](email.md)。 真正的電子郵件別名比許多提供商常用和支援的加號地址（plus addressing）更好，可自行創建別名，如：「yourname +[anythinghere]@example.com」，而這可避免網站，廣告商和跟蹤網路簡單地刪除+符號之後的任何內容，以知道使用者真實電子郵件地址。 [IAB](https://en.wikipedia.org/wiki/Interactive_Advertising_Bureau) 等組織要求廣告商 [規範化電子郵件地址](https://shkspr.mobi/blog/2023/01/the-iab-loves-tracking-users-but-it-hates-users-tracking-them) ；如此一來無論使用者的隱私意願如何，都可以關聯和追蹤它們。

<div class="grid cards" markdown>

- ![addy.io logo](assets/img/email-aliasing/addy.svg){ .twemoji } [addy.io](email-aliasing.md#addyio)
- ![SimpleLogin logo](assets/img/email-aliasing/simplelogin.svg){ .twemoji } [SimpleLogin](email-aliasing.md#simplelogin)

</div>

電子郵件別名還可以在您的電子郵件供應商停止運作時提供保障。 在這種情況下，可輕鬆地將別名設定轉發給新的電子郵件地址。 但反過來，您也需要信任別名服務能夠持續運作。

使用專門的電子郵件別名服務比自定網域上的通用別名有許多好處：

- 有需要時，可以單獨開啟和關閉別名，防止網站隨機發送電子郵件給您。
- 從別名地址發送回覆，屏蔽真實電子郵件地址。

與「臨時電子郵件」服務相比，它們還有許多好處：

- 別名是永久性的，如果您需要接收密碼重設等內容，可以再次開啟別名。
- 電子郵件會發送到您信任的郵箱，而不是儲存在別名服務提供者。
- 臨時電子郵件服務通常會有公共郵箱，任何知道地址的人都可以訪問，別名則個人所私有的。

我們所推薦的電子郵件別名提供商可讓您在他們所控制的網域名稱上建立別名；也可在您自己的自訂網域名稱上建立別名，而只需支付適度的年費。 如果想要最大限度的控制，也可以自主託管。 但是，使用自定網域可能會有隱私上的缺點：如果自己是唯一使用該自定網域的人，只需查看電子郵件地址中的網域名稱並忽略 (@) 符號之前的所有內容，即可輕鬆跟蹤您的動作。

使用別名服務代表您需要同時信任您的電子郵件供應商和您的別名供應商，讓他們處理您未加密的郵件。 有些提供商會透過自動 PGP 加密[^1] 稍微緩解這個問題，在傳送至您最終的電子信箱供應商之前，先將收到的電子郵件加密，將您需要信任的對象從兩個減少到一個。

### addy.io

<div class="admonition recommendation" markdown>

![addy.io logo](assets/img/email-aliasing/addy.svg){ align=right }

**addy.io** 可讓您在共用網域上免費建立 10 個網域別名，或無限制的「標準」別名。

[:octicons-home-16: 首頁](https://addy.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://addy.io/privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://addy.io/faq){ .card-link title=說明文件}
[:octicons-code-16:](https://github.com/anonaddy){ .card-link title="原始碼" }
[:octicons-heart-16:](https://addy.io/donate){ .card-link title=捐款 }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-android: Android](https://addy.io/faq/#is-there-an-android-app)
- [:material-apple-ios: iOS](https://addy.io/faq/#is-there-an-ios-app)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/addy_io)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/addyio-anonymous-email-fo/iadbdpnoknmbdeolbapdackdcogdmjpe)

</details>

</div>

免費帳戶建立共用網域名(像 @addy.io) 的數量為最多10個，月付1美元則可增加到 50 個別外，月付 4美元(或年繳則以3美元計) 則無數量限制。 可建立無限的標準別名，這些別名以 @[username].addy.io 等網域或付費方案自訂網域結尾。 付費帳戶可建立無數的標準別名如尾綴為 @[username]. 或是自定域名。不過如前面提過，標準別名電郵並不利於隱私，因為只依據域名就可以簡單地把別名綁定起來。 當共用網域名服務封鎖此功能時，它就派得上用場了。 Securitum 於 2023 年 9 月 完成對 addy.io 的 [稽核](https://addy.io/blog/addy-io-passes-independent-security-audit) ，[已確認](https://addy.io/addy-io-security-audit.pdf) 沒發現任何重大漏洞。

值得注意的免費功能：

- [x] 10 個共享別名
- [x] 無限制的標準別名數量
- [ ] 無對外回覆
- [x] 1個收件人郵箱
- [x] 自動 PGP 加密[^1]

如果您取消訂閱，您仍可享有付費方案的功能，直到該期帳單最後繳費期限結束為止。 在您當期的最後繳費期限結束後，大部分付費功能（包括任何自訂網域）將會 [停用](https://addy.io/faq/#what-happens-if-i-have-a-subscription-but-then-cancel-it) ，付費帳戶設定將還原為預設值，如果之前已停用，則會啟用 catch-all 功能。

### SimpleLogin

<div class="admonition recommendation" markdown>

![Simplelogin logo](assets/img/email-aliasing/simplelogin.svg){ align=right }

**SimpleLogin** 是免費服務，可在各種共享域名上提供電子郵件別名，並可選擇提供無限別名和自訂域名等付費功能。

[:octicons-home-16: 首頁](https://simplelogin.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://simplelogin.io/privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://simplelogin.io/docs){ .card-link title=說明文件}
[:octicons-code-16:](https://github.com/simple-login){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.simplelogin.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1494359858)
- [:simple-github: GitHub](https://github.com/simple-login/Simple-Login-Android/releases)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/simplelogin)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/dphilobhebphkdjbpfohgikllaljmgbn)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/simpleloginreceive-sen/diacfpipniklenphgljfkmhinphjlfff)
- [:simple-safari: Safari](https://apps.apple.com/app/id6475835429)

</details>

</div>

SimpleLogin 在2022 年 4月8日[已被 Proton AG 收購](https://proton.me/news/proton-and-simplelogin-join-forces)。 如果主要電子郵箱使用 Proton Mail， SimpleLogin是一個不錯的選擇。 這兩種產品現在都由同一家公司擁有，您只需要信任單一實體。 我們預計 SimpleLogin 未來會與 Proton 產品更緊密地整合。 SimpleLogin 繼續支援轉寄至您所選擇的任何電子郵件供應商。 Securitum 在 2022 年初[審核](https://simplelogin.io/blog/security-audit) SimpleLogin，所有問題[均已改善](https://simplelogin.io/audit2022/web.pdf)。

可在設定中將 SimpleLogin 帳戶與 Proton 帳戶作連結。 If you have Proton Pass Plus, Proton Unlimited, or any multi-user Proton plan, you will have SimpleLogin Premium for free.

值得注意的免費功能：

- [x] 10 個共享別名
- [x] 無回復上限
- [x] 1個收件人郵箱
- [ ] 自動 PGP 加密[^1] 只在付費方案下可用

當您結束訂閱後，您建立的所有別名仍可接收和傳送電子郵件。 但是，您不能建立任何超出免費計劃限制的新別名，也不能新增網域、目錄或郵箱。

## 標準

**請注意，我們與所推薦的服務提供商並無任何關係。** 除了 [我們的常規標準](about/criteria.md) 之外，在適用的情況下，我們對電子郵件別名提供商的標準與 [電子郵件提供商](email.md#criteria) 的標準相同。 建議在選擇電子郵件提供商之前熟悉此列表，並進行自己的研究，以確保選出正確適合的電子郵件提供商。

[^1]: 自動 PGP 加密功能可讓您的電子郵箱別名供應商在收到未加密的電子郵件傳入並轉寄到您的主要電子信箱之前先將其加密，確保您的主要電子信箱供應商永遠不會看到未加密的電子郵件內容。
