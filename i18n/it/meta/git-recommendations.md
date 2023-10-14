---
title: Consigli di Git
---

Se apporti modifiche a questo sito web direttamente sull'editor web di GitHub.com, non te ne saresti dovuto preoccupare. Se stai sviluppando localmente e/o sei un editore di siti web a lungo termine (che dovrebbe probabilmente sviluppare localmente!), considera questi consigli.

## Abilitaa la Firma dei Commit con Chiave SSH

Puoi utilizzare una chiave SSH esistente per firmare, o [crearne una nuova](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent).

1. Configura il tuo client di Git per firmare i commit e i tag di default (rimuovi `--global` per firmare di default soltanto per questa repository):
   ```
   git config --global commit.gpgsign true
   git config --global gpg.format ssh
   git config --global tag.gpgSign true
   ```
2. Imposta la tua chiave SSH per accedere a Git con il seguente comando, sostituendo `/PATH/TO/.SSH/KEY. UB` con il percorso della chiave pubblica che desideri utilizzare, ad esempio `/home/user/.ssh/id_ed25519.pub`:
   ```
   git config --global user.signingkey /PATH/TO/.SSH/KEY.PUB
   ```

Assicurati di [aggiungere la tua chiave SSH al tuo profilo di GitHub](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account#adding-a-new-ssh-key-to-your-account) **come una Chiave di Firma** (invece che, od oltre che, come una Chiave d'Autenticazione).

## Rebase on Git pull

Utilizza `git pull --rebase`, invece di `git pull`, estrando le modifiche da GitHub alla tua macchina locale. Così, le tue modifiche locali saranno sempre "in cima" alle modifiche più recenti su GitHub e potrai evitare i commit di unione (non consentiti in questa repository).

Puoi impostarlo come comportamento predefinito:

```
git config --global pull.rebase true
```

## Rebase da `main` prima di inviare una PR

Se stai lavorando al tuo ramo, esegui questi comandi prima di inviare un PR:

```
git fetch origin
git rebase origin/main
```
