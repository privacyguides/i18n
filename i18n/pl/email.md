---
meta_title: "Zalecane szyfrowane prywatne usługi e-mail – Privacy Guides"
title: Usługi e-mail
icon: material/email
description: Ci dostawcy poczty e-mail oferują bezpieczne miejsce do przechowywania Twoich wiadomości e-mail, a wielu z nich zapewnia kompatybilne szyfrowanie OpenPGP do komunikacji z innymi usługodawcami.
cover: email.webp
global:
  - 
    - randomize-element
    - "table tbody"
---

<small>Chroni przed następującymi zagrożeniami:</small>

- [:material-server-network: Usługodawcy](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

Korzystanie z poczty e-mail jest praktycznie niezbędne do używania większości usług online, jednak nie zalecamy jej do rozmów osobistych. Zamiast używać e-maila do kontaktu z innymi ludźmi, rozważ komunikator internetowy obsługujący utajnianie z wyprzedzeniem (forward secrecy).

[Zalecane komunikatory internetowe](real-time-communication.md ""){.md-button}

## Zalecani dostawcy

Do pozostałych zastosowań zalecamy różnorodne usługi e-mail, oparte na zrównoważonych modelach biznesowych i wyposażone we wbudowane funkcje bezpieczeństwa oraz prywatności. Pełną [listę kryteriów](#criteria) znajdziesz w dalszej części strony.

| Dostawca                        | OpenPGP / WKD                          | IMAP / SMTP                                                         | Szyfrowanie z zerowym dostępem                          | Anonimowe metody płatności                |
| ------------------------------- | -------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------- | ----------------------------------------- |
| [Proton Mail](#proton-mail)     | :material-check:{ .pg-green }          | :material-information-outline:{ .pg-blue } Tylko w płatnych planach | :material-check:{ .pg-green }                           | Gotówka                                   |
| [Poczta Mailbox](#mailbox-mail) | :material-check:{ .pg-green }          | :material-check:{ .pg-green }                                       | :material-information-outline:{ .pg-blue } Tylko poczta | Gotówka                                   |
| [Tuta](#tuta)                   | :material-alert-outline:{ .pg-orange } | :material-alert-outline:{ .pg-orange }                              | :material-check:{ .pg-green }                           | Monero <br>Gotówka przez pośrednika |

Oprócz (lub zamiast) jednego z wymienionych tutaj dostawców usług e-mail, możesz rozważyć skorzystanie z dedykowanej [usługi aliasingu e-maili](email-aliasing.md#recommended-providers) w celu zwiększenia swojej prywatności. Między innymi takie usługi pomagają chronić Twoją prawdziwą skrzynkę przed spamem, uniemożliwiają marketerom powiązanie Twoich kont oraz szyfrują wszystkie przychodzące wiadomości za pomocą PGP.

- [Więcej informacji :material-arrow-right-drop-circle:](email-aliasing.md)

## Usługi kompatybilne z OpenPGP

Ci dostawcy natywnie obsługują szyfrowanie i deszyfrowanie OpenPGP oraz standard [Web Key Directory (WKD)](basics/email-security.md#what-is-the-web-key-directory-standard), co umożliwia wysyłanie i odbieranie wiadomości e-mail z szyfrowaniem typu end-to-end (E2EE) niezależnie od dostawcy. Na przykład użytkownik Proton Mail może wysłać zaszyfrowaną wiadomość E2EE do użytkownika poczty Mailbox, lub możesz otrzymywać zaszyfrowane powiadomienia OpenPGP od usług internetowych, które je wspierają.

<div class="grid cards" markdown>

- ![Logo Proton Mail](assets/img/email/protonmail.svg){ .twemoji } [Proton Mail](#proton-mail)
- ![Logo poczty Mailbox](assets/img/email/mailbox-mail.svg){ .twemoji } [Poczta Mailbox](#mailbox-mail)

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Ostrzeżenie</p>

Podczas korzystania z technologii E2EE, takich jak OpenPGP, część metadanych wiadomości e-mail wciąż pozostaje niezaszyfrowana — dotyczy to m.in. nagłówka wiadomości, który zazwyczaj zawiera temat maila! Dowiedz się więcej o [metadanych e-maili](basics/email-security.md#email-metadata-overview).

OpenPGP nie zapewnia również utajniania z wyprzedzeniem, co oznacza, że jeśli prywatny klucz Twój lub odbiorcy zostanie kiedykolwiek skradziony, wszystkie wcześniejsze wiadomości zaszyfrowane tym kluczem mogą zostać ujawnione.

— [Jak chronić swoje klucze prywatne?](basics/email-security.md#how-do-i-protect-my-private-keys)

</div>

### Proton Mail

<div class="admonition recommendation" markdown>

![Logo Proton Mail](assets/img/email/protonmail.svg){ align=right }

**Proton Mail** to usługa e-mail skupiona na prywatności, szyfrowaniu, bezpieczeństwie i prostocie obsługi. Działa od 2013 roku. Proton AG ma siedzibę w Genewie, w Szwajcarii.

Darmowy plan Proton Free oferuje 500 MB miejsca na pocztę, które można bezpłatnie zwiększyć do 1 GB.

[:octicons-home-16: Strona główna](https://proton.me/pl/mail){ .md-button .md-button--primary }
[:simple-torbrowser:](https://protonmailrmez3lotccipshtkleegetolb73fuirgj7r4o4vfu7ozyd.onion){ .card-link title="Usługa onion" }
[:octicons-eye-16:](https://proton.me/pl/legal/policy){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://proton.me/support/pl/mail){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/ProtonMail){ .card-link title="Kod źródłowy" }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonmail.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id979659905?l=pl)
- [:simple-github: GitHub](https://github.com/ProtonMail/android-mail/releases)
- [:fontawesome-brands-windows: Windows](https://proton.me/pl/mail/bridge#download)
- [:simple-apple: macOS](https://proton.me/pl/mail/bridge#download)
- [:simple-linux: Linux](https://proton.me/pl/mail/bridge#download)
- [:octicons-browser-16: Wersja przeglądarkowa](https://mail.proton.me)

</details>

</div>

Konta bezpłatne mają pewne ograniczenia, takie jak brak możliwości wyszukiwania w treści wiadomości oraz brak dostępu do [Proton Mail Bridge](https://proton.me/pl/mail/bridge), który jest wymagany do korzystania z [zalecanego klienta poczty desktopowej](email-clients.md) (np. Thunderbird). Konta płatne obejmują funkcje takie jak Proton Mail Bridge, dodatkową przestrzeń dyskową oraz obsługę własnych domen. Jeśli posiadasz plan Proton Unlimited lub jakikolwiek plan dla wielu użytkowników, otrzymujesz także darmowy dostęp do [SimpleLogin](email-aliasing.md#simplelogin) Premium.

[Raport potwierdzający bezpieczeństwo](https://proton.me/pl/blog/security-audit-all-proton-apps) aplikacji Proton Mail został wydany 9 listopada 2021 roku przez firmę [Securitum](https://research.securitum.com).

Proton Mail gromadzi wewnętrzne raporty o awariach, które **nie są** udostępniane podmiotom trzecim. Funkcję tę można wyłączyć w aplikacji webowej: :gear: → **Wszystkie ustawienia** → **Konto** → **Bezpieczeństwo i prywatność** → **Prywatność i gromadzenie danych**.

#### :material-check:{ .pg-green } Własne domeny i aliasy

Płatni użytkownicy Proton Mail mogą korzystać z własnej domeny lub z adresu typu [catch-all](https://proton.me/pl/support/catch-all). Proton Mail obsługuje również [sub-adresowanie](https://proton.me/pl/support/creating-aliases), przydatne dla osób, które nie chcą kupować własnej domeny.

#### :material-check:{ .pg-green } Prywatne metody płatności

Proton Mail [akceptuje](https://proton.me/pl/support/payment-options) płatność **gotówką** wysłaną pocztą, a także standardowe płatności kartą kredytową/debetową, [Bitcoinem](advanced/payments.md#other-coins-bitcoin-ethereum-etc) oraz przez PayPal.

#### :material-check:{ .pg-green } Bezpieczeństwo konta

Proton Mail obsługuje [uwierzytelnianie dwuskładnikowe](https://proton.me/pl/support/two-factor-authentication-2fa) hasłem jednorazowym ograniczonym czasowo (TOTP) oraz [sprzętowe klucze bezpieczeństwa](https://proton.me/pl/support/2fa-security-key) zgodne ze standardami FIDO2 lub U2F. Aby skorzystać z klucza bezpieczeństwa, należy najpierw skonfigurować uwierzytelnianie TOTP.

#### :material-check:{ .pg-green } Bezpieczeństwo danych

Proton Mail stosuje [szyfrowanie z zerowym dostępem](https://proton.me/blog/zero-access-encryption) (zero-access encryption) dla Twoich wiadomości e-mail oraz [kalendarzy](https://proton.me/news/protoncalendar-security-model). Dane zabezpieczone tym mechanizmem są dostępne wyłącznie dla Ciebie.

Niektóre informacje przechowywane w [Proton Contacts](https://proton.me/pl/support/proton-contacts), takie jak wyświetlane nazwy czy adresy e-mail, nie są objęte szyfrowaniem z zerowym dostępem. Pola kontaktów, które wspierają ten rodzaj szyfrowania (np. numery telefonów), są oznaczone ikoną kłódki.

#### :material-check:{ .pg-green } Szyfrowanie wiadomości e-mail

Proton Mail ma [zintegrowane szyfrowanie OpenPGP](https://proton.me/pl/support/how-to-use-pgp) w swojej aplikacji webowej. Wiadomości między kontami Proton Mail są szyfrowane automatycznie, a szyfrowanie do adresów spoza Proton Mail, które posiadają klucz OpenPGP, można łatwo włączyć w ustawieniach konta. Proton obsługuje również automatyczne wyszukiwanie zewnętrznych kluczy publicznych przez Katalog kluczy publicznych (WKD). Oznacza to, że wiadomości wysyłane do innych dostawców korzystających z WKD będą automatycznie szyfrowane za pomocą OpenPGP, bez konieczności ręcznej wymiany kluczy PGP z kontaktami. Proton Mail umożliwia także [szyfrowanie wiadomości do adresów spoza Proton Mail bez użycia OpenPGP](https://proton.me/support/password-protected-emails) — odbiorca nie musi zakładać konta Proton Mail, by taką wiadomość odczytać.

Proton Mail publikuje również klucze publiczne kont Proton poprzez HTTP w swoim WKD. Dzięki temu osoby spoza Proton Mail mogą łatwo znaleźć klucze OpenPGP kont Proton Mail i korzystać z szyfrowanej komunikacji między różnymi dostawcami (E2EE). Dotyczy to wyłącznie adresów e-mail zakończonych jedną z domen Proton, np. `@proton.me`. Jeśli korzystasz z własnej domeny, musisz [skonfigurować WKD](basics/email-security.md#what-is-the-web-key-directory-standard) osobno.

#### :material-information-outline:{ .pg-blue } Zamknięcie konta

Jeśli posiadasz konto płatne i Twój [rachunek pozostaje nieopłacony](https://proton.me/pl/support/delinquency) przez 14 dni, utracisz dostęp do swoich danych. Po 30 dniach konto zostanie oznaczone jako zaległe i przestanie odbierać nowe wiadomości, przy czym nadal będzie naliczana opłata. Proton [usuwa nieaktywne darmowe konta](https://proton.me/pl/support/inactive-accounts) po upływie jednego roku. **Nie można** ponownie użyć adresu e-mail powiązanego z dezaktywowanym kontem.

#### :material-information-outline:{ .pg-blue } Dodatkowe funkcje

Plan [Proton Unlimited](https://proton.me/pl/support/proton-plans#proton-unlimited) umożliwia dostęp do innych usług Proton, a także zapewnia korzystanie z wielu własnych domen, nieograniczonej liczby aliasów z funkcją hide-my-email oraz 500 GB przestrzeni dyskowej.

### Poczta Mailbox

<div class="admonition recommendation" markdown>

![Logo Mailbox.org](assets/img/email/mailbox-mail.svg){ align=right }

Poczta **Mailbox** to usługa e-mail skoncentrowana na bezpieczeństwie, braku reklam oraz korzystaniu w 100% z energii pochodzącej ze źródeł odnawialnych. Działa od 2014 roku. Mailbox ma siedzibę w Berlinie, w Niemczech.

Konta oferują do 2 GB przestrzeni, którą można zwiększyć w razie potrzeby.

[:octicons-home-16: Strona główna](https://mailbox.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://mailbox.org/en/data-protection-privacy-policy){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://kb.mailbox.org/en/private){ .card-link title="Dokumentacja" }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:octicons-browser-16: W przeglądarce](https://login.mailbox.org)

</details>

</div>

#### :material-check:{ .pg-green } Własne domeny i aliasy

Poczta Mailbox umożliwia korzystanie z własnej domeny oraz obsługuje adresy typu [catch-all](https://kb.mailbox.org/en/private/custom-domains/how-to-set-up-a-catch-all-alias-with-a-custom-domain-name). Usługa wspiera również [sub-adresowanie](https://proton.me/pl/support/creating-aliases), przydatne dla osób, które nie chcą kupować własnej domeny.

#### :material-check:{ .pg-green } Prywatne metody płatności

Poczta Mailbox nie akceptuje żadnych kryptowalut, ponieważ ich operator płatności BitPay zawiesił działalność w Niemczech. Akceptowane są natomiast płatności **gotówką** wysyłaną pocztą, **gotówką** wpłacaną na konto bankowe, przelewem, kartą kredytową, przez PayPal, a także przez niemieckie systemy płatności Paydirekt i Sofortüberweisung.

#### :material-check:{ .pg-green } Bezpieczeństwo konta

Poczta Mailbox obsługuje [uwierzytelnianie dwuskładnikowe](https://kb.mailbox.org/en/private/account-article/how-to-use-two-factor-authentication-2fa) wyłącznie dla swojej aplikacji webowej. Można używać metody TOTP lub klucza [YubiKey](security-keys.md#yubikey) za pośrednictwem [YubiCloud](https://yubico.com/products/services-software/yubicloud). Standardy webowe, takie jak [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online), nie są jeszcze obsługiwane.

#### :material-information-outline:{ .pg-blue } Bezpieczeństwo danych

Poczta Mailbox umożliwia szyfrowanie przychodzących wiadomości za pomocą [szyfrowanej skrzynki pocztowej](https://kb.mailbox.org/en/private/e-mail-article/your-encrypted-mailbox). Nowe wiadomości, które otrzymujesz, są automatycznie szyfrowane Twoim kluczem publicznym.

Jednak oprogramowanie [Open-Xchange](https://pl.wikipedia.org/wiki/Open-Xchange), z którego korzysta poczta Mailbox, [nie obsługuje](https://kb.mailbox.org/en/private/security-privacy-article/encryption-of-calendar-and-address-book) szyfrowania książki adresowej ani kalendarza. Do tych danych bardziej odpowiednie może być [oddzielne rozwiązanie](calendar.md).

#### :material-check:{ .pg-green } Szyfrowanie wiadomości e-mail

Poczta Mailbox ma [zintegrowane szyfrowanie](https://kb.mailbox.org/en/private/e-mail-article/send-encrypted-e-mails-with-guard) w swojej aplikacji webowej, co ułatwia wysyłanie wiadomości do osób posiadających publiczne klucze OpenPGP. Umożliwia również [odszyfrowanie wiadomości przez odbiorcę zdalnego](https://kb.mailbox.org/en/private/e-mail-article/my-recipient-does-not-use-pgp) na serwerach poczty Mailbox. Ta funkcja jest przydatna, gdy zdalny odbiorca nie posiada OpenPGP i nie może samodzielnie odszyfrować wiadomości we własnej skrzynce pocztowej.

Poczta Mailbox obsługuje także wyszukiwanie kluczy publicznych przez HTTP za pośrednictwem swojego WKD. Dzięki temu osoby spoza poczty Mailbox mogą łatwo znaleźć klucze OpenPGP kont Mailbox i korzystać z szyfrowanej komunikacji między różnymi dostawcami (E2EE). Dotyczy to wyłącznie adresów e-mail zakończonych jedną z domen Mailbox, np. `@mailbox.org`. Jeśli korzystasz z własnej domeny, musisz [skonfigurować WKD](basics/email-security.md#what-is-the-web-key-directory-standard) osobno.

#### :material-information-outline:{ .pg-blue } Zamknięcie konta

Twoje konto zostanie przekształcone w konto o ograniczonych uprawnieniach po zakończeniu umowy. Następnie zostanie nieodwracalnie usunięte po upływie [30 dni](https://kb.mailbox.org/en/private/payment-article/what-happens-at-the-end-of-my-contract).

#### :material-information-outline:{ .pg-blue } Dodatkowe funkcje

Do konta poczty Mailbox można uzyskać dostęp za pośrednictwem protokołu IMAP/SMTP, korzystając z ich [usługi .onion](https://kb.mailbox.org/en/private/faq-article/the-tor-exit-node-of-mailbox-org). Jednak interfejs aplikacji webowej nie jest dostępny przez adres .onion, a przy korzystaniu z niego mogą występować błędy certyfikatów TLS.

Wszystkie konta mają ograniczoną przestrzeń w chmurze, która [może być szyfrowana](https://kb.mailbox.org/en/private/drive-article/encrypt-files-on-your-drive). Poczta Mailbox oferuje także alias [@secure.mailbox.org](https://kb.mailbox.org/en/private/e-mail-article/ensuring-e-mails-are-sent-securely), który wymusza szyfrowanie TLS połączenia między serwerami pocztowymi — w przeciwnym razie wiadomość nie zostanie wysłana. Poczta Mailbox obsługuje również [Exchange ActiveSync](https://en.wikipedia.org/wiki/Exchange_ActiveSync), oprócz standardowych protokołów dostępu takich jak IMAP i POP3.

Poczta Mailbox oferuje funkcję cyfrowego spadku we wszystkich planach. Możesz zdecydować, czy chcesz, aby Twoje dane zostały przekazane spadkobiercom, pod warunkiem, że złożą odpowiedni wniosek i przedstawią testament. Alternatywnie możesz wskazać konkretną osobę, podając jej imię, nazwisko i adres.

## Więcej dostawców

These providers store your emails with zero-knowledge encryption, making them great options for keeping your stored emails secure. However, they don't support interoperable encryption standards for E2EE communications between different providers.

<div class="grid cards" markdown>

- ![Tuta logo](assets/img/email/tuta.svg#only-light){ .twemoji loading=lazy }![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ .twemoji loading=lazy } [Tuta](#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Tuta logo](assets/img/email/tuta.svg#only-light){ align=right }
![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ align=right }

**Tuta** (formerly *Tutanota*) is an email service with a focus on security and privacy through the use of encryption. Tuta has been in operation since 2011 and is based in Hanover, Germany.

Free accounts start with 1 GB of storage.

[:octicons-home-16: Homepage](https://tuta.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tuta.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://tuta.com/support){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="Source Code" }
[:octicons-heart-16:](https://tuta.com/community){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
- [:simple-appstore: App Store](https://apps.apple.com/app/id922429609)
- [:simple-github: GitHub](https://github.com/tutao/tutanota/releases)
- [:fontawesome-brands-windows: Windows](https://tuta.com/#download)
- [:simple-apple: macOS](https://tuta.com/#download)
- [:simple-linux: Linux](https://tuta.com/#download)
- [:octicons-browser-16: Web](https://app.tuta.com)

</details>

</div>

Tuta doesn't support the [IMAP protocol](https://tuta.com/support#imap) or the use of third-party [email clients](email-clients.md), and you also won't be able to add [external email accounts](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) to the Tuta app. [Email import](https://github.com/tutao/tutanota/issues/630) is not currently supported either, though this is [due to be changed](https://tuta.com/blog/kickoff-import). Emails can be exported [individually or by bulk selection](https://tuta.com/support#generalMail) per folder, which may be inconvenient if you have many folders.

#### :material-check:{ .pg-green } Własne domeny i aliasy

Paid Tuta accounts can use either 15 or 30 aliases depending on their plan and unlimited aliases on [custom domains](https://tuta.com/support#custom-domain). Tuta doesn't allow for [sub-addressing (plus addresses)](https://tuta.com/support#plus), but you can use a [catch-all](https://tuta.com/support#settings-global) with a custom domain.

#### :material-information-outline:{ .pg-blue } Private Payment Methods

Tuta only directly accepts credit cards and PayPal, however [**cryptocurrency**](cryptocurrency.md) can be used to purchase gift cards via their [partnership](https://tuta.com/support/#cryptocurrency) with ProxyStore.

#### :material-check:{ .pg-green } Bezpieczeństwo konta

Tuta supports [two-factor authentication](https://tuta.com/support#2fa) with either TOTP or U2F.

#### :material-check:{ .pg-green } Bezpieczeństwo danych

Tuta has [zero-access encryption at rest](https://tuta.com/support#what-encrypted) for your emails, [address book contacts](https://tuta.com/support#encrypted-address-book), and [calendars](https://tuta.com/support#calendar). This means the messages and other data stored in your account are only readable by you.

#### :material-information-outline:{ .pg-blue } Email Encryption

Tuta [does not use OpenPGP](https://tuta.com/support/#pgp). Tuta accounts can only receive encrypted emails from non-Tuta email accounts when sent via a [temporary Tuta mailbox](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } Zamknięcie konta

Tuta will [delete inactive free accounts](https://tuta.com/support#inactive-accounts) after six months. You can reuse a deactivated free account if you pay.

#### :material-information-outline:{ .pg-blue } Dodatkowe funkcje

Tuta offers the business version of [Tuta to non-profit organizations](https://tuta.com/blog/secure-email-for-non-profit) for free or with a heavy discount.

## Criteria

**Please note we are not affiliated with any of the providers we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements for any email provider wishing to be recommended, including implementing industry best practices, modern technology and more. We suggest you familiarize yourself with this list before choosing an email provider, and conduct your own research to ensure the email provider you choose is the right choice for you.

### Technologia

We regard these features as important in order to provide a safe and optimal service. You should consider whether the provider has the features you require.

**Minimum do zakwalifikowania się:**

- Must encrypt email account data at rest with zero-access encryption.
- Must be capable of exporting emails as [Mbox](https://en.wikipedia.org/wiki/Mbox) or individual .EML with [RFC5322](https://datatracker.ietf.org/doc/rfc5322) standard.
- Allow users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). Custom domain names are important to users because it allows them to maintain their agency from the service, should it turn bad or be acquired by another company which doesn't prioritize privacy.
- Must operate on owned infrastructure, i.e. not built upon third-party email service providers.

**Najlepszy scenariusz:**

- Should encrypt all account data (contacts, calendars, etc.) at rest with zero-access encryption.
- Should provide integrated webmail E2EE/PGP encryption as a convenience.
- Should support WKD to allow improved discovery of public OpenPGP keys via HTTP. GnuPG users can get a key with this command: `gpg --locate-key example_user@example.com`.
- Support for a temporary mailbox for external users. This is useful when you want to send an encrypted email without sending an actual copy to your recipient. These emails usually have a limited lifespan and then are automatically deleted. They also don't require the recipient to configure any cryptography like OpenPGP.
- Should support [sub-addressing](https://en.wikipedia.org/wiki/Email_address#Sub-addressing).
- Should allow users to use their own [domain name](https://en.wikipedia.org/wiki/Domain_name). Custom domain names are important to users because it allows them to maintain their agency from the service, should it turn bad or be acquired by another company which doesn't prioritize privacy.
- Catch-all or alias functionality for those who use their own domains.
- Should use standard email access protocols such as IMAP, SMTP, or [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol). Standard access protocols ensure customers can easily download all of their email, should they want to switch to another provider.
- Email provider's services should be available via an [onion service](https://en.wikipedia.org/wiki/.onion).

### Prywatność

Preferujemy, aby nasi rekomendowani dostawcy gromadzili jak najmniej danych.

**Minimum do zakwalifikowania się:**

- Must protect sender's IP address, which can involve filtering it from showing in the `Received` header field.
- Must not require personally identifiable information (PII) besides a username and a password.
- Privacy policy must meet the requirements defined by the GDPR.

**Najlepszy scenariusz:**

- Should accept [anonymous payment options](advanced/payments.md) ([cryptocurrency](cryptocurrency.md), cash, gift cards, etc.)
- Should be hosted in a jurisdiction with strong email privacy protection laws.

### Bezpieczeństwo

Email servers deal with a lot of very sensitive data. We expect that providers will adopt industry best practices in order to protect their customers.

**Minimum do zakwalifikowania się:**

- Protection of webmail with 2FA, such as [TOTP](basics/multi-factor-authentication.md#time-based-one-time-password-totp).
- Zero-access encryption, which builds on encryption at rest. The provider does not have the decryption keys to the data they hold. This prevents a rogue employee leaking data they have access to or remote adversary from releasing data they have stolen by gaining unauthorized access to the server.
- [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions) support.
- No TLS errors or vulnerabilities when being profiled by tools such as [Hardenize](https://hardenize.com), [testssl.sh](https://testssl.sh), or [Qualys SSL Labs](https://ssllabs.com/ssltest); this includes certificate related errors and weak DH parameters, such as those that led to [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- A server suite preference (optional on TLS 1.3) for strong cipher suites which support forward secrecy and authenticated encryption.
- A valid [MTA-STS](https://tools.ietf.org/html/rfc8461) and [TLS-RPT](https://tools.ietf.org/html/rfc8460) policy.
- Valid [DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities) records.
- Valid [SPF](https://en.wikipedia.org/wiki/Sender_Policy_Framework) and [DKIM](https://en.wikipedia.org/wiki/DomainKeys_Identified_Mail) records.
- Must have a proper [DMARC](https://en.wikipedia.org/wiki/DMARC) record and policy or use [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) for authentication. If DMARC authentication is being used, the policy must be set to `reject` or `quarantine`.
- A server suite preference of TLS 1.2 or later and a plan for [RFC8996](https://datatracker.ietf.org/doc/rfc8996).
- [SMTPS](https://en.wikipedia.org/wiki/SMTPS) submission, assuming SMTP is used.
- Website security standards such as:
    - [HTTP Strict Transport Security](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - [Subresource Integrity](https://en.wikipedia.org/wiki/Subresource_Integrity) if loading things from external domains.
- Must support viewing of [message headers](https://en.wikipedia.org/wiki/Email#Message_header), as it is a crucial forensic feature to determine if an email is a phishing attempt.

**Najlepszy scenariusz:**

- Should support hardware authentication, i.e. U2F and [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online).
- [DNS Certification Authority Authorization (CAA) Resource Record](https://tools.ietf.org/html/rfc6844) in addition to DANE support.
- Should implement [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), which is useful for people who post to mailing lists [RFC8617](https://tools.ietf.org/html/rfc8617).
- Published security audits from a reputable, third-party firm.
- Programy Bug-Bounty i/lub skoordynowany proces ujawniania luk w zabezpieczeniach.
- Website security standards such as:
    - [Content Security Policy (CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### Zaufanie

You wouldn't trust your finances to someone with a fake identity, so why trust them with your email? Wymagamy, aby rekomendowani przez nas dostawcy publicznie informowali o swojej własności lub przywództwie. Chcielibyśmy również widzieć częste raporty przejrzystości, zwłaszcza w odniesieniu do sposobu obsługi wniosków rządowych.

**Minimum do zakwalifikowania się:**

- Publiczne przywództwo lub własność.

**Najlepszy scenariusz:**

- Częste raporty przejrzystości.

### Marketing

With the email providers we recommend, we like to see responsible marketing.

**Minimum do zakwalifikowania się:**

- Must self-host analytics (no Google Analytics, Adobe Analytics, etc.).
- Must not have any irresponsible marketing, which can include the following:
    - Claims of "unbreakable encryption." Encryption should be used with the intention that it may not be secret in the future when the technology exists to crack it.
    - Guarantees of protecting anonymity 100%. When someone makes a claim that something is 100%, it means there is no certainty for failure. We know people can quite easily de-anonymize themselves in a number of ways, e.g.:
        - Reusing personal information e.g. (email accounts, unique pseudonyms, etc.) that they accessed without anonymity software such as Tor
        - [Browser Fingerprinting](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**Najlepszy scenariusz:**

- Clear and easy-to-read documentation for tasks like setting up 2FA, email clients, OpenPGP, etc.

### Dodatkowa funkcjonalność

While not strictly requirements, there are some other convenience or privacy factors we looked into when determining which providers to recommend.
