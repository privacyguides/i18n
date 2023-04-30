---
meta_title: "Android Recommendations: GrapheneOS and DivestOS - Privacy Guides"
title: "Android"
icon: 'simple/android'
description: You can replace the operating system on your Android phone with these secure and privacy-respecting alternatives.
cover: android.png
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
    sameAs: https://ko.wikipedia.org/wiki/%EC%95%88%EB%93%9C%EB%A1%9C%EC%9D%B4%EB%93%9C_(%EC%9A%B4%EC%98%81%EC%B2%B4%EC%A0%9C)
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
    sameAs: https://ko.wikipedia.org/wiki/%EA%B5%AC%EA%B8%80_%ED%94%BD%EC%85%80
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

![Android logo](assets/img/android/android.svg){ align=right }

The **Android Open Source Project** is an open-source mobile operating system led by Google which powers the majority of the world's mobile devices. Most phones sold with Android are modified to include invasive integrations and apps such as Google Play Services, so you can significantly improve your privacy on your mobile device by replacing your phone's default installation with a version of Android without these invasive features.

[:octicons-home-16:](https://source.android.com/){ .card-link title=Homepage }
[:octicons-info-16:](https://source.android.com/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://cs.android.com/android/platform/superproject/){ .card-link title="Source Code" }

These are the Android operating systems, devices, and apps we recommend to maximize your mobile device's security and privacy. To learn more about Android:

[General Android Overview :material-arrow-right-drop-circle:](os/android-overview.md ""){.md-button}

## AOSP 기반

We recommend installing one of these custom Android operating systems on your device, listed in order of preference, depending on your device's compatibility with these operating systems.

!!! note "참고"

    End-of-life devices (such as GrapheneOS or CalyxOS's "extended support" devices) do not have full security patches (firmware updates) due to the OEM discontinuing support. These devices cannot be considered completely secure regardless of installed software.

### GrapheneOS

!!! recommendation

    ![GrapheneOS 로고](assets/img/android/grapheneos.svg#only-light){ align=right }
    ![GrapheneOS 로고](assets/img/android/grapheneos-dark.svg#only-dark){ align=right }
    
    **GrapheneOS**는 프라이버시 및 보안 면에서 최고의 선택입니다.
    
    GraphneOS는 추가적인 [보안 강화(Security Hardening)](https://en.wikipedia.org/wiki/Hardening_(computing))와 프라이버시 강화 기능을 제공합니다. It has a [hardened memory allocator](https://github.com/GrapheneOS/hardened_malloc), network and sensor permissions, and various other [security features](https://grapheneos.org/features). GrapheneOS also comes with full firmware updates and signed builds, so verified boot is fully supported.
    
    [:octicons-home-16: 홈페이지](https://grapheneos.org/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://grapheneos.org/faq#privacy-policy){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://grapheneos.org/faq){ .card-link title=문서}
    [:octicons-code-16:](https://grapheneos.org/source){ .card-link title="소스 코드" }
    [:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=기부 }

GrapheneOS supports [Sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), which runs [Google Play Services](https://en.wikipedia.org/wiki/Google_Play_Services) fully sandboxed like any other regular app. This means you can take advantage of most Google Play Services, such as [push notifications](https://firebase.google.com/docs/cloud-messaging/), while giving you full control over their permissions and access, and while containing them to a specific [work profile](os/android-overview.md#work-profile) or [user profile](os/android-overview.md#user-profiles) of your choice.

Google Pixel 스마트폰은 현재 GpapheneOS [하드웨어 보안 요구 사항](https://grapheneos.org/faq#device-support)을 충족하는 유일한 기기입니다.

[CalyxOS보다 GrapheneOS를 추천하는 이유 :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/04/21/grapheneos-or-calyxos/ ""){.md-button}

### DivestOS

!!! recommendation

    ![DivestOS 로고](assets/img/android/divestos.svg){ align=right }
    
    **DivestOS**는 [LineageOS](https://lineageos.org/)의 소프트 포크입니다.
    DivestOS는 LineageOS의 다양한 [지원 기기](https://divestos.org/index.php?page=devices&base=LineageOS)를 물려받았습니다. 서명된 빌드가 존재하여, Pixel 외 기기에서 [검증 부팅(Verified Boot)](https://source.android.com/security/verifiedboot)을 사용할 수 있습니다.
    
    [:octicons-home-16: 홈페이지](https://divestos.org){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://divestoseb5nncsydt7zzf5hrfg44md4bxqjs5ifcv4t7gt7u6ohjyyd.onion){ .card-link title="Onion 서비스" }
    [:octicons-eye-16:](https://divestos.org/index.php?page=privacy_policy){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://divestos.org/index.php?page=faq){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/divested-mobile){ .card-link title="소스 코드" }
    [:octicons-heart-16:](https://divested.dev/index.php?page=donate){ .card-link title=기부 }

DivestOS has automated kernel vulnerability ([CVE](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures)) [patching](https://gitlab.com/divested-mobile/cve_checker), fewer proprietary blobs, and a custom [hosts](https://divested.dev/index.php?page=dnsbl) file. Its hardened WebView, [Mulch](https://gitlab.com/divested-mobile/mulch), enables [CFI](https://en.wikipedia.org/wiki/Control-flow_integrity) for all architectures and [network state partitioning](https://developer.mozilla.org/en-US/docs/Web/Privacy/State_Partitioning), and receives out-of-band updates. DivestOS also includes kernel patches from GrapheneOS and enables all available kernel security features via [defconfig hardening](https://github.com/Divested-Mobile/DivestOS-Build/blob/master/Scripts/Common/Functions.sh#L758). All kernels newer than version 3.4 include full page [sanitization](https://lwn.net/Articles/334747/) and all ~22 Clang-compiled kernels have [`-ftrivial-auto-var-init=zero`](https://reviews.llvm.org/D54604?id=174471) enabled.

DivestOS implements some system hardening patches originally developed for GrapheneOS. DivestOS 16.0 and higher implements GrapheneOS's [`INTERNET`](https://developer.android.com/training/basics/network-ops/connecting) and SENSORS permission toggle, [hardened memory allocator](https://github.com/GrapheneOS/hardened_malloc), [exec-spawning](https://blog.privacyguides.org/2022/04/21/grapheneos-or-calyxos/#additional-hardening), [JNI](https://en.wikipedia.org/wiki/Java_Native_Interface) [constification](https://en.wikipedia.org/wiki/Const_(computer_programming)), and partial [bionic](https://en.wikipedia.org/wiki/Bionic_(software)) hardening patchsets. 17.1 and higher features GrapheneOS's per-network full [MAC randomization](https://en.wikipedia.org/wiki/MAC_address#Randomization) option, [`ptrace_scope`](https://www.kernel.org/doc/html/latest/admin-guide/LSM/Yama.html) control, and automatic reboot/Wi-Fi/Bluetooth [timeout options](https://grapheneos.org/features).

DivestOS uses F-Droid as its default app store. Normally, we would recommend avoiding F-Droid due to its numerous [security issues](#f-droid). However, doing so on DivestOS isn't viable; the developers update their apps via their own F-Droid repositories ([DivestOS Official](https://divestos.org/fdroid/official/?fingerprint=E4BE8D6ABFA4D9D4FEEF03CDDA7FF62A73FD64B75566F6DD4E5E577550BE8467) and [DivestOS WebView](https://divestos.org/fdroid/webview/?fingerprint=FB426DA1750A53D7724C8A582B4D34174E64A84B38940E5D5A802E1DFF9A40D2)). We recommend disabling the official F-Droid app and using [Neo Store](https://github.com/NeoApplications/Neo-Store/) with the DivestOS repositories enabled to keep those components up to date. For other apps, our recommended methods of obtaining them still apply.

!!! warning "경고"

    DivestOS 펌웨어 업데이트의 [세부 상태](https://gitlab.com/divested-mobile/firmware-empty/-/blob/master/STATUS) 및 품질 관리는 지원하는 기기에 따라 다릅니다. GrapheneOS와 호환되는 기기라면 GrapheneOS를 권장합니다. GrapheneOS 미지원 기기의 경우, DivestOS는 좋은 대체제입니다.
    
    검증 부팅은 모든 지원 기기에서 사용 가능한 것은 아니며, 일부 기기는 다른 기기보다 더 원활할 수 있습니다.

## Android 기기

기기를 구매할 때는 가급적 최신 제품을 구입해야 합니다. 모바일 기기의 소프트웨어와 펌웨어 지원 기간은 제한되어 있으므로, 최신 제품을 구입해야 최대한 수명을 늘릴 수 있습니다.

이동 통신사로부터 휴대폰을 사는 것은 지양해야 합니다. 이동 통신사에서 판매하는 휴대폰은 보통 **부트로더 잠금**이 걸려 있으며, [OEM 잠금 해제](https://source.android.com/devices/bootloader/locking_unlocking)를 지원하지 않습니다. 이 경우, 어떤 종류의 대체 Android 배포판도 설치할 수 없습니다.

온라인에서 중고 휴대폰을 구입할 때에는 매우 **주의해야** 합니다. 판매자의 평판을 항상 확인하세요. 만약 해당 기기가 도난된 기기였을 경우, [IMEI 블랙리스트](https://www.gsma.com/security/resources/imei-blacklisting/)에 등재될 가능성이 있습니다. 또한 이전 소유자의 활동과 연관될 수 있다는 위험성도 존재합니다.

Android 기기 및 운영 체제 호환성에 관한 추가 정보:

- 수명이 다했거나 거의 다한 기기는 구매하지 마세요. 제조업체에서 추가 펌웨어 업데이트가 제공되는 기기를 구매해야 합니다.
- LineageOS나 /e/ OS가 사전 설치된 휴대폰이나, 적절한 [자체 검사 부팅(Verified Boot)](https://source.android.com/security/verifiedboot) 지원 혹은 펌웨어 업데이트가 없는 Android 휴대폰을 구매하지 마세요. 이러한 기기는 조작되었는지 여부를 확인할 방법이 없습니다.
- 요런대, 어떤 기기나 Android 배포판이 여기에 등재되지 않은 경우에는 그럴 만한 이유가 있을 겁니다. 자세한 내용은 [포럼](https://discuss.privacyguides.net/)을 참고해 주세요.

### Google Pixel

Google Pixel은 Privacy Guides에서 **유일하게** 구매를 권장하는 기기입니다. Pixel 스마트폰은 현재 시중에 존재하는 어떤 Android 기기보다도 강력한 하드웨어 보안을 가지고 있습니다. 제3자 운영 체제에 대한 적절한 AVB 지원이 갖추어져 있으며, Secure Element 역할 Google 커스텀 [Titan](https://security.googleblog.com/2021/10/pixel-6-setting-new-standard-for-mobile.html) 보안 칩을 탑재하고 있습니다.

!!! recommendation

    ![Google Pixel 6](assets/img/android/google-pixel.png){ align=right }
    
    **Google Pixel** devices are known to have good security and properly support [Verified Boot](https://source.android.com/security/verifiedboot), even when installing custom operating systems.
    
    Beginning with the **Pixel 6** and **6 Pro**, Pixel devices receive a minimum of 5 years of guaranteed security updates, ensuring a much longer lifespan compared to the 2-4 years competing OEMs typically offer.
    
    [:material-shopping: Store](https://store.google.com/category/phones){ .md-button .md-button--primary }

Secure Elements like the Titan M2 are more limited than the processor's Trusted Execution Environment used by most other phones as they are only used for secrets storage, hardware attestation, and rate limiting, not for running "trusted" programs. Phones without a Secure Element have to use the TEE for *all* of those functions, resulting in a larger attack surface.

Google Pixel phones use a TEE OS called Trusty which is [open-source](https://source.android.com/security/trusty#whyTrusty), unlike many other phones.

The installation of GrapheneOS on a Pixel phone is easy with their [web installer](https://grapheneos.org/install/web). If you don't feel comfortable doing it yourself and are willing to spend a bit of extra money, check out the [NitroPhone](https://shop.nitrokey.com/shop) as they come preloaded with GrapheneOS from the reputable [Nitrokey](https://www.nitrokey.com/about) company.

A few more tips for purchasing a Google Pixel:

- If you're after a bargain on a Pixel device, we suggest buying an "**a**" model, just after the next flagship is released. Discounts are usually available because Google will be trying to clear their stock.
- Consider price beating options and specials offered at physical stores.
- Look at online community bargain sites in your country. These can alert you to good sales.
- Google provides a list showing the [support cycle](https://support.google.com/nexus/answer/4457705) for each one of their devices. The price per day for a device can be calculated as: $\text{Cost} \over \text {EOL Date}-\text{Current Date}$, meaning that the longer use of the device the lower cost per day.

## 일반 앱

We recommend a wide variety of Android apps throughout this site. The apps listed here are Android-exclusive and specifically enhance or replace key system functionality.

### Shelter

!!! recommendation

    ![Shelter logo](assets/img/android/shelter.svg){ align=right }
    
    **Shelter** is an app that helps you leverage Android's Work Profile functionality to isolate or duplicate apps on your device.
    
    Shelter supports blocking contact search cross profiles and sharing files across profiles via the default file manager ([DocumentsUI](https://source.android.com/devices/architecture/modular-system/documentsui)).
    
    [:octicons-repo-16: 저장소](https://gitea.angry.im/PeterCxy/Shelter#shelter){ .md-button .md-button--primary }
    [:octicons-code-16:](https://gitea.angry.im/PeterCxy/Shelter){ .card-link title="소스 코드" }
    [:octicons-heart-16:](https://www.patreon.com/PeterCxy){ .card-link title=기부 }

!!! warning "경고"

    Shelter is recommended over [Insular](https://secure-system.gitlab.io/Insular/) and [Island](https://github.com/oasisfeng/island) as it supports [contact search blocking](https://secure-system.gitlab.io/Insular/faq.html).
    
    When using Shelter, you are placing complete trust in its developer, as Shelter acts as a [Device Admin](https://developer.android.com/guide/topics/admin/device-admin) to create the Work Profile, and it has extensive access to the data stored within the Work Profile.

### Auditor

!!! recommendation

    ![Auditor logo](assets/img/android/auditor.svg#only-light){ align=right }
    ![Auditor logo](assets/img/android/auditor-dark.svg#only-dark){ align=right }
    
    **Auditor** is an app which leverages hardware security features to provide device integrity monitoring by actively validating the identity of a device and the integrity of its operating system. Currently, it only works with GrapheneOS or the stock operating system for [supported devices](https://attestation.app/about#device-support).
    
    [:octicons-home-16: 홈페이지](https://attestation.app){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://attestation.app/privacy-policy){ .card-link title="프라이버시 정책" }
    [:octicons-info-16:](https://attestation.app/about){ .card-link title=문서}
    [:octicons-code-16:](https://attestation.app/source){ .card-link title="소스 코드" }
    [:octicons-heart-16:](https://attestation.app/donate){ .card-link title=기부 }
    
    ??? downloads "다운로드"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.attestation.auditor.play)
        - [:simple-github: GitHub](https://github.com/GrapheneOS/Auditor/releases)
        - [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

Auditor performs attestation and intrusion detection by:

- Using a [Trust On First Use (TOFU)](https://en.wikipedia.org/wiki/Trust_on_first_use) model between an *auditor* and *auditee*, the pair establish a private key in the [hardware-backed keystore](https://source.android.com/security/keystore/) of the *Auditor*.
- The *auditor* can either be another instance of the Auditor app or the [Remote Attestation Service](https://attestation.app).
- The *auditor* records the current state and configuration of the *auditee*.
- Should tampering with the operating system of the *auditee* happen after the pairing is complete, the auditor will be aware of the change in the device state and configurations.
- You will be alerted to the change.

No personally identifiable information is submitted to the attestation service. We recommend that you sign up with an anonymous account and enable remote attestation for continuous monitoring.

If your [threat model](basics/threat-modeling.md) requires privacy, you could consider using [Orbot](tor.md#orbot) or a VPN to hide your IP address from the attestation service. To make sure that your hardware and operating system is genuine, [perform local attestation](https://grapheneos.org/install/web#verifying-installation) immediately after the device has been installed and prior to any internet connection.

### Secure Camera

!!! recommendation

    ![Secure camera 로고](assets/img/android/secure_camera.svg#only-light){ align=right }
    ![Secure camera 로고](assets/img/android/secure_camera-dark.svg#only-dark){ align=right }
    
    **Secure Camera**는 프라이버시, 보안 중점 카메라 앱으로 사진, 동영상, QR 코드를 찍을 수 있습니다. 기기에서 지원하는 경우 CameraX 공급업체 확장 기능(인물 모드, HDR, 야간 모드, 얼굴 보정, 자동) 또한 지원됩니다.
    
    [:octicons-repo-16: 저장소](https://github.com/GrapheneOS/Camera){ .md-button .md-button--primary }
    [:octicons-info-16:](https://grapheneos.org/usage#camera){ .card-link title=문서}
    [:octicons-code-16:](https://github.com/GrapheneOS/Camera){ .card-link title="소스 코드" }
    [:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=기부 }
    
    ??? downloads "다운로드"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.camera.play)
        - [:simple-github: GitHub](https://github.com/GrapheneOS/Camera/releases)
        - [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

주요 프라이버시 기능은 다음과 같습니다:

- [Exif](https://en.wikipedia.org/wiki/Exif) 메타데이터 자동 제거 (기본 활성화)
- 새로운 [미디어](https://developer.android.com/training/data-storage/shared/media) API를 사용하므로 [저장 공간 ](https://developer.android.com/training/data-storage)권한이 필요하지 않습니다.
- 사운드 녹음을 원치 않는 한 마이크 권한은 필요하지 않습니다.

!!! note "참고"

    현재 동영상 파일은 메타데이터 제거가 지원되지 않지만, 지원 예정입니다.
    
    이미지 방향 메타데이터는 제거되지 않습니다. (Secure Camera 내에서) 위치 기록을 활성화할 경우, 위치 기록은 제거되지 않습니다. 추후에 제거하려면 [ExifEraser](data-redaction.md#exiferaser) 등의 외부 앱을 사용해야 합니다.

### Secure PDF Viewer

!!! recommendation

    ![Secure PDF Viewer 로고](assets/img/android/secure_pdf_viewer.svg#only-light){ align=right }
    ![Secure PDF Viewer 로고](assets/img/android/secure_pdf_viewer-dark.svg#only-dark){ align=right }
    
    **Secure PDF Viewer**는 [pdf.js](https://en.wikipedia.org/wiki/PDF.js) 기반 PDF 뷰어로, 어떤 권한도 필요하지 않습니다. The PDF is fed into a [sandboxed](https://en.wikipedia.org/wiki/Sandbox_(software_development)) [webview](https://developer.android.com/guide/webapps/webview). This means that it doesn't require permission directly to access content or files.
    
    [Content-Security-Policy](https://en.wikipedia.org/wiki/Content_Security_Policy) is used to enforce that the JavaScript and styling properties within the WebView are entirely static content.
    
    [:octicons-repo-16: Repository](https://github.com/GrapheneOS/PdfViewer){ .md-button .md-button--primary }
    [:octicons-code-16:](https://github.com/GrapheneOS/PdfViewer){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.pdfviewer.play)
        - [:simple-github: GitHub](https://github.com/GrapheneOS/PdfViewer/releases)
        - [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

## Obtaining Applications

### GrapheneOS App Store

GrapheneOS's app store is available on [GitHub](https://github.com/GrapheneOS/Apps/releases). It supports Android 12 and above and is capable of updating itself. The app store has standalone applications built by the GrapheneOS project such as the [Auditor](https://attestation.app/), [Camera](https://github.com/GrapheneOS/Camera), and [PDF Viewer](https://github.com/GrapheneOS/PdfViewer). If you are looking for these applications, we highly recommend that you get them from GrapheneOS's app store instead of the Play Store, as the apps on their store are signed by the GrapheneOS's project own signature that Google does not have access to.

### Aurora Store

The Google Play Store requires a Google account to login which is not great for privacy. You can get around this by using an alternative client, such as Aurora Store.

!!! recommendation

    ![Aurora Store logo](assets/img/android/aurora-store.webp){ align=right }
    
    **Aurora Store** is a Google Play Store client which does not require a Google Account, Google Play Services, or microG to download apps.
    
    [:octicons-home-16: Homepage](https://auroraoss.com/){ .md-button .md-button--primary }
    [:octicons-code-16:](https://gitlab.com/AuroraOSS/AuroraStore){ .card-link title="Source Code" }
    
    ??? downloads
    
        - [:simple-gitlab: GitLab](https://gitlab.com/AuroraOSS/AuroraStore/-/releases)

Aurora Store does not allow you to download paid apps with their anonymous account feature. You can optionally log in with your Google account with Aurora Store to download apps you have purchased, which does give access to the list of apps you've installed to Google, however you still benefit from not requiring the full Google Play client and Google Play Services or microG on your device.

### Manually with RSS Notifications

For apps that are released on platforms like GitHub and GitLab, you may be able to add an RSS feed to your [news aggregator](/news-aggregators) that will help you keep track of new releases.

![RSS APK](./assets/img/android/rss-apk-light.png#only-light) ![RSS APK](./assets/img/android/rss-apk-dark.png#only-dark) ![APK Changes](./assets/img/android/rss-changes-light.png#only-light) ![APK Changes](./assets/img/android/rss-changes-dark.png#only-dark)

#### GitHub

GitHub에서는 ([Secure Camera](#secure-camera) 예시) [릴리스 페이지](https://github.com/GrapheneOS/Camera/releases)로 이동한 뒤 URL에 `atom`을 추가하면 됩니다:

`https://github.com/GrapheneOS/Camera/releases.atom`

#### GitLab

GitLab에서는 ([Aurora Store](#aurora-store) 예시) [프로젝트 저장소](https://gitlab.com/AuroraOSS/AuroraStore)로 이동한 뒤 URL에 `/-/tags?format=atom`을 추가하면 됩니다:

`https://gitlab.com/AuroraOSS/AuroraStore/-/tags?format=atom`

#### Verifying APK Fingerprints

If you download APK files to install manually, you can verify their signature with the [`apksigner`](https://developer.android.com/studio/command-line/apksigner) tool, which is a part of Android [build-tools](https://developer.android.com/studio/releases/build-tools).

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

![F-Droid logo](assets/img/android/f-droid.svg){ align=right width=120px }

==We do **not** currently recommend F-Droid as a way to obtain apps.== F-Droid is often recommended as an alternative to Google Play, particularly in the privacy community. The option to add third-party repositories and not be confined to Google's walled garden has led to its popularity. F-Droid additionally has [reproducible builds](https://f-droid.org/en/docs/Reproducible_Builds/) for some applications and is dedicated to free and open-source software. However, there are [notable problems](https://privsec.dev/posts/android/f-droid-security-issues/) with the official F-Droid client, their quality control, and how they build, sign, and deliver packages.

Due to their process of building apps, apps in the official F-Droid repository often fall behind on updates. F-Droid maintainers also reuse package IDs while signing apps with their own keys, which is not ideal as it gives the F-Droid team ultimate trust.

Other popular third-party repositories such as [IzzyOnDroid](https://apt.izzysoft.de/fdroid/) alleviate some of these concerns. The IzzyOnDroid repository pulls builds directly from GitHub and is the next best thing to the developers' own repositories. However, it is not something that we can recommend, as apps are typically [removed](https://github.com/vfsfitvnm/ViMusic/issues/240#issuecomment-1225564446) from that respository when they make it to the main F-Droid repository. While that makes sense (since the goal of that particular repository is to host apps before they're accepted into the main F-Droid repository), it can leave you with installed apps which no longer receive updates.

That said, the [F-Droid](https://f-droid.org/en/packages/) and [IzzyOnDroid](https://apt.izzysoft.de/fdroid/) repositories are home to countless apps, so they can be a useful tool to search for and discover open-source apps that you can then download through Play Store, Aurora Store, or by getting the APK directly from the developer. It is important to keep in mind that some apps in these repositories have not been updated in years and may rely on unsupported libraries, among other things, posing a potential security risk. You should use your best judgement when looking for new apps via this method.

!!! note "참고"

    In some rare cases, the developer of an app will only distribute it through F-Droid ([Gadgetbridge](https://gadgetbridge.org/) is one example of this). If you really need an app like that, we recommend using [Neo Store](https://github.com/NeoApplications/Neo-Store/) instead of the official F-Droid app to obtain it.

## 평가 기준

**Privacy Guides는 권장 목록의 어떠한 프로젝트와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

!!! example "이 단락은 최근에 만들어졌습니다"

    Privacy Guides 팀은 사이트의 모든 항목마다 명확한 평가 기준을 정립하는 중이며, 따라서 세부 내용은 변경될 수 있습니다. 평가 기준에 대해서 질문이 있다면 [포럼에서 문의](https://discuss.privacyguides.net/latest)하시기 바랍니다. (무언가가 목록에 존재하지 않다고 해서 권장 목록을 작성할 때 고려한 적이 없을 것으로 단정 짓지 마세요.) 권장 목록에 어떤 프로젝트를 추가할 때 고려하고 논의해야 할 요소는 매우 많으며, 모든 요소를 문서화하는 것은 현재 진행 중인 작업입니다.

### 운영 체제

- 오픈 소스 소프트웨어여야 합니다.
- Must support bootloader locking with custom AVB key support.
- Must receive major Android updates within 0-1 months of release.
- Must receive Android feature updates (minor version) within 0-14 days of release.
- Must receive regular security patches within 0-5 days of release.
- Must **not** be "rooted" out of the box.
- Must **not** enable Google Play Services by default.
- Must **not** require system modification to support Google Play Services.

### 기기

- Must support at least one of our recommended custom operating systems.
- 현재 새 제품을 팔고 있어야 합니다.
- 최소 5년 이상 보안 업데이트를 받아야 합니다.
- 전용 보안 칩(Secure Element) 하드웨어가 장착되어 있어야 합니다.

### 애플리케이션

- Applications on this page must not be applicable to any other software category on the site.
- General applications should extend or replace core system functionality.
- Applications should receive regular updates and maintenance.
