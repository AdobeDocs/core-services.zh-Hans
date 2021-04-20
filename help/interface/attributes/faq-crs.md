---
description: 有关 Adobe Experience Cloud、Adobe Analytics 和 Adobe Target 中客户属性的常见问题解答。
keywords: 客户属性
solution: Experience Cloud
title: '获取有关客户属性的常见问题解答 '
uuid: e93eb531-23c7-4d75-92e8-75699f58546a
feature: Customer Attributes
topic: Administration
role: Administrator
level: Experienced
translation-type: tm+mt
source-git-commit: b466cffbbb37eec39266d90cb6a849562d608cd9
workflow-type: tm+mt
source-wordcount: '1239'
ht-degree: 99%

---


# 有关客户属性的常见问题解答

有关 Adobe Analytics 和 Adobe Target 中客户属性的常见问题解答和最佳实践。

## 最佳实践和限制 {#section_7F5189B3DAA84EE6865B91D2026EE05A}

使用[!UICONTROL 客户属性]时的指导和限制。

| 问题 | 描述 |
|--- |--- |
| [!UICONTROL 客户属性]订阅限制 | 当您升级到 Analytics Premium 后，需要经过 24 小时的延迟才能使用更多属性。在此延迟期间，您可能会看到“属性订阅数量达到最大值”的错误。 |
| 同一台设备上的多次登录 | 使用客户属性将客户配置文件上传到数据源时，Adobe 建议用户不要共享设备（即，同一 Experience Cloud ID）。Experience Cloud ID (ECID) 会在设备上持续存在。如果共享设备，则可能会引发 ECID 将多位用户链接到同一 ECID，从而导致 [!DNL Target] 中出现意外结果。**注意：**&#x200B;对于移动设备，在安装移动设备应用程序后，ECID 便会永久存在。您必须重新安装该应用程序才能生成新的 ECID。对于 Web，在清除浏览器 Cookie 之后便可生成新的 ECID。 |
| 每日上传频率限制 | Adobe 建议每天只更新一次客户属性。您必须至少等待 24 小时，才能为同一组配置文件上传另一个客户配置文件数据文件。 |
| 自定义 Analytics ID (`s.visitorID`) | 使用 `s.visitorID` 设置客户 ID 是在 Analytics 中标识用户的一种方法。但是，当使用 `s.visitorID.`<br> 标识某个访客时，使用 ID 服务导出或导入 Analytics 数据的集成将不起作用。这包括但不限于共享受众、Analytics for Adobe Target (A4T) 和客户属性。<br>对于这些集成，不支持设置自定义 Analytics ID。 |
| Analytics 中的字符长度限制 | 创建 Analytics 订阅时，已上传文件的字段长度将被截断为 255。 |

## 关于客户属性的常见问题解答 {#section_E47866EEA83348E09FE43CEC5E44C461}

