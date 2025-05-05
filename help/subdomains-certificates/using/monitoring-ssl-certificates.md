---
product: campaign
solution: Campaign
title: 监控子域的 SSL 证书
description: 了解如何监控子域的 SSL 证书
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: a7888e1c-259d-4601-951b-0f1062d90dc2
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 监控子域的 SSL 证书 {#monitoring-ssl-certificates}

## 关于 SSL 证书 {#about-ssl-certificates}

Adobe Campaign 建议您保护托管登陆页面的子域，特别是那些收集客户敏感信息的子域。

**SSL（安全套接字层）加密**&#x200B;可确保您配置给 Adobe 的子域的安全性。当客户填写 Web 表单或访问由 Adobe Campaign 托管的登陆页面时，默认情况下，信息会通过非安全协议 (HTTP) 发送。为确保获得额外的安全性，请使用 HTTPS 协议保护已发送的信息。例如，您的“http://info.mywebsite.com/”子域地址现在将为“https://info.mywebsite.com/”。

**不会在配置的子域本身上安装 SSL 证书**。它们安装在关联的子域上，主要是托管登陆页面、资源页面等页面的子域。

**SSL 证书在特定时间段内提供**（1 年、60 天等）。一旦证书过期，您在访问登陆页面或使用子域的资源时可能会遇到问题。为防止出现这种情况，控制面板允许您监视子域的 SSL 证书，并启动其续订过程。

![](assets/no_certificate.png)

## SSL 证书管理 {#management}

SSL 证书监控是确保子域安全的关键。借助控制面板，您可以自行直接安装和续订子域的 SSL 证书，或将其委派给 Adobe，以便自动执行此过程，而无需您执行任何操作。

强烈建议将子域 SSL 证书管理委派给 Adobe，因为 Adobe 每年都会自动创建证书并在过期前续订证书。这降低了手动管理证书时可能出错的风险。[了解如何将子域的 SSL 证书委派给 Adobe](delegate-ssl.md)

在下面，您将找到与手动管理证书而不是将此操作委托给 Adobe 相关的影响的完整列表：

|       | 客户管理的证书 | Adobe 管理的证书 |
|  ---  |  ---  |  ---  |
| 证书提供方 | 第三方证书颁发机构 | Adobe 通过 AWS Certificate Manager 进行管理 |
| 手动步骤 | CSR 生成、证书购买和安装 | 无 |
| 续订流程 | 客户责任 | 由 Adobe 自动管理 |
| 子域安全 | 除非安装/续订证书，否则域可能具有不安全的子域（跟踪、镜像和解析）。 | 默认情况下，每个新域（如果选择 Adobe 托管）的所有子域都将受到保护。 |
| 证书费用 | 客户承担证书费用 | 免费 |

## 监控 SSL 证书 {#monitoring-certificates}

>[!CONTEXTUALHELP]
>id="cp_subdomain_details"
>title="子域详细信息"
>abstract="检索有关子域的 SSL 证书的信息。"

选择&#x200B;**[!UICONTROL 子域和证书]**&#x200B;信息卡时，子域的 SSL 证书状态可直接从子域的列表中获得。

子域按 SSL 证书最接近过期日期的顺序进行排列，其中包含过期的可视信息（以天为单位）:

* **绿色**：表示子域没有在未来 60 天内过期的证书。
* **橙色**：表示一个或多个子域有将在未来 60 天内过期的证书。
* **红色**：表示一个或多个子域有将在未来 30 天内过期的证书。
* **灰色**：表示尚未为子域安装证书。

![](assets/subdomains_list.png)

要获取有关子域的详细信息，请单击&#x200B;**[!UICONTROL 子域详细信息]**&#x200B;按钮。
此时将显示所有相关子域的列表。其中通常包括登陆页面、资源页面等的子域。

**[!UICONTROL 发送人信息]**&#x200B;选项卡提供有关已配置收件箱的信息（发件人、回复、错误电子邮件）。

![](assets/subdomain_details.png)

如果您的子域的某个 SSL 证书即将过期，您可以直接从控制面板续订该证书。有关更多信息，请参阅以下部分：[续订子域的 SSL 证书](../../subdomains-certificates/using/renewing-subdomain-certificate.md)。

**相关主题：**

* [续订子域的 SSL 证书](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [子域品牌化](../../subdomains-certificates/using/subdomains-branding.md)
