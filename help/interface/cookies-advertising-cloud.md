---
description: 了解用于将广告互动事件映射到转化事件的 Adobe Ad Cloud Cookie，并可能会使用该信息来优化广告投标。
title: 'Advertising Cloud Cookie '
uuid: 2eec48a3-3e81-488e-8e30-5fd62885de0b
feature: Cookie
topic: 管理
role: Administrator
level: Experienced
exl-id: 6818edea-31b1-49fc-bca2-32828c7ca78d
source-git-commit: 40fd81f8a293dc5bca3b41e8f6e708d1be4bae5d
workflow-type: tm+mt
source-wordcount: '538'
ht-degree: 96%

---

# Advertising Cloud Cookie{#advertising-cloud-cookies}

Advertising Cloud 使用 Cookie 将广告互动事件映射到转化事件，并可能使用该信息来优化广告投标。

## Cookie 名称：_lcc

<table id="table_821F8EBE91F244CBA72B0975B961B908"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 属性 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>存储的信息 </p> </td> 
   <td colname="col2"> <p>显示屏点击的 ID 和时间戳（格式为 yyyymmdd）</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>过期 </p> </td> 
   <td colname="col2"> <p>15 分钟</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>使用情况 </p> </td> 
   <td colname="col2"> <p>第三方 Cookie，用于确定显示屏广告的点击事件是否适用于 Adobe Analytics 点击 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>位置 </p> </td> 
   <td colname="col2"> <p>everesttech.net </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>大小 </p> </td> 
   <td colname="col2"> <p>52 字节 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cookie 名称：_tmae

<table id="table_28C2B62595E240D5A3C3E0BE147748C1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 属性 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>存储的信息 </p> </td> 
   <td colname="col2"> <p>使用 Advertising Cloud DSP 跟踪的广告互动的编码 ID 和时间戳 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>过期 </p> </td> 
   <td colname="col2"> <p>1 年 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>使用情况 </p> </td> 
   <td colname="col2"> <p>第三方 Cookie，用于存储用户与广告的互动，如“上次在 2016 年 6 月 30 日观看了广告 xyz123” </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>位置 </p> </td> 
   <td colname="col2"> <p>everesttech.net </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>大小 </p> </td> 
   <td colname="col2"> <p>变量；数据将进行编码，通常不足 1 KB </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cookie 名称：adcloud

<table id="table_D7CD238736BC4571883F92F47673F57C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 属性 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>存储的信息 </p> </td> 
   <td colname="col2"> <p>冲浪者上次访问广告商网站和上次搜索点击的时间戳，以及在用户单击广告时创建的 ef_id</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>过期 </p> </td> 
   <td colname="col2"> <p>在 2021 年 2 月 24 日或之前设置的 Cookie 在 730 天后过期。在 2021 年 2 月 25 日或之后设置的 Cookie 在 364 天后过期。</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>使用情况 </p> </td> 
   <td colname="col2"> <p>第一方 Cookie，用于将冲浪者 ID 与相关受众区段和转化关联 </p> <p> 有关上次访问的信息将用于避免向 Adobe 服务器发出不必要的请求，从而优化页面加载时间。 </p> <p>有关上次搜索点击的信息可帮助确定转化事件是点击的结果还是查看的结果（转化由展示次数产生，但非点击量）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>位置 </p> </td> 
   <td colname="col2"> <p>广告商的顶级域（如 example.com） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>大小 </p> </td> 
   <td colname="col2"> <p>变量，但通常为 50-150 字节 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cookie 名称：ev_sync_*

（ev_sync_ax、ev_sync_bk、ev_sync_dd、ev_sync_fs、ev_sync_ix、ev_sync_nx、ev_sync_ox、ev_sync_pm、ev_sync_rc、ev_sync_tm、ev_sync_yh）

<table id="table_A05C02AB261946E0AABAD78259392D81"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 属性 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>存储的信息 </p> </td> 
   <td colname="col2"> <p>执行同步的日期，格式为yyyymmdd </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>过期 </p> </td> 
   <td colname="col2"> <p>执行同步的日期，格式为yyyymmdd </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>使用情况 </p> </td> 
   <td colname="col2"> <p>第三方广告交易特定的 Cookie，用于同步 Advertising Cloud 冲浪者 ID 与合作伙伴广告交易。它是为新冲浪者创建的，并在过期时发送同步请求。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>位置 </p> </td> 
   <td colname="col2"> <p>everesttech.net </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>大小 </p> </td> 
   <td colname="col2"> <p>8 个字符 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cookie 名称：everest_g_v2

<table id="table_04043292A43B41B69EAF17AF4E217C69"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 属性 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>存储的信息 </p> </td> 
   <td colname="col2"> <p>浏览器和冲浪 ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>过期 </p> </td> 
   <td colname="col2"> <p>2 年 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>使用情况 </p> </td> 
   <td colname="col2"> <p>在用户最初单击客户的广告后创建，用于将当前点击和后续点击与客户网站上的其他事件进行映射 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>位置 </p> </td> 
   <td colname="col2"> <p>everesttech.net </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>大小 </p> </td> 
   <td colname="col2"> <p>~27 个字符 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cookie 名称：everest_session_v2

<table id="table_1A3AE4CA71304ADB943CB1F64BE695F5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 属性 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>存储的信息 </p> </td> 
   <td colname="col2"> <p>会话 ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>过期 </p> </td> 
   <td colname="col2"> <p>浏览器关闭时 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>使用情况 </p> </td> 
   <td colname="col2"> <p>第三方浏览器会话 Cookie，这个 Cookie 适用于所有帐户 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>位置 </p> </td> 
   <td colname="col2"> <p>everesttech.net </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>大小 </p> </td> 
   <td colname="col2"> <p>~16 个字符 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cookie 名称：ev_tm

<table id="table_6C4D9DCFA4BF4FB2BD445E027550955F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 属性 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>存储的信息 </p> </td> 
   <td colname="col2"> <p>Advertising Cloud DSP (Demand Side Platform) ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>过期 </p> </td> 
   <td colname="col2"> <p>2 年 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>使用情况 </p> </td> 
   <td colname="col2"> <p>第三方 Cookie，用于存储与 everest_g_v2 Cookie 中的冲浪者 ID 相对应的 DSP ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>位置 </p> </td> 
   <td colname="col2"> <p>everesttech.net </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>大小 </p> </td> 
   <td colname="col2"> <p>~20 字节 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cookie 名称：id_adcloud

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 属性 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>存储的信息 </p> </td> 
   <td colname="col2"> <p>冲浪者 ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>过期 </p> </td> 
   <td colname="col2"> <p>91 天 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>使用情况 </p> </td> 
   <td colname="col2"> <p>Cookie 已在第一方域中设置，但尚未使用 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>位置 </p> </td> 
   <td colname="col2"> <p>广告商的顶级域（如 example.com） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>大小 </p> </td> 
   <td colname="col2"> <p>16 字节 </p> </td> 
  </tr> 
 </tbody> 
</table>
