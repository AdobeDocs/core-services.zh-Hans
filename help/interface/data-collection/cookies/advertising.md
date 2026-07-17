---
description: 了解用于将广告互动事件映射到转化事件的Adobe Advertising Cookie，并可能使用该信息来优化广告投标。
title: Adobe Advertising Cookies
uuid: 2eec48a3-3e81-488e-8e30-5fd62885de0b
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 6818edea-31b1-49fc-bca2-32828c7ca78d
TQID: 'https://experienceleague.adobe.com/jr9RwaF63elDUN-XewIdrPNsGb6T5wo98vktP5U6jIM'
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: dab36b01-8bfa-48f3-8392-626455a058e6id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2: id: eb7e29b9-c5e9-4ed0-8e4b-6465dabb3cb1
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 9c2010694b8bb32c3922dd65f846375e43b2caac
workflow-type: tm+mt
source-wordcount: 309
ht-degree: 15%

---

# Adobe Advertising Cookie

Adobe Advertising（以前称为Adobe Advertising Cloud）使用Cookie将广告参与事件映射到转化事件，并可能使用该信息来优化广告投标。

>[!NOTE]
>
>测试版Adobe Advertising Javascript标记，它使用[Adobe CX Enterprise ID (ECID)服务](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=zh-Hans)创建第一方[CX Enterprise](experience-cloud.md) `s_ecid` Cookie，而不是Adobe Advertising Cookie。

| Cookie 名称 | 过期 | 大小 | 位置 | 描述 |
| --- | --- | --- | --- | --- |
| **`_lcc`** | 15 分钟 | 52 字节 | `everesttech.net` | 存储显示点击的ID和时间戳。 确定显示广告上的点击事件是否适用于Adobe Analytics点击。 |
| **`_tmae`** | 1 年 | 1 KB | `everesttech.net` | 使用DSP跟踪存储广告互动的编码ID和时间戳。 包含用户对广告的参与度，例如上次查看的广告 |
| **`_tmid`** | 1 年 | ~20 字节 | `everesttech.net` | 存储Adobe Advertising Demand Side Platform (DSP) ID。 对应于`everest_g_v2` Cookie中的访客ID。 |
| **`adcloud`** | 1 年 | 50-150字节 | 第一方 | 访客上次访问网站和上次搜索点击的时间戳。 还存储访客点击广告时创建的`ef_id`。 将访客ID与相关受众区段和转化关联。 通过避免向Adobe发出不必要的请求，帮助优化页面加载时间。 |
| **`ev_sync_*`** |  | 8 字节 | `everesttech.net` | 以`yyymmdd`格式执行同步的日期。 将Adobe Advertising访客ID与合作伙伴广告交换同步。 它是为新访客创建的，并在过期时发送同步请求。 包括Cookie `ev_sync_ax`、`ev_sync_bk`、`ev_sync_dd`、`ev_sync_fs`、`ev_sync_ix`、`ev_sync_nx`、`ev_sync_ox`、`ev_sync_pm`、`ev_sync_rc`、`ev_sync_tm`和`ev_sync_yh`。 |
| **`everest_g_v2`** | 1 年 | ~27 字节 | `everesttech.net` | 存储浏览器和访客ID。 在用户最初单击广告后创建。 用于将当前点击和后续点击与您网站上的其他事件进行映射。 |
| **`everest_session_v2`** | 会话 | ~16 字节 | `everesttech.net` | 存储当前会话ID。 |
| **`id_adcloud`** | 91 天 | 16 字节 | 第一方 | 存储访客ID。 |

{style="table-layout:auto"}

