---
title: "Фронтенды"
icon: material/flip-to-front
description: These open-source frontends for various internet services allow you to access content without JavaScript or other annoyances.
cover: frontends.webp
---

Иногда сервисы пытаются заставить вас создать аккаунт, блокируя доступ к контенту с помощью назойливых всплывающих окон. Они также могут не работать без включенного JavaScript. Эти фронтенды могут позволить вам обойти эти ограничения.

Если вы решите самостоятельно хостить эти фронтенды, важно, чтобы вашим экземпляром пользовались и другие люди, чтобы вашу активность нельзя было отследить. Вы должны быть осторожны с тем, где и как вы размещаете хостинг, поскольку активность других людей будет связана с вашим хостингом.

Если вы используете чей-то экземпляр, обязательно ознакомьтесь с политикой конфиденциальности этого конкретного экземпляра. Они могут быть изменены их владельцами и поэтому могут не отражать политику по умолчанию. Some instances have [Tor](tor.md) .onion addresses which may grant some privacy as long as your search queries don't contain PII.

## TikTok

### ProxiTok

<div class="admonition recommendation" markdown>

![ProxiTok logo](assets/img/frontends/proxitok.svg){ align=right }

**ProxiTok** is an open-source frontend to the [TikTok](https://tiktok.com) website that is also self-hostable.

There are a number of public instances, with some instances having [Tor](tor.md) onion services support.

[:octicons-repo-16: Репозиторий](https://github.com/pablouser1/ProxiTok){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/pablouser1/ProxiTok/wiki/Public-instances){ .card-link title="Публичный экземпляр"}
[:octicons-info-16:](https://github.com/pablouser1/ProxiTok/wiki){ .card-link title=Документация}
[:octicons-code-16:](https://github.com/pablouser1/ProxiTok){ .card-link title="Исходный код" }

</details>

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

ProxiTok is useful if you want to disable JavaScript in your browser, such as [Tor Browser](tor.md#tor-browser) on the Safest security level.

</div>

## YouTube

### FreeTube

<div class="admonition recommendation" markdown>

![Логотип FreeTube](assets/img/frontends/freetube.svg){ align=right }

**FreeTube** - это бесплатное настольное приложение с открытым исходным кодом для [YouTube](https://youtube.com). Когда вы используете FreeTube, ваш список подписок и плейлисты сохранены локально на вашем устройстве.

По умолчанию FreeTube блокирует всю рекламу YouTube. Кроме того, FreeTube опционально интегрируется с [SponsorBlock](https://sponsor.ajay.app), чтобы помочь вам пропускать спонсируемые сегменты видео.

[:octicons-home-16: Homepage](https://freetubeapp.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://freetubeapp.io/privacy.php){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://docs.freetubeapp.io){ .card-link title=Documentation}
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
<p class="admonition-title">Предупреждение</p>

When using FreeTube, your IP address may still be known to YouTube, [Invidious](https://instances.invidious.io) or [SponsorBlock](https://sponsor.ajay.app) depending on your configuration. Consider using a [VPN](vpn.md) or [Tor](tor.md) if your [threat model](basics/threat-modeling.md) requires hiding your IP address.

</div>

### Yattee

<div class="admonition recommendation" markdown>

![Логотип Yattee](assets/img/frontends/yattee.svg){ align=right }

**Yattee** - это бесплатный, ориентированный на конфиденциальность видеоплеер с открытым исходным кодом для iOS, tvOS и macOS для [YouTube](https://youtube.com). При использовании Yattee список подписок сохраняется локально на вашем устройстве.

You will need to take a few [extra steps](https://gonzoknows.com/posts/Yattee) before you can use Yattee to watch YouTube, due to App Store restrictions.

[:octicons-home-16: Homepage](https://github.com/yattee/yattee){ .md-button .md-button--primary }
[:octicons-eye-16:](https://r.yattee.stream/docs/privacy.html){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/yattee/yattee/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/yattee/yattee){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/yattee/yattee/wiki/Donations){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-apple: App Store](https://apps.apple.com/app/id1595136629)
- [:simple-github: GitHub](https://github.com/yattee/yattee/releases)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Предупреждение</p>

When using Yattee, your IP address may still be known to YouTube, [Invidious](https://instances.invidious.io), [Piped](https://github.com/TeamPiped/Piped/wiki/Instances) or [SponsorBlock](https://sponsor.ajay.app) depending on your configuration. Consider using a [VPN](vpn.md) or [Tor](tor.md) if your [threat model](basics/threat-modeling.md) requires hiding your IP address.

</div>

По умолчанию Yattee блокирует всю рекламу на YouTube. Кроме того, Yattee опционально интегрируется с [SponsorBlock](https://sponsor.ajay.app), чтобы помочь вам пропускать спонсируемые сегменты видео.

### LibreTube (Android)

<div class="admonition recommendation" markdown>

![Логотип LibreTube](assets/img/frontends/libretube.svg#only-light){ align=right }
![Логотип LibreTube](assets/img/frontends/libretube-dark.svg#only-dark){ align=right }

**LibreTube** - это бесплатное приложение для Android с открытым исходным кодом для доступа к [YouTube](https://youtube.com), которое использует API [Piped](#piped).

LibreTube позволяет хранить список подписок и плейлисты локально на устройстве Android или в учетной записи на выбранном вами экземпляре Piped, что дает возможность беспрепятственного доступа к ним и на других устройствах.

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
<p class="admonition-title">Предупреждение</p>

When using LibreTube, your IP address will be visible to the [Piped](https://github.com/TeamPiped/Piped/wiki/Instances) instance you choose and/or [SponsorBlock](https://sponsor.ajay.app) depending on your configuration. Consider using a [VPN](vpn.md) or [Tor](tor.md) if your [threat model](basics/threat-modeling.md) requires hiding your IP address.

</div>

По умолчанию LibreTube блокирует всю рекламу YouTube. Кроме того, Libretube использует [SponsorBlock](https://sponsor.ajay.app), чтобы помочь вам пропускать спонсируемые сегменты видео. Вы можете полностью настроить типы сегментов, которые SponsorBlock будет пропускать, или полностью отключить его. На самом видеоплеере также есть кнопка, позволяющая при желании отключить его для конкретного видео.

### NewPipe (Android)

<div class="admonition recommendation annotate" markdown>

![Newpipe logo](assets/img/frontends/newpipe.svg){ align=right }

**NewPipe** is a free and open-source Android application for [YouTube](https://youtube.com), [SoundCloud](https://soundcloud.com), [media.ccc.de](https://media.ccc.de), [Bandcamp](https://bandcamp.com), and [PeerTube](https://joinpeertube.org) (1).

Список подписок и плейлисты сохраняются локально на вашем устройстве Android.

[:octicons-home-16: Homepage](https://newpipe.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://newpipe.net/legal/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://teamnewpipe.github.io/documentation){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/TeamNewPipe/NewPipe){ .card-link title="Source Code" }
[:octicons-heart-16:](https://newpipe.net/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/TeamNewPipe/NewPipe/releases)

</details>

</div>

1. The default instance is [FramaTube](https://framatube.org), however more can be added via **Settings** → **Content** → **PeerTube instances**

<div class="admonition warning" markdown>
<p class="admonition-title">Предупреждение</p>

При использовании NewPipe ваш IP-адрес будет виден используемым видеопровайдерам. Consider using a [VPN](vpn.md) or [Tor](tor.md) if your [threat model](basics/threat-modeling.md) requires hiding your IP address.

</div>

### Invidious

<div class="admonition recommendation" markdown>

![Логотип Invidious](assets/img/frontends/invidious.svg#only-light){ align=right }
![Логотип Invidious](assets/img/frontends/invidious-dark.svg#only-dark){ align=right }

**Invidious** - это бесплатный фронтенд с открытым исходным кодом для [YouTube](https://youtube.com), который можно самостоятельно хостить.

There are a number of public instances, with some instances having [Tor](tor.md) onion services support.

[:octicons-home-16: Homepage](https://invidious.io){ .md-button .md-button--primary }
[:octicons-server-16:](https://instances.invidious.io){ .card-link title="Public Instances"}
[:octicons-info-16:](https://docs.invidious.io){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/iv-org/invidious){ .card-link title="Source Code" }
[:octicons-heart-16:](https://invidious.io/donate){ .card-link title=Contribute }

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
[:octicons-server-16:](https://piped.kavin.rocks/preferences#ddlInstanceSelection){ .card-link title="Public Instances"}
[:octicons-info-16:](https://piped-docs.kavin.rocks){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/TeamPiped/Piped){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/TeamPiped/Piped#donations){ .card-link title=Contribute }

</details>

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Piped полезен, если вы хотите использовать [SponsorBlock](https://sponsor.ajay.app) без установки расширения или получить доступ к контенту с возрастными ограничениями без учетной записи. Сам по себе он не обеспечивает конфиденциальности, и мы не рекомендуем входить в какие-либо учетные записи.

</div>

## Критерии

**Обрати внимание, что у нас нет связей ни с одним проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Перед тем, как вы решите выбрать какой-либо проект, мы рекомендуем вам ознакомиться со списком критериев и провести собственное исследование, чтобы убедиться в правильности своего выбора.

Рекомендованные фронтенды...

- Должны иметь открытый исходный код.
- Должны иметь возможность самостоятельного хостинга.
- Должны предоставлять все основные функции сайта анонимным пользователям.

Мы рассматриваем фронтенды только для сайтов, которые...

- Normally only accessible with JavaScript enabled.
