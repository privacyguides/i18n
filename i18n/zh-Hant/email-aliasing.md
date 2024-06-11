---
title: 電子郵件別名
icon: material/email-lock
description: 電子郵件別名服務可輕鬆地替每次網站註冊生成一個新的電子郵件地址。
cover: email-aliasing.webp
---

電子郵件別名服務可輕鬆地替每次網站註冊生成一個新的電子郵件地址。 電子郵件別名會自動把郵件轉發到所選擇的電子郵件地址，以隱藏“主要”電子郵件地址和[電子郵件提供商](email.md)。 真正的電子郵件別名比許多提供商常用和支持的加地址更好，可自行創建別名，如 'yourname +[anythinghere]@ example.com' ，因為網站，廣告商和跟蹤網絡可以簡單地刪除+符號之後的任何內容，以知道使用者真實電子郵件地址。 [IAB](https://en.wikipedia.org/wiki/Interactive_Advertising_Bureau) 等組織要求廣告商[規範化電子郵件地址](https://shkspr.mobi/blog/2023/01/the-iab-loves-tracking-users-but-it-hates-users-tracking-them) ，無論用戶的隱私意願，都可以關聯和追蹤它們。

<div class="grid cards" markdown>

- ![addy.io logo](assets/img/email-aliasing/addy.svg){ .twemoji } [addy.io](email-aliasing.md#addyio)
- ![SimpleLogin logo](assets/img/email-aliasing/simplelogin.svg){ .twemoji } [SimpleLogin](email-aliasing.md#simplelogin)

</div>

電子郵件別名可以作為一種保護措施，一旦您的電子郵件提供商停止運營。 在這種情況下，可輕鬆地將別名重新路由到新的電子郵件地址。 但這也意謂，把信任轉移到另一家別名服務以繼續享用此功能。

使用專門的電子郵件別名服務比自定網域上的通用別名有許多好處：

- 有需要時，可以單獨開啟和關閉別名，防止網站隨機發送電子郵件給您。
- 從別名地址發送回覆，屏蔽真實電子郵件地址。

與「臨時電子郵件」服務相比，它們還有許多好處：

- 別名是永久性的，如果您需要接收密碼重設等內容，可以再次開啟別名。
- 電子郵件會發送到您信任的郵箱，而不是儲存在別名服務提供者。
- 臨時電子郵件服務通常會有公共郵箱，任何知道地址的人都可以訪問，別名則個人所私有的。

我們建議的電子郵件別名供應商，可讓您在他們控制的網域上創建別名，或您支付適度的年費來自定網域。 如果想要最大限度的控制，也可以自主託管。 但是，使用自定網域可能會有隱私上的缺點：如果自己是唯一使用該自定網域的人，只需查看電子郵件地址中的網域名稱並忽略 (@) 符號之前的所有內容，即可輕鬆跟蹤您的動作。

使用別名服務需要信任電子郵件提供商和別名提供商如何對待用戶未加密的消息。 有些供應商會透過自動 PGP 加密來稍微減輕這種情況，傳送到最終信箱供應商之前加密所傳送的電子郵件，將需要信任的各方數量從兩個減少到一個。

### addy.io

<div class="admonition recommendation" markdown>

![addy.io logo](assets/img/email-aliasing/addy.svg){ align=right }

**addy.io** 可在共用網域上免費建立 10 個網域別名，或無限的匿名程度較低的「標準」別名。

[:octicons-home-16: Homepage](https://addy.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://addy.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://addy.io/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/anonaddy){ .card-link title="Source Code" }
[:octicons-heart-16:](https://addy.io/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-android: Android](https://addy.io/faq/#is-there-an-android-app)
- [:material-apple-ios: iOS](https://addy.io/faq/#is-there-an-ios-app)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/addy_io)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/addyio-anonymous-email-fo/iadbdpnoknmbdeolbapdackdcogdmjpe)

</details>

</div>

免費帳戶建立共用網域名(像 @addy.io) 的數量為最多10個，月付1美元則可增加到 50 個別外，月付 4美元(或年繳則以3美元計) 則無數量限制。 可建立無限的標準別名，這些別名以 @[username].addy.io 等網域或付費方案自訂網域結尾。 付費帳戶可建立無數的標準別名如尾綴為 @[username]. 或是自定域名。不過如前面提過，標準別名電郵並不利於隱私，因為只依據域名就可以簡單地把別名綁定起來。 當共用網域名服務封鎖此功能時，它就派得上用場了。 2023年9月 Securitum 通過https://addy.io/blog/addy-io-passes-independent-security-audit 審查 ，沒發現重大的弱點缺失。

值得注意的免費功能：

- [x] 10 個共享別名
- [x] 無限制的標準別名數量
- [ ] 無對外回覆
- [x] 1個收件人郵箱
- [x] 自動 PGP 加密

### SimpleLogin

<div class="admonition recommendation" markdown>

![Simplelogin logo](assets/img/email-aliasing/simplelogin.svg){ align=right }

**SimpleLogin** 是免費服務，可在各種共享域名上提供電子郵件別名，並可選擇提供無限別名和自訂域名等付費功能。

[:octicons-home-16: Homepage](https://simplelogin.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://simplelogin.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://simplelogin.io/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/simple-login){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.simplelogin.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1494359858)
- [:simple-github: GitHub](https://github.com/simple-login/Simple-Login-Android/releases)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/simplelogin)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/dphilobhebphkdjbpfohgikllaljmgbn)
- [:simple-microsoftedge: Edge](https://microsoftedge.microsoft.com/addons/detail/simpleloginreceive-sen/diacfpipniklenphgljfkmhinphjlfff)
- [:simple-safari: Safari](https://apps.apple.com/app/id6475835429)

</details>

</div>

SimpleLogin 在2022 年 4月8日[已被 Proton AG 收購](https://proton.me/news/proton-and-simplelogin-join-forces)。 如果主要郵箱使用 Proton Mail， SimpleLogin是一個不錯的選擇。 這兩種產品現在都由同一家公司擁有，您只需要信任單一實體。 我們預計 SimpleLogin 未來會與 Proton 產品更緊密地整合。 SimpleLogin 繼續支援轉寄至您所選擇的任何電子郵件供應商。 Securitum 在 2022 年初[審核](https://simplelogin.io/blog/security-audit) SimpleLogin，所有問題[均已改善](https://simplelogin.io/audit2022/web.pdf)。

可在設定中將 SimpleLogin 帳戶與 Proton 帳戶作連結。 如果有 Proton Unlimited 、Business 或 Visionary 計劃，也可免費獲得 SimpleLogin Premium。

值得注意的免費功能：

- [x] 10 個共享別名
- [x] 無回復上限
- [x] 1個收件人郵箱
- [ ] 付費版才有自動 PGP 加密功能

## 標準

\*\*請注意，我們與所推薦的服務提供者並無任何關係。 \*\* 除了[評比標準](about/criteria.md) 之外，我們還按照與一般[電子郵件提供者標準]相同的標準評估電子郵件別名提供者](email.md#criteria) 。 建議在選擇電子郵件提供商之前熟悉此列表，並進行自己的研究，以確保選出正確適合的電子郵件提供商。

\*[自動 PGP 加密]: 可將未加密的電子郵件來文在轉發到郵箱前先予加密，確保主要郵箱提供者永遠不會看到未加密的電子郵件內容。
