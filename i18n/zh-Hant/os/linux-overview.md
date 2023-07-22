---
title: Linux概述
icon: simple/linux
description: Linux 為開源、以隱私為中心的桌面作業系統替代選項，但並非所有發行版都一模一樣。
---

**Linux** is an open-source, privacy-focused desktop operating system alternative. In the face of pervasive telemetry and other privacy-encroaching technologies in mainstream operating systems, Linux desktop has remained the clear choice for people looking for total control over their computers from the ground up.

Our website generally uses the term “Linux” to describe **desktop** Linux distributions. Other operating systems which also use the Linux kernel such as ChromeOS, Android, and Qubes OS are not discussed on this page.

[建議的 Linux 發行版 :material-arrow-right-drop-circle:](../desktop.md ""){.md-button}

## 隱私筆記

There are some notable privacy concerns with Linux which you should be aware of. Despite these drawbacks, desktop Linux distributions are still great for most people who want to:

- 避免商業作業系統經常出現的遙測現象
- 保持 [軟體自由](https://www.gnu.org/philosophy/free-sw.en.html#four-freedoms)
- Use privacy focused systems such as [Whonix](https://www.whonix.org) or [Tails](https://tails.boum.org/)

### Open Source Security

It is a [common misconception](../basics/common-misconceptions.md#open-source-software-is-always-secure-or-proprietary-software-is-more-secure) that Linux and other open-source software is inherently secure simply because the source code is available. There is an expectation that community verification occurs regularly, but this isn’t always [the case](https://seirdy.one/posts/2022/02/02/floss-security/).

In reality, distro security depends on a number of factors, such as project activity, developer experience, the level of rigor applied to code reviews, and how often attention is given to specific parts of the codebase that may go untouched for years.

### Missing Security Features

At the moment, desktop Linux [falls behind alternatives](https://discussion.fedoraproject.org/t/fedora-strategy-2028-proposal-fedora-linux-is-as-secure-as-macos/46899/9) like macOS or Android when it comes to certain security features. We hope to see improvements in these areas in the future.

- **Verified boot** on Linux is not as robust as alternatives such as Apple’s [Secure Boot](https://support.apple.com/guide/security/secac71d5623/web) or Android’s [Verified Boot](https://source.android.com/security/verifiedboot). Verified boot prevents persistent tampering by malware and [evil maid attacks](https://en.wikipedia.org/wiki/Evil_Maid_attack), but is still largely [unavailable on even the most advanced distributions](https://discussion.fedoraproject.org/t/has-silverblue-achieved-verified-boot/27251/3).

- **Strong sandboxing** for apps on Linux is severely lacking, even with containerized apps like Flatpaks or sandboxing solutions like Firejail. Flatpak is the most promising sandboxing utility for Linux thus far, but is still deficient in many areas and allows for [unsafe defaults](https://flatkill.org/2020/) which allow most apps to trivially bypass their sandbox.

Additionally, Linux falls behind in implementing [exploit mitigations](https://madaidans-insecurities.github.io/linux.html#exploit-mitigations) which are now standard on other operating systems, such as Arbitrary Code Guard on Windows or Hardened Runtime on macOS. Also, most Linux programs and Linux itself are coded in memory-unsafe languages. Memory corruption bugs are responsible for the [majority of vulnerabilities](https://msrc.microsoft.com/blog/2019/07/a-proactive-approach-to-more-secure-code/) fixed and assigned a CVE. While this is also true for Windows and macOS, they are quickly making progress on adopting memory-safe languages—such as Rust and Swift, respectively—while there is no similar effort to rewrite Linux in a memory-safe language like Rust.

## 挑選發行版本

所有 Linux 發行版並非一模一樣。 Our [Linux recommendation page](../desktop.md) is not meant to be an authoritative source on which distribution you should use, but our recommendations *are* aligned with the following guidelines. These are a few things you should keep in mind when choosing a distribution:

### 發布週期

強烈建議您選擇與穩定的上遊軟體版本保持接近的發行版，通常稱為滾動發行版。 因為凍結發行週期旳發行版通常不會更新套件版本，並且在安全性更新方面落後。

像 [Debian](https://www.debian.org/security/faq#handling)這樣的凍結發行版，套件維護人員預計會回移補丁修復漏洞，而不是將軟體提昇到上遊開發人員發布的“下一個版本”。 Some security fixes [do not](https://arxiv.org/abs/2105.14565) receive a [CVE ID](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures) (particularly less popular software) at all and therefore do not make it into the distribution with this patching model. 因此小型安全修復有時候要等到下次主要發佈時才一起進行。

我們不認為保留軟體套件和應用臨時補丁是好主意，因為它偏離了開發者計畫讓軟體工作的方式。 [Richard Brown](https://rootco.de/aboutme/) 對此有一份簡報：

<div class="yt-embed">
  <iframe width="560" height="315" src="https://invidious.privacyguides.net/embed/i8c0mg_mS7U?local=true" title="定期發佈是錯的，滾動發佈才可救命" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

### 傳統 vs 原子更新

傳統上 Linux 發行版的是依次更新所需的軟體套件。 如果更新時發生錯誤，傳統更新例如 Fedora, Arch Linux 或 Debian 等發行版所用的更新將變得不太可靠。

原子式更新的發行版要嘛全都更新要嘛完全沒更新 通常事務性更新系統也是原子式的。

事務性更新系統會在更新前後建立快照應用。 如果更新發生失敗(例如因電力故障問題)，就可以輕鬆地滾動回"近期已知的良好狀態"。

原子更新法用於 Silverblue、Tumbleweed 和 NixOS 這類不變的發行版通過此種模式實現可靠性。 [Adam Šamalík](https://twitter.com/adsamalik) 簡報了`rpm-ostree` 如何與 Silverblue 一起運作的情況:

<div class="yt-embed">
  <iframe width="560" height="315" src="https://invidious.privacyguides.net/embed/-hpV5l-gJnQ?local=true" title="試試 Fedora Silverblue — 一套不變的桌面 OS! - Adam Šamalik" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

### “以安全爲重點的發行版

人們常會混淆“以安全為中心”的發行版和“滲透測試”發行版。 A quick search for “the most secure Linux distribution” will often give results like Kali Linux, Black Arch, or Parrot OS. 這些發行版是攻擊性的滲透測試發行版，捆綁了測試其他系統的工具。 它們不包括任何 "額外的安全 "或常規使用的防禦性緩解措施。

### 基於 Arch Linux 的發行版

Arch and Arch-based distributions are not recommended for those new to Linux (regardless of distribution) as they require regular [system maintenance](https://wiki.archlinux.org/title/System_maintenance). Arch does not have a distribution update mechanism for the underlying software choices. 因此，必須了解當前趨勢，並在新技術取代舊有做法時予以採用。

對於一個安全的系統，還應有足夠的 Linux 知識來作正確安全設置，如採用 [強制性訪問控制](https://en.wikipedia.org/wiki/Mandatory_access_control) 系統，設置 [內核模塊](https://en.wikipedia.org/wiki/Loadable_kernel_module#Security) 黑名單，硬化啟動參數，操作 [sysctl](https://en.wikipedia.org/wiki/Sysctl) 參數，並知道需要哪些組件，如 [Polkit](https://en.wikipedia.org/wiki/Polkit)。

Anyone using the [Arch User Repository (AUR)](https://wiki.archlinux.org/title/Arch_User_Repository) **must** be comfortable auditing PKGBUILDs that they download from that service. AUR 軟體套件是社區製作的內容，未經任何審查，很容易受到軟體供應鏈的攻擊， [事實上已發生過這類事件](https://www.bleepingcomputer.com/news/security/malware-found-in-arch-linux-aur-package-repository/)。

The AUR should always be used sparingly, and often there is a lot of bad advice on various pages which direct people to blindly use [AUR helpers](https://wiki.archlinux.org/title/AUR_helpers) without sufficient warning. 類似的警告也適用基於Debian 發行版上使用第三方個人軟體套件檔案(PPAs)或 Fedora使用社區項目(COPR)。

If you are experienced with Linux and wish to use an Arch-based distribution, we generally recommend mainline Arch Linux over any of its derivatives.

Additionally, we recommend **against** these two Arch derivatives specifically:

- **Manjaro**: 此發行版將軟體套件保留 2週，以確保不會破壞他們自己的修改，而不是確保上游的穩定。 使用AUR軟體套件時，通常是根據 Arch 軟體庫中最新的 [存放庫構建](https://en.wikipedia.org/wiki/Library_(computing))。
- **Garuda**: 他們使用 [Chaotic-AUR](https://aur.chaotic.cx/) ，它自動地、盲目地從 AUR 編譯軟件套件。 沒有驗證程序去確保 AUR 套件不會受到供應鏈攻擊。

### Linux-libre 內核與 “Libre” 發行版

We recommend **against** using the Linux-libre kernel, since it [removes security mitigations](https://www.phoronix.com/news/GNU-Linux-Libre-5.7-Released) and [suppresses kernel warnings](https://news.ycombinator.com/item?id=29674846) about vulnerable microcode.

## 一般性建議

### 磁碟加密

大多數Linux 發行版安裝程序中都有啟用 [LUKS](../encryption.md#linux-unified-key-setup) FDE之選項。 如果在安裝時沒有設置這個選項，就只能重新安裝，因為在 [系統系統](https://en.wikipedia.org/wiki/File_system) 被格式化 [磁碟分區](https://en.wikipedia.org/wiki/Disk_partitioning)後進行加密。 我們還建議安全地刪除儲存設備。

- [安全資料清除 :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/05/25/secure-data-erasure/)

### Swap

Consider using [ZRAM](https://wiki.archlinux.org/title/Zram#Using_zram-generator) instead of a traditional swap file or partition to avoid writing potentially sensitive memory data to persistent storage (and improve performance). Fedora-based distributions [use ZRAM by default](https://fedoraproject.org/wiki/Changes/SwapOnZRAM).

If you require suspend-to-disk (hibernation) functionality, you will still need to use a traditional swap file or partition. Make sure that any swap space you do have on a persistent storage device is [encrypted](https://wiki.archlinux.org/title/Dm-crypt/Swap_encryption) at a minimum to mitigate some of these threats.

### Wayland

We recommend using a desktop environment that supports the [Wayland](https://en.wikipedia.org/wiki/Wayland_(display_server_protocol)) display protocol, as it was developed with security [in mind](https://lwn.net/Articles/589147/). Its predecessor ([X11](https://en.wikipedia.org/wiki/X_Window_System)) does not support GUI isolation, which allows any window to [record, log, and inject inputs in other windows](https://blog.invisiblethings.org/2011/04/23/linux-security-circus-on-gui-isolation.html), making any attempt at sandboxing futile. While there are options to do nested X11 such as [Xpra](https://en.wikipedia.org/wiki/Xpra) or [Xephyr](https://en.wikipedia.org/wiki/Xephyr), they often come with negative performance consequences, and are neither convenient to set up nor preferable over Wayland.

幸好常見的桌面環境，如 [GNOME](https://www.gnome.org)， [KDE](https://kde.org)以及視窗管理器 [Sway](https://swaywm.org) 都支持 Wayland。 某些發佈版本如 Fedora 和 Tumbleweed 預設使用它，有些則可能在未來也會這樣作在 X11 成為 [硬性維護模式](https://www.phoronix.com/news/X.Org-Maintenance-Mode-Quickly)後。 如果使用以下的桌面環境，就像在桌面顯示管理器中選擇 "Wayland "一樣簡單([GDM](https://en.wikipedia.org/wiki/GNOME_Display_Manager), [SDDM](https://en.wikipedia.org/wiki/Simple_Desktop_Display_Manager)) 。

我們**反對**使用不支援 Wayland 的桌面環境或視窗管理器，如Cinnamon（Linux Mint）、Pantheon（Elementary OS）、MATE、Xfce 和 i3。

### 商用靭體(Microcode更新)

Some Linux distributions (such as [Linux-libre](https://en.wikipedia.org/wiki/Linux-libre)-based or DIY distros) don’t come with the proprietary [microcode](https://en.wikipedia.org/wiki/Microcode) updates which patch critical security vulnerabilities. 這些漏洞例子包括： [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability)), [Meltdown](https://en.wikipedia.org/wiki/Meltdown_(security_vulnerability)), [SSB](https://en.wikipedia.org/wiki/Speculative_Store_Bypass), [Foreshadow](https://en.wikipedia.org/wiki/Foreshadow), [MDS](https://en.wikipedia.org/wiki/Microarchitectural_Data_Sampling), [SWAPGS](https://en.wikipedia.org/wiki/SWAPGS_(security_vulnerability)), 以及其他 [硬體漏洞](https://www.kernel.org/doc/html/latest/admin-guide/hw-vuln/index.html)。

We **highly recommend** that you install microcode updates, as they contain important security patches for the CPU which can not be fully mitigated in software alone. Fedora 和 openSUSE 都預設採用微碼更新。

### 更新

大多數 Linux 發行版會自動安裝更新或發出提醒。 重要的是保持作業系統系統最新，當發現漏洞時，可修補軟體。

Some distributions (particularly those aimed at advanced users) are more bare bones and expect you to do things yourself (e.g. Arch or Debian). 例如需要手動運行 "軟體套件管理器" (`apt`, `pacman`, `dnf`等等)，以便接收重要的安全更新。

此外，一些發行版不會自動下載靭體更新。 为此，你将需要安装 [`fwupd`](https://wiki.archlinux.org/title/Fwupd)。

## 隱私微調

### MAC 地址隨機化

Many desktop Linux distributions (Fedora, openSUSE, etc.) come with [NetworkManager](https://en.wikipedia.org/wiki/NetworkManager) to configure Ethernet and Wi-Fi settings.

在使用NetworkManager時，可以隨機化 [](https://fedoramagazine.org/randomize-mac-address-nm/) [MAC 地址](https://en.wikipedia.org/wiki/MAC_address)。 這在Wi-Fi 上提供了更多隱私，因為這讓追踪所連網路的特定設備變得更困難。 但這 [**並不是**](https://papers.mathyvanhoef.com/wisec2016.pdf) 讓您匿名。

將設置改為 **隨機** ，而不是 **穩定**，正如 [這篇文章建議](https://fedoramagazine.org/randomize-mac-address-nm/)。

如使用 [systemd-networkd](https://en.wikipedia.org/wiki/Systemd#Ancillary_components)，需要設置 [`MACAddressPolicy=random`](https://www.freedesktop.org/software/systemd/man/systemd.link.html#MACAddressPolicy=) ，以啟用 [RFC 7844 (Anonymity Profiles for DHCP Clients)](https://www.freedesktop.org/software/systemd/man/systemd.network.html#Anonymize=)。

MAC address randomization is primarily beneficial for Wi-Fi connections. For Ethernet connections, randomizing your MAC address provides little (if any) benefit, because a network administrator can trivially identify your device by other means (such as inspecting the port you are connected to on the network switch). 隨機化 Wi-Fi MAC 地址必須有 Wi-Fi 靭體支持。

### 其他標識符

還有一些其他的系統標識符，可能要小心對待。 您應該考慮看看是否適用於您的 [威脅模型](../basics/threat-modeling.md)。

- **主機名稱 **，系統的主機名稱會分享到所連接的網路。 應避免主機名稱像你的名字或作業系統等具識別度的術語，最好用一般術語或隨機字符串。
- **用戶名稱 ** 。同樣地，用戶名稱會在系統中以各種方式使用。 考慮用 "用戶 "這樣一般常見字，而不是您的真實姓名。
- **機器 ID：**：在安裝過程中，會生成一個獨特的機器ID 並存儲在您的設備上。 考慮 [將它設置為一個通用 ID](https://madaidans-insecurities.github.io/guides/linux-hardening.html#machine-id)。

### 系統計數

Fedora 專案使用[`countme`](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting#Detailed_Description) 變量而非獨特 ID 來[計算多少](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting)系統訪問它的鏡像。 Fedora 這樣做是為了確定負載並在必要時為更新提供更好的伺服器。

這個 [選項](https://dnf.readthedocs.io/en/latest/conf_ref.html#options-for-both-main-and-repo) ，目前預設為關閉。 我們建議將 `countme=false` 添加到 `/etc/dnf/dnf.conf` ，以備將來啟用。 使用 `rpm-ostree` 的系統，如 Silverblue，通過遮蔽 [rpm-ostree-countme](https://fedoramagazine.org/getting-better-at-counting-rpm-ostree-based-systems/) 計時器來禁用 countme 選項。

openSUSE 還使用[唯一的 ID](https://en.opensuse.org/openSUSE:Statistics) 來計算系統，可以通過刪除 `/var/lib/zypp/AnonymousUniqueId` 檔來禁用它。
