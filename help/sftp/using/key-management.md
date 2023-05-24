---
product: campaign
solution: Campaign
title: 密钥管理
description: 了解如何管理密钥以连接到 SFTP 服务器
feature: Control Panel
role: Architect
level: Experienced
exl-id: 03815e01-6371-4e1c-b4b8-7abe25957cee
source-git-commit: c1c80c03a351613ec0c6870a11ab39a634e8eab7
workflow-type: tm+mt
source-wordcount: '1054'
ht-degree: 41%

---

# 密钥管理 {#key-management}

>[!CONTEXTUALHELP]
>id="cp_key_management"
>title="关于公钥管理"
>abstract="在此选项卡中，创建、管理和编辑您的公钥。"
>additional-url="https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4#t=166" text="观看演示视频"

Adobe 建议所有客户使用&#x200B;**公钥和私钥对**&#x200B;建立其与 SFTP 服务器的连接。

下面介绍了生成公共 SSH 密钥并添加此密钥以访问 SFTP 服务器的步骤，以及有关身份验证的建议。

服务器的访问权限设置完毕后，请记得&#x200B;**添加 IP 地址，您需要这些地址才能访问允许列表**&#x200B;的服务器，以便连接到该服务器。如需详细信息，请参阅[此部分](../../instances-settings/using/ip-allow-listing-instance-access.md)。

