---
product: campaign
solution: Campaign
title: 登录 SFTP 服务器
description: 了解如何登录SFTP服务器
translation-type: tm+mt
source-git-commit: 317b4c1cee34667a36f5e1a1197649bfd69c151a
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 4%

---


# 登录 SFTP 服务器 {#logging-into-sft-server}

以下步骤详细说明了如何通过SFTP客户端应用程序连接SFTP服务器。

![](assets/do-not-localize/how-to-video.png) 使用Campaign Classic或Campaign Standard在视频中 [发现](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/sftp-management/connect-to-sftp-server.html?lang=en#sftp-management) 此功 [能](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/sftp-management/connect-to-sftp-server.html?lang=en#sftp-management)

登录到服务器之前，请确保：

* 您的SFTP服务器由 **Adobe托管**。
* 您的&#x200B;**用户名**&#x200B;已为服务器设置。You can check this information directly in the Control Panel, in the **Key management** tab from the SFTP Card.
* 您有一 **对私钥和公钥** ，用于登录SFTP服务器。 有关如 [何添加](../../sftp/using/key-management.md) SSH密钥的详细信息，请参阅本节。
* 您 **的公有IP地址已添加到SFTP服务器** 上的允许列表。 否则，请参 [阅本节](../../sftp/using/ip-range-allow-listing.md) ，了解如何将IP范围添加到允许列表。
* 您有权访问SFTP客 **户端软件**。 您可以咨询IT部门，了解他们推荐使用的SFTP客户端应用程序，或在Internet上搜索(如果公司策略允许)。

要连接到SFTP服务器，请执行以下步骤：

1. 启动控制面板，然后从卡 **[!UICONTROL Key Management]** 中选择选 **[!UICONTROL SFTP]** 项卡。

   ![](assets/sftp_card.png)

1. 启动SFTP客户端应用程序，从控制面板复制粘贴服务器地址，然后添加“活动.adobe.com”，然后填写用户名。

   ![](assets/do-not-localize/connect1.png)

1. 在字段 **[!UICONTROL SSH Private Key]** 中，选择存储在计算机中的私钥文件。 它对应一个与公钥同名的文本文件，不带“.pub”扩展名（如“enable”）。

   ![](assets/do-not-localize/connect2.png)

   字 **[!UICONTROL Password]** 段会自动填写文件中的私钥。

   ![](assets/do-not-localize/connect3.png)

   您可以通过比较私钥或公钥的指纹与SFTP卡的“密钥管理”选项卡中显示的密钥的指纹，检查您尝试使用的密钥是否已保存在控制面板中。

   ![](assets/fingerprint_compare.png)

   >[!NOTE]
   >
   >如果您使用的是Mac计算机，则可以通过运行以下命令来视图存储在计算机中的私钥的指纹：
   >
   >`ssh-keygen -lf <path of the privatekey>`

1. 所有信息填写完毕后，单 **[!UICONTROL Connect]** 击以登录到SFTP服务器。

   ![](assets/do-not-localize/sftpconnected.png)
