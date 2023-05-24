---
product: campaign
solution: Campaign
title: 登录 SFTP 服务器
description: 瞭解如何登入您的SFTP伺服器
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

以下步驟詳細說明如何透過SFTP使用者端應用程式連線您的SFTP伺服器。

![](assets/do-not-localize/how-to-video.png)[ 在视频中发现此功能](https://video.tv.adobe.com/v/27263?quality=12)

登入伺服器之前，請確定：

* 您的SFTP伺服器是 **由Adobe託管**.
* 您的&#x200B;**用户名**&#x200B;已为服务器设置。您可以直接在「控制面板」的 **金鑰管理** SFTP卡片中的Tab鍵。
* 您有 **私密金鑰和公開金鑰組** 以登入SFTP伺服器。 請參閱 [本節](../../sftp/using/key-management.md) 瞭解更多如何新增SSH金鑰。
* 您的 **公用IP位址已新增至允許清單** SFTP伺服器上執行。 如果沒有，請參閱 [本節](../../sftp/using/ip-range-allow-listing.md) 瞭解更多有關如何將IP範圍新增至允許清單的資訊。
* 您有權存取 **sftp使用者端軟體**. 您可以向您的IT部門洽詢他們建議使用的SFTP使用者端應用程式，或搜尋網際網路上的應用程式（如果您的公司原則允許的話）。

若要連線至您的SFTP伺服器，請遵循下列步驟：

1. 啟動「控制面板」，然後選取 **[!UICONTROL Key Management]** 標籤從 **[!UICONTROL SFTP]** 卡片。

   ![](assets/sftp_card.png)

1. 啟動SFTP使用者端應用程式，然後從「控制面板」複製並貼上伺服器位址，接著按一下「campaign.adobe.com」，然後填寫您的使用者名稱。

   ![](assets/do-not-localize/connect1.png)

1. 在 **[!UICONTROL SSH Private Key]** 欄位中，選取儲存在電腦中的私密金鑰檔案。 它對應於與您的公開金鑰同名的文字檔案，沒有「.pub」副檔名（例如「enable」）。

   ![](assets/do-not-localize/connect2.png)

   此 **[!UICONTROL Password]** 欄位會自動填入來自檔案的私密金鑰。

   ![](assets/do-not-localize/connect3.png)

   您可以檢查您嘗試使用的金鑰是否已儲存在「控制面板」中，方法是比較私密金鑰或公開金鑰的指紋與SFTP卡的「金鑰管理」標籤中顯示的金鑰指紋。

   ![](assets/fingerprint_compare.png)

   >[!NOTE]
   >
   >如果您使用Mac電腦，可以執行此命令來檢視儲存在電腦中的私密金鑰指紋：
   >
   >`ssh-keygen -lf <path of the privatekey>`

1. 填入所有資訊後，按一下 **[!UICONTROL Connect]** 以登入您的SFTP伺服器。

   ![](assets/do-not-localize/sftpconnected.png)
