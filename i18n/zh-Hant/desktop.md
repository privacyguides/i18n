---
title: "桌上型電腦"
icon: simple/linux
description: 基於隱私保護和軟體自由，通常建議用 Linux 發行版。
cover: desktop.webp
---

<small>防護下列威脅：</small>

- [:material-account-cash: 監控資本主義](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}

基於隱私保護和軟體自由，通常建議用 Linux 發行版。 如果您還不曾用過 Linux ，以下是我們建議可試試的發行版，以及一些 Linux發行版的隱私和安全提升技巧。

- [一般Linux 概述 :material-arrow-right-drop-circle:](os/linux-overview.md)

## 傳統發行版

### Fedora Linux

<div class="admonition recommendation" markdown>

![Fedora logo](assets/img/linux-desktop/fedora.svg){ align=right }

**Fedora Linux** is our recommended desktop distribution for people new to Linux. Fedora 通常會比其他發行版先採用較新的技術 (例如 [Wayland](https://wayland.freedesktop.org) 和 [PipeWire](https://pipewire.org))。 這些新技術通常會在安全性、隱私性和可用性方面有所改善。

[:octicons-home-16: Homepage](https://fedoraproject.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.fedoraproject.org/en-US/docs){ .card-link title=Documentation}
[:octicons-heart-16:](https://whatcanidoforfedora.org){ .card-link title=Contribute }

</details>

</div>

Fedora comes in two primary desktop editions, [Fedora Workstation](https://fedoraproject.org/workstation), which uses the GNOME desktop environment, and [Fedora KDE Plasma Desktop](https://fedoraproject.org/kde), which uses KDE. Historically, Fedora Workstation has been more popular and widely recommended, but KDE has been gaining in popularity and provides an experience more similar to Windows, which may make transitioning to Linux easier for some. The security and privacy benefits of both editions are very similar, so it mostly comes down to personal preference.

Fedora 有一個半滾動的發布週期。 While some packages like the desktop environment are frozen until the next Fedora release, most packages (including the kernel) are updated frequently throughout the lifespan of the release. 每個 Fedora 版本支持一年，每6個月發布新版本。

### openSUSE Tumbleweed

<div class="admonition recommendation" markdown>

![openSUSE Tumbleweed logo](assets/img/linux-desktop/opensuse-tumbleweed.svg){ align=right }

**openSUSE Tumbleweed** 是一個穩定滾動發行版。

openSUSE Tumbleweed 使用 [Btrfs](https://zh.wikipedia.org/wiki/Btrfs) 和 [Snapper](https://zh.opensuse.org/openSUSE:Snapper_Tutorial) 以確保一旦發生問題，快照可以回滾。

[:octicons-home-16: 首頁](https://get.opensuse.org/tumbleweed){ .md-button .md-button--primary }
[:octicons-info-16:](https://doc.opensuse.org){ .card-link title=說明文件}
[:octicons-heart-16:](https://shop.opensuse.org){ .card-link title=捐款 }

</details>

</div>

Tumbleweed 遵循滾動發佈模式，每個更新都是快照發布。 當您升級系統時，會下載新的快照。 每個快照都會由 [openQA](https://openqa.opensuse.org) 執行一系列自動化測試，以確保其品質。

### Arch Linux

<div class="admonition recommendation" markdown>

![Arch logo](assets/img/linux-desktop/archlinux.svg){ align=right }

**Arch Linux** 是一個輕量級、自助式 (DIY) 的發行版，也就是說，您只會得到您所安裝的東西。 如需更多資訊，請參閱他們的 [FAQ](https://wiki.archlinux.org/title/Frequently_asked_questions)。

[:octicons-home-16: 首頁](https://archlinux.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://wiki.archlinux.org){ .card-link title=說明文件}
[:octicons-heart-16:](https://archlinux.org/donate){ .card-link title=捐款 }

</details>

</div>

Arch Linux有一個滾動發佈週期。 沒有固定的發布時間表，套件經常更新。

作為 DIY 發行版，用戶需要 [自行設定與維護](os/linux-overview.md#arch-based-distributions) 系統。 Arch有一個 [官方安裝程式](https://wiki.archlinux.org/title/Archinstall) ，使安裝過程更容易。

[Arch Linux 的套件](https://reproducible.archlinux.org) 大部份都是 [可重現的](https://reproducible-builds.org)[^1]。

## 原子化發行版

**原子化發行版** （有時也稱為 **不可變發行版** ）是透過在核心系統映像上分層變更，而非直接修改系統來處理套件安裝與更新的作業系統。 原子化發行版的優點包括增加穩定性，並能輕易回滾更新。 詳細請見 [*傳統 vs. 原子化 更新*](os/linux-overview.md#traditional-vs-atomic-updates) 以更深入了解。

### Fedora Atomic Desktops

<div class="admonition recommendation" markdown>

![Fedora logo](assets/img/linux-desktop/fedora.svg){ align=right }

**Fedora Atomic Desktops** 是 Fedora 的變體，它使用「rpm-ostree」套件管理器，專注於容器化工作流程和桌面應用程式的 Flatpak。 這些變體版都遵循 Fedora Workstation 同樣的發佈時間表，受益於相同的快速更新並保持非常接近上遊。

[:octicons-home-16: Homepage](https://fedoraproject.org/atomic-desktops){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.fedoraproject.org/en-US/emerging){ .card-link title=Documentation}
[:octicons-heart-16:](https://whatcanidoforfedora.org){ .card-link title=Contribute }

</details>

</div>

[Fedora Atomic Desktops](https://fedoramagazine.org/introducing-fedora-atomic-desktops) 有多種風格，視您偏好的桌面環境而定。 就像我們在 Linux 發行版本的 [標準](#criteria) 中建議避免 X11 一樣，我們建議避免只支援傳統 X11 視窗系統的版本。

These operating systems differ from Fedora Workstation as they replace the [DNF](https://docs.fedoraproject.org/en-US/quick-docs/dnf) package manager with a much more advanced alternative called [`rpm-ostree`](https://coreos.github.io/rpm-ostree). `rpm-ostree` 套件管理器的工作原理是下載系統的基本映像，然後將套件覆蓋在類似 [git](https://en.wikipedia.org/wiki/Git)的提交樹中。 當系統更新時，會下載新的基本影像，並將疊加層應用於該新影像。

更新完成後，您將重新啟動系統進入新的布署。 `rpm-ostree` 會保留系統的兩個布署，以便在新布署出現問題時，可以輕鬆地回退。 此外，還可根據需要釘選更多布署。

[Flatpak](https://flatpak.org) is the primary package installation method on these distributions, as `rpm-ostree` is only meant to overlay packages that cannot stay inside a container on top of the base image.

作為 Flatpaks 的替代方案，您可以選擇 [Toolbx](https://docs.fedoraproject.org/en-US/fedora-silverblue/toolbox) 來建立 [Podman](https://podman.io) 容器，模仿傳統的 Fedora 環境，對於眼光獨到的開發人員而言，這是 [非常有用的功能](https://containertoolbx.org) 。 這些容器與主機作業系統共用一個主目錄。

### NixOS

<div class="admonition recommendation" markdown>

![NixOS logo](assets/img/linux-desktop/nixos.svg){ align=right }

NixOS 是基於 Nix套件管理器的獨立發行版，專注於可重複性和可靠性。

[:octicons-home-16: 首頁](https://nixos.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://nixos.org/learn.html){ .card-link title=說明文件}
[:octicons-heart-16:](https://nixos.org/donate.html){ .card-link title=捐款 }

</details>

</div>

NixOS’ 套件管理器 將各個套件版本儲存在 **Nix store** 底下不同的資料夾。 因此，您可以在系統上安裝相同套件的不同版本。 套件內容寫入資料夾後，該資料夾會變成唯讀。

NixOS 也提供原子化更新。 它會先下載（或建立）新世代系統的套件和檔案，然後再切換到新系統。 There are different ways to switch to a new generation: you can tell NixOS to activate it after reboot, or you can switch to it at runtime. 也可以在運行時就切換到新世代系統來 *測試* ，但不將它設成當前系統。 如果更新過程中遭到打斷，可以重新啟動並自動返回到系統的工作版本。

Nix 套件管理員使用純函數式程式設計語言（稱為 Nix ）來定義套件。

[Nixpkgs](https://github.com/nixos/nixpkgs) （套件的主要來源）包含在單一的 GitHub 儲存庫中。 您也可以用相同的語言定義自己的套件，然後輕鬆地將它們包含在您的配置中。

Nix是一個基於源的套件管理器；如果二進位快取中沒有預先構建的可用性， Nix 只會使用其定義從源構建套件。 它在盡可能獨立於主機系統的沙盒 *純淨*環境（pure environment，此處因找不到資料而直翻）中建立每個套件。 使用此方法建立的二進位檔是可重現的[^1]。

## 以匿名爲重點的發行版

### Whonix

<div class="admonition recommendation" markdown>

![Whonix logo](assets/img/linux-desktop/whonix.svg){ align=right }

**Whonix** 為基於 [Kicksecure](#kicksecure) 專注在安全的 Debian 分支系統。 其目的是在網際網路上提供隱私、安全性和 [:material-incognito: 匿名](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple }。 Whonix 最好與 [Qubes OS](#qubes-os) 配合使用。

[:octicons-home-16: 首頁](https://whonix.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://dds6qkxpwdeubwucdiaord2xgbbeyds25rbsgr73tbfpqpt4a6vjwsyd.onion){ .card-link title="洋蔥服務" }
[:octicons-info-16:](https://whonix.org/wiki/Documentation){ .card-link title=說明文件}
[:octicons-heart-16:](https://whonix.org/wiki/Donate){ .card-link title=捐款 }

</details>

</div>

Whonix 運行兩個虛擬機器：一個“工作站”和一個 Tor “閘道”。 來自工作站的所有通訊都必須通過 Tor 閘道。 這意味著，即使工作站受到某種惡意軟體的破壞，真實的 IP 位址仍然隱藏。

它的功能包括Tor 串流隔離、[擊鍵匿名](https://www.whonix.org/wiki/Keyrinkle_Deanonymization#Kloak)、[加密交換](https://github. com /Whonix/swap-file-creator)，以及強化的記憶體分配器。 Whonix 未來的版本可能會包含 [完整的系統 AppArmor 策略](https://github.com/roddhjav/apparmor.d) 和 [沙盒化應用程式啟動器](https://whonix.org/wiki/Sandbox-app-launcher) ，以完全限制系統上的所有程序。

Whonix 最好 [與 Qubes 結合使用](https://whonix.org/wiki/Qubes/Why_use_Qubes_over_other_Virtualizers)。 我們有一份 [建議指南](os/qubes-overview.md#connecting-to-tor-via-a-vpn) ，說明如何結合 Qubes 中的 VPN ProxyVM 來設定 Whonix，以向 ISP 隱藏您正在使用 Tor。

### Tails

<div class="admonition recommendation" markdown>

![Tails logo](assets/img/linux-desktop/tails.svg){ align=right }

**Tails** 是一個基於Debian 的自生作業系統，通過 Tor 路由所有通訊，透過 DVD ， USB記憶棒或 SD卡安裝幾乎可在任何電腦上啟動。 它使用 [Tor](tor.md) 來維護 隱私 和 [:material-incognito: 匿名](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple } ，同時規避審查，而且在關閉電源後，它不會在使用的電腦上留下任何痕跡。

[:octicons-home-16: 首頁](https://tails.net){ .md-button .md-button--primary }
[:octicons-info-16:](https://tails.net/doc/index.en.html){ .card-link title=說明文件}
[:octicons-heart-16:](https://tails.net/donate){ .card-link title=捐款 }

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

Tails 關閉後 [不會抹除](https://gitlab.tails.boum.org/tails/tails/-/issues/5356) [視訊記憶體](https://en.wikipedia.org/wiki/Dual- ported_video_RAM) 。 使用 Tails 後重新啟動電腦時，電腦可能會短暫顯示之前 Tails 最後一個畫面。 如果是關閉電腦而不是重新啟動，則影像記憶會在斷電一段時間後自動擦除。

</div>

由於失憶功能(意指沒有寫入磁碟)，Tails 非常適合對抗資料探集；然而，它不像 Whonix 那樣是安全加固發行版。 它缺乏 Whonix 的許多匿名和安全功能，並且更新頻率較低（每六周一次）。 被惡意軟體入侵的 Tails 系統可能會繞過透明代理，讓使用者被去匿名化。

Tails Tor 瀏覽器預設包含 [uBlock Origin](browser-extensions.md#ublock-origin) ，這可能會使對手更容易透過指紋識別 Tails 用戶。 [Whonix](desktop.md#whonix) 虛擬機器可能更能防止洩漏，但它沒有失憶功能，因此資料可以從儲存設備上進行恢復。

設計上， Tails 每次重新啟動意謂著完全重置。 加密的 [持久性儲存空間](https://tails.net/doc/persistent_storage/index.en.html) 可設定用以在重新開機之間儲存某些資料。

## 以安全爲重點的發行版

<small>防護下列威脅：</small>

- [:material-bug-outline: 被動攻擊](basics/common-threats.md#security-and-privacy ""){.pg-orange}

### Qubes OS

<div class="admonition recommendation" markdown>

![Qubes OS logo](assets/img/qubes/qubes_os.svg){ align=right }

**Qubes OS** 是開源作業系統，利用安全的虛擬器為桌面運算提供更強的安全性 (或稱"qubes"). Qubes 基於 Xen, X Window 系統與 Linux。 大多數 Linux 應用它都可以執行且適用 Linux 驅動。

[:octicons-home-16: 首頁](https://qubes-os.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://qubesosfasa4zl44o4tws22di6kepyzfeqv3tg4e3ztknltfxqrymdad.onion){ .card-link title="洋蔥服務" }
[:octicons-eye-16:](https://qubes-os.org/privacy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://qubes-os.org/doc){ .card-link title=說明文件 }
[:octicons-code-16:](https://github.com/QubesOS){ .card-link title="原始碼" }
[:octicons-heart-16:](https://qubes-os.org/donate){ .card-link title=捐款 }

</details>

</div>

Qubes OS 作業系統將子系統（例如網路、USB等）和應用程式隔離在個別的 *qubes* 以保護電腦。 如果系統的某個部分遭受 [:material-target-account: 針對性攻擊](basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red} ，額外的隔離可能會保護其他的 *qubes* 和核心系統。

有關 Oubes 運作的進一步資訊，請參考我們完整的 [Qubes OS 介紹](os/qubes-overview.md) 頁面。

### Secureblue

<div class="admonition recommendation" markdown>

![Secureblue logo](assets/img/linux-desktop/secureblue.svg){ align=right }

**Secureblue** is a security-focused operating system based on [Fedora Atomic Desktops](#fedora-atomic-desktops). It includes a number of [security features](https://secureblue.dev/features) intended to proactively defend against the exploitation of both known and unknown vulnerabilities, and ships with [Trivalent](https://github.com/secureblue/Trivalent), their hardened, Chromium-based web browser.

[:octicons-home-16: Homepage](https://secureblue.dev){ .md-button .md-button--primary }
[:octicons-info-16:](https://secureblue.dev/install){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/secureblue/secureblue){ .card-link title="Source Code" }
[:octicons-heart-16:](https://secureblue.dev/donate){ .card-link title="Contribute" }

</div>

**Trivalent** is Secureblue's hardened Chromium for desktop Linux inspired by [GrapheneOS](android/distributions.md#grapheneos)'s Vanadium browser.

Secureblue also provides GrapheneOS's [hardened memory allocator](https://github.com/GrapheneOS/hardened_malloc) and enables it globally (including for Flatpaks).

### Kicksecure

雖然我們 [建議](os/linux-overview.md#release-cycle) 在大多數情況下不要將 Debian 等「永遠過時」的發行版用於桌上型電腦，但 Kicksecure 是一個以 Debian 為基礎的作業系統，它已添加遠超過一般 Linux 安裝的安全加固。

<div class="admonition recommendation" markdown>

![Kicksecure logo](assets/img/linux-desktop/kicksecure.svg){ align=right }

**Kicksecure** ──如要簡單的介紹它：可以說是一組腳本、配置與套件的組合；可大幅減少 Debian 的攻擊面。 它預設涵蓋了大量隱私和加固建議。 它也是 [Whonix](#whonix) 的基礎作業系統。

[:octicons-home-16: 首頁](https://kicksecure.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://kicksecure.com/wiki/Privacy_Policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://kicksecure.com/wiki/Documentation){ .card-link title=說明文件 }
[:octicons-code-16:](https://github.com/Kicksecure){ .card-link title="原始碼" }
[:octicons-heart-16:](https://kicksecure.com/wiki/Donate){ .card-link title=捐款 }

</details>

</div>

## 標準

選擇適合您的 Linux 發行版取決於個人喜好差異，本頁**並非**是每一款發行版的詳盡列表。 我們在 Linux 介紹頁有更詳細的 [如何選擇發行版本](os/linux-overview.md#choosing-your-distribution) 的說明。 *這個*頁面上的發行版通常都遵循我們介紹的指南，且都滿足以下標準：

- 免費且開放原始碼。
- 必須定期接收軟體和內核更新。
- 避免使用 X11，因為它最新的主要版本發布時間已久達 [十多年](https://x.org/wiki/Releases) 。
    - 值得注意的例外是 Qubes，虛擬化避免了 X11 通常會遇到的 [隔離問題](https://blog.invisiblethings.org/2011/04/23/linux-security-circus-on-gui-isolation) 。 此隔離僅適用於 *在不同 qubes 中執行*（虛擬機器）的應用程式；在 *相同* qube 中執行的應用程式無法受到保護。
- 安裝時必須支援全磁碟加密。
- 不可將定期更新發佈凍結超過1年。
    - 我們 [不建議](os/linux-overview.md#release-cycle) 桌機使用“長期支援”或“穩定”發行版。
- 每個 Fedora 版本支援一年，每6個月發布新版本。
- 偏好較大型的專案。
    - 維護作業系統是一項大挑戰，小型專案往往會犯更多可避免的錯誤，或延遲重大更新（或更糟糕的是，很快就完全消失）。 我們傾向於至少可維持10 年的專案（無論是由於公司支持還是非常重要的社區支持），而不是手工構建或只有少數維護人員的專案。

此外，[我們推薦專案的一般準則](about/criteria.md) 仍然適用。 **請注意，我們與推薦的任何項目均無關。**

[^1]: Reproducibility entails the ability to verify that packages and binaries made available to the end user match the source code, which can be useful against potential [:material-package-variant-closed-remove: Supply Chain Attacks](basics/common-threats.md#attacks-against-certain-organizations ""){.pg-viridian}.
