---
title: 关于 [!DNL Customer Attributes]
description: 了解 Experience Cloud 中的  [!DNL Customer Attributes] 了解如何上传客户属性数据，以便在 Adobe Analytics 和 Adobe Target 中使用。
solution: Experience Cloud,Target,Analytics
feature: Customer Attributes
role: Admin
topic: Administration
level: Experienced
exl-id: fe8ad013-76da-49f8-aa51-dc5f6c1b1d79
source-git-commit: 27b9b789e0d4c448105f5acec3aa05c9404443bf
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 63%

---

# Experience Cloud 中的 [!DNL Customer Attributes]

**[!UICONTROL Apps]** ![菜单](assets/menu-icon.png) > **[!DNL Customer Attributes]**

Experience Cloud 中的 [!DNL Customer Attributes] 允许您上传从客户关系管理 (CRM) 数据库中捕获的企业数据。您可以[将数据](t-crs-usecase.md)上传到Experience Cloud中的[!DNL Customer Attributes]数据源，然后在[!DNL Adobe Analytics]和[!DNL Adobe Target]中使用这些数据。

![客户属性概述](assets/custom_reports.png)

## 关于企业客户数据 {#customer-data}

企业客户数据是指收集到的有关客户、潜在客户和合作伙伴的全组织范围的信息。它驻留在其他系统上，可以包括成员资格、忠诚度、年龄、性别、拥有的产品、兴趣和存留期值等信息。

下图是&#x200B;_数据文件_&#x200B;的一个示例，该文件显示了产品的订阅者数据，包括成员ID、授权产品、最常启动的产品等。

![企业客户数据是什么？](assets/01_crs_usecase.png)

创建数据文件后，您可以将其上传到您在&#x200B;**[!UICONTROL Experience Cloud]** > **[!UICONTROL Customer Attributes]**&#x200B;中创建的客户属性来源。

请参阅[上传客户属性数据](t-crs-usecase.md)以了解此工作流。

## Analytics 和 Target 中客户属性的示例

数据保留在 Experience Cloud 中后，您可以对其进行自定义，并将其共享给报表、分段、活动和促销活动等解决方案。

例如：

| 解决方案 | 优势和用例 |
|--- |--- |
| Adobe Analytics | 营销人员和分析人员可以了解：<ul><li>对黄金级客户最有效的在线促销活动。</li><li>黄金级客户搜索的产品与白金级客户搜索的产品。</li><li>重新设计网站是否对老客户的转化率产生积极影响。</li><li>存留期值较低的客户更喜欢在我网站上研究的产品。</li></ul> |
| Adobe Target | 属性数据使 Adobe Target 用户能够：<ul><li>向忠诚俱乐部成员显示特价折扣和产品建议。</li><li>向您的奢侈品客户推荐更昂贵的产品。</li><li>对于已收到电子邮件的客户，在通常为电子邮件注册所保留的空间中显示追加销售产品建议</li></ul> |

{style="table-layout:auto"}
