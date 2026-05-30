---
title: "Na komputery stacjonarne/osobiste"
icon: simple/linux
description: Dystrybucje systemu Linux są powszechnie polecane, jeśli chodzi o ochronę prywatności oraz wolne oprogramowanie.
cover: desktop.webp
---

<small>Chroni przed następującymi zagrożeniami:</small>

- [:material-account-cash: Kapitalizm inwigilacji](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

Dystrybucje systemu Linux są powszechnie polecane, jeśli chodzi o ochronę prywatności oraz wolne oprogramowanie. Jeśli nie korzystasz jeszcze z systemu Linux, poniżej znajdziesz kilka dystrybucji, które polecamy wypróbować oraz kilka ogólnych porad dotyczących lepszej prywatności i bezpieczeństwa, które mają zastosowanie dla wielu dystrybucji systemu Linux.

- [Ogólny przegląd systemów Linuks :material-arrow-right-drop-circle:](os/linux-overview.md)

## Tradycyjne dystrybucje

### Fedora Linuks

<div class="admonition recommendation" markdown>

![Logo Fedory](assets/img/linux-desktop/fedora.svg){ align=right }

**Fedora Linuks** jest polecaną przez nas dystrybucją stacjonarną dla osób, które dopiero rozpoczynają swoją przygodę z Linuksem. Fedora zazwyczaj przyjmuje nowsze technologie (np. [Wayland](https://wayland.freedesktop.org) i [PipeWire](https://pipewire.org)) przed innymi dystrybucjami. Te nowe technologie często wiążą się z poprawą bezpieczeństwa, prywatności i ogólnej użyteczności.

[:octicons-home-16: Strona Główna](https://fedoraproject.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.fedoraproject.org/en-US/docs){ .card-link title="Dokumentacja" }
[:octicons-heart-16:](https://whatcanidoforfedora.org){ .card-link title="Wesprzyj" }

</details>

</div>

Fedora jest dostępna w dwóch podstawowych wersjach stacjonarnych: [Fedora Workstation](https://fedoraproject.org/workstation), która używa środowiska graficznego GNOME, oraz [Fedora KDE Plasma Desktop](https://fedoraproject.org/kde), która używa środowiska KDE. Historycznie Fedora Workstation była bardziej popularna i powszechnie polecana, ale KDE zyskuje na popularności i zapewnia wrażenia bardziej zbliżone do Windows, co może ułatwić niektórym przejście na Linuksa. Korzyści związane z bezpieczeństwem i prywatnością w obu wersjach są bardzo podobne, więc wybór sprowadza się głównie do osobistych preferencji.

Fedora has a semi-rolling release cycle. While some packages like the desktop environment are frozen until the next Fedora release, most packages (including the kernel) are updated frequently throughout the lifespan of the release. Każde wydanie Fedora jest wspierane przez jeden rok, a nowe wersje są wydawane co 6 miesięcy.

### openSUSE Tumbleweed

<div class="admonition recommendation" markdown>

![openSUSE Tumbleweed logo](assets/img/linux-desktop/opensuse-tumbleweed.svg){ align=right }

**openSUSE Tumbleweed** is a stable rolling release distribution.

openSUSE Tumbleweed uses [Btrfs](https://en.wikipedia.org/wiki/Btrfs) and [Snapper](https://en.opensuse.org/openSUSE:Snapper_Tutorial) to ensure that snapshots can be rolled back should there be a problem.

[:octicons-home-16: Strona Główna](https://get.opensuse.org/tumbleweed){ .md-button .md-button--primary }
[:octicons-info-16:](https://doc.opensuse.org){ .card-link title="Dokumentacja" }
[:octicons-heart-16:](https://shop.opensuse.org){ .card-link title="Wesprzyj" }

</details>

</div>

As with the recommendation to avoid X11 in our [criteria](#criteria) for Linux distributions, we recommend avoiding desktop environments that support only the legacy X11 window system (for example, Xfce). Currently, KDE Plasma defaults to X11, but Wayland is supported.

Tumbleweed follows a rolling release model where each update is released as a snapshot of the distribution. Podczas aktualizacji systemu pobierany jest nowy punkt kontrolny. Każdy z nich jest poddawany serii testów przez [openQA](https://openqa.opensuse.org), aby zapewnić o jego jakości.

### Arch Linux

<div class="admonition recommendation" markdown>

![Logo Arch](assets/img/linux-desktop/archlinux.svg){ align=right }

**Arch Linux** jest lekką dystrybucją typu "zrób to sam" (DIY), co oznacza, że otrzymujesz tylko to, co zainstalujesz. Aby uzyskać więcej informacji, zobacz ich [FAQ](https://wiki.archlinux.org/title/Frequently_asked_questions).

[:octicons-home-16: Strona Główna](https://archlinux.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://wiki.archlinux.org){ .card-link title="Dokumentacja" }
[:octicons-heart-16:](https://archlinux.org/donate){ .card-link title="Wesprzyj" }

</details>

</div>

Arch Linux has a rolling release cycle. Nie ma ustalonego harmonogramu wydań, a pakiety są aktualizowane bardzo często.

Jako, że jest to dystrbucja DIY,  [oczekuje się, że skonfigurujesz i utrzymasz](os/linux-overview.md#arch-based-distributions) swój system samodzielnie. Arch posiada [oficjalny instalator](https://wiki.archlinux.org/title/Archinstall), który ułatwia proces instalacji.

Duża część [pakietów Arch Linux](https://reproducible.archlinux.org) jest [odtwarzalna](https://reproducible-builds.org)[^1].

## Dystrybucje atomowe

**Dystrybucje atomowe** (czasami określane również jako **dystrybucje niezmienne**) to systemy operacyjne, które obsługują instalację pakietów i aktualizacje poprzez nakładanie zmian na podstawowy obraz systemu, a nie poprzez bezpośrednią modyfikację systemu. Zalety dystrybucji atomowych obejmują większą stabilność i możliwość łatwego wycofywania aktualizacji. Zobacz [*Tradycyjne vs atomowe aktualizacje*](os/linux-overview.md#traditional-vs-atomic-updates) aby uzyskać więcej informacji.

### Fedora Atomic Desktops

<div class="admonition recommendation" markdown>

![Fedora logo](assets/img/linux-desktop/fedora.svg){ align=right }

**Fedora Atomic Desktops** are variants of Fedora which use the `rpm-ostree` package manager and have a strong focus on containerized workflows and Flatpak for desktop applications. All of these variants follow the same release schedule as Fedora Workstation, benefiting from the same fast updates and staying very close to upstream.

[:octicons-home-16: Strona Główna](https://fedoraproject.org/atomic-desktops){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.fedoraproject.org/en-US/emerging){ .card-link title="Dokumentacja" }
[:octicons-heart-16:](https://whatcanidoforfedora.org){ .card-link title="Wesprzyj" }

</details>

</div>

[Fedora Atomic Desktops](https://fedoramagazine.org/introducing-fedora-atomic-desktops) come in a variety of flavors depending on the desktop environment you prefer. As with the recommendation to avoid X11 in our [criteria](#criteria) for Linux distributions, we recommend avoiding flavors that support only the legacy X11 window system.

These operating systems differ from Fedora Workstation as they replace the [DNF](https://docs.fedoraproject.org/en-US/quick-docs/dnf) package manager with a much more advanced alternative called [`rpm-ostree`](https://coreos.github.io/rpm-ostree). The `rpm-ostree` package manager works by downloading a base image for the system, then overlaying packages over it in a [git](https://en.wikipedia.org/wiki/Git)-like commit tree. When the system is updated, a new base image is downloaded and the overlays will be applied to that new image.

After the update is complete, you will reboot the system into the new deployment. `rpm-ostree` keeps two deployments of the system so that you can easily roll back if something breaks in the new deployment. There is also the option to pin more deployments as needed.

[Flatpak](https://flatpak.org) is the primary package installation method on these distributions, as `rpm-ostree` is only meant to overlay packages that cannot stay inside a container on top of the base image.

As an alternative to Flatpaks, there is the option of [Toolbx](https://docs.fedoraproject.org/en-US/fedora-silverblue/toolbox) to create [Podman](https://podman.io) containers which mimic a traditional Fedora environment, a [useful feature](https://containertoolbx.org) for the discerning developer. These containers share a home directory with the host operating system.

### NixOS

<div class="admonition recommendation" markdown>

![NixOS logo](assets/img/linux-desktop/nixos.svg){ align=right }

NixOS is an independent distribution based on the Nix package manager with a focus on reproducibility and reliability.

[:octicons-home-16: Strona główna](https://nixos.org){ .md-button .md-button--primary }[:octicons-info-16:](https://nixos.org/learn.html){ .card-link title="Dokumentacja" }
[:octicons-heart-16:](https://nixos.org/donate.html){ .card-link title="Wesprzyj" }

</details>

</div>

Menedżer pakietów NixOS przechowuje każdą wersję każdego pakietu w innym folderze w **sklepie Nix**. W związku z tym możesz mieć różne wersje tego samego pakietu zainstalowanego w Twoim systemie Po zapisaniu zawartości pakietu w folderze folder staje się tylko do odczytu.

NixOS zapewnia również aktualizacje atomowe. It first downloads (or builds) the packages and files for the new system generation and then switches to it. There are different ways to switch to a new generation: you can tell NixOS to activate it after reboot, or you can switch to it at runtime. You can also *test* the new generation by switching to it at runtime, but not setting it as the current system generation. If something breaks during the update process, you can just reboot to return to a working version of your system.

The Nix package manager uses a purely functional language—which is also called Nix—to define packages.

[Nixpkgs](https://github.com/nixos/nixpkgs) (the main source of packages) are contained in a single GitHub repository. You can also define your own packages in the same language and then easily include them in your config.

Nix is a source-based package manager; if there’s no pre-built available in the binary cache, Nix will just build the package from source using its definition. It builds each package in a sandboxed *pure* environment, which is as independent of the host system as possible. Binaries built with this method are reproducible[^1].

## Dystrybucje "skoncentrowane na anonimowości"

### Whonix

<div class="admonition recommendation" markdown>

![Whonix logo](assets/img/linux-desktop/whonix.svg){ align=right }

**Whonix** is based on [Kicksecure](#kicksecure), a security-focused fork of Debian. Jego celem jest zapewnienie prywatności, bezpieczeństwa i [:material-incognito: anonimowości](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple } w Internecie. Whonix najlepiej używać w połączeniu z [Qubes OS](#qubes-os).

[:octicons-home-16: Strona główna](https://whonix.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://dds6qkxpwdeubwucdiaord2xgbbeyds25rbsgr73tbfpqpt4a6vjwsyd.onion){ .card-link title="Usługa .onion" }
[:octicons-info-16:](https://whonix.org/wiki/Documentation){ .card-link title="Dokumentacja" }
[:octicons-heart-16:](https://whonix.org/wiki/Donate){ .card-link title="Wesprzyj" }

</details>

</div>

Whonix ma działać jako dwie maszyny wirtualne: "stacja robocza" i "bramka Tor". Cała komunikacja ze stacji roboczej musi przechodzić przez bramę Tor. Oznacza to, że nawet jeśli stacja robocza zostanie przejęta przez złośliwe oprogramowanie, prawdziwy adres IP pozostanie ukryty.

Some of its features include Tor Stream Isolation, [keystroke anonymization](https://whonix.org/wiki/Keystroke_Deanonymization#Kloak), [encrypted swap](https://github.com/Whonix/swap-file-creator), and a hardened memory allocator. Future versions of Whonix will likely include [full system AppArmor policies](https://github.com/roddhjav/apparmor.d) and a [sandboxed app launcher](https://whonix.org/wiki/Sandbox-app-launcher) to fully confine all processes on the system.

Whonix is best used [in conjunction with Qubes](https://whonix.org/wiki/Qubes/Why_use_Qubes_over_other_Virtualizers). We have a [recommended guide](os/qubes-overview.md#connecting-to-tor-via-a-vpn) on configuring Whonix in conjunction with a VPN ProxyVM in Qubes to hide your Tor activities from your ISP.

### Tails

<div class="admonition recommendation" markdown>

![Tails logo](assets/img/linux-desktop/tails.svg){ align=right }

**Tails** is a live operating system based on Debian that routes all communications through Tor, which can boot on on almost any computer from a DVD, USB stick, or SD card installation. Wykorzystuje [Tor](tor.md), aby zachować prywatność i [:material-incognito: Anonimowość](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple } omijając przy tym cenzurę i nie pozostawiając po sobie śladu na komputerze, na którym jest używany po wyłączeniu.

[:octicons-home-16: Strona Główna](https://tails.net){ .md-button .md-button--primary }
[:octicons-info-16:](https://tails.net/doc/index.en.html){ .card-link title="Dokumentacja" }
[:octicons-heart-16:](https://tails.net/donate){ .card-link title="Wesprzyj" }

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Ostrzeżenie</p>

Tails [nie usuwa](https://gitlab.tails.boum.org/tails/tails/-/issues/5356) [pamięci wideo](https://en.wikipedia.org/wiki/Dual-ported_video_RAM) podczas wyłączania. Po ponownym uruchomieniu komputera po użyciu aplikacji Tails może on na chwilę wyświetlić ostatni ekran wyświetlany w aplikacji Tails. Jeśli wyłączysz komputer, zamiast go ponownie uruchamiać, pamięć wideo usunie się automatycznie po pewnym czasie bez zasilania.

</div>

Tails is great for counter forensics due to amnesia (meaning nothing is written to the disk); however, it is not a hardened distribution like Whonix. Brakuje mu wielu funkcji anonimowości i bezpieczeństwa, które posiada Whonix i jest aktualizowany znacznie rzadziej (tylko raz na sześć tygodni). A Tails system that is compromised by malware may potentially bypass the transparent proxy, allowing for the user to be deanonymized.

Tails domyślnie zawiera [uBlock Origin](browser-extensions.md#ublock-origin) w przeglądarce Tor, co może potencjalnie ułatwić adwersarzom pobieranie odcisków palców użytkowników Tails. Maszyny wirtualne [Whonix](desktop.md#whonix) mogą być bardziej odporne na wycieki, jednak nie są amnezyjne, co oznacza, że dane mogą zostać odzyskane z urządzenia pamięci masowej.

Z założenia Tails ma się całkowicie resetować po każdym ponownym uruchomieniu. Szyfrowana [pamięć trwała](https://tails.net/doc/persistent_storage/index.en.html) może być skonfigurowana do przechowywania niektórych danych między restartami.

## Dystrybucje "skoncentrowane na bezpieczeństwie"

<small>Chroni przed następującymi zagrożeniami:</small>

- [:material-bug-outline: Ataki pasywne](basics/common-threats.md#security-and-privacy ""){.pg-orange}

### Qubes OS

<div class="admonition recommendation" markdown>

![Qubes OS logo](assets/img/qubes/qubes_os.svg){ align=right }

**Qubes OS** is an open-source operating system designed to provide strong security for desktop computing through secure virtual machines (or "qubes"). Qubes is based on Xen, the X Window System, and Linux. It can run most Linux applications and use most of the Linux drivers.

[:octicons-home-16: Strona główna](https://qubes-os.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://qubesosfasa4zl44o4tws22di6kepyzfeqv3tg4e3ztknltfxqrymdad.onion){ .card-link title="Serwis cebulowy" }
[:octicons-eye-16:](https://qubes-os.org/privacy){ .card-link title="Serwis .onion" }
[:octicons-info-16:](https://qubes-os.org/doc){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/QubesOS){ .card-link title="Kod źródłowy" }
[:octicons-heart-16:](https://qubes-os.org/donate){ .card-link title="Wesprzyj" }

</details>

</div>

Qubes OS zabezpiecza komputer, izolując podsystemy (np. sieciowe, USB itp.) i aplikacje w oddzielnych *qubes*. Jeśli jedna część systemu zostanie naruszona w ramach [:material-target-account: ataku ukierunkowanego](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red}, dodatkowa izolacja prawdopodobnie ochroni resztę *qubów* i główny system.

Aby uzyskać więcej informacji na temat działania Qubes, przeczytaj naszą pełną stronę [przegląd Qubes OS](os/qubes-overview.md).

### Secureblue

<div class="admonition recommendation" markdown>

![Logo Secureblue](assets/img/linux-desktop/secureblue.svg){ align=right }

**Secureblue** to skoncentrowany na bezpieczeństwie system operacyjny oparty na [Fedora Atomic Desktops](#fedora-atomic-desktops). It includes a number of [security features](https://secureblue.dev/features) intended to proactively defend against the exploitation of both known and unknown vulnerabilities, and ships with [Trivalent](https://github.com/secureblue/Trivalent), their hardened, Chromium-based web browser.

[:octicons-home-16: Strona główna](https://secureblue.dev){ .md-button .md-button--primary }
[:octicons-info-16:](https://secureblue.dev/install){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/secureblue/secureblue){ .card-link title="Kod źródłowy" }
[:octicons-heart-16:](https://secureblue.dev/donate){ .card-link title="Wesprzyj" }

</div>

**Trivalent** is Secureblue's hardened Chromium for desktop Linux inspired by [GrapheneOS](android/distributions.md#grapheneos)'s Vanadium browser.

Secureblue also provides GrapheneOS's [hardened memory allocator](https://github.com/GrapheneOS/hardened_malloc) and enables it globally (including for Flatpaks).

### Kicksecure

While we [recommend against](os/linux-overview.md#release-cycle) "perpetually outdated" distributions like Debian for desktop use in most cases, Kicksecure is a Debian-based operating system which has been hardened to be much more than a typical Linux install.

<div class="admonition recommendation" markdown>

![Logo Kicksecure](assets/img/linux-desktop/kicksecure.svg){ align=right }

**Kicksecure**— w dużym uproszczeniu — to zestaw skryptów, konfiguracji i pakietów, które znacznie zmniejszają powierzchnię ataku Debiana. Domyślnie obejmuje wiele zaleceń dotyczących prywatności i zabezpieczeń. Służy również jako podstawowy system operacyjny dla [Whonix](#whonix).

[:octicons-home-16: Strona główna](https://kicksecure.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://kicksecure.com/wiki/Privacy_Policy){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://kicksecure.com/wiki/Documentation){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/Kicksecure){ .card-link title="Kod źródłowy" }
[:octicons-heart-16:](https://kicksecure.com/wiki/Donate){ .card-link title="Wesprzyj" }

</details>

</div>

## Kryteria

Wybór rozprawy, która jest słuszna dla ciebie, będzie zależeć od wielu osobistych preferencji, i ta strona to **nie** ma być wyczerpującą listą wszystkich możliwych dystrybucji. Nasza strona z przeglądem Linuksa zawiera bardziej szczegółowe porady dotyczące [wyboru dystrybucji](os/linux-overview.md#choosing-your-distribution). The distros on *this* page do all generally follow the guidelines we covered there, and all meet these standards:

- Darmowy i open source.
- Otrzymuje regularne aktualizacje oprogramowania i jądra.
- Unika X11, ponieważ jego ostatnia duża wersja miała miejsce [ponad dekadę](https://x.org/wiki/Releases) temu.
    - The notable exception here is Qubes, but the [isolation issues](https://blog.invisiblethings.org/2011/04/23/linux-security-circus-on-gui-isolation) which X11 typically has are avoided by virtualization. Ta izolacja dotyczy tylko aplikacji *działających w różnych qubes* (maszynach wirtualnych); aplikacje działające w *tym samym* qube nie są chronione przed sobą nawzajem.
- Obsługuje pełne szyfrowanie dysku podczas instalacji.
- Nie zamraża regularnych wydań na dłużej niż 1 rok.
    - [Odradzamy](os/linux-overview.md#release-cycle) wersje dystrybucji "długoterminowego wsparcia" lub "stabilne" dla komputerów stacjonarnych.
- Obsługuje szeroką gamę sprzętu.
- Preferowane większe projekty.
    - Utrzymanie systemu operacyjnego jest dużym wyzwaniem, a mniejsze projekty mają tendencję do popełniania większej liczby możliwych do uniknięcia błędów lub opóźniania krytycznych aktualizacji (lub, co gorsza, całkowitego zniknięcia). Skłaniamy się ku projektom, które prawdopodobnie będą istniały za 10 lat (czy to dzięki wsparciu korporacji, czy bardzo znaczącemu wsparciu społeczności), a z dala od projektów, które są budowane ręcznie lub mają niewielką liczbę konserwatorów.

Ponadto nadal obowiązują [nasze standardowe kryteria](about/criteria.md) dla rekomendowanych projektów. **Należy pamiętać, że nie jesteśmy powiązani z żadnym z polecanych przez nas projektów.**

[^1]: Odtwarzalność wiąże się z możliwością zweryfikowania, czy pakiety i pliki binarne udostępnione użytkownikowi końcowemu są zgodne z kodem źródłowym, co może być przydatne w przypadku potencjalnych [:material-package-variant-closed-remove: ataków w łańcuchu dostaw](basics/common-threats.md#attacks-against-certain-organizations ""){.pg-viridian}.
