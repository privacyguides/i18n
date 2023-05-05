---
meta_title: "How to Create Internet Accounts Privately - Privacy Guides"
title: "Pembuatan Akun"
icon: 'material/account-plus'
description: Membuat akun online bisa dibilang merupakan kebutuhan internet, lakukan langkah-langkah ini untuk memastikan Anda tetap privat.
---

Seringkali orang mendaftar untuk layanan tanpa berpikir. Mungkin itu adalah layanan streaming sehingga Anda dapat menonton acara baru yang dibicarakan semua orang, atau akun yang memberi Anda diskon untuk tempat makanan cepat saji favorit Anda. Apa pun masalahnya, Anda harus mempertimbangkan implikasi untuk data Anda sekarang dan di kemudian hari.

Ada risiko yang terkait dengan setiap layanan baru yang Anda gunakan. Pelanggaran data; pengungkapan informasi pelanggan kepada pihak ketiga; karyawan nakal yang mengakses data; semuanya adalah kemungkinan yang harus dipertimbangkan ketika memberikan informasi Anda. Anda harus yakin bahwa Anda bisa mempercayai layanan ini, itulah sebabnya kami tidak menyarankan untuk menyimpan data berharga pada apa pun kecuali pada produk yang paling matang dan telah teruji. Hal ini biasanya berarti layanan yang menyediakan E2EE dan telah menjalani audit kriptografi. Audit meningkatkan jaminan bahwa produk dirancang tanpa masalah keamanan mencolok yang disebabkan oleh pengembang yang tidak berpengalaman.

