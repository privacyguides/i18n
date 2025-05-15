---
meta_title: "Tor böngésző és hálózat: névtelen webes böngészés – Privacy Guides"
title: "Tor Böngésző"
icon: simple/torbrowser
description: Védd meg internetes böngészésed a kíváncsi szemek elől egy biztonságos hálózat, a Tor használatával, amely megkerüli a cenzúrát.
cover: tor.webp
schema:
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Tor Böngésző
    image: /assets/img/browsers/tor.svg
    url: https://www.torproject.org/hu/
    sameAs: https://hu.wikipedia.org/wiki/Tor_(szoftver)
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

<small>Protects against the following threat(s):</small>

- [:material-account-cash: Surveillance Capitalism](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}
- [:material-eye-outline: Mass Surveillance](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-close-outline: Censorship](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}

**Tor** is a group of volunteer-operated servers that allows you to connect for free and improve your privacy and security on the Internet. A magánszemélyek és szervezetek a Tor-hálózaton keresztül a ".onion rejtett szolgáltatásokkal" is megoszthatnak információkat anélkül, hogy veszélyeztetnék a magánéletüket. Mivel a Tor forgalmat nehéz blokkolni és nyomon követni, a Tor hatékony eszköz a cenzúra megkerülésére.

[Detailed Tor Overview :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button.md-button--primary} [:material-movie-open-play-outline: Video: Why You Need Tor](https://www.privacyguides.org/videos/2025/03/02/why-you-need-tor ""){.md-button}

<div class="admonition tip" markdown>
<p class="admonition-title">Tanács</p>

Mielőtt csatlakoznál a Torhoz, kérjük, olvasd el az [áttekintést](advanced/tor-overview.md) arról, hogy mi a Tor és hogyan csatlakozhatsz hozzá biztonságosan. Javasoljuk, hogy a Torhoz egy megbízható [VPN szolgáltató](vpn.md) segítségével csatlakozz, de ezt **megfelelően** kell tenned, hogy elkerüld az anonimitásod csökkenését.

</div>

There are a variety of ways to connect to the Tor network from your device, the most commonly used being the **Tor Browser**, a fork of Firefox designed for [:material-incognito: anonymous](basics/common-threats.md#anonymity-vs-privacy ""){.pg-purple} browsing for desktop computers and Android.

Some of these apps are better than others; making a determination comes down to your threat model. If you are a casual Tor user who is not worried about your ISP collecting evidence against you, using mobile browser apps like [Onion Browser](#onion-browser-ios) to access the Tor network is probably fine. Az emberek számának növelése, akik mindennaposan használják a Tor-t, segít csökkenteni a Tor rossz hírnevét, és csökkenti az ISP-k (internetszolgáltatók) és kormányok által összeállított "Tor felhasználók listáinak" minőségét.

Ha a teljes anonimitás a legfontosabb számodra, akkor **csak** az asztali Tor Browser klienst használd, ideális esetben egy [Whonix](desktop.md#whonix) + [Qubes](desktop.md#qubes-os) konfigurációban. Mobile browsers are less common on Tor (and more fingerprintable as a result), and other configurations are not as rigorously tested against deanonymization.

## Tor Böngésző

<div class="admonition recommendation" markdown>

![Tor Browser logo](assets/img/browsers/tor.svg){ align=right }

**Tor Browser** is the top choice if you need anonymity, as it provides you with access to the Tor network and bridges, and it includes default settings and extensions that are automatically configured by the default security levels: *Standard*, *Safer* and *Safest*.

[:octicons-home-16: Homepage](https://torproject.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title="Documentation" }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/tor-browser){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title="Contribute" }

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
<p class="admonition-title">Vigyázat!</p>

**Soha** nem telepíts semmilyen további bővítményt a Tor Böngészőre vagy szerkeszd az `about:config` beállításokat, beleértve azokat is, amelyeket a Firefoxhoz javasolunk. A böngésző bővítmények és a nem alap beállítások miatt kitűnsz a Tor-hálózat többi felhasználója közül, így téve a böngésződ könnyebben [fingerprintelhetővé](https://support.torproject.org/glossary/browser-fingerprinting).

</div>

A Tor böngészőt úgy tervezték, hogy megakadályozza az ujjlenyomatolást, vagyis a beazonosításodat a böngésző konfigurációja alapján. Ezért elengedhetetlen, hogy **ne** módosítsd a böngészőt az alapértelmezett [biztonsági szinteken](https://tb-manual.torproject.org/security-settings) túl. When modifying the security level setting, you **must** always restart the browser before continuing to use it. Otherwise, [the security settings may not be fully applied](https://www.privacyguides.org/articles/2025/05/02/tor-security-slider-flaw), putting you at a higher risk of fingerprinting and exploits than you may expect based on the setting chosen.

A Tor Böngésző közvetlen számítógépre telepítése mellett vannak olyan operációs rendszerek is, amelyeket kifejezetten a Tor-hálózathoz való csatlakozásra terveztek, mint például a [Whonix](desktop.md#whonix) a [Qubes OS-en](desktop.md#qubes-os), amelyek még nagyobb biztonságot és védelmet nyújtanak, mint a hagyományos Tor Browser önmagában.

## Onion Browser (iOS)

<div class="admonition recommendation" markdown>

![Onion Browser logo](assets/img/self-contained-networks/onion_browser.svg){ align=right }

Az **Onion Browser** egy nyílt forráskódú böngésző, amely lehetővé teszi a Tor-hálózaton keresztüli anonim böngészést iOS-eszközökön, és amelyet a [Tor Project](https://support.torproject.org/glossary/onion-browser) támogat.

[:material-star-box: Read our latest Onion Browser review.](https://www.privacyguides.org/articles/2024/09/18/onion-browser-review)

[:octicons-home-16: Homepage](https://onionbrowser.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://onionbrowser.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://onionbrowser.com/faqs){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/OnionBrowser/OnionBrowser){ .card-link title="Source Code" }
[:octicons-heart-16:](https://onionbrowser.com/donate){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Letöltés</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id519296448)

</details>

</div>

Onion Browser does not provide the same levels of privacy protections as Tor Browser does on desktop platforms. For casual use it is a perfectly fine way to access hidden services, but if you're concerned about being traced or monitored by advanced adversaries you should not rely on this as an anonymity tool.

[Notably](https://github.com/privacyguides/privacyguides.org/issues/2929), Onion Browser does not *guarantee* all requests go through Tor. When using the built-in version of Tor, [your real IP **will** be leaked via WebRTC and audio/video streams](https://onionbrowser.com/faqs) due to limitations of WebKit. It is *safer* to use Onion Browser alongside [Orbot](alternative-networks.md#orbot), but this still comes with some limitations on iOS.
