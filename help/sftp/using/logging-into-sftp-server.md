---
product: campaign
solution: Campaign
title: 登录 SFTP 服务器
description: 了解如何登录SFTP服务器
translation-type: tm+mt
source-git-commit: 54d3239a566491c854e5d46c297e72afeff83792
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# 登录 SFTP 服务器 {#logging-into-sft-server}

以下步骤详细说明了如何通过SFTP客户端应用程序连接SFTP服务器。

![](assets/do-not-localize/how-to-video.png)[ 在视频中发现此功能](https://video.tv.adobe.com/v/27263?quality=12&captions=chi_hans)

登录到服务器之前，请确保：

* 您的SFTP服务器由Adobe **托管。**
* 您的&#x200B;**用户名**&#x200B;已为服务器设置。您可以直接在控制面板中，在SFTP卡的&#x200B;**密钥管理**&#x200B;选项卡中检查此信息。
* 您有一个&#x200B;**私钥对和公钥对** ，用于登录SFTP服务器。 有关如何添加SSH密钥的详细信息，请参阅[本节](../../sftp/using/key-management.md)。
* 您的&#x200B;**公共IP地址已添加到SFTP服务器上的允许列表**。 否则，请参阅[本节](../../sftp/using/ip-range-allow-listing.md)以了解有关如何将IP范围添加到允许列表的详细信息。
* 您有权访问&#x200B;**SFTP客户端软件**。 您可以咨询IT部门，了解他们推荐使用的SFTP客户端应用程序，或在Internet上搜索(如果公司策略允许)。

要连接到SFTP服务器，请执行以下步骤：

1. 启动控制面板，然后从&#x200B;**[!UICONTROL SFTP]**&#x200B;卡中选择&#x200B;**[!UICONTROL Key Management]**&#x200B;选项卡。

   ![](assets/sftp_card.png)

1. 启动SFTP客户端应用程序，从控制面板复制粘贴服务器地址，然后添加“活动.adobe.com”，然后填写用户名。

   ![](assets/do-not-localize/connect1.png)

1. 在&#x200B;**[!UICONTROL SSH Private Key]**&#x200B;字段中，选择存储在计算机中的私钥文件。 它对应一个与公钥同名的文本文件，不带“.pub”扩展名（如“enable”）。

   ![](assets/do-not-localize/connect2.png)

   **[!UICONTROL Password]**&#x200B;字段会自动填写文件中的私钥。

   ![](assets/do-not-localize/connect3.png)

   您可以通过比较私钥或公钥的指纹与SFTP卡的“密钥管理”选项卡中显示的密钥的指纹，检查您尝试使用的密钥是否已保存在控制面板中。

   ![](assets/fingerprint_compare.png)

   >[!NOTE]
   >
   >如果您使用的是Mac计算机，则可以通过运行以下命令来视图存储在计算机中的私钥的指纹：
   >
   >`ssh-keygen -lf <path of the privatekey>`

1. 填写所有信息后，单击&#x200B;**[!UICONTROL Connect]**&#x200B;登录SFTP服务器。

   ![](assets/do-not-localize/sftpconnected.png)
