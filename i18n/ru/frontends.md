---
title: "Фронтенды"
icon: material/flip-to-front
description: These open-source frontends for various internet services allow you to access content without JavaScript or other annoyances.
cover: frontends.webp
---

<small>Защищает от следующих угроз:</small>

- [:material-account-cash: Капитализм слежки](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Иногда сервисы пытаются заставить вас создать аккаунт, блокируя доступ к контенту с помощью назойливых всплывающих окон. Они также могут не работать без включенного JavaScript. These frontends can allow you to circumvent these restrictions.

Если вы решите самостоятельно хостить эти фронтенды, важно, чтобы вашим экземпляром пользовались и другие люди, чтобы вашу активность нельзя было отследить. Вы должны быть осторожны с тем, где и как вы размещаете хостинг, поскольку активность других людей будет связана с вашим хостингом.

When you are using an instance run by someone else, make sure to read the privacy policy of that specific instance (if available). Они могут быть изменены их владельцами и поэтому могут не отражать политику по умолчанию. Some instances have [Tor](tor.md) .onion addresses, which may grant some privacy as long as your search queries don't contain personally identifiable information.

## Reddit

### Redlib

<div class="admonition recommendation" markdown>

![Redlib logo](assets/img/frontends/redlib.svg){ align=right }

**Redlib** is an open-source frontend to the [Reddit](https://reddit.com) website that is also self-hostable. You can access Redlib through a number of public instances.

[:octicons-repo-16: Repository](https://github.com/redlib-org/redlib){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/redlib-org/redlib-instances/blob/main/instances.md){ .card-link title="Public Instances" }
[:octicons-info-16:](https://github.com/redlib-org/redlib?tab=readme-ov-file#table-of-contents){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/redlib-org/redlib){ .card-link title="Source Code" }

</div>

<div class="admonition note" markdown>
<p class="admonition-title">Note</p>

The [Old Reddit](https://old.reddit.com) website doesn't require as much JavaScript as the new Reddit website does, but it has recently blocked access to IP addresses reserved for public VPNs. You can use Old Reddit in conjunction with the [Tor](tor.md) Onion that was [launched in October 2022](https://forum.torproject.org/t/reddit-onion-service-launch/5305) at [https://old.reddittorjg6rue252oqsxryoxengawnmo46qy4kyii5wtqnwfj4ooad.onion](https://old.reddittorjg6rue252oqsxryoxengawnmo46qy4kyii5wtqnwfj4ooad.onion).

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Redlib is useful if you want to disable JavaScript in your browser, such as [Tor Browser](tor.md#tor-browser) on the Safest security level.

</div>

## TikTok

### ProxiTok

<div class="admonition recommendation" markdown>

![ProxiTok logo](assets/img/frontends/proxitok.svg){ align=right }

**ProxiTok** is an open-source frontend to the [TikTok](https://tiktok.com) website that is also self-hostable.

There are a number of public instances, with some that offer a [Tor](tor.md) onion service or an [I2P](alternative-networks.md#i2p-the-invisible-internet-project) eepsite.

[:octicons-repo-16: Repository](https://github.com/pablouser1/ProxiTok){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/pablouser1/ProxiTok/wiki/Public-instances){ .card-link title="Public Instances" }
[:octicons-info-16:](https://github.com/pablouser1/ProxiTok/wiki){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/pablouser1/ProxiTok){ .card-link title="Source Code" }

</details>

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

ProxiTok is useful if you want to disable JavaScript in your browser, such as [Tor Browser](tor.md#tor-browser) on the Safest security level.

</div>

## YouTube

**Note:** YouTube has gradually rolled out changes to its video player and API that have thwarted some of the methods used by third-party frontends for extracting YouTube data. If you experience reliability issues with one YouTube frontend, consider trying out another that uses a different extraction method.

### Invidious

<div class="admonition recommendation" markdown>

![Логотип Invidious](assets/img/frontends/invidious.svg#only-light){ align=right }
![Логотип Invidious](assets/img/frontends/invidious-dark.svg#only-dark){ align=right }

**Invidious** - это бесплатный фронтенд с открытым исходным кодом для [YouTube](https://youtube.com), который можно самостоятельно хостить.

There are a number of public instances, with some that offer a [Tor](tor.md) onion service or an [I2P](alternative-networks.md#i2p-the-invisible-internet-project) eepsite.

[:octicons-home-16: Homepage](https://invidious.io){ .md-button .md-button--primary }
[:octicons-server-16:](https://docs.invidious.io/instances){ .card-link title="Public Instances" }
[:octicons-info-16:](https://docs.invidious.io){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/iv-org/invidious){ .card-link title="Source Code" }
[:octicons-heart-16:](https://invidious.io/donate){ .card-link title="Contribute" }

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Предупреждение</p>

По умолчанию Invidious не проксирует видеопотоки. Videos watched through Invidious will still make direct connections to Google's servers (e.g. `googlevideo.com`); however, some instances support video proxying—simply enable *Proxy videos* within the instances' settings or add `&local=true` to the URL.

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Invidious is useful if you want to disable JavaScript in your browser, such as [Tor Browser](tor.md#tor-browser) on the Safest security level. Сам по себе он не обеспечивает конфиденциальности, и мы не рекомендуем входить в какие-либо учетные записи.

</div>

### Piped

<div class="admonition recommendation" markdown>

![Логотип Piped](assets/img/frontends/piped.svg){ align=right }

**Piped** - это бесплатный фронтенд с открытым исходным кодом для [YouTube](https://youtube.com), который можно самостоятельно хостить.

Для работы Piped требуется JavaScript, и существует множество публичных экземпляров.

[:octicons-repo-16: Repository](https://github.com/TeamPiped/Piped){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/TeamPiped/documentation/blob/main/content/docs/public-instances/index.md){ .card-link title="Public Instances" }
[:octicons-info-16:](https://docs.piped.video/docs){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/TeamPiped/Piped){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/TeamPiped/Piped#donations){ .card-link title="Contribute" }

</details>

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Piped is useful if you want to use [SponsorBlock](https://sponsor.ajay.app) without installing an extension. Сам по себе он не обеспечивает конфиденциальности, и мы не рекомендуем входить в какие-либо учетные записи.

</div>

### FreeTube

<div class="admonition recommendation" markdown>

![Логотип FreeTube](assets/img/frontends/freetube.svg){ align=right }

**FreeTube** - это бесплатное настольное приложение с открытым исходным кодом для [YouTube](https://youtube.com). FreeTube extracts data from YouTube using its built-in API based on [YouTube.js](https://github.com/LuanRT/YouTube.js) or the [Invidious](#invidious) API. You can configure either as the default, with the other serving as a fallback.

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
<p class="admonition-title">Предупреждение</p>

When using FreeTube, your IP address may still be known to YouTube, [Invidious](https://instances.invidious.io), or [SponsorBlock](https://sponsor.ajay.app) depending on your configuration. Consider using a [VPN](vpn.md) or [Tor](tor.md) if your [threat model](basics/threat-modeling.md) requires hiding your IP address.

</div>

По умолчанию FreeTube блокирует всю рекламу YouTube. In addition, FreeTube optionally integrates with [SponsorBlock](https://sponsor.ajay.app) to help you skip sponsored video segments.

### LibreTube (Android)

<div class="admonition recommendation" markdown>

![Логотип LibreTube](assets/img/frontends/libretube.svg#only-light){ align=right }
![Логотип LibreTube](assets/img/frontends/libretube-dark.svg#only-dark){ align=right }

**LibreTube** - это бесплатное приложение для Android с открытым исходным кодом для доступа к [YouTube](https://youtube.com), которое использует API [Piped](#piped).

Список подписок и плейлисты сохраняются локально на вашем устройстве Android.

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
<p class="admonition-title">Предупреждение</p>

When using LibreTube, your IP address will be visible to YouTube, [Piped](https://github.com/TeamPiped/Piped/wiki/Instances), or [SponsorBlock](https://sponsor.ajay.app) depending on your configuration. Consider using a [VPN](vpn.md) or [Tor](tor.md) if your [threat model](basics/threat-modeling.md) requires hiding your IP address.

</div>

По умолчанию LibreTube блокирует всю рекламу YouTube. Additionally, LibreTube uses [SponsorBlock](https://sponsor.ajay.app) to help you skip sponsored video segments. Вы можете полностью настроить типы сегментов, которые SponsorBlock будет пропускать, или полностью отключить его. На самом видеоплеере также есть кнопка, позволяющая при желании отключить его для конкретного видео.

### NewPipe (Android)

<div class="admonition recommendation annotate" markdown>

![NewPipe logo](assets/img/frontends/newpipe.svg){ align=right }

**NewPipe** is a free and open-source Android application for [YouTube](https://youtube.com), [SoundCloud](https://soundcloud.com), [media.ccc.de](https://media.ccc.de), [Bandcamp](https://bandcamp.com), and [PeerTube](https://joinpeertube.org) (1).

Список подписок и плейлисты сохраняются локально на вашем устройстве Android.

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
<p class="admonition-title">Предупреждение</p>

При использовании NewPipe ваш IP-адрес будет виден используемым видеопровайдерам. Consider using a [VPN](vpn.md) or [Tor](tor.md) if your [threat model](basics/threat-modeling.md) requires hiding your IP address.

</div>

## Критерии

**Обрати внимание, что у нас нет связей ни с одним проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Перед тем, как вы решите выбрать какой-либо проект, мы рекомендуем вам ознакомиться со списком критериев и провести собственное исследование, чтобы убедиться в правильности своего выбора.

We only consider frontends if one of the following is true for a platform:

- Normally only accessible with JavaScript enabled.
- Normally only accessible with an account.
- Blocks access from commercial [VPNs](vpn.md).

Рекомендованные фронтенды...

- Должны иметь открытый исходный код.
- Должны иметь возможность самостоятельного хостинга.
- Должны предоставлять все основные функции сайта анонимным пользователям.
