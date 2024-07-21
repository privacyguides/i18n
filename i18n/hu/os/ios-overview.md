---
title: iOS áttekintés
icon: simple/apple
description: Az iOS egy mobil operációs rendszer, amelyet az Apple fejlesztett ki az iPhone-okra.
---

Az **iOS** és az **iPadOS** az Apple által az iPhone és az iPad termékekhez kifejlesztett saját mobil operációs rendszerek. Ha rendelkezel egy Apple mobil eszközzel, növelheted a magánéletedet a beépített telemetria funkciók kikapcsolásával, valamint néhány adatvédelmi és biztonsági beállítás megerősítésével, amelyek be vannak építve a rendszerbe.

## Adatvédelmi megjegyzés

iOS devices are frequently praised by security experts for their robust data protection and adherence to modern best practices. Azonban az Apple zárt ökoszisztémájának korlátozó volta – különösen a mobil eszközök esetében – továbbra is számos módon hátráltatja a magánélet védelmét.

Általánosságban úgy véljük, hogy az iOS a legtöbb ember számára az átlagosnál jobb adatvédelmi és biztonsági védelmet nyújt, mint a bármelyik gyártótól származó Android készülékek. However, you can achieve even higher standards of privacy with a [custom Android operating system](../android/distributions.md#aosp-derivatives) like GrapheneOS, if you want or need to be completely independent of Apple or Google's cloud services.

### Aktiválási zár

Minden iOS-eszközt le kell ellenőrizni az Apple Activation Lock szerverein, amikor először beállítják vagy visszaállítják, ami azt jelenti, hogy az iOS-eszköz használatához internetkapcsolat **szükséges**.

### Kötelező App Store

Az iOS-en az alkalmazások egyetlen forrása az Apple App Store, amelyhez Apple ID szükséges. Ez azt jelenti, hogy az Apple nyilvántartást vezet minden egyes alkalmazásról, amelyet telepítesz a készülékedre, és valószínűleg össze tudja kapcsolni ezeket az információkat a tényleges személyazonosságoddal, ha megadsz egy fizetési módot az App Store-nak.

### Invazív telemetria

Az Apple-nek korábban is voltak problémái telemetria megfelelő anonimizálásával az iOS-en. [2019-ben](https://theguardian.com/technology/2019/jul/26/apple-contractors-regularly-hear-confidential-details-on-siri-recordings) kiderült, hogy az Apple a Siri felvételeit – amelyek némelyike rendkívül bizalmas információkat tartalmazott – továbbította a szervereire, hogy azt harmadik fél szerződött vállalkozók kézzel vizsgálják felül. Bár átmenetileg leállították ezt a programot, miután [széles körben beszámoltak](https://theverge.com/2019/8/23/20830120/apple-contractors-siri-recordings-listening-1000-a-day-globetech-microsoft-cortana) erről a gyakorlatról, a probléma [2021-ig](https://theguardian.com/technology/2021/jun/07/apple-overhauls-siri-to-address-privacy-concerns-and-improve-performance) nem oldódott meg teljesen.

A közelmúltban kiderült, hogy az Apple [még akkor is továbbítja az analitikai adatokat, ha az](https://gizmodo.com/apple-iphone-analytics-tracking-even-when-off-app-store-1849757558) iOS-en az analitikai megosztás ki van kapcsolva, és [úgy tűnik,](https://twitter.com/mysk_co/status/1594515229915979776) hogy ezek az adatok könnyen összekapcsolhatók az iCloud-fiók egyedi azonosítóival, annak ellenére, hogy állítólag névtelenek.

## Ajánlott konfiguráció

### iCloud

Az Apple termékeivel kapcsolatos adatvédelmi és biztonsági aggályok többsége a felhőszolgáltatásokkal kapcsolatos, nem pedig a hardverrel vagy szoftverrel. Amikor az Apple szolgáltatásait, például az iCloudot használod, a legtöbb adatodat a szervereiken tárolják, és olyan kulcsokkal védik, amelyekhez az Apple alapértelmezés szerint hozzáfér. Az [Apple dokumentációjában](https://support.apple.com/HT202303) tájékozódhatsz arról, hogy mely szolgáltatások végponttól végpontig titkosítottak. Bármi, ami "átvitel alatt", vagy a "szerveren" van, azt jelenti, hogy az Apple hozzáférhet ezekhez az adatokhoz a te engedélyed nélkül. A bűnüldöző szervek időnként visszaéltek ezzel a hozzáférési szinttel, hogy megkerüljék azt a tényt, hogy a felhasználói adatok egyébként biztonságosan titkosítva vannak az eszközön, valamint természetesen az Apple is ugyanúgy ki van téve az adatvédelmi incidenseknek, mint bármely más vállalat.

Ezért ha használod az iCloudot, [engedélyezd a **Speciális adatvédelmet**](https://support.apple.com/HT212520). Ez szinte az összes iCloud-adatot titkosítja az eszközökön tárolt kulcsokkal (végponttól-végpontig terjedő titkosítás), nem pedig az Apple szerverein, így az iCloud-adataid biztonságban lesznek egy esetleges adatsértés esetén, és egyébként rejtve maradnak az Apple elől.

The encryption used by Advanced Data Protection, while strong, [is not *quite* as robust](https://discuss.privacyguides.net/t/apple-advances-user-security-with-powerful-new-data-protections/10778/4) as the encryption offered by other [cloud services](../cloud.md), particularly when it comes to iCloud Drive. While we strongly encourage using Advanced Data Protection if you use iCloud, we would also suggest considering finding an alternative to iCloud from a more [privacy-focused service provider](../tools.md), although it is unlikely most people would be impacted by these encryption quirks.

You can also protect your data by limiting what you sync to iCloud in the first place. At the top of the **Settings** app, you'll see your name and profile picture if you are signed in to iCloud. Select that, then **iCloud**, and turn off the switches for any services you don't want to sync to iCloud. You may see third-party apps listed under **Show All** if they sync to iCloud, which you can disable here.

#### iCloud+

A paid **iCloud+** subscription (with any iCloud storage plan) comes with some privacy-protecting functionality. While these may provide adequate service for current iCloud customers, we wouldn't recommend purchasing an iCloud+ plan over a [VPN](../vpn.md) and [standalone email aliasing service](../email-aliasing.md) just for these features alone.

**Private Relay** is a proxy service which relays your Safari traffic through two servers: one owned by Apple and one owned by a third-party provider (including Akamai, Cloudflare, and Fastly). In theory this should prevent any single provider in the chain—including Apple—from having full visibility into which websites you visit while connected. Unlike a full VPN, Private Relay does not protect traffic from your apps outside of Safari.

**Hide My Email** is Apple's email aliasing service. You can create an email aliases for free when you *Sign In With Apple* on a website or app, or generate unlimited aliases on demand with a paid iCloud+ plan. Hide My Email has the advantage of using the `@icloud.com` domain for its aliases, which may be less likely to be blocked compared to other email aliasing services, but does not offer functionality offered by standalone services such as automatic PGP encryption or multiple mailbox support.

#### Media & Purchases

At the top of the **Settings** app, you'll see your name and profile picture if you are signed in to an Apple ID. Select that, then select **Media & Purchases** > **View Account**.

- [ ] Turn off **Personalized Recommendations**

#### Lokátor

A **Lokátor** egy olyan szolgáltatás, amellyel nyomon követheted Apple-eszközeidet, és megoszthatod a tartózkodási helyedet barátaiddal és családtagjaiddal. Lehetővé teszi továbbá, hogy távolról töröld a készülékedet, ha ellopják, így megakadályozva, hogy a tolvaj hozzáférjen az adataidhoz. Your Find My [location data is E2EE](https://apple.com/legal/privacy/data/en/find-my) when:

- Your location is shared with a family member or friend, and you both use iOS 17 or greater.
- Your device is offline and is located by the Find My Network.

Your location data is not E2EE when your device is online and you use Find My iPhone remotely to locate your device. You will have to make the decision whether these trade-offs are worth the anti-theft benefits of Activation Lock.

At the top of the **Settings** app, you'll see your name and profile picture if you are signed in to an Apple ID. Select that, then select **Find My**. Here you can choose whether to enable or disable Find My location features.

### Settings

Many other privacy-related settings can be found in the **Settings** app.

#### Repülőgép üzemmód

A **repülőgépes üzemmód** engedélyezése megakadályozza, hogy a telefon kapcsolatba lépjen a mobiltornyokkal. Továbbra is képes leszel csatlakozni Wi-Fi-hez és a Bluetooth-hoz, így amikor Wi-Fi-hez csatlakozol, bekapcsolhatod ezt a beállítást.

#### Wi-Fi

A Wi-Fi hálózatokon keresztüli nyomon követés elleni védelem érdekében engedélyezheted a hardvercímek véletlenszerűségét. Az aktuálisan csatlakoztatott hálózatk megtekintéséhez kattints a :material-information: gombra:

- [x] **Privát Wi-Fi cím** bekapcsolása

Lehetőséged van az **IP-címek nyomon követésének korlátozására** is. This is similar to iCloud Private Relay but only affects connections to "known trackers." Because it only affects connections to potentially malicious servers, this setting is probably fine to leave enabled, but if you don't want *any* traffic to be routed through Apple's servers, you should turn it off.

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

Disable **Personalized Ads** if you don't want targeted ads. Select **Apple Advertising**:

- [ ] Turn off **Personalized Ads**

**App Privacy Report** is a built-in tool that allows you to see which permissions your apps are using. Select **App Privacy Report**:

- [x] Select **Turn On App Privacy Report**

[Lockdown Mode](https://blog.privacyguides.org/2022/10/27/macos-ventura-privacy-security-updates/#lockdown-mode) is a security setting you can enable to make your phone more resistant to attacks. Be aware that certain apps and features [won't work](https://support.apple.com/HT212650) as they do normally.

- [x] Select **Turn On Lockdown Mode**

## Additional Advice

### Végponttól-végpontig titkosított hívások

A telefonszolgáltatón keresztül a Telefon alkalmazással kezdeményezett normál telefonhívások nincsenek végponttól-végpontig titkosítással védve. A FaceTime Video éw a FaceTime Audio hívások végponttól-végpontig titkosítottak, de használhatsz helyettük [egy másik alkalmazást](../real-time-communication.md), például a Signal-t.

### Avoid Jailbreaking

Az iPhone jailbreakelése aláássa a biztonságot, és sebezhetővé tesz téged. A nem megbízható, harmadik féltől származó szoftverek futtatása rosszindulatú szoftverekkel fertőzheti meg a készülékedet.

### Titkosított iMessage

The color of the message bubble in the Messages app indicates whether your messages are E2EE or not. A blue bubble indicates that you're using iMessage with E2EE, while a green bubble indicates the other party is using the outdated SMS and MMS protocols. Currently, the only way to get E2EE in Messages is for both parties to be using iMessage on Apple devices.

If either you or your messaging partner have iCloud Backup enabled without Advanced Data Protection, the encryption key will be stored on Apple's servers, meaning they can access your messages. Additionally, iMessage's key exchange is not as secure as alternative implementations, like Signal (which allows you to view the recipients key and verify by QR code), so it shouldn't be relied on for particularly sensitive communications.

### Arcok/információk elsötétítése

If you need to hide information in a photo, you can use Apple's built-in tools to do so. Open the photo you want to edit, press edit in the top right corner of the screen, then press the markup symbol at the top right. Press the plus at the bottom right of the screen, then press the rectangle icon. Now, you can place a rectangle anywhere on the image. Make sure to press the shape icon at the bottom left and select the filled-in rectangle. **Don't** use the highlighter to obfuscate information, because its opacity is not quite 100%.

### iOS béták

Apple always makes beta versions of iOS available early for those that wish to help find and report bugs. We don't recommend installing beta software on your phone. Beta releases are potentially unstable and could have undiscovered security vulnerabilities.

## Biztonsági kiemelések

### Az első feloldás előtt

If your threat model includes forensic tools and you want to minimize the chance of exploits being used to access your phone, you should restart your device frequently. The state *after* a reboot but *before* unlocking your device is referred to as "Before First Unlock" (BFU), and when your device is in that state it makes it [significantly more difficult](https://belkasoft.com/checkm8_glossary) for forensic tools to exploit vulnerabilities to access your data. This BFU state allows you to receive notifications for calls, texts, and alarms, but most of the data on your device is still encrypted and inaccessible. This can be impractical, so consider whether these trade-offs make sense for your situation.
