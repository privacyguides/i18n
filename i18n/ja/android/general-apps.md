---
title: "General Apps"
description: 本記事で紹介するアプリはAndroid専用アプリで、システムの重要な機能を強化あるいは置換するものです。
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: General Android Apps
    url: "./"
  - "@context": http://schema.org
    "@type": MobileApplication
    name: Shelter
    applicationCategory: Utilities
    operatingSystem: Android
  - "@context": http://schema.org
    "@type": MobileApplication
    name: Secure Camera
    applicationCategory: Utilities
    operatingSystem: Android
  - "@context": http://schema.org
    "@type": MobileApplication
    name: Secure PDF Viewer
    applicationCategory: Utilities
    operatingSystem: Android
robots: nofollow, max-snippet:-1, max-image-preview:large
---

<small>以下の脅威から保護します：</small>

- [:material-bug-outline: パッシブ攻撃](../basics/common-threats.md#security-and-privacy){ .pg-orange }

本サイトでは様々なAndroidアプリをおすすめしています。 本記事で紹介するアプリはAndroid専用アプリで、システムの重要な機能を強化あるいは置換するものです。

### Shelter

Android 15以上のデバイスを使用しているのであれば、Shelterではなく、標準機能である[プライベートスペース](../os/android-overview.md#private-space)を使うことを推奨します。サードパーティを信用して強力な権限を与える必要がなく、ほぼ同様の機能が使えます。

<div class="admonition recommendation" markdown>

![Shelterのロゴ](../assets/img/android/shelter.svg){ align=right }

**Shelter**は、Androidの仕事用プロファイル機能を利用して、デバイス上のアプリを隔離または複製できるアプリです。

別プロファイルの連絡先を検索するのをブロックしたり、デフォルトのファイルマネージャー([DocumentsUI](https://source.android.com/devices/architecture/modular-system/documentsui))を使って別プロファイルとファイルを共有するのをブロックする機能があります。

[:octicons-repo-16: リポジトリ](https://gitea.angry.im/PeterCxy/Shelter#shelter){ .md-button .md-button--primary }
[:octicons-code-16:](https://gitea.angry.im/PeterCxy/Shelter){ .card-link title="ソースコード" }
[:octicons-heart-16:](https://patreon.com/PeterCxy){ .card-link title=支援 }

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">注意</p>

Shelterを使用することで、Shelterの開発者を完全に信頼することになります。仕事用プロファイルを作成するためにShelterは[デバイス管理者](https://developer.android.com/guide/topics/admin/device-admin?hl=ja)として実行されるため、プロファイル内の広範囲のデータにアクセスすることができます。

</div>

Shelterは[連絡先の検索をブロック](https://secure-system.gitlab.io/Insular/faq.html)できるため、[Insular](https://secure-system.gitlab.io/Insular)や[Island](https://github.com/oasisfeng/island)よりもおすすめです。

### Secure Camera

<small>以下の脅威から保護します：</small>

- [:material-account-search: 秘密の暴露](../basics/common-threats.md#limiting-public-information){ .pg-green }

<div class="admonition recommendation" markdown>

![Secure cameraのロゴ](../assets/img/android/secure_camera.svg#only-light){ align=right }
![Secure cameraのロゴ](../assets/img/android/secure_camera-dark.svg#only-dark){ align=right }

**Secure Camera**は、プライバシーとセキュリティを重視したカメラアプリで、画像、ビデオ、QRコードを撮影することができます。 CameraXの拡張機能(ポートレートモード、HDR、夜景、顔のレタッチ、オートモード)も、デバイスが対応していれば使用できます。

[:octicons-repo-16: レポジトリ](https://github.com/GrapheneOS/Camera#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://grapheneos.org/usage#camera){ .card-link title=ドキュメント}
[:octicons-code-16:](https://github.com/GrapheneOS/Camera){ .card-link title="ソースコード" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=支援 }

<details class="downloads" markdown>
<summary>ダウンロード</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.camera.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/Camera/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

主なプライバシー機能：

- [Exif](https://en.wikipedia.org/wiki/Exif)メタデータの自動消去(デフォルトで有効)
- 新しく追加された[メディア](https://developer.android.com/training/data-storage/shared/media)APIを使用するため、[ストレージ権限](https://developer.android.com/training/data-storage)が不要
- 音声を録音しない限りマイク権限が不要

<div class="admonition note" markdown>
<p class="admonition-title">補足</p>

現状、動画ファイルからはメタデータは消去されませんが、その機能は追加予定です。

画像の向きのメタデータは消去されません。 Secure Cameraで位置情報を有効にすると、それも消去されません。 このデータを後から消去するには、[ExifEraser](../data-redaction.md#exiferaser-android)などの別のアプリが必要になります。

</div>

### Secure PDF Viewer

<small>以下の脅威から保護します：</small>

- [:material-target-account: 標的型攻撃](../basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }

<div class="admonition recommendation" markdown>

![Secure PDF Viewerのロゴ](../assets/img/android/secure_pdf_viewer.svg#only-light){ align=right }
![Secure PDF Viewerのロゴ](../assets/img/android/secure_pdf_viewer-dark.svg#only-dark){ align=right }

**Secure PDF Viewer**は、[pdf.js](https://ja.wikipedia.org/wiki/PDF.js)をベースにしたPDFビューアで、権限が一切必要ありません。 開いたPDFは[サンドボックス化](https://ja.wikipedia.org/wiki/%E3%82%B5%E3%83%B3%E3%83%89%E3%83%9C%E3%83%83%E3%82%AF%E3%82%B9_\(%E3%82%BD%E3%83%95%E3%83%88%E3%82%A6%E3%82%A7%E3%82%A2%E9%96%8B%E7%99%BA\))された[WebView](https://developer.android.com/guide/webapps/webview)に送られます。 そのため、コンテンツやファイルに直接アクセスしに行く権限が必要ありません。

[Content-Security-Policy](https://en.wikipedia.org/wiki/Content_Security_Policy)を使用することで、WebView内のJavaScriptとスタイルプロパティがすべて静的コンテンツであることを強制するようになっています。

[:octicons-repo-16: リポジトリ](https://github.com/GrapheneOS/PdfViewer#readme){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/GrapheneOS/PdfViewer){ .card-link title="ソースコード" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=支援 }

<details class="downloads" markdown>
<summary>ダウンロード</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.pdfviewer.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/PdfViewer/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

## 規準

\*\*私たちは、推薦するどのプロジェクトとも提携していません。\*\*客観的に推薦できるよう、[標準となる規準](../about/criteria.md)に加えて、一連の明確な要件を定めています。 プロジェクトを利用する前に、このリストをよく理解し、ご自身で調査を行って、そのプロジェクトがあなたにとって適切な選択かどうかをご確認ください。

- 本サイト上の他のカテゴリに当てはまらないアプリのみ本ページに掲載する。
- General applications should extend or replace core system functionality.
- 定期的なアップデート・メンテナンスが行われているアプリであること。
