---
title: Git 使用建議
---

如果想直接在 github.com 網頁編輯器對本站進行修改，則無須擔心此處的建議。 如您使用本地端開發或長期網站編編器(可能為本地端)，請參考以下建議。

## 開啟 SSH 密鑰提交簽署

可使用現有的SSH 密鑰簽署或 [建立新密鑰one](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)。

1. 設置 Git 客戶端以預設簽署提交與標籤(移除 `--global` 以便只對此存取庫作簽署):

    ```bash
    git config --global commit.gpgsign true
    git config --global gpg.format ssh
    git config --global tag.gpgSign true
    ```

2. 透過下方指令來設定簽署 Git 的 SSH 密鑰，把 `/PATH/TO/.SSH/KEY.PUB` 替換成存放公鑰的路徑，如 `/home/user/.ssh/id_ed25519.pub`:

    ```bash
    git config --global user.signingkey /PATH/TO/.SSH/KEY.PUB
    ```

確認 [加入您 GitHub 帳戶中的 SSH 密鑰](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account#adding-a-new-ssh-key-to-your-account) **簽署密鑰** (其不同於驗證密鑰)。

## Rebase on Git pull

使用 `git pull --rebase` 取代 `git pull` 以從 Github 把變動提取回本地端機器。 這種方式會使本地端的變動總在 Github 之上，而您可避免合併提交(本取存庫亦不允許)。

可將它設為默認行為:

```bash
git config --global pull.rebase true
```

## 發送提取請求前，先自 `main`重整。

如果是在自建的旁支工作，提取請求前先執行這些指令:

```bash
git fetch origin
git rebase origin/main
```
