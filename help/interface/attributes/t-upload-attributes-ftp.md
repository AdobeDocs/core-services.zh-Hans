---
description: 如果您不使用拖放操作上传，则可以通过 FTP 将客户属性数据上传到 Experience Cloud。
keywords: Customer Attributes;core services
seo-description: 如果您不使用拖放操作上传，则可以通过 FTP 将客户属性数据上传到 Experience Cloud。
seo-title: 可选 - 通过 FTP 上传数据文件
solution: Experience Cloud
title: 可选 - 通过 FTP 上传数据文件
uuid: 5df565dd-b6f8-420e-981f-4b6fc6f7d0e4
translation-type: tm+mt
source-git-commit: 0bc7032d0052ba03beac1140dfbfd630e1802bfd
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 85%

---


# 可选 - 通过 FTP 上传数据文件

如果您不使用拖放操作上传，则可以通过 FTP 将客户属性数据上传到 Experience Cloud。

在 Experience Cloud 中创建客户属性来源和 FTP 帐户后，您可以上传数据。为每个属性来源创建一个 FTP 帐户。上传的文件存储在该帐户的根文件夹中。该数据必须为 `.csv` 格式，并通过另一个 `.fin` 文件指示上传已完成。

>[!IMPORTANT]
>
>Review [Data file requirements for uploading Customer Attributes](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) before uploading the file.

可以通过FTP或SFTP将文件上传到客户属性FTP站点。

* 您需要支持 SFTP 连接的客户端。
* 您可以使用用户名/密码连接到 SFTP，也可以不使用密码连接到 SFTP，如[此处](https://docs.adobe.com/help/zh-Hans/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/ftp-sftp-cert-auth.html)所示。

**通过 FTP 上传数据文件的方法**

1. [创建客户属性来源并上传数据文件...](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78).

   确保您已登录到位于 [!DNL ftp.adobe.com/<sftpname>] 的 FTP 站点。

1. 单击&#x200B;**[!UICONTROL 操作]** > **[!UICONTROL 文件上传]**。

1. 上传 `.fin` 文件，以便您的文件可被检索到。

   文件类型 `.fin` 是由用户创建的，表示上传已完成。它可以是一个空白的记事本文件。例如，如果您上传 [!DNL crs123.csv]，同时也会上传 [!DNL crs123.fin]。

   如果上传成功，则两个文件都会移到名为&#x200B;**已处理**&#x200B;的文件夹。

   See [Data file requirements for uploading Customer Attributes](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) for important information about file names and structure.
