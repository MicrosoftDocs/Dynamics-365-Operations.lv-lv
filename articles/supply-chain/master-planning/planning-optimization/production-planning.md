---
title: Ražošanas plānošana
description: Šajā tēmā ir aprakstīta ražošanas plānošana un skaidrots, kā modificēt plānotos ražošanas pasūtījumus, izmantojot plānošanas optimizāciju.
author: ChristianRytt
manager: tfehr
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: eda22aa6f1e8d665d8ef390f24b247a76d4c2956
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992399"
---
# <a name="production-planning"></a><span data-ttu-id="e305c-103">Ražošanas plānošana</span><span class="sxs-lookup"><span data-stu-id="e305c-103">Production planning</span></span>

<span data-ttu-id="e305c-104">Optimizācijas plānošana atbalsta vairākus ražošanas scenārijus.</span><span class="sxs-lookup"><span data-stu-id="e305c-104">Planning Optimizations supports several production scenarios.</span></span> <span data-ttu-id="e305c-105">Ja migrēsiet no esošās iebūvētās vispārējās plānošanas programmas, ir svarīgi atcerēties kādu no mainītajiem scenārijiem.</span><span class="sxs-lookup"><span data-stu-id="e305c-105">If you're migrating from the existing, built-in master planning engine, it's important that you be aware of some changed behavior.</span></span>

<!-- The following video gives a short introduction to some of the current capabilities. 
KFM: Link to video for production functionality, coming soon... -->

## <a name="planned-production-orders"></a><span data-ttu-id="e305c-106">Plānotie ražošanas pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="e305c-106">Planned production orders</span></span>

<span data-ttu-id="e305c-107">Kad vispārējā plānošana izveido plānotos pasūtījumus vajadzības izpildei, pasūtījuma tipu nosaka lauka **Plānotais pasūtījums** vērtība.</span><span class="sxs-lookup"><span data-stu-id="e305c-107">When master planning creates planned orders to fulfill requirements, the order type is determined by the value of the **Planned order type** field.</span></span> <span data-ttu-id="e305c-108">Ja **Plānotā pasūtījuma tips** ir iestatīts uz *Ražošana*, tiek izveidoti plānotie ražošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="e305c-108">If the **Planned order type** field is set to *Production*, planned production orders are created.</span></span> <span data-ttu-id="e305c-109">Šie plānotie ražošanas pasūtījumi ietver informāciju par aktīvo materiālu komplektu (MK) un maršruta ID no saistītā ražošanas iestatījuma.</span><span class="sxs-lookup"><span data-stu-id="e305c-109">These planned production orders include information about the active bill of materials (BOM) and the route ID from the related production setup.</span></span>

## <a name="requirements-from-boms"></a><span data-ttu-id="e305c-110">MK prasības</span><span class="sxs-lookup"><span data-stu-id="e305c-110">Requirements from BOMs</span></span>

<span data-ttu-id="e305c-111">MK informācija tiek izplāta vispārējās plānošanas laikā.</span><span class="sxs-lookup"><span data-stu-id="e305c-111">BOM information is honored during master planning.</span></span> <span data-ttu-id="e305c-112">Plāna izvade ietver materiālu piedāvājumu, lai segtu saistīto materiālu pieprasījumu ražošanai.</span><span class="sxs-lookup"><span data-stu-id="e305c-112">The plan output includes material supply to cover related material demand for production.</span></span>

