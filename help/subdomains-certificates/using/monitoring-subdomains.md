---
product: campaign
solution: Campaign
title: 监控子域的 SSL 证书
description: 了解如何监控子域的 SSL 证书
translation-type: tm+mt
source-git-commit: 317b4c1cee34667a36f5e1a1197649bfd69c151a
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 16%

---


# 监控子域 {#monitoring-subdomains}

必须监视子域，以确保所有子域都正确配置以使用Adobe Campaign。

选择卡时，可以直接访问每个生产实例的子域 **[!UICONTROL Subdomains & Certificates]** 列表。

列 **[!UICONTROL Last verification]** 指示上次验证子域的时间。 您可以随时单击……/按 **钮来启** 动验 **[!UICONTROL Verify subdomain]** 证。

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>Adobe不建议使用没有证书日期的子域，因为这可能意味着这些子域可能存在一些可交付性问题。

启动验证时，将执行多个操作以检查子域是否正确配置（实例租户检查、电子邮件发送测试等）

如果子域的验证失败，请与Adobe客户服务部门联系以进一步调查。

**相关主题：**

* [续订子域的 SSL 证书](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [子域品牌化](../../subdomains-certificates/using/subdomains-branding.md)
