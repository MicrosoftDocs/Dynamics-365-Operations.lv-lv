---
title: Vispārējā plānošana ģenerē fantoma precēm plānotos pasūtījumus
description: Plānotie pasūtījumi tiek ģenerēti fantoma precēm pēc tam, kad palaista vispārējā plānošana.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: anderso
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ea4bdb3729d163126234e02524cef331051cd48
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026718"
---
# <a name="master-planning-generates-planned-orders-for-phantom-products"></a><span data-ttu-id="90a0d-103">Vispārējā plānošana ģenerē fantoma precēm plānotos pasūtījumus</span><span class="sxs-lookup"><span data-stu-id="90a0d-103">Master planning generates planned orders for phantom products</span></span>

<span data-ttu-id="90a0d-104">KB numurs: 4614729</span><span class="sxs-lookup"><span data-stu-id="90a0d-104">KB number: 4614729</span></span>

## <a name="symptoms"></a><span data-ttu-id="90a0d-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="90a0d-105">Symptoms</span></span>

<span data-ttu-id="90a0d-106">Plānotie pasūtījumi tiek ģenerēti fantoma precēm pēc tam, kad palaista vispārējā plānošana.</span><span class="sxs-lookup"><span data-stu-id="90a0d-106">Planned orders are generated for phantom products after master planning is run.</span></span>

## <a name="resolution"></a><span data-ttu-id="90a0d-107">Novēršana</span><span class="sxs-lookup"><span data-stu-id="90a0d-107">Resolution</span></span>

<span data-ttu-id="90a0d-108">**Fantoma** opcijas iestatījums izlaistajām precēm nosaka noklusējuma rindas tipu materiālu komplektā (MK).</span><span class="sxs-lookup"><span data-stu-id="90a0d-108">The setting of the **Phantom** option for released products determines the default line type on the bill of material (BOM).</span></span> <span data-ttu-id="90a0d-109">Ja **Fantoma** opcija ir iestatīta uz *Jā*, sistēma joprojām izveidos plānotos pasūtījumus krājumam, bet **Tieši atvasinātās vajadzības** opcija katram plānotajam pasūtījumam tiks iestatīta uz *Jā*.</span><span class="sxs-lookup"><span data-stu-id="90a0d-109">When the **Phantom** option is set to *Yes*, the system will still create planned orders for the item, but the **Directly derived requirement** option for each planned order will be set to *Yes*.</span></span> <span data-ttu-id="90a0d-110">Tāpēc plānoto ražošanas pasūtījumu nevar apstiprināt atsevišķi.</span><span class="sxs-lookup"><span data-stu-id="90a0d-110">Therefore, the planned production order can't be firmed on its own.</span></span> <span data-ttu-id="90a0d-111">Tā vietā tas vienmēr tiks automātiski iekļauts, kad pamata ražošanas pasūtījums ir apstiprināts.</span><span class="sxs-lookup"><span data-stu-id="90a0d-111">Instead, it will always be automatically included when the parent production order is firmed.</span></span> <span data-ttu-id="90a0d-112">Turklāt plānotā fantoma pasūtījuma MK rindas tiek iekļautas pamata ražošanas pasūtījuma MK.</span><span class="sxs-lookup"><span data-stu-id="90a0d-112">Additionally, the BOM lines of the planned phantom order will be included in the BOM of the parent production order.</span></span>
