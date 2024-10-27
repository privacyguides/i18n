---
title: "Resumen de Qubes"
icon: simple/qubesos
description: Qubes es un sistema operativo basado en el aislamiento de aplicaciones en *qubes* (formalmente, máquinas virtuales) para una mayor seguridad.
---

[**Qubes OS**](../desktop.md#qubes-os) es un sistema operativo de código abierto, que utiliza el hipervisor [Xen](https://en.wikipedia.org/wiki/Xen) para proporcionar una fuerte seguridad en la computación de escritororio, a través de *qubes* aislados (que son máquinas virtuales). Puedes asignarle a cada *qube* un nivel de confianza basado en su propósito. Qubes OS proporciona seguridad al utilizar el aislamiento. Solo permite acciones en función de cada caso y, por tanto, es lo contrario de la [enumeración de la maldad](https://ranum.com/security/computer_security/editorials/dumb).

## ¿Cómo funciona Qubes OS?

Qubes utiliza la [compartimentación](https://qubes-os.org/intro) para mantener el sistema seguro. Qubes son creados de plantillas, las predeterminadas siendo para Fedora, Debian y [Whonix](../desktop.md#whonix). Qubes OS también permite crear *qubes* [desechables](https://qubes-os.org/doc/how-to-use-disposables) de un solo uso.

<details class="note" markdown>
<summary>El término <em>qubes</em> es actualizado gradualmente para evitar referirse a ellas como "máquinas virtuales".</summary>

Parte de la información que se encuentra aquí y en la documentación de Qubes OS puede contener lenguaje contradictorio, debido a que el término de "appVM" es gradualmente cambiado a "qube". Los Qubes no son máquinas virtuales completas, pero pueden contener funciones similares a las máquinas virtuales.

</details>

![Arquitectura Qubes](../assets/img/qubes/qubes-trust-level-architecture.png)
<figcaption>Qubes Arquitectura, Crédito: Qué es Qubes OS Introducción</figcaption>

Cada qube tiene un [borde coloreado](https://qubes-os.org/screenshots) que puede ayudar a seguir el rastro del dominio en que se ejecuta. Podrías, por ejemplo, usar un color específico para tu navegador bancario, mientras usas un color diferente para un navegador general no confiado.

![Borde coloreado](../assets/img/qubes/r4.0-xfce-three-domains-at-work.png)
<figcaption>Bordes de ventana de Qubes, Crédito: Capturas de pantalla de Qubes</figcaption>

## ¿Por qué utilizar Qubes?

Qubes OS es útil si tu [modelo de amenazas](../basics/threat-modeling.md) requiere un alto nivel de seguridad e isolación, como por ejemplo, si abrirás archivos poco confiables de fuentes desconocidas. Un motivo frecuente para utilizar Qubes OS es para abrir documentos desde fuentes desconocidas, pero la idea es que si un solo qube está comprometido, este no afecte al resto del sistema.

Qubes OS utiliza una Xen VM [dom0](https://wiki.xenproject.org/wiki/Dom0) para controlar otros *qubes* en el sistema operativo anfitrión, todos los cuales muestran ventanas de aplicaciones individuales dentro del entorno de escritorio de dom0. Hay muchos usos para este tipo de arquitectura. Aquí están algunas tareas que puedes realizar. Puedes ver qué tan seguros son estos procesadores, al incorporar varios pasos.

### Copiando y pegando texto

Puedes [copiar y pegar texto](https://qubes-os.org/doc/how-to-copy-and-paste-text) utilizando `qvm-copy-to-vm` o las siguientes instrucciones:

1. Presiona **Ctrl+C** para decirle al *qube* que quieres copias algo.
2. Presiona **Ctrl+Shift+C** para decirle al *qube* que ponga este buffer a disposición del portapapeles global.
3. Presiona **Ctrl+Shift+V** en el *qube* destinatario para hacer que el portapapeles global esté disponible.
4. Presiona **Ctrl+V** en el *qube* de destino para pegar el contenido en el buffer.

### Intercambio de archivos

Para copiar y pegar archivos y directorios (carpetas) entre un *qube* y otro, puedes usar la opción **Copiar a otro AppVM...** o **Mover a otro AppVM...**. La diferencia es que la opción **Mover** borrará el archivo original. Cualquier opción protegerá al portapapeles de ser filtrado a cualquier otro *qube*. Esto es más seguro que la transferencia de archivos guardados. Una computadora con tapón de aire puede ser forzada a analizar particiones o sistemas de archivos. Esto no es necesario con el sistema de copia inter-qube.

<details class="note" markdown>
<summary>Qubes no tiene su propios sistema de archivos.</summary>

Puedes [copiar y mover archivos](https://qubes-os.org/doc/how-to-copy-and-move-files) entre *qubes*. Al hacerlo, los cambios no son inmediatos y pueden deshacerse fácilmente en caso de accidente. Cuando ejecutas un *qube*, no tiene un sistema de archivos persistente. Puedes crear y eliminar archivos, pero los cambios son efímeros.

</details>

### Interacciones inter-VM

El [framework qrexec](https://qubes-os.org/doc/qrexec) es una parte central de Qubes que permite la comunicación entre dominios. Está construido sobre la librería Xen *vchan*, que facilita el [aislamiento mediante políticas](https://qubes-os.org/news/2020/06/22/new-qrexec-policy-system).

## Conectarse a Tor a través de una VPN

Nosotros [recomendamos](../advanced/tor-overview.md) conectarse a la red Tor a través de un proveedor de [VPN](../vpn.md), y, por suerte, Qubes hace que esto sea fácil de hacer con una combinación de ProxyVMs y Whonix.

Después de [crear una nueva ProxyVM](https://forum.qubes-os.org/t/configuring-a-proxyvm-vpn-gateway/19061) que se conecte a la VPN de tu elección, puedes encadenar tus qubes Whonix a ese ProxyVM **antes de** que se conecten a la red Tor, configurando la NetVM de tu Whonix **Gateway** (`sys-whonix`) a la ProxyVM recién creada.

Tus qubes deberían estar configurados de forma similar a esta:

| Nombre Qube     | Descripción Qube                                                                                   | NetVM           |
| --------------- | -------------------------------------------------------------------------------------------------- | --------------- |
| sys-net         | *Tu qube de red por defecto (preinstalado)*                                                        | *n/a*           |
| sys-firewall    | *Tu qube de red por defecto (preinstalado)*                                                        | sys-net         |
| ==sys-proxyvm== | La VPN ProxyVM que [creaste](https://forum.qubes-os.org/t/configuring-a-proxyvm-vpn-gateway/19061) | sys-firewall    |
| sys-whonix      | Tu MV Whonix Gateway                                                                               | ==sys-proxyvm== |
| anon-whonix     | Tu MV Whonix Workstation                                                                           | sys-whonix      |

## Recursos Adicionales

Para obtener información adicional, te animamos a consultar las extensas páginas de documentación de Qubes OS que se encuentran en el [Sitio Web Qubes OS](https://qubes-os.org/doc). Copias offline se pueden descargar desde el [repositorio de documentación ](https://github.com/QubesOS/qubes-doc)de Qubes OS.

- [Posiblemente el sistema operativo más seguro del mundo](https://opentech.fund/news/qubes-os-arguably-the-worlds-most-secure-operating-system-motherboard) (Open Technology Fund)
- [Compartimentación del software vs. separación física](https://invisiblethingslab.com/resources/2014/Software_compartmentalization_vs_physical_separation.pdf) (J. Rutkowska)
- [Particionando mi vida digital en dominios seguros](https://blog.invisiblethings.org/2011/03/13/partitioning-my-digital-life-into.html) (J. Rutkowska)
- [Artículos Relacionados](https://qubes-os.org/news/categories/#articles) (Qubes OS)
