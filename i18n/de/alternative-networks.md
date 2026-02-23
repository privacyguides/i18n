---
title: "Alternative Netzwerke"
icon: material/vector-polygon
description: These Werkzeuge erlauben dir Zugriff zu Netzwerke außerhalb des World Wide Webs.
cover: alternative-networks.webp
---

<small>Schützt vor der/den folgenden Bedrohung(en):</small>

- [:material-server-network: Dienstanbieter](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }
- [:material-eye-outline: Massenüberwachung](basics/common-threats.md#mass-surveillance-programs){ .pg-blue }
- [:material-account-cash: Überwachungskapitalismus](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

## Anonymisierungsnetzwerke

Wenn es zu Anonymisierungsnetzwerke kommt, wollen wir notieren das [Tor](advanced/tor-overview.md) unsere erste Wahl ist. Es ist bei weitem das meist verwendetes, robust untersuchtes und aktiv entwickeltes anonymes Netzwerk. Das Nutzen von anderen Netzwerken bringt größere Gefahr zu deiner [:material-incognito: Anonymität](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple }, außer wenn du weißt was du machst.

### Tor

<div class="admonition recommendation" markdown>

![Tor logo](assets/img/self-contained-networks/tor.svg){ align=right }

Das **Tor** Netzwerk ist eine Gruppe von Freiwilligen betriebenen Servern die dir erlauben, sich kostenlos zu verbinden und deine Privatsphäre und Sicherheit im Internet zu verbessern. Einzelpersonen und Organisationen können auch Informationen über das Tor-Netzwerk mit ".onion versteckten Diensten" austauschen, ohne ihre Privatsphäre zu gefährden. Da Tor Verkehr schwer zu blockieren und zu verfolgen ist, ist Tor ein effektives Werkzeug gegen [:material-close-outline: Zensur](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }.

[:octicons-home-16:](https://torproject.org){ .card-link title=Homepage }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=Dokumentation }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/core/tor){ .card-link title="Quellcode" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=beitragen }

</div>

Der empfohlene Weg um das Tor Netzwerk zuzugreifen ist über den offiziellen Tor Browser, die folgende Seite beinhaltet mehr Informationen über den Browser:

Du kannst das Tor Netzwerk mit anderen Werkzeugen zugreifen, dies ist abhängig von deinem Bedrohungsmodell.

Du kannst das Tor Netzwerk mit anderen Werkzeugen zugreifen, dies ist abhängig von deinem Bedrohungsmodell. Wenn du ein normaler Tor Nutzer bist, der keine Sorgen macht, dass dein Internetanbieter Beweise über dich sammelt, dann sind Apps wie [Orbot](#orbot) oder Mobile Browser Apps zum Zugriff vom Tor Netzwerk unproblematisch. Wenn mehr Menschen regelmäßig Tor nutzen, hilft das, das schlechte Stigma von Tor zu verringern und senkt zudem die Qualität der "Listen von Tor-Nutzern", die ISPs und Regierungen erstellen können.

<div class="admonition example" markdown>
<p class="admonition-title">Versuche es!</p>

Du kannst versuchen, über Tor bei [xoe4vn5uwdztif6goazfbmogh6wh5jc4up35bqdflu6bkdc5cas5vjqd.onion](http://www.xoe4vn5uwdztif6goazfbmogh6wh5jc4up35bqdflu6bkdc5cas5vjqd.onion) _Privacy Guides_ zu öffnen.

</div>

#### Orbot

<div class="admonition recommendation" markdown>

![Orbot logo](assets/img/self-contained-networks/orbot.svg){ align=right }

**Orbot** ist eine Handy-App, die Verkehr von jeder App auf deinem Handy über das Tor Netzwerk sendet.

[:octicons-home-16: Homepage](https://orbot.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://orbot.app/privacy-policy){ .card-link title="Datenschutzbestimmungen" }
[:octicons-info-16:](https://orbot.app/faqs){ .card-link title="Dokumentation" }
[:octicons-code-16:](https://orbot.app/code){ .card-link title="Quellcode" }
[:octicons-heart-16:](https://orbot.app/donate){ .card-link title="beitragen" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1609461599)
- [:simple-github: GitHub](https://github.com/guardianproject/orbot/releases)
- [:simple-fdroid: F-Droid](https://guardianproject.info/fdroid)

</details>

</div>

We previously recommended enabling the _Isolate Destination Address_ preference in Orbot settings. While this setting can theoretically improve privacy by enforcing the use of a different circuit for each IP address you connect to, it doesn't provide a practical advantage for most applications (especially web browsing), can come with a significant performance penalty, and increases the load on the Tor network. We no longer recommend adjusting this setting from its default value unless you know you need to.[^1]

\=== "Android"

```
Orbot can proxy individual apps if they support SOCKS or HTTP proxying. It can also proxy all your network connections using [VpnService](https://developer.android.com/reference/android/net/VpnService) and can be used with the VPN kill switch in :gear: **Settings** → **Network & internet** → **VPN** → :gear: → **Block connections without VPN**.

Orbot is often outdated on Google Play and the Guardian Project's F-Droid repository, so consider downloading directly from the GitHub repository instead. All versions are signed using the same signature, so they should be compatible with each other.
```

\=== "iOS"

```
On iOS, Orbot has some limitations that could potentially cause crashes or leaks: iOS does not have an effective OS-level feature to block connections without a VPN like Android does, and iOS has an artificial memory limit for network extensions that makes it challenging to run Tor in Orbot without crashes. Currently, it is always safer to use Tor on a desktop computer compared to a mobile device.
```

#### Snowflake

<div class="admonition recommendation" markdown>

![Snowflake logo](assets/img/self-contained-networks/snowflake.svg#only-light){ align=right }
![Snowflake logo](assets/img/self-contained-networks/snowflake-dark.svg#only-dark){ align=right }

**Snowflake** erlaubt dir Bandbreite zum Tor Projekt zu schenken, indem man innerhalb seines Browsers eine "Snowflake Proxy" betreibt.

Leute die zensiert werden, können Snowflake-Proxies benutzen, um sich zum Tor Netzwerk zu verbinden. Snowflake ist ein guter Weg zum Netzwerk beizutragen, auch wenn man nicht das technische Know-How hat, um ein Tor Relay oder Bridge zu betreiben.

[:octicons-home-16: Homepage](https://snowflake.torproject.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/Technical%20Overview){ .card-link title=Dokumentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake){ .card-link title="QuellCode" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=beitragen }

</details>

</div>

Du kannst Snowflake in deinem Browser aktivieren, indem man es in einem neuen Tab öffnet und den Schalter aktiviert. Du kannst es in Hintergrund laufen lassen während du browst, um deine Verbindung beizutragen. Wir empfehlen nicht Snowflake als Browsererweiterung, weil Erweiterungen von Dritten deine Angriffsoberfläche vergrößert.

[Führe Snowflake in deinem Browser aus :material-arrow-right-drop-circle:](https://snowflake.torproject.org/embed.html){ .md-button }

Snowflake erhöht nicht deine Privatsphäre, ebenfalls kann es auch nicht benutzt werden um, innerhalb deines persönlichen Browsers Zugriff aufs Tor Netzwerk zu bekommen. Allerdings solltest du es Berücksichtigen, wenn deine Internetverbindung unzensiert ist, da es Leuten mit zensierter Verbinden mit deren Privatsphären helfen kann. Es gibt keinen Grund sich Sorgen zu machen, welche Webseiten Leute durch deiner Proxy besuchen, da ihre sichtbare IP-Adresse der ihrer Tor-Exit-Node entspricht, nicht deiner.

Das Betreiben einer Snowflake Proxy ist risikoarm, da das Betreiben eines Tor-Relays oder Bridge auch nicht sehr Risikoreich ist. Da aber Verkehr durch dein Netzwerk läuft, kann es wirkungsvoll auf deiner Verbindung sein, am meisten, wenn dein Netzwerk eine Bandbreitenlimitierung hat. Stelle siche, dass du verstehst [wie Snowflake funktioniert](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/home) bevor du eine Proxy betreibst.

### I2P (The Invisible Internet Project)

<div class="admonition recommendation" markdown>

![I2P logo](assets/img/self-contained-networks/i2p.svg#only-light){ align=right }
![I2P logo](assets/img/self-contained-networks/i2p-dark.svg#only-dark){ align=right }

**I2P** ist eine Netzwerkschicht, die deine Verbindung verschlüsselt, und sie über ein Netzwerk von Computern auf der ganzen Welt leitet. Es ist hauptsächlich fokussiert ein alternatives, Privatsphäre-schützendes Netzwerk zu erstellen, statt normales Internetverkehr zu anonymisieren.

[:octicons-home-16: Homepage](https://geti2p.net/en){ .md-button .md-button--primary }
[:octicons-info-16:](https://geti2p.net/en/about/software){ .card-link title=Dokumentation }
[:octicons-code-16:](https://github.com/i2p/i2p.i2p){ .card-link title="Quellcode" }
[:octicons-heart-16:](https://geti2p.net/en/get-involved){ .card-link title=beitragen }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.i2p.android)
- [:simple-android: Android](https://geti2p.net/en/download#android)
- [:fontawesome-brands-windows: Windows](https://geti2p.net/en/download#windows)
- [:simple-apple: macOS](https://geti2p.net/en/download#mac)
- [:simple-linux: Linux](https://geti2p.net/en/download#unix)

</details>

</div>

Unlike Tor, all I2P traffic is internal to the I2P network, which means regular internet websites are **not** directly accessible from I2P. Instead, you can connect to websites which are hosted anonymously and directly on the I2P network, which are called "eepsites" and have domains which end in `.i2p`.

<div class="admonition example" markdown>
<p class="admonition-title">Versuche es!</p>

You can try connecting to _Privacy Guides_ via I2P at [privacyguides.i2p](http://privacyguides.i2p/?i2paddresshelper=fvbkmooriuqgssrjvbxu7nrwms5zyhf34r3uuppoakwwsm7ysv6q.b32.i2p).

</div>

Also, unlike Tor, every I2P node will relay traffic for other users by default, instead of relying on dedicated relay volunteers to run nodes. There are approximately [10,000](https://metrics.torproject.org/networksize.html) relays and bridges on the Tor network compared to ~50,000 on I2P, meaning there is potentially more ways for your traffic to be routed to maximize anonymity. I2P also tends to be more performant than Tor, although this is likely a side effect of Tor being more focused on regular "clearnet" internet traffic and thus using more bottle necked exit nodes. Hidden service performance is generally considered to be much better on I2P compared to Tor. While running P2P applications like BitTorrent is challenging on Tor (and can massively impact Tor network performance), it is very easy and performant on I2P.

There are downsides to I2P's approach, however. Tor relying on dedicated exit nodes means more people in less safe environments can use it, and the relays that do exist on Tor are likely to be more performant and stable, as they generally aren't run on residential connections. Tor is also far more focused on **browser privacy** (i.e. anti-fingerprinting), with a dedicated [Tor Browser](tor.md) to make browsing activity as anonymous as possible. I2P is used via your [regular web browser](desktop-browsers.md), and while you can configure your browser to be more privacy-protecting, you probably still won't have the same browser fingerprint as other I2P users (there's no "crowd" to blend in with in that regard).

Tor is likely to be more resistant to censorship, due to their robust network of bridges and varying [pluggable transports](https://tb-manual.torproject.org/circumvention). On the other hand, I2P uses directory servers for the initial connection which are varying/untrusted and run by volunteers, compared to the hard-coded/trusted ones Tor uses which are likely easier to block.

[^1]: The `IsolateDestAddr` setting is discussed on the [Tor mailing list](https://lists.torproject.org/pipermail/tor-talk/2012-May/024403) and [Whonix's Stream Isolation documentation](https://whonix.org/wiki/Stream_Isolation), where both projects suggest that it is usually not a good approach for most people.
