---
meta_title: The Best Android Operating Systems - Privacy Guides
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
robots: nofollow, max-snippet:-1, max-image-preview:large
---

<small>Schützt vor der/den folgenden Bedrohung(en):</small>

- [:material-target-account: Targeted Attacks](../basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: Passive Angriffe](../basics/common-threats.md#security-and-privacy){ .pg-orange }

A **custom Android-based operating system** (sometimes referred to as a **custom ROM**) can be a way to achieve a higher level of privacy and security on your device. This is in contrast to the "stock" version of Android which comes with your phone from the factory, and is often deeply integrated with Google Play Services as well as other vendor software.

We recommend installing GrapheneOS if you have a Google Pixel as it provides improved security hardening and additional privacy features. The reasons we don't list other operating systems or devices are as follows:

- They often have [weaker security](index.md#install-a-custom-distribution).
- Support is frequently dropped when the maintainer loses interest or upgrades their device, which is in contrast to the predictable [support cycle](https://grapheneos.org/faq#device-lifetime) that GrapheneOS follows.
- They generally have few or no notable privacy or security improvements that make installing them worthwhile.

## GrapheneOS

<div class="admonition recommendation" markdown>

![GrapheneOS-Logo](../assets/img/android/grapheneos.svg#only-light){ align=right }
![GrapheneOS-Logo](../assets/img/android/grapheneos-dark.svg#only-dark){ align=right }

**GrapheneOS** ist die beste Wahl, wenn es um Datenschutz und Sicherheit geht.

GrapheneOS bietet zusätzliche [Sicherheitshärtungen](https://de.wikipedia.org/wiki/Härten_\(Computer\)) und Verbesserungen beim Datenschutz. Es verfügt über eine [gehärtete Speicher-Allocator](https://github.com/GrapheneOS/hardened_malloc), Netzwerk- und Sensorberechtigungen und verschiedene andere [Sicherheitsfunktionen](https://grapheneos.org/features). GrapheneOS wird auch mit vollständigen Firmware-Updates und signierten Builds geliefert, so dass verifiziertes Booten vollständig unterstützt wird.

[:octicons-home-16: Homepage](https://grapheneos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://grapheneos.org/faq#privacy-policy){ .card-link title="Datenschutzrichtlinie" }
[:octicons-info-16:](https://grapheneos.org/faq){ .card-link title=Dokumentation}
[:octicons-code-16:](https://grapheneos.org/source){ .card-link title="Quellcode" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Spenden }

</div>

GrapheneOS unterstützt [sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), das die Google Play Services vollständig sandboxed, wie jede andere reguläre App. Das bedeutet, dass du die meisten Google Play-Dienste, wie z. B. Push-Benachrichtigungen, nutzen kannst, während du die volle Kontrolle über deren Berechtigungen und Zugriff hast und sie auf ein bestimmtes [Arbeitsprofil](../os/android-overview.md#work-profile) oder [Benutzerprofil](../os/android-overview.md#user-profiles) deiner Wahl beschränken kannst.

[Google Pixel-Handys](../mobile-phones.md#google-pixel) sind die einzigen Geräte, die derzeit die [Hardware-Sicherheitsanforderungen](https://grapheneos.org/faq#future-devices) von GrapheneOS erfüllen.

Standardmäßig stellt Android viele Netzwerkverbindungen zu Google her, um DNS-Verbindungsprüfungen durchzuführen, sich mit der aktuellen Netzwerkzeit zu synchronisieren, deine Netzwerkverbindung zu prüfen und viele andere Aufgaben im Hintergrund zu erledigen. GrapheneOS ersetzt diese durch Verbindungen zu Servern, die von GrapheneOS betrieben werden und deren Datenschutzbestimmungen unterliegen. Dies verbirgt Informationen wie deine IP-Adresse [vor Google](../basics/common-threats.md#privacy-from-service-providers), aber es bedeutet, dass es für einen Administrator in deinem Netzwerk oder ISP trivial ist, zu sehen, dass du Verbindungen zu `grapheneos.network`, `grapheneos.org` usw. herstellen, und daraus zu schließen, welches Betriebssystem du verwendest.

Wenn du Informationen wie diese vor einem Angreifer in deinem Netzwerk oder vor deinem ISP verbergen möchtest, **musst** du ein [vertrauenswürdiges VPN](../vpn.md) verwenden und zusätzlich die Einstellung für die Verbindungsprüfung auf **Standard (Google)** ändern. It can be found in :gear: **Settings** → **Network & internet** → **Internet connectivity checks**. This option allows you to connect to Google's servers for connectivity checks, which, alongside the usage of a VPN, helps you blend in with a larger pool of Android devices.

## Kriterien

**Bitte beachte, dass wir mit keinem der Projekte, die wir empfehlen, in Verbindung stehen.** Zusätzlich zu [unseren Standardkriterien](../about/criteria.md) haben wir eine Reihe klarer Anforderungen entwickelt, die es uns ermöglichen, objektive Empfehlungen zu geben. Wir empfehlen dir, dich mit der Liste vertraut zu machen, bevor du dich für ein Projekt entscheidest, und deine eigenen Recherchen anzustellen, um sicherzustellen, dass es die richtige Wahl für dich ist.

- Es muss sich um Open-Source Software handeln.
- Must support bootloader locking with custom AVB key support.
- Muss wichtige Android-Updates innerhalb von 0-1 Monaten nach der Veröffentlichung erhalten.
- Muss innerhalb von 0-14 Tagen nach der Veröffentlichung Updates für Android-Funktionen (kleinere Versionen) erhalten.
- Muss innerhalb von 0-5 Tagen nach der Veröffentlichung regelmäßig Sicherheits-Patches erhalten.
- Darf **nicht** von vornherein aus "gerootet" sein.
- Darf **nicht** Google Play-Dienste standardmäßig aktivieren.
- Darf **keine** Systemänderung zur Unterstützung von Google Play Services erfordern.
