---
title: "Kesalahpahaman Umum"
icon: 'material/robot-confused'
description: Privasi bukanlah topik yang mudah, dan mudah sekali terjebak dalam klaim pemasaran dan disinformasi lainnya.
schema:
  - 
    "@context": https://schema.org
    "@type": FAQPage
    mainEntity:
      - 
        "@type": Question
        name: Apakah perangkat lunak sumber terbuka aman secara inheren?
        acceptedAnswer:
          "@type": Answer
          text: |
            Whether the source code is available and how software is licensed does not inherently affect its security in any way. Open-source software has the potential to be more secure than proprietary software, but there is absolutely no guarantee this is the case. When you evaluate software, you should look at the reputation and security of each tool on an individual basis.
      - 
        "@type": Question
        name: Can shifting trust to another provider increase privacy?
        acceptedAnswer:
          "@type": Answer
          text: |
            Kami banyak membicarakan tentang "pergeseran kepercayaan" saat membahas solusi seperti VPN (yang menggeser kepercayaan yang Anda tempatkan pada ISP Anda ke penyedia VPN). While this protects your browsing data from your ISP specifically, the VPN provider you choose still has access to your browsing data: Your data isn't completely secured from all parties.
      - 
        "@type": Question
        name: Are privacy-focused solutions inherently trustworthy?
        acceptedAnswer:
          "@type": Answer
          text: |
            Berfokus hanya pada kebijakan privasi dan pemasaran sebuah alat atau penyedia layanan bisa membutakan Anda terhadap kelemahannya. Ketika Anda mencari solusi yang lebih pribadi, Anda harus menentukan apa masalah yang mendasarinya dan menemukan solusi teknis untuk masalah tersebut. Sebagai contoh, Anda mungkin ingin menghindari Google Drive, yang memberikan akses ke semua data Anda kepada Google. The underlying problem in this case is lack of E2EE, so you should make sure that the provider you switch to actually implements E2EE, or use a tool (like Cryptomator) which provides E2EE on any cloud provider. Beralih ke penyedia yang "berfokus pada privasi" (yang tidak menerapkan E2EE) tidak akan menyelesaikan masalah Anda: ini hanya mengalihkan kepercayaan dari Google ke penyedia tersebut.
      - 
        "@type": Question
        name: How complicated should my threat model be?
        acceptedAnswer:
          "@type": Answer
          text: |
            Kami sering melihat orang menggambarkan model ancaman privasi yang terlalu rumit. Sering kali, solusi ini mencakup masalah seperti banyak akun email yang berbeda atau pengaturan yang rumit dengan banyak bagian dan kondisi yang bergerak. The replies are usually answers to "What is the best way to do X?"
            Menemukan solusi "terbaik" untuk diri Anda sendiri tidak selalu berarti Anda mencari solusi yang sempurna dengan lusinan kondisi—solusi ini sering kali sulit untuk diterapkan secara realistis. Seperti yang telah kami bahas sebelumnya, keamanan sering kali mengorbankan kenyamanan.
---

## "Perangkat lunak sumber terbuka selalu aman" atau "Perangkat lunak sumber tertutup lebih aman"

Mitos-mitos ini berasal dari sejumlah prasangka, tetapi apakah kode sumber tersedia dan bagaimana perangkat lunak dilisensikan tidak secara inheren memengaruhi keamanannya dengan cara apa pun. ==Perangkat lunak sumber terbuka memiliki *potensi* untuk lebih aman daripada perangkat lunak sumber tertutup, tetapi sama sekali tidak ada jaminan bahwa hal ini benar adanya.== Ketika Anda mengevaluasi perangkat lunak, Anda harus melihat reputasi dan keamanan setiap alat secara individu.

