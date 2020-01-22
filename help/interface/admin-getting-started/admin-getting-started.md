---
description: 了解如何登录到Admin Console、管理Experience cloud用户权限和产品配置以及浏览器支持。
keywords: core services
seo-description: 了解如何登录到Admin Console、管理Experience cloud用户权限和产品配置以及浏览器支持。
seo-title: 管理 Experience Cloud 用户和产品
solution: Experience Cloud
title: 管理 Experience Cloud 用户和产品
uuid: aea4e4c3-f543-4e8d-b553-d838418477d6
translation-type: tm+mt
source-git-commit: 6040c4d2f052c561958624296c8e62c8230ae820

---


# 管理 Experience Cloud 用户和产品 {#topic_3FCB4099640647E3B2411ADBFCE81909}

了解如何登录到Admin Console、管理Experience cloud用户权限和产品配置以及浏览器支持。

>[!IMPORTANT]
>
>在 Admin Console 中管理用户会引入新的术语、界面和导航。以下信息介绍了这些变化，并且提供了指向其他帮助资源的链接。该帮助补充了 Adobe 所有云产品的[《企业管理用户指南》](https://helpx.adobe.com/enterprise/managing/user-guide.html)中的信息。

## Experience Cloud 用户管理中的新增功能 {#concept_06A0A13362F644FB90F947238407637A}

了解 Experience Cloud 用户管理的最新功能。

## 登录到 Admin Console {#section_705072FD4EBE4B70BC69EC81F2BB8669}

在解决方案中，管理员不再管理用户。现在，Experience Cloud 的用户和产品管理均在 Admin Console 中进行。

**要登录到 Admin Console**，请执行以下操作：

1. Navigate to [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/#).
1. 键入您的 [Adobe ID 或 Enterprise ID](https://helpx.adobe.com/enterprise/help/identity.html) 及密码。

或者，从 Experience Cloud 菜单 (![](assets/menu-icon.png)) 中，单击&#x200B;**[!UICONTROL 管理]**>**[!UICONTROL &#x200B;启动 Admin Console]**。

**相关帮助**

适用于 Creative Cloud 和 Document Cloud 的[《管理用户指南》](https://helpx.adobe.com/enterprise/using/users.html)。有些信息与 Experience Cloud 用户管理相关，例如[管理身份类型](https://helpx.adobe.com/enterprise/help/identity.html)。

通过[登录并管理您的配置文件设置](../admin-getting-started/getting-started-experience-cloud.md#topic_AC564B6795334DE39359ADD87F52F2E0)，来管理密码、组织和通知。

## 产品配置文件和群组 {#section_AB50558124D541CF80A0D3D76D35A4BF}

增加产品配置文件意味着以往管理解决方案产品及服务的方式（通过使用群组）发生转变。在 Admin Console 中，权限基于产品配置文件，而产品配置文件则涵盖了若干组可以分配给用户的产品和服务。

举例来说，在 Analytics 中，您可以配置一系列报表工具，例如 Analysis Workspace 和 Report Builder，以及报表包、量度、维度等。通过将这些工具添加到配置文件，您可以向用户授予该产品配置文件的权限。请参阅 [将 Analytics 访问权限分配给产品配置文件](../admin-getting-started/admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391).

**相关帮助**

[授权有限的管理权限](../admin-getting-started/admin-getting-started.md#task_3A072C4AA9734BC59FFA7E015271BC7E)

## Analytics {#section_97DE101F92CD494AB073893680992F1A}

在 Admin Console 中管理 Analytics 用户和产品权限。

[将 Analytics 访问权限分配给产品配置文件](../admin-getting-started/admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391)（在此页面上）。

**用户帐户迁移**

Analytics 用户 ID 迁移工具可帮助 Analytics 管理员将用户帐户从 Analytics 用户管理迁移到 [Adobe Admin Console](https://adminconsole.adobe.com/enterprise/)。

Adobe 正在分阶段向客户推出这项帐户迁移功能。当您需要将现有用户帐户从&#x200B;**[!UICONTROL 管理工具]**>**[!UICONTROL &#x200B;用户管理]**迁移到 Admin Console 时，Adobe 会通知您并给予协助。

After the migration, users sign in using their Adobe ID (or Enterprise ID) and authenticate to their Experience Cloud solutions and services at [experiencecloud.adobe.com](https://experiencecloud.adobe.com). 如果用户尝试通过旧版的登录方式（[!DNL my.omniture.com] 和 [!DNL sc.omniture.com]）进行登录，则会被重定向至 [!DNL experiencecloud.adobe.com]。

**相关帮助**

[Analytics 用户 ID 迁移](https://docs.adobe.com/content/help/en/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html)

## Target - 产品配置文件与工作区 {#section_3860AF177C9E4C7E9C390D36A414F353}

在 Target 中，工作区就是产品配置文件。工作区允许组织向一组特定用户分配一组特定属性。在很多方面，工作区与 Adobe Analytics 中的报表包类似。

请参阅：
* [企业用户权限](https://docs.adobe.com/content/help/en/target/using/administer/manage-users/enterprise/property-channel.html)
* [管理产品和配置文件](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html)
* 视频：[如何在 Adobe 管理控制台中配置 Target 工作区](https://helpx.adobe.com/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

## Campaign - 产品配置文件、租户和安全群组 {#section_09CDF75366444CF5810CF321B7C712F3}

Campaign 中的&#x200B;*租户*&#x200B;会在“Admin Console 产品”页面中显示为&#x200B;*产品*。

*安全群组*&#x200B;会显示为产品配置文件。

有关安 [全组以及将用户分配给安全组](https://helpx.adobe.com/campaign/standard/administration/using/managing-groups-and-users.html) ，请参阅管理组和用户。

## Experience Platform Lauch {#section_F2DA6778DD2D48AA8F794041971EE6B1}

Experience Platform Lauch 会显示在 Admin Console 的“产品”页面上。您可以在 Launch 产品配置文件中包含其他解决方案和核心服务。

See [User Management](https://docs.adobelaunch.com/launch-reference/administration/user-permissions) for information about user permissions in the Admin Console and set up Launch-specific options, including assigning rights to profiles.

## 动态标签管理器 {#section_3A41CF2BD5994B9891537D063571D4ED}

您可以邀请用户使用“动态标签管理”、分配用户角色和将用户添加到群组。

See [Users and Permissions](https://docs.adobe.com/content/help/en/dtm/using/admin/users.html) for information about how to invite users to Dynamic Tag Management and assign user roles and add users to groups.

## Audience Manager {#section_C31E3FA8A1E14463B1B3E07235F1983C}

创建 Audience Manager 用户并将其分配到群组。您还可以查看各种限制（特征、区段、目标和 AlgoModel）。

请参 [阅Audience](https://docs.adobe.com/content/help/en/dtm/using/admin/users.html) manager帮助中的管理。

## 管理 Experience Cloud 产品 {#task_16335111C52D40E9BAC73D0699584DBF}

创建产品配置文件并将该文件分配给权限组。

当您邀请用户加入组织时，您可以授予用户访问产品和产品配置文件的权限。您还可以将有限的管理权限授权给用户。同样，您可以创建用户群组，然后将该群组添加到产品配置文件以启用访问。

1. 在 [Admin Console](https://adminconsole.adobe.com/enterprise/) 中，单击&#x200B;**[!UICONTROL 产品]**。
1. 单击&#x200B;**[!UICONTROL 新建配置文件]**。
1. 配置该配置文件的详细信息，然后单击&#x200B;**[!UICONTROL 下一步]**。
1. 单击&#x200B;**[!UICONTROL 完成]**。

以下资源提供了更多帮助：

* [管理产品和配置文件](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html)
* Target 帮助中的[企业用户权限](https://docs.adobe.com/content/help/en/target/using/administer/manage-users/enterprise/property-channel.html)提供了更多信息。
* 视频：[如何在 Adobe 管理控制台中配置 Target 工作区](https://helpx.adobe.com/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

## 将 Analytics 访问权限分配给产品配置文件 {#task_040673FE3E3E429B9531FBCB8B6A4391}

将 Analytics 报表访问权限（报表包、量度、维度等）分配给产品配置文件。

例如，您可以创建一个产品配置文件，其中包含多个 Analytics 工具（[!UICONTROL Analysis Workspace]、[!UICONTROL Reports &amp; Analytics] 和 [!UICONTROL Report Builder]），然后为其分配用来访问特定量度和维度（包括 eVar）以及创建区段或计算量度等功能的权限。

1. 登录到 [Admin Console](https://adminconsole.adobe.com/enterprise)，然后单击&#x200B;**[!UICONTROL 产品]**（或单击您的产品名称）。
1. 随后，在产品配置文件中，单击&#x200B;**[!UICONTROL 权限]**（只有管理员才能使用）。
1. 配置该配置文件的权限：

| 元素 | 描述 |
|--- |--- |
| Report Suites | 启用特定报表包的权限。 |
| 量度 | 启用流量、转化、自定义事件、解决方案事件和内容识别等的权限。 |
| 维度 | 在粒度级别自定义用户访问权限，包括 eVar、流量报表、解决方案报表和路径报表。 |
| 报表包工具 | 启用 Web 服务、报表包管理、工具和报表，以及功能板项目的用户权限。 |
| Analytics 工具 | 启用常规项目（帐单、日志等）、公司管理、工具、Web 服务访问、Report Builder 和 Data Connectors 集成的用户权限。“自定义 Admin Console”类别中的“公司设置”已被移动到“Analytics 工具”中。 |

## 将管理角色分配给用户 {#task_3A072C4AA9734BC59FFA7E015271BC7E}

在管理控制台中，您可以将有限的管理权限分配给组织中的其他人员。通过分配的角色，用户可以管理最终用户的软件访问权限，提供访问部署功能，以及充当支持代表。

例如，您可以：

* 允许您的创意总监授予 Creative Cloud 的访问权限。
* 允许您的市场营销总监授予 Experience Cloud 的访问权限。
* 保持这两个角色相互独立，使他们二者之间无法逾越彼此的职责范围。

利用这些角色，您还可以同时向其他人员分配管理权限，而不提供超出其所需范围的更多职能。

1. 在 Admin Console 中，单击&#x200B;**[!UICONTROL 用户]**，然后单击用户的名称。
1. 单击&#x200B;**[!UICONTROL 编辑管理权限]**。
1. 配置用户的管理权限。
1. 单击&#x200B;**[!UICONTROL 下一步]**以查看设置，然后单击**[!UICONTROL &#x200B;保存]**。

## 支持的浏览器和系统要求 {#concept_CDC4371EB9BF433E9534F8716DC8A088}

Experience Cloud 中支持的浏览器。

Experience cloud支持的浏览器包括：

* [!DNL Microsoft Edge] (Microsoft已 [停止对Internet](https://www.microsoft.com/en-us/WindowsForBusiness/End-of-IE-support) Explorer 8、9和10的支持。 因此，Adobe 将不会修复针对这些特定 Internet Explorer 版本报告的问题。）
* [!DNL Google Chrome]
* [!DNL Firefox]
* [!DNL Safari]
* [!DNL Opera]

**注意：**&#x200B;尽管 Experience Cloud 界面支持这些浏览器，但单个解决方案可能不会支持每个浏览器。（例如，[Analytics](https://docs.adobe.com/content/help/en/analytics/admin/sys-reqs.html) 不支持 [!DNL Opera]，[Target](https://docs.adobe.com/help/en/target/using/implement-target/before-implement/supported-browsers.html) 不支持 [!DNL Safari]。）

**解决方案和产品要求**

* [Analytics](https://docs.adobe.com/content/help/en/analytics/admin/sys-reqs.html)
* [Report Builder](https://docs.adobe.com/content/help/en/analytics/analyze/report-builder/report-builder-setup/system-requirements.html)
* [Adobe Target](https://docs.adobe.com/help/en/target/using/implement-target/before-implement/supported-browsers.html)
