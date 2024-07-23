---
title: 常規應用程式
schema:
  - "@context": http://schema.org
    "@type": 網頁
    name: 常規 Android 應用程式
    url: ./
  - "@context": http://schema.org
    "@type": 手機應用程式
    name: Shelter
    applicationCategory: Utilities
    operatingSystem: Android
  - "@context": http://schema.org
    "@type": 手機應用程式
    name: Secure Camera
    applicationCategory: Utilities
    operatingSystem: Android
  - "@context": http://schema.org
    "@type": 手機應用程式
    name: Secure PDF Viewer
    applicationCategory: Utilities
    operatingSystem: Android
---

我們在本網站上推薦了各種 Android 應用程式。 此處列出的應用程式是 Android 獨有的，專門增強或替換了關鍵系統功能。

### Shelter

<div class="admonition recommendation" markdown>

![Shelter logo](../assets/img/android/shelter.svg){ align=right }

**Shelter** 是一款應用程序，可協助您利用 Android 的工作設定檔功能來隔離或複製裝置上的應用程式。

Shelter 支援阻止跨配置檔案的聯絡人搜尋以及透過預設檔案管理器跨配置檔案共用檔案 ([DocumentsUI](https://source.android.com/devices/architecture/modular-system/documentsui))。

[:octicons-repo-16: 儲存庫](https://gitea.angry.im/PeterCxy/Shelter#shelter){ .md-button .md-button--primary }
[:octicons-code-16:](https://gitea.angry.im/PeterCxy/Shelter){ .card-link title="原始碼" }
[:octicons-heart-16:](https://patreon.com/PeterCxy){ .card-link title=捐款 }

</div>

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

建議使用Shelter，而不是 [Insular](https://secure-system.gitlab.io/Insular) 和 [Island](https://github.com/oasisfeng/island) ，因為它支援 [聯絡人搜尋屏蔽](https://secure-system.gitlab.io/Insular/faq.html) 。

使用 Shelter 時，您將需要完全信任其開發人員，因為 Shelter 將作為 [設備管理員](https://developer.android.com/guide/topics/admin/device-admin) 來創建工作設定檔，這將使它有大量權限訪問存儲在工作設定檔的資料。

</div>

### Secure Camera

<div class="admonition recommendation" markdown>

![Secure camera logo](../assets/img/android/secure_camera.svg#only-light){ align=right }
![Secure camera logo](../assets/img/android/secure_camera-dark.svg#only-dark){ align=right }

**Secure Camera** 是一款專注於隱私和安全的相機應用程式，可以拍攝影像、影片及掃描QR碼。 可用設備還支援 CameraX 供應商擴充（肖像、HDR、夜視、臉部修飾和自動）。

[:octicons-repo-16: 儲存庫](https://github.com/GrapheneOS/Camera){ .md-button .md-button--primary }
[:octicons-info-16:](https://grapheneos.org/usage#camera){ .card-link title=文檔}
[:octicons-code-16:](https://github.com/GrapheneOS/Camera){ .card-link title="原始碼" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=捐款 }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.camera.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/Camera/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

主要隱私功能包括：

- 自動刪除 [Exif](https://zh.wikipedia.org/wiki/Exif) 元資料（預設啟用）
- 使用新的 [Media](https://developer.android.com/training/data-storage/shared/media) 應用程式接口，因此不需要 [存儲權限](https://developer.android.com/training/data-storage) 。
- 除非需錄制聲音，否則無需 麥克風權限 。

<div class="admonition note" markdown>
<p class="admonition-title">備註</p>

目前拍攝的影片不會被自動刪除元資料，但此功能已確認將在未來添加。

圖片的 方向元資料 不會被自動刪除。 如果您啟用了定位功能（在Secure Camera中），需要注意的是，位置資料與圖片的方向元資料一樣 **不會** 被自動刪除。 如果您在拍攝後想刪除元資料，您將需要使用外部應用程式，例如： [ExifEraser](../data-redaction.md#exiferaser-android) 。

</div>

### Secure PDF Viewer

<div class="admonition recommendation" markdown>

![Secure PDF Viewer logo](../assets/img/android/secure_pdf_viewer.svg#only-light){ align=right }
![Secure PDF Viewer logo](../assets/img/android/secure_pdf_viewer-dark.svg#only-dark){ align=right }

**Secure PDF Viewer** is a PDF viewer based on [pdf.js](https://en.wikipedia.org/wiki/PDF.js) that doesn't require any permissions. The PDF is fed into a [sandboxed](https://en.wikipedia.org/wiki/Sandbox_\(software_development\)) [WebView](https://developer.android.com/guide/webapps/webview). This means that it doesn't require permission directly to access content or files.

[Content-Security-Policy](https://en.wikipedia.org/wiki/Content_Security_Policy) is used to enforce that the JavaScript and styling properties within the WebView are entirely static content.

[:octicons-repo-16: Repository](https://github.com/GrapheneOS/PdfViewer){ .md-button .md-button--primary }
[:octicons-code-16:](https://github.com/GrapheneOS/PdfViewer){ .card-link title="Source Code" }
[:octicons-heart-16:](https://grapheneos.org/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=app.grapheneos.pdfviewer.play)
- [:simple-github: GitHub](https://github.com/GrapheneOS/PdfViewer/releases)
- [:material-cube-outline: GrapheneOS App Store](https://github.com/GrapheneOS/Apps/releases)

</details>

</div>

## 標準

**請注意，我們所推薦專案沒有任何瓜葛** 。除了 [標準準則](../about/criteria.md) 外，我們還制定了一套明確的要求，以便我們能夠提供客觀的建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

- Applications on this page must not be applicable to any other software category on the site.
- General applications should extend or replace core system functionality.
- Applications should receive regular updates and maintenance.
