---
title: "桌上型電腦"
icon: simple/linux
description: 基於隱私保護和軟體自由，通常建議用 Linux 發行版。
cover: desktop.webp
---

基於隱私保護和軟體自由，通常建議用 Linux 發行版。 如果您還不曾用過 Linux ，以下是我們建議可試試的發行版，以及一些 Linux發行版的隱私和安全提升技巧。

- [一般Linux 概述 :material-arrow-right-drop-circle:](os/linux-overview.md)

## 傳統發行版

### Fedora Workstation（Fedora 工作站）

<div class="admonition recommendation" markdown>

![Fedora logo](assets/img/linux-desktop/fedora.svg){ align=right }

**Fedora Workstation** 是我們推薦給Linux新手的發行版。 Fedora generally adopts newer technologies before other distributions e.g., [Wayland](https://wayland.freedesktop.org) and [PipeWire](https://pipewire.org). 這些新技術通常會在安全性、隱私性和可用性方面有所改善。

[:octicons-home-16: Homepage](https://fedoraproject.org/workstation){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.fedoraproject.org/en-US/docs){ .card-link title=Documentation}
[:octicons-heart-16:](https://whatcanidoforfedora.org){ .card-link title=Contribute }

</details>

</div>

Fedora 有一個半滾動的發布週期。 雖然像 [GNOME](https://gnome.org) 這樣的套件在下一個Fedora發布之前會被凍結，但大多數套件（包括內核）在該版的整個生命週期中都會頻繁更新。 每個 Fedora 版本支持一年，每6個月發布新版本。

### openSUSE Tumbleweed

<div class="admonition recommendation" markdown>

![openSUSE Tumbleweed logo](assets/img/linux-desktop/opensuse-tumbleweed.svg){ align=right }

**openSUSE Tumbleweed** 是一個穩定滾動發行版。

openSUSE Tumbleweed uses [Btrfs](https://en.wikipedia.org/wiki/Btrfs) and [Snapper](https://en.opensuse.org/openSUSE:Snapper_Tutorial) to ensure that snapshots can be rolled back should there be a problem.

[:octicons-home-16: Homepage](https://get.opensuse.org/tumbleweed){ .md-button .md-button--primary }
[:octicons-info-16:](https://doc.opensuse.org){ .card-link title=Documentation}
[:octicons-heart-16:](https://shop.opensuse.org){ .card-link title=Contribute }

</details>

</div>

Tumbleweed 遵循滾動發佈模式，每個更新都是快照發布。 當您升級系統時，會下載新的快照。 每個快照都通過一系列自動化測試，由 [openQA](https://openqa.opensuse.org) 運行，以確保其質量。

### Arch Linux

<div class="admonition recommendation" markdown>

![Arch logo](assets/img/linux-desktop/archlinux.svg){ align=right }

**Arch Linux** is a lightweight, do-it-yourself (DIY) distribution, meaning that you only get what you install. 如需更多資訊，請參閱他們的 [FAQ](https://wiki.archlinux.org/title/Frequently_asked_questions)。

[:octicons-home-16: Homepage](https://archlinux.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://wiki.archlinux.org){ .card-link title=Documentation}
[:octicons-heart-16:](https://archlinux.org/donate){ .card-link title=Contribute }

</details>

</div>

Arch Linux有一個滾動發佈週期。 沒有固定的發布時間表，套件經常更新。

作為 DIY 發行版，用戶需要 [自行設置與維護](os/linux-overview.md#arch-based-distributions) 系統。 Arch有一個 [官方安裝程式](https://wiki.archlinux.org/title/Archinstall) ，使安裝過程更容易。

[Arch Linux ](https://reproducible.archlinux.org) 大部份軟體包是 [可復制的](https://reproducible-builds.org)。

## Atomic Distributions

**原子發行版**（有時也稱為**不可變發行版**）是透過分層處理軟體包安裝和更新的作業系統更改核心系統映像，而不是直接修改系統。 Advantages of atomic distros include increased stability and the ability to easily roll back updates. 請見 [*Traditional vs. Atomic Updates*](os/linux-overview.md#traditional-vs-atomic-updates) 更深入了解。

### Fedora Atomic Desktops

<div class="admonition recommendation" markdown>

![Fedora logo](assets/img/linux-desktop/fedora.svg){ align=right }

**Fedora Atomic Desktops** 是 Fedora 的變體，它使用「rpm-ostree」套件管理器，專注於容器化工作流程和桌面應用程式的 Flatpak。 這些變體版都遵循 Fedora Workstation 同樣的發佈時間表，受益於相同的快速更新並保持非常接近上遊。

[:octicons-home-16: Homepage](https://fedoraproject.org/atomic-desktops){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.fedoraproject.org/en-US/emerging){ .card-link title=Documentation}
[:octicons-heart-16:](https://whatcanidoforfedora.org){ .card-link title=Contribute }

</details>

</div>

[Fedora Atomic Desktops](https://fedoramagazine.org/introducing-fedora-atomic-desktops) come in a variety of flavors depending on the desktop environment you prefer, such as **Fedora Silverblue** (which comes with [GNOME](https://gnome.org)), **Fedora Kinoite** (which comes with [KDE](https://kde.org)), **Fedora Sway Atomic**, or **Fedora Budgie Atomic**. 但不推薦最後一個，因為 Budgie 桌面環境[仍需要 X11](https://buddiesofbudgie.org/blog/wayland)。

這些作業系統與 Fedora Workstation 不同，它們用更高級方式替換了[DNF](https://docs.fedoraproject.org/en-US/quick-docs/dnf) 套件 管理器，其叫作[`rpm-ostree`](https://docs.fedoraproject.org/en-US/fedora/latest/system-administrators-guide/package-management/rpm-ostree)。 `rpm-ostree` 套件管理器的工作原理是下載系統的基本映像，然後將套件覆蓋在類似 [git](https://en.wikipedia.org/wiki/Git)的提交樹中。 當系統更新時，會下載新的基本影像，並將疊加層應用於該新影像。

更新完成後，您將重新啟動系統進入新的部署。 `rpm-ostree` keeps two deployments of the system so that you can easily roll back if something breaks in the new deployment. 還可以根據需要固定更多部署。

[Flatpak](https://flatpak.org) 是這些發行版本的主要套件安裝方式，而 `rpm-ostree` 只用在基礎映像上疊加那些無法留在容器的套件。

As an alternative to Flatpaks, there is the option of [Toolbx](https://docs.fedoraproject.org/en-US/fedora-silverblue/toolbox) to create [Podman](https://podman.io) containers which mimic a traditional Fedora environment, a [useful feature](https://containertoolbx.org) for the discerning developer. These containers share a home directory with the host operating system.

### NixOS

<div class="admonition recommendation" markdown>

![NixOS logo](assets/img/linux-desktop/nixos.svg){ align=right }

NixOS 是基於 Nix套件管理器的獨立發行版，專注於可重複性和可靠性。

[:octicons-home-16: Homepage](https://nixos.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://nixos.org/learn.html){ .card-link title=Documentation}
[:octicons-heart-16:](https://nixos.org/donate.html){ .card-link title=Contribute }

</details>

</div>

NixOS’ 套件管理器 將各個套件版本儲存在**Nix store** 底下不同的資料夾。 因此，您可以在系統上安裝相同套件的不同版本。 套件內容寫入資料夾後，該資料夾會變成唯讀。

NixOS also provides atomic updates. It first downloads (or builds) the packages and files for the new system generation and then switches to it. There are different ways to switch to a new generation: you can tell NixOS to activate it after reboot or you can switch to it at runtime. 也可以在運行時間切換到新代系統來 *測試*，但不將它設成當前系統。 如果更新過程中出現打斷，可以重新啟動並自動返回到系統的工作版本。

The Nix package manager uses a purely functional language—which is also called Nix—to define packages.

[Nixpkgs](https://github.com/nixos/nixpkgs) （套件的主要來源）包含在單一的 GitHub 儲存庫中。 您也可以用相同的語言定義自己的套件，然後輕鬆地將它們包含在您的配置中。

Nix是一個基於源的套件管理器；如果二進位快取中沒有預先構建的可用性， Nix 只會使用其定義從源構建套件。 它在沙盒 *純* 環境中構建每個套件，盡可能獨立於主機系統，從而使二進制文件可重現。

## 以匿名爲重點的發行版

### Whonix

<div class="admonition recommendation" markdown>

![Whonix logo](assets/img/linux-desktop/whonix.svg){ align=right }

**Whonix** 為基於 [Kicksecure](#kicksecure) 專注在安全的 Debian 分支系統。 它旨在提供網際網路的隱私、安全和匿名性。 Whonix 最好與 [Qubes OS](# qubes-os) 配合使用。

[:octicons-home-16: Homepage](https://whonix.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://dds6qkxpwdeubwucdiaord2xgbbeyds25rbsgr73tbfpqpt4a6vjwsyd.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://whonix.org/wiki/Documentation){ .card-link title=Documentation}
[:octicons-heart-16:](https://whonix.org/wiki/Donate){ .card-link title=Contribute }

</details>

</div>

Whonix 運行兩個虛擬機器：一個“工作站”和一個 Tor “閘道”。 來自工作站的所有通訊都必須通過 Tor 閘道。 這意味著，即使工作站受到某種惡意軟體的破壞，真實的IP地址仍然隱藏。

它的功能包括Tor 串流隔離、[擊鍵匿名](https://www.whonix.org/wiki/Keyrinkle_Deanonymization#Kloak)、[加密交換](https://github. com /Whonix/swap-file-creator)，以及強化的記憶體分配器。 Future versions of Whonix will likely include [full system AppArmor policies](https://github.com/roddhjav/apparmor.d) and a [sandboxed app launcher](https://whonix.org/wiki/Sandbox-app-launcher) to fully confine all processes on the system.

Whonix 最好[與 Qubes 結合使用](https://whonix.org/wiki/Qubes/Why_use_Qubes_over_other_Virtualizers)。 我們 [曾建議](os/qubes-overview.md#connecting-to-tor-via-a-vpn) on configuring in conjunction with a VPN 在 Qubes 底下與 ProxyVM 一起設定 Whonix 以便能對 ISP 隱瞞 Tor 的活動狀況。

### Tails

<div class="admonition recommendation" markdown>

![Tails logo](assets/img/linux-desktop/tails.svg){ align=right }

**Tails** 是一個基於Debian 的自生作業系統，通過 Tor 路由所有通訊，透過 DVD ， USB記憶棒或 SD卡安裝幾乎可在任何電腦上啟動。 它使用 [Tor](tor.md) 來保護隱私和匿名性，同時規避審查制度，並且使用的電腦在關閉電源後不會留下任何痕跡。

[:octicons-home-16: Homepage](https://tails.net){ .md-button .md-button--primary }
[:octicons-info-16:](https://tails.net/doc/index.en.html){ .card-link title=Documentation}
[:octicons-heart-16:](https://tails.net/donate){ .card-link title=Contribute }

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

Tails 關閉後[不會抹除](https://gitlab.tails.boum.org/tails/tails/-/issues/5356) [視訊記憶體](https://en.wikipedia.org/wiki/Dual- ported_video_RAM) 。 使用 Tails 後重新啟動電腦時，電腦可能會短暫顯示之前 Tails 最後一個畫面。 如果是關閉電腦而不是重新啟動，則影像記憶會在斷電一段時間後自動擦除。

</div>

由於失憶功能(意指沒有寫入磁碟)，Tails 非常適合對抗資料探集；然而，它不像 Whonix 那樣是硬化發行版。 它缺乏 Whonix 的許多匿名和安全功能，並且更新頻率較低（每六周一次）。 A Tails system that is compromised by malware may potentially bypass the transparent proxy, allowing for the user to be deanonymized.

Tails Tor 瀏覽器預設包含 [uBlock Origin](browser-extensions.md#ublock-origin) ，這可能會使對手更容易指紋識別 Tails 用戶。 [Whonix](desktop.md#whonix) 虛擬機器可能更為防洩漏may be more leak-proof, however they are not amnesic, ，但它沒有失憶功能，因此資料可以從儲存設備上進行恢復。

設計上， Tails 每次重新啟動後意謂將完全重置。 加密 [永久存儲](https://tails.net/doc/persistent_storage/index.en.html) 可以配置來存儲一些資料。

## 以安全爲重點的發行版

### Qubes OS

<div class="admonition recommendation" markdown>

![Qubes OS logo](assets/img/qubes/qubes_os.svg){ align=right }

**Qubes OS** 是開源作業系統，利用安全的虛擬器為桌面運算提供更強的安全性 (或稱"qubes"). Qubes 基於 Xen, X Window 系統與 Linux。 大多數 Linux 應用它都可以執行且適用 Linux 驅動。

[:octicons-home-16: Homepage](https://qubes-os.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://qubesosfasa4zl44o4tws22di6kepyzfeqv3tg4e3ztknltfxqrymdad.onion){ .card-link title="Onion Service" }
[:octicons-eye-16:](https://qubes-os.org/privacy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://qubes-os.org/doc){ .card-link title=Documentation }
[:octicons-code-16:](https://github.com/QubesOS){ .card-link title="Source Code" }
[:octicons-heart-16:](https://qubes-os.org/donate){ .card-link title=Contribute }

</details>

</div>

Qubes OS 作業系統將子系統（例如網絡、USB等）和應用程式隔離在個別的 *qubes*以保護電腦。 如果系統的一部分被破壞，其餘的 *qubes*與核心系統仍受到保護。

有關 Oubes 運作的進一步資訊，請參考我們完整的 [Qubes OS 介紹](os/qubes-overview.md) 頁面。

### Kicksecure

While we [recommend against](os/linux-overview.md#release-cycle) "perpetually outdated" distributions like Debian for desktop use in most cases, Kicksecure is a Debian-based operating system which has been hardened to be much more than a typical Linux install.

<div class="admonition recommendation" markdown>

![Kicksecure logo](assets/img/linux-desktop/kicksecure.svg){ align=right }

**Kicksecure**—其簡化的介紹—可以說是一組腳本、置配與套件的組合，可大幅減少 Debian 的攻擊面。 它預設覆蓋了大量的隱私和加固建議。 它也是 [Whonix](#whonix) 的基礎作業系統。

[:octicons-home-16: Homepage](https://kicksecure.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://kicksecure.com/wiki/Privacy_Policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://kicksecure.com/wiki/Documentation){ .card-link title=Documentation }
[:octicons-code-16:](https://github.com/Kicksecure){ .card-link title="Source Code" }
[:octicons-heart-16:](https://kicksecure.com/wiki/Donate){ .card-link title=Contribute }

</details>

</div>

## 標準

選擇適合您的 Linux 發行版取決於個人喜好差異，本頁**並非**是每一款發行版的詳盡列表。 我們在 Linux 介紹頁有更詳細的 [如何選擇發行版本](os/linux-overview.md#choosing-your-distribution) 的說明。 *這個*頁面上的發行版通常都遵循我們介紹的指南，且都滿足以下標準：

- 免費且開放原始碼。
- 必須定期接收軟體和內核更新。
- [Avoids X11](os/linux-overview.md#wayland).
    - 這裡值得注意的例外是 Qubes，但虛擬化可以避免 X11 常發生的隔離問題。 This isolation only applies to apps *running in different qubes* (virtual machines); apps running in the *same* qube are not protected from each other.
- 安裝時必須支援全磁碟加密。
- 不可將定期更新發佈凍結超過1年。
    - 我們 [不建議](os/linux-overview.md#release-cycle) 桌機使用“長期支援”或“穩定”發行版。
- 需要支持各種各樣的硬體。
- 偏好較大型的專案。
    - 維護作業系統是一項大挑戰，小型專案往往會犯更多可避免的錯誤，或延遲重大更新（或更糟糕的是，很快就完全消失）。 我們傾向於至少可維持10 年的專案（無論是由於公司支持還是非常重要的社區支持），而不是手工構建或只有少數維護人員的專案。

此外，[我們推薦專案的一般準則](about/criteria.md) 仍然適用。 **請注意我們和所推薦的服務商沒有任何利害關係。**
