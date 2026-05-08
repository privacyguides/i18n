---
title: Uwierzytelnianie wieloskładnikowe
icon: material/two-factor-authentication
description: These tools assist you with securing your internet accounts with multifactor authentication without sending your secrets to a third party.
cover: multi-factor-authentication.webp
---

<small>Chroni przed następującymi zagrożeniami:</small>

- [:material-target-account: Ataki ukierunkowane](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

<div class="admonition note" markdown>
<p class="admonition-title">Klucz sprzętowy</p>

[Zalecenia dotyczące kluczy sprzętowych](security-keys.md) zostały przeniesione do osobnej kategorii.

</div>

**Aplikacje do uwierzytelniania wieloskładnikowego** wdrażają standard bezpieczeństwa przyjęty przez Internet Engineering Task Force (IETF) o nazwie **Time-based One-time Passwords** lub **TOTP**. This is a method where websites share a secret with you which is used by your authenticator app to generate a six (usually) digit code based on the current time, which you enter while logging in for the website to check. Typically, these codes are regenerated every 30 seconds, and once a new code is generated the old one becomes useless. Even if a hacker gets one six-digit code, there is no way for them to reverse that code to get the original secret or otherwise be able to predict what any future codes might be.

We highly recommend that you use mobile TOTP apps instead of desktop alternatives as Android and iOS have better security and app isolation than most desktop operating systems.

## Ente Auth

<div class="admonition recommendation" markdown>

![Logo Ente Auth](assets/img/multi-factor-authentication/ente-auth.svg){ align=right }

**Ente Auth** to darmowa aplikacja open source która przechowuje i generuje tokeny TOTP. It can be used with an online account to back up and sync your tokens across your devices (and access them via a web interface) in a secure, end-to-end encrypted fashion. It can also be used offline on a single device with no account necessary.

[:octicons-home-16: Strona główna](https://ente.com/auth){ .md-button .md-button--primary }[:octicons-eye-16:](https://ente.com/privacy){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://ente.com/help/auth){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/ente-io/ente/tree/main/auth#readme){ .card-link title="Kod źródłowy" }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.ente.auth)
- [:simple-appstore: App Store](https://apps.apple.com/app/id6444121398)
- [:simple-github: GitHub](https://github.com/ente-io/ente/releases?q=auth)
- [:octicons-browser-16: W przeglądrace](https://auth.ente.io)

</details>

</div>

Kod źródłowy serwera oraz infrastruktura, na której opiera się Ente Auth (jeśli jest używany z kontem online) zostały poddane audytowi przez [[Cure53]](https://ente.com/blog/cern-audit) w październiku 2025 roku.

## Aegis Authenticator (Android)

<div class="admonition recommendation" markdown>

![Logo Aegis](assets/img/multi-factor-authentication/aegis.png){ align=right }

**Aegis Authenticator** to darmowa aplikacja open source dla Androida do zarządzania tokenami weryfikacji dwuetapowej Twoich usług online. Aegis Authenticator działa całkowicie offline/lokalnie, ale zawiera opcję eksportu tokenów do tworzenia kopii zapasowej w przeciwieństwie do wielu alternatyw.

[:octicons-home-16: Strona główna](https://getaegis.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://getaegis.app/aegis/privacy.html){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://github.com/beemdevelopment/Aegis/wiki){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/beemdevelopment/Aegis){ .card-link title="Kod źródłowy" }
[:octicons-heart-16:](https://buymeacoffee.com/beemdevelopment){ .card-link title="Wesprzyj" }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.beemdevelopment.aegis)
- [:simple-github: GitHub](https://github.com/beemdevelopment/Aegis/releases)

</details>

</div>

## Kryteria

**Należy pamiętać, że nie jesteśmy powiązani z żadnym z polecanych przez nas projektów.** Oprócz [naszych standardowych kryteriów](about/criteria.md) opracowaliśmy jasny zestaw wymagań, które pozwalają nam formułować obiektywne zalecenia. Sugerujemy zapoznanie się z tą listą przed wyborem projektu oraz przeprowadzenie własnych badań, aby upewnić się, że jest to odpowiedni wybór dla Ciebie.

- Kod źródłowy musi być publicznie dostępny.
- Nie może wymagać połączenia z Internetem.
- Synchronizacja w chmurze musi być opcjonalna; funkcja synchronizacji, jeśli jest dostępna, musi być E2EE.
