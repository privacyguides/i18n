---
meta_title: "How to Create Internet Accounts Privately - Privacy Guides"
title: "Account Creation"
icon: 'material/account-plus'
description: Creating accounts online is practically an internet necessity, take these steps to make sure you stay private.
---

Çoğu zaman insanlar düşünmeden hizmetlere kaydolurlar. Bu, herkesin konuştuğu yeni diziyi izleyebileceğiniz bir yayın hizmeti ya da en sevdiğiniz fast food restoranında indirim sağlayan bir hesap olabilir. Her ne için olursa olsun, şimdi ve daha sonrası için verileriniz üzerindeki etkilerini göz önünde bulundurmalısınız.

Kullandığınız her yeni hizmetle ilgili riskler vardır. Veri ihlalleri; müşteri bilgilerinin üçüncü taraflara ifşa edilmesi; kötü niyetli çalışanların verilere erişmesi; tüm bunlar bilgilerinizi dışarıya verirken göz önünde bulundurulması gereken olasılıklardır. Hizmete güvenebileceğinizden emin olmanız gerekir. Bu nedenle değerli verilerinizi olgun ve test edilmiş olanlar dışında herhangi bir yerde saklamanızı önermiyoruz. Bu genellikle uçtan uca şifreleme (E2EE) sağlayan ve kriptografik denetimden geçmiş hizmetler anlamına gelir. Denetim, ürünün deneyimsiz bir geliştiricinin neden olduğu göze çarpan güvenlik sorunları olmadan tasarlandığına dair güvenceyi artırır.

