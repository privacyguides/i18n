---
title: "안드로이드"
description: 프라이버시를 침해하는 안드로이드 기본 기능을 프라이버시를 보호하고 안전한 대안으로 교체하는 방법에 대한 조언입니다.
icon: 'simple/android'
cover: android.webp
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: 안드로이드 추천
    url: "./"
  - "@context": http://schema.org
    "@type": CreativeWork
    name: 안드로이드
    image: /assets/img/android/android.svg
    url: https://source.android.com/
    sameAs: https://en.wikipedia.org/wiki/Android_(operating_system)
---

![안드로이드 로고](../assets/img/android/android.svg){ align=right }

**안드로이드 오픈 소스 프로젝트**(AOSP)는 구글이 주도하는 오픈 소스 모바일 운영 체제로, 전 세계 모바일 기기 대부분에서 사용되고 있습니다. 안드로이드가 탑재되어 판매되는 휴대폰 대부분은 구글 플레이 서비스 같은 침해적인 통합 기능과 앱이 포함되도록 수정되어 있으므로, 휴대폰에 기본 설치된 시스템을 이러한 침해적인 기능이 없는 안드로이드 버전으로 교체하면 모바일 기기의 프라이버시를 크게 향상할 수 있습니다.

[안드로이드 개요 :material-arrow-right-drop-circle:](../os/android-overview.md){ .md-button .md-button--primary }

## 권장 사항 { #our-advice }

### 구글 서비스 대체하기 { #replace-google-services }

안드로이드에서는 구글 플레이를 거치지 않고도 앱을 받을 수 있는 방법이 다양하게 있습니다. 가능하다면 프라이버시가 보장되지 않는 출처에서 앱을 받기 전에 다음 방법 중 하나를 먼저 사용해 보세요:

[애플리케이션 받기 :material-arrow-right-drop-circle:](obtaining-apps.md){ .md-button }

카메라 앱처럼 휴대폰에 기본 설치된 앱에도 프라이버시를 보호하는 대안이 많이 있습니다. 이 사이트 전반에서 추천하는 안드로이드 앱 외에도, 유용하게 쓸 수 있는 안드로이드 전용 시스템 유틸리티 목록을 별도로 정리해 두었습니다.

[일반 앱 추천 :material-arrow-right-drop-circle:](general-apps.md){ .md-button }

### 커스텀 배포판 설치하기 { #install-a-custom-distribution }

안드로이드 휴대폰을 구매하면 기본 운영 체제에는 안드로이드 오픈 소스 프로젝트에 속하지 않는 앱과 기능이 함께 탑재되어 있습니다. 이러한 앱 중 상당수는—전화 앱처럼 기본적인 시스템 기능을 제공하는 앱조차도—구글 플레이 서비스와의 침해적인 통합을 필요로 합니다. 그리고 구글 플레이 서비스는 이러한 기본 시스템 앱과 다른 여러 앱이 애초에 작동할 수 있도록 기기의 파일, 연락처 저장소, 통화 기록, SMS 메시지, 위치, 카메라, 마이크 등 수많은 항목에 접근할 수 있는 권한을 요구합니다. 구글 플레이 서비스 같은 프레임워크는 기기의 공격 표면을 넓히며, 안드로이드에서 발생하는 각종 프라이버시 문제의 원인이 됩니다.

이 문제는 흔히 _커스텀 &#xB86C;_&#xC774;라 불리는, 이러한 침해적인 통합이 포함되지 않은 대체 안드로이드 배포판을 사용하여 해결할 수 있습니다. 안타깝게도 많은 커스텀 안드로이드 배포판은 AVB, 롤백 보호, 펌웨어 업데이트 등 중요한 보안 기능을 지원하지 않아 안드로이드 보안 모델을 위반하는 경우가 많습니다. 일부 배포판은 [ADB](https://developer.android.com/studio/command-line/adb)를 통해 루트 권한을 노출하고 디버깅 기능을 위해 [더 느슨한](https://github.com/LineageOS/android_system_sepolicy/search?q=userdebug&type=code) SELinux 정책이 필요한 [`userdebug`](https://source.android.com/setup/build/building#choose-a-target) 빌드를 배포하기도 하는데, 이로 인해 공격 표면은 더욱 넓어지고 보안 모델은 약해집니다.

