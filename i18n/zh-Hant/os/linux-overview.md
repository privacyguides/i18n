---
title: Linux概述
icon: simple/linux
description: Linux 為開源、以隱私為中心的桌面作業系統替代選項，但並非所有發行版都一模一樣。
---

人們通常認為 [開源](https://en.wikipedia.org/wiki/Open-source_software) 軟體本質上是安全的，因為源代碼可以公開取得。 人們期望定期進行社群驗證；然而這種情況 [並不常見](https://seirdy.one/posts/2022/02/02/floss-security/)。 它確實取決於許多因素，例如專案活動、開發人員經驗、用於 [代碼審查的嚴格程度](https://en.wikipedia.org/wiki/Code_review)以及 [代碼庫](https://en.wikipedia.org/wiki/Codebase) 特定部分的關注頻率，這些可能多年未被觸及。

目前，桌面 Linux 確實有一些領域可以比商有作業系統更好地改進，例如：

- 驗證啟動鏈，例如 Apple 的 [Secure Boot](https://support.apple.com/guide/security/startup-security-utility-secc7b34e5b5/web) （帶有 [Secure Enclave](https://support.apple.com/guide/security/secure-enclave-sec59b0b31ff/1/web/1)） ， Android的 [Verified Boot](https://source.android.com/security/verifiedboot)， ChromeOS [Verified boot](https://www.chromium.org/chromium-os/chromiumos-design-docs/security-overview/#verified-boot)或 Microsoft Windows [開機程序](https://docs.microsoft.com/en-us/windows/security/information-protection/secure-the-windows-10-boot-process) 與 [TPM](https://docs.microsoft.com/en-us/windows/security/information-protection/tpm/how-windows-uses-the-tpm)。 這些功能和硬體技術都有助於防止惡意軟體的持續篡改或 [邪惡女僕的攻擊](https://en.wikipedia.org/wiki/Evil_Maid_attack)
- 強大的沙箱解決方案，如在 [macOS](https://developer.apple.com/library/archive/documentation/Security/Conceptual/AppSandboxDesignGuide/AboutAppSandbox/AboutAppSandbox.html)， [ChromeOS](https://chromium.googlesource.com/chromiumos/docs/+/HEAD/sandboxing.md)，和 [Android](https://source.android.com/security/app-sandbox)。 常用的 Linux 沙盒解決方案，如 [Flatpak](https://docs.flatpak.org/en/latest/sandbox-permissions.html) 和 [Firejail](https://firejail.wordpress.com/) ，仍然有很長的路要走。
- 強大的 [漏洞緩解措施](https://madaidans-insecurities.github.io/linux.html#exploit-mitigations)

儘管有這些缺點，但如果可以稍加調整，桌面 Linux 發行版還是很不錯的。

- 避免商業作業系統經常出現的遙測現象
- 保持 [軟體自由](https://www.gnu.org/philosophy/free-sw.en.html#four-freedoms)
- 有專注隱私保護的作業系統，如 [Whonix](https://www.whonix.org) 或 [Tails](https://tails.boum.org/)

我們網站通常使用術語 "Linux "來講述桌面Linux 發行版。 其它也使用Linux內核的作業系統，如 ChromeOS、Android 和Qubes OS，此處不作討論。

[建議的 Linux 發行版 :material-arrow-right-drop-circle:](../desktop.md ""){.md-button}

## 挑選發行版本

所有 Linux 發行版並非一模一樣。 我們的 Linux 建議頁面並不打算成為您應該使用哪個發行版的權威來源，但在選擇使用哪個發行版時，您應該記住一些事情。

### 發布週期

強烈建議您選擇與穩定的上遊軟體版本保持接近的發行版，通常稱為滾動發行版。 因為凍結發行週期旳發行版通常不會更新套件版本，並且在安全性更新方面落後。

像 [Debian](https://www.debian.org/security/faq#handling)這樣的凍結發行版，套件維護人員預計會回移補丁修復漏洞，而不是將軟體提昇到上遊開發人員發布的“下一個版本”。 某些安全修復

根本没收到 [CVE](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures) （特别是不流行的軟體），在此種補丁模式不會放入發行版。 因此小型安全修復有時候要等到下次主要發佈時才一起進行。</p> 

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

人們常會混淆“以安全為中心”的發行版和“滲透測試”發行版。 快速搜索“最安全的 Linux發行版”，通常會得到像 Kali Linux, Black Arch 和 Parrot OS 這樣結果。 這些發行版是攻擊性的滲透測試發行版，捆綁了測試其他系統的工具。 它們不包括任何 "額外的安全 "或常規使用的防禦性緩解措施。



### 基於 Arch Linux 的發行版

不推薦 Arch發行版(無論哪個發行版)給剛接觸 Linux 的人，因為它們需要定期進行 [系統維護](https://wiki.archlinux.org/title/System_maintenance)。 Arch沒有底層軟體選擇的發行版更新機制。 因此，必須了解當前趨勢，並在新技術取代舊有做法時予以採用。

對於一個安全的系統，還應有足夠的 Linux 知識來作正確安全設置，如採用 [強制性訪問控制](https://en.wikipedia.org/wiki/Mandatory_access_control) 系統，設置 [內核模塊](https://en.wikipedia.org/wiki/Loadable_kernel_module#Security) 黑名單，硬化啟動參數，操作 [sysctl](https://en.wikipedia.org/wiki/Sysctl) 參數，並知道需要哪些組件，如 [Polkit](https://en.wikipedia.org/wiki/Polkit)。

使用 [Arch User Repository (AUR)](https://wiki.archlinux.org/title/Arch_User_Repository), **者必須** 對該服務中安裝的 PKGBUILD進行審計。 AUR 軟體套件是社區製作的內容，未經任何審查，很容易受到軟體供應鏈的攻擊， [事實上已發生過這類事件](https://www.bleepingcomputer.com/news/security/malware-found-in-arch-linux-aur-package-repository/)。 應該少用 AUR，而往往各種網頁有很多不好的建議，指導人們盲目地使用 [AUR 幫助器](https://wiki.archlinux.org/title/AUR_helpers) 卻沒有足夠警告。 類似的警告也適用基於Debian 發行版上使用第三方個人軟體套件檔案(PPAs)或 Fedora使用社區項目(COPR)。

如果是 Linux 老手，希望使用基於 Arch 發行版，我們只推薦主線 Arch Linux，而不是任何衍生品。 我們特別建議不要使用這兩種 Arch 衍生品。

- **Manjaro**: 此發行版將軟體套件保留 2週，以確保不會破壞他們自己的修改，而不是確保上游的穩定。 使用AUR軟體套件時，通常是根據 Arch 軟體庫中最新的 [存放庫構建](https://en.wikipedia.org/wiki/Library_(computing))。
- **Garuda**: 他們使用 [Chaotic-AUR](https://aur.chaotic.cx/) ，它自動地、盲目地從 AUR 編譯軟件套件。 沒有驗證程序去確保 AUR 套件不會受到供應鏈攻擊。



### Kicksecure

雖然我們強烈建議不要使用 Debian 這類過時的發行版，但有一種基於Debian 的加固作業系統，比傳統的 Linux 發行版更安全。 [Kicksecure](https://www.kicksecure.com/)。 簡單地說，Kicksecure 是一組腳本、配置和軟體套件，可大大減少 Debian 的攻擊面。 它預設覆蓋了大量的隱私和加固建議。



### Linux-libre 內核與 “Libre” 發行版

我們非常 **不推薦**使用 Linux-libre 內核，因為它[移除了安全緩和](https://www.phoronix.com/news/GNU-Linux-Libre-5.7-Released) 以及由於意識型態而 [壓制有關微碼脆弱的內核警告](https://news.ycombinator.com/item?id=29674846)。



## 一般性建議



### 磁碟加密

大多數Linux 發行版安裝程序中都有啟用 [LUKS](../encryption.md#linux-unified-key-setup) FDE之選項。 如果在安裝時沒有設置這個選項，就只能重新安裝，因為在 [系統系統](https://en.wikipedia.org/wiki/File_system) 被格式化 [磁碟分區](https://en.wikipedia.org/wiki/Disk_partitioning)後進行加密。 我們還建議安全地刪除儲存設備。

- [安全資料清除 :material-arrow-right-drop-circle:](https://blog.privacyguides.org/2022/05/25/secure-data-erasure/)



### Swap

考慮使用[ZRAM](https://wiki.archlinux.org/title/Zram#Using_zram-generator) 或 [加密的d swap](https://wiki.archlinux.org/title/Dm-crypt/Swap_encryption)取代未加密的swap 以避免潛在地把敏感資料推送到 [swap 空間](https://en.wikipedia.org/wiki/Memory_paging)的安全問題。 基於 Fedora 的發行版 [預設使用 ZRAM](https://fedoraproject.org/wiki/Changes/SwapOnZRAM)。



### Wayland

建議使用支持 [Wayland](https://en.wikipedia.org/wiki/Wayland_(display_server_protocol)) 顯示協議的桌面環境，因為它的開發 [考慮到了安全](https://lwn.net/Articles/589147/)。 其前身 [X11](https://en.wikipedia.org/wiki/X_Window_System)，不支持GUI 隔離，允許所有視窗[記錄畫面、日誌和注入其他視窗的輸入](https://blog.invisiblethings.org/2011/04/23/linux-security-circus-on-gui-isolation.html)，使任何沙盒嘗試都是徒勞。 雖然有一些選項可以做嵌套 X11，比如 [Xpra](https://en.wikipedia.org/wiki/Xpra) 或 [Xephyr](https://en.wikipedia.org/wiki/Xephyr)，但它們往往會帶來負面性能，設置也不方便，不如 Wayland 可取。

幸好常見的桌面環境，如 [GNOME](https://www.gnome.org)， [KDE](https://kde.org)以及視窗管理器 [Sway](https://swaywm.org) 都支持 Wayland。 某些發佈版本如 Fedora 和 Tumbleweed 預設使用它，有些則可能在未來也會這樣作在 X11 成為 [硬性維護模式](https://www.phoronix.com/news/X.Org-Maintenance-Mode-Quickly)後。 如果使用以下的桌面環境，就像在桌面顯示管理器中選擇 "Wayland "一樣簡單([GDM](https://en.wikipedia.org/wiki/GNOME_Display_Manager), [SDDM](https://en.wikipedia.org/wiki/Simple_Desktop_Display_Manager)) 。

我們**反對**使用不支援 Wayland 的桌面環境或視窗管理器，如Cinnamon（Linux Mint）、Pantheon（Elementary OS）、MATE、Xfce 和 i3。



### 商用靭體(Microcode更新)

Linux 發行版，如 [Linux-libre](https://en.wikipedia.org/wiki/Linux-libre) 或 DIY(Arch Linux)，不附帶商業專用的 [微碼](https://en.wikipedia.org/wiki/Microcode) 更新，這類更新通常會修補漏洞。 這些漏洞例子包括： [Spectre](https://en.wikipedia.org/wiki/Spectre_(security_vulnerability)), [Meltdown](https://en.wikipedia.org/wiki/Meltdown_(security_vulnerability)), [SSB](https://en.wikipedia.org/wiki/Speculative_Store_Bypass), [Foreshadow](https://en.wikipedia.org/wiki/Foreshadow), [MDS](https://en.wikipedia.org/wiki/Microarchitectural_Data_Sampling), [SWAPGS](https://en.wikipedia.org/wiki/SWAPGS_(security_vulnerability)), 以及其他 [硬體漏洞](https://www.kernel.org/doc/html/latest/admin-guide/hw-vuln/index.html)。

我們 **強烈建議** 安裝微碼更新，因為CPU 出廠時已經在運行專有的微碼。 Fedora 和 openSUSE 都預設採用微碼更新。



### 更新

大多數 Linux 發行版會自動安裝更新或發出提醒。 重要的是保持作業系統系統最新，當發現漏洞時，可修補軟體。

一些發行版（尤其是那些針對進階用戶）更加簡陋，指望使用者自己能做一些事情（例如 Arch 或 Debian）。 例如需要手動運行 "軟體套件管理器" (`apt`, `pacman`, `dnf`等等)，以便接收重要的安全更新。

此外，一些發行版不會自動下載靭體更新。 为此，你将需要安装 [`fwupd`](https://wiki.archlinux.org/title/Fwupd)。



## 隱私微調



### MAC 地址隨機化

許多桌面 Linux 發行版（Fedora、openSUSE等）自帶 [網路管理員](https://en.wikipedia.org/wiki/NetworkManager)，以配置以太網和 Wi-Fi設置。

在使用NetworkManager時，可以隨機化 [](https://fedoramagazine.org/randomize-mac-address-nm/) [MAC 地址](https://en.wikipedia.org/wiki/MAC_address)。 這在Wi-Fi 上提供了更多隱私，因為這讓追踪所連網路的特定設備變得更困難。 但這 [**並不是**](https://papers.mathyvanhoef.com/wisec2016.pdf) 讓您匿名。

將設置改為 **隨機** ，而不是 **穩定**，正如 [這篇文章建議](https://fedoramagazine.org/randomize-mac-address-nm/)。

如使用 [systemd-networkd](https://en.wikipedia.org/wiki/Systemd#Ancillary_components)，需要設置 [`MACAddressPolicy=random`](https://www.freedesktop.org/software/systemd/man/systemd.link.html#MACAddressPolicy=) ，以啟用 [RFC 7844 (Anonymity Profiles for DHCP Clients)](https://www.freedesktop.org/software/systemd/man/systemd.network.html#Anonymize=)。

對以太網上的 MAC 地址進行隨機化的意義不大，因為系統管理員可以通過查看 [網路交換機上使用的端口找到您](https://en.wikipedia.org/wiki/Network_switch)。 隨機化 Wi-Fi MAC 地址必須有 Wi-Fi 靭體支持。



### 其他標識符

還有一些其他的系統標識符，可能要小心對待。 您應該考慮看看是否適用於您的 [威脅模型](../basics/threat-modeling.md)。

- **主機名稱 **，系統的主機名稱會分享到所連接的網路。 應避免主機名稱像你的名字或作業系統等具識別度的術語，最好用一般術語或隨機字符串。
- **用戶名稱 ** 。同樣地，用戶名稱會在系統中以各種方式使用。 考慮用 "用戶 "這樣一般常見字，而不是您的真實姓名。
- **機器 ID：**：在安裝過程中，會生成一個獨特的機器ID 並存儲在您的設備上。 考慮 [將它設置為一個通用 ID](https://madaidans-insecurities.github.io/guides/linux-hardening.html#machine-id)。



### 系統計數

Fedora 專案使用[`countme`](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting#Detailed_Description) 變量而非獨特 ID 來[計算多少](https://fedoraproject.org/wiki/Changes/DNF_Better_Counting)系統訪問它的鏡像。 Fedora 這樣做是為了確定負載並在必要時為更新提供更好的伺服器。

這個 [選項](https://dnf.readthedocs.io/en/latest/conf_ref.html#options-for-both-main-and-repo) ，目前預設為關閉。 我們建議將 `countme=false` 添加到 `/etc/dnf/dnf.conf` ，以備將來啟用。 使用 `rpm-ostree` 的系統，如 Silverblue，通過遮蔽 [rpm-ostree-countme](https://fedoramagazine.org/getting-better-at-counting-rpm-ostree-based-systems/) 計時器來禁用 countme 選項。

openSUSE 還使用[唯一的 ID](https://en.opensuse.org/openSUSE:Statistics) 來計算系統，可以通過刪除 `/var/lib/zypp/AnonymousUniqueId` 檔來禁用它。
