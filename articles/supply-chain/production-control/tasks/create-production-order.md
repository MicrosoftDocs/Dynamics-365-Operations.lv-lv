---
title: Ražošanas pasūtījuma izveide
description: Šajā procedūrā ir parādīts, kā izveidot ražošanas pasūtījumu.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdTable, ProdBOM, ProdRoute, ProdJournalCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 81caa6693d86c797d8565270094556ae4e103e6a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998682"
---
# <a name="create-a-production-order"></a><span data-ttu-id="34d7c-103">Ražošanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="34d7c-103">Create a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="34d7c-104">Šajā procedūrā ir parādīts, kā izveidot ražošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="34d7c-104">This procedure shows how to create a production order.</span></span> <span data-ttu-id="34d7c-105">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="34d7c-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="34d7c-106">Šī ir pirmā procedūra no septiņām, kurā ir paskaidrots ražošanas pasūtījuma cikls.</span><span class="sxs-lookup"><span data-stu-id="34d7c-106">This is the first procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="34d7c-107">Ražošanas pasūtījuma izveide</span><span class="sxs-lookup"><span data-stu-id="34d7c-107">Create a production order</span></span>
1. <span data-ttu-id="34d7c-108">Pārejiet uz sadaļu Ražošanas kontrole > Ražošanas pasūtījumi > Visi ražošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="34d7c-108">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="34d7c-109">Noklikšķiniet uz Jauns ražošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="34d7c-109">Click New production order.</span></span>
3. <span data-ttu-id="34d7c-110">Laukā Krājuma kods ierakstiet D0001.</span><span class="sxs-lookup"><span data-stu-id="34d7c-110">In the Item number field, type 'D0001'.</span></span>
4. <span data-ttu-id="34d7c-111">Laukā Piegāde ierakstiet datumu.</span><span class="sxs-lookup"><span data-stu-id="34d7c-111">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="34d7c-112">Piegādes datums norāda, kad ir jābeidzas ražošanas pasūtījumam, lai piegāde notiktu laikā.</span><span class="sxs-lookup"><span data-stu-id="34d7c-112">The delivery date indicates when the production order should end in order to deliver on time.</span></span> <span data-ttu-id="34d7c-113">Šo datumu var izmantot plānošanas procesā.</span><span class="sxs-lookup"><span data-stu-id="34d7c-113">This date can be used in the scheduling process.</span></span> <span data-ttu-id="34d7c-114">Piemēram, pasūtījumu varat plānot atpakaļ no piegādes datuma.</span><span class="sxs-lookup"><span data-stu-id="34d7c-114">For example, you can schedule the order backward from the delivery date.</span></span>  
5. <span data-ttu-id="34d7c-115">Daudzuma laukā iestatiet vērtību 20.</span><span class="sxs-lookup"><span data-stu-id="34d7c-115">Set Quantity to '20'.</span></span>
    * <span data-ttu-id="34d7c-116">Piezīme: MK numura laukā automātiski tiek rādīts jebkura pašreizējam krājumam aktīvā MK numurs, bet ražošanas pasūtījumam šo MK varat mainīt, apstiprināto MK versiju sarakstā atlasot kādu aktīvu MK.</span><span class="sxs-lookup"><span data-stu-id="34d7c-116">Note: The BOM number field automatically displays the number of any active BOM for the current item, but you can change the BOM for the production order by selecting an active BOM from the list of approved BOM versions.</span></span>    <span data-ttu-id="34d7c-117">Laukā Maršruta numurs automātiski tiek rādīts jebkura pašreizējam krājumam aktīvā maršruta numurs, bet ražošanas pasūtījumam šo vērtību Maršruts varat mainīt, apstiprināto maršrutu versiju sarakstā atlasot kādu aktīvu maršrutu.</span><span class="sxs-lookup"><span data-stu-id="34d7c-117">The Route number field automatically displays the number of any active Route for the current item, but you can change the Route for the production order by selecting an active Route from the list of approved Route versions.</span></span>  
6. <span data-ttu-id="34d7c-118">Noklikšķiniet uz Izveidot.</span><span class="sxs-lookup"><span data-stu-id="34d7c-118">Click Create.</span></span>

