---
description: 实施 Experience Cloud 并成为管理员。该过程使您的解决方案具有现代化功能，如客户属性和受众。
keywords: core services;Customer Attributes
seo-description: 实施 Experience Cloud 并成为管理员。该过程使您的解决方案具有现代化功能，如客户属性和受众。
seo-title: 为核心服务启用 Experience Cloud 解决方案
solution: Experience Cloud
title: 为核心服务启用解决方案
index: true
translation-type: tm+mt
source-git-commit: 0bc7032d0052ba03beac1140dfbfd630e1802bfd
workflow-type: tm+mt
source-wordcount: '2358'
ht-degree: 96%

---


# 为核心服务启用解决方案

对于现有客户，了解如何实现解决方案实施的现代化并实施Experience Cloud，以便您能够使用客户属性和受众等功能。 为此，您将执行以下操作：

1. [加入 Experience Cloud 并成为管理员](#section_2423F0BD3DF642658103310EE5EA6154)
1. [实施 Experience Cloud ID 服务](#section_3C9F6DF37C654D939625BB4D485E4354)
1. [将报表包映射到 Experience Cloud 组织](#section_7B08516B01BA421681DF03D0E86CE3BA)
1. [更新 Analytics AppMeasurement 代码](#section_1798D9D0F05C47E29816AC4EEB9A0913)
1. [更新 Adobe Target 实施](#section_C2F4493C7A36406DAE2266B429A4BD24)
1. [验证核心服务实施](#section_E641782A0F4F44AF8C9C91216BE330D5)
1. [管理用户和产品](#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF)
1. [开始使用核心服务](#section_960C06093623462E8EA247B3E97274A1)

## 步骤 1. 加入 Experience Cloud 并成为管理员 {#section_2423F0BD3DF642658103310EE5EA6154}

加入 Experience Cloud 时需要执行的操作：

![](assets/step1_icon.png) 确保您拥有适当的 Adobe Analytics 或 Adobe Target SKU。

* **Adobe Analytics：** Standard 或 Premium（不是旧版 [!DNL SiteCatalyst] SKU）。
* **Adobe Target：** Standard 或 Premium。

>[!NOTE]
>
>对于 [!DNL Target]，请从 [!DNL mbox.js] 迁移到 at.js。请参阅[从 at.js 1.x 升级到 at.js 2.x](https://docs.adobe.com/content/help/zh-Hans/target/using/implement-target/client-side/upgrading-from-atjs-1x-to-atjs-20.html)。

![](assets/step2_icon.png) 使您的实施符合现代化要求并进行管理员身份配置。

1. 请按照下文[部署 [!UICONTROL Experience Cloud ID 服务]](../core-services/core-services.md#section_3C9F6DF37C654D939625BB4D485E4354)中的步骤执行操作。
1. 请联系您的客户经理，然后开始配置 Experience Cloud。

![](assets/step3_icon.png)在 [!UICONTROL Admin Console] 中管理用户和产品。

### 管理员登录

在成为管理员后，您可以登录 [experiencecloud.adobe.com](https://experiencecloud.adobe.com)。

您将会在 Experience Cloud 菜单导航中看到&#x200B;**[!UICONTROL 管理]**&#x200B;链接。

如需帮助，请参阅 [Experience Cloud 用户和产品管理](../admin-getting-started/admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909)。

### 用户登录

要登录到 Experience Cloud，您的用户必须：

1. 拥有 Adobe ID（或您公司的 Enterprise ID）。
1. 登录到 [experiencecloud.adobe.com](https://experiencecloud.adobe.com)。
1. 属于映射到企业群组的解决方案群组。
1. 如有必要，请将其解决方案帐户关联到 Adobe ID（如下所述）。

![](assets/step4_icon.png)可选：关联现有的用户帐户。

您的用户很有可能已经是解决方案群组的成员，例如先前在 [!UICONTROL Analytics] > [!UICONTROL 管理工具]中管理的 Analytics 群组。

将这些群组映射到 Experience Cloud 企业群组时，这些用户必须手动将其解决方案帐户凭据关联到其 Adobe ID。

请参阅[在 Experience Cloud 中关联帐户](../admin-getting-started/organizations.md#topic_C31CB834F109465A82ED57FF0563B3F1)

>[!NOTE]
>
>在映射企业群组和解决方案群组后，将会自动关联新用户。（将自动创建解决方案凭据，并将凭据关联到其 Adobe ID。）

以下各节介绍如何使实施符合现代化要求。通过使实施符合现代化要求，可在 Experience Cloud 中启用核心服务。

## 步骤 2. 使用 [!UICONTROL Experience Platform Launch] 或 [!UICONTROL Dynamic Tag Management] 实施 [!UICONTROL Experience Cloud ID 服务]。{#section_3C9F6DF37C654D939625BB4D485E4354}

[!UICONTROL Experience Cloud ID 服务]为跨解决方案集成提供了一个通用 ID。它提供了跨域访客标识功能，并为基于通过[!UICONTROL 客户属性]上传的 CRM 数据进行跨设备/浏览器定位和个性化提供了一种途径。

启用 Experience Cloud 核心服务的最简单方法是，通过 [!UICONTROL Experience Platform Launch] 中的 [Experience Cloud ID 服务扩展](https://docs.adobe.com/content/help/zh-Hans/launch/using/implement/solutions/idservice-save.html)或者通过 [!UICONTROL Dynamic Tag Management] 中的 ECID 工具，为 Analytics 和 Adobe Target 自动激活核心服务。（强烈建议使用 Experience Platform Launch。）

![](assets/menu-activation-shell.png)

有关完整的 Experience Cloud ID 服务帮助（以前称为访客 ID），请转到[此处](https://docs.adobe.com/content/help/zh-Hans/id-service/using/home.html)。

**没有使用[!UICONTROL Experience Platform Launch]或[!UICONTROL Dynamic Tag Management]？**

如果您没有使用 [!UICONTROL Experience Platform Launch] 或 [!UICONTROL Dynamic Tag Management]，请通过 JavaScript 部署 ([!DNL VisitorAPI.js]) 手动实施 ID 服务，如下所示：

| 任务 | 描述 |
| -----------| ---------- |  
| [实施适用于 Analytics 的 Experience Cloud ID 服务](https://docs.adobe.com/content/help/zh-Hans/id-service/using/implementation/setup-analytics.html) | Adobe 还建议设置其他[客户 ID](https://docs.adobe.com/content/help/zh-Hans/id-service/using/reference/authenticated-state.html)。这些 ID 与每个访客相关联，并可以启用 Experience Cloud 中现有和未来的功能。 |
| 将现有的 [!DNL s_code] 更新到 H.27.3 或更高版本，或将现有的 [!DNL AppMeasurement.js] 更新到 1.4 或更高版本。 | 这些文件可通过在 Analytics 管理工具的[代码管理器](https://docs.adobe.com/content/help/zh-Hans/analytics/admin/admin-tools/code-manager-admin.html)中下载获得。（如果您需要了解有关 [!DNL AppMeasurement.js] 的更多信息，请参阅 [JavaScript 实施](https://docs.adobe.com/content/help/zh-Hans/analytics/implementation/javascript-implementation/javascript-implementation-overview.html)指南。） |
| 为 Analytics 同步客户 ID | 请参阅 [Analytics - 同步客户 ID](../core-services/core-services.md#section_AD473A6A21C1446498E700363F9A8437)（如下）。 |

## Analytics 和 Target - 同步客户 ID {#section_AD473A6A21C1446498E700363F9A8437}

在设置 Experience Cloud ID 服务时，Adobe 建议您针对 Analytics 和 [!DNL Target] 考虑将自己的[客户 ID](https://docs.adobe.com/content/help/zh-Hans/id-service/using/reference/authenticated-state.html) 与 Experience Cloud 同步。

在 Adobe Target 中，`mbox3rdpartyid` 需要获取客户 ID 并将其发送给 [!DNL Target]。（请参阅 [!DNL Target] 中的[使用客户属性](https://docs.adobe.com/content/help/zh-Hans/target/using/audiences/visitor-profiles/working-with-customer-attributes.html)。）

当访客在您的网站上进行身份验证或以其他方式标识自己时，您的实施必须向页面或应用程序公开此访客的 CRM 客户 ID。然后，您可以使用相应的函数调用将您的客户 ID 同步到 Experience Cloud。此同步会将访客的 CRM 客户 ID 存储在 Experience Cloud 中，并激活该客户的属性以在 Experience Cloud 中使用。

例如，假设 Bob 在您的 CRM 系统中具有客户 ID `52mc210tr42`。当 Bob 在您的网站上进行身份验证时，您必须在该页面上透露此 ID，并使用此 ID 以下面两种方式之一进行同步：

* 使用访客 ID 服务调用 `visitor.setCustomerIDs({"crm_id":"52mc210tr42"})`。或,
* 在 prop 或 eVar 中填充 *`Customer ID (52mc210tr42)`*。

在已知客户 ID 的情况下，必须在每次 [!DNL Analytics] 服务器调用中进行设置。

### Mobile SDK

有关如何在 [Android](https://docs.adobe.com/content/help/zh-Hans/mobile-services/android/overview.html) 和 [iOS](https://docs.adobe.com/content/help/zh-Hans/mobile-services/ios/overview.html) 移动设备应用程序中设置其他客户 ID 的语法示例，请参阅 *Experience Cloud ID 服务*&#x200B;部分。

### 启用历史数据的属性

客户属性数据在访客登录后可用。如果您尚未实施最新的 Experience Cloud ID 服务，并且以前一直在 prop 或 eVar 中跟踪客户 ID，则可以请求一个流程，以将历史登录发送到 Experience Cloud。此流程允许您立即开始使用客户属性。

请联系客户关怀以启用历史数据。

## 步骤 3. 将报表包映射到 Experience Cloud 组织 {#section_7B08516B01BA421681DF03D0E86CE3BA}

Experience Cloud 服务（例如 Experience Cloud ID 服务和[!UICONTROL 人员服务]）与 Experience Cloud 组织相关联，而不是与单个 Analytics 报表包关联。为确保这些服务能够正确运行，必须将每个 Analytics 报表包映射到 Experience Cloud 组织。

请参阅[将报表包映射到组织](report-suite-mapping.md)。

## 步骤 4. (Adobe Analytics) 更新 Analytics AppMeasurement 代码 {#section_1798D9D0F05C47E29816AC4EEB9A0913}

验证您是否位于区域数据收集 (RDC) 中。如果您的数据收集域是 [!DNL omtrdc.net]，或者，如果您的 CNAME 被映射到 [!DNL omtrdc.net]，则您使用的是 RDC。有关更多信息，请参阅[转换到 RDC](https://docs.adobe.com/content/help/zh-Hans/analytics/technotes/rdc/regional-data-collection.html)。如果您使用的是第一方 Cookie，请参阅 [CNAME 和 Experience Cloud ID 服务](https://docs.adobe.com/content/help/zh-Hans/id-service/using/reference/analytics-reference/cname.html)，以获取有关数据收集 CNAME 和跨域跟踪的信息。

建议您更新包括访客 API 在内的 JavaScript 库，以使您的 Analytics 实施现代化。完成此任务的简单方法是在 Dynamic Tag Management 中添加 [!DNL Adobe Analytics] 工具，以指定 *`Automatic`* 作为配置方法。

在 [!UICONTROL Dynamic Tag Management] 中，单击 **[!UICONTROL <Web Property Name>]**>**[!UICONTROL &#x200B;概述&#x200B;]**>**[!UICONTROL &#x200B;添加工具&#x200B;]**>**[!UICONTROL  Adobe Analytics ]**。有关部署信息，请参阅 Dynamic Tag Management 中的[Adobe Analytics 设置](https://docs.adobe.com/content/help/zh-Hans/dtm/using/tools/analytics-dtm.html)。

## 步骤 5. (Adobe Target) 更新 Adobe Target 实施 {#section_C2F4493C7A36406DAE2266B429A4BD24}

* 建议您在 [!UICONTROL Experience Platform Launch] 中添加 [Adobe Target 扩展](https://docs.adobe.com/content/help/zh-Hans/launch/using/extensions-ref/adobe-extension/targetv2-extension/adobe-target-extension-v2.html)，以便自动检索库。您还可以使用 [!UICONTROL Experience Platform Launch] 为 Adobe Target（和其他解决方案）设置 [Experience Cloud ID 服务扩展](https://docs.adobe.com/content/help/zh-Hans/launch/using/extensions-ref/adobe-extension/id-service-extension/overview.html)。Adobe Target **需要**&#x200B;进行 [!UICONTROL Experience Cloud ID 服务]更新才能使用核心服务。（如果使用 [!UICONTROL Dynamic Tag Management]，请添加 [Adobe Target 工具](https://docs.adobe.com/content/help/zh-Hans/dtm/using/tools/target.html)。您还可以使用 [!UICONTROL Dynamic Tag Management] 来为 Adobe Target 部署 Experience Cloud ID 服务。）
* 如果您没有使用 [!UICONTROL Experience Platform Launch] 或 [!UICONTROL Dynamic Tag Management]，请手动[更新 mbox 库](https://docs.adobe.com/content/help/zh-Hans/target/using/implement-target/client-side/mbox-implement/target-download-config-mbox.html)。
* 请求访问权限，以使用 Adobe Analytics 作为 [!DNL Adobe Target] 的报告来源。[!DNL Target]在处理期间， 和 数据将组合在同一服务器调用中，这样两个解决方案之间的访客就可以连接在一起。[!DNL Analytics]请参阅 [Analytics for Target 实施](https://docs.adobe.com/content/help/zh-Hans/target/using/integrate/a4t/a4t.html)。

   >[!IMPORTANT]
   >
   >所有Analytics客户都已配置了核心服务，如客户属性。 如果您不是 Analytics 客户，请联系客户关怀团队以请求进行配置。

## 步骤 6. 验证核心服务实施 {#section_E641782A0F4F44AF8C9C91216BE330D5}

请使用以下流程以确保在您的网站上正确实施 Experience Cloud ID 服务。

1. 清除网站的 Cookie，以便您能够看到对 Experience Cloud ID 服务的请求（请求在首次访问时发生，随后大约每位访客每周发生一次）。
1. 使用一个数据包分析程序或 Web 浏览器调试程序中的网络面板，查找到 [!DNL dpm.demdex.net] 的请求。
1. 验证响应中是否包含 `d_mid` 和一个值，例如：`_setMarketingCloudFields({"d_mid":"4235...`
1. 验证 Analytics 请求是否包含 `mid` 参数 (Experience Cloud ID)。在宽限期内（如果启用），您还应看到 `aid` 参数（Analytics 访客 ID）。

包含 Experience Cloud ID 的预期响应：

![](assets/mac_id_response.png)

包含 Experience Cloud ID（也称为 `mid` 或&#x200B;_访客 ID_）的 Analytics 图像请求：

![](assets/mid.png)

mbox 请求中的 Experience Cloud ID：

![](assets/mbox_request.png)

### 什么是宽限期？

在您部署 Experience Cloud ID 服务后，新的访客将不再从您的数据收集服务器中接收 Analytics Experience Cloud ID。如果您网站的某些部分尚未实施 Experience Cloud ID 服务，那么当访客浏览这些部分时，将无法识别 Experience Cloud ID，与此同时，分配给访客的会是一个旧版 Analytics 访客 ID。这可能会导致潜在的问题，包括重复访问和错误归因。

例如，如果网站的支持部分是在单独的 CMS 中管理的，则此部分可能有不同的 Analytics JavaScript 文件。如果您在将 ID 服务部署到支持网站之前，在主要网站上部署了 Experience Cloud ID，则新访客在访问支持部分时会收到一个旧版 Analytics ID，而且跨两个网站区域的访问都将会报告为不同访问。

在使用多个 JavaScript 文件或其他技术（例如 Flash）的网站上部署 Experience Cloud ID 服务时，可能会导致协调问题，因为您需要同时对网站的所有部分都启用 Experience Cloud ID 服务。通过配置一个宽限期，新的访客可以继续从 ID 服务中接收 Analytics 访客 ID，这样对于网站中没有升级为使用访客 ID 服务的部分而言，也可以始终如一地识别访客。

## 步骤 7. 管理用户和产品 {#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF}

启动并运行后，导航至 [Admin Console](https://adminconsole.adobe.com/)，您可以在其中管理用户和产品配置文件。

![](assets/menu-administration-shell.png)

请参阅 [Experience Cloud 用户和产品管理](../admin-getting-started/admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909)。

### 客户属性

<!-- <p> 
 <note type="important">
  To use the Customer Attributes feature, users must belong to the 
  <span class="term"> Adobe Customer Attributes</span> group, and to solution-level groups (Analytics or Adobe Target). 
 </note> </p> 
 -->

添加到[!UICONTROL 客户属性]群组的用户将在 Experience Cloud 界面的左侧看到[!UICONTROL 客户属性]菜单项。

## 步骤 8. 开始使用核心服务 {#section_960C06093623462E8EA247B3E97274A1}

充分利用以下功能。

![](assets/menu-audiences-shell.png)

### [!UICONTROL 人员] > [!UICONTROL 客户属性]

如果您在客户关系管理 (CRM) 数据库中捕获到企业客户数据，则可以将该数据上传到 Experience Cloud 中的客户属性数据源。上传后，即可在 [!DNL Adobe Analytics] 和 [!DNL Adobe Target] 中利用这些数据。

请参阅[客户属性](../attributes/attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1)。

### [!UICONTROL 人员] > [!UICONTROL 受众库]

Experience Cloud [!UICONTROL 受众]是一个界面，您可以从这里创建受众，合并现有受众以创建组合受众，以及查看所有共享受众。

请参阅[受众](../audience-library/audience-library.md#topic_679810123CAA4E0CA4FA3417FB0100C7)

## 数据存储和隐私披露

如果在 Adobe [!DNL Experience Cloud] 中使用实时受众分析和其他核心服务，那么运用这些服务时，可能会影响存储相关数据的数据中心（和国家/地区）。具体来讲，由于 Adobe [!DNL Experience Cloud] 的核心服务需要利用 Adobe Audience Manager，所以在[!UICONTROL 人员]服务中使用的数据必须存储在位于美国的 Audience Manager 服务器上。

当可以通过[!UICONTROL 人员]服务来利用多种核心服务时，从其他 Adobe 产品向受众管理发送的数据类型包括：

* [!DNL Analytics] 键/值对（prop、eVar、list var 等等）。默认情况下，日志行包含 IP 地址，其中包含 IP 的最后一个八位字节（假定 IP 地址没有被 Adobe [!DNL Analytics] 中的 IP 模糊设置所修改）。
* 根据 Audience Manager 中设置的规则，受众符合资格的特征和区段。
* （可选）您的一个或多个 ID。根据 ID 服务的实施，您可能还会发送一个或多个 ID，例如 CRM ID 或哈希电子邮件地址。如果此数据被发送到 Adobe [!DNL Analytics]，则会转给 Adobe 受众管理。Adobe 不建议将个人数据提交给 Adobe [!DNL Analytics]。而是使用单向哈希对数据进行掩饰，然后再发送给 Adobe。
* 来自 [!DNL Analytics] 通过后端区段共享功能得到的区段。
* 如果未阻止第三方 Cookie，则设置 demdex.net Cookie。`AMCV_###@AdobeOrg` 第一方 Cookie 始终通过 Experience Cloud ID 设置。

所有这些数据元素都将以日志文件的形式传送到 Adobe Audience Manager。Audience Manager 将在美国境内的服务器上处理并存储这些数据。Audience Manager 不提供在美国境外的服务器上存储或处理此数据的选项。

### Cookie 和退出

使用实时受众分析时，不仅需要 [!DNL Analytics] 和 [!DNL Target] 所用的 Cookie，还需要利用 Audience Manager Cookie。

如果您希望向网站访客提供相应的退出选项，则必须将 Audience Manager 退出添加到现有退出过程。

有关说明，请参阅 [Adobe Experience Cloud - 实施 Adobe 退出](https://docs.adobe.com/content/help/zh-Hans/analytics/implementation/javascript-implementation/data-collection/opt-out.html)。

请参阅[数据收集 CNAME 和跨域跟踪](https://docs.adobe.com/content/help/zh-Hans/id-service/using/reference/analytics-reference/cname.html)，以启用跨域跟踪。
