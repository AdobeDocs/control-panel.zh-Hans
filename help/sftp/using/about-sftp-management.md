---
product: campaign
solution: Campaign
title: 关于 SFTP 管理
description: 進一步瞭解「控制面板」中的SFTP管理
testing: SSECD-836 2
feature: Control Panel
role: Architect
level: Intermediate
exl-id: b2c3be80-0d1b-4998-87ab-5280c6213f3d
source-git-commit: 4fc34b07b497c743e2ca6c182e68d6ea5c180ac9
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 16%

---

# 关于 SFTP 管理 {#about-sftp-management}

在控制面板中，您可以与连接到您有权访问的 Campaign 实例的所有 SFTP 服务器进行交互。大多數執行個體都已連線SFTP伺服器（在某些情況下，開發和中繼執行個體可能未連線到任何SFTP伺服器）。

使用SFTP使用者端軟體存取SFTP伺服器，您可線上上尋找和下載。 若要透過這類使用者端應用程式或API連線至伺服器，您必須設定公開SSH金鑰，並將連線至SFTP伺服器的IP位址新增至允許清單。

「控制面板」可讓您執行以下動作來管理SFTP伺服器：

* 監視其 **儲存容量**，
* 管理 **IP位址允許清單**：新增或刪除一或多部伺服器的IP位址範圍，
* 管理 **公開SSH金鑰** 以存取您的伺服器。

以下各節會提供這些動作的詳細資訊。
