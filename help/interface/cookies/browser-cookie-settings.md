---
description: 删除在桌面浏览器和移动设备浏览器中阻止所有 Cookie 的用户。此隐私权设置不包括选择退出Analytics数据收集的用户。
keywords: cookies;privacy
seo-description: 删除在桌面浏览器和移动设备浏览器中阻止所有 Cookie 的用户。此隐私权设置不包括选择退出Analytics数据收集的用户。
seo-title: 启用浏览器 Cookie 的隐私设置
solution: Marketing Cloud,Adobe Analytics,Adobe Target,Adobe Social
title: 启用浏览器 Cookie 的隐私设置
uuid: f6a56e8b-b021-49db-8eb4-6c14af0c7243
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# 启用浏览器 Cookie 的隐私设置{#enable-privacy-settings-for-browser-cookies}

您可以删除在桌面和移动浏览器上阻止所有Cookie的用户。 此功能是一项隐私设置，不包括选择退出数据收集用户，允许您尊重用户停止Analtyics处理的意图。

**为浏览器cookie启用隐私设置**

1. Navigate to **[!UICONTROL Admin Tools]** > **[!UICONTROL Report Suites]**.
1. Click **[!UICONTROL Edit Settings]** > **[!UICONTROL General]** > **[!UICONTROL Privacy Settings]**.
1. 启用&#x200B;**[!UICONTROL 隐私设置]**（适用于桌面和移动设备）。

>[!IMPORTANT]
>
>请注意，许多移动应用程序（如Facebook或Twitter的应用程序内浏览器）可显示为标准移动浏览器，但不允许所有Cookie。 启用此功能可能会从Analytics报告中排除大部分移动流量。

**关于浏览器隐私设置**

法律和法规指导表明，用户阻止cookies的操作与用户进行概要分析的操选择退出作相同。 通过启用此功能，将从桌面浏览器收集的数据（用户已将浏览器设置为阻止所有Cookie）将从Analytics报告中排除。 如果Adobe无法识别Web浏览器，数据将包含在Analytics报告中。

世界各地的立法者都表示（无论是在指导方面还是在解决方面）,cookie浏览器设置表明用户偏好于选择退出分析。 具体而言，这些议员表示，阻止第三方Cookie的浏览器设置是第三方（跨站点）跟踪的退出请求。 阻止所有Cookie是针对所有跟踪的退出请求。 虽然服务器端标识符（如IP地址或用户代理）可能是绕过cookie浏览器设置的理想选项，但一些立法者将它们视图为规避用户选择。