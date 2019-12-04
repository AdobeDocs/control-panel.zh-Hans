---
title: 关于SSL证书
description: 进一步了解SSL证书
translation-type: tm+mt
source-git-commit: ce93b595f4fbc2b3d72aadd034f93392565cb0e2

---


# 关于SSL证书 {#about-ssl-certificates}

Adobe Campaign建议您保护托管登录页面的子域，尤其是那些收集客户敏感信息的子域。

**SSL（安全套接字层）加密** ，可确保您委托给Adobe的子域是安全的。 当您的客户填写Web表单或访问由Adobe Campaign托管的登录页面时，默认情况下，信息会通过非安全协议(HTTP)发送。 要确保更多安全性，请使用HTTPS协议保护发送的信息。 例如，您的“http://info.mywebsite.com/”子域地址现在将为“https://info.mywebsite.com/”。

**委派的子域本身不安装SSL证书**。 它们安装在关联的子域上，主要是托管登录页面、资源页面和其他子域。

**SSL证书的提供期限为特定时间段** （1年、60天等）。 证书过期后，您可能会在访问登录页面或使用子域中的资源时遇到问题。 为避免这种情况，控制面板允许您监视子域的SSL证书，并启动其续订过程。

有关子域委托的更多详细信 [息](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html)。
