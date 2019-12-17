---
title: 设置新子域
description: 了解如何为营销活动实例设置新的子域
translation-type: tm+mt
source-git-commit: 85bef8fa652be883bc2afbc42a2d893ea75a4e77

---


# 设置新子域 {#setting-up-subdomain}

## 完全子域委托 {#full-subdomain-delegation}

控制面板允许您将子域完全委派到Adobe Campaign。 为此，请执行以下步骤：

1. 在卡中， **[!UICONTROL Subdomains & Certificates]**选择所需的生产实例，然后单击**[!UICONTROL Setup new subdomain]**。

   >[!NOTE]
   >
   >子域委派仅适用于 **生产** 实例。

   ![](assets/subdomain1.png)

1. 单击 **[!UICONTROL Next]**以确认完整的委派方法。

   >[!NOTE]
   >
   >[CNAME](#use-cnames) 和自定义方法当前不受控制面板支持。

   ![](assets/subdomain3.png)

1. 在您的组织所使用的托管解决方案中创建所需的子域和命名空间。 为此，请复制并粘贴向导中显示的Adobe Nameserver信息。

   有关如何在托管解决方案中创建子域的详细信息，请参阅此教程视频。

   ![](assets/subdomain4.png)

   创建子域时，请单击相应的Adobe名称服务器信息 **[!UICONTROL Next]**。

1. 为子域选择所需的用例：

   * **营销宣传**:用于商业目的的通信。 示例：销售电子邮件营销活动。
   * **交易和运营通信**:事务通信包含旨在完成收件人已开始与您联系的流程的信息。 示例：购买确认、密码重置电子邮件。 组织通信与组织内外的信息、想法和意见交流有关，无商业目的。
   >[!NOTE]
   >
   >根据用例划分子域是交付性的最佳实践。 这样，每个子域的信誉就被隔离和保护。
   >
   >例如，如果您用于营销通信的子域最终被Internet服务提供商列入黑名单，则您的交易通信子域将不会受到影响，并且将能够继续发送通信。

   ![](assets/subdomain5.png)

1. 输入您在托管解决方案中创建的子域，然后单击 **[!UICONTROL Submit]**。

   >[!NOTE]
   >
   > 确保填写要委 **托的子域** 的全名。 例如，要委派“usoffers.email.weretail.com”子域，请键入“usoffers.email.weretail.com”。

   ![](assets/subdomain6.png)

1. 提交子域后，控制面板将检查它当前指向Adobe NS记录，以及此子域不存在授权开始(SOA)记录。

1. 如果检查成功，控制面板将开始设置包含DNS记录、其他URL、收件箱等的子域。 单击该按钮可获取有关配置进度的更多详细 **[!UICONTROL Process details]**信息。

   ![](assets/subdomain7.png)

在流程结束时，子域将配置为与Adobe Campaign实例一起使用，并将创建以下元素：

* **具有以下** DNS记录的 **子域**:SOA、MX、CNAME、DKIM、SPF、TXT、
* **用于托管镜像** 、资源、跟踪页面和域密钥的其他子域、
* **收件箱**:发送者、错误、回复。

## CNAME的使用 {#use-cnames}

Adobe不建议使用CNAME进行子域委派，也不支持通过控制面板进行子域委派。

要使用此方法，请与您的Adobe客户关怀联系。
