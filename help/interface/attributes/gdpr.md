---
title: '客户属性对《通用数据保护条例》的支持 '
description: 了解客户属性对《通用数据保护条例》的支持
translation-type: tm+mt
source-git-commit: 3f26c1af19a0838913eec2b4135304f5f3fcf0b4
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 100%

---


# 客户属性对《通用数据保护条例》的支持

本页介绍客户属性如何支持《通用数据保护条例》(GDPR)。

>[!IMPORTANT]
>
>本文档的内容不是法律建议，也不会代替法律建议。请咨询您的法律顾问，以获得有关 GDPR 的建议。

[《通用数据保护条例》](https://www.adobe.com/cn/privacy/general-data-protection-regulation/what-is-gdpr.html)法规于 2018 年 5 月 25 日生效，旨在赋予欧盟 (EU) 境内所有个人（数据主体）对其个人数据的控制权。该法规还简化了国际业务的监管环境。该法规适用于向欧盟境内的个人提供商品或服务、监控个人行为或从其收集个人数据的所有企业（数据控制者）对个人数据进行处理的情况，而不论数据控制者的经营场所位于何处。

Adobe Experience Cloud 充当数据处理者，可处理其代表客户接收并存储的任何个人数据。作为数据控制者，您可以决定 Adobe Experience Cloud 代表您处理和存储的个人数据。

本文档介绍了[!UICONTROL 客户属性]如何使用 Adobe Experience Platform 隐私服务 API 和隐私服务 UI 支持数据主体的 GDPR 数据访问和删除权利。

有关 GDPR 对您业务的意义的更多信息，请参阅 [GDPR 与您的业务](https://www.adobe.com/cn/privacy/general-data-protection-regulation.html)。

## 发送[!UICONTROL 客户属性]请求所需的设置

要请求访问和删除[!UICONTROL 客户属性]的数据，您需要：

1. 识别以下内容：

   * IMS 组织 ID
   * 要执行操作的 CRS 数据源的别名 ID
   * 要执行操作的配置文件的 CRM ID

   IMS 组织 ID 是一个由 24 个字符组成的字母数字字符串，其后附加有 @AdobeOrg。如果您的营销团队或内部 Adobe 系统管理员不知道您组织的 IMS 组织 ID，请通过 gdprsupport@adobe.com 与 Adobe 客户关怀团队联系。您需要拥有 IMS 组织 ID 才能向隐私 API 提交请求。

1. 在“[!UICONTROL 隐私服务]”中，您可以向客户属性提交访问和删除请求，并检查现有请求的状态。

## [!UICONTROL 客户属性] JSON 请求中的必填字段值

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
"value”:<*value*>,
"key”:<*key*>,
"displayName”:<*displayName*>
}
```
