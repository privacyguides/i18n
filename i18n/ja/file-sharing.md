---
title: "ファイル共有と同期"
icon: material/share-variant
description: デバイス間や、友人や家族、または匿名でオンライン上でファイルをプライベートに共有する方法をご紹介します。
cover: file-sharing.webp
---

デバイス間、友人や家族、または匿名でオンライン上でファイルをプライベートに共有する方法をご紹介します。

## ファイル共有ソフト

### Send

!!! recommendation

    ![Send logo](assets/img/file-sharing-sync/send.svg){ align=right }
    
    **Send**は、Mozillaの廃止されたFirefox Sendサービスのフォークで、リンクを使って他の人にファイルを送ることができます。 ファイルはサーバーから読み取れないようにデバイス上で暗号化され、オプションでパスワードで保護することもできます。 Sendの保守管理者はは[public instance](https://send.vis.ee/)をホストしています。 他の公開インスタンスを使うこともできるし、Sendを自分でホストすることもできます。
    
    [:octicons-home-16: Homepage](https://send.vis.ee){ .md-button .md-button--primary }
    [:octicons-server-16:](https://github.com/timvisee/send-instances){ .card-link title="Public Instances"}
    [:octicons-info-16:](https://github.com/timvisee/send#readme){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/timvisee/send){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://github.com/sponsors/timvisee){ .card-link title=Contribute }

SendはWeb上、または[ffsendコマンド](https://github.com/timvisee/ffsend)CLI から使用できる。 コマンドラインに慣れていて頻繁にファイルを送信する場合は、JavaScriptベースの暗号化を避けるためにCLIクライアントを使用することをお勧めします。 `--host` フラグを指定すると、特定のサーバーを使用することができます:

```bash
ffsend upload --host https://send.vis.ee/ FILE
```

### OnionShare

!!! recommendation

    ![OnionShare logo](assets/img/file-sharing-sync/onionshare.svg){ align=right }
    
    **OnionShare**は、あらゆるサイズのファイルを安全かつ匿名で共有できるオープンソースツールです。 Torオニオン・サービスとしてアクセス可能なウェブサーバーを起動し、受信者と共有可能な推測不可能なURLでファイルをダウンロードまたは送信することで機能します。
    
    [:octicons-home-16: Homepage](https://onionshare.org){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://lldan5gahapx5k7iafb3s4ikijc4ni7gx5iywdflkba5y2ezyg6sjgyd.onion){ .card-link title="Onion Service" }
    [:octicons-info-16:](https://docs.onionshare.org){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/onionshare/onionshare){ .card-link title="Source Code" }
    
    ??? ダウンロード
    
        - [:simple-windows11: Windows](https://onionshare.org/#download)
        - [:simple-apple: macOS](https://onionshare.org/#download)
        - [:simple-linux: Linux](https://onionshare.org/#download)

### 基準

**私たちが推薦するどのプロジェクトとも提携していないことにご留意ください。** [](about/criteria.md)に加え、客観的な推薦を提供できるよう、明確な要件を定めています。 プロジェクトを利用する前に、このリストをよく理解し、あなたにとって正しい選択であることを確認するために、ご自身で調査を行うことをお勧めします。

!!! example "この項目は最近作成されました"

    私たちは、サイトの各項目に定義された基準を確立することに取り組んでおり、これは変更される可能性があります。 私たちの基準についてご質問がある場合は、[フォーラムでお尋ねください](https://discuss.privacyguides.net/latest)。また、ここに記載されていないものを、私たちが推薦する際に考慮しなかったと決めつけないでください。 プロジェクトをおすすめする際に考慮され、議論される要素は多くあり、すべてを文書化するには時間がかかります。

- 復号化したデータをリモートサーバーに保存してはならない。
- オープンソースのソフトウェアであること。
- Linux、macOS、Windows用のクライアントを持つか、ウェブインターフェースを持つ必要がある。

## FreedomBox

!!! recommendation

    ![FreedomBox logo](assets/img/file-sharing-sync/freedombox.svg){ align=right }
    
    **FreedomBox**は、[シングルボードコンピュータ(SBC)](https://ja.wikipedia.org/wiki/%E3%82%B7%E3%83%B3%E3%82%B0%E3%83%AB%E3%83%9C%E3%83%BC%E3%83%89%E3%82%B3%E3%83%B3%E3%83%94%E3%83%A5%E3%83%BC%E3%82%BF)上で動作するように設計されたオペレーティングシステムです。 目的は、自己ホストしたいと思うかもしれないサーバーアプリケーションを簡単に設定できるようにすることです。
    
    [:octicons-home-16: Homepage](https://freedombox.org){ .md-button .md-button--primary }
    [:octicons-info-16:](https://wiki.debian.org/FreedomBox/Manual){ .card-link title=Documentation}
    [:octicons-code-16:](https://salsa.debian.org/freedombox-team/freedombox){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://freedomboxfoundation.org/donate/){ .card-link title=Contribute }

## ファイル同期ソフト

### Nextcloud(Client-Server)

!!! recommendation

    ![Nextcloud logo](assets/img/productivity/nextcloud.svg){ align=right }
    **Nextcloud**は、フリーでオープンソースのクライアント・サーバーソフトウェアのスイートです。
    
    [:octicons-home-16: Homepage](https://nextcloud.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://nextcloud.com/privacy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://nextcloud.com/support/){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/nextcloud){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://nextcloud.com/contribute/){ .card-link title=Contribute } ダウンロード
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.nextcloud.client)
        - [:simple-appstore: App Store](https://apps.apple.com/app/id1125420102)
        - [:simple-github: GitHub](https://github.com/nextcloud/android/releases)
        - [:simple-windows11: Windows](https://nextcloud.com/install/#install-clients)
        - [:simple-apple: macOS](https://nextcloud.com/install/#install-clients)
        - [:simple-linux: Linux](https://nextcloud.com/install/#install-clients)

!!! 警告

    [E2EEアプリ](https://apps.nextcloud.com/apps/end_to_end_encryption) for Nextcloudの使用は、データ損失の可能性があるため、お勧めしません。

### Syncthing (P2P)

!!! recommendation

    ![Syncthing logo](assets/img/file-sharing-sync/syncthing.svg){ align=right }
    
    **Syncthing**はオープンソースのピアツーピア連続ファイル同期ユーティリティです。 これは、ローカルネットワークまたはインターネットを介し、2つ以上のデバイス間でファイルを同期するために使用されます。 Syncthingは中央集中型のサーバーを使用せず、[Block Exchange Protocol](https://docs.syncthing.net/specs/bep-v1.html#bep-v1)を使用してデバイス間のデータ転送を行います。 すべてのデータはTLSにより暗号化されます。
    
    [:octicons-home-16: Homepage](https://syncthing.net){ .md-button .md-button--primary }
    [:octicons-info-16:](https://docs.syncthing.net){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/syncthing){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://syncthing.net/donations/){ .card-link title=Contribute }
    
    ??? ダウンロード
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.nutomic.syncthingandroid)
        - [:simple-windows11: Windows](https://syncthing.net/downloads/)
        - [:simple-apple: macOS](https://syncthing.net/downloads/)
        - [:simple-linux: Linux](https://syncthing.net/downloads/)
        - [:simple-freebsd: FreeBSD](https://syncthing.net/downloads/)

### 基準

**私たちが推薦するどのプロジェクトとも提携していないことにご留意ください。** [](about/criteria.md)に加え、客観的な推薦を提供できるよう、明確な要件を定めています。 プロジェクトを利用する前に、このリストをよく理解し、あなたにとって正しい選択であることを確認するために、ご自身で調査を行うことをお勧めします。

!!! example "この項目は最近作成されました"

    私たちは、サイトの各項目に定義された基準を確立することに取り組んでおり、これは変更される可能性があります。 私たちの基準についてご質問がある場合は、[フォーラムでお尋ねください](https://discuss.privacyguides.net/latest)。また、ここに記載されていないものを、私たちが推薦する際に考慮しなかったと決めつけないでください。 プロジェクトをおすすめする際に考慮され、議論される要素は多くあり、すべてを文書化するには時間がかかります。

#### 最低要件

- サードパーティのリモート/クラウドサーバーを必要としないこと。
- オープンソースのソフトウェアであること。
- Linux、macOS、Windows用のクライアントを持つか、ウェブインターフェースを持つ必要がある。

#### 満たされることが望ましい基準

私たちのベストケース基準は、このカテゴリーの完璧なプロジェクトに私たちが望むものを表している。 私たちのおすすめは、この機能の一部または全部を含んでいないかもしれませんが、もし含んでいるものがあれば、このページで他のものよりも上位にランクされるかもしれません。

- iOSとAndroid用のモバイルクライアントがあり、少なくともドキュメントのプレビューをサポートしている。
- iOSとAndroidからの写真のバックアップをサポートし、オプションでAndroid上のファイル/フォルダの同期をサポートします。
