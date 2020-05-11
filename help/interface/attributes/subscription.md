---
description: 了解解决方案数据源和配置订阅。 订阅支持Experience Cloud和解决方案(Analytics和目标)之间的客户属性数据流。
keywords: Customer Attributes;core services
seo-description: 了解解决方案数据源和配置订阅。 订阅支持Experience Cloud和解决方案(Analytics和目标)之间的客户属性数据流。
seo-title: 配置订阅
solution: Experience Cloud
title: 配置订阅
uuid: f74a8155-0a21-46b3-9b1e-4c838f72f24f
translation-type: tm+mt
source-git-commit: 0bc7032d0052ba03beac1140dfbfd630e1802bfd
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# 配置订阅

了解解决方案数据源和配置订阅。 订阅支持Experience Cloud和解决方案（Analytics和）之间的客户属性数据 [!DNL Target]流。

例如，Adobe Analytics订阅启用报表中的属性数据。 如果您使用Adobe目标，则可以上传客户属性以进行定位和细分。

**[!UICONTROL 客户属性来源]** > **[!UICONTROL 新建客户属性来源]** >新建 ****

![](assets/configure_subscription_page.png)

| 元素 | 描述 |
|--- |--- |
| 解决方案 | **Adobe Analytics **<br>选择 Analytics，指定要接收属性数据的报表包，以及要包含的属性。<br>**Adobe Target**<br>您可以上传客户属性进行定位和细分。 当您想要基于属性数据来定位测试，或者希望数据可在 Analytics 中用于分段时，此功能非常有用。<br>已上传的访客客户属性数据可在登录时在>**[!DNL Target]**受众**&#x200B;中获取&#x200B;**。<br>支持多个数据源。在您的网站上[设置客户 ID](../core-services/core-services.md)后，请确认至少有一个别名已订阅到[!DNL Target]. |
| 报表包 (Analytics) | 报表包来自 Analytics。<br>您无法在一个属性来源内向 Analytics 订阅添加总计 10 个以上的报表包。选择要包含的报表包时，请考虑以下建议：<ul><li>选择具有一组通用的已验证客户的报表包。 如果一个报告套件中经过身份验证的客户与另一个报告套件中经过身份验证的客户没有重叠，请将这些报告套件分为不同的属性源。</li><li>如果可能，属性源中包含的报表包应具有相似的流量。</li></ul><br>如果您有 10 个以上的报表包具有一组共同的经过身份验证的客户，则可以配置更多的客户属性来源，使每个来源最多包含 10 个报表包。 |
| Attributes to Include (Analytics and [!DNL Target]) | 要发送给解决方案的属性。 <br>配置订阅和选择属性时，根据您拥有的解决 _方案，以下限制_ 适用于每个报表包：<ul><li>Foundation：0 个</li><li>Select：3 个</li><li>Prime：15 个</li><li>Ultimate：200 个</li><li>Standard：总共允许 3 个</li><li>Premium：每个报表包允许 200 个</li><li>[!DNL Target] 标准： 5</li><li>[!DNL Target] 高级： 200</li></ul><br>**注意：**当您升级到 Analytics Premium 时，附加属性会在延迟 24 小时后才可用。在此延迟期间，您可能会看到出现属性订阅达到最大值错误。 |
