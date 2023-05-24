---
product: campaign
solution: Campaign
title: 监测子域
description: 監視子網域，確保所有子網域皆已正確設定為可搭配Adobe Campaign使用。
feature: Control Panel
role: Architect
level: Experienced
exl-id: edd55d07-bf0b-44b0-8281-be69c698d5e8
source-git-commit: acf0334e894649d6b5edf0b96877c3f643894763
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 10%

---


# 监控子域 {#monitoring-subdomains}

監視子網域至關重要，以確保所有子網域皆已正確設定為可搭配Adobe Campaign使用。

選取「 」時，可直接存取每個生產執行個體的子網域清單 **[!UICONTROL Subdomains & Certificates]** 卡片。

此 **[!UICONTROL Last verification]** 欄指出上次驗證子網域的時間。 您可以隨時按一下 **...** / **[!UICONTROL Verify subdomain]** 按鈕。

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>Adobe不建議使用沒有憑證日期的子網域，因為這可能表示這些子網域可能有一些傳遞問題。

啟動驗證時，會執行數個操作來檢查子網域是否已正確設定（例項租使用者檢查、電子郵件傳送測試等） 如果子網域驗證失敗，請聯絡Adobe客戶服務以進一步調查。

**相关主题：**

* [续订子域的 SSL 证书](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [子域品牌化](../../subdomains-certificates/using/subdomains-branding.md)
