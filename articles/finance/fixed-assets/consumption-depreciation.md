---
title: Patēriņa nolietojuma aprēķins
description: Šajā rakstā ir sniegts pārskats par nolietojuma patēriņa metodi.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13751
ms.assetid: d25a681f-49a5-4bfc-aa76-1c6373e35dd8
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2c9d95a7a45ed99c63516749285126c786685c87
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187318"
---
# <a name="consumption-depreciation"></a><span data-ttu-id="55d3a-103">Patēriņa nolietojuma aprēķins</span><span class="sxs-lookup"><span data-stu-id="55d3a-103">Consumption depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="55d3a-104">Šajā rakstā ir sniegts pārskats par nolietojuma patēriņa metodi.</span><span class="sxs-lookup"><span data-stu-id="55d3a-104">This article gives an overview of the Consumption method of depreciation.</span></span>

<span data-ttu-id="55d3a-105">Ja iestatāt nolietojuma tabulu pamatlīdzekļiem un atlasāt opciju **Patēriņš** laukā **Metode**, kurš atrodas lapā **Nolietojuma tabulas**, tad pamatlīdzekļi tiek piešķirti nolietojuma tabulai, pamatojoties uz to lietojumu.</span><span class="sxs-lookup"><span data-stu-id="55d3a-105">If you set up a depreciation profile for fixed assets and select **Consumption** in the **Method** field on the **Depreciation profiles** page, fixed assets are assigned to the depreciation profile based on their usage.</span></span> <span data-ttu-id="55d3a-106">Jums nav jāiestata procentuālais daudzums un intervāli lapā **Nolietojuma tabulas**.</span><span class="sxs-lookup"><span data-stu-id="55d3a-106">You don't have to set up percentages and intervals on the **Depreciation profiles** page.</span></span> <span data-ttu-id="55d3a-107">Kad ir izveidota nolietojuma tabula, kas izmanto metodi Patēriņš, šo metodi varat iestatīt dažādos veidos.</span><span class="sxs-lookup"><span data-stu-id="55d3a-107">After you create a depreciation profile that uses the Consumption method, you can set up the method in various ways.</span></span>

