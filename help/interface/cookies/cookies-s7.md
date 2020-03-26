---
description: Scene7 使用 Cookie 存储可用来将动态媒体传递到浏览器的有用信息。
keywords: cookies;privacy
seo-description: Scene7 使用 Cookie 存储可用来将动态媒体传递到浏览器的有用信息。
seo-title: Scene7 Cookie
solution: Marketing Cloud,Analytics,Adobe Target,Adobe Social
title: Scene7 Cookie
uuid: f9b9d13a-17e5-4139-8c84-6fe5d22c4196
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# Scene7 Cookie{#scene-cookies}

Scene7 使用 Cookie 存储可用来将动态媒体传递到浏览器的有用信息。

Scene7将一些基于AS2 Flash的旧查看器的信息存储在本地。

对于AS2查看器，Cookie:

* 跟踪用户的会话状态，如当前查看的页面和图像、当前缩放级别等。
* 确定自用户上一个会话以来已经有多长时间。 查看器使用此信息决定是否继续上一个会话或开始新会话。 此信息也会发送到Scene7服务器，但不会使用。

对于AS2 Flash eCatalog查看器，Cookie:

* 存储用户生成的内容（最明显的是用户在电子目录查看器的“附注”功能中输入的内容）。 当用户恢复会话时，此内容会恢复。
* 当用户发起电子邮件以与其他用户共享电子目录时，来自第二个AS2查看器项目符号的便签内容将复制到我们的服务器，以将其提供给收件人。 当收件人启动查看器会话时，将从服务器检索附注内容并将其复制到cookie。 此功能很少使用，因此不会过期且不会删除过时的内容。 此时，它会无限期地保留在服务器上。

较新的AS3查看器不实现会话持久性。

**Cookie 名称：VatLogin.jsp**

| 属性 | 描述 |
|---|---|
| 存储的信息 | 设置会话Cookie。 嵌入到IPS ImageServer(IS、IR以及SWF/外观和视频上下文)中的AuthFilter使用cookie进行访问授权。 如果存在，则允许HTTP请求通过。 否则，它将返回未授权。 |
| 过期 | 此Cookie是会话Cookie。 Scene7 IPS [!DNL web.xml] 中设置的当前会话到期为 45 分钟。 |

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
   <td colname="col2"> <p>&lt;assetId&gt;是查看器正在处理的资产的名称。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 过期 </td> 
   <td colname="col2"> 此Cookie是会话Cookie，在浏览器关闭时过期。 </td> 
  </tr> 
 </tbody> 
</table>

**Cookie 名称：s7js.flyout.InfoMessage.displayed`assetId`_idx`id`.ant**

传统DHTML查看器使用浏览器Cookie来存储状态信息和附注数据。 多屏幕DHTML弹出窗口还使用它们使消息指示符会话特定。

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
   <td colname="col2"> <p> </p> <p> &lt;assetId&gt;是查看器正在使用的资产名称，&lt;id&gt;是基于0的附注索引。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 过期 </td> 
   <td colname="col2"> 此Cookie是会话Cookie，在浏览器关闭时过期。 </td> 
  </tr> 
 </tbody> 
</table>

