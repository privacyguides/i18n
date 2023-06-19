---
title: Recomendações Git
---

Se fizer alterações a este site diretamente no editor web disponível em GitHub.com, não terá de se preocupar com isto. Se estiver a desenvolver localmente e/ou for um editor de websites com longa experiência (que provavelmente deveria estar a desenvolver localmente!), considere estas recomendações.

## Ativar a assinatura de compromisso de chave SSH

Para assinar, pode utilizar uma chave SSH existente, ou [criar uma nova](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent).

1. Configure o seu cliente Git para assinar commits e tags por predefinição (remova `--global` para assinar apenas por predefinição para este repositório):
   ```
   git config --global commit.gpgsign true
   git config --global gpg.format ssh
   git config --global tag.gpgSign true
   ```
2. Copie a sua chave pública SSH para a área de transferência, por exemplo:
   ```
   pbcopy < ~/.ssh/id_ed25519.pub
    # Copies the contents of the id_ed25519.pub file to your clipboard
   ```
3. Defina a sua chave SSH para assinar no Git, com o seguinte comando, substituindo a última cadeia de carateres entre aspas pela chave pública, que está na sua área de transferência:
   ```
   git config --global user.signingkey 'ssh-ed25519 AAAAC3(...) user@example.com'
   ```

Certifique-se de que [adiciona a sua chave SSH à sua conta GitHub](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account#adding-a-new-ssh-key-to-your-account) **como uma chave de assinatura** (por oposição a, ou para além de uma chave de autenticação).

## Rebase no Git pull

Use `git pull --rebase` em vez de `git pull`, ao puxar as alterações do GitHub para a sua máquina local. Desta forma, as suas alterações locais estarão sempre "no topo" das alterações mais recentes no GitHub, evitando o merge de commits (que não são permitidos neste repositório).

Pode definir o seguinte comportamento como predefinido:

```
git config --global pull.rebase true
```

## Rebase de `main` antes de submeter um PR

Se estiver a trabalhar no seu próprio branch, execute estes comandos, antes de submeter um PR:

```
git fetch origin
git rebase origin/main
```
