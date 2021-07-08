---
title: Aizkavēšanās tolerance (negatīvās dienas)
description: Šajā tēmā ir sniegta informācija par aizkavēšanās tolerances aprēķināšanu un to, kā tā ietekmē plānotā pasūtījuma izveidi Plānošanas optimizācijā.
author: crytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 748e047e89747f2eabccc04a40c79bcb1e6f3dea
ms.sourcegitcommit: f21659f1c23bc2cd65bbe7fb7210910d5a8e1cb9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/24/2021
ms.locfileid: "6306467"
---
# <a name="delay-tolerance-negative-days"></a><span data-ttu-id="5b2fe-103">Aizkavēšanās tolerance (negatīvās dienas)</span><span class="sxs-lookup"><span data-stu-id="5b2fe-103">Delay tolerance (negative days)</span></span>

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="5b2fe-104">Aizkavēšanās tolerances funkcionalitāte ļauj Plānošanas optimizācijai ņemt vērā vērtību **Negatīvās dienas**, kas ir iestatīta vajadzību grupām.</span><span class="sxs-lookup"><span data-stu-id="5b2fe-104">The delay tolerance functionality enables Planning Optimization to consider the **Negative days** value that is set for coverage groups.</span></span> <span data-ttu-id="5b2fe-105">Tā tiek lietota, lai pagarinātu aizkavēšanās tolerances periodu, kas piemērots vispārējās plānošanas laikā.</span><span class="sxs-lookup"><span data-stu-id="5b2fe-105">It's used to extend the delay tolerance period that is applied during master planning.</span></span> <span data-ttu-id="5b2fe-106">Šādā veidā var izvairīties no jaunu piegādes pasūtījumu izveidošanas, ja esošā piegāde varēs segt pieprasījumu pēc nelielas kavēšanās.</span><span class="sxs-lookup"><span data-stu-id="5b2fe-106">In this way, you can avoid creating new supply orders if existing supply will be able to cover the demand after a short delay.</span></span> <span data-ttu-id="5b2fe-107">Funkcionalitātes mērķis ir noteikt, vai ir lietderīgi izveidot jaunu piegādes pasūtījumu attiecīgajam pieprasījumam.</span><span class="sxs-lookup"><span data-stu-id="5b2fe-107">The purpose of the functionality is to determine whether it makes sense to create a new supply order for a given demand.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="5b2fe-108">Līdzekļa ieslēgšana sistēmā</span><span class="sxs-lookup"><span data-stu-id="5b2fe-108">Turn on the feature in your system</span></span>

