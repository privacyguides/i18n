---
title: Windows 概览
icon: material/microsoft-windows
description: Microsoft Windows 是一个常见的操作系统，但其开箱即用状态极度缺乏隐私保护。我们的指南涵盖了在不更换操作系统的情况下对计算机进行一些改进。
---

**Microsoft Windows** 是许多个人电脑默认搭载的常见操作系统。以下指南旨在提供一些通过禁用一些不必要的功能来改善隐私、减少默认遥测和存储数据的方法。随着时间的推移，微软会向操作系统添加有时可能依赖于基于云的服务的功能。这些功能通常需要某些类型的[可选数据](https://privacy.microsoft.com/data-collection-windows)，这些数据有时会被发送到远程服务器进行处理。

最新的例子之一称为 **Recall**，它是 Copilot AI 功能集的一部分。 Recall 会定期对你在电脑上看到的任何内容进行截图，以便以后向你展示。这些“有帮助”的功能产生了大量的元数据，可以进行取证分析。在大多数情况下，浏览历史记录就足够了，可以安全地禁用此功能。对 Recall 的主要担忧是数据存储在本地数据库中，该数据库在设备开机时解密，这意味着如果设备感染恶意软件，它将成为黑客的容易目标。 Recall 不会从数据库中删除复制的密码或财务信息等敏感信息，但它确实可以防止对受数字版权管理 (DRM) 系统保护的任何受版权保护的内容进行截图。

不幸的是，此功能的添加并没有太多考虑默认启用此类功能对隐私的影响（现在[已不再默认启用](https://wired.com/story/microsoft-recall-off-default-security-concerns)）。然而，这并不是孤例。另一个例子是，微软在未请求许可的情况下，自动在新的 Windows 11 安装中[启用对 OneDrive 的文件夹备份](https://neowin.net/news/windows-11-is-now-automatically-enabling-onedrive-folder-backup-without-asking-permission)。

你可以通过以下指南在不下载任何第三方工具的情况下增强 Windows 的隐私和安全性：

- 初始安装（即将推出）
- [组策略设置](group-policies.md)
- 隐私设置（即将推出）
- 应用程序沙盒（即将推出）
- 安全加固（即将推出）

<div class="admonition example" markdown>
<p class="admonition-title">此部分是新的</p>

本节是一项正在进行的工作，因为与其他操作系统相比，让 Windows 安装更加注重隐私需要花费大量的时间和精力。

</div>

## 隐私注意事项

微软的 Windows 系统，特别是针对普通消费者的版本（如 **家庭版**），往往[默认](https://theguardian.com/technology/2015/jul/31/windows-10-microsoft-faces-criticism-over-privacy-default-settings)不会优先考虑隐私友好的功能。结果我们经常看到[数据收集](https://en.wikipedia.org/wiki/Criticism_of_Microsoft#Telemetry_and_data_collection)超出了必要的范围，而没有任何真正的警告表明这是默认行为。为了在广告领域与 Google 竞争，[Cortana](https://en.wikipedia.org/wiki/Cortana_(virtual_assistant)) 包含“广告 ID”等唯一标识符，以便关联使用情况并协助广告商进行精准广告投放。在发布时，Windows 10 的非企业版无法禁用遥测。现在仍然无法完全禁用，但微软增加了[减少](https://extremetech.com/computing/243079-upcoming-windows-update-reduces-spying-microsoft-still-mum-data-collects)发送给他们的数据的功能。

Windows 11 存在一些限制或默认设置，例如：

- 要求使用 Microsoft 帐户而不是本地帐户。
- 这使得 Windows **专业版**和**企业版**更难找到本地账户选项。
- 默认启用所有数据收集选项，要求用户主动“选择退出”。
- 将 Bing、OneDrive 和 Teams 等 Microsoft 服务深度集成到系统中，难以移除，并作为唯一的选项展示给用户。
- 始终将默认浏览器设置为 Edge，或者如果已更改，则恢复为 Edge。
- 在 Windows 的许多区域以及各种 Microsoft 应用中添加基于云的 AI 功能。
- 不必要地存储敏感数据。即使是存储在本地且未发送给微软的数据，仍然可能成为黑客或恶意软件的目标。

Microsoft 经常使用自动更新功能向您的设备添加新功能并进行收集您的数据且默认启用的更改。某些[隐私功能](https://blogs.windows.com/windows-insider/2023/11/16/previewing-changes-in-windows-to-comply-with-the-digital-markets-act-in-the-european-economic-area)（例&#x5982;_&#x9009;择退&#x51FA;_&#x5C06;在线 Microsoft 帐户与 Windows 同步的选项）要求您在安装期间选择 EEA（欧洲经济区）的国家/地区。可以在安装 Windows 后将其更改为您的真实国家。

## Windows 版本

不幸的是，许多关键隐私和安全功能被锁定在成本更高的 Windows 版本中，而不是在 Windows **家庭版**中提供。**家庭版**缺少的一些功能包括 BitLocker 驱动器加密、Hyper-V 和 Windows 沙盒。在我们的 Windows 指南中，我们将介绍如何适当地使用所有这些功能，因此拥有高级版 Windows 将是必要的。

在配置内置于 Windows 中的隐私和安全设置时，Windows **企业版**提供了最大的灵活性。例如，它们是唯一允许您对通过遥测工具发送给 Microsoft 的数据启用最高级别限制的版本。不幸的是，企业版不进行零售，所以您可能无法购买。

可&#x4F9B;_&#x96F6;&#x552E;_&#x8D2D;买的最佳版本是 Windows **专业版**，因为它拥有您想要用来保护您的设备的几乎所有功能，包括 BitLocker、Hyper-V 等。不幸的是，唯一缺少的是对微软遥测的一些最严格的限制。

学生和教师可能可以从其教育机构免费获得 Windows **教育版**（相当于企业版）或**专业教育版**许可证（相当于专业版），包括在个人设备上使用。许多学校通过 OnTheHub 或 Microsoft Azure for Education 与微软合作，因此你可以查看这些网站或学校的福利页面，看看你是否符合资格。您是否能够获得这些许可证完全取决于您的机构。这可能是许多人获得供个人使用的企业级 Windows 版本的最佳方式。与零售版本相比，使用教育版许可证没有任何额外的隐私或安全风险。

不建议使用 Windows AME 等第三方修改版的 Windows。由于像 Windows AME 这样修改后的 Windows 版本不会收到更新，Windows Defender 中的安全功能和防病毒定义将落后于当前的威胁环境，从而使您容易受到攻击，进而导致您变得更加不安全。

## 获取 Windows

目前，只能购买 Windows 11 许可证密钥，但这些密钥也适用于 Windows 10，因此您仍然可以购买 Windows 11 专业版密钥来激活 Windows 10 安装。

官方的[媒体创建工具](https://microsoft.com/software-download/windows11)是将 Windows 安装程序放到 USB 闪存驱动器上的最佳方式。像 Rufus 或 Etcher 这样的第三方工具可能会意外地修改文件，这可能导致引导问题或安装时的其他麻烦。

此工具只允许您进行**家庭版**或**专业版**安装，因为没有 Windows **企业版**的公开下载。如果您有**企业版**许可证密钥，您可以轻松升级**专业版**安装。为此，请在不输入许可证密钥的情况下安装 Windows **专业版**，然后在安装完成后，在“设置”应用中输入您的**企业版**密钥。输入有效的许可证密钥后，您的**专业版**安装将自动升级为**企业版**。

如果您要安装**教育版**许可证，那么通常会有一个私人下载链接，当您从机构的福利门户获取它时，该链接将与您的许可证密钥一起提供。
