---
meta_title: "Tor Browser and Network: Anonymous Web Browsing - Privacy Guides"
title: "Tor Tarayıcı"
icon: simple/torbrowser
description: Protect your internet browsing from prying eyes by using the Tor network, a secure network which circumvents censorship.
cover: tor.webp
schema:
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Tor Tarayıcı
    image: /assets/img/browsers/tor.svg
    url: https://torproject.org
    sameAs: https://en.wikipedia.org/wiki/Tor_(network)
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
      - Android
    subjectOf:
      "@type": WebPage
      url: "./"
---

<small>Aşağıdaki tehdit(ler)e karşı koruma sağlar:</small>

- [:material-account-cash: Surveillance Capitalism](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}
- [:material-eye-outline: Mass Surveillance](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-close-outline: Sansür](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}

**Tor** is a group of volunteer-operated servers that allows you to connect for free and improve your privacy and security on the Internet. Individuals and organizations can also share information over the Tor network with ".onion hidden services" without compromising their privacy. Because Tor traffic is difficult to block and trace, Tor is an effective censorship circumvention tool.

[Detailed Tor Overview :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button.md-button--primary} [:material-movie-open-play-outline: Video: Why You Need Tor](https://www.privacyguides.org/videos/2025/03/02/why-you-need-tor/ ""){.md-button}

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Before connecting to Tor, please ensure you've read our [overview](advanced/tor-overview.md) on what Tor is and how to connect to it safely. We often recommend connecting to Tor through a trusted [VPN provider](vpn.md), but you have to do so **properly** to avoid decreasing your anonymity.

</div>

There are a variety of ways to connect to the Tor network from your device, the most commonly used being the **Tor Browser**, a fork of Firefox designed for [:material-incognito: anonymous](basics/common-threats.md#anonymity-vs-privacy ""){.pg-purple} browsing for desktop computers and Android.

Some of these apps are better than others, and again making a determination comes down to your threat model. If you are a casual Tor user who is not worried about your ISP collecting evidence against you, using apps like [Orbot](#orbot) or mobile browser apps to access the Tor network is probably fine. Increasing the number of people who use Tor on an everyday basis helps reduce the bad stigma of Tor, and lowers the quality of "lists of Tor users" that ISPs and governments may compile.

If more complete anonymity is paramount to your situation, you should **only** be using the desktop Tor Browser client, ideally in a [Whonix](desktop.md#whonix) + [Qubes](desktop.md#qubes-os) configuration. Mobile browsers are less common on Tor (and more fingerprintable as a result), and other configurations are not as rigorously tested against deanonymization.

## Tor Tarayıcı

<div class="admonition recommendation" markdown>

![Tor Browser logo](assets/img/browsers/tor.svg){ align=right }

**Tor Browser** is the choice if you need anonymity, as it provides you with access to the Tor network and bridges, and it includes default settings and extensions that are automatically configured by the default security levels: *Standard*, *Safer* and *Safest*.

[:octicons-home-16: Homepage](https://torproject.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=Documentation }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/tor-browser){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
- [:simple-android: Android](https://torproject.org/download/#android)
- [:fontawesome-brands-windows: Windows](https://torproject.org/download)
- [:simple-apple: macOS](https://torproject.org/download)
- [:simple-linux: Linux](https://torproject.org/download)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

You should **never** install any additional extensions on Tor Browser or edit `about:config` settings, including the ones we suggest for Firefox. Browser extensions and non-standard settings make you stand out from others on the Tor network, thus making your browser easier to [fingerprint](https://support.torproject.org/glossary/browser-fingerprinting).

</div>

The Tor Browser is designed to prevent fingerprinting, or identifying you based on your browser configuration. Therefore, it is imperative that you do **not** modify the browser beyond the default [security levels](https://tb-manual.torproject.org/security-settings).

In addition to installing Tor Browser on your computer directly, there are also operating systems designed specifically to connect to the Tor network such as [Whonix](desktop.md#whonix) on [Qubes OS](desktop.md#qubes-os), which provide even greater security and protections than the standard Tor Browser alone.

## Orbot

<div class="admonition recommendation" markdown>

![Orbot logosu](assets/img/self-contained-networks/orbot.svg){ align=right }

**Orbot**, cihazınızdaki herhangi bir uygulamadan gelen trafiği Tor ağı üzerinden yönlendiren akıllı telefonlar için ücretsiz bir Tor VPN'dir.

[:octicons-home-16: Ana Sayfa](https://orbot.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://orbot.app/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://orbot.app/faqs){ .card-link title=Documentation}
[:octicons-code-16:](https://orbot.app/code){ .card-link title="Source Code" }
[:octicons-heart-16:](https://orbot.app/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>İndirmeler</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.android)
- [:simple-appstore: Accrescent](https://apps.apple.com/app/id1609461599)
- [:simple-github: GitHub](https://github.com/guardianproject/orbot/releases)

</details>

</div>

Daha önce Orbot ayarlarında *Hedef Adresi İzole Et tercihinin* etkinleştirilmesini önermiştik. Bu ayar, bağlandığınız her IP adresi için farklı bir devre kullanılmasını zorunlu kılarak teorik olarak gizliliği artırabilir, ancak çoğu uygulama (özellikle web taraması) için pratik bir avantaj sağlamaz, önemli bir performans düşüşüne neden olabilir ve Tor ağı üzerindeki yükü artırır. İhtiyacınız olduğunu bilmediğiniz sürece bu ayarın varsayılan değerinden ayarlanmasını artık önermiyoruz.[^1]

<div class="admonition tip" markdown>
<p class="admonition-title">Android için İpuçları</p>

Orbot, SOCKS veya HTTP proxy'yi destekliyorsa tek tek uygulamaları proxy'leyebilir. Ayrıca [VpnService](https://developer.android.com/reference/android/net/VpnService) kullanarak tüm ağ bağlantılarınızı proxy yapabilir ve :gear: **Ayarlar** → **Ağ ve internet** → **VPN** → :gear: → **VPN olmadan bağlantıları engelle** içindeki VPN kill switch ile kullanılabilir.

Orbot, Guardian Project'in [F-Droid repository](https://guardianproject.info/fdroid) ve [Google Play](https://play.google.com/store/apps/details?id=org.torproject.android) sitelerinde genellikle güncel değildir, bu nedenle bunun yerine doğrudan [GitHub repository](https://github.com/guardianproject/orbot/releases) adresinden indirmeyi düşünün.

Tüm sürümler aynı imza kullanılarak imzalanmıştır, bu nedenle birbirleriyle uyumlu olmalıdırlar.

</div>

IOS'ta Orbot, çökmelere veya sızıntılara neden olabilecek bazı sınırlamalara sahiptir: iOS, Android'in yaptığı gibi VPN olmadan bağlantıları engellemek için etkili bir işletim sistemi düzeyinde özelliğe sahip değildir ve iOS'un ağ uzantıları için yapay bir bellek sınırı vardır, bu da Orbot'ta Tor'u çökmeden çalıştırmayı zorlaştırır. Şu anda Tor'u masaüstü bilgisayarda kullanmak mobil cihazda kullanmaya kıyasla her zaman daha güvenlidir.

## Onion Browser (iOS)

<div class="admonition recommendation" markdown>

![Onion Browser logosu](assets/img/self-contained-networks/onion_browser.svg){ align=right }

**Onion Browser**, iOS cihazlarda Tor ağı üzerinden anonim olarak web'de gezinmenizi sağlayan açık kaynaklı bir tarayıcıdır ve [Tor Projesi](https://support.torproject.org/glossary/onion-browser) tarafından desteklenmektedir. [:octicons-home-16: Ana Sayfa](https://cryptomator.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://cryptomator.org/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.cryptomator.org){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/cryptomator){ .card-link title="Source Code" }
[:octicons-heart-16:](https://cryptomator.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>İndirmeler</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id519296448)

</details>

</div>

Onion Browser, masaüstü platformlarda Tor Browser ile aynı düzeyde gizlilik koruması sağlamaz. Sıradan kullanım için gizli hizmetlere erişmenin mükemmel bir yoludur, ancak gelişmiş düşmanlar tarafından izlenmekten veya izlenmekten endişe ediyorsanız, buna bir anonimlik aracı olarak güvenmemelisiniz.

[Özellikle](https://github.com/privacyguides/privacyguides.org/issues/2929), Onion Browser tüm isteklerin Tor üzerinden geçeceğini *garanti* etmez. Tor'un yerleşik sürümünü kullanırken, WebKit'in sınırlamaları nedeniyle [gerçek IP'niz WebRTC ve ses/video akışları aracılığıyla **sızdırılacaktır**](https://onionbrowser.com/faqs). Onion Browser'ı Orbot ile birlikte kullanmak *daha güvenlidir*, ancak bu yine de iOS'ta bazı sınırlamalarla birlikte gelir (yukarıdaki Orbot bölümünde belirtilmiştir).

[^1]: `IsolateDestAddr` ayarı [Tor posta listesinde](https://lists.torproject.org/pipermail/tor-talk/2012-May/024403.html) ve [Whonix'in Stream Isolation belgelerinde](https://whonix.org/wiki/Stream_Isolation) tartışılmaktadır ve her iki proje de bunun çoğu insan için genellikle iyi bir yaklaşım olmadığını önermektedir.
