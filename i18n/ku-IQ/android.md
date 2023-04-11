---
title: "ئەندرۆید"
icon: 'simple/android'
description: '﻿دەتوانیت سیستەمی کارپێکردن سەر تەلەفۆنی ئەندرۆیدەکەت بگۆڕیت بۆ ئەم جێگرەوانەی، کە پارێزراو و ڕێزگرن لە تایبەتمەندێتی.'
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

![Android logo](assets/img/android/android.svg){ align=right }

**پڕۆژەی ئەندرۆیدی سەرچاوەکراوە** سیستەمی سەرچاوەکراوەی کارپێکردنی مۆبایلە کە لە لایەن گووگڵەوە بەڕێوەدەبرێت, کە زۆربەی ئامێرەکانی مۆبایل لە جیهاندا بەکاردێت. Most phones sold with Android are modified to include invasive integrations and apps such as Google Play Services, so you can significantly improve your privacy on your mobile device by replacing your phone's default installation with a version of Android without these invasive features.

[:octicons-home-16:](https://source.android.com/){ .card-link title=Homepage }
[:octicons-info-16:](https://source.android.com/docs){ .card-link title=Documentation}
[:octicons-code-16:](https://cs.android.com/android/platform/superproject/){ .card-link title="Source Code" }

These are the Android operating systems, devices, and apps we recommend to maximize your mobile device's security and privacy. To learn more about Android:

[General Android Overview :material-arrow-right-drop-circle:](os/android-overview.md ""){.md-button}

[Why we recommend GrapheneOS over CalyxOS :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/04/21/grapheneos-or-calyxos/ ""){.md-button}

## AOSP Derivatives

We recommend installing one of these custom Android operating systems on your device, listed in order of preference, depending on your device's compatibility with these operating systems.

!!! note

    End-of-life devices (such as GrapheneOS or CalyxOS's "extended support" devices) do not have full security patches (firmware updates) due to the OEM discontinuing support. These devices cannot be considered completely secure regardless of installed software.

### GrapheneOS

!!! recommendation

    ![GrapheneOS logo](assets/img/android/grapheneos.svg#only-light){ align=right }
    ![GrapheneOS logo](assets/img/android/grapheneos-dark.svg#only-dark){ align=right }
    
    **GrapheneOS** is the best choice when it comes to privacy and security.
    
    GrapheneOS provides additional [security hardening](https://en.wikipedia.org/wiki/Hardening_(computing)) and privacy improvements. It has a [hardened memory allocator](https://github.com/GrapheneOS/hardened_malloc), network and sensor permissions, and various other [security features](https://grapheneos.org/features). GrapheneOS also comes with full firmware updates and signed builds, so verified boot is fully supported.
    
    [:octicons-home-16: Homepage](https://grapheneos.org/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://grapheneos.org/faq#privacy-policy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://grapheneos.org/faq){ .card-link title=Documentation}
    [:octicons-code-16:](https://grapheneos.org/source){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribute }

GrapheneOS supports [Sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), which runs [Google Play Services](https://en.wikipedia.org/wiki/Google_Play_Services) fully sandboxed like any other regular app. This means you can take advantage of most Google Play Services, such as [push notifications](https://firebase.google.com/docs/cloud-messaging/), while giving you full control over their permissions and access, and while containing them to a specific [work profile](os/android-overview.md#work-profile) or [user profile](os/android-overview.md#user-profiles) of your choice.

Google Pixel phones are the only devices that currently meet GrapheneOS's [hardware security requirements](https://grapheneos.org/faq#device-support).

### DivestOS

!!! recommendation

    ![DivestOS logo](assets/img/android/divestos.svg){ align=right }
    
    **DivestOS** is a soft-fork of [LineageOS](https://lineageos.org/).
    DivestOS inherits many [supported devices](https://divestos.org/index.php?page=devices&base=LineageOS) from LineageOS. It has signed builds, making it possible to have [verified boot](https://source.android.com/security/verifiedboot) on some non-Pixel devices.
    
    [:octicons-home-16: Homepage](https://divestos.org){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://divestoseb5nncsydt7zzf5hrfg44md4bxqjs5ifcv4t7gt7u6ohjyyd.onion){ .card-link title="Onion Service" }
    [:octicons-eye-16:](https://divestos.org/index.php?page=privacy_policy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://divestos.org/index.php?page=faq){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/divested-mobile){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://divested.dev/index.php?page=donate){ .card-link title=Contribute }

DivestOS has automated kernel vulnerability ([CVE](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures)) [patching](https://gitlab.com/divested-mobile/cve_checker), fewer proprietary blobs, and a custom [hosts](https://divested.dev/index.php?page=dnsbl) file. Its hardened WebView, [Mulch](https://gitlab.com/divested-mobile/mulch), enables [CFI](https://en.wikipedia.org/wiki/Control-flow_integrity) for all architectures and [network state partitioning](https://developer.mozilla.org/en-US/docs/Web/Privacy/State_Partitioning), and receives out-of-band updates. DivestOS also includes kernel patches from GrapheneOS and enables all available kernel security features via [defconfig hardening](https://github.com/Divested-Mobile/DivestOS-Build/blob/master/Scripts/Common/Functions.sh#L758). All kernels newer than version 3.4 include full page [sanitization](https://lwn.net/Articles/334747/) and all ~22 Clang-compiled kernels have [`-ftrivial-auto-var-init=zero`](https://reviews.llvm.org/D54604?id=174471) enabled.

DivestOS implements some system hardening patches originally developed for GrapheneOS. DivestOS 16.0 and higher implements GrapheneOS's [`INTERNET`](https://developer.android.com/training/basics/network-ops/connecting) and SENSORS permission toggle, [hardened memory allocator](https://github.com/GrapheneOS/hardened_malloc), [exec-spawning](https://blog.privacyguides.org/2022/04/21/grapheneos-or-calyxos/#additional-hardening), [JNI](https://en.wikipedia.org/wiki/Java_Native_Interface) [constification](https://en.wikipedia.org/wiki/Const_(computer_programming)), and partial [bionic](https://en.wikipedia.org/wiki/Bionic_(software)) hardening patchsets. 17.1 and higher features GrapheneOS's per-network full [MAC randomization](https://en.wikipedia.org/wiki/MAC_address#Randomization) option, [`ptrace_scope`](https://www.kernel.org/doc/html/latest/admin-guide/LSM/Yama.html) control, and automatic reboot/Wi-Fi/Bluetooth [timeout options](https://grapheneos.org/features).

DivestOS uses F-Droid as its default app store. Normally, we would recommend avoiding F-Droid due to its numerous [security issues](#f-droid). However, doing so on DivestOS isn't viable; the developers update their apps via their own F-Droid repositories ([DivestOS Official](https://divestos.org/fdroid/official/?fingerprint=E4BE8D6ABFA4D9D4FEEF03CDDA7FF62A73FD64B75566F6DD4E5E577550BE8467) and [DivestOS WebView](https://divestos.org/fdroid/webview/?fingerprint=FB426DA1750A53D7724C8A582B4D34174E64A84B38940E5D5A802E1DFF9A40D2)). We recommend disabling the official F-Droid app and using [Neo Store](https://github.com/NeoApplications/Neo-Store/) with the DivestOS repositories enabled to keep those components up to date. For other apps, our recommended methods of obtaining them still apply.

!!! warning

    DivestOS firmware update [status](https://gitlab.com/divested-mobile/firmware-empty/-/blob/master/STATUS) and quality control varies across the devices it supports. We still recommend GrapheneOS depending on your device's compatibility. For other devices, DivestOS is a good alternative.
    
    Not all of the supported devices have verified boot, and some perform it better than others.

## Android Devices

When purchasing a device, we recommend getting one as new as possible. The software and firmware of mobile devices are only supported for a limited time, so buying new extends that lifespan as much as possible.

Avoid buying phones from mobile network operators. These often have a **locked bootloader** and do not support [OEM unlocking](https://source.android.com/devices/bootloader/locking_unlocking). These phone variants will prevent you from installing any kind of alternative Android distribution.

Be very **careful** about buying second hand phones from online marketplaces. Always check the reputation of the seller. If the device is stolen, there's a possibility of [IMEI blacklisting](https://www.gsma.com/security/resources/imei-blacklisting/). There is also a risk involved with you being associated with the activity of the previous owner.

A few more tips regarding Android devices and operating system compatibility:

- Do not buy devices that have reached or are near their end-of-life, additional firmware updates must be provided by the manufacturer.
- Do not buy preloaded LineageOS or /e/ OS phones or any Android phones without proper [Verified Boot](https://source.android.com/security/verifiedboot) support and firmware updates. These devices also have no way for you to check whether they've been tampered with.
- In short, if a device or Android distribution is not listed here, there is probably a good reason. Check out our [forum](https://discuss.privacyguides.net/) to find details!

### Google Pixel

Google Pixel phones are the **only** devices we recommend for purchase. Pixel phones have stronger hardware security than any other Android devices currently on the market, due to proper AVB support for third-party operating systems and Google's custom [Titan](https://security.googleblog.com/2021/10/pixel-6-setting-new-standard-for-mobile.html) security chips acting as the Secure Element.

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

## General Apps

We recommend a wide variety of Android apps throughout this site. The apps listed here are Android-exclusive and specifically enhance or replace key system functionality.

### Shelter

!!! recommendation

    ![Shelter logo](assets/img/android/shelter.svg){ align=right }
    
    **Shelter** is an app that helps you leverage Android's Work Profile functionality to isolate or duplicate apps on your device.
    
    Shelter supports blocking contact search cross profiles and sharing files across profiles via the default file manager ([DocumentsUI](https://source.android.com/devices/architecture/modular-system/documentsui)).
    
    [:octicons-repo-16: Repository](https://gitea.angry.im/PeterCxy/Shelter#shelter){ .md-button .md-button--primary }
    [:octicons-code-16:](https://gitea.angry.im/PeterCxy/Shelter){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://www.patreon.com/PeterCxy){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.typeblog.shelter)

!!! warning

    Shelter is recommended over [Insular](https://secure-system.gitlab.io/Insular/) and [Island](https://github.com/oasisfeng/island) as it supports [contact search blocking](https://secure-system.gitlab.io/Insular/faq.html).
    
    When using Shelter, you are placing complete trust in its developer, as Shelter acts as a [Device Admin](https://developer.android.com/guide/topics/admin/device-admin) to create the Work Profile, and it has extensive access to the data stored within the Work Profile.

### Auditor

!!! recommendation

    ![Auditor logo](assets/img/android/auditor.svg#only-light){ align=right }
    ![Auditor logo](assets/img/android/auditor-dark.svg#only-dark){ align=right }
    
    **Auditor** is an app which leverages hardware security features to provide device integrity monitoring for [supported devices](https://attestation.app/about#device-support). Currently, it only works with GrapheneOS and the device's stock operating system.
    
    [:octicons-home-16: Homepage](https://attestation.app){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://attestation.app/privacy-policy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://attestation.app/about){ .card-link title=Documentation}
    [:octicons-code-16:](https://attestation.app/source){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://attestation.app/donate){ .card-link title=Contribute }
    
    ??? downloads
    
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

    ![Secure camera logo](assets/img/android/secure_camera.svg#only-light){ align=right }
    ![Secure camera logo](assets/img/android/secure_camera-dark.svg#only-dark){ align=right }
    
    **Secure Camera** is a camera app focused on privacy and security which can capture images, videos and QR codes. CameraX vendor extensions (Portrait, HDR, Night Sight, Face Retouch, and Auto) are also supported on available devices.
    
    [:octicons-repo-16: Repository](https://github.com/GrapheneOS/Camera){ .md-button .md-button--primary }
    [:octicons-info-16:](https://grapheneos.org/usage#camera){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/GrapheneOS/Camera){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.camera.play)
        - [:simple-github: GitHub](https://github.com/GrapheneOS/Camera/releases)
        - [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

Main privacy features include:

- Auto removal of [Exif](https://en.wikipedia.org/wiki/Exif) metadata (enabled by default)
- Use of the new [Media](https://developer.android.com/training/data-storage/shared/media) API, therefore [storage permissions](https://developer.android.com/training/data-storage) are not required
- Microphone permission not required unless you want to record sound

!!! note

    Metadata is not currently deleted from video files but that is planned.
    
    The image orientation metadata is not deleted. If you enable location (in Secure Camera) that **won't** be deleted either. If you want to delete that later you will need to use an external app such as [ExifEraser](data-redaction.md#exiferaser).

### Secure PDF Viewer

!!! recommendation

    ![Secure PDF Viewer logo](assets/img/android/secure_pdf_viewer.svg#only-light){ align=right }
    ![Secure PDF Viewer logo](assets/img/android/secure_pdf_viewer-dark.svg#only-dark){ align=right }
    
    **Secure PDF Viewer** is a PDF viewer based on [pdf.js](https://en.wikipedia.org/wiki/PDF.js) that doesn't require any permissions. The PDF is fed into a [sandboxed](https://en.wikipedia.org/wiki/Sandbox_(software_development)) [webview](https://developer.android.com/guide/webapps/webview). This means that it doesn't require permission directly to access content or files.
    
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

On GitHub, using [Secure Camera](#secure-camera) as an example, you would navigate to its [releases page](https://github.com/GrapheneOS/Camera/releases) and append `.atom` to the URL:

`https://github.com/GrapheneOS/Camera/releases.atom`

#### GitLab

On GitLab, using [Aurora Store](#aurora-store) as an example, you would navigate to its [project repository](https://gitlab.com/AuroraOSS/AuroraStore) and append `/-/tags?format=atom` to the URL:

`https://gitlab.com/AuroraOSS/AuroraStore/-/tags?format=atom`

#### Verifying APK Fingerprints

If you download APK files to install manually, you can verify their signature with the [`apksigner`](https://developer.android.com/studio/command-line/apksigner) tool, which is a part of Android [build-tools](https://developer.android.com/studio/releases/build-tools).

1. Install [Java JDK](https://www.oracle.com/java/technologies/downloads/).

2. Download the [Android Studio command line tools](https://developer.android.com/studio#command-tools).

3. Extract the downloaded archive:

    ```bash
    unzip commandlinetools-*.zip
    cd cmdline-tools
    ./bin/sdkmanager --sdk_root=./ "build-tools;29.0.3"
    ```

4. Run the signature verification command:

    ```bash
    ./build-tools/29.0.3/apksigner verify --print-certs ../Camera-37.apk
    ```

5. The resulting hashes can then be compared with another source. Some developers such as Signal [show the fingerprints](https://signal.org/android/apk/) on their website.

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

!!! note

    In some rare cases, the developer of an app will only distribute it through F-Droid ([Gadgetbridge](https://gadgetbridge.org/) is one example of this). If you really need an app like that, we recommend using [Neo Store](https://github.com/NeoApplications/Neo-Store/) instead of the official F-Droid app to obtain it.

## Criteria

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

!!! example "This section is new"

    We are working on establishing defined criteria for every section of our site, and this may be subject to change. If you have any questions about our criteria, please [ask on our forum](https://discuss.privacyguides.net/latest) and don't assume we didn't consider something when making our recommendations if it is not listed here. There are many factors considered and discussed when we recommend a project, and documenting every single one is a work-in-progress.

### Operating Systems

- Must be open-source software.
- Must support bootloader locking with custom AVB key support.
- Must receive major Android updates within 0-1 months of release.
- Must receive Android feature updates (minor version) within 0-14 days of release.
- Must receive regular security patches within 0-5 days of release.
- Must **not** be "rooted" out of the box.
- Must **not** enable Google Play Services by default.
- Must **not** require system modification to support Google Play Services.

### Devices

- Must support at least one of our recommended custom operating systems.
- Must be currently sold new in stores.
- Must receive a minimum of 5 years of security updates.
- Must have dedicated secure element hardware.

### Applications

- Applications on this page must not be applicable to any other software category on the site.
- General applications should extend or replace core system functionality.
- Applications should receive regular updates and maintenance.
