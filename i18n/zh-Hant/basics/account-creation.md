---
meta_title: "如何私下創建網際網路帳戶 - Privacy Guides"
title: "創建帳號"
icon: 'material/account-plus'
description: 創建帳戶為實際連線網際網路所必要，請採取下列步驟確保您的線上隱私。
---

人們經常不假思索地註冊網路服務。 Maybe it's a streaming service to watch that new show everyone's talking about, or an account that gives you a discount for your favorite fast food place. 無論在什麼樣的場景，您都應該考慮現在和以後對個資的影響。

在新的服務申請帳號時，都伴著相關風險。 資料洩露；向第三方披露客戶資訊、員工有不當的權限可以訪問所有資料，在給出您的個資時都必須考慮的接下來可能的狀況。 您需要確信足夠信任該服務，這就是為什麼我們建議把重要資料儲存在最成熟且通過測試的產品。 這通常意味著提供 E2EE 並經過加密審計的服務。 審計增加了產品設計的保證，減低因開發人員缺乏經驗所導致的安全問題。

某些網路服務並不容易刪除帳號 有時可能會 [覆寫與帳戶相關聯的資料](account-deletion.md#overwriting-account-information) ，但在其他情況下，該服務將保留帳戶變更的完整記錄。

## 服務條款 & 隱私權政策

服務條款是您在使用服務時同意遵守的規則。 隨著更大的服務，這些規則通常由自動化系統強制執行。 有時這些自動化系統可能會出錯。 For example, you may be banned or locked out of your account on some services for using a VPN or VoIP number. 對這種禁令提出上訴通常很困難，而且通常都由系統自動處理而不是人工審核，造成了上訴的困難度。 這也是我們不建議使用 Gmail 作為電子郵件的原因之一。 電子郵件對於訪問您已註冊的其他服務至關重要。

The Privacy Policy is how the service says they will use your data, and it is worth reading so that you understand how your data will be used. 公司或組織可能沒有法律義務遵守政策中包含的所有內容（取決於司法管轄區）。 我們建議您了解當地法律以及這些法律允許供應商收集哪些資訊。

我們建議您尋找特定的術語，例如「資料收集」、「資料分析」、「Cookie」、「廣告」或「第三方」服務。 Sometimes you will be able to opt out from data collection or from sharing your data, but it is best to choose a service that respects your privacy from the start.

請記住，您把信任託付給該公司或組織，冀望其真的遵守自己的隱私政策。

## 身份驗證方式

通常有多種註冊帳戶的方式，每種都有各自的好處和缺點。

### 電子郵件和密碼

建立新帳戶的最常見方式是使用電子郵件地址和密碼。 使用此方法時，您應該使用密碼管理器，並遵循 [關於密碼的最佳做法](passwords-overview.md) 。

<div class="admonition tip" markdown>
<p class="admonition-title">溫馨提示</p>

您也可以使用密碼管理器來管理其他驗證方式！ 只要新增一則條目並填寫相關欄位資訊，您也可註記安全問題或備份金鑰等事項。

</div>

您自己負責管理您的登入憑證。 為了增加安全性，您可以在帳戶上設定 [MFA](multi-factor-authentication.md) 。

[推薦密碼管理員](../passwords.md ""){.md-button}

#### 電子郵件別名

如果您不想將您的真實電子郵件地址提供給服務，您可以選擇使用別名。 We describe them in more detail on our email services recommendation page. 基本上，別名服務允許您生成新的電子郵件位址，將所有電子郵件轉發到您的主位址。 This can help prevent tracking across services and help you manage the marketing emails that sometimes come with the sign-up process. 這些可以根據它們被發送到的別名自動過濾。

如果服務遭到駭客攻擊，您用於註冊的電子郵件可能會收到網路釣魚或垃圾郵件。 為每個服務使用獨特的別名可以幫助確定哪些服務被駭。

[推薦的電子郵件別名服務](../email-aliasing.md ""){.md-button}

### "登入方式：" (OAuth)

[Open Authorization (OAuth)](https://en.wikipedia.org/wiki/OAuth) is an authentication protocol that allows you to register for a service without sharing much information with the service provider, if any, by using an existing account you have with another service instead. 每當您在註冊表單上看到「登入方式: 使用 *提供商名稱*登入」時，它就是 OAuth。

當您透由 OAuth 登入，它會開啟您所選的供應商登入頁面而您的帳戶即會與新帳戶連接。 我們不會分享你的密碼，但會分享一些基本資訊（你可以在登入期間要求查看）。 每次您想要登入同一個帳戶時，都需要進行此程序。

主要優勢是：

- **Security**: You don't have to trust the security practices of the service you're logging into when it comes to storing your login credentials because they are stored with the external OAuth provider. Common OAuth providers like Apple and Google typically follow the best security practices, continuously audit their authentication systems, and don't store credentials inappropriately (such as in plain text).
- **Ease-of-use**: Multiple accounts are managed by a single login.

但也有一些缺陷：

- **Privacy**: The OAuth provider you log in with will know the services you use.
- **Centralization**: If the account you use for OAuth is compromised, or you aren't able to log in to it, all other accounts connected to it are affected.

OAuth 在那些服務之間深度整合情況下，可以特別有用。 我們建議將 OAuth 限制在需要的地方，用 [MFA](multi-factor-authentication.md)來保護主帳戶。

所有使用 OAuth 的服務都將與您的基礎提供商帳戶一樣安全。 例如，想用實體安全金鑰保護某個帳戶，但該服務不支援實體安全金鑰，則可用實體安全金鑰保護您的 OAuth 帳戶，現在您所有帳戶基本上都有硬體 MFA。 但值得注意的是，OAuth 帳戶的弱認證意味著與該登入方式相關的其它帳戶也會很弱。

使用* Google 登入*、*Facebook* 或其他服務時還有額外的危險，通常是OAuth 流程允許*雙向*資料共享。 例如，使用 Twitter 帳戶登入論壇可授予該論壇存取權限，以便在您的 Twitter 帳戶上執行操作，例如發佈、閱讀您的訊息或存取其他個人資料。 OAuth 提供者通常會向您提供要授予外部服務存取權限的內容列表，應確保仔細閱讀該列表，不會無意中授予外部服務存取不需要的任何內容的權限。

惡意應用程式（特別是行動裝置，它們可以用來存取登入OAuth 提供者的WebView 會話）也可以透過劫持與 OAuth 提供者的會話來取得對 OAuth 帳戶的存取權限。 使用任何提供者的*登入方式*選項通常是為了方便，最好只用於相信不會主動惡意的服務。

### 電話號碼

我們建議您避免使用需要電話號碼才能註冊的服務。 A phone number can identify you across multiple services and depending on data sharing agreements this will make your usage easier to track, particularly if one of those services is breached as the phone number is often **not** encrypted.

如果可以的話，你應該避免透露你的真實電話號碼。 Some services will allow the use of VoIP numbers, however these often trigger fraud detection systems, causing an account to be locked down, so we don't recommend that for important accounts.

在許多情況下，您需要提供可以接收短信或電話的號碼，特別是在國際購物時，以防您在邊境審查時的訂單出現問題。 服務通常會使用您的號碼作為驗證方式；不要自作聰明使用假的電話號碼，最後讓自己重要的帳戶被鎖定！

### 使用者名稱與密碼

某些服務允許您在不使用電子郵件地址的情況下註冊，並且只需要您設定用戶名稱和密碼。 當與 VPN 或 Tor 結合時，這些服務可能會提供更高的匿名性。 請記住，對於這類型的帳號，如果你忘記了你的用戶名或密碼，很可能會有**沒有辦法恢復你的帳號**。
