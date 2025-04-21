---
title: Experience Cloud 应用程序中的 AI
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
source-git-commit: 4f51bc948f3d109f8c1211fda44adee17cc05170
workflow-type: tm+mt
source-wordcount: '812'
ht-degree: 6%

---

# Experience Cloud 应用程序中的 AI

本页可帮助您了解创作AI以及如何在Experience Cloud应用程序中使用它。 了解哪些产品功能使用创作AI、AI Assistant，以及是否支持Adobe Firefly。

## 关于创作AI和AI助手

创新型人工智能是一种人工智能，其作用不仅仅是回答问题。 它&#x200B;_创建_&#x200B;内容，_对您的_&#x200B;提示&#x200B;_做出响应_（问题和语句）。

* **创建：**&#x200B;参考AI根据其训练和输入提示从头开始生成新内容（文本、图像、音乐或视频）的能力。 此功能是创作AI的&#x200B;_创作_&#x200B;方面。

* **响应：**&#x200B;指对特定问题、语句或提示提供答案或反应的AI，通常利用其知识或推理能力。

某些Experience Cloud应用程序会利用创新型人工智能，帮助新用户快速获取产品知识，并且经验丰富的用户可在几秒钟内发现运营见解，而不是数小时。

### AI 助手

[AI助手](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/landing)是Experience Platform和相关应用程序中支持的对话工具。 使用它可以加快您的工作流、改进您的产品知识、排查问题或搜索信息。 AI Assistant允许您在几秒钟内发现运营见解，而不是几小时。

所有产品知识答案都可验证，并可通过链接引用Experience League中的产品文档。 [了解AI Assistant](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/ai-assistant/home)以及基于对象的提示类型，以充分利用AI Assistant。

## 使用AI的Experience Cloud应用程序

