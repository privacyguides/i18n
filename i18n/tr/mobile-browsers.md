---
meta_title: "PC ve Mac için Mahremiyete Saygı Gösteren Web Tarayıcıları - Privacy Guides"
title: Mobil Tarayıcılar
icon: material/cellphone-information
description: Bu tarayıcılar telefonunuzda yaptığınız standart internet taraması için önerdiğimiz tarayıcılardır.
cover: mobile-browsers.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Gizli Monil Tarayıcı Önerileri
    url: "./"
    relatedLink: "../desktop-browsers/"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Brave
    image: /assets/img/browsers/brave.svg
    url: https://brave.com
    applicationCategory: Web Browser
    operatingSystem:
      - Android
      - iOS
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Cromite
    image: /assets/img/browsers/cromite.svg
    url: https://cromite.org
    applicationCategory: Web Browser
    operatingSystem:
      - Android
    subjectOf:
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": MobilUygulama
    name: Safari
    image: /assets/img/browsers/safari.svg
    url: https://apple.com/safari
    applicationCategory: Web Tarayıcısı
    operatingSystem:
      - iOS
    subjectOf:
      "@type": Web Sayfası
      url: "./"
---

<small>Aşağıdaki tehdit(ler)e karşı koruma sağlar:</small>

- [:material-account-cash: Gözetim Kapitalizmi](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Bunlar, standart/anonim olmayan internet taraması için şu anda önerilen mobil internet tarayıcıları ve yapılandırmalarıdır. İnternette anonim olarak gezinmeniz gerekiyorsa, bunun yerine [Tor](tor.md) kullanmalısınız.

## Brave

<div class="admonition recommendation" markdown>

![Brave logo](assets/img/browsers/brave.svg){ align=right }

**Brave Browser** yerleşik bir içerik engelleyici ve [gizlilik özellikleri] (https://brave.com/privacy-features) içerir ve bunların çoğu varsayılan olarak etkindir.

Brave, Chromium web tarayıcısı projesi üzerine inşa edilmiştir, bu nedenle kullanımı daha tanıdıktır ve olabildiğince az web sitesi uyumluluğu yaşarsınız.

[:octicons-home-16: Ana Sayfa](https://brave.com){ .md-button .md-button--primary }
[:simple-torbrowser:](https://brave4u7jddbv7cyviptqjc7jusxh72uik7zt6adtckl5f4nwy2v72qd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://brave.com/privacy/browser){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.brave.com){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/brave/brave-browser){ .card-link title="Source Code" }???

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.brave.browser)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1052879175)
- [:simple-github: GitHub](https://github.com/brave/brave-browser/releases)
- [:simple-fdroid: F-Droid](https://brave-browser-apk-release.s3.brave.com/fdroid/repo/index.html)

</details>

</div>

### Önerilen Yapılandırma

Tor Browser, internette gerçekten anonim olarak gezinmenin tek yoludur. Brave kullandığınızda, gizliliğinizi belirli taraflardan korumak için aşağıdaki ayarları değiştirmenizi öneririz, ancak [Tor Browser](tor.md#tor-browser) dışındaki tüm tarayıcılar bir şekilde *birileri* tarafından izlenebilir olacaktır.

=== "Android"

    Bu seçenekler :material-menu: → **Ayarlar** → **Brave Shields & gizlilik** bölümünde bulunabilir.

=== "iOS"

    Bu seçenekler :fontawesome-solid-ellipsis: → **Ayarlar** → **Brave Shields & gizlilik** bölümünde bulunabilir.

#### Brave küresel varsayılanları korur

Brave, [Shields](https://support.brave.com/hc/articles/360022973471-What-is-Shields) özelliğinde bazı parmak izi önleme tedbirleri içeriyor. Bu seçenekleri ziyaret ettiğiniz tüm sayfalarda [global olarak](https://support.brave.com/hc/articles/360023646212-How-do-I-configure-global-and-site-specific-Shields-settings) yapılandırmanızı öneririz.

Shields'in seçenekleri gerektiğinde site bazında düşürülebilir, ancak varsayılan olarak aşağıdakileri ayarlamanızı öneririz:

=== "Android"

    <div class="annotate" markdown>

    - [x] *İzleyicileri engelle & reklamlar* altında **Agresif** 'i seçin
    - [x] **AMP sayfalarını otomatik yönlendir'**i seçin
    - [x] **AMP sayfalarını otomatik yönlendir'**i seçin
    - [x] *Bağlantıları HTTPS'ye yükselt* altında **Tüm** *bağlantıların HTTPS* **kullanmasını iste (katı)** seçeneğini belirleyin
    - \[x\] (İsteğe Bağlı) **Blok Komut Dosyalarını** Seçin (1)
    - [x] *Çerezleri* **Engelle** altında **Üçüncü taraf çerezlerini engelle** 'yi seçin
    - [x] **Blok Parmak İzini Seçi**n
    - [x] **Dil ayarları aracılığıyla parmak izini engelle** öğesini seçin

    <details class="warning" markdown>
    <summary>Varsayılan filtre listelerini kullanma</summary>

    Brave, **İçerik Filtreleme** menüsünden veya dahili `brave://adblock` sayfasından ek içerik filtreleri seçmenize olanak tanır. Bu özelliği kullanmamanızı tavsiye ederiz; bunun yerine varsayılan filtre listelerini saklayın. Ekstra listeler kullanmak sizi diğer Brave kullanıcılarından farklı kılar ve ayrıca Brave'de bir açık varsa ve kullandığınız listelerden birine kötü amaçlı bir kural eklenirse saldırı yüzeyini artırabilir.

    </details>

    - [x] **Bu siteyi kapattığımda beni unut'u** seçin

    </div>

    1. Bu seçenek, birçok siteyi bozacak olan JavaScript'i devre dışı bırakır. Bunları kırmak için, adres çubuğundaki Kalkan simgesine dokunarak ve *Gelişmiş kontroller* altında bu ayarın işaretini kaldırarak site bazında istisnalar ayarlayabilirsiniz.

=== "iOS"

    <div class="annotate" markdown>

    - [x] Select **Aggressive** under *Trackers & Ads Blocking*
    - [x] Select **Strict** under *Upgrade Connections to HTTPS*
    - [x] Select **Auto-Redirect AMP pages**
    - [x] Select **Auto-Redirect Tracking URLs**
    - \[x\] (İsteğe Bağlı) **Blok Komut Dosyalarını** Seçin (1)
    - [x] **Blok Parmak İzini Seçi**n
    - [x] Select **Site Tabs Closed** under *Auto Shred*

    <details class="warning" markdown>
    <summary>Varsayılan filtre listelerini kullanma</summary>

    Brave allows you to select additional content filters within the **Content Filtering** menu. Bu özelliği kullanmamanızı tavsiye ederiz; bunun yerine varsayılan filtre listelerini saklayın. Ekstra listeler kullanmak sizi diğer Brave kullanıcılarından farklı kılar ve ayrıca Brave'de bir açık varsa ve kullandığınız listelerden birine kötü amaçlı bir kural eklenirse saldırı yüzeyini artırabilir.

    </details>

    </div>

    1. This option disables JavaScript, which will break a lot of sites. Bunları kırmak için, adres çubuğundaki Kalkan simgesine dokunarak ve *Gelişmiş kontroller* altında bu ayarın işaretini kaldırarak site bazında istisnalar ayarlayabilirsiniz.

##### Clear browsing data (Android only)

- [x] Select **Clear data on exit**

##### Social Media Blocking (Android only)

- [ ] Tüm sosyal medya bileşenlerinin işaretini kaldırın

#### Other privacy settings

=== "Android"

    <div class="annotate" markdown>

    - [x] Select **Disable non-proxied UDP** under [*WebRTC IP handling policy*](https://support.brave.com/hc/articles/360017989132-How-do-I-change-my-Privacy-Settings#webrtc)
    - \[x\] (Optional) Select **No protection** under *Safe Browsing* (1)
    - [ ] Uncheck **Allow sites to check if you have payment methods saved**
    - [ ] Uncheck **Javascript optimization & security** under the setting with the same name
    - [x] Select **Close tabs on exit**
    - [ ] Uncheck **Allow privacy-preserving product analytics (P3A)**
    - [ ] Uncheck **Automatically send diagnostic reports**
    - [ ] Uncheck **Automatically send daily usage ping to Brave**

    </div>

    1. Brave's [implementation of Safe Browsing](https://support.brave.com/hc/en-us/articles/15222663599629-Safe-Browsing-in-Brave) on Android **does not** proxy [Safe Browsing network requests](https://developers.google.com/safe-browsing/v4/update-api#checking-urls) like its desktop counterpart. This means that your IP address may be seen (and logged) by Google. Note that Safe Browsing is not available for Android devices without Google Play Services.

=== "iOS"

    - [ ] Uncheck **Allow Privacy-Preserving Product Analytics (P3A)**
    - [ ] Uncheck **Automatically send daily usage ping to Brave**

#### Leo

These options can be found in :material-menu: → **Settings** → **Leo**.

<div class="annotate" markdown>

- [ ] Uncheck **Show autocomplete suggestions in address bar** (1)

</div>

1. This option is not present in Brave's iOS app.

#### Search engines

These options can be found in :material-menu:/:fontawesome-solid-ellipsis: → **Settings** → **Search engines**.

- [ ] Uncheck **Show search suggestions**

#### Brave Sync

[Brave Sync](https://support.brave.com/hc/articles/360059793111-Understanding-Brave-Sync), tarama verilerinizin (geçmiş, yer imleri vb.) bir hesap gerektirmeden tüm cihazlarınızda erişilebilir olmasını sağlar ve E2EE ile korur.

## Cromite (Android)

<div class="admonition recommendation" markdown>

![Cromite logo](assets/img/browsers/cromite.svg){ align=right }

**Cromite** is a Chromium-based browser with built-in ad blocking, fingerprinting protections, and other [privacy and security enhancements](https://github.com/uazo/cromite/blob/master/docs/FEATURES.md). It is a fork of the discontinued **Bromite** browser.

[:octicons-home-16: Homepage](https://cromite.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/uazo/cromite/blob/master/docs/PRIVACY_POLICY.md){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/uazo/cromite?tab=readme-ov-file#docs){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/uazo/cromite){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-android: F-Droid](https://cromite.org/fdroid/repo/?fingerprint=49F37E74DEE483DCA2B991334FB5A0200787430D0B5F9A783DD5F13695E9517B)
- [:simple-github: GitHub](https://github.com/uazo/cromite/releases/latest)

</details>

</div>

### Önerilen Yapılandırma

These options can be found in :material-menu: → :gear: **Settings** → **Privacy and security**.

#### Browsing data

- [x] Select **Close all open tabs on exit**

#### Incognito mode

- [x] Select **Open external links in incognito**

#### Security

- [x] Select **Always use secure connections**

This prevents you from unintentionally connecting to a website in plain-text HTTP. HTTP is extremely uncommon nowadays, so this should have little to no impact on your day-to-day browsing.

#### Adblock Plus settings

These options can be found in :material-menu: → :gear: **Settings** → **Adblock Plus settings**.

Cromite contains a customized version of Adblock Plus with EasyList enabled by default, as well as options to select more filter lists within the **Filter lists** menu.

Using extra lists will make you stand out from other Cromite users and may also increase attack surface if a malicious rule is added to one of the lists you use.

- \[x\] (İsteğe bağlı) **Çevreleme önleme ve snippet'leri etkinleştir'i** seçin

Bu ayar, Cromite'ın içerik engellemesinin etkinliğini artırabilecek ek bir Adblock Plus listesi ekler. Öne çıkma ve potansiyel olarak saldırı yüzeyini artırma konusundaki uyarılar geçerlidir.

#### Eski Adblock ayarları

Bu seçenekler :material-menu: → :gear: **Ayarlar** → **Eski Adblock ayarları** bölümünde bulunabilir.

- [ ] Otomatik güncelleme ayarının işaretini kaldırın

Bu, bakımı yapılmamış Bromite adblock filtresi için güncelleme denetimlerini devre dışı bırakır.

## Safari (iOS)

On iOS, any app that can browse the web is [restricted](https://developer.apple.com/app-store/review/guidelines) to using an Apple-provided [WebKit framework](https://developer.apple.com/documentation/webkit), so a browser like [Brave](#brave) does not use the Blink engine (the core component of Chromium) like its counterparts on other operating systems.

<div class="admonition recommendation" markdown>

![Safari logosu](assets/img/browsers/safari.svg){ align=right }

iOS'ta varsayılan tarayıcı **Safari**'dir. Akıllı İzleme Önleme](https://webkit.org/blog/7675/intelligent-tracking-prevention), yalıtılmış ve geçici Özel Tarama sekmeleri, parmak izi koruması (web sitelerine sistem yapılandırmasının basitleştirilmiş bir sürümünü sunarak daha fazla cihazın aynı görünmesini sağlar) ve parmak izi randomizasyonu gibi [gizlilik özellikleri](https://support.apple.com/guide/iphone/browse-the-web-privately-iphb01fc3c85/ios) ve ücretli iCloud+ aboneliği olanlar için Özel Aktarım içerir.

[:octicons-home-16: Ana Sayfa](https://apple.com/safari){ .md-button .md-button--primary }[:octicons-eye-16:](https://apple.com/legal/privacy/data/en/safari){ .card-link title="Privacy Policy" }[:octicons-info-16:](https://support.apple.com/guide/iphone/browse-the-web-iph1fbef4daa/ios){ .card-link title=Documentation}
[](){ .card-link title="Source Code" }
[](){ .card-link title=Contribute" }

</details>

</div>

### Önerilen Yapılandırma

Safari'de bir içerik engelleyici istiyorsanız [AdGuard](browser-extensions.md#adguard) 'ı yüklemenizi öneririz.

Gizlilik/güvenlikle ilgili aşağıdaki seçenekler :gear: **Ayarlar** → **Uygulamalar** → **Safari** bölümünde bulunabilir.

#### Safari'nin Erişimine İzin Ver

**Siri**'nin altında:

- [ ] **Bu Uygulamadan Öğrenmeyi** Devre Dışı Bırak
- [ ] **Uygulamada Göster'i** Devre Dışı Bırak
- [ ] **Ana Ekranda Göster'i** Devre Dışı Bırak
- [ ] **Uygulamada Göster'i** Devre Dışı Bırak

Bu, Siri'nin Siri önerileri için Safari'deki içeriği kullanmasını engeller.

#### Ara

- [ ] **Arama Motoru Önerilerini** Devre Dışı Bırak

Bu ayar, adres çubuğuna yazdığınız her şeyi Safari'de ayarlanan arama motoruna gönderir. Arama önerilerini devre dışı bırakmak, arama motoru sağlayıcınıza hangi verileri gönderdiğinizi daha hassas bir şekilde kontrol etmenizi sağlar.

#### Profiller

Safari, gezintinizi farklı profillerle ayırmanıza olanak tanır. Tüm çerezleriniz, geçmişiniz ve web sitesi verileriniz her profil için ayrıdır. Alışveriş, İş veya Okul gibi farklı amaçlar için farklı profiller kullanmalısınız.

#### Gizlilik & Güvenlik

- [x] **Siteler Arası İzlemeyi Eng**ellemeyi Etkinleştir

Bu, WebKit'in [Akıllı İzleme Korumasını](https://webkit.org/tracking-prevention/#intelligent-tracking-prevention-itp) etkinleştirir. Bu özellik, izleyicileri durdurmak için cihaz üzerinde makine öğrenimini kullanarak istenmeyen izlemeye karşı korunmaya yardımcı olur. ITP birçok yaygın tehdide karşı koruma sağlar, ancak web sitesinin kullanılabilirliğine müdahale etmemek için tasarlandığından tüm izleme yollarını engellemez.

- [x] **Özel Tarama Kilidini Açmak için Face ID/Touch ID Gerektir**' **i** Etkinleştir

Bu ayar, kullanılmadığında özel sekmelerinizi biyometrik/PIN arkasında kilitlemenizi sağlar.

- [ ] **Sahte Web Sitesi Uyarısını** Devre Dışı Bırak

Bu ayar, gezinirken sizi korumak için Google Safe Browsing (veya Çin anakarası veya Hong Kong'daki kullanıcılar için Tencent Safe Browsing) kullanır. Bu nedenle, IP adresiniz Güvenli Tarama sağlayıcınız tarafından kaydedilebilir. Bu ayarın devre dışı bırakılması bu günlüğü devre dışı bırakacaktır, ancak bilinen kimlik avı sitelerine karşı daha savunmasız olabilirsiniz.

- [x] **Güvenli Değil Bağlantı Uyarısını** Etkinleştir

Bu ayar, bir web sitesine bağlantınız HTTPS kullanmıyorsa bir uyarı ekranı gösterir. Safari siteyi otomatik olarak HTTPS'ye yükseltmeye çalışacağından, bunu yalnızca HTTPS bağlantısı olmadığında görmeniz gerekir.

- [ ] **Önemli Noktaları** Devre Dışı Bırak

Apple'ın Safari için gizlilik politikası şu şekildedir:

> Safari, bir web sayfasını ziyaret ederken ilgili önemli noktaların mevcut olup olmadığını belirlemek için web sayfası adresinden hesaplanan bilgileri OHTTP üzerinden Apple'a gönderebilir.

#### Web Siteleri için Ayarlar

**Kamera** Altında

- [x] **Sor'**u seçin

**Mikrofon** Altında

- [x] **Sor'**u seçin

Under **Location**

- [x] **Sor'**u seçin

These settings ensure that websites can only access your camera, microphone, or location after you explicitly grant them access.

#### Other Privacy Settings

These options can be found in :gear: **Settings** → **Apps** → **Safari** → **Advanced**.

##### Fingerprinting Mitigations

**Gelişmiş İzleme ve Parmak İzi Koruması** ayarı belirli değerleri rastgele hale getirerek parmak izinizi almanın daha zor olmasını sağlar:

- [x] **Tüm Tarama**  veya **Özel Tarama**'yı seçin

##### Privacy Preserving Ad Measurement

- [ ] **Gizliliği Koruyan Reklam Ölçümünü** Devre Dışı Bırak

Ad click measurement has traditionally used tracking technology that infringes on user privacy. [Private Click Measurement](https://webkit.org/blog/11529/introducing-private-click-measurement-pcm) is a WebKit feature and proposed web standard aimed towards allowing advertisers to measure the effectiveness of web campaigns without compromising on user privacy.

Bu özelliğin kendi başına çok az gizlilik endişesi vardır, bu nedenle açık bırakmayı seçebilseniz de, Özel Tarama'da otomatik olarak devre dışı bırakılmasının özelliği devre dışı bırakmak için bir gösterge olduğunu düşünüyoruz.

#### Always-on Private Browsing

Open Safari and tap the Tabs button, located in the bottom right. Then, expand the :material-format-list-bulleted: Tab Groups list.

- [x] **Özel**'i seçin

Safari's Private Browsing mode offers additional privacy protections. Private Browsing uses a new [ephemeral](https://developer.apple.com/documentation/foundation/urlsessionconfiguration/1410529-ephemeral) session for each tab, meaning tabs are isolated from one another. There are other smaller privacy benefits with Private Browsing too, such as not sending a webpage’s address to Apple when using Safari's translation feature.

Do note that Private Browsing does not save cookies and website data, so it won't be possible to remain signed in to sites. This may be an inconvenience.

#### iCloud Sync

Safari Geçmişi, Sekme Grupları, iCloud Sekmeleri ve kayıtlı parolaların senkronizasyonu E2EE'dir. However, by default, bookmarks are [not](https://support.apple.com/HT202303). Apple, [gizlilik politikasına](https://support.apple.com/HT212520) uygun olarak bunların şifresini çözebilir ve bunlara erişebilir.

**Gelişmiş Veri Koruması**'nı etkinleştirerek Safari yer işaretleriniz ve indirmeleriniz için E2EE'yi etkinleştirebilirsiniz. Go to :gear: **Settings** → **iCloud** → **Advanced Data Protection**.

- [x] Turn on **Advanced Data Protection**

If you use iCloud with Advanced Data Protection disabled, we also recommend setting Safari's default download location to a local folder on your device. This option can be found in :gear: **Settings** → **Apps** → **Safari** → **General** → **Downloads**.

## Kriter

**Lütfen önerdiğimiz projelerin hiçbirine bağlı olmadığımızı unutmayın.** [standart kriterlerimize](about/criteria.md) ek olarak, objektif tavsiyelerde bulunabilmemiz için bir takım gereklilikler geliştirdik. Bir projeyi kullanmayı seçmeden önce bu listeye aşina olmanızı ve sizin için doğru seçim olduğundan emin olmak için kendi araştırmanızı yapmanızı öneririz.

### Minimum Gereksinimler

- Must support automatic updates.
- Must receive engine updates from upstream releases quickly.
- İçerik engellemeyi desteklemelidir.
- Tarayıcıyı gizliliğe daha saygılı hale getirmek için gereken herhangi bir değişiklik kullanıcı deneyimini olumsuz etkilememelidir.
