---
title: Uwierzytelnianie wieloskładnikowe
icon: material/two-factor-authentication
description: Uwierzytelnianie wieloskładnikowe to kluczowy mechanizm bezpieczeństwa chroniący konta internetowe, choć jedne metody są silniejsze od drugich.
---

**Uwierzytelnianie wieloskładnikowe** (**MFA**) to mechanizm bezpieczeństwa, który wymaga dodatkowych kroków poza podaniem nazwy użytkownika (lub adresu e-mail) i hasła. Najczęstszą metodą są jednorazowe kody ograniczone czasowo, które otrzymuje się SMS-em lub z aplikacji.

Zazwyczaj, jeśli haker (lub przeciwnik) odgadnie hasło, uzyskuje dostęp do konta, do którego to hasło należy. Konto zabezpieczone MFA wymusza, aby atakujący posiadał zarówno hasło (coś, co *znasz*), jak i Twoje urządzenie (coś, co *masz*), np. telefon.

Metody MFA różnią się poziomem bezpieczeństwa, ale opierają się na założeniu, że im trudniej atakującemu uzyskać dostęp do użytej metody MFA, tym lepiej. Przykłady metod MFA (od najsłabszych do najsilniejszych) obejmują SMS, kody e-mail, powiadomienia push w aplikacji, TOTP, Yubico OTP i FIDO.

## Porównanie metod MFA

### MFA przez SMS lub e-mail

