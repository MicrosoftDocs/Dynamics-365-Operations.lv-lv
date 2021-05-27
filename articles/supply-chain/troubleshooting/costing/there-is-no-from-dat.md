---
title: Krājumu cenu lapas cilnē Aktīvās cenas nav vērtības Sākuma datuma
description: Krājumu cenu lapas cilnē Aktīvās cenas nav vērtības Sākuma datuma.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dd13f6a3e5ce3c894e96f420358d337f2e43dba
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026726"
---
# <a name="there-is-no-from-date-value-on-the-active-prices-tab-of-the-item-price-page"></a><span data-ttu-id="de2f6-103">Krājumu cenu lapas cilnē Aktīvās cenas nav vērtības Sākuma datuma</span><span class="sxs-lookup"><span data-stu-id="de2f6-103">There is no From date value on the Active prices tab of the Item price page</span></span>

<span data-ttu-id="de2f6-104">KB numurs: 4613548</span><span class="sxs-lookup"><span data-stu-id="de2f6-104">KB number: 4613548</span></span>

## <a name="symptoms"></a><span data-ttu-id="de2f6-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="de2f6-105">Symptoms</span></span>

<span data-ttu-id="de2f6-106">**Krājumu cenu** lapas cilnē **Aktīvās cenas** nav vērtības **Sākuma datuma**.</span><span class="sxs-lookup"><span data-stu-id="de2f6-106">There is no **From date** value on the **Active prices** tab of the **Item price** page.</span></span>

## <a name="resolution"></a><span data-ttu-id="de2f6-107">Novēršana</span><span class="sxs-lookup"><span data-stu-id="de2f6-107">Resolution</span></span>

<span data-ttu-id="de2f6-108">**Sākuma datuma** vērtība (spēkā stāšanās datums), kas ir iestatīts uz gaidošo cenu, netiek pārvietots uz aktīvo cenu.</span><span class="sxs-lookup"><span data-stu-id="de2f6-108">The **From date** value (effective date) that is set on the pending price isn't transferred to the active price.</span></span>

<span data-ttu-id="de2f6-109">Kad krājuma izmaksu ieraksts tiek ievadīts pirmo reizi, tā statuss ir *Gaidošs* un tam ir plānotais spēkā stāšanās datums.</span><span class="sxs-lookup"><span data-stu-id="de2f6-109">When an item cost record is first entered, it has a status of *Pending* and an intended effective date.</span></span> <span data-ttu-id="de2f6-110">Kad aktivizējat krājuma izmaksu ierakstu, šis statuss tiek atjaunināts uz *Aktīvs* un spēka stāšanās datums tiek atjaunināts uz aktivizēšanas datumu.</span><span class="sxs-lookup"><span data-stu-id="de2f6-110">When you activate the item cost record, the status is updated to *Active*, and the effective date is updated to the activation date.</span></span> <span data-ttu-id="de2f6-111">Tāpēc aktīvās cenas aktivizēšanas datums vienmēr ir faktiskais aktivizēšanas datums.</span><span class="sxs-lookup"><span data-stu-id="de2f6-111">Therefore, the active price's activation date is always the actual date of the activation.</span></span>

<span data-ttu-id="de2f6-112">Papildinformāciju skatiet tēmā [Izmaksu versiju pārskats](../../cost-management/costing-versions.md).</span><span class="sxs-lookup"><span data-stu-id="de2f6-112">For more information, see [Costing versions overview](../../cost-management/costing-versions.md).</span></span>
