---
meta_title: The Best Custom Android OSes (aka Custom ROMs) - Privacy Guides
title: Alternative Distributionen
description: Du kannst das Betriebssystem deines Android-Handys mit diesen sicheren und Privatsphäre-freundlichen Alternativen ersetzen.
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: Private Android-Betriebssysteme
    url: ./
  - "@context": http://schema.org
    "@type": CreativeWork
    name: GrapheneOS
    image: /assets/img/android/grapheneos.svg
    url: https://grapheneos.org/
    sameAs: https://de.wikipedia.org/wiki/GrapheneOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: ./
  - "@context": http://schema.org
    "@type": CreativeWork
    name: Divest
    image: /assets/img/android/divestos.svg
    url: https://divestos.org/
    sameAs: https://de.wikipedia.org/wiki/DivestOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: ./
robots: nofollow, max-snippet:-1, max-image-preview:large
---

<small>Schützt vor der/den folgenden Bedrohung(en):</small>

- [:material-target-account: Targeted Attacks](../basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: Passive Angriffe](../basics/common-threats.md#security-and-privacy){ .pg-orange }

A **custom Android-based operating system** (often known as a **custom ROM**) is a popular way to achieve higher levels of privacy and security on your device. This is in contrast to the "stock" version of Android which comes with your phone from the factory, and is often deeply integrated with Google Play Services.

We recommend installing one of these custom Android operating systems on your device, listed in order of preference, depending on your device's compatibility with these operating systems.

## AOSP-Derivate

### GrapheneOS

<div class="admonition recommendation" markdown>

![GrapheneOS-Logo](../assets/img/android/grapheneos.svg#only-light){ align=right }
![GrapheneOS-Logo](../assets/img/android/grapheneos-dark.svg#only-dark){ align=right }

**GrapheneOS** ist die beste Wahl, wenn es um Datenschutz und Sicherheit geht.

GrapheneOS provides additional [security hardening](https://en.wikipedia.org/wiki/Hardening_\(computing\)) and privacy improvements. It has a [hardened memory allocator](https://github.com/GrapheneOS/hardened_malloc), network and sensor permissions, and various other [security features](https://grapheneos.org/features). GrapheneOS also comes with full firmware updates and signed builds, so verified boot is fully supported.

[:octicons-home-16: Homepage](https://grapheneos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://grapheneos.org/faq#privacy-policy){ .card-link title="Datenschutzrichtlinie" }
[:octicons-info-16:](https://grapheneos.org/faq){ .card-link title=Dokumentation}
[:octicons-code-16:](https://grapheneos.org/source){ .card-link title="Quellcode" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Spenden }

</div>

GrapheneOS supports [sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), which runs Google Play Services fully sandboxed like any other regular app. This means you can take advantage of most Google Play Services, such as push notifications, while giving you full control over their permissions and access, and while containing them to a specific [work profile](../os/android-overview.md#work-profile) or [user profile](../os/android-overview.md#user-profiles) of your choice.

[Google Pixel phones](../mobile-phones.md#google-pixel) are the only devices that currently meet GrapheneOS's [hardware security requirements](https://grapheneos.org/faq#future-devices).

By default, Android makes many network connections to Google to perform DNS connectivity checks, to sync with current network time, to check your network connectivity, and for many other background tasks. GrapheneOS replaces these with connections to servers operated by GrapheneOS and subject to their privacy policy. This hides information like your IP address [from Google](../basics/common-threats.md#privacy-from-service-providers), but means it is trivial for an admin on your network or ISP to see you are making connections to `grapheneos.network`, `grapheneos.org`, etc. and deduce what operating system you are using.

GrapheneOS provides the option to switch back to connecting to Google's servers for many of these background connections if you prefer, but it is far more robust/foolproof to use a [trusted VPN](../vpn.md) and enable Android's native VPN [kill switch](../os/android-overview.md#vpn-killswitch) to hide information like this from adversaries on your network.

### DivestOS

Wenn GrapheneOS nicht mit deinem Handy kompatibel ist, ist DivestOS eine gute Alternative. Es unterstützt eine Vielzahl von Telefonen mit _unterschiedlichen_ Sicherheitsstufen und Qualitätskontrollen.

<div class="admonition recommendation" markdown>

![DivestOS-Logo](../assets/img/android/divestos.svg){ align=right }

**DivestOS** ist ein Soft-Fork von [LineageOS](https://lineageos.org).
DivestOS erbt viele [unterstützte Geräte](https://divestos.org/index.php?page=devices\&base=LineageOS) von LineageOS. It has signed builds, making it possible to have [verified boot](../os/android-overview.md#verified-boot) on some non-Pixel devices. Not all supported devices support verified boot or other security features.

[:octicons-home-16: Homepage](https://divestos.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://divestoseb5nncsydt7zzf5hrfg44md4bxqjs5ifcv4t7gt7u6ohjyyd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://divestos.org/index.php?page=privacy_policy){ .card-link title="Datenschutzrichtlinie" }
[:octicons-info-16:](https://divestos.org/index.php?page=faq){ .card-link title="Dokumentation" }
[:octicons-code-16:](https://github.com/divested-mobile){ .card-link title="Quellcode" }
[:octicons-heart-16:](https://divested.dev/pages/donate){ .card-link title="Spenden" }

</div>

The [status](https://gitlab.com/divested-mobile/firmware-empty/-/blob/master/STATUS) of firmware updates in particular will vary significantly depending on your phone model. While standard AOSP bugs and vulnerabilities can be fixed with standard software updates like those provided by DivestOS, some vulnerabilities cannot be patched without support from the device manufacturer, making end-of-life devices less safe even with an up-to-date alternative ROM like DivestOS.

DivestOS has automated kernel vulnerability ([CVE](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures)) [patching](https://gitlab.com/divested-mobile/cve_checker), fewer proprietary blobs, and a custom [hosts](https://divested.dev/index.php?page=dnsbl) file. Its hardened WebView, [Mulch](https://gitlab.com/divested-mobile/mulch), enables [control-flow integrity](https://en.wikipedia.org/wiki/Control-flow_integrity) for all architectures and [network state partitioning](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning), and receives out-of-band updates.

DivestOS also includes kernel patches from GrapheneOS and enables all available kernel security features via [defconfig hardening](https://github.com/Divested-Mobile/DivestOS-Build/blob/master/Scripts/Common/Functions.sh#L758). All kernels newer than version 3.4 include full page [sanitization](https://lwn.net/Articles/334747) and all ~22 Clang-compiled kernels have [`-ftrivial-auto-var-init=zero`](https://reviews.llvm.org/D54604?id=174471) enabled.

DivestOS implements some system hardening patches originally developed for GrapheneOS. DivestOS 16.0 and higher implements GrapheneOS's `INTERNET` and `SENSORS` permission toggle, [hardened memory allocator](https://github.com/GrapheneOS/hardened_malloc), [exec-spawning](https://grapheneos.org/usage#exec-spawning), Java Native Interface [constification](https://en.wikipedia.org/wiki/Const_\(computer_programming\)), and partial [bionic](https://en.wikipedia.org/wiki/Bionic_\(software\)) hardening patchsets. 17.1 and higher features per-network full MAC address randomization, [`ptrace_scope`](https://kernel.org/doc/html/latest/admin-guide/LSM/Yama.html) control, automatic reboot, and Wi-Fi/Bluetooth [timeout options](https://grapheneos.org/features#attack-surface-reduction).

DivestOS uses F-Droid as its default app store. We normally [recommend avoiding F-Droid](obtaining-apps.md#f-droid), but doing so on DivestOS isn't viable; the developers update their apps via their own F-Droid repository, [DivestOS Official](https://divestos.org/fdroid/official). For these apps you should continue to use F-Droid **with the DivestOS repository enabled** to keep those components up to date. For other apps, our recommended [methods of obtaining them](obtaining-apps.md) still apply.

DivestOS replaces many of Android's background network connections to Google services with alternative services, such as using OpenEUICC for eSIM activation, NTP.org for network time, and Quad9 for DNS. These connections can be modified, but their deviation from a standard Android phone's network connections could mean it is easier for an adversary on your network to deduce what operating system you have installed on your phone. If this is a concern to you, consider using a [trusted VPN](../vpn.md) and enabling the native VPN [kill switch](../os/android-overview.md#vpn-killswitch) to hide this network traffic from your local network and ISP.

## Kriterien

**Bitte beachte, dass wir mit keinem der Projekte, die wir empfehlen, in Verbindung stehen.** Zusätzlich zu [unseren Standardkriterien](../about/criteria.md) haben wir eine Reihe klarer Anforderungen entwickelt, die es uns ermöglichen, objektive Empfehlungen zu geben. Wir empfehlen dir, dich mit der Liste vertraut zu machen, bevor du dich für ein Projekt entscheidest, und deine eigenen Recherchen anzustellen, um sicherzustellen, dass es die richtige Wahl für dich ist.

- Es muss sich um Open-Source Software handeln.
- Must support bootloader locking with custom AVB key support.
- Must receive major Android updates within 0-1 months of release.
- Must receive Android feature updates (minor version) within 0-14 days of release.
- Must receive regular security patches within 0-5 days of release.
- Must **not** be "rooted" out of the box.
- Must **not** enable Google Play Services by default.
- Must **not** require system modification to support Google Play Services.
