---
description: 将客户属性上传到 Experience Cloud 的数据文件要求和多个数据源。
keywords: customer attributes;core services
seo-description: 将客户属性上传到 Experience Cloud 的数据文件要求和多个数据源。
seo-title: 关于客户属性的数据文件和数据源
solution: Experience Cloud
title: 关于客户属性的数据文件和数据源
uuid: 9dd0e364-889b-45db-b190-85c0930a101e
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# 关于客户属性的数据文件和数据源

将客户属性上传到 Experience Cloud 的数据文件要求和多个数据源。

您需要从企业访问CRM或类似数据。 您上传到 Experience Cloud 的数据必须是 `.csv` 文件。如果您通过 FTP 或 sFTP 上传，则还需要上传一个 `.fin` 文件。

上传客户属性是为了每天处理一些文件。为了缓解延迟处理大量小文件的问题，在处理前一批文件后 30 分钟内由同一组织发送的文件将被路由到优先级较低的队列。

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
   <td colname="col2"> <p>以逗号分隔的值文件（如在Excel中创建的文件）。 这是包含客户属性数据的文件。 </p> <p> <b>命名要求：</b> 确保文件扩展名不包含空格。 </p> </td> 
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



**示例CSV**

CSV文件必须遵循以下格式：

示例CSV:

![](assets/cvs.png)

在文本编辑器中查看的同一文件：

![](assets/csv_txt.png)

