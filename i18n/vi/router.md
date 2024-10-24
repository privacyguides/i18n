---
title: "Firmware Bộ định tuyến"
icon: material/router-wireless
description: Alternative operating systems for securing your router or Wi-Fi access point.
cover: router.webp
---

<small>Protects against the following threat(s):</small>

- [:material-account-cash: Surveillance Capitalism](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}
- [:material-bug-outline: Passive Attacks](basics/common-threats.md#security-and-privacy ""){.pg-orange}

Below are a few alternative operating systems that can be used on routers, Wi-Fi access points, etc.

## OpenWrt

<div class="admonition recommendation" markdown>

![OpenWrt logo](assets/img/router/openwrt.svg#only-light){ align=right }
![OpenWrt logo](assets/img/router/openwrt-dark.svg#only-dark){ align=right }

**OpenWrt** là một hệ điều hành (cụ thể là hệ điều hành nhúng) dựa trên nhân Linux, chủ yếu được sử dụng trên các thiết bị nhúng để định tuyến lưu lượng mạng. Các thành phần chính là Linux kernel, using-linux, uClibc và BusyBox. Tất cả các thành phần đã được tối ưu hóa về kích thước, đủ nhỏ để phù hợp với bộ nhớ và lưu trữ hạn chế có sẵn trong bộ định tuyến gia đình.

[Homepage](https://openwrt.org){ .md-button .md-button--primary }

???

</details>

</div>

Bạn có thể tham khảo OpenWrt's [table of hardware](https://openwrt.org/toh/start) để kiểm tra xem thiết bị của bạn có được hỗ trợ hay không.

## OPNsense

<div class="admonition recommendation" markdown>

![OPNsense logo](assets/img/router/opnsense.svg){ align=right }

**OPNsense** is an open-source, FreeBSD-based firewall and routing platform which incorporates many advanced features such as traffic shaping, load balancing, and VPN capabilities, with many more features available in the form of plugins. Nó được cài đặt trên máy tính để làm tường lửa/bộ định tuyến chuyên dụng cho mạng và được chú ý về độ tin cậy và cung cấp các tính năng thường chỉ có trong các tường lửa thương mại đắt tiền.

[:octicons-home-16: Homepage](https://opnsense.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.opnsense.org/index.html){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/opnsense){ .card-link title="Source Code" }
[:octicons-heart-16:](https://opnsense.org/donate){ .card-link title=Contribute }

</details>

</div>

OPNsense was originally developed as a fork of [pfSense](https://en.wikipedia.org/wiki/PfSense), and both projects are noted for being free and reliable firewall distributions which offer features often only found in expensive commercial firewalls. Launched in 2015, the developers of OPNsense [cited](https://docs.opnsense.org/history/thefork.html) a number of security and code-quality issues with pfSense which they felt necessitated a fork of the project, as well as concerns about Netgate's majority acquisition of pfSense and the future direction of the pfSense project.

## Framadate

**Please note we are not affiliated with any of the projects we recommend.** In addition to [our standard criteria](about/criteria.md), we have developed a clear set of requirements to allow us to provide objective recommendations. We suggest you familiarize yourself with this list before choosing to use a project, and conduct your own research to ensure it's the right choice for you.

- Must be open source.
- Must receive regular updates.
- Must support a wide variety of hardware.
