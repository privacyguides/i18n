---
title: "Aliasy e-mail"
icon: material/email-lock
description: Usługa aliasingu adresów e-mail pozwala łatwo wygenerować nowy adres e-mail dla każdej witryny, w której się zarejestrujesz.
cover: email-aliasing.webp
---

<small>Chroni przed następującymi zagrożeniami:</small>

- [:material-account-cash: Kapitalizm inwigilacji](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }
- [:material-account-search: Ekspozycja publiczna](basics/common-threats.md#limiting-public-information){ .pg-green }

Usługa **aliasingu adresów e-mail** pozwala łatwo wygenerować nowy adres e-mail dla każdej witryny, w której się zarejestrujesz. The email aliases you generate are then forwarded to an email address of your choosing, hiding both your "main" email address and the identity of your [email provider](email.md).

Email aliasing can also act as a safeguard in case your email provider ever ceases operation. In that scenario, you can easily re-route your aliases to a new email address. In turn, however, you are placing trust in the aliasing service to continue functioning.

## Zalety

Using a service which allows you to individually manage email aliases has a number of benefits over conventional mailbox management/filtering methods:

### Over Plus Addressing

True email aliasing is better than plus addressing commonly used and supported by many providers, which allows you to create aliases like `yourname+[anythinghere]@example.com`, because websites, advertisers, and tracking networks can trivially remove anything after the `+` sign. Organizacje takie jak [IAB](https://en.wikipedia.org/wiki/Interactive_Advertising_Bureau) wymagają od reklamodawców [normalizacji adresów e-mail](https://shkspr.mobi/blog/2023/01/the-iab-loves-tracking-users-but-it-hates-users-tracking-them), aby można je było skorelować i śledzić, niezależnie od życzeń użytkowników dotyczących prywatności.

### Over Catch-All Aliases

Using a dedicated email aliasing service has a number of benefits over a catch-all alias on a custom domain:

- Aliases can be turned on and off individually when you need them, preventing websites from emailing you randomly.
- Replies are sent from the alias address, shielding your real email address.

### Over Temporary Email Services

Email aliasing services also have a number of benefits over "temporary email" services:

- Aliases are permanent and can be turned on again if you need to receive something like a password reset.
- Emails are sent to your trusted mailbox rather than stored by the alias provider.
- Temporary email services typically have public mailboxes which can be accessed by anyone who knows the address, while aliases are private to you.

## Zalecani dostawcy

<div class="grid cards" markdown>

- ![Logo Addy.io](assets/img/email-aliasing/addy.svg){ .twemoji } [Addy.io](email-aliasing.md#addyio)
- ![Logo SimpleLogin](assets/img/email-aliasing/simplelogin.svg){ .twemoji } [SimpleLogin](email-aliasing.md#simplelogin)

</div>

Our email aliasing recommendations are providers that allow you to create aliases on domains they control, as well as on your own custom domain(s) for a modest yearly fee. They can also be self-hosted if you want maximum control. However, using a custom domain can have privacy-related drawbacks: If you are the only person using your custom domain, your actions can be easily tracked across websites simply by looking at the domain name in the email address and ignoring everything before the `@` symbol.

Using an aliasing service requires trusting both your email provider and your aliasing provider with your unencrypted messages. Some providers mitigate this slightly with automatic PGP encryption[^1], which reduces the number of parties you need to trust from two to one by encrypting incoming emails before they are delivered to your final mailbox provider.

### Addy.io

<div class="admonition recommendation" markdown>

![Logo Addy.io](assets/img/email-aliasing/addy.svg){ align=right }

**Addy.io** lets you create 10 domain aliases on a shared domain for free, or unlimited ["standard" aliases](https://addy.io/faq/#what-is-a-standard-alias).

[:octicons-home-16: Strona główna](https://addy.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://addy.io/privacy){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://addy.io/faq){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/anonaddy){ .card-link title="Kod źródłowy" }
[:octicons-heart-16:](https://addy.io/donate){ .card-link title="Wesprzyj" }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:simple-googleplay: Google Play](https://addy.io/faq/#is-there-an-android-app)
- [:simple-appstore: App Store](https://addy.io/faq/#is-there-an-ios-app)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/addy_io)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/iadbdpnoknmbdeolbapdackdcogdmjpe)

</details>

</div>

Liczba współdzielonych aliasów (które kończą się współdzieloną domeną, taką jak `@addy.io`), które można utworzyć, zależy od subskrybowanego [planu](https://addy.io/#pricing). Możesz zapłacić za te plany za pomocą [kryptowalut](https://addy.io/help/subscribing-with-cryptocurrency) lub kupić vouchera z [ProxyStore](https://addy.io/help/voucher-codes), oficjalnego odsprzedawcy Addy.io.

You can create unlimited standard aliases which end in a domain like `@[username].addy.io` or a custom domain on paid plans. However, as previously mentioned, this can be detrimental to privacy because people can trivially tie your standard aliases together based on the domain name alone. They are useful where a shared domain might be blocked by a service.

Securitum [przeprowadziło audyt](https://addy.io/blog/addy-io-passes-independent-security-audit) Addy.io we wrześniu 2023 r. i nie zidentyfikowało żadnych istotnych luk w zabezpieczeniach (https://addy.io/addy-io-security-audit.pdf).

Godne uwagi bezpłatne funkcje:

- [x] 10 Współdzielonch aliasy
- [x] Nieograniczona liczba standardowych aliasów
- [ ] Brak odpowiedzi wychodzących
- [x] 1 Skrzynka odbiorcza
- [x] Automatyczne szyfrowanie PGP[^1]

Jeśli anulujesz subskrypcję, będziesz nadal korzystać z funkcji płatnego planu do końca cyklu rozliczeniowego. Po zakończeniu bieżącego cyklu rozliczeniowego większość płatnych funkcji (w tym wszelkie niestandardowe domeny) zostanie [dezaktywowana](https://addy.io/faq/#what-happens-if-i-have-a-subscription-but-then-cancel-it), płatne ustawienia konta zostaną przywrócone do wartości domyślnych, a funkcja catch-all zostanie włączona, jeśli była wcześniej wyłączona.

### SimpleLogin

<div class="admonition recommendation" markdown>

![Logo SimpleLogin](assets/img/email-aliasing/simplelogin.svg){ align=right }

**SimpleLogin** to darmowa usługa, która zapewnia aliasy e-mail w różnych współdzielonych nazwach domen, a opcjonalnie zapewnia płatne funkcje, takie jak nieograniczona liczba aliasów i niestandardowe domeny.

[:octicons-home-16: Strona główna](https://simplelogin.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://simplelogin.io/privacy){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://simplelogin.io/docs){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/simple-login){ .card-link title="Kod źródłowy" }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.simplelogin.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1494359858)
- [:simple-github: GitHub](https://github.com/simple-login/Simple-Login-Android/releases)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/simplelogin)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/dphilobhebphkdjbpfohgikllaljmgbn)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/diacfpipniklenphgljfkmhinphjlfff)
- [:simple-safari: Safari](https://apps.apple.com/app/id6475835429)

</details>

</div>

SimpleLogin został [nabyty przez Proton AG](https://proton.me/news/proton-and-simplelogin-join-forces) z dniem 8 kwietnia 2022 roku. Jeśli używasz Proton Mail jako głównej skrzynki pocztowej, SimpleLogin to świetny wybór. As both products are now owned by the same company you now only have to trust a single entity. We also expect that SimpleLogin will be more tightly integrated with Proton's offerings in the future. SimpleLogin nadal obsługuje przekazywanie do dowolnego wybranego przez Ciebie dostawcy poczty elektronicznej.

Możesz połączyć swoje konto SimpleLogin w ustawieniach z kontem Proton. Jeśli posiadasz plan Proton Pass Plus, Proton Unlimited lub jakikolwiek plan dla wielu użytkowników, otrzymasz także darmowy dostęp do SimpleLogin Premium. Możesz również zakupić kuponu na SimpleLogin Premium anonimowo za pośrednictwem ich oficjalnego odsprzedawcy [ProxyStore](https://simplelogin.io/faq).

Securitum [przeprowadziło audyt](https://simplelogin.io/blog/security-audit) SimpleLogin na początku 2022 r. i wszystkie kwestie [zostały rozwiązane](https://simplelogin.io/audit2022/web.pdf).

Godne uwagi bezpłatne funkcje:

- [x] 10 Współdzielonych aliasów
- [x] Nielimitowane odpowiedzi
- [x] 1 Skrzynka odbiorcza
- [ ] Automatyczne szyfrowanie PGP[^1] jest dostępne tylko w płatnych planach.

Po zakończeniu subskrypcji wszystkie utworzone aliasy nadal będą mogły odbierać i wysyłać wiadomości e-mail. Nie można jednak utworzyć żadnych nowych aliasów, które przekroczyłyby limit bezpłatnego planu, ani dodać nowej domeny, katalogu lub skrzynki pocztowej.

## Kryteria

**Pamiętaj, że nie jesteśmy powiązani z żadnym z polecanych przez nas usługodawców.** Oprócz [naszych standardowych kryteriów](about/criteria.md), oceniamy dostawców aliasingu poczty e-mail według tego samego standardu, co nasze [kryteria dostawcy poczty e-mail](email.md#criteria), jeśli ma to zastosowanie. Sugerujemy zapoznanie się z tą listą przed wyborem dostawcy poczty e-mail i przeprowadzenie własnych badań, aby upewnić się, że wybrany dostawca będzie dla Ciebie odpowiedni.

[^1]: Automatyczne szyfrowanie PGP umożliwia CI szyfrowanie niezaszyfrowanych przychodzących wiadomości e-mail przed ich przekazaniem do skrzynki pocztowej, dzięki czemu główny dostawca skrzynki pocztowej nigdy nie zobaczy niezaszyfrowanej treści wiadomości e-mail.