Bazı hizmetlerde hesapları silmek de zor olabilir. Bazen bir hesapla ilişkili [verilerin üzerine yazmak](account-deletion.md#overwriting-account-information) mümkün olabilir. Ancak diğer durumlarda hizmet, hesapta yapılan değişikliklerin tüm geçmişini saklar.

## Hizmet Koşulları & Gizlilik Politikası

ToS, hizmeti kullanırken uymayı kabul ettiğiniz kurallardır. Daha büyük hizmetlerde bu kurallar genellikle otomatik sistemler tarafından uygulanır. Bazen bu otomatik sistemler hata yapabilir. Örneğin, bir VPN veya VOIP numarası kullandığınız için bazı hizmetlerde hesabınız yasaklanabilir veya kilitlenebilir. Bu tür yasaklara itiraz etmek genellikle zordur ve her zaman başarılı olmayan otomatik bir süreci de içerir. Örnek olarak e-posta için Gmail'i kullanmanızı önermememizin nedenlerinden biri de budur. E-posta, kaydolduğunuz diğer hizmetlere erişim için çok önemlidir.

Gizlilik Politikası, hizmetin verilerinizi nasıl kullanacağını söyler, ve verilerinizin nasıl kullanılacağını anlamanız için okumaya değerdir. Bir şirket veya kuruluş yasal olarak politikada yer alan her şeye uymak zorunda olmayabilir (yargı yetkisine bağlı). Yerel yasalarınızın ne olduğu ve bir sağlayıcının neleri toplamasına izin verdiği konusunda fikir sahibi olmanızı tavsiye ederiz.

"Veri toplama", "veri analizi", "çerezler", "reklamlar" veya "3. taraf" hizmetler gibi belirli terimleri aramanızı öneririz. Bazen veri toplamayı veya verilerinizi paylaşmayı devre dışı bırakabilirsiniz, ancak en iyisi en başından gizliliğinize saygı duyan bir hizmet seçmektir.

Aynı zamanda şirkete veya kuruluşa kendi gizlilik politikalarına uyacaklarına dair güvendiğinizi unutmayın.

## Kimlik Doğrulama yöntemleri

Bir hesap oluşturmak için genellikle birden fazla yol olur, ve her birinin kendi avatajları ve dezavantajları vardır.

### E-posta ve şifre

Yeni bir hesap oluşturmanın en yaygın yolu e-posta adresi ve paroladır. Bu yöntemi kullanırken bir parola yöneticisi kullanmalı ve parolalarla ilgili [en iyi uygulamaları](passwords-overview.md)takip etmelisiniz.

<div class="admonition tip" markdown>
<p class="admonition-title">Tip</p>

Parola yöneticinizi diğer kimlik doğrulama yöntemlerini düzenlemek için de kullanabilirsiniz! Yeni bir giriş ekleyin ve uygun alanları doldurun, güvenlik soruları veya yedek anahtar gibi şeyler için notlar ekleyebilirsiniz.

</div>

Oturum açma kimlik bilgilerinizi yönetmekten siz sorumlu olacaksınız. Daha fazla güvenlik için hesaplarınızda [MFA](multi-factor-authentication.md) ayarlayabilirsiniz.

[Önerilen parola yöneticileri](../passwords.md ""){.md-button}

#### Email aliases

If you don't want to give your real email address to a service, you have the option to use an alias. We described them in more detail on our email services recommendation page. Essentially, alias services allow you to generate new email addresses that forward all emails to your main address. This can help prevent tracking across services and help you manage the marketing emails that sometimes come with the sign up process. Those can be filtered automatically based on the alias they are sent to.

Should a service get hacked, you might start receiving phishing or spam emails to the address you used to sign up. Using unique aliases for each service can assist in identifying exactly what service was hacked.

[Recommended email aliasing services](../email-aliasing.md ""){.md-button}

### "Sign in with..." (OAuth)

OAuth is an authentication protocol that allows you to register for a service without sharing much information with the service provider, if any, by using an existing account you have with another service instead. Whenever you see something along the lines of "Sign in with *provider name*" on a registration form, it's typically using OAuth.

When you sign in with OAuth, it will open a login page with the provider you choose, and your existing account and new account will be connected. Your password won't be shared, but some basic information typically will (you can review it during the login request). This process is needed every time you want to log in to the same account.

The main advantages are:

- **Security**: you don't have to trust the security practices of the service you're logging into when it comes to storing your login credentials, because they are stored with the external OAuth provider, which when it comes to services like Apple and Google typically follow the best security practices, continuously audit their authentication systems, and don't store credentials inappropriately (such as in plain text).
- **Ease of use**: multiple accounts are managed by a single login.

But there are disadvantages:

- **Privacy**: the OAuth provider you log in with will know the services you use.
- **Centralization**: if the account you use for OAuth is compromised, or you aren't able to log in to it, all other accounts connected to it are affected.

OAuth can be especially useful in those situations where you could benefit from deeper integration between services. Our recommendation is to limit using OAuth to only where you need it, and always protect the main account with [MFA](multi-factor-authentication.md).

All the services that use OAuth will be as secure as your underlying OAuth provider's account. For example, if you want to secure an account with a hardware key, but that service doesn't support hardware keys, you can secure the account you use with OAuth with a hardware key instead, and now you essentially have hardware MFA on all your accounts. It is worth noting though that weak authentication on your OAuth provider account means that any account tied to that login will also be weak.

There is an additional danger when using *Sign in with Google*, *Facebook*, or another service, which is that typically the OAuth process allows for *bidirectional* data sharing. For example, logging in to a forum with your Twitter account could grant that forum access to do things on your Twitter account such as post, read your messages, or access other personal data. OAuth providers will typically present you with a list of things you are granting the external service access to, and you should always ensure that you read through that list and don't inadvertently grant the external service access to anything it doesn't require.

Malicious applications, particularly on mobile devices where the application has access to the WebView session used for logging in to the OAuth provider, can also abuse this process by hijacking your session with the OAuth provider and gaining access to your OAuth account through those means. Using the *Sign in with* option with any provider should usually be considered a matter of convenience that you only use with services you trust to not be actively malicious.

### Telefon numarası

Kayıt için telefon numarası gerektiren hizmetlerden kaçınmanızı öneririz. A phone number can identify you across multiple services and depending on data sharing agreements this will make your usage easier to track, particularly if one of those services is breached as the phone number is often **not** encrypted.

Mümkünse gerçek telefon numaranızı vermekten kaçınmalısınız. Some services will allow the use of VOIP numbers, however these often trigger fraud detection systems, causing an account to be locked down, so we don't recommend that for important accounts.

In many cases you will need to provide a number that you can receive SMS or calls from, particularly when shopping internationally, in case there is a problem with your order at border screening. It's common for services to use your number as a verification method; don't let yourself get locked out of an important account because you wanted to be clever and give a fake number!

### Kullanıcı adı ve şifre

Bazı hizmetler e-posta kullanmanızı gerektirmeden, sadece kullanıcı adı ve şifre ile kayıt olmanıza izin verirler. Bu hizmetler VPN ve Tor ile birlikte kullanıldığında ekstra gizlilik sağlayabilirler. Bu hesaplar için kullanıcı adınızı veya şifrenizi unutmanız durumunda büyük olasılıkla **hesabınızı kurtarmanın hiçbir yolu olmayacağını** unutmayın.
