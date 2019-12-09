---
description: 有关将客户属性上传到 Experience Cloud 的概述和先决条件。
keywords: core services;customer attributes
seo-description: 有关将客户属性上传到 Experience Cloud 的概述和先决条件。
seo-title: 客户属性
solution: Experience Cloud
title: 客户属性
uuid: 1621402d-990f-46f9-981a-473280559069
translation-type: tm+mt
source-git-commit: ae97db27349940a8df7ee2ba6678683f57585678

---


# 客户属性

## 概述

要找到[!UICONTROL 客户属性]，导航到 **[!DNL Experience Platform]** &gt; **[!UICONTROL 人员]** &gt; **[!UICONTROL 客户属性]**

如果您在客户关系管理 (CRM) 数据库中捕获到企业客户数据，则可以将该数据上传到 Experience Cloud 中的客户属性数据源。上传后，即可利用 [!DNL Adobe Analytics] 和 [!DNL Adobe Target] 中的数据。

![](assets/custom_reports.png)

## 上传客户属性的先决条件 {#section_BD38693AFBF34926BA28E964963B4EA0}


* **解决方案启用：**[为核心服务启用解决方案](../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C)。

* **群组成员资格：**&#x200B;要上传客户属性数据，用户必须是[客户属性群组](../admin-getting-started/admin-getting-started.md#task_3295A85536BF48899A1AB40D207E77E9)的成员。此外，您还必须属于 Adobe Analytics 群组或 Adobe Target 群组。

   要知道您的公司是否具有客户属性的访问权限，您的 [!DNL Experience Cloud] 管理员应当登录到 [!DNL Experience Cloud]。导航到&#x200B;**[!UICONTROL 管理]** &gt; **[!UICONTROL 启动 Admin Console]** &gt; **[!UICONTROL 群组]**。如果&#x200B;*客户属性*&#x200B;显示为其中一个群组，则表示您已经可以开始。

   添加到客户属性群组的用户将在 Experience Cloud 界面的左侧看到“[!UICONTROL 客户属性]”菜单项.

* **Target mbox：**&#x200B;客户属性需要安装 mbox.js 版本 58 或更高版本。


   请参阅 [Mbox.js 实施](https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/mbox-implement/mbox-download.html)。

* **at.js：**&#x200B;任何版本。

## 什么是企业客户数据？{#section_6F34C29F11414842AA57D2B1248FA3C6}

企业数据留存于其他系统中。它可能非常复杂，对不同的人意义各不相同。此数据可包含成员资格、忠诚级别、年龄、性别、拥有的产品、兴趣和生命周期价值等信息。

以下图像是一个数据文件示例，它显示了产品的订阅者数据，包括成员 ID、有权限的产品、启动最多的产品等等。

![](assets/01_crs_usecase.png)

创建数据文件后，您可以将其上传到您在 **[!UICONTROL Experience Cloud]** &gt; **[!UICONTROL 客户属性]**&#x200B;中创建的客户属性来源。

请参阅[上传客户属性数据](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78)，以了解此工作流程。

## 解决方案用例 {#section_4E77650F6CEE4C4ABCD0B3221A5AE5D9}

在数据留存于 Experience Cloud 中后，您可以对数据进行自定义，并将其共享到解决方案，以用于报告、分段、活动和营销活动。

例如：

| 解决方案 | 优点和用例 |
|--- |--- |
| Adobe Analytics | 营销人员和分析人员可以了解：<ul><li>对于黄金级客户最为有效的在线营销活动。</li><li>黄金级客户搜索的产品与白金级客户搜索的产品。</li><li>重新设计的站点是否会对老客户的转化率产生积极影响。</li><li>具有较低生命周期价值的客户一般会在我的站点上搜索哪些产品。</li></ul> |
| Adobe Target | 通过属性数据，Target 用户可以：<ul><li>向忠诚的会籍成员显示特价折扣和优惠。</li><li>向奢华型客户推荐更加昂贵的产品。</li><li>对于已收到电子邮件的客户，在通常为电子邮件注册而保留的空区内，显示追加销售优惠。</li></ul> |
