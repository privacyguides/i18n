---
meta_title: "為什麼電子郵件不是隱私和安全的最佳選擇 - Privacy Guides"
title: 電子郵件安全
icon: material/email
description: Email is insecure in many ways, and these are some of the reasons it isn't our top choice for secure communications.
---

電子郵件本身即非安全的通訊形式。 You can improve your email security with tools such as OpenPGP, which add end-to-end encryption to your messages, but OpenPGP still has a number of drawbacks compared to encryption in other messaging applications.

因此，電子郵件最適合用於從您在線註冊的服務接收交易性電子郵件（如通知、驗證電子郵件、密碼重置等），而不是用於與他人溝通。

## 郵件如何加密

將 E2EE 添加到不同電子郵件提供商之間的電子郵件的標準方法是使用 OpenPGP。 There are different implementations of the OpenPGP standard, the most common being [GnuPG](../encryption.md#gnu-privacy-guard) and [OpenPGP.js](https://openpgpjs.org).

Even if you use OpenPGP, it does not support [forward secrecy](https://en.wikipedia.org/wiki/Forward_secrecy), which means if the private key of either you or the message recipient is ever stolen, all previous messages encrypted with it will be exposed. 這就是為什麼我們建議 [即時通訊](../real-time-communication.md) ，只要有可能，就實現電子郵件的前向保密性，以進行個人對個人的通信。

There is another standard which is popular with business called [S/MIME](https://en.wikipedia.org/wiki/S/MIME), however it requires a certificate issued from a [Certificate Authority](https://en.wikipedia.org/wiki/Certificate_authority) (not all of them issue S/MIME certificates, and often a yearly payment is required). In some cases it is more usable than PGP because it has support in popular/mainstream email applications like Apple Mail, [Google Workplace](https://support.google.com/a/topic/9061730), and [Outlook](https://support.office.com/article/encrypt-messages-by-using-s-mime-in-outlook-on-the-web-878c79fc-7088-4b39-966f-14512658f480). However, S/MIME does not solve the issue of lack of forward secrecy, and isn't particularly more secure than PGP.

## Web Key Directory 網頁金鑰目錄標準介紹

The [Web Key Directory (WKD)](https://wiki.gnupg.org/WKD) standard allows email clients to discover the OpenPGP key for other mailboxes, even those hosted on a different provider. 支援 WKD 的電子郵件用戶端將根據電子郵件位址的網域名稱向收件者的伺服器請求金鑰。 例如，如果向`jonah@privacyguides.org` 發送電子郵件，您的電子郵件用戶端會向`privacyguides.org` 詢問Jonah 的OpenPGP 金鑰，如`privacyguides.org` 擁有該帳戶的金鑰，則您的訊息將自動加密。

除了我們推薦的[電子郵件用戶端](../email-clients.md)支援 WKD外，一些網頁郵件供應商也支援 WKD。 *自己的*金鑰是否發佈到 WKD 供其他人使用取決於網域配置。 如果使用支援 WKD 的[電子郵件提供者](../email.md#openpgp-known-services)，例如 Proton Mail 或 Mailbox.org，他們可以在其網站上發布您網域名所準備的 OpenPGP 金鑰。

如果使用自訂網域，則需另外設定 WKD。 如果你可控制自定域名，則無論電子郵件提供者為何，都可以設定 WKD。 One easy way to do this is to use the "[WKD as a Service](https://keys.openpgp.org/about/usage#wkd-as-a-service)" feature from the `keys.openpgp.org` server: Set a CNAME record on the `openpgpkey` subdomain of your domain pointed to `wkd.keys.openpgp.org`, then upload your key to [keys.openpgp.org](https://keys.openpgp.org). 或者你可以 [在自己的 Web 伺服器搭建 WKD](https://wiki.gnupg.org/WKDHosting) 。

If you use a shared domain from a provider which doesn't support WKD, like `@gmail.com`, you won't be able to share your OpenPGP key with others via this method.

### 哪些郵件客戶端支援 E2EE？

電子郵件服務供應商讓您能使用標準訪問協議如 IMAP 與SMTP，以便應用[我們推薦的電子郵件客戶端軟體](../email-clients.md)。 Depending on the authentication method, this may lead to decreased security if either the provider or the email client does not support [OAuth](account-creation.md#sign-in-with-oauth) or a bridge application as [multifactor authentication](multi-factor-authentication.md) is not possible with plain password authentication.

### 我該如何保護自己的私鑰？

A smart card (such as a [YubiKey](https://support.yubico.com/hc/articles/360013790259-Using-Your-YubiKey-with-OpenPGP) or [Nitrokey](../security-keys.md#nitrokey)) works by receiving an encrypted email message from a device (phone, tablet, computer, etc.) running an email/webmail client. The message is then decrypted by the smart card and the decrypted content is sent back to the device.

It is advantageous for the decryption to occur on the smart card to avoid possibly exposing your private key to a compromised device.

## 電子郵件元資料概覽

Email metadata is stored in the [message header](https://en.wikipedia.org/wiki/Email#Message_header) of the email message and includes some visible headers that you may have seen such as `To`, `From`, `Cc`, `Date`, and `Subject`. 許多電子郵件客戶端和提供商還包含一些隱藏的標題，可以揭示有關您的帳戶的信息。

客戶端軟體可能會使用電子郵件中繼資料來顯示來自誰以及收到訊息的時間。 伺服器可以使用它來確定電子郵件消息必須發送的位置，其中 [個其他目的](https://en.wikipedia.org/wiki/Email#Message_header) 並不總是透明的。

### 誰可以查看電子郵件中繼資料？

Email metadata is protected from outside observers with [opportunistic TLS](https://en.wikipedia.org/wiki/Opportunistic_TLS), but it is still able to be seen by your email client software (or webmail) and any servers relaying the message from you to any recipients including your email provider. 有時，電子郵件伺服器也會使用第三方服務來防範垃圾郵件，垃圾郵件通常也可以訪問您的郵件。

### 爲什麼元數據不能是E2EE ？

電子郵件元數據對於電子郵件最基本的功能（它來自何處，以及它必須去向何處）至關重要。 E2EE was not built into standard email protocols originally, instead requiring add-on software like OpenPGP. Because OpenPGP messages still have to work with traditional email providers, it cannot encrypt some of this email metadata required for identifying the parties communicating. That means that even when using OpenPGP, outside observers can see lots of information about your messages, such as whom you're emailing, when you're emailing, etc.
