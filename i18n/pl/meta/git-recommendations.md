---
title: Zalecenia dotyczące Git
description: Przewodnik dla współtwórców tej strony na temat skutecznego korzystania z systemu Git.
---

Jeśli dokonujesz zmian na tej stronie bezpośrednio w edytorze internetowym GitHub.com, nie musisz się tym przejmować. Jeśli jednak rozwijasz projekt lokalnie i/lub jesteś stałym redaktorem strony (a w takim przypadku prawdopodobnie powinieneś pracować lokalnie!), weź pod uwagę poniższe zalecenia.

## Podpisywanie commitów za pomocą klucza SSH

Możesz użyć istniejącego klucza SSH do podpisywania lub [utworzyć nowy](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent).

1. Skonfiguruj swojego klienta Git, aby domyślnie podpisywał commity i tagi (usuń `--global`, aby domyślnie podpisywać tylko dla tego repozytorium):

    ```bash
    git config --global commit.gpgsign true
    git config --global gpg.format ssh
    git config --global tag.gpgSign true
    ```

2. Ustaw klucz SSH do podpisywania w Git za pomocą poniższegoo polecenia, zastępując `/PATH/TO/.SSH/KLUCZ.PUB` ścieżką do klucza publicznego, którego chcesz użyć, np. `/home/user/.ssh/id_ed25519.pub`:

    ```bash
    git config --global user.signingkey /PATH/TO/.SSH/KLUCZ.PUB
    ```

Upewnij się, że [dodajesz swój klucz SSH do konta GitHub](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account#adding-a-new-ssh-key-to-your-account) **jako klucz podpisu (Signing Key)** — zamiast lub oprócz klucza uwierzytelniającego (Authentication Key).

## Przeprowadź rebase przy git pull

Zamiast polecenia `git pull` użyj polecenia `git pull --rebase` podczas pobierania zmian z GitHuba na swój komputer lokalny. Dzięki temu Twoje lokalne zmiany będą zawsze „nad” najnowszymi zmianami z GitHuba, a dodatkowo unikniesz commitów scalających (merge commits), które są niedozwolone w tym repozytorium.

Możesz ustawić to jako domyślne zachowanie poleceniem:

```bash
git config --global pull.rebase true
```

## Przeprowadź rebase z gałęzi `main` przed wysłaniem PR-a

Jeśli pracujesz na własnej gałęzi, uruchom poniższe polecenia przed zgłoszeniem pull requesta (PR):

```bash
git fetch origin
git rebase origin/main
```
