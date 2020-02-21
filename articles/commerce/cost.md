---
title: Izmaksu konfigurācija sadalīto pasūtījumu pārvaldībai (DOM)
description: Šajā tēmā ir aprakstīta Dynamics 365 Commerce izmaksu konfigurācijas sadalīto pasūtījumu pārvaldības (distributed order management — DOM) funkcionalitāte.
author: josaw1
manager: AnnBe
ms.date: 12/05/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-12-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7644cb9800a418fd123b32a0257b787277fcb19f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004232"
---
# <a name="cost-configuration-for-distributed-order-management-dom"></a><span data-ttu-id="17ed1-103">Izmaksu konfigurācija sadalīto pasūtījumu pārvaldībai (DOM)</span><span class="sxs-lookup"><span data-stu-id="17ed1-103">Cost configuration for distributed order management (DOM)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17ed1-104">Organizācijām ieteicams izmantot vairākus izmaksu komponentus, lai noteiktu optimālu pasūtījuma izpildes vietu.</span><span class="sxs-lookup"><span data-stu-id="17ed1-104">Organizations consider multiple cost components to determine the optimal location to fulfill an order from.</span></span> <span data-ttu-id="17ed1-105">Daži no šiem izmaksu komponentiem ir piegādes izmaksas, apstrādes izmaksas un iepakojuma izmaksas.</span><span class="sxs-lookup"><span data-stu-id="17ed1-105">Some of these cost components are shipping cost, handling cost, and packaging cost.</span></span> <span data-ttu-id="17ed1-106">Šo izmaksu kombinācija tiek aprēķināta tādēļ, lai noteiktu izpildes vietu.</span><span class="sxs-lookup"><span data-stu-id="17ed1-106">A combination of these costs is calculated to determine the fulfillment location.</span></span>

<span data-ttu-id="17ed1-107">Kad Dynamics 365 Commerce pirmā sadalīto pasūtījumu pārvaldības (DOM) iterācija optimizē izpildes vietām piešķirtos pasūtījumus, tiek ņemts vērā tikai attālums.</span><span class="sxs-lookup"><span data-stu-id="17ed1-107">When the first iteration of distributed order management (DOM) in Dynamics 365 Commerce optimized the assignment of orders to fulfillment locations, it factored in distance only.</span></span> <span data-ttu-id="17ed1-108">Lai gan attālums var tikt saistīts ar izmaksām, tas nav tas pats, kas izmaksas.</span><span class="sxs-lookup"><span data-stu-id="17ed1-108">Although distance can be correlated with cost, it isn't the same as cost.</span></span> <span data-ttu-id="17ed1-109">Piemēram, vienā attālumā piegādes pa nakti izmaksas ir lielākas nekā piegādes trīs vai septiņu dienu laikā.</span><span class="sxs-lookup"><span data-stu-id="17ed1-109">For example, an overnight shipping method costs more than three-day shipping or seven-day shipping over the same distance.</span></span>

<span data-ttu-id="17ed1-110">Izmantojot izmaksu konfigurācijas funkciju, mazumtirgotāji var definēt un konfigurēt papildu izmaksu komponentus, kas tiks aprēķināti un ņemti vērā, nosakot optimālo vietu pasūtījumu rindu izpildei.</span><span class="sxs-lookup"><span data-stu-id="17ed1-110">The cost configuration feature lets retailers define and configure additional cost components that will be calculated and factored in to determine the optimal location to fulfill order lines from.</span></span>

<span data-ttu-id="17ed1-111">Kad izmaksu komponenti ir konfigurēti, lai noteiktu optimālo vietu pasūtījuma izpildei, DOM risinātājs izmanto tikai šīs izmaksu definīcijas.</span><span class="sxs-lookup"><span data-stu-id="17ed1-111">When cost components are configured, the DOM solver uses only those cost definitions to determine the optimal location for order fulfillment.</span></span> <span data-ttu-id="17ed1-112">Attāluma komponents netiek uzskatīts par izmaksām.</span><span class="sxs-lookup"><span data-stu-id="17ed1-112">It doesn't consider the distance component as a cost.</span></span> <span data-ttu-id="17ed1-113">Tomēr, ja neviens izmaksu komponents nav konfigurēts, lai noteiktu optimālo vietu pasūtījuma izpildei, DOM risinātājs neizmanto attāluma komponentu kā izmaksas.</span><span class="sxs-lookup"><span data-stu-id="17ed1-113">However, if no cost components are configured, the DOM solver does use the distance component as a cost to determine the optimal location for order fulfillment.</span></span>

