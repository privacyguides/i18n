---
title: Översikt över Linux
icon: simple/linux
description: Linux is an open-source, privacy-focused desktop operating system alternative, but not all distribitions are created equal.
---

**Linux** is an open-source, privacy-focused desktop operating system alternative. In the face of pervasive telemetry and other privacy-encroaching technologies in mainstream operating systems, desktop Linux has remained the clear choice for people looking for total control over their computers from the ground up.

Our website generally uses the term “Linux” to describe **desktop** Linux distributions. Other operating systems which also use the Linux kernel such as ChromeOS, Android, and Qubes OS are not discussed on this page.

[Våra Linux-rekommendationer :material-arrow-right-drop-circle:](../desktop.md ""){.md-button}

## Privacy Notes

There are some notable privacy concerns with Linux which you should be aware of. Despite these drawbacks, desktop Linux distributions are still great for most people who want to:

- Undvik telemetri som ofta kommer med egna operativsystem
- Maintain [software freedom](https://gnu.org/philosophy/free-sw.en.html#four-freedoms)
- Använd integritetsfokuserade system som t. ex. [Whonix](../desktop.md#whonix) eller [Tails](../desktop.md#tails)

### Open-Source Security

It is a [common misconception](../basics/common-misconceptions.md#open-source-software-is-always-secure-or-proprietary-software-is-more-secure) that Linux and other open-source software is inherently secure simply because the source code is available. There is an expectation that community verification occurs regularly, but this isn’t always [the case](https://seirdy.one/posts/2022/02/02/floss-security).

In reality, distro security depends on a number of factors, such as project activity, developer experience, the level of rigor applied to code reviews, and how often attention is given to specific parts of the codebase that may go untouched for years.

### Missing Security Features

At the moment, desktop Linux [falls behind alternatives](https://discussion.fedoraproject.org/t/fedora-strategy-2028-proposal-fedora-linux-is-as-secure-as-macos/46899/9) like macOS or Android when it comes to certain security features. We hope to see improvements in these areas in the future.

- **Verified boot** on Linux is not as robust as alternatives such as Apple’s [Secure Boot](https://support.apple.com/guide/security/secac71d5623/web) or Android’s [Verified Boot](https://source.android.com/security/verifiedboot). Verified boot prevents persistent tampering by malware and [evil maid attacks](https://en.wikipedia.org/wiki/Evil_Maid_attack), but is still largely [unavailable on even the most advanced distributions](https://discussion.fedoraproject.org/t/has-silverblue-achieved-verified-boot/27251/3).

- **Strong sandboxing** for apps on Linux is severely lacking, even with containerized apps like Flatpaks or sandboxing solutions like Firejail. Flatpak is the most promising sandboxing utility for Linux thus far, but is still deficient in many areas and allows for [unsafe defaults](https://flatkill.org/2020) which allow most apps to trivially bypass their sandbox.

Additionally, Linux falls behind in implementing [exploit mitigations](https://madaidans-insecurities.github.io/linux.html#exploit-mitigations) which are now standard on other operating systems, such as Arbitrary Code Guard on Windows or Hardened Runtime on macOS. Also, most Linux programs and Linux itself are coded in memory-unsafe languages. Memory corruption bugs are responsible for the [majority of vulnerabilities](https://msrc.microsoft.com/blog/2019/07/a-proactive-approach-to-more-secure-code) fixed and assigned a CVE. While this is also true for Windows and macOS, they are quickly making progress on adopting memory-safe languages—such as Rust and Swift, respectively—while there is no similar effort to rewrite Linux in a memory-safe language like Rust.

## Välja din distribution

Inte alla Linux-distributioner är skapade lika. Our [Linux recommendation page](../desktop.md) is not meant to be an authoritative source on which distribution you should use, but our recommendations *are* aligned with the following guidelines. These are a few things you should keep in mind when choosing a distribution:

### Utgivningscykel

Vi rekommenderar starkt att du väljer distributioner som ligger nära de stabila uppströmsutgåvorna, ofta kallade rullande utgåvor. Detta beror på att frysta utgåvor ofta inte uppdaterar paketversioner och hamnar bakom säkerhetsuppdateringar.

For frozen distributions such as [Debian](https://debian.org/security/faq#handling), package maintainers are expected to backport patches to fix vulnerabilities rather than bump the software to the “next version” released by the upstream developer. Some security fixes [do not](https://arxiv.org/abs/2105.14565) receive a [CVE ID](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures) (particularly less popular software) at all and therefore do not make it into the distribution with this patching model. As a result, minor security fixes are sometimes held back until the next major release.

Vi tror inte att hålla paket tillbaka och tillämpa tillfälliga patchar är en bra idé, eftersom det skiljer sig från hur utvecklaren kan ha avsett att programvaran ska fungera. [Richard Brown](https://rootco.de/aboutme) has a presentation about this:

<div class="yt-embed">
  <iframe width="560" height="315" src="https://invidious.privacyguides.net/embed/i8c0mg_mS7U?local=true" title="Regelbundna offentliggöranden är fel, rulla för ditt liv" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

### Traditionella och atomära uppdateringar

Traditionellt sett uppdaterar Linuxdistributioner genom att sekventiellt uppdatera de önskade paketen. Traditionella uppdateringar som de som används i Fedora-, Arch Linux- och Debianbaserade distributioner kan vara mindre tillförlitliga om ett fel uppstår under uppdateringen.

Distributioner med atomär uppdatering tillämpar uppdateringar i sin helhet eller inte alls. Typiskt sett är transaktionella uppdateringssystem också atomära.

Ett system för transaktionsuppdatering skapar en ögonblicksbild som görs före och efter att en uppdatering tillämpas. Om en uppdatering misslyckas när som helst (till exempel på grund av ett strömavbrott) kan uppdateringen enkelt återställas till ett "senast kända goda tillstånd"

The Atomic update method is used for [distributions](../desktop.md#atomic-distributions) like Silverblue, Tumbleweed, and NixOS and can achieve reliability with this model. [Adam Šamalík](https://twitter.com/adsamalik) gav en presentation om hur `rpm-ostree` fungerar med Silverblue:

<div class="yt-embed">
  <iframe width="560" height="315" src="https://invidious.privacyguides.net/embed/-hpV5l-gJnQ?local=true" title="Låt oss prova Fedora Silverblue - ett oföränderligt skrivbordsoperativsystem! - Adam Šamalik" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

### "Säkerhetsfokuserad" distribution

Det råder ofta viss förvirring mellan "säkerhetsfokuserade" fördelningar och "pentesting"-fördelningar. A quick search for “the most secure Linux distribution” will often give results like Kali Linux, Black Arch, or Parrot OS. Dessa distributioner är offensiva distributioner för penetrationstestning som innehåller verktyg för att testa andra system. De innehåller ingen "extra säkerhet" eller defensiva åtgärder som är avsedda för vanlig användning.

### Arch Linux baserade distributioner

Arch and Arch-based distributions are not recommended for those new to Linux (regardless of distribution) as they require regular [system maintenance](https://wiki.archlinux.org/title/System_maintenance). Arch does not have a distribution update mechanism for the underlying software choices. Därför måste du hålla dig uppdaterad om aktuella trender och ta till dig teknik när den ersätter äldre metoder på egen hand.

För ett säkert system förväntas du också ha tillräckliga Linuxkunskaper för att korrekt konfigurera säkerheten för deras system, t.ex. anta ett [obligatoriskt system för åtkomstkontroll](https://en.wikipedia.org/wiki/Mandatory_access_control), konfigurera [kernel module](https://en.wikipedia.org/wiki/Loadable_kernel_module#Security) blacklists, skärpa uppstartsparametrar, manipulera [sysctl](https://en.wikipedia.org/wiki/Sysctl) -parametrar och veta vilka komponenter de behöver, t.ex. [Polkit](https://en.wikipedia.org/wiki/Polkit).

Anyone using the [Arch User Repository (AUR)](https://wiki.archlinux.org/title/Arch_User_Repository) **must** be comfortable auditing PKGBUILDs that they download from that service. AUR packages are community-produced content and are not vetted in any way, and therefore are vulnerable to software supply chain attacks, which has in fact happened [in the past](https://bleepingcomputer.com/news/security/malware-found-in-arch-linux-aur-package-repository).

The AUR should always be used sparingly, and often there is a lot of bad advice on various pages which direct people to blindly use [AUR helpers](https://wiki.archlinux.org/title/AUR_helpers) without sufficient warning. Liknande varningar gäller för användning av tredje parts Personal Package Archives (PPAs) på Debianbaserade distributioner eller Community Projects (COPR) på Fedora.

If you are experienced with Linux and wish to use an Arch-based distribution, we generally recommend mainline Arch Linux over any of its derivatives.

Additionally, we recommend **against** these two Arch derivatives specifically:

- **Manjaro**: Denna distribution håller tillbaka paket i två veckor för att se till att deras egna ändringar inte går sönder, inte för att se till att uppströmsversionen är stabil. När AUR-paket används byggs de ofta med de senaste [-biblioteken](https://en.wikipedia.org/wiki/Library_(computing)) från Arch:s arkiv.
- **Garuda**: They use [Chaotic-AUR](https://aur.chaotic.cx) which automatically and blindly compiles packages from the AUR. Det finns ingen verifieringsprocess för att se till att AUR-paketen inte drabbas av attacker i leveranskedjan.

### Linux-libre-kärnan och "Libre"-distributioner

We recommend **against** using the Linux-libre kernel, since it [removes security mitigations](https://phoronix.com/news/GNU-Linux-Libre-5.7-Released) and [suppresses kernel warnings](https://news.ycombinator.com/item?id=29674846) about vulnerable microcode.

## Allmänna rekommendationer

### Enhetskryptering

De flesta Linux-distributioner har ett alternativ i installationsprogrammet för att aktivera [LUKS](../encryption.md#linux-unified-key-setup) fde. Om det här alternativet inte är inställt vid installationstillfället måste du säkerhetskopiera dina data och installera om, eftersom krypteringen tillämpas efter [diskpartitionering](https://en.wikipedia.org/wiki/Disk_partitioning), men innan [filsystem](https://en.wikipedia.org/wiki/File_system) formateras. Vi föreslår också att du raderar din lagringsenhet på ett säkert sätt:

- [Säker radering av data :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/05/25/secure-data-erasure)

### Växla

Consider using [ZRAM](https://wiki.archlinux.org/title/Zram#Using_zram-generator) instead of a traditional swap file or partition to avoid writing potentially sensitive memory data to persistent storage (and improve performance). Fedora-based distributions [use ZRAM by default](https://fedoraproject.org/wiki/Changes/SwapOnZRAM).

If you require suspend-to-disk (hibernation) functionality, you will still need to use a traditional swap file or partition. Make sure that any swap space you do have on a persistent storage device is [encrypted](https://wiki.archlinux.org/title/Dm-crypt/Swap_encryption) at a minimum to mitigate some of these threats.

### Wayland

We recommend using a desktop environment that supports the [Wayland](https://en.wikipedia.org/wiki/Wayland_(display_server_protocol)) display protocol, as it was developed with security [in mind](https://lwn.net/Articles/589147). Its predecessor ([X11](https://en.wikipedia.org/wiki/X_Window_System)) does not support GUI isolation, which allows any window to [record, log, and inject inputs in other windows](https://blog.invisiblethings.org/2011/04/23/linux-security-circus-on-gui-isolation.html), making any attempt at sandboxing futile. While there are options to do nested X11 such as [Xpra](https://en.wikipedia.org/wiki/Xpra) or [Xephyr](https://en.wikipedia.org/wiki/Xephyr), they often come with negative performance consequences, and are neither convenient to set up nor preferable over Wayland.

Fortunately, [Wayland compositors](https://en.wikipedia.org/wiki/Wayland_(protocol)#Wayland_compositors) such as those included with [GNOME](https://gnome.org) and [KDE Plasma](https://kde.org) now have good support for Wayland along with some other compositors that use [wlroots](https://gitlab.freedesktop.org/wlroots/wlroots/-/wikis/Projects-which-use-wlroots), (e.g. [Sway](https://swaywm.org)). Some distributions like Fedora and Tumbleweed use it by default, and some others may do so in the future as X11 is in [hard maintenance mode](https://phoronix.com/news/X.Org-Maintenance-Mode-Quickly). Om du använder en av dessa miljöer är det lika enkelt som att välja "Wayland"-sessionen i skrivbordsdisplayhanteraren ([GDM](https://en.wikipedia.org/wiki/GNOME_Display_Manager), [SDDM](https://en.wikipedia.org/wiki/Simple_Desktop_Display_Manager)).

Vi rekommenderar **mot** om du använder skrivbordsmiljöer eller fönsterhanterare som inte har stöd för Wayland, till exempel Cinnamon (standard i Linux Mint), Pantheon (standard i Elementary OS), MATE, Xfce och i3.

### Proprietär fast programvara (uppdateringar av mikrokod)

Some Linux distributions (such as [Linux-libre](https://en.wikipedia.org/wiki/Linux-libre)-based or DIY distros) don’t come with the proprietary [microcode](https://en.wikipedia.org/wiki/Microcode) updates which patch critical security vulnerabilities. Some notable examples of these vulnerabilities include [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability)), [Meltdown](https://en.wikipedia.org/wiki/Meltdown_(security_vulnerability)), [SSB](https://en.wikipedia.org/wiki/Speculative_Store_Bypass), [Foreshadow](https://en.wikipedia.org/wiki/Foreshadow), [MDS](https://en.wikipedia.org/wiki/Microarchitectural_Data_Sampling), [SWAPGS](https://en.wikipedia.org/wiki/SWAPGS_(security_vulnerability)), and other [hardware vulnerabilities](https://kernel.org/doc/html/latest/admin-guide/hw-vuln/index.html).

We **highly recommend** that you install microcode updates, as they contain important security patches for the CPU which can not be fully mitigated in software alone. Fedora och openSUSE har båda mikrokoduppdateringar som standard.

### Uppdateringar

De flesta Linuxdistributioner installerar automatiskt uppdateringar eller påminner dig om att göra det. Det är viktigt att hålla operativsystemet uppdaterat så att programvaran korrigeras när en sårbarhet hittas.

Some distributions (particularly those aimed at advanced users) are more bare bones and expect you to do things yourself (e.g. Arch or Debian). Dessa kräver att du kör "pakethanteraren" (`apt`, `pacman`, `dnf`, etc.) manuellt för att få viktiga säkerhetsuppdateringar.

Dessutom hämtar vissa distributioner inte uppdateringar av den fasta programvaran automatiskt. For that, you will need to install [`fwupd`](https://wiki.archlinux.org/title/Fwupd).

## Verktyg för integritet

### Randomisering av MAC-adresser

Many desktop Linux distributions (Fedora, openSUSE, etc.) come with [NetworkManager](https://en.wikipedia.org/wiki/NetworkManager) to configure Ethernet and Wi-Fi settings.

It is possible to [randomize](https://fedoramagazine.org/randomize-mac-address-nm) the [MAC address](https://en.wikipedia.org/wiki/MAC_address) when using NetworkManager. Detta ger lite mer integritet i Wi-Fi-nätverk eftersom det är svårare att spåra specifika enheter i nätverket du är ansluten till. Den [**gör dig inte anonym**](https://papers.mathyvanhoef.com/wisec2016.pdf).

We recommend changing the setting to **random** instead of **stable**, as suggested in the [article](https://fedoramagazine.org/randomize-mac-address-nm).

If you are using [systemd-networkd](https://en.wikipedia.org/wiki/Systemd#Ancillary_components), you will need to set [`MACAddressPolicy=random`](https://freedesktop.org/software/systemd/man/systemd.link.html#MACAddressPolicy=) which will enable [RFC 7844 (Anonymity Profiles for DHCP Clients)](https://freedesktop.org/software/systemd/man/systemd.network.html#Anonymize=).

MAC address randomization is primarily beneficial for Wi-Fi connections. For Ethernet connections, randomizing your MAC address provides little (if any) benefit, because a network administrator can trivially identify your device by other means (such as inspecting the port you are connected to on the network switch). Randomisering av Wi-Fi- MAC-adresser beror på stöd från Wi-Fi-programmets fasta programvara.

### Andra identifierare

Det finns andra systemidentifierare som du bör vara försiktig med. Du bör fundera på om detta gäller för din hotmodell [](../basics/threat-modeling.md):

- **Värdnamn:** Systemets värdnamn delas med de nätverk du ansluter till. Du bör undvika att inkludera identifierande termer som ditt namn eller operativsystem i ditt värdnamn och i stället hålla dig till generiska termer eller slumpmässiga strängar.
- **Användarnamn:** På samma sätt används ditt användarnamn på olika sätt i systemet. Överväg att använda generiska termer som "användare" snarare än ditt faktiska namn.
- **Machine ID:** During installation, a unique machine ID is generated and stored on your device. Consider [setting it to a generic ID](https://madaidans-insecurities.github.io/guides/linux-hardening.html#machine-id).

### System Counting

The Fedora Project [counts](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting) how many unique systems access its mirrors by using a [`countme`](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting#Detailed_Description) variable instead of a unique ID. Fedora does this to determine load and provision better servers for updates where necessary.

This [option](https://dnf.readthedocs.io/en/latest/conf_ref.html#options-for-both-main-and-repo) is currently off by default. We recommend adding `countme=false` to `/etc/dnf/dnf.conf` just in case it is enabled in the future. On systems that use `rpm-ostree` such as Silverblue, the countme option is disabled by masking the [rpm-ostree-countme](https://fedoramagazine.org/getting-better-at-counting-rpm-ostree-based-systems) timer.

openSUSE also uses a [unique ID](https://en.opensuse.org/openSUSE:Statistics) to count systems, which can be disabled by emptying the `/var/lib/zypp/AnonymousUniqueId` file.
