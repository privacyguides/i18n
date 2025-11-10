---
title: Linux Overview
icon: simple/linux
description: Linux is an open-source, privacy-focused desktop operating system alternative, but not all distribitions are created equal.
---

**Linux** is an open-source, privacy-focused desktop operating system alternative. In the face of pervasive telemetry and other privacy-encroaching technologies in mainstream operating systems, desktop Linux has remained the clear choice for people looking for total control over their computers from the ground up.

Our website generally uses the term “Linux” to describe **desktop** Linux distributions. Other operating systems which also use the Linux kernel such as ChromeOS, Android, and Qubes OS are not discussed on this page.

[Våra Linux-rekommendationer :material-arrow-right-drop-circle:](../desktop.md ""){.md-button}

## Security Notes

There are some notable security concerns with Linux which you should be aware of. Despite these drawbacks, desktop Linux distributions are still great for most people who want to:

- Undvik telemetri som ofta kommer med egna operativsystem
- Maintain [software freedom](https://gnu.org/philosophy/free-sw.en.html#four-freedoms)
- Använd integritetsfokuserade system som t. ex. [Whonix](../desktop.md#whonix) eller [Tails](../desktop.md#tails)

### Open-Source Security

It is a [common misconception](../basics/common-misconceptions.md#open-source-software-is-always-secure-or-proprietary-software-is-more-secure) that Linux and other open-source software are inherently secure simply because the source code is available. There is an expectation that community verification occurs regularly, but this isn’t always [the case](https://seirdy.one/posts/2022/02/02/floss-security).

In reality, distro security depends on a number of factors, such as project activity, developer experience, the level of rigor applied to code reviews, and how often attention is given to specific parts of the codebase that may go untouched for years.

### Missing Security Features

At the moment, desktop Linux [falls behind alternatives](https://discussion.fedoraproject.org/t/fedora-strategy-2028-proposal-fedora-linux-is-as-secure-as-macos/46899/9) like macOS or Android when it comes to certain security features. We hope to see improvements in these areas in the future.

- **Verified boot** on Linux is not as robust as alternatives such as Apple’s [Secure Boot](https://support.apple.com/guide/security/secac71d5623/web) or Android’s [Verified Boot](https://source.android.com/security/verifiedboot). Verified boot prevents persistent tampering by malware and [evil maid attacks](https://en.wikipedia.org/wiki/Evil_Maid_attack), but is still largely [unavailable on even the most advanced distributions](https://discussion.fedoraproject.org/t/has-silverblue-achieved-verified-boot/27251/3).

- **Strong sandboxing** for apps on Linux is severely lacking, even with containerized apps like Flatpaks or sandboxing solutions like Firejail. Flatpak is the most promising sandboxing utility for Linux thus far, but is still deficient in many areas and allows for [unsafe defaults](https://flatkill.org/2020) which permit most apps to trivially bypass their sandbox.

Additionally, Linux falls behind in implementing [exploit mitigations](https://madaidans-insecurities.github.io/linux.html#exploit-mitigations) which are now standard on other operating systems, such as Arbitrary Code Guard on Windows or Hardened Runtime on macOS. Also, most Linux programs and Linux itself are coded in memory-unsafe languages. Memory corruption bugs are responsible for the [majority of vulnerabilities](https://msrc.microsoft.com/blog/2019/07/a-proactive-approach-to-more-secure-code) fixed and assigned a CVE. While this is also true for Windows and macOS, they are quickly making progress on adopting memory-safe languages such as Rust and Swift, respectively.

## Välja din distribution

Inte alla Linux-distributioner är skapade lika. Our [Linux recommendation page](../desktop.md) is not meant to be an authoritative source on which distribution you should use, but our recommendations *are* aligned with the following guidelines. These are a few things you should keep in mind when choosing a distribution:

### Utgivningscykel

Vi rekommenderar starkt att du väljer distributioner som ligger nära de stabila uppströmsutgåvorna, ofta kallade rullande utgåvor. Detta beror på att frysta utgåvor ofta inte uppdaterar paketversioner och hamnar bakom säkerhetsuppdateringar.

For frozen distributions such as [Debian](https://debian.org/security/faq#handling), package maintainers are expected to backport patches to fix vulnerabilities rather than bump the software to the “next version” released by the upstream developer. Some security fixes (particularly for less popular software) [do not](https://arxiv.org/abs/2105.14565) receive a [CVE ID](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures) at all and therefore do not make it into the distribution with this patching model. As a result, minor security fixes are sometimes held back until the next major release.

Vi tror inte att hålla paket tillbaka och tillämpa tillfälliga patchar är en bra idé, eftersom det skiljer sig från hur utvecklaren kan ha avsett att programvaran ska fungera. [Richard Brown](https://rootco.de/aboutme) has a presentation about this:

- [Regular Releases are Wrong, Roll for your life](https://youtu.be/i8c0mg_mS7U) <small>(YouTube)</small>

### Traditional vs Atomic Updates

Traditionellt sett uppdaterar Linuxdistributioner genom att sekventiellt uppdatera de önskade paketen. Traditional updates such as those used in Fedora, Arch Linux, and Debian-based distributions can be less reliable if an error occurs while updating.

Distros which use atomic updates, on the other hand, apply updates in full or not at all. On an atomic distribution, if an error occurs while updating (perhaps due to a power failure), nothing is changed on the system.

The atomic update method can achieve reliability with this model and is used for [distributions](../desktop.md#atomic-distributions) like Silverblue and NixOS. [Adam Šamalík](https://twitter.com/adsamalik) provides a presentation on how `rpm-ostree` works with Silverblue:

- [Let's try Fedora Silverblue — an immutable desktop OS! - Adam Šamalík](https://youtu.be/-hpV5l-gJnQ) <small>(YouTube)</small>

### "Säkerhetsfokuserad" distribution

Det råder ofta viss förvirring mellan "säkerhetsfokuserade" fördelningar och "pentesting"-fördelningar. A quick search for “the most secure Linux distribution” will often give results like Kali Linux, Black Arch, or Parrot OS. Dessa distributioner är offensiva distributioner för penetrationstestning som innehåller verktyg för att testa andra system. De innehåller ingen "extra säkerhet" eller defensiva åtgärder som är avsedda för vanlig användning.

### Arch Linux baserade distributioner

Arch and Arch-based distributions are not recommended for those new to Linux (regardless of distribution) as they require regular [system maintenance](https://wiki.archlinux.org/title/System_maintenance). Arch does not have a distribution update mechanism for the underlying software choices. As a result you have to stay aware with current trends and adopt technologies on your own as they supersede older practices.

For a secure system, you are also expected to have sufficient Linux knowledge to properly set up security for their system such as adopting a [mandatory access control](#mandatory-access-control) system, setting up [kernel module](https://en.wikipedia.org/wiki/Loadable_kernel_module#Security) blacklists, hardening boot parameters, manipulating [sysctl](https://en.wikipedia.org/wiki/Sysctl) parameters, and knowing what components they need such as [Polkit](https://en.wikipedia.org/wiki/Polkit).

Anyone using the [Arch User Repository (AUR)](https://wiki.archlinux.org/title/Arch_User_Repository) **must** be comfortable auditing PKGBUILDs that they download from that service. AUR packages are community-produced content and are not vetted in any way, and therefore are vulnerable to software [:material-package-variant-closed-remove: Supply Chain Attacks](../basics/common-threats.md#attacks-against-certain-organizations ""){.pg-viridian}, which has in fact happened [in the past](https://bleepingcomputer.com/news/security/malware-found-in-arch-linux-aur-package-repository).

The AUR should always be used sparingly, and often there is a lot of bad advice on various pages which direct people to blindly use [AUR helpers](https://wiki.archlinux.org/title/AUR_helpers) without sufficient warning. Similar warnings apply to the use of third-party Personal Package Archives (PPAs) on Debian-based distributions or Community Projects (COPR) on Fedora.

If you are experienced with Linux and wish to use an Arch-based distribution, we generally recommend mainline Arch Linux over any of its derivatives.

Additionally, we recommend **against** these two Arch derivatives specifically:

- **Manjaro**: Denna distribution håller tillbaka paket i två veckor för att se till att deras egna ändringar inte går sönder, inte för att se till att uppströmsversionen är stabil. När AUR-paket används byggs de ofta med de senaste [-biblioteken](https://en.wikipedia.org/wiki/Library_(computing)) från Arch:s arkiv.
- **Garuda**: They use [Chaotic-AUR](https://aur.chaotic.cx) which automatically and blindly compiles packages from the AUR. Det finns ingen verifieringsprocess för att se till att AUR-paketen inte drabbas av attacker i leveranskedjan.

### Linux-libre-kärnan och "Libre"-distributioner

We recommend **against** using the Linux-libre kernel, since it [removes security mitigations](https://phoronix.com/news/GNU-Linux-Libre-5.7-Released) and [suppresses kernel warnings](https://news.ycombinator.com/item?id=29674846) about vulnerable microcode.

### Mandatory access control

Mandatory access control is a set of additional security controls which help to confine parts of the system such as apps and system services. The two common forms of mandatory access control found in Linux distributions are [SELinux](https://github.com/SELinuxProject) and [AppArmor](https://apparmor.net). Fedora and Tumbleweed use SELinux by default, with Tumbleweed offering an option in its installer to choose AppArmor instead.

SELinux on [Fedora](https://docs.fedoraproject.org/en-US/quick-docs/selinux-getting-started) confines Linux containers, virtual machines, and service daemons by default. AppArmor is used by the snap daemon for [sandboxing](https://snapcraft.io/docs/security-sandboxing) snaps which have [strict](https://snapcraft.io/docs/snap-confinement) confinement such as [Firefox](https://snapcraft.io/firefox). There is a community effort to confine more parts of the system in Fedora with the [ConfinedUsers](https://fedoraproject.org/wiki/SIGs/ConfinedUsers) special interest group.

## Allmänna rekommendationer

### Enhetskryptering

De flesta Linux-distributioner har ett alternativ i installationsprogrammet för att aktivera [LUKS](../encryption.md#linux-unified-key-setup) fde. If this option isn’t set at installation time, you will have to back up your data and re-install, as encryption is applied after [disk partitioning](https://en.wikipedia.org/wiki/Disk_partitioning), but before [file systems](https://en.wikipedia.org/wiki/File_system) are formatted. Vi föreslår också att du raderar din lagringsenhet på ett säkert sätt:

- [Säker radering av data :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/05/25/secure-data-erasure)

### Växla

Consider using [ZRAM](https://wiki.archlinux.org/title/Zram#Using_zram-generator) instead of a traditional swap file or partition to avoid writing potentially sensitive memory data to persistent storage (and improve performance). Fedora-based distributions [use ZRAM by default](https://fedoraproject.org/wiki/Changes/SwapOnZRAM).

If you require suspend-to-disk (hibernation) functionality, you will still need to use a traditional swap file or partition. Make sure that any swap space you do have on a persistent storage device is [encrypted](https://wiki.archlinux.org/title/Dm-crypt/Swap_encryption) at a minimum to mitigate some of these threats.

### Proprietär fast programvara (uppdateringar av mikrokod)

Some Linux distributions (such as [Linux-libre](https://en.wikipedia.org/wiki/Linux-libre)-based or DIY distros) don’t come with the proprietary [microcode](https://en.wikipedia.org/wiki/Microcode) updates which patch critical security vulnerabilities. Some notable examples of these vulnerabilities include [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability)), [Meltdown](https://en.wikipedia.org/wiki/Meltdown_(security_vulnerability)), [SSB](https://en.wikipedia.org/wiki/Speculative_Store_Bypass), [Foreshadow](https://en.wikipedia.org/wiki/Foreshadow), [MDS](https://en.wikipedia.org/wiki/Microarchitectural_Data_Sampling), [SWAPGS](https://en.wikipedia.org/wiki/SWAPGS_(security_vulnerability)), and other [hardware vulnerabilities](https://kernel.org/doc/html/latest/admin-guide/hw-vuln/index.html).

We **highly recommend** that you install microcode updates, as they contain important security patches for the CPU which can not be fully mitigated in software alone. Fedora and openSUSE both apply microcode updates by default.

### Uppdateringar

De flesta Linuxdistributioner installerar automatiskt uppdateringar eller påminner dig om att göra det. Det är viktigt att hålla operativsystemet uppdaterat så att programvaran korrigeras när en sårbarhet hittas.

Some distributions (particularly those aimed at advanced users) are more bare bones and expect you to do things yourself (e.g. Arch or Debian). Dessa kräver att du kör "pakethanteraren" (`apt`, `pacman`, `dnf`, etc.) manuellt för att få viktiga säkerhetsuppdateringar.

Dessutom hämtar vissa distributioner inte uppdateringar av den fasta programvaran automatiskt. For that, you will need to install [`fwupd`](https://wiki.archlinux.org/title/Fwupd).

### Permission Controls

Desktop environments that support the [Wayland](https://wayland.freedesktop.org) display protocol are [more secure](https://lwn.net/Articles/589147) than those that only support X11. Moreover, we *generally* recommend installing and using applications which are sandboxed such as those obtained via **Flatpak**. Flatpak supports the [`security-context-v1`](https://github.com/flatpak/flatpak/pull/4920) protocol and the ability to filter D-Bus protocols, which allow Flatpak to properly identify apps for the purpose of sandboxing them through permission controls.[^1] Conversely, applications outside sandboxes are free to perform privileged actions such as capturing your screen, either by [overwriting the portal permission store](https://invent.kde.org/plasma/xdg-desktop-portal-kde/-/issues/7#note_1112260), or [making use of privileged Wayland protocols](https://github.com/swaywm/sway/pull/7648#issuecomment-2507730794).

## Verktyg för integritet

### Randomisering av MAC-adresser

Many desktop Linux distributions (Fedora, openSUSE, etc.) come with [NetworkManager](https://en.wikipedia.org/wiki/NetworkManager) to configure Ethernet and Wi-Fi settings.

It is possible to randomize the [MAC address](https://en.wikipedia.org/wiki/MAC_address) when using NetworkManager. Detta ger lite mer integritet i Wi-Fi-nätverk eftersom det är svårare att spåra specifika enheter i nätverket du är ansluten till. Den [**gör dig inte anonym**](https://papers.mathyvanhoef.com/wisec2016.pdf).

In the terminal, create a new file `/etc/NetworkManager/conf.d/00-macrandomize.conf` and add the following to it:

```text
[device]
wifi.scan-rand-mac-address=yes

[connection]
wifi.cloned-mac-address=random
ethernet.cloned-mac-address=random
```

Then, restart NetworkManager:

```sh
systemctl restart NetworkManager
```

Optionally, changing the connection parameter from `random` to `stable` will give you a random MAC address *per network*, but keep it stable for that network when you reconnect to it later. Using `random` will give you a random MAC address *per connection*. This may be desirable for networks with captive portals or where you have a static DHCP assignment, at the expense of making you more identifiable by a single network operator you connect to multiple times.

If you are using [systemd-networkd](https://en.wikipedia.org/wiki/Systemd#Ancillary_components), you will need to set [`MACAddressPolicy=random`](https://freedesktop.org/software/systemd/man/systemd.link.html#MACAddressPolicy=) which will enable [RFC 7844 (Anonymity Profiles for DHCP Clients)](https://freedesktop.org/software/systemd/man/systemd.network.html#Anonymize=).

MAC address randomization is primarily beneficial for Wi-Fi connections. For Ethernet connections, randomizing your MAC address provides little (if any) benefit, because a network administrator can trivially identify your device by other means (such as inspecting the port you are connected to on the network switch). Randomisering av Wi-Fi- MAC-adresser beror på stöd från Wi-Fi-programmets fasta programvara.

### Andra identifierare

Det finns andra systemidentifierare som du bör vara försiktig med. Du bör fundera på om detta gäller för din hotmodell [](../basics/threat-modeling.md):

- **Värdnamn:** Systemets värdnamn delas med de nätverk du ansluter till. Du bör undvika att inkludera identifierande termer som ditt namn eller operativsystem i ditt värdnamn och i stället hålla dig till generiska termer eller slumpmässiga strängar.
- **Användarnamn:** På samma sätt används ditt användarnamn på olika sätt i systemet. Överväg att använda generiska termer som "användare" snarare än ditt faktiska namn.
- **Machine ID:** During installation, a unique machine ID is generated and stored on your device. Consider [setting it to a generic ID](https://madaidans-insecurities.github.io/guides/linux-hardening.html#machine-id).

### System Counting

The Fedora Project [counts](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting) how many unique systems access its mirrors by using a [`countme`](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting#Detailed_Description) variable instead of a unique ID. Fedora does this to determine load and provision better servers for updates where necessary.

This [option](https://dnf.readthedocs.io/en/latest/conf_ref.html#options-for-both-main-and-repo) is currently off by default. We recommend adding `countme=false` to `/etc/dnf/dnf.conf` just in case it is enabled in the future. On systems that use `rpm-ostree` such as Silverblue, the `countme` option is disabled by masking the [rpm-ostree-countme](https://fedoramagazine.org/getting-better-at-counting-rpm-ostree-based-systems) timer.

openSUSE also uses a [unique ID](https://en.opensuse.org/openSUSE:Statistics) to count systems, which can be disabled by emptying the `/var/lib/zypp/AnonymousUniqueId` file.

[^1]: This exposes a reliable way for Wayland compositors to get identifying information about a client. Compositors can then apply security policies if desirable. [https://github.com/flatpak/flatpak/commit/f0e626a4b60439f211f06d35df74b675a9ef42f4](https://github.com/flatpak/flatpak/commit/f0e626a4b60439f211f06d35df74b675a9ef42f4)
