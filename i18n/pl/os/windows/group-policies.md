---
title: Group Policy Settings
description: A quick guide to configuring Group Policy to make Windows a bit more privacy respecting.
---

Outside modifying the registry itself, the **Local Group Policy Editor** is the most powerful way to change many aspects of your system without installing third-party tools. Changing these settings requires [Pro Edition](index.md#windows-editions) or better.

These settings should be set on a brand-new installation of Windows. Setting them on your existing installation should work, but may introduce unpredictable behavior and is done at your own risk.

All of these settings have an explanation attached to them in the Group Policy editor which explains exactly what they do, usually in great detail. Please pay attention to those descriptions as you make changes, so you know exactly what we are recommending here. We've also explained some of our choices below whenever the explanation included with Windows is inadequate.

## Szablony administracyjne

You can find these settings by opening `gpedit.msc` and navigating to **Local Computer Policy** > **Computer Configuration** > **Administrative Templates** in the left sidebar. The headers on this page correspond to folders/subfolders within Administrative Templates, and the bullet points correspond to individual policies.

To change any group policy, double click it and select Enabled or Disabled at the top of the window that appears depending on the recommendations below. Some group policies have additional settings that can be configured, and if that's the case the appropriate settings are noted below as well.

### System

#### Device Guard

- Włącz zabezpieczenia oparte na wirtualizacji: **Włączone**
  - Wybierz poziom zabezpieczeń platformy: **Bezpieczny rozruch i ochrona DMA**
  - Konfiguracja funkcji Bezpieczne uruchomienie: **Włączone**

#### Zarządzanie komunikacją internetową

- Wyłącz Program poprawy jakości obsługi klienta systemu Windows: **Włączone**
- Wyłącz funkcję Raportowanie błędów systemu Windows: **Włączone**
- Wyłącz Program poprawy jakości obsługi klienta w programie Windows Messenger: **Włączone**

Note that disabling the Windows Customer Experience Improvement Program also disables some other tracking features that can be individually controlled with Group Policy as well. We don't list them all here or disable them because this setting covers that.

#### Zasady systemu operacyjnego

- Zezwalaj na historię schowka: **Wyłączone**
- Zezwalaj na synchronizację schowka między urządzeniami: **Wyłączone**
- Włącza kanał aktywności: **Wyłączone**
- Zezwalaj na publikowanie aktywności użytkownika: **Wyłączone**
- Zezwalaj na przekazywanie działań użytkownika: **Wyłączone**

#### Profile użytkowników

- Wyłącz identyfikator treści reklamowych: **Włączone**

### Składniki systemu Windows

#### Zasady funkcji Autoodtwarzanie

AutoRun and AutoPlay are features which allow Windows to run a script or perform some other task when a device is connected, sometimes avoiding security measures that involve user consent. This could allow untrusted devices to run malicious code without your knowledge. It's a security best practice to disable these features, and simply open files on your external disks manually.

- Wyłącz funkcję Autoodtwarzanie: **Włączone**
- Wyłącz funkcję Autoodtwarzanie dla urządzeń niezawierających woluminów: **Włączone**
- Ustaw domyślne zachowanie autouruchamiania: **Włączone**
  - Domyślne zachowanie autouruchamiania: **Nie wykonuj żadnych poleceń autouruchamiania**

#### Szyfrowanie dysków funkcją BitLocker

You may wish to re-encrypt your operating system drive after changing these settings.

- Wybierz metodę szyfrowania dysku i siłę szyfrowania (Windows Vista, Windows Server 2008, Windows 7, Windows Server 2008 R2): **Włączone**
  - Wybierz metodę szyfrowania: **AES 256 bitów**

Setting the cipher strength for the Windows 7 policy still applies that strength to newer versions of Windows.

##### Dyski z systemem operacyjnym

- Wymagaj dodatkowego uwierzytelniania przy uruchamianiu: **Włączone**
- Zezwalaj na używanie rozszerzonych numerów PIN przy uruchamianiu: **Włączone**

Despite the names of these policies, this doesn't _require_ you to do anything by default, but it will unlock the _option_ to have a more complex setup (such as requiring a PIN at startup in addition to the TPM) in the BitLocker setup wizard.

#### Zawartość chmury

- Wyłączenie zawartości zoptymalizowanej pod kątem chmury: **Włączone**
- Wyłączenie zawartości stanu konta klienta w chmurze: **Włączone**
- Nie pokazuj porad dotyczących systemu Windows: **Włączone**
- Wyłącz funkcje użytkownika firmy Microsoft: **Włączone**

#### Interfejs użytkownika do obsługi poświadczeń

- Wymagaj ścieżki zaufanej do wprowadzania poświadczeń: **Włączone**
- Wyłącz możliwość używania pytań zabezpieczeń dla kont lokalnych: **Włączone**

#### Zbieranie danych i kompilacje w wersji Preview

- Zezwalaj na dane diagnostyczne: **Włączone**
  - Opcje: **Wysyłaj wymagane dane diagnostyczne** (w wersji Pro); lub
  - Options: **Diagnostic data off** (Enterprise or Education Edition)
- Ogranicz zbieranie dzienników diagnostycznych: **Włączone**
- Ogranicz zbieranie zrzutów: **Włączone**
- Ogranicz opcjonalne dane diagnostyczne dla usługi Desktop Analytics: **Włączone**
  - Opcje: **Wyłącz kolekcję usługi Desktop Analytics**
- Nie pokazuj powiadomień o opiniach: **Włączone**

#### Eksplorator plików

- Pokaż pliki na podstawie Twojego konta i aktywności dostawcy w chmurze: **Włączone**

#### MDM

- Wyłącz rejestrację w usłudze MDM: **Włączone**

#### OneDrive

- Domyślnie zapisuj dokumenty w usłudze OneDrive: **Wyłączone**
- Uniemożliwiaj aplikacji OneDrive generowanie ruchu sieciowego, dopóki użytkownik nie zaloguje się do usługi OneDrive: **Włączone**
- Nie zezwalaj na używanie usługi OneDrive na potrzeby przechowywania plików: **Włączone**

This last setting disables OneDrive on your system; make sure to change it to **Disabled** if you use OneDrive.

#### Push To Install

- Wyłącz usługę Push To Install: **Włączone**

#### Wyszukaj

- Zezwalaj na Cortanę: **Wyłączone**
- Nie wyszukuj w sieci Web ani nie wyświetlaj wyników z sieci Web w funkcji wyszukiwania: **Włączone**
- Określ, jakie informacje mają być udostępniane w funkcji wyszukiwania: **Włączone**
  - Typ informacji: **Informacje anonimowe**

#### Synchronizuj ustawienia

- Nie synchronizuj: **Włączone**

#### Wprowadzanie tekstu

- Ulepsz rozpoznawanie pisma odręcznego i wpisywania: **Wyłączone**

#### Raportowanie błędów systemu Windows

- Nie wysyłaj dodatkowych danych: **Włączone**
- Zgoda > Konfiguruj domyślne ustawienia zgody: **Włączone**
  - Poziom zgody: **Zawsze pytaj przed wysłaniem danych**
