---
title: "File Sharing and Sync"
icon: material/share-variant
description: Discover how to privately share your files between your devices, with your friends and family, or anonymously online.
cover: file-sharing.webp
---

<small>Aşağıdaki tehdit(ler)e karşı koruma sağlar:</small>

- [:material-server-network: Service Providers](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

Discover how to privately share your files between your devices, with your friends and family, or anonymously online.

## Dosya Paylaşımı

If you already use [Proton Drive](cloud.md#proton-drive)[^1] or have a [Bitwarden](passwords.md#bitwarden) Premium[^2] subscription, consider using the file sharing capabilities that they each offer, both of which use end-to-end encryption. Otherwise, the standalone options listed here ensure that the files you share are not read by a remote server.

### Send

<div class="admonition recommendation" markdown>

![Send logo](assets/img/file-sharing-sync/send.svg){ align=right }

**Send** is a fork of Mozilla's discontinued Firefox Send service which allows you to send files to others with a link. Dosyalar cihanızda şifrelenir, böylece sunucu tarafından okunamazlar ve isteğe bağlı olarak parola korumalı da olabilirler. The maintainer of Send hosts a [public instance](https://send.vis.ee). You can use other public instances, or you can host Send yourself.

[:octicons-home-16: Homepage](https://send.vis.ee){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/timvisee/send-instances){ .card-link title="Public Instances"}
[:octicons-info-16:](https://github.com/timvisee/send#readme){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/timvisee/send){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/sponsors/timvisee){ .card-link title=Contribute }

</details>

</div>

Send can be used via its web interface or via the [ffsend](https://github.com/timvisee/ffsend) CLI. If you are familiar with the command-line and send files frequently, we recommend using the CLI client to avoid JavaScript-based encryption. You can specify the `--host` flag to use a specific server:

```bash
ffsend upload --host https://send.vis.ee/ FILE
```

### OnionShare

<div class="admonition recommendation" markdown>

![OnionShare logo](assets/img/file-sharing-sync/onionshare.svg){ align=right }

**OnionShare** is an open-source tool that lets you securely and [:material-incognito: anonymously](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple } share a file of any size. Tor onion hizmeti olarak erişilebilir bir wen sunucusu başlatarak çalışır, böylece dosyaları indirmek veya göndermek için alıcıyla tahmin edilemez bir link paylaşabilirsiniz.

[:octicons-home-16: Homepage](https://onionshare.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://lldan5gahapx5k7iafb3s4ikijc4ni7gx5iywdflkba5y2ezyg6sjgyd.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://docs.onionshare.org){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/onionshare/onionshare){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://onionshare.org/#download)
- [:simple-apple: macOS](https://onionshare.org/#download)
- [:simple-linux: Linux](https://onionshare.org/#download)
- [:simple-flathub: Flathub](https://flathub.org/apps/org.onionshare.OnionShare)

</details>

</div>

OnionShare provides the option to connect via [Tor bridges](https://docs.onionshare.org/2.6.2/en/tor.html#automatic-censorship-circumvention) to circumvent [:material-close-outline: Censorship](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}.

### Kriterler

**Lütfen önerdiğimiz projelerin hiçbirine bağlı olmadığımızı unutmayın.** [standart kriterlerimize](about/criteria.md)ek olarak, objektif tavsiyelerde bulunabilmemiz için bir takım gereklilikler geliştirdik. Bir projeyi kullanmayı seçmeden önce bu listeye aşina olmanızı ve sizin için doğru seçim olduğundan emin olmak için kendi araştırmanızı yapmanızı öneririz.

- Şifresi çözülmüş verileri uzak bir sunucuda depolamamalıdır.
- Açık kaynaklı yazılım olmalıdır.
- Linux, macOS ve Windows için istemcilere sahip olmalı veya bir web arayüzüne sahip olmalıdır.

## FreedomBox

<div class="admonition recommendation" markdown>

![FreedomBox logosu](assets/img/file-sharing-sync/freedombox.svg){ align=right }

**FreedomBox**, [tek kartlı bilgisayar (SBC)](https://en.wikipedia.org/wiki/Single-board_computer) üzerinde çalıştırılmak için tasarlanmış bir işletim sistemidir. The purpose is to make it easy to set up server applications that you might want to self-host.

[:octicons-home-16: Ana Sayfa](https://freedombox.org){ .md-button .md-button--primary }[:octicons-info-16:](https://wiki.debian.org/FreedomBox/Manual){ .card-link title="Privacy Policy" }
[:octicons-code-16:](https://salsa.debian.org/freedombox-team/freedombox){ .card-link title=Documentation}
[:octicons-heart-16:](https://freedomboxfoundation.org/donate){ .card-link title="Source Code" }
[](){ .card-link title=Contribute" }

</details>

</div>

## Dosya Senkronizasyonu

### Nextcloud (İstemci-Sunucu)

<div class="admonition recommendation" markdown>

![Nextcloud logo](assets/img/document-collaboration/nextcloud.svg){ align=right }

**Nextcloud**, kontrol ettiğiniz özel bir sunucuda kendi dosya barındırma hizmetlerinizi oluşturmak için ücretsiz ve açık kaynaklı bir istemci-sunucu yazılımı paketidir.

[:octicons-home-16: Ana Sayfa](https://nextcloud.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://nextcloud.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://nextcloud.com/support){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/nextcloud){ .card-link title="Source Code" }
[:octicons-heart-16:](https://nextcloud.com/contribute){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>İndirmeler</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.nextcloud.client)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1125420102)
- [:simple-github: GitHub](https://github.com/nextcloud/android/releases)
- [:fontawesome-brands-windows: Windows](https://nextcloud.com/install/#install-clients)
- [:simple-apple: macOS](https://nextcloud.com/install/#install-clients)
- [:simple-linux: Linux](https://nextcloud.com/install/#install-clients)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Uyarı</p>

Veri kaybına yol açabileceğinden Nextcloud için [E2EE App](https://apps.nextcloud.com/apps/end_to_end_encryption) kullanılmasını önermiyoruz; son derece deneyseldir ve üretim kalitesinde değildir.

</div>

### Syncthing (P2P)

<div class="admonition recommendation" markdown>

![Syncthing logosu](assets/img/file-sharing-sync/syncthing.svg){ align=right }

**Syncthing** açık kaynaklı bir eşler arası sürekli dosya senkronizasyon yardımcı programıdır. Dosyaları yerel ağ veya internet üzerinden iki veya daha fazla cihaz arasında senkronize etmek için kullanılır. Syncthing merkezi bir sunucu kullanmaz; cihazlar arasında veri aktarımı için [Blok Değişim Protokolü](https://docs.syncthing.net/specs/bep-v1.html#bep-v1) kullanır. Tüm veriler TLS kullanılarak şifrelenir.

[:octicons-home-16: Ana Sayfa](https://syncthing.net){ .md-button .md-button--primary }[:octicons-info-16:](https://docs.syncthing.net){ .card-link title="Privacy Policy" }
[:octicons-code-16:](https://github.com/syncthing){ .card-link title=Documentation}
[:octicons-heart-16:](https://syncthing.net/donations){ .card-link title="Source Code" }
[](){ .card-link title=Contribute" }

<details class="downloads" markdown>
<summary>İndirmeler</summary>

- [:fontawesome-brands-windows: Windows](https://syncthing.net/downloads)
- [:simple-apple: macOS](https://syncthing.net/downloads)
- [:simple-linux: Linux](https://syncthing.net/downloads)
- [:simple-freebsd: Web](https://syncthing.net/downloads)

</details>

</div>

### Kriter

**Lütfen önerdiğimiz projelerin hiçbirine bağlı olmadığımızı unutmayın.** [standart kriterlerimize](about/criteria.md) ek olarak, objektif tavsiyelerde bulunabilmemiz için bir takım gereklilikler geliştirdik. Bir projeyi kullanmayı seçmeden önce bu listeye aşina olmanızı ve sizin için doğru seçim olduğundan emin olmak için kendi araştırmanızı yapmanızı öneririz.

#### Minimum Gereksinimler

- Üçüncü taraf bir uzak/bulut sunucusu gerektirmemelidir.
- Açık kaynaklı yazılım olmalıdır.
- Linux, macOS ve Windows için istemcilere sahip olmalı veya bir web arayüzüne sahip olmalıdır.

#### En İyi Durum

En iyi durum kriterlerimiz, bu kategorideki mükemmel bir projede görmek istediklerimizi temsil etmektedir. Önerilerimiz bu işlevlerden herhangi birini veya tamamını içermeyebilir, ancak içerenler bu sayfada diğerlerinden daha üst sıralarda yer alabilir.

- En azından belge önizlemelerini destekleyen iOS ve Android için mobil istemcilere sahip olmalıdır.
- Should support photo backups from iOS and Android, and optionally support file/folder sync on Android.

[^1]: Proton Drive allows you to [share files or folders](https://proton.me/support/drive-shareable-link) by generating a shareable public link or sending a unique link to a designated email address. Public links can be protected with a password, set to expire, and completely revoked, while links shared via email can have custom permissions and be similarly revoked. Per Proton Drive's [privacy policy](https://proton.me/drive/privacy-policy), file contents, file and folder names, and thumbnail previews are end-to-end encrypted.
[^2]: With a [premium](https://bitwarden.com/help/about-bitwarden-plans/#compare-personal-plans) subscription, [Bitwarden Send](https://bitwarden.com/products/send) allows you to share files and text securely with [end-to-end encryption](https://bitwarden.com/help/send-encryption). Gönder bağlantısı ile birlikte bir [şifre](https://bitwarden.com/help/send-privacy/#send-passwords) de gerekebilir. Bitwarden Send ayrıca [otomatik silme](https://bitwarden.com/help/send-lifespan) özelliğine de sahiptir.