커스텀 안드로이드 배포판을 선택할 때는 해당 배포판이 안드로이드 보안 모델을 준수하는지 확인하는 것이 이상적입니다. 최소한 해당 배포판은 프로덕션 빌드, AVB 지원, 롤백 보호, 시기적절한 펌웨어 및 운영 체제 업데이트, 그리고 [강제(enforcing) 모드](https://source.android.com/security/selinux/concepts#enforcement_levels)로 동작하는 SELinux를 갖추고 있어야 합니다. 프라이버시 가이드가 추천하는 안드로이드 배포판은 모두 이 기준을 충족합니다:

[추천 배포판 :material-arrow-right-drop-circle:](distributions.md){ .md-button }

### 루팅 피하기 { #avoid-root }

안드로이드 휴대폰을 [루팅](https://en.wikipedia.org/wiki/Rooting_(Android))하면 [안드로이드 보안 모델](https://en.wikipedia.org/wiki/Android_(operating_system)#Security_and_privacy) 전체가 약화되므로 보안이 크게 저하될 수 있습니다. 약화된 보안을 악용하는 익스플로잇이 발생하면 프라이버시 역시 저하될 수 있습니다. 일반적인 루팅 방식은 부트 파티션을 직접 변조하기 때문에 자체 검사 부팅을 정상적으로 수행할 수 없게 됩니다. 루트 권한이 필요한 앱은 시스템 파티션도 수정하므로, 자체 검사 부팅을 계속 비활성화한 상태로 두어야 합니다. 또한 사용자 인터페이스에 루트 권한이 직접 노출되면 기기의 공격 표면이 넓어지며, [권한 상승](https://en.wikipedia.org/wiki/Privilege_escalation) 취약점이나 SELinux 정책 우회에 악용될 수 있습니다.

[hosts 파일](https://en.wikipedia.org/wiki/Hosts_(file))을 수정하는 콘텐츠 차단기(애드어웨이 등)와 상시 루트 권한이 필요한 방화벽(AFWall+ 등)은 위험하므로 사용해서는 안 됩니다. 또한 이러한 앱은 본래의 목적을 달성하는 올바른 방법도 아닙니다. 콘텐츠 차단이 목적이라면 대신 암호화된 [DNS](../dns.md)나 VPN에서 제공하는 콘텐츠 차단 기능을 사용하는 것을 권장합니다. 트래커컨트롤과 비루트 모드의 애드어웨이는 (로컬 루프백 VPN을 사용하기 때문에) VPN 슬롯을 차지하므로, [오봇](../alternative-networks.md#orbot)이나 [실제 VPN 제공업체](../vpn.md) 같은 프라이버시 강화 서비스를 사용할 수 없게 됩니다.

AFWall+는 [패킷 필터링](https://en.wikipedia.org/wiki/Firewall_(computing)#Packet_filter) 방식으로 작동하며, 일부 상황에서는 우회될 수 있습니다.

프라이버시 가이드는 휴대폰을 루팅하면서 감수해야 하는 보안상의 희생이 이러한 앱들의 불확실한 프라이버시 이점만큼의 가치가 있다고 생각하지 않습니다.

### 정기적으로 업데이트 설치하기 { #install-updates-regularly }

[지원이 종료된](https://endoflife.date/android) 안드로이드 버전을 사용하지 않는 것이 중요합니다. 최신 안드로이드 버전에서는 운영 체제 보안 업데이트뿐만 아니라 중요한 프라이버시 강화 업데이트도 함께 제공됩니다.

예를 들어 [안드로이드 10 이전](https://developer.android.com/about/versions/10/privacy/changes)에는 [`READ_PHONE_STATE`](https://developer.android.com/reference/android/Manifest.permission#READ_PHONE_STATE) 권한을 가진 앱이라면 어떤 앱이든 휴대폰의 [IMEI](https://en.wikipedia.org/wiki/International_Mobile_Equipment_Identity), [MEID](https://en.wikipedia.org/wiki/Mobile_equipment_identifier), SIM 카드의 [IMSI](https://en.wikipedia.org/wiki/International_mobile_subscriber_identity) 같은 민감하고 고유한 일련번호에 접근할 수 있었지만, 이제는 시스템 앱만 접근할 수 있습니다. 시스템 앱은 OEM이나 안드로이드 배포판에서만 제공됩니다.

### 내장 공유 기능 사용하기 { #use-built-in-sharing-features }

안드로이드에 내장된 공유 기능을 활용하면 여러 앱에 미디어 접근 권한을 부여하지 않아도 됩니다. 많은 애플리케이션에서는 파일을 해당 앱으로 "공유"하는 방식으로 미디어를 업로드할 수 있습니다.

예를 들어 디스코드에 사진을 올리고 싶다면, 디스코드에 미디어와 사진에 대한 전체 접근 권한을 부여하는 대신 파일 관리자나 갤러리를 열어 해당 사진을 디스코드 앱으로 공유하면 됩니다.