Perangkat lunak sumber terbuka *dapat* diaudit oleh pihak ketiga, dan sering kali lebih transparan mengenai potensi kerentanan daripada perangkat lunak sumber tertutup. Ini juga memungkinkan Anda untuk meninjau kode dan menonaktifkan fungsionalitas yang mencurigakan yang Anda temukan. Namun, *kecuali jika Anda melakukannya*, tidak ada jaminan bahwa kode pernah dievaluasi, terutama dengan proyek perangkat lunak yang lebih kecil. The open development process has also sometimes been exploited to introduce new vulnerabilities known as <span class="pg-viridian">:material-package-variant-closed-remove: Supply Chain Attacks</span>, which are discussed further in our [Common Threats](common-threats.md) page.[^1]

Di sisi lain, perangkat lunak sumber tertutup itu kurang transparan, tetapi bukan berarti tidak aman. Proyek-proyek perangkat lunak sumber tertutup utama dapat diaudit secara internal dan oleh lembaga pihak ketiga, dan para peneliti keamanan independen masih bisa menemukan kerentanan dengan teknik seperti rekayasa balik.

Untuk menghindari keputusan yang memiliki bias, ini sangat *penting* bagi Anda untuk mengevaluasi standar privasi dan keamanan perangkat lunak yang Anda gunakan.

## "Menggeser kepercayaan dapat meningkatkan privasi"

Kami banyak membicarakan tentang "pergeseran kepercayaan" saat membahas solusi seperti VPN (yang menggeser kepercayaan yang Anda tempatkan pada ISP Anda ke penyedia VPN). Meskipun ini melindungi data penjelajahan Anda dari ISP Anda *secara khusus*, penyedia VPN yang Anda pilih masih memiliki akses ke data penjelajahan Anda: Data Anda tidak sepenuhnya aman dari semua pihak. Ini berarti bahwa:

1. Anda harus berhati-hati saat memilih penyedia untuk mengalihkan kepercayaan.
2. Anda tetap harus menggunakan teknik lain, seperti E2EE, untuk melindungi data Anda sepenuhnya. Hanya dengan tidak mempercayai satu penyedia layanan untuk mempercayai penyedia layanan lainnya tidak akan mengamankan data Anda.

## "Solusi yang berfokus pada privasi pada dasarnya dapat dipercaya"

