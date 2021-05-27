---
title: Fiziski saņemtie pirkšanas pasūtījumi nav redzami krājumu slēgšanas pārskatā
description: Fiziski saņemtie pirkšanas pasūtījumi nav redzami Pārbaudīt atvērtos daudzumus krājumu slēgšanas pārskatā.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventOpenQtyCritical
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 9508d6d75d8ebee7ca10140ed4c4215d7ad1dda7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026711"
---
# <a name="physically-received-purchase-orders-dont-appear-on-the-inventory-closing-report"></a><span data-ttu-id="3fa7a-103">Fiziski saņemtie pirkšanas pasūtījumi nav redzami krājumu slēgšanas pārskatā</span><span class="sxs-lookup"><span data-stu-id="3fa7a-103">Physically received purchase orders don't appear on the inventory closing report</span></span>

<span data-ttu-id="3fa7a-104">KB numurs: 4612595</span><span class="sxs-lookup"><span data-stu-id="3fa7a-104">KB number: 4612595</span></span>

## <a name="symptoms"></a><span data-ttu-id="3fa7a-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="3fa7a-105">Symptoms</span></span>

<span data-ttu-id="3fa7a-106">Fiziski saņemtie pirkšanas pasūtījumi nav redzami **Pārbaudīt atvērtos daudzumus** krājumu slēgšanas pārskatā.</span><span class="sxs-lookup"><span data-stu-id="3fa7a-106">Physically received purchase orders don't appear on the **Check open quantities** inventory closing report.</span></span>

## <a name="resolution"></a><span data-ttu-id="3fa7a-107">Novēršana</span><span class="sxs-lookup"><span data-stu-id="3fa7a-107">Resolution</span></span>

<span data-ttu-id="3fa7a-108">Pārskatā **Pārbaudīt atvērtos daudzumus** ir norādītas izejas plūsmas darbības, kuras nevar nosegt ar finansiāli atjauninātajām krājumu ieejas plūsmām no atlasītā slēgšanas datuma.</span><span class="sxs-lookup"><span data-stu-id="3fa7a-108">The **Check open quantities** report shows issue transactions that can't be settled against financially updated inventory receipts as of the selected closing date.</span></span> <span data-ttu-id="3fa7a-109">Varat izvēlēties iekļaut pārskatā fiziskās ieejas plūsmas.</span><span class="sxs-lookup"><span data-stu-id="3fa7a-109">You can choose to include physical receipts on the report.</span></span> <span data-ttu-id="3fa7a-110">Tādā gadījumā fiziskas saņemšanas tiks rādītas, ja tās var segt izejas plūsmas darbības, ko nevar nosegt.</span><span class="sxs-lookup"><span data-stu-id="3fa7a-110">In that case, physical receipts will be shown if they can cover the issue transactions that can't be settled.</span></span> <span data-ttu-id="3fa7a-111">Papildinformāciju skatiet rakstā [Notiek gatavošanās krājumu slēgšanai](/dynamicsax-2012/appuser-itpro/preparing-to-run-inventory-close).</span><span class="sxs-lookup"><span data-stu-id="3fa7a-111">For more information, see [Preparing to run inventory close](/dynamicsax-2012/appuser-itpro/preparing-to-run-inventory-close).</span></span>
