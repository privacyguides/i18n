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

[Részletes Tor áttekintés :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button}

<div class="admonition tip" markdown>
<p class="admonition-title">Tanács</p>

Mielőtt csatlakoznál a Torhoz, kérjük, olvasd el az [áttekintést](advanced/tor-overview.md) arról, hogy mi a Tor és hogyan csatlakozhatsz hozzá biztonságosan. Javasoljuk, hogy a Torhoz egy megbízható [VPN szolgáltató](vpn.md) segítségével csatlakozz, de ezt **megfelelően** kell tenned, hogy elkerüld az anonimitásod csökkenését.

</div>

There are a variety of ways to connect to the Tor network from your device, the most commonly used being the **Tor Browser**, a fork of Firefox designed for [:material-incognito: anonymous](basics/common-threats.md#anonymity-vs-privacy ""){.pg-purple} browsing for desktop computers and Android.

Néhány ilyen alkalmazás jobb, mint mások, a választás a fenyegetettségi szintedtől függ. Ha alkalmi Tor-felhasználó vagy, és nem aggódsz amiatt, hogy az internetszolgáltatód bizonyítékokat gyűjt rólad, akkor az olyan alkalmazások, mint az [Orbot](#orbot) vagy a mobil böngésző alkalmazások használata a Tor-hálózat eléréséhez valószínűleg rendben van. Az emberek számának növelése, akik mindennaposan használják a Tor-t, segít csökkenteni a Tor rossz hírnevét, és csökkenti az ISP-k (internetszolgáltatók) és kormányok által összeállított "Tor felhasználók listáinak" minőségét.

Ha a teljes anonimitás a legfontosabb számodra, akkor **csak** az asztali Tor Browser klienst használd, ideális esetben egy [Whonix](desktop.md#whonix) + [Qubes](desktop.md#qubes-os) konfigurációban. Mobile browsers are less common on Tor (and more fingerprintable as a result), and other configurations are not as rigorously tested against de-anonymization.

## Tor Böngésző

<div class="admonition recommendation" markdown>

![Tor Browser logo](assets/img/browsers/tor.svg){ align=right }

A **Tor Böngésző** a legjobb választás, ha anonimitásra van szükséged, mivel hozzáférést biztosít a Tor-hálózathoz és a Tor-hidakhoz, valamint alapértelmezett beállításokat és bővítményeket tartalmaz, amelyek automatikusan előre beállított biztonsági szintek alapján vannak konfigurálva: *Normál*, *Biztonságosabb* és *Legbiztonságosabb*.

[:octicons-home-16: Honlap](https://torproject.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion szolgáltatás" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=Dokumentáció}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/tor-browser){ .card-link title="Forráskód" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Támogatás}

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

A Tor böngészőt úgy tervezték, hogy megakadályozza az ujjlenyomatolást, vagyis a beazonosításodat a böngésző konfigurációja alapján. Ezért elengedhetetlen, hogy **ne** módosítsd a böngészőt az alapértelmezett [biztonsági szinteken](https://tb-manual.torproject.org/security-settings) túl.

A Tor Böngésző közvetlen számítógépre telepítése mellett vannak olyan operációs rendszerek is, amelyeket kifejezetten a Tor-hálózathoz való csatlakozásra terveztek, mint például a [Whonix](desktop.md#whonix) a [Qubes OS-en](desktop.md#qubes-os), amelyek még nagyobb biztonságot és védelmet nyújtanak, mint a hagyományos Tor Browser önmagában.

## Orbot

<div class="admonition recommendation" markdown>

![Orbot logo](assets/img/self-contained-networks/orbot.svg){ align=right }

Az **Orbot** egy ingyenes Tor VPN okostelefonokhoz, amely a Tor hálózaton keresztül irányítja az eszközödön lévő bármely alkalmazás forgalmát.

[:octicons-home-16: Honlap](https://orbot.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://orbot.app/privacy-policy){ .card-link title="Adatvédelmi tájékoztató" }
[:octicons-info-16:](https://orbot.app/faqs){ .card-link title=Dokumentáció}
[:octicons-code-16:](https://orbot.app/code){ .card-link title="Forráskód" }
[:octicons-heart-16:](https://orbot.app/donate){ .card-link title=Támogatás}

<details class="downloads" markdown>
<summary>Letöltés</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1609461599)
- [:simple-github: GitHub](https://github.com/guardianproject/orbot/releases)

</details>

</div>

Korábban ajánlottuk az *Célcím elszigetelése* beállítás engedélyezését az Orbot beállításaiban. Bár ez a beállítás elméletileg javíthatja az adatvédelmet azáltal, hogy minden egyes IP-címhez más-más áramkör használatát kényszeríti, a legtöbb alkalmazásnál (különösen webböngészésnél) nem nyújt gyakorlati előnyt, jelentős teljesítménycsökkenéssel járhat, és növeli a Tor hálózat terhelését. We no longer recommend adjusting this setting from its default value unless you know you need to.[^1]

<div class="admonition tip" markdown>
<p class="admonition-title">Tippek Androidhoz</p>

Az Orbot képes egyes alkalmazások forgalmát átküldeni egy proxyn, ha azok támogatják a SOCKS vagy a HTTP proxyt. A [VpnService](https://developer.android.com/reference/android/net/VpnService) segítségével az összes hálózati kapcsolatodat proxyként is képes kezelni, és a VPN killswitch segítségével is használható a :gear: **beállítások** → **Hálózat és internet** → **VPN** → :gear: → **VPN nélküli kapcsolatok blokkolása** menüpontban.

Az Orbot gyakran elavult szokott lenni a Guardian Project [F-Droid adattárjában](https://guardianproject.info/fdroid) és a [Google Playen](https://play.google.com/store/apps/details?id=org.torproject.android), ezért érdemes inkább közvetlenül a [GitHub adattárból](https://github.com/guardianproject/orbot/releases) letölteni.

Minden verzió ugyanazzal az aláírással van aláírva, így kompatibilisnek kell lenniük egymással.

</div>

## Onion Browser (iOS)

<div class="admonition recommendation" markdown>

![Onion Browser logo](assets/img/self-contained-networks/onion_browser.svg){ align=right }

Az **Onion Browser** egy nyílt forráskódú böngésző, amely lehetővé teszi a Tor-hálózaton keresztüli anonim böngészést iOS-eszközökön, és amelyet a [Tor Project](https://support.torproject.org/glossary/onion-browser) támogat. [:material-star-box: Read our latest Onion Browser review.](/articles/2024/09/18/onion-browser-review)

[:octicons-home-16: Homepage](https://onionbrowser.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://onionbrowser.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://onionbrowser.com/faqs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/OnionBrowser/OnionBrowser){ .card-link title="Source Code" }
[:octicons-heart-16:](https://onionbrowser.com/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Letöltés</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id519296448)

</details>

</div>

Onion Browser does not provide the same levels of privacy protections as Tor Browser does on desktop platforms. For casual use it is a perfectly fine way to access hidden services, but if you're concerned about being traced or monitored by advanced adversaries you should not rely on this as an anonymity tool.

[^1]: The `IsolateDestAddr` setting is discussed on the [Tor mailing list](https://lists.torproject.org/pipermail/tor-talk/2012-May/024403.html) and [Whonix's Stream Isolation documentation](https://whonix.org/wiki/Stream_Isolation), where both projects suggest that it is usually not a good approach for most people.
