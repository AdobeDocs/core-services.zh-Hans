---
description: 了解如何启用浏览器 Cookie 的隐私设置。您可以删除在桌面浏览器和移动设备浏览器中阻止所有 Cookie 的用户。
keywords: cookies;隐私
solution: Experience Cloud, Analytics, Target, Social
title: '浏览器 Cookie 的隐私设置 '
uuid: f6a56e8b-b021-49db-8eb4-6c14af0c7243
feature: Cookie
topic: 管理
role: Administrator
level: Experienced
exl-id: 5d852e0e-4004-4f94-a6f7-3a14a96cd42f
source-git-commit: f720e37b693da2c657cb1efab45620c60bfa81a4
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 60%

---

# 启用浏览器 Cookie 的隐私设置{#enable-privacy-settings-for-browser-cookies}

您可以删除在桌面浏览器和移动设备浏览器中阻止所有 Cookie 的用户。此功能是一项隐私设置，其中不包括选择退出数据收集的用户，这使您能够遵守用户停止Analytics处理的意图。

**启用浏览器 Cookie 的隐私设置**

1. 导航至&#x200B;**[!UICONTROL 管理工具]** > **[!UICONTROL 报表包]**。
1. 单击&#x200B;**[!UICONTROL 编辑设置]** > **[!UICONTROL 常规]** > **[!UICONTROL 隐私设置]**。
1. 启用&#x200B;**[!UICONTROL 隐私设置]**（适用于桌面和移动设备）。

>[!IMPORTANT]
>
>许多移动设备应用程序(例如Facebook或Twitter的应用程序内浏览器)可以显示为标准的移动设备浏览器，但并不允许使用所有Cookie。 启用此功能可能会从 Analytics 报表中排除大部分移动流量。

**关于浏览器隐私设置**

法律和法规指南已表明，用户阻止 Cookie 的行为与用户选择退出分析的行为相同。启用此功能后，Analytics报表中将排除从桌面浏览器收集的数据（用户已将浏览器设置为阻止所有Cookie）。 如果Adobe无法识别Web浏览器，则数据将包含在[!DNL Analytics]报表中。

世界各地的立法者都表示（无论是在指导意见还是在解决方案中），Cookie 浏览器设置表明用户倾向于选择退出分析。具体来说，这些立法者已经表示，阻止第三方 Cookie 的浏览器设置是第三方（跨站点）跟踪的选择退出请求。阻止所有 Cookie 是所有跟踪的选择退出请求。虽然服务器端标识符（如IP地址或用户代理）是绕过Cookie浏览器设置的理想选项，但一些立法者将它们视为对用户选择的规避。
