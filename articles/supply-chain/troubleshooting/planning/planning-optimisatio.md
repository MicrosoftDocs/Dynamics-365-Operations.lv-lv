---
title: Plānotais pirkšanas pasūtījums tiek izveidots, ja pirkums pastāv negatīvo dienu laikā
description: Ja seguma kods ir Min/max, plānošanas optimizācija izveido plānotu pirkšanas pasūtījumu, ja pirkums ir negatīvo dienu laikā.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo,MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 826496c2de956ff949dd79ab8aa643053719bf75
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026717"
---
# <a name="planned-purchase-order-is-created-when-a-purchase-exists-within-negative-days"></a><span data-ttu-id="21870-103">Plānotais pirkšanas pasūtījums tiek izveidots, ja pirkums pastāv negatīvo dienu laikā</span><span class="sxs-lookup"><span data-stu-id="21870-103">Planned purchase order is created when a purchase exists within negative days</span></span>

<span data-ttu-id="21870-104">KB numurs: 4614298</span><span class="sxs-lookup"><span data-stu-id="21870-104">KB number: 4614298</span></span>

## <a name="symptoms"></a><span data-ttu-id="21870-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="21870-105">Symptoms</span></span>

<span data-ttu-id="21870-106">Ja seguma kods ir *Min/max*, plānošanas optimizācija izveido plānotu pirkšanas pasūtījumu, ja pirkums ir negatīvo dienu laikā.</span><span class="sxs-lookup"><span data-stu-id="21870-106">If the coverage code is *Min/max*, Planning Optimization creates a planned purchase order when a purchase exists within negative days.</span></span>

## <a name="resolution"></a><span data-ttu-id="21870-107">Novēršana</span><span class="sxs-lookup"><span data-stu-id="21870-107">Resolution</span></span>

<span data-ttu-id="21870-108">Plānošanas optimizācijas neatbalsta negatīvas dienas.</span><span class="sxs-lookup"><span data-stu-id="21870-108">Planning Optimization doesn't support negative days.</span></span> <span data-ttu-id="21870-109">Tomēr tā vienmēr nodrošina, ka plānotie pasūtījumi netiek plānoti izpildes laikā attiecībā pret pašreizējo datumu.</span><span class="sxs-lookup"><span data-stu-id="21870-109">However, it always ensures that planned orders won't be scheduled within the lead time relative to the current date.</span></span> <span data-ttu-id="21870-110">Piemēram, pirkšanas izpildes laiks ir 10 dienas, un pirkšanas pasūtījumu ir plānots saņemt astoņu dienu laikā no šodienas.</span><span class="sxs-lookup"><span data-stu-id="21870-110">For example, the purchase lead time is 10 days, and a purchase order is expected to arrive eight days from today.</span></span> <span data-ttu-id="21870-111">Šajā gadījumā pirkšanas pasūtījums tiks izmantots kā pieprasījuma piedāvājums, kas ir piecu dienu laikā no šodienas.</span><span class="sxs-lookup"><span data-stu-id="21870-111">In this case, the purchase order will be used as supply for demand that is five days from today.</span></span>

<span data-ttu-id="21870-112">Tāpēc ieteicams koriģēt izpildes laikus, lai segtu visus scenārijus (vai gandrīz visus).</span><span class="sxs-lookup"><span data-stu-id="21870-112">Therefore, we recommend that you adjust your lead times to cover all (or almost all) of your scenarios.</span></span>
