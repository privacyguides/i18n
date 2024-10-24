---
title: Android Overview
icon: simple/android
description: Android is an open-source operating system with strong security protections, which makes it our top choice for phones.
robots: nofollow, max-snippet:-1, max-image-preview:large
---

![Android 로고](../assets/img/android/android.svg){ align=right }

**Android 오픈소스 프로젝트**는 강력한 [애플리케이션 샌드박스](https://source.android.com/docs/security/app-sandbox?hl=ko), [자체 검사 부팅](https://source.android.com/docs/security/features/verifiedboot?hl=ko)(AVB) 기능과 엄밀한 [권한](https://developer.android.com/guide/topics/permissions/overview?hl=ko) 제어 시스템을 갖춘 안전한 모바일 운영 체제입니다.

[:octicons-home-16:](https://source.android.com){ .card-link title=Homepage }
[:octicons-info-16:](https://source.android.com/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://cs.android.com/android/platform/superproject/main){ .card-link title="Source Code" }

[Our Android Advice :material-arrow-right-drop-circle:](../android/index.md ""){.md-button.md-button--primary}

## 보안 보호

Key components of the Android security model include [verified boot](#verified-boot), [firmware updates](#firmware-updates), and a robust [permission system](#android-permissions). These important security features form the baseline of the minimum criteria for our [mobile phone](../mobile-phones.md) and [custom Android OS](../android/distributions.md) recommendations.

### 자체 검사 부팅

[**Verified Boot**](https://source.android.com/security/verifiedboot) is an important part of the Android security model. [Evil maid](https://en.wikipedia.org/wiki/Evil_maid_attack) 공격, 멀웨어 지속성으로부터 보호하고, [롤백 보호](https://source.android.com/security/verifiedboot/verified-boot#rollback-protection)를 통해 보안 업데이트가 다운그레이드되는 일이 없도록 보장합니다.

Android 10 이상부터는 기존의 전체 디스크 암호화보다 유연한 [파일 기반 암호화](https://source.android.com/security/encryption/file-based)로 전환되었습니다. 여러분의 데이터는 고유한 암호화 키로 암호화되고, 운영 체제 파일은 암호화되지 않은 상태로 유지됩니다.

자체 검사 부팅은 운영 체제 파일의 무결성을 보장하여 물리적 접근 권한을 가진 공격자가 디바이스를 변조하거나 멀웨어를 설치하는 것을 방지합니다. 흔치는 않지만 멀웨어가 시스템의 다른 부분을 악용하여 더 높은 접근 권한을 얻어낼 경우, 자체 검사 부팅은 장치를 재부팅할 때 시스템 파티션의 변경을 감지하고 되돌립니다.

안타깝게도, OEM의 자체 검사 부팅을 지원해야 할 의무는 오직 자신들의 기본 Android 배포판에서만 적용됩니다. Google 등 일부 OEM만이 기기에서 사용자 지정 AVB 키 등록을 지원합니다. 또한 제3자 운영 체제에 자체 검사 부팅을 지원하는 하드웨어를 사용하더라도, 어떤 AOSP 파생 버전을 사용하느냐에 따라 자체 검사 부팅 사용 가능 여부가 달라질 수 있습니다. 대표적으로 LineageOS, /e/ OS는 자체 검사 부팅을 지원하지 않습니다. 새 기기를 구매하기 이전에 **먼저** 지원 여부를 확인하실 것을 권장드립니다. 자체 검사 부팅을 지원하지 않는 AOSP 파생 버전은 권장드리지 **않습니다**.

또한, OEM 중에는 마케팅과 달리 자체 검사 부팅을 제대로 구현하지 않는 경우도 많으므로 주의해야 합니다. 예시로 Fairphone 3, 4는 [기본 부트로더가 공개 AVB 서명 키를 신뢰하기 때문에](https://forum.fairphone.com/t/bootloader-avb-keys-used-in-roms-for-fairphone-3-4/83448/11), 기본적으로는 안전하지 않습니다. This breaks verified boot on a stock Fairphone device, as the system will boot alternative Android operating systems (such as /e/) [without any warning](https://source.android.com/security/verifiedboot/boot-flow#locked-devices-with-custom-root-of-trust) about custom operating system usage.

### 펌웨어 업데이트

**Firmware updates** are critical for maintaining security and without them your device cannot be secure. OEM은 자신들의 협력체와 지원 계약을 맺고 제한된 기간 동안 비공개 소스로 된 구성 요소를 제공합니다. 관련 내용은 [Android 보안 게시판](https://source.android.com/security/bulletin)에 자세히 설명되어 있습니다.

휴대폰을 구성하는 요소(프로세서, 무선 기술 등)은 비공개 소스로 된 구성 요소에 의존하기 때문에, 업데이트는 각각의 제조업체로부터 제공받아야 합니다. 지원 기간 내의 기기를 구매해야 하는 이유가 바로 이것입니다. [Qualcomm](https://www.qualcomm.com/news/releases/2020/12/qualcomm-and-google-announce-collaboration-extend-android-os-support-and) and [Samsung](https://news.samsung.com/us/samsung-galaxy-security-extending-updates-knox) support their devices for 4 years, while cheaper products often have shorter support cycles. With the introduction of the [Pixel 6](https://support.google.com/pixelphone/answer/4457705), Google now makes their own SoC, and they will provide a minimum of 5 years of support. With the introduction of the Pixel 8 series, Google increased that support window to 7 years.

SoC 제조업체에서 더 이상 지원하지 않는 EOL 기기는 OEM 업체나 애프터 마켓 Android 배포자로부터 펌웨어 업데이트를 받는 것이 불가능합니다. 즉, 해당 기기의 보안 문제는 해결될 일이 없습니다.

Fairphone, for example, markets their Fairphone 4 device as receiving 6 years of support. 하지만 SoC(Fairphone 4의 Qualcomm Snapdragon 750G)는 훨씬 짧은 EOL 날짜를 가지고 있습니다. 즉, Fairphone이 계속 소프트웨어 보안 업데이트를 릴리스하더라도, Fairphone 4에 대한 Qualcomm의 펌웨어 보안 업데이트는 2023년 9월에 종료됩니다.

### Android 권한

[**Permissions on Android**](https://developer.android.com/guide/topics/permissions/overview) grant you control over what apps are allowed to access. Google은 매 버전마다 권한 시스템을 [개선합니다](https://developer.android.com/about/versions/11/privacy/permissions?hl=ko). 여러분이 설치한 모든 앱은 엄격하게 [샌드박스로 격리](https://source.android.com/docs/security/app-sandbox?hl=ko)되어 있으므로, 바이러스 백신 앱은 설치하실 필요가 없습니다.

구형 Android 버전 스마트폰에 유료로 백신을 구매해 설치하는 것보다, 최신 버전 Android가 설치된 스마트폰이 모든 면에서 더 안전합니다. It's better not to pay for antivirus software and to save money to buy a new smartphone such as a [Google Pixel](../mobile-phones.md#google-pixel).

Android 10:

- [범위 지정 저장소](https://developer.android.com/about/versions/10/privacy/changes?hl=ko#scoped-storage)는 사용자에게 더 많은 파일 제어 권한을 제공하고, [외부 저장소 접근](https://developer.android.com/training/data-storage?hl=ko#permissions)을 제한할 수 있습니다. 앱이 외부 저장소의 특정 디렉터리를 사용하도록 지정하거나, 특정 유형의 미디어를 저장하도록 할 수도 있습니다.
- `ACCESS_BACKGROUND_LOCATION` 권한을 도입하여 더 엄격한 [기기 위치](https://developer.android.com/about/versions/10/privacy/changes?hl=ko#app-access-device-location) 정보 접근을 제공합니다. 앱이 백그라운드에서 실행될 때에는 사용자의 명시적인 허가 없이 위치 정보에 접근할 수 없습니다.

Android 11:

- [일회성 권한](https://developer.android.com/about/versions/11/privacy/permissions?hl=ko#one-time)이 도입되어, 앱에 한 번만 권한을 부여하는 것이 가능합니다.
- [권한 자동 재설정](https://developer.android.com/about/versions/11/privacy/permissions?hl=ko#auto-reset)이 도입되어, 앱에 부여한 [런타임 권한](https://developer.android.com/guide/topics/permissions/overview?hl=ko#runtime)을 자동으로 초기화합니다.
- [전화번호](https://developer.android.com/about/versions/11/privacy/permissions?hl=ko#phone-numbers) 관련 기능 접근 권한이 세분화됩니다.

Android 12:

- [대략적인 위치](https://developer.android.com/about/versions/12/behavior-changes-12?hl=ko#approximate-location) 정보만 허용하는 권한이 도입됩니다.
- [최대 절전 모드 앱](https://developer.android.com/about/versions/12/behavior-changes-12#app-hibernation)이 자동으로 초기화됩니다.
- [데이터 액세스 분석](https://developer.android.com/about/versions/12/behavior-changes-12?hl=ko#data-access-auditing)을 통해 앱의 어느 부분이 특정 유형의 데이터에 접근하는지 쉽게 확인할 수 있습니다.

Android 13:

- A permission for [nearby Wi-Fi access](https://developer.android.com/about/versions/13/behavior-changes-13#nearby-wifi-devices-permission). The MAC addresses of nearby Wi-Fi access points were a popular way for apps to track a user's location.
- [세분화된 미디어 권한](https://developer.android.com/about/versions/13/behavior-changes-13?hl=ko#granular-media-permissions)이 도입되어, 이미지, 동영상, 오디오 파일에만 접근 가능한 권한을 부여할 수 있습니다.
- [`BODY_SENSORS`](https://developer.android.com/about/versions/13/behavior-changes-13?hl=ko#body-sensors-background-permission) 권한이 없으면 백그라운드에서 센서를 사용할 수 없습니다.

앱은 특정 기능에 대한 권한을 요청할 수 있습니다. 예를 들어, QR 코드를 스캔할 수 있는 모든 앱에는 카메라 권한이 필요합니다. 일부 앱은 해당 앱에 필요한 권한보다 더 많은 권한을 요청하는 경우도 있습니다.

[Exodus](https://exodus-privacy.eu.org) can be useful when comparing apps that have similar purposes. 앱이 과도한 권한을 요구하고 광고 및 분석 기능이 많다면, 해당 앱은 피해야 할지도 모릅니다. Privacy Guides는 각 항목의 차이를 보지 않고 **단순히 총합 수치로 비교**하기보다는 각각의 추적기와 그 설명을 하나씩 읽어보실 것을 권장드립니다.

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

앱의 상당 부분이 웹 기반 서비스로 이루어진 경우, 추적은 서버 측에서 이루어질 수도 있습니다. [Facebook](https://reports.exodus-privacy.eu.org/en/reports/com.facebook.katana/latest) shows "no trackers" but certainly does track users' interests and behavior across the site. 앱이 광고 업계에서 제작한 표준 광고 라이브러리 외의 수단을 사용함으로써 탐지에서 벗어나는 것도 있을 수 있는 일이지만, 가능성은 낮습니다.

</div>

<div class="admonition note" markdown>
<p class="admonition-title">Note</p>

Privacy-friendly apps such as [Bitwarden](https://reports.exodus-privacy.eu.org/en/reports/com.x8bit.bitwarden/latest) may show some trackers such as [Google Firebase Analytics](https://reports.exodus-privacy.eu.org/en/trackers/49). 해당 라이브러리는 앱에서 [푸시 알림](https://ko.wikipedia.org/wiki/%ED%91%B8%EC%8B%9C_%EA%B8%B0%EB%B2%95)을 제공할 수 있는 [Firebase 클라우드 메시징(FCM)](https://en.wikipedia.org/wiki/Firebase_Cloud_Messaging)이 포함되어 있습니다. Bitwarden이 바로 [이러한 경우](https://fosstodon.org/@bitwarden/109636825700482007)에 해당합니다. Bitwarden에서 Google Firebase Analytics 트래커가 발견됐다는 사실이 Bitwarden에서 Google Firebase Analytics의 모든 분석 기능을 사용한다는 것을 의미하지는 않습니다.

</div>

## Privacy Features

### 사용자 프로필

Multiple **user profiles** can be found in :gear: **Settings** → **System** → **Users** and are the simplest way to isolate in Android.

With user profiles, you can impose restrictions on a specific profile, such as: making calls, using SMS, or installing apps. 각 프로필은 고유한 암호화 키를 사용하여 암호화되며 다른 프로필의 데이터에 접근할 수 없습니다. 기기 소유자라 할지라도 비밀번호를 모르면 다른 프로필의 데이터를 볼 수 없습니다. '여러 사용자 프로필'은 여타 방법보다 더 안전한 격리 방법입니다.

### 직장 프로필

[**Work Profiles**](https://support.google.com/work/android/answer/6191949) are another way to isolate individual apps and may be more convenient than separate user profiles.

A **device controller** app such as [Shelter](../android/general-apps.md#shelter) is required to create a Work Profile without an enterprise MDM, unless you're using a custom Android OS which includes one.

직장 프로필은 기기 컨트롤러에 따라 작동 방식이 달라집니다. *File Shuttle*, *연락처 검색 차단*을 비롯한 모든 격리 기능은 컨트롤러에서 구현됩니다. You must also fully trust the device controller app, as it has full access to your data inside the work profile.

This method is generally less secure than a secondary user profile; however, it does allow you the convenience of running apps in both the owner profile and work profile simultaneously.

### Private Space

**Private Space** is a feature introduced in Android 15 that adds another way of isolating individual apps. You can set up a private space in the owner profile by navigating to :gear: **Settings** → **Security & privacy** → **Private space**. Once set up, your private space resides at the bottom of the app drawer.

Like user profiles, a private space is encrypted using its own encryption key, and you have the option to set up a different unlock method. Like work profiles, you can use apps from both the owner profile and private space simultaneously. Apps launched from a private space are distinguished by an icon depicting a key within a shield.

Unlike work profiles, Private Space is a feature native to Android that does not require a third-party app to manage it. For this reason, we generally recommend using a private space over a work profile, though you can use a work profile alongside a private space.

### VPN 킬 스위치

Android 7 and above supports a VPN kill switch, and it is available without the need to install third-party apps. 해당 기능은 VPN 연결이 끊어졌을 때 유출이 발생하지 않도록 방지할 수 있습니다. :gear: **설정** → **네트워크 및 인터넷** → **VPN** → :gear: → **연결 차단(VPN 제외)**에서 확인할 수 있습니다.

### 전역 제어

최신 Android 기기에는 Bluetooth 및 위치 서비스를 비활성화할 수 있는 전역 제어 기능이 존재합니다. Android 12에는 카메라, 마이크 접근 제어 기능이 도입되었습니다. 해당 기능들을 사용하지 않을 때에는 전역적으로 비활성화해 두는 것을 권장드립니다. Apps cannot use disabled features (even if granted individual permissions) until re-enabled.

## Google Services

If you are using a device with Google services—whether with the stock operating system or an operating system that safely sandboxes Google Play Services like GrapheneOS—there are a number of additional changes you can make to improve your privacy. 물론, Privacy Guides에서는 '가능하다면' Google 서비스를 아예 사용하지 않거나, Shelter 등의 기기 컨트롤러와 GrapheneOS의 Sandboxed Google Play 기능을 결합해 특정 사용자/업무 프로필로 Google Play 서비스를 제한해서 사용하실 것을 권장드립니다.

### 고급 보호 프로그램

If you have a Google account we suggest enrolling in the [Advanced Protection Program](https://landing.google.com/advancedprotection). [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online)를 지원하는 하드웨어 보안 키를 2개 이상 가지고 있다면 누구나 무료로 이용할 수 있습니다. Alternatively, you can use [passkeys](https://fidoalliance.org/passkeys).

고급 보호 프로그램은 향상된 위협 모니터링 기능을 제공합니다.

- Stricter two-factor authentication; e.g. that [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online) **must** be used and disallows the use of [SMS OTPs](../basics/multi-factor-authentication.md#sms-or-email-mfa), [TOTP](../basics/multi-factor-authentication.md#time-based-one-time-password-totp) and [OAuth](https://en.wikipedia.org/wiki/OAuth)
- Google 및 인증된 제3자 앱만이 계정 데이터에 접근 가능
- Google 계정의 받은 편지함에서 [피싱](https://en.wikipedia.org/wiki/Phishing#Email_phishing) 시도 스캔
- Stricter [safe browser scanning](https://google.com/chrome/privacy/whitepaper.html#malware) with Google Chrome
- 계정 자격 증명 손실 시 더 엄격한 복구 절차

 If you use non-sandboxed Google Play Services (common on stock operating systems), the Advanced Protection Program also comes with [additional benefits](https://support.google.com/accounts/answer/9764949) such as:

- Not allowing app installation outside the Google Play Store, the OS vendor's app store, or via [`adb`](https://en.wikipedia.org/wiki/Android_Debug_Bridge)
- Mandatory automatic device scanning with [Play Protect](https://support.google.com/googleplay/answer/2812853?#zippy=%2Chow-malware-protection-works%2Chow-privacy-alerts-work)
- 검증되지 않은 애플리케이션에 대한 경고 표시

### Google Play 시스템 업데이트

과거에는 Android 보안 업데이트를 해당 운영 체제 공급업체에서 제공하는 구조였습니다. Android 10 이후부터 Android는 더욱 모듈화되었으며, Google은 Play 서비스를 통해 **일부** 시스템 구성 요소에 보안 업데이트를 제공할 수 있게 되었습니다.

여러분이 사용 중인 기기가 Android 10 이상이면서, 업데이트 지원은 종료되었고, Privacy Guides 권장 운영 체제는 지원하지 않는 경우, 별도 운영 체제(Privacy Guides 권장 목록에 등재되지 않은 LineageOS, /e/ OS 등)를 설치하는 것보다 제조사 Android를 그대로 사용하는 편이 더 나을 수도 있습니다. Google의 보안 수정 사항을 **일부** 업데이트 받을 수 있으면서도, 안전하지 않은 Android 파생 운영 체제를 사용함으로써 발생하는 공격 표면 증가와 Android 보안 모델을 위반하게 되는 결과를 피할 수 있습니다. 물론, 가능하다면 아직 지원되는 기기로 빨리 업그레이드하는 편이 더욱 좋습니다.

### 광고 ID

All devices with Google Play Services installed automatically generate an [advertising ID](https://support.google.com/googleplay/android-developer/answer/6048248) used for targeted advertising. 이 기능을 비활성화하여 수집되는 데이터를 제한할 수 있습니다.

[Sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play)가 존재하는 Android 배포판의 경우, :gear: **Settings** → **Apps** → **Sandboxed Google Play** → **Google Settings** → **Ads**, *Delete advertising ID*를 선택하세요.

기본 OS 상태의 기기의 경우(Google Play 서비스가 시스템에 통합된 Android 배포판의 경우), 설정 옵션의 위치는 기기마다 다를 수 있습니다. 확인해보세요.

- :gear: **설정** → **Google** → **광고**
- :gear: **설정** → **개인정보 보호** → **광고**

You will either be given the option to delete your advertising ID or to *Opt out of interest-based ads* (this varies between OEM distributions of Android). If presented with the option to delete the advertising ID, that is preferred. 불가능한 경우에는 동의를 거부하고 광고 ID를 재설정하세요.

### SafetyNet, Play Integrity API

[SafetyNet](https://developer.android.com/training/safetynet/attestation?hl=ko), [Play Integrity API](https://developer.android.com/google/play/integrity?hl=ko)는 일반적으로 [뱅킹 앱](https://grapheneos.org/usage#banking-apps)에서 사용됩니다. 대부분의 뱅킹 앱은 샌드박스가 적용된 Play 서비스를 통해 GrapheneOS에서 정상적으로 작동하지만, 자체적으로 조잡한 변조 방지 메커니즘을 사용하는 일부 비금융 앱은 제대로 작동하지 않을 수 있습니다. GrapheneOS는 `basicIntegrity`(관대한 기기 무결성) 검사를 통과했지만, `ctsProfileMatch`(엄격한 기기 무결성) 인증 검사는 통과하지 못했습니다. Android 8 이상의 기기는 키 유출이나 심각한 취약점이 발생하지 않고서는 우회 불가능한 하드웨어 증명이 지원됩니다.

As for Google Wallet, we don't recommend this due to their [privacy policy](https://payments.google.com/payments/apis-secure/get_legal_document?ldo=0&ldt=privacynotice&ldl=en), which states you must opt out if you don't want your credit rating and personal information shared with affiliate marketing services.
