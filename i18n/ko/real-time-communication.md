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

**Signal**은 Signal Messenger LLC에서 개발한 모바일 앱입니다. 인스턴트 메시지, 음성 및 영상 통화 기능을 제공합니다.

모든 통신은 E2EE가 적용됩니다. 연락처 목록은 Signal PIN으로 암호화되며, 서버에서는 연락처 목록에 접근할 수 없습니다. 개인 프로필 또한 암호화되어 여러분이 대화하는 상대에게만 공유됩니다.

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

Singal은 [비공개 그룹](https://signal.org/blog/signal-private-group-system/)을 지원합니다. 그룹 구성원, 그룹 이름, 아바타, 속성 등은 서버에 기록되지 않습니다. 메타데이터를 최소화하는 [Sealed Sender](https://signal.org/blog/sealed-sender/) 기능도 존재합니다. 해당 기능을 사용할 경우, 발신자 주소는 메시지 본문과 함께 암호화되어 서버에서는 수신자 주소만 볼 수 있습니다. Sealed Sender는 연락처 목록에 있는 사람들에게만 활성화되지만, 스팸 수신 위험성이 높아짐에 따라 모든 수신자에게 활성화하는 것도 가능합니다. Signal을 사용하려면 반드시 자신의 전화번호를 개인 식별 정보로 입력해야만 합니다.

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

Briar supports Forward Secrecy by using the Bramble [Handshake](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BHP.md) and [Transport](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BTP.md) protocol.

## 추가 선택지

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

These messengers do not have [Forward Secrecy](https://en.wikipedia.org/wiki/Forward_secrecy), and while they fulfill certain needs that our previous recommendations may not, we do not recommend them for long-term or sensitive communications. 대화 참여자 중 한 명만 키가 유출되더라도 이전에 주고받은 **모든** 메시지의 기밀성이 손상됩니다.

</div>

### Element

<div class="admonition recommendation" markdown>

![Element 로고](assets/img/messengers/element.svg){ align=right }

**Element**는 [Matrix](https://matrix.org/docs/guides/introduction)라는 안전한 탈중앙화 실시간 통신 [개방형 표준](https://matrix.org/docs/spec) 프로토콜의 레퍼런스 클라이언트입니다.

비공개 대화방(초대가 필요한 대화방)에서 이루어지는 메시지 및 파일 공유는 기본적으로 E2EE가 적용되며, 일대일 음성 및 영상 통화도 마찬가지입니다.

[:octicons-home-16: Homepage](https://element.io/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://element.io/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://element.io/help){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/vector-im){ .card-link title="Source Code" }

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

Matrix 프로토콜 자체는 [이론적으로 PFS를 지원하지만](https://gitlab.matrix.org/matrix-org/olm/blob/master/docs/megolm.md#partial-forward-secrecy), 키 백업 및 사용자 간 메시지 기록 공유 등의 사용자 경험을 해치기 때문에 [현시점에서 Element는 PFS를 지원하지 않습니다](https://github.com/vector-im/element-web/issues/7101).

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

Session은 완전 순방향 비밀성을 지원하지 [않습니다](https://getsession.org/blog/session-protocol-technical-information). 즉, '암호화 시스템이 자동으로 빈번하게 암호화 및 복호화에 사용되는 키를 변경하여, 최신 키가 손상되더라도 민감한 정보는 일부만 노출되게 하는 시스템'이 존재하지 않습니다.

Oxen은 2020년 3월에 Session의 제3자 감사를 요청했습니다. 감사는 2021년 4월에 [완료되었으며](https://getsession.org/session-code-audit), "이 애플리케이션의 전반적인 보안 수준은 양호하며, 프라이버시를 중시하는 사람들이 사용하기에 적합합니다"라는 결론이 내려졌습니다.

Session은 애플리케이션 및 프로토콜의 기술적인 설명을 담은 [백서](https://arxiv.org/pdf/2002.04609.pdf)를 제공하고 있습니다.

## 평가 기준

**Privacy Guides는 권장 목록의 어떠한 프로젝트와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

<div class="admonition example" markdown>
<p class="admonition-title">This section is new</p>

Privacy Guides 팀은 사이트의 모든 항목마다 명확한 평가 기준을 정립하는 중이며, 따라서 세부 내용은 변경될 수 있습니다. 평가 기준에 대해서 질문이 있다면 [포럼에서 문의](https://discuss.privacyguides.net/latest)하시기 바랍니다. (무언가가 목록에 존재하지 않다고 해서 권장 목록을 작성할 때 고려한 적이 없을 것으로 단정 짓지 마세요.) 권장 목록에 어떤 프로젝트를 추가할 때 고려하고 논의해야 할 요소는 매우 많으며, 모든 요소를 문서화하는 것은 현재 진행 중인 작업입니다.

</div>

- 오픈 소스 클라이언트가 있어야 합니다.
- 비공개 메시지에는 E2EE가 기본 적용이어야 합니다.
- 모든 메시지에 E2EE가 지원되어야 합니다.
- 독립적인 감사를 받았어야 합니다.

### 우대 사항

평가 기준에서 '우대 사항'은 해당 부문에서 완벽한 프로젝트에 기대하는 바를 나타냅니다. 다음의 우대 사항에 해당하지 않더라도 권장 목록에 포함될 수 있습니다. 단, 우대 사항에 해당할수록 이 페이지의 다른 항목보다 높은 순위를 갖습니다.

- Should have Forward Secrecy.
- 오픈 소스 서버가 있어야 합니다.
- 탈중앙 방식(연합 방식/P2P 방식)이어야 합니다.
- 모든 메시지에 E2EE가 기본 적용이어야 합니다.
- Linux, macOS, Windows, Android, iOS를 지원해야 합니다.
