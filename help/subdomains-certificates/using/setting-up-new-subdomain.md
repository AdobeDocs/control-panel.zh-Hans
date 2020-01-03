---
title: 设置新子域
description: 了解如何为营销活动实例设置新的子域
translation-type: tm+mt
source-git-commit: 52f155bbbecec9edabc66cbc28756f9579b81f04

---


# 设置新子域 {#setting-up-subdomain}

>[!NOTE]
>
>控制面板的子域委派当前处于测试阶段，并且可能会频繁更新和修改，恕不另行通知。

## 完全子域委托 {#full-subdomain-delegation}

控制面板允许您将子域完全委派到Adobe Campaign。 为此，请执行以下步骤：

1. 在卡中， **[!UICONTROL Subdomains & Certificates]**选择所需的生产实例，然后单击**[!UICONTROL Setup new subdomain]**。

   ![](assets/subdomain1.png)

   >[!NOTE]
   >
   >子域委派仅适用于 **生产** 实例。

1. 单击 **[!UICONTROL Next]**以确认完整的委派方法。

   ![](assets/subdomain3.png)

   >[!NOTE]
   >
   >[CNAME](#use-cnames) 和自定义方法当前不受控制面板支持。

1. 在您的组织所使用的托管解决方案中创建所需的子域和命名空间。 为此，请复制并粘贴向导中显示的Adobe Nameserver信息。 有关如何在托管解决方案中创建子域的详细信息，请参阅教 [程视频](https://video.tv.adobe.com/v/30175?captions=chi_hans)。

   >[!CAUTION]
   >
   >配置命名空间时，请确保 **您永远不要将根子域委派到Adobe**。 否则，域将仅能与Adobe一起使用。 任何其他用途都不可能实现，例如向贵组织的员工发送内部电子邮件。

   ![](assets/subdomain4.png)

   请注意，如果未配置任何子域，您正在设置的子域将被视为主子 **域**。 收件箱（发送者、错误、回复地址）对于稍后在此子域上配置的所有子域将保持不变。

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

   >[!NOTE]
   >
   >在某些情况下，委托会完成，但子域可能无法成功验证。 子域将直接进入列表，其状 **[!UICONTROL Verified subdomains]**态和作业日**[!UICONTROL Unverified]** 志将提供有关错误的信息。 如果您在解决问题时遇到问题，请与客户服务部门联系。
   >
   >请注意，当子域委派运行时，通过控制面板的其他请求将输入队列并仅在子域委派完成后执行，以防止出现任何性能问题。

在流程结束时，子域将配置为与您的Adobe Campaign实例一起使用，并将创建以下元素：

* **具有以下** DNS记录的 **子域**:SOA、MX、CNAME、DKIM、SPF、TXT、
* **用于托管镜像** 、资源、跟踪页面和域密钥的其他子域、
* **收件箱**:发送者、错误、回复。

单击该按钮可获取有关子域的更多详细 **[!UICONTROL Subdomain Details]**信息。

![](assets/subdomain_details_general.png)

![](assets/subdomains_details_senderinfo.png)

>[!NOTE]
>
>除了处理阶段，Adobe还将通知可交付性团队有关新子域的信息，以便审核已创建的子域。 在子域被委派后，审核过程最长可能需要3天。
>
>执行的检查包括反馈循环和垃圾邮件投诉循环测试。 因此，我们建议在审计完成之前不要使用子域，因为这可能导致不良的子域声誉。

## CNAME的使用 {#use-cnames}

Adobe不建议使用CNAME进行子域委派，也不支持通过控制面板进行子域委派。 要使用此方法，请与Adobe客户关怀联系。
