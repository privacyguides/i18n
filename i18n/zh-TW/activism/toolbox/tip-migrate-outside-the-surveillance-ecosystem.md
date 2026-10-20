---
title: 從監控的生態系中打包走人
description: 身為隱私權倡議者，我們必須以身作則，並透過遠離科技巨頭，支持有著良好隱私權實踐的工具與組織。
icon: fontawesome/solid/arrow-right-from-bracket
cover: activism/banner-toolbox-tip-migrate.webp
---

As privacy activists, it's not only important to support the tools and organizations with good privacy practices, but also to lead by example when it comes to **moving away from the surveillance ecosystem**. We cannot afford to compromise our principles simply for [convenience](https://www.privacyguides.org/articles/2025/06/07/selling-surveillance-as-convenience/).

Here's why and how to move away from Big Tech and embrace alternatives:

## 在隱私權相關工作中使用科技巨頭產品所付出的代價

While using the most popular mainstream tools and platforms for our work might seem efficient at first, there can be an immense cost to it, if these tools and platforms aren't aligned with our privacy values.

<style>
.emoji-list-a ol {
  list-style: big-tech;
}
@counter-style big-tech {
  system: cyclic;
  symbols: "👁️‍🗨️" "⚠️" "🚨" "⛔️" "💛";
  suffix: "  ";
</style>

<div class="emoji-list-a" markdown>

1. 第一個缺點在於，當我們使用與自身價值觀背道而馳的產品時，便等於直接參與維持反隱私企業的運作，並助長了[監控資本主義](../../basics/common-threats.md/#surveillance-as-a-business-model)的發展。

2. 第二個缺點在於，光是使用大型科技公司的工具，我們就間接助長了那些對所有人隱私極為不利的服務的使用。

3. 第三個缺點在於，若我們在實際行動與溝通中使用這些工具，便會危及那些仰賴我們的專業知識來保障其資料安全的人士的資料。 They might think: "If this privacy advocate asks me to fill a Google form, it's probably safe enough to use Google products for sensitive data."

   With great _knowledge_ comes great responsibility. We must protect the data people share with us, even more than we would our own.

4. 第四個缺點在於，身為隱私權倡議者，若要求他人使用侵犯其隱私權的工具與我們溝通，可能會損害我們的公信力，並對整個社群造成負面影響。 Observers might think: "If all these privacy advocates use Facebook groups, why should I listen when they recommend that I move away from Facebook?"

5. 最後，第五個缺點在於，我們需&#x8981;_&#x4EE5;身作則_，並證明在不使用侵犯隱私的技術的情況下，**確實**也能夠過著互聯的生活。

   Because a better world _is_ actually possible, right now. It might not be as easy and as convenient, but it's certainly possible to thrive outside the Big Tech surveillance apparatus, especially for privacy activists and digital rights organizations.

   As the saying goes: ==If not us, then who? If not now, then when?==

</div>

## 如何擺脫損害隱私的工具，並選擇更好的替代方案

<div class="admonition question inline end" markdown>
<p class="admonition-title">最好的工具室什麼？</p>

For each proposed alternative, you should always first consider your own [threat model](../../basics/threat-modeling.md). One tool might be ideal for one person or organization, but another tool might be better for another. Make sure to understand well your threat model in order to choose the tools that are the best for your unique situation.

</div>

關於這件事，有兩則好消息：

- 首先，現今已有許多出色的替代方案，不僅能支援各類任務，還能保障您與通訊對象的隱私。

- 其次，你不必全部一次到位！請循序漸進地展開搬遷，但務必持續下去。

以下是一份替代方案清單，您可以開始採用這些方案，以提升倡議工作中的資料隱私：

### 對於個人及組織

<style>
.emoji-list-b ul {
  list-style: tools-individuals;
}
@counter-style tools-individuals {
  system: fixed;
  symbols: "💬" "🧅" "📧" "📑" "☁️" "❓" "📆" "🗣️" "🍪" "🔇" "🤖" "💼" "📞" "🐘";
  suffix: "  ";
</style>

<div class="emoji-list-b" markdown>

- **[Messaging communication](../../real-time-communication.md):** Move your text message communication, audio calls, and video calls to a secure messenger like Signal. Enable features like Signal's username option, and disappearing messages.

- **Sensitive messaging communication:** If your threat model requires a peer-to-peer solution that doesn't need a phone number and transits over the [Tor network](https://www.privacyguides.org/articles/2025/04/30/in-praise-of-tor/), you might want to use an application such as [Cwtch](https://docs.cwtch.im/) or [Briar](../../real-time-communication.md/#briar).

- **[Email communication](../../email.md):** Migrate to a privacy-respectful email service that offers end-to-end encryption, such as Proton Mail or Tuta. Make sure to inform yourself about the limitations of email privacy when using email for sensitive communication.

    <section class="admonition success inline end" markdown>
    <p class="admonition-title">Service providers disclosure and compatibility</p>

  If you use your own custom domain name for email addresses, let the people you communicate with know what your service provider is.

  That way, they will know that if they use a compatible service provider, they might benefit from end-to-end encryption protections for the content of their communications with you without requiring any additional steps.

  For example, this is the case when emailing from a Proton Mail account to another Proton Mail account, or from a Tuta Mail account to another Tuta Mail account.

    </section>

- **[Document storing and sharing](../../document-collaboration.md):** Move away from privacy-invasive Google products to store and share documents. Instead, use an end-to-end encrypted solution such as [CryptPad](https://www.privacyguides.org/articles/2025/02/07/cryptpad-review/) for your collaborative documents and forms. Proton Drive also offers collaborative documents with _Proton Docs_ and _Sheets_.

- **[Storing files](../../cloud.md):** Choose an end-to-end encrypted cloud solution to store and share files. Always keep in mind that if a cloud service provider doesn't offer solid end-to-end encryption, then it can potentially access any of your stored files.

- **Surveys:** Stop using products such as Google Forms to poll your community. Instead, choose a privacy-focused alternative such as [CryptPad Form](https://www.privacyguides.org/articles/2025/02/07/cryptpad-review/#form) or [Framaforms](https://framaforms.org/abc/en/).

- **[Online calendar](../../calendar.md):** Your online calendar can be an important source of sensitive data. Moreover, you might store other's people data in it, or use it to share event links with collaborators. It's essential to make sure to use a privacy-protecting solution for online and collaborative calendars.

- **Groups and events:** When organizing groups or events, be careful to choose platforms that are privacy-respectful and don't require participants to register personal information. Keep in mind that if you only use Facebook groups, you are contributing to people staying on a privacy-invasive platform. If you only use a closed Meetup group, you are demanding people create an account and share their sensitive data in order to join. Instead, use privacy-respectful platforms such as [Mobilizon](https://mobilizon.org/) or [LAUTI](https://lauti.org/) for groups and events, [Discourse](https://www.discourse.org/) for forums, or simply use your own website to advertise in-person events.

- **Website analytics and cookies:** If you own a website for your organization or for your individual advocacy, make sure to remove from it any [tracking technologies](https://blog.mozilla.org/en/firefox/cross-site-tracking-lets-unpack-that/) that could be sending your visitors' data to Google, Facebook, or other advertising corporations. You shouldn't need a cookie banner for your website, because _your website shouldn't use any non-essential cookies_. If you really need website analytics, try using a privacy-respectful alternative such as [Umami](https://umami.is/) or [Plausible Analytics](https://plausible.io/).

- **Smart devices:** Whether you are meeting with other advocates at home or organizing an event, make sure the location is free from Big Tech [surveillance devices](https://www.privacyguides.org/articles/2025/03/10/the-privacy-of-others/#notify-guests-if-you-are-using-a-smart-speaker) that might get easily forgotten. This may include a doorbell equipped with a camera, a smart speaker such as Amazon Echo, Google Home or Google Nest, or any other audio or video recording devices that is on. Physically unplug any such devices in the location _before_ guests arrive. If you cannot unplug them, at least provide a proper warning to any guests before they enter the location and the device collects their audio or video data.

- **Usage of AI:** Be extremely careful if you are using AI platforms. Most current mainstream AI products will send at least some data or metadata to the company's remote server. This can create many privacy issues, ranging from mild to severe. Never use these products to upload data about another person without their _prior explicit consent_. Ideally, refrain from using any AI tools in your advocacy work entirely.

- **Candidates data:** If your organization hires people, be mindful of how you handle candidates' data. Try to select privacy-respecting solutions such as email communication instead of using commercial platforms that might share candidates' data with third-parties. Only request the minimum information required from applicants, and always delete all data you are no longer required to keep as soon as you don't need it anymore.

- **Availability:** Make sure you or your organization is reachable outside the Big Tech ecosystem. If your organization only has a Facebook page, then people without a Facebook account cannot reach out to you. The same is true for other commercial social media. Instead, try to rely on a website you control yourself, or a social network page you can host yourself.

- **[Social media](../../social-networks.md):** Move away from commercial social media platforms. Mainstream platforms are almost all abusing their users' data. By keeping an account there, you are indirectly encouraging your followers to stay there as well, perpetuating the platform's abuse.

  While you may want to keep a minimal presence to advertise that you have now moved your activity to a more privacy-respectful platform, you should keep your engagement there to a minimum.

  Instead, migrate your advocacy work to better social networks that aren't abusing users' data, and encourage your followers to migrate with you. Choose and support a platform that is more aligned with your privacy values, such as [Mastodon](https://www.privacyguides.org/articles/2025/07/15/mastodon-privacy-and-security/) or any other open-source non-commercial applications connected to the [Fediverse](https://blog.elenarossini.com/fediverse-video/).

</div>

## 更多資源

- [經我們社群審核過的大型科技公司替代方案 (_隱私指南_)](../../tools.md)

- [尊重隱私的歐洲式科技替代方案 (_隱私指南_)](https://www.privacyguides.org/articles/2025/03/19/private-european-alternatives/)

- [關於脫離大型科技公司的實用文章與建議 (_The Opt Out Project_)](https://www.optoutproject.net/)

- [若您剛開始接觸這方面，這些是關於如何提升隱私保護的建議 (_隱私指南_)](https://www.privacyguides.org/articles/2025/07/24/privacy-is-like-broccoli/#tools-and-services-you-can-start-using)
