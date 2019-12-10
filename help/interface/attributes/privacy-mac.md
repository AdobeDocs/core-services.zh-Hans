---
description: 有关在 Adobe Experience Cloud 中上传和使用的个人可识别信息 (PII) 的注意事项和最佳实践。
keywords: customer attributes;core services
seo-description: 有关在 Adobe Experience Cloud 中上传和使用的个人可识别信息 (PII) 的注意事项和最佳实践。
seo-title: 隐私注意事项 - 客户属性
solution: Experience Cloud
title: 隐私注意事项 - 客户属性
uuid: 5666dc4e-55fa-4196-9985-cf530cfb9247
translation-type: tm+mt
source-git-commit: ae97db27349940a8df7ee2ba6678683f57585678

---


# 隐私注意事项 - 客户属性

有关在 Adobe Experience Cloud 中上传和使用的个人可识别信息 (PII) 的注意事项和最佳实践。


<!-- <p>https://wiki.corp.adobe.com/display/omtrplatform/Visitor+Enrichment+and+privacy#VisitorEnrichmentandprivacy-INFORMATIONASSOCIATIONOPTIONS </p> -->


* 名字和姓氏
* 家庭或其他实际地址
* 电子邮件地址
* 电话号码
* 身份证号码
* 其他提供具体个人的实际或在线联系方式的标识。（不同地区有不同定义。请在开展业务的所有地区验证是否符合当地与隐私及 PII 相关的法律和法规。）


Adobe 提供的工具允许广告商收集消费者访问其站点或使用其应用程序的行为信息。Adobe 提供的工具还允许广告商采用其他信息管理系统中的离线或外部客户记录来增强此信息。

广告商这么做的一个常见原因是为了在制定适合消费者的市场营销和广告决策时提高信息的可用性。Adobe Analytics 和 Target 可让广告商上传个人可识别信息 (PII)，如电子邮件地址，但只有在将该信息经过哈希处理以使其不可用于联系个人之后才允许这么做。经过哈希处理的信息依然可用于分析和市场营销。在此提醒，Adobe 禁止广告商向 Adobe 发送敏感的个人信息，如医疗记录、财务帐户信息和未成年人的信息。

Adobe 意识到这类市场营销和广告决策可能牵涉消费者隐私，正是因为如此，Adobe 设有内置隐私控制以帮助广告商满足消费者的期望。Adobe 建议广告商仔细考虑哪些信息适合用于市场营销，并在何种环境下才有权使用这类信息。

**最佳实践**

在将 PII 上传到 Adobe Analytics 或 Target 时，Adobe 建议客户在上传之前对 PII 进行哈希处理。经过哈希处理的信息依然可用于分析和市场营销。在此提醒，Adobe 禁止广告商向 Adobe Analytics 和 Target 发送敏感的个人信息，如医疗记录、财务帐户信息和未成年人的信息。

Adobe 建议广告商仔细考虑哪些信息适合用于市场营销，并在何种环境下才有权使用这类信息。

由于客户隐私法律仍在不断地变动之中，Adobe 建议广告商遵守以下三条共同原则：

1. 做您所说（在隐私政策许可的范围内）。
1. 说您所做（在隐私政策许可的范围内）。
1. 不要让您的消费者感到出乎意料。

Adobe 时刻将这些期望铭记于心，因此建议广告商在将浏览行为关联到 PII 时，应提供通知或专门说明消费者已通过验证。例如，可以在网站标题内加入问候语。Adobe 还建议广告商在其隐私政策中介绍会将哪种类型的浏览信息关联到 PII，以及在何种环境下将浏览信息与 PII 关联。最后，Adobe 强烈建议广告商审核他们提供给消费者的退出选项，以了解他们在退出后是否能够以及如何使用未经验证的配置文件信息。

<!-- <p> <b>Vinay Geol</b> should help craft privacy regarding how all MAC uses privacy/cookies. Privacy implications around each part of the workflow. Moving from CRM to MAC. Can it include PII? What is PII? What isn't PII? </p> 
<p>CRM data is Known Data or Info. Going to combine with activity that occurs when visitor was not authenticated. PII wiki: </p> 
<p>https://wiki.corp.adobe.com/display/omtrplatform/Visitor+Enrichment+and+privacy#VisitorEnrichmentandprivacy-INFORMATIONASSOCIATIONOPTIONS </p> 
<p>Refactoring of implementation docs as it relates to privacy and cookies. </p> 
<p>Add content to t-publish-audience-segment, as follows: </p> 
<p> Audiences are not filtered based on the authentication state of a visitor. If a visitor can browse your site in un-authenticated and authenticated states, actions that occur when a visitor is un-authenticated can still cause a visitor to be included in an audience. Please review <link> to understand the full privacy implications of audience sharing. </p> 
<p>That "link" goes to a topic dedicated to PII, with this text: </p> 
<p> - Adobe Analytics allows its advertisers to upload personally identifiable information (PII) such as email addresses. When uploading PII to Adobe Analytics, Adobe recommends that the customer should hash PII prior to uploading it to Adobe. Hashed information can still be used for analysis and for marketing purposes. As a reminder, Adobe prohibits advertisers from sending sensitive personal information to Adobe Analytics, such as medical records, financial account information, and information about minors. </p> 
<p> - Adobe recommends its advertisers carefully consider which information is appropriate to use for marketing purposes and in which circumstances the advertiser has permission to use such information. </p> 
<p> - As consumer privacy law remains in flux, Adobe recommends that advertisers respect three common tenets: 1) Do what you say (in your privacy policy); 2) Say what you do (in your privacy policy); and 3) Don't surprise your consumers. </p> 
<p> - With these expectations in mind, Adobe recommends that when an advertiser associates browsing activities to PII, the advertiser provide notices/personalization indicating that the consumer is authenticated. An example of this is including a 'Hello, Jane' greeting within the header of the website. Adobe also recommends that advertisers describe in its privacy policy what type of browsing information it associates with PII and under what circumstances browsing information is associated with PII. Lastly, Adobe strongly recommends advertisers review the opt out choices they provide their consumers to understand whether and how they can use unauthenticated profile information post opt out. </p> 
<p>Possibly revamp the cookies to include privacy, with best practices: https://docs.adobe.com/content/help/en/core-services/interface/ec-cookies/cookies-privacy.html </p> -->
