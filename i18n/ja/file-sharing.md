---
title: ファイル共有と同期
icon: material/share-variant
description: デバイス間、友人や家族、または匿名でオンライン上でファイルをプライベートに共有する方法をご紹介します。
cover: file-sharing.webp
---

<small>Protects against the following threat(s):</small>

- [:material-server-network:サービスプロバイダー](basics/common-threats.md#privacy-from-service-providers ""){.pg-teal}

デバイス間、友人や家族、または匿名でオンライン上でファイルをプライベートに共有する方法をご紹介します。

## ファイル共有

If you already use [Proton Drive](cloud.md#proton-drive)[^1] or have a [Bitwarden](passwords.md#bitwarden) Premium[^2] subscription, consider using the file sharing capabilities that they each offer, both of which use end-to-end encryption. Otherwise, the standalone options listed here ensure that the files you share are not read by a remote server.

### Send

<div class="admonition recommendation" markdown>

![Send logo](assets/img/file-sharing-sync/send.svg){ align=right }

**Send**は、廃止されたMozilla Firefox Sendサービスのフォークで、リンクを使って他の人にファイルを送ることができます。 ファイルはサーバーから読み取れないようにデバイス上で暗号化され、オプションでパスワードで保護することもできます。 Sendのメンテナーは[公開インスタンス](https://send.vis.ee)をホストしています。 他の公開インスタンスを使うこともできますし、Sendを自分でホストすることもできます。

[:octicons-home-16: Homepage](https://send.vis.ee){ .md-button .md-button--primary }
[:octicons-server-16:](https://github.com/timvisee/send-instances){ .card-link title="Public Instances"}
[:octicons-info-16:](https://github.com/timvisee/send#readme){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/timvisee/send){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/sponsors/timvisee){ .card-link title="Contribute" }

</details>

</div>

SendはWebインターフェース上、または[ffsend](https://github.com/timvisee/ffsend)によるコマンドラインインターフェース上で使うことができます。 コマンドラインに慣れており、頻繁にファイルを送信する場合は、JavaScriptベースの暗号化を避けるためにCLIクライアントを使用することを推奨します。 `--host`フラグを指定すると、特定のサーバーを使用することができます。

```bash
ffsend upload --host https://send.vis.ee/ FILE
```

### OnionShare

<div class="admonition recommendation" markdown>

![OnionShare logo](assets/img/file-sharing-sync/onionshare.svg){ align=right }

**OnionShare** is an open-source tool that lets you securely and [:material-incognito: anonymously](basics/common-threats.md#anonymity-vs-privacy){ .pg-purple } share a file of any size. Torオニオン・サービスとしてアクセスできるウェブサーバーを起動し、ファイルのダウンロードまたは送信に用いられる、推測不可能なURLをファイルの受信者と共有するという形で機能します。

[:octicons-home-16: Homepage](https://onionshare.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://lldan5gahapx5k7iafb3s4ikijc4ni7gx5iywdflkba5y2ezyg6sjgyd.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://docs.onionshare.org){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/onionshare/onionshare){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://onionshare.org/#download)
- [:simple-apple: macOS](https://onionshare.org/#download)
- [:simple-linux: Linux](https://onionshare.org/#download)
- [:simple-flathub: Flathub](https://flathub.org/apps/org.onionshare.OnionShare)

</details>

</div>

OnionShare provides the option to connect via [Tor bridges](https://docs.onionshare.org/2.6.2/en/tor.html#automatic-censorship-circumvention) to circumvent [:material-close-outline: Censorship](basics/common-threats.md#avoiding-censorship ""){.pg-blue-gray}.

### 規準

**私たちは、推薦するどのプロジェクトとも提携していません。**客観的に推薦できるよう、[標準となる規準](about/criteria.md)に加えて、一連の明確な要件を定めています。 プロジェクトを利用する前に、このリストをよく理解し、ご自身で調査を行って、そのプロジェクトがあなたにとって適切な選択かどうかをご確認ください。

- 復号化したデータをリモートサーバーに保存しないこと。
- オープンソースのソフトウェアであること。
- Linux、macOS、Windows用のクライアントがあるか、ウェブインターフェースが備わっていること。

## ファイル同期

### Syncthing（P2P）

<div class="admonition recommendation" markdown>

![Syncthing ロゴ](assets/img/file-sharing-sync/syncthing.svg){ align=right }

**Syncthing**はオープンソースのピアツーピア連続ファイル同期ユーティリティです。 ローカルネットワークまたはインターネットを介し、2つ以上のデバイス間でファイルを同期することができます。 Syncthingは中央集権型のサーバーを使用せず、[Block Exchange Protocol](https://docs.syncthing.net/specs/bep-v1.html#bep-v1)を使用してデバイス間のデータ転送を行います。 すべてのデータはTLSにより暗号化されます。

[:octicons-home-16: ホームページ](https://syncthing.net){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.syncthing.net){ .card-link title=ドキュメント}
[:octicons-code-16:](https://github.com/syncthing){ .card-link title="ソースコード" }
[:octicons-heart-16:](https://syncthing.net/donations){ .card-link title=貢献 }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://syncthing.net/downloads)
- [:simple-apple: macOS](https://syncthing.net/downloads)
- [:simple-linux: Linux](https://syncthing.net/downloads)
- [:simple-freebsd: FreeBSD](https://syncthing.net/downloads)

</details>

</div>

### 規準

**私たちは、推薦するどのプロジェクトとも提携していません。**客観的に推薦できるよう、[標準となる規準](about/criteria.md)に加えて、一連の明確な要件を定めています。 プロジェクトを利用する前に、このリストをよく理解し、ご自身で調査を行って、そのプロジェクトがあなたにとって適切な選択かどうかをご確認ください。

#### 最低要件

- サードパーティのリモート/クラウドサーバーを必要としないこと。
- オープンソースのソフトウェアであること。
- Linux、macOS、Windows用のクライアントがあるか、ウェブインターフェースが備わっていること。

#### 満たされることが望ましい基準

満たされることが望ましい基準には、このカテゴリーの完璧なプロジェクトに私たちが望むものを示しています。 私たちが推薦するプロジェクトは、この機能の一部または全部を含んでいないかもしれませんが、もし含んでいれば、このページで他のプロジェクトよりも上位にランクされるかもしれません。

- Should have mobile clients for iOS and Android which at least support document previews.
- Should support photo backups from iOS and Android, and optionally support file/folder sync on Android.

[^1]: Proton Drive allows you to [share files or folders](https://proton.me/support/drive-shareable-link) by generating a shareable public link or sending a unique link to a designated email address. Public links can be protected with a password, set to expire, and completely revoked, while links shared via email can have custom permissions and be similarly revoked. Per Proton Drive's [privacy policy](https://proton.me/drive/privacy-policy), file contents, file and folder names, and thumbnail previews are end-to-end encrypted.
[^2]: With a [premium](https://bitwarden.com/help/about-bitwarden-plans/#compare-personal-plans) subscription, [Bitwarden Send](https://bitwarden.com/products/send) allows you to share files and text securely with [end-to-end encryption](https://bitwarden.com/help/send-encryption). A [password](https://bitwarden.com/help/send-privacy/#send-passwords) can be required along with the Send link. Bitwarden Send also features [automatic deletion](https://bitwarden.com/help/send-lifespan).
