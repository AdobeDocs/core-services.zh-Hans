---
description: 如何配置 Experience Cloud 触发器。
keywords: integrations;Triggers
seo-description: 如何配置 Experience Cloud 触发器。
seo-title: 触发器
solution: Marketing Cloud
title: 触发器
uuid: dab536e3-1969-4661-919e-5b15f423fecd
translation-type: tm+mt
source-git-commit: fb03bf89bcc6ed4438daf18c8415de3052ba8fa4
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 96%

---


# 触发器

## 触发器概述 {#topic_4F21FCE9A64E46E8B6D51F494FA652A7}

触发器允许您识别、定义并监视关键客户行为，然后生成跨解决方案通信以便重新吸引访客。您可以在实时决策和个性化中使用触发器。

* 为购物车放弃或已删除产品的购物车放弃配置快速再营销
* 表单和应用程序不完整
* 网站上的任何操作或操作序列

![](assets/trigger-abandonment-2.png)

### 触发器类型

通常，触发器可能要用 15-90 分钟时间才能启动市场营销活动。此时间根据数据收集的实施、管道的加载、定义触发器的自定义配置以及 Adobe Campaign 中的工作流而有所不同。

* **放弃：**&#x200B;您可以创建一个触发器，该触发器将在访客查看了产品却未将任何产品添加到购物车时启动。
* **操作：**&#x200B;您可以创建触发器，例如，在新闻稿注册、电子邮件订阅或信用卡申请（确认）后触发的触发器。如果您是零售商，则可以针对注册会员计划的访客创建一个触发器。在媒体和娱乐业中，可以为观看特定节目并且您可能想要收集调查结果的访客创建触发器。
* **会话开始和会话结束：**&#x200B;为会话开始和会话结束事件创建触发器。

## 创建 Experience Cloud 触发器 {#task_821F37183AC045E5AC8EED20317598FE}

创建触发器并配置触发器的条件。 例如，您可以指定访问期间触发器规则的条件，如量度（购物车放弃）或维度（产品名称）。当满足规则时，触发器会运行。

>[!NOTE]
>
>当前的技术限制为 100 个触发器。

1. In the Experience Cloud, click ![](assets/menu-icon.png), then click **[!UICONTROL Launch]**.
2. Locate the [!UICONTROL Triggers] card, then click **[!UICONTROL Manage Triggers]**.
3. 单击&#x200B;**[!UICONTROL 新建触发器]**，然后指定触发器类型：

   ![步骤结果](assets/add-trigger.png)

4. 通过填写以下字段，并将量度和维度项拖动到规则容器中以配置该触发器：

   | 元素 | 描述 |
   |--- |--- |
   | 名称 | 此触发器的友好名称。 |
   | 描述 | 此触发器的描述、使用方式等。 |
   | 报表包 | 用于此触发器的 Analytics [报表包](https://docs.adobe.com/content/help/zh-Hans/analytics/implementation/analytics-basics/ref-reports-report-suites.html)。此设置标识要使用的报表数据。 |
   | 必须包括的访问<br>必须排除的访问<br>没有行动后启动触发器<br>包括元数据 | 您可以定义希望发生的标准或访客行为，以及不希望发生的行为。例如，一个简单的购物车放弃触发器规则可能是：<ul><li>必须包括的访问：购物车加货（量度）和存在。（您可以进一步完善规则，以包含特定产品视图或浏览器类型等维度。）</li><li>必须排除的访问：结帐。</li><li>没有行动后启动触发器：10 分钟。</li><li>包括元数据：允许您添加特定的营销活动维度或与访客行为相关的变量。此字段对 Adobe Campaign 生成正确的再营销电子邮件十分有用。</li></ul><br>您可以在容器内或容器之间指定 Any、And 或 Or 逻辑，具体取决于您确定的标准是否对规则很重要。 |
   | 容器 | 容器是您设置和存储定义触发器的规则、条件或过滤器的位置。如果希望事件同时发生，请将其置于同一容器中。这意味着，每个容器在命中级别中独立处理。例如，如果您有两个由 And 运算符连接的容器，那么当两个命中符合要求时，可以预计这些规则符合条件。 |
   | 没有行动后开始新会话 | 为会话开始和会话结束事件创建触发器。 |

5. 单击&#x200B;**[!UICONTROL 保存]**。
6. 使用这些触发器在 [!DNL Adobe Campaign] 中进行[实时再营销](https://docs.campaign.adobe.com/doc/standard/en/EMA_Transactional_messaging_Marketing_Cloud_Triggers.html)。

### 触发器示例

Experience Cloud 触发器示例：

#### 购物车放弃触发器

例如，以下页面显示了您可以根据访问期间已查看的产品，用于购物车放弃触发器的规则。

![](assets/abandonment-trigger.png)

#### 反向链接触发器

当点击中包含 Men&#39;s Boots 的产品和 Facebook 的反向链接时，就会触发以下触发器。对于要在同一点击中评估的两个条件（*产品*&#x200B;和&#x200B;*反向链接*），应将它们添加到同一容器中。

![](assets/fb-boots-promo.png)
