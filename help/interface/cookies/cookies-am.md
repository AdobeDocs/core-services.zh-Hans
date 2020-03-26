---
description: 受众管理器依赖一些简单的cookie来执行不同的功能。 这些包括指定ID、记录数据调用、错误跟踪和测试，以查看是否可以设置Cookie。 本节列表并描述由受众管理器设置的各种Cookie。
keywords: cookies
seo-description: 受众管理器依赖一些简单的cookie来执行不同的功能。 这些包括指定ID、记录数据调用、错误跟踪和测试，以查看是否可以设置Cookie。 本节列表并描述由受众管理器设置的各种Cookie。
seo-title: Audience Manager Cookie
solution: Marketing Cloud,Audience Manager
title: Audience Manager Cookie
uuid: 8b384c38-b85a-4e93-b00e-41a9d3ae2b21
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# Audience Manager Cookie{#audience-manager-cookies}

受众管理器依赖一些简单的cookie来执行不同的功能。 这些包括指定ID、记录数据调用、错误跟踪和测试，以查看是否可以设置Cookie。 本节列表并描述由受众管理器设置的各种Cookie。

**demdex Cookie**

<table id="table_1CCF7EA2BC9E421F8DEECA5F611E33F6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 属性 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>用途</b> </p> </td> 
   <td colname="col2"> <p> <span class="keyword">Audience Manager</span> 通过设置此 Cookie 来向站点访客分配独特的 ID。<span class="wintitle">demdex</span> Cookie 可帮助 <span class="keyword">Audience Manger</span> 执行基本的功能，例如访客识别、ID 同步、分段、建模和报告等。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>内容</b> </p> </td> 
   <td colname="col2"> <p><span class="wintitle">demdex</span> Cookie 包含唯一用户 ID (UUID)，如下面的示例所示： </p> <p> <span class="codeph"> 06151304227769720433039235178204449977 </span> </p> <p>另请参阅 <a href="https://docs.adobe.com/content/help/en/audience-manager/user-guide/reference/ids-in-aam.html" format="https" scope="external">Audience Manager 中的 ID 索引</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>其他属性</b> </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_11291DA87C5045E880034E06C863BCDA"> 
      <li id="li_40C30A06A12449A4A8748621223CA71B">存留期：<span class="wintitle">demdex</span> Cookie 的生存时间 (TTL) 间隔为 180 天。每次用户与合作伙伴网站交互时，TTL将重置为180天。 如果用户在TTL间隔内没有返回到您的站点，则Cookie将过期。 </li> 
      <li id="li_A589EDA2198249829207A183872EF1FF">Opt-out: <span class="keyword"> Audience Manager </span> resets the cookie with a <span class="codeph"> Do Not Adobe Target </span> string if a user opts-out of data collection. 在这种情况下，Cookie TTL 被设置为 10 年。 </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**dextp Cookie**

<table id="table_7343C9C9ADD24D3FA693ECC76E4A4045"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 属性 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>用途</b> </p> </td> 
   <td colname="col2"> <p> <span class="keyword">Audience Manager</span> 通过设置此 Cookie 来记录其上次执行数据同步调用的情况。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>内容</b> </p> </td> 
   <td colname="col2"> <p><span class="wintitle">dextp</span> Cookie 包含数据提供程序的名称或 ID 及 UNIX UTC 时间戳，格式为用竖线分隔的字符串。在下面的示例中，<i>斜体</i>表示变量占位符。 </p> <p> 
     <ul id="ul_80D0BC3FCF06470991E12712401D784A"> 
      <li id="li_03747A433CEB4756A26CD866E716B89D">旧样式：<span class="codeph"><span class="varname">此处为数据提供程序名称 </span>-1490307822097|<span class="varname"> 此处为数据提供程序名称 </span>-1490307822038</span> </li> 
      <li id="li_79E7000E82DB4ADA9E9887B017343B2D">新样式：<span class="codeph">21-1-1490307821616|544-1-1490307821793|3-1-1490307821852|420-1-1490307822038| </span> </li> 
     </ul> </p> <p>另请参阅下面的dextp数据语法部分。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>其他属性</b> </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_4922AC2CD55D4C888A6FBEB22F8B889B"> 
      <li id="li_91A68C44E53840379C2ACDED25468735">存留期：<span class="wintitle">dextp</span> Cookie 的生存时间 (TTL) 间隔为 180 天。 </li> 
      <li id="li_6B8C674EFAAC4DABA0A640CF29247F99">Opt-out: <span class="keyword"> Audience Manager </span> resets the cookie with a <span class="codeph"> Do Not Adobe Target </span> string if a user opts-out of data collection. 在这种情况下，Cookie TTL 被设置为 10 年。 </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

