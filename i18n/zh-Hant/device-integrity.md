---
title: 設備一致完整
icon: material/security
description: 這些工具可用於檢查裝置是否受到攻擊。
cover: device-integrity.webp
---

這些工具可用於驗證行動裝置的完整性，檢查它們是否有間諜軟體和惡意軟體（例如 Pegasus、Predator 或 KingsPawn）的危害跡象。 本頁重點關注**行動安全性**，因為行動裝置通常具有為人所知配置的唯讀系統，檢測惡意修改比傳統桌面系統更容易。 將來可能會再擴展此頁面的重點。

!!! 注意“這是進階主題”

```
這些工具可能為某些人提供實用性，但大多數人無需擔心也用不上的功能，通常需要更深入的技術知識才能有效使用。
```

**至關重要**是了解，掃描設備是否存在公共危害跡象**不足以**確定設備是“乾淨的”、是否為特定間諜軟體工具的目標。 依賴這些公開可用的掃描工具可能會錯過最新的安全發展，帶來錯誤的安全感。

## 一般建議

現代行動裝置上的大多數系統級漏洞（尤其是零點擊攻擊）都是非持久性的，這意味著它們在重新啟動後不會保留或自動運行。 因此，強烈建議定期重新啟動裝置。 我們建議每個設備至少每週重新啟動一次，但如果特別關注非持久性惡意軟體，我們和許多安全專家建議每日重新啟動計劃。

這意味著攻擊者必須定期重新感染裝置才能保留存取權限，儘管我們指出這並非不可能。 重新啟動裝置也無法確保免受「持久性」惡意軟體的侵害，但由於安全/驗證啟動等現代安全功能，這種情況在行動裝置上不太常見。

## 駭漏後資訊和免責聲明

如果以下任何工具表明可能有 Pegasus、Predator 或 KingsPawn 等間諜軟體危害，建議聯絡：

