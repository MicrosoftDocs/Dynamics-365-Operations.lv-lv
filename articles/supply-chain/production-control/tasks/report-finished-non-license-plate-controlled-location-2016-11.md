---
title: Reģistrēt kā pabeigtu novietojumā, kas nav atkarīgs no numura zīmes (programma, 2016. gada maijs)
description: Šajā uzdevuma ceļvedī aprakstīts piemērs, kā norādīt darbu kā pabeigtu novietojumā, kas nav atkarīgs no numura zīmes.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdParmCostEstimation, ProdParmStartUp, ProdParmReportFinished, WHSWorkTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 180035668d9c8a03b83f669af7459725eecc8def
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981185"
---
# <a name="report-as-finished-to-a-non-license-plate-controlled-location--application-may-2016"></a><span data-ttu-id="f4bfe-103">Reģistrēt kā pabeigtu novietojumā, kas nav atkarīgs no numura zīmes (programma, 2016. gada maijs)</span><span class="sxs-lookup"><span data-stu-id="f4bfe-103">Report as finished to a non-license plate controlled location  (Application, May 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f4bfe-104">Šajā uzdevuma ceļvedī aprakstīts piemērs, kā norādīt darbu kā pabeigtu novietojumā, kas nav atkarīgs no numura zīmes.</span><span class="sxs-lookup"><span data-stu-id="f4bfe-104">This task guide shows an example of reporting as finished to a location that isn't license plate–controlled.</span></span> <span data-ttu-id="f4bfe-105">Šim uzdevumam ir nepieciešama piemērojama darba politika.</span><span class="sxs-lookup"><span data-stu-id="f4bfe-105">An applicable work policy is the prerequisite for this task.</span></span> <span data-ttu-id="f4bfe-106">Iepriekšējā uzdevuma ceļvedī bija aprakstīta darba politikas iestatīšana.</span><span class="sxs-lookup"><span data-stu-id="f4bfe-106">A previous task guide showed the setup of the work policy.</span></span> <span data-ttu-id="f4bfe-107">Šim uzdevumu ceļvedim ir nepieciešama lietojumprogrammas Dynamics AX versija 7.0.1 vai jaunāka versija.</span><span class="sxs-lookup"><span data-stu-id="f4bfe-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>




## <a name="set-up-an-output-location"></a><span data-ttu-id="f4bfe-108">Iestatīt izvades novietojumu</span><span class="sxs-lookup"><span data-stu-id="f4bfe-108">Set up an output location</span></span>
1. <span data-ttu-id="f4bfe-109">Dodieties uz Organizācijas administrēšana > Resursi > Resursu grupas.</span><span class="sxs-lookup"><span data-stu-id="f4bfe-109">Go to Organization administration > Resources > Resource groups.</span></span>
2. <span data-ttu-id="f4bfe-110">Sarakstā atlasiet resursu grupu “5102”.</span><span class="sxs-lookup"><span data-stu-id="f4bfe-110">In the list, select resource group '5102'.</span></span>
3. <span data-ttu-id="f4bfe-111">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="f4bfe-111">Click Edit.</span></span>
4. <span data-ttu-id="f4bfe-112">Laukā Izvades noliktava ievadiet “51”.</span><span class="sxs-lookup"><span data-stu-id="f4bfe-112">In the Output warehouse field, enter '51'.</span></span>
5. <span data-ttu-id="f4bfe-113">Laukā Izvades vieta ievadiet “001”.</span><span class="sxs-lookup"><span data-stu-id="f4bfe-113">In the Output location field, enter '001'.</span></span>
    * <span data-ttu-id="f4bfe-114">Novietojums 001 nav no numura zīmes atkarīgs novietojums.</span><span class="sxs-lookup"><span data-stu-id="f4bfe-114">Location 001 isn't a license plate–controlled location.</span></span> <span data-ttu-id="f4bfe-115">Novietojumu, kas nav atkarīgs no numura zīmes, var iestatīt tikai tad, ja attiecīgajam novietojumam ir piemērojama darba politika.</span><span class="sxs-lookup"><span data-stu-id="f4bfe-115">You can set up a non–license plate output location only if an applicable work policy exists for the location.</span></span>  

