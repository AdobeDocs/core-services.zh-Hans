---
title: 代理作业和AI信用消耗
description: 了解Experience Cloud应用程序中的代理工作和AI信用消耗率。
solution: Experience Cloud
topic: Artificial Intelligence
feature: Agentic AI, AI Tools
role: Admin, User
level: Intermediate
source-git-commit: bb6adf13bed37d4a885b5baec28199efade592e1
workflow-type: tm+mt
source-wordcount: '965'
ht-degree: 3%

---

# Adobe Experience Platform代理工作和AI积分消耗

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
| ------ |-----|------------------------|----------------------|----------------|
| Audience 代理 | 受众/帐户构思 | <ul><li>Real-Time CDP（B2B、B2C和B2P版本）</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 50 | <ul><li>为我显示富裕买家的字段</li><li>查找与客户首选项相关的所有字段</li></ul> |
| Audience 代理 | 基于知识的受众/帐户创建 | <ul><li>Real-Time CDP（B2B、B2C和B2P版本）</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 150 | <ul><li>创建由住在加利福尼亚的人组成的受众</li><li>生成本季度支出超过$1000的VIP成员受众</li><li>构建一个受众，其中包含购买服装但过去60天内未购买过的用户</li></ul> |
| Audience 代理 | 受众/帐户管理 | <ul><li>Real-Time CDP（B2B、B2C和B2P版本）</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 25 | <ul><li>我是否有任何重复的受众？</li><li>显示我最大的5个受众。</li><li>显示未激活到任何目标的受众</li><li>列出实时历程中使用的所有受众</li></ul> |
| Audience 代理 | 受众/帐户分析 | <ul><li>Real-Time CDP（B2B、B2C和B2P版本）</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 25 | <ul><li>上周哪些受众的规模扩大了20%以上？</li><li>与30天前的值相比，受众“忠诚的白金”发生了多少变化？</li><li>我增长最快的受众是什么？</li></ul> |
| Audience 代理 | 购买团体创意 | <ul><li>Adobe Journey Optimizer (B2B edition)</li></ul> | 25 | <ul><li>哪些客户显示对这些产品的意图？</li><li>按XYZ的产品意图显示排名靠前的人员。</li><li>哪些购买团体拥有5个以上的成员？</li></ul> |
| Data Insights Agent | 数据分析和可视化 | <ul><li>Customer Journey Analytics（B2C和B2B版本）</li></ul> | 25 | <ul><li>7月趋势订单</li><li>按地区显示收入。</li><li>按性别显示从3月到6月的订单。</li><li>6月份我的前10个SKU（按利润计算）是什么？</li><li>按月份划分的购买比例</li><li>按产品类别分列的收入份额</li></ul> |
| Journey Agent | 历程构思 | <ul><li>Adobe Journey Optimizer (B2B edition)</li></ul> | 25 | <ul><li>为意图用于我的解决方案的空白帐户创建一个历程，重点关注参与网站内容的人员</li></ul> |
| Journey Agent | 历程创建 | <ul><li>Adobe Journey Optimizer（B2B和B2C版本）</li></ul> | 30 | <ul><li>生成历程以向过去7天内未完成首次购买的用户发送提醒</li><li>用户完成首次购买后，在3天后通过电子邮件发送短信确认信和跟进权益说明</li></ul> |
| Journey Agent | 历程分析 | <ul><li>Adobe Journey Optimizer（B2B和B2C版本）</li></ul> | 50 | <ul><li>我想对7月4日营销活动旅程的按节点分析流失。</li><li>历程X是否存在任何计划冲突</li><li>显示历程X的受众重叠冲突</li></ul> |
| Journey Agent | 历程管理 | <ul><li>Adobe Journey Optimizer（B2B和B2C版本）</li></ul> | 25 | <ul><li>我有多少个实时历程？</li><li>列出使用受众X的所有历程。</li><li>列出当前处于测试模式的所有历程</li></ul> |
| 产品支持代理 | 基于知识的故障排除 | <ul><li>Real-Time CDP（B2B、B2C和B2P版本）</li><li>Adobe Journey Optimizer（B2C和B2B版本）</li><li>Customer Journey Analytics（B2C和B2B版本）</li></ul> | 0 | <ul><li>为什么我的配置文件计数在“许可证使用情况”仪表板和Experience Platform主页上有所不同？</li><li>历程未触发的原因是什么？</li><li>Adobe Experience Platform如何创建实时体验？</li><li>如何在Adobe Experience Platform中配置和使用警报？</li><li>Adobe Experience Platform Activation中的平均配置文件丰富度限制是多少？</li></ul> |
| 产品支持代理 | 支持案例创建和跟踪 | <ul><li>Real-Time CDP（B2B、B2C和B2P版本）</li>Adobe Journey Optimizer（B2C和B2B版本）<li>Customer Journey Analytics（B2C和B2B版本）</li><li>Adobe Experience Manager</li></ul> | 10 | <ul><li>为我的分段作业失败创建新的支持工单</li><li>票证E-001772068的状态如何？</li></ul> |
| 内容审查程序代理 | 内容发现 | <ul><li>Adobe Experience Manager云服务</li></ul> | 5 | <ul><li>显示用于创建WKND优惠活动的内容片段。</li><li>查找产品包装PNG图像。</li><li>在文件夹WKND中显示带有办公室标记的图像。</li><li>WKND文件夹中是否有任何svg？</li><li>显示所有贷款申请表。</li><li>我在找员工入职表。</li></ul> |
| 内容审查程序代理 | <ul><li>内容更新</li><li>内容优化</li><li>Forms创建</li></ul> | <ul><li>Adobe Experience Manager云服务</li></ul> | 10 | <ul><li>创建质量为80%的2000px演绎版as JPEG。</li><li>为Instagram故事创建演绎版。</li><li>在促销横幅上叠加有30%折扣的图像，从中心位置放置100像素。</li><li>将PNG的背景颜色更改为#ff8932。</li></ul> |
| 品牌体验代理 | <ul><li>体验支持</li><li>部署支持</li></ul> | <ul><li>Adobe Experience Manager云服务</li></ul> | 5 | <ul><li>解决我失败的管道问题</li><li>列出主项目的失败管道。</li><li>分析名为“开发管道”的失败管道。</li><li>管道执行1234567疑难解答</li></ul> |
| 品牌体验代理 | 站点现代化 | Adobe Experience Manager云服务 | 100 | <ul><li>迁移页面https://wknd-trendsetters.site</li></ul> |

>[!NOTE]
>
>根据执行的步骤数和每步骤的迭代数，实际AI点数消耗可能会有所不同。

## 有关此主题的更多帮助

* [Experience Cloud的人工智能](/help/interface/features/agentic-ai.md)
* [Adobe Experience Platform代理使用量绑定试用](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/trial)