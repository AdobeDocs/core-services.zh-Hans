---
description: 删除在桌面浏览器和移动设备浏览器中阻止所有 Cookie 的用户。
keywords: cookies；隐私权
seo-description: 删除在桌面浏览器和移动设备浏览器中阻止所有 Cookie 的用户。
seo-title: 启用浏览器 Cookie 的隐私设置
solution: Marketing Cloud、Analytics、Target、Social
title: 启用浏览器 Cookie 的隐私设置
uuid: f6a56e8b-b021-49db-8eb4-6c14 af0 c7243
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: c1630f5de61e410eaf10cf940faa9adc6017fb6b

---


# 启用浏览器 Cookie 的隐私设置{#enable-privacy-settings-for-browser-cookies}

删除在桌面浏览器和移动设备浏览器中阻止所有 Cookie 的用户。

如果用户在其浏览器的 Cookie 设置中阻止了所有 Cookie，那么此设置可以顺应用户希望停止 Analytics 处理的意愿。

1. Navigate to **[!UICONTROL Admin Tools]** &gt; **[!UICONTROL Report Suites]**.
1. Click **[!UICONTROL Edit Settings]** &gt; **[!UICONTROL General]** &gt; **[!UICONTROL Privacy Settings]**.
1. Enable **[!UICONTROL Privacy Settings]** (for desktop or mobile).

   启用此功能后，Analytics 报表将排除从用户已设置为阻止所有 Cookie 的桌面浏览器中收集的数据。如果 Adobe 无法识别浏览器，则数据将包括在 Analytics 报表中。

>[!IMPORTANT]
>
>请注意，许多移动应用程序(如Facebook或Twitter应用程序浏览器)可以作为标准移动浏览器显示，但不允许所有cookie。启用此功能可能会导致从 Analytics 报表中排除很大部分的移动设备流量。

**关于浏览器的隐私设置**

法律和监管指南表示，用户阻止 Cookie 的操作与用户退出分析的操作相同。启用此功能后，Analytics 报表将排除从用户已设置为阻止所有 Cookie 的桌面浏览器中收集的数据。如果 Adobe 无法识别 Web 浏览器，则数据将包括在 Analytics 报表中。

世界各地的立法机构均已表示（在相关方针文件和协议中），浏览器的 Cookie 设置表明用户选择退出分析。具体而言，立法机构表示如果浏览器设置阻止第三方 Cookie，就意味着请求选择退出第三方（跨站点）跟踪；阻止所有 Cookie 则意味着请求选择退出所有跟踪。虽然利用服务器端标识符（例如，IP 地址或用户代理）绕过浏览器的 Cookie 设置是一个很好的办法，但是一些立法机构认为这属于规避用户选择。

<!--
<p>Awaiting content from Vinay May 20 2015 </p>
<p>https://wiki.corp.adobe.com/display/omtrcache/Inferred+Opt+Out </p>
<p>https://wiki.corp.adobe.com/display/omtrplatform/Auto-opt-out+For+Users+Who+Block+Cookies </p>
-->

