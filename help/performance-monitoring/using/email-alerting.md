---
product: campaign
solution: Campaign
title: 电子邮件警报
description: 了解如何在 Campaign 实例出现问题时接收电子邮件通知
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: 7942d2b1-d28f-4760-aa25-5ba94a627fd0
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: ht
source-wordcount: '290'
ht-degree: 100%

---

# 电子邮件警报 {#email-alerting}

为使您的工作更加灵活，控制面板配备了实时电子邮件警报功能。

## 警报列表 {#list}

警报列表如下：

* **SFTP 存储使用情况**：其中一个 SFTP 服务器已达到其容量的 80% 或以上。请参阅 [SFTP 存储管理](../../sftp/using/sftp-storage-management.md)。

* **数据库使用情况**：其中一个实例的数据库已达到其容量的 80% 或以上。请参阅[数据库监控](../../performance-monitoring/using/database-monitoring.md)。

* **SFTP IP 允许列表过期**：您定义的某个 IP 范围已过期或将在 10 天或以内过期。请参阅 [IP 范围允许列表](../../sftp/using/ip-range-allow-listing.md)。

* **SFTP 公钥过期**：您定义的公钥之一已过期或将在 10 天或以内过期。请参阅[密钥管理](../../sftp/using/key-management.md)。

* **SSL 证书过期**：某个子域的 SSL 证书已过期或将在 30 天或以内过期。请参阅[监控子域的 SSL 证书](../../subdomains-certificates/using/monitoring-ssl-certificates.md)。

<!--* **Long running Queries**: A query has been running for more than 24 hours on one of your instances. See [Monitoring active queries](database-active-queries.md).-->

>[!NOTE]
>
>此外，控制面板还允许您&#x200B;**设置提醒**，以便在实例中发生事件（版本和服务评审）之前通过电子邮件接收通知。
>
>为此，您需要订阅电子邮件警报并为所需的即将发生的事件设置提醒。[了解如何为即将发生的事件设置提醒](../../service-events/service-events.md#reminders)

## 订阅警报 {#subscribe}

要订阅这些警报，请执行以下步骤：

1. 在控制面板中的任意位置单击&#x200B;**[!UICONTROL 警报通知]**&#x200B;按钮，然后单击&#x200B;**[!UICONTROL 订阅]**。

   ![](assets/subscribing.png)

1. 将发送一封电子邮件以确认您的订阅。

   ![](assets/email_subscription.png)

1. 订阅后，控制面板将会发送有关系统问题的通知并建议要采取的操作。电子邮件警报会被发送给注册为&#x200B;**所有实例**&#x200B;的管理员的用户。

   ![](assets/alert_sample.png)
