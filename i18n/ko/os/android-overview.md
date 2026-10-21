---
title: 안드로이드 개요
icon: simple/android
description: 안드로이드는 강력한 보안 보호 기능을 갖춘 오픈 소스 운영 체제로, 프라이버시 가이드가 휴대폰에 가장 추천하는 운영 체제입니다.
robots: nofollow, max-snippet:-1, max-image-preview:large
---

![안드로이드 로고](../assets/img/android/android.svg){ align=right }

**안드로이드 오픈 소스 프로젝트**는 강력한 [앱 샌드박싱](https://source.android.com/security/app-sandbox), [자체 검사 부팅](https://source.android.com/security/verifiedboot)(AVB), 견고한 [권한](https://developer.android.com/guide/topics/permissions/overview) 제어 시스템을 갖춘 안전한 모바일 운영 체제입니다.

[:octicons-home-16:](https://source.android.com){ .card-link title="홈페이지" }
[:octicons-info-16:](https://source.android.com/docs){ .card-link title="문서"}
[:octicons-code-16:](https://cs.android.com/android/platform/superproject/main){ .card-link title="소스 코드" }

[안드로이드에 관한 프라이버시 가이드의 조언 :material-arrow-right-drop-circle:](../android/index.md ""){.md-button.md-button--primary}

## 보안 보호 기능 { #security-protections }

안드로이드 보안 모델의 핵심 구성 요소로는 [자체 검사 부팅](#verified-boot), [펌웨어 업데이트](#firmware-updates), 견고한 [권한 시스템](#android-permissions)이 있습니다. 이러한 중요한 보안 기능은 프라이버시 가이드의 [휴대폰](../mobile-phones.md) 및 [커스텀 안드로이드 OS](../android/distributions.md) 추천을 위한 최소 기준의 기반이 됩니다.

### 자체 검사 부팅 { #verified-boot }

[**자체 검사 부팅**](https://source.android.com/security/verifiedboot)은 안드로이드 보안 모델의 중요한 부분입니다. 문서에서 발췌:
> 검증된 부팅(Verified Boot)은 실행되는 모든 코드가 공격자나 손상된 소스가 아닌 신뢰할 수 있는 출처(일반적으로 기기 OEM)에서 비롯되도록 보장하기 위해 노력합니다. 이 기술은 하드웨어로 보호되는 신뢰의 근원(root of trust)부터 부트 로더, 부트 파티션, 그리고 시스템, 벤더, 선택적으로 OEM 파티션을 포함한 기타 검증된 파티션에 이르기까지 완전한 신뢰 체인을 구축합니다. 장치가 부팅되는 동안, 각 단계는 실행을 다음 단계로 넘기기 전에 다음 단계의 무결성과 진위 여부를 확인합니다.

이 기능은 악성코드의 지속성을 차단하고, [롤백 방지 기능을](https://source.android.com/security/verifiedboot/verified-boot#rollback-protection) 통해 보안 업데이트가 이전 버전으로 되돌려지지 않도록 보장합니다.

안드로이드 10 이상은 전체 디스크 암호화에서 더 유연한 [파일 기반 암호화](https://source.android.com/security/encryption/file-based)로 전환했습니다.

자체 검사 부팅은 운영 체제 파일의 무결성을 보장하여, 물리적으로 접근할 수 있는 공격자가 기기를 변조하거나 멀웨어를 설치하는 것을 방지합니다. 만일 멀웨어가 시스템의 다른 부분을 악용하여 더 높은 권한을 얻더라도, 자체 검사 부팅은 기기를 재부팅할 때 시스템 파티션의 변경 사항을 차단하고 되돌립니다.

안타깝게도 OEM은 자사의 순정 안드로이드 배포판에서만 자체 검사 부팅을 지원할 의무가 있습니다. 구글 등 일부 OEM만이 자사 기기에서 사용자 지정 AVB 키 등록을 지원합니다. 또한 리니지OS나 /e/ OS 같은 일부 AOSP 파생 OS는 서드파티 운영 체제용 자체 검사 부팅을 지원하는 하드웨어에서도 자체 검사 부팅을 지원하지 않습니다. 새 기기를 구매하기 **전에** 지원 여부를 확인할 것을 권장합니다. 자체 검사 부팅을 지원하지 않는 AOSP 파생 OS는 권장하지 **않습니다**.

또한 많은 OEM이 자체 검사 부팅을 제대로 구현하지 않으므로, 마케팅 문구 이면을 잘 살펴봐야 합니다. 예를 들어 페어폰 3과 4는 [순정 부트로더가 공개 AVB 서명 키를 신뢰](https://forum.fairphone.com/t/bootloader-avb-keys-used-in-roms-for-fairphone-3-4/83448/11)하기 때문에 기본적으로 안전하지 않습니다. 이로 인해 순정 페어폰 기기에서 자체 검사 부팅이 무력화되는데, 시스템이 커스텀 운영 체제 사용에 대한 [아무런 경고 없이](https://source.android.com/security/verifiedboot/boot-flow#locked-devices-with-custom-root-of-trust) (/e/ 같은) 다른 안드로이드 운영 체제로 부팅되기 때문입니다.

### 펌웨어 업데이트 { #firmware-updates }

**펌웨어 업데이트**는 보안을 유지하는 데 매우 중요하며, 펌웨어 업데이트 없이는 기기가 안전할 수 없습니다. OEM은 협력사와 지원 계약을 맺어 제한된 지원 기간 동안 비공개 소스 구성 요소를 제공합니다. 이에 대한 자세한 내용은 매월 발행되는 [안드로이드 보안 공지](https://source.android.com/security/bulletin)에 나와 있습니다.

프로세서나 무선 기술 같은 휴대폰 구성 요소는 비공개 소스 구성 요소에 의존하므로, 업데이트는 각 제조업체가 제공해야 합니다. 따라서 지원 기간이 남아 있는 기기를 구매하는 것이 중요합니다. [퀄컴](https://qualcomm.com/news/releases/2020/12/qualcomm-and-google-announce-collaboration-extend-android-os-support-and)과 [삼성](https://news.samsung.com/us/samsung-galaxy-security-extending-updates-knox)은 자사 기기를 4년간 지원하지만, 저렴한 제품은 지원 기간이 더 짧은 경우가 많습니다. [픽셀 6](https://support.google.com/pixelphone/answer/4457705)이 출시되면서 구글은 자체 SoC를 만들기 시작했으며, 최소 5년간 지원을 제공합니다. 픽셀 8 시리즈부터 구글은 지원 기간을 7년으로 늘렸습니다.

SoC 제조업체의 지원이 끝난 EOL 기기는 OEM 공급업체나 애프터마켓 안드로이드 배포판 제작자로부터 펌웨어 업데이트를 받을 수 없습니다. 즉, 해당 기기의 보안 문제는 수정되지 않은 채 남게 됩니다.

예를 들어 페어폰은 페어폰 4가 6년간 지원을 받는다고 홍보합니다. 하지만 SoC(페어폰 4의 퀄컴 스냅드래곤 750G)의 EOL 날짜는 그보다 훨씬 이릅니다. 즉, 페어폰이 소프트웨어 보안 업데이트를 계속 출시하더라도, 페어폰 4에 대한 퀄컴의 펌웨어 보안 업데이트는 2023년 9월에 종료됩니다.

### 안드로이드 권한 { #android-permissions }

[**안드로이드의 권한**](https://developer.android.com/guide/topics/permissions/overview)을 통해 앱이 무엇에 접근할 수 있는지 통제할 수 있습니다. 구글은 새 버전마다 권한 시스템을 꾸준히 [개선](https://developer.android.com/about/versions/11/privacy/permissions)하고 있습니다. 설치하는 모든 앱은 엄격하게 [샌드박스 처리](https://source.android.com/security/app-sandbox)되므로 바이러스 백신 앱을 설치할 필요가 없습니다.

최신 버전 안드로이드가 설치된 스마트폰은 유료 백신을 설치한 구형 스마트폰보다 항상 더 안전합니다. 백신 소프트웨어에 돈을 쓰지 말고, 그 돈을 모아 [구글 픽셀](../mobile-phones.md#google-pixel) 같은 새 스마트폰을 구매하는 것이 낫습니다.

안드로이드 10:

- [범위 지정 저장소](https://developer.android.com/about/versions/10/privacy/changes#scoped-storage)를 통해 파일을 더 세밀하게 제어하고, [외부 저장소에 접근](https://developer.android.com/training/data-storage#permissions)할 수 있는 대상을 제한할 수 있습니다. 앱은 외부 저장소의 특정 디렉터리를 사용할 수 있으며, 그곳에 특정 유형의 미디어를 저장할 수 있습니다.
- `ACCESS_BACKGROUND_LOCATION` 권한이 도입되어 [기기 위치](https://developer.android.com/about/versions/10/privacy/changes#app-access-device-location)에 대한 접근이 더 엄격해졌습니다. 이를 통해 사용자의 명시적인 허가 없이 앱이 백그라운드에서 실행될 때 위치에 접근하는 것을 막습니다.

안드로이드 11:

- 앱에 권한을 한 번만 부여할 수 있는 [일회성 권한](https://developer.android.com/about/versions/11/privacy/permissions#one-time).
- 앱을 열 때 부여했던 [런타임 권한](https://developer.android.com/guide/topics/permissions/overview#runtime)을 재설정하는 [권한 자동 재설정](https://developer.android.com/about/versions/11/privacy/permissions#auto-reset).
- [전화번호](https://developer.android.com/about/versions/11/privacy/permissions#phone-numbers) 관련 기능에 접근하기 위한 세분화된 권한.

안드로이드 12:

- [대략적인 위치](https://developer.android.com/about/versions/12/behavior-changes-12#approximate-location)만 부여하는 권한.
- [최대 절전 모드 앱](https://developer.android.com/about/versions/12/behavior-changes-12#app-hibernation)의 권한 자동 재설정.
- 앱의 어느 부분이 특정 유형의 데이터에 접근하는지 쉽게 파악할 수 있는 [데이터 접근 감사](https://developer.android.com/about/versions/12/behavior-changes-12#data-access-auditing).

안드로이드 13:

- [주변 와이파이 접근](https://developer.android.com/about/versions/13/behavior-changes-13#nearby-wifi-devices-permission) 권한. 주변 와이파이 액세스 포인트의 MAC 주소는 앱이 사용자의 위치를 추적하는 데 흔히 사용하던 방법이었습니다.
- 이미지, 동영상, 오디오 파일에만 접근 권한을 부여할 수 있는 더 [세분화된 미디어 권한](https://developer.android.com/about/versions/13/behavior-changes-13#granular-media-permissions).
- 백그라운드에서 센서를 사용하려면 이제 [`BODY_SENSORS`](https://developer.android.com/about/versions/13/behavior-changes-13#body-sensors-background-permission) 권한이 필요합니다.

앱은 특정 기능에 대한 권한을 요청할 수 있습니다. 예를 들어, QR 코드를 스캔할 수 있는 모든 앱에는 카메라 권한이 필요합니다. 일부 앱은 필요한 것보다 더 많은 권한을 요청할 수 있습니다.

비슷한 목적의 앱을 비교할 때는 [엑소더스](https://exodus-privacy.eu.org)가 유용할 수 있습니다. 앱이 많은 권한을 요구하고 광고와 분석 도구가 많이 포함되어 있다면 좋지 않은 신호일 가능성이 높습니다. 단순히 **총개수를 세고** 나열된 항목이 모두 같다고 가정하기보다는, 개별 추적기를 살펴보고 그 설명을 읽어 볼 것을 권장합니다.

<div class="admonition warning" markdown>
<p class="admonition-title">경고</p>

앱의 상당 부분이 웹 기반 서비스로 이루어진 경우, 추적은 서버 측에서 이루어질 수도 있습니다. [페이스북](https://reports.exodus-privacy.eu.org/en/reports/com.facebook.katana/latest)은 "추적기 없음"으로 표시되지만, 사이트 전반에서 사용자의 관심사와 행동을 분명히 추적합니다. 앱이 광고 업계에서 만든 표준 코드 라이브러리를 사용하지 않음으로써 탐지를 피할 수도 있지만, 그럴 가능성은 낮습니다.

</div>

<div class="admonition note" markdown>
<p class="admonition-title">참고</p>

[비트워든](https://reports.exodus-privacy.eu.org/en/reports/com.x8bit.bitwarden/latest) 같은 프라이버시 친화적인 앱에서도 [구글 파이어베이스 애널리틱스](https://reports.exodus-privacy.eu.org/en/trackers/49) 같은 추적기가 표시될 수 있습니다. 이 라이브러리에는 앱에서 [푸시 알림](https://en.wikipedia.org/wiki/Push_technology)을 제공할 수 있는 [파이어베이스 클라우드 메시징](https://en.wikipedia.org/wiki/Firebase_Cloud_Messaging)이 포함되어 있습니다. 비트워든이 [바로 이런 경우](https://fosstodon.org/@bitwarden/109636825700482007)입니다. 그렇다고 해서 비트워든이 구글 파이어베이스 애널리틱스가 제공하는 모든 분석 기능을 사용한다는 의미는 아닙니다.

</div>

## 프라이버시 기능 { #privacy-features }

### 사용자 프로필 { #user-profiles }

여러 **사용자 프로필**은 :gear: **설정** → **시스템** → **사용자**에서 찾을 수 있으며, 안드로이드에서 가장 간단한 격리 방법입니다.

사용자 프로필을 사용하면 특정 프로필에 전화 걸기, SMS 사용, 앱 설치 등의 제한을 걸 수 있습니다. 각 프로필은 고유한 암호화 키를 사용하여 암호화되며 다른 프로필의 데이터에 접근할 수 없습니다. 기기 소유자라 할지라도 비밀번호를 모르면 다른 프로필의 데이터를 볼 수 없습니다. 여러 사용자 프로필은 더 안전한 격리 방법입니다.

### 직장 프로필 { #work-profile }

[**직장 프로필**](https://support.google.com/work/android/answer/6191949)은 개별 앱을 격리하는 또 다른 방법으로, 별도의 사용자 프로필보다 편리할 수 있습니다.

기업용 MDM 없이 직장 프로필을 만들려면 [셸터](../android/general-apps.md#shelter) 같은 **기기 컨트롤러** 앱이 필요합니다. 단, 기기 컨트롤러가 포함된 커스텀 안드로이드 OS를 사용하는 경우는 예외입니다.

직장 프로필이 작동하려면 기기 컨트롤러가 필요합니다. *파일 셔틀*, *연락처 검색 차단* 같은 기능이나 모든 종류의 격리 기능은 컨트롤러가 구현해야 합니다. 또한 기기 컨트롤러 앱은 직장 프로필 안의 데이터에 완전히 접근할 수 있으므로 이 앱을 전적으로 신뢰해야 합니다.

이 방법은 일반적으로 보조 사용자 프로필보다 덜 안전하지만, 소유자 프로필과 직장 프로필의 앱을 동시에 실행할 수 있다는 편리함이 있습니다.

### 비공개 스페이스 { #private-space }

**비공개 스페이스**는 안드로이드 15에 도입된 기능으로, 개별 앱을 격리하는 또 다른 방법을 제공합니다. :gear: **설정** → **보안 및 개인 정보 보호** → **비공개 스페이스**로 이동하여 소유자 프로필에 비공개 스페이스를 설정할 수 있습니다. 설정이 끝나면 비공개 스페이스는 앱 서랍 맨 아래에 위치합니다.

사용자 프로필과 마찬가지로 비공개 스페이스는 자체 암호화 키로 암호화되며, 별도의 잠금 해제 방법을 설정할 수도 있습니다. 직장 프로필과 마찬가지로 소유자 프로필과 비공개 스페이스의 앱을 동시에 사용할 수 있습니다. 비공개 스페이스에서 실행된 앱에는 방패 안에 열쇠가 그려진 아이콘이 표시됩니다.

직장 프로필과 달리 비공개 스페이스는 안드로이드 기본 기능이므로 관리할 서드파티 앱이 필요하지 않습니다. 이러한 이유로 일반적으로 직장 프로필보다 비공개 스페이스를 권장하지만, 비공개 스페이스와 직장 프로필을 함께 사용할 수도 있습니다.

### VPN 킬 스위치 { #vpn-kill-switch }

안드로이드 7 이상은 VPN 킬 스위치를 지원하며, 서드파티 앱을 설치하지 않아도 사용할 수 있습니다. 해당 기능은 VPN 연결이 끊어졌을 때 유출이 발생하지 않도록 방지할 수 있습니다. :gear: **설정** → **네트워크 및 인터넷** → **VPN** → :gear: → **VPN 없는 연결 차단**에서 찾을 수 있습니다.

### 전역 토글 { #global-toggles }

최신 안드로이드 기기에는 블루투스와 위치 서비스를 끌 수 있는 전역 토글이 있습니다. 안드로이드 12에서는 카메라와 마이크용 토글이 도입되었습니다. 사용하지 않을 때는 이러한 기능을 꺼 두는 것을 권장합니다. 꺼 둔 기능은 다시 켤 때까지 앱이 (개별 권한을 부여받았더라도) 사용할 수 없습니다.

## 구글 서비스 { #google-services }

구글 서비스가 있는 기기를 사용한다면(순정 운영 체제이든, 그래핀OS처럼 구글 플레이 서비스를 안전하게 샌드박스 처리하는 운영 체제이든) 프라이버시를 개선하기 위해 추가로 변경할 수 있는 설정이 많습니다. 그래도 구글 서비스를 아예 피하거나, *셸터* 같은 기기 컨트롤러와 그래핀OS의 샌드박스 구글 플레이를 함께 사용하여 구글 플레이 서비스를 특정 사용자/직장 프로필로 제한할 것을 권장합니다.

### 고급 보호 프로그램 { #advanced-protection-program }

구글 계정이 있다면 [고급 보호 프로그램](https://landing.google.com/advancedprotection)에 등록할 것을 권장합니다. [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online)를 지원하는 하드웨어 보안 키가 두 개 이상 있다면 누구나 무료로 이용할 수 있습니다. 또는 [패스키](https://fidoalliance.org/passkeys)를 사용할 수도 있습니다.

고급 보호 프로그램은 강화된 위협 모니터링을 제공하며 다음을 적용합니다:

- 더 엄격한 2단계 인증. 예를 들어 [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online)를 **반드시** 사용해야 하며 [SMS OTP](../basics/multi-factor-authentication.md#sms-or-email-mfa), [TOTP](../basics/multi-factor-authentication.md#time-based-one-time-password-totp), [OAuth](../basics/account-creation.md#sign-in-with-oauth)는 사용할 수 없습니다
- 구글과 인증된 서드파티 앱만 계정 데이터에 접근 가능
- 지메일 계정으로 들어오는 이메일의 [피싱](https://en.wikipedia.org/wiki/Phishing#Email_phishing) 시도 검사
- 구글 크롬의 더 엄격한 [세이프 브라우징 검사](https://google.com/chrome/privacy/whitepaper.html#malware)
- 자격 증명을 분실한 계정에 대한 더 엄격한 복구 절차

 샌드박스 처리되지 않은 구글 플레이 서비스(순정 운영 체제에서 일반적)를 사용한다면, 고급 보호 프로그램은 다음과 같은 [추가 혜택](https://support.google.com/accounts/answer/9764949)도 제공합니다:

- 구글 플레이 스토어, OS 공급업체의 앱 스토어, [`adb`](https://en.wikipedia.org/wiki/Android_Debug_Bridge) 이외의 경로를 통한 앱 설치 차단
- [플레이 프로텍트](https://support.google.com/googleplay/answer/2812853?#zippy=%2Chow-malware-protection-works%2Chow-privacy-alerts-work)를 통한 필수 자동 기기 검사
- 검증되지 않은 애플리케이션에 대한 경고
- 지원되는 앱에 대해 ARM의 하드웨어 기반 [메모리 태깅 확장(MTE)](https://developer.arm.com/documentation/108035/0100/Introduction-to-the-Memory-Tagging-Extension)을 활성화하여, 메모리 손상 버그를 통한 기기 익스플로잇 발생 가능성을 낮춤

### 구글 플레이 시스템 업데이트 { #google-play-system-updates }

과거에는 안드로이드 보안 업데이트를 운영 체제 공급업체가 제공해야 했습니다. 안드로이드는 안드로이드 10부터 더욱 모듈화되었으며, 구글은 권한 있는 플레이 서비스를 통해 **일부** 시스템 구성 요소에 대한 보안 업데이트를 제공할 수 있습니다.

안드로이드 10 이상이 탑재되어 출시된 EOL 기기를 사용하고 있고 추천 운영 체제를 설치할 수 없다면, (리니지OS나 /e/ OS처럼 여기에 소개되지 않은 운영 체제보다는) OEM의 안드로이드를 그대로 사용하는 편이 나을 가능성이 높습니다. 이렇게 하면 구글로부터 **일부** 보안 수정 사항을 받을 수 있으면서도, 안전하지 않은 안드로이드 파생 OS를 사용하여 안드로이드 보안 모델을 위반하고 공격 표면을 늘리는 일을 피할 수 있습니다. 그래도 가능한 한 빨리 지원되는 기기로 업그레이드할 것을 권장합니다.

### 광고 ID { #advertising-id }

구글 플레이 서비스가 설치된 모든 기기는 맞춤 광고에 사용되는 [광고 ID](https://support.google.com/googleplay/android-developer/answer/6048248)를 자동으로 생성합니다. 이 기능을 비활성화하여 여러분에 대해 수집되는 데이터를 제한하세요.

[샌드박스 구글 플레이](https://grapheneos.org/usage#sandboxed-google-play)가 있는 안드로이드 배포판에서는 :gear: **설정** → **앱** → **Sandboxed Google Play** → **Google 설정** → **모든 서비스** → **광고**로 이동하세요.

- [x] **광고 ID 삭제** 선택

권한 있는 구글 플레이 서비스가 있는 안드로이드 배포판(대부분 기기의 순정 설치 포함)에서는 이 설정이 여러 위치 중 한 곳에 있을 수 있습니다. 다음을 확인하세요

- :gear: **설정** → **Google** → **광고**
- :gear: **설정** → **개인정보 보호** → **광고**

광고 ID를 삭제하는 옵션이나 *관심 기반 광고 선택 해제* 옵션 중 하나가 제공됩니다(안드로이드 OEM 배포판마다 다름). 광고 ID를 삭제하는 옵션이 있다면 그쪽을 선택하는 것이 좋습니다. 그렇지 않다면 반드시 선택 해제하고 광고 ID를 재설정하세요.

### SafetyNet 및 Play Integrity API { #safetynet-and-play-integrity-api }

[SafetyNet](https://developer.android.com/training/safetynet/attestation)과 [Play Integrity API](https://developer.android.com/google/play/integrity)는 일반적으로 [뱅킹 앱](https://grapheneos.org/usage#banking-apps)에서 사용됩니다. 많은 뱅킹 앱은 샌드박스 플레이 서비스가 있는 그래핀OS에서 잘 작동하지만, 일부 비금융 앱은 자체적인 조잡한 변조 방지 메커니즘을 사용하여 작동하지 않을 수 있습니다. 그래핀OS는 `basicIntegrity` 검사는 통과하지만, 인증 검사인 `ctsProfileMatch`는 통과하지 못합니다. 안드로이드 8 이상의 기기는 키 유출이나 심각한 취약점 없이는 우회할 수 없는 하드웨어 증명을 지원합니다.

구글 월렛은 [개인정보 처리방침](https://payments.google.com/payments/apis-secure/get_legal_document?ldo=0&ldt=privacynotice&ldl=en) 때문에 권장하지 않습니다. 이 방침에 따르면 신용 등급과 개인 정보가 제휴 마케팅 서비스와 공유되는 것을 원하지 않을 경우 직접 거부(옵트아웃)해야 합니다.
