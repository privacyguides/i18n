---
meta_title: "Dlaczego e-mail nie jest najlepszym wyborem pod względem prywatności i bezpieczeństwa – Privacy Guides"
title: Bezpieczeństwo poczty e-mail
icon: material/email
description: Poczta e-mail jest niezabezpieczoną na wiele sposobów formą komunikacji, a oto niektóre z powodów, dla których nie jest ona naszym pierwszym wyborem, jeśli chodzi o bezpieczną komunikację.
---

E-mail jest domyślnie niezabezpieczoną formą komunikacji. Bezpieczeństwo poczty e-mail można poprawić narzędziami takimi jak OpenPGP, które dodają szyfrowanie typu end-to-end do wiadomości, jednak OpenPGP nadal ma szereg wad w porównaniu z szyfrowaniem stosowanym w innych komunikatorach.

W efekcie e-mail najlepiej nadaje się do otrzymywania wiadomości dotyczących transakcji (np. powiadomień, resetów haseł, wiadomości z linkiem weryfikacyjnym itp.) od usług, na które rejestrujesz się online, a nie do komunikowania się z innymi.

## Przegląd szyfrowania wiadomości e-mail

Standardowym sposobem dodania szyfrowania E2EE do wiadomości między różnymi dostawcami poczty jest użycie OpenPGP. Istnieją różne implementacje standardu OpenPGP, najpopularniejsze to [GnuPG](../encryption.md#gnu-privacy-guard) i [OpenPGP.js](https://openpgpjs.org).

Nawet jeśli używasz OpenPGP, nie obsługuje ono [utajniania z wyprzedzeniem](https://pl.wikipedia.org/wiki/Utajnianie_z_wyprzedzeniem), co oznacza, że jeśli prywatny klucz Twój lub odbiorcy zostanie kiedykolwiek skradziony, wszystkie poprzednie wiadomości zaszyfrowane tym kluczem mogą zostać ujawnione. Dlatego zalecamy korzystanie z [komunikatorów](../real-time-communication.md), które implementują utajnianie z wyprzedzeniem, zamiast poczty e-mail do komunikacji między osobami, o ile to możliwe.

Istnieje też inny standard popularny w środowisku biznesowym — [S/MIME](https://en.wikipedia.org/wiki/S/MIME) — jednak wymaga on certyfikatu wydanego przez [urząd certyfikacji](https://pl.wikipedia.org/wiki/Urząd_certyfikacji) (nie wszystkie urzędy wydają certyfikaty S/MIME, a często konieczne jest coroczna opłata). W niektórych sytuacjach jest on bardziej użyteczny niż PGP, ponieważ jest obsługiwany w popularnych aplikacjach pocztowych, takich jak Poczta Apple, [Google Workspace](https://support.google.com/a/topic/9061730) i [Outlook](https://support.office.com/article/encrypt-messages-by-using-s-mime-in-outlook-on-the-web-878c79fc-7088-4b39-966f-14512658f480). Niemniej S/MIME nie rozwiązuje problemu braku utajniania z wyprzedzeniem i nie jest znacząco bezpieczniejszy niż PGP.

## Czym jest standard Web Key Directory?

Standard [Web Key Directory](https://wiki.gnupg.org/WKD) (WKD, pol. katalog kluczy publicznych) umożliwia klientom poczty e-mail odnaleźć klucz OpenPGP dla innych skrzynek, nawet tych hostowanych przez innego dostawcę. Klienci poczty obsługujący WKD będą pytać serwer odbiorcy o klucz na podstawie nazwy domeny w adresie e-mail. Na przykład, jeśli wyślesz wiadomość na adres `jonah@privacyguides.org`, Twój klient poczty e-mail zapyta `privacyguides.org` o klucz OpenPGP Jonaha, a jeśli `privacyguides.org` ma klucz dla tego konta, Twoja wiadomość zostanie automatycznie zaszyfrowana.

Oprócz [zalecanych przez nas klientów poczty e-mail](../email-clients.md), które obsługują WKD, niektóre usługi webmail również obsługują WKD. To, czy *Twój własny* klucz jest opublikowany w WKD, zależy od konfiguracji domeny. Jeśli korzystasz z [dostawcy poczty](../email.md#openpgp-compatible-services), który obsługuje WKD, takiego jak Proton Mail czy poczty Mailbox, mogą oni opublikować Twój klucz OpenPGP w swojej domenie w Twoim imieniu.

Jeżeli używasz własnej, niestandardowej domeny, konieczne będzie osobne skonfigurowanie WKD. Jeśli masz kontrolę nad nazwą swojej domeny, możesz skonfigurować WKD niezależnie od dostawcy poczty. Jednym z prostszych sposobów jest skorzystanie z funkcji „[WKD as a Service](https://keys.openpgp.org/about/usage#wkd-as-a-service)” serwera `keys.openpgp.org`: ustaw rekord CNAME na subdomenie `openpgpkey` swojej domeny wskazujący na `wkd.keys.openpgp.org`, a następnie prześlij swój klucz na [keys.openpgp.org](https://keys.openpgp.org). Alternatywnie możesz [samodzielnie hostować WKD na własnym serwerze WWW](https://wiki.gnupg.org/WKDHosting).

Jeżeli korzystasz ze współdzielonej domeny dostawcy, który nie obsługuje WKD, np. `@gmail.com`, nie będzie możliwe udostępnienie klucza OpenPGP innym w ten sposób.

### Które klienty poczty e-mail obsługują E2EE?

Dostawcy poczty, którzy pozwalają na korzystanie ze standardowych protokołów dostępu, takich jak IMAP i SMTP, mogą współpracować z dowolnym z [zalecanych przez nas klientów poczty e-mail](../email-clients.md). W zależności od metody uwierzytelniania może to jednak obniżać bezpieczeństwo, jeśli ani dostawca, ani klient poczty nie obsługują [OAuth](account-creation.md#sign-in-with-oauth) lub aplikacji mostkowych, ponieważ w takim przypadku [uwierzytelnianie wieloskładnikowe](multi-factor-authentication.md) nie jest możliwe przy zwykłym logowaniu za pomocą hasła.

### How Do I Protect My Private Keys?

A smart card (such as a [YubiKey](https://support.yubico.com/hc/articles/360013790259-Using-Your-YubiKey-with-OpenPGP) or [Nitrokey](../security-keys.md#nitrokey)) works by receiving an encrypted email message from a device (phone, tablet, computer, etc.) running an email/webmail client. The message is then decrypted by the smart card and the decrypted content is sent back to the device.

It is advantageous for the decryption to occur on the smart card to avoid possibly exposing your private key to a compromised device.

## Email Metadata Overview

Email metadata is stored in the [message header](https://en.wikipedia.org/wiki/Email#Message_header) of the email message and includes some visible headers that you may have seen such as `To`, `From`, `Cc`, `Date`, and `Subject`. There are also a number of hidden headers included by many email clients and providers that can reveal information about your account.

Client software may use email metadata to show who a message is from and what time it was received. Servers may use it to determine where an email message must be sent, among [other purposes](https://en.wikipedia.org/wiki/Email#Message_header) which are not always transparent.

### Who Can View Email Metadata?

Email metadata is protected from outside observers with [opportunistic TLS](https://en.wikipedia.org/wiki/Opportunistic_TLS), but it is still able to be seen by your email client software (or webmail) and any servers relaying the message from you to any recipients including your email provider. Sometimes email servers will also use third-party services to protect against spam, which generally also have access to your messages.

### Why Can't Metadata be E2EE?

Email metadata is crucial to the most basic functionality of email (where it came from, and where it has to go). E2EE was not built into standard email protocols originally, instead requiring add-on software like OpenPGP. Because OpenPGP messages still have to work with traditional email providers, it cannot encrypt some of this email metadata required for identifying the parties communicating. That means that even when using OpenPGP, outside observers can see lots of information about your messages, such as whom you're emailing, when you're emailing, etc.
