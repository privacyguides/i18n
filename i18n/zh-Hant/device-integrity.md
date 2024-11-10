---
title: 設備一致完整
icon: material/security
description: 這些工具可用於檢查裝置是否受到攻擊。
cover: device-integrity.webp
robots: nofollow, max-snippet:-1, max-image-preview:large
---

這些工具可用於驗證行動裝置的完整性，檢查它們是否有間諜軟體和惡意軟體（例如：飛馬（Pegasus）、Predator 或 KingsPawn）的危害跡象。 本頁重點關注 **行動平台安全性** ，因為行動裝置通常具有為人所知配置的唯讀系統，檢測惡意修改比傳統桌面系統更容易。 將來可能會再擴展此頁面的重點。

<div class="admonition note" markdown>
<p class="admonition-title">進階主題</p>

這些工具可能對某些人很實用。 它們提供了多數人用不到的功能，通常需要更深入的技術知識才能有效地利用。

</div>

**至關重要**是了解：掃描設備是否存在公共危害跡象**不足以**確定設備是“乾淨的”、是否為特定間諜軟體工具的目標。 依賴這些公開可用的掃描工具可能會錯過最新的安全發展，帶來錯誤的安全感。

## 一般建議

現代行動裝置上的大多數系統級漏洞（尤其是零點擊攻擊）都是非持久性的，這意味著它們在重新啟動後不會保留或自動運行。 因此，強烈建議定期重新啟動裝置。 我們建議每個設備至少每週重新啟動一次，但如果特別關注非持久性惡意軟體，我們和許多安全專家建議每日重新啟動計劃。

這意味著攻擊者必須定期重新感染裝置才能保留存取權限，儘管我們指出這並非不可能。 重新啟動裝置也無法確保免受「持久性」惡意軟體的侵害，但由於安全/驗證啟動等現代安全功能，這種情況在行動裝置上不太常見。

## 駭漏後資訊和免責聲明

如果以下任何工具表明可能有 Pegasus、Predator 或 KingsPawn 等間諜軟體危害，建議聯絡：

