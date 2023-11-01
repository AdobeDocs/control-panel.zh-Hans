---
product: campaign
solution: Campaign
title: 登录 SFTP 服务器
description: 了解如何登录SFTP服务器
feature: Control Panel, SFTP Management
role: Admin
level: Experienced
exl-id: 713f23bf-fa95-4b8a-b3ec-ca06a4592aa3
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 6%

---

# 登录 SFTP 服务器 {#logging-into-sft-server}

以下步骤详细介绍了如何通过SFTP客户端应用程序连接SFTP服务器。

![](assets/do-not-localize/how-to-video.png)[ 在视频中发现此功能](https://video.tv.adobe.com/v/27263?quality=12)

在登录到服务器之前，请确保：

* 您的SFTP服务器是 **由Adobe托管**.
* 您的&#x200B;**用户名**&#x200B;已为服务器设置。您可以直接在控制面板中的以下位置检查此信息： **密钥管理** 选项卡。
* 您有一个 **私钥对和公共密钥对** 以登录SFTP服务器。 请参阅 [本节](../../sftp/using/key-management.md) 了解有关如何添加SSH密钥的更多信息。
* 您的 **公共IP地址已添加到允许列表** 在SFTP服务器上。 如果不能，请参见 [本节](../../sftp/using/ip-range-allow-listing.md) 有关如何将IP范围添加到允许列表的更多信息。
* 您有权访问 **SFTP客户端软件**. 您可以向您的IT部门咨询他们建议使用的SFTP客户端应用程序，或者在Internet上搜索一个应用程序（如果您的公司策略允许这样做）。

要连接到SFTP服务器，请执行以下步骤：

1. 启动控制面板，然后选择 **[!UICONTROL 密钥管理]** 选项卡 **[!UICONTROL SFTP]** 卡片。

   ![](assets/sftp_card.png)

1. 启动SFTP客户端应用程序，从控制面板中复制粘贴服务器地址，接着复制“campaign.adobe.com”，然后填写您的用户名。

   ![](assets/do-not-localize/connect1.png)

1. 在 **[!UICONTROL SSH私钥]** 字段中，选择存储在计算机上的私钥文件。 它对应于与您的公钥同名的文本文件，不带“.pub”扩展名（例如“enable”）。

   ![](assets/do-not-localize/connect2.png)

   此 **[!UICONTROL 密码]** 字段会自动填充为文件中的私钥。

   ![](assets/do-not-localize/connect3.png)

   您可以通过比较私钥或公钥的指纹与SFTP卡的“密钥管理”选项卡中显示的密钥的指纹来检查您尝试使用的密钥是否已保存在控制面板中。

   ![](assets/fingerprint_compare.png)

   >[!NOTE]
   >
   >如果您使用的是Mac计算机，则可以通过运行此命令查看存储在您计算机上的私钥的指纹：
   >
   >`ssh-keygen -lf <path of the privatekey>`

1. 填写完所有信息后，单击 **[!UICONTROL 连接]** 以登录到SFTP服务器。

   ![](assets/do-not-localize/sftpconnected.png)
