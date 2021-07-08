---
title: Atceltas produktu ieejas plūsmas neatjaunina darbības statusu uz Reģistrētas
description: Pēc produktu ieejas plūsmu atcelšanas saņemšanas kravā, sistēma automātiski atjaunina krājumu transakcijas statusu no Saņemts uz Pasūtīts.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c86457d50a7a9ac2a699a0e0a9c7bdf4cd7c67b
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294126"
---
# <a name="canceled-product-receipts-dont-update-transaction-status-to-registered"></a><span data-ttu-id="e9abd-103">Atceltas produktu ieejas plūsmas neatjaunina darbības statusu uz Reģistrētas</span><span class="sxs-lookup"><span data-stu-id="e9abd-103">Canceled product receipts don't update transaction status to Registered</span></span>

## <a name="symptoms"></a><span data-ttu-id="e9abd-104">Simptomi</span><span class="sxs-lookup"><span data-stu-id="e9abd-104">Symptoms</span></span>

<span data-ttu-id="e9abd-105">Pēc darbības **Atcelt produktu ieejas plūsmas** palaišanas ienākošā kravā, sistēma automātiski atjaunina krājumu transakciju statusu no *Saņemts* uz *Pasūtīts*.</span><span class="sxs-lookup"><span data-stu-id="e9abd-105">After you run the **Cancel product receipts** action on an inbound load, the system automatically updates the status of inventory transactions from *Received* to *Ordered*.</span></span>

## <a name="resolution"></a><span data-ttu-id="e9abd-106">Novēršana</span><span class="sxs-lookup"><span data-stu-id="e9abd-106">Resolution</span></span>

<span data-ttu-id="e9abd-107">Kad pavadzīmes ir atceltas izejošām kravām, krājumu darbību statuss paliek *Izdots*.</span><span class="sxs-lookup"><span data-stu-id="e9abd-107">When packing slips are canceled for outbound loads, the status of inventory transactions remains *Picked*.</span></span> <span data-ttu-id="e9abd-108">Tomēr, kad produktu ieejas plūsmas no ienākošās krāvas tiek atceltas, krājumu transakciju statuss netiek atjaunots uz *Reģistrēts*.</span><span class="sxs-lookup"><span data-stu-id="e9abd-108">However, when product receipts from an inbound load are canceled, the status of inventory transactions isn't restored to *Registered*.</span></span> <span data-ttu-id="e9abd-109">Tādēļ pēc tam, kad produktu ieejas plūsma no ienākošās kravas ir atcelta, noliktavas darbiniekam ir atkārtoti jāreģistrē kravu krājumu daudzumi.</span><span class="sxs-lookup"><span data-stu-id="e9abd-109">Therefore, after a product receipt from an inbound load is canceled, the warehouse worker must re-register item quantities for the loads.</span></span>

<span data-ttu-id="e9abd-110">Papildinformāciju skatiet sadaļā [Reģistrēt krājumu daudzumus, kas tiek saņemti ar ienākošo kravu](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).</span><span class="sxs-lookup"><span data-stu-id="e9abd-110">For more information, see [Register item quantities that arrive on an inbound load](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).</span></span>
