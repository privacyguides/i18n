---
meta_title: "كيفية إنشاء حسابات على الإنترنت بخصوصية - Privacy Guides"
title: "إنشاء الحسابات"
icon: 'material/account-plus'
description: أصبح إنشاء الحسابات على الإنترنت ضرورة شبه أساسية، لذا اتبع هذه الخطوات للحفاظ على خصوصيتك.
---

غالبا ما يسجل الناس في الخدمات دون تفكير. قد تكون خدمة بث لمشاهدة ذلك المسلسل الجديد الذي يتحدث عنه الجميع، أو حسابا يمنحك خصما في مطعم الوجبات السريعة المفضل لديك. مهما كان السبب، ينبغي أن تفكر في تأثير ذلك على بياناتك الآن وفي المستقبل.

هناك مخاطر مرتبطة بكل خدمة جديدة تستخدمها. تسرب البيانات، وكشف معلومات العملاء لجهات خارجية، ووصول موظفين غير موثوق بهم إلى البيانات؛ كلها احتمالات يجب أخذها في الاعتبار عند مشاركة معلوماتك. يجب أن تكون واثقا من قدرتك على الوثوق بالخدمة، ولهذا لا نوصي بتخزين البيانات المهمة إلا على المنتجات الأكثر نضجا والتي أثبتت موثوقيتها مع مرور الوقت. وهذا يعني عادة الخدمات التي توفر E2EE وخضعت لتدقيق تشفيري. يزيد التدقيق من الثقة بأن المنتج صُمم دون مشكلات أمنية واضحة ناتجة عن قلة خبرة المطوّر.

