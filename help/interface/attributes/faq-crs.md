---
description: 关于 Analytics 和 Target 中的客户属性的常见问题解答和最佳实践
keywords: customer attributes
seo-description: 关于 Analytics 和 Target 中的客户属性的常见问题解答和最佳实践
seo-title: 常见问题解答、各种限制和最佳实践
solution: Experience Cloud
title: 常见问题解答、各种限制和最佳实践
uuid: e93eb531-23c7-4d75-92e8-75699f58546a
translation-type: tm+mt
source-git-commit: 31811e718be130612c8688e80084cb7579e94f47

---


# 常见问题解答、各种限制和最佳实践

关于 Analytics 和 Target 中的客户属性的常见问题解答和最佳实践

## 最佳实践和限制 {#section_7F5189B3DAA84EE6865B91D2026EE05A}

使用客户属性时的指 [!UICONTROL 导和限制]。

| 问题 | 描述 |
|--- |--- |
| [!UICONTROL 客户属性] 订阅限制 | 升级到Analytics Premium后，在提供其他属性之前会有24小时的延迟。 在此延迟期间，您可能会看到出现属性订阅达到最大值错误。 |
| 同一设备上的多个登录 | 使用客户属性将客户用户档案上传到数据源时，Adobe建议共享同一设备（即相同的Experience Cloud ID）的用户不要这样做。 这样做可能导致ECID服务（该服务在设备上仍然存在）在同一Experience Cloud ID下链接多个用户，从而导致意外结果 [!DNL Target]。 **注意：** 对于Mobile，安装Mobile应用程序后ECID将永久存在，您必须重新安装该应用程序才能生成新ECID。 对于Web，在清除浏览器cookie后将生成新ECID。 |
| 每日频率上传限制 | Adobe建议您每天只更新一次客户属性。 您必须至少等待24小时，才能为同一组用户档案上传其他客户用户档案数据文件。 |
| 自定义分析ID(`s.visitorID`) | 使用 `s.visitorID` 设置客户 ID 是在 Analytics 中标识用户的一种方法。但是，当使用共享访客(包括但不限于共享受众、Analytics for Adobe目标(A4T)和客户属性)进行标识时，使用ID服务导出或导入Analytics数据的集成将不起作用。 `s.visitorID.`<br><br>对于这些集成，不支持设置自定义 Analytics ID。 |
| Analytics中的字符长度限制 | 创建分析订阅时，已上传文件的字段长度将截断为255。 |

## 关于客户属性的常见问题解答 {#section_E47866EEA83348E09FE43CEC5E44C461}

