---
product: campaign
solution: Campaign
title: 将子域的 SSL 证书委派给 Adobe
description: 了解如何将子域的SSL证书委派给Adobe
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 0eefdbde25c955c84ee7534976256ca4df9a686c
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 25%

---

# 将子域的 SSL 证书委派给 Adobe {#delegate-ssl-certificates}

>[!CONTEXTUALHELP]
>id="cp_managed_ssl"
>title="将子域的 SSL 证书委派给 Adobe"
>abstract="通过控制面板，可让 Adobe 管理您的子域的 SSL 证书。如果您使用 CNAME 设置您的子域，则将自动生成并提供证书记录，以便在您的域托管解决方案中生成证书。"

强烈建议将子域的SSL证书委派给Adobe，因为Adobe每年都会自动创建证书并在证书过期前续订证书。

如果您使用CNAME来设置子域委派，Adobe将提供证书记录以用于您的域托管解决方案来生成证书。

在设置新子域或为已委派的子域执行SSL证书委派到Adobe时。

>[!NOTE]
>
>Adobe 管理的 SSL 是一项免费功能，可供用户免费使用。

## 委派新子域的SSL证书 {#new}

要在设置新子域时委派SSL证书，请启用 **[!UICONTROL Opt for Adobe managed SSL for sub-domains]** 子域配置向导的选项。 稍后将在配置向导中提供要复制到托管解决方案中的证书记录。 有关详细步骤，请参见 [本节](setting-up-new-subdomain.md).

![](assets/cname-adobe-managed.png){width="70%" align="left"}

## 为已委派的子域委派SSL证书 {#delegated}

要为已委派的子域委派SSL证书，请单击所需子域旁边的省略号按钮，然后单击 **[!UICONTROL Switch to Managed SSL]**.

![](assets/delegate-ssl-list.png){width="70%" align="left"}

此时将显示一个对话框，其中包含Adobe自动生成的证书记录。 逐个复制这些记录，或通过下载CSV文件复制这些记录，然后导航到您的域托管解决方案以生成匹配的证书。

请确保所有证书记录都已生成到您的域托管解决方案中。 如果一切配置正确，请确认记录创建，然后单击 **[!UICONTROL Submit]**.

![](assets/delegate-ssl.png){width="70%" align="left"}
