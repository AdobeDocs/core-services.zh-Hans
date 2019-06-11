---
description: 将 Analytics 受众区段发布到 Experience Cloud 和 Adobe Target，以便开展受众市场营销活动。
keywords: 核心服务
seo-description: 将 Analytics 受众区段发布到 Experience Cloud 和 Adobe Target，以便开展受众市场营销活动。
seo-title: 发布 Analytics 受众区段
solution: Experience Cloud
title: 发布 Analytics 受众区段
uuid: 4201dc22-4b79-457c-a614-949bba08617
translation-type: tm+mt
source-git-commit: 85879d92104d8b6d739fb4d17dc8cfb7483a9343

---


# 发布 Analytics 受众区段

将 Analytics 受众区段发布到 Experience Cloud 和 Adobe Target，以便开展受众市场营销活动。

1. 在 Analytics 中[创建区段](https://marketing.adobe.com/resources/help/en_US/analytics/segment/seg_build.html)。
1. 在区段生成器上，启用将此 **[!UICONTROL 设置为Experience Cloud受众]** 选项。

   ![](assets/ec_audience_example.png)

   | 元素 | 描述 |
   |--- |---|
   | 使其成为 Experience Cloud 受众（适用于 &lt;报表包名称&gt;） | 将此区段发布到 Experience Cloud。您可以将受众用于 Adobe Target 中的市场营销活动和 Audience Manager 中的区段。<br>对于要发布的区段，必须填写其标题和描述字段。<br>在启用此选项后，会共享标题和受众区段定义，但不共享实际数据。当该受众与 Target 中的某个活动关联时，Analytics 将开始发送具有 Experience Cloud 和 Target 受众资格的访客的 ID。此时，受众名称和相应的数据开始显示在“Experience Cloud 受众”页面中。<br>从Analytics共享到Experience Cloud的受众不能超过200万个受众成员。<br>由于缓存，Analytics中已删除的报告套件需要12小时才能在Experience Cloud中显示删除。<br>在 Analytics 中，您可以编辑或删除已经发布的区段。如果区段正在使用，会在您编辑区段时给出一条警告消息。您无法删除一个已发布且 Adobe Target 正在使用的区段。<br>当访客符合从Analytics共享的受众资格后，在Target、Advertising Cloud和Campaign中可操作的时间有24-48小时延迟。<br>**数据保密受众**<br>不会根据访客身份验证状态过滤。如果访客可在未验证或已验证的状态下浏览您的站点，则访客在处于未验证状态时执行的操作仍会导致访客被包含在受众中。请参阅 [Analytics 隐私概述](https://marketing.adobe.com/resources/help/en_US/reference/?f=c_Privacy_Overview)，以了解受众共享对隐私的全部影响。 |
   | 选择用于创建受众的窗口 | 请注意，这是一个 **活络的** 时间窗口，而不是一个固定窗口。 |

1. 单击 **[!UICONTROL “保存]**”。
1. 访问 [!DNL Adobe Target]，单击 [!UICONTROL 受众]。
1. 在 [!UICONTROL “受众] ”页面上，找到从Experience Cloud中获取的受众。

   这些受众可在活动中使用。
