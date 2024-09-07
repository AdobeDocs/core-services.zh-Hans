---
title: 帐户首选项和通知
description: 了解Experience Cloud中的用户配置文件和帐户偏好设置。 订阅电子邮件和 [!DNL Slack]的产品通知，并设置产品警报。
solution: Experience Cloud
feature: Account Preferences, Notifications, Alerts
topic: Administration
role: Admin
level: Intermediate
exl-id: 1e34c6b2-a792-41c4-adb7-583de596237f
source-git-commit: b79d6c6fb7bb165fdd5d47061da16f65f6fc7579
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 21%

---

# 帐户首选项和通知 {#preferences}

Experience Cloud[首选项](https://experience.adobe.com/preferences)包括通知（应用程序内、电子邮件和[!DNL Slack]）、订阅和通知。

在首选项中，您可以：

* 搜索[组织](../administration/organizations.md)
* 指定深色主题（并非所有应用程序都支持此主题）。
* 配置用户首选项、通知和订阅。
* 注销Experience Cloud。

## 管理首选项

要管理首选项，请从帐户菜单 ![首选项](../assets/preferences-icon-sm.png) 中选择&#x200B;**[!UICONTROL 首选项]**。

在 [!UICONTROL Experience Cloud 首选项]上，您可以配置以下功能：

| 功能 | 描述 |
|--- |--- |
| 默认[组织](../administration/organizations.md) | 选择您要在启动 Experience Cloud 时看到的组织。 |
| [!UICONTROL 产品数据收集] | 选择 Adobe 可以使用哪些技术来收集有关您如何使用 Adobe 产品的数据。 |
| [通知](#notifications-and-announcements) | 启用[!UICONTROL 应用程序内]、[!UICONTROL 电子邮件]或[Slack](#slack-notifications)通知。 |
| [!UICONTROL 个性化的学习推荐和促销] | 选择您希望从何处接收Adobe产品的[个性化帮助](personalized-learning.md)。 此帮助可通过电子邮件、产品内和Experience League社区提供。 |
| [!UICONTROL 订阅] | 选择您要订阅的产品和类别。[!UICONTROL 通知]弹出框和电子邮件中的通知。 |
| [!UICONTROL 优先级] | 选择您希望视为高优先级的类别。这些类别标有[!UICONTROL 高]标记，可以配置为像警报一样发送。 |
| [!UICONTROL 警报] | 选择您希望在浏览器中显示警报的通知。警报会在窗口右上角出现几秒钟。 |
| 电子邮件 | 指定您希望接收通知电子邮件的频率。（不发送、即时、每日或每周。） |

## 订阅Experience Cloud中的通知 {#notifications}

您可以选择要订阅的产品和类别。 通知显示在[!UICONTROL 通知]弹出框（应用程序内）、电子邮件或[Slack](#slack-notifications)中（具体取决于您的订阅）。

电子邮件和Slack通知对于您未登录Experience Cloud的情况非常有用。

### 订阅应用程序内通知和电子邮件通知

1. 导航到Experience Cloud[首选项](https://experience.adobe.com/preferences)。

1. 在&#x200B;**[!UICONTROL 通知]**&#x200B;下，启用&#x200B;**[!UICONTROL 应用程序内]**&#x200B;或&#x200B;**[!UICONTROL 电子邮件]**。

   对通知的更改会自动保存。

### 订阅[!DNL Slack]通知 {#slack}

>[!NOTE]
>
>Slack通知将发布：**2024年9月11日**


您可以配置帐户首选项以将Experience Cloud通知发送到[!DNL Slack]频道。

**先决条件**

* 您必须拥有Experience Cloud帐户。
* 您必须拥有[!DNL Slack]帐户。 您的Slack管理员可启用Experience Cloud与Slack的集成。
* 您必须是至少一个[!DNL Slack]工作区的一部分。

**订阅Slack通知**

1. 导航到Experience Cloud[首选项](https://experience.adobe.com/preferences)。

1. 找到[!DNL Slack]，然后单击&#x200B;**[!UICONTROL 添加到Slack]**。

   ![添加到Slack](../assets/add-to-slack.png)

   如果安装了[!DNL Slack]，则会打开应用程序并显示权限请求消息。 如果未安装Slack，您必须[请求权限](#slack-troubleshoot)。

1. 单击&#x200B;**[!UICONTROL 允许]**。

1. 在&#x200B;**[!UICONTROL 通知]**&#x200B;下，为所需的产品和类别启用[!DNL Slack]通知。

   ![Slack通知](../assets/slack.png)

   通知更新会自动保存。

### 在Slack中请求权限 {#slack-troubleshoot}

如果未安装[!DNL Slack]，则当您单击“**[!UICONTROL 添加到Slack]**”后打开Slack时，会显示&#x200B;_[!UICONTROL 请求安装]_&#x200B;消息。

![请求Slack集成](../assets/slack-request.png)

**在Slack**&#x200B;中请求权限

1. 在Slack中，从应用程序的右上角选择工作区。

1. 若要请求Slack工作区管理员的申请审批，请单击&#x200B;**[!UICONTROL 提交]**。

1. 申请请求获得批准后，您将在[!DNL Slack]中收到通知。

1. 收到[!DNL Slack]批准后，返回Experience Cloud **[!UICONTROL 通知]**&#x200B;和[订阅Slack](#slack-notifications)（如上所述）。

### 您将在[!DNL Slack]中看到的内容

成功集成Slack后，Slack通知会显示以下信息：

* 将从应用程序名称&#x200B;_Adobe Experience Cloud_&#x200B;接收个人消息。
* 该消息包括特定应用程序(例如Adobe Experience Platform、Adobe Experience Manager等)的产品徽标。
* 用于查看Experience Cloud上所有通知的链接。
* 用于管理Experience Cloud通知首选项的链接。

## 查看Experience Cloud中的[!UICONTROL 通知]和公告 {#view-notifications}

在Experience Cloud标题中，您可以查看[订阅的](#notifications)通知，以及查看公告。

1. 单击标题中的铃铛图标。 ![通知和公告](../assets/bell-icon.png)

1. 单击&#x200B;**[!UICONTROL 通知]**&#x200B;或&#x200B;**[!UICONTROL 公告]**。

   在此位置，您可以接收有关产品、与其他用户的协作以及其他相关更新的重要信息。 更新包括产品版本、维护通知、共享项和审批请求。