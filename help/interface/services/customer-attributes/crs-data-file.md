---
description: 了解上传 [!DNL customer attributes] 到Experience Cloud的数据文件要求和多个数据源。
solution: Experience Cloud
title: 数据文件和数据源
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: e2dfe10d-7003-4afa-a5e6-57703d74efd4
source-git-commit: 2f126877f6a5f090884ebe093f35e4f6d90b4df6
workflow-type: tm+mt
source-wordcount: '1154'
ht-degree: 64%

---

# 关于[!DNL customer attributes]的数据文件和数据源

将[!DNL customer attributes]上传到Experience Cloud的数据文件要求和多个数据源。

您需要拥有从企业访问 CRM 或类似数据的权限。您上传到Experience Cloud的数据必须是`.csv`文件。 如果您通过 FTP 或 sFTP 上传，则还需要上传一个 `.fin` 文件。

[!DNL customer attributes]设计为每天处理一些文件。 为了缓解延迟处理较多小文件的问题，在处理前一批文件后 30 分钟内由同一组织发送的文件将被路由到优先级较低的队列。

## 允许的文件类型和命名要求 {#section_6F64FA02ACCC4215B0862CB6A1821FBF}

| 文件类型 | 描述 |
|--- |--- |
| `.csv` | 以逗号分隔的值文件（例如在 Excel 中创建的文件）。此文件包含客户属性数据。   命名要求：请确保文件扩展名不包含空格。 |
| `.fin` | （必需） `.fin`文件会告知系统您已完成数据上传。 `.fin`文件的名称必须匹配`.csv`文件的名称。  Adobe建议创建一个扩展名为`.fin`的空文本文件。 空文件可节省空间和上传时间。 **注意：**&#x200B;不允许在上传文件后重命名`.fin`文件。 `.fin`文件必须单独上传，并且不能是之前已上传的重命名文件。 在客户属性FTP中上传`.fin`文件后，系统会快速检索数据（在一分钟之内）。 其他基于FTP的Adobe系统则与之不同，后者提取数据并不那么频繁（大约每小时一次）。 使用拖放上传方法时不需要`.fin`文件。 |
| `.gz`或`.zip` | `.gz` (gzip)或`.zip` — 用于压缩文件。 `.zip`文件不能在存档中包含多个文件。 命名要求： `.zip`或`.gz`的名称应与`.csv`文件的名称匹配。 例如，如果`.csv`文件是`crm_small.csv`，则`.zip`文件应该是`crm_small.csv.zip`。 `.fin`文件必须匹配`.csv`。 |


## 属性数据文件的要求 {#section_169FBF5B7BBA47CE825B7A330CF3FE98}

**CSV 示例**

CSV 文件必须遵循以下格式：

![属性数据文件的要求](assets/cvs.png)

在文本编辑器中查看的同一文件：

