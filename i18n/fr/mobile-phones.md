---
title: "Téléphones portables"
icon: material/cellphone-check
description: Les smartphones suivants possèdent la meilleure sécurité hardware pour les systèmes d'exploitation Android alternatifs (custom ROMs en anglais).
cover: android.webp
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: Recommandations de smartphones
    url: "./"
  - "@context": http://schema.org
    "@type": Article
    name: Pixel
    brand:
      "@type": Marque
      name: Google
    image: /assets/img/android/google-pixel.png
    sameAs: https://en.wikipedia.org/wiki/Google_Pixel
    review:
      "@type": Avis
      author:
        "@type": Organisation
        name: Privacy Guides
robots: nofollow, max-snippet:-1, max-image-preview:large
---

<small>Protège contre les menaces suivantes :</small>

- [:material-target-account: Targeted Attacks](basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: Attaque passive](basics/common-threats.md#security-and-privacy){ .pg-orange }

La plupart des fabricants d'équipement d'origine (OEM) fournissent des mises à jour de sécurité pour **smartphones** seulement sur une courte période ; une fois que ces appareils atteignent la fin de leur période de support logiciel, ils ne **peuvent plus** être considéré comme sécurisé, car ils ne reçoivent plus de mise à jour de sécurité pour leur micrologiciel ou leurs drivers (pilotes).

Les smartphones présentés ici reçoivent des mises à jour de sécurité pendant plus longtemps et vous permettent d'installer un système d'exploitation alternatif sans contrevenir au modèle de sécurité Android.

[Recommandations de systèmes d'exploitation Android :material-arrow-right-drop-circle:](android/distributions.md){ .md-button .md-button--primary } [Détails sur la sécurité d'Android :material-arrow-right-drop-circle:](os/android-overview.md#security-protections){ .md-button }

<div class="admonition warning" markdown>
<p class="admonition-title">Avertissement</p>

Les appareils en fin de vie (comme les appareils à "support prolongé" de GrapheneOS) ne reçoivent pas de mise à jour complète de leur micrologiciel en raison de l'abandon de ces mises à jour par les OEM. Ces appareils ne peuvent pas être considérés comme totalement sécurisé, quel que soit le logiciel installé.

</div>

## Conseil d'achat

Lorsque vous achetez un appareil, nous vous recommandons d'en acheter un le plus neuf possible. Puisque le logiciel et le micrologiciel d'un appareil ne sont mis à jour que pendant une courte période, acheter un appareil neuf permet de profiter de celle-ci un maximum.

Évitez d'acheter des téléphones auprès des opérateurs de réseaux mobiles. Ces appareils ont souvent un **bootloader vérouillé** et ne permettent pas le [déverouillage OEM](https://source.android.com/devices/bootloader/locking_unlocking). Cette fonctionnalité vous empêchera totalement d'installer des versions alternatives d'Android.

Soyez particulièrement **vigilant** lorsque vous acheter un smartphone d'occasion en ligne. Vérifiez toujours la réputation du vendeur. Si l'appareil est volé, il peut être inscrit sur la [base de donnée IMEI](https://gsma.com/get-involved/working-groups/terminal-steering-group/imei-database). Dans certains cas, vous pouvez également vous retrouver associé aux agissements du précédent propriétaire.

A few more tips regarding Android devices and operating system compatibility:

- Do not buy devices that have reached or are near their end-of-life; additional firmware updates must be provided by the manufacturer.
- Do not buy preloaded LineageOS or /e/ OS phones or any Android phones without proper [Verified Boot](https://source.android.com/security/verifiedboot) support and firmware updates. These devices also have no way for you to check whether they've been tampered with.
- In short, if a device is not listed here, there is probably a good reason. Check out our [forum](https://discuss.privacyguides.net) to find details!

## Google Pixel

Google Pixel phones are the **only** devices we recommend for purchase. Pixel phones have stronger hardware security than any other Android devices currently on the market, due to proper AVB support for third-party operating systems and Google's custom [Titan](https://security.googleblog.com/2021/10/pixel-6-setting-new-standard-for-mobile.html) security chips acting as the Secure Element.

<div class="admonition recommendation" markdown>

![Google Pixel 6](assets/img/android/google-pixel.png){ align=right }

**Google Pixel** devices are known to have good security and properly support [Verified Boot](https://source.android.com/security/verifiedboot), even when installing custom operating systems.

Beginning with the **Pixel 8** and **8 Pro**, Pixel devices receive a minimum of 7 years of guaranteed security updates, ensuring a much longer lifespan compared to the 2-5 years competing OEMs typically offer.

[:material-shopping: Store](https://store.google.com/category/phones){ .md-button .md-button--primary }

</div>

Secure Elements like the Titan M2 are more limited than the processor's Trusted Execution Environment used by most other phones as they are only used for secrets storage, hardware attestation, and rate limiting, not for running "trusted" programs. Phones without a Secure Element have to use the TEE for _all_ of those functions, resulting in a larger attack surface.

Google Pixel phones use a TEE OS called Trusty which is [open source](https://source.android.com/security/trusty#whyTrusty), unlike many other phones.

The installation of GrapheneOS on a Pixel phone is easy with their [web installer](https://grapheneos.org/install/web). If you don't feel comfortable doing it yourself and are willing to spend a bit of extra money, check out the [NitroPhone](https://shop.nitrokey.com/shop) as they come preloaded with GrapheneOS from the reputable [Nitrokey](https://nitrokey.com/about) company.

A few more tips for purchasing a Google Pixel:

- If you're after a bargain on a Pixel device, we suggest buying an "**a**" model, just after the next flagship is released. Discounts are usually available because Google will be trying to clear their stock.
- Consider price beating options and specials offered at physical stores.
- Look at online community bargain sites in your country. These can alert you to good sales.
- Google provides a list showing the [support cycle](https://support.google.com/nexus/answer/4457705) for each one of their devices. The price per day for a device can be calculated as: <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline" class="tml-display" style="display:inline math;"> <mfrac> <mtext>Cost</mtext> <mrow> <mtext>End of Life Date</mtext> <mo>−</mo> <mtext>Current Date</mtext> </mrow> </mfrac> </math>
  , meaning that the longer use of the device the lower cost per day.
- If the Pixel is unavailable in your region, the [NitroPhone](https://shop.nitrokey.com/shop) can be shipped globally.

## Critères

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. Nous vous suggérons de vous familiariser avec cette liste avant de choisir d'utiliser un projet, et de mener vos propres recherches pour vous assurer que c'est le bon choix pour vous.

- Must support at least one of our recommended custom operating systems.
- Must be currently sold new in stores.
- Must receive a minimum of 5 years of security updates.
- Must have dedicated secure element hardware.
