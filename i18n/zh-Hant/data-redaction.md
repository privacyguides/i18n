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

您 **永遠不應** 透過模糊文字的方式來遮蓋 [圖片中的文字](https://bishopfox.com/blog/unredacter-tool-never-pixelation)。 If you want to redact text in an image, you should draw a box over the text.

</div>

## MAT2

<div class="admonition recommendation" markdown>

![MAT2 logo](assets/img/data-redaction/mat2.svg){ align=right }

**MAT2** is free, cross-platform software which allows you to remove metadata from image, audio, torrent, and document file types. 它提供命令行工具和圖形用戶界面擴展給 [Dolphin](https://0xacab.org/jvoisin/mat2/-/tree/master/dolphin)，其為[KDE](https://kde.org)的預設檔案管理器。

[:octicons-repo-16: Repository](https://0xacab.org/jvoisin/mat2){ .md-button .md-button--primary }
[:octicons-info-16:](https://0xacab.org/jvoisin/mat2/-/blob/master/README.md){ .card-link title="Documentation" }
[:octicons-code-16:](https://0xacab.org/jvoisin/mat2){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>下載</summary>

- [:fontawesome-brands-windows: Windows](https://pypi.org/project/mat2)
- [:simple-apple: macOS](https://0xacab.org/jvoisin/mat2#requirements-setup-on-macos-os-x-using-homebrew)
- [:simple-linux: Linux](https://pypi.org/project/mat2)
- [:octicons-globe-16: 網頁版](https://0xacab.org/jvoisin/mat2#web-interface)

</details>

</div>

## ExifEraser (Android)

<div class="admonition recommendation" markdown>

![ExifEraser logo](assets/img/data-redaction/exiferaser.svg){ align=right }

**ExifEraser** 是 Android 的現代無需許可的圖像中繼資料擦除應用程式。

它目前支援JPEG ， PNG和WebP 檔案格式。

[:octicons-repo-16: Repository](https://github.com/Tommy-Geenexus/exif-eraser){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/Tommy-Geenexus/exif-eraser#readme){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/Tommy-Geenexus/exif-eraser){ .card-link title="Source Code" }

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

## Shortcuts (iOS & macOS)

On iOS and macOS, you can remove image metadata without using any third-party apps by creating a [**shortcut**](https://apps.apple.com/app/id915249334) for this purpose. Here is an example shortcut you can download to use as is:

[:material-tag-minus: Clean Image Metadata](https://icloud.com/shortcuts/fb774ddb7b5b4296871776c67ac0fff9 ""){.md-button}

You can also use it as a model for your own shortcut; just make sure that the **Preserve Metadata** option under the **Convert** action is unchecked. Once added, you can access the shortcut in the share sheet that appears when you select the :octicons-share-24: Share button. You can select multiple images and invoke the shortcut to remove their metadata all at once.

This shortcut removes metadata such as location, device model, lens model, and other camera information. It also sets the image creation date to the time the shortcut was used.

## ExifTool (CLI)

<div class="admonition recommendation" markdown>

![ExifTool logo](assets/img/data-redaction/exiftool.png){ align=right }

**ExifTool** is the original Perl library and command-line application for reading, writing, and editing meta information (Exif, IPTC, XMP, and more) in a wide variety of file formats (JPEG, TIFF, PNG, PDF, RAW, and more).

It is often a component of other Exif removal applications and in most Linux distribution repositories.

[:octicons-home-16: Homepage](https://exiftool.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://exiftool.org/faq.html){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/exiftool/exiftool){ .card-link title="Source Code" }
[:octicons-heart-16:](https://exiftool.org/#donate){ .card-link title="Contribute" }

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
