---
title: "Frontends"
icon: material/flip-to-front
description: These open-source frontends for various internet services allow you to access content without JavaScript or other annoyances.
cover: frontends.webp
---

Soms proberen diensten je te dwingen zich aan te melden voor een account door de toegang tot inhoud te blokkeren met vervelende popups. Ze kunnen ook breken zonder JavaScript. Met deze frontends kunt je deze beperkingen omzeilen.

Bij zelf-hosting is het belangrijk dat er ook andere mensen gebruik maken van jouw instantie, zodat je op kunt gaan in de menigte. Je moet voorzichtig zijn met waar en hoe je host, omdat het gebruik van andere mensen zal worden gekoppeld aan jouw hosting.

Als je een instantie gebruikt die door iemand anders wordt beheerd, moet je het privacybeleid van die specifieke instantie lezen. Ze kunnen door hun eigenaren worden gewijzigd en kunnen daarom niet in overeenstemming zijn met het standaardbeleid. Some instances have [Tor](tor.md) .onion addresses which may grant some privacy as long as your search queries don't contain PII.

## TikTok

### ProxiTok

<div class="admonition recommendation" markdown>

![ProxiTok logo](assets/img/frontends/proxitok.svg){ align=right }

**ProxiTok** is an open-source frontend to the [TikTok](https://www.tiktok.com) website that is also self-hostable.

There are a number of public instances, with some instances having [Tor](tor.md) onion services support.

[:octicons-repo-16: Repository](https://github.com/pablouser1/ProxiTok){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/pablouser1/ProxiTok/wiki/Public-instances){ .card-link title="Public Instances"}
[:octicons-info-16:](https://github.com/pablouser1/ProxiTok/wiki){ .card-link title=Documentatie}
[:octicons-code-16:](https://github.com/pablouser1/ProxiTok){ .card-link title="Broncode" }

</details>

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

ProxiTok is useful if you want to disable JavaScript in your browser, such as [Tor Browser](tor.md#tor-browser) on the Safest security level.

</div>

## YouTube

### FreeTube

<div class="admonition recommendation" markdown>

![FreeTube logo](assets/img/frontends/freetube.svg){ align=right }

**FreeTube** is een gratis en open-source desktop applicatie voor [YouTube](https://youtube.com). Bij gebruik van FreeTube worden je abonnementenlijst en afspeellijsten lokaal op je toestel opgeslagen.

Standaard blokkeert FreeTube alle YouTube-advertenties. Bovendien integreert FreeTube optioneel met [SponsorBlock](https://sponsor.ajay.app) om u te helpen gesponsorde videosegmenten over te slaan.

[:octicons-home-16: Homepage](https://freetubeapp.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://freetubeapp.io/privacy.php){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.freetubeapp.io/){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/FreeTubeApp/FreeTube){ .card-link title="Source Code" }
[:octicons-heart-16:](https://liberapay.com/FreeTube){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://freetubeapp.io/#download)
- [:simple-apple: macOS](https://freetubeapp.io/#download)
- [:simple-linux: Linux](https://freetubeapp.io/#download)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/io.freetubeapp.FreeTube)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

Als je FreeTube gebruikt, kan je IP-adres nog steeds bekend zijn bij YouTube, [Invidious](https://instances.invidious.io) of [SponsorBlock](https://sponsor.ajay.app/), afhankelijk van je configuratie. Consider using a [VPN](vpn.md) or [Tor](tor.md) if your [threat model](basics/threat-modeling.md) requires hiding your IP address.

</div>

### Yattee

<div class="admonition recommendation" markdown>

![Yattee logo](assets/img/frontends/yattee.svg){ align=right }

**Yattee** is een gratis en open-source privacy georiënteerde videospeler voor iOS, tvOS en macOS voor [YouTube](https://youtube.com). Wanneer je Yattee gebruikt, wordt je abonnementenlijst lokaal op je toestel opgeslagen.

Je zult een paar [extra stappen](https://gonzoknows.com/posts/Yattee/) moeten nemen voordat je Yattee kunt gebruiken om YouTube te kijken, vanwege beperkingen in de App Store.

[:octicons-home-16: Homepage](https://github.com/yattee/yattee){ .md-button .md-button--primary }
[:octicons-eye-16:](https://r.yattee.stream/docs/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/yattee/yattee/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/yattee/yattee){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/yattee/yattee/wiki/Donations){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-apple: App Store](https://apps.apple.com/us/app/yattee/id1595136629)
- [:simple-github: GitHub](https://github.com/yattee/yattee/releases)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

Wanneer je Yattee gebruikt, is jouw IP-adres mogelijk nog steeds bekend bij YouTube, [Invidious](https://instances.invidious.io), [Piped](https://github.com/TeamPiped/Piped/wiki/Instances) of [SponsorBlock](https://sponsor.ajay.app/), afhankelijk van jouw configuratie. Consider using a [VPN](vpn.md) or [Tor](tor.md) if your [threat model](basics/threat-modeling.md) requires hiding your IP address.

</div>

Yattee blokkeert standaard alle YouTube-advertenties. Bovendien integreert Yattee optioneel met [SponsorBlock](https://sponsor.ajay.app) om u te helpen gesponsorde videosegmenten over te slaan.

### LibreTube (Android)

<div class="admonition recommendation" markdown>

![LibreTube-logo](assets/img/frontends/libretube.svg#only-light){ align=right }
![LibreTube logo](assets/img/frontends/libretube-dark.svg#only-dark){ align=right }

**LibreTube** is een gratis en open-source Android applicatie voor [YouTube](https://youtube.com) die gebruik maakt van de [Piped](#piped) API.

Met LibreTube kunt u uw abonnementenlijst en afspeellijsten lokaal op uw Android-toestel opslaan, of in een account op uw Piped-instantie naar keuze, waardoor u er ook op andere toestellen naadloos toegang toe hebt.

[:octicons-home-16: Homepage](https://libre-tube.github.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/libre-tube/LibreTube#privacy-policy-and-disclaimer){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/libre-tube/LibreTube#readme){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/libre-tube/LibreTube){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/libre-tube/LibreTube/releases)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

Wanneer u LibreTube gebruikt, is uw IP-adres zichtbaar voor de door u gekozen instantie [Piped](https://github.com/TeamPiped/Piped/wiki/Instances) en/of [SponsorBlock](https://sponsor.ajay.app/), afhankelijk van uw configuratie. Consider using a [VPN](vpn.md) or [Tor](tor.md) if your [threat model](basics/threat-modeling.md) requires hiding your IP address.

</div>

LibreTube blokkeert standaard alle YouTube-advertenties. Bovendien gebruikt Libretube [SponsorBlock](https://sponsor.ajay.app) om u te helpen gesponsorde videosegmenten over te slaan. U kunt de soorten segmenten die SponsorBlock zal overslaan volledig configureren, of volledig uitschakelen. Er is ook een knop op de videospeler zelf om deze desgewenst voor een specifieke video uit te schakelen.

### NewPipe (Android)

<div class="admonition recommendation annotate" markdown>

![Newpipe logo](assets/img/frontends/newpipe.svg){ align=right }

**NewPipe** is een gratis en open-source Android applicatie voor [YouTube](https://youtube.com), [SoundCloud](https://soundcloud.com), [media.ccc.de](https://media.ccc.de), [Bandcamp](https://bandcamp.com), en [PeerTube](https://joinpeertube.org/) (1).

Uw abonnementenlijst en afspeellijsten worden lokaal op uw Android toestel opgeslagen.

[:octicons-home-16: Homepage](https://newpipe.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://newpipe.net/legal/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://teamnewpipe.github.io/documentation/){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/TeamNewPipe/NewPipe){ .card-link title="Source Code" }
[:octicons-heart-16:](https://newpipe.net/donate/){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/TeamNewPipe/NewPipe/releases)

</details>

</div>

1. De standaard instantie is [FramaTube](https://framatube.org/), maar er kunnen er meer worden toegevoegd via **Instellingen** → **Inhoud** → **PeerTube instanties**

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

Wanneer je NewPipe gebruikt, is jouw IP-adres zichtbaar voor de gebruikte videoproviders. Consider using a [VPN](vpn.md) or [Tor](tor.md) if your [threat model](basics/threat-modeling.md) requires hiding your IP address.

</div>

### Invidious

<div class="admonition recommendation" markdown>

![Invidious logo](assets/img/frontends/invidious.svg#only-light){ align=right }
![Invidious logo](assets/img/frontends/invidious-dark.svg#only-dark){ align=right }

**Invidious** is een gratis en open-source frontend voor [YouTube](https://youtube.com) dat ook zelf te hosten is.

There are a number of public instances, with some instances having [Tor](tor.md) onion services support.

[:octicons-home-16: Homepage](https://invidious.io){ .md-button .md-button--primary }
[:octicons-server-16:](https://instances.invidious.io){ .card-link title="Public Instances"}
[:octicons-info-16:](https://docs.invidious.io/){ .card-link title=Documentatie}
[:octicons-code-16:](https://github.com/iv-org/invidious){ .card-link title="Broncode" }
[:octicons-heart-16:](https://invidious.io/donate/){ .card-link title=Bijdragen }

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

Invidious proxied standaard geen videos. Videos watched through Invidious will still make direct connections to Google's servers (e.g. `googlevideo.com`); however, some instances support video proxying—simply enable *Proxy videos* within the instances' settings or add `&local=true` to the URL.

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Invidious is useful if you want to disable JavaScript in your browser, such as [Tor Browser](tor.md#tor-browser) on the Safest security level. Het biedt op zichzelf geen privacy, en wij raden niet aan in te loggen op een account.

</div>

### Piped

<div class="admonition recommendation" markdown>

![Piped logo](assets/img/frontends/piped.svg){ align=right }

**Piped** is een gratis en open-source frontend voor [YouTube](https://youtube.com) dat ook zelf te hosten is.

Piped vereist JavaScript om te kunnen functioneren en er zijn een aantal openbare instanties.

[:octicons-repo-16: Repository](https://github.com/TeamPiped/Piped){ .md-button .md-button--primary }
[:octicons-server-16:](https://piped.kavin.rocks/preferences#ddlInstanceSelection){ .card-link title="Public Instances"}
[:octicons-info-16:](https://piped-docs.kavin.rocks/){ .card-link title=Documentatie}
[:octicons-code-16:](https://github.com/TeamPiped/Piped){ .card-link title="Broncode" }
[:octicons-heart-16:](https://github.com/TeamPiped/Piped#donations){ .card-link title=Bijdragen }

</details>

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Piped is handig als je [SponsorBlock](https://sponsor.ajay.app) wilt gebruiken zonder een extensie te installeren of als je zonder account toegang wilt krijgen tot inhoud met leeftijdsbeperkingen. Het biedt op zichzelf geen privacy, en wij raden niet aan in te loggen op een account.

</div>

## Criteria

**Wij zijn niet verbonden aan de projecten die wij aanbevelen.** Naast [onze standaardcriteria](about/criteria.md)hebben wij een duidelijke reeks eisen ontwikkeld om objectieve aanbevelingen te kunnen doen. Wij stellen voor dat je jezelf vertrouwd maakt met deze lijst voordat je een project kiest, en jouw eigen onderzoek uitvoert om er zeker van te zijn dat je de juiste keuze maakt.

<div class="admonition example" markdown>
<p class="admonition-title">This section is new</p>

We werken aan het vaststellen van gedefinieerde criteria voor elk deel van onze site, en dit kan onderhevig zijn aan verandering. Als je vragen hebt over onze criteria, stel ze dan [op ons forum](https://discuss.privacyguides.net/latest) en neem niet aan dat we iets niet in overweging hebben genomen bij het opstellen van onze aanbevelingen als het hier niet vermeld staat. Er zijn veel factoren die worden overwogen en besproken wanneer wij een project aanbevelen, en het documenteren van elke factor is een werk in uitvoering.

</div>

Aanbevolen frontends...

- Moet open-source software zijn.
- Moet zelf te hosten zijn.
- Moet alle basisfuncties van de website beschikbaar stellen aan anonieme gebruikers.

We overwegen alleen frontends voor websites die...

- Normally only accessible with JavaScript enabled.
