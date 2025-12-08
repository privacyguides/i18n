---
meta_title: "Zalecane czaty AI: Prywatne alternatywy dla ChatGPT – Privacy Guides"
title: "Czat AI"
icon: material/assistant
description: W przeciwieństwie do ChatGPT od OpenAI i jego konkurentów z wielkich firm technologicznych, te narzędzia AI działają lokalnie, więc Twoje dane nigdy nie opuszczają komputera.
cover: ai-chatbots.webp
---

<small>Chroni przed następującymi zagrożeniami:</small>

- [:material-server-network: Dostawcy usług](basics/common-threats.md#privacy-from-service-providers){ .pg-teal }
- [:material-account-cash: Kapitalizm inwigilacji](basics/common-threats.md#surveillance-as-a-business-model){ .pg-brown }
- [:material-close-outline: Cenzura](basics/common-threats.md#avoiding-censorship){ .pg-blue-gray }

Korzystanie z **czatów AI** (lub też **czatów SI**), znanych również jako duże modele językowe (LLM), stało się coraz bardziej powszechne od czasu pojawienia się ChatGPT w 2022 roku. LLM-y mogą pomagać w lepszym pisaniu, ułatwiać zrozumienie nieznanych tematów lub odpowiadać na szeroki zakres pytań. Ich działanie polega na statystycznym przewidywaniu kolejnego słowa w odpowiedzi na podstawie ogromnej ilości danych pozyskanych z sieci.

## Obawy dotyczące prywatność związane z modelami LLM

Dane wykorzystywane do trenowania modeli sztucznej inteligencji obejmują jednak ogromne zbiory publicznie dostępnych informacji zebranych z Internetu, które mogą zawierać poufne dane, takie jak imiona, nazwiska czy adresy. Oprogramowanie sztucznej inteligencji działające w chmurze często [gromadzi dane wejściowe](https://openai.com/policies/row-privacy-policy) użytkownika, co oznacza, że Twoje rozmowy nie są dla nich prywatne. Praktyka ta zwiększa również ryzyko wycieków danych. Ponadto istnieje realna możliwość, że LLM ujawni prywatne informacje z Twoich czatów w przyszłych rozmowach z innymi użytkownikami.

Jeśli obawiasz się takich praktyk, możesz zrezygnować z używania sztucznej inteligencji albo skorzystać z [prawdziwie otwartych modeli](https://proton.me/blog/how-to-build-privacy-first-ai), które publicznie udostępniają i pozwalają zweryfikować zbiory danych użyte do treningu. Przykładem takiego modelu jest [OLMoE](https://allenai.org/blog/olmoe-an-open-small-and-state-of-the-art-mixture-of-experts-model-c258432d0514) opracowany przez [Ai2](https://allenai.org/open-data).

Alternatywnie można uruchamiać modele sztucznej inteligencji lokalnie, dzięki czemu dane nigdy nie opuszczają urządzenia i nie są udostępniane stronom trzecim. Modele lokalne stanowią zatem bardziej prywatną i bezpieczną alternatywę dla rozwiązań chmurowych i pozwalają na przekazywanie modelowi poufnych informacji bez obaw.

## Modele sztucznej inteligencji

### Sprzęt dla lokalnych modeli sztucznej inteligencji

Modele uruchamiane lokalnie są też dość przystępne. Mniejsze modele można uruchamiać z mniejszą prędkością, mając tylko 8 GB pamięci RAM. Najlepsze wrażenia zapewnia jednak bardziej wydajny sprzęt, np. dedykowana karta graficzna z odpowiednią ilością pamięci VRAM lub nowoczesny system z szybką pamięcią LPDDR5X.

LLM-y zwykle rozróżnia się według liczby parametrów — dla modeli open-source dostępnych dla użytkowników końcowych wartości te wahają się od około 1,3 mld do 405 mld parametrów. Na przykład modele o parametrach poniżej 6,7 mld parametrów nadają się głównie do podstawowych zadań, takich jak streszczenia tekstu, natomiast modele w przedziale 7–13 mld stanowią dobry kompromis między jakością a szybkością. Modele o zaawansowanych zdolnościach rozumowania mają zwykle około 70 mld parametrów.

Dla sprzętu konsumenckiego zwykle zaleca się używanie [modeli kwantyzowanych](https://huggingface.co/docs/optimum/en/concept_guides/quantization), które dają najlepszy balans między jakością modelu a wydajnością. Sprawdź poniższą tabelę, aby uzyskać bardziej szczegółowe informacje o typowych wymaganiach dla różnych rozmiarów modeli kwantyzowanych.

| Rozmiar modelu (liczba parametrów) | Minimalna pamięć RAM | Minimalny procesor / sprzęt                             |
| ----------------------------------------------------- | -------------------- | ------------------------------------------------------- |
| 7 mld                                                 | 8 GB                 | Nowoczesny procesor (z obsługą AVX2) |
| 13 mld                                                | 16 GB                | Nowoczesny procesor (z obsługą AVX2) |
| 70 mld                                                | 72 GB                | Karta graficzna z pamięcią VRAM                         |

Aby uruchomić sztuczną inteligencję lokalnie, potrzebujesz zarówno modelu sztucznej inteligencji, jak i klienta sztucznej inteligencji.

### Wybór modelu

Dostępnych jest wiele modeli na licencjach pozwalających na swobodne użycie. Platformą, która umożliwia przeglądanie, badanie i pobieranie modeli w popularnych formatach (np. [GGUF](https://huggingface.co/docs/hub/en/gguf)), jest [Hugging Face](https://huggingface.co/models). Firmy udostępniające dobre modele z otwartymi wagami to m.in. Mistral, Meta, Microsoft i Google. Jednak istnieje też wiele modeli tworzonych przez społeczność oraz modeli [dostrojonych](https://en.wikipedia.org/wiki/Fine-tuning_\(deep_learning\)). Jak wspomniano wcześniej, modele kwantyzowane zwykle oferują najlepszy kompromis jakości i wydajności dla sprzętu konsumenckiego.

Aby wybrać model odpowiedni dla Twoich potrzeb, warto śledzić rankingi i benchmarki. Najbardziej popularnym rankingiem społecznościowym jest [LM Arena](https://lmarena.ai). Z kolei [OpenLLM Leaderboard](https://huggingface.co/spaces/open-llm-leaderboard/open_llm_leaderboard) koncentruje się na wydajności modeli z otwartymi wagami w standardowych benchmarkach, takich jak [MMLU-Pro](https://arxiv.org/abs/2406.01574).  Istnieją też wyspecjalizowane benchmarki mierzące np. [inteligencję emocjonalną](https://eqbench.com), [„nieocenzurowaną ogólną inteligencję”](https://huggingface.co/spaces/DontPlanToEnd/UGI-Leaderboard) oraz [wiele innych](https://nebuly.com/blog/llm-leaderboards).

## Klienci czatu AI

| Cecha/funkcja                  | [Kobold.cpp](#koboldcpp)                                      | [Ollama](#ollama-cli)                                                         | [Llamafile](#llamafile)                                                                                                         |
| ------------------------------ | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| Obsługa GPU                    | :material-check:{ .pg-green } | :material-check:{ .pg-green } | :material-check:{ .pg-green }                                                   |
| Generowanie obrazów            | :material-check:{ .pg-green } | :material-close:{ .pg-red }   | :material-close:{ .pg-red }                                                     |
| Rozpoznawanie mowy             | :material-check:{ .pg-green } | :material-close:{ .pg-red }   | :material-close:{ .pg-red }                                                     |
| Automatyczne pobieranie modeli | :material-close:{ .pg-red }   | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange } Kilka dostępnych modeli                  |
| Niestandardowe parametry       | :material-check:{ .pg-green } | :material-close:{ .pg-red }   | :material-check:{ .pg-green }                                                   |
| Wieloplatformowość             | :material-check:{ .pg-green } | :material-check:{ .pg-green } | :material-alert-outline:{ .pg-orange } Ograniczenia rozmiaru w systemie Windows |

### Kobold.cpp

<div class="admonition recommendation" markdown>

![Logo Kobold.cpp](assets/img/ai-chat/kobold.png){align=right}

**Kobold.cpp** to klient sztucznej inteligencji uruchamiany lokalnie na komputerach z systemem Windows, Mac lub Linux. To doskonały wybór, jeśli zależy Ci na szerokich możliwościach dostosowywania i modyfikacji, na przykład w celu odgrywania ról.

Oprócz obsługi szerokiej gamy modeli tekstowych, Kobold.cpp obsługuje też generatory obrazów, takie jak [Stable Diffusion](https://stability.ai/stable-image), oraz narzędzia do automatycznego rozpoznawania mowy, np. [Whisper](https://github.com/ggerganov/whisper.cpp).

[:octicons-repo-16: Repozytorium](https://github.com/LostRuins/koboldcpp#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/LostRuins/koboldcpp/wiki){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/LostRuins/koboldcpp){ .card-link title="Kod źródłowy" }
[:octicons-lock-16:](https://github.com/LostRuins/koboldcpp/blob/2f3597c29abea8b6da28f21e714b6b24a5aca79b/SECURITY.md){ .card-link title="Polityka bezpieczeństwa" }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:fontawesome-brands-windows: Windows](https://github.com/LostRuins/koboldcpp/releases)
- [:simple-apple: macOS](https://github.com/LostRuins/koboldcpp/releases)
- [:simple-linux: Linux](https://github.com/LostRuins/koboldcpp/releases)

</details>

</div>

<div class="admonition info" markdown>
<p class="admonition-title">Problemy z kompatybilnością</p>

Kobold.cpp może nie działać na komputerach bez obsługi AVX/AVX2.

</div>

Kobold.cpp umożliwia modyfikowanie parametrów, takich jak temperatura modelu czy tzw. system prompt czatu. Pozwala także na utworzenie tunelu sieciowego, dzięki któremu do modeli sztucznej inteligencji można uzyskać dostęp z innych urządzeń, np. ze smartfona.

### Ollama (CLI)

<div class="admonition recommendation" markdown>

![Logo Ollama](assets/img/ai-chat/ollama.png){align=right}

**Ollama** to asystent AI działający z wiersza poleceń, dostępny na komputerach z systemem macOS, Linux i Windows. Ollama to świetny wybór, jeśli zależy Ci na kliencie, który jest łatwy w obsłudze, szeroko kompatybilny i szybki dzięki wykorzystaniu wnioskowania i innych technik. Nie wymaga też żadnej ręcznej konfiguracji.

Oprócz obsługi szerokiej gamy modeli tekstowych, Ollama obsługuje także modele [LLaVA](https://github.com/haotian-liu/LLaVA), oraz posiada eksperymentalne wsparcie dla [możliwości wizyjnych Llama](https://huggingface.co/blog/llama32#what-is-llama-32-vision) opracowanych przez Meta.

[:octicons-home-16: Strona główna](https://ollama.com){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/ollama/ollama#readme){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/ollama/ollama){ .card-link title="Kod źródłowy" }
[:octicons-lock-16:](https://github.com/ollama/ollama/blob/a14f76491d694b2f5a0dec6473514b7f93beeea0/SECURITY.md){ .card-link title="Polityka bezpieczeństwa" }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:fontawesome-brands-windows: Windows](https://ollama.com/download/windows)
- [:simple-apple: macOS](https://ollama.com/download/mac)
- [:simple-linux: Linux](https://ollama.com/download/linux)

</details>

</div>

Ollama upraszcza proces konfiguracji lokalnego czatu AI, automatycznie pobierając wybrany przez Ciebie model. Na przykład polecenie `ollama run llama3.2` automatycznie pobierze i uruchomi model Llama 3.2. Ponadto Ollama prowadzi własną [bibliotekę modeli](https://ollama.com/library), w której hostuje pliki różnych modeli sztucznej inteligencji. Dzięki temu modele są weryfikowane pod kątem wydajności i bezpieczeństwa, co eliminuje konieczność samodzielnego sprawdzania autentyczności plików modelu.

### Llamafile

<div class="admonition recommendation" markdown>

![Logo Llamafile](assets/img/ai-chat/llamafile.webp){align=right}

**Llamafile** to lekki, jednoplikowy program wykonywalny, który pozwala uruchamiać LLM lokalnie na własnym komputerze bez żadnej konfiguracji. Projekt jest [wspierany przez Mozillę](https://hacks.mozilla.org/2023/11/introducing-llamafile) i jest dostępny w systemach Linux, macOS i Windows.

Llamafile obsługuje również LLaVA. Jednak nie wspiera rozpoznawania mowy ani generowania obrazów.

[:octicons-repo-16: Repozytorium](https://github.com/Mozilla-Ocho/llamafile#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/Mozilla-Ocho/llamafile#quickstart){ .card-link title="Dokumentacja" }
[:octicons-code-16:](https://github.com/Mozilla-Ocho/llamafile){ .card-link title="Kod źródłowy" }
[:octicons-lock-16:](https://github.com/Mozilla-Ocho/llamafile#security){ .card-link title="Polityka bezpieczeństwa" }

<details class="downloads" markdown>
<summary>Pobierz</summary>

- [:fontawesome-brands-windows: Windows](https://github.com/Mozilla-Ocho/llamafile#quickstart)
- [:simple-apple: macOS](https://github.com/Mozilla-Ocho/llamafile#quickstart)
- [:simple-linux: Linux](https://github.com/Mozilla-Ocho/llamafile#quickstart)

</details>

</div>

Mozilla udostępniła llamafile tylko dla niektórych modeli Llama i Mistral, podczas gdy dostępnych jest niewiele wersji tworzonych przez zewnętrznych autorów. Ponadto system Windows ogranicza rozmiar plików `.exe` do 4 GB, podczas gdy większość modeli ma większy rozmiar.

Aby obejść te ograniczenia, możesz [wczytać zewnętrzne wagi](https://github.com/Mozilla-Ocho/llamafile#using-llamafile-with-external-weights).

## Bezpieczne pobieranie modeli

Jeśli korzystasz z klienta AI, który utrzymuje własną bibliotekę plików modelu (takiego jak [Ollama](#ollama-cli) czy [Llamafile](#llamafile)), pobieraj modele z tej biblioteki. Jednak jeśli chcesz pobrać modele, które nie znajdują się w ich bibliotece, albo korzystasz z klienta AI, który nie prowadzi własnej biblioteki (np. [Kobold.cpp](#koboldcpp)), musisz podjąć dodatkowe kroki, aby upewnić się, że pobierany model jest bezpieczny i autentyczny.

Zalecamy pobieranie plików modeli z serwisu Hugging Face, ponieważ oferuje on szereg funkcji umożliwiających sprawdzenie, czy pobrane pliki są autentyczne i bezpieczne w użyciu.

Aby sprawdzić autentyczność i bezpieczeństwo modelu, zwróć uwagę na:

- Karty modelu z przejrzystą dokumentacją
- Odznakę zweryfikowanej organizacji
- Opinie społeczności i statystyki użytkowania
- Odznakę „Safe” obok pliku modelu (tylko Hugging Face)
- Pasujące sumy kontrolne[^1]
  - Na Hugging Face skrót (hash) znajdziesz, klikając plik modelu i wybierając przycisk **Copy SHA256** znajdujący się pod nim. Należy porównać tę sumę kontrolną z tą z pobranego pliku modelu.

Pobrany model można uznać za ogólnie bezpieczny, jeśli spełnia wszystkie powyższe kryteria.

## Kryteria

Należy pamiętać, że nie jesteśmy powiązani z żadnym z polecanych przez nas projektów. Oprócz [naszych standardowych kryteriów](about/criteria.md) opracowaliśmy jasny zestaw wymagań, które pozwalają nam formułować obiektywne zalecenia. Sugerujemy zapoznanie się z tą listą przed wyborem projektu oraz przeprowadzenie własnych badań, aby upewnić się, że jest to odpowiedni wybór dla Ciebie.

### Minimalne wymagania

- Musi być open source.
- Nie może przesyłać danych osobowych, w tym danych z czatów.
- Musi być wieloplatformowy.
- Nie może wymagać GPU.
- Musi obsługiwać szybkie wnioskowanie oparte na GPU.
- Nie może wymagać połączenia z Internetem.

### Najlepszy scenariusz

Nasze kryteria „najlepszego scenariusza” określają, jak powinien wyglądać idealny projekt w tej kategorii. Nasze zalecenia nie muszą spełniać wszystkich tych warunków, jednak projekty, które spełniają więcej z nich, mogą być oceniane wyżej od pozostałych na stronie.

- Powinien być łatwy do pobrania i skonfigurowania, np. instalacja jednym kliknięciem.
- Powinien mieć wbudowaną opcję pobierania modeli.
- Użytkownik powinien mieć możliwość modyfikacji parametrów LLM, takich jak system prompt czy temperatura.

\*[LLaVA]: Large Language and Vision Assistant (wielomodalny model sztucznej inteligencji)
\*[LLM]: Duży model językowy (model sztucznej inteligencji, taki jak ChatGPT)
\*[LLMs]: Duże modele językowe (modele sztucznej inteligencji, takie jak ChatGPT)
\*[modele z otwartymi wagami]: Model sztucznej inteligencji, który każdy może pobrać i używać, jednak dane treningowe i/lub zastosowane algorytmy pozostają zastrzeżone.
\*[system prompt]: System prompt (z ang. instrukcja systemowa) to ogólne instrukcje przekazywane przez człowieka, które określają sposób działania modelu.
\*[temperatura]: Temperatura modelu to parametr służący do kontrolowania poziomu losowości i kreatywności generowanego tekstu.

[^1]: Suma kontrolna pliku to rodzaj odcisku palca chroniącego przed manipulacją. Deweloper zwykle udostępnia sumę kontrolną w osobnym pliku tekstowym lub na stronie pobierania. Zweryfikowanie, czy suma kontrolna pobranego pliku zgadza się z tą podaną przez dewelopera, pomaga upewnić się, że plik jest oryginalny i nie został zmodyfikowany w trakcie transferu. Możesz użyć poleceń takich jak `sha256sum` w systemach Linux i macOS albo `certutil -hashfile file SHA256` w systemie Windows, aby wygenerować sumę kontrolną pobranego pliku.
