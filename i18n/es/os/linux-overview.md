---
title: Resumen de Linux
icon: simple/linux
description: Linux es un sistema operativo de escritorio alternativo, de código abierto y centrado en la privacidad, pero no todas las distribuciones son iguales.
---

**Linux** es un sistema operativo de escritorio alternativo, de código abierto y centrado en la privacidad. Frente a la telemetría omnipresente y otras tecnologías que atentan contra la privacidad en los principales sistemas operativos, Linux de escritorio ha seguido siendo la opción clara para quienes buscan un control total sobre sus ordenadores desde la base.

En general, nuestro sitio web utiliza el término "Linux" para describir las distribuciones Linux de **escritorio**. En esta página no se tratan otros sistemas operativos que también utilizan el núcleo Linux, como ChromeOS, Android y Qubes OS.

[Nuestras recomendaciones de Linux: :material-arrow-right-drop-circle:](../desktop.md ""){.md-button}

## Notas de Seguridad

Linux presenta algunos problemas de seguridad importantes que deberías conocer. A pesar de estos inconvenientes, las distribuciones Linux de escritorio siguen siendo estupendas para la mayoría de la gente que desea:

- Evitar la telemetría que, regularmente, viene con los sistemas operativos propietarios
- Mantener la [libertad de software](https://gnu.org/philosophy/free-sw.en.html#four-freedoms)
- Utiliza sistemas centrados en la privacidad como [Whonix](../desktop.md#whonix) o [Tails](../desktop.md#tails)

### Seguridad de Código Abierto

Es un [error común](../basics/common-misconceptions.md#open-source-software-is-always-secure-or-proprietary-software-is-more-secure) pensar que Linux y otros programas de código abierto son intrínsecamente seguros simplemente porque el código fuente está disponible. Se espera que la verificación comunitaria se realice con regularidad, pero este no siempre es [el caso](https://seirdy.one/posts/2022/02/02/floss-security).

En realidad, la seguridad de las distribuciones depende de varios factores, como la actividad del proyecto, la experiencia de los desarrolladores, el nivel de rigor aplicado a las revisiones del código y la frecuencia con la que se presta atención a partes concretas del código base, que pueden permanecer intactas durante años.

### Elementos de Seguridad Ausentes

Por el momento, Linux de escritorio [está por detrás de alternativas](https://discussion.fedoraproject.org/t/fedora-strategy-2028-proposal-fedora-linux-is-as-secure-as-macos/46899/9) como macOS o Android cuando se trata de ciertas características de seguridad. Esperamos ver mejoras en estos ámbitos en el futuro.

- El **arranque verificado ** en Linux no es tan robusto como alternativas como el [Arranque Seguro](https://support.apple.com/guide/security/secac71d5623/web) de Apple o el [Arranque Verificado](https://source.android.com/security/verifiedboot) de Android. El arranque verificado evita la manipulación persistente por parte de malware y [los ataques evil maid](https://en.wikipedia.org/wiki/Evil_Maid_attack), pero sigue [sin estar disponible en gran medida incluso en las distribuciones más avanzadas](https://discussion.fedoraproject.org/t/has-silverblue-achieved-verified-boot/27251/3).

- **Un aislamiento fuerte** para aplicaciones en Linux que es muy deficiente, incluso con aplicaciones en contenedores como Flatpaks o soluciones de aislamiento como Firejail. Flatpak es la utilidad de aislamiento de procesos más prometedora para Linux hasta el momento, pero sigue siendo deficiente en muchas áreas y permite [defaults inseguros](https://flatkill.org/2020) que permiten a la mayoría de las aplicaciones eludir trivialmente su aislamiento de procesos.

Además, Linux se queda atrás en la implementación de [mitigaciones de exploits](https://madaidans-insecurities.github.io/linux.html#exploit-mitigations) que ahora son estándar en otros sistemas operativos, como Protección de Código Arbitrario en Windows o Tiempo de Ejecución Reforzado en macOS. Además, la mayoría de los programas Linux y el propio Linux están codificados en lenguajes poco seguros para la memoria. Los fallos de corrupción de memoria son responsables de la [mayoría de las vulnerabilidades](https://msrc.microsoft.com/blog/2019/07/a-proactive-approach-to-more-secure-code) corregidas y a las que se asigna un CVE. Aunque esto también es cierto para Windows y macOS, están avanzando rápidamente en la adopción de lenguajes seguros para la memoria como Rust y Swift, respectivamente.

## Elegir tu distribución

No todas las distribuciones Linux son iguales. Nuestra [página de recomendaciones de Linux](../desktop.md) no pretende ser una fuente autoritaria sobre qué distribución debes utilizar, pero nuestras recomendaciones *están* alineadas con las siguientes directrices. Estas son algunas cosas que debes tener en cuenta a la hora de elegir una distribución:

### Ciclo de lanzamiento

Recomendamos encarecidamente que elijas distribuciones que permanezcan cerca de los lanzamientos estables del software de origen, comúnmente denominadas como distribuciones de lanzamiento continuo. Esto se debe a que las distribuciones de lanzamiento de ciclo congelado, normalmente no actualizan las versiones de sus paquetes y se encuentran detrás en actualizaciones de seguridad.

Para las distribuciones congeladas como [Debian](https://debian.org/security/faq#handling), se espera que los encargados de mantener los paquetes adapten los parches para corregir vulnerabilidades, en lugar de actualizar el software a la "siguiente versión" lanzada por el desarrollador original. Algunas correcciones de seguridad (en particular para el software menos popular) [no](https://arxiv.org/abs/2105.14565) reciben un [CVE ID](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures) en absoluto y por lo tanto no llegan a la distribución con este modelo de parches. Como resultado, las correcciones de seguridad menores a veces se retrasan hasta la siguiente versión principal.

No creemos que retener paquetes y aplicar parches provisionales sea una buena idea, ya que se aparta de la forma en que el desarrollador podría haber previsto que funcionara el software. [Richard Brown](https://rootco.de/aboutme) tiene una presentación sobre esto:

- [Los Lanzamientos Regulares están Mal, Rueda por tu vida](https://youtu.be/i8c0mg_mS7U) <small>(YouTube)</small>

### Actualizaciones Tradicionales vs. Atómicas

Tradicionalmente, las distribuciones Linux se actualizan mediante la actualización secuencial de los paquetes deseados. Las actualizaciones tradicionales, como las utilizadas en las distribuciones basadas en Fedora, Arch Linux y Debian, pueden ser menos fiables si se produce un error durante la actualización.

En cambio, las distribuciones que utilizan actualizaciones atómicas las aplican en su totalidad o no las aplican en absoluto. En una distribución atómica, si se produce un error durante la actualización (tal vez debido a un fallo de alimentación), no se modifica nada en el sistema.

El método de actualización atómica puede lograr la fiabilidad con este modelo y se utiliza para [distribuciones](../desktop.md#atomic-distributions) como Silverblue y NixOS. [Adam Šamalik](https://twitter.com/adsamalik) brinda una presentación sobre cómo `rpm-ostree` funciona con Silverblue:

- [Probemos Fedora Silverblue: ¡un sistema operativo de escritorio inmutable! - Adam Šamalík](https://youtu.be/-hpV5l-gJnQ) <small>(YouTube)</small>

### Distribuciones "enfocadas en la seguridad"

A menudo existe cierta confusión entre las distribuciones "enfocadas en la seguridad" y las distribuciones "pentesting". Una búsqueda rápida de "la distribución de Linux más segura" suele arrojar resultados como Kali Linux, Black Arch o Parrot OS. Estas distribuciones son distribuciones de pruebas de penetración ofensivas que incluyen herramientas para probar otros sistemas. Estas no incluyen ninguna "seguridad adicional" o mitigaciones defensivas destinadas a un uso regular.

### Distribuciones basadas en Arch Linux

Arch y las distribuciones basadas en Arch no son recomendables para quienes se inician en Linux (independientemente de la distribución), ya que requieren un [mantenimiento del sistema](https://wiki.archlinux.org/title/System_maintenance) regular. Arch no dispone de un mecanismo de actualización de la distribución para las opciones de software subyacentes. En consecuencia, hay que estar al tanto de las tendencias actuales y adoptar las tecnologías por cuenta propia a medida que van sustituyendo a las prácticas más antiguas.

Para un sistema seguro, también se espera que tengas suficientes conocimientos de Linux para configurar correctamente la seguridad de su sistema, como adoptar un sistema de [control de acceso obligatorio](#mandatory-access-control), configurar listas negras de [módulos del núcleo](https://en.wikipedia.org/wiki/Loadable_kernel_module#Security), endurecer los parámetros de arranque, manipular los parámetros de [sysctl](https://en.wikipedia.org/wiki/Sysctl) y saber qué componentes necesitan, como [Polkit](https://en.wikipedia.org/wiki/Polkit).

Cualquiera que utilice el [Repositorio de Usuario de Arch (AUR)](https://wiki.archlinux.org/title/Arch_User_Repository) **debe** sentirse cómodo auditando los PKGBUILDs que descargue de ese servicio. Los paquetes AUR son contenidos producidos por la comunidad y no son examinados de ninguna manera, y por lo tanto son vulnerables a software [:material-package-variant-closed-remove: Ataques a la Cadena de Suministro](../basics/common-threats.md#attacks-against-certain-organizations ""){.pg-viridian}, lo que de hecho ha ocurrido [en el pasado](https://bleepingcomputer.com/news/security/malware-found-in-arch-linux-aur-package-repository).

El AUR debe utilizarse siempre con moderación, y a menudo hay muchos malos consejos en diversas páginas que dirigen a la gente a utilizar ciegamente [AUR helpers](https://wiki.archlinux.org/title/AUR_helpers) sin suficiente advertencia. Se aplican advertencias similares al uso de Archivos de Paquetes Personales (PPA) de terceros en distribuciones basadas en Debian o Proyectos Comunitarios (COPR) en Fedora.

Si tienes experiencia con Linux y deseas utilizar una distribución basada en Arch, generalmente recomendamos Arch Linux de línea principal sobre cualquiera de sus derivados.

Además, estamos en **contra** de usar estos dos derivados de Arch específicamente:

- **Manjaro**: Esta distribución retiene los paquetes durante 2 semanas para asegurarse de que sus propios cambios no se rompan, no para asegurarse de que el flujo ascendente sea estable. Cuando se utilizan paquetes AUR, suelen compilarse con las últimas [bibliotecas](https://en.wikipedia.org/wiki/Library_(computing)) de los repositorios de Arch.
- **Garuda**: Utilizan [Chaotic-AUR](https://aur.chaotic.cx) que compila automáticamente y a ciegas paquetes del AUR. No existe ningún proceso de verificación que garantice que los paquetes AUR no sufran ataques en la cadena de suministro.

### Núcleo Linux-libre y distribuciones "Libre"

Recomendamos **no** utilizar el kernel Linux-libre, ya que [elimina las mitigaciones de seguridad](https://phoronix.com/news/GNU-Linux-Libre-5.7-Released) y [suprime las advertencias del kernel](https://news.ycombinator.com/item?id=29674846) sobre microcódigo vulnerable.

### Control de acceso obligatorio

El control de acceso obligatorio es un conjunto de controles de seguridad adicionales que ayudan a confinar partes del sistema como aplicaciones y servicios del sistema. Las dos formas comunes de control de acceso obligatorio que se encuentran en las distribuciones de Linux son [SELinux](https://github.com/SELinuxProject) y [AppArmor](https://apparmor.net). Fedora y Tumbleweed utilizan SELinux por defecto, y Tumbleweed ofrece una opción en su instalador para elegir AppArmor en su lugar.

SELinux en [Fedora](https://docs.fedoraproject.org/en-US/quick-docs/selinux-getting-started) limita los contenedores Linux, las máquinas virtuales y los demonios de servicio de forma predeterminada. AppArmor es utilizado por el demonio snap para los snaps de[aislamiento](https://snapcraft.io/docs/security-sandboxing) que tienen confinamiento [estricto](https://snapcraft.io/docs/snap-confinement) como [Firefox](https://snapcraft.io/firefox). Existe un esfuerzo de la comunidad para confinar más partes del sistema en Fedora con el grupo de interés especial [ConfinedUsers](https://fedoraproject.org/wiki/SIGs/ConfinedUsers).

## Recomendaciones Generales

### Cifrado de Unidad

La mayoría de las distribuciones de Linux tienen una opción dentro de su instalador para habilitar [LUKS](../encryption.md#linux-unified-key-setup) FDE. Si esta opción no se configura en el momento de la instalación, tendrás que hacer una copia de seguridad de tus datos y volver a instalarla, ya que el cifrado se aplica después de [particionar el disco](https://en.wikipedia.org/wiki/Disk_partitioning), pero antes de formatear [los sistemas de archivos](https://en.wikipedia.org/wiki/File_system). También te sugerimos que borres de forma segura tu dispositivo de almacenamiento:

- [Borrado Seguro de Datos :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/05/25/secure-data-erasure)

### Swap

Considera utilizar [ZRAM](https://wiki.archlinux.org/title/Zram#Using_zram-generator) en lugar de un archivo o partición de swap tradicional para evitar la escritura de datos de memoria potencialmente sensibles en el almacenamiento persistente (y mejorar el rendimiento). Las distribuciones basadas en Fedora [utilizan ZRAM por defecto](https://fedoraproject.org/wiki/Changes/SwapOnZRAM).

Si necesitas la función de suspensión en disco (hibernación), tendrás que utilizar un archivo o partición de swap tradicional. Asegúrate de que cualquier espacio de swap que tengas en un dispositivo de almacenamiento persistente esté [cifrado ](https://wiki.archlinux.org/title/Dm-crypt/Swap_encryption) como mínimo para mitigar algunas de estas amenazas.

### Firmware de Propietario (Actualizaciones de Microcódigo)

Algunas distribuciones de Linux (como las basadas en [Linux-libre](https://en.wikipedia.org/wiki/Linux-libre)o las DIY) no incluyen las actualizaciones de [microcódigo](https://en.wikipedia.org/wiki/Microcode) de propietario que parchean vulnerabilidades de seguridad críticas. Algunos ejemplos notables de estas vulnerabilidades son [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability)), [Meltdown](https://en.wikipedia.org/wiki/Meltdown_(security_vulnerability)), [SSB](https://en.wikipedia.org/wiki/Speculative_Store_Bypass), [Foreshadow](https://en.wikipedia.org/wiki/Foreshadow), [MDS](https://en.wikipedia.org/wiki/Microarchitectural_Data_Sampling), [SWAPGS](https://en.wikipedia.org/wiki/SWAPGS_(security_vulnerability)) y otras [vulnerabilidades de hardware](https://kernel.org/doc/html/latest/admin-guide/hw-vuln/index.html).

Nosotros **recomendamos encarecidamente** que instales las actualizaciones de microcódigo, ya que contienen importantes parches de seguridad para la CPU que no pueden mitigarse totalmente sólo con software. Tanto Fedora como openSUSE aplican actualizaciones de microcódigo por defecto.

### Actualizaciones

La mayoría de las distribuciones de Linux instalan automáticamente las actualizaciones o te recuerdan que debes hacerlo. Es importante mantener el sistema operativo actualizado para que el software esté parcheado cuando se detecte una vulnerabilidad.

Algunas distribuciones (especialmente las dirigidas a usuarios avanzados) son más básicas y esperan que hagas las cosas tú mismo (por ejemplo, Arch o Debian). Con estas distribuciones será necesario ejecutar manualmente el "gestor de paquetes" (`apt`, `pacman`, `dnf`, etc.) para recibir actualizaciones de seguridad importantes.

Además, algunas distribuciones no descargan automáticamente las actualizaciones de firmware. Para ello, deberás instalar [`fwupd`](https://wiki.archlinux.org/title/Fwupd).

### Controles de Permisos

Los entornos de escritorio (DEs) que admiten el protocolo de visualización [Wayland](https://wayland.freedesktop.org) son [más seguros](https://lwn.net/Articles/589147) que los que solo admiten X11. Sin embargo, no todos los DEs aprovechan al máximo las mejoras de seguridad de la arquitectura de Wayland.

Por ejemplo, GNOME tiene una notable ventaja en seguridad comparado con otras DEs al implementar controles de permisos para software de terceros que intenta [capturar tu pantalla](https://gitlab.gnome.org/GNOME/gnome-shell/-/issues/3943). Es decir, cuando una aplicación de terceros intenta capturar tu pantalla, se te pide permiso para compartir tu pantalla con la aplicación.

<figure markdown>
  Permisos de Captura de Pantalla](../assets/img/linux/screenshot_permission.png){ width="450" }
 <figcaption>Diálogo de permisos de captura de pantalla de GNOME</figcaption>
</figure>

Muchas alternativas aún no ofrecen estos mismos controles de permisos,[^1] mientras que otras están esperando a que Wayland implemente estos controles.[^2]

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
- **ID de Máquina:** Durante la instalación, se genera un ID de máquina único que se almacena en tu dispositivo. Considera [configurarlo en un ID genérico](https://madaidans-insecurities.github.io/guides/linux-hardening.html#machine-id).

### Contador de sistema

El Proyecto Fedora [cuenta](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting) cuántos sistemas únicos acceden a sus réplicas utilizando una variable [`countme`](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting#Detailed_Description) en lugar de un ID único. Fedora hace esto para determinar la carga y aprovisionar mejores servidores para las actualizaciones cuando sea necesario.

Esta [opción](https://dnf.readthedocs.io/en/latest/conf_ref.html#options-for-both-main-and-repo) está actualmente desactivada por defecto. Recomendamos añadir `countme=false` en `/etc/dnf/dnf.conf` por si se habilita en el futuro. En sistemas que utilizan `rpm-ostree` como Silverblue, la opción `countme` se desactiva enmascarando el temporizador [rpm-ostree-countme](https://fedoramagazine.org/getting-better-at-counting-rpm-ostree-based-systems).

openSUSE también utiliza un [ID único](https://en.opensuse.org/openSUSE:Statistics) para contar los sistemas, que puede desactivarse vaciando el archivo `/var/lib/zypp/AnonymousUniqueId`.

[^1]: KDE tiene actualmente una propuesta abierta para añadir controles para capturas de pantalla: <https://invent.kde.org/plasma/xdg-desktop-portal-kde/-/issues/7>
[^2]: Sway está esperando a añadir controles de seguridad específicos hasta que "sepa cómo va a funcionar la seguridad en su conjunto" en Wayland: <https://github.com/swaywm/sway/issues/5118#issuecomment-600054496>
