---
title: iOS Overzicht
icon: simpel/apple
description: iOS is een mobiel besturingssysteem ontwikkeld door Apple voor de iPhone.
---

**iOS** en **iPadOS** zijn gesloten mobiele besturingssystemen ontwikkeld door Apple voor respectievelijk hun iPhone en iPad producten. Als u een Apple mobiel apparaat bezit, kunt u uw privacy verbeteren door wat ingebouwde telemetrie functies uit te schakelen en wat privacy- en beveiligingsinstellingen aan te scherpen, welke zijn ingebouwd in het systeem.

## Privacy Opmerkingen

iOS-apparaten worden regelmatig geprijsd door beveiligingsexperts wegens hun robuuste gegevensbeveiliging en voor het volgen van moderne, beste praktijken. Echter, de restrictiviteit van Apples ecosysteem - met name met hun mobiele apparaten - belemmert privacy nog steeds op een aantal manieren.

We zijn over het algemeen van mening dat iOS voor de meeste mensen een beter dan gemiddelde bescherming biedt op het gebied van privacy en beveiliging, vergeleken met klassiek Android-apparaten van welke fabrikant dan ook. Je kunt echter nog hogere privacynormen bereiken met een [aangepast Android-besturingssysteem](../android.md#aosp-derivatives) zoals GrapheneOS, als je volledig onafhankelijk wilt of moet zijn van de clouddiensten van Apple of Google.

### Activeringsslot

Alle iOS-apparaten moeten worden gecontroleerd door de Activeringsslot-servers van Apple wanneer ze voor het eerst worden ingesteld of gereset, wat betekent dat een internetverbinding **vereist** is om een iOS-apparaat te gebruiken.

### Verplichte App Store

De enige bron voor apps op iOS is de App Store van Apple, waarvoor je een Apple ID nodig hebt om toegang te krijgen. Dit betekent dat Apple kennis heeft van elke app die je op je apparaat installeert en die informatie waarschijnlijk kan koppelen aan je werkelijke identiteit als je de App Store een betaalmethode geeft.

### Invasieve telemetrie

Apple heeft in het verleden problemen gehad met het adequaat anonimiseren van hun telemetrie op iOS. [In 2019](https://theguardian.com/technology/2019/jul/26/apple-contractors-regularly-hear-confidential-details-on-siri-recordings) werd ontdekt dat Apple Siri-opnames, waarvan sommige zeer vertrouwelijke informatie bevatten, doorstuurde naar zijn servers voor handmatige controle door externe contractanten. Hoewel dat programma tijdelijk werd stopgezet nadat [er veel over](https://theverge.com/2019/8/23/20830120/apple-contractors-siri-recordings-listening-1000-a-day-globetech-microsoft-cortana) deze praktijk werd [gesproken in het nieuws](https://theverge. com/2019/8/23/20830120/apple-contractors-siri-recordings-listening-1000-a-day-globetech-microsoft-cortana), werd het probleem pas in [2021](https://theguardian.com/technology/2021/jun/07/apple-overhauls-siri-to-address-privacy-concerns-and-improve-performance) volledig opgelost.

Meer recentelijk is ontdekt dat Apple [analyses verstuurt, zelfs als het delen van analyses is uitgeschakeld](https://gizmodo.com/apple-iphone-analytics-tracking-even-when-off-app-store-1849757558) op iOS. Deze gegevens [lijken](https://twitter.com/mysk_co/status/1594515229915979776) gemakkelijk te kunnen worden gekoppeld aan unieke iCloud-accountidentificatoren, ondanks dat ze zogenaamd anoniem zijn.

## Aanbevolen configuratie

### iCloud

De meeste zorgen over privacy en beveiliging van Apple producten hebben te maken met hun clouddiensten, niet met hun hardware of software. Wanneer je gebruik maakt van Apple diensten zoals iCloud, wordt het merendeel van je gegevens opgeslagen op hun servers en beveiligd met sleutels waar Apple standaard toegang toe heeft. Je kunt [de documentatie van Apple](https://support.apple.com/HT202303) raadplegen voor informatie over welke diensten end-to-end versleuteld zijn. Alles in de lijst "in transit" of "on server" betekent dat Apple toegang kan krijgen tot die gegevens zonder jouw toestemming. Dit toegangsniveau is af en toe misbruikt door wetshandhavers om het feit te omzeilen dat je gegevens anders veilig versleuteld op je apparaat staan. Natuurlijk is Apple net als elk ander bedrijf kwetsbaar voor datalekken.

Als je iCloud gebruikt, moet je daarom [ **Geavanceerde gegevensbescherming** inschakelen](https://support.apple.com/HT212520). Hierdoor worden bijna al je iCloud-gegevens versleuteld met sleutels die zijn opgeslagen op je apparaten (end-to-end versleuteling), in plaats van op de servers van Apple, zodat je iCloud-gegevens beveiligd zijn in het geval van een datalek en daarnaast ontoegankelijk blijven voor Apple.

De versleuteling die wordt gebruikt door Advanced Data Protection is weliswaar sterk, maar [niet *zo* robuust](https://discuss.privacyguides.net/t/apple-advances-user-security-with-powerful-new-data-protections/10778/4) als de versleuteling die wordt aangeboden door andere [clouddiensten](../cloud.md), met name als het gaat om iCloud Drive. Hoewel we het gebruik van Geavanceerde gegevensbescherming sterk aanraden als je iCloud gebruikt, raden we je ook aan om een alternatief voor iCloud te zoeken van een [serviceprovider die](../tools.md) meer [gericht is op privacy](../tools. md), hoewel het onwaarschijnlijk is dat de meeste mensen last zullen hebben van deze eigenaardigheden in de versleuteling.

Je kunt je gegevens ook beschermen door te beperken wat je synchroniseert met iCloud. Bovenaan de **Instellingen-app** zie je je naam en profielfoto als je bent aangemeld bij iCloud. Selecteer dat, dan **iCloud** en zet de schakelaars uit voor services die je niet wilt synchroniseren met iCloud. Het kan zijn dat apps van derden worden weergegeven onder **Toon alles** als ze synchroniseren met iCloud, welke je hier kunt uitschakelen.

#### iCloud+

Een betaald **iCloud+** abonnement (met elk iCloud opslagplan) wordt geleverd met een aantal privacybeschermende functies. Hoewel dit voldoende functionaliteit kan bieden voor huidige iCloud-klanten, zouden we het niet aanraden om puur en alleen voor deze functies een iCloud+-abonnement te kopen in plaats van een [VPN](../vpn.md) en [een aparte e-mailaliasing-service](../email-aliasing.md).

**Privédoorgifte** is een proxyservice die je Safari-verkeer via twee servers doorstuurt: een van Apple en een van een externe provider (waaronder Akamai, Cloudflare en Fastly). In theorie zou dit er voor moeten zorgen dat geen enkele provider in de keten, inclusief Apple, volledig inzicht heeft in welke websites je bezoekt terwijl je verbonden bent. In tegenstelling tot een volledige VPN beschermt Privédoorgifte het verkeer van je apps buiten Safari niet.

**Verberg mijn e-mailadres** is de e-mailaliasingdienst van Apple. Je kunt gratis een e-mailalias aanmaken wanneer je *je aanmeldt met je Apple ID* op een website of app, of onbeperkt aliassen op aanvraag genereren met een betaald iCloud+-abonnement. Verberg mijn e-mailadres heeft het voordeel van het gebruik van het `@icloud.com` domein voor zijn aliassen, wat minder snel geblokkeerd wordt in vergelijking met andere e-mail aliasing diensten, maar biedt geen functionaliteit die geboden wordt door standalone diensten zoals automatische PGP encryptie of meerdere mailboxen ondersteuning.

#### Media & Aankopen

Bovenaan de **Instellingen-app** zie je je naam en profielfoto als je bent aangemeld bij iCloud. Selecteer dat en selecteer vervolgens **Media & Aankopen** > **Account bekijken**.

- [ ] Schakel **Gepersonaliseerde aanbevelingen** uit

#### Zoek mijn

**Find My** is a service that lets you track your Apple devices and share your location with your friends and family. It also allows you to wipe your device remotely in case it is stolen, preventing a thief from accessing your data. Your Find My [location data is E2EE](https://apple.com/legal/privacy/data/en/find-my) when:

- Your location is shared with a family member or friend, and you both use iOS 17 or greater.
- Your device is offline and is located by the Find My Network.

Your location data is not E2EE when your device is online and you use Find My iPhone remotely to locate your device. You will have to make the decision whether these trade-offs are worth the anti-theft benefits of Activation Lock.

Bovenaan de **Instellingen-app** zie je je naam en profielfoto als je bent aangemeld bij iCloud. Select that, then select **Find My**. Here you can choose whether to enable or disable Find My location features.

### Instellingen

Many other privacy-related settings can be found in the **Settings** app.

#### Airplane Mode

Enabling **Airplane Mode** stops your phone from contacting cell towers. You will still be able to connect to Wi-Fi and Bluetooth, so whenever you are connected to Wi-Fi you can turn this setting on.

#### Wi-Fi

You can enable hardware address randomization to protect you from tracking across Wi-Fi networks. On the network you are currently connected to, press the :material-information: button:

- [x] Turn on **Private Wi-Fi Address**

You also have the option to **Limit IP Address Tracking**. This is similar to iCloud Private Relay but only affects connections to "known trackers." Because it only affects connections to potentially malicious servers, this setting is probably fine to leave enabled, but if you don't want *any* traffic to be routed through Apple's servers, you should turn it off.

#### Bluetooth

**Bluetooth** should be disabled when you aren't using it as it increases your attack surface. Disabling Bluetooth (or Wi-Fi) via the Control Center only disables it temporarily: you must switch it off in Settings for disabling it to remain effective.

- [ ] Turn off **Bluetooth**

#### General

Your iPhone's device name will by default contain your first name, and this will be visible to anyone on networks you connect to. You should change this to something more generic, like "iPhone." Select **About** > **Name** and enter the device name you prefer.

It is important to install **Software Updates** frequently to get the latest security fixes. You can enable **Automatic Updates** to keep your phone up-to-date without needing to constantly check for updates. Select **Software Update** > **Automatic Updates**:

- [x] Turn on **Download iOS Updates**
- [x] Turn on **Install iOS Updates**
- [x] Turn on **Security Responses & System Files**

**AirDrop** allows you to easily transfer files, but it can allow strangers to send you files you do not want.

- [x] Select **AirDrop** > **Receiving Off**

**AirPlay** lets you seamlessly stream content from your iPhone to a TV; however, you might not always want this. Select **AirPlay & Handoff** > **Automatically AirPlay to TVs**:

- [x] Select **Never** or **Ask**

**Background App Refresh** allows your apps to refresh their content while you're not using them. This may cause them to make unwanted connections. Turning this off can also save battery life, but it may affect an app's ability to receive updated information, particularly weather and messaging apps.

Select **Background App Refresh** and switch off any apps you don't want to continue refreshing in the background. If you don't want any apps to refresh in the background, you can select **Background App Refresh** again and turn it **Off**.

#### Siri & Search

If you don't want anyone to be able to control your phone with Siri when it is locked, you can turn that off here.

- [ ] Turn off **Allow Siri When Locked**

#### Face ID/Touch ID & Passcode

Setting a strong password on your phone is the most important step you can take for physical device security. You'll have to make tradeoffs here between security and convenience: A longer password will be annoying to type in every time, but a shorter password or PIN will be easier to guess. Setting up Face ID or Touch ID along with a strong password can be a good compromise between usability and security.

Select **Turn Passcode On** or **Change Passcode** > **Passcode Options** > **Custom Alphanumeric Code**. Make sure that you create a [secure password](../basics/passwords-overview.md).

If you wish to use Face ID or Touch ID, you can go ahead and set it up now. Your phone will use the password you set up earlier as a fallback in case your biometric verification fails. Biometric unlock methods are primarily a convenience, although they do stop surveillance cameras or people over your shoulder from watching you input your passcode.

If you use biometrics, you should know how to turn them off quickly in an emergency. Holding down the side or power button and *either* volume button until you see the Slide to Power Off slider will disable biometrics, requiring your passcode to unlock. Your passcode will also be required after device restarts.

On some older devices, you may have to press the power button five times to disable biometrics instead, or for devices with Touch ID you may just have to hold down the power button and nothing else. Make sure you try this in advance so you know which method works for your device.

**Stolen Device Protection** is a new feature in iOS 17.3 which adds additional security intended to protect your personal data if your device is stolen while unlocked. If you use biometrics and the Find My Device feature in your Apple ID settings, we recommend enabling this new protection:

- [x] Select **Turn On Protection**

After enabling Stolen Device Protection, [certain actions](https://support.apple.com/HT212510) will require biometric authentication without a password fallback (in the event that a shoulder surfer has obtained your PIN), such as using password autofill, accessing payment information, and disabling Lost Mode. It also adds a security delay to certain actions performed away from your home or another "familiar location," such as requiring a 1-hour timer to reset your Apple ID password or sign out of your Apple ID. This delay is intended to give you time to enable Lost Mode and secure your account before a thief can reset your device.

**Allow Access When Locked** gives you options for what you can allow when your phone is locked. The more of these options you disable, the less someone without your password can do, but the less convenient it will be for you. Pick and choose which of these you don't want someone to have access to if they get their hands on your phone.

- [ ] Turn off **Today View and Search**
- [ ] Turn off **Notification Center**
- [ ] Turn off **Control Center**
- [ ] Turn off **Lock Screen Widgets**
- [ ] Turn off **Siri**
- [ ] Turn off **Reply with Message**
- [ ] Turn off **Home Control**
- [ ] Turn off **Wallet**
- [ ] Turn off **Return Missed Calls**
- [ ] Turn off **USB Accessories**

iPhones are already resistant to brute-force attacks by making you wait long periods of time after multiple failed attempts; however, there have historically been exploits to get around this. To be extra safe, you can set your phone to wipe itself after 10 failed passcode attempts.

<div class="admonition warning" markdown>
<p class="admonition-title">Warning</p>

With this setting enabled, someone could intentionally wipe your phone by entering the wrong password many times. Make sure you have proper backups and only enable this setting if you feel comfortable with it.

</div>

- [x] Turn on **Erase Data**

#### Privacy & beveiliging

**Location Services** allows you to use features like Find My and Maps. If you don't need these features, you can disable Location Services. Alternatively, you can review and pick which apps can use your location here. Select **Location Services**:

- [ ] Turn off **Location Services**

A purple arrow will appear next to an app in these settings that has used your location recently, while a gray arrow indicates that your location has been accessed within the last 24 hours. If you decide to leave Location Services on, Apple will use it for System Services by default. You can review and pick which services can use your location here. However, if you don't want to submit location analytics to Apple, which they use to improve Apple Maps, you can disable this here as well. Select **System Services**:

- [ ] Turn off **iPhone Analytics**
- [ ] Turn off **Routing & Traffic**
- [ ] Turn off **Improve Maps**

You can decide to allow apps to request to **track** you here. Disabling this disallows all apps from tracking you with your phone's advertising ID. Select **Tracking**:

- [ ] Turn off **Allow Apps to Request to Track**

This is disabled by default and cannot be changed for users under 18.

You should turn off **Research Sensor & Usage Data** if you don't wish to participate in studies. Select **Research Sensor & Usage Data**:

- [ ] Turn off **Sensor & Usage Data Collection**

**Safety Check** allows you to quickly view and revoke certain people and apps that might have permission to access your data. Here you can perform an **Emergency Reset**, immediately resetting permissions for all people and apps which might have access to device resources. You can also **Manage Sharing & Access** which allows you to go through and customize who and what has access to your device and account resources.

You should disable analytics if you don't wish to send Apple usage data. Select **Analytics & Improvements**:

- [ ] Turn off **Share iPhone Analytics** or **Share iPhone & Watch Analytics**
- [ ] Turn off **Share iCloud Analytics**
- [ ] Turn off **Improve Fitness+**
- [ ] Turn off **Improve Safety**
- [ ] Turn off **Improve Siri & Dictation**

Disable **Personalized Ads** if you don't want targeted ads. Select **Apple Advertising**:

- [ ] Turn off **Personalized Ads**

**App Privacy Report** is a built-in tool that allows you to see which permissions your apps are using. Select **App Privacy Report**:

- [x] Select **Turn On App Privacy Report**

[Lockdown Mode](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode) is a security setting you can enable to make your phone more resistant to attacks. Be aware that certain apps and features [won't work](https://support.apple.com/HT212650) as they do normally.

- [x] Select **Turn On Lockdown Mode**

## Additional Advice

### E2EE Calls

Normal phone calls made with the Phone app through your carrier are not E2EE. Both FaceTime Video and FaceTime Audio calls are E2EE, or you can use [another app](../real-time-communication.md) like Signal.

### Avoid Jailbreaking

Jailbreaking an iPhone undermines its security and makes you vulnerable. Running untrusted, third-party software could cause your device to be infected with malware.

### Encrypted iMessage

The color of the message bubble in the Messages app indicates whether your messages are E2EE or not. A blue bubble indicates that you're using iMessage with E2EE, while a green bubble indicates the other party is using the outdated SMS and MMS protocols. Currently, the only way to get E2EE in Messages is for both parties to be using iMessage on Apple devices.

If either you or your messaging partner have iCloud Backup enabled without Advanced Data Protection, the encryption key will be stored on Apple's servers, meaning they can access your messages. Additionally, iMessage's key exchange is not as secure as alternative implementations, like Signal (which allows you to view the recipients key and verify by QR code), so it shouldn't be relied on for particularly sensitive communications.

### Blacking Out Faces/Information

If you need to hide information in a photo, you can use Apple's built-in tools to do so. Open the photo you want to edit, press edit in the top right corner of the screen, then press the markup symbol at the top right. Press the plus at the bottom right of the screen, then press the rectangle icon. Now, you can place a rectangle anywhere on the image. Make sure to press the shape icon at the bottom left and select the filled-in rectangle. **Don't** use the highlighter to obfuscate information, because its opacity is not quite 100%.

### iOS Betas

Apple always makes beta versions of iOS available early for those that wish to help find and report bugs. We don't recommend installing beta software on your phone. Beta releases are potentially unstable and could have undiscovered security vulnerabilities.

## Security Highlights

### Before First Unlock

If your threat model includes forensic tools and you want to minimize the chance of exploits being used to access your phone, you should restart your device frequently. The state *after* a reboot but *before* unlocking your device is referred to as "Before First Unlock" (BFU), and when your device is in that state it makes it [significantly more difficult](https://belkasoft.com/checkm8_glossary) for forensic tools to exploit vulnerabilities to access your data. This BFU state allows you to receive notifications for calls, texts, and alarms, but most of the data on your device is still encrypted and inaccessible. This can be impractical, so consider whether these trade-offs make sense for your situation.
