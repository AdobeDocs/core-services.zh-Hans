---
description: 将客户属性上传到 Experience Cloud 的数据文件要求和多个数据源。
keywords: 客户属性；核心服务
seo-description: 将客户属性上传到 Experience Cloud 的数据文件要求和多个数据源。
seo-title: 关于客户属性的数据文件和数据源
solution: Experience Cloud
title: 关于客户属性的数据文件和数据源
uuid: dd0e364-889b-45db-b190-85c0930 a101 e
translation-type: tm+mt
source-git-commit: bae7ac2bc620fc0f9ac149f7dce84fa70e1355c9

---


# 关于客户属性的数据文件和数据源

将客户属性上传到 Experience Cloud 的数据文件要求和多个数据源。

您需要具备贵企业 CRM 或类似数据的访问权限。上传至Experience Cloud的数据必须是 [!DNL .csv] 文件。如果您通过FTP或SFTP上传，还可以上传 [!DNL .fin] 文件。

客户属性每天只需处理几个文件。为减轻大量小文件的延迟处理问题，从同一组织的先前批次的30分钟内发送的文件将路由到较低优先级队列。

<!-- <p>Articulate difference between this and SAINT. </p> -->

## 允许的文件类型和命名要求 {#section_6F64FA02ACCC4215B0862CB6A1821FBF}


<table id="table_C27955F6B52A45B28BEEAAF14FFC86D8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 文件类型 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> .csv </span> </p> </td> 
   <td colname="col2"> <p>逗号分隔值文件（例如在 Excel 中创建的文件）。这个文件包含客户属性数据。 </p> <p> <b>命名要求：</b>确保文件扩展名不包含空格。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> .fin </span> </p> </td> 
   <td colname="col2"> <p>（必需）<span class="filepath">.fin</span> 文件会告知系统您已完成数据上传。<span class="filepath">.fin</span> 文件的名称必须匹配 <span class="filepath">.csv</span> 文件的名称。 </p> <p>Adobe 建议创建一个具有 <span class="filepath">.fin</span> 扩展名的空文本文件。空文件可节省空间和上传时间。 </p> <p> <p>注意：不允许重新命名已上传的 <span class="filepath">.fin</span> 文件。<span class="filepath">.fin</span> 文件必须单独上传，并且不得是之前已上传的重命名文件。 </p> </p> <p>在客户属性 FTP 中上传 <span class="filepath">.fin</span> 文件后，系统会快速检索数据（在一分钟之内）。其他基于 FTP 的 Adobe 系统则与之不同，它们提取数据并不那么频繁（大约每小时一次）。 </p> <p>在使用拖放上传方法时不需要 <span class="filepath">.fin</span> 文件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> .gz</span> 或 <span class="filepath">.zip </span> </p> </td> 
   <td colname="col2"> <p> <span class="filepath">.gz</span> (gzip) 或 <span class="filepath">.zip</span> - 用于压缩文件。<span class="filepath">.zip</span> 文件不能在存档中包含一个以上的文件。 </p> <p> <b>命名要求：</b><span class="filepath">.zip</span> 或 <span class="filepath">.gz</span> 的名称必须匹配 <span class="filepath">.csv</span> 的名称。例如，如果您的 <span class="filepath">.csv</span> 文件是 <span class="filepath">crm_small.csv</span>，则 <span class="filepath">.zip</span> 文件应为 <span class="filepath">crm_small.csv.zip</span>。 </p> <p>.fin 文件必须匹配 .csv 文件。 </p> </td> 
  </tr> 
 </tbody> 
</table>


## 属性数据文件的要求 {#section_169FBF5B7BBA47CE825B7A330CF3FE98}



**示例 CSV**

CSV 文件必须符合以下格式：

示例 CSV：

![](assets/cvs.png)

在文本编辑器中查看的相同文件：

![](assets/csv_txt.png)

**指南**