Mungkin juga sulit untuk menghapus akun pada beberapa layanan. Terkadang [menimpa data](account-deletion.md#overwriting-account-information) yang terkait dengan akun dapat dilakukan, tetapi dalam kasus lain layanan akan menyimpan seluruh riwayat perubahan pada akun.

## Ketentuan Layanan & Kebijakan Privasi

ToS adalah peraturan yang Anda setujui untuk diikuti saat menggunakan layanan. Pada layanan yang lebih besar aturan-aturan ini sering kali ditegakkan oleh sistem otomatis. Terkadang sistem otomatis ini bisa membuat kesalahan. Sebagai contoh, Anda mungkin diblokir atau dikunci dari akun Anda pada beberapa layanan karena menggunakan nomor VPN atau VOIP. Mengajukan banding atas larangan semacam itu sering kali sulit, dan melibatkan proses otomatis juga, yang tidak selalu berhasil. Ini akan menjadi salah satu alasan mengapa kami tidak menyarankan menggunakan Gmail untuk email sebagai contoh. Email sangat penting untuk akses ke layanan lain yang mungkin telah Anda daftarkan.

Kebijakan Privasi adalah bagaimana layanan mengatakan bahwa mereka akan menggunakan data Anda dan perlu dibaca agar Anda memahami bagaimana data Anda akan digunakan. Perusahaan atau organisasi mungkin tidak diwajibkan secara hukum untuk mengikuti semua yang tercantum dalam kebijakan (tergantung pada yurisdiksi). Kami sarankan Anda mengetahui undang-undang setempat dan apa yang diizinkan oleh penyedia layanan untuk dikumpulkan.

Sebaiknya cari istilah-istilah tertentu seperti "pengumpulan data", "analisis data", "cookie", "iklan", atau layanan "pihak ketiga". Kadang-kadang Anda dapat memilih untuk tidak ikut serta dalam pengumpulan data atau membagikan data Anda, tetapi yang terbaik adalah memilih layanan yang menghormati privasi Anda sejak awal.

Ingatlah bahwa Anda juga menaruh kepercayaan pada perusahaan atau organisasi tersebut dan bahwa mereka akan mematuhi kebijakan privasi mereka sendiri.

## Metode autentikasi

Biasanya ada beberapa cara untuk mendaftar akun, masing-masing dengan kelebihan dan kekurangannya sendiri.

### Email dan kata sandi

Cara paling umum untuk membuat akun baru adalah dengan alamat email dan kata sandi. Saat menggunakan metode ini, Anda harus menggunakan pengelola kata sandi dan mengikuti [praktik terbaik](passwords-overview.md) mengenai kata sandi.

!!! tip

    You can use your password manager to organize other authentication methods too! Just add the new entry and fill the appropriate fields, you can add notes for things like security questions or a backup key.

Anda akan bertanggung jawab untuk mengelola kredensial login Anda. Untuk keamanan tambahan, Anda dapat mengatur [MFA](multi-factor-authentication.md) pada akun Anda.

[Pengelola kata sandi yang direkomendasikan](../passwords.md ""){.md-button}

#### Alias surel

Jika Anda tidak ingin memberikan alamat surel asli Anda ke layanan, Anda memiliki opsi untuk menggunakan alias. Kami menjelaskannya secara lebih rinci di halaman rekomendasi layanan surel kami. Pada dasarnya, layanan alias memungkinkan Anda untuk membuat alamat surel baru yang meneruskan semua surel ke alamat utama Anda. Hal ini dapat membantu mencegah pelacakan di seluruh layanan dan membantu Anda mengelola surel pemasaran yang terkadang menyertai proses pendaftaran. Semua itu dapat disaring secara otomatis berdasarkan alias yang dikirim.

Jika layanan diretas, Anda mungkin akan mulai menerima surel phishing atau spam ke alamat yang Anda gunakan untuk mendaftar. Using unique aliases for each service can assist in identifying exactly what service was hacked.

[Recommended email aliasing services](../email.md#email-aliasing-services ""){.md-button}

### "Sign in with..." (OAuth)

OAuth is an authentication protocol that allows you to register for a service without sharing much information with the service provider, if any, by using an existing account you have with another service instead. Whenever you see something along the lines of "Sign in with *provider name*" on a registration form, it's typically using OAuth.

When you sign in with OAuth, it will open a login page with the provider you choose, and your existing account and new account will be connected. Your password won't be shared, but some basic information typically will (you can review it during the login request). Proses ini diperlukan setiap kali Anda ingin masuk ke akun yang sama.

Keuntungan utama adalah:

- **Security**: no risk of being involved in a [data breach](https://en.wikipedia.org/wiki/Data_breach) because the website does not store your credentials.
- **Ease of use**: multiple accounts are managed by a single login.

Tetapi ada kelemahan:

- **Privacy**: the OAuth provider you log in with will know the services you use.
- **Centralization**: if the account you use for OAuth is compromised or you aren't able to login to it, all other accounts connected to it are affected.

OAuth authentication can be especially useful in those situations where you could benefit from deeper integration between services. Our recommendation is to limit using OAuth to only where you need it, and always protect the main account with [MFA](multi-factor-authentication.md).

All the services that use OAuth will be as secure as your underlying provider's account. For example, if you want to secure an account with a hardware key, but that service doesn't support hardware keys, you can secure the account you use with OAuth with a hardware key instead, and now you essentially have hardware MFA on all your accounts. It is worth noting though that weak authentication on your OAuth provider account means that any account tied to that login will also be weak.

### Nomor telepon

Kami sarankan untuk menghindari layanan yang memerlukan nomor telepon untuk mendaftar. Nomor telepon dapat menjadi identitas Anda di berbagai layanan dan tergantung pada perjanjian berbagi data, hal ini akan membuat penggunaan Anda lebih mudah dilacak, terutama jika salah satu layanan tersebut dibobol karena nomor telepon sering kali **tidak** dienkripsi.

Anda harus menghindari memberikan nomor telepon asli Anda jika Anda bisa. Some services will allow the use of VOIP numbers, however these often trigger fraud detection systems, causing an account to be locked down, so we don't recommend that for important accounts.

Dalam banyak kasus, Anda perlu memberikan nomor yang dapat digunakan untuk menerima SMS atau telepon, terutama saat berbelanja internasional, untuk berjaga-jaga jika terjadi masalah dengan pesanan Anda saat pemeriksaan di perbatasan. It's common for services to use your number as a verification method; don't let yourself get locked out of an important account because you wanted to be clever and give a fake number!

### Nama pengguna dan kata sandi

Beberapa layanan memungkinkan Anda untuk mendaftar tanpa menggunakan alamat email dan hanya mengharuskan Anda untuk mengatur nama pengguna dan kata sandi. Layanan ini dapat memberikan peningkatan anonimitas bila dikombinasikan dengan VPN atau Tor. Perlu diingat bahwa untuk akun-akun ini kemungkinan besar tidak akan ada **cara untuk memulihkan akun Anda** jika Anda lupa nama pengguna atau kata sandi Anda.
