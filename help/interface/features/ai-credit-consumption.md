---
title: 代理作业和AI信用消耗
description: 了解Experience Cloud应用程序中的代理工作和AI信用消耗率。
solution: Experience Cloud
topic: Artificial Intelligence
feature: Agentic AI, AI Tools
role: Admin, User
level: Intermediate
source-git-commit: fb09e31069b1eb9f035c115d89b4cd8b4a090583
workflow-type: tm+mt
source-wordcount: '1026'
ht-degree: 4%

---

# Adobe Experience Platform代理工作和AI积分消耗

更新日期：**2026年3月4日**

了解Experience Cloud应用程序中的智能人工智能就业和人工智能信用消费。 有关在现有Experience Cloud应用程序中启用代理AI功能的信息，请参阅Experience Cloud中的[代理AI](agentic-ai.md#existing-apps)。

## 代理作业

_代理作业_&#x200B;是代理执行的一系列任务和操作，以实现客户输入所指示的特定结果。

通过AI Assistant使用自然语言提示，可以要求代理执行特定作业。 根据这些输入，Agent Orchestrator协调相应的代理，以在相关的Experience Cloud应用程序中执行每个步骤。

## AI 积分

_AI点数_&#x200B;是一个基于使用情况的量度，它量化了代理作业的执行情况。 AI积分不适用于[AI优先应用程序](/help/interface/features/agentic-ai.md)。

## AI信用消费

根据所执行作业的复杂性和价值，AI信用使用可能有所不同：

* 简单（通常是单步）任务占用的积分较少
* 复杂（通常为多步）任务会消耗更多积分
* 涉及高级推理、验证、多代理协调或集成的任务消耗更多积分

### 估计的人工智能信贷消费率

| 代理 | 作业 | 支持的应用程序 | 估计的AI积分 | 示例提示 |
| ------ | ----- | ------------------------ | ----------------------- | ----------------- |
| Audience 代理 | 受众/帐户构思 | <ul><li>Real-Time CDP（B2B、B2C和B2P版本）</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 50 | <ul><li><em>为我显示富裕购买者的字段</em></li><li><em>查找与客户首选项相关的所有字段</em></li></ul> |
| Audience 代理 | 基于知识的受众/帐户创建 | <ul><li>Real-Time CDP（B2B、B2C和B2P版本）</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 150 | <ul><li><em>创建由住在加利福尼亚的人组成的受众</em></li><li><em>生成本季度支出超过$1000的VIP成员受众</em></li><li><em>构建一个受众，该受众包含购买服装但过去60天内未购买过的用户</em></li></ul> |
| Audience 代理 | 受众/帐户管理 | <ul><li>Real-Time CDP（B2B、B2C和B2P版本）</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 25 | <ul><li><em>我是否有任何重复的受众？</em></li><li><em>显示我最大的5个受众。</em></li><li><em>显示未激活到任何目标的受众</em></li><li><em>列出实时历程中使用的所有受众</em></li></ul> |
| Audience 代理 | 受众/帐户分析 | <ul><li>Real-Time CDP（B2B、B2C和B2P版本）</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 25 | <ul><li><em>哪些受众在上周增加了超过20%？</em></li><li><em>与30天前的值相比，受众“忠诚的白金”发生了多少变化？</em></li><li><em>我增长最快的受众是哪个？</em></li></ul> |
| Audience 代理 | 购买团体创意 | <ul><li>Adobe Journey Optimizer (B2B edition)</li></ul> | 25 | <ul><li><em>哪些帐户显示对这些产品的意图？</em></li><li><em>按XYZ的产品意图显示排名最前的用户。</em></li><li><em>哪些购买组的成员超过5个？</em></li></ul> |
| Data Insights Agent | 数据分析和可视化 | <ul><li>Customer Journey Analytics（B2C和B2B版本）</li></ul> | 25 | <ul><li><em>7月订单趋势</em></li><li><em>按地区显示收入。</em></li><li><em>按性别显示从3月到6月的订单。</em></li><li><em>6月份按利润计算我的前10个SKU是什么</em></li><li><em>按月份划分的购买比例</em></li><li><em>按产品类别划分的收入份额</em></li></ul> |
| Journey Agent | 历程构思 | <ul><li>Adobe Journey Optimizer (B2B edition)</li></ul> | 25 | <ul><li><em>为意图获取我的解决方案的空白帐户创建历程，重点关注参与网站内容的人员</em></li></ul> |
| Journey Agent | 历程创建 | <ul><li>Adobe Journey Optimizer（B2B和B2C版本）</li></ul> | 30 | <ul><li><em>生成历程以向过去7天内未完成首次购买的用户发送提醒</em></li><li><em>用户完成首次购买后，在3天后通过电子邮件发送短信确认和后续权益说明</em></li></ul> |
| Journey Agent | 历程分析 | <ul><li>Adobe Journey Optimizer（B2B和B2C版本）</li></ul> | 50 | <ul><li><em>我要对7月4日营销活动的历程按节点分析流失。</em></li><li><em>历程X是否存在任何计划冲突</em></li><li><em>向我显示历程X的受众重叠冲突</em></li></ul> |
| Journey Agent | 历程管理 | <ul><li>Adobe Journey Optimizer（B2B和B2C版本）</li></ul> | 25 | <ul><li><em>我有多少个实时历程？</em></li><li><em>列出使用受众X的所有历程。</em></li><li><em>列出当前处于测试模式的所有历程</em></li></ul> |
| 产品支持代理 | 基于知识的故障排除 | <ul><li>Real-Time CDP（B2B、B2C和B2P版本）</li><li>Adobe Journey Optimizer（B2C和B2B版本）</li><li>Customer Journey Analytics（B2C和B2B版本）</li></ul> | 0 | <ul><li><em>为什么我的配置文件计数在“许可证使用情况”仪表板和Experience Platform主页上不同？</em></li><li><em>历程未触发的原因是什么？</em></li><li><em>Adobe Experience Platform如何创建实时体验？</em></li><li><em>如何在Adobe Experience Platform中配置和使用警报？</em></li><li><em>Adobe Experience Platform Activation的平均配置文件丰富度限制是多少？</em></li></ul> |
| 产品支持代理 | 支持案例创建和跟踪 | <ul><li>Real-Time CDP（B2B、B2C和B2P版本）</li><li>Adobe Journey Optimizer（B2C和B2B版本）</li><li>Customer Journey Analytics（B2C和B2B版本）</li><li>Adobe Experience Manager</li></ul> | 10 | <ul><li><em>为失败的分段作业创建新的支持票证</em></li><li><em>票证E-001772068的状态如何？</em></li></ul> |
| 内容审查程序代理 | 内容发现 | <ul><li>Adobe Experience Manager</li></ul> | 5 | <ul><li><em>显示用于创建WKND选件促销活动的内容片段。</em></li><li><em>查找产品包装PNG映像。</em></li><li><em>在文件夹WKND中显示带有标记的Office图像。</em></li><li><em>文件夹WKND中是否有任何svg？</em></li><li><em>显示所有贷款申请表。</em></li><li><em>我正在查找员工入门培训表。</em></li></ul> |
| 内容审查程序代理 | <ul><li>内容优化</li></ul> | <ul><li>Adobe Experience Manager Assets和Dynamic Media</li></ul> | 10 | <ul><li><em>创建质量为80%的2000px演绎版作为JPEG。</em></li><li><em>为Instagram故事创建演绎版。</em></li><li><em>在促销横幅上覆盖图像，用30%的折扣图绘制，从中心放置100像素。</em></li><li><em>将PNG的背景颜色更改为#ff8932。</em></li></ul> |
| 品牌治理代理 | <ul><li>品牌策略检查</li></ul><ul><li>Content Hub的权限</li></ul><ul><li>资产到期</li></ul> | <ul><li>Adobe Experience Manager Sites（品牌策略）</li></ul><ul><li>Adobe Experience Manager Assets</li></ul> | 25 | <ul><li><em>此页面是否符合我的品牌？`https://www.website/en.html`</em></li><li><em>显示所有现有的Content Hub ABAC规则</em></li><li><em>我的任何资源是否即将过期？</em></li></ul> |
| 品牌体验代理 | <ul><li>内容更新</li><li>Forms创建</li><li>管道故障排除</li></ul> | <ul><li>Adobe Experience Manager云服务</li><li>Adobe Experience Manager Sites</li><li>Adobe Experience Manager Forms</li></ul> | 50 | <ul><li><em>在`URL`上，将标题更新为Hello world</em></li><li><em>生成包含姓名、电子邮件和消息字段的联系人表单</em></li><li><em>对失败的管道进行故障排除</em></li><li><em>列出主项目的失败管道。</em></li></ul> |
| 品牌体验代理 | 站点现代化 | Adobe Experience Manager云服务 | 100 | <ul><li><em>迁移页面`https://wknd-trendsetters.site`</em></li></ul> |

>[!NOTE]
>
>根据执行的步骤数和每步骤的迭代数，实际AI点数消耗可能会有所不同。

## 有关此主题的更多帮助

* [Experience Cloud中的GenAI](/help/interface/features/generative-ai.md)
* [Experience Cloud的人工智能](/help/interface/features/agentic-ai.md)
* [Adobe Experience Platform代理使用量绑定试用](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/trial)
