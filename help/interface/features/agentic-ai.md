---
title: Experience Cloud应用程序中的智能代理
description: 了解在CX Enterprise应用程序中可以使用代理人工智能的位置。
solution: Experience Cloud
landing-page-name: ai
landing-page-breadcrumb-title: AI Documentation
topic: Artificial Intelligence
feature: Agentic AI, AI Tools
role: Admin, User
level: Intermediate
exl-id: c1a8f9a7-4752-4040-b5f0-dc775417f536
source-git-commit: 50012e2564e88e1a6e16578e3331136c7df0cb21
workflow-type: tm+mt
source-wordcount: '1131'
ht-degree: 10%

---

# Adobe CX Enterprise中的代理AI

更新日期： 2026年4月6日&#x200B;**&#x200B;**

Adobe Experience Platform代理由[Experience Platform Agent Orchestrator](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-ai/experience-cloud-ai/home)提供支持，以在CX Enterprise应用程序中启用代理AI功能。

这些代理可帮助自动执行任务、更快地提供见解并简化工作流。 因此，团队可以更高效地工作，从CX Enterprise中获得更多价值。

可通过以下任一方式访问CX Enterprise中的AI代理：

* [现有CX Enterprise应用程序](#existing-apps)
* [AI优先的CX企业应用程序](#ai-first-apps)

以下各节将介绍这两种在CX Enterprise中启用代理人工智能的方法。

## 现有CX Enterprise应用程序 {#existing-apps}

在现有应用程序中，您可以使用自然语言通过[AI Assistant](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-ai/experience-cloud-ai/home)对话界面指示Adobe Experience Platform代理。 AI助手可在全屏视图和右边栏视图中可用。

可以在现有CX Enterprise应用程序中为具有以下类别之一的客户启用代理：

* 您购买了Adobe Experience Platform Agents AI信用许可证
* 您被包含在针对使用情况的试用中（提供的有限人工智能积分）
* 您交易了Agent Orchestrator Promo SKU（有时限的试用许可证）

使用AI代理执行&#x200B;_代理作业_&#x200B;将使用AI积分。 了解有关&#x200B;_[代理作业和AI信用消耗](/help/interface/features/ai-credit-consumption.md)_&#x200B;中的代理作业和AI信用消耗的详细信息。

AI代理遵循&#x200B;_您的_&#x200B;输入和监督，并遵守产品级别的访问控制。 您只能执行您有权在底层CX Enterprise应用程序中使用的作业或访问数据。

### 现有CX Enterprise应用程序中的AI代理 {#existing-apps-table}

下表列出了现有CX Enterprise应用程序中可用的Experience Platform Agent。

| 代理名称 | 功能 | 支持的应用程序 |
|---|----------|----------|
| [Audience Agent](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-ai/experience-cloud-ai/agents/audience) | 让您的团队能够使用自然语言提示创建、管理和优化受众，以提高上市难度、效率和上市速度。 | <ul><li>Real-Time CDP（B2B、B2C和B2P版本）</li><li>Adobe Journey Optimizer（B2B和B2C版本）</li></ul> |
| [内容顾问代理](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/content-advisor/overview) | <ul><li>帮助团队使用自然语言在整个企业中快速找到最相关的内容，从而减少搜索所花费的时间，并加快决策和执行速度。</li><li>使用自然语言提示简化从源资源创建可视内容变体的过程。</li></ul> | <ul><li>Adobe Experience Manager Assets</li></ul><ul><li>Dynamic Media（云服务）</li></ul> |
| [Data Insights Agent](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/data-analysis-ai) | 快速解答有关您的数据的问题。 它使用来自数据视图的组件和您的实际数据在 Analysis Workspace 中构建相关的可视化图表。 | <ul><li>Customer Journey Analytics（B2B和B2C版本）</li></ul> |
| [Brand Experience Agent](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/brand-experience/overview) | <ul><li>通过自动重新构建、丰富和验证现有站点，加快数字体验的迁移和现代化，以便团队能够以更低的风险和手动操作更快地向现代、人工智能就绪的体验迁移。</li><li>进行高容量体验创建和更新，显着减少手动工作量和周期时间，使团队能够在不牺牲质量或一致性的情况下更快地移动。</li><li>通过自动生成、结构和验证表单体验，加快创建优化的品牌内表单，使团队能够更快地启动并只需很少的手动操作即可捕获更高质量的数据。</li><li>通过分析根本原因并提出修复建议，帮助AEM CS开发人员和技术管理员解决Cloud Manager管道中的构建步骤失败问题。</li></ul> | <ul><li>Adobe Experience Manager Sites云服务(Experience Modernization)</li></ul><ul><li>Adobe Experience Manager Sites (Experience Production)</li></ul><ul><li>Adobe Experience Manager Forms（表单创建）</li></ul><ul><li>所有基于云的Adobe Experience Manager应用程序（开发支持）</li></ul> |
| [品牌治理代理](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/governance/overview) | 通过自动化的品牌策略检查、权限和智能功能来确保品牌完整性和合规性，从而通过实时治理支持DRM。 | <ul><li>Adobe Experience Manager Assets</li><li>Adobe Experience Manager Sites（品牌策略）</li></ul> |
| [Journey Agent](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent) | 使您的团队能够快速创建、分析和大规模优化多点接触客户历程。 | <ul><li>Adobe Journey Optimizer（B2B和B2C版本）</li></ul> |
| [产品支持代理](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/product-support) | 无需离开工作流即可解决支持问题，创建客户支持工单并使用AI Assistant跟踪案例进度。 | <ul><li>Real-Time CDP（B2B、B2C和B2P版本）</li><li>Adobe Journey Optimizer（B2B和B2C版本）</li><li>Customer Journey Analytics（B2B和B2C版本）</li><li>Adobe Experience Manager</li></ul> |
| [Adobe Marketing Agent for Microsoft 365 Copilot](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-ai/experience-cloud-ai/agents/ama-ms) | 将Experience Platform直接连接到Microsoft 365 Copilot。 您可以在Microsoft 365应用程序（如Teams、Word、Powerpoint和Excel）中询问自然语言问题，以便立即从Experience Platform中检索营销洞察，而不会中断您的工作流程。 | <ul><li> Adobe Agent Orchestrator，可支持Audience Agent、Journey Agent、Customer Journey Analytics数据分析、Experience Platform运营分析</li></ul> |

## AI优先的CX企业应用程序 {#ai-first-apps}

AI优先应用是以Al为内核的生成或遗传的。 它们使用创生或代理式Al执行关键任务，并且代理功能已包含在Al-first应用程序许可证中。 因此，它们不需要Experience Platform Agent Orchestrator许可证。

下表列出了作为所有优先应用程序可用的Experience Platform代理。 通过许可这些优先应用程序来启用这些功能：

| 代理名称 | 功能 | 支持的应用程序 |
|---|----------|----------|
| [Experimentation Agent](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-experiment/experiment/experiment-accelerator-security) | 自动化、分析和综合洞察，以便您可以从集中工作区中快速识别高影响力的实验和发展机会 — 同时减少手动流程。 | <ul><li>AJO Experimentation Accelerator</li></ul> |
| [LLM优化代理](https://experienceleague.adobe.com/zh-hans/docs/llm-optimizer/using/home) | 增强人工智能驱动型搜索环境中的可见性、准确性和影响力，在人工智能生成的答案中提供品牌存在感洞察，提供规范性的内容推荐，并自动执行优化修复。 | <ul><li>Adobe LLM Optimizer</li></ul> |
| [Site Optimization Agent](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-sites-optimizer/content/home) | 通过自动检测和部署网站增强功能，最大限度地提高业务成效。 使用创新型人工智能和多种监控技术，您可以增加网站流量获取、参与度等 | <ul><li>AEM Sites Optimizer</li></ul> |
| [Product Advisor Agent](https://experienceleague.adobe.com/en/docs/brand-concierge/content/documentation/overview) | 通过根据个人偏好和行为量身定制的智能上下文感知产品发现，提高转化率和参与度。 | <ul><li>Adobe Brand Concierge</li></ul> |

## 有关此主题的更多帮助

* [代理作业和AI信用消耗](/help/interface/features/ai-credit-consumption.md)
* CX Enterprise中的[AI](https://experienceleague.adobe.com/zh-hans/docs/ai)文档主页
* [AEM中的代理概述](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/overview)

[!BADGE 了解有关Adobe for Business的更多信息]{type=Informative url="https://business.adobe.com/products/experience-platform/agent-orchestrator.html" tooltip="转到Business.adobe.com"}
