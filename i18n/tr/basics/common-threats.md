---
title: "Common Threats"
icon: 'material/eye-outline'
description: Your threat model is personal to you, but these are some of the things many visitors to this site care about.
---

Broadly speaking, we categorize our recommendations into the [threats](threat-modeling.md) or goals that apply to most people. ==You may be concerned with none, one, a few, or all of these possibilities==, and the tools and services you use depend on what your goals are. You may have specific threats outside these categories as well, which is perfectly fine! The important part is developing an understanding of the benefits and shortcomings of the tools you choose to use, because virtually none of them will protect you from every threat.

<span class="pg-purple">:material-incognito: **Anonymity**</span>
:

Shielding your online activity from your real identity, protecting you from people who are trying to uncover *your* identity specifically.

<span class="pg-red">:material-target-account: **Targeted Attacks**</span>
:

Being protected from hackers or other malicious actors who are trying to gain access to *your* data or devices specifically.

<span class="pg-viridian">:material-package-variant-closed-remove: **Supply Chain Attacks**</span>
:

Typically, a form of <span class="pg-red">:material-target-account: Targeted Attack</span> that centers around a vulnerability or exploit introduced into otherwise good software either directly or through a dependency from a third party.

<span class="pg-orange">:material-bug-outline: **Passive Attacks**</span>
:

Being protected from things like malware, data breaches, and other attacks that are made against many people at once.

<span class="pg-teal">:material-server-network: **Service Providers**</span>
:

Protecting your data from service providers (e.g. with E2EE, which renders your data unreadable to the server).

<span class="pg-blue">:material-eye-outline: **Mass Surveillance**</span>
:

Protection from government agencies, organizations, websites, and services which work together to track your activities.

<span class="pg-brown">:material-account-cash: **Surveillance Capitalism**</span>
:

Protecting yourself from big advertising networks, like Google and Facebook, as well as a myriad of other third-party data collectors.

<span class="pg-green">:material-account-search: **Public Exposure**</span>
:

Limiting the information about you that is accessible online—to search engines or the public.

<span class="pg-blue-gray">:material-close-outline: **Censorship**</span>
:

Avoiding censored access to information or being censored yourself when speaking online.

Some of these threats may be more important to you than others, depending on your specific concerns. For example, a software developer with access to valuable or critical data may be primarily concerned with <span class="pg-viridian">:material-package-variant-closed-remove: Supply Chain Attacks</span> and <span class="pg-red">:material-target-account: Targeted Attacks</span>. They will likely still want to protect their personal data from being swept up in <span class="pg-blue">:material-eye-outline: Mass Surveillance</span> programs. Similarly, many people may be primarily concerned with <span class="pg-green">:material-account-search: Public Exposure</span> of their personal data, but they should still be wary of security-focused issues, such as <span class="pg-orange">:material-bug-outline: Passive Attacks</span>—like malware affecting their devices.

## Anonymity vs. Privacy

<span class="pg-purple">:material-incognito: Anonymity</span>

Anonymity is often confused with privacy, but they're distinct concepts. While privacy is a set of choices you make about how your data is used and shared, anonymity is the complete disassociation of your online activities from your real identity.

Whistleblowers and journalists, for example, can have a much more extreme threat model which requires total anonymity. That's not only hiding what they do, what data they have, and not getting hacked by malicious actors or governments, but also hiding who they are entirely. They will often sacrifice any kind of convenience if it means protecting their anonymity, privacy, or security, because their lives could depend on it. Çoğu insanın bu kadar ileri gitmesine gerek yoktur.

## Güvenlik ve Gizlilik

<span class="pg-orange">:material-bug-outline: Pasif Saldırılar</span>

Güvenlik ve gizlilik de sıklıkla birbirine karıştırılır, çünkü herhangi bir gizlilik görüntüsü elde etmek için güvenliğe ihtiyacınız vardır: Araçları kullanmak - tasarımları gereği özel olsalar bile - daha sonra verilerinizi yayınlayan saldırganlar tarafından kolayca istismar edilebileceklerse boşunadır. Ancak bunun tersi de doğru olmayabilir: Dünyanın en güvenli hizmeti *mutlaka* özel olmak zorunda değildir. Bunun en iyi örneği, ölçekleri göz önüne alındığında, altyapılarını güvence altına almak için sektör lideri güvenlik uzmanları istihdam ederek çok az güvenlik olayı yaşayan Google'a veri emanet etmektir. Google çok güvenli hizmetler sunsa da, çok az kişi Google'ın ücretsiz tüketici ürünlerinde (Gmail, YouTube, vb.) verilerinin gizli olduğunu düşünür.

