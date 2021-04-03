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
ms.openlocfilehash: f9b5e4122fbd83ff76e0605b2f0816e10d2d9aab
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470837"
---
# <a name="production-planning"></a><span data-ttu-id="2ce49-103">Ražošanas plānošana</span><span class="sxs-lookup"><span data-stu-id="2ce49-103">Production planning</span></span>

<span data-ttu-id="2ce49-104">Optimizācijas plānošana atbalsta vairākus ražošanas scenārijus.</span><span class="sxs-lookup"><span data-stu-id="2ce49-104">Planning Optimizations supports several production scenarios.</span></span> <span data-ttu-id="2ce49-105">Ja migrēsiet no esošās iebūvētās vispārējās plānošanas programmas, ir svarīgi atcerēties kādu no mainītajiem scenārijiem.</span><span class="sxs-lookup"><span data-stu-id="2ce49-105">If you're migrating from the existing, built-in master planning engine, it's important that you be aware of some changed behavior.</span></span>

<span data-ttu-id="2ce49-106">Tālāk sniegtais video sniedz īsu ievadu dažiem šajā tēmā minētajiem koncepcijām: [Dynamics 365 Supply Chain Management: optimizācijas uzlabojumu plānošana](https://youtu.be/u1pcmZuZBTw).</span><span class="sxs-lookup"><span data-stu-id="2ce49-106">The following video gives a short introduction to some of the concepts discussed in this topic: [Dynamics 365 Supply Chain Management: Planning Optimization enhancements](https://youtu.be/u1pcmZuZBTw).</span></span>

## <a name="planned-production-orders"></a><span data-ttu-id="2ce49-107">Plānotie ražošanas pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="2ce49-107">Planned production orders</span></span>

<span data-ttu-id="2ce49-108">Kad vispārējā plānošana izveido plānotos pasūtījumus vajadzības izpildei, pasūtījuma tipu nosaka lauka **Plānotais pasūtījums** vērtība.</span><span class="sxs-lookup"><span data-stu-id="2ce49-108">When master planning creates planned orders to fulfill requirements, the order type is determined by the value of the **Planned order type** field.</span></span> <span data-ttu-id="2ce49-109">Ja **Plānotā pasūtījuma tips** ir iestatīts uz *Ražošana*, tiek izveidoti plānotie ražošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="2ce49-109">If the **Planned order type** field is set to *Production*, planned production orders are created.</span></span> <span data-ttu-id="2ce49-110">Šie plānotie ražošanas pasūtījumi ietver informāciju par aktīvo materiālu komplektu (MK) un maršruta ID no saistītā ražošanas iestatījuma.</span><span class="sxs-lookup"><span data-stu-id="2ce49-110">These planned production orders include information about the active bill of materials (BOM) and the route ID from the related production setup.</span></span>

## <a name="requirements-from-boms"></a><span data-ttu-id="2ce49-111">MK prasības</span><span class="sxs-lookup"><span data-stu-id="2ce49-111">Requirements from BOMs</span></span>

<span data-ttu-id="2ce49-112">MK informācija tiek izplāta vispārējās plānošanas laikā.</span><span class="sxs-lookup"><span data-stu-id="2ce49-112">BOM information is honored during master planning.</span></span> <span data-ttu-id="2ce49-113">Plāna izvade ietver materiālu piedāvājumu, lai segtu saistīto materiālu pieprasījumu ražošanai.</span><span class="sxs-lookup"><span data-stu-id="2ce49-113">The plan output includes material supply to cover related material demand for production.</span></span>

<span data-ttu-id="2ce49-114">Vispārējās plānošanas laikā pašreizējais aktīvais MK tiek izmantots, lai noteiktu ražošanai nepieciešamos materiālus.</span><span class="sxs-lookup"><span data-stu-id="2ce49-114">During master planning, the current, active BOM is used to determine the materials that are required for production.</span></span> <span data-ttu-id="2ce49-115">Šis solis tiek veikts caur visiem MK struktūras līmeņiem, kas saistīti ar pieprasīto ražošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="2ce49-115">This step is done through all levels of the BOM structure that is related to the required production order.</span></span> <span data-ttu-id="2ce49-116">Materiālu vajadzības tiek izpildītas, izmantojot pieejamos rīcībā esošos krājumus, esošos pasūtījuma piegādi un apstiprinātos plānotos pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="2ce49-116">Material requirement is fulfilled by using available on-hand inventory, existing on-order supply, and approved planned orders.</span></span> <span data-ttu-id="2ce49-117">Ja jebkurā vietā ir nepieciešami papildu materiāli, pieprasījuma segšanai tiek izveidots plānotais pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="2ce49-117">If additional material is required anywhere, a planned order is created to cover the demand.</span></span>

## <a name="scheduling-during-firming"></a><span data-ttu-id="2ce49-118">Plānošana apstiprināšanas laikā</span><span class="sxs-lookup"><span data-stu-id="2ce49-118">Scheduling during firming</span></span>

<span data-ttu-id="2ce49-119">Plānotie ražošanas pasūtījumi ietver maršruta ID, kas nepieciešams ražošanas plānošanai.</span><span class="sxs-lookup"><span data-stu-id="2ce49-119">Planned production orders include the route ID that is required for production scheduling.</span></span> <span data-ttu-id="2ce49-120">Tomēr plānošanas atbalsts plānotajiem pasūtījumiem tiek gaidīts plānošanas izpildes laikā.</span><span class="sxs-lookup"><span data-stu-id="2ce49-120">However, scheduling support during the planning run for planned orders is pending.</span></span> <span data-ttu-id="2ce49-121">Maršruta ID tiek lietots plānoto ražošanas pasūtījumu plānošanai apstiprināšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="2ce49-121">The route ID is used to schedule planned production orders during firming.</span></span> <span data-ttu-id="2ce49-122">Tāpēc plānoto ražošanas pasūtījumu izpildes laiks var atšķirties no izpildes laika saistītajos, apstiprinātos ražošanas pasūtījumos, kas tiek ģenerēti no tiem, kā aprakstīts šeit:</span><span class="sxs-lookup"><span data-stu-id="2ce49-122">Therefore, the lead time on planned production orders can differ from the lead time on related scheduled, firmed production orders that are generated from them, as described here:</span></span>

- <span data-ttu-id="2ce49-123">**Plānotais ražošanas pasūtījums** – izpildes laiks ir balstīts uz izlaistās preces statisko izpildes laiku.</span><span class="sxs-lookup"><span data-stu-id="2ce49-123">**Planned production order** – The lead time is based on the static lead time from the released product.</span></span>
- <span data-ttu-id="2ce49-124">**Apstiprināts ražošanas pasūtījums** – izpildes laiks ir balstīts uz plānošanu, kas izmanto maršruta informāciju un saistītos resursu ierobežojumus.</span><span class="sxs-lookup"><span data-stu-id="2ce49-124">**Firmed production order** – The lead time is based on scheduling that uses route information and related resource constraints.</span></span>

<span data-ttu-id="2ce49-125">Papildinformāciju par paredzamo līdzekļu pieejamību skatiet sadaļā [Plānošanas optimizācijas atbilstības analīze](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="2ce49-125">For more information about expected feature availability, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

<span data-ttu-id="2ce49-126">Ja ir atkarīga ražošanas funkcionalitāte, kas vēl nav pieejama optimizācijas plānošanai, varat turpināt izmantot iebūvēto vispārējās plānošanas programmu.</span><span class="sxs-lookup"><span data-stu-id="2ce49-126">If you depend on production functionality that isn't yet available for Planning Optimization, you can continue to use the built-in master planning engine.</span></span> <span data-ttu-id="2ce49-127">Izņēmumi nav nepieciešami.</span><span class="sxs-lookup"><span data-stu-id="2ce49-127">No exception is required.</span></span>

## <a name="delays"></a><span data-ttu-id="2ce49-128">Aizkaves</span><span class="sxs-lookup"><span data-stu-id="2ce49-128">Delays</span></span>

<span data-ttu-id="2ce49-129">Ja pieprasītā materiāla izpildes laiks ir ilgāks par laiku starp šodienas datumu un materiālu vajadzības datumu, pieprasītā materiāla plānotais pasūtījums un saistītais ražošanas pasūtījums tiks aizkavēts.</span><span class="sxs-lookup"><span data-stu-id="2ce49-129">If the lead time for required material is longer than the period between today's date and the material requirement date, the planned order for the required material and the related production order will be delayed.</span></span> <span data-ttu-id="2ce49-130">Plānotiem pasūtījumiem aizkave (dienās) tiek aprēķināta, pamatojoties uz izpildei nodotās preces izpildes laiku.</span><span class="sxs-lookup"><span data-stu-id="2ce49-130">For planned orders, the delay (in days) is calculated based on the lead time from the released product.</span></span> <span data-ttu-id="2ce49-131">Tad aizkavēšanās informācija tiek izplatīta caur visiem MK struktūras līmeņiem.</span><span class="sxs-lookup"><span data-stu-id="2ce49-131">The delay information is then propagated through all levels of the BOM structure.</span></span> <span data-ttu-id="2ce49-132">Tāpēc var izsekot atlikto izejmateriālu ietekmi visu veidu debitora pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="2ce49-132">Therefore, you can follow the impact of delayed raw material all the way to the customer sales order.</span></span>

## <a name="modifying-planned-orders"></a><span data-ttu-id="2ce49-133">Plānoto pasūtījumu uzturēšana</span><span class="sxs-lookup"><span data-stu-id="2ce49-133">Modifying planned orders</span></span>

<span data-ttu-id="2ce49-134">Kad jūs maināt informāciju plānotajā pasūtījumā, jūs saņemat šādu ziņojumu: "Ievērojiet, ka manuālo izmaiņu ietekme uz plānotajiem pasūtījumiem netiks atspoguļota pārējā plānā līdz nākamās vispārējās plānošanas palaišanai."</span><span class="sxs-lookup"><span data-stu-id="2ce49-134">When you change information on a planned order, you receive the following message: "Note that the impact of manual changes on planned orders won't be reflected in the rest of the plan until the next master planning run."</span></span>

<span data-ttu-id="2ce49-135">Ja vēlaties mainīt informāciju plānotajā pasūtījumā un redzēt ietekmi uz saistītajām materiālu vajadzībām, sekojiet šiem soļiem.</span><span class="sxs-lookup"><span data-stu-id="2ce49-135">If you want to change information on a planned order and see the impact on the related material requirements, follow these steps.</span></span>

1. <span data-ttu-id="2ce49-136">Atjauniniet plānoto pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="2ce49-136">Update the planned order.</span></span>
2. <span data-ttu-id="2ce49-137">Apstipriniet plānoto pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="2ce49-137">Approve the planned order.</span></span>
3. <span data-ttu-id="2ce49-138">Palaidiet vispārējo plānošanu.</span><span class="sxs-lookup"><span data-stu-id="2ce49-138">Run master planning.</span></span>

<span data-ttu-id="2ce49-139">Palaižot vispārējo plānošanu, nav jāizmanto filtri, ja iekļauti plānotie ražošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="2ce49-139">When you run master planning, you should not use filters if planned production orders are included.</span></span> <span data-ttu-id="2ce49-140">Papildinformāciju skatiet šīs tēmas turpinājumā esošajā sadaļā [Filters](#filters).</span><span class="sxs-lookup"><span data-stu-id="2ce49-140">For more information, see the [Filters](#filters) section later in this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="2ce49-141">Ja plānotā pasūtījuma piegādes datums tiek mainīts uz vēlāku datumu, pieprasījums var tikt piesaistīts jaunajam plānotajam pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="2ce49-141">If the delivery date of the planned order is changed to a later date, the demand might be pegged against a new planned order.</span></span> <span data-ttu-id="2ce49-142">Šī darbība notiek, kad jaunais piegādes datums izraisa piesaistītā pieprasījuma aizkavēšanos, bet atbilstīgi izpildes laika iestatījumiem aizkavēšanos var kavēt.</span><span class="sxs-lookup"><span data-stu-id="2ce49-142">This behavior occurs when the new supply date causes a delay for the pegged demand but, according to the lead time settings, the delay can be avoided.</span></span>

## <a name="explosion-page"></a><span data-ttu-id="2ce49-143">Izvēršanas lapa</span><span class="sxs-lookup"><span data-stu-id="2ce49-143">Explosion page</span></span>

<span data-ttu-id="2ce49-144">Jūs varat izmantot **Izvēršanas** lapu, lai analizētu pieprasījumu, kas nepieciešams noteiktam ražošanas pasūtījumam vai plānotam ražošanas pasūtījumam, saistītajam segumam un piesaistes informācijai.</span><span class="sxs-lookup"><span data-stu-id="2ce49-144">You can use the **Explosion** page to analyze the demand that is required for a specific production order or planned production order, the related coverage, and pegging information.</span></span> <span data-ttu-id="2ce49-145">Informācija par **Izvēršanas** lapu tiek atjaunināta vispārējās plānošanas laikā.</span><span class="sxs-lookup"><span data-stu-id="2ce49-145">Information on the **Explosion** page is updated during master planning.</span></span> <span data-ttu-id="2ce49-146">Informāciju nevar atjaunināt tieši no **Izvēršanas** lapas.</span><span class="sxs-lookup"><span data-stu-id="2ce49-146">You can't update the information directly from the **Explosion** page.</span></span>

## <a name="filters"></a><a name="filters"></a><span data-ttu-id="2ce49-147">Filtri</span><span class="sxs-lookup"><span data-stu-id="2ce49-147">Filters</span></span>

<span data-ttu-id="2ce49-148">Plānošanas scenārijos, kuros ietilpst ražošana, mēs iesakām izvairīties no filtrētām vispārējās plānošanas palaišanas.</span><span class="sxs-lookup"><span data-stu-id="2ce49-148">For planning scenarios that include production, we recommend that you avoid filtered master planning runs.</span></span> <span data-ttu-id="2ce49-149">Lai nodrošinātu, ka plānošanas optimizācijai ir informācija, kas ir nepieciešama pareizā rezultāta jāaprēķina, ir jāietver visas preces, kurām ir jebkādas saistības ar precēm visā plānotā pasūtījuma MK struktūrā.</span><span class="sxs-lookup"><span data-stu-id="2ce49-149">To ensure that Planning Optimization has the information that is required to calculate the correct result, you must include all products that have any relation to products in the whole BOM structure of the planned order.</span></span>

<span data-ttu-id="2ce49-150">Lai arī pakārtotie pakārtotie krājumi tiek automātiski noteikti un ietverti vispārējā plānošanā, kad tiek izmantota iebūvētā vispārējās plānošanas programma, plānošanas optimizācija neveic šo darbību.</span><span class="sxs-lookup"><span data-stu-id="2ce49-150">Although dependent child items are automatically detected and included in master planning runs when the built-in master planning engine is used, Planning Optimization doesn't perform this action.</span></span>

<span data-ttu-id="2ce49-151">Piemēram, ja viena produkta A MK struktūras skrūve tiek izmantota arī preces B ražošanai, tad visi produkti A un B preču MK struktūrā jāiekļauj filtrā.</span><span class="sxs-lookup"><span data-stu-id="2ce49-151">For example, if a single bolt from the BOM structure of product A is also used to produce product B, all products in the BOM structure of products A and B must be included in the filter.</span></span> <span data-ttu-id="2ce49-152">Tā kā tā var būt ļoti sarežģīta, lai nodrošinātu, ka visas preces ir daļa no filtra, ieteicams izvairīties no filtrētas vispārējās plānošanas, kad ir iesaistīti ražošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="2ce49-152">Because it can be very complex to ensure that all products are part of the filter, we recommend that you avoid filtered master planning runs when production orders are involved.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]