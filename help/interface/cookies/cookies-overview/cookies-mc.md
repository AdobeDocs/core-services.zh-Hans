---
description: Adobe Experience Cloud 使用 Cookie 来存储跨多个 Experience Cloud 解决方案使用的访客 ID。
keywords: cookies;隐私
seo-description: Adobe Experience Cloud 使用 Cookie 来存储跨多个 Experience Cloud 解决方案使用的访客 ID。
seo-title: Experience Cloud Cookies
solution: Marketing Cloud,Analytics,Target,Social
title: Experience Cloud Cookies
uuid: a4788c1c-0402-4fc8-b894-cd24fa794f4f
index: y
internal: n
snippet: y
translation-type: ht
source-git-commit: c1630f5de61e410eaf10cf940faa9adc6017fb6b

---


# Experience Cloud Cookies{#experience-cloud-cookies}

Adobe Experience Cloud 使用 Cookie 来存储跨多个 Experience Cloud 解决方案使用的访客 ID。

* [Cookie 名称：s_ecid](../cookies-overview/cookies-mc.md#section-32fd753c3fa54452acd62b021434919a)
* [Cookie 名称：AMCV_###@AdobeOrg](../cookies-overview/cookies-mc.md#section-a12aa2a9296940ae82d8921b381b8fb0)

## Cookie 名称：s_ecid {#section-32fd753c3fa54452acd62b021434919a}

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
 </tbody> 
</table>

## Cookie 名称：AMCV_###@AdobeOrg {#section-a12aa2a9296940ae82d8921b381b8fb0}

[访客 ID 服务](https://marketing.adobe.com/resources/help/zh_CN/mcvid/)使用 JavaScript 在当前网站的域上的 `AMCV_###@AdobeOrg` Cookie 中存储一个唯一的访客 ID，其中 `###` 代表一个随机的字符串。例如：`AMCV_1FD6776A524453CC0A490D44%40AdobeOrg`。另请参阅 [Cookie 和 ID 服务](https://marketing.adobe.com/resources/help/zh_CN/mcvid/mcvid_cookies.html)。

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
   <td colname="col2"> <p> 此 Cookie 用于识别独特访客 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 位置 </p> </td> 
   <td colname="col2"> <p> 此 Cookie 存储在网站的域中（并非图像请求的域中）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 大小 </p> </td> 
   <td colname="col2"> <p> 不固定，此 Cookie 的长度通常在 200 字节左右。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!MORE_LIKE_THIS]
>
>* [Cookie 和 ID 服务](https://marketing.adobe.com/resources/help/zh_CN/mcvid/mcvid_cookies.html)

