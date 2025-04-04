---
title: "Köp faktorly tanamak"
icon: 'material/two-factor-authentication'
description: Bu araçlar, sırlarınızı üçüncü bir tarafa göndermeden internet hesaplarınızı Çok Faktörlü Kimlik Doğrulama ile güvence altına almanıza yardımcı olur.
cover: Çok Faktörlü Kimlik Doğrulama
---

<small>Aşağıdaki tehdit(ler)e karşı koruma sağlar:</small>

- [:material-target-account: Hedefli Saldırılar](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

<div class="admonition note" markdown>
<p class="admonition-title">Donanım Tuşları</p>

[Donanım güvenlik anahtarı önerileri](security-keys.md) kendi kategorisine taşınmıştır.

</div>

**Çok Faktörlü Kimlik Doğrulama Uygulamaları**, İnternet Mühendisliği Görev Gücü (IETF) tarafından kabul edilen ve **Zaman Tabanlı Tek Kullanımlık Parolalar** veya **TOTP** olarak adlandırılan bir güvenlik standardını uygular. Bu, web sitelerinin sizinle bir sır paylaştığı ve kimlik doğrulayıcı uygulamanız tarafından web sitesinin kontrol etmesi için oturum açarken girdiğiniz geçerli saate dayalı altı (genellikle) basamaklı bir kod oluşturmak için kullanılan bir yöntemdir. Typically, these codes are regenerated every 30 seconds, and once a new code is generated the old one becomes useless. Even if a hacker gets one six-digit code, there is no way for them to reverse that code to get the original secret or otherwise be able to predict what any future codes might be.

We highly recommend that you use mobile TOTP apps instead of desktop alternatives as Android and iOS have better security and app isolation than most desktop operating systems.

## Ente Auth

<div class="admonition recommendation" markdown>

![Ente Auth logo](assets/img/multi-factor-authentication/ente-auth.svg){ align=right }

**Ente Auth** is a free and open-source app which stores and generates TOTP tokens. It can be used with an online account to back up and sync your tokens across your devices (and access them via a web interface) in a secure, end-to-end encrypted fashion. It can also be used offline on a single device with no account necessary.

[:octicons-home-16: Homepage](https://ente.io/auth){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ente.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://help.ente.io/auth){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ente-io/ente/tree/main/auth#readme){ .card-link title="Source Code" }

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
## Kriter

**Lütfen önerdiğimiz projelerin hiçbirine bağlı olmadığımızı unutmayın.** [standart kriterlerimize](about/criteria.md) ek olarak, objektif tavsiyelerde bulunabilmemiz için bir takım gereklilikler geliştirdik. Bir projeyi kullanmayı seçmeden önce bu listeye aşina olmanızı ve sizin için doğru seçim olduğundan emin olmak için kendi araştırmanızı yapmanızı öneririz.

- Source code must be publicly available.
- Must not require internet connectivity.
- Cloud syncing must be optional, and (if available) sync functionality must be E2EE.
