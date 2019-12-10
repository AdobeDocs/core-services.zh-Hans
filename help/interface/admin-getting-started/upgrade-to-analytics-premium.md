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
source-git-commit: ae97db27349940a8df7ee2ba6678683f57585678

---


# 升级到 Analytics Premium 和 Experience Cloud

管理员可以了解在升级到 Analytics Premium 时的相应要求和预期，以及作为一名 Experience Cloud 管理员，应在何处查找帮助。

## Analytics Premium {#section_7F50AD7906544F899B844BE31D3BB507}

升级到 Adobe Analytics Premium 后，您可以享用 Analytics Standard 中所有可用的功能或产品，包括 Data Warehouse、Ad Hoc Analysis、Report Builder 和 Data Connectors。（这些产品是使用点解决方案 SiteCatalyst 向客户单独销售的。）

使用 Analytics Premium，您可以：

* 访问 250 个转化变量 (eVar)
* 执行[移动设备应用程序分析](https://docs.adobe.com/content/help/en/mobile-services/using/home.html)
* 使用 Data Workbench（可视数据查询；基于规则的属性；跨渠道分析）

>[!NOTE]
>
>升级时无需进行迁移，但是应当了解以下考虑事项：
>
>* 可在“管理工具”中看到 eVar 76-250 (SiteCatalyst) 和 100-250 (Standard)，但是已无法启用它们。&gt;
>* 贡献分析已由 Adobe 开启。它没有更改位置（仍位于“异常检测”页面中），但现在会自动开始分析所有数据点。&gt;


## Analytics Premium 完整版 {#section_BFAD815EDF364845A52B340B2FD5B64C}

在 Analytics Premium 完整版中，您可以获取 [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) 的所有功能，还可执行以下升级：

| 产品 | 升级 |
|--- |--- |
| Reports and Analytics | <ul><li>[贡献分析](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html)</li><li>[客户属性](../attributes/attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1)（最多 200 个）</li></ul> |
| Data Workbench | <ul><li>算法属性</li><li>预置工作区</li></ul> |
| Analytics 平台 | [实时流](https://helpx.adobe.com/analytics/kb/getting-started-with-livestream-api.html)（原始数据、功能板、触发器） |

## Predictive Intelligence {#section_B407932C07A7476F83FB0275C3FB63DC}

升级到 Predictive Intelligence 可启用 [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) 以及下列产品：

| 产品 | 升级 |
|---|---|
| Reports and Analytics | [贡献分析](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html) |
| Data Workbench | 用于受众资格鉴定和前瞻性市场营销的预置工作区。 |
| Analytics 平台 | 实时流（功能板和触发器） |

## Customer 360 {#section_3B2AC245388248688067DC9A48957AFB}

升级到 Customer 360 可提供 [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) 以及下列产品：

| 产品 | 升级 |
|--- |--- |
| [客户属性](../attributes/attributes.md) | 客户属性（分析和区段共享） |
| Data Workbench | <ul><li>派生的客户属性</li><li>用于受众发现的预置工作区</li></ul> |
| Analytics 平台 | [客户属性](../attributes/attributes.md) |

## 高级属性 {#section_9E4986A8389946CCAA7D003268343296}

高级属性可提供对 [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) 以及 Data Workbench 中算法属性的访问（25% 的服务器调用量）。

## Data Workbench 要求 {#section_D959CA68D6DB42C38707F8E0CA3654CC}

通过向 `dwb@adobe.com` 发送电子邮件，受支持的用户可请求更新所有的客户端许可证，以便反映 Analytics Premium。这会启用算法属性等功能。

技术操作人员将审阅您合同中承诺的内容，并确定适当的托管基础设施（增加或减少功能），然后他们将通过客户经理或采用咨询的方式与您进行协调，进而部署任何更改。

必须停用内部正在运行的所有软件。其中包括传感器，这意味着您需要通过 Analytics 标签来确保进行正确的跟踪。

## Experience Cloud - 管理用户和产品 {#section_6471C54454024301B2E0B687F79F6738}

Experience Cloud 和核心服务可供 Analytics Standard 和 Premium 用户使用，前提是您已遵循[快速入门 - 为核心服务启用解决方案](../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C)中所述的实施现代化。（该过程有助于使您的实施符合现代化要求，并且允许您成为 Experience Cloud 中的管理员。）

加入 Experience Cloud 后，您可以通过 Experience Cloud ([!DNL experiencecloud.adobe.com]) 登录，并开始使用核心服务（包括客户属性、受众以及移动设备应用程序分析）。

### 管理用户和群组

用户管理在 [Adobe 管理控制台](https://helpx.adobe.com/enterprise/help/aedash.html)（产品链接）中执行。

您可以在 Adobe 管理控制台中创建的群组与解决方案群组（例如 Adobe Analytics）之间设置 1 对 1 映射。之后，系统会为添加到所映射的管理控制台群组的新用户自动创建一个 Analytics 解决方案帐户，并将该帐户关联到用户的 Adobe ID。（现有用户必须手动关联其解决方案帐户凭据，才能通过 Experience Cloud 登录来访问解决方案。）

>[!NOTE]
>
>您可以将多个解决方案群组映射到一个 Admin Console 群组。不过，Adobe 建议进行 1 对 1 映射。提前映射群组后，您可以通过上传 CSV 来邀请、创建、授权和添加多个用户。
