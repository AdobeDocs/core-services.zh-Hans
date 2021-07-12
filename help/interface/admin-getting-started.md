---
title: 管理用户和产品
description: 了解如何登录到 Admin Console 并管理 Experience Cloud 用户权限和产品配置文件。了解有关向 Experience Cloud 用户委派管理权限以及 Experience Cloud 浏览器支持的信息。
solution: Admin
index: true
feature: Admin Console
topic: 管理
role: Admin
level: Experienced
exl-id: af9eda5b-d984-44b7-a7b3-52dfc4e03d8f
source-git-commit: 1fb1abc7311573f976f7e6b6ae67f60ada10a3e7
workflow-type: tm+mt
source-wordcount: '1275'
ht-degree: 95%

---

# 管理 Experience Cloud 用户和产品

了解有关登录到 Admin Console 并管理 Experience Cloud 用户权限和产品配置文件，以及浏览器支持的信息。

>[!IMPORTANT]
>
>以下信息专门针对 Experience Cloud 应用程序。此信息补充了 Adobe 所有云产品的[企业管理用户指南](https://helpx.adobe.com/cn/enterprise/admin-guide.html)中更广泛的管理信息。

您可以在“管理工具”中查看所有 Experience Cloud 用户的可排序、可过滤列表及其详细信息。请参阅[在管理工具中查看 Experience Cloud 用户](admin-tool-experience-cloud.md)。

## 什么是产品配置文件？ {#section_AB50558124D541CF80A0D3D76D35A4BF}

[!UICONTROL 产品配置文件]是可以分配给用户的产品组和服务组。在 Experience Cloud 中，权限基于产品的配置文件，而不是基于用户。（但是，您可以将管理权限委派给特定用户。）

例如，在 Analytics 中，您可以配置报表工具集合（如 Analysis Workspace 和 Report Builder）以及报表包、量度和维度。您可以通过将用户添加到产品配置文件来授予对产品配置文件的权限。

* 请参阅本页面上的[将 Analytics 访问权限分配给产品配置文件](admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391)。
* 请参阅此页面上的[将管理角色委派给用户](#delegate-rights)

## 管理 Experience Cloud 产品配置文件 {#task_16335111C52D40E9BAC73D0699584DBF}

您可以创建产品配置文件，并将其分配给权限组。

邀请用户加入组织时，您可以授予用户访问产品和产品配置文件的权限。您还可以将有限的管理权限委派给某个用户。同样，您可以创建用户组，然后将该组添加到产品配置文件以启用访问权限。

1. 在[Admin Console](https://adminconsole.adobe.com/enterprise/)中，选择&#x200B;**[!UICONTROL 产品]**。
1. 选择您的组织名称。
1. 选择&#x200B;**[!UICONTROL 新建配置文件]**。
1. 配置配置文件详细信息，然后选择&#x200B;**[!UICONTROL Save]**。

有关更多信息（以及有关 Creative Cloud 和 Document Cloud 产品管理的帮助），请参阅[管理用户指南](https://helpx.adobe.com/cn/enterprise/admin-guide.html/enterprise/using/users.ug.html)中的[身份](https://helpx.adobe.com/cn/enterprise/admin-guide.html/enterprise/using/identity.ug.html)。

**相关帮助**

* 管理用户指南中的[管理产品和配置文件](https://helpx.adobe.com/cn/enterprise/admin-guide.html/enterprise/using/manage-products.ug.html)。
* 有关更多信息，请参阅 Adobe Target 帮助中的[企业用户权限](https://experienceleague.adobe.com/docs/target/using/administer/manage-users/enterprise/property-channel.html?lang=zh-Hans)。
* 视频：[如何在 Adobe Admin Console 中配置 Adobe Target 工作区](https://helpx.adobe.com/cn/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

<!-- ## What's new in Experience Cloud user management {#concept_06A0A13362F644FB90F947238407637A}

Learn about the latest features in Experience Cloud user and product management.

### Business ID type

Adobe is introducing an identity type called Business ID. This identity type improves the control of user and product management. Adobe is migrating all Adobe IDs (owned by individuals) that are used for business to the new enterprise Business IDs owned by your organization.

If you are an existing Experience Cloud customer, Adobe will migrate all your users with Adobe IDs in the Admin Console to Business IDs. If you are a new enterprise or teams customer, you will add users to the Admin Console using one of the available identity types: Business ID, Enterprise ID, or Federated ID.

What to do

* Your users will need to accept Terms of Use (TOU) changes prior to accounts being migrated to Type2e. 
* Users that belong to multiple organizations might see a Profile Selection screen during the login workflow and need to select the correct one. This ensures that they are logging into the correct organization. (There might be multiple profiles to choose from if a user was a member of multiple organizations before the migration.)

Beginning May 2020, enterprise administrators cannot use the Adobe ID for new organizations created in the Admin Console. Latest: https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=engage&title=Type2e+DX+GTM-->

## 将管理角色分配给用户 {#delegate-rights}

在 Admin Console 中，您可以将有限的管理权限委派给贵组织中的其他人员。凭借委派的角色，用户能够管理对最终用户的软件访问权限，提供访问部署功能，并充当支持代表。

例如，您可以：

* 允许您的创意总监授予对 Creative Cloud 的访问权限。
* 允许您的营销总监授予对 Experience Cloud 的访问权限。
* 将这两个角色分开，以便它们不会逾越彼此的角色权限。

通过使用这些角色，您可以将管理同时委派给其他人，而不会提供超出其需求的更多功能。

1. 在Admin Console中，选择&#x200B;**[!UICONTROL Users]**，然后选择用户名。

   ![](assets/edit-admin-rights.png)

1. 选择&#x200B;**[!UICONTROL 编辑管理权限]**。

   ![](assets/edit-admin-rights-page.png)

1. 指定用户的管理权限。
1. 选择 **[!UICONTROL Save]**。

## 管理 Analytics 用户和产品 {#section_97DE101F92CD494AB073893680992F1A}

您可以将 Analytics 报表访问权限（报表包、量度、维度等）分配给产品配置文件。

例如，您可以创建包含多个 Analytics 工具（[!UICONTROL Analysis Workspace]、[!UICONTROL Reports &amp; Analytics] 和 [!UICONTROL Report Builder]）的产品配置文件。这些配置文件包含对特定量度和维度（包括 eVar）的权限，以及区段或计算量度创建等功能。

1. 登录到[Admin Console](https://adminconsole.adobe.com/enterprise)，然后选择&#x200B;**[!UICONTROL 产品]**。
1. 在[!UICONTROL 产品]页面上，选择您的产品，然后选择&#x200B;**[!UICONTROL 权限]**（仅供管理员使用）。
1. 配置该配置文件的权限：

| 元素 | 描述 |
|--- |--- |
| Report Suites | 启用对特定报表包的权限。 |
| 量度 | 启用流量、转化、自定义事件、解决方案事件和内容识别等的权限。 |
| 维度 | 在粒度级别自定义用户访问权限，包括 eVar、流量报表、解决方案报表和路径报表。 |
| 报表包工具 | 启用 Web 服务、报表包管理、工具和报表及功能板项目的用户权限。 |
| Analytics 工具 | 启用常规项目（帐单、日志等）、公司管理、工具、Web 服务访问、Report Builder 和 Data Connectors 集成的用户权限。“自定义 Admin Console”类别中的“公司设置”已被移动到“Analytics 工具”中。 |

**用户帐户迁移**

Analytics 用户 ID 迁移工具可帮助 Analytics 管理员将用户帐户从 Analytics 用户管理迁移到 [Adobe Admin Console](https://adminconsole.adobe.com/enterprise/)。

Adobe 正在分阶段向客户推出这项帐户迁移功能。当您需要将现有用户帐户从&#x200B;**[!UICONTROL 管理工具]** > **[!UICONTROL 用户管理]**&#x200B;迁移到 Admin Console 时，Adobe 会通知您并给予协助。

迁移后，用户在 [experience.adobe.com](https://experience.adobe.com) 上使用他们的 Adobe ID（或 Enterprise ID）登录，并对其 Experience Cloud 解决方案和服务进行身份验证。如果用户尝试通过旧版的登录方式（[!DNL my.omniture.com]、[!DNL sc.omniture.com] 和 [!DNL experiencecloud.adobe.com]）进行登录，则会被重定向至 [!DNL experience.adobe.com]。

**相关帮助**

有关详细信息，请参阅 [Analytics 用户 ID 迁移](https://experienceleague.adobe.com/docs/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html?lang=zh-Hans)

## 管理 Adobe Target - 产品配置文件与工作区 {#section_3860AF177C9E4C7E9C390D36A414F353}

在 Adobe Target 中，工作区就是产品配置文件。它允许组织为一组特定用户分配一组特定属性。在很多方面，工作区与 Adobe Analytics 中的报表包类似。

请参阅：

* [企业用户权限](https://experienceleague.adobe.com/docs/target/using/administer/manage-users/enterprise/property-channel.html?lang=en)
* [管理产品和配置文件](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-products.ug.html)
* 视频：[如何在 Adobe Admin Console 中配置 Adobe Target 工作区](https://helpx.adobe.com/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

## 管理 Campaign 产品配置文件、租户和安全组 {#section_09CDF75366444CF5810CF321B7C712F3}

Campaign 中的&#x200B;*租户*&#x200B;在 Admin Console“产品”页面上显示为&#x200B;*产品*。

*安全组*&#x200B;显示为产品配置文件。

有关安全组以及将用户分配给安全组的信息，请参阅[管理组和用户](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/users-and-security/managing-groups-and-users.html?lang=zh-Hans)。

## 管理 Experience Platform 数据收集 (Launch) {#section_F2DA6778DD2D48AA8F794041971EE6B1}

Experience Platform [!UICONTROL 数据收集] ([!UICONTROL Launch]) 会显示在 [!UICONTROL Admin Console] 的[!UICONTROL 产品]页面上。您可以在 Launch 产品配置文件中包含其他解决方案和服务。

邀请用户访问 [!UICONTROL Platform Launch]，并分配用户角色和权限。

有关 Admin Console 中用户权限以及设置特定于 Launch 的选项（包括为配置文件分配权限）的信息，请参阅[用户管理](https://experienceleague.adobe.com/docs/launch/using/admin/user-permissions.html?lang=zh-Hans#admin)。

## Experience Manager 即云服务

Adobe Enterprise 客户在 Adobe [!UICONTROL Admin Console] 中表示为组织。Experience Manager 客户可以使用 Adobe [!UICONTROL Admin Console] 管理产品权利以及对 Experience Manager 即[!UICONTROL 云服务]的 IMS 身份验证。

请参阅 [Experience Manager 即云服务的 IMS 支持](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/security/ims-support.html?lang=zh-Hans)。

## Audience Manager {#section_C31E3FA8A1E14463B1B3E07235F1983C}

创建 Audience Manager 用户并将其分配给组。您还可以查看限制（特征、区段、目标和 [!DNL AlgoModel]）。

请参阅 Audience Manager 帮助中的[管理](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/administration/administration-overview.html?lang=zh-Hans)。

## Experience Cloud 中支持的浏览器

* [!DNL Microsoft® Edge]（Microsoft® 已[结束](https://www.microsoft.com/zh-cn/WindowsForBusiness/End-of-IE-support)对 Internet Explorer 8、9 和 10 的支持。因此，Adobe 将不会针对这些特定 Internet Explorer 版本报告的问题进行修复。）
* [!DNL Google Chrome]
* [!DNL Firefox]
* [!DNL Safari]
* [!DNL Opera]

**注意：**&#x200B;尽管 Experience Cloud 界面支持这些浏览器，但单个应用程序可能不会支持每个浏览器。（例如，[Analytics](https://experienceleague.adobe.com/docs/analytics/admin/sys-reqs.html?lang=zh-Hans) 不支持[!DNL Opera]，[Adobe Target](https://experienceleague.adobe.com/docs/target/using/implement-target/before-implement/supported-browsers.html?lang=zh-Hans) 不支持[!DNL Safari]。）

### 解决方案和产品要求

* [Analytics](https://experienceleague.adobe.com/docs/analytics/admin/sys-reqs.html?lang=en)
* [Report Builder](https://experienceleague.adobe.com/docs/analytics/analyze/report-builder/report-builder-setup/system-requirements.html?lang=zh-Hans)
* [Adobe Target](https://experienceleague.adobe.com/docs/target/using/implement-target/before-implement/supported-browsers.html?lang=en)