## <a name="set-up-cost-components"></a><span data-ttu-id="17ed1-114">Izmaksu komponentu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="17ed1-114">Set up cost components</span></span>

<span data-ttu-id="17ed1-115">Sistēmā var definēt divu veidu galvenos izmaksu komponentus: **Piegāde** un **Cits**.</span><span class="sxs-lookup"><span data-stu-id="17ed1-115">Two major cost component types can be defined in the system: **Shipping** and **Other**.</span></span>

<span data-ttu-id="17ed1-116">Abiem izmaksu komponentu veidiem tiek atbalstītas vairākas aprēķinu bāzes, kā parādīts tālāk sniegtajā tabulā.</span><span class="sxs-lookup"><span data-stu-id="17ed1-116">Both cost component types support multiple calculation bases, as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="17ed1-117">Izmaksu komponenta veids</span><span class="sxs-lookup"><span data-stu-id="17ed1-117">Cost component type</span></span></th>
<th><span data-ttu-id="17ed1-118">Aprēķina bāze</span><span class="sxs-lookup"><span data-stu-id="17ed1-118">Calculation basis</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="17ed1-119">Piegāde</span><span class="sxs-lookup"><span data-stu-id="17ed1-119">Shipping</span></span></td>
<td>
<ul>
<li><span data-ttu-id="17ed1-120">Vienkāršs</span><span class="sxs-lookup"><span data-stu-id="17ed1-120">Simple</span></span></li>
<li><span data-ttu-id="17ed1-121">Diferencēts</span><span class="sxs-lookup"><span data-stu-id="17ed1-121">Tiered</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="17ed1-122">Cits</span><span class="sxs-lookup"><span data-stu-id="17ed1-122">Other</span></span></td>
<td>
<ul>
<li><span data-ttu-id="17ed1-123">Pārdošanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="17ed1-123">Sales order</span></span></li>
<li><span data-ttu-id="17ed1-124">Pārdošanas rinda</span><span class="sxs-lookup"><span data-stu-id="17ed1-124">Sales line</span></span></li>
<li><span data-ttu-id="17ed1-125">Vieta</span><span class="sxs-lookup"><span data-stu-id="17ed1-125">Location</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="shipping-cost-component-type"></a><span data-ttu-id="17ed1-126">Piegādes izmaksu komponenta veids</span><span class="sxs-lookup"><span data-stu-id="17ed1-126">Shipping cost component type</span></span>

<span data-ttu-id="17ed1-127">Šajā sadaļā ir paskaidrots, kā iestatīt izmaksu komponenta veida **Piegāde** un piegādes izmaksu aprēķina bāzes kombinācijas.</span><span class="sxs-lookup"><span data-stu-id="17ed1-127">This section explains how to set up each combination of the **Shipping** cost component type and a calculation basis for shipping costs.</span></span> <span data-ttu-id="17ed1-128">Paskaidrots arī tas, kā DOM risinātājs izmanto katru kombināciju.</span><span class="sxs-lookup"><span data-stu-id="17ed1-128">It also explains how the DOM solver uses each combination.</span></span>

#### <a name="cost-component-type--shipping-and-calculation-basis--simple"></a><span data-ttu-id="17ed1-129">Izmaksu komponenta veids = Piegāde; Aprēķina bāze = Vienkārša</span><span class="sxs-lookup"><span data-stu-id="17ed1-129">Cost component type = Shipping and Calculation basis = Simple</span></span>

<span data-ttu-id="17ed1-130">Ja tiek izmantots izmaksu komponenta veids **Piegāde** un aprēķina bāze **Vienkārša**, piegādes veida izmaksas tiek noteiktas, ņemot vērā fiksētās izmaksas vai izmaksas atkarībā no attāluma.</span><span class="sxs-lookup"><span data-stu-id="17ed1-130">If a combination of the **Shipping** cost component type and the **Simple** calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</span></span>

