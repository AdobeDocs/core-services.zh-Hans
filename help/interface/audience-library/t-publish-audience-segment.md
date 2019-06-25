---
description: 将 Analytics 受众区段发布到 Experience Cloud 和 Adobe Target，以便开展受众市场营销活动。
keywords: 核心服务
seo-description: 将 Analytics 受众区段发布到 Experience Cloud 和 Adobe Target，以便开展受众市场营销活动。
seo-title: 发布 Analytics 受众区段
solution: Experience Cloud
title: 发布 Analytics 受众区段
uuid: 4201dc22-4b79-457c-a614-949bba087617
translation-type: ht
source-git-commit: 85879d92104d8b6d739fb4d17dc8cfb7483a9343

---


# 发布 Analytics 受众区段

将 Analytics 受众区段发布到 Experience Cloud 和 Adobe Target，以便开展受众市场营销活动。

1. 在 Analytics 中，[生成区段](https://marketing.adobe.com/resources/help/zh_CN/analytics/segment/seg_build.html)。
1. 在区段生成器中，启用 **[!UICONTROL 使其成为 Experience Cloud 受众]** 选项。

   ![](assets/ec_audience_example.png)

   | 元素 | 描述 |
   |--- |---|
   | 使其成为 Experience Cloud 受众（适用于 &lt;报表包名称&gt;） | 将此区段发布到 Experience Cloud。您可以将受众用于 Adobe Target 中的市场营销活动和 Audience Manager 中的区段。<br>对于要发布的区段，必须填写其标题和描述字段。<br>在启用此选项后，会共享标题和受众区段定义，但不共享实际数据。当该受众与 Target 中的某个活动关联时，Analytics 将开始发送具有 Experience Cloud 和 Target 受众资格的访客的 ID。此时，受众名称和相应的数据开始显示在“Experience Cloud 受众”页面中。<br>从 Analytics 共享到 Experience Cloud 的受众数量不能超过 2000 万个受众成员。<br>由于缓存，在 Analytics 中删除报表包 12 小时后，该删除操作才能反映在 Experience Cloud 中。<br>在 Analytics 中，您可以编辑或删除已经发布的区段。如果区段正在使用，会在您编辑区段时给出一条警告消息。您无法删除一个已发布且 Adobe Target 正在使用的区段。<br>在访客有资格成为从 Analytics 共享的受众后，该信息需经过 24 - 48 小时的延迟，才能在 Target、Advertising Cloud 和 Campaign 中使用。<br>**数据隐私**<br>受众并非基于访客的身份验证状态进行过滤。如果访客可在未验证或已验证的状态下浏览您的站点，则访客在处于未验证状态时执行的操作仍会导致访客被包含在受众中。查看 [Analytics 隐私概述](https://marketing.adobe.com/resources/help/zh_CN/reference/c_Privacy_Overview.html)，了解受众共享的全部隐私含义。 |
   | 选择用于创建受众的窗口 | 请注意，这是一个 **活络的** 时间窗口，而不是一个固定窗口。 |

1. 单击 **[!UICONTROL 保存]**。
1. 访问 [!DNL Adobe Target]，单击[!UICONTROL 受众]。
1. 在[!UICONTROL 受众]页面上，找到来源于 Experience Cloud 的受众。

   这些受众可在活动中使用。
