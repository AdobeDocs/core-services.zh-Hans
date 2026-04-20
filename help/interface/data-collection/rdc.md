---
title: 地区数据收集
description: 了解CX Enterprise中的区域数据收集。
exl-id: 295e9736-2a58-48a8-9968-5dfa33b70d95
TQID: https://experienceleague.adobe.com/hjHQDRoNOP2e6pKhKHB9DZaII2o8eJVzL5wjRzaMFwM
product_v2:
  - id: e1971122-7081-4556-9222-8a31bd71800c
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 1a77ef8d31211fb11c790152e78037a8c3b238a2
workflow-type: tm+mt
source-wordcount: 299
ht-degree: 0%

---

# 地区数据收集

Adobe CX Enterprise使用区域数据收集(RDC)，以便访客与Adobe之间的交互尽可能靠近访客。 在边缘站点本地收集的数据安全地转发到核心站点以供处理。 处理之后，该数据便可用于Adobe CX Enterprise产品和服务。

区域数据收集工作流具备以下优势：

* **性能**：使用RDC，访客连接到最近的边缘站点。 此优化可提供最快的响应时间，从而实现更准确的跟踪和更快的加载时间。
* **冗余**：如果任何边缘站点与核心站点之间的通信中断，Adobe的基础架构会在本地保存数据，然后在通信恢复时将数据转发到核心站点。 如果特定位置遇到中断，Adobe还可以将流量路由到其他边缘站点。

RDC当前包括以下位置（可能发生变化）：

## 第一方数据收集

| RDC类型 | 数据收集中心 |
| --- | --- |
| 全局（默认） | 俄勒冈、弗吉尼亚、爱尔兰、巴黎、孟买、新加坡、东京、悉尼 |
| 全球+中国* | 北京*、俄勒冈、弗吉尼亚、爱尔兰、巴黎、孟买、新加坡、东京、悉尼 |
| 仅限美洲 | 俄勒冈州、弗吉尼亚州 |
| 仅限欧洲 | 爱尔兰、巴黎 |
| 仅限亚太地区 | 孟买、新加坡、东京、悉尼 |
| 仅限中国* | 北京 |

{style="table-layout:auto"}

_*中国RDC需要中国性能优化加载项包，并且仅适用于使用AppMeasurement数据收集的Adobe Analytics。 不支持其他CX Enterprise服务和Web SDK数据收集。 请联系您的Adobe客户团队以了解有关“中国性能优化”附加组件包的更多信息。_

## 第三方数据收集

第三方数据收集包括与您的网站域不匹配的Cookie域。 示例包括`adobedc.net`、`omtrdc.net`和`2o7.net`。

| RDC类型 | 数据收集中心 |
| --- | --- |
| 默认 | 俄勒冈、弗吉尼亚、爱尔兰、巴黎、孟买、新加坡、东京、悉尼 |
| 默认+中国* | 北京*、俄勒冈、弗吉尼亚、爱尔兰、巴黎、孟买、新加坡、东京、悉尼 |

{style="table-layout:auto"}

