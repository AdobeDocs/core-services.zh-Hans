---
description: 了解对第三方 Cookie 的支持如何在各种浏览器中变得越来越有限。
keywords: cookies;隐私
solution: Experience Cloud,Analytics,Target
title: '第三方 Cookie 支持的变化对客户有何影响 '
uuid: 27332e0d-6932-4a6e-b97b-0adeced0b050
feature: Cookie
topic: 管理
role: 管理员
level: 富有经验
translation-type: tm+mt
source-git-commit: 61d60273e933c637dfe4400da78257e1c80015b3
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 99%

---


# 第三方 Cookie 支持的变化对客户有何影响{#how-changes-to-third-party-cookie-support-impacts-customers}

由于各种浏览器对第三方 Cookie 的支持越来越有限，Adobe 一直在着力开发新的解决方案，以期在各种 Adobe Experience Cloud 解决方案中实现客户需求与用户隐私权利的周密平衡。

下表列出了第三方 Cookie 支持对当前实施 Adobe Experience Cloud 解决方案的影响：

## Adobe Analytics 和 Adobe Target

* 采用[第一方实施](/help/interface/cookies/cookies-first-party.md)的客户基本上不会受影响。
* 未使用第一方实施的客户可实施 [Experience Platform ID 服务](https://docs.adobe.com/content/help/zh-Hans/id-service/using/implementation/implementation-guides.html)，将 ID Cookie 存储为不带第一方实施的第一方 Cookie。

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
   * 我们正在内部开展工作，并与广告合作伙伴合作，全面评估对广告投放的影响。

* Social：

   * 对 Facebook 市场广告没有影响。
   * Facebook Exchange (FBX) 受到的影响与展示广告投放受到的影响相同。
