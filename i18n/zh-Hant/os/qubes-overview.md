---
title: "Qubes概述"
icon: simple/qubesos
description: Qubes 作業系統利用*qubes* (過去稱"虛擬機器") 來隔離應用程式以提高安全性。
---

[**Qubes OS**](../desktop.md#qubes-os) 為開源作業系統，其使用 [Xen](https://en.wikipedia.org/wiki/Xen) 管理程序利用 隔離*qubes*(虛擬器)來為桌面運算提供強固的安全。 您可為每一個 *qube* 依其目的指定不同的信賴層級。 Qubes OS 利用隔離作法來提高安全性。 它只允許根據具體情況進行操作，因此與[不良枚舉](https://www.ranum.com/security/computer_security/editorials/dumb/)相反。

## Qubes OS如何工作？

Qubes 使用 [分區化](https://www.qubes-os.org/intro/) 來確保系統安全。 Qubes 從模板創建，預設為 Fedora、Debian 和 [Whonix](../desktop.md#whonix)。 Qubes OS還允許您創建一次性 [一次性](https://www.qubes-os.org/doc/how-to-use-disposables/) *qubes*。

??? 更新改用“*qubes*一辭，避免將它們稱為“虛擬器”。

    由於“appVM”一辭更改為“qube”，此處和 Qubes OS 文檔中的一些資訊可能在語言上產生衝突。 Qube 不是完整的虛擬器，但有與 VM 類似的功能。

![Qubes架構](../assets/img/qubes/qubes-trust-level-architecture.png)
<figcaption>Qubes Architecture, Credit: What is Qubes OS Intro</figcaption>

每個 qubes 都有 [顏色邊框](https://www.qubes-os.org/screenshots/) ，幫助您追蹤它運行的地方。 例如，可以為銀行瀏覽器使用特定的顏色，而一般不信任的瀏覽器則使用不同顏色。

![顏色邊框](../assets/img/qubes/r4.0-xfce-three-domains-at-work.png)
<figcaption>Qubes 視窗邊框，圖片來源： Qubes Screenshots</figcaption>

## 我爲什麼要使用Qubes ？

如果您的 [威脅模型](../basics/threat-modeling.md) 需要強大的安全與隔離，例如認為需要從不信任的來源開啟可疑檔案， Qubes OS 非常有用。 使用 Qubes 作業系統的典型原因是打開不明來源的文檔，其考量是如果單個 qube 受到損害，也不會影響系統的其餘部分。

Qubes OS在主機作業系統上 利用 [dom0](https://wiki.xenproject.org/wiki/Dom0) Xen VM 來控制其他 *qubes* ，這些都在 dom0 的桌面環境中顯示個別的應用程式視窗。 這種類型的架構有很多用途。 以下是您可以執行的一些任務。 您可以看到通過合併多個步驟可以使過程更加安全。

### 復制和黏貼文本

可利用 `qvm-copy-to-vm` 或以下說明 [複製並貼上文本](https://www.qubes-os.org/doc/how-to-copy-and-paste-text/) ：

1. 按 **Ctrl + C** 讓所在的 *qube* 複製某些內容。
2. 按 **Ctrl + Shift + C** 讓 *qube* 將此緩衝區供全局剪貼板使用。
3. 在指定*qube* 下按 **Ctrl + Shift + V** 以使全局剪貼簿可用。
4. 在目標*qube* 中按 **Ctrl + V** 將內容粘貼到緩衝區中。

### 檔案交換

若要將檔案和目錄(資料夾) 從一個*qube* 複製貼到另一個 ，您可以使用選項 **Copy to Other AppVM...** 或 **Move to Other AppVM...**。 不同之處在於 **Move** 選項會刪除原始檔案。 這兩個選項都可以保護您的剪貼簿不會洩漏到任何其他*qube* 。 這比氣隙檔案傳輸更安全。 氣隙電腦仍會被迫解析分區或檔案系統。 這在inter-qube複製系統中是不需要的。

??? *Qube* 沒有自己的檔案系統。

    您可以在 qubes之間[複製和移動檔案](https://www.qubes-os.org/doc/how-to-copy-and-move-files/)。 當這樣做時，不會立即進行更改，並且在發生事故時可以輕鬆撤消。 當您運行 *qube* 時，它沒有持久檔案系統。 您可以創建和刪除檔案，但這些更改是暫時的。

### 虛擬機之間交互

[qrexec 框架](https://www.qubes-os.org/doc/qrexec/) 是 Qubes 的核心構成，其可在域之間進行溝通。 它基於 Xen 庫 *vchan*之上，通過策略</a>促進
隔離。</p> 



## Connecting to Tor via a VPN

We [recommend](../advanced/tor-overview.md) connecting to the Tor network via a [VPN](../vpn.md) provider, and luckily Qubes makes this easy to do with a combination of ProxyVMs and Whonix.

After [creating a new ProxyVM](https://github.com/Qubes-Community/Contents/blob/master/docs/configuration/vpn.md) which connects to the VPN of your choice, you can chain your Whonix qubes to that ProxyVM **before** they connect to the Tor network, by setting the NetVM of your Whonix **Gateway** (`sys-whonix`) to the newly-created ProxyVM.

Your qubes should be configured in a manner similar to this:

| Qube name       | Qube description                                                                                                 | NetVM           |
| --------------- | ---------------------------------------------------------------------------------------------------------------- | --------------- |
| sys-net         | *Your default network qube (pre-installed)*                                                                      | *n/a*           |
| sys-firewall    | *Your default firewall qube (pre-installed)*                                                                     | sys-net         |
| ==sys-proxyvm== | The VPN ProxyVM you [created](https://github.com/Qubes-Community/Contents/blob/master/docs/configuration/vpn.md) | sys-firewall    |
| sys-whonix      | Your Whonix Gateway VM                                                                                           | ==sys-proxyvm== |
| anon-whonix     | Your Whonix Workstation VM                                                                                       | sys-whonix      |




## 其他資源

如需更多資訊，建議瀏覽[Qubes OS 網站](https://www.qubes-os.org/doc/)上 Qubes OS 文件頁面。 可以從Qubes OS [文件庫](https://github.com/QubesOS/qubes-doc)下載離線副本。

- [Arguably the world's most secure operating system](https://www.opentech.fund/news/qubes-os-arguably-the-worlds-most-secure-operating-system-motherboard/) (Open Technology Fund)
- [Software compartmentalization vs. physical separation](https://invisiblethingslab.com/resources/2014/Software_compartmentalization_vs_physical_separation.pdf) (J. Rutkowska)
- [Partitioning my digital life into security domains](https://blog.invisiblethings.org/2011/03/13/partitioning-my-digital-life-into.html) (J. Rutkowska)
- [相關文章](https://www.qubes-os.org/news/categories/#articles) (Qubes OS)
