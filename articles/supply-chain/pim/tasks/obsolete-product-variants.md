---
title: Novecojušu preces variantu atrašana
description: Šajā procedūrā ir parādīts, kā atrast novecojušas izlaistās preces vai preces variantus un kā preces dzīves cikla stāvokli saistīt ar novecojušām precēm.
author: cvocph
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 807297a87a7f0e59023d80fbd371bffbf2b086bd
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807996"
---
# <a name="find-obsolete-product-variants"></a><span data-ttu-id="45bc2-103">Novecojušu preces variantu atrašana</span><span class="sxs-lookup"><span data-stu-id="45bc2-103">Find obsolete product variants</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="45bc2-104">Šajā procedūrā ir parādīts, kā atrast novecojušas izlaistās preces vai preces variantus un kā preces dzīves cikla stāvokli saistīt ar novecojušām precēm.</span><span class="sxs-lookup"><span data-stu-id="45bc2-104">This procedure shows how to find obsolete released products or product variants and how to associate a product lifecycle state to the obsolete products.</span></span> <span data-ttu-id="45bc2-105">Priekšnosacījums: pirms šī uzdevuma ceļveža atskaņošanas ir jādefinē vismaz viens preces dzīves cikla stāvoklis, kas ir neaktīvs plānošanai.</span><span class="sxs-lookup"><span data-stu-id="45bc2-105">Prerequisite: You need to define at least one product lifecycle state that is inactive for planning before you can play this task guide.</span></span>


## <a name="run-a-simulation"></a><span data-ttu-id="45bc2-106">Simulācijas izpilde</span><span class="sxs-lookup"><span data-stu-id="45bc2-106">Run a simulation</span></span>
1. <span data-ttu-id="45bc2-107">Dodieties uz Preču informācijas pārvaldība > Periodiskie uzdevumi > Mainīt dzīves cikla stāvokli novecojušām precēm.</span><span class="sxs-lookup"><span data-stu-id="45bc2-107">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
2. <span data-ttu-id="45bc2-108">Laukā Jauns preces dzīves cikla stāvoklis ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="45bc2-108">In the New product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="45bc2-109">Atlasiet Jā laukā Palaist simulāciju bez preču datu atjaunināšanas.</span><span class="sxs-lookup"><span data-stu-id="45bc2-109">Select Yes in the Run simulation without updating product data field.</span></span>
4. <span data-ttu-id="45bc2-110">Ievadiet skaitli laukā Izslēgt preces, kas izveidotas šādā dienu skaita diapazonā.</span><span class="sxs-lookup"><span data-stu-id="45bc2-110">In the Exclude products created within this number of days field, enter a number.</span></span>
5. <span data-ttu-id="45bc2-111">Ievadiet skaitli laukā Izslēgt transakcijās lietotās preces (dienu skaitā).</span><span class="sxs-lookup"><span data-stu-id="45bc2-111">In the Exclude products used in transactions (in number of days) field, enter a number.</span></span>
6. <span data-ttu-id="45bc2-112">Izvērsiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="45bc2-112">Expand the Records to include section.</span></span>
7. <span data-ttu-id="45bc2-113">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="45bc2-113">Click Filter.</span></span>
8. <span data-ttu-id="45bc2-114">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="45bc2-114">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="45bc2-115">Laukā Kritēriji ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="45bc2-115">In the Criteria field, type a value.</span></span>
10. <span data-ttu-id="45bc2-116">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="45bc2-116">Click OK.</span></span>
11. <span data-ttu-id="45bc2-117">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="45bc2-117">Click OK.</span></span>

> [!NOTE]
> <span data-ttu-id="45bc2-118">Ieteicams izpildīt simulāciju partijā, ja ir paredzama liela preču skaita meklēšana.</span><span class="sxs-lookup"><span data-stu-id="45bc2-118">It is recommended to run the simulation in batch if you expect to search a large number of products.</span></span> <span data-ttu-id="45bc2-119">Turklāt pārliecinieties, ka simulācija netiek palaista uzņēmuma aktīvākajā darba laikā.</span><span class="sxs-lookup"><span data-stu-id="45bc2-119">Also, make sure that the simulation is not run during the most active working time of the company.</span></span>  

