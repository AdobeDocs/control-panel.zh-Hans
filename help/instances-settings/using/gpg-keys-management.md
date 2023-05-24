---
product: campaign
solution: Campaign
title: GPG 密钥管理
description: 瞭解如何管理GPG金鑰，以在Adobe Campaign中加密和解密資料。
feature: Control Panel
role: Architect
level: Experienced
exl-id: 366dd2ea-c6be-41a2-a4d6-4ffecb5f3d39
source-git-commit: 5d2f0d08b7f9ae78fecfaa169190d6248ec4505b
workflow-type: tm+mt
source-wordcount: '1189'
ht-degree: 12%

---

# GPG 密钥管理 {#gpg-keys-management}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_gpg_management"
>title="关于 GPG 密钥"
>abstract="在此选项卡中，您可以在营销实例上安装和/或生成 GPG 密钥，以便加密从 Campaign 发送的数据和解密传入数据。"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/performance-monitoring/about-performance-monitoring.html?lang=zh-Hans" text="关于性能监控"

## 關於GPG加密 {#about-gpg-encryption}

GPG加密可讓您使用公開 — 私密金鑰組系統，保護您的資料，此系統需遵循 [OpenPGP](https://www.openpgp.org/about/standard/) 規格。

實作後，您就可以在傳輸前解密傳入資料，並加密傳出資料，以確保沒有有效相符金鑰組的任何人都不會存取這些資料。

要利用 Campaign 实现 GPG 加密，管理员用户必须直接从控制面板在营销实例上安装和/或生成 GPG 密钥。

然后，您将能够：

* **加密傳送的資料**：使用安裝的公開金鑰加密資料後，Adobe Campaign會將其傳送出去。

* **解密傳入的資料**：Adobe Campaign會使用從「控制面板」下載的公開金鑰，接收從外部系統加密的資料。 Adobe Campaign會使用從「控制面板」產生的私密金鑰解密資料。

## 加密資料 {#encrypting-data}

控制面板允许您加密从 Adobe Campaign 实例中传出的数据。

為此，您需要從PGP加密工具產生GPG金鑰組，然後將公開金鑰安裝到「控制面板」。 之後，您就可以在從執行個體傳送資料之前先加密資料。 为此，请执行以下步骤：

>[!NOTE]
>
>您最多可以在「控制面板」中安裝60個GPG金鑰。

![](assets/do-not-localize/how-to-video.png)[ 在视频中发现此功能](#video)

1. 按照下列步驟，使用PGP加密工具產生公開/私密金鑰組 [OpenPGP規格](https://www.openpgp.org/about/standard/). 要執行此操作，請安裝GPG公用程式或GNuGP軟體。

   >[!NOTE]
   >
   >可使用開放原始碼自由軟體來產生金鑰。 不過，請務必遵循組織的方針，並使用您的IT/安全性組織建議的GPG公用程式。

1. 安裝公用程式後，在Mac終端機或Windows命令中執行以下命令。

   `gpg --full-generate-key`

1. 出現提示時，請為您的金鑰指定所需的引數。 必要的引數包括：

   * **金鑰型別**： RSA
   * **金鑰長度**：3072 - 4096位元
   * **真實名稱** 和 **電子郵件地址**：允許追蹤金鑰組的建立者。 輸入連結至組織或部門的名稱和電子郵件地址。
   * **評論**：在評論欄位中新增標籤，可協助您輕鬆識別用來加密資料的金鑰。
   * **有效期**：日期或&quot;0&quot;，表示無到期日。
   * **複雜密碼**

   ![](assets/do-not-localize/gpg_command.png)

1. 確認後，指令碼將會產生一個金鑰及其相關聯的指紋，您可以將該金鑰匯出至檔案，或直接貼入「控制面板」。 若要匯出檔案，請執行此命令，後面接著您產生之金鑰的指紋。

   `gpg -a --export <fingerprint>`

1. 若要將公開金鑰安裝至「控制面板」，請開啟 **[!UICONTROL Instance settings]** 卡片，然後選取 **[!UICONTROL GPG keys]** 標籤和所需的執行個體。

1. 单击 **[!UICONTROL Install Key]** 按钮。

   ![](assets/gpg_install_button.png)

1. 貼上從PGP加密工具產生的公開金鑰。 您也可以直接拖放您匯出的公開金鑰檔案。

   >[!NOTE]
   >
   >公開金鑰應為OpenPGP格式。

   ![](assets/gpg_install_paste.png)

1. 单击 **[!UICONTROL Install Key]** 按钮。

安裝公開金鑰後，它就會顯示在清單中。 您可以使用 **...** 按鈕來下載或複製其指紋。

![](assets/gpg_install_download.png)

然後，您就可以在Adobe Campaign工作流程中使用金鑰。 使用資料擷取活動時，您可以使用它來加密資料。

![](assets/do-not-localize/how-to-video.png)[ 在视频中发现此功能](#video)

如需有關本主題的詳細資訊，請參閱Adobe Campaign檔案：

**Campaign v7/v8：**

* [壓縮或加密檔案](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/zip-encrypt.html)
* [使用案例：使用安裝於控制面板的金鑰加密及匯出資料](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html#use-case-gpg-encrypt)

**Campaign Standard:**

* [管理加密数据](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html)
* [使用案例：使用安裝於控制面板的金鑰加密及匯出資料](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/zip-encrypt.html#use-case-gpg-encrypt)

## 解密数据 {#decrypting-data}

「控制面板」可讓您解密傳入Adobe Campaign執行個體的外部資料。

為此，您需要直接從「控制面板」產生GPG金鑰組。

* 此 **公開金鑰** 將與外部系統共用，外部系統將使用它來加密要傳送至Campaign的資料。
* 此 **私密金鑰** 將由Campaign用來解密傳入的加密資料。

![](assets/do-not-localize/how-to-video.png)[ 在视频中发现此功能](#video)

若要在「控制面板」中產生金鑰組，請遵循下列步驟：

1. 開啟 **[!UICONTROL Instance settings]** 卡片，然後選取 **[!UICONTROL GPG keys]** 索引標籤和所需的Adobe Campaign執行個體。

1. 单击 **[!UICONTROL Generate Key]** 按钮。

   ![](assets/gpg_generate.png)

1. 指定金鑰的名稱，然後按一下 **[!UICONTROL Generate Key]**. 此名稱可協助您識別在Campaign工作流程中用於解密的金鑰

   ![](assets/gpg_generate_name.png)

產生金鑰組後，公開金鑰就會顯示在清單中。 請注意，產生解密金鑰組時沒有到期日。

您可以使用 **...** 按鈕以下載公開金鑰或複製其指紋。

![](assets/gpg_generate_list.png)

然後，公開金鑰便可與任何外部系統共用。 Adobe Campaign將能夠使用資料載入活動中的私密金鑰，將已使用公開金鑰加密的資料解密。

如需詳細資訊，請參閱Adobe Campaign檔案：

**Campaign v7和v8：**

* [在处理之前解压缩或解密文件](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/unzip-decrypt.html)
* [使用案例：匯入使用控制面板產生的金鑰加密的資料](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/unzip-decrypt.html#use-case-gpg-decrypt)

**Campaign Standard:**

* [管理加密数据](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html)
* [使用案例：匯入使用控制面板產生的金鑰加密的資料](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html#use-case-gpg-decrypt)

## 監控GPG金鑰

若要存取針對您的執行個體安裝和產生的GPG金鑰，請開啟 **[!UICONTROL Instance settings]** 卡片，然後選取 **[!UICONTROL GPG keys]** 標籤。

![](assets/gpg_list.png)

清單會顯示已安裝並為執行個體產生的所有加密和解密GPG金鑰，以及每個金鑰的詳細資訊：

* **[!UICONTROL Name]**：安裝或產生金鑰時定義的名稱。
* **[!UICONTROL Use case]**：此欄指定索引鍵的使用案例：

   ![](assets/gpg_icon_encrypt.png)：已安裝用於資料加密的金鑰。

   ![](assets/gpg_icon_decrypt.png)：金鑰已產生，以允許資料解密。

* **[!UICONTROL Fingerprint]**：金鑰的指紋。
* **[!UICONTROL Expires]**：金鑰的到期日。 請注意，「控制面板」會在主要專案接近到期日時提供視覺指示：

   * 緊急（紅色）會在30天前顯示。
   * 警告（黃色）會於60天前顯示。
   * 一旦鍵過期，就會顯示「過期」紅色橫幅。

   >[!NOTE]
   >
   >請注意，控制面板不會傳送任何電子郵件通知。

根據最佳實務，建議您移除任何不再需要的金鑰。 若要這麼做，請按一下 **...** 按鈕，然後選取 **[!UICONTROL Delete Key].**.

![](assets/gpg_delete.png)

>[!IMPORTANT]
>
>在移除金鑰之前，請確定它並未用於任何Adobe Campaign工作流程，以防止其失敗。

## 教學課程影片 {#video}

以下影片說明如何產生和安裝資料加密所需的GPG金鑰。

有關GPG金鑰管理的其他操作說明影片，請參閱  [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/instance-settings/gpg-key-management/gpg-key-management-overview.html#instance-settings) 和 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/instance-settings/gpg-key-management/gpg-key-management-overview.html#instance-settings) 教學課程頁面。

>[!VIDEO](https://video.tv.adobe.com/v/36386?quality=12)
