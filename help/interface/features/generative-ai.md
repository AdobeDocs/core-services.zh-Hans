---
title: Experience Cloud应用程序中的创新型人工智能
description: 了解创作AI (GenAI)以及Experience Cloud应用程序如何使用GenAI和 [!DNL AI Assistant]。
solution: Experience Cloud
feature: AI Assistant, Generative AI
topic: Administration
role: Admin
level: Intermediate
exl-id: bdc51956-82aa-4aae-b627-a2018f80b5f5
source-git-commit: f1954b7137bcd492a289969e005293b6857824ec
workflow-type: tm+mt
source-wordcount: '1486'
ht-degree: 3%

---

# Experience Cloud产品中的创作AI

本页可帮助您了解哪些产品支持创作AI (GenAI)、[!DNL AI Assistant]，以及Adobe Firefly是否兼容。 您还可以找到指向有关在Experience Cloud应用程序中使用AI的各种方式的信息链接。

**关于生成AI**

创作AI是一种可以创建原始内容的AI。 例如，它可以创建文本、图像、视频、音频或软件代码来响应用户的提示或请求。

* **创建：**&#x200B;根据培训和输入提示从头开始生成内容（文本、图像、音乐或视频）的功能。 此功能是创作AI的&#x200B;_创作_&#x200B;方面。

* **生成响应：**&#x200B;人工智能提供对提示的响应或反应，通常利用其可用的数据和知识存储库。

**是什么 [!DNL AI Assistant]？**

[!DNL AI Assistant]是Experience Platform和相关应用程序中支持的对话工具。 使用它可快速获得&#x200B;_产品知识_，并且在支持的产品中几乎立即获得&#x200B;_运营分析_。

* **产品知识：**&#x200B;产品知识是指以Experience League文档为基础的概念和主题。 了解如何创建有效的[基于目标的提示](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/ai-assistant/home)，以充分利用[!DNL AI Assistant]。 来自Experience League的所有响应均可验证并带有链接引用。

