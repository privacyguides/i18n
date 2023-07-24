---
title: "Qubes概述"
icon: simple/qubesos
description: Qubes 作業系統利用虛擬機器來隔離應用程式以提高安全性。
---

[**Qubes OS**](../desktop.md#qubes-os) 為開源作業系統，其使用 [Xen](https://en.wikipedia.org/wiki/Xen) 管理程序利用隔離虛擬機器來為桌面運算提供強固的安全。 每個虛擬機器被稱為 *Qube* ，可以根據其目的為各個Qube 分配信任等級。 因為 Qubes OS 使用隔離方式的安全措施，授權行為皆以個別案例為準，此正與[badness enumeration](https://www.ranum.com/security/computer_security/editorials/dumb/)壞處枚舉相反。

## Qubes OS如何工作？

Qubes 使用 [分區化](https://www.qubes-os.org/intro/) 來確保系統安全。 Qubes 從模板創建，預設為 Fedora、Debian 和 [Whonix](../desktop.md#whonix)。 Qubes OS還允許您創建一次性 [一次性](https://www.qubes-os.org/doc/how-to-use-disposables/) 虛擬機器。

![Qubes架構](../assets/img/qubes/qubes-trust-level-architecture.png)
<figcaption>Qubes Architecture, Credit: What is Qubes OS Intro</figcaption>

每個Qubes應用程序都有 [顏色邊框](https://www.qubes-os.org/screenshots/) ，幫助您追蹤它所運行的虛擬機器。 例如，可以為銀行瀏覽器使用特定的顏色，而一般不信任的瀏覽器則使用不同顏色。

![顏色邊框](../assets/img/qubes/r4.0-xfce-three-domains-at-work.png)
<figcaption>Qubes 視窗邊框，圖片來源： Qubes Screenshots</figcaption>

## 我爲什麼要使用Qubes ？

如果您的 [威脅模型](../basics/threat-modeling.md) 需要強大的分區和安全性，例如認為需要從不信任的來源開啟可疑檔案， Qubes OS 非常有用。 使用 Qubes OS 的某種典型原因是打開來自不明來源的文件。

Qubes OS 利用 [DOM0](https://wiki.xenproject.org/wiki/Dom0) Xen VM （即「AdminVM」）來控制主機作業系統上其他訪客的 VM 或 Qubes。 其他VM 在 Dom0 桌面環境中顯示個別的應用程式視窗。 您可以根據信任等級為代碼窗口上色，並透過非常細膩的控制來執行應用程式。

### 復制和黏貼文本

可利用 `qvm-copy-to-vm` 或以下說明 [複製並貼上文本](https://www.qubes-os.org/doc/how-to-copy-and-paste-text/) ：

1. 按 **Ctrl + C**  讓 VM 複製某些內容。
2. 按 **Ctrl + Shift + C** 讓 VM 將此緩衝區供全局剪貼板使用。
3. 在目標 VM 中按 **Ctrl + Shift + V** 以使全局剪貼簿可用。
4. 在目標 VM 中按 **Ctrl + V** 將內容粘貼到緩衝區中。

### 檔案交換

若要將檔案和目錄(資料夾)從一個 VM 複製貼到另一個 VM ，您可以使用選項 **Copy to Other AppVM...** 或 **Move to Other AppVM...**。 不同之處在於 **Move** 選項會刪除原始檔案。 這兩個選項都可以保護您的剪貼簿不會洩漏到任何其他 Qubes。 這比網閘式檔案傳輸更安全，因為網閘電腦仍將被迫解析分割區或檔案系統。 這在inter-qube複製系統中是不需要的。

??? info "AppVms沒有自己的檔案系統"

    您可以在Qubes之間[複製和移動檔案](https://www.qubes-os.org/doc/how-to-copy-and-move-files/)。 當這樣做時，不會立即進行更改，並且在發生事故時可以輕鬆撤消。

### 虛擬機之間交互

[qrexec 框架](https://www.qubes-os.org/doc/qrexec/) 是 Qubes 的核心構成，讓虛擬機器在域之間溝通。 它基於 Xen 庫 *vchan*之上，通過策略</a>促進
隔離。</p> 



## 其他資源

如需更多資訊，建議瀏覽[Qubes OS 網站](https://www.qubes-os.org/doc/)上 Qubes OS 文件頁面。 可以從Qubes OS [文件庫](https://github.com/QubesOS/qubes-doc)下載離線副本。

- Open Technology Fund: [*Arguably the world's most secure operating system*](https://www.opentech.fund/news/qubes-os-arguably-the-worlds-most-secure-operating-system-motherboard/)
- J. Rutkowska: [*Software compartmentalization vs. physical separation*](https://invisiblethingslab.com/resources/2014/Software_compartmentalization_vs_physical_separation.pdf)
- J. Rutkowska: [*Partitioning my digital life into security domains*](https://blog.invisiblethings.org/2011/03/13/partitioning-my-digital-life-into.html)
- Qubes OS: [*相關文章*](https://www.qubes-os.org/news/categories/#articles)
