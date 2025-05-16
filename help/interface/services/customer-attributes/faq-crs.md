---
description: 有关 Adobe Experience Cloud 中针对 Adobe Analytics 和 Adobe Target 的  [!DNL Customer Attributes]  的常见问题解答。
solution: Experience Cloud
title: 有关  [!DNL Customer Attributes] 的常见问题解答
uuid: e93eb531-23c7-4d75-92e8-75699f58546a
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 6031e544-822b-4843-b3d8-98a36a3c40e8
source-git-commit: 7fb572beadfddbaeffb5257f0180b754a0d9ea6c
workflow-type: tm+mt
source-wordcount: '1029'
ht-degree: 95%

---

# 有关 [!DNL Customer Attributes] 的常见问题解答

有关 Adobe Analytics 和 Adobe Target 中 [!DNL Customer Attributes] 的常见问题解答和最佳实践。

## 最佳实践和限制 {#section_7F5189B3DAA84EE6865B91D2026EE05A}

使用 [!DNL Customer Attributes] 时的指导和限制。

| 问题 | 描述 |
|--- |--- |
| [!UICONTROL 客户属性]订阅限制 | 当您升级到 Analytics Premium 后，需要经过 24 小时的延迟才能使用更多属性。在此延迟期间，您可能会看到[!UICONTROL 属性订阅数量达到最大值]错误。 |
| 同一台设备上的多次登录 | 使用 [!DNL Customer Attributes] 将客户轮廓上传到数据源时，Adobe 建议用户不要共享设备（即，同一 Experience Cloud ID）。Experience Cloud ID (ECID) 会在设备上持续存在。如果共享设备，则可能会引发 ECID 将多位用户链接到同一 ECID，从而导致 [!DNL Target] 中出现意外结果。**注意：** 对于移动设备，安装移动应用程序后，ECID 便会永久性存在。重新安装该应用程序才能生成新的 ECID。对于 Web，在清除浏览器 Cookie 之后便可生成新的 ECID。 |
| 每日上传频率限制 | Adobe 建议每天只更新一次 [!DNL Customer Attributes]。您必须至少等待 24 小时，才能为同一组轮廓上传另一个客户轮廓数据文件。 |
| 自定义 Analytics ID (`s.visitorID`) | 使用 `s.visitorID` 设置客户 ID 是在 Analytics 中标识用户的一种方法。但是，当使用 `s.visitorID.`<br> 标识某个访客时，使用 ID 服务导出或导入 [!DNL Analytics] 数据的集成会不起作用。这包括但不限于共享受众、[!DNL Analytics] for Adobe Target (A4T) 和 [!DNL Customer Attributes]。<br>对于这些集成，不支持设置自定义 Analytics ID。 |
| [!DNL Analytics] 中的字符长度限制 | 创建 [!DNL Analytics] 订阅时，已上传文件的字段长度将被截断为 255。 |

{style="table-layout:auto"}

## 关于 [!DNL Customer Attributes] 的常见问题 {#section_E47866EEA83348E09FE43CEC5E44C461}

