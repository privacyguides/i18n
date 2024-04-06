---
title: Gambaran Umum Linux
icon: simple/linux
description: Linux adalah alternatif sistem operasi desktop sumber terbuka yang berfokus pada privasi, tetapi tidak semua distribusi diciptakan sama.
---

**Linux** adalah alternatif sistem operasi komputer sumber terbuka yang berfokus pada privasi. Dalam menghadapi telemetri yang merajalela dan teknologi lain yang melanggar privasi dalam sistem operasi utama, Linux tetap menjadi pilihan yang jelas bagi mereka yang mencari kendali penuh atas komputer mereka dari awal.

Situs web kami umumnya menggunakan istilah "Linux" untuk menjelaskan distribusi Linux **desktop**. Sistem operasi lain yang juga menggunakan kernel Linux seperti ChromeOS, Android, dan Qubes OS tidak dibahas di halaman ini.

[Rekomendasi Linux kami :material-arrow-right-drop-circle:](../desktop.md ""){.md-button}

## Catatan Privasi

Ada beberapa masalah privasi penting pada Linux yang harus Anda sadari. Terlepas dari kekurangan ini, distribusi Linux desktop masih bagus untuk kebanyakan orang yang ingin:

- Menghindari telemetri yang sering kali disertakan dengan sistem operasi berpemilik
- Menjaga [kebebasan perangkat lunak](https://gnu.org/philosophy/free-sw.en.html#four-freedoms)
- Menggunakan sistem yang berfokus pada privasi seperti [Whonix](https://whonix.org) atau [Tails](https://tails.net)

### Keamanan Sumber Terbuka

Adalah [kesalahpahaman umum](../basics/common-misconceptions.md#open-source-software-is-always-secure-or-proprietary-software-is-more-secure) bahwa Linux dan perangkat lunak sumber terbuka lainnya secara inheren aman hanya karena kode sumbernya terbuka. Ada ekspektasi bahwa verifikasi komunitas dilakukan secara teratur, tetapi tidak selalu [demikian](https://seirdy.one/posts/2022/02/02/floss-security).

Kenyataannya, keamanan distro bergantung pada sejumlah faktor, seperti aktivitas proyek, pengalaman pengembang, tingkat ketelitian yang diterapkan pada tinjauan kode, dan seberapa sering perhatian diberikan pada bagian tertentu dari basis kode yang mungkin tidak tersentuh selama bertahun-tahun.

### Fitur Keamanan yang tidak terdapat pada Linux

Saat ini, Linux [tertinggal jika dibandingkan alternatif](https://discussion.fedoraproject.org/t/fedora-strategy-2028-proposal-fedora-linux-is-as-secure-as-macos/46899/9) seperti macOS atau Android dalam hal fitur keamanan tertentu. Kami berharap dapat melihat peningkatan di area ini di masa depan.

- **Boot terverifikasi** di Linux tidak sekuat alternatif seperti [Secure Boot](https://support.apple.com/guide/security/secac71d5623/web)-nya Apple atau [Verified Boot](https://source.android.com/security/verifiedboot)-nya Android. Boot terverifikasi mencegah gangguan terus-menerus oleh *malware* dan [serangan pembantu jahat](https://en.wikipedia.org/wiki/Evil_Maid_attack), tetapi sebagian besar masih belum [tersedia pada distribusi yang paling canggih](https://discussion.fedoraproject.org/t/has-silverblue-achieved-verified-boot/27251/3) sekalipun.

- ***Sandboxing* yang kuat** untuk aplikasi di Linux sangat kurang, bahkan dengan aplikasi yang terkontainerisasi seperti Flatpaks atau solusi *sandbox* seperti Firejail. Flatpak adalah utilitas *sandbox* yang paling menjanjikan untuk Linux sejauh ini, tetapi masih memiliki kekurangan di banyak area dan memungkinkan [bawaan](https://flatkill.org/2020) yang [tidak aman](https://flatkill.org/2020) yang memungkinkan sebagian besar aplikasi melewati *sandbox* mereka.

Selain itu, Linux tertinggal dalam mengimplementasikan [mitigasi eksploitasi](https://madaidans-insecurities.github.io/linux.html#exploit-mitigations) yang sekarang menjadi standar pada sistem operasi lain, seperti Arbitrary Code Guard pada Windows atau Hardened Runtime pada macOS. Sebagian besar program Linux dan Linux itu sendiri juga dikodekan dalam bahasa yang tidak aman untuk memori. *Bug* korupsi memori bertanggung jawab atas [sebagian besar kerentanan](https://msrc.microsoft.com/blog/2019/07/a-proactive-approach-to-more-secure-code) yang diperbaiki dan diberi CVE. Meskipun hal ini juga berlaku untuk Windows dan macOS, kedua sistem operasi tersebut dengan cepat membuat kemajuan dalam mengadopsi bahasa yang aman dari segi memori - masing-masing seperti Rust dan Swift - sementara tidak ada upaya yang sama untuk menulis ulang Linux dalam bahasa yang aman dari segi memori seperti Rust.

## Memilih distribusi Anda

Tidak semua distribusi Linux diciptakan sama. [Halaman rekomendasi Linux](../desktop.md) kami tidak dimaksudkan sebagai sumber otoritatif tentang distribusi mana yang harus Anda gunakan, tetapi rekomendasi kami *selaras* dengan pedoman berikut. Berikut ini adalah beberapa hal yang harus Anda ingat ketika memilih distribusi:

### Siklus rilis

Kami sangat menyarankan agar Anda memilih distribusi yang dekat dengan rilis perangkat lunak hulu yang stabil, yang sering disebut sebagai distribusi *rolling release*. Hal ini karena distribusi siklus *frozen release* sering kali tidak memperbarui versi paket dan tertinggal dalam pembaruan keamanan.

Untuk distribusi *frozen* seperti [Debian](https://debian.org/security/faq#handling), pengelola paket diharapkan untuk melakukan *backport patch* untuk memperbaiki kerentanan alih-alih memindahkan perangkat lunak ke "versi berikutnya" yang dirilis oleh pengembang hulu. Beberapa perbaikan keamanan [tidak](https://arxiv.org/abs/2105.14565) menerima [ID CVE](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures) (terutama perangkat lunak yang kurang populer) sama sekali dan oleh karena itu tidak masuk ke dalam distribusi dengan model penambalan ini. Akibatnya, perbaikan keamanan kecil terkadang tertunda hingga rilis besar berikutnya.

Kami tidak percaya bahwa menahan paket dan menerapkan tambalan sementara adalah ide yang bagus, karena hal ini menyimpang dari cara kerja perangkat lunak yang diinginkan oleh pengembang. [Richard Brown](https://rootco.de/aboutme) memiliki presentasi tentang hal ini:

<div class="yt-embed">
  <iframe width="560" height="315" src="https://invidious.privacyguides.net/embed/i8c0mg_mS7U?local=true" title="Regular Releases are Wrong, Roll for your life" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

### Pembaruan Tradisional vs Atomik

Secara tradisional, distribusi Linux melakukan pembaruan dengan memperbarui paket yang diinginkan secara berurutan. Pembaruan tradisional seperti yang digunakan pada distribusi berbasis Fedora, Arch Linux, dan Debian bisa jadi kurang dapat diandalkan jika terjadi kesalahan saat melakukan pembaruan.

Atomic updating distributions apply updates in full or not at all. Typically, transactional update systems are also atomic.

A transactional update system creates a snapshot that is made before and after an update is applied. If an update fails at any time (perhaps due to a power failure), the update can be easily rolled back to a “last known good state."

The Atomic update method is used for [distributions](../desktop.md#atomic-distributions) like Silverblue, Tumbleweed, and NixOS and can achieve reliability with this model. [Adam Šamalík](https://twitter.com/adsamalik) provided a presentation on how `rpm-ostree` works with Silverblue:

<div class="yt-embed">
  <iframe width="560" height="315" src="https://invidious.privacyguides.net/embed/-hpV5l-gJnQ?local=true" title="Let's try Fedora Silverblue — an immutable desktop OS! - Adam Šamalik" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

### “Security-focused” distributions

There is often some confusion between “security-focused” distributions and “pentesting” distributions. A quick search for “the most secure Linux distribution” will often give results like Kali Linux, Black Arch, or Parrot OS. These distributions are offensive penetration testing distributions that bundle tools for testing other systems. They don’t include any “extra security” or defensive mitigations intended for regular use.

### Arch-based distributions

Arch and Arch-based distributions are not recommended for those new to Linux (regardless of distribution) as they require regular [system maintenance](https://wiki.archlinux.org/title/System_maintenance). Arch does not have a distribution update mechanism for the underlying software choices. As a result you have to stay aware with current trends and adopt technologies as they supersede older practices on your own.

For a secure system, you are also expected to have sufficient Linux knowledge to properly set up security for their system such as adopting a [mandatory access control](https://en.wikipedia.org/wiki/Mandatory_access_control) system, setting up [kernel module](https://en.wikipedia.org/wiki/Loadable_kernel_module#Security) blacklists, hardening boot parameters, manipulating [sysctl](https://en.wikipedia.org/wiki/Sysctl) parameters, and knowing what components they need such as [Polkit](https://en.wikipedia.org/wiki/Polkit).

Anyone using the [Arch User Repository (AUR)](https://wiki.archlinux.org/title/Arch_User_Repository) **must** be comfortable auditing PKGBUILDs that they download from that service. AUR packages are community-produced content and are not vetted in any way, and therefore are vulnerable to software supply chain attacks, which has in fact happened [in the past](https://bleepingcomputer.com/news/security/malware-found-in-arch-linux-aur-package-repository).

The AUR should always be used sparingly, and often there is a lot of bad advice on various pages which direct people to blindly use [AUR helpers](https://wiki.archlinux.org/title/AUR_helpers) without sufficient warning. Similar warnings apply to use third-party Personal Package Archives (PPAs) on Debian based distributions or Community Projects (COPR) on Fedora.

If you are experienced with Linux and wish to use an Arch-based distribution, we generally recommend mainline Arch Linux over any of its derivatives.

Additionally, we recommend **against** these two Arch derivatives specifically:

- **Manjaro**: This distribution holds packages back for 2 weeks to make sure that their own changes don’t break, not to make sure that upstream is stable. When AUR packages are used, they are often built against the latest [libraries](https://en.wikipedia.org/wiki/Library_(computing)) from Arch’s repositories.
- **Garuda**: They use [Chaotic-AUR](https://aur.chaotic.cx) which automatically and blindly compiles packages from the AUR. There is no verification process to make sure that the AUR packages don’t suffer from supply chain attacks.

### Linux-libre kernel and “Libre” distributions

We recommend **against** using the Linux-libre kernel, since it [removes security mitigations](https://phoronix.com/news/GNU-Linux-Libre-5.7-Released) and [suppresses kernel warnings](https://news.ycombinator.com/item?id=29674846) about vulnerable microcode.

## General Recommendations

### Drive Encryption

Most Linux distributions have an option within its installer for enabling [LUKS](../encryption.md#linux-unified-key-setup) FDE. If this option isn’t set at installation time, you will have to backup your data and re-install, as encryption is applied after [disk partitioning](https://en.wikipedia.org/wiki/Disk_partitioning), but before [file systems](https://en.wikipedia.org/wiki/File_system) are formatted. We also suggest securely erasing your storage device:

- [Secure Data Erasure :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/05/25/secure-data-erasure)

### Swap

Consider using [ZRAM](https://wiki.archlinux.org/title/Zram#Using_zram-generator) instead of a traditional swap file or partition to avoid writing potentially sensitive memory data to persistent storage (and improve performance). Fedora-based distributions [use ZRAM by default](https://fedoraproject.org/wiki/Changes/SwapOnZRAM).

If you require suspend-to-disk (hibernation) functionality, you will still need to use a traditional swap file or partition. Make sure that any swap space you do have on a persistent storage device is [encrypted](https://wiki.archlinux.org/title/Dm-crypt/Swap_encryption) at a minimum to mitigate some of these threats.

### Wayland

We recommend using a desktop environment that supports the [Wayland](https://en.wikipedia.org/wiki/Wayland_(display_server_protocol)) display protocol, as it was developed with security [in mind](https://lwn.net/Articles/589147). Its predecessor ([X11](https://en.wikipedia.org/wiki/X_Window_System)) does not support GUI isolation, which allows any window to [record, log, and inject inputs in other windows](https://blog.invisiblethings.org/2011/04/23/linux-security-circus-on-gui-isolation.html), making any attempt at sandboxing futile. While there are options to do nested X11 such as [Xpra](https://en.wikipedia.org/wiki/Xpra) or [Xephyr](https://en.wikipedia.org/wiki/Xephyr), they often come with negative performance consequences, and are neither convenient to set up nor preferable over Wayland.

Fortunately, [wayland compositors](https://en.wikipedia.org/wiki/Wayland_(protocol)#Wayland_compositors) such as those included with [GNOME](https://gnome.org) and [KDE Plasma](https://kde.org) now have good support for Wayland along with some other compositors that use [wlroots](https://gitlab.freedesktop.org/wlroots/wlroots/-/wikis/Projects-which-use-wlroots), (e.g. [Sway](https://swaywm.org)). Some distributions like Fedora and Tumbleweed use it by default, and some others may do so in the future as X11 is in [hard maintenance mode](https://phoronix.com/news/X.Org-Maintenance-Mode-Quickly). If you’re using one of those environments it is as easy as selecting the “Wayland” session at the desktop display manager ([GDM](https://en.wikipedia.org/wiki/GNOME_Display_Manager), [SDDM](https://en.wikipedia.org/wiki/Simple_Desktop_Display_Manager)).

We recommend **against** using desktop environments or window managers that do not have Wayland support, such as Cinnamon (default on Linux Mint), Pantheon (default on Elementary OS), MATE, Xfce, and i3.

### Proprietary Firmware (Microcode Updates)

Some Linux distributions (such as [Linux-libre](https://en.wikipedia.org/wiki/Linux-libre)-based or DIY distros) don’t come with the proprietary [microcode](https://en.wikipedia.org/wiki/Microcode) updates which patch critical security vulnerabilities. Some notable examples of these vulnerabilities include [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability)), [Meltdown](https://en.wikipedia.org/wiki/Meltdown_(security_vulnerability)), [SSB](https://en.wikipedia.org/wiki/Speculative_Store_Bypass), [Foreshadow](https://en.wikipedia.org/wiki/Foreshadow), [MDS](https://en.wikipedia.org/wiki/Microarchitectural_Data_Sampling), [SWAPGS](https://en.wikipedia.org/wiki/SWAPGS_(security_vulnerability)), and other [hardware vulnerabilities](https://kernel.org/doc/html/latest/admin-guide/hw-vuln/index.html).

We **highly recommend** that you install microcode updates, as they contain important security patches for the CPU which can not be fully mitigated in software alone. Fedora and openSUSE both have the microcode updates applied by default.

### Updates

Most Linux distributions will automatically install updates or remind you to do so. It is important to keep your OS up to date so that your software is patched when a vulnerability is found.

Some distributions (particularly those aimed at advanced users) are more bare bones and expect you to do things yourself (e.g. Arch or Debian). These will require running the "package manager" (`apt`, `pacman`, `dnf`, etc.) manually in order to receive important security updates.

Additionally, some distributions will not download firmware updates automatically. For that you will need to install [`fwupd`](https://wiki.archlinux.org/title/Fwupd).

## Privacy Tweaks

### MAC Address Randomization

Many desktop Linux distributions (Fedora, openSUSE, etc.) come with [NetworkManager](https://en.wikipedia.org/wiki/NetworkManager) to configure Ethernet and Wi-Fi settings.

It is possible to [randomize](https://fedoramagazine.org/randomize-mac-address-nm) the [MAC address](https://en.wikipedia.org/wiki/MAC_address) when using NetworkManager. This provides a bit more privacy on Wi-Fi networks as it makes it harder to track specific devices on the network you’re connected to. It does [**not**](https://papers.mathyvanhoef.com/wisec2016.pdf) make you anonymous.

We recommend changing the setting to **random** instead of **stable**, as suggested in the [article](https://fedoramagazine.org/randomize-mac-address-nm).

If you are using [systemd-networkd](https://en.wikipedia.org/wiki/Systemd#Ancillary_components), you will need to set [`MACAddressPolicy=random`](https://freedesktop.org/software/systemd/man/systemd.link.html#MACAddressPolicy=) which will enable [RFC 7844 (Anonymity Profiles for DHCP Clients)](https://freedesktop.org/software/systemd/man/systemd.network.html#Anonymize=).

MAC address randomization is primarily beneficial for Wi-Fi connections. For Ethernet connections, randomizing your MAC address provides little (if any) benefit, because a network administrator can trivially identify your device by other means (such as inspecting the port you are connected to on the network switch). Randomizing Wi-Fi MAC addresses depends on support from the Wi-Fi’s firmware.

### Other Identifiers

There are other system identifiers which you may wish to be careful about. You should give this some thought to see if it applies to your [threat model](../basics/threat-modeling.md):

- **Hostnames:** Your system's hostname is shared with the networks you connect to. You should avoid including identifying terms like your name or operating system in your hostname, instead sticking to generic terms or random strings.
- **Usernames:** Similarly, your username is used in a variety of ways across your system. Consider using generic terms like "user" rather than your actual name.
- **Machine ID:**: During installation a unique machine ID is generated and stored on your device. Consider [setting it to a generic ID](https://madaidans-insecurities.github.io/guides/linux-hardening.html#machine-id).

### System Counting

The Fedora Project [counts](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting) how many unique systems access its mirrors by using a [`countme`](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting#Detailed_Description) variable instead of a unique ID. Fedora does this to determine load and provision better servers for updates where necessary.

This [option](https://dnf.readthedocs.io/en/latest/conf_ref.html#options-for-both-main-and-repo) is currently off by default. We recommend adding `countme=false` to `/etc/dnf/dnf.conf` just in case it is enabled in the future. On systems that use `rpm-ostree` such as Silverblue, the countme option is disabled by masking the [rpm-ostree-countme](https://fedoramagazine.org/getting-better-at-counting-rpm-ostree-based-systems) timer.

openSUSE also uses a [unique ID](https://en.opensuse.org/openSUSE:Statistics) to count systems, which can be disabled by deleting the `/var/lib/zypp/AnonymousUniqueId` file.
