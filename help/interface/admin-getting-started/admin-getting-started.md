---
description: 了解如何登录到Admin Console、管理Experience Cloud用户权限和产品配置以及浏览器支持。
keywords: core services
seo-description: 了解如何登录到Admin Console、管理Experience Cloud用户权限和产品配置以及浏览器支持。
seo-title: 管理 Experience Cloud 用户和产品
solution: Experience Cloud
title: 管理 Experience Cloud 用户和产品
uuid: aea4e4c3-f543-4e8d-b553-d838418477d6
translation-type: tm+mt
source-git-commit: b6bd75d92ce96e852a6e548362988a9b4d529fb9

---


# 管理 Experience Cloud 用户和产品 {#topic_3FCB4099640647E3B2411ADBFCE81909}

了解如何登录到Admin Console、管理Experience Cloud用户权限和产品配置以及浏览器支持。

>[!IMPORTANT]
>
>在 Admin Console 中管理用户会引入新的术语、界面和导航。以下信息介绍了这些变化，并且提供了指向其他帮助资源的链接。This help supplements the information in the [Enterprise Administration User Guide](https://helpx.adobe.com/enterprise/managing/user-guide.html) for all Adobe cloud products.

## Experience Cloud 用户管理中的新增功能 {#concept_06A0A13362F644FB90F947238407637A}

了解 Experience Cloud 用户管理的最新功能。

<!--

### Business ID type

Adobe is now introducing a new identity type: **Business ID**. This identity type, improves the control of user and product management, and content, while increasing the flexibility of Experience Cloud and Creative Cloud storage usage among your team. With the introduction of this new identity type, Adobe is migrating all Adobe IDs (owned by the individual) used for business to the new Business IDs (owned by the organization).

If you're an existing Creative Cloud for enterprise or teams customer, Adobe will migrate all your users on the Admin Console with Adobe IDs to Business IDs. If you're a new enterprise or teams customer, you will add users to the Admin Console using one of the available identity types: Business ID, Enterprise ID, or Federated ID. 

Beginning May 89, 2020, enterprise admins cannot use the Adobe ID for new organizations created in the Admin Console. Latest: https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=engage&title=Type2e+DX+GTM

What to do

* Your users will need to accept Terms of Use (TOU) changes prior to accounts being migrated to Type2e. 
* Users that belong to multiple organizations might see a Profile Selection screen during the login workflow and need to select the correct one. This ensures that they are logging into the correct organization. (There might be multiple profiles to choose from if a users was a member of multiple organizations before the migration.)
-->

### 管理工具

管理员可以在管理工具中查看所有Experience Cloud用户及其详细信息的可排序和可过滤列表。 请参 [阅在管理工具中查看Experience Cloud用户](admin-tool-experience-cloud.md)。

## 登录到 Admin Console {#section_705072FD4EBE4B70BC69EC81F2BB8669}

管理员不再管理解决方案中的用户。 Experience Cloud的用户和产品管理现在在管理控制台中进行。

**登录到Admin Console**

1. Navigate to [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/#).
1. 键入 [Adobe ID或Enterprise ID](https://helpx.adobe.com/enterprise/help/identity.html) 和密码。

Alternatively, from the Experience Cloud menu ( ![](assets/menu-icon.png)), click **[!UICONTROL Administration]** > **[!UICONTROL Launch Admin Console]**.

**相关帮助**

[Creative Cloud和](https://helpx.adobe.com/enterprise/using/users.html) Document Cloud管理用户指南。 某些信息与Experience Cloud用户管理相关，例如管 [理身份类型](https://helpx.adobe.com/enterprise/help/identity.html)。

[登录并管理您的配置文件设置](../admin-getting-started/getting-started-experience-cloud.md#topic_AC564B6795334DE39359ADD87F52F2E0) ，以管理密码、组织和通知。

## 产品配置和组 {#section_AB50558124D541CF80A0D3D76D35A4BF}

添加产品配置文件标志着以前（通过使用组）管理解决方案产品和服务的方式发生了变化。 在Admin Console中，权限基于产品配置文件，这些配置文件是您可以分配给用户的产品和服务组。

例如，在Analytics中，您可以配置报告工具的集合，如Analysis Workspace和Report Builder，以及报告套件、指标、维度等。 您可以通过将用户添加到配置文件来向产品配置文件授予权限。 See [Assign Analytics access permissions to a product profile](../admin-getting-started/admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391).

**相关帮助**

[授权有限的管理权限](../admin-getting-started/admin-getting-started.md#task_3A072C4AA9734BC59FFA7E015271BC7E)

## Analytics {#section_97DE101F92CD494AB073893680992F1A}

在 Admin Console 中管理 Analytics 用户和产品权限。

[将 Analytics 访问权限分配给产品配置文件](../admin-getting-started/admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391)（在此页面上）。

**用户帐户迁移**

Analytics 用户 ID 迁移工具可帮助 Analytics 管理员将用户帐户从 Analytics 用户管理迁移到 [Adobe Admin Console](https://adminconsole.adobe.com/enterprise/)。

Adobe 正在分阶段向客户推出这项帐户迁移功能。Adobe will notify and assist you when it is your time to migrate existing user accounts from **[!UICONTROL Admin Tools]** > **[!UICONTROL User Management]** to the Admin Console.

After the migration, users sign in using their Adobe ID (or Enterprise ID) and authenticate to their Experience Cloud solutions and services at [experiencecloud.adobe.com](https://experiencecloud.adobe.com). 如果用户尝试通过旧版的登录方式（[!DNL my.omniture.com] 和 [!DNL sc.omniture.com]）进行登录，则会被重定向至 [!DNL experiencecloud.adobe.com]。

**相关帮助**

[Analytics用户ID迁移](https://docs.adobe.com/content/help/en/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html)

## Target - 产品配置文件与工作区 {#section_3860AF177C9E4C7E9C390D36A414F353}

在Target中，工作区是产品配置。 它允许组织将一组特定用户分配到一组特定属性。 在很多方面，工作区与 Adobe Analytics 中的报表包类似。

请参阅：
* [企业用户权限](https://docs.adobe.com/content/help/en/target/using/administer/manage-users/enterprise/property-channel.html)
* [管理产品和配置](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html)
* 视频：如 [何在Adobe Admin Console中配置目标工作区](https://helpx.adobe.com/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

## Campaign - 产品配置文件、租户和安全群组 {#section_09CDF75366444CF5810CF321B7C712F3}

Campaign中 *的租户* ，在Admin Console产品页 *面中* ，显示为产品。

*安全组* 显示为产品配置。

有关安 [全组以及将用户分配给安全组](https://helpx.adobe.com/campaign/standard/administration/using/managing-groups-and-users.html) ，请参阅管理组和用户。

## Experience Platform Launch {#section_F2DA6778DD2D48AA8F794041971EE6B1}

Experience Platform Launch显示在Admin Console的“产品”页面上。 您可以在Launch产品配置中包含其他解决方案和服务。

请参 [阅用户管理](https://docs.adobelaunch.com/launch-reference/administration/user-permissions) ，以了解有关Admin Console中用户权限的信息并设置特定于启动项的选项，包括为配置文件分配权限。

## 动态标签管理器 {#section_3A41CF2BD5994B9891537D063571D4ED}

您可以邀请用户使用“动态标签管理”、分配用户角色和将用户添加到群组。

See [Users and Permissions](https://docs.adobe.com/content/help/en/dtm/using/admin/users.html) for information about how to invite users to Dynamic Tag Management and assign user roles and add users to groups.

## Audience Manager {#section_C31E3FA8A1E14463B1B3E07235F1983C}

创建Audience Manager用户并将其分配给用户组。 您还可以查看限制（特征、区段、目标和AlgoModel）。

请参 [阅Audience](https://docs.adobe.com/content/help/en/dtm/using/admin/users.html) Manager帮助中的管理。

## 管理 Experience Cloud 产品 {#task_16335111C52D40E9BAC73D0699584DBF}

创建产品配置并将其分配给权限组。

当您邀请用户加入组织时，您可以授予用户对产品和产品配置的访问权限。 您还可以将有限的管理权限委派给用户。 同样，您可以创建用户组，然后将该用户组添加到产品配置以启用访问。

1. In the [Admin Console](https://adminconsole.adobe.com/enterprise/), click **[!UICONTROL Products]**.
1. 单击&#x200B;**[!UICONTROL 新建配置文件]**。
1. 配置该配置文件的详细信息，然后单击&#x200B;**[!UICONTROL 下一步]**。
1. 单击&#x200B;**[!UICONTROL 完成]**。

有关更多帮助，请访问：

* [管理产品和配置](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html)
* [Target帮助中的“企业用户权限](https://docs.adobe.com/content/help/en/target/using/administer/manage-users/enterprise/property-channel.html) ”，以了解更多信息。
* 视频：如 [何在Adobe Admin Console中配置目标工作区](https://helpx.adobe.com/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

## 将 Analytics 访问权限分配给产品配置文件 {#task_040673FE3E3E429B9531FBCB8B6A4391}

将 Analytics 报表访问权限（报表包、量度、维度等）分配给产品配置文件。

例如，您可以创建一个产品配置文件，其中包含多个 Analytics 工具（[!UICONTROL Analysis Workspace]、[!UICONTROL Reports &amp; Analytics] 和 [!UICONTROL Report Builder]），然后为其分配用来访问特定量度和维度（包括 eVar）以及创建区段或计算量度等功能的权限。

1. Sign in to the [Admin Console](https://adminconsole.adobe.com/enterprise), then click **[!UICONTROL Products]** (or click your product name).
1. 随后，在产品配置文件中，单击&#x200B;**[!UICONTROL 权限]**（只有管理员才能使用）。
1. 配置该配置文件的权限：

| 元素 | 描述 |
|--- |--- |
| Report Suites | 为特定报表包启用权限。 |
| 量度 | 启用流量、转化、自定义事件、解决方案事件、内容感知等权限。 |
| 维度 | 在粒度级别自定义用户访问权限，包括 eVar、流量报表、解决方案报表和路径报表。 |
| 报表包工具 | 为Web服务、报表包管理、工具和报表以及仪表板项目启用用户权限。 |
| Analytics 工具 | 启用常规项目（帐单、日志等）、公司管理、工具、Web 服务访问、Report Builder 和 Data Connectors 集成的用户权限。“自定义 Admin Console”类别中的“公司设置”已被移动到“Analytics 工具”中。 |

## 将管理角色分配给用户 {#task_3A072C4AA9734BC59FFA7E015271BC7E}

在Admin Console中，您可以将有限的管理权限委派给组织中的其他人。 授权角色使用户能够管理对最终用户的软件访问，提供访问部署功能并充当支持代表。

例如，您可以：

* 允许您的创意总监授予对Creative Cloud的访问权限。
* 允许您的营销总监授予对Experience Cloud的访问权限。
* 将这两个角色分开，这样它们就不能超越彼此的角色。

通过使用这些角色，您可以同时将管理委派给他人，而不会提供超出他们需要的更多功能。

1. 在 Admin Console 中，单击&#x200B;**[!UICONTROL 用户]**，然后单击用户的名称。
1. 单击&#x200B;**[!UICONTROL 编辑管理权限]**。
1. 配置用户的管理权限。
1. 单击&#x200B;**[!UICONTROL 下一步]**&#x200B;以查看设置，然后单击&#x200B;**[!UICONTROL 保存]**。

## 支持的浏览器和系统要求 {#concept_CDC4371EB9BF433E9534F8716DC8A088}

Experience Cloud中支持的浏览器。

Experience Cloud支持的浏览器包括：

* [!DNL Microsoft Edge] (Microsoft已 [停止对Internet](https://www.microsoft.com/en-us/WindowsForBusiness/End-of-IE-support) Explorer 8、9和10的支持。 因此，Adobe不会修复针对这些特定版本的Internet Explorer报告的问题。)
* [!DNL Google Chrome]
* [!DNL Firefox]
* [!DNL Safari]
* [!DNL Opera]

**注意：**&#x200B;尽管 Experience Cloud 界面支持这些浏览器，但单个解决方案可能不会支持每个浏览器。（例如，[Analytics](https://docs.adobe.com/content/help/en/analytics/admin/sys-reqs.html) 不支持 [!DNL Opera]，[Target](https://docs.adobe.com/help/en/target/using/implement-target/before-implement/supported-browsers.html) 不支持 [!DNL Safari]。）

**解决方案和产品要求**

* [Analytics](https://docs.adobe.com/content/help/en/analytics/admin/sys-reqs.html)
* [Report Builder](https://docs.adobe.com/content/help/en/analytics/analyze/report-builder/report-builder-setup/system-requirements.html)
* [Adobe Target](https://docs.adobe.com/help/en/target/using/implement-target/before-implement/supported-browsers.html)
