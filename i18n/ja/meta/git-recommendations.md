---
title: Gitの推奨事項
---

GitHub.comのウェブエディターでこのウェブサイトに直接変更を加える場合は、この心配する必要はありません。 ローカルで開発している場合、および/または長期的なウェブサイトエディタ（おそらくローカルで開発しているはずです！）である場合は、これらの推奨事項を検討してください。

## SSHキーのコミット署名を有効にする

署名に既存の SSH キーを使用することも、[新しいSSH キーを作成することもできます。](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

1. デフォルトでコミットとタグに署名するように Git クライアントを設定する (remove `--global` to only sign by default for this repo):
   ```
   git config --global commit.gpgsign true
   git config --global gpg.format ssh
   git config --global tag.gpgSign true
   ```
2. SSH公開鍵をクリップボードにコピーします。例：
   ```
   pbcopy < ~/.ssh/id_ed25519.pub
    # Copies the contents of the id_ed25519.pub file to your clipboard
   ```
3. 次のコマンドを使用して、Git に署名するための SSH キーを設定します。引用符で囲まれた最後の文字列をクリップボード内の公開キーに置き換えます。
   ```
   git config --global user.signingkey 'ssh-ed25519 AAAAC3(...) user@example.com'
   ```

Ensure you [add your SSH key to your GitHub account](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account#adding-a-new-ssh-key-to-your-account) **as a Signing Key** (as opposed to or in addition to as an Authentication Key).

## Rebase on Git pull

Use `git pull --rebase` instead of `git pull` when pulling in changes from GitHub to your local machine. This way your local changes will always be "on top of" the latest changes on GitHub, and you avoid merge commits (which are disallowed in this repo).

You can set this to be the default behavior:

```
git config --global pull.rebase true
```

## Rebase from `main` before submitting a PR

If you are working on your own branch, run these commands before submitting a PR:

```
git fetch origin
git rebase origin/main
```
