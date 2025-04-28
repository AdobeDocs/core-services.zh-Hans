---
title: Experience Cloud 应用程序中的 AI
description: 了解创作AI以及Experience Cloud应用程序如何使用genAI和 [!DNL AI Assistant]。
solution: Experience Cloud
feature: AI Assistant, Generative AI
topic: Administration
role: Admin
level: Intermediate
exl-id: bdc51956-82aa-4aae-b627-a2018f80b5f5
source-git-commit: cadc0d7eaaa9acb868f96561c2a562d9d29fc9ac
workflow-type: tm+mt
source-wordcount: '1244'
ht-degree: 3%

---

# Experience Cloud产品中的AI

本页可帮助您了解哪些产品支持创作AI [!DNL AI Assistant]，以及Adobe Firefly是否兼容。 您还可以找到指向产品特定帮助资源的链接，这些帮助资源介绍了如何在Experience Cloud中使用AI。

**关于生成AI**

创新型人工智能是一种人工智能，其作用不仅仅是回答问题。 它可以&#x200B;_创建_&#x200B;内容并&#x200B;_生成对您的问题或语句（称为_&#x200B;提示&#x200B;_）的响应_。

* **创建：**&#x200B;根据培训和输入提示从头开始生成内容（文本、图像、音乐或视频）的功能。 此功能是创作AI的&#x200B;_创作_&#x200B;方面。

* **生成响应：**&#x200B;人工智能提供对提示的响应或反应，通常利用其可用的数据和知识存储库。

**是什么 [!DNL AI Assistant]？**

[!DNL AI Assistant]是Experience Platform和相关应用程序中支持的对话工具。 使用它可快速获得&#x200B;_产品知识_，并且在支持的应用程序中几乎立即获得&#x200B;_运营见解_。

* **产品知识：**&#x200B;产品知识是指以Experience League文档为基础的概念和主题。 来自Experience League的响应是可验证的，并通过链接引用。 了解[基于目标的提示](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/ai-assistant/home)的类型，以充分利用[!DNL AI Assistant]。

* **Operational Insights：** Operational Insights是指Answers AI Assistant生成的有关元数据对象（属性、受众、数据流、数据集、目标、旅程、架构和源）的信息，包括计数、查找和谱系影响。 使用AI助手，您可以在几秒钟内而不是几小时内发现运营见解。

[了解详情](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/landing)

**您的数据仍属于您**

在AI Assistant中，安全是优先事项：

* 客户数据不用于培训语言模型。
* AI助手仅查看您指示的文档。 一切由您掌控。
* 您的人员只能在他们能够访问的文档上使用AI助手。
* 它可随时进行审核：响应可归因于源文档。
* 企业控制可管理谁在公司中拥有人工智能访问权限。

## Experience Cloud产品中的AI可用性

了解在Experience Cloud产品中支持创作AI或[!DNL AI Assistant]。 此外，还指明了对Adobe Firefly的支持。

