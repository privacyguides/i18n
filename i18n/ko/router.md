---
title: "공유기 펌웨어"
icon: material/router-wireless
description: These alternative operating systems can be used to secure your router or Wi-Fi access point.
cover: router.webp
---

본 내용은 공유기(라우터), Wi-Fi 액세스 포인트 장치 등에서 대체하여 사용할 수 있는 운영 체제 목록입니다.

## OpenWrt

<div class="admonition recommendation" markdown>

![OpenWrt 로고](assets/img/router/openwrt.svg#only-light){ align=right }
![OpenWrt 로고](assets/img/router/openwrt-dark.svg#only-dark){ align=right }

**OpenWrt**는 Linux 기반 운영 체제입니다. 주로 임베디드 기기에서 네트워크 트래픽 라우터 용도로 사용됩니다. util-linux, uClibc, BusyBox 등을 포함하고 있습니다. 모든 구성 요소는 가정용 공유기(라우터)에 알맞게 최적화되어 있습니다.

[:octicons-home-16: 홈페이지](https://openwrt.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://openwrt.org/docs/start){ .card-link title=문서}
[:octicons-code-16:](https://github.com/openwrt/openwrt){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://openwrt.org/donate){ .card-link title=기부 }

</details>

</div>

여러분이 사용 중인 기기의 OpenWrt 지원 여부는 [하드웨어 표](https://openwrt.org/toh/start)에서 확인할 수 있습니다.

## OPNsense

<div class="admonition recommendation" markdown>

![OPNsense logo](assets/img/router/opnsense.svg){ align=right }

**OPNsense** is an open-source, FreeBSD-based firewall and routing platform which incorporates many advanced features such as traffic shaping, load balancing, and VPN capabilities, with many more features available in the form of plugins. OPNsense는 일반적으로 경계 방화벽(Perimeter Firewall), 라우터, 무선 액세스 포인트, DHCP 서버, DNS 서버, VPN 엔드포인트상에 배포됩니다.

[:octicons-home-16: Homepage](https://opnsense.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.opnsense.org/index.html){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/opnsense){ .card-link title="Source Code" }
[:octicons-heart-16:](https://opnsense.org/donate){ .card-link title=Contribute }

</details>

</div>

OPNsense는 본래 [pfSense](https://en.wikipedia.org/wiki/PfSense)로부터 포크되어 개발됐으며, 두 프로젝트 모두 고가의 상용 방화벽에서만 볼 수 있는 기능을 제공하는 신뢰성 높은 무료 방화벽 배포판으로 유명합니다. 2015년 출시된 OPNsense의 개발자들은, pfSense의 여러 보안 및 코드 품질 문제와 Netgate가 pfSense의 대주주가 되면서 생긴 향후 프로젝트 방향의 우려로 인해 프로젝트를 포크하였다고 [밝혔습니다](https://docs.opnsense.org/history/thefork.html).

## 평가 기준

**Privacy Guides는 권장 목록의 어떠한 프로젝트와도 제휴를 맺지 않았습니다.** 객관적인 권장 목록을 제공하기 위해, [일반적인 평가 기준](about/criteria.md)에 더해 명확한 요구 사항을 정립하였습니다. 어떠한 프로젝트를 선택해 사용하기 전에, 이러한 요구 사항들을 숙지하고 여러분 스스로 조사하는 과정을 거쳐 적절한 선택을 하시기 바랍니다.

- 오픈 소스여야 합니다.
- 정기적으로 업데이트를 받아야 합니다.
- 다양한 하드웨어를 지원해야 합니다.
