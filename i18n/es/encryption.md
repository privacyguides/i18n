---
meta_title: "Recommended Encryption Software: VeraCrypt, Cryptomator, and OpenPGP - Privacy Guides"
title: "Software de Cifrado"
icon: material/file-lock
description: El cifrado de los datos es la única forma de controlar quién puede acceder a ellos. Estas herramientas le permiten cifrar sus correos electrónicos y cualquier otro archivo.
cover: encryption.webp
---

El **cifrado** es la única forma segura de controlar quién puede acceder a sus datos. Si actualmente no está utilizando software de cifrado para su disco duro, correos electrónicos o archivos, debería elegir una opción aquí.

## Multiplataforma

Las opciones listadas aquí están disponibles en múltiples plataformas y son geniales para crear copias de seguridad cifradas de tus datos.

### Cryptomator (Nube)

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-bug-outline: Ataques pasivos](basics/common-threats.md#security-and-privacy ""){.pg-orange}

<div class="admonition recommendation" markdown>

![Cryptomator logo](assets/img/encryption-software/cryptomator.svg){ align=right }

**Cryptomator** es una solución de cifrado diseñada para guardar archivos de forma privada en cualquier nube de [:material-server-network: Proveedor de Servicios](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }, eliminando la necesidad de confiar en que no accederán a tus archivos. Le permite crear bóvedas que se almacenan en una unidad virtual, cuyo contenido está cifrado y sincronizado con su proveedor de almacenamiento en la nube.

[:octicons-home-16: Página Principal](https://cryptomator.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://cryptomator.org/privacy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://docs.cryptomator.org){ .card-link title="Documentación" }
[:octicons-code-16:](https://github.com/cryptomator){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://cryptomator.org/donate){ .card-link title="Contribuir" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.cryptomator)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1560822163)
- [:simple-android: Android](https://cryptomator.org/android)
- [:fontawesome-brands-windows: Windows](https://cryptomator.org/downloads)
- [:simple-apple: macOS](https://cryptomator.org/downloads)
- [:simple-linux: Linux](https://cryptomator.org/downloads)
- [:simple-flathub: Flathub](https://flathub.org/apps/details/org.cryptomator.Cryptomator)

</details>

</div>

Cryptomator utiliza el cifrado AES-256 para cifrar tanto los archivos como los nombres de los archivos. Cryptomator no puede cifrar metadatos como las marcas de la fecha de acceso, modificación y creación, ni el número y tamaño de los archivos y carpetas.

Cryptomator es de uso gratuito en todas las plataformas de escritorio, así como en iOS en modo "solo lectura". Cryptomator ofrece aplicaciones de [pago](https://cryptomator.org/pricing) con funcionalidad completa en iOS y Android. La versión para Android puede adquirirse de forma anónima a través de [ProxyStore](https://cryptomator.org/coop/proxystore).

Algunas bibliotecas criptográficas de Cryptomator han sido [auditadas](https://community.cryptomator.org/t/has-there-been-a-security-review-audit-of-cryptomator/44) por Cure53. El alcance de las bibliotecas auditadas incluye: [cryptolib](https://github.com/cryptomator/cryptolib), [cryptofs](https://github.com/cryptomator/cryptofs), [siv-mode](https://github.com/cryptomator/siv-mode) y [cryptomator-objc-cryptor](https://github.com/cryptomator/cryptomator-objc-cryptor). La auditoría no se extendió a [cryptolib-swift](https://github.com/cryptomator/cryptolib-swift), que es una biblioteca utilizada por Cryptomator para iOS.

La documentación de Cryptomator detalla con más detalle su [objetivo de seguridad](https://docs.cryptomator.org/en/latest/security/security-target), la [arquitectura de seguridad](https://docs.cryptomator.org/en/latest/security/architecture) y las [mejores prácticas](https://docs.cryptomator.org/en/latest/security/best-practices) de uso.

### VeraCrypt (Disco)

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-target-account: Ataques dirigidos](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

<div class="admonition recommendation" markdown>

![VeraCrypt logo](assets/img/encryption-software/veracrypt.svg#only-light){ align=right }
![VeraCrypt logo](assets/img/encryption-software/veracrypt-dark.svg#only-dark){ align=right }

**VeraCrypt** es una utilidad de software gratuito con el código fuente disponible que se utiliza para el cifrado sobre la marcha. Puede crear un disco cifrado virtual dentro de un archivo, cifrar una partición o cifrar todo el dispositivo de almacenamiento con autenticación previa al arranque.

[:octicons-home-16: Página Principal](https://veracrypt.fr){ .md-button .md-button--primary }
[:octicons-info-16:](https://veracrypt.fr/en/Documentation.html){ .card-link title="Documentación" }
[:octicons-code-16:](https://veracrypt.fr/code){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://veracrypt.fr/en/Donation.html){ .card-link title="Contribuir" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:fontawesome-brands-windows: Windows](https://veracrypt.fr/en/Downloads.html)
- [:simple-apple: macOS](https://veracrypt.fr/en/Downloads.html)
- [:simple-linux: Linux](https://veracrypt.fr/en/Downloads.html)

</details>

</div>

VeraCrypt es una bifurcación del proyecto TrueCrypt ya descontinuado. Según sus desarrolladores, se implementaron mejoras de seguridad y se abordaron los problemas planteados por la auditoría inicial del código de TrueCrypt.

Al cifrar con VeraCrypt, tiene la opción de seleccionar entre diferentes [funciones hash](https://en.wikipedia.org/wiki/VeraCrypt#Encryption_scheme). Le sugerimos **únicamente** seleccionar [SHA-512](https://en.wikipedia.org/wiki/SHA-512) y seleccionar el [AES](https://en.wikipedia.org/wiki/Advanced_Encryption_Standard) como cifrado de bloque.

TrueCrypt ha sido [auditada varias veces](https://en.wikipedia.org/wiki/TrueCrypt#Security_audits), y VeraCrypt también ha sido [auditada por separado](https://en.wikipedia.org/wiki/VeraCrypt#VeraCrypt_audit).

## Cifrado del Sistema Operativo

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-target-account: Ataques dirigidos](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

Las soluciones de cifrado integradas en el sistema operativo suelen aprovechar las características de seguridad del hardware, como un [criptoprocesador seguro](basics/hardware.md#tpmsecure-cryptoprocessor). Por lo tanto, le recomendamos que utilice las soluciones de cifrado integradas en su sistema operativo. Para el cifrado multiplataforma, seguimos recomendando [las herramientas multiplataforma](#multi-platform) por su mayor flexibilidad y para evitar la dependencia del proveedor.

### BitLocker

<div class="admonition recommendation" markdown>

![BitLocker logo](assets/img/encryption-software/bitlocker.png){ align=right }

**BitLocker** es la solución de cifrado de volumen completo incluida con Microsoft Windows que utiliza el módulo de plataforma de confianza ([TPM](https://learn.microsoft.com/windows/security/information-protection/tpm/how-windows-uses-the-tpm)) para la seguridad basada en hardware.

[:octicons-info-16:](https://learn.microsoft.com/windows/security/information-protection/BitLocker/BitLocker-overview){ .card-link title="Documentación" }

</details>

</div>

BitLocker es [compatible oficialmente](https://support.microsoft.com/windows/turn-on-device-encryption-0c453637-bc88-5f74-5105-741561aae838) con las ediciones Pro, Enterprise y Education de Windows. Puede activarse en las ediciones Home siempre que cumplan los siguientes requisitos previos.

<details class="example" markdown>
<summary>Activar BitLocker en Windows Home</summary>

Para habilitar BitLocker en las ediciones "Home" de Windows, debe tener particiones formateadas con una [Tabla de Particiones GUID](https://en.wikipedia.org/wiki/GUID_Partition_Table) y disponer de un módulo TPM dedicado (v1.2, 2.0+). Es posible que tenga que [desactivar la funcionalidad que no es de Bitlocker "Cifrado del dispositivo"](https://discuss.privacyguides.net/t/enabling-bitlocker-on-the-windows-11-home-edition/13303/5) (que es inferior, ya que envía su clave de recuperación a los servidores de Microsoft) si ya está habilitada en su dispositivo antes de seguir esta guía.

1. Abra un símbolo del sistema y verifique el formato de la tabla de particiones de su unidad con el siguiente comando. Debería ver "**GPT**" listado bajo "Partition Style":

    ```powershell
    powershell Get-Disk
    ```

2. Ejecute este comando (en un símbolo del sistema ejecutado como administrador) para verificar su versión de TPM. Debería ver `2.0` o `1.2` junto a `SpecVersion`:

    ```powershell
    powershell Get-WmiObject -Namespace "root/cimv2/security/microsofttpm" -Class WIN32_tpm
    ```

3. Accede a las [Opciones Avanzadas de Inicio](https://support.microsoft.com/windows/advanced-startup-options-including-safe-mode-b90e7808-80b5-a291-d4b8-1a1af602b617). Debe reiniciar mientras pulsa la tecla F8 antes de que se inicie Windows y entrar en el símbolo del sistema ** en **Solucionar problemas** → **Opciones avanzadas** → **Símbolo del sistema**.
4. Inicie sesión con su cuenta de administrador y escriba esto en el símbolo del sistema para iniciar el cifrado:

    ```powershell
    manage-bde -on c: -used
    ```

5. Cierre el símbolo del sistema y continúe con el arranque normal de Windows.
6. Abra un símbolo del sistema como administrador y ejecute los siguientes comandos:

    ```powershell
    manage-bde c: -protectors -add -rp -tpm
    manage-bde -protectors -enable c:
    manage-bde -protectors -get c: > %UserProfile%\Desktop\BitLocker-Recovery-Key.txt
    ```

<div class="admonition tip" markdown>
<p class="admonition-title">Consejo</p>

    Haga una copia de seguridad de `BitLocker-Recovery-Key.txt` en su escritorio para un dispositivo de almacenamiento independiente. La pérdida de este código de recuperación puede resultar en la pérdida de datos.

</div>

</details>

### FileVault

<div class="admonition recommendation" markdown>

![FileVault logo](assets/img/encryption-software/filevault.png){ align=right }

**FileVault** es la solución de cifrado de volúmenes sobre la marcha integrada en macOS. FileVault aprovecha las [capacidades de seguridad de hardware](os/macos-overview.md#hardware-security) presentes en un Apple Silicon SoC o T2 Security Chip.

[:octicons-info-16:](https://support.apple.com/guide/mac-help/encrypt-mac-data-with-filevault-mh11785/mac){ .card-link title="Documentación" }

</details>

</div>

Le recomendamos que no utilice su cuenta de iCloud para la recuperación; en su lugar, debe almacenar de forma segura una clave de recuperación local en un dispositivo de almacenamiento independiente.

### Linux Unified Key Setup

<div class="admonition recommendation" markdown>

![LUKS logo](assets/img/encryption-software/luks.png){ align=right }

**LUKS** es el método FDE por defecto para Linux. Puede utilizarse para cifrar volúmenes completos, particiones o crear contenedores cifrados.

[:octicons-repo-16: Repositorio](https://gitlab.com/cryptsetup/cryptsetup#what-the-){ .md-button .md-button--primary }
[:octicons-info-16:](https://gitlab.com/cryptsetup/cryptsetup/-/wikis/home){ .card-link title="Documentación" }
[:octicons-code-16:](https://gitlab.com/cryptsetup/cryptsetup){ .card-link title="Código Fuente" }

</details>

</div>

<details class="example" markdown>
<summary>Crear y abrir contenedores cifrados</summary>

```bash
dd if=/dev/urandom of=/path-to-file bs=1M count=1024 status=progress
sudo cryptsetup luksFormat /path-to-file
```

#### Abrir contenedores cifrados

Recomendamos abrir los contenedores y volúmenes con `udisksctl` ya que utiliza [Polkit](https://en.wikipedia.org/wiki/Polkit). La mayoría de los gestores de archivos, como los incluidos en los entornos de escritorio más populares, pueden desbloquear archivos cifrados. Herramientas como [udiskie](https://github.com/coldfix/udiskie) pueden ejecutarse en la bandeja del sistema y proporcionar una interfaz de usuario útil.

```bash
udisksctl loop-setup -f /path-to-file
udisksctl unlock -b /dev/loop0
```

</details>

<div class="admonition note" markdown>
<p class="admonition-title">Recuerde hacer copias de seguridad de las cabeceras de volumen</p>

Le recomendamos que siempre haga [copias de seguridad de las cabeceras LUKS](https://wiki.archlinux.org/title/Dm-crypt/Device_encryption#Backup_and_restore) en caso de fallo parcial de la unidad. Esto se puede hacer con:

```bash
cryptsetup luksHeaderBackup /dev/device --header-backup-file /mnt/backup/file.img
```

</div>

## Línea de Comandos

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-target-account: Ataques dirigidos](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}

Las herramientas con interfaces de línea de comandos son útiles para integrar <a href=https://es.wikipedia.org/wiki/Script_de_shell">scripts de shell</a>.

### Kryptor

<div class="admonition recommendation" markdown>

![Kryptor logo](assets/img/encryption-software/kryptor.png){ align=right }

**Kryptor** es una herramienta de cifrado y firma de archivos gratuita y de código abierto que hace uso de algoritmos criptográficos modernos y seguros. Pretende ser una versión mejorada de [age](https://github.com/FiloSottile/age) y [Minisign](https://jedisct1.github.io/minisign/) para ofrecer una alternativa sencilla y más fácil a GPG.

[:octicons-home-16: Página Principal](https://kryptor.co.uk){ .md-button .md-button--primary }
[:octicons-eye-16:](https://kryptor.co.uk/features#privacy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://kryptor.co.uk/tutorial){ .card-link title="Documentación" }
[:octicons-code-16:](https://github.com/samuel-lucas6/Kryptor){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://kryptor.co.uk/#donate){ .card-link title="Contribuir" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:fontawesome-brands-windows: Windows](https://kryptor.co.uk)
- [:simple-apple: macOS](https://kryptor.co.uk)
- [:simple-linux: Linux](https://kryptor.co.uk)

</details>

</div>

### Tomb

<div class="admonition recommendation" markdown>

![Tomb logo](assets/img/encryption-software/tomb.png){ align=right }

**Tomb** es un empaquetador de shell de línea de comandos para LUKS. Admite esteganografía a través de [herramientas de terceros](https://dyne.org/software/tomb/#advanced-usage).

[:octicons-home-16: Página Principal](https://dyne.org/software/tomb){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/dyne/Tomb/wiki){ .card-link title="Documentación" }
[:octicons-code-16:](https://github.com/dyne/Tomb){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://dyne.org/donate){ .card-link title="Contribuir" }

</details>

</div>

## OpenPGP

<small>Protege contra la(s) siguiente(s) amenaza(s):</small>

- [:material-target-account: Ataques dirigidos](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}
- [:material-bug-outline: Ataques pasivos](basics/common-threats.md#security-and-privacy ""){.pg-orange}
- [:material-server-network: Proveedores de servicios](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

OpenPGP es a veces necesario para tareas específicas como la firma digital y el cifrado de correo electrónico. PGP tiene muchas funciones y es [complejo](https://latacora.micro.blog/2019/07/16/the-pgp-problem.html) ya que existe desde hace mucho tiempo. Para tareas como firmar o cifrar archivos, sugerimos las opciones anteriores.

Al cifrar con PGP, tiene la opción de configurar diferentes opciones en su archivo `gpg.conf`. Recomendamos utilizar las opciones estándar especificadas en las [Preguntas Frecuentes de los Usuarios de GnuPG](https://gnupg.org/faq/gnupg-faq.html#new_user_gpg_conf).

<div class="admonition tip" markdown>
<p class="admonition-title">Utilice future defaults al generar una clave</p>

Al [generar claves](https://gnupg.org/gph/en/manual/c14.html) sugerimos usar el comando `future-default` ya que esto instruirá a GnuPG a usar criptografía moderna como [Curve25519](https://es.wikipedia.org/wiki/Curve25519#Popularidad) y [Ed25519](https://ed25519.cr.yp.to):

```bash
gpg --quick-gen-key alice@example.com future-default
```

</div>

### GNU Privacy Guard

<div class="admonition recommendation" markdown>

![GNU Privacy Guard logo](assets/img/encryption-software/gnupg.svg){ align=right }

**GNUPG** es una alternativa con licencia GPL a la suite de software criptográfico PGP. GnuPG cumple con [RFC 4880](https://tools.ietf.org/html/rfc4880), que es la especificación actual del IETF de OpenPGP. El proyecto GnuPG ha estado trabajando en un [borrador actualizado](https://datatracker.ietf.org/doc/draft-ietf-openpgp-crypto-refresh) en un intento de modernizar OpenPGP. GnuPG forma parte del proyecto de software GNU de la Fundación para el Software Libre y ha recibido un importante [funding](https://gnupg.org/blog/20220102-a-new-future-for-gnupg.html) del gobierno alemán.

[:octicons-home-16: Página Principal](https://gnupg.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gnupg.org/privacy-policy.html){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://gnupg.org/documentation/index.html){ .card-link title="Documentación" }
[:octicons-code-16:](https://git.gnupg.org/cgi-bin/gitweb.cgi?p=gnupg.git){ .card-link title="Código Fuente" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.sufficientlysecure.keychain)
- [:fontawesome-brands-windows: Windows](https://gpg4win.org/download.html)
- [:simple-apple: macOS](https://gpgtools.org)
- [:simple-linux: Linux](https://gnupg.org/download/index.html#binary)

</details>

</div>

### GPG4win

<div class="admonition recommendation" markdown>

![GPG4win logo](assets/img/encryption-software/gpg4win.svg){ align=right }

**GPG4win** es un paquete para Windows de [Intevation y g10 Code](https://gpg4win.org/impressum.html). Incluye [varias herramientas](https://gpg4win.org/about.html) que pueden ayudarle a utilizar GPG en Microsoft Windows. El proyecto fue iniciado y originalmente [financiado por](https://web.archive.org/web/20190425125223/https://joinup.ec.europa.eu/news/government-used-cryptography) la Oficina Federal de Seguridad de la Información (BSI) de Alemania en 2005.

[:octicons-home-16: Página Principal](https://gpg4win.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gpg4win.org/privacy-policy.html){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://gpg4win.org/documentation.html){ .card-link title="Documentación" }
[:octicons-code-16:](https://git.gnupg.org/cgi-bin/gitweb.cgi?p=gpg4win.git;a=summary){ .card-link title="Código Fuente" }
[:octicons-heart-16:](https://gpg4win.org/donate.html){ .card-link title="Contribuir" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:fontawesome-brands-windows: Windows](https://gpg4win.org/download.html)

</details>

</div>

### GPG Suite

<div class="admonition recommendation" markdown>

![GPG Suite logo](assets/img/encryption-software/gpgsuite.png){ align=right }

**GPG Suite** proporciona soporte OpenPGP para [Apple Mail](email-clients.md#apple-mail-macos) y otros clientes de correo electrónico en macOS.

Recomendamos echar un vistazo a sus [Primeros pasos](https://gpgtools.tenderapp.com/kb/how-to/first-steps-where-do-i-start-where-do-i-begin-setup-gpgtools-create-a-new-key-your-first-encrypted-email) y [Base de conocimientos](https://gpgtools.tenderapp.com/kb) para obtener ayuda.

[:octicons-home-16: Página Principal](https://gpgtools.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gpgtools.org/privacy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://gpgtools.tenderapp.com/kb){ .card-link title="Documentación" }
[:octicons-code-16:](https://github.com/GPGTools){ .card-link title="Código Fuente" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-apple: macOS](https://gpgtools.org)

</details>

</div>

Actualmente, GPG Suite [no](https://gpgtools.com/sequoia) tiene una versión estable para macOS Sonoma y posteriores.

### OpenKeychain

<div class="admonition recommendation" markdown>

![OpenKeychain logo](assets/img/encryption-software/openkeychain.svg){ align=right }

**OpenKeychain** es una implementación de GnuPG para Android. Es comúnmente requerido por clientes de correo como [Thunderbird](email-clients.md#thunderbird), [FairEmail](email-clients.md#fairemail-android), y otras aplicaciones Android para proporcionar soporte de cifrado.

[:octicons-home-16: Página Principal](https://openkeychain.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://openkeychain.org/help/privacy-policy){ .card-link title="Política de Privacidad" }
[:octicons-info-16:](https://openkeychain.org/faq){ .card-link title="Documentación" }
[:octicons-code-16:](https://github.com/open-keychain/open-keychain){ .card-link title="Código Fuente" }

<details class="downloads" markdown>
<summary>Downloads "Descargas"</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.sufficientlysecure.keychain)

</details>

</div>

Cure53 completó una [auditoría de seguridad](https://openkeychain.org/openkeychain-3-6) de OpenKeychain 3.6 en octubre de 2015. La auditoría publicada y las soluciones de OpenKeychain a los problemas planteados en la auditoría pueden consultarse [aquí](https://github.com/open-keychain/open-keychain/wiki/cure53-Security-Audit-2015).

## Criterios

**Por favor, tenga en cuenta que no estamos afiliados con ninguno de los proyectos que recomendamos.** Además de [nuestros criterios estándar](about/criteria.md), hemos desarrollado un conjunto claro de requisitos que nos permiten ofrecer recomendaciones objetivas. Sugerimos que usted se familiarice con esta lista, antes de decidir utilizar un proyecto y realizar su propia investigación para asegurarse de que es la elección ideal para usted.

### Requisitos Mínimos

- Las aplicaciones de cifrado multiplataforma deben ser de código abierto.
- Las aplicaciones de cifrado de archivos deben permitir el descifrado en Linux, macOS y Windows.
- Las aplicaciones de cifrado de discos externos deben permitir el descifrado en Linux, macOS y Windows.
- Las aplicaciones de cifrado de disco interno (OS) deben ser multiplataforma o estar integradas en el sistema operativo de forma nativa.

### Mejor Caso

Nuestro criterio del mejor caso representa lo que nos gustaría ver del proyecto perfecto en esta categoría. Es posible que nuestras recomendaciones no incluyan todas o algunas de estas funciones, pero las que sí las incluyan pueden estar mejor clasificadas que otras en esta página.

- Las aplicaciones de cifrado del sistema operativo (FDE) deben utilizar seguridad de hardware como un TPM o Secure Enclave.
- Las aplicaciones de cifrado de archivos deben ser compatibles con plataformas móviles, ya sean propias o de terceros.
