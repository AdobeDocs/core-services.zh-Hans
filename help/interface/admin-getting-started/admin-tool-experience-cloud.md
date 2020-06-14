---
description: 了解 Experience Cloud 管理工具，以查看所有 Experience Cloud 用户的可排序和可过滤列表。
keywords: core services
seo-description: 了解 Experience Cloud 管理工具，以查看所有 Experience Cloud 用户的可排序和可过滤列表。
seo-title: 查看 Experience Cloud 用户和用户详细信息
solution: Experience Cloud
title: '查看 Experience Cloud 用户和用户详细信息 '
index: true
translation-type: ht
source-git-commit: 43de353155c640b3ddc519147c94d7e9ffcafe4e
workflow-type: ht
source-wordcount: '693'
ht-degree: 100%

---


# 在“管理工具”中查看 Experience Cloud 用户

管理员可以在“管理工具”中查看所有 Experience Cloud 用户的可排序、可过滤列表及其详细信息。用户详细信息包括用户的产品访问、角色和上次访问信息。（**注意：**&#x200B;应在 [Admin Console](admin-getting-started.md) 中配置用户和产品管理。）

1. 登录 `https://experience.adobe.com/.`

   ![](assets/admin-tool.png)

1. 在 Experience Cloud 主页上，单击&#x200B;**[!UICONTROL 管理工具]**。

   （或者，在主页 URL 中，您可以将 _home_ 替换为 _admin_。）

   此时，将显示[!UICONTROL 用户]页。

## “用户”页面

此页面显示贵组织中有权访问 Experience Cloud 的完整用户列表。它会提供有关解决方案权利和上次登录的信息。您可以搜索、排序和过滤用户列表的自定义视图。

![](assets/admin-tool-users.png)

| 元素 | 描述 |
|---|---|
| [!UICONTROL 名称] | 用户的名字和姓氏。您可以按从 A 到 Z 以及 Z 到 A 对此列进行排序。单击用户名可查看有关该用户的更多详细信息。 |
| [!UICONTROL 电子邮件] | 与用户关联的电子邮件地址。此列可以按 A->Z、Z->A 进行排序。 |
| [!UICONTROL ID 类型] | 用户帐户的标识类型。可应用过滤器以查看特定 ID 类型。有关更多信息，请参阅[管理标识类型](https://helpx.adobe.com/cn/enterprise/using/identity.html)。 |
| [!UICONTROL 解决方案] | 用户可访问的 Experience Cloud 解决方案摘要。您可以应用过滤器来缩小具有特定解决方案访问权限的用户列表。 |
| [!UICONTROL 上次登录] | 用户最近登录 Experience Cloud 的时间和日期。此列可以按升序或降序日期排序。<br> **重要信息：**&#x200B;自 2020 年 1 月 13 日起，用户的上次登录数据将保留 365 天。该信息旨在显示 Experience Cloud 中的当前登录活动，而不是建议在 2020 年 1 月 13 日之前对不活动帐户采取行动。 |

## 自定义用户列表视图

您可以搜索、排序或过滤列以自定义用户列表。

* 按名称或电子邮件搜索用户。搜索与您键入的文本字符串匹配。
* 按升序或降序值对列排序。这适用于[!UICONTROL 名称]、[!UICONTROL 电子邮件]和[!UICONTROL 上次登录]列。
* 单击&#x200B;**[!UICONTROL 过滤依据]**&#x200B;图标可应用多个过滤器以列出具有特定条件的列表。应用多个过滤类别后，搜索将包含“电子邮件域”`AND`“ID 类型”`AND`“解决方案”。

| 元素 | 描述 |
|---------|----------|
| [!UICONTROL 电子邮件域]过滤器 | 在“电子邮件”列中搜索字符串，以将结果范围缩小到一个或多个域。在每个搜索词后按 Enter 键可添加多个过滤器 |
| [!UICONTROL ID 类型]过滤器 | 从可用的 ID 类型中进行选择。可以将多个 ID 类型用作过滤器。 |
| [!UICONTROL 解决方案]过滤器 | 从可用的解决方案中进行选择。多个解决方案过滤器搜索包含“解决方案 1”`OR`“解决方案 2”的结果。 |

## 查看用户详细信息

在[!UICONTROL 用户]页面上，要查看用户的详细信息，请单击用户的电子邮件。

![](assets/admin-tool-user-details.png)

每个用户的详细视图将显示有关用户的解决方案访问权限、管理员和产品角色以及上次访问信息的重要详细信息。

## “关于”部分

此部分显示用户帐户的摘要，包括：

* 用户头像和系统管理员徽章（如果适用）
* 名称
* 电子邮件
* 用户名（Federated ID 帐户的用户名可能与电子邮件地址不同）
* [ID 类型](https://helpx.adobe.com/cn/enterprise/using/identity.html)
* 国家/地区
* 上次登录

## 解决方案摘要

此部分会显示用户可访问的 Experience Cloud 解决方案的摘要。包括产品管理角色（如果适用）。

## 详细的产品访问列表

此部分显示用户的所有产品配置文件成员资格的完整列表。

| 元素 | 描述 |
|---------|----------|
| [!UICONTROL 产品] | 与产品配置文件关联的产品名称。 |
| [!UICONTROL 实例] | 与产品和产品配置文件关联的实例的名称（如登录公司或租户）。 |
| [!UICONTROL 产品配置文件] | 产品配置文件的唯一名称。 |
| [!UICONTROL 按组分配] | 将用户关联到产品配置文件的用户组的名称。空白结果表示未通过组直接将用户分配到产品配置文件。 |
| [!UICONTROL 产品角色] | 产品配置文件中用户的角色分配。目前，此信息仅适用于 Adobe Target 产品配置文件。 |
