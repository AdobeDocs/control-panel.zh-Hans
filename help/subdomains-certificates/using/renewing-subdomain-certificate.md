---
product: campaign
solution: Campaign
title: 续订子域的 SSL 证书
description: 了解如何续订子域的 SSL 证书
feature: Control Panel
role: Architect
level: Experienced
exl-id: e9b7c67d-6afa-44f9-b19d-39c0ec9a7edd
source-git-commit: 963c2af5cdca80ebc2cd79e0708dc4dfe8c6ec1e
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 100%

---

# 续订 SSL 证书 {#renewing-subdomains-ssl-certificates}

>[!CONTEXTUALHELP]
>id="cp_add_ssl_certificate"
>title="SSL 证书续订"
>abstract="要续订 SSL 证书，您需要生成 CSR，为子域购买 SSL 证书并安装证书捆绑包。"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html?lang=zh-Hans#generating-csr" text="生成证书签名请求 (CSR)"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html?lang=zh-Hans#installing-ssl-certificate" text="安装 SSL 证书"

SSL 证书续订过程包括以下 3 个步骤：

1. **生成证书签名请求 (CSR)**

   在购买证书之前，必须为您计划保护的实例和子域生成证书签名请求。您需要提供生成 CSR 所需的一些信息（如通用名称、组织名称和地址等）。[了解详情](generate-csr.md)

1. **购买 SSL 证书**

   生成 CSR 后，您可以将其用于从公司批准的认证中心购买 SSL 证书。

1. **安装 SSL 证书**

   在所需子域上安装购买的 SSL 证书以确保安全。[了解详情](install-ssl-certificate.md)

![](assets/do-not-localize/how-to-video.png)在介绍 [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html?lang=zh-Hans#subdomains-and-certificates) 或 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html?lang=zh-Hans#adding-ssl-certificates) 使用方法的视频中了解这一功能

**相关主题：**

* [可投放性最佳实践指南 - 适用于 Adobe Campaign 的 SSL 证书请求流程](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/campaign/ac-ssl-certificate-request.html?lang=zh-Hans)
* [子域品牌化](../../subdomains-certificates/using/subdomains-branding.md)
* [监测子域](../../subdomains-certificates/using/monitoring-subdomains.md)