dextp Cookie 数据语法：

下表按照元素在数据字符串中的位置列出了 [!DNL dextp] Cookie 中的元素并进行了相关说明。

<table id="table_BE00604B97F24F5A94AA4F566063D785"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 可变位置 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>第一个或第二个</b> </p> </td> 
   <td colname="col2"> <p>数据提供者名称或ID的位置因cookie使用新样式格式还是旧样式格式而异。 </p> <p> <b>旧样式格式：</b> </p> <p> 
     <ul id="ul_5BFBF40E3FE849CA859030F2D070FDF6"> 
      <li id="li_E8F4DC0CB15B472ABE9892B3A61D7F77">Syntax: <span class="codeph"> <span class="varname"> data provider name </span> - <span class="varname"> UNIX UTC timestamp </span> </span> </li> 
      <li id="li_7CD8B101156140F49EA97B18E9591402">示例：<span class="codeph">dataProvider1 – 1490307822038 </span> </li> 
     </ul> </p> <p>旧样式Cookie使用可读名称标识数据提供者。 </p> <p> <b>新样式格式：</b> </p> <p> 
     <ul id="ul_AC6225CA781746148C125F21DFED1ED9"> 
      <li id="li_29C4B52E398B4EA28944980A15B05A57">Syntax: <span class="codeph"> <span class="varname"> data provider ID </span> - 1|2 - <span class="varname"> UNIX UTC timestamp </span> </span> </li> 
      <li id="li_3BF30CA5FED242DF96E0B54AFC64B06F">示例：<span class="codeph"> 123345 - 1 - 1490307822038 </span> </li> 
     </ul> </p> <p>新样式Cookie: </p> <p> 
     <ul id="ul_F05A91A455FA44C7A71186C0C9E31630"> 
      <li id="li_A8C9638173684359BABC4207845A4F48">用数字ID替换可读数据提供程序名称。 </li> 
      <li id="li_28F1E2DB24904E53BE9718AD788CE61E">使用ID 1或ID 2标识呼叫类型。 ID 1表示ID同步调用。 ID 2表示不再使用的已弃用调用。 您不应看到ID为2的许多（或任何）dextp cookie。 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>最后一个</b> </p> </td> 
   <td colname="col2"> <p>最后一个位置包含UNIX UTC时间戳。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**dst Cookie**

<table id="table_83AE9B6350C6408BAECD9FCF33022B98"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 属性 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>用途</b> </p> </td> 
   <td colname="col2"> <p> 如果在向<span class="keyword">目标</span>发送数据时出现错误，<a href="https://docs.adobe.com/content/help/en/audience-manager/user-guide/features/destinations/destinations.html#purposes" format="https" scope="external">Audience Manager</a> 会设置此 Cookie。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>内容</b> </p> </td> 
   <td colname="col2"> <p> <span class="wintitle">DST</span> Cookie 包含目标 ID 集和 UNIX 时间戳，格式为用竖线分隔的字符串。在下面的示例中，<i>斜体</i>表示变量占位符。 </p> <p> 
     <ul id="ul_CE98076A02DA413486C1D341E9806889"> 
      <li id="li_850209D956644749B98C7A208C825C15">语法：<span class="codeph"> <span class="varname"> 目标 ID </span> - <span class="varname"> UNIX UTC 时间戳 </span> </span> </li> 
      <li id="li_4A22152C70844733982230EBF7B9EB78">示例：<span class="codeph">067797-1490349684|1010788-1490349692|1067797-1490349692 </span> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>其他属性</b> </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_5D13DD701B484B51BF2808A69A919106"> 
      <li id="li_4E665114C63246FBA32A4E19984D2693">存留期：<span class="wintitle">dst</span> Cookie 的生存时间 (TTL) 间隔为 180 天。 </li> 
      <li id="li_A682B566704F43D2AB72487EFF212474">Opt-out: <span class="keyword"> Audience Manager </span> resets the cookie with a <span class="codeph"> Do Not Adobe Target </span> string if a user opts-out of data collection. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**_dp Cookie**

这是临时性 Cookie。[!DNL Audience Manager] 会尝试通过设置 [!DNL _dp] Cookie 来确定能否在第三方上下文中的 demdex.net 域内设置其他 Cookie。设置 [!DNL _dp] 时，它包含值 1。[!DNL Audience Manager] 读取此值后会立即删除该 Cookie。如果未设置 [!DNL _dp] Cookie，则 [!DNL Audience Manager] 认为无法设置 Cookie。