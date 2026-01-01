---
title: "Ancaman Umum"
icon: 'material/eye-outline'
description: Model ancaman Anda bersifat pribadi bagi Anda, tetapi ini adalah beberapa hal yang dipedulikan oleh banyak pengunjung situs ini.
---

Secara garis besar, kami mengkategorikan rekomendasi kami ke dalam [ancaman](threat-modeling.md) atau tujuan yang berlaku untuk kebanyakan orang. ==Anda mungkin tidak peduli dengan tidak ada, satu, beberapa, atau semua kemungkinan ini==, dan alat dan layanan yang Anda gunakan tergantung pada tujuan Anda. Anda mungkin juga memiliki ancaman khusus di luar kategori ini, dan itu tidak masalah! Bagian yang penting adalah mengembangkan pemahaman tentang manfaat dan kekurangan alat yang Anda pilih untuk digunakan, karena hampir tidak ada satu pun yang akan melindungi Anda dari setiap ancaman.

<span class="pg-purple">:material-incognito: **Anonimitas**</span>
:

Melindungi aktivitas online Anda dari identitas asli Anda, melindungi Anda dari orang-orang yang mencoba mengungkap identitas *Anda* secara spesifik.

<span class="pg-red">:material-target-account: **Serangan Bertarget**</span>
:

Terlindungi dari peretas atau aktor jahat lainnya yang mencoba mengakses data atau perangkat *Anda* secara khusus.

<span class="pg-viridian">:material-package-variant-closed-remove: **Serangan Rantai Pasokan**</span>
:

Biasanya, bentuk <span class="pg-red">:material-target-account: Serangan Bertarget</span> yang berpusat di sekitar kerentanan atau eksploitasi yang dimasukkan ke dalam perangkat lunak yang baik, baik secara langsung atau melalui ketergantungan dari pihak ketiga.

<span class="pg-orange">:material-bug-outline: **Serangan Pasif**</span>
:

Terlindungi dari hal-hal seperti malware, pembobolan data, dan serangan lain yang dilakukan terhadap banyak orang sekaligus.

<span class="pg-teal">:material-server-network: **Penyedia Layanan**</span>
:

Melindungi data Anda dari penyedia layanan (misalnya dengan E2EE, yang membuat data Anda tidak dapat dibaca oleh server).

<span class="pg-blue">:material-eye-outline: **Pengawasan Massa**</span>
:

Perlindungan dari lembaga pemerintah, organisasi, situs web, dan layanan yang bekerja sama untuk melacak aktivitas Anda.

<span class="pg-brown">:material-account-cash: **Kapitalisme Pengawasan**</span>
:

Melindungi diri Anda dari jaringan periklanan besar, seperti Google dan Facebook, serta segudang pengumpul data pihak ketiga lainnya.

<span class="pg-green">:material-account-search: **Paparan Publik**</span>
:

Membatasi informasi tentang Anda yang data diakses secara online-mesin pencari atau publik.

<span class="pg-blue-gray">:material-close-outline: **Penyensoran**</span>
:

Menghindari akses yang disensor ke informati atau disensor saat berbicara online.

Beberapa ancaman ini mungkin lebih penting bagi Anda daripada yang lain, tergantung pada kekhawatiran Anda. Sebagai contoh, pengembang perangkat lunak yang memiliki akses ke data yang berharga atau penting mungkin akan sangat memperhatikan <span class="pg-viridian">:material-package-variant-closed-remove: Serangan Rantai Pasokan</span> dan <span class="pg-red">:material-target-account: Serangan Bertarget</span>. Mereka mungkin masih ingin melindungi data pribadi mereka agar tidak terseret dalam program<span class="pg-blue">:material-eye-outline: Pengawasan Massal</span>. Demikian pula, banyak orang mungkin lebih peduli dengan <span class="pg-green">:material-account-search: Paparan Publik</span> pada data pribadi mereka, tetapi mereka tetap harus waspada terhadap masalah yang berfokus pada keamanan, seperti <span class="pg-orange">:material-bug-outline: Serangan Pasif</span>—seperti perangkat lunak jahat yang memengaruhi perangkat mereka.

## Anonimitas vs. Privasi

<span class="pg-purple">:material-incognito: Anonimitas</span>

