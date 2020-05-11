---
description: 管理员可以了解在升级到 Analytics Premium 时的相应要求和预期，以及作为一名 Experience Cloud 管理员，应在何处查找帮助。
keywords: upgrading
seo-description: 管理员可以了解在升级到 Analytics Premium 时的相应要求和预期，以及作为一名 Experience Cloud 管理员，应在何处查找帮助。
seo-title: 升级到 Analytics Premium 和 Experience Cloud
solution: Experience Cloud
title: 升级到 Analytics Premium 和 Experience Cloud
topic: Premium
uuid: 450a601c-d199-4e90-b525-19bd9f9576d2
translation-type: tm+mt
source-git-commit: 0bc7032d0052ba03beac1140dfbfd630e1802bfd
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# 升级到 Analytics Premium 和 Experience Cloud

管理员可以了解在升级到 Analytics Premium 时的相应要求和预期，以及作为一名 Experience Cloud 管理员，应在何处查找帮助。

## Analytics Premium {#section_7F50AD7906544F899B844BE31D3BB507}

升级到Adobe Analytics Premium可为您提供Analytics Standard的所有功能或产品，包括数据仓库、临时分析、Report Builder和数据连接器。 （这些产品是使用点解决方案SiteCatalyst单独销售给客户的。）

Analytics Premium为您提供：

* 访问250个转换变量(eVar)
* [移动应用分析](https://docs.adobe.com/content/help/zh-Hans/mobile-services/using/home.html)
* 使用 Data Workbench（可视数据查询；基于规则的属性；跨渠道分析）

>[!NOTE]
>
>升级时无需迁移，但需要注意以下几点：
>
>* eVars 76-250(SiteCatalyst)和100-250（标准）将在管理工具中可见，但尚未启用。>
>* 贡献分析由Adobe启用。 它不会更改位置（在异常检测页面上仍可用），但现在它将自动开始分析所有数据点。>


## Analytics Premium 完整版 {#section_BFAD815EDF364845A52B340B2FD5B64C}

在Analytics Premium Complete中，您可以获得Analytics Premium的所 [有功能](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507)，并获得以下升级：

| 产品 | 升级 |
|--- |--- |
| Reports and Analytics | <ul><li>[贡献分析](https://docs.adobe.com/content/help/zh-Hans/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html)</li><li>[客户属性](../attributes/attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1)（最多 200 个）</li></ul> |
| Data Workbench | <ul><li>算法归因</li><li>预建工作区</li></ul> |
| Analytics Platform | [实时流](https://helpx.adobe.com/analytics/kb/getting-started-with-livestream-api.html) (原始数据、仪表板、触发器) |

## Predictive Intelligence {#section_B407932C07A7476F83FB0275C3FB63DC}

升级到Predictive Intelligence可 [以加](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) :

| 产品 | 升级 |
|---|---|
| Reports and Analytics | [贡献分析](https://docs.adobe.com/content/help/zh-Hans/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html) |
| Data Workbench | 为受众资格和预测营销预建工作区。 |
| Analytics Platform | 实时流(仪表板和触发器) |

## 客户360 {#section_3B2AC245388248688067DC9A48957AFB}

升级到Customer 360优惠 [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) 外加：

| 产品 | 升级 |
|--- |--- |
| [客户属性](../attributes/attributes.md) | 客户属性（分析和区段共享） |
| Data Workbench | <ul><li>派生的客户属性</li><li>用于受众发现的预建工作区</li></ul> |
| Analytics Platform | [客户属性](../attributes/attributes.md) |

## 高级属性 {#section_9E4986A8389946CCAA7D003268343296}

高级归因优惠可 [以访问Analytics](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507)Premium，以及Data Workbench中的Algorithmic Attribution（25%的服务器调用量）。

## 数据工作台要求 {#section_D959CA68D6DB42C38707F8E0CA3654CC}

通过向 `dwb@adobe.com` 发送电子邮件，受支持的用户可请求更新所有的客户端许可证，以便反映 Analytics Premium。这支持像Algorithmic Attribution这样的功能。

技术运营将审查您的合同承诺并确定适当的受管基础架构，增加或减少容量，然后他们将通过客户经理或咨询与您协调，以部署任何更改。

必须停用正在内部部署运行的任何软件。 这包括传感器，这意味着您需要确保通过Analytics标记进行正确跟踪。

## Experience Cloud - 管理用户和产品 {#section_6471C54454024301B2E0B687F79F6738}

Experience Cloud 和核心服务可供 Analytics Standard 和 Premium 用户使用，前提是您已遵循[快速入门 - 为核心服务启用解决方案](../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C)中所述的实施现代化。（该过程有助于使您的实施符合现代化要求，并且允许您成为 Experience Cloud 中的管理员。）

After you join the Experience Cloud, you can log in via the Experience Cloud at [!DNL experiencecloud.adobe.com] and begin using core services (including Customer Attributes, Audiences, and Mobile app analytics).

### 管理用户和群组

用户管理在Adobe Admin Console [(产品链接](https://helpx.adobe.com/enterprise/help/aedash.html) )中执行。

您可以在在Adobe Admin Console中创建的组和解决方案组（如Adobe Analytics）之间设置1:1映射。 此后，添加到映射的Admin Console组的新用户将自动创建一个Analytics解决方案帐户并将其链接到用户的Adobe ID。 （现有用户必须手动链接其解决方案帐户凭据，才能通过Experience Cloud登录名访问解决方案。）

>[!NOTE]
>
>您可以将多个解决方案群组映射到一个 Admin Console 群组。但是，Adobe建议进行1:1映射。 提前映射用户组允许您通过上传CSV来邀请、创建、授权和添加多个用户。
