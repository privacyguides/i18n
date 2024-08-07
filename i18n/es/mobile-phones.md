---
title: Teléfonos celulares
icon: material/cellphone-check
description: Estos dispositivos móviles son compatibles con Android Verified Boot para los sistemas operativos personalizados.
cover: android.webp
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: Recomendaciones de teléfonos celulares
    url: ./
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
---

La mayoría de los **teléfonos celulares** reciben actualizaciones de seguridad en periodos cortos o limitados por parte de los fabricantes; luego de que estos dispositivos alcanzan el final de su periodo de soporte, **no** pueden ser considerados como seguros porque no recibirán actualizaciones de seguridad del firmware o los controladores.

Los dispositivos móviles listados aquí proporcionan una larga vida útil de actualizaciones de seguridad garantizadas y permiten la instalación de un sistema operativo personalizado sin violar el modelo de seguridad de Android.

[Sistemas operativos recomendados :material-arrow-right-drop-circle:](android/distributions.md){ .md-button .md-button--primary } [Detalles sobre la seguridad de Android :material-arrow-right-drop-circle:](os/android-overview.md#security-protections){ .md-button }

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

Al final de su vida útil, los dispositivos (como los dispositivos con el "soporte extendido" de GrapheneOS) no tienen parches de seguridad completos (actualizaciones de firmware) debido a que el fabricante ha finalizado el soporte. Estos dispositivos no se pueden considerarse como completamente seguros, sin importar el software instalado.

</div>

## Consejo de compra

Al comprar un dispositivo, recomendamos obtener uno tan nuevo como sea posible. El software y el firmware de los dispositivos móviles cuentan con soporte por un periodo limitado de tiempo, por lo que comprar uno nuevo extiende la vida útil tanto como sea posible.

Evita comprar teléfonos de los operadores de telefonía celular. Estos suelen tener el **bootloader bloqueado** y no soportan el [desbloqueo OEM](https://source.android.com/devices/bootloader/locking_unlocking). Estas variantes de teléfonos impiden la instalación de cualquier distribución alternativa de Android.

Se **cuidadoso** al comprar teléfonos usados en mercados en línea. Siempre revisa la reputación del vendedor. Si el dispositivo es robado, existe una posibilidad de que se encuentre en la [base de datos de IMEI](https://gsma.com/get-involved/working-groups/terminal-steering-group/imei-database). También hay un riesgo de terminar involucrado en la actividad del propietario anterior.

Algunos consejos adicionales sobre los dispositivos Android y la compatibilidad con sistemas operativos:

- No compres dispositivos que han alcanzado o están cerca de su final de vida útil; las actualizaciones adicionales del firmware deben ser proporcionadas por el fabricante.
- No compres teléfonos con el sistema operativo LineageOS o /e/ preinstalado, o cualquier teléfono Android sin compatibilidad con el [arranque verificado](https://source.android.com/security/verifiedboot) y las actualizaciones de firmware. No puedes comprobar si el dispositivo ha sido manipulado.
- En resumen, si un dispositivo no está listado aquí, probablemente es por una buena razón. ¡Revisa nuestro [foro](https://discuss.privacyguides.net) para obtener más información!

## Google Pixel

Los teléfonos Google Pixel son los **únicos** dispositivos que recomendamos comprar. Los teléfonos Pixel tienen una seguridad de hardware superior a la de otros dispositivos Android en el mercado, debido al correcto soporte de AVB para los sistemas operativos de terceros y los chips personalizados de seguridad [Titan](https://security.googleblog.com/2021/10/pixel-6-setting-new-standard-for-mobile.html) de Google, que actúan como el Elemento de Seguridad.

<div class="admonition recommendation" markdown>

![Google Pixel 6](assets/img/android/google-pixel.png){ align=right }

Los dispositivos **Google Pixel** son conocidos por contar con buena seguridad y compatiblidad con el [arranque verificado](https://source.android.com/security/verifiedboot), incluso cuando se ha instalado un sistema operativo personalizado.

Iniciando con el **Pixel 8** y **8 Pro**, los dispositivos Pixel cuentan como mínimo con 7 años de actualizaciones de seguridad garantizadas, garantizando una mayor vida útil a comparación de los 2-5 años ofrecidos por otros fabricantes.

[:material-shopping: Tienda](https://store.google.com/category/phones){ .md-button .md-button--primary }

</div>

Los Elementos Seguros como el Titan M2 se encuentran limitados al Entorno de Ejecución Confiable del procesador, utilizado por la mayoría de los otros teléfono para el almacenamiento secreto, la certificación de hardware y la limitación de velocidad, no para ejecutar programas "confiables". Los teléfonos sin un Entorno Seguro suelen utilizar TEE para _todas_ las demás funciones, lo que resulta en una gran superficie de ataque.

A diferencia de otros teléfonos, los Google Pixel utilizan un SO TEE de [código abierto](https://source.android.com/security/trusty#whyTrusty) llamado Trusty.

La instalación de GrapheneOS en un Pixel es sencilla con su [instalador web](https://grapheneos.org/install/web). If you don't feel comfortable doing it yourself and are willing to spend a bit of extra money, check out the [NitroPhone](https://shop.nitrokey.com/shop) as they come preloaded with GrapheneOS from the reputable [Nitrokey](https://nitrokey.com/about) company.

A few more tips for purchasing a Google Pixel:

- If you're after a bargain on a Pixel device, we suggest buying an "**a**" model, just after the next flagship is released. Discounts are usually available because Google will be trying to clear their stock.
- Consider price beating options and specials offered at physical stores.
- Look at online community bargain sites in your country. These can alert you to good sales.
- Google provides a list showing the [support cycle](https://support.google.com/nexus/answer/4457705) for each one of their devices. The price per day for a device can be calculated as: <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline" class="tml-display" style="display:inline math;"> <mfrac> <mtext>Cost</mtext> <mrow> <mtext>End of Life Date</mtext> <mo>−</mo> <mtext>Current Date</mtext> </mrow> </mfrac> </math>
  , meaning that the longer use of the device the lower cost per day.
- If the Pixel is unavailable in your region, the [NitroPhone](https://shop.nitrokey.com/shop) can be shipped globally.

## Criterios

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. Sugerimos que te familiarices con esta lista, antes de decidir utilizar un proyecto y realizar tu propia investigación para asegurarte de que es la elección ideal para ti.

- Must support at least one of our recommended custom operating systems.
- Must be currently sold new in stores.
- Must receive a minimum of 5 years of security updates.
- Must have dedicated secure element hardware.