<span data-ttu-id="17ed1-131">Šai kombinācijai ir jāiestata tālāk norādītie lauki.</span><span class="sxs-lookup"><span data-stu-id="17ed1-131">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="17ed1-132">**Izmaksu faktors** — ievadiet unikālu izmaksu faktora identifikatoru.</span><span class="sxs-lookup"><span data-stu-id="17ed1-132">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="17ed1-133">**Apraksts** — ievadiet izmaksu faktora nosaukumu un aprakstu.</span><span class="sxs-lookup"><span data-stu-id="17ed1-133">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="17ed1-134">**Sākuma datums** un **Beigu datums** — izmantojiet šos laukus, lai noteiktu izmaksu faktora derīguma termiņa datumu diapazonu.</span><span class="sxs-lookup"><span data-stu-id="17ed1-134">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="17ed1-135">Ja šos laukus atstāsit tukšus, izmaksu faktors būs derīgs neierobežotu periodu.</span><span class="sxs-lookup"><span data-stu-id="17ed1-135">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="17ed1-136">**Aktīvs** — norāda, vai izmaksu faktors ir aktīvs.</span><span class="sxs-lookup"><span data-stu-id="17ed1-136">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="17ed1-137">DOM ņem vērā tikai aktīvos izmaksu faktorus, kuri ir saistīti ar izpildes profilu.</span><span class="sxs-lookup"><span data-stu-id="17ed1-137">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="17ed1-138">**Uzņēmums** — norāda juridisku personu, kurai tiek konfigurēts izmaksu faktors.</span><span class="sxs-lookup"><span data-stu-id="17ed1-138">**Company** – Specify the legal entity that the cost factor is configured for.</span></span> <span data-ttu-id="17ed1-139">Visām aprēķina kritēriju rindām ir jānorāda viena un tā pati juridiskā persona.</span><span class="sxs-lookup"><span data-stu-id="17ed1-139">All lines of the calculation criteria must be for the same legal entity.</span></span>
- <span data-ttu-id="17ed1-140">**Piegādes veidi** — norāda piegādes veidus, kam izmaksas tiek konfigurētas.</span><span class="sxs-lookup"><span data-stu-id="17ed1-140">**Modes of delivery** – Specify the modes of delivery that the cost is configured for.</span></span>
- <span data-ttu-id="17ed1-141">**Aprēķina veids** — norāda, kā jāaprēķina konkrētā piegādes veida izmaksas.</span><span class="sxs-lookup"><span data-stu-id="17ed1-141">**Calculation type** – Specify how the cost should be calculated for a specific mode of delivery.</span></span> <span data-ttu-id="17ed1-142">Tiek atbalstīti divi tālāk norādītie aprēķinu veidi.</span><span class="sxs-lookup"><span data-stu-id="17ed1-142">Two calculation types are supported:</span></span>

    - <span data-ttu-id="17ed1-143">**Fiksēts** — piegādes veidam tiek izmantotas fiksētās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="17ed1-143">**Fixed** – A flat cost is used for the mode of delivery.</span></span> <span data-ttu-id="17ed1-144">Atlasot šo aprēķina veidu lauks **Izmaksas** tiek izmantots fiksēto izmaksu aprēķināšanai.</span><span class="sxs-lookup"><span data-stu-id="17ed1-144">If you select this calculation type, the **Cost** field defines the flat cost.</span></span>
    - <span data-ttu-id="17ed1-145">**Attāluma vienība** — piegādes veida izmaksas tiek aprēķinātas kā izmaksu vērtība, kas norādīta laukā **Izmaksas**, reizinot attālumu starp piegādes adresi un atrašanās vietām.</span><span class="sxs-lookup"><span data-stu-id="17ed1-145">**Per-distance unit** – The cost for the mode of delivery is calculated as the cost value that is specified in the **Cost** field times the distance between the delivery address and the locations.</span></span>

- <span data-ttu-id="17ed1-146">**Izmaksas** — norāda izmaksu vērtību, kas tiek izmantota kopā ar lauku **Aprēķina veids**, lai aprēķinātu piegādes veida izmaksas.</span><span class="sxs-lookup"><span data-stu-id="17ed1-146">**Cost** – Specify the cost value that is used in conjunction with the **Calculation type** field to compute the cost for a mode of delivery.</span></span>

#### <a name="cost-component-type--shipping-and-calculation-basis--tiered"></a><span data-ttu-id="17ed1-147">Izmaksu komponenta veids = Piegāde; Aprēķina bāze = Sadalīta</span><span class="sxs-lookup"><span data-stu-id="17ed1-147">Cost component type = Shipping and Calculation basis = Tiered</span></span>

