---
meta_title: "Gizliliğinizi ve Güvenliğinizi Korumanız için En İyi Parola Yöneticileri - Privacy Guides"
title: Parola yöneticileri
icon: material/form-textbox-password
description: Parola yöneticileri, parolaları ve diğer kimlik bilgilerini güvenli bir şekilde saklayabilir ve yönetebilirsiniz.
cover: passwords.webp
schema:
  - 
    "@context": http://schema.org
    "@type": Web Sayfası
    name: Parola Yöneticisi Önerileri
    url: "./"
  - 
    "@context": http://schema.org
    "@type": YazılımUygulama
    name: Bitwarden
    image: /assets/img/password-management/bitwarden.svg
    url: https://bitwarden.com
    sameAs: https://tr.wikipedia.org/wiki/Bitwarden
    applicationCategory: Parola Yöneticisi
    operatingSystem:
      - Windows
      - macOS
      - Linux
      - Android
      - iOS
    subjectOf:
      "@context": http://schema.org
      "@type": Web Sayfası
      url: "./"
  - 
    "@context": http://schema.org
    "@type": YazılımUygulama
    name: 1Password
    image: /assets/img/password-management/1password.svg
    url: https://1password.com
    sameAs: https://en.wikipedia.org/wiki/1Password
    applicationCategory: Parola Yöneticisi
    operatingSystem:
      - Windows
      - macOS
      - Linux
      - Android
      - iOS
    subjectOf:
      "@context": http://schema.org
      "@type": Web Sayfası
      url: "./"
  - 
    "@context": http://schema.org
    "@type": YazılımUygulama
    name: Proton Pass
    image: /assets/img/password-management/protonpass.svg
    url: https://proton.me/pass
    applicationCategory: Parola Yöneticisi
    operatingSystem:
      - Android
      - iOS
    subjectOf:
      "@context": http://schema.org
      "@type": Web Sayfası
      url: "./"
  - 
    "@context": http://schema.org
    "@type": YazılımUygulama
    name: Psono
    image: /assets/img/password-management/psono.svg
    url: https://psono.com
    applicationCategory: Parola Yöneticisi
    operatingSystem:
      - Android
      - iOS
    subjectOf:
      "@context": http://schema.org
      "@type": Web Sayfası
      url: "./"
  - 
    "@context": http://schema.org
    "@type": YazılımUygulama
    name: KeePassXC
    image: /assets/img/password-management/keepassxc.svg
    url: https://keepassxc.org
    sameAs: https://tr.wikipedia.org/wiki/KeePassXC
    applicationCategory: Parola Yöneticisi
    operatingSystem:
      - Windows
      - macOS
      - Linux
    subjectOf:
      "@context": http://schema.org
      "@type": Web Sayfası
      url: "./"
  - 
    "@context": http://schema.org
    "@type": YazılımUygulama
    name: KeePassDX
    image: /assets/img/password-management/keepassdx.svg
    url: https://keepassdx.com
    applicationCategory: Parola Yöneticisi
    operatingSystem: Android
    subjectOf:
      "@context": http://schema.org
      "@type": Web Sayfası
      url: "./"
  - 
    "@context": http://schema.org
    "@type": YazılımUygulama
    name: Gopass
    image: /assets/img/password-management/gopass.svg
    url: https://gopass.pw
    applicationCategory: Parola Yöneticisi
    operatingSystem:
      - Windows
      - macOS
      - Linux
      - FreeBSD
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
---

<small>Aşağıdaki tehdit(ler)e karşı koruma sağlar:</small>

