---
title: Linux Overview
icon: simple/linux
description: Linux is an open-source, privacy-focused desktop operating system alternative, but not all distribitions are created equal.
---

**Linux** 是開源、注重隱私的桌面作業系統替代方案。 面對主流作業系統中普遍存在的遙測和其他侵犯隱私的技術，Linux 桌面仍是那些希望能完全控制電腦的用戶明智選擇。

我們網站通常使用術語 "Linux "來講述桌面Linux 發行版。 其它也使用Linux內核的作業系統，如 ChromeOS、Android 和Qubes OS，此處不作討論。

[建議的 Linux 發行版 :material-arrow-right-drop-circle:](../desktop.md ""){.md-button}

## 隱私筆記

用戶應考量 一些使用 Linux 須關注的隱私問題。 儘管有這些缺點，對於大多數用戶，桌面 Linux 發行版還是很棒：

- 避免商業作業系統經常出現的遙測現象
- 維護 [軟體自由](https://gnu.org/philosophy/free-sw.en.html#four-freedoms)
- 使用專注隱私的系統如: [Whonix](../desktop.md#whonix) 或 [Tails](../desktop.md#tails)

### 開源安全

It is a [common misconception](../basics/common-misconceptions.md#open-source-software-is-always-secure-or-proprietary-software-is-more-secure) that Linux and other open-source software are inherently secure simply because the source code is available. 人們期望定期進行社群驗證；然而這種情況 [並不常見](https://seirdy.one/posts/2022/02/02/floss-security)。

現實中，發行版安全取決於許多因素，例如專案活動、開發人員經驗、用於代碼審查的嚴格程度以及代碼庫 特定部分的關注頻率，這些可能多年未被聞問。

### 遺失的安全功能

目前，在某些安全功能方面，桌面 Linux [落後於 macOS 或 Android ](https://discussion.fedoraproject.org/t/fedora-strategy-2028-proposal-fedora-linux-is-as-secure-as-macos/46899/9)。 希望未來能看到這些領域的改進。

- Linux 的**驗證開機** 不如 Apple 的 [Secure Boot 安全開機](https://support.apple.com/guide/security/secac71d5623/web) 或 Android’s [Verified Boot 驗證開機](https://source.android.com/security/verifiedboot)。 驗證開機可防止惡意軟體的持久篡改和 [evil maid attacks 邪惡女傭攻擊](https://en.wikipedia.org/wiki/Evil_Maid_attack)，但其[仍未及於大多數進階的發行版本](https://discussion.fedoraproject.org/t/has-silverblue-achieved-verified-boot/27251/3)。

- Linux 上的應用程式嚴重缺乏**強大的沙盒**，即使便使用 Flatpaks 等容器化應用程式或 Firejail 等沙盒解決方案還是不足。 Flatpak is the most promising sandboxing utility for Linux thus far, but is still deficient in many areas and allows for [unsafe defaults](https://flatkill.org/2020) which permit most apps to trivially bypass their sandbox.

此外，Linux 在實施[漏洞緩解措施](https://madaidans-insecurities.github.io/linux.html#exploit-mitigations)方面落後，這些緩解措施現已成為其他操作系統的標準配置，例如 Windows 上的任意代碼防護或 macOS 上的強化運行時間。 此外，大多數 Linux 程序和 Linux 本身都是用記憶體不安全語言編寫的。 記憶體損壞錯誤是造成[大多數漏洞](https://msrc.microsoft.com/blog/2019/07/a-proactive-approach-to-more-secure-code)的原因已修復並分配了CVE。 雖然 Windows 和 macOS 也是如此，但它們在使用記憶體安全語言（例如 Rust 和 Swift）上正在迅速進展，而Linux 方面則沒有這類以 Rust 重寫記憶體安全的投入 。

## 挑選發行版本

所有 Linux 發行版並非一模一樣。 我們的 [Linux 推薦頁面](../desktop.md)並不是您使用哪個發行版的權威來源，但我們的*建議*與以下準則一致。 選擇發行版時應記住以下幾點：

### 發布週期

強烈建議您選擇與穩定的上遊軟體版本保持接近的發行版，通常稱為滾動發行版。 因為凍結發行週期旳發行版通常不會更新套件版本，並且在安全性更新方面落後。

像 [Debian](https://debian.org/security/faq#handling)這樣的凍結發行版，套件維護人員預計會回移補丁修復漏洞，而不是將軟體提昇到上遊開發人員發布的“下一個版本”。 Some security fixes (particularly for less popular software) [do not](https://arxiv.org/abs/2105.14565) receive a [CVE ID](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures) at all and therefore do not make it into the distribution with this patching model. 因此小型安全修復有時候要等到下次主要發佈時才一起進行。

我們不認為保留軟體套件和應用臨時補丁是好主意，因為它偏離了開發者計畫讓軟體工作的方式。 [Richard Brown](https://rootco.de/aboutme) 對此有一份簡報：

- [Regular Releases are Wrong, Roll for your life](https://youtu.be/i8c0mg_mS7U) <small>(YouTube)</small>

### Traditional vs Atomic Updates

傳統上 Linux 發行版的是依次更新所需的軟體套件。 Traditional updates such as those used in Fedora, Arch Linux, and Debian-based distributions can be less reliable if an error occurs while updating.

Atomic updating distributions, on the other hand, apply updates in full or not at all. On an atomic distribution, if an error occurs while updating (perhaps due to a power failure), nothing is changed on the system.

The atomic update method can achieve reliability with this model and is used for [distributions](../desktop.md#atomic-distributions) like Silverblue and NixOS. [Adam Šamalík](https://twitter.com/adsamalik) provides a presentation on how `rpm-ostree` works with Silverblue:

- [Let's try Fedora Silverblue — an immutable desktop OS! - Adam Šamalik](https://youtu.be/aMo4ZlWznao) <small>(YouTube)</small>

### “以安全爲重點的發行版

人們常會混淆“以安全為中心”的發行版和“滲透測試”發行版。 快速搜索“最安全的 Linux發行版”，通常會得到像 Kali Linux, Black Arch 或 Parrot OS 這樣結果。 這些發行版是攻擊性的滲透測試發行版，捆綁了測試其他系統的工具。 它們不包括任何 "額外的安全 "或常規使用的防禦性緩解措施。

### 基於 Arch Linux 的發行版

不推薦 Arch 或其相關發行版(無論哪個發行版)給剛接觸 Linux 的人，因為它們需要定期進行 [系統維護](https://wiki.archlinux.org/title/System_maintenance)。 Arch沒有底層軟體選擇的發行版更新機制。 As a result you have to stay aware with current trends and adopt technologies on your own as they supersede older practices.

For a secure system, you are also expected to have sufficient Linux knowledge to properly set up security for their system such as adopting a [mandatory access control](#mandatory-access-control) system, setting up [kernel module](https://en.wikipedia.org/wiki/Loadable_kernel_module#Security) blacklists, hardening boot parameters, manipulating [sysctl](https://en.wikipedia.org/wiki/Sysctl) parameters, and knowing what components they need such as [Polkit](https://en.wikipedia.org/wiki/Polkit).

使用 [Arch User Repository (AUR)](https://wiki.archlinux.org/title/Arch_User_Repository), **者必須** 對該服務下載的 PKGBUILD進行審計。 AUR packages are community-produced content and are not vetted in any way, and therefore are vulnerable to software [:material-package-variant-closed-remove: Supply Chain Attacks](../basics/common-threats.md#attacks-against-certain-organizations ""){.pg-viridian}, which has in fact happened [in the past](https://bleepingcomputer.com/news/security/malware-found-in-arch-linux-aur-package-repository).

應該少用 AUR，而往往各種網頁有很多不好的建議，指導人們盲目地使用 [AUR 幫助器](https://wiki.archlinux.org/title/AUR_helpers) 卻沒有足夠警告。 Similar warnings apply to the use of third-party Personal Package Archives (PPAs) on Debian-based distributions or Community Projects (COPR) on Fedora.

如果是 Linux 老手，希望使用基於 Arch 發行版，我們只推薦主線 Arch Linux，而不是任何衍生品。

此外，我們特別**反推薦**這兩個 Arch 衍生品：

- **Manjaro**: 此發行版將軟體套件保留 2週，以確保不會破壞他們自己的修改，而不是確保上游的穩定。 使用AUR軟體套件時，通常是根據 Arch 軟體庫中最新的 [存放庫構建](https://en.wikipedia.org/wiki/Library_(computing))。
- **Garuda**: 他們使用 [Chaotic-AUR](https://aur.chaotic.cx) ，會自動地從 AUR 編譯軟件套件。 沒有驗證程序去確保 AUR 套件不會受到供應鏈攻擊。

### Linux-libre 內核與 “Libre” 發行版

我們建議**不**使用 Linux-libre 內核，因為它[刪除安全緩解措施](https://phoronix.com/news/GNU-Linux-Libre-5.7-Released)並[抑制有關易受攻擊的微代碼的內核警告](https://news.ycombinator.com/item?id=29674846)。

### Mandatory access control

Mandatory access control is a set of additional security controls which help to confine parts of the system such as apps and system services. The two common forms of mandatory access control found in Linux distributions are [SELinux](https://github.com/SELinuxProject) and [AppArmor](https://apparmor.net). While Fedora uses SELinux by default, Tumbleweed [defaults](https://en.opensuse.org/Portal:SELinux) to AppArmor in the installer, with an option to [choose](https://en.opensuse.org/Portal:SELinux/Setup) SELinux instead.

SELinux on [Fedora](https://docs.fedoraproject.org/en-US/quick-docs/selinux-getting-started) confines Linux containers, virtual machines, and service daemons by default. AppArmor is used by the snap daemon for [sandboxing](https://snapcraft.io/docs/security-sandboxing) snaps which have [strict](https://snapcraft.io/docs/snap-confinement) confinement such as [Firefox](https://snapcraft.io/firefox). There is a community effort to confine more parts of the system in Fedora with the [ConfinedUsers](https://fedoraproject.org/wiki/SIGs/ConfinedUsers) special interest group.

## 一般性建議

### 磁碟加密

大多數Linux 發行版安裝程序中都有啟用 [LUKS](../encryption.md#linux-unified-key-setup) FDE之選項。 如果在安裝時沒有設置這個選項，就只能重新安裝，因為在 [系統系統](https://en.wikipedia.org/wiki/File_system) 被格式化 [磁碟分區](https://en.wikipedia.org/wiki/Disk_partitioning)後進行加密。 我們還建議安全地刪除儲存設備。

- [安全資料清除 :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/05/25/secure-data-erasure)

### Swap

考慮使用 [ZRAM](https://wiki.archlinux.org/title/Zram#Using_zram-generator) 而不是傳統的 swap 檔案或分區，以避免將潛在敏感的記憶資料寫入持久存儲（並提高性能）。 基於 Fedora 的發行版 [預設使用 ZRAM](https://fedoraproject.org/wiki/Changes/SwapOnZRAM)。

如果需要 suspend-to-disk （磁盤休眠）功能，則仍然需要使用傳統的swap 檔案或分區。 確保持久存儲設備上的任何交換空間予以[加密](https://wiki.archlinux.org/title/Dm-crypt/Swap_encryption)，以減輕一些威脅。

### 商用靭體(Microcode更新)

Linux 發行版，如 [Linux-libre](https://en.wikipedia.org/wiki/Linux-libre) 或 DIY(Arch Linux)，不附帶商業專用的 [微碼](https://en.wikipedia.org/wiki/Microcode) 更新，這類更新通常會修補漏洞。 這些漏洞的一些著名例子如: [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability))、[ Meltdown ](https://en.wikipedia.org /wiki/Meltdown_(security_vulnerability))、[SSB](https://en.wikipedia.org/wiki/Speculative_Store_Bypass)、[Foreshadow](https:/ / en.wikipedia.org/wiki/Foreshadow)、[MDS](https://en.wikipedia.org/wiki/Microarchitectural_Data_Sampling)、[SWAPGS](https: //en.wikipedia.org/wiki/SWAPGS_(security_vulnerability))，以及其他[硬體漏洞](https://kernel.org/doc/html/latest/admin-guide/hw- vuln /index.html)。

我們**強烈建議**安裝微碼更新，因為它們包含重要的 CPU 安全補丁，無法僅僅靠軟體緩解。 Fedora and openSUSE both apply microcode updates by default.

### 更新

大多數 Linux 發行版會自動安裝更新或發出提醒。 重要的是保持作業系統系統最新，當發現漏洞時，可修補軟體。

一些發行版（尤其是那些針對進階用戶）更加簡陋，指望使用者自己能做一些事情（例如 Arch 或 Debian） 例如需要手動運行 "軟體套件管理器" (`apt`, `pacman`, `dnf`等等)，以便接收重要的安全更新。

此外，一些發行版不會自動下載靭體更新。 為此需要安裝l [`fwupd`](https://wiki.archlinux.org/title/Fwupd)。

### Permission Controls

Desktop environments (DEs) that support the [Wayland](https://wayland.freedesktop.org) display protocol are [more secure](https://lwn.net/Articles/589147) than those that only support X11. However, not all DEs take full advantage of Wayland's architectural security improvements.

For example, GNOME has a notable edge in security compared to other DEs by implementing permission controls for third-party software that tries to [capture your screen](https://gitlab.gnome.org/GNOME/gnome-shell/-/issues/3943). That is, when a third-party application attempts to capture your screen, you are prompted for your permission to share your screen with the app.

<figure markdown>
  ![Screenshot permissions](../assets/img/linux/screenshot_permission.png){ width="450" }
  <figcaption>GNOME's screenshot permission dialog</figcaption>
</figure>

Many alternatives don't provide these same permission controls yet,[^1] while some are waiting for Wayland to implement these controls upstream.[^2]

## 隱私微調

### MAC 地址隨機化

許多桌面 Linux 發行版（Fedora、openSUSE等）自帶 [網路管理員](https://en.wikipedia.org/wiki/NetworkManager)，以配置以太網和 Wi-Fi設置。

可[隨機化](https://fedoramagazine.org/randomize-mac-address-nm)<a href="https://en.wikipedia.org/wiki/MAC_address 使用NetworkManager 時的“MAC 位址”。 這在Wi-Fi 上提供了更多隱私，因為這讓追踪所連網路的特定設備變得更困難。 但這 [**並不是**](https://papers.mathyvanhoef.com/wisec2016.pdf) 讓您匿名。

建議將設定更改為**隨機**，而不是**穩定**，如[這篇文章的說明](https: // fedoramagazine.org/randomize-mac-address-nm)。

如果使用 [systemd-networkd](https://en.wikipedia.org/wiki/Systemd#Ancillary_components)，則需要設定 [`MACAddressPolicy=random`](https://freedesktop. org/software /systemd/man/systemd.link.html#MACAddressPolicy=) 這將啟用[RFC 7844（DHCP 用戶端的匿名設定檔）](https://freedesktop.org/software/ systemd/man /systemd.network.html#Anonymize=)。

MAC 地址隨機化主要有利於 Wi-Fi 連接。 對以太網連接，隨機化 MAC 地址幾乎沒什麼好處（如果有的話），因為網絡管理員可以通過其他方式輕鬆識別您的設備（例如檢查您在網絡交換機上連接的端口）。 隨機化 Wi-Fi MAC 地址必須有 Wi-Fi 靭體支持。

### 其他標識符

還有一些其他的系統標識符，可能要小心對待。 您應該考慮看看是否適用於您的 [威脅模型](../basics/threat-modeling.md)。

- **主機名稱 **，系統的主機名稱會分享到所連接的網路。 應避免主機名稱像你的名字或作業系統等具識別度的術語，最好用一般術語或隨機字符串。
- **用戶名稱 ** 。同樣地，用戶名稱會在系統中以各種方式使用。 考慮用 "用戶 "這樣一般常見字，而不是您的真實姓名。
- **機器 ID**：在安裝過程中，會生成一個獨特的機器ID 並存儲在您的設備上。 考慮 [將它設置為一個通用 ID](https://madaidans-insecurities.github.io/guides/linux-hardening.html#machine-id)。

### 系統計數

Fedora 專案使用[`countme`](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting#Detailed_Description) 變量而非獨特 ID 來[計算多少](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting)系統訪問它的鏡像。 Fedora 這樣做是為了確定負載並在必要時為更新提供更好的伺服器。

這個 [選項](https://dnf.readthedocs.io/en/latest/conf_ref.html#options-for-both-main-and-repo) ，目前預設為關閉。 我們建議將 `countme=false` 添加到 `/etc/dnf/dnf.conf` ，以備將來啟用。 使用 `rpm-ostree` 的系統，如 Silverblue，通過遮蔽 [rpm-ostree-countme](https://fedoramagazine.org/getting-better-at-counting-rpm-ostree-based-systems) 計時器來禁用 countme 選項。

openSUSE 還使用[唯一的 ID](https://en.opensuse.org/openSUSE:Statistics) 來計算系統，可以通過清空`/var/lib/zypp/AnonymousUniqueId` 此檔案來禁用。

[^1]: KDE currently has an open proposal to add controls for screen captures: <https://invent.kde.org/plasma/xdg-desktop-portal-kde/-/issues/7>
[^2]: Sway is waiting to add specific security controls until they "know how security as a whole is going to play out" in Wayland: <https://github.com/swaywm/sway/issues/5118#issuecomment-600054496>
