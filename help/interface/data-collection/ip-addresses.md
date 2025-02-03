---
title: Experience Cloud使用的IP地址
description: 如果贵组织的防火墙阻止源自Adobe的IP地址，请使用此列表更新防火墙设置。
exl-id: 1fca8d3b-ae8b-4095-96ef-d165f912b4c6
source-git-commit: faa9b8067a85f86cc0b559bdeeaed80df2339c7d
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 11%

---

# Experience Cloud使用的IP地址

某些防火墙配置会阻止源自Adobe的数据收集服务器或负责访问数据的服务器的IP地址。 您可以使用此范围列表来更改组织的防火墙设置，以允许从组织内部访问和发送数据。 此页面包括Adobe使用的入站系统（例如数据收集）和出站系统(例如Adobe Analytics中的数据馈送)。

>[!IMPORTANT]
>
>虽然Adobe会尽力保持此文档为最新状态，但它不能保证IP范围列表保持不变。 可能的更改包括：业务增长和扩展，Internet注册管理机构要求对Adobe的IP地址空间进行更改，或Internet服务提供商停止运营。

除了下面列出的IP地址块之外，各个Adobe Experience Cloud产品还会使用他们自己的IP地址：

* [Adobe Analytics](https://experienceleague.adobe.com/en/docs/analytics/technotes/ip-addresses)
* [Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/technotes/ip-addresses)
* [Marketo Engage](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/configure-protocols-for-marketo#step-allowlist-marketo-ips)

## 所有AdobeIP地址块

下表列出了所有Adobe拥有的IP地址。 此表包括全球Adobe运行的所有Adobe员工办公室和数据中心。 它不包括托管在公共云上的服务。

| IP块（CIDR表示法） |
| --- |
| `63.140.32.0/19` |
| `66.117.16.0/20` |
| `66.235.128.0/19` |
| `130.248.0.0/16` |
| `172.82.192.0/18` |
| `185.34.188.0/22` |
| `192.243.240.0/22` |

{style="table-layout:auto"}

## Adobe Experience Cloud数据收集和FTP IP地址块

如果您的组织希望允许特定IP地址范围，您可以参考下表。 其包括：

* 所有Experience Cloud产品的数据收集服务器
* 适用于所有Experience Cloud产品的FTP服务器

上表包含此部分中的所有IP范围。

| 位置 | IP范围（CIDR表示法） |
| --- | --- |
| 澳大利亚 | `63.140.55.0/24` |
| 澳大利亚 | `63.140.56.0/23` |
| 加利福尼亚 | `63.140.32.0/23` |
| 加利福尼亚 | `63.140.34.0/24` |
| 法国 | `63.140.62.0/23` |
| 印度 | `66.117.20.0/24` |
| 印度 | `66.117.22.0/23` |
| 日本 | `130.248.169.0/23` |
| 日本 | `63.140.50.0/23` |
| 日本 | `66.117.31.0/24` |
| 伦敦 | `66.235.156.0/24` |
| 伦敦 | `185.34.188.0/22` |
| 伦敦 | `130.248.152.0/22` |
| 伦敦 | `130.248.244.0/23` |
| 俄勒冈 | `66.235.132.0/22` |
| 俄勒冈 | `130.248.130.0/23` |
| 俄勒冈 | `130.248.150.0/24` |
| 俄勒冈 | `130.248.160.0/21` |
| 俄勒冈 | `192.243.242.0/24` |
| 新加坡 | `130.248.170.0/23` |
| 新加坡 | `130.248.240.0/24` |
| 新加坡 | `63.140.44.0/22` |
| 新加坡 | `63.140.48.0/23` |
| 新加坡 | `66.117.30.0/24` |
| 新加坡 | `172.82.240.8/29` |
| 新加坡 | `172.82.240.88/29` |
| 维吉尼亚 | `63.140.38.0/23` |
| 维吉尼亚 | `63.140.54.0/24` |
| 维吉尼亚 | `67.202.5.244` |

{style="table-layout:auto"}

Adobe Experience Cloud还支持有限容量的IPv6。 这些IP块与上面的IPv4对应块具有类似的数据收集目的，但不包括FTP。

| 位置 | Host |
| --- | --- |
| 澳大利亚 | `2406:da1c:406:1a00::/56` |
| 澳大利亚 | `2406:da1c:ce5:b400::/56` |
| 加利福尼亚 | `2600:1f1c:366:d900::/56` |
| 法国 | `2a05:d012:706:d000::/56` |
| 印度 | `2406:da1a:f34:6a00::/56` |
| 爱尔兰 | `2a05:d018:309:600::/56` |
| 日本 | `2406:da14:b07:ab00::/56` |
| 俄勒冈 | `2600:1f14:1eb:7d00::/56` |
| 俄勒冈 | `2600:1f14:9d3:2b00::/56` |
| 新加坡 | `2406:da18:6e8:1e00::/56` |
| 维吉尼亚 | `2600:1f18:1a20:e800::/56` |
| 维吉尼亚 | `2600:1f18:4fd:6000::/56` |
| 维吉尼亚 | `2600:1f18:b00:e100::/56` |
| 维吉尼亚 | `2600:1f18:d1f:bd00::/56` |

>[!TIP]
>
>Adobe Analytics导出功能(包括Data Warehouse和数据馈送)的FTP连接仅源自伦敦、俄勒冈和新加坡位置的IPv4地址。
