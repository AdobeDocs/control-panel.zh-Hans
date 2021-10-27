---
product: campaign
solution: Campaign
title: 监控子域的 SSL 证书
description: 了解如何监控子域的 SSL 证书
feature: Control Panel
role: Architect
level: Experienced
exl-id: edd55d07-bf0b-44b0-8281-be69c698d5e8
source-git-commit: 46a4e13e8017c5406dcd65f21c9839374dd44aa7
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 16%

---

# 监测子域 {#monitoring-subdomains}

必须监控子域，以确保所有子域均已正确配置以与Adobe Campaign配合使用。

选择 **[!UICONTROL Subdomains & Certificates]** 卡。

的 **[!UICONTROL Last verification]** 列指示上次验证子域的时间。 您可以随时通过单击 **...** / **[!UICONTROL Verify subdomain]** 按钮。

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>Adobe不建议使用没有证书日期的子域，因为这可能意味着这些子域可能存在一些可交付性问题。

启动验证时，会执行多项操作来检查子域是否正确配置（实例租户检查、电子邮件发送测试等）

如果子域的验证失败，请联系Adobe客户关怀团队以进一步调查。

**相关主题：**

* [续订子域的 SSL 证书](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [子域品牌化](../../subdomains-certificates/using/subdomains-branding.md)
