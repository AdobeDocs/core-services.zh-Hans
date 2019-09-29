---
description: Experience Cloud 界面的功能、发行说明和已知问题。
keywords: 核心服务
seo-description: Experience Cloud 界面的功能、发行说明和已知问题。
seo-title: 发行说明汇总
solution: Experience Cloud
title: 发行说明汇总
uuid: fcff8cc6-e587-4bf2-9a75-261d4eabc7d4
translation-type: tm+mt
source-git-commit: 75831abe44d04902691325add2338381754f98ec

---


# 发行说明汇总

Experience Cloud 界面的功能、发行说明和已知问题。

有关文档更新的列表，请参阅 [Experience Cloud](../doc-updates.md#concept_4C8983FCD23848A4B1E4C2D99ED82784)。

要获取涵盖所有解决方案的发行说明，请参阅 [Experience Cloud 发行说明](https://marketing.adobe.com/resources/help/en_US/whatsnew/)。

## 8 月版 - 2019 年

* 修复了 Experience Cloud 登录中导致某些用户会话注销的关键问题。(MCUI-6908)
* 更新了 Experience Cloud 登录，以提高性能并减少延迟。（MCUI-6854、MCUI-6869 和 MCUI-6883）
* 更新了界面外观。（MCUI-6861、MCUI-6911 和 MCUI-6862）
* 修复了 Experience Cloud [!UICONTROL 触发器]存在的问题，之前该问题会导致[!UICONTROL 触发器]定义中的 _Like_ 子句的解释有误。(MCUI-6611)

## 4 月版 - 2019 年

* 更新了应用程序切换器，以便在 Experience Cloud 解决方案套件中包含 Marketo，同时将品牌更新为“Experience Platform”。(MCUI-6529)
* 更新了 Experience Cloud 主页，以包含指向“馈送”和“管理”页面的导航链接。(MCUI-6682)
* 修复了[!UICONTROL 触发器]定义中存在的问题，以纠正“like”子句的用法。(MCUI-6611)
* 改进了客户属性，让登录“订阅”服务的过程为此变得更加顺畅。(MCUI-6519)

## 19.1.1 版 - 2019 年 1 月 17 日

**注意：** 2019 年 3 月，Experience Cloud 界面将不再支持 Internet Explorer 11。

* 修复了导致在帮助中搜索时无法返回结果的问题。(MCUI-1670)
* 修复并改进了触发器中的 eVar 管理。(MCUI-6400)

## 16.5.1 版 - 2016 年 5 月 26 日 {#section_3785F182BC13493F84903CA69EB6D0A8}

**功能和改进**

<table id="table_ABBCE1A66F534059BD728BC2B9AEFA80"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 功能 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>管理控制台中预先配置的产品配置 </p> </td> 
   <td colname="col2"> <p>Experience Cloud 客户管理员可以利用预先创建并映射到 Analytics 和动态标签管理默认权限群组的产品配置。 </p> <p>此优化适用于新配置的组织，它可缩短组织在管理控制台中管理用户所需的时间。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>信息源改进 </p> </td> 
   <td colname="col2"> <p> 在 Experience Cloud 信息源中新建帖子时，“收件人”行现在默认使用当前活动的主题，而非组织。</p> </td> 
  </tr> 
 </tbody> 
</table>

**修复**

* 修复了缩略图无法显示从即时资产共享到 Experience Cloud 信息源的资产问题。(MAC-29955)

## 16.2 版 - 2016 年 2 月 18 日 {#section_D9610373116C4D77A38F67815C725EA3}

<table id="table_C9B288CF42034F329C3C72D95D22E515"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 功能 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Experience Cloud 资产改进 </p> </td> 
   <td colname="col2"> <p>在 Experience Cloud 资产中，您可以从一个中心位置存储、共享和同步数字资产。Experience Cloud 资产可利用 <span class="keyword">Adobe Experience Manager</span> (AEM) 中提供的某些功能。 </p> <p>请参阅 <a href="../experience-cloud-assets/experience-cloud-assets.md#concept_DDA5224C907D4A4F817D795DA0ED64D0" format="dita" scope="local">Experience Cloud</a></p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>帐户链接改进 </p> </td> 
   <td colname="col2"> <p>改进了用于将解决方案帐户与 Experience Cloud (Adobe ID) 关联的界面工作流程。此新工作流程可找到用户与组织关联的所有帐户，并允许选择要关联哪个帐户。我们还简化了帐户链接体验，这样您就不再需要访问“管理组织”页面来手动链接帐户。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**修复**

* 修复了导致 Analytics 无法链接以及无法进行单点登录的问题。此问题显示：“注意: 错误消息: ERROR IMS SSO 失败: 找不到链接的公司。”

**已知问题**

如果您通过 **[!UICONTROL Experience Cloud]** &gt; **[!UICONTROL 激活]**&#x200B;界面访问 Dynamic Tag Management，但您的 Dynamic Tag Management 帐户没有关联到 Experience Cloud (Adobe ID)，则您将无法登录到 Dynamic Tag Management。要避免出现此问题，请在新的浏览器选项卡中直接导航到 [!DNL dtm.adobe.com]。

## 16.1 版 - 2016 年 1 月 21 日 {#section_33B3F7DF6CA347E3AA93801BAC6232CE}

<table id="table_4223658257DA41C999AC710A10D26771"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 功能 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Audience Library 消息 </td> 
   <td colname="col2"> <p> 我们改进了 Audience Library，可在构建受众或发生超时的时显示有用的消息。 </p> <p>例如，在添加五个以上的规则时，会显示一则消息，指示您已超过允许的最大规则数。（MAC-27376、MAC-27375） </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Microsoft 即将[结束](https://www.microsoft.com/en-us/WindowsForBusiness/End-of-IE-support)对 Internet Explorer 8、9 和 10 的支持。因此，我们将不会针对这些特定 Internet Explorer 版本报告的问题进行修复。

## 15.10 版 - 2015 年 10 月 14 日 {#section_68123833D3634BD3A473C12862BF9606}

**已知问题**

* 客户如果通过 Experience Cloud 使用单点登录 (SSO) 方式进入 Analytics，则无法登录 Report Builder。此问题不影响使用旧版 Analytics 凭据的客户。
* 与 Analytics 中“链接至报表”功能相关的已知问题。通过 Experience Cloud 登录到 Analytics 的客户在尝试共享报表时，会被定向到 Analytics 的非单点登录页面。

## 15.9 版 - 2015 年 9 月 10 日 {#section_BCCE3E7DF62A4FF5A57B9C8FE2A5F37B}

* 修复了在上传客户属性数据时导致间歇性超时的 Audience Manager API 性能问题。(MAC-26305)
* 修复了阻止用户向某个订阅添加最多 200 个客户属性的问题。(MAC-26188)
* 修复了导致无法从 Analytics 区段进行受众共享的 Audience Library 问题。此问题会导致系统显示“正在收集数据”（0 个受众）。为了防止出现此问题，Adobe 建议将每个区段的受众成员保持在 5 万人以下。(MAC-25788)
* 修复了“客户属性”-“编辑架构”页面之前存在的一个已知问题，该问题会导致在更改显示名称时产生“内容识别”错误。（MAC-25589，AN-103834）

## 15.7 版 - 2015 年 7 月 22 日 {#section_2683A152176944E48EF6C943892975B7}

* 修复了导致无法在 Analytics 报表中更新“查看/编辑架构”页面（位于客户属性中）上指定的属性描述的问题。(MAC-25985)
* 修复了无法呈现已上传资产中缩略图的问题。(MAC-25863)
* 修复了导致在 Reports &amp; Analytics 中创建的新区段在 Experience Cloud 受众中不可用的问题。(MAC-25817)
* 修复了导致受众在使用访客 ID 服务时无法从 Analytics 共享的问题。（MAC-25788、MAC-25747）
* 现已支持在客户属性中使用多字节字符。(MAC-25552)

**已知问题**

一个已知的问题是导致在 Audience Manager 中创建重复的自动生成帐户，然后自动将这些帐户关联到一位用户的 Experience Cloud 身份。如果您试图在关联帐户之前导航到 Audience Manager，便会出现此问题。Adobe 建议您在导航到 Audience Manager 之前，先将 Audience Manager 帐户关联到 Experience Cloud。(MAC-25640)

## 15.6.1 版 - 2015 年 6 月 11 日 {#section_AD2019F8D2F84C9EB2B0533FAACF7043}

没有可用的信息

## 15.5.1 版 - 2015 年 5 月 13 日 {#section_EF197410964E40D294D0D8024738CFBA}

<table id="table_14E7B35E06C84A258A21D09691B58354"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 功能 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </p> </td> 
   <td colname="col2"> <p>左侧导航器菜单已更新并设置为提供对所有核心服务和解决方案的访问。值得注意的更改包括： </p> 
    <ul id="ul_5BEBAB86B9234A239C4E2DAF8826D8E3"> 
     <li id="li_7FA9F64CE69144B8A8A92746BF40E5A1">The<span class="term">受众库</span>和<span class="term">客户属性</span>菜单选项现在位于<span class="term">受众</span>下方。 </li> 
     <li id="li_95D62A43AE6243DBB2A65EDB830D05C4"><span class="term">Exchange</span> 菜单选项已从“帮助”下拉菜单移至左侧导航器边栏。 </li> 
     <li id="li_0443FD50C78446CD8AA27A4F272CAD31"> <span class="term">解决方案</span>已被删除。您可以从导航器边栏的下半部分启动所有解决方案。 </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

* 修复了无法为某些客户同步客户属性的问题。
* 修复了 [Adobe Target 产品文档](https://marketing.adobe.com/resources/help/ja_JP/target/a4t/)页面无法以日语显示的问题。
* 修复了无法在 [!DNL Creative Cloud] 和 [!DNL Experience Cloud] 之间的评论中使用日语文本的问题。

## 15.4.1 版 - 2015 年 4 月 8 日 {#section_75634120CC934B3381EDEA7F6F976F0A}

<table id="table_3A6FBAE36558425A803B078150862C92"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 功能 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>管理功能得到提升： </p> 
    <ul id="ul_7D5FCBEFA262435D865CA1018BFB792E"> 
     <li id="li_6E98974CCB094ABBAB57C51ED56C3F00"> <span class="wintitle">管理控制台</span> </li> 
     <li id="li_8CDAB6301FD44C3999EE4EEB1A0A2FD6">支持 Enterprise ID 和 Federated ID </li> 
    </ul> </td> 
   <td colname="col2"> <p>用户和群组管理功能已经迁移到管理控制台。新的导航路径是： </p> <p> <span class="uicontrol"> Experience Cloud</span> &gt; <span class="uicontrol">管理</span> &gt; <span class="uicontrol">启动管理控制台</span></p> <p> 此外，还添加了对 Enterprise ID 和 Federated ID 的支持。您可以在同一企业部署中使用 Enterprise ID、Federated ID 以及 Adobe ID。例如，将 Adobe ID 用于可能使用其他 Adobe 产品和服务的用户。将 Enterprise ID 或 Federated ID 用于那些您希望严格管理其帐户的用户。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**修复**

* 修复了一个阻止在 [!DNL Experience Cloud] 和 [!DNL Media Optimizer] 之间进行单点登录的问题。

**已知问题**

* 对于新建的 Experience Cloud 组织，无法在动态标签管理组织与 Experience Cloud 之间建立关联和取消关联。我们正着手解决此问题，预计将在五月份发行的版本中恢复正常功能。如果您在尝试通过 Experience Cloud 以单点登录方式访问动态标签管理时遇到问题，请采用以往的登录方式访问 [!DNL dtm.adobe.com]。
* 一个已知的问题是：对于不属于关联的 Analytics 帐户的报表包，访客将无法共享该报表包中的内容。我们目前正在修复这个问题。

## 15.3.2 版 - 2015 年 3 月 19 日 {#section_07760FD9CA43497FA8BDCCA990A24BFD}

<table id="table_54025DBE2D094FF1BE837BA60816C6DF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 功能 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>客户属性 </p> </td> 
   <td colname="col2"> <p>如果您在客户关系管理 (CRM) 数据库中捕获到企业客户数据，则可以将该数据上传到 Experience Cloud 中的客户属性数据源。在上传数据后，您可以在 Analytics 中运行<span class="uicontrol">访客配置文件</span> &gt; <span class="uicontrol">客户属性</span>报表。 </p> <p>您还可以将上传数据用作 <span class="keyword">Adobe Target</span> 中的受众区段。 </p> <p>请参阅<a href="../attributes/attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1" format="dita" scope="local">客户属性</a>产品文档。 </p> <p> 有关使您的核心服务解决方案实现现代化的信息，请参阅<a href="../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C" format="dita" scope="local">为核心服务启用解决方案</a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 15.3.1 版 - 2015 年 3 月 4 日 {#section_57CB69C044DD47BDBC1A1BEC38957551}

<table id="table_EB3FFBA2DF904546A5185EC9A63BBA98"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 功能 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>群组映射 </p> </td> 
   <td colname="col2"> <p>“群组管理”页面已作为一个管理界面进行了重新设计，您可以在其中创建群组、将用户添加到群组，以及跨多个 Experience Cloud 解决方案应用相关权限。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>一对多映射 </p> </td> 
   <td colname="col2"> <p>现在，当您在 Experience Cloud 中关联解决方案帐户时，如果您有多个解决方案和组织，则可以将多个产品和服务映射到一个组织。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>激活 </p> </td> 
   <td colname="col2"> <p> <a href="../activation/activation.md#concept_EE756B6B0A0643DAB8CA3A00E665406C" format="dita" scope="local">激活</a>现在显示在 <span class="keyword">Experience Cloud</span> 的左侧导航区域中。“<span class="wintitle">激活</span>”功能目前是 <span class="keyword">Experience Cloud</span> 的一项核心服务，由动态标签管理技术组成，单击时会将您导向该处。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>文档更新 - 核心服务 </p> </td> 
   <td colname="col2"> <p>添加了主题<a href="../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C" format="dita" scope="local">为核心服务启用解决方案</a>，以帮助您实施核心服务。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 15.2.1 版 - 2015 年 2 月 19 日 {#section_BC694D5AE16A4E16B44B353ED67947F3}

修复：

* 改进了与帐户配置相关的用户电子邮件邀请工作流程。
* 修复了 [!DNL Experience Cloud] 和 [!DNL Adobe Campaign] 资产无法显示同一文件夹层次结构的资产文件夹问题。
* 修复了无法删除隶属于已停用 [!DNL Target] 活动的受众的问题。
* 修复了[!UICONTROL 新建受众]页面的[!UICONTROL 规则]下无法显示“添加”（加号）图标的问题。
* 改进了 Experience Cloud 界面对 Internet Explorer 9 的支持。

## 15.1.1 版 - 2015 年 1 月 15 日 {#section_F1A352E928AF432E94CC0A289C345184}

[!DNL Adobe Experience Cloud] 协作和共享界面的新增功能和修复。

<table id="table_AD0A8CA760E64227BB04BA6B0E425E80"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 功能 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>只读访问权限。 </p> </td> 
   <td colname="col2"> <p>管理员现在可以授予非管理用户只读访问权限。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**修复**

* 修复了无法在信息卡上渲染 PNG 文件的问题。
* 修复了通过拖放将文件上传到 Experience Cloud 资产时发生的问题。

**已知问题**

* 用户不能在展示板上共享 PowerPoint 文件。
* 只有在重新登录之后，用户管理中所做的群组和授权更改才会生效。
* 某些用户在将大文件类型上传到 Experience Cloud 资产时可能会遇到问题。
* 用户可能无法从 Media Optimizer 中看到他们 Experience Cloud 信息卡上的链接。
* 某些管理用户在接受加入 Experience Cloud 的邀请后关联其帐户时可能会遇到问题。
* 当多个用户同时使用 Experience Cloud 界面时，该界面性能可能会降低。
* 某些用户可以删除过期的资产，而不会收到错误通知。
* 某些用户在同时使用一个 Adobe ID 登录两个浏览器时可能会遇到问题。
* 某些用户在删除了一个 Creative Cloud 用户之后，可能无法再次向共享文件夹添加该 Creative Cloud 用户。
* 在将文件夹从 Experience Cloud 共享到 Creative Cloud 时，某些用户可能会遇到通知延迟问题。
* 某些用户在 Experience Cloud 和 Creative Cloud 之间共享文件夹时可能会遇到问题。
* 启用共享受众之后，某些用户在 Analytics 报表包中创建受众时可能会遇到问题。
* 某些用户在将资产上传到展示板时可能会遇到问题。

## 14.11.1 版 - 2014 年 11 月 13 日 {#section_A6CF1D4F27B9496892A89C983EB39102}

已知问题:

* 某些用户可以删除过期的资产，而不会收到错误通知。
* 某些 [!DNL .png] 文件无法在信息卡中呈现。
* 某些用户在将资产上传到展示板时可能会遇到问题。
* 只有在重新登录之后，用户管理中执行的群组和授权更改才会生效。
* 管理员必须注销然后重新登录，才能查看“帐户设置”中执行的更改。
* 用户不能在展示板上共享 PowerPoint 文件。
* 当多个用户同时使用 [!DNL Experience Cloud] 界面时，该界面性能可能会降低。
* 无法实现 Adobe Experience Manager 与 Creative Cloud 的同步。

## 14.10.1 版 - 2014 年 10 月 16 日 {#section_E3A0F4423B814707AA3745E083500835}

[!DNL Adobe Experience Cloud] 协作和共享界面的新增功能和修复。

<table id="table_7C1ACE8108D54782AE128ACD35069DF5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 功能 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>编辑用户权限 </p> </td> 
   <td colname="col2"> <p>展示板的所有者现在可以编辑特定展示板上的用户权限。 </p> <p> 
     <ol id="ol_B12251C510744538AF9BCE60ACB04016"> 
      <li id="li_87B3EDE9542B47CEBE0BE7F2D1DE844D">在展示板上，单击<span class="uicontrol">设置</span>。 </li> 
      <li id="li_0F4786B0E1E743069D082E7DC488A031">在每个所有者旁边，指定<span class="uicontrol">所有者</span>、<span class="uicontrol">查看者</span>或<span class="uicontrol">编辑者</span>。 </li> 
     </ol> </p> </td> 
  </tr> 
 </tbody> 
</table>

**修复**

* 从 PDF 创建信息卡并分享到展示板会返回错误消息。

**已知问题**

* 某些用户在将资产上传到展示板时可能会遇到问题。
* 某些 [!DNL .png] 文件无法在信息卡中呈现。
* 只有在重新登录之后，用户管理中执行的群组和授权更改才会生效。
* 某些用户可能无法从 PDF 创建信息卡并将其共享到展示板。
* 某些用户可以删除过期的资产，而不会收到错误通知。
* 用户不能在展示板上共享 PowerPoint 文件。
* 当多个用户同时使用 [!DNL Experience Cloud] 界面时，该界面性能可能会降低。
* 无法在“[!DNL Search&Promote]组织和产品访问[!UICONTROL ”页面中关联 ]。

## 14.9.1 版 - 2014 年 9 月 18 日 {#section_20F156A9CC2F4FC59C4970075C181D3A}

**修复和改进功能**

* 现在，在导航到 [!DNL marketing.adobe.com] 时，登录体验和 Adobe 的 Creative Cloud 登录一样。
* 在“管理组织”页面中，关联体验（在收到邀请后）当前对于每个解决方案都是一致的。

**已知问题**

* 只有在重新登录之后，用户管理中执行的群组和授权更改才会生效。
* 某些用户可能无法从 PDF 创建信息卡并将其共享到展示板。
* 某些用户在将资产上传到展示板时可能会遇到问题。
* 某些用户可以删除过期的资产，而不会收到错误通知。
* 用户不能在展示板上共享 PowerPoint 文件。
* 某些 [!DNL .png] 文件无法在信息卡中呈现。
* 当多个用户同时使用 [!DNL Experience Cloud] 界面时，该界面性能可能会降低。
* 无法在“[!DNL Search&Promote]组织和产品访问[!UICONTROL ”页面中关联 ]。
* 某些用户在 [!DNL Creative Cloud] 中取消共享的 [!DNL Experience Cloud] 内容可能会从他们的文件夹中删除。

## 14.8.1 版 - 2014 年 8 月 21 日 {#section_03BF00F6A95A490C91BCC0A1988FA7AA}

[!DNL Adobe Experience Cloud] 协作和共享界面的新增功能和修复。

<table id="table_1E7DBEB5E83B4E4285B6FD1D718CD16D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 功能 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </p> </td> 
   <td colname="col2"> <p>您现在可以从左侧导航栏中访问 <span class="keyword">Adobe Mobile Services</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**已知问题**

* 只有在重新登录之后，用户管理中执行的群组和授权更改才会生效。
* 某些用户可能无法从 PDF 创建信息卡并将其共享到展示板。
* 某些用户在将资产上传到展示板时可能会遇到问题。
* 某些用户可能无法从 [!DNL Target] 登录到 [!DNL Experience Cloud]。
* 某些 Audience Manager 用户无法登录到 [!DNL Experience Cloud]。
* 某些用户可以删除过期的资产，而不会收到错误通知。
* 从 [!DNL Experience Cloud] 删除的文件不会从 [!DNL Digital Asset Management] 中删除。
* 用户不能在展示板上共享 PowerPoint 文件。
* 某些 [!DNL .png] 文件无法在信息卡中呈现。
* 当多个用户同时使用 [!DNL Experience Cloud] 界面时，该界面性能可能会降低。
* 无法在“[!DNL Search&Promote]组织和产品访问[!UICONTROL ”页面中关联 ]。
* 某些用户在 [!DNL Creative Cloud] 中取消共享的 [!DNL Experience Cloud] 内容可能会从他们的文件夹中删除。

## 14.7.1 版 - 2014 年 7 月 24 日 {#section_B22D4F830756463DB27BB4D508D9ADD5}

[!DNL Adobe Experience Cloud] 协作和共享界面的新增功能和修复。

**已知问题**

* 从 [!DNL Experience Cloud] 删除的文件不会从 [!DNL Digital Asset Management] 中删除。
* 某些 [!UICONTROL Exchange] 用户可能在备注中发现他们的名称为一个较长的字符串 ID，而不是他们的名称
* 某些 [!DNL .png] 文件无法在信息卡中呈现
* 上传文件时允许的文件类型比拖放方法允许的要多。为获得最佳结果，请使用“[!UICONTROL 资产]”上传。
* 无法在“[!DNL Search&Promote]组织和产品访问[!UICONTROL ”页面中关联 ]。
* [!DNL Exchange] 用户必须清除 Cookie 才能改善体验。
* 当多个用户同时使用 [!DNL Experience Cloud] 界面时，该界面速度可能会减慢。
* 某些用户在 [!DNL Creative Cloud] 中取消共享的 [!DNL Experience Cloud] 内容可能会从他们的文件夹中删除。
* 用户处于不活动状态 15 分钟以后会被注销。此外，在一个位置注销将会使您从整个 [!DNL Experience Cloud] 中注销。
* 某些用户可能无法将他们的 Audience Manager 帐户关联到 [!DNL Experience Cloud]。
* [!UICONTROL Exchange] 用户在语言选择器中只能看到“英语”。

**修复**

没有报告任何内容。

## 14.6.1 版 - 2014 年 6 月 19 日 {#marketing_cloud_interface}

[!DNL Adobe Experience Cloud] 协作和共享界面的新增功能和修复。

**改进**

<table id="table_C9BD63436BF0414B97B8D07387D1993B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 功能 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>  受众中的<span class="wintitle">保存</span>按钮 </p> </td> 
   <td colname="col2"> <p>现在创建受众时，在您填写完所有必填字段之前，<span class="wintitle">创建新受众</span>页面上的<span class="wintitle">保存</span>按钮处于禁用状态。<!--MAC-19712 --></p> </td> 
  </tr> 
 </tbody> 
</table>

**已知问题**

* 从 [!DNL Experience Cloud] 删除的文件不会从 [!DNL Digital Asset Management] 中删除。
* 上传文件时允许的文件类型比拖放方法允许的要多。为获得最佳结果，请使用“资产”上传。
* 无法在“[!DNL Search&Promote]组织和产品访问[!UICONTROL ”页面中关联 ]。
* 从 [!DNL Analytics] 对趋势报表应用的过滤器不会应用到 [!DNL Experience Cloud] 中的信息卡。
* 某些用户无法将他们的受众管理帐户与其 [!DNL Experience Cloud] 帐户相关联。
* 用户处于不活动状态 15 分钟以后会被注销。此外，在一个位置注销将会使您从整个 Experience Cloud 中注销。
* 某些 Exchange 用户可能在备注中发现他们的名称为一个较长的字符串 ID，而不是他们的名称

**修复**

* 修复了阻止将视频上传到应用程序的问题。

## 14.5.1 版 - 2014 年 5 月 22 日 {#section_7E22B2CB3ABA4D6EAED8CA8EFDE5433E}

<table id="table_4E4B34EEE3D94D78BA1A1FBC62950559"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 功能 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Experience Cloud Exchange </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> Experience Cloud</span> &gt; <span class="uicontrol">帮助</span> &gt; <span class="uicontrol">Exchange</span></p> <p><span class="keyword">Experience Cloud</span> <span class="wintitle">Exchange</span> 是您可以通过应用程序搜索、浏览、选择、付款和下载 Digital Marketing 扩展的一个位置。 </p> <p>这些应用程序包括 Data Connectors、Adobe 核心产品的自定义配置、第三方应用程序、报表和 <span class="keyword">Experience Cloud</span> 信息卡。 </p> <p>请参阅 <a href="../exchange.md#concept_E07F16F070544B82B56527A845C41D59" format="dita" scope="local">Exchange Marketplace</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Experience Cloud 受众 </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> Experience Cloud</span> &gt; <span class="uicontrol">受众</span></p> <p> 在<span class="wintitle">受众</span>中，您可以创建、编辑和管理受众，其方式与处理区段类似。例如，您可以在 Reports &amp; Analytics 中创建一个区段，然后将其共享到 <span class="wintitle">Experience Cloud</span> <span class="wintitle">受众</span>。共享之后，该受众即可用于 <span class="keyword">Adobe Target</span> 营销活动，并出现在 Adobe Audience Manager 的区段中。 </p> <p> <p>注意：要在 Target 中请求启用受众，请访问 <a href="https://www.adobe.com/go/audiences" format="http" scope="external">http://www.adobe.com/go/audiences</a>。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </p> </td> 
   <td colname="col2"> <p>在 <span class="keyword">Experience Cloud</span> 信息卡中提及的用户现在有权使用该信息卡。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </p> </td> 
   <td colname="col2"> <p>新 Adobe 用户可以将他们的 Scene7 帐户关联到 Adobe ID 及其团队成员。管理员也可以从 Scene7 帐户取消关联用户。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>资产同步 </p> </td> 
   <td colname="col2"> <p> 您可以将 Adobe Experience Manager (AEM) 资产内的资产与 Adobe Experience Cloud 和 Adobe Creative Cloud 共享，这样，对这些资产所做的任何更改都会反映在 Adobe Experience Cloud 和 Adobe Creative Cloud 内的共享资产副本中。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**修复**

* [!DNL Experience Cloud] 未关联到 [!DNL Adobe Target]。如果 [!DNL Adobe Target] 登录凭据可以在多个 [!DNL Target] 服务器上使用，则会发生此问题。
* 在 [!DNL Experience Cloud] 中创建了某个用户后，[!DNL Adobe Media Optimizer] 不会自动创建该用户。
* 组合框内用于添加新用户的选项在键入内容时暂时消失。
* 资产信息卡视图中的“评论”链接不可点击。
* 在将自定义标签添加到资产后，其他元数据更改不能持久保留。
* 删除图像时，如果该图像同时被 Adobe Target Essentials 使用，则资产不会发出警告。
* 当多个用户同时使用 [!UICONTROL Experience Cloud] 界面时，该界面性能会降低。
* 删除 [!UICONTROL Experience Cloud 资产]中的图像时，如果该图像同时被 [!DNL Adobe Target Essentials] 使用，则不会发出警告。
* 如果未在登录期间选择&#x200B;**[!UICONTROL 记住我]，则用户将在 15 分钟后被注销。**
* 用户必须先注销，然后再次登录，才能使所有许可和授权更改生效。
* 登录到 [!DNL Experience Cloud] 需要花费超过一秒钟的时间。
* 对于某些用户，从 [!DNL Experience Cloud] 中删除文件时不会与 [!DNL Digital Asset Management] 同步。
* 用户会在浏览器处于不活动状态 15 分钟以后注销。
* 用户不能在展示板上共享 PowerPoint 文件。
* 对于某些用户，Internet Explorer 10 的可视化布局比其他浏览器差。

## 14.4.1 版 - 2014 年 4 月 22 日 {#section_E2A699764E744D2E8D418E9A3D40AF6B}

<table id="table_D95C0DC64F2A4B47BAC83E504CFD6825"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 功能 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>从帮助主题创建信息卡 </p> </td> 
   <td colname="col2"> <p>现在，当您在浏览器的“书签”工具栏中启用“共享到 Adobe Experience Cloud”功能后，就可以通过微型网站 URL 共享帮助页面。 </p> <p> <b>共享帮助主题</b> </p> 
    <ol id="ol_F94B816121494B0FA16CC07B0E96AED8"> 
     <li id="li_F47187D4B5FE46D3A51D257DD569B4D6"> <p>在 <span class="keyword">Experience Cloud</span> 中，单击<span class="uicontrol">管理</span>。 </p> </li> 
     <li id="li_94EF58E7A4974B63951E14F72A710183"> <p>将<span class="uicontrol">共享到 Adobe Experience Cloud</span> 按钮拖动到“书签”工具栏。 </p> </li> 
     <li id="li_69EEC4F25D8F4AD7AA106A10B7F50FF6"> <p>导航到帮助页面（或者停留在此页面上），然后单击浏览器“书签”工具栏上的<span class="uicontrol">共享到 Adobe Experience Cloud</span>。 </p> <p>此步骤会创建一个信息卡，您可以在 <span class="wintitle">Experience Cloud</span> 中进行查看。 </p> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

**修复**

* 在将自定义标签添加到资产后，没有任何其他元数据更改可以持久保留。
* 用户需要刷新展示板才能使已删除的信息卡在视图中消失。
* 如果未在登录期间选择&#x200B;**[!UICONTROL 记住我]，则用户将在 15 分钟后被注销。**
* [!DNL Analytics] 解决方案登录页面显示格式错误。
* 用户必须先注销，然后再次登录，才能使所有许可和授权更改生效。
* 删除图像时，如果该图像同时被 [!UICONTROL  使用，则]资产[!DNL Adobe Target Essentials]不会发出警告。
* 资产信息卡视图中的“评论”链接不可点击。
* 组合框内用于添加新用户的选项在键入内容时暂时消失。
* 登录到 [!DNL Experience Cloud] 需要花费超过一秒钟的时间。
* 从 [!DNL Media Optimizer] 共享的数据不能在 [!DNL Experience Cloud] 中正确显示。
* 在 [!DNL Experience Cloud] 中创建了某个用户后，Adobe [!DNL Media Optimizer] 不会自动创建该用户。
* 如果 [!DNL Adobe Target] 登录凭据可以在多个 [!DNL Target] 服务器上使用，则 [!DNL Experience Cloud] 无法关联到 [!DNL Adobe Target]。
* 当多个用户同时使用 [!DNL Experience Cloud] 界面时，该界面速度可能会减慢。
* 无法在“[!DNL Search&Promote]组织和产品访问[!UICONTROL ”页面中关联 ]。
* [!DNL Adobe Media Optimizer] 模拟信息卡未正确呈现。
* 从 [!DNL Analytics] 对趋势报表应用的过滤器不会应用到 [!DNL Experience Cloud] 中的信息卡。
* 从 Analytics 对趋势报表应用的过滤器不会应用到 Experience Cloud 中的信息卡。
* 某些 Excel 或 CSV 文件无法上传至展示板。
* 某些用户可能无法将他们的受众管理帐户与其 [!DNL Experience Cloud] 相关联。
* 某些用户在 [!DNL Experience Cloud] 中共享 [!DNL Analytics] 区段时可能会遇到错误。
* 某些用户可能无法向下展开至[!UICONTROL 资产选择器]中的子文件夹。
* 某些用户无法在 [!DNL Experience Cloud] 中共享 AdLens 小工具。

## 14.3.1 版 - 2014 年 3 月 13 日 {#section_5D142E3225E3477A84DC01B8197D39BC}

14.3.1 版是维护版本，主要关注速度、稳定性和安全性。其中未包含主要的新增功能。

**修复**

* 增加了删除头像的功能。
* 修复了无法取消关联 [!DNL Adobe Media Optimizer] 帐户的问题。

**已知问题**

* 删除 Experience Cloud 资产中的图像时，如果该图像同时被 Adobe Target Essentials 使用，则不会发出警告。
* 在 [!DNL Analytics] 中刷新信息卡有时会导致扩展信息卡中出现空图表。
* 用户必须先注销，然后再次登录，才能使所有许可和授权更改生效。
* 如果未在登录期间选择 *`Remember me`*，则用户将在 15 分钟后被注销。
* [!DNL Analytics] 解决方案登录页面显示格式错误。
* 资产信息卡视图中的“评论”链接不可点击。
* 当多个用户同时使用 Experience Cloud 界面时，该界面速度可能会减慢
* 如果 [!DNL Adobe Target] 登录凭据可以在多个 Target 服务器上使用，则 Experience Cloud 无法关联到 [!DNL Adobe Target]。
* 登录到 Experience Cloud 需要花费超过一秒钟的时间。
* 在将自定义标签添加到资产后，没有任何其他元数据更改可以持久保留。
* 在 Experience Cloud 中创建了某个用户后，[!DNL Adobe Media Optimizer] 不会自动创建该用户。
* 组合框内用于添加新用户的选项在键入内容时暂时消失。
* 从 [!DNL Media Optimizer] 共享的数据不能在 Experience Cloud 中正确显示。
* 共享 Flickr 图像失败。
* 从 [!DNL Analytics] 对趋势报表应用的过滤器不会应用到 Experience Cloud 中的信息卡。
* 只有在重新登录之后，用户管理中执行的群组和授权更改才会生效。
* 无法在“[!DNL Search&Promote]组织和产品访问[!UICONTROL ”页面中关联 ]。
* 用户需要刷新展示板才能使已删除的信息卡在视图中消失。
* 某些 Excel 或 CSV 文件无法上传至展示板。
* [!DNL Adobe Media Optimizer] 模拟信息卡未正确呈现。
* 某些 PNG 文件无法在信息卡中呈现。
* 无法提交测试版反馈。

## 14.2.1 版 - 2014 年 2 月 24 日 {#section_5AD81B0737C843AFB4BE9C4420D70EB3}

<table id="table_DFAB002358C94A17A7F91DAB323A488F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 功能 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>OEmbed </p> </td> 
   <td colname="col2"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>刷新数据 </p> </td> 
   <td colname="col2"> <p> 
     <!--MAC-18174-->现在，如果解决方案不允许数据刷新，则信息卡上图像的<span class="uicontrol">刷新数据</span>图标会隐藏。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**修复**

* 修复了阻止共享 [!DNL Analytics] 报表应用区段过滤器的问题。
* 修复了导致即使未关联解决方案帐户，“[!UICONTROL Experience Cloud 解决方案]”页面上的解决方案也显示为已关联的问题。
* 修复了亚洲的 [!DNL Adobe Target] 客户无法单击关联页面上的 **[!UICONTROL 继续访问 Experience Cloud]** 按钮的问题。
* 修复了阻止共享 Youtube 视频的问题。
