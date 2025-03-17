---
title: Recomendações para o uso do Git
description: Um guia para colaboradores de sites para contribuir efetivamente utilizando a plataforma Git.
---

Se você alterar este site diretamente no editor da Web do GitHub.com, você não precisará se preocupar com isso. Se você estiver desenvolvendo localmente e/ou for um editor de sites de longo prazo (que provavelmente deveria estar desenvolvendo localmente!), considere estas recomendações.

## Ativar *SSH Key Commit Signing* (assinatura de submissões via SSH)

É possível utilizar uma chave SSH existente para assinatura ou [criar uma nova chave](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent).

1. Configure seu cliente Git para assinar commits e tags por padrão (remova a configuração `--global` para assinar apenas por padrão para este repositório):

    ```bash
    git config --global commit.gpgsign true
    git config --global gpg.format ssh
    git config --global tag.gpgSign true
    ```

2. Defina sua chave SSH para assinatura no Git com o seguinte comando, substituindo `/PATH/TO/.SSH/KEY.PUB` pelo diretório/ *path* da chave pública que você deseja usar, por exemplo, `/home/user/.ssh/id_ed25519.pub`:

    ```bash
    git config --global user.signingkey /PATH/TO/.SSH/KEY.PUB
    ```

Certifique-se de adicionar [sua chave SSH à sua conta do GitHub](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account#adding-a-new-ssh-key-to-your-account) como uma chave do tipo **assinatura** (além de uma chave de autenticação).

## *Rebase* no Git pull

Você deve `git pull --rebase` em vez de `git pull` ao puxar as alterações do GitHub para sua máquina local. Dessa maneira, suas alterações locais sempre estarão "no topo" das alterações mais recentes no GitHub, e você evita <en>commits</em>/submissões de *merge* mesclagem (que não são permitidos neste repositório).

Você pode definir essa configuração comportamento padrão:

```bash
git config --global pull.rebase true
```

## *Rebase* do `código principal` antes de enviar um PR

Se no caso estiver trabalhando em sua própria ramificação/*branch*, execute os seguintes comandos comandos antes de enviar um *pull request*:

```bash
git fetch origin
git rebase origin/main
```