* [[!DNL GenStudio for Performance Marketing]](#gspm)
* [[!DNL Experience Manager Sites]](#aem-sites)
* [[!DNL Journey Optimizer]](#journey-optimizer)
* [[!DNL Journey Optimizer] B2B edition](#ajo-b2b)
* [[!DNL Campaign] Managed Services (Campaign v8 Web)](#campaign-cs)
* [[!DNL Customer Journey Analytics]](#cja)
* [[!DNL Customer Journey Analytics]](#cja-captions)
* [[!DNL Real-Time CDP]](#rtcdp)
* [[!DNL Marketo]](#marketo)
* [[!DNL Workfront]](#workfront)

## Adobe GenStudio for Performance Marketing {#gspm}

[!DNL GenStudio for Performance Marketing]是一个人工智能驱动的平台，它使您能够生成和管理符合您的品牌标准并符合企业政策的营销内容。 生成电子邮件、元广告、LinkedIn广告、展示广告和横幅的内容。

您还可以使用示例、客户角色和产品的描述以及品牌指南对您的GenStudio for Performance Marketing进行品牌培训。

[了解详情](https://experienceleague.adobe.com/zh-hans/docs/genstudio-for-performance-marketing/user-guide/home)

与Adobe Firefly的兼容性： **是**

## Adobe [!DNL Experience Manager Sites] {#aem-sites}

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

[了解有关生成变体的详细信息](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations-integrated-editor)

与Adobe Firefly的兼容性： **是**

## Adobe [!DNL Journey Optimizer] {#journey-optimizer}

在[!DNL Journey Optimizer] (AJO)中，您可以使用[AI助手](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant)获得&#x200B;_产品知识_&#x200B;和&#x200B;_操作分析_ （测试版）。

### 在AJO中使用AI助理的示例

以下是产品知识的输入示例：

* _一个Journey Optimizer沙盒中可以有多少实时活动？_

  输出是从Experience League和其他Adobe数据存储生成的。

以下是操作见解的输入示例：

* _在过去七天中创建了多少历程？_

  对于输出，AI Assistant查询特定于客户的数据存储。 数据存储包含有关[!UICONTROL 历程]的集中式操作数据。 此功能与客户无关，只能从业务对象中提取元数据。 它无法访问沙盒中的数据。

[了解详情](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant)。

与Adobe Firefly的兼容性：**否**

### 用于内容生成的AI助手(AJO Prime和Ultimate) {#ajo-prime}

在AJO _Prime_&#x200B;和&#x200B;_Ultimate_&#x200B;中，您可以使用[内容生成](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative)来生成内容，以便为文本和图像提供主动内容变体建议。

此功能适用于电子邮件、推送通知、网页、内容和短信渠道。 它提供基于提示的文本和图像生成。 AJO Prime和Ultimate中内容生成的输出不会受到任何影响。

[了解详情](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative)

与Adobe Firefly的兼容性： **是**

## [!DNL Journey Optimizer B2B Edition] {#ajo-b2b}

Journey Optimizer B2B edition使用[!DNL AI Assistant]帮助您了解产品知识。

示例输入：

* _如何在帐户历程中发送电子邮件？_

  产品知识输出是从Experience League中提取的。

[了解详情](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/ai-assistant/ai-assistant-overview)

与Adobe Firefly的兼容性：**否**

## [!DNL Campaign] Managed Services (Campaign v8 Web) {#campaign-cs}

Campaign v8 (Campaign Managed Cloud Services)使用[!DNL AI Assistant]生成内容。 通过此功能，您可以根据营销目标自动生成个性化、引人入胜且有效的内容，其中内容针对品牌概述的样式、布局、色调等进行了优化。 您可以跨渠道（如电子邮件、短信和推送）使用它。

**注意：** Campaign Managed Cloud Services中内容生成的输出不受损害。

[了解详情](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-gs)

与Adobe Firefly的兼容性： **是**

## [!DNL Customer Journey Analytics] {#cja}

Customer Journey Analytics使用[!DNL AI Assistant]来帮助您从Experience League中发现产品知识和见解。

如果您是新用户，请快速了解Customer Journey Analytics概念并熟悉产品和功能。 例如：

* _如何在帐户历程中发送电子邮件？_

经验丰富的用户可获得高级用例或学习策略以快速执行任务。 您可以快速了解概念、排除问题或搜索信息。

[了解详情](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/ai-assistant)

与Adobe Firefly的兼容性：**否**

## [!DNL Customer Journey Analytics] {#cja-captions}

您可以在[!DNL Customer Journey Analytics]中使用&#x200B;_智能字幕_&#x200B;以获得最常用Workspace可视化图表的自然语言见解。 智能字幕非常适合需要叙述和上下文以与其他用户共享的分析师。 企业用户可以利用它快速发现高级别的收获。

例如：

* **输入：**&#x200B;在CJA中，运行支持的可视化图表（包括折线图、面积图、条形图、流量图或流失图），然后单击&#x200B;**[!UICONTROL 智能字幕]**。

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
