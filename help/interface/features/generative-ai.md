---
title: Experience Cloud 应用程序中的 AI
description: 了解创作AI以及Experience Cloud应用程序如何使用genAI和 [!DNL AI Assistant]。
solution: Experience Cloud
feature: AI Assistant, Generative AI
topic: Administration
role: Admin
level: Intermediate
exl-id: bdc51956-82aa-4aae-b627-a2018f80b5f5
source-git-commit: c97ace2c192517a49a01c4247d9f6b4220e0514d
workflow-type: tm+mt
source-wordcount: '1103'
ht-degree: 3%

---

# Experience Cloud产品中的AI

本页可帮助您了解哪些产品支持创作AI [!DNL AI Assistant]，以及Adobe Firefly是否兼容。 您还可以找到指向产品特定帮助资源的链接，这些帮助资源介绍了如何在Experience Cloud中使用AI。

**关于生成AI**

创新型人工智能是一种人工智能，其作用不仅仅是回答问题。 它可以&#x200B;_创建_&#x200B;内容并&#x200B;_生成对您的问题或语句（称为_&#x200B;提示&#x200B;_）的响应_。

* **创建：**&#x200B;人工智能根据其训练和输入提示从头开始生成内容（文本、图像、音乐或视频）的能力。 此功能是创作AI的&#x200B;_创作_&#x200B;方面。

* **生成响应：**&#x200B;人工智能对提示提供答案或反应，通常利用其可用的数据和知识存储库。

利用创新型人工智能，如果您不熟悉Experience Cloud，则可以快速获取产品知识。 经验丰富的用户只需几秒钟即可获得运营洞察，而无需花费数小时。

**是什么 [!DNL AI Assistant]？**

[!DNL AI Assistant]是Experience Platform和相关应用程序中支持的对话工具。 这些应用程序使用它的方式类似，但具有特定于产品的优势。 使用它可以加快您的工作流程、提升您的产品知识、排查问题或搜索信息并查找运营见解。 在某些应用程序中，[!DNL AI Assistant]允许您立即发现运营见解。

**产品知识：**&#x200B;产品知识是指以Experience League文档为基础的概念和主题。 来自Experience League的响应是可验证的，并通过链接引用。 了解[基于目标的提示](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/ai-assistant/home)的类型，以充分利用[!DNL AI Assistant]。

**Operational Insights：** Operational Insights是指Answers AI Assistant生成的有关元数据对象（属性、受众、数据流、数据集、目标、旅程、架构和源）的信息，包括计数、查找和谱系影响。

[了解详情](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/landing)

<!-- **Your data remains yours**

In AI Assistant, security is the priority:

* Customer data is not used to train language models.
* AI Assistant looks at only the documents that you tell it to. You are in control.
* Your people can use AI Assistant only on documents they can access.
* It's audit-ready: Responses are attributable to source documents.
* Enterprise controls are in place to manage who has AI access in the company. -->

## Experience Cloud产品中的AI可用性

了解在Experience Cloud产品中支持创作AI或[!DNL AI Assistant]，以及是否支持Adobe Firefly。

