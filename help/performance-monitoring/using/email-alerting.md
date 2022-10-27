---
product: campaign
solution: Campaign
title: 电子邮件警报
description: 了解如何在Campaign实例出现问题时接收电子邮件通知
feature: Control Panel
role: Architect
level: Experienced
exl-id: 7942d2b1-d28f-4760-aa25-5ba94a627fd0
source-git-commit: 80a96152ffcfa184fbeb6fc5cddcb119655ffab1
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 2%

---

# 电子邮件警报 {#email-alerting}

为了为您的工作提供更大的灵活性，控制面板配备了实时电子邮件警报功能。

## 警报列表 {#list}

警报列表如下：

* **SFTP存储使用情况**:您的其中一台SFTP服务器已达到其容量的80%或更大。 请参阅 [SFTP存储管理](../../sftp/using/sftp-storage-management.md).

* **数据库使用情况**:实例的一个数据库已达到其容量的80%或更大。 请参阅 [数据库监控](../../performance-monitoring/using/database-monitoring.md).

* **SFTP IP允许列表过期**:您定义的其中一个IP范围已过期，或将在10天或更短时间内过期。 请参阅 [IP范围允许列表](../../sftp/using/ip-range-allow-listing.md).

* **SFTP公钥过期**:您定义的其中一个公钥已过期，或将在10天或更短时间内过期。 请参阅 [密钥管理](../../sftp/using/key-management.md).

* **SSL证书过期**:您的子域的其中一个SSL证书已过期或将在30天或更短时间内过期。 请参阅 [监控子域的SSL证书](../../subdomains-certificates/using/monitoring-ssl-certificates.md).

<!--* **Long running Queries**: A query has been running for more than 24 hours on one of your instances. See [Monitoring active queries](database-active-queries.md).-->

>[!NOTE]
>
>此外，控制面板允许您 **设置提醒** ，以便在实例中发生事件（版本和服务审查）之前，通过电子邮件接收通知。
>
>为此，您需要订阅了电子邮件警报，并为所需的即将发生的事件设置提醒。 [了解如何为即将发生的事件设置提醒](../../service-events/service-events.md#reminders)

## 订阅警报 {#subscribe}

要订阅这些警报，请执行以下步骤：

1. 单击 **[!UICONTROL Alerting notifications]** 按钮，然后单击 **[!UICONTROL Subscribe]**.

   ![](assets/subscribing.png)

1. 系统会发送电子邮件以确认您的订阅。

   ![](assets/email_subscription.png)

1. 订阅后，控制面板将通知系统问题并建议采取相应操作。 电子邮件警报会发送给已注册的每个人 **所有实例** 是的。

   ![](assets/alert_sample.png)