## <a name="review-the-simulation-results"></a><span data-ttu-id="45bc2-120">Simulācijas rezultātu skatīšana</span><span class="sxs-lookup"><span data-stu-id="45bc2-120">Review the simulation results</span></span>
1. <span data-ttu-id="45bc2-121">Dodieties uz Preču informācijas pārvaldība > Pieprasījumi un pārskati > Preču dzīves cikla stāvokļa uzturēšanas vēsture.</span><span class="sxs-lookup"><span data-stu-id="45bc2-121">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>
   
> [!NOTE]
> <span data-ttu-id="45bc2-122">Šajā lapā varat apskatīt simulācijas rezultātus un novērtēt, cik preču un preces variantu tiks saistīti ar jaunu preces dzīves cikla stāvokli, izpildot atjauninājumu bez simulācijas.</span><span class="sxs-lookup"><span data-stu-id="45bc2-122">On this page, you can review the simulation results and make an assessment of how many products and product variants will be associated with a new product lifecycle state when running the update without simulation.</span></span>  

## <a name="run-the-update-of-the-product-lifecycle-state-for-obsolete-products"></a><span data-ttu-id="45bc2-123">Palaidiet atjaunināšanas procesu preces dzīves cikla stāvoklim novecojušām precēm</span><span class="sxs-lookup"><span data-stu-id="45bc2-123">Run the update of the Product lifecycle state for obsolete products</span></span>
1. <span data-ttu-id="45bc2-124">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="45bc2-124">Close the page.</span></span>
2. <span data-ttu-id="45bc2-125">Dodieties uz Preču informācijas pārvaldība > Periodiskie uzdevumi > Mainīt dzīves cikla stāvokli novecojušām precēm.</span><span class="sxs-lookup"><span data-stu-id="45bc2-125">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
3. <span data-ttu-id="45bc2-126">Izvērsiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="45bc2-126">Expand the Records to include section.</span></span>

> [!NOTE]
> <span data-ttu-id="45bc2-127">Ņemiet vērā, ka ir saglabāta pēdējā atlase.</span><span class="sxs-lookup"><span data-stu-id="45bc2-127">Note that the last selection has been saved.</span></span>  

4. <span data-ttu-id="45bc2-128">Atlasiet Nē laukā Palaist simulāciju bez preču datu atjaunināšanas.</span><span class="sxs-lookup"><span data-stu-id="45bc2-128">Select No in the Run simulation without updating product data field.</span></span>
5. <span data-ttu-id="45bc2-129">Izvērsiet sadaļu Palaist fonā.</span><span class="sxs-lookup"><span data-stu-id="45bc2-129">Expand the Run in the background section.</span></span>

> [!NOTE]
> <span data-ttu-id="45bc2-130">Atkarībā no tā, cik daudz preču un preces variantu ir ietekmēti, apsveriet iespēju palaist šo darbu kā pakešuzdevumu.</span><span class="sxs-lookup"><span data-stu-id="45bc2-130">Depending on how many products and product variants are affected, consider running this job in batch.</span></span> <span data-ttu-id="45bc2-131">Pārliecinieties, ka liels atjaunināšanas darbs netiek palaists uzņēmuma aktīvākajā darba laikā.</span><span class="sxs-lookup"><span data-stu-id="45bc2-131">Make sure that you are not running a large update job during the most active working hours in the company.</span></span>  

6. <span data-ttu-id="45bc2-132">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="45bc2-132">Click OK.</span></span>
7. <span data-ttu-id="45bc2-133">Dodieties uz Preču informācijas pārvaldība > Pieprasījumi un pārskati > Preču dzīves cikla stāvokļa uzturēšanas vēsture.</span><span class="sxs-lookup"><span data-stu-id="45bc2-133">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>

> [!NOTE]
> <span data-ttu-id="45bc2-134">Apskatiet mainītās izlaistās preces un preču variantus.</span><span class="sxs-lookup"><span data-stu-id="45bc2-134">Review the changed released products and product variants.</span></span>  

8. <span data-ttu-id="45bc2-135">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="45bc2-135">In the list, find and select the desired record.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]