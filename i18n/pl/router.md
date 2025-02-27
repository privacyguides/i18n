---
title: "Oprogramowanie routera"
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

**OpenWrt** to system operacyjny oparty na oprogramowaniu Linux; jest używany głównie w urządzeniach wbudowanych do kierowania ruchem sieciowym. Zawiera util-linux, uClibc oraz BusyBox. All the components have been optimized for home routers.

[:octicons-home-16: Strona WWW](https://openwrt.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://openwrt.org/docs/start){ .card-link title=Dokumentacja}
[:octicons-code-16:](https://github.com/openwrt/openwrt){ .card-link title="Kod źródłowy" }
[:octicons-heart-16:](https://openwrt.org/donate){ .card-link title=Wesprzyj }

</details>

</div>

Zapoznaj się z [listą obsługiwanych urządzeń](https://openwrt.org/toh/start), aby sprawdzić, czy Twoje urządzenie jest obsługiwane.

## OPNsense

<div class="admonition recommendation" markdown>

![Logo OPNsense](assets/img/router/opnsense.svg){ align=right }

**OPNsense** to oparta na FreeBSD platforma firewall i routingu o otwartym kodzie źródłowym, która zawiera wiele zaawansowanych funkcji, takich jak kształtowanie ruchu, równoważenie obciążenia i funkcje VPN, z wieloma innymi funkcjami dostępnymi w postaci wtyczek. Po zainstalowaniu na komputerze pełni rolę dedykowanej zapory sieciowej/routera dla sieci i wyróżnia się niezawodnością oraz oferuje funkcje, które można często znaleźć tylko w drogich zaporach sieciowych.

[:octicons-home-16: Strona główna](https://opnsense.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.opnsense.org/index.html){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/opnsense){ .card-link title="Kod źródłowy" }
[:octicons-heart-16:](https://opnsense.org/donate){ .card-link title="Przyczyń się" }

</details>

</div>

OPNsense zostało pierwotnie opracowane na podstawie [pfSense](https://en.wikipedia.org/wiki/PfSense), a oba te projekty są znane z bycia bezpłatnymi i niezawodnymi dystrybucjami zapór sieciowych, które oferują funkcje dostępne często tylko w drogich komercyjnych zaporach sieciowych. Począwszy od 2015 roku programiści OPNsense [ujawnili](https://docs.opnsense.org/history/thefork.html) wiele problemów dotyczących bezpieczeństwa i jakości kodu pfSense, co popchnęło ich w stronę utworzenia pochodnego projektu, jak również obawy związane z większościowym zakupem pfSense przez Netgate i przyszłym kierunkiem rozwoju projektu.

## Kryteria

**Pamiętaj, że nie jesteśmy związani z żadnym z zalecanych projektów.** W dodatku do [naszych standardowych kryteriów](about/criteria.md), opracowaliśmy zestaw wymagań, które umożliwiają nam podejmowanie obiektywnych decyzji. Zalecamy zapoznanie się z tą listą przed zdecydowaniem o wyborze projektu oraz przeprowadzenie własnego rozeznania, aby upewnić się, że będzie dobrym wyborem dla Ciebie.

- Musi być open source.
- Wymagane są regularne aktualizacje.
- Wymagane jest wsparcie dla szerokiej gamy sprzętu.
