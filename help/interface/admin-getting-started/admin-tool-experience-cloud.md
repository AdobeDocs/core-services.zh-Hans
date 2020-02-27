---
description: 了解Experience cloud管理工具，以查看所有Experience cloud用户的可排序和可过滤列表。
keywords: core services
seo-description: 了解Experience cloud管理工具，以查看所有Experience cloud用户的可排序和可过滤列表。
seo-title: 查看Experience cloud用户和用户详细信息
solution: Experience Cloud
title: '查看Experience cloud用户和用户详细信息 '
index: true
translation-type: tm+mt
source-git-commit: 5e57aedb38e6914f7e99b1b26df9e4bb52b9e13d

---


# 在管理工具中查看Experience cloud用户

管理员可以在管理工具中查看所有Experience cloud用户及其详细信息的可排序和可过滤列表。 用户详细信息包括用户的产品访问、角色和上次访问的信息。** (注**&#x200B;意：用户和产品管理在 [Admin Console中配置](admin-getting-started.md)。)

1. Log in to `https://experience.adobe.com/.`

   ![](assets/admin-tool.png)

1. 在Experience cloud主页中，单击管 **[!UICONTROL 理工具。]**

   (或者，在主页URL中，您可以将主页 _替换为__admin。_)

   此时将 [!UICONTROL 显示] “用户”页面。

## “用户”页

此页面显示有权访问您组织中的Experience cloud的用户的完整列表。 它提供有关解决方案授权和上次登录的信息。 您可以搜索、排序和筛选用户列表的自定义视图。

![](assets/admin-tool-users.png)

| 元素 | 描述 |
|---|---|
| [!UICONTROL 名称] | 用户的名和姓。 您可以将此列从A排序到Z，将Z排序到A。 单击用户名可查看有关该用户的更多详细信息。 |
| [!UICONTROL 电子邮件] | 与用户关联的电子邮件地址。 列可以按A->Z、Z->A排序。 |
| [!UICONTROL ID 类型] | 用户帐户的标识类型。 可以应用筛选器来查看特定ID类型。 有关更 [多信息，请参阅](https://helpx.adobe.com/enterprise/using/identity.html) “管理标识类型”。 |
| [!UICONTROL 解决方案] | 用户可访问的Experience cloud解决方案摘要。 您可以应用过滤器来缩小具有特定解决方案访问权限的用户列表。 |
| [!UICONTROL 上次登录] | 最近用户登录Experience cloud的时间和日期。 此列可以按升序或降序日期排序。 <br> **** 重要说明：自2020年1月13日起，用户的上次登录数据将保留365天。 此信息旨在显示Experience cloud中的当前登录活动，而非建议在2020年1月13日之前对不活动帐户采取相应操作。 |

## 自定义用户列表视图

您可以搜索、排序或筛选列以自定义用户列表。

* 按名称或电子邮件搜索用户。 搜索与您键入的文本字符串匹配。
* 按升序或降序值对列排序。 这适用于“名 [!UICONTROL 称”、] “电 [!UICONTROL 子邮件”] 和“ [!UICONTROL 上次登录] ”列。
* 单击“筛 **[!UICONTROL 选依据]** ”图标以应用多个筛选器以列出具有特定条件的用户。 应用多个筛选器类别后，搜索将包含电子邮件域 `AND` ID类型解决 `AND` 方案。

| 元素 | 描述 |
|---------|----------|
| [!UICONTROL 电子邮件域过滤器] (Email Domain filter) | 在“电子邮件”列中搜索字符串，将结果缩小到一个或多个域。 通过在每个搜索词后按Enter键添加多个过滤器 |
| [!UICONTROL ID类型过滤器] (I) | 从可用的ID类型中进行选择。 可以将多个ID类型用作过滤器。 |
| [!UICONTROL 解决方案] (Solution)过滤器 | 从可用的解决方案中进行选择。 多个解决方案过滤器搜索包含Solution 1 `OR` Solution 2的结果。 |

## 查看用户详细信息

在“用 [!UICONTROL 户] ”页面上，要查看用户的详细信息，请单击用户的电子邮件。

![](assets/admin-tool-user-details.png)

每个用户的详细视图显示有关用户的解决方案访问、管理员和产品角色以及上次访问信息的重要详细信息。

## 关于章节

此部分显示用户帐户的摘要，包括：

* 用户头像和系统管理徽章（如果适用）
* 名称
* 电子邮件
* 用户名（Federated ID帐户的用户名可能与电子邮件地址不同）
* [ID 类型](https://helpx.adobe.com/enterprise/using/identity.html)
* 国家/地区
* 上次登录

## 解决方案摘要

此部分显示用户可访问的Experience cloud解决方案摘要。 包括产品管理员角色（如果适用）

## 详细的产品访问列表

此部分显示用户所有产品配置成员资格的完整列表。

| 元素 | 描述 |
|---------|----------|
| [!UICONTROL 产品] | 与产品配置关联的产品名称。 |
| [!UICONTROL 实例] | 与产品和产品配置文件关联的实例的名称（如登录公司或租户）。 |
| [!UICONTROL 产品简介] | 产品配置的唯一名称。 |
| [!UICONTROL 按组分配] | 将用户关联到产品配置的用户组的名称。 空白结果表示用户直接分配到产品配置，而不是通过组分配。 |
| [!UICONTROL 产品角色] | 产品配置中用户的角色分配。 目前，此信息仅适用于Target产品配置。 |
