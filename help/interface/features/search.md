---
description: 了解CX Enterprise中某些应用程序的统一搜索功能。
solution: Experience Cloud
title: Experience Cloud统一搜索
index: true
feature: Central Interface Components
topic: Administration
role: Admin
level: Beginner
exl-id: 70586f18-6f84-4308-bab3-1da7fab823d6
TQID: https://experienceleague.adobe.com/xE4H6kdjbKSwVygCsOV4zTBqPoBHAVMHfJMyYOummg0
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
  - id: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 50012e2564e88e1a6e16578e3331136c7df0cb21
workflow-type: tm+mt
source-wordcount: 639
ht-degree: 0%

---

# CX Enterprise中的[!UICONTROL Unified Search]

通过[!UICONTROL Unified Search]搜索，您可以在一种无缝、一致、一键式的体验中查找可搜索的业务对象或实体。 此搜索还会显示您最近访问的对象。

![全局搜索对象和实体](../assets/platform-search.png)

## 正在访问[!UICONTROL Unified Search]

[!UICONTROL Unified Search]在页面顶部的CX Enterprise页眉的每个页面上都可用。 您还可以使用键盘快捷键`command /`或`ctrl /`来访问搜索。

此功能仅适用于受支持的产品，这些产品目前为：

* Experience Platform (AEP)
* Journey Optimizer (AJO)

随着将更多内容加入索引，此功能将添加到相关应用程序。

## 可搜索的对象和字段

键入时，将显示您有权访问的对象中匹配的排名最前的结果。

我们的算法首先显示最相关的记录。 结果的顺序取决于多种因素，例如：

您的功能和对象权限
匹配百分比
是否存在完全匹配的项

CX Enterprise中的![[!UICONTROL Unified Search]](../assets/unified-search-results.png)

可搜索的业务对象包括：

* 区段（名称、描述、ID）
* 架构（名称、描述、ID）
* 数据集（名称、描述、ID）
* 源（名称、描述、ID）
* 目标（名称、描述、ID）
* 查询（名称、描述、ID）
* 消息（名称、描述、ID）
* 选件（名称、描述、ID）
* 组件（名称、描述、ID）
* 历程（名称、描述、ID）

如果关键字与某个导航页面匹配，则您可获得该导航页面的示例数据集的快速访问链接。 排名最前结果部分显示排名前30的结果。

您还可以从Experience League和Communities找到帮助文章。 支持自然语言查询。

例如，_如何创建架构_&#x200B;将从Experience League中生成&#x200B;_[!UICONTROL Learning]_&#x200B;下的结果：

CX Enterprise帮助中的![[!UICONTROL Unified Search]](../assets/unified-search-learning.png)

搜索算法会首先显示最相关的记录。 结果的顺序取决于多种因素，例如：

* 访问对象的用户权限
* 匹配百分比
* 精确匹配
* _[!UICONTROL Top Results]_&#x200B;部分显示前30个结果。

要优化您的搜索，请单击下列选项之一：

* **[!UICONTROL All Learning]**：在Experience League中打开搜索。
* **[!UICONTROL Show all...]**：使您可进一步细化和筛选结果。

## [!UICONTROL Unified Search]功能

统一搜索中提供了以下功能。

| 功能 | 描述 |
| ------- | ------- |
| 全球语言支持 | 全局搜索能够理解查询，并会生成德语、西班牙语、法语、意大利语、日语、朝鲜语、葡萄牙语和中文结果。 |
| 拼写容错 | 统一搜索使用高级算法提供了可靠的拼写容错。 这些算法计算编辑内容并提供适当的结果。 |
| 突出显示 | 搜索响应会突出显示搜索查询中的匹配关键词，以便您轻松找到与查询匹配的部分和单词。 突出显示也可用于拼写错误的单词。 |
| 代码片段 | 在搜索响应中，您可以看到结果的一个片段。 片段将返回匹配的单词以及围绕匹配关键词的一些内容。 |
| 停用词 | 英语中的一些常用单词被定义为&#x200B;_停用词_。 如果搜索查询中包含停用词，则给予该查询的权重会较低。 <br>停用词包括：_a、an、and、are、as、at、be、but、by、for、if、in、into、is、it、no、not、of、on、or、such、that、the、their、then、there、these、they、this、to、was、will、with_。 <br>其他全局语言不支持停用词。 |
| 自然语言查询 | 当您从Experience League Communities搜索帮助文章或讨论时，您可以使用自然语言键入您的问题并获得响应。 示例搜索：“如何创建架构？” |
| 带引号的精确搜索 | 您可以在查询中使用引号来进行精确搜索。 精确匹配查询中不会纠正拼写错误。 例如：“Luma历程2022”。 |
| 过滤器 | 您可以在完整搜索结果弹出窗口中应用&#x200B;_对象类型_&#x200B;等筛选器以及其他对象特定的筛选器。 在键入搜索查询内容并按Enter键后，将打开一个包含筛选器的完整页面弹出窗口。 |

{style="table-layout:auto"}

## 找不到它？

尝试以下提示：

* 输入更具体的搜索词
* 检查拼写
* 尝试编写完整的搜索词
* 确保您拥有搜索对象的权限

