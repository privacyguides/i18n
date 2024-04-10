---
meta_title: "Tor Browser and Network: Anonymous Web Browsing - Privacy Guides"
title: "متصفِّح تور"
icon: simple/torbrowser
description: Protect your internet browsing from prying eyes by using the Tor network, a secure network which circumvents censorship.
cover: tor.webp
schema:
  - 
    "@context": http://schema.org
    "@type": SoftwareApplication
    name: متصفِّح تور
    image: /assets/img/browsers/tor.svg
    url: https://torproject.org
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

**Tor** is a group of volunteer-operated servers that allows you to connect for free and improve your privacy and security on the Internet. ويمكن للأفراد والمؤسسات مشاركة المعلومات عبرها باستخدام «خدمات .onion الخفية»، وذلك دون نهك خصوصيتهم. فكون اتصالات تور صعبة الحظر والتتبع يجعل تور أداةً فعَّالةً لتجاوز الرقابة.

[نظرة عامة شاملة عن تور :material-arrow-right-drop-circle:](advanced/tor-overview.md ""){.md-button}

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Before connecting to Tor, please ensure you've read our [overview](advanced/tor-overview.md) on what Tor is and how to connect to it safely. We often recommend connecting to Tor through a trusted [VPN provider](vpn.md), but you have to do so **properly** to avoid decreasing your anonymity.

</div>

عندك الكثير من السُّبُل للتتَّصل بشبكة تور من جهازك، وأشيعها **متصفِّح تور**، وهو تشعُّب من فيرفكس مصمَّم للتصفُّح المستور، ويُتاح في أجهزة سطح المكتب ونظام أندرويد.

Some of these apps are better than others, and again making a determination comes down to your threat model. If you are a casual Tor user who is not worried about your ISP collecting evidence against you, using apps like [Orbot](#orbot) or mobile browser apps to access the Tor network is probably fine. Increasing the number of people who use Tor on an everyday basis helps reduce the bad stigma of Tor, and lowers the quality of "lists of Tor users" that ISPs and governments may compile.

If more complete anonymity is paramount to your situation, you should **only** be using the desktop Tor Browser client, ideally in a [Whonix](desktop.md#whonix) + [Qubes](desktop.md#qubes-os) configuration. Mobile browsers are less common on Tor (and more fingerprintable as a result), and other configurations are not as rigorously tested against deanonymization.

## متصفِّح تور

<div class="admonition recommendation" markdown>

![Tor Browser logo](assets/img/browsers/tor.svg){ align=left }

**متصفِّح تور** خير خيار إن أردت المجهولية، فهو يمكِّنك من الاتصال بشبكة تور وجسورها، وفيه إعدادات مبدئية تُضبط حسب مستوى الأمن: *قياسي* و*أأمن* و*أشدُّ أمن*.

[:octicons-home-16: Homepage](https://torproject.org){ .md-button .md-button--primary }
[:simple-torbrowser:](http://2gzyxa5ihm7nsggfxnu52rck2vv4rvmdlkiu3zzui5du4xyclen53wid.onion){ .card-link title="Onion Service" }
[:octicons-info-16:](https://tb-manual.torproject.org){ .card-link title=Documentation }
[:octicons-code-16:](https://gitlab.torproject.org/tpo/applications/tor-browser){ .card-link title="Source Code" }
[:octicons-heart-16:](https://donate.torproject.org){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.torbrowser)
- [:simple-android: Android](https://torproject.org/download/#android)
- [:simple-windows11: Windows](https://torproject.org/download)
- [:simple-apple: macOS](https://torproject.org/download)
- [:simple-linux: Linux](https://torproject.org/download)

</details>

</div>

<div class="admonition danger" markdown>
<p class="admonition-title">Danger</p>

لا تثبِّت أيَّ إضافات في متصفِّح تور **أبدًا**، ولا تحرِّر إعدادات ‹about:config›، ويشمل ذلك ما نقترحه في فيرفكس. تميِّزك الإضافات والإعدادات المختلفة عن البقية في شبكة تور، وهذه يسهِّل تبصيم [fingerprint](https://support.torproject.org/glossary/browser-fingerprinting) متصفِّحك.

</div>

صمِّم متصفِّح تور لمكافحة التبصيم، أو كشف هويَّتك حسب ضبط متصفِّحك. Therefore, it is imperative that you do **not** modify the browser beyond the default [security levels](https://tb-manual.torproject.org/security-settings).

In addition to installing Tor Browser on your computer directly, there are also operating systems designed specifically to connect to the Tor network such as [Whonix](desktop.md#whonix) on [Qubes OS](desktop.md#qubes-os), which provide even greater security and protections than the standard Tor Browser alone.

## أُربوت

<div class="admonition recommendation" markdown>

![Orbot logo](assets/img/self-contained-networks/orbot.svg){ align=left }

**أربوت** هو شبكة تور افتراضية خاصة للأجهزة الذكية، وما يفعله هو توجيه اتصالاتك من أيِّ تطبيق عبر شبكة تور.

[:octicons-home-16: Homepage](https://orbot.app){ .md-button .md-button--primary }
[:octicons-eye-16:](https://orbot.app/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://orbot.app/faqs){ .card-link title=Documentation}
[:octicons-code-16:](https://orbot.app/code){ .card-link title="Source Code" }
[:octicons-heart-16:](https://orbot.app/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-googleplay: Google Play](https://play.google.com/store/apps/details?id=org.torproject.android)
- [:simple-appstore: App Store](https://apps.apple.com/app/id1609461599)
- [:simple-github: GitHub](https://github.com/guardianproject/orbot/releases)

</details>

</div>

We previously recommended enabling the *Isolate Destination Address* preference in Orbot settings. While this setting can theoretically improve privacy by enforcing the use of a different circuit for each IP address you connect to, it doesn't provide a practical advantage for most applications (especially web browsing), can come with a significant performance penalty, and increases the load on the Tor network. We no longer recommend adjusting this setting from its default value unless you know you need to.[^1]

<div class="admonition tip" markdown>
<p class="admonition-title">Tips for Android</p>

بإمكان أربوت التوسُّط لتطبيقات معيَّنة حال دعمها توسُّط SOCKS أو HTTP. It can also proxy all your network connections using [VpnService](https://developer.android.com/reference/android/net/VpnService) and can be used with the VPN killswitch in :gear: **Settings** → **Network & internet** → **VPN** → :gear: → **Block connections without VPN**.

غالبًا ما تجد إصدار أربوت قديمًا في مستودع [إف-درويد](https://guardianproject.info/fdroid) لمشروع جارديَن [ومتجر بلاي](https://play.google.com/store/apps/details?id=org.torproject.android)، فربما من الأفضل أن تنزِّله من [مستودع جت‌هب](https://github.com/guardianproject/orbot/releases) مباشرةً.

كلُّ الإصدارات وُقِّع عليها بنفس التوقيع، لذلك تتوافق.

</div>

## Onion Browser

<div class="admonition recommendation" markdown>

![Onion Browser logo](assets/img/self-contained-networks/onion_browser.svg){ align=right }

**Onion Browser** is an open-source browser that lets you browse the web anonymously over the Tor network on iOS devices and is endorsed by the [Tor Project](https://support.torproject.org/glossary/onion-browser).

[:octicons-home-16: Homepage](https://onionbrowser.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://onionbrowser.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://onionbrowser.com/faqs){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/OnionBrowser/OnionBrowser){ .card-link title="Source Code" }
[:octicons-heart-16:](https://onionbrowser.com/donate){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>Downloads</summary>

- [:simple-appstore: App Store](https://apps.apple.com/app/id519296448)

</details>

</div>
