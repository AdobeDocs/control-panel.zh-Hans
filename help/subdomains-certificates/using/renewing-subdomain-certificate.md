---
title: 续订子域的SSL证书
description: 了解如何续订子域的SSL证书
translation-type: tm+mt
source-git-commit: bc29433167d4699ad9b840381abd0d5bbff8c630
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---


# 续订子域的SSL证书 {#renewing-subdomains-ssl-certificates}

>[!CONTEXTUALHELP]
>id="cp_add_ssl_certificate"
>title="添加SSL证书"
>abstract="要添加SSL证书，您需要生成CSR，为子域购买SSL证书并安装证书包。"
>additional-url="https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#generating-csr" text="生成证书签名请求(CSR)"
>additional-url="https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#installing-ssl-certificate" text="如何安装SSL证书"

>[!IMPORTANT]
>
>控制面板中的子域委派在测试版中可用，如有频繁更新和修改，恕不另行通知。

## 关于证书续订 {#about-certificate-renewal-process}

SSL证书续订过程包括3个步骤：

1. **生成证书签名请求(CSR)Adobe客**&#x200B;户服务会为您生成CSR。 您需要提供生成CSR所需的一些信息（如公用名称、组织名称和地址等）。
1. **购买SSL证书**&#x200B;生成CSR后，您可以下载它并使用它从公司批准的证书颁发机构购买SSL证书。
1. **安装SSL证书购**&#x200B;买SSL证书后，可将其安装到所需子域。

## 生成证书签名请求(CSR) {#generating-csr}

>[!CONTEXTUALHELP]
>id="cp_generate_csr"
>title="生成CSR"
>abstract="必须为您计划在购买证书之前保护的实例和子域生成证书签名请求。"

>[!CONTEXTUALHELP]
>id="cp_select_subdomains"
>title="选择CSR的子域"
>abstract="您可以选择在证书签名请求中包含所有或仅包含特定子域。 只有选定的子域将通过购买的SSL证书进行认证。"
>additional-url="https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#generating-csr" text="生成证书签名请求(CSR)"
>additional-url="https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/subdomains-branding.html" text="关于子域品牌"

要生成证书签名请求(CSR)，请执行以下步骤：

1. 在卡 **[!UICONTROL Subdomains & Certificates]** 中，选择所需的实例，然后单击 **[!UICONTROL Manage Certificate]** 按钮。

   ![](assets/renewal1.png)

1. 选 **[!UICONTROL 1 - Generate a CSR]**&#x200B;择，然 **[!UICONTROL Next]** 后单击以启动向导，引导您完成CSR生成过程。

   ![](assets/renewal2.png)

1. 此时会显示一个表单，其中包含生成CSR所需的所有详细信息。

   确保完整、准确地填写所请求的信息，否则可能无法续订证书（如有必要，请与您的内部团队、安全部门和IT团队联系），然后单击 **[!UICONTROL Next]**。

   * **[!UICONTROL Organization]**: 官方组织名称。
   * **[!UICONTROL Organization Unit]**: 链接到子域的设备(示例： 营销、IT)。
   * **[!UICONTROL Instance]** （预填）: 与子域关联的活动实例的URL。
   ![](assets/renewal3.png)

1. 选择要包含在CSR中的子域，然后单击 **[!UICONTROL OK]**。

   ![](assets/renewal4.png)

1. 所选子域显示在列表中。 对于每个子域，选择要包含的子域，然后单击 **[!UICONTROL Next]**。

   ![](assets/renewal5.png)

1. 此时将显示要包含在CSR中的子域的摘要。 单击 **[!UICONTROL Submit]** 以确认您的请求。

   ![](assets/renewal6.png)

1. 将自动生成并下载与您的选择相对应的。csr文件。 您现在可以使用它从公司批准的证书颁发机构购买SSL证书。

   >[!NOTE]
   >
   >如果未保存／下载CSR，它将丢失，您将必须重新生成它。

## 使用CSR购买证书 {#purchasing-certificate}

从控制面板获取证书签名请求CSR后，从您的组织批准的证书颁发机构购买SSL证书。

## 安装SSL证书 {#installing-ssl-certificate}

>[!CONTEXTUALHELP]
>id="cp_install_ssl_certificate"
>title="安装SSL证书"
>abstract="安装您从您所在组织批准的证书颁发机构购买的SSL证书。"
>additional-url="https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/subdomains-branding.html" text="关于子域品牌"

购买SSL证书后，您可以在实例上安装它。 在继续操作之前，请确保您了解以下先决条件：

* 证书签名请求(CSR)必须是从控制面板中生成的。 否则，您将无法从控制面板安装证书。
* 证书签名请求(CSR)应与已委托给Adobe的子域相匹配。 例如，它不能包含已委托的子域。
* 证书应具有当前日期。 将来无法安装日期为的证书，且不应过期(即有效开始和结束日期)。
* 证书应由受信任的证书颁发机构(CA)颁发，如Comodo、DigiCert、GoDaddy等。
* 证书的大小应为2048位，算法应为RSA。
* 证书应采用X.509 PEM格式。
* 支持SAN证书。
* 不支持通配符证书。
* ZIP文件或证书不应受口令保护。
* ZIP文件最好在单个文件中只包含以下内容：
   * 最终实体证书。
   * 中间证书链（按适当顺序排列）。
   * 根证书（可选）。

要安装证书，请执行以下步骤：

1. 在卡 **[!UICONTROL Subdomains & Certificates]** 中，选择所需的实例，然后单击 **[!UICONTROL Manage Certificate]** 按钮。

   ![](assets/renewal1.png)

1. 选 **[!UICONTROL 3 - Install Certificate Bundle]**&#x200B;择，然 **[!UICONTROL Next]** 后单击以启动向导，该向导将指导您完成证书安装过程。

   ![](assets/install1.png)

1. 选择包含要安装的证书的。zip文件，然后单击 **[!UICONTROL Submit]**。

   ![](assets/install2.png)

>[!NOTE]
>
>证书将安装在CSR中包含的所有域／子域上。 证书中存在的任何其他域／子域将不被考虑在内。

安装SSL证书后，证书的过期日期和状态图标会相应更新。

**相关主题：**

* [添加SSL证书（教程视频）](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/adding-ssl-certificates.html)
* [子域品牌](../../subdomains-certificates/using/subdomains-branding.md)
* [监视子域](../../subdomains-certificates/using/monitoring-subdomains.md)