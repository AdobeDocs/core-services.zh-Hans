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
ht-degree: 42%

---


# 触发器

## 触发器概述 {#topic_4F21FCE9A64E46E8B6D51F494FA652A7}

触发器使您能够识别、定义和监控关键的消费者行为，然后生成跨解决方案通信以重新吸引访客。 您可以在实时决策和个性化中使用触发器。

* 为放弃购物车或放弃购物车而删除产品配置快速再营销
* 表单和应用程序不完整
* 网站上的任何操作或操作序列

![](assets/trigger-abandonment-2.png)

### 触发器类型

通常，触发器可能要用 15-90 分钟时间才能启动市场营销活动。此时间根据数据收集的实施、管道的加载、定义触发器的自定义配置以及 Adobe Campaign 中的工作流而有所不同。

* **放弃：**&#x200B;您可以创建一个触发器，该触发器将在访客查看了产品却未将任何产品添加到购物车时启动。
* **操作：** 例如，您可以创建触发器，以便在新闻稿注册、电子邮件订阅或信用卡申请（确认）后触发。 如果您是零售商，则可以为注册忠诚度项目的访客创建触发器。 在媒体和娱乐业中，为观看某个节目的访客创建触发器，也许您希望用调查来回应。
* **会话开始和会话结束：** 为会话开始和会话结束事件创建触发器。

## 创建 Experience Cloud 触发器 {#task_821F37183AC045E5AC8EED20317598FE}

创建触发器并配置触发器的条件。 例如，您可以指定访问期间触发器规则的条件，如度量（如“放弃购物车”）或维（如产品名称）。 当满足规则时，触发器会运行。

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
   | 报表包 | 用于此 [触发器](https://docs.adobe.com/content/help/en/analytics/implementation/analytics-basics/ref-reports-report-suites.html) 的Analytics报表包。 此设置标识要使用的报告数据。 |
   | Visit must include<br>Visit must not include<br>Trigger after no action<br>Include meta data | 您可以定义希望发生的标准或访客行为，以及不希望发生的行为。例如，一个简单的购物车放弃触发器规则可能是：<ul><li>必须包括的访问：购物车加货（量度）和存在。（您可以进一步完善规则，以包含特定产品视图或浏览器类型等维度。）</li><li>必须排除的访问：结帐。</li><li>没有行动后启动触发器：10 分钟。</li><li>包括元数据：允许您添加特定的营销活动维度或与访客行为相关的变量。此字段对 Adobe Campaign 生成正确的再营销电子邮件十分有用。</li></ul><br>您可以在容器内或容器之间指定 Any、And 或 Or 逻辑，具体取决于您确定的标准是否对规则很重要。 |
   | 容器 | 容器是您设置和存储定义触发器的规则、条件或过滤器的位置。 如果希望事件同时发生，请将其放在同一容器。 这意味着，每个容器在命中级别中独立处理。例如，如果您有两个由 And 运算符连接的容器，那么当两个命中符合要求时，可以预计这些规则符合条件。 |
   | 开始后的新会话 | 为会话开始和会话结束事件创建触发器。 |

5. 单击&#x200B;**[!UICONTROL 保存]**。
6. Use triggers for [real-time remarketing](https://docs.campaign.adobe.com/doc/standard/en/EMA_Transactional_messaging_Marketing_Cloud_Triggers.html) in [!DNL Adobe Campaign].

### 触发器示例

Experience Cloud触发器示例：

#### 购物车放弃触发器

例如，下页显示了您可能用于“购物车放弃”触发器的规则，这些规则基于在访问期间查看的产品。

![](assets/abandonment-trigger.png)

#### 推荐人触发器

当Men&#39;s Boots和Facebook的推荐人产品出现点击时，以下触发器会触发。 For the two criteria (*products* and *referrer*) to be evaluated in the same hit, they should be added to the same container.

![](assets/fb-boots-promo.png)
