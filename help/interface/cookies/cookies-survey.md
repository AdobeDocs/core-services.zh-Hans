---
description: Survey 使用 Cookie 区分来自不同浏览器的请求，并存储可用来更好地了解客户情感的有用信息。
keywords: cookies;隐私
seo-description: Survey 使用 Cookie 区分来自不同浏览器的请求，并存储可用来更好地了解客户情感的有用信息。
seo-title: Survey Cookie
solution: Marketing Cloud,Analytics,Target,Social
title: Survey Cookie
uuid: e57d9b58-3c62-463a-ad52-e2a0de2e1ee1
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: c24b266eda9aae1e86a58ac473fa339f7eb26efe

---


# Survey Cookie{#survey-cookies}

Survey 使用 Cookie 区分来自不同浏览器的请求，并存储可用来更好地了解客户情感的有用信息。

* [Cookie 名称：s_sv_sid](../cookies/cookies-survey.md#section-03aa90aa7e36427b8cb12dc4a0f0291e)
* [Cookie 名称：s_sv_s1](../cookies/cookies-survey.md#section-14ad50dfcd7342f9ac80283b1f0d3400)
* [Cookie 名称：s_sv_p1](../cookies/cookies-survey.md#section-05d1c52c478541609f4a18a9c1eb032f)

## Cookie 名称：s_sv_sid {#section-03aa90aa7e36427b8cb12dc4a0f0291e}

| 属性 | 描述 |
|---|---|
| 存储的信息 | 存储一个唯一数字，以确保正确缓存用于在浏览器内呈现调查的 JavaScript 文件。 |
| 过期 | 此 Cookie 是会话 Cookie，关闭浏览器之后即到期。 |

## Cookie 名称：s_sv_s1 {#section-14ad50dfcd7342f9ac80283b1f0d3400}

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
   <td colname="col2"> <p> 
     <ul id="ul_350369AFBEFF49938026D7D25D012A88"> 
      <li id="li_EA3D03382BFA474B802D1EE2054FABDB">存储在提示访客进行调查时访客通过点击“以后再说”而推迟的调查的 ID。 </li> 
      <li id="li_6111E8D568D64D7CBFB906046134025C"> 存储可以在网站的以下网页上启动的调查的 ID。 </li> 
      <li id="li_A16519F487654435B50577DA08654E70">存储已开始启动的调查的 ID。 </li> 
      <li id="li_8322C91846AB4A65B277C435D61660BF">存储调查系统开始执行的时间（针对延迟的调查）。 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 过期 </td> 
   <td colname="col2"> 此 Cookie 是会话 Cookie，关闭浏览器之后即到期。 </td> 
  </tr> 
 </tbody> 
</table>

## Cookie 名称：s_sv_p1 {#section-05d1c52c478541609f4a18a9c1eb032f}

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
   <td colname="col2"> <p> 
     <ul id="ul_A2717AD89DA540468963E9E7FBD382D5"> 
      <li id="li_21B0165911C74BA796111E9C93142B95">存储已进行或拒绝的调查的 ID。 </li> 
      <li id="li_DD966285CAE7438C9E43AFC4E91569F8">存储用于指定访客是否与采样率匹配的信息。 </li> 
      <li id="li_27BD16FE78BC46C3846BFFE4DF65BCB3">存储在启动“站点退出”调查以确保访客已离开站点时使用的不断增加的数字。 </li> 
      <li id="li_0C9FF8939615407BB9A0DB24C7C31CE6">存储一个标志，该标志用来指示访客是否已达到客户指定的任务设置，并应从调查中排除。 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 过期 </td> 
   <td colname="col2"> 此 Cookie 是永久性的。 </td> 
  </tr> 
 </tbody> 
</table>

<a id="section_488AFFB899004968A2479B2423E6EEB7"></a>

>[!NOTE]
>
>如果要存储在 s_sv_s1 或 s_sv_p1 中的信息太大，则该信息会被拆分，然后按照需要存储在其他 Cookie（命名为 s_sv_s2、s_sv_s3 等或 s_sv_p2、s_sv_p3 等）中。

