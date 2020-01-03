---
title: 子域品牌
description: 进一步了解子域品牌
translation-type: tm+mt
source-git-commit: 85bef8fa652be883bc2afbc42a2d893ea75a4e77

---


# 子域品牌 {#subdomains-branding}

## 为什么要设置子域？ {#why-setting-up-subdomains}

子域是您的域的一个分区，可用于隔离您的品牌或各种类型的流量（交易消息、营销信息等）。

让我们以“mybrand.com”域为例，该域用于发送交易和营销通信。 在这种情况下，您可以决定设置两个子域：

* 交易通信的“info.mybrand.com”子域（购买确认、密码重置等）、
* “marketing.mybrand.com”子域，用于您的潜在电子邮件。

这样做有助于维护域和其他子域的声誉。 例如，如果“marketing.mybrand.com”子域由于交付能力不佳而最终被互联网服务提供商列入黑名单，这将阻止整个“mybrand.com”域和“info.mybrand.com”子域被列入黑名单。

## 子域委托方法 {#subdomain-delegation-methods}

子域委托允许您委派域的子区域（技术上称为“DNS区域”）以与Adobe Campaign一起使用。 可用的设置方法有：

* **向Adobe Campaign进行完全子域委托** （建议）:子域完全委托给Adobe。 Adobe能够控制和维护电子邮件营销活动的交付、呈现和跟踪所需的DNS的所有方面，从而将Campaign作为托管服务提供。

* **使用CNAME** （不建议，也不支持通过控制面板）:创建子域并使用CNAME指向特定于Adobe的记录。 使用此设置，Adobe和客户均有责任维护DNS。

下表概述了这些方法的工作方式以及隐含的工作量：

| 委托方法 | 工作原理 | 工作量 |
|---|---|---|
| **完全委托** | 创建子域和命名空间记录。 然后，Adobe将配置Adobe Campaign所需的所有DNS记录。<br/><br/>在此设置中，Adobe完全负责管理子域和所有DNS记录。 | 低 |
| **CNAME，自定义方法** | 创建子域和命名空间记录。 然后，Adobe将提供要放入DNS服务器中的记录，并将在Adobe Campaign DNS服务器中配置相应的值。<br/><br/>在此设置中，您和Adobe均负责维护DNS。 | 高 |

有关域委派的其他信息，请参[阅此文档](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html)。