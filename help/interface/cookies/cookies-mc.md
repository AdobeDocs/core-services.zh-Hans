---
description: Adobe Experience Cloud 使用 Cookie 来存储跨多个 Experience Cloud 解决方案使用的访客 ID。
keywords: cookies;privacy
seo-description: Adobe Experience Cloud 使用 Cookie 来存储跨多个 Experience Cloud 解决方案使用的访客 ID。
seo-title: Experience Cloud Cookies
solution: Marketing Cloud,Analytics,Adobe Target,Adobe Social
title: Experience Cloud Cookies
uuid: a4788c1c-0402-4fc8-b894-cd24fa794f4f
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

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
   <td colname="col2"> <p>2年 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 使用情况 </p> </td> 
   <td colname="col2"> <p>在客户端设置 AMCV Cookie 之后，此 Cookie 由客户的域设置。此Cookie的用途是在第一方状态中允许持续的ID跟踪，并在AMCV Cookie过期时用作参考ID。 有关更多详细信息，请参阅此处的 AMCV Cookie。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 位置 </p> </td> 
   <td colname="col2"> <p>仅限 CNAME 客户。不适用于第三方场景。Cookie 存储在您的域中，该域与 CNAME 和 Analytics 图像请求使用的域相同。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 大小 </p> </td> 
   <td colname="col2"> <p>45 字节 </p> </td> 
  </tr> 
 </tbody> 
</table>

**Cookie 名称：AMCV_###@AdobeOrg**

[Experience Platform ID服务使用JavaScript将唯一的访客ID存储在当前网站域的](https://docs.adobe.com/content/help/en/id-service/using/home.html) cookie中，其中 `AMCV_###@AdobeOrg``###` 表示随机字符串，如 `AMCV_1FD6776A524453CC0A490D44%40AdobeOrg.`

See also, [Cookies and the ID Service](https://docs.adobe.com/content/help/en/id-service/using/intro/cookies.html).

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
   <td colname="col2"> <p> Experience Cloud解决方案使用的唯一访客ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 过期 </p> </td> 
   <td colname="col2"> <p> 2年 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 使用情况 </p> </td> 
   <td colname="col2"> <p> 此Cookie用于标识唯一访客 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 位置 </p> </td> 
   <td colname="col2"> <p> 此Cookie存储在网站的域（而非图像请求的域）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 大小 </p> </td> 
   <td colname="col2"> <p> 因此，大多数客户可能希望此Cookie的长度约为200字节。 </p> </td> 
  </tr> 
 </tbody> 
</table>
