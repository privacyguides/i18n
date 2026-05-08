---
title: Zarządzanie zdjęciami
icon: material/image
description: Te narzędzia do zarządzania zdjęciami chronią prywatne fotografie przed wścibskimi spojrzeniami dostawców chmury i innych nieuprawnionych podmiotów.
cover: photo-management.webp
---

<small>Chroni przed następującymi zagrożeniami:</small>

- [:material-bug-outline: Ataki pasywne](basics/common-threats.md#security-and-privacy){ .pg-orange }
- [:material-server-network: Dostawcy usług](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }

Większość rozwiązań do zarządzania zdjęciami w chmurze, takich jak Google Photos, Flickr i Amazon Photos, nie zabezpiecza zdjęć przed możliwością dostępu do nich przez samego dostawcę usługodawcę. Te opcje zapewniają prywatność osobistych zdjęć, jednocześnie umożliwiając ich udostępnianie wyłącznie rodzinie i zaufanym osobom.

## Ente Photos

<div class="admonition recommendation" markdown>

![Ente logo](assets/img/photo-management/ente.svg){ align=right }

Ente Photos to kompleksowa usługa tworzenia kopii zapasowych zdjęć z szyfrowaniem end-to-end, która obsługuje automatyczne kopie zapasowe na iOS i Androidzie. Kod jest w pełni open source, zarówno po stronie klienta, jak i serwera. Jest również możliwość [samodzielnego hostowania](https://github.com/ente-io/ente/tree/main/server#self-hosting).

Darmowy plan oferuje 10 GB przestrzeni, pod warunkiem korzystania z usługi co najmniej raz w roku.

[:octicons-home-16: Strona główna](https://ente.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://ente.com/privacy){ .card-link title="Polityka prywatności" }
[:octicons-info-16:](https://ente.com/faq){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/ente-io/ente){ .card-link title="Kod źródłowy" }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=io.ente.photos)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1542026904)
- [:simple-github: GitHub](https://github.com/ente-io/ente/releases?q=photos)
- [:simple-android: Android](https://ente.com/download)
- [:fontawesome-brands-windows: Windows](https://ente.com/download)
- [:simple-apple: macOS](https://ente.com/download)
- [:simple-linux: Linux](https://ente.com/download)
- [:octicons-browser-16: W przeglądarce](https://web.ente.io)

</details>

</div>

Kod źródłowy serwera oraz infrastruktura, na której opiera się Ente Photos zostały poddane audytowi przez [Cure53](https://ente.com/blog/cern-audit) w październiku 2025 roku. Wcześniejsze audyty zostały przeprowadzone przez [Cure53](https://ente.com/blog/cryptography-audit) w marcu 2023 roku oraz przez [Fallible](https://ente.com/reports/Fallible-Audit-Report-19-04-2023.pdf) w kwietniu 2023 roku.

## Kryteria

**Należy pamiętać, że nie jesteśmy powiązani z żadnym z polecanych przez nas projektów.** Oprócz [naszych standardowych kryteriów](about/criteria.md) opracowaliśmy jasny zestaw wymagań, które pozwalają nam formułować obiektywne zalecenia. Sugerujemy zapoznanie się z tą listą przed wyborem projektu oraz przeprowadzenie własnych badań, aby upewnić się, że jest to odpowiedni wybór dla Ciebie.

### Minimalne wymagania

- Dostawcy usług hostowanych w chmurze muszą egzekwować E2EE.
- Musi oferować bezpłatny plan lub okres próbny do testowania.
- Musi obsługiwać uwierzytelnianie wieloskładnikowe TOTP lub FIDO2 albo logowanie za pomocą klucza dostępu.
- Musi oferować interfejs sieciowy obsługujący podstawowe funkcje zarządzania plikami.
- Musi umożliwiać łatwy eksport wszystkich plików/dokumentów.
- Musi być open source.

### Najlepszy scenariusz

- Powinna mieć opublikowany audyt przeprowadzony przez renomowaną, niezależną stronę trzecią.
