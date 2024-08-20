---
title: Android Overview
icon: simple/android
description: Android is an open-source operating system with strong security protections, which makes it our top choice for phones.
robots: nofollow, max-snippet:-1, max-image-preview:large
---

![安卓徽标](../assets/img/android/android.svg){ align=right }

The **Android Open Source Project** is a secure mobile operating system featuring strong [app sandboxing](https://source.android.com/security/app-sandbox), [Verified Boot](https://source.android.com/security/verifiedboot) (AVB), and a robust [permission](https://developer.android.com/guide/topics/permissions/overview) control system.

## Our Advice

### 挑选安卓 ROM

When you buy an Android phone, the default operating system comes bundled with apps and functionality that are not part of the Android Open Source Project. Many of these apps—even apps like the dialer which provide basic system functionality—require invasive integrations with Google Play Services, which in turn asks for privileges to access your files, contacts storage, call logs, SMS messages, location, camera, microphone, and numerous other things on your device in order for those basic system apps and many other apps to function in the first place. Frameworks like Google Play Services increase the attack surface of your device and are the source of various privacy concerns with Android.

换用一个不预装这类软件的安卓 ROM 可以解决这个问题。 不巧，很多安卓 ROM 不支持 AVB、回滚保护、系统更新、等这些关键的安全功能，破坏了安卓的安全模型。 某些 ROM 发布的版本属于 [`userdebug`](https://source.android.com/setup/build/building#choose-a-target) 构建版本。这个版本通过 [ADB](https://developer.android.com/studio/command-line/adb) 来提供 root 访问，并且为了支持调试，[放宽](https://github.com/LineageOS/android_system_sepolicy/search?q=userdebug&type=code)了 SELinux 规则。这进一步扩大了攻击面，弱化了安全模型。

在挑选安卓 ROM 时，理想的情况，是能找到坚持安卓安全模型的 ROM。 最起码的是，你选用的 ROM 应该提供生产版本（而非 `userdebug`版本）的构建，能支持 AVB、回滚保护、按时推送系统更新、把 SELinux 设为[强制模式](https://source.android.com/security/selinux/concepts#enforcement_levels)。 我们推荐的所有安卓 ROM 都满足上述标准。

[我们推荐的安卓 ROM :material-arrow-right-drop-circle:](../android/distributions.md ""){.md-button}

### 避免 Root

[Rooting](https://en.wikipedia.org/wiki/Rooting_(Android)) 安卓手机会大大降低安全性，因为它削弱了完整的 [安卓安全模型](https://en.wikipedia.org/wiki/Android_(operating_system)#Security_and_privacy)。 如果有一个被降低的安全性所帮助的漏洞，这可能会减少隐私。 常见的root方法涉及直接篡改启动分区，使得它不可能成功地进行验证性启动。 Apps that require root will also modify the system partition, meaning that Verified Boot would have to remain disabled. 在用户界面上直接暴露root也增加了你的设备的 [攻击面](https://en.wikipedia.org/wiki/Attack_surface) ，并可能有助于 [特权升级](https://en.wikipedia.org/wiki/Privilege_escalation) 漏洞和SELinux政策的绕过。

Content blockers which modify the [hosts file](https://en.wikipedia.org/wiki/Hosts_(file)) (AdAway) and firewalls (AFWall+) which require root access persistently are dangerous and should not be used. 它们也不是解决其预期目的的正确方法。 For content blocking, we suggest encrypted [DNS](../dns.md) or content blocking functionality provided by a VPN instead. TrackerControl and AdAway in non-root mode will take up the VPN slot (by using a local loopback VPN), preventing you from using privacy enhancing services such as [Orbot](../tor.md#orbot) or a [real VPN provider](../vpn.md).

AFWall+基于 [包过滤](https://en.wikipedia.org/wiki/Firewall_(computing)#Packet_filter) 方法工作，在某些情况下可能会被绕过。

我们认为，通过root手机所做的安全牺牲不值得那些应用程序的可疑隐私利益。

### Install Updates

重要的是，不要使用 [报废的](https://endoflife.date/android) 版本的Android。 Newer versions of Android receive not only security updates for the operating system but also important privacy enhancing updates too.

For example, [prior to Android 10](https://developer.android.com/about/versions/10/privacy/changes) any apps with the [`READ_PHONE_STATE`](https://developer.android.com/reference/android/Manifest.permission#READ_PHONE_STATE) permission could access sensitive and unique serial numbers of your phone such as [IMEI](https://en.wikipedia.org/wiki/International_Mobile_Equipment_Identity), [MEID](https://en.wikipedia.org/wiki/Mobile_equipment_identifier), or your SIM card's [IMSI](https://en.wikipedia.org/wiki/International_mobile_subscriber_identity); whereas now they must be system apps to do so. 系统应用只由OEM或安卓发行提供。

### Sharing Media

You can avoid giving many apps permission to access your media with Android's built-in sharing features. Many applications allow you to "share" a file with them for media upload.

For example, if you want to post a picture to Discord you can open your file manager or gallery and share that picture with the Discord app, instead of granting Discord full access to your media and photos.

## Security Protections

Key components of the Android security model include [verified boot](#verified-boot), [firmware updates](#firmware-updates), and a robust [permission system](#android-permissions). These important security features form the baseline of the minimum criteria for our [mobile phone](../mobile-phones.md) and [custom Android OS](../android/distributions.md) recommendations.

### 已验证的启动

[**Verified Boot**](https://source.android.com/security/verifiedboot) is an important part of the Android security model. 它能够保护您免受 [罪恶的](https://en.wikipedia.org/wiki/Evil_maid_attack) 攻击、恶意软件的持久性，并确保安全更新不能用 [回滚保护降级](https://source.android.com/security/verifiedboot/verified-boot#rollback-protection)

安卓10及以上版本已经从全盘加密转向更灵活的 [基于文件的加密](https://source.android.com/security/encryption/file-based)。 你的数据使用独特的加密密钥进行加密，而操作系统文件则不被加密。

验证启动确保了操作系统文件的完整性，从而防止有物理访问权限的对手在设备上篡改或安装恶意软件。 在不太可能的情况下，如果恶意软件能够利用系统的其他部分并获得更高的特权访问，验证性启动将防止并在重启设备时恢复对系统分区的更改。

遗憾的是，OEM厂商只有在其库存的安卓系统上才有义务支持验证性启动。 只有少数OEM厂商，如谷歌，支持在他们的设备上定制AVB密钥注册。 此外，一些AOSP衍生产品，如LineageOS或/e/ OS，即使在对第三方操作系统有验证启动支持的硬件上也不支持验证启动。 我们建议你在</strong> 购买新设备之前，先查看支持 **。 不支持验证性启动的AOSP衍生产品是 **，不推荐**。</p>

许多原始设备制造商也有破碎的实施验证启动，你必须注意他们的营销之外。 例如，Fairphone 3和4在默认情况下是不安全的，因为 [股票引导程序信任公共AVB签名密钥](https://forum.fairphone.com/t/bootloader-avb-keys-used-in-roms-for-fairphone-3-4/83448/11)。 This breaks verified boot on a stock Fairphone device, as the system will boot alternative Android operating systems (such as /e/) [without any warning](https://source.android.com/security/verifiedboot/boot-flow#locked-devices-with-custom-root-of-trust) about custom operating system usage.

### 固件更新

**Firmware updates** are critical for maintaining security and without them your device cannot be secure. 原始设备制造商与他们的合作伙伴有支持协议，在有限的支持期内提供闭源组件。 这些内容详见每月的 [Android安全公告](https://source.android.com/security/bulletin)。

由于手机的组件，如处理器和无线电技术依赖于闭源组件，更新必须由各自的制造商提供。 因此，重要的是，你要在一个有效的支持周期内购买设备。 [Qualcomm](https://www.qualcomm.com/news/releases/2020/12/qualcomm-and-google-announce-collaboration-extend-android-os-support-and) and [Samsung](https://news.samsung.com/us/samsung-galaxy-security-extending-updates-knox) support their devices for 4 years, while cheaper products often have shorter support cycles. With the introduction of the [Pixel 6](https://support.google.com/pixelphone/answer/4457705), Google now makes their own SoC, and they will provide a minimum of 5 years of support. With the introduction of the Pixel 8 series, Google increased that support window to 7 years.

不再受SoC制造商支持的EOL设备无法从OEM供应商或后市场Android分销商处获得固件更新。 这意味着这些设备的安全问题将继续得不到解决。

Fairphone, for example, markets their Fairphone 4 device as receiving 6 years of support. 然而，SoC（Fairphone 4上的高通骁龙750G）的EOL日期要短得多。 这意味着高通公司为Fairphone 4提供的固件安全更新将在2023年9月结束，无论Fairphone是否继续发布软件安全更新。

### Android 权限

[**Permissions on Android**](https://developer.android.com/guide/topics/permissions/overview) grant you control over what apps are allowed to access. 谷歌定期在每个连续的版本中对权限系统进行 [改善](https://developer.android.com/about/versions/11/privacy/permissions)。 你安装的所有应用程序都是严格的 [沙箱](https://source.android.com/security/app-sandbox)，因此，没有必要安装任何杀毒软件。

A smartphone with the latest version of Android will always be more secure than an old smartphone with an antivirus that you have paid for. It's better not to pay for antivirus software and to save money to buy a new smartphone such as a [Google Pixel](../mobile-phones.md#google-pixel).

Android 10:

- [Scoped Storage](https://developer.android.com/about/versions/10/privacy/changes#scoped-storage) gives you more control over your files and can limit what can [access external storage](https://developer.android.com/training/data-storage#permissions). Apps can have a specific directory in external storage as well as the ability to store specific types of media there.
- Tighter access on [device location](https://developer.android.com/about/versions/10/privacy/changes#app-access-device-location) by introducing the `ACCESS_BACKGROUND_LOCATION` permission. This prevents apps from accessing the location when running in the background without express permission from the user.

Android 11:

- [One-time permissions](https://developer.android.com/about/versions/11/privacy/permissions#one-time) which allows you to grant a permission to an app just once.
- [Auto-reset permissions](https://developer.android.com/about/versions/11/privacy/permissions#auto-reset), which resets [runtime permissions](https://developer.android.com/guide/topics/permissions/overview#runtime) that were granted when the app was opened.
- Granular permissions for accessing [phone number](https://developer.android.com/about/versions/11/privacy/permissions#phone-numbers) related features.

Android 12:

- A permission to grant only the [approximate location](https://developer.android.com/about/versions/12/behavior-changes-12#approximate-location).
- Auto-reset of [hibernated apps](https://developer.android.com/about/versions/12/behavior-changes-12#app-hibernation).
- [Data access auditing](https://developer.android.com/about/versions/12/behavior-changes-12#data-access-auditing) which makes it easier to determine what part of an app is performing a specific type of data access.

Android 13:

- A permission for [nearby Wi-Fi access](https://developer.android.com/about/versions/13/behavior-changes-13#nearby-wifi-devices-permission). The MAC addresses of nearby Wi-Fi access points were a popular way for apps to track a user's location.
- More [granular media permissions](https://developer.android.com/about/versions/13/behavior-changes-13#granular-media-permissions), meaning you can grant access to images, videos or audio files only.
- Background use of sensors now requires the [`BODY_SENSORS`](https://developer.android.com/about/versions/13/behavior-changes-13#body-sensors-background-permission) permission.

An app may request a permission for a specific feature it has. For example, any app that can scan QR codes will require the camera permission. Some apps can request more permissions than they need.

[Exodus](https://exodus-privacy.eu.org) can be useful when comparing apps that have similar purposes. If an app requires a lot of permissions and has a lot of advertising and analytics this is probably a bad sign. We recommend looking at the individual trackers and reading their descriptions rather than simply **counting the total** and assuming all items listed are equal.

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

If an app is mostly a web-based service, the tracking may occur on the server side. [Facebook](https://reports.exodus-privacy.eu.org/en/reports/com.facebook.katana/latest) shows "no trackers" but certainly does track users' interests and behavior across the site. Apps may evade detection by not using standard code libraries produced by the advertising industry, though this is unlikely.

</div>

<div class="admonition note" markdown>
<p class="admonition-title">Note</p>

Privacy-friendly apps such as [Bitwarden](https://reports.exodus-privacy.eu.org/en/reports/com.x8bit.bitwarden/latest) may show some trackers such as [Google Firebase Analytics](https://reports.exodus-privacy.eu.org/en/trackers/49). This library includes [Firebase Cloud Messaging](https://en.wikipedia.org/wiki/Firebase_Cloud_Messaging) which can provide [push notifications](https://en.wikipedia.org/wiki/Push_technology) in apps. This [is the case](https://fosstodon.org/@bitwarden/109636825700482007) with Bitwarden. That doesn't mean that Bitwarden is using all of the analytics features that are provided by Google Firebase Analytics.

</div>

## Privacy Features

### 用户资料

多个用户配置文件可以在 **设置** → **系统** → **多个用户** ，是Android中最简单的隔离方式。

通过用户个人资料，你可以对一个特定的个人资料施加限制，如：打电话、使用短信或在设备上安装应用程序。 每个用户资料使用自己的加密密钥进行加密，不能访问任何其他人的个人资料。 即使是设备所有者，如果不知道他们的密码，也不能查看其他人的个人资料。 多个个人资料是一种更安全的隔离方法。

### 工作身份

[工作配置文件](https://support.google.com/work/android/answer/6191949) 是隔离单个应用程序的另一种方式，可能比单独的用户配置文件更方便。

A **device controller** app such as [Shelter](../android/general-apps.md#shelter) is required to create a Work Profile without an enterprise MDM, unless you're using a custom Android OS which includes one.

该工作档案依赖于设备控制器来运作。 诸如 *文件穿梭* 和 *接触搜索封锁* 或任何种类的隔离功能必须由控制器实现。 You must also fully trust the device controller app, as it has full access to your data inside the work profile.

这种方法通常不如二级用户配置文件安全；但是，它确实允许你在工作和个人配置文件中同时运行应用程序的便利。

### VPN Killswitch

Android 7 and above supports a VPN kill switch, and it is available without the need to install third-party apps. 如果VPN断开连接，此功能可以防止泄漏。 可以在 :gear: **设置** → **网络 & 互联网** → **VPN** → :gear: → **阻止没有VPN的连接**。

### 全局切换

现代安卓设备有全局切换键，用于禁用蓝牙和定位服务。 安卓12引入了相机和麦克风的切换功能。 在不使用时，我们建议禁用这些功能。 Apps cannot use disabled features (even if granted individual permissions) until re-enabled.

## Google Services

If you are using a device with Google services—whether with the stock operating system or an operating system that safely sandboxes Google Play Services like GrapheneOS—there are a number of additional changes you can make to improve your privacy. 我们仍然建议完全避免使用谷歌服务，或者通过将 *Shelter* 等设备控制器与GrapheneOS的沙盒化谷歌游戏结合起来，将谷歌游戏服务限制在特定的用户/工作档案中。

### 高级保护计划

If you have a Google account we suggest enrolling in the [Advanced Protection Program](https://landing.google.com/advancedprotection). 任何拥有两个或更多支持 [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online) 的硬件安全密钥的人都可以免费使用。 Alternatively, you can use [passkeys](https://fidoalliance.org/passkeys).

高级保护计划提供增强的威胁监控，并支持：

- Stricter two-factor authentication; e.g. that [FIDO](../basics/multi-factor-authentication.md#fido-fast-identity-online) **must** be used and disallows the use of [SMS OTPs](../basics/multi-factor-authentication.md#sms-or-email-mfa), [TOTP](../basics/multi-factor-authentication.md#time-based-one-time-password-totp) and [OAuth](https://en.wikipedia.org/wiki/OAuth)
- 只有谷歌和经过验证的第三方应用程序可以访问账户数据
- 在 Gmail 帐户上扫描收到的邮件以进行 [钓鱼](https://en.wikipedia.org/wiki/Phishing#Email_phishing) 尝试
- Stricter [safe browser scanning](https://google.com/chrome/privacy/whitepaper.html#malware) with Google Chrome
- 对丢失凭证的账户有更严格的恢复程序

 If you use non-sandboxed Google Play Services (common on stock operating systems), the Advanced Protection Program also comes with [additional benefits](https://support.google.com/accounts/answer/9764949) such as:

- Not allowing app installation outside the Google Play Store, the OS vendor's app store, or via [`adb`](https://en.wikipedia.org/wiki/Android_Debug_Bridge)
- Mandatory automatic device scanning with [Play Protect](https://support.google.com/googleplay/answer/2812853?#zippy=%2Chow-malware-protection-works%2Chow-privacy-alerts-work)
- 警告你有未经验证的应用程序

### Google Play 系统更新

在过去，安卓系统的安全更新必须由操作系统供应商来提供。 从安卓10开始，安卓变得更加模块化，谷歌可以通过特权游戏服务推送安全更新， **一些** 系统组件。

如果你有一个以安卓10或以上系统出厂的EOL设备，并且无法在你的设备上运行我们推荐的任何操作系统，你很可能最好坚持使用你的OEM安卓安装（而不是这里没有列出的操作系统，如LineageOS或/e/ OS）。 这将允许你从谷歌获得 **，一些** 安全修复，同时不会因为使用不安全的安卓衍生产品而违反安卓安全模式，增加你的攻击面。 我们仍然建议尽快升级到支持的设备。

### 广告 ID

All devices with Google Play Services installed automatically generate an [advertising ID](https://support.google.com/googleplay/android-developer/answer/6048248) used for targeted advertising. 禁用此功能以限制收集到的关于你的数据。

在带有 [Sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play)的安卓发行上，进入 :gear: **设置** → **应用程序** → **Sandboxed Google Play** → **谷歌设置** → **广告**，并选择 *删除广告 ID*。

在拥有特权的谷歌游戏服务的安卓发行版上（如股票操作系统），该设置可能在几个位置之一。 查看

- :gear: **设置** → **谷歌** → **广告**
- :gear: **设置** → **隐私** → **广告**

You will either be given the option to delete your advertising ID or to *Opt out of interest-based ads* (this varies between OEM distributions of Android). If presented with the option to delete the advertising ID, that is preferred. 如果没有，那么请确保选择退出并重新设置你的广告ID。

### SafetyNet和Play Integrity API

[安全网](https://developer.android.com/training/safetynet/attestation) 和 [Play Integrity APIs](https://developer.android.com/google/play/integrity) ，一般用于 [银行应用程序](https://grapheneos.org/usage#banking-apps)。 许多银行应用程序在GrapheneOS中使用沙盒游戏服务可以正常工作，但是一些非金融应用程序有自己的粗略防篡改机制，可能会失败。 GrapheneOS通过了 `basicIntegrity` 检查，但没有通过认证检查 `ctsProfileMatch`。 安卓8或更高版本的设备有硬件认证支持，如果没有泄露的密钥或严重的漏洞，就无法绕过。

As for Google Wallet, we don't recommend this due to their [privacy policy](https://payments.google.com/payments/apis-secure/get_legal_document?ldo=0&ldt=privacynotice&ldl=en), which states you must opt out if you don't want your credit rating and personal information shared with affiliate marketing services.
