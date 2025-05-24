---
title: Android
description: デフォルトのAndroidにあるプライバシーを侵害する機能を、よりプライバシー性が高くて安全なもので置き換えるためのアドバイス。
icon: simple/android
cover: android.webp
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: Android Recommendations
    url: ./
  - "@context": http://schema.org
    "@type": CreativeWork
    name: Android
    image: /assets/img/android/android.svg
    url: https://source.android.com/
    sameAs: https://ja.wikipedia.org/wiki/Android_(%E3%82%AA%E3%83%9A%E3%83%AC%E3%83%BC%E3%83%86%E3%82%A3%E3%83%B3%E3%82%B0%E3%82%B7%E3%82%B9%E3%83%86%E3%83%A0)
---

![Androidのロゴ](../assets/img/android/android.svg){ align=right }

**Androidオープンソースプロジェクト** (AOSP)とは、Googleが手動するオープンソースのモバイル用オペレーティングシステムで、世界の半分以上のモバイルデバイスに使われています。 ほとんどのAndroidスマホは、Google Playサービスのようなプライバシーを侵害する機能・アプリが追加されています。そのため、デフォルトでインストールされているAndroidを、プライバシーを脅かす機能のないバージョンで置き換えることにより、プライバシーを大きく高めることができます。

[Androidの概観 :material-arrow-right-drop-circle:](../os/android-overview.md){ .md-button .md-button--primary }

## 私たちのアドバイス

### Googleのサービスを別のもので置き換えよう

AndroidでGoogle Playを使わずにアプリを入手する方法はたくさんあります。 プライバシー性の低いところから入手する前に、なるべく以下の方法で入手できるか試してみましょう：

[Obtaining Applications :material-arrow-right-drop-circle:](obtaining-apps.md){ .md-button }

カメラアプリなど、最初からスマホにインストールされているアプリについても、世の中にはよりプライバシー性の高いものがたくさん存在します。 本サイトの各ページでおすすめしているAndroidアプリ以外にも、便利なAndroid用システムユーティリティアプリのリストを以下で公開しています。

[General App Recommendations :material-arrow-right-drop-circle:](general-apps.md){ .md-button }

### カスタマイズされたディストリビューションをインストールしよう

Androidスマホを購入すると、Androidオープンソースプロジェクトに含まれないアプリや機能がデフォルトでOSに含まれた状態になっています。 このようなアプリは、電話アプリなどシステムの基本的な機能にあたるアプリでさえも、プライバシーを侵害する形でGoogle Playサービスと連携していることが多いです。そしてGoogle Playサービスがファイル、連絡先、ストレージ、通話履歴、SMSメッセージ、位置情報、カメラ、マイクなど、デバイス上のあらゆるものにアクセスする権限を要求します。権限を与えないと、こういった基本的なシステムアプリ含め多くのアプリがそもそも動作しません。 Google Playサービスのようなフレームワークは、攻撃対象領域を広げてしまうだけでなく、Androidにおけるプライバシー上の様々な懸念の原因でもあります。

