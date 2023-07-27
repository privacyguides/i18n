---
title: סקירה כללית של iOS
icon: simple/apple
description: iOS היא מערכת הפעלה ניידת שפותחה על ידי אפל עבור האייפון.
---

**iOS** ו-**iPadOS** הן מערכות הפעלה קנייניות לנייד שפותחו על ידי אפל עבור מוצרי האייפון והאייפד שלהם, בהתאמה. אם יש לך מכשיר נייד של אפל, תוכל להגביר את הפרטיות שלך על ידי השבתת כמה תכונות טלמטריה מובנות, והקשחת הגדרות פרטיות ואבטחה המובנות במערכת.

## הערות פרטיות

מכשירי iOS זוכים לעתים קרובות לשבחים על ידי מומחי אבטחה על הגנת הנתונים האיתנה והעמידה בשיטות המומלצות המודרניות. עם זאת, ההגבלה של המערכת האקולוגית של אפל - במיוחד עם המכשירים הניידים שלה - עדיין פוגעת בפרטיות במספר דרכים.

בדרך כלל אנו מחשיבים את iOS כמספקת הגנות פרטיות ואבטחה טובות מהממוצע עבור רוב האנשים, בהשוואה למכשירי אנדרואיד במלאי מכל יצרן. עם זאת, אתה יכול להשיג סטנדרטים גבוהים עוד יותר של פרטיות עם [מערכת הפעלה אנדרואיד מותאמת אישית](../android.md) כמו GrapheneOS, אם אתה רוצה או צריך להיות בלתי תלוי לחלוטין באפל או בשירותי הענן של גוגל.

### נעילת הפעלה

כל מכשירי iOS חייבים להיבדק מול שרתי Activation Lock של אפל כאשר הם מוגדרים או מאפסים לראשונה, כלומר חיבור לאינטרנט **נדרש** כדי להשתמש במכשיר iOS.

### חנות אפליקציות חובה

המקור היחיד לאפליקציות ב-iOS הוא חנות האפליקציות של אפל, שדורשת מזהה אפל כדי לגשת אליה. משמעות הדבר היא כי לאפל יש תיעוד של כל אפליקציה שאתה מתקין במכשיר שלך, וסביר להניח שהיא יכולה לקשור את המידע הזה לזהותך האמיתית אם תספק ל-App Store אמצעי תשלום.

### טלמטריה פולשנית

