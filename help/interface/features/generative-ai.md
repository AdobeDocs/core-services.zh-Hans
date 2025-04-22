---
title: Experience Cloud 应用程序中的 AI
description: 了解创作AI以及Experience Cloud应用程序如何使用genAI和AI Assistant。
solution: Experience Cloud
feature: AI Assistant, Generative AI
topic: Administration
role: Admin
level: Intermediate
exl-id: bdc51956-82aa-4aae-b627-a2018f80b5f5
source-git-commit: a5d595fc8ee9b76ee1bf4a24364674a3af447b2a
workflow-type: tm+mt
source-wordcount: '1109'
ht-degree: 4%

---

# Experience Cloud产品中的AI

创新型人工智能是一种人工智能，其作用不仅仅是回答问题。 它&#x200B;_创建_&#x200B;内容，_对您的_&#x200B;提示&#x200B;_做出响应_（问题和语句）。

* **创建：**&#x200B;参考AI根据其训练和输入提示从头开始生成新内容（文本、图像、音乐或视频）的能力。 此功能是创作AI的&#x200B;_创作_&#x200B;方面。

* **响应：**&#x200B;指对特定提示提供答案或反应的AI，通常利用其知识或推理能力。

如果您是Experience Cloud的新手，则可以使用创作AI快速获取产品知识。 作为经验丰富的用户，您可在几秒钟内发现运营见解，而不是几小时。

**关于AI助手**

AI Assistant是一种在Experience Platform和相关应用程序中支持的对话工具。 使用它可以加快您的工作流、改进您的产品知识、排查问题或搜索信息。 在某些应用程序中，AI Assistant可让您立即发现运营见解。

来自Experience League的产品知识响应是可验证的，并通过链接引用。 了解[基于对象的提示](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/ai-assistant/home)的类型，以充分利用AI Assistant。

[了解详情](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/landing)

<!-- **Your data remains yours**

In AI Assistant, security is the priority:

* Customer data is not used to train language models.
* AI Assistant looks at only the documents that you tell it to. You are in control.
* Your people can use AI Assistant only on documents they can access.
* It's audit-ready: Responses are attributable to source documents.
* Enterprise controls are in place to manage who has AI access in the company. -->

## Experience Cloud产品中的AI可用性

了解在Experience Cloud产品中对generative AI或AI Assistant的支持，以及是否支持Adobe Firefly。

