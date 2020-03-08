---
title: 续订子域的SSL证书
description: 了解如何续订子域的SSL证书
translation-type: tm+mt
source-git-commit: f22e356b283ee2601c948d5c1d514a9a59c58451

---


# 续订子域的SSL证书 {#renewing-subdomains-ssl-certificates}

>[!CONTEXTUALHELP]
>id=&quot;cp_add_ssl_certificate&quot;
>title=&quot;添加SSL证书&quot;
>abstract=&quot;要添加SSL证书，您需要生成CSR，为子域购买SSL证书并安装证书包。&quot;
>additional-url=&quot;https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#generating-csr&quot; text=&quot;Generating a Certificate Signing Request(CSR)&quot;
>additional-url=&quot;https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#installing-ssl-certificate&quot; text=&quot;如何安装SSL证书&quot;

>[!IMPORTANT]
>
>控制面板的子域委派功能在测试版中可用，并且如有频繁更新和修改，恕不另行通知。

## 关于证书续订 {#about-certificate-renewal-process}

SSL证书续订过程包括3个步骤：

1. **生成证书签名请求(CSR)** Adobe客户关怀将为您生成CSR。 您需要提供生成CSR所需的一些信息（如公用名称、组织名称和地址等）。
1. **购买SSL证书**&#x200B;生成CSR后，您可以下载它并使用它从贵公司批准的认证中心购买SSL证书。
1. **安装SSL证书购**&#x200B;买SSL证书后，可以将其安装到所需的子域上。

>[!NOTE]
>
>通过控制面板续订SSL证书仅适用于 **完全授权的子域** 。

## 生成证书签名请求(CSR) {#generating-csr}

>[!CONTEXTUALHELP]
>id=&quot;cp_generate_csr&quot;
>title=&quot;Generate CSR&quot;
>abstract=&quot;必须为您计划在购买证书之前保护的实例和子域生成证书签名请求。&quot;

>[!CONTEXTUALHELP]
>id=&quot;cp_select_subdomains&quot;
>title=&quot;为CSR选择子域&quot;
>abstract=&quot;您可以选择将所有或仅特定的子域包含到您的证书签名请求中。 只有选定的子域才会通过购买的SSL证书进行认证。”
>additional-url=&quot;https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#generating-csr&quot; text=&quot;Generating a Certificate Signing Request(CSR)&quot;
>additional-url=&quot;https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/subdomains-branding.html&quot; text=&quot;关于子域品牌&quot;

要生成证书签名请求(CSR)，请执行以下步骤：

1. 在卡 **[!UICONTROL Subdomains & Certificates]** 中，选择所需的实例，然后单击按 **[!UICONTROL Manage Certificate]** 钮。

   ![](assets/renewal1.png)

1. 选 **[!UICONTROL Generate a CSR]**&#x200B;择，然后单 **[!UICONTROL Next]** 击以启动向导，该向导将引导您完成CSR生成过程。

   ![](assets/renewal2.png)

1. 此时会显示一个表单，其中包含生成CSR所需的所有详细信息。

   确保完整、准确地填写所请求的信息，否则可能无法续订证书（如有必要，请与您的内部团队、安全和IT团队联系），然后单击 **[!UICONTROL Next]**。

   * **[!UICONTROL Organization]**:正式组织名称。
   * **[!UICONTROL Organization Unit]**:链接到子域的单位(示例：营销、IT)。
   * **[!UICONTROL Instance]** （预填）:与子域关联的系列活动实例的URL。
   ![](assets/renewal3.png)

1. 选择要包含在CSR中的子域，然后单击 **[!UICONTROL OK]**。

   ![](assets/renewal4.png)

1. 所选子域显示在列表中。 对于每个子域，选择要包含的子域，然后单击 **[!UICONTROL Next]**。

   ![](assets/renewal5.png)

1. 此时将显示要包含在CSR中的子域的摘要。 单击 **[!UICONTROL Submit]** 以确认您的请求。

   ![](assets/renewal6.png)

1. 系统会自动生成并下载与您的选择相对应的。csr文件。 您现在可以使用它从您的公司批准的认证中心购买SSL证书。

   >[!NOTE]
   >
   >如果未保存／下载CSR，则CSR将丢失，您将必须再次生成它。

## 使用CSR购买证书 {#purchasing-certificate}

从控制面板获取证书签名请求CSR后，从您的组织批准的认证中心购买SSL证书。

## 安装SSL证书 {#installing-ssl-certificate}

>[!CONTEXTUALHELP]
>id=&quot;cp_install_ssl_certificate&quot;
>title=&quot;安装SSL证书&quot;
>abstract=&quot;安装您从您所在组织批准的认证中心购买的SSL证书。&quot;
>additional-url=&quot;https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/subdomains-branding.html&quot; text=&quot;关于子域品牌&quot;

购买SSL证书后，您可以在实例中安装它。 在继续操作之前，请确保您了解以下先决条件：

* 证书签名请求(CSR)必须已从控制面板中生成。 否则，您将无法从控制面板安装证书。
* 证书签名请求(CSR)应与已委托给Adobe的子域相匹配。 例如，它不能包含已委托的子域。
* 证书应具有当前日期。 将来不能安装日期为的证书，并且不应过期（即有效的开始日期和结束日期）。
* 证书应由受信任的证书颁发机构(CA)颁发，如Comodo、DigiCert、GoDaddy等。
* 证书的大小应为2048位，算法应为RSA。
* 证书应采用X.509 PEM格式。
* 支持SAN证书。
* 不支持通配符证书。
* ZIP文件或证书不应受口令保护。
* ZIP文件最好在单个文件中仅包含以下内容：
   * 最终实体证书。
   * 中间证书链（按适当顺序排列）。
   * 根证书（可选）。

要安装证书，请执行以下步骤：

1. 在卡 **[!UICONTROL Subdomains & Certificates]** 中，选择所需的实例，然后单击按 **[!UICONTROL Manage Certificate]** 钮。

   ![](assets/renewal1.png)

1. 单击 **[!UICONTROL Install SSL Certificate]**，然 **[!UICONTROL Next]** 后启动向导，该向导将指导您完成证书安装过程。

   ![](assets/install1.png)

1. 选择包含要安装的证书的。zip文件，然后单击 **[!UICONTROL Submit]**。

   ![](assets/install2.png)

安装SSL证书后，证书的过期日期和状态图标会相应地更新。

**相关主题：**

* [添加SSL证书（教程视频）](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/adding-ssl-certificates.html)
* [子域品牌](../../subdomains-certificates/using/subdomains-branding.md)
* [监视子域](../../subdomains-certificates/using/monitoring-subdomains.md)