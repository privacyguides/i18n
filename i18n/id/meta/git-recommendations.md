---
title: Git Recommendations
description: A guide for website contributors on using Git effectively.
---

Jika Anda membuat perubahan pada situs web ini di editor web GitHub.com secara langsung, Anda tidak perlu khawatir tentang hal ini. Jika Anda mengembangkan secara lokal dan/atau merupakan editor situs web jangka panjang (yang mungkin harus mengembangkan secara lokal!), pertimbangkan rekomendasi ini.

## Aktifkan Penandatanganan Komit dengan Kunci SSH

Anda dapat menggunakan kunci SSH yang sudah ada untuk masuk, atau [membuat kunci baru](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent).

1. Konfigurasikan klien Git Anda untuk menandatangani komit dan tag secara default (hapus `--global` untuk hanya menandatangani secara bawaan untuk repo ini):

    ```bash
    git config --global commit.gpgsign true
    git config --global gpg.format ssh
    git config --global tag.gpgSign true
    ```

2. Atur kunci SSH Anda untuk masuk ke Git dengan perintah berikut, mengggantikan `/PATH/TO/.SSH/KEY.PUB` dengan jalur ke kunci publik yang ingin Anda gunakan, mis. `/home/user/.ssh/id_ed25519.pub`:

    ```bash
    git config --global user.signingkey /PATH/TO/.SSH/KEY.PUB
    ```

Pastikan Anda [menambahkan kunci SSH Anda ke akun GitHub](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account#adding-a-new-ssh-key-to-your-account) **Signing Key** (sebagai lawan atau tambahan dari Kunci Autentikasi).

## Rebase pada tarikan Git

Gunakan `git pull --rebase` alih-alih `git pull` saat menarik perubahan dari GitHub ke mesin lokal Anda. Dengan cara ini perubahan lokal Anda akan selalu "di atas" perubahan terbaru di GitHub, dan Anda menghindari komit gabungan (yang dilarang dalam repo ini).

Anda dapat mengatur ini menjadi perilaku default:

```bash
git config --global pull.rebase true
```

## Rebase dari `utama` sebelum mengirimkan PR

Jika Anda bekerja pada cabang Anda sendiri, jalankan perintah ini sebelum mengirimkan PR:

```bash
git fetch origin
git rebase origin/main
```
