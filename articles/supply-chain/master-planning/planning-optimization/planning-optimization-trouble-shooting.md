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
ms.openlocfilehash: 39583c244f09f54551d560e8b1dd9f1a5a1590cc
ms.sourcegitcommit: 72f70c81176e86cda714a4712525f73514c895b7
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/16/2021
ms.locfileid: "5457333"
---
# <a name="troubleshoot-planning-optimization"></a><span data-ttu-id="c1a16-103">Plānošanas optimizācijas problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="c1a16-103">Troubleshoot Planning Optimization</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c1a16-104">Šajā tēmā ir aprakstīts, kā labot tipiskas problēmas, kas var rasties, strādājot ar plānošanas optimizāciju.</span><span class="sxs-lookup"><span data-stu-id="c1a16-104">This topic describes how to fix common issues that you might encounter while working with Planning Optimization.</span></span>

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a><span data-ttu-id="c1a16-105">Plānošanas optimizācijas pievienojumprogrammas instalēšana nav pabeigta</span><span class="sxs-lookup"><span data-stu-id="c1a16-105">Installation of the Planning Optimization add-in doesn't complete</span></span>

<span data-ttu-id="c1a16-106">Plānošanas optimizācijas prasība ir Lifecycle Services (LCS) iespējota, augstas pieejamības vide, 2. līmeņa vai augstāka, (ne OneBox vide) ar Dynamics 365 Supply Chain Management versiju 10.0.7 vai jaunāku.</span><span class="sxs-lookup"><span data-stu-id="c1a16-106">Planning Optimization requires a Lifecycle Services (LCS) enabled, high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="c1a16-107">Mēģinot instalēt pievienojumprogrammu OneBox vidē, instalēšana netiks pabeigta.</span><span class="sxs-lookup"><span data-stu-id="c1a16-107">If you try to install the add-in on a OneBox environment, the installation won't complete.</span></span>

<span data-ttu-id="c1a16-108">**Labojums**: atceliet instalēšanu un izmantojiet augstas pieejamības vidi, 2. vai augstāku līmeni (ne OneBox vidi).</span><span class="sxs-lookup"><span data-stu-id="c1a16-108">**Fix**: Cancel the installation and use a high-availability environment, tier 2 or higher (not a OneBox environment).</span></span>

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a><span data-ttu-id="c1a16-109">Neizdodas pakešuzdevumu plānošana, ja ir iespējota plānošanas optimizācija</span><span class="sxs-lookup"><span data-stu-id="c1a16-109">Planning of batch jobs fails when Planning Optimization is enabled</span></span>

<span data-ttu-id="c1a16-110">Iespējojot plānošanas optimizāciju, iebūvētā vispārējās plānošanas programma tiek automātiski atspējota.</span><span class="sxs-lookup"><span data-stu-id="c1a16-110">When you enable Planning Optimization, the built-in master planning engine is automatically disabled.</span></span> <span data-ttu-id="c1a16-111">Vispārējās plānošanas pakešuzdevumi, kas tika izveidoti iebūvētajam Supply Chain Management plānošanas dzinējam, neizdosies, ja tie tiks aktivizēti plānošanas optimizācijas iespējošanas laikā.</span><span class="sxs-lookup"><span data-stu-id="c1a16-111">Master planning batch jobs that were created for the built-in Supply Chain Management planning engine will fail if they are triggered while Planning Optimization is enabled.</span></span> <span data-ttu-id="c1a16-112">Var tikt parādīts kļūdas ziņojums, piemēram, *Šī operācija izraisīja vispārējo plānošanu, kas netiek atbalstīta, ja ir iespējota plānošanas optimizācija*.</span><span class="sxs-lookup"><span data-stu-id="c1a16-112">You may receive an error message such as *This operation triggered master planning that isn't supported when Planning Optimization is enabled*.</span></span>

<span data-ttu-id="c1a16-113">**Labojums**: atceliet visus vispārējās plānošanas pakešuzdevumus, kas tika izveidoti iebūvētajam Supply Chain Management plānošanas dzinējam.</span><span class="sxs-lookup"><span data-stu-id="c1a16-113">**Fix**: Cancel all master planning batch jobs that were created for the built-in Supply Chain Management planning engine.</span></span>

## <a name="planning-optimization-results-are-different-from-earlier-results"></a><span data-ttu-id="c1a16-114">Plānošanas optimizācijas rezultāti atšķiras no iepriekšējiem rezultātiem</span><span class="sxs-lookup"><span data-stu-id="c1a16-114">Planning Optimization results are different from earlier results</span></span>

