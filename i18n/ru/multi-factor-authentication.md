---
title: "Многофакторная аутентификация"
icon: 'material/two-factor-authentication'
description: Эти инструменты помогут вам защитить ваши учетные записи в интернете с помощью многофакторной аутентификации без передачи ваших секретов третьим лицам.
cover: multi-factor-authentication.webp
---

<small>Защищает от следующих угроз:</small>

- [:material-target-account: Целевые атаки](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

<div class="admonition note" markdown>
<p class="admonition-title">Hardware Keys</p>

[Hardware security key recommendations](security-keys.md) have been moved to their own category.

</div>

**Приложения многофакторной аутентификации** реализуют стандарт безопасности, принятый рабочей группой инженеров интернета (IETF), который называется **Time-based One-time Passwords** или **TOTP**. При этом методе веб-сайты делятся с вами секретом, который вносится в приложение аутентификации. Затем приложение генерирует шестизначные коды, основанные на текущем времени, которые вы вводите при входе на сайт для проверки. Обычно эти коды обновляются каждые 30 секунд, и как только генерируется новый код, старый становится бесполезным. Даже если хакер получит один шестизначный код, у него не будет возможности анализировать этот код, чтобы получить исходный секрет, или каким-либо другим способом предсказать, какими могут быть будущие коды.

Мы настоятельно рекомендуем вам использовать мобильные приложения TOTP вместо настольных альтернатив, поскольку Android и iOS имеют лучшую безопасность и изоляцию приложений, чем большинство настольных операционных систем.

## Ente Auth

<div class="admonition recommendation" markdown>

![Ente Auth logo](assets/img/multi-factor-authentication/ente-auth.svg){ align=right }

**Ente Auth** is a free and open-source app which stores and generates TOTP tokens. It can be used with an online account to back up and sync your tokens across your devices (and access them via a web interface) in a secure, end-to-end encrypted fashion. It can also be used offline on a single device with no account necessary.

[:octicons-home-16: Главная](https://ente.io/auth){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ente.io/privacy){ .card-link title="Политика конфиденциальности" }
[:octicons-info-16:](https://help.ente.io/auth){ .card-link title=Документация}
[:octicons-code-16:](https://github.com/ente-io/ente/tree/main/auth#readme){ .card-link title="Исходный код" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.ente.auth)
- [:simple-appstore: App Store](https://apps.apple.com/app/id6444121398)
- [:simple-github: GitHub](https://github.com/ente-io/ente/releases?q=auth)
- [:octicons-globe-16: Web](https://auth.ente.io)

</details>

</div>

## Aegis Authenticator (Android)

<div class="admonition recommendation" markdown>

![Aegis logo](assets/img/multi-factor-authentication/aegis.png){ align=right }

**Aegis Authenticator** is a free and open-source app for Android to manage your 2-step verification tokens for your online services. Aegis Authenticator operates completely offline/locally, but includes the option to export your tokens for backup unlike many alternatives.

[:octicons-home-16: Homepage](https://getaegis.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://getaegis.app/aegis/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/beemdevelopment/Aegis/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/beemdevelopment/Aegis){ .card-link title="Source Code" }
[:octicons-heart-16:](https://buymeacoffee.com/beemdevelopment){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.beemdevelopment.aegis)
- [:simple-github: GitHub](https://github.com/beemdevelopment/Aegis/releases)

</details>

</div>

<!-- markdownlint-disable-next-line -->
## Критерии

**Обрати внимание, что у нас нет связей ни с одним проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Перед тем, как вы решите выбрать какой-либо проект, мы рекомендуем вам ознакомиться со списком критериев и провести собственное исследование, чтобы убедиться в правильности своего выбора.

- Исходный код должен быть общедоступным.
- Не должно требовать интернет соединения.
- Cloud syncing must be optional, and (if available) sync functionality must be E2EE.
