---
title: Experience Cloud应用程序中的智能代理
description: 了解在Experience Cloud应用程序中何处可以使用代理AI。
solution: Experience Cloud
landing-page-name: ai
landing-page-breadcrumb-title: AI Documentation
topic: Artificial Intelligence
feature: Agentic AI, AI Tools
role: Admin, User
level: Intermediate
exl-id: c1a8f9a7-4752-4040-b5f0-dc775417f536
source-git-commit: 7f0563f5b44d4abb06bc042553d624ec16fbcdc4
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 5%

---

# Experience Cloud中的Experience Platform代理

更新日期：**2025年11月17日**

Adobe [!DNL Experience Platform] [Agent Orchestrator](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-ai/experience-cloud-ai/home)和Adobe Experience Platform代理在Experience Cloud应用程序中启用代理功能。

您可以通过以下任一方式访问这些代理功能：

* [现有 [!DNL Experience Cloud] 应用程序](#existing-apps)：这些应用程序可以自行工作，但启用Experience Platform Agent Orchestrator和代理程序可以提高现有作业和在这些应用程序中执行的工作流的效率，并增加利用这些作业的团队的工作效率。 要在您当前已获得许可的Experience Cloud应用程序中启用这些代理功能，您还必须购买Agent Orchestrator许可证。

* [AI-First [!DNL Experience Cloud] 应用程序](#ai-first-apps)：这些应用程序是以生成型或代理型AI为核心构建的。 它们使用生成性或代理式AI执行关键任务，并且代理功能已包含在AI第一个应用程序许可证中，不需要Agent Orchestrator许可证。

## 现有[!DNL Experience Cloud]应用程序

以下是现有Experience Platform应用程序中可用的、通过许可Agent Orchestrator来启用的Experience Cloud代理列表：

| 代理名称 | 可用性 | 功能 | 支持的应用程序 |
|---|----------|----------|----------|
| [Audience Agent](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-ai/experience-cloud-ai/agents/audience) | 可用 | 让您的团队能够使用自然语言提示创建、管理和优化受众，以提高上市难度、效率和上市速度。 | <ul><li>Real-Time CDP（B2B和B2C添加）</li><li>Adobe Journey Optimizer（B2B和B2C添加）</li></ul> |
| [Data Insights Agent](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/data-analysis-ai) | 可用 | 快速解答有关您的数据的数据问题。 它使用数据视图中的组件并使用实际数据在Analysis Workspace中构建相关可视化图表。 | <ul><li>Customer Journey Analytics</li></ul> |
| [Journey Agent](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent-analyze) | 可用 | 使您的团队能够快速创建、分析和大规模优化多点接触客户历程。 | <ul><li>Adobe Journey Optimizer（B2B和B2C添加）</li></ul> |
| [产品支持代理](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/new-features/customer-support) | 可用 | 无需离开工作流即可解决支持问题，创建客户支持工单并使用AI Assistant跟踪案例进度。 | <ul><li>Real-Time CDP（B2B和B2C添加）</li><li>Adobe Journey Optimizer（B2B和B2C添加）</li><li>Adobe Journey Optimizer B2B edition</li><li>Customer Journey Analytics</li><li>Adobe Experience Manager</li></ul> |

<!-- Product Advisor Agent: Troubleshoot issues, create support tickets, and track progress with AI Assistant. 

<ul><li>Adobe Experience Platform</li><li>Real-Time CDP (B2B and B2C additions)</li><li>Adobe Journey Optimizer (B2B and B2C additions)</li><li>Adobe Journey Optimizer B2B Edition</li><li>Customer Journey Analytics</li><li>Adobe Experience Manager</li></ul> 

Site Advisory Agent: Troubleshoot issues, create support tickets, and track progress with AI Assistant. 

<ul><li>Adobe Experience Platform</li><li>Real-Time CDP (B2B and B2C additions)</li><li>Adobe Journey Optimizer (B2B and B2C additions)</li><li>Adobe Journey Optimizer B2B Edition</li><li>Customer Journey Analytics</li><li>Adobe Experience Manager</li></ul>  -->

<!-- Draft AEM or upcoming agents: release 11/20

Production Agent
Discovery Agent
Development Agent
-->

## 人工智能优先Experience Cloud应用程序

以下是AI-First应用程序中可用的、通过许可这些AI-fFirst应用程序启用的Experience Platform代理列表：

| 代理名称 | 可用性 | 功能 | 支持的应用程序 |
|---|----------|----------|----------|
| [试验代理](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-experiment/experiment/experiment-accelerator-security) | 可用 | 自动化、分析和综合洞察，以便您可以从集中工作区中快速识别高影响力的实验和发展机会 — 同时减少手动流程。 | <ul><li>AJO Experimentation Accelerator</li></ul> |
| [LLM优化代理](https://experienceleague.adobe.com/zh-hans/docs/llm-optimizer/using/home) | 可用 | 增强AI驱动搜索环境中的可见性、准确性和影响力，在AI生成的答案中提供对品牌存在的洞察，提供规范性内容建议，并自动化优化修复。 | <ul><li>Adobe LLM Optimizer</li></ul> |
| [Site Optimization Agent](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-sites-optimizer/content/home) | 可用 | 通过自动检测和部署网站增强功能，最大限度地提高业务成效。 使用创新型人工智能和多种监控技术，您可以增加网站流量获取、参与度等 | <ul><li>AEM Sites Optimizer</li></ul> |

<!-- | Agent name  | Availability | Capabilities | Supported applications   |
|---|----------|----------|----------|
| **Content Optimization Agent** | November 21, 2025 | Simplify creating visual content variants from source assets using natural language prompts.|  <ul><li>Adobe Experience Manager (with [Dynamic Media with OpenAPI](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/dynamicmedia/dynamic-media-open-apis/dynamic-media-open-apis-overview))</li></ul>  |
| **Development Agent** | November 21, 2025 | Helps AEM CS developers and technical administrators troubleshoot build-step failures in the Cloud Manager pipeline by analyzing the root cause and suggesting fixes.|  <ul><li>AI Assistant in AEM Cloud Service and Adobe Managed Services</li></ul>  |
| **Discovery Agent** | November 21, 2025 | Speed authoring and boost discovery with simplified natural-language prompts to instantly find and surface Experience Manager content across images, videos, text-based documents, content fragments, and forms.|  <ul><li>Adobe Experience Manager Cloud Services</li></ul>  |
| **Experience Production Agent** | November 21, 2025 | Automates high-effort and high-volume tasks in the CMS. This agent turns manual, lengthy processes into fast, AI-assisted workflows that keep every experience current and consistent, helping your business achieve your goals.|  <ul><li>Adobe Experience Manager Cloud Services and Edge Delivery Services</li></ul>  |
| [Experimentation Agent](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-experiment/experiment/experiment-accelerator-security) | Available | Automate, analyze, and synthesize insights, so you can quickly identify high-impact experiments and growth opportunities from a centralized workspace — all while reducing manual processes.  | <ul><li>AJO Experimentation Accelerator</li></ul>   |
| **Governance Agent** | November 21, 2025 | Safeguard brand integrity and compliance by enforcing security, regulatory, and brand policies across Experience Manager. This agent applies brand governance to maintain visual and messaging standards. It uses granular permissions to manage access and content changes, and incorporates DRM to uphold licensing and usage constraints. |  <ul><li>Adobe Experience Manager Sites</li><li>Adobe Experience Manager Assets</li><li>Adobe Experience Manager Forms </li></ul>  |
| [LLM Optimization Agent](https://experienceleague.adobe.com/en/docs/llm-optimizer/using/home) | Available | Enhance visibility, accuracy, and influence in AI-driven search environments, provide insights into brand presence in AI-generated answers, offer prescriptive content recommendations, and automate optimization fixes. | <ul><li>Adobe LLM Optimizer</li></ul>   |
| [Site Optimization Agent](https://experienceleague.adobe.com/en/docs/experience-manager-sites-optimizer/content/home) | Available | Maximize business impact by automatically detecting and deploying website enhancements. Using generative AI and multiple monitoring technologies, you can increase site traffic acquisition, engagement, and more | <ul><li>AEM Sites Optimizer</li></ul> | -->

## 有关此主题的更多帮助

* Experience Cloud中的[AI](https://experienceleague.adobe.com/zh-hans/docs/ai)文档主页

[!BADGE 了解有关Adobe for Business的更多信息]{type=Informative url="https://business.adobe.com/products/experience-platform/agent-orchestrator.html" tooltip="转到Business.adobe.com"}








