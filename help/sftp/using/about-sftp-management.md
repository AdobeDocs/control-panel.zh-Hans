---
product: campaign
solution: Campaign
title: 关于 SFTP 管理
description: 了解有关控制面板中的 SFTP 管理功能的更多信息
testing: SSECD-836 2
feature: Control Panel, SFTP Management
role: Admin
level: Intermediate
exl-id: b2c3be80-0d1b-4998-87ab-5280c6213f3d
TQID: https://experienceleague.adobe.com/UZHhTNCld6p1RFGh3DY-2r3VRiLNxCtP0anuPxPnWVE
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: 06babfad697fb874f2b77c5204e30580c55cd0d1
workflow-type: tm+mt
source-wordcount: 168
ht-degree: 100%

---

# 关于 SFTP 管理 {#about-sftp-management}

在控制面板中，您可以与连接到您有权访问的 Campaign 实例的所有 SFTP 服务器进行交互。 大多数实例已连接 SFTP 服务器（在某些情况下，开发和暂存实例可能不会连接到任何 SFTP 服务器）。

需要使用 SFTP 客户端软件（您可以在线查找和下载该软件）来访问 SFTP 服务器。 为了通过客户端应用程序或 API 等连接到服务器，您必须设置公共 SSH 密钥，并将连接到 SFTP 服务器的 IP 地址添加到允许列表。

控制面板允许您执行以下操作来管理 SFTP 服务器：

* 监控其&#x200B;**存储容量**。
* 管理 **IP 地址允许列表**：添加或删除一个或多个服务器的 IP 地址范围；
* 管理&#x200B;**公共 SSH 密钥**&#x200B;以用于访问服务器。

有关每个此类操作的详细信息，请参阅以下部分。
