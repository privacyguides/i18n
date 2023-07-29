---
meta_title: "Рекомендации и сравнение приватных VPN-сервисов, без спонсоров и рекламы - Privacy Guides"
title: "VPN сервисы"
icon: material/vpn
description: Это лучшие VPN-сервисы для защиты вашей конфиденциальности и безопасности в Интернете. Найдите провайдера, который не будет шпионить за вами.
cover: vpn.png
---

Если вам нужна дополнительная **приватность** от своего провайдера, при подключении к публичным сетям Wi-Fi или во время скачивания торрентов, VPN может быть правильным решением для вас, если вы понимаете связанные с этим риски. Мы считаем, что эти VPN-провайдеры на голову выше остальных:

<div class="grid cards" markdown>

- ![Логотип Proton VPN](assets/img/vpn/protonvpn.svg){ .twemoji } [Proton VPN](#proton-vpn)
- ![Логотип IVPN](assets/img/vpn/mini/ivpn.svg){ .twemoji } [IVPN](#ivpn)
- ![Логотип Mullvad](assets/img/vpn/mullvad.svg){ .twemoji } [Mullvad](#mullvad)

</div>

!!! danger "VPN не обеспечивает анонимность"

    Использование VPN **не обеспечивает** анонимность ваших привычек при просмотре веб-страниц, а также **не прибавляет** безопасности при использовании незащищенного (HTTP) трафика.
    
    Если вам нужна **анонимность**, вам следует использовать браузер Tor **вместо** VPN.
    
    Если вам нужна дополнительная **безопасность**, убедитесь, что вы подключаетесь к веб-сайтам, используя HTTPS. VPN не является заменой полезных привычек для обеспечения безопасности.
    
    [Установить Tor](https://www.torproject.org/){ .md-button .md-button--primary } [Мифы Tor & FAQ](advanced/tor-overview.md){ .md-button }

[Подробный обзор VPN :material-arrow-right-drop-circle:](basics/vpn-overview.md ""){.md-button}

## Рекомендованные провайдеры

Рекомендуемые нами провайдеры находятся за пределами США, используют шифрование, принимают Monero, поддерживают WireGuard и OpenVPN и не сохраняют логи вашего трафика. Для получения дополнительной информации, ознакомьтесь с [полным списком критериев](#criteria).

### Proton VPN

!!! recommendation annotate

    ![Логотип Proton VPN](assets/img/vpn/protonvpn.svg){ align=right }
    
    **Proton VPN** - сильный соперник в сфере VPN, работающий с 2016 года. Proton AG базируется в Швейцарии и предлагает ограниченный бесплатный доступ, а также более функциональный премиум вариант.
    
    [:octicons-home-16: Домашняя страница](https://protonvpn.com/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://protonvpn.com/privacy-policy){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://protonvpn.com/support/){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/ProtonVPN){ .card-link title="Исходный код" }
    
    ??? downloads "Скачать"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android)
        - [:simple-appstore: App Store](https://apps.apple.com/app/apple-store/id1437005085)
        - [:simple-github: GitHub](https://github.com/ProtonVPN/android-app/releases)
        - [:simple-windows11: Windows](https://protonvpn.com/download-windows)
        - [:simple-linux: Linux](https://protonvpn.com/support/linux-vpn-setup/)

#### :material-check:{ .pg-green } 68 Стран

Серверы Proton VPN находятся [в 68 странах](https://protonvpn.com/vpn-servers).(1) Выбор VPN-провайдера с ближайшим к вам сервером позволит снизить задержку передаваемого вами сетевого трафика. Это происходит из-за более короткого маршрута (меньше промежуточных серверов) до пункта назначения.
{ .annotate }

1. Последняя проверка: 28.07.2023

Мы также считаем, что для безопасности закрытых ключей VPN-провайдера ему следует использовать [выделенные серверы](https://ru.wikipedia.org/wiki/%D0%92%D1%8B%D0%B4%D0%B5%D0%BB%D0%B5%D0%BD%D0%BD%D1%8B%D0%B9_%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80), а не более дешевые виртуальные хостинги (которые разделены между несколькими клиентами), такие как [виртуальные частные серверы](https://ru.wikipedia.org/wiki/VPS).

#### :material-check:{ .pg-green } Независимый аудит

По состоянию на январь 2020 года компания Proton VPN прошла независимый аудит от SEC Consult. SEC Consult обнаружила несколько уязвимостей среднего и низкого риска в приложениях Proton VPN для Windows, Android и iOS, все из которых Proton VPN "должным образом устранил" ещё до публикации отчетов. Ни одна из выявленных проблем не предоставила бы злоумышленнику удаленный доступ к вашему устройству или трафику. Вы можете просмотреть отдельные отчеты для каждой платформы на сайте [protonvpn.com](https://protonvpn.com/blog/open-source/). В апреле 2022 года Proton VPN прошел [еще один аудит](https://protonvpn.com/blog/no-logs-audit/), отчет был [подготовлен компанией Securitum](https://protonvpn.com/blog/wp-content/uploads/2022/04/securitum-protonvpn-nologs-20220330.pdf). [Аттестационное письмо](https://proton.me/blog/security-audit-all-proton-apps) было предоставлено для приложений Proton VPN 9 ноября 2021 года компанией [Securitum](https://research.securitum.com).

#### :material-check:{ .pg-green } Клиенты с открытым исходным кодом

Proton VPN предоставляет исходный код для своих настольных и мобильных клиентов в своём [GitHub](https://github.com/ProtonVPN).

#### :material-check:{ .pg-green } Принимает наличные

Помимо приема кредитных/дебетовых карт и PayPal, Proton VPN принимает [Bitcoin](advanced/payments.md#other-coins-bitcoin-ethereum-etc) и **наличные/местные валюты** как анонимные формы платежа.

#### :material-check:{ .pg-green } Поддержка WireGuard

Proton VPN, в основном, поддерживает протокол WireGuard®. [WireGuard](https://www.wireguard.com) - это более новый протокол, которой использует современную [криптография](https://www.wireguard.com/protocol/). Кроме того, WireGuard стремится быть более простым и производительным.

Proton VPN [рекомендует](https://protonvpn.com/blog/wireguard/) использовать WireGuard вместе со своими сервисами. В приложениях Proton VPN для Windows, macOS, iOS, Android, ChromeOS и Android TV протокол WireGuard используется по умолчанию; однако [поддержка](https://protonvpn.com/support/how-to-change-vpn-protocols/) для этого протокола отсутствует в их приложении для Linux.

#### :material-alert-outline:{ .pg-orange } Удалённая переадресация портов

В настоящее время Proton VPN поддерживает только эфемерную удаленную [переадресацию портов](https://protonvpn.com/support/port-forwarding/) через NAT-PMP, со временем аренды на 60 секунд. Приложение для Windows обеспечивает легкий доступ к нему, в то время как в других операционных системах вам придется запустить собственное [приложение NAT-PMP](https://protonvpn.com/support/port-forwarding-manual-setup/). Торрент приложения часто поддерживают NAT-PMP нативно.

#### :material-check:{ .pg-green } Приложения для смартфонов

Помимо предоставления стандартных файлов конфигурации OpenVPN, Proton VPN имеет мобильные клиенты в [App Store](https://apps.apple.com/us/app/protonvpn-fast-secure-vpn/id1437005085), [Google Play](https://play.google.com/store/apps/details?id=ch.protonvpn.android&hl=en_US), и [GitHub](https://github.com/ProtonVPN/android-app/releases), позволяющие легко подключаться к их серверам.

#### :material-information-outline:{ .pg-blue } Дополнительная функциональность

В настоящее время клиенты Proton VPN поддерживают двухфакторную аутентификацию на всех платформах, кроме Linux. Proton VPN имеет собственные серверы и дата-центры в Швейцарии, Исландии и Швеции. Он предлагает блокировку рекламы и блокировку известных вредоносных доменов с помощью их DNS. Кроме того, Proton VPN также предлагает "Tor" серверы, позволяющие легко подключаться к onion сайтам, но мы все же настоятельно рекомендуем использовать для этих целей [официальный Tor Browser](https://www.torproject.org/).

#### :material-alert-outline:{ .pg-orange } Функция Killswitch не работает на Mac на базе Intel

При использовании VPN killswitch [возможны системные сбои](https://protonvpn.com/support/macos-t2-chip-kill-switch/) на компьютерах Mac на базе Intel. Если вам необходима эта функция, и вы используете Mac с чипсетом Intel, вам следует рассмотреть возможность использования другой службы VPN.

### IVPN

!!! recommendation

    ![Логотип IVPN](assets/img/vpn/ivpn.svg){ align=right }
    
    **IVPN** — еще один платный VPN-провайдер, работающий с 2009 года. Компания IVPN базируется в Гибралтаре.
    
    [:octicons-home-16: Домашняя страница](https://www.ivpn.net/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://www.ivpn.net/privacy/){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://www.ivpn.net/knowledgebase/general/){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/ivpn){ .card-link title="Исходный код" }
    
    ??? downloads "Скачать"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client)
        - [:octicons-moon-16: Accrescent](https://accrescent.app/app/net.ivpn.client)
        - [:simple-appstore: App Store](https://apps.apple.com/app/ivpn-serious-privacy-protection/id1193122683)
        - [:simple-windows11: Windows](https://www.ivpn.net/apps-windows/)
        - [:simple-apple: macOS](https://www.ivpn.net/apps-macos/)
        - [:simple-linux: Linux](https://www.ivpn.net/apps-linux/)

#### :material-check:{ .pg-green } 35 стран

Серверы IVPN находятся [в 35 странах](https://www.ivpn.net/server-locations).(1) Выбор VPN с ближайшим к вам сервером позволит снизить задержку передаваемого вами трафика. Это происходит из-за более короткого маршрута (меньше промежуточных серверов) до пункта назначения.
{ .annotate }

1. Последняя проверка: 28.07.2023

Мы также считаем, что для безопасности закрытых ключей VPN-провайдера ему следует использовать [выделенные серверы](https://ru.wikipedia.org/wiki/%D0%92%D1%8B%D0%B4%D0%B5%D0%BB%D0%B5%D0%BD%D0%BD%D1%8B%D0%B9_%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80), а не более дешевые виртуальные хостинги (которые разделены между несколькими клиентами), такие как [виртуальные частные серверы](https://ru.wikipedia.org/wiki/VPS).

#### :material-check:{ .pg-green } Независимый аудит

IVPN прошла [аудит отсутствия логов от Cure53](https://cure53.de/audit-report_ivpn.pdf), который подтвердил заявление IVPN о том, что они не сохраняют логи. IVPN также подготовила [отчет о комплексном пентесте Cure53](https://cure53.de/summary-report_ivpn_2019.pdf) в январе 2020 года. Кроме того, IVPN заявила, что в будущем планирует составлять [годовые отчеты](https://www.ivpn.net/blog/independent-security-audit-concluded). Следующий аудит был проведен [в апреле 2022 года](https://www.ivpn.net/blog/ivpn-apps-security-audit-2022-concluded/) и представлен компанией Cure53 [на их сайте](https://cure53.de/pentest-report_IVPN_2022.pdf).

#### :material-check:{ .pg-green } Клиенты с открытым исходным кодом

Начиная с февраля 2020 года [открыт исходный код приложений IVPN](https://www.ivpn.net/blog/ivpn-applications-are-now-open-source). Исходный код можно получить из их [репозиториев на GitHub](https://github.com/ivpn).

#### :material-check:{ .pg-green } Принимает наличные и Monero

Помимо приема кредитных/дебетовых карт и PayPal, IVPN принимает биткоины, **Monero** и **наличные/местные валюты** (по годовым планам) как анонимные формы платежа.

#### :material-check:{ .pg-green } Поддержка WireGuard

IVPN поддерживает протокол WireGuard®️. [WireGuard](https://www.wireguard.com) - это более новый протокол, которой использует современную [криптография](https://www.wireguard.com/protocol/). Кроме того, WireGuard стремится быть более простым и производительным.

IVPN [рекомендует](https://www.ivpn.net/wireguard/) использовать WireGuard для их сервиса, и поэтому протокол по умолчанию используется во всех IVPN приложениях. IVPN также предлагает генератор конфигурации WireGuard для использования с официальными [приложениями](https://www.wireguard.com/install/)WireGuard.

#### :material-alert-outline:{ .pg-orange } Удаленная переадресация портов

IVPN ранее поддерживал перенаправление портов, но убрал эту опцию в [июне 2023 года](https://www.ivpn.net/blog/gradual-removal-of-port-forwarding). Отсутствие этой функции может негативно сказаться на некоторых приложениях, особенно на пиринговых приложениях, таких как торрент-клиенты.

#### :material-check:{ .pg-green } Приложения для смартфонов

Помимо обычных файлов конфигурации OpenVPN, IVPN предлагает приложения в [App Store](https://apps.apple.com/us/app/ivpn-serious-privacy-protection/id1193122683), [Google Play](https://play.google.com/store/apps/details?id=net.ivpn.client) и на [GitHub](https://github.com/ivpn/android-app/releases), позволяющие легко подключиться к их серверам.

#### :material-information-outline:{ .pg-blue } Дополнительная функциональность

Приложения IVPN поддерживают двухфакторную аутентификацию (приложения Mullvad - нет). IVPN также предоставляет функцию "[AntiTracker](https://www.ivpn.net/antitracker)", которая блокирует рекламу и трекеры на сетевом уровне.

### Mullvad

!!! recommendation

    ![Логотип Mullvad](assets/img/vpn/mullvad.svg){ align=right }
    
    **Mullvad** - это быстрый и недорогой VPN с серьезным акцентом на прозрачность и безопасность. Выбор VPN-провайдера с ближайшим к вам сервером позволит снизить задержку передаваемого вами сетевого трафика. Это происходит из-за более короткого маршрута (меньше промежуточных серверов) до пункта назначения.
    
    [:octicons-home-16: Домашняя страница](https://mullvad.net){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion){ .card-link title="Сервис Onion" }
    [:octicons-eye-16:](https://mullvad.net/en/help/privacy-policy/){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://mullvad.net/en/help/){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/mullvad){ .card-link title="Исходный код" }
    
    ??? downloads "Скачать"
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn)
        - [:simple-appstore: App Store](https://apps.apple.com/app/mullvad-vpn/id1488466513)
        - [:simple-github: GitHub](https://github.com/mullvad/mullvadvpn-app/releases)
        - [:simple-windows11: Windows](https://mullvad.net/en/download/windows/)
        - [:simple-apple: macOS](https://mullvad.net/en/download/macos/)
        - [:simple-linux: Linux](https://mullvad.net/en/download/linux/)

#### :material-check:{ .pg-green } 43 Страны

Серверы Mullvad находятся [в 43 странах](https://mullvad.net/servers/).(1) Выбор VPN с ближайшим к вам сервером позволит снизить задержку передаваемого вами трафика. Это происходит из-за более короткого маршрута (меньше промежуточных серверов) до пункта назначения.
{ .annotate }

1. Последняя проверка: 28.07.2023

Мы также считаем, что для безопасности закрытых ключей VPN-провайдера ему следует использовать [выделенные серверы](https://ru.wikipedia.org/wiki/%D0%92%D1%8B%D0%B4%D0%B5%D0%BB%D0%B5%D0%BD%D0%BD%D1%8B%D0%B9_%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80), а не более дешевые виртуальные хостинги (которые разделены между несколькими клиентами), такие как [виртуальные частные серверы](https://ru.wikipedia.org/wiki/VPS).

#### :material-check:{ .pg-green } Независимый аудит

Приложения Mullvad VPN прошли аудит от Cure53 и Assured AB в отчёте на проникновение [опубликованном на сайте cure53.de](https://cure53.de/pentest-report_mullvad_v2.pdf). Исследователи безопасности пришли к выводу:

> Cure53 и Assured AB довольны результатами аудита, а программное обеспечение оставляет в целом положительное впечатление. Учитывая преданность безопасности внутренней команды Mullvad VPN, у тестеров нет сомнений в том, что проект находится на правильном пути с точки зрения безопасности.

В 2020 году [было объявлено](https://mullvad.net/blog/2020/6/25/results-available-audit-mullvad-app/) о проведении повторного аудита и на сайте Cure53 был размещен [итоговый отчет об аудите](https://cure53.de/pentest-report_mullvad_2020_v2.pdf):

> Результаты этого проекта, осуществляемого в мае-июне 2020 года и направленного на комплекс Mullvad, весьма позитивны. [...] Общая экосистема приложений, используемая Mullvad, оставляет впечатление надежности и структурированности. Общая структура приложения позволяет легко и структурировано внедрять исправления и патчи. Более того, результаты, обнаруженные Cure53, демонстрируют важность постоянного аудита и переоценки текущих векторов утечки, чтобы всегда обеспечивать конфиденциальность конечных пользователей. Mullvad отлично справляется с защитой конечных пользователей от утечек личной информации и рисков, связанных с конфиденциальностью.

В 2021 году [было объявлено](https://mullvad.net/en/blog/2021/1/20/no-pii-or-privacy-leaks-found-cure53s-infrastructure-audit/) о проведении аудита инфраструктуры и на сайте Cure53 был размещен [итоговый отчет об аудите](https://cure53.de/pentest-report_mullvad_2021_v1.pdf). Другой отчет был заказан [в июне 2022 года](https://mullvad.net/en/blog/2022/6/22/vpn-server-audit-found-no-information-leakage-or-logging-of-customer-data/) и доступен на [сайте Assured](https://www.assured.se/publications/Assured_Mullvad_relay_server_audit_report_2022.pdf).

#### :material-check:{ .pg-green } Клиенты с открытым исходным кодом

Mullvad предоставляет исходный код для своих настольных и мобильных клиентов в [GitHub](https://github.com/mullvad/mullvadvpn-app).

#### :material-check:{ .pg-green } Принимает наличные и Monero

Помимо приема кредитных/дебетовых карт и PayPal, Mullvad принимает Bitcoin, Bitcoin Cash, **Monero** и **наличные/местные валюты** как анонимные формы платежа. Они также принимают Swish и банковские переводы.

#### :material-check:{ .pg-green } Поддержка WireGuard

Mullvad поддерживает протокол WireGuard®. [WireGuard](https://www.wireguard.com) - это более новый протокол, которой использует современную [криптография](https://www.wireguard.com/protocol/). Кроме того, WireGuard стремится быть более простым и производительным.

Mullvad [рекомендует](https://mullvad.net/en/help/why-wireguard/) использовать WireGuard с их сервисами. Это протокол по умолчанию или единственный протокол в приложениях Mullvad для Android, iOS, macOS и Linux, но в Windows вам придется [вручную включить](https://mullvad.net/en/help/how-turn-wireguard-mullvad-app/) WireGuard. Mullvad также предлагает генератор конфигурации WireGuard для использования с официальными[приложениями](https://www.wireguard.com/install/) WireGuard.

#### :material-check:{ .pg-green } Поддержка IPv6

Mullvad позволяет вам [получить доступ к сервисам, размещенным на IPv6](https://mullvad.net/en/blog/2014/9/15/ipv6-support/), в отличие от других провайдеров, которые блокируют IPv6-соединения.

#### :material-alert-outline:{ .pg-orange } Удалённая переадресация портов

Mullvad ранее поддерживал переадресацию портов, но убрал эту возможность в [мае 2023 года](https://mullvad.net/en/blog/2023/5/29/removing-the-support-for-forwarded-ports/). Отсутствие этой функции может негативно сказаться на некоторых приложениях, особенно на пиринговых приложениях, таких как торрент-клиенты.

#### :material-check:{ .pg-green } Приложения для смартфонов

Mullvad опубликовал клиенты в [App Store](https://apps.apple.com/app/mullvad-vpn/id1488466513) и [Google Play](https://play.google.com/store/apps/details?id=net.mullvad.mullvadvpn), оба поддерживают простой в использовании интерфейс, не требующий ручной настройки соединения WireGuard. Клиент для Android также доступен на [GitHub](https://github.com/mullvad/mullvadvpn-app/releases).

#### :material-information-outline:{ .pg-blue } Дополнительная функциональность

Mullvad очень прозрачен в отношении того, какими узлами они [владеют или арендуют](https://mullvad.net/en/servers/). Они используют [ShadowSocks](https://shadowsocks.org/) в конфигурации ShadowSocks + OpenVPN, что делает их более устойчивыми к фаэрволам с [Deep Packet Inspection](https://en.wikipedia.org/wiki/Deep_packet_inspection), пытающимся блокировать VPN. Предположительно, [Китаю приходится использовать другой метод для блокировки серверов ShadowSocks](https://github.com/net4people/bbs/issues/22). Сайт Mullvad также доступен через Tor по адресу [o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion](http://o54hon2e2vj6c7m3aqqu6uyece65by3vgoxxhlqlsvkmacw6a7m7kiad.onion).

## Критерии

!!! danger "Опасность"

    Важно отметить, что использование VPN не сделает вас анонимным, но в определенных ситуациях это обеспечит вам лучшую конфиденциальность. VPN не является инструментом для незаконной деятельности. Не полагайтесь на политику "отсутствия логов".

**Обратите внимание, что мы не связаны ни с одним из рекомендуемых нами провайдеров. Это позволяет нам давать абсолютно объективные рекомендации.** Помимо [наших стандартных критериев](about/criteria.md), мы разработали четкий набор требований к любому VPN-провайдеру, желающему быть рекомендованным, включая надежное шифрование, независимый аудит безопасности, современные технологии и многое другое. Мы рекомендуем вам ознакомиться с этим списком перед выбором VPN-провайдера, а также провести собственное исследование, чтобы убедиться, что выбранный вами VPN-провайдер заслуживает максимального доверия.

### Технологии

Мы требуем, чтобы все рекомендуемые нами VPN-провайдеры предоставляли файлы конфигурации OpenVPN для использования в любом клиенте. **Если** VPN предоставляет свой собственный пользовательский клиент, мы требуем наличия killswitch для блокировки утечки сетевых данных при отключении.

**Минимальные требования:**

- Поддержка надежных протоколов, таких как WireGuard & OpenVPN.
- Killswitch встроен в приложения.
- Поддержка Multihop. Multihop важен для сохранения конфиденциальности данных в случае компрометации одного узла.
- Если предоставляются приложения VPN, они должны быть [с открытым исходным кодом](https://en.wikipedia.org/wiki/Open_source), как и программное обеспечение VPN, которое обычно в них встроено. Мы считаем, что доступность [исходного кода](https://en.wikipedia.org/wiki/Source_code) обеспечивает большую прозрачность в отношении того, что на самом деле делает ваше устройство.

**В лучшем случае:**

- Поддержка WireGuard и OpenVPN.
- Killswitch с широкими возможностями настройки (включение/выключение в определенных сетях, при включении и т.д.)
- Простые в использовании приложения VPN
- Поддержка [IPv6](https://en.wikipedia.org/wiki/IPv6). Мы ожидаем, что серверы будут разрешать входящие соединения через IPv6 и позволят вам получить доступ к услугам, размещенным на адресах IPv6.
- Возможность [удаленной переадресации портов](https://en.wikipedia.org/wiki/Port_forwarding#Remote_port_forwarding) помогает создавать соединения при использовании программного обеспечения для обмена файлами P2P ([Peer-to-Peer](https://en.wikipedia.org/wiki/Peer-to-peer)) или хостинга сервера (например, Mumble).

### Конфиденциальность

Мы предпочитаем, чтобы рекомендуемые нами поставщики собирали как можно меньше данных. Не собирали личную информацию при регистрации и принимали анонимные формы оплаты.

**Минимальные требования:**

- [Анонимная криптовалюта](cryptocurrency.md) **или** возможность оплаты наличными.
- Для регистрации не требуется никакой личной информации: Только имя пользователя, пароль и, максимум электронная почта.

**В лучшем случае:**

- Принимает множество [анонимных вариантов оплаты](advanced/payments.md).
- Не принимается личная информация (автогенерируемое имя пользователя, не требуется электронная почта и т.д.).

### Безопасность

VPN бессмысленен, если он даже не может обеспечить адекватную безопасность. Мы требуем, чтобы все рекомендуемые нами провайдеры соблюдали современные стандарты безопасности для своих соединений OpenVPN. В идеале, они должны по умолчанию использовать более перспективные схемы шифрования. Мы также требуем, чтобы независимая третья сторона провела аудит безопасности провайдера, в идеале - в полном объеме и на повторяющейся (ежегодной) основе.

**Минимальные требования:**

- Надежные схемы шифрования: OpenVPN с аутентификацией SHA-256; рукопожатие RSA-2048 или лучше; шифрование данных AES-256-GCM или AES-256-CBC.
- Прямая секретность.
- Опубликованные аудиты безопасности от авторитетной сторонней фирмы.

**В лучшем случае:**

- Самое сильное шифрование: RSA-4096.
- Прямая секретность.
- Опубликованные аудиты безопасности от авторитетной сторонней фирмы.
- Программы "bug-bounty" и/или скоординированный процесс раскрытия информации об уязвимостях.

### Доверие

Вы бы не доверили свои финансы человеку с фальшивой личностью, так зачем доверять ему свой интернет трафик? Мы требуем, чтобы рекомендованные нами поставщики услуг открыто заявляли о своих владельцах или своём руководстве. Мы также хотели бы видеть частые отчеты о прозрачности, особенно в отношении того, как обрабатываются правительственные запросы.

**Минимальные требования:**

- Руководство или владение, ориентированное на общественность.

**В лучшем случае:**

- Лидерство, ориентированное на общественность.
- Частые отчеты о прозрачности.

### Маркетинг

От провайдеров VPN, которых мы рекомендуем, мы ожидаем ответственный маркетинг.

**Минимальные требования:**

- Должен самостоятельно проводить аналитику (т.е. не Google Analytics). Сайт провайдера также должен соответствовать требованиям [DNT (Do Not Track)](https://en.wikipedia.org/wiki/Do_Not_Track) для людей, которые хотят отказаться от аналитики.

Не должно быть никакого маркетинга, который является безответственным:

- Предоставление гарантий защиты анонимности на 100%. Когда кто-то утверждает: "Это является на 100% ..." - это не означает, что кто-то не может ошибиться. Мы знаем, что люди могут довольно легко деанонимизировать себя различными способами, например:
    - Повторное использование личной информации, например (учетные записи электронной почты, уникальные псевдонимы и т.д.), к которой они получили доступ без программного обеспечения обеспечивающего анонимность (Tor, VPN и т.д.)
    - [Цифровые отпечатки браузера](https://en.wikipedia.org/wiki/Device_fingerprint#Browser_fingerprint)
- Утверждение, что VPN с одним слоем "более анонимен", чем Tor, который представляет собой сеть из трех или более, регулярно меняющихся, слоёв.
- Использует ответственные формулировки: например, можно сказать, что VPN "отключена" или "не подключена", но утверждать, что кто-то "подвержен утечкам", "уязвим" или "скомпрометирован" - это ненужное использование тревожных формулировок, которые могут быть неверными. Например, этот человек может быть просто использует другого провайдера VPN или Tor.

**В лучшем случае:**

Ответственный маркетинг, который является одновременно образовательным и полезным для потребителя, может включать:

- Точное описание ситуаций, когда вместо VPN следует использовать [Tor](tor.md).
- Доступность веб-сайта провайдера VPN через сервис [.onion](https://en.wikipedia.org/wiki/.onion)

### Дополнительная функциональность

Хотя это и не является строгими требованиями, существуют и другие факторы удобства или конфиденциальности, на которые мы обращали внимание при выборе рекомендуемых провайдеров. К ним относятся функции блокировки рекламы/трекеров, свидетельство канарейки, многослойные соединения, отличная поддержка клиентов, количество разрешенных одновременных подключений и т.д.