- 人權捍衛者、記者或來自民間團體：[國際特赦組織安全實驗室](https://securitylab.amnesty.org/contact-us)
- 企業或政府裝置：您所屬企業、部門或機構的相關資安人員
- 本地執法單位

**除此之外，我們無法直接為您提供幫助。** 我們很樂意在我們的[社區](https://discuss.privacyguides.net)空間中討論您的具體情況或情況並檢查結果，但不太可能提供本頁所述之外的協助。

此頁面上的工具只能偵測破壞跡象，而不能刪除它們。 如果擔心受到威脅，我們建議：

- 考慮完全更換設備
- 考慮更改 SIM/eSIM 號碼
- 不要從備份重置，因為該備份可能已受到損害

這些工具根據他們能夠從裝置存取的資訊以及可公開存取的破壞指標提供分析。 重要的是記住兩件事：

1. 破壞指標就僅是：_指標_。 它們不是明確的發現，有時可能是**誤報**。 如果偵測到有侵駭跡象，則表示應對「潛在」威脅進行更多研究。
2. 這些工具所尋找的危害指標由威脅研究組織發布，但並非所有指標都對外開放！ 這意味著，如果裝置感染了任何公共指標都未偵測到的間諜軟體，則工具可能會**漏報**。 可靠且全面的數位鑑識支援和取得資料後要進行的分類需要存取非公開的指標、研究和威脅情報。

## 外部驗證工具

<small>防護下列威脅：</small>

- [:material-target-account: 針對性攻擊](basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }

外部驗證工具會在您的電腦上執行，並掃描您的行動裝置以尋找「痕跡」，這些「痕跡」有助於識別潛在的損害。

<div class="admonition danger" markdown>
<p class="admonition-title">Danger "危險"</p>

公開的損壞指標不足以確定設備是“乾淨的”、非特定間諜軟體工具的目標。 僅依賴公開指標可能會錯過最新的鑑證痕跡並給予錯誤的安全感。

可靠且全面的數位鑑識支援和取得資料後要進行的分類需要存取非公開的指標、研究和威脅情報。

可透過 [Amnesty International's Security Lab](https://amnesty.org/en/tech/) 或 [Access Now’s Digital Security Helpline](https://accessnow.org/help/) 取得公民社會的此類支援。

</div>

這些工具可能會引發誤報。 如果這些工具中的任何一個發現侵入破壞跡象，需要更深入地挖掘以確定實際風險。 一些報告可能是基於過去訪問過網站的誤報，而多年以前的發現可能是誤報或表明以前（且不再活躍）的問題。

### 行動設備驗證工具包

<div class="admonition recommendation" markdown>

![MVT logo](assets/img/device-integrity/mvt.webp){ align=right }

**Mobile Verification Toolkit** (**MVT**) 是一組實用程式，可簡化和自動化掃描行動裝置的過程，尋找已知間諜軟體活動的潛在目標或感染痕跡。 MVT 由國際特赦組織開發，於 2021 年在 [飛馬計畫（Pegasus Project）](https://forbiddenstories.org/about-the-pegasus-project/) 的背景下發布。

[:octicons-home-16: 首頁](https://mvt.re){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/mvt-project/mvt){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-apple: macOS](https://docs.mvt.re/en/latest/install)
- [:simple-linux: Linux](https://docs.mvt.re/en/latest/install)

</details>

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

使用 MVT 應用程式不足以確定設備是“乾淨的”，不是特定間諜軟體工具的目標。

</div>

MVT 對掃描 iOS 裝置「最」有用。 Android 儲存的診斷資訊非常少，無法用來分流
類潛在的入侵，也因為如此，「mvt-android」的功能也受到限制。 另一方面，加密的 iOS iTunes 備份提供儲存在裝置上足夠大的檔案子集，可在許多情況下偵測可疑工件。 話雖這麼說，MVT 仍為 iOS 和 Android 分析相當有用的工具。

如果使用 iOS 且處於高風險狀態，我們有三個額外建議：

1. 建立並保留定期（每月）iTunes 備份。 如果將來發現新的威脅，可使用 MVT 來尋找和診斷過去的感染。

2. 經常觸發 _sysdiagnose_ 記錄日誌並在外部備份。 如果需要，這些日誌可為鑑識調查人員提供寶貴的資料。

   執行操作過程因型號而異，但可以在較新的手機上按住_電源_ + _音量調高_ + _音量調低_直到感覺到短暫的振動來觸發。 幾分鐘後，帶有時間戳記的 _sysdiagnose_ 日誌將出現在 **設定** > **隱私和安全性** > **分析和改進** > **分析資料** 中。

3. 啟用[鎖定模式](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode)。

如果裝置已 jailbroken 越獄，MVT 可執行更深入的掃描/分析。 除非明確知道在做什麼，否則\*\*不要 Jailbreaking 或root 裝置。\*\*Jailbreaking 裝置會使其面臨相當大的安全風險。

### iMazing (iOS)

<div class="admonition recommendation" markdown>

![iMazing logo](assets/img/device-integrity/imazing.png){ align=right }

**iMazing** 為 iOS 裝置提供免費的間諜軟體分析工具，充當 [MVT](#mobile-verification-toolkit) 的圖形介面包裝器。 相比 MVT ，它更容易運行，前者是專為技術人員和法醫調查人員設計的命令列工具。

[:octicons-home-16: 首頁](https://imazing.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://imazing.com/privacy-policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://imazing.com/spyware-analyzer){ .card-link title=說明文件}

<details class="downloads" markdown>
<summary>下載</summary>

- [:fontawesome-brands-windows: Windows](https://imazing.com/download)
- [:simple-apple: macOS](https://imazing.com/download)

</details>

</div>

iMazing 會自動並以互動方式引導完成使用 [MVT](#mobile-verification-toolkit) 掃描裝置，尋找由各種威脅研究人員發布的可公開存取的入侵指標。 適用於 MVT 的所有資訊和警告也適用於此工具，因此建議熟悉上述部分中有關 MVT 的說明。

## 裝置驗證

<small>防護下列威脅：</small>

- [:material-target-account: 針對性攻擊](basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: 被動攻擊](basics/common-threats.md#security-and-privacy){ .pg-orange }

可安裝這些應用程式來檢查裝置和作業系統是否有篡改跡象，並驗證裝置的身份。

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

使用這些應用程式不足以確定設備是“乾淨的”，並不是特定間諜軟體工具的目標。

</div>

### Auditor (Android)

<div class="admonition recommendation" markdown>

![Auditor logo](assets/img/device-integrity/auditor.svg#only-light){ align=right }
![Auditor logo](assets/img/device-integrity/auditor-dark.svg#only-dark){ align=right }

**Auditor** 是一款利用硬體安全功能通過主動驗證設備身份及其作業系統的完整性來進行完整性監控的應用程式。 目前僅在 GrapheneOS 或 [支援設備](https://attestation.app/about#device-support)的庫存作業系統運行。

[:octicons-home-16: 首頁](https://attestation.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://attestation.app/privacy-policy){ .card-link title="隱私權政策" }
[:octicons-info-16:](https://attestation.app/about){ .card-link title=說明文件}
[:octicons-code-16:](https://attestation.app/source){ .card-link title="原始碼" }
[:octicons-heart-16:](https://attestation.app/donate){ .card-link title=捐款 }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.attestation.auditor.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/Auditor/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

Auditor 並不像本頁上的其他工具一樣是掃描/分析工具。 相反的，它使用由裝置硬體支援的 keystore ，讓您可以驗證裝置的身份，並確保作業系統本身沒有被竄改或遭到 verified boot 降級攻擊。 這為裝置本身提供了非常強大的完整性檢查，但不一定檢查裝置上執行的使用者級應用程式是否是惡意的。

Auditor 使用 **兩個** 設備執行證明和入侵檢測，即一個 _被驗證者（auditee）_ 和一個 _驗證者（auditor）_。 驗證者 可以是任何 Android 10+ 裝置（或是由 [GrapheneOS](android/distributions.md#grapheneos) 所持有的遠端網路服務），而 被驗證者 必須是特定 [支援的裝置](https://attestation.app/about#device-support)。 Auditor 運行原理：

- 在_auditor_和_auditee_之間使用 [Trust On First Use (TOFU)](https://en.wikipedia.org/wiki/Trust_on_first_use) 模式，雙方在 [由硬體支援的 keystore](https://source.android.com/security/keystore/) 中建立 _Auditor（軟體）_ 的私鑰。
- _驗證者_可以是 Auditor應用程式 的另一個實例，也可以是 [遠端憑證服務](https://attestation.app)。
- _驗證者_ 會記錄 _被驗證者_ 當前的狀態和配置。
- 如果在配對完成後 被驗證者的作業系統 遭到篡改 ，驗證者設備 將意識到設備狀態和配置的變化。
- 您將收到更改的提醒。

要注意的是，Auditor 只能在初始配對之後有效檢測變化，而由於其 TOFU 模型，不一定在配對期間或之前檢測到變化。 為了確保硬體和作業系統真實， 在設備安裝後連上網際網路之前，立即 [進行本地認證](https://grapheneos.org/install/web#verifying-installation) 。

沒有個人識別資料被提交給證明服務。 建議使用匿名帳戶註冊，並啟用遠程認證，以進行持續監控。

如果您的 [威脅模型](basics/threat-modeling.md) 需要隱私性，可以考慮使用[Orbot](tor.md#orbot) 或VPN，從證明服務中隱藏 IP地址。

## 設備掃瞄器

<small>防護下列威脅：</small>

- [:material-bug-outline: 被動攻擊](basics/common-threats.md#security-and-privacy){ .pg-orange }

可在設備上安裝這些應用程式，這些應用程式會掃描裝置是否有遭駭洩漏跡象。

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

使用這些應用程式不足以確定設備是“乾淨的”，並不是特定間諜軟體工具的目標。

</div>

### Hypatia (Android)

<div class="admonition recommendation" markdown>

![Hypatia logo](assets/img/device-integrity/hypatia.svg#only-light){ align=right }
![Hypatia logo](assets/img/device-integrity/hypatia-dark.svg#only-dark){ align=right }

**Hypatia** 是 Android 的開放原始碼即時惡意軟體掃描器，由 [DivestOS](android/distributions.md#divestos) 的開發者開發。 它會訪問網際網路以下載已簽署的資料庫更新，但不會上傳您的檔案或任何元資料到雲端（掃描完全在本機執行）。

[:octicons-home-16: 首頁](https://divestos.org/pages/our_apps#hypatia){ .md-button .md-button--primary }
[:octicons-eye-16:](https://divestos.org/pages/privacy_policy#hypatia){ .card-link title="隱私權政策" }
[:octicons-code-16:](https://github.com/divested-mobile/hypatia){ .card-link title="原始碼" }
[:octicons-heart-16:](https://divested.dev/pages/donate){ .card-link title=捐款 }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-fdroid: F-Droid](https://f-droid.org/packages/us.spotco.malwarescanner)

</details>

</div>

Hypatia 特別擅長偵測常見的追蹤軟體（stalkerware）：如果懷疑自己是追蹤軟體的受害者，請 [造訪此頁面](https://stopstalkerware.org/information-for-survivors/) 尋求建議。
