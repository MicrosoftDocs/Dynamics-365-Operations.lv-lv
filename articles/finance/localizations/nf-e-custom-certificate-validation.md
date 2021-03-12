---
title: NF‑e pielāgoto sertifikātu validācija
description: Šajā tēmā sniegta informācija par NF-e pielāgota sertifikāta iespējošanu un izmantošanu.
author: gionoder
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f13e8b8229bbd9e174e5bde7858a468048ba309b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990090"
---
# <a name="nf-e-custom-certificate-validation"></a><span data-ttu-id="0a5e4-103">NF‑e pielāgoto sertifikātu validācija</span><span class="sxs-lookup"><span data-stu-id="0a5e4-103">NF-e custom certificate validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a5e4-104">Ieslēdzot NF-e pielāgoto sertifikātu verifikācijas līdzekli, pielāgota validācija ļauj izveidot savienojumu ar tīmekļa pakalpojumiem.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-104">When you turn the NF-e custom certificate verification feature, custom validation allows a connection with the web services.</span></span> <span data-ttu-id="0a5e4-105">Šis savienojums ir nepieciešams, lai pārsūtītu NF-e un saņemtu autorizāciju no SEFAZ.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-105">This connection is required to transmit NF-e and receive authorization from SEFAZ.</span></span>

<span data-ttu-id="0a5e4-106">Rekvizītu **Servera autentifikācijas nolūks** no V5 sertifikāta izsniedz Brazīlijas maršruta sertificēšanas iestāde.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-106">The **Server authentication purpose** property from the certificate V5 is issued by the Brazilian Root Certificate Authority.</span></span> <span data-ttu-id="0a5e4-107">Šis rekvizīts ir izslēgts pēc noklusējuma, un tas ir jāiespējo manuāli.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-107">This property is turned off by default and must be manually enabled.</span></span> <span data-ttu-id="0a5e4-108">Dažos gadījumos automātiskais sertifikāta atjauninājums var pārslēgt šo rekvizītu uz kā vairs neiespējojamu.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-108">In some circumstances, the automatic certificate update can switch this property to no longer be enabled.</span></span> <span data-ttu-id="0a5e4-109">Ja tā notiek, TLS savienojums tiek ietekmēts, un tas vairs nav uzticams.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-109">If this happens, the TLS connection is affected and is no longer trusted.</span></span> <span data-ttu-id="0a5e4-110">Ir ietekmēta arī spēja izdot NF-e ražošanas vidēs Minasžeraisas (MG) un Paranas (PR) štatos.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-110">The ability to issue NF-e on production environments for states of Minas Gerais (MG) and Paraná (PR) states is also impacted.</span></span>

<span data-ttu-id="0a5e4-111">Šis atjauninājums pieļauj alternatīvu sertifikātu validācijas risinājumu, kas nozīmē, ka ir iespējams izveidot drošus sakarus.</span><span class="sxs-lookup"><span data-stu-id="0a5e4-111">This update allows for an alternative solution for certificate validation, which means that it’s possible to establish a secure communication.</span></span>


