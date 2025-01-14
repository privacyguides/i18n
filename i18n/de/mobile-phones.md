---
title: Mobiltelefone
icon: material/cellphone-check
description: These mobile devices provide the best hardware security support for custom Android operating systems.
cover: android.webp
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: Empfehlungen für Mobiltelefone
    url: ./
  - "@context": http://schema.org
    "@type": Product
    name: Pixel
    brand:
      "@type": Brand
      name: Google
    image: /assets/img/android/google-pixel.png
    sameAs: https://de.wikipedia.org/wiki/Google_Pixel
    review:
      "@type": Review
      author:
        "@type": Organization
        name: Privacy Guides
robots: nofollow, max-snippet:-1, max-image-preview:large
---

<small>Schützt vor der/den folgenden Bedrohung(en):</small>

- [:material-target-account: Targeted Attacks](basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: Passive Angriffe](basics/common-threats.md#security-and-privacy){ .pg-orange }

Die meisten **Mobiltelefone** erhalten nur kurze oder begrenzte Zeitfenster für Sicherheitsupdates von den OEMs; nachdem diese Geräte das Ende ihres Supportzeitraums erreicht haben, können sie **nicht** als sicher angesehen werden, da sie keine Sicherheitsupdates für Firmware oder Treiber mehr erhalten.

Die hier aufgelisteten Mobilgeräte bieten eine lange Lebensdauer garantierter Sicherheitsupdates und ermöglichen Ihnen die Installation eines benutzerdefinierten Betriebssystems, ohne das Android-Sicherheitsmodell zu verletzen.

[Recommended Android Distributions :material-arrow-right-drop-circle:](android/distributions.md){ .md-button .md-button--primary } [Details about Android Security :material-arrow-right-drop-circle:](os/android-overview.md#security-protections){ .md-button }

<div class="admonition warning" markdown>
<p class="admonition-title">Warnung</p>

End-of-Life-Geräte (z. B. "erweitertem Support"-Geräte von GrapheneOS) verfügen nicht über vollständige Sicherheitspatches (Firmware-Updates), da der OEM den Support einstellt. Diese Geräte können unabhängig von der installierten Software nicht als völlig sicher angesehen werden.

</div>

## Kauf-Hinweis

When purchasing a device, we recommend getting one as new as possible. The software and firmware of mobile devices are only supported for a limited time, so buying new extends that lifespan as much as possible.

Avoid buying phones from mobile network operators. These often have a **locked bootloader** and do not support [OEM unlocking](https://source.android.com/devices/bootloader/locking_unlocking). These phone variants will prevent you from installing any kind of alternative Android distribution.

Be very **careful** about buying second hand phones from online marketplaces. Always check the reputation of the seller. If the device is stolen, there's a possibility of it being entered in the [IMEI database](https://gsma.com/get-involved/working-groups/terminal-steering-group/imei-database). There is also a risk involved with you being associated with the activity of the previous owner.

A few more tips regarding Android devices and operating system compatibility:

- Do not buy devices that have reached or are near their end-of-life; additional firmware updates must be provided by the manufacturer.
- Do not buy preloaded LineageOS or /e/ OS phones or any Android phones without proper [Verified Boot](https://source.android.com/security/verifiedboot) support and firmware updates. These devices also have no way for you to check whether they've been tampered with.
- In short, if a device is not listed here, there is probably a good reason. Check out our [forum](https://discuss.privacyguides.net) to find details!

## Google Pixel

Google Pixel-Handys sind die **einzigen** Geräte, die wir zum Kauf empfehlen. Pixel-Telefone verfügen über eine stärkere Hardwaresicherheit als alle anderen Android-Geräte, die derzeit auf dem Markt sind. Dies ist auf die ordnungsgemäße AVB-Unterstützung für Betriebssysteme von Drittanbietern und die eigenen [Titan](https://security.googleblog.com/2021/10/pixel-6-setting-new-standard-for-mobile.html) Sicherheitschips von Google zurückzuführen, die als Secure Element fungieren.

<div class="admonition recommendation" markdown>

![Google Pixel 6](assets/img/android/google-pixel.png){ align=right }

**Google Pixel**-Geräte sind dafür bekannt, dass sie über eine gute Sicherheit verfügen und [Verified Boot](https://source.android.com/security/verifiedboot) ordnungsgemäß unterstützen, selbst wenn sie benutzerdefinierte Betriebssysteme installiert haben.

Ab dem **Pixel 8** und **8 Pro** erhalten Pixel-Geräte mindestens 7 Jahre lang garantierte Sicherheitsupdates, was im Vergleich zu den 2-5 Jahren, die konkurrierende OEMs üblicherweise anbieten, eine viel längere Lebensdauer gewährleistet.

[:material-shopping: Store](https://store.google.com/category/phones){ .md-button .md-button--primary }

</div>

Secure-Elements wie das Titan M2 sind eingeschränkter als die Trusted Execution Environment des Prozessors, die von den meisten anderen Handys verwendet wird, da sie nur für die Speicherung von Geheimnissen, die Hardware-Bescheinigung und die Ratenbegrenzung verwendet werden, nicht aber für die Ausführung "vertrauenswürdiger" Programme. Hndys ohne Secure-Element müssen das TEE für _alle_ diese Funktionen verwenden, was zu einer größeren Angriffsfläche führt.

Google Pixel-Telefone verwenden ein TEE-Betriebssystem namens Trusty, das im Gegensatz zu vielen anderen Telefonen [Open Source] (https://source.android.com/security/trusty#whyTrusty) ist.

Die Installation von GrapheneOS auf einem Pixel-Telefon ist mit dem [Web-Installer](https://grapheneos.org/install/web) einfach. Wenn du dich nicht wohl dabei fühlst, es selbst zu tun und bereit bist, etwas mehr Geld auszugeben, solltest du dir das [NitroPhone](https://shop.nitrokey.com/shop) ansehen, auf dem GrapheneOS von der renommierten Firma [Nitrokey](https://nitrokey.com/about) vorinstalliert ist.

Ein paar weitere Tipps für den Kauf eines Google Pixel:

- Wenn du ein Schnäppchen bei einem Pixel-Gerät machen möchtest, empfehlen wir dir, ein „**a**“-Modell zu kaufen, kurz nachdem das nächste Flaggschiff veröffentlicht wurde. Meist gibt es dann Rabatte, weil Google versucht, seine Bestände zu räumen.
- Consider price beating options and specials offered at physical stores.
- Look at online community bargain sites in your country. These can alert you to good sales.
- Google provides a list showing the [support cycle](https://support.google.com/nexus/answer/4457705) for each one of their devices. The price per day for a device can be calculated as: <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline" class="tml-display" style="display:inline math;"> <mfrac> <mtext>Cost</mtext> <mrow> <mtext>End of Life Date</mtext> <mo>−</mo> <mtext>Current Date</mtext> </mrow> </mfrac> </math>
  , meaning that the longer use of the device the lower cost per day.
- Auch wenn das Pixel in deiner Region nicht verfügbar ist, kann das [NitroPhone](https://shop.nitrokey.com/shop) weltweit versendet werden.

## Kriterien

**Bitte beachte, dass wir mit keinem der Projekte, die wir empfehlen, in Verbindung stehen.** Zusätzlich zu [unseren Standardkriterien](about/criteria.md) haben wir eine Reihe klarer Anforderungen entwickelt, die es uns ermöglichen, objektive Empfehlungen zu geben. Wir empfehlen dir, dich mit der Liste vertraut zu machen, bevor du dich für ein Projekt entscheidest, und deine eigenen Recherchen anzustellen, um sicherzustellen, dass es die richtige Wahl für dich ist.

- Muss mindestens eines der von uns empfohlenen benutzerdefinierten Betriebssysteme unterstützen.
- Muss derzeit neu im Handel erhältlich sein.
- Muss mindestens 5 Jahre lang Sicherheitsupdates erhalten.
- Must have dedicated secure element hardware.
