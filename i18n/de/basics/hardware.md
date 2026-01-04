---
title: "Hardware auswählen"
icon: 'material/chip'
description: Software ist nicht alles, was zählt. Informiere dich über die Hardware-Tools, die du täglich zum Schutz deiner Daten verwendest.
---

Wenn es um Diskussionen über die Privatsphäre geht, wird oft nicht so viel über Hardware nachgedacht wie über die Software, die wir verwenden. Deine Hardware sollte als Fundament betrachtet werden, auf dem du den Rest deiner Datenschutzeinrichtung aufbaust.

## Auswahl eines Computers

Die internen Komponenten deines Gerätes verarbeiten und speichern alle deine digitalen Daten. Es sind wichtig, dass alle Geräte von den Herstellern sowie Entwicklern unterstützt werden, indem sie weiter Sicherheitsupdates bekommen.

### Hardware-Sicherheitsprogramme

Manche Geräte haben ein "Hardware-Sicherheitsprogramm", wo Hersteller zusammenarbeiten, um beste Praktiken sowie Empfehlungen für die Entwicklung von Hardware zu erarbeiten:

- [Windows Secured-core PCs](https://learn.microsoft.com/de-de/windows-hardware/design/device-experiences/oem-highly-secure-11) erfüllen höhere, von Microsoft festgelegte Sicherheitskriterien. Diese Schutzmaßnahmen gelten nicht nur für Windows-Benutzer; auch Benutzer anderer Betriebssysteme können die Vorteile von Funktionen wie [DMA-Schutz](https://learn.microsoft.com/de-de/windows/security/hardware-security/kernel-dma-protection-for-thunderbolt) und der Möglichkeit, Microsoft-Zertifikaten vollständig zu misstrauen, nutzen.
- [Android Ready SE](https://developers.google.com/android/security/android-ready-se) ist eine Zusammenarbeit zwischen Herstellern, um sicherzustellen, dass ihre Geräte den [Best Practices](https://source.android.com/docs/security/best-practices/hardware) entsprechen und einen manipulationssicheren, hardwaregestützten Speicher für Dinge wie Verschlüsselungsschlüssel enthalten.
- macOS, das auf einem Apple SoC läuft, nutzt die Vorteile der [Hardwaresicherheit](../os/macos-overview.md#hardware-security), die bei Betriebssystemen von Drittanbietern möglicherweise nicht verfügbar sind.
- Die [ChromeOS-Sicherheit](https://chromium.org/chromium-os/developer-library/reference/security/security-whitepaper) ist am besten, wenn sie auf einem Chromebook ausgeführt wird, da sie in der Lage ist, verfügbare Hardwarefunktionen wie das [Hardware Root-of-Trust](https://chromium.org/chromium-os/developer-library/reference/security/security-whitepaper/#hardware-root-of-trust-and-verified-boot) zu nutzen.

Auch wenn du diese Betriebssysteme nicht verwendest, teilnahme an diesen Programmen könnte zeigen, dass der Hersteller die besten Praktiken in Bezug auf Hardwaresicherheit sowie akutualisierungen anwendet.

### Vorinstallierte Betriebssysteme

Neue Computer kommen fast immer mit Windows vorinstalliert, außer man kauft einen Mac oder eine spezielle Linux-Maschine. Es sind eine gute Idee das Laufwerk zu löschen und eine frische Kopie des Betriebssystems deiner Wahl zu installieren, auch wenn es nur heißt, dass man Windows von neu installiert. Wegen Vereinbarungen zwischen Hardwareherstellern und unehrlichen Softwareanbietern, kommt die Standard-Windows-Installation oft mit Bloatware, [adware](https://bleepingcomputer.com/news/technology/lenovo-gets-a-slap-on-the-wrist-for-superfish-adware-scandal), oder auch [malware](https://zdnet.com/article/dell-poweredge-motherboards-ship-with-malware) vorinstalliert.

### Firmware-Updates

Hardware hat oft Sicherheitsprobleme die gefunden werden, und durch Firmware-Updates behoben werden.

Fast jedes Komponent in deinem Computer braucht Firmware, um zu funktionieren, von der Hauptplatine bis zu den Speichergeräten. Es ist ideal, dass alle Komponente deines Gerätes völlig unterstützt sind. Apple Geräte, Chromebooks, die meisten Android-Handys und Microsoft Surface-Geräte übernehmen Firmware-Updates, solang das Gerät unterstützt wird.

Wenn du dein eigenen PC baust, wirst du die Firmware deines Motherboards manuell aktualisieren müssen, indem du sie von der Website deines OEMs herunterladest. Wenn du Linux verwendest, solltest du das eingebaute Tool [`fwupd`](https://fwupd.org) verwenden, um alle verfügbaren Firmware-Updates deines Motherboards zu überprüfen und anwenden.

### TPM/Sicherer Kryptoprozessor

Die meisten Computer und Handys kommen mit TPM (oder einem ähnlichen sicheren Kryptoprozessor) ausgestattet, die dein Verschlüsselungsschlüssel speichert und andere sichereheitsrelevante Funktionen übernimmt. Wenn du gerade eine Maschine benutzt, die nicht einer dieser Prozessoren hat, könntest du vielleicht einen Vorteil finden, indem du einen neueren Computer kaufst, der diese Funktion besitzt. Einige Desktop- und Server-Hauptplatinen verfügen über einen "TPM-Header", der eine kleine Zusatzplatine mit dem TPM aufnehmen kann.

<div class="admonition Note" markdown>
<p class="admonition-title">Anmerkung</p>

Virtual TPMs are susceptible to side-channel attacks and external TPMs, as a result of being separate from the CPU on the motherboard, are vulnerable to [sniffing](https://pulsesecurity.co.nz/articles/TPM-sniffing) when an attacker has access to the hardware. The solution to this problem is to include the secure processor inside the CPU itself, which is the case for Apple's chips and Microsoft's [Pluton](https://microsoft.com/en-us/security/blog/2020/11/17/meet-the-microsoft-pluton-processor-the-security-chip-designed-for-the-future-of-windows-pcs).

</div>

### Biometrie

Many devices come equipped with a fingerprint reader or face recognition capabilities. These can be very convenient, but they aren't perfect and sometimes fail. Most devices will fall back to a PIN or password when this happens, meaning that the security of your devices is still only as good as your password.

Biometrics can prevent someone from watching you type in your password, so if shoulder-surfing is part of your threat model then biometrics are a good option.

Most implementations of face authentication require you to be looking at your phone and also only work from a relatively close distance, so you don't need to worry too much about someone pointing your phone at your face to unlock it without your consent. You can still disable biometrics when your phone is locked if you want. On iOS, you can hold the side button and a volume button for 3 seconds to disable Face ID on models that support it. On Android, hold the power button and press Lockdown on the menu.

<div class="admonition warning" markdown>
<p class="admonition-title">Warnung</p>

Some devices do not have the proper hardware for secure face authentication. There are two main types of face authentication: 2D and 3D. 3D face authentication makes use of a dot projector that lets the device create a 3D depth map of your face. Make sure that your device has this capability.

</div>

Android defines three [security classes](https://source.android.com/docs/security/features/biometric/measure#biometric-classes) for biometrics; you should check that your device is Class 3 before enabling biometrics.

### Geräteverschlüsselung

If your device is [encrypted](../encryption.md), your data is most secure when your device is completely powered off (as opposed to merely asleep), i.e. before you've entered your encryption key or lock screen password for the first time. On phones, this state of higher security is referred to as "Before First Unlock" (BFU), and "After First Unlock" (AFU) once you enter the correct password after a reboot/power-on. AFU is considerably less secure against digital forensics toolkits and other exploits, compared to BFU. Therefore, if you are concerned about an attacker with physical access to your device, you should turn it off fully whenever you aren't using it.

This may be impractical, so consider whether it's worth it, but in either case even AFU mode is effective against most threats, given you are using a strong encryption key.

## Externe Geräte

Some threats can't be protected against by your internal components alone. Many of these options are highly situational; please evaluate if they are really necessary for your threat model.

### Hardware-Sicherheitsschlüssel

Hardware keys are devices that use strong cryptography to authenticate you to a device or account. The idea is that because they can not be copied, you can use them to secure accounts in such a way that they can only be accessed with physical possession of the key, eliminating many remote attacks.

[Recommended Hardware Keys :material-arrow-right-drop-circle:](../security-keys.md){ .md-button .md-button--primary } [Learn More about Hardware Keys :material-arrow-right-drop-circle:](multi-factor-authentication.md#hardware-security-keys){ .md-button }

### Kamera/Mikrofon

If you don't want to trust your OS's permission controls to prevent the camera from activating in the first place, you can buy camera blockers that physically prevent light from reaching the camera. You could also buy a device that doesn't have a built-in camera and use an external camera that you can unplug whenever you're done using it. Some devices come with built-in camera blockers or hardware switches that physically disconnect the camera from power.

<div class="admonition warning" markdown>
<p class="admonition-title">Warnung</p>

You should only buy covers that fit your laptop and won't cause damage when you close the lid. Covering the camera will interfere with automatic brightness and face authentication features.

</div>

For microphone access, in most cases you will need to trust your OS's built-in permission controls. Alternatively, buy a device that doesn't have a built-in microphone and use an external microphone that you can unplug when you're done using it. Some devices, like a [MacBook or an iPad](https://support.apple.com/guide/security/hardware-microphone-disconnect-secbbd20b00b/web), feature a hardware disconnect for the microphone when you close the lid.

Many computers have a BIOS option to disable the camera and microphone. When disabled there, the hardware won't even appear as a device on a booted system.

### Privacy Screens

Privacy screens are a film you can put over your normal screen so that the screen is only visible from a certain angle. These are good if your threat model includes others peeking at your screen, but it is not foolproof as anyone could just move to a different viewing angle and see what's on your screen.

### Dead Man's Switches

A dead man's switch stops a piece of machinery from operating without the presence of a human operator. These were originally designed as a safety measure, but the same concept can be applied to an electronic device to lock it when you're not present.

Some laptops are able to [detect](https://support.microsoft.com/en-us/windows/managing-presence-sensing-settings-in-windows-11-82285c93-440c-4e15-9081-c9e38c1290bb) when you're present and can lock automatically when you aren't sitting in front of the screen. You should check the settings in your OS to see if your computer supports this feature.

You can also get cables, like [BusKill](https://buskill.in), that will lock or wipe your computer when the cable is disconnected.

### Anti-Interdiction/Evil Maid Attack

The best way to prevent a targeted attack against you before a device is in your possession is to purchase a device in a physical store, rather than ordering it to your address.

Make sure your device supports secure boot/verified boot, and you have it enabled. Try to avoid leaving your device unattended whenever possible.

### Kensington Locks

Many laptops come equipped with a [Kensington slot](https://www.kensington.com/solutions/product-category/security/?srsltid=AfmBOorQOlRnqRJOAqM-Mvl7wumed0wBdiOgktlvdidpMHNIvGfwj9VI) that can be used to secure your device with a **metal cable** that locks into the slot on your machine. These locks can be combination locks or keyed.

As with all locks, Kensington locks are vulnerable to [physical attacks](https://youtu.be/vgvCxL7dMJk) so you should mainly use them to deter petty theft. You can secure your laptop at home or even when you're out in public using a table leg or something that won't move easily.

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
<p class="admonition-title">Note</p>

A lot of routers come with storage to put your files on so you can access them from any computer on your network. We recommend you don't use networking devices for things other than networking. In the event your router was compromised, your files would also be compromised.

</div>

The most important thing to think about with routers is keeping them up-to-date. Many modern routers will automatically install updates, but many others won't. You should check on your router's settings page for this option. That page can usually be accessed by typing `192.168.1.1` or `192.168.0.1` into the URL bar of any browser assuming you're on the same network. You can also check in the network settings of your OS for "router" or "gateway".

If your router does not support automatic updates, you will need to go to the manufacturer's site to download the updates and apply them manually.

Many consumer-grade routers aren't supported for very long. If your router isn't supported by the manufacturer anymore, you can check if it's supported by [FOSS firmware](../router.md). You can also buy routers that come with FOSS firmware installed by default; these tend to be supported longer than most routers.

Some ISPs provide a combined router/modem. It can be beneficial for security to purchase a separate router and set your ISP router/modem into modem-only mode. This way, even when your ISP-provided router is no longer getting updates, you can still get security updates and patches. It also means any problems that affect your modem won't affect your router and vice versa.
