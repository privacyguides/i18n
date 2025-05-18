---
meta_title: 一番良いAndroidのオペレーティングシステム - Privacy Guides
title: 別のディストリビューション
description: 本記事で紹介する安全かつプライバシー重視のOSで自分のAndroidスマホのOSを置き換えることができます。
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: プライバシー重視のAndroid OS
    url: ./
  - "@context": http://schema.org
    "@type": CreativeWork
    name: GrapheneOS
    image: /assets/img/android/grapheneos.svg
    url: https://grapheneos.org/
    sameAs: https://ja.wikipedia.org/wiki/GrapheneOS
    subjectOf:
      "@context": http://schema.org
      "@type": WebPage
      url: ./
robots: nofollow, max-snippet:-1, max-image-preview:large
---

<small>以下の脅威から保護します：</small>

- [:material-target-account: 標的型攻撃](../basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: パッシブ攻撃](../basics/common-threats.md#security-and-privacy){ .pg-orange }

**AndroidをベースにしたカスタムのOS** (**カスタムROM**と呼ばれることがあります) を自分のデバイスで使えば、プライバシーとセキュリティのレベルを高めることができます。 これは、工場出荷時に搭載される「純正」バージョンのAndroidとは異なるものです。純正バージョンでは、Google Playサービスや他ベンダーのソフトウェアが、OSと密接に連携する形で組み込まれていることが多いです。

Google Pixelを使用している人は、セキュリティが強化され、追加のプライバシー機能を備えているGrapheneOSをインストールすることを推奨します。 他のOSやデバイスを紹介しない理由は以下の通りです：

- [セキュリティが弱い](index.md#install-a-custom-distribution)ことが多い。
- 開発者が興味を失ったり別にデバイスに乗り換えたりして、サポートが終わってしまうということが頻繁に起きる。対照的に、GrapheneOSの[サポート期間](https://grapheneos.org/faq#device-lifetime)はいつ終わるか予測しやすい。
- これといったプライバシーやセキュリティの改善がほとんどなく、インストールする価値がない。

## GrapheneOS

<div class="admonition recommendation" markdown>

![GrapheneOS logo](../assets/img/android/grapheneos.svg#only-light){ align=right }
![GrapheneOS logo](../assets/img/android/grapheneos-dark.svg#only-dark){ align=right }

**GrapheneOS**は、プライバシーとセキュリティにおいては一番良い選択肢です。

GrapheneOSでは、[セキュリティが強化（ハードニング）](https://ja.wikipedia.org/wiki/%E3%83%8F%E3%83%BC%E3%83%89%E3%83%8B%E3%83%B3%E3%82%B0)され、プライバシーが改善されています。 It has a [hardened memory allocator](https://github.com/GrapheneOS/hardened_malloc), network and sensor permissions, and various other [security features](https://grapheneos.org/features). GrapheneOS also comes with full firmware updates and signed builds, so verified boot is fully supported.

[:octicons-home-16: Homepage](https://grapheneos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://grapheneos.org/faq#privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://grapheneos.org/faq){ .card-link title=Documentation}
[:octicons-code-16:](https://grapheneos.org/source){ .card-link title="Source Code" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribute }

</div>

GrapheneOS supports [sandboxed Google Play](https://grapheneos.org/usage#sandboxed-google-play), which runs Google Play Services fully sandboxed like any other regular app. This means you can take advantage of most Google Play Services, such as push notifications, while giving you full control over their permissions and access, and while containing them to a specific [work profile](../os/android-overview.md#work-profile) or [user profile](../os/android-overview.md#user-profiles) of your choice.

[Google Pixel phones](../mobile-phones.md#google-pixel) are the only devices that currently meet GrapheneOS's [hardware security requirements](https://grapheneos.org/faq#future-devices).

By default, Android makes many network connections to Google to perform DNS connectivity checks, to sync with current network time, to check your network connectivity, and for many other background tasks. GrapheneOS replaces these with connections to servers operated by GrapheneOS and subject to their privacy policy. This hides information like your IP address [from Google](../basics/common-threats.md#privacy-from-service-providers), but means it is trivial for an admin on your network or ISP to see you are making connections to `grapheneos.network`, `grapheneos.org`, etc. and deduce what operating system you are using.

If you want to hide information like this from an adversary on your network or ISP, you **must** use a [trusted VPN](../vpn.md) in addition to changing the connectivity check setting to **Standard (Google)**. It can be found in :gear: **Settings** → **Network & internet** → **Internet connectivity checks**. This option allows you to connect to Google's servers for connectivity checks, which, alongside the usage of a VPN, helps you blend in with a larger pool of Android devices.

## 規準

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](../about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. プロジェクトを利用する前に、このリストをよく理解し、ご自身で調査を行って、そのプロジェクトがあなたにとって適切な選択かどうかをご確認ください。

- オープンソースのソフトウェアであること。
- Must support bootloader locking with custom AVB key support.
- Must receive major Android updates within 0-1 months of release.
- Must receive Android feature updates (minor version) within 0-14 days of release.
- Must receive regular security patches within 0-5 days of release.
- Must **not** be "rooted" out of the box.
- Must **not** enable Google Play Services by default.
- Must **not** require system modification to support Google Play Services.
