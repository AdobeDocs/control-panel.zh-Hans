---
title: 设置新子域
description: 了解如何为营销活动实例设置新的子域
translation-type: tm+mt
source-git-commit: cde5b58c1cf65d23b68c5fa6b1a484fc6db40325

---


# 设置子域 {#setting-up-subdomain}

控制面板允许您将子域完全委派到Adobe Campaign。 为此，请按照以下详细步骤操作。

>[!NOTE]
>
>控制面板不支持使用CNAME进行子域委派。 有关此方法的详细信息，请参 [阅本页](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html)。

1. 在卡 **[!UICONTROL Subdomains & Certificates]**中，选择所需的实例，然后单击按**[!UICONTROL Setup new subdomain]** 钮。

   ![](assets/subdomain1.png)

   >[!NOTE]
   >
   >该 **[!UICONTROL Setup new subdomain]**按钮仅可用于生产实例。

1. 选择方 **[!UICONTROL Delegation to Adobe]**法，然后单击**[!UICONTROL Next]**。

   ![](assets/subdomain3.png)

1. 在您的组织所使用的托管解决方案中创建所需的子域。 为此，请复制向导中显示的Adobe Nameserver信息，然后将其粘贴到您的托管解决方案中。

   有关如何在托管解决方案中创建子域的详细信息，请参阅可从向导访问的教程视频。

   ![](assets/subdomain4.png)

   创建子域时，请单击相应的Adobe名称服务器信息 **[!UICONTROL Next]**。

1. 为子域选择所需的用例：

   * **营销宣传**:用于商业目的的通信。 示例：销售电子邮件营销活动。
   * **交易和运营通信**:事务通信包含旨在完成收件人已开始与您联系的流程的信息。 示例：购买确认、密码重置电子邮件。 组织通信与组织内外的信息、想法和意见交流有关，无商业目的。
   按此方式划分子域是交付性的最佳实践。 这样，每个子域的信誉就被隔离和保护。 例如，如果您用于营销通信的子域最终被Internet服务提供商列入黑名单，则您的交易通信子域将不会受到影响，并且将能够继续发送通信。

   ![](assets/subdomain5.png)

   >[!NOTE]
   >
   >您只能选择为实例配置的用例。 如果实例仅配置为“营销通信”，则您将无法选择“交易和操作通信”用例。

1. 输入您使用Adobe Nameserver信息在托管解决方案中创建的子域，然后单击“提 **[交”]**。

   >[!NOTE]
   >
   > 确保填写要委托的 **完整** 子域。 例如，要委派“usoffers.email.weretail.com”子域，请键入“usoffers.email.weretail.com”。

   ![](assets/subdomain6.png)

1. 提交子域后，控制面板将执行各种操作来配置子域并检查其是否正确指向Campaign实例（命名空间记录创建、Campaign实例配置、Start of Authority记录验证等）。

   您可以随时单击按钮，获取有关配置进度的更多详细 **[!UICONTROL Process details]**信息。

   ![](assets/subdomain7.png)

您在流程的最后会得到什么？
* 具有以下DNS记录的子域- SOA、MX、CNAME、DKIM、SPF、TXT。
* 用于托管镜像、资源、跟踪页面和域密钥的其他子域
* 收件箱——发送者、错误、回复
* 最终，子域将配置为与您的Adobe Campaign实例一起使用
