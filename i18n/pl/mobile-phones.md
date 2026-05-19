---
title: Telefony komórkowe
icon: material/cellphone-check
description: Te urządzenia mobilne zapewniają najlepszą obsługę zabezpieczeń sprzętowych dla niestandardowych systemów operacyjnych Android.
cover: android.webp
schema:
  - "@context": http://schema.org
    "@type": WebPage
    name: Zalecenia dotyczące telefonów komórkowych
    url: "./"
  - "@context": http://schema.org
    "@type": Produkt
    name: Pixel
    brand:
      "@type": Marka
      name: Google
    image: /assets/img/android/google-pixel.png
    sameAs: https://pl.wikipedia.org/wiki/Google_Pixel
    review:
      "@type": Recenzja
      author:
        "@type": Organizacja
        name: Privacy Guides
robots: nofollow, max-snippet:-1, max-image-preview:large
---

<small>Chroni przed następującymi zagrożeniami:</small>

- [:material-target-account: Ataki ukierunkowane](basics/common-threats.md#attacks-against-specific-individuals){ .pg-red }
- [:material-bug-outline: Ataki pasywne](basics/common-threats.md#security-and-privacy){ .pg-orange }

Większość **telefonów komórkowych** otrzymuje krótki albo ograniczony okres aktualizacji zabezpieczeń od producentów; po osiągnięciu okresu zakończenia wsparca przez te urządzenia, **nie mogą** zostac uznane za zabezpieczone, ponieważ nie otrzymują one już nowych aktualizacji zabezpieczeń oprogramowania i sterowników.

Wymienione tutaj urządzenia mobilne, zapewniają długi okres gwarantowanych aktualizacji zabezpieczeń i pozwalają na zainstalowanie    niestandardowego systemu operacyjnego bez naruszenia modelu bezpieczeństwa Androida.

[Zalecane dystrybucje Androida :material-arrow-right-drop-circle:](android/distributions.md){ .md-button .md-button--primary } [Szczegóły dotyczące bezpieczeństwa systemu Android :material-arrow-right-drop-circle:](os/android-overview.md#security-protections){ .md-button }

<div class="admonition warning" markdown>
<p class="admonition-title">Ostrzeżenie</p>

Urządzenia z zakończonym okresem wsparcia (takie jak urządzenia z "rozszerzonym wsparciem" dla GrapheneOS) nie posiadają pełnych poprawek bezpieczeństwa (aktualizacji oprogramowania), ponieważ ich producenci przestali je wspierać. Te urządzenia nie mogą być uznawane za w pełni bezpieczne niezależnie od zainstalowanego oprogramowania.

</div>

## Ogólne porady dotyczące zakupu

Kupując urządzenie mobilne, zalecamy zakup możliwie najnowszego modelu. Systemy oraz oprogramowanie sprzętowe urządzeń mobilnych są wspierane tylko przez ograniczony czas, więc kupno nowego urządzenia wydłuża jego żywotność, maksymalnie jak jest to możliwe.

Unikaj kupowania urządzeń od operatorów sieci komórkowych. Często mają one **zablokowany program rozruchowy** i nie obsługują [odblokowania OEM](https://source.android.com/devices/bootloader/locking_unlocking). Te warianty urządzeń uniemożliwią Ci zainstalowanie jakiejkolwiek alternatywnej dystrybucji Androida.

Zachowaj szczególną **ostrożność** w przypadku kupowania używanych urządzeń z internetowych platform handlowych. Zawsze sprawdzaj reputację sprzedawcy. Jeśli urządzenie zostało skradzione, istnieje możliwość, że zostało wprowadzone do [bazy danych IMEI](https://gsma.com/get-involved/working-groups/terminal-steering-group/imei-database). Istnieje również ryzyko powiązania Cię z aktywnością poprzedniego właściciela.

Oto jeszcze parę wskazówek dotyczących urządzeń z Androidem i zgodności systemów operacyjnych:

- Nie kupuj urządzeń, które osiągnęły lub zbliżają się do końca okresu wsparcia; dodatkowe aktualizacje oprogramowania sprzętowego muszą być dostarczane przez producenta.
- Nie kupuj urządzeń z fabrycznie wgranym LineageOS lub /e/ OS lub jakiegokolwiek urządzenia z Androidem bez odpowiedniego wsparcia dla [Zweryfikowanego rozruchu]https://source.android.com/security/verifiedboot oraz aktualizacji oprogramowania. Urządzenia te nie mają również możliwości sprawdzenia, czy nie zostały naruszone.
- Krótko mówiąc, jeśli jakiegoś urządzenia nie ma na liście, prawdopodobnie jest ku temu dobry powód. Sprawdź nasze [forum](https://discuss.privacyguides.net), aby poznać szczegóły!

## Google Pixel

Telefony Google Pixel to **jedyne** urządzenia, których zakup zalecamy. Te urządzenia posiadają silniejsze zabezpieczenia sprzętowe niż jakiekolwiek inne urządzenia z Androidem obecnie dostępne na rynku dzięki odpowiedniemu wsparciu AVB dla alternatywnych systemów operacyjnych oraz układom bezpieczeństwa Google <a href="https://security.googleblog.com/2021/10/pixel-6-setting-new-standard-for-mobile.html">[Titan]</a> działającymi jako Secure Element.

<div class="admonition recommendation" markdown>

![Google Pixel 6](assets/img/android/google-pixel.png){ align=right }

Urządzenia **Google Pixel** są znane z dobrych zabezpieczeń i prawidłowo obsługują [Zweryfikowany rozruch](https://source.android.com/security/verifiedboot), nawet podczas instalowania niestandardowych systemów operacyjnych.

Począwszy od **Pixel 8** i **8 Pro**, urządzenia Pixel otrzymują co najmniej 7 lat gwarantowanych aktualizacji zabezpieczeń, zapewniając znacznie dłuższą żywotność w porównaniu do 2-5 lat, które zazwyczaj oferują konkurencyjni producenci.

[:material-shopping: Sklep](https://store.google.com/category/phones){ .md-button .md-button--primary }

</div>

### Bezpieczeństwo sprzętu

Secure Elements, takie jak Titan M2, są bardziej ograniczone niż Trusted Execution Environment (TEE) procesora używane w większości innych telefonów, ponieważ są używane tylko do przechowywania sekretów, poświadczania sprzętu i ograniczania szybkości, a nie do uruchamiania "zaufanych" programów. Telefony bez Secure Element muszą używać TEE do _wszystkich_ tych funkcji, co skutkuje większą powierzchnią ataku.

Telefony Google Pixel korzystają z systemu operacyjnego TEE o nazwie Trusty, który jest [open source](https://source.android.com/security/trusty#whyTrusty), w przeciwieństwie do wielu innych telefonów.

Seria Pixel 8 i nowsze obsługuje rozszerzenie ARM Memory Tagging Extension ([MTE](https://developer.arm.com/documentation/108035/0100/Introduction-to-the-Memory-Tagging-Extension)), sprzętowe ulepszenie zabezpieczeń, które drastycznie obniża prawdopodobieństwo wystąpienia nadużyć poprzez błędy związane z uszkodzeniem pamięci. Standardowy system operacyjny Pixel umożliwia włączenie MTE dla obsługiwanych aplikacji za pośrednictwem programu zaawansowanej ochrony Google lub opcji programisty, ale jego użyteczność jest dość ograniczona. [GrapheneOS](android/distributions.md#grapheneos), alternatywny system operacyjny Android, który polecamy, znacznie poprawia użyteczność i pokrycie MTE w jego implementacji tej funkcji.

### Zakup Google Pixel

Kilka dodatkowych wskazówek dotyczących zakupu Google Pixel:

- Jeśli szukasz okazji na urządzenie Pixel, sugerujemy zakup modelu "**a**", tuż po wydaniu kolejnego flagowca. Zniżki są zwykle dostępne, ponieważ Google będzie próbowało wyczyścić swoje magazyny.
- Rozważ opcje obniżania cen i promocje oferowane w sklepach fizycznych.
- Sprawdź serwisy społecznościowe w swoim kraju. Mogą Cię poinformować o dobrych przecenach.
- Google udostępnia listę pokazującą [cykl wsparcia](https://support.google.com/nexus/answer/4457705) dla każdego ze swoich urządzeń. Cenę za dzień dla urządzenia można obliczyć jako:
  <0>
  <1>
  <2>Koszt</2>
  <3>
  <2>Data zakończenia wsparcia</2>
  <4>-</4>
  <2>Data bieżąca</2>
  </3>
  </1>
  </0>
  Oznacza to, że im dłuższe użytkowanie urządzenia, tym niższy dzienny koszt.
- Jeśli Pixel jest niedostępny w twoim regionie, [NitroPhone](https://shop.nitrokey.com/shop) może być wysłany globalnie.

Instalacja GrapheneOS na telefonie Pixel jest łatwa dzięki ich [instalatorowi internetowemu](https://grapheneos.org/install/web). Jeśli nie czujesz się komfortowo, robiąc to samemu i jesteś skłonny wydać trochę więcej pieniędzy, sprawdź [NitroPhone](https://shop.nitrokey.com/shop), ponieważ są one fabrycznie wyposażone w GrapheneOS przez renomowaną firmę [Nitrokey](https://nitrokey.com/about).

## Kryteria

**Należy pamiętać, że nie jesteśmy powiązani z żadnym z polecanych przez nas projektów.** Oprócz [naszych standardowych kryteriów](about/criteria.md) opracowaliśmy jasny zestaw wymagań, które pozwalają nam formułować obiektywne zalecenia. Sugerujemy zapoznanie się z tą listą przed wyborem projektu oraz przeprowadzenie własnych badań, aby upewnić się, że jest to odpowiedni wybór dla Ciebie.

- Musi obsługiwać co najmniej jeden z naszych zalecanych niestandardowych systemów operacyjnych.
- Musi być obecnie sprzedawany jako nowy w sklepach.
- Musi otrzymywać aktualizacje zabezpieczeń przez co najmniej 5 lat.
- Musi mieć dedykowany układ secure element.
