---
title: "Frontends"
icon: material/flip-to-front
description: Estes frontends de código aberto para vários serviços da Internet permitem-lhe aceder a conteúdos sem JavaScript ou outro tipo de inconvenientes.
cover: frontends.webp
---

Por vezes, os serviços tentam forçá-lo a criar uma conta, bloqueando o acesso a conteúdos com popups irritantes. Também podem não funcionar como pretendido se o JavaScript não for ativado. Estes frontends existem para permitir contornar estas restrições.

Se optar por auto-hospedar estes frontends, é importante que tenha outras pessoas a utilizar também a sua instância, para que se possa fazer integração. Deve ter cuidado com o local e a forma como aloja, uma vez que a utilização por outras pessoas estará associada ao seu alojamento.

Quando estiver a utilizar uma instância gerida por outra pessoa, certifique-se de que lê a política de privacidade dessa instância específica. Podem ser modificados pelos seus proprietários e, por conseguinte, podem não refletir a política predefinida. Algumas instâncias possuem endereços Tor .onion que podem garantir alguma privacidade, desde que as suas consultas de pesquisa não contenham informações pessoais.

## Twitter

### Nitter

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo Nitter](assets/img/frontends/nitter.svg){ align=right }
    
    O **Nitter** é um frontend gratuito e de código aberto para [Twitter](https://twitter.com) que também é auto-hospedável.
    
    Existem várias instâncias públicas, sendo que algumas instâncias têm suporte para serviços onion [Tor](https://www.torproject.org).
    
    [:octicons-repo-16: Repositório](https://github.com/zedeus/nitter){ .md-button .md-button--primary }
    [:octicons-server-16:](https://github.com/zedeus/nitter/wiki/Instances){ .card-link title="Instâncias Públicas"}
    [:octicons-info-16:](https://github.com/zedeus/nitter/wiki){ .card-link title=Documentação}
    [:octicons-code-16:](https://github.com/zedeus/nitter){ .card-link title="Código-fonte" }
    [:octicons-heart-16:](https://github.com/zedeus/nitter#nitter){ .card-link title=Contribuir }

!!! dica

    O Nitter é útil se pretender navegar no conteúdo do Twitter sem ter de iniciar sessão e se pretender desativar o JavaScript no seu browser, como é o caso do [Tor Browser](https://www.torproject.org/) no nível de segurança Mais seguro. Também lhe permite [criar feeds RSS para o Twitter] (news-aggregators.md#twitter).

## TikTok

### ProxiTok

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![ProxiTok logo](assets/img/frontends/proxitok.svg){ align=right }
    
    **ProxiTok** is an open-source frontend to the [TikTok](https://www.tiktok.com) website that is also self-hostable.
    
    Existem várias instâncias públicas, sendo que algumas instâncias têm suporte para serviços onion [Tor](https://www.torproject.org).
    
    [:octicons-repo-16: Repositório](https://github.com/pablouser1/ProxiTok){ .md-button .md-button--primary }
    [:octicons-server-16:](https://github.com/pablouser1/ProxiTok/wiki/Public-instances){ .card-link title="Instâncias Públicas"}
    [:octicons-info-16:](https://github.com/pablouser1/ProxiTok/wiki){ .card-link title=Documentação}
    [:octicons-code-16:](https://github.com/pablouser1/ProxiTok){ .card-link title="Código-fonte" }

!!! dica

    O ProxiTok é útil se quiser desativar o JavaScript no seu browser, tal como o [Tor Browser](https://www.torproject.org/) no nível de segurança Mais seguro.

## YouTube

### FreeTube

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo FreeTube](assets/img/frontends/freetube.svg){ align=right }
    
    O **FreeTube** é uma aplicação de ambiente de trabalho gratuita e de código aberto para [YouTube](https://youtube.com). Quando utiliza o FreeTube, a sua lista de subscrições e listas de reprodução são guardadas localmente no seu dispositivo.
    
    Por predefinição, o FreeTube bloqueia todos os anúncios do YouTube. Além disso, o FreeTube integra-se opcionalmente com [SponsorBlock](https://sponsor.ajay.app) para o ajudar a saltar segmentos de vídeo patrocinados.
    
    [:octicons-home-16: Homepage](https://freetubeapp.io){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://freetubeapp.io/privacy.php){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://docs.freetubeapp.io/){ .card-link title=Documentação}
    [:octicons-code-16:](https://github.com/FreeTubeApp/FreeTube){ .card-link title="Código-fonte" }
    [:octicons-heart-16:](https://liberapay.com/FreeTube){ .card-link title=Contribuir }
    
    ??? downloads
    
        - [:simple-windows11: Windows](https://freetubeapp.io/#download)
        - [:simple-apple: macOS](https://freetubeapp.io/#download)
        - [:simple-linux: Linux](https://freetubeapp.io/#download)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/io.freetubeapp.FreeTube)

!!! aviso

    Ao utilizar o FreeTube, o seu endereço IP pode ainda ser do conhecimento do YouTube, [Invidious](https://instances.invidious.io) ou [SponsorBlock](https://sponsor.ajay.app/), dependendo da sua configuração. Considere a utilização de uma [VPN](vpn.md) ou [Tor](https://www.torproject.org) se o seu [modelo de ameaça](basics/threat-modeling.md) exigir a ocultação do seu endereço IP.

### Yattee

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo Yattee](assets/img/frontends/yattee.svg){ align=right }
    
    O **Yattee** é um leitor de vídeos do [YouTube](https://youtube.com), gratuito e de código aberto, orientado para a privacidade, com versões para iOS, tvOS e macOS. Quando utiliza o Yattee, a sua lista de subscrições é guardada localmente no seu dispositivo.
    
    Terá de efetuar alguns [passos extra] (https://gonzoknows.com/posts/Yattee/) antes de poder utilizar o Yattee para ver o YouTube, devido a restrições da App Store.
    
    [:octicons-home-16: Homepage](https://github.com/yattee/yattee){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://r.yattee.stream/docs/privacy.html){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://github.com/yattee/yattee/wiki){ .card-link title=Documentação}
    [:octicons-code-16:](https://github.com/yattee/yattee){ .card-link title="Código-fonte" }
    [:octicons-heart-16:](https://github.com/yattee/yattee/wiki/Donations){ .card-link title=Contribuir }
    
    ??? downloads
    
        - [:simple-apple: App Store](https://apps.apple.com/us/app/yattee/id1595136629)
        - [:simple-github: GitHub](https://github.com/yattee/yattee/releases)

!!! aviso

    Ao utilizar o Yattee, o seu endereço IP pode ainda ser do conhecimento do YouTube, [Invidious](https://instances.invidious.io), [Piped](https://github.com/TeamPiped/Piped/wiki/Instances) ou [SponsorBlock](https://sponsor.ajay.app/), dependendo da sua configuração. Considere a utilização de uma [VPN](vpn.md) ou [Tor](https://www.torproject.org) se o seu [modelo de ameaça](basics/threat-modeling.md) exigir a ocultação do seu endereço IP.

Por predefinição, o Yattee bloqueia todos os anúncios do YouTube. Além disso, o Yattee integra-se opcionalmente com [SponsorBlock](https://sponsor.ajay.app) para o ajudar a saltar segmentos de vídeo patrocinados.

### LibreTube (Android)

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo LibreTube](assets/img/frontends/libretube.svg#only-light){ align=right }
    ![Logótipo LibreTube](assets/img/frontends/libretube-dark.svg#only-dark){ align=right }
    
    O **LibreTube** é uma aplicação Android gratuita e de código aberto para [YouTube](https://youtube.com), que utiliza a API [Piped](#piped).
    
    O LibreTube permite-lhe armazenar a sua lista de subscrição e listas de reprodução localmente no seu dispositivo Android, ou numa conta na sua instância de eleição do Piped, o que lhe permite aceder-lhes sem problemas também noutros dispositivos.
    
    [:octicons-home-16: Homepage](https://libre-tube.github.io){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://github.com/libre-tube/LibreTube#privacy-policy-and-disclaimer){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://github.com/libre-tube/LibreTube#readme){ .card-link title=Documentação}
    [:octicons-code-16:](https://github.com/libre-tube/LibreTube){ .card-link title="Código-fonte" }
    
    ??? downloads
    
        - [:simple-github: GitHub](https://github.com/libre-tube/LibreTube/releases)

!!! aviso

    Ao utilizar o LibreTube, o seu endereço IP será visível para a instância [Piped](https://github.com/TeamPiped/Piped/wiki/Instances) que escolher e/ou [SponsorBlock](https://sponsor.ajay.app/), dependendo da sua configuração. Considere a utilização de uma [VPN](vpn.md) ou [Tor](https://www.torproject.org) se o seu [modelo de ameaça](basics/threat-modeling.md) exigir a ocultação do seu endereço IP.

Por defeito, o LibreTube bloqueia todos os anúncios do YouTube. Além disso, o Libretube utiliza o [SponsorBlock](https://sponsor.ajay.app) para o ajudar a saltar segmentos de vídeo patrocinados. É possível configurar totalmente os tipos de segmentos que SponsorBlock irá ignorar ou desactivá-lo completamente. Existe também um botão no próprio leitor de vídeo para o desativar para um vídeo específico, se assim o desejar.

### NewPipe (Android)

!!! recommendation annotate

    ![Logótipo Newpipe](assets/img/frontends/newpipe.svg){ align=right }
    
    **NewPipe** é uma aplicação Android gratuita e de código aberto para [YouTube](https://youtube.com), [SoundCloud](https://soundcloud.com), [media.ccc.de](https://media.ccc.de), [Bandcamp](https://bandcamp.com) e [PeerTube](https://joinpeertube.org/) (1).
    
    A sua lista de subscrição e listas de reprodução são guardadas localmente no seu dispositivo Android.
    
    [:octicons-home-16: Homepage](https://newpipe.net){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://newpipe.net/legal/privacy){ .card-link title="Política de Privacidade" }
    [:octicons-info-16:](https://teamnewpipe.github.io/documentation/){ .card-link title=Documentação}
    [:octicons-code-16:](https://github.com/TeamNewPipe/NewPipe){ .card-link title="Código-fonte" }
    [:octicons-heart-16:](https://newpipe.net/donate/){ .card-link title=Contribuir }
    
    ??? downloads
    
        - [:simple-github: GitHub](https://github.com/TeamNewPipe/NewPipe/releases)

1. A instância predefinida é [FramaTube](https://framatube.org/), mas podem ser adicionadas mais através de **Settings** → **Content** → **PeerTube instances**

!!! aviso

    Ao utilizar o NewPipe, o seu endereço IP será visível para os fornecedores de vídeo utilizados. Considere a utilização de uma [VPN](vpn.md) ou [Tor](https://www.torproject.org) se o seu [modelo de ameaça](basics/threat-modeling.md) exigir a ocultação do seu endereço IP.

### Invidious

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo Invidious](assets/img/frontends/invidious.svg#only-light){ align=right }
    ![Logótipo Invidious](assets/img/frontends/invidious-dark.svg#only-dark){ align=right }
    
    O **Invidious** é um frontend gratuito e de código aberto para [YouTube](https://youtube.com), que também é auto-hospedável.
    
    Existem várias instâncias públicas, sendo que algumas instâncias têm suporte para serviços onion [Tor](https://www.torproject.org).
    
    [:octicons-home-16: Homepage](https://invidious.io){ .md-button .md-button--primary }
    [:octicons-server-16:](https://instances.invidious.io){ .card-link title="Instâncias Públicas"}
    [:octicons-info-16:](https://docs.invidious.io/){ .card-link title=Documentação}
    [:octicons-code-16:](https://github.com/iv-org/invidious){ .card-link title="Código-fonte" }
    [:octicons-heart-16:](https://invidious.io/donate/){ .card-link title=Contribuir }

!!! aviso

    O Invidious não faz proxy de fluxos de vídeo por predefinição. Os vídeos vistos através do Invidious continuarão a fazer ligações diretas aos servidores do Google (por exemplo, `googlevideo.com`); no entanto, algumas instâncias suportam o proxy de vídeo - basta ativar *Proxy videos* nas definições das instâncias ou adicionar `&local=true` ao URL.

!!! dica

    O Invidious é útil se pretender desativar o JavaScript no seu browser, como o [Tor Browser](https://www.torproject.org/) no nível de segurança Mais Seguro. Não proporciona privacidade por si só e não recomendamos que inicie sessão em conta alguma.

### Piped

!!! nota
    Consulte o [Tabela de Hardware](https://openwrt.org/toh/start) para verificar se o seu dispositivo é suportado.

    ![Logótipo Piped](assets/img/frontends/piped.svg){ align=right }
    
    O **Piped** é um frontend gratuito e de código aberto para [YouTube](https://youtube.com), que também é auto-hospedável.
    
    O Piped requer JavaScript para funcionar e existem várias instâncias públicas.
    
    [:octicons-repo-16: Repositório](https://github.com/TeamPiped/Piped){ .md-button .md-button--primary }
    [:octicons-server-16:](https://piped.kavin.rocks/preferences#ddlInstanceSelection){ .card-link title="Instâncias Públicas"}
    [:octicons-info-16:](https://piped-docs.kavin.rocks/){ .card-link title=Documentação}
    [:octicons-code-16:](https://github.com/TeamPiped/Piped){ .card-link title="Código-fonte" }
    [:octicons-heart-16:](https://github.com/TeamPiped/Piped#donations){ .card-link title=Contribuir }

!!! dica

    O Piped é útil se pretender utilizar [SponsorBlock](https://sponsor.ajay.app) sem instalar uma extensão ou para aceder a conteúdos com restrições de idade sem uma conta. Não proporciona privacidade por si só e não recomendamos que inicie sessão em conta alguma.

## Critérios

**Note que não estamos associados a nenhum dos projetos que recomendamos.** Para além dos [nossos critérios padrão](about/criteria.md), temos um conjunto claro de requisitos que nos permitem fornecer recomendações objetivas. Sugerimos que se familiarize com esta lista antes de optar por um projeto e que desenvolva a sua própria investigação para garantir que se trata da escolha certa para si.

!!! exemplo "Esta secção é nova"

    Estamos a trabalhar no sentido de estabelecer critérios para cada secção do nosso site, o que pode originar alterações. Se tiver alguma dúvida sobre os critérios utilizados, por favor [pergunte no nosso fórum] (https://discuss.privacyguides.net/latest) e não parta do princípio de que algo foi excluído das nossas recomendações, caso não esteja listado aqui. São muitos os fatores considerados e discutidos quando recomendamos um projeto, e documentar cada um deles é um trabalho em curso.

Frontends recomendados...

- O software deve ser de código aberto.
- Deve ser auto-hospedável.
- Deve fornecer todas as funcionalidades básicas do site disponíveis para utilizadores anónimos.

Só consideramos frontends para sites que sejam...

- Not normally accessible without JavaScript.
