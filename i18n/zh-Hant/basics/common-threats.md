---
title: "常見威脅"
icon: 'material/eye-outline'
description: 您的威脅模型雖說是個人的事，但它也是本站許多訪客關心的課題。
---

廣義來講，我們將建議歸類為適用於大多數人的 [威脅](threat-modeling.md) 或目標。 您可能會在意各種可能性的組合，而選用的工具和服務則取決於您的目標何在。 You may have specific threats outside these categories as well, which is perfectly fine! 重要的是要了解您選擇使用的工具的好處和缺點，因為幾乎沒有一種工具可以保護您免受任何威脅。

<span class="pg-purple">:material-incognito: **匿名**</span>
:

將您的線上活動與您的真實身分相遮蔽，保護您不受特別想揭露*您*身分的人的攻擊。

<span class="pg-red">:material-target-account: **針對性攻擊**</span>
:

避免駭客或其他惡意行為者特別企圖存取*您的*資料或裝置。

<span class="pg-viridian">:material-package-variant-closed-remove: **供應鏈攻擊**</span>
:

Typically, a form of <span class="pg-red">:material-target-account: Targeted Attack</span> that centers around a vulnerability or exploit introduced into otherwise good software either directly or through a dependency from a third party.

<span class="pg-orange">:material-bug-outline: **被動攻擊**</span>
:

避免惡意軟體、資料外洩和其他同時針對許多人的攻擊。

<span class="pg-teal">:material-server-network: **服務提供商**</span>
:

保護您的資料不被服務供應商讀取（例如使用 E2EE ，使伺服器無法讀取您的資料）。

<span class="pg-blue">:material-eye-outline: **大規模監控**</span>
:

防止政府機構、組織、網站和服務共同追蹤您的活動。

<span class="pg-brown">:material-account-cash: **監控資本主義**</span>
:

保護自己不受大型廣告網路商（如 Google 和 Facebook）以及其他無數第三方資料收集者的侵害。

<span class="pg-green">:material-account-search: **公開曝光**</span>
:

Limiting the information about you that is accessible online—to search engines or the public.

<span class="pg-blue-gray">:material-close-outline: **審查**</span>
:

避免在線上發言時，資訊存取受到審查或自己受到審查。

其中一些威脅對您來說可能比其他威脅更嚴重，這取決於您的具體問題。 例如，有權存取有價值或關鍵資料的軟體開發人員可能主要關心 <span class="pg-viridian">:material-package-variant-closed-remove: 供應鏈攻擊</span> 和 <span class="pg-red">:material-target-account: 針對性的攻擊</span>。 他們可能仍然希望保護自己的個人資料免受 <span class="pg-blue">:material-eye-outline: 大規模監控</span> 計劃的影響。 同樣，許多人主要關心其個人資料的 <span class="pg-green">:material-account-search: 公開曝光</span> ，但他們仍應該警惕聚焦安全的問題，例如 <span class="pg-orange">:material-bug-outline: 被動攻擊</span>—例如惡意軟體影響他們的裝置。

## 匿名 vs. 隱私

<span class="pg-purple">:material-incognito: 匿名</span>

匿名通常與隱私相混淆，但它們是不同的概念。 隱私是您對如何使用和共享資料所做出的一系列選擇，而匿名是將您的線上活動與真實身份完全分離。

舉例來說，揭密者和記者會需要一個更極端、要求完全匿名的威脅模型。 這不僅隱藏了他們所做的事情、擁有的資料，不會被惡意行為者或政府駭客入侵，而且還完全隱暪了他們的身份。 他們經常需犧牲任何形式的便利，以保護自身的匿名性，隱私或安全，因為很可能事關自己的性命。 大多數人都不需要那樣。

## 安全與隱私

<span class="pg-orange">:material-bug-outline: 被動攻擊</span>

