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

| Dostawca                        | OpenPGP / WKD                          | IMAP / SMTP                                                         | Szyfrowanie z zerowym dostępem                          | Anonimowe metody płatności                                 |
| ------------------------------- | -------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------- | ---------------------------------------------------------- |
| [Proton Mail](#proton-mail)     | :material-check:{ .pg-green }          | :material-information-outline:{ .pg-blue } Tylko w płatnych planach | :material-check:{ .pg-green }                           | Gotówka <br>Monero przez pośrednika                  |
| [Poczta Mailbox](#mailbox-mail) | :material-check:{ .pg-green }          | :material-check:{ .pg-green }                                       | :material-information-outline:{ .pg-blue } Tylko poczta | Gotówka                                                    |
| [Tuta](#tuta)                   | :material-alert-outline:{ .pg-orange } | :material-alert-outline:{ .pg-orange }                              | :material-check:{ .pg-green }                           | Monero przez pośrednika <br>Gotówka przez pośrednika |

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

Konta bezpłatne mają pewne ograniczenia, takie jak brak możliwości wyszukiwania w treści wiadomości oraz brak dostępu do [Proton Mail Bridge](https://proton.me/pl/mail/bridge), który jest wymagany do korzystania z [zalecanego klienta poczty desktopowej](email-clients.md), np. Thunderbird. Konta płatne obejmują funkcje takie jak Proton Mail Bridge, dodatkową przestrzeń dyskową oraz obsługę własnych domen. Plan Proton Unlimited lub dowolny plan dla wielu użytkowników obejmuje darmowy dostęp do [SimpleLogin](email-aliasing.md#simplelogin) Premium.

[Raport potwierdzający bezpieczeństwo](https://res.cloudinary.com/dbulfrlrz/images/v1714639878/wp-pme/letter-of-attestation-proton-mail-20211109_3138714c61/letter-of-attestation-proton-mail-20211109_3138714c61.pdf) aplikacji Proton Mail został wydany 9 listopada 2021 roku przez firmę [Securitum](https://research.securitum.com).

Proton Mail gromadzi wewnętrzne raporty o awariach, które **nie są** udostępniane podmiotom trzecim i które mogą zostać wyłączone.

=== "W przeglądarce"

    Z poziomu skrzynki odbiorczej wybierz :gear: → **Wszystkie ustawienia** → **Konto** → **Bezpieczeństwo i prywatność** → **Prywatność i gromadzenie danych**.

    - [ ] Disable **Collect usage dignostics**
    - [ ] Disable **Send crash reports**

=== "W aplikacji mobilnej"

    Z poziomu skrzynki odbiorczej wybierz :material-menu: → :gear: **Ustawienia** → wybierz swoją nazwę użytkownika.

    - [ ] Disable **Send crash reports**
    - [ ] Disable **Collect usage dignostics**

#### :material-check:{ .pg-green } Własne domeny i aliasy

Płatni użytkownicy Proton Mail mogą korzystać z własnej domeny lub z adresu typu [catch-all](https://proton.me/pl/support/catch-all). Proton Mail obsługuje również [sub-adresowanie](https://proton.me/pl/support/creating-aliases), przydatne dla osób, które nie chcą kupować własnej domeny.

#### :material-check:{ .pg-green } Prywatne metody płatności

Proton Mail [akceptuje](https://proton.me/pl/support/payment-options) płatność **gotówką** wysłaną pocztą, a także standardowe płatności kartą kredytową/debetową, [Bitcoinem](advanced/payments.md#other-coins-bitcoin-ethereum-etc) oraz przez PayPal. Additionally, you can use [**Monero**](cryptocurrency.md#monero) to purchase vouchers for Proton Mail Plus or Proton Unlimited via their [official](https://discuss.privacyguides.net/t/add-monero-as-an-anonymous-payment-method-for-proton-services/31058/15) reseller [ProxyStore](https://dys2p.com/en/2025-09-09-proton.html).

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

Poczta **Mailbox** (wcześniej **Mailbox.org**) to usługa e-mail skoncentrowana na bezpieczeństwie, braku reklam oraz korzystaniu w 100% z energii pochodzącej ze źródeł odnawialnych. Działa od 2014 roku. Mailbox ma siedzibę w Berlinie, w Niemczech.

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

## Inni dostawcy

Ci dostawcy przechowują Twoje wiadomości e-mail z wykorzystaniem szyfrowania z wiedzą zerową, co czyni ich doskonałym wyborem do bezpiecznego przechowywania poczty. Nie obsługują jednak interoperacyjnych standardów szyfrowania dla komunikacji E2EE między różnymi usługami.

<div class="grid cards" markdown>

- ![Logo Tuta](assets/img/email/tuta.svg#only-light){ .twemoji loading=lazy }![Logo Tuta](assets/img/email/tuta-dark.svg#only-dark){ .twemoji loading=lazy } [Tuta](#tuta)

</div>

### Tuta

<div class="admonition recommendation" markdown>

![Tuta logo](assets/img/email/tuta.svg#only-light){ align=right }
![Tuta logo](assets/img/email/tuta-dark.svg#only-dark){ align=right }

**Tuta** (wcześniej *Tutanota*) to usługa e-mail koncentrująca się na bezpieczeństwie i prywatności poprzez wykorzystanie szyfrowania. Działa od 2011 roku i ma siedzibę w Hanowerze, w Niemczech.

Darmowe konta oferują 1 GB przestrzeni.

[:octicons-home-16: Strona główna](https://tuta.com/pl){ .md-button .md-button--primary }
[:octicons-eye-16:](https://tuta.com/privacy-policy){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://tuta.com/pl/support){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/tutao/tutanota){ .card-link title="Kod źródłowy" }
[:octicons-heart-16:](https://tuta.com/pl/community){ .card-link title="Wspomóż projekt" }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=de.tutao.tutanota)
- [:simple-appstore: App Store](https://apps.apple.com/app/id922429609)
- [:simple-github: GitHub](https://github.com/tutao/tutanota/releases)
- [:fontawesome-brands-windows: Windows](https://tuta.com/pl#download)
- [:simple-apple: macOS](https://tuta.com/pl/#download)
- [:simple-linux: Linux](https://tuta.com/pl/#download)
- [:octicons-browser-16: W przeglądarce](https://app.tuta.com)

</details>

</div>

Tuta nie obsługuje [protokołu IMAP](https://tuta.com/support#imap) ani korzystania z [zewnętrznych klientów poczty](email-clients.md). Nie jest także możliwe dodawanie [zewnętrznych kont e-mail](https://github.com/tutao/tutanota/issues/544#issuecomment-670473647) do aplikacji Tuta. [Import wiadomości e-mail](https://github.com/tutao/tutanota/issues/630) nie jest obecnie obsługiwany, choć [planowane są zmiany](https://tuta.com/blog/kickoff-import). Wiadomości można eksportować [pojedynczo lub grupowo](https://tuta.com/pl/support#generalMail) w ramach każdego folderu, co może być niewygodne w przypadku dużej liczby folderów.

#### :material-check:{ .pg-green } Własne domeny i aliasy

Płatne konta Tuta pozwalają na użycie 15 lub 30 aliasów w zależności od planu oraz nieograniczonej liczby aliasów w przypadku [niestandardowych domen](https://tuta.com/pl/support#custom-domain). Tuta nie obsługuje [sub-adresowania (adresów z plusem)](https://tuta.com/pl/support#plus), ale umożliwia korzystanie z adresu [catch-all](https://tuta.com/pl/support#settings-global) (skrzynki zbiorczej) dla własnej domeny.

#### :material-information-outline:{ .pg-blue } Prywatne metody płatności

Tuta bezpośrednio akceptuje wyłącznie płatności kartą kredytową oraz przez PayPal. Jednak [**kryptowalutami**](cryptocurrency.md) można zapłacić pośrednio, kupując karty podarunkowe poprzez [współpracę](https://tuta.com/support/#cryptocurrency) z ProxyStore.

#### :material-check:{ .pg-green } Bezpieczeństwo konta

Tuta obsługuje [uwierzytelnianie dwuskładnikowe](https://tuta.com/pl/support#2fa) z użyciem TOTP lub U2F.

#### :material-check:{ .pg-green } Bezpieczeństwo danych

Tuta stosuje [szyfrowanie z zerowym dostępem](https://tuta.com/pl/support#what-encrypted) (zero-access encryption) dla Twoich wiadomości e-mail, [kontaktów w książce adresowej](https://tuta.com/pl/support#encrypted-address-book) oraz [kalendarza](https://tuta.com/pl/support#calendar). Oznacza to, że wiadomości i inne dane przechowywane na Twoim koncie mogą być odczytane wyłącznie przez Ciebie.

#### :material-information-outline:{ .pg-blue } Szyfrowanie wiadomości e-mail

Tuta [nie korzysta z OpenPGP](https://tuta.com/pl/support/#pgp). Konta Tuta mogą otrzymywać zaszyfrowane wiadomości e-mail od użytkowników spoza tej usługi wyłącznie wtedy, gdy są one wysłane za pośrednictwem [tymczasowej skrzynki pocztowej Tuta](https://tuta.com/support/#encrypted-email-external).

#### :material-information-outline:{ .pg-blue } Zamknięcie konta

Tuta [usuwa nieaktywne darmowe konta](https://tuta.com/pl/support#inactive-accounts) po upływie sześciu miesięcy. Można jednak ponownie aktywować dezaktywowane konto darmowe, jeśli zostanie opłacone.

#### :material-information-outline:{ .pg-blue } Dodatkowe funkcje

Tuta oferuje wersję biznesową swojej usługi [organizacjom non-profit](https://tuta.com/blog/secure-email-for-non-profit) bezpłatnie lub z dużym rabatem.

## Kryteria

**Należy pamiętać, że nie jesteśmy powiązani z żadnym z polecanych przez nas dostawców.** Oprócz [naszych standardowych kryteriów](about/criteria.md) opracowaliśmy jasny zestaw wymagań, które musi spełniać każdy dostawca usług e-mail, aby mógł być przez nas polecany — obejmują one wdrożenie najlepszych praktyk branżowych, nowoczesnych technologii i nie tylko. Sugerujemy zapoznanie się z tą listą przed wyborem dostawcy poczty e-mail i przeprowadzenie własnych badań, aby upewnić się, że wybrany dostawca będzie dla Ciebie odpowiedni.

### Technologia

Poniższe funkcje uznajemy za istotne dla zapewnienia bezpiecznej i wydajnej usługi. Warto rozważyć, czy wybrany dostawca oferuje funkcje, których potrzebujesz.

**Minimalne wymagania:**

- Musi szyfrować dane kont e-mail w spoczynku przy użyciu szyfrowania z zerowym dostępem (zero-access encryption).
- Musi umożliwiać eksport wiadomości e-mail w formacie [mbox](https://pl.wikipedia.org/wiki/Mbox) lub jako pojedyncze pliki .EML zgodne ze standardem [RFC5322](https://datatracker.ietf.org/doc/rfc5322).
- Musi pozwalać użytkownikom na korzystanie z własnej [nazwy domeny](https://pl.wikipedia.org/wiki/Domena_internetowa). Własne domeny są istotne, ponieważ pozwalają użytkownikowi zachować niezależność od dostawcy, jeśli ten np. zmieni właściciela lub przestanie dbać o prywatność.
- Musi działać na własnej infrastrukturze, tj. nie może być zbudowany w oparciu o zewnętrzne platformy e-mailowe.

**Najlepszy scenariusz:**

- Powinien szyfrować wszystkie dane konta (kontakty, kalendarze itp.) w spoczynku przy użyciu szyfrowania z zerowym dostępem.
- Powinien oferować zintegrowane szyfrowanie E2EE/PGP w webmailu dla wygody użytkownika.
- Powinien obsługiwać WKD, aby umożliwić łatwiejsze wyszukiwanie publicznych kluczy OpenPGP poprzez HTTP. Użytkownicy GnuPG mogą pobrać klucz poleceniem: `gpg --locate-key uzytkownik@example.com`.
- Powinien wspierać funkcję tymczasowej skrzynki pocztowej dla użytkowników zewnętrznych — przydatną do wysyłania zaszyfrowanych wiadomości bez przekazywania ich kopii odbiorcy. Takie wiadomości mają zwykle ograniczoną żywotność i są automatycznie usuwane; odbiorca nie musi konfigurować żadnych narzędzi kryptograficznych jak OpenPGP.
- Powinien obsługiwać [sub-adresowanie](https://en.wikipedia.org/wiki/Email_address#Sub-addressing).
- Powinien pozwalać użytkownikom na korzystanie z własnej [nazwy domeny](https://pl.wikipedia.org/wiki/Domena_internetowa). Własne domeny są istotne, ponieważ pozwalają użytkownikowi zachować niezależność od dostawcy, jeśli ten np. zmieni właściciela lub przestanie dbać o prywatność.
- Powinien wspierać adresy typu catch-all lub aliasy dla użytkowników korzystających z własnych domen.
- Powinien korzystać ze standardowych protokołów dostępu do poczty, takich jak IMAP, SMTP lub [JMAP](https://en.wikipedia.org/wiki/JSON_Meta_Application_Protocol), co umożliwia łatwe pobranie wszystkich wiadomości w przypadku zmiany dostawcy.
- Usługi dostawcy powinny być dostępne również przez [usługę .onion](https://pl.wikipedia.org/wiki/.onion).

### Prywatność

Preferujemy, aby zalecani przez nas dostawcy gromadzili możliwie najmniej danych.

**Minimalne wymagania:**

- Musi chronić adres IP nadawcy, np. poprzez usuwanie go z nagłówka `Received`.
- Nie może wymagać danych osobowych (PII) innych niż nazwa użytkownika i hasło.
- Polityka prywatności musi spełniać wymogi określone przez RODO.

**Najlepszy scenariusz:**

- Powinien akceptować [anonimowe metody płatności](advanced/payments.md) ([kryptowaluty](cryptocurrency.md), gotówkę, karty podarunkowe itp.).
- Powinien być hostowany w jurysdykcji oferującej silną ochronę prywatności komunikacji e-mailowej.

### Bezpieczeństwo

Serwery pocztowe przetwarzają ogromne ilości wrażliwych danych. Oczekujemy, że dostawcy będą stosować najlepsze praktyki branżowe w celu ochrony swoich klientów.

**Minimalne wymagania:**

- Ochrona dostępu do webmaila z użyciem 2FA, np. [TOTP](basics/multi-factor-authentication.md#time-based-one-time-password-totp).
- Szyfrowanie z zerowym dostępem, będące rozszerzeniem szyfrowania danych w spoczynku — dostawca nie posiada kluczy deszyfrujących dane, co uniemożliwia wyciek informacji przez nieuczciwego pracownika lub zewnętrznego atakującego po uzyskaniu nieautoryzowanego dostępu do serwera.
- Obsługa [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions).
- Brak błędów lub luk TLS podczas testów za pomocą narzędzi takich jak [Hardenize](https://hardenize.com), [testssl.sh](https://testssl.sh) czy [Qualys SSL Labs](https://ssllabs.com/ssltest); dotyczy to błędów certyfikatów i słabych parametrów DH, takich jak te, które doprowadziły do podatności [Logjam](https://en.wikipedia.org/wiki/Logjam_(computer_security)).
- Preferencja serwera dla silnych zestawów szyfrów obsługujących utajnianie z wyprzedzeniem oraz uwierzytelnione szyfrowanie (dla TLS 1.3 opcjonalna).
- Prawidłowo wdrożone polityki [MTA-STS](https://tools.ietf.org/html/rfc8461) i [TLS-RPT](https://tools.ietf.org/html/rfc8460).
- Prawidłowe rekordy [DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities).
- Prawidłowe rekordy [SPF](https://pl.wikipedia.org/wiki/Sender_Policy_Framework) oraz [DKIM](https://pl.wikipedia.org/wiki/DomainKeys_Identified_Mail).
- Poprawnie skonfigurowany rekord i polityka [DMARC](https://en.wikipedia.org/wiki/DMARC) lub alternatywnie użycie [ARC](https://en.wikipedia.org/wiki/Authenticated_Received_Chain) do uwierzytelniania. If DMARC authentication is being used, the policy must be set to `reject` or `quarantine`.
- Preferencja serwera dla TLS 1.2 lub nowszego oraz plan przejścia na zgodność z [RFC8996](https://datatracker.ietf.org/doc/rfc8996).
- Obsługa [SMTPS](https://en.wikipedia.org/wiki/SMTPS) przy założeniu, że używany jest protokół SMTP.
- Wdrożenie standardów bezpieczeństwa stron internetowych, takich jak:
    - [HTTP Strict Transport Security (HSTS)](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)
    - [Subresource Integrity (SRI)](https://en.wikipedia.org/wiki/Subresource_Integrity) przy ładowaniu zasobów z domen zewnętrznych.
- Musi umożliwiać podgląd [nagłówków wiadomości e-mail](https://en.wikipedia.org/wiki/Email#Message_header), co jest kluczowe przy analizie prób phishingu.

**Najlepszy scenariusz:**

- Powinien obsługiwać uwierzytelnianie sprzętowe, tj. U2F i [WebAuthn](basics/multi-factor-authentication.md#fido-fast-identity-online).
- Powinien posiadać rekord [DNS Certification Authority Authorization (CAA)](https://tools.ietf.org/html/rfc6844) oprócz obsługi DANE.
- Powinien implementować [Authenticated Received Chain (ARC)](https://en.wikipedia.org/wiki/Authenticated_Received_Chain), co jest przydatne dla osób korzystających z list mailingowych ([RFC8617](https://tools.ietf.org/html/rfc8617)).
- Opublikowane audyty bezpieczeństwa przeprowadzone przez renomowaną firmę zewnętrzną.
- Programy bug-bounty i/lub skoordynowany proces ujawniania podatności.
- Wdrożenie standardów bezpieczeństwa stron internetowych, takich jak:
    - [Content Security Policy (CSP)](https://en.wikipedia.org/wiki/Content_Security_Policy)
    - [RFC9163 Expect-CT](https://datatracker.ietf.org/doc/rfc9163)

### Zaufanie

Nie powierzył(a)byś swoich finansów komuś o fałszywej tożsamości, więc po co powierzać mu swoje dane e-mail? Wymagamy, aby zalecani przez nas dostawcy ujawniali informacje o właścicielach lub kadrze zarządzającej. Doceniamy również regularne raporty przejrzystości, szczególnie w zakresie tego, jak obsługiwane są żądania organów państwowych.

**Minimalne wymagania:**

- Publicznie dostępne informacje o właścicielu lub kadrze kierowniczej.

**Najlepszy scenariusz:**

- Regularnie publikowane raporty przejrzystości.

### Marketing

W przypadku polecanych przez nas dostawców poczty e-mail zwracamy uwagę na odpowiedzialne praktyki marketingowe.

**Minimalne wymagania:**

- Musi samodzielnie hostować analitykę (bez korzystania z Google Analytics, Adobe Analytics itp.).
- Nie może stosować nieodpowiedzialnych działań marketingowych, w tym m.in.:
    - Twierdzeń o „niemożliwym do złamania szyfrowaniu”. Należy zakładać, że każda forma szyfrowania może zostać w przyszłości złamana wraz z rozwojem technologii.
    - Gwarancji pełnej anonimowości w 100%. Kiedy ktoś zapewnia o 100% skuteczności czegoś, oznacza to, że nie ma żadnej pewności co do niepowodzenia. Zdajemy sobie sprawę, że ludzie mogą dość łatwo ujawnić swoją tożsamość na wiele sposobów, np.:
        - używając tych samych danych osobowych lub pseudonimów bez korzystania z narzędzi zapewniających anonimowość (np. Tor),
        - [przez unikalny odcisk przeglądarki (browser fingerprinting).](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)

**Najlepszy scenariusz:**

- Przejrzysta i czytelna dokumentacja dotycząca czynności takich jak konfiguracja uwierzytelniania dwuskładnikowego (2FA), klienta poczty elektronicznej, OpenPGP itp.

### Dodatkowe funkcje

Nie są to ścisłe wymagania, lecz czynniki zwiększające wygodę i prywatność użytkownika, które brane są pod uwagę przy ocenie dostawców poczty e-mail.
