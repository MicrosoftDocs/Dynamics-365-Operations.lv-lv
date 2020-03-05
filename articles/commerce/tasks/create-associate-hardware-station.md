---
title: " Aparatūras stacijas izveide un sasaiste"
description: Šajā procedūrā ir aprakstīts, kā izveidot jaunu aparatūras staciju.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailHardwareStation, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 772ccc44c01d97a07796bd1ee443012448955f49
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023291"
---
# <a name="create-and-associate-a-hardware-station"></a><span data-ttu-id="cf46d-103"> Aparatūras stacijas izveide un sasaiste</span><span class="sxs-lookup"><span data-stu-id="cf46d-103">Create and associate a hardware station</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="cf46d-104">Šajā procedūrā ir aprakstīts, kā izveidot jaunu aparatūras staciju.</span><span class="sxs-lookup"><span data-stu-id="cf46d-104">This procedure walks through how to create a new hardware station.</span></span> <span data-ttu-id="cf46d-105">Jauns aparatūras profils tiek izveidots un izmantots, lai jaunas aparatūras stacijas pievienotu iepriekš definētajam veikalam (kanālam).</span><span class="sxs-lookup"><span data-stu-id="cf46d-105">A new hardware profile will be created and used to add new hardware stations to a pre-defined store (channel).</span></span> <span data-ttu-id="cf46d-106">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="cf46d-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="cf46d-107">Dodieties uz Komercijas rekvizīti > Kanāli >..</span><span class="sxs-lookup"><span data-stu-id="cf46d-107">Go to Commerce essentials > Channels > ..</span></span> <span data-ttu-id="cf46d-108">> ..</span><span class="sxs-lookup"><span data-stu-id="cf46d-108">> ..</span></span> <span data-ttu-id="cf46d-109">> ..</span><span class="sxs-lookup"><span data-stu-id="cf46d-109">> ..</span></span> <span data-ttu-id="cf46d-110">> Aparatūras stacijas profili.</span><span class="sxs-lookup"><span data-stu-id="cf46d-110">> Hardware station profiles.</span></span>
2. <span data-ttu-id="cf46d-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="cf46d-111">Click New.</span></span>
3. <span data-ttu-id="cf46d-112">Laukā Aparatūras stacijas ID ierakstiet TestHWProfile.</span><span class="sxs-lookup"><span data-stu-id="cf46d-112">In the Hardware station ID field, type 'TestHWProfile'.</span></span>
4. <span data-ttu-id="cf46d-113">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="cf46d-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="cf46d-114">Laukā Porta numurs ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="cf46d-114">In the Port number field, enter a number.</span></span>
6. <span data-ttu-id="cf46d-115">Laukā Aparatūras profils noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="cf46d-115">In the Hardware profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="cf46d-116">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="cf46d-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="cf46d-117">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="cf46d-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="cf46d-118">Laukā Pakotnes nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="cf46d-118">In the Package name field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="cf46d-119">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="cf46d-119">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="cf46d-120">Šis ir standarta pakotne, kurā tiek nodrošināta jauna vide.</span><span class="sxs-lookup"><span data-stu-id="cf46d-120">This is the standard package that comes with a new environment.</span></span> <span data-ttu-id="cf46d-121">Versijas numurs var atšķirties.</span><span class="sxs-lookup"><span data-stu-id="cf46d-121">The version number may vary.</span></span>  
11. <span data-ttu-id="cf46d-122">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="cf46d-122">Click Save.</span></span>
12. <span data-ttu-id="cf46d-123">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="cf46d-123">Close the page.</span></span>
13. <span data-ttu-id="cf46d-124">Dodieties uz Retail un Commerce > Kanāli > Visi mazumtirdzniecības veikali.</span><span class="sxs-lookup"><span data-stu-id="cf46d-124">Go to Retail and Commerce > Channels > All stores.</span></span>
14. <span data-ttu-id="cf46d-125">Sarakstā atlasiet 17. rindu.</span><span class="sxs-lookup"><span data-stu-id="cf46d-125">In the list, select row 17.</span></span>
    * <span data-ttu-id="cf46d-126">Ja tiek izmantoti demonstrācijas uzņēmuma “USRT” dati, šis ir Houston veikals.</span><span class="sxs-lookup"><span data-stu-id="cf46d-126">If you are using the USRT demo data company, this is the Houston store.</span></span>  
15. <span data-ttu-id="cf46d-127">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="cf46d-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="cf46d-128">Pārslēdziet sadaļas Aparatūras stacijas paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="cf46d-128">Toggle the expansion of the Hardware stations section.</span></span>
17. <span data-ttu-id="cf46d-129">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="cf46d-129">Click Add.</span></span>
18. <span data-ttu-id="cf46d-130">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="cf46d-130">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="cf46d-131">Laukā Profila ID noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanas logu.</span><span class="sxs-lookup"><span data-stu-id="cf46d-131">In the Profile ID field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="cf46d-132">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="cf46d-132">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="cf46d-133">Tam ir jābūt jaunajam aparatūras stacijas profilam, kas tika izveidots iepriekšējās darbībās.</span><span class="sxs-lookup"><span data-stu-id="cf46d-133">This must be the new hardware station profile that was created in the previous steps.</span></span>  
21. <span data-ttu-id="cf46d-134">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="cf46d-134">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="cf46d-135">Laukā Resursdatora nosaukums ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="cf46d-135">In the Host name field, type a value.</span></span>
23. <span data-ttu-id="cf46d-136">Laukā EFT termināļa ID ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="cf46d-136">In the EFT terminal ID field, type a value.</span></span>
24. <span data-ttu-id="cf46d-137">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="cf46d-137">Click Save.</span></span>
