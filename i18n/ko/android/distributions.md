---
meta_title: "최고의 안드로이드 운영 체제 - 프라이버시 가이드"
title: 대체 배포판
description: 안드로이드 휴대폰의 운영 체제를 안전하고 프라이버시를 존중하는 다음 대안으로 교체할 수 있습니다.
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: 프라이버시 중심 안드로이드 운영 체제
    url: "./"
  - "@context": http://schema.org
    "@type": CreativeWork
    name: 그래핀OS
    image: /assets/img/android/grapheneos.svg
    url: https://grapheneos.org/
    sameAs: https://en.wikipedia.org/wiki/GrapheneOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
robots: nofollow, max-snippet:-1, max-image-preview:large
---

<small>다음 위협으로부터 보호합니다:</small>

- [:material-target-account: 표적 공격](../basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: 수동적 공격](../basics/common-threats.md#security-and-privacy){ .pg-orange }

**안드로이드 기반 커스텀 운영 체제**(**커스텀 롬**이라고도 함)는 기기의 프라이버시와 보안 수준을 높이는 방법이 될 수 있습니다. 이는 휴대폰 출고 시 기본으로 탑재되어 있으며 구글 플레이 서비스는 물론 다른 제조사 소프트웨어와도 깊게 통합되어 있는 경우가 많은 "순정" 안드로이드와 대비됩니다.

구글 픽셀을 사용하고 있다면 향상된 보안 강화와 추가적인 프라이버시 기능을 제공하는 그래핀OS를 설치할 것을 권장합니다. 다른 운영 체제나 기기를 소개하지 않는 이유는 다음과 같습니다:

- [보안이 더 취약한](index.md#install-a-custom-distribution) 경우가 많습니다.
- 관리자가 흥미를 잃거나 자신의 기기를 바꾸면 지원이 중단되는 경우가 잦습니다. 이는 예측 가능한 [지원 주기](https://grapheneos.org/faq#device-lifetime)를 따르는 그래핀OS와 대조적입니다.
- 대체로 설치할 만한 가치가 있을 정도의 주목할 만한 프라이버시 또는 보안 개선 사항이 거의 또는 전혀 없습니다.

## 그래핀OS { #grapheneos }

<div class="admonition recommendation" markdown>

![그래핀OS 로고](../assets/img/android/grapheneos.svg#only-light){ align=right }
![그래핀OS 로고](../assets/img/android/grapheneos-dark.svg#only-dark){ align=right }

프라이버시와 보안 측면에서 **그래핀OS**는 최고의 선택입니다.

그래핀OS는 추가적인 [보안 강화](https://en.wikipedia.org/wiki/Hardening_(computing))와 프라이버시 개선 기능을 제공합니다. [강화된 메모리 할당자](https://github.com/GrapheneOS/hardened_malloc), 네트워크 및 센서 권한, 그 밖의 다양한 [보안 기능](https://grapheneos.org/features)을 갖추고 있습니다. 또한 그래핀OS는 완전한 펌웨어 업데이트와 서명된 빌드를 제공하므로 자체 검사 부팅을 완벽하게 지원합니다.

[:octicons-home-16: 홈페이지](https://grapheneos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://grapheneos.org/faq#privacy-policy){ .card-link title="개인정보 처리방침" }
[:octicons-info-16:](https://grapheneos.org/faq){ .card-link title="문서" }
[:octicons-code-16:](https://grapheneos.org/source){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title="후원하기" }

</div>

그래핀OS는 [샌드박스 구글 플레이](https://grapheneos.org/usage#sandboxed-google-play)를 지원하며, 이를 통해 구글 플레이 서비스를 다른 일반 앱과 마찬가지로 완전한 샌드박스 환경에서 실행합니다. 덕분에 푸시 알림 등 구글 플레이 서비스 대부분의 기능을 활용하면서도 권한과 접근을 완전히 통제할 수 있으며, 원하는 특정 [직장 프로필](../os/android-overview.md#work-profile)이나 [사용자 프로필](../os/android-overview.md#user-profiles) 안에만 가둬 둘 수 있습니다.

현재 그래핀OS의 [하드웨어 보안 요구 사항](https://grapheneos.org/faq#future-devices)을 충족하는 기기는 [구글 픽셀 휴대폰](../mobile-phones.md#google-pixel)뿐입니다. 픽셀 8 이후 모델은 ARM의 메모리 태깅 확장(MTE)을 지원합니다. MTE는 메모리 손상 버그를 통한 익스플로잇 발생 가능성을 대폭 낮춰 주는 하드웨어 보안 강화 기능입니다. 그래핀OS는 지원 기기에서 MTE의 적용 범위를 크게 확장합니다. 순정 OS에서는 개발자 옵션이나 구글의 고급 보호 프로그램을 통해서만 제한적인 MTE 구현을 선택적으로 활성화할 수 있는 반면, 그래핀OS는 시스템 커널, 기본 시스템 구성 요소, 그리고 자체 웹 브라우저인 바나듐과 그 웹뷰에 더 강력한 MTE 구현을 기본으로 적용합니다.

그래핀OS는 사용자가 설치한 모든 앱에 MTE를 활성화하는 전역 설정도 제공하며, :gear: **설정** → **보안 및 개인 정보 보호** → **익스플로잇 보호**(Exploit protection) → **메모리 태깅**(Memory tagging) → **기본적으로 사용**(Enable by default)에서 설정할 수 있습니다. 또한 호환성 문제로 충돌할 수 있는 앱을 위해 앱별로 MTE를 해제할 수 있는 설정도 제공합니다.

### 연결 확인 { #connectivity-checks }

기본적으로 안드로이드는 DNS 연결 확인, 현재 네트워크 시간 동기화, 네트워크 연결 상태 확인을 비롯한 여러 백그라운드 작업을 위해 구글과 다수의 네트워크 연결을 맺습니다. 그래핀OS는 이러한 연결을 그래핀OS가 운영하며 그래핀OS의 개인정보 처리방침이 적용되는 서버로의 연결로 대체합니다. 이를 통해 IP 주소 같은 정보를 [구글로부터](../basics/common-threats.md#privacy-from-service-providers) 숨길 수 있지만, 네트워크 관리자나 ISP는 사용자가 `grapheneos.network`, `grapheneos.org` 등에 연결하고 있다는 사실을 쉽게 확인하고 어떤 운영 체제를 사용하는지 추론할 수 있습니다.

네트워크상의 공격자나 ISP로부터 이러한 정보를 숨기고 싶다면, 연결 확인 설정을 **Standard (Google)** 옵션으로 변경하는 것과 함께 [신뢰할 수 있는 VPN](../vpn.md)을 **반드시** 사용해야 합니다. :gear: **설정** → **네트워크 및 인터넷** → **인터넷 연결 확인**(Internet connectivity checks)에서 찾을 수 있습니다. 이 옵션을 사용하면 연결 확인 시 구글 서버에 연결하므로, VPN과 함께 사용하면 더 많은 안드로이드 기기 사이에 섞여 눈에 띄지 않게 할 수 있습니다.

## 평가 기준 { #criteria }

**프라이버시 가이드는 추천하는 어떠한 프로젝트와도 제휴 관계가 없습니다.** [표준 평가 기준](../about/criteria.md)에 더해, 객관적인 추천을 제공할 수 있도록 명확한 요구 사항을 마련했습니다. 프로젝트를 선택해 사용하기 전에 이 목록을 숙지하고, 직접 조사하여 자신에게 맞는 선택인지 확인하시기 바랍니다.

- 오픈 소스 소프트웨어여야 합니다.
- 사용자 지정 AVB 키를 이용한 부트로더 잠금을 지원해야 합니다.
- 안드로이드 메이저 업데이트가 출시된 후 0~1개월 이내에 적용되어야 합니다.
- 안드로이드 기능 업데이트(마이너 버전)가 출시된 후 0~14일 이내에 적용되어야 합니다.
- 정기 보안 패치가 출시된 후 0~5일 이내에 적용되어야 합니다.
- 출고 시점부터 "루팅"된 상태여서는 **안 됩니다**.
- 구글 플레이 서비스가 기본적으로 활성화되어 있어서는 **안 됩니다**.
- 구글 플레이 서비스를 지원하기 위해 시스템을 수정할 필요가 **없어야** 합니다.
