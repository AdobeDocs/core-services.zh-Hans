---
description: Adobe Experience Cloud 使用 Cookie 来存储跨多个 Experience Cloud 解决方案使用的访客 ID。
keywords: cookies;privacy
seo-description: Adobe Experience Cloud 使用 Cookie 来存储跨多个 Experience Cloud 解决方案使用的访客 ID。
seo-title: Experience Cloud Cookies
solution: Experience Cloud,Analytics,Target
title: Experience Cloud Cookies
uuid: a4788c1c-0402-4fc8-b894-cd24fa794f4f
translation-type: tm+mt
source-git-commit: 7bd5b20d24d6ed1bcf2ea8cd1555af217013127e
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 100%

---


# Experience Cloud Cookies{#experience-cloud-cookies}

Adobe Experience Cloud 使用 Cookie 来存储跨多个 Experience Cloud 解决方案使用的访客 ID。

**Cookie 名称：s_ecid**

<table id="table_FF4C70D3D4CC425BA65162D5A9504F7D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>属性 </p> </th> 
   <th colname="col2" class="entry"> <p>描述 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>存储的信息 </p> </td> 
   <td colname="col2"> <p> 包含 Experience Cloud ID (ECID) 或 MID 的副本。MID 存储在一个键值对中，它遵循以下语法：s_ecid=MCMID|&lt;ECID&gt; </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 过期 </p> </td> 
   <td colname="col2"> <p>2 年 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 使用情况 </p> </td> 
   <td colname="col2"> <p>在客户端设置 AMCV Cookie 之后，此 Cookie 由客户的域设置。此 Cookie 的用途是允许在第一方状态中进行持久 ID 跟踪，并在 AMCV Cookie 过期时用作参考 ID。有关更多详细信息，请参阅此处的 AMCV Cookie。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 位置 </p> </td> 
   <td colname="col2"> <p>仅限 CNAME 客户。不适用于第三方场景。Cookie 存储在您的域中，该域与 CNAME 和 Analytics 图像请求使用的域相同。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 大小 </p> </td> 
   <td colname="col2"> <p>45 字节 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> SameSite=Lax </p> </td> 
   <td colname="col2"> <p>仅当浏览器 URL 中显示的域与 Cookie 的域匹配时，才发送具有此设置的 Cookie。这是 Chrome 中新增的 Cookie 默认设置。</p> </td> 
  </tr> 
 </tbody> 
</table>

**Cookie 名称：AMCV_###@AdobeOrg**

[Experience Platform ID 服务](https://docs.adobe.com/content/help/zh-Hans/id-service/using/home.html)可使用 JavaScript 在当前网站的域上的 `AMCV_###@AdobeOrg` Cookie 中，存储一个独特访客 ID，其中 `###` 代表一个随机的字符串，例如 `AMCV_1FD6776A524453CC0A490D44%40AdobeOrg.`。

另请参阅 [Cookie 和 ID 服务](https://docs.adobe.com/content/help/zh-Hans/id-service/using/intro/cookies.html)。

<table id="table_1883C0836C1E4AF5A262FBF5000C1B11"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>属性 </p> </th> 
   <th colname="col2" class="entry"> <p>描述 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>存储的信息 </p> </td> 
   <td colname="col2"> <p> Experience Cloud 解决方案使用的独特访客 ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 过期 </p> </td> 
   <td colname="col2"> <p> 2 年 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 使用情况 </p> </td> 
   <td colname="col2"> <p> 此 Cookie 用于标识独特访客 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 位置 </p> </td> 
   <td colname="col2"> <p> 此 Cookie 存储在网站的域（而非图像请求的域）中。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 大小 </p> </td> 
   <td colname="col2"> <p> 各不相同，大多数客户可能希望此 Cookie 的长度在 200 字节左右。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>没有添加任何值。Chrome 将默认设置为 Lax。 </p> </td> 
   <td colname="col2"> <p> 仅当浏览器 URL 中显示的域与 Cookie 的域匹配时，才发送具有此设置的 Cookie。这是 Chrome 中新增的 Cookie 默认设置。 </p> </td> 
  </tr> 
 </tbody> 
</table>