![](assets/do-not-localize/how-to-video.png)在使用 [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/sftp-management/generate-ssh-key.html#sftp-management) 或 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/sftp-management/generate-ssh-key.html#sftp-management) 的视频中了解这一功能

## 最佳实践 {#best-practices}

**关于公共 SSH 密钥**

确保始终使用相同的身份验证连接到服务器，并且您正在使用受支持的密钥格式。

**API 与用户名和密码集成**

在極少數的情況下，某些SFTP伺服器會啟用密碼式驗證。 Adobe建議您使用金鑰式驗證，因為此方法更有效且更安全。 您可以聯絡客戶服務，要求切換至金鑰式驗證。

>[!IMPORTANT]
>
>如果您的密码过期，即使系统中已安装密钥，您也将无法登录 SFTP 帐户。

## 安装 SSH 密钥 {#installing-ssh-key}

>[!CONTEXTUALHELP]
>id="cp_sftp_publickey_add"
>title="公钥添加"
>abstract="为实例生成 SSH 公钥并将它添加到控制面板以访问 SFTP 服务器。"

>[!IMPORTANT]
>
>關於SSH金鑰，您必須一律遵循組織方針。 以下步驟只是如何建立SSH金鑰的範例，可做為向團隊或內部網路群組溝通需求的有用參考點。

1. 导览至 **[!UICONTROL Key Management]**&#x200B;选项卡，然后单击 **[!UICONTROL Add new public key]** 按钮。

   ![](assets/key0.png)

1. 在打开的对话框中，选择要为其创建公钥的用户名以及要为其激活密钥的服务器。

   ![](assets/key1.png)

   >[!NOTE]
   >
   >「控制面板」會檢查指定執行個體上的指定使用者名稱是否作用中，並讓您在一或多個執行個體上啟用金鑰。
   >
   >可以为每个用户添加一个或多个公共 SSH 密钥。

1. 為了更好地管理您的公開金鑰，您可以設定每個金鑰的可用期間。 若要這麼做，請選取 **[!UICONTROL Type]** 下拉式清單，並在對應欄位中定義持續時間。 如需公開金鑰到期的詳細資訊，請參閱 [本節](#expiry).

   ![](assets/key_expiry.png)

   >[!NOTE]
   >
   >根據預設， **[!UICONTROL Type]** 欄位已設為 **[!UICONTROL Unlimited]**，這表示公開金鑰永不過期。

1. 在 **[!UICONTROL Comment]** 欄位中，您可以指出新增此公開金鑰的原因（原因、對象等）。

1. 若要能夠填寫 **[!UICONTROL Public Key]** 欄位中，您必須產生公開SSH金鑰。 根據您的作業系統，請遵循下列步驟。

   **Linux 和 Mac：**

   使用终端生成公钥和私钥对：
   1. 输入以下命令：`ssh-keygen -m pem -t rsa -b 2048 -C "your_email@example.com"`。
   1. 在出现提示时，为您的密钥提供名称。如果 .ssh 目录不存在，系统将为您创建一个目录。
   1. 在出现提示时输入密码，然后重新输入一次。也可保留为空。
   1. 密钥对“name”和“name.pub”由系统创建。搜索“name.pub”文件，然后将其打开。该文件应具有以您指定的电子邮件地址结尾的字母数字字符串。

   **Windows：**

   您可能需要安裝協力廠商工具，協助您以相同格式「name.pub」產生私人/公開金鑰組。

1. 打开 .pub 文件，然后将以“ssh..”开头的整个字符串复制并粘贴到控制面板。

   ![](assets/publickey.png)

   >[!NOTE]
   >
   >此 **[!UICONTROL Public Key]** 欄位僅接受OpenSSH格式。 公共 SSH 密钥大小应为 **2048 位**。

1. 单击&#x200B;**[!UICONTROL Save]**&#x200B;按钮以创建密钥。「控制面板」會儲存公開金鑰及其相關聯的指紋，並使用SHA256格式加密。

>[!IMPORTANT]
>
>如果您建立的金鑰是用來與之前從未連線至所選SFTP伺服器的系統建立連線，您必須先將該系統的公用IP新增至允許清單，才能將此系統與SFTP伺服器搭配使用。 请参阅[此小节](ip-range-allow-listing.md)。

您可以使用指紋來比對儲存在電腦上的私密金鑰與儲存在「控制面板」中的對應公開金鑰。

![](assets/fingerprint_compare.png)

通过“**...**”按钮，您可以删除现有密钥，或将其关联的指纹复制到剪贴板。

![](assets/key_options.png)

## 管理公開金鑰 {#managing-public-keys}

您建立的公開金鑰會顯示在 **[!UICONTROL Key Management]** 標籤。

您可以根據建立日期或編輯日期、建立或編輯該日期的使用者以及IP範圍到期日來排序專案。

您也可以開始輸入名稱或註解，以搜尋公開金鑰。

![](assets/control_panel_key_management_sort.png)

若要編輯一或多個IP範圍，請參閱 [本節](#editing-public-keys).

若要從清單中刪除一個或多個公開金鑰，請選取它們，然後按一下 **[!UICONTROL Delete public key]** 按鈕。

![](assets/control_panel_delete_key.png)

### 到期日 {#expiry}

此 **[!UICONTROL Expires]** 欄會顯示公開金鑰到期前的剩餘天數。

如果您訂閱 [電子郵件警示](../../performance-monitoring/using/email-alerting.md)，您會在公開金鑰到期的10天及5天前，以及到期當日，收到電子郵件通知。 收到警報後，您可以 [編輯公開金鑰](#editing-public-keys) 以視需要延長有效期。

過期的公開金鑰將在7天後自動刪除。 它顯示為 **[!UICONTROL Expired]** 在 **[!UICONTROL Expires]** 欄。 在此7天期間內：

* 過期的公開金鑰無法再用來連線至SFTP伺服器。

* 您可以 [編輯](#editing-public-keys) 過期的公開金鑰並更新其持續時間，以使其再次可用。

* 您可以從清單中刪除它。

## 編輯公開金鑰 {#editing-public-keys}

>[!CONTEXTUALHELP]
>id="cp_sftp_publickey_update"
>title="编辑公钥"
>abstract="更新选定的公钥以访问您的 SFTP 服务器。"

若要編輯公開金鑰，請遵循下列步驟。

>[!NOTE]
>
>您只能編輯自2021年10月版控制面板發行以來建立的公開金鑰。

1. 從中選擇一或多個專案 **[!UICONTROL Key Management]** 清單。
1. 单击 **[!UICONTROL Update public key]** 按钮。

   ![](assets/control_panel_edit_key.png)

1. 您只能編輯公開金鑰到期和/或新增註解。

   >[!NOTE]
   >
   >若要修改OpenSSH格式的使用者名稱、執行個體和公開金鑰，請刪除公開金鑰，並根據您的需求建立新的公開金鑰。

1. 保存您的更改。
