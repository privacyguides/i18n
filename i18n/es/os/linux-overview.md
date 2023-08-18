---
title: Vista general de Linux
icon: simple/linux
description: Linux es una alternativa de sistema operativo de escritorio de código abierto y centrado en la privacidad, pero no todas las distribuciones son iguales.
---

**Linux** es una alternativa de sistema operativo de escritorio de código abierto centrada en la privacidad. Frente a la telemetría omnipresente y otras tecnologías que atentan contra la privacidad en los principales sistemas operativos, Linux de escritorio ha seguido siendo la opción clara para quienes buscan un control total sobre sus ordenadores desde la base.

En general, nuestro sitio web utiliza el término "Linux" para describir las distribuciones Linux de **escritorio**. En esta página no se tratan otros sistemas operativos que también utilizan el núcleo Linux, como ChromeOS, Android y Qubes OS.

[Nuestras recomendaciones de Linux: :material-arrow-right-drop-circle:](../desktop.md ""){.md-button}

## Notas de Privacidad

Linux plantea algunos problemas de privacidad importantes que debes tener en cuenta. A pesar de estos inconvenientes, las distribuciones Linux de escritorio siguen siendo estupendas para la mayoría de la gente que desea:

- Evitar la telemetría que, regularmente, viene con los sistemas operativos propietarios
- Mantener la ['libertad del software'](https://www.gnu.org/philosophy/free-sw.en.html#four-freedoms)
- Utilizar sistemas centrados en la privacidad como [Whonix](https://www.whonix.org) o [Tails](https://tails.boum.org/)

### Seguridad de Código Abierto

Es un [error común](../basics/common-misconceptions.md#open-source-software-is-always-secure-or-proprietary-software-is-more-secure) pensar que Linux y otros programas de código abierto son intrínsecamente seguros simplemente porque el código fuente está disponible. Se espera que la verificación comunitaria se realice con regularidad, pero este no siempre es [el caso](https://seirdy.one/posts/2022/02/02/floss-security/).

En realidad, la seguridad de las distribuciones depende de varios factores, como la actividad del proyecto, la experiencia de los desarrolladores, el nivel de rigor aplicado a las revisiones del código y la frecuencia con la que se presta atención a partes concretas del código base, que pueden permanecer intactas durante años.

### Elementos de Seguridad Ausentes

Por el momento, Linux de escritorio [está por detrás de alternativas](https://discussion.fedoraproject.org/t/fedora-strategy-2028-proposal-fedora-linux-is-as-secure-as-macos/46899/9) como macOS o Android cuando se trata de ciertas características de seguridad. Esperamos ver mejoras en estos ámbitos en el futuro.

- El **arranque verificado ** en Linux no es tan robusto como alternativas como el [Arranque Seguro](https://support.apple.com/guide/security/secac71d5623/web) de Apple o el [Arranque Verificado](https://source.android.com/security/verifiedboot) de Android. El arranque verificado evita la manipulación persistente por parte de malware y [los ataques evil maid](https://en.wikipedia.org/wiki/Evil_Maid_attack), pero sigue [sin estar disponible en gran medida incluso en las distribuciones más avanzadas](https://discussion.fedoraproject.org/t/has-silverblue-achieved-verified-boot/27251/3).

- **Un aislamiento fuerte** para aplicaciones en Linux que es muy deficiente, incluso con aplicaciones en contenedores como Flatpaks o soluciones de aislamiento como Firejail. Flatpak es la utilidad de aislamiento más prometedora para Linux hasta el momento, pero sigue siendo deficiente en muchas áreas y permite [valores predeterminados inseguros](https://flatkill.org/2020/) que permiten a la mayoría de las aplicaciones eludir trivialmente su aislamineto.

Additionally, Linux falls behind in implementing [exploit mitigations](https://madaidans-insecurities.github.io/linux.html#exploit-mitigations) which are now standard on other operating systems, such as Arbitrary Code Guard on Windows or Hardened Runtime on macOS. Also, most Linux programs and Linux itself are coded in memory-unsafe languages. Memory corruption bugs are responsible for the [majority of vulnerabilities](https://msrc.microsoft.com/blog/2019/07/a-proactive-approach-to-more-secure-code/) fixed and assigned a CVE. While this is also true for Windows and macOS, they are quickly making progress on adopting memory-safe languages—such as Rust and Swift, respectively—while there is no similar effort to rewrite Linux in a memory-safe language like Rust.

## Elegir tu distribución

No todas las distribuciones Linux son iguales. Our [Linux recommendation page](../desktop.md) is not meant to be an authoritative source on which distribution you should use, but our recommendations *are* aligned with the following guidelines. These are a few things you should keep in mind when choosing a distribution:

### Ciclo de lanzamiento

Recomendamos encarecidamente que elijas las distribuciones que permanecen cerca a los lanzamientos estables, comúnmente denominadas como distribuciones de lanzamiento continuo. Esto se debe a que las distribuciones de lanzamiento de ciclo congelado, normalmente no actualizan las versiones de sus paquetes y se encuentran detrás en actualizaciones de seguridad.

Para las distribuciones congeladas como [Debian](https://www.debian.org/security/faq#handling), se espera que los encargados de mantener los paquetes adapten los parches para corregir vulnerabilidades, en lugar de actualizar el software a la "siguiente versión" lanzada por el desarrollador original. Some security fixes [do not](https://arxiv.org/abs/2105.14565) receive a [CVE ID](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures) (particularly less popular software) at all and therefore do not make it into the distribution with this patching model. Por ello, a veces las correcciones de seguridad son pospuestas hasta la siguiente versión importante.

No creemos que retener paquetes y aplicar los parches provisionales sea una buena idea, porque se aleja de la forma en que el desarrollador se pudo asegurar que el software funcione. [Richard Brown](https://rootco.de/aboutme/) tiene una presentación sobre esto:

<div class="yt-embed">
  <iframe width="560" height="315" src="https://invidious.privacyguides.net/embed/i8c0mg_mS7U?local=true" title="Las liberaciones regulares son erróneas, rueda por tu vida" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

### Actualizaciones tradicionales vs. Atómicas

Tradicionalmente, las distribuciones de Linux se actualizan secuencialmente, actualizando los paquetes deseados. Las actualizaciones tradicionales, como las utilizadas en las distribuciones basadas en Fedora, Arch Linux y Debian, son menos confiables, si un error se produce al actualizar.

Las distribuciones de actualizaciones Atómicas, aplican las actualizaciones en su totalidad o no del todo. Normalmente, los sistemas de actualización transaccional también son atómicos.

Un sistema de actualización transaccional crea una instantánea que se realiza antes y después de haber aplicado una actualización. Si una actualización falla en cualquier momento (debido a situaciones como fallas de electricidad), la actualización puede revertirse fácilmente al "último estado bueno conocido".

El método de actualizaciones Atómicas es utilizado para distribuciones inmutables como Silverblue, Tumbleweed y NixOS, y puede obtener confiabilidad con este modelo. [Adam Šamalik](https://twitter.com/adsamalik) brinda una presentación sobre cómo `rpm-ostree` funciona con Silverblue:

<div class="yt-embed">
  <iframe width="560" height="315" src="https://invidious.privacyguides.net/embed/-hpV5l-gJnQ?local=true" title="Probemos Fedora Silverblue — ¡un sistema operativo de escritorio inmutable! - Adam Šamalik" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

### Distribuciones "enfocadas en la seguridad"

A menudo existe cierta confusión entre las distribuciones "enfocadas en la privacidad" y las distribuciones "pentesting". A quick search for “the most secure Linux distribution” will often give results like Kali Linux, Black Arch, or Parrot OS. Estas distribuciones son distribuciones de pruebas de penetración ofensivas que incluyen herramientas para probar otros sistemas. Estas no incluyen ninguna "seguridad adicional" o mitigaciones defensivas destinadas a un uso regular.

### Distribuciones basadas en Arch Linux

Arch and Arch-based distributions are not recommended for those new to Linux (regardless of distribution) as they require regular [system maintenance](https://wiki.archlinux.org/title/System_maintenance). Arch does not have a distribution update mechanism for the underlying software choices. Por ello, hay que estar al tanto de las tendencias actuales y adoptar las tecnologías a medida que van sustituyendo a las prácticas más antiguas.

Para un sistema seguro, también se espera que tenga suficientes conocimientos de Linux para configurar correctamente la seguridad de su sistema, como la adopción de un sistema [de control de acceso obligatorio](https://en.wikipedia.org/wiki/Mandatory_access_control), la configuración de listas negras de [módulos del kernel](https://en.wikipedia.org/wiki/Loadable_kernel_module#Security), el endurecimiento de los parámetros de arranque, la manipulación de parámetros[ sysctl](https://en.wikipedia.org/wiki/Sysctl), y saber qué componentes necesitan como [Polkit](https://en.wikipedia.org/wiki/Polkit).

Anyone using the [Arch User Repository (AUR)](https://wiki.archlinux.org/title/Arch_User_Repository) **must** be comfortable auditing PKGBUILDs that they download from that service. Los paquetes AUR son contenidos producidos por la comunidad y no se examinan de ninguna manera, por lo que son vulnerables a los ataques a la cadena de suministro de software, como de hecho ha sucedido en [en el pasado](https://www.bleepingcomputer.com/news/security/malware-found-in-arch-linux-aur-package-repository/).

The AUR should always be used sparingly, and often there is a lot of bad advice on various pages which direct people to blindly use [AUR helpers](https://wiki.archlinux.org/title/AUR_helpers) without sufficient warning. Se aplican advertencias similares al uso de Archivos de Paquetes Personales (PPA) de terceros en distribuciones basadas en Debian o Proyectos Comunitarios (COPR) en Fedora.

If you are experienced with Linux and wish to use an Arch-based distribution, we generally recommend mainline Arch Linux over any of its derivatives.

Additionally, we recommend **against** these two Arch derivatives specifically:

- **Manjaro**: Esta distribución retiene los paquetes durante 2 semanas para asegurarse de que sus propios cambios no se rompan, no para asegurarse de que el flujo ascendente sea estable. Cuando se utilizan paquetes AUR, suelen compilarse con las últimas [bibliotecas](https://en.wikipedia.org/wiki/Library_(computing)) de los repositorios de Arch.
- **Garuda**: Utilizan [Chaotic-AUR](https://aur.chaotic.cx/) que compila automáticamente y a ciegas paquetes del AUR. No existe ningún proceso de verificación que garantice que los paquetes AUR no sufran ataques en la cadena de suministro.

### Kernel Linux-libre y distribuciones "Libre"

We recommend **against** using the Linux-libre kernel, since it [removes security mitigations](https://www.phoronix.com/news/GNU-Linux-Libre-5.7-Released) and [suppresses kernel warnings](https://news.ycombinator.com/item?id=29674846) about vulnerable microcode.

## Recomendaciones Generales

### Cifrado de unidad

La mayoría de las distribuciones de Linux tienen una opción dentro de su instalador para habilitar [LUKS](../encryption.md#linux-unified-key-setup) FDE. Si esta opción no se configura en el momento de la instalación, tendrá que hacer una copia de seguridad de sus datos y volver a instalar, ya que el cifrado se aplica después de [particionar el disco](https://en.wikipedia.org/wiki/Disk_partitioning), pero antes de formatear [el sistema de archivos](https://en.wikipedia.org/wiki/File_system). También te sugerimos que borres de forma segura tu dispositivo de almacenamiento:

- [Borrado seguro de datos :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/05/25/secure-data-erasure/)

### Swap

Consider using [ZRAM](https://wiki.archlinux.org/title/Zram#Using_zram-generator) instead of a traditional swap file or partition to avoid writing potentially sensitive memory data to persistent storage (and improve performance). Fedora-based distributions [use ZRAM by default](https://fedoraproject.org/wiki/Changes/SwapOnZRAM).

If you require suspend-to-disk (hibernation) functionality, you will still need to use a traditional swap file or partition. Make sure that any swap space you do have on a persistent storage device is [encrypted](https://wiki.archlinux.org/title/Dm-crypt/Swap_encryption) at a minimum to mitigate some of these threats.

### Wayland

We recommend using a desktop environment that supports the [Wayland](https://en.wikipedia.org/wiki/Wayland_(display_server_protocol)) display protocol, as it was developed with security [in mind](https://lwn.net/Articles/589147/). Its predecessor ([X11](https://en.wikipedia.org/wiki/X_Window_System)) does not support GUI isolation, which allows any window to [record, log, and inject inputs in other windows](https://blog.invisiblethings.org/2011/04/23/linux-security-circus-on-gui-isolation.html), making any attempt at sandboxing futile. While there are options to do nested X11 such as [Xpra](https://en.wikipedia.org/wiki/Xpra) or [Xephyr](https://en.wikipedia.org/wiki/Xephyr), they often come with negative performance consequences, and are neither convenient to set up nor preferable over Wayland.

Afortunadamente, entornos comunes como [GNOME](https://www.gnome.org), [KDE](https://kde.org), y el gestor de ventanas [Sway](https://swaywm.org) tienen soporte para Wayland. Algunas distribuciones como Fedora y Tumbleweed lo utilizan por defecto, y es posible que otras lo hagan en el futuro, ya que X11 está en [modo de mantenimiento duro](https://www.phoronix.com/news/X.Org-Maintenance-Mode-Quickly). Si estás utilizando uno de esos entornos es tan fácil como seleccionar la sesión "Wayland" en el gestor de pantalla del escritorio ([GDM](https://en.wikipedia.org/wiki/GNOME_Display_Manager), [SDDM](https://en.wikipedia.org/wiki/Simple_Desktop_Display_Manager)).

Estamos **en contra** de usar entornos de escritorio o gestores de ventanas que no tengan soporte para Wayland, como Cinnamon (por defecto en Linux Mint), Pantheon (por defecto en Elementary OS), MATE, Xfce e i3.

### Firmware propietario (actualizaciones de microcódigo)

Some Linux distributions (such as [Linux-libre](https://en.wikipedia.org/wiki/Linux-libre)-based or DIY distros) don’t come with the proprietary [microcode](https://en.wikipedia.org/wiki/Microcode) updates which patch critical security vulnerabilities. Algunos ejemplos notables de estas vulnerabilidades incluyen [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability)), [Meltdown](https://en.wikipedia.org/wiki/Meltdown_(security_vulnerability)), [SSB](https://en.wikipedia.org/wiki/Speculative_Store_Bypass), [Foreshadow](https://en.wikipedia.org/wiki/Foreshadow), [MDS](https://en.wikipedia.org/wiki/Microarchitectural_Data_Sampling), [SWAPGS](https://en.wikipedia.org/wiki/SWAPGS_(security_vulnerability)), y otras [vulnerabilidades de hardware](https://www.kernel.org/doc/html/latest/admin-guide/hw-vuln/index.html).

We **highly recommend** that you install microcode updates, as they contain important security patches for the CPU which can not be fully mitigated in software alone. Tanto Fedora como openSUSE tienen las actualizaciones de microcódigo aplicadas por defecto.

### Actualizaciones

La mayoría de las distribuciones de Linux instalan automáticamente las actualizaciones o le recuerdan que debe hacerlo. Es importante mantener el sistema operativo actualizado para que el software esté parcheado cuando se detecte una vulnerabilidad.

Some distributions (particularly those aimed at advanced users) are more bare bones and expect you to do things yourself (e.g. Arch or Debian). Será necesario ejecutar manualmente el "gestor de paquetes" (`apt`, `pacman`, `dnf`, etc.) para recibir actualizaciones de seguridad importantes.

Además, algunas distribuciones no descargan automáticamente las actualizaciones de firmware. Para eso necesitarás instalar [`fwupd`](https://wiki.archlinux.org/title/Fwupd).

## Ajustes de privacidad

### Aleatorización de direcciones Mac

Many desktop Linux distributions (Fedora, openSUSE, etc.) come with [NetworkManager](https://en.wikipedia.org/wiki/NetworkManager) to configure Ethernet and Wi-Fi settings.

Es posible [aleatorizar](https://fedoramagazine.org/randomize-mac-address-nm/) la [dirección MAC](https://en.wikipedia.org/wiki/MAC_address) cuando se utiliza NetworkManager. Esto proporciona un poco más de privacidad en las redes Wi-Fi, ya que hace más difícil rastrear dispositivos específicos en la red a la que estás conectado. [**No**](https://papers.mathyvanhoef.com/wisec2016.pdf) te hace anónimo.

Recomendamos cambiar la configuración a **aleatoria** en lugar de **estable**, como se sugiere en el [artículo](https://fedoramagazine.org/randomize-mac-address-nm/).

Si estás utilizando [systemd-networkd](https://en.wikipedia.org/wiki/Systemd#Ancillary_components), necesitarás configurar [`MACAddressPolicy=random`](https://www.freedesktop.org/software/systemd/man/systemd.link.html#MACAddressPolicy=) que habilitará [RFC 7844 (Perfiles de anonimato para clientes DHCP)](https://www.freedesktop.org/software/systemd/man/systemd.network.html#Anonymize=).

MAC address randomization is primarily beneficial for Wi-Fi connections. For Ethernet connections, randomizing your MAC address provides little (if any) benefit, because a network administrator can trivially identify your device by other means (such as inspecting the port you are connected to on the network switch). La aleatorización de las direcciones MAC Wi-Fi depende del soporte del firmware de la Wi-Fi.

### Otros identificadores

Hay otros identificadores del sistema con los que conviene tener cuidado. Deberías pensar en esto para ver si se aplica a tu [modelo de amenaza](../basics/threat-modeling.md):

- **Nombres de host:** El nombre de host de tu sistema se comparte con las redes a las que te conectas. Debes evitar incluir términos identificativos como tu nombre o tu sistema operativo en tu nombre de host, en su lugar, cíñete a términos genéricos o cadenas de caracteres aleatorias.
- **Nombres de usuario:** Del mismo modo, tu nombre de usuario se utiliza de diversas maneras en todo el sistema. Considera la posibilidad de utilizar términos genéricos como "usuario" en lugar de tu nombre real.
- **ID de máquina:**Durante la instalación se genera un ID de máquina único que se almacena en tu dispositivo. Considera [configurarlo en un ID genérico](https://madaidans-insecurities.github.io/guides/linux-hardening.html#machine-id).

### Contador de sistema

El Proyecto Fedora [cuenta](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting) cuántos sistemas únicos acceden a sus réplicas utilizando una variable [`countme`](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting#Detailed_Description) en lugar de un ID único. Fedora hace esto para determinar la carga y aprovisionar mejores servidores para las actualizaciones cuando sea necesario.

Esta [opción](https://dnf.readthedocs.io/en/latest/conf_ref.html#options-for-both-main-and-repo) está actualmente desactivada por defecto. Recomendamos añadir `countme=false` en `/etc/dnf/dnf.conf` por si se habilita en el futuro. En sistemas que utilizan `rpm-ostree` como Silverblue, la opción countme se desactiva enmascarando el temporizador [rpm-ostree-countme](https://fedoramagazine.org/getting-better-at-counting-rpm-ostree-based-systems/).

openSUSE también utiliza un [ID único](https://en.opensuse.org/openSUSE:Statistics) para contar los sistemas, que puede desactivarse borrando el archivo `/var/lib/zypp/AnonymousUniqueId`.
