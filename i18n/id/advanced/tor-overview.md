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

1. Pertama: ketika paket tiba di simpul masuk, lapisan pertama enkripsi dihapus. In this encrypted packet, the entry node will find another encrypted packet with the middle node’s address. The entry node will then forward the packet to the middle node.

2. Secondly: when the middle node receives the packet from the entry node, it too will remove a layer of encryption with its key, and this time finds an encrypted packet with the exit node's address. The middle node will then forward the packet to the exit node.

3. Lastly: when the exit node receives its packet, it will remove the last layer of encryption with its key. The exit node will see the destination address and forward the packet to that address.

Below is an alternative diagram showing the process. Each node removes its own layer of encryption, and when the destination server returns data, the same process happens entirely in reverse. For example, the exit node does not know who you are, but it does know which node it came from, and so it adds its own layer of encryption and sends it back.

<figure markdown>
  ![Tor encryption](../assets/img/how-tor-works/tor-encryption.svg#only-light)
  ![Tor encryption](../assets/img/how-tor-works/tor-encryption-dark.svg#only-dark)
  <figcaption>Sending and receiving data through the Tor Network</figcaption>
</figure>

Tor allows us to connect to a server without any single party knowing the entire path. The entry node knows who you are, but not where you are going; the middle node doesn’t know who you are or where you are going; and the exit node knows where you are going, but not who you are. Because the exit node is what makes the final connection, the destination server will never know your IP address.

## Caveats

Though Tor does provide strong privacy guarantees, one must be aware that Tor is not perfect:

- Well-funded adversaries with the capability to passively watch most network traffic over the globe have a chance of deanonymizing Tor users by means of advanced traffic analysis. Nor does Tor protect you from exposing yourself by mistake, such as if you share too much information about your real identity.
- Tor exit nodes can also monitor traffic that passes through them. This means traffic which is not encrypted, such as plain HTTP traffic, can be recorded and monitored. If such traffic contains personally identifiable information, then it can deanonymize you to that exit node. Thus, we recommend using HTTPS over Tor where possible.

If you wish to use Tor for browsing the web, we only recommend the **official** Tor Browser—it is designed to prevent fingerprinting.

- [Tor Browser :material-arrow-right-drop-circle:](../tor.md#tor-browser)

## Sumber Daya Tambahan

- [Panduan Pengguna Tor Browser](https://tb-manual.torproject.org)
- [How Tor Works - Computerphile](https://invidious.privacyguides.net/embed/QRYzre4bf7I?local=true) <small>(YouTube)</small>
- [Tor Onion Services - Computerphile](https://invidious.privacyguides.net/embed/lVcbq_a5N9I?local=true) <small>(YouTube)</small>

[^1]: The first relay in your circuit is called an "entry guard" or "guard". It is a fast and stable relay that remains the first one in your circuit for 2-3 months in order to protect against a known anonymity-breaking attack. The rest of your circuit changes with every new website you visit, and all together these relays provide the full privacy protections of Tor. For more information on how guard relays work, see this [blog post](https://blog.torproject.org/improving-tors-anonymity-changing-guard-parameters) and [paper](https://www-users.cs.umn.edu/~hoppernj/single_guard.pdf) on entry guards. ([https://support.torproject.org/tbb/tbb-2/](https://support.torproject.org/tbb/tbb-2/))

[^2]: Relay flag: a special (dis-)qualification of relays for circuit positions (for example, "Guard", "Exit", "BadExit"), circuit properties (for example, "Fast", "Stable"), or roles (for example, "Authority", "HSDir"), as assigned by the directory authorities and further defined in the directory protocol specification. ([https://metrics.torproject.org/glossary.html](https://metrics.torproject.org/glossary.html))
