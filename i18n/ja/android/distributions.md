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

![GrapheneOSのロゴ](../assets/img/android/grapheneos.svg#only-light){ align=right }
![GrapheneOSのロゴ](../assets/img/android/grapheneos-dark.svg#only-dark){ align=right }

**GrapheneOS**は、プライバシーとセキュリティにおいては一番良い選択肢です。

GrapheneOSでは、[セキュリティが強化（ハードニング）](https://ja.wikipedia.org/wiki/%E3%83%8F%E3%83%BC%E3%83%89%E3%83%8B%E3%83%B3%E3%82%B0)され、プライバシーが改善されています。 [ハードニングされたメモリアロケータ](https://github.com/GrapheneOS/hardened_malloc)、ネットワークとセンサーの権限管理機能、その他のさまざまな[セキュリティ機能](https://grapheneos.org/features)を備えています。 さらに、ファームウェアアップデートがすべて含まれ、ビルドも署名付きのため、セキュアブートに完全対応しています。

[:octicons-home-16: ホームページ](https://grapheneos.org){ .md-button .md-button--primary }
[:octicons-eye-16:](https://grapheneos.org/faq#privacy-policy){ .card-link title="プライバシーポリシー" }
[:octicons-info-16:](https://grapheneos.org/faq){ .card-link title=ドキュメント}
[:octicons-code-16:](https://grapheneos.org/source){ .card-link title="ソースコード" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=支援 }

</div>

GrapheneOSでは、[サンドボックス化されたGoogle Play](https://grapheneos.org/usage#sandboxed-google-play)を使うことができます。これは、Google Playサービスを他のアプリと同じように完全にサンドボックス化して実行するものです。 サンドボックス化により、プッシュ通知などほとんどのGoogle Playサービスが利用可能でありながら、Playサービスの権限やアクセスを完全に制御することができ、また、自由に特定の[仕事用プロファイル](../os/android-overview.md#work-profile)や[ユーザープロファイル](../os/android-overview.md#user-profiles)の中に隔離することができます。

現在、GrapheneOSの[ハードウェアセキュリティ要件](https://grapheneos.org/faq#future-devices)を満たすデバイスは、[Google Pixelスマートフォン](../mobile-phones.md#google-pixel)のみです。

デフォルトでAndroidは、DNS接続確認やネットワーク現在時刻の同期、ネットワーク接続確認など、色々なバックグラウンドタスクのために、Googleに頻繁にネットワーク接続を行います。 GrapheneOSでは、この通信先がGrapheneOSが運営するサーバーに変更されます。この通信は、GrapheneOSのプライバシーポリシーに従って管理されます。 これにより、あなたのIPアドレスなどの情報が[Googleから](../basics/common-threats.md#privacy-from-service-providers)見えなくなりますが、逆にネットワーク管理者やISPからは、あなたが`grapheneos.network`や`grapheneos.org`などに接続しているのが観測できるため、GrapheneOSを使用していることが容易に推測できてしまいます。

使用しているネットワークやISPに存在する敵対者からこのような情報を守りたい場合は、接続確認設定を**Standard (Google)**に変更することに加えて、[信頼できるVPN](../vpn.md)を使用することが**必須**となります。 このオプションは :gear: **設定** → **ネットワークとインターネット** → **Internet connectivity checks**にあります。 このオプションを選ぶことで、Googleのサーバーに対して接続確認するようになり、VPNと組み合わせれば、より大きなAndroidデバイスのグループの中に紛れ込むことができます。

## 規準

\*\*私たちは、推薦するどのプロジェクトとも提携していません。\*\*客観的に推薦できるよう、[標準となる規準](../about/criteria.md)に加えて、一連の明確な要件を定めています。 プロジェクトを利用する前に、このリストをよく理解し、ご自身で調査を行って、そのプロジェクトがあなたにとって適切な選択かどうかをご確認ください。

- オープンソースのソフトウェアであること。
- Must support bootloader locking with custom AVB key support.
- Androidのメジャーアップデートがリリースされてから１ヶ月以内に配信していること。
- Androidのマイナーアップデートがリリースされてから14日以内に配信していること。
- セキュリティアップデートがリリースされてから5日以内に配信していること。
- デフォルトで「ルート化」されていないこと。
- デフォルトでGoogle Playサービスが有効化されていないこと。
- Google Playサービスを有効化するのに、システムへの変更を加える必要がないこと。