* [Adobe GenStudio for Performance Marketing](#gspm)
* [Adobe Experience Manager Sites (Cloud Service)](#aem-sites)
* [Adobe Journey Optimizer](#journey-optimizer)
* [Adobe Journey Optimizer Prime和Ultimate](#ajo-prime-ultimate)
* [Journey Optimizer B2B 版本](#ajo-b2b)

### GenStudio for Performance Marketing {#gspm}

[GenStudio for Performance Marketing](https://experienceleague.adobe.com/zh-hans/docs/genstudio-for-performance-marketing/user-guide/home)是一个创新型人工智能驱动平台，使您能够创建、交付和优化活动资源。 其创作AI功能可转变营销内容的创建、审阅、共享和分析方式。

通过&#x200B;_GenStudio for Performance Marketing创建_（或简单地说&#x200B;_创建_）功能，营销人员和分散的团队可以创建高性能、按品牌划分的体验。 您可以为以下内容生成内容：

* 电子邮件
* 元广告
* LinkedIn广告
* 显示广告
* 横幅

您还可以使用示例、客户角色和产品的描述以及品牌指南对您的GenStudio for Performance Marketing进行品牌培训。 [了解详情...](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/overview)

**与Adobe Firefly的兼容性：**&#x200B;已计划

### Experience Manager Sites {#aem-sites}

AEM Sites使用[生成变体](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations)。 “生成变体”使用创新型人工智能根据提示创建内容变体。 这些提示由[Adobe](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#get-started)提供，或由[用户](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#create-prompt)创建和管理。

创建变体后，您可以在网站上使用内容，并使用Edge Delivery Services中的试验功能衡量其成功与否。

**输入：**&#x200B;输入字段包括：

* 要生成的变体数
* Audience Source
* 受众目标
* 其他上下文
* 客户驱动提示

**输出：**&#x200B;生成的内容/市场副本。 您还可以选择使用Adobe Express的创作AI功能在Firefly中生成图像。

请参阅[生成图像](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#generate-image)。

**与Adobe Firefly的兼容性：**&#x200B;是

## Journey Optimizer {#journey-optimizer}

Journey Optimizer使用[AI助手](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/ai-assistant/home)来回答两类问题：

**产品知识** — 查询Adobe数据存储区(如Experience League产品文档)以了解产品insight。 此输出不受客户限制。 示例：

* 一个Adobe Journey Optimizer沙盒中可以有多少个实时活动？

**Operational Insights (Beta)** — 查询特定于客户的操作分析数据存储区，该数据存储区包含有关历程的集中操作数据，并按客户的沙盒进行分区。 仅从业务对象中提取元数据，而不访问沙盒中的数据。

* 过去七天创建了多少历程？

运营见解输出取决于从客户的业务对象中拉取的元数据。

历程是Journey Optimizer中唯一可用于AI助手的对象，并且元数据是从当前沙盒中提取的。

查看[使用AI助手](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant)和[字段准备工作](https://fieldreadiness-adobe.highspot.com/items/6661f1c132683fd5e6a8adf4?lfrm=srp.1#11)以了解更多信息。

**与Adobe Firefly的兼容性：**&#x200B;否

## Journey Optimizer Prime和Ultimate {#ajo-prime-ultimate}

Journey Optimizer Prime和Ultimate使用[AI Assistant for Content Accelerator](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative)为文本和图像提供主动内容变体建议。

此功能适用于电子邮件、推送、Web和短信渠道。 它提供基于提示的文本和图像生成。

**电子邮件** — 生成完整电子邮件、纯文本或纯图像。 [了解详情...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-email)

**推送通知** — 生成完整的推送通知、纯文本或纯图像。 [了解详情...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-push)

**短信** — 生成完整的短信或仅发送文本。 [了解详情](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-sms)

**网页** — 生成网页图像或网页文本。 [了解详情...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-web)

**内容** — 为各种消息传递活动生成内容。 [了解详情...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-experimentation)

**注意：** AJO Prime和Ultimate中内容加速器的输出不受损害。

**与Adobe Firefly的兼容性：**&#x200B;是

## Journey Optimizer B2B 版本 {#ajo-b2b}

使用[AI助手](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/ai-assistant)进行产品知识提示。

**产品知识** — 查询Adobe数据存储区(如Experience League产品文档)以了解产品insight。 此输出不受客户限制。 | <ul><li>**输入：**&#x200B;如何在帐户历程中发送电子邮件？</li><li>**输出：**&#x200B;产品知识从Experience League提取（公共文档）。 [了解详情...](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/ai-assistant)</li></ul>   | 否   |

<!-- ## Experience Cloud applications that use AI

Learn how Experience Cloud applications use generative AI or AI Assistant, and whether Adobe Firefly is supported. 

| Application | How Generative AI Is Used | Examples | Adobe Firefly? |
|----------|------------|-----------|----------------|
| GenStudio for Performance Marketing | [GenStudio for Performance Marketing](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/home) is a generative AI-driven platform. It infuses the content creation lifecycle with generative AI capabilities that transform how marketing content is created, reviewed, shared, and analyzed.<br>You can train GenStudio for Performance Marketing on your brand using examples, descriptions of customer personas and products, and brand guidelines. |_GenStudio for Performance Marketing Create_ lets you generate content for emails, Meta ads, LinkedIn ads, display ads, and banners. <br>**Inputs:** <ul><li>Use templates to start the content creation process. </li><li>Add parameters like Brands, Products, and Personas (guidelines) and Content (assets) to shape the generated experience. </li><li>Enter descriptive prompts that describe the context or experience you intend to generate. [Learn more...](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/overview)</li></ul> |Yes |
|Adobe Experience Manager Sites (Cloud Service)  | AEM Sites uses [Generate Variations](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations). <br>Generate Variations uses generative AI to create content variations based on prompts. These prompts are either provided by Adobe or created and managed by users. |After creating variations, you can use the content on your website and measure its success using the Experimentation functionality of Edge Delivery Services. <br>**Input:** Input fields include Number of Variations to generate; Audience Source / Audience Target; Additional Context, and customer-driven prompts. <ul><li>[Adobe prompt template](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#get-started) </li><li>[User generated prompt](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#create-prompt)</li></ul> **Output:** Generated Content / Market Copy. You also have the option to generate images in Adobe Express using the generative AI capabilities of Firefly. See [Generate Image](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#generate-image). | Yes|
| Adobe Journey Optimizer |Journey Optimizer uses [AI Assistant](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home) with two classes of questions:<ul><li>**Product knowledge** - Queries Adobe data stores (such as Experience League product documentation) for product insight. This output is customer agnostic. </li><li>**Operational Insights (Beta)** - queries a customer-specific operational insights data store that contains centralized operational data about Journeys, partitioned by the customer's sandbox. Pulls metadata only from business objects and does not access data within the sandbox.</li></ul>|<ul><li>**Product Knowledge Input:** How many live activities can I have in one Adobe Journey Optimizer sandbox?</li><li>**Product Knowledge Output:** Product Knowledge pulls from Experience League (public documentation). </li><li>**Operational Insights Input:** How many Journeys have been created in the last seven days? </li><li>**Operational Insights Output:** Operational Insights output depends on metadata pulled from customer's business objects. Journeys is the only object available in AJO, and metadata is pulled from the current sandbox. </li></ul> See [Work with the AI Assistant](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant) and [Field Readiness](https://fieldreadiness-adobe.highspot.com/items/6661f1c132683fd5e6a8adf4?lfrm=srp.1#11) | No |
| Journey Optimizer: _Prime_ and _Ultimate_  | [AI Assistant for Content Accelerator](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative) brings proactive content variation suggestions for text and images. It is available for email, push, web and SMS channels. This new capability provides prompt-based text and image generation. |<ul><li> **Email** - generate a full email, text only or image only. [Learn more...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-email) </li><li> **Push Notification** - Generate a full push notification, text only or image only. [Learn more...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-push) </li><li> **SMS** - Generate a full SMS, or text only. [Learn more](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-sms) </li><li> **Webpage** - Generate web page images or web page text. [Learn more...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-web) </li><li> **Content** - Generate content for various messaging campaigns. [Learn more...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-experimentation)</li></ul> **Note:** Output from Content Accelerator in AJO Prime and Ultimate is indemnified. | Yes   |
| Journey Optimizer B2B Edition  | Uses [AI Assistant](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/ai-assistant) with one class of questions: <br> **Product knowledge** - Queries Adobe data stores (such as Experience League product documentation) for product insight. This output is customer agnostic. | <ul><li>**Input:** How do I send an email in an account journey?</li><li>**Output:** Product Knowledge pulls from Experience League (public documentation). [Learn more...](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/ai-assistant)</li></ul>   | No   |
| Campaign Managed Cloud Services | [AI Assistant for Content Accelerator](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-gs) auto-generates personalized, engaging, and effective content based on the marketing objective with content optimized for brand outlined styles, layouts, tone, and more across channels like Email, SMS, Push. |<ul><li> **Email** - Generate a full email, text only or image only. [Learn more](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-content) </li><li> **SMS** - Generate full SMS or text only. [Learn more...](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-sms) </li><li> **Push** - Craft compelling messaging and generate content. [Learn more...](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-push) </li></ul> **Note:** Output from Content Accelerator in Campaign Managed Cloud Services is indemnified. | Yes  |
| Customer Journey Analytics   | CJA uses [AI Assistant](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/ai-assistant) to help you discover product knowledge and insights from Experience League. <br>For example, new users can use it to learn Customer Journey Analytics concepts and onboard yourself to products and features that you are unfamiliar with. <br>Experienced users can use AI Assistant to present more advanced use cases or tips and tricks and perform tasks at a fast pace. Understand concepts, troubleshoot problems, or search for information. [Learn more...](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/ai-assistant#knowledge) | <ul><li>**Product Knowledge Input:** How do I build a calculated metric? </li><li> **Product Knowledge Output:** Product Knowledge pulls from Experience League (public documentation). </li></ul> | No |
| Customer Journey Analytics    | [Intelligent Captions](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions) provides natural-language insights for line visualizations in Workspace visualizations.| <ul><li>**Input:** Line visualizations. Captions are auto-generated based on such line visualizations when you click **Intelligent captions**. </li><li> **Output:** Auto-generated natural-language captions.</li></ul>  | No             |
| Real-Time CDP |Uses [AI Assistant](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home) to help you discover product knowledge and insights from Experience League. It queries a database and translates data from the database into a human-readable answer. Two classes of questions: <br> **Product knowledge** - Queries Adobe data stores (such as Experience League product documentation) for product insight. This output is customer agnostic. <br> **Operational Insights (Beta)** - Queries a customer-specific operational insights data store that contains centralized operational data, partitioned by the customer's AEP sandbox. Pulls metadata only from Attributes, Audiences, Dataflows, Datasets, Destinations, Schemas, and Sources, and does not access data within the sandbox. <br>For example, for a query about an audience [!DNL AI Assistant] can access the name of the audience and other associated metadata but cannot access the profiles within that audience. | <ul><li>**Product Knowledge Input:** How is profile richness calculated? </li><li>**Product Knowledge Output:** Product Knowledge pulls from Experience League (public documentation). </li><li> **Operational Insights Input:** How many datasets do I have? </li><li> **Operational Insights Output:** Operational Insights output depends on metadata pulled from Customer's business objects (Attributes, Audiences, Dataflows, Datasets, Destinations, Schemas, and Sources), and includes a link to specific UI page containing queried data. </li></ul>For examples, see the _Product Knowledge_ and _Operational Insights_ input tables in [AI Assistant in Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home)  | No |
| Marketo  | [Dynamic Chat](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/dynamic-chat-overview) creates AI-assisted conversations with customized and pre-approved questions and answers, as well as conversation summary |<ul><li> **Generate Questions:** Provide URLs from which content is extracted and used to generate questions / responses. </li><li> **Conversation Summary:** Generates a summary of a chat conversation. </li></ul> [Learn more...](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/response-library)  | No |
| Workfront | [AI Assistant](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview) in Workfront helps you accomplish your work by offering in-app information and suggestions in a natural-language conversation. AI Assistant offers the following functionality: Summarizes projects/tasks/issues/documents, provides instructions or reference information pulled from the Workfront documentation on Experience League, generates or refines formulas for calculated custom fields.  | <ul><li>**Summarize Project Input:** Summarize this project </li><li> **Summarize Project Output:** Returns brief descriptions of the project's purpose and status, gives examples of tasks that are completed and that are still pending, and provides some additional details and notes.</li><li> **Generate/Refine Formula Input:** "Rewrite this formula to remove the invalid expression error." </li><li> **Generate/Refine Formula Output:** Generated or refined formula. </li></ul>**Note:** AI Assistant may take a few moments to generate the revised formula, depending on the size and complexity of the formula. | No  | -->