Uygulama güvenliği söz konusu olduğunda, kullandığımız yazılımın kötü amaçlı olup olmadığını veya bir gün kötü amaçlı hale gelip gelmeyeceğini genellikle bilemeyiz (ve bazen bilemeyiz). En güvenilir geliştiricilerde bile, yazılımlarının daha sonra istismar edilebilecek ciddi bir güvenlik açığına sahip olmadığının garantisi genellikle yoktur.

Kötü niyetli bir yazılımın *verebileceği* zararı en aza indirmek için bölümlere ayırarak güvenlik sağlamalısınız. Örneğin bu, farklı işler için farklı bilgisayarlar kullanmak, farklı ilgili uygulama gruplarını ayırmak için sanal makineler kullanmak veya uygulama kum havuzu ve zorunlu erişim kontrolüne güçlü bir şekilde odaklanan güvenli bir işletim sistemi kullanmak şeklinde olabilir.

<div class="admonition tip" markdown>
<p class="admonition-title">İpucu</p>

Mobil işletim sistemleri genellikle masaüstü işletim sistemlerine göre daha iyi uygulama korumasına sahiptir: Uygulamalar kök erişimi elde edemez ve sistem kaynaklarına erişim için izin gerektirir.

Masaüstü işletim sistemleri genellikle uygun sandboxing konusunda geride kalmaktadır. ChromeOS, Android'e benzer sandboxing özelliklerine sahiptir ve macOS tam sistem izin kontrolüne sahiptir (ve geliştiriciler uygulamalar için sandboxing'i seçebilirler). Ancak, bu işletim sistemleri kendi OEM'lerine tanımlayıcı bilgiler iletmektedir. Linux, sistem satıcılarına bilgi göndermeme eğilimindedir, ancak istismarlara ve kötü amaçlı uygulamalara karşı zayıf bir korumaya sahiptir. Bu durum, [Qubes OS](../desktop.md#qubes-os) gibi sanal makineleri veya konteynerleri önemli ölçüde kullanan özel dağıtımlarla bir miktar hafifletilebilir.

</div>

## Belirli Kişilere Yönelik Saldırılar

<span class="pg-red">:material-target-account: Hedefli Saldırılar</span>

Belirli bir kişiye yönelik hedefli saldırılarla başa çıkmak daha sorunludur. Yaygın saldırılar arasında e-posta yoluyla kötü amaçlı belgeler gönderme, güvenlik açıklarından yararlanma (örneğin tarayıcılarda ve işletim sistemlerinde) ve fiziksel saldırılar yer alır. Bu sizin için bir endişe kaynağıysa, daha gelişmiş tehdit azaltma stratejileri kullanmalısınız.

<div class="admonition tip" markdown>
<p class="admonition-title">İpucu</p>

Tasarım gereği, **web tarayıcıları**, **e-posta istemcileri** ve **ofis uygulamaları** genellikle size üçüncü taraflardan gönderilen güvenilmeyen kodları çalıştırır. Bu gibi uygulamaları ana sisteminizden ve birbirlerinden ayırmak için birden fazla sanal makine çalıştırmak, bu uygulamalardaki bir açığın sisteminizin geri kalanını tehlikeye atma olasılığını azaltmak için kullanabileceğiniz bir tekniktir. Örneğin, Qubes OS veya Windows'ta Microsoft Defender Application Guard gibi teknolojiler bunu yapmak için uygun yöntemler sağlar.

</div>

