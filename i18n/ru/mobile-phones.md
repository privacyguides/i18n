---
title: Мобильные телефоны
icon: material/cellphone-check
description: These mobile devices provide the best hardware security support for custom Android operating systems.
cover: android.webp
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: Mobile Phone Recommendations
    url: "./"
  - "@context": http://schema.org
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
robots: nofollow, max-snippet:-1, max-image-preview:large
---

<small>Защищает от следующих угроз:</small>

- [:material-target-account: Целенаправленные атаки](basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: Пассивные атаки](basics/common-threats.md#security-and-privacy){ .pg-orange }

Most **mobile phones** receive short or limited windows of security updates from OEMs; after these devices reach the end of their support period, they **cannot** be considered secure as they no longer receive firmware or driver security updates.

The mobile devices listed here provide a long lifespan of guaranteed security updates and allow you to install a custom operating system without violating the Android security model.

[Recommended Android Distributions :material-arrow-right-drop-circle:](android/distributions.md){ .md-button .md-button--primary } [Details about Android Security :material-arrow-right-drop-circle:](os/android-overview.md#security-protections){ .md-button }

<div class="admonition warning" markdown>
<p class="admonition-title">Внимание!</p>

Устройства с истёкшим сроком службы (например, устройства на GrapheneOS с «расширенной поддержкой») не имеют полных исправлений безопасности (обновлений прошивки) из-за прекращения поддержки OEM-производителем. Эти устройства нельзя считать полностью безопасными, независимо от установленного программного обеспечения.

</div>

## General Purchasing Advice

При покупке устройства рекомендуем приобрести как можно более новое. ПО и прошивка мобильных устройств поддерживаются только в течение ограниченного периода времени, поэтому покупка нового устройства продлевает его жизненный цикл настолько, насколько это возможно.

Не покупайте телефоны у операторов мобильной связи. These often have a **locked bootloader** and do not support [OEM unlocking](https://source.android.com/devices/bootloader/locking_unlocking). These phone variants will prevent you from installing any kind of alternative Android distribution.

Будьте очень **осторожны** при покупке подержанных телефонов в интернет-магазинах. Всегда проверяйте репутацию продавца. If the device is stolen, there's a possibility of it being entered in the [IMEI database](https://gsma.com/get-involved/working-groups/terminal-steering-group/imei-database). There is also a risk involved with you being associated with the activity of the previous owner.

A few more tips regarding Android devices and operating system compatibility:

- Do not buy devices that have reached or are near their end-of-life; additional firmware updates must be provided by the manufacturer.
- Do not buy preloaded LineageOS or /e/ OS phones or any Android phones without proper [Verified Boot](https://source.android.com/security/verifiedboot) support and firmware updates. These devices also have no way for you to check whether they've been tampered with.
- Короче говоря, если устройство не указано в этом списке, вероятно, на это есть веская причина. Загляните на наш [форум](https://discuss.privacyguides.net), чтобы узнать подробности!

## Google Pixel

Телефоны Google Pixel - это **единственные** устройства, которые мы рекомендуем к покупке. Телефоны Pixel имеют более высокий уровень аппаратной безопасности, чем любые другие устройства Android, представленные в настоящее время на рынке, благодаря надлежащей поддержке AVB для сторонних операционных систем и кастомным чипам безопасности Google [Titan](https://security.googleblog.com/2021/10/pixel-6-setting-new-standard-for-mobile.html), выступающим в качестве элемента безопасности.

<div class="admonition recommendation" markdown>

![Google Pixel 6](assets/img/android/google-pixel.png){ align=right }

Устройства **Google Pixel** известны хорошей безопасностью и правильной поддержкой [Verified Boot](https://source.android.com/security/verifiedboot), даже при установке сторонних операционных систем.

Начиная с **Pixel 8** и **8 Pro**, устройства Pixel получают минимум 7 лет гарантированных обновлений безопасности, что обеспечивает гораздо более длительный срок службы по сравнению с 2-5 годами, которые обычно предлагают конкурирующие OEM-производители.

[:material-shopping: Магазин](https://store.google.com/category/phones){ .md-button .md-button--primary }

</div>

### Аппаратная безопасность

Элементы безопасности, такие как Titan M2, более ограничены, чем процессорная Trusted Execution Environment (TEE), используемая в большинстве других телефонов, поскольку они используются только для хранения секретов, аппаратной аттестации и ограничения скорости, а не для запуска "доверенных" программ. Телефоны без защищенного элемента вынуждены использовать TEE для _всех_ этих функций, что приводит к увеличению поверхности атаки.

Google Pixel phones use a TEE OS called Trusty which is [open source](https://source.android.com/security/trusty#whyTrusty), unlike many other phones.

The Pixel 8 series and later supports ARM's Memory Tagging Extension ([MTE](https://developer.arm.com/documentation/108035/0100/Introduction-to-the-Memory-Tagging-Extension)), a hardware security enhancement that drastically lowers the probability of exploits occurring through memory corruption bugs. The stock Pixel OS allows you to enable MTE for supported apps through Google's Advanced Protection Program or via a developer option, but its usability is quite limited. [GrapheneOS](android/distributions.md#grapheneos), an alternative Android OS we recommend, greatly improves the usability and coverage of MTE in its implementation of the feature.

### Buying a Google Pixel

A few more tips for purchasing a Google Pixel:

- If you're after a bargain on a Pixel device, we suggest buying an "**a**" model, just after the next flagship is released. Discounts are usually available because Google will be trying to clear their stock.
- Consider price beating options and specials offered at physical stores.
- Look at online community bargain sites in your country. These can alert you to good sales.
- Google provides a list showing the [support cycle](https://support.google.com/nexus/answer/4457705) for each one of their devices. The price per day for a device can be calculated as: <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline" class="tml-display" style="display:inline math;"> <mfrac> <mtext>Cost</mtext> <mrow> <mtext>End of Life Date</mtext> <mo>−</mo> <mtext>Current Date</mtext> </mrow> </mfrac> </math>
  , meaning that the longer use of the device the lower cost per day.
- If the Pixel is unavailable in your region, the [NitroPhone](https://shop.nitrokey.com/shop) can be shipped globally.

The installation of GrapheneOS on a Pixel phone is easy with their [web installer](https://grapheneos.org/install/web). If you don't feel comfortable doing it yourself and are willing to spend a bit of extra money, check out the [NitroPhone](https://shop.nitrokey.com/shop) as they come preloaded with GrapheneOS from the reputable [Nitrokey](https://nitrokey.com/about) company.

## Критерии

**Важно отметить, что мы не связаны с каким-либо проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md), мы разработали чёткий набор требований, обеспечивающий объективность наших рекомендаций. Перед тем, как вы решите выбрать какой-либо проект, мы рекомендуем вам ознакомиться со списком критериев и провести собственное исследование, чтобы убедиться в правильности своего выбора.

- Должны поддерживать хотя бы одну из рекомендованных нами кастомных операционных систем.
- Должны продаваться новыми в магазинах.
- Должны получать обновления безопасности минимум 5 лет.
- Должен быть отдельный аппаратный элемент безопасности.
