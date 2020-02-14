---
description: 关于 Analytics 和 Target 中的客户属性的常见问题解答和最佳实践
keywords: customer attributes
seo-description: 关于 Analytics 和 Target 中的客户属性的常见问题解答和最佳实践
seo-title: 常见问题解答、各种限制和最佳实践
solution: Experience Cloud
title: 常见问题解答、各种限制和最佳实践
uuid: e93eb531-23c7-4d75-92e8-75699f58546a
translation-type: tm+mt
source-git-commit: 5028e1c4a2b5d9d0c225e2bbb36ef2c5a91c5ad9

---


# 常见问题解答、各种限制和最佳实践

关于 Analytics 和 Target 中的客户属性的常见问题解答和最佳实践

## 最佳实践和限制 {#section_7F5189B3DAA84EE6865B91D2026EE05A}

使用客户属性的指导和限制。

| 问题 | 描述 |
|--- |--- |
| 客户属性订阅限制 | 当您升级到 Analytics Premium 时，附加属性会在延迟 24 小时后才可用。在此延迟期间，您可能会看到出现属性订阅达到最大值错误。 |
| 同一设备上的多个登录 | 当使用客户属性将客户档案上传到数据源时，Adobe建议共享相同设备（即同一Experience Cloud ID）的用户不要这样做。 这样做可能导致ECID服务（该服务在设备上仍然存在）在同一Experience Cloud ID下链接多个用户，从而导致意外结果 [!DNL Target]。 **** 注意：对于Mobile，安装Mobile应用程序后ECID是永久的，您必须重新安装该应用程序才能生成新ECID。 对于Web，在清除浏览器Cookie后将生成新ECID。 |
| 每日频率上传限制 | Adobe建议您每天只更新一次客户属性。 您必须等待至少24小时才能为同一组配置文件上传另一个客户配置文件数据文件。 |
| Custom Analytics ID (`s.visitorID`) | 使用 `s.visitorID` 设置客户 ID 是在 Analytics 中标识用户的一种方法。但是，当使用 `s.visitorID.`<br>This包括（但不限于）共享受众、Analytics for Target(A4T)和客户属性来标识访客时，使用ID服务导出或导入Analytics数据的集成将不起作用。<br>对于这些集成，不支持设置自定义 Analytics ID。 |
| Analytics 中的字符长度限制 | 在创建 Analytics 订阅时，上传文件的字段长度会被截断为 255 个字符。 |

## 关于客户属性的常见问题解答 {#section_E47866EEA83348E09FE43CEC5E44C461}