<span data-ttu-id="17ed1-148">Ja tiek izmantots izmaksu komponenta veids **Piegāde** un aprēķina bāze **Sadalīta**, piegādes veida izmaksas tiek noteiktas, ņemot vērā fiksētās izmaksas vai izmaksas atkarībā no attāluma.</span><span class="sxs-lookup"><span data-stu-id="17ed1-148">If a combination of the **Shipping** cost component type and the **Tiered** calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</span></span> <span data-ttu-id="17ed1-149">Šajā kombinācijā attālums ir balstīts uz sadalītu attālumu diapazonu.</span><span class="sxs-lookup"><span data-stu-id="17ed1-149">However, in this combination, the distance is based on a tiered range of distances.</span></span>

<span data-ttu-id="17ed1-150">Šai kombinācijai ir jāiestata tālāk norādītie lauki.</span><span class="sxs-lookup"><span data-stu-id="17ed1-150">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="17ed1-151">**Izmaksu faktors** — ievadiet unikālu izmaksu faktora identifikatoru.</span><span class="sxs-lookup"><span data-stu-id="17ed1-151">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="17ed1-152">**Apraksts** — ievadiet izmaksu faktora nosaukumu un aprakstu.</span><span class="sxs-lookup"><span data-stu-id="17ed1-152">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="17ed1-153">**Noklusējuma izmaksas** — norāda izmaksas, kas jāizmanto piegādes veidam tad, ja attālums starp piegādes adresi un atrašanās vietu nav nevienā no piegādes veida sadalītajiem attālumiem.</span><span class="sxs-lookup"><span data-stu-id="17ed1-153">**Default cost** – Specify the cost that should be used for a mode of delivery if the distance between the delivery address and the location doesn't fall into any of the tiered distances for the mode of delivery.</span></span>
- <span data-ttu-id="17ed1-154">**Sākuma datums** un **Beigu datums** — izmantojiet šos laukus, lai noteiktu izmaksu faktora derīguma termiņa datumu diapazonu.</span><span class="sxs-lookup"><span data-stu-id="17ed1-154">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="17ed1-155">Ja šos laukus atstāsit tukšus, izmaksu faktors būs derīgs neierobežotu periodu.</span><span class="sxs-lookup"><span data-stu-id="17ed1-155">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="17ed1-156">**Aktīvs** — norāda, vai izmaksu faktors ir aktīvs.</span><span class="sxs-lookup"><span data-stu-id="17ed1-156">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="17ed1-157">DOM ņem vērā tikai aktīvos izmaksu faktorus, kuri ir saistīti ar izpildes profilu.</span><span class="sxs-lookup"><span data-stu-id="17ed1-157">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="17ed1-158">**Uzņēmums** — norāda juridisku personu, kurai tiek konfigurēts izmaksu faktors.</span><span class="sxs-lookup"><span data-stu-id="17ed1-158">**Company** – Specify the legal entity that the cost factor is configured for.</span></span> <span data-ttu-id="17ed1-159">Visām aprēķina kritēriju rindām ir jānorāda viena un tā pati juridiskā persona.</span><span class="sxs-lookup"><span data-stu-id="17ed1-159">All lines of the calculation criteria must be for the same legal entity.</span></span>
- <span data-ttu-id="17ed1-160">**Piegādes veidi** — norāda piegādes veidus, kam izmaksas tiek konfigurētas.</span><span class="sxs-lookup"><span data-stu-id="17ed1-160">**Modes of delivery** – Specify the modes of delivery that the cost is configured for.</span></span>
- <span data-ttu-id="17ed1-161">**Attāluma veids** — norāda, vai sadalītais attālums jāaprēķina kā antenas attālums vai ceļa attālums.</span><span class="sxs-lookup"><span data-stu-id="17ed1-161">**Distance type** – Specify whether the tiered distance definition is an aerial distance or a road distance.</span></span>
- <span data-ttu-id="17ed1-162">**Attāluma vienības** — norāda vienību, kas jāizmanto sadalītā attāluma aprēķināšanā.</span><span class="sxs-lookup"><span data-stu-id="17ed1-162">**Distance units** – Specify the unit that the tiered distance is measured in.</span></span>
- <span data-ttu-id="17ed1-163">**Attāluma sākums** — norāda sadalītā attāluma diapazona sākumu.</span><span class="sxs-lookup"><span data-stu-id="17ed1-163">**Distance from** – Specify the start range for the tiered distance.</span></span>
- <span data-ttu-id="17ed1-164">**Attāluma beigas** — norāda sadalītā attāluma diapazona beigas.</span><span class="sxs-lookup"><span data-stu-id="17ed1-164">**Distance to** – Specify the end range for the tiered distance.</span></span>
- <span data-ttu-id="17ed1-165">**Aprēķina veids** — norāda, kā jāaprēķina konkrētā piegādes veida izmaksas un sadalītais attālums.</span><span class="sxs-lookup"><span data-stu-id="17ed1-165">**Calculation type** – Specify how the cost should be calculated for a specific mode of delivery and tiered distance.</span></span> <span data-ttu-id="17ed1-166">Tiek atbalstīti divi tālāk norādītie aprēķinu veidi.</span><span class="sxs-lookup"><span data-stu-id="17ed1-166">Two calculation types are supported:</span></span>

    - <span data-ttu-id="17ed1-167">**Fiksēts** — piegādes veidam tiek izmantotas fiksētās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="17ed1-167">**Fixed** – A flat cost is used for the mode of delivery.</span></span> <span data-ttu-id="17ed1-168">Atlasot šo aprēķina veidu lauks **Izmaksas** tiek izmantots fiksēto izmaksu aprēķināšanai.</span><span class="sxs-lookup"><span data-stu-id="17ed1-168">If you select this calculation type, the **Cost** field defines the flat cost.</span></span>
    - <span data-ttu-id="17ed1-169">**Attāluma vienība** — piegādes veida un sadalītā attāluma izmaksas tiek aprēķinātas kā izmaksu vērtība, kas norādīta laukā **Izmaksas**, reizinot attālumu starp piegādes adresi un atrašanās vietām.</span><span class="sxs-lookup"><span data-stu-id="17ed1-169">**Per distance unit** – The cost for the mode of delivery and tiered distance is calculated as the cost value that is specified in the **Cost** field times the distance between the delivery address and the locations.</span></span>

