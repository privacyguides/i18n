---
title: 이미지 업로드
description: 올바른 형식과 위치에 이미지를 업로드하는 방법에 대한 웹사이트 기여자용 가이드입니다.
---

이 웹사이트에 새 이미지를 추가하거나 기존 이미지를 교체하는 변경을 한다면, 다음과 같은 일반적인 권장 사항을 따르세요:

## 이미지 { #images }

- SVG 이미지를 **선호**하지만, SVG가 없다면 PNG 이미지를 사용할 수 있습니다. 또한 커버 이미지는 [언스플래시](https://unsplash.com)에서 가져온 WebP 형식의 이미지를 선호합니다.

회사 로고는 가능하면 정사각형이어야 하며, PNG(벡터가 아닌 이미지)라면 최소 200x200px이어야 합니다.

## 최적화 { #optimization }

### PNG

[OptiPNG](https://sourceforge.net/projects/optipng) 도구를 사용하여 PNG 이미지를 최적화하세요:

```bash
optipng -o7 file.png
```

### SVG

#### 잉크스케이프 { #inkscape }

모든 SVG 이미지는 [Scour](https://github.com/scour-project/scour)로 최적화하세요.

잉크스케이프에서:

1. 파일(File) > 다른 이름으로 저장(Save As)...
2. 파일 형식을 최적화된 SVG(Optimized SVG) (*.svg)로 설정합니다

**옵션**(Options) 탭에서:

- **좌표의 유효 자릿수**(Number of significant digits for coordinates) > **5**
- [x] **색상 값 단축**(Shorten color values) 켜기
- [x] **CSS 속성을 XML 속성으로 변환**(Convert CSS attributes to XML attributes) 켜기
- [x] **그룹 축소**(Collapse groups) 켜기
- [x] **유사한 속성에 대한 그룹 생성**(Create groups for similar attributes) 켜기
- [ ] **편집기 데이터 유지**(Keep editor data) 끄기
- [ ] **참조되지 않은 정의 유지**(Keep unreferenced definitions) 끄기
- [x] **렌더러 버그 우회**(Work around renderer bugs) 켜기

**SVG 출력**(SVG Output) 탭의 **문서 옵션**(Document options)에서:

- [ ] **XML 선언 제거**(Remove the XML declaration) 끄기
- [x] **메타데이터 제거**(Remove metadata) 켜기
- [x] **주석 제거**(Remove comments) 켜기
- [x] **래스터 이미지 포함**(Embedded raster images) 켜기
- [x] **viewBox 사용**(Enable viewboxing) 켜기

**SVG 출력**(SVG Output)의 **보기 좋게 출력**(Pretty-printing)에서:

- [ ] **줄바꿈과 들여쓰기로 출력 서식 지정**(Format output with line-breaks and indentation) 끄기
- **들여쓰기 문자**(Indentation characters) > **공백**(Space) 선택
- **들여쓰기 깊이**(Depth of indentation) > **1**
- [ ] **루트 SVG 요소에서 "xml:space" 속성 제거**(Strip the "xml:space" attribute from the root SVG element) 끄기

**ID**(IDs) 탭에서:

- [x] **사용하지 않는 ID 제거**(Remove unused IDs) 켜기
- [ ] **ID 단축**(Shorten IDs) 끄기
- **단축된 ID 접두사**(Prefix shortened IDs with) > `leave blank`(비워 둠)
- [x] **숫자로 끝나지 않는 수동 생성 ID 유지**(Preserve manually created IDs not ending with digits) 켜기
- **다음 ID 유지**(Preserve the following IDs) > `leave blank`(비워 둠)
- **다음으로 시작하는 ID 유지**(Preserve IDs starting with) > `leave blank`(비워 둠)

#### CLI

[Scour](https://github.com/scour-project/scour) 명령으로도 같은 작업을 할 수 있습니다:

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

[`cwebp`](https://developers.google.com/speed/webp/docs/using) 명령을 사용하여 PNG나 JPEG 이미지 파일을 WebP 형식으로 변환하세요:

```bash
cwebp -m 6 input_file -o output.webp
```
