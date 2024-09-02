---
title: Android
icon: simple/android
cover: android.webp
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: Android-Empfehlungen
    url: ./
  - "@context": http://schema.org
    "@type": CreativeWork
    name: Android
    image: /assets/img/android/android.svg
    url: https://source.android.com/
    sameAs: https://de.wikipedia.org/wiki/Android_(Betriebssystem)
---

![Android Logo](../assets/img/android/android.svg){ align=right }

Das **Android Open Source Project** (AOSP) ist ein quelloffenes mobiles Betriebssystem unter der Leitung von Google, mit dem die meisten mobilen Geräte weltweit betrieben werden. Die meisten Handys, die mit Android verkauft werden, sind so modifiziert, dass sie invasive Integrationen und Apps wie Google Play Services enthalten. Du kannst also deine Privatsphäre auf deinem Gerät erheblich verbessern, indem du die Standardinstallation deines Smartphones durch eine Android-Version ohne diese invasiven Funktionen ersetzt.

[Allgemeine Android Übersicht :material-arrow-right-drop-circle:](../os/android-overview.md){ .md-button .md-button--primary }

## Unsere Empfehlung

### Google-Dienste ersetzen

Es gibt viele Methoden, um Apps für Android zu erhalten und dabei Google Play zu umgehen. Wann immer möglich, solltest du eine dieser Methoden ausprobieren, bevor du deine Apps aus nicht-privaten Quellen beziehst:

[Apps herunterladen :material-arrow-right-drop-circle:](obtaining-apps.md){ .md-button }

Es gibt auch viele private Alternativen zu den Apps, die auf deinem Handy vorinstalliert sind, wie die Kamera-App. Neben den Android-Apps, die wir auf dieser Website im Allgemeinen empfehlen, haben wir eine Liste von Android-spezifischen Systemprogrammen erstellt, die für dich nützlich sein könnten.

[Allgemeine App-Empfehlungen :material-arrow-right-drop-circle:](general-apps.md){ .md-button }

### Installiere eine Custom-ROM

Wenn du ein Android-Handy kaufst, wird das Standard-Betriebssystem mit Apps und Funktionen ausgeliefert, die nicht Teil des Android Open Source Project sind. Viele dieser Apps - sogar Apps wie der Dialer, der grundlegende Systemfunktionen bereitstellt - erfordern invasive Integrationen mit Google Play Services, die wiederum Zugriffsrechte auf deine Dateien, Kontakte, Anrufliste, SMS-Nachrichten, Standort, Kamera, Mikrofon und zahlreiche andere Funktionen auf deinem Gerät verlangen, damit diese grundlegenden System-Apps und viele andere Apps überhaupt funktionieren. Frameworks wie Google Play Services erhöhen die Angriffsfläche deines Geräts und sind die Ursache für diverse Datenschutzprobleme bei Android.

