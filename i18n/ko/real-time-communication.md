---
meta_title: "The Best Private Instant Messengers - Privacy Guides"
title: "실시간 커뮤니케이션"
icon: material/chat-processing
description: Other instant messengers make all of your private conversations available to the company that runs them.
cover: real-time-communication.png
---

These are our recommendations for encrypted real-time communication.

[Types of Communication Networks :material-arrow-right-drop-circle:](./advanced/communication-network-types.md)

## 암호화 메신저

These messengers are great for securing your sensitive communications.

### Signal

!!! recommendation

    ![Signal 로고](assets/img/messengers/signal.svg){ align=right }
    
    **Signal**은 Signal Messenger LLC에서 개발한 모바일 앱입니다. 인스턴트 메시지, 음성 및 영상 통화 기능을 제공합니다.
    
    모든 통신은 E2EE가 적용됩니다. 연락처 목록은 Signal PIN으로 암호화되며, 서버에서는 연락처 목록에 접근할 수 없습니다. 개인 프로필 또한 암호화되어 여러분이 대화하는 상대에게만 공유됩니다.
    
    [:octicons-home-16: 홈페이지](https://signal.org/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://signal.org/legal/#privacy-policy){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://support.signal.org/hc/en-us){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/signalapp){ .card-link title="소스 코드" }
    [:octicons-heart-16:](https://signal.org/donate/){ .card-link title=기부 }
    
    ??? downloads "다운로드"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.thoughtcrime.securesms)
        - [:simple-appstore: App Store](https://apps.apple.com/app/id874139669)
        - [:simple-android: Android](https://signal.org/android/apk/)
        - [:simple-windows11: Windows](https://signal.org/download/windows)
        - [:simple-apple: macOS](https://signal.org/download/macos)
        - [:simple-linux: Linux](https://signal.org/download/linux)

Signal supports [private groups](https://signal.org/blog/signal-private-group-system/). The server has no record of your group memberships, group titles, group avatars, or group attributes. Signal has minimal metadata when [Sealed Sender](https://signal.org/blog/sealed-sender/) is enabled. The sender address is encrypted along with the message body, and only the recipient address is visible to the server. Sealed Sender is only enabled for people in your contacts list, but can be enabled for all recipients with the increased risk of receiving spam. Signal requires your phone number as a personal identifier.

The protocol was independently [audited](https://eprint.iacr.org/2016/1013.pdf) in 2016. The specification for the Signal protocol can be found in their [documentation](https://signal.org/docs/).

We have some additional tips on configuring and hardening your Signal installation:

[Signal Configuration and Hardening :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening/)

### SimpleX Chat

!!! recommendation

    ![Simplex logo](assets/img/messengers/simplex.svg){ align=right }
    
    **SimpleX** Chat is an instant messenger that is decentralized and doesn't depend on any unique identifiers such as phone numbers or usernames. Users of SimpleX Chat can scan a QR code or click an invite link to participate in group conversations.
    
    [:octicons-home-16: 홈페이지](https://simplex.chat){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://github.com/simplex-chat/simplex-chat/blob/stable/PRIVACY.md){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://github.com/simplex-chat/simplex-chat/tree/stable/docs){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/simplex-chat){ .card-link title="소스 코드" }
    
    ??? downloads "다운로드"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=chat.simplex.app)
        - [:simple-appstore: App Store](https://apps.apple.com/us/app/simplex-chat/id1605771084)
        - [:simple-github: GitHub](https://github.com/simplex-chat/simplex-chat/releases)

SimpleX Chat [was audited](https://simplex.chat/blog/20221108-simplex-chat-v4.2-security-audit-new-website.html) by Trail of Bits in October 2022.

Currently SimpleX Chat only provides a client for Android and iOS. Basic group chatting functionality, direct messaging, editing of messages and markdown are supported. E2EE Audio and Video calls are also supported.

Your data can be exported, and imported onto another device, as there are no central servers where this is backed up.

### Briar

!!! recommendation

    ![Briar logo](assets/img/messengers/briar.svg){ align=right }
    
    **Briar** is an encrypted instant messenger that [connects](https://briarproject.org/how-it-works/) to other clients using the Tor Network. Briar can also connect via Wi-Fi or Bluetooth when in local proximity. Briar’s local mesh mode can be useful when internet availability is a problem.
    
    [:octicons-home-16: 홈페이지](https://briarproject.org/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://briarproject.org/privacy-policy/){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://code.briarproject.org/briar/briar/-/wikis/home){ .card-link title=문서}
    [:octicons-code-16:](https://code.briarproject.org/briar/briar){ .card-link title="소스 코드" }
    [:octicons-heart-16:](https://briarproject.org/){ .card-link title="기부 옵션은 홈페이지 하단에 위치하고 있습니다" }
    
    ??? downloads "다운로드"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.briarproject.briar.android)
        - [:simple-windows11: Windows](https://briarproject.org/download-briar-desktop/)
        - [:simple-linux: Linux](https://briarproject.org/download-briar-desktop/)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/org.briarproject.Briar)

To add a contact on Briar, you must both add each other first. You can either exchange `briar://` links or scan a contact’s QR code if they are nearby.

The client software was independently [audited](https://briarproject.org/news/2017-beta-released-security-audit/), and the anonymous routing protocol uses the Tor network which has also been audited.

Briar has a fully [published specification](https://code.briarproject.org/briar/briar-spec).

Briar supports perfect forward secrecy by using the Bramble [Handshake](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BHP.md) and [Transport](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BTP.md) protocol.

## Additional Options

!!! warning "경고"

    These messengers do not have Perfect [Forward Secrecy](https://en.wikipedia.org/wiki/Forward_secrecy) (PFS), and while they fulfill certain needs that our previous recommendations may not, we do not recommend them for long-term or sensitive communications. Any key compromise among message recipients would affect the confidentiality of **all** past communications.

### Element

!!! recommendation

    ![Element logo](assets/img/messengers/element.svg){ align=right }
    
    **Element** is the reference client for the [Matrix](https://matrix.org/docs/guides/introduction) protocol, an [open standard](https://matrix.org/docs/spec) for secure decentralized real-time communication.
    
    Messages and files shared in private rooms (those which require an invite) are by default E2EE as are one to one voice and video calls.
    
    [:octicons-home-16: 홈페이지](https://element.io/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://element.io/privacy){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://element.io/help){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/vector-im){ .card-link title="소스 코드" }
    
    ??? downloads "다운로드"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=im.vector.app)
        - [:simple-appstore: App Store](https://apps.apple.com/app/vector/id1083446067)
        - [:simple-github: GitHub](https://github.com/vector-im/element-android/releases)
        - [:simple-windows11: Windows](https://element.io/get-started)
        - [:simple-apple: macOS](https://element.io/get-started)
        - [:simple-linux: Linux](https://element.io/get-started)
        - [:octicons-globe-16: Web](https://app.element.io)

프로필 사진, 메시지 반응, 닉네임은 암호화되지 않습니다.

Group voice and video calls are [not](https://github.com/vector-im/element-web/issues/12878) E2EE, and use Jitsi, but this is expected to change with [Native Group VoIP Signalling](https://github.com/matrix-org/matrix-doc/pull/3401). Group calls have [no authentication](https://github.com/vector-im/element-web/issues/13074) currently, meaning that non-room participants can also join the calls. We recommend that you do not use this feature for private meetings.

The Matrix protocol itself [theoretically supports PFS](https://gitlab.matrix.org/matrix-org/olm/blob/master/docs/megolm.md#partial-forward-secrecy), however this is [not currently supported in Element](https://github.com/vector-im/element-web/issues/7101) due to it breaking some aspects of the user experience such as key backups and shared message history.

The protocol was independently [audited](https://matrix.org/blog/2016/11/21/matrixs-olm-end-to-end-encryption-security-assessment-released-and-implemented-cross-platform-on-riot-at-last) in 2016. The specification for the Matrix protocol can be found in their [documentation](https://spec.matrix.org/latest/). The [Olm](https://matrix.org/docs/projects/other/olm) cryptographic ratchet used by Matrix is an implementation of Signal’s [Double Ratchet algorithm](https://signal.org/docs/specifications/doubleratchet/).

### Session

!!! recommendation

    ![Session logo](assets/img/messengers/session.svg){ align=right }
    
    **Session** is a decentralized messenger with a focus on private, secure, and anonymous communications. Session offers support for direct messages, group chats, and voice calls.
    
    Session uses the decentralized [Oxen Service Node Network](https://oxen.io/) to store and route messages. Every encrypted message is routed through three nodes in the Oxen Service Node Network, making it virtually impossible for the nodes to compile meaningful information on those using the network.
    
    [:octicons-home-16: 홈페이지](https://getsession.org/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://getsession.org/privacy-policy){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://getsession.org/faq){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/oxen-io){ .card-link title="소스 코드" }
    
    ??? downloads "다운로드"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=network.loki.messenger)
        - [:simple-appstore: App Store](https://apps.apple.com/app/id1470168868)
        - [:simple-github: GitHub](https://github.com/oxen-io/session-android/releases)
        - [:simple-windows11: Windows](https://getsession.org/download)
        - [:simple-apple: macOS](https://getsession.org/download)
        - [:simple-linux: Linux](https://getsession.org/download)

Session allows for E2EE in one-on-one chats or closed groups which allow for up to 100 members. Open groups have no restriction on the number of members, but are open by design.

Session does [not](https://getsession.org/blog/session-protocol-technical-information) support PFS, which is when an encryption system automatically and frequently changes the keys it uses to encrypt and decrypt information, such that if the latest key is compromised it exposes a smaller portion of sensitive information.

Oxen requested an independent audit for Session in March of 2020. The audit [concluded](https://getsession.org/session-code-audit) in April of 2021, “The overall security level of this application is good and makes it usable for privacy-concerned people.”

Session has a [whitepaper](https://arxiv.org/pdf/2002.04609.pdf) describing the technicals of the app and protocol.

## 평가 기준

**Privacy Guides는 권장 목록의 어떠한 프로젝트와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

!!! example "이 단락은 최근에 만들어졌습니다"

    Privacy Guides 팀은 사이트의 모든 항목마다 명확한 평가 기준을 정립하는 중이며, 따라서 세부 내용은 변경될 수 있습니다. 평가 기준에 대해서 질문이 있다면 [포럼에서 문의](https://discuss.privacyguides.net/latest)하시기 바랍니다. (무언가가 목록에 존재하지 않다고 해서 권장 목록을 작성할 때 고려한 적이 없을 것으로 단정 짓지 마세요.) 권장 목록에 어떤 프로젝트를 추가할 때 고려하고 논의해야 할 요소는 매우 많으며, 모든 요소를 문서화하는 것은 현재 진행 중인 작업입니다.

- 오픈 소스 클라이언트가 있어야 합니다.
- 비공개 메시지에는 E2EE가 기본 적용이어야 합니다.
- 모든 메시지에 E2EE가 지원되어야 합니다.
- 독립적인 감사를 받았어야 합니다.

### 우대 사항

평가 기준에서 '우대 사항'은 해당 부문에서 완벽한 프로젝트에 기대하는 바를 나타냅니다. 다음의 우대 사항에 해당하지 않더라도 권장 목록에 포함될 수 있습니다. 단, 우대 사항에 해당할수록 이 페이지의 다른 항목보다 높은 순위를 갖습니다.

- 완전 순방향 비밀성(Perfect Forward Secrecy)을 보장해야 합니다.
- 오픈 소스 서버가 있어야 합니다.
- 탈중앙 방식(연합 방식/P2P 방식)이어야 합니다.
- 모든 메시지에 E2EE가 기본 적용이어야 합니다.
- Linux, macOS, Windows, Android, iOS를 지원해야 합니다.
