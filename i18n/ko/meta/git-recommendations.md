---
title: 깃 권장 사항
description: 웹사이트 기여자를 위한 효과적인 깃 사용 가이드입니다.
---

GitHub.com의 웹 편집기에서 직접 이 웹사이트를 수정한다면 이 내용은 신경 쓰지 않아도 됩니다. 로컬에서 개발하고 있거나 장기적으로 웹사이트를 편집하는 사람이라면(그렇다면 아마 로컬에서 개발하는 것이 좋을 겁니다!), 다음 권장 사항을 고려해 보세요.

## SSH 키로 커밋 서명 활성화하기 { #enable-ssh-key-commit-signing }

기존 SSH 키를 서명에 사용하거나 [새 키를 생성](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)할 수 있습니다.

1. 깃 클라이언트가 기본적으로 커밋과 태그에 서명하도록 설정합니다(이 저장소에서만 기본으로 서명하려면 `--global`을 제거하세요):

    ```bash
    git config --global commit.gpgsign true
    git config --global gpg.format ssh
    git config --global tag.gpgSign true
    ```

2. 다음 명령으로 깃에서 서명에 사용할 SSH 키를 설정합니다. `/PATH/TO/.SSH/KEY.PUB`는 사용할 공개 키의 경로(예: `/home/user/.ssh/id_ed25519.pub`)로 바꾸세요:

    ```bash
    git config --global user.signingkey /PATH/TO/.SSH/KEY.PUB
    ```

[깃허브 계정에 SSH 키를 추가](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account#adding-a-new-ssh-key-to-your-account)할 때 (인증 키 대신 또는 인증 키와 함께) **서명 키로** 추가했는지 확인하세요.

## 깃 풀 시 리베이스하기 { #rebase-on-git-pull }

깃허브의 변경 사항을 로컬 컴퓨터로 가져올 때는 `git pull` 대신 `git pull --rebase`를 사용하세요. 이렇게 하면 로컬 변경 사항이 항상 깃허브의 최신 변경 사항 "위에" 놓이게 되며, (이 저장소에서 허용되지 않는) 병합 커밋을 피할 수 있습니다.

이를 기본 동작으로 설정할 수 있습니다:

```bash
git config --global pull.rebase true
```

## PR을 제출하기 전에 `main`에서 리베이스하기 { #rebase-from-main-before-submitting-a-pr }

자신의 브랜치에서 작업하고 있다면 PR을 제출하기 전에 다음 명령을 실행하세요:

```bash
git fetch origin
git rebase origin/main
```
