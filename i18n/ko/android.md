---
meta_title: "Android Recommendations: GrapheneOS and DivestOS - Privacy Guides"
title: "Android"
icon: 'simple/android'
description: You can replace the operating system on your Android phone with these secure and privacy-respecting alternatives.
cover: android.webp
schema:
  - 
    "@context": http://schema.org
    "@type": WebPage
    name: Private Android Operating Systems
    url: "./"
  - 
    "@context": http://schema.org
    "@type": CreativeWork
    name: Android
    image: /assets/img/android/android.svg
    url: https://source.android.com/
    sameAs: https://en.wikipedia.org/wiki/Android_(operating_system)
  - 
    "@context": http://schema.org
    "@type": CreativeWork
    name: GrapheneOS
    image: /assets/img/android/grapheneos.svg
    url: https://grapheneos.org/
    sameAs: https://en.wikipedia.org/wiki/GrapheneOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": CreativeWork
    name: Divest
    image: /assets/img/android/divestos.svg
    url: https://divestos.org/
    sameAs: https://en.wikipedia.org/wiki/DivestOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
  - 
    "@context": http://schema.org
    "@type": Product
    name: Pixel
    brand:
      "@type": Brand
      name: Google
    image: /assets/img/android/google-pixel.png
    sameAs: https://en.wikipedia.org/wiki/Google_Pixel
    review:
      "@type": Review
      author:
        "@type": Organization
        name: Privacy Guides
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Shelter
    applicationCategory: Utilities
    operatingSystem: Android
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Auditor
    applicationCategory: Utilities
    operatingSystem: Android
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Secure Camera
    applicationCategory: Utilities
    operatingSystem: Android
  - 
    "@context": http://schema.org
    "@type": MobileApplication
    name: Secure PDF Viewer
    applicationCategory: Utilities
    operatingSystem: Android
---

![Android 로고](assets/img/android/android.svg){ align=right }

**Android 오픈소스 프로젝트**는 Google이 주도하는 오픈 소스 모바일 운영 체제로, 전 세계 모바일 기기의 대부분이 사용하고 있습니다. Android가 탑재되어 판매되는 대부분의 휴대폰은 Google Play 서비스 등의 여러 앱이 강력하게 통합되어 있습니다. 이러한 프라이버시 침해 기능이 포함되지 않은 Android 버전으로 모바일 기기 운영 체제를 교체하여 프라이버시를 크게 향상시킬 수 있습니다.

