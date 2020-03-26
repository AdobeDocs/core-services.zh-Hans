---
description: Target 使用 Cookie 让网站运营者能够测试哪些在线内容和选件与访客更相关。
keywords: cookies;privacy
seo-description: Target 使用 Cookie 让网站运营者能够测试哪些在线内容和选件与访客更相关。
seo-title: Target Cookie
solution: Marketing Cloud,Analytics,Target,Social
title: Target Cookie
uuid: 44f7e32e-8d99-4682-8b54-8364d001b403
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# Adobe Target Cookies{#target-cookies}

Adobe目标使用cookies使网站运营商能够测试哪些在线内容和优惠与访客更相关。

您可以根据需要更改这些设置，但cookie持续时间除外。 更改Cookie设置时，请咨询您的客户代表。

>[!NOTE]
>
>Adobe目标用户还可以创建自定义的第三方Cookie。

<table id="table_54B402C6E19C4A70B1E27BC9DFF776EB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 设置 </th> 
   <th colname="col2" class="entry"> 信息 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Cookie名称 </p> </td> 
   <td colname="col2"> <p>mbox。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Cookie域 </p> </td> 
   <td colname="col2"> <p>您提供mbox的域的二级和顶级。 由于这是来自您的公司域，所以此 Cookie 是第一方 Cookie。示例：<span class="filepath">mycompany.com</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>服务器域 </p> </td> 
   <td colname="col2"> <p> <span class="filepath"> clientcode.tt.omtrdc.net</span>，使用Adobe目标帐户的客户端代码。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Cookie持续时间 </p> </td> 
   <td colname="col2"> <p>Cookie将保留在访客的浏览器上，距上次登录两年后。 您无法更改Cookie持续时间。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>如果您的任何域名包括国家/地区代码（如 [!DNL mycompany.co.uk]），请咨询客户服务部门来配置您的 [!DNL mbox.js] 以支持此功能。

Cookie保留许多值，以管理您的访客体验Adobe目标活动的方式：

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
   <td colname="col2"> <p>用户会话的唯一ID。 默认情况下，此时间为30分钟。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> pc ID</span> </p> </td> 
   <td colname="col2"> <p>访客浏览器的半永久ID。 在手动删除Cookie之前一直有效。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> check</span> </p> </td> 
   <td colname="col2"> <p>用于确定访客是否支持cookie的简单测试值。 每次访客请求页面时设置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> disable</span> </p> </td> 
   <td colname="col2"> <p>如果访客的加载时间超过了 <span class="filepath">mbox.js</span> 文件中设置的超时值，则进行设置。默认情况下，该设置持续 1 小时。 </p> </td> 
  </tr> 
 </tbody> 
</table>

