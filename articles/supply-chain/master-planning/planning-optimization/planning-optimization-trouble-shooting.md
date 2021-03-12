---
title: Plānošanas optimizācijas problēmu novēršana
description: Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar plānošanas optimizāciju.
author: ChristianRytt
manager: tfehr
ms.date: 05/07/2020
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
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 8e67a6faf52b51264555b06f56b289d19ca580d6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992574"
---
# <a name="troubleshoot-planning-optimization"></a><span data-ttu-id="45288-103">Plānošanas optimizācijas problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="45288-103">Troubleshoot Planning Optimization</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="45288-104">Šajā tēmā ir aprakstīts, kā labot tipiskas problēmas, kas var rasties, strādājot ar plānošanas optimizāciju.</span><span class="sxs-lookup"><span data-stu-id="45288-104">This topic describes how to fix common issues that you might encounter while working with Planning Optimization.</span></span>

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a><span data-ttu-id="45288-105">Plānošanas optimizācijas pievienojumprogrammas instalēšana nav pabeigta</span><span class="sxs-lookup"><span data-stu-id="45288-105">Installation of the Planning Optimization add-in doesn't complete</span></span>

<span data-ttu-id="45288-106">Plānošanas optimizācijas prasība ir Lifecycle Services (LCS) iespējota, augstas pieejamības vide, 2. līmeņa vai augstāka, (ne OneBox vide) ar Dynamics 365 Supply Chain Management versiju 10.0.7 vai jaunāku.</span><span class="sxs-lookup"><span data-stu-id="45288-106">Planning Optimization requires a Lifecycle Services (LCS) enabled, high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="45288-107">Mēģinot instalēt pievienojumprogrammu OneBox vidē, instalēšana netiks pabeigta.</span><span class="sxs-lookup"><span data-stu-id="45288-107">If you try to install the add-in on a OneBox environment, the installation won't complete.</span></span>

<span data-ttu-id="45288-108">**Labojums**: atceliet instalēšanu un izmantojiet augstas pieejamības vidi, 2. vai augstāku līmeni (ne OneBox vidi).</span><span class="sxs-lookup"><span data-stu-id="45288-108">**Fix**: Cancel the installation and use a high-availability environment, tier 2 or higher (not a OneBox environment).</span></span>

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a><span data-ttu-id="45288-109">Neizdodas pakešuzdevumu plānošana, ja ir iespējota plānošanas optimizācija</span><span class="sxs-lookup"><span data-stu-id="45288-109">Planning of batch jobs fails when Planning Optimization is enabled</span></span>

<span data-ttu-id="45288-110">Iespējojot plānošanas optimizāciju, iebūvētā vispārējās plānošanas programma tiek automātiski atspējota.</span><span class="sxs-lookup"><span data-stu-id="45288-110">When you enable Planning Optimization, the built-in master planning engine is automatically disabled.</span></span> <span data-ttu-id="45288-111">Vispārējās plānošanas pakešuzdevumi, kas tika izveidoti iebūvētajam Supply Chain Management plānošanas dzinējam, neizdosies, ja tie tiks aktivizēti plānošanas optimizācijas iespējošanas laikā.</span><span class="sxs-lookup"><span data-stu-id="45288-111">Master planning batch jobs that were created for the built-in Supply Chain Management planning engine will fail if they are triggered while Planning Optimization is enabled.</span></span> <span data-ttu-id="45288-112">Var tikt parādīts kļūdas ziņojums, piemēram, *Šī operācija izraisīja vispārējo plānošanu, kas netiek atbalstīta, ja ir iespējota plānošanas optimizācija*.</span><span class="sxs-lookup"><span data-stu-id="45288-112">You may receive an error message such as *This operation triggered master planning that isn't supported when Planning Optimization is enabled*.</span></span>

<span data-ttu-id="45288-113">**Labojums**: atceliet visus vispārējās plānošanas pakešuzdevumus, kas tika izveidoti iebūvētajam Supply Chain Management plānošanas dzinējam.</span><span class="sxs-lookup"><span data-stu-id="45288-113">**Fix**: Cancel all master planning batch jobs that were created for the built-in Supply Chain Management planning engine.</span></span>

## <a name="planning-optimization-results-are-different-from-earlier-results"></a><span data-ttu-id="45288-114">Plānošanas optimizācijas rezultāti atšķiras no iepriekšējiem rezultātiem</span><span class="sxs-lookup"><span data-stu-id="45288-114">Planning Optimization results are different from earlier results</span></span>

<span data-ttu-id="45288-115">Plānošanas optimizācija dažās jomās atšķiras no iebūvētā vispārējās plānošanas projekta.</span><span class="sxs-lookup"><span data-stu-id="45288-115">Planning Optimization differs from the built-in master planning design in some areas.</span></span> <span data-ttu-id="45288-116">To var izraisīt arī vēl nepabeigtas funkcijas.</span><span class="sxs-lookup"><span data-stu-id="45288-116">This can also be caused by pending features.</span></span>

