---
description: Scene7 使用 Cookie 存储可用来将动态媒体传递到浏览器的有用信息。
keywords: cookies;隐私
seo-description: Scene7 使用 Cookie 存储可用来将动态媒体传递到浏览器的有用信息。
seo-title: Scene7 Cookie
solution: Marketing Cloud,Analytics,Target,Social
title: Scene7 Cookie
uuid: f9b9d13a-17e5-4139-8c84-6fe5d22c4196
index: y
internal: n
snippet: y
translation-type: ht
source-git-commit: c1630f5de61e410eaf10cf940faa9adc6017fb6b

---


# Scene7 Cookie{#scene-cookies}

Scene7 使用 Cookie 存储可用来将动态媒体传递到浏览器的有用信息。

Scene7 将信息存储在本地，以便通过一些较旧版本的 AS2 Flash 查看器查看。

对于 AS2 查看器，Cookie：

* 跟踪用户的会话状态，例如，查看的当前页面和图像、当前缩放水平，等等。
* 确定距离上次用户会话的时间。查看器利用此信息决定是继续上一会话，还是启动新会话。此信息还会被发送到 Scene7 服务器，但是服务器不会使用此信息。

对于 AS2 Flash eCatalog 查看器，Cookie：

* 存储用户生成的内容（尤其是用户在 ecatalog 查看器的“便笺”功能中输入的内容）。当用户继续某个会话时会还原此内容。
* 当用户发起与其他用户共享 ecatalog 的电子邮件时，系统会将 AS2 查看器的第二个项目符号对应的便笺内容复制到我们的服务器，以将其提供给收件人。当收件人发起查看器会话时，系统会从服务器中检索便笺内容，并将其复制到 Cookie。此功能很少使用，因此它不会过期，系统也不会删除其旧内容。目前，此功能可在服务器上无限期地存在，永久有效。

较新版本的 AS3 查看器不会实施会话持久性。

* [Cookie 名称：VatLogin.jsp](../cookies-overview/cookies-s7.md#section-03aa90aa7e36427b8cb12dc4a0f0291e)
* [Cookie 名称：s7js.flyout.InfoMessage.displayed.state](../cookies-overview/cookies-s7.md#section-14ad50dfcd7342f9ac80283b1f0d3400)
* [Cookie 名称：s7js.flyout.InfoMessage.displayed_idx.ant](../cookies-overview/cookies-s7.md#section-05d1c52c478541609f4a18a9c1eb032f)

## Cookie 名称：VatLogin.jsp {#section-03aa90aa7e36427b8cb12dc4a0f0291e}

| 属性 | 描述 |
|---|---|
| 存储的信息 | 设置会话 Cookie。嵌入 IPS ImageServer（IS、IR 还有 SWF/皮肤和视频上下文）中的 AuthFilter 使用 Cookie 获取访问授权。如果存在，它将允许 HTTP 请求通过。否则，它会返回未授权访问。 |
| 过期 | 此 Cookie 是会话 Cookie。Scene7 IPS [!DNL web.xml] 中设置的当前会话到期为 45 分钟。 |

## Cookie 名称：s7js.flyout.InfoMessage.displayed<assetId>.state {#section-14ad50dfcd7342f9ac80283b1f0d3400}

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
   <td colname="col2"> <p>&lt;assetId&gt; 是查看器正在使用的资源名称。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 过期 </td> 
   <td colname="col2"> 此 Cookie 是会话 Cookie，关闭浏览器之后即到期。 </td> 
  </tr> 
 </tbody> 
</table>

## Cookie 名称：s7js.flyout.InfoMessage.displayed<assetId>_idx<id>.ant {#section-05d1c52c478541609f4a18a9c1eb032f}

旧的 DHTML 查看器使用浏览器 Cookie 来存储状态信息和便笺数据。多屏幕 DHTML 弹出式屏幕还会使用它们来将消息指示器特定于会话。

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
   <td colname="col2"> <p> </p> <p> &lt;assetId&gt; 是查看器正在使用的资源名称，&lt;id&gt; 是基于 0 的便笺索引。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 过期 </td> 
   <td colname="col2"> 此 Cookie 是会话 Cookie，关闭浏览器之后即到期。 </td> 
  </tr> 
 </tbody> 
</table>

