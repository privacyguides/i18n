---
title: Git Recommendations
description: A guide for website contributors on using Git effectively.
---

اگر مستقیماً در ویرایشگر وب GitHub.com تغییراتی را در این وب سایت ایجاد می‌کنید، نباید نگران این موضوع باشید. اگر به صورت محلی در حال توسعه هستید و/یا یک ویرایشگر طولانی مدت وب سایت هستید (که احتمالاً باید به صورت محلی در حال توسعه باشد!)، این توصیه ها را در نظر بگیرید.

## SSH Key Commit Signing را فعال کنید

می توانید از یک کلید SSH موجود برای امضا استفاده کنید، یا[جدیدش را بسازید](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent).

1. کلاینت Git خود را تنظیم کنید تا به طور پیش‌فرض commitها و برچسب‌ها را امضا کند (`--global` را حذف کنید تا فقط به‌طور پیش‌فرض برای این مخزن امضا شود):

    ```bash
    git config --global commit.gpgsign true
    git config --global gpg.format ssh
    git config --global tag.gpgSign true
    ```

2. Set your SSH key for signing in Git with the following command, substituting `/PATH/TO/.SSH/KEY.PUB` with the path to the public key you'd like to use, e.g. `/home/user/.ssh/id_ed25519.pub`:

    ```bash
    git config --global user.signingkey /PATH/TO/.SSH/KEY.PUB
    ```

مطمئن شوید که [ کلید خصوصی خود را به اکانت GitHub اضافه کنید](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account#adding-a-new-ssh-key-to-your-account) **به عنوان کلید امضا شده** (برخلاف یا علاوه بر آن به عنوان یک کلید احراز هویت).

## دوباره بر روی Git pull قرار دهید

به جای `git pull` از `git pull --rebase` هنگام اعمال تغییرات از GitHub به دستگاه محلی خود استفاده کنید. به این ترتیب تغییرات محلی شما همیشه "در بالای" آخرین تغییرات در GitHub خواهد بود و از ادغام commit (که در این مخزن غیرمجاز هستند) اجتناب می کنید.

می توانید این را به عنوان رفتار پیش فرض تنظیم کنید:

```bash
git config --global pull.rebase true
```

## قبل از ارسال یک PR، از `main` بازنویسی کنید

اگر روی branch خود کار می کنید، این دستورها را قبل از ارسال یک PR اجرا کنید:

```bash
git fetch origin
git rebase origin/main
```
