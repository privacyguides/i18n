---
title: "Escritorio/PC"
icon: simple/linux
description: Las distribuciones de Linux se recomiendan comúnmente para la protección de la privacidad y la libertad del software.
cover: desktop.webp
---

Las distribuciones de Linux se recomiendan comúnmente para la protección de la privacidad y la libertad del software. Si aún no utiliza Linux, a continuación le sugerimos que pruebe algunas distribuciones, así como algunos consejos generales para mejorar la privacidad y la seguridad que son aplicables a muchas distribuciones de Linux.

- [Vista General de Linux :material-arrow-right-drop-circle:](os/linux-overview.md)

## Distribuciones Tradicionales

### Fedora Workstation

<div class="admonition recommendation" markdown>

![Fedora logo](assets/img/linux-desktop/fedora-workstation.svg){ align=right }

**Fedora Workstation** es nuestra distribución recomendada para la gente nueva en Linux. Fedora suele adoptar tecnologías más recientes antes que otras distribuciones, por ejemplo, [Wayland](https://wayland.freedesktop.org/), [PipeWire](https://pipewire.org). Estas nuevas tecnologías suelen venir acompañadas de mejoras en la seguridad, la privacidad y la usabilidad en general.

[:octicons-home-16: Página Principal](https://fedoraproject.org/workstation/){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.fedoraproject.org/en-US/docs/){ .card-link title=Documentación}
[:octicons-heart-16:](https://whatcanidoforfedora.org/){ .card-link title=Contribuir}

</details>

</div>

Fedora tiene un ciclo de lanzamientos semicontinuo. Mientras que algunos paquetes como [GNOME](https://www.gnome.org) quedan congelados hasta la siguiente versión de Fedora, la mayoría de los paquetes (incluido el kernel) se actualizan con frecuencia durante toda la vida útil de la versión. Cada versión de Fedora recibe soporte durante un año, con una nueva versión cada 6 meses.

### openSUSE Tumbleweed

<div class="admonition recommendation" markdown>

![openSUSE Tumbleweed logo](assets/img/linux-desktop/opensuse-tumbleweed.svg){ align=right }

**openSUSE Tumbleweed** es una distribución estable con actualización continua.

openSUSE Tumbleweed cuenta con un sistema de [actualización transaccional](https://kubic.opensuse.org/blog/2018-04-04-transactionalupdates/) que utiliza [Btrfs](https://en.wikipedia.org/wiki/Btrfs) y [Snapper](https://en.opensuse.org/openSUSE:Snapper_Tutorial) para garantizar que las copias instantáneas se puedan revertir en caso de que haya algún problema.

[:octicons-home-16: Página Principal](https://get.opensuse.org/tumbleweed/){ .md-button .md-button--primary }
[:octicons-info-16:](https://doc.opensuse.org/){ .card-link title=Documentación}
[:octicons-heart-16:](https://shop.opensuse.org/){ .card-link title=Contribuir }

</details>

</div>

Tumbleweed sigue un modelo de actualización continua en el que cada actualización se publica como una copia instantánea de la distribución. Al actualizar el sistema, se descarga una nueva copia instantánea. Cada copia instantánea es sometida a una serie de pruebas automatizadas por [openQA](https://openqa.opensuse.org) para garantizar su calidad.

### Arch Linux

<div class="admonition recommendation" markdown>

![Arch logo](assets/img/linux-desktop/archlinux.svg){ align=right }

**Arch Linux** es una distribución ligera del estilo "hágalo usted mismo" (DIY), lo que significa que sólo obtiene lo que instala. Para obtener más información, consulte su [FAQ](https://wiki.archlinux.org/title/Frequently_asked_questions).

[:octicons-home-16: Página Principal](https://archlinux.org/){ .md-button .md-button--primary }
[:octicons-info-16:](https://wiki.archlinux.org/){ .card-link title=Documentación}
[:octicons-heart-16:](https://archlinux.org/donate/){ .card-link title=Contribuir }

</details>

</div>

Arch Linux tiene un ciclo de actualización continuo. No existe un calendario fijo de lanzamientos y los paquetes se actualizan con mucha frecuencia.

Al ser una distribución DIY, se espera que usted [configure y mantenga](os/linux-overview.md#arch-based-distributions) su sistema por su cuenta. Arch dispone de un [instalador oficial](https://wiki.archlinux.org/title/Archinstall) para facilitar el proceso de instalación.

Gran parte de los [paquetes de Arch Linux](https://reproducible.archlinux.org) son [reproducibles](https://reproducible-builds.org).

## Distribuciones Inmutables

### Fedora Atomic Desktops

<div class="admonition recommendation" markdown>

![Fedora logo](assets/img/linux-desktop/fedora.svg){ align=right }

**Fedora Atomic Desktops** are the immutable variants of Fedora with a strong focus on containerized workflows and Flatpak for desktop applications. Todas estas variantes siguen el mismo calendario de lanzamientos que Fedora Workstation, beneficiándose de las mismas actualizaciones rápidas y manteniéndose muy cerca del upstream.

[:octicons-home-16: Homepage](https://fedoraproject.org/atomic-desktops/){ .md-button .md-button--primary }
[:octicons-heart-16:](https://whatcanidoforfedora.org/){ .card-link title=Contribute }

</details>

</div>

The [Fedora Atomic Desktops](https://fedoramagazine.org/introducing-fedora-atomic-desktops/) come in a variety of flavors depending on the desktop environment you prefer, such as **Fedora Silverblue** (which comes with [GNOME](https://www.gnome.org/)), **Fedora Kinoite**, (which comes with [KDE](https://kde.org/)), **Fedora Sway Atomic**, or **Fedora Budgie Atomic**. However, we don't recommend the last of these as the Budgie desktop environment [still requires X11](https://buddiesofbudgie.org/blog/wayland).

These operating systems differ from Fedora Workstation as they replace the [DNF](https://docs.fedoraproject.org/en-US/quick-docs/dnf/) package manager with a much more advanced alternative called [`rpm-ostree`](https://docs.fedoraproject.org/en-US/fedora/latest/system-administrators-guide/package-management/rpm-ostree/). The `rpm-ostree` package manager works by downloading a base image for the system, then overlaying packages over it in a [git](https://en.wikipedia.org/wiki/Git)-like commit tree. When the system is updated, a new base image is downloaded and the overlays will be applied to that new image.

After the update is complete you will reboot the system into the new deployment. `rpm-ostree` keeps two deployments of the system so that you can easily rollback if something breaks in the new deployment. There is also the option to pin more deployments as needed.

[Flatpak](https://www.flatpak.org) is the primary package installation method on these distributions, as `rpm-ostree` is only meant to overlay packages that cannot stay inside of a container on top of the base image.

As an alternative to Flatpaks, there is the option of [Toolbox](https://docs.fedoraproject.org/en-US/fedora-silverblue/toolbox/) to create [Podman](https://podman.io) containers with a shared home directory with the host operating system and mimic a traditional Fedora environment, which is a [useful feature](https://containertoolbx.org) for the discerning developer.

### NixOS

<div class="admonition recommendation" markdown>

![NixOS logo](assets/img/linux-desktop/nixos.svg){ align=right }

NixOS es una distribución independiente basada en el gestor de paquetes Nix y centrada en la reproducibilidad y la fiabilidad.

[:octicons-home-16: Página Principal](https://nixos.org/){ .md-button .md-button--primary }
[:octicons-info-16:](https://nixos.org/learn.html){ .card-link title=Documentación}
[:octicons-heart-16:](https://nixos.org/donate.html){ .card-link title=Contribuir }

</details>

</div>

NixOS’s package manager keeps every version of every package in a different folder in the **Nix store**. Due to this you can have different versions of the same package installed on your system. After the package contents have been written to the folder, the folder is made read-only.

NixOS also provides atomic updates; first it downloads (or builds) the packages and files for the new system generation and then switches to it. There are different ways to switch to a new generation; you can tell NixOS to activate it after reboot or you can switch to it at runtime. You can also *test* the new generation by switching to it at runtime, but not setting it as the current system generation. If something in the update process breaks, you can just reboot and automatically and return to a working version of your system.

Nix the package manager uses a purely functional language - which is also called Nix - to define packages.

[Nixpkgs](https://github.com/nixos/nixpkgs) (the main source of packages) are contained in a single GitHub repository. You can also define your own packages in the same language and then easily include them in your config.

Nix is a source-based package manager; if there’s no pre-built available in the binary cache, Nix will just build the package from source using its definition. It builds each package in a sandboxed *pure* environment, which is as independent of the host system as possible, thus making binaries reproducible.

## Distribuciones Enfocadas en el Anonimato

### Whonix

<div class="admonition recommendation" markdown>

![Whonix logo](assets/img/linux-desktop/whonix.svg){ align=right }

**Whonix** está basado en [Kicksecure](#kicksecure), una bifurcación de Debian centrada en la seguridad. Su objetivo es proporcionar privacidad, seguridad y anonimato en Internet. Whonix se utiliza mejor junto con [Qubes OS](#qubes-os).

[:octicons-home-16: Página principal](https://www.whonix.org/){ .md-button .md-button--primary }
[:simple-torbrowser:](http://www.dds6qkxpwdeubwucdiaord2xgbbeyds25rbsgr73tbfpqpt4a6vjwsyd.onion){ .card-link title="Servicio Onion" }
[:octicons-info-16:](https://www.whonix.org/wiki/Documentation){ .card-link title=Documentación}
[:octicons-heart-16:](https://www.whonix.org/wiki/Donate){ .card-link title=Contribuir }

</details>

</div>

Whonix is meant to run as two virtual machines: a “Workstation” and a Tor “Gateway.” All communications from the Workstation must go through the Tor gateway. This means that even if the Workstation is compromised by malware of some kind, the true IP address remains hidden.

Some of its features include Tor Stream Isolation, [keystroke anonymization](https://www.whonix.org/wiki/Keystroke_Deanonymization#Kloak), [encrypted swap](https://github.com/Whonix/swap-file-creator), and a hardened memory allocator. Future versions of Whonix will likely include [full system AppArmor policies](https://github.com/Whonix/apparmor-profile-everything) and a [sandbox app launcher](https://www.whonix.org/wiki/Sandbox-app-launcher) to fully confine all processes on the system.

Whonix is best used [in conjunction with Qubes](https://www.whonix.org/wiki/Qubes/Why_use_Qubes_over_other_Virtualizers). We have a [recommended guide](os/qubes-overview.md#connecting-to-tor-via-a-vpn) on configuring Whonix in conjunction with a VPN ProxyVM in Qubes to hide your Tor activities from your ISP.

### Tails

<div class="admonition recommendation" markdown>

![Tails logo](assets/img/linux-desktop/tails.svg){ align=right }

**Tails** es un sistema operativo basado en Debian que enruta todas las comunicaciones a través de Tor, y que puede arrancar en casi cualquier ordenador desde un DVD, una memoria USB o una tarjeta SD. Utiliza [Tor](tor.md) para preservar la privacidad y el anonimato a la vez que elude la censura, y no deja rastro de sí mismo en el ordenador en el que se utiliza una vez apagado.

[:octicons-home-16: Página Principal](https://tails.boum.org/){ .md-button .md-button--primary }
[:octicons-info-16:](https://tails.boum.org/doc/index.en.html){ .card-link title=Documentación}
[:octicons-heart-16:](https://tails.boum.org/donate/){ .card-link title=Contribuir }

</details>

</div>

Tails is great for counter forensics due to amnesia (meaning nothing is written to the disk); however, it is not a hardened distribution like Whonix. It lacks many anonymity and security features that Whonix has and gets updated much less often (only once every six weeks). A Tails system that is compromised by malware may potentially bypass the transparent proxy allowing for the user to be deanonymized.

Tails includes [uBlock Origin](desktop-browsers.md#ublock-origin) in Tor Browser by default, which may potentially make it easier for adversaries to fingerprint Tails users. [Whonix](desktop.md#whonix) virtual machines may be more leak-proof, however they are not amnesic, meaning data may be recovered from your storage device.

By design, Tails is meant to completely reset itself after each reboot. Encrypted [persistent storage](https://tails.boum.org/doc/persistent_storage/index.en.html) can be configured to store some data between reboots.

## Distribuciones Enfocadas en la Seguridad

### Qubes OS

<div class="admonition recommendation" markdown>

![Qubes OS logo](assets/img/qubes/qubes_os.svg){ align=right }

**Qubes OS** es un sistema operativo de código abierto diseñado para proporcionar una fuerte seguridad para la informática de escritorio a través de máquinas virtuales seguras (o "qubes"). Qubes se basa en Xen, el Sistema de Ventanas X y Linux. Puede ejecutar la mayoría de las aplicaciones Linux y utilizar la mayoría de los controladores Linux.

[:octicons-home-16: Página Principal](https://www.qubes-os.org/){ .md-button .md-button--primary }
[:simple-torbrowser:](http://qubesosfasa4zl44o4tws22di6kepyzfeqv3tg4e3ztknltfxqrymdad.onion){ .card-link title="Servicio Onion" }
[:octicons-eye-16:](https://www.qubes-os.org/privacy/){ .card-link title="Politica de Privacidad" }
[:octicons-info-16:](https://www.qubes-os.org/doc/){ .card-link title=Documentación }
[:octicons-code-16:](https://github.com/QubesOS/){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://www.qubes-os.org/donate/){ .card-link title=Contribuir }

</details>

</div>

Qubes OS secures the computer by isolating subsystems (e.g., networking, USB, etc.) and applications in separate *qubes*. Should one part of the system be compromised, the extra isolation is likely to protect the rest of the *qubes* and the core system.

For further information about how Qubes works, read our full [Qubes OS overview](os/qubes-overview.md) page.

### Kicksecure

While we [recommend against](os/linux-overview.md#release-cycle) "perpetually outdated" distributions like Debian for Desktop use in most cases, Kicksecure is a Debian-based operating system which has been hardened to be much more than a typical Linux install.

<div class="admonition recommendation" markdown>

![Kicksecure logo](assets/img/linux-desktop/kicksecure.svg){ align=right }

**Kicksecure** -en términos muy simplificados- es un conjunto de scripts, configuraciones y paquetes que reducen sustancialmente la superficie de ataque de Debian. Cubre muchas recomendaciones de privacidad y seguridad por defecto. También sirve de sistema operativo base para [Whonix](#whonix).

[:octicons-home-16: Página Principal](https://www.kicksecure.com/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://www.kicksecure.com/wiki/Privacy_Policy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://www.kicksecure.com/wiki/Documentation){ .card-link title=Documentación}
[:octicons-code-16:](https://github.com/Kicksecure){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://www.kicksecure.com/wiki/Donate){ .card-link title=Contribuir }

</details>

</div>

## Criterios

Choosing a Linux distro that is right for you will come down to a huge variety of personal preferences, and this page is **not** meant to be an exhaustive list of every viable distribution. Our Linux overview page has some advice on [choosing a distro](os/linux-overview.md#choosing-your-distribution) in more detail. The distros on *this* page do all generally follow the guidelines we covered there, and all meet these standards:

- Gratis y de código abierto.
- Recibe actualizaciones periódicas del software y del kernel.
- [Evita X11](os/linux-overview.md#wayland).
    - La excepción notable aquí es Qubes, pero los problemas de aislamiento que X11 suele tener se evitan con la virtualización. Este aislamiento sólo se aplica a las aplicaciones *que se ejecutan en qubes diferentes* (máquinas virtuales), las aplicaciones que se ejecutan en el *mismo* qube no están protegidas entre sí.
- Admite el cifrado de disco completo durante la instalación.
- No congela las publicaciones periódicas durante más de 1 año.
    - Nosotros [no recomendamos](os/linux-overview.md#release-cycle) distribuciones "Long Term Support (Soporte a Largo Plazo)" o "stable (estable)" para uso de escritorio.
- Es compatible con una amplia variedad de hardware.
- Preferencia hacia proyectos más grandes.
    - Mantener un sistema operativo es un gran reto, y los proyectos más pequeños tienden a cometer más errores evitables o a retrasar las actualizaciones críticas (o peor aún, a desaparecer por completo). Nos inclinamos por proyectos que probablemente seguirán existiendo dentro de 10 años (ya sea gracias al respaldo de empresas o a un apoyo muy significativo de la comunidad), y nos alejamos de los proyectos construidos a mano o con un número reducido de mantenedores.

In addition, [our standard criteria](about/criteria.md) for recommended projects still applies. **Please note we are not affiliated with any of the projects we recommend.**
