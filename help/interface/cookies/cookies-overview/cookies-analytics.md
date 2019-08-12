---
description: Adobe Analytics 使用 Cookie 区分来自不同浏览器的请求，并存储应用程序将来可使用的有用信息。这些 Cookie 还可以用来将浏览信息与客户记录相关联。
keywords: cookies;隐私
seo-description: Adobe Analytics 使用 Cookie 区分来自不同浏览器的请求，并存储应用程序将来可使用的有用信息。这些 Cookie 还可以用来将浏览信息与客户记录相关联。
seo-title: Analytics Cookie
solution: Marketing Cloud,Analytics,Target,Social
title: Analytics Cookie
uuid: e2d3d61d-2708-48b2-a7e6-2331f2aed8e0
index: y
internal: n
snippet: y
translation-type: ht
source-git-commit: c1630f5de61e410eaf10cf940faa9adc6017fb6b

---


# Analytics Cookie{#analytics-cookies}

Adobe Analytics 使用 Cookie 区分来自不同浏览器的请求，并存储应用程序将来可使用的有用信息。这些 Cookie 还可以用来将浏览信息与客户记录相关联。

具体来说，Analytics 可通过 Cookie 以匿名方式定义新访客、协助分析点击流数据，并跟踪网站上的历史活动，如针对特定促销活动的响应或销售周期的长度。

* [Cookie 名称：s_ecid](../cookies-overview/cookies-mc.md#section-32fd753c3fa54452acd62b021434919a)
* [Cookie 名称：AMCV_###@AdobeOrg](../cookies-overview/cookies-mc.md#section-a12aa2a9296940ae82d8921b381b8fb0)
* [Cookie 名称：s_cc](../cookies-overview/cookies-analytics.md#section-03aa90aa7e36427b8cb12dc4a0f0291e)
* [Cookie 名称：s_cc](../cookies-overview/cookies-analytics.md#section-03aa90aa7e36427b8cb12dc4a0f0291e)
* [Cookie 名称：s_sq](../cookies-overview/cookies-analytics.md#section-8abfff3a302d494f81a3cfb91e3b09ff)
* [Cookie 名称：s_vi](../cookies-overview/cookies-analytics.md#section-5d50a078de444d12b7d927d68ff3b679)
* [Cookie 名称：s_fid](../cookies-overview/cookies-analytics.md#section-65e33f9bfc264959ac1513e2f4b10ac7)
* [插件设置的 Cookie](../cookies-overview/cookies-analytics.md#section-a6b1cae8454945fab9eea5c7884c40fc)

更多信息可在有关[第一方 Cookie](https://marketing.adobe.com/resources/help/en_US/whitepapers/first_party_cookies/fpcookies_overview.html) 的 Analytics 帮助文档中找到。

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

## Cookie 名称：s_cc {#section-03aa90aa7e36427b8cb12dc4a0f0291e}

<table id="table_34AA90F2FFB84500A77D8F4C5008D453"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>属性 </p> </th> 
   <th colname="col2" class="entry"> <p>描述 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>存储的信息 </p> </td> 
   <td colname="col2"> <p> 该 Cookie 通过 JavaScript 代码设置和读取，用于确定是否启用了 Cookie（只需设为“True”） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 过期 </p> </td> 
   <td colname="col2"> <p> 此 Cookie 是会话 Cookie，关闭浏览器之后即到期 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 使用情况 </p> </td> 
   <td colname="col2"> <p> 所有帐户只有一个 Cookie </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 位置 </p> </td> 
   <td colname="col2"> <p> 此 Cookie 存储在页面的域中 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 大小 </p> </td> 
   <td colname="col2"> <p> 4 字节 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cookie 名称：s_sq {#section-8abfff3a302d494f81a3cfb91e3b09ff}

<table id="table_05EEB54B5EA2409DB1D071FD1484E8F9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>属性 </p> </th> 
   <th colname="col2" class="entry"> <p>描述 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>存储的信息 </p> </td> 
   <td colname="col2"> <p> 在启用 ClickMap 功能和 Activity Map 功能后，将通过 JavaScript 代码设置并读取该 Cookie；它包含用户上一次点击的链接的相关信息 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 过期 </p> </td> 
   <td colname="col2"> <p> 此 Cookie 是会话 Cookie，关闭浏览器之后即到期 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 使用情况 </p> </td> 
   <td colname="col2"> <p> 所有帐户只有一个 Cookie </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 位置 </p> </td> 
   <td colname="col2"> <p> 此 Cookie 存储在页面的域中 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 大小 </p> </td> 
   <td colname="col2"> <p> 因页面 URL 大小而异，但通常为 100-200 字节 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cookie 名称：s_vi {#section-5d50a078de444d12b7d927d68ff3b679}

<table id="table_774F04AA9E3847D9AE7803520B5AAAE3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>属性 </p> </th> 
   <th colname="col2" class="entry"> <p>描述 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>存储的信息 </p> </td> 
   <td colname="col2"> <p> 独特访客 ID 时间/日期戳记 </p> </td> 
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
   <td colname="col2"> <p> 此 Cookie 存储在图像请求的域（如果您使用的是第三方 Cookie，通常为 2O7.net）或您的域（如果您使用的是第一方 Cookie）中。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 大小 </p> </td> 
   <td colname="col2"> <p> 44 字节 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>每个 Analytics 访客 ID 均与 Adobe 服务器上的一个访客资料关联。访客资料在处于 1 年的非活动状态之后会被删除，这与任何访客 ID Cookie 过期日期无关。

## Cookie 名称：s_fid {#section-65e33f9bfc264959ac1513e2f4b10ac7}

<table id="table_B0EDB50677D14A86A1BFB7CCAAE95C88"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>属性 </p> </th> 
   <th colname="col2" class="entry"> <p>描述 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>存储的信息 </p> </td> 
   <td colname="col2"> <p> 回退独特访客 ID 时间戳/日期戳 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 过期 </p> </td> 
   <td colname="col2"> <p>5 年 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 使用情况 </p> </td> 
   <td colname="col2"> <p> 如果由于受第三方 Cookie 限制标准的 <span class="codeph">s_vi</span> Cookie 不可用，将使用此 Cookie 来识别独特访客。在使用第一方 Cookie 的实施中不会使用此 Cookie。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 位置 </p> </td> 
   <td colname="col2"> <p> 此 Cookie 作为第一方 Cookie 存储在您的域中。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 大小 </p> </td> 
   <td colname="col2"> <p> 33 字节 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 插件设置的 Cookie {#section-a6b1cae8454945fab9eea5c7884c40fc}

其他 Cookie 可根据 Analytics 插件的使用情况来设置。这些 Cookie 是提供给客户端的代码段，可用在各种环境中。这些环境包括：从 URL 检索值、连接要传递到 Analytics 的值、捕获表单放弃等。有关每个插件所设置的 Cookie 的特定信息，请与 ClientCare 联系。例如，[!DNL s_vh]Set Once Per *和* Set and Get Last Value *插件使用* Cookie。

仅当电子邮件和浏览器共享相同的 Cookie 空间时，才能正确识别未使用 JavaScript 而传入图像请求的 Conversion 变量 (eVarX)，例如置入电子邮件内的代码。
