---
product: campaign
solution: Campaign
title: 监控子域的 SSL 证书
description: 了解如何监控子域的 SSL 证书
feature: 控制面板
role: Architect
level: Experienced
exl-id: edd55d07-bf0b-44b0-8281-be69c698d5e8
source-git-commit: 3bd3dcc0e09d887cab7d810d43f2c72bb4251ac9
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 17%

---

# 监测子域 {#monitoring-subdomains}

>[!AVAILABILITY]
>
>此功能不适用于Campaign v8。

必须监控子域，以确保所有子域均已正确配置以与Adobe Campaign配合使用。

选择&#x200B;**[!UICONTROL Subdomains & Certificates]**&#x200B;卡时，可以直接访问每个生产实例的子域列表。

**[!UICONTROL Last verification]**&#x200B;列指示上次验证子域的时间。 您可以随时通过单击&#x200B;**...** / **[!UICONTROL Verify subdomain]**&#x200B;按钮。

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>Adobe不建议使用没有证书日期的子域，因为这可能意味着这些子域可能存在一些可交付性问题。

启动验证时，会执行多项操作来检查子域是否正确配置（实例租户检查、电子邮件发送测试等）

如果子域的验证失败，请联系Adobe客户关怀团队以进一步调查。

**相关主题：**

* [续订子域的 SSL 证书](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [子域品牌化](../../subdomains-certificates/using/subdomains-branding.md)
