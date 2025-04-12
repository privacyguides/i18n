---
meta_title: "VPN'ler Gizliliğinizi Nasıl Korur? VPN'e Genel Bakış - Privacy Guides"
title: VPN'e Genel Bakış
icon: material/vpn
description: Sanal Özel Ağlar, riski İnternet Sağlayıcınızdan alıp güvendiğiniz bir üçüncü tarafa aktarır. Bunları aklınızda tutmalısınız.
---

Sanal Özel Ağlar, ağınızın ucunu dünyanın başka bir yerinden çıkmak üzere genişletmenin bir yoludur.

[:material-movie-open-play-outline: Video: VPN'e ihtiyacınız var mı?](https://www.privacyguides.org/videos/2024/12/12/do-you-need-a-vpn/ ""){.md-button}

Normalde bir İSS, ağ sonlandırma cihazınıza (yani modeminize) giren ve çıkan internet trafiğinin akışını görebilir. HTTPS gibi şifreleme protokolleri internette yaygın olarak kullanılmaktadır, bu nedenle tam olarak ne gönderdiğinizi veya okuduğunuzu göremeyebilirler, ancak [talep ettiğiniz alan adları](../advanced/dns-overview.md#why-shouldnt-i-use-encrypted-dns) hakkında bir fikir edinebilirler.

VPN kullanmak, ağınıza duyduğunuz güveni dünyanın başka bir yerindeki bir sunucuya kaydırarak bu bilgileri bile İSS'nizden gizler. Sonuç olarak, İSS yalnızca bir VPN'e bağlı olduğunuzu görür ve VPN'den geçirdiğiniz etkinlik hakkında hiçbir şey görmez.

<div class="admonition note" markdown>
<p class="admonition-title">Notlar</p>

Bu web sitesinde "Sanal Özel Ağlar "dan bahsettiğimizde, genellikle internet trafiğinizi genel sunucuları üzerinden güvenli bir şekilde yönlendirmeleri karşılığında aylık ücret ödediğiniz **ticari** [VPN sağlayıcıları](../vpn.md) kastedilmektedir. Kendi barındırdığınız veya işyerleri tarafından işletilen ve dahili/çalışan ağ kaynaklarına güvenli bir şekilde bağlanmanızı sağlayan VPN'ler gibi başka birçok VPN türü vardır, ancak bu VPN'ler genellikle internet bağlantınızın gizliliğini korumaktan ziyade uzak ağlara güvenli bir şekilde erişmek için tasarlanmıştır.

</div>

## VPN nasıl çalışır?

VPN'ler, cihazınız ile VPN sağlayıcınızın sahip olduğu bir sunucu arasındaki trafiğinizi şifreler. Sizinle VPN sunucusu arasındaki herhangi birinin bakış açısından, VPN sunucusuna bağlanıyormuşsunuz gibi görünür. VPN sunucusu ile hedef siteniz arasındaki herhangi birinin bakış açısından, görebilecekleri tek şey web sitesine bağlanan VPN sunucusudur.

``` mermaid
akış şeması LR
 763931["Cihazınız<div>(VPN İstemcisi ile)</div>"] ===|"VPN Şifreleme"| 404512{"VPN Sunucusu"}
 404512 -.-|"VPN Şifrelemesi Yok"| 593753(("İnternet<div>(Hedefiniz)</div>"))
 subgraph 763931["Cihazınız<div>(VPN İstemcisi ile)</div>"]
 end
```

VPN'in, VPN sunucusu ile internetteki hedefiniz arasındaki trafiğinize herhangi bir güvenlik veya şifreleme eklemediğini unutmayın. Bir web sitesine güvenli bir şekilde erişmek için VPN kullanıp kullanmadığınızdan bağımsız olarak HTTPS'nin kullanımda olduğundan emin **olmalısınız**.

## VPN kullanmalı mıyım?

**Evet**, neredeyse kesinlikle. VPN'in aşağıdakiler de dahil olmak üzere birçok avantajı vardır:

1. Trafiğinizi **yalnızca** İnternet Servis Sağlayıcınızdan gizlemek.
1. İndirmelerinizi (torrentler gibi) İSS'nizden ve korsanla mücadele kuruluşlarından gizlemek.
1. IP'nizi üçüncü taraf web sitelerinden ve hizmetlerinden gizleyerek uyum sağlamanıza yardımcı olur ve IP tabanlı izlemeyi önler.
1. Belirli içerikler üzerindeki coğrafi kısıtlamaları aşmanıza olanak tanır.

VPN'ler, ziyaret ettiğiniz web sitelerinden IP'nizi gizlemek ve ağ trafiğinizi coğrafi olarak kaydırmak gibi Tor'un sağladığı faydaların *bazılarını* sağlayabilir ve iyi VPN sağlayıcıları, özellikle kendi yargı alanınızın dışında bir VPN sağlayıcısı seçerseniz, örneğin baskıcı rejimlerden yasal yetkililerle işbirliği yapmayacaktır.

VPN'ler, cihazınız ile VPN sunucusu arasındaki bağlantı dışındaki verileri şifreleyemez. VPN sağlayıcıları da trafiğinizi İSS'nizin görebildiği gibi görebilir ve değiştirebilir, bu nedenle onlara hala bir güven düzeyi vardır. Ve bir VPN sağlayıcısının "kayıt tutmama" politikalarını hiçbir şekilde doğrulamanın bir yolu yoktur.

## VPN ne zaman uygun değildir?

[Gerçek hayattaki veya tanınmış kimliğinizi](common-misconceptions.md#complicated-is-better) çevrimiçi olarak kullandığınız durumlarda VPN kullanmanın yararlı olması pek olası değildir. Bunu yapmak, bankanızın web sitesine giriş yapmanız gibi spam ve dolandırıcılık tespit sistemlerini tetikleyebilir.

It's important to remember that a VPN will not provide you with absolute anonymity because the VPN provider itself will still have access to your real IP address, destination website information, and often a money trail that can be linked directly back to you. "No logging" policies are merely a promise; if you need complete safety from the network itself, consider using [Tor](../advanced/tor-overview.md) in addition to or instead of a VPN.

Ayrıca, şifrelenmemiş bir HTTP hedefine olan bağlantınızı güvence altına almak için bir VPN'e güvenmemelisiniz. Ziyaret ettiğiniz web sitelerinde gerçekte yaptıklarınızı gizli ve güvenli tutmak için HTTPS kullanmanız gerekir. Bu, şifrelerinizi, oturum belirteçlerinizi ve sorgularınızı VPN sağlayıcısından ve VPN sunucusu ile hedefiniz arasındaki diğer potansiyel düşmanlardan koruyacaktır. Bağlantınızı HTTPS'den HTTP'ye düşürmeye çalışan saldırıları azaltmak için tarayıcınızda yalnızca HTTPS modunu etkinleştirmelisiniz (destekleniyorsa).

## VPN ile şifrelenmiş DNS kullanmalı mıyım?

VPN sağlayıcınız şifrelenmiş DNS sunucularını kendisi barındırmıyorsa, **muhtemelen hayır**. Üçüncü taraf sunucularla DOH/DOT (veya başka bir şifreli DNS biçimi) kullanmak, güvenilecek daha fazla varlık ekleyecektir. VPN sağlayıcınız, IP adreslerine ve diğer yöntemlere dayanarak hangi web sitelerini ziyaret ettiğinizi yine de görebilir. Tüm bunlarla birlikte, tarayıcınızda ECH gibi diğer güvenlik özelliklerini etkinleştirmek için şifrelenmiş DNS'yi etkinleştirmenin bazı avantajları olabilir. Tarayıcı içi şifrelenmiş DNS'e dayanan tarayıcı teknolojileri nispeten yenidir ve henüz yaygın değildir, bu nedenle özellikle sizinle ilgili olup olmadıkları, bağımsız olarak araştırmanız için size bırakacağımız bir egzersizdir.

Şifrelenmiş DNS'in önerilmesinin bir diğer yaygın nedeni de DNS sahtekarlığını önlemesidir. Ancak, tarayıcınızın **HTTPS** ile [TLS sertifikalarını](https://en.wikipedia.org/wiki/Transport_Layer_Security#Digital_certificates) zaten kontrol ediyor olması ve sizi bu konuda uyarması gerekir. **HTTPS** kullanmıyorsanız, bir saldırgan DNS sorgularınız dışında herhangi bir şeyi değiştirebilir ve sonuç çok az farklı olacaktır.

## Tor *ve* VPN kullanmalı mıyım?

Belki de Tor ilk etapta herkes için uygun olmayabilir. [Tehdit modelinizi](threat-modeling.md) göz önünde bulundurun, çünkü düşmanınız VPN sağlayıcınızdan bilgi alma yeteneğine sahip değilse, VPN kullanmak tek başına yeterli koruma sağlayabilir.

Tor kullanıyorsanız, Tor ağına ticari bir VPN sağlayıcısı aracılığıyla bağlanmanız *muhtemelen* en iyisidir. Ancak bu, [Tor'a genel bakış](../advanced/tor-overview.md) sayfamızda daha fazla yazdığımız karmaşık bir konudur.

## Tor'a "Tor düğümleri" sağlayan VPN sağlayıcıları üzerinden mi erişmeliyim?

Bu özelliği kullanmamalısınız: Tor kullanmanın birincil avantajı, VPN sağlayıcınıza güvenmemenizdir; bilgisayarınızdan doğrudan Tor'a bağlanmak yerine VPN'iniz tarafından barındırılan Tor düğümlerini kullandığınızda bu avantaj ortadan kalkar.

Şu anda Tor yalnızca TCP protokolünü desteklemektedir. UDP ( [WebRTC](https://en.wikipedia.org/wiki/WebRTC), [HTTP3/QUIC](https://en.wikipedia.org/wiki/HTTP/3) ve diğer protokoller tarafından kullanılır), [ICMP](https://en.wikipedia.org/wiki/Internet_Control_Message_Protocol) ve diğer paketler düşürülecektir. Bunu telafi etmek için VPN sağlayıcıları genellikle TCP olmayan tüm paketleri VPN sunucuları (ilk atlama noktanız) üzerinden yönlendirir. [ProtonVPN](https://protonvpn.com/support/tor-vpn)'de durum budur. Ayrıca, bu Tor over VPN kurulumunu kullanırken, [İzole Hedef Adresi](https://whonix.org/wiki/Stream_Isolation) (ziyaret ettiğiniz her alan için farklı bir Tor devresi kullanma) gibi diğer önemli Tor özellikleri üzerinde kontrol sahibi olmazsınız.

Bu özellik, anonim kalmak için değil, Tor'daki gizli hizmetlere erişmek için *uygun* bir yol olarak görülmelidir. Uygun anonimlik için gerçek [Tor Tarayıcısını](../tor.md) kullanın.

## Ticari VPN Sahipliği

Çoğu VPN hizmeti aynı [birkaç şirkete](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies) aittir. Bu karanlık şirketler, gerçekte sahip olduğunuzdan daha fazla seçeneğiniz olduğu yanılsamasını yaratmak ve kârı en üst düzeye çıkarmak için çok sayıda küçük VPN hizmeti işletmektedir. Genellikle, paravan şirketlerini besleyen bu sağlayıcılar korkunç gizlilik politikalarına sahiptir ve internet trafiğiniz konusunda güvenilmemelidir. Hangi sağlayıcıyı kullanmaya karar verdiğiniz konusunda çok katı olmalısınız.

Ayrıca, birçok VPN inceleme sitesinin yalnızca en yüksek teklifi verene açık reklam araçları olduğu konusunda dikkatli olmalısınız. ==Gizlilik Kılavuzları harici ürünleri tavsiye ederek para kazanmaz ve asla satış ortaklığı programları kullanmaz.==

[VPN Önerilerimiz](../vpn.md ""){.md-button}

## Modern VPN Alternatifleri

Son zamanlarda, merkezi VPN'lerin sahip olduğu bazı sorunları ele almak için çeşitli kuruluşlar tarafından bazı girişimlerde bulunulmuştur. Bu teknolojiler nispeten yenidir, ancak alan geliştikçe göz önünde bulundurulmaya değerdir.

### Çok Taraflı Röleler

Çok Taraflı Aktarıcılar (MPR'ler) farklı taraflara ait birden fazla düğüm kullanır, böylece hiçbir taraf hem kim olduğunuzu hem de neye bağlandığınızı bilmez. Tor'un arkasındaki temel fikir budur, ancak şimdi bu modeli taklit etmeye çalışan bazı ücretli hizmetler var.

MPR'ler VPN'lerin doğasında olan bir sorunu çözmeye çalışır: onlara tamamen güvenmeniz gerektiği gerçeği. Bu hedefe, sorumlulukları iki veya daha fazla farklı şirket arasında bölümlere ayırarak ulaşırlar.

One example of a commercially available MPR is Apple's iCloud+ Private Relay, which routes your traffic through two servers:

1. İlk olarak, Apple tarafından işletilen bir sunucu.

    Bu sunucu, bağlandığınızda aygıtınızın IP'sini görebilir ve iCloud aboneliğinize bağlı ödeme bilgileriniz ve Apple Kimliğiniz hakkında bilgi sahibidir. Ancak, hangi web sitesine bağlandığınızı göremez.

2. İkinci olarak, Cloudflare veya Fastly gibi ortak bir CDN tarafından işletilen bir sunucu.

    Bu sunucu aslında hedef web sitenize bağlantıyı yapar, ancak cihazınız hakkında hiçbir bilgisi yoktur. Bildiği tek IP adresi Apple'ın sunucusudur.

Other MPRs run by different companies operate in a very similar manner. This protection by segmentation only exists if you trust the two companies to not collude with each other to deanonymize you.

### Merkezi Olmayan VPN'ler

Another attempt at solving the issues with centralized VPN services are dVPNs. These are based on blockchain technology and claim to eliminate trust in a single party by distributing the nodes across lots of different people. However, many times a dVPN will default to a single node, meaning you need to trust that node completely, just like a traditional VPN. Unlike a traditional VPN, this one node that can see all your traffic is a random person instead of your VPN provider that can be audited and has legal responsibilities to uphold their privacy policy. Multi-hop is needed to solve this, but that comes with a stability and performance cost.

Another consideration is legal liability. The exit node will need to deal with legal problems from misuse of the network, an issue that the Tor network has contended with for its entire existence. This discourages regular people from running nodes and makes it more attractive for a malicious actor with lots of resources to host one. This is a big problem if the service is single-node, as the potentially malicious exit node can see who you are and what you're connecting to.

Many dVPNs are used to push a cryptocurrency rather than to make the best service. They also tend to be smaller networks with fewer nodes, making them more vulnerable to [Sybil attacks](https://en.wikipedia.org/wiki/Sybil_attack).

## İlgili VPN Bilgileri

- [VPN ve Gizlilik İnceleme Siteleriyle İlgili Sorun](https://blog.privacyguides.org/2019/11/20/the-trouble-with-vpn-and-privacy-review-sites)
- [Ücretsiz VPN Uygulaması Araştırması](https://top10vpn.com/research/free-vpn-investigations/ownership)
- [Gizli VPN sahipleri ortaya çıktı: Sadece 23 şirket tarafından işletilen 101 VPN ürünü](https://vpnpro.com/blog/hidden-vpn-owners-unveiled-97-vpns-23-companies)
- [Tehlikeli izinler isteyen 24 popüler uygulamanın arkasında gizlice bu Çinli şirket var](https://vpnpro.com/blog/chinese-company-secretly-behind-popular-apps-seeking-dangerous-permissions)
- [VPN -](https://overengineer.dev/blog/2019/04/08/very-precarious-narrative.html) Dennis Schubert tarafından yazılan [Çok Tehlikeli Bir Anlatı](https://overengineer.dev/blog/2019/04/08/very-precarious-narrative.html)
