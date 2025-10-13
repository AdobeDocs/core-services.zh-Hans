---
title: 如何在受众库中创建受众
description: 了解如何在受众库中使用属性规则来创建可共享受众。 了解如何配置规则和定义复合受众。
solution: Experience Cloud
uuid: 7e622539-296e-4ff3-93b0-ec1c08b35429
feature: Audience Library
topic: Administration
role: Admin
level: Experienced
exl-id: b65a12f5-fa89-400a-b279-13c381cd6c22
source-git-commit: c98084e3960e40ae28e55050ce0727abce94ba0c
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 65%

---

# 创建受众

在[!UICONTROL 受众库]中，您可以使用属性规则来创建受众，并定义复合受众以便在Experience Cloud应用程序中共享。

本文可帮助您了解如何执行以下操作：

* 创建受众
* 创建规则
* 使用规则定义复合受众

下图表示复合受众中的两个规则。

![复合受众中的两个规则](assets/audience_sharing.png)

每个圆圈表示定义受众成员资格的规则。符合两个受众规则中的成员资格的访客会发生重叠，从而成为定义的复合受众。

>[!NOTE]
>
>在完成指定期限的数据收集后，将会对受众进行充分定义。

以下示例演示了如何为复合受众创建规则。此受众包括：

* 从页面数据或原始分析数据派生的“家居和园艺”部分。
* 从[!DNL Adobe Analytics]区段[发布的](overview.md)到[!DNL Experience Cloud]派生Chrome和Safari用户。

  ![为复合受众创建规则](assets/audience_create.png)

**创建受众**

1. 单击[!DNL Experience Cloud]个应用（![个应用图标](assets/apps-icon.png)），然后单击&#x200B;**[!UICONTROL 人员]** > **[!UICONTROL 受众库]。**

1. 在[!UICONTROL 受众]页面上，单击&#x200B;**[!UICONTROL 新建]**。 ![新受众](assets/add_icon_small.png)

   ![创建受众](assets/audience_create_new.png)

1. 在[!UICONTROL 创建新受众]页面上，完成&#x200B;**[!UICONTROL 标题]**&#x200B;和&#x200B;**[!UICONTROL 描述]**&#x200B;字段。
1. 在[!UICONTROL 规则]下，选择引用报表包，然后选择属性源：

   * **[!UICONTROL Real-Time Analytics数据：]**（或原始数据）这是从Real-Time Analytics图像请求派生的属性数据。 它包括eVar和事件。 使用此属性源时，必须选择一个报表包，并定义要包括的维度或事件。此报表包选择提供了报表包使用的变量结构。

   >[!NOTE]
   >
   >由于缓存，在Analytics中删除报表包12小时后，该删除操作才能反映在Experience Cloud中。

   * **[!UICONTROL Experience Cloud：]**&#x200B;属性数据派生自[!DNL Experience Cloud]源。 例如，这可以是您在 [!DNL Analytics] 中创建的受众区段的数据，也可以是来自 [!DNL Audience Manager] 的数据。

1. 定义受众规则，然后单击&#x200B;**[!UICONTROL 保存]。**

**示例：为复合受众定义规则**

>[!NOTE]
>
>您在定义受众规则时，应该对实施变量有所了解。

在[!UICONTROL 规则]下，定义 *`Home & Garden`* 属性选择：

* **[!UICONTROL 属性来源：]**&#x200B;原始 Analytics 数据
* **[!UICONTROL 报表包：]**&#x200B;报表包 31
* 维度 = **[!UICONTROL 商店 (Merch) (v6)]** > **[!UICONTROL 等于]** > **[!UICONTROL 家居和园艺]**

![受众库中的属性选择](assets/home_garden.png)

*Chrome 和 Safari 访客*&#x200B;是从 Analytics 中共享的受众区段：

* **[!UICONTROL 属性来源：]** Experience Cloud
* **[!UICONTROL 维度：]** Chrome 和 Safari 访客

![Chrome 和 Safari 访客](assets/chrome_safari.png)

要进行比较，需要添加 *OR* 规则查看某个站点区域（例如庭院和家具）的所有访客。

![受众的 OR 规则](assets/audiences_rule_patio.png)

由此产生的规则是由访问了“家居和园艺”的“Chrome 和 Safari 用户”组成的已定义受众。“庭院和家具”区段提供了有关访问该网站区域的所有访客的更多分析信息。

![Experience Cloud 中的已定义受众](assets/defined_audience.png)

* **历史估计：**（虚线圈）代表基于 [!DNL Analytics] 数据创建的规则。
* **实际受众：**（实心圆）创建的任何规则，其中包含来自 Audience Manager 的 30 天数据。当 Audience Manager 数据达到 30 天时，该行将变为实线并表示实际数字。

在指定的时间段内完成数据收集后，圆圈将合并起来以显示定义的受众。

保存受众后，它便可用于其他Experience Cloud应用程序。 例如，您可以在Adobe Target [活动](https://experienceleague.adobe.com/en/docs/target/using/activities/activities)中包含共享受众。
