---
description: 了解 Experience Cloud 的中央界面组件。在 Admin Console 中获取用户和产品管理帮助，启用 Experience Cloud Service 的应用程序。获取受众库、客户属性、Experience Cloud Assets 等方面的帮助。
title: Experience Cloud界面和管理
uuid: aec6f689-e617-4876-ae6c-e961cfcb991a
feature: Central Interface Components
topic: Administration
role: Admin
level: Experienced
exl-id: aedad5cb-3282-4a97-8e7e-6d65f7b75ba9
source-git-commit: dd4f3b5df4bb7f3775977049e8d9a67e21052f10
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 99%

---

# Experience Cloud 界面和管理

[Experience Cloud](https://experience.adobe.com) 是 Adobe 综合系列的数字营销应用程序、产品和服务。通过其直观界面，您可以快速访问云应用程序、产品功能和服务。

![Experience Cloud](assets/landing.png)

通过 Experience Cloud 的标题，您可以：

* 访问所有 Experience Cloud 应用程序和服务
* 从“帮助”菜单中，搜索产品文档、教程和社区帖子。在 Experience League 中查看结果。
* 使用全局搜索在“搜索”字段中全局搜索业务对象（仅限 Experience Platform 用户）。
* 管理您的帐户[首选项](features/account-preferences.md)（警报、通知和订阅）

## 登录到 Experience Cloud {#signin}

登录并验证您是否处于正确的[组织](administration/organizations.md)中。

1. 导航到 [Adobe Experience Cloud](https://experience.adobe.com)。
1. 请输入您的 Adobe 电子邮件地址，然后单击&#x200B;**[!UICONTROL 继续]**。
1. 单击帐户。
1. 键入您的密码。
1. 验证您是否处于正确的组织中。

   ![验证您是否处于正确的组织中](assets/organizations-menu.png)

   **验证您的组织**

   [组织](administration/organizations.md) 显示在界面标头中。

   如果您的组织使用 Federated ID，则 Experience Cloud 允许您使用组织的单点登录进行登录，而无需输入您的电子邮件地址和密码。将 `#/sso:@domain` 添加到 Experience Cloud URL (`https://experience.adobe.com`) 以完成此任务。

   例如，对于带 Federated ID 和域 `adobecustomer.com` 的组织，请将 URL 链接设置为 `https://experience.adobe.com/#/sso:@adobecustomer.com`。您还可以通过为此 URL 添加书签并追加应用程序路径，直接转到特定应用程序。（例如，对于 Adobe Analytics，使用 `https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`。）

## 访问 Experience Cloud 应用程序 {#navigation}

登录到 Experience Cloud 后，您可以从统一页头中快速访问您的所有应用程序、服务和组织。

要访问组织中为您预配的 Experience Cloud 应用程序和服务，请转到应用程序选择器 ![菜单](assets/apps-icon.png)。

![访问 Experience Cloud 应用程序](assets/platform-core-services.png)

## 获取帮助和支持 {#support}

使用标头中的&#x200B;**[!UICONTROL 帮助中心]**（![资产](assets/help-icon.png)）访问学习和帮助内容，包括[Experience League](https://experienceleague.adobe.com/?lang=zh-Hans#home)上的帮助内容（文档、教程和课程）以及各个应用程序的其他资源。您也可以提交开放式的反馈并创建优先支持服务单。

![获取帮助和支持](assets/search-menu.png)

通过[!UICONTROL 帮助]菜单，您还可以访问：

* **[!UICONTROL 支持]：**&#x200B;创建支持工单或使用 Twitter 联系支持[!UICONTROL 支持]部门。
* **[!UICONTROL 反馈]：**&#x200B;共享您对 Experience Cloud 体验的反馈。您的反馈将用于改进 Adobe 的支持和服务。
* **[!UICONTROL 状态]：**&#x200B;导航到 `https://status.adobe.com/experience_cloud`，检查产品操作状态并[!UICONTROL 管理订阅]。
* **[!UICONTROL 开发人员连接]：**&#x200B;导航到 `adobe.io` 并查找开发人员文档。

## 管理您的用户个人资料

在[!UICONTROL 轮廓]菜单中，您可以：

* 指定深色主题（并非所有应用程序都支持此主题）
* 管理 Experience Cloud [首选项](features/account-preferences.md)
* 选择或搜索 [组织](administration/organizations.md)
* 查看 [!UICONTROL 法律声明]
* 注销
* 配置帐户首选项、通知和订阅

## 查看产品内的通知和公告 {#notifications}

单击铃铛图标即可查看通知和公告。公告可以是相关且可操作的更新，包括产品发布、维护通知、共享项目和批准请求。

![通知和公告](assets/notifications-menu-small.png)

要管理通知和警报，请参阅 [帐户偏好设置和通知](features/account-preferences.md)
