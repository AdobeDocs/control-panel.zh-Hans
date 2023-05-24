---
product: campaign
solution: Campaign
title: 将 IP 范围添加到允许列表
description: 了解如何将 IP 范围添加到 SFTP 服务器访问允许列表
feature: Control Panel
role: Architect
level: Experienced
exl-id: 45a3bfcd-500c-4139-b610-d39989260ab7
source-git-commit: c1c80c03a351613ec0c6870a11ab39a634e8eab7
workflow-type: tm+mt
source-wordcount: '1048'
ht-degree: 39%

---

# 将 IP 范围添加到允许列表 {#ip-range-allow-listing}

>[!CONTEXTUALHELP]
>id="cp_ip_whitelist"
>title="关于 IP 允许列表"
>abstract="在此选项卡中，您可以向允许列表添加 IP 范围，以建立与 SFTP 服务器的连接。此处仅显示您有权访问的 SFTP 服务器。请联系您的管理员以请求访问其他 SFTP 服务器。"
>additional-url="https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4#t=98" text="观看演示视频"

SFTP 服务器受到保护。為了能夠存取它們以檢視檔案或撰寫新檔案，您需要將存取伺服器的系統或使用者端的公用IP位址新增至允許清單。

![](assets/do-not-localize/how-to-video.png)在使用 [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/sftp-management/adding-ip-range-to-allow-list.html#sftp-management) 或 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/sftp-management/adding-ip-range-to-allow-list.html#sftp-management) 的视频中了解这一功能

## 关于 CIDR 格式 {#about-cidr-format}

CIDR（无类域间路由）是在控制面板界面中添加 IP 范围时受支持的格式。

语法依次由 IP 地址、“/”字符和十进制数字组成。中會詳細說明格式及其語法 [本文](https://whatismyipaddress.com/cidr){target="_blank"}.

您可以在網際網路上搜尋免費的線上工具，協助您將現有的IP範圍轉換為CIDR格式。

## 最佳实践 {#best-practices}

在控制面板中将 IP 地址添加到允许列表时，请确保遵循以下建议和限制条件。

* **将 IP 范围添加到允许列表**，而不是单个 IP 地址。要将单个 IP 地址添加到允许列表，请在其中附加“/32”，以标识该范围仅包含单个 IP 地址。
* **请勿向允许列表添加非常宽的范围**，例如，包括 > 265 个 IP 地址。控制面板将拒绝任何介于 /0 和 /23 之间的 CIDR 格式范围。
* 只能将&#x200B;**公共 IP 地址**&#x200B;添加到允许列表。
* 請確定 **定期刪除IP位址** 您不再需要的資訊。

## 向允许列表添加 IP 地址 {#adding-ip-addresses-allow-list}

>[!CONTEXTUALHELP]
>id="cp_sftp_iprange_add"
>title="IP 范围配置"
>abstract="定义要添加到允许列表以连接到 SFTP 服务器的 IP 范围。"

要向允许列表添加 IP 范围，请执行以下步骤：

1. 打开 **[!UICONTROL SFTP]** 卡，然后选择 **[!UICONTROL IP Allow Listing]** 选项卡。
1. 将为每个实例显示允许列表上的 IP 地址列表。从左侧列表中选择所需的实例，然后单击 **[!UICONTROL Add new IP range]**&#x200B;按钮。

   ![](assets/control_panel_add_range.png)

1. 定義您要新增至允許清單的IP範圍。 此欄位僅接受CIDR格式的IP範圍，例如 *192.150.5.0/24*.

   ![](assets/control_panel_add_range4.png)

   >[!IMPORTANT]
   >
   >IP 范围不能与允许列表上的现有范围重叠。在这种情况下，首先删除包含重叠 IP 的范围。

1. 您可以將範圍新增至多個執行個體的允許清單。 为此，请按向下箭头键或键入所需实例的前几个字母，然后从建议列表中选择该实例。

   ![](assets/control_panel_add_range3.png)

1. 定義清單中為此IP範圍顯示的標籤。

   ![](assets/control_panel_add_range2.png)

   >[!NOTE]
   >
   >中允許使用下列特殊字元 **[!UICONTROL Label]** 欄位：
   > `. _ - : / ( ) # , @ [ ] + = & ; { } ! $`

1. 為了更好地管理您的IP允許清單，您可以設定每個IP範圍可用性的持續時間。 若要這麼做，請選取 **[!UICONTROL Type]** 下拉式清單，並在對應欄位中定義持續時間。 如需IP範圍到期的詳細資訊，請參閱 [本節](#expiry).

   ![](assets/control_panel_add_range5.png)

   >[!NOTE]
   >
   >根據預設， **[!UICONTROL Type]** 欄位已設為 **[!UICONTROL Unlimited]**，表示IP範圍永不過期。

1. 在 **[!UICONTROL Comment]** 欄位中，您可以指出允許此IP範圍的原因（原因、對象等）。

1. 单击 **[!UICONTROL Save]** 按钮。允許清單的IP範圍新增專案會顯示為 **[!UICONTROL Pending]** 直到完全處理要求為止，這應該只需要幾秒鐘的時間。

   ![](assets/control_panel_add_range6.png)

>[!IMPORTANT]
>
>如果您嘗試將SFTP伺服器連線至新系統，並因此將新IP範圍新增至允許清單，則可能需要輸入新的公開金鑰才能完成連線。 有关更多信息，请参阅[此章节](key-management.md)。

## 管理IP範圍 {#managing-ip-ranges}

您建立的IP範圍會顯示在 **[!UICONTROL IP Allow Listing]** 標籤。

您可以根據建立日期或編輯日期、建立或編輯該日期的使用者以及IP範圍到期日來排序專案。

您也可以透過開始輸入標籤、範圍、名稱或註解來搜尋IP範圍。

![](assets/control_panel_allow_list_sort.png)

若要編輯一或多個IP範圍，請參閱 [本節](#editing-ip-ranges).

若要從允許清單中刪除一個或多個IP範圍，請選取範圍，然後按一下 **[!UICONTROL Delete IP range]** 按鈕。

![](assets/control_panel_delete_range.png)

### 到期日 {#expiry}

此 **[!UICONTROL Expires]** 欄顯示IP範圍到期前的剩餘天數。

如果您訂閱 [電子郵件警示](../../performance-monitoring/using/email-alerting.md)，您會在IP範圍到期的10天及5天前，以及在到期當天，收到電子郵件通知。 收到警報後，您可以 [編輯IP範圍](#editing-ip-ranges) 以視需要延長有效期。

過期的IP範圍將在7天後自動刪除。 它顯示為 **[!UICONTROL Expired]** 在 **[!UICONTROL Expires]** 欄。 在此7天期間內：

* 過期的IP範圍無法再用來存取SFTP伺服器。

* 您無法建立與過期範圍重疊的另一個IP範圍。 您必須先刪除過期的IP範圍，才能建立新IP範圍。

* 您可以 [編輯](#editing-ip-ranges) 過期的IP範圍並更新其持續時間，以使其再次可用。

* 您可以從允許清單中刪除它。

## 編輯IP範圍 {#editing-ip-ranges}

>[!CONTEXTUALHELP]
>id="cp_sftp_iprange_update"
>title="更新 IP 范围"
>abstract="更新允许连接到 SFTP 服务器的选定 IP 范围。"

若要編輯IP範圍，請遵循下列步驟。

>[!NOTE]
>
>您只能編輯自「控制面板」2021年10月發行版本以來建立的IP範圍。

<!--Edition is not available for IP ranges that have been created before the Control Panel October 2021 release.-->

1. 從中選擇一個或多個IP範圍 **[!UICONTROL IP Allow Listing]** 清單。

1. 单击 **[!UICONTROL Update IP range]** 按钮。

   ![](assets/control_panel_edit_range.png)

1. 您只能編輯IP範圍到期日和/或新增註釋。

   >[!NOTE]
   >
   >若要修改CIDR格式、其標籤或編輯相關執行個體，您必須先刪除IP範圍，然後建立符合您需求的新範圍。

   ![](assets/control_panel_edit_range2.png)

1. 保存您的更改。

## 监控更改 {#monitoring-changes}

此 **[!UICONTROL Job Logs]** 「控制面板」首頁可讓您追蹤及監控對允許清單上IP位址所做的所有變更。

有关控制面板界面的详细信息，请参阅[此部分](../../discover/using/discovering-the-interface.md)。

![](assets/control_panel_ip_log.png)
