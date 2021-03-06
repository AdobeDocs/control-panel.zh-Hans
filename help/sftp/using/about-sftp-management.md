---
product: campaign
solution: Campaign
title: 关于 SFTP 管理
description: 在控制面板中了解有关SFTP管理的更多信息
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

在控制面板中，您可以与连接到您有权访问的 Campaign 实例的所有 SFTP 服务器进行交互。大多数实例已连接SFTP服务器（在某些情况下，开发和暂存实例可能未连接到任何SFTP服务器）。

对SFTP服务器的访问是使用SFTP客户端软件进行的，您可以在线查找和下载该软件。 要通过此类客户端应用程序或API连接到服务器，您必须设置公共SSH密钥，并将连接到SFTP服务器的IP地址添加到允许列表。

通过控制面板，您可以执行以下操作来管理SFTP服务器：

* 监控 **存储容量**,
* 管理 **将IP地址添加到允许列表**:添加或删除一个或多个服务器的IP地址范围，
* 管理 **公共SSH密钥** 访问服务器。

以下各节提供了有关这些操作的详细信息。
