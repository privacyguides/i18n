---
title: 選擇您的硬體
icon: material/chip
description: 隱私保護不能僅聚焦於軟體方面；了解您每天使用的硬體，以保護您的隱私。
---

當談到隱私權的討論時，硬體往往不如軟體那般受到重視。 您的硬體應該被視為建立其他隱私設定的基礎。

## 挑選電腦

您的裝置處理並儲存所有數位資料。 重要的是，您所使用的裝置製造商和開發商必須持續提供安全性更新

### 硬體安全認證

有些裝置會有「硬體安全認證」，例如在設計硬體時，廠商之間會就最佳實務和建議進行合作：

- [Windows 安全核心電腦](https://learn.microsoft.com/en-us/windows-hardware/design/device-experiences/oem-highly-secure-11) 符合 Microsoft 指定的更高安全性標準。 這些保護並不只適用於 Windows 使用者；其他作業系統的使用者仍可利用其 [DMA 保護](https://learn.microsoft.com/en-us/windows/security/information-protection/kernel-dma-protection-for-thunderbolt) 以及 完全不信任 Microsoft 證書 等功能。
- [Android Ready SE](https://developers.google.com/android/security/android-ready-se) 是廠商之間的合作，以確保其裝置遵循 [最佳實踐](https://source.android.com/docs/security/best-practices/hardware) ，並包含基於硬體的可防篡改儲存設備，例如加密金鑰。
- 在 Apple SoC 上執行的 macOS 可利用 [硬體安全性](.../os/macos-overview.md#hardware-security) ，第三方作業系統可能無法使用此類功能。
- [ChromeOS 的安全性](https://chromium.org/chromium-os/developer-library/reference/security/security-whitepaper) 在 Chromebook 上可發揮最佳效果，因為它能利用可用的硬體功能，例如 [硬體信任根](https://chromium.org/chromium-os/developer-library/reference/security/security-whitepaper/#hardware-root-of-trust-and-verified-boot) 。

即使您不使用這些作業系統，參與這些計畫也可能表示製造商在硬體安全性和更新方面遵循最佳實踐。

### 預先安裝的作業系統

新電腦幾乎都會預先安裝 Windows，除非您買的是 Mac 或特殊的 Linux 機器。 通常擦除硬碟並重新安裝您所選擇的作業系統是個好主意，即便是從頭重新安裝 Windows 也同樣如此。 由於硬體廠商與不良軟體廠商之間的協議，預裝的 Windows 通常會預先載入臃腫軟體、[廣告軟體](https://bleepingcomputer.com/news/technology/lenovo-gets-a-slap-on-the-wrist-for-superfish-adware-scandal)，甚至是 [惡意軟體](https://zdnet.com/article/dell-poweredge-motherboards-ship-with-malware) 。

### 韌體更新

硬體經常會有安全問題，這些問題會透過硬體的韌體更新來發現和修補。

從您的主機板到儲存設備，幾乎電腦的每個元件都需要韌體才能運作。 理想的情況是，您裝置的所有元件都能獲得完整支援。 只要裝置受支援，Apple 裝置、Chromebook、大多數 Android 手機和 Microsoft Surface 裝置都會為您處理韌體更新。

如果您自己組裝電腦，可能需要從 OEM 網站下載主機板韌體，手動更新主機板韌體。 如果您使用 Linux，可考慮使用內建的 [`fwupd`](https://fwupd.org) 工具，讓您檢查並套用主機板的任何可用韌體更新。

### TPM/安全加密協處理器

大多數電腦和手機都配備 TPM （或類似的安全加密協處理器），可安全儲存您的加密金鑰，並處理其他與安全相關的功能。 如果您目前使用的機器沒有這些功能，您可能會從購買具有此功能的較新電腦中獲益。 有些桌上型電腦和伺服器主機板有一個「TPM 接口」，可供添加包含 TPM 的小型配件板。

<div class="admonition Note" markdown>
<p class="admonition-title">備註</p>

虛擬 TPM 容易受到側通道攻擊，而外部 TPM 由於與主機板上的 CPU 分離，當攻擊者能夠存取硬體時，容易受到 [監聽](https://pulsesecurity.co.nz/articles/TPM-sniffing) 攻擊。 解決這個問題的方法是將安全加密協處理器包含在 CPU 本身，Apple 的晶片和微軟的 [Pluton](https://microsoft.com/en-us/security/blog/2020/11/17/meet-the-microsoft-pluton-processor-the-security-chip-designed-for-the-future-of-windows-pcs) 就是如此。

</div>

### 生物識別技術

許多裝置都配備了指紋辨識器或臉部辨識功能。 這些方法可能非常方便，但並不完美，有時也會失敗。 當發生這種情況時，大多數裝置都會回退到 PIN 或密碼，這意味著您裝置的安全性仍然取決於密碼。

生物識別技術可以防止有人監視您輸入密碼，因此，如果您的威脅模式中包括肩窺，那麼生物識別技術就是一個很好的選擇。

大多數的臉部辨識實作都需要您看著您的手機，而且也只能在相對較近的距離才能運作，所以您不需要太擔心有人會在未經您同意的情況下，將您的手機對準您的臉部來解鎖。 如果您願意，仍可在手機鎖定時停用生物辨識功能。 在 iOS 上，您可以按住側邊按鈕和音量按鈕 3 秒鐘，在支援 Face ID 的機型上停用 Face ID。 在 Android 上，按住電源按鈕，然後按下功能表上的 鎖定 。

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

有些裝置沒有適當的硬體來進行安全的臉部驗證。 臉部辨識有兩種主要類型：2D 和 3D。 3D 類型的臉部辨識利用點陣投影器，讓裝置為您的臉部建立 3D 深度圖。 請確定您的裝置具有此功能。

</div>

Android 為生物辨識定義了三種 [安全等級](https://source.android.com/docs/security/features/biometric/measure#biometric-classes) ，您應該在啟用生物辨識之前檢查您的裝置是否屬於 Class 3。

### 裝置加密

如果您的裝置已進行 [加密](../encryption.md) ，在裝置完全關機 (而非僅是睡眠狀態) 時，也就是在您第一次輸入加密金鑰或鎖屏密碼之前，您的資料是最安全的（相較於其他狀態）。 在手機上，這種較高安全性的狀態稱為 “Before First Unlock（首次解鎖之前）（BFU）”，而一旦您在重新開機/開機後輸入正確密碼，則稱為 “After First Unlock（首次解鎖之後）（AFU）”。 AFU is considerably less secure against digital forensics toolkits and other exploits, compared to BFU. Therefore, if you are concerned about an attacker with physical access to your device, you should turn it off fully whenever you aren't using it.

This may be impractical, so consider whether it's worth it, but in either case even AFU mode is effective against most threats, given you are using a strong encryption key.

## External Hardware

Some threats can't be protected against by your internal components alone. Many of these options are highly situational; please evaluate if they are really necessary for your threat model.

### 硬件安全金鑰

Hardware keys are devices that use strong cryptography to authenticate you to a device or account. The idea is that because they can not be copied, you can use them to secure accounts in such a way that they can only be accessed with physical possession of the key, eliminating many remote attacks.

[Recommended Hardware Keys :material-arrow-right-drop-circle:](../security-keys.md){ .md-button .md-button--primary } [Learn More about Hardware Keys :material-arrow-right-drop-circle:](multi-factor-authentication.md#hardware-security-keys){ .md-button }

### Camera/Microphone

If you don't want to trust your OS's permission controls to prevent the camera from activating in the first place, you can buy camera blockers that physically prevent light from reaching the camera. You could also buy a device that doesn't have a built-in camera and use an external camera that you can unplug whenever you're done using it. Some devices come with built-in camera blockers or hardware switches that physically disconnect the camera from power.

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

You should only buy covers that fit your laptop and won't cause damage when you close the lid. Covering the camera will interfere with automatic brightness and face authentication features.

</div>

For microphone access, in most cases you will need to trust your OS's built-in permission controls. Alternatively, buy a device that doesn't have a built-in microphone and use an external microphone that you can unplug when you're done using it. Some devices, like a [MacBook or an iPad](https://support.apple.com/guide/security/hardware-microphone-disconnect-secbbd20b00b/web), feature a hardware disconnect for the microphone when you close the lid.

Many computers have a BIOS option to disable the camera and microphone. When disabled there, the hardware won't even appear as a device on a booted system.

### Privacy Screens

Privacy screens are a film you can put over your normal screen so that the screen is only visible from a certain angle. These are good if your threat model includes others peeking at your screen, but it is not foolproof as anyone could just move to a different viewing angle and see what's on your screen.

### Dead Man's Switches

A dead man's switch stops a piece of machinery from operating without the presence of a human operator. These were originally designed as a safety measure, but the same concept can be applied to an electronic device to lock it when you're not present.

Some laptops are able to [detect](https://support.microsoft.com/en-us/windows/managing-presence-sensing-settings-in-windows-11-82285c93-440c-4e15-9081-c9e38c1290bb) when you're present and can lock automatically when you aren't sitting in front of the screen. You should check the settings in your OS to see if your computer supports this feature.

You can also get cables, like [Buskill](https://buskill.in), that will lock or wipe your computer when the cable is disconnected.

### Anti-Interdiction/Evil Maid Attack

The best way to prevent a targeted attack against you before a device is in your possession is to purchase a device in a physical store, rather than ordering it to your address.

Make sure your device supports secure boot/verified boot, and you have it enabled. Try to avoid leaving your device unattended whenever possible.

## Secure your Network

### Compartmentalization

Many solutions exist that allow you to separate what you're doing on a computer, such as virtual machines and sandboxing. However, the best compartmentalization is physical separation. This is useful especially for situations where certain software requires you to bypass security features in your OS, such as with anti-cheat software bundled with many games.

For gaming, it may be useful to designate one machine as your "gaming" machine and only use it for that one task. Keep it on a separate VLAN. This may require the use of a managed switch and a router that supports segregated networks.

Most consumer routers allow you to do this by enabling a separate "guest" network that can't talk to your main network. All untrusted devices can go here, including IoT devices like your smart fridge, thermostat, TV, etc.

### Minimalism

As the saying goes, "less is more". The fewer devices you have connected to your network, the less potential attack surface you'll have and the less work it will be to make sure they all stay up-to-date.

You may find it useful to go around your home and make a list of every connected device you have to help you keep track.

### Routers

Your router handles all your network traffic and acts as your first line of defense between you and the open internet.

<div class="admonition Note" markdown>
<p class="admonition-title">備註</p>

A lot of routers come with storage to put your files on so you can access them from any computer on your network. We recommend you don't use networking devices for things other than networking. In the event your router was compromised, your files would also be compromised.

</div>

The most important thing to think about with routers is keeping them up-to-date. Many modern routers will automatically install updates, but many others won't. You should check on your router's settings page for this option. That page can usually be accessed by typing `192.168.1.1` or `192.168.0.1` into the URL bar of any browser assuming you're on the same network. You can also check in the network settings of your OS for "router" or "gateway".

If your router does not support automatic updates, you will need to go to the manufacturer's site to download the updates and apply them manually.

Many consumer-grade routers aren't supported for very long. If your router isn't supported by the manufacturer anymore, you can check if it's supported by [FOSS firmware](../router.md). You can also buy routers that come with FOSS firmware installed by default; these tend to be supported longer than most routers.

Some ISPs provide a combined router/modem. It can be beneficial for security to purchase a separate router and set your ISP router/modem into modem-only mode. This way, even when your ISP-provided router is no longer getting updates, you can still get security updates and patches. It also means any problems that affect your modem won't affect your router and vice versa.