- [:material-target-account: Hedefli Saldırılar](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}
- [:material-bug-outline: Pasif Saldırılar](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: Service Providers](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

**Password managers** allow you to securely store and manage passwords and other credentials with the use of a master password.

[Introduction to Passwords :material-arrow-right-drop-circle:](basics/passwords-overview.md)

<div class="admonition info" markdown>
<p class="admonition-title">Info</p>

Tarayıcılar ve işletim sistemleri gibi yazılımlardaki yerleşik parola yöneticileri bazen özel parola yöneticisi yazılımları kadar iyi olmayabilir. The advantage of a built-in password manager is good integration with the software, but it can often be very simple and lack privacy and security features that standalone offerings have.

For example, the password manager in Microsoft Edge doesn't offer end-to-end encryption at all. Google's password manager has [optional](https://support.google.com/accounts/answer/11350823) E2EE, and [Apple's](https://support.apple.com/HT202303) offers E2EE by default.

</div>

## Bulut tabanlı

Bu parola yöneticileri, tüm cihazlarınızdan kolay erişim ve cihaz kaybına karşı güvenlik için parolalarınızı bir bulut sunucusuyla senkronize eder.

### Bitwarden

<div class="admonition recommendation" markdown>

![Bitwarden logo](assets/img/password-management/bitwarden.svg){ align=right }

**Bitwarden** is a free and open-source password and passkey manager. It aims to solve password management problems for individuals, teams, and business organizations. Bitwarden is among the best and safest solutions to store all of your logins and passwords while conveniently keeping them synced between all of your devices.

[:octicons-home-16: Homepage](https://bitwarden.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://bitwarden.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://bitwarden.com/help){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/bitwarden){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.x8bit.bitwarden)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1137397744)
- [:simple-github: GitHub](https://github.com/bitwarden/android/releases)
- [:fontawesome-brands-windows: Windows](https://bitwarden.com/download)
- [:simple-apple: macOS](https://bitwarden.com/download)
- [:simple-linux: Linux](https://bitwarden.com/download)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/com.bitwarden.desktop)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/bitwarden-password-manager)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/nngceckbapebfimnlniiiahkandclblb)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/jbkfoedolllekgbhcbcoahefnbanhhlh)
- [:simple-safari: Safari](https://apps.apple.com/app/id1352778147)

</details>

</div>

Bitwarden uses [PBKDF2](https://bitwarden.com/help/kdf-algorithms/#pbkdf2) as its key derivation function (KDF) algorithm by default. It also offers [Argon2](https://bitwarden.com/help/kdf-algorithms/#argon2id), which is more secure, as an alternative. You can change your account's KDF algorithm in the web vault:

- [x] Select **Settings → Security → Keys → KDF algorithm → Argon2id**

Bitwarden's server-side code is [open source](https://github.com/bitwarden/server), so if you don't want to use the Bitwarden cloud, you can easily host your own Bitwarden sync server.

### Proton Pass

<div class="admonition recommendation" markdown>

![Proton Pass logo](assets/img/password-management/protonpass.svg){ align=right }

**Proton Pass** is an open-source, end-to-end encrypted password manager developed by Proton, the team behind [Proton Mail](email.md#proton-mail). It securely stores your login credentials, generates unique email aliases, and supports and stores passkeys.

[:octicons-home-16: Homepage](https://proton.me/pass){ .md-button .md-button--primary }
[:octicons-eye-16:](https://proton.me/pass/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://proton.me/support/pass){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/protonpass){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=proton.android.pass)
- [:simple-appstore: App Store](https://apps.apple.com/app/id6443490629)
- [:fontawesome-brands-windows: Windows](https://proton.me/pass/download)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/proton-pass)
- [:simple-googlechrome: Chrome](https://chromewebstore.google.com/detail/ghmbeldphafepmbegfdlkpapadhbakde)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/gcllgfdnfnllodcaambdaknbipemelie)
- [:octicons-browser-16: Web](https://pass.proton.me)

</details>

</div>

With the acquisition of SimpleLogin in April 2022, Proton has offered a "hide-my-email" feature that lets you create 10 aliases (free plan) or unlimited aliases (paid plans).

The Proton Pass mobile apps and browser extension underwent an audit performed by Cure53 throughout May and June 2023. The security analysis company concluded:

> Proton Pass apps and components leave a rather positive impression in terms of security.

All issues were addressed and fixed shortly after the [report](https://res.cloudinary.com/dbulfrlrz/images/v1707561557/wp-pme/Cure53-proton-pass-20230717/Cure53-proton-pass-20230717.pdf).

### 1Password

<div class="admonition recommendation" markdown>

![1Password logo](assets/img/password-management/1password.svg){ align=right }

**1Password**, parolaları, geçiş anahtarlarını, kredi kartlarını, yazılım lisanslarını ve diğer hassas bilgileri güvenli bir dijital kasada saklamanıza olanak tanıyan, güvenlik ve kullanım kolaylığına odaklanan bir parola yöneticisidir. Kasanız bir [aylık ücret] karşılığında 1Password'ün sunucularında barındırılır (https://1password.com/sign-up).

1Password düzenli olarak [denetlenir](https://support.1password.com/security-assessments) ve olağanüstü müşteri desteği sağlar. 1Password kapalı kaynak kodludur; ancak ürünün güvenliği [security white paper] (https://1passwordstatic.com/files/security/1password-white-paper.pdf) adresinde ayrıntılı olarak belgelenmiştir.

[:octicons-home-16: Homepage](https://tresorit.com/){ class="md-button md-button--primary" }
[:octicons-eye-16:](https://tresorit.com/legal/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.tresorit.com/hc/en-us){ .card-link title=Documentation}

" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.onepassword.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1511601750)
- [:fontawesome-brands-windows: Windows](https://1password.com/downloads/windows)
- [:simple-apple: macOS](https://1password.com/downloads/mac)
- [:simple-linux: Linux](https://1password.com/downloads/linux)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/1password-x-password-manager)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/aeblfdkhhhdcdjpifhhbdiojplfjncoa)
- [:fontawesome-brands-edge: Edge](https://microsoftedge.microsoft.com/addons/detail/dppgmdbiimibapkepcbdbmkaabgiofem)
- [:simple-safari: Safari](https://apps.apple.com/app/id1569813296)
- [:octicons-browser-16: Web](https://my.1password.com/signin)

</details>

</div>

Geleneksel olarak 1Password, macOS ve iOS kullanan kişiler için en iyi parola yöneticisi kullanıcı deneyimini sunmuştur; ancak artık tüm platformlarda özellik eşitliğine ulaşmıştır. 1Password's clients boast many features geared towards families and less technical people, such as an intuitive UI for ease-of-use and navigation, as well as advanced functionality. Özellikle, 1Password'ün neredeyse her özelliği yerel mobil veya masaüstü istemcilerinde mevcuttur.

1Password kasanız hem ana parolanızla hem de sunucularında verilerinizi şifrelemek için rastgele 34 karakterli bir güvenlik anahtarıyla korunur. Bu güvenlik anahtarı verilerinize bir koruma katmanı ekler çünkü verileriniz ana parolanızdan bağımsız olarak yüksek entropi ile güvence altına alınır. Diğer birçok parola yöneticisi çözümü, verilerinizin güvenliğini sağlamak için tamamen ana parolanızın gücüne dayanır.

### Psono

<div class="admonition recommendation" markdown>

![Psono logosu](assets/img/password-management/psono.svg){ align=right }

**Psono**, ekipler için parola yönetimine odaklanan, Almanya'dan ücretsiz ve açık kaynaklı bir parola yöneticisidir. Psono, şifrelerin, dosyaların, yer imlerinin ve e-postaların güvenli paylaşımını destekler. Tüm sırlar bir ana şifre ile korunmaktadır.

[:octicons-home-16: Ana Sayfa](https://psono.com){ .md-button .md-button--primary }[:octicons-eye-16:](https://psono.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://doc.psono.com){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.com/psono){ .card-link title="Source Code" }
[](){ .card-link title=Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.psono.psono)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1545581224)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/psono-pw-password-manager)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/eljmjmgjkbmpmfljlmklcfineebidmlo)
- [:simple-docker: Docker Hub](https://hub.docker.com/r/psono/psono-client)

</details>

</div>

Psono, ürünleri için kapsamlı dokümantasyon sağlar. Psono için web istemcisi kendi kendine barındırılabilir; alternatif olarak, tam Topluluk Sürümünü veya ek özelliklere sahip Kurumsal Sürümü seçebilirsiniz.

Nisan 2024'te Psono, yalnızca tarayıcı uzantısı [için geçiş anahtarları desteği](https://psono.com/blog/psono-introduces-passkeys) ekledi.

### Kriter

**Lütfen önerdiğimiz projelerin hiçbirine bağlı olmadığımızı unutmayın.** [standart kriterlerimize](about/criteria.md)ek olarak, objektif tavsiyelerde bulunabilmemiz için bir takım gereklilikler geliştirdik. Bir projeyi kullanmayı seçmeden önce bu listeye aşina olmanızı ve sizin için doğru seçim olduğundan emin olmak için kendi araştırmanızı yapmanızı öneririz.

#### Minimum Gereksinimler

- Güçlü, standartlara dayalı/modern E2EE kullanmalıdır.
- Kapsamlı bir şekilde belgelenmiş şifreleme ve güvenlik uygulamalarına sahip olmalıdır.
- Saygın, bağımsız bir üçüncü tarafça yayınlanmış bir denetime sahip olmalıdır.
- Gerekli olmayan tüm telemetri isteğe bağlı olmalıdır.
- Faturalama amaçları için gerekenden daha fazla PII toplamamalıdır.

#### En İyi Durum

En iyi durum kriterlerimiz, bu kategorideki mükemmel bir projede görmek istediklerimizi temsil etmektedir. Önerilerimiz bu işlevlerden herhangi birini veya tamamını içermeyebilir, ancak içerenler bu sayfada diğerlerinden daha üst sıralarda yer alabilir.

- Telemetri isteğe bağlı (varsayılan olarak devre dışı) olmalı veya hiç toplanmamalıdır.
- Açık kaynak kodlu ve makul ölçüde kendi kendine barındırılabilir olmalıdır.

## Yerel depolama

Bu seçenekler şifrelenmiş bir parola veritabanını yerel olarak yönetmenizi sağlar.

### KeePassXC

<div class="admonition recommendation" markdown>

![KeePassXC logosu](assets/img/password-management/keepassxc.svg){ align=right }

**KeePassXC**, KeePass Password Safe'in yerel bir çapraz platform portu olan KeePassX'in, zengin özelliklere sahip, platformlar arası ve modern bir açık kaynaklı şifre yöneticisi sağlamak için yeni özellikler ve hata düzeltmeleriyle genişletilmesi ve iyileştirilmesi amacıyla bir topluluk çatallamasıdır.

[:octicons-home-16: Ana Sayfa](https://keepassxc.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://keepassxc.org/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://keepassxc.org/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/keepassxreboot/keepassxc){ .card-link title="Source Code" }
[:octicons-heart-16:](https://keepassxc.org/donate){ .card-link title=Contribute }???

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://keepassxc.org/download/#windows)
- [:simple-apple: macOS](https://keepassxc.org/download/#mac)
- [:simple-linux: Linux](https://keepassxc.org/download/#linux)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.keepassxc.KeePassXC)
- [:simple-firefoxbrowser: Firefox](https://addons.mozilla.org/firefox/addon/keepassxc-browser)
- [:simple-googlechrome: Chrome](https://chrome.google.com/webstore/detail/oboonakemofpalcgghocfoadofidjkkk)

</details>

</div>

KeePassXC dışa aktarma verilerini [CSV](https://en.wikipedia.org/wiki/Comma-separated_values) dosyaları olarak saklar. Bu dosyayı başka bir parola yöneticisine aktarırsanız veri kaybıyla karşılaşabilirsiniz. Her kaydı manuel olarak kontrol etmenizi tavsiye ederiz.

### KeePassDX (Android)

<div class="admonition recommendation" markdown>

![KeePassDX logosu](assets/img/password-management/keepassdx.svg){ align=right }

**KeePassDX** Android için hafif bir şifre yöneticisidir; şifrelenmiş verilerin KeePass formatında tek bir dosyada düzenlenmesine izin verir ve formları güvenli bir şekilde doldurabilir.

[:octicons-home-16: Homepage](https://keepassdx.com){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/Kunzisoft/KeePassDX/wiki){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/Kunzisoft/KeePassDX){ .card-link title="Source Code" }
[:octicons-heart-16:](https://keepassdx.com/#donation){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>İndirmeler</summary>
- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.kunzisoft.keepass.free)
- [:simple-github: Accrescent](https://github.com/Kunzisoft/KeePassDX/releases)
- [ GitHub)

</details>

</div>

The [pro version](https://play.google.com/store/apps/details?id=com.kunzisoft.keepass.pro) of the app allows you to unlock cosmetic content and non-standard protocol features, but more importantly, it helps and encourages development.

### Gopass (CLI)

<div class="admonition recommendation" markdown>

![Gopass logo](assets/img/password-management/gopass.svg){ align=right }

**Gopass** is a minimal password manager for the command line written in Go. Komut dosyası uygulamaları içinde kullanılabilir ve tüm büyük masaüstü ve sunucu işletim sistemlerinde çalışır.

[:octicons-home-16: Homepage](https://gopass.pw){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/gopasspw/gopass/tree/master/docs){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/gopasspw/gopass){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/sponsors/dominikschulz){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://gopass.pw/#install-windows)
- [:simple-apple: macOS](https://gopass.pw/#install-macos)
- [:simple-linux: Linux](https://gopass.pw/#install-linux)
- [:simple-freebsd: FreeBSD](https://gopass.pw/#install-bsd)

</details>

</div>

### Kriter

**Lütfen önerdiğimiz projelerin hiçbirine bağlı olmadığımızı unutmayın.** [standart kriterlerimize](about/criteria.md) ek olarak, objektif tavsiyelerde bulunabilmemiz için bir takım gereklilikler geliştirdik. Bir projeyi kullanmayı seçmeden önce bu listeye aşina olmanızı ve sizin için doğru seçim olduğundan emin olmak için kendi araştırmanızı yapmanızı öneririz.

- Must be cross-platform.
