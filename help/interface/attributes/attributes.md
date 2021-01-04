---
description: 了解Adobe Experience Cloud的客户属性服务以及如何上传数据以用于分析和目标。
keywords: core services;Customer Attributes; Adobe Experience Cloud; Analytics; Target
solution: Experience Cloud
title: '如何使用客户属性 '
uuid: 1621402d-990f-46f9-981a-473280559069
translation-type: tm+mt
source-git-commit: 3f26c1af19a0838913eec2b4135304f5f3fcf0b4
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 79%

---


# 如何在Adobe Experience Cloud使用客户属性

Adobe Experience Cloud的客户属性允许您从客户关系管理(CRM)数据库上传捕获的企业数据。 您可以将数据上传到Experience Cloud中的客户属性数据源，然后使用Adobe Analytics和Adobe Target的数据。

要找到此功能，请导航到&#x200B;**[!DNL Experience Platform]** > **[!UICONTROL People]** > **[!UICONTROL Customer Attributes]**

![](assets/custom_reports.png)

## 上传客户属性的先决条件 {#section_BD38693AFBF34926BA28E964963B4EA0}

* **解决方案启用：**[为 Experience Platform 服务启用解决方案](../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C)。

* **群组成员资格：**&#x200B;要上传客户属性数据，用户必须是[客户属性群组](../admin-getting-started/admin-getting-started.md#task_3295A85536BF48899A1AB40D207E77E9)的成员。此外，您还必须属于 Adobe Analytics 群组或 Adobe Target 群组。

   要了解您的公司是否具有客户属性的访问权限，您的 [!DNL Experience Cloud] 管理员应当登录到 [Experience Cloud](https://experience.adobe.com)。导航到&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL Admin Console]** > **[!UICONTROL 产品]**。如果“客户属性”**&#x200B;显示为其中一个[!UICONTROL 产品配置文件]，则表示您已经可以开始。

   添加到客户属性的用户将在 Experience Cloud 界面的左侧看到“[!UICONTROL 客户属性]”菜单项。

* 客户属性需要使用 **Adobe Target** `at.js`（任何版本）或者 `mbox.js` 版本 58 或更高版本。

   请参阅[如何部署 at.js](https://docs.adobe.com/content/help/zh-Hans/target/using/implement-target/client-side/deploy-at-js/how-to-deployatjs.html) 或 [Mbox.js 实施](https://docs.adobe.com/content/help/zh-Hans/target/using/implement-target/client-side/mbox-implement/mbox-download.html)。

## 什么是企业客户数据？{#section_6F34C29F11414842AA57D2B1248FA3C6}

企业数据保留在其他系统中。企业数据十分复杂，而且对于不同的人员具有不同的意义。此数据可以包括成员资格、忠诚度、年龄、性别、拥有的产品、兴趣和存留期值等信息。

下图是一个数据文件的示例，该文件显示了产品的订阅者数据，包括成员 ID、授权产品、最新推出的产品等等。

![](assets/01_crs_usecase.png)

创建数据文件后，您可以将其上传到您在 **[!UICONTROL Experience Cloud]** > **[!UICONTROL 客户属性]**&#x200B;中创建的客户属性来源。

请参阅[上传客户属性数据](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78)，以了解此工作流程。

## {#section_4E77650F6CEE4C4ABCD0B3221A5AE5D9}分析和目标中的客户属性示例

数据保留在 Experience Cloud 中后，您可以对其进行自定义，并将其共享给报表、分段、活动和促销活动等解决方案。

例如：

| 解决方案 | 优势和用例 |
|--- |--- |
| Adobe Analytics | 营销人员和分析人员可以了解：<ul><li>对黄金级客户最有效的在线促销活动。</li><li>黄金级客户搜索的产品与白金级客户搜索的产品。</li><li>重新设计网站是否对老客户的转化率产生积极影响。</li><li>对存留期值较低的客户来说，更喜欢研究我网站上的哪些产品。</li></ul> |
| Adobe Target | 属性数据使 Adobe Target 用户能够：<ul><li>向忠诚俱乐部成员显示特价折扣和优惠。</li><li>向您的奢侈品客户推荐更昂贵的产品。</li><li>对于已收到电子邮件的客户，在通常为电子邮件注册所保留的空间中显示追加销售选件</li></ul> |
