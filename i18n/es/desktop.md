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

![Fedora logo](assets/img/linux-desktop/fedora.svg){ align=right }

**Fedora Workstation** es nuestra distribución recomendada para la gente nueva en Linux. Fedora generally adopts newer technologies (e.g., [Wayland](https://wayland.freedesktop.org) and [PipeWire](https://pipewire.org)) before other distributions. Estas nuevas tecnologías suelen venir acompañadas de mejoras en la seguridad, la privacidad y la usabilidad en general.

[:octicons-home-16: Página principal](https://fedoraproject.org/workstation){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.fedoraproject.org/en-US/docs){ .card-link title=Documentación}
[:octicons-heart-16:](https://whatcanidoforfedora.org){ .card-link title=Contribuir}

</details>

</div>

Fedora tiene un ciclo de lanzamientos semicontinuo. Mientras algunos paquetes como [GNOME](https://gnome.org) son congelados hasta el próximo lanzamiento de Fedora, la mayoría de los paquetes (incluyendo el kernel) son actualizados con frecuencia a través del ciclo de vida del lanzamiento. Cada versión de Fedora recibe soporte durante un año, con una nueva versión cada 6 meses.

### openSUSE Tumbleweed

<div class="admonition recommendation" markdown>

![openSUSE Tumbleweed logo](assets/img/linux-desktop/opensuse-tumbleweed.svg){ align=right }

**openSUSE Tumbleweed** es una distribución estable con actualización continua.

openSUSE Tumbleweed uses [Btrfs](https://en.wikipedia.org/wiki/Btrfs) and [Snapper](https://en.opensuse.org/openSUSE:Snapper_Tutorial) to ensure that snapshots can be rolled back should there be a problem.

[:octicons-home-16: Página principal](https://get.opensuse.org/tumbleweed){ .md-button .md-button--primary }
[:octicons-info-16:](https://doc.opensuse.org){ .card-link title=Documentación}
[:octicons-heart-16:](https://shop.opensuse.org){ .card-link title=Contribuir}

</details>

</div>

Tumbleweed sigue un modelo de actualización continua en el que cada actualización se publica como una copia instantánea de la distribución. Al actualizar el sistema, se descarga una nueva copia instantánea. Cada copia instantánea es sometida a una serie de pruebas automatizadas por [openQA](https://openqa.opensuse.org) para garantizar su calidad.

### Arch Linux

<div class="admonition recommendation" markdown>

![Arch logo](assets/img/linux-desktop/archlinux.svg){ align=right }

**Arch Linux** is a lightweight, do-it-yourself (DIY) distribution, meaning that you only get what you install. Para obtener más información, consulte su [FAQ](https://wiki.archlinux.org/title/Frequently_asked_questions).

[:octicons-home-16: Página Principal](https://archlinux.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://wiki.archlinux.org){ .card-link title=Documentación}
[:octicons-heart-16:](https://archlinux.org/donate){ .card-link title=Contribuir }

</details>

</div>

Arch Linux tiene un ciclo de actualización continuo. No existe un calendario fijo de lanzamientos y los paquetes se actualizan con mucha frecuencia.

Al ser una distribución DIY, se espera que usted [configure y mantenga](os/linux-overview.md#arch-based-distributions) su sistema por su cuenta. Arch dispone de un [instalador oficial](https://wiki.archlinux.org/title/Archinstall) para facilitar el proceso de instalación.

Gran parte de los [paquetes de Arch Linux](https://reproducible.archlinux.org) son [reproducibles](https://reproducible-builds.org).

## Distribuciones Atómicas

**Las distribuciones atómicas** (a veces también denominadas **distribuciones inmutables**) son sistemas operativos que gestionan la instalación y actualización de paquetes superponiendo cambios sobre la imagen central del sistema, en lugar de modificarlo directamente. Advantages of atomic distros include increased stability and the ability to easily roll back updates. Consulte [*Actualizaciones tradicionales vs. Atómicas*](os/linux-overview.md#traditional-vs-atomic-updates) para obtener más información.

### Fedora Atomic Desktops

<div class="admonition recommendation" markdown>

![Fedora logo](assets/img/linux-desktop/fedora.svg){ align=right }

**Fedora Atomic Desktops** son variantes de Fedora que utilizan el gestor de paquetes `rpm-ostree` y se centran principalmente en flujos de trabajo en contenedores y Flatpak para aplicaciones de escritorio. Todas estas variantes siguen el mismo calendario de lanzamientos que Fedora Workstation, beneficiándose de las mismas actualizaciones rápidas y manteniéndose muy cerca del upstream.

[:octicons-home-16: Homepage](https://fedoraproject.org/atomic-desktops){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.fedoraproject.org/en-US/emerging){ .card-link title=Documentation}
[:octicons-heart-16:](https://whatcanidoforfedora.org){ .card-link title=Contribute }

</details>

</div>

[Fedora Atomic Desktops](https://fedoramagazine.org/introducing-fedora-atomic-desktops) come in a variety of flavors depending on the desktop environment you prefer. As with the recommendation to avoid X11 in our [criteria](#criteria) for Linux distributions, we recommend avoiding flavors that support only the legacy X11 window system.

Estos sistemas operativos difieren de Fedora Workstation en que sustituyen el gestor de paquetes [DNF](https://docs.fedoraproject.org/en-US/quick-docs/dnf) por una alternativa mucho más avanzada denominada [`rpm-ostree`](https://docs.fedoraproject.org/en-US/fedora/latest/system-administrators-guide/package-management/rpm-ostree). El gestor de paquetes `rpm-ostree` funciona descargando una imagen base para el sistema, y luego superponiendo paquetes sobre ella en un árbol de commit [git](https://en.wikipedia.org/wiki/Git)-like. Cuando se actualice el sistema, se descargará una nueva imagen base y las superposiciones se aplicarán a esa nueva imagen.

After the update is complete, you will reboot the system into the new deployment. `rpm-ostree` keeps two deployments of the system so that you can easily roll back if something breaks in the new deployment. También existe la opción de anclar más implementaciones según sea necesario.

[Flatpak](https://flatpak.org) es el método principal de instalación de paquetes en estas distribuciones, ya que `rpm-ostree` solo está pensado para superponer paquetes que no pueden permanecer dentro de un contenedor sobre la imagen base.

As an alternative to Flatpaks, there is the option of [Toolbx](https://docs.fedoraproject.org/en-US/fedora-silverblue/toolbox) to create [Podman](https://podman.io) containers which mimic a traditional Fedora environment, a [useful feature](https://containertoolbx.org) for the discerning developer. These containers share a home directory with the host operating system.

### NixOS

<div class="admonition recommendation" markdown>

![NixOS logo](assets/img/linux-desktop/nixos.svg){ align=right }

NixOS es una distribución independiente basada en el gestor de paquetes Nix y centrada en la reproducibilidad y la fiabilidad.

[:octicons-home-16: Página Principal](https://nixos.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://nixos.org/learn.html){ .card-link title=Documentación}
[:octicons-heart-16:](https://nixos.org/donate.html){ .card-link title=Contribuir }

</details>

</div>

El gestor de paquetes de NixOS guarda cada versión de cada paquete en una carpeta diferente del almacén **Nix**. Debido a esto, puedes tener diferentes versiones del mismo paquete instalado en tu sistema. Después de escribir el contenido del paquete en la carpeta, esta pasa a ser de solo lectura.

NixOS also provides atomic updates. It first downloads (or builds) the packages and files for the new system generation and then switches to it. There are different ways to switch to a new generation: you can tell NixOS to activate it after reboot or you can switch to it at runtime. También puedes *probar* la nueva generación cambiando a ella durante el tiempo de ejecución, pero sin establecerla como la generación actual del sistema. Si algo en el proceso de actualización se rompe, puedes simplemente reiniciar y automáticamente volver a una versión de trabajo de tu sistema.

The Nix package manager uses a purely functional language—which is also called Nix—to define packages.

[Nixpkgs](https://github.com/nixos/nixpkgs) (la fuente principal de paquetes) se encuentra en un único repositorio de GitHub. También puedes definir tus propios paquetes en el mismo idioma e incluirlos fácilmente en tu configuración.

Nix es un gestor de paquetes basado en el código fuente; si no hay ningún paquete preconstruido disponible en la caché de binarios, Nix simplemente construirá el paquete desde el código fuente usando su definición. It builds each package in a sandboxed *pure* environment, which is as independent of the host system as possible. Binaries built with this method are reproducible, which can be useful as a safeguard against [:material-package-variant-closed-remove: Supply Chain Attacks](basics/common-threats.md#attacks-against-certain-organizations ""){.pg-viridian}.

## Distribuciones Enfocadas en el Anonimato

### Whonix

<div class="admonition recommendation" markdown>

![Whonix logo](assets/img/linux-desktop/whonix.svg){ align=right }

**Whonix** está basado en [Kicksecure](#kicksecure), una bifurcación de Debian centrada en la seguridad. Su objetivo es proporcionar privacidad, seguridad y anonimato en Internet. Whonix se utiliza mejor junto con [Qubes OS](#qubes-os).

[:octicons-home-16: Página Principal](https://whonix.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://dds6qkxpwdeubwucdiaord2xgbbeyds25rbsgr73tbfpqpt4a6vjwsyd.onion){ .card-link title="Servicio Onion" }
[:octicons-info-16:](https://whonix.org/wiki/Documentation){ .card-link title=Documentación}
[:octicons-heart-16:](https://whonix.org/wiki/Donate){ .card-link title=Contribuir }

</details>

</div>

Whonix está pensado para funcionar como dos máquinas virtuales: una "Estación de Trabajo" y una "Puerta de Enlace" Tor. Todas las comunicaciones desde la Estación de Trabajo deben pasar por la puerta de enlace Tor. Esto significa que incluso si la Estación de Trabajo se ve comprometida por algún tipo de malware, la verdadera dirección IP permanecerá oculta.

Algunas de sus características incluyen Tor Stream Isolation, [anonimización de pulsaciones de teclas](https://whonix.org/wiki/Keystroke_Deanonymization#Kloak), [swap encriptado](https://github.com/Whonix/swap-file-creator) y un asignador de memoria endurecido. Future versions of Whonix will likely include [full system AppArmor policies](https://github.com/roddhjav/apparmor.d) and a [sandboxed app launcher](https://whonix.org/wiki/Sandbox-app-launcher) to fully confine all processes on the system.

Whonix se utiliza mejor [junto con Qubes](https://whonix.org/wiki/Qubes/Why_use_Qubes_over_other_Virtualizers). Tenemos una [guía recomendada](os/qubes-overview.md#connecting-to-tor-via-a-vpn) sobre la configuración de Whonix junto con una VPN ProxyVM en Qubes para ocultar tus actividades Tor de tu ISP.

### Tails

<div class="admonition recommendation" markdown>

![Tails logo](assets/img/linux-desktop/tails.svg){ align=right }

**Tails** es un sistema operativo basado en Debian que enruta todas las comunicaciones a través de Tor, y que puede arrancar en casi cualquier ordenador desde un DVD, una memoria USB o una tarjeta SD. Utiliza [Tor](tor.md) para preservar la privacidad y el anonimato a la vez que elude la censura, y no deja rastro de sí mismo en el ordenador en el que se utiliza una vez apagado.

[:octicons-home-16: Página Principal](https://tails.net){ .md-button .md-button--primary }
[:octicons-info-16:](https://tails.net/doc/index.en.html){ .card-link title=Documentación}
[:octicons-heart-16:](https://tails.net/donate){ .card-link title=Contribuir }

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

Tails [no borra](https://gitlab.tails.boum.org/tails/tails/-/issues/5356) la [memoria de vídeo](https://en.wikipedia.org/wiki/Dual-ported_video_RAM) al apagar. Cuando reinicie el ordenador después de usar Tails, puede que aparezca brevemente la última pantalla que se mostró en Tails. Si apaga el ordenador en lugar de reiniciarlo, la memoria de vídeo se borrará automáticamente después de estar un tiempo sin alimentación.

</div>

Tails es genial contra el análisis forense debido a la amnesia (lo que significa que no se escribe nada en el disco); sin embargo, no es una distribución endurecida como Whonix. Carece de muchas de las funciones de anonimato y seguridad que tiene Whonix y se actualiza con mucha menos frecuencia (solo una vez cada seis semanas). A Tails system that is compromised by malware may potentially bypass the transparent proxy, allowing for the user to be deanonymized.

Tails includes [uBlock Origin](browser-extensions.md#ublock-origin) in Tor Browser by default, which may potentially make it easier for adversaries to fingerprint Tails users. Las máquinas virtuales de [Whonix](desktop.md#whonix) pueden ser más a prueba de fugas, sin embargo no son amnésicas, lo que significa que los datos pueden ser recuperados de su dispositivo de almacenamiento.

Tails está diseñado para formatearse por completo después de cada reinicio. El [almacenamiento persistente](https://tails.net/doc/persistent_storage/index.en.html) cifrado puede configurarse para almacenar algunos datos entre reinicios.

## Distribuciones Enfocadas en la Seguridad

### Qubes OS

<div class="admonition recommendation" markdown>

![Qubes OS logo](assets/img/qubes/qubes_os.svg){ align=right }

**Qubes OS** es un sistema operativo de código abierto diseñado para proporcionar una fuerte seguridad para la informática de escritorio a través de máquinas virtuales seguras (o "qubes"). Qubes se basa en Xen, el Sistema de Ventanas X y Linux. Puede ejecutar la mayoría de las aplicaciones Linux y utilizar la mayoría de los controladores Linux.

[:octicons-home-16: Página Principal](https://qubes-os.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://qubesosfasa4zl44o4tws22di6kepyzfeqv3tg4e3ztknltfxqrymdad.onion){ .card-link title="Servicio Onion" }
[:octicons-eye-16:](https://qubes-os.org/privacy){ .card-link title="Politica de Privacidad" }
[:octicons-info-16:](https://qubes-os.org/doc){ .card-link title=Documentación }
[:octicons-code-16:](https://github.com/QubesOS){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://qubes-os.org/donate){ .card-link title=Contribuir }

</details>

</div>

Qubes OS asegura el ordenador aislando subsistemas (por ejemplo, redes, USB, etc.) y aplicaciones en *qubes*separadas. En caso de que una parte del sistema se vea comprometida, es probable que el aislamiento adicional proteja el resto de *qubes* y el sistema central.

Para más información sobre el funcionamiento de Qubes, consulta nuestra página [Qubes OS overview](os/qubes-overview.md).

### Kicksecure

While we [recommend against](os/linux-overview.md#release-cycle) "perpetually outdated" distributions like Debian for desktop use in most cases, Kicksecure is a Debian-based operating system which has been hardened to be much more than a typical Linux install.

<div class="admonition recommendation" markdown>

![Kicksecure logo](assets/img/linux-desktop/kicksecure.svg){ align=right }

**Kicksecure** -en términos muy simplificados- es un conjunto de scripts, configuraciones y paquetes que reducen sustancialmente la superficie de ataque de Debian. Cubre muchas recomendaciones de privacidad y seguridad por defecto. También sirve de sistema operativo base para [Whonix](#whonix).

[:octicons-home-16: Página Principal](https://kicksecure.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://kicksecure.com/wiki/Privacy_Policy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://kicksecure.com/wiki/Documentation){ .card-link title=Documentación }
[:octicons-code-16:](https://github.com/Kicksecure){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://kicksecure.com/wiki/Donate){ .card-link title=Contribuir }

</details>

</div>

## Criterios

La elección de una distribución Linux adecuada para ti dependerá de una gran variedad de preferencias personales, y esta página **no** pretende ser una lista exhaustiva de todas las distribuciones viables. En nuestra página de información general sobre Linux encontrarás algunos consejos sobre [elegir una distribución](os/linux-overview.md#choosing-your-distribution) con más detalle. Todas las distribuciones que se encuentran en *esta* página siguen, en general, las directrices que cubrimos allí, y todas cumplen estas normas:

- Gratis y de código abierto.
- Recibe actualizaciones periódicas del software y del kernel.
- Avoids X11, as its last major release was [more than a decade](https://x.org/wiki/Releases) ago.
    - The notable exception here is Qubes, but the [isolation issues](https://blog.invisiblethings.org/2011/04/23/linux-security-circus-on-gui-isolation) which X11 typically has are avoided by virtualization. This isolation only applies to apps *running in different qubes* (virtual machines); apps running in the *same* qube are not protected from each other.
- Admite el cifrado de disco completo durante la instalación.
- No congela las publicaciones periódicas durante más de 1 año.
    - Nosotros [no recomendamos](os/linux-overview.md#release-cycle) distribuciones "Long Term Support (Soporte a Largo Plazo)" o "stable (estable)" para uso de escritorio.
- Es compatible con una amplia variedad de hardware.
- Preferencia hacia proyectos más grandes.
    - Mantener un sistema operativo es un gran reto, y los proyectos más pequeños tienden a cometer más errores evitables o a retrasar las actualizaciones críticas (o peor aún, a desaparecer por completo). Nos inclinamos por proyectos que probablemente seguirán existiendo dentro de 10 años (ya sea gracias al respaldo de empresas o a un apoyo muy significativo de la comunidad), y nos alejamos de los proyectos construidos a mano o con un número reducido de mantenedores.

Además, [nuestros criterios estándar](about/criteria.md) para los proyectos recomendados se siguen aplicando. **Ten en cuenta que no estamos afiliados a ninguno de los proveedores que recomendamos.**
