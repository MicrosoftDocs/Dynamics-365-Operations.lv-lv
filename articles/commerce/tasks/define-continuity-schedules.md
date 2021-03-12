---
title: Nepārtrauktības grafiku definēšana
description: Šajā tēmā aprakstīts, kā iestatīt nepārtrauktības programmu (zināma arī kā atkārtošanās pasūtījumi).
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRContinuitySchedule, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 37c4022cb2f2acf567437c821946ad452ba8f37c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972334"
---
# <a name="define-continuity-schedules"></a><span data-ttu-id="5180e-103">Nepārtrauktības grafiku definēšana</span><span class="sxs-lookup"><span data-stu-id="5180e-103">Define continuity schedules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5180e-104">Šajā tēmā aprakstīts, kā iestatīt nepārtrauktības programmu (zināma arī kā atkārtošanās pasūtījumi).</span><span class="sxs-lookup"><span data-stu-id="5180e-104">This topic walks through setting up a continuity program (otherwise known as reoccurring orders).</span></span> <span data-ttu-id="5180e-105">Šajā tēmā tiek izmantoti uzņēmuma USRT demonstrācijas dati.</span><span class="sxs-lookup"><span data-stu-id="5180e-105">This topic uses company USRT in the demo data.</span></span>


## <a name="create-continuity-program"></a><span data-ttu-id="5180e-106">Nepārtrauktības programmas izveide</span><span class="sxs-lookup"><span data-stu-id="5180e-106">Create continuity program</span></span>
1. <span data-ttu-id="5180e-107">Dodieties uz Mazumtirdzniecība un komercija > Nepārtrauktība > Nepārtrauktības programmas.</span><span class="sxs-lookup"><span data-stu-id="5180e-107">Go to Retail and Commerce > Continuity > Continuity programs.</span></span>
2. <span data-ttu-id="5180e-108">Klikšķiniet Jauns.</span><span class="sxs-lookup"><span data-stu-id="5180e-108">Click New.</span></span>
3. <span data-ttu-id="5180e-109">Grafika ID laukā ierakstiet Nepārtrauktības grafika ID.</span><span class="sxs-lookup"><span data-stu-id="5180e-109">In the Schedule ID field, type the continuity schedule ID.</span></span>
4. <span data-ttu-id="5180e-110">Laukā Pasūtījuma sākums atlasiet "Pirmais notikums".</span><span class="sxs-lookup"><span data-stu-id="5180e-110">In the Order start field, select 'First event'.</span></span>
    * <span data-ttu-id="5180e-111">Ja debitors nepārtrauktības programmā veic jaunu pasūtījumu, ir divas preces nosūtīšanas opcijas: 1.</span><span class="sxs-lookup"><span data-stu-id="5180e-111">If a customer places a new order for the continuity program, there are two options for which product will be shipped:  1.</span></span> <span data-ttu-id="5180e-112">Pirmais notikums: tiek nosūtīta pirmā prece nepārtrauktības programmā.</span><span class="sxs-lookup"><span data-stu-id="5180e-112">First event: the first product in the continuity program will be shipped.</span></span>  <span data-ttu-id="5180e-113">2.</span><span class="sxs-lookup"><span data-stu-id="5180e-113">2.</span></span> <span data-ttu-id="5180e-114">Pašreizējais notikums: tiek nosūtīta pašreizējā prece.</span><span class="sxs-lookup"><span data-stu-id="5180e-114">Current event: the current product will be shipped.</span></span> <span data-ttu-id="5180e-115">Piemēram,</span><span class="sxs-lookup"><span data-stu-id="5180e-115">For example.</span></span> <span data-ttu-id="5180e-116">trīs mēnešus esot programmā, klients saņems trešo programmu.</span><span class="sxs-lookup"><span data-stu-id="5180e-116">three months into the program, the customer will receive the third in the program.</span></span>  
5. <span data-ttu-id="5180e-117">Atlasiet 'Jā', lai uzvedinātu pasūtījuma sākuma datumu.</span><span class="sxs-lookup"><span data-stu-id="5180e-117">Select 'Yes' to prompt for the order start date.</span></span>
6. <span data-ttu-id="5180e-118">Noklikšķiniet uz Pievienot rindu.</span><span class="sxs-lookup"><span data-stu-id="5180e-118">Click Add line.</span></span>
7. <span data-ttu-id="5180e-119">Laukā Krājuma numurs ievadiet krājuma numuru pirmajai precei ('0013').</span><span class="sxs-lookup"><span data-stu-id="5180e-119">In the Item number field, type the item number for the first product ('0013').</span></span>
8. <span data-ttu-id="5180e-120">Ierakstiet 'CP'.</span><span class="sxs-lookup"><span data-stu-id="5180e-120">Type 'CP'.</span></span>
9. <span data-ttu-id="5180e-121">Ievadiet datumu, kad pirmā prece būs pieejama pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="5180e-121">Enter the date when the first product will be available for order.</span></span>
10. <span data-ttu-id="5180e-122">Noklikšķiniet uz Pievienot rindu.</span><span class="sxs-lookup"><span data-stu-id="5180e-122">Click Add line.</span></span>
11. <span data-ttu-id="5180e-123">Laukā Krājuma kods ierakstiet 0014.</span><span class="sxs-lookup"><span data-stu-id="5180e-123">In the Item number field, type '0014'.</span></span>
12. <span data-ttu-id="5180e-124">Laukā Datumu intervāla kods, notīriet vērtību, lai lauks ir tukšs.</span><span class="sxs-lookup"><span data-stu-id="5180e-124">In the Date interval code field, clear the value so the field is empty.</span></span>
    * <span data-ttu-id="5180e-125">Lai veiktu šo procedūru, notīriet datumu intervālu.</span><span class="sxs-lookup"><span data-stu-id="5180e-125">For this procedure, clear the date interval.</span></span> <span data-ttu-id="5180e-126">Jūs varat iestatīt datumu kā inkrementālu no pirmā vienuma sākuma datuma.</span><span class="sxs-lookup"><span data-stu-id="5180e-126">You'll set the date as incremental from the start date of the first item.</span></span>  