<span data-ttu-id="e305c-113">Vispārējās plānošanas laikā pašreizējais aktīvais MK tiek izmantots, lai noteiktu ražošanai nepieciešamos materiālus.</span><span class="sxs-lookup"><span data-stu-id="e305c-113">During master planning, the current, active BOM is used to determine the materials that are required for production.</span></span> <span data-ttu-id="e305c-114">Šis solis tiek veikts caur visiem MK struktūras līmeņiem, kas saistīti ar pieprasīto ražošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="e305c-114">This step is done through all levels of the BOM structure that is related to the required production order.</span></span> <span data-ttu-id="e305c-115">Materiālu vajadzības tiek izpildītas, izmantojot pieejamos rīcībā esošos krājumus, esošos pasūtījuma piegādi un apstiprinātos plānotos pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="e305c-115">Material requirement is fulfilled by using available on-hand inventory, existing on-order supply, and approved planned orders.</span></span> <span data-ttu-id="e305c-116">Ja jebkurā vietā ir nepieciešami papildu materiāli, pieprasījuma segšanai tiek izveidots plānotais pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="e305c-116">If additional material is required anywhere, a planned order is created to cover the demand.</span></span>

## <a name="scheduling-during-firming"></a><span data-ttu-id="e305c-117">Plānošana apstiprināšanas laikā</span><span class="sxs-lookup"><span data-stu-id="e305c-117">Scheduling during firming</span></span>

<span data-ttu-id="e305c-118">Plānotie ražošanas pasūtījumi ietver maršruta ID, kas nepieciešams ražošanas plānošanai.</span><span class="sxs-lookup"><span data-stu-id="e305c-118">Planned production orders include the route ID that is required for production scheduling.</span></span> <span data-ttu-id="e305c-119">Tomēr plānošanas atbalsts plānotajiem pasūtījumiem tiek gaidīts plānošanas izpildes laikā.</span><span class="sxs-lookup"><span data-stu-id="e305c-119">However, scheduling support during the planning run for planned orders is pending.</span></span> <span data-ttu-id="e305c-120">Maršruta ID tiek lietots plānoto ražošanas pasūtījumu plānošanai apstiprināšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="e305c-120">The route ID is used to schedule planned production orders during firming.</span></span> <span data-ttu-id="e305c-121">Tāpēc plānoto ražošanas pasūtījumu izpildes laiks var atšķirties no izpildes laika saistītajos, apstiprinātos ražošanas pasūtījumos, kas tiek ģenerēti no tiem, kā aprakstīts šeit:</span><span class="sxs-lookup"><span data-stu-id="e305c-121">Therefore, the lead time on planned production orders can differ from the lead time on related scheduled, firmed production orders that are generated from them, as described here:</span></span>

- <span data-ttu-id="e305c-122">**Plānotais ražošanas pasūtījums** – izpildes laiks ir balstīts uz izlaistās preces statisko izpildes laiku.</span><span class="sxs-lookup"><span data-stu-id="e305c-122">**Planned production order** – The lead time is based on the static lead time from the released product.</span></span>
- <span data-ttu-id="e305c-123">**Apstiprināts ražošanas pasūtījums** – izpildes laiks ir balstīts uz plānošanu, kas izmanto maršruta informāciju un saistītos resursu ierobežojumus.</span><span class="sxs-lookup"><span data-stu-id="e305c-123">**Firmed production order** – The lead time is based on scheduling that uses route information and related resource constraints.</span></span>

