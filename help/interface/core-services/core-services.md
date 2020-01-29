---
description: 实施 Experience Cloud 并成为管理员。此过程可使您的核心服务功能（例如，客户属性和受众）解决方案符合现代化要求。
keywords: core services;customer attributes
seo-description: 实施 Experience Cloud 并成为管理员。此过程可使您的核心服务功能（例如，客户属性和受众）解决方案符合现代化要求。
seo-title: 为核心服务启用 Experience Cloud 解决方案
solution: Experience Cloud
title: 为核心服务启用解决方案
uuid: 5820060f-9b18-4339-81e0-401d964f7a03
translation-type: tm+mt
source-git-commit: 7e2ff64af9b610eafd2e6077012542434a984e6e

---


# 为核心服务启用解决方案

对于现有客户，了解如何使您的解决方案实施现代化并实施Experience Cloud，以便您能够使用客户属性和受众等功能。 要实现此目的，您将：

1. [加入 Experience Cloud 并成为管理员](#section_2423F0BD3DF642658103310EE5EA6154)
1. [实施Experience Cloud ID服务](#section_3C9F6DF37C654D939625BB4D485E4354)
1. [将报表包映射到Experience cloud组织](#section_7B08516B01BA421681DF03D0E86CE3BA)
1. [更新Analytics appMeasurement代码](#section_1798D9D0F05C47E29816AC4EEB9A0913)
1. [更新Adobe Target实施](#section_C2F4493C7A36406DAE2266B429A4BD24)
1. [验证核心服务实施](#section_E641782A0F4F44AF8C9C91216BE330D5)
1. [管理用户和产品](#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF)
1. [开始使用核心服务](#section_960C06093623462E8EA247B3E97274A1)

<!-- <p>https://marketing-beta.adobe.com/resources/help/core/core-services.html </p> 
<p>https://adobe.sharepoint.com/sites/AGSConsulting/CoreServices/PA/_layouts/15/start.aspx#/ </p> -->

<!-- Core services architecture and data flow wiki: https://wiki.corp.adobe.com/pages/viewpage.action?pageId=1004285689 -->

## 步骤 1. 加入 Experience Cloud 并成为管理员 {#section_2423F0BD3DF642658103310EE5EA6154}

加入 Experience Cloud 时需要执行的操作：

![](assets/step1_icon.png) 确保您拥有适当的 Adobe Analytics 或 Adobe Target SKU。

* **Adobe Analytics：** Standard 或 Premium 版本（而非旧版 SiteCatalyst SKU）。
* **Adobe Target：** Standard 或 Premium 版本。

>[!NOTE]
>
>对于Target，从mbox.js迁移到at.js。 请参 [阅从at.js 1升级。 x至at.js 2。 x](https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/upgrading-from-atjs-1x-to-atjs-20.html).

![](assets/step2_icon.png) 使您的实施符合现代化要求并进行管理员身份配置。


1. 按照下面[部署 Experience Cloud ID 服务](../core-services/core-services.md#section_3C9F6DF37C654D939625BB4D485E4354)中的步骤进行操作。
1. 联系您的帐户管理员，开始 Experience Cloud 的配置过程。

![](assets/step3_icon.png)[!UICONTROL  在管理控制台中管理用户和产品].

**管理员访问权限**

After you are an administrator, you can log in at [experiencecloud.adobe.com](https://experiencecloud.adobe.com).

您将会在 Experience Cloud 菜单导航中看到&#x200B;**[!UICONTROL 管理]**链接。

如需帮助，请参阅 [Experience Cloud 用户和产品管理](../admin-getting-started/admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909)。

**用户访问**

要登录到 Experience Cloud，您的用户必须：


1. 拥有 Adobe ID。
1. Sign in at [experiencecloud.adobe.com](https://experiencecloud.adobe.com).
1. 属于映射到企业群组的解决方案群组。
1. 如有必要，可将他们的解决方案帐户关联到其 Adobe ID（如下所述）。

![](assets/step4_icon.png)可选：关联现有的用户帐户。

Most likely, you have users who are already members of solution groups, such an Analytics group that you previously managed in [!UICONTROL Analytics] > [!UICONTROL Admin Tools].

当您将这些群组映射到 Experience Cloud 企业群组时，这些用户必须手动将其解决方案帐户凭据关联到其 Adobe ID。

请参阅[在 Experience Cloud 中关联帐户](../admin-getting-started/organizations.md#topic_C31CB834F109465A82ED57FF0563B3F1)

> [!NOTE]
> 
> 在映射企业群组和解决方案群组后，将会自动关联新用户。（将自动创建解决方案凭据并将这些凭据关联到其 Adobe ID。）

以下各部分描述了如何使您的实施符合现代化要求。在使您的实施符合现代化要求后，可以在 Experience Cloud 中启用核心服务。

## 步骤 2. 使用 [!UICONTROL Experience Platform Launch] 或动态标签管理 [!UICONTROL ，实]施Experience Cloud ID [!UICONTROL 服务]{#section_3C9F6DF37C654D939625BB4D485E4354}

Experience Cloud ID服 [!UICONTROL 务为跨解决方案集成] ，提供了通用ID。 它提供跨域访客识别和跨设备／浏览器定位和基于通过客户属性上传的CRM数据的个性化 [!UICONTROL 路径]。

The simplest method for enabling Experience Cloud core services is to activate it automatically for Analytics and Target via the [Experience Cloud ID service tool](https://docs.adobe.com/content/help/en/launch/using/implement/solutions/idservice-save.html) in [!UICONTROL Experience Platform Launch], or [!UICONTROL Dynamic Tag Management]. （强烈建议使用Experience Platform Launch。）

![](assets/menu-activation-shell.png)

For complete Experience Cloud ID service help (formerly, visitor ID), go [here](https://docs.adobe.com/content/help/en/id-service/using/home.html).

**不使用[!UICONTROL Experience Platform Launch]或[!UICONTROL 动态标签管理]?**

If you are not using [!UICONTROL Experience Platform Launch] or [!UICONTROL Dynamic Tag Management], manually implement the ID service via the JavaScript Deployment ([!DNL VisitorAPI.js]), as follows:

| 任务 | 描述 |
| -----------| ---------- |  
| [实施适用于 Analytics 的 Experience Cloud ID 服务](https://docs.adobe.com/content/help/en/id-service/using/implementation/setup-analytics.html) | Adobe 还建议设置其他[客户 ID](https://docs.adobe.com/content/help/en/id-service/using/reference/authenticated-state.html)。这些ID与每个访客关联，可在Experience cloud中启用当前和未来功能。 |
| 将现有的 [!DNL s_code] 更新到 H.27.3 或更高版本，或将现有的 [!DNL AppMeasurement.js] 更新到 1.4 或更高版本。 | 这些文件在 Analytics 管理工具的[代码管理器](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/code-manager-admin.html)中提供下载。（如果您需要了解有关 [ 的更多信息，请参阅 ](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/javascript-implementation-overview.html)JavaScript 实施[!DNL AppMeasurement.js]指南。） |
| 同步Analytics的客户ID | 请参阅 [Analytics - 同步客户 ID](../core-services/core-services.md#section_AD473A6A21C1446498E700363F9A8437)（见下文）。 |

## Analytics 和 Target - 同步客户 ID {#section_AD473A6A21C1446498E700363F9A8437}

As a part of setting up the Experience Cloud ID service, Adobe recommends for Analytics and [!DNL Target] that you synchronize your [customer IDs](https://docs.adobe.com/content/help/en/id-service/using/reference/authenticated-state.html) with the Experience Cloud.

In Adobe Target, the `mbox3rdpartyid` needs to get the customer ID and send it to [!DNL Target]. (See [Working with Customer Attributes](https://docs.adobe.com/content/help/en/target/using/audiences/visitor-profiles/working-with-customer-attributes.html) in [!DNL Target].)

当访客在您的网站上进行身份验证或识别自身时，您的实施必须将此人的 CRM 客户 ID 透露给页面或应用程序。然后，您可以使用适当的函数调用，将您的客户 ID 与 Experience Cloud 同步。此同步会将访客的 CRM 客户 ID 存储在 Experience Cloud 中，并激活该客户的属性以便在 Experience Cloud 中使用。

例如，假设 Bob 在您的 CRM 系统中具有客户 ID `52mc210tr42`。当 Bob 在您的网站上进行身份验证时，您必须在该页面上透露此 ID，并使用此 ID 以下面两种方式之一进行同步：

* 使用访客 ID 服务调用 `visitor.setCustomerIDs({"crm_id":"52mc210tr42"})`。或，
* 在 prop 或 eVar 中填写&#x200B;*`Customer ID (52mc210tr42)`*。

在已知客户 ID 的情况下，必须在每次 [!DNL Analytics] 服务器调用中进行设置。

### Mobile SDK

有关如何 *在Android和* iOS [](https://docs.adobe.com/content/help/en/mobile-services/android/overview.html)[](https://docs.adobe.com/content/help/en/mobile-services/ios/overview.html) Mobile应用程序中设置其他客户ID的语法示例，请参阅Experience Cloud ID服务部分。

### 启用历史数据的属性

访客登录后，客户属性数据将变为可用状态。如果您尚未实施最新的 Experience Cloud ID 服务，并且以前一直在跟踪 prop 或 eVar 中的客户 ID，则可以请求一个流程，将历史登录信息发送至 Experience Cloud。此流程允许您立即开始使用客户属性。

联系客户关怀以启用历史数据。

## 步骤 3. Map report suites to an Experience Cloud Organization {#section_7B08516B01BA421681DF03D0E86CE3BA}

Experience Cloud services (such as Experience Cloud ID service and the [!UICONTROL People service]) are associated with an Experience Cloud organization instead of an individual Analytics report suite. 要确保这些服务能够正常运行，必须将每个 Analytics 报表包映射到 Experience Cloud 组织。

请参阅[将报表包映射到组织](report-suite-mapping.md)。

## 步骤 4. (Adobe Analytics) Update your Analytics AppMeasurement code {#section_1798D9D0F05C47E29816AC4EEB9A0913}

验证您是否位于区域数据收集 (RDC) 中。如果您的数据收集域是 [!DNL omtrdc.net]，或者，如果您的 CNAME 被映射到 [!DNL omtrdc.net]，则您使用的是 RDC。请参阅[过渡到 RDC](https://docs.adobe.com/content/help/en/analytics/technotes/rdc/regional-data-collection.html)，以了解详细信息。If you are using first-party cookies, refer to [CNAME and the Experience Cloud ID Service](https://docs.adobe.com/content/help/en/id-service/using/reference/analytics-reference/cname.html) for information about data collection CNAMEs and cross-domain tracking.

建议您更新包括访客 API 在内的 JavaScript 库，以使您的 Analytics 实施现代化。完成此任务的简单方法是在 Dynamic Tag Management 中添加 [!DNL Adobe Analytics] 工具，以指定 *`Automatic`*作为配置方法。

In [!UICONTROL Dynamic Tag Management], click **[!UICONTROL <Web Property Name>]** > **[!UICONTROL 概述]**>**[!UICONTROL &#x200B;添加工具]** > **[!UICONTROL Adobe Analytics]**。请参阅动态标签管理中的[Adobe Analytics 设置](https://docs.adobe.com/content/help/en/dtm/using/tools/analytics-dtm.html)，以了解部署信息。

## 步骤 5. (Adobe Target) Update your Adobe Target implementation {#section_C2F4493C7A36406DAE2266B429A4BD24}

* It is recommended that you add an [Adobe Target extension](https://docs.adobe.com/content/help/en/launch/using/extensions-ref/adobe-extension/targetv2-extension/adobe-target-extension-v2.html) in [!UICONTROL Experience Platform Launch], so that your library retrieval is automatic. 您还可以使用 [Experience Platform Launch为Target](https://docs.adobe.com/content/help/en/launch/using/extensions-ref/adobe-extension/id-service-extension/overview.html) （和其他解决方案）设置 [!UICONTROL Experience Cloud ID服务扩展]。 The [!UICONTROL Experience Cloud ID service] update **is required** for [!UICONTROL Target] to use core services. (如果您使用 [!UICONTROL 动态标签管理]，请添加 [Adobe Target工具](https://docs.adobe.com/content/help/en/dtm/using/tools/target.html)。 You can also use [!UICONTROL Dynamic Tag Management] to deploy the Experience Cloud ID service for Target.)
* 如果您没有使用 [!UICONTROL Experience Platform Launch] 或 [!UICONTROL Dynamic Tag Management]，请手 [动更新mbox库](https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/mbox-implement/target-download-config-mbox.html) 。
* Request access to use Adobe Analytics as the reporting source for [!DNL Adobe Target]. [!DNL Target]在处理期间， 和 数据将组合在同一服务器调用中，这样两个解决方案之间的访客就可以连接在一起。[!DNL Analytics]请参阅[为 Target 实施使用 Analytics](https://docs.adobe.com/content/help/en/target/using/integrate/a4t/a4t.html)。

   >[!IMPORTANT]
   >
   >所有Analytics客户都已针对核心服务（如客户属性）进行配置。 如果您不是 Analytics 客户，请联系客户关怀团队以请求进行配置。

## 步骤 6. 验证核心服务实施 {#section_E641782A0F4F44AF8C9C91216BE330D5}

使用下面的流程确保在您的网站上正确实施 Experience Cloud ID 服务。

1. 清除您网站上的 Cookie，这样可以看到对 Experience Cloud ID 服务的请求（该请求出现在第一次访问时，随后大约每周在每个访客访问时出现一次）。
1. 使用一个数据包分析程序或 Web 浏览器调试程序中的网络面板，查找到 [!DNL dpm.demdex.net] 的请求。
1. 验证响应中是否包含 `d_mid` 和一个值，例如：`_setMarketingCloudFields({"d_mid":"4235...`
1. Verify that the Analytics request contains the `mid` parameter (the Experience Cloud ID). During the grace period (if it is enabled), you should also see an `aid` parameter (the Analytics visitor ID).

包含 Experience Cloud ID 的预期响应：

![](assets/mac_id_response.png)

包含Experience Cloud ID（也称为或访客ID）的分 `mid` 析图 _像请求_:

![](assets/mid.png)

mbox 请求中的 Experience Cloud ID：

![](assets/mbox_request.png)

**什么是宽限期？**

在您部署Experience Cloud ID服务后，新访客不再从您的数据收集服务器接收Analytics Experience Cloud ID。 如果您网站的某些部分尚未实施 Experience Cloud ID 服务，那么当访客浏览这些部分时，将无法识别 Experience Cloud ID，与此同时，分配给访客的会是一个旧版 Analytics 访客 ID。这可能会引起潜在的问题，包括访问重复计数和属性错误。

例如，如果您网站的支持部分是在单独的 CMS 中进行管理，则应有一个单独的 Analytics JavaScript 文件负责处理此部分。如果您在将ID服务部署到支持站点之前在主站点上部署Experience Cloud ID，则新访客在访问支持部分时会收到一个旧版Analytics ID，并且跨两个站点部分的访问会报告为不同的访问。

在使用多个JavaScript文件或其他技术（如Flash）的站点上部署Experience Cloud ID服务可能会导致协调问题，因为您需要同时在站点的所有部分上启用Experience Cloud ID服务。 通过配置宽限期，新访客可继续从ID服务接收Analytics访客ID，这样，在尚未升级为使用访客ID服务的站点部分可以一致地识别访客。

## 步骤 7. 管理用户和产品 {#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF}

Once you are up and running, navigate to the [Admin Console](https://adminconsole.adobe.com/), where you can manage users and product profiles.

![](assets/menu-administration-shell.png)

请参阅 [Experience Cloud 用户和产品管理](../admin-getting-started/admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909)。

**客户属性**

<!-- <p> 
 <note type="important">
  To use the Customer Attributes feature, users must belong to the 
  <span class="term"> Adobe Customer Attributes</span> group, and to solution-level groups (Analytics or Target). 
 </note> </p> 
 -->

Users that are added to the [!UICONTROL Customer Attributes] group will see the [!UICONTROL Customer Attributes] menu item on the left side of the Experience Cloud interface

## 步骤 8. Begin using core services {#section_960C06093623462E8EA247B3E97274A1}

充分利用以下核心服务功能。

![](assets/menu-audiences-shell.png)

**[!UICONTROL “人员]”>“客[!UICONTRO户属性”]**

如果您在客户关系管理 (CRM) 数据库中捕获到企业客户数据，则可以将该数据上传到 Experience Cloud 中的客户属性数据源。上传后，即可在 [!DNL Adobe Analytics] 和 [!DNL Adobe Target] 中利用这些数据。

请参阅[客户属性](../attributes/attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1)。

**[!UICONTROL “人物]”>“[!UICONTROL 受众库”]**

Experience Cloud [!UICONTROL Audiences] is the interface that lets you create audiences, combine existing audiences to create composite audiences, and view all shared audiences.

请参阅[受众](../audience-library/audience-library.md#topic_679810123CAA4E0CA4FA3417FB0100C7)

<!-- aam_mc.xml -->

## 数据存储和隐私泄露

如果在 Adobe [!DNL Experience Cloud] 中使用实时受众分析和其他核心服务，那么运用这些服务时，可能会影响存储相关数据的数据中心（和国家/地区）。Specifically, because the core services of the Adobe [!DNL Experience Cloud] leverage Adobe Audience Manager, data used within the [!UICONTROL People] service must reside within Audience Manager servers in the United States.

When leveraging core services made available via the [!UICONTROL People] service, the types of data sent from other Adobe products to audience management are:

* [!DNL Analytics] 键/值对（prop、eVar、list var 等等）。默认情况下，日志行包含 IP 地址，其中包含 IP 的最后一个八位字节（假定 IP 地址没有被 Adobe [!DNL Analytics] 中的 IP 模糊设置所修改）。
* 根据 Audience Manager 中设定的规则，访客所符合的特征和区段。
* （可选）您的一个或多个 ID。根据您实施的 ID 服务，可能还需要发送一个或多个 ID，例如 CRM ID 或哈希电子邮件地址。如果此数据被发送到 Adobe [!DNL Analytics]，则会转给 Adobe 受众管理。Adobe 不建议将个人数据提交给 Adobe [!DNL Analytics]。而是使用单向哈希对数据进行伪装，然后再发送给 Adobe。
* 来自 [!DNL Analytics] 通过后端区段共享功能得到的区段。
* 如果未阻止第三方 Cookie，则设置 demdex.net Cookie。The `AMCV_###@AdobeOrg` first-party cookie is always set with the Experience Cloud ID service.

所有这些数据元素都会以日志文件的形式提供给 Adobe Audience Manager。Audience Manager 在美国境内处理和存储此数据。Audience Manager 不在美国以外的位置存储或处理此数据。

**Cookie 和退出**

使用实时受众分析时，不仅需要 [!DNL Analytics] 和 [!DNL Target] 所用的 Cookie，还需要利用 Audience Manager Cookie。

如果您希望向网站访客提供相应的退出选项，则必须将 Audience Manager 退出添加到现有退出过程。

请参阅 [Adobe Experience Cloud - 实施 Adobe 退出](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/data-collection/opt-out.html)，以了解相关说明。

请参阅[数据收集 CNAME 和跨域跟踪](https://docs.adobe.com/content/help/en/id-service/using/reference/analytics-reference/cname.html)，以了解如何启用跨域跟踪。