**Fiziksel saldırılardan** endişe ediyorsanız, Android, iOS, macOS veya [Windows (TPM ile)](https://learn.microsoft.com/windows/security/information-protection/secure-the-windows-10-boot-process) gibi güvenli doğrulanmış önyükleme uygulamasına sahip bir işletim sistemi kullanmalısınız. Ayrıca sürücünüzün şifreli olduğundan ve işletim sisteminin şifreleme parolasını girme girişimlerini sınırlandırmak için bir TPM veya Secure [Enclave](https://support.apple.com/guide/security/secure-enclave-sec59b0b31ff/1/web/1) veya [Element](https://developers.google.com/android/security/android-ready-se) kullandığından emin olmalısınız. Çoğu masaüstü işletim sistemi verileri kullanıcı başına ayrı ayrı şifrelemediği için bilgisayarınızı güvenmediğiniz kişilerle paylaşmaktan kaçınmalısınız.

## Belirli Kuruluşlara Yönelik Saldırılar

<span class="pg-viridian">:material-package-variant-closed-remove: Tedarik Zinciri Saldırıları</span>

Tedarik zinciri saldırıları sıklıkla işletmelere, hükümetlere ve aktivistlere yönelik bir <span class="pg-red">:material-target-account: Hedefli Saldırı</span> biçimidir, ancak genel olarak kamuyu da tehlikeye atabilirler.

<div class="admonition example" markdown>
<p class="admonition-title">Örnek</p>

Bunun kayda değer bir örneği 2017 yılında Ukrayna'da popüler bir muhasebe yazılımı olan M.E.Doc'a *NotPetya* virüsünün bulaşması ve ardından bu yazılımı indiren kişilere fidye yazılımı bulaştırmasıyla ortaya çıkmıştır. NotPetya, çeşitli ülkelerdeki 2000'den fazla şirketi etkileyen bir fidye yazılımı saldırısıydı ve NSA tarafından Windows bilgisayarlara ağ üzerinden saldırmak için geliştirilen *EternalBlue* istismarına dayanıyordu.

</div>

Bu tür bir saldırının gerçekleştirilebileceği birkaç yol vardır:

1. Bir katılımcı veya çalışan önce bir proje veya kuruluş içinde güçlü bir konuma gelebilir ve daha sonra kötü amaçlı kod ekleyerek bu konumu kötüye kullanabilir.
2. Bir geliştirici, dışarıdan bir tarafça kötü amaçlı kod eklemeye zorlanabilir.
3. Bir kişi ya da grup, üçüncü taraf bir yazılım bağımlılığını (kütüphane olarak da bilinir) tespit edebilir ve "aşağı akış" yazılım geliştiricileri tarafından kullanılacağını bilerek yukarıdaki iki yöntemle bu bağımlılığa sızmaya çalışabilir.

Bu tür saldırıların gerçekleştirilmesi çok fazla zaman ve hazırlık gerektirebilir ve risklidir çünkü özellikle popüler ve dışarıdan ilgi gören açık kaynaklı projelerde tespit edilebilirler. Ne yazık ki, tamamen ortadan kaldırılması çok zor olduğu için aynı zamanda en tehlikeli olanlardan biridir. Okuyucuları yalnızca iyi bir üne sahip olan ve riski azaltmak için çaba gösteren yazılımları kullanmaya teşvik ediyoruz:

1. Yalnızca bir süredir piyasada olan popüler yazılımları benimseyin. Bir projeye ilgi ne kadar fazla olursa, dış tarafların kötü niyetli değişiklikleri fark etme olasılığı da o kadar artar. Kötü niyetli bir aktörün de anlamlı katkılarla toplumun güvenini kazanmak için daha fazla zaman harcaması gerekecektir.
2. Geliştirici iş istasyonları veya kendi kendine barındırılan sunucular yerine yaygın olarak kullanılan, güvenilir derleme altyapısı platformlarıyla ikili dosyalar yayınlayan yazılımlar bulmak. GitHub Actions gibi bazı sistemler, daha fazla güven için herkese açık olarak çalışan derleme komut dosyasını incelemenize izin verir. Bu, bir geliştiricinin makinesindeki kötü amaçlı yazılımın paketlerine bulaşma olasılığını azaltır ve üretilen ikili dosyaların aslında doğru şekilde üretildiğine dair güven verir.
3. Kimin ne yaptığına dair denetlenebilir bir iz oluşturan bireysel kaynak kodu taahhütleri ve sürümleri üzerinde kod imzalama arayışı. For example: Was the malicious code in the software repository? Which developer added it? Was it added during the build process?
4. Checking whether the source code has meaningful commit messages (such as [conventional commits](https://conventionalcommits.org)) which explain what each change is supposed to accomplish. Clear messages can make it easier for outsiders to the project to verify, audit, and find bugs.
5. Noting the number of contributors or maintainers a program has. A lone developer may be more susceptible to being coerced into adding malicious code by an external party, or to negligently enabling undesirable behavior. This may very well mean software developed by "Big Tech" has more scrutiny than a lone developer who doesn't answer to anyone.

## Privacy from Service Providers

<span class="pg-teal">:material-server-network: Service Providers</span>

We live in a world where almost everything is connected to the internet. Our "private" messages, emails, and social interactions are typically stored on a server, somewhere. Generally, when you send someone a message it's stored on a server, and when your friend wants to read the message the server will show it to them.

The obvious problem with this is that the service provider (or a hacker who has compromised the server) can access your conversations whenever and however they want, without you ever knowing. This applies to many common services, like SMS messaging, Telegram, and Discord.

Thankfully, E2EE can alleviate this issue by encrypting communications between you and your desired recipients before they are even sent to the server. The confidentiality of your messages is guaranteed, assuming the service provider doesn't have access to the private keys of either party.

<div class="admonition note" markdown>
<p class="admonition-title">Note on Web-based Encryption</p>

In practice, the effectiveness of different E2EE implementations varies. Applications, such as [Signal](../real-time-communication.md#signal), run natively on your device, and every copy of the application is the same across different installations. If the service provider were to introduce a [backdoor](https://en.wikipedia.org/wiki/Backdoor_(computing)) in their application—in an attempt to steal your private keys—it could later be detected with [reverse engineering](https://en.wikipedia.org/wiki/Reverse_engineering).

On the other hand, web-based E2EE implementations, such as Proton Mail's web app or Bitwarden's *Web Vault*, rely on the server dynamically serving JavaScript code to the browser to handle cryptography. A malicious server can target you and send you malicious JavaScript code to steal your encryption key (and it would be extremely hard to notice). Because the server can choose to serve different web clients to different people—even if you noticed the attack—it would be incredibly hard to prove the provider's guilt.

Therefore, you should use native applications over web clients whenever possible.

</div>

Even with E2EE, service providers can still profile you based on **metadata**, which typically isn't protected. While the service provider can't read your messages, they can still observe important things, such as whom you're talking to, how often you message them, and when you're typically active. Protection of metadata is fairly uncommon, and—if it's within your [threat model](threat-modeling.md)—you should pay close attention to the technical documentation of the software you're using to see if there's any metadata minimization or protection at all.

## Mass Surveillance Programs

<span class="pg-blue">:material-eye-outline: Mass Surveillance</span>

Mass surveillance is the intricate effort to monitor the "behavior, many activities, or information" of an entire (or substantial fraction of a) population.[^1] It often refers to government programs, such as the ones [disclosed by Edward Snowden in 2013](https://en.wikipedia.org/wiki/Global_surveillance_disclosures_(2013%E2%80%93present)). However, it can also be carried out by corporations, either on behalf of government agencies or by their own initiative.

<div class="admonition abstract" markdown>
<p class="admonition-title">Atlas of Surveillance</p>

If you want to learn more about surveillance methods and how they're implemented in your city you can also take a look at the [Atlas of Surveillance](https://atlasofsurveillance.org) by the [Electronic Frontier Foundation](https://eff.org).

In France, you can take a look at the [Technopolice website](https://technopolice.fr/villes) maintained by the non-profit association La Quadrature du Net.

</div>

Governments often justify mass surveillance programs as necessary means to combat terrorism and prevent crime. However, as breaches of human rights, they're most often used to disproportionately target minority groups and political dissidents, among others.

<div class="admonition quote" markdown>
<p class="admonition-title">ACLU: <em><a href="https://aclu.org/news/national-security/the-privacy-lesson-of-9-11-mass-surveillance-is-not-the-way-forward">The Privacy Lesson of 9/11: Mass Surveillance is Not the Way Forward</a></em></p>

In the face of Edward Snowden's disclosures of government programs such as [PRISM](https://en.wikipedia.org/wiki/PRISM) and [Upstream](https://en.wikipedia.org/wiki/Upstream_collection), intelligence officials also admitted that the NSA had for years been secretly collecting records about virtually every American’s phone calls — who’s calling whom, when those calls are made, and how long they last. This kind of information, when amassed by the NSA day after day, can reveal incredibly sensitive details about people’s lives and associations, such as whether they have called a pastor, an abortion provider, an addiction counselor, or a suicide hotline.

</div>

Despite growing mass surveillance in the United States, the government has found that mass surveillance programs like Section 215 have had "little unique value" with respect to stopping actual crimes or terrorist plots, with efforts largely duplicating the FBI's own targeted surveillance programs.[^2]

Online, you can be tracked via a variety of methods, including but not limited to:

- Your IP address
- Browser cookies
- The data you submit to websites
- Your browser or device fingerprint
- Payment method correlation

If you're concerned about mass surveillance programs, you can use strategies like compartmentalizing your online identities, blending in with other users, or, whenever possible, simply avoiding giving out identifying information.

## Surveillance as a Business Model

<span class="pg-brown">:material-account-cash: Surveillance Capitalism</span>

> Surveillance capitalism is an economic system centered around the capture and commodification of personal data for the core purpose of profit-making.[^3]

For many people, tracking and surveillance by private corporations is a growing concern. Pervasive ad networks, such as those operated by Google and Facebook, span the internet far beyond just the sites they control, tracking your actions along the way. Using tools like content blockers to limit network requests to their servers, and reading the privacy policies of the services you use can help you avoid many basic adversaries (although it can't completely prevent tracking).[^4]

Additionally, even companies outside the *AdTech* or tracking industry can share your information with [data brokers](https://en.wikipedia.org/wiki/Information_broker) (such as Cambridge Analytica, Experian, or Datalogix) or other parties. You can't automatically assume your data is safe just because the service you're using doesn't fall within the typical AdTech or tracking business model. Kurumsal veri toplamaya karşı en güçlü koruma, verilerinizi mümkün olduğunca şifrelemek veya gizlemektir; böylece farklı sağlayıcıların verileri birbiriyle ilişkilendirmesi ve hakkınızda bir profil oluşturması zorlaşır.

## Kamu Bilgisinin Sınırlandırılması

<span class="pg-green">:material-account-search: Kamuya Açıklık</span>

Verilerinizi gizli tutmanın en iyi yolu, onları ilk etapta kamuya açık hale getirmemektir. Çevrimiçi ortamda kendiniz hakkında bulduğunuz istenmeyen bilgileri silmek, gizliliğinizi yeniden kazanmak için atabileceğiniz en iyi ilk adımlardan biridir.

- [Hesap silme ile ilgili kılavuzumuzu görüntüleyin :material-arrow-right-drop-circle:](account-deletion.md)

Bilgi paylaştığınız sitelerde, bu verilerin ne kadar geniş bir alana yayıldığını sınırlamak için hesabınızın gizlilik ayarlarını kontrol etmek çok önemlidir. Örneğin, seçenek varsa hesaplarınızda "özel modu" etkinleştirin: Bu, hesabınızın arama motorları tarafından indekslenmemesini ve izniniz olmadan görüntülenememesini sağlar.

Gerçek bilgilerinizi, bu bilgilere sahip olmaması gereken sitelere zaten gönderdiyseniz, bu çevrimiçi kimlikle ilgili hayali bilgiler göndermek gibi dezenformasyon taktikleri kullanmayı düşünün. Bu, gerçek bilgilerinizi yanlış bilgilerden ayırt edilemez hale getirir.

## Sansürden Kaçınma

<span class="pg-blue-gray">:material-close-outline: Sansür</span>

Çevrimiçi sansür, totaliter hükümetler, ağ yöneticileri ve hizmet sağlayıcıları gibi aktörler tarafından (değişen derecelerde) gerçekleştirilebilir. İletişimi kontrol etmeye ve bilgiye erişimi kısıtlamaya yönelik bu çabalar, insanın İfade Özgürlüğü hakkı ile her zaman uyumsuz olacaktır.[^5]

Twitter ve Facebook gibi platformlar kamuoyu taleplerine, piyasa baskılarına ve devlet kurumlarından gelen baskılara boyun eğdikçe kurumsal platformlarda sansür giderek yaygınlaşıyor. Hükümet baskıları, Beyaz Saray'ın kışkırtıcı bir YouTube videosunun yayından [kaldırılmasını talep](https://nytimes.com/2012/09/17/technology/on-the-web-a-fine-line-on-free-speech-across-globe.html) etmesi gibi işletmelere yönelik gizli talepler olabileceği gibi, Çin hükümetinin şirketlerden katı bir sansür rejimine uymalarını istemesi gibi açık talepler de olabilir.

People concerned with the threat of censorship can use technologies like [Tor](../advanced/tor-overview.md) to circumvent it, and support censorship-resistant communication platforms like [Matrix](../social-networks.md#element), which doesn't have a centralized account authority that can close accounts arbitrarily.

<div class="admonition tip" markdown>
<p class="admonition-title">İpucu</p>

Sansürden kaçmanın kendisi kolay olsa da, bunu yaptığınız gerçeğini gizlemek çok sorunlu olabilir.

Düşmanınızın ağın hangi yönlerini gözlemleyebileceğini ve eylemleriniz için makul inkar edilebilirliğe sahip olup olmadığınızı düşünmelisiniz. Örneğin, [şifreli DNS](../advanced/dns-overview.md#what-is-encrypted-dns) kullanmak, ilkel, DNS tabanlı sansür sistemlerini atlatmanıza yardımcı olabilir, ancak ISS'nizden ziyaret ettiğiniz şeyi gerçekten gizleyemez. VPN veya Tor, ziyaret ettiğiniz ağları ağ yöneticilerinden gizlemenize yardımcı olabilir, ancak ilk etapta bu ağları kullandığınızı gizleyemez. Takılabilir aktarımlar (Obfs4proxy, Meek veya Shadowsocks gibi), yaygın VPN protokollerini veya Tor'u engelleyen güvenlik duvarlarından kaçmanıza yardımcı olabilir, ancak atlatma girişimleriniz yine de problama veya [derin paket incelemesi] (https://en.wikipedia.org/wiki/Deep_packet_inspection) gibi yöntemlerle tespit edilebilir.

</div>

Sansürü aşmaya çalışmanın risklerini, olası sonuçlarını ve düşmanınızın ne kadar sofistike olabileceğini her zaman göz önünde bulundurmalısınız. Yazılım seçiminizde dikkatli olmalı ve yakalanmanız durumunda bir yedek planınız olmalıdır.

[^1]: Wikipedia: [*Kitlesel Gözetim*](https://en.wikipedia.org/wiki/Mass_surveillance) ve [*Gözetim*](https://en.wikipedia.org/wiki/Surveillance).
[^2]: Amerika Birleşik Devletleri Gizlilik ve Sivil Özgürlükler Gözetim Kurulu: [*Bölüm 215 Kapsamında Yürütülen Telefon Kayıtları Programına İlişkin Rapor*](https://documents.pclob.gov/prod/Documents/OversightReport/ec542143-1079-424a-84b3-acc354698560/215-Report_on_the_Telephone_Records_Program.pdf)
[^3]: Wikipedia: [*Gözetim kapitalizmi*](https://en.wikipedia.org/wiki/Surveillance_capitalism)
[^4]: Birçok içerik engelleyici ve antivirüs programının yaptığı gibi["kötülükleri sır](https://ranum.com/security/computer_security/editorials/dumb)alamak" (veya "bildiğimiz tüm kötü şeyleri listelemek") sizi yeni ve bilinmeyen tehditlerden yeterince koruyamaz çünkü bunlar henüz filtre listesine eklenmemiştir. Diğer hafifletme tekniklerini de kullanmalısınız.
[^5]: Birleşmiş Milletler: [*İnsan Hakları Evrensel Beyannamesi*](https://un.org/en/about-us/universal-declaration-of-human-rights).
