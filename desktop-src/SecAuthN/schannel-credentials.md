---
Description: Schannel protocols require credentials to authenticate servers and optionally, clients.
ms.assetid: 8f912af8-fd64-467a-b154-28c60cb14929
title: Schannel Credentials
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# Schannel Credentials

Schannel protocols require credentials to authenticate servers and optionally, clients. Server authentication, where the server provides proof of its identity to the client, is required by the Schannel [*security protocols*](https://www.bing.com/search?q=*security protocols*). Client authentication may be requested by the server at any time.

Schannel credentials are [*X.509*](https://www.bing.com/search?q=*X.509*) certificates. [*Public*](https://www.bing.com/search?q=*Public*) and [*private key*](https://www.bing.com/search?q=*private key*) information from certificates is used to authenticate the server and optionally, the client. These keys are also used to provide message [*integrity*](https://www.bing.com/search?q=*integrity*) while client and server exchange the information required to generate and exchange [*session keys*](https://www.bing.com/search?q=*session keys*).

For programming information, see [Obtaining Schannel Credentials](obtaining-schannel-credentials.md).

 

 


