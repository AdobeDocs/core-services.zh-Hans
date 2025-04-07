---
title: Experience Cloud应用程序中的人工智能
description: 了解Experience Cloud应用程序如何使用创作AI和AI Assistant。
solution: Experience Cloud
feature: AI Assistant, Generative AI
topic: Administration
role: Admin
level: Intermediate
hide: false
hidefromtoc: true
index: n
exl-id: bdc51956-82aa-4aae-b627-a2018f80b5f5
source-git-commit: 3f1065affe2665bb0867de02e4aef4c755c5f201
workflow-type: tm+mt
source-wordcount: '1808'
ht-degree: 4%

---

# Experience Cloud应用程序中的人工智能

本页可帮助您了解Experience Cloud应用程序如何使用创作AI，以及在何处查找特定于应用程序的信息。 了解问题、提示以及输入和输出模型的类。

## 关于创作AI和AI助手

生成AI是一种人工智能，它可以&#x200B;_创建_&#x200B;新内容和&#x200B;_对您的语句和问题（提示）做出响应_：

* **创建：**&#x200B;参考AI根据其训练和输入提示从头开始生成新内容（文本、图像、音乐或视频）的能力。 此功能是创作AI的&#x200B;_创作_&#x200B;方面。

* **响应：**&#x200B;指对特定问题、语句或提示提供答案或反应的AI，通常利用其知识或推理能力。

某些Experience Cloud应用程序会利用创新型人工智能，帮助新用户快速获取产品知识，并且经验丰富的用户可在几秒钟内发现运营见解，而不是数小时。

### AI 助手

[AI助手](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/landing)是Experience Platform和相关应用程序中支持的对话工具。 使用它可以加快您的工作流、改进您的产品知识、排查问题或搜索信息。 AI Assistant允许您在几秒钟内发现运营见解，而不是几小时。

所有产品知识答案都可验证，并可通过链接引用Experience League中的产品文档。 [了解AI Assistant](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home)以及基于对象的提示类型，以充分利用AI Assistant。

## 使用AI的Experience Cloud应用程序

>[!TIP]
>
>Subhead版本（只是一个开始）。..


