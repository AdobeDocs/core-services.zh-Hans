---
description: 实施 Experience Cloud 并成为管理员。此过程可使您的核心服务功能（例如，客户属性和受众）解决方案符合现代化要求。
keywords: 核心服务;客户属性
seo-description: 实施 Experience Cloud 并成为管理员。此过程可使您的核心服务功能（例如，客户属性和受众）解决方案符合现代化要求。
seo-title: 为核心服务启用 Experience Cloud 解决方案
solution: Experience Cloud
title: 为核心服务启用解决方案
uuid: 5820060f-9b18-4339-81e0-401d964f7a03
translation-type: ht
source-git-commit: b4809ff0b4546f105ac6270eca1bfce2b6467876

---


# 为核心服务启用解决方案

实施 Experience Cloud 并成为管理员。此过程可使您的核心服务功能（例如，客户属性和受众）解决方案符合现代化要求。

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
>对于 Target，[从 mbox.js 迁移到 at.js](https://marketing.adobe.com/resources/help/zh_CN/target/ov2/t_target-migrate-atjs.html)。


![](assets/step2_icon.png) 使您的实施符合现代化要求并进行管理员身份配置。


1. 按照下面[部署 Experience Cloud ID 服务](../core-services/core-services.md#section_3C9F6DF37C654D939625BB4D485E4354)中的步骤进行操作。
1. 联系您的帐户管理员，开始 Experience Cloud 的配置过程。

![](assets/step3_icon.png) 在管理控制台中管理用户和产品。

**管理员访问权限**

在成为管理员后，您可以登录 [marketing.adobe.com](https://marketing.adobe.com)。

您将会在 Experience Cloud 菜单导航中看到 **[!UICONTROL 管理]链接。**

如需帮助，请参阅 [Experience Cloud 用户和产品管理](../admin-getting-started/admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909)。

**用户访问**

要登录到 Experience Cloud，您的用户必须：


1. 拥有 Adobe ID。
1. 登录到 [!DNL marketing.adobe.com]。
1. 属于映射到企业群组的解决方案群组。
1. 如有必要，可将他们的解决方案帐户关联到其 Adobe ID（如下所述）。

![](assets/step4_icon.png)可选：关联现有的用户帐户。

您的一些用户可能已经是解决方案群组（例如，您在“Analytics”&gt;“管理工具”中管理的 Analytics 群组）的成员。

当您将这些群组映射到 Experience Cloud 企业群组时，这些用户必须手动将其解决方案帐户凭据关联到其 Adobe ID。

请参阅[在 Experience Cloud 中关联帐户](../admin-getting-started/organizations.md#topic_C31CB834F109465A82ED57FF0563B3F1)

> [!NOTE]
> 
> 在映射企业群组和解决方案群组后，将会自动关联新用户。（将自动创建解决方案凭据并将这些凭据关联到其 Adobe ID。）

以下各部分描述了如何使您的实施符合现代化要求。在使您的实施符合现代化要求后，可以在 Experience Cloud 中启用核心服务。

## 步骤 2. 使用 Dynamic Tag Manager 或 Experience Platform Lauch 实施 Experience Cloud ID 服务{#section_3C9F6DF37C654D939625BB4D485E4354}

启用 Experience Cloud 核心服务的最简便方法是，通过 Dynamic Tag Manager 中的 [Experience Cloud ID 服务工具](https://marketing.adobe.com/resources/help/zh_CN/mcvid/mcvid-dtm-implement.html)自动为 Analytics 和 Target 激活这些服务。（或者使用 Experience Platform Lauch。）

![](assets/menu-activation-shell.png)

有关完整的 Experience Cloud ID 服务（以前称为访客 ID），请访问[此处](https://marketing.adobe.com/resources/help/zh_CN/mcvid/)。

另外，下一代标记管理系统是 [Experience Platform Lauch](https://marketing.adobe.com/resources/help/zh_CN/experience-cloud/launch/)

**不使用动态标签管理或 Launch？**

如果您不使用动态标签管理，请通过 JavaScript 部署 ([!DNL VisitorAPI.js]) 手动实施 ID 服务，如下所示：

1. 执行[实施适用于 Analytics 的 Experience Cloud ID 服务](https://marketing.adobe.com/resources/help/zh_CN/mcvid/mcvid-setup-analytics.html)中描述的步骤。

   Adobe 还建议设置其他[客户 ID](https://marketing.adobe.com/resources/help/zh_CN/mcvid/mcvid-authenticated-state.html)。这些 ID 与每个访客相关联，并可以启用 Experience Cloud 核心服务中现有和未来的功能。

1. 将现有的 [!DNL s_code] 更新到 H.27.3 或更高版本，或将现有的 [!DNL AppMeasurement.js] 更新到 1.4 或更高版本。

   这些文件可从 Analytics 管理工具中的[代码管理器](https://marketing.adobe.com/resources/help/zh_CN/reference/index.html?f=code_manager_admin)下载。

   （如需了解有关 [!DNL AppMeasurement.js] 的更多信息，请参考 [JavaScript 实施](https://marketing.adobe.com/resources/help/zh_CN/sc/implement/js_implementation.html)指南。）

1. 为 Analytics 同步客户 ID。请参阅 [Analytics - 同步客户 ID](../core-services/core-services.md#section_AD473A6A21C1446498E700363F9A8437)（见下文）。

## Analytics 和 Target - 同步客户 ID {#section_AD473A6A21C1446498E700363F9A8437}

在设置 Experience Cloud ID 服务时，Adobe 建议您针对 Analytics 和 Target 考虑将自己的[客户 ID](https://marketing.adobe.com/resources/help/zh_CN/mcvid/mcvid-authenticated-state.html) 与 Experience Cloud 同步。

在 Target 中，[!DNL mbox3rdpartyid] 需要获取客户 ID 并将其发送给 Target。（请参阅 Target 中的[使用客户属性](https://marketing.adobe.com/resources/help/zh_CN/target/target/c_working-with-customer-attributes.html)。）

当访客在您的网站上进行身份验证或识别自身时，您的实施必须将此人的 CRM 客户 ID 透露给页面或应用程序。然后，您可以使用适当的函数调用，将您的客户 ID 与 Experience Cloud 同步。此同步会将访客的 CRM 客户 ID 存储在 Experience Cloud 中，并激活该客户的属性以便在 Experience Cloud 中使用。

例如，假设 Bob 在您的 CRM 系统中具有客户 ID `52mc210tr42`。当 Bob 在您的网站上进行身份验证时，您必须在该页面上透露此 ID，并使用此 ID 以下面两种方式之一进行同步：

* 使用访客 ID 服务调用 `visitor.setCustomerIDs({"crm_id":"52mc210tr42"})`。或，
* 在 prop 或 eVar 中填写*`Customer ID (52mc210tr42)`*。


在已知客户 ID 的情况下，必须在每次 [!DNL Analytics] 服务器调用中进行设置。

**Mobile SDK**

有关如何在 [Android](https://marketing.adobe.com/resources/help/zh_CN/mobile/android/methods.html) 和 [iOS ](https://marketing.adobe.com/resources/help/zh_CN/mobile/ios/?f=methods) 移动应用程序中设置其他客户 ID 的语法示例，请参阅 *Experience Cloud ID 服务*部分。

**启用历史数据的属性**

访客登录后，客户属性数据将变为可用状态。如果您尚未实施最新的 Experience Cloud ID 服务，并且以前一直在跟踪 prop 或 eVar 中的客户 ID，则可以请求一个流程，将历史登录信息发送至 Experience Cloud。此流程允许您立即开始使用客户属性。

联系客户关怀以启用历史数据。

## 步骤 3. 将报表包映射到 Experience Cloud 组织 {#section_7B08516B01BA421681DF03D0E86CE3BA}

Experience Cloud 服务（例如，Experience Cloud ID 服务和“人员”）与 Experience Cloud 组织（而非单个报表包）相关联。要确保这些服务能够正常运行，必须将每个 Analytics 报表包映射到 Experience Cloud 组织。

请参阅[将报表包映射到组织](report-suite-mapping.md)。

## 步骤 4. (Adobe Analytics) 使您的 Analytics AppMeasurement 代码符合现代化要求 {#section_1798D9D0F05C47E29816AC4EEB9A0913}

验证您是否位于区域数据收集 (RDC) 中。如果您的数据收集域是 [!DNL omtrdc.net]，或者，如果您的 CNAME 被映射到 [!DNL omtrdc.net]，则您使用的是 RDC。有关更多信息，请参阅[过渡到 RDC](https://marketing.adobe.com/resources/help/zh_CN/whitepapers/rdc/rdc_transition.html)。如果您使用的是第一方 Cookie，请参阅 [CNAME 和访客 ID 服务](https://marketing.adobe.com/resources/help/zh_CN/mcvid/mcvid_cname.html)，以获取有关数据收集 CNAME 和跨域跟踪的信息。

建议您更新包括访客 API 在内的 JavaScript 库，以使您的 Analytics 实施现代化。完成此任务的简单方法是在 Dynamic Tag Management 中添加 [!DNL Adobe Analytics] 工具，以指定 *`Automatic`* 作为配置方法。

在 Dynamic Tag Management 中，单击 **[!UICONTROL <Web Property Name>]**&gt;**[!UICONTROL 概述]**&gt;**[!UICONTROL 添加工具]**&gt;**[!UICONTROL Adobe Analytics]**。有关部署信息，请参阅 Dynamic Tag Management 中的[Adobe Analytics 设置](https://marketing.adobe.com/resources/help/zh_CN/dtm/analytics_dtm.html)。

## 步骤 5. (Adobe Target) 使您的 Adobe Target 实施符合现代化要求 {#section_C2F4493C7A36406DAE2266B429A4BD24}

* 建议您在 Dynamic Tag Management 中添加 [Adobe Target 工具](https://marketing.adobe.com/resources/help/zh_CN/dtm/target.html)，以便自动检索库。在 Dynamic Tag Management 中，单击 **[!UICONTROL <Web Property Name>]**&gt;**[!UICONTROL 概述]**&gt;**[!UICONTROL 添加工具]**&gt;**[!UICONTROL Adobe Target]**。** 注意：**您还可以使用动态标签管理来为 Target（和其他解决方案）部署 Experience Cloud ID 服务。** 必须 **更新 Experience Cloud ID 服务，这样 Target 才能使用核心服务。
* 如果您未使用 Dynamic Tag Management，请手动[更新您的 mbox 库](https://marketing.adobe.com/resources/help/zh_CN/target/ov/?f=t_mbox_download)。
* 请求访问权限，以使用 Adobe Analytics 作为 Adobe Target 的报告来源。在处理期间，Target 和 Analytics 数据将组合在同一服务器调用中，这样两个解决方案之间的访客就可以连接在一起。请参阅 [Analytics for Target 实施](https://marketing.adobe.com/resources/help/zh_CN/target/a4t/?f=a4t)。
* 
   >[!IMPORTANT]
   >
   >已针对客户属性等核心服务配置了所有 Analytics 客户。如果您不是 Analytics 客户，请联系客户关怀团队以请求进行配置。

## 步骤 6. 验证核心服务实施 {#section_E641782A0F4F44AF8C9C91216BE330D5}

使用下面的流程确保在您的网站上正确实施 Experience Cloud ID 服务。

1. 清除您网站上的 Cookie，这样可以看到对 Experience Cloud ID 服务的请求（该请求出现在第一次访问时，随后大约每周在每个访客访问时出现一次）。1. 使用一个数据包分析程序或 Web 浏览器调试程序中的网络面板，查找到 [!DNL dpm.demdex.net] 的请求。
1. 验证响应中是否包含 `d_mid` 和一个值，例如：`_setMarketingCloudFields({"d_mid":"4235...`
1. 验证 Analytics 请求是否包含 mid 参数 (Experience Cloud ID)。此外，您还应当在宽限期（如果启用）查看 aid 参数（Analytics 访客 ID）。

包含 Experience Cloud ID 的预期响应：

![](assets/mac_id_response.png)

包含 Experience Cloud ID (mid) 的 Analytics 图像请求：

![](assets/mid.png)

mbox 请求中的 Experience Cloud ID：

![](assets/mbox_request.png)

**什么是宽限期？**

当您部署了访客 ID 服务后，新的访客将不再会从您的数据收集服务器中接收到 Analytics 访客 ID。如果您网站的某些部分仍没有实施访客 ID 服务，那么当访客浏览这些部分时，将不能识别 Experience Cloud ID，与此同时，分配给访客的会是一个旧版的 Analytics 访客 ID。这可能会引起潜在的问题，包括访问重复计数和属性错误。

例如，如果您网站的支持部分是在单独的 CMS 中进行管理，则应有一个单独的 Analytics JavaScript 文件负责处理此部分。如果您在为该支持网站部署访客 ID 服务之前，在主网站上部署了访客 ID，那么当新的访客访问支持部分时，他们会收到一个旧版的 Analytics ID，而且跨越这两个网站部分的访问将被报告为不同的访问。

在使用多个 JavaScript 文件或其他技术（例如 Flash）的网站上部署访客 ID 服务可能会导致协调问题，因为您需要同时对网站的所有部分启用访客 ID 服务。通过配置一个宽限期，新的访客则可以继续从访客 ID 服务中接收 Analytics 访客 ID，这样对于网站上未升级成使用访客 ID 服务的部分而言，也可以始终如一地识别访客。

## 步骤 7. 管理用户和产品 {#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF}

启动并运行后，导航至 **[!UICONTROL 管理]** &gt; **[!UICONTROL 启动 Admin Console]**，您可以在其中管理用户和产品配置文件。

![](assets/menu-administration-shell.png)

请参阅 [Experience Cloud 用户和产品管理](../admin-getting-started/admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909)。

**客户属性**

<!-- <p> 
 <note type="important">
  To use the Customer Attributes feature, users must belong to the 
  <span class="term"> Adobe Customer Attributes</span> group, and to solution-level groups (Analytics or Target). 
 </note> </p> 
 -->

添加到客户属性群组的用户将在 Experience Cloud 界面的左侧看到“[!UICONTROL 客户属性]”菜单项

## 步骤 8. 开始使用核心服务 {#section_960C06093623462E8EA247B3E97274A1}

充分利用以下核心服务功能。

![](assets/menu-audiences-shell.png)

**人员 &gt; 客户属性**

如果您在客户关系管理 (CRM) 数据库中捕获到企业客户数据，则可以将该数据上传到 Experience Cloud 中的客户属性数据源。上传后，即可在 [!DNL Adobe Analytics] 和 [!DNL Adobe Target] 中利用这些数据。

请参阅[客户属性](../attributes/attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1)。

**人员 &gt; 受众库**

Experience Cloud 受众是一个界面，您可以从这里创建受众，合并现有受众以创建组合受众，以及查看所有共享受众。

请参阅[受众](../audience-library/audience-library.md#topic_679810123CAA4E0CA4FA3417FB0100C7)

<!-- aam_mc.xml -->

## 数据存储和隐私披露信息

如果在 Adobe [!DNL Experience Cloud] 中使用实时受众分析和其他核心服务，那么运用这些服务时，可能会影响存储相关数据的数据中心（和国家/地区）。具体来讲，由于 Adobe [!DNL Experience Cloud] 的核心服务需要利用 Adobe Audience Manager，所以在“人员”核心服务中使用的数据必须存储在位于美国的 Audience Manager 服务器上。

当可以通过“人员”核心服务来利用多种核心服务时，从其他 Adobe 产品向受众管理发送的数据类型包括：

* [!DNL Analytics] 键/值对（prop、eVar、list var 等等）。默认情况下，日志行包含 IP 地址，其中包含 IP 的最后一个八位字节（假定 IP 地址没有被 Adobe [!DNL Analytics] 中的 IP 模糊设置所修改）。
* 根据 Audience Manager 中设定的规则，访客所符合的特征和区段。
* （可选）您的一个或多个 ID。根据您实施的 ID 服务，可能还需要发送一个或多个 ID，例如 CRM ID 或哈希电子邮件地址。如果此数据被发送到 Adobe [!DNL Analytics]，则会转给 Adobe 受众管理。Adobe 不建议将个人数据提交给 Adobe [!DNL Analytics]。而是使用单向哈希对数据进行伪装，然后再发送给 Adobe。
* 来自 [!DNL Analytics] 通过后端区段共享功能得到的区段。
* 如果未阻止第三方 Cookie，则设置 demdex.net Cookie。`AMCV_###@AdobeOrg` 第一方 Cookie 始终通过 Experience Cloud ID（以前称为“访客 ID 服务”）设置。


所有这些数据元素都会以日志文件的形式提供给 Adobe Audience Manager。Audience Manager 在美国境内处理和存储此数据。Audience Manager 不在美国以外的位置存储或处理此数据。

**Cookie 和退出**

使用实时受众分析时，不仅需要 [!DNL Analytics] 和 [!DNL Target] 所用的 Cookie，还需要利用 Audience Manager Cookie。

如果您希望向网站访客提供相应的退出选项，则必须将 Audience Manager 退出添加到现有退出过程。

有关说明，请参阅 [Adobe Experience Cloud - 实施 Adobe 选择退出](https://marketing.adobe.com/resources/help/zh_CN/sc/implement/opt_out.html)。

有关启用跨域跟踪的信息，请参阅[数据收集 CNAME 和跨域跟踪](https://marketing.adobe.com/resources/help/zh_CN/mcvid/mcvid_cname.html)。
