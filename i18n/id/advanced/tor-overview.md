---
title: "Ikhtisar Tor"
icon: 'simple/torproject'
description: Tor adalah jaringan terdesentralisasi yang gratis untuk digunakan, dan dirancang untuk penggunaan internet seprivat mungkin.
---

Tor adalah jaringan terdesentralisasi yang gratis untuk digunakan, dan dirancang untuk penggunaan internet seprivat mungkin. Jika digunakan dengan benar, jaringan ini memungkinkan penjelajahan dan komunikasi secara privat dan anonim.

## Membangun Jalur ke Layanan Clearnet

"Layanan Clearnet" adalah situs web yang dapat Anda akses dengan peramban apa pun, seperti [privacyguides.org](https://www.privacyguides.org). Tor memungkinkan Anda terhubung ke situs-situs web ini secara anonim dengan mengarahkan lalu lintas Anda melalui jaringan yang terdiri dari ribuan server yang dijalankan secara sukarela yang disebut "simpul" (atau "relai").

Setiap kali Anda [terhubung ke Tor](../tor.md), Tor akan memilih tiga simpul untuk membangun jalur ke internet—jalur ini disebut "sirkuit".

<figure markdown>
  ![Jalur Tor yang menunjukkan perangkat Anda menyambung ke simpul masuk, simpul tengah, dan simpul keluar sebelum mencapai situs web tujuan](../assets/img/how-tor-works/tor-path.svg#only-light)
  ![Jalur Tor yang menunjukkan perangkat Anda menyambung ke simpul masuk, simpul tengah, dan simpul keluar sebelum mencapai situs web tujuan](../assets/img/how-tor-works/tor-path-dark.svg#only-dark)
  <figcaption>Jalur sirkuit Tor</figcaption>
</figure>

Simpul-simpul berikut ini memiliki fungsinya masing-masing:

### Simpul Masuk

Simpul masuk, sering disebut simpul penjaga, adalah simpul pertama yang disambungkan oleh klien Tor Anda. Simpul masuk dapat melihat alamat IP Anda, namun tidak dapat melihat ke mana Anda tersambung.

Tidak seperti simpul lainnya, klien Tor akan memilih simpul entri secara acak dan bertahan dengan simpul tersebut selama dua sampai tiga bulan untuk melindungi Anda dari serangan tertentu.[^1]

### Simpul Tengah

Simpul tengah adalah simpul kedua yang disambungkan oleh klien Tor Anda. Simpul ini dapat melihat dari simpul mana lalu lintas berasal—simpul masuk—dan ke simpul mana lalu lintas tersebut menuju. Simpul tengah tidak dapat, melihat alamat IP Anda atau domain yang Anda sambungkan.

Untuk setiap sirkuit baru, simpul tengah dipilih secara acak dari semua simpul Tor yang tersedia.

### Simpul Keluar

Simpul keluar adalah titik lalu lintas web Anda meninggalkan jaringan Tor dan diteruskan ke tujuan yang Anda inginkan. Simpul keluar tidak dapat melihat alamat IP Anda, tetapi tahu situs apa yang hendak disambungkan.

Simpul keluar akan dipilih secara acak dari semua simpul Tor yang tersedia, yang ditandai sebagai relai keluar.[^2]

## Membangun Jalur ke Layanan Onion

"Layanan Onion" (juga sering disebut sebagai "layanan tersembunyi") adalah situs web yang hanya dapat diakses oleh peramban Tor. Situs web ini memiliki nama domain panjang yang dibuat secara acak yang diakhiri dengan `.onion`.

Proses penyambungan ke Layanan Onion di Tor berjalan sangat mirip dengan proses penyambungan ke layanan clearnet, tetapi lalu lintas Anda dirutekan melalui total **enam** simpul sebelum mencapai server tujuan. Namun, sama seperti sebelumnya, hanya tiga dari simpul-simpul ini yang berkontribusi pada anonimitas *Anda*, tiga simpul lainnya melindungi anonimitas *Layanan Onion*, menyembunyikan IP dan lokasi situs web yang sebenarnya dengan cara yang sama seperti Tor Browser menyembunyikan IP dan lokasi Anda.

<figure style="width:100%" markdown>
  ![Tor path showing your traffic being routed through your three Tor nodes plus three additional Tor nodes which hide the website's identity](../assets/img/how-tor-works/tor-path-hidden-service.svg#only-light)
  ![Tor path showing your traffic being routed through your three Tor nodes plus three additional Tor nodes which hide the website's identity](../assets/img/how-tor-works/tor-path-hidden-service-dark.svg#only-dark)
  <figcaption>Tor circuit pathway with Onion Services. Nodes in the <span class="pg-blue">blue</span> fence belong to your browser, while nodes in the <span class="pg-red">red</span> fence belong to the server, so their identity is hidden from you.</figcaption>
</figure>

## Enkripsi

Tor mengenkripsi setiap paket (blok data yang ditransmisikan) tiga kali dengan kunci dari simpul keluar, tengah, dan masuk—dalam urutan tersebut.

Setelah Tor berhasil membuat sirkuit, transmisi data dilakukan sebagai berikut:

1. Pertama: ketika paket tiba di simpul masuk, lapisan pertama enkripsi dihapus. Dalam paket terenkripsi ini, simpul masuk akan menemukan paket terenkripsi lain dengan alamat simpul tengah. Simpul masuk kemudian akan meneruskan paket ke simpul tengah.

2. Kedua: ketika simpul tengah menerima paket dari simpul masuk, simpul tersebut juga akan menghapus lapisan enkripsi dengan kuncinya, dan kali ini menemukan paket terenkripsi dengan alamat simpul keluar. Simpul tengah kemudian akan meneruskan paket ke simpul keluar.

3. Terakhir: ketika simpul keluar menerima paketnya, simpul ini akan menghapus lapisan enkripsi terakhir dengan kuncinya. Simpul keluar akan melihat alamat tujuan dan meneruskan paket ke alamat tersebut.

Di bawah ini adalah diagram alternatif yang menunjukkan prosesnya. Setiap simpul menghapus lapisan enkripsinya sendiri, dan ketika server tujuan mengembalikan data, proses yang sama terjadi secara terbalik. Sebagai contoh, simpul keluar tidak tahu siapa Anda, tetapi tahu dari simpul mana ia berasal, sehingga ia menambahkan lapisan enkripsinya sendiri dan mengirimkannya kembali.

<figure markdown>
  ![enkripsi Tor](../assets/img/how-tor-works/tor-encryption.svg#only-light)
  ![enkripsi Tor](../assets/img/how-tor-works/tor-encryption-dark.svg#only-dark)
  <figcaption>Mengirim dan menerima data melalui Jaringan Tor</figcaption>
</figure>

Tor memungkinkan kita untuk terhubung ke sebuah server tanpa ada satu pihak pun yang mengetahui seluruh jalurnya. Simpul masuk mengetahui siapa Anda, tetapi tidak mengetahui ke mana Anda akan pergi; simpul tengah tidak mengetahui siapa Anda atau ke mana Anda akan pergi; dan simpul keluar mengetahui ke mana Anda akan pergi, tetapi tidak mengetahui siapa Anda. Karena simpul keluar adalah yang membuat koneksi akhir, server tujuan tidak akan pernah mengetahui alamat IP Anda.

## Peringatan

Meskipun Tor menyediakan jaminan privasi yang kuat, kita harus menyadari bahwa Tor tidaklah sempurna:

- Musuh yang didanai dengan baik dengan kemampuan untuk secara pasif mengawasi sebagian besar lalu lintas jaringan di seluruh dunia memiliki peluang untuk mendeanonimisasi pengguna Tor dengan menggunakan analisis lalu lintas tingkat lanjut. Tor juga tidak melindungi Anda dari mengekspos diri Anda secara tidak sengaja, misalnya jika Anda membagikan terlalu banyak informasi tentang identitas asli Anda.
- Simpul keluar Tor juga dapat memonitor lalu lintas yang melewatinya. Ini berarti lalu lintas yang tidak dienkripsi, seperti lalu lintas HTTP biasa, dapat direkam dan dipantau. Jika lalu lintas tersebut mengandung informasi yang dapat diidentifikasi secara pribadi, lalu lintas tersebut dapat mendeanonimisasi Anda ke simpul keluar tersebut. Oleh karena itu, kami merekomendasikan penggunaan HTTPS melalui Tor jika memungkinkan.

Jika Anda ingin menggunakan Tor untuk menjelajah web, kami hanya merekomendasikan Tor Browser **resmi**—peramban ini dirancang untuk mencegah serangan sidik jari.

- [Tor Browser :material-arrow-right-drop-circle:](../tor.md#tor-browser)

## Sumber Daya Tambahan

- [Panduan Pengguna Tor Browser](https://tb-manual.torproject.org)
- [How Tor Works - Computerphile](https://invidious.privacyguides.net/embed/QRYzre4bf7I?local=true) <small>(YouTube)</small>
- [Tor Onion Services - Computerphile](https://invidious.privacyguides.net/embed/lVcbq_a5N9I?local=true) <small>(YouTube)</small>

[^1]: Relai pertama di sirkuit Anda disebut "penjaga jalan masuk" atau "penjaga". Relai ini adalah relai yang cepat dan stabil yang tetap menjadi relai pertama di sirkuit Anda selama 2-3 bulan untuk melindungi dari serangan pembobolan anonimitas yang telah diketahui. Sisa sirkuit Anda berubah dengan setiap situs web baru yang Anda kunjungi, dan secara keseluruhan relai ini memberikan perlindungan privasi penuh dari Tor. Untuk informasi lebih lanjut tentang cara kerja relai penjaga, lihat [posting blog](https://blog.torproject.org/improving-tors-anonymity-changing-guard-parameters) ini dan [makalah](https://www-users.cs.umn.edu/~hoppernj/single_guard.pdf) tentang relai penjaga. ([https://support.torproject.org/tbb/tbb-2/](https://support.torproject.org/tbb/tbb-2/))

[^2]: Relay flag: a special (dis-)qualification of relays for circuit positions (for example, "Guard", "Exit", "BadExit"), circuit properties (for example, "Fast", "Stable"), or roles (for example, "Authority", "HSDir"), as assigned by the directory authorities and further defined in the directory protocol specification. ([https://metrics.torproject.org/glossary.html](https://metrics.torproject.org/glossary.html))
