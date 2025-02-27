---
title: Uploading Images
description: A guide for website contributors on uploading images in the proper format and location.
---

If you make changes to this website that involve adding new images or replacing existing ones, here are a couple of general recommendations:

## 이미지

- We **prefer** SVG images, but if those do not exist we can use PNG images. Additionally, for cover images, we prefer that they are obtained from [Unsplash](https://unsplash.com) and are in the WebP format.

Company logos should be square if possible, and at least 200x200px if they are PNGs (non-vector images).

## 최적화

### PNG

Use the [OptiPNG](https://sourceforge.net/projects/optipng) tool to optimize PNG images:

```bash
optipng -o7 file.png
```

### SVG

#### Inkscape

SVG 이미지는 모두 [Scour](https://github.com/scour-project/scour)로 최적화하세요.

Inkscape에서 다음과 같이 진행합니다.

1. File > Save As...
2. Set type to: Optimized SVG (*.svg)

**최적화된 SVG 출력**(Optimized SVG Output) 창 - **옵션**(Options):

- **좌표의 유효 자릿수**(Number of significant digits for coordinates) > **5**
- [x] **색상 값 단축하기**(Shorten color values) 활성화
- [x] **CSS 속성을 XML 속성으로 전환시키기**(Convert CSS attributes to XML attributes) 활성화
- [x] **그룹 접기**(Collapse groups) 활성화
- [x] **유사한 특성에 대한 그룹 만들기**(Create groups for similar attributes) 활성화
- [ ] **편집기 데이터 유지하기**(Keep editor data) 비활성화
- [ ] **참조되지 않은 정의 유지하기**(Keep unreferenced definitions) 비활성화
- [x] **렌더링도구 버그 해결 방법**(Work around renderer bugs) 활성화

**SVG 출력**(SVG Output) - **문서 옵션**(Document options):

- [ ] **XML 선언 제거하기**(Remove the XML declaration) 비활성화
- [x] **메타데이터 제거하기**(Remove metadata) 활성화
- [x] **주석 제거하기**(Remove comments) 활성화
- [x] Turn on **Embedded raster images**
- [x] **보기상자 활성화**(Enable viewboxing) 활성화

**SVG 출력**(SVG Output) - **멋을 낸 인쇄물**(Pretty-printing):

- [ ] **줄바꿈 및 들여쓰기로 출력 형식 지정**(Format output with line-breaks and indentation) 비활성화
- **들여쓰기 문자**(Indentation characters) > **스페이스**(Space) 선택
- **들여쓰기 깊이**(Depth of indentation) > **1**
- [ ] **루트 SVG 요소에서 "xml:space" 속성 떼어내기**(Strip the "xml:space" attribute from the root SVG element) 비활성화

**ID**(IDs):

- [x] **사용하지 않는 ID 제거하기**(Remove unused IDs) 활성화
- [ ] **ID 단축하기**(Shorten IDs) 비활성화
- **단축된 ID 접두사**(Prefix shortened IDs with) > 빈 칸으로 유지
- [x] **숫자로 끝나지 않는 수동 입력으로 만들어진 ID 보존하기**(Preserve manually created IDs not ending with digits) 활성화
- **다음 ID 보존하기**(Preserve the following IDs) > 빈 칸으로 유지
- **시작하는 ID 보존하기**(Preserve IDs starting with) > 빈 칸으로 유지

#### CLI

[Scour](https://github.com/scour-project/scour) 명령어로도 동일한 작업이 가능합니다.

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