לאפל היו בעבר בעיות עם אנונימיזציה נכונה של הטלמטריה שלהם ב-iOS. [בשנת 2019](https://www.theguardian.com/technology/2019/jul/26/apple-contractors-regularly-hear-confidential-details-on-siri-recordings), אפל נמצאה משדרת הקלטות Siri - חלקן מכילות מידע סודי ביותר - לשרתים שלהן לבדיקה ידנית על ידי קבלני צד שלישי. בזמן שהם הפסיקו זמנית את התוכנית הזו אחרי האימון הזה היה [דיווח נרחב על](https://www.theverge.com/2019/8/23/20830120/apple-contractors-siri-recordings-listening-1000-a-day-globetech-microsoft-cortana), הבעיה לא נפתרה לחלוטין [עד 2021](https://www.theguardian.com/technology/2021/jun/07/apple-overhauls-siri-to-address-privacy-concerns-and-improve-performance).

לאחרונה, נמצאה שאפל [משדרת ניתוח נתונים גם כאשר שיתוף הניתוח מושבת ](https://gizmodo.com/apple-iphone-analytics-tracking-even-when-off-app-store-1849757558) ב-iOS, והנתונים האלה [נראים](https://twitter.com/mysk_co/status/1594515229915979776) מקושרים בקלות למזהים ייחודיים של חשבון iCloud למרות שהם כביכול אנונימיים. אפל לא תיקנה את [בעיות אלו](https://gizmodo.com/clarence-thomas-aide-venmo-laywers-supreme-court-1850631585) החל מיולי 2023.

## תצורה מומלצת

### iCloud

רוב דאגות הפרטיות והאבטחה של מוצרי Apple קשורות לשירותי הענן שלהם, לא לחומרה או לתוכנה שלהם. כאשר אתה משתמש בשירותי אפל כמו iCloud, רוב המידע שלך מאוחסן בשרתים שלהם ומאובטח באמצעות מפתחות שאליהם יש לאפל גישה כברירת מחדל. You can check [Apple's documentation](https://support.apple.com/HT202303) for information on which services are end-to-end encrypted. Anything listed as "in transit" or "on server" means it's possible for Apple to access that data without your permission. This level of access has occasionally been abused by law enforcement to get around the fact that your data is otherwise securely encrypted on your device, and of course Apple is vulnerable to data breaches like any other company.

Therefore, if you do use iCloud you should [enable **Advanced Data Protection**](https://support.apple.com/HT212520). This encrypts nearly all of your iCloud data with keys stored on your devices (end-to-end encryption), rather than Apple's servers, so that your iCloud data is secured in the event of a data breach, and otherwise hidden from Apple.

The encryption used by Advanced Data Protection, while strong, [is not *quite* as robust](https://discuss.privacyguides.net/t/apple-advances-user-security-with-powerful-new-data-protections/10778/4) as the encryption offered by other [cloud services](../cloud.md), particularly when it comes to iCloud Drive. While we strongly encourage using Advanced Data Protection if you use iCloud, we would also suggest considering finding an alternative to iCloud from a more [privacy-focused service provider](../tools.md), although it is unlikely most people would be impacted by these encryption quirks.

You can also protect your data by limiting what you sync to iCloud in the first place. At the top of the **Settings** app, you'll see your name and profile picture if you are signed in to iCloud. Select that, then **iCloud**, and turn off the switches for any services you don't want to sync to iCloud. You may see third-party apps listed under **Show All** if they sync to iCloud, which you can disable here.

#### iCloud+

A paid **iCloud+** subscription (with any iCloud storage plan) comes with some privacy-protecting functionality. While these may provide adequate service for current iCloud customers, we wouldn't recommend purchasing an iCloud+ plan over a [VPN](../vpn.md) and [standalone email aliasing service](../email.md#email-aliasing-services) just for these features alone.

**Private Relay** is a proxy service which relays your Safari traffic through two servers: one owned by Apple and one owned by a third-party provider (including Akamai, Cloudflare, and Fastly). In theory this should prevent any single provider in the chain—including Apple—from having full visibility into which websites you visit while connected. Unlike a full VPN, Private Relay does not protect traffic from your apps outside of Safari.

**Hide My Email** is Apple's email aliasing service. You can create an email aliases for free when you *Sign In With Apple* on a website or app, or generate unlimited aliases on demand with a paid iCloud+ plan. Hide My Email has the advantage of using the `@icloud.com` domain for its aliases, which may be less likely to be blocked compared to other email aliasing services, but does not offer functionality offered by standalone services such as automatic PGP encryption or multiple mailbox support.

#### Media & Purchases

At the top of the **Settings** app, you'll see your name and profile picture if you are signed in to an Apple ID. Select that, then select **Media & Purchases** > **View Account**.

- [ ] Turn off **Personalized Recommendations**

#### Find My

**Find My** is a service that lets you track your Apple devices and share your location with your friends and family. It also allows you to wipe your device remotely in case it is stolen, preventing a thief from accessing your data. Your Find My [location data is E2EE](https://www.apple.com/legal/privacy/data/en/find-my/) when:

- Your location is shared with a family member or friend, and you both use iOS 15 or greater.
- Your device is offline and is located by the Find My Network.

Your location data is not E2EE when your device is online and you use Find My iPhone remotely to locate your device. You will have to make the decision whether these trade-offs are worth the anti-theft benefits of Activation Lock.

At the top of the **Settings** app, you'll see your name and profile picture if you are signed in to an Apple ID. Select that, then select **Find My**. Here you can choose whether to enable or disable Find My location features.

### הגדרות

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

Select **Turn Passcode On** or **Change Passcode** > **Passcode Options** > **Custom Alphanumeric Code**. Make sure that you create a [secure password](https://www.privacyguides.org/basics/passwords-overview/).

If you wish to use Face ID or Touch ID, you can go ahead and set it up now. Your phone will use the password you set up earlier as a fallback in case your biometric verification fails. Biometric unlock methods are primarily a convenience, although they do stop surveillance cameras or people over your shoulder from watching you input your passcode.

If you use biometrics, you should know how to turn them off quickly in an emergency. Holding down the side or power button and *either* volume button until you see the Slide to Power Off slider will disable biometrics, requiring your passcode to unlock. Your passcode will also be required after device restarts.

On some older devices, you may have to press the power button five times to disable biometrics instead, or for devices with Touch ID you may just have to hold down the power button and nothing else. Make sure you try this in advance so you know which method works for your device.

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

!!! warning "אזהרה"

    With this setting enabled, someone could intentionally wipe your phone by entering the wrong password many times. Make sure you have proper backups and only enable this setting if you feel comfortable with it.

- [x] Turn on **Erase Data**

#### פרטיות

**Location Services** allows you to use features like Find My and Maps. If you don't need these features, you can disable Location Services. Alternatively, you can review and pick which apps can use your location here. Select **Location Services**:

- [ ] Turn off **Location Services**

You can decide to allow apps to request to **track** you here. Disabling this disallows all apps from tracking you with your phone's advertising ID. Select **Tracking**:

- [ ] Turn off **Allow Apps to Request to Track**

You should turn off **Research Sensor & Usage Data** if you don't wish to participate in studies. Select **Research Sensor & Usage Data**:

- [ ] Turn off **Sensor & Usage Data Collection**

**Safety Check** allows you to quickly view and revoke certain people and apps that might have permission to access your data. Here you can perform an **Emergency Reset**, immediately resetting permissions for all people and apps which might have access to device resources, and you can **Manage Sharing & Access** which allows you to go through and customize who and what has access to your device and account resources.

You should disable analytics if you don't wish to send Apple usage data. Select **Analytics & Improvements**:

- [ ] Turn off **Share iPhone Analytics** or **Share iPhone & Watch Analytics**
- [ ] Turn off **Share iCloud Analytics**
- [ ] Turn off **Improve Fitness+**
- [ ] Turn off **Improve Safety**
- [ ] Turn off **Improve Siri & Dictation**

Disable **Personalized Ads** if you don't want targeted ads. Select **Apple Advertising**

- [ ] Turn off **Personalized Ads**

**App Privacy Report** is a built-in tool that allows you to see which permissions your apps are using. Select **App Privacy Report**:

- [x] Select **Turn On App Privacy Report**

[Lockdown Mode](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode) is a security setting you can enable to make your phone more resistant to attacks. Be aware that certain apps and features [won't work](https://support.apple.com/en-us/HT212650) as they do normally.

- [x] Select **Turn On Lockdown Mode**

## Additional Advice

### E2EE Calls

Normal phone calls made with the Phone app through your carrier are not E2EE. Both FaceTime Video and FaceTime Audio calls are E2EE, or you can use [another app](../real-time-communication.md) like Signal.

### Avoid Jailbreaking

Jailbreaking an iPhone undermines its security and makes you vulnerable. Running untrusted, third-party software could cause your device to be infected with malware.

### Encrypted iMessage

The color of the message bubble in the Messages app indicates whether your messages are E2EE or not. A blue bubble indicates that you're using iMessage with E2EE, while a green bubble indicates they're using the outdated SMS and MMS protocols. Currently, the only way to get E2EE in Messages is for both parties to be using iMessage on Apple devices.

If either you or your messaging partner have iCloud Backup enabled without Advanced Data Protection, the encryption key will be stored on Apple's servers, meaning they can access your messages. Additionally, iMessage's key exchange is not as secure as alternative implementations, like Signal (which allows you to view the recipients key and verify by QR code), so it shouldn't be relied on for particularly sensitive communications.

### Blacking Out Faces/Information

If you need to hide information in a photo, you can use Apple's built-in tools to do so. Open the photo you want to edit, press edit in the top right corner of the screen, then press the markup symbol at the top right. Press the plus at the bottom right of the screen, then press the rectangle icon. Now, you can place a rectangle anywhere on the image. Make sure to press the shape icon at the bottom left and select the filled-in rectangle. **Don't** use the highlighter to obfuscate information, because its opacity is not quite 100%.

### iOS Betas

Apple always makes beta versions of iOS available early for those that wish to help find and report bugs. We don't recommend installing beta software on your phone. Beta releases are potentially unstable and could have undiscovered security vulnerabilities.

## Security Highlights

### Before First Unlock

If your threat model includes forensic tools and you want to minimize the chance of exploits being used to access your phone, you should restart your device frequently. The state *after* a reboot but *before* unlocking your device is referred to as "Before First Unlock" (BFU), and when your device is in that state it makes it [significantly more difficult](https://belkasoft.com/checkm8_glossary) for forensic tools to exploit vulnerabilities to access your data. This BFU state allows you to receive notifications for calls, texts, and alarms, but most of the data on your device is still encrypted and inaccessible. This can be impractical, so consider whether these trade-offs make sense for your situation.
