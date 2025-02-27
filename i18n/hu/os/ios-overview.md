---
title: iOS áttekintés
icon: simple/apple
description: Az iOS egy mobil operációs rendszer, amelyet az Apple fejlesztett ki az iPhone-okra.
---

Az **iOS** és az **iPadOS** az Apple által az iPhone és az iPad termékekhez kifejlesztett saját mobil operációs rendszerek. Ha rendelkezel egy Apple mobil eszközzel, növelheted a magánéletedet a beépített telemetria funkciók kikapcsolásával, valamint néhány adatvédelmi és biztonsági beállítás megerősítésével, amelyek be vannak építve a rendszerbe.

## Adatvédelmi megjegyzés

iOS devices are frequently praised by security experts for their robust data protection and adherence to modern best practices. Azonban az Apple zárt ökoszisztémájának korlátozó volta – különösen a mobil eszközök esetében – továbbra is számos módon hátráltatja a magánélet védelmét.

Általánosságban úgy véljük, hogy az iOS a legtöbb ember számára az átlagosnál jobb adatvédelmi és biztonsági védelmet nyújt, mint a bármelyik gyártótól származó Android készülékek. However, you can achieve even higher standards of privacy with a [custom Android operating system](../android/distributions.md) like GrapheneOS, if you want or need to be completely independent of Apple or Google's cloud services.

### Aktiválási zár

Minden iOS-eszközt le kell ellenőrizni az Apple Activation Lock szerverein, amikor először beállítják vagy visszaállítják, ami azt jelenti, hogy az iOS-eszköz használatához internetkapcsolat **szükséges**.

### Kötelező App Store

The only source for apps on iOS is Apple's App Store, which requires an Apple Account to access. Ez azt jelenti, hogy az Apple nyilvántartást vezet minden egyes alkalmazásról, amelyet telepítesz a készülékedre, és valószínűleg össze tudja kapcsolni ezeket az információkat a tényleges személyazonosságoddal, ha megadsz egy fizetési módot az App Store-nak.

### Invazív telemetria

