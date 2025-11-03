---
meta_title: "為什麼電子郵件不是隱私和安全的最佳選擇 - Privacy Guides"
title: 電子郵件安全
icon: material/email
description: 從許多方面來看電子郵件是不安全的，以下是一些我們不把它作為安全通訊機制首選的原因。
---

電子郵件本身即非安全的通訊形式。 您可以使用 OpenPGP 等工具提高電子郵件安全性，這些工具讓訊息內容能夠端對端加密，但與其他訊息軟體當中的加密機制相比，OpenPGP 仍然有許多缺點。

因此，電子郵件最適合用於從您在線註冊的服務接收交易性電子郵件（如通知、驗證電子郵件、密碼重置等），而不是用於與他人溝通。

## 郵件如何加密

將 E2EE 添加到不同電子郵件提供商之間的電子郵件的標準方法是使用 OpenPGP。 OpenPGP 標準有不同的實作方式，最常見的是 [GnuPG](../encryption.md#gnu-privacy-guard) 及 [OpenPGP.js](https://openpgpjs.org)。

就算您使用 OpenPGP，它仍然不支援[向前保密](https://en.wikipedia.org/wiki/Forward_secrecy)，代表一旦您或訊息收件者的私鑰遭竊，所有用來加密的訊息就會曝光。 這就是為什麼我們建議 [即時通訊](../real-time-communication.md) ，只要有可能，就實現電子郵件的前向保密性，以進行個人對個人的通信。

有另一套稱為 [S/MIME](https://en.wikipedia.org/wiki/S/MIME)的標準，受到商業界的觀迎，但需要使用由[憑證管理機構](https://en.wikipedia.org/wiki/Certificate_authority)簽發的憑證（不是所有機構都簽發這種憑證，也時常需要支付年費）。 某些情況下這個機制比 PGP 更好用，因為 Apple Mail、[Google Workspace](https://support.google.com/a/topic/9061730) 以及 [Outlook](https://support.office.com/article/encrypt-messages-by-using-s-mime-in-outlook-on-the-web-878c79fc-7088-4b39-966f-14512658f480) 等知名的郵件軟體支援此機制。 但 S/MIME 仍未解決缺少向前保密性的問題，也沒有比 PGP 更特別安全。

## Web Key Directory 網頁金鑰目錄標準介紹

[網頁金鑰目錄 (WKD)](https://wiki.gnupg.org/WKD) 標準可讓電子郵件軟體尋找其他信箱的 OpenPGP 金鑰，就算是不同信箱服務上也沒問題。 支援 WKD 的電子郵件用戶端將根據電子郵件位址的網域名稱向收件者的伺服器請求金鑰。 例如，如果向`jonah@privacyguides.org` 發送電子郵件，您的電子郵件用戶端會向`privacyguides.org` 詢問Jonah 的OpenPGP 金鑰，如`privacyguides.org` 擁有該帳戶的金鑰，則您的訊息將自動加密。

除了我們推薦的[電子郵件用戶端](../email-clients.md)支援 WKD外，一些網頁郵件供應商也支援 WKD。 *自己的*金鑰是否發佈到 WKD 供其他人使用取決於網域配置。 如果使用支援 WKD 的[電子郵件業者](../email.md#openpgp-compatible-services)，例如 Proton Mail 或 Mailbox Mail，他們可以在其網站上為您發布 OpenPGP 金鑰。

如果使用自訂網域，則需另外設定 WKD。 如果你可控制自定域名，則無論電子郵件提供者為何，都可以設定 WKD。 一個簡單能做這這件事的方式，就是使用 `keys.openpgp.org` 的「[WKD as a Service](https://keys.openpgp.org/about/usage#wkd-as-a-service)」功能：為您的網域設定一組 `openpgpkey` 子網域的 CNAME 紀錄，指到 `wkd.keys.openpgp.org`，然後將您的金鑰上傳到 [keys.openpgp.org](https://keys.openpgp.org)。 或者你可以 [在自己的 Web 伺服器搭建 WKD](https://wiki.gnupg.org/WKDHosting) 。

若您使用不支援 WKD 的共用網域（例如 `@gmail.com`），則無法透過此方法與其他人共用您的 OpenPGP 金鑰。

### 哪些郵件客戶端支援 E2EE？

電子郵件服務供應商讓您能使用標準訪問協議如 IMAP 與SMTP，以便應用[我們推薦的電子郵件客戶端軟體](../email-clients.md)。 視驗證方法而定，如果業者或電子郵件軟體不支援 [OAuth](account-creation.md#sign-in-with-oauth) 或橋接軟體，可能會降低安全性，因為純文字密碼驗證下無法進行[多因素驗證](multi-factor-authentication.md)。

### 我該如何保護自己的私鑰？

智慧卡（例如 [YubiKey](https://support.yubico.com/hc/articles/360013790259-Using-Your-YubiKey-with-OpenPGP) 或 [Nitrokey](../security-keys.md#nitrokey)）的工作原理是先透過執行郵件軟體/網頁郵件裝置（手機、平板電腦、電腦等）接收加密過的電子郵件訊息。 然後智慧卡會解密該訊息，再將解開的內容送回裝置。

在智慧卡上進行解密的優點是可避免將私鑰暴露到某個已遭破解的裝置。

## 電子郵件元資料概覽

電子郵件的後設資料，儲存於[郵件訊息的標頭](https://en.wikipedia.org/wiki/Email#Message_header)當中，包含某些您可能也在郵件軟體中見過的標頭項目，例如 `To`、`From`、`Cc`、`Date` 與 `Subject` 等。 許多電子郵件客戶端和提供商還包含一些隱藏的標題，可以揭示有關您的帳戶的信息。

客戶端軟體可能會使用電子郵件中繼資料來顯示來自誰以及收到訊息的時間。 伺服器可以使用它來確定電子郵件消息必須發送的位置，其中 [個其他目的](https://en.wikipedia.org/wiki/Email#Message_header) 並不總是透明的。

### 誰可以查看電子郵件中繼資料？

電子郵件的後設資料受到 [Opportunistic TLS](https://en.wikipedia.org/wiki/Opportunistic_TLS) 保護，無法被外部觀察者看到，但它仍然能夠被您的電子郵件軟體（或網路郵件）和所有從您到收件者之間的轉寄伺服器看到。 有時，電子郵件伺服器也會使用第三方服務來防範垃圾郵件，垃圾郵件通常也可以訪問您的郵件。

### 爲什麼元數據不能是E2EE ？

電子郵件元數據對於電子郵件最基本的功能（它來自何處，以及它必須去向何處）至關重要。 一開始，標準的電子郵件通訊協定並未內建 E2EE，而是需要使用 OpenPGP 這樣的附加元件。 由於 OpenPGP 訊息仍然需要與傳統的電子郵件業者合作，無法加密訊息中記錄各方通訊者的某些標頭。 也就是說，就算使用 OpenPGP，外部觀察者仍然能看出有關您的訊息的許多資訊，例如您正與誰通信、是什麼時候寄出的等等。
