---
description: 关于 Analytics 和 Target 中的客户属性的常见问题解答和最佳实践
keywords: customer attributes
seo-description: 关于 Analytics 和 Target 中的客户属性的常见问题解答和最佳实践
seo-title: 常见问题解答、各种限制和最佳实践
solution: Experience Cloud
title: 常见问题解答、各种限制和最佳实践
uuid: e93eb531-23c7-4d75-92e8-75699f58546a
translation-type: tm+mt
source-git-commit: 73cb227d2b44024706ce24a9ae6aa06c57a8ce85

---


# 常见问题解答、各种限制和最佳实践

关于 Analytics 和 Target 中的客户属性的常见问题解答和最佳实践

## 最佳实践和限制 {#section_7F5189B3DAA84EE6865B91D2026EE05A}

使用客户属性的指导和限制。

| 问题 | 描述 |
|--- |--- |
| 客户属性订阅限制 | 当您升级到 Analytics Premium 时，附加属性会在延迟 24 小时后才可用。在此延迟期间，您可能会看到出现属性订阅达到最大值错误。 |
| 同一设备上的多个登录 | 当使用客户属性将客户档案上传到数据源时，Adobe建议共享相同设备（即同一Experience Cloud ID）的用户不要这样做。 这样做可能导致ECID服务（该服务在设备上仍然存在）在同一Experience Cloud ID下链接多个用户，从而导致意外结果 [!DNL Target]。 **** 注意：对于Mobile，安装Mobile应用程序后ECID是永久的，您必须重新安装该应用程序才能生成新ECID。 对于Web，在清除浏览器Cookie后将生成新ECID。 |
| 每日频率上传限制 | Adobe建议您每天只更新一次客户属性。 您必须等待至少24小时才能为同一组配置文件上传另一个客户配置文件数据文件。 |
| Custom Analytics ID (`s.visitorID`) | 使用 `s.visitorID` 设置客户 ID 是在 Analytics 中标识用户的一种方法。但是，当使用 `s.visitorID.`<br>This包括（但不限于）共享受众、Analytics for Target(A4T)和客户属性来标识访客时，使用ID服务导出或导入Analytics数据的集成将不起作用。<br>对于这些集成，不支持设置自定义 Analytics ID。 |
| Analytics 中的字符长度限制 | 在创建 Analytics 订阅时，上传文件的字段长度会被截断为 255 个字符。 |

## 关于客户属性的常见问题解答 {#section_E47866EEA83348E09FE43CEC5E44C461}

