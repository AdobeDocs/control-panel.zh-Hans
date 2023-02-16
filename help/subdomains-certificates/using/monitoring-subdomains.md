---
product: campaign
solution: Campaign
title: 监测子域
description: 监控子域，以确保所有子域均已正确配置以与Adobe Campaign配合使用。
feature: Control Panel
role: Architect
level: Experienced
exl-id: edd55d07-bf0b-44b0-8281-be69c698d5e8
source-git-commit: 76c42ba45b3430b1b93458f18b1b0e78f289fad1
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 7%

---

# 监测子域 {#monitoring-subdomains}

>[!CONTEXTUALHELP]
>id="cp_subdomain_undelegate"
>title="删除委派的子域 "
>abstract="利用此屏幕，可删除已在控制面板中委派的任何子域。 请记住，子域删除无法撤消，提交后将不可撤消。<br><br>如果您尝试为所选实例删除主域，将要求您选择将替换该主域的域。"

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
