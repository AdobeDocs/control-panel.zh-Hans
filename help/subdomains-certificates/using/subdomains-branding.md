---
product: campaign
solution: Campaign
title: 子域品牌化
description: 详细了解子域品牌化
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Intermediate
exl-id: a489d051-fb95-45cf-bb6d-33aef10b7795
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '703'
ht-degree: 100%

---

# 子域品牌化 {#subdomains-branding}

>[!CONTEXTUALHELP]
>id="cp_certificate_management"
>title="关于子域和 SSL 证书"
>abstract="监控子域和关联的 SSL 证书。"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html?lang=zh-Hans" text="监控 SSL 证书"

## 为什么要设置子域？ {#why-setting-up-subdomains}

子域是域的一个分支，可用于隔离您的品牌或各种类型的流量（交易消息、营销信息等）。

让我们以“mybrand.com”域为例，该域用于发送交易和营销通信。在这种情况下，您可以决定设置两个子域：

* “info.mybrand.com”子域，用于交易通信（购买确认、密码重置等），
* “marketing.mybrand.com”子域，用于您的潜在电子邮件。

这样，您将能够维护您的域和其他子域的声誉。例如，如果“marketing.mybrand.com”子域由于交付能力不佳而最终被互联网服务提供商加入阻止列表，这将阻止整个“mybrand.com”域和“info.mybrand.com”子域被加入阻止列表。

## 子域配置方法 {#subdomain-delegation-methods}

子域委派允许您委派域的子部分（技术上称为“DNS 区域”）以与 Adobe Campaign 配合使用。可用的设置方法包括：

* **将子域完全委派给 Adobe Campaign**（推荐）：将子域完全委派给 Adobe。Adobe 能够控制和维护发送、渲染和跟踪电子邮件活动所需的 DNS 的所有方面，从而将 Campaign 作为托管服务提供。

* **CNAME 的使用**：创建子域并使用 CNAME 指向 Adobe 特定的记录。使用此设置，Adobe 和客户共同负责维护 DNS。

下表概述了这些方法的工作原理以及隐含的工作量：

| 配置方法 | 工作原理 | 工作量 |
|---|---|---|
| **完全委派** | 创建子域和命名空间记录。然后，Adobe 将配置 Adobe Campaign 所需的所有 DNS 记录。<br/><br/>在此设置中，Adobe 完全负责管理子域和所有 DNS 记录。 | 低 |
| **CNAME，自定义方法** | 创建子域和命名空间记录。然后，Adobe 将提供要放入 DNS 服务器的记录，并在 Adobe Campaign DNS 服务器中配置相应值。<br/><br/>在此设置中，您和 Adobe 共同负责维护 DNS。 | 高 |

有关域委派的其他信息，请参阅[本文档](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html?lang=zh-Hans)。

如果您对子域委派方法有任何疑问，请联系 Adobe 交付团队，或最终联系客户关怀团队以请求提供可投放性方面的建议。

## 子域的用例 (Campaign v7/v8){#subdomains-use-cases}

>[!CONTEXTUALHELP]
>id="cp_add_subdomain_usecase_selection"
>title="选择子域的用例"
>abstract="按用例划分子域是实现交付性的最佳实践。这样，每个子域的信誉将被隔离和受保护。"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/setting-up-new-subdomain.html?lang=zh-Hans" text="设置新子域"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/subdomains-branding.html?lang=zh-Hans" text="子域品牌化"

为 Campaign v7/v8 实例设置子域时，需要选择使用该子域的用例（请参阅[设置新子域](../../subdomains-certificates/using/setting-up-new-subdomain.md)）。

可能的用例包括：

* **营销通信**：表示用于商业目的的通信。示例：销售电子邮件营销活动。

* **交易和运营通信**：表示交易通信包含旨在完成收件人已开始的流程的信息。示例：购买确认、密码重置电子邮件。组织通信涉及在组织内外交流信息、想法和观点，不带商业目的。

**根据用例划分子域是实现交付性的最佳实践**。这样，每个子域的信誉将被隔离和受保护。例如，如果营销通信的子域最终被互联网服务提供商添加到阻止列表，您的交易通信子域将不受影响，并且将能够继续发送通信。

**您可以为营销和事务性用例配置子域**：

* 对于营销用例，子域将配置在 **MID**（中间采购）实例上。
* 对于交易用例，子域将配置在所有 **RT**（消息中心/实时消息递送）实例上，以确保连接性。因此，子域将与您的所有 RT 实例一起运行。

>[!NOTE]
>
>如果您使用 Campaign v7/v8，控制面板将允许您查看哪些 RT/MID 实例已连接到您正在使用的营销实例。有关这方面的详细信息，请参阅[实例详细信息](../../instances-settings/using/instance-details.md)部分。

**相关主题：**

* [设置新子域](../../subdomains-certificates/using/setting-up-new-subdomain.md)
* [监控子域](../../subdomains-certificates/using/monitoring-subdomains.md)
