---
title: Nevar izrakstīt rēķinu uz klientu vērstam pārdošanas pasūtījumam
description: Pēc opcijas Grāmatot rēķinu automātiski iespējošanas vairs nevar izrakstīt rēķinu sākotnējam pārdošanas pasūtījumam un sākotnējam tiešās piegādes pirkšanas pasūtījumam.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ab18a2a1dec4b70c55a55637b087c6b11023aa40
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026707"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a><span data-ttu-id="c4a03-103">Nevar izrakstīt rēķinu uz klientu vērstam pārdošanas pasūtījumam</span><span class="sxs-lookup"><span data-stu-id="c4a03-103">You can't invoice a customer-facing sales order</span></span>

<span data-ttu-id="c4a03-104">KB numurs: 4611793</span><span class="sxs-lookup"><span data-stu-id="c4a03-104">KB number: 4611793</span></span>

## <a name="symptoms"></a><span data-ttu-id="c4a03-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="c4a03-105">Symptoms</span></span>

<span data-ttu-id="c4a03-106">Pēc opcijas **Grāmatot rēķinu automātiski** iespējošanas kreditora lapā **Starpuzņēmums** vairs nevar izrakstīt rēķinu sākotnējam pārdošanas pasūtījumam un sākotnējam tiešās piegādes pirkšanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="c4a03-106">You can no longer invoice the original sales order and the original direct delivery purchase order after you enable the **Post invoice automatically** option on the **Intercompany** page for a vendor.</span></span>

## <a name="resolution"></a><span data-ttu-id="c4a03-107">Novēršana</span><span class="sxs-lookup"><span data-stu-id="c4a03-107">Resolution</span></span>

<span data-ttu-id="c4a03-108">Starpuzņēmumu un tiešās piegādes pasūtījumu rēķinu sinhronizācijas darbību kontrolē un izpilda parametri, kas aprakstīti sadaļā [Parametru iestatīšana starpuzņēmumu pasūtījuma grāmatošanai](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).</span><span class="sxs-lookup"><span data-stu-id="c4a03-108">The synchronization behavior for intercompany and direct delivery order invoices is controlled and forced by the parameters that are described in [Set up parameters to post an intercompany order](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).</span></span>

<span data-ttu-id="c4a03-109">Pēc šo parametru iestatīšanas vispirms jāizraksta rēķins par starpuzņēmumu pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="c4a03-109">After you set those parameters, you must invoice the intercompany sales order first.</span></span> <span data-ttu-id="c4a03-110">Tad tiks sinhronizēti sākotnējie pārdošanas pasūtījumi un pirkšanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="c4a03-110">The original sales orders and purchase orders will then be synchronized.</span></span>