Dieses Problem könnte durch die Verwendung einer alternativen Android-Distribution gelöst werden, allgemein bekannt als _Custom-ROM_, die keine derartigen invasiven Integrationen beinhaltet. Leider verletzen viele Custom-Android-Distributionen oft das Android-Sicherheitsmodell, indem sie kritische Sicherheitsfunktionen wie AVB, Rollback-Schutz, Firmware-Updates usw. nicht unterstützen. Einige Distributionen liefern auch [`userdebug`](https://source.android.com/setup/build/building#choose-a-target) Builds aus, die Root über [ADB](https://developer.android.com/studio/command-line/adb) freilegen und [freizügigere](https://github.com/LineageOS/android_system_sepolicy/search?q=userdebug\&type=code) SELinux-Policies benötigen, um Debugging-Funktionen unterzubringen, was zu einer weiteren erhöhten Angriffsfläche und einem geschwächten Sicherheitsmodell führt.

Idealerweise solltest du bei der Auswahl einer Custom-Android-Distribution sicherstellen, dass sie das Android-Sicherheitsmodell einhält. Zumindest sollte die Distribution Produktions-Builds, Unterstützung für AVB, Rollback-Schutz, schnelle Firmware- und Betriebssystem-Updates und SELinux im [Enforcing-Mode] (https://source.android.com/security/selinux/concepts#enforcement_levels) bieten. Alle unsere empfohlenen Android-Distributionen erfüllen diese Kriterien:

[Empfohlene Betriebssysteme :material-arrow-right-drop-circle:](distributions.md){ .md-button }

### Vermeide Rooten

Das [Rooten](https://de.wikipedia.org/wiki/Rooten) von Android-Smartphones kann die Sicherheit des Geräts erheblich beeinträchtigen, da es das gesamte [Android-Sicherheitsmodell](https://en.wikipedia.org/wiki/Android_\(operating_system\)#Security_and_privacy) schwächt. Dies kann zu einer Beeinträchtigung des Datenschutzes führen, wenn die verminderte Sicherheit ausgenutzt wird. Bei den üblichen Rooting-Methoden wird direkt in die Boot-Partition eingegriffen, sodass ein erfolgreicher Verified Boot nicht möglich ist. Anwendungen, die Root benötigen, verändern auch die Systempartition, was bedeutet, dass Verified Boot deaktiviert bleiben muss. Die Aussetzung von Root direkt in der Benutzeroberfläche vergrößert auch die Angriffsfläche Ihres Geräts und kann zu [Rechteausweitungs](https://de.wikipedia.org/wiki/Rechteausweitung)-Schwachstellen und zur Umgehung von SELinux-Richtlinien beitragen.

Inhaltsblocker, die die [hosts Datei](https://de.wikipedia.org/wiki/Hosts_\(Datei\)) verändern (AdAway), und Firewalls (AFWall+), welche dauerhaft Root-Zugriff erfordern, sind gefährlich und sollten nicht verwendet werden. Sie sind auch nicht der richtige Weg, um den beabsichtigten Zweck zu erfüllen. Für das Blockieren von Inhalten empfehlen wir stattdessen verschlüsselte [DNS](../dns.md) oder eine von einem VPN bereitgestellte Funktion zum Blockieren von Inhalten. TrackerControl und AdAway im Nicht-Root-Modus werden den VPN-Slot belegen (indem sie ein lokales Loopback-VPN verwenden), was Sie daran hindert, datenschutzfreundliche Dienste wie [Orbot](../tor.md#orbot) oder einen [echten VPN-Anbieter](../vpn.md) zu nutzen.

AFWall+ basiert auf dem Ansatz der [Paketfilterung](https://de.wikipedia.org/wiki/Paketfilter) und kann in einigen Situationen umgangen werden.

Wir sind nicht der Meinung, dass die Sicherheitseinbußen, die durch das Rooten eines Smartphones entstehen, die fragwürdigen Datenschutzvorteile dieser Anwendungen wert sind.

### Updates regelmäßig installieren

Es ist wichtig, keine [End-of-Life](https://endoflife.date/android) Version von Android zu verwenden. Neuere Android-Versionen erhalten nicht nur Sicherheitsupdates für das Betriebssystem, sondern auch wichtige Updates zur Verbesserung der Privatsphäre.

Zum Beispiel konnten [vor Android 10](https://developer.android.com/about/versions/10/privacy/changes) alle Apps mit der Berechtigung [`READ_PHONE_STATE`](https://developer.android.com/reference/android/Manifest.permission#READ_PHONE_STATE) auf sensible und eindeutige Seriennummern deines Telefons zugreifen, wie [IMEI](https://en.wikipedia.org/wiki/International_Mobile_Equipment_Identity), [MEID](https://en.wikipedia.org/wiki/Mobile_equipment_identifier) oder die [IMSI](https://en.wikipedia.org/wiki/International_mobile_subscriber_identity) deiner SIM-Karte; während sie dies jetzt nur noch tun können, wenn sie System-Apps sind. Systemanwendungen werden nur vom OEM oder der Android-Distribution bereitgestellt.

### Integrierte Funktionen zum Teilen verwenden

Du kannst vermeiden, vielen Apps die Berechtigung zum Zugriff auf deine Medien zu gewähren, indem du die integrierten Freigabefunktionen von Android nutzt. Viele Apps ermöglichen es dir, eine Datei mit ihnen zu „teilen“ für den Medien-Upload.

Wenn du beispielsweise ein Bild in Discord posten möchtest, kannst du deinen Dateimanager oder deine Galerie öffnen und dieses Bild mit der Discord-App teilen, anstatt Discord vollen Zugriff auf deine Medien und Fotos zu gewähren.
