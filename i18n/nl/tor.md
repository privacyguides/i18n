---
meta_title: "Tor-browser en -netwerk: Anoniem surfen op het web - Privacy Guides"
title: "Tor Netwerk"
icon: simple/torproject
description: Bescherm je surf gedrag tegen pottenkijkers door gebruik te maken van het Tor netwerk, een beveiligd netwerk dat censuur omzeilt.
cover: tor.webp
schema:
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: Tor Browser
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

Het **Tor** netwerk is een groep servers beheerd door vrijwilligers waarmee je gratis verbinding kunt maken en je privacy en veiligheid op het internet kunt verbeteren. Individuen en organisaties kunnen ook informatie delen via het Tor-netwerk met ".onion hidden services" zonder hun privacy in gevaar te brengen. Omdat Tor-verkeer moeilijk te blokkeren en te traceren is, is Tor een effectief middel om censuur te omzeilen.

[:octicons-home-16:](https://torproject.org){ .card-link title=Homepage }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/core/tor){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribute }

Tor werkt door je internetverkeer om te leiden via deze door vrijwilligers beheerde servers, in plaats van een directe verbinding te maken met de site die je probeert te bezoeken. Dit versluiert waar het verkeer vandaan komt, en geen enkele server in het verbindingspad kan het volledige pad zien van waar het verkeer vandaan komt en naartoe gaat, wat betekent dat zelfs de servers die je gebruikt om verbinding te maken jouw anonimiteit niet kunnen doorbreken.

[Gedetailleerd Tor-overzicht :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button}

## Verbinding maken met Tor

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Before connecting to Tor, please ensure you've read our [overview](advanced/tor-overview.md) on what Tor is and how to connect to it safely. We often recommend connecting to Tor through a trusted [VPN provider](vpn.md), but you have to do so **properly** to avoid decreasing your anonymity.

</div>

Er zijn verschillende manieren om verbinding te maken met het Tor-netwerk vanaf je apparaat. De meest gebruikte is de **Tor Browser**, een fork van Firefox ontworpen voor anoniem browsen voor desktop computers en Android.

Some of these apps are better than others, and again making a determination comes down to your threat model. If you are a casual Tor user who is not worried about your ISP collecting evidence against you, using apps like [Orbot](#orbot) or mobile browser apps to access the Tor network is probably fine. Increasing the number of people who use Tor on an everyday basis helps reduce the bad stigma of Tor, and lowers the quality of "lists of Tor users" that ISPs and governments may compile.

If more complete anonymity is paramount to your situation, you should **only** be using the desktop Tor Browser client, ideally in a [Whonix](desktop.md#whonix) + [Qubes](desktop.md#qubes-os) configuration. Mobile browsers are less common on Tor (and more fingerprintable as a result), and other configurations are not as rigorously tested against deanonymization.

### Tor Browser

<div class="admonition recommendation" markdown>

![Tor Browser logo](assets/img/browsers/tor.svg){ align=right }

**Tor Browser** is de keuze als je anonimiteit nodig hebt, omdat het je toegang geeft tot het Tor netwerk en bruggen, en het bevat standaard instellingen en extensies die automatisch geconfigureerd worden door de standaard beveiligingsniveaus: *Standard*, *Safer* en *Safest*.

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

Je moet **nooit** extra extensies installeren op Tor Browser of `about:config` instellingen bewerken, inclusief de extensies die we voorstellen voor Firefox. Browserextensies en niet-standaardinstellingen zorgen ervoor dat je je onderscheidt van anderen op het Tor-netwerk, waardoor je browser gemakkelijker te vinden is op [fingerprint](https://support.torproject.org/glossary/browser-fingerprinting).

</div>

De Tor Browser is ontworpen om fingerprinting, of het identificeren van jou op basis van je browserconfiguratie, te voorkomen. Therefore, it is imperative that you do **not** modify the browser beyond the default [security levels](https://tb-manual.torproject.org/security-settings).

In addition to installing Tor Browser on your computer directly, there are also operating systems designed specifically to connect to the Tor network such as [Whonix](desktop.md#whonix) on [Qubes OS](desktop.md#qubes-os), which provide even greater security and protections than the standard Tor Browser alone.

### Orbot

<div class="admonition recommendation" markdown>

![Orbot logo](assets/img/self-contained-networks/orbot.svg){ align=right }

**Orbot** is een gratis Tor VPN voor smartphones die het verkeer van elke app op je toestel door het Tor-netwerk leidt.

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

Wij hebben eerder aanbevolen *Isolate Destination Address* in de Orbot instellingen in te schakelen. Hoewel deze instelling theoretisch de privacy kan verbeteren door het gebruik van een ander circuit af te dwingen voor elk IP adres waarmee je verbinding maakt, biedt het geen praktisch voordeel voor de meeste toepassingen (vooral web browsen), kan het gepaard gaan met een aanzienlijke prestatievermindering en verhoogt het de belasting van het Tor netwerk. Wij raden je niet langer aan deze instelling te wijzigen ten opzichte van de standaardwaarde, tenzij je weet dat het nodig is.[^1]

<div class="admonition tip" markdown>
<p class="admonition-title">Tips for Android</p>

Orbot kan individuele apps proxyen als ze SOCKS of HTTP proxying ondersteunen. It can also proxy all your network connections using [VpnService](https://developer.android.com/reference/android/net/VpnService) and can be used with the VPN killswitch in :gear: **Settings** → **Network & internet** → **VPN** → :gear: → **Block connections without VPN**.

Orbot is vaak verouderd op de [F-Droid repository](https://guardianproject.info/fdroid) en [Google Play](https://play.google.com/store/apps/details?id=org.torproject.android) van het Guardian Project, dus overweeg in plaats daarvan direct te downloaden van de [GitHub repository](https://github.com/guardianproject/orbot/releases).

Alle versies zijn ondertekend met dezelfde handtekening, zodat ze onderling compatibel zouden moeten zijn.

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

## Relays and Bridges

### Snowflake

<div class="admonition recommendation" markdown>

![Snowflake logo](assets/img/browsers/snowflake.svg#only-light){ align=right }
![Snowflake logo](assets/img/browsers/snowflake-dark.svg#only-dark){ align=right }

**Met Snowflake** kun je bandbreedte doneren aan het Tor Project door een "Snowflake proxy" in je browser te gebruiken.

Mensen die gecensureerd worden kunnen Snowflake proxies gebruiken om verbinding te maken met het Tor-netwerk. Snowflake is een geweldige manier om bij te dragen aan het netwerk, zelfs als je niet de technische know-how hebt om een Tor relay of bridge te runnen.

[:octicons-home-16: Homepage](https://snowflake.torproject.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/Technical%20Overview){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribute }

</details>

</div>

Je kunt Snowflake inschakelen in je browser door deze in een ander tabblad te openen en de schakelaar aan te zetten. Je kunt het op de achtergrond laten werken tijdens het browsen om een bijdrage te leveren met jouw verbinding. We raden het installeren van Snowflake niet aan als een browserextensie; het toevoegen van extensies van derden kan je aanvalsoppervlak vergroten.

[Snowflake uitvoeren in je browser :material-arrow-right-drop-circle:](https://snowflake.torproject.org/embed.html ""){.md-button}

Snowflake verhoogt jouw privacy op geen enkele manier, en wordt ook niet gebruikt om verbinding te maken met het Tor-netwerk binnen jouw persoonlijke browser. Als jouw internetverbinding echter ongecensureerd is, zou je moeten overwegen het te gebruiken om mensen in gecensureerde netwerken te helpen zelf betere privacy te krijgen. Je hoeft je geen zorgen te maken over welke websites mensen via je proxy bezoeken- hun zichtbare surf IP adres zal overeenkomen met hun Tor exit node, niet met die van jou.

Het runnen van een Snowflake proxy is weinig riskant, zelfs meer dan het runnen van een Tor relay of bridge, wat al geen bijzonder riskante onderneming is. Het stuurt echter nog steeds verkeer door jouw netwerk, wat in sommige opzichten gevolgen kan hebben, vooral als jouw netwerk een beperkte bandbreedte heeft. Zorg ervoor dat je [begrijpt hoe Snowflake werkt](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/home) voordat je beslist of je een proxy wilt gebruiken.

[^1]: The `IsolateDestAddr` setting is discussed on the [Tor mailing list](https://lists.torproject.org/pipermail/tor-talk/2012-May/024403.html) and [Whonix's Stream Isolation documentation](https://whonix.org/wiki/Stream_Isolation), where both projects suggest that it is usually not a good approach for most people.