<span data-ttu-id="45288-117">**Labojums**: palaist plānošanas optimizācijas saderības analīzi un pēc tam analizēt rezultātus, vienlaikus atsaucoties uz saistīto dokumentāciju, lai izprastu ietekmi.</span><span class="sxs-lookup"><span data-stu-id="45288-117">**Fix**: Run Planning Optimization fit analysis and then analyze the results while referring to the related documentation to understand the impact.</span></span> <span data-ttu-id="45288-118">Papildinformāciju skatiet [Plānošanas optimizācijas ietilpināšanas analīze](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="45288-118">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

## <a name="master-planning-doesnt-respect-the-coverage-time-fence"></a><span data-ttu-id="45288-119">Vispārējā plānošana neievēro vajadzību periodu</span><span class="sxs-lookup"><span data-stu-id="45288-119">Master planning doesn't respect the coverage time fence</span></span>

<span data-ttu-id="45288-120">Tas ir saistīts ar plānošanas optimizācijas vēl nepabeigtu funkciju.</span><span class="sxs-lookup"><span data-stu-id="45288-120">This is caused by a pending feature for Planning Optimization.</span></span>

<span data-ttu-id="45288-121">**Labojums**: kamēr nav pieejama nepabeigtā funkcija, filtrējiet vai dzēsiet plānotos pasūtījumus, lai noņemtu piegādes ieteikumus ārpus vajadzību perioda.</span><span class="sxs-lookup"><span data-stu-id="45288-121">**Fix**: Until the pending feature is available, filter or delete planned orders to remove supply suggestions outside of the coverage time fence.</span></span>

## <a name="cant-enable-planning-optimization"></a><span data-ttu-id="45288-122">Nevar iespējot plānošanas optimizāciju</span><span class="sxs-lookup"><span data-stu-id="45288-122">Can't enable Planning Optimization</span></span>

<span data-ttu-id="45288-123">**Savienojuma statusam** ir jābūt **Savienots** pirms varat iestatīt **Izmantot plānošanas optimizāciju** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="45288-123">The **Connection status** must be **Connected** before you can set **Use Planning Optimization** to **Yes**.</span></span> <span data-ttu-id="45288-124">Papildinformāciju skatiet [Sākt darbu ar Plānošanas optimizāciju ](get-started.md).</span><span class="sxs-lookup"><span data-stu-id="45288-124">For more information, see [Get started with Planning Optimization](get-started.md).</span></span>

<span data-ttu-id="45288-125">**Labojums**: pārliecinieties, ka plānošanas optimizācijas pievienojumprogramma ir veiksmīgi instalēta.</span><span class="sxs-lookup"><span data-stu-id="45288-125">**Fix**: Make sure that the Planning Optimization add-in was installed successfully.</span></span>

## <a name="error-message-is-shown-during-ctp"></a><span data-ttu-id="45288-126">CTP laikā tiek rādīts kļūdas ziņojums</span><span class="sxs-lookup"><span data-stu-id="45288-126">Error message is shown during CTP</span></span>

<span data-ttu-id="45288-127">Ja ir iespējota plānošanas optimizācija, mēģinot palaist pieejams iegādei (CTP) no pārdošanas pasūtījuma, tiks parādīts šāds kļūdas ziņojums: *Šī operācija izraisīja vispārējo plānošanu, kas netiek atbalstīta, ja ir iespējota plānošanas optimizācija*.</span><span class="sxs-lookup"><span data-stu-id="45288-127">If you try to run capable to promise (CTP) from a sales order when Planning Optimization is enabled, you will receive the following error message: *This operation triggered master planning that isn't supported when the Planning Optimization is enabled*.</span></span>

<span data-ttu-id="45288-128">Tas ir saistīts ar nepabeigtu funkciju, kas tiek plānota kā daļa no ražošanas pasūtījumu atbalsta.</span><span class="sxs-lookup"><span data-stu-id="45288-128">This is related to a pending feature that is planned as part of the support for production orders.</span></span>

<span data-ttu-id="45288-129">**Labojums:** izvairieties no CTP aprēķiniem, kad ir iespējota plānošanas optimizācija, līdz ir pieejams CTP atbalsts.</span><span class="sxs-lookup"><span data-stu-id="45288-129">**Fix:** Avoid CTP calculations when Planning Optimization is enabled until CTP support is available.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="45288-130">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="45288-130">Additional resources</span></span>

[<span data-ttu-id="45288-131">Darba sākšana ar plānošanas optimizāciju</span><span class="sxs-lookup"><span data-stu-id="45288-131">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="45288-132">Plānošanas optimizācijas atbilstības analīze</span><span class="sxs-lookup"><span data-stu-id="45288-132">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)
