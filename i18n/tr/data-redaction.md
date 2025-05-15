---
meta_title: "Meta Veri Temizleyiciler ve Veri Redaksiyon Araçları ile PII'yi Kaldırın - Gizlilik Kılavuzları"
title: "Veri ve Meta Veri Redaksiyonu"
icon: material/tag-remove
description: Paylaştığınız fotoğraf ve dosyalardan GPS konumu ve diğer tanımlayıcı bilgiler gibi meta verileri kaldırmak için bu araçları kullanın.
cover: data-redaction.webp
---

<small>Aşağıdaki tehdit(ler) e karşı koruma sağlar:</small>

- [:material-account-search: Kamuya Açıklık](basics/common-threats.md#limiting-public-information ""){.pg-green}

Dosyaları paylaşırken, ilişkili meta verileri kaldırdığınızdan emin olun. Görüntü dosyaları genellikle [Exif](https://en.wikipedia.org/wiki/Exif) verilerini içerir. Fotoğraflar bazen dosya meta verilerinde GPS koordinatlarını bile içerir.

<div class="admonition warning" markdown>
<p class="admonition-title">Uyarı</p>

Görüntülerdeki metinleri] düzenlemek için bulanıklaştırmayı **asla** kullanmamalısınız (https://bishopfox.com/blog/unredacter-tool-never-pixelation). Bir resimdeki metni redakte etmek istiyorsanız, metnin üzerine bir kutu çizmelisiniz.

</div>

## MAT2

<div class="admonition recommendation" markdown>

![MAT2 logo](assets/img/data-redaction/mat2.svg){ align=right }

**MAT2**, görüntü, ses, torrent ve belge dosya türlerinden meta verileri kaldırmanıza olanak tanıyan ücretsiz, platformlar arası bir yazılımdır. KDE](https://kde.org)'nin varsayılan dosya yöneticisi olan [Dolphin](https://0xacab.org/jvoisin/mat2/-/tree/master/dolphin) için bir uzantı aracılığıyla hem bir komut satırı aracı hem de bir grafik kullanıcı arayüzü sağlar.

[:octicons-repo-16: Repository](https://0xacab.org/jvoisin/mat2){ .md-button .md-button--primary }
[:octicons-info-16:](https://0xacab.org/jvoisin/mat2/-/blob/master/README.md){ .card-link title="Documentation" }
[:octicons-code-16:](https://0xacab.org/jvoisin/mat2){ .card-link title="Kaynak Kod" }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:fontawesome-brands-windows: Windows](https://pypi.org/project/mat2#metadata-and-privacy)
- [:simple-apple: macOS](https://0xacab.org/jvoisin/mat2#requirements-setup-on-macos-os-x-using-homebrew)
- [:simple-linux: Linux](https://pypi.org/project/mat2)
- [:octicons-globe-16: Web](https://0xacab.org/jvoisin/mat2#web-interface)

</details>

</div>

## ExifEraser (Android)

<div class="admonition recommendation" markdown>

![ExifEraser logo](assets/img/data-redaction/exiferaser.svg){ align=right }

**ExifEraser** Android için modern, izinsiz bir görüntü meta veri silme uygulamasıdır.

It currently supports JPEG, PNG, and WebP files.

[:octicons-repo-16: Repository](https://github.com/Tommy-Geenexus/exif-eraser#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/Tommy-Geenexus/exif-eraser#description){ .card-link title="Documentation" }
[:octicons-code-16:](https://github.com/Tommy-Geenexus/exif-eraser){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>İndirmeler</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=com.none.tom.exiferaser)
- [:octicons-moon-16: Accrescent](https://accrescent.app/app/com.none.tom.exiferaser)
- [:simple-github: GitHub](https://github.com/Tommy-Geenexus/exif-eraser/releases)

</details>

</div>

Silinen meta veriler görüntünün dosya türüne bağlıdır:

- **JPEG**: ICC Profili, Exif, Photoshop Görüntü Kaynakları ve XMP/ExtendedXMP meta verileri varsa silinecektir.
- **PNG**: ICC Profili, Exif ve XMP meta verileri varsa silinecektir.
- **WebP**: ICC Profili, Exif ve XMP meta verileri varsa silinecektir.

Görüntüleri işledikten sonra ExifEraser size her görüntüden tam olarak neyin kaldırıldığı hakkında tam bir rapor sunar.

Uygulama, resimlerden meta verileri silmek için birden fazla yol sunar. Şöyle ki:

- ExifEraser ile başka bir uygulamadan görüntü paylaşabilirsiniz.
- Uygulamanın kendisi aracılığıyla tek bir görüntüyü, aynı anda birden fazla görüntüyü veya hatta tüm bir dizini seçebilirsiniz.
- Bir fotoğraf çekmek için işletim sisteminizin kamera uygulamasını kullanan ve ardından meta verileri kaldıran bir "Kamera" seçeneğine sahiptir.
- Her ikisi de bölünmüş ekran modunda açıkken fotoğrafları başka bir uygulamadan ExifEraser'a sürüklemenizi sağlar.
- Son olarak, panonuzdan bir görüntü yapıştırmanıza olanak tanır.

## Kısayollar (iOS & macOS)

IOS ve macOS'ta, herhangi bir üçüncü taraf uygulaması kullanmadan bir görüntü meta verisi oluşturarak görüntü meta verilerini kaldırabilirsiniz. [**kısayol**](https://apps.apple.com/app/id915249334) bu amaç için. İşte olduğu gibi kullanmak için indirebileceğiniz örnek bir kısayol:

[:material-tag-minus: Temiz Görüntü Meta Verileri](https://icloud.com/shortcuts/fb774ddb7b5b4296871776c67ac0fff9 ""){.md-button}

Bunu kendi kısayolunuz için bir model olarak da kullanabilirsiniz; sadece **Dönüştür** eylemi altındaki **Meta Verileri Koru** seçeneğinin işaretli olmadığından emin olun. Eklendikten sonra, :octicons-share-24: Paylaş düğmesini seçtiğinizde görüntülenen paylaşım sayfasındaki kısayola erişebilirsiniz. Birden fazla görüntü seçebilir ve meta verilerini tek seferde kaldırmak için kısayolu çağırabilirsiniz.

Bu kısayol konum, cihaz modeli, lens modeli ve diğer kamera bilgileri gibi meta verileri kaldırır. Ayrıca görüntü oluşturma tarihini kısayolun kullanıldığı zamana ayarlar.

## ExifTool (CLI)

<div class="admonition recommendation" markdown>

![ExifTool logosu](assets/img/data-redaction/exiftool.png){ align=right }

**ExifTool**, çok çeşitli dosya formatlarında (JPEG, TIFF, PNG, PDF, RAW ve daha fazlası) meta bilgileri (Exif, IPTC, XMP ve daha fazlası) okumak, yazmak ve düzenlemek için orijinal Perl kütüphanesi ve komut satırı uygulamasıdır.

Genellikle diğer Exif kaldırma uygulamalarının bir bileşenidir ve çoğu Linux dağıtım deposunda bulunur.

[:octicons-home-16: Homepage](https://exiftool.org){ .md-button .md-button--primary }[:octicons-info-16:](https://exiftool.org/faq.html){ .card-link title="Public Instances"}
[:octicons-code-16:](https://github.com/exiftool/exiftool){ .card-link title=Documentation}
[:octicons-heart-16:](https://exiftool.org/#donate){ .card-link title="Source Code" }
[](){ .card-link title=Contribute" }

<details class="downloads" markdown>
<summary>İndirmeler</summary>
- [:fontawesome-brands-windows: Windows](https://exiftool.org)
- [:simple-apple: macOS](https://exiftool.org)
- [:simple-linux: Linux](https://exiftool.org)
- [ Web)

</details>

</div>

<div class="admonition example" markdown>
<p class="admonition-title">Bir dosya dizininden veri silme</p>

```bash
exiftool -all= *.file_extension
```

</div>

## Kriter

**Lütfen önerdiğimiz projelerin hiçbirine bağlı olmadığımızı unutmayın.** [standart kriterlerimize](about/criteria.md) ek olarak, objektif tavsiyelerde bulunabilmemiz için bir takım gereklilikler geliştirdik. Bir projeyi kullanmayı seçmeden önce bu listeye aşina olmanızı ve sizin için doğru seçim olduğundan emin olmak için kendi araştırmanızı yapmanızı öneririz.

- Açık kaynaklı işletim sistemleri için geliştirilen uygulamalar açık kaynaklı olmalıdır.
- Uygulamalar ücretsiz olmalı ve reklam veya başka sınırlamalar içermemelidir.