## <a name="validate-the-production-order"></a><span data-ttu-id="34d7c-119">Pārbaudīt ražošanas pasūtījumu</span><span class="sxs-lookup"><span data-stu-id="34d7c-119">Validate the production order</span></span>
1. <span data-ttu-id="34d7c-120">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="34d7c-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="34d7c-121">Noklikšķiniet uz saites tam ražošanas pasūtījuma numuram, ko tikko izveidojāt.</span><span class="sxs-lookup"><span data-stu-id="34d7c-121">Click the link for the production order number that you have just created.</span></span> <span data-ttu-id="34d7c-122">Šādi tiek atvērta lapa ar detalizētu informāciju par pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="34d7c-122">This will open the details page for the order.</span></span>  
2. <span data-ttu-id="34d7c-123">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="34d7c-123">Click Edit.</span></span>
3. <span data-ttu-id="34d7c-124">Laukā Piegāde ierakstiet datumu.</span><span class="sxs-lookup"><span data-stu-id="34d7c-124">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="34d7c-125">Piemēram, ražošanas pasūtījumam varat mainīt piegādes datumu.</span><span class="sxs-lookup"><span data-stu-id="34d7c-125">For example, you can change the delivery date for the production order.</span></span>  
4. <span data-ttu-id="34d7c-126">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="34d7c-126">Click Save.</span></span>
5. <span data-ttu-id="34d7c-127">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="34d7c-127">Close the page.</span></span>

## <a name="update-the-bom"></a><span data-ttu-id="34d7c-128">Atjaunināt MK</span><span class="sxs-lookup"><span data-stu-id="34d7c-128">Update the BOM</span></span>
1. <span data-ttu-id="34d7c-129">Darbības rūtī noklikšķiniet uz vienuma Ražošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="34d7c-129">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="34d7c-130">Noklikšķiniet uz MK.</span><span class="sxs-lookup"><span data-stu-id="34d7c-130">Click BOM.</span></span>
    * <span data-ttu-id="34d7c-131">Atveriet MK lapu, lai pārbaudītu MK datus, kas tika kopēti no noklusējuma datiem, kad tika izveidots ražošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="34d7c-131">Open the BOM page to validate the BOM data that was copied from the default data when the production order was created.</span></span> <span data-ttu-id="34d7c-132">Šajā procedūrā jums ir jāatjaunina MK daudzums.</span><span class="sxs-lookup"><span data-stu-id="34d7c-132">In this procedure, you need to update the quantity for a BOM.</span></span>  
3. <span data-ttu-id="34d7c-133">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="34d7c-133">Click Edit.</span></span>
4. <span data-ttu-id="34d7c-134">Laukā Daudzums ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="34d7c-134">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="34d7c-135">Mainot daudzumu MK rindā, ražošanas pasūtījumam tiek ietekmēta materiālu patēriņa izmaksu prognoze.</span><span class="sxs-lookup"><span data-stu-id="34d7c-135">Changing the quantity on the BOM line affects the cost estimate of material consumption for the production order.</span></span>  
5. <span data-ttu-id="34d7c-136">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="34d7c-136">Click Save.</span></span>
6. <span data-ttu-id="34d7c-137">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="34d7c-137">Close the page.</span></span>

## <a name="update-the-production-route"></a><span data-ttu-id="34d7c-138">Atjaunināt ražošanas maršrutu</span><span class="sxs-lookup"><span data-stu-id="34d7c-138">Update the production route</span></span>
1. <span data-ttu-id="34d7c-139">Darbības rūtī noklikšķiniet uz vienuma Ražošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="34d7c-139">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="34d7c-140">Noklikšķiniet uz Maršruts.</span><span class="sxs-lookup"><span data-stu-id="34d7c-140">Click Route.</span></span>
    * <span data-ttu-id="34d7c-141">Atveriet lapu Maršruts, lai pārbaudītu ražošanas maršruta datus, kas tika kopēti no noklusējuma datiem, kad tika izveidots pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="34d7c-141">Open the Route page to validate the data of the production route that was copied from the default data when the order was created.</span></span> <span data-ttu-id="34d7c-142">Šajā procedūrā jums ir jāatjaunina daudzums vienai no operācijām ražošanas maršrutā.</span><span class="sxs-lookup"><span data-stu-id="34d7c-142">In this procedure, you need to update the quantity for one of the operations in the production route.</span></span>  
3. <span data-ttu-id="34d7c-143">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="34d7c-143">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="34d7c-144">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="34d7c-144">Click Edit.</span></span>
5. <span data-ttu-id="34d7c-145">Laukā Apstrādes daudz. ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="34d7c-145">In the Process qty. field, enter a number.</span></span>
    * <span data-ttu-id="34d7c-146">Mainot apstrādes laiku, tiek ietekmēts ražošanas pasūtījuma prognozētais maršruta patēriņš un izmaksas.</span><span class="sxs-lookup"><span data-stu-id="34d7c-146">Changing the process time affects the estimated route consumption and the cost of the production order.</span></span>  
6. <span data-ttu-id="34d7c-147">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="34d7c-147">Click Save.</span></span>
7. <span data-ttu-id="34d7c-148">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="34d7c-148">Close the page.</span></span>