| 问题 | 回答 |
|--- |--- |
| 我是否可以接收有关客户属性上传状态的通知？ | 可以。请参阅[管理通知](https://docs.adobe.com/content/help/zh-Hans/core-services/interface/manage-users-and-products/organizations.html#concept_0105453AD71847B8BFCAF4A40915F157)。 |
| 我应该怎么做才能开始使用客户属性？ | <ol><li>进行配置。如果您是 Analytics 客户，Adobe 将为您配置客户属性。如果您只使用 Adobe Target 而没有使用 Analytics，请联系客户关怀团队以请求配置核心服务。</li> <li>与您的 CRM 团队进行交谈。了解哪些类型的客户数据可以在 Analytics 和整个 Experience Cloud 中使用。</li><li>实施核心服务。有关如何实现实施现代化的步骤，请参阅[启用核心服务的解决方案](https://docs.adobe.com/content/help/zh-Hans/core-services/interface/about-core-services/core-services.html)。（请参阅有关同步客户 ID 的部分，以获取重要信息。）</li></ol> **注意：**[此处](https://docs.adobe.com/content/help/zh-Hans/core-services/interface/manage-users-and-products/faq.html#concept_13219B4E51784577B6FF78AAA203DE91)提供了关于实施核心服务的管理员常见问题解答。 |
| 我可以使用多少个客户属性？ | 您可以向客户属性服务上传数百个 `.csv` 列。但是，在配置订阅和选择属性时，根据您拥有的解决方案，将会受到以下限制（每个报表包）：  <ul><li>Foundation：0 个</li><li>Select：3 个</li><li>Prime：15 个</li><li>Ultimate：200 个</li><li>Standard：总共允许 3 个</li><li>Premium：200 个</li><li>Adobe Target Standard：5 个</li><li>Adobe Target Premium：200 个</li></ul> |
| 是否需要迁移到 Experience Cloud ID 服务？ | 迁移取决于您使用的解决方案。 <ul><li>Adobe Analytics：强烈推荐 </li><li>Adobe Target：必需。 </li></ul><br>使用 Experience Cloud ID 服务可启用最新的 Experience Cloud 功能，其中包括实时受众、Adobe Target 现代化、Analytics 集成，以及视频检测信号跟踪。<br>有关更多详细信息，请参阅[启用核心服务的解决方案](https://docs.adobe.com/content/help/en/core-services/interface/about-core-services/core-services.html)。<br>**注意：**[Experience Cloud ID 服务](https://docs.adobe.com/content/help/zh-Hans/id-service/using/intro/overview.html)是以前称为 _Analytics 访客 ID 服务_&#x200B;的现代化实施。 |
| 客户属性功能与 Adobe Audience Manager 有何关系？ | 虽然 Audience Manager 能够接收数据以执行受众识别，但是它无法执行将属性与历史行为数据关联起来的分析功能。此外，它也不具备 Adobe Analytics 中提供的报表、分析和分段功能。[!UICONTROL 人员]服务可将不同解决方案中的丰富数据捆绑在一起，并将其与单个 ID 关联，以在整个 Experience Cloud 中使用。<br>在 Adobe Target 中，客户属性显示为单个属性，这些属性可以与其他规则组合使用以构建受众。共享给[!UICONTROL 人员]服务的受众是完整受众，无法进行修改。 |
| **（仅限 Analytics）**&#x200B;此功能与 Analytics Premium 中提供的功能有何不同？ | 过去，希望将客户属性数据与 Analytics 数据结合在一起的客户在很大程度上依赖 Data Workbench 工具来实现此功能。客户属性通过在 Reports &amp; Analytics、Ad Hoc Analysis 和 Report Builder 中提供客户属性作为维度和量度，来向更广泛的受众公开此功能。Analytics Standard 客户将有权访问客户属性，但其可以使用的功能有限。Analytics Premium 客户可以使用所有功能。 |
| **（仅限 Adobe Target）**&#x200B;我是否可以为从未使用过 Adobe Target 的客户预加载或上传数据？ | 可以。当访客首次向 Adobe Target 发出请求时，系统将从“客户属性”中获取我们拥有的关于访客的现有信息，并将这些数据用于定位。**注意：**&#x200B;此数据的检索过程可能需要多达 20 分钟，从访客首次与 Adobe Target 交互开始算起。 |
| **（仅限 Adobe Target）**&#x200B;是否可以通过将客户属性数据与共享的受众数据结合来创建超级受众？ | 否。共享的受众数据是一个完整的受众。 |
| **（仅限 Adobe Target）**&#x200B;与 Adobe Target 的批量配置文件 API 相比，客户属性功能如何？ | 可直接通过批量配置文件 API，逐个或批量更新 Adobe Target 配置文件。该功能与客户属性类似，主要区别如下：<ul><li>配置文件 API 是一种 REST API 调用，而客户属性使用 FTP。</li><li>Adobe Target 的配置文件 API 只向 Adobe Target 发送数据，而不会向整个 Experience Cloud 发送数据。</li><li>客户属性提供了一个简单的界面来创建和管理此外部数据。</li></ul> |
| **（仅限 Adobe Target）**&#x200B;将数据从客户属性上传到 Adobe Target 是否可以延长 Adobe Target 访客配置文件的生命周期？ | 可以。请参阅 Adobe Target 帮助中的[访客配置文件生命周期](https://docs.adobe.com/content/help/zh-Hans/target/using/audiences/visitor-profiles/visitor-profile.html)。 |
| **（仅限 Adobe Target）**&#x200B;通过客户 ID 标识访客后，是否可以立即定位客户属性中上传的数据？ | 可以。在对 Adobe Target 的服务器调用（包括 mbox 第三方 ID）中，所有客户属性数据将可用。 |
| **（仅限 Adobe Target）**&#x200B;对于客户属性来源中上传的文件，**[!UICONTROL 同步状态]**&#x200B;列表示什么？ | Adobe Target 发布并同步的记录数可以通过单击针对某个特定属性文件的“同步状态”图标来进行查看。`Sync %` 是一个实时量度，用于指定已在 Adobe Target 中同步的配置文件的百分比。<br> **注意：**&#x200B;属性可能需要长达 24 小时才能与 Adobe Target 同步。 |
| 文件上传量度在“客户属性来源”中表示什么？ | 借助以下量度，您可以检查已上传到“客户属性”的属性状态： <ul><li>记录：属性文件中的记录数。</li><li>**新记录：**&#x200B;属性文件中存在的新记录数。</li> <li>**更新的记录：**&#x200B;已存在于“客户属性”中且文件中的值已更新的记录数。</li><li>**所有数据（记录）：**&#x200B;已成功上传到“客户属性”的记录总数。</li></ul> |
