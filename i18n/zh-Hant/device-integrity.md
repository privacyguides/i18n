---
title: 設備一致完整
icon: material/security
description: 這些工具可用於檢查裝置是否受到攻擊。
cover: device-integrity.webp
---

這些工具可用於驗證行動裝置的完整性，檢查它們是否有間諜軟體和惡意軟體（例如 Pegasus、Predator 或 KingsPawn）的危害跡象。 本頁重點關注**行動安全性**，因為行動裝置通常具有為人所知配置的唯讀系統，檢測惡意修改比傳統桌面系統更容易。 將來可能會再擴展此頁面的重點。

<div class="admonition note" markdown>
<p class="admonition-title">This is an advanced topic</p>

這些工具可能對某些人很實用。 They provide functionality which most people do not need to worry about, and often require more in-depth technical knowledge to use effectively.

</div>

It is **critical** to understand that scanning your device for public indicators of compromise is **not sufficient** to determine that a device is "clean", and not targeted with a particular spyware tool. Reliance on these publicly-available scanning tools can miss recent security developments and give you a false sense of security.

## General Advice

The majority of system-level exploits on modern mobile devices—especially zero-click compromises—are non-persistent, meaning they will not remain or run automatically after a reboot. For this reason, we highly recommend rebooting your device regularly. We recommend everybody reboot their devices once a week at minimum, but if non-persistent malware is of particular concern for you, we and many security experts recommend a daily reboot schedule.

This means an attacker would have to regularly re-infect your device to retain access, although we'll note this is not impossible. Rebooting your device also will not protect you against _persistent_ malware, but this is less common on mobile devices due to modern security features like secure/verified boot.

## Post-Compromise Information & Disclaimer

If any of the following tools indicate a potential compromise by spyware such as Pegasus, Predator, or KingsPawn, we advise that you contact:

