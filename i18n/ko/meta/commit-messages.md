---
title: 커밋 메시지
description: 웹사이트 변경을 요청할 때 유용한 깃 커밋 메시지를 작성하는 방법에 대한 웹사이트 기여자용 가이드입니다.
---

커밋 메시지는 [컨벤셔널 커밋](https://conventionalcommits.org)에서 제시하는 스타일을 따릅니다. 그 제안이 모두 프라이버시 가이드에 적합한 것은 아니므로, 주로 사용하는 유형은 다음과 같습니다:

## 기존 텍스트 업데이트 { #update-to-existing-text }

이 예시는 이미 사이트에 있는 항목의 설명을 조금 업데이트하는 경우에 사용할 수 있습니다.

```text
update: Add mention of security audit (#0000)
```

## 추천 항목/페이지 추가 또는 제거 { #addition-or-removal-of-recommendationspages }

이 예시는 항목을 추가하거나 제거하는 경우입니다. 제거한 이유는 아래와 같이 커밋 본문에 자세히 설명할 수 있습니다. 주요 변경 사항임을 강조하기 위해 `!`를 추가한 점에 유의하세요.

```text
update!: Remove foobar (#0000)

Foobar was removed due to it having numerious security issues and being unmaintained.
```

사실 이 페이지의 _모든_ 유형에 `!`를 추가하여 특히 큰 변경 사항임을 나타낼 수 있지만, 일반적으로 이 경우에 가장 적합합니다.

## 기능/개선 { #featureenhancement }

깃허브에서 `enhancements` 라벨이 붙은 항목처럼 사이트의 새로운 기능이나 개선 사항은 다음과 같이 표시하는 것이 적절할 수 있습니다:

```text
feat: Add blah blah (#0000)

This change adds the forum topics to the main page
```

## 사소한 변경 { #minor-changes }

오타 수정, 문법 수정, 서식/공백 변경, CSS 업데이트 등 글의 **의미에 영향을 주지 않는** 작은 변경 사항입니다.

```text
style: Typo correction in VPN overview
```

## 개발 관련 유형 { #development-related-types }

이러한 커밋 유형은 일반적으로 일반 독자에게 보이지 않는 변경 사항에 사용됩니다.

사이트 관련 버그를 수정하는 변경 사항에는 `fix:`를 사용합니다. 이러한 항목에는 보통 깃허브에서 `bug` 라벨이 붙어 있습니다.

```text
fix: Remove broken Invidious embeds (#0000)
```

README 파일이나 `/docs/about` 또는 `/docs/meta`의 대부분 페이지 등을 포함하여(이에 국한되지 않음) 이 웹사이트의 개발자 문서를 변경할 때는 `docs:`를 사용합니다:

```text
docs: Update Git commit message guidelines (#0000)
```

빌드 프로세스와 관련된 커밋, 주로 의존성 업데이트에는 `build:`를 사용합니다.

```text
build: Bump modules/mkdocs-material from 463e535 to 621a5b8
```

깃허브 액션, DevContainers 또는 기타 자동화된 빌드 플랫폼과 관련된 커밋에는 `ci:`를 사용합니다.

```text
ci: Update Netlify config (#0000)
```

파일 재배치, 내비게이션 순서 변경 등 버그 수정도 기능 추가도 아닌 변경 사항에는 `refactor:`를 사용합니다.

```text
refactor: Move docs/assets to theme/assets
```
