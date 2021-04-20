---
product: campaign
solution: Campaign
title: GPG 密钥管理
description: 了解如何管理GPG密钥以在Adobe Campaign内加密和解密数据。
feature: Control Panel
role: Architect
level: Experienced
translation-type: tm+mt
source-git-commit: 8fc348d0a4c858219fbead48e1d31f86c8576f72
workflow-type: tm+mt
source-wordcount: '1151'
ht-degree: 8%

---


# GPG 密钥管理 {#gpg-keys-management}

## 关于GPG加密{#about-gpg-encryption}

GPG加密允许您使用遵循[OpenPGP](https://www.openpgp.org/about/standard/)规范的公钥 — 私钥对系统保护数据。

实施后，您可以在传输发生之前对传入数据进行解密和加密，以确保没有有效匹配密钥对的任何人都无法访问这些数据。

要利用 Campaign 实现 GPG 加密，管理员用户必须直接从控制面板在营销实例上安装和/或生成 GPG 密钥。

然后，您将能够：

* **加密发送的数据**:Adobe Campaign在使用已安装的公钥对数据进行加密后发送数据。

* **解密传入数据**:Adobe Campaign使用从控制面板下载的公钥从外部系统接收已加密的数据。Adobe Campaign使用从控制面板生成的私钥解密数据。

## 正在加密数据{#encrypting-data}

控制面板允许您加密从 Adobe Campaign 实例中传出的数据。

为此，您需要从PGP加密工具生成GPG密钥对，然后将公钥安装到控制面板中。 然后，您将能够在从实例发送数据之前加密数据。 为此，请执行以下步骤：

![](assets/do-not-localize/how-to-video.png)[ 在视频中发现此功能](#video)

1. 使用遵循[OpenPGP规范](https://www.openpgp.org/about/standard/)的PGP加密工具生成公钥/私钥对。 为此，请安装GPG实用程序或GNuGP软件。

   >[!NOTE]
   >
   >提供了用于生成密钥的开放源代码免费软件。 但是，请确保您遵循组织的指导原则，并使用IT/安全组织建议的GPG实用程序。

1. 安装该实用程序后，在Mac Terminal或Windows命令中运行以下命令。

   `gpg --full-generate-key`

1. 出现提示时，为键指定所需的参数。 所需参数为：

   * **键类型**:RSA
   * **键长**:1024 - 4096比特
   * **实** 名和 **电子邮件地址**:允许跟踪创建密钥对的人。输入链接到您的组织或部门的名称和电子邮件地址。
   * **注释**:在注释字段中添加标签将帮助您轻松识别用于加密数据的密钥。
   * **过期**:日期或“0”表示无过期日期。
   * **密码**

   ![](assets/do-not-localize/gpg_command.png)

1. 确认后，脚本将生成一个具有其关联指纹的密钥，您可以将其导出到文件中，或直接粘贴到控制面板中。 要导出文件，请运行此命令，然后运行您生成的密钥的指纹。

   `gpg -a --export <fingerprint>`

1. 要将公钥安装到控制面板中，请打开&#x200B;**[!UICONTROL Instance settings]**&#x200B;卡，然后选择&#x200B;**[!UICONTROL GPG keys]**&#x200B;选项卡和所需的实例。

1. 单击 **[!UICONTROL Install Key]** 按钮。

   ![](assets/gpg_install_button.png)

1. 粘贴从PGP加密工具生成的公钥。 您还可以直接拖放导出的公钥文件。

   >[!NOTE]
   >
   >公钥应采用OpenPGP格式。

   ![](assets/gpg_install_paste.png)

1. 单击 **[!UICONTROL Install Key]** 按钮。

安装公钥后，该公钥将显示在列表中。 您可以使用&#x200B;**...**&#x200B;按钮下载或复制其指纹。

![](assets/gpg_install_download.png)

然后，该键可用于Adobe Campaign工作流。 使用数据提取活动时，您可以使用它加密数据。

![](assets/do-not-localize/how-to-video.png)[ 在视频中发现此功能](#video)

有关此主题的详细信息，请参阅Adobe Campaign文档：

**Campaign Classic:**

* [压缩或加密文件](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/zip-encrypt.html)
* [用例：使用安装在控制面板上的密钥加密和导出数据](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/how-to-use-workflow-data.html#use-case-gpg-encrypt)

**Campaign Standard:**

* [管理加密数据](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html)
* [用例：使用安装在控制面板上的密钥加密和导出数据](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/zip-encrypt.html#use-case-gpg-encrypt)

## 解密数据 {#decrypting-data}

控制面板允许您解密传入您的Adobe Campaign实例的外部数据。

为此，您需要直接从控制面板生成GPG密钥对。

* **公钥**&#x200B;将与外部系统共享，外部系统将使用公钥加密要发送到活动的数据。
* 活动将使用&#x200B;**私钥**&#x200B;解密传入的加密数据。

![](assets/do-not-localize/how-to-video.png)[ 在视频中发现此功能](#video)

要在控制面板中生成键对，请执行以下步骤：

1. 打开&#x200B;**[!UICONTROL Instance settings]**&#x200B;卡，然后选择&#x200B;**[!UICONTROL GPG keys]**&#x200B;选项卡和所需的Adobe Campaign实例。

1. 单击 **[!UICONTROL Generate Key]** 按钮。

   ![](assets/gpg_generate.png)

1. 指定键的名称，然后单击&#x200B;**[!UICONTROL Generate Key]**。 此名称将帮助您确定用于解密的活动工作流

   ![](assets/gpg_generate_name.png)

生成密钥对后，公共密钥将显示在列表中。 请注意，解密密钥对是在没有过期日期的情况下生成的。

您可以使用&#x200B;**...**&#x200B;按钮，下载公钥或复制其指纹。

![](assets/gpg_generate_list.png)

随后，公共密钥可用于与任何外部系统共享。 Adobe Campaign将能够在数据加载活动中使用私钥来解密已用公钥加密的数据。

有关详细信息，请参阅Adobe Campaign文档：

**Campaign Classic:**

* [在处理之前解压缩或解密文件](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/unzip-decrypt.html)
* [用例：导入使用由控制面板生成的密钥加密的数据](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/unzip-decrypt.html#use-case-gpg-decrypt)

**Campaign Standard:**

* [管理加密数据](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html)
* [用例：导入使用由控制面板生成的密钥加密的数据](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html#use-case-gpg-decrypt)

## 监视GPG密钥

要访问为实例安装和生成的GPG密钥，请打开&#x200B;**[!UICONTROL Instance settings]**&#x200B;卡，然后选择&#x200B;**[!UICONTROL GPG keys]**&#x200B;选项卡。

![](assets/gpg_list.png)

该列表显示为您的实例安装和生成的所有加密和解密GPG密钥，其中包含每个密钥的详细信息：

* **[!UICONTROL Name]**:安装或生成密钥时定义的名称。
* **[!UICONTROL Use case]**:此列指定键的用例：

   ![](assets/gpg_icon_encrypt.png):已为数据加密安装密钥。

   ![](assets/gpg_icon_decrypt.png):已生成密钥以允许数据解密。

* **[!UICONTROL Fingerprint]**:钥匙的指纹。
* **[!UICONTROL Expires]**:密钥的过期日期。请注意，控制面板将在主要期限接近到期时提供可视指示：

   * 30天前显示紧急（红色）。
   * 警告（黄色）在60天前显示。
   * 密钥过期后，将显示“已过期”红色横幅。

   >[!NOTE]
   >
   >请注意，控制面板不会发送任何电子邮件通知。

作为最佳做法，我们建议您删除您不再需要的任何密钥。 为此，请单击&#x200B;**...**&#x200B;按钮，然后选择&#x200B;**[!UICONTROL Delete Key]。**。

![](assets/gpg_delete.png)

>[!IMPORTANT]
>
>在删除密钥之前，请确保在任何Adobe Campaign工作流中未使用该密钥，以防止其失败。

## 教程视频{#video}

以下视频演示了如何生成和安装用于数据加密的GPG密钥。

在[Campaign Classic](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/instance-settings/gpg-key-management/gpg-key-management-overview.html?lang=en#instance-settings)和[Campaign Standard](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/instance-settings/gpg-key-management/gpg-key-management-overview.html?lang=en#instance-settings)教程页面中提供了与GPG键管理相关的其他操作说明视频。

>[!VIDEO](https://video.tv.adobe.com/v/36386?quality=12)

