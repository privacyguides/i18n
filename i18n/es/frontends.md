---
title: "Interfaces de usuario"
icon: material/flip-to-front
description: Estas interfaces de código abierto para diversos servicios de Internet le permiten acceder a los contenidos sin JavaScript ni otras molestias.
cover: frontends.webp
---

A veces, los servicios intentarán obligarle a registrarse mediante el bloqueo al acceso a los contenidos con molestas ventanas emergentes. También pueden fallar si no se activa JavaScript. Estas interfaces pueden permitirle eludir estas restricciones.

Si decides autoalojar, es importante que otras personas utilicen también tu instancia para que puedas pasar desapercibido. Debes tener cuidado con dónde y cómo alojas, ya que el uso de otras personas estará vinculado a tu alojamiento.

Cuando utilices una instancia gestionada por otra persona, asegúrate de leer la política de privacidad de esa instancia en específico. Pueden ser modificados por sus propietarios y, por lo tanto, pueden no reflejar la política por defecto. Algunas instancias tienen direcciones Tor .onion que pueden otorgar cierta privacidad siempre y cuando sus consultas de búsqueda no contengan PII (Información Personal Identificable).

## Twitter

### Nitter

!!! recommendation

    ![Nitter logo](assets/img/frontends/nitter.svg){ align=right }
    
    **Nitter** es una interfaz gratuita y de código abierto para [Twitter](https://twitter.com) que también es autoalojable.
    
    Existen varias instancias públicas, algunas de las cuales disponen de soporte para servicios onion [Tor](https://www.torproject.org).
    
    [:octicons-repo-16: Repositorio](https://github.com/zedeus/nitter){ .md-button .md-button--primary }
    [:octicons-server-16:](https://github.com/zedeus/nitter/wiki/Instances){ .card-link title="Instancias Públicas"}
    [:octicons-info-16:](https://github.com/zedeus/nitter/wiki){ .card-link title=Documentación}
    [:octicons-code-16:](https://github.com/zedeus/nitter){ .card-link title="Código Fuente" }
    [:octicons-heart-16:](https://github.com/zedeus/nitter#nitter){ .card-link title=Contribuir }

!!! tip "Consejo"

    Nitter es útil si quiere navegar por el contenido de Twitter sin tener que iniciar sesión y si quieres desactiva JavaScript en su navegador, como es el caso de [Tor Browser](https://www.torproject.org/) en el nivel de seguridad Más Seguro. También le permite [crear canales RSS para Twitter](news-aggregators.md#twitter).

## TikTok

### ProxiTok

!!! recommendation

    ![ProxiTok logo](assets/img/frontends/proxitok.svg){ align=right }
    
    **ProxiTok** is an open-source frontend to the [TikTok](https://www.tiktok.com) website that is also self-hostable.
    
    Existen varias instancias públicas, algunas de las cuales disponen de soporte para servicios onion [Tor](https://www.torproject.org).
    
    [:octicons-repo-16: Repositorio](https://github.com/pablouser1/ProxiTok){ .md-button .md-button--primary }
    [:octicons-server-16:](https://github.com/pablouser1/ProxiTok/wiki/Public-instances){ .card-link title="Instancias Públicas"}
    [:octicons-info-16:](https://github.com/pablouser1/ProxiTok/wiki){ .card-link title=Documentación}
    [:octicons-code-16:](https://github.com/pablouser1/ProxiTok){ .card-link title="Código Fuente" }

!!! tip "Consejo"

    PorxiTok es útil si quiere desactivar JavaScript en su navegador como en el navegador [Tor](https://www.torproject.org/) en la configuración de seguridad Más Segura.

## YouTube

### FreeTube

!!! recommendation

    ![FreeTube logo](assets/img/frontends/freetube.svg){ align=right }
    
    **FreeTube** es una aplicación de escritorio gratuita y de código abierto para [YouTube](https://youtube.com). Al usar FreeTube, su lista de suscripciones y sus listas de reproducción se guardan localmente en su dispositivo.
    
    Por defecto, FreeTube bloquea todos los anuncios de YouTube. Además, FreeTube se integra opcionalmente con [SponsorBlock](https://sponsor.ajay.app) para ayudarle a saltar segmentos de vídeo patrocinados.
    
    [:octicons-home-16: Página Principal](https://freetubeapp.io){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://freetubeapp.io/privacy.php){ .card-link title="Política de Privacidad" }
    [:octicons-info-16:](https://docs.freetubeapp.io/){ .card-link title=Documentación}
    [:octicons-code-16:](https://github.com/FreeTubeApp/FreeTube){ .card-link title="Código Fuente" }
    [:octicons-heart-16:](https://liberapay.com/FreeTube){ .card-link title=Contribuir }
    
    ??? downloads "Descargas"
    
        - [:simple-windows11: Windows](https://freetubeapp.io/#download)
        - [:simple-apple: macOS](https://freetubeapp.io/#download)
        - [:simple-linux: Linux](https://freetubeapp.io/#download)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/io.freetubeapp.FreeTube)

!!! warning "Advertencia"

    Al utilizar FreeTube, su dirección IP puede seguir siendo conocida por YouTube, [Invidious](https://instances.invidious.io), o [SponsorBlock](https://sponsor.ajay.app/) dependiendo de su configuración. Considere la posibilidad de utilizar una [VPN](vpn.md) o [Tor](https://www.torproject.org) si su [modelo de amenaza](basics/threat-modeling.md) requiere ocultar su dirección IP.

### Yattee

!!! recommendation

    ![Yattee logo](assets/img/frontends/yattee.svg){ align=right }
    
    **Yattee** es un reproductor de vídeo gratuito y de código abierto orientado a la privacidad para iOS, tvOS y macOS para [YouTube](https://youtube.com). Al usar Yattee, su lista de suscripciones se guarda localmente en su dispositivo.
    
    Necesitará realizar algunos [pasos adicionales](https://gonzoknows.com/posts/Yattee/) antes de poder usar Yattee para ver YouTube, debido a las restricciones de la App Store.
    
    [:octicons-home-16: Página Principal](https://github.com/yattee/yattee){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://r.yattee.stream/docs/privacy.html){ .card-link title="Política de Privacidad" }
    [:octicons-info-16:](https://github.com/yattee/yattee/wiki){ .card-link title=Documentación}
    [:octicons-code-16:](https://github.com/yattee/yattee){ .card-link title="Código Fuente" }
    [:octicons-heart-16:](https://github.com/yattee/yattee/wiki/Donations){ .card-link title=Contribuir }
    
    ??? downloads "Descargas"
    
        - [:simple-apple: App Store](https://apps.apple.com/us/app/yattee/id1595136629)
        - [:simple-github: GitHub](https://github.com/yattee/yattee/releases)

!!! warning "Advertencia"

    Al utilizar Yattee, su dirección IP puede seguir siendo conocida por YouTube, [Invidious](https://instances.invidious.io), [Piped](https://github.com/TeamPiped/Piped/wiki/Instances/) o [SponsorBlock](https://sponsor.ajay.app/) dependiendo de su configuración. Considere la posibilidad de utilizar una [VPN](vpn.md) o [Tor](https://www.torproject.org) si su [modelo de amenaza](basics/threat-modeling.md) requiere ocultar su dirección IP.

Por defecto, Yattee bloquea todos los anuncios de YouTube. Además, Yattee se integra opcionalmente con [SponsorBlock](https://sponsor.ajay.app) para ayudarle a saltar segmentos de vídeo patrocinados.

### LibreTube (Android)

!!! recommendation

    ![LibreTube logo](assets/img/frontends/libretube.svg#only-light){ align=right }
    ![LibreTube logo](assets/img/frontends/libretube-dark.svg#only-dark){ align=right }
    
    **LibreTube** es una aplicación Android gratuita y de código abierto para [YouTube](https://youtube.com) que utiliza la API [Piped](#piped).
    
    LibreTube le permite almacenar su lista de suscripciones y listas de reproducción localmente en su dispositivo Android, o en una cuenta de su instancia de Piped preferida, lo que le permite acceder a ellas sin problemas desde otros dispositivos.
    
    [:octicons-home-16: Página Principal](https://libre-tube.github.io){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://github.com/libre-tube/LibreTube#privacy-policy-and-disclaimer){ .card-link title="Política de Privacidad" }
    [:octicons-info-16:](https://github.com/libre-tube/LibreTube#readme){ .card-link title=Documentación}
    [:octicons-code-16:](https://github.com/libre-tube/LibreTube){ .card-link title="Código Fuente" }
    
    ??? downloads "Descargas"
    
        - [:simple-github: GitHub](https://github.com/libre-tube/LibreTube/releases)

!!! warning "Advertencia"

    Al usar LibreTube, su dirección IP será visible para la instancia [Piped](https://github.com/TeamPiped/Piped/wiki/Instances) que elija y/o [SponsorBlock](https://sponsor.ajay.app/) dependiendo de su configuración. Considere la posibilidad de utilizar una [VPN](vpn.md) o [Tor](https://www.torproject.org) si su [modelo de amenaza](basics/threat-modeling.md) requiere ocultar su dirección IP.

Por defecto, LibreTube bloquea todos los anuncios de YouTube. Además, Libretube utiliza [SponsorBlock](https://sponsor.ajay.app) para ayudarle a saltarse los segmentos de vídeo patrocinados. Puede configurar completamente los tipos de segmentos que SponsorBlock omitirá, o desactivarlo por completo. También hay un botón en el propio reproductor de vídeo para desactivarlo para un vídeo específico si lo desea.

### NewPipe (Android)

!!! recommendation annotate

    ![Newpipe logo](assets/img/frontends/newpipe.svg){ align=right }
    
    **NewPipe** es una aplicación Android gratuita y de código abierto para [YouTube](https://youtube.com), [SoundCloud](https://soundcloud.com), [media.ccc.de](https://media.ccc.de), [Bandcamp](https://bandcamp.com) y [PeerTube](https://joinpeertube.org/) (1).
    
    Su lista de suscripciones y sus listas de reproducción se guardan localmente en su dispositivo Android.
    
    [:octicons-home-16: Página Principal](https://newpipe.net){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://newpipe.net/legal/privacy){ .card-link title="Política de Privacidad" }
    [:octicons-info-16:](https://teamnewpipe.github.io/documentation/){ .card-link title=Contribuir}
    [:octicons-code-16:](https://github.com/TeamNewPipe/NewPipe){ .card-link title="Código Fuente" }
    [:octicons-heart-16:](https://newpipe.net/donate/){ .card-link title=Contribuir }
    
    ??? downloads "Descargas"
    
        - [:simple-github: GitHub](https://github.com/TeamNewPipe/NewPipe/releases)

1. La instancia por defecto es [FramaTube](https://framatube.org/), sin embargo, se pueden añadir más a través de **Ajustes** → **Contenido** → **Instancias de PeerTube**

!!! warning "Advertencia"

    Al utilizar NewPipe, su dirección IP será visible para los proveedores de vídeo utilizados. Considere la posibilidad de utilizar una [VPN](vpn.md) o [Tor](https://www.torproject.org) si su [modelo de amenaza](basics/threat-modeling.md) requiere ocultar su dirección IP.

### Invidious

!!! recommendation

    ![Invidious logo](assets/img/frontends/invidious.svg#only-light){ align=right }
    ![Invidious logo](assets/img/frontends/invidious-dark.svg#only-dark){ align=right }
    
    **Invidious** es una interfaz gratuita y de código abierto para [YouTube](https://youtube.com) que además es autoalojable.
    
    Existen varias instancias públicas, algunas de las cuales disponen de soporte para servicios onion [Tor](https://www.torproject.org).
    
    [:octicons-home-16: Página Principal](https://invidious.io){ .md-button .md-button--primary }
    [:octicons-server-16:](https://instances.invidious.io){ .card-link title="Instancias Públicas"}
    [:octicons-info-16:](https://docs.invidious.io/){ .card-link title=Documentación}
    [:octicons-code-16:](https://github.com/iv-org/invidious){ .card-link title="Código Fuente" }
    [:octicons-heart-16:](https://invidious.io/donate/){ .card-link title=Contribuir }

!!! warning "Advertencia"

    Invidious no proporciona un proxy para los vídeos por defecto. Los vídeos que se vean a través de Invidious seguirán realizando conexiones directas a los servidores de Google (ej. 'googlevideo.com'); sin embargo, algunas instancias admiten el proxy de vídeo; basta con habilitar *Proxy videos* en la configuración de las instancias o añadir `&local=true` a la URL.

!!! tip "Consejo"

    Invidious es útil si quiere desactivar JavaScript en su navegador como en el navegador [Tor](https://www.torproject.org/) en la configuración de seguridad Msás Segura. No proporciona privacidad por sí mismo y no se recomienda entrar con ninguna cuenta.

### Piped

!!! recommendation

    ![Piped logo](assets/img/frontends/piped.svg){ align=right }
    
    **Piped** es una interfaz gratuita y de código abierto para [YouTube](https://youtube.com) que además es autoalojable.
    
    Piped requiere JavaScript para funcionar y existen varias instancias públicas.
    
    [:octicons-repo-16: Repositorio](https://github.com/TeamPiped/Piped){ .md-button .md-button--primary }
    [:octicons-server-16:](https://piped.kavin.rocks/preferences#ddlInstanceSelection){ .card-link title="Instancias Públicas"}
    [:octicons-info-16:](https://piped-docs.kavin.rocks/){ .card-link title=Documentación}
    [:octicons-code-16:](https://github.com/TeamPiped/Piped){ .card-link title="Código Fuente" }
    [:octicons-heart-16:](https://github.com/TeamPiped/Piped#donations){ .card-link title=Contribuir }

!!! tip "Consejo"

    Piped es útil si desea utilizar [SponsorBlock](https://sponsor.ajay.app) sin instalar una extensión o acceder a contenidos restringidos por edad sin una cuenta. No proporciona privacidad por sí mismo y no se recomienda entrar con ninguna cuenta.

## Criterios

**Por favor, tenga en cuenta que no estamos afiliados con ninguno de los proyectos que recomendamos.** Además de [nuestros criterios estándar](about/criteria.md), hemos desarrollado un conjunto claro de requisitos que nos permiten ofrecer recomendaciones objetivas. Sugerimos que usted se familiarice con esta lista, antes de decidir utilizar un proyecto y realizar su propia investigación para asegurarse de que es la elección ideal para usted.

!!! example "Esta sección es nueva"

    Estamos trabajando en establecer criterios definidos para cada sección de nuestra página, y esto puede estar sujeto a cambios. Si tiene alguna duda sobre nuestros criterios, por favor [pregunte en nuestro foro](https://discuss.privacyguides.net/latest) y no asuma que no hemos tenido en cuenta algo a la hora de hacer nuestras recomendaciones si no aparece aquí. Son muchos los factores que se tienen en cuenta y se debaten cuando recomendamos un proyecto, y documentar cada uno de ellos es un trabajo en curso.

Las interfaces de usuario recomendadas...

- Deben ser software de código abierto.
- Deben ser autoalojables.
- Deben ofrecer todas las funciones básicas del sitio web a los usuarios anónimos.

Sólo consideramos interfcaes de usuario para sitios web que...

- Normalmente no son accesibles sin JavaScript.
