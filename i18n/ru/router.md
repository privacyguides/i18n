---
title: "Прошивки для роутера"
icon: material/router-wireless
description: Alternative operating systems for securing your router or Wi-Fi access point.
cover: router.webp
---

<small>Protects against the following threat(s):</small>

- [:material-account-cash: Капитализм слежки](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}
- [:material-bug-outline: Пассивные атаки](basics/common-threats.md#security-and-privacy ""){.pg-orange}

Below are a few alternative operating systems that can be used on routers, Wi-Fi access points, etc.

## OpenWrt

<div class="admonition recommendation" markdown>

![Логотип OpenWrt](/assets/img/router/openwrt.svg#only-light){ align=right }
![Логотип OpenWrt](/assets/img/router/openwrt-dark.svg#only-dark){ align=right }

**OpenWrt** - это операционная система, основанная на ядре Linux, используемая в основном на встраиваемых устройствах для маршрутизации сетевого трафика. Основными компонентами являются ядро Linux, util-linux, uClibc и BusyBox. All the components have been optimized for home routers.

[:octicons-home-16: Домашняя страница](https://openwrt.org/ru){ .md-button .md-button--primary }
[:octicons-info-16:](https://openwrt.org/ru/docs/start){ .card-link title=Документация}
[:octicons-code-16:](https://github.com/openwrt/openwrt){ .card-link title="Исходный код" }
[:octicons-heart-16:](https://openwrt.org/donate){ .card-link title=Поддержать }

</details>

</div>

Вы можете обратиться к [таблице устройств](https://openwrt.org/toh/start) OpenWrt, чтобы проверить, поддерживается ли ваше устройство.

## OPNsense

<div class="admonition recommendation" markdown>

![OPNsense logo](assets/img/router/opnsense.svg){ align=right }

**OPNsense** is an open-source, FreeBSD-based firewall and routing platform which incorporates many advanced features such as traffic shaping, load balancing, and VPN capabilities, with many more features available in the form of plugins. OPNsense часто используется для файерволов, роутеров, беспроводных точек доступа, серверов DHCP, DNS серверов и конечных точек VPN.

[:octicons-home-16: Homepage](https://opnsense.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.opnsense.org/index.html){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/opnsense){ .card-link title="Source Code" }
[:octicons-heart-16:](https://opnsense.org/donate){ .card-link title=Contribute }

</details>

</div>

OPNsense был изначально разработан как форк [pfSense](https://en.wikipedia.org/wiki/PfSense), и оба проекта известны как бесплатные и надежные дистрибутивы файерволов, которые предлагают функции, часто встречающиеся только в дорогих коммерческих файерволах. Разработчики OPNsense [назвали](https://docs.opnsense.org/history/thefork.html) ряд проблем с безопасностью и качеством кода pfSense, из-за которых в 2015 году и был разработан форк, а также опасения по поводу приобретения pfSense компанией Netgate и направления, в котором движется разработка pfSense.

## Критерии

**Обратите внимание, что у нас нет связей ни с одним из проектов, которые мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md)мы разработали четкий набор требований, позволяющий нам давать объективные рекомендации. Мы рекомендуем вам ознакомиться с этим списком, прежде чем выбрать программу, и провести самостоятельное исследование, чтобы убедиться, что это правильный выбор для вас.

- Исходный код проекта должен быть открыт.
- Проект должен регулярно обновляться.
- Проект должен поддерживать широкий спектр устройств.
