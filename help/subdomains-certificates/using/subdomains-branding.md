---
title: 子域品牌化
description: 详细了解子域品牌化
translation-type: ht
source-git-commit: f22e356b283ee2601c948d5c1d514a9a59c58451
workflow-type: ht
source-wordcount: '459'
ht-degree: 100%

---


# 子域品牌化 {#subdomains-branding}

>[!CONTEXTUALHELP]
>id="cp_certificate_management"
>title="关于子域和 SSL 证书"
>abstract="监控子域和关联的 SSL 证书。"
>additional-url="https://docs.adobe.com/content/help/zh-Hans/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html" text="如何监控子域的 SSL 证书"

>[!IMPORTANT]
>
>测试版中提供控制面板的子域委派，如有频繁更新和修改，恕不另行通知。

## 为什么要设置子域？{#why-setting-up-subdomains}

子域是域的一个分支，可用于隔离您的品牌或各种类型的流量（交易消息、营销信息等）。

让我们以“mybrand.com”域为例，该域用于发送交易和营销通信。在这种情况下，您可以决定设置两个子域：

* “info.mybrand.com”子域，用于交易通信（购买确认、密码重置等），
* “marketing.mybrand.com”子域，用于您的潜在电子邮件。

这样，您将能够维护您的域和其他子域的声誉。例如，如果“marketing.mybrand.com”子域由于交付能力不佳而最终被互联网服务提供商列入黑名单，这将阻止整个“mybrand.com”域和“info.mybrand.com”子域被列入黑名单。

## 子域委派方法 {#subdomain-delegation-methods}

子域委派允许您委派域的子部分（技术上称为“DNS 区域”）以与 Adobe Campaign 配合使用。可用的设置方法包括：

* **将子域完全委派给 Adobe Campaign**（推荐）：将子域完全委派给 Adobe。Adobe 能够控制和维护发送、渲染和跟踪电子邮件活动所需的 DNS 的所有方面，从而将 Campaign 作为托管服务提供。

* **使用 CNAME**（不建议也不支持通过控制面板）：创建子域，并使用 CNAME 指向 Adobe 特定的记录。使用此设置，Adobe 和客户共同负责维护 DNS。

下表概述了这些方法的工作原理以及隐含的工作量：

| 委派方法 | 工作原理 | 工作量 |
|---|---|---|
| **完全委派** | 创建子域和命名空间记录。然后，Adobe 将配置 Adobe Campaign 所需的所有 DNS 记录。<br/><br/>在此设置中，Adobe 完全负责管理子域和所有 DNS 记录。 | 低 |
| **CNAME，自定义方法** | 创建子域和命名空间记录。然后，Adobe 将提供要放入 DNS 服务器的记录，并在 Adobe Campaign DNS 服务器中配置相应值。<br/><br/>在此设置中，您和 Adobe 共同负责维护 DNS。 | 高 |

有关域委派的其他信息，请参阅[本文档](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html)。

如果您对子域委派方法有任何疑问，请联系 Adobe 可交付性团队，或最终联系客户关怀团队以请求可交付性咨询。

**相关主题：**

* [设置新子域](../../subdomains-certificates/using/setting-up-new-subdomain.md)
* [委派子域（教程视频）](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/subdomain-delegation.html)
* [监控子域](../../subdomains-certificates/using/monitoring-subdomains.md)