<span data-ttu-id="5b2fe-109">Lai padarītu aizkavēšanās tolerances funkcionalitāti pieejamu jūsu sistēmā, dodieties uz sadaļu [Līdzekļu pārvaldība](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) un ieslēdziet līdzekli *Negatīvās dienas Plānošanas optimizācijai*.</span><span class="sxs-lookup"><span data-stu-id="5b2fe-109">To make the delay tolerance functionality available in your system, go to [Feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Negative days for Planning Optimization* feature.</span></span>

## <a name="delay-tolerance-in-planning-optimization"></a><span data-ttu-id="5b2fe-110">Aizkavēšanās tolerance Plānošanas optimizācijā</span><span class="sxs-lookup"><span data-stu-id="5b2fe-110">Delay tolerance in Planning Optimization</span></span>

<span data-ttu-id="5b2fe-111">Aizkavēšanās tolerance norāda dienu skaitu, papildus izpildes laikam, kuru esat gatavs gaidīt, pirms pasūtāt jaunu papildināšanu, kad jau ir plānota esošā piegāde.</span><span class="sxs-lookup"><span data-stu-id="5b2fe-111">Delay tolerance represents the number of days beyond the lead time that you're willing to wait before you order new replenishment when existing supply is already planned.</span></span> <span data-ttu-id="5b2fe-112">Aizkavēšanās tolerance tiek definēta, izmantojot kalendārās dienas, nevis darba dienas.</span><span class="sxs-lookup"><span data-stu-id="5b2fe-112">Delay tolerance is defined by using calendar days, not business days.</span></span>

<span data-ttu-id="5b2fe-113">Vispārējās plānošanas laikā, kad sistēma aprēķina aizkavēšanās toleranci, tā ņem vērā iestatījumu **Negatīvās dienas**.</span><span class="sxs-lookup"><span data-stu-id="5b2fe-113">At the time of master planning, when the system calculates the delay tolerance, it considers the **Negative days** setting.</span></span> <span data-ttu-id="5b2fe-114">Vērtību **Negatīvās dienas** var iestātīt lapā **Vajadzības grupas** vai lapā **Krājumu vajadzība**.</span><span class="sxs-lookup"><span data-stu-id="5b2fe-114">You can set the **Negative days** value on either the **Coverage groups** page or the **Item coverage** page.</span></span>

<span data-ttu-id="5b2fe-115">Sistēma saista aizkavēšanās tolerances aprēķinu ar *agrāko papildināšanas datumu*, kas ir vienāds ar šodienas datumu plus izpildes laiku.</span><span class="sxs-lookup"><span data-stu-id="5b2fe-115">The system links the delay tolerance calculation to the *earliest replenishment date*, which equals today's date plus the lead time.</span></span> <span data-ttu-id="5b2fe-116">Aizkavēšanās tolerance tiek aprēķināta, izmantojot sekojošo formulu, kur *maks()* atrod lielāko no divām vērtībām:</span><span class="sxs-lookup"><span data-stu-id="5b2fe-116">The delay tolerance is calculated by using following formula, where *max()* finds the larger of two values:</span></span>

<span data-ttu-id="5b2fe-117">*maks(Agrākais papildināšanas datums, Pieprasījuma izpildes termiņš)* – *Pieprasījuma izpildes datums* + *Negatīvās dienas*</span><span class="sxs-lookup"><span data-stu-id="5b2fe-117">*max(Earliest replenishment date, Demand due date)* – *Demand due date* + *Negative days*</span></span>

<span data-ttu-id="5b2fe-118">Šī formula nodrošina, ka vispārējā plānošana neveido jaunus piegādes pasūtījumus, ja preces izpildes laikā ir pietiekami daudz piegādes.</span><span class="sxs-lookup"><span data-stu-id="5b2fe-118">This formula ensures that master planning doesn't create new supply orders when enough supply exists during the product lead time.</span></span>

> [!NOTE]
> <span data-ttu-id="5b2fe-119">Aizkavēšanās tolerances aprēķins Plānošanas optimizācijā vienmēr izmanto dinamisko negatīvo dienu aprēķinu no iebūvētās vispārējās plānošanas.</span><span class="sxs-lookup"><span data-stu-id="5b2fe-119">The delay tolerance calculation in Planning Optimization always uses the dynamic negative days calculation from built-in master planning.</span></span> <span data-ttu-id="5b2fe-120">Iestatījums **Izmantot dinamiskās negatīvās dienas** lapā **Vispārējās plānošanas parametri** neietekmē šo uzvedību.</span><span class="sxs-lookup"><span data-stu-id="5b2fe-120">The **Use dynamic negative days** setting on the **Master planning parameters** page has no effect on this behavior.</span></span>

<span data-ttu-id="5b2fe-121">Ja esošais piedāvājums ietver pieprasījuma aizkavi, kas ir mazāka par vai vienāda ar aprēķināto aizkavēšanās toleranci, Plānošanas optimizācija piesaista esošo piedāvājumu ar pieprasījumu.</span><span class="sxs-lookup"><span data-stu-id="5b2fe-121">If the existing supply implies a demand delay that is less than or equal to the calculated delay tolerance, Planning Optimization pegs existing supply with the demand.</span></span> <span data-ttu-id="5b2fe-122">Dažos gadījumos labāk ir novilcināt pieprasījumu, nevis panākt pārmērīgu piedāvājumu.</span><span class="sxs-lookup"><span data-stu-id="5b2fe-122">In some cases, it's better to delay the demand than to end up with oversupply.</span></span>

<span data-ttu-id="5b2fe-123">Tālāk minētās apakšsadaļas sniedz piemērus, kas parāda, kā aizkavēšanās tolerance ietekmē plānoto pasūtījumu izveidi Plānošanas optimizācijā.</span><span class="sxs-lookup"><span data-stu-id="5b2fe-123">The following subsections provide examples that show how delay tolerance affects the creation of planned orders in Planning Optimization.</span></span>

### <a name="example-1"></a><span data-ttu-id="5b2fe-124">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="5b2fe-124">Example 1</span></span>

<span data-ttu-id="5b2fe-125">Precei ir šāda konfigurācija:</span><span class="sxs-lookup"><span data-stu-id="5b2fe-125">A product has the following configuration:</span></span>

- <span data-ttu-id="5b2fe-126">**Izpildes laiks:** *10*</span><span class="sxs-lookup"><span data-stu-id="5b2fe-126">**Lead time:** *10*</span></span>
- <span data-ttu-id="5b2fe-127">**Negatīvās dienas:** *2*</span><span class="sxs-lookup"><span data-stu-id="5b2fe-127">**Negative days:** *2*</span></span>

<span data-ttu-id="5b2fe-128">Precei pastāv šādi piedāvājuma un pieprasījuma veidi:</span><span class="sxs-lookup"><span data-stu-id="5b2fe-128">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="5b2fe-129">**Šodienas pieprasījums:** pārdošanas pasūtījums ar daudzumu 10</span><span class="sxs-lookup"><span data-stu-id="5b2fe-129">**Demand for today:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="5b2fe-130">**Piegāde 12 dienās:** pirkšanas pasūtījums ar daudzumu 10</span><span class="sxs-lookup"><span data-stu-id="5b2fe-130">**Supply in 12 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="5b2fe-131">Esošā piegāde var segt pieprasījumu 12 dienu laikā, un šis periods ir vienāds ar aizkavēšanās toleranci.</span><span class="sxs-lookup"><span data-stu-id="5b2fe-131">Existing supply can cover the demand within 12 days, and that period equals the delay tolerance.</span></span> <span data-ttu-id="5b2fe-132">Tāpēc, kad tiek palaista vispārējā plānošana, plānotie pasūtījumi netiek izveidoti.</span><span class="sxs-lookup"><span data-stu-id="5b2fe-132">Therefore, when master planning runs, no planned orders are created.</span></span>

### <a name="example-2"></a><span data-ttu-id="5b2fe-133">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="5b2fe-133">Example 2</span></span>

<span data-ttu-id="5b2fe-134">Precei ir šāda konfigurācija:</span><span class="sxs-lookup"><span data-stu-id="5b2fe-134">A product has the following configuration:</span></span>

- <span data-ttu-id="5b2fe-135">**Izpildes laiks:** *10*</span><span class="sxs-lookup"><span data-stu-id="5b2fe-135">**Lead time:** *10*</span></span>
- <span data-ttu-id="5b2fe-136">**Negatīvās dienas:** *0*</span><span class="sxs-lookup"><span data-stu-id="5b2fe-136">**Negative days:** *0*</span></span>

<span data-ttu-id="5b2fe-137">Precei pastāv šādi piedāvājuma un pieprasījuma veidi:</span><span class="sxs-lookup"><span data-stu-id="5b2fe-137">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="5b2fe-138">**Šodienas pieprasījums:** pārdošanas pasūtījums ar daudzumu 10</span><span class="sxs-lookup"><span data-stu-id="5b2fe-138">**Demand for today:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="5b2fe-139">**Piegāde 12 dienās:** pirkšanas pasūtījums ar daudzumu 10</span><span class="sxs-lookup"><span data-stu-id="5b2fe-139">**Supply in 12 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="5b2fe-140">Esošais piedāvājums var segt pieprasījumu tikai pēc 12 dienām.</span><span class="sxs-lookup"><span data-stu-id="5b2fe-140">Existing supply can cover the demand only after 12 days.</span></span> <span data-ttu-id="5b2fe-141">Tomēr aizkavēšanās tolerance ir 10 dienas.</span><span class="sxs-lookup"><span data-stu-id="5b2fe-141">However, the delay tolerance is 10 days.</span></span> <span data-ttu-id="5b2fe-142">Tāpēc, kad tiek palaista vispārējā plānošana, tiek izveidots plānotais pasūtījums daudzumam 10.</span><span class="sxs-lookup"><span data-stu-id="5b2fe-142">Therefore, when master planning runs, a planned order for a quantity of 10 is created.</span></span>

### <a name="example-3"></a><span data-ttu-id="5b2fe-143">3. piemērs</span><span class="sxs-lookup"><span data-stu-id="5b2fe-143">Example 3</span></span>

<span data-ttu-id="5b2fe-144">Precei ir šāda konfigurācija:</span><span class="sxs-lookup"><span data-stu-id="5b2fe-144">A product has the following configuration:</span></span>

- <span data-ttu-id="5b2fe-145">**Izpildes laiks:** *10*</span><span class="sxs-lookup"><span data-stu-id="5b2fe-145">**Lead time:** *10*</span></span>
- <span data-ttu-id="5b2fe-146">**Negatīvās dienas:** *2*</span><span class="sxs-lookup"><span data-stu-id="5b2fe-146">**Negative days:** *2*</span></span>

<span data-ttu-id="5b2fe-147">Precei pastāv šādi piedāvājuma un pieprasījuma veidi:</span><span class="sxs-lookup"><span data-stu-id="5b2fe-147">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="5b2fe-148">**Pieprasījums 11 dienās:** pārdošanas pasūtījums ar daudzumu 10</span><span class="sxs-lookup"><span data-stu-id="5b2fe-148">**Demand in 11 days:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="5b2fe-149">**Piegāde 14 dienās:** pirkšanas pasūtījums ar daudzumu 10</span><span class="sxs-lookup"><span data-stu-id="5b2fe-149">**Supply in 14 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="5b2fe-150">Esošais piedāvājums var segt pieprasījumu tikai pēc trim dienām.</span><span class="sxs-lookup"><span data-stu-id="5b2fe-150">Existing supply can cover the demand only after three days.</span></span> <span data-ttu-id="5b2fe-151">Tomēr aizkavēšanās tolerance ir trīs dienas.</span><span class="sxs-lookup"><span data-stu-id="5b2fe-151">However, the delay tolerance is two days.</span></span> <span data-ttu-id="5b2fe-152">(Šajā gadījumā aizkavēšanās tolerance iekļauj tikai divas negatīvās dienas.</span><span class="sxs-lookup"><span data-stu-id="5b2fe-152">(In this case, the delay tolerance includes only the two negative days.</span></span> <span data-ttu-id="5b2fe-153">Pieprasījuma datums nav ietverts, jo tas ir pēc preces izpildes laika.) Tāpēc, kad tiek palaista vispārējā plānošana, tiek izveidots plānotais pasūtījums daudzumam 10.</span><span class="sxs-lookup"><span data-stu-id="5b2fe-153">The demand date isn't included because it's after the product lead time.) Therefore, when master planning runs, a planned order for a quantity of 10 is created.</span></span>
