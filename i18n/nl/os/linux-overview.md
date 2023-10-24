---
title: Linux Overzicht
icon: simple/linux
description: Linux is een open-source, privacy-gericht desktop besturingssysteem alternatief, maar niet alle distributies zijn gelijk.
---

**Linux** is an open-source, privacy-focused desktop operating system alternative. In the face of pervasive telemetry and other privacy-encroaching technologies in mainstream operating systems, Linux desktop has remained the clear choice for people looking for total control over their computers from the ground up.

Our website generally uses the term “Linux” to describe **desktop** Linux distributions. Other operating systems which also use the Linux kernel such as ChromeOS, Android, and Qubes OS are not discussed on this page.

[Onze Linux-aanbevelingen :material-arrow-right-drop-circle:](../desktop.md ""){.md-button}

## Privacy Opmerkingen

There are some notable privacy concerns with Linux which you should be aware of. Despite these drawbacks, desktop Linux distributions are still great for most people who want to:

- Vermijd telemetrie die vaak gepaard gaat met propriëtaire besturingssystemen
- Handhaving van [softwarevrijheid](https://www.gnu.org/philosophy/free-sw.en.html#four-freedoms)
- Use privacy focused systems such as [Whonix](https://www.whonix.org) or [Tails](https://tails.boum.org/)

### Open-Source Security

It is a [common misconception](../basics/common-misconceptions.md#open-source-software-is-always-secure-or-proprietary-software-is-more-secure) that Linux and other open-source software is inherently secure simply because the source code is available. There is an expectation that community verification occurs regularly, but this isn’t always [the case](https://seirdy.one/posts/2022/02/02/floss-security/).

In reality, distro security depends on a number of factors, such as project activity, developer experience, the level of rigor applied to code reviews, and how often attention is given to specific parts of the codebase that may go untouched for years.

### Missing Security Features

At the moment, desktop Linux [falls behind alternatives](https://discussion.fedoraproject.org/t/fedora-strategy-2028-proposal-fedora-linux-is-as-secure-as-macos/46899/9) like macOS or Android when it comes to certain security features. We hope to see improvements in these areas in the future.

- **Verified boot** on Linux is not as robust as alternatives such as Apple’s [Secure Boot](https://support.apple.com/guide/security/secac71d5623/web) or Android’s [Verified Boot](https://source.android.com/security/verifiedboot). Verified boot prevents persistent tampering by malware and [evil maid attacks](https://en.wikipedia.org/wiki/Evil_Maid_attack), but is still largely [unavailable on even the most advanced distributions](https://discussion.fedoraproject.org/t/has-silverblue-achieved-verified-boot/27251/3).

- **Strong sandboxing** for apps on Linux is severely lacking, even with containerized apps like Flatpaks or sandboxing solutions like Firejail. Flatpak is the most promising sandboxing utility for Linux thus far, but is still deficient in many areas and allows for [unsafe defaults](https://flatkill.org/2020/) which allow most apps to trivially bypass their sandbox.

Additionally, Linux falls behind in implementing [exploit mitigations](https://madaidans-insecurities.github.io/linux.html#exploit-mitigations) which are now standard on other operating systems, such as Arbitrary Code Guard on Windows or Hardened Runtime on macOS. Also, most Linux programs and Linux itself are coded in memory-unsafe languages. Memory corruption bugs are responsible for the [majority of vulnerabilities](https://msrc.microsoft.com/blog/2019/07/a-proactive-approach-to-more-secure-code/) fixed and assigned a CVE. While this is also true for Windows and macOS, they are quickly making progress on adopting memory-safe languages—such as Rust and Swift, respectively—while there is no similar effort to rewrite Linux in a memory-safe language like Rust.

## Uw distributie kiezen

Niet alle Linux-distributies zijn gelijk geschapen. Our [Linux recommendation page](../desktop.md) is not meant to be an authoritative source on which distribution you should use, but our recommendations *are* aligned with the following guidelines. These are a few things you should keep in mind when choosing a distribution:

### Vrijgave cyclus

Wij raden je ten zeerste aan distributies te kiezen die dicht bij de stabiele upstream software releases blijven, vaak aangeduid als rolling release distributies. Dit komt omdat distributies met een bevroren releasecyclus vaak de pakketversies niet bijwerken en achterlopen op beveiligingsupdates.

Voor bevroren distributies wordt van pakketbeheerders verwacht dat ze patches backporteren om kwetsbaarheden te verhelpen (Debian is zo'n [voorbeeld](https://www.debian.org/security/faq#handling)) in plaats van de software aan te passen aan de "volgende versie" die door de upstream-ontwikkelaar wordt uitgebracht. Some security fixes [do not](https://arxiv.org/abs/2105.14565) receive a [CVE ID](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures) (particularly less popular software) at all and therefore do not make it into the distribution with this patching model. Als gevolg daarvan worden kleine beveiligingsupdates soms uitgesteld tot de volgende grote release.

Wij geloven niet dat het een goed idee is om pakketten tegen te houden en tussentijdse patches toe te passen, aangezien dit afwijkt van de manier waarop de ontwikkelaar de software bedoeld zou kunnen hebben. [Richard Brown](https://rootco.de/aboutme/) heeft hier een presentatie over:

<div class="yt-embed">
  <iframe width="560" height="315" src="https://invidious.privacyguides.net/embed/i8c0mg_mS7U?local=true" title="Regelmatig uitbrengen is verkeerd, Roll voor je leven" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

### Traditionele vs. Atomische updates

Traditioneel worden Linux distributies bijgewerkt door sequentieel de gewenste pakketten bij te werken. Traditionele updates zoals die gebruikt worden in Fedora, Arch Linux, en Debian gebaseerde distributies kunnen minder betrouwbaar zijn als er een fout optreedt tijdens het updaten.

Atomic updating distributies passen updates volledig of helemaal niet toe. Typisch zijn transactionele updatesystemen ook atomair.

Een transactioneel updatesysteem creëert een momentopname die wordt gemaakt voor en na het toepassen van een update. Als een update op een bepaald moment mislukt (bijvoorbeeld door een stroomstoring), kan de update gemakkelijk worden teruggezet naar een "laatst bekende goede staat"

De Atomic update methode wordt gebruikt voor immutable distributies zoals Silverblue, Tumbleweed, en NixOS en kan betrouwbaarheid bereiken met dit model. [Adam Šamalík](https://twitter.com/adsamalik) gaf een presentatie over hoe `rpm-ostree` werkt met Silverblue:

<div class="yt-embed">
  <iframe width="560" height="315" src="https://invidious.privacyguides.net/embed/-hpV5l-gJnQ?local=true" title="Laten we Fedora Silverblue proberen - een onveranderbaar desktop OS! - Adam Šamalik" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

### "Beveiligingsgerichte" distributies

Er bestaat vaak enige verwarring over "op veiligheid gerichte" distributies en "pentesting"-distributies. A quick search for “the most secure Linux distribution” will often give results like Kali Linux, Black Arch, or Parrot OS. Deze distributies zijn offensieve penetratietestdistributies die hulpmiddelen bundelen voor het testen van andere systemen. Ze bevatten geen "extra beveiliging" of defensieve maatregelen voor normaal gebruik.

### Arch-gebaseerde distributies

Arch and Arch-based distributions are not recommended for those new to Linux (regardless of distribution) as they require regular [system maintenance](https://wiki.archlinux.org/title/System_maintenance). Arch does not have a distribution update mechanism for the underlying software choices. Als gevolg daarvan moet je op de hoogte blijven van de huidige trends en technologieën overnemen naarmate deze oudere praktijken verdringen.

Voor een veilig systeem wordt ook verwacht dat je voldoende Linux kennis hebt om de beveiliging van hun systeem goed in te stellen, zoals het aannemen van een [mandatory access control](https://en.wikipedia.org/wiki/Mandatory_access_control) systeem, het opzetten van [kernel module](https://en.wikipedia.org/wiki/Loadable_kernel_module#Security) blacklists, het harden van boot parameters, het manipuleren van [sysctl](https://en.wikipedia.org/wiki/Sysctl) parameters, en weten welke componenten ze nodig hebben zoals [Polkit](https://en.wikipedia.org/wiki/Polkit).

Anyone using the [Arch User Repository (AUR)](https://wiki.archlinux.org/title/Arch_User_Repository) **must** be comfortable auditing PKGBUILDs that they download from that service. AUR-pakketten zijn door de gemeenschap geproduceerde inhoud en worden op geen enkele manier doorgelicht, en zijn daarom kwetsbaar voor aanvallen op de softwareketen, wat in het verleden inderdaad is gebeurd [](https://www.bleepingcomputer.com/news/security/malware-found-in-arch-linux-aur-package-repository/).

The AUR should always be used sparingly, and often there is a lot of bad advice on various pages which direct people to blindly use [AUR helpers](https://wiki.archlinux.org/title/AUR_helpers) without sufficient warning. Vergelijkbare waarschuwingen gelden voor het gebruik van Personal Package Archives (PPA's) van derden op Debian gebaseerde distributies of Community Projects (COPR) op Fedora.

If you are experienced with Linux and wish to use an Arch-based distribution, we generally recommend mainline Arch Linux over any of its derivatives.

Additionally, we recommend **against** these two Arch derivatives specifically:

- **Manjaro**: Deze distributie houdt pakketten 2 weken achter om er zeker van te zijn dat hun eigen veranderingen niet kapot gaan, niet om er zeker van te zijn dat upstream stabiel is. Wanneer AUR pakketten worden gebruikt, worden ze vaak gebouwd tegen de laatste [bibliotheken](https://en.wikipedia.org/wiki/Library_(computing)) uit Arch's repositories.
- **Garuda**: Zij gebruiken [Chaotic-AUR](https://aur.chaotic.cx/) die automatisch en blindelings pakketten compileert uit de AUR. Er is geen verificatieproces om ervoor te zorgen dat de AUR-pakketten niet te lijden hebben van aanvallen op de toeleveringsketen.

### Linux-libre kernel en "Libre" distributies

We recommend **against** using the Linux-libre kernel, since it [removes security mitigations](https://www.phoronix.com/news/GNU-Linux-Libre-5.7-Released) and [suppresses kernel warnings](https://news.ycombinator.com/item?id=29674846) about vulnerable microcode.

## Algemene aanbevelingen

### Schijfversleuteling

De meeste Linux-distributies hebben een optie in het installatieprogramma om [LUKS](../encryption.md#linux-unified-key-setup) FDE in te schakelen. Als deze optie niet is ingesteld tijdens de installatie, zult je een back-up van jouw gegevens moeten maken en opnieuw moeten installeren, aangezien de versleuteling wordt toegepast na [schijfpartitionering](https://en.wikipedia.org/wiki/Disk_partitioning), maar voordat [bestandssystemen](https://en.wikipedia.org/wiki/File_system) worden geformatteerd. We raden je ook aan jouw opslagapparaat veilig te wissen:

- [Veilig wissen van gegevens :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/05/25/secure-data-erasure/)

### Wissel

Consider using [ZRAM](https://wiki.archlinux.org/title/Zram#Using_zram-generator) instead of a traditional swap file or partition to avoid writing potentially sensitive memory data to persistent storage (and improve performance). Fedora-based distributions [use ZRAM by default](https://fedoraproject.org/wiki/Changes/SwapOnZRAM).

If you require suspend-to-disk (hibernation) functionality, you will still need to use a traditional swap file or partition. Make sure that any swap space you do have on a persistent storage device is [encrypted](https://wiki.archlinux.org/title/Dm-crypt/Swap_encryption) at a minimum to mitigate some of these threats.

### Wayland

We recommend using a desktop environment that supports the [Wayland](https://en.wikipedia.org/wiki/Wayland_(display_server_protocol)) display protocol, as it was developed with security [in mind](https://lwn.net/Articles/589147/). Its predecessor ([X11](https://en.wikipedia.org/wiki/X_Window_System)) does not support GUI isolation, which allows any window to [record, log, and inject inputs in other windows](https://blog.invisiblethings.org/2011/04/23/linux-security-circus-on-gui-isolation.html), making any attempt at sandboxing futile. While there are options to do nested X11 such as [Xpra](https://en.wikipedia.org/wiki/Xpra) or [Xephyr](https://en.wikipedia.org/wiki/Xephyr), they often come with negative performance consequences, and are neither convenient to set up nor preferable over Wayland.

Gelukkig hebben veelgebruikte omgevingen zoals [GNOME](https://www.gnome.org), [KDE](https://kde.org), en de window manager [Sway](https://swaywm.org) ondersteuning voor Wayland. Some distributions like Fedora and Tumbleweed use it by default, and some others may do so in the future as X11 is in [hard maintenance mode](https://www.phoronix.com/news/X.Org-Maintenance-Mode-Quickly). Als je een van deze omgevingen gebruikt is het zo eenvoudig als het selecteren van de "Wayland" sessie bij de desktop display manager ([GDM](https://en.wikipedia.org/wiki/GNOME_Display_Manager), [SDDM](https://en.wikipedia.org/wiki/Simple_Desktop_Display_Manager)).

Wij raden **aan tegen** door desktop omgevingen of window managers te gebruiken die geen Wayland ondersteuning hebben, zoals Cinnamon (standaard op Linux Mint), Pantheon (standaard op Elementary OS), MATE, Xfce, en i3.

### Eigen firmware (Microcode Updates)

Some Linux distributions (such as [Linux-libre](https://en.wikipedia.org/wiki/Linux-libre)-based or DIY distros) don’t come with the proprietary [microcode](https://en.wikipedia.org/wiki/Microcode) updates which patch critical security vulnerabilities. Enkele opmerkelijke voorbeelden van deze kwetsbaarheden zijn [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability)), [Meltdown](https://en.wikipedia.org/wiki/Meltdown_(security_vulnerability)), [SSB](https://en.wikipedia.org/wiki/Speculative_Store_Bypass), [Foreshadow](https://en.wikipedia.org/wiki/Foreshadow), [MDS](https://en.wikipedia.org/wiki/Microarchitectural_Data_Sampling), [SWAPGS](https://en.wikipedia.org/wiki/SWAPGS_(security_vulnerability)), en andere [hardwarekwetsbaarheden](https://www.kernel.org/doc/html/latest/admin-guide/hw-vuln/index.html).

We **highly recommend** that you install microcode updates, as they contain important security patches for the CPU which can not be fully mitigated in software alone. Fedora en openSUSE hebben beide standaard de microcode updates toegepast.

### Updates

De meeste Linux-distributies zullen automatisch updates installeren of u eraan herinneren om dat te doen. Het is belangrijk om jouw besturingssysteem up-to-date te houden, zodat jouw software wordt gepatcht wanneer een kwetsbaarheid wordt gevonden.

Some distributions (particularly those aimed at advanced users) are more bare bones and expect you to do things yourself (e.g. Arch or Debian). Hiervoor moet de "pakketbeheerder" (`apt`, `pacman`, `dnf`, enz.) handmatig worden uitgevoerd om belangrijke beveiligingsupdates te ontvangen.

Bovendien downloaden sommige distributies firmware-updates niet automatisch. Daarvoor moet je [`fwupd`](https://wiki.archlinux.org/title/Fwupd)installeren.

## Privacy Tweaks

### MAC-adres randomisatie

Many desktop Linux distributions (Fedora, openSUSE, etc.) come with [NetworkManager](https://en.wikipedia.org/wiki/NetworkManager) to configure Ethernet and Wi-Fi settings.

Het is mogelijk om [te randomiseren](https://fedoramagazine.org/randomize-mac-address-nm/) het [MAC adres](https://en.wikipedia.org/wiki/MAC_address) bij gebruik van NetworkManager. Dit zorgt voor wat meer privacy op Wi-Fi-netwerken, omdat het moeilijker wordt specifieke apparaten op het netwerk waarmee u verbonden bent, te traceren. Het doet [**niet**](https://papers.mathyvanhoef.com/wisec2016.pdf) maakt je anoniem.

Wij raden aan de instelling te wijzigen in **random** in plaats van **stable**, zoals voorgesteld in het [artikel](https://fedoramagazine.org/randomize-mac-address-nm/).

Als je [systemd-networkd](https://en.wikipedia.org/wiki/Systemd#Ancillary_components)gebruikt, moet je [`MACAddressPolicy=random`](https://www.freedesktop.org/software/systemd/man/systemd.link.html#MACAddressPolicy=) instellen, waardoor [RFC 7844 (Anonymity Profiles for DHCP Clients)](https://www.freedesktop.org/software/systemd/man/systemd.network.html#Anonymize=)wordt ingeschakeld.

MAC address randomization is primarily beneficial for Wi-Fi connections. For Ethernet connections, randomizing your MAC address provides little (if any) benefit, because a network administrator can trivially identify your device by other means (such as inspecting the port you are connected to on the network switch). Het willekeurig maken van Wi-Fi MAC-adressen hangt af van de ondersteuning door de firmware van de Wi-Fi.

### Andere identificatiemiddelen

Er zijn andere systeemidentifiers waar u misschien voorzichtig mee moet zijn. Je moet hier eens over nadenken om te zien of dit van toepassing is op jouw [dreigingsmodel](../basics/threat-modeling.md):

- **Hostnamen:** De hostnaam van jouw systeem wordt gedeeld met de netwerken waarmee je verbinding maakt. Je kunt beter geen identificerende termen zoals jouw naam of besturingssysteem in jouw hostnaam opnemen, maar het bij algemene termen of willekeurige strings houden.
- **Gebruikersnamen:** Ook jouw gebruikersnaam wordt op verschillende manieren in jouw systeem gebruikt. Gebruik liever algemene termen als "gebruiker" dan jouw eigenlijke naam.
- **Machine ID:**: Tijdens de installatie wordt een unieke machine ID gegenereerd en opgeslagen op jouw toestel. Overweeg [het in te stellen op een generieke ID](https://madaidans-insecurities.github.io/guides/linux-hardening.html#machine-id).

### Systeemtelling

Het Fedora Project [telt](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting) hoeveel unieke systemen toegang hebben tot zijn spiegels door gebruik te maken van een [`countme`](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting#Detailed_Description) variabele in plaats van een uniek ID. Fedora doet dit om de belasting te bepalen en waar nodig betere servers voor updates te voorzien.

Deze [optie](https://dnf.readthedocs.io/en/latest/conf_ref.html#options-for-both-main-and-repo) staat momenteel standaard uit. We raden aan om `countme=false` toe te voegen aan `/etc/dnf/dnf.conf` voor het geval het in de toekomst wordt ingeschakeld. Op systemen die `rpm-ostree` gebruiken, zoals Silverblue, wordt de countme optie uitgeschakeld door de [rpm-ostree-countme](https://fedoramagazine.org/getting-better-at-counting-rpm-ostree-based-systems/) timer te maskeren.

openSUSE gebruikt ook een [unieke ID](https://en.opensuse.org/openSUSE:Statistics) om systemen te tellen, die kan worden uitgeschakeld door het bestand `/var/lib/zypp/AnonymousUniqueId` te verwijderen.
