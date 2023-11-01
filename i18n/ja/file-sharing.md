---
title: "ファイル共有と同期"
icon: material/share-variant
description: デバイス間や、友人や家族、または匿名でオンライン上でファイルをプライベートに共有する方法をご紹介します。
cover: file-sharing.webp
---

デバイス間、友人や家族、または匿名でオンライン上でファイルをプライベートに共有する方法をご紹介します。

## ファイル共有

### Send

!!! recommendation

    ![Send logo](assets/img/file-sharing-sync/send.svg){ align=right }
    
    **Send**は、Mozillaの廃止されたFirefox Sendサービスのフォークで、リンクを使って他の人にファイルを送ることができます。 ファイルはサーバーから読み取れないようにデバイス上で暗号化され、オプションでパスワードで保護することもできます。 Sendの保守管理者は[公開インスタンス](https://send.vis.ee/)をホストしています。 他の公開インスタンスを使うこともできますし、Sendを自分でホストすることもできます。
    
    [:octicons-home-16: Homepage](https://send.vis.ee){ .md-button .md-button--primary }
    [:octicons-server-16:](https://github.com/timvisee/send-instances){ .card-link title="公開インスタンス"}
    [:octicons-info-16:](https://github.com/timvisee/send#readme){ .card-link title=ドキュメンテーション}
    [:octicons-code-16:](https://github.com/timvisee/send){ .card-link title="ソースコード" }
    [:octicons-heart-16:](https://github.com/sponsors/timvisee){ .card-link title=貢献 }

SendはWebインターフェース上、または[ffsend](https://github.com/timvisee/ffsend)によるコマンドラインインターフェース上で使うことができます。 コマンドラインに慣れており、頻繁にファイルを送信する場合は、JavaScriptベースの暗号化を避けるためにCLIクライアントを使用することを推奨します。 `--host`フラグを指定すると、特定のサーバーを使用することができます。

```bash
ffsend upload --host https://send.vis.ee/ FILE
```

### OnionShare

!!! recommendation

    ![OnionShare ロゴ](assets/img/file-sharing-sync/onionshare.svg){ align=right }
    
    **OnionShare**は、あらゆるサイズのファイルを安全かつ匿名で共有できるオープンソースのツールです。 Torオニオン・サービスとしてアクセスできるウェブサーバーを起動し、ファイルのダウンロードまたは送信に用いられる、推測不可能なURLをファイルの受信者と共有するという形で機能します。
    
    [:octicons-home-16: Homepage](https://onionshare.org){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://lldan5gahapx5k7iafb3s4ikijc4ni7gx5iywdflkba5y2ezyg6sjgyd.onion){ .card-link title="Onionサービス" }
    [:octicons-info-16:](https://docs.onionshare.org){ .card-link title=ドキュメンテーション}
    [:octicons-code-16:](https://github.com/onionshare/onionshare){ .card-link title="ソースコード" }
    
    ??? ダウンロード
    
        - [:simple-windows11: Windows](https://onionshare.org/#download)
        - [:simple-apple: macOS](https://onionshare.org/#download)
        - [:simple-linux: Linux](https://onionshare.org/#download)

### 規準

**私たちは、推薦するどのプロジェクトとも提携していません。**客観的に推薦できるよう、[標準となる基準](about/criteria.md)に加えて、一連の明確な要件を定めています。 プロジェクトを利用する前に、このリストをよく理解し、ご自身で調査を行って、そのプロジェクトがあなたにとって適切な選択かどうかをご確認ください。

!!! example "この項目は最近作成されました"

    私たちは、サイトの各項目に定義された基準を確立することに取り組んでいます。この基準は変更される可能性があります。 私たちの基準について疑問がある場合は、[フォーラムで質問](https://discuss.privacyguides.net/latest)してください。また、ここに記載されていない場合でも、私たちがプロジェクトを推奨する際に、そうした事柄を考慮しなかったと仮定するのはお止めください。 プロジェクトを推奨する際に考慮され、議論される要素は多くあり、そのすべてを文書化する作業は現在進行中です。

- 復号化したデータをリモートサーバーに保存しないこと。
- オープンソースのソフトウェアであること。
- Linux、macOS、Windows用のクライアントがあるか、ウェブインターフェースが備わっていること。

## FreedomBox

!!! recommendation

    ![FreedomBox ロゴ](assets/img/file-sharing-sync/freedombox.svg){ align=right }
    
    **FreedomBox**は、[シングルボードコンピュータ（SBC）](https://ja.wikipedia.org/wiki/%E3%82%B7%E3%83%B3%E3%82%B0%E3%83%AB%E3%83%9C%E3%83%BC%E3%83%89%E3%82%B3%E3%83%B3%E3%83%94%E3%83%A5%E3%83%BC%E3%82%BF)上で動作するように設計されたオペレーティングシステムです。 目的は、自身でホストしたいサーバーアプリケーションを簡単に立ち上げられるようにすることです。
    
    [:octicons-home-16: Homepage](https://freedombox.org){ .md-button .md-button--primary }
    [:octicons-info-16:](https://wiki.debian.org/FreedomBox/Manual){ .card-link title=ドキュメンテーション}
    [:octicons-code-16:](https://salsa.debian.org/freedombox-team/freedombox){ .card-link title="ソースコード" }
    [:octicons-heart-16:](https://freedomboxfoundation.org/donate/){ .card-link title=貢献 }

## ファイル同期

### Nextcloud（クライアント・サーバー間）

!!! recommendation

    ![Nextcloud ロゴ](assets/img/productivity/nextcloud.svg){ align=right }
    
    **Nextcloud**は、自由でオープンソースのクライアント・サーバーソフトウェアのスイートです。あなた自身が管理する非公開のサーバーでファイルホスティングサービスを構築するのに使用できます。
    
    [:octicons-home-16: Homepage](https://nextcloud.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://nextcloud.com/privacy){ .card-link title="プライバシーポリシー" }
    [:octicons-info-16:](https://nextcloud.com/support/){ .card-link title=ドキュメンテーション}
    [:octicons-code-16:](https://github.com/nextcloud){ .card-link title="ソースコード" }
    [:octicons-heart-16:](https://nextcloud.com/contribute/){ .card-link title=貢献 } ダウンロード
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.nextcloud.client)
        - [:simple-appstore: App Store](https://apps.apple.com/app/id1125420102)
        - [:simple-github: GitHub](https://github.com/nextcloud/android/releases)
        - [:simple-windows11: Windows](https://nextcloud.com/install/#install-clients)
        - [:simple-apple: macOS](https://nextcloud.com/install/#install-clients)
        - [:simple-linux: Linux](https://nextcloud.com/install/#install-clients)

!!! 警告

    Nextcloudでの[E2EEアプリ](https://apps.nextcloud.com/apps/end_to_end_encryption)の使用は、データ損失の可能性があるため、推奨されません。

### Syncthing（P2P）

!!! recommendation

    ![Syncthing ロゴ](assets/img/file-sharing-sync/syncthing.svg){ align=right }
    
    **Syncthing**はオープンソースのピアツーピア連続ファイル同期ユーティリティです。 ローカルネットワークまたはインターネットを介し、2つ以上のデバイス間でファイルを同期することができます。 Syncthingは中央集権型のサーバーを使用せず、[Block Exchange Protocol](https://docs.syncthing.net/specs/bep-v1.html#bep-v1)を使用してデバイス間のデータ転送を行います。 すべてのデータはTLSにより暗号化されます。
    
    [:octicons-home-16: Homepage](https://syncthing.net){ .md-button .md-button--primary }
    [:octicons-info-16:](https://docs.syncthing.net){ .card-link title=ドキュメンテーション}
    [:octicons-code-16:](https://github.com/syncthing){ .card-link title="ソースコード" }
    [:octicons-heart-16:](https://syncthing.net/donations/){ .card-link title=貢献 }
    
    ??? ダウンロード
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.nutomic.syncthingandroid)
        - [:simple-windows11: Windows](https://syncthing.net/downloads/)
        - [:simple-apple: macOS](https://syncthing.net/downloads/)
        - [:simple-linux: Linux](https://syncthing.net/downloads/)
        - [:simple-freebsd: FreeBSD](https://syncthing.net/downloads/)

### 規準

**私たちは、推薦するどのプロジェクトとも提携していません。**客観的に推薦できるよう、[標準となる基準](about/criteria.md)に加えて、一連の明確な要件を定めています。 プロジェクトを利用する前に、このリストをよく理解し、ご自身で調査を行って、そのプロジェクトがあなたにとって適切な選択かどうかをご確認ください。

!!! example "この項目は最近作成されました"

    私たちは、サイトの各項目に定義された基準を確立することに取り組んでいます。この基準は変更される可能性があります。 私たちの基準について疑問がある場合は、[フォーラムで質問](https://discuss.privacyguides.net/latest)してください。また、ここに記載されていない場合でも、私たちがプロジェクトを推奨する際に、そうした事柄を考慮しなかったと仮定するのはお止めください。 プロジェクトを推奨する際に考慮され、議論される要素は多くあり、そのすべてを文書化する作業は現在進行中です。

#### 最低要件

- サードパーティのリモート/クラウドサーバーを必要としないこと。
- オープンソースのソフトウェアであること。
- Linux、macOS、Windows用のクライアントを持つか、ウェブインターフェースを備えていること。

#### 満たされることが望ましい基準

満たされることが望ましい基準には、このカテゴリーの完璧なプロジェクトに私たちが望むものを示しています。 私たちが推薦するプロジェクトは、この機能の一部または全部を含んでいないかもしれませんが、もし含んでいれば、このページで他のプロジェクトよりも上位にランクされるかもしれません。

- iOSとAndroid用のモバイルクライアントがあり、少なくともドキュメントのプレビューをサポートしていること。
- iOSとAndroidからの写真のバックアップをサポートしており、オプションでAndroid上のファイル/フォルダの同期をサポートしていること。