قد يكون من الصعب أيضا حذف حساباتك من بعض الخدمات. أحيانا قد يكون من الممكن [الكتابة فوق البيانات (overwriting)](account-deletion.md#overwriting-account-information) المرتبطة بالحساب، لكن في حالات أخرى قد تحتفظ الخدمة بسجل كامل لكل التغييرات التي أُجريت على الحساب.

## شروط الخدمة وسياسة الخصوصية

شروط الخدمة هي القواعد التي توافق على اتباعها عند استخدام الخدمة. في الخدمات الكبيرة، غالبا ما تطبّق هذه القواعد بواسطة أنظمة آلية (automated systems). أحيانا قد ترتكب هذه الأنظمة الآلية (automated systems) أخطاء. على سبيل المثال، قد يتم حظرك أو منعك من الوصول إلى حسابك في بعض الخدمات بسبب استخدام الـ VPN أو رقم VoIP. غالبا ما يكون الاعتراض على مثل هذا الحظر صعبا، كما أن عملية الاعتراض نفسها تكون آلية أيضا، ولا تنجح دائما. وهذا أحد الأسباب التي تجعلنا لا ننصح باستخدام Gmail للبريد الإلكتروني، على سبيل المثال. البريد الإلكتروني ضروري للوصول إلى الخدمات الأخرى التي قد تكون قد سجلت فيها.

سياسة الخصوصية توضح كيف تقول الخدمة إنها ستستخدم بياناتك، ومن المفيد قراءتها حتى تفهم كيف سيتم استخدام بياناتك. قد لا تكون الشركة أو المؤسسة ملزمة قانونيا باتباع كل ما ورد في السياسة (ويعتمد ذلك على الولاية القضائية). نوصي بأن تكون لديك فكرة عامة عن القوانين المحلية وما الذي تسمح لمزود الخدمة بجمعه.

نوصي بالبحث عن مصطلحات محددة مثل "جمع البيانات (data collection)" و"تحليل البيانات (data analysis)" و"ملفات تعريف الارتباط (cookies)" و"الإعلانات (ads)" أو خدمات "الجهات الخارجية (3rd-party services)". أحيانا ستتمكن من إلغاء الاشتراك في جمع بياناتك أو مشاركتها، لكن من الأفضل اختيار خدمة تحترم خصوصيتك منذ البداية.

ضع في اعتبارك أنك تضع ثقتك أيضا في الشركة أو المؤسسة، وفي التزامها بسياسة الخصوصية الخاصة بها.

## طرق المصادقة (Authentication methods)

عادة ما توجد عدة طرق لإنشاء حساب، ولكل منها مزايا وعيوب.

### البريد الإلكتروني وكلمة المرور

الطريقة الأكثر شيوعا لإنشاء حساب جديد هي استخدام عنوان بريد إلكتروني وكلمة مرور. عند استخدام هذه الطريقة، يجب عليك استخدام password manager واتباع [أفضل الممارسات](passwords-overview.md) المتعلقة بكلمات المرور.

<div class="admonition tip" markdown>
<p class="admonition-title">نصيحة</p>

يمكنك استخدام الـ password manager لتنظيم طرق المصادقة (authentication methods) الأخرى أيضا! Just add the new entry and fill the appropriate fields, you can add notes for things like security questions or a backup key.

</div>

You will be responsible for managing your login credentials. For added security, you can set up [MFA](multi-factor-authentication.md) on your accounts.

[Recommended password managers](../passwords.md ""){.md-button}

#### Email aliases

If you don't want to give your real email address to a service, you have the option to use an alias. We describe them in more detail on our email services recommendation page. Essentially, alias services allow you to generate new email addresses that forward all emails to your main address. This can help prevent tracking across services and help you manage the marketing emails that sometimes come with the sign-up process. Those can be filtered automatically based on the alias they are sent to.

Should a service get hacked, you might start receiving phishing or spam emails to the address you used to sign up. Using unique aliases for each service can assist in identifying exactly what service was hacked.

[Recommended email aliasing services](../email-aliasing.md ""){.md-button}

### "Sign in with..." (OAuth)

[Open Authorization (OAuth)](https://en.wikipedia.org/wiki/OAuth) is an authentication protocol that allows you to register for a service without sharing much information with the service provider, if any, by using an existing account you have with another service instead. Whenever you see something along the lines of "Sign in with *provider name*" on a registration form, it's typically using OAuth.

When you sign in with OAuth, it will open a login page with the provider you choose, and your existing account and new account will be connected. Your password won't be shared, but some basic information typically will (you can review it during the login request). This process is needed every time you want to log in to the same account.

The main advantages are:

- **Security**: You don't have to trust the security practices of the service you're logging into when it comes to storing your login credentials because they are stored with the external OAuth provider. Common OAuth providers like Apple and Google typically follow the best security practices, continuously audit their authentication systems, and don't store credentials inappropriately (such as in plain text).
- **Ease-of-use**: Multiple accounts are managed by a single login.

But there are disadvantages:

- **Privacy**: The OAuth provider you log in with will know the services you use.
- **Centralization**: If the account you use for OAuth is compromised, or you aren't able to log in to it, all other accounts connected to it are affected.

OAuth can be especially useful in those situations where you could benefit from deeper integration between services. Our recommendation is to limit using OAuth to only where you need it, and always protect the main account with [MFA](multi-factor-authentication.md).

All the services that use OAuth will be as secure as your underlying OAuth provider's account. For example, if you want to secure an account with a hardware key, but that service doesn't support hardware keys, you can secure the account you use with OAuth with a hardware key instead, and now you essentially have hardware MFA on all your accounts. It is worth noting though that weak authentication on your OAuth provider account means that any account tied to that login will also be weak.

There is an additional danger when using *Sign in with Google*, *Facebook*, or another service, which is that typically the OAuth process allows for *bidirectional* data sharing. For example, logging in to a forum with your Twitter account could grant that forum access to do things on your Twitter account such as post, read your messages, or access other personal data. OAuth providers will typically present you with a list of things you are granting the external service access to, and you should always ensure that you read through that list and don't inadvertently grant the external service access to anything it doesn't require.

Malicious applications, particularly on mobile devices where the application has access to the WebView session used for logging in to the OAuth provider, can also abuse this process by hijacking your session with the OAuth provider and gaining access to your OAuth account through those means. Using the *Sign in with* option with any provider should usually be considered a matter of convenience that you only use with services you trust to not be actively malicious.

### Phone number

We recommend avoiding services that require a phone number for sign up. A phone number can identify you across multiple services and depending on data sharing agreements this will make your usage easier to track, particularly if one of those services is breached as the phone number is often **not** encrypted.

You should avoid giving out your real phone number if you can. Some services will allow the use of VoIP numbers, however these often trigger fraud detection systems, causing an account to be locked down, so we don't recommend that for important accounts.

In many cases you will need to provide a number that you can receive SMS or calls from, particularly when shopping internationally, in case there is a problem with your order at border screening. It's common for services to use your number as a verification method; don't let yourself get locked out of an important account because you wanted to be clever and give a fake number!

### Username and password

Some services allow you to register without using an email address and only require you to set a username and password. These services may provide increased anonymity when combined with a VPN or Tor. Keep in mind that for these accounts there will most likely be **no way to recover your account** in the event you forget your username or password.
