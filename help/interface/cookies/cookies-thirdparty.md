---
description: 由于各种浏览器对第三方 Cookie 的支持越来越有限，Adobe 一直在着力开发新的解决方案，以期在各种 Adobe Experience Cloud 解决方案中实现客户需求与用户隐私权利的周密平衡。
keywords: cookies;privacy
seo-description: 由于各种浏览器对第三方 Cookie 的支持越来越有限，Adobe 一直在着力开发新的解决方案，以期在各种 Adobe Experience Cloud 解决方案中实现客户需求与用户隐私权利的周密平衡。
seo-title: 第三方 Cookie 支持的变化对客户有何影响
solution: Marketing Cloud,Analytics,Adobe Target,Adobe Social
title: 第三方 Cookie 支持的变化对客户有何影响
uuid: 27332e0d-6932-4a6e-b97b-0adeced0b050
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# How changes to third-party cookie support impact customers{#how-changes-to-third-party-cookie-support-impacts-customers}

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

   * 如果根据Adobe Analytics数据优化搜索，则搜索将受到与Adobe Analytics相同的影响。
   * 转换数据的收集应不受影响。

* 显示:

   * 现在的展示广告再营销完全取决于第三方cookie的使用。
   * 显示屏还严重依赖于各种广告网络cookie的可用性以进行同步。
   * 整体影响未知。 但是，对于第一点，显示受到的影响比其他服务要大。
   * 我们正与我们的广告合作伙伴进行内部合作，以评估广告投放所受的影响。

* Social：

   * 对Facebook市场广告没有影响。
   * Facebook Exchange(FBX)将与展示广告投放一样受到影响。
