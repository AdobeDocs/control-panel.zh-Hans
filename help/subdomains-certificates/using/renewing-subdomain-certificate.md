---
product: campaign
solution: Campaign
title: 续订子域的 SSL 证书
description: 了解如何续订子域的 SSL 证书
feature: Control Panel
role: Architect
level: Experienced
exl-id: e9b7c67d-6afa-44f9-b19d-39c0ec9a7edd
source-git-commit: 5a5ac1a604fe5bdce07479ff84184abdb2e0ddba
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 28%

---

# 续订SSL证书 {#renewing-subdomains-ssl-certificates}

>[!CONTEXTUALHELP]
>id="cp_add_ssl_certificate"
>title="SSL证书续订"
>abstract="要续订SSL证书，您需要生成CSR，为子域购买SSL证书，并安装证书包。"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#generating-csr" text="生成证书签名请求 (CSR)"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#installing-ssl-certificate" text="安装SSL证书"

>[!IMPORTANT]
>
>测试版中提供控制面板的SSL证书续订，如有频繁更新和修改，恕不另行通知。
>
>如果您使用具有混合托管模型的实例，则只能查看与委派的子域关联的证书，并且将无法续订这些证书。

SSL 证书续订过程包括以下 3 个步骤：

1. **生成证书签名请求(CSR)**

   在购买证书之前，必须为您计划保护的实例和子域生成证书签名请求。您需要提供生成 CSR 所需的一些信息（如公用名称、组织名称和地址等）。[了解详情](generate-csr.md)

1. **购买SSL证书**

   生成CSR后，您可以使用它从公司批准的认证中心购买SSL证书。

1. **安装SSL证书**

   在所需子域上安装购买的SSL证书以保护它们。 [了解详情](install-ssl-certificate.md)

![](assets/do-not-localize/how-to-video.png) 使用 [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html#subdomains-and-certificates) 或 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html#adding-ssl-certificates)

**相关主题：**

* [可交付性最佳实践指南 — 适用于Adobe Campaign的SSL证书请求流程](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/campaign/ac-ssl-certificate-request.html)
* [子域品牌化](../../subdomains-certificates/using/subdomains-branding.md)
* [监测子域](../../subdomains-certificates/using/monitoring-subdomains.md)
