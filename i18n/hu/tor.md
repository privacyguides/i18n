---
meta_title: "Tor Böngésző és Hálózat: Névtelen Webes Böngészés - Privacy Guides"
title: "Tor Hálózat"
icon: simple/torproject
description: Védd meg internetes böngészésed a kíváncsi szemek elől a Tor hálózat, egy biztonságos hálózat használatával, amely megkerüli a cenzúrát.
cover: tor.webp
schema:
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Tor Böngésző
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

![Tor logo](assets/img/self-contained-networks/tor.svg){ align=right }

A **Tor** hálózat egy önkéntesek által üzemeltetett szerverekből álló csoport, amely lehetővé teszi, hogy ingyenesen csatlakozhass, és javíts a magánéleteden, valamint a biztonságodon az Interneten. Személyek és szervezetek a Tor-hálózaton keresztül ".onion rejtett szolgáltatásokkal" is megoszthatnak információkat anélkül, hogy veszélyeztetnék a magánéletüket. Mivel a Tor forgalmat nehéz blokkolni és nyomon követni, a Tor egy hatékony cenzúra megkerülő eszköz.

[:octicons-home-16:](https://torproject.org){ .card-link title=Homepage }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/core/tor){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribute }

A Tor úgy működik, hogy az internetes forgalmadat ezeken az önkéntesek által üzemeltetett szervereken keresztül irányítja át, ahelyett, hogy közvetlen kapcsolatot létesítene a meglátogatni kívánt oldallal. Ez elrejti, hogy honnan érkezik a forgalom, és a kapcsolat útvonalában egyetlen szerver sem látja a teljes útvonalat, ahonnan a forgalom érkezik és ahová tart, ami azt jelenti, hogy még az általad csatlakozásra használt szerverek sem tudják megtörni az anonimitásodat.

[Részletes Tor Áttekintés :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button}

## Csatlakozás a Torhoz

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Before connecting to Tor, please ensure you've read our [overview](advanced/tor-overview.md) on what Tor is and how to connect to it safely. We often recommend connecting to Tor through a trusted [VPN provider](vpn.md), but you have to do so **properly** to avoid decreasing your anonymity.

</div>

A Tor-hálózathoz többféleképpen is csatlakozni lehet a készülékedről, a leggyakrabban használt módszer a **Tor Böngésző**, a Firefox egy asztali számítógépekre és Androidra tervezett forkja, ami alkalmas anonim böngészésre.

Some of these apps are better than others, and again making a determination comes down to your threat model. If you are a casual Tor user who is not worried about your ISP collecting evidence against you, using apps like [Orbot](#orbot) or mobile browser apps to access the Tor network is probably fine. Increasing the number of people who use Tor on an everyday basis helps reduce the bad stigma of Tor, and lowers the quality of "lists of Tor users" that ISPs and governments may compile.

If more complete anonymity is paramount to your situation, you should **only** be using the desktop Tor Browser client, ideally in a [Whonix](desktop.md#whonix) + [Qubes](desktop.md#qubes-os) configuration. Mobile browsers are less common on Tor (and more fingerprintable as a result), and other configurations are not as rigorously tested against deanonymization.

### Tor Böngésző

<div class="admonition recommendation" markdown>

![Tor Browser logo](assets/img/browsers/tor.svg){ align=right }

A **Tor Böngésző** a legjobb választás, ha anonimitásra van szükséged, mivel hozzáférést biztosít a Tor-hálózathoz és a Tor-hidakhoz, valamint alapértelmezett beállításokat és bővítményeket tartalmaz, amelyek automatikusan előre beállított biztonsági szintek alapján vannak konfigurálva: *Normál*, *Biztonságosabb* és *Legbiztonságosabb*.

[:octicons-home-16: Homepage](https://torproject.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=Documentation }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/tor-browser){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
- [:simple-android: Android](https://torproject.org/download/#android)
- [:simple-windows11: Windows](https://torproject.org/download)
- [:simple-apple: macOS](https://torproject.org/download)
- [:simple-linux: Linux](https://torproject.org/download)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

**Soha** nem telepíts semmilyen további bővítményt a Tor Böngészőre vagy szerkeszd az `about:config` beállításokat, beleértve azokat is, amelyeket a Firefoxhoz javasolunk. A böngésző bővítmények és a nem alap beállítások miatt kitűnsz a Tor-hálózat többi felhasználója közül, így téve a böngésződ könnyebben [fingerprintelhetővé](https://support.torproject.org/glossary/browser-fingerprinting).

</div>

A Tor böngészőt úgy tervezték, hogy megakadályozza az fingerprintelést, vagyis a beazonosításodat a böngésző konfigurációja alapján. Therefore, it is imperative that you do **not** modify the browser beyond the default [security levels](https://tb-manual.torproject.org/security-settings).

In addition to installing Tor Browser on your computer directly, there are also operating systems designed specifically to connect to the Tor network such as [Whonix](desktop.md#whonix) on [Qubes OS](desktop.md#qubes-os), which provide even greater security and protections than the standard Tor Browser alone.

### Orbot

<div class="admonition recommendation" markdown>

![Orbot logo](assets/img/self-contained-networks/orbot.svg){ align=right }

Az **Orbot** egy ingyenes Tor VPN okostelefonokhoz, amely a Tor hálózaton keresztül irányítja az eszközödön lévő bármely alkalmazás forgalmát.

[:octicons-home-16: Homepage](https://orbot.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://orbot.app/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://orbot.app/faqs){ .card-link title=Documentation}
[:octicons-code-16:](https://orbot.app/code){ .card-link title="Source Code" }
[:octicons-heart-16:](https://orbot.app/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1609461599)
- [:simple-github: GitHub](https://github.com/guardianproject/orbot/releases)

</details>

</div>

Korábban ajánlottuk az *Isolate Destination Address* beállítás engedélyezését az Orbot beállításaiban. Bár ez a beállítás elméletileg javíthatja az adatvédelmet azáltal, hogy minden egyes IP-címhez más-más áramkör használatát kényszeríti, a legtöbb alkalmazásnál (különösen webböngészésnél) nem nyújt gyakorlati előnyt, jelentős teljesítménycsökkenéssel járhat, és növeli a Tor hálózat terhelését. Többé már nem javasoljuk, hogy ezt a beállítást az alapértelmezett értékétől eltérően módosítsd, kivéve, ha tudod, hogy szükséged van rá.[^1]

<div class="admonition tip" markdown>
<p class="admonition-title">Tips for Android</p>

Az Orbot képes egyes alkalmazások forgalmát átküldeni egy proxyn, ha azok támogatják a SOCKS vagy a HTTP proxyt. It can also proxy all your network connections using [VpnService](https://developer.android.com/reference/android/net/VpnService) and can be used with the VPN killswitch in :gear: **Settings** → **Network & internet** → **VPN** → :gear: → **Block connections without VPN**.

Az Orbot gyakran elavult szokott lenni a Guardian Project [F-Droid adattárjában](https://guardianproject.info/fdroid) és a [Google Playen](https://play.google.com/store/apps/details?id=org.torproject.android), ezért érdemes inkább közvetlenül a [GitHub adattárból](https://github.com/guardianproject/orbot/releases) letölteni.

Minden verzió ugyanazzal az aláírással van tanusítva, így kompatibilisnek kéne egymással lenniük.

</div>

### Onion Browser

<div class="admonition recommendation" markdown>

![Onion Browser logo](assets/img/self-contained-networks/onion_browser.svg){ align=right }

**Onion Browser** is an open-source browser that lets you browse the web anonymously over the Tor network on iOS devices and is endorsed by the [Tor Project](https://support.torproject.org/glossary/onion-browser).

[:octicons-home-16: Homepage](https://onionbrowser.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://onionbrowser.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://onionbrowser.com/faqs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/OnionBrowser/OnionBrowser){ .card-link title="Source Code" }
[:octicons-heart-16:](https://onionbrowser.com/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id519296448)

</details>

</div>

## Elosztók and Hidak

### Snowflake

<div class="admonition recommendation" markdown>

![Snowflake logo](assets/img/browsers/snowflake.svg#only-light){ align=right }
![Snowflake logo](assets/img/browsers/snowflake-dark.svg#only-dark){ align=right }

A **Snowflake** lehetővé teszi, hogy sávszélességet adományozz a Tor projektnek azáltal, hogy egy "Snowflake proxy"-t működtetsz a böngésződben.

Azok, akik cenzúra alatt állnak, Snowflake proxykat tudnak használni a Tor-hálózathoz való csatlakozáshoz. A Snowflake egy nagyszerű módja annak, hogy hozzájárulj a hálózathoz, még akkor is, ha nincs meg a technikai tudásod egy Tor elosztó vagy híd üzemeltetéséhez.

[:octicons-home-16: Homepage](https://snowflake.torproject.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/Technical%20Overview){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribute }

</details>

</div>

A Snowflake-et engedélyezheted a böngésződben úgy, hogy megnyitod azt egy másik lapon, és aktiválod a kapcsolót. Futni hagyhatod a háttérben, hogy hozzájárulj a kapcsolatoddal böngészés közben. Nem javasoljuk a Snowflake böngésző bővítményként való telepítését; harmadik féltől származó bővítmények hozzáadása növelheti a támadási felületet.

[A Snowflake futtatása böngészőben :material-arrow-right-drop-circle:](https://snowflake.torproject.org/embed.html ""){.md-button}

A Snowflake semmilyen módon nem növeli az magánéletedet, és a személyes böngésződön keresztül a Tor-hálózathoz kapcsolódni sem használatos. Ha azonban az internetkapcsolatod nincs cenzúrázva, érdemes megfontolni a futtatását, hogy segíts cenzúrázott hálózatokon lévő személyeknek jobb magánéletet elérni. Nem kell aggódnod amiatt, hogy személyek milyen weboldalakhoz férnek hozzá a proxydon keresztül - a látható böngészési IP-címük majd megegyezik a Tor kilépő csomópontjukkal nem pedig tieddel.

Egy Snowflake proxy futtatása alacsony kockázatú, még inkább, mint egy Tor elosztó vagy híd futtatása, amelyek már eleve sem különösebben kockázatos vállalkozások. Ettől függetlenül még mindig forgalom kerül átküldésre a hálózatodon ami bizonyos szempontból hatással lehet arra, különösen, ha a hálózatod sávszélessége korlátozott. Győződj meg róla, hogy érted [hogyan működik a Snowflake](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/home) mielőtt eldöntöd, hogy futtatsz-e proxyt.

[^1]: The `IsolateDestAddr` setting is discussed on the [Tor mailing list](https://lists.torproject.org/pipermail/tor-talk/2012-May/024403.html) and [Whonix's Stream Isolation documentation](https://whonix.org/wiki/Stream_Isolation), where both projects suggest that it is usually not a good approach for most people.
