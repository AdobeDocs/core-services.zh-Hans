---
title: 代理作业和AI信用消耗
description: 了解Experience Cloud应用程序中的代理作业和AI信用消耗。
solution: Experience Cloud
landing-page-name: ai
landing-page-breadcrumb-title: AI Documentation
topic: Artificial Intelligence
feature: Agentic AI, AI Tools
role: Admin, User
level: Intermediate
source-git-commit: 6be65dde7c10f5f51786c0ce01e3ec82379c775f
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 9%

---


## 代理作业和AI信用消耗

### 代理作业

**代理作业**&#x200B;是代理执行的一系列任务和操作，以实现客户输入所指示的特定结果。

客户可以通过人工智能助手使用自然语言提示，要求代理执行特定的作业。 根据这些输入，Agent Orchestrator协调相应的代理，以在相关的Experience Cloud应用程序中执行每个步骤。

### AI积分

**AI信用**&#x200B;是一个基于使用情况的量度，它量化了代理作业的执行情况。 AI积分不适用于AI优先的应用程序。

### AI信用使用

根据所执行作业的复杂性和价值，AI信用使用可能有所不同：

* 简单（通常是单步）任务占用的积分较少
* 复杂（通常为多步）任务会消耗更多积分
* 涉及高级推理、验证、多代理协调或集成的任务消耗更多积分

#### 估计的AI信用消耗率

| 代理 | 作业 | 支持的应用程序 | 预计的AI积分 |
|------|-----|------------------------|----------------------|
| Audience 代理 | 受众/帐户构思 | Real-Time CDP；Adobe Journey Optimizer | 50 |
| Audience 代理 | 基于知识的受众/帐户创建 | Real-Time CDP；Adobe Journey Optimizer | 150 |
| Audience 代理 | 受众/帐户管理 | Real-Time CDP；Adobe Journey Optimizer | 25 |
| Audience 代理 | 受众/帐户分析 | Real-Time CDP；Adobe Journey Optimizer | 25 |
| Audience 代理 | 购买团体创意 | Adobe Journey Optimizer (B2B) | 25 |
| Data Insights Agent | 数据分析和可视化 | Customer Journey Analytics | 25 |
| Data Insights Agent | 数据storytelling和共享 | Customer Journey Analytics | 100 |
| Journey Agent | 历程构思 | Adobe Journey Optimizer (B2B) | 25 |
| Journey Agent | 历程创建 | Adobe Journey Optimizer (B2B、B2C) | 30 |
| Journey Agent | 历程分析 | Adobe Journey Optimizer (B2B、B2C) | 50 |
| Journey Agent | 历程管理 | Adobe Journey Optimizer (B2B、B2C) | 25 |
| 产品支持代理 | 基于知识的故障排除 | 多个Experience Cloud应用程序 | 0 |
| 产品支持代理 | 支持案例创建和跟踪 | 多个Experience Cloud应用程序 | 10 |
| 内容审查程序代理 | 内容发现 | Adobe Experience Manager云服务 | 5 |
| 内容审查程序代理 | 内容更新和优化 | Adobe Experience Manager云服务 | 10 |
| 品牌体验代理 | 部署支持 | Adobe Experience Manager云服务 | 5 |
| 品牌体验代理 | 站点现代化 | Adobe Experience Manager云服务 | 100 |

**注意：**&#x200B;实际人工智能点数消耗可能因执行的步骤数和每步骤的迭代数而异。

