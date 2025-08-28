---
title: 客户属性对《加州消费者隐私法案》的支持
description: 了解客户属性对《加州消费者隐私法案》的支持
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 320defc7-2cd5-4481-955d-77cf6fbfef6d
source-git-commit: 106ad989c5eef60dabbe4b82deaed9d87b09d795
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 63%

---

# 客户属性对《加州消费者隐私法案》的支持

本页介绍对《加州消费者隐私法案》(CCPA)的[!DNL Customer Attributes]支持。

>[!IMPORTANT]
>
>本文档的内容不是法律建议，也不会代替法律建议。请咨询您的法律顾问，以获得有关 (CCPA) 的建议。

CCPA是加利福尼亚州的新隐私法，于2020年1月1日生效。 CCPA 为加利福尼亚州居民提供了有关其个人信息的新权利，并对在加利福尼亚州开展业务的某些实体强加了数据保护责任。CCPA为消费者提供访问和删除其个人信息的权利，以及选择退出需向第三方“出售”个人信息的某些活动的权利。

作为企业，您自行决定 Adobe Experience Cloud 代表您处理和存储哪些个人数据。

作为您的服务提供商，Adobe Experience Cloud 会为您的企业提供支持，以履行因使用 Experience Cloud 产品和服务而需要向 CCPA 承担的责任。上述支持包括管理有关访问和删除个人信息的请求。

本文档介绍[!DNL Customer Attributes]如何使用Adobe Experience Platform Privacy Service API和Privacy Service UI支持数据主体的CCPA数据访问和删除权限。

有关涉及 CCPA 的 Adobe 隐私服务的更多信息，请参阅 [Adobe 隐私中心](https://www.adobe.com/privacy/ccpa.html)。

## 发送 [!DNL Customer Attributes] 请求所需的设置

要提出访问和删除 [!DNL Customer Attributes] 数据的请求，您必须：

1. 确认以下各项：

   * [组织 ID](../../administration/organizations.md)
   * 要执行操作的 CRS 数据源的别名 ID
   * 要执行操作的轮廓的 CRM ID

   您的组织ID是由24个字符组成的字母数字字符串，在末尾附加了@AdobeOrg。 需要组织的 ID 才能将请求提交到隐私 API。如果找不到 ID，请通过 `gdprsupport@adobe.com` 联系 Adobe 客户关怀。

1. 在[!UICONTROL Privacy Service]中，您可以向客户属性提交访问和删除请求，并检查现有请求的状态。

## [!DNL Customer Attributes] JSON请求中的必填字段值

&quot;company context&quot;：

* &quot;namespace&quot;：**imsOrgID**
* &quot;value&quot;： &lt;*您的组织ID值*>

&quot;users&quot;：

* &quot;key&quot;：&lt;*通常是客户的名称*>
* &quot;action&quot;：**access** 或 **delete**
* &quot;user IDs&quot;：
   * &quot;namespace&quot;：&lt;*CRS 数据源的别名 ID*>
   * &quot;type&quot;：**integrationCode**
   * &quot;value&quot;：&lt;*CRM ID*>
* &quot;include&quot;：**CRS**（即适用于该请求的 Adobe 产品）
* &quot;regulation&quot;：**ccpa**（即适用于该请求的隐私法规）

## JSON 请求的示例

```json
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

```json
attributes:
{
"value": "<*value*>",
"key": "<*key*>",
"displayName": "<*displayName*>"
}
```
