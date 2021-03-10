---
product: campaign
solution: Campaign
title: 关于 SFTP 管理
description: 在控制面板中进一步了解SFTP管理
testing: SSECD-836 2
feature: 控制面板
role: 架构师
level: 中间
translation-type: tm+mt
source-git-commit: 4b8020dfd5d1f81a81d0e20025cfabe734744d34
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 4%

---


# 关于 SFTP 管理 {#about-sftp-management}

在控制面板中，您可以与连接到您有权访问的活动实例的所有SFTP服务器进行交互。 大多数实例已连接SFTP服务器（在某些情况下，开发和阶段实例可能未连接到任何SFTP服务器）。

访问SFTP服务器是使用SFTP客户端软件，您可以在线查找和下载该软件。 要连接到服务器，您必须通过此类客户端应用程序或API设置公共SSH密钥，并将连接到SFTP服务器的IP地址添加到允许列表。

通过“控制”面板，您可以执行以下操作来管理SFTP服务器：

* 监视他们的&#x200B;**存储容量**,
* 管理&#x200B;**IP地址允许列出**:添加或删除一个或多个服务器的IP地址范围，
* 管理&#x200B;**公共SSH密钥**&#x200B;以访问服务器。

以下各节提供了有关这些操作的详细信息。
