---
title: "라우터 펌웨어"
icon: material/router-wireless
description: 라우터나 와이파이 액세스 포인트를 보호하기 위한 대체 운영 체제입니다.
cover: router.webp
---

<small>다음 위협으로부터 보호합니다:</small>

- [:material-account-cash: 감시 자본주의](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}
- [:material-bug-outline: 수동적 공격](basics/common-threats.md#security-and-privacy ""){.pg-orange}

다음은 라우터, 와이파이 액세스 포인트 등에서 사용할 수 있는 몇 가지 대체 운영 체제입니다.

## OpenWrt

<div class="admonition recommendation" markdown>

![OpenWrt logo](assets/images/router/openwrt.svg#only-light){ align=right }
![OpenWrt logo](assets/images/router/openwrt-dark.svg#only-dark){ align=right }

**OpenWrt** is a Linux-based operating system; it's primarily used on embedded devices to route network traffic. util-linux, uClibc, BusyBox가 포함되어 있습니다. 모든 구성 요소가 가정용 라우터에 맞게 최적화되어 있습니다.

[:octicons-home-16: 홈페이지](https://openwrt.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://openwrt.org/docs/start){ .card-link title="문서"}
[:octicons-code-16:](https://github.com/openwrt/openwrt){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://openwrt.org/donate){ .card-link title="후원하기" }

</details>

</div>

OpenWrt의 [하드웨어 표](https://openwrt.org/toh/start)에서 사용 중인 기기가 지원되는지 확인할 수 있습니다.

## OPNsense

<div class="admonition recommendation" markdown>

![OPNsense logo](assets/images/router/opnsense.svg){ align=right }

**OPNsense** is an open-source, FreeBSD-based firewall and routing platform which incorporates many advanced features such as traffic shaping, load balancing, and VPN capabilities, with many more features available in the form of plugins. OPNsense는 일반적으로 경계 방화벽, 라우터, 무선 액세스 포인트, DHCP 서버, DNS 서버, VPN 엔드포인트로 사용됩니다.

[:octicons-home-16: 홈페이지](https://opnsense.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.opnsense.org/index.html){ .card-link title="문서"}
[:octicons-code-16:](https://github.com/opnsense){ .card-link title="소스 코드" }
[:octicons-heart-16:](https://opnsense.org/donate){ .card-link title="후원하기" }

</details>

</div>

OPNsense는 원래 [pfSense](https://en.wikipedia.org/wiki/PfSense)의 포크로 개발되었으며, 두 프로젝트 모두 값비싼 상용 방화벽에서나 볼 수 있는 기능을 제공하는 무료이면서 신뢰할 수 있는 방화벽 배포판으로 잘 알려져 있습니다. 2015년에 출시된 OPNsense의 개발자들은 프로젝트를 포크해야 할 필요가 있다고 느낀 pfSense의 여러 보안 및 코드 품질 문제와 함께, 넷게이트가 pfSense의 지분 과반을 인수한 데 따른 pfSense 프로젝트의 향후 방향에 대한 우려를 [언급](https://docs.opnsense.org/history/thefork.html)했습니다.

## 평가 기준 { #criteria }

**프라이버시 가이드는 추천하는 어떠한 프로젝트와도 제휴 관계가 없습니다.** [표준 평가 기준](about/criteria.md)에 더해, 객관적인 추천을 제공할 수 있도록 명확한 요구 사항을 마련했습니다. 프로젝트를 선택해 사용하기 전에 이 목록을 숙지하고, 직접 조사하여 자신에게 맞는 선택인지 확인하시기 바랍니다.

- 오픈 소스여야 합니다.
- 정기적으로 업데이트를 받아야 합니다.
- 다양한 하드웨어를 지원해야 합니다.
