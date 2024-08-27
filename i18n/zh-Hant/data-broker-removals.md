---
title: Data Removal Services
icon: material/database-off
description: Our recommended methods for removing your personal information from data brokers and people search sites.
cover: data-broker-removals.webp
---

<small>Protects against the following threat(s):</small>

- [:material-account-search: Public Exposure](basics/common-threats.md#limiting-public-information){ .pg-green }

"People search sites" operated by data brokers represent an immense privacy risk to the majority of Americans. For many, sensitive personal information such as your address, phone number, email, and age is a simple internet search away. While there is unfortunately no federal regulation in place to protect your data, many of these companies will remove your information from their _public_ databases upon request.

:flag_us: **Note:** Many of these tools are only available in the United States, and data brokers collecting, sharing, and selling information from public records and other resources is largely a US-centric issue. In many other regions, your data is already protected via regulations like the GDPR. We will always advocate for similarly strong privacy protections in the United States, but those affected today may still benefit from these "stop-gap" solutions.

Counterintuitively, removing your personal data on these sites from the internet generally requires _providing_ these companies with your personal data for them to comply with the request. Unfortunately, in most cases it is still worth doing so to minimize the amount of personal data about you which is publicly accessible.

<div class="admonition example" markdown>
<p class="admonition-title">Try it out</p>

Use your favorite [search engine](search-engines.md) to see if your data is trivially exposed by searching for your name in quotes, plus your general location. For example, search for `"Jane Smith" Chicago IL`. In many cases, you may find your personal information makes up many of the first results. Even if results about you aren't readily available though, you may still be affected. The list of data brokers linked below will provide more places to check whether your data is in any public databases.

</div>

## Manual Opt-Outs <small>Free</small>

The quickest, most effective, and most private way to remove yourself from people search sites is to submit opt-out requests manually to each site. This can _seem_ like a daunting task, because there are hundreds of people search sites, but the reality is that the vast majority of these sites are operated by a small handful of companies.

You should search for your information on these 8 sites first, and submit an opt-out request if your information is found. Removing your data from these providers typically removes your data from many smaller sites at the same time.

- Acxiom
- BeenVerified
- InfoTracer
- Intelius
- Radaris
- Spokeo
- TruePeopleSearch
- Whitepages

Once you have done this, it's best to wait a week or two for the requests to propagate to all their sites. Then, you can start to search and opt-out of any remaining sites you find. It can be a good idea to use tools like [Optery](#optery-free-paid)'s free reports or [Google's _Results about you_](#google-results-about-you-free) tool to help find any data that remains on the internet.

Otherwise, privacy journalist Yael Grauer has compiled an excellent list of data broker sites with direct links to their search tools and opt-out pages. You can take some time to go though each site to determine whether they have your information, and remove it:

[:simple-github: Big Ass Data Broker Opt-Out List](https://github.com/yaelwrites/Big-Ass-Data-Broker-Opt-Out-List){ .md-button }

If you don't use an automatic scanner to find results about you, consider setting a reminder to re-do this process every 3, 6, or 12 months depending on your risk level and the amount of personal data you have out there. Unfortunately, it is common for your data to re-appear over time or show up on brand new people search sites even after you opt-out.

## EasyOptOuts <small>Paid</small>

<div class="admonition recommendation" markdown>

![EasyOptOuts logo](assets/img/data-broker-removals/easyoptouts.svg){ align=right }

**EasyOptOuts** is a $20/year service which will search a number of different data broker sites and automatically submit opt-out requests on your behalf. They will perform the first search and removal process immediately, and then re-run the process every 4 months in case your data shows up on new sites over time.

[:octicons-home-16: Homepage](https://easyoptouts.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://easyoptouts.com/privacy){ .card-link title="Privacy Policy" }

</div>

Some websites supported by EasyOptOuts are publicly searchable. In those cases EasyOptOuts will perform a search and only submit an opt-out request if your personal data is already found, to prevent sending your data in an opt-out request to sites that didn't have it already. However, they do support some sites which are not publicly searchable, and in those cases your data will be sent to them in an opt-out request regardless, in case you are in their private databases.

Our testing indicates that EasyOptOuts provides the best value out of any data removal service we've tested, with a very affordable price and high effectiveness. We will publish a detailed review of EasyOptOuts on our blog in the near future and update this page when it is published. [Independent findings from Consumer Reports](https://discuss.privacyguides.net/t/consumer-reports-evaluating-people-search-site-removal-services/19948) also indicate that EasyOptOuts is one of the top performing data removal services.

## Optery <small>Free & Paid</small>

<div class="admonition recommendation" markdown>

![Optery logo](assets/img/data-broker-removals/optery.svg){ align=right }

**Optery** is a free scanning tool which will discover which people search sites have your personal information, provide you with a report of those sites, and link you directly to the self-service removal process to do manually. If you keep your account, the report will be updated quarterly. Optery also has paid plans available where they will submit opt-out requests automatically on your behalf.

[:octicons-home-16: Homepage](https://optery.com){ .md-button .md-button--primary }
[:octicons-eye-16:](https://optery.com/privacy-policy){ .card-link title="Privacy Policy" }
[:octicons-info-16:](https://help.optery.com){ .card-link title=Documentation}

</div>

Optery's free scanning tool is an effective way to discover which data brokers have your information already, and their self-service dashboard allows you to easily submit opt-out requests manually.

We have not finished testing Optery's premium, _automatic_ opt-out plans, although initial results appear to be positive. [Independent findings from Consumer Reports](https://discuss.privacyguides.net/t/consumer-reports-evaluating-people-search-site-removal-services/19948) also indicate that Optery is one of the top performing data removal services. It necessarily takes at least a few months for us to evaluate a new data removal service, so check back here soon for our own test results. We will also publish a detailed review of Optery's full service on our blog when we have completed testing, and we will update this page accordingly.

## Google _與你相關的結果_ <small>免費</small>

此方法需要您將您的個人資訊提交給 Google，讓他們定期監控您的搜尋結果。 Google 聲稱不會將提供給此工具的資訊用於其他 Google 產品，以「個人化您的體驗」。

<div class="admonition recommendation" markdown>

![Google 標誌](assets/img/data-broker-removals/google.svg){ align=right }

**與你相關的結果** 是一個免費工具，可協助您發現您的個人聯絡資訊，包括住家地址、電話號碼和電子郵件地址，是否會出現在 Google 搜尋結果中。 如果發現任何個人資訊，您可以要求刪除。

[:octicons-globe-16: 打開網頁工具](https://myactivity.google.com/results-about-you){ .md-button .md-button--primary }
[:octicons-info-16:](https://support.google.com/websearch/answer/12719076){ .card-link title=說明文件}

</div>

在許多情況下，Google 搜尋是潛在騷擾者或施虐者尋找您個人資訊的第一個地方，因此使用 Google 搜尋是值得的。 但是，此工具不會從被發現的網站本身移除您的資訊，只會移除它們在 Google 上的搜尋結果。 您仍應考慮手動退出所發現的結果，或使用其他服務直接自動退出這些網站。

You can add up to 3 addresses, 3 phone numbers, and 3 email addresses to your Google account to monitor for. The service is only available in select markets (initially the US and UK) to users over 18.

When results are found, they will be available for review in this web tool. You can also optionally receive an email notification delivered to the account's Gmail address that lets you know when new results are found. You will then be able to click **Request to remove** on each discovered listing, and Google will review the request.

In our testing, this tool worked to reliably remove people search sites from Google search results, but was not effective against websites that showed _corporate_ filing information, even if you used your personal address to register a company, nor was it effective against social media profiles.
