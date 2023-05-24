---
title: Android 개요
icon: simple/android
description: Android는 강력한 보안 및 보호 기능을 갖춘 오픈 소스 운영 체제로, 휴대폰에 있어서 최고의 선택입니다.
---

Android는 강력한 [애플리케이션 샌드박스](https://source.android.com/docs/security/app-sandbox?hl=ko), [자체 검사 부팅](https://source.android.com/docs/security/features/verifiedboot?hl=ko)(AVB) 기능과 엄밀한 [권한](https://developer.android.com/guide/topics/permissions/overview?hl=ko) 제어 시스템을 갖춘 안전한 운영 체제입니다.

## Android 배포판 선택

여러분이 Android 휴대폰을 새로 구입하면, 기기의 기본 운영체제 내에 [Android 오픈 소스 프로젝트(AOSP)](https://source.android.com/)에 포함되지 않은 앱, 서비스가 강력히 통합되어 있는 경우가 많습니다. 대표적인 예시로는 Google Play 서비스가 있습니다. Google Play 서비스는 파일, 통화 기록, 연락처, 통화 기록, SMS 메시지, 위치, 카메라, 마이크, 하드웨어 식별자 등에 접근할 수 있으며, 이 권한을 빼앗을 수도 없습니다. 이러한 앱, 서비스는 기기의 공격 표면을 증가시키고 Android의 다양한 프라이버시 문제로 이어집니다.

이 문제는 강력히 통합된 앱이 아예 포함되지 않은 커스텀 Android 배포판을 사용하면 해결할 수 있습니다. 다만 안타깝게도, 대부분의 커스텀 Android 배포판은 AVB, 롤백 보호, 펌웨어 업데이트 등의 중요한 보안 기능을 지원하지 않음으로써 Android 보안 모델을 위반하는 경우가 많습니다. 일부 배포판은 [ADB](https://developer.android.com/studio/command-line/adb?hl=ko)를 통해 루트 권한을 노출하고, 디버깅 기능을 포함하기 위해 [보다 느슨한](https://github.com/LineageOS/android_system_sepolicy/search?q=userdebug&type=code) SELinux 정책을 선택하여 공격 표면의 증가와 보안 모델의 약화를 일으키는 [`userdebug`](https://source.android.com/docs/setup/build/building?hl=ko#choose-a-target) 빌드를 제공하기도 합니다.

커스텀 Android 배포판을 선택할 때는 해당 배포판이 Android 보안 모델을 준수하는지 확인하는 것이 이상적입니다. 배포판은 적어도 프로덕션 빌드, AVB 지원, 롤백 보호, 시기적절한 펌웨어 및 운영 체제 업데이트, [적용 모드](https://source.android.com/docs/security/features/selinux/concepts?hl=ko#enforcement_levels)의 SELinux를 갖춰야 합니다. Privacy Guides에서 권장하는 Android 배포판은 이러한 기준을 모두 충족하고 있습니다.

[Android 시스템 권장 사항 :material-arrow-right-drop-circle:](../android.md ""){.md-button}

## 루팅 방지

Android 휴대폰을 [루팅](https://ko.wikipedia.org/wiki/%EB%A3%A8%ED%8C%85_(%EC%95%88%EB%93%9C%EB%A1%9C%EC%9D%B4%EB%93%9C))할 경우, [전체 Android 보안 모델](https://en.wikipedia.org/wiki/Android_(operating_system)#Security_and_privacy)이 약화되므로 보안 수준이 크게 저하됩니다. 보안 수준이 낮아져 취약점의 발생으로 이어질 경우 프라이버시 또한 저해됩니다. 루팅은 일반적으로 부팅 파티션을 직접 조작하는 방식으로 이루어지므로, 자체 검사 부팅을 제대로 수행할 수 없습니다. 루트 권한을 요구하는 앱 또한 시스템 파티션을 수정하므로 자체 검사 부팅을 활성화할 수 없습니다. 사용자 인터페이스에서 루트 권한이 직접 노출될 경우 기기의 [공격 표면](https://en.wikipedia.org/wiki/Attack_surface)이 증가하고 [권한 에스컬레이션](https://en.wikipedia.org/wiki/Privilege_escalation) 취약성과 SELinux 정책 우회 문제가 발생할 수 있습니다.

광고 차단기의 경우, [호스트 파일](https://ko.wikipedia.org/wiki/Hosts)을 수정하는 광고 차단기(AdAway)나 지속적으로 루트 권한 접근을 요구하는 방화벽(AFWall+)은 위험하므로 사용해서는 안 됩니다. 이러한 방식은 광고 차단기의 본래 목적 면에서도 적절한 방식이 아닙니다. 광고 차단기는 [암호화 DNS](../dns.md) 혹은 [VPN](../vpn.md) 서버 차단 솔루션을 권장드립니다. RethinkDNS, TrackerControl, AdAway는 루트 권한 없이 사용할 경우에는 (로컬 루프백 VPN을 이용하기 때문에) 시스템의 VPN 슬롯을 차지하게 되어버리므로, Orbot이나 실제 VPN 서버 등의 프라이버시 강화 서비스를 사용할 수 없다는 문제가 있습니다.

AFWall+는 [패킷 필터링](https://en.wikipedia.org/wiki/Firewall_(computing)#Packet_filter) 접근법을 기반으로 작동하며, 일부 상황에서는 우회될 수 있습니다.

Privacy Guides는 이러한 앱들의 불확실한 프라이버시 보호 효과가 휴대폰을 루팅함으로써 발생하는 보안상의 희생을 감수할 만큼 중요하다고는 생각하지 않습니다.

## 자체 검사 부팅

[자체 검사 부팅(Verified Boot)](https://source.android.com/security/verifiedboot)은 Android 보안 모델에서 중요한 부분을 차지하고 있습니다. [Evil maid](https://en.wikipedia.org/wiki/Evil_maid_attack) 공격, 멀웨어 지속성으로부터 보호하고, [롤백 보호](https://source.android.com/security/verifiedboot/verified-boot#rollback-protection)를 통해 보안 업데이트가 다운그레이드되는 일이 없도록 보장합니다.

Android 10 이상부터는 기존의 전체 디스크 암호화보다 유연한 [파일 기반 암호화](https://source.android.com/security/encryption/file-based)로 전환되었습니다. 여러분의 데이터는 고유한 암호화 키로 암호화되고, 운영 체제 파일은 암호화되지 않은 상태로 유지됩니다.

자체 검사 부팅은 운영 체제 파일의 무결성을 보장하여 물리적 접근 권한을 가진 공격자가 디바이스를 변조하거나 멀웨어를 설치하는 것을 방지합니다. 흔치는 않지만 멀웨어가 시스템의 다른 부분을 악용하여 더 높은 접근 권한을 얻어낼 경우, 자체 검사 부팅은 장치를 재부팅할 때 시스템 파티션의 변경을 감지하고 되돌립니다.

Unfortunately, OEMs are only obliged to support Verified Boot on their stock Android distribution. Only a few OEMs such as Google support custom AVB key enrollment on their devices. Additionally, some AOSP derivatives such as LineageOS or /e/ OS do not support Verified Boot even on hardware with Verified Boot support for third-party operating systems. We recommend that you check for support **before** purchasing a new device. AOSP derivatives which do not support Verified Boot are **not** recommended.

Many OEMs also have broken implementation of Verified Boot that you have to be aware of beyond their marketing. For example, the Fairphone 3 and 4 are not secure by default, as the [stock bootloader trusts the public AVB signing key](https://forum.fairphone.com/t/bootloader-avb-keys-used-in-roms-for-fairphone-3-4/83448/11). This breaks verified boot on a stock Fairphone device, as the system will boot alternative Android operating systems such (such as /e/) [without any warning](https://source.android.com/security/verifiedboot/boot-flow#locked-devices-with-custom-root-of-trust) about custom operating system usage.

## 펌웨어 업데이트

Firmware updates are critical for maintaining security and without them your device cannot be secure. OEMs have support agreements with their partners to provide the closed-source components for a limited support period. These are detailed in the monthly [Android Security Bulletins](https://source.android.com/security/bulletin).

As the components of the phone, such as the processor and radio technologies rely on closed-source components, the updates must be provided by the respective manufacturers. Therefore, it is important that you purchase a device within an active support cycle. [Qualcomm](https://www.qualcomm.com/news/releases/2020/12/16/qualcomm-and-google-announce-collaboration-extend-android-os-support-and) and [Samsung](https://news.samsung.com/us/samsung-galaxy-security-extending-updates-knox/) support their devices for 4 years, while cheaper products often have shorter support cycles. With the introduction of the [Pixel 6](https://support.google.com/pixelphone/answer/4457705), Google now makes their own SoC and they will provide a minimum of 5 years of support.

EOL devices which are no longer supported by the SoC manufacturer cannot receive firmware updates from OEM vendors or after market Android distributors. This means that security issues with those devices will remain unfixed.

Fairphone, for example, markets their devices as receiving 6 years of support. However, the SoC (Qualcomm Snapdragon 750G on the Fairphone 4) has a considerably shorter EOL date. This means that firmware security updates from Qualcomm for the Fairphone 4 will end in September 2023, regardless of whether Fairphone continues to release software security updates.

## Android 버전

It's important to not use an [end-of-life](https://endoflife.date/android) version of Android. Newer versions of Android not only receive security updates for the operating system but also important privacy enhancing updates too. For example, [prior to Android 10](https://developer.android.com/about/versions/10/privacy/changes), any apps with the [`READ_PHONE_STATE`](https://developer.android.com/reference/android/Manifest.permission#READ_PHONE_STATE) permission could access sensitive and unique serial numbers of your phone such as [IMEI](https://en.wikipedia.org/wiki/International_Mobile_Equipment_Identity), [MEID](https://en.wikipedia.org/wiki/Mobile_equipment_identifier), your SIM card's [IMSI](https://en.wikipedia.org/wiki/International_mobile_subscriber_identity), whereas now they must be system apps to do so. System apps are only provided by the OEM or Android distribution.

## Android 권한

[Andoird에서의 권한](https://developer.android.com/guide/topics/permissions/overview)은 앱이 접근 가능한 항목을 여러분이 제어할 수 있는 권한을 부여합니다. Google은 매 버전마다 권한 시스템을 [개선합니다](https://developer.android.com/about/versions/11/privacy/permissions?hl=ko). 여러분이 설치한 모든 앱은 엄격하게 [샌드박스로 격리](https://source.android.com/docs/security/app-sandbox?hl=ko)되어 있으므로, 바이러스 백신 앱은 설치하실 필요가 없습니다.

구형 Android 버전 스마트폰에 유료로 백신을 구매해 설치하는 것보다, 최신 버전 Android가 설치된 스마트폰이 모든 면에서 더 안전합니다. 바이러스 백신 소프트웨어 비용을 지불하는 대신 돈을 모아 Google Pixel 등의 새 스마트폰을 구입하는 편이 낫습니다.

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

- [근처 Wi-Fi 접근](https://developer.android.com/about/versions/13/behavior-changes-13#nearby-wifi-devices-permission) 권한이 도입됩니다. Wi-Fi 액세스 포인트의 MAC 주소는 앱이 사용자의 위치를 추적하는 용도로 흔히 사용되어 왔습니다.
- [세분화된 미디어 권한](https://developer.android.com/about/versions/13/behavior-changes-13?hl=ko#granular-media-permissions)이 도입되어, 이미지, 동영상, 오디오 파일에만 접근 가능한 권한을 부여할 수 있습니다.
- [`BODY_SENSORS`](https://developer.android.com/about/versions/13/behavior-changes-13?hl=ko#body-sensors-background-permission) 권한이 없으면 백그라운드에서 센서를 사용할 수 없습니다.

An app may request a permission for a specific feature it has. For example, any app that can scan QR codes will require the camera permission. Some apps can request more permissions than they need.

[Exodus](https://exodus-privacy.eu.org/) can be useful when comparing apps that have similar purposes. If an app requires a lot of permissions and has a lot of advertising and analytics this is probably a bad sign. We recommend looking at the individual trackers and reading their descriptions rather than simply **counting the total** and assuming all items listed are equal.

!!! warning "경고"

    앱이 대부분 웹 기반 서비스로 이루어진 경우, 추적은 서버 측에서 이루어질 수도 있습니다. [Facebook](https://reports.exodus-privacy.eu.org/en/reports/com.facebook.katana/latest/)은 '추적기 없음'이라 표시되어 있지만, 사이트 전반에서 사용자의 관심사와 행동을 추적하는 것은 틀림없습니다. 앱이 광고 업계에서 제작한 표준 광고 라이브러리 외의 수단을 사용함으로써 탐지에서 벗어나는 것도 있을 수 있는 일이지만, 가능성은 낮습니다.

!!! note "참고"

    [Bitwarden](https://reports.exodus-privacy.eu.org/en/reports/com.x8bit.bitwarden/latest/) 처럼 프라이버시 친화적인 앱에서도 [Google Firebase Analytics](https://reports.exodus-privacy.eu.org/en/trackers/49/) 등의 일부 추적기가 표시될 수 있습니다. 해당 라이브러리는 앱에서 [푸시 알림](https://ko.wikipedia.org/wiki/%ED%91%B8%EC%8B%9C_%EA%B8%B0%EB%B2%95)을 제공할 수 있는 [Firebase 클라우드 메시징(FCM)](https://en.wikipedia.org/wiki/Firebase_Cloud_Messaging)이 포함되어 있습니다. This [is the case](https://fosstodon.org/@bitwarden/109636825700482007) with Bitwarden. That doesn't mean that Bitwarden is using all of the analytics features that are provided by Google Firebase Analytics.

## Media Access

Quite a few applications allows you to "share" a file with them for media upload. If you want to, for example, tweet a picture to Twitter, do not grant Twitter access to your "media and photos", because it will have access to all of your pictures then. Instead, go to your file manager (documentsUI), hold onto the picture, then share it with Twitter.

## 사용자 프로필

다중 사용자 프로필은 Android에서 격리 환경을 가장 간단하게 구축할 수 있는 방법으로, **설정** → **시스템** → **여러 사용자**에서 확인할 수 있습니다.

With user profiles, you can impose restrictions on a specific profile, such as: making calls, using SMS, or installing apps on the device. 각 프로필은 고유한 암호화 키를 사용하여 암호화되며 다른 프로필의 데이터에 접근할 수 없습니다. 기기 소유자라 할지라도 비밀번호를 모르면 다른 프로필의 데이터를 볼 수 없습니다. Multiple user profiles are a more secure method of isolation.

## 직장 프로필

[직장 프로필](https://support.google.com/work/android/answer/6191949)은 개별 앱을 격리하는 방식 중 하나로, 경우에 따라서 별도 사용자 프로필을 사용하는 것보다 편리합니다.

여러분이 별도로 해당 기능을 탑재한 커스텀 Android 운영 체제를 사용하는 것이 아닌 한, 엔터프라이즈 MDM 없이 직장 프로필을 생성하려면 [Shelter](#recommended-apps) 등의 **기기 컨트롤러** 앱을 사용해야 합니다.

직장 프로필은 기기 컨트롤러에 따라 작동 방식이 달라집니다. *File Shuttle*, *연락처 검색 차단*을 비롯한 모든 격리 기능은 컨트롤러에서 구현됩니다. 기기 컨트롤러는 직장 프로필 내부 데이터의 전체 접근 권한을 가지고 있으므로, 믿을 수 있는 기기 컨트롤러 앱을 사용해야 합니다.

직장 프로필은 보조 사용자 프로필에 비해 보안성은 떨어집니다. 하지만 개인 프로필과 직장 프로필에서 동시에 앱을 실행할 수 있다는 편리함이 존재합니다.

## VPN 킬 스위치

Android 7 이상은 외부 앱을 설치할 필요 없이 VPN 킬 스위치를 자체적으로 지원합니다. 해당 기능은 VPN 연결이 끊어졌을 때 유출이 발생하지 않도록 방지할 수 있습니다. :gear: **설정** → **네트워크 및 인터넷** → **VPN** → :gear: → **연결 차단(VPN 제외)**에서 확인할 수 있습니다.

## Global Toggles

Modern Android devices have global toggles for disabling Bluetooth and location services. Android 12 introduced toggles for the camera and microphone. When not in use, we recommend disabling these features. Apps cannot use disabled features (even if granted individual permission) until re-enabled.

## Google

If you are using a device with Google services, either your stock operating system or an operating system that safely sandboxes Google Play Services like GrapheneOS, there are a number of additional changes you can make to improve your privacy. We still recommend avoiding Google services entirely, or limiting Google Play services to a specific user/work profile by combining a device controller like *Shelter* with GrapheneOS's Sandboxed Google Play.

### 고급 보호 프로그램

Google 계정을 가지고 있다면 [고급 보호 프로그램](https://landing.google.com/advancedprotection/)에 등록하시는 것을 권장드립니다. [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online)를 지원하는 하드웨어 보안 키를 2개 이상 가지고 있다면 누구나 무료로 이용할 수 있습니다.

The Advanced Protection Program provides enhanced threat monitoring and enables:

- Stricter two factor authentication; e.g. that [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online) **must** be used and disallows the use of [SMS OTPs](../basics/multi-factor-authentication.md#sms-or-email-mfa), [TOTP](../basics/multi-factor-authentication.md#time-based-one-time-password-totp) and [OAuth](https://en.wikipedia.org/wiki/OAuth)
- Only Google and verified third-party apps can access account data
- Scanning of incoming emails on Gmail accounts for [phishing](https://en.wikipedia.org/wiki/Phishing#Email_phishing) attempts
- Stricter [safe browser scanning](https://www.google.com/chrome/privacy/whitepaper.html#malware) with Google Chrome
- Stricter recovery process for accounts with lost credentials

 If you use non-sandboxed Google Play Services (common on stock operating systems), the Advanced Protection Program also comes with [additional benefits](https://support.google.com/accounts/answer/9764949?hl=en) such as:

- Not allowing app installation outside of the Google Play Store, the OS vendor's app store, or via [`adb`](https://en.wikipedia.org/wiki/Android_Debug_Bridge)
- Mandatory automatic device scanning with [Play Protect](https://support.google.com/googleplay/answer/2812853?hl=en#zippy=%2Chow-malware-protection-works%2Chow-privacy-alerts-work)
- Warning you about unverified applications

### Google Play 시스템 업데이트

과거에는 Android 보안 업데이트를 해당 운영 체제 공급업체에서 제공하는 구조였습니다. Android 10 이후부터 Android는 더욱 모듈화되었으며, Google은 Play 서비스를 통해 **일부** 시스템 구성 요소에 보안 업데이트를 제공할 수 있게 되었습니다.

여러분이 사용 중인 기기가 Android 10 이상이면서, 업데이트 지원은 종료되었고, Privacy Guides 권장 운영 체제는 지원하지 않는 경우, 별도 운영 체제(Privacy Guides 권장 목록에 등재되지 않은 LineageOS, /e/ OS 등)를 설치하는 것보다 제조사 Android를 그대로 사용하는 편이 더 나을 수도 있습니다. Google의 보안 수정 사항을 **일부** 업데이트 받을 수 있으면서도, 안전하지 않은 Android 파생 운영 체제를 사용함으로써 발생하는 공격 표면 증가와 Android 보안 모델을 위반하게 되는 결과를 피할 수 있습니다. 물론, 가능하다면 아직 지원되는 기기로 빨리 업그레이드하는 편이 더욱 좋습니다.

### 광고 ID

Google Play 서비스가 설치된 모든 기기는 타겟 광고에 사용되는 [광고 ID](https://support.google.com/googleplay/android-developer/answer/6048248?hl=ko)가 자동으로 생성됩니다. 이 기능을 비활성화하여 수집되는 데이터를 제한할 수 있습니다.

On Android distributions with [Sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), go to :gear: **Settings** → **Apps** → **Sandboxed Google Play** → **Google Settings** → **Ads**, and select *Delete advertising ID*.

On Android distributions with privileged Google Play Services (such as stock OSes), the setting may be in one of several locations. Check

- :gear: **설정** → **Google** → **광고**
- :gear: **설정** → **개인정보 보호** → **광고**

You will either be given the option to delete your advertising ID or to *Opt out of interest-based ads*, this varies between OEM distributions of Android. If presented with the option to delete the advertising ID that is preferred. If not, then make sure to opt out and reset your advertising ID.

### SafetyNet, Play Integrity API

[SafetyNet](https://developer.android.com/training/safetynet/attestation?hl=ko), [Play Integrity API](https://developer.android.com/google/play/integrity?hl=ko)는 일반적으로 [뱅킹 앱](https://grapheneos.org/usage#banking-apps)에서 사용됩니다. 대부분의 뱅킹 앱은 샌드박스가 적용된 Play 서비스를 통해 GrapheneOS에서 정상적으로 작동하지만, 자체적으로 조잡한 변조 방지 메커니즘을 사용하는 일부 비금융 앱은 제대로 작동하지 않을 수 있습니다. GrapheneOS는 `basicIntegrity`(관대한 기기 무결성) 검사를 통과했지만, `ctsProfileMatch`(엄격한 기기 무결성) 인증 검사는 통과하지 못했습니다. Android 8 이상의 기기는 키 유출이나 심각한 취약점이 발생하지 않고서는 우회 불가능한 하드웨어 증명이 지원됩니다.

As for Google Wallet, we don't recommend this due to their [privacy policy](https://payments.google.com/payments/apis-secure/get_legal_document?ldo=0&ldt=privacynotice&ldl=en), which states you must opt-out if you don't want your credit rating and personal information shared with affiliate marketing services.