* [GenStudio for Performance Marketing](#gspm)
* [在Experience Manager Sites中生成变体](#aem-sites)
* [Journey Optimizer 中的 AI 助手](#journey-optimizer)
* [Journey Optimizer Prime和Ultimate中的AI助手](#ajo-prime-ultimate)
* [Journey Optimizer B2B edition中的AI助手](#ajo-b2b)
* [Campaign v8 Web用户界面中的AI助手](#campaign-cs)
* [Customer Journey Analytics的人工智能助手](#cja)
* [Customer Journey Analytics中的智能字幕](#cja-captions)
* [Real-Time CDP的人工智能助手](#rtcdp)
* [Marketo中的Dynamic Chat](#marketo)
* [Workfront的人工智能助手](#workfront)

## GenStudio for Performance Marketing {#gspm}

GenStudio for Performance Marketing是一个人工智能驱动的平台，它使您能够生成和管理符合您的品牌标准并符合企业政策的营销内容。 生成电子邮件、元广告、LinkedIn广告、展示广告和横幅的内容。

您还可以使用示例、客户角色和产品的描述以及品牌指南对您的GenStudio for Performance Marketing进行品牌培训。

[了解详情](https://experienceleague.adobe.com/zh-hans/docs/genstudio-for-performance-marketing/user-guide/home)

与Adobe Firefly的兼容性：**计划**

## 在Experience Manager Sites中生成变体 {#aem-sites}

在AEM Sites中生成变体使用生成人工智能，根据提示创建内容变体。 这些提示由Adobe提供或由您创建和管理。

创建变体后，您可以在网站上使用内容，并使用Edge Delivery Services中的试验功能衡量其成功与否。 您还可以选择使用Adobe Express的创作AI功能在Firefly中生成图像。

[了解详情](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations)

与Adobe Firefly的兼容性： **是**

## Journey Optimizer 中的 AI 助手 {#journey-optimizer}

在Journey Optimizer中，使用AI Assistant获取产品知识和操作见解。 例如，询问&#x200B;_一个Journey Optimizer沙盒中可以有多少实时活动？_&#x200B;您将立即从Experience League和其他Adobe数据存储区获得答案。

AI Assistant还可以帮助提供运营见解（测试版）。 例如，您可以快速了解过去七天内创建了多少历程。

对于操作分析，AI Assistant查询特定于客户的数据存储。 数据存储包含有关[!UICONTROL 历程]的集中式操作数据。 此功能与客户无关，只能从业务对象中提取元数据。 它无法访问沙盒中的数据。

[了解详情](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant)。

与Adobe Firefly的兼容性：**否**

## Journey Optimizer Prime和Ultimate中的AI助手 {#ajo-prime-ultimate}

Journey Optimizer Prime和Ultimate使用AI Assistant for Content Accelerator为文本和图像提供主动内容变体建议。

此功能适用于电子邮件、推送通知、网页、内容和短信渠道。 它提供基于提示的文本和图像生成。 AJO Prime和Ultimate中的内容加速器输出不受影响。

[了解详情](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative)

与Adobe Firefly的兼容性： **是**

## Journey Optimizer B2B edition中的AI助手 {#ajo-b2b}

Journey Optimizer B2B edition使用AI Assistant帮助您了解产品知识。

[了解详情](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/ai-assistant/ai-assistant-overview)

与Adobe Firefly的兼容性：**否**

## Campaign v8 Web UI中的AI助手  {#campaign-cs}

Campaign Managed Cloud Services使用AI Assistant进行内容加速器。 通过此功能，您可以根据营销目标自动生成个性化、引人入胜且有效的内容，其中内容针对品牌概述的样式、布局、色调等进行了优化。 您可以跨渠道（如电子邮件、短信和推送）使用它。

**注意：**&#x200B;来自Campaign Managed Cloud Services中内容加速器的输出不受损害。

[了解详情](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-gs)

与Adobe Firefly的兼容性： **是**

## Customer Journey Analytics的人工智能助手 {#cja}

Customer Journey Analytics使用AI Assistant帮助您从Experience League中发现产品知识和见解。 如果您是新用户，请快速了解Customer Journey Analytics概念并熟悉产品和功能。

经验丰富的用户可获得高级用例或学习策略以快速执行任务。 了解概念、排查问题或搜索信息。

[了解详情](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/ai-assistant)

与Adobe Firefly的兼容性：**否**

## Customer Journey Analytics中的智能字幕 {#cja-captions}

Customer Journey Analytics中的智能字幕为最常用的Workspace可视化图表提供自然语言见解。 智能字幕非常适合需要叙述和上下文以与其他用户共享的分析师。 企业用户可以利用它快速发现高级别的收获。

[了解详情](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions)

与Adobe Firefly的兼容性：**否**

## Real-Time CDP的人工智能助手 {#rtcdp}

Real-Time CDP使用AI Assistant帮助您了解Experience League提供的产品知识。 它还提供运营见解（测试版）。 AI Assistant查询特定于客户的运营分析数据存储，该存储包含在AEP沙盒中分区的集中运营数据。 系统仅从属性、受众、数据流、数据集、目标、架构和源中提取元数据，而不访问沙盒中的数据。

例如，如果您查询受众，[!DNL AI Assistant]可以访问受众的名称和其他关联的元数据，但无法访问该受众中的配置文件。

[了解详情](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/ai-assistant/home)

与Adobe Firefly的兼容性：**否**

## Marketo中的Dynamic Chat {#marketo}

利用Adobe Dynamic Chat中由AI提供支持的创新型功能，您可以优化销售代理的生产力，获得有关网站访客意图的洞察，并以安全的方式响应访客问题。 您可以预批准问题、答案和对话摘要。

[了解详情](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/overview)

与Adobe Firefly的兼容性：**否**

## Workfront的人工智能助手 {#workfront}

Workfront中的AI Assistant通过提供应用程序内信息和建议，帮助您完成工作。 您可以：

* 获取某些对象的摘要，为您提供对象意图或详细信息的高级视图。
* 提出问题并让[!DNL AI Assistant]在Experience League上查找答案。
* 根据提示获取生成的公式。 您还可以解决计算字段中的无效自定义表达式中的错误。
* 查找项目、任务和问题。

[了解详情](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview)

与Adobe Firefly的兼容性：**否**
