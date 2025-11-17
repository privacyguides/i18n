---
meta_title: "Los Mejores Sistemas Operativos Android - Privacy Guides"
title: Distribuciones alternativas
description: Puedes reemplazar el sistema operativo en tu teléfono Android por estas alternativas seguras y respetuosas con la privacidad.
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: Private Android Operating Systems
    url: "./"
  - "@context": http://schema.org
    "@type": CreativeWork
    name: GrapheneOS
    image: /assets/img/android/grapheneos.svg
    url: https://grapheneos.org/
    sameAs: https://en.wikipedia.org/wiki/GrapheneOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: "./"
robots: nofollow, max-snippet:-1, max-image-preview:large
---

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-target-account: Ataques Dirigidos](../basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: Ataques Pasivos](../basics/common-threats.md#security-and-privacy){ .pg-orange }

Un **sistema operativo personalizado basado en Android** (a veces denominado **ROM personalizada**) puede ser una forma de conseguir un mayor nivel de privacidad y seguridad en tu dispositivo. Esto contrasta con la versión «stock» de Android que viene con el teléfono de fábrica, y que suele estar profundamente integrada con Google Play Services, así como con el software de otros proveedores.

Recomendamos instalar GrapheneOS si tienes un Google Pixel, ya que proporciona un endurecimiento de seguridad mejorado y funciones de privacidad adicionales. Las razones por las que no enumeramos otros sistemas operativos o dispositivos son las siguientes:

- Suelen tener [seguridad más débil](index.md#install-a-custom-distribution).
- El soporte se abandona con frecuencia cuando el mantenedor pierde interés o actualiza su dispositivo, lo que contrasta con el predecible [ciclo de soporte](https://grapheneos.org/faq#device-lifetime) que sigue GrapheneOS.
- Por lo general, presentan pocas o ninguna mejora notable de la privacidad o la seguridad que haga que merezca la pena instalarlas.

## GrapheneOS

<div class="admonition recommendation" markdown>

![Logo de GrapheneOS](../assets/img/android/grapheneos.svg#only-light){ align=right }
![Logo de GrapheneOS](../assets/img/android/grapheneos-dark.svg#only-dark){ align=right }

**GrapheneOS** es la mejor opción cuando se trata de privacidad y seguridad.

GrapheneOS proporciona [mejoras adicionales de seguridad](https://en.wikipedia.org/wiki/Hardening_\(computing\)) y privacidad. Dispone de un [asignador de memoria reforzado](https://github.com/GrapheneOS/hardened_malloc), permisos de red y sensores, y otras diversas [características de seguridad](https://grapheneos.org/features). GrapheneOS también incluye actualizaciones completas de firmware y compilaciones firmadas, por lo que el arranque verificado es totalmente compatible.

[:octicons-home-16: Página Principal](https://grapheneos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://grapheneos.org/faq#privacy-policy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://grapheneos.org/faq){ .card-link title="Documentación" }
[:octicons-code-16:](https://grapheneos.org/source){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title="Contribuir" }

</div>

GrapheneOS es compatible con [Google Play aislado](https://grapheneos.org/usage#sandboxed-google-play), que ejecuta los servicios de Google Play totalmente aislados como cualquier otra aplicación normal. Esto significa que puedes aprovechar la mayoría de los servicios de Google Play, como las notificaciones push, a la vez que tienes un control total sobre sus permisos y accesos, y los limitas a un [perfil de trabajo](../os/android-overview.md#work-profile) o [perfil de usuario](../os/android-overview.md#user-profiles) específico de tu elección.

Los [teléfonos Google Pixel](../mobile-phones.md#google-pixel) son los únicos dispositivos que actualmente cumplen los [requisitos de seguridad de hardware](https://grapheneos.org/faq#future-devices) de GrapheneOS. Los Pixel 8 y posteriores son compatibles con la Extensión de Etiquetado de Memoria (MTE) de ARM, una mejora de seguridad de hardware que reduce drásticamente la probabilidad de que se produzcan exploits a través de fallos de corrupción de memoria. GrapheneOS amplía enormemente la cobertura de MTE en los dispositivos compatibles. Mientras que el sistema operativo original solo permite optar por una implementación limitada de MTE a través de una opción de desarrollador o el Programa de Protección Avanzada de Google, GrapheneOS cuenta con una implementación más robusta de MTE por defecto en el núcleo del sistema, los componentes del sistema por defecto, y su navegador web Vanadium y su WebView.

GrapheneOS también ofrece una opción global para activar MTE en todas las aplicaciones instaladas por el usuario en :gear: **Configuración** → **Seguridad y privacidad** → **Protección contra exploits** → **Etiquetado de memoria** → **Activar por defecto**. El sistema operativo también ofrece la posibilidad de desactivar MTE en aplicaciones que pueden fallar por problemas de compatibilidad.

### Comprobaciones de Conectividad

Por defecto, Android realiza muchas conexiones de red a Google para realizar comprobaciones de conectividad DNS, para sincronizar con la hora actual de la red, para comprobar tu conectividad de red y para muchas otras tareas en segundo plano. GrapheneOS los sustituye por conexiones a servidores operados por GrapheneOS y sujetos a su política de privacidad. Esto oculta información como tu dirección IP [de Google](../basics/common-threats.md#privacy-from-service-providers), pero significa que es trivial para un administrador de tu red o ISP ver que estás haciendo conexiones a `grapheneos.network`, `grapheneos.org`, etc. y deducir qué sistema operativo estás usando.

Si quieres ocultar información como esta a un adversario de tu red o ISP, **debes** utilizar una [VPN de confianza](../vpn.md) además de cambiar la configuración de comprobación de conectividad a **Estándar (Google)**. Se puede encontrar en :gear: **Configuración** → **Red e Internet** → **Comprobaciones de conectividad a Internet**. Esta opción te permite conectarte a los servidores de Google para comprobar la conectividad, lo que, junto con el uso de una VPN, te ayuda a mezclarte con un grupo mayor de dispositivos Android.

## Criterios

**Por favor, ten en cuenta que no estamos afiliados a ninguno de los proyectos que recomendamos.** Además de [nuestros criterios estándar](../about/criteria.md), hemos desarrollado un conjunto claro de requisitos que nos permiten ofrecer recomendaciones objetivas. Sugerimos que te familiarices con esta lista, antes de decidir utilizar un proyecto y realizar tu propia investigación para asegurarte de que es la elección ideal para ti.

- Debe ser software de código abierto.
- Debe soportar el bloqueo del cargador de arranque con soporte de clave AVB personalizada.
- Debe recibir las principales actualizaciones de Android dentro de 0-1 meses desde su lanzamiento.
- Debe recibir actualizaciones de las funciones de Android (versión menor) en un plazo de 0 a 14 días desde su lanzamiento.
- Debe recibir parches de seguridad periódicos en un plazo de 0 a 5 días desde su publicación.
- No debe estar «rooteado» desde el principio.
- **No** debe habilitar Google Play Services por defecto.
- **No** debe requerir la modificación del sistema para admitir Google Play Services.
