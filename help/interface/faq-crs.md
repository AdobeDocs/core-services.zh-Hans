---
description: 有关 Adobe Experience Cloud、Adobe Analytics 和 Adobe Target 中客户属性的常见问题解答。
keywords: 客户属性
solution: Experience Cloud
title: '获取有关客户属性的常见问题解答 '
uuid: e93eb531-23c7-4d75-92e8-75699f58546a
feature: 客户属性
topic: 管理
role: Administrator
level: Experienced
exl-id: 6031e544-822b-4843-b3d8-98a36a3c40e8
source-git-commit: 145040facf70c6bde5c6c3fae9c7ed7f520c188d
workflow-type: tm+mt
source-wordcount: '1181'
ht-degree: 69%

---

# 有关[!UICONTROL 客户属性]的常见问题解答

Adobe Analytics和Adobe Target中[!UICONTROL 客户属性]的常见问题和最佳实践。

## 最佳实践和限制 {#section_7F5189B3DAA84EE6865B91D2026EE05A}

使用[!UICONTROL 客户属性]时的指导和限制。

| 问题 | 描述 |
|--- |--- |
| [!UICONTROL 客户属性]订阅限制 | 当您升级到 Analytics Premium 后，需要经过 24 小时的延迟才能使用更多属性。在此延迟期间，您可能会看到出现[!UICONTROL 属性订阅Max]错误。 |
| 同一台设备上的多次登录 | 使用[!UICONTROL 客户属性]将客户配置文件上传到数据源时，Adobe建议用户不要共享设备(即同一Experience CloudID)。 Experience Cloud ID (ECID) 会在设备上持续存在。如果共享设备，则可能会引发 ECID 将多位用户链接到同一 ECID，从而导致 [!DNL Target] 中出现意外结果。**注意：** 对于移动设备，安装移动设备应用程序后，ECID便会永久性存在。重新安装应用程序以生成新的ECID。对于 Web，在清除浏览器 Cookie 之后便可生成新的 ECID。 |
| 每日上传频率限制 | Adobe 建议每天只更新一次客户属性。您必须至少等待 24 小时，才能为同一组配置文件上传另一个客户配置文件数据文件。 |
| 自定义 Analytics ID (`s.visitorID`) | 使用 `s.visitorID` 设置客户 ID 是在 Analytics 中标识用户的一种方法。但是，当使用`s.visitorID.`<br>标识某个访客时，使用ID服务导出或导入[!DNL Analytics]数据的集成将不起作用。这包括但不限于共享受众、[!DNL Analytics] for Adobe Target(A4T)和[!UICONTROL 客户属性]。<br>对于这些集成，不支持设置自定义 Analytics ID。 |
|  中的字符长度限制[!DNL Analytics] | 创建[!DNL Analytics]订阅时，已上传文件的字段长度将被截断为255。 |

{style=&quot;table-layout:auto&quot;}

## 关于客户属性的常见问题解答 {#section_E47866EEA83348E09FE43CEC5E44C461}

