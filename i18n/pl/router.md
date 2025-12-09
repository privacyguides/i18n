---
title: "Oprogramowanie układowe routera"
icon: material/router-wireless
description: Alternatywne systemy operacyjne do zabezpieczenia routera lub punktu dostępowego Wi-Fi.
cover: router.webp
---

<small>Chroni przed następującymi zagrożeniami:</small>

- [:material-account-cash: Kapitalizm inwigilacji](basics/common-threats.md#surveillance-as-a-business-model ""){.pg-brown}
- [:material-bug-outline: Ataki pasywne](basics/common-threats.md#security-and-privacy ""){.pg-orange}

Poniżej przedstawiono kilka alternatywnych systemów operacyjnych, które można stosować na routerach, punktach dostępowych Wi-Fi itp.

## OpenWrt

<div class="admonition recommendation" markdown>

![Logo OpenWrt](assets/img/router/openwrt.svg#only-light){ align=right }
![Logo OpenWrt](assets/img/router/openwrt-dark.svg#only-dark){ align=right }

**OpenWrt to system operacyjny oparty na Linuksie; jest używany przede wszystkim na urządzeniach wbudowanych do kierowania ruchem sieciowym. Zawiera on util-linux, uClibc i BusyBox. Wszystkie komponenty zostały zoptymalizowane pod kątem routerów domowych.

[:octicons-home-16: Strona główna](https://openwrt.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://openwrt.org/docs/start){ .card-link title=Dokumentacja}
[:octicons-code-16:](https://github.com/openwrt/openwrt){ .card-link title="Kod źródłowy" }
[:octicons-heart-16:](https://openwrt.org/donate){ .card-link title=Wesprzyj }

</details>

</div>

Możesz sprawdzić [tabelę obsługiwanego sprzętu](https://openwrt.org/toh/start) przez OpenWrt, aby zweryfikować, czy Twoje urządzenie jest wspierane.

## OPNsense

<div class="admonition recommendation" markdown>

![Logo OPNsense](assets/img/router/opnsense.svg){ align=right }

**OPNsense** to platforma zapory i routingu typu open source oparta na FreeBSD, która zawiera wiele zaawansowanych funkcji, takich jak kształtowanie ruchu, równoważenie obciążenia i możliwości VPN; dodatkowe funkcje są dostępne w formie wtyczek. OPNsense bywa wdrażany jako zapora obwodowa, router, bezprzewodowy punkt dostępowy, serwer DHCP, serwer DNS oraz punkt końcowy VPN.

[:octicons-home-16: Strona główna](https://opnsense.org){ .md-button .md-button--primary }
[:octicons-info-16:](https://docs.opnsense.org/index.html){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/opnsense){ .card-link title="Kod źródłowy" }
[:octicons-heart-16:](https://opnsense.org/donate){ .card-link title=Wesprzyj }

</details>

</div>

OPNsense powstał początkowo jako fork [pfSense](https://en.wikipedia.org/wiki/PfSense), a oba projekty są znane jako darmowe i niezawodne dystrybucje zapór sieciowych, oferujące funkcje często spotykane wyłącznie w drogich, komercyjnych rozwiązaniach. Uruchomiony w 2015 roku, zespół OPNsense [wskazał](https://docs.opnsense.org/history/thefork.html) szereg problemów z bezpieczeństwem i jakością kodu pfSense, które ich zdaniem uzasadniały stworzenie forka projektu, oraz wyraził obawy dotyczące przejęcia pfSense przez Netgate i kierunku dalszego rozwoju projektu pfSense.

## Kryteria

**Należy pamiętać, że nie jesteśmy powiązani z żadnym z polecanych przez nas projektów.** Oprócz [naszych standardowych kryteriów](about/criteria.md) opracowaliśmy jasny zestaw wymagań, które pozwalają nam formułować obiektywne zalecenia. Sugerujemy zapoznanie się z tą listą przed wyborem projektu oraz przeprowadzenie własnych badań, aby upewnić się, że jest to odpowiedni wybór dla Ciebie.

- Musi być open source.
- Musi otrzymywać regularne aktualizacje.
- Musi obsługiwać szeroką gamę sprzętu.
