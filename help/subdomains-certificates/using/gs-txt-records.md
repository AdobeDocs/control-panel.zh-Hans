---
product: campaign
solution: Campaign
title: 管理 TXT 记录
description: 了解如何管理 TXT 记录以进行域所有权验证。
feature: Control Panel
role: Architect
level: Experienced
exl-id: 013d6674-0988-4553-a23e-b3ec23da5323
source-git-commit: 9548bef1500498c1778ce5854017388490320595
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 33%

---

# TXT记录入门 {#managing-txt-records}

>[!CONTEXTUALHELP]
>id="cp_siteverification_add"
>title="管理 TXT 记录"
>abstract="TXT 记录是一种 DNS 记录类型，用于提供有关域的文本信息，外部源可以读取该信息。通过控制面板，可将三种类型的记录添加到子域：Google Site Verification、DMARC 和 BIMI 记录。"

## 关于 TXT 记录 {#about}

TXT 记录是一种 DNS 记录类型，用于提供有关域的文本信息，外部源可以读取该信息。控制面板允许您向子域添加三种类型的记录：

* **Google TXT记录** 允许您证明自己拥有域，从而确保电子邮件的高收件箱率和低垃圾邮件率。 [了解如何添加Google TXT记录](managing-txt-records.md)
* **DMARC记录** 提供一种验证发件人域并防止将域用于恶意目的的方法。 [了解如何添加DMARC记录](dmarc.md)
* **BIMI记录** 允许您在邮箱提供商的收件箱中，在电子邮件旁边显示批准的徽标，以增强品牌认知度和信任度。 [了解如何添加BIMI记录](bimi.md)

## 监控子域的记录 {#monitor}

您可以通过访问子域的详细信息，监控已为每个子域添加的所有TXT记录。

在此屏幕中，将显示选定子域的所有TXT类型记录，并在其配置的“值”列中显示信息。 要删除Google TXT、DMARC或BIMI记录，请单击省略号按钮，然后选择删除。 您还可以根据需要编辑DMARC和BIMI记录。

![](assets/txt-records.png)
