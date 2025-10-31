---
title: Przesyłanie obrazów
description: Przewodnik dla współtwórców tej strony na temat przesyłania obrazów w odpowiednim formacie i miejscu.
---

Jeśli wprowadzasz zmiany na tej stronie, które obejmują dodawanie nowych obrazów lub zastępowanie już istniejących, oto kilka ogólnych zaleceń:

## Obrazy

- **Preferowane** są obrazy w formacie SVG, ale jeśli nie są one dostępne, można użyć obrazów w formacie PNG. Ponadto preferujemy, aby obrazy przewodnie pochodziły z serwisu [Unsplash](https://unsplash.com) i były w formacie WebP.

Loga firm powinny być, o ile to możliwe, kwadratowe i mieć rozmiar co najmniej 200×200 pikseli, jeśli są to pliki PNG (grafiki niewektorowe).

## Optymalizacja obrazów

### PNG

Użyj narzędzia [OptiPNG](https://sourceforge.net/projects/optipng), aby zoptymalizować obrazy w formacie PNG:

```bash
optipng -o7 file.png
```

### SVG

#### Inkscape

Użyj narzędzia [Scour](https://github.com/scour-project/scour), aby zoptymalizować pliki SVG.

W programie Inkscape:

1. Plik > Zapisz jako...
2. Ustaw typ: Zoptymalizowany SVG (*.svg)

W zakładce **Opcje**:

- Ustaw opcję **Liczba cyfr znaczących dla współrzędnych** na wartość **5**
- [x] Włącz opcję **Skróć wartości kolorów**
- [x] Włącz opcję **Konwertuj atrybuty CSS na atrybuty XML**
- [x] Włącz opcję **Spłaszcz grupy**
- [x] Włącz opcję **Utwórz grupy dla podobnych atrybutów**
- [ ] Wyłącz opcję **Zachowaj dane edytora**
- [ ] Wyłącz opcję **Zachowaj nieużywane definicje**
- [x] Włącz opcję **Zastosuj obejścia błędów renderowania**

W zakładce **Zapis w formacie SVG** w sekcji **Opcje dokumentu**:

- [ ] Wyłącz opcję **Usuń deklarację XML**
- [x] Włącz opcję **Usuń metadane**
- [x] Włącz opcję **Usuń komentarze**
- [x] Włącz opcję **Osadź obrazy rastrowe**
- [x] Włącz opcję **Włącz skalowanie viewbox**

W zakładce **Zapis w formacie SVG** w sekcji **Formatowanie kodu**:

- [ ] Wyłącz opcję **Sformatuj dane wyjściowe za pomocą wcięć i znaków końca linii**
- **Znaki wcięć** > Wybierz **Spacja**
- **Głębokości wcięć** > **1**
- [ ] Wyłącz opcję **Wytnij atrybut "xml:space" z głównego elementu SVG**

W zakładce **IDs**:

- [x] Włącz opcję **Usuń nieużywane identyfikatory (ID)**
- [ ] Wyłącz opcję **Skróć identyfikatory (ID)**
- **Poprzedź skrócone identyfikatory (ID) przedrostkiem** > `pozostaw puste`
- [x] Włącz opcję **Zachowaj ręcznie utworzone identyfikatory (ID), które nie kończą się cyfrą**
- **Zachowaj następujące identyfikatory (ID)** > `pozostaw puste`
- **Zachowaj identyfikatory (ID) zaczynające się od** > `pozostaw puste`

#### Wiersz poleceń (CLI)

To samo można osiągnąć za pomocą polecenia [Scour](https://github.com/scour-project/scour):

```bash
scour --set-precision=5 \
      --create-groups \
      --renderer-workaround \
      --remove-descriptive-elements \
      --enable-comment-stripping \
      --enable-viewboxing \
      --indent=space \
      --nindent=1 \
      --no-line-breaks \
      --enable-id-stripping \
      --protect-ids-noninkscape \
      input.svg output.svg
```

### WebP

Użyj polecenia [`cwebp`](https://developers.google.com/speed/webp/docs/using), aby przekonwertować pliki graficzne PNG lub JPEG do formatu WebP:

```bash
cwebp -m 6 plik_wejściowy -o plik_wyjściowy.webp
```
