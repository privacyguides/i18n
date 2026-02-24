---
meta_title: "Die besten Android-Betriebssysteme - Privacy Guides"
title: Alternative Distributionen
description: Du kannst das Betriebssystem deines Android-Handys mit diesen sicheren und Privatsphäre-freundlichen Alternativen ersetzen.
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: Private Android-Betriebssysteme
    url: "./"
  - "@context": http://schema.org
    "@type": CreativeWork
    name: GrapheneOS
    image: /assets/img/android/grapheneos.svg
    url: https://grapheneos.org/
    sameAs: https://de.wikipedia.org/wiki/GrapheneOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
robots: nofollow, max-snippet:-1, max-image-preview:large
---

<small>Schützt vor der/den folgenden Bedrohung(en):</small>

- [:material-target-account: Gezielte Angriffe](../basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: Passive Angriffe](../basics/common-threats.md#security-and-privacy){ .pg-orange }

Ein **Custom Android-Betriebssystem** (manchmal auch als **Custom ROM** bezeichnet) kann eine Möglichkeit sein, um ein höheres Maß an Privatsphäre und Sicherheit auf einem Gerät zu erreichen. Dies steht im Gegensatz zu der „Stock“-Version von Android, die mit deinem Handy aus der Fabrik kommt, und häufig tiefgreifend mit Google Play Services, sowie Diensten anderer Hersteller, integriert ist.

Wir empfehlen die Installation von GrapheneOS, wenn du ein Google Pixel besitzt, da es verbesserte Sicherheitshärtungen und zusätzliche Datenschutzfunktionen bietet. Die Gründe, warum wir keine anderen Betriebssysteme oder Geräte auflisten, sind folgende:

- Sie haben oft eine [schwächere Sicherheit](index.md#install-a-custom-distribution).
- Der Support wird häufig eingestellt, wenn der Maintainer das Interesse verliert oder sein Gerät aufrüstet, was im Gegensatz zu dem vorhersehbaren [Support-Zyklus](https://grapheneos.org/faq#device-lifetime) steht, dem GrapheneOS folgt.
- Sie bieten in der Regel nur wenige oder gar keine nennenswerten Verbesserungen des Datenschutzes oder der Sicherheit, die ihre Installation lohnend machen.

## GrapheneOS

<div class="admonition recommendation" markdown>

![GrapheneOS-Logo](../assets/img/android/grapheneos.svg#only-light){ align=right }
![GrapheneOS-Logo](../assets/img/android/grapheneos-dark.svg#only-dark){ align=right }

**GrapheneOS** ist die beste Wahl, wenn es um Datenschutz und Sicherheit geht.

GrapheneOS bietet zusätzliche [Sicherheitshärtungen](https://de.wikipedia.org/wiki/Härten_\(Computer\)) und Verbesserungen beim Datenschutz. Es verfügt über eine [gehärtete Speicher-Allocator](https://github.com/GrapheneOS/hardened_malloc), Netzwerk- und Sensorberechtigungen und verschiedene andere [Sicherheitsfunktionen](https://grapheneos.org/features). GrapheneOS wird auch mit vollständigen Firmware-Updates und signierten Builds geliefert, so dass verifiziertes Booten vollständig unterstützt wird.

[:octicons-home-16: Homepage](https://grapheneos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://grapheneos.org/faq#privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://grapheneos.org/faq){ .card-link title="Documentation" }
[:octicons-code-16:](https://grapheneos.org/source){ .card-link title="Source Code" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title="Contribute" }

</div>

GrapheneOS unterstützt [sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), das die Google Play Services vollständig sandboxed, wie jede andere reguläre App. Das bedeutet, dass du die meisten Google Play-Dienste, wie z. B. Push-Benachrichtigungen, nutzen kannst, während du die volle Kontrolle über deren Berechtigungen und Zugriff hast und sie auf ein bestimmtes [Arbeitsprofil](../os/android-overview.md#work-profile) oder [Benutzerprofil](../os/android-overview.md#user-profiles) deiner Wahl beschränken kannst.

[Google Pixel phones](../mobile-phones.md#google-pixel) are the only devices that currently meet GrapheneOS's [hardware security requirements](https://grapheneos.org/faq#future-devices). The Pixel 8 and later support ARM's Memory Tagging Extension (MTE), a hardware security enhancement that drastically lowers the probability of exploits occurring through memory corruption bugs. GrapheneOS greatly expands the coverage of MTE on supported devices. Whereas the stock OS only allows you to opt in to a limited implementation of MTE via a developer option or Google's Advanced Protection Program, GrapheneOS features a more robust implementation of MTE by default in the system kernel, default system components, and their Vanadium web browser and its WebView.

GrapheneOS also provides a global toggle for enabling MTE on all user-installed apps at :gear: **Settings** → **Security & privacy** → **Exploit protection** → **Memory tagging** → **Enable by default**. The OS also features per-app toggles to opt out of MTE for apps which may crash due to compatibility issues.

### Connectivity Checks

Standardmäßig stellt Android viele Netzwerkverbindungen zu Google her, um DNS-Verbindungsprüfungen durchzuführen, sich mit der aktuellen Netzwerkzeit zu synchronisieren, deine Netzwerkverbindung zu prüfen und viele andere Aufgaben im Hintergrund zu erledigen. GrapheneOS ersetzt diese durch Verbindungen zu Servern, die von GrapheneOS betrieben werden und deren Datenschutzbestimmungen unterliegen. Dies verbirgt Informationen wie deine IP-Adresse [vor Google](../basics/common-threats.md#privacy-from-service-providers), aber es bedeutet, dass es für einen Administrator in deinem Netzwerk oder ISP trivial ist, zu sehen, dass du Verbindungen zu `grapheneos.network`, `grapheneos.org` usw. herstellen, und daraus zu schließen, welches Betriebssystem du verwendest.

Wenn du Informationen wie diese vor einem Angreifer in deinem Netzwerk oder vor deinem ISP verbergen möchtest, **musst** du ein [vertrauenswürdiges VPN](../vpn.md) verwenden und zusätzlich die Einstellung für die Verbindungsprüfung auf **Standard (Google)** ändern. Du findest sie unter :gear: **Einstellungen** → **Netzwerk & Internet** → **Internet connectivity checks**. Mit dieser Option kannst du eine Verbindung zu den Google-Servern herstellen, um die Konnektivität zu prüfen. Zusammen mit der Verwendung eines VPNs kannst du dich so in einen größeren Pool von Android-Geräten einfügen.

## Kriterien

**Bitte beachte, dass wir mit keinem der Projekte, die wir empfehlen, in Verbindung stehen.** Zusätzlich zu [unseren Standardkriterien](../about/criteria.md) haben wir eine Reihe klarer Anforderungen entwickelt, die es uns ermöglichen, objektive Empfehlungen zu geben. Wir empfehlen dir, dich mit der Liste vertraut zu machen, bevor du dich für ein Projekt entscheidest, und deine eigenen Recherchen anzustellen, um sicherzustellen, dass es die richtige Wahl für dich ist.

- Es muss sich um Open-Source Software handeln.
- Muss die Bootloader-Sperre mit benutzerdefiniertem AVB-Key unterstützen.
- Muss wichtige Android-Updates innerhalb von 0-1 Monaten nach der Veröffentlichung erhalten.
- Muss innerhalb von 0-14 Tagen nach der Veröffentlichung Updates für Android-Funktionen (kleinere Versionen) erhalten.
- Muss innerhalb von 0-5 Tagen nach der Veröffentlichung regelmäßig Sicherheits-Patches erhalten.
- Darf **nicht** von vornherein aus "gerootet" sein.
- Darf **nicht** Google Play-Dienste standardmäßig aktivieren.
- Darf **keine** Systemänderung zur Unterstützung von Google Play Services erfordern.