## <a name="set-up-and-use-consumption-depreciation"></a><span data-ttu-id="55d3a-108">Patēriņa nolietojuma iestatīšana un lietošana</span><span class="sxs-lookup"><span data-stu-id="55d3a-108">Set up and use consumption depreciation</span></span>
1.  <span data-ttu-id="55d3a-109">Lapā **Nolietojuma tabulas** izveidojiet nolietojuma tabulu.</span><span class="sxs-lookup"><span data-stu-id="55d3a-109">On the **Depreciation profiles** page, create the depreciation profile.</span></span> <span data-ttu-id="55d3a-110">Patēriņa aprēķināšanai nolietojuma tabulā ir jābūt iekļautam ID un nosaukumam, un ir jābūt atlasītam vienumam **Patēriņš** laukā **Metode**.</span><span class="sxs-lookup"><span data-stu-id="55d3a-110">For consumption calculations, the depreciation profile must have an ID and a name, and **Consumption** must be selected in the **Method** field.</span></span>
2.  <span data-ttu-id="55d3a-111">Lapā **Patēriņa koeficienti** iestatiet patēriņa koeficientus.</span><span class="sxs-lookup"><span data-stu-id="55d3a-111">On the **Consumption factors** page, set up consumption factors.</span></span> <span data-ttu-id="55d3a-112">Katram patēriņa koeficientam ir nepieciešams ID un nosaukums, kā arī patēriņa koeficients, kas ir norādīts kā daudzums vai kā procenti.</span><span class="sxs-lookup"><span data-stu-id="55d3a-112">Each consumption factor must have an ID and a name, and a consumption factor that is specified as either a quantity or a percentage.</span></span>
3.  <span data-ttu-id="55d3a-113">Lapā **Patēriņa vienības** iestatiet patēriņa vienības.</span><span class="sxs-lookup"><span data-stu-id="55d3a-113">On the **Consumption units** page, set up consumption units.</span></span> <span data-ttu-id="55d3a-114">Katrai patēriņa vienībai ir nepieciešams ID un nosaukums.</span><span class="sxs-lookup"><span data-stu-id="55d3a-114">Each consumption unit must have an ID and a name.</span></span> <span data-ttu-id="55d3a-115">Nolietojuma vienības tiek izmantotas, lai aprēķinātu patēriņa nolietojumu lapā **Patēriņa nolietojums**.</span><span class="sxs-lookup"><span data-stu-id="55d3a-115">Depreciation units are used to calculate consumption depreciation on the **Consumption depreciation** page.</span></span> <span data-ttu-id="55d3a-116">Vienību piemēri ir kilometrs (km), kilograms (kg) un stunda.</span><span class="sxs-lookup"><span data-stu-id="55d3a-116">Examples of units are kilometer (km), kilogram (kg), and hour.</span></span>
4.  <span data-ttu-id="55d3a-117">Lapā **Pamatlīdzekļi** iestatiet atsevišķus pamatlīdzekļus.</span><span class="sxs-lookup"><span data-stu-id="55d3a-117">On the **Fixed assets** page, set up individual fixed assets.</span></span> <span data-ttu-id="55d3a-118">Katram pamatlīdzeklim atlasiet vērtības modeļus un nolietojuma grāmatas, kurām ir nolietojuma tabulas.</span><span class="sxs-lookup"><span data-stu-id="55d3a-118">For each fixed asset, select value models and depreciation books that have depreciation profiles.</span></span> <span data-ttu-id="55d3a-119">Patēriņa nolietojumam jums ir jāiestata vērtības modeļi vai nolietojuma grāmatas, ja kādam no jūsu pamatlīdzekļiem tiek lietotas tādas nolietojuma tabulas, kas ir balstītas uz metodi Patēriņš.</span><span class="sxs-lookup"><span data-stu-id="55d3a-119">You must set up value models or depreciation books for consumption depreciation if any of your fixed assets use depreciation profiles that are based on the Consumption method.</span></span> <span data-ttu-id="55d3a-120">Šis iestatījums tiek veikts vai nu cilnē **Nolietojums**, lapā **Vērtības modeļi**, vai kopsavilkuma cilnē **Vispārīgi**, lapā **Nolietojuma tabula**.</span><span class="sxs-lookup"><span data-stu-id="55d3a-120">This setup is done either on the **Depreciation** tab of the **Value models** page or on the **General** FastTab of the **Depreciation profile** page.</span></span> <span data-ttu-id="55d3a-121">Vairākiem pamatlīdzekļiem varat izvēlēties vienu un to pašu vērtības modeli.</span><span class="sxs-lookup"><span data-stu-id="55d3a-121">You can use the same value model for multiple fixed assets.</span></span> <span data-ttu-id="55d3a-122">Nolietojuma tabulas ir katram pamatlīdzeklim atlasītā vērtības modeļa vai nolietojuma grāmatas daļa.</span><span class="sxs-lookup"><span data-stu-id="55d3a-122">Depreciation profiles are part of the value model or depreciation book that you select for each fixed asset.</span></span> <span data-ttu-id="55d3a-123">Nolietojuma tabulas nevar pievienot vai modificēt tieši lapā **Pamatlīdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="55d3a-123">You can't add or modify depreciation profiles directly on the **Fixed assets** page.</span></span> <span data-ttu-id="55d3a-124">Nolietojuma tabulas varat modificēt tikai lapā **Nolietojuma grāmatas**.</span><span class="sxs-lookup"><span data-stu-id="55d3a-124">You can modify depreciation profiles only on the **Depreciation books** page.</span></span>
5.  <span data-ttu-id="55d3a-125">Lapā **Vērtības modeļi** vai lapā **Nolietojuma grāmatas**, lauku grupā **Patēriņa nolietojums** ierakstiet informāciju tālāk uzskaitītajos laukos.</span><span class="sxs-lookup"><span data-stu-id="55d3a-125">On the **Value models** page or the **Depreciation books** page, in the **Consumption depreciation** field group, enter information in the following fields:</span></span>
    -   <span data-ttu-id="55d3a-126">Patēriņa koeficients</span><span class="sxs-lookup"><span data-stu-id="55d3a-126">Consumption factor</span></span>
    -   <span data-ttu-id="55d3a-127">Vienība</span><span class="sxs-lookup"><span data-stu-id="55d3a-127">Unit</span></span>
    -   <span data-ttu-id="55d3a-128">Vienības nolietojums</span><span class="sxs-lookup"><span data-stu-id="55d3a-128">Unit depreciation</span></span>
    -   <span data-ttu-id="55d3a-129">Aprēķinātais patēriņš</span><span class="sxs-lookup"><span data-stu-id="55d3a-129">Estimated consumption</span></span>

    <span data-ttu-id="55d3a-130">Laukā**Grāmatotais patēriņš** tiek rādīts patēriņa nolietojums tādās vienībās, kas jau ir grāmatotas pamatlīdzekļa un vērtības modeļa kombinācijai vai nolietojuma grāmatai.</span><span class="sxs-lookup"><span data-stu-id="55d3a-130">The **Posted consumption** field shows the consumption depreciation, in units, that has already been posted either for the combination of the fixed asset and value model, or for the depreciation book.</span></span> <span data-ttu-id="55d3a-131">Vērtību šajā laukā nevar manuāli atjaunināt.</span><span class="sxs-lookup"><span data-stu-id="55d3a-131">You can't manually update the value in this field.</span></span>

