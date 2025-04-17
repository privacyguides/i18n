---
title: Android
description: Our advice for replacing privacy-invasive default Android features with private and secure alternatives.
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

## Nos conseils

### Replace Google Services

There are many methods of obtaining apps on Android while avoiding Google Play. Whenever possible, try using one of these methods before getting your apps from non-private sources:

[Obtaining Applications :material-arrow-right-drop-circle:](obtaining-apps.md){ .md-button }

There are also many private alternatives to the apps that come pre-installed on your phone, such as the camera app. Besides the Android apps we recommend throughout this site in general, we've created a list of system utilities specific to Android which you might find useful.

[General App Recommendations :material-arrow-right-drop-circle:](general-apps.md){ .md-button }

### Install a Custom Distribution

Lorsque vous achetez un téléphone Android, le système d'exploitation par défaut est livré avec des applications et des fonctionnalités qui ne font pas partie de l'Android Open-Source Project. Un grand nombre de ces applications - même des applications comme l'app Téléphone qui fournissent des fonctions système de base - nécessitent des intégrations invasives avec les services Google Play, qui demandent à leur tour des privilèges pour accéder à vos fichiers, au stockage de vos contacts, aux journaux d'appels, aux messages SMS, à la localisation, à l'appareil photo, au microphone et à de nombreux autres éléments de votre appareil afin que ces applications systèmes de base et beaucoup d'autres applications puissent simplement fonctionner. Les environnements tels que les services Google Play augmentent la surface d'attaque de votre appareil et sont à l'origine de divers problèmes de confidentialité liés à Android.

This problem could be solved by using an alternative Android distribution, commonly known as a _custom ROM_, that does not come with such invasive integration. Malheureusement, de nombreuses distributions d'Android enfreignent souvent le modèle de sécurité d'Android en ne prenant pas en charge les fonctions de sécurité essentielles telles que l'AVB, le rollback protection, les mises à jour du firmware, etc. Some distributions also ship [`userdebug`](https://source.android.com/setup/build/building#choose-a-target) builds which expose root via [ADB](https://developer.android.com/studio/command-line/adb) and require more permissive SELinux policies to accommodate debugging features, resulting in a further increased attack surface and weakened security model.

Idéalement, lorsque vous choisissez une distribution Android, vous devez vous assurer qu'elle respecte le modèle de sécurité Android. At the very least, the distribution should have production builds, support for AVB, rollback protection, timely firmware and operating system updates, and SELinux in [enforcing mode](https://source.android.com/security/selinux/concepts#enforcement_levels). All of our recommended Android distributions satisfy these criteria:

[Recommended Distributions :material-arrow-right-drop-circle:](distributions.md){ .md-button }

### Avoid Root

[Rooting](https://en.wikipedia.org/wiki/Rooting_\(Android\)) Android phones can decrease security significantly as it weakens the complete [Android security model](https://en.wikipedia.org/wiki/Android_\(operating_system\)#Security_and_privacy). Cela peut nuire à la protection de la vie privée en cas d'exploitation facilitée par la diminution de la sécurité. Les méthodes courantes de rootage impliquent une modification directe de la partition de démarrage, ce qui rend impossible l'exécution du Démarrage Vérifié. Apps that require root will also modify the system partition, meaning that Verified Boot would have to remain disabled. Having root exposed directly in the user interface also increases the attack surface of your device and may assist in [privilege escalation](https://en.wikipedia.org/wiki/Privilege_escalation) vulnerabilities and SELinux policy bypasses.

Content blockers which modify the [hosts file](https://en.wikipedia.org/wiki/Hosts_\(file\)) (like AdAway) and firewalls which require root access persistently (like AFWall+) are dangerous and should not be used. Ils ne sont pas non plus la bonne façon de résoudre les problèmes auxquels ils sont destinés. For content blocking, we suggest encrypted [DNS](../dns.md) or content blocking functionality provided by a VPN instead. TrackerControl and AdAway in non-root mode will take up the VPN slot (by using a local loopback VPN), preventing you from using privacy-enhancing services such as [Orbot](../alternative-networks.md#orbot) or a [real VPN provider](../vpn.md).

AFWall+ works based on the [packet filtering](https://en.wikipedia.org/wiki/Firewall_\(computing\)#Packet_filter) approach and may be bypassable in some situations.

Nous ne pensons pas que les sacrifices de sécurité en rootant un smartphone valent les avantages discutables de ces applications en matière de vie privée.

### Install Updates Regularly

It's important to not use an [end-of-life](https://endoflife.date/android) version of Android. Newer versions of Android receive not only security updates for the operating system but also important privacy enhancing updates too.

For example, [prior to Android 10](https://developer.android.com/about/versions/10/privacy/changes) any apps with the [`READ_PHONE_STATE`](https://developer.android.com/reference/android/Manifest.permission#READ_PHONE_STATE) permission could access sensitive and unique serial numbers of your phone such as [IMEI](https://en.wikipedia.org/wiki/International_Mobile_Equipment_Identity), [MEID](https://en.wikipedia.org/wiki/Mobile_equipment_identifier), or your SIM card's [IMSI](https://en.wikipedia.org/wiki/International_mobile_subscriber_identity); whereas now they must be system apps to do so. Les applications système sont uniquement fournies par le fabricant ou la distribution Android.

### Use Built-in Sharing Features

Vous pouvez éviter de donner à de nombreuses applications l'autorisation d'accéder à vos médias grâce aux fonctions de partage intégrées d'Android. De nombreuses applications vous permettent de "partager" un fichier avec elles pour l'envoi de médias.

Par exemple, si vous souhaitez publier une photo sur Discord, vous pouvez ouvrir votre gestionnaire de fichiers ou votre galerie et partager cette photo avec l'application Discord, au lieu d'accorder à Discord un accès complet à vos médias et photos.
