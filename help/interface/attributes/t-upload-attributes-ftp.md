---
description: 如果您不使用拖放操作上传，则可以通过 FTP 将客户属性数据上传到 Experience Cloud。
keywords: 客户属性；核心服务
seo-description: 如果您不使用拖放操作上传，则可以通过 FTP 将客户属性数据上传到 Experience Cloud。
seo-title: 可选 - 通过 FTP 上传数据文件
solution: Experience Cloud
title: 可选 - 通过 FTP 上传数据文件
uuid: 5df565dd-b6 f8-420e-981f-4b6 fc6 d7 d0 e4
translation-type: tm+mt
source-git-commit: 979b2202a70e2a5362aa86a65a17d7c4279b3a1a

---


# 可选 - 通过 FTP 上传数据文件

如果您不使用拖放操作上传，则可以通过 FTP 将客户属性数据上传到 Experience Cloud。

当您在 Experience Cloud 中创建客户属性来源和 FTP 帐户后，可上传数据。您可以针对每个属性来源创建一个 FTP 帐户。已上传的文件存储在该帐户的根文件夹中。数据必须 [!DNL .csv] 采用格式，另一 [!DNL .fin] 个文件则表示上传完成。

>[!IMPORTANT]
>
>查看 [上传客户属性](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) 前上传客户属性的数据文件要求。


将文件上传到客户属性 FTP 站点可通过 FTP 或 SFTP 完成。

* 您需要一个支持 SFTP 连接的客户端。
* 你可以使用用户名/密码或不使用密码进行 SFTP 连接，如[此处](https://marketing.adobe.com/resources/help/en_US/whitepapers/ftp/?f=ftp_sftp_cert_auth)所述。



<!-- <p>Error states - get with Matt and Dave </p> 
<p>What are the most common reasons for doing this? Retail? Do a use case example, then show an AN example. </p> 
<p>You create one FTP per attribute source. Files go to the root folder in that account. The file type .fin is user-created. (For example, upload a .csv then a .fin of the same name, which signals you have completed the upload. https://wiki.corp.adobe.com/display/marketingcloud/Customer+Record+Services#CustomerRecordServices-FileFormats (leverage for doc). Possibly link from FTP File Reqs page to a help file about naming conventions. Need a new file type page for this. Similar content here: https://marketing.adobe.com/resources/help/en_US/reference/c_general_file_structure.html and here: https://marketing.adobe.com/resources/help/en_US/whitepapers/ftp/ftp_datasources.html </p> 
<p>Drag-n-drop and zip functionality for uploads - 1/21/2015. S/b less than 100 megs for drag and drop zip file. Fin file not required for drag/drop. </p> 
<p>Preview Data - shows the last upload (?) </p> 
<p>Need a link to the "instructions" on that information icon with the image. </p> 
<p>Workflow: Drag and drop, validate schema, configure subscription, save/activate. </p> -->
**通过 FTP 上传数据文件的方法**

1. [创建客户属性来源并上传数据文件...](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78).

   确保您已登录FTP站点 [!DNL ftp. adobe. com/<sftpname>]。

1. 单击 **[!UICONTROL “操作]** ”&gt; **[!UICONTROL “文件上传]**”。

1. 上传 [!DNL .fin] 文件，以便检索文件。

   文件类型 [!DNL .fin] 由用户创建，并表示上传已完成。它可以是一个空白的记事本文件。例如，上传 [!DNL crs123.csv]后，您也可以上传 [!DNL crs123.fin]。

   如果上传成功，这两个文件会被移到一个名为 **已处理** 的文件夹中。


   请参阅[上传客户属性的数据文件要求](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19)，以了解有关文件名和结构的重要信息。
