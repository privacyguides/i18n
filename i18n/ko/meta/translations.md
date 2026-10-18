---
title: 번역
description: 웹사이트에 번역을 추가하는 방법에 대한 웹사이트 기여자용 가이드입니다.
---

크라우딘은 문서가 잘 갖춰져 있으므로 [시작하기](https://support.crowdin.com/crowdin-intro) 가이드를 살펴볼 것을 권장합니다. 이 사이트는 대부분 [마크다운](https://en.wikipedia.org/wiki/Markdown)으로 작성되어 있어 쉽게 기여할 수 있습니다. 이 페이지에는 사이트에서 마주칠 수 있는 특정 문법을 번역할 때 도움이 되는 몇 가지 팁이 담겨 있습니다.

추가로 궁금한 점이 있다면 매트릭스의 현지화 채팅방([#pg-i18n:aragon.sh](https://matrix.to/#/%23pg-i18n:aragon.sh))에 참여하시고, 프로젝트에 대한 자세한 정보는 [발표 블로그 글](https://blog.privacyguides.org/2023/02/26/i18n-announcement)을 읽어 보세요.

사이트의 영어판이 기본 버전이므로 변경 사항은 영어판에 먼저 반영된다는 점에 유의하세요. 영어판보다 뒤처진 언어를 발견하면 도움을 주세요. 모든 번역의 정확성을 보장할 수는 없습니다. 특정 지역에 관한 콘텐츠를 제안하고 싶다면 [메인 저장소](https://github.com/privacyguides/privacyguides.org)에 이슈나 풀 리퀘스트를 열어 주세요.

## 번역 결과물 { #translation-output }

번역 소프트웨어는 꽤 정확하게 번역하지만, 번역된 문자열이 올바른지는 직접 확인해야 합니다.

예를 들면 다음과 같습니다:

```text
![Software logo](assets/img/path/to/image.svg){ align=right }
```

위와 같은 이미지 삽입 문법에서 `![`가 빠지거나, 텍스트와 경로 사이(`](` 부분)에 공백이 추가로 들어간 경우가 종종 있었습니다. 번역 문자열이 명백히 잘못되었다면 휴지통 아이콘을 눌러 **삭제**하거나, 가장 좋다고 생각하는 번역에 [투표](https://support.crowdin.com/enterprise/getting-started-for-volunteers/#voting-view)해 주세요. 잘못된 문자열을 삭제하면 조직의 [번역 메모리](https://support.crowdin.com/enterprise/translation-memory)에서 제거되므로, 같은 원문이 다시 나타났을 때 잘못된 번역이 제안되지 않습니다.

## 문장 부호 { #punctuation }

위의 안내 상자 같은 예에서 문자열 텍스트를 지정할 때는 반드시 `" "`와 같은 큰따옴표를 사용해야 합니다. MkDocs는 `「 」`나 `« »` 같은 다른 기호를 올바르게 해석하지 못합니다. 그 외에 본문에서 일반적인 인용을 표시할 때는 다른 문장 부호를 사용해도 괜찮습니다.

## 전각 문자와 마크다운 문법 { #fullwidth-alternatives-and-markdown-syntax }

한중일(CJK) 문자 체계에서는 일반적인 기호의 "전각" 변형을 사용하는 경우가 많습니다. 이는 서로 다른 문자이므로 마크다운 문법에 사용할 수 없습니다.

- 링크에는 `（`(전각 왼쪽 괄호 U+FF08)나 `）`(전각 오른쪽 괄호 U+FF09)가 아닌 일반 괄호, 즉 `(`(왼쪽 괄호 U+0028)와 `)`(오른쪽 괄호 U+0029)를 사용해야 합니다.
- 들여쓴 인용 텍스트에는 `：`(전각 콜론 U+FF1A)가 아닌 `:`(콜론 U+003A)를 사용해야 합니다.
- 그림에는 `！`(전각 느낌표 U+FF01)가 아닌 `!`(느낌표 U+0021)를 사용해야 합니다.
