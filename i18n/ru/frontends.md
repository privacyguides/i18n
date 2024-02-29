---
title: "Фронтенды"
icon: material/flip-to-front
description: Эти фронтенды с открытым исходным кодом для различных интернет-сервисов позволяют получить доступ к содержимому без JavaScript или других раздражающих факторов.
cover: frontends.webp
---

Иногда сервисы пытаются заставить вас создать аккаунт, блокируя доступ к контенту с помощью назойливых всплывающих окон. Они также могут не работать без включенного JavaScript. Эти фронтенды могут позволить вам обойти эти ограничения.

Если вы решите самостоятельно хостить эти фронтенды, важно, чтобы вашим экземпляром пользовались и другие люди, чтобы вашу активность нельзя было отследить. Вы должны быть осторожны с тем, где и как вы размещаете хостинг, поскольку активность других людей будет связана с вашим хостингом.

Если вы используете чей-то экземпляр, обязательно ознакомьтесь с политикой конфиденциальности этого конкретного экземпляра. Они могут быть изменены их владельцами и поэтому могут не отражать политику по умолчанию. Некоторые экземпляры имеют адреса .onion, которые могут обеспечить некоторую конфиденциальность, если ваши поисковые запросы не содержат ПД.

## TikTok

### ProxiTok

!!! recommendation

    ![ProxiTok logo](assets/img/frontends/proxitok.svg){ align=right }
    
    **ProxiTok** is an open-source frontend to the [TikTok](https://www.tiktok.com) website that is also self-hostable.
    
    Существует ряд публичных экземпляров, причем некоторые экземпляры имеют поддержку [Tor](https://www.torproject.org).
    
    [:octicons-repo-16: Репозиторий](https://github.com/pablouser1/ProxiTok){ .md-button .md-button--primary }
    [:octicons-server-16:](https://github.com/pablouser1/ProxiTok/wiki/Public-instances){ .card-link title="Публичный экземпляр"}
    [:octicons-info-16:](https://github.com/pablouser1/ProxiTok/wiki){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/pablouser1/ProxiTok){ .card-link title="Исходный код" }

!!! tip "Совет"

    ProxiTok полезен, если вы хотите отключить JavaScript в своем браузере, как в случае с [Tor Browser](https://www.torproject.org/) с выбранным "высшим" уровне безопасности.

## YouTube

### FreeTube

!!! recommendation

    ![Логотип FreeTube](assets/img/frontends/freetube.svg){ align=right }
    
    **FreeTube** - это бесплатное настольное приложение с открытым исходным кодом для [YouTube](https://youtube.com). Когда вы используете FreeTube, ваш список подписок и плейлисты сохранены локально на вашем устройстве.
    
    По умолчанию FreeTube блокирует всю рекламу YouTube. Кроме того, FreeTube опционально интегрируется с [SponsorBlock](https://sponsor.ajay.app), чтобы помочь вам пропускать спонсируемые сегменты видео.
    
    [:octicons-home-16: Домашняя страница](https://freetubeapp.io){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://freetubeapp.io/privacy.php){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://docs.freetubeapp.io/){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/FreeTubeApp/FreeTube){ .card-link title="Исходный код" }
    [:octicons-heart-16:](https://liberapay.com/FreeTube){ .card-link title=Поддержать }
    
    ??? downloads "Скачать"
    
        - [:simple-windows11: Windows](https://freetubeapp.io/#download)
        - [:simple-apple: macOS](https://freetubeapp.io/#download)
        - [:simple-linux: Linux](https://freetubeapp.io/#download)
        - [:simple-flathub: Flathub](https://flathub.org/apps/details/io.freetubeapp.FreeTube)

!!! warning "Осторожно"

    При использовании FreeTube ваш IP-адрес все равно может быть известен YouTube, [Invidious](https://instances.invidious.io) или [SponsorBlock](https://sponsor.ajay.app/) в зависимости от вашей конфигурации. Используйте [VPN](/vpn) или [Tor](https://www.torproject.org), если ваша [модель угроз](/threat-modeling) требует скрытия вашего IP-адреса.

### Yattee

!!! recommendation

    ![Логотип Yattee](assets/img/frontends/yattee.svg){ align=right }
    
    **Yattee** - это бесплатный, ориентированный на конфиденциальность видеоплеер с открытым исходным кодом для iOS, tvOS и macOS для [YouTube](https://youtube.com). При использовании Yattee список подписок сохраняется локально на вашем устройстве.
    
    Вам придется сделать несколько [дополнительных шагов](https://gonzoknows.com/posts/Yattee/), прежде чем вы сможете использовать Yattee для просмотра YouTube, из-за ограничений App Store.
    
    [:octicons-home-16: Домашняя страница](https://github.com/yattee/yattee){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://r.yattee.stream/docs/privacy.html){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://github.com/yattee/yattee/wiki){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/yattee/yattee){ .card-link title="Исходный код" }
    [:octicons-heart-16:](https://github.com/yattee/yattee/wiki/Donations){ .card-link title=Поддержать }
    
    ??? downloads "Скачать"
    
        - [:simple-apple: App Store](https://apps.apple.com/us/app/yattee/id1595136629)
        - [:simple-github: GitHub](https://github.com/yattee/yattee/releases)

!!! warning "Осторожно"

    При использовании Yattee ваш IP-адрес все еще может быть известен YouTube, [Invidious](https://instances.invidious.io), [Piped](https://github.com/TeamPiped/Piped/wiki/Instances) или [SponsorBlock](https://sponsor.ajay.app/) в зависимости от вашей конфигурации. Используйте [VPN](/vpn) или [Tor](https://www.torproject.org), если ваша [модель угроз](/threat-modeling) требует скрытия вашего IP-адреса.

По умолчанию Yattee блокирует всю рекламу на YouTube. Кроме того, Yattee опционально интегрируется с [SponsorBlock](https://sponsor.ajay.app), чтобы помочь вам пропускать спонсируемые сегменты видео.

### LibreTube (Android)

!!! recommendation

    ![Логотип LibreTube](assets/img/frontends/libretube.svg#only-light){ align=right }
    ![Логотип LibreTube](assets/img/frontends/libretube-dark.svg#only-dark){ align=right }
    
    **LibreTube** - это бесплатное приложение для Android с открытым исходным кодом для доступа к [YouTube](https://youtube.com), которое использует API [Piped](#piped).
    
    LibreTube позволяет хранить список подписок и плейлисты локально на устройстве Android или в учетной записи на выбранном вами экземпляре Piped, что дает возможность беспрепятственного доступа к ним и на других устройствах.
    
    [:octicons-home-16: Домашняя страница](https://libre-tube.github.io){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://github.com/libre-tube/LibreTube#privacy-policy-and-disclaimer){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://github.com/libre-tube/LibreTube#readme){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/libre-tube/LibreTube){ .card-link title="Исходный код" }
    
    ??? downloads "Скачать"
    
        - [:simple-github: GitHub](https://github.com/libre-tube/LibreTube/releases)

!!! warning "Осторожно"

    При использовании LibreTube ваш IP-адрес будет виден выбранному вами экземпляру [Piped](https://github.com/TeamPiped/Piped/wiki/Instances) и/или [SponsorBlock](https://sponsor.ajay.app/) в зависимости от вашей конфигурации. Используйте [VPN](/vpn) или [Tor](https://www.torproject.org), если ваша [модель угроз](/threat-modeling) требует скрытия вашего IP-адреса.

По умолчанию LibreTube блокирует всю рекламу YouTube. Кроме того, Libretube использует [SponsorBlock](https://sponsor.ajay.app), чтобы помочь вам пропускать спонсируемые сегменты видео. Вы можете полностью настроить типы сегментов, которые SponsorBlock будет пропускать, или полностью отключить его. На самом видеоплеере также есть кнопка, позволяющая при желании отключить его для конкретного видео.

### NewPipe (Android)

!!! recommendation annotate

    ![Логотип Newpipe](assets/img/frontends/newpipe.svg){ align=right }
    
    **NewPipe** - это бесплатное приложение для Android с открытым исходным кодом для [YouTube](https://youtube.com), [SoundCloud](https://soundcloud.com), [media.ccc.de](https://media.ccc.de), [Bandcamp](https://bandcamp.com) и [PeerTube](https://joinpeertube.org/) (1).
    
    Список подписок и плейлисты сохраняются локально на вашем устройстве Android.
    
    [:octicons-home-16: Домашняя страница](https://newpipe.net){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://newpipe.net/legal/privacy){ .card-link title="Политика конфиденциальности" }
    [:octicons-info-16:](https://teamnewpipe.github.io/documentation/){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/TeamNewPipe/NewPipe){ .card-link title="Исходный код" }
    [:octicons-heart-16:](https://newpipe.net/donate/){ .card-link title=Поддержать }
    
    ??? downloads "Скачать"
    
        - [:simple-github: GitHub](https://github.com/TeamNewPipe/NewPipe/releases)

1. По умолчанию используется экземпляр [FramaTube](https://framatube.org/), однако другие экземпляры можно добавить через **Настройки** → **Контент** → **Серверы PeerTube**

!!! warning "Осторожно"

    При использовании NewPipe ваш IP-адрес будет виден используемым видеопровайдерам. Используйте [VPN](/vpn) или [Tor](https://www.torproject.org), если ваша [модель угроз](/threat-modeling) требует скрытия вашего IP-адреса.

### Invidious

!!! recommendation

    ![Логотип Invidious](assets/img/frontends/invidious.svg#only-light){ align=right }
    ![Логотип Invidious](assets/img/frontends/invidious-dark.svg#only-dark){ align=right }
    
    **Invidious** - это бесплатный фронтенд с открытым исходным кодом для [YouTube](https://youtube.com), который можно самостоятельно хостить.
    
    Существует ряд публичных экземпляров, причем некоторые экземпляры имеют поддержку [Tor](https://www.torproject.org).
    
    [:octicons-home-16: Домашняя страница](https://invidious.io){ .md-button .md-button--primary }
    [:octicons-server-16:](https://instances.invidious.io){ .card-link title="Публичный экземпляр"}
    [:octicons-info-16:](https://docs.invidious.io/){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/iv-org/invidious){ .card-link title="Исходный код" }
    [:octicons-heart-16:](https://invidious.io/donate/){ .card-link title=Поддержать }

!!! warning "Осторожно"

    По умолчанию Invidious не проксирует видеопотоки. Видео, просматриваемое через Invidious, по-прежнему будет напрямую подключаться к серверам Google (например, `googlevideo.com`); однако некоторые экземпляры поддерживают проксирование видео - просто включите *Proxy videos* в настройках экземпляра или добавьте `&local=true` к URL.

!!! tip "Совет"

    Invidious полезен, если вы хотите отключить JavaScript в вашем браузере, например [Tor Browser](https://www.torproject.org/) с выбранным "высшим" уровне безопасности. Сам по себе он не обеспечивает конфиденциальности, и мы не рекомендуем входить в какие-либо учетные записи.

### Piped

!!! recommendation

    ![Логотип Piped](assets/img/frontends/piped.svg){ align=right }
    
    **Piped** - это бесплатный фронтенд с открытым исходным кодом для [YouTube](https://youtube.com), который можно самостоятельно хостить.
    
    Для работы Piped требуется JavaScript, и существует множество публичных экземпляров.
    
    [:octicons-repo-16: Репозиторий](https://github.com/TeamPiped/Piped){ .md-button .md-button--primary }
    [:octicons-server-16:](https://piped.kavin.rocks/preferences#ddlInstanceSelection){ .card-link title="Публичный экземпляр"}
    [:octicons-info-16:](https://piped-docs.kavin.rocks/){ .card-link title=Документация}
    [:octicons-code-16:](https://github.com/TeamPiped/Piped){ .card-link title="Исходный код" }
    [:octicons-heart-16:](https://github.com/TeamPiped/Piped#donations){ .card-link title=Поддержать }

!!! tip "Совет"

    Piped полезен, если вы хотите использовать [SponsorBlock](https://sponsor.ajay.app) без установки расширения или получить доступ к контенту с возрастными ограничениями без учетной записи. Сам по себе он не обеспечивает конфиденциальности, и мы не рекомендуем входить в какие-либо учетные записи.

## Критерии

**Обрати внимание, что у нас нет связей ни с одним проектом, который мы рекомендуем.** В дополнение к [нашим стандартным критериям](about/criteria.md) мы разработали четкий набор требований, позволяющий давать объективные рекомендации. Перед тем, как вы решите выбрать какой-либо проект, мы рекомендуем вам ознакомиться со списком критериев и провести собственное исследование, чтобы убедиться в правильности своего выбора.

!!! example "Это новый раздел"

    Мы всё еще работаем над установлением критериев для каждого раздела нашего сайта, поэтому они могут поменяться в будущем. Если у вас есть вопросы по поводу наших критериев, пожалуйста, [задавайте их на нашем форуме](https://discuss.privacyguides.net/latest). Если какой-то критерий здесь не указан, это не значит, что мы его не учли. Перед тем, как рекомендовать какой-либо проект мы учитываем и обсуждаем множество факторов. Документирование этих факторов ещё не завершено.

Рекомендованные фронтенды...

- Должны иметь открытый исходный код.
- Должны иметь возможность самостоятельного хостинга.
- Должны предоставлять все основные функции сайта анонимным пользователям.

Мы рассматриваем фронтенды только для сайтов, которые...

- Normally only accessible with JavaScript enabled.
