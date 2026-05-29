---
title: 代理AI使用监控
description: 了解CX Enterprise中的AI使用情况监控。 跟踪采用情况、审查对话和反馈，并管理使用、质量和成本可见性的AI积分。
solution: Experience Cloud, Experience Platform
topic: Artificial Intelligence
feature: Agentic AI, AI Tools
role: Admin, User
level: Intermediate
autotag-review: '2026-05-27T16:30:16.764Z'
TQID: 'https://experienceleague.adobe.com/J74yr0gGkFu1bzTmMvhrQ8TNaRX6nRjWY9WAwd3uydk'
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
  - id: e1971122-7081-4556-9222-8a31bd71800c
feature_v2:
  - id: f84b2906-3ce9-4ef0-86f6-cda249273937
subfeature_v2:
  - id: cda95149-19e1-4cfa-a57e-751283a32378
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
source-git-commit: 294e1638dc175d94fcd01927dbc6e6caafddf3f6
workflow-type: tm+mt
source-wordcount: 948
ht-degree: 2%

---

# 代理AI使用情况监视仪表板

CX Enterprise提供两个仪表板，用于监视现有CX Enterprise应用程序中的代理AI使用情况。 这些仪表板可帮助您了解用户通过[!DNL AI Assistant]和其他对话界面访问的[!DNL Experience Platform Agents]的采用、参与、反馈质量和AI信用消耗。

