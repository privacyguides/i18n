---
meta_title: "최고의 프라이버시 보호 메신저 - 프라이버시 가이드"
title: 실시간 커뮤니케이션
icon: material/chat-processing
description: 시그널, 심플렉스 같은 암호화 메신저는 민감한 대화를 엿보는 눈으로부터 안전하게 지켜 줍니다.
cover: real-time-communication.webp
---

<small>다음 위협으로부터 보호합니다:</small>

- [:material-bug-outline: 수동적 공격](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: 서비스 제공업체](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}
- [:material-eye-outline: 대규모 감시](basics/common-threats.md#mass-surveillance-programs ""){.pg-blue}
- [:material-account-cash: 감시 자본주의](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

암호화된 **실시간 커뮤니케이션**에 대한 이 추천 앱은 민감한 대화를 안전하게 지키는 데 매우 유용합니다. 이러한 메신저는 다양한 [통신 네트워크 유형](advanced/communication-network-types.md)으로 제공됩니다.

[:material-movie-open-play-outline: 동영상: 이제 SMS 사용을 그만둘 때입니다](https://www.privacyguides.org/videos/2025/01/24/its-time-to-stop-using-sms-heres-why ""){.md-button}

## 시그널 { #signal }

<div class="admonition recommendation" markdown>

![시그널 로고](assets/img/messengers/signal.svg){ align=right }

**시그널**은 시그널 메신저 LLC가 개발한 모바일 앱입니다. 이 앱은 순방향 비밀성[^1]과 침해 후 보안(post-compromise security)을 지원하는 매우 안전한 암호화 프로토콜인 시그널 프로토콜로 보호되는 메시지와 통화를 제공합니다.[^2]

[:octicons-home-16: 홈페이지](https://signal.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://signal.org/legal/#privacy-policy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://support.signal.org){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/signalapp){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://signal.org/donate){ .card-link title="후원하기" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=org.thoughtcrime.securesms)
- [:simple-appstore: 앱 스토어](https://apps.apple.com/app/id874139669)
- [:simple-github: 깃허브](https://github.com/signalapp/Signal-Android/releases)
- [:simple-android: 안드로이드](https://signal.org/android/apk)
- [:fontawesome-brands-windows: 윈도우](https://signal.org/download/windows)
- [:simple-apple: macOS](https://signal.org/download/macos)
- [:simple-linux: 리눅스](https://signal.org/download/linux)

</details>

</div>

시그널은 가입할 때 전화번호가 필요하지만, 연락처에 전화번호를 숨기려면 사용자 이름을 만들어야 합니다:

1. 시그널에서 앱 설정을 열고 맨 위의 계정 프로필을 탭하세요.
2. **사용자 이름**(Username)을 탭하고 "시그널 사용자 이름 설정"(Set up your Signal username) 화면에서 **계속**(Continue)을 선택하세요.
3. 사용자 이름을 입력하세요. 사용자 이름은 고유성을 유지하고 다른 사람이 추측하지 못하도록 항상 고유한 숫자 조합과 짝을 이룹니다. 예를 들어 "John"을 입력하면 사용자 이름은 `@john.35`처럼 될 수 있습니다. 기본적으로 사용자 이름을 만들 때 숫자 2자리가 붙지만, 사용자 이름 길이 제한(32자)에 도달할 때까지 숫자를 더 추가할 수 있습니다.
4. 앱 설정 메인 페이지로 돌아가 **개인정보 보호**(Privacy)를 선택하세요.
5. **전화번호**(Phone Number)를 선택하세요.
6. **내 전화번호를 볼 수 있는 사람**(Who Can See My Number) 설정을 **아무도 없음**(Nobody)으로 변경하세요.
7. (선택 사항) 이미 여러분의 전화번호를 알고 있는 사람이 시그널 계정/사용자 이름을 찾지 못하게 하려면 **전화번호로 나를 찾을 수 있는 사람**(Who Can Find Me By Number) 설정도 **아무도 없음**(Nobody)으로 변경하세요

시그널 설정과 보안 강화에 관한 추가 팁도 준비해 두었습니다:

[시그널 설정 및 보안 강화 :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/07/07/signal-configuration-and-hardening)

시그널의 연락처 목록은 시그널 PIN으로 암호화되며 서버는 이에 접근할 수 없습니다. 개인 프로필도 암호화되며, 대화하는 연락처와만 공유됩니다.

시그널은 서버에 그룹 멤버십, 그룹 이름, 그룹 아바타, 그룹 속성에 대한 기록이 남지 않는 [비공개 그룹](https://signal.org/blog/signal-private-group-system)을 지원합니다. [봉인된 발신자(Sealed Sender)](https://signal.org/blog/sealed-sender)를 활성화하면 시그널의 메타데이터는 최소화됩니다. 발신자 주소가 메시지 본문과 함께 암호화되며, 서버에는 수신자 주소만 보입니다. 봉인된 발신자는 연락처 목록에 있는 사람에게만 활성화되지만, 스팸을 받을 위험이 커지는 대신 모든 수신자에게 활성화할 수도 있습니다.

이 프로토콜은 2016년에 독립적인 [감사](https://eprint.iacr.org/2016/1013.pdf)를 받았습니다. 시그널 프로토콜의 사양은 시그널 [문서](https://signal.org/docs)에서 확인할 수 있습니다.

### 몰리(안드로이드) { #molly-android }

안드로이드를 사용하고 있고 위협 모델상 [:material-target-account: 표적 공격](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}에 대비해야 한다면, 여러 보안 및 사용성 개선 사항을 갖춘 이 대체 앱으로 시그널 네트워크를 이용하는 것을 고려해 볼 수 있습니다.

<div class="admonition recommendation" markdown>

![몰리 로고](assets/img/messengers/molly.svg){ align=right }

**몰리**는 안드로이드용 대체 시그널 클라이언트로, 로컬 데이터베이스를 패스프레이즈로 암호화하여 저장하고, 사용하지 않는 RAM 데이터를 안전하게 파쇄하며, 토르를 통해 연결을 라우팅하는 등 [다양한 기능](https://www.privacyguides.org/articles/2022/07/07/signal-configuration-and-hardening#privacy-and-security-features)을 제공합니다. 또한 예약 백업, 자동 잠금, 안드로이드 휴대폰을 시그널 계정의 주 기기가 아닌 연결된 기기로 사용하는 기능 등 사용성 개선 사항도 갖추고 있습니다.

[:octicons-home-16: 홈페이지](https://molly.im){ .md-button .md-button--primary }
[:octicons-eye-16:](https://signal.org/legal/#privacy-policy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://github.com/mollyim/mollyim-android/wiki){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/mollyim/mollyim-android){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://opencollective.com/mollyim){ .card-link title="후원하기" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-fdroid: F-Droid](https://molly.im/fdroid)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/im.molly.app)
- [:simple-github: 깃허브](https://github.com/mollyim/mollyim-android/releases)

</details>

</div>

몰리를 사용하면 안전하고 시기적절한 업데이트를 제공받기 위해 시그널 팀*과* 몰리 팀을 모두 신뢰해야 하므로, 여러 주체를 신뢰하게 된다는 점에 유의하세요.

몰리는 [재현 가능한 빌드](https://github.com/mollyim/mollyim-android/tree/main/reproducible-builds)를 지원하므로, 컴파일된 APK가 소스 코드와 일치하는지 확인할 수 있습니다.

## 심플렉스 챗 { #simplex-chat }

<div class="admonition recommendation" markdown>

![심플렉스 챗 로고](assets/img/messengers/simplex.svg){ align=right }

**심플렉스 챗**은 전화번호나 사용자 이름 같은 고유 식별자에 의존하지 않는 메신저입니다. 탈중앙화 네트워크 덕분에 심플렉스 챗은 [:material-close-outline: 검열](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }에 맞서는 효과적인 도구가 됩니다.

[:octicons-home-16: 홈페이지](https://simplex.chat){ .md-button .md-button--primary }
[:octicons-eye-16:](https://simplex.chat/privacy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://simplex.chat/docs/simplex.html){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/simplex-chat){ .card-link title="소스 코드" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=chat.simplex.app)
- [:simple-appstore: 앱 스토어](https://apps.apple.com/app/id1605771084)
- [:simple-github: 깃허브](https://github.com/simplex-chat/simplex-chat/releases)
- [:fontawesome-brands-windows: 윈도우](https://simplex.chat/downloads/#desktop-app)
- [:simple-apple: macOS](https://simplex.chat/downloads/#desktop-app)
- [:simple-linux: 리눅스](https://simplex.chat/downloads/#desktop-app)
- [:simple-flathub: Flathub](https://flathub.org/en/apps/chat.simplex.simplex)

</details>

</div>

심플렉스 챗은 양자 내성을 갖춘 더블 래칫 암호화를 사용하는 [심플렉스 메시징 프로토콜](https://github.com/simplex-chat/simplexmq/blob/stable/protocol/simplex-messaging.md)로 보호되는 1:1 메시지, 그룹 채팅, E2EE 통화를 제공합니다. 또한 심플렉스 챗은 메시지를 전달하는 데 단방향 ["심플렉스 큐"](https://github.com/simplex-chat/simplexmq/blob/stable/protocol/simplex-messaging.md#simplex-queue)를 사용하여 메타데이터를 보호합니다.

심플렉스 챗에서 대화에 참여하려면 QR 코드를 스캔하거나 초대 링크를 클릭해야 합니다. 이를 통해 별도의 채널로 연락처를 확인할 수 있으므로, 네트워크 제공업체의 중간자 공격을 막을 수 있습니다. 데이터를 백업하는 중앙 서버가 없으므로, 데이터를 내보내 다른 기기로 가져올 수 있습니다.

심플렉스 챗에 구현된 프라이버시 및 보안 [기능](https://github.com/simplex-chat/simplex-chat#privacy-and-security-technical-details-and-limitations)의 전체 목록은 앱의 저장소에서 확인할 수 있습니다.

심플렉스 챗은 [2024년 7월](https://simplex.chat/blog/20241014-simplex-network-v6-1-security-review-better-calls-user-experience.html#simplex-cryptographic-design-review-by-trail-of-bits)과 [2022년 10월](https://simplex.chat/blog/20221108-simplex-chat-v4.2-security-audit-new-website)에 독립적인 감사를 받았습니다.

## 브라이어 { #briar }

<div class="admonition recommendation" markdown>

![브라이어 로고](assets/img/messengers/briar.svg){ align=right }

**브라이어**는 [토르 네트워크](alternative-networks.md#tor)를 사용해 다른 클라이언트와 [연결](https://briarproject.org/how-it-works)되는 암호화 메신저로, [:material-close-outline: 검열](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray } 우회에 효과적인 도구입니다. 브라이어는 가까운 거리에 있을 때 와이파이나 블루투스로도 연결할 수 있습니다. 브라이어의 로컬 메시 모드는 인터넷을 사용하기 어려운 상황에서 유용할 수 있습니다.

[:octicons-home-16: 홈페이지](https://briarproject.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://briarproject.org/privacy-policy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://code.briarproject.org/briar/briar/-/wikis/home){ .card-link title="문서" }
[:octicons-code-16:](https://code.briarproject.org/briar/briar){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://code.briarproject.org/briar/briar#donate){ .card-link title="후원하기" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=org.briarproject.briar.android)
- [:fontawesome-brands-windows: 윈도우](https://briarproject.org/download-briar-desktop)
- [:simple-linux: 리눅스](https://briarproject.org/download-briar-desktop)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.briarproject.Briar)

</details>

</div>

브라이어에서 연락처를 추가하려면 서로 먼저 상대방을 추가해야 합니다. `briar://` 링크를 교환하거나, 가까이 있다면 상대방의 QR 코드를 스캔할 수 있습니다.

브라이어는 [사양을 완전히 공개](https://code.briarproject.org/briar/briar-spec)하고 있습니다. 브라이어는 브램블 [핸드셰이크](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BHP.md) 및 [전송](https://code.briarproject.org/briar/briar-spec/blob/master/protocols/BTP.md) 프로토콜을 사용해 순방향 비밀성[^1]을 지원합니다.

클라이언트 소프트웨어는 독립적인 [감사](https://briarproject.org/news/2017-beta-released-security-audit)를 받았으며, 익명 라우팅 프로토콜은 마찬가지로 감사를 받은 토르 네트워크를 사용합니다.

## 평가 기준 { #criteria }

**프라이버시 가이드는 추천하는 어떠한 프로젝트와도 제휴 관계가 없습니다.** [표준 평가 기준](about/criteria.md)에 더해, 객관적인 추천을 제공할 수 있도록 명확한 요구 사항을 마련했습니다. 프로젝트를 선택해 사용하기 전에 이 목록을 숙지하고, 직접 조사하여 자신에게 맞는 선택인지 확인하시기 바랍니다.

### 최소 요구 사항 { #minimum-requirements }

- 클라이언트가 오픈 소스여야 합니다.
- 연락처와 개인 식별자(특히 전화번호나 이메일)를 공유하도록 요구해서는 안 됩니다.
- 비공개 메시지에 기본적으로 E2EE를 사용해야 합니다.
- 모든 메시지에 E2EE를 지원해야 합니다.
- 순방향 비밀성[^1]을 지원해야 합니다
- 평판이 좋은 독립적인 제3자의 감사 결과가 공개되어 있어야 합니다.

### 우대 사항 { #best-case }

우대 사항은 이 카테고리에서 완벽한 프로젝트라면 갖추었으면 하는 사항을 나타냅니다. 추천 항목에 이 기능 중 일부 또는 전부가 없을 수도 있지만, 이러한 기능을 갖춘 항목은 이 페이지에서 다른 항목보다 높은 순위에 오를 수 있습니다.

- 미래 비밀성(침해 후 보안)[^2]을 지원하는 것이 좋습니다
- 서버가 오픈 소스인 것이 좋습니다.
- 탈중앙화 네트워크, 즉 [연합형 또는 P2P](advanced/communication-network-types.md) 네트워크를 사용하는 것이 좋습니다.
- 모든 메시지에 기본적으로 E2EE를 사용하는 것이 좋습니다.
- 리눅스, macOS, 윈도우, 안드로이드, iOS를 지원하는 것이 좋습니다.

[^1]: [순방향 비밀성](https://en.wikipedia.org/wiki/Forward_secrecy)이란 키를 매우 자주 교체하여, 현재 암호화 키가 유출되더라도 **과거** 메시지까지 노출되지 않도록 하는 것입니다.
[^2]: 미래 비밀성(또는 [침해 후 보안](https://eprint.iacr.org/2016/221.pdf))이란 공격자가 개인 키를 탈취한 후에도, 이후의 세션 키까지 추가로 탈취하지 않는 한 **향후** 메시지를 복호화하지 못하도록 막는 기능입니다. 공격자는 가로채지 못한 키 교환이 일어나는 즉시 접근 권한을 잃게 되므로, 사실상 당사자 간의 모든 통신을 가로챌 수밖에 없게 됩니다.
