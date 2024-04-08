---
title: "Interfaces de usuario"
icon: material/flip-to-front
description: Estas interfaces de código abierto para varios servicios de Internet, te permiten acceder al contenido sin JavaScript u otras molestias.
cover: frontends.webp
---

A veces, los servicios intentarán obligarle a registrarse mediante el bloqueo al acceso a los contenidos con molestas ventanas emergentes. También pueden fallar si no se activa JavaScript. Estas interfaces pueden permitirle eludir estas restricciones.

Si decides autoalojar, es importante que otras personas utilicen también tu instancia para que puedas pasar desapercibido. Debes tener cuidado con dónde y cómo alojas, ya que el uso de otras personas estará vinculado a tu alojamiento.

Cuando utilices una instancia gestionada por otra persona, asegúrate de leer la política de privacidad de esa instancia en específico. Pueden ser modificados por sus propietarios y, por lo tanto, pueden no reflejar la política por defecto. Algunas instancias tienen direcciones .onion de [Tor](tor.md) que pueden otorgar algo de privacidad mientras tus búsquedas no contengan PII (Información Personal Identificable).

## TikTok

### ProxiTok

<div class="admonition recommendation" markdown>

![ProxiTok logo](assets/img/frontends/proxitok.svg){ align=right }

**ProxiTok** es un frontend de código abierto para el sitio web [TikTok](https://tiktok.com) que también es autoalojable.

Existen varias instancias públicas, algunas de las cuales disponen de soporte para servicios onion [Tor](tor.md).

[:octicons-repo-16: Repositorio](https://github.com/pablouser1/ProxiTok){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/pablouser1/ProxiTok/wiki/Public-instances){ .card-link title="Instancias Públicas"}
[:octicons-info-16:](https://github.com/pablouser1/ProxiTok/wiki){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/pablouser1/ProxiTok){ .card-link title="Código Fuente" }

</details>

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Consejo</p>

ProxiTok es útil si quieres desactivar JavaScript en tu navegador, como [Tor Browser](tor.md#tor-browser) en el nivel de seguridad Más Seguro.

</div>

## YouTube

### FreeTube

<div class="admonition recommendation" markdown>

![FreeTube logo](assets/img/frontends/freetube.svg){ align=right }

**FreeTube** es una aplicación de escritorio gratuita y de código abierto para [YouTube](https://youtube.com). Al usar FreeTube, su lista de suscripciones y sus listas de reproducción se guardan localmente en su dispositivo.

Por defecto, FreeTube bloquea todos los anuncios de YouTube. Además, FreeTube se integra opcionalmente con [SponsorBlock](https://sponsor.ajay.app) para ayudarle a saltar segmentos de vídeo patrocinados.

[:octicons-home-16: Página Principal](https://freetubeapp.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://freetubeapp.io/privacy.php){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://docs.freetubeapp.io){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/FreeTubeApp/FreeTube){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://liberapay.com/FreeTube){ .card-link title=Contribuir }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-windows11: Windows](https://freetubeapp.io/#download)
- [:simple-apple: macOS](https://freetubeapp.io/#download)
- [:simple-linux: Linux](https://freetubeapp.io/#download)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/io.freetubeapp.FreeTube)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

Al utilizar FreeTube, tu dirección IP puede seguir siendo conocida por YouTube, [Invidious](https://instances.invidious.io), o [SponsorBlock](https://sponsor.ajay.app) dependiendo de tu configuración. Considera usar una [VPN](vpn.md) o [Tor](tor.md) si tu [modelo de amenaza](basics/threat-modeling.md) requiere ocultar tu dirección IP.

</div>

### Yattee

<div class="admonition recommendation" markdown>

![Yattee logo](assets/img/frontends/yattee.svg){ align=right }

**Yattee** es un reproductor de vídeo gratuito y de código abierto orientado a la privacidad para iOS, tvOS y macOS para [YouTube](https://youtube.com). Al usar Yattee, su lista de suscripciones se guarda localmente en su dispositivo.

Tendrás que seguir algunos [pasos adicionales](https://gonzoknows.com/posts/Yattee) antes de poder utilizar Yattee para ver YouTube, debido a las restricciones de la App Store.

[:octicons-home-16: Página Principal](https://github.com/yattee/yattee){ .md-button .md-button--primary }
[:octicons-eye-16:](https://r.yattee.stream/docs/privacy.html){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://github.com/yattee/yattee/wiki){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/yattee/yattee){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://github.com/yattee/yattee/wiki/Donations){ .card-link title=Contribuir }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-apple: App Store](https://apps.apple.com/app/id1595136629)
- [:simple-github: GitHub](https://github.com/yattee/yattee/releases)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

Al utilizar Yattee, tu dirección IP puede seguir siendo conocida por YouTube, [Invidious](https://instances.invidious.io), [Piped](https://github.com/TeamPiped/Piped/wiki/Instances) o [SponsorBlock](https://sponsor.ajay.app) dependiendo de tu configuración. Considera usar una [VPN](vpn.md) o [Tor](tor.md) si tu [modelo de amenaza](basics/threat-modeling.md) requiere ocultar tu dirección IP.

</div>

Por defecto, Yattee bloquea todos los anuncios de YouTube. Además, Yattee se integra opcionalmente con [SponsorBlock](https://sponsor.ajay.app) para ayudarle a saltar segmentos de vídeo patrocinados.

### LibreTube (Android)

<div class="admonition recommendation" markdown>

![LibreTube logo](assets/img/frontends/libretube.svg#only-light){ align=right }
![LibreTube logo](assets/img/frontends/libretube-dark.svg#only-dark){ align=right }

**LibreTube** es una aplicación Android gratuita y de código abierto para [YouTube](https://youtube.com) que utiliza la API [Piped](#piped).

LibreTube le permite almacenar su lista de suscripciones y listas de reproducción localmente en su dispositivo Android, o en una cuenta de su instancia de Piped preferida, lo que le permite acceder a ellas sin problemas desde otros dispositivos.

[:octicons-home-16: Homepage](https://libretube.dev){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/libre-tube/LibreTube/blob/master/PRIVACY_POLICY.md){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://libretube.dev/#faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/libre-tube/LibreTube){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/libre-tube/LibreTube#donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-github: GitHub](https://github.com/libre-tube/LibreTube/releases)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

Cuando uses LibreTube, tu dirección IP será visible para la instancia [Piped](https://github.com/TeamPiped/Piped/wiki/Instances) que elijas y/o [SponsorBlock](https://sponsor.ajay.app) dependiendo de tu configuración. Considera usar una [VPN](vpn.md) o [Tor](tor.md) si tu [modelo de amenaza](basics/threat-modeling.md) requiere ocultar tu dirección IP.

</div>

Por defecto, LibreTube bloquea todos los anuncios de YouTube. Additionally, LibreTube uses [SponsorBlock](https://sponsor.ajay.app) to help you skip sponsored video segments. Puede configurar completamente los tipos de segmentos que SponsorBlock omitirá, o desactivarlo por completo. También hay un botón en el propio reproductor de vídeo para desactivarlo para un vídeo específico si lo desea.

### NewPipe (Android)

<div class="admonition recommendation annotate" markdown>

![Newpipe logo](assets/img/frontends/newpipe.svg){ align=right }

**NewPipe** es una aplicación Android gratuita y de código abierto para [YouTube](https://youtube.com), [SoundCloud](https://soundcloud.com), [media.ccc.de](https://media.ccc.de), [Bandcamp](https://bandcamp.com) y [PeerTube](https://joinpeertube.org) (1).

Tu lista de suscripciones y tus listas de reproducción se guardan localmente en tu dispositivo Android.

[:octicons-home-16: Homepage](https://newpipe.net){ .md-button .md-button--primary }
[:octicons-eye-16:](https://newpipe.net/legal/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://newpipe.net/FAQ){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/TeamNewPipe/NewPipe){ .card-link title="Source Code" }
[:octicons-heart-16:](https://newpipe.net/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-github: GitHub](https://github.com/TeamNewPipe/NewPipe/releases)

</details>

</div>

1. La instancia por defecto es [FramaTube](https://framatube.org), sin embargo, se pueden añadir más a través de **Ajustes** → **Contenido** → **Instancias de PeerTube**

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

Al utilizar NewPipe, su dirección IP será visible para los proveedores de vídeo utilizados. Considera usar una [VPN](vpn.md) o [Tor](tor.md) si tu [modelo de amenaza](basics/threat-modeling.md) requiere ocultar tu dirección IP.

</div>

### Invidious

<div class="admonition recommendation" markdown>

![Invidious logo](assets/img/frontends/invidious.svg#only-light){ align=right }
![Invidious logo](assets/img/frontends/invidious-dark.svg#only-dark){ align=right }

**Invidious** es una interfaz gratuita y de código abierto para [YouTube](https://youtube.com) que además es autoalojable.

Existen varias instancias públicas, algunas de las cuales disponen de soporte para servicios onion [Tor](tor.md).

[:octicons-home-16: Página Principal](https://invidious.io){ .md-button .md-button--primary }
[:octicons-server-16:](https://instances.invidious.io){ .card-link title="Instancias Públicas"}
[:octicons-info-16:](https://docs.invidious.io){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/iv-org/invidious){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://invidious.io/donate){ .card-link title=Contribuir }

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

Invidious no proporciona un proxy para los vídeos por defecto. Los vídeos visualizados a través de Invidious seguirán estableciendo conexiones directas con los servidores de Google (por ejemplo, `googlevideo.com`); sin embargo, algunas instancias admiten el proxy de vídeo; basta con habilitar *Proxy videos* en la configuración de las instancias o añadir `&local=true` a la URL.

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Consejo</p>

Invidious es útil si deseas desactivar JavaScript en tu navegador, como [Tor Browser](tor.md#tor-browser) en el nivel de seguridad Más Seguro. No proporciona privacidad por sí mismo y no se recomienda entrar con ninguna cuenta.

</div>

### Piped

<div class="admonition recommendation" markdown>

![Piped logo](assets/img/frontends/piped.svg){ align=right }

**Piped** es una interfaz gratuita y de código abierto para [YouTube](https://youtube.com) que además es autoalojable.

Piped requiere JavaScript para funcionar y existen varias instancias públicas.

[:octicons-repo-16: Repository](https://github.com/TeamPiped/Piped){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/TeamPiped/Piped/wiki/Instances){ .card-link title="Public Instances"}
[:octicons-info-16:](https://docs.piped.video/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/TeamPiped/Piped){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/TeamPiped/Piped#donations){ .card-link title=Contribute }

</details>

</div>

<div class="admonition tip" markdown>
<p class="admonition-title">Consejo</p>

Piped es útil si desea utilizar [SponsorBlock](https://sponsor.ajay.app) sin instalar una extensión o acceder a contenidos restringidos por edad sin una cuenta. No proporciona privacidad por sí mismo y no se recomienda entrar con ninguna cuenta.

</div>

## Criterios

**Por favor, tenga en cuenta que no estamos afiliados con ninguno de los proyectos que recomendamos.** Además de [nuestros criterios estándar](about/criteria.md), hemos desarrollado un conjunto claro de requisitos que nos permiten ofrecer recomendaciones objetivas. Sugerimos que usted se familiarice con esta lista, antes de decidir utilizar un proyecto y realizar su propia investigación para asegurarse de que es la elección ideal para usted.

Las interfaces de usuario recomendadas...

- Deben ser software de código abierto.
- Deben ser autoalojables.
- Deben ofrecer todas las funciones básicas del sitio web a los usuarios anónimos.

Sólo consideramos interfcaes de usuario para sitios web que son...

- Normalmente solo accesibles con JavaScript activado.