在Adobe CX Enterprise的[代理AI](agentic-ai.md)文档中，使用监视作用域中的代理列在现有CX Enterprise应用程序[&#128279;](agentic-ai.md#existing-apps-table)中的AI代理中。

## 许可证用量仪表板

[!DNL Adobe Experience Platform]许可证使用情况仪表板显示您组织的已许可AI积分权利以及在用户运行[!DNL Experience Platform Agents]时消耗的AI积分总数。

管理员使用此功能板根据权利跟踪许可证使用情况。 要访问仪表板，请参阅[!DNL Experience Platform]文档中的[许可证使用情况仪表板](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/dashboards/guides/license-usage)。

## Agentic AI监控仪表板

人工智能监测仪表板使卓越中心(COE)成员和其他治理利益攸关方能够了解人工智能的使用和采用。 您可以查看7天或30天期间的趋势，以了解谁使用[!DNL AI Assistant]或其他对话界面（如[Adobe Marketing Agent for Microsoft 365 Copilot](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-ai/experience-cloud-ai/agents/ama-ms)）与[!DNL Experience Platform Agents]交互，他们在这些交互中执行的操作，以及他们收到的值。

Agentic AI监控仪表板包括以下视图：

| 功能板 | 用途 |
| --- | --- |
| **概述** | 跨用户、对话、反馈和信用消耗的汇总量度 |
| **用户** | 按用户的使用频率、分布和参与 |
| **反馈** | 响应质量和用户满意度的信号 |
| **AI积分** | 信用消耗趋势和余额 |

这些视图共同帮助您使用数据而不是假设来指导代理采用。

## 概述仪表板

概述仪表板是整个组织中采用和参与量度的中心位置。 它将高级趋势与更深入的分析联系起来。 通过任何量度，您可以深入查看各个对话，以了解数字背后的驱动因素。

### “概述”功能板上的量度

* **随时间推移提示：**&#x200B;总体使用增长和采用趋势。
* **活动用户和对话：**&#x200B;与[!DNL Experience Platform Agents]交互的用户数。
* **每个对话的平均提示数：**&#x200B;每个对话的参与深度。
* **反馈：**&#x200B;来自用户的向上和向下拇指分布反馈（仅适用于[!DNL AI Assistant]交互）。

### 对话重播

对话重放显示单个交互，而不仅仅是聚合。 您可以分析多个对话的模式，并从高级趋势转移到特定对话。

* **提示和响应历史记录：**&#x200B;用户的提示和响应已传递。
* **反馈信号：**&#x200B;用户通过竖起或竖下大拇指进行交互，以识别摩擦、阻止或支持需求。 此信息可帮助您的组织改善提示相关性，并帮助Adobe在一段时间内提高响应质量。

## 用户仪表板

“用户”仪表板显示随着时间的推移，不同用户的代理采用和参与度的变化。 您可以查看哪些人主动使用[!DNL Experience Platform Agents]，他们使用哪个表面以及他们参与的频率。 管理员和COE成员可以深入了解各个用户活动和对话，以了解参与模式和使用行为。

### 用户仪表板上的量度

* **一段时间内的采用和参与趋势：**&#x200B;跟踪选定时间段内用户区段的变化情况。 用户被分类为：
   * **新：**&#x200B;选定时段内的第一个活动，前12个月内无活动。
   * **重复：**&#x200B;选定时段和上一个时段中的活动。
   * **返回：**&#x200B;选定时段内的活动，但不是前一时段内的活动。
   * **不活动：**&#x200B;选定时段中没有活动，但前一时段有活动。
* **用户参与模式：**&#x200B;用户与代理进行交互的频率以及参与随时间变化的频率。
* **对话活动：**&#x200B;每个用户的对话数和提示数。
* **最活跃用户：**&#x200B;高度参与的用户和团队推动采用代理。

## 反馈仪表板

“反馈”仪表板显示针对代理交互提交的用户反馈。 您可以查看哪些对话用户以正面或负面方式标记，并调查反馈背后的交互。 从反馈摘要中，深入查看各个对话以查看提示、响应、推理详细信息和反馈注释。

### 反馈仪表板上的量度

* **反馈随时间变化的趋势：**&#x200B;用户反馈随时间变化的方式。
* **向上和向下拇指反馈：**&#x200B;正面和负面交互信号。
* **反馈类别：**&#x200B;每条竖起大拇指和竖起大拇指背后的理由。
* **提示和响应历史记录：**&#x200B;用户提示和与提交的反馈关联的响应。
* **反馈详细信息和注释：**&#x200B;反馈提交期间用户的其他上下文和注释。

## AI信用仪表板

AI信用仪表板显示贵组织对[!DNL Experience Platform Agents]的使用如何转化为AI信用消费。

### AI信用仪表板上的量度

* **已使用的AI积分总数：** AI积分中的代理总使用量。
* **每日和每月趋势：**&#x200B;消费模式的尖峰、下降和变化。
* **AI剩余信用额度：**&#x200B;剩余信用额度，以便您能够主动计划并避免超额。

## 访问和管理

Agentic AI使用监控仪表板公开AI Assistant活动，包括使用模式、对话级别的洞察、反馈信号和操作量度。 这些信息中有些可能包括敏感的业务上下文、提示活动或用户交互数据。

访问权限基于权限，仅供授权的COE管理员和批准的管理用户使用。 以下部分将介绍如何授予仪表板权限。

## 启用功能板权限

通过更新每个授权用户的产品配置文件或角色，在[!DNL Adobe Experience Platform]中授予仪表板访问权限。

1. 转到[!DNL Experience Platform] **管理** > **权限**。

1. 打开要更新的产品配置文件或角色。

   ![启用仪表板权限](../features/assets/dashboards-permissions.png)

1. 在&#x200B;**[!UICONTROL AI Assistant]**&#x200B;权限下，单击&#x200B;**[!UICONTROL Add Resource]**，然后启用&#x200B;**[!UICONTROL View AI Assistant usage dashboard]**。

   此权限授予对Agentic AI使用监控仪表板的访问权限。

1. 在&#x200B;**[!UICONTROL Dashboards]**&#x200B;权限下，根据每个用户的责任配置仪表板访问权限。

   ![启用仪表板权限](../features/assets/dashboards-add-resource.png)

   授权治理用户的建议权限：

   * **[!UICONTROL View License Usage Dashboard]**
   * **[!UICONTROL View Standard Dashboards]**
   * **[!UICONTROL Export Dashboard Data]** （可选，仅适用于已批准的治理用户）

   您可以根据需要授予的其他权限：

   * **[!UICONTROL Manage Custom Dashboards]**
   * **[!UICONTROL View Custom Dashboards]**
   * **[!UICONTROL Manage Standard Dashboards]**

## 有关此主题的更多帮助

* [Adobe CX Enterprise中的代理AI](agentic-ai.md)
* [代理作业和AI信用消耗](ai-credit-consumption.md)
* [许可证使用情况仪表板](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/dashboards/guides/license-usage) (Experience Platform)
