---
title: "Qubes概述"
icon: simple/qubesos
description: Qubes 作業系統利用*qubes* (過去稱"虛擬機器") 來隔離應用程式以提高安全性。
---

[**Qubes OS**](../desktop.md#qubes-os) 為開源作業系統，其使用 [Xen](https://en.wikipedia.org/wiki/Xen) 管理程序利用 隔離*qubes*(虛擬器)來為桌面運算提供強固的安全。 您可為每一個 *qube* 依其目的指定不同的信賴層級。 Qubes OS 利用隔離作法來提高安全性。 It only permits actions on a per-case basis and therefore is the opposite of [badness enumeration](https://ranum.com/security/computer_security/editorials/dumb).

## Qubes OS如何工作？

Qubes uses [compartmentalization](https://qubes-os.org/intro) to keep the system secure. Qubes 從模板創建，預設為 Fedora、Debian 和 [Whonix](../desktop.md#whonix)。 Qubes OS also allows you to create once-use [disposable](https://qubes-os.org/doc/how-to-use-disposables) *qubes*.

<details class="note" markdown>
<summary>The term <em>qubes</em> is gradually being updated to avoid referring to them as "virtual machines".</summary>

由於“appVM”一辭更改為“qube”，此處和 Qubes OS 文檔中的一些資訊可能在語言上產生衝突。 Qube 不是完整的虛擬器，但有與 VM 類似的功能。

</details>

![Qubes架構](../assets/img/qubes/qubes-trust-level-architecture.png)
<figcaption>Qubes Architecture, Credit: What is Qubes OS Intro</figcaption>

Each qube has a [colored border](https://qubes-os.org/screenshots) that can help you keep track of the domain in which it runs. 例如，可以為銀行瀏覽器使用特定的顏色，而一般不信任的瀏覽器則使用不同顏色。

![顏色邊框](../assets/img/qubes/r4.0-xfce-three-domains-at-work.png)
<figcaption>Qubes 視窗邊框，圖片來源： Qubes Screenshots</figcaption>

## 我爲什麼要使用Qubes ？

如果您的 [威脅模型](../basics/threat-modeling.md) 需要強大的安全與隔離，例如認為需要從不信任的來源開啟可疑檔案， Qubes OS 非常有用。 使用 Qubes 作業系統的典型原因是打開不明來源的文檔，其考量是如果單個 qube 受到損害，也不會影響系統的其餘部分。

Qubes OS在主機作業系統上 利用 [dom0](https://wiki.xenproject.org/wiki/Dom0) Xen VM 來控制其他 *qubes* ，這些都在 dom0 的桌面環境中顯示個別的應用程式視窗。 這種類型的架構有很多用途。 以下是您可以執行的一些任務。 您可以看到通過合併多個步驟可以使過程更加安全。

### 復制和黏貼文本

You can [copy and paste text](https://qubes-os.org/doc/how-to-copy-and-paste-text) using `qvm-copy-to-vm` or the below instructions:

1. 按 **Ctrl + C** 讓所在的 *qube* 複製某些內容。
2. 按 **Ctrl + Shift + C** 讓 *qube* 將此緩衝區供全局剪貼板使用。
3. 在指定*qube* 下按 **Ctrl + Shift + V** 以使全局剪貼簿可用。
4. 在目標*qube* 中按 **Ctrl + V** 將內容粘貼到緩衝區中。

### 檔案交換

若要將檔案和目錄(資料夾) 從一個*qube* 複製貼到另一個 ，您可以使用選項 **Copy to Other AppVM...** 或 **Move to Other AppVM...**。 不同之處在於 **Move** 選項會刪除原始檔案。 這兩個選項都可以保護您的剪貼簿不會洩漏到任何其他*qube* 。 這比氣隙檔案傳輸更安全。 氣隙電腦仍會被迫解析分區或檔案系統。 這在inter-qube複製系統中是不需要的。

<details class="note" markdown>
<summary>Qubes do not have their own filesystems.</summary>

You can [copy and move files](https://qubes-os.org/doc/how-to-copy-and-move-files) between *qubes*. 當這樣做時，不會立即進行更改，並且在發生事故時可以輕鬆撤消。 When you run a *qube*, it does not have a persistent filesystem. 您可以創建和刪除檔案，但這些更改是暫時的。

</details>

### 虛擬機之間交互

The [qrexec framework](https://qubes-os.org/doc/qrexec) is a core part of Qubes which allows communication between domains. It is built on top of the Xen library *vchan*, which facilitates [isolation through policies](https://qubes-os.org/news/2020/06/22/new-qrexec-policy-system).

## 透過 VPN 連接 Tor

[建議](../advanced/tor-overview.md) 使用 [VPN](../vpn.md) 來連接 Tor 網絡，Qubes 可以很輕鬆地結合 ProxyVMs 與 Whonix 來操作。

[建立新的 ProxyVM](https://github.com/Qubes-Community/Contents/blob/master/docs/configuration/vpn.md) 後再連接到所選的 VPN，可**先將** Whonix qubes 串接至 ProxyVM 再連上 Tor 網絡，其用法是設置Whonix 所建立的 NetVM **Gateway** (`sys-whonix`) 。

Qubes 設置大概像這樣：

| Qube 名稱         | Qube 簡述                                                                                              | NetVM           |
| --------------- | ---------------------------------------------------------------------------------------------------- | --------------- |
| sys-net         | *預設的網路 qube (已預先安裝)*                                                                                 | *n/a*           |
| sys-firewall    | *預設的防火牆 qube (已預先安裝)*                                                                                | sys-net         |
| ==sys-proxyvm== | [建立的 VPN ProxyVM](https://github.com/Qubes-Community/Contents/blob/master/docs/configuration/vpn.md) | sys-firewall    |
| sys-whonix      | Whonix Gateway VM                                                                                    | ==sys-proxyvm== |
| anon-whonix     | Whonix Workstation VM                                                                                | sys-whonix      |

## 其他資源

For additional information we encourage you to consult the extensive Qubes OS documentation pages located on the [Qubes OS Website](https://qubes-os.org/doc). 可以從Qubes OS [文件庫](https://github.com/QubesOS/qubes-doc)下載離線副本。

- [Arguably the world's most secure operating system](https://opentech.fund/news/qubes-os-arguably-the-worlds-most-secure-operating-system-motherboard) (Open Technology Fund)
- [Software compartmentalization vs. physical separation](https://invisiblethingslab.com/resources/2014/Software_compartmentalization_vs_physical_separation.pdf) (J. Rutkowska)
- [Partitioning my digital life into security domains](https://blog.invisiblethings.org/2011/03/13/partitioning-my-digital-life-into.html) (J. Rutkowska)
- [Related Articles](https://qubes-os.org/news/categories/#articles) (Qubes OS)
