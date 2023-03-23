---
product: campaign
solution: Campaign
title: GPG 密钥管理
description: 了解如何管理GPG密钥，以在Adobe Campaign中加密和解密数据。
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

## 关于GPG加密 {#about-gpg-encryption}

GPG加密允许您使用以下系统的公共 — 私钥对保护数据： [OpenPGP](https://www.openpgp.org/about/standard/) 规范。

实施后，您可以在传输之前对传入数据进行解密和加密，以确保没有有效匹配密钥对的任何人都不会访问这些数据。

要利用 Campaign 实现 GPG 加密，管理员用户必须直接从控制面板在营销实例上安装和/或生成 GPG 密钥。

然后，您将能够：

* **加密发送的数据**:Adobe Campaign在使用已安装的公钥对数据进行加密后，会发送数据。

* **解密传入数据**:Adobe Campaign接收从外部系统使用从控制面板下载的公共密钥加密的数据。 Adobe Campaign使用从控制面板生成的私钥解密数据。

## 加密数据 {#encrypting-data}

控制面板允许您加密从 Adobe Campaign 实例中传出的数据。

要实现此目的，您需要从PGP加密工具生成GPG密钥对，然后将公共密钥安装到控制面板中。 然后，您将能够在从实例发送数据之前对其进行加密。 为此，请执行以下步骤：

>[!NOTE]
>
>您最多可以在控制面板中安装60个GPG密钥。

![](assets/do-not-localize/how-to-video.png)[ 在视频中发现此功能](#video)

1. 使用PGP加密工具生成公钥/私钥对，该工具跟在 [OpenPGP规范](https://www.openpgp.org/about/standard/). 为此，请安装GPG实用程序或GNuGP软件。

   >[!NOTE]
   >
   >提供了用于生成密钥的开源免费软件。 但是，请确保遵循贵组织的准则，并使用IT/安全组织推荐的GPG实用程序。

1. 安装该实用程序后，在Mac终端或Windows命令中运行以下命令。

   `gpg --full-generate-key`

1. 出现提示时，为您的键指定所需的参数。 必需的参数包括：

   * **键类型**:RSA
   * **键长度**:3072 - 4096比特
   * **实名** 和 **电子邮件地址**:用于跟踪创建密钥对的人。 输入链接到您的组织或部门的名称和电子邮件地址。
   * **评论**:向注释字段添加标签将帮助您轻松识别用于加密数据的密钥。
   * **过期**:日期或“0”表示没有过期日期。
   * **密码**

   ![](assets/do-not-localize/gpg_command.png)

1. 确认后，脚本将生成一个具有其关联指纹的密钥，您可以将其导出到文件中，或直接粘贴到控制面板中。 要导出文件，请运行此命令，然后运行生成的密钥的指纹。

   `gpg -a --export <fingerprint>`

1. 要将公钥安装到控制面板中，请打开 **[!UICONTROL Instance settings]** 卡，然后选择 **[!UICONTROL GPG keys]** 选项卡和所需的实例。

1. 单击 **[!UICONTROL Install Key]** 按钮。

   ![](assets/gpg_install_button.png)

1. 粘贴从PGP加密工具生成的公共密钥。 您还可以直接拖放导出的公共密钥文件。

   >[!NOTE]
   >
   >公钥应采用OpenPGP格式。

   ![](assets/gpg_install_paste.png)

1. 单击 **[!UICONTROL Install Key]** 按钮。

安装公钥后，该公钥会显示在列表中。 您可以使用 **...** 按钮下载或复制其指纹。

![](assets/gpg_install_download.png)

然后，可在Adobe Campaign工作流中使用键。 在使用数据提取活动时，您可以使用该数据来加密数据。

![](assets/do-not-localize/how-to-video.png)[ 在视频中发现此功能](#video)

有关此主题的更多信息，请参阅Adobe Campaign文档：

**Campaign v7/v8:**

* [压缩或加密文件](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/zip-encrypt.html)
* [用例：使用安装在控制面板上的密钥加密和导出数据](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html#use-case-gpg-encrypt)

**Campaign Standard:**

* [管理加密数据](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html)
* [用例：使用安装在控制面板上的密钥加密和导出数据](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/zip-encrypt.html#use-case-gpg-encrypt)

## 解密数据 {#decrypting-data}

控制面板允许您解密传入Adobe Campaign实例的外部数据。

为此，您需要直接从控制面板生成GPG密钥对。

* 的 **公钥** 将与外部系统共享，外部系统将使用该系统加密要发送到Campaign的数据。
* 的 **私钥** 将被Campaign用来解密传入的加密数据。

![](assets/do-not-localize/how-to-video.png)[ 在视频中发现此功能](#video)

要在控制面板中生成键对，请执行以下步骤：

1. 打开 **[!UICONTROL Instance settings]** 卡，然后选择 **[!UICONTROL GPG keys]** 选项卡和所需的Adobe Campaign实例。

1. 单击 **[!UICONTROL Generate Key]** 按钮。

   ![](assets/gpg_generate.png)

1. 指定键的名称，然后单击 **[!UICONTROL Generate Key]**. 此名称将帮助您确定在Campaign工作流中用于解密的密钥

   ![](assets/gpg_generate_name.png)

生成密钥对后，公共密钥将显示在列表中。 请注意，解密密钥对是在没有过期日期的情况下生成的。

您可以使用 **...** 按钮下载公钥或复制其指纹。

![](assets/gpg_generate_list.png)

然后，可以与任何外部系统共享公共密钥。 Adobe Campaign将能够在数据加载活动中使用私钥解密已使用公钥加密的数据。

有关更多信息，请参阅Adobe Campaign文档：

**Campaign v7和v8:**

* [在处理之前解压缩或解密文件](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/unzip-decrypt.html)
* [用例：导入使用由控制面板生成的密钥加密的数据](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/unzip-decrypt.html#use-case-gpg-decrypt)

**Campaign Standard:**

* [管理加密数据](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html)
* [用例：导入使用由控制面板生成的密钥加密的数据](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html#use-case-gpg-decrypt)

## 监控GPG密钥

要访问为实例安装和生成的GPG密钥，请打开 **[!UICONTROL Instance settings]** 卡，然后选择 **[!UICONTROL GPG keys]** 选项卡。

![](assets/gpg_list.png)

该列表显示已为实例安装和生成的所有加密和解密GPG密钥，其中包含每个密钥的详细信息：

* **[!UICONTROL Name]**:安装或生成密钥时定义的名称。
* **[!UICONTROL Use case]**:此列指定键的用例：

   ![](assets/gpg_icon_encrypt.png):已安装密钥以进行数据加密。

   ![](assets/gpg_icon_decrypt.png):已生成密钥以允许数据解密。

* **[!UICONTROL Fingerprint]**:钥匙的指纹。
* **[!UICONTROL Expires]**:密钥的过期日期。 请注意，控制面板将在关键到期日临近时提供直观指示：

   * 30天前显示紧急（红色）。
   * 警告（黄色）在60天前显示。
   * 密钥过期后，将显示“已过期”的红色横幅。

   >[!NOTE]
   >
   >请注意，控制面板不会发送任何电子邮件通知。

作为最佳实践，我们建议您删除不再需要的任何键。 为此，请单击 **...** 按钮，然后选择 **[!UICONTROL Delete Key].**.

![](assets/gpg_delete.png)

>[!IMPORTANT]
>
>在删除密钥之前，请确保未在任何Adobe Campaign工作流中使用该密钥，以防止其失败。

## 教程视频 {#video}

以下视频演示如何生成和安装用于数据加密的GPG密钥。

有关与GPG密钥管理相关的其他操作方法视频，请访问  [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/instance-settings/gpg-key-management/gpg-key-management-overview.html#instance-settings) 和 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/instance-settings/gpg-key-management/gpg-key-management-overview.html#instance-settings) 教程页面。

>[!VIDEO](https://video.tv.adobe.com/v/36386?quality=12)
