---
description: 管理员可以了解在升级到 Analytics Premium 时的相应要求和预期，以及作为一名 Experience Cloud 管理员，应在何处查找帮助。
keywords: Adobe Analytics Premium upgrade
solution: Experience Cloud
title: '如何升级到Analytics Premium和Experience Cloud '
topic: Premium
uuid: 450a601c-d199-4e90-b525-19bd9f9576d2
translation-type: tm+mt
source-git-commit: 3f26c1af19a0838913eec2b4135304f5f3fcf0b4
workflow-type: tm+mt
source-wordcount: '641'
ht-degree: 98%

---


# 升级到 Analytics Premium 和 Experience Cloud

管理员可以了解在升级到 Analytics Premium 时的相应要求和预期，以及作为一名 Experience Cloud 管理员，应在何处查找帮助。

## Analytics Premium {#section_7F50AD7906544F899B844BE31D3BB507}

升级到 Adobe Analytics Premium 后，您可以使用 Analytics Standard 提供的所有功能或产品，包括 Data Warehouse、Ad Hoc Analysis、Report Builder 和 Data Connectors。（这些产品是使用单点解决方案 SiteCatalyst 单独出售给客户的。）

Analytics Premium 允许您：

* 访问 250 个转化变量 (eVar)
* [移动设备应用程序 Analytics](https://docs.adobe.com/content/help/zh-Hans/mobile-services/using/home.html)
* 使用 Data Workbench（可视数据查询；基于规则的属性；跨渠道分析）

>[!NOTE]
>
>升级时不需要迁移，但是要注意一些注意事项：
>
>* eVars 76-250 (SiteCatalyst) 和 100-250 (Standard) 将在管理工具中可见，但尚未被启用。>
>* 贡献分析由 Adobe 启用。它不会更改位置（仍位于“异常检测”页面上），但是现在它将自动开始分析所有数据点。>


## Analytics Premium Complete {#section_BFAD815EDF364845A52B340B2FD5B64C}

在 Analytics Premium Complete 中，您可以获得 [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) 的所有功能，并获得以下升级：

| 产品 | 升级 |
|--- |--- |
| Reports and Analytics | <ul><li>[贡献分析](https://docs.adobe.com/content/help/zh-Hans/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html)</li><li>[客户属性](../attributes/attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1)（最多 200 个）</li></ul> |
| Data Workbench | <ul><li>算法归因</li><li>预建工作区</li></ul> |
| Analytics Platform | [实时流](https://helpx.adobe.com/cn/analytics/kb/getting-started-with-livestream-api.html)（原始数据、功能板、触发器） |

## Predictive Intelligence {#section_B407932C07A7476F83FB0275C3FB63DC}

升级到 Predictive Intelligence 可启用 [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) 以及：

| 产品 | 升级 |
|---|---|
| Reports and Analytics | [贡献分析](https://docs.adobe.com/content/help/zh-Hans/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html) |
| Data Workbench | 用于受众资格和预测营销的预建工作区。 |
| Analytics Platform | 实时流（功能板和触发器） |

## Customer 360 {#section_3B2AC245388248688067DC9A48957AFB}

升级到 Customer 360 可启用 [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) 以及：

| 产品 | 升级 |
|--- |--- |
| [客户属性](../attributes/attributes.md) | 客户属性（分析和区段共享） |
| Data Workbench | <ul><li>派生的客户属性</li><li>用于受众发现的预建工作区</li></ul> |
| Analytics Platform | [客户属性](../attributes/attributes.md) |

## 高级属性 {#section_9E4986A8389946CCAA7D003268343296}

通过高级属性可访问 [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507)，以及 Data Workbench 中的算法归因（服务器调用量为 25％）。

## Data Workbench 要求 {#section_D959CA68D6DB42C38707F8E0CA3654CC}

通过向 `dwb@adobe.com` 发送电子邮件，受支持的用户可请求更新所有的客户端许可证，以便反映 Analytics Premium。这样可以启用算法归因等功能。

技术运营人员将审查您的合同承诺并确定适当的托管基础结构，以增加或减少容量，然后他们将通过客户经理或咨询人员与您进行协调以部署任何更改。

必须停用在本地运行的所有软件，包括传感器，这意味着您需要确保通过 Analytics 标记进行正确跟踪。

## Experience Cloud - 管理用户和产品 {#section_6471C54454024301B2E0B687F79F6738}

Experience Cloud 和核心服务可供 Analytics Standard 和 Premium 用户使用，前提是您已遵循[快速入门 - 为核心服务启用解决方案](../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C)中所述的实施现代化。（该过程有助于使您的实施符合现代化要求，并且允许您成为 Experience Cloud 中的管理员。）

加入 Experience Cloud 后，您可以通过 Experience Cloud ([!DNL experiencecloud.adobe.com]) 登录，并开始使用核心服务（包括客户属性、受众以及移动设备应用程序分析）。

### 管理用户和群组

用户管理在 [Adobe Admin Console](https://helpx.adobe.com/cn/enterprise/help/aedash.html)（产品链接）中执行。

您可以将在 Adobe Admin Console 中创建的群组与解决方案群组（例如 Adobe Analytics）之间的映射设置为 1:1。之后，将会为添加到 Admin Console 映射群组的新用户自动创建 Analytics 解决方案帐户，并将其关联到该用户的 Adobe ID。（现有用户必须手动关联其解决方案帐户凭据，才能通过 Experience Cloud 登录访问解决方案。）

>[!NOTE]
>
>您可以将多个解决方案群组映射到一个 Admin Console 群组。但是，Adobe 建议设置 1:1 映射。提前映射组允许您通过上传 CSV 来邀请、创建、许可和添加多个用户。
