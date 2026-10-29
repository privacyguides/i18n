---
title: 다중 인증
icon: material/two-factor-authentication
description: 이 도구는 비밀 정보를 제3자에게 보내지 않고도 다중 인증으로 인터넷 계정을 보호할 수 있도록 도와줍니다.
cover: multi-factor-authentication.webp
---

<small>다음 위협으로부터 보호합니다:</small>

- [:material-target-account: 표적 공격](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

<div class="admonition note" markdown>
<p class="admonition-title">하드웨어 키</p>

[하드웨어 보안 키 추천](security-keys.md)은 별도 카테고리로 이동했습니다.

</div>

**다중 인증 앱**은 국제 인터넷 표준화 기구(IETF)가 채택한 **시간 기반 일회용 비밀번호**, 즉 **TOTP**라는 보안 표준을 구현합니다. 이는 웹사이트가 여러분과 비밀을 공유하고, 인증 앱이 이 비밀을 사용해 현재 시간을 기반으로 (보통) 6자리 코드를 생성하면, 로그인할 때 이 코드를 입력해 웹사이트가 확인하는 방식입니다. 일반적으로 이 코드는 30초마다 새로 생성되며, 새 코드가 생성되면 이전 코드는 쓸모없게 됩니다. 해커가 6자리 코드 하나를 손에 넣더라도, 그 코드를 역산해 원래 비밀을 알아내거나 향후 코드를 예측할 방법은 없습니다.

안드로이드와 iOS는 대부분의 데스크톱 운영 체제보다 보안과 앱 격리가 뛰어나므로, 데스크톱용 대안 대신 모바일 TOTP 앱을 사용할 것을 강력히 권장합니다.

## 엔테 오스 { #ente-auth }

<div class="admonition recommendation" markdown>

![엔테 오스 로고](assets/img/multi-factor-authentication/ente-auth.svg){ align=right }

**엔테 오스**는 TOTP 토큰을 저장하고 생성하는 자유 오픈 소스 앱입니다. 온라인 계정과 함께 사용하면 종단 간 암호화된 안전한 방식으로 기기 간에 토큰을 백업하고 동기화할 수 있습니다(웹 인터페이스로 접근할 수도 있습니다). 계정 없이 단일 기기에서 오프라인으로 사용할 수도 있습니다.

[:octicons-home-16: Homepage](https://ente.com/auth){ .md-button .md-button--primary } [:octicons-eye-16:](https://ente.com/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://ente.com/help/auth){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/ente/ente/tree/main/mobile/apps/auth){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=io.ente.auth)
- [:simple-appstore: 앱 스토어](https://apps.apple.com/app/id6444121398)
- [:simple-github: 깃허브](https://github.com/ente-io/ente/releases?q=auth)
- [:octicons-browser-16: 웹](https://auth.ente.io)

</details>

</div>

(온라인 계정과 함께 사용하는 경우) 엔테 오스의 기반이 되는 서버 측 소스 코드와 인프라는 2025년 10월 [Cure53](https://ente.com/blog/cern-audit)의 감사를 받았습니다.

## 이지스 오센티케이터(안드로이드) { #aegis-authenticator-android }

<div class="admonition recommendation" markdown>

![이지스 로고](assets/img/multi-factor-authentication/aegis.png){ align=right }

**이지스 오센티케이터**는 온라인 서비스의 2단계 인증 토큰을 관리하는 안드로이드용 자유 오픈 소스 앱입니다. 이지스 오센티케이터는 완전히 오프라인/로컬로 작동하지만, 다른 많은 대안과 달리 백업을 위해 토큰을 내보내는 옵션을 제공합니다.

[:octicons-home-16: 홈페이지](https://getaegis.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://getaegis.app/aegis/privacy.html){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://github.com/beemdevelopment/Aegis/wiki){ .card-link title="문서" }
[:octicons-code-16:](https://github.com/beemdevelopment/Aegis){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://buymeacoffee.com/beemdevelopment){ .card-link title="후원하기" }

<details class="downloads" markdown>
<summary>다운로드</summary>

- [:simple-googleplay: 구글 플레이](https://play.google.com/store/apps/details?id=com.beemdevelopment.aegis)
- [:simple-github: 깃허브](https://github.com/beemdevelopment/Aegis/releases)

</details>

</div>

## 평가 기준 { #criteria }

**프라이버시 가이드는 추천하는 어떠한 프로젝트와도 제휴 관계가 없습니다.** [표준 평가 기준](about/criteria.md)에 더해, 객관적인 추천을 제공할 수 있도록 명확한 요구 사항을 마련했습니다. 프로젝트를 선택해 사용하기 전에 이 목록을 숙지하고, 직접 조사하여 자신에게 맞는 선택인지 확인하시기 바랍니다.

- 소스 코드가 공개되어 있어야 합니다.
- 인터넷 연결이 필수여서는 안 됩니다.
- 클라우드 동기화는 선택 사항이어야 하며, 동기화 기능이 있다면 E2EE로 보호되어야 합니다.