Anonimitas sering disalahartikan sebagai privasi, tetapi keduanya merupakan konsep yang berbeda. Sementara privasi adalah serangkaian pilihan yang Anda buat tentang bagaimana data Anda digunakan dan dibagikan, anonimitas adalah pemisahan aktivitas daring Anda dari identitas asli Anda.

Pelapor dan jurnalis, misalnya, dapat memiliki model ancaman yang jauh lebih ekstrem yang membutuhkan anonimitas total. Hal itu tidak hanya menyembunyikan apa yang mereka lakukan, data apa yang mereka miliki, dan tidak diretas oleh pihak-pihak jahat atau pemerintah, tetapi juga menyembunyikan siapa mereka sepenuhnya. Mereka sering kali akan mengorbankan segala jenis kenyamanan jika itu berarti melindungi anonimitas, privasi, atau keamanan mereka, karena hidup mereka dapat bergantung pada hal tersebut. Kebanyakan orang tidak perlu melangkah terlalu jauh.

## Keamanan dan Privasi

<span class="pg-orange">:material-bug-outline: Serangan Pasif</span>

Keamanan dan privasi juga sering tertukar, karena Anda membutuhkan keamanan untuk mendapatkan kemiripan dengan privasi: Menggunakan alat—bahkan jika alat itu dirancang untuk—tidak ada gunanya jika alat itu dapat dengan mudah dieksploitasi oleh penyerang yang kemudian merilis data Anda. Namun, kebalikannya belum tentu benar: Layanan yang paling aman di dunia *belum tentu* pribadi. Contoh terbaik dari hal ini adalah mempercayakan data kepada Google yang, mengingat skalanya, hanya mengalami sedikit insiden keamanan dengan mempekerjakan pakar keamanan terkemuka di industri untuk mengamankan infrastruktur mereka. Meskipun Google menyediakan layanan yang sangat aman, hanya sedikit orang yang menganggap data mereka pribadi di produk konsumen gratis Google (Gmail, YouTube, dll.)

Dalam hal keamanan aplikasi, umumnya kami tidak (dan terkadang tidak bisa) mengetahui apakah perangkat lunak yang kita gunakan berbahaya, atau suatu hari nanti bisa menjadi berbahaya. Bahkan pada pengembang yang paling tepercaya sekalipun, pada umumnya tidak ada jaminan bahwa perangkat lunak mereka tidak memiliki kerentanan serius yang nantinya dapat dieksploitasi.

Untuk meminimalkan kerusakan *yang dapat* dilakukan oleh perangkat lunak berbahaya, Anda harus menggunakan keamanan dengan kompartementalisasi. Sebagai contoh, hal ini dapat berupa penggunaan komputer yang berbeda untuk pekerjaan yang berbeda, menggunakan mesin virtual untuk memisahkan berbagai kelompok aplikasi yang terkait, atau menggunakan sistem operasi yang aman dengan fokus yang kuat pada aplikasi sandboxing dan kontrol akses yang wajib.

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Sistem operasi seluler umumnya memiliki aplikasi sandbox yang lebih baik daripada sistem operasi desktop: Aplikasi tidak dapat memperoleh akses root, dan memerlukan izin untuk mengakses sumber daya sistem.

