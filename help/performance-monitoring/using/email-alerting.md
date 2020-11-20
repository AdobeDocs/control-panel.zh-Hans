---
product: campaign
solution: Campaign
title: 电子邮件警报
description: 了解如何在活动实例出现问题时接收电子邮件通知
translation-type: tm+mt
source-git-commit: 168ae32d7931497bb37d63f7dd1d14eadbb4b1bf
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# 电子邮件警报 {#email-alerting}

为了为您的工作提供更大的灵活性，控制面板配备了实时电子邮件警报功能。

要订阅这些警报，请按照以下步骤操作：

1. 单击控制面板 **[!UICONTROL Alerting notifications]** 中任意位置提供的按钮，然后单击 **[!UICONTROL Subscribe]**。

   ![](assets/subscribing.png)

1. 系统会发送一封电子邮件，确认您的订阅。

   ![](assets/email_subscription.png)

1. 订阅后，控制面板将通知系统问题并建议采取相应操作。 电子邮件警报将发送给已注册其管理员 **的所有实** 例的所有人。

   ![](assets/alert_sample.png)


警报的列表如下：

* **SFTP存储使用情况**:您的某个SFTP服务器已达到其容量的80%或以上。 See [SFTP storage management](../../sftp/using/sftp-storage-management.md).

* **数据库使用**:实例的一个数据库已达到其容量的80%或更多。 请参 [阅数据库监视](../../performance-monitoring/using/database-monitoring.md)。

* **SSL证书过期**:您的某个子域的SSL证书已过期或将在60天或更短时间内过期。 See [Monitoring subdomains&#39; SSL certificates](../../subdomains-certificates/using/monitoring-ssl-certificates.md).