安全性和隱私也經常被混淆，因為您需要安全性來獲得任何形式的隱私：使用的工具----即便設計私密----但若很容易地受到攻擊者造成資料外洩，一切就是白廢了。 然而，相反的情況並不一定成立：世界上最安全的服務*不一定是* 私密的。 最好的例子是信任把資料交給 Google，因為它們規模龐大聘請業界領先的安全專家來保護其基礎設施，幾乎沒有發生過安全事故。 儘管 Google 提供了非常安全的服務，但很少有人會認為在Google 免費消費產品（Gmail、YouTube 等）中的資料是私密的。

當涉及到應用程式安全性時，我們通常不知道（有時甚至無法知道）使用的軟體是否是惡意軟體或者有一天它會變成惡意軟體。 即使是最值得信賴的開發人員，通常情況下也無法保證他們的軟體沒有嚴重的漏洞有一天會被利用。

減少惡意軟體*可能造成的破壞* ，最好能落實安全劃分方案。 例如，用不同電腦作不同的事、利用虛擬器來分組不同的相關應用程式，或者使用一個高集中的應用程式沙盒和強制訪問控制的安全操作系統。

<div class="admonition tip" markdown>
<p class="admonition-title">溫馨提示</p>

行動作業系統通常具有比桌面作業系統具備更好的應用程式沙盒：應用程式沒有根存取權限，且需要存取系統資源的權限。

