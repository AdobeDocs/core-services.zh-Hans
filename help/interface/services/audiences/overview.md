---
title: '[!DNL Audience Library]'
description: 了解如何在CX Enterprise [!DNL Audience Library]中管理将访客数据转换为受众分段。
solution: Experience Cloud
type: Documentation
uuid: 92faf3a8-1375-4e32-905b-74cad48144d3
feature: Audience Library
topic: Administration
role: Admin
level: Experienced
exl-id: 1c6e54ac-4886-46ed-9df7-201d2df31847
TQID: https://experienceleague.adobe.com/QEAfCWPNI-JhDw-HjZwBGv0TlqyctIqSwz8eVQqS6Gg
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
  - id: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: ff2b9b37-92e0-45fc-b853-379d44c08c89
source-git-commit: 50012e2564e88e1a6e16578e3331136c7df0cb21
workflow-type: tm+mt
source-wordcount: 760
ht-degree: 44%

---

# CX企业版受众

[!DNL Audience Library]显示CX Enterprise中的受众。 受众是访客的集合（[!DNL CX Enterprise] ID 列表）。 您可以管理访客数据到受众细分的转换。 因此，创建和管理受众与创建和使用区段类似。 您还可以将受众区段共享到 [!DNL CX Enterprise] 中的产品和服务。

![CX Enterprise受众](assets/audiences.png)

受众可从各种来源创建或派生，如：

* 在[!DNL CX Enterprise]中创建的新受众
* 发布到[!DNL CX Enterprise]的[!DNL Analytics]区段
* [!DNL Audience Manager]

**实时与历史受众比较**

所有受众，无论其来源如何，都可供实时定位用例访问。 但是，从 Analytics 共享到 Audience Manager 的受众不可供实时定位访问。 系统将以两种方式评估受众：

* 每四小时对 Analytics 的历史受众评估一次。 处理和共享的总时间最长可能需要八小时。 历史受众始终包括回访访客。
* 实时受众源于CX Enterprise Audiences并且是实时评估的。

## 应用程序如何使用受众

下表介绍了受众在CX企业应用程序中的使用方式：

| 解决方案 | 描述 |
| --- | --- |
| CX Enterprise 受众 | 使用受众库在本地创建、管理和共享受众。 您可以：<ul><li>通过原始Analytics属性使用实时受众。</li><li>合并受众以创建复合受众，从而将实时数据和历史数据连接起来。</li><li>查看预计受众规模的图形视图。</li></ul><br>有关要创建哪种受众类型的建议，请参阅[受众创建选项](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html?lang=zh-Hans)。 |
| Analytics | 在分段中，您可以构建区段，将其与报表包组合，然后将该区段发布到CX Enterprise。 发布区段会将该区段显示在CX Enterprise的[!DNL Audience Library]页面上。 （有关详细信息，请参阅[!DNL Analytics]帮助中的[将区段发布到CX Enterprise](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-publish.html?lang=zh-Hans)。） 该受众还可用作由[!DNL Adobe Target]提供的营销活动体验以及[!DNL Audience Manager]中的目标受众。 在您从[!DNL Adobe Analytics]共享受众并选择该受众以在活动的营销活动中使用后，过去90天内符合区段定义条件的访客资料将被发送到[!UICONTROL 受众服务]。 共享受众数量的限制已增加到 75 个。 从[!DNL Analytics]共享到CX Enterprise的受众数量不能超过2000万个独特成员。 另外，由于缓存，在Analytics中删除报表包12小时后，该删除操作才能反映在CX Enterprise中。 |
| Mobile Services | 使用[!UICONTROL 设备类型]报表中的环状层次图可视化图表分析移动流量。 |
| [!DNL Target] | 利用 [ID 服务](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=zh-Hans)将访客 ID 和数据统一到单个可操作的轮廓中，以供在应用程序间使用。 在Adobe Analytics中创建区段的过程中显示的[!UICONTROL 发布到CX Enterprise]复选框允许该区段在Adobe Target的自定义受众库中可用。 在 [!DNL Analytics] 或 [!DNL Audience Manager] 中创建的区段可用于 [!DNL Target] 中的活动。 例如，您可以根据 [!DNL Analytics] 转化量度和在 [!DNL Analytics] 中创建的受众区段，来创建营销活动。 |
| [!DNL Audience Manager] | 共享受众在 [!DNL Audience Manager] 分段中可用。 所有CX Enterprise受众均可在[!DNL Audience Manager]中以本机方式使用，这提供了：<ul><li>关于如何在应用程序工作流程中共享和使用受众的内置自动化功能</li><li>非现场目标</li><li>相似建模</li></ul> |
| 促销活动 | <ul><li>将共享受众从不同的Adobe CX Enterprise应用程序导入到Adobe Campaign中。</li><li>以共享受众的形式导出收件人列表。 这些共享受众可在您使用的其他Adobe CX Enterprise应用程序中使用。</li></ul> |
| Advertising Cloud | 将受众用作目标。 |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>在访客有资格成为从 Analytics 共享的受众后，该信息需经过 4 - 8 小时的延迟，才能在 [!DNL Target]、Ad Cloud 和 Campaign Standard 中使用。

## 受众库界面元素

[!DNL CX Enterprise]提供了一个用于创建和管理受众的库，并具有实时的本地受众识别。

**[!UICONTROL CX Enterprise]** > **[!UICONTROL Experience Platform]** > **[!UICONTROL 人员]** > **[!UICONTROL 受众库]**

![在受众库中添加受众](assets/audience_library.png)


| 元素 | 描述 |
| --- | --- |
| 新建 | [创建受众](https://experienceleague.adobe.com/zh-hans/docs/core-services/interface/services/audiences/create)。 |
| 标题和描述 | 列标题，用于识别和描述受众。 |
| 作者 | 创建受众区段的人员。 |
| 来源 | 标识创建受众的位置。<ul><li>**Analytics：**&#x200B;在Adobe Analytics中创建的区段，然后发布到CX Enterprise。</li><li>**CX Enterprise：**&#x200B;在CX Enterprise Audiences[&#128279;](https://experienceleague.adobe.com/zh-hans/docs/core-services/interface/services/audiences/create)中创建的新受众。</li><li>**Audience Manager：** Audience Manager创建的受众自动显示在CX Enterprise Audiences中。</li></ul> |
| 当前数量 | 当前受众数量。 |
| 活动 | 区段的活动状态。 |

{style="table-layout:auto"}

## 从Adobe Analytics发布受众

有关详细信息，请参阅Adobe Analytics文档中的[将区段发布到CX Enterprise](https://experienceleague.adobe.com/zh-hans/docs/analytics/components/segmentation/segmentation-workflow/seg-publish)。
