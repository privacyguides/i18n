---
meta_title: "為什麼電子郵件不是隱私和安全的最佳選擇 - Privacy Guides"
title: 電子郵件安全
icon: material/email
description: Email is insecure in many ways, and these are some of the reasons it isn't our top choice for secure communications.
---

電子郵件本身即非安全的通訊形式。 You can improve your email security with tools such as OpenPGP, which add End-to-End Encryption to your messages, but OpenPGP still has a number of drawbacks compared to encryption in other messaging applications.

因此，電子郵件最適合用於從您在線註冊的服務接收交易性電子郵件（如通知、驗證電子郵件、密碼重置等），而不是用於與他人溝通。

## 郵件如何加密

將 E2EE 添加到不同電子郵件提供商之間的電子郵件的標準方法是使用 OpenPGP。 OpenPGP 標準有不同的實現，最常見的是 [GnuPG](https://en.wikipedia.org/wiki/GNU_Privacy_Guard) 和 [OpenPGP.js](https://openpgpjs.org)。

即使您使用OpenPGP ，它也不支援 [向前保密](https://en.wikipedia.org/wiki/Forward_secrecy)，這意味著如果您或收件人的私鑰被盜，所有先前加密的消息都將被曝光。 這就是為什麼我們建議 [即時通訊](../real-time-communication.md) ，只要有可能，就實現電子郵件的前向保密性，以進行個人對個人的通信。

There is another standard which is popular with business called [S/MIME](https://en.wikipedia.org/wiki/S/MIME), however, it requires a certificate issued from a [Certificate Authority](https://en.wikipedia.org/wiki/Certificate_authority) (not all of them issue S/MIME certificates, and often a yearly payment is required). In some cases it is more usable than PGP because it has support in popular/mainstream email applications like Apple Mail, [Google Workplace](https://support.google.com/a/topic/9061730), and [Outlook](https://support.office.com/article/encrypt-messages-by-using-s-mime-in-outlook-on-the-web-878c79fc-7088-4b39-966f-14512658f480). However, S/MIME does not solve the issue of lack of forward secrecy, and isn't particularly more secure than PGP.

## Web Key Directory 網頁金鑰目錄標準介紹

The [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD) standard allows email clients to discover the OpenPGP key for other mailboxes, even those hosted on a different provider. 支援 WKD 的電子郵件用戶端將根據電子郵件位址的網域名稱向收件者的伺服器請求金鑰。 例如，如果向`jonah@privacyguides.org` 發送電子郵件，您的電子郵件用戶端會向`privacyguides.org` 詢問Jonah 的OpenPGP 金鑰，如`privacyguides.org` 擁有該帳戶的金鑰，則您的訊息將自動加密。

除了我們推薦的[電子郵件用戶端](../email-clients.md)支援 WKD外，一些網頁郵件供應商也支援 WKD。 *自己的*金鑰是否發佈到 WKD 供其他人使用取決於網域配置。 如果使用支援 WKD 的[電子郵件提供者](../email.md#openpgp-known-services)，例如 Proton Mail 或 Mailbox.org，他們可以在其網站上發布您網域名所準備的 OpenPGP 金鑰。

如果使用自訂網域，則需另外設定 WKD。 如果你可控制自定域名，則無論電子郵件提供者為何，都可以設定 WKD。 一個簡單的方法是使用 [WKD as a Service](https://keys.openpgp.org/about/usage#wkd-as-a-service) 功能，透過指向`wkd.keys.openpgp.org` 網域的`openpgpkey` 子網域來設定CNAME記錄，然後將金鑰上傳到 [keys.openpgp.org](https://keys.openpgp.org) 。 或者你可以 [在自己的 Web 伺服器搭建 WKD](https://wiki.gnupg.org/WKDHosting) 。

如使用不支援 WKD 供應商的共用網域（例如 @gmail.com），則無法透過此方法與其他人共用你的 OpenPGP 金鑰。

### 哪些郵件客戶端支援 E2EE？

電子郵件服務供應商讓您能使用標準訪問協議如 IMAP 與SMTP，以便應用[我們推薦的電子郵件客戶端軟體](../email-clients.md)。 安全性則視驗證方法而定，如果提供者或電子郵件用戶端不支援 OATH 或橋接應用程式，這可能會導致安全性降低，因為在純密碼驗證環境下無法使用[多重要素驗證](multi-factor-authentication.md)。

### 我該如何保護自己的私鑰？

A smart card (such as a [YubiKey](https://support.yubico.com/hc/articles/360013790259-Using-Your-YubiKey-with-OpenPGP) or [Nitrokey](../security-keys.md#nitrokey)) works by receiving an encrypted email message from a device (phone, tablet, computer, etc.) running an email/webmail client. The message is then decrypted by the smart card and the decrypted content is sent back to the device.

It is advantageous for the decryption to occur on the smart card to avoid possibly exposing your private key to a compromised device.

## 電子郵件元資料概覽

電子郵件中繼資料儲存在電子郵件的 [個訊息標題](https://en. wikipedia. org/wiki/Email#Message_header) 中，並包含您可能已經看到的一些可見標題，例如： `To`、 `From`、 `Cc`、 `Date`、 `Subject`。 許多電子郵件客戶端和提供商還包含一些隱藏的標題，可以揭示有關您的帳戶的信息。

客戶端軟體可能會使用電子郵件中繼資料來顯示來自誰以及收到訊息的時間。 伺服器可以使用它來確定電子郵件消息必須發送的位置，其中 [個其他目的](https://en.wikipedia.org/wiki/Email#Message_header) 並不總是透明的。

### 誰可以查看電子郵件中繼資料？

電子郵件元數據受到外部觀察者的保護， [Opportunistic TLS](https://en.wikipedia.org/wiki/Opportunistic_TLS) 保護它免受外部觀察者的影響，但它仍然能夠被您的電子郵件客戶端軟體（或網路郵件）和任何伺服器看到，將您的消息轉發給任何收件人，包括您的電子郵件提供商。 有時，電子郵件伺服器也會使用第三方服務來防範垃圾郵件，垃圾郵件通常也可以訪問您的郵件。

### 爲什麼元數據不能是E2EE ？

電子郵件元數據對於電子郵件最基本的功能（它來自何處，以及它必須去向何處）至關重要。 E2EE 最初並未內建於電子郵件協議中，而是需要像 OpenPGP 這樣的附加軟體。 Because OpenPGP messages still have to work with traditional email providers, it cannot encrypt some of this email metadata required for identifying the parties communicating. That means that even when using OpenPGP, outside observers can see lots of information about your messages, such as whom you're emailing, when you're emailing, etc.
