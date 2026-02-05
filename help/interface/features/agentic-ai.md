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
source-git-commit: 41fcf134da13336cb9ac26e6ea96690c8bc53b8e
workflow-type: tm+mt
source-wordcount: '935'
ht-degree: 4%

---

# Adobe Experience Cloud的人工智能

更新日期：**2026年1月29日**

Adobe Experience Platform代理由[Experience Platform Agent Orchestrator](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-ai/experience-cloud-ai/home)提供支持，以在Experience Cloud应用程序中启用代理AI功能。

这些代理可帮助自动执行任务、更快地提供见解并简化工作流。 因此，团队可以更高效地工作，并从Experience Cloud中获得更多价值。

可通过以下任一方式访问Experience Cloud中的AI代理：

* [现有Experience Cloud应用程序](#existing-apps)
* [人工智能优先的Experience Cloud应用程序](#ai-first-apps)

以下各部分将介绍这两种在Experience Cloud中启用智能人工智能的方法。

## 现有Experience Cloud应用程序 {#existing-apps}

在现有应用程序中，您可以使用自然语言通过[AI Assistant](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-ai/experience-cloud-ai/home)对话界面指示Adobe Experience Platform代理。 AI助手可在全屏视图和右边栏视图中可用。

可以在现有Experience Cloud应用程序中为客户启用代理，这些代理具有以下类别之一：

* 您购买了Adobe Experience Platform Agents AI信用许可证
* 您被包含在针对使用情况的试用中（提供的有限人工智能积分）
* 您交易了Agent Orchestrator Promo SKU（有时限的试用许可证）

使用AI代理执行&#x200B;_代理作业_&#x200B;将使用AI积分。 了解有关&#x200B;_[代理作业和AI信用消耗](/help/interface/features/ai-credit-consumption.md)_&#x200B;中的代理作业和AI信用消耗的详细信息。

AI代理遵循&#x200B;_您的_&#x200B;输入和监督，并遵守产品级别的访问控制。 您只能执行您有权在基础Experience Cloud应用程序中使用的作业或访问数据。

### 现有Experience Cloud应用程序中的AI代理 {#existing-apps-table}

下表列出了现有Experience Platform应用程序中可用的Experience Cloud代理。

| 代理名称 | 功能 | 支持的应用程序 |
|---|----------|----------|
| [Audience Agent](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-ai/experience-cloud-ai/agents/audience) | 让您的团队能够使用自然语言提示创建、管理和优化受众，以提高上市难度、效率和上市速度。 | <ul><li>Real-Time CDP（B2B、B2C和B2P版本）</li><li>Adobe Journey Optimizer（B2B和B2C版本）</li></ul> |
| **内容顾问代理** | <ul><li>[内容发现](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/ai-in-aem/agents/discovery/overview)：帮助团队使用自然语言在整个企业中快速找到最相关的内容，从而减少搜索所花费的时间，并加快决策和执行。</li><li>[内容优化](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/ai-in-aem/agents/content-optimization/overview)：使用自然语言提示简化从源资源创建可视内容变体的过程。</li></ul> | <ul><li>Adobe Experience Manager（内容发现）</li></ul><ul><li>Adobe Experience Manager与带OpenAPI的Dynamic Media（内容优化）</li></ul><ul><li>Adobe Experience Manager Cloud Services和Edge Delivery Services (Experience Production) </li></ul> |
| [Data Insights Agent](https://experienceleague.adobe.com/zh-hans/docs/analytics-platform/using/cja-overview/cja-b2c-overview/data-analysis-ai) | 快速解答有关您的数据的问题。 它使用来自数据视图的组件和您的实际数据在 Analysis Workspace 中构建相关的可视化图表。 | <ul><li>Customer Journey Analytics（B2B和B2C版本）</li></ul> |
| **品牌体验代理** | <ul><li>[体验现代化](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/ai-in-aem/agents/modernization/overview)：通过自动重新构建、丰富和验证现有站点来加快数字体验的迁移和现代化，以便团队能够以更低的风险和更少的手动操作更快地向现代、支持AI的体验迁移。</li><li>[体验生产](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/ai-in-aem/agents/production/overview)*：进行高容量体验创建和更新，从而大大减少手动工作量和周期时间，以便团队能够在不牺牲质量或一致性的情况下更快地移动。</li><li>[Forms创建](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/ai-in-aem/agents/production/form-creation)：通过自动生成、结构和验证表单体验，加快创建优化的、按品牌排列的表单，使团队能够更快地启动并只需很少的手动操作即可捕获更高质量的数据。</li><li>[开发支持](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/ai-in-aem/agents/development/overview)：通过分析根本原因并提出修复建议，帮助AEM CS开发人员和技术管理员解决Cloud Manager管道中的构建步骤失败问题。</li></ul> | <ul><li>AEM SITES CS</li></ul><ul><li>AEM Sites</li></ul><ul><li>AEM Forms</li></ul><ul><li>所有基于云的AEM应用程序</li></ul> |
| **品牌治理代理*** | <ul><li>[品牌治理](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/ai-in-aem/agents/governance/overview):Safeguard通过自动的品牌策略检查、权限和智能功能实现品牌完整性和合规性，以支持DRM和实时治理。</li><li>[Experience Production](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/ai-in-aem/agents/production/overview)：在CMS中自动执行大量工作和高容量任务。 该代理将手动冗长的流程转换为快速的AI辅助工作流，让每个体验都保持最新和一致，帮助您的企业实现目标。</li> | <ul><li>AEM Assets</li></li></ul> |
| [Journey Agent](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent-analyze) | 使您的团队能够快速创建、分析和大规模优化多点接触客户历程。 | <ul><li>Adobe Journey Optimizer（B2B和B2C版本）</li></ul> |
| [产品支持代理](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/ai-assistant/new-features/customer-support) | 无需离开工作流即可解决支持问题，创建客户支持工单并使用AI Assistant跟踪案例进度。 | <ul><li>Real-Time CDP（B2B、B2C和B2P版本）</li><li>Adobe Journey Optimizer（B2B和B2C版本）</li><li>Customer Journey Analytics（B2B和B2C版本）</li><li>Adobe Experience Manager</li></ul> |

星号(*)：客户可通过资源管理器程序访问此代理。 资源管理器程序是一个仅受邀请的程序，它提供对Adobe最新代理功能的早期访问。 有关更多信息，请联系您的客户代表。

## 人工智能优先的Experience Cloud应用程序 {#ai-first-apps}

AI优先应用是以Al为内核的生成或遗传的。 它们使用创生或代理式Al执行关键任务，并且代理功能已包含在Al-first应用程序许可证中。 因此，它们不需要Experience Platform Agent Orchestrator许可证。

下表列出了作为所有优先应用程序可用的Experience Platform代理。 通过许可这些优先应用程序来启用这些功能：

| 代理名称 | 功能 | 支持的应用程序 |
|---|----------|----------|
| [Experimentation Agent](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/content-management/content-experiment/experiment/experiment-accelerator-security) | 自动化、分析和综合洞察，以便您可以从集中工作区中快速识别高影响力的实验和发展机会 — 同时减少手动流程。 | <ul><li>AJO Experimentation Accelerator</li></ul> |
| [LLM优化代理](https://experienceleague.adobe.com/zh-hans/docs/llm-optimizer/using/home) | 增强人工智能驱动型搜索环境中的可见性、准确性和影响力，在人工智能生成的答案中提供品牌存在感洞察，提供规范性的内容推荐，并自动执行优化修复。 | <ul><li>Adobe LLM Optimizer</li></ul> |
| [Site Optimization Agent](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-sites-optimizer/content/home) | 通过自动检测和部署网站增强功能，最大限度地提高业务成效。 使用创新型人工智能和多种监控技术，您可以增加网站流量获取、参与度等 | <ul><li>AEM Sites Optimizer</li></ul> |
| [Product Advisor Agent](https://experienceleague.adobe.com/zh-hans/docs/brand-concierge/content/documentation/overview) | 通过根据个人偏好和行为量身定制的智能上下文感知产品发现，提高转化率和参与度。 | <ul><li>Adobe Brand Concierge</li></ul> |

## 有关此主题的更多帮助

* [代理作业和AI信用消耗](/help/interface/features/ai-credit-consumption.md)
* Experience Cloud中的[AI](https://experienceleague.adobe.com/zh-hans/docs/ai)文档主页
* [AEM代理概述](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-cloud-service/content/ai-in-aem/agents/overview)

[!BADGE 了解有关Adobe for Business的更多信息]{type=Informative url="https://business.adobe.com/cn/products/experience-platform/agent-orchestrator.html" tooltip="转到Business.adobe.com"}