## <a name="examples"></a><span data-ttu-id="55d3a-132">Piemēri</span><span class="sxs-lookup"><span data-stu-id="55d3a-132">Examples</span></span>
### <a name="example-1"></a><span data-ttu-id="55d3a-133">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="55d3a-133">Example 1</span></span>

<span data-ttu-id="55d3a-134">Šāds patēriņa faktors ir iestatīts 31. janvārī:</span><span class="sxs-lookup"><span data-stu-id="55d3a-134">The following consumption factor is set up for January 31:</span></span>

-   <span data-ttu-id="55d3a-135">Daudzums ir 1000.</span><span class="sxs-lookup"><span data-stu-id="55d3a-135">The quantity is 1,000.</span></span>
-   <span data-ttu-id="55d3a-136">Pamatlīdzeklim norādītā vienības nolietojuma cena ir 1,5.</span><span class="sxs-lookup"><span data-stu-id="55d3a-136">The unit depreciation price that is specified for the fixed asset is 1.5.</span></span>

<span data-ttu-id="55d3a-137">Nolietojuma priekšlikums 31. janvārī ir šāds: Daudzums × Vienības nolietojums 1000 × 1,5 = 1500 Ja šim pamatlīdzeklim norādītais koeficients ir procentuāls koeficients, tad daudzums, kas tiek prognozēts laukā **Aprēķinātais patēriņš** attiecībā uz pamatlīdzekļa vērtības modeli, tiek reizināts ar procentiem, kuri ir iestatīti atlasītajam beigu datumam.</span><span class="sxs-lookup"><span data-stu-id="55d3a-137">The depreciation proposal on January 31 is as follows: Quantity × Unit depreciation 1,000 × 1.5 = 1,500 If the factor that is specified for the fixed asset is a percentage factor, the quantity that is estimated in the **Estimated consumption** field for the value model of the fixed asset is multiplied by the percentage that is set up for the selected end date.</span></span> <span data-ttu-id="55d3a-138">Pēc tam iegūtais daudzums tiek piedāvāts kā nolietojuma daudzums attiecīgajam periodam.</span><span class="sxs-lookup"><span data-stu-id="55d3a-138">The resulting quantity is then suggested as the depreciation quantity for the period.</span></span>

### <a name="example-2"></a><span data-ttu-id="55d3a-139">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="55d3a-139">Example 2</span></span>

<span data-ttu-id="55d3a-140">31 janvārim patēriņa nolietojumam tiek iestatīts tālāk norādītais patēriņa koeficients.</span><span class="sxs-lookup"><span data-stu-id="55d3a-140">The following factor for consumption depreciation is set up for January 31:</span></span>

-   <span data-ttu-id="55d3a-141">Procentuālais daudzums ir 10 procenti.</span><span class="sxs-lookup"><span data-stu-id="55d3a-141">The percentage is 10 percent.</span></span>
-   <span data-ttu-id="55d3a-142">Pamatlīdzeklim norādītā vienības nolietojuma cena ir 1,5.</span><span class="sxs-lookup"><span data-stu-id="55d3a-142">The unit depreciation price that is specified for the fixed asset is 1.5.</span></span>
-   <span data-ttu-id="55d3a-143">Pamatlīdzekļa novērtētais daudzums ir 2000.</span><span class="sxs-lookup"><span data-stu-id="55d3a-143">The estimated quantity of the fixed asset is 2,000.</span></span>

<span data-ttu-id="55d3a-144">Nolietojuma priekšlikums 31. janvārī ir šāds: Novērtētais daudzums × Procenti × Vienības nolietojums 2000 × 0,10 × 1,5 = 300</span><span class="sxs-lookup"><span data-stu-id="55d3a-144">The depreciation proposal on January 31 is as follows: Estimated quantity × Percentage × Unit depreciation 2,000 × .10 × 1.5 = 300</span></span>



