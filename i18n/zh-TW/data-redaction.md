---
meta_title: "使用中繼資料清除器和數據編輯工具移除個人識別資料 - Privacy Guides"
title: "資料和中繼資料處理"
icon: material/tag-remove
description: 使用這些工具來移除所分享的相片和文件中的GPS定位和其他識別資訊等中繼資料。
cover: data-redaction.webp
---

<small>防護下列威脅：</small>

- [:material-account-search: 公共曝露](basics/common-threats.md#limiting-public-information ""){.pg-green}

分享檔案時，請務必移除相關的中繼資料。 映像文件通常包含 [Exif](https://en.wikipedia.org/wiki/Exif) 數據。 照片有時甚至在文件元數據中包含GPS坐標。

<div class="admonition warning" markdown>
<p class="admonition-title">警告</p>

您 **永遠不應** 透過模糊文字的方式來遮蓋 [圖片中的文字](https://bishopfox.com/blog/unredacter-tool-never-pixelation)。 若要遮蔽圖片中的文字，請在文字上繪製方框。

</div>

## MAT2

<div class="admonition recommendation" markdown>

![MAT2 標誌](assets/img/data-redaction/mat2.svg){ align=right }

**MAT2** 是自由的跨平台軟體，可以移除影像、音訊、torrent 與文件檔案類型的中介資料。 其同時提供了命令列工具與圖形化使用者介面，並透過擴充套件整合至 [Dolphin](https://github.com/jvoisin/mat2/tree/master/dolphin)（[KDE](https://kde.org) 預設的檔案管理程式）。

[:octicons-repo-16: 軟體倉庫](https://github.com/jvoisin/mat2#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/jvoisin/mat2#how-to-use-mat2){ .card-link title="文件" }
[:octicons-code-16:](https://github.com/jvoisin/mat2){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:fontawesome-brands-windows: Windows](https://pypi.org/project/mat2)
- [:simple-apple: macOS](https://github.com/jvoisin/mat2#requirements-setup-on-macos-os-x-using-homebrew)
- [:simple-linux: Linux](https://pypi.org/project/mat2)
- [:octicons-browser-16: 網頁](https://github.com/jvoisin/mat2#web-interface)

</details>

</div>

## ExifEraser (Android)

<div class="admonition recommendation" markdown>

![ExifEraser logo](assets/img/data-redaction/exiferaser.svg){ align=right }

**ExifEraser** 是 Android 的現代無需許可的圖像中繼資料擦除應用程式。

其目前支援 JPEG、PNG 與 WebP 檔案。

[:octicons-repo-16: 軟體倉庫](https://github.com/Tommy-Geenexus/exif-eraser#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/Tommy-Geenexus/exif-eraser#description){ .card-link title="文件" }
[:octicons-code-16:](https://github.com/Tommy-Geenexus/exif-eraser){ .card-link title="原始碼" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.none.tom.exiferaser)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/com.none.tom.exiferaser)
- [:simple-github: GitHub](https://github.com/Tommy-Geenexus/exif-eraser/releases)

</details>

</div>

被清除的元資料取決於影像的檔案類型：

- **JPEG**：可清除 ICC Profile、Exif、Photoshop Image Resources 和 XMP/ExtendedXMP 等中繼資料。
- **PNG**：可清除 ICC Profile、Exif和XMP等中繼資料。
- **WebP**: 可清除 ICC Profile、Exif 和XMP 等中繼資料。

處理完影像後， ExifEraser會為您提供一份完整的報告，說明每張影像中究竟刪除了哪些內容。

該應用程式提供了多種方式來清除圖像中的中繼數據。 亦即:

- 您可以使用 ExifEraser 分享其他應用程式的圖片。
- 通過應用程式本身，可以一次選擇單個圖片，多個圖片，甚至是整個目錄。
- 它具有“相機”選項，該選項使用操作系統的相機應用程式拍攝照片，然後從中刪除中繼數據。
- 在分割視窗模式下，它可以從另一個應用程式拖放圖片到 ExifEraser 。
- 最後，它允許您從剪貼板黏貼圖像。

## 捷徑（iOS 與 macOS）

在 iOS 與 macOS 上，您可以透過建立[**捷徑**](https://apps.apple.com/app/id915249334)來移除影像的中介資料。 以下是一個可直接下載使用的捷徑範例：

[:material-tag-minus: 清理影像中介資料](https://icloud.com/shortcuts/fb774ddb7b5b4296871776c67ac0fff9 ""){.md-button}

您也可以使用它作為自己捷徑的範本，只要確定不要勾選**轉換**動作下的**保留中介資料**選項即可。 新增後，您可以在選取 :octicons-share-24: 分享按鈕時出現的分享頁面中存取捷徑。 您可以選取多個影像，然後呼叫捷徑一次移除它們的中介資料。

此捷徑可移除位置、裝置型號、鏡頭型號與其他相機資訊等中介資料。 它也會將影像建立日期設定為使用捷徑的時間。

## ExifTool (CLI)

<div class="admonition recommendation" markdown>

![ExifTool 標誌](assets/img/data-redaction/exiftool.png){ align=right }

**ExifTool** 是原始的 Perl 函式庫與命令列應用程式，用來讀取、寫入與編輯各種檔案格式（JPEG、TIFF、PNG、PDF、RAW 等等）的中介資料（Exif、IPTC、XMP 等等）。

其通常是其他 Exif 移除應用程式的元件，大多數的 Linux 散佈版軟體庫中也有收錄。

[:octicons-home-16: 首頁](https://exiftool.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://exiftool.org/faq.html){ .card-link title="文件" }
[:octicons-code-16:](https://github.com/exiftool/exiftool){ .card-link title="原始碼" }
[:octicons-heart-16:](https://exiftool.org/#donate){ .card-link title="貢獻" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:fontawesome-brands-windows: Windows](https://exiftool.org)
- [:simple-apple: macOS](https://exiftool.org)
- [:simple-linux: Linux](https://exiftool.org)

</details>

</div>

<div class="admonition example" markdown>
<p class="admonition-title">從檔案目錄中刪除資料</p>

```bash
exiftool -all= *.file_extension
```

</div>

## 標準

**請注意，我們與推薦的任何項目均無關。**除了[我們的通用標準](about/criteria.md)外，我們還制定了一套明確的要求，以便我們能夠提供客觀的建議。 我們建議您在選擇使用項目之前先熟悉此列表，並進行自己的研究，以確保它是您的正確選擇。

- 為開源作業系統開發的應用程式必須是開源的。
- 應用程式必須是免費的，不應包含廣告或其他限制。