* **Operational Insights：** [Operational Insights](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/ai-assistant/questions#objects-questions)指有关您的元数据对象（属性、受众、数据流、数据集等）的生成的响应。 使用[!DNL AI Assistant]，您可以在几秒钟内完成可能需要数小时或数天的任务。

[了解AI助手](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/ai-assistant/landing)

<!--## Adobe Marketing Agent for Microsoft 365 Copilot 

The Adobe Marketing Agent for Microsoft 365 Copilot is a generative AI-powered assistant designed to enhance marketing workflows by integrating Adobe's marketing capabilities directly into Microsoft 365 applications such as Word, PowerPoint, Teams, and Outlook. This collaboration between Adobe and Microsoft aims to streamline marketing processes, allowing marketers to access insights and tools within their existing work environments.
Adobe for Business

Key features and capabilities:

**Audience Refinement:** Marketers can use natural language prompts within Microsoft 365 to access data and insights from Adobe Experience Platform, enabling quick audience analysis and segmentation for personalized campaigns. 

**Insight Discovery:** The agent can retrieve meaningful insights from Adobe Customer Journey Analytics, facilitating the creation of campaign performance reports directly within Microsoft apps, thus supporting informed decision-making. 

**Content Creation:** Through integration with Adobe Express, users can generate high-quality images and assets within Microsoft 365 applications, aiding in the development of presentations, documents, and social media content. 
Adobe Newsroom

**Workflow Optimization:** The agent can automate tasks in Adobe Workfront, manage content approvals, and provide real-time alerts in Microsoft Teams based on analytics data, enhancing operational efficiency. 

**Campaign Performance Monitoring:** Users can query the agent for campaign performance metrics, which can be visualized and incorporated into PowerPoint presentations for easy sharing and analysis. 
Adobe for Business

Currently in private preview, the Adobe Marketing Agent for Microsoft 365 Copilot is expected to be generally available later in 2025. This integration represents a significant step in unifying marketing tools and data, aiming to improve productivity and collaboration for marketing teams.
 -->

## Experience Cloud产品中的GenAI可用性

了解以下Experience Cloud应用程序如何支持创作AI或[!DNL AI Assistant]。 此外，还指明了对Adobe Firefly的支持。

* [[!DNL GenStudio for Performance Marketing]](#gspm)
* [[!DNL Experience Manager]](#aem)
* [[!DNL Journey Optimizer]](#journey-optimizer)
* [[!DNL Journey Optimizer] B2B edition](#ajo-b2b)
* [[!DNL Campaign]托管云服务](#campaign-cs)
* [[!DNL Customer Journey Analytics]](#cja)
* [[!DNL Real-Time CDP]](#rtcdp)
* [[!DNL Marketo]](#marketo)
* [[!DNL Workfront]](#workfront)

## Adobe GenStudio for Performance Marketing {#gspm}

[!DNL GenStudio for Performance Marketing]是一个人工智能驱动的平台，它使您能够生成和管理符合您的品牌标准并符合企业政策的营销内容。 生成电子邮件、元广告、LinkedIn广告、展示广告和横幅的内容。

您还可以使用示例、客户角色和产品的描述以及品牌指南对您的GenStudio for Performance Marketing进行品牌培训。

[了解详情](https://experienceleague.adobe.com/zh-hans/docs/genstudio-for-performance-marketing/user-guide/home)

Adobe Firefly兼容性：**是**

## Adobe [!DNL Experience Manager] {#aem}

以下部分简要介绍AEM应用程序中的创作AI。

### Experience Manager Sites

在AEM Sites中，您可以使用&#x200B;_[!UICONTROL 生成变体]_。 此功能使用创新型人工智能根据输入提示创建内容变体。 提示由Adobe提供或由您创建和管理。

创建变体后，您可以在网站上使用该内容，并使用Edge Delivery Services中的[试验](https://www.aem.live/docs/experimentation)功能衡量其成功与否。 您还可以选择使用Adobe Express的创作AI功能在Firefly中生成图像。

**输入和输出示例**

输入字段包括：

* 要生成的变体数
* Audience Source
* 受众目标
* 其他上下文
* 客户驱动提示

输出是生成的内容或市场副本。

Adobe Firefly兼容性：**是**

[了解有关生成变体的详细信息](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/generative-ai/generate-variations-integrated-editor)

### Experience Manager Assets

[!UICONTROL Content Hub]作为[!DNL Experience Manager Assets as a Cloud Service]的一部分提供，用于使组织及其业务合作伙伴对品牌上内容的访问普及化。 它侧重于分发资产以供大规模激活，并创建品牌内内容变体以提高营销敏捷性。

在Content Hub中，您可以使用Adobe Express创建内容(如果您拥有Adobe Express权限)。 您可以使用简单的工具编辑现有内容，使用模板和品牌元素生成品牌内变体，并使用[!DNL Adobe Firefly]中的最新GenAI功能创建内容。

[了解详情](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/assets/content-hub/product-overview)

Adobe Firefly兼容性：**是**

## Adobe [!DNL Journey Optimizer] {#journey-optimizer}

在[!DNL Journey Optimizer] (AJO)中，您可以使用[AI助手](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/get-started/ai-assistant)获得&#x200B;_产品知识_&#x200B;和&#x200B;_操作分析_ （测试版）。

### 在AJO中使用AI助理的示例

以下是产品知识的输入示例：

* _一个Journey Optimizer沙盒中可以有多少实时活动？_

  输出是从Experience League和其他Adobe数据存储生成的。

以下是操作见解的输入示例：

* _在过去七天中创建了多少历程？_

  对于输出，AI Assistant查询特定于客户的数据存储。 数据存储包含有关[!UICONTROL 历程]的集中式操作数据。 此功能与客户无关，只能从业务对象中提取元数据。 它无法访问沙盒中的数据。

[了解详情](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/get-started/ai-assistant)。

Adobe Firefly兼容性：**否**

### 用于内容生成的AI助手(AJO Prime和Ultimate) {#ajo-prime}

在AJO _Prime_&#x200B;和&#x200B;_Ultimate_&#x200B;中，您可以使用[内容生成](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative)来生成内容，以便为文本和图像提供主动内容变体建议。

此功能适用于电子邮件、推送通知、网页、内容和短信渠道。 它提供基于提示的文本和图像生成。 AJO Prime和Ultimate中内容生成的输出不会受到任何影响。

[了解详情](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative)

Adobe Firefly兼容性：**是**

## [!DNL Journey Optimizer B2B Edition] {#ajo-b2b}

Journey Optimizer B2B edition使用[!DNL AI Assistant]帮助您了解产品知识。

示例输入：

* _如何在帐户历程中发送电子邮件？_

  产品知识输出是从Experience League中提取的。

[了解详情](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-b2b/user/ai-assistant/ai-assistant-overview)

Adobe Firefly兼容性：**否**

## [!DNL Campaign]托管云服务 {#campaign-cs}

Campaign Managed Cloud Services使用[!DNL AI Assistant]生成内容。 通过此功能，您可以根据营销目标自动生成个性化、引人入胜且有效的内容，其中内容针对品牌概述的样式、布局、色调等进行了优化。 您可以跨渠道（如电子邮件、短信和推送）使用它。

**注意：** Campaign Managed Cloud Services中内容生成的输出不受损害。

[了解详情](https://experienceleague.adobe.com/zh-hans/docs/campaign-web/v8/content/ai-assistant/generative-gs)

Adobe Firefly兼容性：**是**

## [!DNL Customer Journey Analytics] {#cja}

通过Customer Journey Analytics，可通过以下方式使用创作AI：

* [!DNL AI Assistant]产品知识和见解
* Workspace可视化图表中的[!UICONTROL 智能字幕]
* AI和GenAI自动分配[!DNL Content Analytics]中的每个资源元数据

**AI 助手**

从Experience League中了解产品知识和见解。 如果您是新用户，请快速了解Customer Journey Analytics概念并熟悉产品和功能。 例如：

* _如何在帐户历程中发送电子邮件？_

经验丰富的用户可获得高级用例或学习策略以快速执行任务。 您可以快速了解概念、排除问题或搜索信息。

[了解详情](https://experienceleague.adobe.com/zh-hans/docs/analytics-platform/using/cja-overview/cja-b2c-overview/ai-assistant)

**智能字幕**

您可以在[!DNL Customer Journey Analytics]中使用&#x200B;_智能字幕_&#x200B;以获得最常用Workspace可视化图表的自然语言见解。 智能字幕非常适合需要叙述和上下文以与其他用户共享的分析师。 企业用户可以利用它快速发现高级别的收获。

例如：

* **输入：**&#x200B;在CJA中，运行支持的可视化图表（包括折线图、面积图、条形图、流量图或流失图），然后单击&#x200B;**[!UICONTROL 智能字幕]**。

* **输出：**&#x200B;查看自动生成的自然语言字幕，其中显示上下文和键收藏。 然后，您可以对生成的数据执行一些操作，如查看、复制数据并与您的组织共享。 [查看方式](https://video.tv.adobe.com/v/3443148/?quality=12&learn=on#_blank&captions=chi_hans)

[了解详情](https://experienceleague.adobe.com/zh-hans/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions)

**Content Analytics**

Content Analytics使用AI和GenAI自动分配每个资源元数据，例如主题、场景、前景色等。 属性是人工智能分配的元数据标记，用于描述资源或体验中的内容。

例如：前台`color: red`是自动分配的属性。 可视化图表可帮助您识别哪些资产的属性对转化贡献最大。 [了解详情](https://experienceleague.adobe.com/zh-hans/docs/analytics-platform/using/content-analytics/report/report#template)

Adobe Firefly兼容性：**否**

## [!DNL Real-Time CDP] {#rtcdp}

Real-Time CDP使用[!DNL AI Assistant]帮助您了解Experience League的产品知识。 它还提供运营见解（测试版）。 [!DNL AI Assistant]查询特定于客户的操作分析数据存储区，其中包含在AEP沙盒中分区的集中化操作数据。 系统仅从属性、受众、数据流、数据集、目标、架构和源中提取元数据，而不访问沙盒中的数据。

例如，如果您查询受众，[!DNL AI Assistant]可以访问受众的名称和其他关联的元数据，但无法访问该受众中的配置文件。

[了解详情](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/ai-assistant/home)

Adobe Firefly兼容性：**否**

## [!DNL Marketo] {#marketo}

在Marketo中，创作AI在交互式网络研讨会和Dynamic Chat中提供。

**交互式网络研讨会**

为您的录制的网络研讨会自动生成章节和摘要，使受众更容易访问和导航这些章节和摘要。 功能包括：

* 自动生成章节
* AI生成的文本摘要
* 可编辑内容 — 修改生成的章节和摘要
* 轻松集成 — 通过将HTML代码复制到您选择的网页编辑器，将章节和摘要添加到您的登陆页面

[了解详情](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/demand-generation/events/interactive-webinars/gen-ai)

**Dynamic Chat**

利用Adobe Dynamic Chat中由AI提供支持的创新型功能，您可以优化销售代理的生产力，获得有关网站访客意图的洞察，并以安全的方式响应访客问题。 您可以预批准问题、答案和对话摘要。

[了解详情](https://experienceleague.adobe.com/zh-hans/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/overview)

Adobe Firefly兼容性：**否**

## [!DNL Workfront] {#workfront}

[!DNL Workfront]中的[!DNL AI Assistant]通过提供应用程序内信息和建议帮助您完成工作。 您可以：

* 获取某些对象的摘要，为您提供对象意图或详细信息的高级视图。
* 提出问题并让[!DNL AI Assistant]在Experience League上查找答案。
* 根据提示获取生成的公式。 您还可以解决计算字段中的无效自定义表达式中的错误。
* 查找项目、任务和问题。

[了解详情](https://experienceleague.adobe.com/zh-hans/docs/workfront/using/basics/ai-assistant/ai-assistant-overview)

Adobe Firefly兼容性：**否**

## 其他资源

* [信任中心上负责的AI资源](https://www.adobe.com/trust/responsible-ai.html)<!-- * [Customer AI Propensity Scoring Model Card](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/ai-assistant/model-cards/ai-model-cards/customer-ai) -->

**免责声明：**&#x200B;此页面上的信息仅用于一般信息目的。 我们的目标是使其保持准确和最新，但软件和AI功能可能会经常变化。 我们不保证信息的完整性和可靠性。 在根据此内容做出决策之前，请仔细检查任何重要详细信息。
