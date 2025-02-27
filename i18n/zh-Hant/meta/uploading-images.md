---
title: 上傳圖片
description: 網站供稿者以正確格式和取得方式上傳圖片的指南。
---

如果您對本網站進行的變更涉及新增圖片或取代現有圖片，以下是幾項一般建議：

## 圖片

- 我們**偏好** SVG 影像，但如果沒有 SVG 影像，我們也可以使用 PNG 影像。 此外，對於封面圖片，我們希望它們是從 [Unsplash](https://unsplash.com) 取得，並且是 WebP 格式。

Company logos should be square if possible, and at least 200x200px if they are PNGs (non-vector images).

## 最佳化

### PNG

使用 [OptiPNG](https://sourceforge.net/projects/optipng) 工具來最佳化影像：

```bash
optipng -o7 file.png
```

### SVG

#### Inkscape

[清理](https://github.com/scour-project/scour) 所有 SVG 圖片。

在 Inkscape：

1. File > Save As...
2. Set type to: Optimized SVG (*.svg)

在「 **選項** 」標籤中：

- **坐標的有效位數** > **5**
- [x] 打開 **縮短顏色值**
- [x] 開啟 **將 CSS 屬性轉換為 XML 屬性**
- [x] 開啟 **折疊羣組**
- [x] 開啟 **為類似屬性建立羣組**
- [ ] 關閉 **保留編輯器資料**
- [ ] 關閉 **保留未引用的定義**
- [x] 打開 **工作周圍的渲染器錯誤**

在 **文件選項**下的 **SVG 輸出** 標籤：

- [ ] 關閉 **移除 XML 宣告**
- [x] 打開 **移除元數據**
- [x] 開啟 **刪除評論**
- [x] Turn on **Embedded raster images**
- [x] 打開 **啓用 viewboxing **

在 **Pretty-printing**下的 **SVG 輸出** 標籤：

- [ ] 關閉 **斷行分隔輸出格式和縮排**
- **縮排字元** > 選擇 **空格**
- ** 縮排寛度** > **1**
- [ ]關閉 **從根 SVG 元素** 刪除"xml: space"屬性

在 **IDS** 標籤中：

- [x] 打開 **移除未使用的IDs**
- [ ] 關閉 **縮短IDs**
- **縮短前綴` `的IDs** >
- [x] 開啟 **保留手動創建非以數字**結尾的 IDs
- **保留以下 IDs** > `留空`
- **保留以** > `  `開頭的ID</code>

#### 命令列

使用 [Scour](https://github.com/scour-project/scour) 命令可以做到同樣的事情：

```bash
scour --set-precision=5 \
      --create-groups \
      --renderer-workaround \
      --remove-descriptive-elements \
      --enable-comment-stripping \
      --enable-viewboxing \
      --indent=space \
      --nindent=1 \
      --no-line-breaks \
      --enable-id-stripping \
      --protect-ids-noninkscape \
      input.svg output.svg
```

### WebP

使用 [cwebp](https://developers.google.com/speed/webp/docs/using) 指令將 PNG 或 JPEG 影像檔案轉換成 WebP 格式：

```bash
cwebp -q 70 -m 6 input_file -o output.webp
```
