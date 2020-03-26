---
description: 有关在 Adobe Experience Cloud 中上传和使用的个人可识别信息 (PII) 的注意事项和最佳实践。
keywords: customer attributes;core services
seo-description: 有关在 Adobe Experience Cloud 中上传和使用的个人可识别信息 (PII) 的注意事项和最佳实践。
seo-title: 隐私注意事项 - 客户属性
solution: Experience Cloud
title: 隐私注意事项 - 客户属性
uuid: 5666dc4e-55fa-4196-9985-cf530cfb9247
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# 隐私注意事项 - 客户属性

有关在 Adobe Experience Cloud 中上传和使用的个人可识别信息 (PII) 的注意事项和最佳实践。


<!-- <p>https://wiki.corp.adobe.com/display/omtrplatform/Visitor+Enrichment+and+privacy#VisitorEnrichmentandprivacy-INFORMATIONASSOCIATIONOPTIONS </p> -->


* 名字和姓氏
* 主页或其他物理地址
* 电子邮件地址
* 电话号码
* 社会安全号
* 允许个人进行物理或在线联系的其他标识符。 (因位置而异。 请验证并遵守与隐私和PII相关的当地法律和法规，以便与您开展业务的所有地点相关。)


Adobe提供的工具使广告商能够收集消费者访问其网站或使用其应用程序的行为信息。 Adobe还提供了一些工具，使广告商能够利用其他信息管理系统中广告商可能拥有的线下或外部客户记录来增强这些信息。

广告商这样做的一个常见原因是，在作出适合消费者的营销和广告决策时，改进可用的信息。 Adobe Analytics和目标允许广告商上传个人身份信息(PII)（如电子邮件地址），但必须经过哈希处理才能使其无法用于联系个人。 哈希信息仍可用于分析和营销目的。 作为提醒，Adobe禁止广告商向Adobe发送敏感的个人信息，如医疗记录、财务帐户信息和未成年人信息。

Adobe认识到，这些类型的营销和广告决策可能会影响消费者隐私，这正是Adobe内置隐私控制来帮助广告商满足其消费者期望的原因。 Adobe建议其广告商仔细考虑哪些信息适合用于营销目的，以及广告商在哪些情况下有权使用这些信息。

**最佳实践**

将PII上传到Adobe Analytics或Adobe目标时，Adobe建议客户在将PII上传到Adobe之前对其进行哈希处理。 哈希信息仍可用于分析和营销目的。 作为提醒，Adobe禁止广告商向Adobe Analytics和Adobe目标发送敏感的个人信息，如医疗记录、财务帐户信息和未成年人信息。

Adobe建议其广告商仔细考虑哪些信息适合用于营销目的，以及广告商在哪些情况下有权使用这些信息。

随着消费者隐私法的不断变化，Adobe建议广告商遵守以下三个共同原则：

1. 按照您的说法（在隐私权政策中）执行。
1. 说出您的行为（在隐私权政策中）。
1. 不要让您的消费者感到意外。

考虑到这些期望，Adobe建议广告商将浏览活动关联到PII时，广告商会提供通知或个性化，指示消费者已通过身份验证。 其示例包括网站标题中的问候语。 Adobe还建议广告商在其隐私权政策中说明其与PII关联的浏览信息类型以及在哪些情况下浏览信息与PII关联。 最后，Adobe强烈建议广告商查看他们为消费者提供的选择退出选项，以了解他们是否可以使用未经身份验证的用户档案信息帖子以及如何使选择退出用。

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