桌面操作系統通常在適當的沙盒化上落後。 ChromeOS has similar sandboxing capabilities to Android, and macOS has full system permission control (and developers can opt in to sandboxing for applications). 然而，這些作業系統確實會將識別資料傳回給各自的OEMs。 Linux 傾向於不對系統供應商提交資料，但它在漏洞和惡意應用程式的保護很差。 這可以通過專門的發行版來緩解，這些發行版大量使用虛擬器或容器，例如 [Qubes OS](../desktop.md#qubes-os)。

</div>

## 針對特定個人的攻擊

<span class="pg-red">:material-target-account: 針對性攻擊</span>

針對特定人士的針對性攻擊更難處理。 常見的攻擊包括通過電子郵件發送惡意文件、利用(瀏覽器和操作系統的)漏洞以及物理攻擊。 如果這是您擔心這點，應該採用更先進的威脅減輕策略。

<div class="admonition tip" markdown>
<p class="admonition-title">溫馨提示</p>

在設計上， **網頁瀏覽器**、**電子郵件用戶端** 和 **辦公室應用程式** 常常運行源自第三方的無法信任的代碼。 運行多個虛擬器-將這些應用程式與主機系統相互分開，此技術可減少系統遭到應用程式攻擊的機會。 例如， Qubes OS 或 Windows 上的 Microsoft Defender Application Guard 等技術提供了方便的作法。

</div>

若特別擔心 **物理攻擊**，就應選用具安全驗證開機的作業系統，例如 Android, iOS, macOS, 或[Windows (帶 TPM)](https://learn.microsoft.com/windows/security/information-protection/secure-the-windows-10-boot-process)。 應確保您的驅動器是加密的，並且操作系統使用 TPM或 Secure [Enclave](https://support.apple.com/guide/security/secure-enclave-sec59b0b31ff/1/web/1) 或 [Element](https://developers.google.com/android/security/android-ready-se) 來限制輸入加密密碼的嘗試率。 您應該避免與不信任的人共享您的電腦，因為大多數桌面作業系統不會單獨加密每個用戶的數據。

## 針對某些組織的攻擊

<span class="pg-viridian">:material-package-variant-closed-remove: 供應鏈攻擊</span>

供應鏈攻擊往往是 <span class="pg-red">:material-target-account: 針對性攻擊</span> 的一種，其指向企業、政府和活動人士的利益，也可能最終損害廣大公眾的利益。

<div class="admonition example" markdown>
<p class="admonition-title">範例</p>

一個著名例子是 2017 年，當時烏克蘭流行的會計軟體 M.E.Doc 感染了 *NotPetya* 病毒，隨後勒索軟體感染了下載該軟體的人。 NotPetya 本身就是一種勒索軟體攻擊，影響了跨國 2000 多家公司，其基於 NSA 開發的 *EternalBlue* 漏洞來透過網路攻擊 Windows 電腦。

</div>

執行此類攻擊的方式有以下幾種：

1. 貢獻者或員工可能會先在專案或組織中取得權力地位，然後濫用該地位，加入惡意程式碼。
2. 開發人員可能會受到外部脅迫添加惡意程式碼。
3. 個人或團體可能會識別第三方軟體依賴（也稱為庫），並透過上述兩種方法對其進行滲透，因為他們知道它將被「下游」軟體開發人員使用。

此類攻擊可能需要大量時間和準備才能執行，且存在風險，因為它們可以被檢測到，特別是在開源專案中，如果很受歡迎受到外部關注的話。 不幸的是，它們也是最危險的之一，很難完全緩解。 我們鼓勵讀者僅使用具有良好聲譽的軟體，並透過以下方式努力降低風險：

1. 只採用已經存在一段時間的流行軟體。 對於專案的興趣越大，外界注意到惡意變更的可能性就越大。 惡意行為者還需要花費更多時間透過有意義的貢獻來贏得社群信任。
2. 尋找透過廣泛使用的、可信任的構建基礎架構平台發布二進位檔案的軟體，而不是開發人員工作站或自架伺服器。 某些系統（例如 GitHub Actions）可檢查公開執行的建置腳本，以獲得額外的信心。 這降低了開發人員電腦上的惡意軟體感染其軟體包的可能性，讓人確信生成的二進位檔案是正確生成的。
3. 尋找單一原始碼提交和發布的程式碼簽名，這會建立誰做了什麼的可審計追蹤。 例如：惡意程式碼是否在軟體儲放庫中？ 哪個開發者添加的？ 是建置過程中新增的嗎？
4. 檢查原始程式碼是否提交有意義的訊息（例如： [常規提交](https://conventionalcommits.org) ），這些訊息解釋了更改應完成的任務。 清晰的訊息可以讓外部人士更容易驗證、審核和發現錯誤。
5. 注意程式的貢獻者或維護者的數量。 單獨的開發人員可能較容易受到外部人員的威脅而新增惡意程式碼，或因疏忽導致不良行為。 這很可能意味著「大型科技公司」開發的軟體比不向任何人負責的單獨開發人員受到更多審查。

## 服務供應商的隱私權

<span class="pg-teal">:material-server-network: 服務提供商</span>

我們活在一個幾乎所有東西都連上網際網路的世界。 我們的「私人」訊息、電子郵件和社交互動通常儲存在伺服器的某個地方。 通常，當您向某人發送訊息時，它會儲存在伺服器上，當對方想要閱讀訊息時，伺服器會將其顯示給他們。

顯而易見的問題是，服務提供商（或破壞伺服器的駭客）可以隨時隨地訪問您的對話，而您永遠不會知道。 這適用於許多常見的服務，例如 SMS 訊息、Telegram 和 Discord。

慶幸的是， E2EE 可以加密您與收件人之間的通訊，甚至在訊息送到伺服器之前，緩解此問題。 假設服務提供商無法訪問任何一方的私鑰，您的訊息保密性得到保證。

<div class="admonition note" markdown>
<p class="admonition-title">Web 加密備註提醒</p>

實際上，不同 E2EE 操作的效力各不相同。 應用程式，例如 [Signal](../real-time-communication.md#signal)，會在您的裝置上原生執行，且此應用程式在不同設備的安裝上都是如此。 如果服務提供商在他們的應用程式中植入[後門](https://zh.wikipedia.org/wiki/Backdoor_(computing)) ----試圖竊取您的私鑰----它稍後可以通過[逆向工程](https://zh.wikipedia.org/wiki/Reverse_engineering)偵測。

另一方面，基於網頁的 E2EE 實作，例如 Proton Mail 的網頁應用程式或 Bitwarden 的 *Web Vault* ，則依賴伺服器動態提供 JavaScript 程式碼給瀏覽器來處理加密。 惡意伺服器可以針對您發送惡意 JavaScript 代碼以竊取您的加密金鑰（這將非常難以察覺）。 因為伺服器可以選擇為不同的人提供不同的網頁用戶端，即使您注意到攻擊也很難證明提供商有罪。

因此，您應該盡可能使用原生軟體程式多於網頁客戶端。

</div>

即便使用 E2EE ，服務商仍然可以對**元數據**進行分析，這通常不受保護。 While the service provider can't read your messages, they can still observe important things, such as whom you're talking to, how often you message them, and when you're typically active. 元數據的保護不多，如果它在您的 [威脅模型](threat-modeling.md) 中，就應該密切注意使用軟體的技術說明，看看元數據是否最小化或任何保護。

## 大規模監控計劃

<span class="pg-blue">:material-eye-outline: 大規模監控</span>

大規模監控是對全體 (或其中某一群特定)人群進行錯綜複雜的監視活動。[^1] 它通常是指政府項目，例如由[Edward Snowden 在 2013](https://en.wikipedia.org/wiki/Global_surveillance_disclosures_(2013%E2%80%93present))所揭露的內幕。 然而，它也可以由公司代表政府機構或由他們自己主動進行。

<div class="admonition abstract" markdown>
<p class="admonition-title">監控地圖集</p>

如想進一步了解監控方法及其在您的城市的實施方式，也可以查看[電子前鋒基金會 EFF](https://eff.org/)的[監控地圖集](https://atlasofsurveillance.org/)。

In France, you can take a look at the [Technopolice website](https://technopolice.fr/villes) maintained by the non-profit association La Quadrature du Net.

</div>

政府常認為大規模監控計劃是打擊恐怖主義和預防犯罪的必要手段。 然而，作為違反人權的行為，它們最常被用來過度針對少數族群和政治異見人士等。

<div class="admonition quote" markdown>
<p class="admonition-title">ACLU： <em><a href="https://aclu.org/news/national-security/the-privacy-lesson-of-9-11-mass-surveillance-is-not-the-way-forward">The Privacy Lesson of 9/11: Mass Surveillance is Not the Way Forward</a></em></p>

對於愛德華·斯諾登（Edward Snowden）披露的 [PRISM](https://zh.wikipedia.org/wiki/PRISM)和 [Upstream](https://en.wikipedia.org/wiki/Upstream_collection)等政府計劃，情報官員承認，國家安全局多年來一直祕密地收集每個美國人電話記錄—誰、何時及通話時間多久。 當 NSA 日復一日地收集這類資訊時，就可以揭示人們生活相關聯的敏感細節，例如他們是否打電話給牧師、墮胎提供者、成癮顧問或自殺熱線。

</div>

儘管在美國有越來越多的大規模監控，政府卻發現像依 215 條採取的監控計畫在阻卻犯案與恐怖陰謀上沒有實用價值，它們幾乎只是重複著 FBI 所做的特定監控計畫而已。[^2]

在線上，可透過各種方式追蹤您，包括但不限於：

- 您的 IP 位址
- 瀏覽器 cookie
- 您提交到網站的資料
- 您的瀏覽器或裝置指紋
- 付款方式關聯

如果您擔心大規模監控計劃，您可以隨時隨地策略性避免提供識別個資，例如劃分您的網路身份，與其他用戶混合。

## 「監視」：作為一種商業模式

<span class="pg-brown">:material-account-cash: 監控資本主義</span>

> 監控資本主義的核心是獲取個人資料並將之商品化，以謀求最大利潤的經濟體系。[^3]

對於許多人來說，私人公司的追蹤和監視是一個越來越令人擔憂的問題。 無處不在的廣告網路，例如 Google 和 Facebook 營運的廣告網路，跨越網路遠超過他們直接控制的網站，沿途跟蹤您的行為。 使用內容攔截工具來限制對伺服器的請求、閱讀了解所用服務的隱私政策，都有助於避開許多基本對手 (雖然這不能完全防止跟蹤)。[^4]

Additionally, even companies outside the *AdTech* or tracking industry can share your information with [data brokers](https://en.wikipedia.org/wiki/Information_broker) (such as Cambridge Analytica, Experian, or Datalogix) or other parties. 您不能僅因為您使用的服務不屬於典型的 AdTech 或追蹤產業商業模式，而自行假設您的資料是安全的。 對抗企業資料收集最好的保護是盡可能加密或混淆您的數據，讓不同的供應商難以將資料相互關聯去建立您的個人檔案。

## 限制公共資訊

<span class="pg-green">:material-account-search: 公共曝露</span>

保持資料私密性的最佳方法是根本不要公開它。 刪除網路上有關您現已不用的資訊是恢復隱私的最佳第一步。

- [查看帳戶刪除指南 :material-arrow-right-drop-circle:](account-deletion.md)

對於您分享資訊的網站，檢查帳戶的隱私設定以限制資料傳播的範圍非常重要。 例如，如果提供選項，請在您的帳戶上啟用「私人模式」：這可確保您的帳戶不會被搜尋引擎編入索引，而且在未經您的許可下無法查看。

如果您已經將真實資訊提交給不應該擁有該資訊的網站，請考慮使用虛假策略，例如提交該網路身份的虛構資訊。 這使得您的真實資訊無法與虛假資訊作區分。

## 避免審查

<span class="pg-blue-gray">:material-close-outline: 審查</span>

網路審查包括由極權主義政府、網路管理員和服務提供商等主體進行的行為（在不同程度上）。 這些試圖控制通訊與限縮資料取用的作為，往往不見容於意見自由的基本人權。[^5]

對企業平臺的審查越來越普遍，如Twitter 和 Facebook 等平臺屈服於公眾需求、市場和政府機構的壓力。 政府對企業的施壓可能是隱蔽的，例如白宮私下 [要求拿掉](https://nytimes.com/2012/09/17/technology/on-the-web-a-fine-line-on-free-speech-across-globe.html) 某個勯動的 Youtube 影片，或是公開者如中國政府命令企業要遵循嚴厲的審查制度。

關注審查威脅的人可以使用像 [Tor](../advanced/tor-overview.md) 這樣的技術來規避它，並支援像 [Matrix](../real-time-communication.md#element)這樣的抗審查通訊平臺，該平臺沒有可以任意關閉帳戶的集中帳戶權限。

<div class="admonition tip" markdown>
<p class="admonition-title">溫馨提示</p>

雖然很容易避掉審查，但隱藏您正在做的事可就沒那麼簡單了。

您應該考慮可讓對手觀察哪些網路行為，以及能否對這些行為有合理的否認說辭。 例如，使用[加密 DNS](../advanced/dns-overview.md#what-is-encrypted-dns)可以幫助您繞過對 DNS 基本審查系統，但它無法對 ISP 隱藏您正在訪問的內容。 VPN 或 Tor 有助於向網路管理員隱藏您正在訪問的內容，但無法隱藏您正在使用 VPN 或 Tor 。 可插拔傳輸（例如 Obfs4proxy、Meek 或 Shadowsocks）可以幫助您避開阻擋常見VPN 協議或 Tor 的防火牆，但仍然可以通過探測或[深度封包檢查](https://en.wikipedia.org/wiki/Deep_packet_inspection) 等方法檢測您嘗試做的規避。

</div>

您必須考慮試圖繞過網路審查的風險、潛在的後果以及您的對手可能很經驗老道。 您應該謹慎選擇軟體，並制定備份計劃以防被抓住。

[^1]: 維基百科: [*大型監控*](https://en.wikipedia.org/wiki/Mass_surveillance) 與 [*監控*](https://en.wikipedia.org/wiki/Surveillance).
[^2]: 美國隱私和公民自由監督委員會： [*根據第 215 條進行的電話記錄計劃的報告*](https://documents.pclob.gov/prod/Documents/OversightReport/ec542143-1079-424a-84b3-acc354698560/215-Report_on_the_Telephone_Records_Program.pdf)
[^3]: 維基百科: [*監控資本主義*](https://en.wikipedia.org/wiki/Surveillance_capitalism)
[^4]: “[枚舉壞處](https://ranum.com/security/computer_security/editorials/dumb)” （或“列出所知的全部壞事” ），未能充分保護您免受新的和未知的威脅，因為許多內容攔截程式和防病毒程式尚未被添加到過濾器列表。 您還應採用其他緩解技術。
[^5]: 聯合國： [*世界人權宣言*](https://un.org/en/about-us/universal-declaration-of-human-rights)。
