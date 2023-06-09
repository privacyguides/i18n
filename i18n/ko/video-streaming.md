---
title: "동영상 스트리밍"
icon: material/video-wireless
description: These networks allow you to stream internet content without building an advertising profile based on your interests.
cover: video-streaming.png
---

The primary threat when using a video streaming platform is that your streaming habits and subscription lists could be used to profile you. You should combine these tools with a [VPN](vpn.md) or [Tor](https://www.torproject.org/) to make it harder to profile your usage.

## LBRY

!!! recommendation

    ![LBRY logo](assets/img/video-streaming/lbry.svg){ align=right }
    
    **The LBRY network** is a decentralized video sharing network. It uses a [BitTorrent](https://wikipedia.org/wiki/BitTorrent)-like network to store the video content, and a [blockchain](https://wikipedia.org/wiki/Blockchain) to store the indexes for those videos. The main benefit of this design is censorship resistance.
    
    **The LBRY desktop client** helps you stream videos from the LBRY network and stores your subscription list in your own LBRY wallet.
    
    [:octicons-home-16: Homepage](https://lbry.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://lbry.com/privacypolicy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://lbry.com/faq){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/lbryio/lbry-desktop){ .card-link title="Source Code" }
    
    ??? downloads
    
        - [:simple-windows11: Windows](https://lbry.com/windows)
        - [:simple-apple: macOS](https://lbry.com/osx)
        - [:simple-linux: Linux](https://lbry.com/linux)

!!! note

    Only the **LBRY desktop client** is recommended, as the [Odysee](https://odysee.com) website and the LBRY clients in F-Droid, Play Store, and the App Store have mandatory synchronization and telemetry.

!!! warning "경고"

    While watching and hosting videos, your IP address is visible to the LBRY network. Consider using a [VPN](vpn.md) or [Tor](https://www.torproject.org) if your [threat model](basics/threat-modeling.md) requires hiding your IP address.

We recommend **against** synchronizing your wallet with LBRY Inc., as synchronizing encrypted wallets is not supported yet. If you synchronize your wallet with LBRY Inc., you have to trust them to not look at your subscription list, [LBC](https://lbry.com/faq/earn-credits) funds, or take control of your channel.

You can disable *Save hosting data to help the LBRY network* option in :gear: **Settings** → **Advanced Settings**, to avoid exposing your IP address and watched videos when using LBRY for a prolonged period of time.

## 평가 기준

**Privacy Guides는 권장 목록의 어떠한 프로젝트와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

!!! example "이 단락은 최근에 만들어졌습니다"

    Privacy Guides 팀은 사이트의 모든 항목마다 명확한 평가 기준을 정립하는 중이며, 따라서 세부 내용은 변경될 수 있습니다. 평가 기준에 대해서 질문이 있다면 [포럼에서 문의](https://discuss.privacyguides.net/latest)하시기 바랍니다. (무언가가 목록에 존재하지 않다고 해서 권장 목록을 작성할 때 고려한 적이 없을 것으로 단정 짓지 마세요.) 권장 목록에 어떤 프로젝트를 추가할 때 고려하고 논의해야 할 요소는 매우 많으며, 모든 요소를 문서화하는 것은 현재 진행 중인 작업입니다.

- Must not require a centralized account to view videos.
    - Decentralized authentication, such as via a mobile wallet's private key is acceptable.
