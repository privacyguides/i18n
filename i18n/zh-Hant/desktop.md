---
title: "桌上型電腦"
icon: simple/linux
description: 因為隱私保護和軟體自由，通常建議用 Linux發行版。
cover: desktop.webp
---

基於隱私保護和軟體自由，通常建議用 Linux 發行版。 如果您還不曾用過 Linux ，以下是我們建議可試試的發行版，以及一些 Linux發行版的隱私和安全提升技巧。

- [一般Linux 概述 :material-arrow-right-drop-circle:](os/linux-overview.md)

## 傳統發行版

### Fedora Workstation（Fedora 工作站）

!!! recommendation

    ![Fedora logo](assets/img/linux-desktop/fedora-workstation.svg){ align=right }
    
    **Fedora Workstation** 是我們推薦給Linux新手的發行版。 Fedora 通常較其他發行版更早採用較新技術，例如 [Wayland](https://wayland.freedesktop.org/) ， [PipeWire](https://pipewire.org)。 這些新技術通常會在安全性、隱私性和可用性方面有所改善。
    
    [:octicons-home-16: Homepage](https://fedoraproject.org/workstation/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://docs.fedoraproject.org/en-US/docs/){ .card-link title=Documentation}
    [:octicons-heart-16:](https://whatcanidoforfedora.org/){ .card-link title=Contribute }

Fedora 有一個半滾動的發布週期。 雖然像 [GNOME](https://www.gnome.org) 這樣的套件在下一個Fedora發布之前會被凍結，但大多數套件（包括內核）在該版的整個生命週期中都會頻繁更新。 每個 Fedora 版本支持一年，每6個月發布新版本。

### openSUSE Tumbleweed

!!! recommendation

    ![openSUSE Tumbleweed logo](assets/img/linux-desktop/opensuse-tumbleweed.svg){ align=right }
    
    **openSUSE Tumbleweed** 是一個穩定滾動發行版。
    
    openSUSE Tumbleweed 有一個 [transactional update](https://kubic.opensuse.org/blog/2018-04-04-transactionalupdates/)系統，使用 [Btrfs](https://en.wikipedia.org/wiki/Btrfs)和 [Snapper](https://en.opensuse.org/openSUSE: Snapper_Tutorial)來確保快照可以在出現問題時回滾。
    
    [:octicons-home-16: Homepage](https://get.opensuse.org/tumbleweed/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://doc.opensuse.org/){ .card-link title=Documentation}
    [:octicons-heart-16:](https://shop.opensuse.org/){ .card-link title=Contribute }

Tumbleweed 遵循滾動發佈模式，每個更新都是快照發布。 當您升級系統時，會下載新的快照。 每個快照都通過一系列自動化測試，由 [openQA](https://openqa.opensuse.org) 運行，以確保其質量。

### Arch Linux

!!! recommendation

    ![Arch logo](assets/img/linux-desktop/archlinux.svg){ align=right }
    
    **Arch Linux** 是一個輕量級的、自己動手(DIY)的發行版，意味著只能得到你安裝的東西。 如需更多資訊，請參閱他們的 [FAQ](https://wiki.archlinux.org/title/Frequently_asked_questions)。
    
    [:octicons-home-16: Homepage](https://archlinux.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://wiki.archlinux.org/){ .card-link title=Documentation}
    [:octicons-heart-16:](https://archlinux.org/donate/){ .card-link title=Contribute }

Arch Linux有一個滾動發佈週期。 沒有固定的發布時間表，套件經常更新。

作為 DIY 發行版，用戶需要 [自行設置與維護](os/linux-overview.md#arch-based-distributions) 系統。 Arch有一個 [官方安裝程式](https://wiki.archlinux.org/title/Archinstall) ，使安裝過程更容易。

[Arch Linux ](https://reproducible.archlinux.org) 大部份軟體包是 [可復制的](https://reproducible-builds.org)。

## 不可變動的發行版本

### Fedora Silverblue

!!! recommendation

    ![Fedora Silverblue logo](assets/img/linux-desktop/fedora-silverblue.svg){ align=right }
    
    **Fedora Silverblue** 和 **Fedora Kinoite** 是自 Fedora 變體的不可更動發行版，主要關注容器工作流程。 Silverblue 搭配 [GNOME](https://www.gnome.org/)桌面環境，而 Kinoite 則探 [KDE](https://kde.org/)。 Silverblue 和 Kinoite 遵循 Fedora Workstation 同樣的發佈時間表，受益於相同的快速更新並保持非常接近上遊。
    
    [:octicons-home-16: Homepage](https://fedoraproject.org/silverblue/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://docs.fedoraproject.org/en-US/fedora-silverblue/){ .card-link title=Documentation}
    [:octicons-heart-16:](https://whatcanidoforfedora.org/){ .card-link title=Contribute }

Silverblue (及 Kinoite) 和 Fedora Workstation 差異是它們 替換掉 [DNF](https://docs.fedoraproject.org/en-US/quick-docs/dnf/) 套件管理改成更先進的 [`rpm-ostree`](https://docs.fedoraproject.org/en-US/fedora/latest/system-administrators-guide/package-management/rpm-ostree/)方式。 `rpm-ostree` 套件管理器的工作原理是下載系統的基本映像，然後將套件覆蓋在類似 [git](https://en.wikipedia.org/wiki/Git)的提交樹中。 當系統更新時，會下載新的基本影像，並將疊加層應用於該新影像。

更新完成後，您將重新啟動系統進入新的部署。 `rpm-ostree` 保留系統的兩個部署，以便在新部署中出現故障時可以輕鬆回滾。 還可以根據需要固定更多部署。

[Flatpak](https://www.flatpak.org) 是這些發行版本的主要套件安裝方式，而 `rpm-ostree` 只用在基礎映像上疊加那些無法留在容器的套件。

作為  Flatpaks 替代品， [Toolbox](https://docs.fedoraproject.org/en-US/fedora-silverblue/toolbox/)可以建立 [Podman](https://podman.io) 容器，與主機系統共用主目與仿傳統 Fedora 環境。挑剔的開發者 [喜歡這個功能](https://containertoolbx.org)。

### NixOS

!!! recommendation

    ![NixOS logo](assets/img/linux-desktop/nixos.svg){ align=right }
    
    NixOS 是基於 Nix套件管理器的獨立發行版，專注於可重複性和可靠性。
    
    [:octicons-home-16: Homepage](https://nixos.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://nixos.org/learn.html){ .card-link title=Documentation}
    [:octicons-heart-16:](https://nixos.org/donate.html){ .card-link title=Contribute }

NixOS’ 套件管理器 將各個套件版本儲存在**Nix store** 底下不同的資料夾。 因此，您可以在系統上安裝相同套件的不同版本。 套件內容寫入資料夾後，該資料夾會變成唯讀。

NixOS 還提供原子更新：它會下載或(建立)新系統生成需要的套件和檔案，然後切換到新系統。 有不同的方法來切換到新代系統：讓 NixOS 重新啟動時激活它，或者在運行時切換。 也可以在運行時間切換到新代系統來 *測試*，但不將它設成當前系統。 如果更新過程中出現打斷，可以重新啟動並自動返回到系統的工作版本。

Nix 套件管理器使用純函數式語言（也稱為Nix ）來定義套件。

[Nixpkgs](https://github.com/nixos/nixpkgs) （套件的主要來源）包含在單一的 GitHub 儲存庫中。 您也可以用相同的語言定義自己的套件，然後輕鬆地將它們包含在您的配置中。

Nix是一個基於源的套件管理器；如果二進位快取中沒有預先構建的可用性， Nix 只會使用其定義從源構建套件。 它在沙盒 *純* 環境中構建每個套件，盡可能獨立於主機系統，從而使二進制文件可重現。

## 以匿名爲重點的發行版

### Whonix

!!! recommendation

    ![Whonix logo](assets/img/linux-desktop/whonix.svg){ align=right }
    
    **Whonix** 為基於 [Kicksecure](#kicksecure) 專注在安全的 Debian 分支系統。 它旨在提供網際網路的隱私、安全和匿名性。 Whonix 最好與 [Qubes OS](# qubes-os) 配合使用。
    
    [:octicons-home-16: Homepage](https://www.whonix.org/){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://www.dds6qkxpwdeubwucdiaord2xgbbeyds25rbsgr73tbfpqpt4a6vjwsyd.onion){ .card-link title="Onion Service" }
    [:octicons-info-16:](https://www.whonix.org/wiki/Documentation){ .card-link title=Documentation}
    [:octicons-heart-16:](https://www.whonix.org/wiki/Donate){ .card-link title=Contribute }

Whonix 運行兩個虛擬機器：一個“工作站”和一個 Tor “閘道”。 來自工作站的所有通訊都必須通過 Tor 閘道。 這意味著，即使工作站受到某種惡意軟體的破壞，真實的IP地址仍然隱藏。

它的一些功能包括 Tor Stream Isolation ， [按鍵匿名](https://www.whonix.org/wiki/Keystroke_Deanonymization#Kloak)， [加密交換](https://github.com/Whonix/swap-file-creator)以及加固的記憶體分配器。

Whonix 未來版本可能包括 [完整系統 AppArmor](https://github.com/Whonix/apparmor-profile-everything) 和 [個沙盒應用程式啟動器](https://www.whonix.org/wiki/Sandbox-app-launcher) ，以完全限制系統上的所有進程。

Whonix 最好與 Qubes</a>一起使用

，與其他 hypervisor相比， Qubes-Whonix 有不同 [缺點](https://forums.whonix.org/t/qubes-whonix-security-disadvantages-help-wanted/8581) 。</p> 



### Tails

!!! recommendation

    ![Tails logo](assets/img/linux-desktop/tails.svg){ align=right }
    
    **Tails** 是一個基於Debian 的自生作業系統，通過 Tor 路由所有通訊，透過 DVD ， USB記憶棒或 SD卡安裝幾乎可在任何電腦上啟動。 它使用 [Tor](tor.md) 來保護隱私和匿名性，同時規避審查制度，並且使用的電腦在關閉電源後不會留下任何痕跡。
    
    [:octicons-home-16: Homepage](https://tails.boum.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://tails.boum.org/doc/index.en.html){ .card-link title=Documentation}
    [:octicons-heart-16:](https://tails.boum.org/donate/){ .card-link title=Contribute }
    

由於失憶功能(意指沒有寫入磁碟)，Tails 非常適合對抗資料探集；然而，它不像 Whonix 那樣是硬化發行版。 它缺乏 Whonix 的許多匿名和安全功能，並且更新頻率較低（每六周一次）。 被惡意軟體入侵的 Tails 系統可能會繞過透明代理，使用戶去匿名化。

Tails Tor 瀏覽器預設包含 [uBlock Origin](desktop-browsers.md#ublock-origin) ，這可能會使對手更容易指紋識別 Tails 用戶。 [Whonix](desktop.md#whonix) 虛擬機器可能更為防洩漏may be more leak-proof, however they are not amnesic, ，但它沒有失憶功能，因此資料可以從儲存設備上進行恢復。

設計上， Tails 每次重新啟動後意謂將完全重置。 加密 [永久存儲](https://tails.boum.org/doc/persistent_storage/index.en.html) 可以配置來存儲一些資料。



## 以安全爲重點的發行版



### Qubes OS

!!! recommendation

    ![Qubes OS logo](assets/img/qubes/qubes_os.svg){ align=right }
    
    **Qubes OS** 是開源作業系統，利用安全的虛擬器為桌面運算提供更強的安全性 (或稱"qubes"). Qubes 基於 Xen, X Window 系統與 Linux。 大多數 Linux 應用它都可以執行且適用 Linux 驅動。
    
    [:octicons-home-16: Homepage](https://www.qubes-os.org/){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://qubesosfasa4zl44o4tws22di6kepyzfeqv3tg4e3ztknltfxqrymdad.onion){ .card-link title="Onion Service" }
    [:octicons-eye-16:](https://www.qubes-os.org/privacy/){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://www.qubes-os.org/doc/){ .card-link title=Documentation }
    [:octicons-code-16:](https://github.com/QubesOS/){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://www.qubes-os.org/donate/){ .card-link title=Contribute }
    

Qubes OS 作業系統將子系統（例如網絡、USB等）和應用程式隔離在個別的 *qubes*以保護電腦。 如果系統的一部分被破壞，其餘的 *qubes*與核心系統仍受到保護。

有關 Oubes 運作的進一步資訊，請參考我們完整的 [Qubes OS 介紹](os/qubes-overview.md) 頁面。



### Kicksecure

雖然我們在大多數情況下[建議不要](os/linux-overview.md#release-cycle)使用“永遠過時”的發行版，例如用於桌面的 Debian，但 Kicksecure 是一個基於 Debian 的操作系統，其功能已強化，遠遠超出了典型的 Linux 安裝。

!!! 推薦

    ![Kicksecure logo](assets/img/linux-desktop/kicksecure.svg){ align=right }
    
    **Kicksecure**—其簡化的介紹—可以說是一組腳本、置配與套件的組合，可大幅減少 Debian 的攻擊面。 它預設覆蓋了大量的隱私和加固建議。 它也是 [Whonix](#whonix) 的基礎作業系統。
    
    [:octicons-home-16: Homepage](https://www.kicksecure.com/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.kicksecure.com/wiki/Privacy_Policy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://www.kicksecure.com/wiki/Documentation){ .card-link title=Documentation }
    [:octicons-code-16:](https://github.com/Kicksecure){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://www.kicksecure.com/wiki/Donate){ .card-link title=Contribute }
    



## 標準

選擇適合您的 Linux 發行版取決於個人喜好差異，本頁**並非**是每一款發行版的詳盡列表。 我們在 Linux 介紹頁有更詳細的 [如何選擇發行版本](os/linux-overview.md#choosing-your-distribution) 的說明。 *這個*頁面上的發行版通常都遵循我們介紹的指南，且都滿足以下標準：

- Free and open source.
- 必須定期接收軟體和內核更新。
- [Avoids X11](os/linux-overview.md#wayland). 
      - 這裡值得注意的例外是 Qubes，但虛擬化可以避免 X11 常發生的隔離問題。 其隔離僅適用於*在不同 qube*（虛擬機）中運行的應用程式，在*同一個* qube 運行的應用程式則無法保護。
- 安裝時必須支援全磁碟加密。
- 不可將定期更新發佈凍結超過1年。 
      - 我們 [不建議](os/linux-overview.md#release-cycle) 桌機使用“長期支援”或“穩定”發行版。
- 需要支持各種各樣的硬體。
- 偏好較大型的專案。 
      - 維護作業系統是一項大挑戰，小型專案往往會犯更多可避免的錯誤，或延遲重大更新（或更糟糕的是，很快就完全消失）。 我們傾向於至少可維持10 年的專案（無論是由於公司支持還是非常重要的社區支持），而不是手工構建或只有少數維護人員的專案。

此外，[我們推薦專案的一般準則](about/criteria.md) 仍然適用。 **請注意我們和所推薦的服務商沒有任何利害關係。**
