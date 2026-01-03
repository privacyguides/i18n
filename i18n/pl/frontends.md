---
title: "Alternatywne interfejsy"
icon: material/flip-to-front
description: Te alternatywne interfejsy typu open source dla różnych usług internetowych umożliwiają dostęp do treści bez JavaScriptu i innych uciążliwości.
cover: frontends.webp
---

<small>Chroni przed następującymi zagrożeniami:</small>

- [:material-account-cash: Kapitalizm inwigilacji](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Czasami serwisy próbują wymusić założenie konta, blokując dostęp do treści natrętnymi wyskakującymi okienkami. Mogą one również przestać działać poprawnie bez włączonej obsługi JavaScriptu. Opisane tu interfejsy (ang. *frontends*) pozwalają na obejście tych ograniczeń.

Jeśli zdecydujesz się na samodzielne hostowanie tych interfejsów ważne jest, aby z Twojej instancji korzystały też inne osoby — dzięki temu łatwiej „wtopić się w tłum”. Należy zachować ostrożność przy wyborze miejsca i sposobu hostowania, ponieważ aktywność innych osób będzie powiązana z Twoim serwerem.

Korzystając z instancji należącej do kogoś innego, zapoznaj się z jej polityką prywatności (o ile jest dostępna). Właściciele mogą ją modyfikować, więc nie musi ona odzwierciedlać domyślnej polityki. Niektóre instancje posiadają adresy .onion w sieci [Tor](tor.md), co może zapewnić dodatkową prywatność pod warunkiem, że Twoje zapytania nie zawierają informacji umożliwiających identyfikację.

## Reddit

### Redlib

<div class="admonition recommendation" markdown>

![Logo Redlib](assets/img/frontends/redlib.svg){ align=right }

**Redlib** to interfejs open source dla serwisu [Reddit](https://reddit.com), który można również hostować samodzielnie. Dostęp do Redlib jest możliwy za pośrednictwem wielu instancji publicznych.

[:octicons-repo-16: Repozytorium](https://github.com/redlib-org/redlib){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/redlib-org/redlib-instances/blob/main/instances.md){ .card-link title="Instancje publiczne" }
[:octicons-info-16:](https://github.com/redlib-org/redlib?tab=readme-ov-file#table-of-contents){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/redlib-org/redlib){ .card-link title="Kod źródłowy" }

</div>

<div class="admonition note" markdown>
<p class="admonition-title">Uwaga</p>

Strona [Old Reddit](https://old.reddit.com) wymaga znacznie mniej JavaScriptu niż nowa wersja Reddita, jednak ostatnio zablokowano na niej dostęp dla adresów IP zarezerwowanych dla publicznych sieci VPN. Możesz korzystać z Old Reddit poprzez, [uruchomioną w październiku 2022 r.](https://forum.torproject.org/t/reddit-onion-service-launch/5305), usługę .onion w sieci [Tor](tor.md), pod adresem: [https://old.reddittorjg6rue252oqsxryoxengawnmo46qy4kyii5wtqnwfj4ooad.onion](https://old.reddittorjg6rue252oqsxryoxengawnmo46qy4kyii5wtqnwfj4ooad.onion).

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Porada</p>

Redlib jest przydatny, jeśli chcesz wyłączyć JavaScript w przeglądarce, takiej jak [Tor Browser](tor.md#tor-browser) przy ustawieniu „najbezpieczniejszego” poziomu bezpieczeństwa.

</div>

## TikTok

### ProxiTok

<div class="admonition recommendation" markdown>

![ProxiTok logo](assets/img/frontends/proxitok.svg){ align=right }

**ProxiTok** is an open-source frontend to the [TikTok](https://tiktok.com) website that is also self-hostable.

There are a number of public instances, with some that offer a [Tor](tor.md) onion service or an [I2P](alternative-networks.md#i2p-the-invisible-internet-project) eepsite.

[:octicons-repo-16: Repozytorium](https://github.com/pablouser1/ProxiTok){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/pablouser1/ProxiTok/wiki/Public-instances){ .card-link title="Instancje publiczne" }
[:octicons-info-16:](https://github.com/pablouser1/ProxiTok/wiki){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/pablouser1/ProxiTok){ .card-link title="Kod źródłowy" }

</details>

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Porada</p>

ProxiTok is useful if you want to disable JavaScript in your browser, such as [Tor Browser](tor.md#tor-browser) on the Safest security level.

</div>

## YouTube

**Note:** YouTube has gradually rolled out changes to its video player and API that have thwarted some of the methods used by third-party frontends for extracting YouTube data. If you experience reliability issues with one YouTube frontend, consider trying out another that uses a different extraction method.

### Invidious

<div class="admonition recommendation" markdown>

![Invidious logo](assets/img/frontends/invidious.svg#only-light){ align=right }
![Invidious logo](assets/img/frontends/invidious-dark.svg#only-dark){ align=right }

**Invidious** is a free and open-source frontend for [YouTube](https://youtube.com) that is also self-hostable.

There are a number of public instances, with some that offer a [Tor](tor.md) onion service or an [I2P](alternative-networks.md#i2p-the-invisible-internet-project) eepsite.

[:octicons-home-16: Homepage](https://invidious.io){ .md-button .md-button--primary }
[:octicons-server-16:](https://docs.invidious.io/instances){ .card-link title="Public Instances" }
[:octicons-info-16:](https://docs.invidious.io){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/iv-org/invidious){ .card-link title="Source Code" }
[:octicons-heart-16:](https://invidious.io/donate){ .card-link title="Contribute" }

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Ostrzeżenie</p>

Invidious does not proxy video streams by default. Videos watched through Invidious will still make direct connections to Google's servers (e.g. `googlevideo.com`); however, some instances support video proxying—simply enable *Proxy videos* within the instances' settings or add `&local=true` to the URL.

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Porada</p>

Invidious is useful if you want to disable JavaScript in your browser, such as [Tor Browser](tor.md#tor-browser) on the Safest security level. It does not provide privacy by itself, and we don’t recommend logging into any accounts.

</div>

### Piped

<div class="admonition recommendation" markdown>

![Piped logo](assets/img/frontends/piped.svg){ align=right }

**Piped** is a free and open-source frontend for [YouTube](https://youtube.com) that is also self-hostable.

Piped requires JavaScript in order to function and there are a number of public instances.

[:octicons-repo-16: Repository](https://github.com/TeamPiped/Piped){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/TeamPiped/documentation/blob/main/content/docs/public-instances/index.md){ .card-link title="Public Instances" }
[:octicons-info-16:](https://docs.piped.video/docs){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/TeamPiped/Piped){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/TeamPiped/Piped#donations){ .card-link title="Contribute" }

</details>

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Porada</p>

Piped is useful if you want to use [SponsorBlock](https://sponsor.ajay.app) without installing an extension. It does not provide privacy by itself, and we don’t recommend logging into any accounts.

</div>

### FreeTube

<div class="admonition recommendation" markdown>

![FreeTube logo](assets/img/frontends/freetube.svg){ align=right }

**FreeTube** is a free and open-source desktop application for [YouTube](https://youtube.com). FreeTube extracts data from YouTube using its built-in API based on [YouTube.js](https://github.com/LuanRT/YouTube.js) or the [Invidious](#invidious) API. You can configure either as the default, with the other serving as a fallback.

When using FreeTube, your subscription list, playlists, watch history and search history are saved locally on your device.

[:octicons-home-16: Homepage](https://freetubeapp.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://freetubeapp.io/privacy.php){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.freetubeapp.io){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/FreeTubeApp/FreeTube){ .card-link title="Source Code" }
[:octicons-heart-16:](https://liberapay.com/FreeTube){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://freetubeapp.io/#download)
- [:simple-apple: macOS](https://freetubeapp.io/#download)
- [:simple-linux: Linux](https://freetubeapp.io/#download)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/io.freetubeapp.FreeTube)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Ostrzeżenie</p>

When using FreeTube, your IP address may still be known to YouTube, [Invidious](https://instances.invidious.io), or [SponsorBlock](https://sponsor.ajay.app) depending on your configuration. Consider using a [VPN](vpn.md) or [Tor](tor.md) if your [threat model](basics/threat-modeling.md) requires hiding your IP address.

</div>

By default, FreeTube blocks all YouTube advertisements. In addition, FreeTube optionally integrates with [SponsorBlock](https://sponsor.ajay.app) to help you skip sponsored video segments.

### Yattee

<div class="admonition recommendation" markdown>

![Yattee logo](assets/img/frontends/yattee.svg){ align=right }

**Yattee** is a free and open-source privacy oriented video player for iOS, tvOS, and macOS for [YouTube](https://youtube.com). Due to App Store restrictions, you will need to take a few [extra steps](https://web.archive.org/web/20230330122839/https://gonzoknows.com/posts/Yattee) before you can use Yattee to watch YouTube. Yattee allows you to connect to instances of [Invidious](#invidious) or [Piped](#piped).

When using Yattee, your subscription list is saved locally on your device.

[:octicons-home-16: Homepage](https://github.com/yattee/yattee){ .md-button .md-button--primary }
[:octicons-eye-16:](https://r.yattee.stream/docs/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/yattee/yattee/wiki){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/yattee/yattee){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/yattee/yattee/wiki/Donations){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-apple: App Store](https://apps.apple.com/app/id1595136629)
- [:simple-github: GitHub](https://github.com/yattee/yattee/releases)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Ostrzeżenie</p>

When using Yattee, your IP address may still be known to YouTube, [Invidious](https://instances.invidious.io), [Piped](https://github.com/TeamPiped/Piped/wiki/Instances), or [SponsorBlock](https://sponsor.ajay.app) depending on your configuration. Consider using a [VPN](vpn.md) or [Tor](tor.md) if your [threat model](basics/threat-modeling.md) requires hiding your IP address.

</div>

By default, Yattee blocks all YouTube advertisements. In addition, Yattee optionally integrates with [SponsorBlock](https://sponsor.ajay.app) to help you skip sponsored video segments.

### LibreTube (Android)

<div class="admonition recommendation" markdown>

![LibreTube logo](assets/img/frontends/libretube.svg#only-light){ align=right }
![LibreTube logo](assets/img/frontends/libretube-dark.svg#only-dark){ align=right }

**LibreTube** is a free and open-source Android application for [YouTube](https://youtube.com) which uses the [Piped](#piped) API.

Your subscription list and playlists are saved locally on your Android device.

[:octicons-home-16: Homepage](https://libretube.dev){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/libre-tube/LibreTube/blob/master/PRIVACY_POLICY.md){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://libretube.dev/#faq){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/libre-tube/LibreTube){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/libre-tube/LibreTube#donate){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/libre-tube/LibreTube/releases)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Ostrzeżenie</p>

When using LibreTube, your IP address will be visible to YouTube, [Piped](https://github.com/TeamPiped/Piped/wiki/Instances), or [SponsorBlock](https://sponsor.ajay.app) depending on your configuration. Consider using a [VPN](vpn.md) or [Tor](tor.md) if your [threat model](basics/threat-modeling.md) requires hiding your IP address.

</div>

By default, LibreTube blocks all YouTube advertisements. Additionally, LibreTube uses [SponsorBlock](https://sponsor.ajay.app) to help you skip sponsored video segments. You are able to fully configure the types of segments that SponsorBlock will skip, or disable it completely. There is also a button on the video player itself to disable it for a specific video if desired.

### NewPipe (Android)

<div class="admonition recommendation annotate" markdown>

![NewPipe logo](assets/img/frontends/newpipe.svg){ align=right }

**NewPipe** is a free and open-source Android application for [YouTube](https://youtube.com), [SoundCloud](https://soundcloud.com), [media.ccc.de](https://media.ccc.de), [Bandcamp](https://bandcamp.com), and [PeerTube](https://joinpeertube.org) (1).

Your subscription list and playlists are saved locally on your Android device.

[:octicons-home-16: Homepage](https://newpipe.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://newpipe.net/legal/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://newpipe.net/FAQ){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/TeamNewPipe/NewPipe){ .card-link title="Source Code" }
[:octicons-heart-16:](https://newpipe.net/donate){ .card-link title="Contribute" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/TeamNewPipe/NewPipe/releases)

</details>

</div>

1. The default instance is [FramaTube](https://framatube.org), however more can be added via **Settings** → **Content** → **PeerTube instances**.

<div class="admonition warning" markdown>
<p class="admonition-title">Ostrzeżenie</p>

When using NewPipe, your IP address will be visible to the video providers used. Consider using a [VPN](vpn.md) or [Tor](tor.md) if your [threat model](basics/threat-modeling.md) requires hiding your IP address.

</div>

## Kryteria

**Należy pamiętać, że nie jesteśmy powiązani z żadnym z polecanych przez nas projektów.** Oprócz [naszych standardowych kryteriów](about/criteria.md) opracowaliśmy jasny zestaw wymagań, które pozwalają nam formułować obiektywne zalecenia. Sugerujemy zapoznanie się z tą listą przed wyborem projektu oraz przeprowadzenie własnych badań, aby upewnić się, że jest to odpowiedni wybór dla Ciebie.

We only consider frontends if one of the following is true for a platform:

- Normally only accessible with JavaScript enabled.
- Normally only accessible with an account.
- Blocks access from commercial [VPNs](vpn.md).

Recommended frontends...

- Musi być oprogramowaniem typu open source.
- Must be self-hostable.
- Must provide all basic website functionality available to anonymous users.
