---
title: 登录SFTP服务器
description: 了解如何登录SFTP服务器
translation-type: tm+mt
source-git-commit: 8ee999b89af88a1a59956838d5722ce8fc6b3955

---


# 登录SFTP服务器 {#logging-into-sft-server}

以下步骤详细说明了如何通过SFTP客户端应用程序连接SFTP服务器。

在登录到服务器之前，请确保：

* 您的SFTP服务器 **由Adobe托管**。
* 您的&#x200B;**用户名**&#x200B;已为服务器设置。You can check this information directly in the Control Panel, in the **Key management** tab from the SFTP Card.
* 您有一个 **私钥对和公钥对** ，用于登录SFTP服务器。 有关如 [何添加SSH密钥](../../sftp/using/key-management.md) ，请参阅本节。
* 您的 **公共IP地址已在SFTP服务器上列入白名单** 。 否则，请参阅本 [节](../../sftp/using/ip-range-whitelisting.md) ，了解有关如何将您的IP范围列入白名单的更多信息。
* 您可以访问 **SFTP客户端软件**。 您可以咨询IT部门，了解他们建议使用的SFTP客户端应用程序，或在公司策略允许的情况下在Internet上搜索。

要连接到SFTP服务器，请执行以下步骤：

1. Launch the Control Panel, then select the **[!UICONTROL Key Management]** tab from the **[!UICONTROL SFTP]** card.

   ![](assets/fingerprintNEW2.png)

1. 启动您的SFTP客户端应用程序，然后从控制面板复制并粘贴服务器地址，后跟“campaign.adobe.com”，然后填写您的用户名。

   ![](assets/connect1.png)

1. 在字段 **[!UICONTROL SSH Private Key]** 中，选择存储在计算机中的私钥文件。 它对应于一个与公钥同名的文本文件，不带“.pub”扩展名（例如“enable”）。

   ![](assets/connect2.png)

   字 **[!UICONTROL Password]** 段会自动填充文件中的私钥。

   ![](assets/connect3.png)

   您可以通过将私钥或公钥的指纹与SFTP卡的“密钥管理”选项卡中显示的密钥的指纹进行比较，检查是否在控制面板中保存了您尝试使用的密钥。

   ![](assets/fingerprint3.png)

   >[!NOTE]
   >
   >如果您使用的是Mac计算机，则可以通过运行以下命令查看存储在计算机中的私钥的指纹：
   >
   >`ssh-keygen -lf <path of the privatekey>`

1. 所有信息填写完毕后，单 **[!UICONTROL Connect]** 击以登录SFTP服务器。

   ![](assets/sftpconnected.png)
