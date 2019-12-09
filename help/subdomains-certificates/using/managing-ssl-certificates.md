---
title: 管理子域的SSL证书
description: 了解如何监视子域的SSL证书并启动其续订过程
translation-type: tm+mt
source-git-commit: 6bc165f995d34d21b5bce379db3095317db10906

---


# 管理子域的SSL证书 {#managing-subdomains-ssl-certificates}

该 **[!UICONTROL Subdomains and Certificates]**卡允许您查看登录页面和资源所在的子域和关联子域中安装了SSL证书的哪些。 您还可以轻松查看哪些子域具有过期的证书，以便预测其过期。

如果证书即将过期，您随后可以发起客户关怀请求，并提供所有必需信息以续订证书并确保实例正常工作。

>[!NOTE]
>
>Adobe 建议您&#x200B;**在证书即将到期之前**，续订相关子域的 SSL 证书。证书续订可能需要数天，具体取决于您的组织，我们建议您为此流程分配适当的时间。

## 监视SSL证书 {#monitoring-ssl-certificates}

选择卡时，可以直接访问每个实例的子域列 **[!UICONTROL Subdomains & Certificates]**表。

子域按SSL证书的最近过期日期进行排列，其中包含过期的可视信息（以天为单位）:

* **绿色**:子域未在未来60天内过期的证书。
* **橙色**:一个或多个子域有一个证书，该证书将在接下来的60天内过期。
* **红色**:一个或多个子域有一个证书，该证书将在30天内过期。

![](assets/visual_alert2.png)

To get more details on a subdomain&#39;s certificates, click the **[!UICONTROL Certificate Details]**button.

![](assets/certificate_details4.png)

所有相关子域的列表将显示在其证书上。 它通常包括登陆页面、资源页面等的子域。

![](assets/monitoring_subdomains_details2.png)

如有必要，您可以从此窗口启动证书续订请求。 有关此内容的详细信息，请参阅下面的部分。

## 启动SSL证书续订 {#initiating-ssl-certificate-renewal}

>[!NOTE]
>
>控制面板不自动管理证书续订。 它仅允许您准 **备要发送到Adobe Campaign客户关怀的请求** ，以启动续订流程。

SSL证书续订过程包括3个步骤：

1. **生成证书签名请求(CSR)** Adobe客户关怀会根据客户关怀门户提供的请求为您生成CSR。 您需要提供生成CSR所需的一些信息（如公用名称、组织名称和地址等）。 在控制面板中，您可以在启动续订过程时看到所需项目的列表。 有关此内容的详细信息，请参阅下面的部分。
1. **购买SSL证书**&#x200B;一旦客户关怀部门生成CSR，您就可以下载SSL证书并从贵公司批准的认证中心购买SSL证书。
1. **安装SSL证书**&#x200B;购买SSL证书后，您需要将其提供给Adobe客户关怀团队。 此时将安装证书，并且您将在控制面板中看到证书的更新过期日期。

要在控制面板中启动SSL证书续订，请执行以下步骤：

1. 打开卡 **[!UICONTROL Subdomains & Certificates]**，然后单击具有**[!UICONTROL Certificate details]** 过期证书的子域的图标。

   ![](assets/renewal1.png)

1. 此时将显示相关子域的列表。其中通常包括登陆页面、资源页面等的子域。Click the **[!UICONTROL Ticket Details]**button to initiate the certificates renewal process.

   ![](assets/renewal2.png)

1. 此时会显示一个表单，其中包含续订SSL证书所需的所有详细信息。 确保完整、准确地填写所请求的信息（如有必要，请与内部团队、安全和IT团队联系）。 否则，将无法生成证书签名请求，您将无法续订证书。

   * **[!UICONTROL IMS Org]**:您组织的ID。
   * **[!UICONTROL Instance]**:与子域关联的系列活动实例的URL。
   * **[!UICONTROL Common name]**:这通常是跟踪子域URL，与具有即将过期证书的子域相关联。
   * **[!UICONTROL Subdomains]**:链接到具有过期证书的子域的子域。 如果要将单个SSL证书应用到其他子域，可将其添加到此列表。 在这种情况下，请确保这些子域与同一IMS组织和实例URL关联。
   >[!CAUTION]
   >
   >The **[!UICONTROL IMS Org]**and**[!UICONTROL Instance]** fields are filled in automatically by the Control Panel and should not be modified.

   ![](assets/renewal3.png)

1. 表单完成后，单击按 **[!UICONTROL Copy Details]**钮将信息保存到剪贴板。

   >[!NOTE]
   >
   >如果您没有清除浏览器历史记录，您输入的信息将会保存，以便您以后使用它来续订证书。

1. 单击按 **[!UICONTROL Log new ticket]**钮。 您会被自动重定向到Adobe Campaign客户关怀登录页面。

   ![](assets/renewal4.png)

1. 登录，然后使用“SSL证书CSR请求”主题创建新的支持票证。
将之前复制的所有信息粘贴到票证正文中，然后单击“提交”。

   >[!NOTE]
   >
   >如果您没有权限为您的组织提交支持案例，请将您复制到剪贴板的所有信息传递给您的支持联系人，并要求他们为您打开一个新的客户关怀票证。

**相关主题：**

* [Campaign standard教程视频](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/managing-ssl-certificates.html)
* [Campaign Classic教程视频](https://docs.adobe.com/content/help/en/campaign-learn/campaign-classic-tutorials/administrating/control-panel-acc/managing-ssl-certificates.html)
