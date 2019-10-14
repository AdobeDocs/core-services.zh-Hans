---
description: 如果您不使用拖放操作上传，则可以通过 FTP 将客户属性数据上传到 Experience Cloud。
keywords: 客户属性;核心服务
seo-description: 如果您不使用拖放操作上传，则可以通过 FTP 将客户属性数据上传到 Experience Cloud。
seo-title: 可选 - 通过 FTP 上传数据文件
solution: Experience Cloud
title: 可选 - 通过 FTP 上传数据文件
uuid: 5df565dd-b6f8-420e-981f-4b6fc6f7d0e4
translation-type: tm+mt
source-git-commit: d304e625bd2125854d9ed932674522284995e030

---


# 可选 - 通过 FTP 上传数据文件

如果您不使用拖放操作上传，则可以通过 FTP 将客户属性数据上传到 Experience Cloud。

当您在 Experience Cloud 中创建客户属性来源和 FTP 帐户后，可上传数据。您可以针对每个属性来源创建一个 FTP 帐户。已上传的文件存储在该帐户的根文件夹中。该数据必须为 `.csv` 格式，并通过另一个 `.fin` 文件指示上传已完成。

>[!IMPORTANT]
>
>在上传文件之前，先查看[上传客户属性的数据文件要求](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19)。

将文件上传到客户属性 FTP 站点可通过 FTP 或 SFTP 完成。

* 您需要一个支持 SFTP 连接的客户端。
* 你可以使用用户名/密码或不使用密码进行 SFTP 连接，如[此处](https://docs.adobe.com/help/en/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/ftp-sftp-cert-auth.html)所述。

**通过 FTP 上传数据文件的方法**

1. [创建客户属性来源并上传数据文件...](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78).

   确保您已登录到位于 [!DNL ftp.adobe.com/<sftpname>] 的 FTP 站点。

1. 单击&#x200B;**[!UICONTROL 操作]** &gt; **[!UICONTROL 文件上传]**。

1. 上传 `.fin` 文件，以便您的文件可被检索到。

   文件类型 `.fin` 是由用户创建的，表示上传已完成。它可以是一个空白的记事本文件。例如，如果您上传 [!DNL crs123.csv]，同时也会上传 [!DNL crs123.fin]。

   如果上传成功，这两个文件会被移到一个名为&#x200B;**已处理**&#x200B;的文件夹中。

   请参阅[上传客户属性的数据文件要求](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19)，以了解有关文件名和结构的重要信息。
