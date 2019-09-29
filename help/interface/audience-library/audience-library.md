---
description: 管理访客数据到受众区段的转换。
seo-description: 管理访客数据到受众区段的转换。
seo-title: 受众
solution: Experience Cloud
title: 受众
uuid: 92faf3a8-1375-4e32-905b-74cad48144d3
translation-type: tm+mt
source-git-commit: f8b48077d936e289d66c1a93a96fe9ebaa4f0136

---


# 受众{#topic_679810123CAA4E0CA4FA3417FB0100C7}

受众是访客的集合（访客 ID 的列表）。Adobe 的受众服务可管理如何将访客数据转换至受众区段。因此，创建和管理受众与创建和使用区段类似，只是前者增加了一项将受众区段共享到 [!DNL Experience Cloud] 的功能。

![](assets/audiences.png)

受众可从各种来源创建或派生，如：

* 在 [!DNL Experience Cloud] 中创建的新受众
* 从发布到 [!DNL Analytics] 的 [!DNL Experience Cloud] 区段
* 从 [!DNL Audience Manager]

**实时与历史受众比较**

所有受众，无论其来源如何，都可供实时定位用例访问。但是，从 Analytics 到 Audience Manager 共享的受众不可供实时定位访问。系统通过以下两种方式评估受众：

* 源于 Analytics 的历史受众每 12 个小时接受一次评估。历史受众始终包含回访访客。
* 实时受众源于 Experience Cloud 受众并接受实时评估。


## 解决方案如何使用受众 {#concept_01EB9345C5344597BC94A864EDD38EE1}

下表说明了受众在 Experience Cloud 解决方案中的使用方式：

| 解决方案 | 描述 |
|--- |--- |
| Experience Cloud 受众 | 使用[受众库](../audience-library/audience-library.md)界面在本地创建、管理和共享受众。您可以：<ul><li>使用原始 analytics 属性的实时受众</li><li>加入实时和历史数据，合并受众以创建组合受众</li><li>请参阅预计受众大小的图示</li></ul><br>有关要创建的受众类型的建议，请参阅：[Experience Cloud 受众](https://helpx.adobe.com/marketing-cloud-core/kb/People/Audience-Creation-Options.html)。 |
| Analytics | 在分段中，您可以构建区段，将其与报表包合并，然后[将区段发布到 Experience Cloud](../audience-library/audience-library.md)。发布区段会使其显示在[受众](../audience-library/audience-library.md)页面上。该受众还会作为一个目标受众在以下两个位置可用：Adobe Target 提供的营销活动体验中，以及在 Audience Manager 中。从 Analytics 共享受众并选择该受众以在活动的营销活动中使用后，过去 90 天内所有符合区段定义标准的访客资料均会发送到 Experience Cloud 受众服务平台。重要提示：您必须将从 Analytics 共享的受众数量限制为 20，以避免额外的处理延迟。从 Analytics 共享到 Experience Cloud 的受众数量不能超过 2000 万个独特成员。另外，由于缓存，在 Analytics 中删除报表包 12 小时后，该删除操作才能反映在 Experience Cloud 中。 |
| Mobile Services | Analyze mobile traffic using the sunburst visualization in the [Device Types](https://marketing.adobe.com/resources/help/en_US/mobile/?f=reports_devices). |
| Target | [ID 服务](https://marketing.adobe.com/resources/help/en_US/mcvid/)将访客 ID 与数据合并为一份可操作的资料，以便在各个解决方案之间使用。在 Adobe Analytics 的区段创建过程中显示的[发布到 Experience Cloud](../audience-library/audience-library.md) 复选框，允许该区段在 Adobe Target 的自定义受众库中可用。在 Analytics 或 Audience Manager 中创建的区段可用于 Target 中的活动。例如，你可以根据 Analytics 转化量度和 Analytics 中创建的受众区段，来创建营销活动。 |
| Audience Manager | 共享受众可在 Audience Manager 区段中使用。所有 Experience Cloud 受众均可在 Audience Manager 本地使用，Audience Manager 提供了以下功能：<ul><li>内置的自动化，管理如何在解决方案工作流程中共享和使用这些受众</li><li>异地目标</li><li>相似建模</li></ul> |
| Campaign | <ul><li>将从不同 Adobe Experience Cloud 解决方案共享的受众导入到 Adobe Campaign。</li><li>以共享受众的形式导出收件人列表。这些共享受众可用于您所使用的不同 Adobe Experience Cloud 解决方案。</li></ul> |
| Media Optimizer | 将受众用作目标。 |


>[!IMPORTANT]
>
>在访客有资格成为从 Analytics 共享的受众后，该信息需经过 24 - 48 小时的延迟，才能在 Target、Media Optimizer 和 Campaign 中使用。

## 更多帮助 - 问题、指导和用例 {#section_C7F151644D8A45F7B6FC54F58845635D}


| 需要帮助的方面 | 资源 |
|--- |--- |
| 找不到受众？ | 确保已对您进行配置。请参阅[快速入门 - 为核心服务启用解决方案](../core-services/core-services.md)。<br>单击[此处](https://www.adobe.com/go/audiences)请求 Profiles &amp; Audiences（集成配置表单）的访问权限。 |
| 用例 | 有关应使用哪种解决方案的更多指导，请参阅知识库中的[受众创建选项](https://helpx.adobe.com/marketing-cloud-core/kb/People/Audience-Creation-Options.html)。 |
| 论坛 | [受众论坛](https://forums.adobe.com/community/experience-cloud/platform/core-services/people-service/audiences)是另外一个可获取受众相关帮助的资源。 |


## 受众库界面元素 {#section_D04ACEF61CEF4B189AE6BA9F40D0DBF4}

[!DNL Experience Cloud] 提供了一个供创建和管理受众的库，且使用的是实时的本地受众识别。

**[!UICONTROL Experience Cloud]** &gt; **[!UICONTROL Experience Platform]** &gt; **[!UICONTROL 人员]** &gt; **[!UICONTROL 受众库]**

![](assets/audience_library.png)

| 元素 | 描述 |
|--- |--- |
| 新建 | [创建受众](../audience-library/audience-library.md). |
| 标题和描述 | 列标题，用于识别和描述受众。 |
| 作者 | 创建受众区段的人。 |
| 来源 | 识别受众的创建位置。<ul><li>**Analytics：**&#x200B;在 Reports &amp; Analytics 或 Ad Hoc Analysis 中创建，然后[发布到 Experience Cloud](../audience-library/audience-library.md) 的区段。</li><li>**Experience Cloud：**&#x200B;新受众[在 Experience Cloud 受众中创建](../audience-library/audience-library.md)。</li><li>**Audience Manager：**&#x200B;由 Audience Manager 创建的受众自动显示在 Experience Cloud 受众中。</li></ul> |
| 当前大小 | 当前受众大小 |
| 活动 | 区段的活动状态。 |
