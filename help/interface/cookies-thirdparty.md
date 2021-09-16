---
description: 了解对第三方 Cookie 的支持如何在各种浏览器中变得越来越有限。
keywords: cookies;隐私
solution: Experience Cloud,Analytics,Target
title: '第三方 Cookie 支持的变化对客户有何影响 '
uuid: 27332e0d-6932-4a6e-b97b-0adeced0b050
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 3d12a1b1-c952-4b42-815d-f64b31429cec
source-git-commit: 1fb1abc7311573f976f7e6b6ae67f60ada10a3e7
workflow-type: ht
source-wordcount: '265'
ht-degree: 100%

---

# 第三方 Cookie 支持的变化对客户有何影响{#how-changes-to-third-party-cookie-support-impacts-customers}

对第三方 Cookie 的支持在各种浏览器中变得日益有限。因此，Adobe 一直致力于开发全新解决方案，在客户需求与客户的隐私权力之间进行认真权衡以打造 Experience Cloud 应用程序。

下表列出了第三方 Cookie 支持对当前实施 Experience Cloud 应用程序的影响：

## Adobe Analytics 和 Adobe Target

* Analytics 和 Target 在很大程度上不受影响，因为相同的站点活动仅依赖于第一方 Cookie。需要第三方 Cookie 来了解跨域的用户活动。对于阻止第三方 Cookie 的浏览器，无法使用 Cookie 进行跨域跟踪。

## Adobe Experience Manager

* 由于 Adobe Experience Manager 完全在客户的域内运行，与第三方 Cookie 的交互微乎其微，因此受到的影响很小，甚至毫无影响。

## Adobe Social

* 只要客户使用了最新版本的代码，Social 便不会受到影响。

## Adobe Advertising Cloud

* 搜索:

   * 这里的搜索根据 Adobe Analytics 数据进行了优化，因此搜索受到的影响与 Adobe Analytics 一样。
   * 转化数据的收集不应受到影响。

* 显示:

   * 现在的显示重新营销完全取决于第三方 Cookie 的使用情况。
   * 显示是否同步在很大程度上还取决于各种广告网络 Cookie 的可用性。
   * 整体影响尚未可知。但是，对于第一点，显示受到的影响要高于其他服务受到的影响。
   * Adobe 正在内部开展工作，并与 Adobe 的广告合作伙伴合作，全面评估对广告投放的影响。
