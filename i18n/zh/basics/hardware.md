---
title: "选择硬件"
icon: 'material/chip'
description: 软件并不是唯一的关键所在；了解每天用来保护隐私的硬件工具。
---

在讨论隐私时，人们通常不像考虑使用的软件那样多地考虑硬件。应该将硬件视为构建其他隐私设置的基础。

## 挑选计算机

设备的内部组件处理并存储你所有的数字数据。重要的是，所有设备都受到制造商和开发者的支持，能够持续接收安全更新。

### 硬件安全计划

有些设备会有“硬件安全计划”，即供应商之间在设计硬件时的最佳实践和建议方面的合作，例如：

- [Windows 保护核心电脑](https://learn.microsoft.com/en-us/windows-hardware/design/device-experiences/oem-highly-secure-11)符合由微软指定的更高安全标准。这些保护不仅仅适用于Windows用户；其他操作系统的用户仍然可以利用[DMA 保护](https://learn.microsoft.com/en-us/windows/security/information-protection/kernel-dma-protection-for-thunderbolt)等功能，以及完全不信任微软证书的能力。
- [Android Ready SE](https://developers.google.com/android/security/android-ready-se)是供应商之间的合作，确保其设备遵循[最佳实践](https://source.android.com/docs/security/best-practices/hardware)，并包括用于加密密钥等内容的抗篡改硬件支持的存储。
- 在 Apple SoC 上运行的 macOS 利用了第三方操作系统可能无法提供的[硬件安全功能](../os/macos-overview.md#hardware-security)。
- [ChromeOS 安全性](https://chromium.org/chromium-os/developer-library/reference/security/security-whitepaper)在 Chromebook 上运行时处于最佳状态，因为它能够利用可用的硬件功能，例如[硬件信任根](https://chromium.org/chromium-os/developer-library/reference/security/security-whitepaper/#hardware-root-of-trust-and-verified-boot)。

即使你不使用这些操作系统，参与这些计划也可能表明制造商在硬件安全和更新方面遵循了最佳实践。

### 预装操作系统

除非你购买Mac或专门的Linux计算机，否则新电脑几乎总是预装了Windows。通常最好是擦除驱动器并全新安装你选择的操作系统，即使这意味着从头开始重新安装Windows。由于硬件供应商与可疑软件供应商之间的协议，默认的Windows安装通常预装了臃肿软件、[广告软件](https://bleepingcomputer.com/news/technology/lenovo-gets-a-slap-on-the-wrist-for-superfish-adware-scandal)甚至[恶意软件](https://zdnet.com/article/dell-poweredge-motherboards-ship-with-malware)。

### 固件更新

硬件通常存在安全问题，这些问题会被发现并通过你的硬件的固件更新进行修补。

从主板到存储设备，你的计算机的几乎每个组件都需要固件才能运行。理想情况是设备的所有的组件都能得到完全支持。苹果设备、Chromebook、大多数Android手机和Microsoft Surface设备只要受支持，就会为你处理固件更新。

如果你自己组装电脑，你可能需要从OEM的网站下载并手动更新主板固件。如果你使用Linux，请考虑使用内置的 [`fwupd`](https://fwupd.org) 工具，该工具可以让你检查并应用主板可用的任何固件更新。

### TPM/安全加密处理器

大多数计算机和手机都配备了TPM（或类似的安全加密处理器），它可以安全地存储加密密钥并处理其他与安全相关的功能。如果你目前使用的计算机没有此功能，你可能会从购买具有此功能的较新计算机中受益。某些台式机和服务器主板有一个“TPM 接针”，可以接插包含TPM的小型附件板。

<div class="admonition Note" markdown>
<p class="admonition-title">注意</p>

虚拟 TPM 容易受到侧信道攻击，而由于外部 TPM 与主板上的 CPU 是分离的，因此当攻击者可以接触到硬件时，它们容易受到[嗅探攻击](https://pulsesecurity.co.nz/articles/TPM-sniffing)。解决此问题的方法是将安全处理器包含在 CPU 内部，苹果的芯片和微软的 [Pluton](https://microsoft.com/en-us/security/blog/2020/11/17/meet-the-microsoft-pluton-processor-the-security-chip-designed-for-the-future-of-windows-pcs) 就是如此。

</div>

### 生物特征识别

许多设备配备了指纹读取器或面部识别功能。这可能非常方便，但并不完美，有时会失效。大多数设备在发生这种情况时会回退到使用 PIN 或密码，这意味着设备的安全性仍然取决于密码的安全性。

生物特征识别可以防止他人偷看你输入密码，因此，如果肩窥是你的威胁模型的一部分，那么生物特征识别是一个不错的选择。

大多数面部认证的实现要求你注视手机，并且只能在相对较近的距离内工作，所以你不需要太担心有人在未经你同意的情况下将手机对准你的脸来解锁。如果需要，你仍然可以在手机锁定时禁用生物特征识别。在 iOS 上，在支持面容 ID 的机型上，你可以按住侧边按钮和音量按钮 3 秒钟来禁用面容 ID。在 Android 上，按住电源按钮并在菜单上按“锁定”。

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

有些设备没有用于安全面部认证的适当硬件。面部认证主要有两种类型：2D 和 3D。 3D 面部认证利用点阵投影仪，使设备能够创建你面部的 3D 深度图。请确保你的设备具有此功能。

</div>

Android为生物特征识别定义了三个[安全级别](https://source.android.com/docs/security/features/biometric/measure#biometric-classes)；在启用生物特征识别之前，应检查设备是否属于级别 3。

### 设备加密

如果你的设备已[加密](../encryption.md)，那么当设备完全关机（而不是仅仅休眠）时，即在你首次输入加密密钥或锁屏密码之前，你的数据是最安全的。在手机上，这种更高安全性的状态被称为“首次解锁前”（BFU），而在重启/开机后输入正确的密码后则称为“首次解锁后”（AFU）。与 BFU 相比，AFU 对抗数字取证工具包和其他漏洞利用的安全性要低得多。因此，如果你担心攻击者对你的设备进行物理接触，你应该在不使用时将其完全关机。

这可能不太实际，因此请考虑是否值得，但无论如何，如果你使用了强加密密钥，即使是 AFU 模式也能有效抵御大多数威胁。

## 外部硬件

有些威胁不能仅靠内部组件来防御。其中许多选项具有很强的局限性；请评估它们对于你的威胁模型是否真的必要。

### 硬件安全密钥

硬件密钥是使用强加密技术对设备或帐户进行身份验证的设备。核心理念是，由于它们不能被复制，你可以使用它们来保护帐户，只有在物理上拥有该密钥时才能访问，从而消除了许多远程攻击。

[推荐硬件密钥 :material-arrow-right-drop-circle:](../security-keys.md){ .md-button .md-button--primary } [详细了解硬件密钥 :material-arrow-right-drop-circle:](multi-factor-authentication.md#hardware-security-keys){ .md-button }

### 摄像头/麦克风

如果你不想信任操作系统的权限控制来阻止摄像头激活，你可以购买摄像头遮挡盖，从物理上阻止光线到达摄像头。你也可以购买一台没有内置摄像头的设备，并使用外接摄像头，用完后随时拔掉。一些设备配有内置摄像头遮挡盖或硬件开关，以物理方式断开摄像头的电源。

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

你只应购买适合你的笔记本电脑且在合上盖子时不会造成损坏的保护盖。遮挡摄像头会干扰自动亮度和面部认证功能。

</div>

对于麦克风的访问，在大多数情况下，你将需要信任操作系统内置的权限控制。或者，购买一台没有内置麦克风的设备，并使用外接麦克风，用完后可以拔掉。某些设备（如 [MacBook 或 iPad](https://support.apple.com/guide/security/hardware-microphone-disconnect-secbbd20b00b/web)）在你合上盖子时提供麦克风的硬件断开连接功能。

许多计算机的 BIOS 选项可以禁用摄像头和麦克风。在那里禁用时，该硬件甚至不会作为设备出现在启动的系统中。

### 隐私屏幕/防窥膜

防窥膜是一种可以贴在普通屏幕上的薄膜，使屏幕只能在特定角度可见。如果你的威胁模型包括他人偷看你的屏幕，这些是个不错的选择，但它并非万无一失，因为任何人只需转移到不同的视角就可以看到你的屏幕内容。

### 失能开关

失能开关会在没有操作员在场的情况下阻止机器运行。这些最初被设计为安全措施，但同样的概念也可应用于电子设备，在你不在场时将其锁定。

某些笔记本电脑能够[检测](https://support.microsoft.com/en-us/windows/managing-presence-sensing-settings-in-windows-11-82285c93-440c-4e15-9081-c9e38c1290bb)到你是否在场，并能在你不在屏幕前时自动锁定。你应该检查操作系统中的设置，以查看你的计算机是否支持此功能。

你还可以购买类似 [BusKill](https://buskill.in) 这样的线缆，当线缆断开连接时，它会锁定或擦除你的计算机。

### 反拦截/邪恶女佣攻击

在设备属于你之前，防止针对你的定向攻击的最好方法是在实体店购买设备，而不是将其订购到你的地址。

确保你的设备支持安全启动/验证启动，并且你已将其启用。尽可能避免让你的设备无人看管。

### 肯辛顿锁 (Kensington Locks)

许多笔记本电脑配备了[肯辛顿锁孔](https://www.kensington.com/solutions/product-category/security/?srsltid=AfmBOorQOlRnqRJOAqM-Mvl7wumed0wBdiOgktlvdidpMHNIvGfwj9VI)，你可以使用一条锁定在机器插槽中的**金属缆线**来保护你的设备。这些锁可以是密码锁或钥匙锁。

像所有锁具一样，肯辛顿锁容易受到[物理攻击](https://youtu.be/vgvCxL7dMJk)，因此你应主要使用它们来震慑小偷小摸。你可以使用桌腿或不容易移动的物品，在家里甚至在公共场合保护你的笔记本电脑。

## 保护网络安全

### 隔离

存在许多允许你分离计算机上的操作的解决方案，例如虚拟机和沙盒。然而，最好的隔离是物理分离。这对于某些软件要求你绕过操作系统中的安全功能的情况特别有用，例如许多游戏捆绑的反作弊软件。

对于游戏，指定一台机器作为你的“游戏机”并仅将其用于该任务可能会很有用。将其保留在单独的 VLAN 上。这可能需要使用支持隔离网络的管理型交换机和路由器。

大多数消费级路由器允许你通过启用一个无法与你的主网络通信的独立“访客”网络来实现此目的。所有不受信任的设备都可以放在这里，包括物联网设备，如智能冰箱、恒温器、电视等。

### 极简主义

俗话说，“少即是多”。连接到网络的设备越少，潜在的攻击面就越少，确保它们保持最新的工作量也就越少。

你可能会发现，在家里走一圈并列出你拥有的每个联网设备的清单，以帮助你保持跟踪，这很有用。

### 路由器

你的路由器处理你所有的网络流量，充当你与开放互联网之间的第一道防线。

<div class="admonition Note" markdown>
<p class="admonition-title">注意</p>

很多路由器都配有存储空间来存放你的文件，以便你可以从网络上的任何计算机访问它们。我们建议你不要将网络设备用于除网络以外的事情。如果你的路由器受到攻击，你的文件也将受到影响。

</div>

关于路由器，最重要的事情是保持它们是最新的。许多现代路由器会自动安装更新，但也有许多不会。你应该在路由器的设置页面检查这个选项。假设你在同一个网络上，通常可以通过在任何浏览器的 URL 栏中键入 `192.168.1.1` 或 `192.168.0.1` 来访问该页面。你也可以在操作系统的网络设置中查找“路由器”或“网关”。

如果你的路由器不支持自动更新，你需要去制造商的网站下载更新并手动应用它们。

许多消费级路由器的支持时间不是很长。如果制造商不再支持你的路由器，你可以检查它是否受[自由开源固件](../router.md)支持。你也可以购买默认安装了自由开源固件的路由器；这些路由器的支持时间往往比大多数路由器长。

某些互联网服务提供商（ISP）提供路由器/调制解调器二合一设备。为了安全起见，购买一台单独的路由器并将 ISP 的路由器/调制解调器设置为仅调制解调器模式会很有益处。这样，即使你的 ISP 提供的路由器不再获得更新，你仍然可以获得安全更新和补丁。这也意味着任何影响你调制解调器的问题都不会影响你的路由器，反之亦然。
