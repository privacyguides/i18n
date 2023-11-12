---
meta_title: "Tor Browser and Network: Anonymous Web Browsing - Privacy Guides"
title: "Tor Network"
icon: simple/torproject
description: Protect your internet browsing from prying eyes by using the Tor network, a secure network which circumvents censorship.
cover: tor.webp
schema:
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: متصفِّح تور
    image: /assets/img/browsers/tor.svg
    url: https://www.torproject.org
    sameAs: https://en.wikipedia.org/wiki/Tor_(network)
    applicationCategory: Web Browser
    operatingSystem:
      - Windows
      - macOS
      - Linux
      - Android
    subjectOf:
      "@type": WebPage
      url: "./"
---

![شعار تور](assets/img/self-contained-networks/tor.svg){ align=right }

شبكة **تور** هي خوادم يديرها متطوِّعون تتيح لك الاتصال بها مجَّانًا وتحسِّن خصوصيتك وأمنك في الإنترنت. ويمكن للأفراد والمؤسسات مشاركة المعلومات عبرها باستخدام «خدمات .onion الخفية»، وذلك دون نهك خصوصيتهم. فكون اتصالات تور صعبة الحظر والتتبع يجعل تور أداةً فعَّالةً لتجاوز الرقابة.

[:octicons-home-16:](https://www.torproject.org){ .card-link title=Homepage }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://tb-manual.torproject.org/){ .card-link title=Documentation}
[:octicons-code-16:](https://gitlab.torproject.org/tpo/core/tor){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=Contribute }

يعمل تور عن طريق توجيه اتصالاتك عبر خوادم المتطوِّعين، وذلك بدلًا من الاتصال بالموقع الذي تريد مباشرةً. يلبِّس هذا أصل الاتصال، وليس بوسع أي خادم في سبيل الاتصال رؤيته من بدايته لمقصده، مما يعني أن حتى الخوادم المستخدمة للاتصال لا تنتهك مجهوليتك.

[نظرة عامة شاملة عن تور :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button}

## الاتصال بتور

!!! tip

    Before connecting to Tor, please ensure you've read our [overview](advanced/tor-overview.md) on what Tor is and how to connect to it safely. We often recommend connecting to Tor through a trusted [VPN provider](vpn.md), but you have to do so **properly** to avoid decreasing your anonymity.

عندك الكثير من السُّبُل للتتَّصل بشبكة تور من جهازك، وأشيعها **متصفِّح تور**، وهو تشعُّب من فيرفكس مصمَّم للتصفُّح المستور، ويُتاح في أجهزة سطح المكتب ونظام أندرويد.

Some of these apps are better than others, and again making a determination comes down to your threat model. If you are a casual Tor user who is not worried about your ISP collecting evidence against you, using apps like [Orbot](#orbot) or mobile browser apps to access the Tor network is probably fine. Increasing the number of people who use Tor on an everyday basis helps reduce the bad stigma of Tor, and lowers the quality of "lists of Tor users" that ISPs and governments may compile.

If more complete anonymity is paramount to your situation, you should **only** be using the desktop Tor Browser client, ideally in a [Whonix](desktop.md#whonix) + [Qubes](desktop.md#qubes-os) configuration. Mobile browsers are less common on Tor (and more fingerprintable as a result), and other configurations are not as rigorously tested against deanonymization.

### متصفِّح تور

!!! recommendation

    ![Tor Browser logo](assets/img/browsers/tor.svg){ align=left }
    
    **متصفِّح تور** خير خيار إن أردت المجهولية، فهو يمكِّنك من الاتصال بشبكة تور وجسورها، وفيه إعدادات مبدئية تُضبط حسب مستوى الأمن: *قياسي* و*أأمن* و*أشدُّ أمن*.
    
    [:octicons-home-16: Homepage](https://www.torproject.org){ .md-button .md-button--primary }
    [:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
    [:octicons-info-16:](https://tb-manual.torproject.org/){ .card-link title=Documentation }
    [:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/tor-browser){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
        - [:simple-android: Android](https://www.torproject.org/download/#android)
        - [:simple-windows11: Windows](https://www.torproject.org/download/)
        - [:simple-apple: macOS](https://www.torproject.org/download/)
        - [:simple-linux: Linux](https://www.torproject.org/download/)

!!! خطر

    لا تثبِّت أيَّ إضافات في متصفِّح تور **أبدًا**، ولا تحرِّر إعدادات ‹about:config›، ويشمل ذلك ما نقترحه في فيرفكس. تميِّزك الإضافات والإعدادات المختلفة عن البقية في شبكة تور، وهذه يسهِّل تبصيم [fingerprint](https://support.torproject.org/glossary/browser-fingerprinting) متصفِّحك.

صمِّم متصفِّح تور لمكافحة التبصيم، أو كشف هويَّتك حسب ضبط متصفِّحك. وزبدة القول أنه عليك **ألا** تعدِّل المتصفِّح خلا [مستويات الأمن](https://tb-manual.torproject.org/security-settings/) المبدئية.

In addition to installing Tor Browser on your computer directly, there are also operating systems designed specifically to connect to the Tor network such as [Whonix](desktop.md#whonix) on [Qubes OS](desktop.md#qubes-os), which provide even greater security and protections than the standard Tor Browser alone.

### أُربوت

!!! recommendation

    ![Orbot logo](assets/img/self-contained-networks/orbot.svg){ align=left }
    
    **أربوت** هو شبكة تور افتراضية خاصة للأجهزة الذكية، وما يفعله هو توجيه اتصالاتك من أيِّ تطبيق عبر شبكة تور.
    
    [:octicons-home-16: الصفحة الرئيسة](https://orbot.app/){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://orbot.app/privacy-policy){ .card-link title="سياسة الخصوصية" }
    [:octicons-info-16:](https://orbot.app/faqs){ .card-link title=التوثيق}
    [:octicons-code-16:](https://orbot.app/code){ .card-link title="رمز المصدر" }
    [:octicons-heart-16:](https://orbot.app/donate){ .card-link title=ساهم }
    
    ??? التنزيلات
    
        - [:simple-googleplay: متجر بلاي](https://play.google.com/store/apps/details?id=org.torproject.android)
        - [:simple-appstore: آب ستور](https://apps.apple.com/us/app/orbot/id1609461599)
        - [:simple-github: جت‌هب](https://github.com/guardianproject/orbot/releases)

We previously recommended enabling the *Isolate Destination Address* preference in Orbot settings. While this setting can theoretically improve privacy by enforcing the use of a different circuit for each IP address you connect to, it doesn't provide a practical advantage for most applications (especially web browsing), can come with a significant performance penalty, and increases the load on the Tor network. We no longer recommend adjusting this setting from its default value unless you know you need to.[^1]

!!! فائدة «فوائد لنظام أندرويد»

    بإمكان أربوت التوسُّط لتطبيقات معيَّنة حال دعمها توسُّط SOCKS أو HTTP. ويستطيع أيضا توسيط كلِّ اتصالات شبكتك باستخدام شبكة افتراضية خاصَّة [VpnService](https://developer.android.com/reference/android/net/VpnService)، ولك استخدامه مع مفتاح أيقاف الشبكات الافتراضية في :gear: **الإعدادات** ← **الشبكة والإنترنت** ← **الشبكات الافتراضية الخاصة** ← :gear: ← **امنع الاتصالات دون شبكة افتراضية خاصَّة**.
    
    غالبًا ما تجد إصدار أربوت قديمًا في مستودع [إف-درويد](https://guardianproject.info/fdroid) لمشروع جارديَن [ومتجر بلاي](https://play.google.com/store/apps/details?id=org.torproject.android)، فربما من الأفضل أن تنزِّله من [مستودع جت‌هب](https://github.com/guardianproject/orbot/releases) مباشرةً.
    
    كلُّ الإصدارات وُقِّع عليها بنفس التوقيع، لذلك تتوافق.

### Onion Browser

!!! recommendation

    ![Onion Browser logo](assets/img/self-contained-networks/onion_browser.svg){ align=right }
    
    **Onion Browser** is an open-source browser that lets you browse the web anonymously over the Tor network on iOS devices and is endorsed by the [Tor Project](https://support.torproject.org/glossary/onion-browser/).
    
    [:octicons-home-16: Homepage](https://onionbrowser.com){ .md-button .md-button--primary }
    [:octicons-eye-16:](https://onionbrowser.com/privacy-policy){ .card-link title="Privacy Policy" }
    [:octicons-info-16:](https://onionbrowser.com/faqs){ .card-link title=Documentation}
    [:octicons-code-16:](https://github.com/OnionBrowser/OnionBrowser){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://onionbrowser.com/donate){ .card-link title=Contribute }
    
    ??? downloads
    
        - [:simple-appstore: App Store](https://apps.apple.com/app/id519296448)

## المرحِّلات والجسور

### سنوفليك

!!! recommendation

    ![Snowflake logo](assets/img/browsers/snowflake.svg#only-light){ align=left }
    ![Snowflake logo](assets/img/browsers/snowflake-dark.svg#only-dark){ align=left }
    
    يتيح لك **سنوفليك** أن تساهم بشيء من حيِّز نطاقك في مشروع تور، ويكون ذلك عبر تشغيل «وسيط سنوفليك» ضمن متصفِّحك.
    
    يستطيع من يخضع للرقابة أن يستعمل وسطاء سنوفليك ليتَّصل بشبكة تور. ييسِّر سنوفليك المساهمة في شبكة تور، فلا تحتاج لمعلومات تقنية لتشغِّل مرحِّل تور أو جسرًا له.
    
    [:octicons-home-16: Homepage](https://snowflake.torproject.org/){ .md-button .md-button--primary }
    [:octicons-info-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/Technical%20Overview){ .card-link title=Documentation}
    [:octicons-code-16:](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake){ .card-link title="Source Code" }
    [:octicons-heart-16:](https://donate.torproject.org/){ .card-link title=Contribute }

You can enable Snowflake in your browser by opening it in another tab and turning the switch on. You can leave it running in the background while you browse to contribute your connection. We don't recommend installing Snowflake as a browser extension; adding third-party extensions can increase your attack surface.

[Run Snowflake in your Browser :material-arrow-right-drop-circle:](https://snowflake.torproject.org/embed.html ""){.md-button}

لا يفيد سنوفليك في تحسين خصوصيتك أبدًا، وليس سبيلًا لاتصال بشبكة تور داخل متصفِّحك. ولكن إن كان اتصالك بالإنترنت لا يخضع لرقابة فتخيَّر تشغيله لتعين من يستعمل شبكات تخضع لها في تحسين خصوصيتهم. ولا تقلق حيال أيِّ صفحات يزورها من يستخدم وسيطك، ﻷن عنوان IP لهم يطابق ذاك التابع لعقدة مخرج تور، لا عقدتك.

إن تشغيل وسيط سنوفليك ليس منذرًا بالخطر، بل أقلُّ خطرًا من تشغيل مرحِّل تور أو جسر له، وهذا ليس بذاك الخطر أصلًا. ولكنه يوسِّط الاتصالات عبر شبكتك، ولعلَّ لهذا تبعات، خاصَّةً إن كانت شبكتك محدودةً. عليك تمعُّن [سبيل عمل سنوفليك](https://gitlab.torproject.org/tpo/anti-censorship/pluggable-transports/snowflake/-/wikis/home) قبل أن تقرِّر تشغيل وسيط.

[^1]: The `IsolateDestAddr` setting is discussed on the [Tor mailing list](https://lists.torproject.org/pipermail/tor-talk/2012-May/024403.html) and [Whonix's Stream Isolation documentation](https://www.whonix.org/wiki/Stream_Isolation), where both projects suggest that it is usually not a good approach for most people.
