---
product: campaign
solution: Campaign
title: 电子邮件警报
description: 瞭解在您的Campaign執行個體發生問題時如何接收電子郵件通知
feature: Control Panel
role: Architect
level: Experienced
exl-id: 7942d2b1-d28f-4760-aa25-5ba94a627fd0
source-git-commit: 80a96152ffcfa184fbeb6fc5cddcb119655ffab1
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 3%

---

# 电子邮件警报 {#email-alerting}

為了給您的工作提供更大的彈性，「控制面板」配備了即時電子郵件警報功能。

## 警示清單 {#list}

警示清單如下：

* **SFTP儲存空間使用量**：您的其中一個SFTP伺服器已達到其容量的80%或更多。 请参阅 [SFTP 存储管理](../../sftp/using/sftp-storage-management.md)。

* **資料庫使用狀況**：其中一個執行個體的資料庫已達到其容量的80%或更多。 另請參閱 [資料庫監視](../../performance-monitoring/using/database-monitoring.md).

* **SFTP IP允許清單到期**：您定義的其中一個IP範圍已過期，或將在10天或更短時間內過期。 另請參閱 [IP範圍允許清單](../../sftp/using/ip-range-allow-listing.md).

* **SFTP公開金鑰過期**：您定義的其中一個公開金鑰已過期，或即將在10天或更短時間內過期。 另請參閱 [金鑰管理](../../sftp/using/key-management.md).

* **SSL憑證到期**：您的其中一個子網域的SSL憑證已過期或將在30天或更短時間內過期。 另請參閱 [監視子網域的SSL憑證](../../subdomains-certificates/using/monitoring-ssl-certificates.md).

<!--* **Long running Queries**: A query has been running for more than 24 hours on one of your instances. See [Monitoring active queries](database-active-queries.md).-->

>[!NOTE]
>
>此外，「控制面板」可讓您 **設定提醒** 以便在執行個體上發生事件（發行和服務審查）之前透過電子郵件通知。
>
>若要這麼做，您必須訂閱電子郵件警示，並為想要的近期事件設定提醒。 [瞭解如何為即將到來的活動設定提醒](../../service-events/service-events.md#reminders)

## 订阅警报 {#subscribe}

若要訂閱這些警示，請遵循下列步驟：

1. 按一下 **[!UICONTROL Alerting notifications]** 按鈕可供使用，然後按一下 **[!UICONTROL Subscribe]**.

   ![](assets/subscribing.png)

1. 系統會傳送電子郵件以確認您的訂閱。

   ![](assets/email_subscription.png)

1. 訂閱後，「控制面板」會通知系統問題並建議要採取的動作。 電子郵件警示會傳送給已註冊的人 **所有執行個體** 他們的管理員。

   ![](assets/alert_sample.png)