* [GenStudio for Performance Marketing](#gspm)
* [Experience Manager Sites (Cloud Service)](#aem-sites)
* 更多即将出现……

### GenStudio for Performance Marketing {#gspm}

[GenStudio for Performance Marketing](https://experienceleague.adobe.com/zh-hans/docs/genstudio-for-performance-marketing/user-guide/home)是一个创作AI驱动的平台。 它在内容创建生命周期中注入了创作AI功能，这些功能可转变营销内容的创建、审阅、共享和分析方式。

_GenStudio for Performance Marketing创建_&#x200B;利用Adobe GenAI的强大功能，使营销人员和分散的团队能够创建高性能、品牌化的体验。 生成以下内容：

* 电子邮件
* 元广告
* LinkedIn广告
* 显示广告
* 横幅

您可以使用示例、客户角色和产品的描述以及品牌指南对GenStudio for Performance Marketing进行品牌培训。 [了解详情。](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/overview)

**与Adobe Firefly的兼容性：**&#x200B;已计划

### Experience Manager Sites {#aem-sites}

AEM Sites使用[生成变体](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations)。 “生成变体”使用创新型人工智能根据提示创建内容变体。 这些提示由[Adobe](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#get-started)提供，或由[用户](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#create-prompt)创建和管理。

创建变体后，您可以在网站上使用内容，并使用Edge Delivery Services的实验功能衡量其成功与否。

**输入：**&#x200B;输入字段包括：

* 要生成的变体数
* Audience Source
* 受众目标
* 其他上下文
* 客户驱动提示

**输出：**&#x200B;生成的内容/市场副本。 您还可以选择使用Adobe Express的创作AI功能在Firefly中生成图像。

请参阅[生成图像](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#generate-image)。

**与Adobe Firefly的兼容性：**&#x200B;是

## Adobe Journey Optimizer

Journey Optimizer使用[AI助手](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home)来回答两类问题：

**产品知识** — 查询Adobe数据存储区(如Experience League产品文档)以了解产品insight。 此输出不受客户限制。 示例：

* 一个Adobe Journey Optimizer沙盒中可以有多少个实时活动？

**Operational Insights (Beta)** — 查询特定于客户的操作分析数据存储区，该数据存储区包含有关历程的集中操作数据，并按客户的沙盒进行分区。 仅从业务对象中提取元数据，而不访问沙盒中的数据。

* 过去七天创建了多少历程？

运营见解输出取决于从客户的业务对象中拉取的元数据。

历程是Journey Optimizer中唯一可用于AI助手的对象，并且元数据是从当前沙盒中提取的。

查看[使用AI助手](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant)和[字段准备工作](https://fieldreadiness-adobe.highspot.com/items/6661f1c132683fd5e6a8adf4?lfrm=srp.1#11)以了解更多信息。

**与Adobe Firefly的兼容性：**&#x200B;否



## 使用AI的Experience Cloud应用程序

>[!TIP]
>
>表版本……


了解Experience Cloud应用程序如何使用创作AI或AI Assistant，以及是否支持Adobe Firefly。

| 应用程序 | 如何使用创作AI | 示例 | Adobe Firefly？ |
|----------|------------|-----------|----------------|
| GenStudio for Performance Marketing | [GenStudio for Performance Marketing](https://experienceleague.adobe.com/zh-hans/docs/genstudio-for-performance-marketing/user-guide/home)是一个创作AI驱动的平台。 它在内容创建生命周期中注入了创作AI功能，这些功能可转变营销内容的创建、审阅、共享和分析方式。<br>您可以使用示例、客户角色和产品的描述以及品牌准则来培训GenStudio for Performance Marketing的品牌知识。 | _GenStudio for Performance Marketing创建_&#x200B;允许您生成电子邮件、中继广告、LinkedIn广告、展示广告和横幅的内容。 <br>**输入：** <ul><li>使用模板开始内容创建过程。 </li><li>添加品牌、产品和角色（准则）和内容（资产）等参数以塑造生成的体验。 </li><li>输入描述性提示，用于描述要生成的上下文或体验。 [了解详情...](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/overview)</li></ul> | 是 |
| Adobe Experience Manager Sites (Cloud Service) | AEM Sites使用[生成变体](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations)。 <br>生成变体使用生成人工智能，根据提示创建内容变体。 这些提示由Adobe提供或由用户创建和管理。 | 创建变体后，您可以在网站上使用内容，并使用Edge Delivery Services的实验功能衡量其成功与否。 <br>**输入：**&#x200B;输入字段包括要生成的变体数；受众Source/受众目标；其他上下文和客户驱动提示。 <ul><li>[Adobe提示模板](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#get-started) </li><li>[用户生成的提示](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#create-prompt)</li></ul> **输出：**&#x200B;生成的内容/市场副本。 您还可以选择使用Adobe Express的创作AI功能在Firefly中生成图像。 请参阅[生成图像](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#generate-image)。 | 是 |
| Adobe Journey Optimizer | Journey Optimizer使用[AI助手](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home)来回答两类问题：<ul><li>**产品知识** — 查询Adobe数据存储区(如Experience League产品文档)以了解产品insight。 此输出不受客户限制。 </li><li>**Operational Insights (Beta)** — 查询特定于客户的操作分析数据存储区，该数据存储区包含有关历程的集中操作数据，并按客户的沙盒进行分区。 仅从业务对象中提取元数据，而不访问沙盒中的数据。</li></ul> | <ul><li>**产品知识输入：**&#x200B;一个Adobe Journey Optimizer沙盒中可以有多少实时活动？</li><li>**产品知识输出：**&#x200B;从Experience League提取的产品知识（公共文档）。 </li><li>**运营分析输入：**&#x200B;过去七天中创建了多少历程？ </li><li>**Operational Insights输出：** Operational Insights输出取决于从客户的业务对象提取的元数据。 历程是AJO中唯一可用的对象，并且元数据是从当前沙盒中提取的。 </li></ul> 查看[使用AI助手](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant)和[字段准备工作](https://fieldreadiness-adobe.highspot.com/items/6661f1c132683fd5e6a8adf4?lfrm=srp.1#11) | 否 |
| Journey Optimizer：_Prime_&#x200B;和&#x200B;_Ultimate_ | [内容加速器的AI助手](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative)为文本和图像提供主动内容变体建议。 它可用于电子邮件、推送、Web和短信渠道。 这项新功能提供了基于提示的文本和图像生成功能。 | <ul><li> **电子邮件** — 生成完整电子邮件、纯文本或纯图像。 [了解详情...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-email) </li><li> **推送通知** — 生成完整的推送通知、纯文本或纯图像。 [了解详情...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-push) </li><li> **短信** — 生成完整的短信或仅发送文本。 [了解详情](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-sms) </li><li> **网页** — 生成网页图像或网页文本。 [了解详情...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-web) </li><li> **内容** — 为各种消息传递活动生成内容。 [了解详情...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-experimentation)</li></ul> **注意：** AJO Prime和Ultimate中内容加速器的输出不受损害。 | 是 |
| Journey Optimizer B2B 版本 | 使用[AI助手](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/ai-assistant)有一个类问题： <br> **产品知识** — 查询Adobe数据存储区(如Experience League产品文档)以了解产品insight。 此输出不受客户限制。 | <ul><li>**输入：**&#x200B;如何在帐户历程中发送电子邮件？</li><li>**输出：**&#x200B;产品知识从Experience League提取（公共文档）。 [了解详情...](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/ai-assistant)</li></ul> | 否 |
| Campaign托管式云服务 | [内容加速器人工智能助手](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-gs)根据营销目标自动生成个性化、引人入胜且有效的内容，内容在电子邮件、短信、推送等渠道间针对品牌概述的样式、布局、音调等进行了优化。 | <ul><li> **电子邮件** — 生成完整电子邮件、纯文本或纯图像。 [了解详情](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-content) </li><li> **短信** — 仅生成完整的短信或文本。 [了解详情...](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-sms) </li><li> **推送** — 制作引人注目的消息并生成内容。 [了解详情...](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-push) </li></ul> **注意：**&#x200B;来自Campaign Managed Cloud Services中内容加速器的输出不受损害。 | 是 |
| Customer Journey Analytics | CJA使用[AI助手](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/ai-assistant)帮助您从Experience League中探索产品知识和见解。 <br>例如，新用户可以使用它来了解Customer Journey Analytics概念，并了解您不熟悉的产品和功能。 <br>经验丰富的用户可以使用AI Assistant提供更高级的用例或提示和技巧，并快速执行任务。 了解概念、排查问题或搜索信息。 [了解详情...](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/ai-assistant#knowledge) | <ul><li>**产品知识输入：**&#x200B;如何生成计算量度？ </li><li> **产品知识输出：**&#x200B;从Experience League提取的产品知识（公共文档）。 </li></ul> | 否 |
| Customer Journey Analytics | [智能字幕](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions)为Workspace可视化中的线条可视化提供自然语言见解。 | <ul><li>**输入：**&#x200B;行可视化。 当您单击&#x200B;**智能字幕**&#x200B;时，字幕会根据此类行可视化自动生成。 </li><li> **输出：**&#x200B;自动生成的自然语言字幕。</li></ul> | 否 |
| Real-Time CDP | 使用[AI助手](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home)帮助您从Experience League中发现产品知识和见解。 它查询数据库并将数据库中的数据转换为人类可读的答案。 两类问题： <br> **产品知识** — 查询Adobe数据存储区(如Experience League产品文档)以了解产品insight。 此输出不受客户限制。<br> **Operational Insights (Beta)** — 查询特定于客户的操作分析数据存储区，该数据存储区包含按客户的AEP沙盒进行分区的集中式操作数据。 仅从属性、受众、数据流、数据集、目标、架构和源中提取元数据，并不访问沙盒中的数据。 <br>例如，对于有关受众的查询，[!DNL AI Assistant]可以访问受众的名称和其他关联的元数据，但无法访问该受众内的配置文件。 | <ul><li>**产品知识输入：**&#x200B;如何计算配置文件丰富度？ </li><li>**产品知识输出：**&#x200B;从Experience League提取的产品知识（公共文档）。 </li><li> **操作分析输入：**&#x200B;我有多少数据集？ </li><li> **Operational Insights输出：** Operational Insights输出取决于从客户的业务对象（属性、受众、数据流、数据集、目标、架构和源）提取的元数据，并包括指向包含查询数据的特定UI页面的链接。 </li></ul>有关示例，请参阅Experience Platform中的[AI助手](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home)中的&#x200B;_产品知识_&#x200B;和&#x200B;_操作分析_&#x200B;输入表 | 否 |
| Marketo | [Dynamic Chat](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/dynamic-chat-overview)通过自定义和预批准的问题和答案以及对话摘要创建人工智能辅助对话 | <ul><li> **生成问题：**&#x200B;提供从中提取内容并用于生成问题/响应的URL。 </li><li> **对话摘要：**&#x200B;生成聊天对话摘要。 </li></ul> [了解详情...](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/response-library) | 否 |
| Workfront | Workfront中的[AI助手](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview)通过在自然语言对话中提供应用程序内信息和建议，帮助您完成工作。 AI Assistant提供以下功能：汇总项目/任务/问题/文档，提供从Experience League上的Workfront文档提取的说明或参考信息，为计算的自定义字段生成或优化公式。 | <ul><li>**汇总项目输入：**&#x200B;汇总此项目 </li><li> **概述项目输出：**&#x200B;返回项目用途和状态的简短描述，给出已完成和仍在等待中的任务的示例，并提供一些其他详细信息和说明。</li><li> **生成/优化公式输入：**“重写此公式以删除无效的表达式错误。” </li><li> **生成/优化公式输出：**&#x200B;已生成或优化公式。 </li></ul>**注意：** AI Assistant可能需要一些时间来生成修订的公式，具体取决于公式的大小和复杂性。 | 否 |
