---
title: Raccomandazioni Git
---

Se apporti modifiche a questo sito web dall'editor web di GitHub.com, non dovresti preoccuparti di questo. Se stai sviluppando a livello locale e/o siete editor di siti web a lungo termine (che probabilmente dovrebbero sviluppare a livello locale!), segui queste raccomandazioni.

## Abilita la firma per i commit tramite chiave SSH

Puoi usare una chiave SSH già esistente per firmare, o[creane una nuova](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent).

1. Configura il tuo client Git per firmare i commit e i tag in modo predefinito (rimuovere `--global` per firmare solo in modo predefinito per questa repo):
   ```
   git config --global commit.gpgsign true
   git config --global gpg.format ssh
   git config --global tag.gpgSign true
   ```
2. Copia la tua chiave pubblica SSH negli appunti, per esempio:
   ```
   pbcopy < ~/.ssh/id_ed25519.pub
    # Copies the contents of the id_ed25519.pub file to your clipboard
   ```
3. Imposta la tua chiave SSH per firmare in Git con il comando seguente, sostituendo l'ultima stringa tra virgolette con la tua chiave pubblica negli appunti:
   ```
   git config --global user.signingkey 'ssh-ed25519 AAAAC3(...) user@example.com'
   ```

Assicuarti di [aggiungere la tua chiave SSH al tuo account GitHub](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account#adding-a-new-ssh-key-to-your-account) **come Signing Key** (al contrario o in aggiunta alla Authentication Key).

## Rebase su Git pull

Usa `git pull --rebase` invece di `git pull` quando estrai le modifiche da GitHub alla tua macchina locale. In questo modo le modifiche locali saranno sempre "in cima" alle ultime modifiche su GitHub, evitando cosi i commit di unione (che non sono permessi in questa repo).

È possibile impostare questa funzione come predefinita:

```
git config --global pull.rebase true
```

## Rebase da`main`prima di inviare una PR

Se stai lavorando sulla tua branch, esegui questi comandi prima di inviare una PR:

```
git fetch origin
git rebase origin/main
```
