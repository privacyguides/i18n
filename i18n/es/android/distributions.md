---
meta_title: Los mejores sistemas operativos personalizados de Android (también conocidos como Custom ROMs) - Privacy Guides
title: Distribuciones alternativas
description: Puedes reemplazar el sistema operativo en tu teléfono Android por estas alternativas seguras y respetuosas con la privacidad.
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: Private Android Operating Systems
    url: ./
  - "@context": http://schema.org
    "@type": CreativeWork
    name: GrapheneOS
    image: /assets/img/android/grapheneos.svg
    url: https://grapheneos.org/
    sameAs: https://en.wikipedia.org/wiki/GrapheneOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: ./
  - "@context": http://schema.org
    "@type": CreativeWork
    name: Divest
    image: /assets/img/android/divestos.svg
    url: https://divestos.org/
    sameAs: https://en.wikipedia.org/wiki/DivestOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: ./
robots: nofollow, max-snippet:-1, max-image-preview:large
---

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-target-account: Ataques Dirigidos](../basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: Ataques Pasivos](../basics/common-threats.md#security-and-privacy){ .pg-orange }

Un **sistema operativo personalizado basado en Android** (también conocido como **ROM** personalizada) es una manera popular de alcanzar altos niveles de privacidad y seguridad en tu dispositivo. Esto contrasta con la versión "stock" de Android que viene preinstalada en tu teléfono y está profundamente integrada con los Servicios de Google Play.

Recomendamos instalar uno de estos sistemas operativos personalizados Android en tu dispositivo, listados en orden de preferencia, dependiendo de la compatibilidad de tu dispositivo con estos sistemas operativos.

## Derivados de AOSP

### GrapheneOS

<div class="admonition recommendation" markdown>

![Logo de GrapheneOS](../assets/img/android/grapheneos.svg#only-light){ align=right }
![Logo de GrapheneOS](../assets/img/android/grapheneos-dark.svg#only-dark){ align=right }

**GrapheneOS** es la mejor opción cuando se trata de privacidad y seguridad.

GrapheneOS proporciona [mejoras adicionales de seguridad](https://en.wikipedia.org/wiki/Hardening_\(computing\)) y privacidad. Dispone de un [asignador de memoria reforzado](https://github.com/GrapheneOS/hardened_malloc), permisos de red y sensores, y otras diversas [características de seguridad](https://grapheneos.org/features). GrapheneOS también incluye actualizaciones completas de firmware y compilaciones firmadas, por lo que el arranque verificado es totalmente compatible.

[:octicons-home-16: Página Principal](https://grapheneos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://grapheneos.org/faq#privacy-policy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://grapheneos.org/faq){ .card-link title=Documentación}
[:octicons-code-16:](https://grapheneos.org/source){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribuir }

</div>

GrapheneOS es compatible con [Google Play aislado](https://grapheneos.org/usage#sandboxed-google-play), que ejecuta los servicios de Google Play totalmente aislados como cualquier otra aplicación normal. Esto significa que puedes aprovechar la mayoría de los servicios de Google Play, como las notificaciones push, a la vez que tienes un control total sobre sus permisos y accesos, y los limitas a un [perfil de trabajo](../os/android-overview.md#work-profile) o [perfil de usuario](../os/android-overview.md#user-profiles) específico de tu elección.

Los [teléfonos Google Pixel](../mobile-phones.md#google-pixel) son los únicos dispositivos que actualmente cumplen los [requisitos de seguridad de hardware] de GrapheneOS(https://grapheneos.org/faq#future-devices).

Por defecto, Android realiza muchas conexiones de red a Google para realizar comprobaciones de conectividad DNS, para sincronizar con la hora actual de la red, para comprobar tu conectividad de red y para muchas otras tareas en segundo plano. GrapheneOS los sustituye por conexiones a servidores operados por GrapheneOS y sujetos a su política de privacidad. Esto oculta información como tu dirección IP [de Google](../basics/common-threats.md#privacy-from-service-providers), pero significa que es trivial para un administrador de tu red o ISP ver que estás haciendo conexiones a `grapheneos.network`, `grapheneos.org`, etc. y deducir qué sistema operativo estás usando.

Si quieres ocultar información como esta a un adversario de tu red o ISP, **debes** utilizar una [VPN de confianza](../vpn.md) además de cambiar la configuración de comprobación de conectividad a **Estándar (Google)**. Se puede encontrar en :gear: **Configuración** → **Red e Internet** → **Comprobaciones de conectividad a Internet**. Esta opción te permite conectarte a los servidores de Google para comprobar la conectividad, lo que, junto con el uso de una VPN, te ayuda a mezclarte con un grupo mayor de dispositivos Android.

### DivestOS

Si GrapheneOS no es compatible con tu teléfono, DivestOS es una buena alternativa. Admite una amplia variedad de teléfonos con _varios_ niveles de protecciones de seguridad y control de calidad.

<div class="admonition recommendation" markdown>

![DivestOS logo](../assets/img/android/divestos.svg){ align=right }

**DivestOS** is a soft-fork of [LineageOS](https://lineageos.org).
DivestOS inherits many [supported devices](https://divestos.org/index.php?page=devices\&base=LineageOS) from LineageOS. It has signed builds, making it possible to have [verified boot](../os/android-overview.md#verified-boot) on some non-Pixel devices. Not all supported devices support verified boot or other security features.

[:octicons-home-16: Homepage](https://divestos.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://divestoseb5nncsydt7zzf5hrfg44md4bxqjs5ifcv4t7gt7u6ohjyyd.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://divestos.org/index.php?page=privacy_policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://divestos.org/index.php?page=faq){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/divested-mobile){ .card-link title="Source Code" }
[:octicons-heart-16:](https://divested.dev/pages/donate){ .card-link title="Contribute" }

</div>

The [status](https://gitlab.com/divested-mobile/firmware-empty/-/blob/master/STATUS) of firmware updates in particular will vary significantly depending on your phone model. While standard AOSP bugs and vulnerabilities can be fixed with standard software updates like those provided by DivestOS, some vulnerabilities cannot be patched without support from the device manufacturer, making end-of-life devices less safe even with an up-to-date alternative ROM like DivestOS.

DivestOS has automated kernel vulnerability ([CVE](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures)) [patching](https://gitlab.com/divested-mobile/cve_checker), fewer proprietary blobs, and a custom [hosts](https://divested.dev/index.php?page=dnsbl) file. Its hardened WebView, [Mulch](https://gitlab.com/divested-mobile/mulch), enables [control-flow integrity](https://en.wikipedia.org/wiki/Control-flow_integrity) for all architectures and [network state partitioning](https://developer.mozilla.org/docs/Web/Privacy/State_Partitioning), and receives out-of-band updates.

DivestOS also includes kernel patches from GrapheneOS and enables all available kernel security features via [defconfig hardening](https://github.com/Divested-Mobile/DivestOS-Build/blob/master/Scripts/Common/Functions.sh#L758). All kernels newer than version 3.4 include full page [sanitization](https://lwn.net/Articles/334747) and all ~22 Clang-compiled kernels have [`-ftrivial-auto-var-init=zero`](https://reviews.llvm.org/D54604?id=174471) enabled.

DivestOS implements some system hardening patches originally developed for GrapheneOS. DivestOS 16.0 and higher implements GrapheneOS's `INTERNET` and `SENSORS` permission toggle, [hardened memory allocator](https://github.com/GrapheneOS/hardened_malloc), [exec-spawning](https://grapheneos.org/usage#exec-spawning), Java Native Interface [constification](https://en.wikipedia.org/wiki/Const_\(computer_programming\)), and partial [bionic](https://en.wikipedia.org/wiki/Bionic_\(software\)) hardening patchsets. 17.1 and higher features per-network full MAC address randomization, [`ptrace_scope`](https://kernel.org/doc/html/latest/admin-guide/LSM/Yama.html) control, automatic reboot, and Wi-Fi/Bluetooth [timeout options](https://grapheneos.org/features#attack-surface-reduction).

DivestOS uses F-Droid as its default app store. We normally [recommend avoiding F-Droid](obtaining-apps.md#f-droid), but doing so on DivestOS isn't viable; the developers update their apps via their own F-Droid repository, [DivestOS Official](https://divestos.org/fdroid/official). For these apps you should continue to use F-Droid **with the DivestOS repository enabled** to keep those components up to date. For other apps, our recommended [methods of obtaining them](obtaining-apps.md) still apply.

DivestOS replaces many of Android's background network connections to Google services with alternative services, such as using OpenEUICC for eSIM activation, NTP.org for network time, and Quad9 for DNS. These connections can be modified, but their deviation from a standard Android phone's network connections could mean it is easier for an adversary on your network to deduce what operating system you have installed on your phone. If this is a concern to you, consider using a [trusted VPN](../vpn.md) and enabling the native VPN [kill switch](../os/android-overview.md#vpn-killswitch) to hide this network traffic from your local network and ISP.

## Criterios

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](../about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. Sugerimos que te familiarices con esta lista, antes de decidir utilizar un proyecto y realizar tu propia investigación para asegurarte de que es la elección ideal para ti.

- Debe ser software de código abierto.
- Must support bootloader locking with custom AVB key support.
- Must receive major Android updates within 0-1 months of release.
- Must receive Android feature updates (minor version) within 0-14 days of release.
- Must receive regular security patches within 0-5 days of release.
- Must **not** be "rooted" out of the box.
- Must **not** enable Google Play Services by default.
- Must **not** require system modification to support Google Play Services.
