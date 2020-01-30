---
title: 监视子域的SSL证书
description: 了解如何监视子域的SSL证书
translation-type: tm+mt
source-git-commit: 762c445713e6e728fc1a45d5fcf8c9c1cb0dcdf6

---


# 监视子域 {#monitoring-subdomains}

必须监控子域，以确保所有子域均正确配置以与Adobe Campaign配合使用。

选择卡时，可以直接访问每个生产实例的子域列 **[!UICONTROL Subdomains & Certificates]**表。

列 **[!UICONTROL Last verification]**指示上次验证子域的时间。** 您可以随时通过单击…… **./按**[!UICONTROL Verify subdomain]** 钮。

![](assets/subdomain_verification.png)

>[!CAUTION]
>
>Adobe不建议使用没有证书日期的子域，因为这可能意味着这些子域可能存在一些可交付性问题。

启动验证时，将执行多个操作以检查子域是否正确配置（实例租户检查、电子邮件发送测试等）

如果子域的验证失败，请与Adobe客户服务部门联系以进一步调查。

**相关主题：**

* [添加SSL证书（教程视频）](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/adding-ssl-certificates.html)
* [续订子域的SSL证书](../..help/subdomains-certificates/using/renewing-subdomain-certificate.md)
* [子域品牌](../../subdomains-certificates/using/subdomains-branding.md)
