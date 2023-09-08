---
meta_title: "E-posta, Gizlilik ve Güvenlik için Neden En İyi Seçenek Değildir - Privacy Guides"
title: E-posta Güvenliği
icon: material/email
description: Email is inherently insecure in many ways, and these are some of the reasons it isn't our top choice for secure communications.
---

E-posta varsayılan olarak güvensiz bir iletişim şeklidir. Mesajlarınıza Uçtan Uca Şifreleme ekleyen OpenPGP gibi araçlarla e-posta güvenliğinizi artırabilirsiniz, ancak OpenPGP'nin diğer mesajlaşma uygulamalarındaki şifrelemeye kıyasla hala bir takım dezavantajları vardır ve e-postanın tasarlanma şekli nedeniyle bazı e-posta verileri hiçbir zaman doğal olarak şifrelenemez.

Sonuç olarak e-posta, başkalarıyla iletişim kurmak için değil, çevrimiçi olarak kaydolduğunuz hizmetlerden işlem e-postaları (bildirimler, doğrulama e-postaları, parola sıfırlama vb. gibi) almak için en iyi şekilde kullanılır.

## E-posta Şifrelemeye Genel Bakış

Farklı e-posta sağlayıcıları arasındaki e-postalara uçtan uca şifreleme eklemenin standart yolu OpenPGP kullanmaktır. OpenPGP standardının farklı uygulamaları vardır, en yaygın olanları [GnuPG](https://en.wikipedia.org/wiki/GNU_Privacy_Guard) ve [OpenPGP.js](https://openpgpjs.org).

İş dünyasında popüler olan [S/MIME](https://en.wikipedia.org/wiki/S/MIME)adında başka bir standart daha vardır, ancak bir [Sertifika Yetkilisi](https://en.wikipedia.org/wiki/Certificate_authority) tarafından verilen bir sertifika gerektirir (hepsi S/MIME sertifikası vermez). [Google Workplace](https://support.google.com/a/topic/9061730?hl=en&ref_topic=9061731) ve [Web için Outlook veya Exchange Server 2016, 2019](https://support.office.com/en-us/article/encrypt-messages-by-using-s-mime-in-outlook-on-the-web-878c79fc-7088-4b39-966f-14512658f480)desteği vardır.

Even if you use OpenPGP, it does not support [forward secrecy](https://en.wikipedia.org/wiki/Forward_secrecy), which means if either your or the recipient's private key is ever stolen, all previous messages encrypted with it will be exposed. Bu nedenle, mümkün olduğunca kişiden kişiye iletişim için e-posta yerine ileri gizlilik uygulayan [anlık mesajlaşma programlarını](../real-time-communication.md) öneriyoruz.

### What Email Clients Support E2EE?

Email providers which allow you to use standard access protocols like IMAP and SMTP can be used with any of the [email clients we recommend](../email-clients.md). Depending on the authentication method, this may lead to the decrease security if either the provider or the email client does not support OATH or a bridge application as [multi-factor authentication](multi-factor-authentication.md) is not possible with plain password authentication.

### How Do I Protect My Private Keys?

A smartcard (such as a [YubiKey](https://support.yubico.com/hc/en-us/articles/360013790259-Using-Your-YubiKey-with-OpenPGP) or [Nitrokey](https://www.nitrokey.com)) works by receiving an encrypted email message from a device (phone, tablet, computer, etc.) running an email/webmail client. The message is then decrypted by the smartcard and the decrypted content is sent back to the device.

It is advantageous for the decryption to occur on the smartcard so as to avoid possibly exposing your private key to a compromised device.

## Email Metadata Overview

Email metadata is stored in the [message header](https://en.wikipedia.org/wiki/Email#Message_header) of the email message and includes some visible headers that you may have seen such as: `To`, `From`, `Cc`, `Date`, `Subject`. There are also a number of hidden headers included by many email clients and providers that can reveal information about your account.

Client software may use email metadata to show who a message is from and what time it was received. Servers may use it to determine where an email message must be sent, among [other purposes](https://en.wikipedia.org/wiki/Email#Message_header) which are not always transparent.

### Who Can View Email Metadata?

Email metadata is protected from outside observers with [Opportunistic TLS](https://en.wikipedia.org/wiki/Opportunistic_TLS) protecting it from outside observers, but it is still able to be seen by your email client software (or webmail) and any servers relaying the message from you to any recipients including your email provider. Sometimes email servers will also use third-party services to protect against spam, which generally also have access to your messages.

### Why Can't Metadata be E2EE?

Email metadata is crucial to the most basic functionality of email (where it came from, and where it has to go). E2EE was not built into the email protocols originally, instead requiring add-on software like OpenPGP. Because OpenPGP messages still have to work with traditional email providers, it cannot encrypt email metadata, only the message body itself. That means that even when using OpenPGP, outside observers can see lots of information about your messages, such as who you're emailing, the subject lines, when you're emailing, etc.
