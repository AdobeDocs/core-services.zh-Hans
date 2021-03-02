---
description: 了解如何为浏览器cookie启用隐私设置。 您可以删除在桌面浏览器和移动设备浏览器中阻止所有 Cookie 的用户。
keywords: cookies;隐私
solution: Experience Cloud, Analytics, Target, Social
title: '浏览器Cookie的隐私设置 '
uuid: f6a56e8b-b021-49db-8eb4-6c14af0c7243
feature: Cookie
topic: 管理
role: 管理员
level: 富有经验
translation-type: tm+mt
source-git-commit: 61d60273e933c637dfe4400da78257e1c80015b3
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 95%

---


# 启用浏览器 Cookie 的隐私设置{#enable-privacy-settings-for-browser-cookies}

您可以删除在桌面浏览器和移动设备浏览器中阻止所有 Cookie 的用户。此功能是一个隐私设置，它不适用于选择退出数据收集的用户，该设置使您能够根据用户的意愿停止 Analytics 处理。

**启用浏览器 Cookie 的隐私设置**

1. 导航至&#x200B;**[!UICONTROL 管理工具]** > **[!UICONTROL 报表包]**。
1. 单击&#x200B;**[!UICONTROL 编辑设置]** > **[!UICONTROL 常规]** > **[!UICONTROL 隐私设置]**。
1. 启用&#x200B;**[!UICONTROL 隐私设置]**（适用于桌面和移动设备）。

>[!IMPORTANT]
>
>请注意，很多移动设备应用程序（例如，Facebook 或 Twitter 的应用程序内浏览器）可能会显示为标准的移动设备浏览器，但是并不能允许使用所有 Cookie。启用此功能可能会从 Analytics 报表中排除大部分移动流量。

**关于浏览器隐私设置**

法律和法规指南已表明，用户阻止 Cookie 的行为与用户选择退出分析的行为相同。启用此功能后，Analytics 报表中将排除从桌面浏览器收集的数据（用户已将浏览器设置为阻止所有 Cookie）。如果 Adobe 无法识别 Web 浏览器，数据将包含在 Analytics 报表中。

世界各地的立法者都表示（无论是在指导意见还是在解决方案中），Cookie 浏览器设置表明用户倾向于选择退出分析。具体来说，这些立法者已经表示，阻止第三方 Cookie 的浏览器设置是第三方（跨站点）跟踪的选择退出请求。阻止所有 Cookie 是所有跟踪的选择退出请求。虽然服务器端标识符（如 IP 地址或用户代理）可能是绕过 Cookie 浏览器设置的理想选项，但一些立法者将它们视为对用户选择的规避。