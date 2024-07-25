---
title: 上傳圖片
---

If you make changes to this website that involve adding new images or replacing existing ones, here are a couple of general recommendations:

## 圖片

- We **prefer** SVG images, but if those do not exist we can use PNG images. Additionally, for cover images, we prefer that they are obtained from [Unsplash](https://unsplash.com) and are in the WebP format.

公司 logo 的畫布尺寸爲：

- 128x128px
- 384x128px

## 最佳化

### PNG

Use the [OptiPNG](https://sourceforge.net/projects/optipng) tool to optimize PNG images:

```bash
optipng -o7 file.png
```

### SVG

#### Inkscape

[清理](https://github.com/scour-project/scour) 所有 SVG 圖片。

在 Inkscape：

1. 檔案另存爲...
2. 將類型設定為最佳化SVG (*.svg)

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
- [x] 打開 **嵌入式光柵映像**
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

Use the [cwebp](https://developers.google.com/speed/webp/docs/using) command to convert PNG or JPEG image files to WebP format:

```bash
cwebp -q 70 -m 6 input_file -o output.webp
```