## <a name="create-a-production-order-and-report-it-as-finished"></a><span data-ttu-id="f4bfe-116">Izveidot ražošanas pasūtījumu un norādīt to kā pabeigtu</span><span class="sxs-lookup"><span data-stu-id="f4bfe-116">Create a production order and report it as finished</span></span>
1. <span data-ttu-id="f4bfe-117">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f4bfe-117">Close the page.</span></span>
2. <span data-ttu-id="f4bfe-118">Pārejiet uz sadaļu Ražošanas kontrole > Ražošanas pasūtījumi > Visi ražošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="f4bfe-118">Go to Production control > Production orders > All production orders.</span></span>
3. <span data-ttu-id="f4bfe-119">Noklikšķiniet uz Jauns ražošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="f4bfe-119">Click New production order.</span></span>
4. <span data-ttu-id="f4bfe-120">Laukā Krājuma kods ievadiet “L0101”.</span><span class="sxs-lookup"><span data-stu-id="f4bfe-120">In the Item number field, enter 'L0101'.</span></span>
5. <span data-ttu-id="f4bfe-121">Noklikšķiniet uz Izveidot.</span><span class="sxs-lookup"><span data-stu-id="f4bfe-121">Click Create.</span></span>
6. <span data-ttu-id="f4bfe-122">Darbību rūtī noklikšķiniet uz Ražošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="f4bfe-122">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="f4bfe-123">Noklikšķiniet uz Novērtējums.</span><span class="sxs-lookup"><span data-stu-id="f4bfe-123">Click Estimate.</span></span>
8. <span data-ttu-id="f4bfe-124">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="f4bfe-124">Click OK.</span></span>
9. <span data-ttu-id="f4bfe-125">Noklikšķiniet uz Sākt.</span><span class="sxs-lookup"><span data-stu-id="f4bfe-125">Click Start.</span></span>
10. <span data-ttu-id="f4bfe-126">Noklikšķiniet uz cilnes Vispārīgie iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="f4bfe-126">Click the General tab.</span></span>
11. <span data-ttu-id="f4bfe-127">Laukā Automātisks MK patēriņš atlasiet "Nekad".</span><span class="sxs-lookup"><span data-stu-id="f4bfe-127">In the Automatic BOM consumption field, select 'Never'.</span></span>
12. <span data-ttu-id="f4bfe-128">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="f4bfe-128">Click OK.</span></span>
13. <span data-ttu-id="f4bfe-129">Noklikšķiniet uz Ziņot kā pabeigtu.</span><span class="sxs-lookup"><span data-stu-id="f4bfe-129">Click Report as finished.</span></span>
14. <span data-ttu-id="f4bfe-130">Noklikšķiniet uz cilnes Vispārīgie iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="f4bfe-130">Click the General tab.</span></span>
15. <span data-ttu-id="f4bfe-131">Laukā Pieņemt kļūdu atlasiet vienumu Jā.</span><span class="sxs-lookup"><span data-stu-id="f4bfe-131">Select Yes in the Accept error field.</span></span>
16. <span data-ttu-id="f4bfe-132">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="f4bfe-132">Click OK.</span></span>
17. <span data-ttu-id="f4bfe-133">Darbību rūtī noklikšķiniet uz Noliktava.</span><span class="sxs-lookup"><span data-stu-id="f4bfe-133">On the Action Pane, click Warehouse.</span></span>
18. <span data-ttu-id="f4bfe-134">Noklikšķiniet uz Detalizēta informācija par darbu.</span><span class="sxs-lookup"><span data-stu-id="f4bfe-134">Click Work details.</span></span>
    * <span data-ttu-id="f4bfe-135">Kad ražošanas pasūtījums tika norādīts kā pabeigts, netika ģenerēts darbs izvietošanai.</span><span class="sxs-lookup"><span data-stu-id="f4bfe-135">When the production order was reported as finished, no work was generated for put-away.</span></span> <span data-ttu-id="f4bfe-136">Tas notiek tāpēc, ka ir definēta darba politika, kas neļauj ģenerēt darbu, kad produkts L0101 tiek norādīts kā pabeigts novietojumā 001.</span><span class="sxs-lookup"><span data-stu-id="f4bfe-136">This occurs because a work policy is defined that prevents work from being generated when product L0101 is reported as finished to location 001.</span></span>  