| 问题 | 回答 |
|--- |--- |
| 我是否可以接收有关客户属性的上传状态的通知？ | 可以。请参阅[管理通知](https://docs.adobe.com/content/help/en/core-services/interface/manage-users-and-products/organizations.html#concept_0105453AD71847B8BFCAF4A40915F157)。 |
| 如何开始使用客户属性？ | <ol><li>设置。 如果您是Analytics客户，Adobe将为您配置客户属性。 如果您仅使用Adobe目标，且没有Analytics，则必须联系客户服务部门请求核心服务的配置。</li> <li>与您的CRM团队进行对话。 了解在Analytics和整个Experience Cloud中使用的有趣客户数据类型。</li><li>实施核心服务。 有关如 [何实现实施现代化的步骤](https://docs.adobe.com/content/help/zh-Hans/core-services/interface/about-core-services/core-services.html) ，请参阅为核心服务启用解决方案。 （有关重要信息，请参阅关于同步客户ID的部分。）</li></ol> **注意：** 此处提供管理员实施核心服务的常见问题 [解答](https://docs.adobe.com/content/help/en/core-services/interface/manage-users-and-products/faq.html#concept_13219B4E51784577B6FF78AAA203DE91)。 |
| 我可以使用多少个客户属性？ | You can upload hundreds of `.csv` columns to the customer attribute service. 但是，在配置订阅和选择属性时，会根据您拥有的解决方案采用以下限制（每个报告包）:  <ul><li>Foundation：0 个</li><li>Select：3 个</li><li>Prime：15 个</li><li>Ultimate：200 个</li><li>Standard：总共允许 3 个</li><li>高级： 200</li><li>Adobe目标标准： 5</li><li>Adobe目标Premium: 200</li></ul> |
| 是否需要迁移到Experience Cloud ID服务？ | 迁移取决于您使用的解决方案。 <ul><li>Adobe Analytics:  强烈建议 </li><li>Adobe目标: 必需。 </li></ul><br> 使用ID服务可增强该功能，为使用最新的Experience Cloud功能(包括实时受众、Adobe目标现代化、Analytics集成和视频心跳跟踪)打开大门。 <br> 有关详细信息，请 [参阅启用核心服务解决方案](https://docs.adobe.com/content/help/zh-Hans/core-services/interface/about-core-services/core-services.html)。 <br>**注意：** Experience Cloud [ID服务是](https://docs.adobe.com/content/help/zh-Hans/id-service/using/intro/overview.html) “Analytics访客ID”服务的现代 _化实施。_ |
| 客户属性功能与Adobe受众管理器有何关系？ | 虽然受众管理器可以接收数据以执行受众识别，但它无法执行将属性与历史行为数据关联的分析功能，也无法提供Adobe Analytics中提供的报告、分析和细分功能。 [!UICONTROL People] 支持将不同解决方案中的丰富数据绑定在一起并与单个ID关联，以便在Experience Cloud中使用。 <br>在Adobe目标中，客户属性显示为单个属性，这些属性可以与其他规则结合以构建受众。 共享给People服 [!UICONTROL 务的受众] 是无法修改的完整受众。 |
| **（仅限Analytics）** ，此功能与Analytics Premium中提供的功能有何不同？ | 过去，有意将客户属性数据与Analytics数据相结合的客户严重依赖数据工作台工具来实现此功能。 客户属性在报告和分析、专门受众和报告构建器中提供作为维度和指标的客户属性，从而使这一功能面向更广泛的分析。 Analytics Standard客户将有权访问客户属性，但功能有限。 Analytics Premium客户可以获得完整功能。 |
| **(仅限Adobe目标** )我是否可以为Adobe目标从未见过的客户预加载或上传数据？ | 可以。当访客向Adobe目标提出第一个请求时，系统将从客户属性中获取我们现有的关于他们的信息，并使用该数据进行定位。 **注意：**  检索此访客最长可能需要20分钟时间，这是与Adobe目标的首次交互。 |
| **(仅限Adobe目标** )我是否可以通过将客户属性数据与共享受众数据相结合来创建超级受众? | 否。共享受众数据是已完成的受众。 |
| **(仅限Adobe目标** )客户属性功能与Adobe目标的批量用户档案API相比如何？ | 批量用户档案API使Adobe目标用户档案能够直接通过API进行更新，无论是针对单个用户档案还是批量更新。 该功能与客户属性类似，主要区别如下：<ul><li>用户档案API是REST API调用，客户属性使用FTP。</li><li>Adobe目标的用户档案API只向Adobe目标发送数据，而不是向整个Experience Cloud发送数据。</li><li>客户属性提供了创建和管理此外部数据的简单界面。</li></ul> |
| **(仅限Adobe目标** )将客户属性中的数据上传到Adobe目标是否会延长Adobe目标访客的用户档案寿命？ | 可以。请参阅 Adobe Target 帮助中的[访客配置文件生命周期](https://docs.adobe.com/content/help/en/target/using/audiences/visitor-profiles/visitor-profile.html)。 |
| **(仅限Adobe目标** )在客户ID识别访客后，能否立即目标在客户属性中上传的数据？ | 可以。在对Adobe目标（包括mbox第三方ID）的服务器调用中，将提供所有客户属性数据。 |
| **(仅限Adobe目标** )“同步状 **[!UICONTROL 态]** ”列对于客户属性源中上传的文件表示什么？ | Adobe目标发布和同步的记录数可通过单击特定属性文件的“同步状态”图标来查看。 `Sync %` 是一个实时度量，它指定在Adobe用户档案中同步的目标的%。<br> **注意：** 属性与Adobe目标同步可能需要24小时。 |
| 文件上传量度在客户属性来源中表示什么？ | 您可以借助以下指标检查上传到客户属性的属性的状态： <ul><li>记录：  属性文件中的记录数。</li><li>**新记录：** 属性文件中存在的新记录数。</li> <li>**更新的记录：** 其中已存在于“客户属性”中且文件中具有更新值的记录数。</li><li>**所有数据（记录）:** 成功上传到客户属性的记录总数。</li></ul> |
