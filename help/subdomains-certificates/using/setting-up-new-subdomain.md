---
title: 设置新子域
description: 了解如何为营销活动实例设置新的子域
translation-type: tm+mt
source-git-commit: c44f6800a0f7905fe9e5619388c7007f0af8f973

---


# 设置新子域 {#setting-up-subdomain}

>[!IMPORTANT]
>
>控制面板的子域委派将在1月底之前在测试版中可用，并且如有频繁更新和修改，恕不另行通知。

如果您对子域委托方法有任何疑问，请联系Adobe可交付性团队，或最终联系客户关怀以请求可交付性咨询。

## 完全子域委托 {#full-subdomain-delegation}

控制面板允许您将子域完全委派到Adobe Campaign。 为此，请按照以下步骤操作。

>[!NOTE]
>
>如果选定实例之前没有配置的子域，则委托给Adobe的第一个子域将成为该实例的主子域 **** ，您将无法在将来更改它。
>
>将使用主子域为其他子域创建反向DNS记录。 其他子域的回复和弹回地址将从主子域生成。

1. 在卡中， **[!UICONTROL Subdomains & Certificates]**选择所需的生产实例，然后单击**[!UICONTROL Setup new subdomain]**。

   ![](assets/subdomain1.png)

   >[!NOTE]
   >
   >子域委托仅可用于 **生产** 实例。

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

1. 提交子域后，控制面板将检查它是否正确指向Adobe NS记录，以及此子域不存在授权开始(SOA)记录。

1. 如果检查成功，控制面板将开始设置包含DNS记录、其他URL、收件箱等的子域。 单击该按钮可获取有关配置进度的更多详细 **[!UICONTROL Process details]**信息。

   ![](assets/subdomain7.png)

   >[!NOTE]
   >
   >在某些情况下，委托会完成，但子域可能无法成功验证。 子域将直接进入列表，其 **[!UICONTROL Verified subdomains]**状态和作**[!UICONTROL Unverified]** 业日志提供有关错误的信息。 如果您在解决问题时遇到问题，请与客户服务部门联系。
   >
   >请注意，当子域委派运行时，通过控制面板的其他请求将输入队列并仅在子域委派完成后执行，以防止出现任何性能问题。

在流程结束时，子域将配置为与您的Adobe Campaign实例一起使用，并将创建以下元素：

* **具有以下** DNS记录的 **子域**:SOA、MX、CNAME、DKIM、SPF、TXT、
* **用于托管镜像** 、资源、跟踪页面和域密钥的其他子域，
* **收件箱**:发送者、错误、回复。

>[!NOTE]
>
>默认情况下，控制面板中的“回复”收件箱配置为清除电子邮件且不可再查看。 如果要监视营销活动的“回复”收件箱，请勿使用此地址。


单击该按钮可获取有关子域的更多详细 **[!UICONTROL Subdomain Details]**信息。

![](assets/subdomain_details_general.png)

![](assets/subdomains_details_senderinfo.png)

>[!NOTE]
>
>除了处理阶段，Adobe还将通知可交付性团队有关新子域的信息，以便审核已创建的子域。 在子域被委派后，审核过程最长可能需要3天。
>
>执行的检查包括反馈循环和垃圾邮件投诉循环测试。 因此，我们建议在审计完成之前不要使用子域，因为这可能导致不良的子域信誉。

## CNAME的使用 {#use-cnames}

控制面板不支持使用CNAME进行子域委派。 要使用此方法，请与Adobe客户关怀联系。
