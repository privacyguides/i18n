---
title: "이메일 별칭"
icon: material/email-lock
description: 이메일 별칭 서비스를 사용하면 가입하는 웹사이트마다 새 이메일 주소를 쉽게 생성할 수 있습니다.
cover: email-aliasing.webp
---

<small>다음 위협으로부터 보호합니다:</small>

- [:material-account-cash: 감시 자본주의](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }
- [:material-account-search: 공개 노출](basics/common-threats.md#limiting-public-information){ .pg-green }

**이메일 별칭 서비스**를 사용하면 가입하는 웹사이트마다 새 이메일 주소를 쉽게 생성할 수 있습니다. 생성한 이메일 별칭으로 온 메일은 여러분이 선택한 이메일 주소로 전달되므로, "주" 이메일 주소와 [이메일 제공업체](email.md)를 모두 숨길 수 있습니다.

이메일 별칭은 이메일 제공업체가 운영을 중단할 경우에 대비한 안전장치 역할도 할 수 있습니다. 그런 상황에서는 별칭을 새 이메일 주소로 쉽게 다시 연결할 수 있습니다. 하지만 그 대신 별칭 서비스가 계속 운영될 것이라고 신뢰해야 합니다.

## 장점 { #benefits }

이메일 별칭을 개별적으로 관리할 수 있는 서비스를 사용하면 기존의 메일함 관리/필터링 방식에 비해 여러 장점이 있습니다:

### 플러스 주소 방식 대비 { #over-plus-addressing }

많은 제공업체가 흔히 지원하는 플러스 주소 방식은 `yourname+[anythinghere]@example.com` 같은 별칭을 만들 수 있게 해 주지만, 웹사이트, 광고주, 추적 네트워크가 `+` 기호 뒤의 내용을 손쉽게 제거할 수 있으므로 진정한 이메일 별칭이 더 좋습니다. [IAB](https://en.wikipedia.org/wiki/Interactive_Advertising_Bureau) 같은 단체는 사용자의 프라이버시 의사와 관계없이 이메일 주소를 연관 짓고 추적할 수 있도록 광고주에게 [이메일 주소를 정규화](https://shkspr.mobi/blog/2023/01/the-iab-loves-tracking-users-but-it-hates-users-tracking-them)할 것을 요구합니다.

### 캐치올 별칭 대비 { #over-catch-all-aliases }

전용 이메일 별칭 서비스를 사용하면 사용자 지정 도메인의 캐치올 별칭에 비해 여러 장점이 있습니다:

- 필요할 때 별칭을 개별적으로 켜고 끌 수 있어, 웹사이트가 무작위로 이메일을 보내는 것을 막을 수 있습니다.
- 답장이 별칭 주소에서 발송되므로 실제 이메일 주소가 보호됩니다.

### 임시 이메일 서비스 대비 { #over-temporary-email-services }

이메일 별칭 서비스는 "임시 이메일" 서비스에 비해서도 여러 장점이 있습니다:

- 별칭은 영구적이며, 비밀번호 재설정 메일 같은 것을 받아야 할 때 다시 켤 수 있습니다.
- 이메일은 별칭 제공업체에 저장되지 않고 여러분이 신뢰하는 메일함으로 전송됩니다.
- 임시 이메일 서비스는 일반적으로 주소를 아는 누구나 접근할 수 있는 공개 메일함을 사용하지만, 별칭은 여러분만 사용할 수 있습니다.

## 추천 제공업체 { #recommended-providers }

<div class="grid cards" markdown>

- ![Addy.io 로고](assets/img/email-aliasing/addy.svg){ .twemoji } [Addy.io](email-aliasing.md#addyio)
- ![심플로그인 로고](assets/img/email-aliasing/simplelogin.svg){ .twemoji } [심플로그인](email-aliasing.md#simplelogin)

</div>

프라이버시 가이드가 추천하는 이메일 별칭 제공업체는 업체가 관리하는 도메인은 물론, 소정의 연간 요금으로 여러분의 사용자 지정 도메인에서도 별칭을 만들 수 있는 곳입니다. 최대한 통제하고 싶다면 자체 호스팅할 수도 있습니다. 하지만 사용자 지정 도메인을 사용하면 프라이버시 측면의 단점이 있을 수 있습니다. 여러분만 사용하는 사용자 지정 도메인이라면, 이메일 주소에서 `@` 기호 앞부분을 무시하고 도메인 이름만 봐도 웹사이트 전반에서 여러분의 활동을 쉽게 추적할 수 있습니다.

별칭 서비스를 사용하면 이메일 제공업체와 별칭 제공업체 모두에게 암호화되지 않은 메시지를 맡겨야 합니다. 일부 제공업체는 자동 PGP 암호화[^1]로 이 문제를 조금 완화합니다. 수신 이메일을 최종 메일함 제공업체에 전달하기 전에 암호화하므로, 신뢰해야 할 주체가 둘에서 하나로 줄어듭니다.

### Addy.io

<div class="admonition recommendation" markdown>

![Addy.io 로고](assets/img/email-aliasing/addy.svg){ align=right }

**Addy.io**에서는 공유 도메인에서 도메인 별칭 10개를 무료로 만들거나, ["표준" 별칭](https://addy.io/faq/#what-is-a-standard-alias)을 무제한으로 만들 수 있습니다.

[:octicons-home-16: 홈페이지](https://addy.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://addy.io/privacy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://addy.io/faq){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/anonaddy){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://addy.io/donate){ .card-link title="후원하기" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://addy.io/faq/#is-there-an-android-app)
- [:simple-appstore: 앱 스토어](https://addy.io/faq/#is-there-an-ios-app)
- [:simple-firefoxbrowser: 파이어폭스](https://addons.mozilla.org/firefox/addon/addy_io)
- [:simple-googlechrome: 크롬](https://chrome.google.com/webstore/detail/iadbdpnoknmbdeolbapdackdcogdmjpe)

</details>

</div>

만들 수 있는 공유 별칭(`@addy.io` 같은 공유 도메인으로 끝나는 별칭)의 수는 구독 중인 [요금제](https://addy.io/#pricing)에 따라 다릅니다. 이러한 요금제는 [암호화폐](https://addy.io/help/subscribing-with-cryptocurrency)로 결제하거나, Addy.io의 공식 재판매업체인 [프록시스토어](https://addy.io/help/voucher-codes)에서 바우처 코드를 구매할 수 있습니다.

유료 요금제에서는 `@[username].addy.io` 같은 도메인으로 끝나는 표준 별칭이나 사용자 지정 도메인 별칭을 무제한으로 만들 수 있습니다. 하지만 앞서 언급했듯이, 도메인 이름만으로도 표준 별칭을 손쉽게 서로 연결할 수 있으므로 프라이버시에 해로울 수 있습니다. 표준 별칭은 서비스가 공유 도메인을 차단하는 경우에 유용합니다.

시큐리텀은 2023년 9월 Addy.io를 [감사](https://addy.io/blog/addy-io-passes-independent-security-audit)했으며, 심각한 취약점은 [발견되지 않았습니다](https://addy.io/addy-io-security-audit.pdf).

주요 무료 기능:

- [x] 공유 별칭 10개
- [x] 표준 별칭 무제한
- [ ] 답장 발송 불가
- [x] 수신 메일함 1개
- [x] 자동 PGP 암호화[^1]

구독을 취소하더라도 결제 주기가 끝날 때까지는 유료 요금제의 기능을 계속 사용할 수 있습니다. 현재 결제 주기가 끝나면 (사용자 지정 도메인을 포함한) 대부분의 유료 기능이 [비활성화](https://addy.io/faq/#what-happens-if-i-have-a-subscription-but-then-cancel-it)되고, 유료 계정 설정이 기본값으로 되돌아가며, 캐치올이 비활성화되어 있었다면 다시 활성화됩니다.

### 심플로그인 { #simplelogin }

<div class="admonition recommendation" markdown>

![심플로그인 로고](assets/img/email-aliasing/simplelogin.svg){ align=right }

**심플로그인**은 다양한 공유 도메인 이름으로 이메일 별칭을 제공하는 무료 서비스로, 별칭 무제한이나 사용자 지정 도메인 같은 유료 기능도 선택적으로 제공합니다.

[:octicons-home-16: 홈페이지](https://simplelogin.io){ .md-button .md-button--primary }
[:octicons-eye-16:](https://simplelogin.io/privacy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://simplelogin.io/docs){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/simple-login){ .card-link title="소스 코드" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=io.simplelogin.android)
- [:simple-appstore: 앱 스토어](https://apps.apple.com/app/id1494359858)
- [:simple-github: 깃허브](https://github.com/simple-login/Simple-Login-Android/releases)
- [:simple-firefoxbrowser: 파이어폭스](https://addons.mozilla.org/firefox/addon/simplelogin)
- [:simple-googlechrome: 크롬](https://chrome.google.com/webstore/detail/dphilobhebphkdjbpfohgikllaljmgbn)
- [:fontawesome-brands-edge: 엣지](https://microsoftedge.microsoft.com/addons/detail/diacfpipniklenphgljfkmhinphjlfff)
- [:simple-safari: 사파리](https://apps.apple.com/app/id6475835429)

</details>

</div>

심플로그인은 2022년 4월 8일 [프로톤 AG에 인수](https://proton.me/news/proton-and-simplelogin-join-forces)되어, [프로톤 메일](email.md#proton-mail)을 주 메일함으로 사용하는 사용자에게 훌륭한 선택지가 되었습니다. 이 인수로 인해 이메일 서비스에 대해 단일 주체만 신뢰하면 됩니다. 심플로그인은 여전히 원하는 어떤 이메일 제공업체로든 메일을 전달할 수 있습니다.

설정에서 심플로그인 계정을 프로톤 계정과 연결할 수 있습니다. 프로톤 패스 플러스, 프로톤 언리미티드 또는 다중 사용자 프로톤 요금제를 사용하고 있다면 심플로그인 프리미엄을 무료로 이용할 수 있습니다. 마찬가지로 이제 심플로그인의 [무료 및 프리미엄 요금제](https://simplelogin.io/pricing/)에는 모두 프로톤 패스 구독이 포함됩니다. 공식 재판매업체인 [프록시스토어](https://simplelogin.io/faq)를 통해 심플로그인 프리미엄 바우처 코드를 익명으로 구매할 수도 있습니다.

시큐리텀은 2022년 초 심플로그인을 [감사](https://simplelogin.io/blog/security-audit)했으며, 모든 문제가 [해결되었습니다](https://simplelogin.io/audit2022/web.pdf).

주요 무료 기능:

- [x] 공유 별칭 10개
- [x] 답장 무제한
- [x] 수신 메일함 1개
- [ ] 자동 PGP 암호화[^1]는 유료 요금제에서만 사용 가능

구독이 끝나더라도 만들어 둔 모든 별칭으로 이메일을 계속 주고받을 수 있습니다. 하지만 무료 요금제 한도를 넘는 새 별칭을 만들거나, 새 도메인, 디렉터리, 메일함을 추가할 수는 없습니다.

## 평가 기준 { #criteria }

**프라이버시 가이드는 추천하는 어떠한 제공업체와도 제휴 관계가 없습니다.** [표준 평가 기준](about/criteria.md)에 더해, 이메일 별칭 제공업체도 해당되는 경우 일반 [이메일 제공업체 평가 기준](email.md#criteria)과 같은 기준으로 평가합니다. 이메일 별칭 서비스를 선택하기 전에 이 목록을 숙지하고, 직접 조사하여 선택한 제공업체가 자신에게 맞는지 확인하시기 바랍니다.

[^1]: 자동 PGP 암호화를 사용하면 암호화되지 않은 수신 이메일이 메일함으로 전달되기 전에 암호화되므로, 주 메일함 제공업체가 암호화되지 않은 이메일 내용을 볼 수 없습니다.