[:octicons-home-16:](https://source.android.com/){ .card-link title=홈페이지 }
[:octicons-info-16:](https://source.android.com/docs){ .card-link title=문서}
[:octicons-code-16:](https://cs.android.com/android/platform/superproject/){ .card-link title="소스 코드" }

본 내용은 모바일 기기의 보안 및 프라이버시 보호를 극대화하는 용도로 권장드리는 Android 운영 체제, 기기, 애플리케이션 목록입니다. Android 자체에 대한 내용은 Android 기본 개요를 참고해주세요.

[Android 기본 개요 :material-arrow-right-drop-circle:](os/android-overview.md ""){.md-button}

## AOSP 기반

Privacy Guides에서 권장하는 커스텀 Android 운영 체제의 우선 순위는 본 페이지에 나열된 순서와 동일합니다. 여러분이 가진 기기 호환성에 따라 적절한 운영 체제를 선택하시는 것을 권장드립니다.

<div class="admonition note" markdown>
<p class="admonition-title">Note</p>

지원 종료 기기(GrapheneOS, CalyxOS에서 '연장 지원'에 해당하는 기기)의 경우, OEM 지원 중단으로 인해 전체 보안 패치(펌웨어 업데이트)를 제공받을 수 없습니다. 지원 종료 기기는 그 어떤 소프트웨어를 설치하더라도 완벽히 안전하다고 간주할 수 없습니다.

</div>

### GrapheneOS

<div class="admonition recommendation" markdown>

![GrapheneOS 로고](assets/img/android/grapheneos.svg#only-light){ align=right }
![GrapheneOS 로고](assets/img/android/grapheneos-dark.svg#only-dark){ align=right }

**GrapheneOS**는 프라이버시 및 보안 면에서 최고의 선택입니다.

GraphneOS는 추가적인 [보안 강화](https://en.wikipedia.org/wiki/Hardening_(computing))와 프라이버시 강화 기능을 제공합니다. [메모리 할당 보안 강화](https://github.com/GrapheneOS/hardened_malloc), 네트워크 및 센서 권한 등 다양한 [보안 기능](https://grapheneos.org/features)을 포함하고 있습니다. GrapheneOS는 전체 펌웨어 업데이트 및 서명된 빌드 또한 제공하므로, 자체 검사 부팅을 완벽하게 지원합니다.

[:octicons-home-16: 홈페이지](https://grapheneos.org/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://grapheneos.org/faq#privacy-policy){ .card-link title="프라이버시 정책" }
[:octicons-info-16:](https://grapheneos.org/faq){ .card-link title=문서}
[:octicons-code-16:](https://grapheneos.org/source){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=기부 }

</div>

GrapheneOS는 [Sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play) 지원하여, [Google Play 서비스](https://en.wikipedia.org/wiki/Google_Play_Services)를 여타 일반 앱처럼 완벽하게 샌드박스를 적용하여 실행할 수 있습니다. 즉, 원하는 특정 [직장 프로필](os/android-overview.md#work-profile)이나 [사용자 프로필](os/android-overview.md#user-profiles)에 추가하여, [푸시 알림](https://firebase.google.com/docs/cloud-messaging/) 등 대부분의 Google Play 서비스를 이용하면서도 권한 및 접근 영역을 완전히 제어할 수 있습니다.

Google Pixel 스마트폰은 현재 GrapheneOS [하드웨어 보안 요구 사항](https://grapheneos.org/faq#device-support)을 충족하는 유일한 기기입니다.

[CalyxOS보다 GrapheneOS를 추천하는 이유 :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/04/21/grapheneos-or-calyxos/ ""){.md-button}

### DivestOS

<div class="admonition recommendation" markdown>

![DivestOS 로고](assets/img/android/divestos.svg){ align=right }

**DivestOS**는 [LineageOS](https://lineageos.org/)의 소프트 포크입니다.
DivestOS inherits many [supported devices](https://divestos.org/index.php?page=devices&base=LineageOS) from LineageOS. 서명된 빌드가 존재하여, Pixel 외 기기에서 [검증 부팅(Verified Boot)](https://source.android.com/security/verifiedboot)을 사용할 수 있습니다.

[:octicons-home-16: 홈페이지](https://divestos.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://divestoseb5nncsydt7zzf5hrfg44md4bxqjs5ifcv4t7gt7u6ohjyyd.onion){ .card-link title="Onion 서비스" }
[:octicons-eye-16:](https://divestos.org/index.php?page=privacy_policy){ .card-link title="프라이버시 정책" }
[:octicons-info-16:](https://divestos.org/index.php?page=faq){ .card-link title=문서}
[:octicons-code-16:](https://github.com/divested-mobile){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://divested.dev/pages/donate){ .card-link title=기부 }

</div>

DivestOS has automated kernel vulnerability ([CVE](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures)) [patching](https://gitlab.com/divested-mobile/cve_checker), fewer proprietary blobs, and a custom [hosts](https://divested.dev/index.php?page=dnsbl) file. Its hardened WebView, [Mulch](https://gitlab.com/divested-mobile/mulch), enables [CFI](https://en.wikipedia.org/wiki/Control-flow_integrity) for all architectures and [network state partitioning](https://developer.mozilla.org/en-US/docs/Web/Privacy/State_Partitioning), and receives out-of-band updates. DivestOS also includes kernel patches from GrapheneOS and enables all available kernel security features via [defconfig hardening](https://github.com/Divested-Mobile/DivestOS-Build/blob/master/Scripts/Common/Functions.sh#L758). All kernels newer than version 3.4 include full page [sanitization](https://lwn.net/Articles/334747/) and all ~22 Clang-compiled kernels have [`-ftrivial-auto-var-init=zero`](https://reviews.llvm.org/D54604?id=174471) enabled.

DivestOS implements some system hardening patches originally developed for GrapheneOS. DivestOS 16.0 and higher implements GrapheneOS's [`INTERNET`](https://developer.android.com/training/basics/network-ops/connecting) and SENSORS permission toggle, [hardened memory allocator](https://github.com/GrapheneOS/hardened_malloc), [exec-spawning](https://blog.privacyguides.org/2022/04/21/grapheneos-or-calyxos/#additional-hardening), [JNI](https://en.wikipedia.org/wiki/Java_Native_Interface) [constification](https://en.wikipedia.org/wiki/Const_(computer_programming)), and partial [bionic](https://en.wikipedia.org/wiki/Bionic_(software)) hardening patchsets. 17.1 and higher features GrapheneOS's per-network full [MAC randomization](https://en.wikipedia.org/wiki/MAC_address#Randomization) option, [`ptrace_scope`](https://www.kernel.org/doc/html/latest/admin-guide/LSM/Yama.html) control, and automatic reboot/Wi-Fi/Bluetooth [timeout options](https://grapheneos.org/features).

DivestOS uses F-Droid as its default app store. We normally [recommend avoiding F-Droid](#f-droid), but doing so on DivestOS isn't viable; the developers update their apps via their own F-Droid repositories ([DivestOS Official](https://divestos.org/fdroid/official/?fingerprint=E4BE8D6ABFA4D9D4FEEF03CDDA7FF62A73FD64B75566F6DD4E5E577550BE8467) and [DivestOS WebView](https://divestos.org/fdroid/webview/?fingerprint=FB426DA1750A53D7724C8A582B4D34174E64A84B38940E5D5A802E1DFF9A40D2)). We recommend disabling the official F-Droid app and using [F-Droid Basic](https://f-droid.org/en/packages/org.fdroid.basic/) **with the DivestOS repositories enabled** to keep those components up to date. For other apps, our recommended methods of obtaining them still apply.

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

DivestOS 펌웨어 업데이트의 [세부 상태](https://gitlab.com/divested-mobile/firmware-empty/-/blob/master/STATUS) 및 품질 관리는 지원하는 기기에 따라 다릅니다. GrapheneOS와 호환되는 기기라면 GrapheneOS를 권장합니다. GrapheneOS 미지원 기기의 경우, DivestOS는 좋은 대체제입니다.

검증 부팅은 모든 지원 기기에서 사용 가능한 것은 아니며, 일부 기기는 다른 기기보다 더 원활할 수 있습니다.

</div>

## Android 기기

기기를 구매할 때는 가급적 최신 제품을 구입해야 합니다. 모바일 기기의 소프트웨어와 펌웨어 지원 기간은 제한되어 있으므로, 최신 제품을 구입해야 최대한 수명을 늘릴 수 있습니다.

이동 통신사로부터 휴대폰을 사는 것은 지양해야 합니다. 이동 통신사에서 판매하는 휴대폰은 보통 **부트로더 잠금**이 걸려 있으며, [OEM 잠금 해제](https://source.android.com/devices/bootloader/locking_unlocking)를 지원하지 않습니다. 이 경우, 어떤 종류의 대체 Android 배포판도 설치할 수 없습니다.

온라인에서 중고 휴대폰을 구입할 때에는 매우 **주의해야** 합니다. 판매자의 평판을 항상 확인하세요. If the device is stolen, there's a possibility of it being entered in the [IMEI database](https://www.gsma.com/get-involved/working-groups/terminal-steering-group/imei-database). 또한 이전 소유자의 활동과 연관될 수 있다는 위험성도 존재합니다.

Android 기기 및 운영 체제 호환성에 관한 추가 정보:

- 수명이 다했거나 거의 다한 기기는 구매하지 마세요. 제조업체에서 추가 펌웨어 업데이트가 제공되는 기기를 구매해야 합니다.
- LineageOS나 /e/ OS가 사전 설치된 휴대폰이나, 적절한 [자체 검사 부팅(Verified Boot)](https://source.android.com/security/verifiedboot) 지원 혹은 펌웨어 업데이트가 없는 Android 휴대폰을 구매하지 마세요. 이러한 기기는 조작되었는지 여부를 확인할 방법이 없습니다.
- 요런대, 어떤 기기나 Android 배포판이 여기에 등재되지 않은 경우에는 그럴 만한 이유가 있을 겁니다. 자세한 내용은 [포럼](https://discuss.privacyguides.net/)을 참고해 주세요.

### Google Pixel

Google Pixel은 Privacy Guides에서 **유일하게** 구매를 권장하는 기기입니다. Pixel 스마트폰은 현재 시중에 존재하는 어떤 Android 기기보다도 강력한 하드웨어 보안을 가지고 있습니다. 제3자 운영 체제에 대한 적절한 AVB 지원이 갖추어져 있으며, Secure Element 역할 Google 커스텀 [Titan](https://security.googleblog.com/2021/10/pixel-6-setting-new-standard-for-mobile.html) 보안 칩을 탑재하고 있습니다.

<div class="admonition recommendation" markdown>

![Google Pixel 6](assets/img/android/google-pixel.png){ align=right }

**Google Pixel** devices are known to have good security and properly support [Verified Boot](https://source.android.com/security/verifiedboot), even when installing custom operating systems.

Beginning with the **Pixel 8** and **8 Pro**, Pixel devices receive a minimum of 7 years of guaranteed security updates, ensuring a much longer lifespan compared to the 2-5 years competing OEMs typically offer.

[:material-shopping: Store](https://store.google.com/category/phones){ .md-button .md-button--primary }

</div>

Secure Elements like the Titan M2 are more limited than the processor's Trusted Execution Environment used by most other phones as they are only used for secrets storage, hardware attestation, and rate limiting, not for running "trusted" programs. Phones without a Secure Element have to use the TEE for *all* of those functions, resulting in a larger attack surface.

Google Pixel phones use a TEE OS called Trusty which is [open source](https://source.android.com/security/trusty#whyTrusty), unlike many other phones.

The installation of GrapheneOS on a Pixel phone is easy with their [web installer](https://grapheneos.org/install/web). If you don't feel comfortable doing it yourself and are willing to spend a bit of extra money, check out the [NitroPhone](https://shop.nitrokey.com/shop) as they come preloaded with GrapheneOS from the reputable [Nitrokey](https://www.nitrokey.com/about) company.

A few more tips for purchasing a Google Pixel:

- If you're after a bargain on a Pixel device, we suggest buying an "**a**" model, just after the next flagship is released. Discounts are usually available because Google will be trying to clear their stock.
- Consider price beating options and specials offered at physical stores.
- Look at online community bargain sites in your country. These can alert you to good sales.
- Google provides a list showing the [support cycle](https://support.google.com/nexus/answer/4457705) for each one of their devices. The price per day for a device can be calculated as: $\text{Cost} \over \text {EOL Date}-\text{Current Date}$, meaning that the longer use of the device the lower cost per day.
- If the Pixel is unavailable in your region, the [NitroPhone](https://shop.nitrokey.com/shop) can be shipped globally.

## 일반 앱

We recommend a wide variety of Android apps throughout this site. The apps listed here are Android-exclusive and specifically enhance or replace key system functionality.

### Shelter

<div class="admonition recommendation" markdown>

![Shelter 로고](assets/img/android/shelter.svg){ align=right }

**Shelter**는 Android의 직장 프로필 기능을 이용해 기기에서 앱을 격리/복제할 수 있게 해주는 앱입니다.

Shelter는 기본 파일 관리자([DocumentsUI](https://source.android.com/docs/core/architecture/modular-system/documentsui?hl=ko))를 통해 프로필 간 연락처 검색 차단 및 프로필 간 파일 공유를 지원합니다.

[:octicons-repo-16: 저장소](https://gitea.angry.im/PeterCxy/Shelter#shelter){ .md-button .md-button--primary }
[:octicons-code-16:](https://gitea.angry.im/PeterCxy/Shelter){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://www.patreon.com/PeterCxy){ .card-link title=기부 }

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

Shelter is recommended over [Insular](https://secure-system.gitlab.io/Insular/) and [Island](https://github.com/oasisfeng/island) as it supports [contact search blocking](https://secure-system.gitlab.io/Insular/faq.html).

When using Shelter, you are placing complete trust in its developer, as Shelter acts as a [Device Admin](https://developer.android.com/guide/topics/admin/device-admin) to create the Work Profile, and it has extensive access to the data stored within the Work Profile.

</div>

### Secure Camera

<div class="admonition recommendation" markdown>

![Secure camera 로고](assets/img/android/secure_camera.svg#only-light){ align=right }
![Secure camera 로고](assets/img/android/secure_camera-dark.svg#only-dark){ align=right }

**Secure Camera**는 프라이버시, 보안 중점 카메라 앱으로 사진, 동영상, QR 코드를 찍을 수 있습니다. 기기에서 지원하는 경우 CameraX 공급업체 확장 기능(인물 모드, HDR, 야간 모드, 얼굴 보정, 자동) 또한 지원됩니다.

[:octicons-repo-16: Repository](https://github.com/GrapheneOS/Camera){ .md-button .md-button--primary }
[:octicons-info-16:](https://grapheneos.org/usage#camera){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/GrapheneOS/Camera){ .card-link title="Source Code" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.camera.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/Camera/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

주요 프라이버시 기능은 다음과 같습니다:

- [Exif](https://en.wikipedia.org/wiki/Exif) 메타데이터 자동 제거 (기본 활성화)
- 새로운 [미디어](https://developer.android.com/training/data-storage/shared/media) API를 사용하므로 [저장 공간 ](https://developer.android.com/training/data-storage)권한이 필요하지 않습니다.
- 사운드 녹음을 원치 않는 한 마이크 권한은 필요하지 않습니다.

<div class="admonition note" markdown>
<p class="admonition-title">Note</p>

현재 동영상 파일은 메타데이터 제거가 지원되지 않지만, 지원 예정입니다.

이미지 방향 메타데이터는 제거되지 않습니다. (Secure Camera 내에서) 위치 기록을 활성화할 경우, 위치 기록은 제거되지 않습니다. 추후에 제거하려면 [ExifEraser](data-redaction.md#exiferaser) 등의 외부 앱을 사용해야 합니다.

</div>

### Secure PDF Viewer

<div class="admonition recommendation" markdown>

![Secure PDF Viewer 로고](assets/img/android/secure_pdf_viewer.svg#only-light){ align=right }
![Secure PDF Viewer 로고](assets/img/android/secure_pdf_viewer-dark.svg#only-dark){ align=right }

**Secure PDF Viewer**는 [pdf.js](https://en.wikipedia.org/wiki/PDF.js) 기반 PDF 뷰어로, 어떤 권한도 필요하지 않습니다. The PDF is fed into a [sandboxed](https://en.wikipedia.org/wiki/Sandbox_(software_development)) [webview](https://developer.android.com/guide/webapps/webview). This means that it doesn't require permission directly to access content or files.

[Content-Security-Policy](https://en.wikipedia.org/wiki/Content_Security_Policy) is used to enforce that the JavaScript and styling properties within the WebView are entirely static content.

[:octicons-repo-16: Repository](https://github.com/GrapheneOS/PdfViewer){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/GrapheneOS/PdfViewer){ .card-link title="Source Code" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.pdfviewer.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/PdfViewer/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

## Obtaining Applications

### Obtainium

<div class="admonition recommendation" markdown>

![Obtainium logo](assets/img/android/obtainium.svg){ align=right }

**Obtainium** is an app manager which allows you to install and update apps directly from the developer's own releases page (i.e. GitHub, GitLab, the developer's website, etc.), rather than a centralized app store/repository. It supports automatic background updates on Android 12 and higher.

[:octicons-repo-16: Repository](https://github.com/ImranR98/Obtainium#readme){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/ImranR98/Obtainium){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/sponsors/ImranR98){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-github: GitHub](https://github.com/ImranR98/Obtainium/releases)

</details>

</div>

Obtainium allows you to download APK installer files from a wide variety of sources, and it is up to you to ensure those sources and apps are legitimate. For example, using Obtainium to install Signal from [Signal's APK landing page](https://signal.org/android/apk/) should be fine, but installing from third-party APK repositories like Aptoide or APKPure may pose additional risks. The risk of installing a malicious *update* is lower, because Android itself verifies that all app updates are signed by the same developer as the existing app on your phone before installing them.

### GrapheneOS 앱 스토어

GrapheneOS 앱 스토어는 [GitHub](https://github.com/GrapheneOS/Apps/releases)에서 찾을 수 있습니다. 안드로이드 12 이상을 지원하며 자체 업데이트를 지원합니다. 앱 스토어에는 [Auditor](https://attestation.app/), [Camera](https://github.com/GrapheneOS/Camera), [PDF Viewer](https://github.com/GrapheneOS/PdfViewer) 등 GraphneOS 프로젝트에서 제작한 독립 실행형 애플리케이션이 있습니다. 이러한 애플리케이션을 찾는 경우, GrapheneOS 앱 스토어의 앱은 Google이 접근할 수 없는 GrapheneOS 프로젝트 자체 서명으로 서명되어 있으므로, Play 스토어 대신 GrapheneOS 앱 스토어에서 다운로드하실 것을 권장드립니다.

### Aurora Store

Google Play 스토어는 Google 계정 로그인이 필수적이기 때문에 프라이버시 면에서 좋지 않습니다. Aurora Store와 같은 대체 클라이언트를 사용하면 이 문제를 해결할 수 있습니다.

<div class="admonition recommendation" markdown>

![Aurora Store 로고](assets/img/android/aurora-store.webp){ align=right }

**Aurora Store**는 Google 계정, Google Play 서비스, microG 없이 앱을 다운로드할 수 있는 Google Play 스토어 클라이언트입니다.

[:octicons-home-16: Homepage](https://auroraoss.com/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gitlab.com/AuroraOSS/AuroraStore/-/blob/master/POLICY.md){ .card-link title="Privacy Policy" }
[:octicons-code-16:](https://gitlab.com/AuroraOSS/AuroraStore){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-gitlab: GitLab](https://gitlab.com/AuroraOSS/AuroraStore/-/releases)

</details>

</div>

Aurora Store에서는 익명 계정 기능을 사용해 유료 앱은 다운로드 불가능합니다. You can optionally log in with your Google account with Aurora Store to download apps you have purchased, which does give access to the list of apps you've installed to Google, however you still benefit from not requiring the full Google Play client and Google Play Services or microG on your device.

### Manually with RSS Notifications

For apps that are released on platforms like GitHub and GitLab, you may be able to add an RSS feed to your [news aggregator](news-aggregators.md) that will help you keep track of new releases.

![RSS APK](./assets/img/android/rss-apk-light.png#only-light) ![RSS APK](./assets/img/android/rss-apk-dark.png#only-dark) ![APK Changes](./assets/img/android/rss-changes-light.png#only-light) ![APK Changes](./assets/img/android/rss-changes-dark.png#only-dark)

#### GitHub

GitHub에서는 ([Secure Camera](#secure-camera) 예시) [릴리스 페이지](https://github.com/GrapheneOS/Camera/releases)로 이동한 뒤 URL에 `atom`을 추가하면 됩니다:

`https://github.com/GrapheneOS/Camera/releases.atom`

#### GitLab

GitLab에서는 ([Aurora Store](#aurora-store) 예시) [프로젝트 저장소](https://gitlab.com/AuroraOSS/AuroraStore)로 이동한 뒤 URL에 `/-/tags?format=atom`을 추가하면 됩니다:

`https://gitlab.com/AuroraOSS/AuroraStore/-/tags?format=atom`

#### APK 핑거프린트 확인

APK 파일을 다운로드해 수동으로 설치하는 경우, Android [빌드 도구](https://developer.android.com/studio/releases/build-tools)의 일부인 [`apksigner`](https://developer.android.com/studio/command-line/apksigner)를 사용해 앱 서명을 확인할 수 있습니다.

1. [Java JDK](https://www.oracle.com/java/technologies/downloads/)를 설치합니다.

2. [Android 스튜디오 명령줄 도구](https://developer.android.com/studio#command-tools)를 다운로드합니다.

3. 다운로드한 압축 파일을 압축 해제합니다.

    ```bash
    unzip commandlinetools-*.zip
    cd cmdline-tools
    ./bin/sdkmanager --sdk_root=./ "build-tools;29.0.3"
    ```

4. 서명 확인 명령어를 실행합니다:

    ```bash
    ./build-tools/29.0.3/apksigner verify --print-certs ../Camera-37.apk
    ```

5. 이제 결과 해시를 다른 소스와 비교할 수 있습니다. [Signal처럼](https://signal.org/android/apk/) 일부 개발자는 웹사이트에서 인증서 지문을 명시합니다.

    ```bash
    Signer #1 certificate DN: CN=GrapheneOS
    Signer #1 certificate SHA-256 digest: 6436b155b917c2f9a9ed1d15c4993a5968ffabc94947c13f2aeee14b7b27ed59
    Signer #1 certificate SHA-1 digest: 23e108677a2e1b1d6e6b056f3bb951df7ad5570c
    Signer #1 certificate MD5 digest: dbbcd0cac71bd6fa2102a0297c6e0dd3
    ```

### F-Droid

![F-Droid 로고](assets/img/android/f-droid.svg){ align=right width=120px }

==We only recommend F-Droid as a way to obtain apps which cannot be obtained via the means above.== F-Droid is often recommended as an alternative to Google Play, particularly in the privacy community. The option to add third-party repositories and not be confined to Google's walled garden has led to its popularity. F-Droid additionally has [reproducible builds](https://f-droid.org/en/docs/Reproducible_Builds/) for some applications and is dedicated to free and open-source software. However, there are some security-related downsides to how F-Droid builds, signs, and delivers packages:

Due to their process of building apps, apps in the official F-Droid repository often fall behind on updates. F-Droid maintainers also reuse package IDs while signing apps with their own keys, which is not ideal as it gives the F-Droid team ultimate trust. Additionally, the requirements for an app to be included in the official F-Droid repo are less strict than other app stores like Google Play, meaning that F-Droid tends to host a lot more apps which are older, unmaintained, or otherwise no longer meet [modern security standards](https://developer.android.com/google/play/requirements/target-sdk).

Other popular third-party repositories for F-Droid such as [IzzyOnDroid](https://apt.izzysoft.de/fdroid/) alleviate some of these concerns. The IzzyOnDroid repository pulls builds directly from GitHub and is the next best thing to the developers' own repositories. However, it is not something that we can fully recommend, as apps are typically [removed](https://github.com/vfsfitvnm/ViMusic/issues/240#issuecomment-1225564446) from that repository if they are later added to the main F-Droid repository. While that makes sense (since the goal of that particular repository is to host apps before they're accepted into the main F-Droid repository), it can leave you with installed apps which no longer receive updates.

That said, the [F-Droid](https://f-droid.org/en/packages/) and [IzzyOnDroid](https://apt.izzysoft.de/fdroid/) repositories are home to countless apps, so they can be a useful tool to search for and discover open-source apps that you can then download through other means such as the Play Store, Aurora Store, or by getting the APK directly from the developer. You should use your best judgement when looking for new apps via this method, and keep an eye on how frequently the app is updated. Outdated apps may rely on unsupported libraries, among other things, posing a potential security risk.

<div class="admonition note" markdown>
<p class="admonition-title">F-Droid Basic</p>

In some rare cases, the developer of an app will only distribute it through F-Droid ([Gadgetbridge](https://gadgetbridge.org/) is one example of this). If you really need an app like that, we recommend using the newer [F-Droid Basic](https://f-droid.org/en/packages/org.fdroid.basic/) client instead of the original F-Droid app to obtain it. F-Droid Basic can do unattended updates without privileged extension or root, and has a reduced feature set (limiting attack surface).

</div>

## 평가 기준

**Privacy Guides는 권장 목록의 어떠한 프로젝트와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

<div class="admonition example" markdown>
<p class="admonition-title">This section is new</p>

Privacy Guides 팀은 사이트의 모든 항목마다 명확한 평가 기준을 정립하는 중이며, 따라서 세부 내용은 변경될 수 있습니다. 평가 기준에 대해서 질문이 있다면 [포럼에서 문의](https://discuss.privacyguides.net/latest)하시기 바랍니다. (무언가가 목록에 존재하지 않다고 해서 권장 목록을 작성할 때 고려한 적이 없을 것으로 단정 짓지 마세요.) 권장 목록에 어떤 프로젝트를 추가할 때 고려하고 논의해야 할 요소는 매우 많으며, 모든 요소를 문서화하는 것은 현재 진행 중인 작업입니다.

</div>

### 운영 체제

- 오픈 소스 소프트웨어여야 합니다.
- 부트로더 잠금 시 사용자 지정 AVB 키를 사용할 수 있도록 지원해야 합니다.
- Android 메이저 업데이트는 출시 1개월 이내에 제공되어야 합니다.
- Android 기능 업데이트(마이너 버전)은 출시 14일 이내에 제공되어야 합니다.
- 정기적인 보안 패치는 출시 5일 이내에 제공되어야 합니다.
- 기본적으로 루팅이 되어있어서는 **안 됩니다**.
- Google Play 서비스가 기본적으로 활성화된 상태로 제공되어서는 **안 됩니다**.
- Google Play 서비스를 활성화하기 위해 시스템 수정이 필요해서는 **안 됩니다**.

### 기기

- 권장 운영 체제 중 한 가지 이상을 지원해야 합니다.
- 현재 새 제품을 팔고 있어야 합니다.
- 최소 5년 이상 보안 업데이트를 받아야 합니다.
- 전용 보안 칩(Secure Element) 하드웨어가 장착되어 있어야 합니다.

### 애플리케이션

- 본 페이지에 등재된 애플리케이션은 Privacy Guides 사이트의 다른 소프트웨어 카테고리에 해당되지 않아야 합니다.
- 일반 애플리케이션은 핵심 시스템 기능을 확장하거나 대체해야 합니다.
- 애플리케이션은 꾸준한 업데이트 및 유지 관리가 이루어져야 합니다.
