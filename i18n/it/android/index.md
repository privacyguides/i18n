---
title: "Android"
description: Our advice for replacing privacy-invasive default Android features with private and secure alternatives.
icon: 'simple/android'
cover: android.webp
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: Android Recommendations
    url: "./"
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

## I nostri consigli

### Replace Google Services

There are many methods of obtaining apps on Android while avoiding Google Play. Whenever possible, try using one of these methods before getting your apps from non-private sources:

[Obtaining Applications :material-arrow-right-drop-circle:](obtaining-apps.md){ .md-button }

There are also many private alternatives to the apps that come pre-installed on your phone, such as the camera app. Besides the Android apps we recommend throughout this site in general, we've created a list of system utilities specific to Android which you might find useful.

[General App Recommendations :material-arrow-right-drop-circle:](general-apps.md){ .md-button }

### Install a Custom Distribution

Quando acquisti un telefono Android, il sistema operativo predefinito viene fornito con applicazioni e funzionalità che non fanno parte dell'Android Open Source Project. Molte di queste app, anche quelle come il dialer che forniscono le funzionalità di base del sistema, richiedono integrazioni invasive con Google Play Services, che a sua volta richiede i privilegi di accesso ai file, all'archiviazione dei contatti, ai registri delle chiamate, ai messaggi SMS, alla posizione, alla fotocamera, al microfono e a numerosi altri elementi del dispositivo per far funzionare le app di base del sistema e molte altre applicazioni. Framework come Google Play Services aumentano la superficie di attacco del dispositivo e sono all'origine di vari problemi di privacy con Android.

This problem could be solved by using an alternative Android distribution, commonly known as a _custom ROM_, that does not come with such invasive integration. Purtroppo, molte distribuzioni di Android personalizzate spesso violano il modello di sicurezza di Android, non supportando funzioni di sicurezza critiche come AVB, protezione rollback, aggiornamenti del firmware e così via. Some distributions also ship [`userdebug`](https://source.android.com/setup/build/building#choose-a-target) builds which expose root via [ADB](https://developer.android.com/studio/command-line/adb) and require [more permissive](https://github.com/LineageOS/android_system_sepolicy/search?q=userdebug&type=code) SELinux policies to accommodate debugging features, resulting in a further increased attack surface and weakened security model.

Idealmente, quando si sceglie una distribuzione modificata di Android, bisogna assicurarsi che rispetti il modello di sicurezza Android. At the very least, the distribution should have production builds, support for AVB, rollback protection, timely firmware and operating system updates, and SELinux in [enforcing mode](https://source.android.com/security/selinux/concepts#enforcement_levels). All of our recommended Android distributions satisfy these criteria:

[Recommended Distributions :material-arrow-right-drop-circle:](distributions.md){ .md-button }

### Avoid Root

[Rooting](https://en.wikipedia.org/wiki/Rooting_\(Android\)) Android phones can decrease security significantly as it weakens the complete [Android security model](https://en.wikipedia.org/wiki/Android_\(operating_system\)#Security_and_privacy). Ciò può ridurre la privacy in caso di exploit assistito dalla sicurezza ridotta. I metodi di rooting comuni richiedono la manomissione diretta della partizione d'avvio, rendendo impossibile l'esecuzione corretta dell'Avvio Verificato. Apps that require root will also modify the system partition, meaning that Verified Boot would have to remain disabled. Having root exposed directly in the user interface also increases the attack surface of your device and may assist in [privilege escalation](https://en.wikipedia.org/wiki/Privilege_escalation) vulnerabilities and SELinux policy bypasses.

Content blockers which modify the [hosts file](https://en.wikipedia.org/wiki/Hosts_\(file\)) (like AdAway) and firewalls which require root access persistently (like AFWall+) are dangerous and should not be used. Inoltre, sono il modo errato per risolvere i loro scopi. For content blocking, we suggest encrypted [DNS](../dns.md) or content blocking functionality provided by a VPN instead. TrackerControl and AdAway in non-root mode will take up the VPN slot (by using a local loopback VPN), preventing you from using privacy-enhancing services such as [Orbot](../alternative-networks.md#orbot) or a [real VPN provider](../vpn.md).

AFWall+ works based on the [packet filtering](https://en.wikipedia.org/wiki/Firewall_\(computing\)#Packet_filter) approach and may be bypassable in some situations.

Non crediamo che i sacrifici di sicurezza effettuati dal rooting di un telefono, valgano i discutibili benefici della privacy di tali app.

### Install Updates Regularly

It's important to not use an [end-of-life](https://endoflife.date/android) version of Android. Newer versions of Android receive not only security updates for the operating system but also important privacy enhancing updates too.

For example, [prior to Android 10](https://developer.android.com/about/versions/10/privacy/changes) any apps with the [`READ_PHONE_STATE`](https://developer.android.com/reference/android/Manifest.permission#READ_PHONE_STATE) permission could access sensitive and unique serial numbers of your phone such as [IMEI](https://en.wikipedia.org/wiki/International_Mobile_Equipment_Identity), [MEID](https://en.wikipedia.org/wiki/Mobile_equipment_identifier), or your SIM card's [IMSI](https://en.wikipedia.org/wiki/International_mobile_subscriber_identity); whereas now they must be system apps to do so. Le app di sistema sono fornite soltanto dall'OEM o dalla distribuzione di Android.

### Use Built-in Sharing Features

Puoi evitare di consentire a molte app l'autorizzazione d'accesso ai tuoi file multimediali, con le funzionalità di condivisione integrate di Android. Molte applicazioni ti consentono di "condividere" un file con esse, tramite caricamento dello stesso.

Ad esempio, se desideri pubblicare un'immagine su Discord, puoi aprire il tuo gestore di file o galleria e condividerla con l'app di Discord, invece di concedere a Discord l'accesso completo ai tuoi file multimediali e foto.