- <span data-ttu-id="17ed1-170">**Izmaksas** — norāda izmaksu vērtību, kas tiek izmantota kopā ar lauku **Aprēķina veids**, lai aprēķinātu piegādes veida izmaksas.</span><span class="sxs-lookup"><span data-stu-id="17ed1-170">**Cost** – Specify the cost value that is used in conjunction with the **Calculation type** field to compute the cost for a mode of delivery.</span></span>

> [!NOTE]
> - <span data-ttu-id="17ed1-171">Definējot sadalītos attālumus, sistēma pārbauda, vai netrūkst kāda attāluma un vai nav tādu attālumu, kas pārklājas.</span><span class="sxs-lookup"><span data-stu-id="17ed1-171">When you define tiered distances, the system validates that there are no missing or overlapping distances.</span></span>
> - <span data-ttu-id="17ed1-172">Visiem sadalītajiem attālumiem piegādes veidam jāizmanto vienāds attāluma veids.</span><span class="sxs-lookup"><span data-stu-id="17ed1-172">The distance type that is used for a mode of delivery must be the same across all the tiered distances.</span></span>

### <a name="other-cost-component-type"></a><span data-ttu-id="17ed1-173">Cits izmaksu komponenta veids</span><span class="sxs-lookup"><span data-stu-id="17ed1-173">Other cost component type</span></span>

<span data-ttu-id="17ed1-174">Šajā sadaļā ir paskaidrots, kā iestatīt izmaksu komponenta veida **Cits** un cita ar piegādes izmaksām nesaistīta izmaksu veida kombinācijas.</span><span class="sxs-lookup"><span data-stu-id="17ed1-174">This section explains how to set up each combination of the **Other** cost component type and an other cost type for non-shipping costs.</span></span> <span data-ttu-id="17ed1-175">Paskaidrots arī tas, kā DOM risinātājs izmanto katru kombināciju.</span><span class="sxs-lookup"><span data-stu-id="17ed1-175">It also explains how the DOM solver uses each combination.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--sales-order"></a><span data-ttu-id="17ed1-176">Izmaksu komponenta veids = Cits; Cits izmaksu veids = Pārdošanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="17ed1-176">Cost component type = Other and Other cost type = Sales order</span></span>

