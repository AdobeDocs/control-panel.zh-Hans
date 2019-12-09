---
title: 监视子域的SSL证书
description: 了解如何监视子域的SSL证书
translation-type: tm+mt
source-git-commit: cde5b58c1cf65d23b68c5fa6b1a484fc6db40325

---


# 监视子域的SSL证书 {#monitoring-ssl-certificates}

Adobe Campaign建议您保护托管登录页面的子域，尤其是那些收集客户敏感信息的子域。

**SSL（安全套接字层）加密** ，可确保您委托给Adobe的子域是安全的。 当您的客户填写Web表单或访问由Adobe Campaign托管的登录页面时，默认情况下，信息会通过非安全协议(HTTP)发送。 要确保更多安全性，请使用HTTPS协议保护发送的信息。 例如，您的“http://info.mywebsite.com/”子域地址现在将为“https://info.mywebsite.com/”。

**委派的子域本身不安装SSL证书**。 它们安装在关联的子域上，主要是托管登录页面、资源页面和其他子域。

**SSL证书的提供期限为特定时间段** （1年、60天等）。 证书过期后，您可能会在访问登录页面或使用子域中的资源时遇到问题。 为避免这种情况，控制面板允许您监视子域的SSL证书，并启动其续订过程。

有关子域委托的更多详细信 [息](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html)。

该 **[!UICONTROL Subdomains and Certificates]**卡允许您查看登录页面和资源所在的子域和关联子域中安装了SSL证书的哪些。

您还可以轻松查看哪些子域具有过期的证书，并根据需要续订它们。

>[!NOTE]
>
>Adobe 建议您&#x200B;**在证书即将到期之前**，续订相关子域的 SSL 证书。证书续订可能需要数天，具体取决于您的组织，我们建议您为此流程分配适当的时间。
<!-- note to remove? immediate, no more delay? -->

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
