---
title: "Escritorio/PC"
icon: simple/linux
description: Las distribuciones de Linux se recomiendan comúnmente para la protección de la privacidad y la libertad del software.
cover: desktop.webp
---

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-account-cash: Capitalismo de Vigilancia](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Las distribuciones de Linux se recomiendan comúnmente para la protección de la privacidad y la libertad del software. Si aún no utiliza Linux, a continuación le sugerimos que pruebe algunas distribuciones, así como algunos consejos generales para mejorar la privacidad y la seguridad que son aplicables a muchas distribuciones de Linux.

- [Vista General de Linux :material-arrow-right-drop-circle:](os/linux-overview.md)

## Distribuciones Tradicionales

### Fedora Linux

<div class="admonition recommendation" markdown>

![Fedora logo](assets/img/linux-desktop/fedora.svg){ align=right }

**Fedora Linux** is our recommended desktop distribution for people new to Linux. Fedora generalmente adopta tecnologías más nuevas (por ejemplo, [Wayland](https://wayland.freedesktop.org) y [PipeWire](https://pipewire.org)) antes que otras distribuciones. Estas nuevas tecnologías suelen venir acompañadas de mejoras en la seguridad, la privacidad y la usabilidad en general.

[:octicons-home-16: Homepage](https://fedoraproject.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.fedoraproject.org/en-US/docs){ .card-link title="Documentation" }
[:octicons-heart-16:](https://whatcanidoforfedora.org){ .card-link title="Contribute" }

</details>

</div>

Fedora comes in two primary desktop editions, [Fedora Workstation](https://fedoraproject.org/workstation), which uses the GNOME desktop environment, and [Fedora KDE Plasma Desktop](https://fedoraproject.org/kde), which uses KDE. Historically, Fedora Workstation has been more popular and widely recommended, but KDE has been gaining in popularity and provides an experience more similar to Windows, which may make transitioning to Linux easier for some. The security and privacy benefits of both editions are very similar, so it mostly comes down to personal preference.

Fedora tiene un ciclo de lanzamientos semicontinuo. While some packages like the desktop environment are frozen until the next Fedora release, most packages (including the kernel) are updated frequently throughout the lifespan of the release. Cada versión de Fedora recibe soporte durante un año, con una nueva versión cada 6 meses.

### openSUSE Tumbleweed

<div class="admonition recommendation" markdown>

![openSUSE Tumbleweed logo](assets/img/linux-desktop/opensuse-tumbleweed.svg){ align=right }

**openSUSE Tumbleweed** es una distribución estable con actualización continua.

openSUSE Tumbleweed utiliza [Btrfs](https://es.wikipedia.org/wiki/Btrfs) y [Snapper](https://en.opensuse.org/openSUSE:Snapper_Tutorial) para garantizar que las instantáneas se puedan revertir en caso de que se produzca algún problema.

[:octicons-home-16: Homepage](https://get.opensuse.org/tumbleweed){ .md-button .md-button--primary }
[:octicons-info-16:](https://doc.opensuse.org){ .card-link title="Documentation" }
[:octicons-heart-16:](https://shop.opensuse.org){ .card-link title="Contribute" }

</details>

</div>

Tumbleweed sigue un modelo de actualización continua en el que cada actualización se publica como una copia instantánea de la distribución. Al actualizar el sistema, se descarga una nueva copia instantánea. Cada copia instantánea es sometida a una serie de pruebas automatizadas por [openQA](https://openqa.opensuse.org) para garantizar su calidad.

### Arch Linux

<div class="admonition recommendation" markdown>

![Arch logo](assets/img/linux-desktop/archlinux.svg){ align=right }

**Arch Linux** es una distribución ligera, "hágalo usted mismo" (DIY), lo que significa que solo tienes lo que instalas. Para obtener más información, consulte su [FAQ](https://wiki.archlinux.org/title/Frequently_asked_questions).

[:octicons-home-16: Homepage](https://archlinux.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://wiki.archlinux.org){ .card-link title="Documentation" }
[:octicons-heart-16:](https://archlinux.org/donate){ .card-link title="Contribute" }

</details>

</div>

Arch Linux tiene un ciclo de actualización continuo. No existe un calendario fijo de lanzamientos y los paquetes se actualizan con mucha frecuencia.

Al ser una distribución DIY, se espera que usted [configure y mantenga](os/linux-overview.md#arch-based-distributions) su sistema por su cuenta. Arch dispone de un [instalador oficial](https://wiki.archlinux.org/title/Archinstall) para facilitar el proceso de instalación.

Gran parte de [los paquetes de Arch Linux](https://reproducible.archlinux.org) son [reproducibles](https://reproducible-builds.org)[^1].

## Distribuciones Atómicas

**Las distribuciones atómicas** (a veces también denominadas **distribuciones inmutables**) son sistemas operativos que gestionan la instalación y actualización de paquetes superponiendo cambios sobre la imagen central del sistema, en lugar de modificarlo directamente. Las ventajas de las distribuciones atómicas incluyen una mayor estabilidad y la posibilidad de deshacer fácilmente las actualizaciones. Consulte [*Actualizaciones tradicionales vs. Atómicas*](os/linux-overview.md#traditional-vs-atomic-updates) para obtener más información.

### Fedora Atomic Desktops

<div class="admonition recommendation" markdown>

![Fedora logo](assets/img/linux-desktop/fedora.svg){ align=right }

**Fedora Atomic Desktops** son variantes de Fedora que utilizan el gestor de paquetes `rpm-ostree` y se centran principalmente en flujos de trabajo en contenedores y Flatpak para aplicaciones de escritorio. Todas estas variantes siguen el mismo calendario de lanzamientos que Fedora Workstation, beneficiándose de las mismas actualizaciones rápidas y manteniéndose muy cerca del upstream.

[:octicons-home-16: Homepage](https://fedoraproject.org/atomic-desktops){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.fedoraproject.org/en-US/emerging){ .card-link title="Documentation" }
[:octicons-heart-16:](https://whatcanidoforfedora.org){ .card-link title="Contribute" }

</details>

</div>

[Fedora Atomic Desktops](https://fedoramagazine.org/introducing-fedora-atomic-desktops) viene en una variedad de tipos dependiendo del entorno de escritorio que prefieras. Al igual que con la recomendación de evitar X11 en nuestros [criterios](#criteria) para las distribuciones de Linux, recomendamos evitar los tipos que solo soportan el sistema de ventanas X11 heredado.

These operating systems differ from Fedora Workstation as they replace the [DNF](https://docs.fedoraproject.org/en-US/quick-docs/dnf) package manager with a much more advanced alternative called [`rpm-ostree`](https://coreos.github.io/rpm-ostree). El gestor de paquetes `rpm-ostree` funciona descargando una imagen base para el sistema, y luego superponiendo paquetes sobre ella en un árbol de commit [git](https://en.wikipedia.org/wiki/Git)-like. Cuando se actualice el sistema, se descargará una nueva imagen base y las superposiciones se aplicarán a esa nueva imagen.

Una vez finalizada la actualización, reiniciará el sistema en la nueva implantación. `rpm-ostree` mantiene dos despliegues del sistema para que usted pueda fácilmente volver atrás si algo se rompe en el nuevo despliegue. También existe la opción de anclar más implementaciones según sea necesario.

[Flatpak](https://flatpak.org) is the primary package installation method on these distributions, as `rpm-ostree` is only meant to overlay packages that cannot stay inside a container on top of the base image.

Como alternativa a Flatpaks, existe la opción de [Toolbx](https://docs.fedoraproject.org/en-US/fedora-silverblue/toolbox) para crear contenedores [Podman](https://podman.io) que imitan un entorno Fedora tradicional, una [característica útil](https://containertoolbx.org) para el desarrollador exigente. Estos contenedores comparten un directorio de inicio con el sistema operativo anfitrión.

### NixOS

<div class="admonition recommendation" markdown>

![NixOS logo](assets/img/linux-desktop/nixos.svg){ align=right }

NixOS es una distribución independiente basada en el gestor de paquetes Nix y centrada en la reproducibilidad y la fiabilidad.

[:octicons-home-16: Homepage](https://nixos.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://nixos.org/learn.html){ .card-link title="Documentation" }
[:octicons-heart-16:](https://nixos.org/donate.html){ .card-link title="Contribute" }

</details>

</div>

El gestor de paquetes de NixOS guarda cada versión de cada paquete en una carpeta diferente del almacén **Nix**. Debido a esto, puedes tener diferentes versiones del mismo paquete instalado en tu sistema. Después de escribir el contenido del paquete en la carpeta, esta pasa a ser de solo lectura.

NixOS también proporciona actualizaciones atómicas. Primero descarga (o construye) los paquetes y archivos para la nueva generación de sistemas y luego cambia a ella. There are different ways to switch to a new generation: you can tell NixOS to activate it after reboot, or you can switch to it at runtime. También puedes *probar* la nueva generación cambiando a ella durante el tiempo de ejecución, pero sin establecerla como la generación actual del sistema. Si algo en el proceso de actualización se rompe, puedes simplemente reiniciar y automáticamente volver a una versión de trabajo de tu sistema.

El gestor de paquetes Nix utiliza un lenguaje puramente funcional -que también se llama Nix- para definir paquetes.

[Nixpkgs](https://github.com/nixos/nixpkgs) (la fuente principal de paquetes) se encuentra en un único repositorio de GitHub. También puedes definir tus propios paquetes en el mismo idioma e incluirlos fácilmente en tu configuración.

Nix es un gestor de paquetes basado en el código fuente; si no hay ningún paquete preconstruido disponible en la caché de binarios, Nix simplemente construirá el paquete desde el código fuente usando su definición. Construye cada paquete en un entorno aislado *puro*, lo más independiente posible del sistema anfitrión. Los binarios construidos con este método son reproducibles[^1].

## Distribuciones Enfocadas en el Anonimato

### Whonix

<div class="admonition recommendation" markdown>

![Whonix logo](assets/img/linux-desktop/whonix.svg){ align=right }

**Whonix** está basado en [Kicksecure](#kicksecure), una bifurcación de Debian centrada en la seguridad. Su objetivo es proporcionar privacidad, seguridad y [:material-incognito: Anonimato](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple } en Internet. Whonix se utiliza mejor junto con [Qubes OS](#qubes-os).

[:octicons-home-16: Homepage](https://whonix.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://dds6qkxpwdeubwucdiaord2xgbbeyds25rbsgr73tbfpqpt4a6vjwsyd.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://whonix.org/wiki/Documentation){ .card-link title="Documentation" }
[:octicons-heart-16:](https://whonix.org/wiki/Donate){ .card-link title="Contribute" }

</details>

</div>

Whonix está pensado para funcionar como dos máquinas virtuales: una "Estación de Trabajo" y una "Puerta de Enlace" Tor. Todas las comunicaciones desde la Estación de Trabajo deben pasar por la puerta de enlace Tor. Esto significa que incluso si la Estación de Trabajo se ve comprometida por algún tipo de malware, la verdadera dirección IP permanecerá oculta.

Algunas de sus características incluyen Tor Stream Isolation, [anonimización de pulsaciones de teclas](https://whonix.org/wiki/Keystroke_Deanonymization#Kloak), [swap encriptado](https://github.com/Whonix/swap-file-creator) y un asignador de memoria endurecido. Las futuras versiones de Whonix probablemente incluirán [políticas AppArmor para todo el sistema](https://github.com/roddhjav/apparmor.d) y un [lanzador de aplicaciones aislado](https://whonix.org/wiki/Sandbox-app-launcher) para confinar completamente todos los procesos del sistema.

Whonix se utiliza mejor [junto con Qubes](https://whonix.org/wiki/Qubes/Why_use_Qubes_over_other_Virtualizers). Tenemos una [guía recomendada](os/qubes-overview.md#connecting-to-tor-via-a-vpn) sobre la configuración de Whonix junto con una VPN ProxyVM en Qubes para ocultar tus actividades Tor de tu ISP.

### Tails

<div class="admonition recommendation" markdown>

![Tails logo](assets/img/linux-desktop/tails.svg){ align=right }

**Tails** es un sistema operativo basado en Debian que enruta todas las comunicaciones a través de Tor, y que puede arrancar en casi cualquier ordenador desde un DVD, una memoria USB o una tarjeta SD. Utiliza [Tor](tor.md) para preservar la privacidad y el [:material-incognito: Anonimato](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple } mientras elude la censura, y no deja rastro de sí mismo en el ordenador en el que se utiliza una vez apagado.

[:octicons-home-16: Homepage](https://tails.net){ .md-button .md-button--primary }
[:octicons-info-16:](https://tails.net/doc/index.en.html){ .card-link title="Documentation" }
[:octicons-heart-16:](https://tails.net/donate){ .card-link title="Contribute" }

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

Tails [no borra](https://gitlab.tails.boum.org/tails/tails/-/issues/5356) la [memoria de vídeo](https://en.wikipedia.org/wiki/Dual-ported_video_RAM) al apagar. Cuando reinicie el ordenador después de usar Tails, puede que aparezca brevemente la última pantalla que se mostró en Tails. Si apaga el ordenador en lugar de reiniciarlo, la memoria de vídeo se borrará automáticamente después de estar un tiempo sin alimentación.

</div>

Tails es genial contra el análisis forense debido a la amnesia (lo que significa que no se escribe nada en el disco); sin embargo, no es una distribución endurecida como Whonix. Carece de muchas de las funciones de anonimato y seguridad que tiene Whonix y se actualiza con mucha menos frecuencia (solo una vez cada seis semanas). Un sistema Tails comprometido por malware puede potencialmente saltarse el proxy transparente, permitiendo que el usuario sea desanonimizado.

Tails incluye [uBlock Origin](browser-extensions.md#ublock-origin) en el Navegador Tor por defecto, lo que potencialmente puede facilitar a los adversarios la toma de huellas digitales de los usuarios de Tails. Las máquinas virtuales de [Whonix](desktop.md#whonix) pueden ser más a prueba de fugas, sin embargo no son amnésicas, lo que significa que los datos pueden ser recuperados de su dispositivo de almacenamiento.

Tails está diseñado para formatearse por completo después de cada reinicio. El [almacenamiento persistente](https://tails.net/doc/persistent_storage/index.en.html) cifrado puede configurarse para almacenar algunos datos entre reinicios.

## Distribuciones Enfocadas en la Seguridad

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-bug-outline: Ataques pasivos](basics/common-threats.md#security-and-privacy ""){.pg-orange}

### Qubes OS

<div class="admonition recommendation" markdown>

![Qubes OS logo](assets/img/qubes/qubes_os.svg){ align=right }

**Qubes OS** es un sistema operativo de código abierto diseñado para proporcionar una fuerte seguridad para la informática de escritorio a través de máquinas virtuales seguras (o "qubes"). Qubes se basa en Xen, el Sistema de Ventanas X y Linux. Puede ejecutar la mayoría de las aplicaciones Linux y utilizar la mayoría de los controladores Linux.

[:octicons-home-16: Homepage](https://qubes-os.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://qubesosfasa4zl44o4tws22di6kepyzfeqv3tg4e3ztknltfxqrymdad.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://qubes-os.org/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://qubes-os.org/doc){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/QubesOS){ .card-link title="Source Code" }
[:octicons-heart-16:](https://qubes-os.org/donate){ .card-link title="Contribute" }

</details>

</div>

Qubes OS asegura el ordenador aislando subsistemas (por ejemplo, redes, USB, etc.) y aplicaciones en *qubes*separadas. En caso de que una parte del sistema se vea comprometida a través de un exploit en un [:material-target-account: Ataque Dirigido](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}, es probable que el aislamiento adicional proteja el resto de las *qubes* y el núcleo del sistema.

Para más información sobre el funcionamiento de Qubes, consulta nuestra página [Qubes OS overview](os/qubes-overview.md).

### Secureblue

<div class="admonition recommendation" markdown>

![Secureblue logo](assets/img/linux-desktop/secureblue.svg){ align=right }

**Secureblue** is a security-focused operating system based on [Fedora Atomic Desktops](#fedora-atomic-desktops). It includes a number of [security features](https://secureblue.dev/features) intended to proactively defend against the exploitation of both known and unknown vulnerabilities, and ships with [Trivalent](https://github.com/secureblue/Trivalent), their hardened, Chromium-based web browser.

[:octicons-home-16: Homepage](https://secureblue.dev){ .md-button .md-button--primary }
[:octicons-info-16:](https://secureblue.dev/install){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/secureblue/secureblue){ .card-link title="Source Code" }
[:octicons-heart-16:](https://secureblue.dev/donate){ .card-link title="Contribute" }

</div>

**Trivalent** is Secureblue's hardened Chromium for desktop Linux inspired by [GrapheneOS](android/distributions.md#grapheneos)'s Vanadium browser.

Secureblue also provides GrapheneOS's [hardened memory allocator](https://github.com/GrapheneOS/hardened_malloc) and enables it globally (including for Flatpaks).

### Kicksecure

Aunque en la mayoría de los casos [desaconsejamos](os/linux-overview.md#release-cycle) las distribuciones "perpetuamente obsoletas" como Debian para uso de escritorio, Kicksecure es un sistema operativo basado en Debian que ha sido reforzado para ser mucho más que una instalación típica de Linux.

<div class="admonition recommendation" markdown>

![Kicksecure logo](assets/img/linux-desktop/kicksecure.svg){ align=right }

**Kicksecure** -en términos muy simplificados- es un conjunto de scripts, configuraciones y paquetes que reducen sustancialmente la superficie de ataque de Debian. Cubre muchas recomendaciones de privacidad y seguridad por defecto. También sirve de sistema operativo base para [Whonix](#whonix).

[:octicons-home-16: Homepage](https://kicksecure.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://kicksecure.com/wiki/Privacy_Policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kicksecure.com/wiki/Documentation){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/Kicksecure){ .card-link title="Source Code" }
[:octicons-heart-16:](https://kicksecure.com/wiki/Donate){ .card-link title="Contribute" }

</details>

</div>

## Criterios

La elección de una distribución Linux adecuada para ti dependerá de una gran variedad de preferencias personales, y esta página **no** pretende ser una lista exhaustiva de todas las distribuciones viables. En nuestra página de información general sobre Linux encontrarás algunos consejos sobre [elegir una distribución](os/linux-overview.md#choosing-your-distribution) con más detalle. Todas las distribuciones que se encuentran en *esta* página siguen, en general, las directrices que cubrimos allí, y todas cumplen estas normas:

- Gratis y de código abierto.
- Recibe actualizaciones periódicas del software y del kernel.
- Evita X11, ya que su última versión importante fue hace [más de una década](https://x.org/wiki/Releases).
    - La excepción notable aquí es Qubes, pero los [problemas de aislamiento](https://blog.invisiblethings.org/2011/04/23/linux-security-circus-on-gui-isolation) que X11 suele tener se evitan con la virtualización. Este aislamiento solo se aplica a las aplicaciones *que se ejecutan en diferentes qubes* (máquinas virtuales); las aplicaciones que se ejecutan en el *mismo* qube no están protegidas entre sí.
- Admite el cifrado de disco completo durante la instalación.
- No congela las publicaciones periódicas durante más de 1 año.
    - Nosotros [no recomendamos](os/linux-overview.md#release-cycle) distribuciones "Long Term Support (Soporte a Largo Plazo)" o "stable (estable)" para uso de escritorio.
- Es compatible con una amplia variedad de hardware.
- Preferencia hacia proyectos más grandes.
    - Mantener un sistema operativo es un gran reto, y los proyectos más pequeños tienden a cometer más errores evitables o a retrasar las actualizaciones críticas (o peor aún, a desaparecer por completo). Nos inclinamos por proyectos que probablemente seguirán existiendo dentro de 10 años (ya sea gracias al respaldo de empresas o a un apoyo muy significativo de la comunidad), y nos alejamos de los proyectos construidos a mano o con un número reducido de mantenedores.

Además, [nuestros criterios estándar](about/criteria.md) para los proyectos recomendados se siguen aplicando. **Ten en cuenta que no estamos afiliados a ninguno de los proveedores que recomendamos.**

[^1]: La reproducibilidad implica la capacidad de verificar que los paquetes y binarios puestos a disposición del usuario final coinciden con el código fuente, lo que puede ser útil contra posibles [:material-package-variant-closed-remove: Ataques a la Cadena de Suministro](basics/common-threats.md#attacks-against-certain-organizations ""){.pg-viridian}.
