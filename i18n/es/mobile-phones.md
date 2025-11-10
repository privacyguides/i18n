---
title: Teléfonos celulares
icon: material/cellphone-check
description: Estos dispositivos móviles ofrecen el mejor soporte de seguridad de hardware para sistemas operativos Android personalizados.
cover: android.webp
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: Recomendaciones de teléfonos celulares
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

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-target-account: Ataques dirigidos](basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: Ataques pasivos](basics/common-threats.md#security-and-privacy){ .pg-orange }

La mayoría de los **teléfonos celulares** reciben actualizaciones de seguridad en periodos cortos o limitados por parte de los fabricantes; luego de que estos dispositivos alcanzan el final de su periodo de soporte, **no** pueden ser considerados como seguros porque no recibirán actualizaciones de seguridad del firmware o los controladores.

Los dispositivos móviles listados aquí proporcionan una larga vida útil de actualizaciones de seguridad garantizadas y permiten la instalación de un sistema operativo personalizado sin violar el modelo de seguridad de Android.

[Distribuciones de Android Recomendadas :material-arrow-right-drop-circle:](android/distributions.md){ .md-button .md-button--primary } [Detalles sobre la Seguridad de Android :material-arrow-right-drop-circle:](os/android-overview.md#security-protections){ .md-button }

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

Al final de su vida útil, los dispositivos (como los dispositivos con el "soporte extendido" de GrapheneOS) no tienen parches de seguridad completos (actualizaciones de firmware) debido a que el fabricante ha finalizado el soporte. Estos dispositivos no se pueden considerarse como completamente seguros, sin importar el software instalado.

</div>

## General Purchasing Advice

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

### Seguridad del hardware

Secure Elements like the Titan M2 are more limited than the processor's Trusted Execution Environment (TEE) used by most other phones as they are only used for secrets storage, hardware attestation, and rate limiting, not for running "trusted" programs. Los teléfonos sin un Entorno Seguro suelen utilizar TEE para _todas_ las demás funciones, lo que resulta en una gran superficie de ataque.

A diferencia de otros teléfonos, los Google Pixel utilizan un SO TEE de [código abierto](https://source.android.com/security/trusty#whyTrusty) llamado Trusty.

The Pixel 8 series and later supports ARM's Memory Tagging Extension ([MTE](https://developer.arm.com/documentation/108035/0100/Introduction-to-the-Memory-Tagging-Extension)), a hardware security enhancement that drastically lowers the probability of exploits occurring through memory corruption bugs. The stock Pixel OS allows you to enable MTE for supported apps through Google's Advanced Protection Program or via a developer option, but its usability is quite limited. [GrapheneOS](android/distributions.md#grapheneos), an alternative Android OS we recommend, greatly improves the usability and coverage of MTE in its implementation of the feature.

### Buying a Google Pixel

Algunos consejos adicionales al comprar un Google Pixel:

- Si buscas un Pixel económico, sugerimos comprar un modelo **a**, justo después del lanzamiento del modelo más nuevo. Los descuentos suelen estar disponibles porque Google intentará liquidar sus existencias.
- Considera las ofertas y promociones disponibles en tiendas físicas.
- Revisa las comunidades de ofertas en tu país. Estas pueden informarte sobre buenos descuentos.
- Google proporciona un listad con el [ciclo de soporte](https://support.google.com/nexus/answer/4457705) para cada uno de sus dispositivos. El precio por día de un dispositivo puede calcularse de la siguiente manera: <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline" class="tml-display" style="display:inline math;"> <mfrac> <mtext> Costo</mtext> <mrow> <mtext>Fecha del fin de vida útil</mtext> <mo>-</mo> <mtext>Fecha actual</mtext> </mrow> </mfrac> </math>
  , significando que el precio es más bajo entre más se use el dispositivo.
- Si el Pixel no se encuentra disponible en tu país, el [NitroPhone](https://shop.nitrokey.com/shop) cuenta con envíos a nivel mundial.

La instalación de GrapheneOS en un Pixel es sencilla con su [instalador web](https://grapheneos.org/install/web). Si no te sientes cómodo realizando esto por ti mismo y te gustaría invertir un poco más de dinero, echa un vistazo al [NitroPhone](https://shop.nitrokey.com/shop) que viene con GrapheneOS preinstalado y proviene de la reputada empresa [Nitrokey](https://nitrokey.com/about).

## Criterios

**Por favor, tome en cuenta que no estamos afiliados con ninguno de los proyectos recomendados.** Además de nuestros [criterios estándar](about/criteria.md), hemos desarrollado un claro conjunto de requerimientos que nos permite proporcionar recomendaciones objetivas. Sugerimos que te familiarices con esta lista, antes de decidir utilizar un proyecto y realizar tu propia investigación para asegurarte de que es la elección ideal para ti.

- Ser compatible como mínimo con uno de los sistemas operativos personalizados que recomendamos.
- Debe venderse como nuevo en las tiendas.
- Debe recibir actualizaciones de seguridad como mínimo durante 5 años.
- Debe contar con hardware dedicado de elemento seguro.
