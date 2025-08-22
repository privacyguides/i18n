---
title: "Réseaux alternatifs"
icon: material/vector-polygon
description: Ces outils vous permettent d'accéder à des réseaux autres que le World Wide Web.
cover: alternative-networks.webp
---

<small>Protects against the following threat(s):</small>

 - [:material-server-network: Service Providers](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }
 - [:material-eye-outline: Mass Surveillance](basics/common-threats.md#mass-surveillance-programs){ .pg-blue }
 - [:material-account-cash: Surveillance Capitalism](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }

## Réseaux d'anonymisation

En ce qui concerne les réseaux d'anonymisation, nous tenons à souligner que [Tor](advanced/tor-overview.md) est notre premier choix. C'est de loin le réseau anonyme le plus utilisé, le plus étudié et le plus activement développé. Using other networks could be more likely to endanger your [:material-incognito: Anonymity](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple }, unless you know what you're doing.

### Tor

<div class="admonition recommendation" markdown>

![Logo Tor](assets/img/self-contained-networks/tor.svg){ align=right }

Le réseau **Tor** est un groupe de serveurs gérés par des bénévoles qui vous permet de vous connecter gratuitement et d'améliorer votre confidentialité et votre sécurité sur Internet. Les particuliers et les organisations peuvent également partager des informations sur le réseau Tor avec des "services cachés .onion" sans compromettre leur vie privée. Because Tor traffic is difficult to block and trace, Tor is an effective [:material-close-outline: Censorship](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray } circumvention tool.

[:octicons-home-16:](https://torproject.org){ .card-link title="Page d'accueil" }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Service onion" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/core/tor){ .card-link title="Code source" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribuer }

</div>

Le moyen recommandé pour accéder au réseau Tor est le navigateur officiel Tor, que nous avons décrit plus en détail sur une page dédiée :

[Informations sur le navigateur Tor :material-arrow-right-drop-circle:](tor.md){ .md-button .md-button--primary } [Introduction détaillée à Tor :material-arrow-right-drop-circle:](advanced/tor-overview.md){ .md-button }

You can access the Tor network using other tools; making this determination comes down to your threat model. If you are a casual Tor user who is not worried about your ISP collecting evidence against you, using apps like [Orbot](#orbot) or mobile browser apps to access the Tor network is probably fine. L'augmentation du nombre de personnes qui utilisent Tor au quotidien permet de réduire la mauvaise image de Tor et de diminuer la qualité des "listes d'utilisateurs de Tor" que les FAIs et les gouvernements peuvent compiler.

<div class="admonition example" markdown>
<p class="admonition-title">Essayez-le!</p>

Vous pouvez essayer de vous connecter à _Privacy Guides_ via Tor à [xoe4vn5uwdztif6goazfbmogh6wh5jc4up35bqdflu6bkdc5cas5vjqd.onion](http://www.xoe4vn5uwdztif6goazfbmogh6wh5jc4up35bqdflu6bkdc5cas5vjqd.onion).

</div>

#### Orbot

<div class="admonition recommendation" markdown>

![Orbot logo](assets/img/self-contained-networks/orbot.svg){ align=right }

**Orbot** is a mobile application which routes traffic from any app on your device through the Tor network.

[:octicons-home-16: Homepage](https://orbot.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://orbot.app/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://orbot.app/faqs){ .card-link title="Documentation" }
[:octicons-code-16:](https://orbot.app/code){ .card-link title="Source Code" }
[:octicons-heart-16:](https://orbot.app/donate){ .card-link title="Contribute" }

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

**Snowflake** vous permet de donner de la bande passante au projet Tor en hébergant un "proxy Snowflake" dans votre navigateur.

Les personnes censurées peuvent utiliser les proxys Snowflake pour se connecter au réseau Tor. Snowflake est un excellent moyen de contribuer au réseau même si vous n'avez pas le savoir-faire technique pour gérer un relais ou un pont Tor.

[:octicons-home-16: Page d'accueil](https://snowflake.torproject.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/Technical%20Overview){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake){ .card-link title="Code source" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribuer }

</details>

</div>

Vous pouvez activer Snowflake dans votre navigateur en l'ouvrant dans un autre onglet et en activant l'interrupteur. Vous pouvez le laisser fonctionner en arrière-plan pendant que vous naviguez pour contribuer avec votre connexion. Nous ne recommandons pas d'installer Snowflake en tant qu'extension de navigateur, car l'ajout d'extensions tierces peut augmenter votre surface d'attaque.

[Exécuter snowflake dans votre navigateur :material-arrow-right-drop-circle:](https://snowflake.torproject.org/embed.html){ .md-button }

Snowflake n'améliore en rien votre vie privée et n'est pas utilisé pour se connecter au réseau Tor depuis votre navigateur personnel. Toutefois, si votre connexion Internet n'est pas censurée, vous devriez envisager de l'utiliser pour aider les personnes se trouvant sur des réseaux censurés à améliorer elles-mêmes leur vie privée. Il n'y a pas besoin de s'inquiéter des sites web auxquels les gens accèdent via votre proxy - leur adresse IP de navigation visible correspondra à leur nœud de sortie Tor, pas à la vôtre.

Running a Snowflake proxy is low-risk, even more so than running a Tor relay or bridge which are already not particularly risky endeavors. Toutefois, il achemine le trafic par le biais de votre réseau, ce qui peut avoir un impact à certains égards, surtout si votre réseau a une bande passante limitée. Assurez-vous de bien comprendre [le fonctionnement de Snowflake](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/home) avant de décider d'utiliser ou non un proxy.

### I2P (Le projet Internet invisible)

<div class="admonition recommendation" markdown>

![logo I2P](assets/img/self-contained-networks/i2p.svg#only-light){ align=right }
![logo I2P](assets/img/self-contained-networks/i2p-dark.svg#only-dark){ align=right }

**I2P** is a network layer which encrypts your connections and routes them via a network of computers distributed around the world. Elle vise principalement à créer un réseau alternatif de protection de la vie privée plutôt qu'à rendre anonymes les connexions internet ordinaires.

[:octicons-home-16: Page d'accueil](https://geti2p.net/en){ .md-button .md-button--primary }
[:octicons-info-16:](https://geti2p.net/en/about/software){ .card-link title=Documentation }
[:octicons-code-16:](https://github.com/i2p/i2p.i2p){ .card-link title="Code source" }
[:octicons-heart-16:](https://geti2p.net/en/get-involved){ .card-link title=Contribuer }

<details class="downloads" markdown>
<summary>Downloads</summary>

 - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.i2p.android)
 - [:simple-android: Android](https://geti2p.net/en/download#android)
 - [:fontawesome-brands-windows: Windows](https://geti2p.net/en/download#windows)
 - [:simple-apple: macOS](https://geti2p.net/en/download#mac)
 - [:simple-linux: Linux](https://geti2p.net/en/download#unix)

</details>

</div>

Contrairement à Tor, tout le trafic I2P est interne au réseau I2P, ce qui signifie que les sites Internet ordinaires ne sont **pas** directement accessibles depuis I2P. A la place, vous pouvez vous connecter à des sites web qui sont hébergés anonymement et directement sur le réseau I2P, qui sont appelés "eepsites" et dont les domaines se terminent par `.i2p`.

<div class="admonition example" markdown>
<p class="admonition-title">Essayez-le!</p>

Vous pouvez essayer de vous connecter à _Privacy Guides_ via I2P à l'adresse [privacyguides.i2p](http://privacyguides.i2p/?i2paddresshelper=fvbkmooriuqgssrjvbxu7nrwms5zyhf34r3uuppoakwwsm7ysv6q.b32.i2p).

</div>

En outre, contrairement à Tor, chaque nœud I2P relaiera par défaut le trafic pour les autres utilisateurs, au lieu de s'appuyer sur des volontaires de relais dédiés pour faire fonctionner les nœuds. Il y a environ [10 000](https://metrics.torproject.org/networksize.html) relais et ponts sur le réseau Tor contre environ 50 000 sur I2P, ce qui signifie qu'il y a potentiellement plus de façons pour votre trafic d'être acheminé afin de maximiser l'anonymat. I2P also tends to be more performant than Tor, although this is likely a side effect of Tor being more focused on regular "clearnet" internet traffic and thus using more bottle necked exit nodes. Les performances des services cachés sont généralement considérées comme bien meilleures sur I2P que sur Tor. Alors que l'exécution d'applications P2P comme BitTorrent est difficile sur Tor (et peut avoir un impact massif sur les performances du réseau Tor), elle est très facile et performante sur I2P.

L'approche de I2P présente toutefois des inconvénients. Le fait que Tor s'appuie sur des nœuds de sortie dédiés signifie que davantage de personnes dans des environnements moins sûrs peuvent l'utiliser, et les relais qui existent sur Tor sont susceptibles d'être plus performants et plus stables, car ils ne sont généralement pas exécutés sur des connexions résidentielles. Tor est également beaucoup plus axé sur la **confidentialité du navigateur** (c'est-à-dire empêcher la capture d'empreintes numériques), avec un [Navigateur Tor](tor.md) dédié pour rendre l'activité de navigation aussi anonyme que possible. I2P est utilisé via votre [navigateur web ordinaire](desktop-browsers.md), et bien que vous puissiez configurer votre navigateur pour mieux protéger votre vie privée, vous n'aurez probablement pas la même empreinte numérique de navigateur que les autres utilisateurs de I2P (il n'y a pas de "foule" à laquelle se fondre à cet égard).

Tor est susceptible de mieux résister à la censure, en raison de son solide réseau de ponts et de divers [transports enfichables] (https://tb-manual.torproject.org/circumvention). D'autre part, l'I2P utilise des serveurs d'annuaire pour la connexion initiale, qui varient, ne sont pas fiables et sont gérés par des bénévoles, alors que Tor utilise des serveurs codés en dur et fiables, qui sont probablement plus faciles à bloquer.

[^1]: The `IsolateDestAddr` setting is discussed on the [Tor mailing list](https://lists.torproject.org/pipermail/tor-talk/2012-May/024403) and [Whonix's Stream Isolation documentation](https://whonix.org/wiki/Stream_Isolation), where both projects suggest that it is usually not a good approach for most people.
