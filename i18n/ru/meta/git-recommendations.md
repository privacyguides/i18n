---
title: Рекомендации по Git
---

Если вы вносите изменения на этом сайте непосредственно в веб-редакторе GitHub.com, вам не стоит беспокоиться об этом. Если вы разрабатываете локально и/или являетесь долгосрочным редактором веб-сайта (который, вероятно, должен разрабатывать локально!), примите во внимание эти рекомендации.

## Включите SSH Key Commit Signing

Вы можете использовать существующий SSH-ключ для подписи или [создать новый](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent).

1. Настройте ваш Git-клиент на подпись коммитов и тегов по умолчанию (удалите `--global`, чтобы подписывать по умолчанию только этот репозиторий):
   ```
   git config --global commit.gpgsign true
   git config --global gpg.format ssh
   git config --global tag.gpgSign true
   ```
2. Set your SSH key for signing in Git with the following command, substituting `/PATH/TO/.SSH/KEY.PUB` with the path to the public key you'd like to use, e.g. `/home/user/.ssh/id_ed25519.pub`:
   ```
   git config --global user.signingkey /PATH/TO/.SSH/KEY.PUB
   ```

Убедитесь, что вы [добавили свой SSH-ключ в учетную запись GitHub](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account#adding-a-new-ssh-key-to-your-account) **в качестве ключа подписи** (в отличие от ключа идентификации или в дополнение к нему).

## Rebase on Git pull

Используйте `git pull --rebase` вместо `git pull` при переносе изменений с GitHub на локальную машину. Таким образом, ваши локальные изменения всегда будут "поверх" последних изменений на GitHub, и вы избежите коммитов слияния (которые запрещены в этом репозитории).

Вы можете установить это поведение по умолчанию:

```
git config --global pull.rebase true
```

## Rebase from `main` before submitting a PR

Если вы работаете над собственной веткой, выполните эти команды перед отправкой PR:

```
git fetch origin
git rebase origin/main
```