<span data-ttu-id="17ed1-177">Izmaksu komponenta veida **Cits** un cita izmaksu veida **Pārdošanas pasūtījums** kombinācija tiek izmantota, lai pārdošanas pasūtījuma līmenī definētu ar piegādi nesaistītas izmaksas.</span><span class="sxs-lookup"><span data-stu-id="17ed1-177">A combination of the **Other** cost component type and the **Sales order** other cost type is used to define non-shipping costs at the sales order level.</span></span>

<span data-ttu-id="17ed1-178">Šai kombinācijai ir jāiestata tālāk norādītie lauki.</span><span class="sxs-lookup"><span data-stu-id="17ed1-178">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="17ed1-179">**Izmaksu faktors** — ievadiet unikālu izmaksu faktora identifikatoru.</span><span class="sxs-lookup"><span data-stu-id="17ed1-179">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="17ed1-180">**Apraksts** — ievadiet izmaksu faktora nosaukumu un aprakstu.</span><span class="sxs-lookup"><span data-stu-id="17ed1-180">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="17ed1-181">**Sākuma datums** un **Beigu datums** — izmantojiet šos laukus, lai noteiktu izmaksu faktora derīguma termiņa datumu diapazonu.</span><span class="sxs-lookup"><span data-stu-id="17ed1-181">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="17ed1-182">Ja šos laukus atstāsit tukšus, izmaksu faktors būs derīgs neierobežotu periodu.</span><span class="sxs-lookup"><span data-stu-id="17ed1-182">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="17ed1-183">**Aktīvs** — norāda, vai izmaksu faktors ir aktīvs.</span><span class="sxs-lookup"><span data-stu-id="17ed1-183">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="17ed1-184">DOM ņem vērā tikai aktīvos izmaksu faktorus, kuri ir saistīti ar izpildes profilu.</span><span class="sxs-lookup"><span data-stu-id="17ed1-184">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="17ed1-185">**Izmaksas** — pārdošanas pasūtījuma līmenī norāda ar piegādi nesaistīto izmaksu vērtību.</span><span class="sxs-lookup"><span data-stu-id="17ed1-185">**Cost** – Specify the cost value for a non-shipping cost at the sales order level.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--sales-line"></a><span data-ttu-id="17ed1-186">Izmaksu komponenta veids = Cits; Cits izmaksu veids = Pārdošanas rinda</span><span class="sxs-lookup"><span data-stu-id="17ed1-186">Cost component type = Other and Other cost type = Sales line</span></span>

<span data-ttu-id="17ed1-187">Izmaksu komponenta veida **Cits** un cita izmaksu veida **Pārdošanas rinda** kombinācija tiek izmantota, lai pārdošanas pasūtījuma rindas līmenī definētu ar piegādi nesaistītas izmaksas.</span><span class="sxs-lookup"><span data-stu-id="17ed1-187">A combination of the **Other** cost component type and the **Sales line** other cost type is used to define non-shipping costs at the sales order line level.</span></span>

<span data-ttu-id="17ed1-188">Šai kombinācijai ir jāiestata tālāk norādītie lauki.</span><span class="sxs-lookup"><span data-stu-id="17ed1-188">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="17ed1-189">**Izmaksu faktors** — ievadiet unikālu izmaksu faktora identifikatoru.</span><span class="sxs-lookup"><span data-stu-id="17ed1-189">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="17ed1-190">**Apraksts** — ievadiet izmaksu faktora nosaukumu un aprakstu.</span><span class="sxs-lookup"><span data-stu-id="17ed1-190">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="17ed1-191">**Sākuma datums** un **Beigu datums** — izmantojiet šos laukus, lai noteiktu izmaksu faktora derīguma termiņa datumu diapazonu.</span><span class="sxs-lookup"><span data-stu-id="17ed1-191">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="17ed1-192">Ja šos laukus atstāsit tukšus, izmaksu faktors būs derīgs neierobežotu periodu.</span><span class="sxs-lookup"><span data-stu-id="17ed1-192">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="17ed1-193">**Aktīvs** — norāda, vai izmaksu faktors ir aktīvs.</span><span class="sxs-lookup"><span data-stu-id="17ed1-193">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="17ed1-194">DOM ņem vērā tikai aktīvos izmaksu faktorus, kuri ir saistīti ar izpildes profilu.</span><span class="sxs-lookup"><span data-stu-id="17ed1-194">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="17ed1-195">**Izmaksas** — pārdošanas pasūtījuma rindas līmenī norāda ar piegādi nesaistīto izmaksu vērtību.</span><span class="sxs-lookup"><span data-stu-id="17ed1-195">**Cost** – Specify the cost value for a non-shipping cost at the sales order line level.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--location"></a><span data-ttu-id="17ed1-196">Izmaksu komponenta veids = Cits; Cits izmaksu veids = Vieta</span><span class="sxs-lookup"><span data-stu-id="17ed1-196">Cost component type = Other and Other cost type = Location</span></span>