<table id="table_88631069013B408EBB0A810657662B36"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 问题 </th> 
   <th colname="col2" class="entry"> 回答 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>我能收到关于客户属性上传状态的通知吗？ </p> </td> 
   <td colname="col2"> <p>可以。请参阅<a href="../admin-getting-started/organizations.md#concept_0105453AD71847B8BFCAF4A40915F157" format="dita" scope="local">管理通知</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 若要初步了解客户属性，我需要做哪些工作？ </p> </td> 
   <td colname="col2"> 
    <ol id="ol_1FACEF0990B6486B8DE86245D17695A8"> 
     <li id="li_F0C1542853684F8591FDC1B441D31A56"> <p>进行配置。 </p> <p>如果您是 <b>Analytics</b> 客户，Adobe 则会为您配置客户属性。如果您仅使用 <b>Target</b> 并且不具备 Analytics，则必须联系客户关怀团队，以请求配置核心服务。 </p> </li> 
     <li id="li_444FEDEE4B7244F79BA847662F5B17CB"> <p>与您的 CRM 团队进行沟通。找出哪类客户数据可以在 Analytics 及整个 Experience Cloud 中使用。 </p> </li> 
     <li id="li_32D4AAF8C29748A78801A0E1BFB37AF5"> <p>实施核心服务。 </p> <p>请参阅<a href="../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C" format="dita" scope="local"> 快速入门 - 为核心服务启用解决方案</a>，以了解如何使您的核心服务实施符合现代化要求。（请参阅关于同步客户 ID 的部分，以了解重要信息。） </p> </li> 
    </ol> <p> <b>注意：</b>有关针对管理员的核心服务实施常见问题解答，请访问<a href="../admin-getting-started/faq.md#concept_13219B4E51784577B6FF78AAA203DE91" format="dita" scope="local">此处</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 我可以使用多少个客户属性？ </p> </td> 
   <td colname="col2"> <p>您可以向客户属性服务上传数百个 <span class="filepath">.csv</span> 列。但是，在配置订阅和选择属性时，会根据您拥有的解决方案应用以下限制（每个报表包）:</p> <p> 
     <ul>
     <li>Foundation：0 个</li>
     <li>Select：3 个</li>
     <li>Prime：15 个</li>
     <li>Ultimate：200 个</li>
     <li>Standard：总共允许 3 个</li>
     <li>高级：200</li>
     <li>Target Standard：5 个</li>
     <li>Target Premium：200 个</li></ul>
     </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>必须要迁移到 Experience Cloud ID 服务吗？ </p> </td> 
   <td colname="col2"> <p>迁移与否取决于您使用的解决方案。 </p> <p> 
     <ul id="ul_9C473434B5DA4C6299AAB209DEDFCDE7"> 
      <li id="li_8BC10EB2825F4ADF8CA61F71D4994A28"> <b>Adobe Analytics：</b>强烈建议迁移 </li> 
      <li id="li_56F518E3F3DF4C93B6F7EF3B40ACC52F"> <b>Adobe Target：</b>必须迁移。 </li> 
     </ul> </p> <p>使用 ID 服务可增强该功能，并使您有机会使用最新的 Experience Cloud 功能，包括实时受众、Target 现代化、Analytics 集成和视频心跳跟踪。 </p> <p>有关详细信息，请参阅<a href="../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C" format="dita" scope="local">核心服务 - 如何启用您的解决方案</a>。 </p> <p> <b>注意</b>:Experience Cloud ID服务 <span class="term"> ，是对以前称为</span> Analytics访客ID服务的现代化实施 <span class="term"></span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>客户属性功能如何与 Adobe Audience Manager 关联？ </p> </td> 
   <td colname="col2"> <p>虽然 Audience Manager 可以接收数据以执行受众识别，它却无法执行分析功能以将属性关联到历史行为数据，或提供 Adobe Analytics 中可用的报告、分析和区段功能。“人员”核心服务允许绑定来自不同解决方案的大量数据，并与单一 ID 关联，进而可以在 Experience Cloud 中使用。 </p> <p> 在 Adobe Target 中，客户属性显示为单独的属性，它们可以与其他规则组合在一起，以便构建受众。“人员”核心服务中共享的受众属于完整的受众，无法对其进行修改。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>（仅限 Analytics）</b>此功能与 Analytics Premium 中提供的功能有何区别？ </p> </td> 
   <td colname="col2"> <p>以前，如果客户希望将客户属性数据与 Analytics 数据组合在一起，他们需要大大依赖 Data Workbench 工具来实现此功能。通过将客户属性作为 Reports &amp; Analytics、Ad Hoc Analysis 和 Report Builder 中的维度和量度，使更多受众有机会使用此功能。Analytics Standard 客户将有权访问客户属性，但其功能有限。Analytics Premium 客户可以使用其完整的功能。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>（仅限 Target）</b>我可以预先加载或上传从未在 Target 中出现过的客户数据吗？ </p> </td> 
   <td colname="col2"> <p> 可以。在访客向 Target 提出第一个请求时，系统将从客户属性中提取我们目前所拥有的关于他们的信息，并使用该数据进行定位。 </p> <p> <p>注意：此数据的检索过程可能需要多达 20 分钟，从访客首次与 Target 交互开始算起。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>（仅限 Target）</b>我可以通过将客户属性数据与共享受众数据合并在一起来创建超级受众吗？ </p> </td> 
   <td colname="col2"> <p>否。共享受众数据是已完成的受众。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>（仅限 Target）</b>客户属性功能与 Target 的批量配置文件 API 相比有何不同？ </p> </td> 
   <td colname="col2"> <p> 可直接通过<a href="https://www.adobe.io/apis/experiencecloud/target.html" format="https" scope="external">批量配置文件 API</a>，逐个或批量更新 Target 配置文件。该功能类似于客户属性，但又存在以下不同之处： </p> 
    <ul id="ul_5AAA4A8497C04F50A8AAA9F776BB868E"> 
     <li id="li_B20AEA397F3B4C86A1140CDA61ABD575">配置文件 API 是一个 REST API 调用，而客户属性使用的是 FTP。 </li> 
     <li id="li_7FBE428EF5D34B6AA09B6368E8210344">Target 的配置文件 API 仅向 Target 而并非向整个 Experience Cloud 发送数据。 </li> 
     <li id="li_CBB4D3FAF53944E0A066A4AD9F9C8760">客户属性提供了一个简单的界面来创建和管理此外部数据。 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>（仅限 Target）</b>从客户属性向 Adobe Target 上传数据时，是否会延长 Target 访客的配置文件生命周期？ </p> </td> 
   <td colname="col2"> <p>能。请参阅 Adobe Target 帮助中的<a href="https://docs.adobe.com/content/help/en/target/using/audiences/visitor-profiles/visitor-profile.html" format="https" scope="external">访客配置文件生命周期</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>（仅限 Target）</b>根据客户 ID 识别访客后，我能否立即定位在客户属性中上传的数据？ </p> </td> 
   <td colname="col2"> <p>是. </p> <p>在对 Target 进行的服务器调用中（其中包括 mbox 第三方 ID），所有客户属性数据都将可用。 </p> </td> 
  </tr> 
    <tr> 
   <td colname="col1"> <p> <b> （仅限Target）</b> “同步状态”列对于在客户属性来源中上传的文件表示什么？ </p> </td> 
   <td colname="col2"> <p> 通过单击特定属性文件的“同步状态”图标，可以查看由Target发布和同步的记录数。 “同步%”是一个实时度量，它指定在Target中同步的配置文件的%。 </p> <p> <b></b> 注意：与Target同步的属性可能需要24小时。 </p>
 </td> 
  </tr> 
 </tbody> 
</table>
