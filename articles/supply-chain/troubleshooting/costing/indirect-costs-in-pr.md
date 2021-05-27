---
title: Procesa pārskata netiešās izmaksas ietver dzēstus ražošanas pasūtījumus
description: Netiešās izmaksas procesā pārskats sniedz informāciju par ražošanas pasūtījumiem, kas tika daļēji apstrādāti un vēlāk dzēsti.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdIndirectCostInProgress
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 707fa9bb30129c3656e10c6756dee770a7712e65
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026712"
---
# <a name="the-indirect-costs-in-process-report-includes-deleted-production-orders"></a><span data-ttu-id="2539f-103">Procesa pārskata netiešās izmaksas ietver dzēstus ražošanas pasūtījumus</span><span class="sxs-lookup"><span data-stu-id="2539f-103">The Indirect costs in process report includes deleted production orders</span></span>

<span data-ttu-id="2539f-104">KB numurs: 4612748</span><span class="sxs-lookup"><span data-stu-id="2539f-104">KB number: 4612748</span></span>

## <a name="symptoms"></a><span data-ttu-id="2539f-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="2539f-105">Symptoms</span></span>

<span data-ttu-id="2539f-106">**Netiešās izmaksas procesā** pārskats sniedz informāciju par ražošanas pasūtījumiem, kas tika daļēji apstrādāti un vēlāk dzēsti.</span><span class="sxs-lookup"><span data-stu-id="2539f-106">The **Indirect costs in process** report presents information about production orders that were partially processed and later deleted.</span></span>

## <a name="resolution"></a><span data-ttu-id="2539f-107">Novēršana</span><span class="sxs-lookup"><span data-stu-id="2539f-107">Resolution</span></span>

<span data-ttu-id="2539f-108">Atsaucot ražošanas pasūtījumu, tiek atsauktas arī visi šī ražošanas pasūtījuma darījumi.</span><span class="sxs-lookup"><span data-stu-id="2539f-108">When you reverse a production order, you also reverse all the transactions of that production order.</span></span> <span data-ttu-id="2539f-109">Dzēšot ražošanas pasūtījumu, apakšgrāmatas tabulās un virsgrāmatā saglabājas visi ar to saistītie darījumi.</span><span class="sxs-lookup"><span data-stu-id="2539f-109">When you delete the production order, the subledger tables and general ledger persist all transactions that are related to it.</span></span> <span data-ttu-id="2539f-110">Pārskati rādīs darījumus apakšgrāmatas tabulās.</span><span class="sxs-lookup"><span data-stu-id="2539f-110">The reports will show the transactions in the subledger tables.</span></span> <span data-ttu-id="2539f-111">Konkrētam ražošanas pasūtījumam neto vērtībai jābūt 0,00.</span><span class="sxs-lookup"><span data-stu-id="2539f-111">For the specific production order, the net value should be 0.00.</span></span>
