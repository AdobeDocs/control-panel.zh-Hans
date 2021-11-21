---
product: campaign
solution: Campaign
title: 登录 SFTP 服务器
description: 了解如何登录SFTP服务器
feature: Control Panel
role: Architect
level: Experienced
exl-id: 713f23bf-fa95-4b8a-b3ec-ca06a4592aa3
source-git-commit: 4fc34b07b497c743e2ca6c182e68d6ea5c180ac9
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 6%

---

# 登录 SFTP 服务器 {#logging-into-sft-server}

以下步骤详细介绍如何通过SFTP客户端应用程序连接SFTP服务器。

![](assets/do-not-localize/how-to-video.png)[ 在视频中发现此功能](https://video.tv.adobe.com/v/27263?quality=12)

登录到服务器之前，请确保：

* 您的SFTP服务器为 **由Adobe托管**.
* 您的&#x200B;**用户名**&#x200B;已为服务器设置。您可以直接在控制面板的 **密钥管理** 选项卡。
* 您拥有 **私钥和公钥对** 登录到SFTP服务器。 请参阅 [此部分](../../sftp/using/key-management.md) 以了解有关如何添加SSH密钥的更多信息。
* 您的 **公共IP地址已添加到允许列表** 在SFTP服务器上。 如果没有，请参阅 [此部分](../../sftp/using/ip-range-allow-listing.md) 以了解有关如何将IP范围添加到允许列表的更多信息。
* 您有权访问 **SFTP客户端软件**. 您可以咨询您的IT部门（其建议使用的SFTP客户端应用程序），或者在Internet上搜索（如果公司策略允许）。

要连接到SFTP服务器，请执行以下步骤：

1. 启动控制面板，然后选择 **[!UICONTROL Key Management]** 选项卡 **[!UICONTROL SFTP]** 卡。

   ![](assets/sftp_card.png)

1. 启动SFTP客户端应用程序，从控制面板复制并粘贴服务器地址，接着复制“campaign.adobe.com”，然后填写您的用户名。

   ![](assets/do-not-localize/connect1.png)

1. 在 **[!UICONTROL SSH Private Key]** 字段中，选择存储在计算机中的私钥文件。 它对应于与公钥同名，但没有“.pub”扩展名（例如，“enable”）的文本文件。

   ![](assets/do-not-localize/connect2.png)

   的 **[!UICONTROL Password]** 字段中，将自动使用文件中的私钥进行填充。

   ![](assets/do-not-localize/connect3.png)

   您可以通过将私钥或公钥的指纹与SFTP卡的“密钥管理”选项卡中显示的密钥的指纹进行比较，来检查您尝试使用的密钥是否保存在控制面板中。

   ![](assets/fingerprint_compare.png)

   >[!NOTE]
   >
   >如果您使用的是Mac计算机，则可以通过运行以下命令查看存储在计算机中的私钥的指纹：
   >
   >`ssh-keygen -lf <path of the privatekey>`

1. 填写完所有信息后，单击 **[!UICONTROL Connect]** 登录到SFTP服务器。

   ![](assets/do-not-localize/sftpconnected.png)