* [[!DNL GenStudio for Performance Marketing]](#gspm)
* [[!DNL Experience Manager Sites]](#aem-sites)
* [[!DNL Journey Optimizer]](#journey-optimizer)
* [[!DNL Journey Optimizer] Prime和Ultimate](#ajo-prime-ultimate)
* [[!DNL Journey Optimizer] B2B edition](#ajo-b2b)
* [[!DNL Campaign] v8 Web用户界面](#campaign-cs)
* [[!DNL Customer Journey Analytics]](#cja)
* [[!DNL Customer Journey Analytics]](#cja-captions)
* [[!DNL Real-Time CDP]](#rtcdp)
* [[!DNL Marketo]](#marketo)
* [[!DNL Workfront]](#workfront)

## GenStudio for Performance Marketing {#gspm}

[!DNL GenStudio for Performance Marketing]是一个人工智能驱动的平台，它使您能够生成和管理符合您的品牌标准并符合企业政策的营销内容。 生成电子邮件、元广告、LinkedIn广告、展示广告和横幅的内容。

您还可以使用示例、客户角色和产品的描述以及品牌指南对您的GenStudio for Performance Marketing进行品牌培训。

[了解详情](https://experienceleague.adobe.com/zh-hans/docs/genstudio-for-performance-marketing/user-guide/home)

与Adobe Firefly的兼容性： **是**

## [!DNL Experience Manager Sites] {#aem-sites}

在AEM Sites中，您可以使用[!UICONTROL 生成变体]根据提示创建内容变体。 这些提示由Adobe提供或由您创建和管理。

创建变体后，您可以在网站上使用内容，并使用Edge Delivery Services中的试验功能衡量其成功与否。 您还可以选择使用Adobe Express的创作AI功能在Firefly中生成图像。

[了解详情](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations-integrated-editor)

与Adobe Firefly的兼容性： **是**

## [!DNL Journey Optimizer] {#journey-optimizer}

在[!DNL Journey Optimizer]中，使用[!DNL AI Assistant]获取产品知识和操作见解。 例如，询问&#x200B;_一个Journey Optimizer沙盒中可以有多少实时活动？_&#x200B;您将立即从Experience League和其他Adobe数据存储区获得答案。

[!DNL AI Assistant]还可以帮助提供运营分析（测试版）。 例如，您可以快速了解过去七天内创建了多少历程。

对于运营分析，[!DNL AI Assistant]查询特定于客户的数据存储。 数据存储包含有关[!UICONTROL 历程]的集中式操作数据。 此功能与客户无关，只能从业务对象中提取元数据。 它无法访问沙盒中的数据。

[了解详情](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant)。

与Adobe Firefly的兼容性：**否**

## [!DNL Journey Optimizer] Prime和Ultimate {#ajo-prime-ultimate}

[!DNL Journey Optimizer] Prime和Ultimate使用[!DNL AI Assistant]生成内容，为文本和图像提供主动内容变体建议。

此功能适用于电子邮件、推送通知、网页、内容和短信渠道。 它提供基于提示的文本和图像生成。 AJO Prime和Ultimate中内容生成的输出不会受到任何影响。

[了解详情](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative)

与Adobe Firefly的兼容性： **是**

## [!DNL Journey Optimizer B2B Edition] {#ajo-b2b}

Journey Optimizer B2B edition使用[!DNL AI Assistant]帮助您了解产品知识。

[了解详情](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/ai-assistant/ai-assistant-overview)

与Adobe Firefly的兼容性：**否**

## [!DNL Campaign] v8 Web UI {#campaign-cs}

Campaign Managed Cloud Services使用[!DNL AI Assistant]生成内容。 通过此功能，您可以根据营销目标自动生成个性化、引人入胜且有效的内容，其中内容针对品牌概述的样式、布局、色调等进行了优化。 您可以跨渠道（如电子邮件、短信和推送）使用它。

**注意：** Campaign Managed Cloud Services中内容生成的输出不受损害。

[了解详情](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-gs)

与Adobe Firefly的兼容性： **是**

## [!DNL Customer Journey Analytics] {#cja}

Customer Journey Analytics使用[!DNL AI Assistant]来帮助您从Experience League中发现产品知识和见解。 如果您是新用户，请快速了解Customer Journey Analytics概念并熟悉产品和功能。

经验丰富的用户可获得高级用例或学习策略以快速执行任务。 了解概念、排查问题或搜索信息。

[了解详情](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/ai-assistant)

与Adobe Firefly的兼容性：**否**

## [!DNL Customer Journey Analytics] {#cja-captions}

您可以在[!DNL Customer Journey Analytics]中使用&#x200B;_智能字幕_&#x200B;以获得最常用Workspace可视化图表的自然语言见解。 智能字幕非常适合需要叙述和上下文以与其他用户共享的分析师。 企业用户可以利用它快速发现高级别的收获。

例如：

* **输入：**&#x200B;在CJA中，运行支持的可视化图表（包括折线图、面积图、条形图、流量或流失），然后单击&#x200B;**[!UICONTROL 智能字幕]**。

* **输出：**&#x200B;查看自动生成的自然语言字幕，其中显示上下文和键收藏。 然后，您可以对生成的数据执行一些操作，如查看、复制数据并与您的组织共享。 [查看方式](https://video.tv.adobe.com/v/3420131/?quality=12&learn=on#_blank)

[了解详情](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions)

与Adobe Firefly的兼容性：**否**

## [!DNL Real-Time CDP] {#rtcdp}

Real-Time CDP使用[!DNL AI Assistant]帮助您了解Experience League的产品知识。 它还提供运营见解（测试版）。 [!DNL AI Assistant]查询特定于客户的操作分析数据存储区，其中包含在AEP沙盒中分区的集中化操作数据。 系统仅从属性、受众、数据流、数据集、目标、架构和源中提取元数据，而不访问沙盒中的数据。

例如，如果您查询受众，[!DNL AI Assistant]可以访问受众的名称和其他关联的元数据，但无法访问该受众中的配置文件。

[了解详情](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/ai-assistant/home)

与Adobe Firefly的兼容性：**否**

## [!DNL Marketo] {#marketo}

利用Adobe Dynamic Chat中由AI提供支持的创新型功能，您可以优化销售代理的生产力，获得有关网站访客意图的洞察，并以安全的方式响应访客问题。 您可以预批准问题、答案和对话摘要。

[了解详情](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/overview)

与Adobe Firefly的兼容性：**否**

## [!DNL Workfront] {#workfront}

[!DNL Workfront]中的[!DNL AI Assistant]通过提供应用程序内信息和建议帮助您完成工作。 您可以：

* 获取某些对象的摘要，为您提供对象意图或详细信息的高级视图。
* 提出问题并让[!DNL AI Assistant]在Experience League上查找答案。
* 根据提示获取生成的公式。 您还可以解决计算字段中的无效自定义表达式中的错误。
* 查找项目、任务和问题。

[了解详情](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview)

与Adobe Firefly的兼容性：**否**
