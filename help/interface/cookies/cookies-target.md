---
description: 了解 Adobe Target 如何使用 Cookie，以便让网站运营者能够测试哪些在线内容和选件与访客更相关。
keywords: cookies;隐私
solution: Experience Cloud,Analytics,Target,Social
title: 'Adobe Target Cookie '
uuid: 44f7e32e-8d99-4682-8b54-8364d001b403
feature: Cookie
topic: 管理
role: 管理员
level: 富有经验
translation-type: tm+mt
source-git-commit: 61d60273e933c637dfe4400da78257e1c80015b3
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 99%

---


# Adobe Target Cookie{#target-cookies}

Adobe Target 使用 Cookie 让网站运营者能够测试哪些在线内容和选件与访客更相关。

除 Cookie 持续时间外，您可以根据需要更改这些设置。更改 Cookie 设置时，请咨询您的客户代表。

>[!NOTE]
>
>Adobe Target 用户还可以创建自定义的第三方 Cookie。

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
   <td colname="col2"> <p> <span class="filepath">clientcode.tt.omtrdc.net</span>，使用 Adobe Target 帐户的客户代码。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Cookie 持续时间 </p> </td> 
   <td colname="col2"> <p>自访客上次登录起，Cookie 在访客的浏览器中保留两年。无法更改 Cookie 持续时间。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>如果您的任何域名包括国家/地区代码（如 [!DNL mycompany.co.uk]），请咨询客户服务部门来配置您的 [!DNL mbox.js] 以支持此功能。

Cookie 会保留大量值以管理访客对 Adobe Target 促销活动的体验：

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
   <td colname="col2"> <p>用户会话的唯一 ID。默认情况下，该值持续 30 小时。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> pc ID</span> </p> </td> 
   <td colname="col2"> <p>访客浏览器的半永久 ID。持续存在，直到手动删除 Cookie 为止。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> check</span> </p> </td> 
   <td colname="col2"> <p>用于确定访客是否支持 Cookie 的简单测试值。在每次访客请求页面时设置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> disable</span> </p> </td> 
   <td colname="col2"> <p>如果访客的加载时间超过了 <span class="filepath">mbox.js</span> 文件中设置的超时值，则进行设置。默认情况下，该设置持续 1 小时。 </p> </td> 
  </tr> 
 </tbody> 
</table>

