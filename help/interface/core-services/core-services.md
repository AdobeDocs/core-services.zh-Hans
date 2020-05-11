---
description: 实施Experience Cloud并成为管理员。 该过程使您的解决方案具有现代化功能，如客户属性和受众。
keywords: core services;Customer Attributes
seo-description: 实施Experience Cloud并成为管理员。 该过程使您的解决方案具有现代化功能，如客户属性和受众。
seo-title: 为核心服务启用 Experience Cloud 解决方案
solution: Experience Cloud
title: 为核心服务启用解决方案
index: true
translation-type: tm+mt
source-git-commit: 0bc7032d0052ba03beac1140dfbfd630e1802bfd
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# 为核心服务启用解决方案

对于现有客户，了解如何实现解决方案实施的现代化并实施Experience Cloud，以便您能够使用客户属性和受众等功能。 要完成此操作，您将：

1. [加入 Experience Cloud 并成为管理员](#section_2423F0BD3DF642658103310EE5EA6154)
1. [实施Experience Cloud ID服务](#section_3C9F6DF37C654D939625BB4D485E4354)
1. [将报表包映射到Experience Cloud组织](#section_7B08516B01BA421681DF03D0E86CE3BA)
1. [更新Analytics AppMeasurement代码](#section_1798D9D0F05C47E29816AC4EEB9A0913)
1. [更新Adobe目标实施](#section_C2F4493C7A36406DAE2266B429A4BD24)
1. [验证核心服务实施](#section_E641782A0F4F44AF8C9C91216BE330D5)
1. [管理用户和产品](#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF)
1. [开始使用核心服务](#section_960C06093623462E8EA247B3E97274A1)

## 步骤 1. 加入 Experience Cloud 并成为管理员 {#section_2423F0BD3DF642658103310EE5EA6154}

加入 Experience Cloud 时需要执行的操作：

![](assets/step1_icon.png) 确保您拥有适当的 Adobe Analytics 或 Adobe Target SKU。

* **Adobe Analytics:** 标准版或高级版(不是旧 [!DNL SiteCatalyst] 版SKU)。
* **Adobe目标:** 标准版或高级版。

>[!NOTE]
>
>对 [!DNL Target]于，从迁移到at.js [!DNL mbox.js]。 See [Upgrading from at.js 1. x to at.js 2. x](https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/upgrading-from-atjs-1x-to-atjs-20.html).

![](assets/step2_icon.png) 使您的实施符合现代化要求并进行管理员身份配置。

1. 请按照以下步 [骤部署 [!UICONTROL Experience Cloud ID服务]](../core-services/core-services.md#section_3C9F6DF37C654D939625BB4D485E4354)。
1. 联系您的客户经理并开始Experience Cloud的配置过程。

![](assets/step3_icon.png) 在Admin Console中管理用户 [!UICONTROL 和产品]。

### 管理员登录

After you are an administrator, you can log in at [experiencecloud.adobe.com](https://experiencecloud.adobe.com).

您将会在 Experience Cloud 菜单导航中看到&#x200B;**[!UICONTROL 管理]**&#x200B;链接。

如需帮助，请参阅 [Experience Cloud 用户和产品管理](../admin-getting-started/admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909)。

### 用户登录

要登录Experience Cloud，您的用户必须：

1. 拥有Adobe ID(或适用于您的公司的Enterprise ID)。
1. Sign in at [experiencecloud.adobe.com](https://experiencecloud.adobe.com).
1. 属于映射到企业组的解决方案组。
1. 如有必要，将其解决方案帐户链接到其Adobe ID（如下所述）。

![](assets/step4_icon.png)可选：关联现有的用户帐户。

您的用户很可能已是解决方案组(例如您之前在Analytics >管理工具中管理的 [!UICONTROL Analytics] 组) [!UICONTROL 的成员]。

将这些组映射到Experience Cloud企业组时，这些用户必须手动将其解决方案帐户凭据关联到其Adobe ID。

请参 [阅在Experience Cloud中关联帐户](../admin-getting-started/organizations.md#topic_C31CB834F109465A82ED57FF0563B3F1)

>[!NOTE]
>
>在映射企业群组和解决方案群组后，将会自动关联新用户。（解决方案凭据将自动创建并链接到其Adobe ID。）

以下各节介绍如何使您的实施现代化。 实施现代化可在Experience Cloud中实现核心服务。

## 步骤 2. 使用 [!UICONTROL Experience Platform Launch] 或动 [!UICONTROL 态标签管理实][!UICONTROL 施Experience Cloud ID服务] {#section_3C9F6DF37C654D939625BB4D485E4354}

Experience [!UICONTROL Cloud ID服务提供] 通用ID进行跨解决方案集成。 它提供跨域访客标识和跨设备／浏览器定位和基于通过客户属性上传的CRM数据的 [!UICONTROL 个性化路径]。

启用Experience Cloud核心服务的最简单方法是通过Experience Platform Launch中的 [Experience Cloud ID Service扩展](https://docs.adobe.com/content/help/zh-Hans/launch/using/implement/solutions/idservice-save.html) ，或通 [!UICONTROL 过动态标签管理中的ECID工具为Analytics和Adobe][!UICONTROL 目标自动]激活它。 （强烈建议使用Experience Platform Launch。）

![](assets/menu-activation-shell.png)

有关完整的Experience Cloud ID服务帮助(以前称为访客ID)，请转 [到此处](https://docs.adobe.com/content/help/zh-Hans/id-service/using/home.html)。

**未使用[!UICONTROL Experience Platform Launch]或[!UICONTROL 动态标签管理]?**

If you are not using [!UICONTROL Experience Platform Launch] or [!UICONTROL Dynamic Tag Management], manually implement the ID service via the JavaScript Deployment ([!DNL VisitorAPI.js]), as follows:

| 任务 | 描述 |
| -----------| ---------- |  
| [实施适用于 Analytics 的 Experience Cloud ID 服务](https://docs.adobe.com/content/help/en/id-service/using/implementation/setup-analytics.html) | Adobe还建议设置其 [他客户ID](https://docs.adobe.com/content/help/zh-Hans/id-service/using/reference/authenticated-state.html)。 这些ID与每个访客关联，可在Experience Cloud中启用当前和未来功能。 |
| 将现有的 [!DNL s_code] 更新到 H.27.3 或更高版本，或将现有的 [!DNL AppMeasurement.js] 更新到 1.4 或更高版本。 | 这些文件可在Analytics Admin Tools的代码 [管理器](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/code-manager-admin.html) 中下载。  (如果 [您需要有关的更多信息](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/javascript-implementation-overview.html) ，可参阅《JavaScript实施指南 [!DNL AppMeasurement.js]》。) |
| 同步Analytics的客户ID | See [Analytics - synching the customer ID](../core-services/core-services.md#section_AD473A6A21C1446498E700363F9A8437) (below). |

## Analytics &amp; Adobe Target - synching the customer ID {#section_AD473A6A21C1446498E700363F9A8437}

As a part of setting up the Experience Cloud ID Service, Adobe recommends for Analytics and [!DNL Target] that you synchronize your [customer IDs](https://docs.adobe.com/content/help/zh-Hans/id-service/using/reference/authenticated-state.html) with the Experience Cloud.

In Adobe Target, the `mbox3rdpartyid` needs to get the customer ID and send it to [!DNL Target]. (请参 [阅中的使用客户](https://docs.adobe.com/content/help/zh-Hans/target/using/audiences/visitor-profiles/working-with-customer-attributes.html) 属 [!DNL Target]性。)

当访客在您的网站上进行身份验证或以其他方式识别自己时，您的实施必须将该人的CRM客户ID公开给页面或应用程序。 然后，您可以使用相应的函数调用将您的客户ID同步到Experience Cloud。 此同步将访客的CRM客户ID存储在Experience Cloud中，并激活该客户的属性以在Experience Cloud中使用。

例如，假设 Bob 在您的 CRM 系统中具有客户 ID `52mc210tr42`。当 Bob 在您的网站上进行身份验证时，您必须在该页面上透露此 ID，并使用此 ID 以下面两种方式之一进行同步：

* 使用访客 ID 服务调用 `visitor.setCustomerIDs({"crm_id":"52mc210tr42"})`。或,
* 在prop *`Customer ID (52mc210tr42)`* 或eVar中填充。

在已知客户 ID 的情况下，必须在每次 [!DNL Analytics] 服务器调用中进行设置。

### Mobile SDK

有关如何 *在Android和iOS* Mobile应用程序中设置其他客户ID的语法示例，请参 [阅Experience Cloud](https://docs.adobe.com/content/help/zh-Hans/mobile-services/android/overview.html) ID [服务部分](https://docs.adobe.com/content/help/zh-Hans/mobile-services/ios/overview.html) 。

### 启用历史数据的属性

客户属性数据在访客登录后可用。 如果您尚未实施最新的Experience Cloud ID服务，并且您过去一直在prop或eVar中跟踪客户ID，则可以请求一个流程，将历史登录发送到Experience Cloud。 此流程允许您立即开始使用客户属性。

联系客户关怀以启用历史数据。

## 步骤 3. Map report suites to an Experience Cloud Organization {#section_7B08516B01BA421681DF03D0E86CE3BA}

Experience Cloud服务(如Experience Cloud ID服务和人 [!UICONTROL 员服务])与Experience Cloud组织相关联，而不是与单个Analytics报表包相关联。 要确保这些服务能够正确运行，必须将每个Analytics报告套件映射到Experience Cloud组织。

请参阅[将报表包映射到组织](report-suite-mapping.md)。

## 步骤 4. (Adobe Analytics) Update your Analytics AppMeasurement code {#section_1798D9D0F05C47E29816AC4EEB9A0913}

验证您是否位于区域数据收集 (RDC) 中。如果您的数据收集域是 [!DNL omtrdc.net]，或者，如果您的 CNAME 被映射到 [!DNL omtrdc.net]，则您使用的是 RDC。有关 [详细信息](https://docs.adobe.com/content/help/en/analytics/technotes/rdc/regional-data-collection.html) ，请参阅转换到RDC。 如果您使用第一方Cookie，请参 [阅CNAME和Experience Cloud ID服务](https://docs.adobe.com/content/help/zh-Hans/id-service/using/reference/analytics-reference/cname.html) ，了解有关数据收集CNAME和跨域跟踪的信息。

建议您更新包括访客 API 在内的 JavaScript 库，以使您的 Analytics 实施现代化。完成此任务的简单方法是在 Dynamic Tag Management 中添加 [!DNL Adobe Analytics] 工具，以指定 *`Automatic`* 作为配置方法。

In [!UICONTROL Dynamic Tag Management], click **[!UICONTROL <Web Property Name>]**>概**[!UICONTROL &#x200B;述&#x200B;]**>**[!UICONTROL &#x200B;添加工具&#x200B;]**>**[!UICONTROL  Adobe Analytics ]**。 有关[部署信息，请参阅](https://docs.adobe.com/content/help/en/dtm/using/tools/analytics-dtm.html)“动态标签管理”中的Adobe Analytics设置。

## 步骤 5. (Adobe Target) Update your Adobe Target implementation {#section_C2F4493C7A36406DAE2266B429A4BD24}

* 建议您在Experience Platform Launch [中添加](https://docs.adobe.com/content/help/en/launch/using/extensions-ref/adobe-extension/targetv2-extension/adobe-target-extension-v2.html)Adobe目标扩展，以便库检索自动进行。 您还可以使用Experience Platform Launch [为Adobe目标](https://docs.adobe.com/content/help/zh-Hans/launch/using/extensions-ref/adobe-extension/id-service-extension/overview.html) （和其他解决方案）设 [!UICONTROL 置Experience Cloud ID服务扩展]。 Adobe [!UICONTROL 目标使用核] 心服 **务需要** Experience Cloud ID服务更新。 (如果您使用 [!UICONTROL 动态标签管理]，请添加 [Adobe目标工具](https://docs.adobe.com/content/help/en/dtm/using/tools/target.html)。 您还可以使 [!UICONTROL 用动态标签] 管理来部署Experience Cloud ID服务，用于Adobe目标。)
* 如果您未使用Experience [!UICONTROL Platform Launch] 或 [!UICONTROL Dynamic Tag Management]，请 [手动更新mbox库](https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/mbox-implement/target-download-config-mbox.html) 。
* Request access to use Adobe Analytics as the reporting source for [!DNL Adobe Target]. [!DNL Target]在处理期间， 和 数据将组合在同一服务器调用中，这样两个解决方案之间的访客就可以连接在一起。[!DNL Analytics]See [Analytics for Target Implementation](https://docs.adobe.com/content/help/zh-Hans/target/using/integrate/a4t/a4t.html).

   >[!IMPORTANT]
   >
   >所有Analytics客户都已配置了核心服务，如客户属性。 如果您不是 Analytics 客户，请联系客户关怀团队以请求进行配置。

## 步骤 6. 验证核心服务实施 {#section_E641782A0F4F44AF8C9C91216BE330D5}

请使用以下过程确保在您的站点上正确实施Experience Cloud ID服务。

1. 清除网站的cookie，以便您能够看到Experience Cloud ID服务的请求(请求在首次访问时发生，然后每周大约一次访客)。
1. Using a packet analyzer or the network panel in a web browser debugger, look for a request going to [!DNL dpm.demdex.net].
1. 验证响应中是否包含 `d_mid` 和一个值，例如：`_setMarketingCloudFields({"d_mid":"4235...`
1. 验证Analytics请求是否包 `mid` 含参数(Experience Cloud ID)。 在宽限期内（如果启用），您还应看到一 `aid` 个参数(分析访客ID)。

需要包含Experience Cloud ID的响应：

![](assets/mac_id_response.png)

包含Experience Cloud ID(也称为或访客ID)的 `mid` 分析 _图像请求_:

![](assets/mid.png)

mbox请求中的Experience Cloud ID:

![](assets/mbox_request.png)

### 宽限期是什么？

在您部署Experience Cloud ID服务后，新访客不再从您的数据收集服务器接收Analytics Experience Cloud ID。 如果您网站的各个部分尚未实施Experience Cloud ID服务，则当访客浏览到这些部分时，将无法识别Experience Cloud ID，并为访客分配了旧版Analytics访客ID。 这可能导致潜在问题，包括重复访问和错误归因。

例如，如果站点的支持部分是在单独的CMS中管理的，则此部分可能有一个不同的Analytics JavaScript文件。 如果您在将ID服务部署到支持站点之前在主站点上部署Experience Cloud ID，新访客在访问支持部分时会收到一个旧版Analytics ID，跨两个站点部分的访问将报告为不同的访问。

在使用多个JavaScript文件或其他技术（如Flash）的站点上部署Experience Cloud ID服务可能会导致协调问题，因为您需要同时在站点的所有部分上启用Experience Cloud ID服务。 通过配置宽限期，新访客可以继续从ID服务接收Analytics访客ID，因此，在尚未升级为使用访客ID服务的站点部分可以一致地识别访客。

## 步骤 7. 管理用户和产品 {#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF}

Once you are up and running, navigate to the [Admin Console](https://adminconsole.adobe.com/), where you can manage users and product profiles.

![](assets/menu-administration-shell.png)

请参阅 [Experience Cloud 用户和产品管理](../admin-getting-started/admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909)。

### 客户属性

<!-- <p> 
 <note type="important">
  To use the Customer Attributes feature, users must belong to the 
  <span class="term"> Adobe Customer Attributes</span> group, and to solution-level groups (Analytics or Adobe Target). 
 </note> </p> 
 -->

Users that are added to the [!UICONTROL Customer Attributes] group will see the [!UICONTROL Customer Attributes] menu item on the left side of the Experience Cloud interface.

## 步骤 8. Begin using core services {#section_960C06093623462E8EA247B3E97274A1}

充分利用以下功能。

![](assets/menu-audiences-shell.png)

### [!UICONTROL “人员] ”>“ [!UICONTROL 客户属性”]

如果您在客户关系管理 (CRM) 数据库中捕获到企业客户数据，则可以将该数据上传到 Experience Cloud 中的客户属性数据源。上传后，即可在 [!DNL Adobe Analytics] 和 [!DNL Adobe Target] 中利用这些数据。

请参阅[客户属性](../attributes/attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1)。

### [!UICONTROL 人物] > [!UICONTROL 受众库]

Experience Cloud [!UICONTROL Audiences] is the interface that lets you create audiences, combine existing audiences to create composite audiences, and view all shared audiences.

请参阅[受众](../audience-library/audience-library.md#topic_679810123CAA4E0CA4FA3417FB0100C7)

## 数据存储和隐私泄露

如果在 Adobe [!DNL Experience Cloud] 中使用实时受众分析和其他核心服务，那么运用这些服务时，可能会影响存储相关数据的数据中心（和国家/地区）。Specifically, because the core services of the Adobe [!DNL Experience Cloud] leverage Adobe Audience Manager, data used within the [!UICONTROL People] service must reside within Audience Manager servers in the United States.

When leveraging core services made available via the [!UICONTROL People] service, the types of data sent from other Adobe products to audience management are:

* [!DNL Analytics] 键/值对（prop、eVar、list var 等等）。默认情况下，日志行包含 IP 地址，其中包含 IP 的最后一个八位字节（假定 IP 地址没有被 Adobe [!DNL Analytics] 中的 IP 模糊设置所修改）。
* 根据访客管理器中设置的规则，受众有资格获得的特征和区段。
* （可选）您的一个或多个ID。 根据您对ID服务的实施，您可能还在发送一个或多个ID，如CRM ID或散列电子邮件地址。 如果此数据被发送到 Adobe [!DNL Analytics]，则会转给 Adobe 受众管理。Adobe 不建议将个人数据提交给 Adobe [!DNL Analytics]。相反，在将数据发送到Adobe之前，使用单向哈希来掩码数据。
* 来自 [!DNL Analytics] 通过后端区段共享功能得到的区段。
* 如果未阻止第三方 Cookie，则设置 demdex.net Cookie。The `AMCV_###@AdobeOrg` first-party cookie is always set with the Experience Cloud ID Service.

所有这些数据元素都以日志文件的形式提供给Adobe受众管理器。 受众管理器在美国处理和存储此数据。 受众管理器不提供在美国以外存储或处理此数据的选项。

### Cookie 和退出

使用实时受众分析时，不仅需要 [!DNL Analytics] 和 [!DNL Target] 所用的 Cookie，还需要利用 Audience Manager Cookie。

如果您希望向网站访客提供相应的退出选项，则必须将 Audience Manager 退出添加到现有退出过程。

请参 [阅Adobe Experience Cloud —— 实施Adobe选择退出](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/data-collection/opt-out.html) ，以获取说明。

请参 [阅数据收集CNAME和跨域跟踪](https://docs.adobe.com/content/help/zh-Hans/id-service/using/reference/analytics-reference/cname.html) ，以启用跨域跟踪。