<table id="table_A9849CC9AA784763921DE057F0F61515"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 项目 </th> 
   <th colname="col2" class="entry"> 描述 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>拖放 </p> </td> 
   <td colname="col2"> <p>拖放文件应当小于 100 MB。 </p> <p>在使用拖放上传方法时不需要 <span class="filepath">.fin</span> 文件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>客户 ID 列 </p> </td> 
   <td colname="col2"> <p> 第一列必须是一个唯一客户 ID。使用的 ID 应当与将要传送至 Experience Cloud ID 服务的 ID 相对应。 </p> <p>对于 Analytics，该 ID 存储在 prop 或 eVar 中。 </p> <p>对于 Target，该 ID 为 setCustomerID 值。（请参阅 <a href="../core-services/core-services.md#section_AD473A6A21C1446498E700363F9A8437" format="dita" scope="local">Analytics 和 Target - 同步客户 ID</a>） </p> <p> 此客户 ID 是您的 CRM 用于数据库中每位人员的唯一标识符。其余的列是来自您的 CRM 的属性。您将选择要上传多少个属性。 </p> <p>建议使用易记好读的列标题名称，但也不是必需的。在上传后验证架构时，您可以将易记的名称映射到已上传的行和列。 </p> <p> <b>关于客户 ID</b> </p> <p>通常情况下，企业使用来自 CRM 系统的客户 ID。此 ID 是在人员登录时使用 <span class="codeph">setCustomerIDs</span> 调用设置的。此 ID 还用作上传到 Experience Cloud 的 CRM 文件中的键值。an<a href="../attributes/t-crs-usecase.md#task_09DAC0F2B76141E491721C1E679AABC8" format="dita" scope="local">别名 ID</a> 是 Audience Manager 中数据存储的友好名称，其中存储了别名数据。系统会将别名发送到此数据存储（通过 setCustomerIDs）。CRM 文件将被应用到该数据存储中的数据。 </p> <p>有关 <span class="codeph">setCustomerIDs</span> 的信息，请参阅<a href="https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-authenticated-state.html" format="https" scope="external">客户 ID 和身份验证状态</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>后续的标题和列 </p> </td> 
   <td colname="col2"> <p>后续的标题应表示每个属性的名称。 </p> <p> 这些列应当包含来自 CRM 的客户属性。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>属性限制 </p> </td> 
   <td colname="col2"> <p>您可以向 Experience Cloud 中的客户属性服务上传数百个 <span class="filepath">.csv</span> 列。但是，在配置订阅和选择属性时，根据您拥有的解决方案，将会受到以下限制： </p> <p> 
     <ul id="ul_2BB85067918D4BB3B59394F3E3E37A6D"> 
      <li id="li_93703988B9934384B4B94A839D028380"> <b>Analytics Standard</b>：总共 3 个 </li> 
      <li id="li_D1E5E7BD24C54591B14D15DE97447835"> <b>Analytics Premium</b>：每个报表包 200 个 </li> 
      <li id="li_8C891FE3D1EF49FA9F81E2E32CD0B9CA"> <b>Target Standard：</b>5 个 </li> 
      <li id="li_2B66D43023F34EA685CE2C38A9250CEA"> <b>Target Premium：</b>200 个 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>行限制 </p> </td> 
   <td colname="col2"> <p>行的数量不存在已知的限制。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>列限制 </p> </td> 
   <td colname="col2"> <p>从实用性考虑，列的数量限制在 200 个左右。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>字符限制 </p> </td> 
   <td colname="col2"> <p>在创建 Analytics 订阅时，上传文件的字段长度会被截断为 255 个字符。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>FTP 指南和大小限制 </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_E157EE6F98914EADA0C103D1D1E705D3"> 
      <li id="li_84FBD455DD164A28AC16F4A5AB19E4B3">每个上传的FTP最大文件大小限制为GB。 </li> 
      <li>每次上传的最小文件大小限制为10MB。 </li>
      <li>您可以每半小时上传一个文件。 </li>
      <li id="li_B69A20C51D824727AA99C1F6F78537A4"> 您应当将您的 <span class="filepath">.csv</span>（和 <span class="filepath">.fin</span>）文件放在 FTP 站点的根文件夹中。 </li> 
     </ul> </p> <p> <p>重要提示：FTP 帐户允许的总空间量为 40 GB。您将负责删除处理后的文件。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>文件要求 </p> </td> 
   <td colname="col2"> <p> 每个属性来源应当包含相同数量的以逗号分隔的字段。 </p> <p> 包含换行符、双引号或逗号的字段必须用引号引起来。 </p> <p> 字段中的双引号字符必须使用反斜线 (\) 进行转义。 </p> <p> 空白列存储为 <span class="term"> null </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>多个文件 </p> </td> 
   <td colname="col2"> <p>上传客户属性数据时，如果您要快速上传多个文件，尤其是文件较大时，请确保之前的文件在上传下一个文件之前已经过处理。您可以通过检查上一个文件何时移至客户属性FTP帐户中的已处理或失败的文件夹来监控此操作。 </p> <p> 将大型文件分解为较小的文件并快速提交，实际上可能会减缓处理速度，除非在提交下一个文件之前确保每个文件得到完全处理。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>字符编码 </p> </td> 
   <td colname="col2"> <p>对于日本，必须使用 UTF-8。 </p> </td> 
  </tr> 
   <tr> 
   <td colname="col1"> <p>历史数据 </p> </td> 
   <td colname="col2"> <p> 客户属性绑定到 Analytics 中的基本访客资料。因此，在 Analytics 中访客资料的整个生命周期内，客户属性都与该访客关联。这包括客户首次登录之前发生的行为。 </p> <p> 如果您使用 Data Warehouse 回填方法，数据会绑定到基于 Analytics ID (AID) 的 post_visid_high/low。如果您正在使用 Experience Cloud ID 服务，数据会绑定到基于 Experience Cloud ID (MID) 的 post_visid_high/low。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>数据馈送 </p> </td> 
   <td colname="col2"> <p>客户属性不能用于数据馈送。 </p> </td> 
  </tr> 
 </tbody> 
</table>


## 利用多个数据源 {#section_76DEB6001C614F4DB8BCC3E5D05088CB}

创建、修改或删除客户属性来源时，大约会有一小时的延迟。在此之后，ID 才开始与新的数据源进行同步。

每个客户属性来源的别名 ID 必须是唯一的。如果有多个数据源使用相同的 ID，则应当遵循以下步骤对其进行设置：

**在 VisitorAPI.js 或动态标签管理的 Experience Cloud ID 工具中：**

设置两个客户 ID，使其分别对应于适当的数据源：

```
Visitor.setCustomerIDs({ 
     "ds_id1”:"123456", 
     "ds_id2":"123456" 
});
```

（请参阅[客户 ID 和身份验证状态](https://marketing.adobe.com/resources/help/en_US/mcvid/?f=mcvid_customer_ids)以了解详细信息。）

在 **[!UICONTROL Experience Cloud]** &gt; **[!UICONTROL “人员”]** &gt; **[!UICONTROL “客户属性]**”中：

使用与上方客户 ID 对应的唯一别名 ID 创建两个客户属性来源。使用这种方法，可以将同一参考 ID 发送至多个客户属性来源。
