---
title: 이미지 업로드 방법
---

본 내용은 Privacy Guides에 기여할 때 주의해야 하는 규정입니다.

## 이미지

- SVG 이미지가 선호되지만, 적절한 SVG 이미지가 존재하지 않는 경우 PNG 이미지를 사용할 수 있습니다.

업체 로고는 캔버스 크기를 다음과 같이 설정합니다.

- 128x128px
- 384x128px

## 최적화

### PNG

PNG 이미지는 [OptiPNG](https://sourceforge.net/projects/optipng/)를 이용해 최적화하세요.

```bash
optipng -o7 file.png
```

### SVG

#### Inkscape

SVG 이미지는 모두 [Scour](https://github.com/scour-project/scour)로 최적화하세요.

Inkscape에서 다음과 같이 진행합니다.

1. **파일**(File) - **다른 이름으로 저장하기...**(Save As...)
2. 저장 형식을 **최적화된 SVG (*.svg)**(Optimized SVG (*.svg))로 설정합니다.

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
- [x] **래스터 이미지 끼워넣기**(Embeded raster images) 활성화
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
