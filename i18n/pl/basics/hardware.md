---
title: "Wybór sprzętu"
icon: 'material/chip'
description: Oprogramowanie to nie wszystko; dowiedz się więcej o narzędziach sprzętowych, których używasz na co dzień, aby chronić swoją prywatność.
---

Gdy mowa o prywatności, sprzęt bywa często pomijany na rzecz dyskusji o używanym oprogramowaniu. Twój sprzęt powinien być traktowany jako fundament, na którym budujesz resztę swojej konfiguracji prywatności.

## Wybór komputera

Komponenty wewnętrzne urządzeń przetwarzają i przechowują wszystkie Twoje dane cyfrowe. Ważne jest, aby wszystkie urządzenia były wspierane przez producenta i deweloperów w postaci regularnych aktualizacji zabezpieczeń.

### Programy bezpieczeństwa sprzętowego

Niektóre urządzenia uczestniczą w „programie bezpieczeństwa sprzętowego” — to współpraca producentów określająca dobre praktyki i zalecenia przy projektowaniu sprzętu, na przykład:

- [Komputery z systemem Windows z zabezpieczonym rdzeniem](https://learn.microsoft.com/pl-pl/windows-hardware/design/device-experiences/oem-highly-secure-11) spełniają wyższe kryteria bezpieczeństwa określone przez Microsoft. Zabezpieczenia te nie dotyczą wyłącznie użytkowników systemu Windowsa; użytkownicy innych systemów operacyjnych nadal mogą korzystać z funkcji takich jak [ochrona DMA](https://learn.microsoft.com/pl-pl/windows/security/information-protection/kernel-dma-protection-for-thunderbolt) oraz z możliwości całkowitego braku zaufania do certyfikatów Microsoftu.
- [Android Ready SE](https://developers.google.com/android/security/android-ready-se) to współpraca między producentami mająca na celu zapewnienie, że ich urządzenia stosują [najlepsze praktyki](https://source.android.com/docs/security/best-practices/hardware) i zawierają odporną na manipulacje, sprzętową przestrzeń do przechowywania elementów takich jak klucze szyfrowania.
- macOS uruchamiany na układzie SoC firmy Apple wykorzystuje [zabezpieczenia sprzętowe](../os/macos-overview.md#hardware-security), które mogą być niedostępne w systemach operacyjnych firm trzecich.
- [Bezpieczeństwo systemu ChromeOS](https://chromium.org/chromium-os/developer-library/reference/security/security-whitepaper) jest najlepsze, gdy działa na Chromebooku, ponieważ może wtedy wykorzystać dostępne funkcje sprzętowe, takie jak [sprzętowy root-of-trust](https://chromium.org/chromium-os/developer-library/reference/security/security-whitepaper/#hardware-root-of-trust-and-verified-boot).

Nawet jeśli nie korzystasz z tych systemów operacyjnych, udział producenta w takich programach może świadczyć o tym, że stosuje on najlepsze praktyki dotyczące bezpieczeństwa sprzętowego i aktualizacji.

### Preinstalowany system operacyjny

Nowe komputery prawie zawsze są dostarczane z preinstalowanym systemem Windows, chyba że kupisz Maca lub specjalistyczną maszynę z Linuksem. Zwykle warto wyczyścić dysk i zainstalować świeżą kopię wybranego systemu operacyjnego, nawet jeśli oznacza to jedynie ponowną instalację systemu Windows od zera. Z powodu umów między producentami sprzętu a nieuczciwymi dostawcami oprogramowania, domyślna instalacja systemu Windows często bywa wstępnie załadowana oprogramowaniem typu bloatware, [adware](https://bleepingcomputer.com/news/technology/lenovo-gets-a-slap-on-the-wrist-for-superfish-adware-scandal), a czasem nawet [złośliwym oprogramowaniem](https://zdnet.com/article/dell-poweredge-motherboards-ship-with-malware).

### Aktualizacje oprogramowania układowego

Sprzęt często ma luki bezpieczeństwa, które są wykrywane i łatane w aktualizacjach oprogramowania układowego.

Prawie każdy komponent komputera wymaga oprogramowania układowego, aby działać — od płyty głównej po urządzenia pamięci masowej. W idealnym przypadku wszystkie elementy urządzenia powinny być w pełni wspierane przez producenta. Urządzenia Apple, Chromebooki, większość telefonów z Androidem oraz urządzenia Microsoft Surface będą obsługiwać aktualizacje oprogramowania układowego automatycznie, o ile dane urządzenie jest wspierane.

Jeśli składasz własny komputer, może być konieczne ręczne zaktualizowanie oprogramowania układowego płyty głównej, pobierając je ze strony producenta OEM płyty. Jeśli korzystasz z Linuksa, rozważ użycie wbudowanego narzędzia [`fwupd`](https://fwupd.org), które pozwala sprawdzić i zastosować dostępne aktualizacje oprogramowania układowego dla płyty głównej i innych komponentów.

### TPM / bezpieczny kryptoprocesor

Większość komputerów i telefonów jest wyposażona w moduł TPM (lub podobny bezpieczny kryptoprocesor), który bezpiecznie przechowuje klucze szyfrowania i obsługuje inne funkcje związane z bezpieczeństwem. Jeśli obecnie korzystasz z maszyny, która nie ma takiego modułu, warto rozważyć zakup nowszego urządzenia wyposażonego w tę funkcję. Niektóre płyty główne do komputerów stacjonarnych i serwerów mają złącze „TPM header”, które pozwala dodać małą płytkę zawierającą moduł TPM.

<div class="admonition Note" markdown>
<p class="admonition-title">Uwaga</p>

Wirtualne moduły TPM są podatne na ataki kanałów bocznych (ang. _side-channel attacks_), a zewnętrzne moduły TPM — jako elementy oddzielone od procesora na płycie głównej — mogą być narażone na tzw. [TPM sniffing](https://pulsesecurity.co.nz/articles/TPM-sniffing), gdy atakujący ma fizyczny dostęp do sprzętu. Rozwiązaniem jest umieszczenie bezpiecznego procesora wewnątrz samego procesora, tak jak ma to miejsce w układach Apple oraz w rozwiązaniu firmy Microsoft [Pluton](https://microsoft.com/en-us/security/blog/2020/11/17/meet-the-microsoft-pluton-processor-the-security-chip-designed-for-the-future-of-windows-pcs).

</div>

### Biometria

Wiele urządzeń wyposażonych jest w czytnik linii papilarnych lub funkcję rozpoznawania twarzy. Są to wygodne rozwiązania, ale nie są nieomylne i czasem zawodzą. W większości przypadków następuje wtedy powrót do kodu PIN lub hasła, więc bezpieczeństwo urządzenia zależy nadal od siły użytego hasła.

Biometria może zapobiec sytuacjom, w których ktoś obserwuje wpisywane hasło — więc jeśli tzw. _shoulder-surfing_ („podglądanie zza ramienia”) jest elementem Twojego modelu zagrożeń, biometria może być dobrą opcją.

Większość implementacji uwierzytelniania twarzy wymaga, aby patrzeć na telefon i działa jedynie ze stosunkowo bliskiej odległości, więc nie musisz nadmiernie obawiać się, że ktoś bez Twojej zgody skieruje telefon na Twoją twarz, by odblokować urządzenie. Biometrię można też wyłączyć, gdy telefon jest zablokowany. W systemie iOS przytrzymaj boczny przycisk i dowolny przycisk głośności przez 3 sekundy, aby wyłączyć Face ID na modelach, które go obsługują. Na Androidzie przytrzymaj przycisk zasilania i wybierz opcję „Blokada” w menu.

<div class="admonition warning" markdown>
<p class="admonition-title">Ostrzeżenie</p>

Niektóre urządzenia nie mają odpowiedniego sprzętu do bezpiecznego uwierzytelniania twarzy. Istnieją dwa główne rodzaje uwierzytelniania twarzy: 2D i 3D. 3D wykorzystuje projektor kropek, który pozwala urządzeniu utworzyć trójwymiarową mapę głębi twarzy. Upewnij się, że Twoje urządzenie ma taką funkcję.

</div>

Android definiuje trzy [klasy bezpieczeństwa](https://source.android.com/docs/security/features/biometric/measure#biometric-classes) dla biometrii; przed włączeniem biometrii upewnij się, że urządzenie jest klasy 3.

### Szyfrowanie urządzenia

Jeśli urządzenie jest [zaszyfrowane](../encryption.md), dane są najbezpieczniejsze, gdy urządzenie jest całkowicie wyłączone (a nie tylko uśpione) — czyli zanim po raz pierwszy wprowadzisz klucz szyfrowania lub hasło blokady ekranu. W telefonach ten stan większego bezpieczeństwa nazywany jest „Before First Unlock” (BFU, dosł. _przed pierwszym odblokowaniem_), a po wprowadzeniu prawidłowego hasła po ponownym uruchomieniu/włączeniu — „After First Unlock” (AFU, dosł. _po pierwszym odblokowaniu_). AFU jest znacznie mniej odporny przed narzędziami do analizy kryminalistycznej i innymi eksploitami w porównaniu do BFU. Dlatego też, jeśli obawiasz się atakującego mającego fizyczny dostęp do Twojego urządzenia, należy je całkowicie wyłączać, gdy go nie używasz.

Może to być niepraktyczne — więc przemyśl, czy warto — ale nawet tryb AFU jest skuteczny wobec większości zagrożeń, pod warunkiem, że używany jest silny klucz szyfrowania.

## Sprzęt zewnętrzny

Niektóre zagrożenia nie są do opanowania wyłącznie przez komponenty wewnętrzne. Wiele z opisanych tu opcji jest wysoce sytuacyjnych; oceń, czy faktycznie są konieczne w Twoim modelu zagrożeń.

### Sprzętowe klucze bezpieczeństwa

Hardware keys are devices that use strong cryptography to authenticate you to a device or account. The idea is that because they can not be copied, you can use them to secure accounts in such a way that they can only be accessed with physical possession of the key, eliminating many remote attacks.

[Recommended Hardware Keys :material-arrow-right-drop-circle:](../security-keys.md){ .md-button .md-button--primary } [Learn More about Hardware Keys :material-arrow-right-drop-circle:](multi-factor-authentication.md#hardware-security-keys){ .md-button }

### Camera/Microphone

If you don't want to trust your OS's permission controls to prevent the camera from activating in the first place, you can buy camera blockers that physically prevent light from reaching the camera. You could also buy a device that doesn't have a built-in camera and use an external camera that you can unplug whenever you're done using it. Some devices come with built-in camera blockers or hardware switches that physically disconnect the camera from power.

<div class="admonition warning" markdown>
<p class="admonition-title">Ostrzeżenie</p>

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
<p class="admonition-title">Uwaga</p>

A lot of routers come with storage to put your files on so you can access them from any computer on your network. We recommend you don't use networking devices for things other than networking. In the event your router was compromised, your files would also be compromised.

</div>

The most important thing to think about with routers is keeping them up-to-date. Many modern routers will automatically install updates, but many others won't. You should check on your router's settings page for this option. That page can usually be accessed by typing `192.168.1.1` or `192.168.0.1` into the URL bar of any browser assuming you're on the same network. You can also check in the network settings of your OS for "router" or "gateway".

If your router does not support automatic updates, you will need to go to the manufacturer's site to download the updates and apply them manually.

Many consumer-grade routers aren't supported for very long. If your router isn't supported by the manufacturer anymore, you can check if it's supported by [FOSS firmware](../router.md). You can also buy routers that come with FOSS firmware installed by default; these tend to be supported longer than most routers.

Some ISPs provide a combined router/modem. It can be beneficial for security to purchase a separate router and set your ISP router/modem into modem-only mode. This way, even when your ISP-provided router is no longer getting updates, you can still get security updates and patches. It also means any problems that affect your modem won't affect your router and vice versa.
