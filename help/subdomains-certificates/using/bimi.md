---
product: campaign
solution: Campaign
title: 添加BIMI记录
description: 了解如何为子域添加BIMI记录。
feature: Control Panel
role: Architect
level: Experienced
exl-id: eb7863fb-6e6d-4821-a156-03fee03cdd0e
source-git-commit: 64ea5e26786eea107983ee5025025c81334b0a91
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 0%

---

# 添加BIMI记录 {#dmarc}

## 关于BIMI记录 {#about}

邮件识别品牌指示器(BIMI)是一种行业标准，允许在邮箱提供商收件箱中的发件人电子邮件旁边显示批准的徽标，以增强品牌认知和信任。 它通过DMARC身份验证来验证发件人的身份，从而帮助防止电子邮件欺诈和网络钓鱼，使恶意行为者更难在电子邮件中假冒合法品牌。

有关BIMI实施的详细信息，请参见 [Adobe可投放性最佳实践指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-bimi.html)

![](assets/bimi-example.png){width="70%" align="center"}

## 限制和先决条件 {#limitations}

* SPF、DKIM和DMARC记录是创建BIMI记录的先决条件。
* 只能使用完全子域委派为子域添加BIMI记录。 [了解有关子域配置方法的更多信息](subdomains-branding.md#subdomain-delegation-methods)
* DMARC记录先决条件：

   * 子域的记录策略类型必须设置为“隔离”或“拒绝”。 DMARC策略类型设置为“无”时，无法创建BIMI记录。
   * 应用DMARC策略的电子邮件百分比必须为100%。 BIMI不支持将此百分比设为小于100%的DMARC政策。

[了解如何配置DMARC记录](dmarc.md)

## 为子域添加BIMI记录 {#add}

要为子域添加BIMI记录，请执行以下步骤：

1. 从子域列表中，单击所需子域旁边的省略号按钮，然后选择 **[!UICONTROL Subdomain details]**.

1. 单击 **[!UICONTROL Add TXT record]** 按钮，然后选择 **[!UICONTROL BIMI]** 从 **[!UICONTROL Record type]** 下拉列表。

   ![](assets/bimi-add.png)

1. 在 **[!UICONTROL Company Logo URL]**，指定包含您的徽标的SVG文件的URL。

1. 不过 **[!UICONTROL Certificate URL]** 可选，对于Gmail和Apple等覆盖邮箱市场80%的邮箱提供商而言，这是必需的。 因此，我们建议您获取经过验证的标记证书(VMC)，以真正利用BIMI。

   +++如何获得VMC？

   获取VMC的主要步骤如下：

   1. 在VMC发行商认可的知识产权局注册您的品牌徽标作为商标。 如果您有一个法律团队，我们建议您与其合作，以获取您的徽标商标或验证其已添加商标。

   1. 验证徽标已商标后，请联系DigiCert或Entrust证书颁发机构(CA)以请求VMC。

   1. 当VMC获得批准时，您将收到一个实体证书Privacy Enhanced Mail (PEM)文件。 将您从CA获取的任何其他中间证书附加到此PEM文件。 将PEM文件（以及附加的文件）上载到公共Web服务器，并记下PEM文件URL。 您将在BIMI TXT记录中使用URL。

   1. 一旦在特定子域的子域详细信息页面中显示BIMI记录，您就可以使用可用的BIMI检查器 [此处](https://bimigroup.org/bimi-generator/) 检查BIMI记录是否正常工作。

   有关BIMI实施的详细信息，请参见 [BIMI标准文档](https://bimigroup.org/implementation-guide/)
+++

1. 单击 **[!UICONTROL Add]** 确认创建BIMI记录。

处理BIMI记录创建后（大约5分钟），该记录会显示在子域的详细信息屏幕中。 [了解如何监测子域的TXT记录](gs-txt-records.md#monitor)