Sistem operasi desktop umumnya tertinggal dalam hal sandbox yang tepat. ChromeOS memiliki kemampuan sandboxing yang mirip dengan Android, dan macOS memiliki kontrol izin sistem penuh (dan pengembang bisa memilih untuk melakukan sandboxing untuk aplikasi). Namun demikian, sistem operasi ini mengirimkan informasi identifikasi ke OEM masing-masing. Linux cenderung tidak menyerahkan informasi kepada vendor sistem, tetapi memiliki perlindungan yang buruk terhadap eksploitasi dan aplikasi jahat. Hal ini dapat dikurangi dengan distribusi khusus yang memanfaatkan mesin virtual atau kontainer secara signifikan, seperti [Qubes OS](../desktop.md#qubes-os).

</div>

## Serangan terhadap Individual Tertentu

<span class="pg-red">:material-target-account: Serangan Bertarget</span>

Serangan yang ditargetkan terhadap orang tertentu akan lebih sulit ditangani. Serangan yang umum terjadi termasuk mengirim dokumen berbahaya melalui surel, mengeksploitasi kerentanan (misalnya pada peramban dan sistem operasi), dan serangan fisik. Jika hal ini menjadi perhatian Anda, Anda harus menggunakan strategi mitigasi ancaman yang lebih canggih.

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Secara rancangan, **peramban web**, **klien surel**, dan **aplikasi perkantoran** biasanya menjalankan kode yang tidak dipercaya, yang dikirimkan kepada Anda dari pihak ketiga. Menjalankan beberapa mesin virtual—untuk memisahkan aplikasi seperti ini dari sistem hos Anda, dan juga satu sama lain—adalah salah satu teknik yang bisa Anda gunakan untuk mengurangi kemungkinan eksploitasi pada aplikasi-aplikasi ini yang mengorbankan sistem Anda yang lain. Sebagai contoh, teknologi seperti Qubes OS atau Microsoft Defender Application Guard pada Windows menyediakan metode yang nyaman untuk melakukan hal ini.

</div>

Jika Anda khawatir dengan **serangan fisik**, Anda sebaiknya menggunakan sistem operasi dengan implementasi boot terverifikasi yang aman, seperti Android, iOS, macOS, atau [Windows (dengan TPM)](https://learn.microsoft.com/windows/security/information-protection/secure-the-windows-10-boot-process). Anda juga harus memastikan bahwa penyimpanan Anda dienkripsi, dan bahwa sistem operasi menggunakan TPM atau Secure [Enclave](https://support.apple.com/guide/security/secure-enclave-sec59b0b31ff/1/web/1) atau [Element](https://developers.google.com/android/security/android-ready-se) untuk menilai batas upaya memasukkan frasa sandi enkripsi. Anda sebaiknya menghindari berbagi komputer dengan orang yang tidak Anda percayai, karena sebagian besar sistem operasi desktop tidak mengenkripsi data secara terpisah per pengguna.

## Serangan terhadap Organisasi Tertentu

<span class="pg-viridian">:material-package-variant-closed-remove: Serangan Rantai Pasokan</span>

Serangan rantai pasokan sering kali merupakan bentuk <span class="pg-red">:material-target-account: Serangan Bertarget</span> terhadap bisnis, pemerintah, dan aktivis, meskipun pada akhirnya dapat membahayakan masyarakat luas juga.

<div class="admonition example" markdown>
<p class="admonition-title">Contoh</p>

Contoh penting dari hal ini terjadi pada tahun 2017 ketika M.E.Doc, perangkat lunak akuntansi yang populer di Ukraina, terinfeksi virus *NotPetya*, yang kemudian menginfeksi orang-orang yang mengunduh perangkat lunak tersebut dengan ransomware. NotPetya sendiri merupakan serangan ransomware yang berdampak pada lebih dari 2000 perusahaan di berbagai negara, dan didasarkan pada eksploitasi *EternalBlue* yang dikembangkan oleh NSA untuk menyerang komputer Windows melalui jaringan.

</div>

Ada beberapa cara di mana jenis serangan ini dapat dilakukan:

1. Seorang kontributor atau karyawan mungkin pertama-tama bekerja dengan cara mereka sendiri untuk mendapatkan posisi yang berkuasa dalam sebuah proyek atau organisasi, dan kemudian menyalahgunakan posisi tersebut dengan menambahkan kode berbahaya.
2. Seorang pengembang dapat dipaksa oleh pihak luar untuk menambahkan kode berbahaya.
3. Seorang individu atau kelompok dapat mengidentifikasi ketergantungan perangkat lunak pihak ketiga (juga dikenal sebagai pustaka) dan bekerja untuk menyusup ke dalamnya dengan dua metode di atas, dengan mengetahui bahwa hal itu akan digunakan oleh pengembang perangkat lunak "hilir".

Serangan semacam ini membutuhkan banyak waktu dan persiapan untuk melakukannya dan berisiko karena dapat terdeteksi, terutama pada proyek-proyek open source jika proyek tersebut populer dan memiliki ketertarikan dari pihak luar. Sayangnya, mereka juga merupakan salah satu yang paling berbahaya karena sangat sulit untuk dimitigasi sepenuhnya. Kami menganjurkan pembaca untuk hanya menggunakan perangkat lunak yang memiliki reputasi baik dan berupaya mengurangi risiko dengan:

1. Hanya mengadopsi perangkat lunak populer yang sudah ada sejak lama. Semakin besar minat terhadap suatu proyek, semakin besar kemungkinan pihak eksternal akan melihat perubahan yang berbahaya. Pelaku jahat juga perlu menghabiskan lebih banyak waktu untuk mendapatkan kepercayaan komunitas dengan kontribusi yang berarti.
2. Menemukan perangkat lunak yang merilis binari dengan platform infrastruktur pembangunan yang banyak digunakan dan terpercaya, sebagai lawan dari workstation pengembang atau server yang dihosting sendiri. Beberapa sistem seperti Github Actions memungkinkan Anda memeriksa skrip build yang berjalan secara publik untuk mendapatkan keyakinan ekstra. Hal ini mengurangi kemungkinan malware pada mesin pengembang dapat menginfeksi paket mereka, dan memberikan keyakinan bahwa binari yang dihasilkan benar-benar diproduksi dengan benar.
3. Mencari penandatanganan kode pada setiap commit dan rilis kode sumber, yang menciptakan jejak yang dapat diaudit tentang siapa yang melakukan apa. Sebagai contoh: Apakah kode berbahaya ada di dalam repositori perangkat lunak? Pengambang mana yang menambahkannya? Apakah ditambahkan selama proses pembuatan?
4. Memeriksa apakah kode sumber memiliki pesan commit yang berarti (seperti [conventional commits](https://conventionalcommits.org)) yang menjelaskan apa yang seharusnya dicapai oleh setiap perubahan. Pesan yang jelas dapat memudahkan pihak luar proyek untuk memverifikasi, mengaudit, dan menemukan bug.
5. Memperhatikan jumlah kontributor atau pengelola yang memiliki sebuah program. Seorang pengembang tunggal mungkin lebih rentan untuk dipaksa menambahkan kode berbahaya oleh pihak eksternal, atau secara lalai mengaktifkan perilaku yang tidak diinginkan. Hal ini mungkin berarti perangkat lunak yang dikembangkan oleh "Big Tech" memiliki pengawasan yang lebih ketat daripada pengembang tunggal yang tidak bertanggung jawab kepada siapa pun.

## Privasi dari Penyedia Layanan

<span class="pg-teal">:material-server-network: Penyedia Layanan</span>

Kita hidup di dunia di mana hampir semua hal terhubung ke internet. Pesan, surel, dan interaksi sosial "pribadi" kita biasanya disimpan di sebuah server, di suatu tempat. Umumnya, ketika Anda mengirim pesan kepada seseorang, pesan tersebut disimpan di server, dan ketika teman Anda ingin membaca pesan tersebut, server akan menampilkannya kepada mereka.

Masalah yang jelas dengan hal ini adalah penyedia layanan (atau peretas yang telah membobol server) dapat mengakses percakapan Anda kapan pun dan bagaimanapun mereka inginkan, tanpa Anda ketahui. Hal ini berlaku untuk banyak layanan umum, seperti pesan SMS, Telegram, dan Discord.

Untungnya, E2EE dapat mengatasi masalah ini dengan mengenkripsi komunikasi antara Anda dan penerima yang Anda inginkan bahkan sebelum dikirim ke server. Kerahasiaan pesan Anda dijamin, dengan asumsi penyedia layanan tidak memiliki akses ke kunci pribadi salah satu pihak.

<div class="admonition note" markdown>
<p class="admonition-title">Catatan tentang Enkripsi Berbasis Web</p>

Dalam praktiknya, efektivitas implementasi E2EE yang berbeda bervariasi. Aplikasi, seperti [Signal](../real-time-communication.md#signal), berjalan secara asli pada perangkat Anda, dan setiap salinan aplikasi sama pada instalasi yang berbeda. Jika penyedia layanan memperkenalkan sebuah [pintu belakang](https://id.wikipedia.org/wiki/Pintu_belakang_(komputer)) dalam aplikasi mereka—dalam upaya untuk mencuri kunci pribadi Anda—nantinya dapat dideteksi dengan [rekayasa balik] (https://id.wikipedia.org/wiki/Rekayasa_balik).

Di sisi lain, implementasi E2EE berbasis web, seperti aplikasi web Proton Mail atau "Web Vault" dari Bitwarden, bergantung pada server yang secara dinamis menyajikan kode JavaScript ke peramban untuk menangani kriptografi. Sebuah server jahat dapat menargetkan Anda dan mengirimkan kode JavaScript berbahaya untuk mencuri kunci enkripsi Anda (dan akan sangat sulit untuk diketahui). Karena server dapat memilih untuk melayani klien web yang berbeda untuk orang yang berbeda—bahkan jika Anda menyadari serangan itu—akan sangat sulit untuk membuktikan kesalahan penyedia.

Oleh karena itu, Anda seharusnya menggunakan aplikasi asli daripada klien web bila memungkinkan.

</div>

Bahkan dengan E2EE, penyedia layanan masih bisa membuat profil Anda berdasarkan **metadata**, yang biasanya tidak dilindungi. Meskipun penyedia layanan tidak dapat membaca pesan Anda, mereka masih dapat mengamati hal-hal penting, seperti siapa yang Anda ajak bicara, seberapa sering Anda mengirim pesan kepada mereka, dan kapan Anda biasanya aktif. Perlindungan metadata cukup jarang dilakukan, dan—jika ada dalam [model ancaman](threat-modeling.md)—Anda harus memperhatikan dengan seksama dokumentasi teknis perangkat lunak yang Anda gunakan untuk mengetahui apakah ada minimalisasi atau perlindungan metadata sama sekali.

## Program Pengawasan Massal

<span class="pg-blue">:material-eye-outline: Pengawasan Massal</span>

Pengawasan massal adalah upaya yang rumit untuk memantau "perilaku, berbagai aktivitas, atau informasi" dari seluruh (atau sebagian besar) populasi.[^1] Hal ini sering merujuk pada program pemerintah, seperti yang [diungkapkan oleh Edward Snowden pada tahun 2013](https://en.wikipedia.org/wiki/Global_surveillance_disclosures_(2013%E2%80%93present)). Namun, hal ini juga dapat dilakukan oleh perusahaan, baik atas nama lembaga pemerintah maupun atas inisiatif sendiri.

<div class="admonition abstract" markdown>
<p class="admonition-title">Atlas Pengawasan</p>

Jika Anda ingin mempelajari lebih lanjut tentang metode pengawasan dan bagaimana metode tersebut diterapkan di kota Anda, Anda juga dapat melihat [Atlas Surveillance](https://atlasofsurveillance.org) oleh [Electronic Frontier Foundation](https://eff.org).

Di Prancis, Anda dapat melihat [Technopolice website](https://technopolice.fr/villes) dikelola oleh asosiasi nirlaba La Quadrature du Net.

</div>

Pemerintah sering kali membenarkan program pengawasan massal sebagai cara yang diperlukan untuk memerangi terorisme dan mencegah kejahatan. Namun, sebagai pelanggaran hak asasi manusia, mereka paling sering digunakan untuk menargetkan kelompok minoritas dan pembangkang politik secara tidak proporsional.

<div class="admonition quote" markdown>
<p class="admonition-title">ACLU: <em><a href="https://aclu.org/news/national-security/the-privacy-lesson-of-9-11-mass-surveillance-is-not-the-way-forward">Pelajaran Privasi dari Peristiwa 9/11: Pengawasan Massal Bukanlah Jalan ke Depan</a></em></p>

Dalam menghadapi pengungkapan Edward Showden mengenai programn pemerintah seperti [PRISM](https://en.wikipedia.org/wiki/PRISM) dan [Upstream](https://en.wikipedia.org/wiki/Upstream_collection), para pejabat intellijen juga mengakui bahwa NSA selama bertahun-tahun secara diam-diam telah mengumpulkan data tentang hampir semua panggilan telepon warga Amerika Serikat - siapa yang menelepon siapa, kapan panggilan itu dilakukan, dan berapa lama panggilan itu berlangsung. Informasi semacam ini, ketika dikumpulkan oleh NSA dari hari ke hari, dapat mengungkapkan detail yang sangat sensitif tentang kehidupan dan pergaulan seseorang, seperti apakah mereka pernah menelepon pendeta, penyedia layanan aborsi, konselor kecanduan, atau bantuan pencegahan bunuh diri.

</div>

Meskipun pengawasan massal semakin meningkat di Amerika Serikat, pemerintah telah menemukan bahwa program pengawasan massal seperti Bagian 215 hanya memiliki "sedikit nilai unik" dalam hal menghentikan kejahatan aktual atau plot teroris, dengan upaya-upaya yang sebagian besar menduplikasi program pengawasan yang ditargetkan oleh FBI.[^2]

Secara online, Anda dapat dilacak melalui berbagai metode, termasuk namun tidak terbatas pada:

- Alamat IP Anda
- Kuki peramban
- Data yang Anda kirimkan ke situs web
- Sidik jari peramban atau perangkat Anda
- Korelasi metode pembayaran

Jika Anda khawatir dengan program pengawasan massal, Anda bisa menggunakan strategi seperti mengkotak-kotakkan indentitas online Anda, berbaur dengan pengguna lain, atau, jika memungkinkan, hindari memberikan informasi identitas.

## Pengawasan sebagai Model Bisnis

<span class="pg-brown">:material-account-cash: Kapitalisme Pengawasan</span>

> Kapitalisme pengawasan adalah sistem ekonomi yang berpusat di sekitar penangkapan dan komodifikasi data pribadi untuk tujuan utama mencari keuntungan.[^3]

Bagi banyak orang, pelacakan dan pengawasan oleh perusahaan swasta merupakan masalah yang terus meningkat. Jaringan iklan yang tersebar luas, seperti yang dioperasikan oleh Google dan Facebook, menjangkau internet jauh lebih dari sekadar situs yang mereka kendalikan, melacak tindakan Anda di sepanjang jalan. Menggunakan alat seperti pemblokir konten untuk membatasi permintaan jaringan ke server mereka, dan membaca kebijakan privasi layanan yang Anda gunakan bisa membantu Anda menghindari banyak musuh dasar (meskipun tidak bisa sepenuhnya mencegah pelacakan).[^4]

Selain itu, bahkan perusahaan di luar industri *AdTech* atau pelacakan dapat membagikan informasi Anda dengan pialang [data](https://en.wikipedia.org/wiki/Information_broker) (seperti Cambridge Analytica, Experian, atau Datalogix) atau pihak lain. Anda tidak bisa secara otomatis berasumsi bahwa data Anda aman hanya karena layanan yang Anda gunakan tidak termasuk dalam model bisnis AdTech atau pelacakan pada umumnya. Perlindungan terkuat terhadap pengumpulan data perusahaan adalah dengan mengenkripsi atau mengaburkan data Anda jika memungkinkan, sehingga menyulitkan penyedia layanan yang berbeda untuk menghubungkan data satu sama lain dan membuat profil Anda.

## Membatasi Informasi Publik

<span class="pg-green">:material-account-search: Paparan Publik</span>

Cara terbaik untuk menjaga data Anda tetap pribadi adalah dengan tidak mempublikasikannya sejak awal. Menghapus informasi yang tidak diinginkan yang Anda temukan tentang diri Anda secara daring adalah salah satu langkah pertama terbaik yang dapat Anda lakukan untuk mendapatkan kembali privasi Anda.

- [Lihat panduan kami tentang penghapusan akun :material-arrow-right-drop-circle:](account-deletion.md)

Di situs-situs di mana Anda berbagi informasi, memeriksa pengaturan privasi akun Anda untuk membatasi seberapa luas data tersebut disebarkan sangatlah penting. Misalnya, aktifkan "mode pribadi" pada akun Anda jika diberi opsi: Hal ini akan memastikan bahwa akun Anda tidak diindeks oleh mesin pencari, dan tidak dapat dilihat tanpa izin Anda.

Jika Anda telah mengirimkan informasi asli Anda ke situs-situs yang seharusnya tidak memilikinya, pertimbangkan untuk menggunakan taktik disinformasi, seperti mengirimkan informasi fiktif yang terkait dengan identitas daring tersebut. Hal ini membuat informasi asli Anda tidak dapat dibedakan dari informasi palsu.

## Menghindari Penyensoran

<span class="pg-blue-gray">:material-close-outline: Penyensoran</span>

Penyensoran secara daring bisa dilakukan (dalam berbagai tingkatan) oleh berbagai pihak, termasuk pemerintah totaliter, administrator jaringan, dan penyedia layanan. Upaya-upaya untuk mengendalikan komunikasi dan membatasi akses terhadap informasi akan selalu tidak sesuai dengan hak asasi manusia atas Kebebasan Berekspresi.[^5]

Penyensoran pada platform perusahaan semakin umum terjadi, karena platform seperti Twitter dan Facebook menyerah pada permintaan publik, tekanan pasar, dan tekanan dari lembaga pemerintah. Tekanan pemerintah dapat berupa permintaan terselubung kepada bisnis, seperti Gedung Putih yang [meminta penghapusan](https://nytimes.com/2012/09/17/technology/on-the-web-a-fine-line-on-free-speech-across-globe.html) video YouTube yang provokatif, atau secara terang-terangan, seperti pemerintah Cina yang mewajibkan perusahaan untuk mematuhi rezim sensor yang ketat.

Orang-orang yang khawatir dengan ancaman sensor bisa menggunakan teknologi seperti [Tor](../advanced/tor-overview.md) untuk mengelakkannya, dan mendukung platform komunikasi yang tahan sensor seperti [Matrix](../social-networks.md#element), yang tidak memiliki otoritas akun terpusat yang bisa menutup akun secara sewenang-wenang.

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Meskipun menghindari penyensoran itu sendiri bisa jadi mudah, menyembunyikan fakta bahwa Anda melakukannya bisa jadi sangat bermasalah.

Anda harus mempertimbangkan aspek mana dari jaringan yang dapat diamati oleh musuh Anda, dan apakah Anda memiliki penyangkalan yang masuk akal atas tindakan Anda. Sebagai contoh, menggunakan [DNS terenkripsi](../advanced/dns-overview.md#what-is-encrypted-dns) bisa membantu Anda melalui sistem sensor berbasis DNS yang belum sempurna, tetapi tidak bisa menyembunyikan apa yang Anda kunjungi dari ISP Anda. Sebuah VPN atau Tor bisa membantu menyembunyikan apa yang Anda kunjungi dari administrator jaringan, tetapi tidak bisa menyembunyikan kalau Anda menggunakan jaringan tersebut sejak awal. Transport yang dapat dicolokkan (seperti Obfs4proxy, Meek, atau Shadowsocks) dapat membantu Anda menghindari dinding api yang memblokir protokol VPN umum atau Tor, tetapi upaya pengelabuan Anda masih bisa dideteksi dengan metode seperti pengujian atau [inspeksi paket dalam](https://en.wikipedia.org/wiki/Deep_packet_inspection).

</div>

Anda harus selalu mempertimbangkan risiko mencoba menerobos sensor, konsekuensi potensial, dan seberapa canggih musuh Anda. Anda harus berhati-hati dalam memilih perangkat lunak, dan memiliki rencana cadangan untuk berjaga-jaga seandainya Anda ketahuan.

[^1]: Wikipedia: [*Pengawasan Massal*](https://en.wikipedia.org/wiki/Mass_surveillance) dan [*Pengawasan*](https://en.wikipedia.org/wiki/Surveillance).
[^2]: Badan Pengawasan Privasi dan Kebebasan Sipil Amerika Serikat: [*Laporan tentang Program Rekaman Telepon yang Dilakukan berdasarkan Pasal 215*](https://documents.pclob.gov/prod/Documents/OversightReport/ec542143-1079-424a-84b3-acc354698560/215-Report_on_the_Telephone_Records_Program.pdf)
[^3]: Wikipedia: [*Kapitalisme pengawasan*](https://en.wikipedia.org/wiki/Surveillance_capitalism)
[^4]: "[Mengandung Keburukan](https://ranum.com/security/computer_security/editorials/dumb)" (atau, "membuat daftar semua hal buruk yang kita ketahui"), seperti yang dilakukan oleh banyak pemblokir konten dan program antivirus, tidak cukup melindungi Anda dari ancaman baru, dan tidak dikenal karena ancaman tersebut belum ditambahkan ke daftar filter. Anda juga harus menggunakan teknik mitigasi lainnya.
[^5]: Perserikatan Bangsa-Bangsa: [*Deklarasi Universal Hak Asasi Manusia*](https://un.org/en/about-us/universal-declaration-of-human-rights).
