---
description: 了解如何在 Experience Cloud 中使用属性规则来创建受众和定义组合受众。
keywords: core services
seo-description: 了解如何在 Experience Cloud 中使用属性规则来创建受众和定义组合受众。
seo-title: 创建受众
solution: Experience Cloud
title: 创建受众
uuid: 7e622539-296e-4ff3-93b0-ec1c08b35429
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# 创建受众

了解如何在 Experience Cloud 中使用属性规则来创建受众和定义组合受众。

本文帮助您了解如何：

* 创建受众
* 创建规则
* 使用规则定义复合受众

下图表示复合受众中的两个规则。

![](assets/audience_sharing.png)

每个圈子都表示定义受众会员资格的规则。 在两个访客规则中符合成员资格的受众会重叠，以成为复合的、定义的受众。

>[!NOTE]
>
>在完成指定期限的数据收集以后，受众会得到完全定义。以下示例演示如何为复合受众创建规则。 本受众包括：

* “主页和花园”部分源自页面数据或原始分析数据。
* 来源于[发布](../audience-library/audience-library.md#task_32FEEFE0B32E4E388CD4D892D727282A)到 [!DNL Experience Cloud] 的 [!DNL Adobe Analytics] 区段的 Chrome 和 Safari 用户。

   ![](assets/audience_create.png)

1. In the [!DNL Experience Cloud], under [!DNL Experience Platform], click **[!UICONTROL People]** > **[!UICONTROL Audience Library].**
1. On the [!UICONTROL Audiences] page, click **[!UICONTROL New]**. ![](assets/add_icon_small.png)

   ![步骤结果](assets/audience_create_new.png)

1. 在[!UICONTROL 创建新受众]页面，指定标题和描述。
1. 在[!UICONTROL 规则]下，选择一个属性来源：

   * **[!UICONTROL 实时 Analytics 数据：]**（或原始数据)此类数据是指从实时 Analytics 图像请求派生而来的属性数据，包括 eVar 和事件等数据。使用此属性来源时，必须选择一个报表包，并定义要包含的维或事件。 此报表包选择提供了报表包使用的变量结构。
   >[!NOTE]
   >
   >由于缓存，在 Analytics 中删除报表包 12 小时后，该删除操作才能反映在 Experience Cloud 中。

   * **[!UICONTROL Experience Cloud：]**&#x200B;从 [!DNL Experience Cloud] 来源派生的属性数据。例如，这可以是您在 [!DNL Analytics] 中创建的受众区段的数据，也可以是来自 [!DNL Audience Manager] 的数据。

1. 定义受众规则，然后单击 **[!UICONTROL 保存]。**

>[!NOTE]
>
>您在定义受众规则时，应该对实施变量有所了解。

在[!UICONTROL 规则]下，定义 *`Home & Garden`* 属性选择：

* **[!UICONTROL 属性来源：]**&#x200B;原始 Analytics 数据
* **[!UICONTROL 报表包：]**&#x200B;报表包 31
* Dimension = **[!UICONTROL Store (Merch) (v6)]** > **[!UICONTROL Equals]** > **[!UICONTROL Home &amp; Garden]**

![](assets/home_garden.png)

*Chrome 和 Safari 访客*&#x200B;是从 Analytics 中共享的受众区段：

* **[!UICONTROL 属性来源：]** Experience Cloud
* **[!UICONTROL 维度：]** Chrome 和 Safari 访客

![](assets/chrome_safari.png)

要进行比较，需要添加 *OR* 规则查看某个站点区域（例如庭院和家具）的所有访客。

![](assets/audiences_rule_patio.png)

生成的规则是由访问Home &amp; Garden的Chrome和Safari用户组成的定义受众。 天井和家具部分提供对访问该站点部分的所有访客的更多洞察。

![](assets/defined_audience.png)

* **历史估计：**（虚线圈）代表基于 [!DNL Analytics] 数据创建的规则。
* **实际受众:** （实心圆）从受众管理器创建的具有30天数据的任何规则。 当受众管理器数据达到30天时，该行将变为实线并表示实际数字。

在指定时间段内完成数据收集后，圈子组合显示定义的受众。

保存受众后，它便可用于其他解决方案。 例如，您可以在Adobe受众活动中包含共享目标。
