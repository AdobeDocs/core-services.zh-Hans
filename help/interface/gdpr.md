---
title: “对通用数据保护条例的 [!DNL Customer Attributes] 支持”
description: 了解客户属性对《通用数据保护条例》的支持
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 02417c0c-6780-4699-9470-f1685c3cd25d
source-git-commit: f229ec33ff721527e6a4c920ea63eabb4102935a
workflow-type: ht
source-wordcount: '394'
ht-degree: 100%

---

# 对通用数据保护条例的 [!DNL Customer Attributes] 支持

本页面介绍了 [!DNL Customer Attributes] 如何支持通用数据保护条例 (GDPR)。

>[!IMPORTANT]
>
>本文档的内容不是法律建议，也不会代替法律建议。请咨询您的法律顾问，以获得有关 GDPR 的建议。

[《通用数据保护条例》](https://business.adobe.com/privacy/general-data-protection-regulation.html)法规于 2018 年 5 月 25 日生效，旨在赋予欧盟 (EU) 境内所有个人（数据主体）对其个人数据的控制权。该法规还简化了国际业务的监管环境。该法规适用于向欧盟境内的个人提供商品或服务、监控个人行为或从其收集个人数据的所有企业（数据控制者）对个人数据进行处理的情况，而不论数据控制者的经营场所位于何处。

Adobe Experience Cloud 充当数据处理者，可处理其代表客户接收并存储的任何个人数据。作为数据控制者，您可以决定 Adobe Experience Cloud 代表您处理和存储的个人数据。

本文档介绍了 [!DNL Customer Attributes] 如何使用 Adobe Experience Platform Privacy Service API 和 Privacy Service UI 支持数据主体的 GDPR 数据访问和删除权利。

有关 GDPR 对您业务的意义的更多信息，请参阅 [GDPR 与您的业务](https://business.adobe.com/privacy/general-data-protection-regulation.html)。

## 发送 [!DNL Customer Attributes] 请求所需的设置

要提出访问和删除 [!DNL Customer Attributes] 数据的请求，您必须：

1. 确认以下各项：

   * [组织 ID](#organizations.md)
   * 要执行操作的 CRS 数据源的别名 ID
   * 要执行操作的配置文件的 CRM ID

   您的[组织 ID](#organizations.md) 是一个 24 字符的数字字母字符串，在末尾附加了 @AdobeOrg。需要组织的 ID 才能将请求提交到隐私 API。如果找不到 ID，请通过 `gdprsupport@adobe.com` 联系 Adobe 客户关怀。

1. 在[!UICONTROL 隐私服务]中，您可以向 [!DNL Customer Attributes] 提交访问和删除请求，并检查现有请求的状态。

## [!DNL Customer Attributes] JSON 请求中的必填字段值

&quot;company context&quot;：

* &quot;namespace&quot;：**imsOrgID**
* &quot;value&quot;：&lt;*您的 IMS 组织 ID 值*>

&quot;users&quot;：

* &quot;key&quot;：&lt;*通常是客户的名称*>

* &quot;action&quot;：**access** 或 **delete**

* &quot;user IDs&quot;：

   * &quot;namespace&quot;：&lt;*CRS 数据源的别名 ID*>

   * &quot;type&quot;：**integrationCode**

   * &quot;value&quot;：&lt;*CRM ID*>

* &quot;include&quot;：**CRS**（即适用于该请求的 Adobe 产品）

* &quot;regulation&quot;：**gdpr**（即适用于该请求的隐私法规）

## JSON 请求的示例

```
{
  "companyContexts": [
    {
      "namespace": "imsOrgID",
      "value": "<IMS_ORG_ID>"
    }
  ],
  "users": [
    {
      "key": "<KEY>",
      "action": [
        "<access/delete>"
      ],
      "userIDs": [
        {
          "namespace": "<Alias ID of CRS Data Source>",
          "type": "integrationCode",
          "value": "<CRM ID>"
        }
      ]
    }
  ],
  "regulation": "<gdpr/ccpa/pdpa>",
  "include": [
    "CRS"
  ]
}
```

## 针对访问请求返回的数据字段

```
attributes:
{
"value":<*value*>,
"key":<*key*>,
"displayName":<*displayName*>
}
```
