---
title: "프론트엔드"
icon: material/flip-to-front
description: These open-source frontends for various internet services allow you to access content without JavaScript or other annoyances.
cover: frontends.png
---

Sometimes services will try to force you to sign up for an account by blocking access to content with annoying popups. They might also break without JavaScript enabled. These frontends can allow you to get around these restrictions.

If you choose to self-host these frontends, it is important that you have other people using your instance as well in order for you to blend in. You should be careful with where and how you are hosting, as other peoples' usage will be linked to your hosting.

When you are using an instance run by someone else, make sure to read the privacy policy of that specific instance. They can be modified by their owners and therefore may not reflect the default policy. Some instances have Tor .onion addresses which may grant some privacy as long as your search queries don't contain PII.

## Twitter

### Nitter

!!! recommendation

    ![Nitter logo](assets/img/frontends/nitter.svg){ align=right }
    
    **Nitter** is a free and open-source frontend for [Twitter](https://twitter.com) that is also self-hostable.
    
    There are a number of public instances, with some instances having [Tor](https://www.torproject.org) onion services support.
    
    [:octicons-repo-16: 저장소](https://github.com/zedeus/nitter){ .md-button .md-button--primary }
    [:octicons-server-16:](https://github.com/zedeus/nitter/wiki/Instances){ .card-link title="공개 인스턴스"}
    [:octicons-info-16:](https://github.com/zedeus/nitter/wiki){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/zedeus/nitter){ .card-link title="소스 코드" }
    [:octicons-heart-16:](https://github.com/zedeus/nitter#nitter){ .card-link title=기부 }

!!! tip "도움말"

    Nitter is useful if you want to browse Twitter content without having to log in and if you want to disable JavaScript in your browser, as is the case with [Tor Browser](https://www.torproject.org/) on the Safest security level. It also allows you to [create RSS feeds for Twitter](news-aggregators.md#twitter).

## TikTok

### ProxiTok

!!! recommendation

    ![ProxiTok logo](assets/img/frontends/proxitok.svg){ align=right }
    
    **ProxiTok** is an open source frontend to the [TikTok](https://www.tiktok.com) website that is also self-hostable.
    
    There are a number of public instances, with some instances having [Tor](https://www.torproject.org) onion services support.
    
    [:octicons-repo-16: 저장소](https://github.com/pablouser1/ProxiTok){ .md-button .md-button--primary }
    [:octicons-server-16:](https://github.com/pablouser1/ProxiTok/wiki/Public-instances){ .card-link title="공개 인스턴스"}
    [:octicons-info-16:](https://github.com/pablouser1/ProxiTok/wiki){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/pablouser1/ProxiTok){ .card-link title="소스 코드" }

!!! tip "도움말"

    ProxiTok is useful if you want to disable JavaScript in your browser, such as [Tor Browser](https://www.torproject.org/) on the Safest security level.

## YouTube

### FreeTube

!!! recommendation

    ![FreeTube logo](assets/img/frontends/freetube.svg){ align=right }
    
    **FreeTube** is a free and open-source desktop application for [YouTube](https://youtube.com). When using FreeTube, your subscription list and playlists are saved locally on your device.
    
    By default, FreeTube blocks all YouTube advertisements. In addition, FreeTube optionally integrates with [SponsorBlock](https://sponsor.ajay.app) to help you skip sponsored video segments.
    
    [:octicons-home-16: 홈페이지](https://freetubeapp.io){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://freetubeapp.io/privacy.php){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://docs.freetubeapp.io/){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/FreeTubeApp/FreeTube){ .card-link title="소스 코드" }
    [:octicons-heart-16:](https://liberapay.com/FreeTube){ .card-link title=기부 }
    
    ??? downloads "다운로드"
    
        - [:simple-windows11: Windows](https://freetubeapp.io/#download)
        - [:simple-apple: macOS](https://freetubeapp.io/#download)
        - [:simple-linux: Linux](https://freetubeapp.io/#download)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/io.freetubeapp.FreeTube)

!!! warning "경고"

    When using FreeTube, your IP address may still be known to YouTube, [Invidious](https://instances.invidious.io) or [SponsorBlock](https://sponsor.ajay.app/) depending on your configuration. Consider using a [VPN](vpn.md) or [Tor](https://www.torproject.org) if your [threat model](basics/threat-modeling.md) requires hiding your IP address.

### Yattee

!!! recommendation

    ![Yattee logo](assets/img/frontends/yattee.svg){ align=right }
    
    **Yattee** is a free and open-source privacy oriented video player for iOS, tvOS and macOS for [YouTube](https://youtube.com). When using Yattee, your subscription list are saved locally on your device.
    
    You will need to take a few [extra steps](https://gonzoknows.com/posts/Yattee/) before you can use Yattee to watch YouTube, due to App Store restrictions.
    
    [:octicons-home-16: 홈페이지](https://github.com/yattee/yattee){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://r.yattee.stream/docs/privacy.html){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://github.com/yattee/yattee/wiki){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/yattee/yattee){ .card-link title="소스 코드" }
    [:octicons-heart-16:](https://github.com/yattee/yattee/wiki/Donations){ .card-link title=기부 }
    
    ??? downloads "다운로드"
    
        - [:simple-apple: App Store](https://apps.apple.com/us/app/yattee/id1595136629)
        - [:simple-github: GitHub](https://github.com/yattee/yattee/releases)

!!! warning "경고"

    When using Yattee, your IP address may still be known to YouTube, [Invidious](https://instances.invidious.io), [Piped](https://github.com/TeamPiped/Piped/wiki/Instances) or [SponsorBlock](https://sponsor.ajay.app/) depending on your configuration. Consider using a [VPN](vpn.md) or [Tor](https://www.torproject.org) if your [threat model](basics/threat-modeling.md) requires hiding your IP address.

By default, Yattee blocks all YouTube advertisements. In addition, Yattee optionally integrates with [SponsorBlock](https://sponsor.ajay.app) to help you skip sponsored video segments.

### LibreTube (Android)

!!! recommendation

    ![LibreTube logo](assets/img/frontends/libretube.svg#only-light){ align=right }
    ![LibreTube logo](assets/img/frontends/libretube-dark.svg#only-dark){ align=right }
    
    **LibreTube** is a free and open-source Android application for [YouTube](https://youtube.com) which uses the [Piped](#piped) API.
    
    LibreTube allows you to store your subscription list and playlists locally on your Android device, or to an account on your Piped instance of choice, which allows you to access them seamlessly on other devices as well.
    
    [:octicons-home-16: 홈페이지](https://libre-tube.github.io){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://github.com/libre-tube/LibreTube#privacy-policy-and-disclaimer){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://github.com/libre-tube/LibreTube#readme){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/libre-tube/LibreTube){ .card-link title="소스 코드" }
    
    ??? downloads "다운로드"
    
        - [:simple-github: GitHub](https://github.com/libre-tube/LibreTube/releases)

!!! warning "경고"

    When using LibreTube, your IP address will be visible to the [Piped](https://github.com/TeamPiped/Piped/wiki/Instances) instance you choose and/or [SponsorBlock](https://sponsor.ajay.app/) depending on your configuration. Consider using a [VPN](vpn.md) or [Tor](https://www.torproject.org) if your [threat model](basics/threat-modeling.md) requires hiding your IP address.

By default, LibreTube blocks all YouTube advertisements. Additionally, Libretube uses [SponsorBlock](https://sponsor.ajay.app) to help you skip sponsored video segments. You are able to fully configure the types of segments that SponsorBlock will skip, or disable it completely. There is also a button on the video player itself to disable it for a specific video if desired.

### NewPipe (Android)

!!! recommendation annotate

    ![Newpipe logo](assets/img/frontends/newpipe.svg){ align=right }
    
    **NewPipe** is a free and open-source Android application for [YouTube](https://youtube.com), [SoundCloud](https://soundcloud.com), [media.ccc.de](https://media.ccc.de), [Bandcamp](https://bandcamp.com), and [PeerTube](https://joinpeertube.org/) (1).
    
    Your subscription list and playlists are saved locally on your Android device.
    
    [:octicons-home-16: 홈페이지](https://newpipe.net){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://newpipe.net/legal/privacy){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://teamnewpipe.github.io/documentation/){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/TeamNewPipe/NewPipe){ .card-link title="소스 코드" }
    [:octicons-heart-16:](https://newpipe.net/donate/){ .card-link title=기부 }
    
    ??? downloads "다운로드"
    
        - [:simple-github: GitHub](https://github.com/TeamNewPipe/NewPipe/releases)

1. The default instance is [FramaTube](https://framatube.org/), however more can be added via **Settings** → **Content** → **PeerTube instances**

!!! warning "경고"

    When using NewPipe, your IP address will be visible to the video providers used. Consider using a [VPN](vpn.md) or [Tor](https://www.torproject.org) if your [threat model](basics/threat-modeling.md) requires hiding your IP address.

### Invidious

!!! recommendation

    ![Invidious logo](assets/img/frontends/invidious.svg#only-light){ align=right }
    ![Invidious logo](assets/img/frontends/invidious-dark.svg#only-dark){ align=right }
    
    **Invidious** is a free and open-source frontend for [YouTube](https://youtube.com) that is also self-hostable.
    
    There are a number of public instances, with some instances having [Tor](https://www.torproject.org) onion services support.
    
    [:octicons-home-16: 홈페이지](https://invidious.io){ .md-button .md-button--primary }
    [:octicons-server-16:](https://instances.invidious.io){ .card-link title="공개 인스턴스"}
    [:octicons-info-16:](https://docs.invidious.io/){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/iv-org/invidious){ .card-link title="소스 코드" }
    [:octicons-heart-16:](https://invidious.io/donate/){ .card-link title=기부 }

!!! warning "경고"

    Invidious does not proxy video streams by default. Videos watched through Invidious will still make direct connections to Google's servers (e.g. `googlevideo.com`); however, some instances support video proxying—simply enable *Proxy videos* within the instances' settings or add `&local=true` to the URL.

!!! tip "도움말"

    Invidious is useful if you want to disable JavaScript in your browser, such as [Tor Browser](https://www.torproject.org/) on the Safest security level. It does not provide privacy by itself, and we don’t recommend logging into any accounts.

### Piped

!!! recommendation

    ![Piped logo](assets/img/frontends/piped.svg){ align=right }
    
    **Piped** is a free and open-source frontend for [YouTube](https://youtube.com) that is also self-hostable.
    
    Piped requires JavaScript in order to function and there are a number of public instances.
    
    [:octicons-repo-16: 저장소](https://github.com/TeamPiped/Piped){ .md-button .md-button--primary }
    [:octicons-server-16:](https://piped.kavin.rocks/preferences#ddlInstanceSelection){ .card-link title="공개 인스턴스"}
    [:octicons-info-16:](https://piped-docs.kavin.rocks/){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/TeamPiped/Piped){ .card-link title="소스 코드" }
    [:octicons-heart-16:](https://github.com/TeamPiped/Piped#donations){ .card-link title=기부 }

!!! tip "도움말"

    Piped is useful if you want to use [SponsorBlock](https://sponsor.ajay.app) without installing an extension or to access age-restricted content without an account. It does not provide privacy by itself, and we don’t recommend logging into any accounts.

## 평가 기준

**Privacy Guides는 권장 목록의 어떠한 프로젝트와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

!!! example "이 단락은 최근에 만들어졌습니다"

    Privacy Guides 팀은 사이트의 모든 항목마다 명확한 평가 기준을 정립하는 중이며, 따라서 세부 내용은 변경될 수 있습니다. 평가 기준에 대해서 질문이 있다면 [포럼에서 문의](https://discuss.privacyguides.net/latest)하시기 바랍니다. (무언가가 목록에 존재하지 않다고 해서 권장 목록을 작성할 때 고려한 적이 없을 것으로 단정 짓지 마세요.) 권장 목록에 어떤 프로젝트를 추가할 때 고려하고 논의해야 할 요소는 매우 많으며, 모든 요소를 문서화하는 것은 현재 진행 중인 작업입니다.

Recommended frontends...

- 오픈 소스 소프트웨어여야 합니다.
- 자체 호스팅이 가능해야 합니다.
- 익명 사용자도 웹사이트의 기본적인 기능을 모두 사용할 수 있어야 합니다.

We only consider frontends for websites which are...

- Not normally accessible without JavaScript.
