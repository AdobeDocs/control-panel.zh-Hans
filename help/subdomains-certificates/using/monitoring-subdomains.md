---
product: campaign
solution: Campaign
title: 监测子域
description: 监控子域，确保所有子域均已正确配置以用于Adobe Campaign。
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: edd55d07-bf0b-44b0-8281-be69c698d5e8
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 9%

---


# 监控子域 {#monitoring-subdomains}

必须监控子域，以确保所有子域均已正确配置以便与Adobe Campaign配合使用。

选择 **[!UICONTROL 子域和证书]** 卡片。

此 **[!UICONTROL 上次验证]** 列指示上次验证子域的时间。 您可以随时通过单击 **...** / **[!UICONTROL 验证子域]** 按钮。

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>Adobe不建议使用没有证书日期的子域，因为这可能意味着这些子域可能有一些可投放性问题。

启动验证时，会执行若干操作来检查子域是否正确配置（例如租户检查、电子邮件发送测试等） 如果子域验证失败，请联系Adobe客户关怀部门以进一步调查。

**相关主题：**

* [续订子域的 SSL 证书](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [子域品牌化](../../subdomains-certificates/using/subdomains-branding.md)