Apple has historically had problems with properly disassociating their telemetry from Apple Accounts on iOS. In [2019](https://theguardian.com/technology/2019/jul/26/apple-contractors-regularly-hear-confidential-details-on-siri-recordings), Apple was found to transmit Siri recordings—some containing highly confidential information—to their servers for manual review by third-party contractors. Though Apple temporarily stopped that program after that practice was [widely reported on](https://theverge.com/2019/8/23/20830120/apple-contractors-siri-recordings-listening-1000-a-day-globetech-microsoft-cortana), the company rolled out a switch to [**opt out** of uploading conversations with Siri](https://theguardian.com/technology/2019/oct/30/apple-lets-users-opt-out-of-having-siri-conversations-recorded) a few months later in the succeeding iOS update. Moreover, in 2021, [Apple reworked Siri](https://theguardian.com/technology/2021/jun/07/apple-overhauls-siri-to-address-privacy-concerns-and-improve-performance) so that it processes voice recordings locally rather than sending it to their servers.

More recently, Apple has been found to transmit analytics [even when analytics sharing is disabled](https://gizmodo.com/apple-iphone-analytics-tracking-even-when-off-app-store-1849757558) on iOS, and this data [appears](https://twitter.com/mysk_co/status/1594515229915979776) to be easily linked to unique iCloud account identifiers despite supposedly being decoupled from Apple Accounts.

### Traffic Outside Active VPN Connections

Apple's [privacy policy regarding VPNs](https://apple.com/legal/privacy/data/en/vpns) states:

> Even when a VPN is active, some traffic that is necessary for essential system services will take place outside the VPN so that your device can function properly.

## Ajánlott konfiguráció

**Note:** This guide assumes that you're running the latest version of iOS.

### iCloud

Az Apple termékeivel kapcsolatos adatvédelmi és biztonsági aggályok többsége a felhőszolgáltatásokkal kapcsolatos, nem pedig a hardverrel vagy szoftverrel. Amikor az Apple szolgáltatásait, például az iCloudot használod, a legtöbb adatodat a szervereiken tárolják, és olyan kulcsokkal védik, amelyekhez az Apple alapértelmezés szerint hozzáfér. Az [Apple dokumentációjában](https://support.apple.com/HT202303) tájékozódhatsz arról, hogy mely szolgáltatások végponttól végpontig titkosítottak. Bármi, ami "átvitel alatt", vagy a "szerveren" van, azt jelenti, hogy az Apple hozzáférhet ezekhez az adatokhoz a te engedélyed nélkül. A bűnüldöző szervek időnként visszaéltek ezzel a hozzáférési szinttel, hogy megkerüljék azt a tényt, hogy a felhasználói adatok egyébként biztonságosan titkosítva vannak az eszközön, valamint természetesen az Apple is ugyanúgy ki van téve az adatvédelmi incidenseknek, mint bármely más vállalat.

Ezért ha használod az iCloudot, [engedélyezd a **Speciális adatvédelmet**](https://support.apple.com/HT212520). Ez szinte az összes iCloud-adatot titkosítja az eszközökön tárolt kulcsokkal (végponttól-végpontig terjedő titkosítás), nem pedig az Apple szerverein, így az iCloud-adataid biztonságban lesznek egy esetleges adatsértés esetén, és egyébként rejtve maradnak az Apple elől.

The encryption used by Advanced Data Protection, while strong, [is not *quite* as robust](https://discuss.privacyguides.net/t/apple-advances-user-security-with-powerful-new-data-protections/10778/4) as the encryption offered by other [cloud services](../cloud.md), particularly when it comes to iCloud Drive. While we strongly encourage using Advanced Data Protection if you use iCloud, we would also suggest considering finding an alternative to iCloud from a more [privacy-focused service provider](../tools.md), although it is unlikely most people would be impacted by these encryption quirks.

You can also protect your data by limiting what you sync to iCloud in the first place. At the top of the **Settings** app, you'll see your name and profile picture if you are signed in to iCloud. Select that, then **iCloud**, and turn off the switches for any services you don't want to sync to iCloud. You may see third-party apps listed under **Show All** if they sync to iCloud, which you can disable here.

#### iCloud+

A paid **iCloud+** subscription (with any iCloud storage plan) comes with some privacy-protecting functionality. While these may provide adequate service for current iCloud customers, we wouldn't recommend purchasing an iCloud+ plan over a [VPN](../vpn.md) and [standalone email aliasing service](../email-aliasing.md) just for these features alone.

[**Private Relay**](https://apple.com/legal/privacy/data/en/icloud-relay) is a proxy service which relays all of your Safari traffic, your DNS queries, and unencrypted traffic on your device through two servers: one owned by Apple and one owned by a third-party provider (including Akamai, Cloudflare, and Fastly). In theory this should prevent any single provider in the chain—including Apple—from having full visibility into which websites you visit while connected. Unlike a VPN, Private Relay does not protect traffic that's already encrypted.

**Hide My Email** is Apple's email aliasing service. You can create an email aliases for free when you *Sign In With Apple* on a website or app, or generate unlimited aliases on demand with a paid iCloud+ plan. Hide My Email has the advantage of using the `@icloud.com` domain for its aliases, which may be less likely to be blocked compared to other email aliasing services, but does not offer functionality offered by standalone services such as automatic PGP encryption or multiple mailbox support.

#### Media & Purchases

At the top of the **Settings** app, you'll see your name and profile picture if you are signed in to an Apple Account. Select that, then select **Media & Purchases** → **View Account**.

- [ ] Turn off **Personalized Recommendations**

#### Lokátor

A **Lokátor** egy olyan szolgáltatás, amellyel nyomon követheted Apple-eszközeidet, és megoszthatod a tartózkodási helyedet barátaiddal és családtagjaiddal. Lehetővé teszi továbbá, hogy távolról töröld a készülékedet, ha ellopják, így megakadályozva, hogy a tolvaj hozzáférjen az adataidhoz. Your Find My [location data is E2EE](https://apple.com/legal/privacy/data/en/find-my) when:

- Your location is shared with a family member or friend, and you both use iOS 17 or greater.
- Your device is offline and is located by the Find My Network.

Your location data is not E2EE when your device is online and you use Find My iPhone remotely to locate your device. You will have to make the decision whether these trade-offs are worth the anti-theft benefits of Activation Lock.

At the top of the **Settings** app, you'll see your name and profile picture if you are signed in to an Apple Account. Select that, then select **Find My**. Here you can choose whether to enable or disable Find My location features.

### Settings

Many other privacy-related settings can be found in the **Settings** app.

#### Repülőgép üzemmód

A **repülőgépes üzemmód** engedélyezése megakadályozza, hogy a telefon kapcsolatba lépjen a mobiltornyokkal. Továbbra is képes leszel csatlakozni Wi-Fi-hez és a Bluetooth-hoz, így amikor Wi-Fi-hez csatlakozol, bekapcsolhatod ezt a beállítást.

#### Wi-Fi

You can enable [hardware address randomization](https://support.apple.com/en-us/102509#triswitch) to protect you from tracking across Wi-Fi networks, and on the same network over time. On the network you are currently connected to, tap the :material-information: button:

- [x] Set **Private Wi-Fi Address** to **Fixed** or **Rotating**

Lehetőséged van az **IP-címek nyomon követésének korlátozására** is. This is similar to iCloud Private Relay but only affects connections to "known trackers." Because it only affects connections to potentially malicious servers, this setting is probably fine to leave enabled, but if you don't want *any* traffic to be routed through Apple's servers, you should turn it off.

#### Bluetooth

**Bluetooth** should be disabled when you aren't using it as it increases your attack surface. Disabling Bluetooth (or Wi-Fi) via the Control Center only disables it temporarily: you must switch it off in Settings for disabling it to remain effective.

- [ ] Turn off **Bluetooth**

Note that Bluetooth is automatically turned on after every system update.

#### General

Your iPhone's device name will by default contain your first name, and this will be visible to anyone on networks you connect to. You should change this to something more generic, like "iPhone." Select **About** → **Name** and enter the device name you prefer.

It is important to install **Software Updates** frequently to get the latest security fixes. You can enable **Automatic Updates** to keep your phone up-to-date without needing to constantly check for updates. Select **Software Update** → **Automatic Updates**:

- [x] Turn on **Download iOS Updates**
- [x] Turn on **Install iOS Updates**
- [x] Turn on **Security Responses & System Files**

**AirDrop** is commonly used to easily share files, but it represents a significant privacy risk. The AirDrop protocol constantly broadcasts your personal information to your surroundings, with [very weak](https://usenix.org/system/files/sec21-heinrich.pdf) security protections. Your identity can easily be discovered by attackers even with limited resources, and the Chinese government has [openly acknowledged](https://arstechnica.com/security/2024/01/hackers-can-id-unique-apple-airdrop-users-chinese-authorities-claim-to-do-just-that) using such techniques to identify AirDrop users in public since 2022.

- [x] Select **AirDrop** → **Receiving Off**

**AirPlay** lets you seamlessly stream content from your iPhone to a TV; however, you might not always want this. Select **AirPlay & Continuity** → **Automatically AirPlay**:

- [x] Select **Never** or **Ask**

**Background App Refresh** allows your apps to refresh their content while you're not using them. This may cause them to make unwanted connections. Turning this off can also save battery life, but may affect an app's ability to receive updated information, particularly weather and messaging apps.

Select **Background App Refresh** and switch off any apps you don't want to continue refreshing in the background. If you don't want any apps to refresh in the background, you can select **Background App Refresh** again and turn it **Off**.

#### Siri & Search

If you don't want anyone to be able to control your phone with Siri when it is locked, you can turn that off here.

- [ ] Turn off **Allow Siri When Locked**

#### Face ID/Touch ID & Passcode

Setting a strong password on your phone is the most important step you can take for physical device security. You'll have to make trade-offs here between security and convenience: A longer password will be annoying to type in every time, but a shorter password or PIN will be easier to guess. Setting up Face ID or Touch ID along with a strong password can be a good compromise between usability and security.

Select **Turn Passcode On** or **Change Passcode** → **Passcode Options** → **Custom Alphanumeric Code**. Make sure that you create a [secure password](../basics/passwords-overview.md).

If you wish to use Face ID or Touch ID, you can go ahead and set it up now. Your phone will use the password you set up earlier as a fallback in case your biometric verification fails. Biometric unlock methods are primarily a convenience, although they do stop surveillance cameras or people over your shoulder from watching you input your passcode.

If you use biometrics, you should know how to turn them off quickly in an emergency. Holding down the side or power button and *either* volume button until you see the Slide to Power Off slider will disable biometrics, requiring your passcode to unlock. Your passcode will also be required after device restarts.

On some older devices, you may have to press the power button five times to disable biometrics instead, or for devices with Touch ID, you may just have to hold down the power button and nothing else. Make sure you try this in advance, so you know which method works for your device.

**Stolen Device Protection** adds additional security intended to protect your personal data if your device is stolen while unlocked. If you use biometrics and the Find My Device feature in your Apple Account settings, we recommend enabling this new protection:

- [x] Select **Turn On Protection**

After enabling Stolen Device Protection, [certain actions](https://support.apple.com/HT212510) will require biometric authentication without a password fallback (in the event that a shoulder surfer has obtained your PIN), such as using password autofill, accessing payment information, and disabling Lost Mode. It also adds a security delay to certain actions performed away from your home or another "familiar location," such as requiring a 1-hour timer to reset your Apple Account password or sign out of your Apple Account. This delay is intended to give you time to enable Lost Mode and secure your account before a thief can reset your device.

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

Az iPhone-ok már most is ellenállnak a brute-force támadásoknak, mivel több sikertelen próbálkozás után hosszú ideig kell várakoznia; azonban a múltban már voltak olyan megoldások, amelyekkel ezt meg lehetett kerülni. Az extra biztonság kedvéért beállíthatod, hogy a telefonod 10 sikertelen jelkódkísérlet után törölje magát.

<div class="admonition warning" markdown>
<p class="admonition-title">Figyelmeztetés</p>

Ha ezt a beállítást engedélyezed, valaki szándékosan törölheti a telefonodat azzal, ha többször rossz jelszót ír be. Győződj meg róla, hogy megfelelő biztonsági mentésekkel rendelkezel, és csak akkor engedélyezd ezt a beállítást, ha részedről ez a kockázat rendben van.

</div>

- [x] **Adatok törlésének** bekapcsolása

#### Privacy & Security

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
- [ ] Turn off **Improve Assistive Voice Features**
- [ ] Turn off **Improve AR Location Accuracy**

Disable **Personalized Ads** if you don't want targeted ads. Select **Apple Advertising**:

- [ ] Turn off **Personalized Ads**

**App Privacy Report** is a built-in tool that allows you to see which permissions your apps are using. Select **App Privacy Report**:

- [x] Select **Turn On App Privacy Report**

[Lockdown Mode](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode) is a security setting you can enable to make your phone more resistant to attacks. Be aware that certain apps and features [won't work](https://support.apple.com/HT212650) as they do normally.

- [x] Select **Turn On Lockdown Mode**

## Additional Advice

### Végponttól-végpontig titkosított hívások

A telefonszolgáltatón keresztül a Telefon alkalmazással kezdeményezett normál telefonhívások nincsenek végponttól-végpontig titkosítással védve. Both FaceTime Video and FaceTime Audio calls are E2EE. Alternatively, you can use [another app](../real-time-communication.md) like Signal for E2EE calls.

### Titkosított iMessage

The [color of the message bubble](https://support.apple.com/en-us/104972) in the Messages app indicates whether your messages are E2EE or not. A blue bubble indicates that you're using iMessage with E2EE, while a green bubble indicates the other party is using either the outdated SMS and MMS protocols or RCS. RCS on iOS is **not** E2EE. Currently, the only way to have E2EE in Messages is for both parties to be using iMessage on Apple devices.

If either you or your messaging partner have iCloud Backup enabled without Advanced Data Protection, the encryption key will be stored on Apple's servers, meaning they can access your messages. Additionally, iMessage's key exchange is not as secure as alternative implementations like Signal's (which allows you to view the recipients key and verify by QR code), so it shouldn't be relied on for particularly sensitive communications.

### Photo Permissions

When an app prompts you for access to your device's photo library, iOS provides you with options to limit what an app can access.

Rather than allow an app to access all the photos on your device, you can allow it to only access whichever photos you choose by tapping the "Select Photos..." option in the permission dialog. You can change photo access permissions at any time by navigating to **Settings** → **Privacy & Security** → **Photos**.

![Photo Permissions](../assets/img/ios/photo-permissions-light.png#only-light) ![Photo Permissions](../assets/img/ios/photo-permissions-dark.png#only-dark)

**Add Photos Only** is a permission that only gives an app the ability to download photos to the photo library. Not all apps which request photo library access provide this option.

![Private Access](../assets/img/ios/private-access-light.png#only-light) ![Private Access](../assets/img/ios/private-access-dark.png#only-dark)

Some apps also support **Private Access**, which functions similarly to the **Limited Access** permission. However, photos shared to apps using Private Access include their location by default. We recommend unchecking this setting if you do not [remove photo metadata](../data-redaction.md) beforehand.

### Contact Permissions

Similarly, rather than allow an app to access all the contacts saved on your device, you can allow it to only access whichever contacts you choose. You can change contact access permissions at any time by navigating to **Settings** → **Privacy & Security** → **Contacts**.

![Contact Permissions](../assets/img/ios/contact-permissions-light.png#only-light) ![Contact Permissions](../assets/img/ios/contact-permissions-dark.png#only-dark)

### Require Biometrics and Hide Apps

iOS offers the ability to lock most apps behind Touch ID/Face ID or your passcode, which can be useful for protecting sensitive content in apps which do not provide the option themselves. You can lock an app by long-pressing on it and selecting **Require Face ID/Touch ID**. Any app locked in this way requires biometric authentication whenever opening it or accessing its contents in other apps. Also, notification previews for locked apps will not be shown.

In addition to locking apps behind biometrics, you can also hide apps so that they don't appear on the Home Screen, App Library, the app list in **Settings**, etc. While hiding apps may be useful in situations where you have to hand your unlocked phone to someone else, the concealment provided by the feature is not absolute, as a hidden app is still visible in some places such as the battery usage list. Moreover, one notable trade off of hiding an app is that you will not receive any of its notifications.

You can hide an app by long-pressing on it and selecting **Require Face ID/Touch ID** → **Hide and Require Face ID/Touch ID**. Note that pre-installed Apple apps, as well as the default web browser and email app, cannot be hidden. Hidden apps reside in a **Hidden** folder at the bottom of the App Library, which can be unlocked using biometrics. This folder appears in the App Library whether you hid any apps or not, which provides you a degree of plausible deniability.

### Redacting Elements in Images

If you need to hide information in a photo, you can use Apple's built-in editing tools to do so.

If your device supports it, you can use the [Clean Up](https://support.apple.com/en-us/121429) feature to pixelate faces or remove objects from images.

- Open the **Photos** app and tap the photo you have selected for redaction
- Tap the :material-tune: (at the bottom of the screen)
- Tap the button labeled **Clean Up**
- Draw a circle around whatever you want to redact. Faces will be pixelated, and it will attempt to delete anything else.

Our warning [against blurring text](../data-redaction.md) also applies here, so we recommend to instead add a black shape with 100% opacity over it. In addition to redacting text, you can also black out any face or object using the **Photos** app.

- Tap the image you have selected for redaction
- Tap the :material-tune: (at the bottom of the screen) → markup symbol (top right) → plus icon at the bottom right
- Select **Add Shape** and choose the square or circle
- On the toolbar, tap the circle (left-most option) and choose black as the color for filling in the shape. You can also move the shape and increase its size as you see fit.

**Don't** use the highlighter to obfuscate information, as its opacity is not quite 100%.

### Avoid Jailbreaking

Az iPhone jailbreakelése aláássa a biztonságot, és sebezhetővé tesz téged. A nem megbízható, harmadik féltől származó szoftverek futtatása rosszindulatú szoftverekkel fertőzheti meg a készülékedet.

### iOS béták

Apple always makes beta versions of iOS available early for those that wish to help find and report bugs. We don't recommend installing beta software on your phone. Beta releases are potentially unstable and could have undiscovered security vulnerabilities.

## Biztonsági kiemelések

### Az első feloldás előtt

If your threat model includes [:material-target-account: Targeted Attacks](../basics/common-threats.md#attacks-against-specific-individuals ""){.pg-red} that involve forensic tools, and you want to minimize the chance of exploits being used to access your phone, you should restart your device frequently. The state *after* a reboot but *before* unlocking your device is referred to as "Before First Unlock" (BFU), and when your device is in that state it makes it [significantly more difficult](https://belkasoft.com/checkm8_glossary) for forensic tools to exploit vulnerabilities to access your data. This BFU state allows you to receive notifications for calls, texts, and alarms, but most of the data on your device is still encrypted and inaccessible. This can be impractical, so consider whether these trade-offs make sense for your situation.
