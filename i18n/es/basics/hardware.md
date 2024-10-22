---
title: Eligiendo Tu Hardware
icon: material/chip
description: El software no es lo único importante; aprende sobre las herramientas de hardware que puedes utilizar a diario para proteger tu privacidad.
---

Cuando se habla sobre privacidad, no se piensa tanto en el hardware como en el software que utilizamos. Tu hardware debe ser considerado como la base sobre la que construirás el resto de tu configuración de privacidad.

## Eligiendo una computadora

Los componentes internos de tus dispositivos procesan y almacenan toda tu información digital. Es importante que todos los dispositivos cuenten con soporte de parte del fabricante y los desarrolladores, con la recepción de actualizaciones de seguridad.

### Programas de seguridad del hardware

Algunos dispositivos tienen un "programa de seguridad del hardware", que consiste en una colaboración entre los proveedores sobre las mejores prácticas y recomendaciones al momento de diseñar un hardware, por ejemplo:

- [Los equipos de núcleo seguro de Windows](https://learn.microsoft.com/en-us/windows-hardware/design/device-experiences/oem-highly-secure-11) cumplen con unos criterios superiores de seguridad especificados por Microsoft. Estas protecciones no aplican únicamente a los usuarios de Windows; los usuarios de otros sistemas operativos pueden aprovechar características como la [protección DMA](https://learn.microsoft.com/en-us/windows/security/information-protection/kernel-dma-protection-for-thunderbolt) y la capacidad de desconfiar completamente de los certificados de Microsoft.
- [Android Ready SE](https://developers.google.com/android/security/android-ready-se) es una colaboración entre proveedores para garantizar que sus dispositivos siguen las [mejores prácticas](https://source.android.com/docs/security/best-practices/hardware) e incluyen almacenamiento respaldado por hardware a prueba de manipulaciones para cosas como las claves de cifrado.
- La ejecución de macOS en un SoC de Apple aprovecha las ventajas de la [seguridad del hardware](../os/macos-overview.md#hardware-security) que pueden no estar disponibles con sistemas operativos de terceros.
- La [seguridad de ChromeOS](https://chromium.org/chromium-os/developer-library/reference/security/security-whitepaper) es óptima cuando se ejecuta en un Chromebook, ya que puede hacer uso de las funciones de hardware disponibles, como la [raíz de confianza de hardware](https://chromium.org/chromium-os/developer-library/reference/security/security-whitepaper/#hardware-root-of-trust-and-verified-boot).

Incluso si no utilizas estos sistemas operativos, la participación en estos programas puede indicar que el fabricante sigue las mejores prácticas en lo que respecta a la seguridad y las actualizaciones del hardware.

### SO Preinstalado

Los ordenadores nuevos casi siempre vienen con Windows preinstalado, a no ser que compres un Mac o una máquina especializada en Linux. Suele ser una buena idea borrar la unidad e instalar una copia nueva del sistema operativo elegido, aunque eso signifique reinstalar Windows desde cero. Debido a los acuerdos entre los proveedores de hardware y los proveedores de software sospechoso, la instalación predeterminada de Windows a menudo viene precargada con bloatware, [adware](https://bleepingcomputer.com/news/technology/lenovo-gets-a-slap-on-the-wrist-for-superfish-adware-scandal), o incluso [malware](https://zdnet.com/article/dell-poweredge-motherboards-ship-with-malware).

### Actualizaciones de Firmware

El hardware suele tener problemas de seguridad que se descubren y parchean mediante actualizaciones del firmware de tu hardware.

Casi todos los componentes de la computadora necesitan firmware para funcionar, desde la placa base hasta los dispositivos de almacenamiento. Lo ideal es que todos los componentes de tu dispositivo sean totalmente compatibles. Los dispositivos Apple, Chromebooks, la mayoría de los teléfonos Android y los dispositivos Microsoft Surface gestionarán las actualizaciones de firmware por ti siempre que el dispositivo sea compatible.

Si construyes tu propio PC, es posible que tengas que actualizar manualmente el firmware de la placa base descargándolo desde el sitio web del fabricante. Si usas Linux, considera usar la herramienta integrada [`fwupd`](https://fwupd.org) que te permitirá buscar y aplicar cualquier actualización de firmware disponible para tu placa base.

### TPM/Criptoprocesador Seguro

La mayoría de computadoras y teléfonos vienen equipados con un TPM (o un criptoprocesador seguro similar) que almacena de forma segura tus claves de cifrado y maneja otras funciones relacionadas con la seguridad. Si actualmente utilizas una máquina que no tiene una de estas características, puede que te convenga comprar un ordenador más nuevo que disponga de ella. Algunas placas base de ordenadores de sobremesa y servidores tienen un «encabezado TPM» que puede aceptar una pequeña placa accesoria que contiene el TPM.

<div class="admonition Note" markdown>
<p class="admonition-title">Nota</p>

Los TPM virtuales son susceptibles de sufrir ataques de canal lateral y los TPM externos, al estar separados de la CPU en la placa base, son vulnerables al [sniffing](https://pulsesecurity.co.nz/articles/TPM-sniffing) cuando un atacante tiene acceso al hardware. La solución a este problema es incluir el procesador seguro dentro de la propia CPU, como es el caso de los chips de Apple y [Pluton](https://microsoft.com/en-us/security/blog/2020/11/17/meet-the-microsoft-pluton-processor-the-security-chip-designed-for-the-future-of-windows-pcs) de Microsoft.

</div>

### Biometría

Muchos dispositivos vienen equipados con un lector de huellas dactilares o funciones de reconocimiento facial. Pueden ser muy prácticos, pero no son perfectos y a veces fallan. La mayoría de los dispositivos volverán a utilizar un PIN o una contraseña cuando esto ocurra, lo que significa que la seguridad de tus dispositivos sigue dependiendo de tu contraseña.

La biometría puede impedir que alguien te vea teclear tu contraseña, así que si el shoulder-surfing forma parte de tu modelo de amenazas, la biometría es una buena opción.

La mayoría de las implementaciones de autenticación facial requieren que estés mirando el teléfono y, además, solo funcionan desde una distancia relativamente cercana, por lo que no tienes que preocuparte demasiado de que alguien te apunte a la cara para desbloquearlo sin tu consentimiento. You can still disable biometrics when your phone is locked if you want. On iOS, you can hold the side button and a volume button for 3 seconds to disable Face ID on models that support it. On Android, hold the power button and press Lockdown on the menu.

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

Some devices do not have the proper hardware for secure face authentication. There's two main types of face authentication: 2D and 3D. 3D face authentication makes use of a dot projector that lets the device create a 3D depth map of your face. Make sure that your device has this capability.

</div>

Android defines three [security classes](https://source.android.com/docs/security/features/biometric/measure#biometric-classes) for biometrics; you should check that your device is Class 3 before enabling biometrics.

### Device Encryption

If your device is [encrypted](../encryption.md), your data is most secure when your device is completely powered off (as opposed to merely asleep), i.e. before you've entered your encryption key or lock screen password for the first time. On phones, this state of higher security is referred to as "Before First Unlock" (BFU), and "After First Unlock" (AFU) once you enter the correct password after a reboot/power-on. AFU is considerably less secure against digital forensics toolkits and other exploits, compared to BFU. Therefore, if you are concerned about an attacker with physical access to your device, you should turn it off fully whenever you aren't using it.

This may be impractical, so consider whether it's worth it, but in either case even AFU mode is effective against most threats, given you are using a strong encryption key.

## External Hardware

Some threats can't be protected against by your internal components alone. Many of these options are highly situational; please evaluate if they are really necessary for your threat model.

### Llaves de Seguridad

Hardware keys are devices that use strong cryptography to authenticate you to a device or account. The idea is that because they can not be copied, you can use them to secure accounts in such a way that they can only be accessed with physical possession of the key, eliminating many remote attacks.

[Recommended Hardware Keys :material-arrow-right-drop-circle:](../security-keys.md){ .md-button .md-button--primary } [Learn More about Hardware Keys :material-arrow-right-drop-circle:](multi-factor-authentication.md#hardware-security-keys){ .md-button }

### Camera/Microphone

If you don't want to trust your OS's permission controls to prevent the camera from activating in the first place, you can buy camera blockers that physically prevent light from reaching the camera. You could also buy a device that doesn't have a built-in camera and use an external camera that you can unplug whenever you're done using it. Some devices come with built-in camera blockers or hardware switches that physically disconnect the camera from power.

<div class="admonition warning" markdown>
<p class="admonition-title">Advertencia</p>

You should only buy covers that fit your laptop and won't cause damage when you close the lid. Covering the camera will interfere with automatic brightness and face authentication features.

</div>

For microphone access, in most cases you will need to trust your OS's built-in permission controls. Alternatively, buy a device that doesn't have a built-in microphone and use an external microphone that you can unplug when you're done using it. Some devices, like a [MacBook or an iPad](https://support.apple.com/guide/security/hardware-microphone-disconnect-secbbd20b00b/web), feature a hardware disconnect for the microphone when you close the lid.

Many computers have a BIOS option to disable the camera and microphone. When disabled there, the hardware won't even appear as a device on a booted system.

### Privacy Screens

Privacy screens are a film you can put over your normal screen so that the screen is only visible from a certain angle. These are good if your threat model includes others peeking at your screen, but it is not foolproof as anyone could just move to a different viewing angle and see what's on your screen.

### Dead Man's Switches

A dead man's switch stops a piece of machinery from operating without the presence of a human operator. These were originally designed as a safety measure, but the same concept can be applied to an electronic device to lock it when you're not present.

Some laptops are able to [detect](https://support.microsoft.com/en-us/windows/managing-presence-sensing-settings-in-windows-11-82285c93-440c-4e15-9081-c9e38c1290bb) when you're present and can lock automatically when you aren't sitting in front of the screen. You should check the settings in your OS to see if your computer supports this feature.

You can also get cables, like [Buskill](https://buskill.in), that will lock or wipe your computer when the cable is disconnected.

### Anti-Interdiction/Evil Maid Attack

The best way to prevent a targeted attack against you before a device is in your possession is to purchase a device in a physical store, rather than ordering it to your address.

Make sure your device supports secure boot/verified boot, and you have it enabled. Try to avoid leaving your device unattended whenever possible.

## Secure your Network

### Compartmentalization

Many solutions exist that allow you to separate what you're doing on a computer, such as virtual machines and sandboxing. However, the best compartmentalization is physical separation. This is useful especially for situations where certain software requires you to bypass security features in your OS, such as with anti-cheat software bundled with many games.

For gaming, it may be useful to designate one machine as your "gaming" machine and only use it for that one task. Keep it on a separate VLAN. This may require the use of a managed switch and a router that supports segregated networks.

Most consumer routers allow you to do this by enabling a separate "guest" network that can't talk to your main network. All untrusted devices can go here, including IoT devices like your smart fridge, thermostat, TV, etc.

### Minimalism

As the saying goes, "less is more". The fewer devices you have connected to your network, the less potential attack surface you'll have and the less work it will be to make sure they all stay up-to-date.

You may find it useful to go around your home and make a list of every connected device you have to help you keep track.

### Routers

Your router handles all your network traffic and acts as your first line of defense between you and the open internet.

<div class="admonition Note" markdown>
<p class="admonition-title">Nota</p>

A lot of routers come with storage to put your files on so you can access them from any computer on your network. We recommend you don't use networking devices for things other than networking. In the event your router was compromised, your files would also be compromised.

</div>

The most important thing to think about with routers is keeping them up-to-date. Many modern routers will automatically install updates, but many others won't. You should check on your router's settings page for this option. That page can usually be accessed by typing `192.168.1.1` or `192.168.0.1` into the URL bar of any browser assuming you're on the same network. You can also check in the network settings of your OS for "router" or "gateway".

If your router does not support automatic updates, you will need to go to the manufacturer's site to download the updates and apply them manually.

Many consumer-grade routers aren't supported for very long. If your router isn't supported by the manufacturer anymore, you can check if it's supported by [FOSS firmware](../router.md). You can also buy routers that come with FOSS firmware installed by default; these tend to be supported longer than most routers.

Some ISPs provide a combined router/modem. It can be beneficial for security to purchase a separate router and set your ISP router/modem into modem-only mode. This way, even when your ISP-provided router is no longer getting updates, you can still get security updates and patches. It also means any problems that affect your modem won't affect your router and vice versa.
