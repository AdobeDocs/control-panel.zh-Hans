---
product: campaign
solution: Campaign
title: 监控关键联系人和事件
description: '了解如何在Adobe中识别实例和关键联系人中发生的事件。 '
feature: Control Panel
role: Architect
level: Intermediate
source-git-commit: da68420340ea8605f6e1347e86797c9e6a790ea6
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---

# 监控关键联系人和事件 {#keycontacts-events}

>[!CONTEXTUALHELP]
>id="cp_servicecalendar_serviceevents"
>title="服务日历"
>abstract="“关键联系人”部分列出了Adobe联系的人员，以便在您的实例中提出任何请求或提出问题。 在服务事件日历部分中，您可以识别选定实例的所有过去版本和即将发布的版本以及服务审阅。"

>[!IMPORTANT]
>
>服务日历在测试版中提供，如有频繁更新和修改，恕不另行通知。

确定在实例中计划的事件对于监控Campaign实例至关重要。

通过控制面板，您可以监控实例中发生的版本和服务审核，并Adobe访问任何请求或问题的关键联系人列表。

这些信息可从 **[!UICONTROL Service Calendar]** 卡片。

## 关键联系人 {#key-contacts}

的 **[!UICONTROL Key contacts]** 部分列出了在Adobe可联系的人员，以便您在实例中提出任何请求或提出问题。

>[!NOTE]
>
>此部分将仅显示托管服务帐户的信息。

![](assets/service-events-contacts.png)

主要联系人包括以下角色：

* **[!UICONTROL TAM]**:技术客户经理，
* **[!UICONTROL CSM]**:客户成功经理，
* **[!UICONTROL Deliverability]**:可交付性操作的联系人，
* **[!UICONTROL Transition Manager]**:Managed Services过渡管理器(仅限Managed Services帐户)、
* **[!UICONTROL On-boarding Specialist]**:分配给帐户的专家，可帮助您在船上Campaign Classic(仅限Managed Services帐户)。

## 事件 {#events}

的 **[!UICONTROL Service Event Calendar]** 部分显示选定实例的所有过去和即将发布的版本和服务审阅。

![](assets/service-events-calendar.png)

的 **[!UICONTROL Note]** 列提供有关每个版本状态的信息：

* **[!UICONTROL General availability]**:最新可用的稳定版本。
* **[!UICONTROL Limited availability]**:仅限按需部署。
* **[!UICONTROL Release candidate]**:工程部门已验证。 等待生产校样。
* **[!UICONTROL Pre release]**:提前提供以满足特定客户需求。
* **[!UICONTROL No longer available]**:该内部版本不存在主要问题，但提供了一个新内部版本，并进行了其他错误修复。 需要升级。
* **[!UICONTROL Deprecated]**:构建嵌入已知回归。
不再支持内部版本。 必须升级。

您可以为一个或多个即将发生的事件分配一个标记以跟踪它们。 要实现此目的，请单击事件名称旁边的椭圆按钮。

![](assets/service-events-flag.png)
