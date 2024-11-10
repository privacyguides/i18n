---
title: Linux 概述
icon: simple/linux
description: Linux 是一種開放原始碼、注重隱私的桌面作業系統替代選項，但並非所有的發行版都是一樣的。
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

一個 [常見的誤解](../basics/common-misconceptions.md#open-source-software-is-always-secure-or-proprietary-software-is-more-secure) 是，Linux 和其他開放原始碼軟體天生就很安全，只因為原始碼是可被存取的。 人們期望定期進行社群驗證；然而這種情況 [並不常見](https://seirdy.one/posts/2022/02/02/floss-security)。

現實中，發行版安全取決於許多因素，例如專案活動、開發人員經驗、用於代碼審查的嚴格程度以及代碼庫 特定部分的關注頻率，這些可能多年未被聞問。

### 遺失的安全功能

目前，在某些安全功能方面，桌面 Linux [落後於 macOS 或 Android ](https://discussion.fedoraproject.org/t/fedora-strategy-2028-proposal-fedora-linux-is-as-secure-as-macos/46899/9)。 希望未來能看到這些領域的改進。

- Linux 的**驗證開機** 不如 Apple 的 [Secure Boot 安全開機](https://support.apple.com/guide/security/secac71d5623/web) 或 Android’s [Verified Boot 驗證開機](https://source.android.com/security/verifiedboot)。 驗證開機可防止惡意軟體的持久篡改和 [evil maid attacks 邪惡女傭攻擊](https://en.wikipedia.org/wiki/Evil_Maid_attack)，但其[仍未及於大多數進階的發行版本](https://discussion.fedoraproject.org/t/has-silverblue-achieved-verified-boot/27251/3)。

- Linux 上的應用程式嚴重缺乏**強大的沙盒**，即使便使用 Flatpaks 等容器化應用程式或 Firejail 等沙盒解決方案還是不足。 Flatpak 是迄今為止最被看好的 Linux 沙盒實用工具，但它仍存在許多缺陷，且允許 [不安全的預設設定](https://flatkill.org/2020) ，這使得大多數應用程式可輕鬆繞過其沙盒。

此外，Linux 在實施 [漏洞緩解措施](https://madaidans-insecurities.github.io/linux.html#exploit-mitigations) 方面落後，這些緩解措施現已成為其他操作系統的標準配置，例如 Windows 上的任意代碼防護或 macOS 上的強化運行時間。 此外，大多數 Linux 程式和 Linux 本身都是用記憶體不安全語言編寫的。 記憶體損壞錯誤是造成[大多數漏洞](https://msrc.microsoft.com/blog/2019/07/a-proactive-approach-to-more-secure-code)的原因已修復並分配了CVE。 雖然 Windows 和 macOS 也是如此，但它們在使用記憶體安全語言（例如 Rust 和 Swift）上正在迅速進展，而Linux 方面則沒有這類以 Rust 重寫記憶體安全的投入 。

## 挑選發行版本

所有 Linux 發行版並非一模一樣。 我們的 [Linux 推薦頁面](../desktop.md)並不是您使用哪個發行版的權威來源，但我們的*建議*與以下準則一致。 選擇發行版時應記住以下幾點：

### 發布週期

強烈建議您選擇與穩定的上遊軟體版本保持接近的發行版，通常稱為滾動發行版。 因為凍結發行週期旳發行版通常不會更新套件版本，並且在安全性更新方面落後。

像 [Debian](https://debian.org/security/faq#handling)這樣的凍結發行版，套件維護人員預計會回移補丁修復漏洞，而不是將軟體提昇到上遊開發人員發布的“下一個版本”。 有些安全修補程式 (尤其是不太流行的軟體) 根本 [不會](https://arxiv.org/abs/2105.14565) 收到 [CVE ID](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures) ，因此無法透過此修補模式修補。 因此小型安全修復有時候要等到下次主要發佈時才一起進行。

我們不認為保留軟體套件和應用臨時補丁是好主意，因為它偏離了開發者計畫讓軟體工作的方式。 [Richard Brown](https://rootco.de/aboutme) 對此有一份簡報：

- [Regular Releases are Wrong, Roll for your life](https://youtu.be/i8c0mg_mS7U) <small>(YouTube)</small>

### 傳統 vs 原子更新

傳統上 Linux 發行版的更新模式是依次更新所需的軟體套件。 Fedora、Arch Linux 和其他基於 Debian 的發行版皆採納此種模式—而這種模式如果在更新時發生錯誤，其系統可靠性可能會因此降低。

而原子更新模式則是完全套用更新或完全不套用更新。 在採納原子更新模式的發行版上，如果在更新時發生錯誤（也許是由於停電），系統上就不會有任何改變。

因此 Silverblue 和 NixOS 等 [發行版](../desktop.md#atomic-distributions) 在這種情況下便可以依靠原子更新模式維持系統穩定性。 [Adam Šamalík](https://twitter.com/adsamalik) 介紹 `rpm-ostree` 如何與 Silverblue 搭配使用：

- [Let's try Fedora Silverblue — an immutable desktop OS! - Adam Šamalik](https://youtu.be/aMo4ZlWznao) <small>(YouTube)</small>

### 「注重安全」的發行版

人們常會混淆「注重安全」的發行版和「滲透測試」發行版。 快速搜索「最安全的 Linux發行版」，通常會得到像 Kali Linux、Black Arch 或 Parrot OS 這樣的結果。 這些發行版是攻擊性滲透測試發行版，捆綁了測試其他系統的工具。 它們不包括任何「額外的安全性」或常規使用的防禦性緩解措施。

### 基於 Arch Linux 的發行版

不推薦 Arch 或其相關發行版(無論哪個發行版)給剛接觸 Linux 的人，因為它們需要定期進行 [系統維護](https://wiki.archlinux.org/title/System_maintenance)。 Arch沒有底層軟體選擇的發行版更新機制。 因此，您必須瞭解當前趨勢，並在新做法取代舊有做法時自行採用。

對於安全的系統，您也應該有足夠的 Linux 知識來正確設定其系統，例如添加 [強制訪問控制](#mandatory-access-control) 系統、設定 [核心模組](https://en.wikipedia.org/wiki/Loadable_kernel_module#Security) 黑名單、加固開機參數、修改 [sysctl](https://en.wikipedia.org/wiki/Sysctl)參數，以及知道他們需要哪些元件，例如：[Polkit](https://en.wikipedia.org/wiki/Polkit)。

使用 [Arch User Repository (AUR)](https://wiki.archlinux.org/title/Arch_User_Repository)者 **必須** 對該服務下載的 PKGBUILD進行審計。 AUR 套件是社群製作的內容，未經任何審核，因此容易受到軟體 [:material-package-variant-closed-remove: 供應鏈攻擊](../basics/common-threats.md#attacks-against-certain-organizations ""){.pg-viridian} ，事實上 [過去](https://bleepingcomputer.com/news/security/malware-found-in-arch-linux-aur-package-repository) 確實曾發生過。

應該少用 AUR，而往往各種網頁有很多不好的建議，指導人們盲目地使用 [AUR 助手](https://wiki.archlinux.org/title/AUR_helpers) 卻沒有足夠警告。 類似的警告也適用於使用基於 Debian 的發行版上的第三方個人套件檔案（PPA）或 Fedora 系統上的社群專案（COPR）。

如果是 Linux 老手，希望使用基於 Arch 發行版，我們只推薦主線 Arch Linux，而不是任何衍生品。

此外，我們特別**反推薦**這兩個 Arch 衍生品：

- **Manjaro**: 此發行版將軟體套件保留 2週，以確保不會破壞他們自己的修改，而不是確保上游的穩定。 使用AUR軟體套件時，通常是根據 Arch 軟體庫中最新的 [存放庫構建](https://en.wikipedia.org/wiki/Library_(computing))。
- **Garuda**: 他們使用 [Chaotic-AUR](https://aur.chaotic.cx) ，會自動從 AUR 編譯軟體套件。 沒有驗證程序去確保 AUR 套件不會受到供應鏈攻擊。

### Linux-libre 內核與 “Libre” 發行版

我們建議**不**使用 Linux-libre 內核，因為它[刪除安全緩解措施](https://phoronix.com/news/GNU-Linux-Libre-5.7-Released)並[抑制有關易受攻擊的微代碼的內核警告](https://news.ycombinator.com/item?id=29674846)。

### 強制訪問控制

強制訪問控制是一套額外的安全控制，有助於限制應用程式和系統服務等部分。 Linux 發行版本中常見的兩種強制訪問控制實作是 [SELinux](https://github.com/SELinuxProject) 和 [AppArmor](https://apparmor.net) 。 Fedora 預設使用 SELinux，而 Tumbleweed 則在安裝程式中[預設](https://en.opensuse.org/Portal:SELinux)使用 AppArmor，並允許您[選擇](https://en.opensuse.org/Portal:SELinux/Setup)改用 SELinux 。

[Fedora](https://docs.fedoraproject.org/en-US/quick-docs/selinux-getting-started) 上的 SELinux 預設會限制 Linux軟體容器、虛擬機器和守護進程。 AppArmor 由 Snap 守護進程 用於 [沙盒化](https://snapcraft.io/docs/security-sandboxing) Snap，這些由 Snap 提供的軟體有 [嚴格](https://snapcraft.io/docs/snap-confinement) 限制，例如 [Firefox](https://snapcraft.io/firefox) 。 在 Fedora 的 [ConfinedUsers](https://fedoraproject.org/wiki/SIGs/ConfinedUsers) 特別興趣小組中，有社群致力於限制系統的更多部分。

## 一般性建議

### 磁碟加密

大多數Linux 發行版安裝程式中都有啟用 [LUKS](../encryption.md#linux-unified-key-setup) FDE之選項。 如果在安裝時沒有設定這個選項，就只能重新安裝，因為在 [系統系統](https://en.wikipedia.org/wiki/File_system) 被格式化 [磁碟分區](https://en.wikipedia.org/wiki/Disk_partitioning)後進行加密。 我們還建議安全地刪除儲存設備。

- [安全資料清除 :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/05/25/secure-data-erasure)

### Swap

考慮使用 [ZRAM](https://wiki.archlinux.org/title/Zram#Using_zram-generator) 而不是傳統的 swap 檔案或分區，以避免將潛在敏感的記憶資料寫入持久儲存（並提高性能）。 基於 Fedora 的發行版 [預設使用 ZRAM](https://fedoraproject.org/wiki/Changes/SwapOnZRAM)。

如果需要 suspend-to-disk （磁盤休眠）功能，則仍然需要使用傳統的swap 檔案或分區。 確保持久儲存設備上的任何交換空間予以[加密](https://wiki.archlinux.org/title/Dm-crypt/Swap_encryption)，以減輕一些威脅。

### 商用靭體(Microcode更新)

Linux 發行版，如 [Linux-libre](https://en.wikipedia.org/wiki/Linux-libre) 或 DIY(Arch Linux)，不附帶商業專用的 [微碼](https://en.wikipedia.org/wiki/Microcode) 更新，這類更新通常會修補漏洞。 這些漏洞的一些著名例子如: [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability))、[ Meltdown ](https://en.wikipedia.org /wiki/Meltdown_(security_vulnerability))、[SSB](https://en.wikipedia.org/wiki/Speculative_Store_Bypass)、[Foreshadow](https:/ / en.wikipedia.org/wiki/Foreshadow)、[MDS](https://en.wikipedia.org/wiki/Microarchitectural_Data_Sampling)、[SWAPGS](https: //en.wikipedia.org/wiki/SWAPGS_(security_vulnerability))，以及其他[硬體漏洞](https://kernel.org/doc/html/latest/admin-guide/hw- vuln /index.html)。

我們**強烈建議**安裝微碼更新，因為它們包含重要的 CPU 安全補丁，無法僅僅靠軟體緩解。 Fedora 和 openSUSE 預設都會套用微碼更新。

### 更新

大多數 Linux 發行版會自動安裝更新或發出提醒。 重要的是保持作業系統系統最新，當發現漏洞時，可修補軟體。

一些發行版（尤其是那些針對進階用戶）更加簡陋，指望使用者自己能做一些事情（例如 Arch 或 Debian） 例如需要手動運行 "軟體套件管理器" (`apt`, `pacman`, `dnf`等等)，以便接收重要的安全更新。

此外，一些發行版不會自動下載靭體更新。 為此需要安裝l [`fwupd`](https://wiki.archlinux.org/title/Fwupd)。

### 權限控制

支援 [Wayland](https://wayland.freedesktop.org) 顯示通訊協定的桌面環境 (DE) 比只支援 X11 的桌面環境 [更安全](https://lwn.net/Articles/589147) 。 然而，並非所有的 DE 都能充分利用 Wayland 的架構安全性改進。

舉例來說，GNOME 藉由對嘗試 [擷取螢幕的](https://gitlab.gnome.org/GNOME/gnome-shell/-/issues/3943) 第三方軟體實施權限控制，在安全性上比其他 DE 有顯著的優勢。 也就是說，當第三方應用程式嘗試擷取您的螢幕時，會提示您是否同意與該應用程式分享您的螢幕。

<figure markdown>
  ![Screenshot permissions](../assets/img/linux/screenshot_permission.png){ width="450" }
  <figcaption>GNOME 的截圖權限對話框</figcaption>
</figure>

許多替代方案尚未提供這些相同的權限控制[^1]；而有些則在等待 Wayland 在上游實作這些控制[^2]。

## 隱私微調

### MAC 位址隨機化

許多桌面 Linux 發行版（Fedora、openSUSE等）自帶 [網路管理員](https://en.wikipedia.org/wiki/NetworkManager)，以配定以太網和 Wi-Fi設定。

可[隨機化](https://fedoramagazine.org/randomize-mac-address-nm)<a href="https://en.wikipedia.org/wiki/MAC_address 使用NetworkManager 時的“MAC 位址”。 這在Wi-Fi 上提供了更多隱私，因為這讓追踪所連網路的特定設備變得更困難。 但這 [**並不是**](https://papers.mathyvanhoef.com/wisec2016.pdf) 讓您匿名。

建議將設定更改為**隨機**，而不是**穩定**，如[這篇文章的說明](https: // fedoramagazine.org/randomize-mac-address-nm)。

如果使用 [systemd-networkd](https://en.wikipedia.org/wiki/Systemd#Ancillary_components)，則需要設定 [`MACAddressPolicy=random`](https://freedesktop. org/software /systemd/man/systemd.link.html#MACAddressPolicy=) 這將啟用[RFC 7844（DHCP 用戶端的匿名設定檔）](https://freedesktop.org/software/ systemd/man /systemd.network.html#Anonymize=)。

MAC 位址隨機化主要有利於 Wi-Fi 連接。 對於乙太網路連接，隨機化 MAC 位址幾乎沒什麼好處(如果有的話)，因為網路管理員可以通過其他方式輕鬆識別您的裝置(例如檢查您在網路交換機上連接的端口)。 隨機化 Wi-Fi MAC 位址必須有 Wi-Fi 靭體支援。

### 其他標識符

還有一些其他的系統標識符，可能要小心對待。 您應該考慮看看是否適用於您的 [威脅模型](../basics/threat-modeling.md)。

- **主機名稱 **，系統的主機名稱會分享到所連接的網路。 應避免主機名稱像你的名字或作業系統等具識別度的術語，最好用一般術語或隨機字符串。
- **用戶名稱 ** 。同樣地，用戶名稱會在系統中以各種方式使用。 考慮用 "用戶 "這樣一般常見字，而不是您的真實姓名。
- **機器 ID**：在安裝過程中，會生成一個獨特的機器ID 並儲存在您的裝置上。 考慮 [將它設定為一個通用 ID](https://madaidans-insecurities.github.io/guides/linux-hardening.html#machine-id)。

### 系統計數

Fedora 專案使用[`countme`](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting#Detailed_Description) 變量而非獨特 ID 來[計算多少](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting)系統訪問它的鏡像。 Fedora 這樣做是為了確定負載並在必要時為更新提供更好的伺服器。

這個 [選項](https://dnf.readthedocs.io/en/latest/conf_ref.html#options-for-both-main-and-repo) ，目前預設為關閉。 我們建議將 `countme=false` 添加到 `/etc/dnf/dnf.conf` ，以備將來啟用。 使用 `rpm-ostree` 的系統，如 Silverblue，通過遮蔽 [rpm-ostree-countme](https://fedoramagazine.org/getting-better-at-counting-rpm-ostree-based-systems) 計時器來禁用 countme 選項。

openSUSE 還使用[唯一的 ID](https://en.opensuse.org/openSUSE:Statistics) 來計算系統，可以通過清空`/var/lib/zypp/AnonymousUniqueId` 此檔案來禁用。

[^1]: KDE 目前有一個開放的提案，加入螢幕擷取的控制： <https://invent.kde.org/plasma/xdg-desktop-portal-kde/-/issues/7>
[^2]: Sway 正在等待加入特定的安全控制，直到他們「知道 Wayland 的整體安全性會如何發展」： <https://github.com/swaywm/sway/issues/5118#issuecomment-600054496>