13. <span data-ttu-id="5180e-127">Šeit var ievadīt intervālu, kādā preces tiek izsūtītas.</span><span class="sxs-lookup"><span data-stu-id="5180e-127">Here you'll enter the interval at which the products are shipped.</span></span> <span data-ttu-id="5180e-128">Ierakstiet '30'.</span><span class="sxs-lookup"><span data-stu-id="5180e-128">Type '30'.</span></span>
    * <span data-ttu-id="5180e-129">Mēneša programmai, jums būs jāievada 30 dienu intervālu.</span><span class="sxs-lookup"><span data-stu-id="5180e-129">For a monthly program, you'll enter 30 days for the interval.</span></span>  
14. <span data-ttu-id="5180e-130">Noklikšķiniet uz Pievienot rindu.</span><span class="sxs-lookup"><span data-stu-id="5180e-130">Click Add line.</span></span>
15. <span data-ttu-id="5180e-131">Laukā Krājuma kods ierakstiet 0015.</span><span class="sxs-lookup"><span data-stu-id="5180e-131">In the Item number field, type '0015'.</span></span>
16. <span data-ttu-id="5180e-132">Ierakstiet 'Beigas'.</span><span class="sxs-lookup"><span data-stu-id="5180e-132">Type 'End'.</span></span>
17. <span data-ttu-id="5180e-133">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="5180e-133">Click Save.</span></span>

## <a name="assign-to-continuity-item"></a><span data-ttu-id="5180e-134">Piešķirt nepārtrauktības krājumam</span><span class="sxs-lookup"><span data-stu-id="5180e-134">Assign to continuity item</span></span>
1. <span data-ttu-id="5180e-135">Pārejiet uz sadaļu Preču informācijas pārvaldība > Preces > Izlaistās preces.</span><span class="sxs-lookup"><span data-stu-id="5180e-135">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="5180e-136">Atlasiet vienumu '0016'.</span><span class="sxs-lookup"><span data-stu-id="5180e-136">Select item '0016'.</span></span>
    * <span data-ttu-id="5180e-137">Lai veiktu šo procedūru, jums būs jāatlasa krājuma numuru 0016.</span><span class="sxs-lookup"><span data-stu-id="5180e-137">For this procedure, you'll select item number 0016.</span></span> <span data-ttu-id="5180e-138">Parasti Jums būs izveidota izlaista prece, kurai ir pielietota papildu nepārtrauktības biznesa loģika, ja tā ir izvietota pārdošanas pasūtījumā zvanu centrā.</span><span class="sxs-lookup"><span data-stu-id="5180e-138">Normally, you'll have created a released product that has additional continuity business logic applied when it's placed on a sales order in call center.</span></span>  
3. <span data-ttu-id="5180e-139">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="5180e-139">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="5180e-140">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="5180e-140">Click Edit.</span></span>
5. <span data-ttu-id="5180e-141">Izvērsiet vai sakļaujiet sadaļu Pārdot.</span><span class="sxs-lookup"><span data-stu-id="5180e-141">Expand or collapse the Sell section.</span></span>
6. <span data-ttu-id="5180e-142">Šeit jums jāievada nepārtrauktība programma, kuru pārstāv šis krājums.</span><span class="sxs-lookup"><span data-stu-id="5180e-142">Here you'll enter the continuity program that this item represents.</span></span> <span data-ttu-id="5180e-143">Ierakstiet Grafika ID, ko izveidojāt iepriekš.</span><span class="sxs-lookup"><span data-stu-id="5180e-143">Type the Schedule ID you created earlier.</span></span>
    * <span data-ttu-id="5180e-144">Ja šī prece tiek pārdota zvanu centrā, papildu biznesa loģika tiek pielietota no atlasītās nepārtrauktības programmas.</span><span class="sxs-lookup"><span data-stu-id="5180e-144">When this item is sold in a call center, additional business logic is applied from the selected continuity program.</span></span>  
7. <span data-ttu-id="5180e-145">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="5180e-145">Click Save.</span></span>