<span data-ttu-id="17ed1-197">Izmaksu komponenta veida **Cits** un cita izmaksu veida **Vieta** kombinācija tiek izmantota, lai atsevišķai vietai vai vietu grupai definētu ar piegādes izmaksām nesaistītas izmaksas.</span><span class="sxs-lookup"><span data-stu-id="17ed1-197">A combination of the **Other** cost component type and the **Location** other cost type is used to define non-shipping costs for a group of locations or an individual location.</span></span>

<span data-ttu-id="17ed1-198">Šai kombinācijai ir jāiestata tālāk norādītie lauki.</span><span class="sxs-lookup"><span data-stu-id="17ed1-198">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="17ed1-199">**Izmaksu faktors** — ievadiet unikālu izmaksu faktora identifikatoru.</span><span class="sxs-lookup"><span data-stu-id="17ed1-199">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="17ed1-200">**Apraksts** — ievadiet izmaksu faktora nosaukumu un aprakstu.</span><span class="sxs-lookup"><span data-stu-id="17ed1-200">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="17ed1-201">**Sākuma datums** un **Beigu datums** — izmantojiet šos laukus, lai noteiktu izmaksu faktora derīguma termiņa datumu diapazonu.</span><span class="sxs-lookup"><span data-stu-id="17ed1-201">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="17ed1-202">Ja šos laukus atstāsit tukšus, izmaksu faktors būs derīgs neierobežotu periodu.</span><span class="sxs-lookup"><span data-stu-id="17ed1-202">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="17ed1-203">**Aktīvs** — norāda, vai izmaksu faktors ir aktīvs.</span><span class="sxs-lookup"><span data-stu-id="17ed1-203">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="17ed1-204">DOM ņem vērā tikai aktīvos izmaksu faktorus, kuri ir saistīti ar izpildes profilu.</span><span class="sxs-lookup"><span data-stu-id="17ed1-204">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="17ed1-205">**Izpildes vietu grupa** — norāda vietu grupu, kurai tiek definētas ar piegādi nesaistītās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="17ed1-205">**Fulfillment group** – Specify the group of locations that the non-shipping cost is defined for.</span></span>
- <span data-ttu-id="17ed1-206">**Izpildes vieta** — norāda vietu, kurai tiek definētas ar piegādi nesaistītās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="17ed1-206">**Fulfillment location** – Specify the location that the non-shipping cost is defined for.</span></span>

    > [!NOTE]
    > <span data-ttu-id="17ed1-207">Ja aprēķina kritērijos ir iestatīta atrašanās vieta, izpildes vietu un izpildes vietu grupu nevar norādīt vienā rindā.</span><span class="sxs-lookup"><span data-stu-id="17ed1-207">You can't specify a fulfillment group and a fulfillment location on the same line for location-based calculation criteria.</span></span>

- <span data-ttu-id="17ed1-208">**Izmaksas** — izpildes grupas vai izpildes vietas līmeņos norāda ar piegādi nesaistīto izmaksu vērtību.</span><span class="sxs-lookup"><span data-stu-id="17ed1-208">**Cost** – Specify the cost value for a non-shipping cost at the fulfillment group level or fulfillment location level.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="17ed1-209">Lai DOM palaišanas laikā šīs izmaksas tiktu ņemtas vērā, izmaksu faktors ir jāpievieno attiecīgajam izpildes profilam.</span><span class="sxs-lookup"><span data-stu-id="17ed1-209">For DOM to consider these costs when it's run, you must add the cost factor to the relevant fulfillment profile.</span></span>