| 问题 | 回答 |
|--- |--- |
| 我能收到关于客户属性上传状态的通知吗？ | 可以。请参阅[管理通知](https://docs.adobe.com/content/help/en/core-services/interface/manage-users-and-products/organizations.html#concept_0105453AD71847B8BFCAF4A40915F157)。 |
| 若要初步了解客户属性，我需要做哪些工作？ | <ol><li>进行配置。如果您是 Analytics 客户，Adobe 则会为您配置客户属性。如果您仅使用 Target 并且不具备 Analytics，则必须联系客户关怀团队，以请求配置核心服务。</li> <li>与您的 CRM 团队进行沟通。找出哪类客户数据可以在 Analytics 及整个 Experience Cloud 中使用。</li><li>实施核心服务。有关如 [何实现实施现代化的步骤](https://docs.adobe.com/content/help/en/core-services/interface/about-core-services/core-services.html) ，请参阅为核心服务启用解决方案。 （请参阅关于同步客户 ID 的部分，以了解重要信息。）</li></ol> **注意：**&#x200B;有关针对管理员的核心服务实施常见问题解答，请访问[此处](https://docs.adobe.com/content/help/en/core-services/interface/manage-users-and-products/faq.html#concept_13219B4E51784577B6FF78AAA203DE91)。 |
| 我可以使用多少个客户属性？ | You can upload hundreds of `.csv` columns to the customer attribute service. 但是，在配置订阅和选择属性时，会根据您拥有的解决方案应用以下限制（每个报表包）:  <ul><li>Foundation：0 个</li><li>Select：3 个</li><li>Prime：15 个</li><li>Ultimate：200 个</li><li>Standard：总共允许 3 个</li><li>高级：200</li><li>Target Standard：5 个</li><li>Target Premium：200 个</li></ul> |
| 必须要迁移到 Experience Cloud ID 服务吗？ | 迁移与否取决于您使用的解决方案。 <ul><li>Adobe Analytics：强烈建议迁移 </li><li>Adobe Target：必须迁移。 </li></ul><br>使用 ID 服务可增强该功能，并使您有机会使用最新的 Experience Cloud 功能，包括实时受众、Target 现代化、Analytics 集成和视频心跳跟踪。<br> 有关详细信息，请参 [阅为核心服务启用解决方案](https://docs.adobe.com/content/help/en/core-services/interface/about-core-services/core-services.html)。 <br>**注意：** [Experience Cloud ID服务是对以前称为](https://docs.adobe.com/content/help/en/id-service/using/intro/overview.html)_Analytics访客ID服务的现代化实施。_ |
| 客户属性功能如何与 Adobe Audience Manager 关联？ | 虽然 Audience Manager 可以接收数据以执行受众识别，它却无法执行分析功能以将属性关联到历史行为数据，或提供 Adobe Analytics 中可用的报告、分析和区段功能。“人员”核心服务允许绑定来自不同解决方案的大量数据，并与单一 ID 关联，进而可以在 Experience Cloud 中使用。<br>在 Adobe Target 中，客户属性显示为单独的属性，它们可以与其他规则组合在一起，以便构建受众。“人员”核心服务中共享的受众属于完整的受众，无法对其进行修改。 |
| **（仅限 Analytics）**&#x200B;此功能与 Analytics Premium 中提供的功能有何区别？ | 以前，如果客户希望将客户属性数据与 Analytics 数据组合在一起，他们需要大大依赖 Data Workbench 工具来实现此功能。通过将客户属性作为 Reports &amp; Analytics、Ad Hoc Analysis 和 Report Builder 中的维度和量度，使更多受众有机会使用此功能。Analytics Standard 客户将有权访问客户属性，但其功能有限。Analytics Premium 客户可以使用其完整的功能。 |
| **（仅限 Target）**&#x200B;我可以预先加载或上传从未在 Target 中出现过的客户数据吗？ | 可以。在访客向 Target 提出第一个请求时，系统将从客户属性中提取我们目前所拥有的关于他们的信息，并使用该数据进行定位。**注意：**&#x200B;此数据的检索过程可能需要多达 20 分钟，从访客首次与 Target 交互开始算起。 |
| **（仅限 Target）**&#x200B;我可以通过将客户属性数据与共享受众数据合并在一起来创建超级受众吗？ | 否。共享受众数据是已完成的受众。 |
| **（仅限 Target）**&#x200B;客户属性功能与 Target 的批量配置文件 API 相比有何不同？ | 可直接通过批量配置文件 API，逐个或批量更新 Target 配置文件。该功能类似于客户属性，但又存在以下不同之处： <ul><li>配置文件 API 是一个 REST API 调用，而客户属性使用的是 FTP。 </li><li>Target 的配置文件 API 仅向 Target 而并非向整个 Experience Cloud 发送数据。 </li><li>客户属性提供了一个简单的界面来创建和管理此外部数据。 </li></ul> |
| **（仅限 Target）**&#x200B;从客户属性向 Adobe Target 上传数据时，是否会延长 Target 访客的配置文件生命周期？ | 可以。请参阅 Adobe Target 帮助中的[访客配置文件生命周期](https://docs.adobe.com/content/help/en/target/using/audiences/visitor-profiles/visitor-profile.html)。 |
| **（仅限 Target）**&#x200B;根据客户 ID 识别访客后，我能否立即定位在客户属性中上传的数据？ | 可以。在对 Target 进行的服务器调用中（其中包括 mbox 第三方 ID），所有客户属性数据都将可用。 |
| **（仅限Target）** “同步状态” **** 列代表在“客户属性来源”中上传的文件的哪些内容？ | 通过单击特定属性文件的“同步状态”图标，可以查看由Target发布和同步的记录数。 `Sync %` 是一个实时度量，它指定在Target中同步的配置文件的%。<br> **** 注意：与Target同步的属性可能需要24小时。 |
| 文件上传量度在客户属性来源中表示什么？ | 您可以借助以下指标检查上传到客户属性的属性的状态： <ul><li>记录： 属性文件中的记录数。</li><li>**** 新记录：属性文件中存在的新记录数。</li> <li>**** 更新的记录：其中已存在于“客户属性”中且文件中具有更新值的记录数。</li><li>**** 所有数据（记录）:成功上传到客户属性的记录总数。</li></ul> |
