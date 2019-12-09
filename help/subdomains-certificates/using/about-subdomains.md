---
title: 关于子域
description: 进一步了解子域
translation-type: tm+mt
source-git-commit: c2ef995d49118943bdd77e6d3c14ef7ec643e672

---


# 关于子域 {#about-subdomains}

## 为什么要设置子域？ {#why-setting-up-subdomains}

子域是您的域的一个分区，可用于隔离各种类型的流量（公司、营销信息等）。

让我们举一个“mybrand.com”域的示例，它用于发送信息性和营销通信：

* info.mybrand.com，用于内部通信
* marketing.mybrand.com，以便您发送潜在电子邮件。

在这种情况下，您可以决定将“marketing.mybrand.com”子域委派到Adobe Campaign。 这样，您将有助于维护您的域和其他子域的声誉。 例如，如果“marketing.mybrand.com”子域由于交付能力不佳而最终被互联网服务提供商列入黑名单，这将阻止整个“mybrand.com”域和“info.mybrand.com”子域被阻止。

## 子域委托方法 {#subdomain-delegation-methods}

子域委托允许您委派域的子区域（技术上称为“DNS区域”）以与Adobe Campaign一起使用。 可用的设置方法有：

* **向Adobe Campaign进行完全子域委托** （建议）

   子域完全委托给Adobe。 Adobe能够控制和维护电子邮件营销活动的交付、呈现和跟踪所需的DNS的所有方面，从而将Campaign作为托管服务提供。

* **使用CNAME** （不建议，也不支持通过控制面板）:

   创建子域并使用CNAME指向特定于Adobe的记录。 使用此设置，Adobe和客户均有责任维护DNS。

有关这些方法（默示责任、要求等）的详细信息，请参阅 [本文档](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html)。
