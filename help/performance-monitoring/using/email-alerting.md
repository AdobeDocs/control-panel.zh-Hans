---
product: campaign
solution: Campaign
title: 电子邮件警报
description: 了解如何在活动实例出现问题时接收电子邮件通知
feature: Control Panel
role: Architect
level: Experienced
translation-type: tm+mt
source-git-commit: 4b8020dfd5d1f81a81d0e20025cfabe734744d34
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 3%

---


# 电子邮件警报 {#email-alerting}

为了为您的工作提供更大的灵活性，控制面板配备了实时电子邮件警报功能。

要订阅这些警报，请执行以下步骤：

1. 单击控制面板中任意位置提供的&#x200B;**[!UICONTROL Alerting notifications]**&#x200B;按钮，然后单击&#x200B;**[!UICONTROL Subscribe]**。

   ![](assets/subscribing.png)

1. 系统会发送一封电子邮件，确认您的订阅。

   ![](assets/email_subscription.png)

1. 订阅后，控制面板将通知系统问题并建议采取相应操作。 电子邮件警报将发送给已注册&#x200B;**所有实例**&#x200B;且它们是管理员的所有实例。

   ![](assets/alert_sample.png)


警报的列表如下：

* **SFTP存储使用**:您的SFTP服务器已达到其容量的80%或以上。请参阅[SFTP存储管理](../../sftp/using/sftp-storage-management.md)。

* **数据库使用**:您的实例的一个数据库已达到其容量的80%或以上。请参阅[数据库监视](../../performance-monitoring/using/database-monitoring.md)。

* **SSL证书过期**:您的子域之一的SSL证书已过期或将在60天或更短时间内过期。请参阅[监视子域的SSL证书](../../subdomains-certificates/using/monitoring-ssl-certificates.md)。

