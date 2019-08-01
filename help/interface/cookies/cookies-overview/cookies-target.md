---
description: Target 使用 Cookie 让网站运营者能够测试哪些在线内容和选件与访客更相关。
keywords: cookies；隐私权
seo-description: Target 使用 Cookie 让网站运营者能够测试哪些在线内容和选件与访客更相关。
seo-title: Target Cookie
solution: Marketing Cloud、Analytics、Target、Social
title: Target Cookie
uuid: 44f7e32e-8d99-4682-8b54-8364d001b403
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: c1630f5de61e410eaf10cf940faa9adc6017fb6b

---


# Target Cookie{#target-cookies}

Target 使用 Cookie 让网站运营者能够测试哪些在线内容和选件与访客更相关。

您可以根据需要更改这些设置，但 Cookie 持续时间除外。更改 Cookie 设置时可咨询您的客服专员。

>[!NOTE]
>
>目标用户还可以创建自定义的第三方cookie。

<table id="table_54B402C6E19C4A70B1E27BC9DFF776EB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 设置 </th> 
   <th colname="col2" class="entry"> 信息 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Cookie 名称 </p> </td> 
   <td colname="col2"> <p>mbox。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Cookie 域 </p> </td> 
   <td colname="col2"> <p>提供 mbox 的二级域和顶级域。由于这是来自您的公司域，所以此 Cookie 是第一方 Cookie。示例：<span class="filepath">mycompany.com</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>服务器域 </p> </td> 
   <td colname="col2"> <p> <span class="filepath">clientcode.tt.omtrdc.net</span>，使用 Target 帐户的客户代码。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Cookie 持续时间 </p> </td> 
   <td colname="col2"> <p>从访客最后一次登录的时间算起，Cookie 将在访客浏览器中保留两个星期。您不能更改 Cookie 持续时间。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>If any of your domain names include a country code, such as [!DNL mycompany.co.uk], work with your Client Services to configure your [!DNL mbox.js] to support this.

此 Cookie 保存一系列值，以控制您的访客体验 Target 营销活动的方式：

<table id="table_5245F72A2D5A4322B40ABB10B7DFB338"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 值 </th> 
   <th colname="col2" class="entry"> 定义 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> session ID</span> </p> </td> 
   <td colname="col2"> <p>用户会话的唯一 ID。默认情况下，该 ID 持续 30 分钟。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> pc ID</span> </p> </td> 
   <td colname="col2"> <p>访客浏览器的半永久性 ID。持续到 Cookie 被手动删除为止。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> check</span> </p> </td> 
   <td colname="col2"> <p>用来确定访客是否支持 Cookie 的简单测试值。每次用户请求页面时设置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> disable</span> </p> </td> 
   <td colname="col2"> <p>如果访客的加载时间超过了 <span class="filepath">mbox.js</span> 文件中设置的超时值，则进行设置。默认情况下，该设置持续 1 小时。 </p> </td> 
  </tr> 
 </tbody> 
</table>

