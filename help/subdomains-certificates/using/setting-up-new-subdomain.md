---
title: 设置新子域
description: 了解如何为活动实例设置新子域
translation-type: ht
source-git-commit: 47b4c6abd7b41a63d881b658849ac985c72656f8
workflow-type: ht
source-wordcount: '932'
ht-degree: 100%

---


# 设置新子域 {#setting-up-subdomain}

>[!CONTEXTUALHELP]
>id="cp_subdomain_management"
>title="设置新子域并管理证书"
>abstract="您需要设置一个新子域并管理子域的 SSL 证书，以开始使用 Adobe Campaign 发送电子邮件或发布登陆页面。"
>additional-url="https://docs.adobe.com/content/help/zh-Hans/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html" text="如何监控子域的 SSL 证书"

>[!IMPORTANT]
>
>测试版中提供控制面板的子域委派，如有频繁更新和修改，恕不另行通知。

## 完全子域委派 {#full-subdomain-delegation}

控制面板允许您将子域完全委派给 Adobe Campaign。为此，请执行以下步骤：

>[!NOTE]
>
>如果所选实例没有以前配置的子域，则委派给 Adobe 的第一个子域将成为该实例的&#x200B;**主子域**，之后您将无法进行更改。
>
>将使用主子域为其他子域创建反转 DNS 记录。其他子域的回复地址和退回地址将从主子域生成。

1. 在 **[!UICONTROL Subdomains & Certificates]**&#x200B;卡中，选择所需的生产实例，然后单击 **[!UICONTROL Setup new subdomain]**。

   ![](assets/subdomain1.png)

   >[!NOTE]
   >
   >子域委派仅可用于&#x200B;**生产**&#x200B;实例。

1. 单击 **[!UICONTROL Next]**&#x200B;以确认完整委派方法。

   ![](assets/subdomain3.png)

   >[!NOTE]
   >
   >控制面板当前不支持 [CNAME](#use-cnames) 和自定义方法。

1. 在您的组织使用的托管解决方案中创建所需的子域和名称服务器。为此，请复制并粘贴向导中显示的 Adobe 名称服务器信息。有关如何在托管解决方案中创建子域的详细信息，请参阅[教程视频](https://video.tv.adobe.com/v/30175?captions=chi_hans)。

   >[!IMPORTANT]
   >
   >配置名称服务器时，请确保&#x200B;**从不将根子域委派给 Adobe**。否则，域将仅能与 Adobe 配合使用。任何其他用途都不可能实现，例如向组织的员工发送内部电子邮件。
   >
   >此外，**不要为此新子域创建单独的区域文件**。

   ![](assets/subdomain4.png)

   在使用相应的 Adobe 名称服务器信息创建子域后，单击 **[!UICONTROL Next]**。

1. 为子域选择所需的用例：

   * **营销通信**：表示用于商业目的的通信。示例：销售电子邮件营销活动。
   * **交易和运营通信**：表示交易通信包含旨在完成收件人已开始的流程的信息。示例：购买确认、密码重置电子邮件。组织通信涉及在组织内外交流信息、想法和观点，不带商业目的。
   ![](assets/subdomain5.png)

   **根据用例划分子域是实现交付性的最佳实践**。这样，每个子域的信誉将被隔离和受保护。例如，如果营销通信的子域最终被互联网服务提供商列入黑名单，您的交易通信子域将不受影响，并且将能够继续发送通信。

   **您可以为营销和交易用例委派子域**：

   * 对于营销用例，子域将配置在 **MID**（中间采购）实例上。
   * 对于交易用例，子域将配置在所有 **RT**（消息中心/实时消息递送）实例上，以确保连接性。因此，子域将与您的所有 RT 实例一起运行。
   >[!NOTE]
   >
   >如果您使用 Campaign Classic，控制面板将允许您查看哪些 RT/MID 实例已连接到您正在使用的营销实例。如需详细信息，请参阅[此部分](../../instances-settings/using/instance-details.md)。

1. 输入您在托管解决方案中创建的子域，然后单击 **[!UICONTROL Submit]**。

   确保填写要委派的子域的&#x200B;**全名**。例如，要委派“usoffers.email.weretail.com”子域，请键入“usoffers.email.weretail.com”。

   ![](assets/subdomain6.png)

1. 提交子域后，控制面板将检查它是否正确指向 Adobe NS 记录，以及此子域不存在“授权开始”(SOA) 记录。

1. 如果检查成功，控制面板将开始设置包含 DNS 记录、其他 URL、收件箱等的子域。您可以通过单击 **[!UICONTROL Process details]**&#x200B;按钮获取有关配置进度的更多详细信息。

   ![](assets/subdomain7.png)

   >[!NOTE]
   >
   >在某些情况下，委派会完成，但子域可能无法成功验证。子域将直接进入 **[!UICONTROL Verified subdomains]**&#x200B;列表，其中包含&#x200B;**[!UICONTROL Unverified]** 状态和提供错误信息的作业日志。如果您在解决此问题时遇到麻烦，请联系客户关怀团队。
   >
   >请注意，当子域委派运行时，通过控制面板的其他请求将输入队列并仅在子域委派完成后执行，以防止出现任何性能问题。

在流程结束时，子域将配置为与 Adobe Campaign 实例配合使用，并将创建以下元素：

* **具有以下** DNS 记录的&#x200B;**子域**：SOA、MX、CNAME、DKIM、SPF、TXT；
* 用于托管镜像、资源、跟踪页面和域密钥的&#x200B;**其他子域**；
* **收件箱**：发件人、错误、回复。

>[!NOTE]
>
>默认情况下，控制面板中的“回复”收件箱配置为清除电子邮件且不可查看。如果要监控营销活动的“回复”收件箱，请勿使用此地址。

您可以通过单击 **[!UICONTROL Subdomain details]**&#x200B;和 **[!UICONTROL Sender info]** 按钮获取有关子域的更多详细信息。

![](assets/detail_buttons.png)

![](assets/subdomain_details.png)

![](assets/sender_info.png)

>[!IMPORTANT]
>
>在处理阶段后，您应与 Adobe 客户关怀团队确认已向可交付性团队提出审核请求，以审核已创建的新子域。委派子域后，审核过程最长可能需要 3 至 10 个工作日。
>
>执行的检查包括反馈循环和垃圾邮件投诉循环测试。因此，我们不建议在审核完成之前使用子域，因为它可能导致子域声誉受损。

## 使用 CNAME {#use-cnames}

控制面板不支持使用 CNAME 进行子域委派。要使用此方法，请与 Adobe 客户关怀团队联系。

**相关主题：**

* [委派子域（教程视频）](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/subdomain-delegation.html)
* [子域品牌化](../../subdomains-certificates/using/subdomains-branding.md)
* [监控子域](../../subdomains-certificates/using/monitoring-subdomains.md)