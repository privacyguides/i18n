---
title: "Yönlendirici Yazılımı"
icon: material/router-wireless
description: Alternative operating systems for securing your router or Wi-Fi access point.
cover: router.webp
---

<small>Aşağıdaki tehdit(ler)e karşı koruma sağlar:</small>

- [:material-account-cash: Surveillance Capitalism](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}
- [:material-bug-outline: Pasif Saldırılar](basics/common-threats.md#security-and-privacy ""){.pg-orange}

Below are a few alternative operating systems that can be used on routers, Wi-Fi access points, etc.

## OpenWrt

<div class="admonition recommendation" markdown>

![OpenWrt logo](assets/img/router/openwrt.svg#only-light){ align=right }
![OpenWrt logo](assets/img/router/openwrt-dark.svg#only-dark){ align=right }

**OpenWrt** Linux kernelini temel alan, gömülü cihazlarda ağ trafiğini yönlendirmek için kullanılan bir işletim sistemidir. (Gömülü bir işletim sistemi de denebilir.). Ana bileşenler Linux kerneli, util - linux, uClibc ve BusyBox'tur. All the components have been optimized for home routers.

[:octicons-home-16: Anasayfa](https://openwrt.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://openwrt.org/docs/start){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/openwrt/openwrt){ .card-link title="Source Code" }
[:octicons-heart-16:](https://openwrt.org/donate){ .card-link title=Contribute }

</details>

</div>

Cihazınızın desteklenip desteklenmediğini kontrol etmek için OpenWrt'nin [donanım tablosuna](https://openwrt.org/toh/start) başvurabilirsiniz.

## pfSense

<div class="admonition recommendation" markdown>

![OPNsense logo](assets/img/router/opnsense.svg){ align=right }

**OPNsense** is an open-source, FreeBSD-based firewall and routing platform which incorporates many advanced features such as traffic shaping, load balancing, and VPN capabilities, with many more features available in the form of plugins. Bir ağ için özel bir güvenlik duvarı/yönlendirici yapmak üzere bir bilgisayara kurulmuştur ve güvenilirliği, genellikle, sadece pahalı ticari güvenlik duvarlarında bulunan özellikler sunmasıyla bilinir.

[:octicons-home-16: Homepage](https://opnsense.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.opnsense.org/index.html){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/opnsense){ .card-link title="Source Code" }
[:octicons-heart-16:](https://opnsense.org/donate){ .card-link title=Contribute }

</details>

</div>

OPNsense was originally developed as a fork of [pfSense](https://en.wikipedia.org/wiki/PfSense), and both projects are noted for being free and reliable firewall distributions which offer features often only found in expensive commercial firewalls. Launched in 2015, the developers of OPNsense [cited](https://docs.opnsense.org/history/thefork.html) a number of security and code-quality issues with pfSense which they felt necessitated a fork of the project, as well as concerns about Netgate's majority acquisition of pfSense and the future direction of the pfSense project.

## Kriter

**Lütfen önerdiğimiz projelerin hiçbirine bağlı olmadığımızı unutmayın.** [standart kriterlerimize](about/criteria.md) ek olarak, objektif tavsiyelerde bulunabilmemiz için bir takım gereklilikler geliştirdik. Bir projeyi kullanmayı seçmeden önce bu listeye aşina olmanızı ve sizin için doğru seçim olduğundan emin olmak için kendi araştırmanızı yapmanızı öneririz.

- Must be open source.
- Must receive regular updates.
- Must support a wide variety of hardware.
