---
meta_title: "The Best Private Instant Messengers - Privacy Guides"
title: "실시간 커뮤니케이션"
icon: material/chat-processing
description: Other instant messengers make all of your private conversations available to the company that runs them.
cover: real-time-communication.webp
---

본 내용은 실시간 커뮤니케이션 용도로 권장드리는 암호화 메신저 목록입니다.

[통신 네트워크 유형 :material-arrow-right-drop-circle:](./advanced/communication-network-types.md)

## 암호화 메신저

암호화 메신저는 민감한 대화를 보호하는 용도로 유용합니다.

### Signal

<div class="admonition recommendation" markdown>

![Signal 로고](assets/img/messengers/signal.svg){ align=right }

**Signal**은 Signal Messenger LLC에서 개발한 모바일 앱입니다. The app provides instant messaging and calls secured with the Signal Protocol, an extremely secure encryption protocol which supports forward secrecy[^1] and post-compromise security.[^2]

[:octicons-home-16: Homepage](https://signal.org/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://signal.org/legal/#privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://support.signal.org/hc/en-us){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/signalapp){ .card-link title="Source Code" }
[:octicons-heart-16:](https://signal.org/donate/){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.thoughtcrime.securesms)
- [:simple-appstore: App Store](https://apps.apple.com/app/id874139669)
- [:simple-android: Android](https://signal.org/android/apk/)
- [:simple-windows11: Windows](https://signal.org/download/windows)
- [:simple-apple: macOS](https://signal.org/download/macos)
- [:simple-linux: Linux](https://signal.org/download/linux)

</details>

</div>

Signal requires your phone number for registration, however you should create a username to hide your phone number from your contacts:

1. In Signal, open the app's settings and tap your account profile at the top.
2. Tap **Username** and choose **Continue** on the "Set up your Signal username" screen.
3. Enter a username. Your username will always be paired with a unique set of digits to keep your username unique and prevent people from guessing it, for example if you enter "John" your username might end up being `@john.35`.
4. Go back to the main app settings page and select **Privacy**.
5. Select **Phone Number**
6. Change the **Who Can See My Number** setting to: **Nobody**

You can optionally change the **Who Can Find Me By Number** setting to **Nobody** as well, if you want to prevent people who already have your phone number from discovering your Signal account/username.

Contact lists on Signal are encrypted using your Signal PIN and the server does not have access to them. 개인 프로필 또한 암호화되어 여러분이 대화하는 상대에게만 공유됩니다. Signal supports [private groups](https://signal.org/blog/signal-private-group-system/), where the server has no record of your group memberships, group titles, group avatars, or group attributes. 메타데이터를 최소화하는 [Sealed Sender](https://signal.org/blog/sealed-sender/) 기능도 존재합니다. 해당 기능을 사용할 경우, 발신자 주소는 메시지 본문과 함께 암호화되어 서버에서는 수신자 주소만 볼 수 있습니다. Sealed Sender는 연락처 목록에 있는 사람들에게만 활성화되지만, 스팸 수신 위험성이 높아짐에 따라 모든 수신자에게 활성화하는 것도 가능합니다.

Signal 프로토콜은 2016년에 독립적으로 [감사를 받았습니다](https://eprint.iacr.org/2016/1013.pdf). Signal 프로토콜 사양은 [문서](https://signal.org/docs/)에서 확인할 수 있습니다.

Signal 설치 구성 및 보안 강화 관련 도움말이 필요하신 분은 다음 내용을 참고하세요.

[Signal 설정 및 보안 강화 :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening/)

### SimpleX Chat

<div class="admonition recommendation" markdown>

![Simplex 로고](assets/img/messengers/simplex.svg){ align=right }

**SimpleX** Chat은 탈중앙화 메신저입니다. 전화번호나 사용자 아이디 등의 고유 식별자에 의존하지 않는 것이 특징입니다. SimpleX Chat에서는 QR 코드를 스캔하거나 초대 링크를 클릭하여 그룹 대화에 참여합니다.

[:octicons-home-16: Homepage](https://simplex.chat){ .md-button .md-button--primary }
[:octicons-eye-16:](https://github.com/simplex-chat/simplex-chat/blob/stable/PRIVACY.md){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://github.com/simplex-chat/simplex-chat/tree/stable/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/simplex-chat){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=chat.simplex.app)
- [:simple-appstore: App Store](https://apps.apple.com/us/app/simplex-chat/id1605771084)
- [:simple-github: GitHub](https://github.com/simplex-chat/simplex-chat/releases)
- [:simple-windows11: Windows](https://simplex.chat/downloads/#desktop-app)
- [:simple-apple: macOS](https://simplex.chat/downloads/#desktop-app)
- [:simple-linux: Linux](https://simplex.chat/downloads/#desktop-app)

</details>

</div>

SimpleX Chat 보안 감사는 Trail of Bits이 2022년 10월에 [진행하였습니다](https://simplex.chat/blog/20221108-simplex-chat-v4.2-security-audit-new-website.html).

SimpleX Chat supports basic group chatting functionality, direct messaging, and editing of messages and markdown. E2EE 음성 및 영상 통화 또한 지원됩니다. 여러분은 데이터를 내보내고 다른 기기에서 해당 데이터를 가져올 수 있습니다. Simplex Chat은 데이터가 백업되는 중앙 서버가 존재하지 않습니다.

### Briar

<div class="admonition recommendation" markdown>

![Briar 로고](assets/img/messengers/briar.svg){ align=right }

**Briar**는 Tor 네트워크를 이용해 다른 클라이언트에 연결하는 방식으로 [작동하는](https://briarproject.org/how-it-works/) 암호화 메신저입니다. 근거리에 있는 경우 Wi-Fi 혹은 Bluetooth를 통해 연결하는 것도 가능합니다. Briar 로컬 메시 모드는 인터넷을 제대로 사용할 수 없는 상황에도 유용합니다.

[:octicons-home-16: Homepage](https://briarproject.org/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://briarproject.org/privacy-policy/){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://code.briarproject.org/briar/briar/-/wikis/home){ .card-link title=Documentation}
[:octicons-code-16:](https://code.briarproject.org/briar/briar){ .card-link title="Source Code" }
[:octicons-heart-16:](https://briarproject.org/){ .card-link title="Donation options are listed on the bottom of the homepage" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.briarproject.briar.android)
- [:simple-windows11: Windows](https://briarproject.org/download-briar-desktop/)
- [:simple-linux: Linux](https://briarproject.org/download-briar-desktop/)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.briarproject.Briar)

</details>

</div>

Briar 연락처에 누군가를 등록하려면 서로가 모두 서로를 연락처에 추가해야 합니다. `briar://` 링크를 서로 교환하거나, (가까운 거리에 있는 경우) 연락처에서 QR 코드를 스캔하여 추가할 수 있습니다.

클라이언트 소프트웨어는 제3자로부터 [보안 감사를 받았습니다](https://briarproject.org/news/2017-beta-released-security-audit/). 메신저의 익명 라우팅 프로토콜은 마찬가지로 보안 감사가 진행된 바 있는 Tor 네트워크가 사용됩니다.

Briar [사양 문서](https://code.briarproject.org/briar/briar-spec)는 전체 공개되어 있습니다.

Briar supports forward secrecy[^1] by using the Bramble [Handshake](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BHP.md) and [Transport](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BTP.md) protocol.

## 추가 선택지

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

These messengers do not have forward secrecy[^1], and while they fulfill certain needs that our previous recommendations may not, we do not recommend them for long-term or sensitive communications. 대화 참여자 중 한 명만 키가 유출되더라도 이전에 주고받은 **모든** 메시지의 기밀성이 손상됩니다.

</div>

### Element

<div class="admonition recommendation" markdown>

![Element logo](assets/img/messengers/element.svg){ align=right }

**Element** is the reference [client](https://matrix.org/ecosystem/clients/) for the [Matrix](https://matrix.org/docs/guides/introduction) protocol, an [open standard](https://matrix.org/docs/spec) for secure decentralized real-time communication.

비공개 대화방(초대가 필요한 대화방)에서 이루어지는 메시지 및 파일 공유는 기본적으로 E2EE가 적용되며, 일대일 음성 및 영상 통화도 마찬가지입니다.

[:octicons-home-16: Homepage](https://element.io/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://element.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://element.io/help){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/element-hq){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=im.vector.app)
- [:simple-appstore: App Store](https://apps.apple.com/app/vector/id1083446067)
- [:simple-github: GitHub](https://github.com/vector-im/element-android/releases)
- [:simple-windows11: Windows](https://element.io/get-started)
- [:simple-apple: macOS](https://element.io/get-started)
- [:simple-linux: Linux](https://element.io/get-started)
- [:octicons-globe-16: Web](https://app.element.io)

</details>

</div>

프로필 사진, 메시지 반응, 닉네임은 암호화가 적용되지 않습니다.

그룹 음성 및 영상 통화에는 E2EE가 [아닌](https://github.com/vector-im/element-web/issues/12878), Jitsi를 사용합니다. 단, 이는 추후 [Native Group VoIP Signalling](https://github.com/matrix-org/matrix-doc/pull/3401)으로 변경될 예정입니다. 현재 그룹 통화는 인증 과정을 거치지 [않습니다](https://github.com/vector-im/element-web/issues/13074). 즉, 룸 참가자가 아닌 사람도 통화에 난입하는 것이 가능합니다. 사적인 모임에서는 해당 기능을 사용하지 않는 것이 좋습니다.

The Matrix protocol itself [theoretically supports forward secrecy](https://gitlab.matrix.org/matrix-org/olm/blob/master/docs/megolm.md#partial-forward-secrecy)[^1], however this is [not currently supported in Element](https://github.com/vector-im/element-web/issues/7101) due to it breaking some aspects of the user experience such as key backups and shared message history.

Matrix 프로토콜은 2016년에 독립적으로 [감사를 받았습니다](https://matrix.org/blog/2016/11/21/matrixs-olm-end-to-end-encryption-security-assessment-released-and-implemented-cross-platform-on-riot-at-last). Matirx 프로토콜 사양은 [문서](https://spec.matrix.org/latest/)에서 확인할 수 있습니다. The [Olm cryptographic ratchet](https://matrix.org/docs/matrix-concepts/end-to-end-encryption/) used by Matrix is an implementation of Signal’s [Double Ratchet algorithm](https://signal.org/docs/specifications/doubleratchet/).

### Session

<div class="admonition recommendation" markdown>

![Session 로고](assets/img/messengers/session.svg){ align=right }

**Session**는 비공개, 보안, 익명 대화에 중점을 둔 탈중앙화 메신저입니다. Session은 개인 메시지, 그룹 채팅, 음성 통화를 지원합니다.

Session은 탈중앙화된 [Oxen Service Node Network](https://oxen.io/)를 이용해 메시지 저장 및 라우팅을 수행합니다. 모든 암호화 메시지는 Oxen 서비스 노드 네트워크의 노드 3개를 이용해 라우팅되므로, 특정 노드가 사용자에 대한 의미 있는 정보를 수집하는 것은 불가능에 가깝습니다.

[:octicons-home-16: Homepage](https://getsession.org/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://getsession.org/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://getsession.org/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/oxen-io){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=network.loki.messenger)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1470168868)
- [:simple-github: GitHub](https://github.com/oxen-io/session-android/releases)
- [:simple-windows11: Windows](https://getsession.org/download)
- [:simple-apple: macOS](https://getsession.org/download)
- [:simple-linux: Linux](https://getsession.org/download)

</details>

</div>

Session은 일대일 채팅 및 최대 100명까지 참여 가능한 비공개 그룹에서 E2EE를 지원합니다. 공개 그룹은 구성원 수에 제한이 없지만, 설계상 개방되어 있습니다.

Session was previously based on Signal Protocol before replacing it with their own in December 2020. Session Protocol does [not](https://getsession.org/blog/session-protocol-technical-information) support forward secrecy.[^1]

Oxen requested an independent audit for Session in March 2020. The audit [concluded](https://getsession.org/session-code-audit) in April 2021, “The overall security level of this application is good and makes it usable for privacy-concerned people.”

Session has a [whitepaper](https://arxiv.org/pdf/2002.04609.pdf) describing the technical details of the app and protocol.

## 평가 기준

**Privacy Guides는 권장 목록의 어떠한 프로젝트와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

<div class="admonition example" markdown>
<p class="admonition-title">This section is new</p>

Privacy Guides 팀은 사이트의 모든 항목마다 명확한 평가 기준을 정립하는 중이며, 따라서 세부 내용은 변경될 수 있습니다. 평가 기준에 대해서 질문이 있다면 [포럼에서 문의](https://discuss.privacyguides.net/latest)하시기 바랍니다. (무언가가 목록에 존재하지 않다고 해서 권장 목록을 작성할 때 고려한 적이 없을 것으로 단정 짓지 마세요.) 권장 목록에 어떤 프로젝트를 추가할 때 고려하고 논의해야 할 요소는 매우 많으며, 모든 요소를 문서화하는 것은 현재 진행 중인 작업입니다.

</div>

- Has open-source clients.
- Does not require sharing personal identifiers (phone numbers or emails in particular) with contacts.
- Uses E2EE for private messages by default.
- Supports E2EE for all messages.
- Has been independently audited.

### 우대 사항

평가 기준에서 '우대 사항'은 해당 부문에서 완벽한 프로젝트에 기대하는 바를 나타냅니다. 다음의 우대 사항에 해당하지 않더라도 권장 목록에 포함될 수 있습니다. 단, 우대 사항에 해당할수록 이 페이지의 다른 항목보다 높은 순위를 갖습니다.

- Supports Forward Secrecy[^1]
- Supports Future Secrecy (Post-Compromise Security)[^2]
- Has open-source servers.
- Decentralized, i.e. [federated or P2P](advanced/communication-network-types.md).
- Uses E2EE for all messages by default.
- Supports Linux, macOS, Windows, Android, and iOS.

[^1]: [Forward Secrecy](https://en.wikipedia.org/wiki/Forward_secrecy) is where keys are rotated very frequently, so that if the current encryption key is compromised, it does not expose **past** messages as well.
[^2]: Future Secrecy (or Post-Compromise Security) is a feature where an attacker is prevented from decrypting **future** messages after compromising a private key, unless they compromise more session keys in the future as well. This effectively forces the attacker to intercept all communication between parties, since they lose access as soon as a key exchange occurs that is not intercepted.