| 问题 | 回答 |
|--- |--- |
| 我是否可以接收有关 [!DNL Customer Attributes] 上传状态的通知？ | 可以。 |
| 我应该怎样做才能开始使用 [!DNL Customer Attributes]？ | <ol><li>进行配置。如果您是 Analytics 客户，Adobe 将为您配置 [!DNL Customer Attributes]。如果您只使用 Adobe Target 而没有使用 Analytics，请联系客户关怀团队以请求配置核心服务。</li> <li>与您的 CRM 团队进行交谈。了解哪些类型的客户数据可以在 Analytics 和整个 Experience Cloud 中使用。</li><li>实施核心服务。</li></ol> |
| 我可以使用多少个 [!DNL Customer Attributes]？ | 您可以向客户属性服务上传数百个 `.csv` 列。但是，在配置订阅和选择属性时，根据您拥有的应用程序，将会受到以下限制（每个报表包）：  <ul><li>Foundation：0 个</li><li>Select：3 个</li><li>Prime：15 个</li><li>Ultimate：200 个</li><li>Standard：总共允许 3 个</li><li>Premium：200 个</li><li>Adobe Target Standard：5 个</li><li>Adobe Target Premium：200 个</li></ul> |
| 是否需要迁移到 Experience Cloud ID 服务？ | 迁移取决于您使用的应用程序。 <ul><li>Adobe Analytics：强烈推荐 </li><li>Adobe Target：必需。 </li></ul><br>使用Experience Cloud ID服务可启用最新的Experience Cloud功能，包括实时受众、Adobe Target现代化、Analytics集成和视频检测信号跟踪。 |
| 客户属性功能与 Adobe Audience Manager 有何关系？ | 虽然 Audience Manager 能够接收数据以执行受众识别，但是它无法执行将属性与历史行为数据关联起来的分析功能。此外，它也不具备 Adobe Analytics 中提供的报表、分析和分段功能。[!UICONTROL 人员]服务可将不同应用程序中的丰富数据捆绑在一起，并将其与单个 ID 关联，以在整个 Experience Cloud 中使用。<br>在 Adobe Target 中，[!DNL Customer Attributes] 显示为单个属性，这些属性可以与其他规则组合使用以生成受众。共享给[!UICONTROL 人员]服务的受众是完整受众，无法进行修改。 |
| **（仅限 Analytics）**&#x200B;此功能与 Analytics Premium 中提供的功能有何不同？ | 过去，客户希望将客户属性数据与 Analytics 数据结合在一起时，很大程度上依赖 Data Workbench 工具来实现此功能。[!DNL Customer Attributes]通过在Report Builder中提供[!DNL Customer Attributes]作为维度和量度向更广泛的受众公开此功能。 Analytics Standard 客户有权访问 [!DNL Customer Attributes]，但可以使用的功能有限。Analytics Premium 客户可以使用所有功能。 |
| **（仅限 Adobe Target）**&#x200B;我是否可以为从未使用过 Adobe Target 的客户预加载或上传数据？ | 可以。当访客首次向 Adobe Target 发出请求时，系统将从 [!DNL Customer Attributes] 中获取 Adobe 拥有的关于访客的现有信息，并将这些数据用于定位。**注意：**&#x200B;此数据的检索过程从访客首次与 Adobe Target 交互起可能需要多达 20 分钟的时间。 |
| **（仅限 Adobe Target）**&#x200B;是否可以通过将客户属性数据与共享的受众数据结合来创建超级受众？ | 不可以。共享的受众数据是一个完整的受众。 |
| **（仅限 Adobe Target）**&#x200B;与 Adobe Target 的批量轮廓 API 相比，[!DNL Customer Attributes] 功能如何？ | 可直接通过批量轮廓 API，逐个或批量更新 Adobe Target 轮廓。该功能与 [!DNL Customer Attributes] 类似，主要区别如下：<ul><li>轮廓 API 是一种 REST API 调用，而 [!DNL Customer Attributes] 使用 FTP。</li><li>Adobe Target 的轮廓 API 只向 Adobe Target 发送数据，而不会向整个 Experience Cloud 发送数据。</li><li>[!DNL Customer Attributes] 提供了一个简单的界面来创建和管理此外部数据。</li></ul> |
| **（仅限 Adobe Target）**&#x200B;将数据从 [!DNL Customer Attributes] 上传到 Adobe Target 是否可以延长 Adobe Target 访客轮廓的生命周期？ | 可以。请参阅 Adobe Target 帮助中的[访客轮廓生命周期](https://experienceleague.adobe.com/docs/target/using/audiences/visitor-profiles/visitor-profile.html?lang=zh-Hans)。 |
| **（仅限 Adobe Target）**&#x200B;通过客户 ID 标识访客后，是否可以立即定位 [!DNL Customer Attributes] 中上传的数据？ | 可以。在对 Adobe Target 的服务器调用（包括 mbox 第三方 ID）中，所有客户属性数据将可用。 |
| **（仅限 Adobe Target）** 对于客户属性源中上传的文件，**[!UICONTROL 同步状态]**&#x200B;列表示什么？ | Adobe Target 发布并同步的记录数可以通过选择针对某个特定属性文件的“同步状态”图标来进行查看。`Sync %` 是一个实时指标，用于指定已在 Adobe Target 中同步的轮廓的百分比。<br> **注意：**&#x200B;属性可能需要长达 24 小时才能与 Adobe Target 同步。 |
| 文件上传量度在 [!DNL Customer Attributes] 来源中表示什么？ | 借助以下量度，您可以检查已上传到 [!DNL Customer Attributes] 的属性状态： <ul><li>记录：属性文件中的记录数。</li><li>**新记录：**&#x200B;属性文件中存在的新记录数。</li> <li>**更新的记录：**&#x200B;已存在于 [!DNL Customer Attributes] 中且文件中的值已更新的记录数。</li><li>**所有数据（记录）：**&#x200B;已成功上传到 [!DNL Customer Attributes] 的记录总数。</li></ul> |

{style="table-layout:auto"}
