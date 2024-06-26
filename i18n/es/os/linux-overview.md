---
title: Vista General de Linux
icon: simple/linux
description: Linux es una alternativa de sistema operativo de escritorio de código abierto y centrado en la privacidad, pero no todas las distribuciones son iguales.
---

**Linux** es una alternativa de sistema operativo de escritorio de código abierto centrada en la privacidad. In the face of pervasive telemetry and other privacy-encroaching technologies in mainstream operating systems, desktop Linux has remained the clear choice for people looking for total control over their computers from the ground up.

En general, nuestro sitio web utiliza el término "Linux" para describir las distribuciones Linux de **escritorio**. En esta página no se tratan otros sistemas operativos que también utilizan el núcleo Linux, como ChromeOS, Android y Qubes OS.

[Nuestras recomendaciones de Linux: :material-arrow-right-drop-circle:](../desktop.md ""){.md-button}

## Notas de Privacidad

Linux plantea algunos problemas de privacidad importantes que debes tener en cuenta. A pesar de estos inconvenientes, las distribuciones Linux de escritorio siguen siendo estupendas para la mayoría de la gente que desea:

- Evitar la telemetría que, regularmente, viene con los sistemas operativos propietarios
- Mantener la [libertad de software](https://gnu.org/philosophy/free-sw.en.html#four-freedoms)
- Use privacy-focused systems such as [Whonix](../desktop.md#whonix) or [Tails](../desktop.md#tails)

### Seguridad de Código Abierto

Es un [error común](../basics/common-misconceptions.md#open-source-software-is-always-secure-or-proprietary-software-is-more-secure) pensar que Linux y otros programas de código abierto son intrínsecamente seguros simplemente porque el código fuente está disponible. Se espera que la verificación comunitaria se realice con regularidad, pero este no siempre es [el caso](https://seirdy.one/posts/2022/02/02/floss-security).

En realidad, la seguridad de las distribuciones depende de varios factores, como la actividad del proyecto, la experiencia de los desarrolladores, el nivel de rigor aplicado a las revisiones del código y la frecuencia con la que se presta atención a partes concretas del código base, que pueden permanecer intactas durante años.

### Elementos de Seguridad Ausentes

Por el momento, Linux de escritorio [está por detrás de alternativas](https://discussion.fedoraproject.org/t/fedora-strategy-2028-proposal-fedora-linux-is-as-secure-as-macos/46899/9) como macOS o Android cuando se trata de ciertas características de seguridad. Esperamos ver mejoras en estos ámbitos en el futuro.

- El **arranque verificado ** en Linux no es tan robusto como alternativas como el [Arranque Seguro](https://support.apple.com/guide/security/secac71d5623/web) de Apple o el [Arranque Verificado](https://source.android.com/security/verifiedboot) de Android. El arranque verificado evita la manipulación persistente por parte de malware y [los ataques evil maid](https://en.wikipedia.org/wiki/Evil_Maid_attack), pero sigue [sin estar disponible en gran medida incluso en las distribuciones más avanzadas](https://discussion.fedoraproject.org/t/has-silverblue-achieved-verified-boot/27251/3).

- **Un aislamiento fuerte** para aplicaciones en Linux que es muy deficiente, incluso con aplicaciones en contenedores como Flatpaks o soluciones de aislamiento como Firejail. Flatpak es la utilidad de aislamiento más prometedora para Linux hasta el momento, pero sigue siendo deficiente en muchas áreas y permite [valores predeterminados inseguros](https://flatkill.org/2020) que permiten a la mayoría de las aplicaciones eludir trivialmente su aislamineto.

Además, Linux se queda atrás en la implementación de [mitigaciones de exploits](https://madaidans-insecurities.github.io/linux.html#exploit-mitigations) que ahora son estándar en otros sistemas operativos, como Protección de Código Arbitrario en Windows o Tiempo de Ejecución Reforzado en macOS. Además, la mayoría de los programas Linux y el propio Linux están codificados en lenguajes poco seguros para la memoria. Los fallos de corrupción de memoria son responsables de la [mayoría de las vulnerabilidades](https://msrc.microsoft.com/blog/2019/07/a-proactive-approach-to-more-secure-code) corregidas y a las que se asigna un CVE. Aunque esto también es cierto para Windows y macOS, estos están avanzando rápidamente en la adopción de lenguajes seguros para la memoria -como Rust y Swift, respectivamente-, mientras que no existe un esfuerzo similar para reescribir Linux en un lenguaje seguro para la memoria como Rust.

## Elegir tu distribución

No todas las distribuciones Linux son iguales. Nuestra [página de recomendaciones de Linux](../desktop.md) no pretende ser una fuente autoritaria sobre qué distribución debes utilizar, pero nuestras recomendaciones *están* alineadas con las siguientes directrices. Estas son algunas cosas que debes tener en cuenta a la hora de elegir una distribución:

### Ciclo de lanzamiento

Recomendamos encarecidamente que elijas distribuciones que permanezcan cerca de los lanzamientos estables del software de origen, comúnmente denominadas como distribuciones de lanzamiento continuo. Esto se debe a que las distribuciones de lanzamiento de ciclo congelado, normalmente no actualizan las versiones de sus paquetes y se encuentran detrás en actualizaciones de seguridad.

Para las distribuciones congeladas como [Debian](https://debian.org/security/faq#handling), se espera que los encargados de mantener los paquetes adapten los parches para corregir vulnerabilidades, en lugar de actualizar el software a la "siguiente versión" lanzada por el desarrollador original. Algunas correcciones de seguridad [no](https://arxiv.org/abs/2105.14565) reciben un [CVE ID](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures) (en particular el software menos popular) y por lo tanto no llegan a la distribución con este modelo de parches. As a result, minor security fixes are sometimes held back until the next major release.

No creemos que retener paquetes y aplicar parches provisionales sea una buena idea, ya que se aparta de la forma en que el desarrollador podría haber previsto que funcionara el software. [Richard Brown](https://rootco.de/aboutme) tiene una presentación sobre esto:

<div class="yt-embed">
  <iframe width="560" height="315" src="https://invidious.privacyguides.net/embed/i8c0mg_mS7U?local=true" title="Las liberaciones regulares son erróneas, rueda por tu vida" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

### Actualizaciones tradicionales vs. Atómicas

Tradicionalmente, las distribuciones Linux se actualizan mediante la actualización secuencial de los paquetes deseados. Las actualizaciones tradicionales, como las utilizadas en las distribuciones basadas en Fedora, Arch Linux y Debian, son menos confiables, si un error se produce al actualizar.

Las distribuciones de actualización atómica aplican las actualizaciones en su totalidad o no las aplican. Normalmente, los sistemas de actualización transaccional también son atómicos.

Un sistema de actualización transaccional crea una instantánea que se realiza antes y después de haber aplicado una actualización. Si una actualización falla en cualquier momento (debido a situaciones como fallas de electricidad), la actualización puede revertirse fácilmente al "último estado bueno conocido".

El método de actualización Atómica es usado para [distribuciones](../desktop.md#atomic-distributions) como Silverblue, Tumbleweed, y NixOS y puede lograr confiabilidad con este modelo. [Adam Šamalik](https://twitter.com/adsamalik) brinda una presentación sobre cómo `rpm-ostree` funciona con Silverblue:

<div class="yt-embed">
  <iframe width="560" height="315" src="https://invidious.privacyguides.net/embed/-hpV5l-gJnQ?local=true" title="Probemos Fedora Silverblue — ¡un sistema operativo de escritorio inmutable! - Adam Šamalik" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

### Distribuciones "enfocadas en la seguridad"

A menudo existe cierta confusión entre las distribuciones "enfocadas en la seguridad" y las distribuciones "pentesting". Una búsqueda rápida de "la distribución de Linux más segura" suele arrojar resultados como Kali Linux, Black Arch o Parrot OS. Estas distribuciones son distribuciones de pruebas de penetración ofensivas que incluyen herramientas para probar otros sistemas. Estas no incluyen ninguna "seguridad adicional" o mitigaciones defensivas destinadas a un uso regular.

### Distribuciones basadas en Arch Linux

Arch y las distribuciones basadas en Arch no son recomendables para quienes se inician en Linux (independientemente de la distribución), ya que requieren un [mantenimiento del sistema](https://wiki.archlinux.org/title/System_maintenance) regular. Arch no dispone de un mecanismo de actualización de la distribución para las opciones de software subyacentes. Por ello, hay que estar al tanto de las tendencias actuales y adoptar las tecnologías a medida que van sustituyendo a las prácticas más antiguas.

Para un sistema seguro, también se espera que tengas suficientes conocimientos de Linux para configurar correctamente la seguridad del sistema, como la adopción de un sistema [de control de acceso obligatorio](https://en.wikipedia.org/wiki/Mandatory_access_control), la configuración de [módulos del kernel](https://en.wikipedia.org/wiki/Loadable_kernel_module#Security), listas negras, el endurecimiento de los parámetros de arranque, la manipulación de parámetros [sysctl](https://en.wikipedia.org/wiki/Sysctl), y saber qué componentes necesitan, como [Polkit](https://en.wikipedia.org/wiki/Polkit).

Cualquiera que utilice el [Repositorio de Usuario de Arch (AUR)](https://wiki.archlinux.org/title/Arch_User_Repository) **debe** sentirse cómodo auditando los PKGBUILDs que descargue de ese servicio. Los paquetes AUR son contenidos producidos por la comunidad y no se examinan de ninguna manera, por lo que son vulnerables a los ataques a la cadena de suministro de software, como de hecho ha sucedido en [en el pasado](https://bleepingcomputer.com/news/security/malware-found-in-arch-linux-aur-package-repository).

El AUR debe utilizarse siempre con moderación, y a menudo hay muchos malos consejos en diversas páginas que dirigen a la gente a utilizar ciegamente [AUR helpers](https://wiki.archlinux.org/title/AUR_helpers) sin suficiente advertencia. Se aplican advertencias similares al uso de Archivos de Paquetes Personales (PPA) de terceros en distribuciones basadas en Debian o Proyectos Comunitarios (COPR) en Fedora.

Si tienes experiencia con Linux y deseas utilizar una distribución basada en Arch, generalmente recomendamos Arch Linux de línea principal sobre cualquiera de sus derivados.

Además, estamos en **contra** de usar estos dos derivados de Arch específicamente:

- **Manjaro**: Esta distribución retiene los paquetes durante 2 semanas para asegurarse de que sus propios cambios no se rompan, no para asegurarse de que el flujo ascendente sea estable. Cuando se utilizan paquetes AUR, suelen compilarse con las últimas [bibliotecas](https://en.wikipedia.org/wiki/Library_(computing)) de los repositorios de Arch.
- **Garuda**: Utilizan [Chaotic-AUR](https://aur.chaotic.cx) que compila automáticamente y a ciegas paquetes del AUR. No existe ningún proceso de verificación que garantice que los paquetes AUR no sufran ataques en la cadena de suministro.

### Núcleo Linux-libre y distribuciones "Libre"

Recomendamos **no** utilizar el kernel Linux-libre, ya que [elimina las mitigaciones de seguridad](https://phoronix.com/news/GNU-Linux-Libre-5.7-Released) y [suprime las advertencias del kernel](https://news.ycombinator.com/item?id=29674846) sobre microcódigo vulnerable.

## Recomendaciones Generales

### Cifrado de Unidad

La mayoría de las distribuciones de Linux tienen una opción dentro de su instalador para habilitar [LUKS](../encryption.md#linux-unified-key-setup) FDE. Si esta opción no se configura en el momento de la instalación, tendrás que hacer una copia de seguridad de tus datos y volver a instalarla, ya que el cifrado se aplica después de [particionar el disco](https://en.wikipedia.org/wiki/Disk_partitioning), pero antes de formatear [el sistema de archivos](https://en.wikipedia.org/wiki/File_system). También te sugerimos que borres de forma segura tu dispositivo de almacenamiento:

- [Borrado Seguro de Datos :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/05/25/secure-data-erasure)

### Swap

Considera utilizar [ZRAM](https://wiki.archlinux.org/title/Zram#Using_zram-generator) en lugar de un archivo o partición de swap tradicional para evitar la escritura de datos de memoria potencialmente sensibles en el almacenamiento persistente (y mejorar el rendimiento). Las distribuciones basadas en Fedora [utilizan ZRAM por defecto](https://fedoraproject.org/wiki/Changes/SwapOnZRAM).

Si necesitas la función de suspensión en disco (hibernación), tendrás que utilizar un archivo o partición de swap tradicional. Asegúrate de que cualquier espacio de swap que tengas en un dispositivo de almacenamiento persistente esté [cifrado ](https://wiki.archlinux.org/title/Dm-crypt/Swap_encryption) como mínimo para mitigar algunas de estas amenazas.

### Wayland

Recomendamos utilizar un entorno de escritorio compatible con el protocolo de visualización [Wayland](https://en.wikipedia.org/wiki/Wayland_(display_server_protocol)), ya que se ha desarrollado teniendo [en cuenta](https://lwn.net/Articles/589147) la seguridad. Su predecesor ([X11](https://en.wikipedia.org/wiki/X_Window_System)) no soporta el aislamiento GUI, lo que permite a cualquier ventana [grabar, registrar e inyectar entradas en otras ventanas](https://blog.invisiblethings.org/2011/04/23/linux-security-circus-on-gui-isolation.html), haciendo inútil cualquier intento de aislamiento. Aunque hay opciones para hacer X11 anidado como [Xpra](https://en.wikipedia.org/wiki/Xpra) o [Xephyr](https://en.wikipedia.org/wiki/Xephyr), a menudo vienen con consecuencias negativas en el rendimiento, y no son ni convenientes de configurar ni preferibles sobre Wayland.

Fortunately, [Wayland compositors](https://en.wikipedia.org/wiki/Wayland_(protocol)#Wayland_compositors) such as those included with [GNOME](https://gnome.org) and [KDE Plasma](https://kde.org) now have good support for Wayland along with some other compositors that use [wlroots](https://gitlab.freedesktop.org/wlroots/wlroots/-/wikis/Projects-which-use-wlroots), (e.g. [Sway](https://swaywm.org)). Algunas distribuciones como Fedora y Tumbleweed lo utilizan por defecto, y es posible que otras lo hagan en el futuro, ya que X11 está en [modo de mantenimiento duro](https://phoronix.com/news/X.Org-Maintenance-Mode-Quickly). Si estás utilizando uno de esos entornos es tan fácil como seleccionar la sesión "Wayland" en el gestor de pantalla del escritorio ([GDM](https://en.wikipedia.org/wiki/GNOME_Display_Manager), [SDDM](https://en.wikipedia.org/wiki/Simple_Desktop_Display_Manager)).

Estamos **en contra** de usar entornos de escritorio o gestores de ventanas que no tengan soporte para Wayland, como Cinnamon (por defecto en Linux Mint), Pantheon (por defecto en Elementary OS), MATE, Xfce e i3.

### Firmware de Propietario (Actualizaciones de Microcódigo)

Algunas distribuciones de Linux (como las basadas en [Linux-libre](https://en.wikipedia.org/wiki/Linux-libre)o las DIY) no incluyen las actualizaciones de [microcódigo](https://en.wikipedia.org/wiki/Microcode) de propietario que parchean vulnerabilidades de seguridad críticas. Algunos ejemplos notables de estas vulnerabilidades son [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability)), [Meltdown](https://en.wikipedia.org/wiki/Meltdown_(security_vulnerability)), [SSB](https://en.wikipedia.org/wiki/Speculative_Store_Bypass), [Foreshadow](https://en.wikipedia.org/wiki/Foreshadow), [MDS](https://en.wikipedia.org/wiki/Microarchitectural_Data_Sampling), [SWAPGS](https://en.wikipedia.org/wiki/SWAPGS_(security_vulnerability)) y otras [vulnerabilidades de hardware](https://kernel.org/doc/html/latest/admin-guide/hw-vuln/index.html).

Nosotros **recomendamos encarecidamente** que instales las actualizaciones de microcódigo, ya que contienen importantes parches de seguridad para la CPU que no pueden mitigarse totalmente sólo con software. Tanto Fedora como openSUSE tienen las actualizaciones de microcódigo aplicadas por defecto.

### Actualizaciones

La mayoría de las distribuciones de Linux instalan automáticamente las actualizaciones o te recuerdan que debes hacerlo. Es importante mantener el sistema operativo actualizado para que el software esté parcheado cuando se detecte una vulnerabilidad.

Algunas distribuciones (especialmente las dirigidas a usuarios avanzados) son más básicas y esperan que hagas las cosas tú mismo (por ejemplo, Arch o Debian). Con estas distribuciones será necesario ejecutar manualmente el "gestor de paquetes" (`apt`, `pacman`, `dnf`, etc.) para recibir actualizaciones de seguridad importantes.

Además, algunas distribuciones no descargan automáticamente las actualizaciones de firmware. For that, you will need to install [`fwupd`](https://wiki.archlinux.org/title/Fwupd).

## Ajustes de privacidad

### Aleatorización de direcciones Mac

Muchas distribuciones Linux de escritorio (Fedora, openSUSE, etc.) vienen con [NetworkManager](https://en.wikipedia.org/wiki/NetworkManager) para configurar los ajustes de Ethernet y Wi-Fi.

Es posible [aleatorizar](https://fedoramagazine.org/randomize-mac-address-nm) la [dirección MAC](https://en.wikipedia.org/wiki/MAC_address) cuando se utiliza NetworkManager. Esto proporciona un poco más de privacidad en las redes Wi-Fi, ya que hace más difícil rastrear dispositivos específicos en la red a la que estás conectado. [**No**](https://papers.mathyvanhoef.com/wisec2016.pdf) te hace anónimo.

Recomendamos cambiar la configuración a **aleatoria** en lugar de **estable**, como se sugiere en el [artículo](https://fedoramagazine.org/randomize-mac-address-nm).

Si estás utilizando [systemd-networkd](https://en.wikipedia.org/wiki/Systemd#Ancillary_components), necesitarás configurar [`MACAddressPolicy=aleatorio`](https://freedesktop.org/software/systemd/man/systemd.link.html#MACAddressPolicy=) que activará [RFC 7844 (Perfiles de Anonimato para Clientes DHCP)](https://freedesktop.org/software/systemd/man/systemd.network.html#Anonymize=).

La aleatorización de direcciones MAC es beneficiosa sobre todo para las conexiones Wi-Fi. En el caso de las conexiones Ethernet, aleatorizar la dirección MAC aporta pocas ventajas (si es que aporta alguna), ya que un administrador de red puede identificar trivialmente tu dispositivo por otros medios (como inspeccionar el puerto al que está conectado en el conmutador de red). La aleatorización de las direcciones MAC Wi-Fi depende del soporte del firmware de la Wi-Fi.

### Otros identificadores

Hay otros identificadores del sistema con los que conviene tener cuidado. Deberías pensar en esto para ver si se aplica a tu [modelo de amenaza](../basics/threat-modeling.md):

- **Nombres de host:** El nombre de host de tu sistema se comparte con las redes a las que te conectas. Debes evitar incluir términos identificativos como tu nombre o tu sistema operativo en tu nombre de host, en su lugar, cíñete a términos genéricos o cadenas de caracteres aleatorias.
- **Nombres de usuario:** Del mismo modo, tu nombre de usuario se utiliza de diversas maneras en todo el sistema. Considera la posibilidad de utilizar términos genéricos como "usuario" en lugar de tu nombre real.
- **Machine ID:** During installation, a unique machine ID is generated and stored on your device. Considera [configurarlo en un ID genérico](https://madaidans-insecurities.github.io/guides/linux-hardening.html#machine-id).

### Contador de sistema

El Proyecto Fedora [cuenta](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting) cuántos sistemas únicos acceden a sus réplicas utilizando una variable [`countme`](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting#Detailed_Description) en lugar de un ID único. Fedora hace esto para determinar la carga y aprovisionar mejores servidores para las actualizaciones cuando sea necesario.

Esta [opción](https://dnf.readthedocs.io/en/latest/conf_ref.html#options-for-both-main-and-repo) está actualmente desactivada por defecto. Recomendamos añadir `countme=false` en `/etc/dnf/dnf.conf` por si se habilita en el futuro. En sistemas que utilizan `rpm-ostree`, como Silverblue, la opción countme se desactiva enmascarando el temporizador [rpm-ostree-countme](https://fedoramagazine.org/getting-better-at-counting-rpm-ostree-based-systems).

openSUSE also uses a [unique ID](https://en.opensuse.org/openSUSE:Statistics) to count systems, which can be disabled by emptying the `/var/lib/zypp/AnonymousUniqueId` file.
