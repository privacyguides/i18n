---
title: Android
icon: simple/android
cover: android.webp
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: Android Recommendations
    url: ./
  - "@context": http://schema.org
    "@type": CreativeWork
    name: Android
    image: /assets/img/android/android.svg
    url: https://source.android.com/
    sameAs: https://en.wikipedia.org/wiki/Android_(operating_system)
---

![Android logo](../assets/img/android/android.svg){ align=right }

The **Android Open Source Project** (AOSP) is an open-source mobile operating system led by Google which powers the majority of the world's mobile devices. Most phones sold with Android are modified to include invasive integrations and apps such as Google Play Services, so you can significantly improve your privacy on your mobile device by replacing your phone's default installation with a version of Android without these invasive features.

[General Android Overview :material-arrow-right-drop-circle:](../os/android-overview.md){ .md-button .md-button--primary }

## Unsere Empfehlung

### Replace Google Services

There are many methods of obtaining apps on Android while avoiding Google Play. Whenever possible, try using one of these methods before getting your apps from non-private sources:

[Obtaining Applications :material-arrow-right-drop-circle:](obtaining-apps.md){ .md-button }

There are also many private alternatives to the apps that come pre-installed on your phone, such as the camera app. Besides the Android apps we recommend throughout this site in general, we've created a list of system utilities specific to Android which you might find useful.

[General App Recommendations :material-arrow-right-drop-circle:](general-apps.md){ .md-button }

### Install a Custom Distribution

Wenn du ein Android-Handy kaufst, wird das Standard-Betriebssystem mit Apps und Funktionen ausgeliefert, die nicht Teil des Android Open Source Project sind. Viele dieser Apps - sogar Apps wie der Dialer, der grundlegende Systemfunktionen bereitstellt - erfordern invasive Integrationen mit Google Play Services, die wiederum Zugriffsrechte auf deine Dateien, Kontakte, Anrufliste, SMS-Nachrichten, Standort, Kamera, Mikrofon und zahlreiche andere Funktionen auf deinem Gerät verlangen, damit diese grundlegenden System-Apps und viele andere Apps überhaupt funktionieren. Frameworks wie Google Play Services erhöhen die Angriffsfläche deines Geräts und sind die Ursache für diverse Datenschutzprobleme bei Android.

This problem could be solved by using an alternative Android distribution, commonly known as a _custom ROM_, that does not come with such invasive integration. Leider verletzen viele Custom-Android-Distributionen oft das Android-Sicherheitsmodell, indem sie kritische Sicherheitsfunktionen wie AVB, Rollback-Schutz, Firmware-Updates usw. nicht unterstützen. Some distributions also ship [`userdebug`](https://source.android.com/setup/build/building#choose-a-target) builds which expose root via [ADB](https://developer.android.com/studio/command-line/adb) and require [more permissive](https://github.com/LineageOS/android_system_sepolicy/search?q=userdebug\&type=code) SELinux policies to accommodate debugging features, resulting in a further increased attack surface and weakened security model.

Idealerweise solltest du bei der Auswahl einer Custom-Android-Distribution sicherstellen, dass sie das Android-Sicherheitsmodell einhält. At the very least, the distribution should have production builds, support for AVB, rollback protection, timely firmware and operating system updates, and SELinux in [enforcing mode](https://source.android.com/security/selinux/concepts#enforcement_levels). All of our recommended Android distributions satisfy these criteria:

[Recommended Distributions :material-arrow-right-drop-circle:](distributions.md){ .md-button }

### Avoid Root

[Rooting](https://en.wikipedia.org/wiki/Rooting_\(Android\)) Android phones can decrease security significantly as it weakens the complete [Android security model](https://en.wikipedia.org/wiki/Android_\(operating_system\)#Security_and_privacy). Dies kann zu einer Beeinträchtigung des Datenschutzes führen, wenn die verminderte Sicherheit ausgenutzt wird. Bei den üblichen Rooting-Methoden wird direkt in die Boot-Partition eingegriffen, sodass ein erfolgreicher Verified Boot nicht möglich ist. Anwendungen, die Root benötigen, verändern auch die Systempartition, was bedeutet, dass Verified Boot deaktiviert bleiben muss. Having root exposed directly in the user interface also increases the attack surface of your device and may assist in [privilege escalation](https://en.wikipedia.org/wiki/Privilege_escalation) vulnerabilities and SELinux policy bypasses.

Content blockers which modify the [hosts file](https://en.wikipedia.org/wiki/Hosts_\(file\)) (AdAway) and firewalls (AFWall+) which require root access persistently are dangerous and should not be used. Sie sind auch nicht der richtige Weg, um den beabsichtigten Zweck zu erfüllen. For content blocking, we suggest encrypted [DNS](../dns.md) or content blocking functionality provided by a VPN instead. TrackerControl and AdAway in non-root mode will take up the VPN slot (by using a local loopback VPN), preventing you from using privacy enhancing services such as [Orbot](../tor.md#orbot) or a [real VPN provider](../vpn.md).

AFWall+ works based on the [packet filtering](https://en.wikipedia.org/wiki/Firewall_\(computing\)#Packet_filter) approach and may be bypassable in some situations.

Wir sind nicht der Meinung, dass die Sicherheitseinbußen, die durch das Rooten eines Smartphones entstehen, die fragwürdigen Datenschutzvorteile dieser Anwendungen wert sind.

### Install Updates Regularly

It's important to not use an [end-of-life](https://endoflife.date/android) version of Android. Neuere Android-Versionen erhalten nicht nur Sicherheitsupdates für das Betriebssystem, sondern auch wichtige Updates zur Verbesserung der Privatsphäre.

For example, [prior to Android 10](https://developer.android.com/about/versions/10/privacy/changes) any apps with the [`READ_PHONE_STATE`](https://developer.android.com/reference/android/Manifest.permission#READ_PHONE_STATE) permission could access sensitive and unique serial numbers of your phone such as [IMEI](https://en.wikipedia.org/wiki/International_Mobile_Equipment_Identity), [MEID](https://en.wikipedia.org/wiki/Mobile_equipment_identifier), or your SIM card's [IMSI](https://en.wikipedia.org/wiki/International_mobile_subscriber_identity); whereas now they must be system apps to do so. Systemanwendungen werden nur vom OEM oder der Android-Distribution bereitgestellt.

### Use Built-in Sharing Features

Du kannst vermeiden, vielen Apps die Berechtigung zum Zugriff auf deine Medien zu gewähren, indem du die integrierten Freigabefunktionen von Android nutzt. Viele Apps ermöglichen es dir, eine Datei mit ihnen zu „teilen“ für den Medien-Upload.

Wenn du beispielsweise ein Bild in Discord posten möchtest, kannst du deinen Dateimanager oder deine Galerie öffnen und dieses Bild mit der Discord-App teilen, anstatt Discord vollen Zugriff auf deine Medien und Fotos zu gewähren.
