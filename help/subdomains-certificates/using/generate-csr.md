---
product: campaign
solution: Campaign
title: 续订子域的 SSL 证书
description: 了解如何续订子域的 SSL 证书
feature: Control Panel
role: Architect
level: Experienced
exl-id: b6d017c2-f633-48f7-8180-1264c1087fa2
source-git-commit: 9be5a3ae48dccf74f509aa95fee29bbfdafddcdf
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 59%

---

# 生成 CSR {#generating-csr}

>[!CONTEXTUALHELP]
>id="cp_generate_csr"
>title="CSR 生成"
>abstract="在购买证书之前，必须为您计划保护的实例和子域生成证书签名请求。"

>[!CONTEXTUALHELP]
>id="cp_select_subdomains"
>title="选择 CSR的子域"
>abstract="您可以选择在证书签名请求中包含所有子域或仅包含特定子域。只有选定的子域将通过购买的 SSL 证书进行认证。"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/subdomains-branding.html?lang=zh-Hans" text="关于子域品牌化"

## 生成 CSR {#generate}

要生成证书签名请求 (CSR)，请执行以下步骤：

1. 在 **[!UICONTROL Subdomains & Certificates]**&#x200B;卡中，选择所需的实例，然后单击 **[!UICONTROL Manage Certificate]** 按钮。

   ![](assets/renewal1.png)

1. 选择 **[!UICONTROL 1 - Generate a CSR]**，然后单击 **[!UICONTROL Next]** 以启动向导，引导您完成 CSR 生成过程。

   ![](assets/renewal2.png)

1. 此时将显示一个表单，其中包含生成 CSR 所需的所有详细信息。

   请确保完整准确地填写所请求的信息，否则可能无法续订证书（如有必要，请与您的内部团队、安全部门和 IT 团队联系），然后单击 **[!UICONTROL Next]**。

   * **[!UICONTROL Organization]**：官方组织名称。
   * **[!UICONTROL Organization Unit]**：链接到子域的单位（示例：营销、IT）。
   * **[!UICONTROL Instance]**（预填充）：与子域关联的 Campaign 实例的 URL。
   * **[!UICONTROL Common name]**：一般名稱預設為選取，您可以視需要選取其中一個子網域。

   ![](assets/renewal3.png)

1. 选择要包含在 CSR 中的子域，然后单击 **[!UICONTROL OK]**。

   ![](assets/renewal4.png)

1. 所选子域将显示在列表中。对于每个子域，选择要包含的子域，然后单击 **[!UICONTROL Next]**。

   ![](assets/renewal5.png)

1. 此时将显示要包含在 CSR 中的子域的摘要。单击 **[!UICONTROL Submit]**&#x200B;以确认您的请求。

   ![](assets/renewal6.png)

   >[!NOTE]
   >
   >此 **[!UICONTROL Copy CSR content]** 按鈕可讓您複製與CSR相關的所有資訊（組織ID、執行個體、組織名稱、通用名稱、包含的子網域等）

1. 将自动生成并下载与您的选择相对应的 .csr 文件。您现在可以使用它从公司批准的认证中心购买 SSL 证书。如果您需要再次下載CSR，請按照中詳述的步驟操作 [本節](#download).

產生CSR並下載後，您就可以使用它從貴組織核准的憑證機構購買SSL憑證。

購買SSL憑證後，您就能在執行個體上安裝該憑證，以保護您的子網域。 [了解详情](install-ssl-certificate.md)

## 下載CSR {#download}

若要購買SSL憑證，您必須先下載憑證申請檔。 CSR會在產生後自動下載。 您也可以隨時從工作記錄檔再次下載：

1. 在 **[!UICONTROL Job Logs]**，選取 **[!UICONTROL Finished]** 標籤，然後篩選清單以顯示與子網域管理相關的作業。

   ![](assets/renewal-download.png)

1. 開啟與CSR產生相對應的工作，然後按一下 **[!UICONTROL Downbload]** 連結以取得.csr檔案。

   ![](assets/renewal-download-button.png)