- If you are a human rights defender, journalist, or from a civil society organization: [Amnesty International's Security Lab](https://securitylab.amnesty.org/contact-us/)
- If a business or government device is compromised: Contact the appropriate security liason at your enterprise, department, or agency
- Local law enforcement

**We are unable to help you directly beyond this.** We are happy to discuss your specific situation or circumstances and review your results in our [community](https://discuss.privacyguides.net) spaces, but it is unlikely we can assist you beyond what is written on this page.

The tools on this page are only capable of detecting indicators of compromise, not removing them. If you are concerned about having been compromised, we advise that you:

- Consider replacing the device completely
- Consider changing your SIM/eSIM number
- Not restore from a backup, because that backup may be compromised

These tools provide analysis based on the information they have the ability to access from your device, and publicly-accessible indicators of compromise. It is important to keep in mind two things:

1. Indicators of compromise are just that: _indicators_. They are not a definitive finding, and may occasionally be **false positives**. If an indicator of compromise is detected, it means you should do additional research into the _potential_ threat.
2. The indicators of compromise these tools look for are published by threat research organizations, but not all indicators are made available to the public! This means that these tools can present a **false negative**, if your device is infected with spyware which is not detected by any of the public indicators. Reliable and comprehensive digital forensic support and triage requires access to non-public indicators, research and threat intelligence.

## External Verification Tools

External verification tools run on your computer and scan your mobile device for forensic traces which are helpful to identify potential compromise.

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

Public indicators of compromise are insufficient to determine that a device is "clean", and not targeted with a particular spyware tool. Reliance on public indicators alone can miss recent forensic traces and give a false sense of security.

Reliable and comprehensive digital forensic support and triage requires access to non-public indicators, research and threat intelligence.

Such support is available to civil society through [Amnesty International's Security Lab](https://www.amnesty.org/en/tech/) or [Access Now’s Digital Security Helpline](https://www.accessnow.org/help/).

</div>

這些工具可能會引發誤報。 如果這些工具中的任何一個發現侵入破壞跡象，需要更深入地挖掘以確定實際風險。 一些報告可能是基於過去訪問過網站的誤報，而多年以前的發現可能是誤報或表明以前（且不再活躍）的問題。

### 行動設備驗證工具包

<div class="admonition recommendation" markdown>

![MVT logo](assets/img/device-integrity/mvt.webp){ align=right }

**Mobile Verification Toolkit** (**MVT**) is a collection of utilities which simplifies and automates the process of scanning mobile devices for potential traces of targeting or infection by known spyware campaigns. MVT was developed by Amnesty International and released in 2021 in the context of the [Pegasus Project](https://forbiddenstories.org/about-the-pegasus-project/).

[:octicons-home-16: Homepage](https://mvt.re/){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/mvt-project/mvt){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-apple: macOS](https://docs.mvt.re/en/latest/install/)
- [:simple-linux: Linux](https://docs.mvt.re/en/latest/install/)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

使用 MVT 應用程式不足以確定設備是“乾淨的”，不是特定間諜軟體工具的目標。

</div>

MVT 對掃描 iOS 裝置「最」有用。 Android 儲存可用於分類潛在危害的診斷資訊非常少，因此「mvt-android」功能也受到限制。 另一方面，加密的 iOS iTunes 備份提供儲存在裝置上足夠大的檔案子集，可在許多情況下偵測可疑工件。 話雖這麼說，MVT 仍為 iOS 和 Android 分析相當有用的工具。

如果使用 iOS 且處於高風險狀態，我們有三個額外建議：

1. 建立並保留定期（每月）iTunes 備份。 如果將來發現新的威脅，可使用 MVT 來尋找和診斷過去的感染。

2. 經常觸發 _sysdiagnose_ 記錄日誌並在外部備份。 如果需要，這些日誌可為鑑識調查人員提供寶貴的資料。

   執行操作過程因型號而異，但可以在較新的手機上按住_電源_ + _音量調高_ + _音量調低_直到感覺到短暫的振動來觸發。 幾分鐘後，帶有時間戳記的 _sysdiagnose_ 日誌將出現在 **設定** > **隱私和安全性** > **分析和改進** > **分析資料** 中。

3. 啟用[鎖定模式](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode)。

如果裝置已 jailbroken 越獄，MVT 可執行更深入的掃描/分析。 除非明確知道在做什麼，否則\*\*不要 Jailbreaking 或root 裝置。\*\*Jailbreaking 裝置會使其面臨相當大的安全風險。

### iMazing (iOS)

<div class="admonition recommendation" markdown>

![iMazing logo](assets/img/device-integrity/imazing.png){ align=right }

**iMazing** provides a free spyware analyzer tool for iOS devices which acts as a GUI-wrapper for [MVT](#mobile-verification-toolkit). This can be much easier to run compared to MVT itself, which is a command-line tool designed for technologists and forensic investigators.

[:octicons-home-16: Homepage](https://imazing.com/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://imazing.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://imazing.com/spyware-analyzer){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-windows11: Windows](https://imazing.com/download)
- [:simple-apple: macOS](https://imazing.com/download)

</details>

</div>

iMazing 會自動並以互動方式引導完成使用 [MVT](#mobile-verification-toolkit) 掃描裝置，尋找由各種威脅研究人員發布的可公開存取的入侵指標。 適用於 MVT 的所有資訊和警告也適用於此工具，因此建議熟悉上述部分中有關 MVT 的說明。

## 裝置驗證

可安裝這些應用程式來檢查裝置和作業系統是否有篡改跡象，並驗證裝置的身份。

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

使用這些應用程式不足以確定設備是“乾淨的”，並不是特定間諜軟體工具的目標。

</div>

### Auditor (Android)

<div class="admonition recommendation" markdown>

![Auditor logo](assets/img/device-integrity/auditor.svg#only-light){ align=right }
![Auditor logo](assets/img/device-integrity/auditor-dark.svg#only-dark){ align=right }

**Auditor** is an app which leverages hardware security features to provide device integrity monitoring by actively validating the identity of a device and the integrity of its operating system. Currently, it only works with GrapheneOS or the stock operating system for [supported devices](https://attestation.app/about#device-support).

[:octicons-home-16: Homepage](https://attestation.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://attestation.app/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://attestation.app/about){ .card-link title=Documentation}
[:octicons-code-16:](https://attestation.app/source){ .card-link title="Source Code" }
[:octicons-heart-16:](https://attestation.app/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.attestation.auditor.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/Auditor/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

Auditor 不像本頁的其他某些掃描/分析工具，而是使用裝置的硬體支援金鑰庫來允許驗證裝置的身份並確保作業系統本身沒有被篡改或透過驗證啟動降級。 這為裝置本身提供了非常強大的完整性檢查，但不一定檢查裝置上執行的使用者級應用程式是否是惡意的。

審核員使用**兩個**設備執行證明和入侵檢測，即一個_被審核者_（正在驗證的設備）和一個_審核員_（執行驗證的設備）。 審核者可以是任何Android 10+ 裝置（或由[GrapheneOS](android.md#grapheneos) 運行的遠端Web 服務），而受審核者必須是專門的[支援的裝置](https\://attestation.app /about #device-support）。 Auditor 適用於:

- 在_審核員_和_被審核者_之間使用 [Trust On First Use (TOFU)](https://en.wikipedia.org/wiki/Trust_on_first_use) 模式，雙方在兩人在[硬體支援的金鑰庫](https://source.android.com/security/keystore/)the pair establish a private key in the [hardware-backed keystore](https://source.android.com/security/keystore/)中建立 _審計員_私鑰。
- _審核員_可以是審核員應用程式的另一個實例，也可以是[遠端憑證服務](https://attestation.app)。
- _審計者_ 記錄 _審計對象_ 當前的狀態和配置。
- 如果在配對完成後發生篡改 審計對象的作業系統 ，審計人員將意識到設備狀態和配置的變化。
- 您將收到更改的提醒。

要注意的是，Auditor 只能在初始配對之後有效檢測變化，而由於其 TOFU 模型，不一定在配對期間或之前檢測到變化。 為了確保硬體和作業系統真實， 在設備安裝後連上網際網路之前，立即 [進行本地認證](https://grapheneos.org/install/web#verifying-installation) 。

沒有個人識別資料被提交給證明服務。 建議使用匿名帳戶註冊，並啟用遠程認證，以進行持續監控。

如果您的 [威脅模型](basics/threat-modeling.md) 需要隱私，可以考慮使用[Orbot](tor.md#orbot) 或VPN，從證明服務中隱藏 IP地址。

## 設備掃瞄器

可在設備上安裝這些應用程序，這些應用程式會掃描裝置是否有遭駭洩漏跡象。

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

使用這些應用程式不足以確定設備是“乾淨的”，並不是特定間諜軟體工具的目標。

</div>

### Hypatia (Android)

<div class="admonition recommendation" markdown>

![Hypatia logo](assets/img/device-integrity/hypatia.svg#only-light){ align=right }
![Hypatia logo](assets/img/device-integrity/hypatia-dark.svg#only-dark){ align=right }

**Hypatia** is an open source real-time malware scanner for Android, from the developer of [DivestOS](android.md#divestos). It accesses the internet to download signature database updates, but does not upload your files or any metadata to the cloud (scans are performed entirely locally).

[:octicons-home-16: Homepage](https://divestos.org/pages/our_apps#hypatia){ .md-button .md-button--primary }
[:octicons-eye-16:](https://divestos.org/pages/privacy_policy#hypatia){ .card-link title="Privacy Policy" }
[:octicons-code-16:](https://github.com/divested-mobile/hypatia){ .card-link title="Source Code" }
[:octicons-heart-16:](https://divested.dev/pages/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-android: F-Droid](https://f-droid.org/packages/us.spotco.malwarescanner/)

</details>

</div>

Hypatia 特別擅長偵測常見的追蹤軟體：如果懷疑自己是追蹤軟體的受害者，請[造訪此頁面](https://stopstalkerware.org/information-for-survivors/) 尋求建議。

### iVerify (iOS)

<div class="admonition recommendation" markdown>

![iVerify logo](assets/img/device-integrity/iverify.webp){ align=right }

**iVerify** is an iOS app which automatically scans your device to check configuration settings, patch level, and other areas of security. It also checks your device for indicators of compromise by jailbreak tools or spyware such as Pegasus.

[:octicons-home-16: Homepage](https://www.iverify.io/consumer){ .md-button .md-button--primary }
[:octicons-eye-16:](https://www.iverify.io/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://www.iverify.io/frequently-asked-questions#iVerify-General){ .card-link title=Documentation}

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-appstore: App Store](https://apps.apple.com/us/app/iverify/id1466120520)

</details>

</div>

與所有 iOS 應用程式一樣，iVerify 僅限於從 iOS 應用程式沙箱內觀察裝置。 它無法提供像 [MVT](#mobile-verification-toolkit) 全系統分析工具的強大分析。 它的主要功能是檢測設備是否 jailbroken，但是「專門」設計用於繞過 iVerify 檢查的假設威脅很可能會成功做到這一點。

iVerify 不是「防毒」工具，不會偵測非系統級惡意軟體，例如惡意自訂鍵盤或惡意 Wi-Fi 同步設定。

除了裝置掃描之外，iVerify 還包括許多有用的附加安全實用程序，包括裝置重新啟動提醒、iOS 更新通知（通常比Apple 的交錯更新通知更快）、一些基本的隱私和安全指南，以及一款基於 HTTPS 的 DNS 工具，可將裝置的 [DNS](dns.md) 查詢安全地連接到 Quad9、Cloudflare 或 Google。
