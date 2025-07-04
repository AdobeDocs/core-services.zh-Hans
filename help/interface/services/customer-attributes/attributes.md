---
title: '[!DNL Customer attributes]'
description: 了解 Experience Cloud 中的  [!DNL customer attributes] 了解如何上传客户属性数据，以便在 Adobe Analytics 和 Adobe Target 中使用。
solution: Experience Cloud,Target,Analytics
feature: Customer Attributes
role: Admin
topic: Administration
level: Experienced
exl-id: fe8ad013-76da-49f8-aa51-dc5f6c1b1d79
source-git-commit: 361175f290d73f1637673420700874a2415e3fca
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 78%

---

# Experience Cloud 中的 [!DNL Customer attributes]

Experience Cloud 中的 [!DNL Customer attributes] 允许您上传从客户关系管理 (CRM) 数据库中捕获的企业数据。您可以将数据上传到 Experience Cloud 中的客户属性数据源，然后在 [!DNL Adobe Analytics] 和 [!DNL Adobe Target] 中使用这些数据。

## 找到 [!DNL customer attributes] 功能

1. 登录到[!DNL Experience Cloud]并选择菜单![菜单](assets/menu-icon.png)图标。

1. 选择&#x200B;**[!UICONTROL 客户属性]**。

![客户属性概述](assets/custom_reports.png)

## 上传 [!DNL customer attributes] 的先决条件 {#prerequisites}

* **组成员资格：**&#x200B;要上传客户属性数据，用户必须是客户属性组的成员。 此外，您还必须属于 Adobe Analytics 群组或 Adobe Target 群组。

  要知道您的公司是否具有客户属性的访问权限，您的[!DNL Experience Cloud]管理员应登录到[Experience Cloud](https://experience.adobe.com)。 导航到&#x200B;**[!UICONTROL Admin Console]** > **[!UICONTROL 产品]**。 如果 *[!DNL Customer Attributes]* 显示为其中一个[!UICONTROL 产品轮廓]，则表示您已经可以开始。

  添加到 [!DNL Customer Attributes] 的用户将在 Experience Cloud 界面的左侧看到[!UICONTROL 客户属性]菜单项。

* 客户属性需要使用 **Adobe Target**`at.js`（任何版本）或 `mbox.js` 版本 58 或更高版本。

  参阅[如何部署 at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/overview.html?lang=zh-Hans)。

## 企业客户数据是什么？ {#enterprise_data}

企业数据保留在其他系统中。企业数据十分复杂，而且对于不同的人员具有不同的意义。此数据可以包括成员资格、忠诚度、年龄、性别、拥有的产品、兴趣和存留期值等信息。

下图是一个数据文件的示例，该文件显示了产品的订阅者数据，包括成员 ID、授权产品、最新推出的产品等等。

![企业客户数据是什么？](assets/01_crs_usecase.png)

创建数据文件后，您可以将其上传到您在&#x200B;**[!UICONTROL Experience Cloud]** > **[!UICONTROL 客户属性]**&#x200B;中创建的客户属性源。

请参阅[上传客户属性数据](t-crs-usecase.md)以了解此工作流。

## Analytics和Target中的客户属性示例 {#examples}

数据保留在 Experience Cloud 中后，您可以对其进行自定义，并将其共享给报表、分段、活动和促销活动等解决方案。

例如：

| 解决方案 | 优势和用例 |
|--- |--- |
| Adobe Analytics | 营销人员和分析人员可以了解：<ul><li>对黄金级客户最有效的在线促销活动。</li><li>黄金级客户搜索的产品与白金级客户搜索的产品。</li><li>重新设计网站是否对老客户的转化率产生积极影响。</li><li>存留期值较低的客户更喜欢在我网站上研究的产品。</li></ul> |
| Adobe Target | 属性数据使 Adobe Target 用户能够：<ul><li>向忠诚俱乐部成员显示特价折扣和产品建议。</li><li>向您的奢侈品客户推荐更昂贵的产品。</li><li>对于已收到电子邮件的客户，在通常为电子邮件注册所保留的空间中显示追加销售产品建议</li></ul> |

{style="table-layout:auto"}
