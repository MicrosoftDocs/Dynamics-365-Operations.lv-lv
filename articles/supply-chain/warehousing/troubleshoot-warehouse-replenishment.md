---
title: Noliktavas papildināšanas problēmu novēršana
description: Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar noliktavu papildināšanu programmā Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e4d87e85520c2b6f2346fddf3b985d4e17fe35cb
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644877"
---
# <a name="troubleshoot-warehouse-replenishment"></a><span data-ttu-id="199d3-103">Noliktavas papildināšanas problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="199d3-103">Troubleshoot warehouse replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="199d3-104">Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar noliktavu papildināšanu programmā Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="199d3-104">This topic describes how to fix common issues that you might encounter while you work with warehouse replenishment in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a><span data-ttu-id="199d3-105">Es saņemu sekojošu brīdinājuma ziņojumu: "Darbu %1 nevar atbloķēt, jo tam ir nepabeigts papildināšanas darbs."</span><span class="sxs-lookup"><span data-stu-id="199d3-105">I receive the following error message: "Work %1 cannot be unblocked because it has unfinished replenishment work."</span></span>

### <a name="issue-description"></a><span data-ttu-id="199d3-106">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="199d3-106">Issue description</span></span>

<span data-ttu-id="199d3-107">Izdošanas darbs ir bloķēts atkarīgā papildināšanas darba dēļ.</span><span class="sxs-lookup"><span data-stu-id="199d3-107">Picking work is blocked because of dependent replenishment work.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="199d3-108">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="199d3-108">Issue resolution</span></span>

<span data-ttu-id="199d3-109">Kad izmantojat kopuma pieprasījuma papildināšanu, ja izdošanas vieta ir jāpapildina, lai izpildītu avota pasūtījuma pieprasījumu, sistēma izveido gan papildināšanas darbu, gan izdošanas darbu.</span><span class="sxs-lookup"><span data-stu-id="199d3-109">When you use wave demand replenishment, if a picking location must be replenished to fulfill the source order demand, the system creates both the replenishment work and the picking work.</span></span> <span data-ttu-id="199d3-110">Tomēr tas bloķē izdošanas darbu, līdz papildināšanas darbs ir pabeigts.</span><span class="sxs-lookup"><span data-stu-id="199d3-110">However, it blocks the picking work until the replenishment work is completed.</span></span> <span data-ttu-id="199d3-111">Šī darbība ir tīša, jo izdošanas vietai nav pietiekami daudz krājumu, ja vien papildināšanas darbs nav pabeigts.</span><span class="sxs-lookup"><span data-stu-id="199d3-111">This behavior is intentional, because the picking location won't have enough inventory unless the replenishment work is completed.</span></span> <span data-ttu-id="199d3-112">Pabeidziet papildināšanas darbu un pēc tam apstrādājiet izdošanas darbu.</span><span class="sxs-lookup"><span data-stu-id="199d3-112">Complete the replenishment work, and then process the picking work.</span></span>
