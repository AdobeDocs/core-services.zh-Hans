---
description: 管理访客数据到受众区段的转换。
seo-description: 管理访客数据到受众区段的转换。
seo-title: 受众
solution: Experience Cloud
title: 受众
uuid: 92faf3a8-1375-4e32-905b-74cad48144d3
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# 受众{#topic_679810123CAA4E0CA4FA3417FB0100C7}

受众是访客(列表ID)的集合。 Adobe的受众服务管理将访客数据转换为受众细分。 因此，创建和管理受众与创建和使用区段类似，只是前者增加了一项将受众区段共享到 [!DNL Experience Cloud] 的功能。

![](assets/audiences.png)

受众可从各种来源创建或派生，如：

* 在 [!DNL Experience Cloud] 中创建的新受众
* 从发布到 [!DNL Analytics] 的 [!DNL Experience Cloud] 区段
* 从 [!DNL Audience Manager]

**实时与历史受众比较**

所有受众，无论其来源如何，都可供实时定位用例访问。但是，从 Analytics 到 Audience Manager 共享的受众不可供实时定位访问。系统以两种方式评估受众:

* Analytics的历史受众每4小时评估一次。 处理和共享的总时间最长可能需要8小时。  历史受众始终包括退货访客。
* 实时受众源于 Experience Cloud 受众并接受实时评估。

## 解决方案如何使用受众 {#concept_01EB9345C5344597BC94A864EDD38EE1}

下表介绍了受众在Experience Cloud解决方案中的使用方式：

| 解决方案 | 描述 |
|--- |--- |
| Experience Cloud 受众 | 使用[受众库](../audience-library/audience-library.md)界面在本地创建、管理和共享受众。您可以：<ul><li>使用原始分析属性实时受众</li><li>合并受众以创建复合数据，并结合实时和历史数据</li><li>查看估计视图大小的图形受众</li></ul><br>有关要创建的受众类型的建议，请参阅： [Experience Cloud受众](https://helpx.adobe.com/marketing-cloud-core/kb/People/Audience-Creation-Options.html)。 |
| Analytics | 在细分中，您可以构建区段，将其与报表包组合，然后 [将区段发布到Experience Cloud](../audience-library/audience-library.md)。 发布区段会使其显示在[受众](../audience-library/audience-library.md)页面上。该受众还会作为一个目标受众在以下两个位置可用：Adobe Target 提供的营销活动体验中，以及在 Audience Manager 中。Once an audience is shared from Analytics, and selected for use in an active campaign, all the visitor profiles who met the segment definition criteria for the past 90 days are sent to the Experience Cloud [!UICONTROL Audience Services] platform. 共享受众的限制已增加到75个。 从Analytics共享到Experience Cloud的受众不能超过2000万个唯一成员。 此外，由于缓存，在Analytics中删除的报表包需要12小时才能在Experience Cloud中显示删除。 |
| Mobile Services | 使用“设备类型”报告中的日暴流可视化 [!UICONTROL 分析移动流量] 。 |
| [!DNL Target] | The [ID service](https://docs.adobe.com/content/help/en/id-service/using/home.html) unifies visitor IDs and data into a single, actionable profile for use across solutions. 在 Adobe Analytics 的区段创建过程中显示的[发布到 Experience Cloud](../audience-library/audience-library.md) 复选框，允许该区段在 Adobe Target 的自定义受众库中可用。A segment created in Analytics or Audience Manager can be used for activities in  [!DNL Target].  例如，你可以根据 Analytics 转化量度和 Analytics 中创建的受众区段，来创建营销活动。 |
| Audience Manager | 共享受众在受众管理器细分中可用。 所有 Experience Cloud 受众均可在 Audience Manager 本地使用，Audience Manager 提供了以下功能：<ul><li>关于如何在解决方案工作流中共享和使用它们的内置自动化功能</li><li>非现场目标</li><li>相似建模</li></ul> |
| Campaign | <ul><li>将从不同 Adobe Experience Cloud 解决方案共享的受众导入到 Adobe Campaign。</li><li>以共享收件人的形式导出受众列表。 这些共享受众可用于您使用的不同Adobe Experience Cloud解决方案。</li></ul> |
| Media Optimizer | 将受众用作目标。 |

>[!IMPORTANT]
>
>Once a visitor qualifies for the audience shared from Analytics, there is a 4-8 hour delay before that information is actionable in [!DNL Target], Ad Cloud, and Campaign Standard.

## 更多帮助 - 问题、指导和用例 {#section_C7F151644D8A45F7B6FC54F58845635D}

| 帮助 | 资源 |
|--- |--- |
| 找不到受众? | 确保已配置您。 See [Getting started - enable your solutions for core services](../core-services/core-services.md).<br>单击 [此处](https://www.adobe.com/go/audiences) ，请求访问用户档案和受众（集成供应表单）。 |
| 用例 | 有关使用哪种解决方案的更多指导，请访问知识 [库中的受众创建选项](https://helpx.adobe.com/marketing-cloud-core/kb/People/Audience-Creation-Options.html) 。 |
| 论坛 | The [Audiences forum](https://forums.adobe.com/community/experience-cloud/platform/core-services/people-service/audiences) is an additional resource to get help with audiences. |

## 受众库界面元素 {#section_D04ACEF61CEF4B189AE6BA9F40D0DBF4}

[!DNL Experience Cloud] 提供了一个供创建和管理受众的库，且使用的是实时的本地受众识别。

**[!UICONTROL Experience Cloud]** > **[!UICONTROL Experience Platform]** >人 **[!UICONTROL 员]** > **[!UICONTROL 受众库]**

![](assets/audience_library.png)

| 元素 | 描述 |
|--- |--- |
| 新建 | [创建受众](../audience-library/audience-library.md). |
| 标题和描述 | 列标题，用于识别和描述受众。 |
| 作者 | 创建受众区段的人员。 |
| 源 | 标识受众的创建位置。<ul><li>**Analytics：**&#x200B;在 Reports &amp; Analytics 或 Ad Hoc Analysis 中创建，然后[发布到 Experience Cloud](../audience-library/audience-library.md) 的区段。</li><li>**Experience Cloud：**&#x200B;新受众[在 Experience Cloud 受众中创建](../audience-library/audience-library.md)。</li><li>**Audience Manager：**&#x200B;由 Audience Manager 创建的受众自动显示在 Experience Cloud 受众中。</li></ul> |
| 当前大小 | 当前受众大小。 |
| 活动 | 区段的活动状态。 |
