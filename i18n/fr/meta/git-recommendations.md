---
title: Git Recommendations
description: A guide for website contributors on using Git effectively.
---

Si vous apportez des modifications à ce site web directement sur l'éditeur web de GitHub.com, vous ne devriez pas avoir à vous en soucier. Si vous développez localement et/ou êtes un éditeur du site web à long terme (qui devrait probablement développer localement !), tenez compte de ces recommandations.

## Activer la signature de commit par clé SSH

Vous pouvez utiliser une clé SSH existante pour la signature, ou [en créer une nouvelle](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent).

1. Configurez votre client Git pour signer les commits et les tags par défaut (supprimez `--global` pour ne signer par défaut que pour ce dépôt) :

    ```bash
    git config --global commit.gpgsign true
    git config --global gpg.format ssh
    git config --global tag.gpgSign true
    ```

2. Définissez votre clé SSH pour la signature dans Git avec la commande suivante, en remplaçant `/CHEMIN/VERS/.SSH/KEY.PUB` par le chemin vers la clé publique que vous souhaitez utiliser, par exemple `/home/user/.ssh/id_ed25519.pub`:

    ```bash
    git config --global user.signingkey /CHEMIN/VERS/.SSH/KEY.PUB
    ```

Assurez-vous que vous [ajoutez votre clé SSH à votre compte GitHub](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account#adding-a-new-ssh-key-to-your-account) **en tant que clé de signature** (par opposition ou en plus qu'en tant que clé d'authentification).

## Rebase on Git pull

Utilisez `git pull --rebase` au lieu de `git pull` pour transférer les modifications de GitHub vers votre machine locale. De cette façon, vos modifications locales seront toujours "au dessus" des dernières modifications sur GitHub, et vous évitez les commits de merge (qui sont interdits dans ce dépôt).

Vous pouvez définir cette option comme étant le comportement par défaut :

```bash
git config --global pull.rebase true
```

## Rebase depuis `main` avant de soumettre une PR

Si vous travaillez sur votre propre branche, exécutez ces commandes avant de soumettre une PR :

```bash
git fetch origin
git rebase origin/main
```