- 如果您是人權捍衛者、記者或來自民間團體：[國際特赦組織安全實驗室](https://securitylab.amnesty.org/contact-us/)
- 如果企業或政府設備受到威脅：請聯絡企業、部門或機構的相應安全聯絡員
- 本地執法單位

**除此之外，我們無法直接為您提供幫助。** 我們很樂意在我們的[社區](https://discuss.privacyguides.net)空間中討論您的具體情況或情況並檢查結果，但不太可能提供本頁所述之外的協助。

此頁面上的工具只能偵測破壞跡象，而不能刪除它們。 如果擔心受到威脅，我們建議：

- 考慮完全更換設備
- 考慮更改 SIM/eSIM 號碼
- 不要從備份重置，因為該備份可能已受到損害

這些工具根據他們能夠從裝置存取的資訊以及可公開存取的破壞指標提供分析。 重要的是記住兩件事：

1. 破壞指標就僅是：_指標_。 它們不是明確的發現，有時可能是**誤報**。 如果偵測到有侵駭跡象，則表示應對「潛在」威脅進行更多研究。
2. 這些工具尋找的侵駭指標由威脅研究組織發布，但並非所有指標都對外開放！ 這意味著，如果裝置感染了任何公共指標都未偵測到的間諜軟體，則工具可能會**漏報**。 可靠且全面的數位鑑識支援和分類需要存取非公開指標、研究和威脅情報。

## 外部驗證工具

External verification tools run on your computer and scan your mobile device for forensic traces which are helpful to identify potential compromise.

!!! danger "危險"

```
Public indicators of compromise are insufficient to determine that a device is "clean", and not targeted with a particular spyware tool. Reliance on public indicators alone can miss recent forensic traces and give a false sense of security.

Reliable and comprehensive digital forensic support and triage requires access to non-public indicators, research and threat intelligence.

Such support is available to civil society through [Amnesty International's Security Lab](https://www.amnesty.org/en/tech/) or [Access Now’s Digital Security Helpline](https://www.accessnow.org/help/).
```

These tools can trigger false-positives. If any of these tools finds indicators of compromise, you need to dig deeper to determine your actual risk. Some reports may be false positives based on websites you've visited in the past, and findings which are many years old are likely either false-positives or indicate previous (and no longer active) compromise.

### Mobile Verification Toolkit

!!! 推薦

```
![MVT logo](assets/img/device-integrity/mvt.webp){ align=right }

**Mobile Verification Toolkit** (**MVT**) is a collection of utilities which simplifies and automates the process of scanning mobile devices for potential traces of targeting or infection by known spyware campaigns. MVT was developed by Amnesty International and released in 2021 in the context of the [Pegasus Project](https://forbiddenstories.org/about-the-pegasus-project/).

[:octicons-home-16: Homepage](https://mvt.re/){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/mvt-project/mvt){ .card-link title="Source Code" }

??? downloads

    - [:simple-apple: macOS](https://docs.mvt.re/en/latest/install/)
    - [:simple-linux: Linux](https://docs.mvt.re/en/latest/install/)
```

!!! warning "警告"

```
Using MVT is insufficient to determine that a device is "clean", and not targeted with a particular spyware tool.
```

MVT is _most_ useful for scanning iOS devices. Android stores very little diagnostic information useful to triage potential compromises, and because of this `mvt-android` capabilities are limited as well. On the other hand, encrypted iOS iTunes backups provide a large enough subset of files stored on the device to detect suspicious artifacts in many cases. This being said, MVT does still provide fairly useful tools for both iOS and Android analysis.

If you use iOS and are at high-risk, we have three additional suggestions for you:

1. Create and keep regular (monthly) iTunes backups. This allows you to find and diagnose past infections later with MVT, if new threats are discovered in the future.

2. Trigger _sysdiagnose_ logs often and back them up externally. These logs can provide invaluable data to future forensic investigators if need be.

   The process to do so varies by model, but you can trigger it on newer phones by holding down _Power_ + _Volume Up_ + _Volume Down_ until you feel a brief vibration. After a few minutes, the timestamped _sysdiagnose_ log will appear in **Settings** > **Privacy & Security** > **Analytics & Improvements** > **Analytics Data**.

3. Enable [Lockdown Mode](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode).

MVT allows you to perform deeper scans/analysis if your device is jailbroken. Unless you know what you are doing, **do not jailbreak or root your device.** Jailbreaking your device exposes it to considerable security risks.

### iMazing (iOS)

!!! 推薦

```
![iMazing logo](assets/img/device-integrity/imazing.png){ align=right }

**iMazing** provides a free spyware analyzer tool for iOS devices which acts as a GUI-wrapper for [MVT](#mobile-verification-toolkit). This can be much easier to run compared to MVT itself, which is a command-line tool designed for technologists and forensic investigators.

[:octicons-home-16: Homepage](https://imazing.com/){ .md-button .md-button--primary }
[:octicons-eye-16:](https://imazing.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://imazing.com/spyware-analyzer){ .card-link title=Documentation}

??? downloads

    - [:simple-windows11: Windows](https://imazing.com/download)
    - [:simple-apple: macOS](https://imazing.com/download)
```

iMazing automates and interactively guides you through the process of using [MVT](#mobile-verification-toolkit) to scan your device for publicly-accessible indicators of compromise published by various threat researchers. All of the information and warnings which apply to MVT apply to this tool as well, so we suggest you also familiarize yourself with the notes on MVT in the sections above.

## 裝置驗證

These are apps you can install which check your device and operating system for signs of tampering, and validate the identity of your device.

!!! warning "警告"

```
Using these apps is insufficient to determine that a device is "clean", and not targeted with a particular spyware tool.
```

### Auditor (Android)

!!! 推薦

```
![Auditor logo](assets/img/device-integrity/auditor.svg#only-light){ align=right }
![Auditor logo](assets/img/device-integrity/auditor-dark.svg#only-dark){ align=right }

**Auditor** is an app which leverages hardware security features to provide device integrity monitoring by actively validating the identity of a device and the integrity of its operating system. Currently, it only works with GrapheneOS or the stock operating system for [supported devices](https://attestation.app/about#device-support).

[:octicons-home-16: Homepage](https://attestation.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://attestation.app/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://attestation.app/about){ .card-link title=Documentation}
[:octicons-code-16:](https://attestation.app/source){ .card-link title="Source Code" }
[:octicons-heart-16:](https://attestation.app/donate){ .card-link title=Contribute }

??? downloads

    - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.attestation.auditor.play)
    - [:simple-github: GitHub](https://github.com/GrapheneOS/Auditor/releases)
    - [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)
```

Auditor is not a scanning/analysis tool like some other tools on this page, rather it uses your device's hardware-backed keystore to allow you to verify the identity of your device and gain assurance that the operating system itself hasn't been tampered with or downgraded via verified boot. This provides a very robust integrity check of your device itself, but doesn't necessarily check whether the user-level apps running on your device are malicious.

Auditor performs attestation and intrusion detection with **two** devices, an _auditee_ (the device being verified) and an _auditor_ (the device performing the verification). The auditor can be any Android 10+ device (or a remote web service operated by [GrapheneOS](android.md#grapheneos)), while the auditee must be a specifically [supported device](https://attestation.app/about#device-support). Auditor 適用於:

- Using a [Trust On First Use (TOFU)](https://en.wikipedia.org/wiki/Trust_on_first_use) model between an _auditor_ and _auditee_, the pair establish a private key in the [hardware-backed keystore](https://source.android.com/security/keystore/) of the _Auditor_.
- The _auditor_ can either be another instance of the Auditor app or the [Remote Attestation Service](https://attestation.app).
- The _auditor_ records the current state and configuration of the _auditee_.
- Should tampering with the operating system of the _auditee_ happen after the pairing is complete, the auditor will be aware of the change in the device state and configurations.
- You will be alerted to the change.

It is important to note that Auditor can only effectively detect changes **after** the initial pairing, not necessarily during or before due to its TOFU model. To make sure that your hardware and operating system is genuine, [perform local attestation](https://grapheneos.org/install/web#verifying-installation) immediately after the device has been installed and prior to any internet connection.

No personally identifiable information is submitted to the attestation service. We recommend that you sign up with an anonymous account and enable remote attestation for continuous monitoring.

If your [threat model](basics/threat-modeling.md) requires privacy, you could consider using [Orbot](tor.md#orbot) or a VPN to hide your IP address from the attestation service.

## 設備掃瞄器

These are apps you can install on your device which scan your device for signs of compromise.

!!! warning "警告"

```
Using these apps is insufficient to determine that a device is "clean", and not targeted with a particular spyware tool.
```

### Hypatia (Android)

!!! 推薦

```
![Hypatia logo](assets/img/device-integrity/hypatia.svg#only-light){ align=right }
![Hypatia logo](assets/img/device-integrity/hypatia-dark.svg#only-dark){ align=right }

**Hypatia** is an open source real-time malware scanner for Android, from the developer of [DivestOS](android.md#divestos). It accesses the internet to download signature database updates, but does not upload your files or any metadata to the cloud (scans are performed entirely locally).

[:octicons-home-16: Homepage](https://divestos.org/pages/our_apps#hypatia){ .md-button .md-button--primary }
[:octicons-eye-16:](https://divestos.org/pages/privacy_policy#hypatia){ .card-link title="Privacy Policy" }
[:octicons-code-16:](https://github.com/divested-mobile/hypatia){ .card-link title="Source Code" }
[:octicons-heart-16:](https://divested.dev/pages/donate){ .card-link title=Contribute }

??? downloads

    - [:simple-android: F-Droid](https://f-droid.org/packages/us.spotco.malwarescanner/)
```

Hypatia is particularly good at detecting common stalkerware: If you suspect you are a victim of stalkerware, you should [visit this page](https://stopstalkerware.org/information-for-survivors/) for advice.

### iVerify (iOS)

!!! 推薦

```
![iVerify logo](assets/img/device-integrity/iverify.webp){ align=right }

**iVerify** is an iOS app which automatically scans your device to check configuration settings, patch level, and other areas of security. It also checks your device for indicators of compromise by jailbreak tools or spyware such as Pegasus.

[:octicons-home-16: Homepage](https://www.iverify.io/consumer){ .md-button .md-button--primary }
[:octicons-eye-16:](https://www.iverify.io/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://www.iverify.io/frequently-asked-questions#iVerify-General){ .card-link title=Documentation}

??? downloads

    - [:simple-appstore: App Store](https://apps.apple.com/us/app/iverify/id1466120520)
```

Like all iOS apps, iVerify is restricted to what it can observe about your device from within the iOS App Sandbox. It will not provide nearly as robust analysis as a full-system analysis tool like [MVT](#mobile-verification-toolkit). Its primary function is to detect whether your device is jailbroken, which it is effective at, however a hypothetical threat which is _specifically_ designed to bypass iVerify's checks would likely succeed at doing so.

iVerify is **not** an "antivirus" tool, and will not detect non-system-level malware such as malicious custom keyboards or malicious Wi-Fi Sync configurations, for example.

In addition to device scanning, iVerify also includes a number of additional security utilities which you may find useful, including device reboot reminders, iOS update notifications (which are often faster than Apple's staggered update notification rollout), some basic privacy and security guides, and a DNS over HTTPS tool which can connect your device's [DNS](dns.md) queries securely to Quad9, Cloudflare, or Google.
