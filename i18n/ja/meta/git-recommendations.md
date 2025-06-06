---
title: Git Recommendations
description: A guide for website contributors on using Git effectively.
---

GitHub.comのウェブエディターでこのウェブサイトに直接変更を加える場合は、このことを心配する必要はありません。 ローカルで開発している場合や、ウェブサイトを長期的に編集している（おそらくローカルで開発しているはずです！）場合は、以下の推奨事項を検討してください。

## SSHキーのコミット署名を有効にする

署名に既存の SSH キーを使用することも、[新しいSSH キーを作成することもできます](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)。

1. デフォルトでコミットとタグに署名するように Git クライアントを設定する (remove `--global` to only sign by default for this repo):

    ```bash
    git config --global commit.gpgsign true
    git config --global gpg.format ssh
    git config --global tag.gpgSign true
    ```

2. Set your SSH key for signing in Git with the following command, substituting `/PATH/TO/.SSH/KEY.PUB` with the path to the public key you'd like to use, e.g. `/home/user/.ssh/id_ed25519.pub`:

    ```bash
    git config --global user.signingkey /PATH/TO/.SSH/KEY.PUB
    ```

Ensure you [add your SSH key to your GitHub account](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account#adding-a-new-ssh-key-to-your-account) **as a Signing Key** (as opposed to or in addition to as an Authentication Key).

## Git pullでrebaseを行うこと

Use `git pull --rebase` instead of `git pull` when pulling in changes from GitHub to your local machine. This way your local changes will always be "on top of" the latest changes on GitHub, and you avoid merge commits (which are disallowed in this repo).

You can set this to be the default behavior:

```bash
git config --global pull.rebase true
```

## Rebase from `main` before submitting a PR

If you are working on your own branch, run these commands before submitting a PR:

```bash
git fetch origin
git rebase origin/main
```
