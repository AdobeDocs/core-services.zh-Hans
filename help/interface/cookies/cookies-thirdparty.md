---
description: 由于各种浏览器对第三方 Cookie 的支持越来越有限，Adobe 一直在着力开发新的解决方案，以期在各种 Adobe Experience Cloud 解决方案中实现客户需求与用户隐私权利的周密平衡。
keywords: cookies;隐私
seo-description: 由于各种浏览器对第三方 Cookie 的支持越来越有限，Adobe 一直在着力开发新的解决方案，以期在各种 Adobe Experience Cloud 解决方案中实现客户需求与用户隐私权利的周密平衡。
seo-title: 第三方 Cookie 支持的变化对客户有何影响
solution: Marketing Cloud,Analytics,Target,Social
title: 第三方 Cookie 支持的变化对客户有何影响
uuid: 27332e0d-6932-4a6e-b97b-0adeced0b050
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: f59badcd3423ada51a3fe0c605158a009d5b1d64

---


# 第三方 Cookie 支持的变化对客户有何影响{#how-changes-to-third-party-cookie-support-impacts-customers}

由于各种浏览器对第三方 Cookie 的支持越来越有限，Adobe 一直在着力开发新的解决方案，以期在各种 Adobe Experience Cloud 解决方案中实现客户需求与用户隐私权利的周密平衡。

下表列出了第三方 Cookie 支持对当前实施 Adobe Experience Cloud 解决方案的影响：

## Adobe Analytics 和 Adobe Target

* 采用[第一方实施](/help/interface/cookies/cookies-first-party.md)的客户基本上不会受影响。
* Customers that are not using first-party implementation can implement the [Experience Platform ID Service](https://docs.adobe.com/content/help/en/id-service/using/implementation-guides/implementation-guides.html) to store the ID cookie as a first-party cookie without a first-party implementation.

## Adobe Experience Manager

* 由于 Adobe Experience Manager 完全在客户的域内运行，与第三方 Cookie 的交互微乎其微，因此受到的影响很小，甚至毫无影响。

## Adobe Social

* 只要客户使用了最新版本的代码，Social 便不会受到影响。

## Adobe Advertising Cloud

* 搜索:

   * 由于搜索需要基于 Adobe Analytics 数据来优化，因此搜索会受到影响，此影响与 Adobe Analytics 受到的影响相同。
   * 转化数据收集应该不会受影响。

* 显示：

   * 目前显示再营销功能完全依赖于第三方 Cookie 的使用。
   * 显示功能在实现同步方面也高度依赖于各类广告网络 Cookie 的可用性。
   * 整体影响尚未可知。但是，根据第一点，对显示的影响会大于其他服务。
   * 关于对广告展示的最大影响，我们将在内部进行评估，同时还将与广告合作伙伴合作进行评估。

* Social：

   * 对 Facebook 市场广告没有任何影响。
   * Facebook Exchange (FBX) 会受到影响，此影响与对广告展示的影响相同。