Otrzymywanie kodów OTP przez SMS lub e-mail to jedna ze słabszych metod zabezpieczenia kont za pomocą MFA. Uzyskanie kodu e-mailem lub SMS-em osłabia ideę „czegoś, co *masz*”, ponieważ istnieje wiele sposobów, w jakie atakujący może [przejąć Twój numer telefonu](https://en.wikipedia.org/wiki/SIM_swap_scam) lub uzyskać dostęp do skrzynki e-mail bez fizycznego dostępu do któregokolwiek z Twoich urządzeń. Jeśli nieuprawniona osoba uzyskałaby dostęp do e-maila, mogłaby wykorzystać go zarówno do zresetowania hasła, jak i do odebrania kodu uwierzytelniającego, co dawałoby jej pełny dostęp do konta.

### Powiadomienia push

MFA przez powiadomienia push przyjmuje formę wiadomości wysyłanej do aplikacji na telefonie z prośbą o potwierdzenie nowego logowania do konta. Ta metoda jest o wiele lepsza niż przez SMS czy e-mail, ponieważ atakujący zwykle nie będzie w stanie otrzymać tych powiadomień bez uprzednio zalogowanego urządzenia, co oznacza konieczność wcześniejszego przejęcia jednego z pozostałych urządzeń.

Wszyscy popełniamy błędy i istnieje ryzyko przypadkowego zaakceptowania próby logowania. Autoryzacje logowania przez powiadomienia push są zwykle wysyłane jednocześnie na *wszystkie* Twoje urządzenia, co zwiększa dostępność kodu MFA, jeśli posiadasz wiele urządzeń.

Bezpieczeństwo MFA opartego na powiadomieniach push zależy zarówno od jakości aplikacji, komponentu serwerowego, jak i od wiarygodności dewelopera ją tworzącego. Instalacja aplikacji może także wymagać przyznania inwazyjnych uprawnień, które dają dostęp do innych danych na urządzeniu. Ponadto pojedyncza aplikacja wymusza posiadanie odrębnej aplikacji dla każdej usługi — aplikacja ta może nie wymagać hasła do uruchomienia, w przeciwieństwie do dobrej aplikacji generującej TOTP.

### Hasło jednorazowe ograniczone czasowo (TOTP)

TOTP jest jedną z najpowszechniejszych form MFA. Podczas konfiguracji TOTP zazwyczaj trzeba zeskanować [kod QR](https://en.wikipedia.org/wiki/QR_code), który ustanawia „[wspólny sekret](https://en.wikipedia.org/wiki/Shared_secret)” z usługą, z której zamierza się korzystać. Wspólny sekret jest przechowywany w danych aplikacji uwierzytelniającej i bywa czasem chroniony hasłem.

Kod ograniczony czasowo jest następnie generowany na podstawie wspólnego sekretu i bieżącego czasu. Ponieważ kod jest ważny tylko przez krótki czas, bez dostępu do wspólnego sekretu przeciwnik nie jest w stanie wygenerować nowych kodów.

Jeżeli posiadasz sprzętowy klucz bezpieczeństwa z obsługą TOTP (na przykład YubiKey z [Yubico Authenticator](https://yubico.com/products/yubico-authenticator)), zaleca się przechowywać tam swoje „wspólne sekrety”. Sprzęt taki jak YubiKey został zaprojektowany tak, by utrudniać wyodrębnienie i skopiowanie „wspólnego sekretu”. YubiKey nie jest też podłączony do Internetu, w przeciwieństwie do telefonu z aplikacją generującą TOTP.

W przeciwieńśtwie do [WebAuthn](#fido-fast-identity-online), TOTP nie chroni przed [phishingiem](https://pl.wikipedia.org/wiki/Phishing) ani atakami polegającymi na ponownym użyciu kodu. Jeśli przeciwnik uzyska od Ciebie ważny kod, może go użyć tyle razy, ile chce, dopóki nie wygaśnie (zazwyczaj po 60 sekundach).

Przeciwnik może stworzyć stronę podszywającą się pod oficjalną usługę w celu wyłudzenia nazwy użytkownika, hasła i aktualnego kodu TOTP. Jeśli następnie użyje przechwyconych danych, może zalogować się do prawdziwej usługi i przejąć konto.

Choć nie jest to rozwiązanie idealne, TOTP jest wystarczająco bezpieczny dla większości osób, a gdy [sprzętowe klucze bezpieczeństwa](../security-keys.md) nie są obsługiwane, [aplikacje uwierzytelniające](../multi-factor-authentication.md) wciąż stanowią dobrą opcję.

### Sprzętowe klucze bezpieczeństwa

YubiKey przechowuje dane na odpornym na manipulacje układzie półprzewodnikowym, do którego [nie da się nieinwazyjnie uzyskać dostępu](https://security.stackexchange.com/a/245772) bez kosztownego procesu i laboratorium kryminalistycznego.

Klucze te zwykle pełnią wiele funkcji i udostępniają kilka metod uwierzytelniania. Poniżej opisano najczęściej spotykane.

#### Yubico OTP

Yubico OTP to protokół uwierzytelniania zwykle implementowany w sprzętowych kluczach bezpieczeństwa. Po wybraniu Yubico OTP klucz wygeneruje identyfikator publiczny, identyfikator prywatny oraz klucz tajny, który następnie jest przesyłany na serwer Yubico OTP.

Podczas logowania na stronę wystarczy fizycznie dotknąć klucza bezpieczeństwa. Klucz emuluje klawiaturę i wpisuje jednorazowe hasło w pole hasła.

The service will then forward the one-time password to the Yubico OTP server for validation. A counter is incremented both on the key and Yubico's validation server. The OTP can only be used once, and when a successful authentication occurs, the counter is increased which prevents reuse of the OTP. Yubico provides a [detailed document](https://developers.yubico.com/OTP/OTPs_Explained.html) about the process.

<figure markdown>
  ![Yubico OTP](../assets/img/multi-factor-authentication/yubico-otp.png)
</figure>

There are some benefits and disadvantages to using Yubico OTP when compared to TOTP.

The Yubico validation server is a cloud based service, and you're placing trust in Yubico that they are storing data securely and not profiling you. The public ID associated with Yubico OTP is reused on every website and could be another avenue for third-parties to profile you. Like TOTP, Yubico OTP does not provide phishing resistance.

If your threat model requires you to have different identities on different websites, **do not** use Yubico OTP with the same hardware security key across those websites as public ID is unique to each security key.

#### FIDO (Fast IDentity Online)

[FIDO](https://en.wikipedia.org/wiki/FIDO_Alliance) includes a number of standards, first there was [U2F](https://en.wikipedia.org/wiki/Universal_2nd_Factor) and then later [FIDO2](https://en.wikipedia.org/wiki/FIDO2_Project) which includes the web standard [WebAuthn](https://en.wikipedia.org/wiki/WebAuthn).

U2F and FIDO2 refer to the [Client to Authenticator Protocol](https://en.wikipedia.org/wiki/Client_to_Authenticator_Protocol), which is the protocol between the security key and the computer, such as a laptop or phone. It complements WebAuthn which is the component used to authenticate with the website (the "Relying Party") you're trying to log in on.

WebAuthn is the most secure and private form of second factor authentication. While the authentication experience is similar to Yubico OTP, the key does not print out a one-time password and validate with a third-party server. Instead, it uses [public key cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography) for authentication.

<figure markdown>
  ![FIDO](../assets/img/multi-factor-authentication/fido.png)
</figure>

When you create an account, the public key is sent to the service, then when you log in, the service will require you to "sign" some data with your private key. The benefit of this is that no password data is ever stored by the service, so there is nothing for an adversary to steal.

This presentation discusses the history of password authentication, the pitfalls (such as password reuse), and the standards for FIDO2 and [WebAuthn](https://webauthn.guide):

- [How FIDO2 and WebAuthn Stop Account Takeovers](https://youtu.be/aMo4ZlWznao) <small>(YouTube)</small>

FIDO2 and WebAuthn have superior security and privacy properties when compared to any MFA methods.

Typically, for web services it is used with WebAuthn which is a part of the [W3C recommendations](https://en.wikipedia.org/wiki/World_Wide_Web_Consortium#W3C_recommendation_(REC)). It uses public key authentication and is more secure than shared secrets used in Yubico OTP and TOTP methods, as it includes the origin name (usually, the domain name) during authentication. Attestation is provided to protect you from phishing attacks, as it helps you to determine that you are using the authentic service and not a fake copy.

Unlike Yubico OTP, WebAuthn does not use any public ID, so the key is **not** identifiable across different websites. It also does not use any third-party cloud server for authentication. All communication is completed between the key and the website you are logging into. FIDO also uses a counter which is incremented upon use in order to prevent session reuse and cloned keys.

If a website or service supports WebAuthn for the authentication, it is highly recommended that you use it over any other form of MFA.

## Ogólne zalecenia

Przedstawiamy następujące ogólne zalecenia:

### Z której metody mam skorzystać?

When configuring your MFA method, keep in mind that it is only as secure as your weakest authentication method you use. This means it is important that you only use the best MFA method available. For instance, if you are already using TOTP, you should disable email and SMS MFA. If you are already using FIDO2/WebAuthn, you should not be using Yubico OTP or TOTP on your account.

### Kopie zapasowe

You should always have backups for your MFA method. Hardware security keys can get lost, stolen or simply stop working over time. It is recommended that you have a pair of hardware security keys with the same access to your accounts instead of just one.

When using TOTP with an authenticator app, be sure to back up your recovery keys or the app itself, or copy the "shared secrets" to another instance of the app on a different phone or to an encrypted container (e.g. [VeraCrypt](../encryption.md#veracrypt-disk)).

### Konfiguracja początkowa

When buying a security key, it is important that you change the default credentials, set up password protection for the key, and enable touch confirmation if your key supports it. Products such as the YubiKey have multiple interfaces with separate credentials for each one of them, so you should go over each interface and set up protection as well.

### E-mail i SMS

If you have to use email for MFA, make sure that the email account itself is secured with a proper MFA method.

If you use SMS MFA, use a carrier who will not switch your phone number to a new SIM card without account access, or use a dedicated VoIP number from a provider with similar security to avoid a [SIM swap attack](https://en.wikipedia.org/wiki/SIM_swap_scam).

[MFA tools we recommend](../multi-factor-authentication.md ""){.md-button}

## Więcej miejsc do ustawienia MFA

Beyond just securing your website logins, multifactor authentication can be used to secure your local logins, SSH keys or even password databases as well.

### macOS

macOS has [native support](https://support.apple.com/guide/deployment/intro-to-smart-card-integration-depd0b888248/web) for authentication with smart cards (PIV). If you have a smart card or a hardware security key that supports the PIV interface such as the YubiKey, we recommend that you follow your smart card or hardware security vendor's documentation and set up second factor authentication for your macOS computer.

Yubico have a guide [Using Your YubiKey as a Smart Card in macOS](https://support.yubico.com/hc/articles/360016649059) which can help you set up your YubiKey on macOS.

After your smart card/security key is set up, we recommend running this command in the Terminal:

```text
sudo defaults write /Library/Preferences/com.apple.loginwindow DisableFDEAutoLogin -bool YES
```

The command will prevent an adversary from bypassing MFA when the computer boots.

### Linux

<div class="admonition warning" markdown>
<p class="admonition-title">Ostrzeżenie</p>

If the hostname of your system changes (such as due to DHCP), you would be unable to login. It is vital that you set up a proper hostname for your computer before following this guide.

</div>

The `pam_u2f` module on Linux can provide two-factor authentication for logging in on most popular Linux distributions. If you have a hardware security key that supports U2F, you can set up MFA authentication for your login. Yubico has a guide [Ubuntu Linux Login Guide - U2F](https://support.yubico.com/hc/articles/360016649099-Ubuntu-Linux-Login-Guide-U2F) which should work on any distribution. The package manager commands—such as `apt-get`—and package names may however differ. This guide does **not** apply to Qubes OS.

### Qubes OS

Qubes OS has support for Challenge-Response authentication with YubiKeys. If you have a YubiKey with Challenge-Response authentication support, take a look at the Qubes OS [YubiKey documentation](https://qubes-os.org/doc/yubikey) if you want to set up MFA on Qubes OS.

### SSH

#### Hardware Security Keys

SSH MFA could be set up using multiple different authentication methods that are popular with hardware security keys. We recommend that you check out Yubico's [documentation](https://developers.yubico.com/SSH) on how to set this up.

#### TOTP

SSH MFA can also be set up using TOTP. DigitalOcean has provided a tutorial [How To Set Up Multi-Factor Authentication for SSH on Ubuntu 20.04](https://digitalocean.com/community/tutorials/how-to-set-up-multi-factor-authentication-for-ssh-on-ubuntu-20-04). Most things should be the same regardless of distribution, however the package manager commands—such as `apt-get`—and package names may differ.

### KeePass (and KeePassXC)

KeePass and KeePassXC databases can be secured using HOTP or Challenge-Response as a second-factor of authentication. Yubico has provided a document for KeePass [Using Your YubiKey with KeePass](https://support.yubico.com/hc/articles/360013779759-Using-Your-YubiKey-with-KeePass) and there is also one on the [KeePassXC](https://keepassxc.org/docs/#faq-yubikey-2fa) website.