この問題は、上記のようなプライバシーを侵害する機能のない、別のAndroidディストリビューション(_カスタムROM_と呼ばれることが多い)を使えば解決できます。 しかし残念ながら、多くのカスタムAndroidディストリビューションは、AVBや、ロールバック保護、ファームウェア・アップデートなどの重要なセキュリティ機能をサポートしておらず、しばしばAndroidのセキュリティーモデルに違反しています。 ディストリビューションによっては、[`userdebug`](https://source.android.com/setup/build/building#choose-a-target)ビルドが配布されています。このビルドでは、[ADB](https://developer.android.com/studio/command-line/adb)経由でrootにアクセスでき、さらにデバッグ機能に対応するためにSELinux ポリシーが緩められた状態になっており、結果、攻撃対象領域が増え、さらに弱いセキュリティモデルとなってしまっています。

Androidのカスタムディストリビューションを選択する場合には、Androidのセキュリティーモデルが維持されていることを確認してください。 最低限、ディストリビューションは本番用ビルドを使い、AVBやロールバック保護の対応、迅速なファームフェア・オペレーティングシステムのアップデート、SELinuxの[強制モード](https://source.android.com/security/selinux/concepts#enforcement_levels)の使用をするべきです。 以下のページで私たちが推奨しているAndroidディストリビューションはすべて、この基準を満たしています：

[推奨ディストリビューション :material-arrow-right-drop-circle:](distributions.md){ .md-button }

### root化を避けよう

Androidスマホを[root化](https://ja.wikipedia.org/wiki/Root%E5%8C%96_\(Android_OS\))すると、本来全体としてまとまっている[Androidセキュリティモデル](https://en.wikipedia.org/wiki/Android_\(operating_system\)#Security_and_privacy)を弱めることになるため、セキュリティを大幅に低下させる可能性があります。 root化によって低下したセキュリティーの脆弱性が悪用されると、プライバシーが損なわれてしまう可能性があります。 一般的な方法でroot化を行うと、ブートパーティションが直接変更されてしまうため、確認付きブートを行うことはできなくなります。 root権限が必要なアプリもシステムパーティションに変更を加えるため、確認付きブートを無効化せざるをえなくなります。 また、UI上でroot権限に直接アクセスできるようにしてしまうと、デバイスの攻撃対象領域が増加し、[権限昇格](https://en.wikipedia.org/wiki/Privilege_escalation)の脆弱性につながったり、SELinuxポリシーを回避されるおそれがあります。

[hostsファイル](https://ja.wikipedia.org/wiki/Hosts)を変更するコンテンツブロッカー(AdAwayなど)や、永続的にroot権限を必要とするファイアウォール(AFWall+など)は危険であり、使用を避けるべきです。 また、このようなアプリは、各目的を達成する方法として間違っています。 コンテンツブロッカーとしては、暗号化された[DNS](../dns.md)を使用するか、もしくはVPNに付随するコンテンツブロック機能を使用することを推奨します。 TrackerControlとAdAway は、非rootモードで使用すると(ローカルのループバック VPN を使用するため)VPNスロットを占有してしまうので、[Orbot](../alternative-networks.md#orbot)や[本当のVPN](../vpn.md)などのプライバシーを強化するサービスが使用できなくなります。

AFWall+は、[パケットフィルター](https://ja.wikipedia.org/wiki/%E3%83%95%E3%82%A1%E3%82%A4%E3%82%A2%E3%82%A6%E3%82%A9%E3%83%BC%E3%83%AB#%E3%83%91%E3%82%B1%E3%83%83%E3%83%88%E3%83%95%E3%82%A3%E3%83%AB%E3%82%BF%E5%9E%8B)の形で動作するため、環境によっては回避されてしまう可能性があります。

We do not believe that the security sacrifices made by rooting a phone are worth the questionable privacy benefits of those apps.

### Install Updates Regularly

It's important to not use an [end-of-life](https://endoflife.date/android) version of Android. Newer versions of Android receive not only security updates for the operating system but also important privacy enhancing updates too.

For example, [prior to Android 10](https://developer.android.com/about/versions/10/privacy/changes) any apps with the [`READ_PHONE_STATE`](https://developer.android.com/reference/android/Manifest.permission#READ_PHONE_STATE) permission could access sensitive and unique serial numbers of your phone such as [IMEI](https://en.wikipedia.org/wiki/International_Mobile_Equipment_Identity), [MEID](https://en.wikipedia.org/wiki/Mobile_equipment_identifier), or your SIM card's [IMSI](https://en.wikipedia.org/wiki/International_mobile_subscriber_identity); whereas now they must be system apps to do so. System apps are only provided by the OEM or Android distribution.

### Use Built-in Sharing Features

Androidに内蔵された共有機能を使えば、多くのアプリにメディアへのアクセス許可を与える必要がなくなります。 多くのアプリでは、メディアをアップロードするためにファイルを「共有」することができます。

例えば、Discordに写真を投稿したい場合は、Discordにメディアや写真へのフルアクセスを許可する代わりに、ファイルマネージャーやギャラリーを開いて、その写真を Discord アプリと共有できます。
