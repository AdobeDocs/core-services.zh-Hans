---
description: 了解有关解决方案数据源和配置订阅的信息。通过订阅，可以在 Experience Cloud 和各解决方案（Analytics 和 Target）之间传输客户属性数据流。
keywords: 客户属性；核心服务
seo-description: 了解有关解决方案数据源和配置订阅的信息。通过订阅，可以在 Experience Cloud 和各解决方案（Analytics 和 Target）之间传输客户属性数据流。
seo-title: 配置订阅
solution: Experience Cloud
title: 配置订阅
uuid: f74a8155-0a21-46b3-9b1e-4c838f72f24f
translation-type: tm+mt
source-git-commit: 979b2202a70e2a5362aa86a65a17d7c4279b3a1a

---


# 配置订阅

了解有关解决方案数据源和配置订阅的信息。通过订阅，可以在 Experience Cloud 和各解决方案（Analytics 和 Target）之间传输客户属性数据流。

例如，Adobe Analytics 订阅可在报表中启用属性数据。如果您使用 Adobe Target，则可以上传客户属性，以便进行定位和分段。

**[!UICONTROL 客户属性源]** &gt; **[!UICONTROL 创建新客户属性源]** &gt; **[!UICONTROL 新增功能]**

![](assets/configure_subscription_page.png)

| 元素 | 描述 |
|--- |--- |
| 解决方案 | **Adobe AnalyticsSelect**<br>Analytics，指定要接收属性数据的报表包，以及要包含的属性。<br>**Adobe Target您**<br>可以上传定位和细分的客户属性。当您想要基于属性数据来定位测试，或者希望数据可在 Analytics 中用于分段时，此功能非常有用。<br>登录后，单击 Target &gt; 受众，即可使用访客的上传客户属性数据。<br>支持多个数据源。在您的网站上[设置客户 ID](../core-services/core-services.md) 后，请确认至少有一个别名已订阅到 Target。 |
| 报表包 (Analytics) | Analytics中的报表包。<br>您无法在一个属性来源内向 Analytics 订阅添加总计 10 个以上的报表包。在选择要包含哪些报表包时，请考虑以下建议：<ul><li>选择具有一组经过身份验证的共同客户的报表包。如果一个报表包中经过身份验证的的客户与另一报表包中经过身份验证的客户不重合，则将这些报表包分入不同的属性来源。</li><li>如有可能，一个属性来源中包含的报表包应当具有相似的流量。</li></ul><br>如果您有 10 个以上的报表包具有一组共同的经过身份验证的客户，则可以配置更多的客户属性来源，使每个来源最多包含 10 个报表包。 |
| 要包含的属性(Analytics和Target) | 您希望发送至解决方案的属性。<br>在配置订阅和选择属性时，根据您拥有的解决方案，将会受到以下限制：<ul><li>基金会：0</li><li>选择：3</li><li>Prime：15</li><li>Ultimate：200</li><li>Standard：总共允许 3 个</li><li>Premium：每个报表包允许 200 个</li><li>Target Standard：5 个</li><li>Target Premium：200 个</li></ul><br>**注意：** 当您升级到 Analytics Premium 时，附加属性会在延迟 24 小时后才可用。在此延迟期间，您可能会看到出现属性订阅达到最大值错误。 |
