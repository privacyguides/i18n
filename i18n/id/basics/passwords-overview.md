---
title: "Introduction to Passwords"
icon: 'material/form-textbox-password'
description: These are some tips and tricks on how to create the strongest passwords and keep your accounts secure.
---

Kata sandi adalah bagian penting dari kehidupan digital kita sehari-hari. Kami menggunakannya untuk melindungi akun, perangkat, dan rahasia kami. Meskipun sering kali menjadi satu-satunya hal antara kita dan musuh yang mengincar informasi pribadi kita, tidak banyak yang memikirkannya, yang sering kali membuat orang menggunakan kata sandi yang dapat dengan mudah ditebak atau dipaksakan.

## Praktik Terbaik

### Gunakan kata sandi yang unik untuk setiap layanan

Bayangkan ini; Anda mendaftar untuk akun dengan email dan kata sandi yang sama pada beberapa layanan daring. Jika salah satu dari penyedia layanan tersebut jahat, atau layanan mereka mengalami pembobolan data yang mengekspos kata sandi Anda dalam format yang tidak terenkripsi, maka yang harus dilakukan oleh pelaku kejahatan adalah mencoba kombinasi email dan kata sandi tersebut pada beberapa layanan populer hingga berhasil. Tidak masalah seberapa kuat satu kata sandi itu, karena mereka sudah memilikinya.

