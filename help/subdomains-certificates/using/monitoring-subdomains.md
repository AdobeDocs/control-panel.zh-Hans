---
product: campaign
solution: Campaign
title: 监测子域
description: 重要的是，要监控子域以确保所有子域均已正确配置，以便与 Adobe Campaign 配合使用。
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: edd55d07-bf0b-44b0-8281-be69c698d5e8
TQID: 'https://experienceleague.adobe.com/49fMBOZ2iN7xs7PpnYRLDHpQO5eXMTvn-veAxpjeH7w'
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
feature_v2:
  - id: ae9127b0-c11d-467b-903d-a84cef43f6ed
    internal-label: Control Panel
  - id: a7760dfc-5c44-4d77-bb68-c50b1e265c93
    internal-label: Security and privacy
subfeature_v2:
  - id: f807e46f-d823-43a9-98be-82e0b2f3a05c
    internal-label: Subdomains and certificates
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
source-git-commit: b2723b0683a305a992b710a37a3e47927e1fb65e
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 100%
---
# 监控子域 {#monitoring-subdomains}

重要的是，要监控子域以确保所有子域均已正确配置，以便与 Adobe Campaign 配合使用。

选择&#x200B;**[!UICONTROL 子域和证书]**&#x200B;信息卡时，可以直接访问每个生产实例的子域列表。

**[!UICONTROL 上次验证]**&#x200B;列会指明上次验证子域的时间。 您可以通过单击 **...**/**[!UICONTROL 验证子域]**&#x200B;按钮随时进行验证。

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>Adobe 不建议使用没有证书日期的子域，因为这可能意味着此类子域可能存在某些可投放性问题。

启动验证时，会执行多个操作以检查子域是否配置正确（实例租户检查、电子邮件发送测试等）。 如果子域验证失败，请联系 Adobe 客户关怀部门以作进一步调查。

**相关主题：**

* [续订子域的 SSL 证书](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [子域品牌化](../../subdomains-certificates/using/subdomains-branding.md)