**准则**

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
   <td colname="col2"> <p>拖放文件应小于100 MB。 </p> <p>在使用拖放上传方法时不需要 <span class="filepath">.fin</span> 文件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>客户ID列 </p> </td> 
   <td colname="col2"> <p> 第一列必须是唯一的客户ID。 使用的ID应与传递到Experience Cloud ID服务的ID相对应。 </p> <p>对于Analytics,ID存储在prop或eVar中。 </p> <p>对于目标,setCustomerID值。 (See <a href="../core-services/core-services.md#section_AD473A6A21C1446498E700363F9A8437" format="dita" scope="local"> Analytics &amp; Adobe Target - synching the customer ID </a>) </p> <p> 此客户ID是CRM为数据库中的每个人使用的唯一标识符。 其余的列是来自您的CRM的属性。 您将选择要上传的属性数。 </p> <p>建议对列标题使用易记、可读的名称，但不要求。 在上传后验证模式时，可以将友好名称映射到已上载的行和列。 </p> <p> <b>关于客户ID</b> </p> <p>通常，企业使用CRM系统中的客户ID。 此 ID 是在人员登录时使用 <span class="codeph">setCustomerIDs</span> 调用设置的。此ID还用作上传到Experience Cloud的CRM文件中的密钥。 An <a href="../attributes/t-crs-usecase.md#task_09DAC0F2B76141E491721C1E679AABC8" format="dita" scope="local"> Alias ID </a> is a friendly name for a data store in Audience Manager, where the alias data is stored. 系统将别名发送到此数据存储（通过setCustomerID）。 CRM文件将应用于该数据存储中的数据。 </p> <p>有关 <span class="codeph">setCustomerIDs</span> 的信息，请参阅<a href="https://docs.adobe.com/content/help/en/id-service/using/reference/authenticated-state.html" format="https" scope="external">客户 ID 和身份验证状态</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>后续标题和列 </p> </td> 
   <td colname="col2"> <p>后续的标题应代表每个属性的名称。 </p> <p> 这些列应包含来自CRM的客户属性。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>属性限制 </p> </td> 
   <td colname="col2"> <p>您可以向 Experience Cloud 中的客户属性服务上传数百个 <span class="filepath">.csv</span> 列。但是，在配置订阅和选择属性时，根据您拥有的解决方案，以下限制适用： </p> <p> 
     <ul id="ul_2BB85067918D4BB3B59394F3E3E37A6D"> 
      <li id="li_93703988B9934384B4B94A839D028380"> <b>Analytics Standard</b>:3共 </li> 
      <li id="li_D1E5E7BD24C54591B14D15DE97447835"> <b>Analytics Premium</b>:每个报告包200个 </li> 
      <li id="li_8C891FE3D1EF49FA9F81E2E32CD0B9CA"> <b>Adobe目标标准：</b> 5 </li> 
      <li id="li_2B66D43023F34EA685CE2C38A9250CEA"> <b>Adobe目标高级版：</b> 200 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>行限制 </p> </td> 
   <td colname="col2"> <p>对行数没有已知限制。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>列限制 </p> </td> 
   <td colname="col2"> <p>为实用起见，将列数限制在200左右。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>字符限制 </p> </td> 
   <td colname="col2"> <p>创建Analytics订阅时，上传文件的字段长度会被截断为255。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>FTP 指南和大小限制 </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_E157EE6F98914EADA0C103D1D1E705D3"> 
      <li id="li_84FBD455DD164A28AC16F4A5AB19E4B3">FTP 的最大文件大小限制为每次上传 4 GB。 </li> 
      <li>最小文件大小限制为每次上传 10 MB。 </li>
      <li>您可以每半小时上传一个文件。 </li>
      <li id="li_B69A20C51D824727AA99C1F6F78537A4"> 您应当将您的 <span class="filepath">.csv</span>（和 <span class="filepath">.fin</span>）文件放在 FTP 站点的根文件夹中。 </li> 
     </ul> </p> <p> <p>重要提示：FTP 帐户允许的总空间量为 40 GB。您有责任删除已处理的文件。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>文件要求 </p> </td> 
   <td colname="col2"> <p> 每个属性源应包含相同数量的以逗号分隔的字段。 </p> <p> 包含换行符、多次引号或逗号的字段必须加引号。 </p> <p> 字段中的多次引号字符必须使用反斜杠(\)进行转义。 </p> <p> 空列存储为 <span class="term"> null </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>多个文件 </p> </td> 
   <td colname="col2"> <p>上传客户属性数据时，如果您要快速且连续上传多个文件，尤其是文件较大时，请确保在上一个文件处理完成之后再上传下一个文件。您可以通过查看上一个文件被移动到客户属性 FTP 帐户中已处理或失败文件夹中的时间来监控上传情况。 </p> <p> 如果将大文件分成较小的文件，并连续快速提交这些文件，实际上可能会减慢处理速度，除非您可以确保在提交下一个文件之前已完全处理每个文件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>字符编码 </p> </td> 
   <td colname="col2"> <p>对于日本，UTF-8是必填项。 </p> </td> 
  </tr> 
   <tr> 
   <td colname="col1"> <p>历史数据 </p> </td> 
   <td colname="col2"> <p> 客户属性与Analytics中的基础访客用户档案相关联。 因此，在Analytics中，客户属性与该访客的整个生命周期中的访客相关联。 这包括在客户首次登录之前发生的行为。 </p> <p> 如果使用数据仓库回填方法，则数据将绑定到基于Analytics ID(AID)的post_visid_high/low。 如果您使用的是Experience Cloud ID服务，则数据将绑定到基于Experience Cloud ID(MID)的post_visid_high/low。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>数据馈送 </p> </td> 
   <td colname="col2"> <p>客户属性在数据馈送中不可用。 </p> </td> 
  </tr> 
 </tbody> 
</table>


## 利用多个数据源 {#section_76DEB6001C614F4DB8BCC3E5D05088CB}

在创建、修改或删除客户属性源时，在ID开始与新数据源同步前约有一小时的延迟。

每个客户属性来源的别名ID必须是唯一的。 如果您有多个使用同一ID的数据源，则应按如下方式设置它们：

**在VisitorAPI.js或动态标签管理中的Experience Cloud ID工具中：**

设置两个客户 ID，使其分别对应于适当的数据源：

```
Visitor.setCustomerIDs({ 
     "ds_id1”:"123456", 
     "ds_id2":"123456" 
});
```

(See [Customer IDs and Authentication States](https://docs.adobe.com/content/help/en/id-service/using/reference/authenticated-state.html) for more information.)

In the **[!UICONTROL Experience Cloud]** > **[!UICONTROL People]** > **[!UICONTROL Customer Attributes]**:

使用与上述客户ID对应的唯一别名ID创建两个客户属性来源。 使用此方法可将相同的引用ID发送到多个客户属性源