Ini disebut [credential stuffing](https://en.wikipedia.org/wiki/Credential_stuffing), dan merupakan salah satu cara paling umum akun Anda dapat disusupi oleh pihak-pihak yang tidak bertanggung jawab. To avoid this, make sure that you never re-use your passwords.

### Gunakan kata sandi yang dibuat secara acak

==You should **never** rely on yourself to come up with a good password.== We recommend using [randomly generated passwords](#passwords) or [diceware passphrases](#diceware-passphrases) with sufficient entropy to protect your accounts and devices.

Semua [pengelola kata sandi yang kami rekomendasikan](../passwords.md) menyertakan pembuat kata sandi bawaan yang dapat Anda gunakan.

### Memutar Kata Sandi

You should avoid changing passwords that you have to remember (such as your password manager's master password) too often unless you have reason to believe it has been compromised, as changing it too often exposes you to the risk of forgetting it.

When it comes to passwords that you don't have to remember (such as passwords stored inside your password manager), if your [threat model](threat-modeling.md) calls for it, we recommend going through important accounts (especially accounts that don't use multifactor authentication) and changing their password every couple of months, in case they have been compromised in a data breach that hasn't become public yet. Sebagian besar pengelola kata sandi memungkinkan Anda untuk mengatur tanggal kedaluwarsa untuk kata sandi Anda agar lebih mudah dikelola.

<div class="admonition tip" markdown>
<p class="admonition-title">Checking for data breaches</p>

If your password manager lets you check for compromised passwords, make sure to do so and promptly change any password that may have been exposed in a data breach. Sebagai alternatif, Anda dapat mengikuti [Have I Been Pwned's Latest Breaches feed](https://feeds.feedburner.com/HaveIBeenPwnedLatestBreaches) dengan bantuan [news aggregator](../news-aggregators.md).

</div>

## Membuat kata sandi yang kuat

### Kata sandi

Banyak layanan yang memberlakukan kriteria tertentu dalam hal kata sandi, termasuk panjang minimum atau maksimum, serta karakter khusus apa saja, jika ada, yang dapat digunakan. You should use your password manager's built-in password generator to create passwords that are as long and complex as the service will allow by including capitalized and lowercase letters, numbers and special characters.

Jika Anda memerlukan kata sandi yang dapat Anda hafal, kami merekomendasikan [kata sandi diceware](#diceware-passphrases).

### Diceware Passphrases

Diceware adalah sebuah metode untuk membuat kata sandi yang mudah diingat, tetapi sulit ditebak.

Diceware passphrases are a great option when you need to memorize or manually input your credentials, such as for your password manager's master password or your device's encryption password.

An example of a diceware passphrase is `viewable fastness reluctant squishy seventeen shown pencil`.

To generate a diceware passphrase using real dice, follow these steps:

<div class="admonition Note" markdown>
<p class="admonition-title">Note</p>

These instructions assume that you are using [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) to generate the passphrase, which requires five dice rolls per word. Other word lists may require more or less rolls per word, and may require a different amount of words to achieve the same entropy.

</div>

1. Lempar dadu enam sisi sebanyak lima kali, catat nomornya setelah setiap lemparan.

2. As an example, let's say you rolled `2-5-2-6-6`. Look through the [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) for the word that corresponds to `25266`.

3. Anda akan menemukan kata `mengenkripsi`. Tuliskan kata itu.

4. Ulangi proses ini hingga kata sandi Anda memiliki kata sebanyak yang Anda butuhkan, yang harus Anda pisahkan dengan spasi.

<div class="admonition warning" markdown>
<p class="admonition-title">Important</p>

You should **not** re-roll words until you get a combination of words that appeal to you. The process should be completely random.

</div>

If you don't have access to or would prefer to not use real dice, you can use your password manager's built-in password generator, as most of them have the option to generate diceware passphrases in addition to regular passwords.

We recommend using [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) to generate your diceware passphrases, as it offers the exact same security as the original list, while containing words that are easier to memorize. There are also [word lists in different languages](https://theworld.com/~reinhold/diceware.html#Diceware%20in%20Other%20Languages|outline), if you do not want your passphrase to be in English.

<details class="note" markdown>
<summary>Explanation of entropy and strength of diceware passphrases</summary>

To demonstrate how strong diceware passphrases are, we'll use the aforementioned seven word passphrase (`viewable fastness reluctant squishy seventeen shown pencil`) and [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) as an example.

One metric to determine the strength of a diceware passphrase is how much entropy it has. The entropy per word in a diceware passphrase is calculated as <math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <mtext>WordsInList</mtext> <mo form="postfix" stretchy="false">)</mo> </mrow> </math> and the overall entropy of the passphrase is calculated as: <math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <msup> <mtext>WordsInList</mtext> <mtext>WordsInPhrase</mtext> </msup> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>

Therefore, each word in the aforementioned list results in ~12.9 bits of entropy (<math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <mn>7776</mn> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>), and a seven word passphrase derived from it has ~90.47 bits of entropy (<math> <mrow> <msub> <mtext>log</mtext> <mn>2</mn> </msub> <mo form="prefix" stretchy="false">(</mo> <msup> <mn>7776</mn> <mn>7</mn> </msup> <mo form="postfix" stretchy="false">)</mo> </mrow> </math>).

The [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) contains 7776 unique words. To calculate the amount of possible passphrases, all we have to do is <math> <msup> <mtext>WordsInList</mtext> <mtext>WordsInPhrase</mtext> </msup> </math>, or in our case, <math><msup><mn>7776</mn><mn>7</mn></msup></math>.

Let's put all of this in perspective: A seven word passphrase using [EFF's large word list](https://eff.org/files/2016/07/18/eff_large_wordlist.txt) is one of ~1,719,070,799,748,422,500,000,000,000 possible passphrases.

On average, it takes trying 50% of all the possible combinations to guess your phrase. With that in mind, even if your adversary is capable of ~1,000,000,000,000 guesses per second, it would still take them ~27,255,689 years to guess your passphrase. That is the case even if the following things are true:

- Musuh Anda tahu bahwa Anda menggunakan metode diceware.
- Your adversary knows the specific word list that you used.
- Musuh Anda mengetahui berapa banyak kata yang terkandung dalam kata sandi Anda.

</details>

Singkatnya, kata sandi diceware adalah pilihan terbaik Anda ketika Anda membutuhkan sesuatu yang mudah diingat *dan* sangat kuat.

## Menyimpan Kata Sandi

### Pengelola Kata Sandi

Cara terbaik untuk menyimpan kata sandi Anda adalah dengan menggunakan pengelola kata sandi. They allow you to store your passwords in a file or in the cloud and protect them with a single master password. Dengan begitu, Anda hanya perlu mengingat satu kata sandi yang kuat, yang memungkinkan Anda mengakses kata sandi lainnya.

There are many good options to choose from, both cloud-based and local. Pilih salah satu pengelola kata sandi yang kami rekomendasikan dan gunakan untuk membuat kata sandi yang kuat di semua akun Anda. We recommend securing your password manager with a [diceware passphrase](#diceware-passphrases) comprised of at least seven words.

[Daftar pengelola kata sandi yang direkomendasikan](../passwords.md ""){.md-button}

<div class="admonition warning" markdown>
<p class="admonition-title">Don't place your passwords and TOTP tokens inside the same password manager</p>

When using [TOTP codes as multifactor authentication](multi-factor-authentication.md#time-based-one-time-password-totp), the best security practice is to keep your TOTP codes in a [separate app](../multi-factor-authentication.md).

Storing your TOTP tokens in the same place as your passwords, while convenient, reduces the accounts to a single factor in the event that an adversary gains access to your password manager.

Selain itu, kami tidak menyarankan untuk menyimpan kode pemulihan sekali pakai di pengelola kata sandi Anda. Data tersebut harus disimpan secara terpisah, misalnya dalam wadah terenkripsi pada perangkat penyimpanan offline.

</div>

### Cadangan

You should store an [encrypted](../encryption.md) backup of your passwords on multiple storage devices or a cloud storage provider. Hal ini dapat membantu Anda mengakses kata sandi jika terjadi sesuatu pada perangkat utama atau layanan yang Anda gunakan.
