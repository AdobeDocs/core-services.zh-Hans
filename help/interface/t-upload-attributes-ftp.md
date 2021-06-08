---
description: 了解如何通过 FTP 将客户属性数据上传到 Experience Cloud。
keywords: 客户属性;核心服务
solution: Experience Cloud
title: '通过 FTP 上传客户属性数据文件 '
uuid: 5df565dd-b6f8-420e-981f-4b6fc6f7d0e4
feature: 客户属性
topic: 管理
role: Administrator
level: Experienced
exl-id: ed9e4a8f-493a-4a0f-a87e-674c7da95b99
source-git-commit: ebefd433e96da422674e7ee71c8988d4011fed11
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 90%

---

# 可选 - 通过 FTP 上传数据文件

如果您不使用拖放操作上传，则可以通过 FTP 将客户属性数据上传到 Experience Cloud。

在 Experience Cloud 中创建客户属性来源和 FTP 帐户后，您可以上传数据。为每个属性来源创建一个 FTP 帐户。上传的文件存储在该帐户的根文件夹中。数据必须为`.csv`格式，并通过另一个`.fin`文件指示上传已完成。

>[!IMPORTANT]
>
>在上传文件之前，先查看[上传客户属性的数据文件要求](crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19)。

可通过 FTP 或 SFTP，将文件上传到客户属性 FTP 站点。

* 您需要支持 SFTP 连接的客户端。
* 您可以使用用户名/密码连接到 SFTP，也可以不使用密码连接到 SFTP，如[此处](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/ftp-sftp-cert-auth.html?lang=en)所示。

**通过 FTP 上传数据文件的方法**

1. [创建客户属性来源并上传数据文件...](t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78).

   确保您已登录位于 `ftp.adobe.com/<sftpname>` 的 FTP 站点。

1. 单击&#x200B;**[!UICONTROL 操作]** > **[!UICONTROL 文件上传]**。

1. 上传 `.fin` 文件，以便您的文件可被检索到。

   文件类型 `.fin` 是由用户创建的，表示上传已完成。它可以是一个空白的记事本文件。例如，如果您上传 [!DNL crs123.csv]，同时也会上传 [!DNL crs123.fin]。

   如果上传成功，则两个文件都会移到名为&#x200B;**已处理**&#x200B;的文件夹。

   请参阅[上传客户属性的数据文件要求](crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19)，以了解有关文件名和结构的重要信息。
