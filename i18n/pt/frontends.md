---
title: "Interfaces"
icon: material/flip-to-front
description: These open-source frontends for various internet services allow you to access content without JavaScript or other annoyances.
cover: frontends.webp
---

Por vezes, os serviços tentam forçá-lo a criar uma conta, bloqueando o acesso a conteúdos com popups irritantes. Também podem não funcionar como pretendido se o JavaScript não for ativado. Estes frontends existem para permitir contornar estas restrições.

Se optar por auto-hospedar estes frontends, é importante que tenha outras pessoas a utilizar também a sua instância, para que se possa fazer integração. Deve ter cuidado com o local e a forma como aloja, uma vez que a utilização por outras pessoas estará associada ao seu alojamento.

Quando estiver a utilizar uma instância gerida por outra pessoa, certifique-se de que lê a política de privacidade dessa instância específica. Podem ser modificados pelos seus proprietários e, por conseguinte, podem não refletir a política predefinida. Some instances have [Tor](tor.md) .onion addresses which may grant some privacy as long as your search queries don't contain PII.

## Reddit

### Redlib

<div class="admonition recommendation" markdown>

![Redlib logo](assets/img/frontends/redlib.svg){ align=right }

**Redlib** is an open-source frontend to the [Reddit](https://reddit.com) website that is also self-hostable.

There are a number of public instances, with some instances having [Tor](tor.md) onion services support.

[:octicons-repo-16: Repository](https://github.com/redlib-org/redlib){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/redlib-org/redlib-instances/blob/main/instances.md){ .card-link title="Public Instances"}
[:octicons-info-16:](https://github.com/redlib-org/redlib?tab=readme-ov-file#table-of-contents){ .card-link title=Documentation}
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

There are a number of public instances, with some instances having [Tor](tor.md) onion services support.

[:octicons-repo-16: Repositório](https://github.com/pablouser1/ProxiTok){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/pablouser1/ProxiTok/wiki/Public-instances){ .card-link title="Instâncias Públicas"}
[:octicons-info-16:](https://github.com/pablouser1/ProxiTok/wiki){ .card-link title=Documentação}
[:octicons-code-16:](https://github.com/pablouser1/ProxiTok){ .card-link title="Código-fonte" }

</details>

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

ProxiTok is useful if you want to disable JavaScript in your browser, such as [Tor Browser](tor.md#tor-browser) on the Safest security level.

</div>

## YouTube

### FreeTube

<div class="admonition recommendation" markdown>

![Logótipo FreeTube](assets/img/frontends/freetube.svg){ align=right }

O **FreeTube** é uma aplicação de ambiente de trabalho gratuita e de código aberto para [YouTube](https://youtube.com). Quando utiliza o FreeTube, a sua lista de subscrições e listas de reprodução são guardadas localmente no seu dispositivo.

Por predefinição, o FreeTube bloqueia todos os anúncios do YouTube. Além disso, o FreeTube integra-se opcionalmente com [SponsorBlock](https://sponsor.ajay.app) para o ajudar a saltar segmentos de vídeo patrocinados.

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
<p class="admonition-title">Warning</p>

When using FreeTube, your IP address may still be known to YouTube, [Invidious](https://instances.invidious.io) or [SponsorBlock](https://sponsor.ajay.app) depending on your configuration. Consider using a [VPN](vpn.md) or [Tor](tor.md) if your [threat model](basics/threat-modeling.md) requires hiding your IP address.

</div>

### Yattee

<div class="admonition recommendation" markdown>

![Logótipo Yattee](assets/img/frontends/yattee.svg){ align=right }

O **Yattee** é um leitor de vídeos do [YouTube](https://youtube.com), gratuito e de código aberto, orientado para a privacidade, com versões para iOS, tvOS e macOS. Quando utiliza o Yattee, a sua lista de subscrições é guardada localmente no seu dispositivo.

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
<p class="admonition-title">Warning</p>

When using Yattee, your IP address may still be known to YouTube, [Invidious](https://instances.invidious.io), [Piped](https://github.com/TeamPiped/Piped/wiki/Instances) or [SponsorBlock](https://sponsor.ajay.app) depending on your configuration. Consider using a [VPN](vpn.md) or [Tor](tor.md) if your [threat model](basics/threat-modeling.md) requires hiding your IP address.

</div>

Por predefinição, o Yattee bloqueia todos os anúncios do YouTube. Além disso, o Yattee integra-se opcionalmente com [SponsorBlock](https://sponsor.ajay.app) para o ajudar a saltar segmentos de vídeo patrocinados.

### LibreTube (Android)

<div class="admonition recommendation" markdown>

![Logótipo LibreTube](assets/img/frontends/libretube.svg#only-light){ align=right }
![Logótipo LibreTube](assets/img/frontends/libretube-dark.svg#only-dark){ align=right }

O **LibreTube** é uma aplicação Android gratuita e de código aberto para [YouTube](https://youtube.com), que utiliza a API [Piped](#piped).

O LibreTube permite-lhe armazenar a sua lista de subscrição e listas de reprodução localmente no seu dispositivo Android, ou numa conta na sua instância de eleição do Piped, o que lhe permite aceder-lhes sem problemas também noutros dispositivos.

[:octicons-home-16: Homepage](https://libretube.dev){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/libre-tube/LibreTube/blob/master/PRIVACY_POLICY.md){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://libretube.dev/#faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/libre-tube/LibreTube){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/libre-tube/LibreTube#donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/libre-tube/LibreTube/releases)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

When using LibreTube, your IP address will be visible to the [Piped](https://github.com/TeamPiped/Piped/wiki/Instances) instance you choose and/or [SponsorBlock](https://sponsor.ajay.app) depending on your configuration. Consider using a [VPN](vpn.md) or [Tor](tor.md) if your [threat model](basics/threat-modeling.md) requires hiding your IP address.

</div>

Por defeito, o LibreTube bloqueia todos os anúncios do YouTube. Additionally, LibreTube uses [SponsorBlock](https://sponsor.ajay.app) to help you skip sponsored video segments. É possível configurar totalmente os tipos de segmentos que SponsorBlock irá ignorar ou desactivá-lo completamente. Existe também um botão no próprio leitor de vídeo para o desativar para um vídeo específico, se assim o desejar.

### NewPipe (Android)

<div class="admonition recommendation annotate" markdown>

![Newpipe logo](assets/img/frontends/newpipe.svg){ align=right }

**NewPipe** is a free and open-source Android application for [YouTube](https://youtube.com), [SoundCloud](https://soundcloud.com), [media.ccc.de](https://media.ccc.de), [Bandcamp](https://bandcamp.com), and [PeerTube](https://joinpeertube.org) (1).

A sua lista de subscrição e listas de reprodução são guardadas localmente no seu dispositivo Android.

[:octicons-home-16: Homepage](https://newpipe.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://newpipe.net/legal/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://newpipe.net/FAQ){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/TeamNewPipe/NewPipe){ .card-link title="Source Code" }
[:octicons-heart-16:](https://newpipe.net/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/TeamNewPipe/NewPipe/releases)

</details>

</div>

1. The default instance is [FramaTube](https://framatube.org), however more can be added via **Settings** → **Content** → **PeerTube instances**

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

Ao utilizar o NewPipe, o seu endereço IP será visível para os fornecedores de vídeo utilizados. Consider using a [VPN](vpn.md) or [Tor](tor.md) if your [threat model](basics/threat-modeling.md) requires hiding your IP address.

</div>

### Invidious

<div class="admonition recommendation" markdown>

![Logótipo Invidious](assets/img/frontends/invidious.svg#only-light){ align=right }
![Logótipo Invidious](assets/img/frontends/invidious-dark.svg#only-dark){ align=right }

O **Invidious** é um frontend gratuito e de código aberto para [YouTube](https://youtube.com), que também é auto-hospedável.

There are a number of public instances, with some instances having [Tor](tor.md) onion services support.

[:octicons-home-16: Homepage](https://invidious.io){ .md-button .md-button--primary }
[:octicons-server-16:](https://instances.invidious.io){ .card-link title="Public Instances"}
[:octicons-info-16:](https://docs.invidious.io){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/iv-org/invidious){ .card-link title="Source Code" }
[:octicons-heart-16:](https://invidious.io/donate){ .card-link title=Contribute }

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

O Invidious não faz proxy de fluxos de vídeo por predefinição. Videos watched through Invidious will still make direct connections to Google's servers (e.g. `googlevideo.com`); however, some instances support video proxying—simply enable *Proxy videos* within the instances' settings or add `&local=true` to the URL.

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Invidious is useful if you want to disable JavaScript in your browser, such as [Tor Browser](tor.md#tor-browser) on the Safest security level. Não proporciona privacidade por si só e não recomendamos que inicie sessão em conta alguma.

</div>

### Piped

<div class="admonition recommendation" markdown>

![Logótipo Piped](assets/img/frontends/piped.svg){ align=right }

O **Piped** é um frontend gratuito e de código aberto para [YouTube](https://youtube.com), que também é auto-hospedável.

O Piped requer JavaScript para funcionar e existem várias instâncias públicas.

[:octicons-repo-16: Repository](https://github.com/TeamPiped/Piped){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/TeamPiped/Piped/wiki/Instances){ .card-link title="Public Instances"}
[:octicons-info-16:](https://docs.piped.video/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/TeamPiped/Piped){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/TeamPiped/Piped#donations){ .card-link title=Contribute }

</details>

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

O Piped é útil se pretender utilizar [SponsorBlock](https://sponsor.ajay.app) sem instalar uma extensão ou para aceder a conteúdos com restrições de idade sem uma conta. Não proporciona privacidade por si só e não recomendamos que inicie sessão em conta alguma.

</div>

## Critérios

**Note que não estamos associados a nenhum dos projetos que recomendamos.** Para além dos [nossos critérios padrão](about/criteria.md), temos um conjunto claro de requisitos que nos permitem fornecer recomendações objetivas. Sugerimos que se familiarize com esta lista antes de optar por um projeto e que desenvolva a sua própria investigação para garantir que se trata da escolha certa para si.

Frontends recomendados...

- O software deve ser de código aberto.
- Deve ser auto-hospedável.
- Deve fornecer todas as funcionalidades básicas do site disponíveis para utilizadores anónimos.

We only consider frontends if one of the following is true for a platform:

- Normally only accessible with JavaScript enabled.
- Normally only accessible with an account.
- Blocks access from commercial [VPNs](vpn.md).
