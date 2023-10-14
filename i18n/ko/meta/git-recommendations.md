---
title: Git 사용 안내
---

본 내용은 GitHub.com의 웹 편집기에서 직접 웹사이트를 수정하는 경우에는 신경 쓸 필요가 없습니다. 로컬에서 개발 중이거나, 지속적으로 사이트에 기여하려는 경우(아마도 로컬에서 개발하셔야 할 겁니다) 참고 바랍니다.

## SSH 키 커밋 서명 활성화

서명용 SSH 키는 기존 키를 사용하거나, [새로 생성하여](https://docs.github.com/ko/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) 사용할 수 있습니다.

1. Git 클라이언트를 설정해 커밋과 태그가 기본적으로 서명되도록 합니다(현재 저장소에서만 서명하려면 `--global` 부분을 제거하세요).
   ```
   git config --global commit.gpgsign true
   git config --global gpg.format ssh
   git config --global tag.gpgSign true
   ```
2. Set your SSH key for signing in Git with the following command, substituting `/PATH/TO/.SSH/KEY.PUB` with the path to the public key you'd like to use, e.g. `/home/user/.ssh/id_ed25519.pub`:
   ```
   git config --global user.signingkey /PATH/TO/.SSH/KEY.PUB
   ```

[GitHub 계정에 새 SSH 키 추가](https://docs.github.com/ko/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account#adding-a-new-ssh-key-to-your-account) 문서를 참고해 **서명 키**로 추가합니다(주의: 인증 키와 서명 키는 별도입니다).

## Git Pull 리베이스

로컬 작업 환경으로 변경 사항을 가져올 때는 `git pull` 대신 `git pull --rebase`를 사용하세요. 이로써 로컬 변경 사항이 항상 GitHub의 최신 변경 사항보다 앞서게 되며, 병합(merge) 커밋이 생성되는 것을 피할 수 있습니다(본 프로젝트의 저장소에서는 병합 커밋이 허용되지 않습니다).

항상 자동으로 리베이스되도록 설정할 수도 있습니다.

```
git config --global pull.rebase true
```

## PR 제출 이전에 `main` 브랜치로부터 리베이스

자체 브랜치에서 작업하는 경우, PR을 제출하기 전에 다음 명령어를 실행합니다.

```
git fetch origin
git rebase origin/main
```