![属性数据文件的要求](assets/csv_txt.png)

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
   <td colname="col2"> <p>拖放文件应小于 100 MB。 </p> <p>在使用拖放上传方法时不需要 <span class="filepath">.fin</span> 文件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>客户ID列 </p> </td> 
   <td colname="col2"> <p> 第一列必须是唯一的客户 ID。使用的 ID 应该与传递给 Experience Cloud ID 服务的 ID 相对应。 </p> <p>对于 Analytics，其为存储在 prop 或 eVar 中的 ID。 </p> <p>对于Target，设置customerID值。 </p> <p> 此客户 ID 是 CRM 在数据库中针对每个人使用的唯一标识符。其余列为来自 CRM 的属性。您选择要上传的属性数量。 </p> <p>建议对列标题使用友好、可读的名称，但不是必需的。当您在上传后验证架构时，可以将友好名称映射到上传的行和列。 </p> <p> <b>关于客户ID</b> </p> <p>企业通常使用 CRM 系统中的客户 ID。此ID是在人员登录时使用<span class="codeph"> setcustomerIDs </span>调用设置的。 在上传到Experience Cloud的CRM文件中，还使用此ID作为密钥。 <a href="t-crs-usecase.md" format="dita" scope="local">别名 ID</a> 是 Audience Manager 中数据存储的友好名称，其中存储了别名数据。系统将别名发送到此数据存储（通过setcustomerID）。 CRM 文件将应用于该数据存储中的数据。 </p> <p>有关<span class="codeph"> setcustomerID </span>的信息，请参阅<a href="https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html?lang=zh-Hans" format="https" scope="external">客户ID和身份验证状态</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>后续标题和列 </p> </td> 
   <td colname="col2"> <p>后续标题应表示每个属性的名称。 </p> <p> 这些列应包含来自 CRM 的客户属性。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>属性限制 </p> </td> 
   <td colname="col2"> <p>您可以向Experience Cloud中的客户属性服务上传数百个<span class="filepath"> .csv </span>列。 但是，在配置订阅并选择属性时，根据您拥有的应用程序，将会受到以下限制： </p> <p> 
     <ul id="ul_2BB85067918D4BB3B59394F3E3E37A6D"> 
      <li id="li_93703988B9934384B4B94A839D028380"> <b>Analytics Standard</b>：总共 3 个 </li> 
      <li id="li_D1E5E7BD24C54591B14D15DE97447835"> <b>Analytics Premium</b>：每个报表包 200 个 </li> 
      <li id="li_8C891FE3D1EF49FA9F81E2E32CD0B9CA"> <b>Adobe Target Standard：</b>5 个 </li> 
      <li id="li_2B66D43023F34EA685CE2C38A9250CEA"> <b>Adobe Target Premium：</b>200 个 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>行数限制 </p> </td> 
   <td colname="col2"> <p>对行数的限制未知。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>列数限制 </p> </td> 
   <td colname="col2"> <p>为实用起见，请将列数限制在 200 左右。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>字符限制 </p> </td> 
   <td colname="col2"> <p>创建 Analytics 订阅时，已上传文件的字段长度将被截断为 255。 </p> </td> 
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
   <td colname="col2"> <p> 每个属性来源应包含相同数量且以逗号分隔的字段。 </p> <p> 包含换行符、双引号或逗号的字段必须加引号。 </p> <p> 字段中的双引号字符必须使用反斜杠 (\) 进行转义。 </p> <p> 空列将存储为 <span class="term">null</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>多个文件 </p> </td> 
   <td colname="col2"> <p>上传客户属性数据时，如果您要快速且连续上传多个文件，尤其是文件较大时，请确保在上一个文件处理完成之后再上传下一个文件。您可以通过查看上一个文件被移动到[!UICONTROL 客户属性] FTP帐户中已处理或失败文件夹中的时间来监控上传情况。 </p> <p> 如果将大文件分成较小的文件，并连续快速提交这些文件，实际上可能会减慢处理速度，除非您可以确保在提交下一个文件之前已完成处理每个文件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>字符编码 </p> </td> 
   <td colname="col2"> <p>对于日文，必须使用 UTF-8。 </p> </td> 
  </tr> 
   <tr> 
   <td colname="col1"> <p>历史数据 </p> </td> 
   <td colname="col2"> <p> 客户属性与[!DNL Analytics]中的基础访客配置文件关联。 因此，在[!DNL Analytics]中，[!UICONTROL 客户属性]在访客配置文件的整个生命周期内都与该访客相关联。 该轮廓包括客户首次登录之前发生的行为。 </p> <p> 如果使用的是 Data Warehouse 回填方法，则数据将绑定到基于 Analytics ID (AID) 的 post_visid_high/low。如果使用的是 Experience Cloud ID 服务，则数据将绑定到基于 Experience Cloud ID (MID) 的 post_visid_high/low。 </p> <p> 请注意，从2022年10月开始，Data Warehouse回填方法将不再可用。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>数据馈送 </p> </td> 
   <td colname="col2"> <p>客户属性在数据馈送中不可用。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 使用多个数据源 {#multiple}

创建、修改或删除客户属性来源时，大约会有一小时的延迟。在此之后，ID 才开始与新的数据源进行同步。

每个客户属性来源的别名 ID 必须是唯一的。如果您有多个数据源使用同一 ID，可按照以下方式对其进行设置：

**在 VisitorAPI.js 或 Dynamic Tag Management 的 Experience Cloud ID 工具中：**

设置两个客户 ID，使其分别对应于适当的数据源：

```
Visitor.setcustomerIDs({ 
     "ds_id1":"123456", 
     "ds_id2":"123456" 
});
```

（有关详细信息，请参阅[客户ID和身份验证状态](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html?lang=zh-Hans)。）

在&#x200B;**[!UICONTROL Experience Cloud]** > **[!UICONTROL 客户属性]**&#x200B;中：

使用与上述客户 ID 对应的唯一别名 ID 创建两个客户属性来源。使用此方法可以将相同的引用 ID 发送到多个客户属性来源。
