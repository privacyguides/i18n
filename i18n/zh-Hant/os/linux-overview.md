---
title: Linux 概述
icon: simple/linux
description: Linux 為開源、以隱私為中心的桌面作業系統替代選項，但並非所有發行版都一模一樣。
---

**Linux** 是開源、注重隱私的桌面作業系統替代方案。 面對主流作業系統中普遍存在的遙測和其他侵犯隱私的技術，Linux 桌面仍是那些用戶希望能完全控制電腦的明智選擇。

我們網站通常使用術語 "Linux "來講述桌面Linux 發行版。 其它也使用Linux內核的作業系統，如 ChromeOS、Android 和Qubes OS，此處不作討論。

[建議的 Linux 發行版 :material-arrow-right-drop-circle:](../desktop.md ""){.md-button}

## 隱私筆記

用戶應考量 一些使用 Linux 須關注的隱私問題。 儘管有這些缺點，對於大多數用戶，桌面 Linux 發行版還是很棒：

- 避免商業作業系統經常出現的遙測現象
- Maintain [software freedom](https://gnu.org/philosophy/free-sw.en.html#four-freedoms)
- Use privacy focused systems such as [Whonix](https://whonix.org) or [Tails](https://tails.net)

### 開源安全

人們往往[迷思](../basics/common-misconceptions.md#open-source-software-is-always-secure-or-proprietary-software-is-more-secure)認為 Linux 與其它開源軟體本較安全，因為源代碼可以公開取得。 There is an expectation that community verification occurs regularly, but this isn’t always [the case](https://seirdy.one/posts/2022/02/02/floss-security).

現實中，發行版安全取決於許多因素，例如專案活動、開發人員經驗、用於代碼審查的嚴格程度以及代碼庫 特定部分的關注頻率，這些可能多年未被聞問。

### 遺失的安全功能

目前，在某些安全功能方面，桌面 Linux [落後於 macOS 或 Android ](https://discussion.fedoraproject.org/t/fedora-strategy-2028-proposal-fedora-linux-is-as-secure-as-macos/46899/9)。 希望未來能看到這些領域的改進。

- Linux 的**驗證開機** 不如 Apple 的 [Secure Boot 安全開機](https://support.apple.com/guide/security/secac71d5623/web) 或 Android’s [Verified Boot 驗證開機](https://source.android.com/security/verifiedboot)。 驗證開機可防止惡意軟體的持久篡改和 [evil maid attacks 邪惡女傭攻擊](https://en.wikipedia.org/wiki/Evil_Maid_attack)，但其[仍未及於大多數進階的發行版本](https://discussion.fedoraproject.org/t/has-silverblue-achieved-verified-boot/27251/3)。

- Linux 上的應用程式嚴重缺乏**強大的沙盒**，即使便使用 Flatpaks 等容器化應用程式或 Firejail 等沙盒解決方案還是不足。 Flatpak is the most promising sandboxing utility for Linux thus far, but is still deficient in many areas and allows for [unsafe defaults](https://flatkill.org/2020) which allow most apps to trivially bypass their sandbox.

此外，Linux 在實施[漏洞緩解措施](https://madaidans-insecurities.github.io/linux.html#exploit-mitigations)方面落後，這些緩解措施現已成為其他操作系統的標準配置，例如 Windows 上的任意代碼防護或 macOS 上的強化運行時間。 此外，大多數 Linux 程序和 Linux 本身都是用記憶體不安全語言編寫的。 Memory corruption bugs are responsible for the [majority of vulnerabilities](https://msrc.microsoft.com/blog/2019/07/a-proactive-approach-to-more-secure-code) fixed and assigned a CVE. 雖然 Windows 和 macOS 也是如此，但它們在使用記憶體安全語言（例如 Rust 和 Swift）上正在迅速進展，而Linux 方面則沒有這類以 Rust 重寫記憶體安全的投入 。

## 挑選發行版本

所有 Linux 發行版並非一模一樣。 我們的 [Linux 推薦頁面](../desktop.md)並不是您使用哪個發行版的權威來源，但我們的*建議*與以下準則一致。 選擇發行版時應記住以下幾點：

### 發布週期

強烈建議您選擇與穩定的上遊軟體版本保持接近的發行版，通常稱為滾動發行版。 因為凍結發行週期旳發行版通常不會更新套件版本，並且在安全性更新方面落後。

For frozen distributions such as [Debian](https://debian.org/security/faq#handling), package maintainers are expected to backport patches to fix vulnerabilities rather than bump the software to the “next version” released by the upstream developer. 某些安全修復

根本没收到 [CVE ID](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures) （特别是不流行的軟體），在此種補丁模式不會放入發行版。 因此小型安全修復有時候要等到下次主要發佈時才一起進行。</p> 

我們不認為保留軟體套件和應用臨時補丁是好主意，因為它偏離了開發者計畫讓軟體工作的方式。 [Richard Brown](https://rootco.de/aboutme) has a presentation about this:

<div class="yt-embed">
  <iframe width="560" height="315" src="https://invidious.privacyguides.net/embed/i8c0mg_mS7U?local=true" title="定期發佈是錯的，滾動發佈才可救命" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

### 傳統 vs 原子更新

傳統上 Linux 發行版的是依次更新所需的軟體套件。 如果更新時發生錯誤，傳統更新例如 Fedora, Arch Linux 或 Debian 等發行版所用的更新將變得不太可靠。

原子式更新的發行版要嘛全都更新要嘛完全沒更新 通常事務性更新系統也是原子式的。

事務性更新系統會在更新前後建立快照應用。 如果更新發生失敗(例如因電力故障問題)，就可以輕鬆地滾動回"近期已知的良好狀態"。

原子更新法用於 Silverblue、Tumbleweed 和 NixOS 這類[發行版](../desktop.md#atomic-distributions)通過此種模式實現可靠性。 [Adam Šamalík](https://twitter.com/adsamalik) 簡報了`rpm-ostree` 如何與 Silverblue 一起運作的情況:

<div class="yt-embed">
  <iframe width="560" height="315" src="https://invidious.privacyguides.net/embed/-hpV5l-gJnQ?local=true" title="試試 Fedora Silverblue — 一套不變的桌面 OS! - Adam Šamalik" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

### “以安全爲重點的發行版

人們常會混淆“以安全為中心”的發行版和“滲透測試”發行版。 快速搜索“最安全的 Linux發行版”，通常會得到像 Kali Linux, Black Arch 或 Parrot OS 這樣結果。 這些發行版是攻擊性的滲透測試發行版，捆綁了測試其他系統的工具。 它們不包括任何 "額外的安全 "或常規使用的防禦性緩解措施。



### 基於 Arch Linux 的發行版

不推薦 Arch 或其相關發行版(無論哪個發行版)給剛接觸 Linux 的人，因為它們需要定期進行 [系統維護](https://wiki.archlinux.org/title/System_maintenance)。 Arch沒有底層軟體選擇的發行版更新機制。 因此，必須了解當前趨勢，並在新技術取代舊有做法時予以採用。

對於一個安全的系統，還應有足夠的 Linux 知識來作正確安全設置，如採用 [強制性訪問控制](https://en.wikipedia.org/wiki/Mandatory_access_control) 系統，設置 [內核模塊](https://en.wikipedia.org/wiki/Loadable_kernel_module#Security) 黑名單，硬化啟動參數，操作 [sysctl](https://en.wikipedia.org/wiki/Sysctl) 參數，並知道需要哪些組件，如 [Polkit](https://en.wikipedia.org/wiki/Polkit)。

使用 [Arch User Repository (AUR)](https://wiki.archlinux.org/title/Arch_User_Repository), **者必須** 對該服務下載的 PKGBUILD進行審計。 AUR packages are community-produced content and are not vetted in any way, and therefore are vulnerable to software supply chain attacks, which has in fact happened [in the past](https://bleepingcomputer.com/news/security/malware-found-in-arch-linux-aur-package-repository).

應該少用 AUR，而往往各種網頁有很多不好的建議，指導人們盲目地使用 [AUR 幫助器](https://wiki.archlinux.org/title/AUR_helpers) 卻沒有足夠警告。 類似的警告也適用基於Debian 發行版上使用第三方個人軟體套件檔案(PPAs)或 Fedora使用社區項目(COPR)。

如果是 Linux 老手，希望使用基於 Arch 發行版，我們只推薦主線 Arch Linux，而不是任何衍生品。

此外，我們特別**反推薦**這兩個 Arch 衍生品：

- **Manjaro**: 此發行版將軟體套件保留 2週，以確保不會破壞他們自己的修改，而不是確保上游的穩定。 使用AUR軟體套件時，通常是根據 Arch 軟體庫中最新的 [存放庫構建](https://en.wikipedia.org/wiki/Library_(computing))。
- **Garuda**: They use [Chaotic-AUR](https://aur.chaotic.cx) which automatically and blindly compiles packages from the AUR. 沒有驗證程序去確保 AUR 套件不會受到供應鏈攻擊。



### Linux-libre 內核與 “Libre” 發行版

We recommend **against** using the Linux-libre kernel, since it [removes security mitigations](https://phoronix.com/news/GNU-Linux-Libre-5.7-Released) and [suppresses kernel warnings](https://news.ycombinator.com/item?id=29674846) about vulnerable microcode.



## 一般性建議



### 磁碟加密

大多數Linux 發行版安裝程序中都有啟用 [LUKS](../encryption.md#linux-unified-key-setup) FDE之選項。 如果在安裝時沒有設置這個選項，就只能重新安裝，因為在 [系統系統](https://en.wikipedia.org/wiki/File_system) 被格式化 [磁碟分區](https://en.wikipedia.org/wiki/Disk_partitioning)後進行加密。 我們還建議安全地刪除儲存設備。

- [安全資料清除 :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/05/25/secure-data-erasure)



### Swap

考慮使用 [ZRAM](https://wiki.archlinux.org/title/Zram#Using_zram-generator) 而不是傳統的 swap 檔案或分區，以避免將潛在敏感的記憶資料寫入持久存儲（並提高性能）。 基於 Fedora 的發行版 [預設使用 ZRAM](https://fedoraproject.org/wiki/Changes/SwapOnZRAM)。

如果需要 suspend-to-disk （磁盤休眠）功能，則仍然需要使用傳統的swap 檔案或分區。 確保持久存儲設備上的任何交換空間予以[加密](https://wiki.archlinux.org/title/Dm-crypt/Swap_encryption)，以減輕一些威脅。



### Wayland

We recommend using a desktop environment that supports the [Wayland](https://en.wikipedia.org/wiki/Wayland_(display_server_protocol)) display protocol, as it was developed with security [in mind](https://lwn.net/Articles/589147). 其前身( [X11](https://en.wikipedia.org/wiki/X_Window_System))，不支持GUI 隔離，允許所有視窗[記錄畫面、日誌和注入其他視窗的輸入](https://blog.invisiblethings.org/2011/04/23/linux-security-circus-on-gui-isolation.html)，使任何沙盒嘗試都是徒勞。 雖然有一些選項可以做嵌套 X11，比如 [Xpra](https://en.wikipedia.org/wiki/Xpra) 或 [Xephyr](https://en.wikipedia.org/wiki/Xephyr)，但它們往往會帶來負面性能，設置也不方便，不如 Wayland 可取。

Fortunately, [wayland compositors](https://en.wikipedia.org/wiki/Wayland_(protocol)#Wayland_compositors) such as those included with [GNOME](https://gnome.org) and [KDE Plasma](https://kde.org) now have good support for Wayland along with some other compositors that use [wlroots](https://gitlab.freedesktop.org/wlroots/wlroots/-/wikis/Projects-which-use-wlroots), (e.g. [Sway](https://swaywm.org)). Some distributions like Fedora and Tumbleweed use it by default, and some others may do so in the future as X11 is in [hard maintenance mode](https://phoronix.com/news/X.Org-Maintenance-Mode-Quickly). 如果使用以下的桌面環境，就像在桌面顯示管理器中選擇 "Wayland "一樣簡單([GDM](https://en.wikipedia.org/wiki/GNOME_Display_Manager), [SDDM](https://en.wikipedia.org/wiki/Simple_Desktop_Display_Manager)) 。

我們**反對**使用不支援 Wayland 的桌面環境或視窗管理器，如Cinnamon（Linux Mint）、Pantheon（Elementary OS）、MATE、Xfce 和 i3。



### 商用靭體(Microcode更新)

Linux 發行版，如 [Linux-libre](https://en.wikipedia.org/wiki/Linux-libre) 或 DIY(Arch Linux)，不附帶商業專用的 [微碼](https://en.wikipedia.org/wiki/Microcode) 更新，這類更新通常會修補漏洞。 Some notable examples of these vulnerabilities include [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability)), [Meltdown](https://en.wikipedia.org/wiki/Meltdown_(security_vulnerability)), [SSB](https://en.wikipedia.org/wiki/Speculative_Store_Bypass), [Foreshadow](https://en.wikipedia.org/wiki/Foreshadow), [MDS](https://en.wikipedia.org/wiki/Microarchitectural_Data_Sampling), [SWAPGS](https://en.wikipedia.org/wiki/SWAPGS_(security_vulnerability)), and other [hardware vulnerabilities](https://kernel.org/doc/html/latest/admin-guide/hw-vuln/index.html).

我們**強烈建議**安裝微碼更新，因為它們包含重要的 CPU 安全補丁，無法僅僅靠軟體緩解。 Fedora 和 openSUSE 都預設採用微碼更新。



### 更新

大多數 Linux 發行版會自動安裝更新或發出提醒。 重要的是保持作業系統系統最新，當發現漏洞時，可修補軟體。

一些發行版（尤其是那些針對進階用戶）更加簡陋，指望使用者自己能做一些事情（例如 Arch 或 Debian） 例如需要手動運行 "軟體套件管理器" (`apt`, `pacman`, `dnf`等等)，以便接收重要的安全更新。

此外，一些發行版不會自動下載靭體更新。 为此，你将需要安装 [`fwupd`](https://wiki.archlinux.org/title/Fwupd)。



## 隱私微調



### MAC 地址隨機化

許多桌面 Linux 發行版（Fedora、openSUSE等）自帶 [網路管理員](https://en.wikipedia.org/wiki/NetworkManager)，以配置以太網和 Wi-Fi設置。

It is possible to [randomize](https://fedoramagazine.org/randomize-mac-address-nm) the [MAC address](https://en.wikipedia.org/wiki/MAC_address) when using NetworkManager. 這在Wi-Fi 上提供了更多隱私，因為這讓追踪所連網路的特定設備變得更困難。 但這 [**並不是**](https://papers.mathyvanhoef.com/wisec2016.pdf) 讓您匿名。

We recommend changing the setting to **random** instead of **stable**, as suggested in the [article](https://fedoramagazine.org/randomize-mac-address-nm).

If you are using [systemd-networkd](https://en.wikipedia.org/wiki/Systemd#Ancillary_components), you will need to set [`MACAddressPolicy=random`](https://freedesktop.org/software/systemd/man/systemd.link.html#MACAddressPolicy=) which will enable [RFC 7844 (Anonymity Profiles for DHCP Clients)](https://freedesktop.org/software/systemd/man/systemd.network.html#Anonymize=).

MAC 地址隨機化主要有利於 Wi-Fi 連接。 對以太網連接，隨機化 MAC 地址幾乎沒什麼好處（如果有的話），因為網絡管理員可以通過其他方式輕鬆識別您的設備（例如檢查您在網絡交換機上連接的端口）。 隨機化 Wi-Fi MAC 地址必須有 Wi-Fi 靭體支持。



### 其他標識符

還有一些其他的系統標識符，可能要小心對待。 您應該考慮看看是否適用於您的 [威脅模型](../basics/threat-modeling.md)。

- **主機名稱 **，系統的主機名稱會分享到所連接的網路。 應避免主機名稱像你的名字或作業系統等具識別度的術語，最好用一般術語或隨機字符串。
- **用戶名稱 ** 。同樣地，用戶名稱會在系統中以各種方式使用。 考慮用 "用戶 "這樣一般常見字，而不是您的真實姓名。
- **機器 ID：**：在安裝過程中，會生成一個獨特的機器ID 並存儲在您的設備上。 考慮 [將它設置為一個通用 ID](https://madaidans-insecurities.github.io/guides/linux-hardening.html#machine-id)。



### 系統計數

Fedora 專案使用[`countme`](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting#Detailed_Description) 變量而非獨特 ID 來[計算多少](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting)系統訪問它的鏡像。 Fedora 這樣做是為了確定負載並在必要時為更新提供更好的伺服器。

這個 [選項](https://dnf.readthedocs.io/en/latest/conf_ref.html#options-for-both-main-and-repo) ，目前預設為關閉。 我們建議將 `countme=false` 添加到 `/etc/dnf/dnf.conf` ，以備將來啟用。 On systems that use `rpm-ostree` such as Silverblue, the countme option is disabled by masking the [rpm-ostree-countme](https://fedoramagazine.org/getting-better-at-counting-rpm-ostree-based-systems) timer.

openSUSE 還使用[唯一的 ID](https://en.opensuse.org/openSUSE:Statistics) 來計算系統，可以通過刪除 `/var/lib/zypp/AnonymousUniqueId` 檔來禁用它。
