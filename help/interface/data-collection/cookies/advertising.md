---
description: 了解用于将广告参与事件映射到转化事件的Adobe AdvertisingCookie，并可能使用该信息来优化广告投标。
title: Adobe Advertising Cookie
uuid: 2eec48a3-3e81-488e-8e30-5fd62885de0b
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 6818edea-31b1-49fc-bca2-32828c7ca78d
source-git-commit: 4d2dc1e6126e26f61475efbd33efe98bd47153d5
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 13%

---

# Adobe Advertising Cookie

Adobe Advertising(以前称为Adobe Advertising Cloud)使用Cookie将广告参与事件映射到转化事件，并可能使用该信息来优化广告投标。

>[!NOTE]
>
>测试版Adobe AdvertisingJavascript标记，它使用 [Adobe Experience Cloud ID (ECID)服务](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=zh-Hans) 创建第一方 [Experience Cloud](experience-cloud.md) `s_ecid` Cookie，而不是Adobe AdvertisingCookie。

| Cookie 名称 | 过期 | 大小 | 位置 | 描述 |
| --- | --- | --- | --- | --- |
| **`_lcc`** | 15 分钟 | 52 字节 | `everesttech.net` | 存储显示点击的ID和时间戳。 确定显示广告上的点击事件是否适用于Adobe Analytics点击。 |
| **`_tmae`** | 1 年 | 1 KB | `everesttech.net` | 使用DSP跟踪存储广告互动的编码ID和时间戳。 包含用户对广告的参与度，例如上次查看的广告 |
| **`_tmid`** | 1 年 | ~20 字节 | `everesttech.net` | 存储Adobe AdvertisingDemand Side Platform(DSP) ID。 对应于中的访客ID `everest_g_v2` Cookie。 |
| **`adcloud`** | 1 年 | 50-150字节 | 第一方 | 访客上次访问网站和上次搜索点击的时间戳。 同时存储 `ef_id` 这是访客点击广告时创建的。 将访客ID与相关受众区段和转化关联。 通过避免向Adobe发出不必要的请求，帮助优化页面加载时间。 |
| **`ev_sync_*`** |  | 8 字节 | `everesttech.net` | 在中执行同步的日期 `yyymmdd` 格式。 将Adobe Advertising访客ID与合作伙伴广告交换同步。 它是为新访客创建的，并在过期时发送同步请求。 包含Cookie `ev_sync_ax`， `ev_sync_bk`， `ev_sync_dd`， `ev_sync_fs`， `ev_sync_ix`， `ev_sync_nx`， `ev_sync_ox`， `ev_sync_pm`， `ev_sync_rc`， `ev_sync_tm`、和 `ev_sync_yh`. |
| **`everest_g_v2`** | 1 年 | ~27 字节 | `everesttech.net` | 存储浏览器和访客ID。 在用户最初单击广告后创建。 用于将当前点击和后续点击与您网站上的其他事件进行映射。 |
| **`everest_session_v2`** | 会话 | ~16 字节 | `everesttech.net` | 存储当前会话ID。 |
| **`id_adcloud`** | 91 天 | 16 字节 | 第一方 | 存储访客ID。 |

{style="table-layout:auto"}
