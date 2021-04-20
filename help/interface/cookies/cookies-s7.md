---
description: Adobe Scene7 如何使用 Cookie 存储可用来将动态媒体传递到浏览器的有用信息。
keywords: cookies;隐私
solution: Experience Cloud,Analytics,Target
title: 'Scene7 Cookie '
uuid: f9b9d13a-17e5-4139-8c84-6fe5d22c4196
feature: Cookies
topic: Administration
role: Administrator
level: Experienced
translation-type: ht
source-git-commit: 61d60273e933c637dfe4400da78257e1c80015b3
workflow-type: ht
source-wordcount: '417'
ht-degree: 100%

---


# Scene7 Cookie{#scene-cookies}

Scene7 使用 Cookie 存储可用来将动态媒体传递到浏览器的有用信息。

Scene7 会在本地存储一些基于旧版 AS2 Flash 的查看器的信息。

对于 AS2 查看器，Cookie 能够：

* 跟踪用户的会话状态，如当前页面和已查看的图像、当前缩放级别等。
* 确定自用户的上一个会话以来已经过的时间。查看器使用此信息来决定是继续上一个会话还是启动一个新的会话。此信息也会发送到 Scene7 服务器，但不会被使用。

对于 AS2 Flash eCatalog 查看器，Cookie 能够：

* 存储用户生成的内容（主要是用户在 ecatalog 查看器的“附注”功能中输入的内容）。当用户继续某个会话时，此内容会恢复。
* 当用户发起电子邮件以与其他用户共享 ecatalog 时，系统会将来自第二个 AS2 查看器项目符号的附注内容复制到我们的服务器中，以提供给收件人。当收件人启动查看器会话时，将从服务器检索附注内容并将该内容复制到 Cookie。此功能很少使用，因此不会过期，也不会删除旧内容。此时，它将无限期地保留在服务器上。

新版的 AS3 查看器不实施会话持久性。

**Cookie 名称：VatLogin.jsp**

| 属性 | 描述 |
|---|---|
| 存储的信息 | 设置会话 Cookie。嵌入到 IPS ImageServer（IS、IR 以及 SWF/皮肤和视频上下文）中的 AuthFilter 可使用 Cookie 获取访问授权。如果存在，则允许 HTTP 请求通过。否则，它将显示未授权。 |
| 过期 | 此 Cookie 是会话 Cookie。Scene7 IPS [!DNL web.xml] 中设置的当前会话到期为 45 分钟。 |

**Cookie 名称：s7js.flyout.InfoMessage.displayed`assetId`.state**

<table id="table_6835D64C5D464A049F576621F2BE3FAD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 属性 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 存储的信息 </td> 
   <td colname="col2"> <p>&lt;assetId&gt; 是查看器正在处理的资产的名称。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 过期 </td> 
   <td colname="col2"> 此 Cookie 是会话 Cookie，在浏览器关闭时过期。 </td> 
  </tr> 
 </tbody> 
</table>

**Cookie 名称：s7js.flyout.InfoMessage.displayed`assetId`_idx`id`.ant**

旧版 DHTML 查看器使用浏览器 Cookie 来存储状态信息和附注数据。多屏幕 DHTML 弹出窗口还使用这些 Cookie 使消息指示符特定于会话。

<table id="table_8F6CC83D32D54BEE99884318AD126C98"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 属性 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 存储的信息 </td> 
   <td colname="col2"> <p> </p> <p> &lt;assetId&gt; 是查看器正在处理的资产名称，&lt;id&gt; 是基于 0 的附注索引。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 过期 </td> 
   <td colname="col2"> 此 Cookie 是会话 Cookie，在浏览器关闭时过期。 </td> 
  </tr> 
 </tbody> 
</table>