| 问题 | 回答 |
|--- |--- |
| 我是否可以接收有关客户属性上传状态的通知？ | 可以。 |
| 我应该怎么做才能开始使用客户属性？ | <ol><li>进行配置。如果您是 Analytics 客户，Adobe 将为您配置客户属性。如果您只使用 Adobe Target 而没有使用 Analytics，请联系客户关怀团队以请求配置核心服务。</li> <li>与您的 CRM 团队进行交谈。了解哪些类型的客户数据可以在 Analytics 和整个 Experience Cloud 中使用。</li><li>实施核心服务。有关如何实现实施现代化的步骤，请参阅[启用核心服务的解决方案](core-services.md)。（请参阅有关同步客户 ID 的部分，以获取重要信息。）</li></ol> **注意：**[此处](faq.md)提供了关于实施核心服务的管理员常见问题解答。 |
| 我可以使用多少个客户属性？ | 您可以向客户属性服务上传数百个`.csv`列。 但是，在配置订阅和选择属性时，根据您拥有的解决方案，将会受到以下限制（每个报表包）：  <ul><li>Foundation：0 个</li><li>Select：3 个</li><li>Prime：15 个</li><li>Ultimate：200 个</li><li>Standard：总共允许 3 个</li><li>Premium：200 个</li><li>Adobe Target Standard：5 个</li><li>Adobe Target Premium：200 个</li></ul> |
| 是否需要迁移到 Experience Cloud ID 服务？ | 迁移取决于您使用的解决方案。 <ul><li>Adobe Analytics：强烈推荐 </li><li>Adobe Target：必需。 </li></ul><br>使用 Experience Cloud ID 服务可启用最新的 Experience Cloud 功能，其中包括实时受众、Adobe Target 现代化、Analytics 集成，以及视频检测信号跟踪。<br>有关更多详细信息，请参阅[启用核心服务的解决方案](core-services.md)。<br>**注意：**[Experience Cloud ID 服务](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=en)是以前称为 _Analytics 访客 ID 服务_ 的现代化实施。 |
| “客户属性”功能与Adobe Audience Manager有何关系？ | 虽然 Audience Manager 能够接收数据以执行受众识别，但是它无法执行将属性与历史行为数据关联起来的分析功能。此外，它也不具备 Adobe Analytics 中提供的报表、分析和分段功能。[!UICONTROL 人员]服务可将不同解决方案中的丰富数据捆绑在一起，并将其与单个 ID 关联，以在整个 Experience Cloud 中使用。<br>在 Adobe Target 中，客户属性显示为单个属性，这些属性可以与其他规则组合使用以构建受众。共享给[!UICONTROL 人员]服务的受众是完整受众，无法进行修改。 |
| **（仅限 Analytics）**&#x200B;此功能与 Analytics Premium 中提供的功能有何不同？ | 过去，有兴趣将客户属性数据与Analytics数据结合的客户在很大程度上依赖Data Workbench工具来实现此功能。 [!UICONTROL 客户] 属性通过在Reports &amp; Analytics、Ad Hoc Analysis和Report Builder中提供客户属性作为维度和量度，将此功能提供给更广泛的受众。Analytics Standard客户有权访问客户属性，但其功能有限。 Analytics Premium 客户可以使用所有功能。 |
| **（仅限 Adobe Target）**&#x200B;我是否可以为从未使用过 Adobe Target 的客户预加载或上传数据？ | 可以。当访客首次向Adobe Target发出请求时，系统会从“客户属性”中获取Adobe有关访客的现有信息，并将该数据用于定位。 **注意：**&#x200B;此数据的检索过程可能需要多达 20 分钟，从访客首次与 Adobe Target 交互开始算起。 |
| **(仅限Adobe Target)** 是否可以通过将客户属性数据与共享的受众数据相结合来创建超级受众？ | 否。共享的受众数据是一个完整的受众。 |
| **（仅限 Adobe Target）**[!UICONTROL 与 Adobe Target 的批量配置文件 API 相比，客户属性功能如何？] | 可直接通过批量配置文件 API，逐个或批量更新 Adobe Target 配置文件。该功能与客户属性类似，主要区别如下：<ul><li>配置文件 API 是一种 REST API 调用，而客户属性使用 FTP。</li><li>Adobe Target 的配置文件 API 只向 Adobe Target 发送数据，而不会向整个 Experience Cloud 发送数据。</li><li>客户属性提供了一个简单的界面，用于创建和管理此外部数据。</li></ul> |
| **（仅限 Adobe Target）**&#x200B;将数据从客户属性上传到 Adobe Target 是否可以延长 Adobe Target 访客配置文件的生命周期？ | 可以。请参阅 Adobe Target 帮助中的[访客配置文件生命周期](https://experienceleague.adobe.com/docs/target/using/audiences/visitor-profiles/visitor-profile.html?lang=en)。 |
| **（仅限 Adobe Target）**&#x200B;通过客户 ID 标识访客后，是否可以立即定位客户属性中上传的数据？ | 可以。在对Adobe Target（包括mbox第三方ID）的服务器调用中，所有客户属性数据均可用。 |
| **(仅限Adobe Target)** 对于“客户属性” **[!UICONTROL 来]** 源中上传的文件，“同步状态”列表示什么？ | Adobe Target 发布并同步的记录数可以通过单击针对某个特定属性文件的“同步状态”图标来进行查看。`Sync %` 是一个实时量度，用于指定已在Adobe Target中同步的用户档案的百分比。<br> **注意：**&#x200B;属性可能需要长达 24 小时才能与 Adobe Target 同步。 |
| 文件上传量度在“客户属性来源”中表示什么？ | 借助以下量度，您可以检查已上传到“客户属性”的属性状态： <ul><li>记录：属性文件中的记录数。</li><li>**新记录：**&#x200B;属性文件中存在的新记录数。</li> <li>**更新的记录：** 客户属性中存在且文件中的值已更新的记录数。</li><li>**所有数据（记录）：**&#x200B;已成功上传到“客户属性”的记录总数。</li></ul> |

{style=&quot;table-layout:auto&quot;}