Berfokus hanya pada kebijakan privasi dan pemasaran sebuah alat atau penyedia layanan bisa membutakan Anda terhadap kelemahannya. Ketika Anda mencari solusi yang lebih pribadi, Anda harus menentukan apa masalah yang mendasarinya dan menemukan solusi teknis untuk masalah tersebut. Sebagai contoh, Anda mungkin ingin menghindari Google Drive, yang memberikan akses ke semua data Anda kepada Google. Masalah yang mendasari dalam kasus ini adalah kurangnya E2EE, jadi Anda harus memastikan bahwa penyedia yang Anda pilih benar-benar mengimplementasikan E2EE, atau menggunakan alat bantu (seperti [Cryptomator](../encryption.md#cryptomator-cloud)) yang menyediakan E2EE pada penyedia cloud mana pun. Beralih ke penyedia yang "berfokus pada privasi" (yang tidak menerapkan E2EE) tidak akan menyelesaikan masalah Anda: ini hanya mengalihkan kepercayaan dari Google ke penyedia tersebut.

Kebijakan privasi dan praktik bisnis penyedia yang Anda pilih sangat penting, tetapi harus dianggap nomor dua setelah jaminan teknis privasi Anda: Anda seharusnya tidak boleh mengalihkan kepercayaan ke penyedia lain ketika mempercayai penyedia sama sekali tidak menjadi persyaratan.

## "Rumit itu lebih baik"

Kami sering melihat orang menggambarkan model ancaman privasi yang terlalu rumit. Sering kali, solusi ini mencakup masalah seperti banyak akun email yang berbeda atau pengaturan yang rumit dengan banyak bagian dan kondisi yang bergerak. Balasan biasanya berupa jawaban atas pertanyaan "Apa cara terbaik untuk melakukan *X*?"

Menemukan solusi "terbaik" untuk diri Anda sendiri tidak selalu berarti Anda mencari solusi yang sempurna dengan lusinan kondisi—solusi ini sering kali sulit untuk diterapkan secara realistis. Seperti yang telah kami bahas sebelumnya, keamanan sering kali mengorbankan kenyamanan. Di bawah ini, kami memberikan beberapa kiat:

1. ==Tindakan harus memiliki tujuan tertentu:== Pikirkan tentang cara melakukan apa yang Anda inginkan dengan tindakan yang paling sedikit.
2. ==Menghilangkan titik-titik kegagalan manusia:== Kita gagal, lelah, dan melupakan hal-hal. Untuk menjaga keamanan, hindari mengandalkan kondisi dan proses manual yang harus Anda ingat.
3. ==Gunakan tingkat perlindungan yang tepat untuk apa yang Anda inginkan.== Kami sering melihat rekomendasi yang disebut sebagai solusi penegakan hukum atau solusi antisomasi. Hal ini sering kali membutuhkan pengetahuan khusus dan umumnya tidak sesuai dengan keinginan banyak orang. Tidak ada gunanya membangun model ancaman yang rumit untuk anonimitas jika Anda dapat dengan mudah dibocorkan identitasnya hanya karena sebuah kesalahan.

Jadi, bagaimana ini terlihat?

Salah satu model ancaman yang paling jelas adalah model di mana orang *tahu siapa Anda* dan model di mana mereka tidak tahu. Di situ akan selalu ada situasi di mana Anda harus menyatakan nama resmi Anda dan ada situasi lain di mana Anda tidak perlu melakukannya.

1. **Known identity** - A known identity is used for things where you must declare your name. There are many legal documents and contracts where a legal identity is required. This could range from opening a bank account, signing a property lease, obtaining a passport, customs declarations when importing items, or otherwise dealing with your government. These things will usually lead to credentials such as credit cards, credit rating checks, account numbers, and possibly physical addresses.

    We don't suggest using a VPN or Tor for any of these things, as your identity is already known through other means.

    <div class="admonition tip" markdown>
    <p class="admonition-title">Tip</p>

    When shopping online, the use of a [parcel locker](https://en.wikipedia.org/wiki/Parcel_locker) can help keep your physical address private.

    </div>

2. **Unknown identity** - An unknown identity could be a stable pseudonym that you regularly use. It is not anonymous because it doesn't change. If you're part of an online community, you may wish to retain a persona that others know. This pseudonym isn't anonymous because—if monitored for long enough—details about the owner can reveal further information, such as the way they write, their general knowledge about topics of interest, etc.

    You may wish to use a VPN for this, to mask your IP address. Financial transactions are more difficult to mask: You could consider using anonymous cryptocurrencies, such as [Monero](https://getmonero.org). Employing altcoin shifting may also help to disguise where your currency originated. Typically, exchanges require KYC (know your customer) to be completed before they'll allow you to exchange fiat currency into any kind of cryptocurrency. Local meet-up options may also be a solution; however, those are often more expensive and sometimes also require KYC.

3. **Anonymous identity** - Even with experience, anonymous identities are difficult to maintain over long periods of time. They should be short-term and short-lived identities which are rotated regularly.

    Using Tor can help with this. It is also worth noting that greater anonymity is possible through asynchronous communication: Real-time communication is vulnerable to analysis of typing patterns (i.e. more than a paragraph of text, distributed on a forum, via email, etc.)

[^1]: A notable supply chain attack occurred in March 2024, when a malicious maintainer added a obfuscated backdoor into `xz`, a popular compression library. The backdoor ([CVE-2024-3094](https://cve.org/CVERecord?id=CVE-2024-3094)) was intended to give an unknown party remote access to most Linux servers via SSH, but it was discovered before it had been widely deployed.
