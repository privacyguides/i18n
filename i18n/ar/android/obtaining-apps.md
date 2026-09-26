---
title: "نزيل التطبيقات"
description: نوصي بهذه الطرق للحصول على التطبيقات على Android دون الحاجة إلى التعامل مع خدمات Google Play.
---

هناك طرق عديدة للحصول على تطبيقات Android بخصوصية، حتى من Play Store، دون الحاجة إلى التعامل مع خدمات Google Play. نوصي بالطرق التالية للحصول على التطبيقات على Android، مرتبة حسب الأفضلية.

## Obtainium

<div class="admonition recommendation" markdown>

![Obtainium logo](../assets/img/android/obtainium.svg){ align=right }

تطبيق Obtainium هو مدير تطبيقات (App Manager) يتيح لك تثبيت التطبيقات وتحديثها مباشرةً من صفحة الإصدارات الخاصة بالمطور نفسه. مثل GitHub أو GitLab أو موقع المطور نفسه، بدلا من الاعتماد على متجر تطبيقات أو مستودع مركزي (Centralized App Store/Repository). يدعم التحديثات التلقائية في الخلفية على Android 12 والإصدارات الأحدث.

[:octicons-repo-16: Repository](https://github.com/ImranR98/Obtainium#readme){ .md-button .md-button--primary }
[:octicons-info-16:](https://github.com/ImranR98/Obtainium/wiki){ .card-link title=Documentation}
[:octicons-code-16:](https://github.com/ImranR98/Obtainium){ .card-link title="Source Code" }
[:octicons-heart-16:](https://github.com/sponsors/ImranR98){ .card-link title=Contribute }

<details class="downloads" markdown>
<summary>التنزيلات</summary>

- [:simple-github: GitHub](https://github.com/ImranR98/Obtainium/releases)

</details>

</div>

يتيح لك Obtainium تنزيل ملفات تثبيت APK من مجموعة كبيرة من المصادر، وتقع عليك مسؤولية التأكد من أن هذه المصادر والتطبيقات موثوقة وشرعية. على سبيل المثال، يُفترض أن يكون استخدام Obtainium لتثبيت Signal من صفحة APK الرسمية الخاصة بـ [Signal](https://signal.org/android/apk) آمنًا، لكن تثبيت التطبيقات من مستودعات APK تابعة لجهات خارجية مثل Aptoide أو APKPure قد ينطوي على مخاطر إضافية. خطر تثبيت تحديث ضار أقل، لأن Android يتأكد قبل التثبيت أن التحديث صادر من نفس مطور التطبيق الموجود على هاتفك.

## متجر تطبيقات GrapheneOS

يتوفر متجر تطبيقات GrapheneOS على GitHub. It supports Android 12 and above and is capable of updating itself. يضم متجر التطبيقات، تطبيقات مستقلة طوّرها مشروع GrapheneOS، مثل [Auditor](../device-integrity.md#auditor-android) و[Camera](general-apps.md#secure-camera) و[PDF Viewer](general-apps.md#secure-pdf-viewer). إذا كنت تبحث عن هذه التطبيقات، فننصح بشدة بتنزيلها من متجر GrapheneOS بدلا من Play Store، لأن التطبيقات الموجودة في متجر GrapheneOS موقعة بتوقيع خاص بالمشروع نفسه، ولا تملك Google إمكانية الوصول إليه.

## متجر أورورا

يتطلب Google Play Store تسجيل الدخول باستخدام حساب Google، وهذا ليس جيدا للخصوصية. يمكنك تجنب ذلك باستخدام تطبيق بديل، مثل Aurora Store.

<div class="admonition recommendation" markdown>

![Aurora Store logo](../assets/img/android/aurora-store.webp){ align=right }

تطبيق **Aurora Store** هو تطبيق بديل لـ Google Play Store، ولا يحتاج إلى حساب Google أو Google Play Services أو microG لتنزيل التطبيقات.

[:octicons-home-16: Homepage](https://auroraoss.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://gitlab.com/AuroraOSS/AuroraStore/-/blob/master/POLICY.md){ .card-link title="Privacy Policy" }
[:octicons-code-16:](https://gitlab.com/AuroraOSS/AuroraStore){ .card-link title="Source Code" }

<details class="downloads" markdown>
<summary>التنزيلات</summary>

- [:simple-gitlab: GitLab](https://gitlab.com/AuroraOSS/AuroraStore/-/releases)

</details>

</div>

لا يتيح لك Aurora Store تنزيل التطبيقات المدفوعة عند استخدام ميزة الحساب المجهول. يمكنك أيضا تسجيل الدخول إلى Aurora Store باستخدام حساب Google لتنزيل التطبيقات التي اشتريتها، لكن هذا سيتيح لـ Google معرفة قائمة التطبيقات التي ثبتها. ومع ذلك، ستظل تستفيد من عدم الحاجة إلى تثبيت Google Play Store الكامل أو Google Play Services أو microG على جهازك.

## يدويًا باستخدام إشعارات RSS

بالنسبة للتطبيقات التي تُنشر على منصات مثل GitHub وGitLab، يمكنك إضافة RSS feed إلى [قارئ الأخبار](../news-aggregators.md) لمتابعة الإصدارات الجديدة.

![RSS APK](../assets/img/android/rss-apk-light.png#only-light) ![RSS APK](../assets/img/android/rss-apk-dark.png#only-dark) ![APK Changes](../assets/img/android/rss-changes-light.png#only-light) ![APK Changes](../assets/img/android/rss-changes-dark.png#only-dark)

### GitHub

On GitHub, using [Secure Camera](general-apps.md#secure-camera) as an example, you would navigate to its [releases page](https://github.com/GrapheneOS/Camera/releases) and append `.atom` to the URL:

`https://github.com/GrapheneOS/Camera/releases.atom`

### GitLab

On GitLab, using [Aurora Store](#aurora-store) as an example, you would navigate to its [project repository](https://gitlab.com/AuroraOSS/AuroraStore) and append `/-/tags?format=atom` to the URL:

`https://gitlab.com/AuroraOSS/AuroraStore/-/tags?format=atom`

### Verifying APK Fingerprints

If you download APK files to install manually, you can verify their signature with the [`apksigner`](https://developer.android.com/studio/command-line/apksigner) tool, which is a part of Android [build-tools](https://developer.android.com/studio/releases/build-tools).

1. Install [Java JDK](https://oracle.com/java/technologies/downloads).

2. Download the [Android Studio command line tools](https://developer.android.com/studio#command-tools).

3. Extract the downloaded archive:

   ```bash
   unzip commandlinetools-*.zip
   cd cmdline-tools
   ./bin/sdkmanager --sdk_root=./ "build-tools;29.0.3"
   ```

4. Run the signature verification command:

   ```bash
   ./build-tools/29.0.3/apksigner verify --print-certs ../Camera-37.apk
   ```

5. The resulting hashes can then be compared with another source. Some developers such as Signal [show the fingerprints](https://signal.org/android/apk) on their website.

   ```bash
   Signer #1 certificate DN: CN=GrapheneOS
   Signer #1 certificate SHA-256 digest: 6436b155b917c2f9a9ed1d15c4993a5968ffabc94947c13f2aeee14b7b27ed59
   Signer #1 certificate SHA-1 digest: 23e108677a2e1b1d6e6b056f3bb951df7ad5570c
   Signer #1 certificate MD5 digest: dbbcd0cac71bd6fa2102a0297c6e0dd3
   ```

## F-Droid

![F-Droid logo](../assets/img/android/f-droid.svg){ align=right width=120px }

\==We only recommend F-Droid as a way to obtain apps which cannot be obtained via the means above.== F-Droid is often recommended as an alternative to Google Play, particularly within the privacy community. The option to add third-party repositories and not be confined to Google's walled garden has led to its popularity. F-Droid additionally has [reproducible builds](https://f-droid.org/en/docs/Reproducible_Builds) for some applications and is dedicated to free and open-source software. However, there are some security-related downsides to how F-Droid builds, signs, and delivers packages:

Due to their process of building apps, apps in the _official_ F-Droid repository often fall behind on updates. F-Droid maintainers also reuse package IDs while signing apps with their own keys, which is not ideal as it gives the F-Droid team ultimate trust. Additionally, the requirements for an app to be included in the official F-Droid repo are less strict than other app stores like Google Play, meaning that F-Droid tends to host a lot more apps which are older, unmaintained, or otherwise no longer meet [modern security standards](https://developer.android.com/google/play/requirements/target-sdk).

Other popular third-party repositories for F-Droid such as [IzzyOnDroid](https://apt.izzysoft.de/fdroid) alleviate some of these concerns. The IzzyOnDroid repository pulls builds directly from code forges (GitHub, GitLab, etc.) and is the next best thing to the developers' own repositories. They also offer [reproducible builds](https://android.izzysoft.de/articles/named/iod-rbs-mirrors-clients) for hundreds of applications and have developers who verify the reproducibility of developer-signed APKs. Furthermore, the IzzyOnDroid team conducts [additional security scans](https://android.izzysoft.de/articles/named/iod-scan-apkchecks) of apps housed in the repo, which usually result in [deliberations](https://github.com/gouravkhunger/QuotesApp/issues/22) between them and app developers toward privacy improvements in their apps. Note that apps may be removed from the IzzyOnDroid repo in [certain circumstances](https://gitlab.com/IzzyOnDroid/repo#are-apps-removed-from-the-repo--and-when-does-that-happen).

The [F-Droid](https://f-droid.org/en/packages) and [IzzyOnDroid](https://apt.izzysoft.de/fdroid) repositories are home to countless apps, so they can be useful places to search for and discover open-source apps that you can then download through other means such as the Play Store, Aurora Store, or by getting the APK directly from the developer. You should use your best judgment when looking for new apps via this method, and keep an eye on how frequently the app is updated. Outdated apps may rely on unsupported libraries, among other things, posing a potential security risk.

<div class="admonition note" markdown>
<p class="admonition-title">F-Droid Basic</p>

In some rare cases, the developer of an app will only distribute it through F-Droid ([Gadgetbridge](../health-and-wellness.md#gadgetbridge) is one example of this). If you really need an app like that, we recommend using the newer [F-Droid Basic](https://f-droid.org/en/packages/org.fdroid.basic) client instead of the original F-Droid app to obtain it. F-Droid Basic supports automatic background updates without privileged extension or root, and has a reduced feature set (limiting attack surface).

</div>
