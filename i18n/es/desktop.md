---
title: "Escritorio/PC"
icon: simple/linux
description: Las distribuciones de Linux se recomiendan comúnmente para la protección de la privacidad y la libertad del software.
cover: desktop.png
---

Las distribuciones de Linux se recomiendan comúnmente para la protección de la privacidad y la libertad del software. Si aún no utiliza Linux, a continuación le sugerimos que pruebe algunas distribuciones, así como algunos consejos generales para mejorar la privacidad y la seguridad que son aplicables a muchas distribuciones de Linux.

- [Vista General de Linux :material-arrow-right-drop-circle:](os/linux-overview.md)

## Distribuciones Tradicionales

### Fedora Workstation

!!! recommendation

    ![Fedora logo](assets/img/linux-desktop/fedora-workstation.svg){ align=right }
    
    **Fedora Workstation** es nuestra distribución recomendada para la gente nueva en Linux. Fedora suele adoptar tecnologías más recientes antes que otras distribuciones, por ejemplo, [Wayland](https://wayland.freedesktop.org/), [PipeWire](https://pipewire.org). Estas nuevas tecnologías suelen venir acompañadas de mejoras en la seguridad, la privacidad y la usabilidad en general.
    
    [:octicons-home-16: Página Principal](https://getfedora.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://docs.fedoraproject.org/en-US/docs/){ .card-link title=Documentación}
    [:octicons-heart-16:](https://whatcanidoforfedora.org/){ .card-link title=Contribuir}

Fedora tiene un ciclo de lanzamientos semicontinuo. Mientras que algunos paquetes como [GNOME](https://www.gnome.org) quedan congelados hasta la siguiente versión de Fedora, la mayoría de los paquetes (incluido el kernel) se actualizan con frecuencia durante toda la vida útil de la versión. Cada versión de Fedora recibe soporte durante un año, con una nueva versión cada 6 meses.

### openSUSE Tumbleweed

!!! recommendation

    ![openSUSE Tumbleweed logo](assets/img/linux-desktop/opensuse-tumbleweed.svg){ align=right }
    
    **openSUSE Tumbleweed** es una distribución estable con actualización continua.
    
    openSUSE Tumbleweed cuenta con un sistema de [actualización transaccional](https://kubic.opensuse.org/blog/2018-04-04-transactionalupdates/) que utiliza [Btrfs](https://en.wikipedia.org/wiki/Btrfs) y [Snapper](https://en.opensuse.org/openSUSE:Snapper_Tutorial) para garantizar que las copias instantáneas se puedan revertir en caso de que haya algún problema.
    
    [:octicons-home-16: Página Principal](https://get.opensuse.org/tumbleweed/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://doc.opensuse.org/){ .card-link title=Documentación}
    [:octicons-heart-16:](https://shop.opensuse.org/){ .card-link title=Contribuir }

Tumbleweed sigue un modelo de actualización continua en el que cada actualización se publica como una copia instantánea de la distribución. Al actualizar el sistema, se descarga una nueva copia instantánea. Cada copia instantánea es sometida a una serie de pruebas automatizadas por [openQA](https://openqa.opensuse.org) para garantizar su calidad.

### Arch Linux

!!! recommendation

    ![Arch logo](assets/img/linux-desktop/archlinux.svg){ align=right }
    
    **Arch Linux** es una distribución ligera del estilo "hágalo usted mismo" (DIY), lo que significa que sólo obtiene lo que instala. Para obtener más información, consulte su [FAQ](https://wiki.archlinux.org/title/Frequently_asked_questions).
    
    [:octicons-home-16: Página Principal](https://archlinux.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://wiki.archlinux.org/){ .card-link title=Documentación}
    [:octicons-heart-16:](https://archlinux.org/donate/){ .card-link title=Contribuir }

Arch Linux tiene un ciclo de actualización continuo. No existe un calendario fijo de lanzamientos y los paquetes se actualizan con mucha frecuencia.

Al ser una distribución DIY, se espera que usted [configure y mantenga](os/linux-overview.md#arch-based-distributions) su sistema por su cuenta. Arch dispone de un [instalador oficial](https://wiki.archlinux.org/title/Archinstall) para facilitar el proceso de instalación.

Gran parte de los [paquetes de Arch Linux](https://reproducible.archlinux.org) son [reproducibles](https://reproducible-builds.org).

## Distribuciones Inmutables

### Fedora Silverblue

!!! recommendation

    ![Fedora Silverblue logo](assets/img/linux-desktop/fedora-silverblue.svg){ align=right }
    
    **Fedora Silverblue** y **Fedora Kinoite** son variantes inmutables de Fedora con un fuerte enfoque en los flujos de trabajo en contenedores. Silverblue viene con el entorno de escritorio [GNOME](https://www.gnome.org/) mientras que Kinoite viene con [KDE](https://kde.org/). Silverblue y Kinoite siguen el mismo calendario de lanzamientos que Fedora Workstation, beneficiándose de las mismas actualizaciones rápidas y manteniéndose muy cerca del upstream.
    
    [:octicons-home-16: Página Principal](https://silverblue.fedoraproject.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://docs.fedoraproject.org/en-US/fedora-silverblue/){ .card-link title=Documentación}
    [:octicons-heart-16:](https://whatcanidoforfedora.org/){ .card-link title=Contribuir }

Silverblue (y Kinoite) difieren de Fedora Workstation en que sustituyen el gestor de paquetes [DNF](https://fedoraproject.org/wiki/DNF) por una alternativa mucho más avanzada llamada [`rpm-ostree`](https://docs.fedoraproject.org/en-US/fedora/rawhide/system-administrators-guide/package-management/rpm-ostree/). El gestor de paquetes `rpm-ostree` funciona descargando una imagen base para el sistema, y luego superponiendo paquetes sobre ella en un árbol de commit como el de [git](https://es.wikipedia.org/wiki/Git). Cuando se actualice el sistema, se descargará una nueva imagen de base y las superposiciones se aplicarán a esa nueva imagen.

Una vez completada la actualización, se reiniciará el sistema con la nueva implementación. `rpm-ostree` mantiene dos implementaciones del sistema para que pueda revertir fácilmente si algo se rompe en la nueva implementación. También existe la opción de anclar más implementaciones según sea necesario.

[Flatpak](https://www.flatpak.org) es el método principal de instalación de paquetes en estas distribuciones, ya que `rpm-ostree` sólo está pensado para superponer paquetes que no pueden permanecer dentro de un contenedor sobre la imagen base.

Como alternativa a Flatpaks, existe la opción de [Toolbox](https://docs.fedoraproject.org/en-US/fedora-silverblue/toolbox/) para crear contenedores [Podman](https://podman.io) con un directorio raíz compartido con el sistema operativo anfitrión e imitar un entorno Fedora tradicional, lo cual es una [característica útil](https://containertoolbx.org) para el desarrollador exigente.

### NixOS

!!! recommendation

    ![NixOS logo](assets/img/linux-desktop/nixos.svg){ align=right }
    
    NixOS es una distribución independiente basada en el gestor de paquetes Nix y centrada en la reproducibilidad y la fiabilidad.
    
    [:octicons-home-16: Página Principal](https://nixos.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://nixos.org/learn.html){ .card-link title=Documentación}
    [:octicons-heart-16:](https://nixos.org/donate.html){ .card-link title=Contribuir }

El gestor de paquetes de NixOS guarda cada versión de cada paquete en una carpeta diferente del **almacén Nix**. Debido a esto, puede tener diferentes versiones del mismo paquete instalado en su sistema. Después de escribir el contenido del paquete en la carpeta, ésta pasa a ser de sólo lectura.

NixOS también proporciona actualizaciones atómicas; primero descarga (o construye) los paquetes y archivos para la nueva generación del sistema y luego cambia a ella. Hay diferentes maneras de cambiar a una nueva generación; puede decirle a NixOS que la active después de reiniciar o puede cambiar a ella durante el tiempo de ejecución. También puede *probar* la nueva generación cambiando a ella durante el tiempo de ejecución, pero sin establecerla como la generación actual del sistema. Si algo en el proceso de actualización se rompe, puede simplemente reiniciar y automáticamente y volver a una versión que funcione de su sistema.

El gestor de paquetes Nix utiliza un lenguaje puramente funcional -que también se llama Nix- para definir paquetes.

[Nixpkgs](https://github.com/nixos/nixpkgs) (la fuente principal de paquetes) se encuentra en un único repositorio de GitHub. También puede definir sus propios paquetes en el mismo idioma e incluirlos fácilmente en su configuración.

Nix es un gestor de paquetes basado en el código fuente; si no hay ningún paquete preconstruido disponible en la caché de binarios, Nix simplemente construirá el paquete desde el código fuente usando su definición. Construye cada paquete en un entorno aislado *puro*, que es lo más independiente posible del sistema anfitrión, lo que hace que los binarios sean reproducibles.

## Distribuciones Enfocadas en el Anonimato

### Whonix

!!! recommendation

    ![Whonix logo](assets/img/linux-desktop/whonix.svg){ align=right }
    
    **Whonix** is based on [Kicksecure](#kicksecure), a security-focused fork of Debian. Su objetivo es proporcionar privacidad, seguridad y anonimato en Internet. Whonix se utiliza mejor junto con [Qubes OS](#qubes-os).
    
    [:octicons-home-16: Página principal](https://www.whonix.org/){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://www.dds6qkxpwdeubwucdiaord2xgbbeyds25rbsgr73tbfpqpt4a6vjwsyd.onion){ .card-link title="Servicio Onion" }
    [:octicons-info-16:](https://www.whonix.org/wiki/Documentation){ .card-link title=Documentación}
    [:octicons-heart-16:](https://www.whonix.org/wiki/Donate){ .card-link title=Contribuir }

Whonix está pensado para funcionar como dos máquinas virtuales: una "Estación de Trabajo" y una "Puerta de Enlace" Tor. Todas las comunicaciones desde la Estación de Trabajo deben pasar por la puerta de enlace Tor. Esto significa que incluso si la Estación de Trabajo se ve comprometida por algún tipo de malware, la verdadera dirección IP permanece oculta.

Algunas de sus características incluyen Tor Stream Isolation, [anonimización de pulsaciones](https://www.whonix.org/wiki/Keystroke_Deanonymization#Kloak), [swap encriptado ](https://github.com/Whonix/swap-file-creator), y un asignador de memoria endurecido.

Las futuras versiones de Whonix probablemente incluirán [políticas AppArmor para todo el sistema](https://github.com/Whonix/apparmor-profile-everything) y un lanzador de aplicaciones en entorno aislado [](https://www.whonix.org/wiki/Sandbox-app-launcher) para confinar completamente todos los procesos del sistema.

Whonix se utiliza mejor [junto con Qubes](https://www.whonix.org/wiki/Qubes/Why_use_Qubes_over_other_Virtualizers), Qubes-Whonix tiene varias [desventajas](https://forums.whonix.org/t/qubes-whonix-security-disadvantages-help-wanted/8581) cuando se compara con otros hipervisores.

### Tails

!!! recommendation

    ![Tails logo](assets/img/linux-desktop/tails.svg){ align=right }
    
    **Tails** es un sistema operativo basado en Debian que enruta todas las comunicaciones a través de Tor, y que puede arrancar en casi cualquier ordenador desde un DVD, una memoria USB o una tarjeta SD. Utiliza [Tor](tor.md) para preservar la privacidad y el anonimato a la vez que elude la censura, y no deja rastro de sí mismo en el ordenador en el que se utiliza una vez apagado.
    
    [:octicons-home-16: Página Principal](https://tails.boum.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://tails.boum.org/doc/index.en.html){ .card-link title=Documentación}
    [:octicons-heart-16:](https://tails.boum.org/donate/){ .card-link title=Contribuir }

Tails es genial contra el análisis forense debido a la amnesia (lo que significa que no se escribe nada en el disco); sin embargo, no es una distribución endurecida como Whonix. Carece de muchas de las funciones de anonimato y seguridad que tiene Whonix y se actualiza con mucha menos frecuencia (sólo una vez cada seis semanas). Un sistema Tails comprometido por malware puede potencialmente eludir el proxy transparente permitiendo que el usuario sea desanonimizado.

Tails incluye [uBlock Origin](desktop-browsers.md#ublock-origin) en el Navegador Tor por defecto, lo que potencialmente puede facilitar a los adversarios la toma de huellas digitales de los usuarios de Tails. Las máquinas virtualesd de [Whonix](desktop.md#whonix) pueden ser más a prueba de fugas, sin embargo no son amnésicas, lo que significa que los datos pueden ser recuperados de su dispositivo de almacenamiento.

Tails está diseñado para formatearse por completo después de cada reinicio. [El almacenamiento persistente](https://tails.boum.org/doc/persistent_storage/index.en.html) cifrado puede configurarse para almacenar algunos datos entre reinicios.

## Distribuciones Enfocadas en la Seguridad

### Qubes OS

!!! recommendation

    ![Qubes OS logo](assets/img/qubes/qubes_os.svg){ align=right }
    
    **Qubes OS** is an open-source operating system designed to provide strong security for desktop computing through secure virtual machines (a.k.a. "Qubes"). Qubes se basa en Xen, el Sistema de Ventanas X y Linux, y puede ejecutar la mayoría de las aplicaciones Linux y utilizar la mayoría de los controladores de Linux.
    
    [:octicons-home-16: Homepage](https://www.qubes-os.org/){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://qubesosfasa4zl44o4tws22di6kepyzfeqv3tg4e3ztknltfxqrymdad.onion){ .card-link title="Onion Service" }
    [:octicons-eye-16:](https://www.qubes-os.org/privacy/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://www.qubes-os.org/doc/){ .card-link title=Documentation }
    [:octicons-code-16:](https://github.com/QubesOS/){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://www.qubes-os.org/donate/){ .card-link title=Contribute }

Qubes OS secures the computer by isolating subsystems (e.g., networking, USB, etc.) and applications in separate VMs. Should one part of the system be compromised, the extra isolation is likely to protect the rest of the system.

For further information about how Qubes works, read our full [Qubes OS overview](os/qubes-overview.md) page.

### Kicksecure

While we [recommend against](os/linux-overview.md#release-cycle) "perpetually outdated" distributions like Debian for Desktop use in most cases, Kicksecure is a Debian-based operating system which has been hardened to be much more than a typical Linux install.

!!! recommendation

    ![Kicksecure logo](assets/img/linux-desktop/kicksecure.svg){ align=right }
    
    **Kicksecure**—in oversimplified terms—is a set of scripts, configurations, and packages that substantially reduce the attack surface of Debian. Cubre muchas recomendaciones de privacidad y seguridad por defecto. It also serves as the base OS for [Whonix](#whonix).
    
    [:octicons-home-16: Homepage](https://www.kicksecure.com/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.kicksecure.com/wiki/Privacy_Policy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://www.kicksecure.com/wiki/Documentation){ .card-link title=Documentation }
    [:octicons-code-16:](https://github.com/Kicksecure){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://www.kicksecure.com/wiki/Donate){ .card-link title=Contribute }

## Criterios

Choosing a Linux distro that is right for you will come down to a huge variety of personal preferences, and this page is **not** meant to be an exhaustive list of every viable distribution. Our Linux overview page has some advice on [choosing a distro](os/linux-overview.md#choosing-your-distribution) in more detail. The distros on *this* page do all generally follow the guidelines we covered there, and all meet these standards:

- Free and open-source.
- Receives regular software and kernel updates.
- [Avoids X11](os/linux-overview.md#wayland).
    - The notable exception here is Qubes, but the isolation issues which X11 typically has are avoided by virtualization. This isolation only applies to apps *running in different qubes* (virtual machines), apps running in the *same* qube are not protected from each other.
- Supports full-disk encryption during installation.
- Doesn't freeze regular releases for more than 1 year.
    - We [recommend against](os/linux-overview.md#release-cycle) "Long Term Support" or "stable" distro releases for desktop usage.
- Supports a wide variety of hardware.
- Preference towards larger projects.
    - Maintaining an operating system is a major challenge, and smaller projects have a tendency to make more avoidable mistakes, or delay critical updates (or worse, disappear entirely). We lean towards projects which will likely be around 10 years from now (whether that's due to corporate backing or very significant community support), and away from projects which are hand-built or have a small number of maintainers.

In addition, [our standard criteria](about/criteria.md) for recommended projects still applies. **Please note we are not affiliated with any of the projects we recommend.**
