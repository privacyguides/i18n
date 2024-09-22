---
title: Git Recommendations
description: A guide for website contributors on using Git effectively.
---

Wenn du Änderungen an dieser Website direkt im Webeditor von GitHub.com vornimmst, solltest du dir hierüber keine Gedanken machen müssen. Wenn du lokal entwickelst und/oder ein langjähriger Website-Editor bist (der wahrscheinlich auch lokal entwickeln sollte!), solltest du diese Empfehlungen berücksichtigen.

## SSH-Schlüssel Commit-Signierung aktivieren

Du kannst einen vorhandenen SSH-Schlüssel zum Signieren verwenden oder [einen neuen Schlüssel erstellen](https://docs.github.com/de/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent).

1. Konfiguriere deinen Git-Client so, dass er Commits und Tags standardmäßig signiert (entferne `--global`, um nur für dieses Repo standardmäßig zu signieren):

    ```bash
    git config --global commit.gpgsign true
    git config --global gpg.format ssh
    git config --global tag.gpgSign true
    ```

2. Lege deinen SSH-Schlüssel für die Signierung in Git mit folgendem Befehl fest, wobei du `/PFAD/ZUM/.SSH/SCHLÜSSEL.PUB` durch den Pfad zu dem öffentlichen Schlüssel, den du verwenden möchtest, ersetzt, z. B. `/home/user/.ssh/id_ed25519.pub`:

    ```bash
    git config --global user.signingkey /PFAD/ZUM/.SSH/SCHLÜSSEL.PUB
    ```

Stelle sicher, dass du [deinen SSH-Schlüssel zu deinem GitHub-Konto](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account#adding-a-new-ssh-key-to-your-account) **als Signierschlüssel** hinzufügst (im Gegensatz zu oder zusätzlich zu einem Authentifizierungsschlüssel).

## Rebase auf Git Pull

Verwende `git pull --rebase` anstelle von `git pull`, wenn du Änderungen von GitHub auf deinen lokalen Rechner überträgst. Auf diese Weise sind deine lokalen Änderungen immer auf dem neuesten Stand der Änderungen auf GitHub, und du vermeidest Merge Commits (die in diesem Repo nicht erlaubt sind).

Du kannst dies als Standard festlegen:

```bash
git config --global pull.rebase true
```

## Rebase von `main` bevor du einen PR einreichst

Wenn du an deinem eigenen Branch arbeitest, führe diese Befehle aus, bevor du einen PR einreichst:

```bash
git fetch origin
git rebase origin/main
```
