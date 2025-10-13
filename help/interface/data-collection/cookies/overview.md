---
description: 了解 Adobe Experience Cloud 中的解决方案和服务如何使用 Cookie。
title: 如何在Experience Cloud中使用Cookie
uuid: 4255a13a-917b-4b5f-a7d4-4b2e7521d189
exl-id: 60f1a89e-d989-461b-a6a3-c1df022cd30b
source-git-commit: d6dc659104b3b24b60495cd97adb21ebb3962fc7
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 10%

---

# Experience Cloud中使用的Cookie

Adobe Experience Cloud使用Cookie。 Cookie是网站发送到您的浏览器的一小段数据，用于存储以供将来使用。 Cookie可帮助网站在您再次访问或在页面之间移动时记住某些内容。 Cookie有助于跟踪访问情况并区分不同的设备。

法律通常要求您先获得许可，然后才能在某人的设备上存储或使用Cookie。 Adobe建议咨询您的法律团队，了解适用的规则。

## 关于第一方 Cookie

Adobe Experience Cloud使用Cookie来跟踪不会在页面查看或浏览器会话之间持续的信息。 如果可能，Adobe会使用第一方Cookie（与您自己的网站绑定）。 要在您拥有的多个网站或域中跟踪活动，需要第三方Cookie。

某些浏览器和防间谍软件工具会阻止第三方Cookie。 Adobe提供了一些方法来确保Cookie仍然有效，即使Cookie被阻止也是如此。 其工作方式取决于您使用的是Experience Platform Identity Service (ECID)还是旧版Analytics Cookie（如`s_vi` Cookie）：

* [Experience Cloud Identity Service](https://experienceleague.adobe.com/zh-hans/docs/id-service/using/intro/overview)： ECID服务始终设置第一方Cookie，无论您的收集域是否与网站域匹配。 它使用JavaScript将Cookie放置在您网站的域中。

* [Analytics旧版标识符](analytics.md)（如`s_vi` Cookie）：Cookie是第一方还是第三方取决于您的设置：

   * 如果您的数据收集服务器与您网站的域相同，则Cookie是第一方。
   * 如果不匹配，则Cookie为第三方。 如果第三方Cookie被阻止，Adobe会设置一个回退Cookie (`s_fid`)，而不是常规的Cookie。

为确保您的收藏集服务器与您网站的域相匹配，您可以使用&#x200B;**CNAME设置**。 这涉及更新您的DNS设置以将自定义域（您拥有）指向Adobe服务器。 这会使跟踪Cookie显示为第一方。 虽然一个CNAME可以跨多个域工作，但任何与CNAME不匹配的域仍会设置第三方Cookie。

>[!NOTE]
>
>Apple的智能防跟踪(ITP)功能会限制Adobe的第一方Cookie的持续时间，即使您的收集域与网站域匹配也是如此。 ITP会影响macOS上的Safari以及iOS和iPadOS上的所有浏览器。 自2020年11月起，使用CNAME设置的Cookie与使用JavaScript设置的Cookie一样快速过期。 此时间限制将来可能会更改。

以下是文本的简化版本：

## Cookie 和隐私

Adobe非常重视隐私和数据安全。 它可与隐私组织、监管机构以及AdChoices等程序合作，让用户能够控制其数据的使用方式。

Adobe Experience Cloud中的大多数Cookie不存储个人信息。 它们是安全的，仅供您的公司用于报表、内容和广告。 除匿名、行业范围的报表(如Digital Marketing Insight报表)外，Adobe不与其他客户或第三方共享此数据。

Adobe不会合并跨不同公司的浏览器数据。 为了保护隐私，某些Adobe工具允许每个网站使用自己的一组Cookie。 有些服务器还允许使用您自己的域来执行Cookie，使其成为第一方且更加安全。

Cookie只能存储之前在其中保存的信息。 他们无法在您的设备上运行代码或读取其他数据。 此外，Web浏览器仅允许设置它们的网站读取Cookie。 例如，只有Adobe.com可以读取它设置的Cookie。

下图说明了标准图像请求的 Cookie 用法：

![标准图像请求的 Cookie 用法](assets/CookiesProcessGraphic-01.png)

下图说明了直接图像请求（在未加载 JS 文件的情况下使用）的 Cookie 用法：

![直接图像请求的 Cookie 用法](assets/CookiesProcessGraphic2.png)