<span data-ttu-id="e305c-124">Papildinformāciju par paredzamo līdzekļu pieejamību skatiet sadaļā [Plānošanas optimizācijas atbilstības analīze](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e305c-124">For more information about expected feature availability, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

<span data-ttu-id="e305c-125">Ja ir atkarīga ražošanas funkcionalitāte, kas vēl nav pieejama optimizācijas plānošanai, varat turpināt izmantot iebūvēto vispārējās plānošanas programmu.</span><span class="sxs-lookup"><span data-stu-id="e305c-125">If you depend on production functionality that isn't yet available for Planning Optimization, you can continue to use the built-in master planning engine.</span></span> <span data-ttu-id="e305c-126">Izņēmumi nav nepieciešami.</span><span class="sxs-lookup"><span data-stu-id="e305c-126">No exception is required.</span></span>

## <a name="delays"></a><span data-ttu-id="e305c-127">Aizkaves</span><span class="sxs-lookup"><span data-stu-id="e305c-127">Delays</span></span>

<span data-ttu-id="e305c-128">Ja pieprasītā materiāla izpildes laiks ir ilgāks par laiku starp šodienas datumu un materiālu vajadzības datumu, pieprasītā materiāla plānotais pasūtījums un saistītais ražošanas pasūtījums tiks aizkavēts.</span><span class="sxs-lookup"><span data-stu-id="e305c-128">If the lead time for required material is longer than the period between today's date and the material requirement date, the planned order for the required material and the related production order will be delayed.</span></span> <span data-ttu-id="e305c-129">Plānotiem pasūtījumiem aizkave (dienās) tiek aprēķināta, pamatojoties uz izpildei nodotās preces izpildes laiku.</span><span class="sxs-lookup"><span data-stu-id="e305c-129">For planned orders, the delay (in days) is calculated based on the lead time from the released product.</span></span> <span data-ttu-id="e305c-130">Tad aizkavēšanās informācija tiek izplatīta caur visiem MK struktūras līmeņiem.</span><span class="sxs-lookup"><span data-stu-id="e305c-130">The delay information is then propagated through all levels of the BOM structure.</span></span> <span data-ttu-id="e305c-131">Tāpēc var izsekot atlikto izejmateriālu ietekmi visu veidu debitora pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="e305c-131">Therefore, you can follow the impact of delayed raw material all the way to the customer sales order.</span></span>

## <a name="modifying-planned-orders"></a><span data-ttu-id="e305c-132">Plānoto pasūtījumu uzturēšana</span><span class="sxs-lookup"><span data-stu-id="e305c-132">Modifying planned orders</span></span>

<span data-ttu-id="e305c-133">Kad jūs maināt informāciju plānotajā pasūtījumā, jūs saņemat šādu ziņojumu: "Ievērojiet, ka manuālo izmaiņu ietekme uz plānotajiem pasūtījumiem netiks atspoguļota pārējā plānā līdz nākamās vispārējās plānošanas palaišanai."</span><span class="sxs-lookup"><span data-stu-id="e305c-133">When you change information on a planned order, you receive the following message: "Note that the impact of manual changes on planned orders won't be reflected in the rest of the plan until the next master planning run."</span></span>

<span data-ttu-id="e305c-134">Ja vēlaties mainīt informāciju plānotajā pasūtījumā un redzēt ietekmi uz saistītajām materiālu vajadzībām, sekojiet šiem soļiem.</span><span class="sxs-lookup"><span data-stu-id="e305c-134">If you want to change information on a planned order and see the impact on the related material requirements, follow these steps.</span></span>

1. <span data-ttu-id="e305c-135">Atjauniniet plānoto pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="e305c-135">Update the planned order.</span></span>
2. <span data-ttu-id="e305c-136">Apstipriniet plānoto pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="e305c-136">Approve the planned order.</span></span>
3. <span data-ttu-id="e305c-137">Palaidiet vispārējo plānošanu.</span><span class="sxs-lookup"><span data-stu-id="e305c-137">Run master planning.</span></span>

<span data-ttu-id="e305c-138">Palaižot vispārējo plānošanu, nav jāizmanto filtri, ja iekļauti plānotie ražošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="e305c-138">When you run master planning, you should not use filters if planned production orders are included.</span></span> <span data-ttu-id="e305c-139">Papildinformāciju skatiet šīs tēmas turpinājumā esošajā sadaļā [Filters](#filters).</span><span class="sxs-lookup"><span data-stu-id="e305c-139">For more information, see the [Filters](#filters) section later in this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="e305c-140">Ja plānotā pasūtījuma piegādes datums tiek mainīts uz vēlāku datumu, pieprasījums var tikt piesaistīts jaunajam plānotajam pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="e305c-140">If the delivery date of the planned order is changed to a later date, the demand might be pegged against a new planned order.</span></span> <span data-ttu-id="e305c-141">Šī darbība notiek, kad jaunais piegādes datums izraisa piesaistītā pieprasījuma aizkavēšanos, bet atbilstīgi izpildes laika iestatījumiem aizkavēšanos var kavēt.</span><span class="sxs-lookup"><span data-stu-id="e305c-141">This behavior occurs when the new supply date causes a delay for the pegged demand but, according to the lead time settings, the delay can be avoided.</span></span>

## <a name="explosion-page"></a><span data-ttu-id="e305c-142">Izvēršanas lapa</span><span class="sxs-lookup"><span data-stu-id="e305c-142">Explosion page</span></span>

<span data-ttu-id="e305c-143">Jūs varat izmantot **Izvēršanas** lapu, lai analizētu pieprasījumu, kas nepieciešams noteiktam ražošanas pasūtījumam vai plānotam ražošanas pasūtījumam, saistītajam segumam un piesaistes informācijai.</span><span class="sxs-lookup"><span data-stu-id="e305c-143">You can use the **Explosion** page to analyze the demand that is required for a specific production order or planned production order, the related coverage, and pegging information.</span></span> <span data-ttu-id="e305c-144">Informācija par **Izvēršanas** lapu tiek atjaunināta vispārējās plānošanas laikā.</span><span class="sxs-lookup"><span data-stu-id="e305c-144">Information on the **Explosion** page is updated during master planning.</span></span> <span data-ttu-id="e305c-145">Informāciju nevar atjaunināt tieši no **Izvēršanas** lapas.</span><span class="sxs-lookup"><span data-stu-id="e305c-145">You can't update the information directly from the **Explosion** page.</span></span>

## <a name="filters"></a><a name="filters"></a><span data-ttu-id="e305c-146">Filtri</span><span class="sxs-lookup"><span data-stu-id="e305c-146">Filters</span></span>

<span data-ttu-id="e305c-147">Plānošanas scenārijos, kuros ietilpst ražošana, mēs iesakām izvairīties no filtrētām vispārējās plānošanas palaišanas.</span><span class="sxs-lookup"><span data-stu-id="e305c-147">For planning scenarios that include production, we recommend that you avoid filtered master planning runs.</span></span> <span data-ttu-id="e305c-148">Lai nodrošinātu, ka plānošanas optimizācijai ir informācija, kas ir nepieciešama pareizā rezultāta jāaprēķina, ir jāietver visas preces, kurām ir jebkādas saistības ar precēm visā plānotā pasūtījuma MK struktūrā.</span><span class="sxs-lookup"><span data-stu-id="e305c-148">To ensure that Planning Optimization has the information that is required to calculate the correct result, you must include all products that have any relation to products in the whole BOM structure of the planned order.</span></span>

<span data-ttu-id="e305c-149">Lai arī pakārtotie pakārtotie krājumi tiek automātiski noteikti un ietverti vispārējā plānošanā, kad tiek izmantota iebūvētā vispārējās plānošanas programma, plānošanas optimizācija neveic šo darbību.</span><span class="sxs-lookup"><span data-stu-id="e305c-149">Although dependent child items are automatically detected and included in master planning runs when the built-in master planning engine is used, Planning Optimization doesn't perform this action.</span></span>

<span data-ttu-id="e305c-150">Piemēram, ja viena produkta A MK struktūras skrūve tiek izmantota arī preces B ražošanai, tad visi produkti A un B preču MK struktūrā jāiekļauj filtrā.</span><span class="sxs-lookup"><span data-stu-id="e305c-150">For example, if a single bolt from the BOM structure of product A is also used to produce product B, all products in the BOM structure of products A and B must be included in the filter.</span></span> <span data-ttu-id="e305c-151">Tā kā tā var būt ļoti sarežģīta, lai nodrošinātu, ka visas preces ir daļa no filtra, ieteicams izvairīties no filtrētas vispārējās plānošanas, kad ir iesaistīti ražošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="e305c-151">Because it can be very complex to ensure that all products are part of the filter, we recommend that you avoid filtered master planning runs when production orders are involved.</span></span>