<span data-ttu-id="c1a16-115">Plānošanas optimizācija dažās jomās atšķiras no iebūvētā vispārējās plānošanas projekta.</span><span class="sxs-lookup"><span data-stu-id="c1a16-115">Planning Optimization differs from the built-in master planning design in some areas.</span></span> <span data-ttu-id="c1a16-116">To var izraisīt arī vēl nepabeigtas funkcijas.</span><span class="sxs-lookup"><span data-stu-id="c1a16-116">This can also be caused by pending features.</span></span>

<span data-ttu-id="c1a16-117">**Labojums**: palaist plānošanas optimizācijas saderības analīzi un pēc tam analizēt rezultātus, vienlaikus atsaucoties uz saistīto dokumentāciju, lai izprastu ietekmi.</span><span class="sxs-lookup"><span data-stu-id="c1a16-117">**Fix**: Run Planning Optimization fit analysis and then analyze the results while referring to the related documentation to understand the impact.</span></span> <span data-ttu-id="c1a16-118">Papildinformāciju skatiet [Plānošanas optimizācijas ietilpināšanas analīze](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c1a16-118">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

## <a name="cant-enable-planning-optimization"></a><span data-ttu-id="c1a16-119">Nevar iespējot plānošanas optimizāciju</span><span class="sxs-lookup"><span data-stu-id="c1a16-119">Can't enable Planning Optimization</span></span>

<span data-ttu-id="c1a16-120">**Savienojuma statusam** ir jābūt **Savienots** pirms varat iestatīt **Izmantot plānošanas optimizāciju** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="c1a16-120">The **Connection status** must be **Connected** before you can set **Use Planning Optimization** to **Yes**.</span></span> <span data-ttu-id="c1a16-121">Papildinformāciju skatiet [Sākt darbu ar Plānošanas optimizāciju ](get-started.md).</span><span class="sxs-lookup"><span data-stu-id="c1a16-121">For more information, see [Get started with Planning Optimization](get-started.md).</span></span>

<span data-ttu-id="c1a16-122">**Labojums**: pārliecinieties, ka plānošanas optimizācijas pievienojumprogramma ir veiksmīgi instalēta.</span><span class="sxs-lookup"><span data-stu-id="c1a16-122">**Fix**: Make sure that the Planning Optimization add-in was installed successfully.</span></span>

## <a name="error-message-is-shown-during-ctp"></a><span data-ttu-id="c1a16-123">CTP laikā tiek rādīts kļūdas ziņojums</span><span class="sxs-lookup"><span data-stu-id="c1a16-123">Error message is shown during CTP</span></span>

<span data-ttu-id="c1a16-124">Ja ir iespējota plānošanas optimizācija, mēģinot palaist pieejams iegādei (CTP) no pārdošanas pasūtījuma, tiks parādīts šāds kļūdas ziņojums: *Šī operācija izraisīja vispārējo plānošanu, kas netiek atbalstīta, ja ir iespējota plānošanas optimizācija*.</span><span class="sxs-lookup"><span data-stu-id="c1a16-124">If you try to run capable to promise (CTP) from a sales order when Planning Optimization is enabled, you will receive the following error message: *This operation triggered master planning that isn't supported when the Planning Optimization is enabled*.</span></span>

<span data-ttu-id="c1a16-125">Tas ir saistīts ar nepabeigtu funkciju, kas tiek plānota kā daļa no ražošanas pasūtījumu atbalsta.</span><span class="sxs-lookup"><span data-stu-id="c1a16-125">This is related to a pending feature that is planned as part of the support for production orders.</span></span>

<span data-ttu-id="c1a16-126">**Labojums:** izvairieties no CTP aprēķiniem, kad ir iespējota plānošanas optimizācija, līdz ir pieejams CTP atbalsts.</span><span class="sxs-lookup"><span data-stu-id="c1a16-126">**Fix:** Avoid CTP calculations when Planning Optimization is enabled until CTP support is available.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c1a16-127">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="c1a16-127">Additional resources</span></span>

[<span data-ttu-id="c1a16-128">Darba sākšana ar plānošanas optimizāciju</span><span class="sxs-lookup"><span data-stu-id="c1a16-128">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="c1a16-129">Plānošanas optimizācijas atbilstības analīze</span><span class="sxs-lookup"><span data-stu-id="c1a16-129">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]